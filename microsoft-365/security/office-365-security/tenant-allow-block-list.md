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
ms.openlocfilehash: 270e38d65857de2f4d06460fb3bb77f72a165ecf
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538962"
---
# <a name="manage-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-103">Gérer la liste Autoriser/Bloquer du client</span><span class="sxs-lookup"><span data-stu-id="37b2c-103">Manage the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="37b2c-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="37b2c-104">**Applies to**</span></span>
- [<span data-ttu-id="37b2c-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="37b2c-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="37b2c-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="37b2c-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="37b2c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37b2c-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
>
> <span data-ttu-id="37b2c-108">Les fonctionnalités décrites dans cet article sont en prévisualisation, peuvent faire l’objet de changements et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="37b2c-108">The features described in this article are in Preview, are subject to change, and are not available in all organizations.</span></span>  <span data-ttu-id="37b2c-109">Si votre organisation ne dispose pas des fonctionnalités d’usurpation d’informations décrites dans cet article, consultez l’ancienne expérience de gestion de l’usurpation d’adresse chez [Manage spoofof senders using the spoof intelligence policy and spoof intelligence insight in EOP](walkthrough-spoof-intelligence-insight.md).</span><span class="sxs-lookup"><span data-stu-id="37b2c-109">If your organization does not have the spoof features as described in this article, see the older spoof management experience at [Manage spoofed senders using the spoof intelligence policy and spoof intelligence insight in EOP](walkthrough-spoof-intelligence-insight.md).</span></span>
>
> <span data-ttu-id="37b2c-110">Vous ne pouvez pas **configurer d’URL** ou d’éléments de fichier autorisés dans la liste d’adresses client autorisées/bloqués pour le moment.</span><span class="sxs-lookup"><span data-stu-id="37b2c-110">You can't **configure** allowed URL or file items in the Tenant Allow/Block List at this time.</span></span>

<span data-ttu-id="37b2c-111">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, vous pouvez ne pas être d’accord avec le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="37b2c-111">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="37b2c-112">Par exemple, un bon message peut être marqué comme mauvais (faux positif) ou un message erroné peut être autorisé (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="37b2c-112">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="37b2c-113">La liste des locataires autoriser/bloquer dans le Centre de sécurité & conformité vous permet de remplacer manuellement les verdicts de filtrage Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="37b2c-113">The Tenant Allow/Block List in the Security & Compliance Center gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="37b2c-114">La liste d’adresses client autoriser/bloquer est utilisée pendant le flux de messagerie et au moment des clics de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37b2c-114">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="37b2c-115">Vous pouvez spécifier les types de substitutions suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-115">You can specify the following types of overrides:</span></span>

- <span data-ttu-id="37b2c-116">URL à bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-116">URLs to block.</span></span>
- <span data-ttu-id="37b2c-117">Fichiers à bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-117">Files to block.</span></span>
- <span data-ttu-id="37b2c-118">Domaines d’expéditeur de courrier en masse à autoriser.</span><span class="sxs-lookup"><span data-stu-id="37b2c-118">Bulk mail sender domains to allow.</span></span> <span data-ttu-id="37b2c-119">Pour plus d’informations sur le courrier en nombre, le niveau de confiance en bloc (BCL) et le filtrage des messages en bloc par des stratégies anti-courrier indésirable, voir Le niveau de réclamation en bloc [(BCL) dans EOP.](bulk-complaint-level-values.md)</span><span class="sxs-lookup"><span data-stu-id="37b2c-119">For more information about bulk mail, the bulk confidence level (BCL), and bulk mail filtering by anti-spam policies, see [Bulk complaint level (BCL) in EOP](bulk-complaint-level-values.md).</span></span>
- <span data-ttu-id="37b2c-120">Expéditeurs usurpés à autoriser ou bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-120">Spoofed senders to allow or block.</span></span> <span data-ttu-id="37b2c-121">Si vous remplacez le verdict [](learn-about-spoof-intelligence.md)d’usurpation d’informations sur l’usurpation d’adresse, l’expéditeur  usurpé devient une entrée d’accès ou de blocage manuelle qui apparaît uniquement sous l’onglet Usurpation d’adresse dans la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-121">If you override the allow or block verdict in the [spoof intelligence insight](learn-about-spoof-intelligence.md), the spoofed sender becomes a manual allow or block entry that only appears on the **Spoof** tab in the Tenant Allow/Block List.</span></span> <span data-ttu-id="37b2c-122">Vous pouvez également créer manuellement des entrées d’autoriser ou de bloquer des expéditeurs usurpés ici avant qu’ils ne sont détectés par la veille contre l’usurpation d’adresses.</span><span class="sxs-lookup"><span data-stu-id="37b2c-122">You can also manually create allow or block entries for spoofed senders here before they're detected by spoof intelligence.</span></span>

<span data-ttu-id="37b2c-123">Cet article explique comment configurer des entrées dans la liste d’adresses client autoriser/bloquer dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="37b2c-123">This article describes how to configure entries in the Tenant Allow/Block List in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="37b2c-124">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="37b2c-124">What do you need to know before you begin?</span></span>

- <span data-ttu-id="37b2c-125">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="37b2c-125">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="37b2c-126">Pour aller directement à la page Liste **d’accueil/de** blocage du client, utilisez <https://protection.office.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="37b2c-126">To go directly to the **Tenant Allow/Block List** page, use <https://protection.office.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="37b2c-127">Vous spécifiez des fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="37b2c-127">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="37b2c-128">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-128">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```console
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="37b2c-129">Un exemple de valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="37b2c-129">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="37b2c-130">Les valeurs de hachage perceptif (pHash) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="37b2c-130">Perceptual hash (pHash) values are not supported.</span></span>

- <span data-ttu-id="37b2c-131">Les valeurs d’URL disponibles sont décrites dans la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) de la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="37b2c-131">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

- <span data-ttu-id="37b2c-132">La liste d’adresses client autorise un maximum de 500 entrées pour les URL et 500 entrées pour les hâchés de fichiers.</span><span class="sxs-lookup"><span data-stu-id="37b2c-132">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="37b2c-133">Le nombre maximal de caractères pour chaque entrée est :</span><span class="sxs-lookup"><span data-stu-id="37b2c-133">The maximum number of characters for each entry is:</span></span>
  - <span data-ttu-id="37b2c-134">Hèmes de fichier = 64</span><span class="sxs-lookup"><span data-stu-id="37b2c-134">File hashes = 64</span></span>
  - <span data-ttu-id="37b2c-135">URL = 250</span><span class="sxs-lookup"><span data-stu-id="37b2c-135">URL = 250</span></span>

- <span data-ttu-id="37b2c-136">Une entrée doit être active dans les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="37b2c-136">An entry should be active within 30 minutes.</span></span>

- <span data-ttu-id="37b2c-137">Par défaut, les entrées de la liste d’inscriptions au client sont expirées au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="37b2c-137">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="37b2c-138">Vous pouvez spécifier une date ou les définir pour qu’elles n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="37b2c-138">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="37b2c-139">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="37b2c-139">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="37b2c-140">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="37b2c-140">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="37b2c-141">Des autorisations doivent vous avoir été attribuées dans Exchange Online pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="37b2c-141">You need to be assigned permissions in Exchange Online before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="37b2c-142">**URL, fichiers et autoriser les expéditeurs en bloc**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-142">**URLs, files, and allow bulk senders**:</span></span>
    - <span data-ttu-id="37b2c-143">Pour ajouter et supprimer des valeurs de la liste d’attente des locataires, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="37b2c-143">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
    - <span data-ttu-id="37b2c-144">Pour un accès en lecture seule à la liste d’accès  au  client autorisé/bloqué, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37b2c-144">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>
  - <span data-ttu-id="37b2c-145">**Usurpation :** l’une des combinaisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-145">**Spoofing**: One of the following combinations:</span></span>
    - <span data-ttu-id="37b2c-146">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-146">**Organization Management**</span></span>
    - <span data-ttu-id="37b2c-147">**Administrateur de sécurité** <u>et</u> **configuration en affichage seul** ou gestion de **l’organisation en affichage seul.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-147">**Security Administrator** <u>and</u> **View-Only Configuration** or **View-Only Organization Management**.</span></span>

  <span data-ttu-id="37b2c-148">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="37b2c-148">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="37b2c-149">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="37b2c-149">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="37b2c-150">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="37b2c-150">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="37b2c-151">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="37b2c-151">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-security--compliance-center-to-create-block-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-152">Utiliser le Centre de sécurité & conformité pour créer des entrées d’URL de blocage dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-152">Use the Security & Compliance Center to create block URL entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="37b2c-153">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-153">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-154">Dans la page **Liste d’adresses** client autoriser/bloquer, vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Bloquer**</span><span class="sxs-lookup"><span data-stu-id="37b2c-154">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Block**</span></span>

3. <span data-ttu-id="37b2c-155">Dans le **volant Bloquer les URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-155">In the **Block URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="37b2c-156">**Ajouter des URL à bloquer :** entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="37b2c-156">**Add URLs to block**: Enter one URL per line, up to a maximum of 20.</span></span> <span data-ttu-id="37b2c-157">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) pour la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="37b2c-157">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

   - <span data-ttu-id="37b2c-158">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-158">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="37b2c-159">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="37b2c-159">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

       <span data-ttu-id="37b2c-160">ou</span><span class="sxs-lookup"><span data-stu-id="37b2c-160">or</span></span>

     - <span data-ttu-id="37b2c-161">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="37b2c-161">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="37b2c-163">.</span><span class="sxs-lookup"><span data-stu-id="37b2c-163">.</span></span>

   - <span data-ttu-id="37b2c-164">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="37b2c-164">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="37b2c-165">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-165">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-block-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-166">Utiliser le Centre de sécurité & conformité pour créer des entrées de fichiers bloqués dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="37b2c-166">Use the Security & Compliance Center to create block file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="37b2c-167">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-167">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-168">Dans la page **Client Autoriser/Bloquer la liste,** sélectionnez l’onglet **Fichiers,** puis cliquez sur **Bloquer.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-168">On the **Tenant Allow/Block List** page, select the **Files** tab, and then click **Block**.</span></span>

3. <span data-ttu-id="37b2c-169">Dans la **zone Ajouter des fichiers pour bloquer** le flyout qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-169">In the **Add files to block** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="37b2c-170">**Ajouter des hachages de fichier**: entrez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="37b2c-170">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="37b2c-171">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-171">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="37b2c-172">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="37b2c-172">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="37b2c-173">ou</span><span class="sxs-lookup"><span data-stu-id="37b2c-173">or</span></span>

     - <span data-ttu-id="37b2c-174">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="37b2c-174">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="37b2c-176">.</span><span class="sxs-lookup"><span data-stu-id="37b2c-176">.</span></span>

   - <span data-ttu-id="37b2c-177">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="37b2c-177">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="37b2c-178">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-178">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-allow-bulk-mail-sender-domain-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-179">Utiliser le Centre de sécurité & conformité pour créer des entrées de domaine d’expéditeur de courrier en nombre dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-179">Use the Security & Compliance Center to create allow bulk mail sender domain entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="37b2c-180">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-180">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-181">Dans la page Liste d’adresses client **autoriser/bloquer,** sélectionnez l’onglet Domaines de l’expéditeur pour le contournement **BCL,** puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-181">On the **Tenant Allow/Block List** page, select the **Sender domains for BCL bypass** tab, and then click **Add**.</span></span>

3. <span data-ttu-id="37b2c-182">Dans le **programme volant Ajouter un domaine d’expéditeur** pour le contournement BCL qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-182">In the **Add sender domain for BCL bypass** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="37b2c-183">**Ajouter des domaines d’expéditeur pour le** contournement BCL : entrez un domaine source de courrier en nombre par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="37b2c-183">**Add sender domains for BCL bypass**: Enter one source domain of good bulk mail per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="37b2c-184">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-184">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="37b2c-185">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="37b2c-185">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="37b2c-186">ou</span><span class="sxs-lookup"><span data-stu-id="37b2c-186">or</span></span>

     - <span data-ttu-id="37b2c-187">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="37b2c-187">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="37b2c-189">.</span><span class="sxs-lookup"><span data-stu-id="37b2c-189">.</span></span>

4. <span data-ttu-id="37b2c-190">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-190">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-create-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-191">Utiliser le Centre de sécurité & conformité pour créer des entrées d’expéditeurs usurpés ou autoriser ou bloquer dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-191">Use the Security & Compliance Center to create allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-192">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="37b2c-192">**Notes**:</span></span>

- <span data-ttu-id="37b2c-193">Seule la _combinaison_ de l’utilisateur usurpé et de l’infrastructure d’envoi, telle que définie dans la paire de domaines, est spécifiquement autorisée ou bloquée à l’usurpation. </span><span class="sxs-lookup"><span data-stu-id="37b2c-193">Only the _combination_ of the spoofed user _and_ the sending infrastructure as defined in the domain pair is specifically allowed or blocked from spoofing.</span></span>
- <span data-ttu-id="37b2c-194">Lorsque vous configurez une entrée d’autoriser ou de bloquer une paire de domaines, les messages de cette paire de domaines n’apparaissent plus dans l’aperçu de l’usurpation d’intelligence.</span><span class="sxs-lookup"><span data-stu-id="37b2c-194">When you configure an allow or block entry for a domain pair, messages from that domain pair no longer appear in the spoof intelligence insight.</span></span>
- <span data-ttu-id="37b2c-195">Les entrées des expéditeurs usurpés n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="37b2c-195">Entries for spoofed senders never expire.</span></span>

1. <span data-ttu-id="37b2c-196">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-196">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-197">Dans la page **Client autoriser/Bloquer la liste,** sélectionnez l’onglet **Usurpation** d’informations, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-197">On the **Tenant Allow/Block List** page, select the **Spoofing** tab, and then click **Add**.</span></span>

3. <span data-ttu-id="37b2c-198">Dans le **volant Ajouter de nouvelles paires de domaines** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-198">In the **Add new domain pairs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="37b2c-199">**Ajoutez de nouvelles paires de domaines avec des caractères génériques**: entrez une paire de domaines par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="37b2c-199">**Add new domain pairs with wildcards**: Enter one domain pair per line, up to a maximum of 20.</span></span> <span data-ttu-id="37b2c-200">Pour plus d’informations sur la syntaxe des entrées d’expéditeur usurpées, voir la syntaxe de paire domaine pour les entrées d’expéditeur usurpées dans la section Client [Autoriser/Bloquer](#domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list) la liste plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="37b2c-200">For details about the syntax for spoofed sender entries, see the [Domain pair syntax for spoofed sender entries in the Tenant Allow/Block List](#domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list) section later in this article.</span></span>

   - <span data-ttu-id="37b2c-201">**Type d’usurpation**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-201">**Spoof type**: Select one of the following values:</span></span>
     - <span data-ttu-id="37b2c-202">**Interne**: l’expéditeur usurpé se trouve dans un domaine appartenant à votre organisation [(un domaine accepté).](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)</span><span class="sxs-lookup"><span data-stu-id="37b2c-202">**Internal**: The spoofed sender is in a domain that belongs to your organization (an [accepted domain](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)).</span></span>
     - <span data-ttu-id="37b2c-203">**Externe**: l’expéditeur usurpé se trouve dans un domaine externe.</span><span class="sxs-lookup"><span data-stu-id="37b2c-203">**External**: The spoofed sender is in an external domain.</span></span>

   - <span data-ttu-id="37b2c-204">**Action**: **sélectionnez Autoriser** ou **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-204">**Action**: Select **Allow** or **Block**.</span></span>

4. <span data-ttu-id="37b2c-205">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-205">When you're finished, click **Add**.</span></span>

## <a name="use-the-security--compliance-center-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-206">Utiliser le Centre de sécurité & conformité pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="37b2c-206">Use the Security & Compliance Center to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="37b2c-207">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-207">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-208">Sélectionnez l’onglet de votre choix.</span><span class="sxs-lookup"><span data-stu-id="37b2c-208">Select the tab you want.</span></span> <span data-ttu-id="37b2c-209">Les colonnes disponibles dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="37b2c-209">The columns that are available depend on the tab you selected:</span></span>

   - <span data-ttu-id="37b2c-210">**URL**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-210">**URLs**:</span></span>
     - <span data-ttu-id="37b2c-211">**Valeur**: URL.</span><span class="sxs-lookup"><span data-stu-id="37b2c-211">**Value**: The URL.</span></span>
     - <span data-ttu-id="37b2c-212">**Action**: La valeur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-212">**Action**: The value **Block**.</span></span>
     - <span data-ttu-id="37b2c-213">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="37b2c-213">**Last updated date**</span></span>
     - <span data-ttu-id="37b2c-214">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="37b2c-214">**Expiration date**</span></span>
     - <span data-ttu-id="37b2c-215">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="37b2c-215">**Note**</span></span>

   - <span data-ttu-id="37b2c-216">**Files**</span><span class="sxs-lookup"><span data-stu-id="37b2c-216">**Files**</span></span>
     - <span data-ttu-id="37b2c-217">**Valeur**: hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="37b2c-217">**Value**: The file hash.</span></span>
     - <span data-ttu-id="37b2c-218">**Action**: La valeur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-218">**Action**: The value **Block**.</span></span>
     - <span data-ttu-id="37b2c-219">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="37b2c-219">**Last updated date**</span></span>
     - <span data-ttu-id="37b2c-220">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="37b2c-220">**Expiration date**</span></span>
     - <span data-ttu-id="37b2c-221">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="37b2c-221">**Note**</span></span>

   - <span data-ttu-id="37b2c-222">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-222">**Sender domains for BCL bypass**</span></span>
     - <span data-ttu-id="37b2c-223">**Valeur**: domaine de l’expéditeur du courrier en masse.</span><span class="sxs-lookup"><span data-stu-id="37b2c-223">**Value**: The bulk mail sender's domain.</span></span>
     - <span data-ttu-id="37b2c-224">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="37b2c-224">**Last updated date**</span></span>
     - <span data-ttu-id="37b2c-225">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="37b2c-225">**Expiration date**</span></span>

   - <span data-ttu-id="37b2c-226">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-226">**Spoofing**</span></span>
     - <span data-ttu-id="37b2c-227">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="37b2c-227">**Spoofed user**</span></span>
     - <span data-ttu-id="37b2c-228">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="37b2c-228">**Sending infrastructure**</span></span>
     - <span data-ttu-id="37b2c-229">**Type d’usurpation**: valeur **Interne** ou **Externe.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-229">**Spoof type**: The value **Internal** or **External**.</span></span>
     - <span data-ttu-id="37b2c-230">**Action**: la valeur **Bloquer ou** **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-230">**Action**: The value **Block** or **Allow**.</span></span>

   <span data-ttu-id="37b2c-231">Vous pouvez cliquer sur un en-tête de colonne pour trier par ordre croissant ou décroit.</span><span class="sxs-lookup"><span data-stu-id="37b2c-231">You can click on a column heading to sort in ascending or descending order.</span></span>

   <span data-ttu-id="37b2c-232">Vous pouvez cliquer sur **Grouper** pour grouper les résultats.</span><span class="sxs-lookup"><span data-stu-id="37b2c-232">You can click **Group** to group the results.</span></span> <span data-ttu-id="37b2c-233">Les valeurs disponibles dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="37b2c-233">The values that are available depend on the tab you selected:</span></span>

   - <span data-ttu-id="37b2c-234">**URL : vous** pouvez grouper les résultats par **action.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-234">**URLs**: You can group the results by **Action**.</span></span>
   - <span data-ttu-id="37b2c-235">**Fichiers**: vous pouvez grouper les résultats par **action.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-235">**Files**: You can group the results by **Action**.</span></span>
   - <span data-ttu-id="37b2c-236">**Domaines des expéditeurs pour le contournement BCL :** **le groupe** n’est pas disponible sous cet onglet.</span><span class="sxs-lookup"><span data-stu-id="37b2c-236">**Sender domains for BCL bypass**: **Group** is not available on this tab.</span></span>
   - <span data-ttu-id="37b2c-237">**Usurpation :** vous pouvez grouper les résultats par **action** ou **type d’usurpation.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-237">**Spoofing**: You can group the results by **Action** or **Spoof type**.</span></span>

   <span data-ttu-id="37b2c-238">Cliquez **sur** Rechercher, entrez une partie ou l’ensemble d’une valeur, puis appuyez sur Entrée pour trouver une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="37b2c-238">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="37b2c-239">Lorsque vous avez terminé, cliquez sur **Effacer l’icône** ![ de recherche Effacer la ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) recherche.</span><span class="sxs-lookup"><span data-stu-id="37b2c-239">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

   <span data-ttu-id="37b2c-240">Cliquez **sur Filtrer** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="37b2c-240">Click **Filter** to filter the results.</span></span> <span data-ttu-id="37b2c-241">Les valeurs disponibles dans le flyout **Filter** qui s’affiche dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="37b2c-241">The values that are available in **Filter** flyout that appears depend on the tab you selected:</span></span>

   - <span data-ttu-id="37b2c-242">**URL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-242">**URLs**</span></span>
     - <span data-ttu-id="37b2c-243">**Action**</span><span class="sxs-lookup"><span data-stu-id="37b2c-243">**Action**</span></span>
     - <span data-ttu-id="37b2c-244">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="37b2c-244">**Never expire**</span></span>
     - <span data-ttu-id="37b2c-245">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="37b2c-245">**Last updated date**</span></span>
     - <span data-ttu-id="37b2c-246">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="37b2c-246">**Expiration date**</span></span>

   - <span data-ttu-id="37b2c-247">**Files**</span><span class="sxs-lookup"><span data-stu-id="37b2c-247">**Files**</span></span>
     - <span data-ttu-id="37b2c-248">**Action**</span><span class="sxs-lookup"><span data-stu-id="37b2c-248">**Action**</span></span>
     - <span data-ttu-id="37b2c-249">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="37b2c-249">**Never expire**</span></span>
     - <span data-ttu-id="37b2c-250">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="37b2c-250">**Last updated date**</span></span>
     - <span data-ttu-id="37b2c-251">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="37b2c-251">**Expiration date**</span></span>

   - <span data-ttu-id="37b2c-252">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-252">**Sender domains for BCL bypass**</span></span>
     - <span data-ttu-id="37b2c-253">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="37b2c-253">**Never expire**</span></span>
     - <span data-ttu-id="37b2c-254">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="37b2c-254">**Last updated date**</span></span>
     - <span data-ttu-id="37b2c-255">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="37b2c-255">**Expiration date**</span></span>

   - <span data-ttu-id="37b2c-256">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-256">**Spoofing**</span></span>
     - <span data-ttu-id="37b2c-257">**Action**</span><span class="sxs-lookup"><span data-stu-id="37b2c-257">**Action**</span></span>
     - <span data-ttu-id="37b2c-258">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-258">**Spoof type**</span></span>

   <span data-ttu-id="37b2c-259">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-259">When you're finished, click **Apply**.</span></span> <span data-ttu-id="37b2c-260">Pour effacer les filtres existants,  cliquez sur **Filtrer** et dans le volant de filtre qui s’affiche, cliquez **sur Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-260">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-security--compliance-center-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-261">Utiliser le Centre de sécurité & conformité pour modifier des entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="37b2c-261">Use the Security & Compliance Center to modify entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="37b2c-262">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-262">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-263">Sélectionnez l’onglet qui contient le type d’entrée à modifier :</span><span class="sxs-lookup"><span data-stu-id="37b2c-263">Select the tab that contains the type of entry that you want to modify:</span></span>
   - <span data-ttu-id="37b2c-264">**URL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-264">**URLs**</span></span>
   - <span data-ttu-id="37b2c-265">**Files**</span><span class="sxs-lookup"><span data-stu-id="37b2c-265">**Files**</span></span>
   - <span data-ttu-id="37b2c-266">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-266">**Sender domains for BCL bypass**</span></span>
   - <span data-ttu-id="37b2c-267">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-267">**Spoofing**</span></span>

3. <span data-ttu-id="37b2c-268">Sélectionnez l’entrée à modifier, puis cliquez **sur** Modifier ![ l’icône ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="37b2c-268">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span> <span data-ttu-id="37b2c-269">Les valeurs que vous pouvez modifier dans le volant qui s’affiche dépendent de l’onglet que vous avez sélectionné à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="37b2c-269">The values that you are able to modify in the flyout that appears depend on the tab you selected in the previous step:</span></span>

   - <span data-ttu-id="37b2c-270">**URL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-270">**URLs**</span></span>
     - <span data-ttu-id="37b2c-271">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="37b2c-271">**Never expire** and/or expiration date.</span></span>
     - <span data-ttu-id="37b2c-272">**Note facultative**</span><span class="sxs-lookup"><span data-stu-id="37b2c-272">**Optional note**</span></span>

   - <span data-ttu-id="37b2c-273">**Files**</span><span class="sxs-lookup"><span data-stu-id="37b2c-273">**Files**</span></span>
     - <span data-ttu-id="37b2c-274">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="37b2c-274">**Never expire** and/or expiration date.</span></span>
     - <span data-ttu-id="37b2c-275">**Note facultative**</span><span class="sxs-lookup"><span data-stu-id="37b2c-275">**Optional note**</span></span>

   - <span data-ttu-id="37b2c-276">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-276">**Sender domains for BCL bypass**</span></span>
     - <span data-ttu-id="37b2c-277">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="37b2c-277">**Never expire** and/or expiration date.</span></span>

   - <span data-ttu-id="37b2c-278">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-278">**Spoofing**</span></span>
     - <span data-ttu-id="37b2c-279">**Action**: vous pouvez modifier la valeur sur **Autoriser** ou **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-279">**Action**: You can change the value to **Allow** or **Block**.</span></span>

4. <span data-ttu-id="37b2c-280">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-280">When you're finished, click **Save**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-281">Utiliser le Centre de sécurité & conformité pour supprimer des entrées de la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="37b2c-281">Use the Security & Compliance Center to remove entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="37b2c-282">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="37b2c-282">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="37b2c-283">Sélectionnez l’onglet qui contient le type d’entrée à supprimer :</span><span class="sxs-lookup"><span data-stu-id="37b2c-283">Select the tab that contains the type of entry that you want to remove:</span></span>
   - <span data-ttu-id="37b2c-284">**URL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-284">**URLs**</span></span>
   - <span data-ttu-id="37b2c-285">**Files**</span><span class="sxs-lookup"><span data-stu-id="37b2c-285">**Files**</span></span>
   - <span data-ttu-id="37b2c-286">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="37b2c-286">**Sender domains for BCL bypass**</span></span>
   - <span data-ttu-id="37b2c-287">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="37b2c-287">**Spoofing**</span></span>

3. <span data-ttu-id="37b2c-288">Sélectionnez l’entrée à supprimer, puis cliquez **sur** Supprimer ![ l’icône ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-288">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="37b2c-289">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="37b2c-289">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-290">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-290">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-block-file-or-url-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-291">Utiliser PowerShell pour ajouter des entrées de bloc de fichier ou d’URL à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-291">Use PowerShell to add block file or URL entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-292">Pour ajouter des entrées de blocage de fichier ou d’URL dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-292">To add block file or URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <FileHash | Url> -Block -Entries "Value1","Value2",..."ValueN" <-ExpirationDate Date | -NoExpiration> [-Notes <String>]
```

<span data-ttu-id="37b2c-293">Cet exemple ajoute une entrée de fichier de blocage pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="37b2c-293">This example adds a block file entry for the specified files that never expires.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType FileHash -Block -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="37b2c-294">Cet exemple ajoute une entrée d’URL de bloc pour contoso.com et tous les sous-contoso.com (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="37b2c-294">This example adds a block URL entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="37b2c-295">Étant donné que nous n’avons pas utilisé les paramètres ExpirationDate ou NoExpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="37b2c-295">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Block -Entries ~contoso.com
```

<span data-ttu-id="37b2c-296">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-296">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-add-allow-bulk-mail-sender-domain-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-297">Utiliser PowerShell pour ajouter des entrées de domaine d’expéditeur de courrier en nombre à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-297">Use PowerShell to add allow bulk mail sender domain entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-298">Pour ajouter des entrées de domaine d’expéditeur de courrier en nombre dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-298">To add allow bulk mail sender domain entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType BulkSender -Block:$false -Entries "Value1","Value2",..."ValueN" <-ExpirationDate Date | -NoExpiration> [-Notes <String>]
```

<span data-ttu-id="37b2c-299">Cet exemple ajoute une entrée d’expéditeur en bloc autorisée pour le domaine spécifié qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="37b2c-299">This example adds an allowed bulk sender entry for the specified domain that never expires.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType BulkSender -Block:$false -Entries contosodailydeals.com
New-TenantAllowBlockListItems -ListType FileHash -Block -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="37b2c-300">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-300">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-add-allow-or-block-spoofed-sender-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-301">Utiliser PowerShell pour ajouter des entrées d’expéditeurs usurpés ou autoriser ou bloquer à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-301">Use PowerShell to add allow or block spoofed sender entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-302">Pour ajouter des entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-302">To add spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListSpoofItems -SpoofedUser <Domain | EmailAddress | *> -SendingInfrastructure <Domain | IPAddress/24> -SpoofType <External | Internal> -Action <Allow | Block>
```

<span data-ttu-id="37b2c-303">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListSpoofItems](/powershell/module/exchange/new-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-303">For detailed syntax and parameter information, see [New-TenantAllowBlockListSpoofItems](/powershell/module/exchange/new-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-view-block-file-or-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-304">Utiliser PowerShell pour afficher les entrées de bloc de fichiers ou d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-304">Use PowerShell to view block file or URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-305">Pour afficher les entrées de fichier ou d’URL bloqués dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-305">To view block file or URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <FileHash | URL> [-Entry <FileHashValue | URLValue>] [<-ExpirationDate Date | -NoExpiration>]
```

<span data-ttu-id="37b2c-306">Cet exemple renvoie des informations pour la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="37b2c-306">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="37b2c-307">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="37b2c-307">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Block
```

<span data-ttu-id="37b2c-308">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems.](/powershell/module/exchange/get-tenantallowblocklistitems)</span><span class="sxs-lookup"><span data-stu-id="37b2c-308">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-allow-bulk-mail-sender-domain-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-309">Utiliser PowerShell pour afficher les entrées de domaine d’expéditeur de courrier en nombre dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-309">Use PowerShell to view allow bulk mail sender domain entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-310">Pour afficher les entrées de domaine d’expéditeur de courrier en nombre dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-310">To view allow bulk mail sender domain entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType BulkSender [-Entry <BulkSenderDomainValue>] [<-ExpirationDate Date | -NoExpiration>]
```

<span data-ttu-id="37b2c-311">Cet exemple renvoie tous les domaines d’expéditeur de courrier en masse autorisés.</span><span class="sxs-lookup"><span data-stu-id="37b2c-311">This example returns all allowed bulk mail sender domains.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType BulkSender
```

<span data-ttu-id="37b2c-312">Cet exemple renvoie des informations pour le domaine d’expéditeur en bloc spécifié.</span><span class="sxs-lookup"><span data-stu-id="37b2c-312">This example returns information for the specified bulk sender domain.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "contosodailydeals.com"
```

<span data-ttu-id="37b2c-313">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems.](/powershell/module/exchange/get-tenantallowblocklistitems)</span><span class="sxs-lookup"><span data-stu-id="37b2c-313">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-314">Utiliser PowerShell pour afficher ou bloquer les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-314">Use PowerShell to view allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-315">Pour afficher les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-315">To view spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems [-Action <Allow | Block>] [-SpoofType <External | Internal>
```

<span data-ttu-id="37b2c-316">Cet exemple renvoie toutes les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-316">This example returns all spoofed sender entries in the Tenant Allow/Block List.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems
```

<span data-ttu-id="37b2c-317">Cet exemple renvoie toutes les entrées d’expéditeur usurpées qui sont internes.</span><span class="sxs-lookup"><span data-stu-id="37b2c-317">This example returns all allow spoofed sender entries that are internal.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems -Action Allow -SpoofType Internal
```

<span data-ttu-id="37b2c-318">Cet exemple renvoie toutes les entrées d’expéditeur usurpées bloquées qui sont externes.</span><span class="sxs-lookup"><span data-stu-id="37b2c-318">This example returns all blocked spoofed sender entries that are external.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems -Action Block -SpoofType External
```

<span data-ttu-id="37b2c-319">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-TenantAllowBlockListSpoofItems](/powershell/module/exchange/get-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-319">For detailed syntax and parameter information, see [Get-TenantAllowBlockListSpoofItems](/powershell/module/exchange/get-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-modify-block-file-and-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-320">Utiliser PowerShell pour modifier les entrées de blocage de fichiers et d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-320">Use PowerShell to modify block file and URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-321">Pour modifier les entrées de blocage de fichiers et d’URL dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-321">To modify block file and URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <FileHash | Url> -Ids <"Id1","Id2",..."IdN"> [<-ExpirationDate Date | -NoExpiration>] [-Notes <String>]
```

<span data-ttu-id="37b2c-322">Cet exemple modifie la date d’expiration de l’entrée d’URL de bloc spécifiée.</span><span class="sxs-lookup"><span data-stu-id="37b2c-322">This example changes the expiration date of the specified block URL entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate "5/30/2020"
```

<span data-ttu-id="37b2c-323">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-323">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-allow-bulk-mail-sender-domain-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-324">Utiliser PowerShell pour modifier les entrées de domaine d’expéditeur de courrier en nombre dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-324">Use PowerShell to modify allow bulk mail sender domain entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-325">Pour modifier autoriser les entrées de domaine d’expéditeur de courrier en nombre dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-325">To modify allow bulk mail sender domain entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType BulkSender -Ids <"Id1","Id2",..."IdN"> [<-ExpirationDate Date | -NoExpiration>] [-Notes <String>]
```

<span data-ttu-id="37b2c-326">Cet exemple modifie l’expiration de l’entrée de domaine d’expéditeur de courrier en nombre spécifiée pour qu’elle n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="37b2c-326">This example changes the expiration of the specified allow bulk mail sender domain entry to never expire.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType BulkSender -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -NoExpiration
```

<span data-ttu-id="37b2c-327">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems.](/powershell/module/exchange/get-tenantallowblocklistitems)</span><span class="sxs-lookup"><span data-stu-id="37b2c-327">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-328">Utiliser PowerShell pour modifier les entrées d’expéditeurs usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-328">Use PowerShell to modify allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-329">Pour modifier les entrées d’expéditeurs usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-329">To modify allow or block spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListSpoofItems -Ids <"Id1","Id2",..."IdN"> -Action <Allow | Block>
```

<span data-ttu-id="37b2c-330">Cet exemple modifie l’entrée de l’expéditeur usurpé de l’autoriser à la bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-330">This example changes spoofed sender entry from allow to block.</span></span>

```powershell
Set-TenantAllowBlockListItems -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -Action Block
```

<span data-ttu-id="37b2c-331">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListSpoofItems](/powershell/module/exchange/set-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-331">For detailed syntax and parameter information, see [Set-TenantAllowBlockListSpoofItems](/powershell/module/exchange/set-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-remove-bulk-mail-sender-domain-file-and-domain-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-332">Utiliser PowerShell pour supprimer les entrées de domaine, de fichier et de domaine de l’expéditeur de courrier en bloc de la liste d’adresses client</span><span class="sxs-lookup"><span data-stu-id="37b2c-332">Use PowerShell to remove bulk mail sender domain, file, and domain entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-333">Pour supprimer les entrées de domaine d’expéditeur de courrier en nombre, bloquer les entrées de fichier et bloquer les entrées d’URL de la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-333">To remove allow bulk mail sender domain entries, block file entries, and block URL entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <BulkSender | FileHash | Url> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="37b2c-334">Cet exemple supprime l’entrée d’URL de bloc spécifiée de la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="37b2c-334">This example removes the specified block URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="37b2c-335">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-335">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-allow-or-block-spoofed-sender-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-336">Utiliser PowerShell pour supprimer les entrées d’expéditeurs usurpées de la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-336">Use PowerShell to remove allow or block spoofed sender entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-337">Pour supprimer les entrées d’expéditeurs usurpant l’usurpation d’adresse de client de la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-337">To remove allow or block spoof sender entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListSpoofItems -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="37b2c-338">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListSpoofItems](/powershell/module/exchange/remove-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="37b2c-338">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListSpoofItems](/powershell/module/exchange/remove-tenantallowblocklistspoofitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-339">Syntaxe d’URL pour la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-339">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="37b2c-340">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="37b2c-340">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="37b2c-341">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="37b2c-341">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="37b2c-342">Unicode n’est pas pris en charge, mais c’est le cas de Punycode.</span><span class="sxs-lookup"><span data-stu-id="37b2c-342">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="37b2c-343">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="37b2c-343">Hostnames are allowed if all of the following statements are true:</span></span>
  - <span data-ttu-id="37b2c-344">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="37b2c-344">The hostname contains a period.</span></span>
  - <span data-ttu-id="37b2c-345">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="37b2c-345">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="37b2c-346">Il y a au moins deux caractères à droite du point.</span><span class="sxs-lookup"><span data-stu-id="37b2c-346">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="37b2c-347">Par exemple, `t.co` est autorisé ou `.com` `contoso.` non.</span><span class="sxs-lookup"><span data-stu-id="37b2c-347">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="37b2c-348">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="37b2c-348">Subpaths are not implied.</span></span>

  <span data-ttu-id="37b2c-349">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="37b2c-349">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="37b2c-350">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-350">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="37b2c-351">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="37b2c-351">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="37b2c-352">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="37b2c-352">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="37b2c-353">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="37b2c-353">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="37b2c-354">Par exemple, `contoso.com/*` est autorisé ou `contoso.com*` `contoso.com/ab*` non.</span><span class="sxs-lookup"><span data-stu-id="37b2c-354">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="37b2c-355">Tous les sous-chemins ne sont pas impliqués par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="37b2c-355">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="37b2c-356">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="37b2c-356">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="37b2c-357">`*.com*` n’est pas valide (domaine non résolvable et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="37b2c-357">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="37b2c-358">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="37b2c-358">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="37b2c-359">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="37b2c-359">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="37b2c-360">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="37b2c-360">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="37b2c-361">Par `~contoso.com` exemple, `contoso.com` inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="37b2c-361">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="37b2c-362">Les entrées d’URL qui contiennent des protocoles (par exemple, , ou ) échouent, car les entrées `http://` `https://` `ftp://` d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="37b2c-362">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="37b2c-363">Un nom d’utilisateur ou un mot de passe ne sont pas pris en charge ou requis.</span><span class="sxs-lookup"><span data-stu-id="37b2c-363">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="37b2c-364">Les guillemets (' ou « ) sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="37b2c-364">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="37b2c-365">Une URL doit inclure toutes les redirections lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="37b2c-365">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="37b2c-366">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="37b2c-366">URL entry scenarios</span></span>

<span data-ttu-id="37b2c-367">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="37b2c-367">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="37b2c-368">Scénario : aucun caractère générique</span><span class="sxs-lookup"><span data-stu-id="37b2c-368">Scenario: No wildcards</span></span>

<span data-ttu-id="37b2c-369">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="37b2c-369">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="37b2c-370">**Autoriser la correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-370">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="37b2c-371">**Autoriser non la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-371">**Allow not matched**:</span></span>

  - <span data-ttu-id="37b2c-372">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-372">abc-contoso.com</span></span>
  - <span data-ttu-id="37b2c-373">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-373">contoso.com/a</span></span>
  - <span data-ttu-id="37b2c-374">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-374">payroll.contoso.com</span></span>
  - <span data-ttu-id="37b2c-375">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-375">test.com/contoso.com</span></span>
  - <span data-ttu-id="37b2c-376">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-376">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="37b2c-377">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-377">www.contoso.com</span></span>
  - <span data-ttu-id="37b2c-378">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-378">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="37b2c-379">**Bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-379">**Block match**:</span></span>

  - <span data-ttu-id="37b2c-380">contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-380">contoso.com</span></span>
  - <span data-ttu-id="37b2c-381">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-381">contoso.com/a</span></span>
  - <span data-ttu-id="37b2c-382">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-382">payroll.contoso.com</span></span>
  - <span data-ttu-id="37b2c-383">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-383">test.com/contoso.com</span></span>
  - <span data-ttu-id="37b2c-384">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-384">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="37b2c-385">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-385">www.contoso.com</span></span>
  - <span data-ttu-id="37b2c-386">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-386">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="37b2c-387">**Bloc non correspond :** abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-387">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="37b2c-388">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="37b2c-388">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="37b2c-389">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="37b2c-389">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="37b2c-390">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-390">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-391">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-391">www.contoso.com</span></span>
  - <span data-ttu-id="37b2c-392">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-392">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="37b2c-393">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="37b2c-393">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="37b2c-394">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-394">123contoso.com</span></span>
  - <span data-ttu-id="37b2c-395">contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-395">contoso.com</span></span>
  - <span data-ttu-id="37b2c-396">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-396">test.com/contoso.com</span></span>
  - <span data-ttu-id="37b2c-397">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="37b2c-397">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="37b2c-398">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37b2c-398">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="37b2c-399">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="37b2c-399">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="37b2c-400">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-400">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-401">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="37b2c-401">contoso.com/a/b</span></span>
  - <span data-ttu-id="37b2c-402">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="37b2c-402">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="37b2c-403">contoso.com/a/?q=joe@t.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-403">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="37b2c-404">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="37b2c-404">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="37b2c-405">contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-405">contoso.com</span></span>
  - <span data-ttu-id="37b2c-406">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-406">contoso.com/a</span></span>
  - <span data-ttu-id="37b2c-407">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-407">www.contoso.com</span></span>
  - <span data-ttu-id="37b2c-408">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-408">www.contoso.com/q=a@contoso.com</span></span>

#### <a name="scenario-left-tilde"></a><span data-ttu-id="37b2c-409">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="37b2c-409">Scenario: Left tilde</span></span>

<span data-ttu-id="37b2c-410">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="37b2c-410">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="37b2c-411">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-411">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-412">contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-412">contoso.com</span></span>
  - <span data-ttu-id="37b2c-413">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-413">www.contoso.com</span></span>
  - <span data-ttu-id="37b2c-414">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-414">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="37b2c-415">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="37b2c-415">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="37b2c-416">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-416">123contoso.com</span></span>
  - <span data-ttu-id="37b2c-417">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="37b2c-417">contoso.com/abc</span></span>
  - <span data-ttu-id="37b2c-418">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="37b2c-418">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="37b2c-419">Scénario : suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="37b2c-419">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="37b2c-420">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="37b2c-420">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="37b2c-421">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-421">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-422">contoso.com/?q=whatever@fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-422">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="37b2c-423">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-423">contoso.com/a</span></span>
  - <span data-ttu-id="37b2c-424">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="37b2c-424">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="37b2c-425">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="37b2c-425">contoso.com/ab</span></span>
  - <span data-ttu-id="37b2c-426">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="37b2c-426">contoso.com/b</span></span>
  - <span data-ttu-id="37b2c-427">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="37b2c-427">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="37b2c-428">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="37b2c-428">contoso.com/ba</span></span>

- <span data-ttu-id="37b2c-429">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-429">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="37b2c-430">Scénario : sous-domaine générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="37b2c-430">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="37b2c-431">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="37b2c-431">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="37b2c-432">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-432">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-433">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="37b2c-433">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="37b2c-434">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="37b2c-434">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="37b2c-435">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-435">www.contoso.com/a</span></span>
  - <span data-ttu-id="37b2c-436">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="37b2c-436">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="37b2c-437">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="37b2c-437">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="37b2c-438">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="37b2c-438">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="37b2c-439">Scénario : tilde gauche et droite</span><span class="sxs-lookup"><span data-stu-id="37b2c-439">Scenario: Left and right tilde</span></span>

<span data-ttu-id="37b2c-440">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="37b2c-440">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="37b2c-441">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-441">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-442">contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-442">contoso.com</span></span>
  - <span data-ttu-id="37b2c-443">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-443">contoso.com/a</span></span>
  - <span data-ttu-id="37b2c-444">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-444">www.contoso.com</span></span>
  - <span data-ttu-id="37b2c-445">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="37b2c-445">www.contoso.com/b</span></span>
  - <span data-ttu-id="37b2c-446">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-446">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="37b2c-447">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="37b2c-447">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="37b2c-448">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-448">123contoso.com</span></span>
  - <span data-ttu-id="37b2c-449">contoso.org</span><span class="sxs-lookup"><span data-stu-id="37b2c-449">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="37b2c-450">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="37b2c-450">Scenario: IP address</span></span>

<span data-ttu-id="37b2c-451">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="37b2c-451">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="37b2c-452">**Autoriser la correspondance** **et bloquer la correspondance**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="37b2c-452">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="37b2c-453">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="37b2c-453">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="37b2c-454">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-454">1.2.3.4/a</span></span>
  - <span data-ttu-id="37b2c-455">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="37b2c-455">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="37b2c-456">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="37b2c-456">IP address with right wildcard</span></span>

<span data-ttu-id="37b2c-457">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="37b2c-457">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="37b2c-458">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-458">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="37b2c-459">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="37b2c-459">1.2.3.4/b</span></span>
  - <span data-ttu-id="37b2c-460">1.2.3.4/baaaa</span><span class="sxs-lookup"><span data-stu-id="37b2c-460">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="37b2c-461">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="37b2c-461">Examples of invalid entries</span></span>

<span data-ttu-id="37b2c-462">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="37b2c-462">The following entries are invalid:</span></span>

- <span data-ttu-id="37b2c-463">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-463">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="37b2c-464">contoso</span><span class="sxs-lookup"><span data-stu-id="37b2c-464">contoso</span></span>
  - <span data-ttu-id="37b2c-465">\*.contoso.\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-465">\*.contoso.\*</span></span>
  - <span data-ttu-id="37b2c-466">\*.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-466">\*.com</span></span>
  - <span data-ttu-id="37b2c-467">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="37b2c-467">\*.pdf</span></span>

- <span data-ttu-id="37b2c-468">**Caractère générique sur du texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-468">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="37b2c-469">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-469">\*contoso.com</span></span>
  - <span data-ttu-id="37b2c-470">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-470">contoso.com\*</span></span>
  - <span data-ttu-id="37b2c-471">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="37b2c-471">\*1.2.3.4</span></span>
  - <span data-ttu-id="37b2c-472">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-472">1.2.3.4\*</span></span>
  - <span data-ttu-id="37b2c-473">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-473">contoso.com/a\*</span></span>
  - <span data-ttu-id="37b2c-474">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-474">contoso.com/ab\*</span></span>

- <span data-ttu-id="37b2c-475">**Adresses IP avec ports**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-475">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="37b2c-476">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="37b2c-476">contoso.com:443</span></span>
  - <span data-ttu-id="37b2c-477">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="37b2c-477">abc.contoso.com:25</span></span>

- <span data-ttu-id="37b2c-478">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-478">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="37b2c-479">\*.\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-479">\*.\*</span></span>

- <span data-ttu-id="37b2c-480">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="37b2c-480">**Middle wildcards**:</span></span>

  - <span data-ttu-id="37b2c-481">conto \* so.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-481">conto\*so.com</span></span>
  - <span data-ttu-id="37b2c-482">conto~so.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-482">conto~so.com</span></span>

- <span data-ttu-id="37b2c-483">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="37b2c-483">**Double wildcards**</span></span>

  - <span data-ttu-id="37b2c-484">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-484">contoso.com/\*\*</span></span>
  - <span data-ttu-id="37b2c-485">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="37b2c-485">contoso.com/\*/\*</span></span>

## <a name="domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="37b2c-486">Syntaxe de paire de domaines pour les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="37b2c-486">Domain pair syntax for spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="37b2c-487">Une paire de domaines pour un expéditeur usurpé dans la liste d’adresses client autoriser/bloquer utilise la syntaxe suivante `<Spoofed user>, <Sending infrastructure>` :</span><span class="sxs-lookup"><span data-stu-id="37b2c-487">A domain pair for a spoofed sender in the Tenant Allow/Block List uses the following syntax: `<Spoofed user>, <Sending infrastructure>`.</span></span>

- <span data-ttu-id="37b2c-488">**Utilisateur usurpé**: cette valeur implique l’adresse e-mail de l’utilisateur  usurpé qui s’affiche dans la zone De des clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="37b2c-488">**Spoofed user**: This value involves the email address of the spoofed user that's displayed in the **From** box in email clients.</span></span> <span data-ttu-id="37b2c-489">Cette adresse est également appelée `5322.From` adresse.</span><span class="sxs-lookup"><span data-stu-id="37b2c-489">This address is also known as the `5322.From` address.</span></span> <span data-ttu-id="37b2c-490">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-490">Valid values include:</span></span>
  - <span data-ttu-id="37b2c-491">Adresse de messagerie individuelle (par exemple, chris@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="37b2c-491">An individual email address (for example, chris@contoso.com).</span></span>
  - <span data-ttu-id="37b2c-492">Un domaine de messagerie (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="37b2c-492">An email domain (for example, contoso.com).</span></span>
  - <span data-ttu-id="37b2c-493">Caractère générique (par exemple, \* ).</span><span class="sxs-lookup"><span data-stu-id="37b2c-493">The wildcard character (for example, \*).</span></span>

- <span data-ttu-id="37b2c-494">**Infrastructure d’envoi**: cette valeur indique la source des messages de l’utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="37b2c-494">**Sending infrastructure**: This value indicates the source of messages from the spoofed user.</span></span> <span data-ttu-id="37b2c-495">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b2c-495">Valid values include:</span></span>
  - <span data-ttu-id="37b2c-496">Domaine trouvé dans une recherche DNS inversée (enregistrement PTR) de l’adresse IP du serveur de messagerie source (par exemple, fabrikam.com).</span><span class="sxs-lookup"><span data-stu-id="37b2c-496">The domain found in a reverse DNS lookup (PTR record) of the source email server's IP address (for example, fabrikam.com).</span></span>
  - <span data-ttu-id="37b2c-497">Si l’adresse IP source n’a pas d’enregistrement PTR, l’infrastructure d’envoi est identifiée comme \<source IP\> /24 (par exemple, 192.168.100.100/24).</span><span class="sxs-lookup"><span data-stu-id="37b2c-497">If the source IP address has no PTR record, then the sending infrastructure is identified as \<source IP\>/24 (for example, 192.168.100.100/24).</span></span>

<span data-ttu-id="37b2c-498">Voici quelques exemples de paires de domaines valides pour identifier les expéditeurs usurpés :</span><span class="sxs-lookup"><span data-stu-id="37b2c-498">Here are some examples of valid domain pairs to identify spoofed senders:</span></span>

- `contoso.com, 192.168.100.100/24`
- `chris@contoso.com, fabrikam.com`
- `*, contoso.net`

<span data-ttu-id="37b2c-499">L’ajout d’une paire de domaines autorise ou bloque uniquement la *combinaison* de l’utilisateur usurpé *et* de l’infrastructure d’envoi.</span><span class="sxs-lookup"><span data-stu-id="37b2c-499">Adding a domain pair only allows or blocks the *combination* of the spoofed user *and* the sending infrastructure.</span></span> <span data-ttu-id="37b2c-500">Il n’autorise pas le courrier électronique provenant de l’utilisateur usurpé d’aucune source, ni le courrier provenant de la source d’infrastructure d’envoi pour tout utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="37b2c-500">It does not allow email from the spoofed user from any source, nor does it allow email from the sending infrastructure source for any spoofed user.</span></span>

<span data-ttu-id="37b2c-501">Par exemple, vous ajoutez une entrée d’accès pour la paire de domaines suivante :</span><span class="sxs-lookup"><span data-stu-id="37b2c-501">For example, you add an allow entry for the following domain pair:</span></span>

- <span data-ttu-id="37b2c-502">**Domaine**: gmail.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-502">**Domain**: gmail.com</span></span>
- <span data-ttu-id="37b2c-503">**Infrastructure**: tms.mx.com</span><span class="sxs-lookup"><span data-stu-id="37b2c-503">**Infrastructure**: tms.mx.com</span></span>

<span data-ttu-id="37b2c-504">Seuls les messages provenant *de* ce domaine et de cette paire d’infrastructure d’envoi sont autorisés à usurper l’usurpation.</span><span class="sxs-lookup"><span data-stu-id="37b2c-504">Only messages from that domain *and* sending infrastructure pair are allowed to spoof.</span></span> <span data-ttu-id="37b2c-505">Les autres expéditeurs qui tentent d’usurper gmail.com ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="37b2c-505">Other senders attempting to spoof gmail.com aren't allowed.</span></span> <span data-ttu-id="37b2c-506">Les messages provenant d’expéditeurs d’autres domaines tms.mx.com sont vérifiés par la veille contre l’usurpation d’adresse.</span><span class="sxs-lookup"><span data-stu-id="37b2c-506">Messages from senders in other domains originating from tms.mx.com are checked by spoof intelligence.</span></span>
