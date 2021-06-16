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
ms.openlocfilehash: 4228bb8abb70bbd96605a7d0f021a1a483e8715c
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52929730"
---
# <a name="manage-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-103">Gérer la liste Autoriser/Bloquer du client</span><span class="sxs-lookup"><span data-stu-id="f522c-103">Manage the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="f522c-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f522c-104">**Applies to**</span></span>
- [<span data-ttu-id="f522c-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="f522c-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="f522c-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="f522c-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="f522c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f522c-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
>
> <span data-ttu-id="f522c-108">Les fonctionnalités décrites dans cet article sont en prévisualisation, peuvent faire l’objet de changements et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="f522c-108">The features described in this article are in Preview, are subject to change, and are not available in all organizations.</span></span>  <span data-ttu-id="f522c-109">Si votre organisation ne dispose pas des fonctionnalités d’usurpation d’informations décrites dans cet article, consultez l’ancienne expérience de gestion de l’usurpation d’adresses chez [Manage spoofed senders using the spoof intelligence policy and spoof intelligence insight in EOP](walkthrough-spoof-intelligence-insight.md).</span><span class="sxs-lookup"><span data-stu-id="f522c-109">If your organization does not have the spoof features as described in this article, see the older spoof management experience at [Manage spoofed senders using the spoof intelligence policy and spoof intelligence insight in EOP](walkthrough-spoof-intelligence-insight.md).</span></span>
>
> <span data-ttu-id="f522c-110">Vous ne pouvez pas **configurer d’URL** ou d’éléments de fichier autorisés dans la liste d’adresses client autorisées/bloqués pour le moment.</span><span class="sxs-lookup"><span data-stu-id="f522c-110">You can't **configure** allowed URL or file items in the Tenant Allow/Block List at this time.</span></span>

<span data-ttu-id="f522c-111">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, vous pouvez ne pas être d’accord avec le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="f522c-111">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="f522c-112">Par exemple, un bon message peut être marqué comme mauvais (faux positif) ou un message erroné peut être autorisé (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="f522c-112">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="f522c-113">La liste des locataires autoriser/bloquer dans le portail Microsoft 365 Defender vous permet de remplacer manuellement les verdicts de filtrage Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="f522c-113">The Tenant Allow/Block List in the Microsoft 365 Defender portal gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="f522c-114">La liste d’adresses client autoriser/bloquer est utilisée pendant le flux de messagerie et au moment des clics de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f522c-114">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="f522c-115">Vous pouvez spécifier les types de substitutions suivants :</span><span class="sxs-lookup"><span data-stu-id="f522c-115">You can specify the following types of overrides:</span></span>

- <span data-ttu-id="f522c-116">URL à bloquer.</span><span class="sxs-lookup"><span data-stu-id="f522c-116">URLs to block.</span></span>
- <span data-ttu-id="f522c-117">Fichiers à bloquer.</span><span class="sxs-lookup"><span data-stu-id="f522c-117">Files to block.</span></span>
- <span data-ttu-id="f522c-118">Expéditeurs usurpés à autoriser ou bloquer.</span><span class="sxs-lookup"><span data-stu-id="f522c-118">Spoofed senders to allow or block.</span></span> <span data-ttu-id="f522c-119">Si vous remplacez le verdict [](learn-about-spoof-intelligence.md)d’usurpation d’adresses ou de verdicts d’usurpation d’adresse, l’expéditeur usurpé devient une entrée d’accès ou de blocage manuelle qui apparaît uniquement sous l’onglet Usurpation d’adresse dans la liste d’adresses client autoriser/bloquer. </span><span class="sxs-lookup"><span data-stu-id="f522c-119">If you override the allow or block verdict in the [spoof intelligence insight](learn-about-spoof-intelligence.md), the spoofed sender becomes a manual allow or block entry that only appears on the **Spoof** tab in the Tenant Allow/Block List.</span></span> <span data-ttu-id="f522c-120">Vous pouvez également créer manuellement des entrées d’autoriser ou de bloquer des expéditeurs usurpés ici avant qu’ils ne sont détectés par la veille contre l’usurpation d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f522c-120">You can also manually create allow or block entries for spoofed senders here before they're detected by spoof intelligence.</span></span>

<span data-ttu-id="f522c-121">Cet article explique comment configurer des entrées dans la liste d’adresses client autoriser/bloquer dans le portail Microsoft 365 Defender ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="f522c-121">This article describes how to configure entries in the Tenant Allow/Block List in the Microsoft 365 Defender portal or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f522c-122">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f522c-122">What do you need to know before you begin?</span></span>

- <span data-ttu-id="f522c-123">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="f522c-123">You open the Microsoft 365 Defender portal at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="f522c-124">Pour aller directement à la page Des listes **d’accueil/de** blocage des clients, utilisez <https://security.microsoft.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="f522c-124">To go directly to the **Tenant Allow/Block Lists** page, use <https://security.microsoft.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="f522c-125">Vous spécifiez des fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="f522c-125">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="f522c-126">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="f522c-126">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```console
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="f522c-127">Un exemple de valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="f522c-127">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="f522c-128">Les valeurs de hachage perceptif (pHash) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f522c-128">Perceptual hash (pHash) values are not supported.</span></span>

- <span data-ttu-id="f522c-129">Les valeurs d’URL disponibles sont décrites dans la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) de la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f522c-129">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

- <span data-ttu-id="f522c-130">La liste d’adresses client autorise un maximum de 500 entrées pour les URL et 500 entrées pour les hâchés de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f522c-130">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="f522c-131">Le nombre maximal de caractères pour chaque entrée est :</span><span class="sxs-lookup"><span data-stu-id="f522c-131">The maximum number of characters for each entry is:</span></span>
  - <span data-ttu-id="f522c-132">Hèmes de fichier = 64</span><span class="sxs-lookup"><span data-stu-id="f522c-132">File hashes = 64</span></span>
  - <span data-ttu-id="f522c-133">URL = 250</span><span class="sxs-lookup"><span data-stu-id="f522c-133">URL = 250</span></span>

- <span data-ttu-id="f522c-134">Une entrée doit être active dans les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="f522c-134">An entry should be active within 30 minutes.</span></span>

- <span data-ttu-id="f522c-135">Par défaut, les entrées de la liste d’inscriptions au client sont expirées au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="f522c-135">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="f522c-136">Vous pouvez spécifier une date ou les définir pour qu’elles n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="f522c-136">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="f522c-137">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="f522c-137">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="f522c-138">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="f522c-138">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="f522c-139">Des autorisations doivent vous avoir été attribuées dans Exchange Online pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="f522c-139">You need to be assigned permissions in Exchange Online before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="f522c-140">**URL et fichiers**:</span><span class="sxs-lookup"><span data-stu-id="f522c-140">**URLs and files**:</span></span>
    - <span data-ttu-id="f522c-141">Pour ajouter et supprimer des valeurs de la liste d’attente des locataires, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="f522c-141">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
    - <span data-ttu-id="f522c-142">Pour un accès en lecture seule à la liste des locataires  autorisé/bloqué, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="f522c-142">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>
  - <span data-ttu-id="f522c-143">**Usurpation :** l’une des combinaisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="f522c-143">**Spoofing**: One of the following combinations:</span></span>
    - <span data-ttu-id="f522c-144">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="f522c-144">**Organization Management**</span></span>
    - <span data-ttu-id="f522c-145">**Administrateur de la** <u>sécurité et</u> **configuration en affichage seul** ou gestion **de l’organisation en affichage seul.**</span><span class="sxs-lookup"><span data-stu-id="f522c-145">**Security Administrator** <u>and</u> **View-Only Configuration** or **View-Only Organization Management**.</span></span>

  <span data-ttu-id="f522c-146">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="f522c-146">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="f522c-147">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f522c-147">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="f522c-148">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f522c-148">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="f522c-149">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f522c-149">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-block-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-150">Utiliser le portail Microsoft 365 Defender pour créer des entrées d’URL de blocage dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-150">Use the Microsoft 365 Defender portal to create block URL entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="f522c-151">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** Tenant \> **Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="f522c-151">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="f522c-152">Dans la page **Liste d’adresses** client autoriser/bloquer, vérifiez que l’onglet **URL** est sélectionné, puis cliquez sur **Bloquer**</span><span class="sxs-lookup"><span data-stu-id="f522c-152">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click **Block**</span></span>

3. <span data-ttu-id="f522c-153">Dans le **volant Bloquer les URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f522c-153">In the **Block URLs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="f522c-154">**Ajouter des URL à bloquer :** entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="f522c-154">**Add URLs to block**: Enter one URL per line, up to a maximum of 20.</span></span> <span data-ttu-id="f522c-155">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) pour la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f522c-155">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

   - <span data-ttu-id="f522c-156">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f522c-156">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="f522c-157">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="f522c-157">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

       <span data-ttu-id="f522c-158">ou</span><span class="sxs-lookup"><span data-stu-id="f522c-158">or</span></span>

     - <span data-ttu-id="f522c-159">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="f522c-159">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="f522c-161">.</span><span class="sxs-lookup"><span data-stu-id="f522c-161">.</span></span>

   - <span data-ttu-id="f522c-162">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="f522c-162">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="f522c-163">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f522c-163">When you're finished, click **Add**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-block-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-164">Utiliser le portail Microsoft 365 Defender pour créer des entrées de fichiers bloqués dans la liste des locataires autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-164">Use the Microsoft 365 Defender portal to create block file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="f522c-165">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** Tenant \> **Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="f522c-165">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="f522c-166">Dans la page **Client Autoriser/Bloquer la liste,** sélectionnez l’onglet **Fichiers,** puis cliquez sur **Bloquer.**</span><span class="sxs-lookup"><span data-stu-id="f522c-166">On the **Tenant Allow/Block List** page, select the **Files** tab, and then click **Block**.</span></span>

3. <span data-ttu-id="f522c-167">Dans la **zone Ajouter des fichiers pour bloquer** le flyout qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f522c-167">In the **Add files to block** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="f522c-168">**Ajouter des hachages de fichier**: entrez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="f522c-168">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>

   - <span data-ttu-id="f522c-169">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f522c-169">**Never expire**: Do one of the following steps:</span></span>

     - <span data-ttu-id="f522c-170">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la case Expires on pour spécifier la ![ ](../../media/scc-toggle-off.png) date d’expiration des entrées. </span><span class="sxs-lookup"><span data-stu-id="f522c-170">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Expires on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="f522c-171">ou</span><span class="sxs-lookup"><span data-stu-id="f522c-171">or</span></span>

     - <span data-ttu-id="f522c-172">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="f522c-172">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="f522c-174">.</span><span class="sxs-lookup"><span data-stu-id="f522c-174">.</span></span>

   - <span data-ttu-id="f522c-175">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="f522c-175">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="f522c-176">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f522c-176">When you're finished, click **Add**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-177">Utiliser le portail Microsoft 365 Defender pour créer des entrées d’expéditeurs usurpées dans la liste d’expéditeurs bloqués ou d’adresses de client</span><span class="sxs-lookup"><span data-stu-id="f522c-177">Use the Microsoft 365 Defender portal to create allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-178">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="f522c-178">**Notes**:</span></span>

- <span data-ttu-id="f522c-179">Seule la _combinaison_ de l’utilisateur usurpé et de l’infrastructure d’envoi, telle que définie dans la paire de domaines, est spécifiquement autorisée ou bloquée à l’usurpation. </span><span class="sxs-lookup"><span data-stu-id="f522c-179">Only the _combination_ of the spoofed user _and_ the sending infrastructure as defined in the domain pair is specifically allowed or blocked from spoofing.</span></span>
- <span data-ttu-id="f522c-180">Lorsque vous configurez une entrée d’autoriser ou de bloquer une paire de domaines, les messages provenant de cette paire de domaines n’apparaissent plus dans l’aperçu de l’usurpation d’intelligence.</span><span class="sxs-lookup"><span data-stu-id="f522c-180">When you configure an allow or block entry for a domain pair, messages from that domain pair no longer appear in the spoof intelligence insight.</span></span>
- <span data-ttu-id="f522c-181">Les entrées des expéditeurs usurpés n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="f522c-181">Entries for spoofed senders never expire.</span></span>

1. <span data-ttu-id="f522c-182">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** Tenant \> **Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="f522c-182">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="f522c-183">Dans la page **Client autoriser/Bloquer la liste,** sélectionnez l’onglet **Usurpation** d’informations, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f522c-183">On the **Tenant Allow/Block List** page, select the **Spoofing** tab, and then click **Add**.</span></span>

3. <span data-ttu-id="f522c-184">Dans le **volant Ajouter de nouvelles paires de domaines** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f522c-184">In the **Add new domain pairs** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="f522c-185">**Ajoutez de nouvelles paires de domaines avec des caractères génériques**: entrez une paire de domaines par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="f522c-185">**Add new domain pairs with wildcards**: Enter one domain pair per line, up to a maximum of 20.</span></span> <span data-ttu-id="f522c-186">Pour plus d’informations sur la syntaxe des entrées d’expéditeur usurpées, voir la syntaxe de paire domaine pour les entrées d’expéditeur usurpées dans la section Client [Autoriser/Bloquer](#domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list) la liste plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f522c-186">For details about the syntax for spoofed sender entries, see the [Domain pair syntax for spoofed sender entries in the Tenant Allow/Block List](#domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list) section later in this article.</span></span>

   - <span data-ttu-id="f522c-187">**Type d’usurpation**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f522c-187">**Spoof type**: Select one of the following values:</span></span>
     - <span data-ttu-id="f522c-188">**Interne**: l’expéditeur usurpé se trouve dans un domaine appartenant à votre organisation [(un domaine accepté).](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)</span><span class="sxs-lookup"><span data-stu-id="f522c-188">**Internal**: The spoofed sender is in a domain that belongs to your organization (an [accepted domain](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)).</span></span>
     - <span data-ttu-id="f522c-189">**Externe**: l’expéditeur usurpé se trouve dans un domaine externe.</span><span class="sxs-lookup"><span data-stu-id="f522c-189">**External**: The spoofed sender is in an external domain.</span></span>

   - <span data-ttu-id="f522c-190">**Action**: **sélectionnez Autoriser** ou **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="f522c-190">**Action**: Select **Allow** or **Block**.</span></span>

4. <span data-ttu-id="f522c-191">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f522c-191">When you're finished, click **Add**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-192">Utiliser le portail Microsoft 365 Defender pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="f522c-192">Use the Microsoft 365 Defender portal to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="f522c-193">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** Tenant \> **Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="f522c-193">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="f522c-194">Sélectionnez l’onglet de votre choix.</span><span class="sxs-lookup"><span data-stu-id="f522c-194">Select the tab you want.</span></span> <span data-ttu-id="f522c-195">Les colonnes disponibles dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="f522c-195">The columns that are available depend on the tab you selected:</span></span>

   - <span data-ttu-id="f522c-196">**URL**:</span><span class="sxs-lookup"><span data-stu-id="f522c-196">**URLs**:</span></span>
     - <span data-ttu-id="f522c-197">**Valeur**: URL.</span><span class="sxs-lookup"><span data-stu-id="f522c-197">**Value**: The URL.</span></span>
     - <span data-ttu-id="f522c-198">**Action**: La valeur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="f522c-198">**Action**: The value **Block**.</span></span>
     - <span data-ttu-id="f522c-199">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="f522c-199">**Last updated date**</span></span>
     - <span data-ttu-id="f522c-200">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="f522c-200">**Expiration date**</span></span>
     - <span data-ttu-id="f522c-201">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="f522c-201">**Note**</span></span>

   - <span data-ttu-id="f522c-202">**Files**</span><span class="sxs-lookup"><span data-stu-id="f522c-202">**Files**</span></span>
     - <span data-ttu-id="f522c-203">**Valeur**: hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="f522c-203">**Value**: The file hash.</span></span>
     - <span data-ttu-id="f522c-204">**Action**: La valeur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="f522c-204">**Action**: The value **Block**.</span></span>
     - <span data-ttu-id="f522c-205">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="f522c-205">**Last updated date**</span></span>
     - <span data-ttu-id="f522c-206">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="f522c-206">**Expiration date**</span></span>
     - <span data-ttu-id="f522c-207">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="f522c-207">**Note**</span></span>

   - <span data-ttu-id="f522c-208">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="f522c-208">**Spoofing**</span></span>
     - <span data-ttu-id="f522c-209">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="f522c-209">**Spoofed user**</span></span>
     - <span data-ttu-id="f522c-210">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f522c-210">**Sending infrastructure**</span></span>
     - <span data-ttu-id="f522c-211">**Type d’usurpation**: valeur **Interne** ou **Externe.**</span><span class="sxs-lookup"><span data-stu-id="f522c-211">**Spoof type**: The value **Internal** or **External**.</span></span>
     - <span data-ttu-id="f522c-212">**Action**: la valeur **Bloquer ou** **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="f522c-212">**Action**: The value **Block** or **Allow**.</span></span>

   <span data-ttu-id="f522c-213">Vous pouvez cliquer sur un en-tête de colonne pour trier par ordre croissant ou décroit.</span><span class="sxs-lookup"><span data-stu-id="f522c-213">You can click on a column heading to sort in ascending or descending order.</span></span>

   <span data-ttu-id="f522c-214">Vous pouvez cliquer sur **Groupe** pour grouper les résultats.</span><span class="sxs-lookup"><span data-stu-id="f522c-214">You can click **Group** to group the results.</span></span> <span data-ttu-id="f522c-215">Les valeurs disponibles dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="f522c-215">The values that are available depend on the tab you selected:</span></span>

   - <span data-ttu-id="f522c-216">**URL : vous** pouvez grouper les résultats par **action.**</span><span class="sxs-lookup"><span data-stu-id="f522c-216">**URLs**: You can group the results by **Action**.</span></span>
   - <span data-ttu-id="f522c-217">**Fichiers**: vous pouvez grouper les résultats par **action.**</span><span class="sxs-lookup"><span data-stu-id="f522c-217">**Files**: You can group the results by **Action**.</span></span>
   - <span data-ttu-id="f522c-218">**Domaines des expéditeurs pour le contournement BCL :** **le groupe** n’est pas disponible sous cet onglet.</span><span class="sxs-lookup"><span data-stu-id="f522c-218">**Sender domains for BCL bypass**: **Group** is not available on this tab.</span></span>
   - <span data-ttu-id="f522c-219">**Usurpation :** vous pouvez grouper les résultats par **action** ou **type d’usurpation.**</span><span class="sxs-lookup"><span data-stu-id="f522c-219">**Spoofing**: You can group the results by **Action** or **Spoof type**.</span></span>

   <span data-ttu-id="f522c-220">Cliquez **sur** Rechercher, entrez une partie ou l’ensemble d’une valeur, puis appuyez sur Entrée pour trouver une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f522c-220">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="f522c-221">Lorsque vous avez terminé, cliquez sur **Effacer l’icône** ![ de recherche Effacer la ](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) recherche.</span><span class="sxs-lookup"><span data-stu-id="f522c-221">When you're finished, click **Clear search** ![Clear search icon](../../media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif).</span></span>

   <span data-ttu-id="f522c-222">Cliquez **sur Filtrer** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="f522c-222">Click **Filter** to filter the results.</span></span> <span data-ttu-id="f522c-223">Les valeurs disponibles dans le flyout **Filter** qui s’affiche dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="f522c-223">The values that are available in **Filter** flyout that appears depend on the tab you selected:</span></span>

   - <span data-ttu-id="f522c-224">**URL**</span><span class="sxs-lookup"><span data-stu-id="f522c-224">**URLs**</span></span>
     - <span data-ttu-id="f522c-225">**Action**</span><span class="sxs-lookup"><span data-stu-id="f522c-225">**Action**</span></span>
     - <span data-ttu-id="f522c-226">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="f522c-226">**Never expire**</span></span>
     - <span data-ttu-id="f522c-227">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="f522c-227">**Last updated date**</span></span>
     - <span data-ttu-id="f522c-228">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="f522c-228">**Expiration date**</span></span>

   - <span data-ttu-id="f522c-229">**Files**</span><span class="sxs-lookup"><span data-stu-id="f522c-229">**Files**</span></span>
     - <span data-ttu-id="f522c-230">**Action**</span><span class="sxs-lookup"><span data-stu-id="f522c-230">**Action**</span></span>
     - <span data-ttu-id="f522c-231">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="f522c-231">**Never expire**</span></span>
     - <span data-ttu-id="f522c-232">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="f522c-232">**Last updated date**</span></span>
     - <span data-ttu-id="f522c-233">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="f522c-233">**Expiration date**</span></span>

   - <span data-ttu-id="f522c-234">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="f522c-234">**Sender domains for BCL bypass**</span></span>
     - <span data-ttu-id="f522c-235">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="f522c-235">**Never expire**</span></span>
     - <span data-ttu-id="f522c-236">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="f522c-236">**Last updated date**</span></span>
     - <span data-ttu-id="f522c-237">**Date d’expiration**</span><span class="sxs-lookup"><span data-stu-id="f522c-237">**Expiration date**</span></span>

   - <span data-ttu-id="f522c-238">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="f522c-238">**Spoofing**</span></span>
     - <span data-ttu-id="f522c-239">**Action**</span><span class="sxs-lookup"><span data-stu-id="f522c-239">**Action**</span></span>
     - <span data-ttu-id="f522c-240">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="f522c-240">**Spoof type**</span></span>

   <span data-ttu-id="f522c-241">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="f522c-241">When you're finished, click **Apply**.</span></span> <span data-ttu-id="f522c-242">Pour effacer les filtres existants,  cliquez sur **Filtrer** et, dans le volant de filtre qui s’affiche, cliquez **sur Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="f522c-242">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-243">Utiliser le portail Microsoft 365 Defender pour modifier des entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="f522c-243">Use the Microsoft 365 Defender portal to modify entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="f522c-244">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** Tenant \> **Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="f522c-244">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="f522c-245">Sélectionnez l’onglet qui contient le type d’entrée à modifier :</span><span class="sxs-lookup"><span data-stu-id="f522c-245">Select the tab that contains the type of entry that you want to modify:</span></span>
   - <span data-ttu-id="f522c-246">**URL**</span><span class="sxs-lookup"><span data-stu-id="f522c-246">**URLs**</span></span>
   - <span data-ttu-id="f522c-247">**Files**</span><span class="sxs-lookup"><span data-stu-id="f522c-247">**Files**</span></span>
   - <span data-ttu-id="f522c-248">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="f522c-248">**Sender domains for BCL bypass**</span></span>
   - <span data-ttu-id="f522c-249">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="f522c-249">**Spoofing**</span></span>

3. <span data-ttu-id="f522c-250">Sélectionnez l’entrée à modifier, puis cliquez **sur** Modifier ![ l’icône ](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="f522c-250">Select the entry that you want to modify, and then click **Edit** ![Edit icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png).</span></span> <span data-ttu-id="f522c-251">Les valeurs que vous pouvez modifier dans le volant qui s’affiche dépendent de l’onglet que vous avez sélectionné à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="f522c-251">The values that you are able to modify in the flyout that appears depend on the tab you selected in the previous step:</span></span>

   - <span data-ttu-id="f522c-252">**URL**</span><span class="sxs-lookup"><span data-stu-id="f522c-252">**URLs**</span></span>
     - <span data-ttu-id="f522c-253">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="f522c-253">**Never expire** and/or expiration date.</span></span>
     - <span data-ttu-id="f522c-254">**Note facultative**</span><span class="sxs-lookup"><span data-stu-id="f522c-254">**Optional note**</span></span>

   - <span data-ttu-id="f522c-255">**Files**</span><span class="sxs-lookup"><span data-stu-id="f522c-255">**Files**</span></span>
     - <span data-ttu-id="f522c-256">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="f522c-256">**Never expire** and/or expiration date.</span></span>
     - <span data-ttu-id="f522c-257">**Note facultative**</span><span class="sxs-lookup"><span data-stu-id="f522c-257">**Optional note**</span></span>

   - <span data-ttu-id="f522c-258">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="f522c-258">**Sender domains for BCL bypass**</span></span>
     - <span data-ttu-id="f522c-259">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="f522c-259">**Never expire** and/or expiration date.</span></span>

   - <span data-ttu-id="f522c-260">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="f522c-260">**Spoofing**</span></span>
     - <span data-ttu-id="f522c-261">**Action**: vous pouvez modifier la valeur sur **Autoriser** ou **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="f522c-261">**Action**: You can change the value to **Allow** or **Block**.</span></span>

4. <span data-ttu-id="f522c-262">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f522c-262">When you're finished, click **Save**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-263">Utiliser le portail Microsoft 365 Defender pour supprimer des entrées de la liste des locataires autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-263">Use the Microsoft 365 Defender portal to remove entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="f522c-264">Dans le portail Microsoft 365 Defender, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="f522c-264">In the Microsoft 365 Defender portal, go to **Threat management** \> **Policy** \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="f522c-265">Sélectionnez l’onglet qui contient le type d’entrée à supprimer :</span><span class="sxs-lookup"><span data-stu-id="f522c-265">Select the tab that contains the type of entry that you want to remove:</span></span>
   - <span data-ttu-id="f522c-266">**URL**</span><span class="sxs-lookup"><span data-stu-id="f522c-266">**URLs**</span></span>
   - <span data-ttu-id="f522c-267">**Files**</span><span class="sxs-lookup"><span data-stu-id="f522c-267">**Files**</span></span>
   - <span data-ttu-id="f522c-268">**Domaines des expéditeurs pour le contournement BCL**</span><span class="sxs-lookup"><span data-stu-id="f522c-268">**Sender domains for BCL bypass**</span></span>
   - <span data-ttu-id="f522c-269">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="f522c-269">**Spoofing**</span></span>

3. <span data-ttu-id="f522c-270">Sélectionnez l’entrée à supprimer, puis cliquez **sur** Supprimer ![ l’icône ](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="f522c-270">Select the entry that you want to remove, and then click **Delete** ![Delete icon](../../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>

4. <span data-ttu-id="f522c-271">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="f522c-271">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-272">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-272">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-block-file-or-url-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-273">Utiliser PowerShell pour ajouter des entrées de bloc de fichier ou d’URL à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-273">Use PowerShell to add block file or URL entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-274">Pour ajouter des entrées de blocage de fichier ou d’URL dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-274">To add block file or URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <FileHash | Url> -Block -Entries "Value1","Value2",..."ValueN" <-ExpirationDate Date | -NoExpiration> [-Notes <String>]
```

<span data-ttu-id="f522c-275">Cet exemple ajoute une entrée de fichier de blocage pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="f522c-275">This example adds a block file entry for the specified files that never expires.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType FileHash -Block -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="f522c-276">Cet exemple ajoute une entrée d’URL de bloc pour contoso.com et tous les sous-contoso.com (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f522c-276">This example adds a block URL entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="f522c-277">Étant donné que nous n’avons pas utilisé les paramètres ExpirationDate ou NoExpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="f522c-277">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Block -Entries ~contoso.com
```

<span data-ttu-id="f522c-278">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-278">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-add-allow-or-block-spoofed-sender-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-279">Utiliser PowerShell pour ajouter des entrées d’expéditeurs usurpés ou autoriser ou bloquer à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-279">Use PowerShell to add allow or block spoofed sender entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-280">Pour ajouter des entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-280">To add spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListSpoofItems -SpoofedUser <Domain | EmailAddress | *> -SendingInfrastructure <Domain | IPAddress/24> -SpoofType <External | Internal> -Action <Allow | Block>
```

<span data-ttu-id="f522c-281">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListSpoofItems](/powershell/module/exchange/new-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-281">For detailed syntax and parameter information, see [New-TenantAllowBlockListSpoofItems](/powershell/module/exchange/new-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-view-block-file-or-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-282">Utiliser PowerShell pour afficher les entrées de fichier ou d’URL bloqués dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-282">Use PowerShell to view block file or URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-283">Pour afficher les entrées de fichier ou d’URL bloqués dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-283">To view block file or URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <FileHash | URL> [-Entry <FileHashValue | URLValue>] [<-ExpirationDate Date | -NoExpiration>]
```

<span data-ttu-id="f522c-284">Cet exemple renvoie des informations pour la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f522c-284">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="f522c-285">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="f522c-285">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Block
```

<span data-ttu-id="f522c-286">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-286">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-287">Utiliser PowerShell pour afficher ou bloquer les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-287">Use PowerShell to view allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-288">Pour afficher les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-288">To view spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems [-Action <Allow | Block>] [-SpoofType <External | Internal>
```

<span data-ttu-id="f522c-289">Cet exemple renvoie toutes les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="f522c-289">This example returns all spoofed sender entries in the Tenant Allow/Block List.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems
```

<span data-ttu-id="f522c-290">Cet exemple renvoie toutes les entrées d’expéditeur usurpées qui sont internes.</span><span class="sxs-lookup"><span data-stu-id="f522c-290">This example returns all allow spoofed sender entries that are internal.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems -Action Allow -SpoofType Internal
```

<span data-ttu-id="f522c-291">Cet exemple renvoie toutes les entrées d’expéditeur usurpées bloquées qui sont externes.</span><span class="sxs-lookup"><span data-stu-id="f522c-291">This example returns all blocked spoofed sender entries that are external.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems -Action Block -SpoofType External
```

<span data-ttu-id="f522c-292">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-TenantAllowBlockListSpoofItems](/powershell/module/exchange/get-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-292">For detailed syntax and parameter information, see [Get-TenantAllowBlockListSpoofItems](/powershell/module/exchange/get-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-modify-block-file-and-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-293">Utiliser PowerShell pour modifier les entrées de blocage de fichiers et d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-293">Use PowerShell to modify block file and URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-294">Pour modifier les entrées de blocage de fichiers et d’URL dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-294">To modify block file and URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <FileHash | Url> -Ids <"Id1","Id2",..."IdN"> [<-ExpirationDate Date | -NoExpiration>] [-Notes <String>]
```

<span data-ttu-id="f522c-295">Cet exemple modifie la date d’expiration de l’entrée d’URL de bloc spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f522c-295">This example changes the expiration date of the specified block URL entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate "5/30/2020"
```

<span data-ttu-id="f522c-296">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-296">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-297">Utiliser PowerShell pour modifier les entrées d’expéditeurs usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-297">Use PowerShell to modify allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-298">Pour modifier les entrées d’expéditeurs usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-298">To modify allow or block spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListSpoofItems -Ids <"Id1","Id2",..."IdN"> -Action <Allow | Block>
```

<span data-ttu-id="f522c-299">Cet exemple modifie l’entrée de l’expéditeur usurpé de l’adresse « allow » à « block ».</span><span class="sxs-lookup"><span data-stu-id="f522c-299">This example changes spoofed sender entry from allow to block.</span></span>

```powershell
Set-TenantAllowBlockListItems -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -Action Block
```

<span data-ttu-id="f522c-300">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListSpoofItems](/powershell/module/exchange/set-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-300">For detailed syntax and parameter information, see [Set-TenantAllowBlockListSpoofItems](/powershell/module/exchange/set-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-remove-url-or-file-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-301">Utiliser PowerShell pour supprimer l’URL ou les entrées de fichier de la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-301">Use PowerShell to remove URL or file entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-302">Pour supprimer des entrées de fichier et d’URL de la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-302">To remove file and URL entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <FileHash | Url> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="f522c-303">Cet exemple supprime l’entrée d’URL de bloc spécifiée de la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="f522c-303">This example removes the specified block URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="f522c-304">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-304">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-allow-or-block-spoofed-sender-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-305">Utiliser PowerShell pour supprimer les entrées d’expéditeurs usurpées de la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-305">Use PowerShell to remove allow or block spoofed sender entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-306">Pour supprimer les entrées d’expéditeurs usurpant l’usurpation d’adresse de client de la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-306">To remove allow or block spoof sender entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListSpoofItems -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="f522c-307">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListSpoofItems](/powershell/module/exchange/remove-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="f522c-307">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListSpoofItems](/powershell/module/exchange/remove-tenantallowblocklistspoofitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-308">Syntaxe d’URL pour la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-308">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="f522c-309">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="f522c-309">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="f522c-310">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="f522c-310">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="f522c-311">Unicode n’est pas pris en charge, mais c’est le cas de Punycode.</span><span class="sxs-lookup"><span data-stu-id="f522c-311">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="f522c-312">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="f522c-312">Hostnames are allowed if all of the following statements are true:</span></span>
  - <span data-ttu-id="f522c-313">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="f522c-313">The hostname contains a period.</span></span>
  - <span data-ttu-id="f522c-314">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="f522c-314">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="f522c-315">Il y a au moins deux caractères à droite du point.</span><span class="sxs-lookup"><span data-stu-id="f522c-315">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="f522c-316">Par exemple, `t.co` est autorisé ou `.com` `contoso.` non.</span><span class="sxs-lookup"><span data-stu-id="f522c-316">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="f522c-317">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="f522c-317">Subpaths are not implied.</span></span>

  <span data-ttu-id="f522c-318">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="f522c-318">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="f522c-319">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="f522c-319">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="f522c-320">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="f522c-320">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="f522c-321">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="f522c-321">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="f522c-322">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f522c-322">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="f522c-323">Par exemple, `contoso.com/*` est autorisé ou `contoso.com*` `contoso.com/ab*` non.</span><span class="sxs-lookup"><span data-stu-id="f522c-323">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="f522c-324">Tous les sous-chemins ne sont pas impliqués par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="f522c-324">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="f522c-325">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="f522c-325">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="f522c-326">`*.com*` n’est pas valide (domaine non résolvable et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="f522c-326">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="f522c-327">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="f522c-327">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="f522c-328">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="f522c-328">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="f522c-329">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="f522c-329">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="f522c-330">Par `~contoso.com` exemple, `contoso.com` inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="f522c-330">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="f522c-331">Les entrées d’URL qui contiennent des protocoles (par exemple, , ou ) échouent, car les entrées `http://` `https://` `ftp://` d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="f522c-331">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="f522c-332">Un nom d’utilisateur ou un mot de passe ne sont pas pris en charge ou requis.</span><span class="sxs-lookup"><span data-stu-id="f522c-332">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="f522c-333">Les guillemets (' ou « ) sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="f522c-333">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="f522c-334">Une URL doit inclure toutes les redirections lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="f522c-334">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="f522c-335">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="f522c-335">URL entry scenarios</span></span>

<span data-ttu-id="f522c-336">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f522c-336">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="f522c-337">Scénario : aucun caractère générique</span><span class="sxs-lookup"><span data-stu-id="f522c-337">Scenario: No wildcards</span></span>

<span data-ttu-id="f522c-338">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="f522c-338">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="f522c-339">**Autoriser la correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-339">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="f522c-340">**Autoriser non la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-340">**Allow not matched**:</span></span>

  - <span data-ttu-id="f522c-341">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-341">abc-contoso.com</span></span>
  - <span data-ttu-id="f522c-342">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="f522c-342">contoso.com/a</span></span>
  - <span data-ttu-id="f522c-343">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-343">payroll.contoso.com</span></span>
  - <span data-ttu-id="f522c-344">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-344">test.com/contoso.com</span></span>
  - <span data-ttu-id="f522c-345">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-345">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="f522c-346">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-346">www.contoso.com</span></span>
  - <span data-ttu-id="f522c-347">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-347">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="f522c-348">**Bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-348">**Block match**:</span></span>

  - <span data-ttu-id="f522c-349">contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-349">contoso.com</span></span>
  - <span data-ttu-id="f522c-350">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="f522c-350">contoso.com/a</span></span>
  - <span data-ttu-id="f522c-351">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-351">payroll.contoso.com</span></span>
  - <span data-ttu-id="f522c-352">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-352">test.com/contoso.com</span></span>
  - <span data-ttu-id="f522c-353">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-353">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="f522c-354">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-354">www.contoso.com</span></span>
  - <span data-ttu-id="f522c-355">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-355">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="f522c-356">**Bloc non correspond :** abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-356">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="f522c-357">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="f522c-357">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="f522c-358">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="f522c-358">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="f522c-359">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-359">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-360">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-360">www.contoso.com</span></span>
  - <span data-ttu-id="f522c-361">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-361">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="f522c-362">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="f522c-362">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="f522c-363">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-363">123contoso.com</span></span>
  - <span data-ttu-id="f522c-364">contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-364">contoso.com</span></span>
  - <span data-ttu-id="f522c-365">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-365">test.com/contoso.com</span></span>
  - <span data-ttu-id="f522c-366">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="f522c-366">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="f522c-367">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f522c-367">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="f522c-368">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="f522c-368">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="f522c-369">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-369">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-370">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="f522c-370">contoso.com/a/b</span></span>
  - <span data-ttu-id="f522c-371">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="f522c-371">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="f522c-372">contoso.com/a/?q=joe@t.com</span><span class="sxs-lookup"><span data-stu-id="f522c-372">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="f522c-373">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="f522c-373">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="f522c-374">contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-374">contoso.com</span></span>
  - <span data-ttu-id="f522c-375">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="f522c-375">contoso.com/a</span></span>
  - <span data-ttu-id="f522c-376">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-376">www.contoso.com</span></span>
  - <span data-ttu-id="f522c-377">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-377">www.contoso.com/q=a@contoso.com</span></span>

#### <a name="scenario-left-tilde"></a><span data-ttu-id="f522c-378">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="f522c-378">Scenario: Left tilde</span></span>

<span data-ttu-id="f522c-379">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="f522c-379">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="f522c-380">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-380">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-381">contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-381">contoso.com</span></span>
  - <span data-ttu-id="f522c-382">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-382">www.contoso.com</span></span>
  - <span data-ttu-id="f522c-383">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-383">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="f522c-384">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="f522c-384">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="f522c-385">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-385">123contoso.com</span></span>
  - <span data-ttu-id="f522c-386">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="f522c-386">contoso.com/abc</span></span>
  - <span data-ttu-id="f522c-387">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="f522c-387">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="f522c-388">Scénario : suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="f522c-388">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="f522c-389">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="f522c-389">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="f522c-390">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-390">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-391">contoso.com/?q=whatever@fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="f522c-391">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="f522c-392">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="f522c-392">contoso.com/a</span></span>
  - <span data-ttu-id="f522c-393">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="f522c-393">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="f522c-394">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="f522c-394">contoso.com/ab</span></span>
  - <span data-ttu-id="f522c-395">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="f522c-395">contoso.com/b</span></span>
  - <span data-ttu-id="f522c-396">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="f522c-396">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="f522c-397">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="f522c-397">contoso.com/ba</span></span>

- <span data-ttu-id="f522c-398">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-398">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="f522c-399">Scénario : sous-domaine générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="f522c-399">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="f522c-400">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="f522c-400">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="f522c-401">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-401">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-402">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="f522c-402">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="f522c-403">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="f522c-403">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="f522c-404">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="f522c-404">www.contoso.com/a</span></span>
  - <span data-ttu-id="f522c-405">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="f522c-405">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="f522c-406">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="f522c-406">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="f522c-407">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="f522c-407">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="f522c-408">Scénario : tilde gauche et droite</span><span class="sxs-lookup"><span data-stu-id="f522c-408">Scenario: Left and right tilde</span></span>

<span data-ttu-id="f522c-409">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="f522c-409">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="f522c-410">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-410">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-411">contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-411">contoso.com</span></span>
  - <span data-ttu-id="f522c-412">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="f522c-412">contoso.com/a</span></span>
  - <span data-ttu-id="f522c-413">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-413">www.contoso.com</span></span>
  - <span data-ttu-id="f522c-414">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="f522c-414">www.contoso.com/b</span></span>
  - <span data-ttu-id="f522c-415">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-415">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="f522c-416">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="f522c-416">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="f522c-417">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-417">123contoso.com</span></span>
  - <span data-ttu-id="f522c-418">contoso.org</span><span class="sxs-lookup"><span data-stu-id="f522c-418">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="f522c-419">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="f522c-419">Scenario: IP address</span></span>

<span data-ttu-id="f522c-420">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="f522c-420">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="f522c-421">**Autoriser la correspondance** **et bloquer la correspondance**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="f522c-421">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="f522c-422">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="f522c-422">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="f522c-423">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="f522c-423">1.2.3.4/a</span></span>
  - <span data-ttu-id="f522c-424">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="f522c-424">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="f522c-425">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="f522c-425">IP address with right wildcard</span></span>

<span data-ttu-id="f522c-426">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="f522c-426">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="f522c-427">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="f522c-427">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="f522c-428">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="f522c-428">1.2.3.4/b</span></span>
  - <span data-ttu-id="f522c-429">1.2.3.4/baaaa</span><span class="sxs-lookup"><span data-stu-id="f522c-429">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="f522c-430">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="f522c-430">Examples of invalid entries</span></span>

<span data-ttu-id="f522c-431">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="f522c-431">The following entries are invalid:</span></span>

- <span data-ttu-id="f522c-432">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="f522c-432">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="f522c-433">contoso</span><span class="sxs-lookup"><span data-stu-id="f522c-433">contoso</span></span>
  - <span data-ttu-id="f522c-434">\*.contoso.\*</span><span class="sxs-lookup"><span data-stu-id="f522c-434">\*.contoso.\*</span></span>
  - <span data-ttu-id="f522c-435">\*.com</span><span class="sxs-lookup"><span data-stu-id="f522c-435">\*.com</span></span>
  - <span data-ttu-id="f522c-436">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="f522c-436">\*.pdf</span></span>

- <span data-ttu-id="f522c-437">**Caractère générique sur du texte ou sans espacement :**</span><span class="sxs-lookup"><span data-stu-id="f522c-437">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="f522c-438">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="f522c-438">\*contoso.com</span></span>
  - <span data-ttu-id="f522c-439">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="f522c-439">contoso.com\*</span></span>
  - <span data-ttu-id="f522c-440">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="f522c-440">\*1.2.3.4</span></span>
  - <span data-ttu-id="f522c-441">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="f522c-441">1.2.3.4\*</span></span>
  - <span data-ttu-id="f522c-442">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="f522c-442">contoso.com/a\*</span></span>
  - <span data-ttu-id="f522c-443">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="f522c-443">contoso.com/ab\*</span></span>

- <span data-ttu-id="f522c-444">**Adresses IP avec ports**:</span><span class="sxs-lookup"><span data-stu-id="f522c-444">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="f522c-445">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="f522c-445">contoso.com:443</span></span>
  - <span data-ttu-id="f522c-446">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="f522c-446">abc.contoso.com:25</span></span>

- <span data-ttu-id="f522c-447">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="f522c-447">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="f522c-448">\*.\*</span><span class="sxs-lookup"><span data-stu-id="f522c-448">\*.\*</span></span>

- <span data-ttu-id="f522c-449">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="f522c-449">**Middle wildcards**:</span></span>

  - <span data-ttu-id="f522c-450">conto \* so.com</span><span class="sxs-lookup"><span data-stu-id="f522c-450">conto\*so.com</span></span>
  - <span data-ttu-id="f522c-451">conto~so.com</span><span class="sxs-lookup"><span data-stu-id="f522c-451">conto~so.com</span></span>

- <span data-ttu-id="f522c-452">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="f522c-452">**Double wildcards**</span></span>

  - <span data-ttu-id="f522c-453">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="f522c-453">contoso.com/\*\*</span></span>
  - <span data-ttu-id="f522c-454">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="f522c-454">contoso.com/\*/\*</span></span>

## <a name="domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="f522c-455">Syntaxe de paire de domaines pour les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="f522c-455">Domain pair syntax for spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="f522c-456">Une paire de domaines pour un expéditeur usurpé dans la liste d’adresses client autoriser/bloquer utilise la syntaxe suivante `<Spoofed user>, <Sending infrastructure>` :</span><span class="sxs-lookup"><span data-stu-id="f522c-456">A domain pair for a spoofed sender in the Tenant Allow/Block List uses the following syntax: `<Spoofed user>, <Sending infrastructure>`.</span></span>

- <span data-ttu-id="f522c-457">**Utilisateur usurpé**: cette valeur implique l’adresse e-mail de l’utilisateur  usurpé qui s’affiche dans la zone De des clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f522c-457">**Spoofed user**: This value involves the email address of the spoofed user that's displayed in the **From** box in email clients.</span></span> <span data-ttu-id="f522c-458">Cette adresse est également appelée `5322.From` adresse.</span><span class="sxs-lookup"><span data-stu-id="f522c-458">This address is also known as the `5322.From` address.</span></span> <span data-ttu-id="f522c-459">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f522c-459">Valid values include:</span></span>
  - <span data-ttu-id="f522c-460">Adresse de messagerie individuelle (par exemple, chris@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f522c-460">An individual email address (for example, chris@contoso.com).</span></span>
  - <span data-ttu-id="f522c-461">Un domaine de messagerie (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f522c-461">An email domain (for example, contoso.com).</span></span>
  - <span data-ttu-id="f522c-462">Caractère générique (par exemple, \* ).</span><span class="sxs-lookup"><span data-stu-id="f522c-462">The wildcard character (for example, \*).</span></span>

- <span data-ttu-id="f522c-463">**Infrastructure d’envoi**: cette valeur indique la source des messages de l’utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="f522c-463">**Sending infrastructure**: This value indicates the source of messages from the spoofed user.</span></span> <span data-ttu-id="f522c-464">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f522c-464">Valid values include:</span></span>
  - <span data-ttu-id="f522c-465">Domaine trouvé dans une recherche DNS inversée (enregistrement PTR) de l’adresse IP du serveur de messagerie source (par exemple, fabrikam.com).</span><span class="sxs-lookup"><span data-stu-id="f522c-465">The domain found in a reverse DNS lookup (PTR record) of the source email server's IP address (for example, fabrikam.com).</span></span>
  - <span data-ttu-id="f522c-466">Si l’adresse IP source n’a pas d’enregistrement PTR, l’infrastructure d’envoi est identifiée comme \<source IP\> /24 (par exemple, 192.168.100.100/24).</span><span class="sxs-lookup"><span data-stu-id="f522c-466">If the source IP address has no PTR record, then the sending infrastructure is identified as \<source IP\>/24 (for example, 192.168.100.100/24).</span></span>

<span data-ttu-id="f522c-467">Voici quelques exemples de paires de domaines valides pour identifier les expéditeurs usurpés :</span><span class="sxs-lookup"><span data-stu-id="f522c-467">Here are some examples of valid domain pairs to identify spoofed senders:</span></span>

- `contoso.com, 192.168.100.100/24`
- `chris@contoso.com, fabrikam.com`
- `*, contoso.net`

<span data-ttu-id="f522c-468">Le nombre maximal d’entrées d’expéditeur usurpées est de 1 000.</span><span class="sxs-lookup"><span data-stu-id="f522c-468">The maximum number of spoofed sender entries is 1000.</span></span> 

<span data-ttu-id="f522c-469">L’ajout d’une paire de domaines autorise ou bloque uniquement la *combinaison* de l’utilisateur usurpé *et* de l’infrastructure d’envoi.</span><span class="sxs-lookup"><span data-stu-id="f522c-469">Adding a domain pair only allows or blocks the *combination* of the spoofed user *and* the sending infrastructure.</span></span> <span data-ttu-id="f522c-470">Il n’autorise pas le courrier électronique provenant de l’utilisateur usurpé d’aucune source, ni le courrier provenant de la source d’infrastructure d’envoi pour tout utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="f522c-470">It does not allow email from the spoofed user from any source, nor does it allow email from the sending infrastructure source for any spoofed user.</span></span> 

<span data-ttu-id="f522c-471">Par exemple, vous ajoutez une entrée d’accès pour la paire de domaines suivante :</span><span class="sxs-lookup"><span data-stu-id="f522c-471">For example, you add an allow entry for the following domain pair:</span></span>

- <span data-ttu-id="f522c-472">**Domaine**: gmail.com</span><span class="sxs-lookup"><span data-stu-id="f522c-472">**Domain**: gmail.com</span></span>
- <span data-ttu-id="f522c-473">**Infrastructure**: tms.mx.com</span><span class="sxs-lookup"><span data-stu-id="f522c-473">**Infrastructure**: tms.mx.com</span></span>

<span data-ttu-id="f522c-474">Seuls les messages provenant *de* ce domaine et de cette paire d’infrastructure d’envoi sont autorisés à usurper l’usurpation.</span><span class="sxs-lookup"><span data-stu-id="f522c-474">Only messages from that domain *and* sending infrastructure pair are allowed to spoof.</span></span> <span data-ttu-id="f522c-475">Les autres expéditeurs qui tentent d’usurper gmail.com ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="f522c-475">Other senders attempting to spoof gmail.com aren't allowed.</span></span> <span data-ttu-id="f522c-476">Les messages provenant d’expéditeurs d’autres domaines tms.mx.com sont vérifiés par la veille contre l’usurpation d’adresse.</span><span class="sxs-lookup"><span data-stu-id="f522c-476">Messages from senders in other domains originating from tms.mx.com are checked by spoof intelligence.</span></span>
