---
title: Balises utilisateur dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 04/21/2021
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à identifier des groupes spécifiques d’utilisateurs à l’aide de balises utilisateur dans Microsoft Defender Office 365 Plan 2. Le filtrage des balises est disponible pour les alertes, les rapports et les enquêtes dans Microsoft Defender Office 365 pour identifier rapidement les utilisateurs marqués.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 3ac53891e0eb106ab3681251cc4cb8c969b51f8a
ms.sourcegitcommit: cd55fe6abe25b1e4f5fbe8295d3a99aebd97ce66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53083115"
---
# <a name="user-tags-in-microsoft-defender-for-office-365"></a><span data-ttu-id="f1827-104">Balises utilisateur dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f1827-104">User tags in Microsoft Defender for Office 365</span></span>

> [!NOTE]
> <span data-ttu-id="f1827-105">La fonctionnalité de balises utilisateur est en prévisualisation, n’est pas disponible pour tout le monde et peut faire l’objet de changements.</span><span class="sxs-lookup"><span data-stu-id="f1827-105">The user tags feature is in Preview, isn't available to everyone, and is subject to change.</span></span> <span data-ttu-id="f1827-106">Pour plus d’informations sur la planification de publication, consultez la [feuille de Microsoft 365 de publication.](https://www.microsoft.com/microsoft-365/roadmap)</span><span class="sxs-lookup"><span data-stu-id="f1827-106">For information about the release schedule, check out the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

<span data-ttu-id="f1827-107">Les balises utilisateur sont des identificateurs pour des groupes spécifiques d’utilisateurs [dans Microsoft Defender Office 365](defender-for-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="f1827-107">User tags are identifiers for specific groups of users in [Microsoft Defender for Office 365](defender-for-office-365.md).</span></span> <span data-ttu-id="f1827-108">Il existe deux types de balises utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f1827-108">There are two types of user tags:</span></span>

- <span data-ttu-id="f1827-109">**Balises système**: actuellement, [les comptes de priorité](../../admin/setup/priority-accounts.md) sont le seul type de balise système.</span><span class="sxs-lookup"><span data-stu-id="f1827-109">**System tags**: Currently, [Priority accounts](../../admin/setup/priority-accounts.md) is the only type of system tag.</span></span>
- <span data-ttu-id="f1827-110">**Balises personnalisées**: vous créez ces balises utilisateur vous-même.</span><span class="sxs-lookup"><span data-stu-id="f1827-110">**Custom tags**: You create these user tags yourself.</span></span>

<span data-ttu-id="f1827-111">Si votre organisation dispose de Defender pour Office 365 Plan 2 (inclus dans votre abonnement ou en tant qu’complément), vous pouvez créer des balises utilisateur personnalisées en plus de l’utilisation de la balise de comptes prioritaires.</span><span class="sxs-lookup"><span data-stu-id="f1827-111">If your organization has Defender for Office 365 Plan 2 (included in your subscription or as an add-on), you can create custom user tags in addition to using the priority accounts tag.</span></span>

> [!NOTE]
> <span data-ttu-id="f1827-112">Actuellement, vous pouvez uniquement appliquer des balises utilisateur aux utilisateurs de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="f1827-112">Currently, you can only apply user tags to mailbox users.</span></span>

<span data-ttu-id="f1827-113">Après avoir appliqué des balises système ou des balises personnalisées aux utilisateurs, vous pouvez les utiliser comme filtres dans les alertes, les rapports et les enquêtes :</span><span class="sxs-lookup"><span data-stu-id="f1827-113">After you apply system tags or custom tags to users, you can use those tags as filters in alerts, reports, and investigations:</span></span>

- [<span data-ttu-id="f1827-114">Alertes</span><span class="sxs-lookup"><span data-stu-id="f1827-114">Alerts</span></span>](alerts.md)
- [<span data-ttu-id="f1827-115">Stratégies d’alerte personnalisées</span><span class="sxs-lookup"><span data-stu-id="f1827-115">Custom alert policies</span></span>](../../compliance/alert-policies.md#viewing-alerts)
- [<span data-ttu-id="f1827-116">Détections en temps réel et de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="f1827-116">Threat Explorer and real-time detections</span></span>](threat-explorer.md)
- [<span data-ttu-id="f1827-117">Page de l’entité d’e-mail</span><span class="sxs-lookup"><span data-stu-id="f1827-117">Email entity page</span></span>](mdo-email-entity-page.md#other-innovations)
- [<span data-ttu-id="f1827-118">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f1827-118">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="f1827-119">Vues de campagne</span><span class="sxs-lookup"><span data-stu-id="f1827-119">Campaign Views</span></span>](campaigns.md)
- <span data-ttu-id="f1827-120">Pour les comptes prioritaires, [](/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report) vous pouvez utiliser le rapport Problèmes de messagerie pour les comptes prioritaires dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="f1827-120">For priority accounts, you can use the [Email issues for priority accounts report](/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report) in the Exchange admin center (EAC).</span></span>

<span data-ttu-id="f1827-121">Cet article explique comment configurer des balises utilisateur dans le portail Microsoft 365 Defender utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1827-121">This article explains how to configure user tags in the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="f1827-122">Il n’existe aucune cmdlet dans Microsoft 365 Defender portail pour gérer les balises utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1827-122">There are no cmdlets in Microsoft 365 Defender portal to manage user tags.</span></span>

<span data-ttu-id="f1827-123">Pour voir comment les balises utilisateur font partie de la stratégie visant à protéger les comptes d’utilisateur à fort impact, consultez [recommandations](security-recommendations-for-priority-accounts.md)en matière de sécurité pour les comptes prioritaires dans Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="f1827-123">To see how user tags are part of the strategy to help protect high-impact user accounts, see [Security recommendations for priority accounts in Microsoft 365](security-recommendations-for-priority-accounts.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f1827-124">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f1827-124">What do you need to know before you begin?</span></span>

- <span data-ttu-id="f1827-125">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="f1827-125">You open the Microsoft 365 Defender portal at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="f1827-126">Pour aller directement à la page **des balises utilisateur,** ouvrez <https://security.microsoft.com/securitysettings/userTags> .</span><span class="sxs-lookup"><span data-stu-id="f1827-126">To go directly to the **User tags** page, open <https://security.microsoft.com/securitysettings/userTags>.</span></span>

- <span data-ttu-id="f1827-127">Des autorisations doivent vous être attribuées dans le portail Microsoft 365 Defender avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="f1827-127">You need to be assigned permissions in the Microsoft 365 Defender portal before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="f1827-128">Pour créer, modifier et supprimer des balises utilisateur,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur de** la sécurité.</span><span class="sxs-lookup"><span data-stu-id="f1827-128">To create, modify, and delete user tags, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="f1827-129">Pour ajouter et supprimer des membres de balises utilisateur existantes, vous devez  être membre des groupes de rôles Gestion de l’organisation, Administrateur de la sécurité ou Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f1827-129">To add and remove members from existing user tags, you need to be a member of the **Organization Management**, **Security Administrator**, or **Security Operator** role groups</span></span>
  - <span data-ttu-id="f1827-130">Pour accéder en lecture seule aux balises utilisateur,  vous devez être membre des groupes de rôles Lecteur global ou **Lecteur** de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f1827-130">For read-only access to user tags, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="f1827-131">Pour plus d’informations, consultez [Autorisations dans le portail Microsoft 365 Defender](permissions-microsoft-365-security-center.md).</span><span class="sxs-lookup"><span data-stu-id="f1827-131">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="f1827-132">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365. </span><span class="sxs-lookup"><span data-stu-id="f1827-132">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="f1827-133">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f1827-133">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="f1827-134">La gestion des balises utilisateur est contrôlée par les **rôles Lecteur de balises** et **Gestionnaire de balises.**</span><span class="sxs-lookup"><span data-stu-id="f1827-134">User tag management is controlled by the **Tag Reader** and **Tag Manager** roles.</span></span>

- <span data-ttu-id="f1827-135">Vous pouvez également gérer et surveiller les comptes prioritaires dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f1827-135">You can also manage and monitor priority accounts in the Microsoft 365 admin center.</span></span> <span data-ttu-id="f1827-136">Pour obtenir des instructions, voir [Gérer et surveiller les comptes prioritaires.](../../admin/setup/priority-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="f1827-136">For instructions, see [Manage and monitor priority accounts](../../admin/setup/priority-accounts.md).</span></span>

- <span data-ttu-id="f1827-137">Pour plus d’informations _sur la sécurisation des_ comptes privilégiés (comptes d’administrateur), consultez cette [rubrique.](/azure/architecture/framework/security/critical-impact-accounts)</span><span class="sxs-lookup"><span data-stu-id="f1827-137">For information about securing _privileged accounts_ (admin accounts), see [this topic](/azure/architecture/framework/security/critical-impact-accounts).</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-user-tags"></a><span data-ttu-id="f1827-138">Utiliser le portail Microsoft 365 Defender pour créer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="f1827-138">Use the Microsoft 365 Defender portal to create user tags</span></span>

1. <span data-ttu-id="f1827-139">Dans le portail Microsoft 365 Defender, go to **Paramètres** \> **Email & collaboration** User \> **tags**.</span><span class="sxs-lookup"><span data-stu-id="f1827-139">In the Microsoft 365 Defender portal, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="f1827-140">Dans la page **Balises utilisateur,** cliquez ![ sur Créer une balise icône Créer une ](../../media/m365-cc-sc-create-icon.png) **balise.**</span><span class="sxs-lookup"><span data-stu-id="f1827-140">On the **User tags** page, click ![Create tag icon](../../media/m365-cc-sc-create-icon.png) **Create tag**.</span></span>

3. <span data-ttu-id="f1827-141">**L’Assistant Créer** une balise s’ouvre dans un nouveau volant.</span><span class="sxs-lookup"><span data-stu-id="f1827-141">The **Create tag** wizard opens in a new flyout.</span></span> <span data-ttu-id="f1827-142">Dans la page **Définir la balise,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1827-142">On the **Define tag** page, configure the following settings:</span></span>
   - <span data-ttu-id="f1827-143">**Nom**: entrez un nom unique et descriptif pour la balise.</span><span class="sxs-lookup"><span data-stu-id="f1827-143">**Name**: Enter a unique, descriptive name for the tag.</span></span> <span data-ttu-id="f1827-144">Il s’agit de la valeur que vous verrez et utiliserez.</span><span class="sxs-lookup"><span data-stu-id="f1827-144">This is the value that you'll see and use.</span></span> <span data-ttu-id="f1827-145">Notez que vous ne pouvez pas renommer une balise après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="f1827-145">Note that you can't rename a tag after you create it.</span></span>
   - <span data-ttu-id="f1827-146">**Description**: entrez une description facultative de la balise.</span><span class="sxs-lookup"><span data-stu-id="f1827-146">**Description**: Enter an optional description for the tag.</span></span>

   <span data-ttu-id="f1827-147">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f1827-147">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="f1827-148">Dans la page **Affecter des membres,** faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f1827-148">On the **Assign members** page, do either of the following steps:</span></span>
   - <span data-ttu-id="f1827-149">Cliquez sur ![ Ajouter des membres icône Ajouter des ](../../media/m365-cc-sc-create-icon.png) **membres.**</span><span class="sxs-lookup"><span data-stu-id="f1827-149">Click ![Add members icon](../../media/m365-cc-sc-create-icon.png) **Add members**.</span></span> <span data-ttu-id="f1827-150">Dans le volant qui s’affiche, faites l’une des étapes suivantes pour ajouter des utilisateurs individuels ou des groupes :</span><span class="sxs-lookup"><span data-stu-id="f1827-150">In the fly out that appears, do any of the following steps to add individual users or groups:</span></span>
     - <span data-ttu-id="f1827-151">Cliquez dans la zone et faites défiler la liste pour sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="f1827-151">Click in the box and scroll through the list to select a user or group.</span></span>
     - <span data-ttu-id="f1827-152">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="f1827-152">Click in the box and start typing to filter the list and select a user or group.</span></span>
     - <span data-ttu-id="f1827-153">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="f1827-153">To add additional values, click in an empty area in the box.</span></span>
     - <span data-ttu-id="f1827-154">Pour supprimer des entrées individuelles, cliquez sur</span><span class="sxs-lookup"><span data-stu-id="f1827-154">To remove individual entries, click</span></span> ![Icône Supprimer l’entrée](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="f1827-156">à côté de l’entrée dans la zone.</span><span class="sxs-lookup"><span data-stu-id="f1827-156">next to the entry in the box.</span></span>
     - <span data-ttu-id="f1827-157">Pour supprimer toutes les entrées, cliquez sur Icône Supprimer l’entrée dans l’élément Utilisateurs nn et groupes nn sélectionnés ![ ](../../media/m365-cc-sc-remove-selection-icon.png) sous la zone. </span><span class="sxs-lookup"><span data-stu-id="f1827-157">To remove all entries, click ![Remove entry icon](../../media/m365-cc-sc-remove-selection-icon.png) on the **Selected nn users and nn groups** item below the box.</span></span>

     <span data-ttu-id="f1827-158">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f1827-158">When you're finished, click **Add**.</span></span>

     <span data-ttu-id="f1827-159">De retour sur la page **Affecter** des membres, vous pouvez également supprimer des entrées en cliquant sur l’icône ![ Supprimer en côté de ](../../media/m365-cc-sc-delete-icon.png) l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f1827-159">Back on the **Assign members** page, you can also remove entries by clicking ![Delete icon](../../media/m365-cc-sc-delete-icon.png) next to the entry.</span></span>

   - <span data-ttu-id="f1827-160">Cliquez **sur Importer** pour sélectionner un fichier texte qui contient les adresses de messagerie des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="f1827-160">Click **Import** to select a text file that contains the email addresses of the users or groups.</span></span> <span data-ttu-id="f1827-161">Assurez-vous que le fichier texte contient une entrée par ligne.</span><span class="sxs-lookup"><span data-stu-id="f1827-161">Be sure the text file contains one entry per line.</span></span>

   <span data-ttu-id="f1827-162">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f1827-162">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="f1827-163">Dans la page **de balise Révision** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="f1827-163">On the **Review tag** page that appears, review your settings.</span></span> <span data-ttu-id="f1827-164">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="f1827-164">You can select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="f1827-165">Vous pouvez également cliquer sur **Précédent** ou sélectionner la page spécifique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="f1827-165">Or you can click **Back** or select the specific page in the wizard.</span></span>

   <span data-ttu-id="f1827-166">Lorsque vous avez terminé, cliquez sur **Envoyer,** puis sur **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="f1827-166">When you're finished, click **Submit**, and then click **Done**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-user-tags"></a><span data-ttu-id="f1827-167">Utiliser le portail Microsoft 365 Defender pour afficher les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="f1827-167">Use the Microsoft 365 Defender portal to view user tags</span></span>

1. <span data-ttu-id="f1827-168">Dans le portail Microsoft 365 Defender, go to **Paramètres** \> **Email & collaboration** User \> **tags**.</span><span class="sxs-lookup"><span data-stu-id="f1827-168">In the Microsoft 365 Defender portal, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="f1827-169">Dans la page **Balises utilisateur,** les propriétés suivantes sont affichées dans la liste des balises utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f1827-169">On the **User tags** page, the following properties are displayed in the list of user tags:</span></span>

   - <span data-ttu-id="f1827-170">**Balise**: nom de la balise utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1827-170">**Tag**: The name of the user tag.</span></span> <span data-ttu-id="f1827-171">Notez que cela inclut la balise système **de** compte Priorité intégrée.</span><span class="sxs-lookup"><span data-stu-id="f1827-171">Note that this includes the built-in **Priority account** system tag.</span></span>
   - <span data-ttu-id="f1827-172">**Appliqué à**: nombre de membres</span><span class="sxs-lookup"><span data-stu-id="f1827-172">**Applied to**: The number of members</span></span>
   - <span data-ttu-id="f1827-173">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="f1827-173">**Last modified**</span></span>
   - <span data-ttu-id="f1827-174">**Créé le**</span><span class="sxs-lookup"><span data-stu-id="f1827-174">**Created on**</span></span>

3. <span data-ttu-id="f1827-175">Lorsque vous sélectionnez une balise utilisateur en cliquant sur le nom, les détails sont affichés dans un volant.</span><span class="sxs-lookup"><span data-stu-id="f1827-175">When you select a user tag by clicking on the name, the details are displayed in a flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-user-tags"></a><span data-ttu-id="f1827-176">Utiliser le portail Microsoft 365 Defender pour modifier les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="f1827-176">Use the Microsoft 365 Defender portal to modify user tags</span></span>

1. <span data-ttu-id="f1827-177">Dans le portail Microsoft 365 Defender, go to **Paramètres** \> **Email & collaboration** User \> **tags**.</span><span class="sxs-lookup"><span data-stu-id="f1827-177">In the Microsoft 365 Defender portal, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="f1827-178">Dans la page **Balises utilisateur,** sélectionnez la balise utilisateur dans la liste, puis cliquez sur Modifier la balise modifier l’icône ![ de balise ](../../media/m365-cc-sc-edit-icon.png) **.**</span><span class="sxs-lookup"><span data-stu-id="f1827-178">On the **User tags** page, select the user tag from the list, and then click ![Edit tag icon](../../media/m365-cc-sc-edit-icon.png) **Edit tag**.</span></span>

3. <span data-ttu-id="f1827-179">Dans le volet d’informations qui s’affiche, le même Assistant et les mêmes paramètres sont disponibles comme décrit dans la section Utiliser le portail [Microsoft 365 Defender](#use-the-microsoft-365-defender-portal-to-create-user-tags) pour créer des balises utilisateur plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f1827-179">In the details flyout that appears, the same wizard and settings are available as described in the [Use the Microsoft 365 Defender portal to create user tags](#use-the-microsoft-365-defender-portal-to-create-user-tags) section earlier in this article.</span></span>

   <span data-ttu-id="f1827-180">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="f1827-180">**Notes**:</span></span>

   - <span data-ttu-id="f1827-181">La **page Définir la** balise n’est pas disponible pour la balise système de compte priorité intégrée, vous ne pouvez donc pas renommer cette balise ou modifier la description. </span><span class="sxs-lookup"><span data-stu-id="f1827-181">The **Define tag** page is not available for the built-in **Priority account** system tag, so you can't rename this tag or change the description.</span></span>
   - <span data-ttu-id="f1827-182">Vous ne pouvez pas renommer une balise personnalisée, mais vous pouvez modifier la description.</span><span class="sxs-lookup"><span data-stu-id="f1827-182">You can't rename a custom tag, but you can change the description.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-user-tags"></a><span data-ttu-id="f1827-183">Utiliser le portail Microsoft 365 Defender pour supprimer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="f1827-183">Use the Microsoft 365 Defender portal to remove user tags</span></span>

> [!NOTE]
> <span data-ttu-id="f1827-184">Vous ne pouvez pas supprimer la balise système de compte **Priorité** intégrée.</span><span class="sxs-lookup"><span data-stu-id="f1827-184">You can't remove the built-in **Priority account** system tag.</span></span>

1. <span data-ttu-id="f1827-185">Dans le portail Microsoft 365 Defender, go to **Paramètres** \> **Email & collaboration** User \> **tags**.</span><span class="sxs-lookup"><span data-stu-id="f1827-185">In the Microsoft 365 Defender portal, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="f1827-186">Dans la page **Balises utilisateur,** sélectionnez la balise utilisateur dans la liste, puis cliquez sur Supprimer la balise Supprimer l’icône ![ de ](../../media/m365-cc-sc-delete-icon.png) **balise**.</span><span class="sxs-lookup"><span data-stu-id="f1827-186">On the **User tags** page, select the user tag from the list, and then click ![Delete tag icon](../../media/m365-cc-sc-delete-icon.png) **Delete tag**.</span></span>

3. <span data-ttu-id="f1827-187">Lisez l’avertissement dans la boîte de dialogue de confirmation qui s’affiche, puis cliquez sur **Oui, supprimer.**</span><span class="sxs-lookup"><span data-stu-id="f1827-187">Read the warning in the confirmation dialog that appears, and then click **Yes, remove**.</span></span>
