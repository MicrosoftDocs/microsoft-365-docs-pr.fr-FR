---
title: Centre d’administration Exchange dans EOP autonome
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
ms.collection:
- M365-security-compliance
description: Découvrez l’interface de gestion Web dans Exchange Online Protection (EOP).
ms.openlocfilehash: 777597489e54c642220cb42f0c686b675101897f
ms.sourcegitcommit: 73b2426001dc5a3f4b857366ef51e877db549098
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2020
ms.locfileid: "44616997"
---
# <a name="exchange-admin-center-in-standalone-eop"></a><span data-ttu-id="356c2-103">Centre d’administration Exchange dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="356c2-103">Exchange admin center in standalone EOP</span></span>

<span data-ttu-id="356c2-104">Le centre d’administration Exchange (EAA) est une console de gestion basée sur le Web pour Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="356c2-104">The Exchange admin center (EAC) is a web-based management console for standalone Exchange Online Protection (EOP).</span></span>

<span data-ttu-id="356c2-105">Vous recherchez la version Exchange Online de cette rubrique ?</span><span class="sxs-lookup"><span data-stu-id="356c2-105">Looking for the Exchange Online version of this topic?</span></span> <span data-ttu-id="356c2-106">Consultez la rubrique [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="356c2-106">See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

## <a name="open-the-eac-in-eop"></a><span data-ttu-id="356c2-107">Ouvrir le centre d’administration Exchange dans EOP</span><span class="sxs-lookup"><span data-stu-id="356c2-107">Open the EAC in EOP</span></span>

<span data-ttu-id="356c2-108">Les clients EOP autonomes peuvent accéder au centre d’administration Exchange à l’aide des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="356c2-108">Standalone EOP customers can access the EAC by using the following methods:</span></span>

- <span data-ttu-id="356c2-109">**À partir du centre d’administration Microsoft 365**:</span><span class="sxs-lookup"><span data-stu-id="356c2-109">**From the Microsoft 365 admin center**:</span></span>

  1. <span data-ttu-id="356c2-110">Accédez à <https://admin.microsoft.com> et cliquez sur **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="356c2-110">Go to <https://admin.microsoft.com> and click **Show all**.</span></span>

     ![Cliquez sur Afficher tout dans le centre d’administration Microsoft 365](../../media/m365-center-show-all.png)

  2. <span data-ttu-id="356c2-112">Dans la section **centres d’administration** qui s’affiche, cliquez sur **tous les centres d’administration**.</span><span class="sxs-lookup"><span data-stu-id="356c2-112">In the **Admin centers** section that appears, click **All admin centers**.</span></span>

     ![Cliquez sur tous les centres d’administration dans le centre d’administration Microsoft 365](../../media/m365-center-select-all-admin-centers.png)

  3. <span data-ttu-id="356c2-114">Sur la page **tous les centres d’administration** qui s’affiche, cliquez sur **Exchange Online Protection**.</span><span class="sxs-lookup"><span data-stu-id="356c2-114">On the **All admin centers** page that appears, click **Exchange Online Protection**.</span></span>

- <span data-ttu-id="356c2-115">Accédez directement à `https://admin.protection.outlook.com/ecp/` .</span><span class="sxs-lookup"><span data-stu-id="356c2-115">Go directly to `https://admin.protection.outlook.com/ecp/`.</span></span>

## <a name="common-user-interface-elements-in-the-eac-in-eop"></a><span data-ttu-id="356c2-116">Éléments d’interface utilisateur courants dans le centre d’administration Exchange dans EOP</span><span class="sxs-lookup"><span data-stu-id="356c2-116">Common user interface elements in the EAC in EOP</span></span>

<span data-ttu-id="356c2-117">Cette section décrit les éléments d'interface utilisateur disponibles dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="356c2-117">This section describes the user interface elements that are found in the EAC.</span></span>

![EOP-AdminCenter](../../media/EOP-AdminCenter.png)

### <a name="feature-pane"></a><span data-ttu-id="356c2-119">Volet des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="356c2-119">Feature Pane</span></span>

<span data-ttu-id="356c2-p102">Il s'agit du premier niveau de navigation pour la plupart des tâches que vous effectuez au sein du CAE. Le volet des fonctionnalités est organisé par domaines de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="356c2-p102">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>

- <span data-ttu-id="356c2-122">**Destinataires**: c’est ici que vous pouvez afficher les groupes et les contacts externes.</span><span class="sxs-lookup"><span data-stu-id="356c2-122">**Recipients**: This is where you'll view groups and external contacts.</span></span>

- <span data-ttu-id="356c2-123">**Autorisations**: ce qui vous permet de gérer les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="356c2-123">**Permissions**: This where you'll manage admin roles.</span></span>

- <span data-ttu-id="356c2-124">**Gestion**de la conformité : c’est ici que vous trouverez le rapport de groupe de rôles d’administrateur et le rapport du journal d’audit de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="356c2-124">**Compliance Management**: This is where you'll find the administrator role group report and the admin audit log report.</span></span>

- <span data-ttu-id="356c2-125">**Protection**: c’est ici que vous pouvez gérer les stratégies de protection contre les programmes malveillants, la stratégie de filtrage des connexions par défaut et DKIM.</span><span class="sxs-lookup"><span data-stu-id="356c2-125">**Protection**: This is where you can manage anti-malware policies, the default connection filter policy, and DKIM.</span></span>

  > [!NOTE]
  > <span data-ttu-id="356c2-126">Vous devez gérer les stratégies anti-programme malveillant et la stratégie de filtrage des connexions par défaut dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="356c2-126">You should manage anti-malware policies and the default connection filter policy in the Security & Compliance Center.</span></span> <span data-ttu-id="356c2-127">Pour plus d’informations, consultez la rubrique [configurer des stratégies anti-programmes malveillants dans EOP](configure-anti-malware-policies.md) et [configurer le filtrage des connexions dans EOP](configure-the-connection-filter-policy.md).</span><span class="sxs-lookup"><span data-stu-id="356c2-127">For more information, see [Configure anti-malware policies in EOP](configure-anti-malware-policies.md) and [Configure connection filtering in EOP](configure-the-connection-filter-policy.md).</span></span>

- <span data-ttu-id="356c2-128">**Flux de messagerie**: c’est ici que vous gérerez les règles de flux de messagerie (également appelées règles de transport), les domaines acceptés et les connecteurs, ainsi que les emplacements où vous pouvez exécuter le suivi des messages.</span><span class="sxs-lookup"><span data-stu-id="356c2-128">**Mail Flow**: This is where you'll manage mail flow rules (also known as transport rules), accepted domains, and connectors, as well as where you can go to run message trace.</span></span>

- <span data-ttu-id="356c2-129">**Hybride**: c’est ici que vous pouvez exécuter l' [Assistant Configuration hybride](https://docs.microsoft.com/Exchange/hybrid-configuration-wizard)et où vous pouvez installer le [module Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/mfa-connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="356c2-129">**Hybrid**: This is where you can run the [Hybrid Configuration Wizard](https://docs.microsoft.com/Exchange/hybrid-configuration-wizard), and where you can install the [Exchange Online PowerShell module](https://docs.microsoft.com/powershell/exchange/mfa-connect-to-exchange-online-powershell).</span></span>

### <a name="tabs"></a><span data-ttu-id="356c2-130">Onglets</span><span class="sxs-lookup"><span data-stu-id="356c2-130">Tabs</span></span>

<span data-ttu-id="356c2-p104">Les onglets constituent votre deuxième niveau de navigation. Chaque domaine de fonctionnalités contient différents onglets, chacun représentant une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="356c2-p104">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>

### <a name="toolbar"></a><span data-ttu-id="356c2-133">Barre d'outils</span><span class="sxs-lookup"><span data-stu-id="356c2-133">Toolbar</span></span>

<span data-ttu-id="356c2-p105">Lorsque vous cliquez sur la plupart des onglets, vous devez voir une barre d'outils. La barre d'outils contient des icônes qui correspondent à une action spécifique. Le tableau suivant décrit les icônes et leurs actions.</span><span class="sxs-lookup"><span data-stu-id="356c2-p105">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>

||||
|---|---|---|
|<span data-ttu-id="356c2-137">**Icône**</span><span class="sxs-lookup"><span data-stu-id="356c2-137">**Icon**</span></span>|<span data-ttu-id="356c2-138">**Nom**</span><span class="sxs-lookup"><span data-stu-id="356c2-138">**Name**</span></span>|<span data-ttu-id="356c2-139">**Action**</span><span class="sxs-lookup"><span data-stu-id="356c2-139">**Action**</span></span>|
|![Icône Ajouter](../../media/ITPro-EAC-AddIcon.gif)|<span data-ttu-id="356c2-141">Ajouter, Nouveau</span><span class="sxs-lookup"><span data-stu-id="356c2-141">Add, New</span></span>|<span data-ttu-id="356c2-p106">Permet de créer un objet. Certaines de ces icônes comportent une flèche vers le bas associée, sur laquelle vous pouvez cliquer pour afficher des objets supplémentaires que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="356c2-p106">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>|
|![Icône Modifier](../../media/ITPro-EAC-EditIcon.gif)|<span data-ttu-id="356c2-145">Modifier</span><span class="sxs-lookup"><span data-stu-id="356c2-145">Edit</span></span>|<span data-ttu-id="356c2-146">Permet de modifier un objet.</span><span class="sxs-lookup"><span data-stu-id="356c2-146">Use this icon to edit an object.</span></span>|
|![Icône Supprimer](../../media/ITPro-EAC-DeleteIcon.gif)|<span data-ttu-id="356c2-148">Supprimer</span><span class="sxs-lookup"><span data-stu-id="356c2-148">Delete</span></span>|<span data-ttu-id="356c2-p107">Permet de supprimer un objet. Certaines des icônes de suppression comportent une flèche vers le bas, sur laquelle vous pouvez cliquer pour afficher des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="356c2-p107">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>|
|![Icône Recherche](../../media/ITPro-EAC-.gif)|<span data-ttu-id="356c2-152">Rechercher</span><span class="sxs-lookup"><span data-stu-id="356c2-152">Search</span></span>|<span data-ttu-id="356c2-153">Permet d'ouvrir une zone de recherche dans laquelle vous pouvez entrer une expression pour rechercher un objet.</span><span class="sxs-lookup"><span data-stu-id="356c2-153">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>|
|![Icône Actualiser](../../media/ITPro-EAC-RefreshIcon.gif)|<span data-ttu-id="356c2-155">Actualiser</span><span class="sxs-lookup"><span data-stu-id="356c2-155">Refresh</span></span>|<span data-ttu-id="356c2-156">Permet d'actualiser l'affichage Liste.</span><span class="sxs-lookup"><span data-stu-id="356c2-156">Use this icon to refresh the list view.</span></span>|
|![Icône Options supplémentaires](../../media/ITPro-EAC-MoreOptionsIcon.gif)|<span data-ttu-id="356c2-158">Plus d'options</span><span class="sxs-lookup"><span data-stu-id="356c2-158">More options</span></span>|<span data-ttu-id="356c2-p108">Utilisez cette icône pour afficher d'autres actions que vous pouvez effectuer pour les objets figurant sous cet onglet. Par exemple, dans **Destinataires \> Utilisateurs**, le fait de cliquer sur cette icône affiche l'option de **Recherche avancée**.  </span><span class="sxs-lookup"><span data-stu-id="356c2-p108">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.</span></span>|
|![Icône flèche vers le haut](../../media/ITPro-EAC-UpArrowIcon.gif)![Icône de flèche vers le bas](../../media/ITPro-EAC-DownArrowIcon.gif)|<span data-ttu-id="356c2-163">Flèche Haut et flèche Bas</span><span class="sxs-lookup"><span data-stu-id="356c2-163">Up arrow and down arrow</span></span>|<span data-ttu-id="356c2-164">Utilisez ces icônes pour relever ou abaisser la priorité d'un objet.</span><span class="sxs-lookup"><span data-stu-id="356c2-164">Use these icons to move an object's priority up or down.</span></span>|
|![Icône Suppression](../../media/ITPro-EAC-RemoveIcon.gif)|<span data-ttu-id="356c2-166">Supprimer</span><span class="sxs-lookup"><span data-stu-id="356c2-166">Remove</span></span>|<span data-ttu-id="356c2-167">Permet de supprimer des objets d'une liste.</span><span class="sxs-lookup"><span data-stu-id="356c2-167">Use this icon to remove objects from a list.</span></span>|
|

### <a name="list-view"></a><span data-ttu-id="356c2-168">Affichage Liste</span><span class="sxs-lookup"><span data-stu-id="356c2-168">List View</span></span>

<span data-ttu-id="356c2-p109">Dans la plupart des cas, vous devez voir un affichage Liste lorsque vous sélectionnez un onglet. La limite d'affichage de l'affichage Liste du CAE est d'environ 10 000 objets. En outre, la pagination est incluse pour vous permettre de paginer les résultats.</span><span class="sxs-lookup"><span data-stu-id="356c2-p109">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>

### <a name="details-pane"></a><span data-ttu-id="356c2-172">Volet d'informations</span><span class="sxs-lookup"><span data-stu-id="356c2-172">Details Pane</span></span>

<span data-ttu-id="356c2-p110">Quand vous sélectionnez un objet de l'affichage Liste, les informations relatives à cet objet apparaissent dans le volet d'informations. Dans certains cas, le volet d'informations inclut les tâches de gestion.</span><span class="sxs-lookup"><span data-stu-id="356c2-p110">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>

### <a name="me-tile-and-help"></a><span data-ttu-id="356c2-175">Vignette de l'utilisateur en cours et Aide</span><span class="sxs-lookup"><span data-stu-id="356c2-175">Me tile and Help</span></span>

<span data-ttu-id="356c2-p111">La vignette **Moi** vous permet de fermer votre session du Centre d'administration Exchange (CAE) pour ouvrir ensuite une session en tant qu'utilisateur différent. Dans le menu déroulant **Aide**![Icône d'aide](../../media/ITPro-EAC-HelpIcon.gif), vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="356c2-p111">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](../../media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can perform the following actions:</span></span>

- <span data-ttu-id="356c2-178">**Aide**: cliquez sur l' ![ icône aide ](../../media/ITPro-EAC-HelpIcon.gif) pour afficher le contenu de l’aide en ligne.</span><span class="sxs-lookup"><span data-stu-id="356c2-178">**Help**: Click ![Help Icon](../../media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span>

- <span data-ttu-id="356c2-179">**Commentaires**: laisser une évaluation.</span><span class="sxs-lookup"><span data-stu-id="356c2-179">**Feedback**: Leave feedback.</span></span>

- <span data-ttu-id="356c2-180">**Communauté**: Publiez une question pour trouver des réponses dans les forums de la communauté.</span><span class="sxs-lookup"><span data-stu-id="356c2-180">**Community**: Post a question for find answers in the community forums.</span></span>

- <span data-ttu-id="356c2-181">**Désactiver la bulle d'** aide : la bulle d’aide affiche une aide contextuelle pour les champs lorsque vous créez ou modifiez un objet.</span><span class="sxs-lookup"><span data-stu-id="356c2-181">**Disable Help bubble**: The Help bubble displays contextual help for fields when you create or edit an object.</span></span> <span data-ttu-id="356c2-182">Vous pouvez activer ou désactiver la bulle d'aide.</span><span class="sxs-lookup"><span data-stu-id="356c2-182">You can turn off the Help bubble or turn it on if it has been disabled.</span></span>

- <span data-ttu-id="356c2-183">**Afficher la journalisation des commandes**: une nouvelle fenêtre s’ouvre et affiche les commandes PowerShell équivalentes en fonction des informations que vous avez configurées dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="356c2-183">**Show Command Logging**: A new window opens that shows the equivalent PowerShell commands based on what you configured in EAC.</span></span>

## <a name="supported-browsers"></a><span data-ttu-id="356c2-184">Navigateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="356c2-184">Supported Browsers</span></span>

<span data-ttu-id="356c2-185">Pour bénéficier d’une meilleure expérience d’utilisation du CAE, nous vous recommandons de toujours utiliser les navigateurs, clients Office et applications les plus récents.</span><span class="sxs-lookup"><span data-stu-id="356c2-185">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps.</span></span> <span data-ttu-id="356c2-186">Nous vous recommandons également d'installer les mises à jour logicielles lorsqu'elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="356c2-186">We also recommend that you install software updates when they become available.</span></span> <span data-ttu-id="356c2-187">Pour plus d’informations sur les navigateurs pris en charge et la configuration système requise pour le service, voir [Configuration requise pour Office](https://products.office.com/office-system-requirements).</span><span class="sxs-lookup"><span data-stu-id="356c2-187">For more information about the supported browsers and system requirements for the service, see [System requirements for Office](https://products.office.com/office-system-requirements).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="356c2-188">Langues prises en charge</span><span class="sxs-lookup"><span data-stu-id="356c2-188">Supported languages</span></span>

<span data-ttu-id="356c2-189">Les langues suivantes sont prises en charge et disponibles pour le centre d’administration Exchange en mode autonome EOP.</span><span class="sxs-lookup"><span data-stu-id="356c2-189">The following languages are supported and available for the EAC in standalone EOP.</span></span>

- <span data-ttu-id="356c2-190">Amharique</span><span class="sxs-lookup"><span data-stu-id="356c2-190">Amharic</span></span>

- <span data-ttu-id="356c2-191">Arabe</span><span class="sxs-lookup"><span data-stu-id="356c2-191">Arabic</span></span>

- <span data-ttu-id="356c2-192">basque (Basque)</span><span class="sxs-lookup"><span data-stu-id="356c2-192">Basque (Basque)</span></span>

- <span data-ttu-id="356c2-193">Bengla (Inde)</span><span class="sxs-lookup"><span data-stu-id="356c2-193">Bengali (India)</span></span>

- <span data-ttu-id="356c2-194">Bulgare</span><span class="sxs-lookup"><span data-stu-id="356c2-194">Bulgarian</span></span>

- <span data-ttu-id="356c2-195">Catalan</span><span class="sxs-lookup"><span data-stu-id="356c2-195">Catalan</span></span>

- <span data-ttu-id="356c2-196">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="356c2-196">Chinese (Simplified)</span></span>

- <span data-ttu-id="356c2-197">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="356c2-197">Chinese (Traditional)</span></span>

- <span data-ttu-id="356c2-198">Croate</span><span class="sxs-lookup"><span data-stu-id="356c2-198">Croatian</span></span>

- <span data-ttu-id="356c2-199">Tchèque</span><span class="sxs-lookup"><span data-stu-id="356c2-199">Czech</span></span>

- <span data-ttu-id="356c2-200">Danois</span><span class="sxs-lookup"><span data-stu-id="356c2-200">Danish</span></span>

- <span data-ttu-id="356c2-201">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="356c2-201">Dutch</span></span>

- <span data-ttu-id="356c2-202">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="356c2-202">Dutch</span></span>

- <span data-ttu-id="356c2-203">Anglais</span><span class="sxs-lookup"><span data-stu-id="356c2-203">English</span></span>

- <span data-ttu-id="356c2-204">Estonien</span><span class="sxs-lookup"><span data-stu-id="356c2-204">Estonian</span></span>

- <span data-ttu-id="356c2-205">Filipino (Philippines)</span><span class="sxs-lookup"><span data-stu-id="356c2-205">Filipino (Philippines)</span></span>

- <span data-ttu-id="356c2-206">Finnois</span><span class="sxs-lookup"><span data-stu-id="356c2-206">Finnish</span></span>

- <span data-ttu-id="356c2-207">Français</span><span class="sxs-lookup"><span data-stu-id="356c2-207">French</span></span>

- <span data-ttu-id="356c2-208">Galicien</span><span class="sxs-lookup"><span data-stu-id="356c2-208">Galician</span></span>

- <span data-ttu-id="356c2-209">Allemand</span><span class="sxs-lookup"><span data-stu-id="356c2-209">German</span></span>

- <span data-ttu-id="356c2-210">Grec</span><span class="sxs-lookup"><span data-stu-id="356c2-210">Greek</span></span>

- <span data-ttu-id="356c2-211">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="356c2-211">Gujarati</span></span>

- <span data-ttu-id="356c2-212">Hébreu</span><span class="sxs-lookup"><span data-stu-id="356c2-212">Hebrew</span></span>

- <span data-ttu-id="356c2-213">Hindi</span><span class="sxs-lookup"><span data-stu-id="356c2-213">Hindi</span></span>

- <span data-ttu-id="356c2-214">Hongrois</span><span class="sxs-lookup"><span data-stu-id="356c2-214">Hungarian</span></span>

- <span data-ttu-id="356c2-215">Islandais</span><span class="sxs-lookup"><span data-stu-id="356c2-215">Icelandic</span></span>

- <span data-ttu-id="356c2-216">Indonésien</span><span class="sxs-lookup"><span data-stu-id="356c2-216">Indonesian</span></span>

- <span data-ttu-id="356c2-217">Italien</span><span class="sxs-lookup"><span data-stu-id="356c2-217">Italian</span></span>

- <span data-ttu-id="356c2-218">Japonais</span><span class="sxs-lookup"><span data-stu-id="356c2-218">Japanese</span></span>

- <span data-ttu-id="356c2-219">Kannada</span><span class="sxs-lookup"><span data-stu-id="356c2-219">Kannada</span></span>

- <span data-ttu-id="356c2-220">Kazakh</span><span class="sxs-lookup"><span data-stu-id="356c2-220">Kazakh</span></span>

- <span data-ttu-id="356c2-221">Kiswahili</span><span class="sxs-lookup"><span data-stu-id="356c2-221">Kiswahili</span></span>

- <span data-ttu-id="356c2-222">Coréen</span><span class="sxs-lookup"><span data-stu-id="356c2-222">Korean</span></span>

- <span data-ttu-id="356c2-223">Letton</span><span class="sxs-lookup"><span data-stu-id="356c2-223">Latvian</span></span>

- <span data-ttu-id="356c2-224">Lituanien</span><span class="sxs-lookup"><span data-stu-id="356c2-224">Lithuanian</span></span>

- <span data-ttu-id="356c2-225">Malais (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="356c2-225">Malay (Brunei Darussalam)</span></span>

- <span data-ttu-id="356c2-226">Malais (Malaisie)</span><span class="sxs-lookup"><span data-stu-id="356c2-226">Malay (Malaysia)</span></span>

- <span data-ttu-id="356c2-227">Malayalam</span><span class="sxs-lookup"><span data-stu-id="356c2-227">Malayalam</span></span>

- <span data-ttu-id="356c2-228">Marathe</span><span class="sxs-lookup"><span data-stu-id="356c2-228">Marathi</span></span>

- <span data-ttu-id="356c2-229">Norvégien (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="356c2-229">Norwegian (Bokmål)</span></span>

- <span data-ttu-id="356c2-230">Norvégien (nynorsk)</span><span class="sxs-lookup"><span data-stu-id="356c2-230">Norwegian (Nynorsk)</span></span>

- <span data-ttu-id="356c2-231">Odia</span><span class="sxs-lookup"><span data-stu-id="356c2-231">Oriya</span></span>

- <span data-ttu-id="356c2-232">Perse</span><span class="sxs-lookup"><span data-stu-id="356c2-232">Persian</span></span>

- <span data-ttu-id="356c2-233">Polonais</span><span class="sxs-lookup"><span data-stu-id="356c2-233">Polish</span></span>

- <span data-ttu-id="356c2-234">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="356c2-234">Portuguese (Brazil)</span></span>

- <span data-ttu-id="356c2-235">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="356c2-235">Portuguese (Portugal)</span></span>

- <span data-ttu-id="356c2-236">Roumain</span><span class="sxs-lookup"><span data-stu-id="356c2-236">Romanian</span></span>

- <span data-ttu-id="356c2-237">Russe</span><span class="sxs-lookup"><span data-stu-id="356c2-237">Russian</span></span>

- <span data-ttu-id="356c2-238">Serbe (cyrillique, Serbie)</span><span class="sxs-lookup"><span data-stu-id="356c2-238">Serbian (Cyrillic, Serbia)</span></span>

- <span data-ttu-id="356c2-239">Serbe (latin)</span><span class="sxs-lookup"><span data-stu-id="356c2-239">Serbian (Latin)</span></span>

- <span data-ttu-id="356c2-240">Slovaque</span><span class="sxs-lookup"><span data-stu-id="356c2-240">Slovak</span></span>

- <span data-ttu-id="356c2-241">Slovène</span><span class="sxs-lookup"><span data-stu-id="356c2-241">Slovenian</span></span>

- <span data-ttu-id="356c2-242">Espagnol</span><span class="sxs-lookup"><span data-stu-id="356c2-242">Spanish</span></span>

- <span data-ttu-id="356c2-243">Suédois</span><span class="sxs-lookup"><span data-stu-id="356c2-243">Swedish</span></span>

- <span data-ttu-id="356c2-244">Tamoul</span><span class="sxs-lookup"><span data-stu-id="356c2-244">Tamil</span></span>

- <span data-ttu-id="356c2-245">Télougou</span><span class="sxs-lookup"><span data-stu-id="356c2-245">Telugu</span></span>

- <span data-ttu-id="356c2-246">Thaï</span><span class="sxs-lookup"><span data-stu-id="356c2-246">Thai</span></span>

- <span data-ttu-id="356c2-247">Turc</span><span class="sxs-lookup"><span data-stu-id="356c2-247">Turkish</span></span>

- <span data-ttu-id="356c2-248">Ukrainien</span><span class="sxs-lookup"><span data-stu-id="356c2-248">Ukrainian</span></span>

- <span data-ttu-id="356c2-249">Ourdou</span><span class="sxs-lookup"><span data-stu-id="356c2-249">Urdu</span></span>

- <span data-ttu-id="356c2-250">Vietnamien</span><span class="sxs-lookup"><span data-stu-id="356c2-250">Vietnamese</span></span>

- <span data-ttu-id="356c2-251">Gallois</span><span class="sxs-lookup"><span data-stu-id="356c2-251">Welsh</span></span>
