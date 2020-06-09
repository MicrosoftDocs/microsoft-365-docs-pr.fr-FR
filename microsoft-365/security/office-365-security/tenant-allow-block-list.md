---
title: Gérer les URL et les fichiers autorisés et bloqués dans la liste d’autorisation/de blocage du client
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Les administrateurs peuvent apprendre à configurer les entrées d’URL et de fichiers dans la liste des clients autorisés/bloqués du centre de sécurité & Compliance Center.
ms.openlocfilehash: 0143ee2601a4cb9593c79f8c6c62d1f06914088f
ms.sourcegitcommit: 73b2426001dc5a3f4b857366ef51e877db549098
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2020
ms.locfileid: "44613419"
---
# <a name="manage-urls-and-files-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-103">Gérer les URL et les fichiers dans la liste d’autorisation/de blocage du client</span><span class="sxs-lookup"><span data-stu-id="7a382-103">Manage URLs and files in the Tenant Allow/Block List</span></span>

> [!NOTE]
> <span data-ttu-id="7a382-104">Les fonctionnalités décrites dans cette rubrique sont en mode aperçu, sont sujettes à modification et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="7a382-104">The features described in this topic are in Preview, are subject to change, and are not available in all organizations.</span></span>

<span data-ttu-id="7a382-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, vous pouvez ne pas utiliser le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="7a382-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="7a382-106">Par exemple, un bon message peut être marqué comme incorrect (faux positif) ou un message incorrect peut être autorisé par (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="7a382-106">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="7a382-107">La liste des clients autorisés/bloqués du centre de sécurité & conformité vous offre un moyen de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7a382-107">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="7a382-108">La liste d’autorisation/de blocage de client est utilisée pendant le flux de messagerie et au moment de l’utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="7a382-108">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="7a382-109">Vous pouvez spécifier des URL et des fichiers à autoriser ou à bloquer dans la liste des clients autorisés/bloqués.</span><span class="sxs-lookup"><span data-stu-id="7a382-109">You can specify URLs and files to allow or block in the Tenant Allow/Block List.</span></span>

<span data-ttu-id="7a382-110">Cette rubrique décrit comment configurer les entrées dans la liste des clients autorisés/bloqués du centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande autonome EOP PowerShell pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="7a382-110">This topic describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7a382-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7a382-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7a382-112">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="7a382-112">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="7a382-113">Pour accéder directement à la page d' **autorisation/de blocage de client** , utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="7a382-113">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="7a382-114">Vous spécifiez les fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="7a382-114">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="7a382-115">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="7a382-115">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```dos
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="7a382-116">Par exemple, la valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="7a382-116">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="7a382-117">Les valeurs de hachage de percepteur (pHash) ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="7a382-117">Perceptual hash (pHash) values are not allowed.</span></span>

- <span data-ttu-id="7a382-118">Les valeurs d’URL disponibles sont décrites dans la [syntaxe URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7a382-118">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

- <span data-ttu-id="7a382-119">La liste d’autorisation/de blocage de client autorise un nombre maximal de 500 entrées pour les URL et 500 entrées pour les hachages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7a382-119">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="7a382-120">Une entrée doit être active dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="7a382-120">An entry should be active within 15 minutes.</span></span>

- <span data-ttu-id="7a382-121">Les entrées bloquées prévalent sur les entrées autoriser.</span><span class="sxs-lookup"><span data-stu-id="7a382-121">Block entries take precedence over allow entries.</span></span>

- <span data-ttu-id="7a382-122">Par défaut, les entrées de la liste d’autorisation/de blocage client expirent au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="7a382-122">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="7a382-123">Vous pouvez spécifier une date ou la définir pour qu’elle n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="7a382-123">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="7a382-124">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7a382-124">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="7a382-125">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="7a382-125">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="7a382-126">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="7a382-126">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="7a382-127">Pour ajouter et supprimer des valeurs dans la liste d’autorisation/de blocage de client, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="7a382-127">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="7a382-128">Pour un accès en lecture seule à la liste verte/rouge de client, vous devez être membre du groupe de rôles **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="7a382-128">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Security Reader** role group.</span></span> <span data-ttu-id="7a382-129">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="7a382-129">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-130">Utiliser le centre de sécurité & conformité pour créer des entrées d’URL dans la liste verte/rouge de client</span><span class="sxs-lookup"><span data-stu-id="7a382-130">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="7a382-131">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la syntaxe de l' [URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7a382-131">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

1. <span data-ttu-id="7a382-132">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="7a382-132">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="7a382-133">Sur la page **liste des clients autorisés/bloqués** , vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="7a382-133">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Add**</span></span>

3. <span data-ttu-id="7a382-134">Dans la fenêtre mobile **ajouter de nouvelles URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a382-134">In the **Add new URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="7a382-135">**Ajouter des URL avec des caractères génériques**: entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="7a382-135">**Add URLs with wildcards**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="7a382-136">**Bloquer/autoriser**: indiquez si vous souhaitez **autoriser** ou **bloquer** les URL spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7a382-136">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified URLs.</span></span>

   - <span data-ttu-id="7a382-137">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a382-137">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="7a382-138">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration des entrées.</span><span class="sxs-lookup"><span data-stu-id="7a382-138">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="7a382-139">ou</span><span class="sxs-lookup"><span data-stu-id="7a382-139">or</span></span>

     - <span data-ttu-id="7a382-140">Déplacez le bouton bascule vers la droite pour configurer les entrées de sorte qu’elles n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="7a382-140">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="7a382-142">.</span><span class="sxs-lookup"><span data-stu-id="7a382-142">.</span></span>

   - <span data-ttu-id="7a382-143">**Facultatif Remarque**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="7a382-143">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="7a382-144">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7a382-144">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-145">Utiliser le centre de sécurité & conformité pour créer des entrées de fichier dans la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="7a382-145">Use the Security & Compliance Center to create file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="7a382-146">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="7a382-146">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="7a382-147">Sur la page **liste des clients autorisés/bloqués** , sélectionnez l’onglet **fichiers** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7a382-147">On the **Tenant Allow/Block List** page, select **Files** tab, and then click **Add**.</span></span>

3. <span data-ttu-id="7a382-148">Dans la fenêtre mobile **ajouter de nouveaux fichiers** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a382-148">In the **Add new files** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="7a382-149">**Ajouter des hachages de fichier**: saisissez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="7a382-149">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="7a382-150">**Bloquer/autoriser**: indiquez si vous souhaitez **autoriser** ou **bloquer** les fichiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7a382-150">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified files.</span></span>

   - <span data-ttu-id="7a382-151">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a382-151">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="7a382-152">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration des entrées.</span><span class="sxs-lookup"><span data-stu-id="7a382-152">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="7a382-153">ou</span><span class="sxs-lookup"><span data-stu-id="7a382-153">or</span></span>

     - <span data-ttu-id="7a382-154">Déplacez le bouton bascule vers la droite pour configurer les entrées de sorte qu’elles n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="7a382-154">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="7a382-156">.</span><span class="sxs-lookup"><span data-stu-id="7a382-156">.</span></span>

   - <span data-ttu-id="7a382-157">**Facultatif Remarque**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="7a382-157">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="7a382-158">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7a382-158">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-159">Utiliser le centre de sécurité & conformité pour afficher les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-159">Use the Security & Compliance Center to view URL and file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="7a382-160">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="7a382-160">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="7a382-161">Sélectionnez l’onglet **URL** ou **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="7a382-161">Select the **URLs** tab or the **Files** tab.</span></span>

<span data-ttu-id="7a382-162">Cliquez sur les en-têtes de colonne suivants pour trier dans l’ordre croissant ou décroissant :</span><span class="sxs-lookup"><span data-stu-id="7a382-162">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="7a382-163">**Valeur**: l’URL ou le hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="7a382-163">**Value**: The URL or the file hash.</span></span>
- <span data-ttu-id="7a382-164">**Action**: **bloquer** ou **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="7a382-164">**Action**: **Block** or **Allow**.</span></span>
- <span data-ttu-id="7a382-165">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="7a382-165">**Last updated date**</span></span>
- <span data-ttu-id="7a382-166">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="7a382-166">**Expiration date**</span></span>
- <span data-ttu-id="7a382-167">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="7a382-167">**Note**</span></span>

<span data-ttu-id="7a382-168">Cliquez sur **groupe** pour regrouper les entrées par **action** (**bloquer** ou **autoriser**) ou **aucune**.</span><span class="sxs-lookup"><span data-stu-id="7a382-168">Click **Group** to group the entries by **Action** (**Block** or **Allow**) or **None**.</span></span>

<span data-ttu-id="7a382-169">Cliquez sur **Rechercher**, entrez la totalité ou une partie d’une URL ou d’une valeur de fichier, puis appuyez sur entrée pour rechercher une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="7a382-169">Click **Search**, enter all or part of a URL or file value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="7a382-170">Lorsque vous avez terminé, cliquez sur **Effacer** l' ![ icône Rechercher ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) .</span><span class="sxs-lookup"><span data-stu-id="7a382-170">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="7a382-171">Cliquez sur **filtre**.</span><span class="sxs-lookup"><span data-stu-id="7a382-171">Click **Filter**.</span></span> <span data-ttu-id="7a382-172">Dans le menu volant **filtre** qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a382-172">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="7a382-173">**Action**: sélectionnez **autoriser**, **bloquer** ou les deux.</span><span class="sxs-lookup"><span data-stu-id="7a382-173">**Action**: Select **Allow**, **Block** or both.</span></span>

- <span data-ttu-id="7a382-174">**N’expire jamais**: sélectionnez désactivé (désactiver ![ ](../../media/scc-toggle-off.png) ) ou activé ( ![ bascule ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) ).</span><span class="sxs-lookup"><span data-stu-id="7a382-174">**Never expire**: Select off (![Toggle off](../../media/scc-toggle-off.png)) or on (![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)).</span></span>

- <span data-ttu-id="7a382-175">**Dernière mise à jour**: sélectionnez une date**de**début (de), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="7a382-175">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="7a382-176">**Date d’expiration**: sélectionnez une date de début (**de**), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="7a382-176">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="7a382-177">Lorsque vous avez terminé, cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="7a382-177">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="7a382-178">Pour effacer les filtres existants, cliquez sur **Filtrer**et, dans le menu volant **filtre** qui s’affiche, cliquez sur **effacer les filtres**.</span><span class="sxs-lookup"><span data-stu-id="7a382-178">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-179">Utiliser le centre de sécurité & conformité pour modifier les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-179">Use the Security & Compliance Center to modify URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="7a382-180">Vous ne pouvez pas modifier la valeur de l’URL ou du fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="7a382-180">You can't modify the URL or file value itself.</span></span> <span data-ttu-id="7a382-181">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="7a382-181">Instead, you need to delete the entry and recreate it.</span></span>

1. <span data-ttu-id="7a382-182">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="7a382-182">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="7a382-183">Sélectionnez l’onglet **URL** ou **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="7a382-183">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="7a382-184">Sélectionnez l’entrée que vous souhaitez modifier, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) .</span><span class="sxs-lookup"><span data-stu-id="7a382-184">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="7a382-185">Dans le menu volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a382-185">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="7a382-186">**Bloquer/autoriser**: sélectionnez **autoriser** ou **bloquer**.</span><span class="sxs-lookup"><span data-stu-id="7a382-186">**Block/Allow**: Select **Allow** or **Block**.</span></span>

   - <span data-ttu-id="7a382-187">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a382-187">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="7a382-188">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="7a382-188">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

     <span data-ttu-id="7a382-189">ou</span><span class="sxs-lookup"><span data-stu-id="7a382-189">or</span></span>

     - <span data-ttu-id="7a382-190">Déplacez le bouton bascule vers la droite pour configurer l’entrée de sorte qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="7a382-190">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="7a382-192">.</span><span class="sxs-lookup"><span data-stu-id="7a382-192">.</span></span>

   - <span data-ttu-id="7a382-193">**Facultatif Remarque**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="7a382-193">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="7a382-194">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7a382-194">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-url-and-file-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-195">Utiliser le centre de sécurité & conformité pour supprimer les entrées d’URL et de fichier de la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="7a382-195">Use the Security & Compliance Center to remove URL and file entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="7a382-196">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="7a382-196">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="7a382-197">Sélectionnez l’onglet **URL** ou **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="7a382-197">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="7a382-198">Sélectionnez l’entrée que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) .</span><span class="sxs-lookup"><span data-stu-id="7a382-198">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="7a382-199">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="7a382-199">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-200">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-200">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-201">Utiliser PowerShell pour ajouter des entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-201">Use PowerShell to add URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="7a382-202">Pour ajouter des entrées d’URL et de fichier dans la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7a382-202">To add URL and file entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <Url | FileHash> -Action <Allow | Block> -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="7a382-203">Cet exemple montre comment ajouter une entrée de bloc d’URL pour contoso.com et tous les sous-domaines (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7a382-203">This example adds a URL block entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="7a382-204">Étant donné que nous n’utilisons pas les paramètres ExpirationDate ou noexpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="7a382-204">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType Url -Action Block -Entries ~contoso.com
```

```powershell
New-TenantAllowBlockListItem -ListType FileHash -Action Allow -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="7a382-205">Cet exemple ajoute une entrée d’autorisation de fichier pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="7a382-205">This example adds a file allow entry for the specified files that never expires.</span></span>

<span data-ttu-id="7a382-206">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="7a382-206">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-207">Utiliser PowerShell pour afficher les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-207">Use PowerShell to view URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="7a382-208">Pour afficher les entrées d’URL et de fichier dans la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7a382-208">To view URL and file entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <Url | FileHash> [-Entry <URLValue | FileHashValue>] [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="7a382-209">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="7a382-209">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Action Block
```

<span data-ttu-id="7a382-210">Cet exemple renvoie des informations sur la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7a382-210">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="7a382-211">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="7a382-211">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-212">Utiliser PowerShell pour modifier les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-212">Use PowerShell to modify URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="7a382-213">Vous ne pouvez pas modifier la valeur de l’URL ou du fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="7a382-213">You can't modify the URL or file value itself.</span></span> <span data-ttu-id="7a382-214">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="7a382-214">Instead, you need to delete the entry and recreate it.</span></span>

<span data-ttu-id="7a382-215">Pour modifier les entrées d’URL et de fichier dans la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7a382-215">To modify URL and file entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN"> [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="7a382-216">Cet exemple montre comment modifier la date d’expiration de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7a382-216">This example changes the expiration date of the specified entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="7a382-217">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="7a382-217">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-url-and-file-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-218">Utiliser PowerShell pour supprimer les entrées d’URL et de fichier de la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="7a382-218">Use PowerShell to remove URL and file entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="7a382-219">Pour supprimer les entrées d’URL et de fichier de la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7a382-219">To remove URL and file entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="7a382-220">Cet exemple supprime l’entrée d’URL spécifiée de la liste des clients bloqués/bloqués.</span><span class="sxs-lookup"><span data-stu-id="7a382-220">This example removes the specified URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="7a382-221">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="7a382-221">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="7a382-222">Syntaxe d’URL de la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="7a382-222">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="7a382-223">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="7a382-223">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="7a382-224">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test. pdf).</span><span class="sxs-lookup"><span data-stu-id="7a382-224">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="7a382-225">Unicode n’est pas pris en charge, mais Punycode est.</span><span class="sxs-lookup"><span data-stu-id="7a382-225">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="7a382-226">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="7a382-226">Hostnames are allowed if all of the following statements are true:</span></span>

  - <span data-ttu-id="7a382-227">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="7a382-227">The hostname contains a period.</span></span>
  - <span data-ttu-id="7a382-228">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="7a382-228">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="7a382-229">Il y a au moins deux caractères à droite de la période.</span><span class="sxs-lookup"><span data-stu-id="7a382-229">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="7a382-230">Par exemple, `t.co` est autorisé ou n’est `.com` `contoso.` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7a382-230">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="7a382-231">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="7a382-231">Subpaths are not implied.</span></span>

  <span data-ttu-id="7a382-232">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="7a382-232">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="7a382-233">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="7a382-233">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="7a382-234">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="7a382-234">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="7a382-235">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7a382-235">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="7a382-236">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7a382-236">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="7a382-237">Par exemple, `contoso.com/*` est autorisé ou n’est `contoso.com*` `contoso.com/ab*` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7a382-237">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="7a382-238">Tous les sous-chemins ne sont pas implicitement par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="7a382-238">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="7a382-239">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="7a382-239">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="7a382-240">`*.com*`n’est pas valide (ce n’est pas un domaine pouvant être résolu et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="7a382-240">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="7a382-241">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="7a382-241">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="7a382-242">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="7a382-242">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="7a382-243">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="7a382-243">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="7a382-244">Par exemple `~contoso.com` `contoso.com` , inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="7a382-244">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="7a382-245">Les entrées d’URL qui contiennent des protocoles (par exemple,, `http://` `https://` ou `ftp://` ) échouent, car les entrées d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="7a382-245">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="7a382-246">Un nom d’utilisateur ou un mot de passe n’est pas pris en charge ou obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7a382-246">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="7a382-247">Les guillemets ('ou ") sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7a382-247">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="7a382-248">Une URL doit inclure toutes les redirections, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7a382-248">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="7a382-249">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="7a382-249">URL entry scenarios</span></span>

<span data-ttu-id="7a382-250">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a382-250">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="7a382-251">Scénario : pas de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="7a382-251">Scenario: No wildcards</span></span>

<span data-ttu-id="7a382-252">**Entrée**:`contoso.com`</span><span class="sxs-lookup"><span data-stu-id="7a382-252">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="7a382-253">**Correspondance autorisée**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-253">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="7a382-254">**Ne pas faire correspondre**:</span><span class="sxs-lookup"><span data-stu-id="7a382-254">**Allow not matched**:</span></span>

  - <span data-ttu-id="7a382-255">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-255">abc-contoso.com</span></span>
  - <span data-ttu-id="7a382-256">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="7a382-256">contoso.com/a</span></span>
  - <span data-ttu-id="7a382-257">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-257">payroll.contoso.com</span></span>
  - <span data-ttu-id="7a382-258">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-258">test.com/contoso.com</span></span>
  - <span data-ttu-id="7a382-259">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-259">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="7a382-260">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-260">www.contoso.com</span></span>
  - <span data-ttu-id="7a382-261">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="7a382-261">www.contoso.com/q=a@contoso.com</span></span>
  
- <span data-ttu-id="7a382-262">**Correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-262">**Block match**:</span></span>

  - <span data-ttu-id="7a382-263">contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-263">contoso.com</span></span>
  - <span data-ttu-id="7a382-264">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="7a382-264">contoso.com/a</span></span>
  - <span data-ttu-id="7a382-265">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-265">payroll.contoso.com</span></span>
  - <span data-ttu-id="7a382-266">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-266">test.com/contoso.com</span></span>
  - <span data-ttu-id="7a382-267">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-267">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="7a382-268">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-268">www.contoso.com</span></span>
  - <span data-ttu-id="7a382-269">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="7a382-269">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="7a382-270">**Bloc sans correspondance**: ABC-contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-270">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="7a382-271">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="7a382-271">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="7a382-272">**Entrée**:`*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="7a382-272">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="7a382-273">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-273">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-274">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-274">www.contoso.com</span></span>
  - <span data-ttu-id="7a382-275">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-275">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="7a382-276">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="7a382-276">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="7a382-277">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-277">123contoso.com</span></span>
  - <span data-ttu-id="7a382-278">contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-278">contoso.com</span></span>
  - <span data-ttu-id="7a382-279">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-279">test.com/contoso.com</span></span>
  - <span data-ttu-id="7a382-280">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="7a382-280">www.contoso.com/abc</span></span>
  
#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="7a382-281">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="7a382-281">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="7a382-282">**Entrée**:`contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="7a382-282">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="7a382-283">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-283">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-284">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="7a382-284">contoso.com/a/b</span></span>
  - <span data-ttu-id="7a382-285">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="7a382-285">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="7a382-286">contoso. com/a/ ? q = joe@t. com</span><span class="sxs-lookup"><span data-stu-id="7a382-286">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="7a382-287">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="7a382-287">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="7a382-288">contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-288">contoso.com</span></span>
  - <span data-ttu-id="7a382-289">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="7a382-289">contoso.com/a</span></span>
  - <span data-ttu-id="7a382-290">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-290">www.contoso.com</span></span>
  - <span data-ttu-id="7a382-291">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="7a382-291">www.contoso.com/q=a@contoso.com</span></span>
  
#### <a name="scenario-left-tilde"></a><span data-ttu-id="7a382-292">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="7a382-292">Scenario: Left tilde</span></span>

<span data-ttu-id="7a382-293">**Entrée**:`~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="7a382-293">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="7a382-294">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-294">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-295">contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-295">contoso.com</span></span>
  - <span data-ttu-id="7a382-296">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-296">www.contoso.com</span></span>
  - <span data-ttu-id="7a382-297">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-297">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="7a382-298">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="7a382-298">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="7a382-299">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-299">123contoso.com</span></span>
  - <span data-ttu-id="7a382-300">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="7a382-300">contoso.com/abc</span></span>
  - <span data-ttu-id="7a382-301">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="7a382-301">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="7a382-302">Scénario : suffixe de caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="7a382-302">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="7a382-303">**Entrée**:`contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="7a382-303">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="7a382-304">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-304">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-305">contoso. com/ ? q = whatever@fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="7a382-305">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="7a382-306">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="7a382-306">contoso.com/a</span></span>
  - <span data-ttu-id="7a382-307">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="7a382-307">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="7a382-308">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="7a382-308">contoso.com/ab</span></span>
  - <span data-ttu-id="7a382-309">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="7a382-309">contoso.com/b</span></span>
  - <span data-ttu-id="7a382-310">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="7a382-310">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="7a382-311">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="7a382-311">contoso.com/ba</span></span>

- <span data-ttu-id="7a382-312">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-312">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="7a382-313">Scénario : sous-domaine du caractère générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="7a382-313">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="7a382-314">**Entrée**:`*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="7a382-314">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="7a382-315">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-315">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-316">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="7a382-316">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="7a382-317">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="7a382-317">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="7a382-318">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="7a382-318">www.contoso.com/a</span></span>
  - <span data-ttu-id="7a382-319">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="7a382-319">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="7a382-320">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="7a382-320">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="7a382-321">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="7a382-321">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="7a382-322">Scénario : tilde gauche et droit</span><span class="sxs-lookup"><span data-stu-id="7a382-322">Scenario: Left and right tilde</span></span>

<span data-ttu-id="7a382-323">**Entrée**:`~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="7a382-323">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="7a382-324">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-324">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-325">contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-325">contoso.com</span></span>
  - <span data-ttu-id="7a382-326">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="7a382-326">contoso.com/a</span></span>
  - <span data-ttu-id="7a382-327">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-327">www.contoso.com</span></span>
  - <span data-ttu-id="7a382-328">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="7a382-328">www.contoso.com/b</span></span>
  - <span data-ttu-id="7a382-329">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-329">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="7a382-330">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="7a382-330">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="7a382-331">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-331">123contoso.com</span></span>
  - <span data-ttu-id="7a382-332">contoso.org</span><span class="sxs-lookup"><span data-stu-id="7a382-332">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="7a382-333">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="7a382-333">Scenario: IP address</span></span>

<span data-ttu-id="7a382-334">**Entrée**:`1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="7a382-334">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="7a382-335">**Autoriser la correspondance** et la **correspondance de bloc**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="7a382-335">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="7a382-336">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="7a382-336">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="7a382-337">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="7a382-337">1.2.3.4/a</span></span>
  - <span data-ttu-id="7a382-338">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="7a382-338">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="7a382-339">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="7a382-339">IP address with right wildcard</span></span>

<span data-ttu-id="7a382-340">**Entrée**:`1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="7a382-340">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="7a382-341">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="7a382-341">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="7a382-342">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="7a382-342">1.2.3.4/b</span></span>
  - <span data-ttu-id="7a382-343">1.2.3.4/bAAAA</span><span class="sxs-lookup"><span data-stu-id="7a382-343">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="7a382-344">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="7a382-344">Examples of invalid entries</span></span>

<span data-ttu-id="7a382-345">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="7a382-345">The following entries are invalid:</span></span>

- <span data-ttu-id="7a382-346">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="7a382-346">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="7a382-347">contoso</span><span class="sxs-lookup"><span data-stu-id="7a382-347">contoso</span></span>
  - <span data-ttu-id="7a382-348">\*contoso.\*</span><span class="sxs-lookup"><span data-stu-id="7a382-348">\*.contoso.\*</span></span>
  - <span data-ttu-id="7a382-349">\*. com</span><span class="sxs-lookup"><span data-stu-id="7a382-349">\*.com</span></span>
  - <span data-ttu-id="7a382-350">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="7a382-350">\*.pdf</span></span>

- <span data-ttu-id="7a382-351">**Caractères génériques sur le texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="7a382-351">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="7a382-352">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="7a382-352">\*contoso.com</span></span>
  - <span data-ttu-id="7a382-353">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="7a382-353">contoso.com\*</span></span>
  - <span data-ttu-id="7a382-354">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="7a382-354">\*1.2.3.4</span></span>
  - <span data-ttu-id="7a382-355">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="7a382-355">1.2.3.4\*</span></span>
  - <span data-ttu-id="7a382-356">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="7a382-356">contoso.com/a\*</span></span>
  - <span data-ttu-id="7a382-357">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="7a382-357">contoso.com/ab\*</span></span>

- <span data-ttu-id="7a382-358">**Adresses IP avec des ports**:</span><span class="sxs-lookup"><span data-stu-id="7a382-358">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="7a382-359">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="7a382-359">contoso.com:443</span></span>
  - <span data-ttu-id="7a382-360">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="7a382-360">abc.contoso.com:25</span></span>

- <span data-ttu-id="7a382-361">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="7a382-361">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="7a382-362">\*.\*</span><span class="sxs-lookup"><span data-stu-id="7a382-362">\*.\*</span></span>

- <span data-ttu-id="7a382-363">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="7a382-363">**Middle wildcards**:</span></span>

  - <span data-ttu-id="7a382-364">CONT \* so.com</span><span class="sxs-lookup"><span data-stu-id="7a382-364">conto\*so.com</span></span>
  - <span data-ttu-id="7a382-365">Conto ~ so. com</span><span class="sxs-lookup"><span data-stu-id="7a382-365">conto~so.com</span></span>

- <span data-ttu-id="7a382-366">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="7a382-366">**Double wildcards**</span></span>

  - <span data-ttu-id="7a382-367">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="7a382-367">contoso.com/\*\*</span></span>
  - <span data-ttu-id="7a382-368">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="7a382-368">contoso.com/\*/\*</span></span>
