---
title: Gérer vos autoriser et bloquer dans la liste d’autoriser/bloquer le client
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
description: Les administrateurs peuvent apprendre à configurer des autoriser et des blocs dans la liste d’adresses client autoriser/bloquer dans le portail de sécurité.
ms.openlocfilehash: c789b09224d00f5bb41ae29d6d2a6efa64d23a8d
ms.sourcegitcommit: 495b66b77d6dbe6d69e5b06b304089e4e476e568
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "49799712"
---
# <a name="managing-allows-and-blocks-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-103">Gestion des autoriser et des blocs dans la liste d’accès/blocage du client</span><span class="sxs-lookup"><span data-stu-id="9963b-103">Managing allows and blocks in the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="9963b-104">Les fonctionnalités décrites dans cet article sont en prévisualisation, peuvent faire l’objet de changements et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="9963b-104">The features described in this article are in Preview, are subject to change, and are not available in all organizations.</span></span>

<span data-ttu-id="9963b-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, vous pouvez ne pas être d’accord avec le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="9963b-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="9963b-106">Par exemple, un bon message peut être marqué comme mauvais (faux positif) ou un message erroné peut être autorisé (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="9963b-106">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="9963b-107">La liste d’attente des clients dans le Centre de sécurité & conformité vous permet de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9963b-107">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="9963b-108">La liste d’adresses client autoriser/bloquer est utilisée pendant le flux de messagerie et au moment des clics de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9963b-108">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="9963b-109">Vous pouvez spécifier des URL à autoriser ou à bloquer dans la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="9963b-109">You can specify URLs to allow or block in the Tenant Allow/Block List.</span></span>

<span data-ttu-id="9963b-110">Cette rubrique décrit comment configurer des entrées dans la liste d’adresses client autoriser/bloquer dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="9963b-110">This topic describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9963b-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9963b-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9963b-112">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="9963b-112">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="9963b-113">Pour aller directement à la page Liste **d’accueil/de** blocage du client, utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="9963b-113">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="9963b-114">Les valeurs d’URL disponibles sont décrites dans la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) de la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9963b-114">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

- <span data-ttu-id="9963b-115">La liste d’adresses client autorise un maximum de 500 entrées pour les URL.</span><span class="sxs-lookup"><span data-stu-id="9963b-115">The Tenant Allow/Block List allows a maximum of 500 entries for URLs.</span></span>

- <span data-ttu-id="9963b-116">Une entrée doit être active dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="9963b-116">An entry should be active within 15 minutes.</span></span>

- <span data-ttu-id="9963b-117">Les entrées de bloc sont prioritaires sur les entrées d’accès.</span><span class="sxs-lookup"><span data-stu-id="9963b-117">Block entries take precedence over allow entries.</span></span>

- <span data-ttu-id="9963b-118">Par défaut, les entrées de la liste d’inscriptions au client sont expirées au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="9963b-118">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="9963b-119">Vous pouvez spécifier une date ou les définir pour qu’elles n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="9963b-119">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="9963b-120">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="9963b-120">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="9963b-121">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="9963b-121">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="9963b-122">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="9963b-122">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="9963b-123">Pour ajouter et supprimer des valeurs de la liste d’attente des locataires, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="9963b-123">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="9963b-124">Pour un accès en lecture seule à la liste d’accès  au  client autorisé/bloqué, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9963b-124">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="9963b-125">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9963b-125">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="9963b-126">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="9963b-126">**Notes**:</span></span>

  - <span data-ttu-id="9963b-127">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9963b-127">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="9963b-128">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="9963b-128">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="9963b-129">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9963b-129">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-130">Utiliser le Centre de sécurité & conformité pour créer des entrées d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="9963b-130">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9963b-131">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) pour la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9963b-131">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

1. <span data-ttu-id="9963b-132">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9963b-132">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9963b-133">Dans la page **Liste d’adresses client autoriser/bloquer,** vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Ajouter**</span><span class="sxs-lookup"><span data-stu-id="9963b-133">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Add**</span></span>

3. <span data-ttu-id="9963b-134">Dans le **volant Ajouter de** nouvelles URL qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9963b-134">In the **Add new URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9963b-135">**Ajouter des URL avec des caractères génériques**: entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="9963b-135">**Add URLs with wildcards**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="9963b-136">**Bloquer/Autoriser**: indiquez si vous **souhaitez** autoriser ou **bloquer** les URL spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9963b-136">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified URLs.</span></span>

   - <span data-ttu-id="9963b-137">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9963b-137">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9963b-138">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="9963b-138">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="9963b-139">ou</span><span class="sxs-lookup"><span data-stu-id="9963b-139">or</span></span>

     - <span data-ttu-id="9963b-140">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="9963b-140">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="9963b-142">.</span><span class="sxs-lookup"><span data-stu-id="9963b-142">.</span></span>

   - <span data-ttu-id="9963b-143">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="9963b-143">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="9963b-144">Lorsque vous avez terminé, cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="9963b-144">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-145">Utiliser le Centre de sécurité & conformité pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9963b-145">Use the Security & Compliance Center to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9963b-146">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9963b-146">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9963b-147">Sélectionnez **l’onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="9963b-147">Select the **URLs** tab.</span></span>

<span data-ttu-id="9963b-148">Cliquez sur les en-tête de colonne suivants pour trier par ordre croissant ou décroit :</span><span class="sxs-lookup"><span data-stu-id="9963b-148">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="9963b-149">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9963b-149">**Value**</span></span>
- <span data-ttu-id="9963b-150">**Action**: **bloquer ou** **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="9963b-150">**Action**: **Block** or **Allow**.</span></span>
- <span data-ttu-id="9963b-151">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="9963b-151">**Last updated date**</span></span>
- <span data-ttu-id="9963b-152">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="9963b-152">**Expiration date**</span></span>
- <span data-ttu-id="9963b-153">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="9963b-153">**Note**</span></span>

<span data-ttu-id="9963b-154">Cliquez **sur Groupe** pour grouper les entrées par **Action** **(Bloquer** ou **Autoriser)** ou **Aucune**.</span><span class="sxs-lookup"><span data-stu-id="9963b-154">Click **Group** to group the entries by **Action** (**Block** or **Allow**) or **None**.</span></span>

<span data-ttu-id="9963b-155">Cliquez **sur** Rechercher, entrez une partie ou l’ensemble d’une valeur, puis appuyez sur Entrée pour trouver une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="9963b-155">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="9963b-156">Lorsque vous avez terminé, cliquez sur **Effacer l’icône** ![ effacer la ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) recherche.</span><span class="sxs-lookup"><span data-stu-id="9963b-156">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="9963b-157">Cliquez sur **Filtrer.**</span><span class="sxs-lookup"><span data-stu-id="9963b-157">Click **Filter**.</span></span> <span data-ttu-id="9963b-158">Dans le **flyout** Filter qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9963b-158">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="9963b-159">**Action**: **sélectionnez Autoriser,** **Bloquer** ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9963b-159">**Action**: Select **Allow**, **Block** or both.</span></span>

- <span data-ttu-id="9963b-160">**N’expirez** jamais : sélectionnez Off: ![ Toggle off ](../../media/scc-toggle-off.png) or on: ![ Toggle on ](../../media/scc-toggle-on.png) .</span><span class="sxs-lookup"><span data-stu-id="9963b-160">**Never expire**: Select off: ![Toggle off](../../media/scc-toggle-off.png) or on: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

- <span data-ttu-id="9963b-161">**Dernière mise à jour**: sélectionnez une date de début (**De**), une date de fin (**À**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9963b-161">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="9963b-162">**Date d’expiration**: sélectionnez une date de début (**De**), une date de fin (**À**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9963b-162">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="9963b-163">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="9963b-163">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="9963b-164">Pour effacer les filtres existants,  cliquez sur **Filtrer** et, dans le volant de filtre qui s’affiche, cliquez **sur Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="9963b-164">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-165">Utiliser le Centre de sécurité & conformité pour modifier des entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9963b-165">Use the Security & Compliance Center to modify entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9963b-166">Vous ne pouvez pas modifier la valeur de l’URL elle-même.</span><span class="sxs-lookup"><span data-stu-id="9963b-166">You can't modify the URL value itself.</span></span> <span data-ttu-id="9963b-167">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="9963b-167">Instead, you need to delete the entry and recreate it.</span></span>

1. <span data-ttu-id="9963b-168">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9963b-168">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9963b-169">Sélectionnez **l’onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="9963b-169">Select the **URLs** tab.</span></span>

3. <span data-ttu-id="9963b-170">Sélectionnez l’entrée à modifier,  puis cliquez sur Modifier ![ l’icône ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="9963b-170">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="9963b-171">Dans le volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9963b-171">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9963b-172">**Bloquer/Autoriser :** **sélectionnez Autoriser** ou **Bloquer.**</span><span class="sxs-lookup"><span data-stu-id="9963b-172">**Block/Allow**: Select **Allow** or **Block**.</span></span>

   - <span data-ttu-id="9963b-173">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9963b-173">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9963b-174">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration de l’entrée. </span><span class="sxs-lookup"><span data-stu-id="9963b-174">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

     <span data-ttu-id="9963b-175">ou</span><span class="sxs-lookup"><span data-stu-id="9963b-175">or</span></span>

     - <span data-ttu-id="9963b-176">Déplacez le basculement vers la droite pour configurer l’entrée pour qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="9963b-176">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="9963b-178">.</span><span class="sxs-lookup"><span data-stu-id="9963b-178">.</span></span>

   - <span data-ttu-id="9963b-179">**Remarque facultative**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9963b-179">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="9963b-180">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9963b-180">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-181">Utiliser le Centre de sécurité & conformité pour supprimer des entrées de la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9963b-181">Use the Security & Compliance Center to remove entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9963b-182">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9963b-182">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9963b-183">Sélectionnez **l’onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="9963b-183">Select the **URLs** tab.</span></span>

3. <span data-ttu-id="9963b-184">Sélectionnez l’entrée à supprimer, puis cliquez **sur** Supprimer ![ l’icône ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="9963b-184">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="9963b-185">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="9963b-185">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-186">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="9963b-186">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-187">Utiliser PowerShell pour ajouter des entrées dans la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="9963b-187">Use PowerShell to add entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9963b-188">Pour ajouter des entrées dans la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9963b-188">To add entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Action <Allow | Block> -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="9963b-189">Cet exemple ajoute une entrée de bloc d’URL pour contoso.com et tous les sous-contoso.com (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="9963b-189">This example adds a URL block entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="9963b-190">Étant donné que nous n’avons pas utilisé les paramètres ExpirationDate ou NoExpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="9963b-190">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType Url -Action Block -Entries ~contoso.com
```

<span data-ttu-id="9963b-191">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9963b-191">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-192">Utiliser PowerShell pour afficher les entrées dans la liste d’attente du client</span><span class="sxs-lookup"><span data-stu-id="9963b-192">Use PowerShell to view entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9963b-193">Pour afficher les entrées de la liste d’inscriptions client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9963b-193">To view entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url [-Entry <URLValue>] [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="9963b-194">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="9963b-194">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Action Block
```

<span data-ttu-id="9963b-195">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems.](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems)</span><span class="sxs-lookup"><span data-stu-id="9963b-195">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-196">Utiliser PowerShell pour modifier des entrées dans la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="9963b-196">Use PowerShell to modify entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9963b-197">Vous ne pouvez pas modifier la valeur de l’URL elle-même.</span><span class="sxs-lookup"><span data-stu-id="9963b-197">You can't modify the URL value itself.</span></span> <span data-ttu-id="9963b-198">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="9963b-198">Instead, you need to delete the entry and recreate it.</span></span>

<span data-ttu-id="9963b-199">Pour modifier des entrées dans la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9963b-199">To modify entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids <"Id1","Id2",..."IdN"> [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="9963b-200">Cet exemple modifie la date d’expiration de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9963b-200">This example changes the expiration date of the specified entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="9963b-201">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9963b-201">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-202">Utiliser PowerShell pour supprimer des entrées de la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="9963b-202">Use PowerShell to remove entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="9963b-203">Pour supprimer des entrées de la liste des locataires autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9963b-203">To remove entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="9963b-204">Cet exemple supprime l’entrée d’URL spécifiée de la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="9963b-204">This example removes the specified URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="9963b-205">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9963b-205">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="9963b-206">Syntaxe d’URL pour la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="9963b-206">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="9963b-207">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="9963b-207">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="9963b-208">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="9963b-208">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="9963b-209">Unicode n’est pas pris en charge, mais c’est le cas de Punycode.</span><span class="sxs-lookup"><span data-stu-id="9963b-209">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="9963b-210">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="9963b-210">Hostnames are allowed if all of the following statements are true:</span></span>

  - <span data-ttu-id="9963b-211">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="9963b-211">The hostname contains a period.</span></span>
  - <span data-ttu-id="9963b-212">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="9963b-212">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="9963b-213">Il y a au moins deux caractères à droite du point.</span><span class="sxs-lookup"><span data-stu-id="9963b-213">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="9963b-214">Par exemple, `t.co` est autorisé ou `.com` `contoso.` non.</span><span class="sxs-lookup"><span data-stu-id="9963b-214">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="9963b-215">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="9963b-215">Subpaths are not implied.</span></span>

  <span data-ttu-id="9963b-216">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="9963b-216">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="9963b-217">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9963b-217">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="9963b-218">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="9963b-218">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="9963b-219">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="9963b-219">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="9963b-220">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9963b-220">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="9963b-221">Par exemple, `contoso.com/*` est autorisé ou `contoso.com*` `contoso.com/ab*` non.</span><span class="sxs-lookup"><span data-stu-id="9963b-221">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="9963b-222">Tous les sous-chemins ne sont pas impliqués par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="9963b-222">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="9963b-223">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="9963b-223">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="9963b-224">`*.com*` n’est pas valide (domaine non résolvable et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="9963b-224">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="9963b-225">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="9963b-225">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="9963b-226">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9963b-226">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="9963b-227">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="9963b-227">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="9963b-228">Par `~contoso.com` exemple, `contoso.com` inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="9963b-228">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="9963b-229">Les entrées d’URL qui contiennent des protocoles (par exemple, , ou ) échouent, car les entrées `http://` `https://` `ftp://` d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="9963b-229">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="9963b-230">Un nom d’utilisateur ou un mot de passe ne sont pas pris en charge ou requis.</span><span class="sxs-lookup"><span data-stu-id="9963b-230">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="9963b-231">Les guillemets (' ou « ) sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9963b-231">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="9963b-232">Une URL doit inclure toutes les redirections lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="9963b-232">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="9963b-233">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="9963b-233">URL entry scenarios</span></span>

<span data-ttu-id="9963b-234">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9963b-234">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="9963b-235">Scénario : aucun caractère générique</span><span class="sxs-lookup"><span data-stu-id="9963b-235">Scenario: No wildcards</span></span>

<span data-ttu-id="9963b-236">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9963b-236">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="9963b-237">**Autoriser la correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-237">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="9963b-238">**Autoriser non la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-238">**Allow not matched**:</span></span>

  - <span data-ttu-id="9963b-239">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-239">abc-contoso.com</span></span>
  - <span data-ttu-id="9963b-240">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9963b-240">contoso.com/a</span></span>
  - <span data-ttu-id="9963b-241">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-241">payroll.contoso.com</span></span>
  - <span data-ttu-id="9963b-242">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-242">test.com/contoso.com</span></span>
  - <span data-ttu-id="9963b-243">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-243">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="9963b-244">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-244">www.contoso.com</span></span>
  - <span data-ttu-id="9963b-245">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-245">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="9963b-246">**Bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-246">**Block match**:</span></span>

  - <span data-ttu-id="9963b-247">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-247">contoso.com</span></span>
  - <span data-ttu-id="9963b-248">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9963b-248">contoso.com/a</span></span>
  - <span data-ttu-id="9963b-249">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-249">payroll.contoso.com</span></span>
  - <span data-ttu-id="9963b-250">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-250">test.com/contoso.com</span></span>
  - <span data-ttu-id="9963b-251">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-251">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="9963b-252">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-252">www.contoso.com</span></span>
  - <span data-ttu-id="9963b-253">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-253">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="9963b-254">**Bloc non correspond :** abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-254">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="9963b-255">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="9963b-255">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="9963b-256">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9963b-256">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="9963b-257">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-257">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-258">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-258">www.contoso.com</span></span>
  - <span data-ttu-id="9963b-259">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-259">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9963b-260">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9963b-260">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9963b-261">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-261">123contoso.com</span></span>
  - <span data-ttu-id="9963b-262">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-262">contoso.com</span></span>
  - <span data-ttu-id="9963b-263">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-263">test.com/contoso.com</span></span>
  - <span data-ttu-id="9963b-264">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9963b-264">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="9963b-265">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9963b-265">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="9963b-266">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="9963b-266">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="9963b-267">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-267">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-268">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="9963b-268">contoso.com/a/b</span></span>
  - <span data-ttu-id="9963b-269">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9963b-269">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9963b-270">contoso.com/a/?q=joe@t.com</span><span class="sxs-lookup"><span data-stu-id="9963b-270">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="9963b-271">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9963b-271">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9963b-272">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-272">contoso.com</span></span>
  - <span data-ttu-id="9963b-273">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9963b-273">contoso.com/a</span></span>
  - <span data-ttu-id="9963b-274">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-274">www.contoso.com</span></span>
  - <span data-ttu-id="9963b-275">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-275">www.contoso.com/q=a@contoso.com</span></span>

#### <a name="scenario-left-tilde"></a><span data-ttu-id="9963b-276">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="9963b-276">Scenario: Left tilde</span></span>

<span data-ttu-id="9963b-277">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9963b-277">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="9963b-278">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-278">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-279">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-279">contoso.com</span></span>
  - <span data-ttu-id="9963b-280">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-280">www.contoso.com</span></span>
  - <span data-ttu-id="9963b-281">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-281">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9963b-282">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9963b-282">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9963b-283">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-283">123contoso.com</span></span>
  - <span data-ttu-id="9963b-284">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9963b-284">contoso.com/abc</span></span>
  - <span data-ttu-id="9963b-285">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9963b-285">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="9963b-286">Scénario : suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="9963b-286">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="9963b-287">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="9963b-287">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="9963b-288">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-288">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-289">contoso.com/?q=whatever@fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="9963b-289">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="9963b-290">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9963b-290">contoso.com/a</span></span>
  - <span data-ttu-id="9963b-291">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9963b-291">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9963b-292">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="9963b-292">contoso.com/ab</span></span>
  - <span data-ttu-id="9963b-293">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9963b-293">contoso.com/b</span></span>
  - <span data-ttu-id="9963b-294">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="9963b-294">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="9963b-295">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="9963b-295">contoso.com/ba</span></span>

- <span data-ttu-id="9963b-296">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-296">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="9963b-297">Scénario : sous-domaine générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="9963b-297">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="9963b-298">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="9963b-298">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="9963b-299">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-299">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-300">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="9963b-300">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="9963b-301">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9963b-301">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9963b-302">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9963b-302">www.contoso.com/a</span></span>
  - <span data-ttu-id="9963b-303">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="9963b-303">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="9963b-304">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="9963b-304">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="9963b-305">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9963b-305">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="9963b-306">Scénario : tilde gauche et droite</span><span class="sxs-lookup"><span data-stu-id="9963b-306">Scenario: Left and right tilde</span></span>

<span data-ttu-id="9963b-307">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="9963b-307">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="9963b-308">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-308">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-309">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-309">contoso.com</span></span>
  - <span data-ttu-id="9963b-310">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9963b-310">contoso.com/a</span></span>
  - <span data-ttu-id="9963b-311">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-311">www.contoso.com</span></span>
  - <span data-ttu-id="9963b-312">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9963b-312">www.contoso.com/b</span></span>
  - <span data-ttu-id="9963b-313">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-313">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9963b-314">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9963b-314">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9963b-315">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-315">123contoso.com</span></span>
  - <span data-ttu-id="9963b-316">contoso.org</span><span class="sxs-lookup"><span data-stu-id="9963b-316">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="9963b-317">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="9963b-317">Scenario: IP address</span></span>

<span data-ttu-id="9963b-318">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="9963b-318">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="9963b-319">**Autoriser la correspondance** **et bloquer la correspondance**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9963b-319">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="9963b-320">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9963b-320">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9963b-321">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="9963b-321">1.2.3.4/a</span></span>
  - <span data-ttu-id="9963b-322">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="9963b-322">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="9963b-323">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="9963b-323">IP address with right wildcard</span></span>

<span data-ttu-id="9963b-324">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="9963b-324">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="9963b-325">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9963b-325">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9963b-326">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="9963b-326">1.2.3.4/b</span></span>
  - <span data-ttu-id="9963b-327">1.2.3.4/baaaa</span><span class="sxs-lookup"><span data-stu-id="9963b-327">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="9963b-328">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="9963b-328">Examples of invalid entries</span></span>

<span data-ttu-id="9963b-329">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="9963b-329">The following entries are invalid:</span></span>

- <span data-ttu-id="9963b-330">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="9963b-330">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="9963b-331">contoso</span><span class="sxs-lookup"><span data-stu-id="9963b-331">contoso</span></span>
  - <span data-ttu-id="9963b-332">\*.contoso.\*</span><span class="sxs-lookup"><span data-stu-id="9963b-332">\*.contoso.\*</span></span>
  - <span data-ttu-id="9963b-333">\*.com</span><span class="sxs-lookup"><span data-stu-id="9963b-333">\*.com</span></span>
  - <span data-ttu-id="9963b-334">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="9963b-334">\*.pdf</span></span>

- <span data-ttu-id="9963b-335">**Caractère générique sur du texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="9963b-335">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="9963b-336">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="9963b-336">\*contoso.com</span></span>
  - <span data-ttu-id="9963b-337">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="9963b-337">contoso.com\*</span></span>
  - <span data-ttu-id="9963b-338">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9963b-338">\*1.2.3.4</span></span>
  - <span data-ttu-id="9963b-339">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="9963b-339">1.2.3.4\*</span></span>
  - <span data-ttu-id="9963b-340">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="9963b-340">contoso.com/a\*</span></span>
  - <span data-ttu-id="9963b-341">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="9963b-341">contoso.com/ab\*</span></span>

- <span data-ttu-id="9963b-342">**Adresses IP avec ports**:</span><span class="sxs-lookup"><span data-stu-id="9963b-342">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="9963b-343">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="9963b-343">contoso.com:443</span></span>
  - <span data-ttu-id="9963b-344">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="9963b-344">abc.contoso.com:25</span></span>

- <span data-ttu-id="9963b-345">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="9963b-345">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="9963b-346">\*.\*</span><span class="sxs-lookup"><span data-stu-id="9963b-346">\*.\*</span></span>

- <span data-ttu-id="9963b-347">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="9963b-347">**Middle wildcards**:</span></span>

  - <span data-ttu-id="9963b-348">conto \* so.com</span><span class="sxs-lookup"><span data-stu-id="9963b-348">conto\*so.com</span></span>
  - <span data-ttu-id="9963b-349">conto~so.com</span><span class="sxs-lookup"><span data-stu-id="9963b-349">conto~so.com</span></span>

- <span data-ttu-id="9963b-350">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="9963b-350">**Double wildcards**</span></span>

  - <span data-ttu-id="9963b-351">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="9963b-351">contoso.com/\*\*</span></span>
  - <span data-ttu-id="9963b-352">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="9963b-352">contoso.com/\*/\*</span></span>
