---
title: Balises utilisateur dans Office 365 – Protection avancée contre les menaces
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à identifier des groupes d’utilisateurs spécifiques à l’aide de balises utilisateur dans Office 365 DAV (plan 2). Le filtrage des balises est disponible dans les alertes, les rapports et les enquêtes dans la protection avancée contre les menaces d’Office 365 pour identifier rapidement les utilisateurs balisés.
ms.openlocfilehash: 16e756b95e16e40f4df738e825e842681c67e22c
ms.sourcegitcommit: cd17328baa58448214487e3e68c37590ab9fd08d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48399384"
---
# <a name="user-tags-in-office-365-atp"></a><span data-ttu-id="10a31-104">Balises utilisateur dans Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="10a31-104">User tags in Office 365 ATP</span></span>

<span data-ttu-id="10a31-105">Les balises utilisateur sont des identificateurs pour des groupes d’utilisateurs spécifiques dans [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="10a31-105">User tags are identifiers for specific groups of users in [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md).</span></span> <span data-ttu-id="10a31-106">Il existe deux types de balises utilisateur :</span><span class="sxs-lookup"><span data-stu-id="10a31-106">There are two types of user tags:</span></span>

- <span data-ttu-id="10a31-107">**Balises système**: actuellement, le [compte de priorité](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts) est le seul type de balise système.</span><span class="sxs-lookup"><span data-stu-id="10a31-107">**System tags**: Currently, [Priority accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts) is the only type of system tag.</span></span>
- <span data-ttu-id="10a31-108">**Balises personnalisées**: créez ces balises utilisateur vous-même.</span><span class="sxs-lookup"><span data-stu-id="10a31-108">**Custom tags**: You create these user tags yourself.</span></span>

<span data-ttu-id="10a31-109">Si votre organisation dispose d’Office 365 DAV plan 2 (inclus dans votre abonnement ou en tant que module complémentaire), vous pouvez créer des balises utilisateur personnalisées en plus de l’utilisation de la balise Accounts Priority.</span><span class="sxs-lookup"><span data-stu-id="10a31-109">If your organization has Office 365 ATP Plan 2 (included in your subscription or as an add-on), you can create custom user tags in addition to using the priority accounts tag.</span></span>

<span data-ttu-id="10a31-110">Une fois que vous avez appliqué des balises système ou des balises personnalisées aux utilisateurs, vous pouvez utiliser ces balises comme filtres dans les alertes, les rapports et les analyses :</span><span class="sxs-lookup"><span data-stu-id="10a31-110">After you apply system tags or custom tags to users, you can use those tags as filters in alerts, reports, and investigations:</span></span>

- [<span data-ttu-id="10a31-111">Alertes dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="10a31-111">Alerts in the Security & Compliance Center</span></span>](alerts.md)
- [<span data-ttu-id="10a31-112">Explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="10a31-112">Threat Explorer and real-time detections</span></span>](threat-explorer.md)
- [<span data-ttu-id="10a31-113">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="10a31-113">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="10a31-114">Vues de campagne</span><span class="sxs-lookup"><span data-stu-id="10a31-114">Campaign Views</span></span>](campaigns.md)

<span data-ttu-id="10a31-115">Cet article explique comment configurer les balises utilisateur dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="10a31-115">This article explains how to configure user tags in the Security & Compliance Center.</span></span> <span data-ttu-id="10a31-116">Il n’existe pas de cmdlets dans Security & Compliance Center pour gérer les balises utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10a31-116">There are no cmdlets in Security & Compliance Center to manage user tags.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="10a31-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="10a31-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="10a31-118">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="10a31-118">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="10a31-119">Pour accéder directement à la page **balises utilisateur** , ouvrez <https://protection.office.com/userTags> .</span><span class="sxs-lookup"><span data-stu-id="10a31-119">To go directly to the **User tags** page, open <https://protection.office.com/userTags>.</span></span>

- <span data-ttu-id="10a31-120">Pour créer, modifier ou supprimer des **balises utilisateur personnalisées**, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="10a31-120">To create, modify, or remove **custom user tags**, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="10a31-121">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="10a31-121">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="10a31-122">Pour configurer des comptes de priorité (balises système), vous devez être un [administrateur général](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) ou un [administrateur Exchange](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#exchange-administrator).</span><span class="sxs-lookup"><span data-stu-id="10a31-122">To configure priority accounts (system tags), you need to be a [Global Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) or an [Exchange Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#exchange-administrator).</span></span>

  <span data-ttu-id="10a31-123">Vous pouvez également gérer et surveiller les comptes de priorité dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="10a31-123">You can also manage and monitor priority accounts in the Microsoft 365 admin center.</span></span> <span data-ttu-id="10a31-124">Pour obtenir des instructions, consultez la rubrique [Manage and Monitor Priority Accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts).</span><span class="sxs-lookup"><span data-stu-id="10a31-124">For instructions, see [Manage and monitor priority accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts).</span></span>

## <a name="use-the-security-center-to-create-user-tags"></a><span data-ttu-id="10a31-125">Utiliser le centre de sécurité pour créer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="10a31-125">Use the Security Center to create user tags</span></span>

1. <span data-ttu-id="10a31-126">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="10a31-126">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="10a31-127">Sur la page **balises utilisateur** qui s’ouvre, cliquez sur **créer une balise**.</span><span class="sxs-lookup"><span data-stu-id="10a31-127">On the **User tags** page that opens, click **Create tag**.</span></span>

3. <span data-ttu-id="10a31-128">L’Assistant **créer une balise** s’ouvre en un nouveau. Dans la page **définir la balise** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="10a31-128">The **Create tag** wizard opens in a new fly out. On the **Define tag** page, configure the following settings:</span></span>

   - <span data-ttu-id="10a31-129">**Nom**: entrez un nom unique et descriptif pour la balise.</span><span class="sxs-lookup"><span data-stu-id="10a31-129">**Name**: Enter a unique, descriptive name for the tag.</span></span> <span data-ttu-id="10a31-130">Il s’agit de la valeur que vous allez voir et utiliser.</span><span class="sxs-lookup"><span data-stu-id="10a31-130">This is the value that you'll see and use.</span></span>

   - <span data-ttu-id="10a31-131">**Description**: entrez une description facultative pour la balise.</span><span class="sxs-lookup"><span data-stu-id="10a31-131">**Description**: Enter an optional description for the tag.</span></span>

   <span data-ttu-id="10a31-132">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="10a31-132">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="10a31-133">Dans la page **affecter des boîtes aux lettres** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="10a31-133">On the **Assign mailboxes** page, do either of the following steps:</span></span>

   - <span data-ttu-id="10a31-134">Cliquez sur **Ajouter des boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="10a31-134">Click **Add mailboxes**.</span></span> <span data-ttu-id="10a31-135">Dans le survol qui s’affiche, effectuez l’une des opérations suivantes pour ajouter des utilisateurs ou des groupes individuels :</span><span class="sxs-lookup"><span data-stu-id="10a31-135">In the fly out that appears, do any of the following steps to add individual users or groups:</span></span>

     - <span data-ttu-id="10a31-136">Cliquez dans la zone et faites défiler la liste pour sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="10a31-136">Click in the box and scroll through the list to select a user or group.</span></span>
     - <span data-ttu-id="10a31-137">Cliquez dans la zone et commencez à taper pour filtrer la liste, puis sélectionnez un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="10a31-137">Click in the box and start typing to filter the list and select a user or group.</span></span>
     - <span data-ttu-id="10a31-138">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="10a31-138">To add additional values, click in an empty area in the box.</span></span>
     - <span data-ttu-id="10a31-139">Pour supprimer des entrées individuelles de la zone, cliquez sur **supprimer** l' ![ icône supprimer de ](../../media/scc-remove-icon.png) l’utilisateur ou du groupe dans la zone.</span><span class="sxs-lookup"><span data-stu-id="10a31-139">To remove individual entries from the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user or group in the box.</span></span>
     - <span data-ttu-id="10a31-140">Pour supprimer les entrées existantes de la liste située en dessous du champ, cliquez sur **supprimer** ![ l’icône supprimer de l' ](../../media/scc-remove-icon.png) entrée.</span><span class="sxs-lookup"><span data-stu-id="10a31-140">To remove existing entries from the list below the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) the entry.</span></span>

     <span data-ttu-id="10a31-141">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="10a31-141">When you're finished, click **Add**.</span></span>

   - <span data-ttu-id="10a31-142">Cliquez sur **Importer** pour sélectionner un fichier texte qui contient les adresses de messagerie des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="10a31-142">Click **Import** to select a text file that contains the email addresses of the users or groups.</span></span> <span data-ttu-id="10a31-143">Assurez-vous que le fichier texte contient une entrée par ligne.</span><span class="sxs-lookup"><span data-stu-id="10a31-143">Be sure the text file contains one entry per line.</span></span>

   <span data-ttu-id="10a31-144">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="10a31-144">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="10a31-145">Dans la page **balise de révision** , vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="10a31-145">On the **Review tag** page, review your settings.</span></span> <span data-ttu-id="10a31-146">Vous pouvez cliquer sur **modifier** dans la section spécifique pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="10a31-146">You can click **Edit** in the specific section to make changes.</span></span>

   <span data-ttu-id="10a31-147">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="10a31-147">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-view-user-tags"></a><span data-ttu-id="10a31-148">Utiliser le centre de sécurité pour afficher les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="10a31-148">Use the Security Center to view user tags</span></span>

1. <span data-ttu-id="10a31-149">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="10a31-149">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="10a31-150">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez afficher (ne cliquez pas sur la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="10a31-150">On the **User tags** page that opens, select the user tag that you want to view (don't click on the checkbox).</span></span>

3. <span data-ttu-id="10a31-151">Dans le menu déroulant en lecture seule qui s’affiche, passez en revue les paramètres.</span><span class="sxs-lookup"><span data-stu-id="10a31-151">In the read-only details fly out that appears, review the settings.</span></span>

   <span data-ttu-id="10a31-152">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="10a31-152">When you're finished, click **Close**.</span></span>

## <a name="use-the-security-center-to-modify-user-tags"></a><span data-ttu-id="10a31-153">Utiliser le centre de sécurité pour modifier les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="10a31-153">Use the Security Center to modify user tags</span></span>

1. <span data-ttu-id="10a31-154">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="10a31-154">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="10a31-155">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez afficher, puis cliquez sur **modifier la balise**.</span><span class="sxs-lookup"><span data-stu-id="10a31-155">On the **User tags** page that opens, select the user tag that you want to view, and then click **Edit tag**.</span></span>

3. <span data-ttu-id="10a31-156">L’Assistant stratégie s’ouvre dans une **balise de modification** . Cliquez sur **suivant** pour passer en revue et modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="10a31-156">The policy wizard opens in an **Edit tag** fly out. Click **Next** to review and modify the settings.</span></span>

   <span data-ttu-id="10a31-157">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="10a31-157">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-remove-user-tags"></a><span data-ttu-id="10a31-158">Utiliser le centre de sécurité pour supprimer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="10a31-158">Use the Security Center to remove user tags</span></span>

<span data-ttu-id="10a31-159">**Remarque**: vous ne pouvez pas supprimer la balise de **compte de priorité** intégrée.</span><span class="sxs-lookup"><span data-stu-id="10a31-159">**Note**: You can't remove the built-in **Priority account** tag.</span></span>

1. <span data-ttu-id="10a31-160">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="10a31-160">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="10a31-161">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez supprimer, cliquez sur **Supprimer la balise**, puis sélectionnez **Oui, supprimer** dans l’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="10a31-161">On the **User tags** page that opens, select the user tag that you want to remove, click **Delete tag**, and then select **Yes, remove** in the warning that appears.</span></span>
