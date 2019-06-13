---
title: Utilisation de Microsoft Consulting Services
description: préparation et étapes à suivre pour utiliser MCS pour empaqueter vos applications
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation, applications, MCS, Packaging
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 39a5102d045d9ed79b631a3b477bd1c72dea76de
ms.sourcegitcommit: 498340389e1c34f49f0b2da382c23c8d5334ae47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "34918723"
---
# <a name="working-with-microsoft-consulting-services"></a><span data-ttu-id="6eef9-104">Utilisation de Microsoft Consulting Services</span><span class="sxs-lookup"><span data-stu-id="6eef9-104">Working with Microsoft Consulting Services</span></span>

<span data-ttu-id="6eef9-105">Vous pouvez vous exercer avec Microsoft Consulting Services (MCS) pour obtenir les applications à utiliser avec le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6eef9-105">You can engage with Microsoft Consulting Services (MCS) to get your apps packaged for use with Microsoft Managed Desktop.</span></span> <span data-ttu-id="6eef9-106">Pour obtenir des informations exactes, collaborez avec votre représentant commercial pour contacter MCS et étendre votre projet d’empaquetage d’application spécifique.</span><span class="sxs-lookup"><span data-stu-id="6eef9-106">For exact details, work with your account representative to contact MCS and scope your specific app packaging project.</span></span>

## <a name="roles-and-responsibilities"></a><span data-ttu-id="6eef9-107">Rôles et responsabilités</span><span class="sxs-lookup"><span data-stu-id="6eef9-107">Roles and responsibilities</span></span>

<span data-ttu-id="6eef9-108">Pour utiliser l’empaquetage d’applications MCS, **vous devez fournir les éléments**suivants:</span><span class="sxs-lookup"><span data-stu-id="6eef9-108">To work with MCS app packaging, **you must provide these elements**:</span></span>

- <span data-ttu-id="6eef9-109">Fichiers du programme d’installation source (par exemple, Setup. exe ou. msi).</span><span class="sxs-lookup"><span data-stu-id="6eef9-109">The source installer files (e.g., setup.exe or .msi).</span></span>
- <span data-ttu-id="6eef9-110">Les instructions d’installation, spécifiant des détails sur la façon dont l’installation finale doit ressembler.</span><span class="sxs-lookup"><span data-stu-id="6eef9-110">The installation instructions, specifying details about how the final installation should look.</span></span> <span data-ttu-id="6eef9-111">Par exemple, un raccourci Bureau doit-il exister vers l’application?</span><span class="sxs-lookup"><span data-stu-id="6eef9-111">For example, should there be a desktop shortcut to the app?</span></span> <span data-ttu-id="6eef9-112">Quelle doit être la visibilité de l’application?</span><span class="sxs-lookup"><span data-stu-id="6eef9-112">What should the app's visibility be?</span></span> <span data-ttu-id="6eef9-113">L’application doit-elle se connecter à un serveur et, le cas échéant, laquelle?</span><span class="sxs-lookup"><span data-stu-id="6eef9-113">Should the app connect to a server and if so, which one?</span></span> <!--For details, see the [application packaging request template](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/managed-desktop/get-ready/downloads/app-packaging-template.docx). -->
- <span data-ttu-id="6eef9-114">Vous devez effectuer vos propres tests d’acceptation pour vérifier que l’application fonctionne comme vous le souhaitez dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6eef9-114">You must perform your own acceptance testing to verify that the app works as you need it to in your environment.</span></span>

<span data-ttu-id="6eef9-115">**MCS se chargera des actions suivantes:**</span><span class="sxs-lookup"><span data-stu-id="6eef9-115">**MCS will take care of these actions:**</span></span>

- <span data-ttu-id="6eef9-116">Vérifier si l’application est interdite ou restreinte dans l’environnement de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6eef9-116">Checking whether the app is prohibited or restricted in the Microsoft Managed Desktop environment.</span></span>
- <span data-ttu-id="6eef9-117">Test de l’installation, du démarrage et de la désinstallation de l’application pour garantir la compatibilité avec Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6eef9-117">Testing of installation, starting, and uninstallation of the app to ensure compatibility with Windows 10.</span></span> <span data-ttu-id="6eef9-118">Si MCS identifie un problème de compatibilité, il remet l’application à l' [application de bureau pour garantir](https://docs.microsoft.com/fasttrack/win-10-desktop-app-assure) le programme de correction.</span><span class="sxs-lookup"><span data-stu-id="6eef9-118">If MCS discovers a compatibility issue, they will hand off the app to the [Desktop App Assure](https://docs.microsoft.com/fasttrack/win-10-desktop-app-assure) program for remediation.</span></span>
- <span data-ttu-id="6eef9-119">Empaquetez l’application dans votre spécification, puis testez le déploiement de l’application à l’aide de Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="6eef9-119">Packaging the app to your specification and then testing app deployment by using Microsoft Intune.</span></span>

## <a name="app-delivery-schedule"></a><span data-ttu-id="6eef9-120">Calendrier de remise d’application</span><span class="sxs-lookup"><span data-stu-id="6eef9-120">App delivery schedule</span></span>

<span data-ttu-id="6eef9-121">Démarrez le processus d’empaquetage en téléchargeant les informations de l’application dans le portail de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6eef9-121">Start the packaging process by uploading the app information to the Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="6eef9-122">L’équipe de Packaging examine les nouvelles soumissions tous les jeudis.</span><span class="sxs-lookup"><span data-stu-id="6eef9-122">The packaging team reviews new submissions every Thursday.</span></span> <span data-ttu-id="6eef9-123">Après la révision et l’empaquetage, les applications empaquetées sont fournies le vendredi suivant.</span><span class="sxs-lookup"><span data-stu-id="6eef9-123">After review and packaging, the packaged apps are delivered the following Friday.</span></span> <span data-ttu-id="6eef9-124">Jusqu’à cinq applications par semaine peuvent être empaquetées pour démarrer, mais le service peut évoluer pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6eef9-124">Up to five apps per week can be packaged to start but the service can scale to meet your needs.</span></span>

![calendrier illustrant les dates de révision, d’empaquetage et de livraison de l’application](images/MCS-cal.png)

<span data-ttu-id="6eef9-126">Vous serez informé une fois que l’application aura été livrée.</span><span class="sxs-lookup"><span data-stu-id="6eef9-126">You'll be notified once the app has been delivered.</span></span> <span data-ttu-id="6eef9-127">À ce stade, vous disposez de 21 jours pour effectuer des tests d’acceptation et vous déconnecter du travail dans le portail de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6eef9-127">At that point, you have 21 days to perform acceptance testing and sign off on the work in the Microsoft Managed Desktop portal.</span></span> <span data-ttu-id="6eef9-128">Si vous rencontrez un problème avec l’application pendant le test d’acceptation, rejetez l’application dans le portail de bureau géré Microsoft et vous serez connecté par courrier électronique avec un gestionnaire de package MCS pour comprendre et résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="6eef9-128">If discover some problem with the app during your acceptance testing, reject the app in the Microsoft Managed Desktop portal and you will be connected via email with an MCS packager to understand and resolve the issue.</span></span>

## <a name="testing-accounts-and-environment"></a><span data-ttu-id="6eef9-129">Test des comptes et de l’environnement</span><span class="sxs-lookup"><span data-stu-id="6eef9-129">Testing accounts and environment</span></span>

<span data-ttu-id="6eef9-130">Pour que l’équipe de Packaging termine la migration vers Microsoft Intune, nous vous recommandons de fournir certaines autorisations:</span><span class="sxs-lookup"><span data-stu-id="6eef9-130">For the packaging team to complete the migration to Microsoft Intune we recommend that you provide certain permissions:</span></span>
 
-   <span data-ttu-id="6eef9-131">Accès aux fonctionnalités de déploiement d’applications de Microsoft Intune pour le gestionnaire de package afin d’ajouter et d’affecter l’application</span><span class="sxs-lookup"><span data-stu-id="6eef9-131">Access to Microsoft Intune’s App Deployment capabilities for the packager to add and assign the app</span></span> 
-   <span data-ttu-id="6eef9-132">Les groupes de test, les comptes d’utilisateur et les licences pour les logiciels d’empaquetage pour pouvoir tester les applications</span><span class="sxs-lookup"><span data-stu-id="6eef9-132">Test groups, user accounts, and licenses for the packagers to be able to test the apps</span></span>

<span data-ttu-id="6eef9-133">MCS utilise ces autorisations pour effectuer les actions suivantes:</span><span class="sxs-lookup"><span data-stu-id="6eef9-133">MCS will use those permissions to perform the following actions:</span></span>
 
-   <span data-ttu-id="6eef9-134">S’assurer que l’application fonctionne sur l’ordinateur virtuel configuré pour Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="6eef9-134">Ensuring that the app works on virtual machine configured for Microsoft Managed Desktop</span></span>
-   <span data-ttu-id="6eef9-135">Téléchargement de l’application vers Microsoft Intune pour le déploiement vers vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6eef9-135">Uploading the app to Microsoft Intune for deployment to your users</span></span>

<span data-ttu-id="6eef9-136">Sans ces autorisations, il est possible que MCS se déplace vers l’avant, mais il ne pourra pas télécharger les applications dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6eef9-136">Without these permissions, it is possible for MCS to move forward, but they will not be able to upload the applications to your environment.</span></span>


