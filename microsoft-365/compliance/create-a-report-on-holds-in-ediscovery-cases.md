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
description: Découvrez comment générer un rapport qui contient des informations sur toutes les conservations associées à des cas eDiscovery.
ms.openlocfilehash: b4387434d57373f9569b6472786e8ad40de85b21
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44818033"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases"></a><span data-ttu-id="39901-103">Créer un rapport sur les conservations définies dans les cas eDiscovery </span><span class="sxs-lookup"><span data-stu-id="39901-103">Create a report on holds in eDiscovery cases</span></span>
  
<span data-ttu-id="39901-104">Le script de cet article permet aux administrateurs eDiscovery et aux gestionnaires eDiscovery de générer un rapport contenant des informations sur toutes les suspensions associées à des cas eDiscovery dans le centre de conformité dans Office 365 ou Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="39901-104">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the the compliance center in Office 365 or Microsoft 365.</span></span> <span data-ttu-id="39901-105">Le rapport contient des informations telles que le nom du cas dans lequel une conservation est associée, les emplacements de contenu placés en conservation et si la suspension est basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="39901-105">The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based.</span></span> <span data-ttu-id="39901-106">S’il existe des cas qui n’ont aucune conservation, le script crée un rapport supplémentaire avec une liste de cas sans conservation.</span><span class="sxs-lookup"><span data-stu-id="39901-106">If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="39901-107">Consultez la section [plus d’informations](#more-information) pour obtenir une description détaillée des informations incluses dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="39901-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span>
  
## <a name="admin-requirements-and-script-information"></a><span data-ttu-id="39901-108">Exigences en matière d’administration et informations sur les scripts</span><span class="sxs-lookup"><span data-stu-id="39901-108">Admin requirements and script information</span></span>

- <span data-ttu-id="39901-109">Pour générer un rapport sur tous les cas de découverte électronique dans votre organisation, vous devez être un administrateur de découverte électronique dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="39901-109">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization.</span></span> <span data-ttu-id="39901-110">Si vous êtes un gestionnaire eDiscovery, le rapport n’inclut que les informations sur les cas accessibles.</span><span class="sxs-lookup"><span data-stu-id="39901-110">If you are an eDiscovery Manager, the report will only include information about the cases that you can access.</span></span> <span data-ttu-id="39901-111">Pour plus d’informations sur les autorisations de découverte électronique, consultez la rubrique [attribution d’autorisations eDiscovery](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="39901-111">For more information about eDiscovery permissions, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="39901-112">Le script de cet article a une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="39901-112">The script in this article has minimal error handling.</span></span> <span data-ttu-id="39901-113">L’objectif principal est de créer rapidement un rapport sur les conservations associées aux cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="39901-113">The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="39901-114">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service.</span><span class="sxs-lookup"><span data-stu-id="39901-114">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="39901-115">The sample scripts are provided AS IS without warranty of any kind.</span><span class="sxs-lookup"><span data-stu-id="39901-115">The sample scripts are provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="39901-116">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span><span class="sxs-lookup"><span data-stu-id="39901-116">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="39901-117">The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.</span><span class="sxs-lookup"><span data-stu-id="39901-117">The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.</span></span> <span data-ttu-id="39901-118">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span><span class="sxs-lookup"><span data-stu-id="39901-118">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security--compliance-center-powershell"></a><span data-ttu-id="39901-119">Étape 1 : Connectez-vous au centre de sécurité & conformité PowerShell</span><span class="sxs-lookup"><span data-stu-id="39901-119">Step 1: Connect to the Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="39901-120">La première étape consiste à vous connecter à la sécurité & Centre de conformité PowerShell pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="39901-120">The first step is to connect to Security & Compliance Center PowerShell for your organization.</span></span> <span data-ttu-id="39901-121">Pour consulter des instructions détaillées, voir [Se connecter au Centre de sécurité et conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="39901-121">For step-by-step instructions, see [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
<span data-ttu-id="39901-122">Si votre compte Microsoft 365 utilise l’authentification multi-facteur (MFA) ou l’authentification fédérée, vous ne pouvez pas utiliser les instructions de la rubrique précédente pour vous connecter au Centre de sécurité et conformité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39901-122">If your Microsoft 365 account uses multi-factor authentication (MFA) or federated authentication, you can't use the instructions in the previous topic on connecting to Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="39901-123">Consultez plutôt les instructions de la rubrique [Se connecter au Centre de sécurité et conformité PowerShell à l’aide de l’authentification multi-facteur](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="39901-123">Instead, see the instructions in the topic [Connect to Security & Compliance Center PowerShell using multi-factor authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).</span></span>
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="39901-124">Étape 2 : exécuter le script pour signaler les suspensions associées à des cas de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="39901-124">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="39901-125">Une fois que vous êtes connecté à la sécurité & Centre de conformité PowerShell, l’étape suivante consiste à créer et exécuter le script qui collecte des informations sur les cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="39901-125">After you've connected to Security & Compliance Center PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="39901-126">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="39901-126">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
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

2. <span data-ttu-id="39901-127">Dans la session Windows PowerShell qui s’est ouverte à l’étape 1, accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="39901-127">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="39901-128">Exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="39901-128">Run the script; for example:</span></span>

    ```powershell
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="39901-129">Le script vous invite à entrer un dossier cible dans lequel enregistrer le rapport.</span><span class="sxs-lookup"><span data-stu-id="39901-129">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="39901-130">Tapez le chemin d’accès complet du dossier dans lequel le rapport doit être enregistré, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="39901-130">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="39901-131">Pour enregistrer le rapport dans le dossier dans lequel se trouve le script, tapez un point (« . ») lorsque vous êtes invité à indiquer un dossier cible.</span><span class="sxs-lookup"><span data-stu-id="39901-131">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder.</span></span> <span data-ttu-id="39901-132">Pour enregistrer le rapport dans un sous-dossier du dossier où se trouve le script, tapez simplement le nom du sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="39901-132">To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="39901-133">Le script commence à collecter des informations sur tous les cas de découverte électronique dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="39901-133">The script starts to collect information about all the eDiscovery cases in your organization.</span></span> <span data-ttu-id="39901-134">N’accédez pas au fichier de rapport pendant l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="39901-134">Don't access the report file while the script is running.</span></span> <span data-ttu-id="39901-135">Une fois le script terminé, un message de confirmation s’affiche dans la session Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39901-135">After the script is complete, a confirmation message is displayed in the Windows PowerShell session.</span></span> <span data-ttu-id="39901-136">Une fois ce message affiché, vous pouvez accéder au rapport dans le dossier que vous avez spécifié à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="39901-136">After this message is displayed, you can access the report in the folder that you specified in Step 4.</span></span> <span data-ttu-id="39901-137">Le nom de fichier du rapport est `CaseHoldsReport<DateTimeStamp>.csv` .</span><span class="sxs-lookup"><span data-stu-id="39901-137">The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="39901-138">Plus, le script crée également un rapport avec une liste de cas qui n’ont aucune conservation.</span><span class="sxs-lookup"><span data-stu-id="39901-138">Addtionally, the script also creates a report with a list of cases that don't have any holds.</span></span> <span data-ttu-id="39901-139">Le nom de fichier de ce rapport est `CaseswithNoHolds<DateTimeStamp>.csv` .</span><span class="sxs-lookup"><span data-stu-id="39901-139">The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="39901-140">Voici un exemple d’exécution du script CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="39901-140">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![Sortie après l’exécution du script CaseHoldsReport.ps1](../media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="39901-142">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="39901-142">More information</span></span>

<span data-ttu-id="39901-143">Le rapport de suspension de cas qui est créé lorsque vous exécutez le script dans cet article contient les informations suivantes sur chaque blocage.</span><span class="sxs-lookup"><span data-stu-id="39901-143">The case holds report that's created when you run the script in this article contains the following information about each hold.</span></span> <span data-ttu-id="39901-144">Comme expliqué précédemment, vous devez être un administrateur eDiscovery pour renvoyer des informations pour toutes les suspensions de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="39901-144">As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization.</span></span> <span data-ttu-id="39901-145">Pour plus d’informations sur les conservations d’incidents, consultez la rubrique [cas eDiscovery](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="39901-145">For more information about case holds, see [eDiscovery cases](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="39901-146">Nom de la conservation et nom du cas eDiscovery auquel la conservation est associée.</span><span class="sxs-lookup"><span data-stu-id="39901-146">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="39901-147">Indique si le cas de découverte électronique est actif ou fermé.</span><span class="sxs-lookup"><span data-stu-id="39901-147">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="39901-148">Indique si la conservation est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="39901-148">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="39901-149">Membres du cas eDiscovery auquel est associée la conservation.</span><span class="sxs-lookup"><span data-stu-id="39901-149">The members of the eDiscovery case that the hold is associated with.</span></span> <span data-ttu-id="39901-150">Les membres de cas peuvent afficher ou gérer un cas, en fonction des autorisations eDiscovery auxquelles ils ont été affectés.</span><span class="sxs-lookup"><span data-stu-id="39901-150">Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="39901-151">Date et heure de création de la demande de devis.</span><span class="sxs-lookup"><span data-stu-id="39901-151">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="39901-152">Si une demande de devis est fermée, la personne qui l’a fermée et l’heure et la date de clôture.</span><span class="sxs-lookup"><span data-stu-id="39901-152">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="39901-153">Les emplacements des boîtes aux lettres Exchange et des sites SharePoint en conservation.</span><span class="sxs-lookup"><span data-stu-id="39901-153">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="39901-154">Si la suspension est basée sur une requête, la syntaxe de requête.</span><span class="sxs-lookup"><span data-stu-id="39901-154">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="39901-155">L’heure et la date de création de la conservation et la personne qui l’a créée.</span><span class="sxs-lookup"><span data-stu-id="39901-155">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="39901-156">Date et heure de la dernière modification de la conservation et de la personne qui l’a modifiée.</span><span class="sxs-lookup"><span data-stu-id="39901-156">The time and date the hold was last changed and the person who changed it.</span></span>
