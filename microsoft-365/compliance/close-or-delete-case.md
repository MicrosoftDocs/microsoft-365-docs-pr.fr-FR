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
ms.openlocfilehash: 7b11faa2ccdb44fca916b2f602d5120adadf1739
ms.sourcegitcommit: 4f6ef4cd09c3ed36dc0be3702b0636bad6cff8a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/26/2021
ms.locfileid: "52657638"
---
# <a name="close-or-delete-an-advanced-ediscovery-case"></a><span data-ttu-id="ab506-103">Fermer ou supprimer un cas Advanced eDiscovery dossier</span><span class="sxs-lookup"><span data-stu-id="ab506-103">Close or delete an Advanced eDiscovery case</span></span>

<span data-ttu-id="ab506-104">Lorsque le dossier juridique ou l’examen pris en charge par un Advanced eDiscovery est terminé, vous pouvez fermer ou supprimer un cas.</span><span class="sxs-lookup"><span data-stu-id="ab506-104">When the legal case or investigation supported by an Advanced eDiscovery case is completed, you can close or delete a case.</span></span> <span data-ttu-id="ab506-105">Vous pouvez également rouvrir un cas fermé.</span><span class="sxs-lookup"><span data-stu-id="ab506-105">You can also reopen a closed case.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="ab506-106">Fermer un cas</span><span class="sxs-lookup"><span data-stu-id="ab506-106">Close a case</span></span>

<span data-ttu-id="ab506-107">Voici ce qui se produit lorsque vous fermez Advanced eDiscovery cas :</span><span class="sxs-lookup"><span data-stu-id="ab506-107">Here's what happens when you close an Advanced eDiscovery case:</span></span>

- <span data-ttu-id="ab506-108">Si le cas contient des emplacements de contenu en attente, ces conservations sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="ab506-108">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="ab506-109">Une fois la période d’attente désactivée, une période de grâce de 30 jours (appelée attente différée) est appliquée aux emplacements de contenu qui étaient en attente.</span><span class="sxs-lookup"><span data-stu-id="ab506-109">After the hold is turned off, a 30-day grace period (called a *delay hold*) is applied to content locations that were on hold.</span></span> <span data-ttu-id="ab506-110">Cela permet d’empêcher la suppression immédiate du contenu et donne aux administrateurs la possibilité de rechercher ou de récupérer du contenu qui sera définitivement supprimé après l’expiration de la période de retard.</span><span class="sxs-lookup"><span data-stu-id="ab506-110">This helps prevent content from being immediately deleted and gives admins an opportunity to search for or recover content that will be permanently deleted after the delay hold period expires.</span></span> <span data-ttu-id="ab506-111">Pour plus d’informations, voir [Suppression d’emplacements de contenu d’une attente eDiscovery.](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold)</span><span class="sxs-lookup"><span data-stu-id="ab506-111">For more information, see [Removing content locations from an eDiscovery hold](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold).</span></span>

- <span data-ttu-id="ab506-112">La fermeture d’un cas désactive uniquement les conservations associées à ce cas.</span><span class="sxs-lookup"><span data-stu-id="ab506-112">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="ab506-113">Si d’autres sont conservées sur un emplacement de contenu (par exemple, une attente pour litige, une découverte électronique principale ou une attente d’un autre cas de Advanced eDiscovery), celles-ci sont conservées.</span><span class="sxs-lookup"><span data-stu-id="ab506-113">If other holds are place on a content location (such as a Litigation Hold, Core eDiscovery hold, or a hold from a different Advanced eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="ab506-114">Le cas est toujours répertorié sur la page eDiscovery dans le centre Microsoft 365 conformité.</span><span class="sxs-lookup"><span data-stu-id="ab506-114">The case is still listed on the eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ab506-115">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="ab506-115">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="ab506-116">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="ab506-116">You can edit a case after it's closed.</span></span> <span data-ttu-id="ab506-117">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="ab506-117">For example, you can add or removing members, create searches, export search results, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="ab506-118">La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lorsqu’un cas est fermé.</span><span class="sxs-lookup"><span data-stu-id="ab506-118">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="ab506-119">Pour fermer un cas :</span><span class="sxs-lookup"><span data-stu-id="ab506-119">To close a case:</span></span>

1. <span data-ttu-id="ab506-120">Dans la page **Advanced eDiscovery**, sélectionnez le cas que vous voulez fermer.</span><span class="sxs-lookup"><span data-stu-id="ab506-120">On the **Advanced eDiscovery** page, select the case that you want to close.</span></span>

2. <span data-ttu-id="ab506-121">Sous l’onglet **Paramètres**, sous **Informations de cas**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ab506-121">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="ab506-122">En bas de la page volant **Informations** sur la cas, cliquez sur (**...**) **Plus d’options,** puis cliquez sur **Fermer le cas**.</span><span class="sxs-lookup"><span data-stu-id="ab506-122">At the bottom of the **Case Information** flyout page, click (**...**) **More options**, and then click **Close case**.</span></span>

   ![Option du menu Plus d’options pour fermer Advanced eDiscovery cas](..\Media\CloseAdvancedeDiscoveryCase.png)

   <span data-ttu-id="ab506-124">L’exécution du processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="ab506-124">It might take up to 60 minutes for the closing process to complete.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="ab506-125">Rouvrir un cas fermé</span><span class="sxs-lookup"><span data-stu-id="ab506-125">Reopen a closed case</span></span>

<span data-ttu-id="ab506-126">Lorsque vous rouvrez un Advanced eDiscovery, les cas de non-remise en vigueur lors de la fermeture du cas ne sont pas rétablis automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ab506-126">When you reopen an Advanced eDiscovery case, any holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="ab506-127">Une fois le cas rouvert, vous devez passer à l’onglet **Holds** et activer les précédentes.</span><span class="sxs-lookup"><span data-stu-id="ab506-127">After the case is reopened, you'll have to go to the **Holds** tab and turn on the previous holds.</span></span> <span data-ttu-id="ab506-128">Pour activer une conservation, sélectionnez-la pour afficher la page de menu volant, puis réglez la bascule **État** sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="ab506-128">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>

<span data-ttu-id="ab506-129">Pour rouvrir un cas fermé :</span><span class="sxs-lookup"><span data-stu-id="ab506-129">To reopen a closed case:</span></span>

1. <span data-ttu-id="ab506-130">Dans la page **Advanced eDiscovery**, sélectionnez le cas que vous voulez rouvrir.</span><span class="sxs-lookup"><span data-stu-id="ab506-130">On the **Advanced eDiscovery** page, select the case that you want to reopen.</span></span>

2. <span data-ttu-id="ab506-131">Sous l’onglet **Paramètres**, sous **Informations de cas**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ab506-131">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="ab506-132">En bas de la page volant **Informations** sur la cas, cliquez sur (**...**) **Plus d’options,** puis cliquez sur **Rouvrir le cas.**</span><span class="sxs-lookup"><span data-stu-id="ab506-132">At the bottom of the **Case Information** flyout page, click (**...**) **More options**, and then click **Reopen case**.</span></span>

   ![Option du menu Plus d’options pour rouvrir un cas Advanced eDiscovery dossier](..\Media\ReopenAdvancedeDiscoveryCase.png)

   <span data-ttu-id="ab506-134">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="ab506-134">It might take up to 60 minutes for the reopening process to complete.</span></span>

## <a name="delete-a-case"></a><span data-ttu-id="ab506-135">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="ab506-135">Delete a case</span></span>

<span data-ttu-id="ab506-136">Vous pouvez supprimer les cas d’Advanced eDiscovery actifs et fermés.</span><span class="sxs-lookup"><span data-stu-id="ab506-136">You can delete both active and closed Advanced eDiscovery cases.</span></span> <span data-ttu-id="ab506-137">Lorsque vous supprimez un cas, tous les composants associés au cas, tels que la liste des consignataires, communications, recherches, ensembles de révision et tâche d’exportation sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="ab506-137">When you delete a case, all components associated with the case, such as the list of custodians, communications, searches, review sets, and export job are deleted.</span></span> <span data-ttu-id="ab506-138">Le cas est supprimé de la liste des cas sur la page **Advanced eDiscovery** dans le centre Microsoft 365 conformité.</span><span class="sxs-lookup"><span data-stu-id="ab506-138">The case is removed from the list of cases on the **Advanced eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ab506-139">Vous ne pouvez pas récupérer ou rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="ab506-139">You can't recover or reopen a deleted case.</span></span>

> [!NOTE]
> <span data-ttu-id="ab506-140">Dans les scénarios de débordement de données, la seule façon de supprimer des éléments d’un jeu à réviser consiste à supprimer Advanced eDiscovery cas.</span><span class="sxs-lookup"><span data-stu-id="ab506-140">In data spillage scenarios, the only way to remove items in a review set is to delete the Advanced eDiscovery case.</span></span> <span data-ttu-id="ab506-141">Les autres méthodes de « recherche et purge » ne suppriment pas les éléments d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="ab506-141">Other "search and purge" methods don't remove items from a review set.</span></span>

<span data-ttu-id="ab506-142">Avant de pouvoir supprimer un cas (qu’il soit  actif ou fermé), vous devez d’abord supprimer toutes les ententes associées au cas.</span><span class="sxs-lookup"><span data-stu-id="ab506-142">Before you can delete a case (whether it's active or closed), you must first delete *all* holds associated with the case.</span></span> <span data-ttu-id="ab506-143">Cela inclut la suppression des maintiens avec l’état **« Off**».</span><span class="sxs-lookup"><span data-stu-id="ab506-143">That includes deleting holds with a status of **Off**.</span></span>

<span data-ttu-id="ab506-144">Pour supprimer les cas associés à un cas :</span><span class="sxs-lookup"><span data-stu-id="ab506-144">To delete holds associated with a case:</span></span>

1. <span data-ttu-id="ab506-145">Dans le **cas où** vous Advanced eDiscovery supprimer, Advanced eDiscovery l’onglet Contient.</span><span class="sxs-lookup"><span data-stu-id="ab506-145">Go the **Holds** tab in the Advanced eDiscovery case that you want to delete.</span></span>

2. <span data-ttu-id="ab506-146">Cliquez sur la attente à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ab506-146">Click the hold that you want to delete.</span></span>

3. <span data-ttu-id="ab506-147">Dans la page volante, cliquez sur **Supprimer la attente.**</span><span class="sxs-lookup"><span data-stu-id="ab506-147">On the flyout page, click **Delete hold**.</span></span>

<span data-ttu-id="ab506-148">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="ab506-148">To delete a case:</span></span>

1. <span data-ttu-id="ab506-149">Dans la page **Advanced eDiscovery**, sélectionnez le cas que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="ab506-149">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="ab506-150">Sous l’onglet **Paramètres**, sous **Informations de cas**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ab506-150">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="ab506-151">En bas de la page volant **Informations** sur la cas, cliquez sur (**...**) **Plus d’options,** puis cliquez sur **Supprimer le cas**.</span><span class="sxs-lookup"><span data-stu-id="ab506-151">At the bottom of the **Case Information** flyout page, click (**...**) **More options**, and then click **Delete case**.</span></span>

   ![Option du menu Plus d’options pour supprimer Advanced eDiscovery cas](..\Media\DeleteAdvancedeDiscoveryCase.png)
