---
title: RGPD
description: 'Conseils techniques Microsoft : ENSEMBLE D’OUTILS DE MIGRATION FASTTRACK POUR ENVOYER UNE DEMANDE DE SUPPRESSION'
keywords: Migration FastTrack, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
localization_priority: Priority
Robots: NOFOLLOW,NOINDEX
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: mohitku
author: MohitKumar
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 162a64535f82f24411121ed81e36078511eb8eba
ms.sourcegitcommit: 74ef7179887eedc696c975a82c865b2d4b3808fd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "47416910"
---
# <a name="fasttrack-migration-toolset-for-submitting-delete-request"></a><span data-ttu-id="423ca-104">Ensemble d’outils de migration FastTrack pour envoyer une demande de suppression</span><span class="sxs-lookup"><span data-stu-id="423ca-104">FastTrack Migration Toolset for Submitting Delete Request</span></span>

## <a name="toolset-purpose"></a><span data-ttu-id="423ca-105">Objectif de l’ensemble d’outils</span><span class="sxs-lookup"><span data-stu-id="423ca-105">Toolset purpose</span></span>

<span data-ttu-id="423ca-p101">Si vous êtes un client actuellement engagé dans les migrations FastTrack, la suppression du compte d’utilisateur n’entraîne pas la suppression de la copie des données détenue par l’équipe Microsoft FastTrack, conservée dans le seul but d’exécuter la migration. Si, lors de la migration, vous souhaitez que l’équipe Microsoft FastTrack supprime également la copie des données, envoyez une demande via cet ensemble d’outils. Dans le cours normal des activités, Microsoft FastTrack supprimera toutes les copies de données une fois la migration terminée.</span><span class="sxs-lookup"><span data-stu-id="423ca-p101">In the event that you are a customer currently engaged in FastTrack migrations, deleting the user account will not delete the data copy held by the Microsoft FastTrack team, which is held for the sole purpose of completing the migration. If during the migration you would like the Microsoft FastTrack team to also delete the data copy, submit a request via this tool set. In the ordinary course of business, Microsoft FastTrack will delete all data copies once the migration is complete.</span></span>

### <a name="supported-platforms"></a><span data-ttu-id="423ca-109">Plateformes prises en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-109">Supported platforms</span></span>
<span data-ttu-id="423ca-p102">Microsoft prend en charge la version initiale de cet ensemble d’outils dans la console PowerShell et la plateforme Windows. Les plateformes connues suivantes sont prises en charge par cet ensemble d’outils :</span><span class="sxs-lookup"><span data-stu-id="423ca-p102">Microsoft supports the initial release of this  toolset in the Windows platform and PowerShell console. The following known platforms are supported by this toolset:</span></span>
 
<span data-ttu-id="423ca-112">***Tableau 1 : plateformes prises en charge par cet ensemble d’outils***</span><span class="sxs-lookup"><span data-stu-id="423ca-112">***Table 1 — Platforms supported by this toolset***</span></span>
 
<!--start table here HEADER -->
 
|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
| |<span data-ttu-id="423ca-113">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="423ca-113">**Windows 7**</span></span>|<span data-ttu-id="423ca-114">**Windows 8**</span><span class="sxs-lookup"><span data-stu-id="423ca-114">**Windows 8**</span></span>|<span data-ttu-id="423ca-115">**Windows 10**</span><span class="sxs-lookup"><span data-stu-id="423ca-115">**Windows 10**</span></span>|<span data-ttu-id="423ca-116">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="423ca-116">**Windows Server 2012**</span></span>|<span data-ttu-id="423ca-117">**Windows Server 2016**</span><span class="sxs-lookup"><span data-stu-id="423ca-117">**Windows Server 2016**</span></span>|
|<span data-ttu-id="423ca-118">PS 5.0</span><span class="sxs-lookup"><span data-stu-id="423ca-118">PS 5.0</span></span>|<span data-ttu-id="423ca-119">Non</span><span class="sxs-lookup"><span data-stu-id="423ca-119">Not</span></span><br/><span data-ttu-id="423ca-120">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-120">Supported</span></span>|<span data-ttu-id="423ca-121">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-121">Supported</span></span>|<span data-ttu-id="423ca-122">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-122">Supported</span></span>|<span data-ttu-id="423ca-123">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-123">Supported</span></span>|<span data-ttu-id="423ca-124">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-124">Supported</span></span>|
|<span data-ttu-id="423ca-125">PS 5.1</span><span class="sxs-lookup"><span data-stu-id="423ca-125">PS 5.1</span></span>|<span data-ttu-id="423ca-126">Non</span><span class="sxs-lookup"><span data-stu-id="423ca-126">Not</span></span><br/><span data-ttu-id="423ca-127">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-127">Supported</span></span>|<span data-ttu-id="423ca-128">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-128">Supported</span></span>|<span data-ttu-id="423ca-129">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-129">Supported</span></span>|<span data-ttu-id="423ca-130">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-130">Supported</span></span>|<span data-ttu-id="423ca-131">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="423ca-131">Supported</span></span>|
|||
 
<!-- end of table -->

### <a name="obtaining-the-toolset"></a><span data-ttu-id="423ca-132">Obtention de l’ensemble d’outils</span><span class="sxs-lookup"><span data-stu-id="423ca-132">Obtaining the toolset</span></span>

<span data-ttu-id="423ca-p103">Cet ensemble d’outils est disponible dans la galerie PowerShell sur l’application console PowerShell. Pour rechercher et charger ce module de cmdlet, ouvrez tout d’abord PowerShell en mode administrateur afin d’être autorisé à installer le module. Si vous n’avez jamais utilisé PowerShell, accédez à la barre des tâches Windows et saisissez « PowerShell » dans la zone de recherche. Faites un clic droit sur l’application console pour la sélectionner, choisissez **Exécuter en tant qu’administrateur**, puis cliquez sur **Oui** pour exécuter Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="423ca-p103">This toolset is available in the PowerShell Gallery on the PowerShell console application.  To locate and load this cmdlet module, first open PowerShell in administrator mode so it has the appropriate permissions to install the module. If you have not used PowerShell previously go to your Windows Task Bar and in the search box type “PowerShell”. Select the console app using right-click and choose **Run as administrator**, then click **Yes** to run Windows PowerShell.</span></span>

![PowerShell : exécuter en tant qu’administrateur](../media/fasttrack-powershell_image.png)

![PowerShell : autoriser l’application à apporter des modifications](../media/fasttrack-run-powershell_image.png)

<span data-ttu-id="423ca-p104">À présent que la console est ouverte, vous devez définir des autorisations pour l’exécution des scripts. Saisissez la commande suivante pour autoriser l’exécution des scripts : « Set-ExecutionPolicy ; ExecutionPolicy: Bypass ; Scope: Process »</span><span class="sxs-lookup"><span data-stu-id="423ca-p104">Now that the console is open, you need to set permissions for script execution. Type the following command to allow the scripts to run: ‘Set-ExecutionPolicy — ExecutionPolicy: Bypass — Scope: Process’</span></span>

<span data-ttu-id="423ca-141">Vous serez invité à confirmer cette action, car l’administrateur peut modifier l’étendue à sa guise.</span><span class="sxs-lookup"><span data-stu-id="423ca-141">You will be prompted to confirm this action, as the administrator can change the scope at their discretion.</span></span>

<span data-ttu-id="423ca-142">***Définir la stratégie d’exécution***</span><span class="sxs-lookup"><span data-stu-id="423ca-142">***Set Execution Policy***</span></span>

![Définir la modification de la stratégie d’exécution dans PowerShell](../media/powershell-set-execution-policy_image.png)

<span data-ttu-id="423ca-144">À présent que la console est configurée pour autoriser le script, exécutez la commande suivante pour installer le module :</span><span class="sxs-lookup"><span data-stu-id="423ca-144">Now that the console is set to allow the script,  run this next command to install the module:</span></span>

><span data-ttu-id="423ca-145">`Install-Module -Name Microsoft.FastTrack ` -Repository PSGallery \`</span><span class="sxs-lookup"><span data-stu-id="423ca-145">`Install-Module -Name Microsoft.FastTrack ` -Repository PSGallery \`</span></span>
>        
>               -WarningAction: SilentlyContinue `
>               -Force’

### <a name="prerequisites-for-module"></a><span data-ttu-id="423ca-146">Conditions préalables pour le module</span><span class="sxs-lookup"><span data-stu-id="423ca-146">Prerequisites for module</span></span>
<span data-ttu-id="423ca-p105">Pour exécuter correctement ce module, vous devrez peut-être installer des modules dépendants si ce n’est pas déjà fait. Vous devrez peut-être redémarrer PowerShell.</span><span class="sxs-lookup"><span data-stu-id="423ca-p105">To successfully execute this module, you may need to install dependent modules for use if they are not already installed. You may need to restart PowerShell.</span></span>  

<span data-ttu-id="423ca-149">Pour envoyer une DSR, vous devez tout d’abord vous connecter à l’aide de vos identifiants Office 365 : saisissez les identifiants corrects pour valider votre statut d’administrateur général et collecter des informations client.</span><span class="sxs-lookup"><span data-stu-id="423ca-149">In order to submit a DSR, you must first log in using your Office 365 credentials — entering the proper credentials will validate your global administrator status and collect tenant information.</span></span> 

<span data-ttu-id="423ca-150">**Clé Api de la Recherche Rapide de Compte de la Connexion: \<API Key provided by FastTrack MVM\>**</span><span class="sxs-lookup"><span data-stu-id="423ca-150">**Login-FastTrackAccount -ApiKey: \<API Key provided by FastTrack MVM\>**</span></span>

<span data-ttu-id="423ca-151">Une fois que vous êtes connecté, les identifiants et la clé sont stockés pour être utilisés avec les modules FastTrack pendant le reste de la session PowerShell actuelle.</span><span class="sxs-lookup"><span data-stu-id="423ca-151">Once successfully logged in, the credentials and key will be stored for use with FastTrack modules for the remainder of the current PowerShell session.</span></span>

<span data-ttu-id="423ca-152">Si vous avez besoin de vous connecter à un environnement cloud autre que commercial, vous devrez ajouter *-Environment* à la commande *Login* avec l’un des environnements valides suivants :</span><span class="sxs-lookup"><span data-stu-id="423ca-152">If you need to connect to a cloud environment, other than commercial, *-Environment* will need to be added to *Log in* command with one of the following valid environments:</span></span>
- <span data-ttu-id="423ca-153">AzureCloud</span><span class="sxs-lookup"><span data-stu-id="423ca-153">AzureCloud</span></span>
- <span data-ttu-id="423ca-154">AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="423ca-154">AzureChinaCloud</span></span>
- <span data-ttu-id="423ca-155">AzureGermanCloud</span><span class="sxs-lookup"><span data-stu-id="423ca-155">AzureGermanCloud</span></span>
- <span data-ttu-id="423ca-156">AzureUSGovernmentCloud</span><span class="sxs-lookup"><span data-stu-id="423ca-156">AzureUSGovernmentCloud</span></span>

<span data-ttu-id="423ca-157">**Login-FastTrackAcccount -ApiKey\ <API Key provided by FastTrack MVM> -Environment: <cloud environment\>**</span><span class="sxs-lookup"><span data-stu-id="423ca-157">**Login-FastTrackAcccount -ApiKey\ <API Key provided by FastTrack MVM> -Environment: <cloud environment\>**</span></span>

<span data-ttu-id="423ca-158">Pour envoyer une demande de DSR, exécutez la commande suivante : FastTrackGdprDsrRequest soumettre - DsrRequestUserEmail : SubjectUserEmail@mycompany.com</span><span class="sxs-lookup"><span data-stu-id="423ca-158">To submit a DSR request, run the following command: Submit-FastTrackGdprDsrRequest -DsrRequestUserEmail: SubjectUserEmail@mycompany.com</span></span>

<span data-ttu-id="423ca-p106">En cas de réussite, la cmdlet renvoie un objet d’ID de transaction. Veuillez conserver l’ID de transaction.</span><span class="sxs-lookup"><span data-stu-id="423ca-p106">On success — the cmdlet will return a Transaction ID object. Please retain the Transaction ID.</span></span>


#### <a name="checking-the-status-of-a-request-transaction"></a><span data-ttu-id="423ca-161">Vérification de l’état de transaction d’une demande</span><span class="sxs-lookup"><span data-stu-id="423ca-161">Checking the status of a request transaction</span></span>

<span data-ttu-id="423ca-162">Exécutez la fonction suivante à l’aide de l’ID de transaction obtenu précédemment : Get-FastTrackGdprDsrRequest -TransactionID: “YourTransactionID”</span><span class="sxs-lookup"><span data-stu-id="423ca-162">Run the following function using the previously obtained Transaction ID: Get-FastTrackGdprDsrRequest -TransactionID: “YourTransactionID”</span></span>

#### <a name="transaction-status-codes"></a><span data-ttu-id="423ca-163">Codes d’état de transaction</span><span class="sxs-lookup"><span data-stu-id="423ca-163">Transaction Status Codes</span></span>
<!--start table here no header -->

|||
|:-----|:-----|:-----|
|<span data-ttu-id="423ca-164">**Transaction**</span><span class="sxs-lookup"><span data-stu-id="423ca-164">**Transaction**</span></span> |<span data-ttu-id="423ca-165">**État**</span><span class="sxs-lookup"><span data-stu-id="423ca-165">**Status**</span></span>|
|<span data-ttu-id="423ca-166">**Créée**</span><span class="sxs-lookup"><span data-stu-id="423ca-166">**Created**</span></span> |<span data-ttu-id="423ca-167">Demande créée</span><span class="sxs-lookup"><span data-stu-id="423ca-167">Request has been created</span></span>|
|<span data-ttu-id="423ca-168">**Échec**</span><span class="sxs-lookup"><span data-stu-id="423ca-168">**Failed**</span></span>|<span data-ttu-id="423ca-169">Échec de la création de la demande : renvoyez-la ou contactez le support technique</span><span class="sxs-lookup"><span data-stu-id="423ca-169">Request failed to create, please resubmit, or contact support</span></span>|
|<span data-ttu-id="423ca-170">**Terminée**</span><span class="sxs-lookup"><span data-stu-id="423ca-170">**Completed**</span></span>|<span data-ttu-id="423ca-171">Demande terminée et purgée</span><span class="sxs-lookup"><span data-stu-id="423ca-171">Request has been completed and sanitized</span></span>|
|||

<!-- end of table -->

<!-- original version: **Created**  Request has been created<br/>**Failed** Request failed to create, please resubmit, or contact support<br/>**Completed** Request has been completed and sanitized -->


## <a name="learn-more"></a><span data-ttu-id="423ca-172">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="423ca-172">Learn more</span></span>
[<span data-ttu-id="423ca-173">Centre de gestion de la confidentialité Microsoft</span><span class="sxs-lookup"><span data-stu-id="423ca-173">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview
)
