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
ms.openlocfilehash: 67c3badb86f1cfb9bf644cc202ed67e3163a6772
ms.sourcegitcommit: ac3e9ccb7b43a42e600af8f44e6f30019533faeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2021
ms.locfileid: "52933154"
---
# <a name="manage-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-103">Gérer la liste Autoriser/Bloquer du client</span><span class="sxs-lookup"><span data-stu-id="6abab-103">Manage the Tenant Allow/Block List</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="6abab-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6abab-104">**Applies to**</span></span>
- [<span data-ttu-id="6abab-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="6abab-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="6abab-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="6abab-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="6abab-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6abab-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
>
> <span data-ttu-id="6abab-108">Les fonctionnalités décrites dans cet article sont en prévisualisation, peuvent faire l’objet de changements et ne sont pas disponibles dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="6abab-108">The features described in this article are in Preview, are subject to change, and are not available in all organizations.</span></span>  <span data-ttu-id="6abab-109">Si votre organisation ne dispose pas des fonctionnalités d’usurpation d’informations décrites dans cet article, consultez l’ancienne expérience de gestion de l’usurpation d’adresses chez [Manage spoofed senders using the spoof intelligence policy and spoof intelligence insight in EOP](walkthrough-spoof-intelligence-insight.md).</span><span class="sxs-lookup"><span data-stu-id="6abab-109">If your organization does not have the spoof features as described in this article, see the older spoof management experience at [Manage spoofed senders using the spoof intelligence policy and spoof intelligence insight in EOP](walkthrough-spoof-intelligence-insight.md).</span></span>
>
> <span data-ttu-id="6abab-110">Vous ne pouvez pas **configurer d’URL** ou d’éléments de fichier autorisés dans la liste d’adresses client autorisées/bloqués pour le moment.</span><span class="sxs-lookup"><span data-stu-id="6abab-110">You can't **configure** allowed URL or file items in the Tenant Allow/Block List at this time.</span></span>

<span data-ttu-id="6abab-111">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, vous pouvez ne pas être d’accord avec le verdict de filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="6abab-111">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you might disagree with the EOP filtering verdict.</span></span> <span data-ttu-id="6abab-112">Par exemple, un bon message peut être marqué comme mauvais (faux positif) ou un message erroné peut être autorisé (faux négatif).</span><span class="sxs-lookup"><span data-stu-id="6abab-112">For example, a good message might be marked as bad (a false positive), or a bad message might be allowed through (a false negative).</span></span>

<span data-ttu-id="6abab-113">La liste des locataires autoriser/bloquer dans le portail Microsoft 365 Defender vous permet de remplacer manuellement les verdicts de filtrage Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="6abab-113">The Tenant Allow/Block List in the Microsoft 365 Defender portal gives you a way to manually override the Microsoft 365 filtering verdicts.</span></span> <span data-ttu-id="6abab-114">La liste d’adresses client autoriser/bloquer est utilisée pendant le flux de messagerie et au moment des clics de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6abab-114">The Tenant Allow/Block List is used during mail flow and at the time of user clicks.</span></span> <span data-ttu-id="6abab-115">Vous pouvez spécifier les types de substitutions suivants :</span><span class="sxs-lookup"><span data-stu-id="6abab-115">You can specify the following types of overrides:</span></span>

- <span data-ttu-id="6abab-116">URL à bloquer.</span><span class="sxs-lookup"><span data-stu-id="6abab-116">URLs to block.</span></span>
- <span data-ttu-id="6abab-117">Fichiers à bloquer.</span><span class="sxs-lookup"><span data-stu-id="6abab-117">Files to block.</span></span>
- <span data-ttu-id="6abab-118">Expéditeurs usurpés à autoriser ou bloquer.</span><span class="sxs-lookup"><span data-stu-id="6abab-118">Spoofed senders to allow or block.</span></span> <span data-ttu-id="6abab-119">Si vous remplacez le verdict [](learn-about-spoof-intelligence.md)d’usurpation d’adresses ou de verdicts d’usurpation d’adresse, l’expéditeur usurpé devient une entrée d’accès ou de blocage manuelle qui apparaît uniquement sous l’onglet Usurpation d’adresse dans la liste d’adresses client autoriser/bloquer. </span><span class="sxs-lookup"><span data-stu-id="6abab-119">If you override the allow or block verdict in the [spoof intelligence insight](learn-about-spoof-intelligence.md), the spoofed sender becomes a manual allow or block entry that only appears on the **Spoof** tab in the Tenant Allow/Block List.</span></span> <span data-ttu-id="6abab-120">Vous pouvez également créer manuellement des entrées d’autoriser ou de bloquer des expéditeurs usurpés ici avant qu’ils ne sont détectés par la veille contre l’usurpation d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6abab-120">You can also manually create allow or block entries for spoofed senders here before they're detected by spoof intelligence.</span></span>

<span data-ttu-id="6abab-121">Cet article explique comment configurer des entrées dans la liste d’adresses client autoriser/bloquer dans le portail Microsoft 365 Defender ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="6abab-121">This article describes how to configure entries in the Tenant Allow/Block List in the Microsoft 365 Defender portal or in PowerShell (Exchange Online PowerShell for Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="6abab-122">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6abab-122">What do you need to know before you begin?</span></span>

- <span data-ttu-id="6abab-123">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="6abab-123">You open the Microsoft 365 Defender portal at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="6abab-124">Pour aller directement à la page Des listes **d’accueil/de** blocage des clients, utilisez <https://security.microsoft.com/tenantAllowBlockList> .</span><span class="sxs-lookup"><span data-stu-id="6abab-124">To go directly to the **Tenant Allow/Block Lists** page, use <https://security.microsoft.com/tenantAllowBlockList>.</span></span>

- <span data-ttu-id="6abab-125">Vous spécifiez des fichiers à l’aide de la valeur de hachage SHA256 du fichier.</span><span class="sxs-lookup"><span data-stu-id="6abab-125">You specify files by using the SHA256 hash value of the file.</span></span> <span data-ttu-id="6abab-126">Pour rechercher la valeur de hachage SHA256 d’un fichier dans Windows, exécutez la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="6abab-126">To find the SHA256 hash value of a file in Windows, run the following command in a Command Prompt:</span></span>

  ```console
  certutil.exe -hashfile "<Path>\<Filename>" SHA256
  ```

  <span data-ttu-id="6abab-127">Un exemple de valeur est `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a` .</span><span class="sxs-lookup"><span data-stu-id="6abab-127">An example value is `768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3a`.</span></span> <span data-ttu-id="6abab-128">Les valeurs de hachage perceptif (pHash) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6abab-128">Perceptual hash (pHash) values are not supported.</span></span>

- <span data-ttu-id="6abab-129">Les valeurs d’URL disponibles sont décrites dans la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) de la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6abab-129">The available URL values are described in the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>

- <span data-ttu-id="6abab-130">La liste d’adresses client autorise un maximum de 500 entrées pour les URL et 500 entrées pour les hâchés de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6abab-130">The Tenant Allow/Block List allows a maximum of 500 entries for URLs, and 500 entries for file hashes.</span></span>

- <span data-ttu-id="6abab-131">Le nombre maximal de caractères pour chaque entrée est :</span><span class="sxs-lookup"><span data-stu-id="6abab-131">The maximum number of characters for each entry is:</span></span>
  - <span data-ttu-id="6abab-132">Hèmes de fichier = 64</span><span class="sxs-lookup"><span data-stu-id="6abab-132">File hashes = 64</span></span>
  - <span data-ttu-id="6abab-133">URL = 250</span><span class="sxs-lookup"><span data-stu-id="6abab-133">URL = 250</span></span>

- <span data-ttu-id="6abab-134">Une entrée doit être active dans les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="6abab-134">An entry should be active within 30 minutes.</span></span>

- <span data-ttu-id="6abab-135">Par défaut, les entrées de la liste d’inscriptions au client sont expirées au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="6abab-135">By default, entries in the Tenant Allow/Block List will expire after 30 days.</span></span> <span data-ttu-id="6abab-136">Vous pouvez spécifier une date ou les définir pour qu’elles n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="6abab-136">You can specify a date or set them to never expire.</span></span>

- <span data-ttu-id="6abab-137">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="6abab-137">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="6abab-138">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="6abab-138">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="6abab-139">Des autorisations doivent vous avoir été attribuées dans Exchange Online pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="6abab-139">You need to be assigned permissions in Exchange Online before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="6abab-140">**URL et fichiers**:</span><span class="sxs-lookup"><span data-stu-id="6abab-140">**URLs and files**:</span></span>
    - <span data-ttu-id="6abab-141">Pour ajouter et supprimer des valeurs de la liste d’attente des locataires, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="6abab-141">To add and remove values from the Tenant Allow/Block List, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
    - <span data-ttu-id="6abab-142">Pour un accès en lecture seule à la liste des locataires  autorisé/bloqué, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="6abab-142">For read-only access to the Tenant Allow/Block List, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>
  - <span data-ttu-id="6abab-143">**Usurpation :** l’une des combinaisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="6abab-143">**Spoofing**: One of the following combinations:</span></span>
    - <span data-ttu-id="6abab-144">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="6abab-144">**Organization Management**</span></span>
    - <span data-ttu-id="6abab-145">**Administrateur de la** <u>sécurité et</u> **configuration en affichage seul** ou gestion **de l’organisation en affichage seul.**</span><span class="sxs-lookup"><span data-stu-id="6abab-145">**Security Administrator** <u>and</u> **View-Only Configuration** or **View-Only Organization Management**.</span></span>

  <span data-ttu-id="6abab-146">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="6abab-146">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="6abab-147">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6abab-147">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="6abab-148">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6abab-148">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="6abab-149">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6abab-149">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-block-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-150">Utiliser le portail Microsoft 365 Defender pour créer des entrées d’URL de blocage dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-150">Use the Microsoft 365 Defender portal to create block URL entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="6abab-151">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="6abab-151">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="6abab-152">Dans la page Liste d’adresses  client **autoriser/bloquer,** vérifiez que l’onglet URL est sélectionné, puis cliquez sur Bloquer l’icône ![ ](../../media/m365-cc-sc-create-icon.png) **Bloquer.**</span><span class="sxs-lookup"><span data-stu-id="6abab-152">On the **Tenant Allow/Block List** page, verify that the **URLs** tab is selected, and then click ![Block icon](../../media/m365-cc-sc-create-icon.png) **Block**.</span></span>

3. <span data-ttu-id="6abab-153">Dans le **volant Bloquer les URL** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6abab-153">In the **Block URLs** flyout that appears, configure the following settings:</span></span>
   - <span data-ttu-id="6abab-154">**Ajouter des URL avec des caractères génériques**: entrez une URL par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="6abab-154">**Add URLs with wildcards**: Enter one URL per line, up to a maximum of 20.</span></span> <span data-ttu-id="6abab-155">Pour plus d’informations sur la syntaxe des entrées d’URL, voir la [syntaxe d’URL](#url-syntax-for-the-tenant-allowblock-list) pour la section Tenant Allow/Block List plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6abab-155">For details about the syntax for URL entries, see the [URL syntax for the Tenant Allow/Block List](#url-syntax-for-the-tenant-allowblock-list) section later in this article.</span></span>
   - <span data-ttu-id="6abab-156">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6abab-156">**Never expire**: Do one of the following steps:</span></span>
     - <span data-ttu-id="6abab-157">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la zone Supprimer sur pour spécifier la ![ date d’expiration ](../../media/scc-toggle-off.png) des entrées. </span><span class="sxs-lookup"><span data-stu-id="6abab-157">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Remove on** box to specify the expiration date for the entries.</span></span>

       <span data-ttu-id="6abab-158">ou</span><span class="sxs-lookup"><span data-stu-id="6abab-158">or</span></span>

     - <span data-ttu-id="6abab-159">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="6abab-159">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="6abab-161">.</span><span class="sxs-lookup"><span data-stu-id="6abab-161">.</span></span>
   - <span data-ttu-id="6abab-162">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="6abab-162">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="6abab-163">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6abab-163">When you're finished, click **Add**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-block-file-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-164">Utiliser le portail Microsoft 365 Defender pour créer des entrées de fichiers bloqués dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="6abab-164">Use the Microsoft 365 Defender portal to create block file entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="6abab-165">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="6abab-165">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="6abab-166">Dans la page Liste des clients **autoriser/bloquer,** sélectionnez l’onglet **Fichiers,** puis cliquez sur Bloquer l’icône ![ ](../../media/m365-cc-sc-create-icon.png) **Bloquer.**</span><span class="sxs-lookup"><span data-stu-id="6abab-166">On the **Tenant Allow/Block List** page, select the **Files** tab, and then click ![Block icon](../../media/m365-cc-sc-create-icon.png) **Block**.</span></span>

3. <span data-ttu-id="6abab-167">Dans le **volant Bloquer les fichiers** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6abab-167">In the **Block files** flyout that appears, configure the following settings:</span></span>
   - <span data-ttu-id="6abab-168">**Ajouter des hachages de fichier**: entrez une valeur de hachage SHA256 par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="6abab-168">**Add file hashes**: Enter one SHA256 hash value per line, up to a maximum of 20.</span></span>
   - <span data-ttu-id="6abab-169">**N’expirez jamais**: faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6abab-169">**Never expire**: Do one of the following steps:</span></span>
     - <span data-ttu-id="6abab-170">Vérifiez que le paramètre est désactivé (basculement désactivé) et utilisez la zone Supprimer sur pour spécifier la ![ date d’expiration ](../../media/scc-toggle-off.png) des entrées. </span><span class="sxs-lookup"><span data-stu-id="6abab-170">Verify the setting is turned off (![Toggle off](../../media/scc-toggle-off.png)) and use the **Remove on** box to specify the expiration date for the entries.</span></span>

     <span data-ttu-id="6abab-171">ou</span><span class="sxs-lookup"><span data-stu-id="6abab-171">or</span></span>

     - <span data-ttu-id="6abab-172">Déplacez le basculement vers la droite pour configurer les entrées pour qu’ils n’expirent jamais :</span><span class="sxs-lookup"><span data-stu-id="6abab-172">Move the toggle to the right to configure the entries to never expire:</span></span> ![Activer](../../media/scc-toggle-on.png)<span data-ttu-id="6abab-174">.</span><span class="sxs-lookup"><span data-stu-id="6abab-174">.</span></span>
   - <span data-ttu-id="6abab-175">**Remarque facultative**: entrez un texte descriptif pour les entrées.</span><span class="sxs-lookup"><span data-stu-id="6abab-175">**Optional note**: Enter descriptive text for the entries.</span></span>

4. <span data-ttu-id="6abab-176">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6abab-176">When you're finished, click **Add**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-177">Utiliser le portail Microsoft 365 Defender pour créer des entrées d’expéditeurs usurpées dans la liste d’expéditeurs bloqués ou d’adresses de client</span><span class="sxs-lookup"><span data-stu-id="6abab-177">Use the Microsoft 365 Defender portal to create allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-178">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="6abab-178">**Notes**:</span></span>

- <span data-ttu-id="6abab-179">Seule la _combinaison_ de l’utilisateur usurpé et de l’infrastructure d’envoi, telle que définie dans la paire de domaines, est spécifiquement autorisée ou bloquée à l’usurpation. </span><span class="sxs-lookup"><span data-stu-id="6abab-179">Only the _combination_ of the spoofed user _and_ the sending infrastructure as defined in the domain pair is specifically allowed or blocked from spoofing.</span></span>
- <span data-ttu-id="6abab-180">Lorsque vous configurez une entrée d’autoriser ou de bloquer une paire de domaines, les messages provenant de cette paire de domaines n’apparaissent plus dans l’aperçu de l’usurpation d’intelligence.</span><span class="sxs-lookup"><span data-stu-id="6abab-180">When you configure an allow or block entry for a domain pair, messages from that domain pair no longer appear in the spoof intelligence insight.</span></span>
- <span data-ttu-id="6abab-181">Les entrées des expéditeurs usurpés n’expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="6abab-181">Entries for spoofed senders never expire.</span></span>

1. <span data-ttu-id="6abab-182">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="6abab-182">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="6abab-183">Dans la page **Client autoriser/Bloquer la liste,** sélectionnez l’onglet **Usurpation** d’informations, puis cliquez sur Bloquer ![ l’icône ](../../media/m365-cc-sc-create-icon.png) **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="6abab-183">On the **Tenant Allow/Block List** page, select the **Spoofing** tab, and then click ![Block icon](../../media/m365-cc-sc-create-icon.png) **Add**.</span></span>

3. <span data-ttu-id="6abab-184">Dans le **volant Ajouter de nouvelles paires de domaines** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6abab-184">In the **Add new domain pairs** flyout that appears, configure the following settings:</span></span>
   - <span data-ttu-id="6abab-185">**Ajoutez de nouvelles paires de domaines avec des caractères génériques**: entrez une paire de domaines par ligne, jusqu’à un maximum de 20.</span><span class="sxs-lookup"><span data-stu-id="6abab-185">**Add new domain pairs with wildcards**: Enter one domain pair per line, up to a maximum of 20.</span></span> <span data-ttu-id="6abab-186">Pour plus d’informations sur la syntaxe des entrées d’expéditeur usurpées, voir la syntaxe de paire domaine pour les entrées d’expéditeur usurpées dans la section Client [Autoriser/Bloquer](#domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list) la liste plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6abab-186">For details about the syntax for spoofed sender entries, see the [Domain pair syntax for spoofed sender entries in the Tenant Allow/Block List](#domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list) section later in this article.</span></span>
   - <span data-ttu-id="6abab-187">**Type d’usurpation**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6abab-187">**Spoof type**: Select one of the following values:</span></span>
     - <span data-ttu-id="6abab-188">**Interne**: l’expéditeur usurpé se trouve dans un domaine appartenant à votre organisation [(un domaine accepté).](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)</span><span class="sxs-lookup"><span data-stu-id="6abab-188">**Internal**: The spoofed sender is in a domain that belongs to your organization (an [accepted domain](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)).</span></span>
     - <span data-ttu-id="6abab-189">**Externe**: l’expéditeur usurpé se trouve dans un domaine externe.</span><span class="sxs-lookup"><span data-stu-id="6abab-189">**External**: The spoofed sender is in an external domain.</span></span>
   - <span data-ttu-id="6abab-190">**Action**: **sélectionnez Autoriser** ou **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="6abab-190">**Action**: Select **Allow** or **Block**.</span></span>

4. <span data-ttu-id="6abab-191">Lorsque vous avez terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6abab-191">When you're finished, click **Add**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-192">Utiliser le portail Microsoft 365 Defender pour afficher les entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="6abab-192">Use the Microsoft 365 Defender portal to view entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="6abab-193">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="6abab-193">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="6abab-194">Sélectionnez l’onglet de votre choix.</span><span class="sxs-lookup"><span data-stu-id="6abab-194">Select the tab you want.</span></span> <span data-ttu-id="6abab-195">Les colonnes disponibles dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="6abab-195">The columns that are available depend on the tab you selected:</span></span>

   - <span data-ttu-id="6abab-196">**URL**:</span><span class="sxs-lookup"><span data-stu-id="6abab-196">**URLs**:</span></span>
     - <span data-ttu-id="6abab-197">**Valeur**: URL.</span><span class="sxs-lookup"><span data-stu-id="6abab-197">**Value**: The URL.</span></span>
     - <span data-ttu-id="6abab-198">**Action**: La valeur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="6abab-198">**Action**: The value **Block**.</span></span>
     - <span data-ttu-id="6abab-199">**Dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="6abab-199">**Last updated**</span></span>
     - <span data-ttu-id="6abab-200">**Supprimer le**</span><span class="sxs-lookup"><span data-stu-id="6abab-200">**Remove on**</span></span>
     - <span data-ttu-id="6abab-201">**Notes**</span><span class="sxs-lookup"><span data-stu-id="6abab-201">**Notes**</span></span>
   - <span data-ttu-id="6abab-202">**Files**</span><span class="sxs-lookup"><span data-stu-id="6abab-202">**Files**</span></span>
     - <span data-ttu-id="6abab-203">**Valeur**: hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="6abab-203">**Value**: The file hash.</span></span>
     - <span data-ttu-id="6abab-204">**Action**: La valeur **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="6abab-204">**Action**: The value **Block**.</span></span>
     - <span data-ttu-id="6abab-205">**Dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="6abab-205">**Last updated**</span></span>
     - <span data-ttu-id="6abab-206">**Supprimer le**</span><span class="sxs-lookup"><span data-stu-id="6abab-206">**Remove on**</span></span>
     - <span data-ttu-id="6abab-207">**Notes**</span><span class="sxs-lookup"><span data-stu-id="6abab-207">**Notes**</span></span>
   - <span data-ttu-id="6abab-208">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="6abab-208">**Spoofing**</span></span>
     - <span data-ttu-id="6abab-209">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="6abab-209">**Spoofed user**</span></span>
     - <span data-ttu-id="6abab-210">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="6abab-210">**Sending infrastructure**</span></span>
     - <span data-ttu-id="6abab-211">**Type d’usurpation**: valeur **Interne** ou **Externe.**</span><span class="sxs-lookup"><span data-stu-id="6abab-211">**Spoof type**: The value **Internal** or **External**.</span></span>
     - <span data-ttu-id="6abab-212">**Action**: la valeur **Bloquer ou** **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="6abab-212">**Action**: The value **Block** or **Allow**.</span></span>

   <span data-ttu-id="6abab-213">Vous pouvez cliquer sur un en-tête de colonne pour trier par ordre croissant ou décroit.</span><span class="sxs-lookup"><span data-stu-id="6abab-213">You can click on a column heading to sort in ascending or descending order.</span></span>

   <span data-ttu-id="6abab-214">Vous pouvez cliquer sur **Groupe** pour grouper les résultats.</span><span class="sxs-lookup"><span data-stu-id="6abab-214">You can click **Group** to group the results.</span></span> <span data-ttu-id="6abab-215">Les valeurs disponibles dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="6abab-215">The values that are available depend on the tab you selected:</span></span>

   - <span data-ttu-id="6abab-216">**URL : vous** pouvez grouper les résultats par **action.**</span><span class="sxs-lookup"><span data-stu-id="6abab-216">**URLs**: You can group the results by **Action**.</span></span>
   - <span data-ttu-id="6abab-217">**Fichiers**: vous pouvez grouper les résultats par **action.**</span><span class="sxs-lookup"><span data-stu-id="6abab-217">**Files**: You can group the results by **Action**.</span></span>
   - <span data-ttu-id="6abab-218">**Usurpation :** vous pouvez grouper les résultats par **action** ou **type d’usurpation.**</span><span class="sxs-lookup"><span data-stu-id="6abab-218">**Spoofing**: You can group the results by **Action** or **Spoof type**.</span></span>

   <span data-ttu-id="6abab-219">Cliquez **sur** Rechercher, entrez une partie ou l’ensemble d’une valeur, puis appuyez sur Entrée pour trouver une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="6abab-219">Click **Search**, enter all or part of a value, and then press ENTER to find a specific value.</span></span> <span data-ttu-id="6abab-220">Lorsque vous avez terminé, cliquez sur ![ Effacer l’icône de recherche ](../../media/m365-cc-sc-close-icon.png) **Effacer la recherche.**</span><span class="sxs-lookup"><span data-stu-id="6abab-220">When you're finished, click ![Clear search icon](../../media/m365-cc-sc-close-icon.png) **Clear search**.</span></span>

   <span data-ttu-id="6abab-221">Cliquez **sur Filtrer** pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="6abab-221">Click **Filter** to filter the results.</span></span> <span data-ttu-id="6abab-222">Les valeurs disponibles dans le flyout **Filter** qui s’affiche dépendent de l’onglet que vous avez sélectionné :</span><span class="sxs-lookup"><span data-stu-id="6abab-222">The values that are available in **Filter** flyout that appears depend on the tab you selected:</span></span>

   - <span data-ttu-id="6abab-223">**URL**</span><span class="sxs-lookup"><span data-stu-id="6abab-223">**URLs**</span></span>
     - <span data-ttu-id="6abab-224">**Action**</span><span class="sxs-lookup"><span data-stu-id="6abab-224">**Action**</span></span>
     - <span data-ttu-id="6abab-225">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="6abab-225">**Never expire**</span></span>
     - <span data-ttu-id="6abab-226">**Date de la dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="6abab-226">**Last updated date**</span></span>
     - <span data-ttu-id="6abab-227">**Supprimer le**</span><span class="sxs-lookup"><span data-stu-id="6abab-227">**Remove on**</span></span>
   - <span data-ttu-id="6abab-228">**Files**</span><span class="sxs-lookup"><span data-stu-id="6abab-228">**Files**</span></span>
     - <span data-ttu-id="6abab-229">**Action**</span><span class="sxs-lookup"><span data-stu-id="6abab-229">**Action**</span></span>
     - <span data-ttu-id="6abab-230">**Ne jamais expirer**</span><span class="sxs-lookup"><span data-stu-id="6abab-230">**Never expire**</span></span>
     - <span data-ttu-id="6abab-231">**Dernière mise à jour**</span><span class="sxs-lookup"><span data-stu-id="6abab-231">**Last updated**</span></span>
     - <span data-ttu-id="6abab-232">**Supprimer le**</span><span class="sxs-lookup"><span data-stu-id="6abab-232">**Remove on**</span></span>
   - <span data-ttu-id="6abab-233">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="6abab-233">**Spoofing**</span></span>
     - <span data-ttu-id="6abab-234">**Action**</span><span class="sxs-lookup"><span data-stu-id="6abab-234">**Action**</span></span>
     - <span data-ttu-id="6abab-235">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="6abab-235">**Spoof type**</span></span>

   <span data-ttu-id="6abab-236">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="6abab-236">When you're finished, click **Apply**.</span></span> <span data-ttu-id="6abab-237">Pour effacer les filtres existants,  cliquez sur **Filtrer** et, dans le volant de filtre qui s’affiche, cliquez **sur Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="6abab-237">To clear existing filters, click **Filter**, and in the **Filter** flyout that appears, click **Clear filters**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-238">Utiliser le portail Microsoft 365 Defender pour modifier des entrées dans la liste d’attente des locataires</span><span class="sxs-lookup"><span data-stu-id="6abab-238">Use the Microsoft 365 Defender portal to modify entries in the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="6abab-239">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="6abab-239">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="6abab-240">Sélectionnez l’onglet qui contient le type d’entrée à modifier :</span><span class="sxs-lookup"><span data-stu-id="6abab-240">Select the tab that contains the type of entry that you want to modify:</span></span>
   - <span data-ttu-id="6abab-241">**URL**</span><span class="sxs-lookup"><span data-stu-id="6abab-241">**URLs**</span></span>
   - <span data-ttu-id="6abab-242">**Files**</span><span class="sxs-lookup"><span data-stu-id="6abab-242">**Files**</span></span>
   - <span data-ttu-id="6abab-243">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="6abab-243">**Spoofing**</span></span>

3. <span data-ttu-id="6abab-244">Sélectionnez l’entrée à modifier, puis cliquez sur ![ Modifier ](../../media/m365-cc-sc-edit-icon.png) **l’icône Modifier.**</span><span class="sxs-lookup"><span data-stu-id="6abab-244">Select the entry that you want to modify, and then click ![Edit icon](../../media/m365-cc-sc-edit-icon.png) **Edit**.</span></span> <span data-ttu-id="6abab-245">Les valeurs que vous pouvez modifier dans le volant qui s’affiche dépendent de l’onglet que vous avez sélectionné à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="6abab-245">The values that you are able to modify in the flyout that appears depend on the tab you selected in the previous step:</span></span>
   - <span data-ttu-id="6abab-246">**URL**</span><span class="sxs-lookup"><span data-stu-id="6abab-246">**URLs**</span></span>
     - <span data-ttu-id="6abab-247">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="6abab-247">**Never expire** and/or expiration date.</span></span>
     - <span data-ttu-id="6abab-248">**Note facultative**</span><span class="sxs-lookup"><span data-stu-id="6abab-248">**Optional note**</span></span>
   - <span data-ttu-id="6abab-249">**Files**</span><span class="sxs-lookup"><span data-stu-id="6abab-249">**Files**</span></span>
     - <span data-ttu-id="6abab-250">**Ne jamais expirer** et/ou date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="6abab-250">**Never expire** and/or expiration date.</span></span>
     - <span data-ttu-id="6abab-251">**Note facultative**</span><span class="sxs-lookup"><span data-stu-id="6abab-251">**Optional note**</span></span>
   - <span data-ttu-id="6abab-252">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="6abab-252">**Spoofing**</span></span>
     - <span data-ttu-id="6abab-253">**Action**: vous pouvez modifier la valeur sur **Autoriser** ou **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="6abab-253">**Action**: You can change the value to **Allow** or **Block**.</span></span>
4. <span data-ttu-id="6abab-254">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6abab-254">When you're finished, click **Save**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-255">Utiliser le portail Microsoft 365 Defender pour supprimer des entrées de la liste des locataires autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-255">Use the Microsoft 365 Defender portal to remove entries from the Tenant Allow/Block List</span></span>

1. <span data-ttu-id="6abab-256">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span><span class="sxs-lookup"><span data-stu-id="6abab-256">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Rules** section \> **Tenant Allow/Block Lists**.</span></span>

2. <span data-ttu-id="6abab-257">Sélectionnez l’onglet qui contient le type d’entrée à supprimer :</span><span class="sxs-lookup"><span data-stu-id="6abab-257">Select the tab that contains the type of entry that you want to remove:</span></span>
   - <span data-ttu-id="6abab-258">**URL**</span><span class="sxs-lookup"><span data-stu-id="6abab-258">**URLs**</span></span>
   - <span data-ttu-id="6abab-259">**Files**</span><span class="sxs-lookup"><span data-stu-id="6abab-259">**Files**</span></span>
   - <span data-ttu-id="6abab-260">**Usurpation**</span><span class="sxs-lookup"><span data-stu-id="6abab-260">**Spoofing**</span></span>

3. <span data-ttu-id="6abab-261">Sélectionnez l’entrée à supprimer, puis cliquez sur ![ Supprimer ](../../media/m365-cc-sc-delete-icon.png) **l’icône Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="6abab-261">Select the entry that you want to remove, and then click ![Delete icon](../../media/m365-cc-sc-delete-icon.png) **Delete**.</span></span>

4. <span data-ttu-id="6abab-262">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="6abab-262">In the warning dialog that appears, click **Delete**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-263">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-263">Use Exchange Online PowerShell or standalone EOP PowerShell to configure the Tenant Allow/Block List</span></span>

### <a name="use-powershell-to-add-block-file-or-url-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-264">Utiliser PowerShell pour ajouter des entrées de bloc de fichier ou d’URL à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-264">Use PowerShell to add block file or URL entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-265">Pour ajouter des entrées de blocage de fichier ou d’URL dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-265">To add block file or URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListItems -ListType <FileHash | Url> -Block -Entries "Value1","Value2",..."ValueN" <-ExpirationDate Date | -NoExpiration> [-Notes <String>]
```

<span data-ttu-id="6abab-266">Cet exemple ajoute une entrée de fichier de blocage pour les fichiers spécifiés qui n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="6abab-266">This example adds a block file entry for the specified files that never expires.</span></span>

```powershell
New-TenantAllowBlockListItem -ListType FileHash -Block -Entries "768a813668695ef2483b2bde7cf5d1b2db0423a0d3e63e498f3ab6f2eb13ea3","2c0a35409ff0873cfa28b70b8224e9aca2362241c1f0ed6f622fef8d4722fd9a" -NoExpiration
```

<span data-ttu-id="6abab-267">Cet exemple ajoute une entrée d’URL de bloc pour contoso.com et tous les sous-contoso.com (par exemple, contoso.com, www.contoso.com et xyz.abc.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="6abab-267">This example adds a block URL entry for contoso.com and all subdomains (for example, contoso.com, www.contoso.com, and xyz.abc.contoso.com).</span></span> <span data-ttu-id="6abab-268">Étant donné que nous n’avons pas utilisé les paramètres ExpirationDate ou NoExpiration, l’entrée expire au bout de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="6abab-268">Because we didn't use the ExpirationDate or NoExpiration parameters, the entry expires after 30 days.</span></span>

```powershell
New-TenantAllowBlockListItems -ListType Url -Block -Entries ~contoso.com
```

<span data-ttu-id="6abab-269">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-269">For detailed syntax and parameter information, see [New-TenantAllowBlockListItems](/powershell/module/exchange/new-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-add-allow-or-block-spoofed-sender-entries-to-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-270">Utiliser PowerShell pour ajouter des entrées d’expéditeurs usurpés ou autoriser ou bloquer à la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-270">Use PowerShell to add allow or block spoofed sender entries to the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-271">Pour ajouter des entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-271">To add spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
New-TenantAllowBlockListSpoofItems -SpoofedUser <Domain | EmailAddress | *> -SendingInfrastructure <Domain | IPAddress/24> -SpoofType <External | Internal> -Action <Allow | Block>
```

<span data-ttu-id="6abab-272">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TenantAllowBlockListSpoofItems](/powershell/module/exchange/new-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-272">For detailed syntax and parameter information, see [New-TenantAllowBlockListSpoofItems](/powershell/module/exchange/new-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-view-block-file-or-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-273">Utiliser PowerShell pour afficher les entrées de fichier ou d’URL bloqués dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-273">Use PowerShell to view block file or URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-274">Pour afficher les entrées de fichier ou d’URL bloqués dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-274">To view block file or URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType <FileHash | URL> [-Entry <FileHashValue | URLValue>] [<-ExpirationDate Date | -NoExpiration>]
```

<span data-ttu-id="6abab-275">Cet exemple renvoie des informations pour la valeur de hachage de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6abab-275">This example returns information for the specified file hash value.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType FileHash -Entry "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"
```

<span data-ttu-id="6abab-276">Cet exemple renvoie toutes les URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="6abab-276">This example returns all blocked URLs.</span></span>

```powershell
Get-TenantAllowBlockListItems -ListType Url -Block
```

<span data-ttu-id="6abab-277">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-277">For detailed syntax and parameter information, see [Get-TenantAllowBlockListItems](/powershell/module/exchange/get-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-view-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-278">Utiliser PowerShell pour afficher ou bloquer les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-278">Use PowerShell to view allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-279">Pour afficher les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-279">To view spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems [-Action <Allow | Block>] [-SpoofType <External | Internal>
```

<span data-ttu-id="6abab-280">Cet exemple renvoie toutes les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="6abab-280">This example returns all spoofed sender entries in the Tenant Allow/Block List.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems
```

<span data-ttu-id="6abab-281">Cet exemple renvoie toutes les entrées d’expéditeur usurpées qui sont internes.</span><span class="sxs-lookup"><span data-stu-id="6abab-281">This example returns all allow spoofed sender entries that are internal.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems -Action Allow -SpoofType Internal
```

<span data-ttu-id="6abab-282">Cet exemple renvoie toutes les entrées d’expéditeur usurpées bloquées qui sont externes.</span><span class="sxs-lookup"><span data-stu-id="6abab-282">This example returns all blocked spoofed sender entries that are external.</span></span>

```powershell
Get-TenantAllowBlockListSpoofItems -Action Block -SpoofType External
```

<span data-ttu-id="6abab-283">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-TenantAllowBlockListSpoofItems](/powershell/module/exchange/get-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-283">For detailed syntax and parameter information, see [Get-TenantAllowBlockListSpoofItems](/powershell/module/exchange/get-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-modify-block-file-and-url-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-284">Utiliser PowerShell pour modifier les entrées de blocage de fichiers et d’URL dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-284">Use PowerShell to modify block file and URL entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-285">Pour modifier les entrées de blocage de fichiers et d’URL dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-285">To modify block file and URL entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType <FileHash | Url> -Ids <"Id1","Id2",..."IdN"> [<-ExpirationDate Date | -NoExpiration>] [-Notes <String>]
```

<span data-ttu-id="6abab-286">Cet exemple modifie la date d’expiration de l’entrée d’URL de bloc spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6abab-286">This example changes the expiration date of the specified block URL entry.</span></span>

```powershell
Set-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -ExpirationDate "5/30/2020"
```

<span data-ttu-id="6abab-287">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-287">For detailed syntax and parameter information, see [Set-TenantAllowBlockListItems](/powershell/module/exchange/set-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-modify-allow-or-block-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-288">Utiliser PowerShell pour modifier les entrées d’expéditeurs usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-288">Use PowerShell to modify allow or block spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-289">Pour modifier les entrées d’expéditeurs usurpées dans la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-289">To modify allow or block spoofed sender entries in the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Set-TenantAllowBlockListSpoofItems -Ids <"Id1","Id2",..."IdN"> -Action <Allow | Block>
```

<span data-ttu-id="6abab-290">Cet exemple modifie l’entrée de l’expéditeur usurpé de l’adresse « allow » à « block ».</span><span class="sxs-lookup"><span data-stu-id="6abab-290">This example changes spoofed sender entry from allow to block.</span></span>

```powershell
Set-TenantAllowBlockListItems -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSRAAAA" -Action Block
```

<span data-ttu-id="6abab-291">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-TenantAllowBlockListSpoofItems](/powershell/module/exchange/set-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-291">For detailed syntax and parameter information, see [Set-TenantAllowBlockListSpoofItems](/powershell/module/exchange/set-tenantallowblocklistspoofitems).</span></span>

### <a name="use-powershell-to-remove-url-or-file-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-292">Utiliser PowerShell pour supprimer l’URL ou les entrées de fichier de la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-292">Use PowerShell to remove URL or file entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-293">Pour supprimer des entrées de fichier et d’URL de la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-293">To remove file and URL entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType <FileHash | Url> -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="6abab-294">Cet exemple supprime l’entrée d’URL de bloc spécifiée de la liste d’adresses client autoriser/bloquer.</span><span class="sxs-lookup"><span data-stu-id="6abab-294">This example removes the specified block URL entry from the Tenant Allow/Block List.</span></span>

```powershell
Remove-TenantAllowBlockListItems -ListType Url -Ids "RgAAAAAI8gSyI_NmQqzeh-HXJBywBwCqfQNJY8hBTbdlKFkv6BcUAAAl_QCZAACqfQNJY8hBTbdlKFkv6BcUAAAl_oSPAAAA0"
```

<span data-ttu-id="6abab-295">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-295">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListItems](/powershell/module/exchange/remove-tenantallowblocklistitems).</span></span>

### <a name="use-powershell-to-remove-allow-or-block-spoofed-sender-entries-from-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-296">Utiliser PowerShell pour supprimer les entrées d’expéditeurs usurpées de la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-296">Use PowerShell to remove allow or block spoofed sender entries from the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-297">Pour supprimer les entrées d’expéditeurs usurpant l’usurpation d’adresse de client de la liste d’adresses client autoriser/bloquer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-297">To remove allow or block spoof sender entries from the Tenant Allow/Block List, use the following syntax:</span></span>

```powershell
Remove-TenantAllowBlockListSpoofItems -Ids <"Id1","Id2",..."IdN">
```

<span data-ttu-id="6abab-298">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-TenantAllowBlockListSpoofItems](/powershell/module/exchange/remove-tenantallowblocklistspoofitems).</span><span class="sxs-lookup"><span data-stu-id="6abab-298">For detailed syntax and parameter information, see [Remove-TenantAllowBlockListSpoofItems](/powershell/module/exchange/remove-tenantallowblocklistspoofitems).</span></span>

## <a name="url-syntax-for-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-299">Syntaxe d’URL pour la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-299">URL syntax for the Tenant Allow/Block List</span></span>

- <span data-ttu-id="6abab-300">Les adresses IP4v et IPv6 sont autorisées, mais pas les ports TCP/UDP.</span><span class="sxs-lookup"><span data-stu-id="6abab-300">IP4v and IPv6 addresses are allowed, but TCP/UDP ports are not.</span></span>

- <span data-ttu-id="6abab-301">Les extensions de nom de fichier ne sont pas autorisées (par exemple, test.pdf).</span><span class="sxs-lookup"><span data-stu-id="6abab-301">Filename extensions are not allowed (for example, test.pdf).</span></span>

- <span data-ttu-id="6abab-302">Unicode n’est pas pris en charge, mais c’est le cas de Punycode.</span><span class="sxs-lookup"><span data-stu-id="6abab-302">Unicode is not supported, but Punycode is.</span></span>

- <span data-ttu-id="6abab-303">Les noms d’hôte sont autorisés si toutes les instructions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="6abab-303">Hostnames are allowed if all of the following statements are true:</span></span>
  - <span data-ttu-id="6abab-304">Le nom d’hôte contient un point.</span><span class="sxs-lookup"><span data-stu-id="6abab-304">The hostname contains a period.</span></span>
  - <span data-ttu-id="6abab-305">Il y a au moins un caractère à gauche du point.</span><span class="sxs-lookup"><span data-stu-id="6abab-305">There is at least one character to the left of the period.</span></span>
  - <span data-ttu-id="6abab-306">Il y a au moins deux caractères à droite du point.</span><span class="sxs-lookup"><span data-stu-id="6abab-306">There are at least two characters to the right of the period.</span></span>

  <span data-ttu-id="6abab-307">Par exemple, `t.co` est autorisé ou `.com` `contoso.` non.</span><span class="sxs-lookup"><span data-stu-id="6abab-307">For example, `t.co` is allowed; `.com` or `contoso.` are not allowed.</span></span>

- <span data-ttu-id="6abab-308">Les sous-chemins ne sont pas implicites.</span><span class="sxs-lookup"><span data-stu-id="6abab-308">Subpaths are not implied.</span></span>

  <span data-ttu-id="6abab-309">Par exemple, `contoso.com` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="6abab-309">For example, `contoso.com` does not include `contoso.com/a`.</span></span>

- <span data-ttu-id="6abab-310">Les caractères génériques (\*) sont autorisés dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="6abab-310">Wildcards (\*) are allowed in the following scenarios:</span></span>

  - <span data-ttu-id="6abab-311">Un caractère générique gauche doit être suivi d’un point pour spécifier un sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="6abab-311">A left wildcard must be followed by a period to specify a subdomain.</span></span>

    <span data-ttu-id="6abab-312">Par exemple, `*.contoso.com` est autorisé ; `*contoso.com` n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="6abab-312">For example, `*.contoso.com` is allowed; `*contoso.com` is not allowed.</span></span>

  - <span data-ttu-id="6abab-313">Un caractère générique droit doit suivre une barre oblique (/) pour spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="6abab-313">A right wildcard must follow a forward slash (/) to specify a path.</span></span>

    <span data-ttu-id="6abab-314">Par exemple, `contoso.com/*` est autorisé ou `contoso.com*` `contoso.com/ab*` non.</span><span class="sxs-lookup"><span data-stu-id="6abab-314">For example, `contoso.com/*` is allowed; `contoso.com*` or `contoso.com/ab*` are not allowed.</span></span>

  - <span data-ttu-id="6abab-315">Tous les sous-chemins ne sont pas impliqués par un caractère générique de droite.</span><span class="sxs-lookup"><span data-stu-id="6abab-315">All subpaths are not implied by a right wildcard.</span></span>

    <span data-ttu-id="6abab-316">Par exemple, `contoso.com/*` n’inclut pas `contoso.com/a` .</span><span class="sxs-lookup"><span data-stu-id="6abab-316">For example, `contoso.com/*` does not include `contoso.com/a`.</span></span>

  - <span data-ttu-id="6abab-317">`*.com*` n’est pas valide (domaine non résolvable et le caractère générique droit ne suit pas une barre oblique).</span><span class="sxs-lookup"><span data-stu-id="6abab-317">`*.com*` is invalid (not a resolvable domain and the right wildcard does not follow a forward slash).</span></span>

  - <span data-ttu-id="6abab-318">Les caractères génériques ne sont pas autorisés dans les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="6abab-318">Wildcards are not allowed in IP addresses.</span></span>

- <span data-ttu-id="6abab-319">Le caractère tilde (~) est disponible dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="6abab-319">The tilde (~) character is available in the following scenarios:</span></span>

  - <span data-ttu-id="6abab-320">Un tilde gauche implique un domaine et tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="6abab-320">A left tilde implies a domain and all subdomains.</span></span>

    <span data-ttu-id="6abab-321">Par `~contoso.com` exemple, `contoso.com` inclut et `*.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="6abab-321">For example `~contoso.com` includes `contoso.com` and `*.contoso.com`.</span></span>

- <span data-ttu-id="6abab-322">Les entrées d’URL qui contiennent des protocoles (par exemple, , ou ) échouent, car les entrées `http://` `https://` `ftp://` d’URL s’appliquent à tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="6abab-322">URL entries that contain protocols (for example, `http://`, `https://`, or `ftp://`) will fail, because URL entries apply to all protocols.</span></span>

- <span data-ttu-id="6abab-323">Un nom d’utilisateur ou un mot de passe ne sont pas pris en charge ou requis.</span><span class="sxs-lookup"><span data-stu-id="6abab-323">A username or password aren't supported or required.</span></span>

- <span data-ttu-id="6abab-324">Les guillemets (' ou « ) sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="6abab-324">Quotes (' or ") are invalid characters.</span></span>

- <span data-ttu-id="6abab-325">Une URL doit inclure toutes les redirections lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="6abab-325">A URL should include all redirects where possible.</span></span>

### <a name="url-entry-scenarios"></a><span data-ttu-id="6abab-326">Scénarios d’entrée d’URL</span><span class="sxs-lookup"><span data-stu-id="6abab-326">URL entry scenarios</span></span>

<span data-ttu-id="6abab-327">Les entrées d’URL valides et leurs résultats sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6abab-327">Valid URL entries and their results are described in the following sections.</span></span>

#### <a name="scenario-no-wildcards"></a><span data-ttu-id="6abab-328">Scénario : aucun caractère générique</span><span class="sxs-lookup"><span data-stu-id="6abab-328">Scenario: No wildcards</span></span>

<span data-ttu-id="6abab-329">**Entrée**: `contoso.com`</span><span class="sxs-lookup"><span data-stu-id="6abab-329">**Entry**: `contoso.com`</span></span>

- <span data-ttu-id="6abab-330">**Autoriser la correspondance**: contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-330">**Allow match**: contoso.com</span></span>

- <span data-ttu-id="6abab-331">**Autoriser non la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-331">**Allow not matched**:</span></span>

  - <span data-ttu-id="6abab-332">abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-332">abc-contoso.com</span></span>
  - <span data-ttu-id="6abab-333">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="6abab-333">contoso.com/a</span></span>
  - <span data-ttu-id="6abab-334">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-334">payroll.contoso.com</span></span>
  - <span data-ttu-id="6abab-335">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-335">test.com/contoso.com</span></span>
  - <span data-ttu-id="6abab-336">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-336">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="6abab-337">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-337">www.contoso.com</span></span>
  - <span data-ttu-id="6abab-338">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-338">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="6abab-339">**Bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-339">**Block match**:</span></span>

  - <span data-ttu-id="6abab-340">contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-340">contoso.com</span></span>
  - <span data-ttu-id="6abab-341">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="6abab-341">contoso.com/a</span></span>
  - <span data-ttu-id="6abab-342">payroll.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-342">payroll.contoso.com</span></span>
  - <span data-ttu-id="6abab-343">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-343">test.com/contoso.com</span></span>
  - <span data-ttu-id="6abab-344">test.com/q=contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-344">test.com/q=contoso.com</span></span>
  - <span data-ttu-id="6abab-345">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-345">www.contoso.com</span></span>
  - <span data-ttu-id="6abab-346">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-346">www.contoso.com/q=a@contoso.com</span></span>

- <span data-ttu-id="6abab-347">**Bloc non correspond :** abc-contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-347">**Block not matched**: abc-contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain"></a><span data-ttu-id="6abab-348">Scénario : caractère générique gauche (sous-domaine)</span><span class="sxs-lookup"><span data-stu-id="6abab-348">Scenario: Left wildcard (subdomain)</span></span>

<span data-ttu-id="6abab-349">**Entrée**: `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="6abab-349">**Entry**: `*.contoso.com`</span></span>

- <span data-ttu-id="6abab-350">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-350">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-351">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-351">www.contoso.com</span></span>
  - <span data-ttu-id="6abab-352">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-352">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="6abab-353">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="6abab-353">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="6abab-354">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-354">123contoso.com</span></span>
  - <span data-ttu-id="6abab-355">contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-355">contoso.com</span></span>
  - <span data-ttu-id="6abab-356">test.com/contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-356">test.com/contoso.com</span></span>
  - <span data-ttu-id="6abab-357">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="6abab-357">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-at-top-of-path"></a><span data-ttu-id="6abab-358">Scénario : caractère générique droit en haut du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6abab-358">Scenario: Right wildcard at top of path</span></span>

<span data-ttu-id="6abab-359">**Entrée**: `contoso.com/a/*`</span><span class="sxs-lookup"><span data-stu-id="6abab-359">**Entry**: `contoso.com/a/*`</span></span>

- <span data-ttu-id="6abab-360">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-360">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-361">contoso.com/a/b</span><span class="sxs-lookup"><span data-stu-id="6abab-361">contoso.com/a/b</span></span>
  - <span data-ttu-id="6abab-362">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="6abab-362">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="6abab-363">contoso.com/a/?q=joe@t.com</span><span class="sxs-lookup"><span data-stu-id="6abab-363">contoso.com/a/?q=joe@t.com</span></span>

- <span data-ttu-id="6abab-364">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="6abab-364">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="6abab-365">contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-365">contoso.com</span></span>
  - <span data-ttu-id="6abab-366">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="6abab-366">contoso.com/a</span></span>
  - <span data-ttu-id="6abab-367">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-367">www.contoso.com</span></span>
  - <span data-ttu-id="6abab-368">www.contoso.com/q=a@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-368">www.contoso.com/q=a@contoso.com</span></span>

#### <a name="scenario-left-tilde"></a><span data-ttu-id="6abab-369">Scénario : tilde gauche</span><span class="sxs-lookup"><span data-stu-id="6abab-369">Scenario: Left tilde</span></span>

<span data-ttu-id="6abab-370">**Entrée**: `~contoso.com`</span><span class="sxs-lookup"><span data-stu-id="6abab-370">**Entry**: `~contoso.com`</span></span>

- <span data-ttu-id="6abab-371">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-371">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-372">contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-372">contoso.com</span></span>
  - <span data-ttu-id="6abab-373">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-373">www.contoso.com</span></span>
  - <span data-ttu-id="6abab-374">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-374">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="6abab-375">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="6abab-375">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="6abab-376">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-376">123contoso.com</span></span>
  - <span data-ttu-id="6abab-377">contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="6abab-377">contoso.com/abc</span></span>
  - <span data-ttu-id="6abab-378">www.contoso.com/abc</span><span class="sxs-lookup"><span data-stu-id="6abab-378">www.contoso.com/abc</span></span>

#### <a name="scenario-right-wildcard-suffix"></a><span data-ttu-id="6abab-379">Scénario : suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="6abab-379">Scenario: Right wildcard suffix</span></span>

<span data-ttu-id="6abab-380">**Entrée**: `contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="6abab-380">**Entry**: `contoso.com/*`</span></span>

- <span data-ttu-id="6abab-381">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-381">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-382">contoso.com/?q=whatever@fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="6abab-382">contoso.com/?q=whatever@fabrikam.com</span></span>
  - <span data-ttu-id="6abab-383">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="6abab-383">contoso.com/a</span></span>
  - <span data-ttu-id="6abab-384">contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="6abab-384">contoso.com/a/b/c</span></span>
  - <span data-ttu-id="6abab-385">contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="6abab-385">contoso.com/ab</span></span>
  - <span data-ttu-id="6abab-386">contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="6abab-386">contoso.com/b</span></span>
  - <span data-ttu-id="6abab-387">contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="6abab-387">contoso.com/b/a/c</span></span>
  - <span data-ttu-id="6abab-388">contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="6abab-388">contoso.com/ba</span></span>

- <span data-ttu-id="6abab-389">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-389">**Allow not matched** and **Block not matched**: contoso.com</span></span>

#### <a name="scenario-left-wildcard-subdomain-and-right-wildcard-suffix"></a><span data-ttu-id="6abab-390">Scénario : sous-domaine générique gauche et suffixe générique droit</span><span class="sxs-lookup"><span data-stu-id="6abab-390">Scenario: Left wildcard subdomain and right wildcard suffix</span></span>

<span data-ttu-id="6abab-391">**Entrée**: `*.contoso.com/*`</span><span class="sxs-lookup"><span data-stu-id="6abab-391">**Entry**: `*.contoso.com/*`</span></span>

- <span data-ttu-id="6abab-392">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-392">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-393">abc.contoso.com/ab</span><span class="sxs-lookup"><span data-stu-id="6abab-393">abc.contoso.com/ab</span></span>
  - <span data-ttu-id="6abab-394">abc.xyz.contoso.com/a/b/c</span><span class="sxs-lookup"><span data-stu-id="6abab-394">abc.xyz.contoso.com/a/b/c</span></span>
  - <span data-ttu-id="6abab-395">www.contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="6abab-395">www.contoso.com/a</span></span>
  - <span data-ttu-id="6abab-396">www.contoso.com/b/a/c</span><span class="sxs-lookup"><span data-stu-id="6abab-396">www.contoso.com/b/a/c</span></span>
  - <span data-ttu-id="6abab-397">xyz.contoso.com/ba</span><span class="sxs-lookup"><span data-stu-id="6abab-397">xyz.contoso.com/ba</span></span>

- <span data-ttu-id="6abab-398">**Autoriser non la correspondance et** Bloquer non correspond **:** contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="6abab-398">**Allow not matched** and **Block not matched**: contoso.com/b</span></span>

#### <a name="scenario-left-and-right-tilde"></a><span data-ttu-id="6abab-399">Scénario : tilde gauche et droite</span><span class="sxs-lookup"><span data-stu-id="6abab-399">Scenario: Left and right tilde</span></span>

<span data-ttu-id="6abab-400">**Entrée**: `~contoso.com~`</span><span class="sxs-lookup"><span data-stu-id="6abab-400">**Entry**: `~contoso.com~`</span></span>

- <span data-ttu-id="6abab-401">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-401">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-402">contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-402">contoso.com</span></span>
  - <span data-ttu-id="6abab-403">contoso.com/a</span><span class="sxs-lookup"><span data-stu-id="6abab-403">contoso.com/a</span></span>
  - <span data-ttu-id="6abab-404">www.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-404">www.contoso.com</span></span>
  - <span data-ttu-id="6abab-405">www.contoso.com/b</span><span class="sxs-lookup"><span data-stu-id="6abab-405">www.contoso.com/b</span></span>
  - <span data-ttu-id="6abab-406">xyz.abc.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-406">xyz.abc.contoso.com</span></span>

- <span data-ttu-id="6abab-407">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="6abab-407">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="6abab-408">123contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-408">123contoso.com</span></span>
  - <span data-ttu-id="6abab-409">contoso.org</span><span class="sxs-lookup"><span data-stu-id="6abab-409">contoso.org</span></span>

#### <a name="scenario-ip-address"></a><span data-ttu-id="6abab-410">Scénario : adresse IP</span><span class="sxs-lookup"><span data-stu-id="6abab-410">Scenario: IP address</span></span>

<span data-ttu-id="6abab-411">**Entrée**: `1.2.3.4`</span><span class="sxs-lookup"><span data-stu-id="6abab-411">**Entry**: `1.2.3.4`</span></span>

- <span data-ttu-id="6abab-412">**Autoriser la correspondance** **et bloquer la correspondance**: 1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="6abab-412">**Allow match** and **Block match**: 1.2.3.4</span></span>

- <span data-ttu-id="6abab-413">**Autoriser non la correspondance et** Bloquer non correspond **:**</span><span class="sxs-lookup"><span data-stu-id="6abab-413">**Allow not matched** and **Block not matched**:</span></span>

  - <span data-ttu-id="6abab-414">1.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="6abab-414">1.2.3.4/a</span></span>
  - <span data-ttu-id="6abab-415">11.2.3.4/a</span><span class="sxs-lookup"><span data-stu-id="6abab-415">11.2.3.4/a</span></span>

#### <a name="ip-address-with-right-wildcard"></a><span data-ttu-id="6abab-416">Adresse IP avec caractère générique droit</span><span class="sxs-lookup"><span data-stu-id="6abab-416">IP address with right wildcard</span></span>

<span data-ttu-id="6abab-417">**Entrée**: `1.2.3.4/*`</span><span class="sxs-lookup"><span data-stu-id="6abab-417">**Entry**: `1.2.3.4/*`</span></span>

- <span data-ttu-id="6abab-418">**Autoriser la correspondance** et **bloquer la correspondance**:</span><span class="sxs-lookup"><span data-stu-id="6abab-418">**Allow match** and **Block match**:</span></span>

  - <span data-ttu-id="6abab-419">1.2.3.4/b</span><span class="sxs-lookup"><span data-stu-id="6abab-419">1.2.3.4/b</span></span>
  - <span data-ttu-id="6abab-420">1.2.3.4/baaaa</span><span class="sxs-lookup"><span data-stu-id="6abab-420">1.2.3.4/baaaa</span></span>

### <a name="examples-of-invalid-entries"></a><span data-ttu-id="6abab-421">Exemples d’entrées non valides</span><span class="sxs-lookup"><span data-stu-id="6abab-421">Examples of invalid entries</span></span>

<span data-ttu-id="6abab-422">Les entrées suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="6abab-422">The following entries are invalid:</span></span>

- <span data-ttu-id="6abab-423">**Valeurs de domaine manquantes ou non valides**:</span><span class="sxs-lookup"><span data-stu-id="6abab-423">**Missing or invalid domain values**:</span></span>

  - <span data-ttu-id="6abab-424">contoso</span><span class="sxs-lookup"><span data-stu-id="6abab-424">contoso</span></span>
  - <span data-ttu-id="6abab-425">\*.contoso.\*</span><span class="sxs-lookup"><span data-stu-id="6abab-425">\*.contoso.\*</span></span>
  - <span data-ttu-id="6abab-426">\*.com</span><span class="sxs-lookup"><span data-stu-id="6abab-426">\*.com</span></span>
  - <span data-ttu-id="6abab-427">\*.pdf</span><span class="sxs-lookup"><span data-stu-id="6abab-427">\*.pdf</span></span>

- <span data-ttu-id="6abab-428">**Caractère générique sur du texte ou sans espacement**:</span><span class="sxs-lookup"><span data-stu-id="6abab-428">**Wildcard on text or without spacing characters**:</span></span>

  - <span data-ttu-id="6abab-429">\*contoso.com</span><span class="sxs-lookup"><span data-stu-id="6abab-429">\*contoso.com</span></span>
  - <span data-ttu-id="6abab-430">contoso.com\*</span><span class="sxs-lookup"><span data-stu-id="6abab-430">contoso.com\*</span></span>
  - <span data-ttu-id="6abab-431">\*1.2.3.4</span><span class="sxs-lookup"><span data-stu-id="6abab-431">\*1.2.3.4</span></span>
  - <span data-ttu-id="6abab-432">1.2.3.4\*</span><span class="sxs-lookup"><span data-stu-id="6abab-432">1.2.3.4\*</span></span>
  - <span data-ttu-id="6abab-433">contoso.com/a\*</span><span class="sxs-lookup"><span data-stu-id="6abab-433">contoso.com/a\*</span></span>
  - <span data-ttu-id="6abab-434">contoso.com/ab\*</span><span class="sxs-lookup"><span data-stu-id="6abab-434">contoso.com/ab\*</span></span>

- <span data-ttu-id="6abab-435">**Adresses IP avec ports**:</span><span class="sxs-lookup"><span data-stu-id="6abab-435">**IP addresses with ports**:</span></span>

  - <span data-ttu-id="6abab-436">contoso.com:443</span><span class="sxs-lookup"><span data-stu-id="6abab-436">contoso.com:443</span></span>
  - <span data-ttu-id="6abab-437">abc.contoso.com:25</span><span class="sxs-lookup"><span data-stu-id="6abab-437">abc.contoso.com:25</span></span>

- <span data-ttu-id="6abab-438">**Caractères génériques non descriptifs**:</span><span class="sxs-lookup"><span data-stu-id="6abab-438">**Non-descriptive wildcards**:</span></span>

  - \*
  - <span data-ttu-id="6abab-439">\*.\*</span><span class="sxs-lookup"><span data-stu-id="6abab-439">\*.\*</span></span>

- <span data-ttu-id="6abab-440">**Caractères génériques intermédiaires**:</span><span class="sxs-lookup"><span data-stu-id="6abab-440">**Middle wildcards**:</span></span>

  - <span data-ttu-id="6abab-441">conto \* so.com</span><span class="sxs-lookup"><span data-stu-id="6abab-441">conto\*so.com</span></span>
  - <span data-ttu-id="6abab-442">conto~so.com</span><span class="sxs-lookup"><span data-stu-id="6abab-442">conto~so.com</span></span>

- <span data-ttu-id="6abab-443">**Caractères génériques doubles**</span><span class="sxs-lookup"><span data-stu-id="6abab-443">**Double wildcards**</span></span>

  - <span data-ttu-id="6abab-444">contoso.com/\*\*</span><span class="sxs-lookup"><span data-stu-id="6abab-444">contoso.com/\*\*</span></span>
  - <span data-ttu-id="6abab-445">contoso.com/\*/\*</span><span class="sxs-lookup"><span data-stu-id="6abab-445">contoso.com/\*/\*</span></span>

## <a name="domain-pair-syntax-for-spoofed-sender-entries-in-the-tenant-allowblock-list"></a><span data-ttu-id="6abab-446">Syntaxe de paire de domaines pour les entrées d’expéditeur usurpées dans la liste d’adresses client autoriser/bloquer</span><span class="sxs-lookup"><span data-stu-id="6abab-446">Domain pair syntax for spoofed sender entries in the Tenant Allow/Block List</span></span>

<span data-ttu-id="6abab-447">Une paire de domaines pour un expéditeur usurpé dans la liste d’adresses client autoriser/bloquer utilise la syntaxe suivante `<Spoofed user>, <Sending infrastructure>` :</span><span class="sxs-lookup"><span data-stu-id="6abab-447">A domain pair for a spoofed sender in the Tenant Allow/Block List uses the following syntax: `<Spoofed user>, <Sending infrastructure>`.</span></span>

- <span data-ttu-id="6abab-448">**Utilisateur usurpé**: cette valeur implique l’adresse e-mail de l’utilisateur  usurpé qui s’affiche dans la zone De des clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6abab-448">**Spoofed user**: This value involves the email address of the spoofed user that's displayed in the **From** box in email clients.</span></span> <span data-ttu-id="6abab-449">Cette adresse est également appelée `5322.From` adresse.</span><span class="sxs-lookup"><span data-stu-id="6abab-449">This address is also known as the `5322.From` address.</span></span> <span data-ttu-id="6abab-450">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6abab-450">Valid values include:</span></span>
  - <span data-ttu-id="6abab-451">Adresse de messagerie individuelle (par exemple, chris@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="6abab-451">An individual email address (for example, chris@contoso.com).</span></span>
  - <span data-ttu-id="6abab-452">Un domaine de messagerie (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="6abab-452">An email domain (for example, contoso.com).</span></span>
  - <span data-ttu-id="6abab-453">Caractère générique (par exemple, \* ).</span><span class="sxs-lookup"><span data-stu-id="6abab-453">The wildcard character (for example, \*).</span></span>

- <span data-ttu-id="6abab-454">**Infrastructure d’envoi**: cette valeur indique la source des messages de l’utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="6abab-454">**Sending infrastructure**: This value indicates the source of messages from the spoofed user.</span></span> <span data-ttu-id="6abab-455">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6abab-455">Valid values include:</span></span>
  - <span data-ttu-id="6abab-456">Domaine trouvé dans une recherche DNS inversée (enregistrement PTR) de l’adresse IP du serveur de messagerie source (par exemple, fabrikam.com).</span><span class="sxs-lookup"><span data-stu-id="6abab-456">The domain found in a reverse DNS lookup (PTR record) of the source email server's IP address (for example, fabrikam.com).</span></span>
  - <span data-ttu-id="6abab-457">Si l’adresse IP source n’a pas d’enregistrement PTR, l’infrastructure d’envoi est identifiée comme \<source IP\> /24 (par exemple, 192.168.100.100/24).</span><span class="sxs-lookup"><span data-stu-id="6abab-457">If the source IP address has no PTR record, then the sending infrastructure is identified as \<source IP\>/24 (for example, 192.168.100.100/24).</span></span>

<span data-ttu-id="6abab-458">Voici quelques exemples de paires de domaines valides pour identifier les expéditeurs usurpés :</span><span class="sxs-lookup"><span data-stu-id="6abab-458">Here are some examples of valid domain pairs to identify spoofed senders:</span></span>

- `contoso.com, 192.168.100.100/24`
- `chris@contoso.com, fabrikam.com`
- `*, contoso.net`

<span data-ttu-id="6abab-459">Le nombre maximal d’entrées d’expéditeur usurpées est de 1 000.</span><span class="sxs-lookup"><span data-stu-id="6abab-459">The maximum number of spoofed sender entries is 1000.</span></span>

<span data-ttu-id="6abab-460">L’ajout d’une paire de domaines autorise ou bloque uniquement la *combinaison* de l’utilisateur usurpé *et* de l’infrastructure d’envoi.</span><span class="sxs-lookup"><span data-stu-id="6abab-460">Adding a domain pair only allows or blocks the *combination* of the spoofed user *and* the sending infrastructure.</span></span> <span data-ttu-id="6abab-461">Il n’autorise pas le courrier électronique provenant de l’utilisateur usurpé d’aucune source, ni le courrier provenant de la source d’infrastructure d’envoi pour tout utilisateur usurpé.</span><span class="sxs-lookup"><span data-stu-id="6abab-461">It does not allow email from the spoofed user from any source, nor does it allow email from the sending infrastructure source for any spoofed user.</span></span> 

<span data-ttu-id="6abab-462">Par exemple, vous ajoutez une entrée d’accès pour la paire de domaines suivante :</span><span class="sxs-lookup"><span data-stu-id="6abab-462">For example, you add an allow entry for the following domain pair:</span></span>

- <span data-ttu-id="6abab-463">**Domaine**: gmail.com</span><span class="sxs-lookup"><span data-stu-id="6abab-463">**Domain**: gmail.com</span></span>
- <span data-ttu-id="6abab-464">**Infrastructure**: tms.mx.com</span><span class="sxs-lookup"><span data-stu-id="6abab-464">**Infrastructure**: tms.mx.com</span></span>

<span data-ttu-id="6abab-465">Seuls les messages provenant de ce domaine et *de* cette paire d’infrastructure d’envoi sont autorisés à usurper l’usurpation.</span><span class="sxs-lookup"><span data-stu-id="6abab-465">Only messages from that domain *and* sending infrastructure pair are allowed to spoof.</span></span> <span data-ttu-id="6abab-466">Les autres expéditeurs qui tentent d’usurper gmail.com ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="6abab-466">Other senders attempting to spoof gmail.com aren't allowed.</span></span> <span data-ttu-id="6abab-467">Les messages provenant d’expéditeurs d’autres domaines tms.mx.com sont vérifiés par la veille contre l’usurpation d’adresse.</span><span class="sxs-lookup"><span data-stu-id="6abab-467">Messages from senders in other domains originating from tms.mx.com are checked by spoof intelligence.</span></span>
