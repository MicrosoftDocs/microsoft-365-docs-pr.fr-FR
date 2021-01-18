---
title: Découvrir la rétention pour Yammer
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Découvrir les stratégies de rétention qui s’appliquent à Microsoft Teams.
ms.openlocfilehash: ce3e298d5d0a034b30865e9fa1278325ce25c1e6
ms.sourcegitcommit: 27cb4591e08f62ba0a08d6dcf224bf2039034fe5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2021
ms.locfileid: "49883703"
---
# <a name="learn-about-retention-for-yammer"></a><span data-ttu-id="50e31-103">Découvrir la rétention pour Yammer</span><span class="sxs-lookup"><span data-stu-id="50e31-103">Learn about retention for Yammer</span></span>

><span data-ttu-id="50e31-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="50e31-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

> [!NOTE]
> <span data-ttu-id="50e31-105">Cette fonctionnalité est disponible en version préliminaire et n’est pas encore disponible pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="50e31-105">This feature is in preview and not yet available for all customers.</span></span>

<span data-ttu-id="50e31-106">Les informations contenues dans cet article complètent l’article [Découvrir la rétention](retention.md) car elles contiennent des informations spécifiques à Yammer.</span><span class="sxs-lookup"><span data-stu-id="50e31-106">The information in this article supplements [Learn about retention](retention.md) because it has information that's specific to Yammer.</span></span>

<span data-ttu-id="50e31-107">Pour les autres charges de travail, consultez:</span><span class="sxs-lookup"><span data-stu-id="50e31-107">For other workloads, see:</span></span>

- [<span data-ttu-id="50e31-108">En savoir plus sur la rétention dans SharePoint et OneDrive</span><span class="sxs-lookup"><span data-stu-id="50e31-108">Learn about retention for SharePoint and OneDrive</span></span>](retention-policies-sharepoint.md)
- [<span data-ttu-id="50e31-109">En savoir plus sur la rétention dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="50e31-109">Learn about retention for Microsoft Teams</span></span>](retention-policies-teams.md)
- [<span data-ttu-id="50e31-110">Découvrir la rétention pour Exchange</span><span class="sxs-lookup"><span data-stu-id="50e31-110">Learn about retention for Exchange</span></span>](retention-policies-exchange.md)

## <a name="whats-included-for-retention-and-deletion"></a><span data-ttu-id="50e31-111">Éléments composant la rétention et la suppression</span><span class="sxs-lookup"><span data-stu-id="50e31-111">What's included for retention and deletion</span></span>

<span data-ttu-id="50e31-112">Les éléments Yammer suivants peuvent être conservés et supprimés à l’aide des stratégies de rétention Yammer: Messages de communauté et messages privés.</span><span class="sxs-lookup"><span data-stu-id="50e31-112">The following Yammer items can be retained and deleted by using retention policies for Yammer: Community messages and private messages.</span></span>

<span data-ttu-id="50e31-113">Les réactions des autres personnes sous la forme d’émoticônes ne sont pas incluses dans ces messages.</span><span class="sxs-lookup"><span data-stu-id="50e31-113">Reactions from others in the form of emoticons are not included in these messages.</span></span>

## <a name="how-retention-works-with-yammer"></a><span data-ttu-id="50e31-114">Fonctionnement de la rétention pour Yammer</span><span class="sxs-lookup"><span data-stu-id="50e31-114">How retention works with Yammer</span></span>

<span data-ttu-id="50e31-115">Vous pouvez utiliser une stratégie de rétention pour conserver et supprimer des messages de communauté et des messages privés dans Yammer.</span><span class="sxs-lookup"><span data-stu-id="50e31-115">You can use a retention policy to retain and delete community messages and private messages in Yammer.</span></span> <span data-ttu-id="50e31-116">Les messages privés sont stockées dans un dossier masqué de la boîte aux lettres de chaque utilisateur participant à la conversation. Les messages communautaires sont stockés dans un dossier masqué similaire dans la boîte aux lettres de groupe de la communauté.</span><span class="sxs-lookup"><span data-stu-id="50e31-116">Private messages are stored in a hidden folder in the mailbox of each user included in the message, and community messages are stored in a similar hidden folder in the group mailbox for the community.</span></span>

<span data-ttu-id="50e31-117">Les messages Yammer ne sont pas affectés par les stratégies de rétention configurées pour les boîtes aux lettres des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="50e31-117">Yammer messages are not affected by retention policies that are configured for user or group mailboxes.</span></span> <span data-ttu-id="50e31-118">Même si les messages Yammer sont stockés dans Exchange, ces données Yammer sont incluses uniquement par une stratégie de rétention configurée pour les **messages de la communauté Yammer** et les emplacements des **messages privés Yammer**.</span><span class="sxs-lookup"><span data-stu-id="50e31-118">Even though Yammer messages are stored in Exchange, this Yammer data is included only by a retention policy that's configured for the **Yammer community messages** and **Yammer private messages** locations.</span></span>

> [!NOTE]
> <span data-ttu-id="50e31-119">Si un utilisateur est inclus dans une stratégie de rétention active qui conserve les données Yammer et que vous supprimez une boîte aux lettres d’un utilisateur inclus dans cette stratégie, la boîte aux lettres est convertie en [boîte aux lettres inactive](inactive-mailboxes-in-office-365.md) pour conserver les données Yammer.</span><span class="sxs-lookup"><span data-stu-id="50e31-119">If a user is included in an active retention policy that retains Yammer data and you a delete a mailbox of a user who is included in this policy, to retain the Yammer data, the mailbox is converted into an [inactive mailbox](inactive-mailboxes-in-office-365.md).</span></span> <span data-ttu-id="50e31-120">Si vous n’avez pas besoin de conserver ces données Yammer pour l’utilisateur, excluez son compte de la stratégie de rétention avant de supprimer sa boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="50e31-120">If you don't need to retain this Yammer data for the user, exclude the user account from the retention policy before you delete their mailbox.</span></span>

<span data-ttu-id="50e31-121">Une fois qu'une politique de rétention est configurée pour les messages Yammer, une tâche de temporisation du service Exchange évalue périodiquement les éléments du dossier caché où sont stockés ces messages Yammer.</span><span class="sxs-lookup"><span data-stu-id="50e31-121">After a retention policy is configured for Yammer messages, a timer job from the Exchange service periodically evaluates items in the hidden folder where these Yammer messages are stored.</span></span> <span data-ttu-id="50e31-122">Le travail de chronométrage prend jusqu'à sept jours.</span><span class="sxs-lookup"><span data-stu-id="50e31-122">The timer job takes up to seven days to run.</span></span> <span data-ttu-id="50e31-123">Lorsque ces éléments ont expiré leur période de rétention, ils sont déplacés vers le dossier SubstrateHolds - un autre dossier caché qui se trouve dans la boîte aux lettres de chaque utilisateur ou groupe pour stocker les éléments « à suppression douce » avant qu'ils ne soient définitivement supprimés.</span><span class="sxs-lookup"><span data-stu-id="50e31-123">When these items have expired their retention period, they are moved to the SubstrateHolds folder—a hidden folder that's in every user or group mailbox to store "soft-deleted" items before they are permanently deleted.</span></span>

<span data-ttu-id="50e31-124">Une fois qu'une politique de rétention est configurée pour les messages Yammer, les chemins que prend le contenu dépendent du fait que la politique de rétention doit conserver puis supprimer, conserver seulement ou supprimer seulement.</span><span class="sxs-lookup"><span data-stu-id="50e31-124">After a retention policy is configured for Yammer messages, the paths the content takes depend on whether the retention policy is to retain and then delete, to retain only, or delete only.</span></span>

<span data-ttu-id="50e31-125">Lorsque la politique de rétention consiste à conserver puis à supprimer :</span><span class="sxs-lookup"><span data-stu-id="50e31-125">When the retention policy is to retain and then delete:</span></span>

![Diagramme de flux de rétention des messages Yammer](../media/yammerretentionlifecycle.png)

<span data-ttu-id="50e31-127">Pour les deux voies du diagramme :</span><span class="sxs-lookup"><span data-stu-id="50e31-127">For the two paths in the diagram:</span></span>

1. <span data-ttu-id="50e31-128">**Si un message Yammer est édité ou supprimé** par l'utilisateur pendant la période de conservation, le message original est immédiatement copié (s'il est édité) ou déplacé (s'il est supprimé) dans le dossier SubstrateHolds.</span><span class="sxs-lookup"><span data-stu-id="50e31-128">**If a Yammer message is edited or deleted** by the user during the retention period, the original message is immediately copied (if edited) or moved (if deleted) to the SubstrateHolds folder.</span></span> <span data-ttu-id="50e31-129">Le message y est stocké jusqu'à l'expiration de la période de conservation, puis le message est supprimé définitivement.</span><span class="sxs-lookup"><span data-stu-id="50e31-129">The message is stored there until the retention period expires and then the message is immediately permanently deleted.</span></span>

2. <span data-ttu-id="50e31-130">**Si un message Yammer n'est pas supprimé** et pour les messages courants après édition, le message est déplacé dans le dossier SubstrateHolds après l'expiration de la période de conservation.</span><span class="sxs-lookup"><span data-stu-id="50e31-130">**If a Yammer message is not deleted** and for current messages after editing, the message is moved to the SubstrateHolds folder after the retention period expires.</span></span> <span data-ttu-id="50e31-131">Cette action prend jusqu'à sept jours à compter de la date d'expiration.</span><span class="sxs-lookup"><span data-stu-id="50e31-131">This action takes up to seven days from the expiry date.</span></span> <span data-ttu-id="50e31-132">Lorsque le message se trouve dans le dossier SubstrateHolds, il est alors définitivement supprimé.</span><span class="sxs-lookup"><span data-stu-id="50e31-132">When the message is in the SubstrateHolds folder, it is then immediately permanently deleted.</span></span> 

> [!NOTE]
> <span data-ttu-id="50e31-133">Les messages dans le dossier SubstrateHolds sont recherchés par les outils d'eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="50e31-133">Messages in the SubstrateHolds folder are searchable by eDiscovery tools.</span></span> <span data-ttu-id="50e31-134">Tant que les messages ne sont pas définitivement supprimés (dans le dossier SubstrateHolds), ils restent recherchés par les outils d'eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="50e31-134">Until messages are permanently deleted (in the SubstrateHolds folder), they remain searchable by eDiscovery tools.</span></span>

<span data-ttu-id="50e31-135">Lorsque la stratégie de rétention consiste à conserver uniquement ou à supprimer uniquement, les chemins d'accès au contenu sont des variantes de rétention et de suppression.</span><span class="sxs-lookup"><span data-stu-id="50e31-135">When the retention policy is retain-only, or delete-only, the content's paths are variations of retain and delete.</span></span>

### <a name="content-paths-for-retain-only-retention-policy"></a><span data-ttu-id="50e31-136">Chemins d’accès au contenu pour la stratégie de rétention de conservation uniquement</span><span class="sxs-lookup"><span data-stu-id="50e31-136">Content paths for retain-only retention policy</span></span>

1. <span data-ttu-id="50e31-137">**Si un message Yammer est édité ou supprimé**:Une copie du message original est immédiatement créée dans le dossier SubstrateHolds et y est conservée jusqu'à l'expiration de la période de conservation.</span><span class="sxs-lookup"><span data-stu-id="50e31-137">**If a Yammer message is edited or deleted**: A copy of the original message is immediately created in the SubstrateHolds folder and retained there until the retention period expires.</span></span> <span data-ttu-id="50e31-138">Ensuite, le message est définitivement supprimé du dossier SubstrateHolds.</span><span class="sxs-lookup"><span data-stu-id="50e31-138">Then the message is immediately permanently deleted from the SubstrateHolds folder.</span></span>

2. <span data-ttu-id="50e31-139">**Si le message Yammer n'est pas modifié ou supprimé** et pour les messages courants après édition pendant la période de rétention : Rien ne se passe avant et après la période de rétention ; le message reste dans son emplacement d'origine.</span><span class="sxs-lookup"><span data-stu-id="50e31-139">**If the Yammer message is not modified or deleted** and for current messages after editing during the retention period: Nothing happens before and after the retention period; the message remains in its original location.</span></span>

### <a name="content-paths-for-delete-only-retention-policy"></a><span data-ttu-id="50e31-140">Chemins d’accès du contenu pour la stratégie de rétention de suppression uniquement</span><span class="sxs-lookup"><span data-stu-id="50e31-140">Content paths for delete-only retention policy</span></span>

1. <span data-ttu-id="50e31-141">**Si le message Yammer n’est pas supprimé** pendant la période de rétention : à la fin de la période de rétention, il est déplacé vers le dossier SubstrateHolds.</span><span class="sxs-lookup"><span data-stu-id="50e31-141">**If the Yammer message is not deleted** during the retention period: At the end of the retention period, the message is moved to the SubstrateHolds folder.</span></span> <span data-ttu-id="50e31-142">Cette action prend jusqu'à sept jours à compter de la date d'expiration.</span><span class="sxs-lookup"><span data-stu-id="50e31-142">This action takes up to seven days from the expiry date.</span></span> <span data-ttu-id="50e31-143">Ensuite, le message est définitivement supprimé du dossier SubstrateHolds.</span><span class="sxs-lookup"><span data-stu-id="50e31-143">Then the message is immediately permanently deleted from the SubstrateHolds folder.</span></span>

2. <span data-ttu-id="50e31-144">**Si le message Yammer est supprimé par l'utilisateur** pendant cette période, l'élément est immédiatement déplacé vers le dossier SubstrateHolds où il est immédiatement supprimé définitivement.</span><span class="sxs-lookup"><span data-stu-id="50e31-144">**If the Yammer message is deleted by the user** during the period, the item is immediately moved to the SubstrateHolds folder where it is immediately permanently deleted.</span></span>


## <a name="messages-and-external-users"></a><span data-ttu-id="50e31-145">Messages et utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="50e31-145">Messages and external users</span></span>

<span data-ttu-id="50e31-146">Par défaut, une stratégie de rétention pour les messages privés Yammer s’applique à tous les utilisateurs de votre organisation, mais pas aux utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="50e31-146">By default, a retention policy for Yammer private messages applies to all users in your organization, but not external users.</span></span> <span data-ttu-id="50e31-147">Vous pouvez appliquer une stratégie de rétention à des utilisateurs externes si vous utilisez le **Choisir Utilisateur** puis spécifiez leur compte.</span><span class="sxs-lookup"><span data-stu-id="50e31-147">You can apply a retention policy to external users if you use the **Choose user** and specify their account.</span></span> 

<span data-ttu-id="50e31-148">Pour l’instant, les utilisateurs invités B2B Azure ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="50e31-148">At this time, Azure B2B guest users are not supported.</span></span>

## <a name="when-a-user-leaves-the-organization"></a><span data-ttu-id="50e31-149">Lorsqu’un utilisateur quitte l’organisation</span><span class="sxs-lookup"><span data-stu-id="50e31-149">When a user leaves the organization</span></span> 

<span data-ttu-id="50e31-150">Si un utilisateur quitte votre organisation et que son compte Microsoft 365 est supprimé, leurs messages privés Yammer soumis à une rétention sont stockés dans une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="50e31-150">If a user leaves your organization and their Microsoft 365 account is deleted, their Yammer private messages that are subject to retention are stored in an inactive mailbox.</span></span> <span data-ttu-id="50e31-151">Les messages de conversation restent soumis à une stratégie de rétention qui a été placée sur l’utilisateur avant que sa boîte aux lettres ne soit inactive et les contenus sont disponibles pour une recherche eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="50e31-151">These messages remain subject to any retention policy that was placed on the user before their mailbox was made inactive, and the contents are available to an eDiscovery search.</span></span> <span data-ttu-id="50e31-152">Pour plus d’informations, consultez [Boîtes aux lettres inactives dans Exchange Online](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="50e31-152">For more information, see [Inactive mailboxes in Exchange Online](inactive-mailboxes-in-office-365.md).</span></span> 

<span data-ttu-id="50e31-153">Si l’utilisateur a stocké des fichiers dans Yammer, consultez la [section équivalente](retention-policies-sharepoint.md#when-a-user-leaves-the-organization) pour SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="50e31-153">If the user stored any files in Yammer, see the [equivalent section](retention-policies-sharepoint.md#when-a-user-leaves-the-organization) for SharePoint and OneDrive.</span></span>

## <a name="limitations"></a><span data-ttu-id="50e31-154">Limites</span><span class="sxs-lookup"><span data-stu-id="50e31-154">Limitations</span></span>

<span data-ttu-id="50e31-155">Les stratégies de rétention de Yammer sont actuellement en préversion et nous travaillons continuellement sur l’optimisation des fonctionnalités de rétention.</span><span class="sxs-lookup"><span data-stu-id="50e31-155">Yammer retention policies are currently in preview and we're continuously working on optimizing retention functionality.</span></span> <span data-ttu-id="50e31-156">En attendant, voici quelques limitations à prendre en compte lors de l’utilisation de la rétention pour les messages communautaires et les messages privés Yammer:</span><span class="sxs-lookup"><span data-stu-id="50e31-156">In the meantime, be aware of the following limitation when you use retention for Yammer community messages and private messages:</span></span>

- <span data-ttu-id="50e31-157">Lorsque vous sélectionnez **Choisir les utilisateurs** pour l’emplacement des **messages privés Yammer**, les invités et les utilisateurs qui n’utilisent pas de boîte aux lettres peuvent s’afficher.</span><span class="sxs-lookup"><span data-stu-id="50e31-157">When you select **Choose users** for the **Yammer private messages** location, you might see guests and non-mailbox users.</span></span> <span data-ttu-id="50e31-158">Les stratégies de rétention ne sont pas conçues pour ces utilisateurs. Ne les sélectionnez pas.</span><span class="sxs-lookup"><span data-stu-id="50e31-158">Retention policies aren't designed for these users, so don't select them.</span></span>

## <a name="configuration-guidance"></a><span data-ttu-id="50e31-159">Instructions de configuration</span><span class="sxs-lookup"><span data-stu-id="50e31-159">Configuration guidance</span></span>

<span data-ttu-id="50e31-160">Si vous n’avez jamais configurer la rétention dans Microsoft 365, voir [Prise en main des stratégies et des étiquettes de rétention](get-started-with-retention.md).</span><span class="sxs-lookup"><span data-stu-id="50e31-160">If you're new to configuring retention in Microsoft 365, see [Get started with retention policies and retention labels](get-started-with-retention.md).</span></span>

<span data-ttu-id="50e31-161">Si vous êtes prêt à configurer une stratégie de rétention pour Yammer, voir [Créer et configurer des stratégies de rétention](create-retention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="50e31-161">If you're ready to configure a retention policy for Yammer, see [Create and configure retention policies](create-retention-policies.md).</span></span>
