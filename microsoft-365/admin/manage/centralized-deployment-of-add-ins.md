---
title: Déterminer si le déploiement centralisé des add-ins fonctionne pour votre organisation
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b4527d49-4073-4b43-8274-31b7a3166f92
description: Déterminez si votre client et vos utilisateurs répondent aux exigences, afin de pouvoir utiliser le déploiement centralisé pour déployer des add-ins Office.
ms.openlocfilehash: 1516a10932158ba137f58900e0c19c5fea3bd119
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51580953"
---
# <a name="determine-if-centralized-deployment-of-add-ins-works-for-your-organization"></a><span data-ttu-id="ea3e8-103">Déterminer si le déploiement centralisé des add-ins fonctionne pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="ea3e8-103">Determine if Centralized Deployment of add-ins works for your organization</span></span>

<span data-ttu-id="ea3e8-104">Le déploiement centralisé est le moyen recommandé et le plus riche en fonctionnalités pour la plupart des clients de déployer des add-ins Office pour des utilisateurs et des groupes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-104">Centralized Deployment is the recommended and most feature-rich way for most customers to deploy Office add-ins to users and groups within your organization.</span></span> <span data-ttu-id="ea3e8-105">Si vous êtes un administrateur, utilisez ces conseils pour déterminer si votre organisation et les utilisateurs répondent aux exigences afin de pouvoir utiliser le déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-105">If you're an admin, use this guidance to determine if your organization and users meet the requirements so that you can use Centralized Deployment.</span></span>

<span data-ttu-id="ea3e8-106">Une déploiement centralisé offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-106">Centralized Deployment provides the following benefits:</span></span>
  
- <span data-ttu-id="ea3e8-107">Un administrateur général peut affecter un add-in directement à un utilisateur, à plusieurs utilisateurs via un groupe ou à tous les membres de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-107">A Global admin can assign an add-in directly to a user, to multiple users via a group, or to everyone in the organization.</span></span>
    
- <span data-ttu-id="ea3e8-108">Lorsque l’application Office concernée démarre, le add-in se télécharge automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-108">When the relevant Office application starts, the add-in automatically downloads.</span></span> <span data-ttu-id="ea3e8-109">Si le add-in prend en charge les commandes de l’application, celui-ci apparaît automatiquement dans le ruban dans l’application Office.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-109">If the add-in supports add-in commands, the add-in automatically appears in the ribbon within the Office application.</span></span>
    
- <span data-ttu-id="ea3e8-110">Les add-ins n’apparaissent plus pour les utilisateurs si l’administrateur le met hors service ou le supprime, ou si l’utilisateur est supprimé d’Azure Active Directory ou d’un groupe à qui le module est affecté.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-110">Add-ins no longer appear for users if the admin turns off or deletes the add-in, or if the user is removed from Azure Active Directory or from a group that the add-in is assigned to.</span></span>

<span data-ttu-id="ea3e8-111">Le déploiement centralisé prend en charge trois plateformes de bureau pour les applications Windows, Mac et Office en ligne.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-111">Centralized Deployment supports three desktop platforms Windows, Mac and Online Office apps.</span></span> <span data-ttu-id="ea3e8-112">Le déploiement centralisé prend également en charge iOS et Android (applications Outlook Mobile uniquement).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-112">Centralized Deployment also supports iOS and Android (Outlook Mobile Add-ins Only).</span></span>

<span data-ttu-id="ea3e8-113">L’ouverture d’un client pour tous les utilisateurs peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-113">It can take up to 24 hours for an add-in to show up for client for all users.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="ea3e8-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ea3e8-114">Requirements</span></span>

<span data-ttu-id="ea3e8-115">Le déploiement centralisé des add-ins nécessite que les utilisateurs utilisent les références (SSO) Microsoft 365 Entreprise : E3/E5/F3 ou Business : Business Basic, Business Standard, Business Premium (et sont signés dans Office à l’aide de leur ID d’organisation) et qu’ils ont des boîtes aux lettres Exchange Online et Exchange Online actives.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-115">Centralized deployment of add-ins requires that the users are using Microsoft 365 Enterprise SKUs: E3/E5/F3 or Business SKUs: Business Basic, Business Standard, Business Premium (and are signed into Office using their organizational ID), and have Exchange Online and active Exchange Online mailboxes.</span></span> <span data-ttu-id="ea3e8-116">Votre annuaire d’abonnement doit être dans Azure Active Directory ou fédéré.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-116">Your subscription directory must either be in, or federated to Azure Active Directory.</span></span>
<span data-ttu-id="ea3e8-117">Vous pouvez afficher les exigences spécifiques d’Office et d’Exchange ci-dessous, ou utiliser le contrôle de compatibilité du déploiement [centralisé.](#centralized-deployment-compatibility-checker)</span><span class="sxs-lookup"><span data-stu-id="ea3e8-117">You can view specific requirements for Office and Exchange below, or use the [Centralized Deployment Compatibility Checker](#centralized-deployment-compatibility-checker).</span></span>

<span data-ttu-id="ea3e8-118">La fonctionnalité Déploiement centralisé ne prend pas en charge ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-118">Centralized Deployment doesn't support the following:</span></span>
  
- <span data-ttu-id="ea3e8-119">des compléments ciblant Word, Excel ou PowerPoint dans Office 2013 ;</span><span class="sxs-lookup"><span data-stu-id="ea3e8-119">Add-ins that target Word, Excel, or PowerPoint in Office 2013</span></span> 
- <span data-ttu-id="ea3e8-120">un service d'annuaire local ;</span><span class="sxs-lookup"><span data-stu-id="ea3e8-120">An on-premises directory service</span></span>
- <span data-ttu-id="ea3e8-121">Déploiement d’un add-in vers une boîte aux lettres exchange sur place</span><span class="sxs-lookup"><span data-stu-id="ea3e8-121">Add-in Deployment to an Exchange On-Prem Mailbox</span></span>
- <span data-ttu-id="ea3e8-122">le déploiement de compléments vers SharePoint ;</span><span class="sxs-lookup"><span data-stu-id="ea3e8-122">Add-in deployment to SharePoint</span></span>  
- <span data-ttu-id="ea3e8-123">Applications Teams</span><span class="sxs-lookup"><span data-stu-id="ea3e8-123">Teams apps</span></span>
- <span data-ttu-id="ea3e8-124">Déploiement de composants COM (Component Object Model) ou de Visual Studio outils pour Office (VSTO).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-124">Deployment of Component Object Model (COM) or Visual Studio Tools for Office (VSTO) add-ins.</span></span>
- <span data-ttu-id="ea3e8-125">Déploiements de Microsoft 365 qui n’incluent pas Exchange Online comme les S SKUs : Microsoft 365 Apps for Business et Microsoft 365 Apps for Enterprise.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-125">Deployments of Microsoft 365 that do not include Exchange Online such as SKUs: Microsoft 365 Apps for Business and Microsoft 365 Apps for Enterprise.</span></span>

### <a name="office-requirements"></a><span data-ttu-id="ea3e8-126">Conditions requises pour Office</span><span class="sxs-lookup"><span data-stu-id="ea3e8-126">Office Requirements</span></span>

- <span data-ttu-id="ea3e8-127">Pour les add-ins Word, Excel et PowerPoint, vos utilisateurs doivent utiliser l’une des utilisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-127">For Word, Excel, and PowerPoint add-ins, your users must be using one of the following:</span></span>
  - <span data-ttu-id="ea3e8-128">Sur un appareil Windows, version 1704 ou ultérieure des références (S SKUs) Microsoft 365 Entreprise : E3/E5/F3 ou Business : Business Basic, Business Standard, Business Premium.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-128">On a Windows device, Version 1704 or later of Microsoft 365 Enterprise SKUs: E3/E5/F3 or Business SKUs: Business Basic, Business Standard, Business Premium.</span></span>
  - <span data-ttu-id="ea3e8-129">Sur un Mac, version 15.34 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-129">On a Mac, Version 15.34 or later.</span></span>

- <span data-ttu-id="ea3e8-130">Pour Outlook, vos utilisateurs doivent utiliser l’une des utilisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-130">For Outlook, your users must be using one of the following:</span></span> 
  - <span data-ttu-id="ea3e8-131">Version 1701 ou ultérieure des références Microsoft 365 Entreprise : référenceS E3/E5/F3 ou Business : Business Basic, Business Standard, Business Premium.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-131">Version 1701 or later of Microsoft 365 Enterprise SKUs: E3/E5/F3 or Business SKUs: Business Basic, Business Standard, Business Premium.</span></span>
  - <span data-ttu-id="ea3e8-132">Version 1808 ou ultérieure Office Professionnel Plus 2019 ou Office Standard 2019.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-132">Version 1808 or later of Office Professional Plus 2019 or Office Standard 2019.</span></span>
  - <span data-ttu-id="ea3e8-133">Version 16.0.4494.1000 ou ultérieure de Office Professionnel Plus 2016 (MSI) ou Office Standard 2016 (MSI)\*</span><span class="sxs-lookup"><span data-stu-id="ea3e8-133">Version 16.0.4494.1000 or later of Office Professional Plus 2016 (MSI) or Office Standard 2016 (MSI)\*</span></span>
  - <span data-ttu-id="ea3e8-134">Version 15.0.4937.1000 ou ultérieure de Office Professionnel Plus 2013 (MSI) ou Office Standard 2013 (MSI)\*</span><span class="sxs-lookup"><span data-stu-id="ea3e8-134">Version 15.0.4937.1000 or later of Office Professional Plus 2013 (MSI) or Office Standard 2013 (MSI)\*</span></span>
  - <span data-ttu-id="ea3e8-135">Version 16.0.9318.1000 ou ultérieure d’Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="ea3e8-135">Version 16.0.9318.1000 or later of Office 2016 for Mac</span></span> 
- <span data-ttu-id="ea3e8-136">Version 2.75.0 ou ultérieure d’Outlook Mobile pour iOS</span><span class="sxs-lookup"><span data-stu-id="ea3e8-136">Version 2.75.0 or later of Outlook mobile for iOS</span></span> 
- <span data-ttu-id="ea3e8-137">Version 2.2.145 ou ultérieure d’Outlook Mobile pour Android</span><span class="sxs-lookup"><span data-stu-id="ea3e8-137">Version 2.2.145 or later of Outlook mobile for Android</span></span> 
    
    <span data-ttu-id="ea3e8-138">\*Les versions MSI d’Outlook montrent les add-ins installés par l’administrateur dans le ruban Outlook approprié, et non dans la section « Mes modules ».</span><span class="sxs-lookup"><span data-stu-id="ea3e8-138">\*MSI versions of Outlook show admin-installed add-ins in the appropriate Outlook ribbon, not the "My add-ins" section.</span></span>

### <a name="exchange-online-requirements"></a><span data-ttu-id="ea3e8-139">Conditions requises pour Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ea3e8-139">Exchange Online requirements</span></span>

<span data-ttu-id="ea3e8-140">Microsoft Exchange stocke les manifestes du add-in dans le client de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-140">Microsoft Exchange stores the add-in manifests within your organization's tenant.</span></span> <span data-ttu-id="ea3e8-141">L’administrateur déployant des applications et les utilisateurs qui les reçoivent doivent se trouver sur une version d’Exchange Online qui prend en charge l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-141">The admin deploying add-ins and the users receiving those add-ins must be on a version of Exchange Online that supports OAuth authentication.</span></span>
  
<span data-ttu-id="ea3e8-p106">Pour connaître la configuration utilisée, consultez l'administrateur Exchange de votre organisation. Vous pouvez vérifier la connectivité OAuth de chaque utilisateur à l'aide de l'applet de commande PowerShell [Test-OAuthConnectivity](/powershell/module/exchange/test-oauthconnectivity).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-p106">Check with your organization's Exchange admin to find out which configuration is in use. OAuth connectivity per user can be verified by using the [Test-OAuthConnectivity](/powershell/module/exchange/test-oauthconnectivity) PowerShell cmdlet.</span></span> 


### <a name="centralized-deployment-compatibility-checker"></a><span data-ttu-id="ea3e8-144">Contrôle de compatibilité du déploiement centralisé</span><span class="sxs-lookup"><span data-stu-id="ea3e8-144">Centralized Deployment Compatibility Checker</span></span>

<span data-ttu-id="ea3e8-145">À l’aide du contrôle de compatibilité du déploiement centralisé, vous pouvez vérifier si les utilisateurs de votre client sont configurer pour utiliser le déploiement centralisé pour Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-145">Using the Centralized Deployment Compatibility Checker, you can verify whether the users on your tenant are set up to use Centralized Deployment for Word, Excel and PowerPoint.</span></span> <span data-ttu-id="ea3e8-146">Le vérificateur de compatibilité n'est pas requis pour la prise en charge d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-146">The Compatibility Checker is not required for Outlook support.</span></span> <span data-ttu-id="ea3e8-147">Téléchargez le vérificateur de compatibilité [ici](https://aka.ms/officeaddindeploymentorgcompatibilitychecker).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-147">Download the compatibility checker [here](https://aka.ms/officeaddindeploymentorgcompatibilitychecker).</span></span>
  
#### <a name="run-the-compatibility-checker"></a><span data-ttu-id="ea3e8-148">Exécuter le contrôle de compatibilité</span><span class="sxs-lookup"><span data-stu-id="ea3e8-148">Run the compatibility checker</span></span>
  
1. <span data-ttu-id="ea3e8-149">Démarrez une fenêtre PowerShell.exe avec élévation de PowerShell.exe.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-149">Start an elevated PowerShell.exe window.</span></span>
    
2. <span data-ttu-id="ea3e8-150">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-150">Run the following command:</span></span>

   ```powershell
   Import-Module O365CompatibilityChecker
   ```
    
3. <span data-ttu-id="ea3e8-151">Exécutez **la commande Invoke-CompatabilityCheck** :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-151">Run the **Invoke-CompatabilityCheck** command:</span></span>

   ```powershell
   Invoke-CompatibilityCheck
   ```
   <span data-ttu-id="ea3e8-152">Cette commande vous demande  *_TenantDomain_* (par exemple, *TailspinToysIncorporated.onmicrosoft). </span> com*) et  *_Les informations d’identification TenantAdmin_* (utilisez vos informations d’identification d’administrateur global), puis demande le consentement.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-152">This command prompts you for  *_TenantDomain_* (for example, *TailspinToysIncorporated.onmicrosoft.</span>com*) and  *_TenantAdmin_* credentials (use your global admin credentials), and then requests consent.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="ea3e8-153">Selon le nombre d'utilisateurs dans votre client, l'exécution du vérificateur peut prendre quelques minutes ou plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-153">Depending on the number of users in your tenant, the checker could complete in minutes or hours.</span></span> 
  
<span data-ttu-id="ea3e8-154">Une fois l'exécution de l'outil terminée, celui-ci génère un fichier de sortie dans un format séparé par des virgules (.csv).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-154">When the tool finishes running, it produces an output file in comma-separated (.csv) format.</span></span> <span data-ttu-id="ea3e8-155">Le fichier est enregistré **dans C:\windows\system32** par défaut.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-155">The file is saved to **C:\windows\system32** by default.</span></span> <span data-ttu-id="ea3e8-156">Le fichier de sortie contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-156">The output file contains the following information:</span></span>
  
- <span data-ttu-id="ea3e8-157">Nom d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="ea3e8-157">User Name</span></span>
    
- <span data-ttu-id="ea3e8-158">ID d'utilisateur (adresse de courrier de l'utilisateur)</span><span class="sxs-lookup"><span data-stu-id="ea3e8-158">User ID (User's email address)</span></span>
    
- <span data-ttu-id="ea3e8-159">Déploiement centralisé prêt - Si les autres éléments sont vérifiés</span><span class="sxs-lookup"><span data-stu-id="ea3e8-159">Centralized Deployment ready - If the remaining items are true</span></span>
    
- <span data-ttu-id="ea3e8-160">Plan Office : le plan d’Office pour qui ils sont titulaires d’une licence</span><span class="sxs-lookup"><span data-stu-id="ea3e8-160">Office plan - The plan of Office they are licensed for</span></span>
    
- <span data-ttu-id="ea3e8-161">Activation d'Office - Si l'utilisateur a activé Office</span><span class="sxs-lookup"><span data-stu-id="ea3e8-161">Office Activated - If they have activated Office</span></span>
    
- <span data-ttu-id="ea3e8-162">Boîte aux lettres prise en charge - Si l'utilisateur a une boîte aux lettres OAuth</span><span class="sxs-lookup"><span data-stu-id="ea3e8-162">Supported Mailbox - If they are on an OAuth-enabled mailbox</span></span>

> [!NOTE]
> <span data-ttu-id="ea3e8-163">L’authentification multifacteur n’est pas prise en charge lors de l’utilisation du module PowerShell de déploiement central.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-163">Multifactor authentication is not supported when using the Central Deployment PowerShell module.</span></span>
  
## <a name="user-and-group-assignments"></a><span data-ttu-id="ea3e8-164">Affectations à des utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="ea3e8-164">User and group assignments</span></span>

<span data-ttu-id="ea3e8-165">La fonctionnalité déploiement centralisé prend actuellement en charge la majorité des groupes pris en charge par Azure Active Directory, y compris les groupes Microsoft 365, les listes de distribution et les groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-165">The Centralized Deployment feature currently supports the majority of groups supported by Azure Active Directory, including Microsoft 365 groups, distribution lists, and security groups.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ea3e8-166">Les groupes de sécurité sans extension messagerie ne sont pas actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-166">Non-mail enabled security groups are not currently supported.</span></span> 
  
<span data-ttu-id="ea3e8-167">Le déploiement centralisé prend en charge les affectations à des utilisateurs individuels, des groupes et à tous les utilisateurs du client.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-167">Centralized Deployment supports assignments to individual users, groups, and everyone in the tenant.</span></span> <span data-ttu-id="ea3e8-168">La fonctionnalité Déploiement centralisé prend en charge les utilisateurs au sein de groupes de niveau supérieur ou de groupes sans groupes parents, mais pas les utilisateurs au sein de groupes imbriqués ou qui ont des groupes parents.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-168">Centralized Deployment supports users in top-level groups or groups without parent groups, but not users in nested groups or groups that have parent groups.</span></span>
   
<span data-ttu-id="ea3e8-p110">Examinons l'exemple suivant où un complément est affecté à Nicoletta, à Ariane et au groupe Service commercial. Le Service des ventes Région ouest étant un groupe imbriqué, aucun complément n'est affecté à Noël et Jérôme.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-p110">Take a look at the following example where Sandra, Sheila, and the Sales Department group are assigned to an add-in. Because the West Coast Sales Department is a nested group, Bert and Fred aren't assigned to an add-in.</span></span>
  
![Diagramme du service des ventes](../../media/683094bb-1160-4cce-810d-26ef7264c592.png)

   
### <a name="find-out-if-a-group-contains-nested-groups"></a><span data-ttu-id="ea3e8-172">Déterminer si un groupe contient des groupes imbriqués</span><span class="sxs-lookup"><span data-stu-id="ea3e8-172">Find out if a group contains nested groups</span></span>

<span data-ttu-id="ea3e8-173">La manière la plus simple de détecter si un groupe contient des groupes imbriqués consiste à afficher la carte de visite du groupe dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-173">The easiest way to detect if a group contains nested groups is to view the group contact card within Outlook.</span></span> <span data-ttu-id="ea3e8-174">Si vous entrez le nom du groupe dans le champ **À** d’un e-mail, puis sélectionnez le nom du groupe lorsqu’il est résolu, il vous indique s’il contient des utilisateurs ou des groupes imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-174">If you enter the group name within the **To** field of an email and then select the group name when it resolves, it will show you if it contains users or nested groups.</span></span> <span data-ttu-id="ea3e8-175">Dans l'exemple ci-dessous, l'onglet **Membres** de la carte de visite Outlook du groupe Test n'affiche aucun utilisateur et seulement deux sous-groupes.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-175">In the example below, the **Members** tab of the Outlook contact card for the Test Group shows no users and only two sub groups.</span></span> 
  
![Onglet Membres de la carte de visite Outlook](../../media/d9db88c4-d752-426c-a480-b11a5b3adcd6.png)
  
<span data-ttu-id="ea3e8-p112">Vous pouvez effectuer la requête inverse en résolvant le groupe pour voir s'il est membre d'un groupe. Dans l'exemple ci-dessous, vous pouvez voir sous l'onglet **Appartenance** de la carte de visite Outlook que le Sous-groupe 1 est membre du groupe Test.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-p112">You can do the opposite query by resolving the group to see if it's a member of any group. In the example below, you can see under the **Membership** tab of the Outlook contact card that Sub Group 1 is a member of the Test Group.</span></span> 
  
![Onglet Appartenance à la carte de visite Outlook](../../media/a9f9b6ab-9c19-4822-9e3d-414ca068c42f.png)
  
<span data-ttu-id="ea3e8-p113">Vous pouvez également utiliser l'API Graph Azure Active Directory pour exécuter des requêtes afin d'obtenir la liste des groupes au sein d'un groupe. Pour plus d'informations, voir [Opérations sur les groupes | Référence de l'API Graph](/previous-versions/azure/ad/graph/api/groups-operations).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-p113">Alternately, you can use the Azure Active Directory Graph API to run queries to find the list of groups within a group. For more information, see [Operations on groups | Graph API reference](/previous-versions/azure/ad/graph/api/groups-operations).</span></span>
  
### <a name="contacting-microsoft-for-support"></a><span data-ttu-id="ea3e8-182">Contacter Microsoft pour obtenir une assistance</span><span class="sxs-lookup"><span data-stu-id="ea3e8-182">Contacting Microsoft for support</span></span>

<span data-ttu-id="ea3e8-183">Si vous ou vos utilisateurs rencontrez des problèmes lors du chargement du add-in lors de l’utilisation des applications Office pour le web (Word, Excel, etc.), qui ont été déployées de manière centralisée, vous devrez peut-être contacter le support Microsoft[(](../contact-support-for-business-products.md)découvrez comment ).</span><span class="sxs-lookup"><span data-stu-id="ea3e8-183">If you or your users encounter problems loading the add-in while using Office apps for the web (Word, Excel, etc.), which were centrally deployed, you may need to contact Microsoft support ([learn how](../contact-support-for-business-products.md)).</span></span> <span data-ttu-id="ea3e8-184">Fournissez les informations suivantes sur votre environnement Microsoft 365 dans le ticket de support.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-184">Provide the following information about your Microsoft 365 environment in the support ticket.</span></span>
  
|<span data-ttu-id="ea3e8-185">**Plateforme**</span><span class="sxs-lookup"><span data-stu-id="ea3e8-185">**Platform**</span></span>|<span data-ttu-id="ea3e8-186">**Informations de débogage**</span><span class="sxs-lookup"><span data-stu-id="ea3e8-186">**Debug information**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea3e8-187">Office</span><span class="sxs-lookup"><span data-stu-id="ea3e8-187">Office</span></span>  <br/> | <span data-ttu-id="ea3e8-188">Journaux Charles/Fiddler</span><span class="sxs-lookup"><span data-stu-id="ea3e8-188">Charles/Fiddler logs</span></span>  <br/>  <span data-ttu-id="ea3e8-189">ID de client ( [Découvrez comment](/onedrive/find-your-office-365-tenant-id.aspx))</span><span class="sxs-lookup"><span data-stu-id="ea3e8-189">Tenant ID ( [learn how](/onedrive/find-your-office-365-tenant-id.aspx))</span></span>  <br/>  <span data-ttu-id="ea3e8-190">CorrelationID.</span><span class="sxs-lookup"><span data-stu-id="ea3e8-190">CorrelationID.</span></span> <span data-ttu-id="ea3e8-191">Affichez la source de l’une des pages Office et recherchez la valeur de l’ID de corrélation et envoyez-la pour prendre en charge :</span><span class="sxs-lookup"><span data-stu-id="ea3e8-191">View the source of one of the office pages and look for the Correlation ID value and send it to support:</span></span>  <br/>`<input name=" **wdCorrelationId**" type="hidden" value=" **{BC17079E-505F-3000-C177-26A8E27EB623}**">`  <br/>  `<input name="user_id" type="hidden" value="1003bffd96933623"></form>`  <br/> |
|<span data-ttu-id="ea3e8-192">Clients riches (Windows, Mac)</span><span class="sxs-lookup"><span data-stu-id="ea3e8-192">Rich clients (Windows, Mac)</span></span>  <br/> | <span data-ttu-id="ea3e8-193">Journaux Charles/Fiddler</span><span class="sxs-lookup"><span data-stu-id="ea3e8-193">Charles/Fiddler logs</span></span>  <br/>  <span data-ttu-id="ea3e8-194">Numéros de build de l’application cliente (de préférence en tant que capture d’écran de **Fichier/Compte)**</span><span class="sxs-lookup"><span data-stu-id="ea3e8-194">Build numbers of the client app (preferably as a screenshot from **File/Account**)</span></span>  <br/> |
