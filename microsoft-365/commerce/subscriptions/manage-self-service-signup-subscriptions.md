---
title: Gérer les abonnements d’abonnement en libre-service
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- commerce
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
description: Découvrez comment gérer des abonnements gratuits en libre-service pour votre organisation.
ms.openlocfilehash: 589466908dcda1461011f046b99be21788c1a018
ms.sourcegitcommit: 20d1158c54a5058093eb8aac23d7e4dc68054688
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2020
ms.locfileid: "49376304"
---
# <a name="manage-self-service-sign-up-subscriptions"></a><span data-ttu-id="a1302-103">Gérer les abonnements d’abonnement en libre-service</span><span class="sxs-lookup"><span data-stu-id="a1302-103">Manage self-service sign-up subscriptions</span></span>

## <a name="what-are-self-service-sign-up-subscriptions"></a><span data-ttu-id="a1302-104">Qu’est-ce que les abonnements d’abonnement en libre-service ?</span><span class="sxs-lookup"><span data-stu-id="a1302-104">What are self-service sign-up subscriptions?</span></span>

<span data-ttu-id="a1302-105">Il existe un nombre limité d’abonnements gratuits d’abonnement libre-service disponibles pour les utilisateurs de votre organisation qui s’inscrivent à.</span><span class="sxs-lookup"><span data-stu-id="a1302-105">There are a limited number of free self-service sign-up subscriptions available for users in your organization to sign up for.</span></span> <span data-ttu-id="a1302-106">Un utilisateur peut uniquement s’inscrire et utiliser un abonnement d’abonnement libre-service pour lui-même.</span><span class="sxs-lookup"><span data-stu-id="a1302-106">A user can only sign up for and use a self-service sign-up subscription for themselves.</span></span> <span data-ttu-id="a1302-107">Vous pouvez gérer les abonnements d’abonnement en libre-service en bloquant les utilisateurs de s’inscrire et en supprimant les abonnements gratuits pour lesquels les utilisateurs se sont inscrits.</span><span class="sxs-lookup"><span data-stu-id="a1302-107">You manage self-service sign-up subscriptions by blocking users from signing up, and by deleting free subscriptions that users have signed up for.</span></span> <span data-ttu-id="a1302-108">Pour plus d’informations sur l’inscription en libre-service et les abonnements disponibles, consultez la rubrique [utilisation de l’authentification en libre-service dans votre organisation](../../admin/misc/self-service-sign-up.md).</span><span class="sxs-lookup"><span data-stu-id="a1302-108">For more information about self-service sign up and the available subscriptions, see [Using self-service sign up in your organization](../../admin/misc/self-service-sign-up.md).</span></span>

## <a name="view-a-list-of-self-service-sign-up-subscriptions"></a><span data-ttu-id="a1302-109">Afficher la liste des abonnements d’abonnement en libre-service</span><span class="sxs-lookup"><span data-stu-id="a1302-109">View a list of self-service sign-up subscriptions</span></span>

1. <span data-ttu-id="a1302-110">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="a1302-110">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="a1302-111">Sur l’onglet **produits** , sélectionnez l’icône de filtre, puis sélectionnez **libre**.</span><span class="sxs-lookup"><span data-stu-id="a1302-111">On the **Products** tab, select the filter icon, then select **Free**.</span></span> <span data-ttu-id="a1302-112">La liste de tous les abonnements d’abonnement libre-service s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a1302-112">A list of all self-service sign-up subscriptions is displayed.</span></span>

## <a name="how-are-these-subscriptions-different-from-self-service-purchase-subscriptions"></a><span data-ttu-id="a1302-113">En quoi ces abonnements sont-ils différents des abonnements aux achats en libre-service ?</span><span class="sxs-lookup"><span data-stu-id="a1302-113">How are these subscriptions different from self-service purchase subscriptions?</span></span>

<span data-ttu-id="a1302-114">Les abonnements d’inscription en libre-service sont gratuits et sont disponibles pour une liste plus importante de produits que les abonnements aux achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="a1302-114">Self-service sign-up subscriptions are free and are available for a larger list of products than self-service purchase subscriptions.</span></span> <span data-ttu-id="a1302-115">Lorsqu’un utilisateur s’inscrit à un abonnement d’achat en libre-service, il est responsable du paiement.</span><span class="sxs-lookup"><span data-stu-id="a1302-115">When a user signs up for a self-service purchase subscription, they're responsible for paying for it.</span></span> <span data-ttu-id="a1302-116">Les abonnements aux achats en libre-service sont disponibles uniquement pour les produits Power Platform (Power BI, Power Apps et Power automate), Project et Visio.</span><span class="sxs-lookup"><span data-stu-id="a1302-116">Self-service purchase subscriptions are only available for Power Platform products (Power BI, Power Apps, and Power Automate), Project, and Visio.</span></span> <span data-ttu-id="a1302-117">Pour plus d’informations, consultez la rubrique [Forum aux questions sur les achats en libre-service](self-service-purchase-faq.md).</span><span class="sxs-lookup"><span data-stu-id="a1302-117">For more information, see [Self-service purchase FAQ](self-service-purchase-faq.md).</span></span>

## <a name="block-users-from-signing-up"></a><span data-ttu-id="a1302-118">Empêcher les utilisateurs de s’inscrire</span><span class="sxs-lookup"><span data-stu-id="a1302-118">Block users from signing up</span></span>

<span data-ttu-id="a1302-119">Vous utilisez la cmdlet [**Set-MsolCompanySettings**](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0&preserve-view=true) avec le paramètre **AllowAdHocSubscriptions** pour contrôler si les utilisateurs peuvent s’inscrire pour des abonnements d’abonnement en libre-service.</span><span class="sxs-lookup"><span data-stu-id="a1302-119">You use the [**Set-MsolCompanySettings**](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0&preserve-view=true) cmdlet with the **AllowAdHocSubscriptions** parameter to control whether users can sign up for self-service sign-up subscriptions.</span></span> <span data-ttu-id="a1302-120">Pour plus d’informations, voir [Comment puis-je contrôler les paramètres en libre-service ?](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span><span class="sxs-lookup"><span data-stu-id="a1302-120">For more information, see [How do I control self-service settings?](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span></span>

## <a name="delete-a-self-service-sign-up-subscription"></a><span data-ttu-id="a1302-121">Supprimer un abonnement d’abonnement libre-service</span><span class="sxs-lookup"><span data-stu-id="a1302-121">Delete a self-service sign-up subscription</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1302-122">Lorsque vous supprimez un abonnement d’abonnement libre-service, vous empêchez tous les utilisateurs d’accéder à leurs données et à leurs messages électroniques et de supprimer toutes les données et tous les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a1302-122">When you delete a self-service sign-up subscription, you block all users from accessing their data and email and delete all data and email.</span></span>

1. <span data-ttu-id="a1302-123">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="a1302-123">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="a1302-124">Sur l’onglet **produits** , sélectionnez l’icône de filtre, puis sélectionnez **libre**.</span><span class="sxs-lookup"><span data-stu-id="a1302-124">On the **Products** tab, select the filter icon, then select **Free**.</span></span>
3. <span data-ttu-id="a1302-125">Sélectionnez l’abonnement d’inscription libre-service que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a1302-125">Select the self-service sign-up subscription that you want to delete.</span></span> 
4. <span data-ttu-id="a1302-126">Sur la page Détails de l’abonnement, dans la section **paramètres d’abonnements et de paiement** , sélectionnez **Supprimer l’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="a1302-126">On the subscription details page, in the **Subscriptions and payment settings** section, select **Delete subscription**.</span></span>
5. <span data-ttu-id="a1302-127">Dans le volet **supprimer un abonnement** , activez la case à cocher, puis sélectionnez Supprimer l' **abonnement**.</span><span class="sxs-lookup"><span data-stu-id="a1302-127">In the **Delete subscription** pane, select the check box, then select **Delete subscription**.</span></span>

## <a name="i-have-a-self-service-sign-up-subscription-that-blocks-directory-deletion"></a><span data-ttu-id="a1302-128">J’ai un abonnement d’inscription libre-service qui bloque la suppression d’annuaire</span><span class="sxs-lookup"><span data-stu-id="a1302-128">I have a self-service sign-up subscription that blocks directory deletion</span></span>

<span data-ttu-id="a1302-129">Les produits d’abonnement en libre-service que des utilisateurs individuels peuvent également créer un utilisateur invité pour l’authentification dans votre répertoire Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a1302-129">The self-service sign-up products that individual users can sign up for also create a guest user for authentication in your Azure AD directory.</span></span> <span data-ttu-id="a1302-130">Pour éviter toute perte de données, ces produits en libre-service bloquent les suppressions d’annuaires jusqu’à ce qu’ils soient entièrement supprimés de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a1302-130">To avoid data loss, these self-service products block directory deletions until they're fully deleted from the directory.</span></span> <span data-ttu-id="a1302-131">Ils ne peuvent être supprimés que par l’administrateur Azure AD. Pour plus d’informations, consultez [la rubrique supprimer un répertoire dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto).</span><span class="sxs-lookup"><span data-stu-id="a1302-131">They can only be deleted by the Azure AD admin. For more information, see [Delete a directory in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto).</span></span>