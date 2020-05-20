---
title: Fermer ou supprimer un cas
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Découvrez ce qui se passe lorsqu’une enquête ou une casse légale prise en charge par un cas avancé eDiscovery est fermée ou supprimée.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: e64f5cc0483129396a28cbf657778001e5d372a7
ms.sourcegitcommit: 261d51b90a9ad53a6a42348c414b1b1e1230c37f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "44292410"
---
# <a name="close-or-delete-an-advanced-ediscovery-case"></a><span data-ttu-id="8e81a-103">Fermer ou supprimer un cas avancé eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8e81a-103">Close or delete an Advanced eDiscovery case</span></span>

<span data-ttu-id="8e81a-104">Lorsque le cas juridique ou l’enquête pris en charge par un cas avancé eDiscovery est terminé, vous pouvez fermer ou supprimer un incident.</span><span class="sxs-lookup"><span data-stu-id="8e81a-104">When the legal case or investigation supported by an Advanced eDiscovery case is completed, you can close or delete a case.</span></span> <span data-ttu-id="8e81a-105">Vous pouvez également rouvrir un cas fermé.</span><span class="sxs-lookup"><span data-stu-id="8e81a-105">You can also reopen a closed case.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="8e81a-106">Fermer un incident</span><span class="sxs-lookup"><span data-stu-id="8e81a-106">Close a case</span></span>

<span data-ttu-id="8e81a-107">Voici ce qui se passe lorsque vous fermez un cas avancé de découverte électronique :</span><span class="sxs-lookup"><span data-stu-id="8e81a-107">Here's what happens when you close an Advanced eDiscovery case:</span></span>

- <span data-ttu-id="8e81a-108">Si le cas contient des emplacements de contenu en conservation, ceux-ci sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="8e81a-108">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="8e81a-109">Cela peut entraîner la suppression ou le vidage définitifs du contenu, soit par l’utilisateur, soit par un processus automatisé, tel qu’une stratégie de suppression.</span><span class="sxs-lookup"><span data-stu-id="8e81a-109">This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>

- <span data-ttu-id="8e81a-110">La fermeture d’un incident ne désactive que les blocages associés à ce cas.</span><span class="sxs-lookup"><span data-stu-id="8e81a-110">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="8e81a-111">Si d’autres suspensions sont placées sur un emplacement de contenu (comme une conservation pour litige, la conservation de découverte électronique principale ou une suspension d’un autre cas de découverte électronique avancée), ces conservations seront toujours conservées.</span><span class="sxs-lookup"><span data-stu-id="8e81a-111">If other holds are place on a content location (such as a Litigation Hold, Core eDiscovery hold, or a hold from a different Advanced eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="8e81a-112">Le cas est toujours mentionné sur la page eDiscovery dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8e81a-112">The case is still listed on the eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="8e81a-113">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="8e81a-113">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="8e81a-114">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="8e81a-114">You can edit a case after it's closed.</span></span> <span data-ttu-id="8e81a-115">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="8e81a-115">For example, you can add or removing members, create searches, export search results, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="8e81a-116">La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lors de la fermeture d’un cas.</span><span class="sxs-lookup"><span data-stu-id="8e81a-116">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="8e81a-117">Pour fermer un incident :</span><span class="sxs-lookup"><span data-stu-id="8e81a-117">To close a case:</span></span>

1. <span data-ttu-id="8e81a-118">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="8e81a-118">On the **Advanced eDiscovery** page, select the case that you want to close.</span></span>

2. <span data-ttu-id="8e81a-119">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-119">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="8e81a-120">Cliquez sur **Fermer le cas**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-120">Click **Close case**.</span></span>

   <span data-ttu-id="8e81a-121">Le processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="8e81a-121">It might take up to 60 minutes for the closing process to complete.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="8e81a-122">Rouvrir un litige clos</span><span class="sxs-lookup"><span data-stu-id="8e81a-122">Reopen a closed case</span></span>

<span data-ttu-id="8e81a-123">Lorsque vous rouvrez un cas avancé eDiscovery, les conservations qui étaient en place lors de la fermeture de l’incident ne sont pas automatiquement rétablis.</span><span class="sxs-lookup"><span data-stu-id="8e81a-123">When you reopen an Advanced eDiscovery case, any holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="8e81a-124">Une fois le cas rouvert, vous devez accéder à l’onglet **suspensions** et activer les suspensions précédentes.</span><span class="sxs-lookup"><span data-stu-id="8e81a-124">After the case is reopened, you'll have to go to the **Holds** tab and turn on the previous holds.</span></span> <span data-ttu-id="8e81a-125">Pour activer une suspension, sélectionnez-la pour afficher la page de menu volant, puis définissez la bascule d' **État** sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-125">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>

<span data-ttu-id="8e81a-126">Pour rouvrir un cas fermé :</span><span class="sxs-lookup"><span data-stu-id="8e81a-126">To reopen a closed case:</span></span>

1. <span data-ttu-id="8e81a-127">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="8e81a-127">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="8e81a-128">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-128">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="8e81a-129">Cliquez sur **rouvrir la demande de devis**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-129">Click **Reopen case**.</span></span>

   <span data-ttu-id="8e81a-130">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="8e81a-130">It might take up to 60 minutes for the reopening process to complete.</span></span>

## <a name="delete-a-case"></a><span data-ttu-id="8e81a-131">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="8e81a-131">Delete a case</span></span>

<span data-ttu-id="8e81a-132">Vous pouvez supprimer à la fois des cas de découverte électronique avancée et active.</span><span class="sxs-lookup"><span data-stu-id="8e81a-132">You can delete both active and closed Advanced eDiscovery cases.</span></span> <span data-ttu-id="8e81a-133">Lorsque vous supprimez un incident, tous les composants associés à celui-ci, tels que la liste des dépositaires, les communications, les recherches, les ensembles de révision et les tâches d’exportation, sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="8e81a-133">When you delete a case, all components associated with the case, such as the list of custodians, communications, searches, review sets, and export job are deleted.</span></span> <span data-ttu-id="8e81a-134">Le cas est supprimé de la liste des incidents de la page **Advanced eDiscovery** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8e81a-134">The case is removed from the list of cases on the **Advanced eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="8e81a-135">Vous ne pouvez pas récupérer ou rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="8e81a-135">You can't recover or reopen a deleted case.</span></span>

> [!NOTE]
> <span data-ttu-id="8e81a-136">Dans les scénarios de fuite de données, la seule façon de supprimer des éléments dans un jeu de révision est de supprimer le cas avancé de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="8e81a-136">In data spillage scenarios, the only way to remove items in a review set is to delete the Advanced eDiscovery case.</span></span> <span data-ttu-id="8e81a-137">Les autres méthodes « recherche et purge » ne suppriment pas les éléments d’un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="8e81a-137">Other "search and purge" methods don't remove items from a review set.</span></span>

<span data-ttu-id="8e81a-138">Avant de pouvoir supprimer un incident (qu’il soit actif ou fermé), vous devez d’abord supprimer *toutes les* conservations associées au cas.</span><span class="sxs-lookup"><span data-stu-id="8e81a-138">Before you can delete a case (whether it's active or closed), you must first delete *all* holds associated with the case.</span></span> <span data-ttu-id="8e81a-139">Cela inclut la suppression des blocages dont l’État est **off**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-139">That includes deleting holds with a status of **Off**.</span></span>

<span data-ttu-id="8e81a-140">Pour supprimer les conservations associées à un cas :</span><span class="sxs-lookup"><span data-stu-id="8e81a-140">To delete holds associated with a case:</span></span>

1. <span data-ttu-id="8e81a-141">Accédez à l’onglet **suspensions** dans le cas eDiscovery avancé que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="8e81a-141">Go the **Holds** tab in the Advanced eDiscovery case that you want to delete.</span></span>

2. <span data-ttu-id="8e81a-142">Cliquez sur la conservation que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="8e81a-142">Click the hold that you want to delete.</span></span>

3. <span data-ttu-id="8e81a-143">Sur la page de la fenêtre volante, cliquez sur **Supprimer la conservation**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-143">On the flyout page, click **Delete hold**.</span></span>

<span data-ttu-id="8e81a-144">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="8e81a-144">To delete a case:</span></span>

1. <span data-ttu-id="8e81a-145">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="8e81a-145">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="8e81a-146">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-146">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="8e81a-147">Cliquez sur **supprimer le cas**.</span><span class="sxs-lookup"><span data-stu-id="8e81a-147">Click **Delete case**.</span></span>
