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
ms.openlocfilehash: be8d133a8215fc40c6d33025f9f4d1dee0f3b609
ms.sourcegitcommit: 5c96d06496d40d2523edbea336f7355c3c77cc80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "44412783"
---
# <a name="close-or-delete-an-advanced-ediscovery-case"></a><span data-ttu-id="2d5a5-103">Fermer ou supprimer un cas avancé eDiscovery</span><span class="sxs-lookup"><span data-stu-id="2d5a5-103">Close or delete an Advanced eDiscovery case</span></span>

<span data-ttu-id="2d5a5-104">Lorsque le cas juridique ou l’enquête pris en charge par un cas avancé eDiscovery est terminé, vous pouvez fermer ou supprimer un incident.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-104">When the legal case or investigation supported by an Advanced eDiscovery case is completed, you can close or delete a case.</span></span> <span data-ttu-id="2d5a5-105">Vous pouvez également rouvrir un cas fermé.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-105">You can also reopen a closed case.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="2d5a5-106">Fermer un incident</span><span class="sxs-lookup"><span data-stu-id="2d5a5-106">Close a case</span></span>

<span data-ttu-id="2d5a5-107">Voici ce qui se passe lorsque vous fermez un cas avancé de découverte électronique :</span><span class="sxs-lookup"><span data-stu-id="2d5a5-107">Here's what happens when you close an Advanced eDiscovery case:</span></span>

- <span data-ttu-id="2d5a5-108">Si le cas contient des emplacements de contenu en conservation, ceux-ci sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-108">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="2d5a5-109">Une fois la conservation désactivée, une période de grâce de 30 jours (appelée *conservation différée*) est appliquée aux emplacements de contenu en attente.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-109">After the hold is turned off, a 30-day grace period (called a *delay hold*) is applied to content locations that were on hold.</span></span> <span data-ttu-id="2d5a5-110">Cela permet d’empêcher la suppression immédiate du contenu et donne aux administrateurs la possibilité de rechercher ou de récupérer du contenu qui sera définitivement supprimé après l’expiration de la période de blocage.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-110">This helps prevent content from being immediately deleted and gives admins an opportunity to search for or recover content that will be permanently deleted after the delay hold period expires.</span></span> <span data-ttu-id="2d5a5-111">Pour plus d’informations, consultez la rubrique [suppression des emplacements de contenu d’une conservation eDiscovery](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold).</span><span class="sxs-lookup"><span data-stu-id="2d5a5-111">For more information, see [Removing content locations from an eDiscovery hold](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold).</span></span>

- <span data-ttu-id="2d5a5-112">La fermeture d’un incident ne désactive que les blocages associés à ce cas.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-112">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="2d5a5-113">Si d’autres suspensions sont placées sur un emplacement de contenu (comme une conservation pour litige, la conservation de découverte électronique principale ou une suspension d’un autre cas de découverte électronique avancée), ces conservations seront toujours conservées.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-113">If other holds are place on a content location (such as a Litigation Hold, Core eDiscovery hold, or a hold from a different Advanced eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="2d5a5-114">Le cas est toujours mentionné sur la page eDiscovery dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-114">The case is still listed on the eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="2d5a5-115">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-115">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="2d5a5-116">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-116">You can edit a case after it's closed.</span></span> <span data-ttu-id="2d5a5-117">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-117">For example, you can add or removing members, create searches, export search results, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="2d5a5-118">La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lors de la fermeture d’un cas.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-118">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="2d5a5-119">Pour fermer un incident :</span><span class="sxs-lookup"><span data-stu-id="2d5a5-119">To close a case:</span></span>

1. <span data-ttu-id="2d5a5-120">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-120">On the **Advanced eDiscovery** page, select the case that you want to close.</span></span>

2. <span data-ttu-id="2d5a5-121">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-121">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="2d5a5-122">Cliquez sur **Fermer le cas**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-122">Click **Close case**.</span></span>

   <span data-ttu-id="2d5a5-123">Le processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-123">It might take up to 60 minutes for the closing process to complete.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="2d5a5-124">Rouvrir un litige clos</span><span class="sxs-lookup"><span data-stu-id="2d5a5-124">Reopen a closed case</span></span>

<span data-ttu-id="2d5a5-125">Lorsque vous rouvrez un cas avancé eDiscovery, les conservations qui étaient en place lors de la fermeture de l’incident ne sont pas automatiquement rétablis.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-125">When you reopen an Advanced eDiscovery case, any holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="2d5a5-126">Une fois le cas rouvert, vous devez accéder à l’onglet **suspensions** et activer les suspensions précédentes.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-126">After the case is reopened, you'll have to go to the **Holds** tab and turn on the previous holds.</span></span> <span data-ttu-id="2d5a5-127">Pour activer une suspension, sélectionnez-la pour afficher la page de menu volant, puis définissez la bascule d' **État** sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-127">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>

<span data-ttu-id="2d5a5-128">Pour rouvrir un cas fermé :</span><span class="sxs-lookup"><span data-stu-id="2d5a5-128">To reopen a closed case:</span></span>

1. <span data-ttu-id="2d5a5-129">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-129">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="2d5a5-130">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-130">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="2d5a5-131">Cliquez sur **rouvrir la demande de devis**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-131">Click **Reopen case**.</span></span>

   <span data-ttu-id="2d5a5-132">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-132">It might take up to 60 minutes for the reopening process to complete.</span></span>

## <a name="delete-a-case"></a><span data-ttu-id="2d5a5-133">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="2d5a5-133">Delete a case</span></span>

<span data-ttu-id="2d5a5-134">Vous pouvez supprimer à la fois des cas de découverte électronique avancée et active.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-134">You can delete both active and closed Advanced eDiscovery cases.</span></span> <span data-ttu-id="2d5a5-135">Lorsque vous supprimez un incident, tous les composants associés à celui-ci, tels que la liste des dépositaires, les communications, les recherches, les ensembles de révision et les tâches d’exportation, sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-135">When you delete a case, all components associated with the case, such as the list of custodians, communications, searches, review sets, and export job are deleted.</span></span> <span data-ttu-id="2d5a5-136">Le cas est supprimé de la liste des incidents de la page **Advanced eDiscovery** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-136">The case is removed from the list of cases on the **Advanced eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="2d5a5-137">Vous ne pouvez pas récupérer ou rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-137">You can't recover or reopen a deleted case.</span></span>

> [!NOTE]
> <span data-ttu-id="2d5a5-138">Dans les scénarios de fuite de données, la seule façon de supprimer des éléments dans un jeu de révision est de supprimer le cas avancé de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-138">In data spillage scenarios, the only way to remove items in a review set is to delete the Advanced eDiscovery case.</span></span> <span data-ttu-id="2d5a5-139">Les autres méthodes « recherche et purge » ne suppriment pas les éléments d’un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-139">Other "search and purge" methods don't remove items from a review set.</span></span>

<span data-ttu-id="2d5a5-140">Avant de pouvoir supprimer un incident (qu’il soit actif ou fermé), vous devez d’abord supprimer *toutes les* conservations associées au cas.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-140">Before you can delete a case (whether it's active or closed), you must first delete *all* holds associated with the case.</span></span> <span data-ttu-id="2d5a5-141">Cela inclut la suppression des blocages dont l’État est **off**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-141">That includes deleting holds with a status of **Off**.</span></span>

<span data-ttu-id="2d5a5-142">Pour supprimer les conservations associées à un cas :</span><span class="sxs-lookup"><span data-stu-id="2d5a5-142">To delete holds associated with a case:</span></span>

1. <span data-ttu-id="2d5a5-143">Accédez à l’onglet **suspensions** dans le cas eDiscovery avancé que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-143">Go the **Holds** tab in the Advanced eDiscovery case that you want to delete.</span></span>

2. <span data-ttu-id="2d5a5-144">Cliquez sur la conservation que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-144">Click the hold that you want to delete.</span></span>

3. <span data-ttu-id="2d5a5-145">Sur la page de la fenêtre volante, cliquez sur **Supprimer la conservation**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-145">On the flyout page, click **Delete hold**.</span></span>

<span data-ttu-id="2d5a5-146">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="2d5a5-146">To delete a case:</span></span>

1. <span data-ttu-id="2d5a5-147">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-147">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="2d5a5-148">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-148">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="2d5a5-149">Cliquez sur **supprimer le cas**.</span><span class="sxs-lookup"><span data-stu-id="2d5a5-149">Click **Delete case**.</span></span>
