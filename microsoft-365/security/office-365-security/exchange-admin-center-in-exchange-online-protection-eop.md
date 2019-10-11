---
title: Centre d’administration Exchange dans Exchange Online Protection
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
description: Le Centre d'administration Exchange (CAE) est la console de gestion basée sur le web pour Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 3c83e87e6fa88e8fbcc0f16a0043707a9c9ec93a
ms.sourcegitcommit: cbf117a4cd92a907115c9f10752f3c557361e586
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "37441571"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="601b0-103">Centre d’administration Exchange dans Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="601b0-103">Exchange admin center in Exchange Online Protection</span></span>

<span data-ttu-id="601b0-104">Le Centre d'administration Exchange (CAE) est la console de gestion basée sur le web pour Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="601b0-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span>

<span data-ttu-id="601b0-105">Vous recherchez la version Exchange Server de cette rubrique ?</span><span class="sxs-lookup"><span data-stu-id="601b0-105">Looking for the Exchange Server version of this topic?</span></span> <span data-ttu-id="601b0-106">Consultez la rubrique [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="601b0-106">See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>

<span data-ttu-id="601b0-107">Vous recherchez la version Exchange Online de cette rubrique ?</span><span class="sxs-lookup"><span data-stu-id="601b0-107">Looking for the Exchange Online version of this topic?</span></span> <span data-ttu-id="601b0-108">Consultez la rubrique [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="601b0-108">See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>

## <a name="accessing-the-eac"></a><span data-ttu-id="601b0-109">Accès au CAE</span><span class="sxs-lookup"><span data-stu-id="601b0-109">Accessing the EAC</span></span>

<span data-ttu-id="601b0-110">Dans la plupart des cas, les clients EOP accèdent au centre d’administration Exchange par le biais du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="601b0-110">In most cases, EOP customers will access the EAC through the Microsoft 365 admin center.</span></span> <span data-ttu-id="601b0-111">Un lien vers EOP est disponible dans le menu déroulant de la vignette **Administrateur**, située près de la vignette **Moi**.</span><span class="sxs-lookup"><span data-stu-id="601b0-111">You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile.</span></span> <span data-ttu-id="601b0-112">Cliquez sur la vignette **Administrateur** et sélectionnez **Exchange Online Protection** dans le menu déroulant pour accéder au CAE.</span><span class="sxs-lookup"><span data-stu-id="601b0-112">Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span>

<span data-ttu-id="601b0-p104">Vous pouvez également accéder à la page de connexion du CAE directement via l'URL suivante : `https://admin.protection.outlook.com/ecp/<companydomain>`. Par exemple, `https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com`. Après avoir indiqué vos informations de connexion d'utilisateur, vous être envoyé directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="601b0-p104">You can also access the EAC sign in page directly via the following URL: `https://admin.protection.outlook.com/ecp/<companydomain>`. For example, `https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com`. After specifying your user credentials you will be taken directly into the EAC.</span></span>

## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="601b0-116">Éléments d'interface utilisateur courants dans le CAE</span><span class="sxs-lookup"><span data-stu-id="601b0-116">Common user interface elements in the EAC</span></span>

<span data-ttu-id="601b0-117">Cette section décrit les éléments d'interface utilisateur disponibles dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="601b0-117">This section describes the user interface elements that are found in the EAC.</span></span>

![EOP-AdminCenter](../media/EOP-AdminCenter.png)

### <a name="feature-pane"></a><span data-ttu-id="601b0-119">Volet des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="601b0-119">Feature Pane</span></span>

<span data-ttu-id="601b0-p105">Il s'agit du premier niveau de navigation pour la plupart des tâches que vous effectuez au sein du CAE. Le volet des fonctionnalités est organisé par domaines de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="601b0-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>

1. <span data-ttu-id="601b0-122">**Destinataires**: c’est ici que vous allez afficher les utilisateurs internes et les contacts externes.</span><span class="sxs-lookup"><span data-stu-id="601b0-122">**Recipients**: This is where you'll view internal users and external contacts.</span></span>

2. <span data-ttu-id="601b0-123">**Autorisations**: ce qui vous permet de gérer les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="601b0-123">**Permissions**: This where you'll manage administrator roles.</span></span>

3. <span data-ttu-id="601b0-124">**Gestion de la conformité**: c’est ici que se trouvent les journaux et les rapports d’audit, tels que le rapport de groupe de rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="601b0-124">**Compliance Management**: This is where you'll find audit logs and reports, such as the administrator role group report.</span></span>

4. <span data-ttu-id="601b0-125">**Protection**: c’est ici que vous gérerez la protection contre les programmes malveillants et le courrier indésirable pour votre organisation, ainsi que gérer les messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="601b0-125">**Protection**: This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span>

5. <span data-ttu-id="601b0-126">**Flux de messagerie**: c’est ici que vous gérerez les règles, les domaines acceptés et les connecteurs, ainsi que les emplacements dans lesquels vous allez effectuer le suivi des messages.</span><span class="sxs-lookup"><span data-stu-id="601b0-126">**Mail Flow**: This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span>

### <a name="tabs"></a><span data-ttu-id="601b0-127">Onglets</span><span class="sxs-lookup"><span data-stu-id="601b0-127">Tabs</span></span>

<span data-ttu-id="601b0-p106">Les onglets constituent votre deuxième niveau de navigation. Chaque domaine de fonctionnalités contient différents onglets, chacun représentant une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="601b0-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>

### <a name="toolbar"></a><span data-ttu-id="601b0-130">Barre d'outils</span><span class="sxs-lookup"><span data-stu-id="601b0-130">Toolbar</span></span>

<span data-ttu-id="601b0-p107">Lorsque vous cliquez sur la plupart des onglets, vous devez voir une barre d'outils. La barre d'outils contient des icônes qui correspondent à une action spécifique. Le tableau suivant décrit les icônes et leurs actions.</span><span class="sxs-lookup"><span data-stu-id="601b0-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>

|<span data-ttu-id="601b0-134">**Icône**</span><span class="sxs-lookup"><span data-stu-id="601b0-134">**Icon**</span></span>|<span data-ttu-id="601b0-135">**Nom**</span><span class="sxs-lookup"><span data-stu-id="601b0-135">**Name**</span></span>|<span data-ttu-id="601b0-136">**Action**</span><span class="sxs-lookup"><span data-stu-id="601b0-136">**Action**</span></span>|
|:-----|:-----|:-----|
|![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif)|<span data-ttu-id="601b0-138">Ajouter, Nouveau</span><span class="sxs-lookup"><span data-stu-id="601b0-138">Add, New</span></span>|<span data-ttu-id="601b0-p108">Permet de créer un objet. Certaines de ces icônes comportent une flèche vers le bas associée, sur laquelle vous pouvez cliquer pour afficher des objets supplémentaires que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="601b0-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>|
|![Icône Modifier](../media/ITPro-EAC-EditIcon.gif)|<span data-ttu-id="601b0-142">Modifier</span><span class="sxs-lookup"><span data-stu-id="601b0-142">Edit</span></span>|<span data-ttu-id="601b0-143">Permet de modifier un objet.</span><span class="sxs-lookup"><span data-stu-id="601b0-143">Use this icon to edit an object.</span></span>|
|![Icône Supprimer](../media/ITPro-EAC-DeleteIcon.gif)|<span data-ttu-id="601b0-145">Supprimer</span><span class="sxs-lookup"><span data-stu-id="601b0-145">Delete</span></span>|<span data-ttu-id="601b0-p109">Permet de supprimer un objet. Certaines des icônes de suppression comportent une flèche vers le bas, sur laquelle vous pouvez cliquer pour afficher des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="601b0-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>|
|![Icône Recherche](../media/ITPro-EAC-.gif)|<span data-ttu-id="601b0-149">Rechercher</span><span class="sxs-lookup"><span data-stu-id="601b0-149">Search</span></span>|<span data-ttu-id="601b0-150">Permet d'ouvrir une zone de recherche dans laquelle vous pouvez entrer une expression pour rechercher un objet.</span><span class="sxs-lookup"><span data-stu-id="601b0-150">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>|
|![Icône Actualiser](../media/ITPro-EAC-RefreshIcon.gif)|<span data-ttu-id="601b0-152">Actualiser</span><span class="sxs-lookup"><span data-stu-id="601b0-152">Refresh</span></span>|<span data-ttu-id="601b0-153">Permet d'actualiser l'affichage Liste.</span><span class="sxs-lookup"><span data-stu-id="601b0-153">Use this icon to refresh the list view.</span></span>|
|![Icône Options supplémentaires](../media/ITPro-EAC-MoreOptionsIcon.gif)|<span data-ttu-id="601b0-155">Plus d'options</span><span class="sxs-lookup"><span data-stu-id="601b0-155">More options</span></span>|<span data-ttu-id="601b0-p110">Utilisez cette icône pour afficher d'autres actions que vous pouvez effectuer pour les objets figurant sous cet onglet. Par exemple, dans **Destinataires \> Utilisateurs**, le fait de cliquer sur cette icône affiche l'option de **Recherche avancée**.  </span><span class="sxs-lookup"><span data-stu-id="601b0-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.</span></span>|
|![Icône flèche vers le haut](../media/ITPro-EAC-UpArrowIcon.gif)![Icône de flèche vers le bas](../media/ITPro-EAC-DownArrowIcon.gif)|<span data-ttu-id="601b0-160">Flèche Haut et flèche Bas</span><span class="sxs-lookup"><span data-stu-id="601b0-160">Up arrow and down arrow</span></span>|<span data-ttu-id="601b0-161">Utilisez ces icônes pour relever ou abaisser la priorité d'un objet.</span><span class="sxs-lookup"><span data-stu-id="601b0-161">Use these icons to move an object's priority up or down.</span></span>|
|![Icône Suppression](../media/ITPro-EAC-RemoveIcon.gif)|<span data-ttu-id="601b0-163">Supprimer</span><span class="sxs-lookup"><span data-stu-id="601b0-163">Remove</span></span>|<span data-ttu-id="601b0-164">Permet de supprimer des objets d'une liste.</span><span class="sxs-lookup"><span data-stu-id="601b0-164">Use this icon to remove objects from a list.</span></span>|

### <a name="list-view"></a><span data-ttu-id="601b0-165">Affichage Liste</span><span class="sxs-lookup"><span data-stu-id="601b0-165">List View</span></span>

<span data-ttu-id="601b0-p111">Dans la plupart des cas, vous devez voir un affichage Liste lorsque vous sélectionnez un onglet. La limite d'affichage de l'affichage Liste du CAE est d'environ 10 000 objets. En outre, la pagination est incluse pour vous permettre de paginer les résultats.</span><span class="sxs-lookup"><span data-stu-id="601b0-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>

### <a name="details-pane"></a><span data-ttu-id="601b0-169">Volet d'informations</span><span class="sxs-lookup"><span data-stu-id="601b0-169">Details Pane</span></span>

<span data-ttu-id="601b0-p112">Quand vous sélectionnez un objet de l'affichage Liste, les informations relatives à cet objet apparaissent dans le volet d'informations. Dans certains cas, le volet d'informations inclut les tâches de gestion.</span><span class="sxs-lookup"><span data-stu-id="601b0-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>

### <a name="me-tile-and-help"></a><span data-ttu-id="601b0-172">Vignette de l'utilisateur en cours et Aide</span><span class="sxs-lookup"><span data-stu-id="601b0-172">Me tile and Help</span></span>

<span data-ttu-id="601b0-p113">La vignette **Moi** vous permet de fermer votre session du Centre d'administration Exchange (CAE) pour ouvrir ensuite une session en tant qu'utilisateur différent. Dans le menu déroulant **Aide**![Icône d'aide](../media/ITPro-EAC-HelpIcon.gif), vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="601b0-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](../media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can perform the following actions:</span></span>

1. <span data-ttu-id="601b0-175">**Aide**: cliquez ![sur l'](../media/ITPro-EAC-HelpIcon.gif) icône aide pour afficher le contenu de l’aide en ligne.</span><span class="sxs-lookup"><span data-stu-id="601b0-175">**Help**: Click ![Help Icon](../media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span>

2. <span data-ttu-id="601b0-176">**Désactiver la bulle d'** aide : la bulle d’aide affiche une aide contextuelle pour les champs lorsque vous créez ou modifiez un objet.</span><span class="sxs-lookup"><span data-stu-id="601b0-176">**Disable Help bubble**: The Help bubble displays contextual help for fields when you create or edit an object.</span></span> <span data-ttu-id="601b0-177">Vous pouvez activer ou désactiver la bulle d'aide.</span><span class="sxs-lookup"><span data-stu-id="601b0-177">You can turn off the Help bubble or turn it on if it has been disabled.</span></span>

3. <span data-ttu-id="601b0-178">**Copyright**: cliquez sur ce lien pour lire l’avis de copyright pour Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="601b0-178">**Copyright**: Click this link to read the copyright notice for Exchange Online Protection.</span></span>

4. <span data-ttu-id="601b0-179">**Confidentialité**: cliquez pour lire la politique de confidentialité pour Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="601b0-179">**Privacy**: Click to read the privacy policy for Exchange Online Protection.</span></span>

## <a name="supported-browsers"></a><span data-ttu-id="601b0-180">Navigateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="601b0-180">Supported Browsers</span></span>

<span data-ttu-id="601b0-p115">Pour bénéficier d'une meilleure expérience d'utilisation du CAE, nous vous recommandons de toujours utiliser les navigateurs, clients Office et applications les plus récents. Nous vous recommandons également d'installer les mises à jour logicielles lorsqu'elles sont disponibles. Pour plus d'informations sur les navigateurs pris en charge et la configuration requise pour le service, voir [Configuration requise pour Office 365](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="601b0-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span>

## <a name="supported-languages-in-eop"></a><span data-ttu-id="601b0-184">Langues prises en charge dans EOP</span><span class="sxs-lookup"><span data-stu-id="601b0-184">Supported languages in EOP</span></span>

<span data-ttu-id="601b0-185">Les langues suivantes sont prises en charge et disponibles dans Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="601b0-185">The following languages are supported and available for Exchange Online Protection.</span></span>

- <span data-ttu-id="601b0-186">Amharique</span><span class="sxs-lookup"><span data-stu-id="601b0-186">Amharic</span></span>

- <span data-ttu-id="601b0-187">Arabe</span><span class="sxs-lookup"><span data-stu-id="601b0-187">Arabic</span></span>

- <span data-ttu-id="601b0-188">basque (Basque)</span><span class="sxs-lookup"><span data-stu-id="601b0-188">Basque (Basque)</span></span>

- <span data-ttu-id="601b0-189">Bengla (Inde)</span><span class="sxs-lookup"><span data-stu-id="601b0-189">Bengali (India)</span></span>

- <span data-ttu-id="601b0-190">Bulgare</span><span class="sxs-lookup"><span data-stu-id="601b0-190">Bulgarian</span></span>

- <span data-ttu-id="601b0-191">Catalan</span><span class="sxs-lookup"><span data-stu-id="601b0-191">Catalan</span></span>

- <span data-ttu-id="601b0-192">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="601b0-192">Chinese (Simplified)</span></span>

- <span data-ttu-id="601b0-193">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="601b0-193">Chinese (Traditional)</span></span>

- <span data-ttu-id="601b0-194">Croate</span><span class="sxs-lookup"><span data-stu-id="601b0-194">Croatian</span></span>

- <span data-ttu-id="601b0-195">Tchèque</span><span class="sxs-lookup"><span data-stu-id="601b0-195">Czech</span></span>

- <span data-ttu-id="601b0-196">Danois</span><span class="sxs-lookup"><span data-stu-id="601b0-196">Danish</span></span>

- <span data-ttu-id="601b0-197">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="601b0-197">Dutch</span></span>

- <span data-ttu-id="601b0-198">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="601b0-198">Dutch</span></span>

- <span data-ttu-id="601b0-199">Anglais</span><span class="sxs-lookup"><span data-stu-id="601b0-199">English</span></span>

- <span data-ttu-id="601b0-200">Estonien</span><span class="sxs-lookup"><span data-stu-id="601b0-200">Estonian</span></span>

- <span data-ttu-id="601b0-201">Filipino (Philippines)</span><span class="sxs-lookup"><span data-stu-id="601b0-201">Filipino (Philippines)</span></span>

- <span data-ttu-id="601b0-202">Finnois</span><span class="sxs-lookup"><span data-stu-id="601b0-202">Finnish</span></span>

- <span data-ttu-id="601b0-203">Français</span><span class="sxs-lookup"><span data-stu-id="601b0-203">French</span></span>

- <span data-ttu-id="601b0-204">Galicien</span><span class="sxs-lookup"><span data-stu-id="601b0-204">Galician</span></span>

- <span data-ttu-id="601b0-205">Allemand</span><span class="sxs-lookup"><span data-stu-id="601b0-205">German</span></span>

- <span data-ttu-id="601b0-206">Grec</span><span class="sxs-lookup"><span data-stu-id="601b0-206">Greek</span></span>

- <span data-ttu-id="601b0-207">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="601b0-207">Gujarati</span></span>

- <span data-ttu-id="601b0-208">Hébreu</span><span class="sxs-lookup"><span data-stu-id="601b0-208">Hebrew</span></span>

- <span data-ttu-id="601b0-209">Hindi</span><span class="sxs-lookup"><span data-stu-id="601b0-209">Hindi</span></span>

- <span data-ttu-id="601b0-210">Hongrois</span><span class="sxs-lookup"><span data-stu-id="601b0-210">Hungarian</span></span>

- <span data-ttu-id="601b0-211">Islandais</span><span class="sxs-lookup"><span data-stu-id="601b0-211">Icelandic</span></span>

- <span data-ttu-id="601b0-212">Indonésien</span><span class="sxs-lookup"><span data-stu-id="601b0-212">Indonesian</span></span>

- <span data-ttu-id="601b0-213">Italien</span><span class="sxs-lookup"><span data-stu-id="601b0-213">Italian</span></span>

- <span data-ttu-id="601b0-214">Japonais</span><span class="sxs-lookup"><span data-stu-id="601b0-214">Japanese</span></span>

- <span data-ttu-id="601b0-215">Kannada</span><span class="sxs-lookup"><span data-stu-id="601b0-215">Kannada</span></span>

- <span data-ttu-id="601b0-216">Kazakh</span><span class="sxs-lookup"><span data-stu-id="601b0-216">Kazakh</span></span>

- <span data-ttu-id="601b0-217">Kiswahili</span><span class="sxs-lookup"><span data-stu-id="601b0-217">Kiswahili</span></span>

- <span data-ttu-id="601b0-218">Coréen</span><span class="sxs-lookup"><span data-stu-id="601b0-218">Korean</span></span>

- <span data-ttu-id="601b0-219">Letton</span><span class="sxs-lookup"><span data-stu-id="601b0-219">Latvian</span></span>

- <span data-ttu-id="601b0-220">Lituanien</span><span class="sxs-lookup"><span data-stu-id="601b0-220">Lithuanian</span></span>

- <span data-ttu-id="601b0-221">Malais (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="601b0-221">Malay (Brunei Darussalam)</span></span>

- <span data-ttu-id="601b0-222">Malais (Malaisie)</span><span class="sxs-lookup"><span data-stu-id="601b0-222">Malay (Malaysia)</span></span>

- <span data-ttu-id="601b0-223">Malayalam</span><span class="sxs-lookup"><span data-stu-id="601b0-223">Malayalam</span></span>

- <span data-ttu-id="601b0-224">Marathe</span><span class="sxs-lookup"><span data-stu-id="601b0-224">Marathi</span></span>

- <span data-ttu-id="601b0-225">Norvégien (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="601b0-225">Norwegian (Bokmål)</span></span>

- <span data-ttu-id="601b0-226">Norvégien (nynorsk)</span><span class="sxs-lookup"><span data-stu-id="601b0-226">Norwegian (Nynorsk)</span></span>

- <span data-ttu-id="601b0-227">Odia</span><span class="sxs-lookup"><span data-stu-id="601b0-227">Oriya</span></span>

- <span data-ttu-id="601b0-228">Perse</span><span class="sxs-lookup"><span data-stu-id="601b0-228">Persian</span></span>

- <span data-ttu-id="601b0-229">Polonais</span><span class="sxs-lookup"><span data-stu-id="601b0-229">Polish</span></span>

- <span data-ttu-id="601b0-230">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="601b0-230">Portuguese (Brazil)</span></span>

- <span data-ttu-id="601b0-231">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="601b0-231">Portuguese (Portugal)</span></span>

- <span data-ttu-id="601b0-232">Roumain</span><span class="sxs-lookup"><span data-stu-id="601b0-232">Romanian</span></span>

- <span data-ttu-id="601b0-233">Russe</span><span class="sxs-lookup"><span data-stu-id="601b0-233">Russian</span></span>

- <span data-ttu-id="601b0-234">Serbe (cyrillique, Serbie)</span><span class="sxs-lookup"><span data-stu-id="601b0-234">Serbian (Cyrillic, Serbia)</span></span>

- <span data-ttu-id="601b0-235">Serbe (latin)</span><span class="sxs-lookup"><span data-stu-id="601b0-235">Serbian (Latin)</span></span>

- <span data-ttu-id="601b0-236">Slovaque</span><span class="sxs-lookup"><span data-stu-id="601b0-236">Slovak</span></span>

- <span data-ttu-id="601b0-237">Slovène</span><span class="sxs-lookup"><span data-stu-id="601b0-237">Slovenian</span></span>

- <span data-ttu-id="601b0-238">Espagnol</span><span class="sxs-lookup"><span data-stu-id="601b0-238">Spanish</span></span>

- <span data-ttu-id="601b0-239">Suédois</span><span class="sxs-lookup"><span data-stu-id="601b0-239">Swedish</span></span>

- <span data-ttu-id="601b0-240">Tamoul</span><span class="sxs-lookup"><span data-stu-id="601b0-240">Tamil</span></span>

- <span data-ttu-id="601b0-241">Télougou</span><span class="sxs-lookup"><span data-stu-id="601b0-241">Telugu</span></span>

- <span data-ttu-id="601b0-242">Thaï</span><span class="sxs-lookup"><span data-stu-id="601b0-242">Thai</span></span>

- <span data-ttu-id="601b0-243">Turc</span><span class="sxs-lookup"><span data-stu-id="601b0-243">Turkish</span></span>

- <span data-ttu-id="601b0-244">Ukrainien</span><span class="sxs-lookup"><span data-stu-id="601b0-244">Ukrainian</span></span>

- <span data-ttu-id="601b0-245">Ourdou</span><span class="sxs-lookup"><span data-stu-id="601b0-245">Urdu</span></span>

- <span data-ttu-id="601b0-246">Vietnamien</span><span class="sxs-lookup"><span data-stu-id="601b0-246">Vietnamese</span></span>

- <span data-ttu-id="601b0-247">Gallois</span><span class="sxs-lookup"><span data-stu-id="601b0-247">Welsh</span></span>


