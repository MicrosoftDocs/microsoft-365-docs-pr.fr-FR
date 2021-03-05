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
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à identifier des groupes spécifiques d’utilisateurs à l’aide de balises utilisateur dans Microsoft Defender pour Office 365 Plan 2. Le filtrage des balises est disponible dans les alertes, les rapports et les enquêtes dans Microsoft Defender pour Office 365 pour identifier rapidement les utilisateurs marqués.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6e5ddffad6405f48a9af55b5123729eb256064a7
ms.sourcegitcommit: 375168ee66be862cf3b00f2733c7be02e63408cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50453644"
---
# <a name="user-tags-in-microsoft-defender-for-office-365"></a><span data-ttu-id="1cd69-104">Balises utilisateur dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1cd69-104">User tags in Microsoft Defender for Office 365</span></span>

> [!NOTE]
> <span data-ttu-id="1cd69-105">La fonctionnalité de balises utilisateur est en prévisualisation, n’est pas disponible pour tout le monde et peut faire l’objet de changements.</span><span class="sxs-lookup"><span data-stu-id="1cd69-105">The user tags feature is in Preview, isn't available to everyone, and is subject to change.</span></span> <span data-ttu-id="1cd69-106">Pour plus d’informations sur la planification de publication, consultez la feuille [de route Microsoft 365.](https://www.microsoft.com/microsoft-365/roadmap)</span><span class="sxs-lookup"><span data-stu-id="1cd69-106">For information about the release schedule, check out the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

<span data-ttu-id="1cd69-107">Les balises utilisateur sont des identificateurs pour des groupes spécifiques d’utilisateurs [dans Microsoft Defender pour Office 365.](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="1cd69-107">User tags are identifiers for specific groups of users in [Microsoft Defender for Office 365](office-365-atp.md).</span></span> <span data-ttu-id="1cd69-108">Il existe deux types de balises utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1cd69-108">There are two types of user tags:</span></span>

- <span data-ttu-id="1cd69-109">**Balises système**: actuellement, [les comptes de priorité](../../admin/setup/priority-accounts.md) sont le seul type de balise système.</span><span class="sxs-lookup"><span data-stu-id="1cd69-109">**System tags**: Currently, [Priority accounts](../../admin/setup/priority-accounts.md) is the only type of system tag.</span></span>
- <span data-ttu-id="1cd69-110">**Balises personnalisées**: vous créez ces balises utilisateur vous-même.</span><span class="sxs-lookup"><span data-stu-id="1cd69-110">**Custom tags**: You create these user tags yourself.</span></span>

<span data-ttu-id="1cd69-111">Si votre organisation dispose de Defender pour Office 365 Plan 2 (inclus dans votre abonnement ou en tant qu’complément), vous pouvez créer des balises utilisateur personnalisées en plus de l’utilisation de la balise de comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="1cd69-111">If your organization has Defender for Office 365 Plan 2 (included in your subscription or as an add-on), you can create custom user tags in addition to using the priority accounts tag.</span></span>

<span data-ttu-id="1cd69-112">Après avoir appliqué des balises système ou des balises personnalisées aux utilisateurs, vous pouvez les utiliser comme filtres dans les alertes, les rapports et les enquêtes :</span><span class="sxs-lookup"><span data-stu-id="1cd69-112">After you apply system tags or custom tags to users, you can use those tags as filters in alerts, reports, and investigations:</span></span>

- [<span data-ttu-id="1cd69-113">Alertes dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="1cd69-113">Alerts in the Security & Compliance Center</span></span>](alerts.md)
- [<span data-ttu-id="1cd69-114">Détections en temps réel et de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="1cd69-114">Threat Explorer and real-time detections</span></span>](threat-explorer.md)
- [<span data-ttu-id="1cd69-115">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="1cd69-115">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="1cd69-116">Vues de campagne</span><span class="sxs-lookup"><span data-stu-id="1cd69-116">Campaign Views</span></span>](campaigns.md)
- <span data-ttu-id="1cd69-117">Pour les comptes prioritaires, [](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report) vous pouvez utiliser le rapport Problèmes de messagerie pour les comptes prioritaires dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="1cd69-117">For priority accounts, you can use the [Email issues for priority accounts report](https://docs.microsoft.com/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report) in the Exchange admin center (EAC).</span></span>

<span data-ttu-id="1cd69-118">Cet article explique comment configurer des balises utilisateur dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="1cd69-118">This article explains how to configure user tags in the Security & Compliance Center.</span></span> <span data-ttu-id="1cd69-119">Il n’existe aucune cmdlet dans le Centre de sécurité & conformité pour gérer les balises utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1cd69-119">There are no cmdlets in Security & Compliance Center to manage user tags.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1cd69-120">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1cd69-120">What do you need to know before you begin?</span></span>

- <span data-ttu-id="1cd69-121">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="1cd69-121">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="1cd69-122">Pour aller directement à la page **des balises utilisateur,** ouvrez <https://protection.office.com/userTags> .</span><span class="sxs-lookup"><span data-stu-id="1cd69-122">To go directly to the **User tags** page, open <https://protection.office.com/userTags>.</span></span>

- <span data-ttu-id="1cd69-123">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="1cd69-123">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="1cd69-124">Pour créer, modifier et supprimer des balises utilisateur,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1cd69-124">To create, modify, and delete user tags, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="1cd69-125">Pour ajouter et supprimer des membres de balises utilisateur existantes, vous devez  être membre des groupes de rôles Gestion de l’organisation, Administrateur de la sécurité ou Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="1cd69-125">To add and remove members from existing user tags, you need to be a member of the **Organization Management**, **Security Administrator**, or **Security Operator** role groups</span></span>
  - <span data-ttu-id="1cd69-126">Pour accéder en lecture seule aux balises utilisateur,  vous devez être membre des groupes de rôles Lecteur global ou **Lecteur** de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1cd69-126">For read-only access to user tags, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="1cd69-127">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="1cd69-127">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="1cd69-128">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="1cd69-128">**Notes**:</span></span>

  - <span data-ttu-id="1cd69-129">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1cd69-129">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="1cd69-130">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1cd69-130">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="1cd69-131">La gestion des balises utilisateur est contrôlée par les **rôles Lecteur de balises** et **Gestionnaire de balises.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-131">User tag management is controlled by the **Tag Reader** and **Tag Manager** roles.</span></span>

- <span data-ttu-id="1cd69-132">Vous pouvez également gérer et surveiller les comptes prioritaires dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1cd69-132">You can also manage and monitor priority accounts in the Microsoft 365 admin center.</span></span> <span data-ttu-id="1cd69-133">Pour obtenir des instructions, voir [Gérer et surveiller les comptes prioritaires.](../../admin/setup/priority-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="1cd69-133">For instructions, see [Manage and monitor priority accounts](../../admin/setup/priority-accounts.md).</span></span>

## <a name="use-the-security-center-to-create-user-tags"></a><span data-ttu-id="1cd69-134">Utiliser le Centre de sécurité pour créer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="1cd69-134">Use the Security Center to create user tags</span></span>

1. <span data-ttu-id="1cd69-135">Dans le Centre de sécurité, allez aux **balises utilisateur de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-135">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="1cd69-136">Dans la page **Balises utilisateur** qui s’ouvre, cliquez **sur Créer une balise.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-136">On the **User tags** page that opens, click **Create tag**.</span></span>

3. <span data-ttu-id="1cd69-137">**L’Assistant Création** d’une balise s’ouvre dans un nouveau volant. Dans la page **Définir la balise,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1cd69-137">The **Create tag** wizard opens in a new fly out. On the **Define tag** page, configure the following settings:</span></span>
   - <span data-ttu-id="1cd69-138">**Nom**: entrez un nom unique et descriptif pour la balise.</span><span class="sxs-lookup"><span data-stu-id="1cd69-138">**Name**: Enter a unique, descriptive name for the tag.</span></span> <span data-ttu-id="1cd69-139">Il s’agit de la valeur que vous verrez et utiliserez.</span><span class="sxs-lookup"><span data-stu-id="1cd69-139">This is the value that you'll see and use.</span></span>
   - <span data-ttu-id="1cd69-140">**Description**: entrez une description facultative de la balise.</span><span class="sxs-lookup"><span data-stu-id="1cd69-140">**Description**: Enter an optional description for the tag.</span></span>

   <span data-ttu-id="1cd69-141">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1cd69-141">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="1cd69-142">Dans la page **Affecter des** utilisateurs, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1cd69-142">On the **Assign users** page, do either of the following steps:</span></span>

   - <span data-ttu-id="1cd69-143">Cliquez **sur Ajouter des utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-143">Click **Add users**.</span></span> <span data-ttu-id="1cd69-144">Dans le volant qui s’affiche, faites l’une des étapes suivantes pour ajouter des utilisateurs individuels ou des groupes :</span><span class="sxs-lookup"><span data-stu-id="1cd69-144">In the fly out that appears, do any of the following steps to add individual users or groups:</span></span>
     - <span data-ttu-id="1cd69-145">Cliquez dans la zone et faites défiler la liste pour sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="1cd69-145">Click in the box and scroll through the list to select a user or group.</span></span>
     - <span data-ttu-id="1cd69-146">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="1cd69-146">Click in the box and start typing to filter the list and select a user or group.</span></span>
     - <span data-ttu-id="1cd69-147">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="1cd69-147">To add additional values, click in an empty area in the box.</span></span>
     - <span data-ttu-id="1cd69-148">Pour supprimer des entrées individuelles de la zone, cliquez sur **Supprimer** l’icône sur l’utilisateur ou ![ le groupe dans la ](../../media/scc-remove-icon.png) zone.</span><span class="sxs-lookup"><span data-stu-id="1cd69-148">To remove individual entries from the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user or group in the box.</span></span>
     - <span data-ttu-id="1cd69-149">Pour supprimer des entrées existantes de la liste sous la zone, cliquez sur **Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) Supprimer l’entrée.</span><span class="sxs-lookup"><span data-stu-id="1cd69-149">To remove existing entries from the list below the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) the entry.</span></span>

     <span data-ttu-id="1cd69-150">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="1cd69-150">When you're finished, click **Add**.</span></span>

   - <span data-ttu-id="1cd69-151">Cliquez **sur Importer** pour sélectionner un fichier texte qui contient les adresses de messagerie des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="1cd69-151">Click **Import** to select a text file that contains the email addresses of the users or groups.</span></span> <span data-ttu-id="1cd69-152">Assurez-vous que le fichier texte contient une entrée par ligne.</span><span class="sxs-lookup"><span data-stu-id="1cd69-152">Be sure the text file contains one entry per line.</span></span>

   <span data-ttu-id="1cd69-153">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1cd69-153">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="1cd69-154">Dans la page **De révision,** examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="1cd69-154">On the **Review tag** page, review your settings.</span></span> <span data-ttu-id="1cd69-155">Vous pouvez cliquer **sur Modifier** dans la section spécifique pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="1cd69-155">You can click **Edit** in the specific section to make changes.</span></span>

   <span data-ttu-id="1cd69-156">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-156">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-view-user-tags"></a><span data-ttu-id="1cd69-157">Utiliser le Centre de sécurité pour afficher les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="1cd69-157">Use the Security Center to view user tags</span></span>

1. <span data-ttu-id="1cd69-158">Dans le Centre de sécurité, allez aux **balises utilisateur de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-158">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="1cd69-159">Dans la page **Balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur à afficher (ne cliquez pas sur la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="1cd69-159">On the **User tags** page that opens, select the user tag that you want to view (don't click on the checkbox).</span></span>

3. <span data-ttu-id="1cd69-160">Dans la liste des détails en lecture seule qui s’affiche, examinez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="1cd69-160">In the read-only details fly out that appears, review the settings.</span></span>

   <span data-ttu-id="1cd69-161">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="1cd69-161">When you're finished, click **Close**.</span></span>

## <a name="use-the-security-center-to-modify-user-tags"></a><span data-ttu-id="1cd69-162">Utiliser le Centre de sécurité pour modifier des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="1cd69-162">Use the Security Center to modify user tags</span></span>

1. <span data-ttu-id="1cd69-163">Dans le Centre de sécurité, allez aux **balises utilisateur de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-163">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="1cd69-164">Dans la page **Balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur à afficher, puis cliquez sur **Modifier la balise**.</span><span class="sxs-lookup"><span data-stu-id="1cd69-164">On the **User tags** page that opens, select the user tag that you want to view, and then click **Edit tag**.</span></span>

3. <span data-ttu-id="1cd69-165">L’Assistant Stratégie s’ouvre dans un **volant de balise Modifier.** Cliquez **sur Suivant** pour passer en revue et modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="1cd69-165">The policy wizard opens in an **Edit tag** fly out. Click **Next** to review and modify the settings.</span></span>

   <span data-ttu-id="1cd69-166">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-166">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-remove-user-tags"></a><span data-ttu-id="1cd69-167">Utiliser le Centre de sécurité pour supprimer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="1cd69-167">Use the Security Center to remove user tags</span></span>

<span data-ttu-id="1cd69-168">**Remarque**: vous ne pouvez pas supprimer la balise de compte **Priority** intégrée.</span><span class="sxs-lookup"><span data-stu-id="1cd69-168">**Note**: You can't remove the built-in **Priority account** tag.</span></span>

1. <span data-ttu-id="1cd69-169">Dans le Centre de sécurité, allez aux **balises utilisateur de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="1cd69-169">In the Security Center, go to **Threat management** \> **User tags**.</span></span>

2. <span data-ttu-id="1cd69-170">Dans **la** page Balises utilisateur qui s’ouvre, sélectionnez la balise utilisateur à supprimer, cliquez sur Supprimer la **balise,** puis sélectionnez **Oui,** supprimez l’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1cd69-170">On the **User tags** page that opens, select the user tag that you want to remove, click **Delete tag**, and then select **Yes, remove** in the warning that appears.</span></span>
