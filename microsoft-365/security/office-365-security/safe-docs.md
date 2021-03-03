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
description: Découvrez la sécurité des documents sécurisés dans Microsoft 365 E5 ou Microsoft 365 E5 Security.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 75dfa9e5687a4c4b561067190e7ce338074b2f66
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50407419"
---
# <a name="safe-documents-in-microsoft-365-e5"></a><span data-ttu-id="60458-103">Documents sécurisés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="60458-103">Safe Documents in Microsoft 365 E5</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="60458-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="60458-104">**Applies to**</span></span>
- [<span data-ttu-id="60458-105">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="60458-105">Microsoft Defender for Office 365 plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="60458-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="60458-106">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="60458-107">La fonctionnalité Documents sécurisés dans Microsoft 365 E5 ou Microsoft 365 E5 Security utilise [Microsoft Defender pour](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) le point de terminaison pour analyser les documents et les fichiers ouverts en affichage protégé. [](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653)</span><span class="sxs-lookup"><span data-stu-id="60458-107">Safe Documents is a feature in Microsoft 365 E5 or Microsoft 365 E5 Security that uses [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="60458-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="60458-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="60458-109">Les documents sécurisés sont disponibles uniquement pour les utilisateurs titulaires de licences De sécurité *Microsoft 365 E5* ou *Microsoft 365 E5.*</span><span class="sxs-lookup"><span data-stu-id="60458-109">Safe Documents is available only to users with *Microsoft 365 E5* or *Microsoft 365 E5 Security* licenses.</span></span> <span data-ttu-id="60458-110">Ces licences ne sont pas incluses dans les plans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="60458-110">These licenses are not included in Microsoft Defender for Office 365 plans.</span></span>

- <span data-ttu-id="60458-111">La sécurité des documents est prise en charge dans Microsoft 365 Apps for enterprise (anciennement Office 365 ProPlus) version 2004 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="60458-111">Safe Documents is supported in Microsoft 365 Apps for enterprise (formerly known as Office 365 ProPlus) version 2004 or later.</span></span>

- <span data-ttu-id="60458-112">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="60458-112">You open the Security & Compliance Center at <https://protection.office.com>.</span></span> <span data-ttu-id="60458-113">Pour aller directement à la page Pièces **jointes sécurisées ATP,** ouvrez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="60458-113">To go directly to the **ATP Safe Attachments** page, open <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="60458-114">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="60458-114">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="60458-115">Des autorisations doivent vous être attribuées dans **Exchange Online** avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="60458-115">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="60458-116">Pour configurer les paramètres des documents sécurisés,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur de** la sécurité.</span><span class="sxs-lookup"><span data-stu-id="60458-116">To configure Safe Documents settings, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="60458-117">Pour accéder en lecture seule aux paramètres des documents  sécurisés,  vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="60458-117">For read-only access to Safe Documents settings, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="60458-118">Pour plus d'informations, voir [Permissions en échange en ligne](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="60458-118">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="60458-119">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux _utilisateurs_ les autorisations et autorisations requises pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="60458-119">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="60458-120">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="60458-120">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="60458-121">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60458-121">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

### <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="60458-122">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="60458-122">How does Microsoft handle your data?</span></span>

<span data-ttu-id="60458-123">Pour vous protéger, les documents sécurisés envoient des fichiers au cloud [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="60458-123">To keep you protected, Safe Documents sends files to the [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span> <span data-ttu-id="60458-124">Pour plus d’informations sur la façon dont Microsoft Defender pour le point de terminaison gère vos données, voir : Microsoft Defender pour le stockage et la confidentialité des données de [point de terminaison.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span><span class="sxs-lookup"><span data-stu-id="60458-124">Details on how Microsoft Defender for Endpoint handles your data can be found here: [Microsoft Defender for Endpoint data storage and privacy](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span>

<span data-ttu-id="60458-125">Les fichiers envoyés par des documents sécurisés ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse (généralement, moins de 24 heures).</span><span class="sxs-lookup"><span data-stu-id="60458-125">Files sent by Safe Documents are not retained in Defender beyond the time needed for analysis (typically, less than 24 hours).</span></span>

## <a name="use-the-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="60458-126">Utiliser le Centre de sécurité & conformité pour configurer des documents sécurisés</span><span class="sxs-lookup"><span data-stu-id="60458-126">Use the Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="60458-127">Dans le Centre de sécurité &  conformité, allez dans Stratégie de gestion des menaces - Pièces jointes sécurisées , puis cliquez sur \>  \>  **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="60458-127">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="60458-128">Dans le **volant des paramètres globaux** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="60458-128">In the **Global settings** fly out that appears, configure the following settings:</span></span>

   - <span data-ttu-id="60458-129">**Activer les documents sécurisés pour les clients Office**: déplacez le basculement vers la droite pour activer la fonctionnalité : ![ Activer/ ](../../media/scc-toggle-on.png) Activer.</span><span class="sxs-lookup"><span data-stu-id="60458-129">**Turn on Safe Documents for Office clients**: Move the toggle to the right to turn on the feature: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

   - <span data-ttu-id="60458-130">Autoriser les utilisateurs à cliquer dans le affichage protégé, même si les **documents sécurisés identifient** le fichier comme malveillant : nous vous recommandons de laisser cette option désactivée (laissez le bouton bascule vers la gauche : ![ ](../../media/scc-toggle-off.png) bascule).</span><span class="sxs-lookup"><span data-stu-id="60458-130">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious**: We recommend that you leave this option turned off (leave the toggle to the left: ![Toggle off](../../media/scc-toggle-off.png)).</span></span>

   <span data-ttu-id="60458-131">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60458-131">When you're finished, click **Save**.</span></span>

   ![Paramètres de documents sécurisés après la sélection des paramètres globaux dans la page Pièces jointes sécurisées.](../../media/safe-docs.png)

### <a name="use-exchange-online-powershell-to-configure-safe-documents"></a><span data-ttu-id="60458-133">Utiliser Exchange Online PowerShell pour configurer des documents sécurisés</span><span class="sxs-lookup"><span data-stu-id="60458-133">Use Exchange Online PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="60458-134">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="60458-134">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- <span data-ttu-id="60458-135">Le _paramètre EnableSafeDocs_ active ou désactive les documents sécurisés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="60458-135">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>
- <span data-ttu-id="60458-136">Le _paramètre AllowSafeDocsOpen_ permet ou empêche les utilisateurs de quitter le affichage protégé (c’est-à-dire, l’ouverture du document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="60458-136">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="60458-137">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents qui ont été identifiés comme malveillants en affichage protégé.</span><span class="sxs-lookup"><span data-stu-id="60458-137">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="60458-138">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="60458-138">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="60458-139">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="60458-139">How do I know this worked?</span></span>

<span data-ttu-id="60458-140">Pour vérifier que vous avez activé et configuré les documents sécurisés, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="60458-140">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="60458-141">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments,** click Global **settings**, and verify the Turn on Safe Documents for Office **clients** and Allow people to click **through Protected View even if Safe Documents identifies the file as malicious** settings.</span><span class="sxs-lookup"><span data-stu-id="60458-141">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, click **Global settings**, and verify the **Turn on Safe Documents for Office clients** and **Allow people to click through Protected View even if Safe Documents identifies the file as malicious** settings.</span></span>

- <span data-ttu-id="60458-142">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="60458-142">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```

- <span data-ttu-id="60458-143">Les fichiers suivants sont disponibles pour tester la protection des documents sécurisés.</span><span class="sxs-lookup"><span data-stu-id="60458-143">The following files are available to test Safe Documents protection.</span></span> <span data-ttu-id="60458-144">Ces documents sont similaires au fichier EICAR.TXT pour tester les solutions antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="60458-144">These documents are similar to the EICAR.TXT file for testing anti-malware and anti-virus solutions.</span></span> <span data-ttu-id="60458-145">Les fichiers ne sont pas dangereux, mais ils déclenchent la protection des documents sécurisés.</span><span class="sxs-lookup"><span data-stu-id="60458-145">The files are not harmful, but they will trigger Safe Documents protection.</span></span>

  - [<span data-ttu-id="60458-146">SafeDocsDemo.docx</span><span class="sxs-lookup"><span data-stu-id="60458-146">SafeDocsDemo.docx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.docx)
  - [<span data-ttu-id="60458-147">SafeDocsDemo.pptx</span><span class="sxs-lookup"><span data-stu-id="60458-147">SafeDocsDemo.pptx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.pptx)
  - [<span data-ttu-id="60458-148">SafeDocsDemo.xlsx</span><span class="sxs-lookup"><span data-stu-id="60458-148">SafeDocsDemo.xlsx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.xlsx)
