---
title: Documents sécurisés dans Office 365 PACM
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
ms.openlocfilehash: 8918c7da26a60c7cfd64b7148d0added82cc6642
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47949453"
---
# <a name="safe-documents-in-microsoft-365-e5"></a><span data-ttu-id="68c54-103">Documents approuvés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="68c54-103">Safe Documents in Microsoft 365 E5</span></span>

<span data-ttu-id="68c54-104">Documents approuvés est une fonctionnalité de Microsoft 365 E5 ou Microsoft 365 E5 sécurité qui utilise la [protection avancée contre les menaces de Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyser des documents et des fichiers ouverts en [mode protégé](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span><span class="sxs-lookup"><span data-stu-id="68c54-104">Safe Documents is a feature in Microsoft 365 E5 or Microsoft 365 E5 Security that uses [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="68c54-105">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="68c54-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="68c54-106">Les documents approuvés sont désormais généralement disponibles pour les utilisateurs de la version 2004 de Office (12730. x) ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68c54-106">Safe Documents is now generally available to users with Office Version 2004 (12730.x) or greater!</span></span> <span data-ttu-id="68c54-107">Cette fonctionnalité est désactivée par défaut et doit être activée par l’administrateur de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="68c54-107">This feature is off by default and will need to be enabled by the Security Administrator.</span></span>

- <span data-ttu-id="68c54-108">Cette fonctionnalité est disponible uniquement pour les utilisateurs disposant de la licence de sécurité *microsoft 365 E5* ou *Microsoft 365 E5* (non incluse dans les plans Office 365 ATP).</span><span class="sxs-lookup"><span data-stu-id="68c54-108">This feature is only available to users with the *Microsoft 365 E5* or *Microsoft 365 E5 Security* license (not included in Office 365 ATP plans).</span></span>

- <span data-ttu-id="68c54-109">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="68c54-109">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="68c54-110">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="68c54-110">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="68c54-111">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="68c54-111">For more information about</span></span> 

- <span data-ttu-id="68c54-112">Des autorisations doivent vous être attribuées avant de pouvoir effectuer les procédures de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="68c54-112">You need to be assigned permissions before you can perform the procedures in this topic.</span></span> <span data-ttu-id="68c54-113">Pour activer et configurer des documents approuvés, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="68c54-113">To enable and configure Safe Documents, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="68c54-114">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="68c54-114">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="68c54-115">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="68c54-115">How does Microsoft handle your data?</span></span>

<span data-ttu-id="68c54-116">Pour rester protégé, les documents fiables envoient des fichiers au Cloud de [protection avancée contre les menaces Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="68c54-116">To keep you protected, Safe Documents sends files to the [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span>

- <span data-ttu-id="68c54-117">Vous trouverez [ici](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)des informations détaillées sur la façon dont Microsoft Defender Advanced Threat Protection gère vos données.</span><span class="sxs-lookup"><span data-stu-id="68c54-117">Details on how Microsoft Defender Advanced Threat Protection handles your data can be found [here](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span>
- <span data-ttu-id="68c54-118">Outre les instructions ci-dessus, les fichiers envoyés par des documents approuvés ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse, qui est généralement inférieur à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="68c54-118">In addition to the guidelines above, files sent by Safe Documents are not retained in Defender beyond the time needed for analysis, which is typically less than 24 hours.</span></span>

## <a name="use-the-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="68c54-119">Utiliser le centre de sécurité & conformité pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="68c54-119">Use the Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="68c54-120">Ouvrez le centre de sécurité & conformité à l’adresse <https://protection.office.com> .</span><span class="sxs-lookup"><span data-stu-id="68c54-120">Open the Security & Compliance Center at <https://protection.office.com>.</span></span>

2. <span data-ttu-id="68c54-121">Accédez à la stratégie de **gestion des menaces** \> **Policy** \> **pièces jointes sûres ATP**.</span><span class="sxs-lookup"><span data-stu-id="68c54-121">Go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

3. <span data-ttu-id="68c54-122">Dans la section **aider les utilisateurs à rester sûrs lors de l’approbation d’un fichier à ouvrir en dehors du mode protégé dans les applications Office** , configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="68c54-122">In the **Help people stay safe when trusting a file to open outside Protected View in Office applications** section, configure either of the following settings:</span></span>

   - <span data-ttu-id="68c54-123">**Activer des documents approuvés pour les clients Office**</span><span class="sxs-lookup"><span data-stu-id="68c54-123">**Turn on Safe Documents for Office clients**</span></span>

   - <span data-ttu-id="68c54-124">**Autoriser les utilisateurs à cliquer en mode protégé même si les documents approuvés identifient le fichier comme malveillant**: nous vous recommandons de ne pas activer cette option.</span><span class="sxs-lookup"><span data-stu-id="68c54-124">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious**: We recommend that you don't enable this option.</span></span>

4. <span data-ttu-id="68c54-125">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="68c54-125">When you're finished, click **Save**.</span></span>

![Page pièces jointes approuvées ATP](../../media/safe-docs.png)

### <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-documents"></a><span data-ttu-id="68c54-127">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer des documents fiables</span><span class="sxs-lookup"><span data-stu-id="68c54-127">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="68c54-128">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="68c54-128">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- <span data-ttu-id="68c54-129">Le paramètre _EnableSafeDocs_ active ou désactive les documents approuvés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="68c54-129">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>

- <span data-ttu-id="68c54-130">Le paramètre _AllowSafeDocsOpen_ autorise ou empêche les utilisateurs de quitter le mode protégé (c’est-à-dire, d’ouvrir le document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="68c54-130">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="68c54-131">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents identifiés comme étant malveillants en mode protégé.</span><span class="sxs-lookup"><span data-stu-id="68c54-131">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="68c54-132">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="68c54-132">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="68c54-133">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="68c54-133">How do I know this worked?</span></span>

<span data-ttu-id="68c54-134">Pour vérifier que vous avez bien activé et configuré les documents approuvés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="68c54-134">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="68c54-135">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** \> **Policy** \> **pièces jointes**au niveau de sécurité ATP et vérifiez que les sélections dans la section **aider les utilisateurs à rester sécurisés lors de l’ouverture d’un fichier pour ouvrir en dehors de la section applications Office** .</span><span class="sxs-lookup"><span data-stu-id="68c54-135">In the Security & Compliance Center go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and verify the selections in the **Help people stay safe when trusting a file to open outside Protected View in Office applications** section.</span></span>

- <span data-ttu-id="68c54-136">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="68c54-136">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```
