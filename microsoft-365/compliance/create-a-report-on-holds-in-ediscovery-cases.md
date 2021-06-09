---
title: 'Créer un rapport sur les conservations définies dans les cas eDiscovery '
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment générer un rapport qui contient des informations sur toutes les actuellement en cours associées à des cas eDiscovery.
ms.openlocfilehash: 04282f6f2481d892fa16d685936efeec55feae77
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50908408"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases"></a><span data-ttu-id="68709-103">Créer un rapport sur les conservations définies dans les cas eDiscovery </span><span class="sxs-lookup"><span data-stu-id="68709-103">Create a report on holds in eDiscovery cases</span></span>

<span data-ttu-id="68709-104">Le script de cet article permet aux administrateurs eDiscovery et aux responsables eDiscovery de générer un rapport qui contient des informations sur toutes les obligations associées aux cas eDiscovery dans le centre de conformité dans Office 365 ou Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="68709-104">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the the compliance center in Office 365 or Microsoft 365.</span></span> <span data-ttu-id="68709-105">Le rapport contient des informations telles que le nom du cas où une mise en attente est associée, les emplacements de contenu qui sont placés en attente et si la mise en attente est basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="68709-105">The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based.</span></span> <span data-ttu-id="68709-106">S’il existe des cas qui n’ont aucune attente, le script crée un rapport supplémentaire avec une liste de cas sans attente.</span><span class="sxs-lookup"><span data-stu-id="68709-106">If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="68709-107">Consultez la section [Plus](#more-information) d’informations pour obtenir une description détaillée des informations incluses dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="68709-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span>

## <a name="admin-requirements-and-script-information"></a><span data-ttu-id="68709-108">Exigences de l’administrateur et informations sur les scripts</span><span class="sxs-lookup"><span data-stu-id="68709-108">Admin requirements and script information</span></span>

- <span data-ttu-id="68709-109">Pour générer un rapport sur tous les cas eDiscovery de votre organisation, vous devez être administrateur eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68709-109">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization.</span></span> <span data-ttu-id="68709-110">Si vous êtes gestionnaire eDiscovery, le rapport inclut uniquement des informations sur les cas accessibles.</span><span class="sxs-lookup"><span data-stu-id="68709-110">If you are an eDiscovery Manager, the report will only include information about the cases that you can access.</span></span> <span data-ttu-id="68709-111">Pour plus d’informations sur les autorisations eDiscovery, voir [Attribuer des autorisations eDiscovery.](assign-ediscovery-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="68709-111">For more information about eDiscovery permissions, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>

- <span data-ttu-id="68709-112">Le script de cet article présente une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="68709-112">The script in this article has minimal error handling.</span></span> <span data-ttu-id="68709-113">L’objectif principal est de créer rapidement un rapport sur les cas de découverte électronique associés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68709-113">The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>

- <span data-ttu-id="68709-p104">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="68709-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-connect-to-the-security--compliance-center-powershell"></a><span data-ttu-id="68709-119">Étape 1 : Connecter au Centre de sécurité & conformité PowerShell</span><span class="sxs-lookup"><span data-stu-id="68709-119">Step 1: Connect to the Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="68709-120">L’étape suivante consiste à se connecter au Centre de sécurité et conformité PowerShell de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68709-120">The first step is to connect to Security & Compliance Center PowerShell for your organization.</span></span> <span data-ttu-id="68709-121">Pour consulter des instructions détaillées, voir [Se connecter au Centre de sécurité et conformité PowerShell](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="68709-121">For step-by-step instructions, see [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="68709-122">Étape 2 : Exécuter le script pour signaler les cas de découverte électronique associés</span><span class="sxs-lookup"><span data-stu-id="68709-122">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="68709-123">Une fois que vous êtes connecté au Centre de sécurité & conformité PowerShell, l’étape suivante consiste à créer et exécuter le script qui collecte des informations sur les cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68709-123">After you've connected to Security & Compliance Center PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span>

1. <span data-ttu-id="68709-124">Enregistrez le texte suivant dans un fichier Windows PowerShell script à l’aide d’un suffixe de nom de fichier .ps1 ; par exemple, CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="68709-124">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span>

   ```powershell
   #script begin
   " "
   write-host "***********************************************"
   write-host "   Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
   write-host "        eDiscovery cases - Holds report         " -foregroundColor yellow -backgroundcolor darkgreen
   write-host "***********************************************"
   " "
   #prompt users to specify a path to store the output files
   $time=get-date
   $Path = Read-Host 'Enter a file path to save the report to a .csv file'
   $outputpath=$Path+'\'+'CaseHoldsReport'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
   $noholdsfilepath=$Path+'\'+'CaseswithNoHolds'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
   #add case details to the csv file
   function add-tocasereport{
   Param([string]$casename,
   [String]$casestatus,
   [datetime]$casecreatedtime,
   [string]$casemembers,
   [datetime]$caseClosedDateTime,
   [string]$caseclosedby,
   [string]$holdname,
   [String]$Holdenabled,
   [string]$holdcreatedby,
   [string]$holdlastmodifiedby,
   [string]$ExchangeLocation,
   [string]$sharePointlocation,
   [string]$ContentMatchQuery,
   [datetime]$holdcreatedtime,
   [datetime]$holdchangedtime
   )
   $addRow = New-Object PSObject
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case name" -Value $casename
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case status" -Value $casestatus
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case members" -Value $casemembers
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case created time" -Value $casecreatedtime
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed time" -Value $caseClosedDateTime
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed by" -Value $caseclosedby
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold name" -Value $holdname
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold enabled" -Value $Holdenabled
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created by" -Value $holdcreatedby
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold last changed by" -Value $holdlastmodifiedby
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Exchange locations" -Value  $ExchangeLocation
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "SharePoint locations" -Value $sharePointlocation
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold query" -Value $ContentMatchQuery
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created time (UTC)" -Value $holdcreatedtime
   Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold changed time (UTC)" -Value $holdchangedtime
   $allholdreport = $addRow | Select-Object "Case name","Case status","Hold name","Hold enabled","Case members", "Case created time","Case closed time","Case closed by","Exchange locations","SharePoint locations","Hold query","Hold created by","Hold created time (UTC)","Hold last changed by","Hold changed time (UTC)"
   $allholdreport | export-csv -path $outputPath -notypeinfo -append -Encoding ascii
   }
   #get information on the cases and pass values to the case report function
   " "
   write-host "Gathering a list of cases and holds..."
   " "
   $edc =Get-ComplianceCase -ErrorAction SilentlyContinue
   foreach($cc in $edc)
   {
   write-host "Working on case :" $cc.name
   if($cc.status -eq 'Closed')
   {
   $cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
   add-tocasereport -casename $cc.name -casestatus $cc.Status -caseclosedby $cc.closedby -caseClosedDateTime $cc.ClosedDateTime -casemembers $cmembers
   }
   else{
   $cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
   $policies = Get-CaseHoldPolicy -Case $cc.Name | %{ Get-CaseHoldPolicy $_.Name -Case $_.CaseId -DistributionDetail}
   if ($policies -ne $NULL)
   {
   foreach ($policy in $policies)
   {
   $rule=Get-CaseHoldRule -Policy $policy.name
   add-tocasereport -casename $cc.name -casemembers $cmembers -casestatus $cc.Status -casecreatedtime $cc.CreatedDateTime -holdname $policy.name -holdenabled $policy.enabled -holdcreatedby $policy.CreatedBy -holdlastmodifiedby $policy.LastModifiedBy -ExchangeLocation (($policy.exchangelocation.name)-join ';') -SharePointLocation (($policy.sharePointlocation.name)-join ';') -ContentMatchQuery $rule.ContentMatchQuery -holdcreatedtime $policy.WhenCreatedUTC -holdchangedtime $policy.WhenChangedUTC
   }
   }
   else{
   write-host "No hold policies found in case:" $cc.name -foregroundColor 'Yellow'
   " "
   [string]$cc.name | out-file -filepath $noholdsfilepath -append
   }
   }
   }

   " "
   Write-host "Script complete! Report files saved to this folder: '$Path'"
   " "
   #script end
   ```

2. <span data-ttu-id="68709-125">Dans la session Windows PowerShell ouverte à l’étape 1, allez dans le dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="68709-125">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span>

3. <span data-ttu-id="68709-126">Exécutez le script . par exemple :</span><span class="sxs-lookup"><span data-stu-id="68709-126">Run the script; for example:</span></span>

   ```powershell
   .\CaseHoldsReport.ps1
   ```

   <span data-ttu-id="68709-127">Le script vous invite à enregistrer le rapport dans un dossier cible.</span><span class="sxs-lookup"><span data-stu-id="68709-127">The script will prompt for a target folder to save the report to.</span></span>

4. <span data-ttu-id="68709-128">Tapez le nom du chemin d’accès complet du dossier où enregistrer le rapport, puis appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="68709-128">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>

   > [!TIP]
   > <span data-ttu-id="68709-129">Pour enregistrer le rapport dans le dossier où se trouve le script, tapez un point (« . ») lorsque vous y invitez un dossier cible.</span><span class="sxs-lookup"><span data-stu-id="68709-129">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder.</span></span> <span data-ttu-id="68709-130">Pour enregistrer le rapport dans un sous-dossier du dossier où se trouve le script, tapez simplement le nom du sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="68709-130">To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span>

   <span data-ttu-id="68709-131">Le script commence à collecter des informations sur tous les cas eDiscovery de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68709-131">The script starts to collect information about all the eDiscovery cases in your organization.</span></span> <span data-ttu-id="68709-132">N’accédez pas au fichier de rapport pendant l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="68709-132">Don't access the report file while the script is running.</span></span> <span data-ttu-id="68709-133">Une fois le script terminé, un message de confirmation s’affiche dans la session Windows PowerShell session.</span><span class="sxs-lookup"><span data-stu-id="68709-133">After the script is complete, a confirmation message is displayed in the Windows PowerShell session.</span></span> <span data-ttu-id="68709-134">Une fois ce message affiché, vous pouvez accéder au rapport dans le dossier que vous avez spécifié à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="68709-134">After this message is displayed, you can access the report in the folder that you specified in Step 4.</span></span> <span data-ttu-id="68709-135">Le nom de fichier du rapport est `CaseHoldsReport<DateTimeStamp>.csv` .</span><span class="sxs-lookup"><span data-stu-id="68709-135">The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

   <span data-ttu-id="68709-136">Par ailleurs, le script crée également un rapport avec une liste de cas qui ne sont pas en attente.</span><span class="sxs-lookup"><span data-stu-id="68709-136">Addtionally, the script also creates a report with a list of cases that don't have any holds.</span></span> <span data-ttu-id="68709-137">Le nom de fichier de ce rapport est `CaseswithNoHolds<DateTimeStamp>.csv` .</span><span class="sxs-lookup"><span data-stu-id="68709-137">The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>

   <span data-ttu-id="68709-138">Voici un exemple d’exécution du script CaseHoldsReport.ps1 script.</span><span class="sxs-lookup"><span data-stu-id="68709-138">Here's an example of running the CaseHoldsReport.ps1 script.</span></span>

   ![Sortie après l’exécution du script CaseHoldsReport.ps1 script](../media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)

## <a name="more-information"></a><span data-ttu-id="68709-140">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="68709-140">More information</span></span>

<span data-ttu-id="68709-141">Le rapport de cas qui est créé lorsque vous exécutez le script dans cet article contient les informations suivantes sur chaque attente.</span><span class="sxs-lookup"><span data-stu-id="68709-141">The case holds report that's created when you run the script in this article contains the following information about each hold.</span></span> <span data-ttu-id="68709-142">Comme indiqué précédemment, vous devez être administrateur eDiscovery pour retourner des informations pour toutes les ententées de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68709-142">As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization.</span></span> <span data-ttu-id="68709-143">Pour plus d’informations sur les cas de non-lieu, voir les cas [eDiscovery.](./get-started-core-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="68709-143">For more information about case holds, see [eDiscovery cases](./get-started-core-ediscovery.md).</span></span>

- <span data-ttu-id="68709-144">Nom de la garde à vue et nom du cas eDiscovery à l’associé.</span><span class="sxs-lookup"><span data-stu-id="68709-144">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>

- <span data-ttu-id="68709-145">Si le cas eDiscovery est actif ou fermé.</span><span class="sxs-lookup"><span data-stu-id="68709-145">Whether or not the eDiscovery case is active or closed.</span></span>

- <span data-ttu-id="68709-146">Si la attente est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="68709-146">Whether or not the hold is enabled or disabled.</span></span>

- <span data-ttu-id="68709-147">Les membres du cas eDiscovery associés à la attente.</span><span class="sxs-lookup"><span data-stu-id="68709-147">The members of the eDiscovery case that the hold is associated with.</span></span> <span data-ttu-id="68709-148">Les membres de cas peuvent afficher ou gérer un cas, en fonction des autorisations eDiscovery qui leur ont été attribuées.</span><span class="sxs-lookup"><span data-stu-id="68709-148">Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>

- <span data-ttu-id="68709-149">Heure et date de création du cas.</span><span class="sxs-lookup"><span data-stu-id="68709-149">The time and date the case was created.</span></span>

- <span data-ttu-id="68709-150">Si un cas est fermé, la personne qui l’a fermé, ainsi que l’heure et la date de fermeture.</span><span class="sxs-lookup"><span data-stu-id="68709-150">If a case is closed, the person who closed it and the time and date it was closed.</span></span>

- <span data-ttu-id="68709-151">Le Exchange boîtes aux lettres et SharePoint sites en attente.</span><span class="sxs-lookup"><span data-stu-id="68709-151">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>

- <span data-ttu-id="68709-152">Si la requête est en attente, la syntaxe de la requête.</span><span class="sxs-lookup"><span data-stu-id="68709-152">If the hold is query-based, the query syntax.</span></span>

- <span data-ttu-id="68709-153">Heure et date de création de la attente et de la personne qui l’a créée.</span><span class="sxs-lookup"><span data-stu-id="68709-153">The time and date the hold was created and the person who created it.</span></span>

- <span data-ttu-id="68709-154">Heure et date de la dernière changement de la date et de la personne qui l’a modifiée.</span><span class="sxs-lookup"><span data-stu-id="68709-154">The time and date the hold was last changed and the person who changed it.</span></span>