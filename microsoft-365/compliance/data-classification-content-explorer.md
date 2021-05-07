---
title: Prise en main de l’explorateur de contenu
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: L’Explorateur de contenu vous permet d’afficher des éléments étiquetés en mode natif.
ms.openlocfilehash: b39dd09012e7cde6c19ea88a0915154da84c712a
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114214"
---
# <a name="get-started-with-content-explorer"></a><span data-ttu-id="69cf3-103">Prise en main de l’explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="69cf3-103">Get started with content explorer</span></span>

<span data-ttu-id="69cf3-104">L’Explorateur de contenu de la classification des données vous permet d’afficher en mode natif les éléments qui ont été synthétisés dans la page vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="69cf3-104">The data classification content explorer allows you to natively view the items that were summarized on the overview page.</span></span>

![capture d’écran réduite de l’explorateur de contenu](../media/data-classification-content-explorer-1.png)

## <a name="prerequisites"></a><span data-ttu-id="69cf3-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="69cf3-106">Prerequisites</span></span>

<span data-ttu-id="69cf3-107">Chaque compte qui accède et utilise la classification de données doit posséder une licence pour l’un des abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="69cf3-107">Every account that accesses and uses data classification must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="69cf3-108">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="69cf3-108">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="69cf3-109">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="69cf3-109">Office 365 (E5)</span></span>
- <span data-ttu-id="69cf3-110">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="69cf3-110">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="69cf3-111">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="69cf3-111">Advanced Threat Intelligence (E5) add-on</span></span>
- <span data-ttu-id="69cf3-112">Microsoft 365 E5/A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="69cf3-112">Microsoft 365 E5/A5 Info Protection & Governance</span></span>
- <span data-ttu-id="69cf3-113">Conformité Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="69cf3-113">Microsoft 365 E5/A5 Compliance</span></span>


### <a name="permissions"></a><span data-ttu-id="69cf3-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="69cf3-114">Permissions</span></span>

<span data-ttu-id="69cf3-115">Pour accéder à l’onglet Explorateur de contenu, un compte doit être affecté à une appartenance dans l’un de ces rôles ou groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="69cf3-115">In order to get access to the content explorer tab, an account must be assigned membership in any one of these roles or role groups.</span></span> 

<span data-ttu-id="69cf3-116">**Groupes de rôles Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="69cf3-116">**Microsoft 365 role groups**</span></span>

- <span data-ttu-id="69cf3-117">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="69cf3-117">Global administrator</span></span>
- <span data-ttu-id="69cf3-118">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="69cf3-118">Compliance administrator</span></span>
- <span data-ttu-id="69cf3-119">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="69cf3-119">Security administrator</span></span>
- <span data-ttu-id="69cf3-120">Administrateur de conformité des données</span><span class="sxs-lookup"><span data-stu-id="69cf3-120">Compliance data administrator</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69cf3-121">L’appartenance à ces groupes de rôles ne vous permet pas d’afficher la liste des éléments ou le contenu des éléments dans l’explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-121">Membership in these role groups does not allow you to view the list of items in content explorer or to view the contents of the items in content explorer.</span></span>

### <a name="required-permissions-to-access-items-in-content-explorer"></a><span data-ttu-id="69cf3-122">Autorisations requises pour accéder aux éléments dans l’explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="69cf3-122">Required permissions to access items in content explorer</span></span>

<span data-ttu-id="69cf3-123">L’accès à l’explorateur de contenu est fortement restreint, car il vous permet de lire le contenu de fichiers numérisés.</span><span class="sxs-lookup"><span data-stu-id="69cf3-123">Access to content explorer is highly restricted because it lets you read the contents of scanned files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69cf3-124">Ces autorisations remplacent les autorisations attribuées localement aux éléments, ce qui permet d’afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-124">These permissions supercede permissions that are locally assigned to the items, which allows viewing of the content.</span></span> 

<span data-ttu-id="69cf3-125">Il existe deux rôles qui octroient l’accès à l’Explorateur de contenu et l’accès à celui-ci à l’aide du [Centre de sécurité et de conformité Microsoft](https://protection.office.com/permissions):</span><span class="sxs-lookup"><span data-stu-id="69cf3-125">There are two roles that grant access to content explorer and it is granted using the [Microsoft Security & Compliance Center](https://protection.office.com/permissions):</span></span>

- <span data-ttu-id="69cf3-126">**Visionneuse de liste de l’explorateur de contenu** : l’appartenance à ce groupe de rôle vous permet d’afficher chaque élément et son emplacement dans la liste.</span><span class="sxs-lookup"><span data-stu-id="69cf3-126">**Content Explorer List viewer**: Membership in this role group allows you to see each item and its location in list view.</span></span> <span data-ttu-id="69cf3-127">Le rôle `data classification list viewer` a été pré-attribué à ce groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="69cf3-127">The `data classification list viewer` role has been pre-assigned to this role group.</span></span>

- <span data-ttu-id="69cf3-128">**Visionneuse de contenu de l’Explorateur de contenu** : l’appartenance à ce groupe de rôles vous permet d’afficher le contenu de chaque élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="69cf3-128">**Content Explorer Content viewer**: Membership in this role group allows you to view the contents of each item in the list.</span></span> <span data-ttu-id="69cf3-129">Le rôle `data classification content viewer` a été pré-attribué à ce groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="69cf3-129">The `data classification content viewer` role has been pre-assigned to this role group.</span></span>

<span data-ttu-id="69cf3-130">Le compte que vous utilisez pour accéder à l’Explorateur de contenu doit se trouver dans l’un des groupes de rôles ou les deux.</span><span class="sxs-lookup"><span data-stu-id="69cf3-130">The account you use to access content explorer must be in one or both of the role groups.</span></span> <span data-ttu-id="69cf3-131">Il s’agit de groupes de rôles indépendants qui ne sont pas cumulatifs.</span><span class="sxs-lookup"><span data-stu-id="69cf3-131">These are independent role groups and are not cumulative.</span></span> <span data-ttu-id="69cf3-132">Par exemple, si vous voulez accorder à un compte la possibilité d’afficher les éléments et leur emplacement uniquement, attribuez des droits à la visionneuse de liste de l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-132">For example, if you want to grant an account the ability to view the items and their locations only, grant Content Explorer List viewer rights.</span></span> <span data-ttu-id="69cf3-133">Si vous souhaitez que ce même compte puisse également afficher le contenu des éléments de la liste, vous pouvez également octroyer des droits de visionneuse de contenu dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-133">If you want that same account to also be able to view the contents of the items in the list, grant Content Explorer Content viewer rights as well.</span></span>

<span data-ttu-id="69cf3-134">Vous pouvez également attribuer l’un ou l’autre des rôles (ou les deux) à un groupe de rôles personnalisé afin de personnaliser l’accès à l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-134">You can also assign either or both of the roles to a custom role group to tailor access to content explorer.</span></span>

<span data-ttu-id="69cf3-135">Un administrateur général, un administrateur de conformité ou un administrateur de données peut attribuer l'appartenance nécessaire au groupe de rôle de la visionneuse de liste de l’explorateur de contenu et de la visionneuse de contenu de l'explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-135">A Global admin, Compliance admin, or Data admin can assign the necessary Content Explorer List Viewer, and Content Explorer Content Viewer role group membership.</span></span>

## <a name="content-explorer"></a><span data-ttu-id="69cf3-136">Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="69cf3-136">Content explorer</span></span>

<span data-ttu-id="69cf3-137">L’Explorateur de contenu présente un instantané actuel des éléments qui ont une étiquette de confidentialité, une étiquette de rétention ou ont été classés comme un type d’informations sensibles au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="69cf3-137">Content explorer shows a current snapshot of the items that have a sensitivity label, a retention label or have been classified as a sensitive information type in your organization.</span></span>

### <a name="sensitive-information-types"></a><span data-ttu-id="69cf3-138">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="69cf3-138">Sensitive information types</span></span>

<span data-ttu-id="69cf3-139">Une [stratégie DLP](dlp-learn-about-dlp.md) peut contribuer à protéger les informations sensibles, définies selon des **types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="69cf3-139">A [DLP policy](dlp-learn-about-dlp.md) can help protect sensitive information, which is defined as a **sensitive information type**.</span></span> <span data-ttu-id="69cf3-140">Microsoft 365 inclut des [définitions pour de nombreux types d’informations sensibles courants](sensitive-information-type-entity-definitions.md) provenant de nombreuses régions différentes qui sont prêtes à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="69cf3-140">Microsoft 365 includes [definitions for many common sensitive information types](sensitive-information-type-entity-definitions.md) from across many different regions that are ready for you to use.</span></span> <span data-ttu-id="69cf3-141">Par exemple, un numéro de carte bancaire, des numéros de compte bancaire, des numéros d’identification nationaux et des numéros de service Windows Live ID.</span><span class="sxs-lookup"><span data-stu-id="69cf3-141">For example, a credit card number, bank account numbers, national ID numbers, and Windows Live ID service numbers.</span></span>

> [!NOTE]
> <span data-ttu-id="69cf3-142">Actuellement, l’explorateur de contenu n’analyse pas les types d’informations sensibles dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="69cf3-142">Content explorer doesn't currently scan for sensitive information types in Exchange Online.</span></span>

### <a name="sensitivity-labels"></a><span data-ttu-id="69cf3-143">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="69cf3-143">Sensitivity labels</span></span>

<span data-ttu-id="69cf3-144">Une [étiquette de confidentialité](sensitivity-labels.md) est tout simplement une balise qui indique la valeur de l’élément pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="69cf3-144">A [sensitivity label](sensitivity-labels.md) is simply a tag that indicates the value of the item to your organization.</span></span> <span data-ttu-id="69cf3-145">Elle peut être appliquée manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="69cf3-145">It can be applied manually, or automatically.</span></span> <span data-ttu-id="69cf3-146">Une appliquée, elle est incorporée au document et elle le suit où qu’il aille.</span><span class="sxs-lookup"><span data-stu-id="69cf3-146">Once applied it gets embedded in the document and will follow it everywhere it goes.</span></span> <span data-ttu-id="69cf3-147">L’étiquette de confidentialité permet d’appliquer différents comportements de protection, tels que le filigrane ou le chiffrement obligatoires.</span><span class="sxs-lookup"><span data-stu-id="69cf3-147">A sensitivity label enables various protective behaviors, such as mandatory watermarking or encryption.</span></span>

<span data-ttu-id="69cf3-148">Les étiquettes de confidentialité doivent être activées pour les fichiers stockés dans SharePoint et OneDrive pour que les données correspondantes apparaissent dans la page de classification des données.</span><span class="sxs-lookup"><span data-stu-id="69cf3-148">Sensitivity labels must be enabled for files that are in SharePoint and OneDrive in order for the corresponding data to surface in the data classification page.</span></span> <span data-ttu-id="69cf3-149">Pour plus d’informations, voir [Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="69cf3-149">For more information, see [Enable sensitivity labels for Office files in SharePoint and OneDrive](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

### <a name="retention-labels"></a><span data-ttu-id="69cf3-150">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="69cf3-150">Retention labels</span></span>

<span data-ttu-id="69cf3-151">Les [étiquettes de rétention](retention.md) vous permettent de définir la durée de conservation d’un élément étiqueté et les étapes à suivre avant de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="69cf3-151">A [retention label](retention.md) allows you to define how long a labeled item is kept and the steps to be taken prior to deleting it.</span></span> <span data-ttu-id="69cf3-152">Elles peuvent être appliquées manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="69cf3-152">They are applied manually or automatically via policies.</span></span> <span data-ttu-id="69cf3-153">Elles peuvent jouer un rôle en aidant votre organisation à respecter les exigences légales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="69cf3-153">They can play a role in helping your organization stay in compliance with legal and regulatory requirements.</span></span>

### <a name="how-to-use-content-explorer"></a><span data-ttu-id="69cf3-154">Utilisation de l’Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="69cf3-154">How to use content explorer</span></span>

1. <span data-ttu-id="69cf3-155">Ouvrez **Centre de conformité Microsoft 365**  > **Classification de données** > **Explorateur de contenu**.</span><span class="sxs-lookup"><span data-stu-id="69cf3-155">Open **Microsoft 365 compliance center**  > **Data classification** > **Content explorer**.</span></span>
2. <span data-ttu-id="69cf3-156">Si vous connaissez le nom de l’étiquette ou le type d’informations sensibles, vous pouvez le taper dans la zone de filtre.</span><span class="sxs-lookup"><span data-stu-id="69cf3-156">If you know the name of the label, or the sensitive information type, you can type that into the filter box.</span></span>
3. <span data-ttu-id="69cf3-157">Vous pouvez également rechercher l’élément en développant le type d’étiquette et en sélectionnant l’étiquette dans la liste.</span><span class="sxs-lookup"><span data-stu-id="69cf3-157">Alternately, you can browse for the item by expanding the label type and selecting the label from the list.</span></span>
4. <span data-ttu-id="69cf3-158">Sélectionnez un emplacement sous **Tous les emplacements** et explorez la structure de dossiers vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="69cf3-158">Select a location under **All locations** and drill down the folder structure to the item.</span></span>
5. <span data-ttu-id="69cf3-159">Double-cliquez pour ouvrir l’élément en mode natif dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="69cf3-159">Double-click to open the item natively in content explorer.</span></span>

### <a name="export"></a><span data-ttu-id="69cf3-160">Exporter</span><span class="sxs-lookup"><span data-stu-id="69cf3-160">Export</span></span>
<span data-ttu-id="69cf3-161">Le contrôle des **exportations** crée un fichier .csv qui contient une liste de tout ce qui s’affiche dans le volet **Tous les emplacements**.</span><span class="sxs-lookup"><span data-stu-id="69cf3-161">The **export** control will create a .csv file that contains a listing of whatever is showing in the **All locations** pane.</span></span>

![Contrôle des exportations de la classification des données](../media/data_classification_export_control.png)


### <a name="search"></a><span data-ttu-id="69cf3-163">Rechercher</span><span class="sxs-lookup"><span data-stu-id="69cf3-163">Search</span></span>

<span data-ttu-id="69cf3-164">Lorsque vous explorez un emplacement, par exemple, un dossier Exchange, ou un site SharePoint ou OneDrive, l’outil de **recherche** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="69cf3-164">When you drill down into a location, such as an Exchange folder, or a SharePoint or OneDrive site, the **search** tool appears.</span></span>

![Outil de recherche dans l’explorateur de contenu](../media/data_classification_search_tool.png)


<span data-ttu-id="69cf3-166">L’étendue de l’outil de recherche définie ce qui s’affiche dans le volet **Tous les emplacements** et ce que vous pouvez rechercher varie en fonction de l’emplacement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="69cf3-166">The scope of the search tool is what is displaying in the **All locations** pane and what you can search on varies depending on the selected location.</span></span> 

<span data-ttu-id="69cf3-167">Lorsque **Exchange** est l’emplacement sélectionné, vous pouvez effectuer une recherche sur l’adresse de messagerie complète de la boîte aux lettres, par exemple `user@domainname.com`.</span><span class="sxs-lookup"><span data-stu-id="69cf3-167">When **Exchange** is the selected location, you can search on the full email address of the mailbox, for example `user@domainname.com`.</span></span>

<span data-ttu-id="69cf3-168">Lorsque **SharePoint** ou **OneDrive** sont les emplacement sélectionnés, l’outil de recherche s’affiche lorsque vous explorez les noms, les dossiers et les fichiers du site.</span><span class="sxs-lookup"><span data-stu-id="69cf3-168">When either **SharePoint** or **OneDrive** are selected location, the search tool will appear when you drill down to site names, folders and files.</span></span> 

> [!NOTE]
> <span data-ttu-id="69cf3-169">**OneDrive** Nous avons écouté vos précieux commentaires sur l’intégration de OneDrive pendant notre programme d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="69cf3-169">**OneDrive** We have listened to your valuable feedback on OneDrive integration during our preview program.</span></span> <span data-ttu-id="69cf3-170">Sur la base de ces commentaires, la fonctionnalité OneDrive restera en préversion jusqu’à ce que tous les correctifs soient en place.</span><span class="sxs-lookup"><span data-stu-id="69cf3-170">Based on that feedback, the OneDrive functionality will remain in preview till all fixes are in place.</span></span> <span data-ttu-id="69cf3-171">En fonction de votre client, certains utilisateurs peuvent ne pas voir OneDrive comme un emplacement.</span><span class="sxs-lookup"><span data-stu-id="69cf3-171">Depending on your tenant, some customers may not see OneDrive as a location.</span></span> <span data-ttu-id="69cf3-172">Nous apprécions votre soutien sans faille sur ce projet.</span><span class="sxs-lookup"><span data-stu-id="69cf3-172">We appreciate your continued support on this.</span></span>

<span data-ttu-id="69cf3-173">Vous pouvez effectuer une recherche sur les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="69cf3-173">You can search on:</span></span>


|<span data-ttu-id="69cf3-174">valeur</span><span class="sxs-lookup"><span data-stu-id="69cf3-174">value</span></span>|<span data-ttu-id="69cf3-175">exemple</span><span class="sxs-lookup"><span data-stu-id="69cf3-175">example</span></span>  |
|---------|---------|
|<span data-ttu-id="69cf3-176">nom complet du site</span><span class="sxs-lookup"><span data-stu-id="69cf3-176">full site name</span></span>    |`https://contoso.onmicrosoft.com/sites/sitename`    |
|<span data-ttu-id="69cf3-177">nom du dossier racine : obtient tous les sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="69cf3-177">root folder name - gets all subfolders</span></span>    | `/sites`        |
|<span data-ttu-id="69cf3-178">nom du fichier</span><span class="sxs-lookup"><span data-stu-id="69cf3-178">file name</span></span>    |    `RES_Resume_1234.txt`     |
|<span data-ttu-id="69cf3-179">texte au début du nom de fichier</span><span class="sxs-lookup"><span data-stu-id="69cf3-179">text at the beginning of file name</span></span>| `RES`|
|<span data-ttu-id="69cf3-180">texte après un caractère de soulignement (_) dans le nom de fichier</span><span class="sxs-lookup"><span data-stu-id="69cf3-180">text after an underscore character ( _ ) in file name</span></span>|<span data-ttu-id="69cf3-181">`Resume` ou `1234`</span><span class="sxs-lookup"><span data-stu-id="69cf3-181">`Resume` or `1234`</span></span>| 
|<span data-ttu-id="69cf3-182">extension du fichier</span><span class="sxs-lookup"><span data-stu-id="69cf3-182">file extension</span></span>|`txt`|


## <a name="see-also"></a><span data-ttu-id="69cf3-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69cf3-183">See also</span></span>

- [<span data-ttu-id="69cf3-184">En savoir plus sur les étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="69cf3-184">Learn about sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="69cf3-185">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="69cf3-185">Learn about retention policies and retention labels</span></span>](retention.md)
- [<span data-ttu-id="69cf3-186">Définitions d’entités des types d’informations sensibles.md</span><span class="sxs-lookup"><span data-stu-id="69cf3-186">Sensitive information type entity definitions.md</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="69cf3-187">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="69cf3-187">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)