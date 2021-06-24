---
title: Documents sécurisés dans Microsoft Defender pour Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: kshi
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez comment Coffre documents dans Microsoft 365 E5 ou Microsoft 365 E5 Sécurité.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 0e1bd2150a04e51e0d06c6cd1c17a71a032df1a5
ms.sourcegitcommit: ebb1c3b4d94058a58344317beb9475c8a2eae9a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53108606"
---
# <a name="safe-documents-in-microsoft-365-e5"></a><span data-ttu-id="1d2b2-103">Documents sécurisés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="1d2b2-103">Safe Documents in Microsoft 365 E5</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1d2b2-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1d2b2-104">**Applies to**</span></span>
- [<span data-ttu-id="1d2b2-105">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1d2b2-105">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="1d2b2-106">Coffre Les documents sont une fonctionnalité de Microsoft 365 E5 ou de Microsoft 365 E5 Sécurité qui utilise [Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour [](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653) le point de terminaison pour analyser les documents et les fichiers ouverts en affichage protégé ou Application Guard [pour Office](https://support.microsoft.com/topic/9e0fb9c2-ffad-43bf-8ba3-78f785fdba46).</span><span class="sxs-lookup"><span data-stu-id="1d2b2-106">Safe Documents is a feature in Microsoft 365 E5 or Microsoft 365 E5 Security that uses [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653) or [Application Guard for Office](https://support.microsoft.com/topic/9e0fb9c2-ffad-43bf-8ba3-78f785fdba46).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1d2b2-107">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1d2b2-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="1d2b2-108">Coffre Les documents sont disponibles uniquement pour les *utilisateurs Microsoft 365 E5* ou *Microsoft 365 E5 Sécurité* licences.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-108">Safe Documents is available only to users with *Microsoft 365 E5* or *Microsoft 365 E5 Security* licenses.</span></span> <span data-ttu-id="1d2b2-109">Ces licences ne sont pas incluses dans Microsoft Defender pour Office 365 plans.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-109">These licenses are not included in Microsoft Defender for Office 365 plans.</span></span>

- <span data-ttu-id="1d2b2-110">Coffre Les documents sont pris en charge Applications Microsoft 365 pour les grandes entreprises (anciennement Office 365 ProPlus) version 2004 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-110">Safe Documents is supported in Microsoft 365 Apps for enterprise (formerly known as Office 365 ProPlus) version 2004 or later.</span></span>

- <span data-ttu-id="1d2b2-111">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-111">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="1d2b2-112">Pour aller directement à la page **Coffre pièces jointes,** utilisez <https://security.microsoft.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="1d2b2-112">To go directly to the **Safe Attachments** page, use <https://security.microsoft.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="1d2b2-113">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="1d2b2-113">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="1d2b2-114">Vous avez besoin d’autorisations **Exchange Online** pour pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="1d2b2-114">You need permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="1d2b2-115">Pour configurer les Coffre Documents, vous devez être membre  des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-115">To configure Safe Documents settings, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="1d2b2-116">Pour accéder en lecture seule aux paramètres Coffre Documents, vous  devez être  membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-116">For read-only access to Safe Documents settings, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="1d2b2-117">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="1d2b2-117">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="1d2b2-118">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-118">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="1d2b2-119">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1d2b2-119">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="1d2b2-120">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-120">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

### <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="1d2b2-121">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="1d2b2-121">How does Microsoft handle your data?</span></span>

<span data-ttu-id="1d2b2-122">Pour vous protéger, Coffre Documents envoie des fichiers au cloud [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-122">To keep you protected, Safe Documents sends files to the [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span> <span data-ttu-id="1d2b2-123">Pour plus d’informations sur la façon dont Microsoft Defender pour le point de terminaison gère vos données, voir : Microsoft Defender pour le stockage et la confidentialité des données de [point de terminaison.](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span><span class="sxs-lookup"><span data-stu-id="1d2b2-123">Details on how Microsoft Defender for Endpoint handles your data can be found here: [Microsoft Defender for Endpoint data storage and privacy](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span>

<span data-ttu-id="1d2b2-124">Les fichiers envoyés par Coffre Documents ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse (généralement, moins de 24 heures).</span><span class="sxs-lookup"><span data-stu-id="1d2b2-124">Files sent by Safe Documents are not retained in Defender beyond the time needed for analysis (typically, less than 24 hours).</span></span>

## <a name="use-the-microsoft-365-defender-to-configure-safe-documents"></a><span data-ttu-id="1d2b2-125">Utiliser la Microsoft 365 Defender pour configurer les documents Coffre documents</span><span class="sxs-lookup"><span data-stu-id="1d2b2-125">Use the Microsoft 365 Defender to configure Safe Documents</span></span>

1. <span data-ttu-id="1d2b2-126">Ouvrez le portail Microsoft 365 Defender et  allez à la section Stratégies de collaboration & de messagerie & règles de stratégies de menaces dans la \>  \>  \>  section \> **Stratégies Coffre pièces jointes.**</span><span class="sxs-lookup"><span data-stu-id="1d2b2-126">Open the Microsoft 365 Defender portal and go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="1d2b2-127">Dans la page **Coffre pièces jointes,** cliquez **sur Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="1d2b2-127">On the **Safe Attachments** page, click **Global settings**.</span></span>

3. <span data-ttu-id="1d2b2-128">Dans le **volant des paramètres globaux** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d2b2-128">In the **Global settings** fly out that appears, configure the following settings:</span></span>
   - <span data-ttu-id="1d2b2-129">**Activer Coffre documents** pour Office clients : déplacez le basculement vers la droite pour activer la fonctionnalité : ![ Activer/ ](../../media/scc-toggle-on.png) Activer.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-129">**Turn on Safe Documents for Office clients**: Move the toggle to the right to turn on the feature: ![Toggle on](../../media/scc-toggle-on.png).</span></span>
   - <span data-ttu-id="1d2b2-130">Autoriser les utilisateurs à cliquer dans le affichage protégé, même si **Coffre Documents a** identifié le fichier comme malveillant : nous vous recommandons de laisser cette option désactivée (laissez le bouton bascule vers la gauche : Bascule). ![ ](../../media/scc-toggle-off.png)</span><span class="sxs-lookup"><span data-stu-id="1d2b2-130">**Allow people to click through Protected View even if Safe Documents identified the file as malicious**: We recommend that you leave this option turned off (leave the toggle to the left: ![Toggle off](../../media/scc-toggle-off.png)).</span></span>

   <span data-ttu-id="1d2b2-131">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-131">When you're finished, click **Save**.</span></span>

   ![Coffre Documents settings after selecting Global settings on the Coffre Attachments page.](../../media/safe-docs-global-settings.png)

### <a name="use-exchange-online-powershell-to-configure-safe-documents"></a><span data-ttu-id="1d2b2-133">Utiliser Exchange Online PowerShell pour configurer Coffre Documents</span><span class="sxs-lookup"><span data-stu-id="1d2b2-133">Use Exchange Online PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="1d2b2-134">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1d2b2-134">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- <span data-ttu-id="1d2b2-135">Le _paramètre EnableSafeDocs_ active ou désactive Coffre Documents pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-135">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>
- <span data-ttu-id="1d2b2-136">Le _paramètre AllowSafeDocsOpen_ permet ou empêche les utilisateurs de quitter le affichage protégé (c’est-à-dire, l’ouverture du document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-136">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="1d2b2-137">Cet exemple active Coffre documents pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents qui ont été identifiés comme malveillants en affichage protégé.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-137">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="1d2b2-138">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="1d2b2-138">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="onboard-to-the-microsoft-defender-for-endpoint-service-to-enable-auditing-capabilities"></a><span data-ttu-id="1d2b2-139">Intégration au service Microsoft Defender for Endpoint pour activer les fonctionnalités d’audit</span><span class="sxs-lookup"><span data-stu-id="1d2b2-139">Onboard to the Microsoft Defender for Endpoint Service to enable auditing capabilities</span></span>

<span data-ttu-id="1d2b2-140">Pour déployer Microsoft Defender pour endpoint, vous devez passer par les différentes phases de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-140">To deploy Microsoft Defender for Endpoint, you need to go through the various phases of deployment.</span></span> <span data-ttu-id="1d2b2-141">Après l’intégration, vous pouvez configurer les fonctionnalités d’audit dans Microsoft 365 Defender portail.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-141">After onboarding, you can configure auditing capabilities in the Microsoft 365 Defender portal.</span></span>

<span data-ttu-id="1d2b2-142">Pour plus d’informations, [voir Intégrer au service Microsoft Defender for Endpoint.](/microsoft-365/security/defender-endpoint/onboarding)</span><span class="sxs-lookup"><span data-stu-id="1d2b2-142">To learn more, see [Onboard to the Microsoft Defender for Endpoint service](/microsoft-365/security/defender-endpoint/onboarding).</span></span> <span data-ttu-id="1d2b2-143">Si vous avez besoin d’aide supplémentaire, reportez-vous à Résoudre les problèmes d’intégration de Microsoft Defender pour les points [de terminaison.](/microsoft-365/security/defender-endpoint/troubleshoot-onboarding)</span><span class="sxs-lookup"><span data-stu-id="1d2b2-143">If you need additional help, refer to [Troubleshoot Microsoft Defender for Endpoint onboarding issues](/microsoft-365/security/defender-endpoint/troubleshoot-onboarding).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="1d2b2-144">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="1d2b2-144">How do I know this worked?</span></span>

<span data-ttu-id="1d2b2-145">Pour vérifier que vous avez activé et configuré Coffre Documents, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d2b2-145">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="1d2b2-146">Dans le portail Microsoft 365 Defender, consultez la page Stratégies de collaboration de messagerie **&** stratégies de & Règles de stratégies de \>  \>  \>  menaces section \> **Stratégies Coffre Paramètres** \>    globaux des pièces jointes, puis vérifiez que l’outil Activer les documents Coffre pour les clients Office et autoriser les utilisateurs à cliquer en affichage protégé même si Coffre Documents identifie le fichier comme des paramètres malveillants.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-146">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments** \> **Global settings**, and verify the **Turn on Safe Documents for Office clients** and **Allow people to click through Protected View even if Safe Documents identifies the file as malicious** settings.</span></span>

- <span data-ttu-id="1d2b2-147">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="1d2b2-147">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```

- <span data-ttu-id="1d2b2-148">Les fichiers suivants sont disponibles pour tester la protection Coffre documents.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-148">The following files are available to test Safe Documents protection.</span></span> <span data-ttu-id="1d2b2-149">Ces documents sont similaires au fichier EICAR.TXT pour tester les solutions antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-149">These documents are similar to the EICAR.TXT file for testing anti-malware and anti-virus solutions.</span></span> <span data-ttu-id="1d2b2-150">Les fichiers ne sont pas dangereux, mais ils déclenchent la protection Coffre documents.</span><span class="sxs-lookup"><span data-stu-id="1d2b2-150">The files are not harmful, but they will trigger Safe Documents protection.</span></span>

  - [<span data-ttu-id="1d2b2-151">SafeDocsDemo.docx</span><span class="sxs-lookup"><span data-stu-id="1d2b2-151">SafeDocsDemo.docx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.docx)
  - [<span data-ttu-id="1d2b2-152">SafeDocsDemo.pptx</span><span class="sxs-lookup"><span data-stu-id="1d2b2-152">SafeDocsDemo.pptx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.pptx)
  - [<span data-ttu-id="1d2b2-153">SafeDocsDemo.xlsx</span><span class="sxs-lookup"><span data-stu-id="1d2b2-153">SafeDocsDemo.xlsx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.xlsx)
