---
title: Ajouter la marque de votre organisation à vos messages chiffrés
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/1/2020
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
description: Découvrez comment les administrateurs généraux d’Office 365 peuvent appliquer la personnalisation de votre organisation aux messages électroniques chiffrés & contenu du portail de chiffrement.
ms.openlocfilehash: 56b948fc941da4fb221d929ecd59c5300b135e39
ms.sourcegitcommit: c0495e224f12c448bfc162ef2e4b33b82f064ac8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49709496"
---
# <a name="add-your-organizations-brand-to-your-microsoft-365-for-business-message-encryption-encrypted-messages"></a><span data-ttu-id="cd35a-103">Ajouter la marque de votre organisation à vos messages chiffrés Microsoft 365 pour le chiffrement des messages professionnels</span><span class="sxs-lookup"><span data-stu-id="cd35a-103">Add your organization's brand to your Microsoft 365 for business Message Encryption encrypted messages</span></span>

<span data-ttu-id="cd35a-104">Vous pouvez appliquer la personnalisation de votre entreprise pour personnaliser l’apparence des messages électroniques de votre organisation et le portail de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="cd35a-104">You can apply your company branding to customize the look of your organization's email messages and the encryption portal.</span></span> <span data-ttu-id="cd35a-105">Avant de commencer, vous devez appliquer les autorisations d’administrateur général à votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="cd35a-105">You'll need to apply global administrator permissions to your work or school account before you can get started.</span></span> <span data-ttu-id="cd35a-106">Une fois que vous disposez de ces autorisations, utilisez les applets de commande Get-OMEConfiguration et Set-OMEConfiguration Windows PowerShell pour personnaliser ces parties de messages électroniques chiffrés :</span><span class="sxs-lookup"><span data-stu-id="cd35a-106">Once you have these permissions, use the Get-OMEConfiguration and Set-OMEConfiguration Windows PowerShell cmdlets to customize these parts of encrypted email messages:</span></span>
  
- <span data-ttu-id="cd35a-107">Texte d’introduction</span><span class="sxs-lookup"><span data-stu-id="cd35a-107">Introductory text</span></span>

- <span data-ttu-id="cd35a-108">Disclaimer text</span><span class="sxs-lookup"><span data-stu-id="cd35a-108">Disclaimer text</span></span>

- <span data-ttu-id="cd35a-109">URL de la déclaration de confidentialité de votre organisation</span><span class="sxs-lookup"><span data-stu-id="cd35a-109">URL for Your organization's privacy statement</span></span>

- <span data-ttu-id="cd35a-110">Texte dans le portail OME</span><span class="sxs-lookup"><span data-stu-id="cd35a-110">Text in the OME portal</span></span>

- <span data-ttu-id="cd35a-111">Logo qui apparaît dans le message électronique et dans le portail OME, ou s’il faut utiliser un logo du tout</span><span class="sxs-lookup"><span data-stu-id="cd35a-111">Logo that appears in the email message and OME portal, or whether to use a logo at all</span></span>

- <span data-ttu-id="cd35a-112">Couleur d’arrière-plan dans le message électronique et le portail OME</span><span class="sxs-lookup"><span data-stu-id="cd35a-112">Background color in the email message and OME portal</span></span>

<span data-ttu-id="cd35a-113">Vous pouvez également rétablir l’apparence par défaut à tout moment.</span><span class="sxs-lookup"><span data-stu-id="cd35a-113">You can also revert back to the default look and feel at any time.</span></span>

<span data-ttu-id="cd35a-114">Si vous souhaitez davantage de contrôle, utilisez le chiffrement de messages avancé Office 365 pour créer plusieurs modèles pour les messages électroniques chiffrés provenant de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cd35a-114">If you'd like more control, use Office 365 Advanced Message Encryption to create multiple templates for encrypted emails originating from your organization.</span></span> <span data-ttu-id="cd35a-115">Utilisez ces modèles pour contrôler des parties de l’expérience de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="cd35a-115">Use these templates to control parts of the end-user experience.</span></span> <span data-ttu-id="cd35a-116">Par exemple, indiquez si les destinataires peuvent utiliser les comptes Google, Yahoo et Microsoft pour se connecter au portail de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="cd35a-116">For example, specify whether recipients can use Google, Yahoo, and Microsoft Accounts to sign in to the encryption portal.</span></span> <span data-ttu-id="cd35a-117">Utilisez des modèles pour répondre à plusieurs cas d’utilisation, par exemple :</span><span class="sxs-lookup"><span data-stu-id="cd35a-117">Use templates to fulfill several use cases, such as:</span></span>

- <span data-ttu-id="cd35a-118">Services individuels, tels que finance, ventes, etc.</span><span class="sxs-lookup"><span data-stu-id="cd35a-118">Individual departments, such as Finance, Sales, and so on.</span></span>

- <span data-ttu-id="cd35a-119">Différents produits</span><span class="sxs-lookup"><span data-stu-id="cd35a-119">Different products</span></span>

- <span data-ttu-id="cd35a-120">Différents pays ou régions géographiques</span><span class="sxs-lookup"><span data-stu-id="cd35a-120">Different geographical regions or countries</span></span>

- <span data-ttu-id="cd35a-121">Si vous souhaitez autoriser la révocation des courriers électroniques</span><span class="sxs-lookup"><span data-stu-id="cd35a-121">Whether you want to allow emails to be revoked</span></span>

- <span data-ttu-id="cd35a-122">Si vous souhaitez que les e-mails envoyés à des destinataires externes expirent après un nombre de jours spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd35a-122">Whether you want emails sent to external recipients to expire after a specified number of days.</span></span>

<span data-ttu-id="cd35a-123">Une fois que vous avez créé les modèles, vous pouvez les appliquer à des messages électroniques chiffrés à l’aide de règles de flux de messagerie Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd35a-123">Once you've created the templates, you can apply them to encrypted emails by using Exchange mail flow rules.</span></span> <span data-ttu-id="cd35a-124">Si vous disposez d’Office 365 Advanced message Encryption, vous pouvez révoquer tous les messages que vous avez personnalisés à l’aide de ces modèles.</span><span class="sxs-lookup"><span data-stu-id="cd35a-124">If you have Office 365 Advanced Message Encryption, you can revoke any email that you've branded by using these templates.</span></span>

## <a name="work-with-ome-branding-templates"></a><span data-ttu-id="cd35a-125">Utiliser des modèles de personnalisation OME</span><span class="sxs-lookup"><span data-stu-id="cd35a-125">Work with OME branding templates</span></span>

<span data-ttu-id="cd35a-126">Vous pouvez modifier plusieurs fonctionnalités dans un modèle de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="cd35a-126">You can modify several features within a branding template.</span></span> <span data-ttu-id="cd35a-127">Vous pouvez modifier, mais pas supprimer, le modèle par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd35a-127">You can modify, but not remove, the default template.</span></span> <span data-ttu-id="cd35a-128">Si vous disposez d’un chiffrement de messages avancé, vous pouvez également créer, modifier et supprimer des modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cd35a-128">If you have Advanced Message Encryption, you can also create, modify, and remove custom templates.</span></span> <span data-ttu-id="cd35a-129">Utilisez Windows PowerShell pour utiliser un modèle de personnalisation à la fois.</span><span class="sxs-lookup"><span data-stu-id="cd35a-129">Use Windows PowerShell to work with one branding template at a time.</span></span>

- <span data-ttu-id="cd35a-130">[Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/set-omeconfiguration) -modifiez le modèle de personnalisation par défaut ou un modèle de personnalisation que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="cd35a-130">[Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/set-omeconfiguration) - Modify the default branding template or a custom branding template that you created.</span></span>
- <span data-ttu-id="cd35a-131">[New-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/new-omeconfiguration) -créer un modèle de personnalisation, le chiffrement de messages avancé uniquement.</span><span class="sxs-lookup"><span data-stu-id="cd35a-131">[New-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/new-omeconfiguration) - Create a new branding template, Advanced Message Encryption only.</span></span>
- <span data-ttu-id="cd35a-132">[Remove-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/remove-omeconfiguration) -supprimer un modèle de personnalisation personnalisé, chiffrement de message avancé uniquement.</span><span class="sxs-lookup"><span data-stu-id="cd35a-132">[Remove-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/remove-omeconfiguration) - Remove a custom branding template, Advanced Message Encryption only.</span></span> <span data-ttu-id="cd35a-133">Vous ne pouvez pas supprimer le modèle de personnalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd35a-133">You can't delete the default branding template.</span></span>
  
## <a name="modify-an-ome-branding-template"></a><span data-ttu-id="cd35a-134">Modifier un modèle de personnalisation OME</span><span class="sxs-lookup"><span data-stu-id="cd35a-134">Modify an OME branding template</span></span>

<span data-ttu-id="cd35a-135">Utilisez Windows PowerShell pour modifier un modèle de personnalisation à la fois.</span><span class="sxs-lookup"><span data-stu-id="cd35a-135">Use Windows PowerShell to modify one branding template at a time.</span></span> <span data-ttu-id="cd35a-136">Si vous disposez d’un chiffrement de messages avancé, vous pouvez également créer, modifier et supprimer des modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cd35a-136">If you have Advanced Message Encryption, you can also create, modify, and remove custom templates.</span></span>

1. <span data-ttu-id="cd35a-137">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cd35a-137">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="cd35a-138">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="cd35a-138">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="cd35a-139">Utilisez la cmdlet Set-OMEConfiguration comme décrit dans [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/Set-OMEConfiguration) ou utilisez le graphique et le tableau ci-dessous pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="cd35a-139">Use the Set-OMEConfiguration cmdlet as described in [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/Set-OMEConfiguration) or use the following graphic and table for guidance.</span></span>

![Composants de messagerie personnalisables](../media/ome-template-breakout.png)

|<span data-ttu-id="cd35a-141">**Pour personnaliser cette fonctionnalité de l’expérience de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="cd35a-141">**To customize this feature of the encryption experience**</span></span>|<span data-ttu-id="cd35a-142">**Utilisez ces commandes**</span><span class="sxs-lookup"><span data-stu-id="cd35a-142">**Use these commands**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd35a-143">Couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="cd35a-143">Background color</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -BackgroundColor "<#RRGGBB hexadecimal color code or name value>"` <br/> <span data-ttu-id="cd35a-144">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-144">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"` <br/> <span data-ttu-id="cd35a-145">Pour plus d’informations sur les couleurs d’arrière-plan, voir la section [couleurs d’arrière-plan](#background-color-reference) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="cd35a-145">For more information about background colors, see the [Background colors](#background-color-reference) section later in this article.</span></span>|
|<span data-ttu-id="cd35a-146">Logo</span><span class="sxs-lookup"><span data-stu-id="cd35a-146">Logo</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -Image <Byte[]>` <br/> <span data-ttu-id="cd35a-147">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-147">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> <span data-ttu-id="cd35a-148">Formats de fichier pris en charge : .png, .jpg, .bmp ou .tiff</span><span class="sxs-lookup"><span data-stu-id="cd35a-148">Supported file formats: .png, .jpg, .bmp, or .tiff</span></span>  <br/> <span data-ttu-id="cd35a-149">Taille optimale de fichier de logo : moins de 40 ko</span><span class="sxs-lookup"><span data-stu-id="cd35a-149">Optimal size of logo file: less than 40 KB</span></span>  <br/> <span data-ttu-id="cd35a-150">Taille optimale de l’image de logo : 170x70 pixels.</span><span class="sxs-lookup"><span data-stu-id="cd35a-150">Optimal size of logo image: 170x70 pixels.</span></span> <span data-ttu-id="cd35a-151">Si votre image dépasse ces dimensions, le service redimensionne votre logo pour qu’il s’affiche dans le portail.</span><span class="sxs-lookup"><span data-stu-id="cd35a-151">If your image exceeds these dimensions, the service resizes your logo for display in the portal.</span></span> <span data-ttu-id="cd35a-152">Le service ne modifie pas le fichier graphique lui-même.</span><span class="sxs-lookup"><span data-stu-id="cd35a-152">The service doesn't modify the graphic file itself.</span></span> <span data-ttu-id="cd35a-153">Pour obtenir de meilleurs résultats, utilisez la taille optimale.</span><span class="sxs-lookup"><span data-stu-id="cd35a-153">For best results, use the optimal size.</span></span>|
|<span data-ttu-id="cd35a-154">Texte en regard du nom et de l’adresse de messagerie de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="cd35a-154">Text next to the sender's name and email address</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -IntroductionText "<String up to 1024 characters>"` <br/> <span data-ttu-id="cd35a-155">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-155">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|<span data-ttu-id="cd35a-156">Texte qui apparaît sur le bouton « Lire le message »</span><span class="sxs-lookup"><span data-stu-id="cd35a-156">Text that appears on the "Read Message" button</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -ReadButtonText "<String up to 1024 characters>"` <br/> <span data-ttu-id="cd35a-157">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-157">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|<span data-ttu-id="cd35a-158">Texte qui apparaît sous le bouton « Lire le message »</span><span class="sxs-lookup"><span data-stu-id="cd35a-158">Text that appears below the "Read Message" button</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -EmailText "<String up to 1024 characters>"` <br/> <span data-ttu-id="cd35a-159">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-159">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|<span data-ttu-id="cd35a-160">URL du lien déclaration de confidentialité</span><span class="sxs-lookup"><span data-stu-id="cd35a-160">URL for the Privacy Statement link</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -PrivacyStatementURL "<URL>"` <br/> <span data-ttu-id="cd35a-161">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-161">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -PrivacyStatementURL "https://contoso.com/privacystatement.html"`|
|<span data-ttu-id="cd35a-162">Déclaration de non-responsabilité du message électronique qui contient le message chiffré</span><span class="sxs-lookup"><span data-stu-id="cd35a-162">Disclaimer statement in the email that contains the encrypted message</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> <span data-ttu-id="cd35a-163">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-163">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|<span data-ttu-id="cd35a-164">Texte qui s’affiche en haut du portail d’affichage du message chiffré</span><span class="sxs-lookup"><span data-stu-id="cd35a-164">Text that appears at the top of the encrypted mail viewing portal</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> <span data-ttu-id="cd35a-165">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-165">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."`|
|<span data-ttu-id="cd35a-166">Pour activer ou désactiver l’authentification avec un code d’accès unique pour ce modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd35a-166">To enable or disable authentication with a one-time pass code for this custom template</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -OTPEnabled <$true|$false>` <br/> <span data-ttu-id="cd35a-167">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-167">**Examples:**</span></span> <br/><span data-ttu-id="cd35a-168">Pour activer les codes secrets à usage unique pour ce modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd35a-168">To enable one-time passcodes for this custom template</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> <span data-ttu-id="cd35a-169">Pour désactiver les codes secrets à usage unique pour ce modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd35a-169">To disable one-time passcodes for this custom template</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|<span data-ttu-id="cd35a-170">Pour activer ou désactiver l’authentification avec des identités Microsoft, Google ou Yahoo pour ce modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd35a-170">To enable or disable authentication with Microsoft, Google, or Yahoo identities for this custom template</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -SocialIdSignIn <$true|$false>` <br/> <span data-ttu-id="cd35a-171">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-171">**Examples:**</span></span> <br/><span data-ttu-id="cd35a-172">Pour activer les ID de mise en réseau pour ce modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd35a-172">To enable social IDs for this custom template</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> <span data-ttu-id="cd35a-173">Pour désactiver les ID de mise en réseau pour ce modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd35a-173">To disable social IDs for this custom template</span></span> <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="create-an-ome-branding-template-advanced-message-encryption"></a><span data-ttu-id="cd35a-174">Créer un modèle de personnalisation OME (chiffrement avancé des messages)</span><span class="sxs-lookup"><span data-stu-id="cd35a-174">Create an OME branding template (Advanced Message Encryption)</span></span>

<span data-ttu-id="cd35a-175">Si vous disposez d’Office 365 Advanced message Encryption, vous pouvez créer des modèles de personnalisation pour votre organisation à l’aide de la cmdlet [New-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/new-omeconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="cd35a-175">If you have Office 365 Advanced Message Encryption, you can create custom branding templates for your organization by using the [New-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/new-omeconfiguration) cmdlet.</span></span> <span data-ttu-id="cd35a-176">Une fois que vous avez créé le modèle, vous pouvez modifier le modèle à l’aide de l’applet de commande Set-OMEConfiguration, comme décrit dans [modifier un modèle de personnalisation OME](#modify-an-ome-branding-template).</span><span class="sxs-lookup"><span data-stu-id="cd35a-176">Once you've created the template, you modify the template by using the Set-OMEConfiguration cmdlet as described in [Modify an OME branding template](#modify-an-ome-branding-template).</span></span> <span data-ttu-id="cd35a-177">Vous pouvez créer plusieurs modèles.</span><span class="sxs-lookup"><span data-stu-id="cd35a-177">You can create multiple templates.</span></span>

<span data-ttu-id="cd35a-178">Pour créer un modèle de personnalisation :</span><span class="sxs-lookup"><span data-stu-id="cd35a-178">To create a new custom branding template:</span></span>

1. <span data-ttu-id="cd35a-179">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cd35a-179">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="cd35a-180">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="cd35a-180">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="cd35a-181">Utilisez la cmdlet [New-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/new-omeconfiguration) pour créer un nouveau modèle.</span><span class="sxs-lookup"><span data-stu-id="cd35a-181">Use the [New-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/new-omeconfiguration) cmdlet to create a new template.</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<OMEConfigurationName>"
   ```

   <span data-ttu-id="cd35a-182">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cd35a-182">For example,</span></span>

   ```powershell
   New-OMEConfiguration -Identity "Custom branding template"
   ```

## <a name="return-the-default-branding-template-to-its-original-values"></a><span data-ttu-id="cd35a-183">Rétablir les valeurs d’origine du modèle de personnalisation par défaut</span><span class="sxs-lookup"><span data-stu-id="cd35a-183">Return the default branding template to its original values</span></span>

<span data-ttu-id="cd35a-184">Pour supprimer toutes les modifications apportées au modèle par défaut, y compris les personnalisations de la marque, et ainsi de suite, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd35a-184">To remove all modifications from the default template, including brand customizations, and so on, complete these steps:</span></span>
  
1. <span data-ttu-id="cd35a-185">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cd35a-185">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="cd35a-186">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="cd35a-186">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="cd35a-187">Utilisez la cmdlet **Set-OMEConfiguration** comme décrit dans [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/Set-OMEConfiguration).</span><span class="sxs-lookup"><span data-stu-id="cd35a-187">Use the **Set-OMEConfiguration** cmdlet as described in [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/Set-OMEConfiguration).</span></span> <span data-ttu-id="cd35a-188">Pour supprimer les personnalisations personnalisées de votre organisation des valeurs DisclaimerText, EmailText et PortalText, définissez la valeur sur une chaîne vide, `""` .</span><span class="sxs-lookup"><span data-stu-id="cd35a-188">To remove your organization's branded customizations from the DisclaimerText, EmailText, and PortalText values, set the value to an empty string, `""`.</span></span> <span data-ttu-id="cd35a-189">Pour toutes les valeurs d’image, telles que logo, définissez la valeur sur  `"$null"` .</span><span class="sxs-lookup"><span data-stu-id="cd35a-189">For all image values, such as Logo, set the value to  `"$null"`.</span></span>

   <span data-ttu-id="cd35a-190">Le tableau suivant décrit les valeurs par défaut de l’option de personnalisation du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="cd35a-190">The following table describes the encryption customization option defaults.</span></span>

   <span data-ttu-id="cd35a-191">**Pour annuler cette fonctionnalité de chiffrement et rétablir le texte et l’image par défaut**</span><span class="sxs-lookup"><span data-stu-id="cd35a-191">**To revert this feature of the encryption experience back to the default text and image**</span></span>|<span data-ttu-id="cd35a-192">**Utilisez ces commandes**</span><span class="sxs-lookup"><span data-stu-id="cd35a-192">**Use these commands**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="cd35a-193">Texte par défaut fourni avec des messages électroniques chiffrés</span><span class="sxs-lookup"><span data-stu-id="cd35a-193">Default text that comes with encrypted email messages</span></span>  <br/> <span data-ttu-id="cd35a-194">Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés</span><span class="sxs-lookup"><span data-stu-id="cd35a-194">The default text appears above the instructions for viewing encrypted messages</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -EmailText "<empty string>"` <br/> <span data-ttu-id="cd35a-195">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-195">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
   |<span data-ttu-id="cd35a-196">Déclaration de non-responsabilité du message électronique qui contient le message chiffré</span><span class="sxs-lookup"><span data-stu-id="cd35a-196">Disclaimer statement in the email that contains the encrypted message</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" DisclaimerText "<empty string>"` <br/> <span data-ttu-id="cd35a-197">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-197">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
   |<span data-ttu-id="cd35a-198">Texte qui s’affiche en haut du portail d’affichage du message chiffré</span><span class="sxs-lookup"><span data-stu-id="cd35a-198">Text that appears at the top of the encrypted mail viewing portal</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -PortalText "<empty string>"` <br/> <span data-ttu-id="cd35a-199">**Exemple de rétablissement de la valeur par défaut :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-199">**Example reverting back to default:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""`|
   |<span data-ttu-id="cd35a-200">Logo</span><span class="sxs-lookup"><span data-stu-id="cd35a-200">Logo</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -Image <"$null">` <br/> <span data-ttu-id="cd35a-201">**Exemple de rétablissement de la valeur par défaut :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-201">**Example reverting back to default:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
   |<span data-ttu-id="cd35a-202">Couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="cd35a-202">Background color</span></span>|`Set-OMEConfiguration -Identity "<OMEConfigurationName>" -BackgroundColor "$null">` <br/> <span data-ttu-id="cd35a-203">**Exemple de rétablissement de la valeur par défaut :**</span><span class="sxs-lookup"><span data-stu-id="cd35a-203">**Example reverting back to default:**</span></span> <br/> `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|
   |

## <a name="remove-a-custom-branding-template-advanced-message-encryption"></a><span data-ttu-id="cd35a-204">Supprimer un modèle de personnalisation (chiffrement de message avancé)</span><span class="sxs-lookup"><span data-stu-id="cd35a-204">Remove a custom branding template (Advanced Message Encryption)</span></span>

<span data-ttu-id="cd35a-205">Vous pouvez uniquement supprimer ou supprimer des modèles de personnalisation que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="cd35a-205">You can only remove or delete branding templates that you've made.</span></span> <span data-ttu-id="cd35a-206">Vous ne pouvez pas supprimer le modèle de personnalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd35a-206">You can't remove the default branding template.</span></span>

<span data-ttu-id="cd35a-207">Pour supprimer un modèle de personnalisation :</span><span class="sxs-lookup"><span data-stu-id="cd35a-207">To remove a custom branding template:</span></span>
  
1. <span data-ttu-id="cd35a-208">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cd35a-208">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="cd35a-209">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="cd35a-209">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="cd35a-210">Utilisez la cmdlet **Remove-OMEConfiguration** comme suit :</span><span class="sxs-lookup"><span data-stu-id="cd35a-210">Use the **Remove-OMEConfiguration** cmdlet as follows:</span></span>

   ```powershell
   Remove-OMEConfiguration -Identity ""<OMEConfigurationName>"
   ```

   <span data-ttu-id="cd35a-211">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cd35a-211">For example,</span></span>

   ```powershell
   Remove-OMEConfiguration -Identity "Branding template 1"
   ```

   <span data-ttu-id="cd35a-212">Pour plus d’informations, consultez la rubrique [Remove-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/remove-omeconfiguration).</span><span class="sxs-lookup"><span data-stu-id="cd35a-212">For more information, see [Remove-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/remove-omeconfiguration).</span></span>

## <a name="create-an-exchange-mail-flow-rule-that-applies-your-custom-branding-to-encrypted-emails"></a><span data-ttu-id="cd35a-213">Créer une règle de flux de messagerie Exchange qui applique votre personnalisation aux courriers chiffrés</span><span class="sxs-lookup"><span data-stu-id="cd35a-213">Create an Exchange mail flow rule that applies your custom branding to encrypted emails</span></span>

<span data-ttu-id="cd35a-214">Une fois que vous avez modifié le modèle par défaut ou créé des modèles de personnalisation, vous pouvez créer des règles de flux de messagerie Exchange pour appliquer votre personnalisation personnalisée en fonction de certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="cd35a-214">After you've either modified the default template or created new branding templates, you can create Exchange mail flow rules to apply your custom branding based on certain conditions.</span></span> <span data-ttu-id="cd35a-215">Une telle règle applique une personnalisation personnalisée dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="cd35a-215">Such a rule will apply custom branding in the following scenarios:</span></span>

- <span data-ttu-id="cd35a-216">Si le courrier électronique a été chiffré manuellement par l’utilisateur final à l’aide d’Outlook ou d’Outlook sur le Web, anciennement Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="cd35a-216">If the email was manually encrypted by the end user using Outlook or Outlook on the web, formerly Outlook Web App</span></span>

- <span data-ttu-id="cd35a-217">Si le courrier électronique a été automatiquement chiffré par une règle de flux de messagerie Exchange ou une stratégie de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="cd35a-217">If the email was automatically encrypted by an Exchange mail flow rule or Data Loss Prevention policy</span></span>

<span data-ttu-id="cd35a-218">Pour plus d’informations sur la création d’une règle de flux de messagerie Exchange qui applique le chiffrement, voir [définir des règles de flux de messagerie pour chiffrer des messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="cd35a-218">For information on how to create an Exchange mail flow rule that applies encryption, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

1. <span data-ttu-id="cd35a-219">Dans un navigateur Web, à l’aide d’un compte professionnel ou scolaire auquel des autorisations d’administrateur général ont été accordées, [Connectez-vous à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span><span class="sxs-lookup"><span data-stu-id="cd35a-219">In a web browser, using a work or school account that has been granted global administrator permissions, [sign in to Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).</span></span>

2. <span data-ttu-id="cd35a-220">Sélectionnez la vignette **admin** .</span><span class="sxs-lookup"><span data-stu-id="cd35a-220">Choose the **Admin** tile.</span></span>

3. <span data-ttu-id="cd35a-221">Dans le centre d’administration 365 de Microsoft, sélectionnez **centres** d’administration \> **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="cd35a-221">In the Microsoft 365 admin center, choose **Admin centers** \> **Exchange**.</span></span>

4. <span data-ttu-id="cd35a-222">Dans le centre d’administration Exchange, accédez à règles de **flux de messagerie** \>  et sélectionnez **nouvelle** ![ icône ](../media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="cd35a-222">In the EAC, go to **Mail flow** \> **Rules** and select **New** ![New icon](../media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Create a new rule**.</span></span> <span data-ttu-id="cd35a-223">Pour plus d’informations sur l’utilisation du centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="cd35a-223">For more information about using the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

5. <span data-ttu-id="cd35a-224">Dans **nom**, tapez un nom pour la règle, par exemple, personnalisation pour le service des ventes.</span><span class="sxs-lookup"><span data-stu-id="cd35a-224">In **Name**, type a name for the rule, such as Branding for sales department.</span></span>

6. <span data-ttu-id="cd35a-225">Dans **appliquer cette règle si**, sélectionnez la condition que **l’expéditeur se trouve à l’intérieur de l’organisation** et les autres conditions souhaitées dans la liste des conditions disponibles.</span><span class="sxs-lookup"><span data-stu-id="cd35a-225">In **Apply this rule if**, select the condition **The sender is located inside the organization** and other conditions you want from the list of available conditions.</span></span> <span data-ttu-id="cd35a-226">Par exemple, vous pouvez appliquer un modèle de personnalisation particulier à :</span><span class="sxs-lookup"><span data-stu-id="cd35a-226">For example, you might want to apply a particular branding template to:</span></span>

   - <span data-ttu-id="cd35a-227">Tous les messages chiffrés envoyés par les membres du service financier</span><span class="sxs-lookup"><span data-stu-id="cd35a-227">All encrypted emails sent from members of the finance department</span></span>
   - <span data-ttu-id="cd35a-228">Messages chiffrés envoyés avec un mot clé tel que « externe » ou « partenaire »</span><span class="sxs-lookup"><span data-stu-id="cd35a-228">Encrypted emails sent with a certain keyword such as "External" or "Partner"</span></span>
   - <span data-ttu-id="cd35a-229">Messages chiffrés envoyés à un domaine particulier</span><span class="sxs-lookup"><span data-stu-id="cd35a-229">Encrypted emails sent to a particular domain</span></span>

7. <span data-ttu-id="cd35a-230">Dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité des messages appliquer la** personnalisation \> **aux messages OME**.</span><span class="sxs-lookup"><span data-stu-id="cd35a-230">From **Do the following**, select **Modify the message security** \> **Apply custom branding to OME messages**.</span></span> <span data-ttu-id="cd35a-231">Ensuite, dans la liste déroulante, sélectionnez un modèle de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="cd35a-231">Next, from the drop-down, select a branding template.</span></span>

8. <span data-ttu-id="cd35a-232">Module Vous pouvez configurer la règle de flux de messagerie pour appliquer le chiffrement et la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="cd35a-232">(Optional) You can configure the mail flow rule to apply encryption and custom branding.</span></span> <span data-ttu-id="cd35a-233">Dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité des messages**, puis choisissez **appliquer le chiffrement de messages Office 365 et protection des droits**.</span><span class="sxs-lookup"><span data-stu-id="cd35a-233">From **Do the following**, select **Modify the message security**, and then choose **Apply Office 365 Message Encryption and rights protection**.</span></span> <span data-ttu-id="cd35a-234">Sélectionnez un modèle RMS dans la liste, cliquez sur **Enregistrer**, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd35a-234">Select an RMS template from the list, choose **Save**, and then choose **OK**.</span></span>
  
   <span data-ttu-id="cd35a-235">La liste des modèles comprend les modèles et les options par défaut, ainsi que tous les modèles personnalisés que vous créez.</span><span class="sxs-lookup"><span data-stu-id="cd35a-235">The list of templates includes default templates and options and any custom templates you create.</span></span> <span data-ttu-id="cd35a-236">Si la liste est vide, vérifiez que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="cd35a-236">If the list is empty, ensure that you have set up Office 365 Message Encryption with the new capabilities.</span></span> <span data-ttu-id="cd35a-237">Pour obtenir des instructions, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="cd35a-237">For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md).</span></span> <span data-ttu-id="cd35a-238">Pour plus d’informations sur les modèles par défaut, reportez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates).</span><span class="sxs-lookup"><span data-stu-id="cd35a-238">For information about the default templates, see [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates).</span></span> <span data-ttu-id="cd35a-239">Pour plus d’informations sur l’option **ne pas transférer** , reportez-vous à l' [option ne pas transférer pour les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails).</span><span class="sxs-lookup"><span data-stu-id="cd35a-239">For information about the **Do Not Forward** option, see [Do Not Forward option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails).</span></span> <span data-ttu-id="cd35a-240">Pour plus d’informations sur l’option **chiffrer uniquement** , reportez-vous à la rubrique [chiffrer uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).</span><span class="sxs-lookup"><span data-stu-id="cd35a-240">For information about the **encrypt only** option, see [Encrypt Only option for emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).</span></span>

   <span data-ttu-id="cd35a-241">Sélectionnez **Ajouter une action** si vous souhaitez spécifier une autre action.</span><span class="sxs-lookup"><span data-stu-id="cd35a-241">Choose **add action** if you want to specify another action.</span></span>

## <a name="background-color-reference"></a><span data-ttu-id="cd35a-242">Référence de couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="cd35a-242">Background color reference</span></span>

<span data-ttu-id="cd35a-243">Les noms de couleur que vous pouvez utiliser pour la couleur d’arrière-plan sont limités.</span><span class="sxs-lookup"><span data-stu-id="cd35a-243">The color names that you can use for the background color are limited.</span></span> <span data-ttu-id="cd35a-244">Au lieu d’un nom de couleur, vous pouvez utiliser une valeur de code hexadécimal (#RRGGBB).</span><span class="sxs-lookup"><span data-stu-id="cd35a-244">Instead of a color name, you can use a hex code value (#RRGGBB).</span></span> <span data-ttu-id="cd35a-245">Vous pouvez utiliser une valeur de code hexadécimal correspondant à un nom de couleur, ou vous pouvez utiliser une valeur de code hexadécimal personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cd35a-245">You can use a hex code value that corresponds to a color name, or you can use a custom hex code value.</span></span> <span data-ttu-id="cd35a-246">Veillez à placer la valeur de code hexadécimal entre guillemets (par exemple, `"#f0f8ff"` ).</span><span class="sxs-lookup"><span data-stu-id="cd35a-246">Be sure to enclose the hex code value in quotation marks (for example, `"#f0f8ff"`).</span></span>

<span data-ttu-id="cd35a-247">Les noms de couleur d’arrière-plan disponibles et les valeurs de code hexadécimal correspondantes sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cd35a-247">The available background color names and their corresponding hex code values are described in the following table.</span></span>

|<span data-ttu-id="cd35a-248">**Nom de la couleur**</span><span class="sxs-lookup"><span data-stu-id="cd35a-248">**Color name**</span></span>|<span data-ttu-id="cd35a-249">**Code de couleur**</span><span class="sxs-lookup"><span data-stu-id="cd35a-249">**Color code**</span></span>|
|---|---|
|`aliceblue`|<span data-ttu-id="cd35a-250">#f0f8ff</span><span class="sxs-lookup"><span data-stu-id="cd35a-250">#f0f8ff</span></span>|
|`antiquewhite`|<span data-ttu-id="cd35a-251">#faebd7</span><span class="sxs-lookup"><span data-stu-id="cd35a-251">#faebd7</span></span>|
|`aqua`|<span data-ttu-id="cd35a-252">#00ffff</span><span class="sxs-lookup"><span data-stu-id="cd35a-252">#00ffff</span></span>|
|`aquamarine`|<span data-ttu-id="cd35a-253">#7fffd4</span><span class="sxs-lookup"><span data-stu-id="cd35a-253">#7fffd4</span></span>|
|`azure`|<span data-ttu-id="cd35a-254">#f0ffff</span><span class="sxs-lookup"><span data-stu-id="cd35a-254">#f0ffff</span></span>|
|`beige`|<span data-ttu-id="cd35a-255">#f5f5dc</span><span class="sxs-lookup"><span data-stu-id="cd35a-255">#f5f5dc</span></span>|
|`bisque`|<span data-ttu-id="cd35a-256">#ffe4c4</span><span class="sxs-lookup"><span data-stu-id="cd35a-256">#ffe4c4</span></span>|
|`black`|<span data-ttu-id="cd35a-257">#000000</span><span class="sxs-lookup"><span data-stu-id="cd35a-257">#000000</span></span>|
|`blanchedalmond`|<span data-ttu-id="cd35a-258">#ffebcd</span><span class="sxs-lookup"><span data-stu-id="cd35a-258">#ffebcd</span></span>|
|`blue`|<span data-ttu-id="cd35a-259">#0000ff</span><span class="sxs-lookup"><span data-stu-id="cd35a-259">#0000ff</span></span>|
|`blueviolet`|<span data-ttu-id="cd35a-260">#8a2be2</span><span class="sxs-lookup"><span data-stu-id="cd35a-260">#8a2be2</span></span>|
|`brown`|<span data-ttu-id="cd35a-261">#a52a2a</span><span class="sxs-lookup"><span data-stu-id="cd35a-261">#a52a2a</span></span>|
|`burlywood`|<span data-ttu-id="cd35a-262">#deb887</span><span class="sxs-lookup"><span data-stu-id="cd35a-262">#deb887</span></span>|
|`cadetblue`|<span data-ttu-id="cd35a-263">#5f9ea0</span><span class="sxs-lookup"><span data-stu-id="cd35a-263">#5f9ea0</span></span>|
|`chartreuse`|<span data-ttu-id="cd35a-264">#7fff00</span><span class="sxs-lookup"><span data-stu-id="cd35a-264">#7fff00</span></span>|
|`chocolate`|<span data-ttu-id="cd35a-265">#d2691e</span><span class="sxs-lookup"><span data-stu-id="cd35a-265">#d2691e</span></span>|
|`coral`|<span data-ttu-id="cd35a-266">#ff7f50</span><span class="sxs-lookup"><span data-stu-id="cd35a-266">#ff7f50</span></span>|
|`cornflowerblue`|<span data-ttu-id="cd35a-267">#6495ed</span><span class="sxs-lookup"><span data-stu-id="cd35a-267">#6495ed</span></span>|
|`cornsilk`|<span data-ttu-id="cd35a-268">#fff8dc</span><span class="sxs-lookup"><span data-stu-id="cd35a-268">#fff8dc</span></span>|
|`crimson`|<span data-ttu-id="cd35a-269">#dc143c</span><span class="sxs-lookup"><span data-stu-id="cd35a-269">#dc143c</span></span>|
|`cyan`|<span data-ttu-id="cd35a-270">#00ffff</span><span class="sxs-lookup"><span data-stu-id="cd35a-270">#00ffff</span></span>|
|`darkblue`|<span data-ttu-id="cd35a-271">#00008b</span><span class="sxs-lookup"><span data-stu-id="cd35a-271">#00008b</span></span>|
|`darkcyan`|<span data-ttu-id="cd35a-272">#008b8b</span><span class="sxs-lookup"><span data-stu-id="cd35a-272">#008b8b</span></span>|
|`darkgoldenrod`|<span data-ttu-id="cd35a-273">#b8860b</span><span class="sxs-lookup"><span data-stu-id="cd35a-273">#b8860b</span></span>|
|`darkgray`|<span data-ttu-id="cd35a-274">#a9a9a9</span><span class="sxs-lookup"><span data-stu-id="cd35a-274">#a9a9a9</span></span>|
|`darkgreen`|<span data-ttu-id="cd35a-275">#006400</span><span class="sxs-lookup"><span data-stu-id="cd35a-275">#006400</span></span>|
|`darkkhaki`|<span data-ttu-id="cd35a-276">#bdb76b</span><span class="sxs-lookup"><span data-stu-id="cd35a-276">#bdb76b</span></span>|
|`darkmagenta`|<span data-ttu-id="cd35a-277">#8b008b</span><span class="sxs-lookup"><span data-stu-id="cd35a-277">#8b008b</span></span>|
|`darkolivegreen`|<span data-ttu-id="cd35a-278">#556b2f</span><span class="sxs-lookup"><span data-stu-id="cd35a-278">#556b2f</span></span>|
|`darkorange`|<span data-ttu-id="cd35a-279">#ff8c00</span><span class="sxs-lookup"><span data-stu-id="cd35a-279">#ff8c00</span></span>|
|`darkorchid`|<span data-ttu-id="cd35a-280">#9932cc</span><span class="sxs-lookup"><span data-stu-id="cd35a-280">#9932cc</span></span>|
|`darkred`|<span data-ttu-id="cd35a-281">#8b0000</span><span class="sxs-lookup"><span data-stu-id="cd35a-281">#8b0000</span></span>|
|`darksalmon`|<span data-ttu-id="cd35a-282">#e9967a</span><span class="sxs-lookup"><span data-stu-id="cd35a-282">#e9967a</span></span>|
|`darkseagreen`|<span data-ttu-id="cd35a-283">#8fbc8f</span><span class="sxs-lookup"><span data-stu-id="cd35a-283">#8fbc8f</span></span>|
|`darkslateblue`|<span data-ttu-id="cd35a-284">#483d8b</span><span class="sxs-lookup"><span data-stu-id="cd35a-284">#483d8b</span></span>|
|`darkslategray`|<span data-ttu-id="cd35a-285">#2f4f4f</span><span class="sxs-lookup"><span data-stu-id="cd35a-285">#2f4f4f</span></span>|
|`darkturquoise`|<span data-ttu-id="cd35a-286">#00ced1</span><span class="sxs-lookup"><span data-stu-id="cd35a-286">#00ced1</span></span>|
|`darkviolet`|<span data-ttu-id="cd35a-287">#9400d3</span><span class="sxs-lookup"><span data-stu-id="cd35a-287">#9400d3</span></span>|
|`deeppink`|<span data-ttu-id="cd35a-288">#ff1493</span><span class="sxs-lookup"><span data-stu-id="cd35a-288">#ff1493</span></span>|
|`deepskyblue`|<span data-ttu-id="cd35a-289">#00bfff</span><span class="sxs-lookup"><span data-stu-id="cd35a-289">#00bfff</span></span>|
|`dimgray`|<span data-ttu-id="cd35a-290">#696969</span><span class="sxs-lookup"><span data-stu-id="cd35a-290">#696969</span></span>|
|`dodgerblue`|<span data-ttu-id="cd35a-291">#1e90ff</span><span class="sxs-lookup"><span data-stu-id="cd35a-291">#1e90ff</span></span>|
|`firebrick`|<span data-ttu-id="cd35a-292">#b22222</span><span class="sxs-lookup"><span data-stu-id="cd35a-292">#b22222</span></span>|
|`floralwhite`|<span data-ttu-id="cd35a-293">#fffaf0</span><span class="sxs-lookup"><span data-stu-id="cd35a-293">#fffaf0</span></span>|
|`forestgreen`|<span data-ttu-id="cd35a-294">#228b22</span><span class="sxs-lookup"><span data-stu-id="cd35a-294">#228b22</span></span>|
|`fuchsia`|<span data-ttu-id="cd35a-295">#ff00ff</span><span class="sxs-lookup"><span data-stu-id="cd35a-295">#ff00ff</span></span>|
|`gainsboro`|<span data-ttu-id="cd35a-296">#dcdcdc</span><span class="sxs-lookup"><span data-stu-id="cd35a-296">#dcdcdc</span></span>|
|`ghostwhite`|<span data-ttu-id="cd35a-297">#f8f8ff</span><span class="sxs-lookup"><span data-stu-id="cd35a-297">#f8f8ff</span></span>|
|`gold`|<span data-ttu-id="cd35a-298">#ffd700</span><span class="sxs-lookup"><span data-stu-id="cd35a-298">#ffd700</span></span>|
|`goldenrod`|<span data-ttu-id="cd35a-299">#daa520</span><span class="sxs-lookup"><span data-stu-id="cd35a-299">#daa520</span></span>|
|`gray`|<span data-ttu-id="cd35a-300">#808080</span><span class="sxs-lookup"><span data-stu-id="cd35a-300">#808080</span></span>|
|`green`|<span data-ttu-id="cd35a-301">#008000</span><span class="sxs-lookup"><span data-stu-id="cd35a-301">#008000</span></span>|
|`greenyellow`|<span data-ttu-id="cd35a-302">#adff2f</span><span class="sxs-lookup"><span data-stu-id="cd35a-302">#adff2f</span></span>|
|`honeydew`|<span data-ttu-id="cd35a-303">#f0fff0</span><span class="sxs-lookup"><span data-stu-id="cd35a-303">#f0fff0</span></span>|
|`hotpink`|<span data-ttu-id="cd35a-304">#ff69b4</span><span class="sxs-lookup"><span data-stu-id="cd35a-304">#ff69b4</span></span>|
|`indianred`|<span data-ttu-id="cd35a-305">#cd5c5c</span><span class="sxs-lookup"><span data-stu-id="cd35a-305">#cd5c5c</span></span>|
|`indigo`|<span data-ttu-id="cd35a-306">#4b0082</span><span class="sxs-lookup"><span data-stu-id="cd35a-306">#4b0082</span></span>|
|`ivory`|<span data-ttu-id="cd35a-307">#fffff0</span><span class="sxs-lookup"><span data-stu-id="cd35a-307">#fffff0</span></span>|
|`khaki`|<span data-ttu-id="cd35a-308">#f0e68c</span><span class="sxs-lookup"><span data-stu-id="cd35a-308">#f0e68c</span></span>|
|`lavender`|<span data-ttu-id="cd35a-309">#e6e6fa</span><span class="sxs-lookup"><span data-stu-id="cd35a-309">#e6e6fa</span></span>|
|`lavenderblush`|<span data-ttu-id="cd35a-310">#fff0f5</span><span class="sxs-lookup"><span data-stu-id="cd35a-310">#fff0f5</span></span>|
|`lawngreen`|<span data-ttu-id="cd35a-311">#7cfc00</span><span class="sxs-lookup"><span data-stu-id="cd35a-311">#7cfc00</span></span>|
|`lemonchiffon`|<span data-ttu-id="cd35a-312">#fffacd</span><span class="sxs-lookup"><span data-stu-id="cd35a-312">#fffacd</span></span>|
|`lightblue`|<span data-ttu-id="cd35a-313">#add8e6</span><span class="sxs-lookup"><span data-stu-id="cd35a-313">#add8e6</span></span>|
|`lightcoral`|<span data-ttu-id="cd35a-314">#f08080</span><span class="sxs-lookup"><span data-stu-id="cd35a-314">#f08080</span></span>|
|`lightcyan`|<span data-ttu-id="cd35a-315">#e0ffff</span><span class="sxs-lookup"><span data-stu-id="cd35a-315">#e0ffff</span></span>|
|`lightgoldenrodyellow`|<span data-ttu-id="cd35a-316">#fafad2</span><span class="sxs-lookup"><span data-stu-id="cd35a-316">#fafad2</span></span>|
|`lightgray`|<span data-ttu-id="cd35a-317">#d3d3d3</span><span class="sxs-lookup"><span data-stu-id="cd35a-317">#d3d3d3</span></span>|
|`lightgrey`|<span data-ttu-id="cd35a-318">#d3d3d3</span><span class="sxs-lookup"><span data-stu-id="cd35a-318">#d3d3d3</span></span>|
|`lightgreen`|<span data-ttu-id="cd35a-319">#90ee90</span><span class="sxs-lookup"><span data-stu-id="cd35a-319">#90ee90</span></span>|
|`lightpink`|<span data-ttu-id="cd35a-320">#ffb6c1</span><span class="sxs-lookup"><span data-stu-id="cd35a-320">#ffb6c1</span></span>|
|`lightsalmon`|<span data-ttu-id="cd35a-321">#ffa07a</span><span class="sxs-lookup"><span data-stu-id="cd35a-321">#ffa07a</span></span>|
|`lightseagreen`|<span data-ttu-id="cd35a-322">#20b2aa</span><span class="sxs-lookup"><span data-stu-id="cd35a-322">#20b2aa</span></span>|
|`lightskyblue`|<span data-ttu-id="cd35a-323">#87cefa</span><span class="sxs-lookup"><span data-stu-id="cd35a-323">#87cefa</span></span>|
|`lightslategray`|<span data-ttu-id="cd35a-324">#778899</span><span class="sxs-lookup"><span data-stu-id="cd35a-324">#778899</span></span>|
|`lightsteelblue`|<span data-ttu-id="cd35a-325">#b0c4de</span><span class="sxs-lookup"><span data-stu-id="cd35a-325">#b0c4de</span></span>|
|`lightyellow`|<span data-ttu-id="cd35a-326">#ffffe0</span><span class="sxs-lookup"><span data-stu-id="cd35a-326">#ffffe0</span></span>|
|`lime`|<span data-ttu-id="cd35a-327">#00ff00</span><span class="sxs-lookup"><span data-stu-id="cd35a-327">#00ff00</span></span>|
|`limegreen`|<span data-ttu-id="cd35a-328">#32cd32</span><span class="sxs-lookup"><span data-stu-id="cd35a-328">#32cd32</span></span>|
|`linen`|<span data-ttu-id="cd35a-329">#faf0e6</span><span class="sxs-lookup"><span data-stu-id="cd35a-329">#faf0e6</span></span>|
|`magenta`|<span data-ttu-id="cd35a-330">#ff00ff</span><span class="sxs-lookup"><span data-stu-id="cd35a-330">#ff00ff</span></span>|
|`maroon`|<span data-ttu-id="cd35a-331">#800000</span><span class="sxs-lookup"><span data-stu-id="cd35a-331">#800000</span></span>|
|`mediumaquamarine`|<span data-ttu-id="cd35a-332">#66cdaa</span><span class="sxs-lookup"><span data-stu-id="cd35a-332">#66cdaa</span></span>|
|`mediumblue`|<span data-ttu-id="cd35a-333">#0000cd</span><span class="sxs-lookup"><span data-stu-id="cd35a-333">#0000cd</span></span>|
|`mediumorchid`|<span data-ttu-id="cd35a-334">#ba55d3</span><span class="sxs-lookup"><span data-stu-id="cd35a-334">#ba55d3</span></span>|
|`mediumpurple`|<span data-ttu-id="cd35a-335">#9370db</span><span class="sxs-lookup"><span data-stu-id="cd35a-335">#9370db</span></span>|
|`mediumseagreen`|<span data-ttu-id="cd35a-336">#3cb371</span><span class="sxs-lookup"><span data-stu-id="cd35a-336">#3cb371</span></span>|
|`mediumslateblue`|<span data-ttu-id="cd35a-337">#7b68ee</span><span class="sxs-lookup"><span data-stu-id="cd35a-337">#7b68ee</span></span>|
|`mediumspringgreen`|<span data-ttu-id="cd35a-338">#00fa9a</span><span class="sxs-lookup"><span data-stu-id="cd35a-338">#00fa9a</span></span>|
|`mediumturquoise`|<span data-ttu-id="cd35a-339">#48d1cc</span><span class="sxs-lookup"><span data-stu-id="cd35a-339">#48d1cc</span></span>|
|`mediumvioletred`|<span data-ttu-id="cd35a-340">#c71585</span><span class="sxs-lookup"><span data-stu-id="cd35a-340">#c71585</span></span>|
|`midnightblue`|<span data-ttu-id="cd35a-341">#191970</span><span class="sxs-lookup"><span data-stu-id="cd35a-341">#191970</span></span>|
|`mintcream`|<span data-ttu-id="cd35a-342">#f5fffa</span><span class="sxs-lookup"><span data-stu-id="cd35a-342">#f5fffa</span></span>|
|`mistyrose`|<span data-ttu-id="cd35a-343">#ffe4e1</span><span class="sxs-lookup"><span data-stu-id="cd35a-343">#ffe4e1</span></span>|
|`moccasin`|<span data-ttu-id="cd35a-344">#ffe4b5</span><span class="sxs-lookup"><span data-stu-id="cd35a-344">#ffe4b5</span></span>|
|`navajowhite`|<span data-ttu-id="cd35a-345">#ffdead</span><span class="sxs-lookup"><span data-stu-id="cd35a-345">#ffdead</span></span>|
|`navy`|<span data-ttu-id="cd35a-346">#000080</span><span class="sxs-lookup"><span data-stu-id="cd35a-346">#000080</span></span>|
|`oldlace`|<span data-ttu-id="cd35a-347">#fdf5e6</span><span class="sxs-lookup"><span data-stu-id="cd35a-347">#fdf5e6</span></span>|
|`olive`|<span data-ttu-id="cd35a-348">#808000</span><span class="sxs-lookup"><span data-stu-id="cd35a-348">#808000</span></span>|
|`olivedrab`|<span data-ttu-id="cd35a-349">#6b8e23</span><span class="sxs-lookup"><span data-stu-id="cd35a-349">#6b8e23</span></span>|
|`orange`|<span data-ttu-id="cd35a-350">#ffa500</span><span class="sxs-lookup"><span data-stu-id="cd35a-350">#ffa500</span></span>|
|`orangered`|<span data-ttu-id="cd35a-351">#ff4500</span><span class="sxs-lookup"><span data-stu-id="cd35a-351">#ff4500</span></span>|
|`orchid`|<span data-ttu-id="cd35a-352">#da70d6</span><span class="sxs-lookup"><span data-stu-id="cd35a-352">#da70d6</span></span>|
|`palegoldenrod`|<span data-ttu-id="cd35a-353">#eee8aa</span><span class="sxs-lookup"><span data-stu-id="cd35a-353">#eee8aa</span></span>|
|`palegreen`|<span data-ttu-id="cd35a-354">#98fb98</span><span class="sxs-lookup"><span data-stu-id="cd35a-354">#98fb98</span></span>|
|`paleturquoise`|<span data-ttu-id="cd35a-355">#afeeee</span><span class="sxs-lookup"><span data-stu-id="cd35a-355">#afeeee</span></span>|
|`palevioletred`|<span data-ttu-id="cd35a-356">#db7093</span><span class="sxs-lookup"><span data-stu-id="cd35a-356">#db7093</span></span>|
|`papayawhip`|<span data-ttu-id="cd35a-357">#ffefd5</span><span class="sxs-lookup"><span data-stu-id="cd35a-357">#ffefd5</span></span>|
|`peachpuff`|<span data-ttu-id="cd35a-358">#ffdab9</span><span class="sxs-lookup"><span data-stu-id="cd35a-358">#ffdab9</span></span>|
|`peru`|<span data-ttu-id="cd35a-359">#cd853f</span><span class="sxs-lookup"><span data-stu-id="cd35a-359">#cd853f</span></span>|
|`pink`|<span data-ttu-id="cd35a-360">#ffc0cb</span><span class="sxs-lookup"><span data-stu-id="cd35a-360">#ffc0cb</span></span>|
|`plum`|<span data-ttu-id="cd35a-361">#dda0dd</span><span class="sxs-lookup"><span data-stu-id="cd35a-361">#dda0dd</span></span>|
|`powderblue`|<span data-ttu-id="cd35a-362">#b0e0e6</span><span class="sxs-lookup"><span data-stu-id="cd35a-362">#b0e0e6</span></span>|
|`purple`|<span data-ttu-id="cd35a-363">#800080</span><span class="sxs-lookup"><span data-stu-id="cd35a-363">#800080</span></span>|
|`red`|<span data-ttu-id="cd35a-364">#ff0000</span><span class="sxs-lookup"><span data-stu-id="cd35a-364">#ff0000</span></span>|
|`rosybrown`|<span data-ttu-id="cd35a-365">#bc8f8f</span><span class="sxs-lookup"><span data-stu-id="cd35a-365">#bc8f8f</span></span>|
|`royalblue`|<span data-ttu-id="cd35a-366">#4169e1</span><span class="sxs-lookup"><span data-stu-id="cd35a-366">#4169e1</span></span>|
|`saddlebrown`|<span data-ttu-id="cd35a-367">#8b4513</span><span class="sxs-lookup"><span data-stu-id="cd35a-367">#8b4513</span></span>|
|`salmon`|<span data-ttu-id="cd35a-368">#fa8072</span><span class="sxs-lookup"><span data-stu-id="cd35a-368">#fa8072</span></span>|
|`sandybrown`|<span data-ttu-id="cd35a-369">#f4a460</span><span class="sxs-lookup"><span data-stu-id="cd35a-369">#f4a460</span></span>|
|`seagreen`|<span data-ttu-id="cd35a-370">#00ff00</span><span class="sxs-lookup"><span data-stu-id="cd35a-370">#00ff00</span></span>|
|`seashell`|<span data-ttu-id="cd35a-371">#fff5ee</span><span class="sxs-lookup"><span data-stu-id="cd35a-371">#fff5ee</span></span>|
|`sienna`|<span data-ttu-id="cd35a-372">#a0522d</span><span class="sxs-lookup"><span data-stu-id="cd35a-372">#a0522d</span></span>|
|`silver`|<span data-ttu-id="cd35a-373">#c0c0c0</span><span class="sxs-lookup"><span data-stu-id="cd35a-373">#c0c0c0</span></span>|
|`skyblue`|<span data-ttu-id="cd35a-374">#87ceeb</span><span class="sxs-lookup"><span data-stu-id="cd35a-374">#87ceeb</span></span>|
|`slateblue`|<span data-ttu-id="cd35a-375">#6a5acd</span><span class="sxs-lookup"><span data-stu-id="cd35a-375">#6a5acd</span></span>|
|`slategray`|<span data-ttu-id="cd35a-376">#708090</span><span class="sxs-lookup"><span data-stu-id="cd35a-376">#708090</span></span>|
|`snow`|<span data-ttu-id="cd35a-377">#fffafa</span><span class="sxs-lookup"><span data-stu-id="cd35a-377">#fffafa</span></span>|
|`springgreen`|<span data-ttu-id="cd35a-378">#00ff7f</span><span class="sxs-lookup"><span data-stu-id="cd35a-378">#00ff7f</span></span>|
|`steelblue`|<span data-ttu-id="cd35a-379">#4682b4</span><span class="sxs-lookup"><span data-stu-id="cd35a-379">#4682b4</span></span>|
|`tan`|<span data-ttu-id="cd35a-380">#d2b48c</span><span class="sxs-lookup"><span data-stu-id="cd35a-380">#d2b48c</span></span>|
|`teal`|<span data-ttu-id="cd35a-381">#008080</span><span class="sxs-lookup"><span data-stu-id="cd35a-381">#008080</span></span>|
|`thistle`|<span data-ttu-id="cd35a-382">#d8bfd8</span><span class="sxs-lookup"><span data-stu-id="cd35a-382">#d8bfd8</span></span>|
|`tomato`|<span data-ttu-id="cd35a-383">#ff6347</span><span class="sxs-lookup"><span data-stu-id="cd35a-383">#ff6347</span></span>|
|`turquoise`|<span data-ttu-id="cd35a-384">#40e0d0</span><span class="sxs-lookup"><span data-stu-id="cd35a-384">#40e0d0</span></span>|
|`violet`|<span data-ttu-id="cd35a-385">#ee82ee</span><span class="sxs-lookup"><span data-stu-id="cd35a-385">#ee82ee</span></span>|
|`wheat`|<span data-ttu-id="cd35a-386">#f5deb3</span><span class="sxs-lookup"><span data-stu-id="cd35a-386">#f5deb3</span></span>|
|`white`|<span data-ttu-id="cd35a-387">#ffffff</span><span class="sxs-lookup"><span data-stu-id="cd35a-387">#ffffff</span></span>|
|`whitesmoke`|<span data-ttu-id="cd35a-388">#f5f5f5</span><span class="sxs-lookup"><span data-stu-id="cd35a-388">#f5f5f5</span></span>|
|`yellow`|<span data-ttu-id="cd35a-389">#ffff00</span><span class="sxs-lookup"><span data-stu-id="cd35a-389">#ffff00</span></span>|
|`yellowgreen`|<span data-ttu-id="cd35a-390">#9acd32</span><span class="sxs-lookup"><span data-stu-id="cd35a-390">#9acd32</span></span>|
