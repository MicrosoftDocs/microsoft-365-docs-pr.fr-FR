---
title: Documents sécurisés dans Office 365 PACM
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: kshi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez les documents sûrs dans Office 365 dav.
ms.openlocfilehash: e9b1fadd3e9e6dab337a0c3ded380c5c49f53bab
ms.sourcegitcommit: 584e2e9db8c541fe32624acdca5e12ee327fdb63
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2020
ms.locfileid: "44678669"
---
# <a name="safe-documents-in-office-365-advanced-threat-protection"></a><span data-ttu-id="df013-103">Documents fiables dans Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="df013-103">Safe Documents in Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="df013-104">La fonctionnalité documents approuvés est une fonctionnalité d’Office 365 protection avancée contre les menaces (Office 365 ATP) qui utilise la [protection avancée contre les menaces de Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyser les documents et les fichiers ouverts en [mode protégé](https://support.office.com/article/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span><span class="sxs-lookup"><span data-stu-id="df013-104">Safe Documents is a feature in Office 365 Advanced Threat Protection (Office 365 ATP) that uses [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.office.com/article/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="df013-105">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="df013-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="df013-106">Cette fonctionnalité est disponible uniquement pour les utilisateurs disposant de la licence de sécurité Microsoft 365 E5 ou Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="df013-106">This feature is only available to users with the Microsoft 365 E5 or Microsoft 365 E5 Security license.</span></span>

- <span data-ttu-id="df013-107">Les documents approuvés sont actuellement disponibles pour la préversion publique, disponibles pour les utilisateurs qui font partie du [programme Office Insider](https://insider.office.com/en-us/join) sur le canal actuel (aperçu) avec Office version 2002 (12527,20092) ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="df013-107">Safe Documents is currently available for public preview, available to users that are part of the [Office Insider Program](https://insider.office.com/en-us/join) on Current Channel (Preview) with Office Version 2002 (12527.20092) or greater.</span></span> <span data-ttu-id="df013-108">Cette fonctionnalité est désactivée par défaut et doit être activée par l’administrateur de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="df013-108">This feature is off by default and will need to be enabled by the Security Administrator.</span></span>

- <span data-ttu-id="df013-109">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="df013-109">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="df013-110">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="df013-110">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="df013-111">Des autorisations doivent vous être attribuées avant de pouvoir effectuer les procédures de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="df013-111">You need to be assigned permissions before you can perform the procedures in this topic.</span></span> <span data-ttu-id="df013-112">Pour activer et configurer des documents approuvés, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="df013-112">To enable and configure Safe Documents, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="df013-113">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="df013-113">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="df013-114">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="df013-114">How does Microsoft handle your data?</span></span>

<span data-ttu-id="df013-115">Pour rester protégé, les documents fiables envoient des fichiers au Cloud de [protection avancée contre les menaces Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="df013-115">To keep you protected, Safe Documents sends files to the [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span>

- <span data-ttu-id="df013-116">Vous trouverez [ici](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy) des informations détaillées sur la façon dont Microsoft Defender Advanced thread protection gère vos données.</span><span class="sxs-lookup"><span data-stu-id="df013-116">Details on how Microsoft Defender Advanced Thread Protection handles your data can be found [here](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span></span>
- <span data-ttu-id="df013-117">Outre les instructions ci-dessus, les fichiers envoyés par des documents approuvés ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse, ce qui correspond généralement à moins de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="df013-117">In addition to the guidelines above, files sent by Safe Documents are not retained in Defender beyond the time needed for analysis, which is typically less than 24 hours</span></span>

## <a name="use-the-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="df013-118">Utiliser le centre de sécurité & conformité pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="df013-118">Use the Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="df013-119">Ouvrez le centre de sécurité & conformité à l’adresse <https://protection.office.com> .</span><span class="sxs-lookup"><span data-stu-id="df013-119">Open the Security & Compliance Center at <https://protection.office.com>.</span></span>

2. <span data-ttu-id="df013-120">Accédez à la stratégie de **gestion des menaces** \> **Policy** \> **pièces jointes sûres ATP**.</span><span class="sxs-lookup"><span data-stu-id="df013-120">Go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

3. <span data-ttu-id="df013-121">Dans la section **aider les utilisateurs à rester sûrs lors de l’approbation d’un fichier à ouvrir en dehors du mode protégé dans les applications Office** , configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="df013-121">In the **Help people stay safe when trusting a file to open outside Protected View in Office applications** section, configure either of the following settings:</span></span>

   - <span data-ttu-id="df013-122">**Activer les documents approuvés pour les clients Office (les fichiers seront également envoyés vers Microsoft Cloud pour les analyses en profondeur)**</span><span class="sxs-lookup"><span data-stu-id="df013-122">**Turn on Safe Documents for Office clients (Files will also be sent to Microsoft Cloud for deep analyses)**</span></span>

   - <span data-ttu-id="df013-123">**Autoriser les utilisateurs à cliquer en mode protégé même si les documents approuvés identifient le fichier comme malveillant**: nous vous recommandons de ne pas activer cette option.</span><span class="sxs-lookup"><span data-stu-id="df013-123">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious**: We recommend that you don't enable this option.</span></span>

4. <span data-ttu-id="df013-124">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="df013-124">When you're finished, click **Save**.</span></span>

![Page pièces jointes approuvées ATP](../../media/safe-docs.png)

### <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-documents"></a><span data-ttu-id="df013-126">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer des documents fiables</span><span class="sxs-lookup"><span data-stu-id="df013-126">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="df013-127">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="df013-127">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true|$false> -AllowSafeDocsOpen <$true|$false>
```

- <span data-ttu-id="df013-128">Le paramètre _EnableSafeDocs_ active ou désactive les documents approuvés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="df013-128">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>

- <span data-ttu-id="df013-129">Le paramètre _AllowSafeDocsOpen_ autorise ou empêche les utilisateurs de quitter le mode protégé (c’est-à-dire, d’ouvrir le document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="df013-129">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="df013-130">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents identifiés comme étant malveillants en mode protégé.</span><span class="sxs-lookup"><span data-stu-id="df013-130">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="df013-131">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="df013-131">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="df013-132">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="df013-132">How do I know this worked?</span></span>

<span data-ttu-id="df013-133">Pour vérifier que vous avez bien activé et configuré les documents approuvés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="df013-133">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="df013-134">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** \> **Policy** \> **pièces jointes**au niveau de sécurité ATP et vérifiez que les sélections dans la section **aider les utilisateurs à rester sécurisés lors de l’ouverture d’un fichier pour ouvrir en dehors de la section applications Office** .</span><span class="sxs-lookup"><span data-stu-id="df013-134">In the Security & Compliance Center go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and verify the selections in the **Help people stay safe when trusting a file to open outside Protected View in Office applications** section.</span></span>

- <span data-ttu-id="df013-135">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="df013-135">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```
