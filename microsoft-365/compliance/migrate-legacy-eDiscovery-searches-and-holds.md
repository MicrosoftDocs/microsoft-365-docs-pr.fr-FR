---
title: Migration des recherches et des suspensions de découverte électronique héritées vers le centre de conformité Microsoft 365
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: f53d9cbf719b0e16749c9ea1dcae2533f8c48e50
ms.sourcegitcommit: 7d07e7ec84390a8f05034d3639fa5db912809585
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42091381"
---
# <a name="migrate-legacy-ediscovery-searches-and-holds-to-the-microsoft-365-compliance-center"></a><span data-ttu-id="5c77a-102">Migration des recherches et des suspensions de découverte électronique héritées vers le centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5c77a-102">Migrate legacy eDiscovery searches and holds to the Microsoft 365 compliance center</span></span>

<span data-ttu-id="5c77a-103">Le centre de conformité Microsoft 365 offre une expérience améliorée pour l’utilisation de la fonctionnalité eDiscovery, notamment : une fiabilité plus élevée, de meilleures performances et de nombreuses fonctionnalités adaptées aux flux de travail eDiscovery, notamment des cas d’organisation de votre contenu, examiner les ensembles à Passez en revue le contenu et l’analyse pour vous aider à rechercher des données à des fins de révision, telles que le regroupement presque en double, le Threading de messagerie électronique, l’analyse des thèmes et le codage prédictif.</span><span class="sxs-lookup"><span data-stu-id="5c77a-103">The Microsoft 365 compliance center provides an improved experience for eDiscovery usage, including: higher reliability, better performance and many features tailored to eDiscovery workflows including cases to organize your content by matter, review sets to review content and analytics to help cull data for review such as near-duplicate grouping, email threading, themes analysis, and predictive coding.</span></span>

<span data-ttu-id="5c77a-104">Pour aider les clients à tirer parti des fonctionnalités nouvelles et améliorées, cet article fournit des conseils de base sur la migration des recherches de découverte électronique inaltérable dans le centre d’administration Exchange vers le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c77a-104">To help customers take advantage of the new and improved functionality, this article provides basic guidance on how to migrate In-Place eDiscovery searches and holds from the Exchange admin center to the Microsoft 365 compliance center.</span></span>

> [!NOTE]
> <span data-ttu-id="5c77a-105">Étant donné qu’il existe de nombreux scénarios différents, cet article fournit des conseils généraux pour effectuer des recherches et des suspensions dans un cas de découverte électronique de base dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c77a-105">Because there are many different scenarios, this article provides general guidance to transition searches and holds to a core eDiscovery case in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="5c77a-106">L’utilisation de cas de découverte électronique n’est pas toujours requise, mais elle ajoute une couche supplémentaire de sécurité en vous permettant d’attribuer des autorisations pour contrôler les personnes ayant accès aux cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5c77a-106">Using eDiscovery cases aren't always required, but they add an extra layer of security by letting you assign permissions to control who has access to the eDiscovery cases in your organization.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="5c77a-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5c77a-107">Before you begin</span></span>

- <span data-ttu-id="5c77a-108">Pour exécuter les commandes PowerShell décrites dans cet article, vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de conformité Office 365 Security &.</span><span class="sxs-lookup"><span data-stu-id="5c77a-108">You have to be a member of the eDiscovery Manager role group in the Office 365 Security & Compliance Center to run the PowerShell commands described in this article.</span></span> <span data-ttu-id="5c77a-109">Vous devez également être membre du groupe de rôles gestion de la découverte dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c77a-109">You also have to be a member of the Discovery Management role group in the Exchange admin center.</span></span>

- <span data-ttu-id="5c77a-110">Cet article fournit des instructions sur la création d’une conservation eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="5c77a-110">This article provides guidance on how to create an eDiscovery hold.</span></span> <span data-ttu-id="5c77a-111">La stratégie de blocage sera appliquée aux boîtes aux lettres par le biais d’un processus asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5c77a-111">The hold policy will be applied to mailboxes through an asynchronous process.</span></span> <span data-ttu-id="5c77a-112">Lors de la création d’une conservation de découverte électronique, vous devez créer un CaseHoldPolicy et CaseHoldRule, sinon la conservation ne sera pas créée et les emplacements de contenu ne seront pas mis en attente.</span><span class="sxs-lookup"><span data-stu-id="5c77a-112">When creating an eDiscovery hold, you must create both a CaseHoldPolicy and CaseHoldRule, otherwise the hold will not be created and content locations will not be placed on hold.</span></span>

## <a name="step-1-connect-to-exchange-online-powershell-and-office-365-security--compliance-center-powershell"></a><span data-ttu-id="5c77a-113">Étape 1 : Connectez-vous à Exchange Online PowerShell et à Office 365 Security & Compliance Center PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c77a-113">Step 1: Connect to Exchange Online PowerShell and Office 365 Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="5c77a-114">La première étape consiste à vous connecter au centre de sécurité Exchange Online PowerShell et Office 365 Security & PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5c77a-114">The first step is to connect to Exchange Online PowerShell and Office 365 Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="5c77a-115">Vous pouvez copier le script suivant, le coller dans une fenêtre PowerShell, puis l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="5c77a-115">You can copy the following script, paste it into a PowerShell window and then run it.</span></span> <span data-ttu-id="5c77a-116">Vous serez invité à fournir les informations d’identification de l’organisation à laquelle vous souhaitez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="5c77a-116">You'll be prompted for credentials for the organization that you want to connect to.</span></span> 

```powershell
$UserCredential = Get-Credential
$sccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $sccSession -DisableNameChecking
$exoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $exoSession -AllowClobber -DisableNameChecking
```

<span data-ttu-id="5c77a-117">Vous devez exécuter les commandes dans les étapes suivantes de cette session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5c77a-117">You need to run the commands in the following steps in this PowerShell session.</span></span>

## <a name="step-2-get-a-list-of-in-place-ediscovery-searches-by-using-get-mailboxsearch"></a><span data-ttu-id="5c77a-118">Étape 2 : obtenir la liste des recherches de découverte électronique inaltérable à l’aide de Get-MailboxSearch</span><span class="sxs-lookup"><span data-stu-id="5c77a-118">Step 2: Get a list of In-Place eDiscovery searches by using Get-MailboxSearch</span></span>

<span data-ttu-id="5c77a-119">Une fois que vous avez effectué l’authentification, vous pouvez obtenir la liste des recherches de découverte électronique inaltérable en exécutant la cmdlet **Get-MailboxSearch** .</span><span class="sxs-lookup"><span data-stu-id="5c77a-119">After you've authenticated, you can get a list of In-Place eDiscovery searches by running the **Get-MailboxSearch** cmdlet.</span></span> <span data-ttu-id="5c77a-120">Copiez et collez la commande suivante dans PowerShell, puis exécutez-la.</span><span class="sxs-lookup"><span data-stu-id="5c77a-120">Copy and paste the following command into PowerShell and then run it.</span></span> <span data-ttu-id="5c77a-121">Une liste des recherches s’affiche avec leur nom et l’état des conservations inaltérables.</span><span class="sxs-lookup"><span data-stu-id="5c77a-121">A list of searches will be listed with their names and the status of any In-Place Holds.</span></span>

```powershell
Get-MailboxSearch
```

<span data-ttu-id="5c77a-122">La sortie de la cmdlet sera semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5c77a-122">The cmdlet output will be similar to the following:</span></span>

![Exemple PowerShell Get-MailboxSearch](../media/MigrateLegacyeDiscovery1.png)

## <a name="step-3-get-information-about-the-in-place-ediscovery-searches-and-in-place-holds-you-want-to-migrate"></a><span data-ttu-id="5c77a-124">Étape 3 : obtenir des informations sur les recherches de découverte électronique inaltérable et les conservations inaltérables que vous souhaitez migrer</span><span class="sxs-lookup"><span data-stu-id="5c77a-124">Step 3: Get information about the In-Place eDiscovery searches and In-Place Holds you want to migrate</span></span>

<span data-ttu-id="5c77a-125">Une fois encore, vous allez utiliser la cmdlet **Get-MailboxSearch** , mais cette fois pour obtenir les propriétés de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5c77a-125">Again you will use the **Get-MailboxSearch** cmdlet, but this time to get the properties of the search.</span></span> <span data-ttu-id="5c77a-126">Vous pouvez stocker ces propriétés dans une variable pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5c77a-126">You can store these properties in a variable for use later.</span></span> <span data-ttu-id="5c77a-127">L’exemple suivant stocke les résultats de la cmdlet **Get-MailboxSearch** dans une variable, puis affiche les propriétés de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5c77a-127">The following example stores the results of the **Get-MailboxSearch** cmdlet in a variable and then displays the properties of the search.</span></span>

```powershell
$search = Get-MailboxSearch -Identity "Search 1"
```

```powershell
$search | FL
```

<span data-ttu-id="5c77a-128">La sortie de ces deux commandes est similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5c77a-128">The output of these two commands will be similar to the following:</span></span>

![Exemple de sortie PowerShell de l’utilisation de Get-MailboxSearch pour une recherche individuelle](../media/MigrateLegacyeDiscovery2.png)

> [!NOTE]
> <span data-ttu-id="5c77a-130">La durée de la conservation inaltérable dans cet exemple est indéfinie (*ItemHoldPeriod : Unlimited*).</span><span class="sxs-lookup"><span data-stu-id="5c77a-130">The duration of the In-Place Hold in this example is indefinite (*ItemHoldPeriod: Unlimited*).</span></span> <span data-ttu-id="5c77a-131">C’est généralement le cas pour la découverte électronique et les scénarios d’enquête légale.</span><span class="sxs-lookup"><span data-stu-id="5c77a-131">This is typical for eDiscovery and legal investigation scenarios.</span></span> <span data-ttu-id="5c77a-132">Si la durée de la conservation est différente de la valeur indéfinie, la raison est probablement le fait que la conservation est utilisée pour conserver le contenu dans un scénario de rétention.</span><span class="sxs-lookup"><span data-stu-id="5c77a-132">If the hold duration has is different value than indefinite, the reason is likely because the hold is being used to retain content in a retention scenario.</span></span> <span data-ttu-id="5c77a-133">Au lieu d’utiliser les applets de commande eDiscovery dans Office 365 Security & Centre de conformité PowerShell pour les scénarios de rétention, nous vous recommandons d’utiliser [New-retentioncompliancepolicy permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancepolicy) et [New-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancerule) pour conserver le contenu.</span><span class="sxs-lookup"><span data-stu-id="5c77a-133">Instead of using the eDiscovery cmdlets in Office 365 Security & Compliance Center PowerShell for retention scenarios, we recommend that you use [New-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancepolicy) and [New-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancerule) to retain content.</span></span> <span data-ttu-id="5c77a-134">Le résultat de l’utilisation de ces cmdlets est similaire à celui de **New-CaseHoldPolicy** et **New-CaseHoldRule**, mais vous pouvez spécifier une période de rétention et une action de rétention, telles que la suppression de contenu après l’expiration de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="5c77a-134">The result of using these cmdlets will be similar to using **New-CaseHoldPolicy** and **New-CaseHoldRule**, but you'll able to specify a retention period and a retention action, such as deleting content after the retention period expires.</span></span> <span data-ttu-id="5c77a-135">En outre, l’utilisation des cmdlets de rétention n’exige pas que vous associiez les conservations de rétention à un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="5c77a-135">Also, using the retention cmdlets don't require you to associate the retention holds with an eDiscovery case.</span></span>

## <a name="step-4-create-a-case-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="5c77a-136">Étape 4 : créer un cas dans le centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5c77a-136">Step 4: Create a case in the Microsoft 365 Compliance center</span></span>

<span data-ttu-id="5c77a-137">Pour créer une conservation de découverte électronique, vous devez créer un cas eDiscovery pour associer le blocage à.</span><span class="sxs-lookup"><span data-stu-id="5c77a-137">To create an eDiscovery hold, you have to create an eDiscovery case to associate the hold with.</span></span> <span data-ttu-id="5c77a-138">L’exemple suivant crée un cas de découverte électronique à l’aide d’un nom de votre choix.</span><span class="sxs-lookup"><span data-stu-id="5c77a-138">The following example creates an eDiscovery case using a name of your choice.</span></span> <span data-ttu-id="5c77a-139">Nous allons stocker les propriétés du nouveau cas dans une variable pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5c77a-139">We will store the properties of the new case in a variable for use later.</span></span> <span data-ttu-id="5c77a-140">Vous pouvez afficher ces propriétés en exécutant la `$case | FL` commande après avoir créé le cas.</span><span class="sxs-lookup"><span data-stu-id="5c77a-140">You can view those properties by running the `$case | FL` command after you create the case.</span></span>

```powershell
$case = New-ComplianceCase -Name "[Case name of your choice]"
```
![Exemple d’exécution de la commande New-ComplianceCase](../media/MigrateLegacyeDiscovery3.png)

## <a name="step-5-create-the-ediscovery-hold"></a><span data-ttu-id="5c77a-142">Étape 5 : créer le blocage eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5c77a-142">Step 5: Create the eDiscovery hold</span></span>

<span data-ttu-id="5c77a-143">Une fois le cas créé, vous pouvez créer la conservation et l’associer au cas que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="5c77a-143">After the case is created, you can create the hold and associate it with the case that you created in the previous step.</span></span> <span data-ttu-id="5c77a-144">N’oubliez pas que vous devez créer une stratégie de blocage de cas et une règle de conservation des cas.</span><span class="sxs-lookup"><span data-stu-id="5c77a-144">It's important to remember that you must create both a case hold policy and a case hold rule.</span></span> <span data-ttu-id="5c77a-145">Si la règle de conservation des dossiers n’est pas créée après la création de la stratégie de blocage de cas, la conservation de la découverte électronique n’est pas créée et aucun contenu n’est placé en conservation.</span><span class="sxs-lookup"><span data-stu-id="5c77a-145">If the case hold rule isn't created after you created case hold policy, the eDiscovery hold will not be created and any content won't be placed on hold.</span></span>

<span data-ttu-id="5c77a-146">Exécutez les commandes suivantes pour recréer le blocage eDiscovery que vous souhaitez migrer.</span><span class="sxs-lookup"><span data-stu-id="5c77a-146">Run the following commands to re-create the eDiscovery hold that you want to migrate.</span></span> <span data-ttu-id="5c77a-147">Ces exemples utilisent les propriétés du blocage sur place de l’étape 3 que vous souhaitez migrer.</span><span class="sxs-lookup"><span data-stu-id="5c77a-147">These examples use the properties from In-Place Hold from Step 3 that you want to migrate.</span></span> <span data-ttu-id="5c77a-148">La première commande crée une stratégie de conservation de la demande de devis et enregistre les propriétés dans une variable.</span><span class="sxs-lookup"><span data-stu-id="5c77a-148">The first command creates a new case hold policy and saves the properties to a variable.</span></span> <span data-ttu-id="5c77a-149">La deuxième commande crée la règle de conservation de casse correspondante.</span><span class="sxs-lookup"><span data-stu-id="5c77a-149">The second command creates the corresponding case hold rule.</span></span>

```powershell
$policy = New-CaseHoldPolicy -Name $search.Name -Case $case.Identity -ExchangeLocation $search.SourceMailboxes
```

```powershell
New-CaseHoldRule -Name $search.Name -Policy $policy.Identity
```

![Exemple d’utilisation des applets de commande NewCaseHoldPolicy et NewCaseHoldRule](../media/MigrateLegacyeDiscovery4.png)

## <a name="step-6-verify-the-ediscovery-hold"></a><span data-ttu-id="5c77a-151">Étape 6 : vérifier la conservation de la découverte électronique</span><span class="sxs-lookup"><span data-stu-id="5c77a-151">Step 6: Verify the eDiscovery hold</span></span>

<span data-ttu-id="5c77a-152">Pour vous assurer qu’il n’y a aucun problème lors de la création de la suspension, il est conseillé de vérifier que l’état de distribution de suspension est réussi.</span><span class="sxs-lookup"><span data-stu-id="5c77a-152">To make sure there were no issues in creating the hold, it's good to check that the hold distribution status is successful.</span></span> <span data-ttu-id="5c77a-153">La distribution signifie que la conservation a été appliquée à tous les emplacements de contenu spécifiés dans le paramètre *exchangelocation permet* à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="5c77a-153">Distribution means that the hold has been applied to all the content locations specified in the *ExchangeLocation* parameter in the previous step.</span></span> <span data-ttu-id="5c77a-154">Pour ce faire, vous pouvez exécuter la cmdlet **Get-CaseHoldPolicy** .</span><span class="sxs-lookup"><span data-stu-id="5c77a-154">To do this, you can run the **Get-CaseHoldPolicy** cmdlet.</span></span> <span data-ttu-id="5c77a-155">Étant donné que les propriétés enregistrées dans la variable *$Policy* que vous avez créée à l’étape précédente ne sont pas automatiquement mises à jour dans la variable, vous devez réexécuter l’applet de commande pour vérifier que la distribution a réussi.</span><span class="sxs-lookup"><span data-stu-id="5c77a-155">Because the properties saved to the *$policy* variable that you created in the previous step aren't automatically updated in the variable, you need to rerun the cmdlet to verify that distribution is successful.</span></span> <span data-ttu-id="5c77a-156">La distribution des stratégies de conservation des dossiers peut prendre entre 5 minutes et 24 heures.</span><span class="sxs-lookup"><span data-stu-id="5c77a-156">It can take between 5 minutes and 24 hours for case hold policies to be successfully distributed.</span></span>

<span data-ttu-id="5c77a-157">Exécutez la commande suivante pour vérifier que la conservation de découverte électronique a été correctement distribuée.</span><span class="sxs-lookup"><span data-stu-id="5c77a-157">Run the following command to verify that the eDiscovery hold has been successfully distributed.</span></span>

```powershell
Get-CaseHoldPolicy -Identity $policy.Identity | Select name, DistributionStatus
```

<span data-ttu-id="5c77a-158">La valeur de **Success** pour la propriété *DistributionStatus* indique que la conservation a été correctement placée sur les emplacements de contenu.</span><span class="sxs-lookup"><span data-stu-id="5c77a-158">The value of **Success** for the *DistributionStatus* property indicates the hold was successfully placed on the content locations.</span></span> <span data-ttu-id="5c77a-159">Si la distribution n’est pas encore terminée, la valeur **en attente** est affichée.</span><span class="sxs-lookup"><span data-stu-id="5c77a-159">If the distribution is not yet complete, a value of **Pending** is displayed.</span></span>

![Exemple PowerShell Get-CaseHoldPolicy](../media/MigrateLegacyeDiscovery5.png)

## <a name="step-7-create-the-search"></a><span data-ttu-id="5c77a-161">Étape 7 : créer la recherche</span><span class="sxs-lookup"><span data-stu-id="5c77a-161">Step 7: Create the search</span></span>

<span data-ttu-id="5c77a-162">La dernière étape consiste à recréer la recherche que vous avez identifiée à l’étape 3 et à l’associer au cas.</span><span class="sxs-lookup"><span data-stu-id="5c77a-162">The last step is to re-create the search that you identified in Step 3 and associate it with the case.</span></span> <span data-ttu-id="5c77a-163">Une fois la recherche créée, vous pouvez l’exécuter à l’aide de la cmdlet **Start-ComplianceSearch** ou de l’exécuter ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="5c77a-163">After you create the search, you can run it by using the **Start-ComplianceSearch** cmdlet or run at a later time.</span></span>

```powershell
New-ComplianceSearch -Name $search.Name -ExchangeLocation $search.SourceMailboxes -ContentMatchQuery $search.SearchQuery -Case $case.name
```

![PowerShell New-ComplianceSearch-exemple](../media/MigrateLegacyeDiscovery6.png)

## <a name="step-8-verify-the-case-hold-and-search-in-the-microsoft-365-compliance-center"></a><span data-ttu-id="5c77a-165">Étape 8 : vérifier le cas, la mise en attente et la recherche dans le centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5c77a-165">Step 8: Verify the case, hold, and search in the Microsoft 365 compliance center</span></span>

<span data-ttu-id="5c77a-166">Pour vous assurer que tout est correctement configuré, accédez au centre de conformité Microsoft 365 à l' [https://compliance.microsoft.com](https://compliance.microsoft.com)adresse, puis cliquez sur **eDiscovery > Core**.</span><span class="sxs-lookup"><span data-stu-id="5c77a-166">To make sure that everything is set up correctly, go to the Microsoft 365 compliance center at [https://compliance.microsoft.com](https://compliance.microsoft.com), and click **eDiscovery > Core**.</span></span>

![Découverte électronique du centre de conformité Microsoft 365](../media/MigrateLegacyeDiscovery7.png)

<span data-ttu-id="5c77a-168">Le cas que vous avez créé à l’étape 3 est affiché dans la page de **découverte électronique principale** .</span><span class="sxs-lookup"><span data-stu-id="5c77a-168">The case that you created in Step 3 is listed on the **Core eDiscovery** page.</span></span> <span data-ttu-id="5c77a-169">Ouvrez le cas, puis notez le blocage que vous avez créé à l’étape 4 de la figure de l’onglet **suspensions** . Vous pouvez cliquer sur le blocage pour afficher les détails, notamment le nombre de boîtes aux lettres auxquelles la conservation est appliquée et l’état de la distribution.</span><span class="sxs-lookup"><span data-stu-id="5c77a-169">Open the case and then notice the hold that you created in Step 4 in listed on the **Holds** tab. You can click the hold to see details, including the number of mailboxes the hold is applied to and the distribution status.</span></span>

![conservations eDiscovery dans le centre de conformité Microsoft 365](../media/MigrateLegacyeDiscovery8.png)

<span data-ttu-id="5c77a-171">La recherche que vous avez créée à l’étape 7 est indiquée dans la boîte de l’onglet **recherches** du cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="5c77a-171">The search that you created in Step 7 is listed on the listed on the **Searches** tab of the eDiscovery case.</span></span>

![recherche de cas eDiscovery dans le centre de conformité Microsoft 365](../media/MigrateLegacyeDiscovery9.png)

<span data-ttu-id="5c77a-173">Si vous migrez une recherche de découverte électronique inaltérable, mais que vous ne l’associez pas à un cas de découverte électronique, celle-ci est indiquée sur la page recherche de contenu dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c77a-173">If you migrate an In-Place eDiscovery search but don't associate it with an eDiscovery case, it will be listed on the Content search page in the Microsoft 365 compliance center.</span></span>

## <a name="more-information"></a><span data-ttu-id="5c77a-174">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5c77a-174">More information</span></span>

- <span data-ttu-id="5c77a-175">Pour plus d’informations sur les conservations de la découverte électronique inaltérable & dans le centre d’administration Exchange, voir :</span><span class="sxs-lookup"><span data-stu-id="5c77a-175">For more information about In-Place eDiscovery & Holds in the Exchange admin center, see:</span></span>
  
  - [<span data-ttu-id="5c77a-176">Découverte électronique locale</span><span class="sxs-lookup"><span data-stu-id="5c77a-176">In-Place eDiscovery</span></span>](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)

  - [<span data-ttu-id="5c77a-177">Conservation inaltérable et conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="5c77a-177">In-Place Hold and Litigation Hold</span></span>](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds)

- <span data-ttu-id="5c77a-178">Pour plus d’informations sur les applets de commande PowerShell utilisées dans l’article, voir :</span><span class="sxs-lookup"><span data-stu-id="5c77a-178">For more information about the PowerShell cmdlets used in the article, see:</span></span>

  - [<span data-ttu-id="5c77a-179">Get-MailboxSearch</span><span class="sxs-lookup"><span data-stu-id="5c77a-179">Get-MailboxSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/get-mailboxsearch)
  
  - [<span data-ttu-id="5c77a-180">New-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="5c77a-180">New-ComplianceCase</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-ediscovery/new-compliancecase)

  - [<span data-ttu-id="5c77a-181">New-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="5c77a-181">New-CaseHoldPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-ediscovery/new-caseholdpolicy)
  
  - [<span data-ttu-id="5c77a-182">New-CaseHoldRule</span><span class="sxs-lookup"><span data-stu-id="5c77a-182">New-CaseHoldRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-ediscovery/new-caseholdrule)

  - [<span data-ttu-id="5c77a-183">Get-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="5c77a-183">Get-CaseHoldPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-ediscovery/get-caseholdpolicy)
  
  - [<span data-ttu-id="5c77a-184">New-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="5c77a-184">New-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)

  - [<span data-ttu-id="5c77a-185">Start-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="5c77a-185">Start-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)

- <span data-ttu-id="5c77a-186">Pour plus d’informations sur le centre de conformité Microsoft 365, consultez [la rubrique Overview of the microsoft 365 Compliance Center](microsoft-365-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="5c77a-186">For more information about the Microsoft 365 compliance center, see [Overview of the Microsoft 365 compliance center](microsoft-365-compliance-center.md).</span></span>
