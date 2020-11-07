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
description: Découvrez Comment collecter des informations de diagnostic eDiscovery pour un cas de support Microsoft.
ms.openlocfilehash: 107309748e2f27b50be5f8e8fc76afcb693989f9
ms.sourcegitcommit: dab50e1cc5bba920720b80033c93457f5ca1c330
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2020
ms.locfileid: "48944391"
---
# <a name="collect-ediscovery-diagnostic-information"></a><span data-ttu-id="f03d6-103">Collecter des informations de diagnostic eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f03d6-103">Collect eDiscovery diagnostic information</span></span>

<span data-ttu-id="f03d6-104">Parfois, les ingénieurs du support Microsoft ont besoin d’informations spécifiques sur votre problème lorsque vous ouvrez une demande de support liée à Core eDiscovery ou Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f03d6-104">Occasionally Microsoft Support engineers require specific information about your issue when you open a support case related to Core eDiscovery or Advanced eDiscovery.</span></span> <span data-ttu-id="f03d6-105">Cet article fournit des conseils sur la façon de collecter des informations de diagnostic pour aider les ingénieurs à examiner et résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="f03d6-105">This article provides guidance on how to collect diagnostic information to help support engineers investigate and resolve issues.</span></span> <span data-ttu-id="f03d6-106">En règle générale, vous n’avez pas besoin de collecter ces informations jusqu’à ce qu’un ingénieur du support technique Microsoft vous demande de le faire.</span><span class="sxs-lookup"><span data-stu-id="f03d6-106">Typically, you don't need to collect this information until asked to do so by a Microsoft Support engineer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f03d6-107">La sortie des applets de commande et des informations de diagnostic décrites dans cet article peut inclure des informations sensibles sur les litiges ou les investigations internes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f03d6-107">The output from the cmdlets and diagnostic information described in this article may include sensitive information about litigation or internal investigations in your organization.</span></span> <span data-ttu-id="f03d6-108">Avant d’envoyer les informations de diagnostic brutes au support Microsoft, vous devez passer en revue les informations et biffer les informations sensibles (telles que les noms ou autres informations relatives aux parties au litige ou à l’enquête) en les remplaçant par `XXXXXXX` .</span><span class="sxs-lookup"><span data-stu-id="f03d6-108">Before sending the raw diagnostic information to Microsoft Support, you should review the information and redact any sensitive information (such as names or other information about parties to litigation or investigation) by replacing it with `XXXXXXX`.</span></span> <span data-ttu-id="f03d6-109">Cette méthode indique également à l’ingénieur du support Microsoft que des informations ont été rédigées.</span><span class="sxs-lookup"><span data-stu-id="f03d6-109">Using this method will also indicate to the Microsoft Support engineer that information was redacted.</span></span>

## <a name="collect-diagnostic-information-for-core-ediscovery"></a><span data-ttu-id="f03d6-110">Collecter les informations de diagnostic pour la découverte électronique principale</span><span class="sxs-lookup"><span data-stu-id="f03d6-110">Collect diagnostic information for Core eDiscovery</span></span>

<span data-ttu-id="f03d6-111">La collecte des informations de diagnostic pour la découverte électronique principale est basée sur les cmdlets, de sorte que vous devez utiliser la sécurité & PowerShell du centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="f03d6-111">Collecting diagnostic information for Core eDiscovery is cmdlet-based, so you'll have to use Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="f03d6-112">Les exemples PowerShell suivants exécuteront des cmdlets, puis enregistreront la sortie dans un fichier texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="f03d6-112">The following PowerShell examples will run cmdlets and then save the output to a specified text file.</span></span> <span data-ttu-id="f03d6-113">Dans la plupart des cas de prise en charge, vous devez uniquement exécuter l’une de ces commandes.</span><span class="sxs-lookup"><span data-stu-id="f03d6-113">In most support cases, you should only have to run one of these commands.</span></span>

<span data-ttu-id="f03d6-114">Pour exécuter les applets de commande suivantes, [Connectez-vous à la </span> sécurité & Centre de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="f03d6-114">To run the following cmdlets, [connect to Security & Compliance Center PowerShell</span>](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span> <span data-ttu-id="f03d6-115">Une fois que vous êtes connecté, exécutez une ou plusieurs des commandes suivantes et assurez-vous de remplacer les espaces réservés par les noms d’objet réels.</span><span class="sxs-lookup"><span data-stu-id="f03d6-115">After you're connected, run one or more of the following commands and be sure to replace placeholders with the actual object names.</span></span>

<span data-ttu-id="f03d6-116">Une fois que vous avez vérifié le fichier texte généré et redacting les informations sensibles, envoyez-le à l’ingénieur du support technique Microsoft en travaillant sur votre cas.</span><span class="sxs-lookup"><span data-stu-id="f03d6-116">After reviewing the generated text file and redacting sensitive information, send it to the Microsoft Support engineer working on your case.</span></span>

> [!NOTE]
> <span data-ttu-id="f03d6-117">Vous pouvez également exécuter les commandes de cette section pour collecter des informations de diagnostic pour les recherches et les exportations figurant sur la page **recherche de contenu** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f03d6-117">You can also run the commands in this section to collect diagnostic information for the searches and exports listed on the **Content search** page in the Microsoft 365 compliance center.</span></span>

### <a name="collect-information-about-searches"></a><span data-ttu-id="f03d6-118">Collecter des informations sur les recherches</span><span class="sxs-lookup"><span data-stu-id="f03d6-118">Collect information about searches</span></span>

<span data-ttu-id="f03d6-119">La commande suivante collecte des informations utiles lors de l’étude des problèmes liés à une recherche de contenu ou à une recherche associée à un cas de découverte électronique principale.</span><span class="sxs-lookup"><span data-stu-id="f03d6-119">The following command collects information that's helpful when investigating issues with a Content search or a search associated with a Core eDiscovery case.</span></span>

```powershell
Get-ComplianceSearch "<Search name>" | FL > "ComplianceSearch.txt"
```

### <a name="collect-information-about-search-actions"></a><span data-ttu-id="f03d6-120">Collecter des informations sur les actions de recherche</span><span class="sxs-lookup"><span data-stu-id="f03d6-120">Collect information about search actions</span></span>

<span data-ttu-id="f03d6-121">La commande suivante collecte des informations pour identifier les problèmes liés à l’aperçu, à l’exportation ou au vidage des résultats d’une recherche de contenu ou d’une recherche associée à un cas de découverte électronique principale.</span><span class="sxs-lookup"><span data-stu-id="f03d6-121">The following command collects information to investigate problems with previewing, exporting, or purging the results of a Content search or a search associated with a Core eDiscovery case.</span></span> <span data-ttu-id="f03d6-122">Vous pouvez identifier le nom de l’action de recherche en cliquant sur une exportation qui est indiquée sous l’onglet **exportations** . Pour identifier les noms des actions d’aperçu et de purge, vous pouvez exécuter la cmdlet **Get-ComplianceSearchAction** pour afficher la liste de toutes les actions.</span><span class="sxs-lookup"><span data-stu-id="f03d6-122">You can identify the name of the search action by clicking an export that's listed on the **Exports** tab. To identify the names of preview and purge actions, you can run the **Get-ComplianceSearchAction** cmdlet to display a list of all actions.</span></span> <span data-ttu-id="f03d6-123">Le format du nom de l’action de recherche est construit en ajoutant `_Preview` , `_Export` ou `_Purge` au nom de la recherche correspondante.</span><span class="sxs-lookup"><span data-stu-id="f03d6-123">The format for the search action name is constructed by appending `_Preview`, `_Export`, or `_Purge` to the name of the corresponding search.</span></span>

```powershell
Get-ComplianceSearchAction "<Search action name>" | FL > "ComplianceSearchAction.txt"
```

### <a name="collect-information-about-ediscovery-holds"></a><span data-ttu-id="f03d6-124">Collecte d’informations sur les conservations eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f03d6-124">Collect information about eDiscovery holds</span></span>

<span data-ttu-id="f03d6-125">Lorsqu’une conservation de découverte électronique associée à un cas de découverte électronique principale ne fonctionne pas comme prévu, exécutez la commande suivante pour collecter des informations sur la stratégie de blocage de la casse et la règle de blocage de la découverte électronique associée.</span><span class="sxs-lookup"><span data-stu-id="f03d6-125">When an eDiscovery hold associated with a Core eDiscovery case isn't functioning as expected, run the following command to collect information about the Case Hold Policy and associated Case Hold Rule for the eDiscovery hold.</span></span> <span data-ttu-id="f03d6-126">Le *nom* de la stratégie de conservation de la casse dans la commande suivante est le même que le nom du blocage eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f03d6-126">The *Case hold policy name* in the following command is the same as the name of the eDiscovery hold.</span></span> <span data-ttu-id="f03d6-127">Vous pouvez identifier ce nom dans les onglets de **suspensions** dans le cas de découverte électronique principale.</span><span class="sxs-lookup"><span data-stu-id="f03d6-127">You can identify this name on the **Holds** tabs in the Core eDiscovery case.</span></span>

```powershell
Get-CaseHoldPolicy "<Case hold policy name>" | %{"--CaseHoldPolicy--";$_|FL;"--CaseHoldRule--";Get-CaseHoldRule -Policy $_.Name | FL} > "eDiscoveryCaseHold.txt"
```

### <a name="collect-all-case-information"></a><span data-ttu-id="f03d6-128">Collecter toutes les informations de cas</span><span class="sxs-lookup"><span data-stu-id="f03d6-128">Collect all case information</span></span>

<span data-ttu-id="f03d6-129">Parfois, il n’est pas évident que les informations requises par le support Microsoft pour enquêter sur votre problème.</span><span class="sxs-lookup"><span data-stu-id="f03d6-129">Sometimes, it's not apparent what information is required by Microsoft Support to investigate your issue.</span></span> <span data-ttu-id="f03d6-130">Dans ce cas, vous pouvez collecter toutes les informations de diagnostic pour un cas de découverte électronique de base.</span><span class="sxs-lookup"><span data-stu-id="f03d6-130">In this situation, you can collect all of the diagnostics information for a Core eDiscovery case.</span></span> <span data-ttu-id="f03d6-131">Le *nom principal du cas eDiscovery* dans la commande suivante est identique au nom d’un cas qui est affiché sur la page **principale de découverte électronique** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f03d6-131">The *Core eDiscovery case name* in the following command is the same as the name of a case that's displayed on the **Core eDiscovery** page in the Microsoft 365 compliance center.</span></span>

```powershell
Get-ComplianceCase "<Core eDiscovery case name>"| %{"$($_.Name)";"`t==Searches==";Get-ComplianceSearch -Case $_.Name | FL;"`t==Search Actions==";Get-ComplianceSearchAction -Case $_.Name |FL;"`t==Holds==";Get-CaseHoldPolicy -Case $_.Name | %{$_|FL;"`t`t ==$($_.Name) Rules==";Get-CaseHoldRule -Policy $_.Name | FL}} > "eDiscoveryCase.txt"
```

## <a name="collect-diagnostic-information-for-advanced-ediscovery"></a><span data-ttu-id="f03d6-132">Collecter des informations de diagnostic pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f03d6-132">Collect diagnostic information for Advanced eDiscovery</span></span>

<span data-ttu-id="f03d6-133">L’onglet **paramètres** dans un cas avancé de découverte électronique vous permet de copier rapidement les informations de diagnostic pour le cas.</span><span class="sxs-lookup"><span data-stu-id="f03d6-133">The **Settings** tab in an Advanced eDiscovery case lets you quickly copy the diagnostic information for the case.</span></span> <span data-ttu-id="f03d6-134">Les informations de diagnostic sont enregistrées dans le presse-papiers afin que vous puissiez les coller dans un fichier texte et les envoyer au support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f03d6-134">The diagnostic information is saved to the clipboard so you can paste it to a text file and send to Microsoft Support.</span></span>

1. <span data-ttu-id="f03d6-135">Accédez à [https://compliance.microsoft.com](https://compliance.microsoft.com/) , puis cliquez sur **Afficher tous les > EDiscovery > Advanced**.</span><span class="sxs-lookup"><span data-stu-id="f03d6-135">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com/) and then click **Show all > eDiscovery > Advanced**.</span></span>

2. <span data-ttu-id="f03d6-136">Sélectionnez un cas, puis cliquez sur l’onglet **paramètres** .</span><span class="sxs-lookup"><span data-stu-id="f03d6-136">Select a case and then click the **Settings** tab.</span></span>

3. <span data-ttu-id="f03d6-137">Sous **informations** sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="f03d6-137">Under **Case Information** , click **Select**.</span></span>

4. <span data-ttu-id="f03d6-138">Sur la page de menu volant, cliquez sur **copier les informations de diagnostic** pour copier les informations dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="f03d6-138">On the flyout page, click **Copy diagnostic information** to copy the info to the clipboard.</span></span>

5. <span data-ttu-id="f03d6-139">Ouvrez un fichier texte (dans le bloc-notes), puis collez les informations dans le fichier texte.</span><span class="sxs-lookup"><span data-stu-id="f03d6-139">Open a text file (in Notepad) and then paste the information in the text file.</span></span>

6. <span data-ttu-id="f03d6-140">Enregistrez le fichier texte et nommez-le comme vous le souhaitez `AeD Diagnostic Info YYYY.MM.DD` (par exemple, `AeD Diagnostic Info 2020.11.03` ).</span><span class="sxs-lookup"><span data-stu-id="f03d6-140">Save the text file and name it something like `AeD Diagnostic Info YYYY.MM.DD` (for example, `AeD Diagnostic Info 2020.11.03`).</span></span>

<span data-ttu-id="f03d6-141">Une fois que vous avez consulté le fichier et redacting informations sensibles, envoyez-le à l’ingénieur du support technique Microsoft en travaillant sur votre cas.</span><span class="sxs-lookup"><span data-stu-id="f03d6-141">After reviewing the file and redacting sensitive information, send it to the Microsoft Support engineer working on your case.</span></span>
