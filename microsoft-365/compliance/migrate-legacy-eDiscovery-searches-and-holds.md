---
title: Migrer les recherches et les données de découverte électronique héritées vers le Centre de conformité Microsoft 365
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: ef5562aa6f5c7519d19452100b55dd4bc30d4126
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926322"
---
# <a name="migrate-legacy-ediscovery-searches-and-holds-to-the-microsoft-365-compliance-center"></a><span data-ttu-id="17603-102">Migrer les recherches et les données de découverte électronique héritées vers le Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="17603-102">Migrate legacy eDiscovery searches and holds to the Microsoft 365 compliance center</span></span>

<span data-ttu-id="17603-103">Le Centre de conformité Microsoft 365 offre une expérience améliorée pour l’utilisation d’eDiscovery, notamment : une fiabilité supérieure, de meilleures performances et de nombreuses fonctionnalités adaptées aux flux de travail eDiscovery, y compris les cas pour organiser votre contenu en fonction de la matière, les ensembles de révision pour examiner le contenu et l’analyse afin d’aider à annuler les données pour révision telles que le regroupement quasi-dupliqué, le thread de messagerie électronique, l’analyse des thèmes et le codage prédictif.</span><span class="sxs-lookup"><span data-stu-id="17603-103">The Microsoft 365 compliance center provides an improved experience for eDiscovery usage, including: higher reliability, better performance and many features tailored to eDiscovery workflows including cases to organize your content by matter, review sets to review content and analytics to help cull data for review such as near-duplicate grouping, email threading, themes analysis, and predictive coding.</span></span>

<span data-ttu-id="17603-104">Pour aider les clients à tirer parti des fonctionnalités nouvelles et améliorées, cet article fournit des instructions de base sur la migration des recherches et des données de découverte électronique In-Place du Centre d’administration Exchange vers le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="17603-104">To help customers take advantage of the new and improved functionality, this article provides basic guidance on how to migrate In-Place eDiscovery searches and holds from the Exchange admin center to the Microsoft 365 compliance center.</span></span>

> [!NOTE]
> <span data-ttu-id="17603-105">Étant donné qu’il existe de nombreux scénarios différents, cet article fournit des instructions générales pour la transition des recherches et des recherches en cas de découverte électronique principale dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="17603-105">Because there are many different scenarios, this article provides general guidance to transition searches and holds to a core eDiscovery case in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="17603-106">L’utilisation de cas eDiscovery n’est pas toujours requise, mais elles ajoutent une couche supplémentaire de sécurité en vous permettant d’attribuer des autorisations pour contrôler qui a accès aux cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="17603-106">Using eDiscovery cases aren't always required, but they add an extra layer of security by letting you assign permissions to control who has access to the eDiscovery cases in your organization.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="17603-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="17603-107">Before you begin</span></span>

- <span data-ttu-id="17603-108">Vous devez être membre du groupe de rôles Gestionnaire eDiscovery dans le Centre de sécurité & conformité pour exécuter les commandes PowerShell décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="17603-108">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center to run the PowerShell commands described in this article.</span></span> <span data-ttu-id="17603-109">Vous devez également être membre du groupe de rôles Gestion de la découverte dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="17603-109">You also have to be a member of the Discovery Management role group in the Exchange admin center.</span></span>

- <span data-ttu-id="17603-110">Cet article fournit des instructions sur la création d’une attente eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="17603-110">This article provides guidance on how to create an eDiscovery hold.</span></span> <span data-ttu-id="17603-111">La stratégie de attente sera appliquée aux boîtes aux lettres par le biais d’un processus asynchrone.</span><span class="sxs-lookup"><span data-stu-id="17603-111">The hold policy will be applied to mailboxes through an asynchronous process.</span></span> <span data-ttu-id="17603-112">Lors de la création d’une mise en attente eDiscovery, vous devez créer une case CaseHoldPolicy et CaseHoldRule, sinon la mise en attente ne sera pas créée et les emplacements de contenu ne seront pas placés en attente.</span><span class="sxs-lookup"><span data-stu-id="17603-112">When creating an eDiscovery hold, you must create both a CaseHoldPolicy and CaseHoldRule, otherwise the hold will not be created and content locations will not be placed on hold.</span></span>

## <a name="step-1-connect-to-exchange-online-powershell-and-security--compliance-center-powershell"></a><span data-ttu-id="17603-113">Étape 1 : Se connecter à Exchange Online PowerShell et au Centre de sécurité & conformité PowerShell</span><span class="sxs-lookup"><span data-stu-id="17603-113">Step 1: Connect to Exchange Online PowerShell and Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="17603-114">La première étape consiste à se connecter à Exchange Online PowerShell et au Centre de sécurité & conformité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="17603-114">The first step is to connect to Exchange Online PowerShell and Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="17603-115">Vous pouvez copier le script suivant, le coller dans une fenêtre PowerShell, puis l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="17603-115">You can copy the following script, paste it into a PowerShell window and then run it.</span></span> <span data-ttu-id="17603-116">Vous serez invité à entrer les informations d’identification de l’organisation à qui vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="17603-116">You'll be prompted for credentials for the organization that you want to connect to.</span></span> 

```powershell
$UserCredential = Get-Credential
$sccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $sccSession -DisableNameChecking
$exoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $exoSession -AllowClobber -DisableNameChecking
```

<span data-ttu-id="17603-117">Vous devez exécuter les commandes dans les étapes suivantes de cette session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="17603-117">You need to run the commands in the following steps in this PowerShell session.</span></span>

## <a name="step-2-get-a-list-of-in-place-ediscovery-searches-by-using-get-mailboxsearch"></a><span data-ttu-id="17603-118">Étape 2 : Obtenir la liste des recherches In-Place de découverte électronique à l’aide de Get-MailboxSearch</span><span class="sxs-lookup"><span data-stu-id="17603-118">Step 2: Get a list of In-Place eDiscovery searches by using Get-MailboxSearch</span></span>

<span data-ttu-id="17603-119">Une fois que vous vous êtes authentifié, vous pouvez obtenir la liste In-Place recherches de découverte électronique en exécutant la cmdlet **Get-MailboxSearch.**</span><span class="sxs-lookup"><span data-stu-id="17603-119">After you've authenticated, you can get a list of In-Place eDiscovery searches by running the **Get-MailboxSearch** cmdlet.</span></span> <span data-ttu-id="17603-120">Copiez et collez la commande suivante dans PowerShell, puis exécutez-la.</span><span class="sxs-lookup"><span data-stu-id="17603-120">Copy and paste the following command into PowerShell and then run it.</span></span> <span data-ttu-id="17603-121">Une liste de recherches sera répertoriée avec leurs noms et l’état des In-Place de recherche.</span><span class="sxs-lookup"><span data-stu-id="17603-121">A list of searches will be listed with their names and the status of any In-Place Holds.</span></span>

```powershell
Get-MailboxSearch
```

<span data-ttu-id="17603-122">La sortie de la cmdlet sera similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="17603-122">The cmdlet output will be similar to the following:</span></span>

![Exemple d'Get-MailboxSearch PowerShell](../media/MigrateLegacyeDiscovery1.png)

## <a name="step-3-get-information-about-the-in-place-ediscovery-searches-and-in-place-holds-you-want-to-migrate"></a><span data-ttu-id="17603-124">Étape 3 : Obtenir des informations sur les recherches In-Place eDiscovery et les In-Place que vous souhaitez migrer</span><span class="sxs-lookup"><span data-stu-id="17603-124">Step 3: Get information about the In-Place eDiscovery searches and In-Place Holds you want to migrate</span></span>

<span data-ttu-id="17603-125">Là encore, vous utiliserez la cmdlet **Get-MailboxSearch,** mais cette fois pour obtenir les propriétés de la recherche.</span><span class="sxs-lookup"><span data-stu-id="17603-125">Again you will use the **Get-MailboxSearch** cmdlet, but this time to get the properties of the search.</span></span> <span data-ttu-id="17603-126">Vous pouvez stocker ces propriétés dans une variable pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="17603-126">You can store these properties in a variable for use later.</span></span> <span data-ttu-id="17603-127">L’exemple suivant stocke les résultats de la cmdlet **Get-MailboxSearch** dans une variable, puis affiche les propriétés de la recherche.</span><span class="sxs-lookup"><span data-stu-id="17603-127">The following example stores the results of the **Get-MailboxSearch** cmdlet in a variable and then displays the properties of the search.</span></span>

```powershell
$search = Get-MailboxSearch -Identity "Search 1"
```

```powershell
$search | FL
```

<span data-ttu-id="17603-128">La sortie de ces deux commandes sera similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="17603-128">The output of these two commands will be similar to the following:</span></span>

![Exemple de sortie PowerShell à partir de l'Get-MailboxSearch pour une recherche individuelle](../media/MigrateLegacyeDiscovery2.png)

> [!NOTE]
> <span data-ttu-id="17603-130">La durée de la In-Place de suspension dans cet exemple est indéfinie (*ItemHoldPeriod : Unlimited*).</span><span class="sxs-lookup"><span data-stu-id="17603-130">The duration of the In-Place Hold in this example is indefinite (*ItemHoldPeriod: Unlimited*).</span></span> <span data-ttu-id="17603-131">Cela est courant dans les scénarios de découverte électronique et d’enquête juridique.</span><span class="sxs-lookup"><span data-stu-id="17603-131">This is typical for eDiscovery and legal investigation scenarios.</span></span> <span data-ttu-id="17603-132">Si la durée de la conservation est différente d’une valeur indéfinie, la raison est probablement que la conservation est utilisée pour conserver du contenu dans un scénario de rétention.</span><span class="sxs-lookup"><span data-stu-id="17603-132">If the hold duration has is different value than indefinite, the reason is likely because the hold is being used to retain content in a retention scenario.</span></span> <span data-ttu-id="17603-133">Au lieu d’utiliser les cmdlets eDiscovery dans le Centre de sécurité & conformité PowerShell pour les scénarios de rétention, nous vous recommandons d’utiliser [New-RetentionCompliancePolicy](/powershell/module/exchange/new-retentioncompliancepolicy) et [New-RetentionComplianceRule](/powershell/module/exchange/new-retentioncompliancerule) pour conserver le contenu.</span><span class="sxs-lookup"><span data-stu-id="17603-133">Instead of using the eDiscovery cmdlets in Security & Compliance Center PowerShell for retention scenarios, we recommend that you use [New-RetentionCompliancePolicy](/powershell/module/exchange/new-retentioncompliancepolicy) and [New-RetentionComplianceRule](/powershell/module/exchange/new-retentioncompliancerule) to retain content.</span></span> <span data-ttu-id="17603-134">Le résultat de l’utilisation de ces cmdlets sera similaire à l’utilisation de **New-CaseHoldPolicy** et **New-CaseHoldRule,** mais vous pourrez spécifier une période de rétention et une action de rétention, telle que la suppression de contenu après l’expiration de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="17603-134">The result of using these cmdlets will be similar to using **New-CaseHoldPolicy** and **New-CaseHoldRule**, but you'll able to specify a retention period and a retention action, such as deleting content after the retention period expires.</span></span> <span data-ttu-id="17603-135">En outre, l’utilisation des cmdlets de rétention ne vous oblige pas à associer les conservations de rétention à un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="17603-135">Also, using the retention cmdlets don't require you to associate the retention holds with an eDiscovery case.</span></span>

## <a name="step-4-create-a-case-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="17603-136">Étape 4 : Créer un cas dans le Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="17603-136">Step 4: Create a case in the Microsoft 365 Compliance center</span></span>

<span data-ttu-id="17603-137">Pour créer une attente eDiscovery, vous devez créer un cas eDiscovery à associer à la recherche.</span><span class="sxs-lookup"><span data-stu-id="17603-137">To create an eDiscovery hold, you have to create an eDiscovery case to associate the hold with.</span></span> <span data-ttu-id="17603-138">L’exemple suivant crée un cas eDiscovery à l’aide du nom de votre choix.</span><span class="sxs-lookup"><span data-stu-id="17603-138">The following example creates an eDiscovery case using a name of your choice.</span></span> <span data-ttu-id="17603-139">Nous stockerons les propriétés du nouveau cas dans une variable pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="17603-139">We will store the properties of the new case in a variable for use later.</span></span> <span data-ttu-id="17603-140">Vous pouvez afficher ces propriétés en exécutant la `$case | FL` commande après avoir créé le cas.</span><span class="sxs-lookup"><span data-stu-id="17603-140">You can view those properties by running the `$case | FL` command after you create the case.</span></span>

```powershell
$case = New-ComplianceCase -Name "[Case name of your choice]"
```
![Exemple d’exécution de la commande New-ComplianceCase commande](../media/MigrateLegacyeDiscovery3.png)

## <a name="step-5-create-the-ediscovery-hold"></a><span data-ttu-id="17603-142">Étape 5 : Créer le hold eDiscovery</span><span class="sxs-lookup"><span data-stu-id="17603-142">Step 5: Create the eDiscovery hold</span></span>

<span data-ttu-id="17603-143">Une fois le cas créé, vous pouvez créer la attente et l’associer au cas que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="17603-143">After the case is created, you can create the hold and associate it with the case that you created in the previous step.</span></span> <span data-ttu-id="17603-144">Il est important de ne pas oublier que vous devez créer une stratégie de cas de attente et une règle de cas de attente.</span><span class="sxs-lookup"><span data-stu-id="17603-144">It's important to remember that you must create both a case hold policy and a case hold rule.</span></span> <span data-ttu-id="17603-145">Si la règle de mise en attente n’est pas créée après la création de la stratégie de mise en attente, la mise en attente eDiscovery n’est pas créée et tout contenu n’est pas mis en attente.</span><span class="sxs-lookup"><span data-stu-id="17603-145">If the case hold rule isn't created after you created case hold policy, the eDiscovery hold will not be created and any content won't be placed on hold.</span></span>

<span data-ttu-id="17603-146">Exécutez les commandes suivantes pour re-créer le hold eDiscovery que vous souhaitez migrer.</span><span class="sxs-lookup"><span data-stu-id="17603-146">Run the following commands to re-create the eDiscovery hold that you want to migrate.</span></span> <span data-ttu-id="17603-147">Ces exemples utilisent les propriétés de la In-Place de l’étape 3 que vous souhaitez migrer.</span><span class="sxs-lookup"><span data-stu-id="17603-147">These examples use the properties from In-Place Hold from Step 3 that you want to migrate.</span></span> <span data-ttu-id="17603-148">La première commande crée une stratégie de cas de attente et enregistre les propriétés dans une variable.</span><span class="sxs-lookup"><span data-stu-id="17603-148">The first command creates a new case hold policy and saves the properties to a variable.</span></span> <span data-ttu-id="17603-149">La deuxième commande crée la règle de cas de attente correspondante.</span><span class="sxs-lookup"><span data-stu-id="17603-149">The second command creates the corresponding case hold rule.</span></span>

```powershell
$policy = New-CaseHoldPolicy -Name $search.Name -Case $case.Identity -ExchangeLocation $search.SourceMailboxes
```

```powershell
New-CaseHoldRule -Name $search.Name -Policy $policy.Identity
```

![Exemple d’utilisation des cmdlets NewCaseHoldPolicy et NewCaseHoldRule](../media/MigrateLegacyeDiscovery4.png)

## <a name="step-6-verify-the-ediscovery-hold"></a><span data-ttu-id="17603-151">Étape 6 : Vérifier le hold eDiscovery</span><span class="sxs-lookup"><span data-stu-id="17603-151">Step 6: Verify the eDiscovery hold</span></span>

<span data-ttu-id="17603-152">Pour vous assurer qu’il n’y a aucun problème lors de la création de la mise en attente, il est bon de vérifier que l’état de la distribution de la mise en attente a réussi.</span><span class="sxs-lookup"><span data-stu-id="17603-152">To make sure there were no issues in creating the hold, it's good to check that the hold distribution status is successful.</span></span> <span data-ttu-id="17603-153">La distribution signifie que la attente a été appliquée à tous les emplacements de contenu spécifiés dans le *paramètre ExchangeLocation* à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="17603-153">Distribution means that the hold has been applied to all the content locations specified in the *ExchangeLocation* parameter in the previous step.</span></span> <span data-ttu-id="17603-154">Pour ce faire, vous pouvez exécuter la cmdlet **Get-CaseHoldPolicy.**</span><span class="sxs-lookup"><span data-stu-id="17603-154">To do this, you can run the **Get-CaseHoldPolicy** cmdlet.</span></span> <span data-ttu-id="17603-155">Étant donné que les propriétés enregistrées dans la variable $policy que vous avez créée à l’étape précédente ne sont pas automatiquement mises à jour dans la variable, vous devez réexécuter la cmdlet pour vérifier que la distribution *a* réussi.</span><span class="sxs-lookup"><span data-stu-id="17603-155">Because the properties saved to the *$policy* variable that you created in the previous step aren't automatically updated in the variable, you need to rerun the cmdlet to verify that distribution is successful.</span></span> <span data-ttu-id="17603-156">La distribution des stratégies de cas peut prendre entre 5 et 24 heures.</span><span class="sxs-lookup"><span data-stu-id="17603-156">It can take between 5 minutes and 24 hours for case hold policies to be successfully distributed.</span></span>

<span data-ttu-id="17603-157">Exécutez la commande suivante pour vérifier que la découverte électronique a bien été distribuée.</span><span class="sxs-lookup"><span data-stu-id="17603-157">Run the following command to verify that the eDiscovery hold has been successfully distributed.</span></span>

```powershell
Get-CaseHoldPolicy -Identity $policy.Identity | Select name, DistributionStatus
```

<span data-ttu-id="17603-158">La valeur Success de **la** *propriété DistributionStatus* indique que la mise en attente a été correctement placée sur les emplacements de contenu.</span><span class="sxs-lookup"><span data-stu-id="17603-158">The value of **Success** for the *DistributionStatus* property indicates the hold was successfully placed on the content locations.</span></span> <span data-ttu-id="17603-159">Si la distribution n’est pas encore terminée, la valeur **En attente** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="17603-159">If the distribution is not yet complete, a value of **Pending** is displayed.</span></span>

![Exemple de Get-CaseHoldPolicy PowerShell](../media/MigrateLegacyeDiscovery5.png)

## <a name="step-7-create-the-search"></a><span data-ttu-id="17603-161">Étape 7 : Créer la recherche</span><span class="sxs-lookup"><span data-stu-id="17603-161">Step 7: Create the search</span></span>

<span data-ttu-id="17603-162">La dernière étape consiste à re-créer la recherche que vous avez identifiée à l’étape 3 et à l’associer au cas.</span><span class="sxs-lookup"><span data-stu-id="17603-162">The last step is to re-create the search that you identified in Step 3 and associate it with the case.</span></span> <span data-ttu-id="17603-163">Après avoir créé la recherche, vous pouvez l’exécuter à l’aide de la cmdlet **Start-ComplianceSearch** ou l’exécuter ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="17603-163">After you create the search, you can run it by using the **Start-ComplianceSearch** cmdlet or run at a later time.</span></span>

```powershell
New-ComplianceSearch -Name $search.Name -ExchangeLocation $search.SourceMailboxes -ContentMatchQuery $search.SearchQuery -Case $case.name
```

![Exemple de New-ComplianceSearch PowerShell](../media/MigrateLegacyeDiscovery6.png)

## <a name="step-8-verify-the-case-hold-and-search-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="17603-165">Étape 8 : Vérifier le cas, la mise en attente et la recherche dans le Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="17603-165">Step 8: Verify the case, hold, and search in the Microsoft 365 compliance center</span></span>

<span data-ttu-id="17603-166">Pour vous assurer que tout est correctement installé, rendez-vous dans le Centre de conformité Microsoft 365 à l’adresse , puis cliquez sur [https://compliance.microsoft.com](https://compliance.microsoft.com) **eDiscovery > Core**.</span><span class="sxs-lookup"><span data-stu-id="17603-166">To make sure that everything is set up correctly, go to the Microsoft 365 compliance center at [https://compliance.microsoft.com](https://compliance.microsoft.com), and click **eDiscovery > Core**.</span></span>

![Microsoft 365 Compliance Center eDiscovery](../media/MigrateLegacyeDiscovery7.png)

<span data-ttu-id="17603-168">Le cas que vous avez créé à l’étape 3 est répertorié dans la page **Core eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="17603-168">The case that you created in Step 3 is listed on the **Core eDiscovery** page.</span></span> <span data-ttu-id="17603-169">Ouvrez le cas, puis notez la attente que vous avez créée à l’étape 4 de l’onglet **Attentes.** Vous pouvez cliquer sur la boîte aux lettres pour voir les détails, y compris le nombre de boîtes aux lettres à lesquelles la boîte aux lettres est appliquée et l’état de distribution.</span><span class="sxs-lookup"><span data-stu-id="17603-169">Open the case and then notice the hold that you created in Step 4 in listed on the **Holds** tab. You can click the hold to see details, including the number of mailboxes the hold is applied to and the distribution status.</span></span>

![eDiscovery se tient dans le Centre de conformité Microsoft 365](../media/MigrateLegacyeDiscovery8.png)

<span data-ttu-id="17603-171">La recherche que vous avez créée à l’étape  7 est répertoriée sous l’onglet Recherches du cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="17603-171">The search that you created in Step 7 is listed on the listed on the **Searches** tab of the eDiscovery case.</span></span>

![Recherche de cas eDiscovery dans le Centre de conformité Microsoft 365](../media/MigrateLegacyeDiscovery9.png)

<span data-ttu-id="17603-173">Si vous migrez une recherche eDiscovery In-Place mais que vous ne l’associez pas à un cas eDiscovery, elle sera répertoriée sur la page de recherche de contenu dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="17603-173">If you migrate an In-Place eDiscovery search but don't associate it with an eDiscovery case, it will be listed on the Content search page in the Microsoft 365 compliance center.</span></span>

## <a name="more-information"></a><span data-ttu-id="17603-174">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="17603-174">More information</span></span>

- <span data-ttu-id="17603-175">Pour plus d’informations In-Place la & eDiscovery dans le Centre d’administration Exchange, voir :</span><span class="sxs-lookup"><span data-stu-id="17603-175">For more information about In-Place eDiscovery & Holds in the Exchange admin center, see:</span></span>
  
  - [<span data-ttu-id="17603-176">Découverte électronique locale</span><span class="sxs-lookup"><span data-stu-id="17603-176">In-Place eDiscovery</span></span>](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)

  - [<span data-ttu-id="17603-177">Conservation inaltérable et conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="17603-177">In-Place Hold and Litigation Hold</span></span>](/exchange/security-and-compliance/in-place-and-litigation-holds)

- <span data-ttu-id="17603-178">Pour plus d’informations sur les cmdlets PowerShell utilisées dans l’article, voir :</span><span class="sxs-lookup"><span data-stu-id="17603-178">For more information about the PowerShell cmdlets used in the article, see:</span></span>

  - [<span data-ttu-id="17603-179">Get-MailboxSearch</span><span class="sxs-lookup"><span data-stu-id="17603-179">Get-MailboxSearch</span></span>](/powershell/module/exchange/get-mailboxsearch)
  
  - [<span data-ttu-id="17603-180">New-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="17603-180">New-ComplianceCase</span></span>](/powershell/module/exchange/new-compliancecase)

  - [<span data-ttu-id="17603-181">New-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="17603-181">New-CaseHoldPolicy</span></span>](/powershell/module/exchange/new-caseholdpolicy)
  
  - [<span data-ttu-id="17603-182">New-CaseHoldRule</span><span class="sxs-lookup"><span data-stu-id="17603-182">New-CaseHoldRule</span></span>](/powershell/module/exchange/new-caseholdrule)

  - [<span data-ttu-id="17603-183">Get-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="17603-183">Get-CaseHoldPolicy</span></span>](/powershell/module/exchange/get-caseholdpolicy)
  
  - [<span data-ttu-id="17603-184">New-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="17603-184">New-ComplianceSearch</span></span>](/powershell/module/exchange/new-compliancesearch)

  - [<span data-ttu-id="17603-185">Start-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="17603-185">Start-ComplianceSearch</span></span>](/powershell/module/exchange/start-compliancesearch)

- <span data-ttu-id="17603-186">Pour plus d’informations sur le Centre de conformité Microsoft 365, voir Vue d’ensemble du Centre de conformité [Microsoft 365.](microsoft-365-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="17603-186">For more information about the Microsoft 365 compliance center, see [Overview of the Microsoft 365 compliance center](microsoft-365-compliance-center.md).</span></span>