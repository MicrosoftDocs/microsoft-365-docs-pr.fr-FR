---
title: Gérer vos autoriser et bloquer dans la liste d’autoriser/bloquer des locataires
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
ms.openlocfilehash: 2f97308bfc3600e4e85f5ac92d951b12d9a50f24
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50928531"
---
# <a name="manage-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-103">Gérer la liste Autoriser/Bloquer du client</span><span class="sxs-lookup"><span data-stu-id="9663d-103">Manage the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="9663d-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9663d-104">**Applies to**</span></span>
- [<span data-ttu-id="9663d-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="9663d-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="9663d-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="9663d-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="9663d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9663d-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

> [!NOTE]
>
> <span data-ttu-id="9663d-108">Les fonctionnalités décrites dans cet article sont en prévisualisation, peuvent faire l’objet de changements et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="9663d-108">The features described in this article are in Preview, are subject to change, and are not available in all organizations.</span></span>
>
> <span data-ttu-id="9663d-109">Vous ne pouvez pas **configurer les éléments** autorisés dans la liste des locataires autorisés/bloqués pour le moment.</span><span class="sxs-lookup"><span data-stu-id="9663d-109">You can't **configure** allowed items in the Tenant Allow/Block List at this time.</span></span>

<span data-ttu-id="9663d-110">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, vous pouvez ne pas être d’accord avec le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="9663d-110">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="9663d-111">Par exemple, un bon message peut être marqué comme mauvais (faux positif) ou un message erroné peut être autorisé (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="9663d-111">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="9663d-112">La liste d’attente des clients dans le Centre de sécurité & conformité vous permet de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9663d-112">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="9663d-113">La liste d’adresses client autoriser/bloquer est utilisée pendant le flux de messagerie et au moment des clics de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9663d-113">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="9663d-114">Vous pouvez spécifier des URL ou des fichiers à toujours bloquer.</span><span class="sxs-lookup"><span data-stu-id="9663d-114">You can specify URLs or files to always block.</span></span>

<span data-ttu-id="9663d-115">Cet article explique comment configurer des entrées dans la liste d’adresses client autoriser/bloquer dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="9663d-115">This article describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9663d-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9663d-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9663d-117">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="9663d-117">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="9663d-118">Pour aller directement à la page **Autoriser/Bloquer la liste des** locataires, utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="9663d-118">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="9663d-119">Vous spécifiez des fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="9663d-119">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="9663d-120">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="9663d-120">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```console
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="9663d-121">Un exemple de valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="9663d-121">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="9663d-122">Les valeurs de hachage perceptif (pHash) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9663d-122">Perceptual hash (pHash) values are not supported.</span></span>

- <span data-ttu-id="9663d-123">Les valeurs d’URL disponibles sont décrites dans la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) de la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9663d-123">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

- <span data-ttu-id="9663d-124">La liste d’adresses client autorise un maximum de 500 entrées pour les URL et 500 entrées pour les hâchés de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9663d-124">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="9663d-125">Le nombre maximal de caractères pour chaque entrée est :</span><span class="sxs-lookup"><span data-stu-id="9663d-125">The maximum number of characters for each entry is:</span></span>
  - <span data-ttu-id="9663d-126">Hèmes de fichier = 64</span><span class="sxs-lookup"><span data-stu-id="9663d-126">File hashes = 64</span></span>
  - <span data-ttu-id="9663d-127">URL = 250</span><span class="sxs-lookup"><span data-stu-id="9663d-127">URL = 250</span></span>

- <span data-ttu-id="9663d-128">Une entrée doit être active dans les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="9663d-128">An entry should be active within 30 minutes.</span></span>

- <span data-ttu-id="9663d-129">Par défaut, les entrées de la liste d’inscriptions au client sont expirées au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="9663d-129">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="9663d-130">Vous pouvez spécifier une date ou la définir pour qu’elles n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="9663d-130">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="9663d-131">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="9663d-131">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="9663d-132">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="9663d-132">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="9663d-133">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="9663d-133">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="9663d-134">Pour ajouter et supprimer des valeurs de la liste d’attente des locataires, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="9663d-134">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="9663d-135">Pour un accès en lecture seule à la liste des locataires  autorisé/bloqué, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="9663d-135">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="9663d-136">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="9663d-136">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  > 
  > - <span data-ttu-id="9663d-137">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9663d-137">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="9663d-138">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9663d-138">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  > - <span data-ttu-id="9663d-139">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9663d-139">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-140">Utiliser le Centre de sécurité & conformité pour créer des entrées d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="9663d-140">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9663d-141">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) pour la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9663d-141">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

1. <span data-ttu-id="9663d-142">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9663d-142">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9663d-143">Dans la page **Liste d’adresses** client autoriser/bloquer, vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Bloquer**</span><span class="sxs-lookup"><span data-stu-id="9663d-143">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Block**</span></span>

3. <span data-ttu-id="9663d-144">Dans le **volant Bloquer les URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9663d-144">In the **Block URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9663d-145">**Ajouter des URL à bloquer :** entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="9663d-145">**Add URLs to block**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="9663d-146">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9663d-146">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9663d-147">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="9663d-147">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

       <span data-ttu-id="9663d-148">ou</span><span class="sxs-lookup"><span data-stu-id="9663d-148">or</span></span>

     - <span data-ttu-id="9663d-149">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="9663d-149">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="9663d-151">.</span><span class="sxs-lookup"><span data-stu-id="9663d-151">.</span></span>

   - <span data-ttu-id="9663d-152">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="9663d-152">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="9663d-153">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9663d-153">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-154">Utiliser le Centre de sécurité & conformité pour créer des entrées de fichier dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9663d-154">Use the Security & Compliance Center to create file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9663d-155">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9663d-155">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9663d-156">Dans la page **Liste des clients autoriser/bloquer,** sélectionnez **l’onglet Fichiers,** puis cliquez sur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="9663d-156">On the **Tenant Allow/Block List** page, select **Files** tab, and then click **Block**.</span></span>

3. <span data-ttu-id="9663d-157">Dans la **zone Ajouter des fichiers pour bloquer** le flyout qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9663d-157">In the **Add files to block** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9663d-158">**Ajouter des hachages de fichier**: entrez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="9663d-158">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="9663d-159">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9663d-159">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9663d-160">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="9663d-160">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="9663d-161">ou</span><span class="sxs-lookup"><span data-stu-id="9663d-161">or</span></span>

     - <span data-ttu-id="9663d-162">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="9663d-162">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="9663d-164">.</span><span class="sxs-lookup"><span data-stu-id="9663d-164">.</span></span>

   - <span data-ttu-id="9663d-165">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="9663d-165">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="9663d-166">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9663d-166">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-167">Utiliser le Centre de sécurité & conformité pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9663d-167">Use the Security & Compliance Center to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9663d-168">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9663d-168">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9663d-169">Sélectionnez **l’onglet URL** ou **Fichiers.**</span><span class="sxs-lookup"><span data-stu-id="9663d-169">Select the **URLs** tab or the **Files** tab.</span></span>

<span data-ttu-id="9663d-170">Cliquez sur les en-tête de colonne suivants pour trier par ordre croissant ou décroit :</span><span class="sxs-lookup"><span data-stu-id="9663d-170">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="9663d-171">**Valeur**: URL ou hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="9663d-171">**Value**: The URL or the file hash.</span></span>
- <span data-ttu-id="9663d-172">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="9663d-172">**Last updated date**</span></span>
- <span data-ttu-id="9663d-173">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="9663d-173">**Expiration date**</span></span>
- <span data-ttu-id="9663d-174">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="9663d-174">**Note**</span></span>

<span data-ttu-id="9663d-175">Cliquez **sur** Rechercher, entrez une partie ou l’ensemble d’une valeur, puis appuyez sur Entrée pour trouver une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="9663d-175">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="9663d-176">Lorsque vous avez terminé, cliquez sur **Effacer l’icône** ![ effacer la ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) recherche.</span><span class="sxs-lookup"><span data-stu-id="9663d-176">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="9663d-177">Cliquez sur **Filtrer.**</span><span class="sxs-lookup"><span data-stu-id="9663d-177">Click **Filter**.</span></span> <span data-ttu-id="9663d-178">Dans le **volant de** filtre qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9663d-178">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="9663d-179">**N’expirez** jamais : sélectionnez Off: ![ Toggle off ](../../media/scc-toggle-off.png) or on: ![ Toggle on ](../../media/scc-toggle-on.png) .</span><span class="sxs-lookup"><span data-stu-id="9663d-179">**Never expire**: Select off: ![Toggle off](../../media/scc-toggle-off.png) or on: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

- <span data-ttu-id="9663d-180">**Dernière mise à jour**: sélectionnez une date de début (**De**), une date de fin (**À**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9663d-180">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="9663d-181">**Date d’expiration**: sélectionnez une date de début (**De**), une date de fin (**À**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9663d-181">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="9663d-182">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="9663d-182">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="9663d-183">Pour effacer les filtres existants,  cliquez sur **Filtrer** et dans le volant de filtre qui s’affiche, cliquez **sur Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="9663d-183">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-block-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-184">Utiliser le Centre de sécurité & conformité pour modifier les entrées de blocage dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9663d-184">Use the Security & Compliance Center to modify block entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9663d-185">Vous ne pouvez pas modifier l’URL ou les valeurs de fichier bloquées existantes dans une entrée.</span><span class="sxs-lookup"><span data-stu-id="9663d-185">You can't modify the existing blocked URL or file values within an entry.</span></span> <span data-ttu-id="9663d-186">Pour modifier ces valeurs, vous devez supprimer et recréer l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9663d-186">To modify these values, you need to delete and recreate the entry.</span></span>

1. <span data-ttu-id="9663d-187">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9663d-187">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9663d-188">Sélectionnez **l’onglet URL** ou **Fichiers.**</span><span class="sxs-lookup"><span data-stu-id="9663d-188">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="9663d-189">Sélectionnez l’entrée de blocage à modifier, puis cliquez **sur** Modifier ![ l’icône ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="9663d-189">Select the block entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="9663d-190">Dans le volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9663d-190">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9663d-191">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9663d-191">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9663d-192">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration de l’entrée. </span><span class="sxs-lookup"><span data-stu-id="9663d-192">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

       <span data-ttu-id="9663d-193">ou</span><span class="sxs-lookup"><span data-stu-id="9663d-193">or</span></span>

     - <span data-ttu-id="9663d-194">Déplacez le basculement vers la droite pour configurer l’entrée de manière à ce qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="9663d-194">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="9663d-196">.</span><span class="sxs-lookup"><span data-stu-id="9663d-196">.</span></span>

   - <span data-ttu-id="9663d-197">**Remarque facultative**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9663d-197">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="9663d-198">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9663d-198">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-block-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-199">Utiliser le Centre de sécurité & conformité pour supprimer des entrées de blocage de la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9663d-199">Use the Security & Compliance Center to remove block entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9663d-200">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="9663d-200">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9663d-201">Sélectionnez **l’onglet URL** ou **Fichiers.**</span><span class="sxs-lookup"><span data-stu-id="9663d-201">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="9663d-202">Sélectionnez l’entrée de blocage à supprimer, puis cliquez **sur** Supprimer ![ l’icône ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="9663d-202">Select the block entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="9663d-203">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="9663d-203">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-204">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="9663d-204">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-block-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-205">Utiliser PowerShell pour ajouter des entrées de bloc à la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="9663d-205">Use PowerShell to add block entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="9663d-206">Pour ajouter des entrées de bloc dans la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9663d-206">To add block entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <Url | FileHash> -Block -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="9663d-207">Cet exemple ajoute une entrée d’URL de bloc pour contoso.com et tous les sous-contoso.com (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="9663d-207">This example adds a block URL entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="9663d-208">Étant donné que nous n’avons pas utilisé les paramètres ExpirationDate ou NoExpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="9663d-208">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Block -Entries ~contoso.com
```

<span data-ttu-id="9663d-209">Cet exemple ajoute une entrée de bloc de fichiers pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="9663d-209">This example adds a block file entry for the specified files that never expires.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType FileHash -Block -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="9663d-210">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9663d-210">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-211">Utiliser PowerShell pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="9663d-211">Use PowerShell to view entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9663d-212">Pour afficher les entrées de la liste d’inscriptions client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9663d-212">To view entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <Url | FileHash> [-Entry <URLValue | FileHashValue>] [-Block] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="9663d-213">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="9663d-213">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Block
```

<span data-ttu-id="9663d-214">Cet exemple renvoie des informations pour la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9663d-214">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="9663d-215">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9663d-215">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-block-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-216">Utiliser PowerShell pour modifier les entrées de bloc dans la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="9663d-216">Use PowerShell to modify block entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9663d-217">Vous ne pouvez pas modifier l’URL ou les valeurs de fichier existantes dans une entrée de bloc.</span><span class="sxs-lookup"><span data-stu-id="9663d-217">You can't modify the existing URL or file values within a block entry.</span></span> <span data-ttu-id="9663d-218">Pour modifier ces valeurs, vous devez supprimer et recréer l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9663d-218">To modify these values, you need to delete and recreate the entry.</span></span>

<span data-ttu-id="9663d-219">Pour modifier les entrées de bloc dans la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9663d-219">To modify block entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN"> [-Block] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="9663d-220">Cet exemple modifie la date d’expiration de l’entrée de bloc spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9663d-220">This example changes the expiration date of the specified block entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="9663d-221">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9663d-221">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-block-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-222">Utiliser PowerShell pour supprimer des entrées de blocage de la liste d’accès au client</span><span class="sxs-lookup"><span data-stu-id="9663d-222">Use PowerShell to remove block entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="9663d-223">Pour supprimer des entrées de blocage de la liste d’accès au client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9663d-223">To remove block entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="9663d-224">Cet exemple supprime l’entrée d’URL de bloc spécifiée de la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="9663d-224">This example removes the specified block URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="9663d-225">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9663d-225">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="9663d-226">Syntaxe d’URL pour la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="9663d-226">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="9663d-227">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="9663d-227">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="9663d-228">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="9663d-228">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="9663d-229">Unicode n’est pas pris en charge, mais c’est le cas de Punycode.</span><span class="sxs-lookup"><span data-stu-id="9663d-229">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="9663d-230">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="9663d-230">Hostnames are allowed if all of the following statements are true:</span></span>
  - <span data-ttu-id="9663d-231">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="9663d-231">The hostname contains a period.</span></span>
  - <span data-ttu-id="9663d-232">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="9663d-232">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="9663d-233">Il y a au moins deux caractères à droite du point.</span><span class="sxs-lookup"><span data-stu-id="9663d-233">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="9663d-234">Par exemple, `t.co` est autorisé ou `.com` `contoso.` non.</span><span class="sxs-lookup"><span data-stu-id="9663d-234">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="9663d-235">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="9663d-235">Subpaths are not implied.</span></span>

  <span data-ttu-id="9663d-236">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="9663d-236">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="9663d-237">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9663d-237">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="9663d-238">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="9663d-238">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="9663d-239">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="9663d-239">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="9663d-240">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9663d-240">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="9663d-241">Par exemple, `contoso.com/*` est autorisé ou `contoso.com*` `contoso.com/ab*` non.</span><span class="sxs-lookup"><span data-stu-id="9663d-241">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="9663d-242">Tous les sous-chemins ne sont pas impliqués par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="9663d-242">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="9663d-243">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="9663d-243">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="9663d-244">`*.com*` n’est pas valide (domaine non résolvable et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="9663d-244">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="9663d-245">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="9663d-245">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="9663d-246">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9663d-246">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="9663d-247">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="9663d-247">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="9663d-248">Par `~contoso.com` exemple, `contoso.com` inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="9663d-248">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="9663d-249">Les entrées d’URL qui contiennent des protocoles (par exemple, , ou ) échouent, car les entrées `http://` `https://` `ftp://` d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="9663d-249">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="9663d-250">Un nom d’utilisateur ou un mot de passe ne sont pas pris en charge ou requis.</span><span class="sxs-lookup"><span data-stu-id="9663d-250">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="9663d-251">Les guillemets (' ou « ) sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9663d-251">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="9663d-252">Une URL doit inclure toutes les redirections lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="9663d-252">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="9663d-253">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="9663d-253">URL entry scenarios</span></span>

<span data-ttu-id="9663d-254">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9663d-254">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="9663d-255">Scénario : aucun caractère générique</span><span class="sxs-lookup"><span data-stu-id="9663d-255">Scenario: No wildcards</span></span>

<span data-ttu-id="9663d-256">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9663d-256">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="9663d-257">**Autoriser la correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-257">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="9663d-258">**Autoriser non la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-258">**Allow not matched**:</span></span>

  - <span data-ttu-id="9663d-259">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-259">abc-contoso.com</span></span>
  - <span data-ttu-id="9663d-260">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9663d-260">contoso.com/a</span></span>
  - <span data-ttu-id="9663d-261">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-261">payroll.contoso.com</span></span>
  - <span data-ttu-id="9663d-262">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-262">test.com/contoso.com</span></span>
  - <span data-ttu-id="9663d-263">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-263">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="9663d-264">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-264">www.contoso.com</span></span>
  - <span data-ttu-id="9663d-265">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-265">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="9663d-266">**Bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-266">**Block match**:</span></span>

  - <span data-ttu-id="9663d-267">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-267">contoso.com</span></span>
  - <span data-ttu-id="9663d-268">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9663d-268">contoso.com/a</span></span>
  - <span data-ttu-id="9663d-269">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-269">payroll.contoso.com</span></span>
  - <span data-ttu-id="9663d-270">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-270">test.com/contoso.com</span></span>
  - <span data-ttu-id="9663d-271">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-271">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="9663d-272">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-272">www.contoso.com</span></span>
  - <span data-ttu-id="9663d-273">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-273">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="9663d-274">**Bloc non correspond :** abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-274">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="9663d-275">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="9663d-275">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="9663d-276">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9663d-276">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="9663d-277">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-277">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-278">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-278">www.contoso.com</span></span>
  - <span data-ttu-id="9663d-279">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-279">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9663d-280">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9663d-280">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9663d-281">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-281">123contoso.com</span></span>
  - <span data-ttu-id="9663d-282">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-282">contoso.com</span></span>
  - <span data-ttu-id="9663d-283">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-283">test.com/contoso.com</span></span>
  - <span data-ttu-id="9663d-284">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9663d-284">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="9663d-285">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9663d-285">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="9663d-286">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="9663d-286">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="9663d-287">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-287">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-288">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="9663d-288">contoso.com/a/b</span></span>
  - <span data-ttu-id="9663d-289">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9663d-289">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9663d-290">contoso.com/a/?q=joe@t.com</span><span class="sxs-lookup"><span data-stu-id="9663d-290">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="9663d-291">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9663d-291">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9663d-292">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-292">contoso.com</span></span>
  - <span data-ttu-id="9663d-293">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9663d-293">contoso.com/a</span></span>
  - <span data-ttu-id="9663d-294">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-294">www.contoso.com</span></span>
  - <span data-ttu-id="9663d-295">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-295">www.contoso.com/q=a@contoso.com</span></span>

#### <a name="scenario-left-tilde"></a><span data-ttu-id="9663d-296">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="9663d-296">Scenario: Left tilde</span></span>

<span data-ttu-id="9663d-297">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9663d-297">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="9663d-298">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-298">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-299">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-299">contoso.com</span></span>
  - <span data-ttu-id="9663d-300">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-300">www.contoso.com</span></span>
  - <span data-ttu-id="9663d-301">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-301">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9663d-302">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9663d-302">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9663d-303">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-303">123contoso.com</span></span>
  - <span data-ttu-id="9663d-304">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9663d-304">contoso.com/abc</span></span>
  - <span data-ttu-id="9663d-305">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9663d-305">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="9663d-306">Scénario : suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="9663d-306">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="9663d-307">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="9663d-307">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="9663d-308">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-308">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-309">contoso.com/?q=whatever@fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="9663d-309">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="9663d-310">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9663d-310">contoso.com/a</span></span>
  - <span data-ttu-id="9663d-311">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9663d-311">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9663d-312">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="9663d-312">contoso.com/ab</span></span>
  - <span data-ttu-id="9663d-313">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9663d-313">contoso.com/b</span></span>
  - <span data-ttu-id="9663d-314">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="9663d-314">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="9663d-315">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="9663d-315">contoso.com/ba</span></span>

- <span data-ttu-id="9663d-316">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-316">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="9663d-317">Scénario : sous-domaine générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="9663d-317">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="9663d-318">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="9663d-318">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="9663d-319">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-319">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-320">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="9663d-320">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="9663d-321">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9663d-321">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9663d-322">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9663d-322">www.contoso.com/a</span></span>
  - <span data-ttu-id="9663d-323">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="9663d-323">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="9663d-324">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="9663d-324">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="9663d-325">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9663d-325">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="9663d-326">Scénario : tilde gauche et droite</span><span class="sxs-lookup"><span data-stu-id="9663d-326">Scenario: Left and right tilde</span></span>

<span data-ttu-id="9663d-327">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="9663d-327">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="9663d-328">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-328">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-329">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-329">contoso.com</span></span>
  - <span data-ttu-id="9663d-330">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9663d-330">contoso.com/a</span></span>
  - <span data-ttu-id="9663d-331">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-331">www.contoso.com</span></span>
  - <span data-ttu-id="9663d-332">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9663d-332">www.contoso.com/b</span></span>
  - <span data-ttu-id="9663d-333">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-333">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9663d-334">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9663d-334">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9663d-335">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-335">123contoso.com</span></span>
  - <span data-ttu-id="9663d-336">contoso.org</span><span class="sxs-lookup"><span data-stu-id="9663d-336">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="9663d-337">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="9663d-337">Scenario: IP address</span></span>

<span data-ttu-id="9663d-338">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="9663d-338">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="9663d-339">**Autoriser la correspondance** **et bloquer la correspondance**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9663d-339">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="9663d-340">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="9663d-340">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9663d-341">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="9663d-341">1.2.3.4/a</span></span>
  - <span data-ttu-id="9663d-342">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="9663d-342">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="9663d-343">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="9663d-343">IP address with right wildcard</span></span>

<span data-ttu-id="9663d-344">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="9663d-344">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="9663d-345">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9663d-345">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9663d-346">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="9663d-346">1.2.3.4/b</span></span>
  - <span data-ttu-id="9663d-347">1.2.3.4/baaaa</span><span class="sxs-lookup"><span data-stu-id="9663d-347">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="9663d-348">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="9663d-348">Examples of invalid entries</span></span>

<span data-ttu-id="9663d-349">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="9663d-349">The following entries are invalid:</span></span>

- <span data-ttu-id="9663d-350">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="9663d-350">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="9663d-351">contoso</span><span class="sxs-lookup"><span data-stu-id="9663d-351">contoso</span></span>
  - <span data-ttu-id="9663d-352">\*.contoso.\*</span><span class="sxs-lookup"><span data-stu-id="9663d-352">\*.contoso.\*</span></span>
  - <span data-ttu-id="9663d-353">\*.com</span><span class="sxs-lookup"><span data-stu-id="9663d-353">\*.com</span></span>
  - <span data-ttu-id="9663d-354">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="9663d-354">\*.pdf</span></span>

- <span data-ttu-id="9663d-355">**Caractère générique sur du texte ou sans espacement :**</span><span class="sxs-lookup"><span data-stu-id="9663d-355">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="9663d-356">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="9663d-356">\*contoso.com</span></span>
  - <span data-ttu-id="9663d-357">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="9663d-357">contoso.com\*</span></span>
  - <span data-ttu-id="9663d-358">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9663d-358">\*1.2.3.4</span></span>
  - <span data-ttu-id="9663d-359">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="9663d-359">1.2.3.4\*</span></span>
  - <span data-ttu-id="9663d-360">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="9663d-360">contoso.com/a\*</span></span>
  - <span data-ttu-id="9663d-361">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="9663d-361">contoso.com/ab\*</span></span>

- <span data-ttu-id="9663d-362">**Adresses IP avec ports**:</span><span class="sxs-lookup"><span data-stu-id="9663d-362">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="9663d-363">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="9663d-363">contoso.com:443</span></span>
  - <span data-ttu-id="9663d-364">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="9663d-364">abc.contoso.com:25</span></span>

- <span data-ttu-id="9663d-365">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="9663d-365">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="9663d-366">\*.\*</span><span class="sxs-lookup"><span data-stu-id="9663d-366">\*.\*</span></span>

- <span data-ttu-id="9663d-367">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="9663d-367">**Middle wildcards**:</span></span>

  - <span data-ttu-id="9663d-368">conto \* so.com</span><span class="sxs-lookup"><span data-stu-id="9663d-368">conto\*so.com</span></span>
  - <span data-ttu-id="9663d-369">conto~so.com</span><span class="sxs-lookup"><span data-stu-id="9663d-369">conto~so.com</span></span>

- <span data-ttu-id="9663d-370">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="9663d-370">**Double wildcards**</span></span>

  - <span data-ttu-id="9663d-371">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="9663d-371">contoso.com/\*\*</span></span>
  - <span data-ttu-id="9663d-372">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="9663d-372">contoso.com/\*/\*</span></span>