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
description: Dans cet article, découvrez comment vérifier l’état de votre synchronisation d’annuaires dans Office 365.
ms.openlocfilehash: 7577ed358a262d5b0ef2932bc73cf61941bec31b
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48326948"
---
# <a name="view-directory-synchronization-status-in-microsoft-365"></a><span data-ttu-id="5242a-103">Afficher l’état de la synchronisation d’annuaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5242a-103">View directory synchronization status in Microsoft 365</span></span>

<span data-ttu-id="5242a-104">Si vous avez intégré vos services de domaine Active Directory (AD DS) locaux à Azure Active Directory (Azure AD) en synchronisant votre environnement local avec Microsoft 365, vous pouvez également vérifier l’état de votre synchronisation.</span><span class="sxs-lookup"><span data-stu-id="5242a-104">If you have integrated your on-premises Active Directory Domain Services (AD DS) with Azure Active Directory (Azure AD) by synchronizing your on-premises environment with Microsoft 365, you can also check the status of your synchronization.</span></span>
  
## <a name="view-directory-synchronization-status"></a><span data-ttu-id="5242a-105">Consulter l’état de synchronisation des annuaires</span><span class="sxs-lookup"><span data-stu-id="5242a-105">View directory synchronization status</span></span>

- <span data-ttu-id="5242a-106">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) et choisissez **État DirSync** sur la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="5242a-106">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) and choose **DirSync Status** on the home page.</span></span>
- <span data-ttu-id="5242a-107">Vous pouvez également vous  rendre sur Utilisateurs actifs et, sur la page Utilisateurs actifs, choisir Plus de synchronisation \>    \> **d’annuaires.**</span><span class="sxs-lookup"><span data-stu-id="5242a-107">Alternately, you can go to **Users** \> **Active users**, and on the **Active users** page, choose **More** \> **Directory synchronization**.</span></span> <span data-ttu-id="5242a-108">Dans le volet Synchronisation d’annuaires, choisissez **Go to DirSync management**. </span><span class="sxs-lookup"><span data-stu-id="5242a-108">On the **Directory Synchronization** pane, choose **Go to DirSync management**.</span></span>

## <a name="information-on-the-manage-directory-synchronization-page"></a><span data-ttu-id="5242a-109">Informations sur la page Gérer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="5242a-109">Information on the Manage directory synchronization page</span></span>

<span data-ttu-id="5242a-110">Le tableau suivant répertorie les fonctionnalités dont vous pouvez obtenir des informations sur la page.</span><span class="sxs-lookup"><span data-stu-id="5242a-110">The following table lists the features you can get information about on the page.</span></span>
  
<span data-ttu-id="5242a-111">En cas de problème avec votre synchronisation d’annuaires, les erreurs sont également répertoriées sur cette page.</span><span class="sxs-lookup"><span data-stu-id="5242a-111">If there is a problem with your directory synchronization, the errors are listed on this page as well.</span></span> <span data-ttu-id="5242a-112">Pour plus d’informations sur les différentes erreurs que vous pouvez rencontrer, voir Identifier les erreurs de synchronisation d’annuaires [dans Microsoft 365.](identify-directory-synchronization-errors.md)</span><span class="sxs-lookup"><span data-stu-id="5242a-112">For more information about different errors you might encounter, see [Identify directory synchronization errors in Microsoft 365](identify-directory-synchronization-errors.md).</span></span>
  
|<span data-ttu-id="5242a-113">Item</span><span class="sxs-lookup"><span data-stu-id="5242a-113">Item</span></span>|<span data-ttu-id="5242a-114">Objet</span><span class="sxs-lookup"><span data-stu-id="5242a-114">What it's for</span></span>|
|:-----|:-----|
|<span data-ttu-id="5242a-115">**Domaines vérifiés**</span><span class="sxs-lookup"><span data-stu-id="5242a-115">**Domains verified**</span></span> | <span data-ttu-id="5242a-116">Nombre de domaines dans votre client Microsoft 365 que vous avez vérifiés.</span><span class="sxs-lookup"><span data-stu-id="5242a-116">Number of domains in your Microsoft 365 tenant that you have verified you own.</span></span> |
|<span data-ttu-id="5242a-117">**Domaines non vérifiés**</span><span class="sxs-lookup"><span data-stu-id="5242a-117">**Domains not verified**</span></span> | <span data-ttu-id="5242a-118">Domaines que vous avez ajoutés, mais pas vérifiés.</span><span class="sxs-lookup"><span data-stu-id="5242a-118">Domains you have added, but not verified.</span></span> |
|<span data-ttu-id="5242a-119">**Synchronisation d’annuaires activée**</span><span class="sxs-lookup"><span data-stu-id="5242a-119">**Directory sync enabled**</span></span> |<span data-ttu-id="5242a-120">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5242a-120">True or False.</span></span> <span data-ttu-id="5242a-121">Spécifie si vous avez activé la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="5242a-121">Specifies whether you have enabled directory sync.</span></span> |
|<span data-ttu-id="5242a-122">**Dernière synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="5242a-122">**Latest directory sync**</span></span> | <span data-ttu-id="5242a-123">Dernière synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="5242a-123">Last time directory sync ran.</span></span> <span data-ttu-id="5242a-124">Affiche un avertissement et un lien vers un outil de dépannage si la dernière synchronisation a eu lieu il y a plus de trois jours.</span><span class="sxs-lookup"><span data-stu-id="5242a-124">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="5242a-125">**Synchronisation de mot de passe activée**</span><span class="sxs-lookup"><span data-stu-id="5242a-125">**Password sync enabled**</span></span> | <span data-ttu-id="5242a-126">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5242a-126">True or False.</span></span> <span data-ttu-id="5242a-127">Spécifie si vous disposez d’une synchronisation de hachage de mot de passe entre notre site local et votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5242a-127">Specifies whether you have password hash sync between our on-premises and your Microsoft 365 tenant.</span></span> |
|<span data-ttu-id="5242a-128">**Dernière synchronisation de mot de passe**</span><span class="sxs-lookup"><span data-stu-id="5242a-128">**Last Password Sync**</span></span> | <span data-ttu-id="5242a-129">Dernière synchronisation de hachage du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5242a-129">Last time password hash sync ran.</span></span> <span data-ttu-id="5242a-130">Affiche un avertissement et un lien vers un outil de dépannage si la dernière synchronisation a eu lieu il y a plus de trois jours.</span><span class="sxs-lookup"><span data-stu-id="5242a-130">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="5242a-131">**Version du client de synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="5242a-131">**Directory sync client version**</span></span> | <span data-ttu-id="5242a-132">Contient un lien de téléchargement si une nouvelle version d’Azure AD Connect a été publiée.</span><span class="sxs-lookup"><span data-stu-id="5242a-132">Contains a download link if a new version of Azure AD Connect has been released.</span></span> |
|<span data-ttu-id="5242a-133">**Compte de service de synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="5242a-133">**Directory sync service account**</span></span> | <span data-ttu-id="5242a-134">Affiche le nom de votre compte de service de synchronisation d’annuaires Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5242a-134">Displays the name of your Microsoft 365 directory sync service account.</span></span> |
|||

## <a name="monitor-synchronization-health"></a><span data-ttu-id="5242a-135">Surveiller l’état de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="5242a-135">Monitor synchronization health</span></span>

<span data-ttu-id="5242a-136">Dans cette section, vous allez installer un agent d’intégrité Azure AD Connect sur chacun de vos contrôleurs de domaine AD DS pour surveiller votre infrastructure d’identité et les services de synchronisation fournis par Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="5242a-136">In this section, you'll install an Azure AD Connect Health agent on each of your on-premises AD DS domain controllers to monitor your identity infrastructure and the synchronization services provided by Azure AD Connect.</span></span> <span data-ttu-id="5242a-137">Les informations de surveillance sont disponibles sur un portail Azure AD Connect Health, où vous pouvez afficher les alertes, surveiller les performances, analyser les utilisations, etc.</span><span class="sxs-lookup"><span data-stu-id="5242a-137">The monitoring information is made available in an Azure AD Connect Health portal, where you can view alerts, performance monitoring, usage analytics, and other information.</span></span>

<span data-ttu-id="5242a-138">La décision de conception clé concernant l’utilisation d’Azure AD Connect Health est basée sur la manière dont vous utilisez Azure AD Connect :</span><span class="sxs-lookup"><span data-stu-id="5242a-138">The key design decision of how to use Azure AD Connect Health is based on how you are using Azure AD Connect:</span></span>

- <span data-ttu-id="5242a-139">Si vous utilisez de nouveau l’option d’**authentification gérée**, commencez avec la rubrique relative à l’[utilisation d’Azure AD Connect Health avec la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="5242a-139">If you’re using the **managed authentication** option, start with [Using Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) to understand and configure Azure AD Connect Health.</span></span>
- <span data-ttu-id="5242a-140">Si vous synchronisez uniquement les noms des comptes et des groupes à l’aide de l’**authentification fédérée** avec Active Directory Federation Services (AD FS), commencez avec la rubrique [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="5242a-140">If you're synchronizing just the names of the accounts and groups using **federated authentication** with Active Directory Federation Services (AD FS), start with [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) to understand and configure Azure AD Connect Health.</span></span>

<span data-ttu-id="5242a-141">Lorsque vous avez terminé, vous aurez :</span><span class="sxs-lookup"><span data-stu-id="5242a-141">When complete, you’ll have:</span></span>

- <span data-ttu-id="5242a-142">l’agent Azure AD Connect Health installé sur vos serveurs de fournisseur d’identité local ;</span><span class="sxs-lookup"><span data-stu-id="5242a-142">The Azure AD Connect Health agent installed on your on-premises identity provider servers.</span></span>
- <span data-ttu-id="5242a-143">le portail Azure AD Connect Health qui affiche l’état actuel de vos activités d’infrastructure et de synchronisation locales avec le client Azure AD pour votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5242a-143">The Azure AD Connect Health portal displaying the current state of your on-premises infrastructure and synchronization activities with the Azure AD tenant for your Microsoft 365 subscription.</span></span>

