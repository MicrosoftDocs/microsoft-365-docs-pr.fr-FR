---
title: Déterminer si le déploiement centralisé des compléments fonctionne pour votre organisation
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b4527d49-4073-4b43-8274-31b7a3166f92
description: Déterminez si votre client et vos utilisateurs satisfont à la configuration requise, afin que vous puissiez utiliser un déploiement centralisé pour déployer des compléments Office.
ms.openlocfilehash: 0fcdb9901c708842470f72106ab4eea20ff8b17e
ms.sourcegitcommit: bd8d55f82ca008af1b93a9bb4d1545f68e8188ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2020
ms.locfileid: "44011722"
---
# <a name="determine-if-centralized-deployment-of-add-ins-works-for-your-organization"></a><span data-ttu-id="a9720-103">Déterminer si le déploiement centralisé des compléments fonctionne pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="a9720-103">Determine if Centralized Deployment of add-ins works for your organization</span></span>

<span data-ttu-id="a9720-104">Le déploiement centralisé est la méthode recommandée et la plus riche en fonctionnalités pour la plupart des clients qui déploient des compléments Office pour les utilisateurs et les groupes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a9720-104">Centralized Deployment is the recommended and most feature-rich way for most customers to deploy Office add-ins to users and groups within your organization.</span></span> <span data-ttu-id="a9720-105">Si vous êtes administrateur, utilisez ce guide pour déterminer si votre client et vos utilisateurs satisfont à la configuration requise afin que vous puissiez utiliser un déploiement centralisé.</span><span class="sxs-lookup"><span data-stu-id="a9720-105">If you're an admin, use this guidance to determine if your tenant and users meet the requirements so that you can use Centralized Deployment.</span></span>
<span data-ttu-id="a9720-106">Le déploiement centralisé prend en charge les applications Windows, Mac, iOS, Android et en ligne.</span><span class="sxs-lookup"><span data-stu-id="a9720-106">Centralized Deployment supports Windows, Mac, iOS, Android and Online Office apps.</span></span>
<span data-ttu-id="a9720-107">Un complément peut prendre jusqu’à 12 heures pour s’afficher pour le client pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a9720-107">It can take up to 12 hours for an add-in to show up for client for all users.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="a9720-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9720-108">Requirements</span></span>

<span data-ttu-id="a9720-109">Le déploiement centralisé des compléments nécessite que les utilisateurs utilisent les applications Microsoft 365 pour Enterprise (et sont connectés à Office à l’aide de leur ID d’organisation) et disposent de boîtes aux lettres Exchange Online et Exchange Online actives.</span><span class="sxs-lookup"><span data-stu-id="a9720-109">Centralized deployment of add-ins requires that the users are using Microsoft 365 Apps for enterprise (and are signed into Office using their organizational ID), and have Exchange Online and active Exchange Online mailboxes.</span></span> <span data-ttu-id="a9720-110">Le répertoire de votre abonnement doit être dans ou fédéré à Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9720-110">Your subscription directory must either be in, or federated to Azure Active Directory.</span></span>
<span data-ttu-id="a9720-111">Vous pouvez afficher les conditions requises spécifiques pour Office et Exchange ci-dessous, ou utiliser le [Vérificateur de compatibilité de déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide#office-365-centralized-deployment-compatibility-checker).</span><span class="sxs-lookup"><span data-stu-id="a9720-111">You can view specific requirements for Office and Exchange below, or use the [Centralized Deployment Compatibility Checker](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide#office-365-centralized-deployment-compatibility-checker).</span></span>

<span data-ttu-id="a9720-112">La fonctionnalité Déploiement centralisé ne prend pas en charge ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="a9720-112">Centralized Deployment doesn't support the following:</span></span>
  
- <span data-ttu-id="a9720-113">des compléments ciblant Word, Excel ou PowerPoint dans Office 2013 ;</span><span class="sxs-lookup"><span data-stu-id="a9720-113">Add-ins that target Word, Excel, or PowerPoint in Office 2013</span></span>
    
- <span data-ttu-id="a9720-114">un service d'annuaire local ;</span><span class="sxs-lookup"><span data-stu-id="a9720-114">An on-premises directory service</span></span>
    
- <span data-ttu-id="a9720-115">le déploiement de compléments vers SharePoint ;</span><span class="sxs-lookup"><span data-stu-id="a9720-115">Add-in deployment to SharePoint</span></span>  

- <span data-ttu-id="a9720-116">Applications teams</span><span class="sxs-lookup"><span data-stu-id="a9720-116">Teams apps</span></span>
   
- <span data-ttu-id="a9720-117">le déploiement de compléments COM (Component Object Model) ou Visual Studio Tools pour Office (VSTO).</span><span class="sxs-lookup"><span data-stu-id="a9720-117">Deployment of Component Object Model (COM) or Visual Studio Tools for Office (VSTO) add-ins</span></span>
    
- <span data-ttu-id="a9720-118">Déploiements de Microsoft 365 qui n’incluent pas Exchange, comme Microsoft 365 apps pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="a9720-118">Deployments of Microsoft 365 that do not include Exchange such as Microsoft 365 Apps for business</span></span>

### <a name="office-requirements"></a><span data-ttu-id="a9720-119">Configuration requise pour Office</span><span class="sxs-lookup"><span data-stu-id="a9720-119">Office Requirements</span></span>

- <span data-ttu-id="a9720-120">Pour les compléments Word, Excel et PowerPoint, vos utilisateurs doivent utiliser l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a9720-120">For Word, Excel, and PowerPoint add-ins, your users must be using one of the following:</span></span>
  - <span data-ttu-id="a9720-121">Sur un appareil Windows, version 1704 ou ultérieure de Microsoft 365 apps pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="a9720-121">On a Windows device, Version 1704 or later of Microsoft 365 Apps for enterprise.</span></span>
  - <span data-ttu-id="a9720-122">Sur un Mac, version 15,34 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a9720-122">On a Mac, Version 15.34 or later.</span></span>

- <span data-ttu-id="a9720-123">Pour Outlook, vos utilisateurs doivent utiliser l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a9720-123">For Outlook, your users must be using one of the following:</span></span> 
  - <span data-ttu-id="a9720-124">Version 1701 ou ultérieure des applications Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="a9720-124">Version 1701 or later of Microsoft 365 Apps for enterprise.</span></span>
  - <span data-ttu-id="a9720-125">Version 1808 ou ultérieure d’Office professionnel plus 2019 ou Office standard 2019.</span><span class="sxs-lookup"><span data-stu-id="a9720-125">Version 1808 or later of Office Professional Plus 2019 or Office Standard 2019.</span></span>
  - <span data-ttu-id="a9720-126">Version 16.0.4494.1000 ou ultérieure d’Office professionnel plus 2016 (MSI) ou Office standard 2016 (MSI)\*</span><span class="sxs-lookup"><span data-stu-id="a9720-126">Version 16.0.4494.1000 or later of Office Professional Plus 2016 (MSI) or Office Standard 2016 (MSI)\*</span></span>
  - <span data-ttu-id="a9720-127">Version 15.0.4937.1000 ou ultérieure d’Office professionnel plus 2013 (MSI) ou Office standard 2013 (MSI)\*</span><span class="sxs-lookup"><span data-stu-id="a9720-127">Version 15.0.4937.1000 or later of Office Professional Plus 2013 (MSI) or Office Standard 2013 (MSI)\*</span></span>
  - <span data-ttu-id="a9720-128">Version 16.0.9318.1000 ou ultérieure d’Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="a9720-128">Version 16.0.9318.1000 or later of Office 2016 for Mac</span></span> 
- <span data-ttu-id="a9720-129">Version 2.75.0 ou ultérieure d’Outlook Mobile pour iOS</span><span class="sxs-lookup"><span data-stu-id="a9720-129">Version 2.75.0 or later of Outlook mobile for iOS</span></span> 
- <span data-ttu-id="a9720-130">Version 2.2.145 ou ultérieure d’Outlook Mobile pour Android</span><span class="sxs-lookup"><span data-stu-id="a9720-130">Version 2.2.145 or later of Outlook mobile for Android</span></span> 
    
    <span data-ttu-id="a9720-131">\* Les versions MSI d’Outlook affichent les compléments installés par l’administrateur dans le ruban Outlook approprié, et non dans la section « mes compléments ».</span><span class="sxs-lookup"><span data-stu-id="a9720-131">\*MSI versions of Outlook show admin-installed add-ins in the appropriate Outlook ribbon, not the "My add-ins" section.</span></span>
    

#### <a name="find-out-if-microsoft-365-apps-for-enterprise-is-installed"></a><span data-ttu-id="a9720-132">Déterminer si les applications Microsoft 365 pour les entreprises sont installées</span><span class="sxs-lookup"><span data-stu-id="a9720-132">Find out if Microsoft 365 Apps for enterprise is installed</span></span>

<span data-ttu-id="a9720-133">Pour utiliser les applications Microsoft 365 pour Enterprise, un utilisateur doit disposer d’un compte Microsoft 365 et avoir reçu une licence.</span><span class="sxs-lookup"><span data-stu-id="a9720-133">To use Microsoft 365 Apps for enterprise, a user must have an Microsoft 365 account and must have been assigned a license.</span></span> <span data-ttu-id="a9720-134">Pour plus d’informations, reportez-vous à la rubrique [Overview of Microsoft 365 Apps for Enterprise](https://go.microsoft.com/fwlink/p/?linkid=846328).</span><span class="sxs-lookup"><span data-stu-id="a9720-134">For more information, see [Overview of Microsoft 365 Apps for enterprise](https://go.microsoft.com/fwlink/p/?linkid=846328).</span></span>

<span data-ttu-id="a9720-135">Le moyen le plus simple de détecter si les applications Microsoft 365 pour Enterprise sont installées sur un utilisateur et de l’utiliser récemment est d’utiliser le rapport des activations de Microsoft Office, qui est disponible dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a9720-135">The simplest way to detect if a user has Microsoft 365 Apps for enterprise installed and has been using it recently is to use the Microsoft Office Activations report, which is available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="a9720-136">Le rapport fournit la liste de tous les utilisateurs qui ont activé les applications Microsoft 365 pour les entreprises au cours des 7, 30, 90 ou 180 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="a9720-136">The report provides a list of all users who have activated Microsoft 365 Apps for enterprise within the last 7 days, 30 days, 90 days, or 180 days.</span></span> <span data-ttu-id="a9720-137">À des fins de déploiement centralisé, les activations de bureau pour Windows ou Mac sont les colonnes importantes dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="a9720-137">For centralized deployment purposes, the desktop activations for Windows or Mac are the important columns in the report.</span></span> <span data-ttu-id="a9720-138">Vous pouvez exporter le rapport vers Excel.</span><span class="sxs-lookup"><span data-stu-id="a9720-138">You can export the report to Excel.</span></span> <span data-ttu-id="a9720-139">Pour plus d’informations sur le rapport, reportez-vous à [la rubrique rapports microsoft 365 dans le centre d’administration-activations de Microsoft Office](../activity-reports/microsoft-office-activations.md).</span><span class="sxs-lookup"><span data-stu-id="a9720-139">For more information about the report, see [Microsoft 365 Reports in the Admin Center - Microsoft Office activations](../activity-reports/microsoft-office-activations.md).</span></span>
  
<span data-ttu-id="a9720-140">Si vous ne souhaitez pas utiliser le rapport d’activation, vous pouvez demander à un utilisateur d’ouvrir une application Office telle que Word sur son ordinateur, puis choisir le **compte**de **fichier** \> .</span><span class="sxs-lookup"><span data-stu-id="a9720-140">If you don't want to use the Activations report, you can ask a user to open an Office application such as Word on their machine, and then choose **File** \> **Account**.</span></span> <span data-ttu-id="a9720-141">Sous **informations sur le produit**, vous devez voir le **produit abonnement** et les **applications Microsoft 365 pour entreprise**, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="a9720-141">Under **Product Information**, you should see **Subscription Product** and **Microsoft Microsoft 365 Apps for enterprise**, as shown in the following image.</span></span>

![Informations sur le produit dans une application Office](../../media/4bff2bb8-0690-4d22-ac1f-b8881807fa39.png)
  
<span data-ttu-id="a9720-143">Pour obtenir de l’aide concernant les applications Microsoft 365 pour les entreprises, consultez la rubrique [Troubleshooting Tips for microsoft 365 Apps for Enterprise](https://go.microsoft.com/fwlink/p/?linkid=846339).</span><span class="sxs-lookup"><span data-stu-id="a9720-143">For help with Microsoft 365 Apps for enterprise, see [Troubleshooting tips for Microsoft 365 Apps for enterprise](https://go.microsoft.com/fwlink/p/?linkid=846339).</span></span>


### <a name="exchange-online-requirements"></a><span data-ttu-id="a9720-144">Configuration requise pour Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a9720-144">Exchange Online requirements</span></span>

<span data-ttu-id="a9720-145">Microsoft Exchange stocke les manifestes des compléments au sein du client de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a9720-145">Microsoft Exchange stores the add-in manifests within your organization's tenant.</span></span> <span data-ttu-id="a9720-146">L’administrateur déployant des compléments et les utilisateurs qui les reçoivent doivent se trouver sur une version d’Exchange Online qui prend en charge l’authentification OAuth.</span><span class="sxs-lookup"><span data-stu-id="a9720-146">The admin deploying add-ins and the users receiving those add-ins must be on a version of Exchange Online that supports OAuth authentication.</span></span>
  
<span data-ttu-id="a9720-p107">Pour connaître la configuration utilisée, consultez l'administrateur Exchange de votre organisation. Vous pouvez vérifier la connectivité OAuth de chaque utilisateur à l'aide de l'applet de commande PowerShell [Test-OAuthConnectivity](https://go.microsoft.com/fwlink/p/?linkid=846351).</span><span class="sxs-lookup"><span data-stu-id="a9720-p107">Check with your organization's Exchange admin to find out which configuration is in use. OAuth connectivity per user can be verified by using the [Test-OAuthConnectivity](https://go.microsoft.com/fwlink/p/?linkid=846351) PowerShell cmdlet.</span></span> 


### <a name="centralized-deployment-compatibility-checker"></a><span data-ttu-id="a9720-149">Vérificateur de compatibilité de déploiement centralisé</span><span class="sxs-lookup"><span data-stu-id="a9720-149">Centralized Deployment Compatibility Checker</span></span>

<span data-ttu-id="a9720-150">À l’aide du vérificateur de compatibilité du déploiement centralisé, vous pouvez vérifier si les utilisateurs de votre client sont configurés pour utiliser un déploiement centralisé pour Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="a9720-150">Using the Centralized Deployment Compatibility Checker, you can verify whether the users on your tenant are set up to use Centralized Deployment for Word, Excel and PowerPoint.</span></span> <span data-ttu-id="a9720-151">Le vérificateur de compatibilité n'est pas requis pour la prise en charge d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="a9720-151">The Compatibility Checker is not required for Outlook support.</span></span> <span data-ttu-id="a9720-152">Téléchargez le vérificateur de compatibilité [ici](https://aka.ms/officeaddindeploymentorgcompatibilitychecker).</span><span class="sxs-lookup"><span data-stu-id="a9720-152">Download the compatibility checker [here](https://aka.ms/officeaddindeploymentorgcompatibilitychecker).</span></span>
  
#### <a name="run-the-compatibility-checker"></a><span data-ttu-id="a9720-153">Exécuter le vérificateur de compatibilité</span><span class="sxs-lookup"><span data-stu-id="a9720-153">Run the compatibility checker</span></span>
  
1. <span data-ttu-id="a9720-154">Démarrez une fenêtre PowerShell. exe avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="a9720-154">Start an elevated PowerShell.exe window.</span></span>
    
2. <span data-ttu-id="a9720-155">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a9720-155">Run the following command:</span></span>

```powershell
Import-Module O365CompatibilityChecker
```
    
3. <span data-ttu-id="a9720-156">Exécutez la commande **Invoke-CompatabilityCheck** :</span><span class="sxs-lookup"><span data-stu-id="a9720-156">Run the **Invoke-CompatabilityCheck** command:</span></span>

```powershell
Invoke-CompatibilityCheck
```
   <span data-ttu-id="a9720-157">qui vous demande *_TenantDomain_* (par exemple, *TailspinToysIncorporated. onmicrosoft.</span> com*) et *_TENANTADMIN_* (utilisez vos informations d’identification d’administrateur général), puis demande le consentement.</span><span class="sxs-lookup"><span data-stu-id="a9720-157">which prompts you for  *_TenantDomain_* (for example, *TailspinToysIncorporated.onmicrosoft.</span>com*) and  *_TenantAdmin_* credentials (use your global admin credentials), and then requests consent.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a9720-158">Selon le nombre d'utilisateurs dans votre client, l'exécution du vérificateur peut prendre quelques minutes ou plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="a9720-158">Depending on the number of users in your tenant, the checker could complete in minutes or hours.</span></span> 
  
<span data-ttu-id="a9720-159">Une fois l'exécution de l'outil terminée, celui-ci génère un fichier de sortie dans un format séparé par des virgules (.csv).</span><span class="sxs-lookup"><span data-stu-id="a9720-159">When the tool finishes running, it produces an output file in comma-separated (.csv) format.</span></span> <span data-ttu-id="a9720-160">Par défaut, le fichier est enregistré dans **C:\Windows\System32** .</span><span class="sxs-lookup"><span data-stu-id="a9720-160">The file is saved to **C:\windows\system32** by default.</span></span> <span data-ttu-id="a9720-161">Le fichier de sortie contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a9720-161">The output file contains the following information:</span></span>
  
- <span data-ttu-id="a9720-162">Nom d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="a9720-162">User Name</span></span>
    
- <span data-ttu-id="a9720-163">ID d'utilisateur (adresse de courrier de l'utilisateur)</span><span class="sxs-lookup"><span data-stu-id="a9720-163">User ID (User's email address)</span></span>
    
- <span data-ttu-id="a9720-164">Déploiement centralisé prêt - Si les autres éléments sont vérifiés</span><span class="sxs-lookup"><span data-stu-id="a9720-164">Centralized Deployment ready - If the remaining items are true</span></span>
    
- <span data-ttu-id="a9720-165">Plan Office : le plan d’Office pour lequel il existe une licence pour</span><span class="sxs-lookup"><span data-stu-id="a9720-165">Office plan - The plan of Office they are licensed for</span></span>
    
- <span data-ttu-id="a9720-166">Activation d'Office - Si l'utilisateur a activé Office</span><span class="sxs-lookup"><span data-stu-id="a9720-166">Office Activated - If they have activated Office</span></span>
    
- <span data-ttu-id="a9720-167">Boîte aux lettres prise en charge - Si l'utilisateur a une boîte aux lettres OAuth</span><span class="sxs-lookup"><span data-stu-id="a9720-167">Supported Mailbox - If they are on an OAuth-enabled mailbox</span></span>


  
## <a name="user-and-group-assignments"></a><span data-ttu-id="a9720-168">Affectations à des utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="a9720-168">User and group assignments</span></span>

<span data-ttu-id="a9720-169">La fonctionnalité de déploiement centralisé prend actuellement en charge la majorité des groupes pris en charge par Azure Active Directory, y compris les groupes Microsoft 365, les listes de distribution et les groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a9720-169">The Centralized Deployment feature currently supports the majority of groups supported by Azure Active Directory, including Microsoft 365 groups, distribution lists, and security groups.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a9720-170">Les groupes de sécurité sans extension messagerie ne sont pas actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a9720-170">Non-mail enabled security groups are not currently supported.</span></span> 
  
<span data-ttu-id="a9720-171">Le déploiement centralisé prend en charge les affectations à des utilisateurs individuels, des groupes et tout le monde dans le client.</span><span class="sxs-lookup"><span data-stu-id="a9720-171">Centralized Deployment supports assignments to individual users, groups, and everyone in the tenant.</span></span> <span data-ttu-id="a9720-172">La fonctionnalité Déploiement centralisé prend en charge les utilisateurs au sein de groupes de niveau supérieur ou de groupes sans groupes parents, mais pas les utilisateurs au sein de groupes imbriqués ou qui ont des groupes parents.</span><span class="sxs-lookup"><span data-stu-id="a9720-172">Centralized Deployment supports users in top-level groups or groups without parent groups, but not users in nested groups or groups that have parent groups.</span></span>
   
<span data-ttu-id="a9720-p111">Examinons l'exemple suivant où un complément est affecté à Nicoletta, à Ariane et au groupe Service commercial. Le Service des ventes Région ouest étant un groupe imbriqué, aucun complément n'est affecté à Noël et Jérôme.</span><span class="sxs-lookup"><span data-stu-id="a9720-p111">Take a look at the following example where Sandra, Sheila, and the Sales Department group are assigned to an add-in. Because the West Coast Sales Department is a nested group, Bert and Fred aren't assigned to an add-in.</span></span>
  
![Diagramme du service des ventes](../../media/683094bb-1160-4cce-810d-26ef7264c592.png)

   
### <a name="find-out-if-a-group-contains-nested-groups"></a><span data-ttu-id="a9720-176">Déterminer si un groupe contient des groupes imbriqués</span><span class="sxs-lookup"><span data-stu-id="a9720-176">Find out if a group contains nested groups</span></span>

<span data-ttu-id="a9720-177">La manière la plus simple de détecter si un groupe contient des groupes imbriqués consiste à afficher la carte de visite du groupe dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="a9720-177">The easiest way to detect if a group contains nested groups is to view the group contact card within Outlook.</span></span> <span data-ttu-id="a9720-178">Si vous entrez le nom du groupe dans le champ **à** d’un e-mail, puis que vous sélectionnez le nom du groupe lorsqu’il est résolu, il vous indique s’il contient des utilisateurs ou des groupes imbriqués.</span><span class="sxs-lookup"><span data-stu-id="a9720-178">If you enter the group name within the **To** field of an email and then select the group name when it resolves, it will show you if it contains users or nested groups.</span></span> <span data-ttu-id="a9720-179">Dans l'exemple ci-dessous, l'onglet **Membres** de la carte de visite Outlook du groupe Test n'affiche aucun utilisateur et seulement deux sous-groupes.</span><span class="sxs-lookup"><span data-stu-id="a9720-179">In the example below, the **Members** tab of the Outlook contact card for the Test Group shows no users and only two sub groups.</span></span> 
  
![Onglet membres de la carte de visite Outlook](../../media/d9db88c4-d752-426c-a480-b11a5b3adcd6.png)
  
<span data-ttu-id="a9720-p113">Vous pouvez effectuer la requête inverse en résolvant le groupe pour voir s'il est membre d'un groupe. Dans l'exemple ci-dessous, vous pouvez voir sous l'onglet **Appartenance** de la carte de visite Outlook que le Sous-groupe 1 est membre du groupe Test.</span><span class="sxs-lookup"><span data-stu-id="a9720-p113">You can do the opposite query by resolving the group to see if it's a member of any group. In the example below, you can see under the **Membership** tab of the Outlook contact card that Sub Group 1 is a member of the Test Group.</span></span> 
  
![Onglet appartenance de la carte de visite Outlook](../../media/a9f9b6ab-9c19-4822-9e3d-414ca068c42f.png)
  
<span data-ttu-id="a9720-p114">Vous pouvez également utiliser l'API Graph Azure Active Directory pour exécuter des requêtes afin d'obtenir la liste des groupes au sein d'un groupe. Pour plus d'informations, voir [Opérations sur les groupes | Référence de l'API Graph](https://go.microsoft.com/fwlink/p/?linkid=846342).</span><span class="sxs-lookup"><span data-stu-id="a9720-p114">Alternately, you can use the Azure Active Directory Graph API to run queries to find the list of groups within a group. For more information, see [Operations on groups | Graph API reference](https://go.microsoft.com/fwlink/p/?linkid=846342).</span></span>
  
### <a name="contacting-microsoft-for-support"></a><span data-ttu-id="a9720-186">Contacter Microsoft pour obtenir une assistance</span><span class="sxs-lookup"><span data-stu-id="a9720-186">Contacting Microsoft for support</span></span>

<span data-ttu-id="a9720-187">Si vous ou vos utilisateurs rencontrez des problèmes lors du chargement du complément lors de l’utilisation d’applications Office pour le Web (Word, Excel, etc.), qui ont été déployées de manière centralisée, vous devrez peut-être contacter le support technique Microsoft ([Découvrez comment](../contact-support-for-business-products.md)).</span><span class="sxs-lookup"><span data-stu-id="a9720-187">If you or your users encounter problems loading the add-in while using Office apps for the web (Word, Excel, etc.), which were centrally deployed, you may need to contact Microsoft support ([learn how](../contact-support-for-business-products.md)).</span></span> <span data-ttu-id="a9720-188">Fournissez les informations suivantes sur votre environnement Microsoft 365 dans le ticket de support.</span><span class="sxs-lookup"><span data-stu-id="a9720-188">Provide the following information about your Microsoft 365 environment in the support ticket.</span></span>
  
|<span data-ttu-id="a9720-189">**Plateforme**</span><span class="sxs-lookup"><span data-stu-id="a9720-189">**Platform**</span></span>|<span data-ttu-id="a9720-190">**Informations de débogage**</span><span class="sxs-lookup"><span data-stu-id="a9720-190">**Debug information**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a9720-191">Office</span><span class="sxs-lookup"><span data-stu-id="a9720-191">Office</span></span>  <br/> | <span data-ttu-id="a9720-192">Journaux Charles/Fiddler</span><span class="sxs-lookup"><span data-stu-id="a9720-192">Charles/Fiddler logs</span></span>  <br/>  <span data-ttu-id="a9720-193">ID de client ( [Découvrez comment](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b.aspx))</span><span class="sxs-lookup"><span data-stu-id="a9720-193">Tenant ID ( [learn how](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b.aspx))</span></span>  <br/>  <span data-ttu-id="a9720-194">Corrélation.</span><span class="sxs-lookup"><span data-stu-id="a9720-194">CorrelationID.</span></span> <span data-ttu-id="a9720-195">Affichez la source d’une des pages Office et recherchez la valeur de l’ID de corrélation et envoyez-la au support technique :</span><span class="sxs-lookup"><span data-stu-id="a9720-195">View the source of one of the office pages and look for the Correlation ID value and send it to support:</span></span>  <br/>`<input name=" **wdCorrelationId**" type="hidden" value=" **{BC17079E-505F-3000-C177-26A8E27EB623}**">`  <br/>  `<input name="user_id" type="hidden" value="1003bffd96933623"></form>`  <br/> |
|<span data-ttu-id="a9720-196">Clients riches (Windows, Mac)</span><span class="sxs-lookup"><span data-stu-id="a9720-196">Rich clients (Windows, Mac)</span></span>  <br/> | <span data-ttu-id="a9720-197">Journaux Charles/Fiddler</span><span class="sxs-lookup"><span data-stu-id="a9720-197">Charles/Fiddler logs</span></span>  <br/>  <span data-ttu-id="a9720-198">Numéros de build de l’application cliente (de préférence sous la forme d’une capture d’écran du **fichier/compte**)</span><span class="sxs-lookup"><span data-stu-id="a9720-198">Build numbers of the client app (preferably as a screenshot from **File/Account**)</span></span>  <br/> |
   

