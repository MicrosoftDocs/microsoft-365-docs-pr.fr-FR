---
title: Gérer vos URL autorisées et bloquées dans la liste d’autorisation/de blocage du client
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
description: Les administrateurs peuvent apprendre à configurer les entrées d’URL dans la liste des clients autorisés/bloqués du centre de sécurité & Compliance Center.
ms.openlocfilehash: 1aae54ffd6026a7fc131017a10f9676d96be9b69
ms.sourcegitcommit: d81c7cea85af6ad5fef81d3c930514a51464368c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2020
ms.locfileid: "49572637"
---
# <a name="manage-urls-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-103">Gérer les URL dans la liste Autoriser/Bloquer du client</span><span class="sxs-lookup"><span data-stu-id="efbe6-103">Manage URLs in the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="efbe6-104">Les fonctionnalités décrites dans cette rubrique sont en mode aperçu, sont sujettes à modification et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="efbe6-104">The features described in this topic are in Preview, are subject to change, and are not available in all organizations.</span></span>

<span data-ttu-id="efbe6-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, vous pouvez ne pas utiliser le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="efbe6-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="efbe6-106">Par exemple, un bon message peut être marqué comme incorrect (faux positif) ou un message incorrect peut être autorisé par (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="efbe6-106">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="efbe6-107">La liste des clients autorisés/bloqués du centre de sécurité & conformité vous offre un moyen de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="efbe6-107">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="efbe6-108">La liste d’autorisation/de blocage de client est utilisée pendant le flux de messagerie et au moment de l’utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="efbe6-108">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="efbe6-109">Vous pouvez spécifier des URL à autoriser ou à bloquer dans la liste des clients autorisés/bloqués.</span><span class="sxs-lookup"><span data-stu-id="efbe6-109">You can specify URLs to allow or block in the Tenant Allow/Block List.</span></span>

<span data-ttu-id="efbe6-110">Cette rubrique décrit comment configurer les entrées dans la liste des clients autorisés/bloqués du centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande autonome EOP PowerShell pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="efbe6-110">This topic describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="efbe6-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="efbe6-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="efbe6-112">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="efbe6-112">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="efbe6-113">Pour accéder directement à la page d' **autorisation/de blocage de client** , utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="efbe6-113">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="efbe6-114">Les valeurs d’URL disponibles sont décrites dans la [syntaxe URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="efbe6-114">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

- <span data-ttu-id="efbe6-115">La liste d’autorisation/de blocage client autorise un nombre maximal de 500 entrées pour les URL.</span><span class="sxs-lookup"><span data-stu-id="efbe6-115">The Tenant Allow/Block List allows a maximum of 500 entries for URLs.</span></span>

- <span data-ttu-id="efbe6-116">Une entrée doit être active dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="efbe6-116">An entry should be active within 15 minutes.</span></span>

- <span data-ttu-id="efbe6-117">Les entrées bloquées prévalent sur les entrées autoriser.</span><span class="sxs-lookup"><span data-stu-id="efbe6-117">Block entries take precedence over allow entries.</span></span>

- <span data-ttu-id="efbe6-118">Par défaut, les entrées de la liste d’autorisation/de blocage client expirent au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="efbe6-118">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="efbe6-119">Vous pouvez spécifier une date ou la définir pour qu’elle n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="efbe6-119">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="efbe6-120">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="efbe6-120">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="efbe6-121">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="efbe6-121">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="efbe6-122">Avant de pouvoir effectuer les procédures décrites dans cet article, vous devez disposer d’autorisations dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="efbe6-122">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="efbe6-123">Pour ajouter et supprimer des valeurs dans la liste d’autorisation/de blocage de client, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="efbe6-123">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="efbe6-124">Pour un accès en lecture seule à la liste verte/rouge de client, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="efbe6-124">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="efbe6-125">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="efbe6-125">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="efbe6-126">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-126">**Notes**:</span></span>

  - <span data-ttu-id="efbe6-127">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le centre d’administration 365 de Microsoft donne aux utilisateurs les autorisations requises dans le centre de sécurité & conformité _et_ des autorisations pour d’autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="efbe6-127">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="efbe6-128">Si vous souhaitez en savoir plus, veuillez consulter la page [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="efbe6-128">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="efbe6-129">Le groupe de rôles gestion de l' **Organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) offre également un accès en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="efbe6-129">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-130">Utiliser le centre de sécurité & conformité pour créer des entrées d’URL dans la liste verte/rouge de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-130">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="efbe6-131">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la syntaxe de l' [URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="efbe6-131">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

1. <span data-ttu-id="efbe6-132">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="efbe6-132">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="efbe6-133">Sur la page **liste des clients autorisés/bloqués** , vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="efbe6-133">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Add**</span></span>

3. <span data-ttu-id="efbe6-134">Dans la fenêtre mobile **ajouter de nouvelles URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="efbe6-134">In the **Add new URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="efbe6-135">**Ajouter des URL avec des caractères génériques**: entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="efbe6-135">**Add URLs with wildcards**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="efbe6-136">**Bloquer/autoriser**: indiquez si vous souhaitez **autoriser** ou **bloquer** les URL spécifiées.</span><span class="sxs-lookup"><span data-stu-id="efbe6-136">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified URLs.</span></span>

   - <span data-ttu-id="efbe6-137">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="efbe6-137">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="efbe6-138">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration des entrées.</span><span class="sxs-lookup"><span data-stu-id="efbe6-138">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="efbe6-139">ou</span><span class="sxs-lookup"><span data-stu-id="efbe6-139">or</span></span>

     - <span data-ttu-id="efbe6-140">Déplacez le bouton bascule vers la droite pour configurer les entrées de sorte qu’elles n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="efbe6-140">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="efbe6-142">.</span><span class="sxs-lookup"><span data-stu-id="efbe6-142">.</span></span>

   - <span data-ttu-id="efbe6-143">**Facultatif Remarque**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="efbe6-143">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="efbe6-144">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-144">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-145">Utiliser le centre de sécurité & conformité pour afficher les entrées dans la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="efbe6-145">Use the Security & Compliance Center to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="efbe6-146">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="efbe6-146">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="efbe6-147">Sélectionnez l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="efbe6-147">Select the **URLs** tab.</span></span>

<span data-ttu-id="efbe6-148">Cliquez sur les en-têtes de colonne suivants pour trier dans l’ordre croissant ou décroissant :</span><span class="sxs-lookup"><span data-stu-id="efbe6-148">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="efbe6-149">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="efbe6-149">**Value**</span></span>
- <span data-ttu-id="efbe6-150">**Action**: **bloquer** ou **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-150">**Action**: **Block** or **Allow**.</span></span>
- <span data-ttu-id="efbe6-151">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="efbe6-151">**Last updated date**</span></span>
- <span data-ttu-id="efbe6-152">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="efbe6-152">**Expiration date**</span></span>
- <span data-ttu-id="efbe6-153">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="efbe6-153">**Note**</span></span>

<span data-ttu-id="efbe6-154">Cliquez sur **groupe** pour regrouper les entrées par **action** (**bloquer** ou **autoriser**) ou **aucune**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-154">Click **Group** to group the entries by **Action** (**Block** or **Allow**) or **None**.</span></span>

<span data-ttu-id="efbe6-155">Cliquez sur **Rechercher**, entrez la totalité ou une partie d’une valeur, puis appuyez sur entrée pour rechercher une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="efbe6-155">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="efbe6-156">Lorsque vous avez terminé, cliquez sur **Effacer** l' ![ icône Rechercher ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) .</span><span class="sxs-lookup"><span data-stu-id="efbe6-156">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="efbe6-157">Cliquez sur **filtre**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-157">Click **Filter**.</span></span> <span data-ttu-id="efbe6-158">Dans le menu volant **filtre** qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="efbe6-158">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="efbe6-159">**Action**: sélectionnez **autoriser**, **bloquer** ou les deux.</span><span class="sxs-lookup"><span data-stu-id="efbe6-159">**Action**: Select **Allow**, **Block** or both.</span></span>

- <span data-ttu-id="efbe6-160">**N’expire jamais**: sélectionnez désactivé (désactiver ![ ](../../media/scc-toggle-off.png) ) ou activé ( ![ bascule ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) ).</span><span class="sxs-lookup"><span data-stu-id="efbe6-160">**Never expire**: Select off (![Toggle off](../../media/scc-toggle-off.png)) or on (![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)).</span></span>

- <span data-ttu-id="efbe6-161">**Dernière mise à jour**: sélectionnez une date **de** début (de), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="efbe6-161">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="efbe6-162">**Date d’expiration**: sélectionnez une date de début (**de**), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="efbe6-162">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="efbe6-163">Lorsque vous avez terminé, cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-163">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="efbe6-164">Pour effacer les filtres existants, cliquez sur **Filtrer** et, dans le menu volant **filtre** qui s’affiche, cliquez sur **effacer les filtres**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-164">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-165">Utiliser le centre de sécurité & conformité pour modifier des entrées dans la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="efbe6-165">Use the Security & Compliance Center to modify entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="efbe6-166">Vous ne pouvez pas modifier la valeur de l’URL proprement dite.</span><span class="sxs-lookup"><span data-stu-id="efbe6-166">You can't modify the URL value itself.</span></span> <span data-ttu-id="efbe6-167">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="efbe6-167">Instead, you need to delete the entry and recreate it.</span></span>

1. <span data-ttu-id="efbe6-168">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="efbe6-168">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="efbe6-169">Sélectionnez l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="efbe6-169">Select the **URLs** tab.</span></span>

3. <span data-ttu-id="efbe6-170">Sélectionnez l’entrée que vous souhaitez modifier, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) .</span><span class="sxs-lookup"><span data-stu-id="efbe6-170">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="efbe6-171">Dans le menu volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="efbe6-171">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="efbe6-172">**Bloquer/autoriser**: sélectionnez **autoriser** ou **bloquer**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-172">**Block/Allow**: Select **Allow** or **Block**.</span></span>

   - <span data-ttu-id="efbe6-173">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="efbe6-173">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="efbe6-174">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="efbe6-174">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

     <span data-ttu-id="efbe6-175">ou</span><span class="sxs-lookup"><span data-stu-id="efbe6-175">or</span></span>

     - <span data-ttu-id="efbe6-176">Déplacez le bouton bascule vers la droite pour configurer l’entrée de sorte qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="efbe6-176">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="efbe6-178">.</span><span class="sxs-lookup"><span data-stu-id="efbe6-178">.</span></span>

   - <span data-ttu-id="efbe6-179">**Facultatif Remarque**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="efbe6-179">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="efbe6-180">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-180">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-181">Utiliser le centre de sécurité & conformité pour supprimer des entrées de la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="efbe6-181">Use the Security & Compliance Center to remove entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="efbe6-182">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge** de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="efbe6-182">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="efbe6-183">Sélectionnez l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="efbe6-183">Select the **URLs** tab.</span></span>

3. <span data-ttu-id="efbe6-184">Sélectionnez l’entrée que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) .</span><span class="sxs-lookup"><span data-stu-id="efbe6-184">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="efbe6-185">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="efbe6-185">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-186">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-186">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-187">Utiliser PowerShell pour ajouter des entrées dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-187">Use PowerShell to add entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="efbe6-188">Pour ajouter des entrées dans la liste d’autorisation/de blocage de client, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="efbe6-188">To add entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Action <Allow | Block> -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="efbe6-189">Cet exemple montre comment ajouter une entrée de bloc d’URL pour contoso.com et tous les sous-domaines (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="efbe6-189">This example adds a URL block entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="efbe6-190">Étant donné que nous n’utilisons pas les paramètres ExpirationDate ou noexpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="efbe6-190">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType Url -Action Block -Entries ~contoso.com
```

<span data-ttu-id="efbe6-191">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="efbe6-191">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-192">Utiliser PowerShell pour afficher les entrées dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-192">Use PowerShell to view entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="efbe6-193">Pour afficher les entrées dans la liste d’autorisation/de blocage de client, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="efbe6-193">To view entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url [-Entry <URLValue>] [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="efbe6-194">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="efbe6-194">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Action Block
```

<span data-ttu-id="efbe6-195">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="efbe6-195">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-196">Utiliser PowerShell pour modifier des entrées dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-196">Use PowerShell to modify entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="efbe6-197">Vous ne pouvez pas modifier la valeur de l’URL proprement dite.</span><span class="sxs-lookup"><span data-stu-id="efbe6-197">You can't modify the URL value itself.</span></span> <span data-ttu-id="efbe6-198">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="efbe6-198">Instead, you need to delete the entry and recreate it.</span></span>

<span data-ttu-id="efbe6-199">Pour modifier les entrées de la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="efbe6-199">To modify entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids <"Id1","Id2",..."IdN"> [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="efbe6-200">Cet exemple montre comment modifier la date d’expiration de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="efbe6-200">This example changes the expiration date of the specified entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="efbe6-201">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="efbe6-201">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-202">Utiliser PowerShell pour supprimer des entrées de la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-202">Use PowerShell to remove entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="efbe6-203">Pour supprimer des entrées de la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="efbe6-203">To remove entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="efbe6-204">Cet exemple supprime l’entrée d’URL spécifiée de la liste des clients bloqués/bloqués.</span><span class="sxs-lookup"><span data-stu-id="efbe6-204">This example removes the specified URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="efbe6-205">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="efbe6-205">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="efbe6-206">Syntaxe d’URL de la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="efbe6-206">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="efbe6-207">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="efbe6-207">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="efbe6-208">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="efbe6-208">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="efbe6-209">Unicode n’est pas pris en charge, mais Punycode est.</span><span class="sxs-lookup"><span data-stu-id="efbe6-209">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="efbe6-210">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="efbe6-210">Hostnames are allowed if all of the following statements are true:</span></span>

  - <span data-ttu-id="efbe6-211">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="efbe6-211">The hostname contains a period.</span></span>
  - <span data-ttu-id="efbe6-212">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="efbe6-212">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="efbe6-213">Il y a au moins deux caractères à droite de la période.</span><span class="sxs-lookup"><span data-stu-id="efbe6-213">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="efbe6-214">Par exemple, `t.co` est autorisé ou n’est `.com` `contoso.` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="efbe6-214">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="efbe6-215">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="efbe6-215">Subpaths are not implied.</span></span>

  <span data-ttu-id="efbe6-216">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="efbe6-216">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="efbe6-217">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="efbe6-217">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="efbe6-218">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="efbe6-218">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="efbe6-219">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="efbe6-219">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="efbe6-220">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="efbe6-220">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="efbe6-221">Par exemple, `contoso.com/*` est autorisé ou n’est `contoso.com*` `contoso.com/ab*` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="efbe6-221">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="efbe6-222">Tous les sous-chemins ne sont pas implicitement par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="efbe6-222">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="efbe6-223">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="efbe6-223">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="efbe6-224">`*.com*` n’est pas valide (ce n’est pas un domaine pouvant être résolu et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="efbe6-224">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="efbe6-225">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="efbe6-225">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="efbe6-226">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="efbe6-226">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="efbe6-227">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="efbe6-227">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="efbe6-228">Par exemple `~contoso.com` `contoso.com` , inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="efbe6-228">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="efbe6-229">Les entrées d’URL qui contiennent des protocoles (par exemple,, `http://` `https://` ou `ftp://` ) échouent, car les entrées d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="efbe6-229">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="efbe6-230">Un nom d’utilisateur ou un mot de passe n’est pas pris en charge ou obligatoire.</span><span class="sxs-lookup"><span data-stu-id="efbe6-230">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="efbe6-231">Les guillemets ('ou ") sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="efbe6-231">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="efbe6-232">Une URL doit inclure toutes les redirections, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="efbe6-232">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="efbe6-233">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="efbe6-233">URL entry scenarios</span></span>

<span data-ttu-id="efbe6-234">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="efbe6-234">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="efbe6-235">Scénario : pas de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="efbe6-235">Scenario: No wildcards</span></span>

<span data-ttu-id="efbe6-236">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="efbe6-236">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="efbe6-237">**Correspondance autorisée**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-237">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="efbe6-238">**Ne pas faire correspondre**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-238">**Allow not matched**:</span></span>

  - <span data-ttu-id="efbe6-239">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-239">abc-contoso.com</span></span>
  - <span data-ttu-id="efbe6-240">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-240">contoso.com/a</span></span>
  - <span data-ttu-id="efbe6-241">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-241">payroll.contoso.com</span></span>
  - <span data-ttu-id="efbe6-242">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-242">test.com/contoso.com</span></span>
  - <span data-ttu-id="efbe6-243">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-243">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="efbe6-244">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-244">www.contoso.com</span></span>
  - <span data-ttu-id="efbe6-245">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-245">www.contoso.com/q=a@contoso.com</span></span>
  
- <span data-ttu-id="efbe6-246">**Correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-246">**Block match**:</span></span>

  - <span data-ttu-id="efbe6-247">contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-247">contoso.com</span></span>
  - <span data-ttu-id="efbe6-248">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-248">contoso.com/a</span></span>
  - <span data-ttu-id="efbe6-249">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-249">payroll.contoso.com</span></span>
  - <span data-ttu-id="efbe6-250">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-250">test.com/contoso.com</span></span>
  - <span data-ttu-id="efbe6-251">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-251">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="efbe6-252">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-252">www.contoso.com</span></span>
  - <span data-ttu-id="efbe6-253">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-253">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="efbe6-254">**Bloc sans correspondance**: ABC-contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-254">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="efbe6-255">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="efbe6-255">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="efbe6-256">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="efbe6-256">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="efbe6-257">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-257">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-258">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-258">www.contoso.com</span></span>
  - <span data-ttu-id="efbe6-259">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-259">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="efbe6-260">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-260">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="efbe6-261">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-261">123contoso.com</span></span>
  - <span data-ttu-id="efbe6-262">contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-262">contoso.com</span></span>
  - <span data-ttu-id="efbe6-263">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-263">test.com/contoso.com</span></span>
  - <span data-ttu-id="efbe6-264">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="efbe6-264">www.contoso.com/abc</span></span>
  
#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="efbe6-265">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="efbe6-265">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="efbe6-266">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="efbe6-266">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="efbe6-267">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-267">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-268">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="efbe6-268">contoso.com/a/b</span></span>
  - <span data-ttu-id="efbe6-269">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="efbe6-269">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="efbe6-270">contoso. com/a/ ? q = joe@t. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-270">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="efbe6-271">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-271">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="efbe6-272">contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-272">contoso.com</span></span>
  - <span data-ttu-id="efbe6-273">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-273">contoso.com/a</span></span>
  - <span data-ttu-id="efbe6-274">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-274">www.contoso.com</span></span>
  - <span data-ttu-id="efbe6-275">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-275">www.contoso.com/q=a@contoso.com</span></span>
  
#### <a name="scenario-left-tilde"></a><span data-ttu-id="efbe6-276">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="efbe6-276">Scenario: Left tilde</span></span>

<span data-ttu-id="efbe6-277">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="efbe6-277">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="efbe6-278">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-278">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-279">contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-279">contoso.com</span></span>
  - <span data-ttu-id="efbe6-280">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-280">www.contoso.com</span></span>
  - <span data-ttu-id="efbe6-281">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-281">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="efbe6-282">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-282">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="efbe6-283">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-283">123contoso.com</span></span>
  - <span data-ttu-id="efbe6-284">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="efbe6-284">contoso.com/abc</span></span>
  - <span data-ttu-id="efbe6-285">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="efbe6-285">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="efbe6-286">Scénario : suffixe de caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="efbe6-286">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="efbe6-287">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="efbe6-287">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="efbe6-288">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-288">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-289">contoso. com/ ? q = whatever@fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-289">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="efbe6-290">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-290">contoso.com/a</span></span>
  - <span data-ttu-id="efbe6-291">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="efbe6-291">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="efbe6-292">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="efbe6-292">contoso.com/ab</span></span>
  - <span data-ttu-id="efbe6-293">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="efbe6-293">contoso.com/b</span></span>
  - <span data-ttu-id="efbe6-294">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="efbe6-294">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="efbe6-295">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="efbe6-295">contoso.com/ba</span></span>

- <span data-ttu-id="efbe6-296">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-296">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="efbe6-297">Scénario : sous-domaine du caractère générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="efbe6-297">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="efbe6-298">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="efbe6-298">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="efbe6-299">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-299">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-300">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="efbe6-300">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="efbe6-301">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="efbe6-301">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="efbe6-302">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-302">www.contoso.com/a</span></span>
  - <span data-ttu-id="efbe6-303">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="efbe6-303">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="efbe6-304">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="efbe6-304">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="efbe6-305">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="efbe6-305">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="efbe6-306">Scénario : tilde gauche et droit</span><span class="sxs-lookup"><span data-stu-id="efbe6-306">Scenario: Left and right tilde</span></span>

<span data-ttu-id="efbe6-307">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="efbe6-307">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="efbe6-308">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-308">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-309">contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-309">contoso.com</span></span>
  - <span data-ttu-id="efbe6-310">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-310">contoso.com/a</span></span>
  - <span data-ttu-id="efbe6-311">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-311">www.contoso.com</span></span>
  - <span data-ttu-id="efbe6-312">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="efbe6-312">www.contoso.com/b</span></span>
  - <span data-ttu-id="efbe6-313">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-313">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="efbe6-314">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-314">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="efbe6-315">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-315">123contoso.com</span></span>
  - <span data-ttu-id="efbe6-316">contoso.org</span><span class="sxs-lookup"><span data-stu-id="efbe6-316">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="efbe6-317">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="efbe6-317">Scenario: IP address</span></span>

<span data-ttu-id="efbe6-318">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="efbe6-318">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="efbe6-319">**Autoriser la correspondance** et la **correspondance de bloc**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="efbe6-319">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="efbe6-320">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-320">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="efbe6-321">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-321">1.2.3.4/a</span></span>
  - <span data-ttu-id="efbe6-322">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="efbe6-322">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="efbe6-323">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="efbe6-323">IP address with right wildcard</span></span>

<span data-ttu-id="efbe6-324">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="efbe6-324">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="efbe6-325">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-325">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="efbe6-326">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="efbe6-326">1.2.3.4/b</span></span>
  - <span data-ttu-id="efbe6-327">1.2.3.4/bAAAA</span><span class="sxs-lookup"><span data-stu-id="efbe6-327">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="efbe6-328">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="efbe6-328">Examples of invalid entries</span></span>

<span data-ttu-id="efbe6-329">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="efbe6-329">The following entries are invalid:</span></span>

- <span data-ttu-id="efbe6-330">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-330">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="efbe6-331">contoso</span><span class="sxs-lookup"><span data-stu-id="efbe6-331">contoso</span></span>
  - <span data-ttu-id="efbe6-332">\*contoso.\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-332">\*.contoso.\*</span></span>
  - <span data-ttu-id="efbe6-333">\*. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-333">\*.com</span></span>
  - <span data-ttu-id="efbe6-334">\*. pdf</span><span class="sxs-lookup"><span data-stu-id="efbe6-334">\*.pdf</span></span>

- <span data-ttu-id="efbe6-335">**Caractères génériques sur le texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-335">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="efbe6-336">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-336">\*contoso.com</span></span>
  - <span data-ttu-id="efbe6-337">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-337">contoso.com\*</span></span>
  - <span data-ttu-id="efbe6-338">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="efbe6-338">\*1.2.3.4</span></span>
  - <span data-ttu-id="efbe6-339">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-339">1.2.3.4\*</span></span>
  - <span data-ttu-id="efbe6-340">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-340">contoso.com/a\*</span></span>
  - <span data-ttu-id="efbe6-341">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-341">contoso.com/ab\*</span></span>

- <span data-ttu-id="efbe6-342">**Adresses IP avec des ports**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-342">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="efbe6-343">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="efbe6-343">contoso.com:443</span></span>
  - <span data-ttu-id="efbe6-344">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="efbe6-344">abc.contoso.com:25</span></span>

- <span data-ttu-id="efbe6-345">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-345">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="efbe6-346">\*.\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-346">\*.\*</span></span>

- <span data-ttu-id="efbe6-347">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="efbe6-347">**Middle wildcards**:</span></span>

  - <span data-ttu-id="efbe6-348">CONT \* so.com</span><span class="sxs-lookup"><span data-stu-id="efbe6-348">conto\*so.com</span></span>
  - <span data-ttu-id="efbe6-349">Conto ~ so. com</span><span class="sxs-lookup"><span data-stu-id="efbe6-349">conto~so.com</span></span>

- <span data-ttu-id="efbe6-350">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="efbe6-350">**Double wildcards**</span></span>

  - <span data-ttu-id="efbe6-351">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-351">contoso.com/\*\*</span></span>
  - <span data-ttu-id="efbe6-352">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="efbe6-352">contoso.com/\*/\*</span></span>
