---
title: Appliquer automatiquement une étiquette sensibilité au contenu
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
audience: Admin
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
description: Lorsque vous créez une étiquette de critère de diffusion, vous pouvez affecter automatiquement une étiquette à un document ou message électronique ou vous pouvez inviter les utilisateurs pour sélectionner l’étiquette que vous recommandez.
ms.openlocfilehash: a1ea81bf8c65d3f54d26b19eae3b590f11283c30
ms.sourcegitcommit: 109b44aa71bb8453d0a602663df0fcf7ed7dfdbe
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/25/2020
ms.locfileid: "42277211"
---
# <a name="apply-a-sensitivity-label-to-content-automatically"></a><span data-ttu-id="5f39a-103">Appliquer automatiquement une étiquette sensibilité au contenu</span><span class="sxs-lookup"><span data-stu-id="5f39a-103">Apply a sensitivity label to content automatically</span></span>

<span data-ttu-id="5f39a-104">Lorsque vous créez une étiquette de confidentialité, vous pouvez attribuer automatiquement une étiquette au contenu ayant des informations sensibles, ou vous pouvez inviter les utilisateurs à appliquer celle que vous recommandez.</span><span class="sxs-lookup"><span data-stu-id="5f39a-104">When you create a sensitivity label, you can automatically assign that label to content when it contains sensitive information, or you can prompt users to apply the label that you recommend.</span></span>

<span data-ttu-id="5f39a-105">La possibilité d’appliquer automatiquement des étiquettes à du contenu est importante pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f39a-105">The ability to apply sensitivity labels to content automatically is important because:</span></span>

- <span data-ttu-id="5f39a-106">Vous n’avez pas besoin de former les utilisateurs concernant l’ensemble de vos classifications.</span><span class="sxs-lookup"><span data-stu-id="5f39a-106">You don't need to train your users on all of your classifications.</span></span>

- <span data-ttu-id="5f39a-107">Vous n’avez pas à dépendre des utilisateurs pour classer correctement tout le contenu.</span><span class="sxs-lookup"><span data-stu-id="5f39a-107">You don't need to rely on users to classify all content correctly.</span></span>

- <span data-ttu-id="5f39a-108">Les utilisateurs n’ont plus à connaître les stratégies de gouvernance des données : à la place, ils peuvent se concentrer sur leur travail.</span><span class="sxs-lookup"><span data-stu-id="5f39a-108">Users no longer need to know about your policies — they can instead focus on their work.</span></span>

<span data-ttu-id="5f39a-109">L’étiquetage automatique dans les applications Office pour Windows est pris en charge par le client d’étiquetage unifié Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="5f39a-109">Automatic labeling in Office apps for Windows is supported by the Azure Information Protection unified labeling client.</span></span> <span data-ttu-id="5f39a-110">Pour l’étiquetage intégré dans les applications Office, cette fonctionnalité est [en mode Aperçu pour certaines applications](sensitivity-labels-office-apps.md#support-for-sensitivity-label-capabilities-in-apps).</span><span class="sxs-lookup"><span data-stu-id="5f39a-110">For built-in labeling in Office apps, this capability is [in preview for some apps](sensitivity-labels-office-apps.md#support-for-sensitivity-label-capabilities-in-apps).</span></span>

<span data-ttu-id="5f39a-111">Les paramètres d’étiquetage automatique des applications Office sont disponibles lorsque vous [créer ou modifier une étiquette de confidentialité](create-sensitivity-labels.md) :</span><span class="sxs-lookup"><span data-stu-id="5f39a-111">The auto-labeling settings for Office apps are available when you [create or edit a sensitivity label](create-sensitivity-labels.md):</span></span>

![Options d’étiquetage automatique pour les étiquettes de confidentialité](../media/sensitivity-labels-auto-labeling-options.png)

## <a name="how-to-configure-auto-labeling-for-office-apps"></a><span data-ttu-id="5f39a-113">Comment configurer l’étiquetage automatique pour les applications Office</span><span class="sxs-lookup"><span data-stu-id="5f39a-113">How to configure auto-labeling for Office apps</span></span>

<span data-ttu-id="5f39a-114">L’une des fonctionnalités les plus puissantes des étiquettes de confidentialité est la possibilité d’appliquer celles-ci automatiquement à tout contenu correspondant à certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="5f39a-114">One of the most powerful features of sensitivity labels is the ability to apply them automatically to content that matches certain conditions.</span></span> <span data-ttu-id="5f39a-115">Dans ce cas, les personnes au sein de votre organisation n’ont pas besoin d’appliquer les étiquettes de confidentialité. Office 365 s’en charge à leur place.</span><span class="sxs-lookup"><span data-stu-id="5f39a-115">In this case, people in your organization don't need to apply the sensitivity labels — Office 365 does the work for them.</span></span>

<span data-ttu-id="5f39a-116">Vous pouvez choisir d’appliquer automatiquement des étiquettes de confidentialité au contenu lorsque celui-ci contient des types spécifiques d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="5f39a-116">You can choose to apply sensitivity labels to content automatically when that content contains specific types of sensitive information.</span></span> <span data-ttu-id="5f39a-117">Choisissez parmi une liste de types d’informations ou de classifieurs sensibles :</span><span class="sxs-lookup"><span data-stu-id="5f39a-117">Choose from a list of sensitive info types or classifers:</span></span>

![Conditions de l’étiquetage automatique dans les applications Office](../media/sensitivity-labels-conditions.png)

> [!NOTE]
> <span data-ttu-id="5f39a-119">Pour le moment, l’option des **classifieurs** se présente sous la forme d’une version d’évaluation limitée et vous devez envoyer un formulaire à Microsoft pour activer cette fonctionnalité pour votre client.</span><span class="sxs-lookup"><span data-stu-id="5f39a-119">Currently, the option for **Classifers** is in limited preview and requires you to submit a form to Microsoft to enable this capability for your tenant.</span></span> <span data-ttu-id="5f39a-120">Pour plus d’informations, consultez l’article de blog [annonçant l'étiquetage automatique dans les applications Office à l'aide de classifieurs intégrés (édition limitée)](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/announcing-automatic-labeling-in-office-apps-using-built-in/ba-p/1192889).</span><span class="sxs-lookup"><span data-stu-id="5f39a-120">For more information, see the blog post [Announcing automatic labeling in Office Apps using built-in classifiers - Limited Preview](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/announcing-automatic-labeling-in-office-apps-using-built-in/ba-p/1192889).</span></span>

<span data-ttu-id="5f39a-121">Lorsqu’une étiquette de confidentialité est appliquée automatiquement, les utilisateurs voit une notification dans leur application Office.</span><span class="sxs-lookup"><span data-stu-id="5f39a-121">When this sensitivity label is automatically applied, the user sees a notification in their Office app.</span></span> <span data-ttu-id="5f39a-122">Ils peuvent sélectionner **OK** pour ignorer la notification.</span><span class="sxs-lookup"><span data-stu-id="5f39a-122">They can choose **OK** to dismiss the notification.</span></span>

![Notification dont un document disposait d’une étiquette appliquée automatiquement](../media/sensitivity-labels-msg-doc-was-auto-labeled.PNG)

### <a name="configuring-sensitive-info-types-for-a-label"></a><span data-ttu-id="5f39a-124">Configuration des types d’informations sensibles pour une étiquette</span><span class="sxs-lookup"><span data-stu-id="5f39a-124">Configuring sensitive info types for a label</span></span>

<span data-ttu-id="5f39a-125">Lorsque vous sélectionnez l’option **types d’informations sensibles**, vous voyez la même liste de types d'informations sensibles que lorsque vous créez une stratégie de protection contre la perte des données (DLP, data loss prevention).</span><span class="sxs-lookup"><span data-stu-id="5f39a-125">When you select the **Sensitive info types** option, you see the same list of sensitive information types as when you create a data loss prevention (DLP) policy.</span></span> <span data-ttu-id="5f39a-126">Par exemple, vous pouvez appliquer automatiquement une étiquette hautement confidentiel à tout contenu ayant des informations d’identification personnelle (PII) de clients, comme les numéros de carte de crédit ou les numéros de sécurité sociale :</span><span class="sxs-lookup"><span data-stu-id="5f39a-126">So you can, for example, automatically apply a Highly Confidential label to any content that contains customers' personally identifiable information (PII), such as credit card numbers or social security numbers:</span></span>

![Types d’informations sensibles pour l’étiquetage automatique dans les applications Office](../media/sensitivity-labels-sensitive-info-types.png)

<span data-ttu-id="5f39a-128">Après avoir sélectionné vos types d’informations sensibles, vous pouvez affiner votre condition en modifiant le nombre d’instances ou la précision des correspondances.</span><span class="sxs-lookup"><span data-stu-id="5f39a-128">After you select your sensitive information types, you can refine your condition by changing the instance count or match accuracy.</span></span> <span data-ttu-id="5f39a-129">Pour plus d’informations, voir[Optimisation des règles afin de les rendre plus facile ou plus difficile à associer](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span><span class="sxs-lookup"><span data-stu-id="5f39a-129">For more information, see [Tuning rules to make them easier or harder to match](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span></span>

<span data-ttu-id="5f39a-130">De plus, vous pouvez choisir si une condition doit détecter tous les types d’informations sensibles ou seulement l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="5f39a-130">Further, you can choose whether a condition must detect all sensitive information types, or just one of them.</span></span> <span data-ttu-id="5f39a-131">Pour améliorer la flexibilité ou la complexité de vos conditions, vous pouvez ajouter des groupes et utiliser des opérateurs logiques entre les groupes.</span><span class="sxs-lookup"><span data-stu-id="5f39a-131">And to make your conditions more flexible or complex, you can add groups and use logical operators between the groups.</span></span> <span data-ttu-id="5f39a-132">Pour plus d’informations, voir [Regroupement et opérateurs logiques](data-loss-prevention-policies.md#grouping-and-logical-operators).</span><span class="sxs-lookup"><span data-stu-id="5f39a-132">For more information, see [Grouping and logical operators](data-loss-prevention-policies.md#grouping-and-logical-operators).</span></span>

![Options pour le nombre d’instances et la précision des correspondances](../media/Sensitivity-labels-instance-count-match-accuracy.png)

### <a name="configuring-classifers-for-a-label"></a><span data-ttu-id="5f39a-134">Configuration des classifieurs pour une étiquette</span><span class="sxs-lookup"><span data-stu-id="5f39a-134">Configuring classifers for a label</span></span>

<span data-ttu-id="5f39a-135">Lorsque vous sélectionnez l’option **classifieurs**, sélectionnez un ou plusieurs classifieurs prédéfinis :</span><span class="sxs-lookup"><span data-stu-id="5f39a-135">When you select the **Classifers** option, select one or more of the built-in classifiers:</span></span>

![Options pour les classifieurs et les étiquettes de sensibilité](../media/sensitivity-labels-classifers.png)

<span data-ttu-id="5f39a-137">Pour plus d’informations sur ces classifieurs, voir [Prise en main des classifieurs d’entraînement (version d'essai)](classifier-getting-started-with.md).</span><span class="sxs-lookup"><span data-stu-id="5f39a-137">For more information about these classifers, see [Getting started with trainable classifiers (preview)](classifier-getting-started-with.md).</span></span>

<span data-ttu-id="5f39a-138">Pendant la période d’évaluation, les applications suivantes prennent en charge les classifieurs pour les étiquettes de confidentialité :</span><span class="sxs-lookup"><span data-stu-id="5f39a-138">During the preview period, the following apps support classifers for sensitivity labels:</span></span>

- <span data-ttu-id="5f39a-139">Applications de bureau Office 365 ProPlus pour Windows, de [Office Insider](https://office.com/insider) :</span><span class="sxs-lookup"><span data-stu-id="5f39a-139">Office 365 ProPlus desktop apps for Windows, from [Office Insider](https://office.com/insider):</span></span>
    - <span data-ttu-id="5f39a-140">Word</span><span class="sxs-lookup"><span data-stu-id="5f39a-140">Word</span></span>
    - <span data-ttu-id="5f39a-141">Excel</span><span class="sxs-lookup"><span data-stu-id="5f39a-141">Excel</span></span>
    - <span data-ttu-id="5f39a-142">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="5f39a-142">PowerPoint</span></span>

- <span data-ttu-id="5f39a-143">Office pour les applications Web, lorsque vous avez [activé les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)](sensitivity-labels-sharepoint-onedrive-files.md) :</span><span class="sxs-lookup"><span data-stu-id="5f39a-143">Office for the web apps, when you have [enabled sensitivity labels for Office files in SharePoint and OneDrive (public preview)](sensitivity-labels-sharepoint-onedrive-files.md):</span></span>
    - <span data-ttu-id="5f39a-144">Word</span><span class="sxs-lookup"><span data-stu-id="5f39a-144">Word</span></span>
    - <span data-ttu-id="5f39a-145">Excel</span><span class="sxs-lookup"><span data-stu-id="5f39a-145">Excel</span></span>
    - <span data-ttu-id="5f39a-146">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="5f39a-146">PowerPoint</span></span>
    - <span data-ttu-id="5f39a-147">Outlook</span><span class="sxs-lookup"><span data-stu-id="5f39a-147">Outlook</span></span>

## <a name="recommend-that-the-user-apply-a-sensitivity-label"></a><span data-ttu-id="5f39a-148">Recommandé que l’utilisateur applique une étiquette de critère de diffusion</span><span class="sxs-lookup"><span data-stu-id="5f39a-148">Recommend that the user apply a sensitivity label</span></span>

<span data-ttu-id="5f39a-149">Si vous le souhaitez, vous pouvez recommander à vos utilisateurs qu’ils appliquent l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="5f39a-149">If you prefer, you can recommend to your users that they apply the label.</span></span> <span data-ttu-id="5f39a-150">Cette option permet à vos utilisateurs d’accepter la classification et toute protection associée, ou d’ignorer la recommandation si l’étiquette ne convient pas à leur contenu.</span><span class="sxs-lookup"><span data-stu-id="5f39a-150">With this option, your users can accept the classification and any associated protection, or dismiss the recommendation if the label isn't suitable for their content.</span></span>

<span data-ttu-id="5f39a-151">Les étiquettes recommandées sont prises en charge dans Word, PowerPoint et Excel.</span><span class="sxs-lookup"><span data-stu-id="5f39a-151">Recommended labels are supported for Word, PowerPoint, and Excel.</span></span>

![Option pour recommander une étiquette de confidentialité à des utilisateurs](../media/Sensitivity-labels-Recommended-label-option.png)

<span data-ttu-id="5f39a-p110">Voici un exemple d’une invite de commandes lorsque vous configurez une condition à appliquer une étiquette comme action recommandée avec un Conseil de stratégie personnalisé. Vous pouvez choisir quel texte s’affiche dans le Conseil de stratégie.</span><span class="sxs-lookup"><span data-stu-id="5f39a-p110">Here's an example of a prompt when you configure a condition to apply a label as a recommended action, with a custom policy tip. You can choose what text is displayed in the policy tip.</span></span>

![Invite à appliquer une étiquette recommandée](../media/Sensitivity-label-Prompt-for-required-label.png)

## <a name="how-automatic-or-recommended-labels-are-applied"></a><span data-ttu-id="5f39a-156">Comment les étiquettes automatiques ou recommandées sont appliquées</span><span class="sxs-lookup"><span data-stu-id="5f39a-156">How automatic or recommended labels are applied</span></span>

- <span data-ttu-id="5f39a-157">L’étiquetage automatique s’applique à Word, Excel et PowerPoint lors de l’enregistrement d’un document et à Outlook lorsque vous envoyez un courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5f39a-157">Automatic labeling applies to Word, Excel, and PowerPoint when you save a document, and to Outlook when you send an email.</span></span> <span data-ttu-id="5f39a-158">Ces conditions détectent les informations sensibles dans le corps de texte dans les documents et les courriers électroniques, ainsi que dans les en-têtes et pieds de page, mais pas dans la ligne d’objet ni dans les pièces jointes du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5f39a-158">These conditions detect sensitive information in the body text in documents and emails, and to headers and footers — but not in the subject line or attachments of email.</span></span>

- <span data-ttu-id="5f39a-159">Vous ne pouvez pas utiliser la classification automatique pour les documents et les e-mails qui ont été précédemment étiquetés manuellement ou automatiquement avec une classification supérieure.</span><span class="sxs-lookup"><span data-stu-id="5f39a-159">You can't use automatic labeling for documents and emails that were previously manually labeled, or previously automatically labeled with a higher sensitivity.</span></span> <span data-ttu-id="5f39a-160">N’oubliez pas que vous ne pouvez appliquer qu’une seule étiquette de confidentialité à un document ou un e-mail (en plus d’une seule étiquette de rétention).</span><span class="sxs-lookup"><span data-stu-id="5f39a-160">Remember, you can only apply a single sensitivity label to a document or email (in addition to a single retention label).</span></span>

- <span data-ttu-id="5f39a-161">La classification recommandée s’applique à Word, Excel et PowerPoint lorsque vous enregistrez des documents.</span><span class="sxs-lookup"><span data-stu-id="5f39a-161">Recommended labeling applies to Word, Excel, and PowerPoint when you save documents.</span></span>

- <span data-ttu-id="5f39a-162">Vous ne pouvez pas utiliser la classification recommandée pour les documents qui ont été étiquetés précédemment avec une classification supérieure.</span><span class="sxs-lookup"><span data-stu-id="5f39a-162">You can't use recommended labeling for documents that were previously labeled with a higher sensitivity.</span></span> <span data-ttu-id="5f39a-163">Lorsque le contenu est déjà étiqueté avec une classification supérieure, l'utilisateur ne voit pas l'invite avec la recommandation et le conseil de stratégie.</span><span class="sxs-lookup"><span data-stu-id="5f39a-163">When the content's already labeled with a higher sensitivity, the user won't see the prompt with the recommendation and policy tip.</span></span>

## <a name="how-multiple-conditions-are-evaluated-when-they-apply-to-more-than-one-label"></a><span data-ttu-id="5f39a-164">Comment plusieurs conditions sont évaluées lorsqu’elles s’appliquent à plus d’une étiquette</span><span class="sxs-lookup"><span data-stu-id="5f39a-164">How multiple conditions are evaluated when they apply to more than one label</span></span>

<span data-ttu-id="5f39a-p114">Les étiquettes sont classées pour évaluation en fonction de leur position que vous spécifiez dans la stratégie: l’étiquette positionné a tout d’abord la position la plus basse (au moins sensible) et l’étiquette positionnée a dernière position plus élevée (plus sensible). Pour plus d’informations sur la priorité, voir [Priorité étiquettes (ordre aspects importants)](sensitivity-labels.md#label-priority-order-matters).</span><span class="sxs-lookup"><span data-stu-id="5f39a-p114">The labels are ordered for evaluation according to their position that you specify in the policy: The label positioned first has the lowest position (least sensitive) and the label positioned last has the highest position (most sensitive). For more information on priority, see [Label priority (order matters)](sensitivity-labels.md#label-priority-order-matters).</span></span>

## <a name="dont-configure-a-parent-label-to-be-applied-automatically-or-recommended"></a><span data-ttu-id="5f39a-167">Ne configurez pas une étiquette parent pour l’appliquer automatiquement ou la recommander.</span><span class="sxs-lookup"><span data-stu-id="5f39a-167">Don't configure a parent label to be applied automatically or recommended</span></span>

<span data-ttu-id="5f39a-168">Une étiquette parent (une étiquette comportant des sous-étiquettes) ne peut pas être appliquée au contenu.</span><span class="sxs-lookup"><span data-stu-id="5f39a-168">Remember, you can't apply a parent label (a label with sublabels) to content.</span></span> <span data-ttu-id="5f39a-169">Évitez de configurer une étiquette parent pour l’appliquer automatiquement ou la recommander, car elle ne sera pas appliquée au contenu des applications Office qui utilisent le client d’étiquetage unifié Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="5f39a-169">Make sure that you don't configure a parent label to be auto-applied or recommended, because the parent label won't be applied to content in Office apps that use the Azure Information Protection unified labeling client.</span></span> <span data-ttu-id="5f39a-170">Pour en savoir plus sur les étiquettes parents et les sous-étiquettes, consultez la section [Sous-étiquettes (regroupement d’étiquettes)](sensitivity-labels.md#sublabels-grouping-labels).</span><span class="sxs-lookup"><span data-stu-id="5f39a-170">For more information on parent labels and sublabels, see [Sublabels (grouping labels)](sensitivity-labels.md#sublabels-grouping-labels).</span></span>
