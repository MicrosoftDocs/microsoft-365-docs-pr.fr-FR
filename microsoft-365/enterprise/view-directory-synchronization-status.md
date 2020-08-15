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
ms.openlocfilehash: c77898b58b58c6ae91492debd7ad66f395d80d52
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689958"
---
# <a name="view-directory-synchronization-status-in-microsoft-365"></a><span data-ttu-id="962ae-103">Afficher l’état de la synchronisation d’annuaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="962ae-103">View directory synchronization status in Microsoft 365</span></span>

<span data-ttu-id="962ae-104">Si vous avez intégré Active Directory sur site à Azure AD en synchronisant votre environnement local avec Microsoft 365, vous pouvez également vérifier l’état de votre synchronisation.</span><span class="sxs-lookup"><span data-stu-id="962ae-104">If you have integrated your on-premises Active Directory with Azure AD by synchronizing your on-premises environment with Microsoft 365, you can also check the status of your synchronization.</span></span>
  
## <a name="view-directory-synchronization-status"></a><span data-ttu-id="962ae-105">Consulter l’état de synchronisation des annuaires</span><span class="sxs-lookup"><span data-stu-id="962ae-105">View directory synchronization status</span></span>

- <span data-ttu-id="962ae-106">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) et choisissez **DirSync Status** sur la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="962ae-106">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) and choose **DirSync Status** on the home page.</span></span>
- <span data-ttu-id="962ae-107">Vous pouvez également **accéder à utilisateurs** \> **actifs**, puis, sur la page **utilisateurs actifs** , sélectionner plus de **More** \> **synchronisation d’annuaires**.</span><span class="sxs-lookup"><span data-stu-id="962ae-107">Alternately, you can go to **Users** \> **Active users**, and on the **Active users** page, choose **More** \> **Directory synchronization**.</span></span> <span data-ttu-id="962ae-108">Dans le volet **synchronisation d’annuaires** , sélectionnez **accéder à la gestion DirSync**.</span><span class="sxs-lookup"><span data-stu-id="962ae-108">On the **Directory Synchronization** pane, choose **Go to DirSync management**.</span></span>

## <a name="information-on-the-manage-directory-synchronization-page"></a><span data-ttu-id="962ae-109">Informations sur la page gérer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="962ae-109">Information on the Manage directory synchronization page</span></span>

<span data-ttu-id="962ae-110">Le tableau suivant répertorie les fonctionnalités sur lesquelles vous pouvez obtenir des informations sur la page.</span><span class="sxs-lookup"><span data-stu-id="962ae-110">The following table lists the features you can get information about on the page.</span></span>
  
<span data-ttu-id="962ae-111">En cas de problème avec la synchronisation d’annuaires, les erreurs sont également répertoriées sur cette page.</span><span class="sxs-lookup"><span data-stu-id="962ae-111">If there is a problem with your directory synchronization, the errors are listed on this page as well.</span></span> <span data-ttu-id="962ae-112">Pour plus d’informations sur les différentes erreurs que vous pouvez rencontrer, consultez la rubrique [identifier les erreurs de synchronisation d’annuaires dans Microsoft 365](identify-directory-synchronization-errors.md).</span><span class="sxs-lookup"><span data-stu-id="962ae-112">For more information about different errors you might encounter, see [Identify directory synchronization errors in Microsoft 365](identify-directory-synchronization-errors.md).</span></span>
  
|<span data-ttu-id="962ae-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="962ae-113">**Item**</span></span>|<span data-ttu-id="962ae-114">**Objet**</span><span class="sxs-lookup"><span data-stu-id="962ae-114">**What it's for**</span></span>|
|:-----|:-----|
|<span data-ttu-id="962ae-115">**Domaines vérifiés**</span><span class="sxs-lookup"><span data-stu-id="962ae-115">**Domains verified**</span></span> | <span data-ttu-id="962ae-116">Nombre de domaines de votre client Microsoft 365 que vous avez vérifié.</span><span class="sxs-lookup"><span data-stu-id="962ae-116">Number of domains in your Microsoft 365 tenant that you have verified you own.</span></span> |
|<span data-ttu-id="962ae-117">**Domaines non vérifiés**</span><span class="sxs-lookup"><span data-stu-id="962ae-117">**Domains not verified**</span></span> | <span data-ttu-id="962ae-118">Les domaines que vous avez ajoutés, mais qui n’ont pas été vérifiés.</span><span class="sxs-lookup"><span data-stu-id="962ae-118">Domains you have added, but not verified.</span></span> |
|<span data-ttu-id="962ae-119">**Synchronisation d’annuaires activée**</span><span class="sxs-lookup"><span data-stu-id="962ae-119">**Directory sync enabled**</span></span> |<span data-ttu-id="962ae-120">True ou false.</span><span class="sxs-lookup"><span data-stu-id="962ae-120">True or False.</span></span> <span data-ttu-id="962ae-121">Indique si la synchronisation d’annuaires est activée.</span><span class="sxs-lookup"><span data-stu-id="962ae-121">Specifies whether you have enabled directory sync.</span></span> |
|<span data-ttu-id="962ae-122">**Dernière synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="962ae-122">**Latest directory sync**</span></span> | <span data-ttu-id="962ae-123">Dernière exécution de la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="962ae-123">Last time directory sync ran.</span></span> <span data-ttu-id="962ae-124">Affichera un avertissement et un lien vers un outil de dépannage Si la dernière synchronisation remonte à plus de trois jours.</span><span class="sxs-lookup"><span data-stu-id="962ae-124">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="962ae-125">**Synchronisation de mot de passe activée**</span><span class="sxs-lookup"><span data-stu-id="962ae-125">**Password sync enabled**</span></span> | <span data-ttu-id="962ae-126">True ou false.</span><span class="sxs-lookup"><span data-stu-id="962ae-126">True or False.</span></span> <span data-ttu-id="962ae-127">Indique si la synchronisation de hachage de mot de passe s’est déplacée entre notre client local et votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="962ae-127">Specifies whether you have password hash sync between our on-premises and your Microsoft 365 tenant.</span></span> |
|<span data-ttu-id="962ae-128">**Dernière synchronisation de mot de passe**</span><span class="sxs-lookup"><span data-stu-id="962ae-128">**Last Password Sync**</span></span> | <span data-ttu-id="962ae-129">Dernière exécution de la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="962ae-129">Last time password hash sync ran.</span></span> <span data-ttu-id="962ae-130">Affichera un avertissement et un lien vers un outil de dépannage Si la dernière synchronisation remonte à plus de trois jours.</span><span class="sxs-lookup"><span data-stu-id="962ae-130">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="962ae-131">**Version du client de synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="962ae-131">**Directory sync client version**</span></span> | <span data-ttu-id="962ae-132">Contient un lien de téléchargement si une nouvelle version d’Azure AD Connect a été publiée.</span><span class="sxs-lookup"><span data-stu-id="962ae-132">Contains a download link if a new version of Azure AD Connect has been released.</span></span> |
|<span data-ttu-id="962ae-133">**Compte de service de synchronisation d’annuaires**</span><span class="sxs-lookup"><span data-stu-id="962ae-133">**Directory sync service account**</span></span> | <span data-ttu-id="962ae-134">Affiche le nom de votre compte de service de synchronisation d’annuaires Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="962ae-134">Displays the name of your Microsoft 365 directory sync service account.</span></span> |