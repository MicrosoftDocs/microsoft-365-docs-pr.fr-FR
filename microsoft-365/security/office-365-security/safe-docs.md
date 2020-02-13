---
title: Documents approuvés dans Office 365 DAV
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
ms.openlocfilehash: db73fc152a5a580a28bf6d8424ebc2a139cf3303
ms.sourcegitcommit: c2a36b16e354e20db5fd6275175ca856eae55bfc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2020
ms.locfileid: "41960346"
---
# <a name="safe-documents-in-office-365-advanced-threat-protection"></a><span data-ttu-id="ea44e-103">Documents approuvés dans Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ea44e-103">Safe Documents in Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="ea44e-104">Documents approuvés est une fonctionnalité d’Office 365 protection avancée contre les menaces qui utilise la [protection avancée contre les menaces de Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyser les documents et les fichiers ouverts en [mode protégé](https://support.office.com/article/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span><span class="sxs-lookup"><span data-stu-id="ea44e-104">Safe Documents is a feature in Office 365 Advanced Threat Protection (ATP) that uses [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.office.com/article/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="ea44e-105">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ea44e-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="ea44e-106">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="ea44e-106">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="ea44e-107">Pour vous connecter à Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="ea44e-107">To connect to Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="ea44e-108">Des autorisations doivent vous être attribuées avant de pouvoir effectuer les procédures de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ea44e-108">You need to be assigned permissions before you can perform the procedures in this topic.</span></span> <span data-ttu-id="ea44e-109">Pour activer et configurer des documents approuvés, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="ea44e-109">To enable and configure Safe Documents, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="ea44e-110">Pour plus d’informations sur les groupes de rôles dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="ea44e-110">For more information about role groups in the Security & Compliance Center, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-office-365-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="ea44e-111">Utiliser le centre de sécurité & conformité Office 365 pour configurer des documents approuvés</span><span class="sxs-lookup"><span data-stu-id="ea44e-111">Use the Office 365 Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="ea44e-112">Ouvrez le centre de sécurité & conformité Office 365 <https://protection.office.com>à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="ea44e-112">Open the Office 365 Security & Compliance Center at <https://protection.office.com>.</span></span>

2. <span data-ttu-id="ea44e-113">Accédez à la **stratégie** \> de **gestion** \> des menaces **pièces jointes sûres ATP**.</span><span class="sxs-lookup"><span data-stu-id="ea44e-113">Go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

3. <span data-ttu-id="ea44e-114">Dans la section **aider les utilisateurs à rester sûrs lors de l’approbation d’un fichier à ouvrir en dehors du mode protégé dans les applications Office** , configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea44e-114">In the **Help people stay safe when trusting a file to open outside Protected View in Office applications** section, configure either of the following settings:</span></span>

   - <span data-ttu-id="ea44e-115">**Activer les documents approuvés pour les clients Office (les fichiers seront également envoyés vers Microsoft Cloud pour les analyses en profondeur)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-115">**Turn on Safe Documents for Office clients (Files will also be sent to Microsoft Cloud for deep analyses)**</span></span>

   - <span data-ttu-id="ea44e-116">**Autoriser les utilisateurs à cliquer en mode protégé même si les documents approuvés identifient le fichier comme malveillant**: nous vous recommandons de ne pas activer cette option.</span><span class="sxs-lookup"><span data-stu-id="ea44e-116">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious**: We recommend that you don't enable this option.</span></span>

4. <span data-ttu-id="ea44e-117">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ea44e-117">When you're finished, click **Save**.</span></span>

![Page pièces jointes approuvées ATP](../media/safe-docs.png)

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-safe-documents"></a><span data-ttu-id="ea44e-119">Utiliser Exchange Online PowerShell ou Exchange Online Protection PowerShell pour configurer des documents fiables</span><span class="sxs-lookup"><span data-stu-id="ea44e-119">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="ea44e-120">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="ea44e-120">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true|$false> -AllowSafeDocsOpen <$true|$false>
```

- <span data-ttu-id="ea44e-121">Le paramètre _EnableSafeDocs_ active ou désactive les documents approuvés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ea44e-121">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>

- <span data-ttu-id="ea44e-122">Le paramètre _AllowSafeDocsOpen_ autorise ou empêche les utilisateurs de quitter le mode protégé (c’est-à-dire, d’ouvrir le document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="ea44e-122">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="ea44e-123">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents identifiés comme étant malveillants en mode protégé.</span><span class="sxs-lookup"><span data-stu-id="ea44e-123">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="ea44e-124">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="ea44e-124">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-atppolicyforo365).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="ea44e-125">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="ea44e-125">How do I know this worked?</span></span>

<span data-ttu-id="ea44e-126">Pour vérifier que vous avez bien activé et configuré les documents approuvés, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea44e-126">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="ea44e-127">Dans le centre de sécurité & conformité, accédez à la **stratégie** \> de **gestion** \> des menaces **pièces jointes**au niveau de sécurité ATP et vérifiez que les sélections dans la section **aider les utilisateurs à rester sécurisés lors de l’ouverture d’un fichier pour ouvrir en dehors de la section applications Office** .</span><span class="sxs-lookup"><span data-stu-id="ea44e-127">In the Security & Compliance Center go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and verify the selections in the **Help people stay safe when trusting a file to open outside Protected View in Office applications** section.</span></span>

- <span data-ttu-id="ea44e-128">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="ea44e-128">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```
