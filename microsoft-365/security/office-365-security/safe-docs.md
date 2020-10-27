---
title: Documents sécurisés dans Office 365 – Protection avancée contre les menaces
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
ms.openlocfilehash: baa04f74388b702b42a0bdb83a7f0797ace09883
ms.sourcegitcommit: 45c0afcf958069c5c1b31f9b6c762d8dd806e1e9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48773948"
---
# <a name="safe-documents-in-microsoft-365-e5"></a><span data-ttu-id="564ba-103">Documents sécurisés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="564ba-103">Safe Documents in Microsoft 365 E5</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="564ba-104">Documents approuvés est une fonctionnalité de Microsoft 365 E5 ou Microsoft 365 E5 sécurité qui utilise la [protection avancée contre les menaces de Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyser des documents et des fichiers ouverts en [mode protégé](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span><span class="sxs-lookup"><span data-stu-id="564ba-104">Safe Documents is a feature in Microsoft 365 E5 or Microsoft 365 E5 Security that uses [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="564ba-105">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="564ba-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="564ba-106">Les documents approuvés sont disponibles uniquement pour les utilisateurs disposant de licences de sécurité Microsoft *365 E5* ou *Microsoft 365 E5* .</span><span class="sxs-lookup"><span data-stu-id="564ba-106">Safe Documents is available only to users with *Microsoft 365 E5* or *Microsoft 365 E5 Security* licenses.</span></span> <span data-ttu-id="564ba-107">Ces licences ne sont pas incluses dans les plans Office 365 Advanced Threat Protection (ATP).</span><span class="sxs-lookup"><span data-stu-id="564ba-107">These licenses are not included in Office 365 Advanced Threat Protection (ATP) plans.</span></span>

- <span data-ttu-id="564ba-108">Les documents approuvés sont pris en charge dans les applications Microsoft 365 pour entreprise (anciennement appelé Office 365 ProPlus) version 2004 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="564ba-108">Safe Documents is supported in Microsoft 365 Apps for enterprise (formerly known as Office 365 ProPlus) version 2004 or later.</span></span>

- <span data-ttu-id="564ba-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="564ba-109">You open the Security & Compliance Center at <https://protection.office.com>.</span></span> <span data-ttu-id="564ba-110">Pour accéder directement à la page **pièces jointes approuvées ATP** , ouvrez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="564ba-110">To go directly to the **ATP Safe Attachments** page, open <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="564ba-111">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="564ba-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="564ba-112">Des autorisations doivent vous être attribuées avant de pouvoir effectuer les procédures de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="564ba-112">You need to be assigned permissions before you can perform the procedures in this topic.</span></span> <span data-ttu-id="564ba-113">Pour activer et configurer des documents approuvés, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="564ba-113">To enable and configure Safe Documents, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="564ba-114">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="564ba-114">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="564ba-115">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="564ba-115">How does Microsoft handle your data?</span></span>

<span data-ttu-id="564ba-116">Pour rester protégé, les documents fiables envoient des fichiers au Cloud de [protection avancée contre les menaces Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="564ba-116">To keep you protected, Safe Documents sends files to the [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span> <span data-ttu-id="564ba-117">Vous trouverez ci-dessous des détails sur la façon dont Microsoft Defender ATP gère vos données : [stockage et confidentialité des données Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="564ba-117">Details on how Microsoft Defender ATP handles your data can be found here: [Microsoft Defender ATP data storage and privacy](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span>

<span data-ttu-id="564ba-118">Les fichiers envoyés par des documents approuvés ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse (généralement, moins de 24 heures).</span><span class="sxs-lookup"><span data-stu-id="564ba-118">Files sent by Safe Documents are not retained in Defender beyond the time needed for analysis (typically, less than 24 hours).</span></span>

## <a name="use-the-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="564ba-119">Utiliser le centre de sécurité & conformité pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="564ba-119">Use the Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="564ba-120">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \> **Policy** \> **pièces jointes ATP** , puis cliquez sur **paramètres globaux** .</span><span class="sxs-lookup"><span data-stu-id="564ba-120">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments** , and then click **Global settings** .</span></span>

2. <span data-ttu-id="564ba-121">Dans les **paramètres globaux** , effectuer un survol qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="564ba-121">In the **Global settings** fly out that appears, configure the following settings:</span></span>

   - <span data-ttu-id="564ba-122">**Activer les documents approuvés pour les clients Office** : déplacez le bouton bascule vers la droite pour activer la fonctionnalité : ![ activer/désactiver ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) .</span><span class="sxs-lookup"><span data-stu-id="564ba-122">**Turn on Safe Documents for Office clients** : Move the toggle to the right to turn on the feature: ![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png).</span></span>

   - <span data-ttu-id="564ba-123">**Autoriser les utilisateurs à cliquer en mode protégé même si les documents approuvés identifient le fichier comme malveillant** : nous vous recommandons de laisser cette option désactivée (laissez le bouton bascule vers la gauche : ![ désactiver ](../../media/scc-toggle-off.png) ).</span><span class="sxs-lookup"><span data-stu-id="564ba-123">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious** : We recommend that you leave this option turned off (leave the toggle to the left: ![Toggle off](../../media/scc-toggle-off.png)).</span></span>

   <span data-ttu-id="564ba-124">Lorsque vous avez terminé, cliquez sur **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="564ba-124">When you're finished, click **Save** .</span></span>

   ![Paramètres des documents approuvés après la sélection des paramètres globaux dans la page pièces jointes approuvées ATP.](../../media/safe-docs.png)

### <a name="use-exchange-online-powershell-to-configure-safe-documents"></a><span data-ttu-id="564ba-126">Utiliser Exchange Online PowerShell pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="564ba-126">Use Exchange Online PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="564ba-127">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="564ba-127">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- <span data-ttu-id="564ba-128">Le paramètre _EnableSafeDocs_ active ou désactive les documents approuvés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="564ba-128">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>
- <span data-ttu-id="564ba-129">Le paramètre _AllowSafeDocsOpen_ autorise ou empêche les utilisateurs de quitter le mode protégé (c’est-à-dire, d’ouvrir le document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="564ba-129">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="564ba-130">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents identifiés comme étant malveillants en mode protégé.</span><span class="sxs-lookup"><span data-stu-id="564ba-130">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="564ba-131">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="564ba-131">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="564ba-132">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="564ba-132">How do I know this worked?</span></span>

<span data-ttu-id="564ba-133">Pour vérifier que vous avez bien activé et configuré les documents approuvés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="564ba-133">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="564ba-134">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** \> **Policy** \> **pièces jointes** de niveau de sécurité ATP, cliquez sur **paramètres globaux** , puis vérifiez que l’autorisation documents **sûrs pour les clients Office** et **autoriser les utilisateurs à cliquer via le mode protégé même si les documents approuvés identifie le fichier comme des paramètres malveillants** .</span><span class="sxs-lookup"><span data-stu-id="564ba-134">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments** , click **Global settings** , and verify the **Turn on Safe Documents for Office clients** and **Allow people to click through Protected View even if Safe Documents identifies the file as malicious** settings.</span></span>

- <span data-ttu-id="564ba-135">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="564ba-135">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```

- <span data-ttu-id="564ba-136">Les fichiers suivants sont disponibles pour tester la protection des documents approuvés.</span><span class="sxs-lookup"><span data-stu-id="564ba-136">The following files are available to test Safe Documents protection.</span></span> <span data-ttu-id="564ba-137">Ces documents sont similaires au fichier EICAR.TXT pour le test de solutions anti-programme malveillant et anti-virus.</span><span class="sxs-lookup"><span data-stu-id="564ba-137">These documents are similar to the EICAR.TXT file for testing anti-malware and anti-virus solutions.</span></span> <span data-ttu-id="564ba-138">Les fichiers ne sont pas nocifs, mais ils déclenchent la protection des documents approuvés.</span><span class="sxs-lookup"><span data-stu-id="564ba-138">The files are not harmful, but they will trigger Safe Documents protection.</span></span>

  - [<span data-ttu-id="564ba-139">SafeDocsDemo.docx</span><span class="sxs-lookup"><span data-stu-id="564ba-139">SafeDocsDemo.docx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.docx)
  - [<span data-ttu-id="564ba-140">SafeDocsDemo.pptx</span><span class="sxs-lookup"><span data-stu-id="564ba-140">SafeDocsDemo.pptx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.pptx)
  - [<span data-ttu-id="564ba-141">SafeDocsDemo.xlsx</span><span class="sxs-lookup"><span data-stu-id="564ba-141">SafeDocsDemo.xlsx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.xlsx)
