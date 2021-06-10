---
title: Installer les Portail d’entreprise Intune sur les appareils
description: Informations sur l’installation de l’application portail d’entreprise Bureau géré Microsoft appareils
keywords: Bureau géré Microsoft, Microsoft 365, Portail d’entreprise
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: f9f36d6ca14be610ce9374380349264439282a6a
ms.sourcegitcommit: 1206319a5d3fed8d52a2581b8beafc34ab064b1c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2021
ms.locfileid: "52086684"
---
# <a name="install-intune-company-portal-on-devices"></a><span data-ttu-id="d32de-104">Installer les Portail d’entreprise Intune sur les appareils</span><span class="sxs-lookup"><span data-stu-id="d32de-104">Install Intune Company Portal on devices</span></span>

<span data-ttu-id="d32de-105">Bureau géré Microsoft nécessite que les administrateurs informatiques installent Portail d’entreprise Intune pour leurs utilisateurs avec Bureau géré Microsoft appareils.</span><span class="sxs-lookup"><span data-stu-id="d32de-105">Microsoft Managed Desktop requires that IT administrators install Intune Company Portal for their users with Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="d32de-106">Voici quelques avantages pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="d32de-106">Here are some benefits for your organization:</span></span>
- <span data-ttu-id="d32de-107">Les utilisateurs disposent d’un seul endroit pour parcourir et installer les applications disponibles.</span><span class="sxs-lookup"><span data-stu-id="d32de-107">Users have one place to browse and install available applications.</span></span> 
- <span data-ttu-id="d32de-108">Les administrateurs informatiques peuvent organiser les applications par catégories pour leurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d32de-108">IT administrators can organize applications by categories for their users.</span></span>  
- <span data-ttu-id="d32de-109">Certaines applications (comme Microsoft Project et Microsoft Visio) nécessitent Portail d’entreprise déployer avec Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d32de-109">Some applications (like Microsoft Project and Microsoft Visio) require Company Portal to deploy with Microsoft Managed Desktop.</span></span>
- <span data-ttu-id="d32de-110">Les administrateurs informatiques peuvent personnaliser Portail d’entreprise pour leur organisation.</span><span class="sxs-lookup"><span data-stu-id="d32de-110">IT administrators can customize Company Portal for their organization.</span></span> <span data-ttu-id="d32de-111">Cela inclut la création d’images de marque, l’ajout de contacts de support local, etc.</span><span class="sxs-lookup"><span data-stu-id="d32de-111">This includes brand imaging, adding in local support contacts, and more.</span></span> <span data-ttu-id="d32de-112">Pour plus d’informations, [voir How to Configure the Microsoft Intune Portail d’entreprise app](/intune/company-portal-app).</span><span class="sxs-lookup"><span data-stu-id="d32de-112">For more information, see [How to Configure the Microsoft Intune Company Portal app](/intune/company-portal-app).</span></span>   

<span data-ttu-id="d32de-113">Cette rubrique documente le processus de déploiement des Portail d’entreprise Intune à vos utilisateurs Bureau géré Microsoft utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d32de-113">This topic documents the process for deploying the Intune Company Portal to your Microsoft Managed Desktop users.</span></span> <span data-ttu-id="d32de-114">Le processus global ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="d32de-114">The overall process looks like this:</span></span>
1. <span data-ttu-id="d32de-115">Acheter Portail d’entreprise de Microsoft Store pour Entreprises et synchroniser avec Intune</span><span class="sxs-lookup"><span data-stu-id="d32de-115">Purchase Company Portal from Microsoft Store for Business and sync with Intune</span></span>
2. <span data-ttu-id="d32de-116">Affecter des Portail d’entreprise à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d32de-116">Assign Company Portal to your users</span></span>
3. <span data-ttu-id="d32de-117">Communiquer les changements à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d32de-117">Communicate change to your users</span></span>

## <a name="step-1---purchase-company-portal-from-microsoft-store-for-business-and-sync-with-intune"></a><span data-ttu-id="d32de-118">Étape 1 : acheter des Portail d’entreprise auprès Microsoft Store pour Entreprises et synchroniser avec Intune</span><span class="sxs-lookup"><span data-stu-id="d32de-118">Step 1 - Purchase Company Portal from Microsoft Store for Business and sync with Intune</span></span>
<span data-ttu-id="d32de-119">Pour plus d’informations sur l’achat des applications et la synchronisation avec Intune, voir Microsoft Store pour Entreprises [applications dans](deploy-apps.md#msfb-apps) Deploy apps to *Bureau géré Microsoft devices*.</span><span class="sxs-lookup"><span data-stu-id="d32de-119">For info on how to purchase the apps and sync with Intune, see [Microsoft Store for Business apps](deploy-apps.md#msfb-apps) in *Deploy apps to Microsoft Managed Desktop devices*.</span></span>

<span data-ttu-id="d32de-120">Cette rubrique fournit des informations sur la façon de :</span><span class="sxs-lookup"><span data-stu-id="d32de-120">This topic provides info on how to:</span></span> 
- <span data-ttu-id="d32de-121">Acheter des Portail d’entreprise dans Microsoft Store pour Entreprises</span><span class="sxs-lookup"><span data-stu-id="d32de-121">Purchase Company Portal from Microsoft Store for Business</span></span> 
- <span data-ttu-id="d32de-122">Forcer la synchronisation entre Intune et Microsoft Store pour Entreprises</span><span class="sxs-lookup"><span data-stu-id="d32de-122">Force sync between Intune and Microsoft Store for Business</span></span>
- <span data-ttu-id="d32de-123">Vérifier la synchronisation active entre Intune et Microsoft Store pour Entreprises</span><span class="sxs-lookup"><span data-stu-id="d32de-123">Verify active sync between Intune and Microsoft Store for Business</span></span> 

## <a name="step-2---assign-company-portal-to-your-users"></a><span data-ttu-id="d32de-124">Étape 2 : affecter des Portail d’entreprise à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d32de-124">Step 2 - Assign Company Portal to your users</span></span>
<span data-ttu-id="d32de-125">Après votre inscription dans Bureau géré Microsoft, nous allons déployer automatiquement Portail d’entreprise sur votre client et installer l’application sur Bureau géré Microsoft appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d32de-125">Following your enrollment in Microsoft Managed Desktop, we will automatically deploy Company Portal to your tenant and install the app on Microsoft Managed Desktop devices in your organization.</span></span>

## <a name="step-3---communicate-change-to-your-users"></a><span data-ttu-id="d32de-126">Étape 3 : communiquer les changements à vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d32de-126">Step 3 - Communicate change to your users</span></span>
<span data-ttu-id="d32de-127">En tant qu’administrateur informatique de votre organisation, il est important de faire savoir à vos utilisateurs comment utiliser les Portail d’entreprise votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d32de-127">As the IT administrator for your organization, it’s important to let your users know how to use Company Portal in your organization.</span></span> <span data-ttu-id="d32de-128">Bureau géré Microsoft recommande :</span><span class="sxs-lookup"><span data-stu-id="d32de-128">Microsoft Managed Desktop recommends:</span></span>
- <span data-ttu-id="d32de-129">Étapes d’installation des applications à partir du Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d32de-129">Steps on installing applications from the Company Portal.</span></span> <span data-ttu-id="d32de-130">Pour plus d’informations, [voir Installer et partager des applications sur votre appareil.](/intune-user-help/install-apps-cpapp-windows)</span><span class="sxs-lookup"><span data-stu-id="d32de-130">For more information, see [Install and share apps on your device](/intune-user-help/install-apps-cpapp-windows).</span></span>
- <span data-ttu-id="d32de-131">Comment envoyer des demandes aux administrateurs informatiques pour les applications qui ne sont pas actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="d32de-131">How to send requests to IT administrators for applications that are not currently available.</span></span> <span data-ttu-id="d32de-132">Pour plus d’informations, voir [Demander une application pour le travail ou l’école.](/intune-user-help/install-apps-cpapp-windows#request-an-app-for-work-or-school)</span><span class="sxs-lookup"><span data-stu-id="d32de-132">For more information, see [Request an app for work or school](/intune-user-help/install-apps-cpapp-windows#request-an-app-for-work-or-school).</span></span>  

## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="d32de-133">Étapes de mise en Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="d32de-133">Steps to get started with Microsoft Managed Desktop</span></span>

1. [<span data-ttu-id="d32de-134">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="d32de-134">Add and verify admin contacts in the Admin portal</span></span>](add-admin-contacts.md)
2. [<span data-ttu-id="d32de-135">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="d32de-135">Adjust conditional access</span></span>](conditional-access.md)
3. [<span data-ttu-id="d32de-136">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="d32de-136">Assign licenses</span></span>](assign-licenses.md)
4. <span data-ttu-id="d32de-137">Déployer Portail d’entreprise Intune (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="d32de-137">Deploy Intune Company Portal (this topic)</span></span>
5. [<span data-ttu-id="d32de-138">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="d32de-138">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="d32de-139">Configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="d32de-139">Set up devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="d32de-140">Préparer vos utilisateurs à l’utilisation les appareils</span><span class="sxs-lookup"><span data-stu-id="d32de-140">Get your users ready to use devices</span></span>](get-started-devices.md)
8. [<span data-ttu-id="d32de-141">Déployer des applications</span><span class="sxs-lookup"><span data-stu-id="d32de-141">Deploy apps</span></span>](deploy-apps.md)
