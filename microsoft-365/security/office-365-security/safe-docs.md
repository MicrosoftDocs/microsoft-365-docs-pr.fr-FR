---
title: Documents sécurisés dans Microsoft Defender pour Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: kshi
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez les documents sûrs dans Microsoft 365 E5 ou Microsoft 365 E5 sécurité.
ms.openlocfilehash: 1bf802422dc05babaf5e2616468f8326b7007dc8
ms.sourcegitcommit: 29eb89b8ba0628fbef350e8995d2c38369a4ffa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "49682936"
---
# <a name="safe-documents-in-microsoft-365-e5"></a><span data-ttu-id="fb6a1-103">Documents sécurisés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="fb6a1-103">Safe Documents in Microsoft 365 E5</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="fb6a1-104">Documents approuvés est une fonctionnalité de Microsoft 365 E5 ou Microsoft 365 E5 sécurité qui utilise [Microsoft Defender pour le point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyser des documents et des fichiers ouverts en [mode protégé](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-104">Safe Documents is a feature in Microsoft 365 E5 or Microsoft 365 E5 Security that uses [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="fb6a1-105">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fb6a1-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="fb6a1-106">Les documents approuvés sont disponibles uniquement pour les utilisateurs disposant de licences de sécurité Microsoft *365 E5* ou *Microsoft 365 E5* .</span><span class="sxs-lookup"><span data-stu-id="fb6a1-106">Safe Documents is available only to users with *Microsoft 365 E5* or *Microsoft 365 E5 Security* licenses.</span></span> <span data-ttu-id="fb6a1-107">Ces licences ne sont pas incluses dans les plans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-107">These licenses are not included in Microsoft Defender for Office 365 plans.</span></span>

- <span data-ttu-id="fb6a1-108">Les documents approuvés sont pris en charge dans les applications Microsoft 365 pour entreprise (anciennement appelé Office 365 ProPlus) version 2004 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-108">Safe Documents is supported in Microsoft 365 Apps for enterprise (formerly known as Office 365 ProPlus) version 2004 or later.</span></span>

- <span data-ttu-id="fb6a1-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-109">You open the Security & Compliance Center at <https://protection.office.com>.</span></span> <span data-ttu-id="fb6a1-110">Pour accéder directement à la page **pièces jointes approuvées ATP** , ouvrez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="fb6a1-110">To go directly to the **ATP Safe Attachments** page, open <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="fb6a1-111">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="fb6a1-112">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-112">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="fb6a1-113">Pour configurer les paramètres des documents approuvés, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="fb6a1-113">To configure Safe Documents settings, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="fb6a1-114">Pour un accès en lecture seule aux paramètres des documents approuvés, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="fb6a1-114">For read-only access to Safe Documents settings, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="fb6a1-115">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-115">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="fb6a1-116">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="fb6a1-116">**Notes**:</span></span>

  - <span data-ttu-id="fb6a1-117">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-117">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="fb6a1-118">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-118">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="fb6a1-119">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-119">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

### <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="fb6a1-120">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="fb6a1-120">How does Microsoft handle your data?</span></span>

<span data-ttu-id="fb6a1-121">Pour rester protégé, les documents fiables envoient des fichiers au Cloud [Microsoft Defender pour les points de terminaison](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-121">To keep you protected, Safe Documents sends files to the [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span> <span data-ttu-id="fb6a1-122">Vous trouverez ci-dessous des détails sur la façon dont Microsoft Defender pour les points de terminaison gère vos données : [Microsoft Defender pour le stockage et la confidentialité des données de point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-122">Details on how Microsoft Defender for Endpoint handles your data can be found here: [Microsoft Defender for Endpoint data storage and privacy](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span>

<span data-ttu-id="fb6a1-123">Les fichiers envoyés par des documents approuvés ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse (généralement, moins de 24 heures).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-123">Files sent by Safe Documents are not retained in Defender beyond the time needed for analysis (typically, less than 24 hours).</span></span>

## <a name="use-the-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="fb6a1-124">Utiliser le centre de sécurité & conformité pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="fb6a1-124">Use the Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="fb6a1-125">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**, puis cliquez sur **paramètres globaux**.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-125">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="fb6a1-126">Dans les **paramètres globaux** , effectuer un survol qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb6a1-126">In the **Global settings** fly out that appears, configure the following settings:</span></span>

   - <span data-ttu-id="fb6a1-127">**Activer les documents approuvés pour les clients Office**: déplacez le bouton bascule vers la droite pour activer la fonctionnalité : ![ activer/désactiver ](../../media/scc-toggle-on.png) .</span><span class="sxs-lookup"><span data-stu-id="fb6a1-127">**Turn on Safe Documents for Office clients**: Move the toggle to the right to turn on the feature: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

   - <span data-ttu-id="fb6a1-128">**Autoriser les utilisateurs à cliquer en mode protégé même si les documents approuvés identifient le fichier comme malveillant**: nous vous recommandons de laisser cette option désactivée (laissez le bouton bascule vers la gauche : ![ désactiver ](../../media/scc-toggle-off.png) ).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-128">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious**: We recommend that you leave this option turned off (leave the toggle to the left: ![Toggle off](../../media/scc-toggle-off.png)).</span></span>

   <span data-ttu-id="fb6a1-129">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-129">When you're finished, click **Save**.</span></span>

   ![Paramètres des documents approuvés après la sélection des paramètres globaux dans la page pièces jointes fiables.](../../media/safe-docs.png)

### <a name="use-exchange-online-powershell-to-configure-safe-documents"></a><span data-ttu-id="fb6a1-131">Utiliser Exchange Online PowerShell pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="fb6a1-131">Use Exchange Online PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="fb6a1-132">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fb6a1-132">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- <span data-ttu-id="fb6a1-133">Le paramètre _EnableSafeDocs_ active ou désactive les documents approuvés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-133">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>
- <span data-ttu-id="fb6a1-134">Le paramètre _AllowSafeDocsOpen_ autorise ou empêche les utilisateurs de quitter le mode protégé (c’est-à-dire, d’ouvrir le document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-134">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="fb6a1-135">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents identifiés comme étant malveillants en mode protégé.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-135">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="fb6a1-136">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="fb6a1-136">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="fb6a1-137">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="fb6a1-137">How do I know this worked?</span></span>

<span data-ttu-id="fb6a1-138">Pour vérifier que vous avez bien activé et configuré les documents approuvés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb6a1-138">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="fb6a1-139">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** \>  \> **pièces jointes** de niveau de sécurité ATP, cliquez sur **paramètres globaux**, puis vérifiez que l’autorisation documents **sûrs pour les clients Office** et **autoriser les utilisateurs à cliquer via le mode protégé même si les documents approuvés identifie le fichier comme des paramètres malveillants** .</span><span class="sxs-lookup"><span data-stu-id="fb6a1-139">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, click **Global settings**, and verify the **Turn on Safe Documents for Office clients** and **Allow people to click through Protected View even if Safe Documents identifies the file as malicious** settings.</span></span>

- <span data-ttu-id="fb6a1-140">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="fb6a1-140">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```

- <span data-ttu-id="fb6a1-141">Les fichiers suivants sont disponibles pour tester la protection des documents approuvés.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-141">The following files are available to test Safe Documents protection.</span></span> <span data-ttu-id="fb6a1-142">Ces documents sont similaires au fichier EICAR.TXT pour le test de solutions anti-programme malveillant et anti-virus.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-142">These documents are similar to the EICAR.TXT file for testing anti-malware and anti-virus solutions.</span></span> <span data-ttu-id="fb6a1-143">Les fichiers ne sont pas nocifs, mais ils déclenchent la protection des documents approuvés.</span><span class="sxs-lookup"><span data-stu-id="fb6a1-143">The files are not harmful, but they will trigger Safe Documents protection.</span></span>

  - [<span data-ttu-id="fb6a1-144">SafeDocsDemo.docx</span><span class="sxs-lookup"><span data-stu-id="fb6a1-144">SafeDocsDemo.docx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.docx)
  - [<span data-ttu-id="fb6a1-145">SafeDocsDemo.pptx</span><span class="sxs-lookup"><span data-stu-id="fb6a1-145">SafeDocsDemo.pptx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.pptx)
  - [<span data-ttu-id="fb6a1-146">SafeDocsDemo.xlsx</span><span class="sxs-lookup"><span data-stu-id="fb6a1-146">SafeDocsDemo.xlsx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.xlsx)
