---
title: Gérer le chiffrement de messages Office 365
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 5/8/2019
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Une fois que vous avez terminé la configuration chiffrement de messages Office 365 (OME), découvrez comment personnaliser votre déploiement de plusieurs façons.
ms.openlocfilehash: a2b3dde44ea541deb41eeb9d55d5ed745fa6c719
ms.sourcegitcommit: 07e536f1a6e335f114da55048844e4a866fe731b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "52650983"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="c37d8-103">Gérer le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="c37d8-103">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="c37d8-104">Une fois que vous avez terminé la configuration chiffrement de messages Office 365 (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs manières.</span><span class="sxs-lookup"><span data-stu-id="c37d8-104">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in several ways.</span></span> <span data-ttu-id="c37d8-105">Par exemple, vous pouvez configurer s’il faut activer  les codes de passe à temps partiel, afficher le bouton Chiffrer dans Outlook sur le web, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c37d8-105">For example, you can configure whether to enable one-time pass codes, display the **Encrypt** button in Outlook on the web, and more.</span></span> <span data-ttu-id="c37d8-106">Les tâches de cet article décrivent comment.</span><span class="sxs-lookup"><span data-stu-id="c37d8-106">The tasks in this article describe how.</span></span>

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="c37d8-107">Déterminer si les destinataires des comptes Google, Yahoo et Microsoft peuvent utiliser ces comptes pour se chiffrement de messages Office 365 portail</span><span class="sxs-lookup"><span data-stu-id="c37d8-107">Manage whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="c37d8-108">Lorsque vous définissez les nouvelles fonctionnalités chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires extérieurs à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c37d8-108">When you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your organization.</span></span> <span data-ttu-id="c37d8-109">Si le destinataire utilise un *ID social* tel qu’un compte Google, un compte Yahoo ou un compte Microsoft, le destinataire peut se connecter au portail OME avec un ID social.</span><span class="sxs-lookup"><span data-stu-id="c37d8-109">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal with a social ID.</span></span> <span data-ttu-id="c37d8-110">Si vous le souhaitez, vous pouvez choisir de ne pas autoriser les destinataires à utiliser des ID de réseau social pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="c37d8-110">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="c37d8-111">Pour déterminer si les destinataires peuvent utiliser des ID sociaux pour se connecter au portail OME</span><span class="sxs-lookup"><span data-stu-id="c37d8-111">To manage whether recipients can use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="c37d8-112">[Connecter à Exchange Online à l’aide de Remote PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-112">[Connect to Exchange Online Using Remote PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-113">Exécutez lSet-OMEConfiguration cmdlet avec le paramètre SocialIdSignIn comme suit :</span><span class="sxs-lookup"><span data-stu-id="c37d8-113">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   <span data-ttu-id="c37d8-114">Par exemple, pour désactiver les ID sociaux :</span><span class="sxs-lookup"><span data-stu-id="c37d8-114">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="c37d8-115">Pour activer les ID sociaux :</span><span class="sxs-lookup"><span data-stu-id="c37d8-115">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a><span data-ttu-id="c37d8-116">Gérer l’utilisation de codes de passe à usage unique pour le portail chiffrement de messages Office 365 web</span><span class="sxs-lookup"><span data-stu-id="c37d8-116">Manage the use of one-time pass codes for the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="c37d8-117">Si le destinataire d’un message chiffré par OME n’utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien d’affichage web à durée limitée qui lui permet de lire le message.</span><span class="sxs-lookup"><span data-stu-id="c37d8-117">If the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="c37d8-118">Ce lien inclut un code de passe à une seule fois.</span><span class="sxs-lookup"><span data-stu-id="c37d8-118">This link includes a one-time pass code.</span></span> <span data-ttu-id="c37d8-119">En tant qu’administrateur, vous pouvez décider si les destinataires peuvent utiliser des codes de passe à usage unique pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="c37d8-119">As an administrator, you can decide if recipients can use one-time pass codes to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a><span data-ttu-id="c37d8-120">Pour savoir si OME génère des codes de passe à temps partiel</span><span class="sxs-lookup"><span data-stu-id="c37d8-120">To manage whether OME generates one-time pass codes</span></span>
  
1. <span data-ttu-id="c37d8-121">Utilisez un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c37d8-121">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c37d8-122">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-122">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-123">Exécutez la cmdlet Set-OMEConfiguration avec le paramètre OTPEnabled :</span><span class="sxs-lookup"><span data-stu-id="c37d8-123">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="c37d8-124">Par exemple, pour désactiver les codes de passe à une seule heure :</span><span class="sxs-lookup"><span data-stu-id="c37d8-124">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="c37d8-125">Pour activer les codes de passe à une seule fois :</span><span class="sxs-lookup"><span data-stu-id="c37d8-125">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-encrypt-button-in-outlook-on-the-web"></a><span data-ttu-id="c37d8-126">Gérer l’affichage du bouton Chiffrer dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="c37d8-126">Manage the display of the Encrypt button in Outlook on the web</span></span>

<span data-ttu-id="c37d8-127">En tant qu’administrateur, vous pouvez décider d’afficher ou non ce bouton pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="c37d8-127">As an administrator, you can manage whether to display this button to end users.</span></span>
  
### <a name="to-manage-whether-the-encrypt-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="c37d8-128">Pour déterminer si le bouton Chiffrer apparaît dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="c37d8-128">To manage whether the Encrypt button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="c37d8-129">Utilisez un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c37d8-129">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c37d8-130">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-130">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-131">Exécutez lSet-IRMConfiguration cmdlet avec le paramètre -SimplifiedClientAccessEnabled :</span><span class="sxs-lookup"><span data-stu-id="c37d8-131">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="c37d8-132">Par exemple, pour désactiver le bouton **Chiffrer** :</span><span class="sxs-lookup"><span data-stu-id="c37d8-132">For example, to disable the **Encrypt** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="c37d8-133">Pour activer le **bouton Chiffrer** :</span><span class="sxs-lookup"><span data-stu-id="c37d8-133">To enable the **Encrypt** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="c37d8-134">Activer le déchiffrement côté service des messages électroniques pour les utilisateurs de l’application de messagerie iOS</span><span class="sxs-lookup"><span data-stu-id="c37d8-134">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="c37d8-135">L’application de messagerie iOS ne peut pas déchiffrer les messages protégés par chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="c37d8-135">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="c37d8-136">En tant qu Microsoft 365 de messagerie, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="c37d8-136">As a Microsoft 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="c37d8-137">Lorsque vous choisissez d’utiliser le déchiffrement côté service, le service envoie une copie déchiffrée du message à l’appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="c37d8-137">When you choose to do use service-side decryption, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="c37d8-138">L’appareil client stocke une copie déchiffrée du message.</span><span class="sxs-lookup"><span data-stu-id="c37d8-138">The client device stores a decrypted copy of the message.</span></span> <span data-ttu-id="c37d8-139">Le message conserve également des informations sur les droits d’utilisation, même si l’application de messagerie iOS n’applique pas de droits d’utilisation côté client à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c37d8-139">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="c37d8-140">L’utilisateur peut copier ou imprimer le message même s’il n’en avait pas à l’origine les droits.</span><span class="sxs-lookup"><span data-stu-id="c37d8-140">The user can copy or print the message even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="c37d8-141">Toutefois, si l’utilisateur tente d’effectuer une action qui nécessite le serveur de messagerie Microsoft 365, telle que le forwarding du message, le serveur n’autorise pas l’action si l’utilisateur n’en avait pas à l’origine le droit d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c37d8-141">However, if the user attempts to complete an action that requires the Microsoft 365 mail server, such as forwarding the message, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span> <span data-ttu-id="c37d8-142">Toutefois, les utilisateurs finaux peuvent contourner la restriction d’utilisation « Ne pas transmettre » en axant le message à partir d’un autre compte dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="c37d8-142">However, end users can work around "Do Not Forward" usage restriction by forwarding the message from a different account within the iOS mail app.</span></span> <span data-ttu-id="c37d8-143">Que vous définissez ou non le déchiffrement côté service du courrier, les pièces jointes au courrier chiffré et protégé par des droits ne peuvent pas être vues dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="c37d8-143">Regardless of whether you set up service-side decryption of mail, attachments to encrypted and rights protected mail can't be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="c37d8-144">Si vous choisissez de ne pas autoriser l’envoi de messages déchiffrés aux utilisateurs de l’application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu’ils ne sont pas en droit d’afficher le message.</span><span class="sxs-lookup"><span data-stu-id="c37d8-144">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="c37d8-145">Par défaut, le déchiffrement côté service des messages électroniques n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="c37d8-145">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="c37d8-146">Pour plus d’informations et pour une vue de l’expérience client, voir Afficher les messages chiffrés [sur iPhone ou iPad](https://support.microsoft.com/en-us/office/view-protected-messages-on-your-iphone-or-ipad-4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="c37d8-146">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.microsoft.com/en-us/office/view-protected-messages-on-your-iphone-or-ipad-4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="c37d8-147">Pour déterminer si les utilisateurs de l’application de messagerie iOS peuvent afficher les messages protégés par chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="c37d8-147">To manage whether iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="c37d8-148">Utilisez un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c37d8-148">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c37d8-149">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-149">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-150">Exécutez la cmdlet Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps :</span><span class="sxs-lookup"><span data-stu-id="c37d8-150">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="c37d8-151">Par exemple, pour configurer le service pour déchiffrer les messages avant qu’ils ne sont envoyés à des applications nonlightened telles que l’application de messagerie iOS :</span><span class="sxs-lookup"><span data-stu-id="c37d8-151">For example, to configure the service to decrypt messages before they're sent to unenlightened apps like the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="c37d8-152">Vous pouvez également configurer le service pour qu’il n’envoie pas de messages déchiffrés à des applications non configurées :</span><span class="sxs-lookup"><span data-stu-id="c37d8-152">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

> [!NOTE]
> <span data-ttu-id="c37d8-153">Les stratégies de boîte aux lettres individuelles (OWA/ActiveSync) remplacent ces paramètres (par exemple, si -IRMEnabled est définie sur False dans la stratégie de boîte aux lettres OWA ou activeSync, ces configurations ne s’appliquent pas).</span><span class="sxs-lookup"><span data-stu-id="c37d8-153">Individual mailbox policies (OWA/ActiveSync) override these settings (i.e. if -IRMEnabled is set to False within the respective OWA Mailbox policy, or ActiveSync Mailbox policy, then these configurations would not apply).</span></span>

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="c37d8-154">Activer le déchiffrement côté service des pièces jointes pour les clients de messagerie de navigateur web</span><span class="sxs-lookup"><span data-stu-id="c37d8-154">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="c37d8-155">Normalement, lorsque vous utilisez le chiffrement Office 365 messages, les pièces jointes sont automatiquement chiffrées.</span><span class="sxs-lookup"><span data-stu-id="c37d8-155">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="c37d8-156">En tant qu’administrateur, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes de courrier que les utilisateurs téléchargent à partir d’un navigateur web.</span><span class="sxs-lookup"><span data-stu-id="c37d8-156">As an administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="c37d8-157">Lorsque vous utilisez le déchiffrement côté service, le service envoie une copie déchiffrée du fichier à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c37d8-157">When you use service-side decryption, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="c37d8-158">Le message est toujours chiffré.</span><span class="sxs-lookup"><span data-stu-id="c37d8-158">The message is still encrypted.</span></span> <span data-ttu-id="c37d8-159">La pièce jointe conserve également les informations sur les droits d’utilisation, même si le navigateur n’applique pas les droits d’utilisation côté client à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c37d8-159">The email attachment also keeps information about usage rights even though the browser doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="c37d8-160">L’utilisateur peut copier ou imprimer la pièce jointe même s’il n’en avait pas à l’origine les droits.</span><span class="sxs-lookup"><span data-stu-id="c37d8-160">The user can copy or print the email attachment even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="c37d8-161">Toutefois, si l’utilisateur tente d’effectuer une action qui nécessite le serveur de messagerie Microsoft 365, telle que le forwarding de la pièce jointe, le serveur n’autorise pas l’action si l’utilisateur n’en avait pas à l’origine le droit d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c37d8-161">However, if the user tries to complete an action that requires the Microsoft 365 mail server, such as forwarding the attachment, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span>
  
<span data-ttu-id="c37d8-162">Que vous setiez ou non le déchiffrement côté service des pièces jointes, les utilisateurs ne peuvent pas afficher les pièces jointes des messages chiffrés et protégés par des droits dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="c37d8-162">Regardless of whether you set up service-side decryption of attachments, users can't view any attachments to encrypted and rights protected mail in the iOS mail app.</span></span>
  
<span data-ttu-id="c37d8-163">Si vous choisissez de ne pas autoriser les pièces jointes déchiffrées, qui est la valeur par défaut, les utilisateurs reçoivent un message qui indique qu’ils ne sont pas en droit d’afficher la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="c37d8-163">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="c37d8-164">Pour plus d’informations sur la façon dont Microsoft 365 implémente le chiffrement pour les e-mails et les pièces jointes avec l’option Encrypt-Only, voir l’option Chiffrer uniquement pour [les e-mails.](/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="c37d8-164">For more information about how Microsoft 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="c37d8-165">Pour déterminer si les pièces jointes sont déchiffrées lors du téléchargement à partir d’un navigateur web</span><span class="sxs-lookup"><span data-stu-id="c37d8-165">To manage whether email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="c37d8-166">Utilisez un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c37d8-166">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c37d8-167">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-167">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-168">Exécutez Set-IRMConfiguration cmdlet avec le paramètre DecryptAttachmentForEncryptOnly :</span><span class="sxs-lookup"><span data-stu-id="c37d8-168">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentForEncryptOnly parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentForEncryptOnly <$true|$false>
   ```

   <span data-ttu-id="c37d8-169">Par exemple, pour configurer le service pour déchiffrer les pièces jointes lorsqu’un utilisateur les télécharge à partir d’un navigateur web :</span><span class="sxs-lookup"><span data-stu-id="c37d8-169">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $true
   ```

   <span data-ttu-id="c37d8-170">Pour configurer le service afin qu’il laisse les pièces jointes chiffrées telles qu’elles sont au téléchargement :</span><span class="sxs-lookup"><span data-stu-id="c37d8-170">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail"></a><span data-ttu-id="c37d8-171">Vérifier que tous les destinataires externes utilisent le portail OME pour lire les messages chiffrés</span><span class="sxs-lookup"><span data-stu-id="c37d8-171">Ensure all external recipients use the OME Portal to read encrypted mail</span></span>

<span data-ttu-id="c37d8-172">Vous pouvez utiliser des modèles de personnalisation pour obliger les destinataires à recevoir un wrapper qui les dirige vers la lecture de messages chiffrés dans le portail OME au lieu d’utiliser Outlook ou Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="c37d8-172">You can use custom branding templates to force recipients to receive a wrapper mail that directs them to read encrypted email in the OME Portal instead of using Outlook or Outlook on the web.</span></span> <span data-ttu-id="c37d8-173">Vous pouvez le faire si vous souhaitez mieux contrôler la façon dont les destinataires utilisent le courrier qu’ils reçoivent.</span><span class="sxs-lookup"><span data-stu-id="c37d8-173">You might want to do this if you use want greater control over how recipients use the mail they receive.</span></span> <span data-ttu-id="c37d8-174">Par exemple, si des destinataires externes visualisent le courrier électronique dans le portail web, vous pouvez définir une date d’expiration pour le courrier électronique et révoquer le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="c37d8-174">For example, if external recipients view email in the web portal, you can set an expiration date for the email, and you can revoke the email.</span></span> <span data-ttu-id="c37d8-175">Ces fonctionnalités sont uniquement pris en charge via le portail OME.</span><span class="sxs-lookup"><span data-stu-id="c37d8-175">These features are only supported through the OME Portal.</span></span> <span data-ttu-id="c37d8-176">Vous pouvez utiliser l’option Chiffrer et l’option Ne pas forwarder lors de la création des règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c37d8-176">You can use the Encrypt option and the Do Not Forward option when creating the mail flow rules.</span></span>

### <a name="use-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email"></a><span data-ttu-id="c37d8-177">Utiliser un modèle personnalisé pour forcer tous les destinataires externes à utiliser le portail OME et pour le courrier électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="c37d8-177">Use a custom template to force all external recipients to use the OME Portal and for encrypted email</span></span>

1. <span data-ttu-id="c37d8-178">Utilisez un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c37d8-178">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c37d8-179">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-179">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-180">Exécutez lNew-TransportRule cmdlet :</span><span class="sxs-lookup"><span data-stu-id="c37d8-180">Run the New-TransportRule cmdlet:</span></span>

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    <span data-ttu-id="c37d8-181">où :</span><span class="sxs-lookup"><span data-stu-id="c37d8-181">where:</span></span>

   - <span data-ttu-id="c37d8-182">`mail flow rule name` est le nom que vous souhaitez utiliser pour la nouvelle règle de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c37d8-182">`mail flow rule name` is the name you want to use for the new mail flow rule.</span></span>

   - <span data-ttu-id="c37d8-183">`option name` est soit `Encrypt` `Do Not Forward` ou .</span><span class="sxs-lookup"><span data-stu-id="c37d8-183">`option name` is either `Encrypt` or `Do Not Forward`.</span></span>

   - <span data-ttu-id="c37d8-184">`template name` est le nom que vous avez donné au modèle de personnalisation, par exemple `OME Configuration` .</span><span class="sxs-lookup"><span data-stu-id="c37d8-184">`template name` is the name you gave the custom branding template, for example `OME Configuration`.</span></span>

   <span data-ttu-id="c37d8-185">Pour chiffrer tous les messages externes à l’aide du modèle « Configuration OME » et appliquer lEncrypt-Only option :</span><span class="sxs-lookup"><span data-stu-id="c37d8-185">To encrypt all external email with the "OME Configuration" template and apply the Encrypt-Only option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "OME Configuration"
   ```

   <span data-ttu-id="c37d8-186">Pour chiffrer tous les messages externes à l’aide du modèle « Configuration OME » et appliquer l’option Ne pas forwarder :</span><span class="sxs-lookup"><span data-stu-id="c37d8-186">To encrypt all external email with the "OME Configuration" template and apply the Do Not Forward option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "OME Configuration"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="c37d8-187">Personnaliser l’apparence des messages électroniques et du portail OME</span><span class="sxs-lookup"><span data-stu-id="c37d8-187">Customize the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="c37d8-188">Pour plus d’informations sur la façon dont vous pouvez personnaliser OME pour votre organisation, voir Ajouter la marque de votre organisation [à vos messages chiffrés.](add-your-organization-brand-to-encrypted-messages.md)</span><span class="sxs-lookup"><span data-stu-id="c37d8-188">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disable-the-new-capabilities-for-ome"></a><span data-ttu-id="c37d8-189">Désactiver les nouvelles fonctionnalités pour OME</span><span class="sxs-lookup"><span data-stu-id="c37d8-189">Disable the new capabilities for OME</span></span>

<span data-ttu-id="c37d8-190">Nous espérons qu’elle n’y arrive pas, mais si nécessaire, la désactivation des nouvelles fonctionnalités pour OME est très simple.</span><span class="sxs-lookup"><span data-stu-id="c37d8-190">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="c37d8-191">Tout d’abord, vous devez supprimer toutes les règles de flux de messagerie que vous avez créées qui utilisent les nouvelles fonctionnalités OME.</span><span class="sxs-lookup"><span data-stu-id="c37d8-191">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="c37d8-192">Pour plus d’informations sur la suppression des règles de flux de messagerie, voir [Gérer les règles de flux de messagerie.](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules)</span><span class="sxs-lookup"><span data-stu-id="c37d8-192">For information about removing mail flow rules, see [Manage mail flow rules](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules).</span></span> <span data-ttu-id="c37d8-193">Ensuite, complétez ces étapes dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c37d8-193">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="c37d8-194">Pour désactiver les nouvelles fonctionnalités pour OME</span><span class="sxs-lookup"><span data-stu-id="c37d8-194">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="c37d8-195">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c37d8-195">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c37d8-196">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c37d8-196">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="c37d8-197">Si vous avez  activé le bouton Chiffrer dans Outlook sur le web, désactivez-le en exécutant la cmdlet Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled.</span><span class="sxs-lookup"><span data-stu-id="c37d8-197">If you enabled the **Encrypt** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="c37d8-198">Sinon, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="c37d8-198">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="c37d8-199">Désactivez les nouvelles fonctionnalités pour OME en exécutant la cmdlet Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled définie sur false :</span><span class="sxs-lookup"><span data-stu-id="c37d8-199">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
