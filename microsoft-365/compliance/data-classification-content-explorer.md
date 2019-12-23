---
title: Utilisation de l’Explorateur de contenu de la classification des données (préversion)
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
ms.openlocfilehash: 8a795e0582599dc3160f896a6361b773caa6c4e4
ms.sourcegitcommit: 6ae69c40bafa6aef633789c3df0fa20590bdcf40
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2019
ms.locfileid: "40823796"
---
# <a name="using-data-classification-content-explorer-preview"></a><span data-ttu-id="7d27d-103">Utilisation de l’Explorateur de contenu de la classification des données (préversion)</span><span class="sxs-lookup"><span data-stu-id="7d27d-103">Using data classification content explorer (preview)</span></span>

<span data-ttu-id="7d27d-104">L’Explorateur de contenu de la classification des données vous permet d’afficher en mode natif les éléments qui ont été synthétisés dans la page vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="7d27d-104">The data classification content explorer allows you to natively view the items that were summarized on the overview page.</span></span>

## <a name="content-explorer"></a><span data-ttu-id="7d27d-105">Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="7d27d-105">Content explorer</span></span>

<span data-ttu-id="7d27d-106">L’Explorateur de contenu présente un instantané actuel des éléments qui ont une étiquette de confidentialité, une étiquette de rétention ou ont été classés comme un type d’informations sensibles au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7d27d-106">Content explorer shows a current snapshot of the items that have a sensitivity label, a retention label or have been classified as a sensitive information type in your organization.</span></span>

### <a name="sensitive-information-types"></a><span data-ttu-id="7d27d-107">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7d27d-107">Sensitive information types</span></span>

<span data-ttu-id="7d27d-108">Une [stratégie DLP](data-loss-prevention-policies.md) peut contribuer à protéger les informations sensibles, définies selon des **types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="7d27d-108">A [DLP policy](data-loss-prevention-policies.md) can help protect sensitive information, which is defined as a **sensitive information type**.</span></span> <span data-ttu-id="7d27d-109">Microsoft 365 inclut des [définitions de pour de nombreux types d’informations sensibles courants](what-the-sensitive-information-types-look-for.md) dans de nombreuses régions différentes, prêtes à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="7d27d-109">Microsoft 365 includes [definitions for many common sensitive information types](what-the-sensitive-information-types-look-for.md) across many different regions that are ready for you to use.</span></span> <span data-ttu-id="7d27d-110">Par exemple, un numéro de carte bancaire, des numéros de compte bancaire, des numéros d’identification nationaux et des numéros de service Windows Live ID.</span><span class="sxs-lookup"><span data-stu-id="7d27d-110">For example, a credit card number, bank account numbers, national ID numbers, and Windows Live ID service numbers.</span></span>

### <a name="sensitivity-labels"></a><span data-ttu-id="7d27d-111">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="7d27d-111">Sensitivity labels</span></span>

<span data-ttu-id="7d27d-112">Une [étiquette de confidentialité](sensitivity-labels.md) est tout simplement une balise qui indique la valeur de l’élément pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7d27d-112">A [sensitivity label](sensitivity-labels.md) is simply a tag that indicates the value of the item to your organization.</span></span> <span data-ttu-id="7d27d-113">Elle peut être appliquée manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7d27d-113">It can be applied manually, or automatically.</span></span> <span data-ttu-id="7d27d-114">Une appliquée, elle est incorporée au document et elle le suit où qu’il aille.</span><span class="sxs-lookup"><span data-stu-id="7d27d-114">Once applied it gets embedded in the document and will follow it everywhere it goes.</span></span> <span data-ttu-id="7d27d-115">L’étiquette de confidentialité permet d’appliquer différents comportements de protection, tels que le filigrane ou le chiffrement obligatoires.</span><span class="sxs-lookup"><span data-stu-id="7d27d-115">A sensitivity label enables various protective behaviors, such as mandatory watermarking or encryption.</span></span> <span data-ttu-id="7d27d-116">Lorsque la protection de point de terminaison est activée, vous pouvez même empêcher un élément de quitter votre contrôle organisationnel.</span><span class="sxs-lookup"><span data-stu-id="7d27d-116">With end point protection enabled you can even prevent an item from leaving your organizational control.</span></span>

<span data-ttu-id="7d27d-117">Les étiquettes de confidentialité doivent être activées pour les fichiers stockés dans SharePoint et OneDrive pour que les données correspondantes apparaissent dans la page de classification des données.</span><span class="sxs-lookup"><span data-stu-id="7d27d-117">Sensitivity labels must be enabled for files that are in SharePoint and OneDrive in order for the corresponding data to surface in the data classification page.</span></span> <span data-ttu-id="7d27d-118">Pour en savoir plus, consulter [Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="7d27d-118">[Enable sensitivity labels for Office files in SharePoint and OneDrive (public preview)](sensitivity-labels-sharepoint-onedrive-files.md)</span></span>

### <a name="retention-labels"></a><span data-ttu-id="7d27d-119">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="7d27d-119">Retention labels</span></span>

<span data-ttu-id="7d27d-120">Les [étiquettes de rétention](labels.md) vous permettent de définir la durée de conservation d’un élément étiqueté et les étapes à suivre avant de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="7d27d-120">A [retention label](labels.md) allows you to define how long a labeled item is kept and the steps to be taken prior to deleting it.</span></span> <span data-ttu-id="7d27d-121">Elles peuvent être appliquées manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7d27d-121">They are applied manually or automatically via policies.</span></span> <span data-ttu-id="7d27d-122">Elles peuvent jouer un rôle en aidant votre organisation à respecter les exigences légales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="7d27d-122">They can play a role in helping your organization stay in compliance with legal and regulatory requirements.</span></span>

![capture d’écran réduite de l’Explorateur de contenu](media/data-classification-content-explorer-1.png)

### <a name="permissions"></a><span data-ttu-id="7d27d-124">Autorisations</span><span class="sxs-lookup"><span data-stu-id="7d27d-124">Permissions</span></span>

<span data-ttu-id="7d27d-125">Il existe deux rôles qui octroient l’accès à l’Explorateur de contenu :</span><span class="sxs-lookup"><span data-stu-id="7d27d-125">There are two roles that grant access to Content explorer:</span></span>

- <span data-ttu-id="7d27d-126">**Visionneuse de liste de l’Explorateur de contenu**: l’appartenance à ce rôle vous permet d’afficher chaque élément et son emplacement.</span><span class="sxs-lookup"><span data-stu-id="7d27d-126">**Content Explorer List viewer**: Membership in this role allows you to see each item and its location.</span></span>

- <span data-ttu-id="7d27d-127">**Visionneuse de contenu de l’Explorateur de contenu**: l’appartenance à ce rôle vous permet d’afficher le contenu de chaque élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7d27d-127">**Content Explorer Content viewer**: Membership in this role allows you to view the contents of each item in the list.</span></span>

<span data-ttu-id="7d27d-128">Le compte que vous utilisez pour accéder à l’Explorateur de contenu doit se trouver dans l’un des rôles ou les deux.</span><span class="sxs-lookup"><span data-stu-id="7d27d-128">The account you use to access Content explorer must be in one or both of the roles.</span></span> <span data-ttu-id="7d27d-129">Il s’agit de rôles indépendants qui ne sont pas cumulatifs.</span><span class="sxs-lookup"><span data-stu-id="7d27d-129">These are independent roles and are not cumulative.</span></span> <span data-ttu-id="7d27d-130">Par exemple, si vous voulez accorder à un compte la possibilité d’afficher les éléments et leur emplacement uniquement, attribuez des droits à la visionneuse de liste de l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7d27d-130">For example, if you want to grant an account the ability to view the items and their locations only, grant Content Explorer List viewer rights.</span></span> <span data-ttu-id="7d27d-131">Si vous souhaitez que ce même compte puisse également afficher le contenu des éléments de la liste, vous pouvez également octroyer des droits de visionneuse de contenu dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7d27d-131">If you want that same account to also be able to view the contents of the items in the list, grant Content Explorer Content viewer rights as well.</span></span>

### <a name="how-to-use-content-explorer"></a><span data-ttu-id="7d27d-132">Utilisation de l’Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="7d27d-132">How to use content explorer</span></span>

1. <span data-ttu-id="7d27d-133">Ouvrez **Centre de conformité Microsoft 365**  > **Classification de données** > **Explorateur de contenu**.</span><span class="sxs-lookup"><span data-stu-id="7d27d-133">Open **Microsoft 365 compliance center**  > **Data classification** > **Content explorer**.</span></span>
2. <span data-ttu-id="7d27d-134">Si vous connaissez le nom de l'étiquette ou le type d'informations sensibles, vous pouvez la taper dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="7d27d-134">If you know the name of the label, or the sensitive information type, you can type that into the search box.</span></span>
3. <span data-ttu-id="7d27d-135">Vous pouvez également rechercher l'élément en développant le type d'étiquette et en sélectionnant l'étiquette dans la liste, un élément de la partie à l'étiquette de rétention de la liste est affiché ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7d27d-135">Alternately, you can browse for the item by expanding the label type and selecting the label from the list, an item from the retention label portion of the list is show below.</span></span>
4. <span data-ttu-id="7d27d-136">Sélectionnez un emplacement sous **Tous les emplacements** et explorez la structure de dossiers vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="7d27d-136">Select a location under **All locations** and drill down the folder structure to the item.</span></span>
5. <span data-ttu-id="7d27d-137">Double-cliquez pour ouvrir l’élément en mode natif dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7d27d-137">Double-click to open the item natively in content explorer.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d27d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d27d-138">See also</span></span>

- [<span data-ttu-id="7d27d-139">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="7d27d-139">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="7d27d-140">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="7d27d-140">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="7d27d-141">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7d27d-141">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="7d27d-142">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="7d27d-142">Overview of retention policies</span></span>](retention-policies.md)
- [<span data-ttu-id="7d27d-143">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="7d27d-143">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
