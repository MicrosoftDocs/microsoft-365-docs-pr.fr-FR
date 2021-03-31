---
title: Utilisation de Microsoft Consulting Services
description: Préparation et étapes à suivre pour travailler avec MCS afin de mettre en package vos applications
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: 1441ca3305a5f3e5a83ddd5e1547812f08d7d96b
ms.sourcegitcommit: 39609c4d8c432c8e7d7a31cb35c8020e5207385b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "51445695"
---
# <a name="working-with-microsoft-consulting-services"></a><span data-ttu-id="8fd3b-104">Utilisation de Microsoft Consulting Services</span><span class="sxs-lookup"><span data-stu-id="8fd3b-104">Working with Microsoft Consulting Services</span></span>

<span data-ttu-id="8fd3b-105">Vous pouvez utiliser Microsoft Consulting Services (MCS) pour obtenir vos applications empaquetées pour une utilisation avec Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-105">You can engage with Microsoft Consulting Services (MCS) to get your apps packaged for use with Microsoft Managed Desktop.</span></span> <span data-ttu-id="8fd3b-106">Pour plus d’informations, contactez votre représentant de compte pour contacter MCS et déterminer l’étendue de votre projet d’empaquetage d’application spécifique.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-106">For exact details, work with your account representative to contact MCS and scope your specific app packaging project.</span></span>

## <a name="roles-and-responsibilities"></a><span data-ttu-id="8fd3b-107">Rôles et responsabilités</span><span class="sxs-lookup"><span data-stu-id="8fd3b-107">Roles and responsibilities</span></span>

<span data-ttu-id="8fd3b-108">Pour travailler avec l’empaquetage d’application MCS, **vous devez fournir les éléments ci-après**:</span><span class="sxs-lookup"><span data-stu-id="8fd3b-108">To work with MCS app packaging, **you must provide these elements**:</span></span>

- <span data-ttu-id="8fd3b-109">Fichiers du programme d’installation source (par exemple, setup.exe ou .msi).</span><span class="sxs-lookup"><span data-stu-id="8fd3b-109">The source installer files (for example, setup.exe or .msi).</span></span>
- <span data-ttu-id="8fd3b-110">Instructions d’installation spécifiant l’apparence de l’installation finale.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-110">The installation instructions, specifying details about how the final installation should look.</span></span> <span data-ttu-id="8fd3b-111">Par exemple, doit-il y avoir un raccourci bureau vers l’application ?</span><span class="sxs-lookup"><span data-stu-id="8fd3b-111">For example, should there be a desktop shortcut to the app?</span></span> <span data-ttu-id="8fd3b-112">Quelle doit être la visibilité de l’application ?</span><span class="sxs-lookup"><span data-stu-id="8fd3b-112">What should the app's visibility be?</span></span> <span data-ttu-id="8fd3b-113">L’application doit-elle se connecter à un serveur et, si c’est le cas, laquelle ?</span><span class="sxs-lookup"><span data-stu-id="8fd3b-113">Should the app connect to a server and if so, which one?</span></span> <span data-ttu-id="8fd3b-114">Pour plus d’informations, voir le modèle de demande [d’empaquetage d’application.](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/managed-desktop/get-ready/downloads/app-packaging-template.docx)</span><span class="sxs-lookup"><span data-stu-id="8fd3b-114">For details, see the [application packaging request template](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/managed-desktop/get-ready/downloads/app-packaging-template.docx).</span></span>
- <span data-ttu-id="8fd3b-115">Vous devez effectuer vos propres tests d’acceptation pour vérifier que l’application fonctionne comme vous le souhaitez dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-115">You must perform your own acceptance testing to verify that the app works as you need it to in your environment.</span></span>

<span data-ttu-id="8fd3b-116">**MCS s’occupe des actions ci-après :**</span><span class="sxs-lookup"><span data-stu-id="8fd3b-116">**MCS will take care of these actions:**</span></span>

- <span data-ttu-id="8fd3b-117">Vérification de l’interdiction ou de la restriction de l’application dans l’environnement Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-117">Checking whether the app is prohibited or restricted in the Microsoft Managed Desktop environment.</span></span>
- <span data-ttu-id="8fd3b-118">Test de l’installation, du démarrage et de la désinstallation de l’application pour garantir la compatibilité avec Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-118">Testing of installation, starting, and uninstallation of the app to ensure compatibility with Windows 10.</span></span> <span data-ttu-id="8fd3b-119">Si MCS découvre un problème de compatibilité, il va remettre l’application au programme [App Assure](https://docs.microsoft.com/fasttrack/products-and-capabilities#app-assure) pour correction.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-119">If MCS discovers a compatibility issue, they will hand off the app to the [App Assure](https://docs.microsoft.com/fasttrack/products-and-capabilities#app-assure) program for remediation.</span></span>
- <span data-ttu-id="8fd3b-120">Empaquetage de l’application selon vos spécifications, puis test du déploiement de l’application à l’aide de Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-120">Packaging the app to your specification and then testing app deployment by using Microsoft Intune.</span></span>

## <a name="app-delivery-schedule"></a><span data-ttu-id="8fd3b-121">Planification de remise des applications</span><span class="sxs-lookup"><span data-stu-id="8fd3b-121">App delivery schedule</span></span>

<span data-ttu-id="8fd3b-122">Démarrez le processus d’empaquetage en téléchargeant les informations de l’application sur le portail Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-122">Start the packaging process by uploading the app information to the Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="8fd3b-123">L’équipe de packaging examine les nouvelles soumissions tous les jeudis.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-123">The packaging team reviews new submissions every Thursday.</span></span> <span data-ttu-id="8fd3b-124">Après révision et empaquetage, les applications empaquetées sont livrées le vendredi suivant.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-124">After review and packaging, the packaged apps are delivered the following Friday.</span></span> <span data-ttu-id="8fd3b-125">Jusqu’à cinq applications par semaine peuvent être empaquetées pour démarrer, mais le service peut être mis à l’échelle en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-125">Up to five apps per week can be packaged to start but the service can scale to meet your needs.</span></span>

![calendrier montrant l’entrée entrante de l’application un jeudi (le 21 dans cet exemple), la validation multimédia le jour suivant, l’empaquetage le lundi suivant (le 25) et la remise de l’application le vendredi suivant (le 29)](../../media/MCS-cal.png)

<span data-ttu-id="8fd3b-127">Une fois l’application livrée, vous en serez informé.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-127">You'll be notified once the app has been delivered.</span></span> <span data-ttu-id="8fd3b-128">À ce stade, vous avez 21 jours pour effectuer des tests d’acceptation et approuver le travail dans le portail Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-128">At that point, you have 21 days to perform acceptance testing and approve the work in the Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="8fd3b-129">Si vous découvrez un problème avec l’application lors de vos tests d’acceptation, rejetez l’application dans le portail Bureau géré Microsoft et vous serez connecté par courrier électronique à un packageur MCS pour comprendre et résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-129">If discover some problem with the app during your acceptance testing, reject the app in the Microsoft Managed Desktop portal and you will be connected via email with an MCS packager to understand and resolve the issue.</span></span>

## <a name="testing-accounts-and-environment"></a><span data-ttu-id="8fd3b-130">Test des comptes et de l’environnement</span><span class="sxs-lookup"><span data-stu-id="8fd3b-130">Testing accounts and environment</span></span>

<span data-ttu-id="8fd3b-131">Pour que l’équipe de packaging termine la migration vers Microsoft Intune, nous vous recommandons de fournir certaines autorisations :</span><span class="sxs-lookup"><span data-stu-id="8fd3b-131">For the packaging team to complete the migration to Microsoft Intune, we recommend that you provide certain permissions:</span></span>
 
-   <span data-ttu-id="8fd3b-132">Accès aux fonctionnalités de déploiement d’application de Microsoft Intune pour le packager afin d’ajouter et d’affecter l’application</span><span class="sxs-lookup"><span data-stu-id="8fd3b-132">Access to Microsoft Intune’s App Deployment capabilities for the packager to add and assign the app</span></span> 
-   <span data-ttu-id="8fd3b-133">Tester les groupes, les comptes d’utilisateur et les licences des packageurs pour pouvoir tester les applications</span><span class="sxs-lookup"><span data-stu-id="8fd3b-133">Test groups, user accounts, and licenses for the packagers to be able to test the apps</span></span>

<span data-ttu-id="8fd3b-134">MCS utilisera ces autorisations pour effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8fd3b-134">MCS will use those permissions to perform the following actions:</span></span>
 
-   <span data-ttu-id="8fd3b-135">S’assurer que l’application fonctionne sur une machine virtuelle configurée pour le Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="8fd3b-135">Ensuring that the app works on virtual machine configured for Microsoft Managed Desktop</span></span>
-   <span data-ttu-id="8fd3b-136">Téléchargement de l’application vers Microsoft Intune pour le déploiement vers vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8fd3b-136">Uploading the app to Microsoft Intune for deployment to your users</span></span>

<span data-ttu-id="8fd3b-137">Sans ces autorisations, mcS peut avancer, mais il ne pourra pas télécharger les applications vers votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8fd3b-137">Without these permissions, it is possible for MCS to move forward, but they will not be able to upload the applications to your environment.</span></span>
