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
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
ms.collection:
- M365-security-compliance
description: Découvrez l’interface de gestion web dans Exchange Online Protection (EOP) autonome.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 81af6c64d2ec3204d0c9d46888bbfe21335955bd
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166218"
---
# <a name="exchange-admin-center-in-standalone-eop"></a><span data-ttu-id="c8e6f-103">Centre d’administration Exchange dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="c8e6f-103">Exchange admin center in standalone EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="c8e6f-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c8e6f-104">**Applies to**</span></span>
-  [<span data-ttu-id="c8e6f-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="c8e6f-105">Exchange Online Protection standalone</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)

<span data-ttu-id="c8e6f-106">Le Centre d’administration Exchange (CAE) est une console de gestion web pour Exchange Online Protection (EOP) autonome.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-106">The Exchange admin center (EAC) is a web-based management console for standalone Exchange Online Protection (EOP).</span></span>

<span data-ttu-id="c8e6f-107">Vous recherchez la version Exchange Online de cette rubrique ?</span><span class="sxs-lookup"><span data-stu-id="c8e6f-107">Looking for the Exchange Online version of this topic?</span></span> <span data-ttu-id="c8e6f-108">Consultez la rubrique [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="c8e6f-108">See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

## <a name="open-the-eac-in-eop"></a><span data-ttu-id="c8e6f-109">Ouvrir le CAE dans EOP</span><span class="sxs-lookup"><span data-stu-id="c8e6f-109">Open the EAC in EOP</span></span>

<span data-ttu-id="c8e6f-110">Les clients EOP autonomes peuvent accéder au CAE en utilisant les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8e6f-110">Standalone EOP customers can access the EAC by using the following methods:</span></span>

- <span data-ttu-id="c8e6f-111">**À partir du Centre d’administration Microsoft 365**:</span><span class="sxs-lookup"><span data-stu-id="c8e6f-111">**From the Microsoft 365 admin center**:</span></span>

  1. <span data-ttu-id="c8e6f-112">Go to <https://admin.microsoft.com> and click Show **all**.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-112">Go to <https://admin.microsoft.com> and click **Show all**.</span></span>

     ![Cliquez sur Afficher tout dans le Centre d’administration Microsoft 365](../../media/m365-center-show-all.png)

  2. <span data-ttu-id="c8e6f-114">Dans la section **Centres d’administration** qui s’affiche, cliquez **sur Tous les centres d’administration.**</span><span class="sxs-lookup"><span data-stu-id="c8e6f-114">In the **Admin centers** section that appears, click **All admin centers**.</span></span>

     ![Cliquez sur Tous les centres d’administration dans le Centre d’administration Microsoft 365](../../media/m365-center-select-all-admin-centers.png)

  3. <span data-ttu-id="c8e6f-116">Dans la page **Tous les centres d’administration** qui s’affiche, cliquez **sur Exchange Online Protection**.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-116">On the **All admin centers** page that appears, click **Exchange Online Protection**.</span></span>

- <span data-ttu-id="c8e6f-117">Go directly to `https://admin.protection.outlook.com/ecp/` .</span><span class="sxs-lookup"><span data-stu-id="c8e6f-117">Go directly to `https://admin.protection.outlook.com/ecp/`.</span></span>

## <a name="common-user-interface-elements-in-the-eac-in-eop"></a><span data-ttu-id="c8e6f-118">Éléments d’interface utilisateur courants dans le CAE dans EOP</span><span class="sxs-lookup"><span data-stu-id="c8e6f-118">Common user interface elements in the EAC in EOP</span></span>

<span data-ttu-id="c8e6f-119">Cette section décrit les éléments d'interface utilisateur disponibles dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-119">This section describes the user interface elements that are found in the EAC.</span></span>

![Centre d’administration Exchange dans Exchange Online Protection](../../media/EOP-AdminCenter.png)

### <a name="feature-pane"></a><span data-ttu-id="c8e6f-121">Volet des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c8e6f-121">Feature Pane</span></span>

<span data-ttu-id="c8e6f-p102">Il s'agit du premier niveau de navigation pour la plupart des tâches que vous effectuez au sein du CAE. Le volet des fonctionnalités est organisé par domaines de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p102">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>

- <span data-ttu-id="c8e6f-124">**Destinataires**: il s’agit de l’endroit où vous allez afficher les groupes et les contacts externes.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-124">**Recipients**: This is where you'll view groups and external contacts.</span></span>

- <span data-ttu-id="c8e6f-125">**Autorisations :** c’est ici que vous allez gérer les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-125">**Permissions**: This where you'll manage admin roles.</span></span>

- <span data-ttu-id="c8e6f-126">**Gestion de la** conformité : il s’agit de l’endroit où se trouvent le rapport du groupe de rôles d’administrateur et le rapport du journal d’audit de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-126">**Compliance Management**: This is where you'll find the administrator role group report and the admin audit log report.</span></span>

- <span data-ttu-id="c8e6f-127">**Protection**: il s’agit de l’endroit où vous pouvez gérer les stratégies anti-programme malveillant, la stratégie de filtrage des connexions par défaut et DKIM.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-127">**Protection**: This is where you can manage anti-malware policies, the default connection filter policy, and DKIM.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c8e6f-128">Vous devez gérer les stratégies anti-programme malveillant et la stratégie de filtrage des connexions par défaut dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-128">You should manage anti-malware policies and the default connection filter policy in the Security & Compliance Center.</span></span> <span data-ttu-id="c8e6f-129">Pour plus d’informations, voir [Configure anti-malware policies in EOP](configure-anti-malware-policies.md) and [Configure connection filtering in EOP](configure-the-connection-filter-policy.md).</span><span class="sxs-lookup"><span data-stu-id="c8e6f-129">For more information, see [Configure anti-malware policies in EOP](configure-anti-malware-policies.md) and [Configure connection filtering in EOP](configure-the-connection-filter-policy.md).</span></span>

- <span data-ttu-id="c8e6f-130">**Flux de** messagerie : il s’agit de l’endroit où vous allez gérer les règles de flux de messagerie (également appelées règles de transport), les domaines acceptés et les connecteurs, ainsi que l’endroit où vous pouvez exécuter le suivi des messages.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-130">**Mail Flow**: This is where you'll manage mail flow rules (also known as transport rules), accepted domains, and connectors, as well as where you can go to run message trace.</span></span>

- <span data-ttu-id="c8e6f-131">**Hybride**: il s’agit de l’endroit où vous pouvez exécuter l’Assistant [Configuration](https://docs.microsoft.com/Exchange/hybrid-configuration-wizard)hybride et où vous pouvez installer le [module Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/mfa-connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="c8e6f-131">**Hybrid**: This is where you can run the [Hybrid Configuration Wizard](https://docs.microsoft.com/Exchange/hybrid-configuration-wizard), and where you can install the [Exchange Online PowerShell module](https://docs.microsoft.com/powershell/exchange/mfa-connect-to-exchange-online-powershell).</span></span>

### <a name="tabs"></a><span data-ttu-id="c8e6f-132">Onglets</span><span class="sxs-lookup"><span data-stu-id="c8e6f-132">Tabs</span></span>

<span data-ttu-id="c8e6f-p104">Les onglets constituent votre deuxième niveau de navigation. Chaque domaine de fonctionnalités contient différents onglets, chacun représentant une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p104">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>

### <a name="toolbar"></a><span data-ttu-id="c8e6f-135">Barre d'outils</span><span class="sxs-lookup"><span data-stu-id="c8e6f-135">Toolbar</span></span>

<span data-ttu-id="c8e6f-p105">Lorsque vous cliquez sur la plupart des onglets, vous devez voir une barre d'outils. La barre d'outils contient des icônes qui correspondent à une action spécifique. Le tableau suivant décrit les icônes et leurs actions.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p105">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>

****

|<span data-ttu-id="c8e6f-139">Icône</span><span class="sxs-lookup"><span data-stu-id="c8e6f-139">Icon</span></span>|<span data-ttu-id="c8e6f-140">Nom</span><span class="sxs-lookup"><span data-stu-id="c8e6f-140">Name</span></span>|<span data-ttu-id="c8e6f-141">Action</span><span class="sxs-lookup"><span data-stu-id="c8e6f-141">Action</span></span>|
|---|---|---|
|![Icône Ajouter](../../media/ITPro-EAC-AddIcon.gif)|<span data-ttu-id="c8e6f-143">Ajouter, Nouveau</span><span class="sxs-lookup"><span data-stu-id="c8e6f-143">Add, New</span></span>|<span data-ttu-id="c8e6f-p106">Permet de créer un objet. Certaines de ces icônes comportent une flèche vers le bas associée, sur laquelle vous pouvez cliquer pour afficher des objets supplémentaires que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p106">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>|
|![Icône Modifier](../../media/ITPro-EAC-EditIcon.gif)|<span data-ttu-id="c8e6f-147">Modifier</span><span class="sxs-lookup"><span data-stu-id="c8e6f-147">Edit</span></span>|<span data-ttu-id="c8e6f-148">Permet de modifier un objet.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-148">Use this icon to edit an object.</span></span>|
|![Icône Supprimer](../../media/ITPro-EAC-DeleteIcon.gif)|<span data-ttu-id="c8e6f-150">Supprimer</span><span class="sxs-lookup"><span data-stu-id="c8e6f-150">Delete</span></span>|<span data-ttu-id="c8e6f-p107">Permet de supprimer un objet. Certaines des icônes de suppression comportent une flèche vers le bas, sur laquelle vous pouvez cliquer pour afficher des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p107">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>|
|![Icône Recherche](../../media/ITPro-EAC-.gif)|<span data-ttu-id="c8e6f-154">Rechercher</span><span class="sxs-lookup"><span data-stu-id="c8e6f-154">Search</span></span>|<span data-ttu-id="c8e6f-155">Permet d'ouvrir une zone de recherche dans laquelle vous pouvez entrer une expression pour rechercher un objet.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-155">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>|
|![Icône Actualiser](../../media/ITPro-EAC-RefreshIcon.gif)|<span data-ttu-id="c8e6f-157">Actualiser</span><span class="sxs-lookup"><span data-stu-id="c8e6f-157">Refresh</span></span>|<span data-ttu-id="c8e6f-158">Permet d'actualiser l'affichage Liste.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-158">Use this icon to refresh the list view.</span></span>|
|![Icône Options supplémentaires](../../media/ITPro-EAC-MoreOptionsIcon.gif)|<span data-ttu-id="c8e6f-160">Plus d'options</span><span class="sxs-lookup"><span data-stu-id="c8e6f-160">More options</span></span>|<span data-ttu-id="c8e6f-p108">Utilisez cette icône pour afficher d'autres actions que vous pouvez effectuer pour les objets figurant sous cet onglet. Par exemple, dans **Destinataires \> Utilisateurs**, le fait de cliquer sur cette icône affiche l'option de **Recherche avancée**.  </span><span class="sxs-lookup"><span data-stu-id="c8e6f-p108">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.</span></span>|
|![Icône flèche vers le haut](../../media/ITPro-EAC-UpArrowIcon.gif)![Icône de flèche vers le bas](../../media/ITPro-EAC-DownArrowIcon.gif)|<span data-ttu-id="c8e6f-165">Flèche Haut et flèche Bas</span><span class="sxs-lookup"><span data-stu-id="c8e6f-165">Up arrow and down arrow</span></span>|<span data-ttu-id="c8e6f-166">Utilisez ces icônes pour relever ou abaisser la priorité d'un objet.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-166">Use these icons to move an object's priority up or down.</span></span>|
|![Icône Suppression](../../media/ITPro-EAC-RemoveIcon.gif)|<span data-ttu-id="c8e6f-168">Supprimer</span><span class="sxs-lookup"><span data-stu-id="c8e6f-168">Remove</span></span>|<span data-ttu-id="c8e6f-169">Permet de supprimer des objets d'une liste.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-169">Use this icon to remove objects from a list.</span></span>|
|

### <a name="list-view"></a><span data-ttu-id="c8e6f-170">Affichage Liste</span><span class="sxs-lookup"><span data-stu-id="c8e6f-170">List View</span></span>

<span data-ttu-id="c8e6f-p109">Dans la plupart des cas, vous devez voir un affichage Liste lorsque vous sélectionnez un onglet. La limite d'affichage de l'affichage Liste du CAE est d'environ 10 000 objets. En outre, la pagination est incluse pour vous permettre de paginer les résultats.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p109">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>

### <a name="details-pane"></a><span data-ttu-id="c8e6f-174">Volet d'informations</span><span class="sxs-lookup"><span data-stu-id="c8e6f-174">Details Pane</span></span>

<span data-ttu-id="c8e6f-p110">Quand vous sélectionnez un objet de l'affichage Liste, les informations relatives à cet objet apparaissent dans le volet d'informations. Dans certains cas, le volet d'informations inclut les tâches de gestion.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-p110">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>

### <a name="me-tile-and-help"></a><span data-ttu-id="c8e6f-177">Vignette de l'utilisateur en cours et Aide</span><span class="sxs-lookup"><span data-stu-id="c8e6f-177">Me tile and Help</span></span>

<span data-ttu-id="c8e6f-178">La vignette **Moi** vous permet de fermer votre session du Centre d'administration Exchange (CAE) pour ouvrir ensuite une session en tant qu'utilisateur différent.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-178">The **Me** tile allows you to sign out the EAC and sign in as a different user.</span></span> <span data-ttu-id="c8e6f-179">Dans le menu **déroulant** Icône Aide, vous pouvez ![ faire les actions ](../../media/ITPro-EAC-HelpIcon.gif) suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8e6f-179">From the **Help**![Help Icon](../../media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can do the following actions:</span></span>

- <span data-ttu-id="c8e6f-180">**Aide :** cliquez sur ![ Icône Aide pour afficher le contenu de ](../../media/ITPro-EAC-HelpIcon.gif) l’aide en ligne.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-180">**Help**: Click ![Help Icon](../../media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span>
- <span data-ttu-id="c8e6f-181">**Commentaires :** laisser des commentaires.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-181">**Feedback**: Leave feedback.</span></span>
- <span data-ttu-id="c8e6f-182">**Communauté**: publiez une question pour trouver des réponses dans les forums de la communauté.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-182">**Community**: Post a question for find answers in the community forums.</span></span>
- <span data-ttu-id="c8e6f-183">**Désactiver la bulle d’aide**: la bulle d’aide affiche une aide contextuelle pour les champs lorsque vous créez ou modifiez un objet.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-183">**Disable Help bubble**: The Help bubble displays contextual help for fields when you create or edit an object.</span></span> <span data-ttu-id="c8e6f-184">Vous pouvez activer ou désactiver la bulle d'aide.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-184">You can turn off the Help bubble or turn it on if it has been disabled.</span></span>
- <span data-ttu-id="c8e6f-185">**Afficher la journalisation** des commandes : une nouvelle fenêtre s’ouvre et affiche les commandes PowerShell équivalentes en fonction de ce que vous avez configuré dans le CENTRE D’EAC.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-185">**Show Command Logging**: A new window opens that shows the equivalent PowerShell commands based on what you configured in EAC.</span></span>

## <a name="supported-browsers"></a><span data-ttu-id="c8e6f-186">Navigateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8e6f-186">Supported Browsers</span></span>

<span data-ttu-id="c8e6f-187">Pour bénéficier d’une meilleure expérience d’utilisation du CAE, nous vous recommandons de toujours utiliser les navigateurs, clients Office et applications les plus récents.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-187">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps.</span></span> <span data-ttu-id="c8e6f-188">Nous vous recommandons également d'installer les mises à jour logicielles lorsqu'elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-188">We also recommend that you install software updates when they become available.</span></span> <span data-ttu-id="c8e6f-189">Pour plus d’informations sur les navigateurs pris en charge et la système requise pour le service, voir [System requirements for Office](https://products.office.com/office-system-requirements).</span><span class="sxs-lookup"><span data-stu-id="c8e6f-189">For more information about the supported browsers and system requirements for the service, see [System requirements for Office](https://products.office.com/office-system-requirements).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="c8e6f-190">Langues prises en charge</span><span class="sxs-lookup"><span data-stu-id="c8e6f-190">Supported languages</span></span>

<span data-ttu-id="c8e6f-191">Les langues suivantes sont pris en charge et disponibles pour le CAE dans EOP autonome.</span><span class="sxs-lookup"><span data-stu-id="c8e6f-191">The following languages are supported and available for the EAC in standalone EOP.</span></span>

- <span data-ttu-id="c8e6f-192">Amharique</span><span class="sxs-lookup"><span data-stu-id="c8e6f-192">Amharic</span></span>
- <span data-ttu-id="c8e6f-193">Arabe</span><span class="sxs-lookup"><span data-stu-id="c8e6f-193">Arabic</span></span>
- <span data-ttu-id="c8e6f-194">basque (Basque)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-194">Basque (Basque)</span></span>
- <span data-ttu-id="c8e6f-195">Bengla (Inde)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-195">Bengali (India)</span></span>
- <span data-ttu-id="c8e6f-196">Bulgare</span><span class="sxs-lookup"><span data-stu-id="c8e6f-196">Bulgarian</span></span>
- <span data-ttu-id="c8e6f-197">Catalan</span><span class="sxs-lookup"><span data-stu-id="c8e6f-197">Catalan</span></span>
- <span data-ttu-id="c8e6f-198">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-198">Chinese (Simplified)</span></span>
- <span data-ttu-id="c8e6f-199">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-199">Chinese (Traditional)</span></span>
- <span data-ttu-id="c8e6f-200">Croate</span><span class="sxs-lookup"><span data-stu-id="c8e6f-200">Croatian</span></span>
- <span data-ttu-id="c8e6f-201">Tchèque</span><span class="sxs-lookup"><span data-stu-id="c8e6f-201">Czech</span></span>
- <span data-ttu-id="c8e6f-202">Danois</span><span class="sxs-lookup"><span data-stu-id="c8e6f-202">Danish</span></span>
- <span data-ttu-id="c8e6f-203">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="c8e6f-203">Dutch</span></span>
- <span data-ttu-id="c8e6f-204">Anglais</span><span class="sxs-lookup"><span data-stu-id="c8e6f-204">English</span></span>
- <span data-ttu-id="c8e6f-205">Estonien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-205">Estonian</span></span>
- <span data-ttu-id="c8e6f-206">Filipino (Philippines)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-206">Filipino (Philippines)</span></span>
- <span data-ttu-id="c8e6f-207">Finnois</span><span class="sxs-lookup"><span data-stu-id="c8e6f-207">Finnish</span></span>
- <span data-ttu-id="c8e6f-208">Français</span><span class="sxs-lookup"><span data-stu-id="c8e6f-208">French</span></span>
- <span data-ttu-id="c8e6f-209">Galicien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-209">Galician</span></span>
- <span data-ttu-id="c8e6f-210">Allemand</span><span class="sxs-lookup"><span data-stu-id="c8e6f-210">German</span></span>
- <span data-ttu-id="c8e6f-211">Grec</span><span class="sxs-lookup"><span data-stu-id="c8e6f-211">Greek</span></span>
- <span data-ttu-id="c8e6f-212">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="c8e6f-212">Gujarati</span></span>
- <span data-ttu-id="c8e6f-213">Hébreu</span><span class="sxs-lookup"><span data-stu-id="c8e6f-213">Hebrew</span></span>
- <span data-ttu-id="c8e6f-214">Hindi</span><span class="sxs-lookup"><span data-stu-id="c8e6f-214">Hindi</span></span>
- <span data-ttu-id="c8e6f-215">Hongrois</span><span class="sxs-lookup"><span data-stu-id="c8e6f-215">Hungarian</span></span>
- <span data-ttu-id="c8e6f-216">Islandais</span><span class="sxs-lookup"><span data-stu-id="c8e6f-216">Icelandic</span></span>
- <span data-ttu-id="c8e6f-217">Indonésien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-217">Indonesian</span></span>
- <span data-ttu-id="c8e6f-218">Italien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-218">Italian</span></span>
- <span data-ttu-id="c8e6f-219">Japonais</span><span class="sxs-lookup"><span data-stu-id="c8e6f-219">Japanese</span></span>
- <span data-ttu-id="c8e6f-220">Kannada</span><span class="sxs-lookup"><span data-stu-id="c8e6f-220">Kannada</span></span>
- <span data-ttu-id="c8e6f-221">Kazakh</span><span class="sxs-lookup"><span data-stu-id="c8e6f-221">Kazakh</span></span>
- <span data-ttu-id="c8e6f-222">Kiswahili</span><span class="sxs-lookup"><span data-stu-id="c8e6f-222">Kiswahili</span></span>
- <span data-ttu-id="c8e6f-223">Coréen</span><span class="sxs-lookup"><span data-stu-id="c8e6f-223">Korean</span></span>
- <span data-ttu-id="c8e6f-224">Letton</span><span class="sxs-lookup"><span data-stu-id="c8e6f-224">Latvian</span></span>
- <span data-ttu-id="c8e6f-225">Lituanien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-225">Lithuanian</span></span>
- <span data-ttu-id="c8e6f-226">Malais (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-226">Malay (Brunei Darussalam)</span></span>
- <span data-ttu-id="c8e6f-227">Malais (Malaisie)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-227">Malay (Malaysia)</span></span>
- <span data-ttu-id="c8e6f-228">Malayalam</span><span class="sxs-lookup"><span data-stu-id="c8e6f-228">Malayalam</span></span>
- <span data-ttu-id="c8e6f-229">Marathe</span><span class="sxs-lookup"><span data-stu-id="c8e6f-229">Marathi</span></span>
- <span data-ttu-id="c8e6f-230">Norvégien (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-230">Norwegian (Bokmål)</span></span>
- <span data-ttu-id="c8e6f-231">Norvégien (nynorsk)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-231">Norwegian (Nynorsk)</span></span>
- <span data-ttu-id="c8e6f-232">Odia</span><span class="sxs-lookup"><span data-stu-id="c8e6f-232">Oriya</span></span>
- <span data-ttu-id="c8e6f-233">Perse</span><span class="sxs-lookup"><span data-stu-id="c8e6f-233">Persian</span></span>
- <span data-ttu-id="c8e6f-234">Polonais</span><span class="sxs-lookup"><span data-stu-id="c8e6f-234">Polish</span></span>
- <span data-ttu-id="c8e6f-235">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-235">Portuguese (Brazil)</span></span>
- <span data-ttu-id="c8e6f-236">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-236">Portuguese (Portugal)</span></span>
- <span data-ttu-id="c8e6f-237">Roumain</span><span class="sxs-lookup"><span data-stu-id="c8e6f-237">Romanian</span></span>
- <span data-ttu-id="c8e6f-238">Russe</span><span class="sxs-lookup"><span data-stu-id="c8e6f-238">Russian</span></span>
- <span data-ttu-id="c8e6f-239">Serbe (cyrillique, Serbie)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-239">Serbian (Cyrillic, Serbia)</span></span>
- <span data-ttu-id="c8e6f-240">Serbe (latin)</span><span class="sxs-lookup"><span data-stu-id="c8e6f-240">Serbian (Latin)</span></span>
- <span data-ttu-id="c8e6f-241">Slovaque</span><span class="sxs-lookup"><span data-stu-id="c8e6f-241">Slovak</span></span>
- <span data-ttu-id="c8e6f-242">Slovène</span><span class="sxs-lookup"><span data-stu-id="c8e6f-242">Slovenian</span></span>
- <span data-ttu-id="c8e6f-243">Espagnol</span><span class="sxs-lookup"><span data-stu-id="c8e6f-243">Spanish</span></span>
- <span data-ttu-id="c8e6f-244">Suédois</span><span class="sxs-lookup"><span data-stu-id="c8e6f-244">Swedish</span></span>
- <span data-ttu-id="c8e6f-245">Tamoul</span><span class="sxs-lookup"><span data-stu-id="c8e6f-245">Tamil</span></span>
- <span data-ttu-id="c8e6f-246">Télougou</span><span class="sxs-lookup"><span data-stu-id="c8e6f-246">Telugu</span></span>
- <span data-ttu-id="c8e6f-247">Thaï</span><span class="sxs-lookup"><span data-stu-id="c8e6f-247">Thai</span></span>
- <span data-ttu-id="c8e6f-248">Turc</span><span class="sxs-lookup"><span data-stu-id="c8e6f-248">Turkish</span></span>
- <span data-ttu-id="c8e6f-249">Ukrainien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-249">Ukrainian</span></span>
- <span data-ttu-id="c8e6f-250">Ourdou</span><span class="sxs-lookup"><span data-stu-id="c8e6f-250">Urdu</span></span>
- <span data-ttu-id="c8e6f-251">Vietnamien</span><span class="sxs-lookup"><span data-stu-id="c8e6f-251">Vietnamese</span></span>
- <span data-ttu-id="c8e6f-252">Gallois</span><span class="sxs-lookup"><span data-stu-id="c8e6f-252">Welsh</span></span>
