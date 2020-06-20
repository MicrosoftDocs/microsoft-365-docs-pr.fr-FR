---
title: Gérer le chiffrement de messages Office 365
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
description: Une fois que vous avez terminé la configuration d’Office 365 message Encryption (OME), Découvrez comment personnaliser votre déploiement de plusieurs façons.
ms.openlocfilehash: 83fa620852ea9b2e0cd50d50b6715742658b7239
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44815431"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="56624-103">Gérer le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="56624-103">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="56624-104">Une fois que vous avez terminé la configuration d’Office 365 message Encryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="56624-104">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in several ways.</span></span> <span data-ttu-id="56624-105">Par exemple, vous pouvez configurer s’il faut activer des codes de passe unique, afficher le bouton **chiffrer** dans Outlook sur le Web, etc.</span><span class="sxs-lookup"><span data-stu-id="56624-105">For example, you can configure whether to enable one-time pass codes, display the **Encrypt** button in Outlook on the web, and more.</span></span> <span data-ttu-id="56624-106">Les tâches décrites dans cet article expliquent comment procéder.</span><span class="sxs-lookup"><span data-stu-id="56624-106">The tasks in this article describe how.</span></span>

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="56624-107">Gérer si Google, Yahoo et les destinataires de comptes Microsoft peuvent utiliser ces comptes pour se connecter au portail de chiffrement des messages Office 365</span><span class="sxs-lookup"><span data-stu-id="56624-107">Manage whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="56624-108">Lorsque vous configurez les nouvelles fonctionnalités de chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires qui se trouvent en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="56624-108">When you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your organization.</span></span> <span data-ttu-id="56624-109">Si le destinataire utilise un *ID* de société comme un compte Google, un compte Yahoo ou un compte Microsoft, le destinataire peut se connecter au portail OME à l’aide d’un identifiant social.</span><span class="sxs-lookup"><span data-stu-id="56624-109">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal with a social ID.</span></span> <span data-ttu-id="56624-110">Si vous le souhaitez, vous pouvez choisir de ne pas autoriser les destinataires à utiliser des ID sociaux pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="56624-110">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="56624-111">Pour savoir si les destinataires peuvent utiliser des ID sociaux pour se connecter au portail OME</span><span class="sxs-lookup"><span data-stu-id="56624-111">To manage whether recipients can use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="56624-112">[Connectez-vous à Exchange Online à l’aide de Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="56624-112">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="56624-113">Exécutez la cmdlet Set-OMEConfiguration avec le paramètre SocialIdSignIn comme suit :</span><span class="sxs-lookup"><span data-stu-id="56624-113">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   <span data-ttu-id="56624-114">Par exemple, pour désactiver les ID de mise en réseau :</span><span class="sxs-lookup"><span data-stu-id="56624-114">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="56624-115">Pour activer les ID de mise en réseau :</span><span class="sxs-lookup"><span data-stu-id="56624-115">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a><span data-ttu-id="56624-116">Gérer l’utilisation de codes d’accès unique pour le portail de chiffrement des messages Office 365</span><span class="sxs-lookup"><span data-stu-id="56624-116">Manage the use of one-time pass codes for the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="56624-117">Si le destinataire d’un message chiffré par OME n’utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien d’affichage Web de temps limité qui lui permet de lire le message.</span><span class="sxs-lookup"><span data-stu-id="56624-117">If the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="56624-118">Ce lien inclut un code d’accès unique.</span><span class="sxs-lookup"><span data-stu-id="56624-118">This link includes a one-time pass code.</span></span> <span data-ttu-id="56624-119">En tant qu’administrateur, vous pouvez décider si les destinataires peuvent utiliser des codes de transmission à usage unique pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="56624-119">As an administrator, you can decide if recipients can use one-time pass codes to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a><span data-ttu-id="56624-120">Pour gérer si OME génère des codes d’accès en une seule fois</span><span class="sxs-lookup"><span data-stu-id="56624-120">To manage whether OME generates one-time pass codes</span></span>
  
1. <span data-ttu-id="56624-121">Utilisez un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation et démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="56624-121">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="56624-122">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="56624-122">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="56624-123">Exécutez la cmdlet Set-OMEConfiguration avec le paramètre OTPEnabled :</span><span class="sxs-lookup"><span data-stu-id="56624-123">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="56624-124">Par exemple, pour désactiver les codes d’accès à usage unique :</span><span class="sxs-lookup"><span data-stu-id="56624-124">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="56624-125">Pour activer les codes d’accès à usage unique :</span><span class="sxs-lookup"><span data-stu-id="56624-125">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-encrypt-button-in-outlook-on-the-web"></a><span data-ttu-id="56624-126">Gérer l’affichage du bouton chiffrer dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="56624-126">Manage the display of the Encrypt button in Outlook on the web</span></span>

<span data-ttu-id="56624-127">En tant qu’administrateur, vous pouvez gérer l’affichage de ce bouton pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="56624-127">As an administrator, you can manage whether to display this button to end users.</span></span>
  
### <a name="to-manage-whether-the-encrypt-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="56624-128">Pour gérer l’affichage du bouton chiffrer dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="56624-128">To manage whether the Encrypt button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="56624-129">Utilisez un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation et démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="56624-129">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="56624-130">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="56624-130">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="56624-131">Exécutez la cmdlet Set-IRMConfiguration avec le paramètre-SimplifiedClientAccessEnabled :</span><span class="sxs-lookup"><span data-stu-id="56624-131">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="56624-132">Par exemple, pour désactiver le bouton **chiffrer** :</span><span class="sxs-lookup"><span data-stu-id="56624-132">For example, to disable the **Encrypt** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="56624-133">Pour activer le bouton **chiffrer** :</span><span class="sxs-lookup"><span data-stu-id="56624-133">To enable the **Encrypt** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="56624-134">Activer le déchiffrement côté service des messages électroniques pour les utilisateurs de l’application de messagerie iOS</span><span class="sxs-lookup"><span data-stu-id="56624-134">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="56624-135">L’application de messagerie iOS ne peut pas déchiffrer les messages protégés avec le chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="56624-135">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="56624-136">En tant qu’administrateur Microsoft 365, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="56624-136">As a Microsoft 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="56624-137">Lorsque vous choisissez d’utiliser le déchiffrement côté service, le service envoie une copie déchiffrée du message à l’appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="56624-137">When you choose to do use service-side decryption, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="56624-138">L’appareil client stocke une copie déchiffrée du message.</span><span class="sxs-lookup"><span data-stu-id="56624-138">The client device stores a decrypted copy of the message.</span></span> <span data-ttu-id="56624-139">Le message conserve également des informations sur les droits d’utilisation, même si l’application de messagerie iOS n’applique pas de droits d’utilisation côté client à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56624-139">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="56624-140">L’utilisateur peut copier ou imprimer le message même s’il ne dispose pas des droits nécessaires pour le faire.</span><span class="sxs-lookup"><span data-stu-id="56624-140">The user can copy or print the message even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="56624-141">Toutefois, si l’utilisateur tente d’effectuer une action qui nécessite le serveur de messagerie Microsoft 365, par exemple, le transfert du message, le serveur n’autorise pas l’action si l’utilisateur n’a pas le droit d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="56624-141">However, if the user attempts to complete an action that requires the Microsoft 365 mail server, such as forwarding the message, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span> <span data-ttu-id="56624-142">Toutefois, les utilisateurs finaux peuvent contourner les restrictions d’utilisation « ne pas transférer » en transférant le message à partir d’un compte différent au sein de l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="56624-142">However, end users can work around "Do Not Forward" usage restriction by forwarding the message from a different account within the iOS mail app.</span></span> <span data-ttu-id="56624-143">Que vous configurez le déchiffrement côté service du courrier, les pièces jointes aux messages chiffrés et protégés par des droits ne peuvent pas être visualisées dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="56624-143">Regardless of whether you set up service-side decryption of mail, attachments to encrypted and rights protected mail can't be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="56624-144">Si vous choisissez de ne pas autoriser les messages déchiffrés à être envoyés aux utilisateurs de l’application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu’ils ne disposent pas des droits pour afficher le message.</span><span class="sxs-lookup"><span data-stu-id="56624-144">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="56624-145">Par défaut, le déchiffrement côté service des messages électroniques n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="56624-145">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="56624-146">Pour plus d’informations et pour une vue de l’expérience client, consultez la rubrique [afficher des messages chiffrés sur votre iPhone ou iPad](https://support.microsoft.com/en-us/office/view-protected-messages-on-your-iphone-or-ipad-4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="56624-146">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.microsoft.com/en-us/office/view-protected-messages-on-your-iphone-or-ipad-4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="56624-147">Pour gérer si les utilisateurs de l’application de messagerie iOS peuvent afficher les messages protégés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="56624-147">To manage whether iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="56624-148">Utilisez un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation et démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="56624-148">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="56624-149">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="56624-149">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="56624-150">Exécutez la cmdlet Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps :</span><span class="sxs-lookup"><span data-stu-id="56624-150">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="56624-151">Par exemple, pour configurer le service afin de déchiffrer les messages avant qu’ils soient envoyés à des applications non satisfaites, telles que l’application de messagerie iOS :</span><span class="sxs-lookup"><span data-stu-id="56624-151">For example, to configure the service to decrypt messages before they're sent to unenlightened apps like the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="56624-152">Ou, pour configurer le service de sorte qu’il n’envoie pas de messages déchiffrés à des applications incorrectes :</span><span class="sxs-lookup"><span data-stu-id="56624-152">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

> [!NOTE]
> <span data-ttu-id="56624-153">Les stratégies de boîte aux lettres individuelles (OWA/ActiveSync) remplacent ces paramètres (par exemple, si-IRMEnabled est défini sur false dans la stratégie de boîte aux lettres OWA correspondante ou dans la stratégie de boîte aux lettres ActiveSync, ces configurations ne s’appliquent pas).</span><span class="sxs-lookup"><span data-stu-id="56624-153">Individual mailbox policies (OWA/ActiveSync) override these settings (i.e. if -IRMEnabled is set to False within the respective OWA Mailbox policy, or ActiveSync Mailbox policy, then these configurations would not apply).</span></span>

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="56624-154">Activer le déchiffrement côté service des pièces jointes de courrier électronique pour les clients de messagerie de navigateur Web</span><span class="sxs-lookup"><span data-stu-id="56624-154">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="56624-155">En règle générale, lorsque vous utilisez le chiffrement de messages Office 365, les pièces jointes sont automatiquement chiffrées.</span><span class="sxs-lookup"><span data-stu-id="56624-155">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="56624-156">En tant qu’administrateur, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes que les utilisateurs téléchargent à partir d’un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="56624-156">As an administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="56624-157">Lorsque vous utilisez le déchiffrement côté service, le service envoie une copie déchiffrée du fichier sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="56624-157">When you use service-side decryption, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="56624-158">Le message est toujours chiffré.</span><span class="sxs-lookup"><span data-stu-id="56624-158">The message is still encrypted.</span></span> <span data-ttu-id="56624-159">La pièce jointe conserve également des informations sur les droits d’utilisation, même si le navigateur n’applique pas de droits d’utilisation côté client à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56624-159">The email attachment also keeps information about usage rights even though the browser doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="56624-160">L’utilisateur peut copier ou imprimer la pièce jointe du message, même s’il ne dispose pas des droits nécessaires pour le faire.</span><span class="sxs-lookup"><span data-stu-id="56624-160">The user can copy or print the email attachment even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="56624-161">Toutefois, si l’utilisateur tente d’effectuer une action qui nécessite le serveur de messagerie Microsoft 365, par exemple, le transfert de la pièce jointe, le serveur n’autorise pas l’action si l’utilisateur n’est pas à l’origine de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="56624-161">However, if the user tries to complete an action that requires the Microsoft 365 mail server, such as forwarding the attachment, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span>
  
<span data-ttu-id="56624-162">Que vous configurez le déchiffrement côté service des pièces jointes, les utilisateurs ne peuvent pas afficher les pièces jointes aux messages chiffrés et protégés par des droits dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="56624-162">Regardless of whether you set up service-side decryption of attachments, users can't view any attachments to encrypted and rights protected mail in the iOS mail app.</span></span>
  
<span data-ttu-id="56624-163">Si vous choisissez de ne pas autoriser les pièces jointes déchiffrées, ce qui correspond à la valeur par défaut, les utilisateurs reçoivent un message qui indique qu’ils ne disposent pas des droits pour afficher la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="56624-163">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="56624-164">Pour plus d’informations sur la façon dont Microsoft 365 implémente le chiffrement pour les courriers électroniques et les pièces jointes avec l’option de chiffrement uniquement, voir [option chiffrer uniquement pour les messages électroniques.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="56624-164">For more information about how Microsoft 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="56624-165">Pour gérer si les pièces jointes sont déchiffrées lors du téléchargement à partir d’un navigateur Web</span><span class="sxs-lookup"><span data-stu-id="56624-165">To manage whether email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="56624-166">Utilisez un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation et démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="56624-166">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="56624-167">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="56624-167">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="56624-168">Exécutez la cmdlet Set-IRMConfiguration avec le paramètre DecryptAttachmentForEncryptOnly :</span><span class="sxs-lookup"><span data-stu-id="56624-168">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentForEncryptOnly parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentForEncryptOnly <$true|$false>
   ```

   <span data-ttu-id="56624-169">Par exemple, pour configurer le service afin de déchiffrer les pièces jointes lorsqu’un utilisateur les télécharge à partir d’un navigateur Web :</span><span class="sxs-lookup"><span data-stu-id="56624-169">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $true
   ```

   <span data-ttu-id="56624-170">Pour configurer le service de sorte qu’il quitte les pièces jointes chiffrées lorsqu’il est téléchargé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="56624-170">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail"></a><span data-ttu-id="56624-171">Vérifier que tous les destinataires externes utilisent le portail OME pour lire les messages chiffrés</span><span class="sxs-lookup"><span data-stu-id="56624-171">Ensure all external recipients use the OME Portal to read encrypted mail</span></span>

<span data-ttu-id="56624-172">Vous pouvez utiliser des modèles personnalisés pour obliger les destinataires à recevoir un message de wrapper qui les achemine pour lire des messages chiffrés dans le portail OME au lieu d’utiliser Outlook ou Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="56624-172">You can use custom branding templates to force recipients to receive a wrapper mail that directs them to read encrypted email in the OME Portal instead of using Outlook or Outlook on the web.</span></span> <span data-ttu-id="56624-173">Vous souhaiterez peut-être procéder ainsi si vous avez besoin d’un plus grand contrôle sur la façon dont les destinataires utilisent les messages qu’ils reçoivent.</span><span class="sxs-lookup"><span data-stu-id="56624-173">You might want to do this if you use want greater control over how recipients use the mail they receive.</span></span> <span data-ttu-id="56624-174">Par exemple, si des destinataires externes affichent le courrier électronique dans le portail Web, vous pouvez définir une date d’expiration pour le courrier électronique et vous pouvez révoquer le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="56624-174">For example, if external recipients view email in the web portal, you can set an expiration date for the email, and you can revoke the email.</span></span> <span data-ttu-id="56624-175">Ces fonctionnalités sont uniquement prises en charge par le biais du portail OME.</span><span class="sxs-lookup"><span data-stu-id="56624-175">These features are only supported through the OME Portal.</span></span> <span data-ttu-id="56624-176">Vous pouvez utiliser l’option chiffrer et l’option ne pas transférer lors de la création des règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="56624-176">You can use the Encrypt option and the Do Not Forward option when creating the mail flow rules.</span></span>

### <a name="use-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email"></a><span data-ttu-id="56624-177">Utiliser un modèle personnalisé pour obliger tous les destinataires externes à utiliser le portail OME et le courrier chiffré</span><span class="sxs-lookup"><span data-stu-id="56624-177">Use a custom template to force all external recipients to use the OME Portal and for encrypted email</span></span>

1. <span data-ttu-id="56624-178">Utilisez un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation et démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="56624-178">Use a work or school account that has global administrator permissions in your organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="56624-179">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="56624-179">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="56624-180">Exécutez la cmdlet New-TransportRule :</span><span class="sxs-lookup"><span data-stu-id="56624-180">Run the New-TransportRule cmdlet:</span></span>

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    <span data-ttu-id="56624-181">où :</span><span class="sxs-lookup"><span data-stu-id="56624-181">where:</span></span>

   - <span data-ttu-id="56624-182">`mail flow rule name`est le nom que vous souhaitez utiliser pour la nouvelle règle de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="56624-182">`mail flow rule name` is the name you want to use for the new mail flow rule.</span></span>

   - <span data-ttu-id="56624-183">`option name`est soit `Encrypt` ou `Do Not Forward` .</span><span class="sxs-lookup"><span data-stu-id="56624-183">`option name` is either `Encrypt` or `Do Not Forward`.</span></span>

   - <span data-ttu-id="56624-184">`template name`est le nom que vous avez attribué au modèle personnalisé, par exemple `OME Configuration` .</span><span class="sxs-lookup"><span data-stu-id="56624-184">`template name` is the name you gave the custom branding template, for example `OME Configuration`.</span></span>

   <span data-ttu-id="56624-185">Pour chiffrer tous les messages électroniques externes avec le modèle « configuration de OME » et appliquer l’option de chiffrement uniquement :</span><span class="sxs-lookup"><span data-stu-id="56624-185">To encrypt all external email with the "OME Configuration" template and apply the Encrypt-Only option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "OME Configuration"
   ```

   <span data-ttu-id="56624-186">Pour chiffrer tous les messages électroniques externes avec le modèle « configuration de OME » et appliquer l’option ne pas transférer :</span><span class="sxs-lookup"><span data-stu-id="56624-186">To encrypt all external email with the "OME Configuration" template and apply the Do Not Forward option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "OME Configuration"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="56624-187">Personnaliser l’apparence des messages électroniques et le portail OME</span><span class="sxs-lookup"><span data-stu-id="56624-187">Customize the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="56624-188">Pour plus d’informations sur la façon de personnaliser OME pour votre organisation, consultez la rubrique [Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="56624-188">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disable-the-new-capabilities-for-ome"></a><span data-ttu-id="56624-189">Désactiver les nouvelles fonctionnalités pour OME</span><span class="sxs-lookup"><span data-stu-id="56624-189">Disable the new capabilities for OME</span></span>

<span data-ttu-id="56624-190">Nous espérons qu’il n’y parviendra pas, mais si vous le souhaitez, la désactivation des nouvelles fonctionnalités de OME est très simple.</span><span class="sxs-lookup"><span data-stu-id="56624-190">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="56624-191">Tout d’abord, vous devez supprimer toutes les règles de flux de messagerie que vous avez créées qui utilisent les nouvelles fonctionnalités de OME.</span><span class="sxs-lookup"><span data-stu-id="56624-191">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="56624-192">Pour plus d’informations sur la suppression des règles de flux de messagerie, consultez la rubrique [Manage mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="56624-192">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="56624-193">Ensuite, effectuez ces étapes dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="56624-193">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="56624-194">Pour désactiver les nouvelles fonctionnalités de OME</span><span class="sxs-lookup"><span data-stu-id="56624-194">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="56624-195">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="56624-195">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="56624-196">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="56624-196">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="56624-197">Si vous avez activé le bouton **chiffrer** dans Outlook sur le Web, désactivez-le en exécutant la cmdlet Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled.</span><span class="sxs-lookup"><span data-stu-id="56624-197">If you enabled the **Encrypt** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="56624-198">Sinon, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="56624-198">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="56624-199">Désactivez les nouvelles fonctionnalités de OME en exécutant l’applet de commande Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled défini sur false :</span><span class="sxs-lookup"><span data-stu-id="56624-199">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
