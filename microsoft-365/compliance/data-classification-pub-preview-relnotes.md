---
title: Notes de publication pour la classification des données
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
description: Notes de publication pour la classification des données.
ms.openlocfilehash: 2b9302cfa49f9445d3cbeb5109aef70e0c8d8f7f
ms.sourcegitcommit: 47de4402174c263ae8d70c910ca068a7581d04ae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "49663039"
---
# <a name="data-classification-release-notes"></a><span data-ttu-id="622b0-103">Notes de publication pour la classification des données</span><span class="sxs-lookup"><span data-stu-id="622b0-103">Data classification release notes</span></span>


## <a name="exchange-mailbox-count"></a><span data-ttu-id="622b0-104">Nombre de boîtes aux lettres Exchange</span><span class="sxs-lookup"><span data-stu-id="622b0-104">Exchange mailbox count</span></span>

<span data-ttu-id="622b0-105">Vous remarquerez qu’une petite info-bulle apparaît lorsque vous explorez des boîtes aux lettres Exchange.</span><span class="sxs-lookup"><span data-stu-id="622b0-105">You will notice a small tool tip appear when you drill into Exchange mailboxes.</span></span> <span data-ttu-id="622b0-106">Il s'agit là d'évoquer le fait que le nombre agrégé affiché pour le type d’information sensible, l’étiquette de confidentialité et l’étiquette de rétention ne correspondent pas parfaitement au nombre d’éléments que vous trouverez dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="622b0-106">This is to call out the fact that the aggregate count displayed for sensitive information type, sensitivity label and retention label may not exactly match the number of items that you will find inside the mailbox.</span></span> <span data-ttu-id="622b0-107">Cela est dû au fait que descendre dans la hiérarchie du dossier permet de récupérer l’affichage en direct du contenu, lequel est classé, alors que le nombre agrégé est calculé.</span><span class="sxs-lookup"><span data-stu-id="622b0-107">This is because the drill-down into the folder fetches the live view of content, which is classified, while the aggregated count is calculated.</span></span>


## <a name="rendering-of-encrypted-documents"></a><span data-ttu-id="622b0-108">Rendu de documents chiffrés</span><span class="sxs-lookup"><span data-stu-id="622b0-108">Rendering of encrypted documents</span></span>

<span data-ttu-id="622b0-109">L'affichage des fichiers SharePoint, Exchange et OneDrive chiffrés n'a pas lieu dans l’explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="622b0-109">SharePoint, Exchange, and OneDrive files that are encrypted don't render in the content explorer.</span></span> <span data-ttu-id="622b0-110">Il s’agit d’un problème sensible qui nécessite un équilibre entre le besoin d'afficher le contenu de fichiers dans l’explorateur de contenu et la nécessité de conserver les contenus chiffrés.</span><span class="sxs-lookup"><span data-stu-id="622b0-110">This is a sensitive issue that requires a balance between the need to see file contents in content explorer and the need to keep the contents encrypted.</span></span> <span data-ttu-id="622b0-111">Avec les autorisations accordées par les groupes de rôle de la **visionneuse de liste de l’explorateur de contenu** et la **visionneuse de contenu de l’explorateur de contenu**, un affichage de la liste des fichiers, des métadonnées de fichier et un lien que vous pouvez utiliser pour accéder au contenu via le client web.</span><span class="sxs-lookup"><span data-stu-id="622b0-111">With the permissions granted by **Content Explorer List Viewer**, and **Content Explorer Content Viewer** role groups, you will see a list view of the files, the file  metadata, and a link you can use to access the content via the web client.</span></span>

## <a name="supported-characters-in-retention-label-names-in-sharepoint-search"></a><span data-ttu-id="622b0-112">Caractères pris en charge dans les noms d'étiquettes de rétention de la recherche SharePoint</span><span class="sxs-lookup"><span data-stu-id="622b0-112">Supported characters in retention label names in SharePoint search</span></span>

<span data-ttu-id="622b0-113">La recherche SharePoint ne prend pas en charge les noms d’étiquettes de rétention qui contiennent `-` ou `_`.</span><span class="sxs-lookup"><span data-stu-id="622b0-113">SharePoint search doesn't support retention label names with `-`, or `_` in them.</span></span> <span data-ttu-id="622b0-114">Par exemple, `Label-MIP` et `Label_MIP` ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="622b0-114">For example, `Label-MIP` and `Label_MIP` aren't supported.</span></span> <span data-ttu-id="622b0-115">La recherche SharePoint prend en charge ces caractères dans les noms d’étiquettes de confidentialité et les noms de type information sensible.</span><span class="sxs-lookup"><span data-stu-id="622b0-115">SharePoint search does support those characters in sensitivity label names and sensitive information type names.</span></span>

## <a name="onedrive-remains-in-preview"></a><span data-ttu-id="622b0-116">OneDrive reste en mode aperçu</span><span class="sxs-lookup"><span data-stu-id="622b0-116">OneDrive remains in preview</span></span>

<span data-ttu-id="622b0-117">Merci pour vos précieux commentaires sur l’intégration de OneDrive pendant notre programme de préversion.</span><span class="sxs-lookup"><span data-stu-id="622b0-117">Thanks for your valuable feedback on OneDrive integration during our preview program.</span></span> <span data-ttu-id="622b0-118">À mesure que nous travaillons sur les détails, vous pouvez constater des données/flux incohérents.</span><span class="sxs-lookup"><span data-stu-id="622b0-118">As we work through the specifics, you may run into inconsistent data / flows.</span></span> <span data-ttu-id="622b0-119">Nous continuerons à proposer OneDrive en préversion jusqu’à ce que tous les correctifs soient en place.</span><span class="sxs-lookup"><span data-stu-id="622b0-119">We'll continue to showcase OneDrive in preview until all fixes are in place.</span></span> <span data-ttu-id="622b0-120">Nous apprécions votre soutien constant.</span><span class="sxs-lookup"><span data-stu-id="622b0-120">We appreciate your continued support.</span></span>


## <a name="see-also"></a><span data-ttu-id="622b0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="622b0-121">See also</span></span>

- [<span data-ttu-id="622b0-122">Prise en main de la classification des données (préversion)</span><span class="sxs-lookup"><span data-stu-id="622b0-122">Get started with data classification (preview)</span></span>](data-classification-overview.md)
- [<span data-ttu-id="622b0-123">Afficher l’activité des étiquettes (aperçu)</span><span class="sxs-lookup"><span data-stu-id="622b0-123">View label activity (preview)</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="622b0-124">Afficher le contenu étiqueté (aperçu)</span><span class="sxs-lookup"><span data-stu-id="622b0-124">View labeled content (preview)</span></span>](data-classification-content-explorer.md)
- [<span data-ttu-id="622b0-125">En savoir plus sur les étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="622b0-125">Learn about sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="622b0-126">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="622b0-126">Learn about retention policies and retention labels</span></span>](retention.md)
- [<span data-ttu-id="622b0-127">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="622b0-127">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)