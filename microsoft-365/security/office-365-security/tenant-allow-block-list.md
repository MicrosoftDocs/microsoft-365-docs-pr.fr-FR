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
ms.openlocfilehash: eb9dcc5b239aae1366a0a2e0eebd68b3f0082e6b
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48202338"
---
# <a name="manage-urls-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-103">Gérer les URL dans la liste verte/rouge du client</span><span class="sxs-lookup"><span data-stu-id="8c95f-103">Manage URLs in the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="8c95f-104">Les fonctionnalités décrites dans cette rubrique sont en mode aperçu, sont sujettes à modification et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="8c95f-104">The features described in this topic are in Preview, are subject to change, and are not available in all organizations.</span></span>

<span data-ttu-id="8c95f-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, vous pouvez ne pas utiliser le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="8c95f-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="8c95f-106">Par exemple, un bon message peut être marqué comme incorrect (faux positif) ou un message incorrect peut être autorisé par (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="8c95f-106">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="8c95f-107">La liste des clients autorisés/bloqués du centre de sécurité & conformité vous offre un moyen de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8c95f-107">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="8c95f-108">La liste d’autorisation/de blocage de client est utilisée pendant le flux de messagerie et au moment de l’utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="8c95f-108">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="8c95f-109">Vous pouvez spécifier des URL à autoriser ou à bloquer dans la liste des clients autorisés/bloqués.</span><span class="sxs-lookup"><span data-stu-id="8c95f-109">You can specify URLs to allow or block in the Tenant Allow/Block List.</span></span>

<span data-ttu-id="8c95f-110">Cette rubrique décrit comment configurer les entrées dans la liste des clients autorisés/bloqués du centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande autonome EOP PowerShell pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="8c95f-110">This topic describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8c95f-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8c95f-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8c95f-112">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="8c95f-112">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="8c95f-113">Pour accéder directement à la page d' **autorisation/de blocage de client** , utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="8c95f-113">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="8c95f-114">Les valeurs d’URL disponibles sont décrites dans la [syntaxe URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8c95f-114">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

- <span data-ttu-id="8c95f-115">La liste d’autorisation/de blocage client autorise un nombre maximal de 500 entrées pour les URL.</span><span class="sxs-lookup"><span data-stu-id="8c95f-115">The Tenant Allow/Block List allows a maximum of 500 entries for URLs.</span></span>

- <span data-ttu-id="8c95f-116">Une entrée doit être active dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="8c95f-116">An entry should be active within 15 minutes.</span></span>

- <span data-ttu-id="8c95f-117">Les entrées bloquées prévalent sur les entrées autoriser.</span><span class="sxs-lookup"><span data-stu-id="8c95f-117">Block entries take precedence over allow entries.</span></span>

- <span data-ttu-id="8c95f-118">Par défaut, les entrées de la liste d’autorisation/de blocage client expirent au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="8c95f-118">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="8c95f-119">Vous pouvez spécifier une date ou la définir pour qu’elle n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="8c95f-119">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="8c95f-120">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="8c95f-120">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="8c95f-121">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="8c95f-121">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="8c95f-122">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures. décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="8c95f-122">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="8c95f-123">Pour ajouter et supprimer des valeurs dans la liste d’autorisation/de blocage de client, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-123">To add and remove values from the Tenant Allow/Block List, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="8c95f-124">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8c95f-124">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="8c95f-125">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="8c95f-125">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="8c95f-126">Pour un accès en lecture seule à la liste verte/rouge de client, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-126">For read-only access to the Tenant Allow/Block List, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="8c95f-127">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8c95f-127">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="8c95f-128">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="8c95f-128">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-129">Utiliser le centre de sécurité & conformité pour créer des entrées d’URL dans la liste verte/rouge de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-129">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="8c95f-130">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la syntaxe de l' [URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8c95f-130">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

1. <span data-ttu-id="8c95f-131">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="8c95f-131">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="8c95f-132">Sur la page **liste des clients autorisés/bloqués** , vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="8c95f-132">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Add**</span></span>

3. <span data-ttu-id="8c95f-133">Dans la fenêtre mobile **ajouter de nouvelles URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-133">In the **Add new URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="8c95f-134">**Ajouter des URL avec des caractères génériques**: entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="8c95f-134">**Add URLs with wildcards**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="8c95f-135">**Bloquer/autoriser**: indiquez si vous souhaitez **autoriser** ou **bloquer** les URL spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8c95f-135">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified URLs.</span></span>

   - <span data-ttu-id="8c95f-136">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c95f-136">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="8c95f-137">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration des entrées.</span><span class="sxs-lookup"><span data-stu-id="8c95f-137">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="8c95f-138">ou</span><span class="sxs-lookup"><span data-stu-id="8c95f-138">or</span></span>

     - <span data-ttu-id="8c95f-139">Déplacez le bouton bascule vers la droite pour configurer les entrées de sorte qu’elles n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="8c95f-139">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="8c95f-141">.</span><span class="sxs-lookup"><span data-stu-id="8c95f-141">.</span></span>

   - <span data-ttu-id="8c95f-142">**Facultatif Remarque**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="8c95f-142">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="8c95f-143">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-143">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-144">Utiliser le centre de sécurité & conformité pour afficher les entrées dans la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="8c95f-144">Use the Security & Compliance Center to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="8c95f-145">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="8c95f-145">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="8c95f-146">Sélectionnez l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="8c95f-146">Select the **URLs** tab.</span></span>

<span data-ttu-id="8c95f-147">Cliquez sur les en-têtes de colonne suivants pour trier dans l’ordre croissant ou décroissant :</span><span class="sxs-lookup"><span data-stu-id="8c95f-147">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="8c95f-148">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8c95f-148">**Value**</span></span>
- <span data-ttu-id="8c95f-149">**Action**: **bloquer** ou **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-149">**Action**: **Block** or **Allow**.</span></span>
- <span data-ttu-id="8c95f-150">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="8c95f-150">**Last updated date**</span></span>
- <span data-ttu-id="8c95f-151">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="8c95f-151">**Expiration date**</span></span>
- <span data-ttu-id="8c95f-152">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="8c95f-152">**Note**</span></span>

<span data-ttu-id="8c95f-153">Cliquez sur **groupe** pour regrouper les entrées par **action** (**bloquer** ou **autoriser**) ou **aucune**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-153">Click **Group** to group the entries by **Action** (**Block** or **Allow**) or **None**.</span></span>

<span data-ttu-id="8c95f-154">Cliquez sur **Rechercher**, entrez la totalité ou une partie d’une valeur, puis appuyez sur entrée pour rechercher une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8c95f-154">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="8c95f-155">Lorsque vous avez terminé, cliquez sur **Effacer** l' ![ icône Rechercher ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) .</span><span class="sxs-lookup"><span data-stu-id="8c95f-155">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="8c95f-156">Cliquez sur **filtre**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-156">Click **Filter**.</span></span> <span data-ttu-id="8c95f-157">Dans le menu volant **filtre** qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-157">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="8c95f-158">**Action**: sélectionnez **autoriser**, **bloquer** ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8c95f-158">**Action**: Select **Allow**, **Block** or both.</span></span>

- <span data-ttu-id="8c95f-159">**N’expire jamais**: sélectionnez désactivé (désactiver ![ ](../../media/scc-toggle-off.png) ) ou activé ( ![ bascule ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) ).</span><span class="sxs-lookup"><span data-stu-id="8c95f-159">**Never expire**: Select off (![Toggle off](../../media/scc-toggle-off.png)) or on (![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)).</span></span>

- <span data-ttu-id="8c95f-160">**Dernière mise à jour**: sélectionnez une date**de**début (de), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8c95f-160">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="8c95f-161">**Date d’expiration**: sélectionnez une date de début (**de**), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8c95f-161">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="8c95f-162">Lorsque vous avez terminé, cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-162">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="8c95f-163">Pour effacer les filtres existants, cliquez sur **Filtrer**et, dans le menu volant **filtre** qui s’affiche, cliquez sur **effacer les filtres**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-163">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-164">Utiliser le centre de sécurité & conformité pour modifier des entrées dans la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="8c95f-164">Use the Security & Compliance Center to modify entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="8c95f-165">Vous ne pouvez pas modifier la valeur de l’URL proprement dite.</span><span class="sxs-lookup"><span data-stu-id="8c95f-165">You can't modify the URL value itself.</span></span> <span data-ttu-id="8c95f-166">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="8c95f-166">Instead, you need to delete the entry and recreate it.</span></span>

1. <span data-ttu-id="8c95f-167">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="8c95f-167">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="8c95f-168">Sélectionnez l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="8c95f-168">Select the **URLs** tab.</span></span>

3. <span data-ttu-id="8c95f-169">Sélectionnez l’entrée que vous souhaitez modifier, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) .</span><span class="sxs-lookup"><span data-stu-id="8c95f-169">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="8c95f-170">Dans le menu volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-170">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="8c95f-171">**Bloquer/autoriser**: sélectionnez **autoriser** ou **bloquer**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-171">**Block/Allow**: Select **Allow** or **Block**.</span></span>

   - <span data-ttu-id="8c95f-172">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c95f-172">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="8c95f-173">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c95f-173">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

     <span data-ttu-id="8c95f-174">ou</span><span class="sxs-lookup"><span data-stu-id="8c95f-174">or</span></span>

     - <span data-ttu-id="8c95f-175">Déplacez le bouton bascule vers la droite pour configurer l’entrée de sorte qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="8c95f-175">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="8c95f-177">.</span><span class="sxs-lookup"><span data-stu-id="8c95f-177">.</span></span>

   - <span data-ttu-id="8c95f-178">**Facultatif Remarque**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c95f-178">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="8c95f-179">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-179">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-180">Utiliser le centre de sécurité & conformité pour supprimer des entrées de la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="8c95f-180">Use the Security & Compliance Center to remove entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="8c95f-181">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="8c95f-181">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="8c95f-182">Sélectionnez l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="8c95f-182">Select the **URLs** tab.</span></span>

3. <span data-ttu-id="8c95f-183">Sélectionnez l’entrée que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) .</span><span class="sxs-lookup"><span data-stu-id="8c95f-183">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="8c95f-184">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="8c95f-184">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-185">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-185">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-186">Utiliser PowerShell pour ajouter des entrées dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-186">Use PowerShell to add entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="8c95f-187">Pour ajouter des entrées dans la liste d’autorisation/de blocage de client, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8c95f-187">To add entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Action <Allow | Block> -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="8c95f-188">Cet exemple montre comment ajouter une entrée de bloc d’URL pour contoso.com et tous les sous-domaines (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="8c95f-188">This example adds a URL block entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="8c95f-189">Étant donné que nous n’utilisons pas les paramètres ExpirationDate ou noexpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="8c95f-189">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType Url -Action Block -Entries ~contoso.com
```

<span data-ttu-id="8c95f-190">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="8c95f-190">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-191">Utiliser PowerShell pour afficher les entrées dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-191">Use PowerShell to view entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="8c95f-192">Pour afficher les entrées dans la liste d’autorisation/de blocage de client, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8c95f-192">To view entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url [-Entry <URLValue>] [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="8c95f-193">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="8c95f-193">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Action Block
```

<span data-ttu-id="8c95f-194">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="8c95f-194">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-195">Utiliser PowerShell pour modifier des entrées dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-195">Use PowerShell to modify entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="8c95f-196">Vous ne pouvez pas modifier la valeur de l’URL proprement dite.</span><span class="sxs-lookup"><span data-stu-id="8c95f-196">You can't modify the URL value itself.</span></span> <span data-ttu-id="8c95f-197">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="8c95f-197">Instead, you need to delete the entry and recreate it.</span></span>

<span data-ttu-id="8c95f-198">Pour modifier les entrées de la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8c95f-198">To modify entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids <"Id1","Id2",..."IdN"> [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="8c95f-199">Cet exemple montre comment modifier la date d’expiration de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8c95f-199">This example changes the expiration date of the specified entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="8c95f-200">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="8c95f-200">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-201">Utiliser PowerShell pour supprimer des entrées de la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-201">Use PowerShell to remove entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="8c95f-202">Pour supprimer des entrées de la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8c95f-202">To remove entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="8c95f-203">Cet exemple supprime l’entrée d’URL spécifiée de la liste des clients bloqués/bloqués.</span><span class="sxs-lookup"><span data-stu-id="8c95f-203">This example removes the specified URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="8c95f-204">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="8c95f-204">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="8c95f-205">Syntaxe d’URL de la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="8c95f-205">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="8c95f-206">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="8c95f-206">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="8c95f-207">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="8c95f-207">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="8c95f-208">Unicode n’est pas pris en charge, mais Punycode est.</span><span class="sxs-lookup"><span data-stu-id="8c95f-208">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="8c95f-209">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="8c95f-209">Hostnames are allowed if all of the following statements are true:</span></span>

  - <span data-ttu-id="8c95f-210">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="8c95f-210">The hostname contains a period.</span></span>
  - <span data-ttu-id="8c95f-211">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="8c95f-211">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="8c95f-212">Il y a au moins deux caractères à droite de la période.</span><span class="sxs-lookup"><span data-stu-id="8c95f-212">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="8c95f-213">Par exemple, `t.co` est autorisé ou n’est `.com` `contoso.` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="8c95f-213">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="8c95f-214">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="8c95f-214">Subpaths are not implied.</span></span>

  <span data-ttu-id="8c95f-215">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="8c95f-215">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="8c95f-216">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-216">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="8c95f-217">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="8c95f-217">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="8c95f-218">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="8c95f-218">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="8c95f-219">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8c95f-219">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="8c95f-220">Par exemple, `contoso.com/*` est autorisé ou n’est `contoso.com*` `contoso.com/ab*` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="8c95f-220">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="8c95f-221">Tous les sous-chemins ne sont pas implicitement par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="8c95f-221">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="8c95f-222">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="8c95f-222">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="8c95f-223">`*.com*` n’est pas valide (ce n’est pas un domaine pouvant être résolu et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="8c95f-223">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="8c95f-224">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="8c95f-224">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="8c95f-225">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="8c95f-225">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="8c95f-226">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="8c95f-226">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="8c95f-227">Par exemple `~contoso.com` `contoso.com` , inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="8c95f-227">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="8c95f-228">Les entrées d’URL qui contiennent des protocoles (par exemple,, `http://` `https://` ou `ftp://` ) échouent, car les entrées d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="8c95f-228">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="8c95f-229">Un nom d’utilisateur ou un mot de passe n’est pas pris en charge ou obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8c95f-229">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="8c95f-230">Les guillemets ('ou ") sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="8c95f-230">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="8c95f-231">Une URL doit inclure toutes les redirections, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8c95f-231">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="8c95f-232">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="8c95f-232">URL entry scenarios</span></span>

<span data-ttu-id="8c95f-233">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c95f-233">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="8c95f-234">Scénario : pas de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="8c95f-234">Scenario: No wildcards</span></span>

<span data-ttu-id="8c95f-235">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="8c95f-235">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="8c95f-236">**Correspondance autorisée**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-236">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="8c95f-237">**Ne pas faire correspondre**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-237">**Allow not matched**:</span></span>

  - <span data-ttu-id="8c95f-238">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-238">abc-contoso.com</span></span>
  - <span data-ttu-id="8c95f-239">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-239">contoso.com/a</span></span>
  - <span data-ttu-id="8c95f-240">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-240">payroll.contoso.com</span></span>
  - <span data-ttu-id="8c95f-241">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-241">test.com/contoso.com</span></span>
  - <span data-ttu-id="8c95f-242">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-242">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="8c95f-243">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-243">www.contoso.com</span></span>
  - <span data-ttu-id="8c95f-244">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-244">www.contoso.com/q=a@contoso.com</span></span>
  
- <span data-ttu-id="8c95f-245">**Correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-245">**Block match**:</span></span>

  - <span data-ttu-id="8c95f-246">contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-246">contoso.com</span></span>
  - <span data-ttu-id="8c95f-247">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-247">contoso.com/a</span></span>
  - <span data-ttu-id="8c95f-248">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-248">payroll.contoso.com</span></span>
  - <span data-ttu-id="8c95f-249">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-249">test.com/contoso.com</span></span>
  - <span data-ttu-id="8c95f-250">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-250">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="8c95f-251">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-251">www.contoso.com</span></span>
  - <span data-ttu-id="8c95f-252">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-252">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="8c95f-253">**Bloc sans correspondance**: ABC-contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-253">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="8c95f-254">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="8c95f-254">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="8c95f-255">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="8c95f-255">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="8c95f-256">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-256">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-257">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-257">www.contoso.com</span></span>
  - <span data-ttu-id="8c95f-258">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-258">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="8c95f-259">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-259">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="8c95f-260">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-260">123contoso.com</span></span>
  - <span data-ttu-id="8c95f-261">contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-261">contoso.com</span></span>
  - <span data-ttu-id="8c95f-262">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-262">test.com/contoso.com</span></span>
  - <span data-ttu-id="8c95f-263">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="8c95f-263">www.contoso.com/abc</span></span>
  
#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="8c95f-264">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8c95f-264">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="8c95f-265">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="8c95f-265">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="8c95f-266">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-266">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-267">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="8c95f-267">contoso.com/a/b</span></span>
  - <span data-ttu-id="8c95f-268">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="8c95f-268">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="8c95f-269">contoso. com/a/ ? q = joe@t. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-269">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="8c95f-270">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-270">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="8c95f-271">contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-271">contoso.com</span></span>
  - <span data-ttu-id="8c95f-272">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-272">contoso.com/a</span></span>
  - <span data-ttu-id="8c95f-273">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-273">www.contoso.com</span></span>
  - <span data-ttu-id="8c95f-274">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-274">www.contoso.com/q=a@contoso.com</span></span>
  
#### <a name="scenario-left-tilde"></a><span data-ttu-id="8c95f-275">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="8c95f-275">Scenario: Left tilde</span></span>

<span data-ttu-id="8c95f-276">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="8c95f-276">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="8c95f-277">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-277">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-278">contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-278">contoso.com</span></span>
  - <span data-ttu-id="8c95f-279">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-279">www.contoso.com</span></span>
  - <span data-ttu-id="8c95f-280">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-280">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="8c95f-281">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-281">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="8c95f-282">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-282">123contoso.com</span></span>
  - <span data-ttu-id="8c95f-283">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="8c95f-283">contoso.com/abc</span></span>
  - <span data-ttu-id="8c95f-284">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="8c95f-284">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="8c95f-285">Scénario : suffixe de caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="8c95f-285">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="8c95f-286">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="8c95f-286">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="8c95f-287">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-287">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-288">contoso. com/ ? q = whatever@fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-288">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="8c95f-289">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-289">contoso.com/a</span></span>
  - <span data-ttu-id="8c95f-290">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="8c95f-290">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="8c95f-291">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="8c95f-291">contoso.com/ab</span></span>
  - <span data-ttu-id="8c95f-292">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="8c95f-292">contoso.com/b</span></span>
  - <span data-ttu-id="8c95f-293">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="8c95f-293">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="8c95f-294">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="8c95f-294">contoso.com/ba</span></span>

- <span data-ttu-id="8c95f-295">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-295">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="8c95f-296">Scénario : sous-domaine du caractère générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="8c95f-296">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="8c95f-297">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="8c95f-297">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="8c95f-298">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-298">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-299">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="8c95f-299">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="8c95f-300">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="8c95f-300">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="8c95f-301">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-301">www.contoso.com/a</span></span>
  - <span data-ttu-id="8c95f-302">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="8c95f-302">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="8c95f-303">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="8c95f-303">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="8c95f-304">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="8c95f-304">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="8c95f-305">Scénario : tilde gauche et droit</span><span class="sxs-lookup"><span data-stu-id="8c95f-305">Scenario: Left and right tilde</span></span>

<span data-ttu-id="8c95f-306">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="8c95f-306">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="8c95f-307">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-307">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-308">contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-308">contoso.com</span></span>
  - <span data-ttu-id="8c95f-309">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-309">contoso.com/a</span></span>
  - <span data-ttu-id="8c95f-310">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-310">www.contoso.com</span></span>
  - <span data-ttu-id="8c95f-311">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="8c95f-311">www.contoso.com/b</span></span>
  - <span data-ttu-id="8c95f-312">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-312">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="8c95f-313">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-313">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="8c95f-314">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-314">123contoso.com</span></span>
  - <span data-ttu-id="8c95f-315">contoso.org</span><span class="sxs-lookup"><span data-stu-id="8c95f-315">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="8c95f-316">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="8c95f-316">Scenario: IP address</span></span>

<span data-ttu-id="8c95f-317">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="8c95f-317">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="8c95f-318">**Autoriser la correspondance** et la **correspondance de bloc**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="8c95f-318">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="8c95f-319">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-319">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="8c95f-320">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-320">1.2.3.4/a</span></span>
  - <span data-ttu-id="8c95f-321">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="8c95f-321">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="8c95f-322">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="8c95f-322">IP address with right wildcard</span></span>

<span data-ttu-id="8c95f-323">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="8c95f-323">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="8c95f-324">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-324">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="8c95f-325">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="8c95f-325">1.2.3.4/b</span></span>
  - <span data-ttu-id="8c95f-326">1.2.3.4/bAAAA</span><span class="sxs-lookup"><span data-stu-id="8c95f-326">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="8c95f-327">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="8c95f-327">Examples of invalid entries</span></span>

<span data-ttu-id="8c95f-328">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="8c95f-328">The following entries are invalid:</span></span>

- <span data-ttu-id="8c95f-329">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-329">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="8c95f-330">contoso</span><span class="sxs-lookup"><span data-stu-id="8c95f-330">contoso</span></span>
  - <span data-ttu-id="8c95f-331">\*contoso.\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-331">\*.contoso.\*</span></span>
  - <span data-ttu-id="8c95f-332">\*. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-332">\*.com</span></span>
  - <span data-ttu-id="8c95f-333">\*. pdf</span><span class="sxs-lookup"><span data-stu-id="8c95f-333">\*.pdf</span></span>

- <span data-ttu-id="8c95f-334">**Caractères génériques sur le texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-334">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="8c95f-335">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-335">\*contoso.com</span></span>
  - <span data-ttu-id="8c95f-336">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-336">contoso.com\*</span></span>
  - <span data-ttu-id="8c95f-337">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="8c95f-337">\*1.2.3.4</span></span>
  - <span data-ttu-id="8c95f-338">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-338">1.2.3.4\*</span></span>
  - <span data-ttu-id="8c95f-339">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-339">contoso.com/a\*</span></span>
  - <span data-ttu-id="8c95f-340">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-340">contoso.com/ab\*</span></span>

- <span data-ttu-id="8c95f-341">**Adresses IP avec des ports**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-341">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="8c95f-342">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="8c95f-342">contoso.com:443</span></span>
  - <span data-ttu-id="8c95f-343">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="8c95f-343">abc.contoso.com:25</span></span>

- <span data-ttu-id="8c95f-344">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-344">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="8c95f-345">\*.\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-345">\*.\*</span></span>

- <span data-ttu-id="8c95f-346">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="8c95f-346">**Middle wildcards**:</span></span>

  - <span data-ttu-id="8c95f-347">CONT \* so.com</span><span class="sxs-lookup"><span data-stu-id="8c95f-347">conto\*so.com</span></span>
  - <span data-ttu-id="8c95f-348">Conto ~ so. com</span><span class="sxs-lookup"><span data-stu-id="8c95f-348">conto~so.com</span></span>

- <span data-ttu-id="8c95f-349">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="8c95f-349">**Double wildcards**</span></span>

  - <span data-ttu-id="8c95f-350">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-350">contoso.com/\*\*</span></span>
  - <span data-ttu-id="8c95f-351">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="8c95f-351">contoso.com/\*/\*</span></span>
