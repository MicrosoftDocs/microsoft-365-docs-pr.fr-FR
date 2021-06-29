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
description: Découvrez ce qui se produit lorsqu’un examen ou un dossier juridique pris en charge par un Advanced eDiscovery est fermé ou supprimé.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: efbcbe34e6d7d8b564bcfa0cf9bbd8a1fbb59709
ms.sourcegitcommit: 6749455c52b0f98a92f6fffbc2bb86caf3538bd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53194627"
---
# <a name="close-or-delete-an-advanced-ediscovery-case"></a><span data-ttu-id="31fa6-103">Fermer ou supprimer un cas Advanced eDiscovery dossier</span><span class="sxs-lookup"><span data-stu-id="31fa6-103">Close or delete an Advanced eDiscovery case</span></span>

<span data-ttu-id="31fa6-104">Lorsque le dossier juridique ou l’examen pris en charge par un Advanced eDiscovery est terminé, vous pouvez fermer ou supprimer un cas.</span><span class="sxs-lookup"><span data-stu-id="31fa6-104">When the legal case or investigation supported by an Advanced eDiscovery case is completed, you can close or delete a case.</span></span> <span data-ttu-id="31fa6-105">Vous pouvez également rouvrir un cas fermé.</span><span class="sxs-lookup"><span data-stu-id="31fa6-105">You can also reopen a closed case.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="31fa6-106">Fermer un cas</span><span class="sxs-lookup"><span data-stu-id="31fa6-106">Close a case</span></span>

<span data-ttu-id="31fa6-107">Voici ce qui se produit lorsque vous fermez Advanced eDiscovery cas :</span><span class="sxs-lookup"><span data-stu-id="31fa6-107">Here's what happens when you close an Advanced eDiscovery case:</span></span>

- <span data-ttu-id="31fa6-108">Si le cas contient des emplacements de contenu en attente, ces conservations sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="31fa6-108">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="31fa6-109">Une fois la attente désactivée, une période de grâce de 30 jours (appelée attente différée) est appliquée aux emplacements de contenu qui étaient en attente.</span><span class="sxs-lookup"><span data-stu-id="31fa6-109">After the hold is turned off, a 30-day grace period (called a *delay hold*) is applied to content locations that were on hold.</span></span> <span data-ttu-id="31fa6-110">Cela permet d’empêcher la suppression immédiate du contenu et donne aux administrateurs la possibilité de rechercher ou de récupérer du contenu qui sera définitivement supprimé après l’expiration de la période de retard.</span><span class="sxs-lookup"><span data-stu-id="31fa6-110">This helps prevent content from being immediately deleted and gives admins an opportunity to search for or recover content that will be permanently deleted after the delay hold period expires.</span></span> <span data-ttu-id="31fa6-111">Pour plus d’informations, voir [Suppression d’emplacements de contenu d’une attente eDiscovery.](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold)</span><span class="sxs-lookup"><span data-stu-id="31fa6-111">For more information, see [Removing content locations from an eDiscovery hold](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold).</span></span>

- <span data-ttu-id="31fa6-112">La fermeture d’un cas désactive uniquement les conservations associées à ce cas.</span><span class="sxs-lookup"><span data-stu-id="31fa6-112">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="31fa6-113">Si d’autres sont conservées sur un emplacement de contenu (par exemple, une attente pour litige, une découverte électronique principale ou une attente d’un autre cas de Advanced eDiscovery), celles-ci sont conservées.</span><span class="sxs-lookup"><span data-stu-id="31fa6-113">If other holds are place on a content location (such as a Litigation Hold, Core eDiscovery hold, or a hold from a different Advanced eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="31fa6-114">Le cas est toujours répertorié sur la page eDiscovery dans la Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="31fa6-114">The case is still listed on the eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="31fa6-115">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="31fa6-115">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="31fa6-116">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="31fa6-116">You can edit a case after it's closed.</span></span> <span data-ttu-id="31fa6-117">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="31fa6-117">For example, you can add or removing members, create searches, export search results, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="31fa6-118">La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lorsqu’un cas est fermé.</span><span class="sxs-lookup"><span data-stu-id="31fa6-118">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="31fa6-119">Pour fermer un cas :</span><span class="sxs-lookup"><span data-stu-id="31fa6-119">To close a case:</span></span>

1. <span data-ttu-id="31fa6-120">Dans la page **Advanced eDiscovery**, sélectionnez le cas que vous voulez fermer.</span><span class="sxs-lookup"><span data-stu-id="31fa6-120">On the **Advanced eDiscovery** page, select the case that you want to close.</span></span>

2. <span data-ttu-id="31fa6-121">Sous l’onglet **Paramètres**, sous **Informations de cas**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="31fa6-121">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

   ![Accéder à la page de flyout des informations de cas dans Advanced eDiscovery cas](..\media\AeDSelectCaseInformation.png) 

3. <span data-ttu-id="31fa6-123">En bas de la page volant **Informations** sur la cas, cliquez sur **Actions,** puis cliquez sur **Fermer le cas.**</span><span class="sxs-lookup"><span data-stu-id="31fa6-123">At the bottom of the **Case Information** flyout page, click **Actions**, and then click **Close case**.</span></span>

   <span data-ttu-id="31fa6-124">L’exécution du processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="31fa6-124">It might take up to 60 minutes for the closing process to complete.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="31fa6-125">Rouvrir un cas fermé</span><span class="sxs-lookup"><span data-stu-id="31fa6-125">Reopen a closed case</span></span>

<span data-ttu-id="31fa6-126">Lorsque vous rouvrez un Advanced eDiscovery, les cas de non-remise en vigueur lors de la fermeture du cas ne sont pas automatiquement rétablis.</span><span class="sxs-lookup"><span data-stu-id="31fa6-126">When you reopen an Advanced eDiscovery case, any holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="31fa6-127">Une fois le cas rouvert, vous devez passer à l’onglet **Holds** et activer les précédentes.</span><span class="sxs-lookup"><span data-stu-id="31fa6-127">After the case is reopened, you'll have to go to the **Holds** tab and turn on the previous holds.</span></span> <span data-ttu-id="31fa6-128">Pour activer une conservation, sélectionnez-la pour afficher la page de menu volant, puis réglez la bascule **État** sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="31fa6-128">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>

<span data-ttu-id="31fa6-129">Pour rouvrir un cas fermé :</span><span class="sxs-lookup"><span data-stu-id="31fa6-129">To reopen a closed case:</span></span>

1. <span data-ttu-id="31fa6-130">Dans la page **Advanced eDiscovery**, sélectionnez le cas que vous voulez rouvrir.</span><span class="sxs-lookup"><span data-stu-id="31fa6-130">On the **Advanced eDiscovery** page, select the case that you want to reopen.</span></span>

2. <span data-ttu-id="31fa6-131">Sous l’onglet **Paramètres**, sous **Informations de cas**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="31fa6-131">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="31fa6-132">Au bas de la page volant **Informations** sur la cas, cliquez sur **Actions,** puis cliquez sur **Rouvrir le cas.**</span><span class="sxs-lookup"><span data-stu-id="31fa6-132">At the bottom of the **Case Information** flyout page, click **Actions**, and then click **Reopen case**.</span></span>

   <span data-ttu-id="31fa6-133">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="31fa6-133">It might take up to 60 minutes for the reopening process to complete.</span></span>

## <a name="delete-a-case"></a><span data-ttu-id="31fa6-134">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="31fa6-134">Delete a case</span></span>

<span data-ttu-id="31fa6-135">Vous pouvez supprimer les cas d’Advanced eDiscovery actifs et fermés.</span><span class="sxs-lookup"><span data-stu-id="31fa6-135">You can delete both active and closed Advanced eDiscovery cases.</span></span> <span data-ttu-id="31fa6-136">Lorsque vous supprimez un cas, tous les composants associés au cas, tels que la liste des consignataires, communications, recherches, ensembles de révision et tâche d’exportation sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="31fa6-136">When you delete a case, all components associated with the case, such as the list of custodians, communications, searches, review sets, and export job are deleted.</span></span> <span data-ttu-id="31fa6-137">Le cas est supprimé de la liste des cas sur la page **Advanced eDiscovery** dans la Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="31fa6-137">The case is removed from the list of cases on the **Advanced eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="31fa6-138">Vous ne pouvez pas récupérer ou rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="31fa6-138">You can't recover or reopen a deleted case.</span></span>

> [!NOTE]
> <span data-ttu-id="31fa6-139">Dans les scénarios de débordement de données, la seule façon de supprimer des éléments d’un jeu à réviser consiste à supprimer Advanced eDiscovery cas.</span><span class="sxs-lookup"><span data-stu-id="31fa6-139">In data spillage scenarios, the only way to remove items in a review set is to delete the Advanced eDiscovery case.</span></span> <span data-ttu-id="31fa6-140">Les autres méthodes de « recherche et purge » ne suppriment pas les éléments d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="31fa6-140">Other "search and purge" methods don't remove items from a review set.</span></span>

<span data-ttu-id="31fa6-141">Avant de pouvoir supprimer un cas (qu’il soit  actif ou fermé), vous devez d’abord supprimer toutes les ententes associées au cas.</span><span class="sxs-lookup"><span data-stu-id="31fa6-141">Before you can delete a case (whether it's active or closed), you must first delete *all* holds associated with the case.</span></span> <span data-ttu-id="31fa6-142">Cela inclut la suppression des maintiens avec l’état **« Off**».</span><span class="sxs-lookup"><span data-stu-id="31fa6-142">That includes deleting holds with a status of **Off**.</span></span>

<span data-ttu-id="31fa6-143">Pour supprimer les cas associés à un cas :</span><span class="sxs-lookup"><span data-stu-id="31fa6-143">To delete holds associated with a case:</span></span>

1. <span data-ttu-id="31fa6-144">Dans le **cas où** vous Advanced eDiscovery supprimer, Advanced eDiscovery l’onglet Contient.</span><span class="sxs-lookup"><span data-stu-id="31fa6-144">Go the **Holds** tab in the Advanced eDiscovery case that you want to delete.</span></span>

2. <span data-ttu-id="31fa6-145">Cliquez sur la attente à supprimer.</span><span class="sxs-lookup"><span data-stu-id="31fa6-145">Click the hold that you want to delete.</span></span>

3. <span data-ttu-id="31fa6-146">Dans la page volante, cliquez **sur Supprimer la attente.**</span><span class="sxs-lookup"><span data-stu-id="31fa6-146">On the flyout page, click **Delete hold**.</span></span>

<span data-ttu-id="31fa6-147">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="31fa6-147">To delete a case:</span></span>

1. <span data-ttu-id="31fa6-148">Dans la page **Advanced eDiscovery**, sélectionnez le cas que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="31fa6-148">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="31fa6-149">Sous l’onglet **Paramètres**, sous **Informations de cas**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="31fa6-149">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="31fa6-150">En bas de la page volant **Informations** sur la cas, cliquez sur **Actions,** puis cliquez **sur Supprimer le cas.**</span><span class="sxs-lookup"><span data-stu-id="31fa6-150">At the bottom of the **Case Information** flyout page, click **Actions**, and then click **Delete case**.</span></span>

