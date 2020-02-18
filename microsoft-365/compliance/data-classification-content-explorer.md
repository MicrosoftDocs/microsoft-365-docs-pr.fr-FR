---
title: Utilisation de l’Explorateur de contenu de la classification des données (préversion)
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
search.appverid:
- MOE150
- MET150
description: L’Explorateur de contenu vous permet d’afficher des éléments étiquetés en mode natif.
ms.openlocfilehash: 2d9be42c00940bf9d37d1fdeb9b15b071aa412ac
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42076425"
---
# <a name="using-data-classification-content-explorer-preview"></a><span data-ttu-id="3f996-103">Utilisation de l’Explorateur de contenu de la classification des données (préversion)</span><span class="sxs-lookup"><span data-stu-id="3f996-103">Using data classification content explorer (preview)</span></span>

<span data-ttu-id="3f996-104">L’Explorateur de contenu de la classification des données vous permet d’afficher en mode natif les éléments qui ont été synthétisés dans la page vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="3f996-104">The data classification content explorer allows you to natively view the items that were summarized on the overview page.</span></span>

## <a name="content-explorer"></a><span data-ttu-id="3f996-105">Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="3f996-105">Content explorer</span></span>

<span data-ttu-id="3f996-106">L’Explorateur de contenu présente un instantané actuel des éléments qui ont une étiquette de confidentialité, une étiquette de rétention ou ont été classés comme un type d’informations sensibles au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3f996-106">Content explorer shows a current snapshot of the items that have a sensitivity label, a retention label or have been classified as a sensitive information type in your organization.</span></span>

### <a name="sensitive-information-types"></a><span data-ttu-id="3f996-107">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="3f996-107">Sensitive information types</span></span>

<span data-ttu-id="3f996-108">Une [stratégie DLP](data-loss-prevention-policies.md) peut contribuer à protéger les informations sensibles, définies selon des **types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="3f996-108">A [DLP policy](data-loss-prevention-policies.md) can help protect sensitive information, which is defined as a **sensitive information type**.</span></span> <span data-ttu-id="3f996-109">Microsoft 365 inclut des [définitions de pour de nombreux types d’informations sensibles courants](what-the-sensitive-information-types-look-for.md) dans de nombreuses régions différentes, prêtes à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="3f996-109">Microsoft 365 includes [definitions for many common sensitive information types](what-the-sensitive-information-types-look-for.md) across many different regions that are ready for you to use.</span></span> <span data-ttu-id="3f996-110">Par exemple, un numéro de carte bancaire, des numéros de compte bancaire, des numéros d’identification nationaux et des numéros de service Windows Live ID.</span><span class="sxs-lookup"><span data-stu-id="3f996-110">For example, a credit card number, bank account numbers, national ID numbers, and Windows Live ID service numbers.</span></span>

### <a name="sensitivity-labels"></a><span data-ttu-id="3f996-111">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="3f996-111">Sensitivity labels</span></span>

<span data-ttu-id="3f996-112">Une [étiquette de confidentialité](sensitivity-labels.md) est tout simplement une balise qui indique la valeur de l’élément pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3f996-112">A [sensitivity label](sensitivity-labels.md) is simply a tag that indicates the value of the item to your organization.</span></span> <span data-ttu-id="3f996-113">Elle peut être appliquée manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3f996-113">It can be applied manually, or automatically.</span></span> <span data-ttu-id="3f996-114">Une appliquée, elle est incorporée au document et elle le suit où qu’il aille.</span><span class="sxs-lookup"><span data-stu-id="3f996-114">Once applied it gets embedded in the document and will follow it everywhere it goes.</span></span> <span data-ttu-id="3f996-115">L’étiquette de confidentialité permet d’appliquer différents comportements de protection, tels que le filigrane ou le chiffrement obligatoires.</span><span class="sxs-lookup"><span data-stu-id="3f996-115">A sensitivity label enables various protective behaviors, such as mandatory watermarking or encryption.</span></span> <span data-ttu-id="3f996-116">Lorsque la protection de point de terminaison est activée, vous pouvez même empêcher un élément de quitter votre contrôle organisationnel.</span><span class="sxs-lookup"><span data-stu-id="3f996-116">With end point protection enabled you can even prevent an item from leaving your organizational control.</span></span>

<span data-ttu-id="3f996-117">Les étiquettes de confidentialité doivent être activées pour les fichiers stockés dans SharePoint et OneDrive pour que les données correspondantes apparaissent dans la page de classification des données.</span><span class="sxs-lookup"><span data-stu-id="3f996-117">Sensitivity labels must be enabled for files that are in SharePoint and OneDrive in order for the corresponding data to surface in the data classification page.</span></span> <span data-ttu-id="3f996-118">Pour en savoir plus, consulter [Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="3f996-118">For more information, see [Enable sensitivity labels for Office files in SharePoint and OneDrive (public preview)](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

### <a name="retention-labels"></a><span data-ttu-id="3f996-119">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="3f996-119">Retention labels</span></span>

<span data-ttu-id="3f996-120">Les [étiquettes de rétention](labels.md) vous permettent de définir la durée de conservation d’un élément étiqueté et les étapes à suivre avant de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="3f996-120">A [retention label](labels.md) allows you to define how long a labeled item is kept and the steps to be taken prior to deleting it.</span></span> <span data-ttu-id="3f996-121">Elles peuvent être appliquées manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3f996-121">They are applied manually or automatically via policies.</span></span> <span data-ttu-id="3f996-122">Elles peuvent jouer un rôle en aidant votre organisation à respecter les exigences légales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="3f996-122">They can play a role in helping your organization stay in compliance with legal and regulatory requirements.</span></span>

![capture d’écran réduite de l’Explorateur de contenu](../media/data-classification-content-explorer-1.png)

### <a name="permissions"></a><span data-ttu-id="3f996-124">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3f996-124">Permissions</span></span>

<span data-ttu-id="3f996-125">Deux rôles accordent l'accès à l'explorateur de contenu :</span><span class="sxs-lookup"><span data-stu-id="3f996-125">There are two roles that grant access to content explorer:</span></span>

- <span data-ttu-id="3f996-126">**Visionneuse de liste de l’Explorateur de contenu**: l’appartenance à ce groupe de rôle vous permet d’afficher chaque élément et son emplacement.</span><span class="sxs-lookup"><span data-stu-id="3f996-126">**Content Explorer List viewer**: Membership in this role group allows you to see each item and its location.</span></span> <span data-ttu-id="3f996-127">Le rôle `data classification list viewer` a été pré-attribué à ce groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="3f996-127">The `data classification list viewer` role has been pre-assigned to this role group.</span></span>

- <span data-ttu-id="3f996-128">**Visionneuse de contenu de l’Explorateur de contenu** : l’appartenance à ce groupe de rôles vous permet d’afficher le contenu de chaque élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="3f996-128">**Content Explorer Content viewer**: Membership in this role group allows you to view the contents of each item in the list.</span></span> <span data-ttu-id="3f996-129">Le rôle `data classification content viewer` a été pré-attribué à ce groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="3f996-129">The `data classification content viewer` role has been pre-assigned to this role group.</span></span>

<span data-ttu-id="3f996-130">Le compte que vous utilisez pour accéder à l’Explorateur de contenu doit se trouver dans l’un des groupes de rôles ou les deux.</span><span class="sxs-lookup"><span data-stu-id="3f996-130">The account you use to access content explorer must be in one or both of the role groups.</span></span> <span data-ttu-id="3f996-131">Il s’agit de groupes de rôles indépendants qui ne sont pas cumulatifs.</span><span class="sxs-lookup"><span data-stu-id="3f996-131">These are independent role groups and are not cumulative.</span></span> <span data-ttu-id="3f996-132">Par exemple, si vous voulez accorder à un compte la possibilité d’afficher les éléments et leur emplacement uniquement, attribuez des droits à la visionneuse de liste de l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="3f996-132">For example, if you want to grant an account the ability to view the items and their locations only, grant Content Explorer List viewer rights.</span></span> <span data-ttu-id="3f996-133">Si vous souhaitez que ce même compte puisse également afficher le contenu des éléments de la liste, vous pouvez également octroyer des droits de visionneuse de contenu dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="3f996-133">If you want that same account to also be able to view the contents of the items in the list, grant Content Explorer Content viewer rights as well.</span></span>

<span data-ttu-id="3f996-134">Vous pouvez également attribuer l’un ou l’autre des rôles (ou les deux) à un groupe de rôles personnalisé afin de personnaliser l’accès à l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="3f996-134">You can also assign either or both of the roles to a custom role group to tailor access to content explorer.</span></span>

### <a name="how-to-use-content-explorer"></a><span data-ttu-id="3f996-135">Utilisation de l’Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="3f996-135">How to use content explorer</span></span>

1. <span data-ttu-id="3f996-136">Ouvrez **Centre de conformité Microsoft 365**  > **Classification de données** > **Explorateur de contenu**.</span><span class="sxs-lookup"><span data-stu-id="3f996-136">Open **Microsoft 365 compliance center**  > **Data classification** > **Content explorer**.</span></span>
2. <span data-ttu-id="3f996-137">Si vous connaissez le nom de l'étiquette ou le type d'informations sensibles, vous pouvez la taper dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="3f996-137">If you know the name of the label, or the sensitive information type, you can type that into the search box.</span></span>
3. <span data-ttu-id="3f996-138">Vous pouvez également rechercher l'élément en développant le type d'étiquette et en sélectionnant l'étiquette dans la liste, un élément de la partie à l'étiquette de rétention de la liste est affiché ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3f996-138">Alternately, you can browse for the item by expanding the label type and selecting the label from the list, an item from the retention label portion of the list is show below.</span></span>
4. <span data-ttu-id="3f996-139">Sélectionnez un emplacement sous **Tous les emplacements** et explorez la structure de dossiers vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="3f996-139">Select a location under **All locations** and drill down the folder structure to the item.</span></span>
5. <span data-ttu-id="3f996-140">Double-cliquez pour ouvrir l’élément en mode natif dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="3f996-140">Double-click to open the item natively in content explorer.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f996-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f996-141">See also</span></span>

- [<span data-ttu-id="3f996-142">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="3f996-142">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="3f996-143">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="3f996-143">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="3f996-144">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="3f996-144">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="3f996-145">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="3f996-145">Overview of retention policies</span></span>](retention-policies.md)
- [<span data-ttu-id="3f996-146">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="3f996-146">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
