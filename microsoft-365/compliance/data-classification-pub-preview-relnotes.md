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
ms.openlocfilehash: bbef6729680db2c9a6aec4caa9036ec23fad6949
ms.sourcegitcommit: f6840dfcfdbcadc53cda591fd6cf9ddcb749d303
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2020
ms.locfileid: "44327603"
---
# <a name="data-classification-release-notes"></a><span data-ttu-id="606c3-103">Notes de publication pour la classification des données</span><span class="sxs-lookup"><span data-stu-id="606c3-103">Data classification release notes</span></span>

<span data-ttu-id="606c3-104">Consultez ces notes de publication pour bénéficier d’une expérience optimale avec la classification des données.</span><span class="sxs-lookup"><span data-stu-id="606c3-104">Please review these release notes so that you have the best experience with data classification.</span></span>

## <a name="exchange-mailbox-count"></a><span data-ttu-id="606c3-105">Nombre de boîtes aux lettres Exchange</span><span class="sxs-lookup"><span data-stu-id="606c3-105">Exchange mailbox count</span></span>

<span data-ttu-id="606c3-106">Vous remarquerez qu’une petite info-bulle apparaît lorsque vous explorez des boîtes aux lettres Exchange.</span><span class="sxs-lookup"><span data-stu-id="606c3-106">You will notice a small tool tip appear when you drill into Exchange mailboxes.</span></span> <span data-ttu-id="606c3-107">Il s'agit là d'évoquer le fait que le nombre agrégé affiché pour le type d’information sensible, l’étiquette de confidentialité et l’étiquette de rétention ne correspondent pas parfaitement au nombre d’éléments que vous trouverez dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="606c3-107">This is to call out the fact that the aggregate count displayed for sensitive information type, sensitivity label and retention label may not exactly match the number of items that you will find inside the mailbox.</span></span> <span data-ttu-id="606c3-108">Cela est dû au fait que la descente dans la hiérarchie du dossier permet de récupérer l’affichage en direct du contenu, lequel est classifié, alors que le nombre agrégé est calculé.</span><span class="sxs-lookup"><span data-stu-id="606c3-108">This is because the drill down into the folder fetches the live view of content, which is classified, while the aggregated count is calculated.</span></span>


## <a name="rendering-of-encrypted-documents"></a><span data-ttu-id="606c3-109">Rendu de documents chiffrés</span><span class="sxs-lookup"><span data-stu-id="606c3-109">Rendering of encrypted documents</span></span>

<span data-ttu-id="606c3-110">L'affichage des fichiers SharePoint, Exchange et OneDrive chiffrés n'a pas lieu dans l’explorateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="606c3-110">SharePoint, Exchange, and OneDrive files that are encrypted will not render in the content explorer.</span></span> <span data-ttu-id="606c3-111">Il s’agit d’un problème sensible qui nécessite un équilibre entre le besoin d'afficher le contenu de fichiers dans l’explorateur de contenu et la nécessité de conserver les contenus chiffrés.</span><span class="sxs-lookup"><span data-stu-id="606c3-111">This is a sensitive issue that requires a balance between the need to see file contents in content explorer and the need to keep the contents encrypted.</span></span> <span data-ttu-id="606c3-112">Avec les autorisations accordées par les groupes de rôle de la **visionneuse de liste de l’explorateur de contenu**et la **visionneuse de contenu de l’explorateur de contenu**, un affichage de la liste des fichiers, des métadonnées de fichier et un lien que vous pouvez utiliser pour accéder au contenu via le client web.</span><span class="sxs-lookup"><span data-stu-id="606c3-112">With the permissions granted by **Content Explorer List Viewer**, and **Content Explorer Content Viewer** role groups, you will see a list view of the files, the file  metadata, and a link you can use to access the content via the web client.</span></span>

## <a name="supported-characters-in-retention-label-names-in-sharepoint-search"></a><span data-ttu-id="606c3-113">Caractères pris en charge dans les noms d'étiquettes de rétention de la recherche SharePoint</span><span class="sxs-lookup"><span data-stu-id="606c3-113">Supported characters in retention label names in SharePoint search</span></span>

<span data-ttu-id="606c3-114">La recherche SharePoint ne prend pas en charge les noms d’étiquettes de rétention avec `-` ou `_` dans celles-ci.</span><span class="sxs-lookup"><span data-stu-id="606c3-114">SharePoint search does not support retention label names with `-`, or `_` in them.</span></span> <span data-ttu-id="606c3-115">Par exemple, `Label-MIP` et `Label_MIP` ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="606c3-115">For example `Label-MIP` and `Label_MIP` are not supported.</span></span> <span data-ttu-id="606c3-116">La recherche SharePoint prend en charge ces caractères dans les noms d’étiquettes de confidentialité et les noms de type information sensible.</span><span class="sxs-lookup"><span data-stu-id="606c3-116">SharePoint search does support those characters in sensitivity label names and sensitive information type names.</span></span>

## <a name="onedrive-remains-in-preview"></a><span data-ttu-id="606c3-117">OneDrive reste en mode aperçu</span><span class="sxs-lookup"><span data-stu-id="606c3-117">OneDrive remains in preview</span></span>

<span data-ttu-id="606c3-118">Nous avons écouté vos commentaires intéressants sur l’intégration de OneDrive pendant notre programme d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="606c3-118">We have listened to your valuable feedback on OneDrive integration during our preview program.</span></span> <span data-ttu-id="606c3-119">Au fur et à mesure que nous travaillons dans les détails, vous pouvez être amené à utiliser des données/flux incohérents.</span><span class="sxs-lookup"><span data-stu-id="606c3-119">As we work through the specifics, you may run into inconsistent data / flows.</span></span> <span data-ttu-id="606c3-120">Nous continuerons à présenter OneDrive en version préliminaire jusqu’à ce que tous les correctifs soient en place.</span><span class="sxs-lookup"><span data-stu-id="606c3-120">We will continue to showcase OneDrive in preview till all fixes are in place.</span></span> <span data-ttu-id="606c3-121">Nous apprécions votre support technique.</span><span class="sxs-lookup"><span data-stu-id="606c3-121">We appreciate your continued support on this.</span></span>


## <a name="see-also"></a><span data-ttu-id="606c3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="606c3-122">See also</span></span>

- [<span data-ttu-id="606c3-123">Prise en main de la classification des données (préversion)</span><span class="sxs-lookup"><span data-stu-id="606c3-123">Get started with data classification (preview)</span></span>](data-classification-overview.md)
- [<span data-ttu-id="606c3-124">Afficher l’activité des étiquettes (aperçu)</span><span class="sxs-lookup"><span data-stu-id="606c3-124">View label activity (preview)</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="606c3-125">Afficher le contenu étiqueté (aperçu)</span><span class="sxs-lookup"><span data-stu-id="606c3-125">View labeled content (preview)</span></span>](data-classification-content-explorer.md)
- [<span data-ttu-id="606c3-126">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="606c3-126">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="606c3-127">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="606c3-127">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="606c3-128">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="606c3-128">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)