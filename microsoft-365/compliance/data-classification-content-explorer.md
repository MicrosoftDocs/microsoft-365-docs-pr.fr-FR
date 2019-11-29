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
ms.openlocfilehash: 6f062901acbf149f6fc56c266d10b370ed0c1112
ms.sourcegitcommit: 8ca97fa879ae4ea44468be629d6c32b429efeeec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/16/2019
ms.locfileid: "39268496"
---
# <a name="using-data-classification-content-explorer-preview"></a><span data-ttu-id="7c31a-103">Utilisation de l’Explorateur de contenu de la classification des données (préversion)</span><span class="sxs-lookup"><span data-stu-id="7c31a-103">Using data classification content explorer (preview)</span></span>

<span data-ttu-id="7c31a-104">L’Explorateur de contenu de la classification des données vous permet d’afficher en mode natif les éléments qui ont été synthétisés dans la page vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="7c31a-104">The data classification content explorer allows you to natively view the items that were summarized on the overview page.</span></span>

## <a name="content-explorer"></a><span data-ttu-id="7c31a-105">Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="7c31a-105">Content explorer</span></span>

<span data-ttu-id="7c31a-106">L’Explorateur de contenu est un instantané actuel des éléments qui ont une étiquette de confidentialité, une étiquette de rétention ou ont été classés comme un type d’informations sensibles au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7c31a-106">Content explorer is a current snapshot of the items that have a sensitivity label, a retention label or have been classified as a sensitive information type in your organization.</span></span>

![capture d’écran réduite de l’Explorateur de contenu](media/data-classification-content-explorer-1.png)

### <a name="permissions"></a><span data-ttu-id="7c31a-108">Autorisations</span><span class="sxs-lookup"><span data-stu-id="7c31a-108">Permissions</span></span>

<span data-ttu-id="7c31a-109">Il existe deux rôles qui octroient l’accès à l’Explorateur de contenu :</span><span class="sxs-lookup"><span data-stu-id="7c31a-109">There are two roles that grant access to Content explorer:</span></span>

- <span data-ttu-id="7c31a-110">**Visionneuse de liste de l’Explorateur de contenu**: l’appartenance à ce rôle vous permet d’afficher chaque élément et son emplacement.</span><span class="sxs-lookup"><span data-stu-id="7c31a-110">**Content Explorer List viewer**: Membership in this role allows you to see each item and its location.</span></span>

- <span data-ttu-id="7c31a-111">**Visionneuse de contenu de l’Explorateur de contenu**: l’appartenance à ce rôle vous permet d’afficher le contenu de chaque élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7c31a-111">**Content Explorer Content viewer**: Membership in this role allows you to view the contents of each item in the list.</span></span>

<span data-ttu-id="7c31a-112">Le compte que vous utilisez pour accéder à l’Explorateur de contenu doit se trouver dans l’un des rôles ou les deux.</span><span class="sxs-lookup"><span data-stu-id="7c31a-112">The account you use to access Content explorer must be in one or both of the roles.</span></span> <span data-ttu-id="7c31a-113">Il s’agit de rôles indépendants qui ne sont pas cumulatifs.</span><span class="sxs-lookup"><span data-stu-id="7c31a-113">These are independent roles and are not cumulative.</span></span> <span data-ttu-id="7c31a-114">Par exemple, si vous voulez accorder à un compte la possibilité d’afficher les éléments et leur emplacement uniquement, attribuez des droits à la visionneuse de liste de l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7c31a-114">For example, if you want to grant an account the ability to view the items and their locations only, grant Content Explorer List viewer rights.</span></span> <span data-ttu-id="7c31a-115">Si vous souhaitez que ce même compte puisse également afficher le contenu des éléments de la liste, vous pouvez également octroyer des droits de visionneuse de contenu dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7c31a-115">If you want that same account to also be able to view the contents of the items in the list, grant Content Explorer Content viewer rights as well.</span></span>

### <a name="how-to-use-content-explorer"></a><span data-ttu-id="7c31a-116">Utilisation de l’Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="7c31a-116">How to use content explorer</span></span>

1. <span data-ttu-id="7c31a-117">Ouvrez **Centre de conformité Microsoft 365**  > **Classification de données** > **Explorateur de contenu**.</span><span class="sxs-lookup"><span data-stu-id="7c31a-117">Open **Microsoft 365 compliance center**  > **Data classification** > **Content explorer**.</span></span>
2. <span data-ttu-id="7c31a-118">Si vous connaissez le nom de l'étiquette ou le type d'informations sensibles, vous pouvez la taper dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c31a-118">If you know the name of the label, or the sensitive information type, you can type that into the search box.</span></span>
3. <span data-ttu-id="7c31a-119">Vous pouvez également rechercher l'élément en développant le type d'étiquette et en sélectionnant l'étiquette dans la liste, un élément de la partie à l'étiquette de rétention de la liste est affiché ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7c31a-119">Alternately, you can browse for the item by expanding the label type and selecting the label from the list, an item from the retention label portion of the list is show below.</span></span>
4. <span data-ttu-id="7c31a-120">Sélectionnez un emplacement sous **Tous les emplacements** et explorez la structure de dossiers vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="7c31a-120">Select a location under **All locations** and drill down the folder structure to the item.</span></span>
5. <span data-ttu-id="7c31a-121">Double-cliquez pour ouvrir l’élément en mode natif dans l’Explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7c31a-121">Double click to open the item natively in content explorer.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c31a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c31a-122">See also</span></span>

- [<span data-ttu-id="7c31a-123">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="7c31a-123">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="7c31a-124">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="7c31a-124">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="7c31a-125">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7c31a-125">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="7c31a-126">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="7c31a-126">Overview of retention policies</span></span>](retention-policies.md)
