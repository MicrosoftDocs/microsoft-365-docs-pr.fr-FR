---
title: Balises utilisateur
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
description: Les administrateurs peuvent apprendre à identifier des groupes d’utilisateurs spécifiques à l’aide de balises utilisateur dans Oiffce 365 DAV plan 2. Le filtrage des balises est disponible dans les alertes, les rapports et les enquêtes dans la protection avancée contre les menaces d’Office 365 pour identifier rapidement les utilisateurs balisés.
ms.openlocfilehash: d47c5c00e3cf0362c44aebc18d11db4bba68a149
ms.sourcegitcommit: e5ac81132cc5fd248350627a3cc7b3c640f53b6e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48210025"
---
# <a name="user-tags-in-the-microsoft-security-center"></a><span data-ttu-id="ab4fa-104">Balises utilisateur dans le centre de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="ab4fa-104">User tags in the Microsoft Security Center</span></span>

<span data-ttu-id="ab4fa-105">Les balises utilisateur sont des identificateurs pour des groupes d’utilisateurs spécifiques dans [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="ab4fa-105">User tags are identifiers for specific groups of users in [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md).</span></span> <span data-ttu-id="ab4fa-106">Les [comptes de priorité](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts) sont un type de balise utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-106">[Priority accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts) are a type of user tag.</span></span> <span data-ttu-id="ab4fa-107">Si votre organisation dispose d’Office 365 DAV plan 2 (inclus dans votre abonnement ou en tant que module complémentaire), vous pouvez créer des balises utilisateur personnalisées en plus de l’utilisation de la balise Accounts Priority.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-107">If your organization has Office 365 ATP Plan 2 (included in your subscription or as an add-on), you can create custom user tags in addition to using the priority accounts tag.</span></span>

<span data-ttu-id="ab4fa-108">Une fois que vous avez appliqué des balises à des utilisateurs spécifiques, vous pouvez utiliser ces balises en tant que filtres dans les alertes, les rapports et les analyses :</span><span class="sxs-lookup"><span data-stu-id="ab4fa-108">After you apply tags to specific users, you can use those tags as filters in alerts, reports, and investigations:</span></span>

- [<span data-ttu-id="ab4fa-109">Alertes dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="ab4fa-109">Alerts in the Security & Compliance Center</span></span>](alerts.md)
- [<span data-ttu-id="ab4fa-110">Explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="ab4fa-110">Threat Explorer and real-time detections</span></span>](threat-explorer.md)
- [<span data-ttu-id="ab4fa-111">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ab4fa-111">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="ab4fa-112">Affichages de campagne</span><span class="sxs-lookup"><span data-stu-id="ab4fa-112">Campaign Views</span></span>](campaigns.md)

<span data-ttu-id="ab4fa-113">Cet article explique comment configurer les balises utilisateur dans le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-113">This article explains how to configure user tags in the Security Center.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="ab4fa-114">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ab4fa-114">What do you need to know before you begin?</span></span>

- <span data-ttu-id="ab4fa-115">Vous ouvrez le centre de sécurité à l’adresse <https://security.microsoft.com/> .</span><span class="sxs-lookup"><span data-stu-id="ab4fa-115">You open the Security Center at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="ab4fa-116">Pour accéder directement à la page **balises utilisateur** , ouvrez <https://security.microsoft.com/securitysettings/userTags> .</span><span class="sxs-lookup"><span data-stu-id="ab4fa-116">To go directly to the **User tags** page, open <https://security.microsoft.com/securitysettings/userTags>.</span></span>

- <span data-ttu-id="ab4fa-117">Pour créer, modifier ou supprimer des balises utilisateur, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-117">To create, modify, or remove user tags, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="ab4fa-118">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="ab4fa-118">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="ab4fa-119">Vous pouvez également gérer et surveiller les comptes de priorité dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-119">You can also manage and monitor priority accounts in the Microsoft 365 admin center.</span></span> <span data-ttu-id="ab4fa-120">Pour obtenir des instructions, consultez la rubrique [Manage and Monitor Priority Accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts).</span><span class="sxs-lookup"><span data-stu-id="ab4fa-120">For instructions, see [Manage and monitor priority accounts](https://docs.microsoft.com/microsoft-365/admin/setup/priority-accounts).</span></span>

## <a name="use-the-security-center-to-create-user-tags"></a><span data-ttu-id="ab4fa-121">Utiliser le centre de sécurité pour créer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="ab4fa-121">Use the Security Center to create user tags</span></span>

1. <span data-ttu-id="ab4fa-122">Dans le centre de sécurité, accédez à **paramètres** \> **e-mail &** les \> **balises utilisateur**de collaboration.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-122">In the Security Center, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="ab4fa-123">Sur la page **balises utilisateur** qui s’ouvre, cliquez sur **créer une balise**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-123">On the **User tags** page that opens, click **Create tag**.</span></span>

3. <span data-ttu-id="ab4fa-124">L’Assistant **créer une balise** s’ouvre en un nouveau. Dans la page **définir la balise** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ab4fa-124">The **Create tag** wizard opens in a new fly out. On the **Define tag** page, configure the following settings:</span></span>

   - <span data-ttu-id="ab4fa-125">**Nom**: entrez un nom unique et descriptif pour la balise.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-125">**Name**: Enter a unique, descriptive name for the tag.</span></span> <span data-ttu-id="ab4fa-126">Il s’agit de la valeur que vous allez voir et utiliser.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-126">This is the value that you'll see and use.</span></span>

   - <span data-ttu-id="ab4fa-127">**Description**: entrez une description facultative pour la balise.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-127">**Description**: Enter an optional description for the tag.</span></span>

   <span data-ttu-id="ab4fa-128">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-128">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="ab4fa-129">Dans la page **affecter des boîtes aux lettres** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab4fa-129">On the **Assign mailboxes** page, do either of the following steps:</span></span>

   - <span data-ttu-id="ab4fa-130">Cliquez sur **Ajouter des boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-130">Click **Add mailboxes**.</span></span> <span data-ttu-id="ab4fa-131">Dans le survol qui s’affiche, effectuez l’une des opérations suivantes pour ajouter des utilisateurs ou des groupes individuels :</span><span class="sxs-lookup"><span data-stu-id="ab4fa-131">In the fly out that appears, do any of the following steps to add individual users or groups:</span></span>

     - <span data-ttu-id="ab4fa-132">Cliquez dans la zone et faites défiler la liste pour sélectionner un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-132">Click in the box and scroll through the list to select a user or group.</span></span>
     - <span data-ttu-id="ab4fa-133">Cliquez dans la zone et commencez à taper pour filtrer la liste, puis sélectionnez un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-133">Click in the box and start typing to filter the list and select a user or group.</span></span>
     - <span data-ttu-id="ab4fa-134">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-134">To add additional values, click in an empty area in the box.</span></span>
     - <span data-ttu-id="ab4fa-135">Pour supprimer des entrées individuelles de la zone, cliquez sur **supprimer** l' ![ icône supprimer de ](../../media/scc-remove-icon.png) l’utilisateur ou du groupe dans la zone.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-135">To remove individual entries from the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user or group in the box.</span></span>
     - <span data-ttu-id="ab4fa-136">Pour supprimer les entrées existantes de la liste située en dessous du champ, cliquez sur **supprimer** ![ l’icône supprimer de l' ](../../media/scc-remove-icon.png) entrée.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-136">To remove existing entries from the list below the box, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) the entry.</span></span>

     <span data-ttu-id="ab4fa-137">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-137">When you're finished, click **Add**.</span></span>

   - <span data-ttu-id="ab4fa-138">Cliquez sur **Importer** pour sélectionner un fichier texte qui contient les adresses de messagerie des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-138">Click **Import** to select a text file that contains the email addresses of the users or groups.</span></span> <span data-ttu-id="ab4fa-139">Assurez-vous que le fichier texte contient une entrée par ligne.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-139">Be sure the text file contains one entry per line.</span></span>

   <span data-ttu-id="ab4fa-140">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-140">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="ab4fa-141">Dans la page **balise de révision** , vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-141">On the **Review tag** page, review your settings.</span></span> <span data-ttu-id="ab4fa-142">Vous pouvez cliquer sur **modifier** dans la section spécifique pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-142">You can click **Edit** in the specific section to make changes.</span></span>

   <span data-ttu-id="ab4fa-143">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-143">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-view-user-tags"></a><span data-ttu-id="ab4fa-144">Utiliser le centre de sécurité pour afficher les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="ab4fa-144">Use the Security Center to view user tags</span></span>

1. <span data-ttu-id="ab4fa-145">Dans le centre de sécurité, accédez à **paramètres** \> **e-mail &** les \> **balises utilisateur**de collaboration.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-145">In the Security Center, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="ab4fa-146">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez afficher (ne cliquez pas sur la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="ab4fa-146">On the **User tags** page that opens, select the user tag that you want to view (don't click on the checkbox).</span></span>

3. <span data-ttu-id="ab4fa-147">Dans le menu déroulant en lecture seule qui s’affiche, passez en revue les paramètres.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-147">In the read-only details fly out that appears, review the settings.</span></span>

   <span data-ttu-id="ab4fa-148">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-148">When you're finished, click **Close**.</span></span>

## <a name="use-the-security-center-to-modify-user-tags"></a><span data-ttu-id="ab4fa-149">Utiliser le centre de sécurité pour modifier les balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="ab4fa-149">Use the Security Center to modify user tags</span></span>

1. <span data-ttu-id="ab4fa-150">Dans le centre de sécurité, accédez à **paramètres** \> **e-mail &** les \> **balises utilisateur**de collaboration.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-150">In the Security Center, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="ab4fa-151">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez afficher, puis cliquez sur **modifier la balise**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-151">On the **User tags** page that opens, select the user tag that you want to view, and then click **Edit tag**.</span></span>

3. <span data-ttu-id="ab4fa-152">L’Assistant stratégie s’ouvre dans une **balise de modification** . Cliquez sur **suivant** pour passer en revue et modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-152">The policy wizard opens in an **Edit tag** fly out. Click **Next** to review and modify the settings.</span></span>

   <span data-ttu-id="ab4fa-153">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-153">When you're finished, click **Submit**.</span></span>

## <a name="use-the-security-center-to-remove-user-tags"></a><span data-ttu-id="ab4fa-154">Utiliser le centre de sécurité pour supprimer des balises utilisateur</span><span class="sxs-lookup"><span data-stu-id="ab4fa-154">Use the Security Center to remove user tags</span></span>

<span data-ttu-id="ab4fa-155">**Remarque**: vous ne pouvez pas supprimer la balise de **compte de priorité** intégrée.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-155">**Note**: You can't remove the built-in **Priority account** tag.</span></span>

1. <span data-ttu-id="ab4fa-156">Dans le centre de sécurité, accédez à **paramètres** \> **e-mail &** les \> **balises utilisateur**de collaboration.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-156">In the Security Center, go to **Settings** \> **Email & collaboration** \> **User tags**.</span></span>

2. <span data-ttu-id="ab4fa-157">Sur la page **balises utilisateur** qui s’ouvre, sélectionnez la balise utilisateur que vous souhaitez supprimer, cliquez sur **Supprimer la balise**, puis sélectionnez **Oui, supprimer** dans l’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ab4fa-157">On the **User tags** page that opens, select the user tag that you want to remove, click **Delete tag**, and then select **Yes, remove** in the warning that appears.</span></span>
