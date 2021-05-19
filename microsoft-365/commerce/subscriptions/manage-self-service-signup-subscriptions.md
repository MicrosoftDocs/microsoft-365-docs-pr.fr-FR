---
title: Gérer les abonnements d’inscription en libre-service
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: jkinma, jmueller
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- commerce_subscriptions
search.appverid: MET150
description: Découvrez comment gérer les abonnements gratuits à l’inscription en libre-service pour votre organisation.
ms.date: 03/17/2021
ms.openlocfilehash: 741c9e0b45f127ffc0753b34982073f90c525d5b
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52536069"
---
# <a name="manage-self-service-sign-up-subscriptions"></a><span data-ttu-id="b2f58-103">Gérer les abonnements d’inscription en libre-service</span><span class="sxs-lookup"><span data-stu-id="b2f58-103">Manage self-service sign-up subscriptions</span></span>

## <a name="what-are-self-service-sign-up-subscriptions"></a><span data-ttu-id="b2f58-104">Qu’est-ce que les abonnements en libre-service ?</span><span class="sxs-lookup"><span data-stu-id="b2f58-104">What are self-service sign-up subscriptions?</span></span>

<span data-ttu-id="b2f58-105">Un nombre limité d’abonnements d’inscription libre-service est disponible pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b2f58-105">There are a limited number of free self-service sign-up subscriptions available for users in your organization to sign up for.</span></span> <span data-ttu-id="b2f58-106">Un utilisateur peut uniquement s’inscrire et utiliser un abonnement d’inscription en libre-service pour lui-même.</span><span class="sxs-lookup"><span data-stu-id="b2f58-106">A user can only sign up for and use a self-service sign-up subscription for themselves.</span></span> <span data-ttu-id="b2f58-107">Vous gérez les abonnements d’inscription en libre-service en bloquant l’inscription des utilisateurs et en supprimant les abonnements gratuits pour les utilisateurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="b2f58-107">You manage self-service sign-up subscriptions by blocking users from signing up, and by deleting free subscriptions that users have signed up for.</span></span> <span data-ttu-id="b2f58-108">Pour plus d’informations sur l’inscription en libre-service et les abonnements disponibles, voir l’utilisation de l’inscription en [libre-service dans votre organisation.](../../admin/misc/self-service-sign-up.md)</span><span class="sxs-lookup"><span data-stu-id="b2f58-108">For more information about self-service sign up and the available subscriptions, see [Using self-service sign up in your organization](../../admin/misc/self-service-sign-up.md).</span></span>

## <a name="view-a-list-of-self-service-sign-up-subscriptions"></a><span data-ttu-id="b2f58-109">Afficher la liste des abonnements d’inscription en libre-service</span><span class="sxs-lookup"><span data-stu-id="b2f58-109">View a list of self-service sign-up subscriptions</span></span>

1. <span data-ttu-id="b2f58-110">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="b2f58-110">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="b2f58-111">Sous **l’onglet Produits,** sélectionnez l’icône de filtre, puis sélectionnez **Gratuit**.</span><span class="sxs-lookup"><span data-stu-id="b2f58-111">On the **Products** tab, select the filter icon, then select **Free**.</span></span> <span data-ttu-id="b2f58-112">Une liste de tous les abonnements d’inscription en libre-service s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b2f58-112">A list of all self-service sign-up subscriptions is displayed.</span></span>

## <a name="how-are-these-subscriptions-different-from-self-service-purchase-subscriptions"></a><span data-ttu-id="b2f58-113">En quoi ces abonnements sont-ils différents des abonnements d’achat en libre-service ?</span><span class="sxs-lookup"><span data-stu-id="b2f58-113">How are these subscriptions different from self-service purchase subscriptions?</span></span>

<span data-ttu-id="b2f58-114">Les abonnements d’inscription en libre-service sont gratuits et sont disponibles pour une plus grande liste de produits que les abonnements d’achat en libre-service.</span><span class="sxs-lookup"><span data-stu-id="b2f58-114">Self-service sign-up subscriptions are free and are available for a larger list of products than self-service purchase subscriptions.</span></span> <span data-ttu-id="b2f58-115">Lorsqu’un utilisateur s’est abonné à un abonnement d’achat en libre-service, il est responsable de son paiement.</span><span class="sxs-lookup"><span data-stu-id="b2f58-115">When a user signs up for a self-service purchase subscription, they're responsible for paying for it.</span></span> <span data-ttu-id="b2f58-116">Les abonnements à des achats en libre-service sont disponibles uniquement pour les produits Power Platform (Power BI, Power Apps et Power Automate), Project et Visio.</span><span class="sxs-lookup"><span data-stu-id="b2f58-116">Self-service purchase subscriptions are only available for Power Platform products (Power BI, Power Apps, and Power Automate), Project, and Visio.</span></span> <span data-ttu-id="b2f58-117">Pour plus d’informations, [voir le FAQ sur les achats en libre-service.](self-service-purchase-faq.yml)</span><span class="sxs-lookup"><span data-stu-id="b2f58-117">For more information, see [Self-service purchase FAQ](self-service-purchase-faq.yml).</span></span>

## <a name="block-users-from-signing-up"></a><span data-ttu-id="b2f58-118">Empêcher les utilisateurs de s’inscrire</span><span class="sxs-lookup"><span data-stu-id="b2f58-118">Block users from signing up</span></span>

<span data-ttu-id="b2f58-119">Vous utilisez la cmdlet [**Set-MsolCompanySettings**](/powershell/module/msonline/set-msolcompanysettings?preserve-view=true&view=azureadps-1.0) avec le paramètre **AllowAdHocSubscriptions** pour contrôler si les utilisateurs peuvent s’inscrire à des abonnements d’inscription en libre-service.</span><span class="sxs-lookup"><span data-stu-id="b2f58-119">You use the [**Set-MsolCompanySettings**](/powershell/module/msonline/set-msolcompanysettings?preserve-view=true&view=azureadps-1.0) cmdlet with the **AllowAdHocSubscriptions** parameter to control whether users can sign up for self-service sign-up subscriptions.</span></span> <span data-ttu-id="b2f58-120">Pour plus d’informations, [voir Comment contrôler les paramètres libre-service ?](/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span><span class="sxs-lookup"><span data-stu-id="b2f58-120">For more information, see [How do I control self-service settings?](/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span></span>

## <a name="delete-a-self-service-sign-up-subscription"></a><span data-ttu-id="b2f58-121">Supprimer un abonnement d’inscription en libre-service</span><span class="sxs-lookup"><span data-stu-id="b2f58-121">Delete a self-service sign-up subscription</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2f58-122">Lorsque vous supprimez un abonnement d’inscription en libre-service, vous bloquez l’accès de tous les utilisateurs à leurs données et messages électroniques et supprimez toutes les données et tous les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="b2f58-122">When you delete a self-service sign-up subscription, you block all users from accessing their data and email and delete all data and email.</span></span>

1. <span data-ttu-id="b2f58-123">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="b2f58-123">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="b2f58-124">Sous **l’onglet Produits,** sélectionnez l’icône de filtre, puis sélectionnez **Gratuit**.</span><span class="sxs-lookup"><span data-stu-id="b2f58-124">On the **Products** tab, select the filter icon, then select **Free**.</span></span>
3. <span data-ttu-id="b2f58-125">Sélectionnez l’abonnement d’inscription en libre-service à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b2f58-125">Select the self-service sign-up subscription that you want to delete.</span></span> 
4. <span data-ttu-id="b2f58-126">Dans la page détails de l’abonnement, dans la section Abonnements et **paramètres de** paiement, sélectionnez **Supprimer l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="b2f58-126">On the subscription details page, in the **Subscriptions and payment settings** section, select **Delete subscription**.</span></span>
5. <span data-ttu-id="b2f58-127">Dans le **volet Supprimer l’abonnement,** cochez la case, puis **supprimez l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="b2f58-127">In the **Delete subscription** pane, select the check box, then select **Delete subscription**.</span></span>

## <a name="i-have-a-self-service-sign-up-subscription-that-blocks-directory-deletion"></a><span data-ttu-id="b2f58-128">J’ai un abonnement en libre-service qui bloque la suppression d’annuaires</span><span class="sxs-lookup"><span data-stu-id="b2f58-128">I have a self-service sign-up subscription that blocks directory deletion</span></span>

<span data-ttu-id="b2f58-129">Les produits d’inscription en libre-service que les utilisateurs individuels peuvent inscrire créent également un utilisateur invité pour l’authentification dans votre annuaire Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b2f58-129">The self-service sign-up products that individual users can sign up for also create a guest user for authentication in your Azure AD directory.</span></span> <span data-ttu-id="b2f58-130">Pour éviter la perte de données, ces produits en libre-service bloquent les suppressions d’annuaires jusqu’à ce qu’elles soient entièrement supprimées de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="b2f58-130">To avoid data loss, these self-service products block directory deletions until they're fully deleted from the directory.</span></span> <span data-ttu-id="b2f58-131">Ils peuvent uniquement être supprimés par l’administrateur Azure AD. Pour plus d’informations, [voir Supprimer un répertoire dans Azure Active Directory](/azure/active-directory/users-groups-roles/directory-delete-howto).</span><span class="sxs-lookup"><span data-stu-id="b2f58-131">They can only be deleted by the Azure AD admin. For more information, see [Delete a directory in Azure Active Directory](/azure/active-directory/users-groups-roles/directory-delete-howto).</span></span>
