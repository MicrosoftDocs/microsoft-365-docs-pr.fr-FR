---
title: Utiliser un script PowerShell pour effectuer une recherche dans le journal d’audit
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom: seo-marvel-apr2020
description: Utilisez un script PowerShell, qui exécute la commande cmdlet Search-UnifiedAuditLog, pour effectuer des recherches dans le journal d’audit. Ce script est optimisé pour renvoyer des enregistrements d’audit de grande taille (jusqu’à 50 000). Le script exporte ces enregistrements dans un fichier CSV que vous pouvez afficher ou transformer à l’aide de Power Query dans Excel.
ms.openlocfilehash: d4fcf59297747d0499f6616438299ad8cbe96d7f
ms.sourcegitcommit: c0cfb9b354db56fdd329aec2a89a9b2cf160c4b0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "50094785"
---
# <a name="use-a-powershell-script-to-search-the-audit-log"></a><span data-ttu-id="665c9-105">Utiliser un script PowerShell pour effectuer une recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="665c9-105">Use a PowerShell script to search the audit log</span></span>

<span data-ttu-id="665c9-106">La sécurité, la conformité et l’audit sont désormais une priorité absolue pour les administrateurs informatiques du monde actuel.</span><span class="sxs-lookup"><span data-stu-id="665c9-106">Security, compliance, and auditing have become a top priority for IT administrators in today’s world.</span></span> <span data-ttu-id="665c9-107">Microsoft 365 offre plusieurs fonctionnalités intégrées pour aider les organisations à gérer la sécurité, la conformité et l’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-107">Microsoft 365 has several built-in capabilities to help organizations manage security, compliance, and auditing.</span></span> <span data-ttu-id="665c9-108">En particulier, la journalisation d’audit unifiée peut vous aider à examiner les incidents de sécurité et les problèmes de conformité.</span><span class="sxs-lookup"><span data-stu-id="665c9-108">In particular, unified audit logging can help you investigate security incidents and compliance issues.</span></span> <span data-ttu-id="665c9-109">Vous pouvez récupérer les journaux d’audit à l’aide des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="665c9-109">You can retrieve audit logs by using the following methods:</span></span>

- [<span data-ttu-id="665c9-110">L’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="665c9-110">The Office 365 Management Activity API</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)

- <span data-ttu-id="665c9-111">L’[outil de recherche dans le journal d’audit](search-the-audit-log-in-security-and-compliance.md) dans le Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="665c9-111">The [audit log search tool](search-the-audit-log-in-security-and-compliance.md) in the Microsoft 365 compliance center</span></span>

- <span data-ttu-id="665c9-112">La commande cmdlet [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-unifiedauditlog) dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="665c9-112">The [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-unifiedauditlog) cmdlet in Exchange Online PowerShell</span></span>

<span data-ttu-id="665c9-113">Si vous devez récupérer régulièrement les journaux d’audit, vous devez envisager une solution qui utilise l’API Activité de gestion Office 365, car elle peut offrir aux grandes organisations l’évolutivité et les performances nécessaires pour récupérer régulièrement des millions d’enregistrements d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-113">If you need to retrieve audit logs on a regular basis, you should consider a solution that uses the Office 365 Management Activity API because it that can provide large organizations with the scalability and performance to retrieve millions of audit records on an ongoing basis.</span></span> <span data-ttu-id="665c9-114">L'utilisation de l'outil de recherche du journal d'audit dans le Centre de conformité Microsoft 365 est un bon moyen de trouver rapidement les enregistrements d'audit pour des opérations spécifiques qui se produisent dans une plage de temps plus courte.</span><span class="sxs-lookup"><span data-stu-id="665c9-114">Using the audit log search tool in Microsoft 365 compliance center is a good way to quickly find audit records for specific operations that occur in shorter time range.</span></span> <span data-ttu-id="665c9-115">L’utilisation de plages de temps plus longues dans l’outil de recherche dans le journal d’audit, en particulier pour les grandes organisations, peut renvoyer trop d’enregistrements pour être facilement gérables ou exportés.</span><span class="sxs-lookup"><span data-stu-id="665c9-115">Using longer time ranges in the audit log search tool, especially for large organizations, might return too many records to easily manage or export.</span></span>

<span data-ttu-id="665c9-116">Lorsque vous devez récupérer manuellement des données d’audit pour une enquête ou un incident spécifique, en particulier pour les plages de dates plus longues dans les grandes organisations, il peut être préférable d’utiliser la commande cmdlet **Search-UnifiedAuditLog**.</span><span class="sxs-lookup"><span data-stu-id="665c9-116">When there are situations where you need to manually retrieve auditing data for a specific investigation or incident, particularly for longer date ranges in larger organizations, using the **Search-UnifiedAuditLog** cmdlet may be the best option.</span></span> <span data-ttu-id="665c9-117">Cet article inclut un script PowerShell qui utilise la commande cmdlet pour récupérer jusqu’à 50 000 enregistrements d’audit, puis les exporte dans un fichier CSV que vous pouvez mettre en forme à l’aide de Power Query dans Excel pour vous aider dans votre révision.</span><span class="sxs-lookup"><span data-stu-id="665c9-117">This article includes a PowerShell script that uses the cmdlet to retrieve up to 50,000 audit records and then export them to a CSV file that you can format using Power Query in Excel to help with your review.</span></span> <span data-ttu-id="665c9-118">L’utilisation du script décrit dans cet article réduit également le risque de délai d’utilisation des recherches importantes dans le journal d’audit dans le service.</span><span class="sxs-lookup"><span data-stu-id="665c9-118">Using the script in this article also minimizes the chance that large audit log searches will time out in the service.</span></span>

## <a name="before-you-run-the-script"></a><span data-ttu-id="665c9-119">Avant d’exécuter l’exemple de code :</span><span class="sxs-lookup"><span data-stu-id="665c9-119">Before you run the script</span></span>

- <span data-ttu-id="665c9-120">La journalisation d’audit doit être activée pour que votre organisation utilise le script pour renvoyer des enregistrements d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-120">Audit logging has to be enabled for your organization to successfully use the script to return audit records.</span></span> <span data-ttu-id="665c9-121">Nous activons par défaut la journalisation d’audit pour les organisations d’entreprise Microsoft 365 et Office 365.</span><span class="sxs-lookup"><span data-stu-id="665c9-121">Audit logging is turned on by default for Microsoft 365 and Office 365 enterprise organizations.</span></span> <span data-ttu-id="665c9-122">Pour vérifier que vous avez activé la recherche dans le journal d’audit pour votre organisation, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="665c9-122">To verify that audit log search is turned on for your organization, you can run the following command in Exchange Online PowerShell:</span></span>

  ```powershell
  Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
  ```
  
  <span data-ttu-id="665c9-123">La valeur `True` de la propriété **UnifiedAuditLogIn élémentsenabled** indique que vous avez activé la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-123">The value of `True` for the **UnifiedAuditLogIngestionEnabled** property indicates that audit log search is turned on.</span></span>

- <span data-ttu-id="665c9-124">Vous devez avoir le rôle Journaux d’audit en affichage seul ou Journaux d’audit dans Exchange Online pour exécuter correctement le script.</span><span class="sxs-lookup"><span data-stu-id="665c9-124">You have to be assigned the View-Only Audit Logs or Audit Logs role in Exchange Online to run successfully the script.</span></span> <span data-ttu-id="665c9-125">Par défaut, ces rôles sont affectés aux groupes de rôles Gestion de la conformité et Gestion de l’organisation sur la page Autorisations dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="665c9-125">By default, these roles are assigned to the Compliance Management and Organization Management role groups on the Permissions page in the Exchange admin center.</span></span> <span data-ttu-id="665c9-126">Pour plus d’informations, voir la section « Exigences pour effectuer une recherche dans le journal d’audit » dans [Effectuer des recherches dans le journal d’audit dans le Centre de conformité](search-the-audit-log-in-security-and-compliance.md#requirements-to-search-the-audit-log).</span><span class="sxs-lookup"><span data-stu-id="665c9-126">For more information, see the "Requirements to search the audit log" section in [Search the audit log in the compliance center](search-the-audit-log-in-security-and-compliance.md#requirements-to-search-the-audit-log).</span></span>

- <span data-ttu-id="665c9-127">La fin du script peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="665c9-127">It may take a long time for the script to complete.</span></span> <span data-ttu-id="665c9-128">Le temps d’exécuter dépend de la plage de dates et de la taille de l’intervalle pour laquelle vous configurez le script afin de récupérer les enregistrements d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-128">How long it takes to run depends on the date range and the size of the interval that you configure the script to retrieve audit records for.</span></span> <span data-ttu-id="665c9-129">Des plages de dates plus grandes et des intervalles plus petits entraînent une durée d’exécution longue.</span><span class="sxs-lookup"><span data-stu-id="665c9-129">Larger date ranges and smaller intervals will result in a long running time.</span></span> <span data-ttu-id="665c9-130">Pour plus d’informations sur la plage de dates et les intervalles, consultez le tableau de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="665c9-130">See the table in Step 2 for more information about the date range and intervals.</span></span>

- <span data-ttu-id="665c9-131">L’exemple de script fourni dans cet article n’est pas pris en charge par les services ou programmes d’assistance standard de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="665c9-131">The sample script provided in this article isn't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="665c9-132">L’exemple de script est fourni tel quel, sans garantie d’aucune sorte.</span><span class="sxs-lookup"><span data-stu-id="665c9-132">The sample script is provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="665c9-133">Microsoft Corporation décline aussi toute garantie implicite, y compris et sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier.</span><span class="sxs-lookup"><span data-stu-id="665c9-133">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="665c9-134">La totalité des risques découlant de l’utilisation ou de la performance de l’exemple de script et de la documentation repose sur vous.</span><span class="sxs-lookup"><span data-stu-id="665c9-134">The entire risk arising out of the use or performance of the sample script and documentation remains with you.</span></span> <span data-ttu-id="665c9-135">En aucun cas Microsoft, ses auteurs ou quiconque impliqué dans la création, la production ou la livraison de script ne sera responsable de tous dommages quels qu’ils soient (y compris, sans limitation, les dommages pour perte de profits, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser l’exemple de script ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="665c9-135">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the script be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample script or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-connect-to-exchange-online-powershell"></a><span data-ttu-id="665c9-136">Étape 1 : Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="665c9-136">Step 1: Connect to Exchange Online PowerShell</span></span>

<span data-ttu-id="665c9-137">La première étape consiste à se connecter à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="665c9-137">The first step is to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="665c9-138">Vous pouvez vous connecter à l’aide de l’authentification moderne ou de l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="665c9-138">You can connect using modern authentication or with multi-factor authentication (MFA).</span></span> <span data-ttu-id="665c9-139">Pour obtenir des instructions, consultez [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="665c9-139">For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

## <a name="step-2-modify-and-run-the-script-to-retrieve-audit-records"></a><span data-ttu-id="665c9-140">Étape 2 : modifier et exécuter le script pour récupérer les enregistrements d’audit</span><span class="sxs-lookup"><span data-stu-id="665c9-140">Step 2: Modify and run the script to retrieve audit records</span></span>

<span data-ttu-id="665c9-141">Une fois que vous êtes connecté à Exchange Online PowerShell, l’étape suivante consiste à créer, modifier et exécuter le script afin de récupérer les données d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-141">After you've connected to Exchange Online PowerShell, the next step is to create, modify, and run the script to retrieve the auditing data.</span></span> <span data-ttu-id="665c9-142">Les sept premières lignes du script de recherche dans le journal d’audit contiennent les variables suivantes que vous pouvez modifier pour configurer votre recherche.</span><span class="sxs-lookup"><span data-stu-id="665c9-142">The first seven lines in the audit log search script contain the following variables that you can modify to configure your search.</span></span> <span data-ttu-id="665c9-143">Consultez le tableau à l’étape 2 pour obtenir une description de ces variables.</span><span class="sxs-lookup"><span data-stu-id="665c9-143">See the table in step 2 for a description of these variables.</span></span>

1. <span data-ttu-id="665c9-144">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide du suffixe de nom de fichier .ps1.</span><span class="sxs-lookup"><span data-stu-id="665c9-144">Save the following text to a Windows PowerShell script by using a filename suffix of .ps1.</span></span> <span data-ttu-id="665c9-145">Par exemple, SearchAuditLog.ps1.</span><span class="sxs-lookup"><span data-stu-id="665c9-145">For example, SearchAuditLog.ps1.</span></span>

```powershell
#Modify the values for the following variables to configure the audit log search.
$logFile = "d:\AuditLogSearch\AuditLogSearchLog.txt"
$outputFile = "d:\AuditLogSearch\AuditLogRecords.csv"
[DateTime]$start = [DateTime]::UtcNow.AddDays(-1)
[DateTime]$end = [DateTime]::UtcNow
$record = "AzureActiveDirectory"
$resultSize = 5000
$intervalMinutes = 60

#Start script
[DateTime]$currentStart = $start
[DateTime]$currentEnd = $start

Function Write-LogFile ([String]$Message)
{
    $final = [DateTime]::Now.ToString("s") + ":" + $Message
    $final | Out-File $logFile -Append
}

Write-LogFile "BEGIN: Retrieving audit records between $($start) and $($end), RecordType=$record, PageSize=$resultSize."
Write-Host "Retrieving audit records for the date range between $($start) and $($end), RecordType=$record, ResultsSize=$resultSize"

$totalCount = 0
while ($true)
{
    $currentEnd = $currentStart.AddMinutes($intervalMinutes)
    if ($currentEnd -gt $end)
    {
        $currentEnd = $end
    }

    if ($currentStart -eq $currentEnd)
    {
        break
    }

    $sessionID = [DateTime]::Now.ToString("s")
    Write-LogFile "INFO: Retrieving audit records for activities performed between $($currentStart) and $($currentEnd)"
    Write-Host "Retrieving audit records for activities performed between $($currentStart) and $($currentEnd)"
    $currentCount = 0

    $sw = [Diagnostics.StopWatch]::StartNew()
    do
    {
        $results = Search-UnifiedAuditLog -StartDate $currentStart -EndDate $currentEnd -RecordType $record -SessionId $sessionID -SessionCommand ReturnLargeSet -ResultSize $resultSize

        if (($results | Measure-Object).Count -ne 0)
        {
            $results | export-csv -Path $outputFile -Append -NoTypeInformation

            $currentTotal = $results[0].ResultCount
            $totalCount += $results.Count
            $currentCount += $results.Count
            Write-LogFile "INFO: Retrieved $($currentCount) audit records out of the total $($currentTotal)"

            if ($currentTotal -eq $results[$results.Count - 1].ResultIndex)
            {
                $message = "INFO: Successfully retrieved $($currentTotal) audit records for the current time range. Moving on!"
                Write-LogFile $message
                Write-Host "Successfully retrieved $($currentTotal) audit records for the current time range. Moving on to the next interval." -foregroundColor Yellow
                ""
                break
            } 
        }
    }
    while (($results | Measure-Object).Count -ne 0)

    $currentStart = $currentEnd
}

Write-LogFile "END: Retrieving audit records between $($start) and $($end), RecordType=$record, PageSize=$resultSize, total count: $totalCount."
Write-Host "Script complete! Finished retrieving audit records for the date range between $($start) and $($end). Total count: $totalCount" -foregroundColor Green

```

2. <span data-ttu-id="665c9-146">Modifiez les variables répertoriées dans le tableau suivant pour configurer les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="665c9-146">Modify the variables listed in the following table to configure the search criteria.</span></span> <span data-ttu-id="665c9-147">Le script inclut des exemples de valeurs pour ces variables, mais vous devez les modifier (sauf indication contraire) pour répondre à vos exigences spécifiques.</span><span class="sxs-lookup"><span data-stu-id="665c9-147">The script includes sample values for these variables, but you should change them (unless stated otherwise) to meet your specific requirements.</span></span>

   |<span data-ttu-id="665c9-148">Variable</span><span class="sxs-lookup"><span data-stu-id="665c9-148">Variable</span></span>|<span data-ttu-id="665c9-149">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="665c9-149">Sample value</span></span>|<span data-ttu-id="665c9-150">Description</span><span class="sxs-lookup"><span data-stu-id="665c9-150">Description</span></span>|
   |---|---|---|
   |`$logFile`|<span data-ttu-id="665c9-151">"d:\temp\AuditSearchLog.txt"</span><span class="sxs-lookup"><span data-stu-id="665c9-151">"d:\temp\AuditSearchLog.txt"</span></span>|<span data-ttu-id="665c9-152">Indique le nom et l’emplacement du fichier journal qui contient des informations sur la progression de la recherche dans le journal d’audit effectuée par le script.</span><span class="sxs-lookup"><span data-stu-id="665c9-152">Specifies the name and location for the log file that contains information about the progress of the audit log search performed by the script.</span></span>|
   |`$outputFile`|<span data-ttu-id="665c9-153">"d:\temp\AuditRecords.csv"</span><span class="sxs-lookup"><span data-stu-id="665c9-153">"d:\temp\AuditRecords.csv"</span></span>|<span data-ttu-id="665c9-154">Indique le nom et l’emplacement du fichier CSV contenant les enregistrements d’audit renvoyés par le script.</span><span class="sxs-lookup"><span data-stu-id="665c9-154">Specifies the name and location of the CSV file that contains the audit records returned by the script.</span></span>|
   |<span data-ttu-id="665c9-155">`[DateTime]$start` et `[DateTime]$end`</span><span class="sxs-lookup"><span data-stu-id="665c9-155">`[DateTime]$start` and `[DateTime]$end`</span></span>|[DateTime]::UtcNow.AddDays(-1) <br/>[DateTime]::UtcNow|<span data-ttu-id="665c9-158">Spécifie la plage de dates pour la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-158">Specifies the date range for the audit log search.</span></span> <span data-ttu-id="665c9-159">Le script retourne les enregistrements des activités d’audit qui se sont produites dans la plage de dates spécifiée.</span><span class="sxs-lookup"><span data-stu-id="665c9-159">The script will return records for audit activities that occurred within the specified date range.</span></span> <span data-ttu-id="665c9-160">Par exemple, pour renvoyer les activités effectuées en janvier 2021, vous pouvez utiliser une date de début de `"2021-01-01"` et une date de fin de `"2021-01-31"` (n’oubliez pas d’entourer les valeurs de guillemets doubles) La valeur d’exemple dans le script renvoie les enregistrements des activités effectuées au cours des 24 heures précédentes.</span><span class="sxs-lookup"><span data-stu-id="665c9-160">For example, to return activities performed in January 2021, you can use a start date of `"2021-01-01"` and an end date of `"2021-01-31"` (be sure to surround the values in double-quotation marks) The sample value in the script returns records for activities performed in the previous 24 hours.</span></span> <span data-ttu-id="665c9-161">si vous n’incluez pas d’horodatage dans la valeur, l’horodatage par défaut est 00:00 (minuit) pour la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="665c9-161">If you don't include a timestamp in the value, the default timestamp is 12:00 AM (midnight) on the specified date.</span></span>|
   |`$record`|<span data-ttu-id="665c9-162">« AzureActiveDirectory »</span><span class="sxs-lookup"><span data-stu-id="665c9-162">"AzureActiveDirectory"</span></span>|<span data-ttu-id="665c9-163">Spécifie le type d’enregistrement des activités d’audit (également *opérations*) à rechercher.</span><span class="sxs-lookup"><span data-stu-id="665c9-163">Specifies the record type of the audit activities (also called *operations*) to search for.</span></span> <span data-ttu-id="665c9-164">Cette propriété indique le service ou la fonctionnalité dans qui une activité a été déclenchée.</span><span class="sxs-lookup"><span data-stu-id="665c9-164">This property indicates the service or feature that an activity was triggered in.</span></span> <span data-ttu-id="665c9-165">Pour obtenir la liste des types d’enregistrement que vous pouvez utiliser pour cette variable, consultez [Type d’enregistrement journal d’audit](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#auditlogrecordtype).</span><span class="sxs-lookup"><span data-stu-id="665c9-165">For a list of record types that you can use for this variable, see [Audit log record type](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#auditlogrecordtype).</span></span> <span data-ttu-id="665c9-166">Vous pouvez utiliser le nom du type d’enregistrement ou la valeur ENUM.</span><span class="sxs-lookup"><span data-stu-id="665c9-166">You can use the record type name or ENUM value.</span></span> <br/><br/><span data-ttu-id="665c9-167">**Conseil :** pour renvoyer les enregistrements d'audit pour tous les types d'enregistrements, utilisez la valeur `$null` (sans guillemets doubles).</span><span class="sxs-lookup"><span data-stu-id="665c9-167">**Tip:** To return audit records for all record types, use the value `$null` (without double-quotations marks).</span></span>|
   |`$resultSize`|<span data-ttu-id="665c9-168">5000</span><span class="sxs-lookup"><span data-stu-id="665c9-168">5000</span></span>|<span data-ttu-id="665c9-169">Spécifie le nombre de résultats renvoyés chaque fois que la commande cmdlet **Search-UnifiedAuditLog** est appelée par le script (appelé *jeu de résultats*).</span><span class="sxs-lookup"><span data-stu-id="665c9-169">Specifies the number of results returned each time the **Search-UnifiedAuditLog** cmdlet is called by the script (called a *result set*).</span></span> <span data-ttu-id="665c9-170">La valeur de 5 000 est la valeur maximale prise en charge par la commande cmdlet.</span><span class="sxs-lookup"><span data-stu-id="665c9-170">The value of 5,000 is the maximum value supported by the cmdlet.</span></span> <span data-ttu-id="665c9-171">Laissez cette valeur telle qu’elle est.</span><span class="sxs-lookup"><span data-stu-id="665c9-171">Leave this value as-is.</span></span>|
   |`$intervalMinutes`|<span data-ttu-id="665c9-172">60</span><span class="sxs-lookup"><span data-stu-id="665c9-172">60</span></span>|<span data-ttu-id="665c9-173">Pour dépasser la limite de 5 000 enregistrements renvoyés, cette variable prend la plage de données que vous avez spécifiée et la découpe en intervalles de temps plus courts.</span><span class="sxs-lookup"><span data-stu-id="665c9-173">To help overcome the limit of 5000 records returned, this variable takes the data range you specified and slices it up into smaller time intervals.</span></span> <span data-ttu-id="665c9-174">Chaque intervalle, et non la plage de dates entière, est soumis à la limite de sortie de l’enregistrement de 5 000 de la commande.</span><span class="sxs-lookup"><span data-stu-id="665c9-174">Now each interval, not the entire date range, is subject to the 5000 record output limit of the command.</span></span> <span data-ttu-id="665c9-175">La valeur par défaut de 5 000 enregistrements par intervalle de 60 minutes dans la plage de dates doit être suffisante pour la plupart des organisations.</span><span class="sxs-lookup"><span data-stu-id="665c9-175">The default value of 5000 records per 60-minute interval within the date range should be sufficient for most organizations.</span></span> <span data-ttu-id="665c9-176">Toutefois, si le script renvoie une erreur qui indique `maximum results limitation reached`, diminuez l’intervalle de temps (par exemple, à 30 minutes, voire 15 minutes) et réexécutez le script.</span><span class="sxs-lookup"><span data-stu-id="665c9-176">But, if the script returns an error that says, `maximum results limitation reached`, decrease the time interval (for example, to 30 minutes or even 15 minutes) and rerun the script.</span></span>|
   ||||

   <span data-ttu-id="665c9-177">La plupart des variables répertoriées dans le tableau précédent correspondent aux paramètres de la commande cmdlet **Search-UnifiedAuditLog**.</span><span class="sxs-lookup"><span data-stu-id="665c9-177">Most of the variables listed in the previous table correspond to parameters for the **Search-UnifiedAuditLog** cmdlet.</span></span> <span data-ttu-id="665c9-178">Pour plus d'informations sur ces paramètres, voir [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-unifiedauditlog).</span><span class="sxs-lookup"><span data-stu-id="665c9-178">For more information about these parameters, see [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-unifiedauditlog).</span></span>

3. <span data-ttu-id="665c9-179">Sur votre ordinateur local, ouvrez Windows PowerShell et allez dans le dossier dans lequel vous avez enregistré le script modifié.</span><span class="sxs-lookup"><span data-stu-id="665c9-179">On your local computer, open Windows PowerShell and go to the folder where you saved the modified script.</span></span>

4. <span data-ttu-id="665c9-180">Dans Exchange Online PowerShell, exécutez le script suivant par exemple :</span><span class="sxs-lookup"><span data-stu-id="665c9-180">Run the script in Exchange Online PowerShell; for example:</span></span>

   ```powershell
   .\SearchAuditLog.ps1
   ```

<span data-ttu-id="665c9-181">Le script affiche les messages de progression pendant son exécution.</span><span class="sxs-lookup"><span data-stu-id="665c9-181">The script displays progress messages while it's running.</span></span> <span data-ttu-id="665c9-182">Une fois l’exécution du script terminée, il crée le fichier journal et le fichier CSV qui contient les enregistrements d’audit et les enregistre dans les dossiers définis par les variables `$logFile` et `$outputFile`.</span><span class="sxs-lookup"><span data-stu-id="665c9-182">After the script is finished running, it creates the log file and the CSV file that contains the audit records and saves them to the folders defined by the `$logFile` and `$outputFile` variables.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="665c9-183">Il existe une limite de 50 000 pour le nombre maximal d’enregistrements d’audit renvoyés chaque fois que vous exécutez ce script.</span><span class="sxs-lookup"><span data-stu-id="665c9-183">There is a 50,000 limit for the maximum number of audit records returned each time you run this script.</span></span> <span data-ttu-id="665c9-184">Si vous exécutez ce script et qu’il renvoie 50 000 résultats, il est probable que les enregistrements d’audit pour les activités qui se sont produites dans la plage de dates n’ont pas été inclus.</span><span class="sxs-lookup"><span data-stu-id="665c9-184">If you run this script and it returns 50,000 results, then it's likely that audit records for activities that occurred within the date range weren't included.</span></span> <span data-ttu-id="665c9-185">Dans ce cas, nous vous recommandons de diviser la plage de dates en plus petites durées, puis de réexécuter le script pour chaque plage de dates.</span><span class="sxs-lookup"><span data-stu-id="665c9-185">If this happens, we recommend that you divide the date range into smaller durations and then rerun the script for each date range.</span></span> <span data-ttu-id="665c9-186">Par exemple, si une plage de dates de 90 jours renvoie 50 000 résultats, vous pouvez réexécuter le script deux fois, une fois pour les 45 premiers jours de la plage de dates, puis de nouveau pour les 45 prochains jours.</span><span class="sxs-lookup"><span data-stu-id="665c9-186">For example, if a date range of 90 days returns 50,000 results then you can rerun the script twice, once for the first 45 days in the date range and then again for the next 45 days.</span></span>

## <a name="step-3-format-and-view-the-audit-records"></a><span data-ttu-id="665c9-187">Étape 3 : formater et afficher les enregistrements d’audit</span><span class="sxs-lookup"><span data-stu-id="665c9-187">Step 3: Format and view the audit records</span></span>

<span data-ttu-id="665c9-188">Après avoir exécuté le script et exporté les enregistrements d’audit dans un fichier CSV, vous souhaitez peut-être mettre en forme le fichier CSV afin de faciliter l’examen et l’analyse des enregistrements d’audit.</span><span class="sxs-lookup"><span data-stu-id="665c9-188">After you've run the script and exported the audit records to a CSV file, you may want to format the CSV to make easier to review and analyze the audit records.</span></span> <span data-ttu-id="665c9-189">Une des façons de cela consiste à transformer JavaScript Object Notation Power Query dans Excel pour fractionner chaque propriété de l’objet JSON dans la colonne **AuditData** dans sa propre colonne.</span><span class="sxs-lookup"><span data-stu-id="665c9-189">One way to do this is to the Power Query JSON transform feature in Excel to split each property in the JSON object in the **AuditData** column into its own column.</span></span> <span data-ttu-id="665c9-190">Pour obtenir des instructions détaillées, consultez « Étape 2 : mise en forme du journal d’audit exporté à l’aide de l’Éditeur Power Query » dans [Exporter, configurer et afficher des enregistrements du journal d’audit](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor).</span><span class="sxs-lookup"><span data-stu-id="665c9-190">For step-by-step instructions, see "Step 2: Format the exported audit log using the Power Query Editor" in [Export, configure, and view audit log records](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor).</span></span>
