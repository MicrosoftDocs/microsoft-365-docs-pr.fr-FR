---
title: Prise en main de la classification des données (aperçu)
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
description: Le tableau de bord de classification des données vous permet de consulter les données sensibles qui ont été trouvées et classifiées au sein de votre organisation.
ms.openlocfilehash: 76c1199fa3842428900db197f15728c116f778b9
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42076387"
---
# <a name="data-classification-overview-preview"></a><span data-ttu-id="36033-103">Vue d’ensemble de la classification des données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="36033-103">Data classification overview (preview)</span></span>

<span data-ttu-id="36033-104">En tant qu’administrateur Microsoft 365 ou administrateur de conformité, vous pouvez évaluer et baliser les contenus de votre organisation afin de contrôler leur destination, de les protéger où qu’ils soient et de vous assurer qu’ils sont conservés et supprimés en fonction des besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36033-104">As a Microsoft 365 administrator or compliance administrator, you can evaluate and then tag content in your organization in order to control where it goes, protect it no matter where it is and to ensure that it is preserved and deleted according your your organizations needs.</span></span> <span data-ttu-id="36033-105">Pour ce faire, vous devez utiliser les [étiquettes de confidentialité](sensitivity-labels.md), les [étiquettes de rétention](labels.md) et la classification des informations sensibles par types.</span><span class="sxs-lookup"><span data-stu-id="36033-105">You do this through the application of [sensitivity labels](sensitivity-labels.md), [retention labels](labels.md), and sensitive information type classification.</span></span> <span data-ttu-id="36033-106">Plusieurs méthodes s’offrent à vous pour effectuer la découverte, l’évaluation et le balisage, mais le résultat final est de disposer d’un grand nombre de documents et de messages électroniques balisés et classifiés avec ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="36033-106">There are various ways to do the discovery, evaluation and tagging, but the end result is that you may have very large numbers of documents and emails that are tagged and classified with one or both of these labels.</span></span> <span data-ttu-id="36033-107">Après avoir appliqué vos étiquettes de rétention et vos étiquettes de sensibilité, vous souhaiterez voir de quelle manière elles sont utilisées par vos clients.</span><span class="sxs-lookup"><span data-stu-id="36033-107">After you apply  your retention labels and sensitivity labels, you’ll want to see how the labels are being used across your tenant and what is being done with those items.</span></span> <span data-ttu-id="36033-108">La page classification des données fournit une visibilité dans ce corps de contenu, notamment :</span><span class="sxs-lookup"><span data-stu-id="36033-108">The data classification page provides visibility into that body of content, specifically:</span></span>

- <span data-ttu-id="36033-109">le nombre d’éléments qui ont été classifiés en tant que types d’informations sensibles et la nature de ces classifications</span><span class="sxs-lookup"><span data-stu-id="36033-109">the number items that have been classified as a sensitive information type and what those classifications are</span></span>
- <span data-ttu-id="36033-110">les étiquettes de confidentialité les plus utilisées dans Microsoft 365 et Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="36033-110">the top applied sensitivity labels in both Microsoft 365 and Azure Information Protection</span></span>
- <span data-ttu-id="36033-111">les étiquettes de rétention les plus utilisées</span><span class="sxs-lookup"><span data-stu-id="36033-111">the top applied retention labels</span></span>
- <span data-ttu-id="36033-112">la synthèse des activités que les utilisateurs effectuent sur votre contenu sensible</span><span class="sxs-lookup"><span data-stu-id="36033-112">a summary of activities that users are taking on your sensitive content</span></span>
- <span data-ttu-id="36033-113">les emplacements de vos données sensibles et conservées</span><span class="sxs-lookup"><span data-stu-id="36033-113">the locations of your sensitive and retained data</span></span>

<span data-ttu-id="36033-114">Vous trouverez la classification des données dans le **Centre de conformité Microsoft 365** ou le **Centre de sécurité Microsoft 365** > **Classification** > **Classification des données**.</span><span class="sxs-lookup"><span data-stu-id="36033-114">You can find data classification in the **Microsoft 365 compliance center** or **Microsoft 365 security center** > **Classification** > **Data Classification**.</span></span>

## <a name="sensitive-information-types-used-most-in-your-content"></a><span data-ttu-id="36033-115">Types d’informations sensibles utilisés le plus fréquemment dans votre contenu</span><span class="sxs-lookup"><span data-stu-id="36033-115">Sensitive information types used most in your content</span></span>

<span data-ttu-id="36033-116">Microsoft 365 fournit de nombreuses définitions des types d’informations sensibles, par exemple un élément contenant un numéro de sécurité sociale ou un numéro de carte bancaire.</span><span class="sxs-lookup"><span data-stu-id="36033-116">Microsoft 365 comes with many definitions of sensitive information types, such as an item containing a social security number or a credit card number.</span></span> <span data-ttu-id="36033-117">Pour plus d’informations sur les types d’informations sensibles, voir [Eléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="36033-117">For more information on sensitive information types, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>

<span data-ttu-id="36033-118">La carte type d’informations sensibles présente les principaux types d’informations sensibles qui ont été détectés et étiquetés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36033-118">The sensitive information type card shows the top sensitive information types that have been found and labeled across your organization.</span></span>

![principaux types d’informations sensibles](../media/data-classification-sens-info-types-card.png)

<span data-ttu-id="36033-120">Pour déterminer le nombre d’éléments dans une catégorie de classification donnée, pointez sur la barre pour la catégorie.</span><span class="sxs-lookup"><span data-stu-id="36033-120">To find out how many items are in any given classification category, hover over the bar for the category.</span></span>

![détail de pointage des principaux types d’informations sensibles](../media/data-classification-sens-info-types-hover.png)

> [!NOTE]
> <span data-ttu-id="36033-122">Si la carte affiche le message « Aucune donnée détectée avec des informations sensibles ».</span><span class="sxs-lookup"><span data-stu-id="36033-122">If the card displays the message "No data found with sensitive information".</span></span> <span data-ttu-id="36033-123">Cela signifie qu’il n’y a aucun élément de votre organisation classifié comme étant un type d’informations sensibles ou aucun élément analysé.</span><span class="sxs-lookup"><span data-stu-id="36033-123">It means that there are no items in your organization that have been classified as being a sensitive information type or no items that have been crawled.</span></span> <span data-ttu-id="36033-124">Pour commencer à utiliser les étiquettes, voir :</span><span class="sxs-lookup"><span data-stu-id="36033-124">To get started with labels, see:</span></span>
>- [<span data-ttu-id="36033-125">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="36033-125">Sensitivity labels</span></span>](sensitivity-labels.md)
>- [<span data-ttu-id="36033-126">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="36033-126">Retention labels</span></span>](labels.md)
>- [<span data-ttu-id="36033-127">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="36033-127">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

## <a name="top-sensitivity-labels-applied-to-content"></a><span data-ttu-id="36033-128">Principales étiquettes de confidentialité appliquées au contenu</span><span class="sxs-lookup"><span data-stu-id="36033-128">Top sensitivity labels applied to content</span></span>

<span data-ttu-id="36033-129">Lorsque vous appliquez une étiquette de confidentialité à un élément via Microsoft 365 ou Azure information protection (AIP), deux événements se produisent :</span><span class="sxs-lookup"><span data-stu-id="36033-129">When you apply a sensitivity label to an item either through Microsoft 365 or Azure Information Protection (AIP), two things happen:</span></span>

- <span data-ttu-id="36033-130">une balise qui indique que la valeur de l’élément pour votre organisation est incorporée dans le document et qu’elle le suivra partout</span><span class="sxs-lookup"><span data-stu-id="36033-130">a tag that indicates the value of the item to your org is embedded in the document and will follow it everywhere it goes</span></span>
- <span data-ttu-id="36033-131">la présence de la balise permet différents comportements de protection, tels que le filigrane ou le chiffrement obligatoires.</span><span class="sxs-lookup"><span data-stu-id="36033-131">the presence of the tag enables various protective behaviors, such as mandatory watermarking or encryption.</span></span> <span data-ttu-id="36033-132">Lorsque la protection de point de terminaison est activée, vous pouvez même empêcher un élément de quitter votre contrôle organisationnel.</span><span class="sxs-lookup"><span data-stu-id="36033-132">With end point protection enabled you can even prevent an item from leaving your organizational control.</span></span>

<span data-ttu-id="36033-133">Pour plus d’informations sur les étiquettes de confidentialité, voir : [En savoir plus sur les étiquettes de confidentialité](sensitivity-labels.md).</span><span class="sxs-lookup"><span data-stu-id="36033-133">For more information on sensitivity labels, see: [Learn about sensitivity labels](sensitivity-labels.md)</span></span>

<span data-ttu-id="36033-134">Les étiquettes de confidentialité doivent être activées pour les fichiers stockés dans SharePoint et OneDrive pour que les données correspondantes apparaissent dans la page de classification des données.</span><span class="sxs-lookup"><span data-stu-id="36033-134">Sensitivity labels must be enabled for files that are in SharePoint and OneDrive in order for the corresponding data to surface in the data classification page.</span></span> <span data-ttu-id="36033-135">Pour en savoir plus, consulter [Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="36033-135">For more information, see [Enable sensitivity labels for Office files in SharePoint and OneDrive (public preview)](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

<span data-ttu-id="36033-136">La carte d’étiquette de confidentialité affiche le nombre d’éléments (adresse de messagerie ou document) par niveau de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="36033-136">The sensitivity label card shows the number of items (email or document) by sensitivity level.</span></span>

![répartition du contenu par capture d’écran de l’espace réservé pour la classification des étiquettes de confidentialité](../media/data-classification-top-sensitivity-labels-applied.png)

> [!NOTE]
> <span data-ttu-id="36033-138">Si vous n’avez pas créé ou publié d’étiquettes de confidentialité ou si aucune étiquette de confidentialité n’a été appliquée à votre contenu, cette carte affiche le message « Aucune étiquette de confidentialité détectée ».</span><span class="sxs-lookup"><span data-stu-id="36033-138">If you haven't created or published any sensitivity labels or no content has had a sensitivity label applied, this card will display the message "No sensitivity labels detected".</span></span> <span data-ttu-id="36033-139">Pour commencer à utiliser les étiquettes, voir :</span><span class="sxs-lookup"><span data-stu-id="36033-139">To get started with labels, see:</span></span>
>- <span data-ttu-id="36033-140">[étiquettes de confidentialité](sensitivity-labels.md) ou pour AIP [configurer la stratégie Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy)</span><span class="sxs-lookup"><span data-stu-id="36033-140">[sensitivity labels](sensitivity-labels.md) or for AIP [Configure the Azure information protection policy](https://docs.microsoft.com/azure/information-protection/configure-policy)</span></span>

## <a name="top-retention-labels-applied-to-content"></a><span data-ttu-id="36033-141">Principales étiquettes de rétention appliquées au contenu</span><span class="sxs-lookup"><span data-stu-id="36033-141">Top retention labels applied to content</span></span>

<span data-ttu-id="36033-142">Les étiquettes de rétention sont utilisées pour gérer la disposition du contenu au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36033-142">Retention labels are used to manage the disposition of content in your organization.</span></span> <span data-ttu-id="36033-143">Lorsqu’elles sont appliquées, elles peuvent être utilisées pour contrôler la durée de conservation d’un document avant sa suppression, s’il doit être révisé avant sa suppression, la date d’expiration de sa période de rétention, ou s’il doit être marqué comme un enregistrement qui ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="36033-143">When applied, they can be used to control how long a document will be kept before deletion, whether it should be reviewed prior to deletion, when it's retention period expires, or whether it should be marked as a record which can never be deleted.</span></span> <span data-ttu-id="36033-144">Pour plus d’informations, voir[Vue d’ensemble des étiquettes de rétention](labels.md).</span><span class="sxs-lookup"><span data-stu-id="36033-144">For more information see, [Overview of retention labels](labels.md).</span></span>

<span data-ttu-id="36033-145">La carte étiquettes de rétention les plus utilisées vous indique le nombre d’éléments ayant une étiquette de rétention donnée.</span><span class="sxs-lookup"><span data-stu-id="36033-145">The top applied retention labels card shows you how many items have a given retention label.</span></span>

![capture d’écran de l’espace réservé pour les étiquettes de rétention les plus utilisées](../media/data-classification-top-retention-labels-applied.png)

> [!NOTE]
> <span data-ttu-id="36033-147">Si cette carte affiche le message, « Aucune étiquette de rétention détectée », cela veut dire que vous n’avez pas créé ou publié d’étiquettes de rétention ou qu’aucune étiquette de rétention n’a été appliquée à votre contenu.</span><span class="sxs-lookup"><span data-stu-id="36033-147">If this card displays the message, "No retention labels detected, it means you haven't created or published any retention  labels or no content has had a retention label applied.</span></span> <span data-ttu-id="36033-148">Pour commencer à utiliser les étiquettes de rétention, voir :</span><span class="sxs-lookup"><span data-stu-id="36033-148">To get started with retention labels, see:</span></span>
>- [<span data-ttu-id="36033-149">Vue d’ensemble des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="36033-149">Overview of retention labels</span></span>](labels.md)

## <a name="top-activities-detected"></a><span data-ttu-id="36033-150">Principales activités détectées</span><span class="sxs-lookup"><span data-stu-id="36033-150">Top activities detected</span></span>

<span data-ttu-id="36033-151">Cette carte décrit brièvement les actions les plus courantes que les utilisateurs effectuent sur les éléments étiquetés comme sensibles.</span><span class="sxs-lookup"><span data-stu-id="36033-151">This card provides a quick summary of the most common actions that users are taking on the sensitivity labeled items.</span></span> <span data-ttu-id="36033-152">Vous pouvez utiliser [L’explorateur d’activité](data-classification-activity-explorer.md) pour explorer en profondeur huit activités différentes que Microsoft 365 suit sur le contenu étiqueté et le contenu qui se trouve sur les points de terminaison de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="36033-152">You can use the [Activity explorer](data-classification-activity-explorer.md) to drill deep down on eight different activities that Microsoft 365 tracks on labeled content and content that is located on Windows 10 endpoints.</span></span>

> [!NOTE]
> <span data-ttu-id="36033-153">Si cette carte affiche le message « Aucune activité détectée », cela signifie qu’il n’y a eu aucune activité sur les fichiers, ou que l’audit de l’utilisateur et de l’administrateur n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="36033-153">If this card displays the message, "No activity detected" it means that there's been no activity on the files or that user and admin auditing isn't turned on.</span></span> <span data-ttu-id="36033-154">Pour activer les journaux d’audit, voir :</span><span class="sxs-lookup"><span data-stu-id="36033-154">To turn the audit logs on , see:</span></span>
>- [<span data-ttu-id="36033-155">Effectuer des recherches dans le journal d’audit depuis le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="36033-155">Search the audit log in security & compliance center</span></span>](search-the-audit-log-in-security-and-compliance.md)

## <a name="sensitivity-and-retention-labeled-data-by-location"></a><span data-ttu-id="36033-156">Données étiquetées confidentielles ou retenues par emplacement</span><span class="sxs-lookup"><span data-stu-id="36033-156">Sensitivity and retention labeled data by location</span></span>

<span data-ttu-id="36033-157">L’objectif de la création de rapports sur la classification des données est de fournir une visibilité sur le nombre d’éléments qui ont une étiquette, ainsi que leur emplacement.</span><span class="sxs-lookup"><span data-stu-id="36033-157">The point of the data classification reporting is to provide visibility into the number of items that have which label as well as their location.</span></span> <span data-ttu-id="36033-158">Ces cartes vous permettent de connaître le nombre d’éléments étiquetés dans Exchange, SharePoint, OneDrive, etc.</span><span class="sxs-lookup"><span data-stu-id="36033-158">These cards let you know how many labeled items the are in Exchange, SharePoint, and OneDrive etc.</span></span>

> [!NOTE]
> <span data-ttu-id="36033-159">Si cette carte affiche le message, « Aucun emplacement détecté », cela veut dire que vous n’avez pas créé ou publié d’étiquettes de confidentialité ou qu’aucune étiquette de confidentialité n’a été appliquée à votre contenu.</span><span class="sxs-lookup"><span data-stu-id="36033-159">If this card displays the message, "No locations detected, it means you haven't created or published any sensitivity labels or no content has had a retention label applied.</span></span> <span data-ttu-id="36033-160">Pour commencer à utiliser les étiquettes de confidentialité, voir :</span><span class="sxs-lookup"><span data-stu-id="36033-160">To get started with sensitivity labels, see:</span></span>
>- [<span data-ttu-id="36033-161">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="36033-161">Sensitivity labels</span></span>](sensitivity-labels.md)

## <a name="see-also"></a><span data-ttu-id="36033-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36033-162">See also</span></span>

- [<span data-ttu-id="36033-163">Afficher l’activité des étiquettes (aperçu)</span><span class="sxs-lookup"><span data-stu-id="36033-163">View label activity (preview)</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="36033-164">Afficher le contenu étiqueté (aperçu)</span><span class="sxs-lookup"><span data-stu-id="36033-164">View labeled content (preview)</span></span>](data-classification-content-explorer.md)
- [<span data-ttu-id="36033-165">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="36033-165">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="36033-166">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="36033-166">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="36033-167">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="36033-167">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="36033-168">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="36033-168">Overview of retention policies</span></span>](retention-policies.md)
