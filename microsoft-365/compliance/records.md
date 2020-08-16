---
title: Découvrir les enregistrements
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Découvrir les enregistrements pour vous aider à implémenter une solution de gestion des enregistrements dans Microsoft 365.
ms.openlocfilehash: e64e91aeef307d05f23c47987a84baaf386324df
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46685440"
---
# <a name="learn-about-records"></a><span data-ttu-id="9511d-103">Découvrir les enregistrements</span><span class="sxs-lookup"><span data-stu-id="9511d-103">Learn about records</span></span>

><span data-ttu-id="9511d-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="9511d-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="9511d-105">La gestion des enregistrements dans Microsoft 365 permet à votre organisation de respecter les stratégies d’entreprise et les obligations légales ou réglementaires, tout en réduisant les risques et la responsabilité juridique.</span><span class="sxs-lookup"><span data-stu-id="9511d-105">Managing records in Microsoft 365 helps your organization comply with corporate policies and legal or regulatory obligations, while also reducing risk and legal liability.</span></span>

<span data-ttu-id="9511d-106">Lorsque le contenu est marqué comme un enregistrement :</span><span class="sxs-lookup"><span data-stu-id="9511d-106">When content is marked as a record:</span></span>

- <span data-ttu-id="9511d-107">Des restrictions sont appliquées aux éléments en ce qui concerne les [actions autorisées ou bloquées](#compare-restrictions-for-what-actions-are-allowed-or-blocked).</span><span class="sxs-lookup"><span data-stu-id="9511d-107">Restrictions are placed on the items in terms of what [actions are allowed or blocked](#compare-restrictions-for-what-actions-are-allowed-or-blocked).</span></span>

- <span data-ttu-id="9511d-108">Des activités supplémentaires sur l’élément sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="9511d-108">Additional activities about the item are logged.</span></span>

- <span data-ttu-id="9511d-109">Vous avez une preuve de destruction lorsque les éléments sont supprimés à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="9511d-109">You have proof of disposition when the items are deleted at the end of their retention period.</span></span>

<span data-ttu-id="9511d-110">Vous utilisez les [étiquettes de rétention](retention.md#retention-labels) pour marquer du contenu sous la forme d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9511d-110">You use [retention labels](retention.md#retention-labels) to mark content as a record.</span></span> <span data-ttu-id="9511d-111">Vous pouvez soit publier ces étiquettes pour permettre aux utilisateurs et aux administrateurs de les appliquer manuellement au contenu, soit appliquer automatiquement ces étiquettes au contenu que vous voulez marquer comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9511d-111">You can either publish those labels so that users and administrators can manually apply them to content, or auto-apply those labels to content that you want to mark as a record.</span></span>

<span data-ttu-id="9511d-112">En utilisant des étiquettes de rétention pour marquer du contenu en tant qu’enregistrement, vous pouvez implémenter une stratégie de gestion des enregistrements unique et cohérente dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9511d-112">By using retention labels to mark content as records, you can implement a single and consistent strategy for managing records across your Microsoft 365 environment.</span></span>

## <a name="compare-restrictions-for-what-actions-are-allowed-or-blocked"></a><span data-ttu-id="9511d-113">Comparer des restrictions relatives aux actions autorisées ou bloquées</span><span class="sxs-lookup"><span data-stu-id="9511d-113">Compare restrictions for what actions are allowed or blocked</span></span>

<span data-ttu-id="9511d-114">Utilisez le tableau suivant pour identifier les restrictions placées sur du contenu suite à l’application d’une étiquette de rétention standard, ainsi que les étiquettes de rétention qui marquent du contenu en tant qu’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9511d-114">Use the following table to identify what restrictions are placed on content as a result of applying a standard retention label, and retention labels that mark content as a record.</span></span> 

<span data-ttu-id="9511d-115">Une étiquette de rétention standard a la configuration de conservation des données sans marquer le contenu comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9511d-115">A standard retention label has the configuration to retain data without marking content as a record.</span></span>

>[!NOTE] 
> <span data-ttu-id="9511d-116">Pour couvrir tous les cas de figure, le tableau inclut les colonnes d’un enregistrement verrouillé et déverrouillé, applicable à SharePoint et OneDrive, mais pas à Exchange.</span><span class="sxs-lookup"><span data-stu-id="9511d-116">For completeness, the table includes columns for a locked and unlocked record, which is applicable to SharePoint and OneDrive, but not Exchange.</span></span> <span data-ttu-id="9511d-117">La possibilité de verrouiller et de déverrouiller un enregistrement utilise le [contrôle de version](record-versioning.md) qui n’est pas pris en charge pour les éléments Exchange.</span><span class="sxs-lookup"><span data-stu-id="9511d-117">The ability to lock and unlock a record uses [record versioning](record-versioning.md) that isn't supported for Exchange items.</span></span> <span data-ttu-id="9511d-118">Par conséquent, pour tous les éléments Exchange marqués en tant qu’enregistrement, le comportement mappe vers l’**Enregistrement – colonne verrouillée**, et l’**Enregistrement – colonne déverrouillée** n’est pas pertinent.</span><span class="sxs-lookup"><span data-stu-id="9511d-118">So for all Exchange items that are marked as a record, the behavior maps to the **Record - locked** column, and the **Record - unlocked column** is not relevant.</span></span>


|<span data-ttu-id="9511d-119">Action</span><span class="sxs-lookup"><span data-stu-id="9511d-119">Action</span></span>| <span data-ttu-id="9511d-120">Étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="9511d-120">Retention label</span></span> |<span data-ttu-id="9511d-121">Enregistrement – colonne verrouillée</span><span class="sxs-lookup"><span data-stu-id="9511d-121">Record - locked</span></span>| <span data-ttu-id="9511d-122">Enregistrement – colonne déverrouillée</span><span class="sxs-lookup"><span data-stu-id="9511d-122">Record - unlocked</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9511d-123">Modifier les contenus</span><span class="sxs-lookup"><span data-stu-id="9511d-123">Edit contents</span></span>|<span data-ttu-id="9511d-124">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-124">Allowed</span></span> | <span data-ttu-id="9511d-125">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="9511d-125">**Blocked**</span></span> | <span data-ttu-id="9511d-126">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-126">Allowed</span></span>|
|<span data-ttu-id="9511d-127">Modifier les propriétés, y compris Renommer</span><span class="sxs-lookup"><span data-stu-id="9511d-127">Edit properties, including rename</span></span>|<span data-ttu-id="9511d-128">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-128">Allowed</span></span> |<span data-ttu-id="9511d-129">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-129">Allowed</span></span> | <span data-ttu-id="9511d-130">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-130">Allowed</span></span>|
|<span data-ttu-id="9511d-131">Supprimer</span><span class="sxs-lookup"><span data-stu-id="9511d-131">Delete</span></span>|<span data-ttu-id="9511d-132"><sup>1</sup> autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-132">Allowed <sup>1</sup></span></span> |<span data-ttu-id="9511d-133">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="9511d-133">**Blocked**</span></span> | <span data-ttu-id="9511d-134">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="9511d-134">**Blocked**</span></span>|
|<span data-ttu-id="9511d-135">Copier</span><span class="sxs-lookup"><span data-stu-id="9511d-135">Copy</span></span>|<span data-ttu-id="9511d-136">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-136">Allowed</span></span> |<span data-ttu-id="9511d-137">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-137">Allowed</span></span> | <span data-ttu-id="9511d-138">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-138">Allowed</span></span>|
|<span data-ttu-id="9511d-139">Se déplacer au sein du conteneur <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="9511d-139">Move within container <sup>2</sup></span></span>|<span data-ttu-id="9511d-140">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-140">Allowed</span></span> |<span data-ttu-id="9511d-141">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-141">Allowed</span></span> | <span data-ttu-id="9511d-142">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-142">Allowed</span></span>|
|<span data-ttu-id="9511d-143">Se déplacer dans les conteneurs <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="9511d-143">Move across containers <sup>2</sup></span></span>|<span data-ttu-id="9511d-144">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-144">Allowed</span></span> |<span data-ttu-id="9511d-145">Autorisé si jamais déverrouillé</span><span class="sxs-lookup"><span data-stu-id="9511d-145">Allowed if never unlocked</span></span> | <span data-ttu-id="9511d-146">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-146">Allowed</span></span>|
|<span data-ttu-id="9511d-147">Ouvert/lu</span><span class="sxs-lookup"><span data-stu-id="9511d-147">Open/Read</span></span>|<span data-ttu-id="9511d-148">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-148">Allowed</span></span> |<span data-ttu-id="9511d-149">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-149">Allowed</span></span> | <span data-ttu-id="9511d-150">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-150">Allowed</span></span>|
|<span data-ttu-id="9511d-151">Modifier l’étiquette</span><span class="sxs-lookup"><span data-stu-id="9511d-151">Change label</span></span>|<span data-ttu-id="9511d-152">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-152">Allowed</span></span> |<span data-ttu-id="9511d-153">Autorisé – administrateur de conteneur uniquement</span><span class="sxs-lookup"><span data-stu-id="9511d-153">Allowed - container admin only</span></span> | <span data-ttu-id="9511d-154">Autorisé – administrateur de conteneur uniquement</span><span class="sxs-lookup"><span data-stu-id="9511d-154">Allowed - container admin only</span></span>|
|<span data-ttu-id="9511d-155">Supprimer l’étiquette</span><span class="sxs-lookup"><span data-stu-id="9511d-155">Remove label</span></span>|<span data-ttu-id="9511d-156">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9511d-156">Allowed</span></span> |<span data-ttu-id="9511d-157">Autorisé – administrateur de conteneur uniquement</span><span class="sxs-lookup"><span data-stu-id="9511d-157">Allowed - container admin only</span></span> | <span data-ttu-id="9511d-158">Autorisé – administrateur de conteneur uniquement</span><span class="sxs-lookup"><span data-stu-id="9511d-158">Allowed - container admin only</span></span>|

<span data-ttu-id="9511d-159">Notes de bas de page :</span><span class="sxs-lookup"><span data-stu-id="9511d-159">Footnotes:</span></span>

<span data-ttu-id="9511d-160"><sup>1</sup> Prise en charge par OneDrive et Exchange en conservant une copie dans un emplacement sécurisé, mais bloqué par SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9511d-160"><sup>1</sup> Supported by OneDrive and Exchange by retaining a copy in a secured location, but blocked by SharePoint.</span></span>

<span data-ttu-id="9511d-161">Message qu’un utilisateur voit s’il essaie de supprimer un document étiqueté dans SharePoint :</span><span class="sxs-lookup"><span data-stu-id="9511d-161">Message a user sees if they try to delete a labeled document in SharePoint:</span></span>

![Message indiquant que l’élément n’a pas été supprimé dans SharePoint](../media/d0020726-1593-4a96-b07c-89b275e75c49.png)


<span data-ttu-id="9511d-163"><sup>2</sup> Les conteneurs incluent les bibliothèques de documents SharePoint et les boîtes aux lettres Exchange.</span><span class="sxs-lookup"><span data-stu-id="9511d-163"><sup>2</sup> Containers include SharePoint document libraries and Exchange mailboxes.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9511d-164">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9511d-164">Next steps</span></span>

<span data-ttu-id="9511d-165">Si vous n’avez pas encore d’étiquettes de rétention à utiliser pour la gestion des enregistrements, consultez [Prise en main des stratégies et des étiquettes de rétention](get-started-with-retention.md).</span><span class="sxs-lookup"><span data-stu-id="9511d-165">If you don't yet have retention labels to use for records management, see [Get started with retention policies and retention labels](get-started-with-retention.md).</span></span>

<span data-ttu-id="9511d-166">Pour marquer du contenu en tant qu’enregistrement, consultez [Déclarer des enregistrements à l’aide d’étiquettes de rétention](declare-records.md).</span><span class="sxs-lookup"><span data-stu-id="9511d-166">To mark content as a record, see [Declare records by using retention labels](declare-records.md).</span></span>
