---
title: Balises utilisateur dans Microsoft Defender pour Office 365
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
description: Les administrateurs peuvent apprendre à identifier des groupes d’utilisateurs spécifiques à l’aide de balises utilisateur dans Microsoft Defender pour Office 365 plan 2. Le filtrage des balises est disponible dans les alertes, les rapports et les analyses de Microsoft Defender pour Office 365 afin d’identifier rapidement les utilisateurs balisés.
ms.openlocfilehash: 136de95addae7dcd48de2c6ac1f30ce67714817c
ms.sourcegitcommit: 38d828ae8d4350ae774a939c8decf30cb36c3bea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49552018"
---
# <a name="user-tags-in-microsoft-defender-for-office-365"></a><span data-ttu-id="68abf-104">Balises utilisateur dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="68abf-104">User tags in Microsoft Defender for Office 365</span></span>

> [!NOTE]
> <span data-ttu-id="68abf-105">La fonctionnalité de balises utilisateur est en mode aperçu, n’est pas accessible à tous et peut faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="68abf-105">The user tags feature is in Preview, isn't available to everyone, and is subject to change.</span></span> <span data-ttu-id="68abf-106">Pour plus d’informations sur le calendrier des publications, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="68abf-106">For information about the release schedule, check out the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

<span data-ttu-id="68abf-107">Les balises utilisateur sont des identificateurs pour des groupes d’utilisateurs spécifiques dans [Microsoft Defender pour Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="68abf-107">User tags are identifiers for specific groups of users in [Microsoft Defender for Office 365](office-365-atp.md).</span></span> <span data-ttu-id="68abf-108">Il existe deux types de balises utilisateur :</span><span class="sxs-lookup"><span data-stu-id="68abf-108">There are two types of user tags:</span></span>

- <span data-ttu-id="68abf-109">**Balises système**: actuellement, le [compte de priorité](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts) est le seul type de balise système.</span><span class="sxs-lookup"><span data-stu-id="68abf-109">**System tags**: Currently, [Priority accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts) is the only type of system tag.</span></span>
- <span data-ttu-id="68abf-110">**Balises personnalisées**: créez ces balises utilisateur vous-même.</span><span class="sxs-lookup"><span data-stu-id="68abf-110">**Custom tags**: You create these user tags yourself.</span></span>

<span data-ttu-id="68abf-111">Si votre organisation a Defender pour Office 365 plan 2 (inclus dans votre abonnement ou en tant que module complémentaire), vous pouvez créer des balises utilisateur personnalisées en plus de l’utilisation de la balise Accounts Priority.</span><span class="sxs-lookup"><span data-stu-id="68abf-111">If your organization has Defender for Office 365 Plan 2 (included in your subscription or as an add-on), you can create custom user tags in addition to using the priority accounts tag.</span></span>

<span data-ttu-id="68abf-112">Une fois que vous avez appliqué des balises système ou des balises personnalisées aux utilisateurs, vous pouvez utiliser ces balises comme filtres dans les alertes, les rapports et les analyses :</span><span class="sxs-lookup"><span data-stu-id="68abf-112">After you apply system tags or custom tags to users, you can use those tags as filters in alerts, reports, and investigations:</span></span>

- [<span data-ttu-id="68abf-113">Alertes dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="68abf-113">Alerts in the Security & Compliance Center</span></span>](alerts.md)
- [<span data-ttu-id="68abf-114">Explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="68abf-114">Threat Explorer and real-time detections</span></span>](threat-explorer.md)
- [<span data-ttu-id="68abf-115">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="68abf-115">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="68abf-116">Vues de campagne</span><span class="sxs-lookup"><span data-stu-id="68abf-116">Campaign Views</span></span>](campaigns.md)
- <span data-ttu-id="68abf-117">Pour les comptes prioritaires, vous pouvez utiliser le [rapport problèmes de messagerie pour les comptes prioritaires](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report) dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="68abf-117">For priority accounts, you can use the [Email issues for priority accounts report](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report) in the Exchange admin center (EAC).</span></span>

<span data-ttu-id="68abf-118">Cet article explique comment configurer les balises utilisateur dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="68abf-118">This article explains how to configure user tags in the Security & Compliance Center.</span></span> <span data-ttu-id="68abf-119">Il n’existe pas de cmdlets dans Security & Compliance Center pour gérer les balises utilisateur.</span><span class="sxs-lookup"><span data-stu-id="68abf-119">There are no cmdlets in Security & Compliance Center to manage user tags.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="68abf-120">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="68abf-120">What do you need to know before you begin?</span></span>

- <span data-ttu-id="68abf-121">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="68abf-121">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="68abf-122">Pour accéder directement à la page **balises utilisateur** , ouvrez <https://protection.office.com/userTags> .</span><span class="sxs-lookup"><span data-stu-id="68abf-122">To go directly to the **User tags** page, open <https://protection.office.com/userTags>.</span></span>

- <span data-ttu-id="68abf-123">Pour créer, modifier ou supprimer des **balises utilisateur personnalisées**, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="68abf-123">To create, modify, or remove **custom user tags**, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="68abf-124">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="68abf-124">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="68abf-125">Pour configurer des comptes de priorité (balises système), vous devez être un [administrateur général](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) ou un [administrateur Exchange](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#exchange-administrator).</span><span class="sxs-lookup"><span data-stu-id="68abf-125">To configure priority accounts (system tags), you need to be a [Global Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) or an [Exchange Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#exchange-administrator).</span></span>

  <span data-ttu-id="68abf-126">Vous pouvez également gérer et surveiller les comptes de priorité dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68abf-126">You can also manage and monitor priority accounts in the Microsoft 365 admin center.</span></span> <span data-ttu-id="68abf-127">Pour obtenir des instructions, consultez la rubrique [Manage and Monitor Priority Accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts).</span><span class="sxs-lookup"><span data-stu-id="68abf-127">For instructions, see [Manage and monitor priority accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts).</span></span>

## <a name="use-the-security-center-to-create-user-tags"></a><span data-ttu-id="68abf-128">Utiliser le centre de sécurité pour créer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="68abf-128">Use the Security Center to create user tags</span></span>

1. <span data-ttu-id="68abf-129">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="68abf-129">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="68abf-130">Sur la page **balises utilisateur** qui s’ouvre, cliquez sur **créer une balise**.</span><span class="sxs-lookup"><span data-stu-id="68abf-130">On the **User tags** page that opens, click **Create tag**.</span></span>

3. <span data-ttu-id="68abf-131">L’Assistant **créer une balise** s’ouvre en un nouveau. Dans la page **définir la balise** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="68abf-131">The **Create tag** wizard opens in a new fly out. On the **Define tag** page, configure the following settings:</span></span>
   - <span data-ttu-id="68abf-132">**Nom**: entrez un nom unique et descriptif pour la balise.</span><span class="sxs-lookup"><span data-stu-id="68abf-132">**Name**: Enter a unique, descriptive name for the tag.</span></span> <span data-ttu-id="68abf-133">Il s’agit de la valeur que vous allez voir et utiliser.</span><span class="sxs-lookup"><span data-stu-id="68abf-133">This is the value that you'll see and use.</span></span>
   - <span data-ttu-id="68abf-134">**Description**: entrez une description facultative pour la balise.</span><span class="sxs-lookup"><span data-stu-id="68abf-134">**Description**: Enter an optional description for the tag.</span></span>

   <span data-ttu-id="68abf-135">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="68abf-135">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="68abf-136">Dans la page **affecter des utilisateurs** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="68abf-136">On the **Assign users** page, do either of the following steps:</span></span>

   - <span data-ttu-id="68abf-137">Cliquez sur **Ajouter des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="68abf-137">Click **Add users**.</span></span> <span data-ttu-id="68abf-138">Dans le survol qui s’affiche, effectuez l’une des opérations suivantes pour ajouter des utilisateurs ou des groupes individuels :</span><span class="sxs-lookup"><span data-stu-id="68abf-138">In the fly out that appears, do any of the following steps to add individual users or groups:</span></span>
     - <span data-ttu-id="68abf-139">Cliquez dans la zone et faites défiler la liste pour sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="68abf-139">Click in the box and scroll through the list to select a user or group.</span></span>
     - <span data-ttu-id="68abf-140">Cliquez dans la zone et commencez à taper pour filtrer la liste, puis sélectionnez un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="68abf-140">Click in the box and start typing to filter the list and select a user or group.</span></span>
     - <span data-ttu-id="68abf-141">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="68abf-141">To add additional values, click in an empty area in the box.</span></span>
     - <span data-ttu-id="68abf-142">Pour supprimer des entrées individuelles de la zone, cliquez sur **supprimer** l' ![ icône supprimer de ](../../media/scc-remove-icon.png) l’utilisateur ou du groupe dans la zone.</span><span class="sxs-lookup"><span data-stu-id="68abf-142">To remove individual entries from the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user or group in the box.</span></span>
     - <span data-ttu-id="68abf-143">Pour supprimer les entrées existantes de la liste située en dessous du champ, cliquez sur **supprimer** ![ l’icône supprimer de l' ](../../media/scc-remove-icon.png) entrée.</span><span class="sxs-lookup"><span data-stu-id="68abf-143">To remove existing entries from the list below the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) the entry.</span></span>

     <span data-ttu-id="68abf-144">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="68abf-144">When you're finished, click **Add**.</span></span>

   - <span data-ttu-id="68abf-145">Cliquez sur **Importer** pour sélectionner un fichier texte qui contient les adresses de messagerie des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="68abf-145">Click **Import** to select a text file that contains the email addresses of the users or groups.</span></span> <span data-ttu-id="68abf-146">Assurez-vous que le fichier texte contient une entrée par ligne.</span><span class="sxs-lookup"><span data-stu-id="68abf-146">Be sure the text file contains one entry per line.</span></span>

   <span data-ttu-id="68abf-147">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="68abf-147">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="68abf-148">Dans la page **balise de révision** , vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="68abf-148">On the **Review tag** page, review your settings.</span></span> <span data-ttu-id="68abf-149">Vous pouvez cliquer sur **modifier** dans la section spécifique pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="68abf-149">You can click **Edit** in the specific section to make changes.</span></span>

   <span data-ttu-id="68abf-150">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="68abf-150">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-view-user-tags"></a><span data-ttu-id="68abf-151">Utiliser le centre de sécurité pour afficher les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="68abf-151">Use the Security Center to view user tags</span></span>

1. <span data-ttu-id="68abf-152">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="68abf-152">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="68abf-153">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez afficher (ne cliquez pas sur la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="68abf-153">On the **User tags** page that opens, select the user tag that you want to view (don't click on the checkbox).</span></span>

3. <span data-ttu-id="68abf-154">Dans le menu déroulant en lecture seule qui s’affiche, passez en revue les paramètres.</span><span class="sxs-lookup"><span data-stu-id="68abf-154">In the read-only details fly out that appears, review the settings.</span></span>

   <span data-ttu-id="68abf-155">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="68abf-155">When you're finished, click **Close**.</span></span>

## <a name="use-the-security-center-to-modify-user-tags"></a><span data-ttu-id="68abf-156">Utiliser le centre de sécurité pour modifier les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="68abf-156">Use the Security Center to modify user tags</span></span>

1. <span data-ttu-id="68abf-157">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="68abf-157">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="68abf-158">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez afficher, puis cliquez sur **modifier la balise**.</span><span class="sxs-lookup"><span data-stu-id="68abf-158">On the **User tags** page that opens, select the user tag that you want to view, and then click **Edit tag**.</span></span>

3. <span data-ttu-id="68abf-159">L’Assistant stratégie s’ouvre dans une **balise de modification** . Cliquez sur **suivant** pour passer en revue et modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="68abf-159">The policy wizard opens in an **Edit tag** fly out. Click **Next** to review and modify the settings.</span></span>

   <span data-ttu-id="68abf-160">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="68abf-160">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-remove-user-tags"></a><span data-ttu-id="68abf-161">Utiliser le centre de sécurité pour supprimer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="68abf-161">Use the Security Center to remove user tags</span></span>

<span data-ttu-id="68abf-162">**Remarque**: vous ne pouvez pas supprimer la balise de **compte de priorité** intégrée.</span><span class="sxs-lookup"><span data-stu-id="68abf-162">**Note**: You can't remove the built-in **Priority account** tag.</span></span>

1. <span data-ttu-id="68abf-163">Dans le centre de sécurité, accédez **Threat management** aux \> **balises utilisateur** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="68abf-163">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="68abf-164">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez supprimer, cliquez sur **Supprimer la balise**, puis sélectionnez **Oui, supprimer** dans l’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="68abf-164">On the **User tags** page that opens, select the user tag that you want to remove, click **Delete tag**, and then select **Yes, remove** in the warning that appears.</span></span>
