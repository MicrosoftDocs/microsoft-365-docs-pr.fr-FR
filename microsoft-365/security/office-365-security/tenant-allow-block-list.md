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
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à configurer des autoriser et des blocs dans la liste d’adresses client autoriser/bloquer dans le portail de sécurité.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 103ddc9aa0858f9203582ac07a655fd7f5506cf3
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587586"
---
# <a name="manage-the-tenant-allowblock-list"></a><span data-ttu-id="952df-103">Gérer la liste Autoriser/Bloquer du client</span><span class="sxs-lookup"><span data-stu-id="952df-103">Manage the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="952df-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="952df-104">**Applies to**</span></span>
- [<span data-ttu-id="952df-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="952df-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="952df-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="952df-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="952df-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="952df-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="952df-108">Vous ne pouvez pas **configurer les éléments** autorisés dans la liste des locataires autorisés/bloqués pour le moment.</span><span class="sxs-lookup"><span data-stu-id="952df-108">You can't **configure** allowed items in the Tenant Allow/Block List at this time.</span></span>

<span data-ttu-id="952df-109">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, vous pouvez ne pas être d’accord avec le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="952df-109">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="952df-110">Par exemple, un bon message peut être marqué comme mauvais (faux positif) ou un message erroné peut être autorisé (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="952df-110">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="952df-111">La liste d’attente des clients dans le Centre de sécurité & conformité vous permet de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="952df-111">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="952df-112">La liste d’adresses client autoriser/bloquer est utilisée pendant le flux de messagerie et au moment des clics de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="952df-112">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="952df-113">Vous pouvez spécifier des URL ou des fichiers à toujours bloquer.</span><span class="sxs-lookup"><span data-stu-id="952df-113">You can specify URLs or files to always block.</span></span>

<span data-ttu-id="952df-114">Cet article explique comment configurer des entrées dans la liste d’adresses client autoriser/bloquer dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="952df-114">This article describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="952df-115">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="952df-115">What do you need to know before you begin?</span></span>

- <span data-ttu-id="952df-116">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="952df-116">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="952df-117">Pour aller directement à la page **Autoriser/Bloquer la liste des** locataires, utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="952df-117">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="952df-118">Vous spécifiez des fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="952df-118">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="952df-119">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="952df-119">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```console
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="952df-120">Un exemple de valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="952df-120">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="952df-121">Les valeurs de hachage perceptif (pHash) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="952df-121">Perceptual hash (pHash) values are not supported.</span></span>

- <span data-ttu-id="952df-122">Les valeurs d’URL disponibles sont décrites dans la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) de la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="952df-122">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

- <span data-ttu-id="952df-123">La liste d’adresses client autorise un maximum de 500 entrées pour les URL et 500 entrées pour les hâchés de fichiers.</span><span class="sxs-lookup"><span data-stu-id="952df-123">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="952df-124">Le nombre maximal de caractères pour chaque entrée est :</span><span class="sxs-lookup"><span data-stu-id="952df-124">The maximum number of characters for each entry is:</span></span>
  - <span data-ttu-id="952df-125">Hèmes de fichier = 64</span><span class="sxs-lookup"><span data-stu-id="952df-125">File hashes = 64</span></span>
  - <span data-ttu-id="952df-126">URL = 250</span><span class="sxs-lookup"><span data-stu-id="952df-126">URL = 250</span></span>

- <span data-ttu-id="952df-127">Une entrée doit être active dans les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="952df-127">An entry should be active within 30 minutes.</span></span>

- <span data-ttu-id="952df-128">Par défaut, les entrées de la liste d’inscriptions au client sont expirées au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="952df-128">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="952df-129">Vous pouvez spécifier une date ou la définir pour qu’elles n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="952df-129">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="952df-130">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="952df-130">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="952df-131">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="952df-131">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="952df-132">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="952df-132">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="952df-133">Pour ajouter et supprimer des valeurs de la liste d’attente des locataires, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="952df-133">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="952df-134">Pour un accès en lecture seule à la liste des locataires  autorisé/bloqué, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="952df-134">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="952df-135">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="952df-135">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  > 
  > - <span data-ttu-id="952df-136">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="952df-136">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="952df-137">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="952df-137">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  > - <span data-ttu-id="952df-138">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="952df-138">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="952df-139">Utiliser le Centre de sécurité & conformité pour créer des entrées d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="952df-139">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="952df-140">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) pour la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="952df-140">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

1. <span data-ttu-id="952df-141">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="952df-141">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="952df-142">Dans la page **Liste d’adresses** client autoriser/bloquer, vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Bloquer**</span><span class="sxs-lookup"><span data-stu-id="952df-142">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Block**</span></span>

3. <span data-ttu-id="952df-143">Dans le **volant Bloquer les URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="952df-143">In the **Block URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="952df-144">**Ajouter des URL à bloquer :** entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="952df-144">**Add URLs to block**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="952df-145">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="952df-145">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="952df-146">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="952df-146">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

       <span data-ttu-id="952df-147">ou</span><span class="sxs-lookup"><span data-stu-id="952df-147">or</span></span>

     - <span data-ttu-id="952df-148">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="952df-148">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="952df-150">.</span><span class="sxs-lookup"><span data-stu-id="952df-150">.</span></span>

   - <span data-ttu-id="952df-151">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="952df-151">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="952df-152">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="952df-152">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="952df-153">Utiliser le Centre de sécurité & conformité pour créer des entrées de fichier dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="952df-153">Use the Security & Compliance Center to create file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="952df-154">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="952df-154">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="952df-155">Dans la page **Liste des clients autoriser/bloquer,** sélectionnez **l’onglet Fichiers,** puis cliquez sur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="952df-155">On the **Tenant Allow/Block List** page, select **Files** tab, and then click **Block**.</span></span>

3. <span data-ttu-id="952df-156">Dans la **zone Ajouter des fichiers pour bloquer** le flyout qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="952df-156">In the **Add files to block** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="952df-157">**Ajouter des hachages de fichier**: entrez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="952df-157">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="952df-158">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="952df-158">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="952df-159">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="952df-159">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="952df-160">ou</span><span class="sxs-lookup"><span data-stu-id="952df-160">or</span></span>

     - <span data-ttu-id="952df-161">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="952df-161">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="952df-163">.</span><span class="sxs-lookup"><span data-stu-id="952df-163">.</span></span>

   - <span data-ttu-id="952df-164">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="952df-164">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="952df-165">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="952df-165">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="952df-166">Utiliser le Centre de sécurité & conformité pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="952df-166">Use the Security & Compliance Center to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="952df-167">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="952df-167">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="952df-168">Sélectionnez **l’onglet URL** ou **Fichiers.**</span><span class="sxs-lookup"><span data-stu-id="952df-168">Select the **URLs** tab or the **Files** tab.</span></span>

<span data-ttu-id="952df-169">Cliquez sur les en-tête de colonne suivants pour trier par ordre croissant ou décroit :</span><span class="sxs-lookup"><span data-stu-id="952df-169">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="952df-170">**Valeur**: URL ou hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="952df-170">**Value**: The URL or the file hash.</span></span>
- <span data-ttu-id="952df-171">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="952df-171">**Last updated date**</span></span>
- <span data-ttu-id="952df-172">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="952df-172">**Expiration date**</span></span>
- <span data-ttu-id="952df-173">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="952df-173">**Note**</span></span>

<span data-ttu-id="952df-174">Cliquez **sur** Rechercher, entrez une partie ou l’ensemble d’une valeur, puis appuyez sur Entrée pour trouver une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="952df-174">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="952df-175">Lorsque vous avez terminé, cliquez sur **Effacer l’icône** ![ effacer la ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) recherche.</span><span class="sxs-lookup"><span data-stu-id="952df-175">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="952df-176">Cliquez sur **Filtrer.**</span><span class="sxs-lookup"><span data-stu-id="952df-176">Click **Filter**.</span></span> <span data-ttu-id="952df-177">Dans le **volant de** filtre qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="952df-177">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="952df-178">**N’expirez** jamais : sélectionnez Off: ![ Toggle off ](../../media/scc-toggle-off.png) or on: ![ Toggle on ](../../media/scc-toggle-on.png) .</span><span class="sxs-lookup"><span data-stu-id="952df-178">**Never expire**: Select off: ![Toggle off](../../media/scc-toggle-off.png) or on: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

- <span data-ttu-id="952df-179">**Dernière mise à jour**: sélectionnez une date de début (**De**), une date de fin (**À**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="952df-179">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="952df-180">**Date d’expiration**: sélectionnez une date de début (**De**), une date de fin (**À**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="952df-180">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="952df-181">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="952df-181">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="952df-182">Pour effacer les filtres existants,  cliquez sur **Filtrer** et dans le volant de filtre qui s’affiche, cliquez **sur Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="952df-182">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-block-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="952df-183">Utiliser le Centre de sécurité & conformité pour modifier les entrées de blocage dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="952df-183">Use the Security & Compliance Center to modify block entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="952df-184">Vous ne pouvez pas modifier l’URL ou les valeurs de fichier bloquées existantes dans une entrée.</span><span class="sxs-lookup"><span data-stu-id="952df-184">You can't modify the existing blocked URL or file values within an entry.</span></span> <span data-ttu-id="952df-185">Pour modifier ces valeurs, vous devez supprimer et recréer l’entrée.</span><span class="sxs-lookup"><span data-stu-id="952df-185">To modify these values, you need to delete and recreate the entry.</span></span>

1. <span data-ttu-id="952df-186">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="952df-186">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="952df-187">Sélectionnez **l’onglet URL** ou **Fichiers.**</span><span class="sxs-lookup"><span data-stu-id="952df-187">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="952df-188">Sélectionnez l’entrée de blocage à modifier, puis cliquez **sur** Modifier ![ l’icône ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="952df-188">Select the block entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="952df-189">Dans le volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="952df-189">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="952df-190">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="952df-190">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="952df-191">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration de l’entrée. </span><span class="sxs-lookup"><span data-stu-id="952df-191">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

       <span data-ttu-id="952df-192">ou</span><span class="sxs-lookup"><span data-stu-id="952df-192">or</span></span>

     - <span data-ttu-id="952df-193">Déplacez le basculement vers la droite pour configurer l’entrée pour qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="952df-193">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="952df-195">.</span><span class="sxs-lookup"><span data-stu-id="952df-195">.</span></span>

   - <span data-ttu-id="952df-196">**Remarque facultative**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="952df-196">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="952df-197">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="952df-197">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-block-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="952df-198">Utiliser le Centre de sécurité & conformité pour supprimer des entrées de blocage de la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="952df-198">Use the Security & Compliance Center to remove block entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="952df-199">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="952df-199">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="952df-200">Sélectionnez **l’onglet URL** ou **Fichiers.**</span><span class="sxs-lookup"><span data-stu-id="952df-200">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="952df-201">Sélectionnez l’entrée de blocage à supprimer, puis cliquez **sur** Supprimer ![ l’icône ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="952df-201">Select the block entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="952df-202">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="952df-202">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="952df-203">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="952df-203">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-block-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="952df-204">Utiliser PowerShell pour ajouter des entrées de bloc à la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="952df-204">Use PowerShell to add block entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="952df-205">Pour ajouter des entrées de bloc dans la liste d’attente des locataires, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="952df-205">To add block entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <Url | FileHash> -Block -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="952df-206">Cet exemple ajoute une entrée d’URL de bloc pour contoso.com et tous les sous-contoso.com (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="952df-206">This example adds a block URL entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="952df-207">Étant donné que nous n’avons pas utilisé les paramètres ExpirationDate ou NoExpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="952df-207">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Block -Entries ~contoso.com
```

<span data-ttu-id="952df-208">Cet exemple ajoute une entrée de bloc de fichiers pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="952df-208">This example adds a block file entry for the specified files that never expires.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType FileHash -Block -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="952df-209">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="952df-209">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="952df-210">Utiliser PowerShell pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="952df-210">Use PowerShell to view entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="952df-211">Pour afficher les entrées de la liste d’inscriptions client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="952df-211">To view entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <Url | FileHash> [-Entry <URLValue | FileHashValue>] [-Block] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="952df-212">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="952df-212">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Block
```

<span data-ttu-id="952df-213">Cet exemple renvoie des informations pour la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="952df-213">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="952df-214">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="952df-214">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-block-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="952df-215">Utiliser PowerShell pour modifier les entrées de bloc dans la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="952df-215">Use PowerShell to modify block entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="952df-216">Vous ne pouvez pas modifier l’URL ou les valeurs de fichier existantes dans une entrée de bloc.</span><span class="sxs-lookup"><span data-stu-id="952df-216">You can't modify the existing URL or file values within a block entry.</span></span> <span data-ttu-id="952df-217">Pour modifier ces valeurs, vous devez supprimer et recréer l’entrée.</span><span class="sxs-lookup"><span data-stu-id="952df-217">To modify these values, you need to delete and recreate the entry.</span></span>

<span data-ttu-id="952df-218">Pour modifier les entrées de bloc dans la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="952df-218">To modify block entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN"> [-Block] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="952df-219">Cet exemple modifie la date d’expiration de l’entrée de bloc spécifiée.</span><span class="sxs-lookup"><span data-stu-id="952df-219">This example changes the expiration date of the specified block entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="952df-220">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="952df-220">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-block-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="952df-221">Utiliser PowerShell pour supprimer des entrées de blocage de la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="952df-221">Use PowerShell to remove block entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="952df-222">Pour supprimer des entrées de blocage de la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="952df-222">To remove block entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="952df-223">Cet exemple supprime l’entrée d’URL de bloc spécifiée de la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="952df-223">This example removes the specified block URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="952df-224">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="952df-224">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="952df-225">Syntaxe d’URL pour la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="952df-225">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="952df-226">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="952df-226">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="952df-227">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="952df-227">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="952df-228">Unicode n’est pas pris en charge, mais c’est le cas de Punycode.</span><span class="sxs-lookup"><span data-stu-id="952df-228">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="952df-229">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="952df-229">Hostnames are allowed if all of the following statements are true:</span></span>
  - <span data-ttu-id="952df-230">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="952df-230">The hostname contains a period.</span></span>
  - <span data-ttu-id="952df-231">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="952df-231">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="952df-232">Il y a au moins deux caractères à droite du point.</span><span class="sxs-lookup"><span data-stu-id="952df-232">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="952df-233">Par exemple, `t.co` est autorisé ou `.com` `contoso.` non.</span><span class="sxs-lookup"><span data-stu-id="952df-233">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="952df-234">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="952df-234">Subpaths are not implied.</span></span>

  <span data-ttu-id="952df-235">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="952df-235">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="952df-236">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="952df-236">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="952df-237">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="952df-237">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="952df-238">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="952df-238">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="952df-239">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="952df-239">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="952df-240">Par exemple, `contoso.com/*` est autorisé ou `contoso.com*` `contoso.com/ab*` non.</span><span class="sxs-lookup"><span data-stu-id="952df-240">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="952df-241">Tous les sous-chemins ne sont pas impliqués par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="952df-241">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="952df-242">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="952df-242">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="952df-243">`*.com*` n’est pas valide (domaine non résolvable et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="952df-243">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="952df-244">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="952df-244">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="952df-245">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="952df-245">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="952df-246">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="952df-246">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="952df-247">Par `~contoso.com` exemple, `contoso.com` inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="952df-247">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="952df-248">Les entrées d’URL qui contiennent des protocoles (par exemple, , ou ) échouent, car les entrées `http://` `https://` `ftp://` d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="952df-248">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="952df-249">Un nom d’utilisateur ou un mot de passe ne sont pas pris en charge ou requis.</span><span class="sxs-lookup"><span data-stu-id="952df-249">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="952df-250">Les guillemets (' ou « ) sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="952df-250">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="952df-251">Une URL doit inclure toutes les redirections lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="952df-251">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="952df-252">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="952df-252">URL entry scenarios</span></span>

<span data-ttu-id="952df-253">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="952df-253">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="952df-254">Scénario : aucun caractère générique</span><span class="sxs-lookup"><span data-stu-id="952df-254">Scenario: No wildcards</span></span>

<span data-ttu-id="952df-255">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="952df-255">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="952df-256">**Autoriser la correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-256">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="952df-257">**Autoriser non la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-257">**Allow not matched**:</span></span>

  - <span data-ttu-id="952df-258">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-258">abc-contoso.com</span></span>
  - <span data-ttu-id="952df-259">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="952df-259">contoso.com/a</span></span>
  - <span data-ttu-id="952df-260">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-260">payroll.contoso.com</span></span>
  - <span data-ttu-id="952df-261">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-261">test.com/contoso.com</span></span>
  - <span data-ttu-id="952df-262">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-262">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="952df-263">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-263">www.contoso.com</span></span>
  - <span data-ttu-id="952df-264">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-264">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="952df-265">**Bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-265">**Block match**:</span></span>

  - <span data-ttu-id="952df-266">contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-266">contoso.com</span></span>
  - <span data-ttu-id="952df-267">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="952df-267">contoso.com/a</span></span>
  - <span data-ttu-id="952df-268">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-268">payroll.contoso.com</span></span>
  - <span data-ttu-id="952df-269">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-269">test.com/contoso.com</span></span>
  - <span data-ttu-id="952df-270">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-270">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="952df-271">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-271">www.contoso.com</span></span>
  - <span data-ttu-id="952df-272">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-272">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="952df-273">**Bloc non correspond :** abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-273">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="952df-274">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="952df-274">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="952df-275">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="952df-275">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="952df-276">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-276">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-277">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-277">www.contoso.com</span></span>
  - <span data-ttu-id="952df-278">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-278">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="952df-279">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="952df-279">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="952df-280">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-280">123contoso.com</span></span>
  - <span data-ttu-id="952df-281">contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-281">contoso.com</span></span>
  - <span data-ttu-id="952df-282">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-282">test.com/contoso.com</span></span>
  - <span data-ttu-id="952df-283">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="952df-283">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="952df-284">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="952df-284">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="952df-285">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="952df-285">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="952df-286">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-286">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-287">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="952df-287">contoso.com/a/b</span></span>
  - <span data-ttu-id="952df-288">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="952df-288">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="952df-289">contoso.com/a/?q=joe@t.com</span><span class="sxs-lookup"><span data-stu-id="952df-289">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="952df-290">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="952df-290">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="952df-291">contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-291">contoso.com</span></span>
  - <span data-ttu-id="952df-292">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="952df-292">contoso.com/a</span></span>
  - <span data-ttu-id="952df-293">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-293">www.contoso.com</span></span>
  - <span data-ttu-id="952df-294">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-294">www.contoso.com/q=a@contoso.com</span></span>

#### <a name="scenario-left-tilde"></a><span data-ttu-id="952df-295">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="952df-295">Scenario: Left tilde</span></span>

<span data-ttu-id="952df-296">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="952df-296">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="952df-297">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-297">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-298">contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-298">contoso.com</span></span>
  - <span data-ttu-id="952df-299">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-299">www.contoso.com</span></span>
  - <span data-ttu-id="952df-300">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-300">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="952df-301">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="952df-301">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="952df-302">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-302">123contoso.com</span></span>
  - <span data-ttu-id="952df-303">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="952df-303">contoso.com/abc</span></span>
  - <span data-ttu-id="952df-304">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="952df-304">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="952df-305">Scénario : suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="952df-305">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="952df-306">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="952df-306">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="952df-307">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-307">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-308">contoso.com/?q=whatever@fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="952df-308">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="952df-309">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="952df-309">contoso.com/a</span></span>
  - <span data-ttu-id="952df-310">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="952df-310">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="952df-311">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="952df-311">contoso.com/ab</span></span>
  - <span data-ttu-id="952df-312">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="952df-312">contoso.com/b</span></span>
  - <span data-ttu-id="952df-313">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="952df-313">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="952df-314">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="952df-314">contoso.com/ba</span></span>

- <span data-ttu-id="952df-315">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-315">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="952df-316">Scénario : sous-domaine générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="952df-316">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="952df-317">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="952df-317">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="952df-318">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-318">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-319">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="952df-319">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="952df-320">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="952df-320">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="952df-321">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="952df-321">www.contoso.com/a</span></span>
  - <span data-ttu-id="952df-322">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="952df-322">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="952df-323">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="952df-323">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="952df-324">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="952df-324">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="952df-325">Scénario : tilde gauche et droite</span><span class="sxs-lookup"><span data-stu-id="952df-325">Scenario: Left and right tilde</span></span>

<span data-ttu-id="952df-326">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="952df-326">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="952df-327">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-327">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-328">contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-328">contoso.com</span></span>
  - <span data-ttu-id="952df-329">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="952df-329">contoso.com/a</span></span>
  - <span data-ttu-id="952df-330">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-330">www.contoso.com</span></span>
  - <span data-ttu-id="952df-331">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="952df-331">www.contoso.com/b</span></span>
  - <span data-ttu-id="952df-332">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-332">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="952df-333">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="952df-333">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="952df-334">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-334">123contoso.com</span></span>
  - <span data-ttu-id="952df-335">contoso.org</span><span class="sxs-lookup"><span data-stu-id="952df-335">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="952df-336">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="952df-336">Scenario: IP address</span></span>

<span data-ttu-id="952df-337">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="952df-337">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="952df-338">**Autoriser la correspondance** **et bloquer la correspondance**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="952df-338">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="952df-339">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="952df-339">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="952df-340">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="952df-340">1.2.3.4/a</span></span>
  - <span data-ttu-id="952df-341">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="952df-341">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="952df-342">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="952df-342">IP address with right wildcard</span></span>

<span data-ttu-id="952df-343">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="952df-343">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="952df-344">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="952df-344">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="952df-345">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="952df-345">1.2.3.4/b</span></span>
  - <span data-ttu-id="952df-346">1.2.3.4/baaaa</span><span class="sxs-lookup"><span data-stu-id="952df-346">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="952df-347">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="952df-347">Examples of invalid entries</span></span>

<span data-ttu-id="952df-348">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="952df-348">The following entries are invalid:</span></span>

- <span data-ttu-id="952df-349">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="952df-349">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="952df-350">contoso</span><span class="sxs-lookup"><span data-stu-id="952df-350">contoso</span></span>
  - <span data-ttu-id="952df-351">\*.contoso.\*</span><span class="sxs-lookup"><span data-stu-id="952df-351">\*.contoso.\*</span></span>
  - <span data-ttu-id="952df-352">\*.com</span><span class="sxs-lookup"><span data-stu-id="952df-352">\*.com</span></span>
  - <span data-ttu-id="952df-353">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="952df-353">\*.pdf</span></span>

- <span data-ttu-id="952df-354">**Caractère générique sur du texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="952df-354">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="952df-355">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="952df-355">\*contoso.com</span></span>
  - <span data-ttu-id="952df-356">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="952df-356">contoso.com\*</span></span>
  - <span data-ttu-id="952df-357">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="952df-357">\*1.2.3.4</span></span>
  - <span data-ttu-id="952df-358">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="952df-358">1.2.3.4\*</span></span>
  - <span data-ttu-id="952df-359">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="952df-359">contoso.com/a\*</span></span>
  - <span data-ttu-id="952df-360">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="952df-360">contoso.com/ab\*</span></span>

- <span data-ttu-id="952df-361">**Adresses IP avec ports**:</span><span class="sxs-lookup"><span data-stu-id="952df-361">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="952df-362">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="952df-362">contoso.com:443</span></span>
  - <span data-ttu-id="952df-363">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="952df-363">abc.contoso.com:25</span></span>

- <span data-ttu-id="952df-364">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="952df-364">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="952df-365">\*.\*</span><span class="sxs-lookup"><span data-stu-id="952df-365">\*.\*</span></span>

- <span data-ttu-id="952df-366">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="952df-366">**Middle wildcards**:</span></span>

  - <span data-ttu-id="952df-367">conto \* so.com</span><span class="sxs-lookup"><span data-stu-id="952df-367">conto\*so.com</span></span>
  - <span data-ttu-id="952df-368">conto~so.com</span><span class="sxs-lookup"><span data-stu-id="952df-368">conto~so.com</span></span>

- <span data-ttu-id="952df-369">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="952df-369">**Double wildcards**</span></span>

  - <span data-ttu-id="952df-370">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="952df-370">contoso.com/\*\*</span></span>
  - <span data-ttu-id="952df-371">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="952df-371">contoso.com/\*/\*</span></span>
