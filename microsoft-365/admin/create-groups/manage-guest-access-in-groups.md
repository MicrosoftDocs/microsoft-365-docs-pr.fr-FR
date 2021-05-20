---
title: Gérer l’accès invité dans Microsoft 365 groupes
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
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
- MET150
- MOE150
ms.assetid: 9de497a9-2f5c-43d6-ae18-767f2e6fe6e0
description: Découvrez comment ajouter des invités à un groupe Microsoft 365, afficher les utilisateurs invités et utiliser PowerShell pour contrôler l’accès invité.
ms.openlocfilehash: c52f0094e724040b71d5d72cded049fed57e3969
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52571936"
---
# <a name="manage-guest-access-in-microsoft-365-groups"></a><span data-ttu-id="3c764-103">Gérer l’accès invité dans Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="3c764-103">Manage guest access in Microsoft 365 groups</span></span>

<span data-ttu-id="3c764-104">Par défaut, l’accès invité pour Microsoft 365 groupes est désactivé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3c764-104">By default, guest access for Microsoft 365 groups is turned on for your organization.</span></span> <span data-ttu-id="3c764-105">Les administrateurs peuvent contrôler s’il faut autoriser l’accès invité à des groupes pour l’ensemble de leur organisation ou pour des groupes individuels.</span><span class="sxs-lookup"><span data-stu-id="3c764-105">Admins can control whether to allow guest access to groups for their whole organization or for individual groups.</span></span>

<span data-ttu-id="3c764-106">Lorsqu’il est allumé, les membres du groupe peuvent inviter des utilisateurs invités à un groupe Microsoft 365 via Outlook web.</span><span class="sxs-lookup"><span data-stu-id="3c764-106">When it's turned on, group members can invite guest users to a Microsoft 365 group through Outlook on Web.</span></span> <span data-ttu-id="3c764-107">Les invitations sont envoyées au propriétaire du groupe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="3c764-107">Invitations are sent to the group owner for approval.</span></span>

<span data-ttu-id="3c764-108">Une fois approuvé, l’utilisateur invité est ajouté à l’annuaire et au groupe.</span><span class="sxs-lookup"><span data-stu-id="3c764-108">Once approved, the guest user is added to the directory and the group.</span></span>

> [!Note]
> <span data-ttu-id="3c764-109">Yammer Entreprise réseaux qui sont en mode natif ou la région ue ne [sont](/yammer/manage-security-and-compliance/manage-data-compliance) pas en charge les invités réseau.</span><span class="sxs-lookup"><span data-stu-id="3c764-109">Yammer Enterprise networks that are in Native Mode or the [EU Geo](/yammer/manage-security-and-compliance/manage-data-compliance) do not support network guests.</span></span>
> <span data-ttu-id="3c764-110">Microsoft 365 Les Yammer connectés ne peuvent pas prendre en charge l’accès invité actuellement, mais vous pouvez créer des groupes externes non connectés dans Yammer réseau.</span><span class="sxs-lookup"><span data-stu-id="3c764-110">Microsoft 365 Connected Yammer groups do not currently support guest access, but you can create non-connected, external groups in your Yammer network.</span></span> <span data-ttu-id="3c764-111">Voir [Créer et gérer des groupes externes dans Yammer](/yammer/work-with-external-users/create-and-manage-external-groups) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="3c764-111">See [Create and manage external groups in Yammer](/yammer/work-with-external-users/create-and-manage-external-groups) for instructions.</span></span>

<span data-ttu-id="3c764-112">L’accès invité dans les groupes est souvent utilisé dans le cadre d’un scénario plus large qui inclut SharePoint ou Teams.</span><span class="sxs-lookup"><span data-stu-id="3c764-112">Guest access in groups is often used as part of a broader scenario that includes SharePoint or Teams.</span></span> <span data-ttu-id="3c764-113">Ces services ont leurs propres paramètres de partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="3c764-113">These services have their own guest sharing settings.</span></span> <span data-ttu-id="3c764-114">Pour obtenir des instructions complètes sur la configuration du partage d’invités entre groupes, SharePoint et Teams, voir :</span><span class="sxs-lookup"><span data-stu-id="3c764-114">For complete instructions for setting up guest sharing across groups, SharePoint, and Teams, see:</span></span>

- [<span data-ttu-id="3c764-115">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="3c764-115">Collaborate with guests in a site</span></span>](../../solutions/collaborate-in-site.md)
- [<span data-ttu-id="3c764-116">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="3c764-116">Collaborate with guests in a team</span></span>](../../solutions/collaborate-as-team.md)

## <a name="manage-groups-guest-access"></a><span data-ttu-id="3c764-117">Gérer l’accès invité des groupes</span><span class="sxs-lookup"><span data-stu-id="3c764-117">Manage groups guest access</span></span>

<span data-ttu-id="3c764-118">Si vous souhaitez activer ou désactiver l’accès invité dans les groupes, vous pouvez le faire dans Microsoft 365 d’administration.</span><span class="sxs-lookup"><span data-stu-id="3c764-118">If you want to enable or disable guest access in groups, you can do so in the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="3c764-119">Dans le Centre d’administration, sélectionnez Afficher  tous Paramètres l’organisation et sous l’onglet \>  \>  **Services,** **sélectionnez Microsoft 365 groupes.**</span><span class="sxs-lookup"><span data-stu-id="3c764-119">In the admin center, go to **Show all** \> **Settings** \> **Org settings** and on the **Services** tab, select **Microsoft 365 groups**.</span></span>
  
2. <span data-ttu-id="3c764-120">Dans la page **Microsoft 365** groupes, choisissez si vous souhaitez laisser des personnes extérieures à votre organisation accéder aux ressources de groupe ou laisser les propriétaires de groupes ajouter des personnes extérieures à votre organisation à des groupes.</span><span class="sxs-lookup"><span data-stu-id="3c764-120">On the **Microsoft 365 Groups** page, choose whether you want to let people outside your organization access group resources or let group owners add people outside your organization to groups.</span></span>

## <a name="add-guests-to-a-microsoft-365-group-from-the-admin-center"></a><span data-ttu-id="3c764-121">Ajouter des invités à un groupe Microsoft 365 à partir du Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="3c764-121">Add guests to a Microsoft 365 group from the admin center</span></span>

<span data-ttu-id="3c764-122">Si l’invité existe déjà dans votre annuaire, vous pouvez l’ajouter à vos groupes à partir du centre Microsoft 365'administration.</span><span class="sxs-lookup"><span data-stu-id="3c764-122">If the guest already exists in your directory, you can add them to your groups from the Microsoft 365 admin center.</span></span> <span data-ttu-id="3c764-123">(Les groupes avec appartenance dynamique doivent être [gérés Azure Active Directory](/azure/active-directory/enterprise-users/groups-create-rule).)</span><span class="sxs-lookup"><span data-stu-id="3c764-123">(Groups with dynamic membership must be [managed in Azure Active Directory](/azure/active-directory/enterprise-users/groups-create-rule).)</span></span>
  
1. <span data-ttu-id="3c764-124">Dans le Centre d’administration, allez à la page   >  **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="3c764-124">In the admin center, go to the **Groups** > **Groups** page.</span></span>
  
2. <span data-ttu-id="3c764-125">Cliquez sur le groupe à qui vous souhaitez ajouter l’invité, puis sélectionnez Afficher **tout et gérer** les membres sous **l’onglet Membres.**</span><span class="sxs-lookup"><span data-stu-id="3c764-125">Click the group you want to add the guest to, and select **View all and manage members** on the **Members** tab.</span></span> 
  
4. <span data-ttu-id="3c764-126">Sélectionnez **Ajouter** des membres et choisissez le nom de l’invité que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="3c764-126">Select **Add members**, and choose the name of the guest you want to add.</span></span>
    
5. <span data-ttu-id="3c764-127">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3c764-127">Select **Save**.</span></span>

<span data-ttu-id="3c764-128">Si vous souhaitez ajouter un invité directement à l’annuaire, vous pouvez ajouter Azure Active Directory utilisateurs [de collaboration B2B](/azure/active-directory/b2b/add-users-administrator)dans le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="3c764-128">If you want to add a guest to the directory directly, you can [Add Azure Active Directory B2B collaboration users in the Azure portal](/azure/active-directory/b2b/add-users-administrator).</span></span>

<span data-ttu-id="3c764-129">Si vous souhaitez modifier les informations d’un invité, vous pouvez ajouter ou mettre à jour les informations de profil d’un utilisateur à [l’aide Azure Active Directory](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="3c764-129">If you want to edit any of a guest's information, you can [Add or update a user's profile information using Azure Active Directory](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

## <a name="related-content"></a><span data-ttu-id="3c764-130">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="3c764-130">Related content</span></span>

<span data-ttu-id="3c764-131">[Bloquer les utilisateurs invités d’un groupe spécifique](../../solutions/per-group-guest-access.md) (article)</span><span class="sxs-lookup"><span data-stu-id="3c764-131">[Block guest users from a specific group](../../solutions/per-group-guest-access.md) (article)</span></span>

<span data-ttu-id="3c764-132">[Gérer l’appartenance à un groupe dans Microsoft 365'administration centrale](add-or-remove-members-from-groups.md) (article)</span><span class="sxs-lookup"><span data-stu-id="3c764-132">[Manage group membership in the Microsoft 365 admin center](add-or-remove-members-from-groups.md) (article)</span></span>
  
<span data-ttu-id="3c764-133">[Azure Active Directory’accès aux données](/azure/active-directory/active-directory-azure-ad-controls-perform-access-review) (article)</span><span class="sxs-lookup"><span data-stu-id="3c764-133">[Azure Active Directory access reviews](/azure/active-directory/active-directory-azure-ad-controls-perform-access-review) (article)</span></span>

<span data-ttu-id="3c764-134">[Set-AzureADUser](/powershell/module/azuread/set-azureaduser) (article)</span><span class="sxs-lookup"><span data-stu-id="3c764-134">[Set-AzureADUser](/powershell/module/azuread/set-azureaduser) (article)</span></span>