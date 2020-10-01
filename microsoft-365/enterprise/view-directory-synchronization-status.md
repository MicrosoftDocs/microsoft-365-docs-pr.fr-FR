---
title: Afficher l’état de la synchronisation d’annuaires dans Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOE150
- MED150
ms.assetid: 18be3b98-34ae-47be-9337-ab6c3fb372ac
description: Dans cet article, Découvrez comment vérifier l’état de votre synchronisation d’annuaires dans Office 365.
ms.openlocfilehash: 7577ed358a262d5b0ef2932bc73cf61941bec31b
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48326948"
---
# <a name="view-directory-synchronization-status-in-microsoft-365"></a><span data-ttu-id="4ee20-103">Afficher l’état de la synchronisation d’annuaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4ee20-103">View directory synchronization status in Microsoft 365</span></span>

<span data-ttu-id="4ee20-104">Si vous avez intégré vos services de domaine Active Directory (AD DS) sur site à Azure Active Directory (Azure AD) en synchronisant votre environnement local avec Microsoft 365, vous pouvez également vérifier l’état de votre synchronisation.</span><span class="sxs-lookup"><span data-stu-id="4ee20-104">If you have integrated your on-premises Active Directory Domain Services (AD DS) with Azure Active Directory (Azure AD) by synchronizing your on-premises environment with Microsoft 365, you can also check the status of your synchronization.</span></span>
  
## <a name="view-directory-synchronization-status"></a><span data-ttu-id="4ee20-105">Consulter l’état de synchronisation des annuaires</span><span class="sxs-lookup"><span data-stu-id="4ee20-105">View directory synchronization status</span></span>

- <span data-ttu-id="4ee20-106">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) et choisissez **DirSync Status** sur la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="4ee20-106">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) and choose **DirSync Status** on the home page.</span></span>
- <span data-ttu-id="4ee20-107">Vous pouvez également **accéder à utilisateurs** \> **actifs**, puis, sur la page **utilisateurs actifs** , sélectionner plus de **More** \> **synchronisation d’annuaires**.</span><span class="sxs-lookup"><span data-stu-id="4ee20-107">Alternately, you can go to **Users** \> **Active users**, and on the **Active users** page, choose **More** \> **Directory synchronization**.</span></span> <span data-ttu-id="4ee20-108">Dans le volet **synchronisation d’annuaires** , sélectionnez **accéder à la gestion DirSync**.</span><span class="sxs-lookup"><span data-stu-id="4ee20-108">On the **Directory Synchronization** pane, choose **Go to DirSync management**.</span></span>

## <a name="information-on-the-manage-directory-synchronization-page"></a><span data-ttu-id="4ee20-109">Informations sur la page gérer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="4ee20-109">Information on the Manage directory synchronization page</span></span>

<span data-ttu-id="4ee20-110">Le tableau suivant répertorie les fonctionnalités sur lesquelles vous pouvez obtenir des informations sur la page.</span><span class="sxs-lookup"><span data-stu-id="4ee20-110">The following table lists the features you can get information about on the page.</span></span>
  
<span data-ttu-id="4ee20-111">En cas de problème avec la synchronisation d’annuaires, les erreurs sont également répertoriées sur cette page.</span><span class="sxs-lookup"><span data-stu-id="4ee20-111">If there is a problem with your directory synchronization, the errors are listed on this page as well.</span></span> <span data-ttu-id="4ee20-112">Pour plus d’informations sur les différentes erreurs que vous pouvez rencontrer, consultez la rubrique [identifier les erreurs de synchronisation d’annuaires dans Microsoft 365](identify-directory-synchronization-errors.md).</span><span class="sxs-lookup"><span data-stu-id="4ee20-112">For more information about different errors you might encounter, see [Identify directory synchronization errors in Microsoft 365](identify-directory-synchronization-errors.md).</span></span>
  
|<span data-ttu-id="4ee20-113">Item</span><span class="sxs-lookup"><span data-stu-id="4ee20-113">Item</span></span>|<span data-ttu-id="4ee20-114">Objet</span><span class="sxs-lookup"><span data-stu-id="4ee20-114">What it's for</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ee20-115">**Domaines vérifiés**</span><span class="sxs-lookup"><span data-stu-id="4ee20-115">**Domains verified**</span></span> | <span data-ttu-id="4ee20-116">Nombre de domaines de votre client Microsoft 365 que vous avez vérifié.</span><span class="sxs-lookup"><span data-stu-id="4ee20-116">Number of domains in your Microsoft 365 tenant that you have verified you own.</span></span> |
|<span data-ttu-id="4ee20-117">**Domaines non vérifiés**</span><span class="sxs-lookup"><span data-stu-id="4ee20-117">**Domains not verified**</span></span> | <span data-ttu-id="4ee20-118">Les domaines que vous avez ajoutés, mais qui n’ont pas été vérifiés.</span><span class="sxs-lookup"><span data-stu-id="4ee20-118">Domains you have added, but not verified.</span></span> |
|<span data-ttu-id="4ee20-119">**Synchronisation d’annuaires activée**</span><span class="sxs-lookup"><span data-stu-id="4ee20-119">**Directory sync enabled**</span></span> |<span data-ttu-id="4ee20-120">True ou false.</span><span class="sxs-lookup"><span data-stu-id="4ee20-120">True or False.</span></span> <span data-ttu-id="4ee20-121">Indique si la synchronisation d’annuaires est activée.</span><span class="sxs-lookup"><span data-stu-id="4ee20-121">Specifies whether you have enabled directory sync.</span></span> |
|<span data-ttu-id="4ee20-122">**Dernière synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="4ee20-122">**Latest directory sync**</span></span> | <span data-ttu-id="4ee20-123">Dernière exécution de la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="4ee20-123">Last time directory sync ran.</span></span> <span data-ttu-id="4ee20-124">Affichera un avertissement et un lien vers un outil de dépannage Si la dernière synchronisation remonte à plus de trois jours.</span><span class="sxs-lookup"><span data-stu-id="4ee20-124">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="4ee20-125">**Synchronisation de mot de passe activée**</span><span class="sxs-lookup"><span data-stu-id="4ee20-125">**Password sync enabled**</span></span> | <span data-ttu-id="4ee20-126">True ou false.</span><span class="sxs-lookup"><span data-stu-id="4ee20-126">True or False.</span></span> <span data-ttu-id="4ee20-127">Indique si la synchronisation de hachage de mot de passe s’est déplacée entre notre client local et votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4ee20-127">Specifies whether you have password hash sync between our on-premises and your Microsoft 365 tenant.</span></span> |
|<span data-ttu-id="4ee20-128">**Dernière synchronisation de mot de passe**</span><span class="sxs-lookup"><span data-stu-id="4ee20-128">**Last Password Sync**</span></span> | <span data-ttu-id="4ee20-129">Dernière exécution de la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4ee20-129">Last time password hash sync ran.</span></span> <span data-ttu-id="4ee20-130">Affichera un avertissement et un lien vers un outil de dépannage Si la dernière synchronisation remonte à plus de trois jours.</span><span class="sxs-lookup"><span data-stu-id="4ee20-130">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="4ee20-131">**Version du client de synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="4ee20-131">**Directory sync client version**</span></span> | <span data-ttu-id="4ee20-132">Contient un lien de téléchargement si une nouvelle version d’Azure AD Connect a été publiée.</span><span class="sxs-lookup"><span data-stu-id="4ee20-132">Contains a download link if a new version of Azure AD Connect has been released.</span></span> |
|<span data-ttu-id="4ee20-133">**Compte de service de synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="4ee20-133">**Directory sync service account**</span></span> | <span data-ttu-id="4ee20-134">Affiche le nom de votre compte de service de synchronisation d’annuaires Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4ee20-134">Displays the name of your Microsoft 365 directory sync service account.</span></span> |
|||

## <a name="monitor-synchronization-health"></a><span data-ttu-id="4ee20-135">Surveiller l’état de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="4ee20-135">Monitor synchronization health</span></span>

<span data-ttu-id="4ee20-136">Dans cette section, vous allez installer un agent d’intégrité Azure AD Connect sur chacun de vos contrôleurs de domaine AD DS pour surveiller votre infrastructure d’identité et les services de synchronisation fournis par Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="4ee20-136">In this section, you'll install an Azure AD Connect Health agent on each of your on-premises AD DS domain controllers to monitor your identity infrastructure and the synchronization services provided by Azure AD Connect.</span></span> <span data-ttu-id="4ee20-137">Les informations de surveillance sont disponibles sur un portail Azure AD Connect Health, où vous pouvez afficher les alertes, surveiller les performances, analyser les utilisations, etc.</span><span class="sxs-lookup"><span data-stu-id="4ee20-137">The monitoring information is made available in an Azure AD Connect Health portal, where you can view alerts, performance monitoring, usage analytics, and other information.</span></span>

<span data-ttu-id="4ee20-138">La décision de conception clé concernant l’utilisation d’Azure AD Connect Health est basée sur la manière dont vous utilisez Azure AD Connect :</span><span class="sxs-lookup"><span data-stu-id="4ee20-138">The key design decision of how to use Azure AD Connect Health is based on how you are using Azure AD Connect:</span></span>

- <span data-ttu-id="4ee20-139">Si vous utilisez de nouveau l’option d’**authentification gérée**, commencez avec la rubrique relative à l’[utilisation d’Azure AD Connect Health avec la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="4ee20-139">If you’re using the **managed authentication** option, start with [Using Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) to understand and configure Azure AD Connect Health.</span></span>
- <span data-ttu-id="4ee20-140">Si vous synchronisez uniquement les noms des comptes et des groupes à l’aide de l’**authentification fédérée** avec Active Directory Federation Services (AD FS), commencez avec la rubrique [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="4ee20-140">If you're synchronizing just the names of the accounts and groups using **federated authentication** with Active Directory Federation Services (AD FS), start with [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) to understand and configure Azure AD Connect Health.</span></span>

<span data-ttu-id="4ee20-141">Lorsque vous avez terminé, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4ee20-141">When complete, you’ll have:</span></span>

- <span data-ttu-id="4ee20-142">l’agent Azure AD Connect Health installé sur vos serveurs de fournisseur d’identité local ;</span><span class="sxs-lookup"><span data-stu-id="4ee20-142">The Azure AD Connect Health agent installed on your on-premises identity provider servers.</span></span>
- <span data-ttu-id="4ee20-143">le portail Azure AD Connect Health qui affiche l’état actuel de vos activités d’infrastructure et de synchronisation locales avec le client Azure AD pour votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4ee20-143">The Azure AD Connect Health portal displaying the current state of your on-premises infrastructure and synchronization activities with the Azure AD tenant for your Microsoft 365 subscription.</span></span>

