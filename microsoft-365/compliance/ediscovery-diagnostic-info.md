---
title: Collecter des informations de diagnostic eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment collecter des informations de diagnostic eDiscovery pour un cas de support Microsoft.
ms.openlocfilehash: 842f8baf770f178df3298bbfa911de26ce946ed0
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926554"
---
# <a name="collect-ediscovery-diagnostic-information"></a><span data-ttu-id="3874d-103">Collecter des informations de diagnostic eDiscovery</span><span class="sxs-lookup"><span data-stu-id="3874d-103">Collect eDiscovery diagnostic information</span></span>

<span data-ttu-id="3874d-104">Parfois, les ingénieurs du support Microsoft ont besoin d’informations spécifiques sur votre problème lorsque vous ouvrez un cas de support lié à Core eDiscovery ou Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3874d-104">Occasionally Microsoft Support engineers require specific information about your issue when you open a support case related to Core eDiscovery or Advanced eDiscovery.</span></span> <span data-ttu-id="3874d-105">Cet article fournit des instructions sur la collecte d’informations de diagnostic pour aider les ingénieurs du support technique à examiner et à résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="3874d-105">This article provides guidance on how to collect diagnostic information to help support engineers investigate and resolve issues.</span></span> <span data-ttu-id="3874d-106">En règle générale, vous n’avez pas besoin de collecter ces informations tant qu’un ingénieur du Support Microsoft ne vous y a pas demandé.</span><span class="sxs-lookup"><span data-stu-id="3874d-106">Typically, you don't need to collect this information until asked to do so by a Microsoft Support engineer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3874d-107">Les résultats des cmdlets et des informations de diagnostic décrites dans cet article peuvent inclure des informations sensibles sur les litiges ou les enquêtes internes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3874d-107">The output from the cmdlets and diagnostic information described in this article may include sensitive information about litigation or internal investigations in your organization.</span></span> <span data-ttu-id="3874d-108">Avant d’envoyer les informations de diagnostic brutes au Support Microsoft, vous devez passer en revue ces informations et les rendre confidentielles (telles que des noms ou d’autres informations sur les parties à des litiges ou à des enquêtes) en les remplaçant par `XXXXXXX` .</span><span class="sxs-lookup"><span data-stu-id="3874d-108">Before sending the raw diagnostic information to Microsoft Support, you should review the information and redact any sensitive information (such as names or other information about parties to litigation or investigation) by replacing it with `XXXXXXX`.</span></span> <span data-ttu-id="3874d-109">L’utilisation de cette méthode indique également à l’ingénieur du support Microsoft que les informations ont été expurgées.</span><span class="sxs-lookup"><span data-stu-id="3874d-109">Using this method will also indicate to the Microsoft Support engineer that information was redacted.</span></span>

## <a name="collect-diagnostic-information-for-core-ediscovery"></a><span data-ttu-id="3874d-110">Collecter des informations de diagnostic pour core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="3874d-110">Collect diagnostic information for Core eDiscovery</span></span>

<span data-ttu-id="3874d-111">La collecte d’informations de diagnostic pour core eDiscovery est basée sur les cmdlet. Vous devez donc utiliser le Centre de sécurité & conformité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3874d-111">Collecting diagnostic information for Core eDiscovery is cmdlet-based, so you'll have to use Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="3874d-112">Les exemples PowerShell suivants exécutent des cmdlets, puis enregistrent la sortie dans un fichier texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="3874d-112">The following PowerShell examples will run cmdlets and then save the output to a specified text file.</span></span> <span data-ttu-id="3874d-113">Dans la plupart des cas de prise en charge, vous ne devez exécuter qu’une de ces commandes.</span><span class="sxs-lookup"><span data-stu-id="3874d-113">In most support cases, you should only have to run one of these commands.</span></span>

<span data-ttu-id="3874d-114">Pour exécuter les cmdlets suivantes, [connectez-vous </span> au Centre de sécurité & conformité PowerShell](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="3874d-114">To run the following cmdlets, [connect to Security & Compliance Center PowerShell</span>](/powershell/exchange/connect-to-scc-powershell).</span></span> <span data-ttu-id="3874d-115">Une fois connecté, exécutez une ou plusieurs des commandes suivantes et assurez-vous de remplacer les espaces réservé par les noms d’objets réels.</span><span class="sxs-lookup"><span data-stu-id="3874d-115">After you're connected, run one or more of the following commands and be sure to replace placeholders with the actual object names.</span></span>

<span data-ttu-id="3874d-116">Après avoir passé en revue le fichier texte généré et publié des informations sensibles, envoyez-le à l’ingénieur du support Microsoft qui travaille sur votre cas.</span><span class="sxs-lookup"><span data-stu-id="3874d-116">After reviewing the generated text file and redacting sensitive information, send it to the Microsoft Support engineer working on your case.</span></span>

> [!NOTE]
> <span data-ttu-id="3874d-117">Vous pouvez également exécuter les commandes de cette section pour collecter des informations de diagnostic pour les recherches et les exportations répertoriées sur la **page** de recherche de contenu dans le centre de conformité Microsoft 365 de recherche.</span><span class="sxs-lookup"><span data-stu-id="3874d-117">You can also run the commands in this section to collect diagnostic information for the searches and exports listed on the **Content search** page in the Microsoft 365 compliance center.</span></span>

### <a name="collect-information-about-searches"></a><span data-ttu-id="3874d-118">Collecter des informations sur les recherches</span><span class="sxs-lookup"><span data-stu-id="3874d-118">Collect information about searches</span></span>

<span data-ttu-id="3874d-119">La commande suivante collecte des informations utiles lors de l’étude de problèmes liés à une recherche de contenu ou à une recherche associée à un cas core eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3874d-119">The following command collects information that's helpful when investigating issues with a Content search or a search associated with a Core eDiscovery case.</span></span>

```powershell
Get-ComplianceSearch "<Search name>" | FL > "ComplianceSearch.txt"
```

### <a name="collect-information-about-search-actions"></a><span data-ttu-id="3874d-120">Collecter des informations sur les actions de recherche</span><span class="sxs-lookup"><span data-stu-id="3874d-120">Collect information about search actions</span></span>

<span data-ttu-id="3874d-121">La commande suivante collecte des informations pour examiner les problèmes liés à l’aperçu, l’exportation ou la purge des résultats d’une recherche de contenu ou d’une recherche associée à un cas core eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3874d-121">The following command collects information to investigate problems with previewing, exporting, or purging the results of a Content search or a search associated with a Core eDiscovery case.</span></span> <span data-ttu-id="3874d-122">Vous pouvez identifier le nom de l’action de recherche en cliquant sur une exportation répertoriée sous **l’onglet Exportation.** Pour identifier les noms des actions d’aperçu et de purge, vous pouvez exécuter la cmdlet **Get-ComplianceSearchAction** pour afficher la liste de toutes les actions.</span><span class="sxs-lookup"><span data-stu-id="3874d-122">You can identify the name of the search action by clicking an export that's listed on the **Exports** tab. To identify the names of preview and purge actions, you can run the **Get-ComplianceSearchAction** cmdlet to display a list of all actions.</span></span> <span data-ttu-id="3874d-123">Le format du nom de l’action de recherche est construit en attente, ou au nom `_Preview` `_Export` de la recherche `_Purge` correspondante.</span><span class="sxs-lookup"><span data-stu-id="3874d-123">The format for the search action name is constructed by appending `_Preview`, `_Export`, or `_Purge` to the name of the corresponding search.</span></span>

```powershell
Get-ComplianceSearchAction "<Search action name>" | FL > "ComplianceSearchAction.txt"
```

### <a name="collect-information-about-ediscovery-holds"></a><span data-ttu-id="3874d-124">Collecter des informations sur les holds eDiscovery</span><span class="sxs-lookup"><span data-stu-id="3874d-124">Collect information about eDiscovery holds</span></span>

<span data-ttu-id="3874d-125">Lorsqu’une attente eDiscovery associée à un cas eDiscovery principal ne fonctionne pas comme prévu, exécutez la commande suivante pour collecter des informations sur la stratégie de cas de attente et la règle de cas associée pour la attente eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3874d-125">When an eDiscovery hold associated with a Core eDiscovery case isn't functioning as expected, run the following command to collect information about the Case Hold Policy and associated Case Hold Rule for the eDiscovery hold.</span></span> <span data-ttu-id="3874d-126">Le *nom de la stratégie de prise* en main dans la commande suivante est identique au nom de la découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="3874d-126">The *Case hold policy name* in the following command is the same as the name of the eDiscovery hold.</span></span> <span data-ttu-id="3874d-127">Vous pouvez identifier ce nom sous les **onglets Holds** dans le cas core eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3874d-127">You can identify this name on the **Holds** tabs in the Core eDiscovery case.</span></span>

```powershell
Get-CaseHoldPolicy "<Case hold policy name>" | %{"--CaseHoldPolicy--";$_|FL;"--CaseHoldRule--";Get-CaseHoldRule -Policy $_.Name | FL} > "eDiscoveryCaseHold.txt"
```

### <a name="collect-all-case-information"></a><span data-ttu-id="3874d-128">Collecter toutes les informations de cas</span><span class="sxs-lookup"><span data-stu-id="3874d-128">Collect all case information</span></span>

<span data-ttu-id="3874d-129">Parfois, il n’est pas évident de savoir quelles informations sont requises par le Support Microsoft pour examiner votre problème.</span><span class="sxs-lookup"><span data-stu-id="3874d-129">Sometimes, it's not apparent what information is required by Microsoft Support to investigate your issue.</span></span> <span data-ttu-id="3874d-130">Dans ce cas, vous pouvez collecter toutes les informations de diagnostic pour un cas core eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3874d-130">In this situation, you can collect all of the diagnostics information for a Core eDiscovery case.</span></span> <span data-ttu-id="3874d-131">Le nom du cas core *eDiscovery* dans la commande suivante est identique au nom d’un cas qui s’affiche sur la page Core **eDiscovery** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3874d-131">The *Core eDiscovery case name* in the following command is the same as the name of a case that's displayed on the **Core eDiscovery** page in the Microsoft 365 compliance center.</span></span>

```powershell
Get-ComplianceCase "<Core eDiscovery case name>"| %{"$($_.Name)";"`t==Searches==";Get-ComplianceSearch -Case $_.Name | FL;"`t==Search Actions==";Get-ComplianceSearchAction -Case $_.Name |FL;"`t==Holds==";Get-CaseHoldPolicy -Case $_.Name | %{$_|FL;"`t`t ==$($_.Name) Rules==";Get-CaseHoldRule -Policy $_.Name | FL}} > "eDiscoveryCase.txt"
```

## <a name="collect-diagnostic-information-for-advanced-ediscovery"></a><span data-ttu-id="3874d-132">Collecter des informations de diagnostic pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="3874d-132">Collect diagnostic information for Advanced eDiscovery</span></span>

<span data-ttu-id="3874d-133">**L Paramètres** onglet dans un Advanced eDiscovery vous permet de copier rapidement les informations de diagnostic pour le cas.</span><span class="sxs-lookup"><span data-stu-id="3874d-133">The **Settings** tab in an Advanced eDiscovery case lets you quickly copy the diagnostic information for the case.</span></span> <span data-ttu-id="3874d-134">Les informations de diagnostic sont enregistrées dans le Presse-papiers afin que vous pouvez les coller dans un fichier texte et les envoyer au Support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3874d-134">The diagnostic information is saved to the clipboard so you can paste it to a text file and send to Microsoft Support.</span></span>

1. <span data-ttu-id="3874d-135">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com/) and then click Show all > **eDiscovery > Advanced**.</span><span class="sxs-lookup"><span data-stu-id="3874d-135">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com/) and then click **Show all > eDiscovery > Advanced**.</span></span>

2. <span data-ttu-id="3874d-136">Sélectionnez un cas, puis cliquez sur **l’Paramètres’onglet.**</span><span class="sxs-lookup"><span data-stu-id="3874d-136">Select a case and then click the **Settings** tab.</span></span>

3. <span data-ttu-id="3874d-137">Sous **Informations de cas,** cliquez sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="3874d-137">Under **Case Information**, click **Select**.</span></span>

4. <span data-ttu-id="3874d-138">Dans la page volante, cliquez sur **Copier les informations de diagnostic** pour copier les informations dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="3874d-138">On the flyout page, click **Copy diagnostic information** to copy the info to the clipboard.</span></span>

5. <span data-ttu-id="3874d-139">Ouvrez un fichier texte (Bloc-notes), puis collez les informations dans le fichier texte.</span><span class="sxs-lookup"><span data-stu-id="3874d-139">Open a text file (in Notepad) and then paste the information in the text file.</span></span>

6. <span data-ttu-id="3874d-140">Enregistrez le fichier texte et nommez-le comme vous le `AeD Diagnostic Info YYYY.MM.DD` souhaitez (par exemple, `AeD Diagnostic Info 2020.11.03` ).</span><span class="sxs-lookup"><span data-stu-id="3874d-140">Save the text file and name it something like `AeD Diagnostic Info YYYY.MM.DD` (for example, `AeD Diagnostic Info 2020.11.03`).</span></span>

<span data-ttu-id="3874d-141">Après avoir passé en revue le fichier et envoyé des informations sensibles, envoyez-le à l’ingénieur du support Microsoft qui travaille sur votre cas.</span><span class="sxs-lookup"><span data-stu-id="3874d-141">After reviewing the file and redacting sensitive information, send it to the Microsoft Support engineer working on your case.</span></span>