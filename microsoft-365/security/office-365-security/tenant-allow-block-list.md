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
ms.openlocfilehash: 742a44c7ed63c8a3037e2ada295c94f89afa9c93
ms.sourcegitcommit: df6cc8c2eb2a65c7668f2953b0f7ec783a596d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/13/2020
ms.locfileid: "44726814"
---
# <a name="manage-urls-and-files-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-103">Gérer les URL et les fichiers dans la liste d’autorisation/de blocage du client</span><span class="sxs-lookup"><span data-stu-id="9739e-103">Manage URLs and files in the Tenant Allow/Block List</span></span>

> [!NOTE]
> <span data-ttu-id="9739e-104">Les fonctionnalités décrites dans cette rubrique sont en mode aperçu, sont sujettes à modification et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="9739e-104">The features described in this topic are in Preview, are subject to change, and are not available in all organizations.</span></span>

<span data-ttu-id="9739e-105">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, vous pouvez ne pas utiliser le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="9739e-105">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="9739e-106">Par exemple, un bon message peut être marqué comme incorrect (faux positif) ou un message incorrect peut être autorisé par (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="9739e-106">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="9739e-107">La liste des clients autorisés/bloqués du centre de sécurité & conformité vous offre un moyen de remplacer manuellement les verdicts de filtrage Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9739e-107">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="9739e-108">La liste d’autorisation/de blocage de client est utilisée pendant le flux de messagerie et au moment de l’utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="9739e-108">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="9739e-109">Vous pouvez spécifier des URL et des fichiers à autoriser ou à bloquer dans la liste des clients autorisés/bloqués.</span><span class="sxs-lookup"><span data-stu-id="9739e-109">You can specify URLs and files to allow or block in the Tenant Allow/Block List.</span></span>

<span data-ttu-id="9739e-110">Cette rubrique décrit comment configurer les entrées dans la liste des clients autorisés/bloqués du centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande autonome EOP PowerShell pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="9739e-110">This topic describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9739e-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9739e-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9739e-112">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="9739e-112">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="9739e-113">Pour accéder directement à la page d' **autorisation/de blocage de client** , utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="9739e-113">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="9739e-114">Vous spécifiez les fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="9739e-114">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="9739e-115">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="9739e-115">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```dos
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="9739e-116">Par exemple, la valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="9739e-116">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="9739e-117">Les valeurs de hachage de percepteur (pHash) ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="9739e-117">Perceptual hash (pHash) values are not allowed.</span></span>

- <span data-ttu-id="9739e-118">Les valeurs d’URL disponibles sont décrites dans la [syntaxe URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9739e-118">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

- <span data-ttu-id="9739e-119">La liste d’autorisation/de blocage de client autorise un nombre maximal de 500 entrées pour les URL et 500 entrées pour les hachages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9739e-119">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="9739e-120">Une entrée doit être active dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="9739e-120">An entry should be active within 15 minutes.</span></span>

- <span data-ttu-id="9739e-121">Les entrées bloquées prévalent sur les entrées autoriser.</span><span class="sxs-lookup"><span data-stu-id="9739e-121">Block entries take precedence over allow entries.</span></span>

- <span data-ttu-id="9739e-122">Par défaut, les entrées de la liste d’autorisation/de blocage client expirent au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="9739e-122">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="9739e-123">Vous pouvez spécifier une date ou la définir pour qu’elle n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="9739e-123">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="9739e-124">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="9739e-124">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="9739e-125">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="9739e-125">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="9739e-126">Avant de pouvoir effectuer les procédures décrites dans cette rubrique, vous devez disposer des autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9739e-126">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="9739e-127">Pour ajouter et supprimer des valeurs dans la liste d’autorisation/de blocage de client, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-127">To add and remove values from the Tenant Allow/Block List, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="9739e-128">**Gestion** de l’organisation ou **administrateur de sécurité** dans le [Centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9739e-128">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="9739e-129">Gestion de l' **organisation** ou gestion de l' **hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="9739e-129">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="9739e-130">Pour un accès en lecture seule à la liste verte/rouge de client, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-130">For read-only access to the Tenant Allow/Block List, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="9739e-131">**Lecteur de sécurité** dans le [centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9739e-131">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="9739e-132">**Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="9739e-132">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

## <a name="use-the-security--compliance-center-to-create-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-133">Utiliser le centre de sécurité & conformité pour créer des entrées d’URL dans la liste verte/rouge de client</span><span class="sxs-lookup"><span data-stu-id="9739e-133">Use the Security & Compliance Center to create URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9739e-134">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la syntaxe de l' [URL de la section liste des clients autorisés/bloqués](#url-syntax-for-the-tenant-allowblock-list) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9739e-134">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this topic.</span></span>

1. <span data-ttu-id="9739e-135">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="9739e-135">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9739e-136">Sur la page **liste des clients autorisés/bloqués** , vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="9739e-136">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Add**</span></span>

3. <span data-ttu-id="9739e-137">Dans la fenêtre mobile **ajouter de nouvelles URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-137">In the **Add new URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9739e-138">**Ajouter des URL avec des caractères génériques**: entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="9739e-138">**Add URLs with wildcards**: Enter one URL per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="9739e-139">**Bloquer/autoriser**: indiquez si vous souhaitez **autoriser** ou **bloquer** les URL spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9739e-139">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified URLs.</span></span>

   - <span data-ttu-id="9739e-140">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9739e-140">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9739e-141">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration des entrées.</span><span class="sxs-lookup"><span data-stu-id="9739e-141">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="9739e-142">ou</span><span class="sxs-lookup"><span data-stu-id="9739e-142">or</span></span>

     - <span data-ttu-id="9739e-143">Déplacez le bouton bascule vers la droite pour configurer les entrées de sorte qu’elles n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="9739e-143">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="9739e-145">.</span><span class="sxs-lookup"><span data-stu-id="9739e-145">.</span></span>

   - <span data-ttu-id="9739e-146">**Facultatif Remarque**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="9739e-146">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="9739e-147">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9739e-147">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-148">Utiliser le centre de sécurité & conformité pour créer des entrées de fichier dans la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="9739e-148">Use the Security & Compliance Center to create file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9739e-149">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="9739e-149">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9739e-150">Sur la page **liste des clients autorisés/bloqués** , sélectionnez l’onglet **fichiers** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9739e-150">On the **Tenant Allow/Block List** page, select **Files** tab, and then click **Add**.</span></span>

3. <span data-ttu-id="9739e-151">Dans la fenêtre mobile **ajouter de nouveaux fichiers** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-151">In the **Add new files** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9739e-152">**Ajouter des hachages de fichier**: saisissez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="9739e-152">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="9739e-153">**Bloquer/autoriser**: indiquez si vous souhaitez **autoriser** ou **bloquer** les fichiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9739e-153">**Block/Allow**: Select whether you want to **Allow** or **Block** the specified files.</span></span>

   - <span data-ttu-id="9739e-154">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9739e-154">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9739e-155">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration des entrées.</span><span class="sxs-lookup"><span data-stu-id="9739e-155">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="9739e-156">ou</span><span class="sxs-lookup"><span data-stu-id="9739e-156">or</span></span>

     - <span data-ttu-id="9739e-157">Déplacez le bouton bascule vers la droite pour configurer les entrées de sorte qu’elles n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="9739e-157">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="9739e-159">.</span><span class="sxs-lookup"><span data-stu-id="9739e-159">.</span></span>

   - <span data-ttu-id="9739e-160">**Facultatif Remarque**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="9739e-160">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="9739e-161">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9739e-161">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-162">Utiliser le centre de sécurité & conformité pour afficher les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-162">Use the Security & Compliance Center to view URL and file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9739e-163">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="9739e-163">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9739e-164">Sélectionnez l’onglet **URL** ou **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="9739e-164">Select the **URLs** tab or the **Files** tab.</span></span>

<span data-ttu-id="9739e-165">Cliquez sur les en-têtes de colonne suivants pour trier dans l’ordre croissant ou décroissant :</span><span class="sxs-lookup"><span data-stu-id="9739e-165">Click on the following column headings to sort in ascending or descending order:</span></span>

- <span data-ttu-id="9739e-166">**Valeur**: l’URL ou le hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="9739e-166">**Value**: The URL or the file hash.</span></span>
- <span data-ttu-id="9739e-167">**Action**: **bloquer** ou **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="9739e-167">**Action**: **Block** or **Allow**.</span></span>
- <span data-ttu-id="9739e-168">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="9739e-168">**Last updated date**</span></span>
- <span data-ttu-id="9739e-169">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="9739e-169">**Expiration date**</span></span>
- <span data-ttu-id="9739e-170">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="9739e-170">**Note**</span></span>

<span data-ttu-id="9739e-171">Cliquez sur **groupe** pour regrouper les entrées par **action** (**bloquer** ou **autoriser**) ou **aucune**.</span><span class="sxs-lookup"><span data-stu-id="9739e-171">Click **Group** to group the entries by **Action** (**Block** or **Allow**) or **None**.</span></span>

<span data-ttu-id="9739e-172">Cliquez sur **Rechercher**, entrez la totalité ou une partie d’une URL ou d’une valeur de fichier, puis appuyez sur entrée pour rechercher une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="9739e-172">Click **Search**, enter all or part of a URL or file value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="9739e-173">Lorsque vous avez terminé, cliquez sur **Effacer** l' ![ icône Rechercher ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) .</span><span class="sxs-lookup"><span data-stu-id="9739e-173">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

<span data-ttu-id="9739e-174">Cliquez sur **filtre**.</span><span class="sxs-lookup"><span data-stu-id="9739e-174">Click **Filter**.</span></span> <span data-ttu-id="9739e-175">Dans le menu volant **filtre** qui s’affiche, configurez l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-175">In the **Filter** flyout that appears, configure any of the following settings:</span></span>

- <span data-ttu-id="9739e-176">**Action**: sélectionnez **autoriser**, **bloquer** ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9739e-176">**Action**: Select **Allow**, **Block** or both.</span></span>

- <span data-ttu-id="9739e-177">**N’expire jamais**: sélectionnez désactivé (désactiver ![ ](../../media/scc-toggle-off.png) ) ou activé ( ![ bascule ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) ).</span><span class="sxs-lookup"><span data-stu-id="9739e-177">**Never expire**: Select off (![Toggle off](../../media/scc-toggle-off.png)) or on (![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)).</span></span>

- <span data-ttu-id="9739e-178">**Dernière mise à jour**: sélectionnez une date**de**début (de), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9739e-178">**Last updated**: Select a start date (**From**), an end date (**To**) or both.</span></span>

- <span data-ttu-id="9739e-179">**Date d’expiration**: sélectionnez une date de début (**de**), une date de fin (**à**) ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9739e-179">**Expiration date**: Select a start date (**From**), an end date (**To**) or both.</span></span>

<span data-ttu-id="9739e-180">Lorsque vous avez terminé, cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="9739e-180">When you're finished, click **Apply**.</span></span>

<span data-ttu-id="9739e-181">Pour effacer les filtres existants, cliquez sur **Filtrer**et, dans le menu volant **filtre** qui s’affiche, cliquez sur **effacer les filtres**.</span><span class="sxs-lookup"><span data-stu-id="9739e-181">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-182">Utiliser le centre de sécurité & conformité pour modifier les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-182">Use the Security & Compliance Center to modify URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9739e-183">Vous ne pouvez pas modifier la valeur de l’URL ou du fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="9739e-183">You can't modify the URL or file value itself.</span></span> <span data-ttu-id="9739e-184">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="9739e-184">Instead, you need to delete the entry and recreate it.</span></span>

1. <span data-ttu-id="9739e-185">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="9739e-185">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9739e-186">Sélectionnez l’onglet **URL** ou **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="9739e-186">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="9739e-187">Sélectionnez l’entrée que vous souhaitez modifier, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) .</span><span class="sxs-lookup"><span data-stu-id="9739e-187">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span>

4. <span data-ttu-id="9739e-188">Dans le menu volant qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-188">In the flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="9739e-189">**Bloquer/autoriser**: sélectionnez **autoriser** ou **bloquer**.</span><span class="sxs-lookup"><span data-stu-id="9739e-189">**Block/Allow**: Select **Allow** or **Block**.</span></span>

   - <span data-ttu-id="9739e-190">N' **expire jamais**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9739e-190">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="9739e-191">Vérifiez que le paramètre est désactivé (désactivez-le ![ ](../../media/scc-toggle-off.png) ) et utilisez la zone **expire** le, pour spécifier la date d’expiration de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9739e-191">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entry.</span></span>

     <span data-ttu-id="9739e-192">ou</span><span class="sxs-lookup"><span data-stu-id="9739e-192">or</span></span>

     - <span data-ttu-id="9739e-193">Déplacez le bouton bascule vers la droite pour configurer l’entrée de sorte qu’elle n’expire jamais :</span><span class="sxs-lookup"><span data-stu-id="9739e-193">Move the toggle to the right to configure the entry to never expire:</span></span> ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)<span data-ttu-id="9739e-195">.</span><span class="sxs-lookup"><span data-stu-id="9739e-195">.</span></span>

   - <span data-ttu-id="9739e-196">**Facultatif Remarque**: entrez un texte descriptif pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9739e-196">**Optional note**: Enter descriptive text for the entry.</span></span>

5. <span data-ttu-id="9739e-197">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9739e-197">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-url-and-file-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-198">Utiliser le centre de sécurité & conformité pour supprimer les entrées d’URL et de fichier de la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="9739e-198">Use the Security & Compliance Center to remove URL and file entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="9739e-199">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **Policy** \> **liste verte/rouge**de la stratégie de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="9739e-199">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="9739e-200">Sélectionnez l’onglet **URL** ou **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="9739e-200">Select the **URLs** tab or the **Files** tab.</span></span>

3. <span data-ttu-id="9739e-201">Sélectionnez l’entrée que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) .</span><span class="sxs-lookup"><span data-stu-id="9739e-201">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="9739e-202">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9739e-202">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-203">Utiliser Exchange Online PowerShell ou le PowerShell autonome EOP pour configurer la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-203">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-204">Utiliser PowerShell pour ajouter des entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-204">Use PowerShell to add URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9739e-205">Pour ajouter des entrées d’URL et de fichier dans la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9739e-205">To add URL and file entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <Url | FileHash> -Action <Allow | Block> -Entries <String[]> [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="9739e-206">Cet exemple montre comment ajouter une entrée de bloc d’URL pour contoso.com et tous les sous-domaines (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="9739e-206">This example adds a URL block entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="9739e-207">Étant donné que nous n’utilisons pas les paramètres ExpirationDate ou noexpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="9739e-207">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType Url -Action Block -Entries ~contoso.com
```

```powershell
New-TenantAllowBlockListItem -ListType FileHash -Action Allow -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="9739e-208">Cet exemple ajoute une entrée d’autorisation de fichier pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="9739e-208">This example adds a file allow entry for the specified files that never expires.</span></span>

<span data-ttu-id="9739e-209">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9739e-209">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-210">Utiliser PowerShell pour afficher les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-210">Use PowerShell to view URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9739e-211">Pour afficher les entrées d’URL et de fichier dans la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9739e-211">To view URL and file entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <Url | FileHash> [-Entry <URLValue | FileHashValue>] [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration]
```

<span data-ttu-id="9739e-212">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="9739e-212">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Action Block
```

<span data-ttu-id="9739e-213">Cet exemple renvoie des informations sur la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9739e-213">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="9739e-214">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9739e-214">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-url-and-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-215">Utiliser PowerShell pour modifier les entrées d’URL et de fichiers dans la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-215">Use PowerShell to modify URL and file entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="9739e-216">Vous ne pouvez pas modifier la valeur de l’URL ou du fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="9739e-216">You can't modify the URL or file value itself.</span></span> <span data-ttu-id="9739e-217">Au lieu de cela, vous devez supprimer l’entrée et la recréer.</span><span class="sxs-lookup"><span data-stu-id="9739e-217">Instead, you need to delete the entry and recreate it.</span></span>

<span data-ttu-id="9739e-218">Pour modifier les entrées d’URL et de fichier dans la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9739e-218">To modify URL and file entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN"> [-Action <Allow | Block>] [-ExpirationDate <DateTime>] [-NoExpiration] [-Notes <String>]
```

<span data-ttu-id="9739e-219">Cet exemple montre comment modifier la date d’expiration de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9739e-219">This example changes the expiration date of the specified entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate (Get-Date "5/30/2020 9:30 AM").ToUniversalTime()
```

<span data-ttu-id="9739e-220">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9739e-220">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-url-and-file-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-221">Utiliser PowerShell pour supprimer les entrées d’URL et de fichier de la liste des clients autorisés/bloqués</span><span class="sxs-lookup"><span data-stu-id="9739e-221">Use PowerShell to remove URL and file entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="9739e-222">Pour supprimer les entrées d’URL et de fichier de la liste des clients autorisés/bloqués, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9739e-222">To remove URL and file entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <Url | FileHash> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="9739e-223">Cet exemple supprime l’entrée d’URL spécifiée de la liste des clients bloqués/bloqués.</span><span class="sxs-lookup"><span data-stu-id="9739e-223">This example removes the specified URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="9739e-224">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="9739e-224">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](https://docs.microsoft.com/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="9739e-225">Syntaxe d’URL de la liste d’autorisation/de blocage de client</span><span class="sxs-lookup"><span data-stu-id="9739e-225">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="9739e-226">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="9739e-226">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="9739e-227">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="9739e-227">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="9739e-228">Unicode n’est pas pris en charge, mais Punycode est.</span><span class="sxs-lookup"><span data-stu-id="9739e-228">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="9739e-229">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="9739e-229">Hostnames are allowed if all of the following statements are true:</span></span>

  - <span data-ttu-id="9739e-230">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="9739e-230">The hostname contains a period.</span></span>
  - <span data-ttu-id="9739e-231">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="9739e-231">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="9739e-232">Il y a au moins deux caractères à droite de la période.</span><span class="sxs-lookup"><span data-stu-id="9739e-232">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="9739e-233">Par exemple, `t.co` est autorisé ou n’est `.com` `contoso.` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="9739e-233">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="9739e-234">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="9739e-234">Subpaths are not implied.</span></span>

  <span data-ttu-id="9739e-235">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="9739e-235">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="9739e-236">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-236">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="9739e-237">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="9739e-237">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="9739e-238">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="9739e-238">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="9739e-239">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9739e-239">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="9739e-240">Par exemple, `contoso.com/*` est autorisé ou n’est `contoso.com*` `contoso.com/ab*` pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="9739e-240">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="9739e-241">Tous les sous-chemins ne sont pas implicitement par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="9739e-241">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="9739e-242">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="9739e-242">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="9739e-243">`*.com*`n’est pas valide (ce n’est pas un domaine pouvant être résolu et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="9739e-243">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="9739e-244">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="9739e-244">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="9739e-245">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9739e-245">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="9739e-246">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="9739e-246">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="9739e-247">Par exemple `~contoso.com` `contoso.com` , inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="9739e-247">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="9739e-248">Les entrées d’URL qui contiennent des protocoles (par exemple,, `http://` `https://` ou `ftp://` ) échouent, car les entrées d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="9739e-248">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="9739e-249">Un nom d’utilisateur ou un mot de passe n’est pas pris en charge ou obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9739e-249">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="9739e-250">Les guillemets ('ou ") sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9739e-250">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="9739e-251">Une URL doit inclure toutes les redirections, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9739e-251">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="9739e-252">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="9739e-252">URL entry scenarios</span></span>

<span data-ttu-id="9739e-253">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9739e-253">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="9739e-254">Scénario : pas de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="9739e-254">Scenario: No wildcards</span></span>

<span data-ttu-id="9739e-255">**Entrée**:`contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9739e-255">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="9739e-256">**Correspondance autorisée**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-256">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="9739e-257">**Ne pas faire correspondre**:</span><span class="sxs-lookup"><span data-stu-id="9739e-257">**Allow not matched**:</span></span>

  - <span data-ttu-id="9739e-258">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-258">abc-contoso.com</span></span>
  - <span data-ttu-id="9739e-259">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9739e-259">contoso.com/a</span></span>
  - <span data-ttu-id="9739e-260">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-260">payroll.contoso.com</span></span>
  - <span data-ttu-id="9739e-261">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-261">test.com/contoso.com</span></span>
  - <span data-ttu-id="9739e-262">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-262">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="9739e-263">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-263">www.contoso.com</span></span>
  - <span data-ttu-id="9739e-264">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="9739e-264">www.contoso.com/q=a@contoso.com</span></span>
  
- <span data-ttu-id="9739e-265">**Correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-265">**Block match**:</span></span>

  - <span data-ttu-id="9739e-266">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-266">contoso.com</span></span>
  - <span data-ttu-id="9739e-267">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9739e-267">contoso.com/a</span></span>
  - <span data-ttu-id="9739e-268">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-268">payroll.contoso.com</span></span>
  - <span data-ttu-id="9739e-269">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-269">test.com/contoso.com</span></span>
  - <span data-ttu-id="9739e-270">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-270">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="9739e-271">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-271">www.contoso.com</span></span>
  - <span data-ttu-id="9739e-272">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="9739e-272">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="9739e-273">**Bloc sans correspondance**: ABC-contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-273">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="9739e-274">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="9739e-274">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="9739e-275">**Entrée**:`*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9739e-275">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="9739e-276">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-276">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-277">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-277">www.contoso.com</span></span>
  - <span data-ttu-id="9739e-278">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-278">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9739e-279">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9739e-279">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9739e-280">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-280">123contoso.com</span></span>
  - <span data-ttu-id="9739e-281">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-281">contoso.com</span></span>
  - <span data-ttu-id="9739e-282">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-282">test.com/contoso.com</span></span>
  - <span data-ttu-id="9739e-283">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9739e-283">www.contoso.com/abc</span></span>
  
#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="9739e-284">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9739e-284">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="9739e-285">**Entrée**:`contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="9739e-285">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="9739e-286">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-286">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-287">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="9739e-287">contoso.com/a/b</span></span>
  - <span data-ttu-id="9739e-288">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9739e-288">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9739e-289">contoso. com/a/ ? q = joe@t. com</span><span class="sxs-lookup"><span data-stu-id="9739e-289">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="9739e-290">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9739e-290">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9739e-291">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-291">contoso.com</span></span>
  - <span data-ttu-id="9739e-292">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9739e-292">contoso.com/a</span></span>
  - <span data-ttu-id="9739e-293">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-293">www.contoso.com</span></span>
  - <span data-ttu-id="9739e-294">www. contoso. com/q = a@contoso. com</span><span class="sxs-lookup"><span data-stu-id="9739e-294">www.contoso.com/q=a@contoso.com</span></span>
  
#### <a name="scenario-left-tilde"></a><span data-ttu-id="9739e-295">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="9739e-295">Scenario: Left tilde</span></span>

<span data-ttu-id="9739e-296">**Entrée**:`~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="9739e-296">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="9739e-297">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-297">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-298">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-298">contoso.com</span></span>
  - <span data-ttu-id="9739e-299">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-299">www.contoso.com</span></span>
  - <span data-ttu-id="9739e-300">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-300">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9739e-301">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9739e-301">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9739e-302">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-302">123contoso.com</span></span>
  - <span data-ttu-id="9739e-303">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9739e-303">contoso.com/abc</span></span>
  - <span data-ttu-id="9739e-304">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="9739e-304">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="9739e-305">Scénario : suffixe de caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="9739e-305">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="9739e-306">**Entrée**:`contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="9739e-306">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="9739e-307">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-307">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-308">contoso. com/ ? q = whatever@fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="9739e-308">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="9739e-309">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9739e-309">contoso.com/a</span></span>
  - <span data-ttu-id="9739e-310">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9739e-310">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9739e-311">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="9739e-311">contoso.com/ab</span></span>
  - <span data-ttu-id="9739e-312">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9739e-312">contoso.com/b</span></span>
  - <span data-ttu-id="9739e-313">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="9739e-313">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="9739e-314">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="9739e-314">contoso.com/ba</span></span>

- <span data-ttu-id="9739e-315">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-315">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="9739e-316">Scénario : sous-domaine du caractère générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="9739e-316">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="9739e-317">**Entrée**:`*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="9739e-317">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="9739e-318">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-318">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-319">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="9739e-319">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="9739e-320">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="9739e-320">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="9739e-321">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9739e-321">www.contoso.com/a</span></span>
  - <span data-ttu-id="9739e-322">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="9739e-322">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="9739e-323">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="9739e-323">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="9739e-324">**N’autoriser ni correspondance** , ni **bloc sans correspondance**: contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9739e-324">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="9739e-325">Scénario : tilde gauche et droit</span><span class="sxs-lookup"><span data-stu-id="9739e-325">Scenario: Left and right tilde</span></span>

<span data-ttu-id="9739e-326">**Entrée**:`~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="9739e-326">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="9739e-327">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-327">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-328">contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-328">contoso.com</span></span>
  - <span data-ttu-id="9739e-329">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="9739e-329">contoso.com/a</span></span>
  - <span data-ttu-id="9739e-330">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-330">www.contoso.com</span></span>
  - <span data-ttu-id="9739e-331">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="9739e-331">www.contoso.com/b</span></span>
  - <span data-ttu-id="9739e-332">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-332">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="9739e-333">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9739e-333">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9739e-334">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-334">123contoso.com</span></span>
  - <span data-ttu-id="9739e-335">contoso.org</span><span class="sxs-lookup"><span data-stu-id="9739e-335">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="9739e-336">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="9739e-336">Scenario: IP address</span></span>

<span data-ttu-id="9739e-337">**Entrée**:`1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="9739e-337">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="9739e-338">**Autoriser la correspondance** et la **correspondance de bloc**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9739e-338">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="9739e-339">**N’autoriser ni correspondance** , ni **bloc sans correspondance**:</span><span class="sxs-lookup"><span data-stu-id="9739e-339">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="9739e-340">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="9739e-340">1.2.3.4/a</span></span>
  - <span data-ttu-id="9739e-341">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="9739e-341">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="9739e-342">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="9739e-342">IP address with right wildcard</span></span>

<span data-ttu-id="9739e-343">**Entrée**:`1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="9739e-343">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="9739e-344">**Autoriser** la correspondance et la **correspondance de bloc**:</span><span class="sxs-lookup"><span data-stu-id="9739e-344">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="9739e-345">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="9739e-345">1.2.3.4/b</span></span>
  - <span data-ttu-id="9739e-346">1.2.3.4/bAAAA</span><span class="sxs-lookup"><span data-stu-id="9739e-346">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="9739e-347">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="9739e-347">Examples of invalid entries</span></span>

<span data-ttu-id="9739e-348">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="9739e-348">The following entries are invalid:</span></span>

- <span data-ttu-id="9739e-349">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="9739e-349">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="9739e-350">contoso</span><span class="sxs-lookup"><span data-stu-id="9739e-350">contoso</span></span>
  - <span data-ttu-id="9739e-351">\*contoso.\*</span><span class="sxs-lookup"><span data-stu-id="9739e-351">\*.contoso.\*</span></span>
  - <span data-ttu-id="9739e-352">\*. com</span><span class="sxs-lookup"><span data-stu-id="9739e-352">\*.com</span></span>
  - <span data-ttu-id="9739e-353">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="9739e-353">\*.pdf</span></span>

- <span data-ttu-id="9739e-354">**Caractères génériques sur le texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="9739e-354">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="9739e-355">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="9739e-355">\*contoso.com</span></span>
  - <span data-ttu-id="9739e-356">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="9739e-356">contoso.com\*</span></span>
  - <span data-ttu-id="9739e-357">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9739e-357">\*1.2.3.4</span></span>
  - <span data-ttu-id="9739e-358">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="9739e-358">1.2.3.4\*</span></span>
  - <span data-ttu-id="9739e-359">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="9739e-359">contoso.com/a\*</span></span>
  - <span data-ttu-id="9739e-360">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="9739e-360">contoso.com/ab\*</span></span>

- <span data-ttu-id="9739e-361">**Adresses IP avec des ports**:</span><span class="sxs-lookup"><span data-stu-id="9739e-361">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="9739e-362">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="9739e-362">contoso.com:443</span></span>
  - <span data-ttu-id="9739e-363">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="9739e-363">abc.contoso.com:25</span></span>

- <span data-ttu-id="9739e-364">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="9739e-364">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="9739e-365">\*.\*</span><span class="sxs-lookup"><span data-stu-id="9739e-365">\*.\*</span></span>

- <span data-ttu-id="9739e-366">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="9739e-366">**Middle wildcards**:</span></span>

  - <span data-ttu-id="9739e-367">CONT \* so.com</span><span class="sxs-lookup"><span data-stu-id="9739e-367">conto\*so.com</span></span>
  - <span data-ttu-id="9739e-368">Conto ~ so. com</span><span class="sxs-lookup"><span data-stu-id="9739e-368">conto~so.com</span></span>

- <span data-ttu-id="9739e-369">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="9739e-369">**Double wildcards**</span></span>

  - <span data-ttu-id="9739e-370">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="9739e-370">contoso.com/\*\*</span></span>
  - <span data-ttu-id="9739e-371">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="9739e-371">contoso.com/\*/\*</span></span>
