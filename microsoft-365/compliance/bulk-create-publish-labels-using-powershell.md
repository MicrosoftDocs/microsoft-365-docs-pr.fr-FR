---
title: Création et publication en bloc d’étiquettes de rétention à l’aide de PowerShell
ms.author: laurawi
author: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
- SPO_Content
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: Dans Office 365, vous pouvez utiliser des étiquettes de rétention pour implémenter une planification de rétention pour votre organisation. En tant que gestionnaire des enregistrements ou responsable de la mise en conformité, vous avez peut-être des centaines d’étiquettes de rétention à créer et à publier. Vous pouvez le faire via l’interface utilisateur dans le Centre de sécurité et conformité, mais créer des étiquettes de rétention une à une est chronophage et inefficace. En utilisant le script et les fichiers .csv fournis ci-dessous, vous pouvez créer et publier en bloc des étiquettes de rétention et des stratégies d’étiquette de rétention. Commencez par créer une liste des étiquettes de rétention et une liste des stratégies d’étiquette de rétention dans Excel, puis créez les étiquettes de rétention et les stratégies d’étiquette de rétention en bloc dans ces listes à l’aide de PowerShell. Cette méthode vous permet de créer et de publier en une fois toutes les étiquettes de rétention nécessaires pour votre planification de rétention.
ms.openlocfilehash: 2be7c2251a3a35f32ff9754134cca1f5958b447a
ms.sourcegitcommit: 1c962bd0d51dc12419c4e6e393bb734c972b7e38
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "38708090"
---
# <a name="bulk-create-and-publish-retention-labels-by-using-powershell"></a><span data-ttu-id="575b5-108">Création et publication en bloc d’étiquettes de rétention à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="575b5-108">Bulk create and publish retention labels by using PowerShell</span></span>

<span data-ttu-id="575b5-p102">Dans Office 365, vous pouvez utiliser des étiquettes de rétention pour implémenter une planification de rétention pour votre organisation. En tant que gestionnaire des enregistrements ou responsable de la mise en conformité, vous avez peut-être des centaines d’étiquettes de rétention à créer et à publier. Vous pouvez le faire via l’interface utilisateur dans le Centre de sécurité et de conformité, mais créer des étiquettes de rétention une à une est chronophage et inefficace.</span><span class="sxs-lookup"><span data-stu-id="575b5-p102">In Office 365, you can use retention labels to implement a retention schedule for your organization. As a record manager or compliance officer, you might have hundreds of retention labels to create and publish. You can do this through the UI in the Security &amp; Compliance Center, but creating retention labels one at a time is time-consuming and inefficient.</span></span>
  
<span data-ttu-id="575b5-p103">En utilisant le script et les fichiers .csv fournis ci-dessous, vous pouvez créer et publier en bloc des étiquettes de rétention et des stratégies d’étiquette de rétention. Commencez par créer une liste des étiquettes de rétention et une liste des stratégies d’étiquette de rétention dans Excel, puis créez les étiquettes de rétention et les stratégies d’étiquette de rétention en bloc dans ces listes à l’aide de PowerShell. Cette méthode vous permet de créer et de publier en une fois toutes les étiquettes de rétention nécessaires pour votre planification de rétention.</span><span class="sxs-lookup"><span data-stu-id="575b5-p103">By using the script and .csv files provided below, you can bulk create retention labels and publish retention label policies. First you create a list of the retention labels and a list of the retention label policies in Excel, and then you bulk create the retention labels and retention label policies in those lists by using PowerShell. This makes it easier to create and publish at one time, all of the retention labels that your retention schedule requires.</span></span>
  
<span data-ttu-id="575b5-115">Pour en savoir plus sur les étiquettes de rétention, consultez l’article [Vue d’ensemble des étiquettes de rétention](labels.md).</span><span class="sxs-lookup"><span data-stu-id="575b5-115">For more information about retention labels, see [Overview of labels](labels.md).</span></span>
  
## <a name="disclaimer"></a><span data-ttu-id="575b5-116">Clause d’exclusion</span><span class="sxs-lookup"><span data-stu-id="575b5-116">Disclaimer</span></span>

<span data-ttu-id="575b5-p104">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="575b5-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-create-a-csv-file-for-creating-the-retention-labels"></a><span data-ttu-id="575b5-122">Étape 1 : créer un fichier .csv pour créer les étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="575b5-122">Step 1: Create a .csv file for creating the retention labels</span></span>

<span data-ttu-id="575b5-p105">Tout d’abord, créez un fichier .csv qui contient une liste de vos étiquettes de rétention avec leurs paramètres. Pour utiliser l’exemple ci-dessous en tant que modèle, copiez-le dans Excel, convertissez le texte en colonnes (dans Excel \> onglet **Données** \> **Texte en colonnes** \> **Délimité** \> **Virgule** \> **Général**), puis enregistrez la feuille de calcul dans un fichier .csv à un emplacement facile à trouver.</span><span class="sxs-lookup"><span data-stu-id="575b5-p105">First you create a .csv file that contains a list of your retention labels with their settings. You can use the sample below as a template by copying it into Excel, converting the text to columns (in Excel \> **Data** tab \> **Text to Columns** \> **Delimited** \> **Comma** \> **General**), and then saving the worksheet as a .csv file in a location that's easy to find.</span></span>
  
<span data-ttu-id="575b5-125">Pour en savoir plus sur les valeurs de paramètre pour cette cmdlet, consultez l’article [New-ComplianceTag](https://go.microsoft.com/fwlink/?linkid=866511).</span><span class="sxs-lookup"><span data-stu-id="575b5-125">For more information about the parameter values for this cmdlet, see [New-ComplianceTag](https://go.microsoft.com/fwlink/?linkid=866511).</span></span>
  
<span data-ttu-id="575b5-126">Remarques :</span><span class="sxs-lookup"><span data-stu-id="575b5-126">Notes:</span></span>
  
- <span data-ttu-id="575b5-127">Si vous ne fournissez aucun fichier source pour la création d’étiquettes de rétention, le script se poursuit et vous invite à identifier le fichier source pour la publication des étiquettes de rétention (voir la section suivante), puis le script publie uniquement les étiquettes de rétention existantes.</span><span class="sxs-lookup"><span data-stu-id="575b5-127">If you don't provide a source file for creating retention labels, the script moves on and prompts you for the source file for publishing retention labels (see the next section), and the script will publish only existing retention labels.</span></span>
    
- <span data-ttu-id="575b5-p106">Si le fichier .csv contient une étiquette de rétention portant le même nom qu’une étiquette de rétention existante, le script ignore la création de cette étiquette de rétention. Aucune étiquette de rétention en double n’est créée.</span><span class="sxs-lookup"><span data-stu-id="575b5-p106">If the .csv file contains a retention label with the same name as one that already exists, the script skips creating that retention label. No duplicate retention labels are created.</span></span>
    
- <span data-ttu-id="575b5-p107">Si vous modifiez ou renommez les en-têtes de colonne, le script échoue. Le script nécessite un fichier .csv au format fourni ici.</span><span class="sxs-lookup"><span data-stu-id="575b5-p107">If you change or rename the column headers, the script will fail. The script requires a .csv file in the format provided here.</span></span>
    
### <a name="sample-csv-file"></a><span data-ttu-id="575b5-132">Exemple de fichier .csv</span><span class="sxs-lookup"><span data-stu-id="575b5-132">Sample .csv file</span></span>

```
Name (Required),Comment (Optional),IsRecordLabel (Required),RetentionAction (Optional),RetentionDuration (Optional),RetentionType (Optional),ReviewerEmail (Optional)
LabelName_t_1,Record - keep and delete - 2 years,$true,KeepAndDelete,730,CreationAgeInDays,
LabelName_t_2,Keep and delete tag - 7 years,$false,KeepAndDelete,2555,ModificationAgeInDays,
LabelName_t_3,5 year delete,$false,Delete,1825,TaggedAgeInDays,
LabelName_t_4,Record label tag - financial,$true,Keep,730,CreationAgeInDays,
```

## <a name="step-2-create-a-csv-file-for-publishing-the-labels"></a><span data-ttu-id="575b5-133">Étape 2 : créer un fichier .csv pour la publication des étiquettes</span><span class="sxs-lookup"><span data-stu-id="575b5-133">Step 2: Create a .csv file for publishing the labels</span></span>

<span data-ttu-id="575b5-p108">Ensuite, créez un fichier .csv contenant une liste des stratégies d’étiquette de rétention avec leurs emplacements et d’autres paramètres. Pour utiliser l’exemple ci-dessous en tant que modèle, copiez-le dans Excel, convertissez le texte en colonnes (dans Excel \> onglet **Données** \> **Texte en colonnes** \> **Délimité** \> **Virgule** \> **Général**), puis enregistrez la feuille de calcul dans un fichier .csv à un emplacement facile à trouver.</span><span class="sxs-lookup"><span data-stu-id="575b5-p108">Next you create a .csv file that contains a list of retention label policies with their locations and other settings. You can use the sample below as a template by copying it into Excel, converting the text to columns (in Excel \> **Data** tab \> **Text to Columns** \> **Delimited** \> **Comma** \> **General**), and then saving the worksheet as a .csv file in a location that's easy to find.</span></span>
  
<span data-ttu-id="575b5-136">Pour en savoir plus sur les valeurs de paramètre pour cette cmdlet, consultez l’article [New-RetentionCompliancePolicy](https://go.microsoft.com/fwlink/?linkid=866512).</span><span class="sxs-lookup"><span data-stu-id="575b5-136">For more information about the parameter values for this cmdlet, see [New-RetentionCompliancePolicy](https://go.microsoft.com/fwlink/?linkid=866512).</span></span>
  
<span data-ttu-id="575b5-137">Remarques :</span><span class="sxs-lookup"><span data-stu-id="575b5-137">Notes:</span></span>
  
- <span data-ttu-id="575b5-138">Si vous ne fournissez aucun fichier source pour la publication des étiquettes de rétention, le script crée des étiquettes de rétention (voir la section précédente), mais ne les publie pas.</span><span class="sxs-lookup"><span data-stu-id="575b5-138">If you don't provide a source file for publishing retention labels, the script creates retention labels (see the previous section) but does not publish them.</span></span>
    
- <span data-ttu-id="575b5-p109">Si le fichier .csv contient une stratégie d’étiquette de rétention portant le même nom qu’une stratégie existante, le script ignore la création de cette stratégie d’étiquette de rétention. Aucune stratégie d’étiquette de rétention en double n’est créée.</span><span class="sxs-lookup"><span data-stu-id="575b5-p109">If the .csv file contains a retention label policy with the same name as one that already exists, the script skips creating that retention label policy. No duplicate retention label policies are created.</span></span>
    
- <span data-ttu-id="575b5-p110">Le script publie uniquement les étiquettes de rétention appliquées manuellement au contenu. Il ne prend pas en charge les étiquettes de rétention appliquées automatiquement au contenu.</span><span class="sxs-lookup"><span data-stu-id="575b5-p110">The script publishes only retention labels that are applied manually to content. This script does not support retention labels that are auto-applied to content.</span></span>
    
- <span data-ttu-id="575b5-p111">Si vous modifiez ou renommez les en-têtes de colonne, le script échoue. Le script nécessite un fichier .csv au format fourni ici.</span><span class="sxs-lookup"><span data-stu-id="575b5-p111">If you change or rename the column headers, the script will fail. The script requires a .csv file in the format provided here.</span></span>
    
### <a name="sample-csv-file"></a><span data-ttu-id="575b5-145">Exemple de fichier .csv</span><span class="sxs-lookup"><span data-stu-id="575b5-145">Sample .csv file</span></span>

```
Policy Name (Required),PublishComplianceTag (Required),Comment (Optional),Enabled (Required),ExchangeLocation (Optional),ExchangeLocationException (Optional),ModernGroupLocation (Optional),ModernGroupLocationException (Optional),OneDriveLocation (Optional),OneDriveLocationException (Optional),PublicFolderLocation (Optional),SharePointLocation (Optional),SharePointLocationException (Optional),SkypeLocation (Optional),SkypeLocationException (Optional)
Publishing Policy Red1,"LabelName_t_1, LabelName_t_2, LabelName_t_3, LabelName_t_4",N/A,$true,All,,All,,All,,,All,,,
Publishing Policy Orange1,"LabelName_t_1, LabelName_t_2",N/A,$true,All,,,,,,,,,,
Publishing Policy Yellow1,"LabelName_t_3, LabelName_t_4",N/A,$false,All,,,,,,,,,,
```

## <a name="step-3-create-the-powershell-script"></a><span data-ttu-id="575b5-146">Étape 3 : créer le script PowerShell</span><span class="sxs-lookup"><span data-stu-id="575b5-146">Step 3: Create the PowerShell script</span></span>

<span data-ttu-id="575b5-p112">Copiez et collez le script PowerShell indiqué ci-dessous dans le Bloc-notes. Enregistrez le fichier en utilisant le suffixe de nom de fichier .ps1 à un emplacement facile à trouver, par exemple \<path\>CreateRetentionSchedule.ps1.</span><span class="sxs-lookup"><span data-stu-id="575b5-p112">Copy and paste the below PowerShell script into Notepad. Save the file by using a filename suffix of .ps1 in a location that's easy to find -- for example, \<path\>CreateRetentionSchedule.ps1.</span></span>
  
### <a name="powershell-script"></a><span data-ttu-id="575b5-149">Script PowerShell</span><span class="sxs-lookup"><span data-stu-id="575b5-149">PowerShell script</span></span>

```
<#
. Steps: Import and Publish Compliance Tag
    ○ Load compliance tag csv file 
    ○ Validate csv file input
    ○ Create compliance tag
    ○ Create compliance policy
    ○ Publish compliance tag for the policy
    ○ Generate the log for tags creation
    ○ Generate the csv result for the tags created and published
. Syntax
    .\Publish-ComplianceTag.ps1 [-LabelListCSV <string>] [-PolicyListCSV <string>] 
. Detailed Description
    1) [-LabelListCSV <string>]
    -LabelListCSV ".\SampleInputFile_LabelList.csv"
    Load compliance tag for creation.
    2) [-PolicyListCSV <string>]
    -PolicyListCSV ".\SampleInputFile_PolicyList.csv"
    Load compliance tag for creation.
#>
param (
    [Parameter(Mandatory = $true)]
    [string]$LabelListCSV = "",
    [Parameter(Mandatory = $true)]
    [string]$PolicyListCSV = "",
    [Switch]$ResultCSV
)
# -------------------
# File operation
# -------------------
Function FileExist
{
    Param(
        # File path needed to check
        [Parameter(Mandatory = $true)]
        [String]$FilePath,
        [Switch]$Warning
    )
    $inputFileExist = Test-Path $FilePath
    if (!$inputFileExist)
    {
        if ($Warning -eq $false) 
        { 
            WriteToLog -Type "Failed" -Message "[File: $FilePath] The file doesn't exist"
            throw 
        }
        else 
        { 
            WriteToLog -Type "Warning" -Message "[File: $FilePath] The file doesn't exist"
        }
    }
    else
    {
        WriteToLog -Type "Succeed" -Message "[File: $FilePath] The file is found"
    }
}
# -------------------
# Log operation
# -------------------
Function WriteToLog
{
    Param(
        # Message want to write to log file
        [Parameter(Mandatory = $true)]
        [String]$Message,
        # "Succeed" or "Faild"
        [String]$Type = "Message"
    )
    $date = Get-Date -Format 'HH:mm:ss'
    $logInfo = $date + " - [$Type] " + $Message
    $logInfo | Out-File -FilePath $logfilePath -Append
    if ($Type -eq "Succeed") { Write-Host $logInfo -ForegroundColor Green }
    elseif ($Type -eq "Failed") { Write-Host $logInfo -ForegroundColor Red }
    elseif ($Type -eq "Warning") { Write-Host $logInfo -ForegroundColor Yellow }
    elseif ($Type -eq "Start") { Write-Host $logInfo -ForegroundColor Cyan }
    else { Write-Verbose $logInfo }
}
Function Create-Log
{
    Param(
        # Log folder Root
        [Parameter(Mandatory = $true)]
        [String]$LogFolderRoot,
        # The function Log file for
        [Parameter(Mandatory = $true)]
        [String]$LogFunction
    )
    $logFolderPath = "$LogFolderRoot\logfiles"
    $folderExist = Test-Path "$logFolderPath"
    if (!$folderExist)
    {
        $folder = New-Item "$logFolderPath" -type directory
    }
    $date = Get-Date -Format 'MMddyyyy_HHmmss'
    $logfilePath = "$logFolderPath\Log_{0}_{1}.txt" -f $LogFunction, $date
    Write-Verbose "Log file is writen to: $logfilePath"
    $logfile = New-Item $logfilePath  -type file
    return $logfilePath
}
Function Create-ResultCSV
{
    Param(
        # Result folder Root
        [Parameter(Mandatory = $true)]
        [String]$ResultFolderRoot,
        # The function Result file for
        [Parameter(Mandatory = $true)]
        [String]$ResultFunction
    )
    $retFolderPath = "$ResultFolderRoot\logfiles"
    $folderExist = Test-Path "$retFolderPath"
    if (!$folderExist)
    {
        $folder = New-Item "$retFolderPath" -type directory
    }
    $date = Get-Date -Format 'MMddyyyy_HHmmss'
    $retfilePath = "$retFolderPath\Result_{0}_{1}.csv" -f $ResultFunction, $date
    Write-Verbose "Result file is writen to: $retfilePath"
    $retfile = New-Item $retfilePath  -type file
    return $retfilePath
}
# -------------------
# Prepare Log File
# -------------------
$scriptPath = '.\'
$logfilePath = Create-Log -LogFolderRoot $scriptPath -LogFunction "Publish_Compliance_Tag"
if ($ResultCSV)
{
    $tagRetFile = Create-ResultCSV -ResultFolderRoot $scriptPath -ResultFunction "Tag_Creation"
    $tagPubRetFile = Create-ResultCSV -ResultFolderRoot $scriptPath -ResultFunction "Tag_Publish"
}
# -------------------
# Invoke Powershell cmdlet
# -------------------
Function InvokePowerShellCmdlet
{
    Param(
        [Parameter(Mandatory = $true)]
        [String]$CmdLet
    )
    try
    {
        WriteToLog -Type "Start" -Message "Execute Cmdlet : '$CmdLet'" 
        return Invoke-Expression $CmdLet -ErrorAction SilentlyContinue
    }
    catch
    {
        WriteToLog -Type "Failed" "Failed to execute cmdlet!"
        WriteToLog -Type "Failed" $error[0]
        return $null
    }
}
# -------------------
# Create Compliance Tag
# -------------------
Function CreateComplianceTag
{
    Param(
        # File path needed to check
        [Parameter(Mandatory = $true)]
        [String]$FilePath
    )
    
    WriteToLog -Type "Start" "Start to create Compliance Tag"
    FileExist $FilePath
    
    # TODO Validate CSV file for the Header
    try
    {
        # Import csv
        $labels = Import-Csv $FilePath
        # Retrieve existing compliance tags
        $tags = InvokePowerShellCmdlet "Get-ComplianceTag"
        foreach($lab in $labels)
        {
            # Cmdlet parameters
            $para = [String]::Empty;
            $name = [String]::Empty;
            $cmdlet = 'New-ComplianceTag'
            if ([String]::IsNullOrEmpty($lab.'Name (Required)'))
            {
                WriteToLog -Type "Failed" -Message "Could not acquire table for writing."
                throw;
            }
            else
            {
                $name = $lab.'Name (Required)'
                $cmdlet += " -Name '" + $name + "'"
            }
            if (![String]::IsNullOrEmpty($lab.'Comment (Optional)'))
            {
                $para = $lab.'Comment (Optional)'
                $cmdlet += " -Comment '" + $para + "'"
            }
            if (![String]::IsNullOrEmpty($lab.'IsRecordLabel (Required)'))
            {
                $para = $lab.'IsRecordLabel (Required)'
                $cmdlet += " -IsRecordLabel " + $para
            }
            if (![String]::IsNullOrEmpty($lab.'RetentionAction (Optional)'))
            {
                $para = $lab.'RetentionAction (Optional)'
                $cmdlet += " -RetentionAction " + $para 
            }
            if (![String]::IsNullOrEmpty($lab.'RetentionDuration (Optional)'))
            {
                $para = $lab.'RetentionDuration (Optional)'
                $cmdlet += " -RetentionDuration " + $para
            }
            if (![String]::IsNullOrEmpty($lab.'RetentionType (Optional)'))
            {
                $para = $lab.'RetentionType (Optional)'
                $cmdlet += " -RetentionType " + $para
            }
            if (![String]::IsNullOrEmpty($lab.'ReviewerEmail (Optional)'))
            {
                $emails = $lab.'ReviewerEmail (Optional)'.Split(",") | ForEach-Object { $_.Trim() }
                if (($emails -ne $null) -and ($emails.Count -ne 0))
                {
                    $eml = '@('
                    foreach($email in $emails)
                    {
                        $eml += "'{0}'," -f $email
                    }
                    $eml = $eml.Substring(0, $eml.Length - 1) + ')'
                    
                    $cmdlet += " -ReviewerEmail " + $eml
                }
            }
            # If the tag already exists, skip for creation
            if (($tags -eq $null) -or ($tags | ? { $_.Name.ToLower() -eq $name.ToLower() }) -eq $null)
            {
                # Create compliance tag
                $msg = "Execute Cmdlet : {0}" -f $cmdlet
                
                $ret = InvokePowerShellCmdlet $cmdlet
            
                if ($ret -eq $null)
                {
                    WriteToLog -Type "Failed" $error[0]
                    break;
                }
            }
            else
            {
                WriteToLog -Type "Warning" -Message "The tag '$name' already exists! Skip for creation!"
            }
        }
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in input"
    }
}
# -------------------
# Create Retention Compliance Policy
# -------------------
Function CreateRetentionCompliancePolicy
{
    Param(
        # File path needed to check
        [Parameter(Mandatory = $true)]
        [String]$FilePath
    )
    
    WriteToLog -Type "Start" "Start to Create Retention Policy"
    FileExist $FilePath
    try
    {
        # Import csv
        $list = Import-Csv -Path $FilePath
        # Retrieve existing retention compliance policy
        $policies = InvokePowerShellCmdlet "Get-RetentionCompliancePolicy"
        foreach($rp in $list)
        {
            # Cmdlet parameters
            $para = [String]::Empty;
            $name = [String]::Empty;
            $rpid = [String]::Empty;
            $cmdlet = 'New-RetentionCompliancePolicy'
            if ([String]::IsNullOrEmpty($rp.'Policy Name (Required)'))
            {
                WriteToLog -Type "Failed" -Message "Could not acquire table for writing."
                throw;
            }
            else
            {
               $name = $rp.'Policy Name (Required)'
               $cmdlet += " -Name '" + $name + "'"
            }
            if ([String]::IsNullOrEmpty($rp.'Enabled (Required)'))
            {
                WriteToLog -Type "Failed" -Message "Could not acquire table for writing."
                throw;
            }
            else
            {
                $enabled = $rp.'Enabled (Required)'
                $cmdlet += " -Enabled " + $enabled
            }
            if (![String]::IsNullOrEmpty($rp.'ExchangeLocation (Optional)'))
            {
                $para = $rp.'ExchangeLocation (Optional)'
                $cmdlet += " -ExchangeLocation " + $para
            }
         
            if (![String]::IsNullOrEmpty($rp.'ExchangeLocationException (Optional)'))
            {
                $para = $rp.'ExchangeLocationException (Optional)'
                $cmdlet += " -ExchangeLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'ModernGroupLocation (Optional)'))
            {
                $para = $rp.'ModernGroupLocation (Optional)'
                $cmdlet += " -ModernGroupLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'ModernGroupLocationException (Optional)'))
            {
                $para = $rp.'ModernGroupLocationException (Optional)'
                $cmdlet += " -ModernGroupLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'OneDriveLocation (Optional)'))
            {
                $para = $rp.'OneDriveLocation (Optional)'
                $cmdlet += " -OneDriveLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'OneDriveLocationException (Optional)'))
            {
                $para = $rp.'OneDriveLocationException (Optional)'
                $cmdlet += " -OneDriveLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SharePointLocation (Optional)'))
            {
                $para = $rp.'SharePointLocation (Optional)'
                $cmdlet += " -SharePointLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SharePointLocationException (Optional)'))
            {
                $para = $rp.'SharePointLocationException (Optional)'
                $cmdlet += " -SharePointLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'PublicFolderLocation (Optional)'))
            {
                $para = $rp.'PublicFolderLocation (Optional)'
                $cmdlet += " -PublicFolderLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SkypeLocation (Optional)'))
            {
                $para = $rp.'SkypeLocation (Optional)'
                $cmdlet += " -SkypeLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SkypeLocationException (Optional)'))
            {
                $para = $rp.'SkypeLocationException (Optional)'
                $cmdlet += " -SkypeLocationException " + $para
            }
            # If the policy already exists, skip for creation
            if (($policies -eq $null) -or ($policies | ? { $_.Name.ToLower() -eq $name.ToLower() }) -eq $null)
            {
                # Create retention compliance policy
                $msg = "Execute Cmdlet : {0}" -f $cmdlet
            
                $ret = invokepowershellcmdlet $cmdlet
            
                if ($ret -eq $null)
                {
                    WriteToLog -Type "Failed" $error[0]
                    break;
                }
                $rpid = $ret.Guid
            }
            else
            {
                WriteToLog -Type "Warning" -Message "The policy '$name' already exists! Skip for creation!"
                $rpid = ($policies | ? { $_.Name.ToLower() -eq $name.ToLower() }).Guid
            }
                        
            # Retrieve tag name for publishing
            $ts = $rp.'PublishComplianceTag (Required)'
            $tagList = $ts.Split(",") | ForEach-Object { $_.Trim() }
            
            WriteToLog -Type "Message" -Message "Publish Tags : '$ts'" 
            
            PublishComplianceTag -PolicyGuid $rpid -TagName $tagList
        }
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in input"
    }
}
# -------------------
# Publish Compliance Tag
# -------------------
Function PublishComplianceTag
{
    Param(
        [Parameter(Mandatory = $true)]
        [String]$PolicyGuid,
        [Parameter(Mandatory = $true)]
        [String[]]$TagNames
    )
    
    WriteToLog -Type "Start" "Start to Publish Compliance Tag"
    try
    {
        # Retrieve existing rule related to the given compliance policy
        $rule = InvokePowerShellCmdlet ("Get-RetentionComplianceRule -Policy {0}" -f $PolicyGuid)
        $tagGuids = New-Object System.Collections.ArrayList
        
        foreach ($tn in $TagNames)
        {
            $t = InvokePowerShellCmdlet ("Get-ComplianceTag {0}" -f $tn)
            $tagGuids.Add($t.Guid) | Out-Null
        }
        if ($rule -ne $null)
        {
            foreach ($r in $rule)
            {
                if ([String]::IsNullOrEmpty($r.PublishComplianceTag))
                {
                    continue;
                }
                else
                {
                    $tl = $r.PublishComplianceTag.Split(",")
                    if ($tagGuids.Contains([GUID]$tl[0]))
                    {
                        $tagGuids.Remove([GUID]$tl[0]);
                    }
                }
            }
        }
        
        foreach($t in $tagGuids)
        {
            # Publish compliance tag
            $cmdlet = "New-RetentionComplianceRule -Policy {0} -PublishComplianceTag {1}" -f $PolicyGuid, $t
            $ret = InvokePowerShellCmdlet $cmdlet
            
            if ($ret -eq $null)
            {
                WriteToLog -Type "Failed" $error[0]
                break;
            }
        }
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in input"
    }
}
# -------------------
# Export All Labels Created in The Process
# -------------------
Function ExportCreatedComplianceTag
{
    Param(
        [Parameter(Mandatory = $true)]
        [String]$LabelFilePath
    )
    
    WriteToLog -Type "Start" "Start to Export Compliance Tag Created"
    try
    {
        # Import input csv
        $labels = Import-Csv $LabelFilePath
        # Create result table
        $tabName = "ResultTable"
        $table = New-Object system.Data.DataTable "$tabName"
        $col1 = New-Object system.Data.DataColumn Name,([string])
        $col2 = New-Object system.Data.DataColumn Comment,([string])
        $col3 = New-Object system.Data.DataColumn IsRecordLabel,([string])
        $col4 = New-Object system.Data.DataColumn RetentionAction,([string])
        $col5 = New-Object system.Data.DataColumn RetentionDuration,([string])
        $col6 = New-Object system.Data.DataColumn RetentionType,([string])
        $col7 = New-Object system.Data.DataColumn ReviewerEmail,([string])
        
        # Add the Columns
        $table.columns.add($col1)
        $table.columns.add($col2)
        $table.columns.add($col3)
        $table.columns.add($col4)
        $table.columns.add($col5)
        $table.columns.add($col6)
        $table.columns.add($col7)
        foreach($lab in $labels)
        {
            $t = InvokePowerShellCmdlet ("Get-ComplianceTag '{0}' " -f $lab.'Name (Required)')
            
            # Create a result row
            $row = $table.NewRow()
            $row['Name'] = $t.Name
            $row['Comment'] = $t.Comment
            $row['IsRecordLabel'] = $t.IsRecordLabel
            $row['RetentionAction'] = $t.RetentionAction
            $row['RetentionDuration'] = $t.RetentionDuration
            $row['RetentionType'] = $t.RetentionType
            $row['ReviewerEmail'] = $t.ReviewerEmail
            
            # Add the row to the table
            $table.Rows.Add($row)
        }
        $table | Export-Csv $tagRetFile -NoTypeInformation
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in exporting results."
    }
}
# -------------------
# Export All Published Labels and Policies in The Process
# -------------------
Function ExportPublishedComplianceTagAndPolicy
{
    Param(
        [Parameter(Mandatory = $true)]
        [String[]]$PolicyFilePath
    )
    
    WriteToLog -Type "Start" "Start to Export Published Compliance Tag and Policy"
    try
    {
        # Import input csv
        $policies = Import-Csv $PolicyFilePath
        # Create result table
        $tabName = "ResultTable"
        $table = New-Object system.Data.DataTable "$tabName"
        $col1 = New-Object system.Data.DataColumn 'Policy Name',([string])
        $col2 = New-Object system.Data.DataColumn PublishComplianceTag,([string])
        $col3 = New-Object system.Data.DataColumn Comment,([string])
        $col4 = New-Object system.Data.DataColumn Enabled,([string])
        $col5 = New-Object system.Data.DataColumn ExchangeLocation,([string])
        $col6 = New-Object system.Data.DataColumn ExchangeLocationException,([string])
        $col7 = New-Object system.Data.DataColumn ModernGroupLocation,([string])
        $col8 = New-Object system.Data.DataColumn ModernGroupLocationException,([string])
        $col9 = New-Object system.Data.DataColumn OneDriveLocation,([string])
        $col10 = New-Object system.Data.DataColumn OneDriveLocationException,([string])
        $col11 = New-Object system.Data.DataColumn PublicFolderLocation,([string])
        $col12 = New-Object system.Data.DataColumn SharePointLocation,([string])
        $col13 = New-Object system.Data.DataColumn SharePointLocationException,([string])
        $col14 = New-Object system.Data.DataColumn SkypeLocation,([string])
        $col15 = New-Object system.Data.DataColumn SkypeLocationException,([string])
        
        # Add the Columns
        $table.columns.add($col1)
        $table.columns.add($col2)
        $table.columns.add($col3)
        $table.columns.add($col4)
        $table.columns.add($col5)
        $table.columns.add($col6)
        $table.columns.add($col7)
        $table.columns.add($col8)
        $table.columns.add($col9)
        $table.columns.add($col10)
        $table.columns.add($col11)
        $table.columns.add($col12)
        $table.columns.add($col13)
        $table.columns.add($col14)
        $table.columns.add($col15)
        foreach($policy in $policies)
        {
            $t = InvokePowerShellCmdlet ("Get-RetentionCompliancePolicy '{0}' -DistributionDetail" -f $policy.'Policy Name (Required)')
            
            # Create a result row
            $row = $table.NewRow()
            $row['Policy Name'] = $t.Name
            
            $rules = InvokePowerShellCmdlet ("Get-RetentionComplianceRule -Policy {0}" -f $t.Guid)
            $tagList = [String]::Empty
            foreach($rule in $rules)
            {
                if ([String]::IsNullOrEmpty($rule.PublishComplianceTag) -eq $False)
                {
                    $tName = $rule.PublishComplianceTag.Split(',')[1]
                    $tagList = [String]::Concat($tagList, $tName, ",")
                }
            }
            if (![String]::IsNullOrEmpty($tagList))
            {
                $tagList = $tagList.Substring(0, $tagList.LastIndexOf(','))
            }
            $row['PublishComplianceTag'] = $tagList
            $row['Comment'] = $t.Comment
            $row['Enabled'] = $t.Enabled
            $row['ExchangeLocation'] = $t.ExchangeLocation
            $row['ExchangeLocationException'] = $t.ExchangeLocationException
            $row['ModernGroupLocation'] = $t.ModernGroupLocation
            $row['ModernGroupLocationException'] = $t.ModernGroupLocationException
            $row['OneDriveLocation'] = $t.OneDriveLocation
            $row['OneDriveLocationException'] = $t.OneDriveLocationException
            $row['PublicFolderLocation'] = $t.PublicFolderLocation
            $row['SharePointLocation'] = $t.SharePointLocation
            $row['SharePointLocationException'] = $t.SharePointLocationException
            $row['SkypeLocation'] = $t.SkypeLocation
            $row['SkypeLocationException'] = $t.SkypeLocationException
            
            # Add the row to the table
            $table.Rows.Add($row)
        }
        $table | Export-Csv $tagPubRetFile -NoTypeInformation
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in exporting results."
    }
}
# Create compliance tag
CreateComplianceTag -FilePath $LabelListCSV
# Create retention policy and publish compliance tag with the policy
CreateRetentionCompliancePolicy -FilePath $PolicyListCSV
# Export to result csv
if ($ResultCSV)
{
    ExportCreatedComplianceTag -LabelFilePath $LabelListCSV
    ExportPublishedComplianceTagAndPolicy -PolicyFilePath $PolicyListCSV 
}

```

## <a name="step-4-connect-to-security-amp-compliance-center-powershell"></a><span data-ttu-id="575b5-150">Étape 4 : connectez-vous au Centre de sécurité &amp; conformité PowerShell</span><span class="sxs-lookup"><span data-stu-id="575b5-150">Step 4: Connect to Security &amp; Compliance Center PowerShell</span></span>

<span data-ttu-id="575b5-151">Consultez les étapes décrites ici :</span><span class="sxs-lookup"><span data-stu-id="575b5-151">Follow the steps here:</span></span>
  
- [<span data-ttu-id="575b5-152">Connexion au Centre de sécurité &amp; conformité Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="575b5-152">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
## <a name="step-5-run-the-powershell-script-to-create-and-publish-the-retention-labels"></a><span data-ttu-id="575b5-153">Étape 5 : exécuter le script PowerShell pour créer et publier les étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="575b5-153">Step 5: Run the PowerShell script to create and publish the retention labels</span></span>

<span data-ttu-id="575b5-154">Une fois que vous êtes connecté au Centre de sécurité &amp; conformité PowerShell, exécutez le script qui crée et publie les étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="575b5-154">After you've connected to Security &amp; Compliance Center PowerShell, next you run the script that creates and publishes the retention labels.</span></span>
  
1. <span data-ttu-id="575b5-155">Dans la session de sécurité &amp; conformité PowerShell, saisissez le chemin d’accès suivi des caractères .\ et le nom de fichier du script, puis appuyez sur ENTRÉE pour exécuter le script, par exemple :</span><span class="sxs-lookup"><span data-stu-id="575b5-155">In the Security &amp; Compliance PowerShell session, enter the path, followed by the characters .\ and file name of the script, and then press ENTER to run the script - for example:</span></span>
    
  ```
  <path>.\CreateRetentionSchedule.ps1
  ```

    <span data-ttu-id="575b5-156">Le script vous invite à saisir les emplacements des fichiers .csv que vous avez créés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="575b5-156">The script will prompt you for the locations of the .csv files that you created above.</span></span>
    
2. <span data-ttu-id="575b5-157">Saisissez le chemin d’accès suivi des caractères .\ et le nom de fichier du script, puis appuyez sur ENTRÉE, par exemple :</span><span class="sxs-lookup"><span data-stu-id="575b5-157">Enter the path, followed by the characters .\ and file name of the .csv file, and then press ENTER - for example:</span></span>
    
  ```
  <path>.\LabelsToCreate.csv
  ```

## <a name="step-6-view-the-log-file-with-the-results"></a><span data-ttu-id="575b5-158">Étape 6 : afficher le fichier journal avec les résultats</span><span class="sxs-lookup"><span data-stu-id="575b5-158">Step 6: View the log file with the results</span></span>

<span data-ttu-id="575b5-p113">Lors de son exécution, le script génère un fichier journal qui enregistre chaque action effectuée et si l’action a réussi ou a échoué. Le fichier journal inclut toutes les métadonnées sur les étiquettes de rétention créées et publiées. Le fichier journal figure dans cet emplacement (notez que les chiffres contenus dans le nom du fichier varient).</span><span class="sxs-lookup"><span data-stu-id="575b5-p113">When you run the script, it generates a log file that records each action it took and whether the action succeeded or failed. The log file includes all metadata about the retention labels created and the retention labels published. You can find the log file at this location -- note that the digits in the file name vary.</span></span>
  
```
<path>.\Log_Publish_Compliance_Tag_01112018_151239.txt
```


