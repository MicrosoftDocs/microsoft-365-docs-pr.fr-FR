---
title: Gérer les demandes de licence
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: micurn, nicholak
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- MACBillingLicensesRequests
- AdminSurgePortfolio
- commerce_licensing
search.appverid: MET150
description: Découvrez comment examiner et approuver ou refuser les demandes de licence des utilisateurs pour votre abonnement Microsoft 365 entreprise.
ms.date: 06/07/2021
ms.openlocfilehash: 23258d21ebb413c56323aa4dab25cee60baf2be0
ms.sourcegitcommit: a4c93a4c7d7db08fe3b032b58d5c7dbbb9476e90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "53256806"
---
# <a name="manage-license-requests"></a><span data-ttu-id="2d781-103">Gérer les demandes de licence</span><span class="sxs-lookup"><span data-stu-id="2d781-103">Manage license requests</span></span>

> [!NOTE]
> <span data-ttu-id="2d781-104">Les informations de cet article s’appliquent uniquement aux produits achetés en libre-service.</span><span class="sxs-lookup"><span data-stu-id="2d781-104">The information in this article only applies to self-service purchased products.</span></span> <span data-ttu-id="2d781-105">Pour en savoir plus, consultez [la faq sur l’achat en libre-service.](../subscriptions/self-service-purchase-faq.yml)</span><span class="sxs-lookup"><span data-stu-id="2d781-105">To learn more, see [Self-service purchase FAQ](../subscriptions/self-service-purchase-faq.yml).</span></span>

<span data-ttu-id="2d781-106">Si vous désactivez les achats en libre-service dans votre organisation, vous pouvez utiliser les demandes de licences pour gérer le processus de demande de licence pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2d781-106">If you disable self-service purchases in your organization, you can use licenses requests to manage the license request process for your users.</span></span> <span data-ttu-id="2d781-107">Lorsqu’un utilisateur tente d’effectuer un achat en libre-service pour un produit que vous avez bloqué, il peut soumettre une demande de licence à vous, l’administrateur. Lorsqu’ils font une demande, ils peuvent ajouter les noms d’autres utilisateurs qui ont également besoin de licences pour le produit.</span><span class="sxs-lookup"><span data-stu-id="2d781-107">When a user tries to make a self-service purchase for a product that you’ve blocked, they can submit a request for a license to you, the admin. When they make a request, they can add the names of other users who also need licenses for the product.</span></span>

> [!NOTE]
> <span data-ttu-id="2d781-108">Si vous bloquez les utilisateurs d’effectuer des achats en libre-service, Microsoft ne leur envoie pas de courriers électroniques marketing.</span><span class="sxs-lookup"><span data-stu-id="2d781-108">If you block users from making self-service purchases, Microsoft doesn’t send them marketing emails.</span></span> <span data-ttu-id="2d781-109">En outre, s’ils utilisent une version d’essai d’un produit, ils ne voient pas d’invite pour l’acheter.</span><span class="sxs-lookup"><span data-stu-id="2d781-109">Also, if they’re using a trial version of a product, they don’t see prompts to buy it.</span></span> <span data-ttu-id="2d781-110">Pour plus d’informations, voir [Gérer les achats en libre-service (administrateur).](../subscriptions/manage-self-service-purchases-admins.md)</span><span class="sxs-lookup"><span data-stu-id="2d781-110">To learn more, see [Manage self-service purchases (Admin)](../subscriptions/manage-self-service-purchases-admins.md).</span></span>

<span data-ttu-id="2d781-111">Pour voir et gérer les demandes de licence, l’administrateur utilise **l’onglet Demandes** dans la page **Licences.**</span><span class="sxs-lookup"><span data-stu-id="2d781-111">To see and manage license requests, admin uses the **Requests** tab on the **Licensing** page.</span></span> <span data-ttu-id="2d781-112">La liste affiche le nom du produit demandé, le nom de la personne qui demande une licence, la date demandée et l’état de la demande.</span><span class="sxs-lookup"><span data-stu-id="2d781-112">The list shows the name of the product that is requested, name of the person requesting a license, date requested, and status of the request.</span></span> <span data-ttu-id="2d781-113">Les administrateurs peuvent filtrer la liste pour afficher les demandes en attente ou terminées.</span><span class="sxs-lookup"><span data-stu-id="2d781-113">Admins can filter the list to show requests that are pending or completed.</span></span> <span data-ttu-id="2d781-114">Les demandes sont maintenues pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2d781-114">Requests are held for 30 days.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2d781-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2d781-115">Before you begin</span></span>

<span data-ttu-id="2d781-116">Vous devez être un administrateur global pour effectuer les tâches de cet article.</span><span class="sxs-lookup"><span data-stu-id="2d781-116">You must be a Global admin to perform the tasks in this article.</span></span> <span data-ttu-id="2d781-117">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2d781-117">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="use-your-own-request-process"></a><span data-ttu-id="2d781-118">Utiliser votre propre processus de demande</span><span class="sxs-lookup"><span data-stu-id="2d781-118">Use your own request process</span></span>

<span data-ttu-id="2d781-119">Si votre organisation possède son propre processus de demande, vous pouvez l’utiliser à la place.</span><span class="sxs-lookup"><span data-stu-id="2d781-119">If your organization has its own request process, you can use it instead.</span></span> <span data-ttu-id="2d781-120">Vous créez un message qui s’affiche pour les utilisateurs lorsqu’ils demandent une licence.</span><span class="sxs-lookup"><span data-stu-id="2d781-120">You create a message that is displayed to users when they request a license.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d781-121">Si vous utilisez votre propre processus de demande, aucune demande n’est affichée sous **l’onglet Demandes.** Les demandes existantes avant l’ajout de votre message continuent d’apparaître jusqu’à ce que vous les approuviez ou les refusez.</span><span class="sxs-lookup"><span data-stu-id="2d781-121">If you use your own request process, no requests are displayed on the **Requests** tab. Existing requests from before you added your message continue to appear until you approve or decline them.</span></span>

1. <span data-ttu-id="2d781-122">Dans le Centre d’administration, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation,</a> puis sélectionnez **l’onglet Demandes.**</span><span class="sxs-lookup"><span data-stu-id="2d781-122">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page, then select the **Requests** tab.</span></span>
2. <span data-ttu-id="2d781-123">Sélectionnez **Utiliser votre processus de demande existant à la place.**</span><span class="sxs-lookup"><span data-stu-id="2d781-123">Select **Use your existing request process instead**.</span></span>
3. <span data-ttu-id="2d781-124">Dans le volet droit, dans la zone **Message,** tapez le message que les utilisateurs doivent voir lorsqu’ils demandent une licence.</span><span class="sxs-lookup"><span data-stu-id="2d781-124">In the right pane, in the **Message** box, type the message you want users to see when they request a license.</span></span> <span data-ttu-id="2d781-125">Si vous souhaitez également inclure un lien vers la stratégie de votre organisation ou une autre documentation, entrez l’URL dans la zone de texte Lien vers la **documentation (facultatif).**</span><span class="sxs-lookup"><span data-stu-id="2d781-125">If you want to also include a link to your organizations policy or other documentation, enter the URL in the **Link to documentation (optional)** text box.</span></span>
4. <span data-ttu-id="2d781-126">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2d781-126">Select **Save**.</span></span>

<span data-ttu-id="2d781-127">Lorsque vous revenir à la liste **demandes,** vous voyez le message Que vous utilisez **votre propre processus** de demande de licence .</span><span class="sxs-lookup"><span data-stu-id="2d781-127">When you return to the **Requests** list, you see the message **You’re using your own license request process**.</span></span> <span data-ttu-id="2d781-128">Pour apporter des modifications au message envoyé aux utilisateurs, sélectionnez Utiliser votre processus **de demande existant à la place.**</span><span class="sxs-lookup"><span data-stu-id="2d781-128">To make changes to the message that is sent to users, select **Use your existing request process instead**.</span></span>

## <a name="stop-using-your-own-request-process"></a><span data-ttu-id="2d781-129">Arrêter d’utiliser votre propre processus de demande</span><span class="sxs-lookup"><span data-stu-id="2d781-129">Stop using your own request process</span></span>

1. <span data-ttu-id="2d781-130">Dans le Centre d’administration, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation,</a> puis sélectionnez **l’onglet Demandes.**</span><span class="sxs-lookup"><span data-stu-id="2d781-130">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page, then select the **Requests** tab.</span></span>
2. <span data-ttu-id="2d781-131">Sélectionnez **Utiliser votre processus de demande existant à la place.**</span><span class="sxs-lookup"><span data-stu-id="2d781-131">Select **Use your existing request process instead**.</span></span>
3. <span data-ttu-id="2d781-132">Dans le volet droit, cochez la case Utiliser le processus de demande de **mon** organisation.</span><span class="sxs-lookup"><span data-stu-id="2d781-132">In the right pane, clear the **Use my organization’s request process** check box.</span></span>
4. <span data-ttu-id="2d781-133">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2d781-133">Select **Save**.</span></span>

## <a name="approve-or-deny-a-license-request"></a><span data-ttu-id="2d781-134">Approuver ou refuser une demande de licence</span><span class="sxs-lookup"><span data-stu-id="2d781-134">Approve or deny a license request</span></span>

1. <span data-ttu-id="2d781-135">Dans le Centre d’administration, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation,</a> puis sélectionnez **l’onglet Demandes.**</span><span class="sxs-lookup"><span data-stu-id="2d781-135">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page, then select the **Requests** tab.</span></span>
2. <span data-ttu-id="2d781-136">Sélectionnez la ligne qui contient la demande à réviser.</span><span class="sxs-lookup"><span data-stu-id="2d781-136">Select the row that contains the request you want to review.</span></span> <span data-ttu-id="2d781-137">Le volet droit affiche des détails sur les utilisateurs qui souhaitent obtenir des licences pour le produit.</span><span class="sxs-lookup"><span data-stu-id="2d781-137">The right pane shows details about which users want licenses to the product.</span></span>
3. <span data-ttu-id="2d781-138">Pour refuser l’intégralité de la demande, sélectionnez **N’approuvez pas** et, dans la boîte de dialogue, sélectionnez Ne **pas approuver.**</span><span class="sxs-lookup"><span data-stu-id="2d781-138">To deny the entire request, select **Don’t approve**, and in the dialog box, select **Don’t approve**.</span></span>
4. <span data-ttu-id="2d781-139">Pour refuser la demande à certains utilisateurs, mais en approuver d’autres, sélectionnez le X par le nom des utilisateurs que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2d781-139">To deny some users for the request, but approve others, select the X by the name of the users that you want to remove.</span></span> <span data-ttu-id="2d781-140">Leurs noms sont déplacés sous **Ne pas affecter à ces utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="2d781-140">Their names are moved under **Do not assign to these users**.</span></span>
5. <span data-ttu-id="2d781-141">Si vous avez plusieurs produits, sous Sélectionner un **produit,** sélectionnez celui pour qui vous souhaitez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="2d781-141">If you have more than one product, under **Select a product**, select the one that you want to use to assign licenses for.</span></span>
6. <span data-ttu-id="2d781-142">Pour refuser l’accès des utilisateurs à certains services et applications, développez Activer ou désactiver les applications et **services,** puis cochez les cases de ceux que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="2d781-142">To deny users access to certain app and services, expand **Turn apps and services on or off**, then clear the check boxes for the ones you want to exclude.</span></span>
7. <span data-ttu-id="2d781-143">En bas du volet, tapez un message facultatif dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="2d781-143">At the bottom of the pane, type an optional message in the text box.</span></span>
8. <span data-ttu-id="2d781-144">Lorsque vous avez terminé, sélectionnez **Approuver.**</span><span class="sxs-lookup"><span data-stu-id="2d781-144">When you’re finished, select **Approve**.</span></span> <span data-ttu-id="2d781-145">Le volet droit affiche les détails de la demande.</span><span class="sxs-lookup"><span data-stu-id="2d781-145">The right pane shows the details of the request.</span></span>
9. <span data-ttu-id="2d781-146">Fermez le volet droit.</span><span class="sxs-lookup"><span data-stu-id="2d781-146">Close the right pane.</span></span>
    <span data-ttu-id="2d781-147">Les utilisateurs reçoivent un courrier électronique qui indique que leur demande a été approuvée ou refusée.</span><span class="sxs-lookup"><span data-stu-id="2d781-147">Users receive an email that says their request was approved or denied.</span></span>

## <a name="related-content"></a><span data-ttu-id="2d781-148">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="2d781-148">Related content</span></span>

<span data-ttu-id="2d781-149">[Attribuer des licences aux utilisateurs](../../admin/manage/assign-licenses-to-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2d781-149">[Assign licenses to users](../../admin/manage/assign-licenses-to-users.md) (article)</span></span>\
<span data-ttu-id="2d781-150">[Déplacer les utilisateurs vers un autre abonnement](../subscriptions/move-users-different-subscription.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2d781-150">[Move users to a different subscription](../subscriptions/move-users-different-subscription.md) (article)</span></span>\
<span data-ttu-id="2d781-151">[Acheter ou supprimer des licences d’abonnement](buy-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2d781-151">[Buy or remove subscription licenses](buy-licenses.md) (article)</span></span>
