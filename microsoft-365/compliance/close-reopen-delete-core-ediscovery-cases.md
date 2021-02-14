---
title: Fermer, rouvrir et supprimer des cas eDiscovery principaux
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Cet article explique comment gérer les cas eDiscovery principaux. Cela inclut la fermeture d’un cas, la réouverture d’un cas fermé et la suppression d’un cas.
ms.openlocfilehash: 17b243a7207fd6927188b42e585101ff1d258b76
ms.sourcegitcommit: 5c96d06496d40d2523edbea336f7355c3c77cc80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "44412793"
---
# <a name="close-reopen-and-delete-a-core-ediscovery-case"></a><span data-ttu-id="0842b-104">Fermer, rouvrir et supprimer un cas core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0842b-104">Close, reopen, and delete a Core eDiscovery case</span></span>

<span data-ttu-id="0842b-105">Cet article explique comment fermer, rouvrir et supprimer des cas eDiscovery principaux dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0842b-105">This article describes how to close, reopen, and delete Core eDiscovery cases in Microsoft 365.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="0842b-106">Fermer un cas</span><span class="sxs-lookup"><span data-stu-id="0842b-106">Close a case</span></span>

<span data-ttu-id="0842b-107">Lorsque le dossier juridique ou l’examen pris en charge par un cas eDiscovery principal est terminé, vous pouvez fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="0842b-107">When the legal case or investigation supported by a Core eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="0842b-108">Voici ce qui se produit lorsque vous fermez un cas :</span><span class="sxs-lookup"><span data-stu-id="0842b-108">Here's what happens when you close a case:</span></span>
  
- <span data-ttu-id="0842b-109">Si le cas contient des emplacements de contenu en attente eDiscovery, ces derniers sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="0842b-109">If the case contains any content locations on eDiscovery hold, those holds will be turned off.</span></span> <span data-ttu-id="0842b-110">Une fois la attente désactivée, une période de grâce de 30 jours (appelée attente différée) est appliquée aux emplacements de contenu qui étaient en attente.</span><span class="sxs-lookup"><span data-stu-id="0842b-110">After the hold is turned off, a 30-day grace period (called a *delay hold*) is applied to content locations that were on hold.</span></span> <span data-ttu-id="0842b-111">Cela permet d’empêcher la suppression immédiate du contenu et offre aux administrateurs la possibilité de rechercher et de restaurer du contenu avant qu’il ne soit définitivement supprimé après l’expiration de la période d’attente.</span><span class="sxs-lookup"><span data-stu-id="0842b-111">This helps prevent content from being immediately deleted and provides admins the opportunity to search for and restore content before it may be permanently deleted after the delay hold period expires.</span></span> <span data-ttu-id="0842b-112">Pour plus d’informations, voir [Suppression d’emplacements de contenu d’une attente eDiscovery.](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold)</span><span class="sxs-lookup"><span data-stu-id="0842b-112">For more information, see [Removing content locations from an eDiscovery hold](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold).</span></span>

- <span data-ttu-id="0842b-113">La fermeture d’un cas désactive uniquement les conservations associées à ce cas.</span><span class="sxs-lookup"><span data-stu-id="0842b-113">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="0842b-114">Si d’autres conservations sont placées sur un emplacement de contenu (par exemple, une conservation pour litige, une stratégie de rétention ou une conservation à partir d’un autre cas core eDiscovery), ces conservations seront conservées.</span><span class="sxs-lookup"><span data-stu-id="0842b-114">If other holds are placed on a content location (such as a Litigation Hold, a retention policy, or a hold from a different Core eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="0842b-115">Le cas est toujours répertorié sur la page Core eDiscovery dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0842b-115">The case is still listed on the Core eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="0842b-116">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="0842b-116">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="0842b-117">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="0842b-117">You can edit a case after it's closed.</span></span> <span data-ttu-id="0842b-118">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches et exporter des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="0842b-118">For example, you can add or removing members, create searches, and export search results.</span></span> <span data-ttu-id="0842b-119">La principale différence entre les cas actifs et fermés est que les cas de découverte électronique sont désactivés lorsqu’un cas est fermé.</span><span class="sxs-lookup"><span data-stu-id="0842b-119">The primary difference between active and closed cases is that eDiscovery holds are turned off when a case is closed.</span></span>

<span data-ttu-id="0842b-120">Pour fermer un cas :</span><span class="sxs-lookup"><span data-stu-id="0842b-120">To close a case:</span></span>
  
1. <span data-ttu-id="0842b-121">Dans le Centre de conformité Microsoft 365, cliquez sur **eDiscovery** Core pour afficher la liste des cas  >   eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0842b-121">In the Microsoft 365 compliance center, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="0842b-122">Cliquez sur le nom du cas que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="0842b-122">Click the name of the case that you want to close.</span></span>

    <span data-ttu-id="0842b-123">La page de présentation Gérer **ce** cas s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0842b-123">The **Manage this case** flyout page is displayed.</span></span>

3. <span data-ttu-id="0842b-124">Sous **Gérer l’état du cas,** cliquez **sur Fermer le cas.**</span><span class="sxs-lookup"><span data-stu-id="0842b-124">Under **Manage case status**, click **Close case**.</span></span>

    <span data-ttu-id="0842b-125">Un avertissement s’affiche et vous avertit que les mises en cause associées au cas seront désactivées.</span><span class="sxs-lookup"><span data-stu-id="0842b-125">A warning is displayed saying that the holds associated with the case will be turned off.</span></span>

4. <span data-ttu-id="0842b-126">Cliquez **sur Oui** pour fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="0842b-126">Click **Yes** to close the case.</span></span>

    <span data-ttu-id="0842b-127">L’état sur la page de gestion **de** ce dossier volant est modifié de **Actif** à **Fermeture.**</span><span class="sxs-lookup"><span data-stu-id="0842b-127">The status on the **Manage this case** flyout page is changed from **Active** to **Closing**.</span></span>

5. <span data-ttu-id="0842b-128">Fermez la page **Gérer ce cas.**</span><span class="sxs-lookup"><span data-stu-id="0842b-128">Close the **Manage this case** page.</span></span>

6. <span data-ttu-id="0842b-129">Dans la page **Core eDiscovery,** cliquez sur **Actualiser** pour mettre à jour l’état du cas fermé.</span><span class="sxs-lookup"><span data-stu-id="0842b-129">On the **Core eDiscovery** page, click **Refresh** to update the status of the closed case.</span></span> <span data-ttu-id="0842b-130">L’exécution du processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="0842b-130">It might take up to 60 minutes for the closing process to complete.</span></span>

    <span data-ttu-id="0842b-131">Une fois le processus terminé, l’état du cas passe à **Fermé** sur la page **Core eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="0842b-131">When the process is complete, the status of the case is changed to **Closed** on the **Core eDiscovery** page.</span></span> <span data-ttu-id="0842b-132">Cliquez à nouveau sur le  nom du cas pour afficher la page de présentation Gérer ce cas, qui contient des informations sur le moment où le cas a été fermé et qui l’a fermé.</span><span class="sxs-lookup"><span data-stu-id="0842b-132">Click the name of the case again to display the **Manage this case** flyout page, which contains information about when the case was closed and who closed it.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="0842b-133">Rouvrir un cas fermé</span><span class="sxs-lookup"><span data-stu-id="0842b-133">Reopen a closed case</span></span>

<span data-ttu-id="0842b-134">Lorsque vous rouvrez un cas, les cas de découverte électronique mis en place lors de la fermeture ne sont pas automatiquement rétablis.</span><span class="sxs-lookup"><span data-stu-id="0842b-134">When you reopen a case, any eDiscovery holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="0842b-135">Une fois le cas rouvert, vous devez vous rendre sur la page **Dentes** et activer les précédentes.</span><span class="sxs-lookup"><span data-stu-id="0842b-135">After the case is reopened, you'll have to go to the **Holds** page and turn on the previous holds.</span></span> <span data-ttu-id="0842b-136">Pour activer une conservation, sélectionnez-la pour afficher la page de menu volant, puis réglez la bascule **État** sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="0842b-136">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>
  
1. <span data-ttu-id="0842b-137">Dans le Centre de conformité Microsoft 365, cliquez sur **eDiscovery** Core pour afficher la liste des cas  >   eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0842b-137">In the Microsoft 365 compliance center, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="0842b-138">Cliquez sur le nom du cas que vous souhaitez rouvrir.</span><span class="sxs-lookup"><span data-stu-id="0842b-138">Click the name of the case that you want to reopen.</span></span>

    <span data-ttu-id="0842b-139">La page de présentation Gérer **ce** cas s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0842b-139">The **Manage this case** flyout page is displayed.</span></span> 

3. <span data-ttu-id="0842b-140">Sous **Gérer l’état du cas,** cliquez **sur Rouvrir le cas.**</span><span class="sxs-lookup"><span data-stu-id="0842b-140">Under **Manage case status**, click **Reopen case**.</span></span>

    <span data-ttu-id="0842b-141">Un avertissement s’affiche pour vous dire que les mises en place associées au cas lors de sa fermeture ne seront pas automatiquement allumées.</span><span class="sxs-lookup"><span data-stu-id="0842b-141">A warning is displayed saying that the holds that were associated with the case when it was closed won't be turned on automatically.</span></span>

4. <span data-ttu-id="0842b-142">Cliquez **sur Oui** pour rouvrir le cas.</span><span class="sxs-lookup"><span data-stu-id="0842b-142">Click **Yes** to reopen the case.</span></span>

    <span data-ttu-id="0842b-143">L’état de la page De gestion **de** ce volant de cas passe de **Fermé** à **Actif.**</span><span class="sxs-lookup"><span data-stu-id="0842b-143">The status on the **Manage this case** flyout page is changed from **Closed** to **Active**.</span></span>

5. <span data-ttu-id="0842b-144">Fermez la page **Gérer ce cas.**</span><span class="sxs-lookup"><span data-stu-id="0842b-144">Close the **Manage this case** page.</span></span> 

6. <span data-ttu-id="0842b-145">Dans la page **Core eDiscovery,** cliquez sur **Actualiser** pour mettre à jour l’état du cas rouvert.</span><span class="sxs-lookup"><span data-stu-id="0842b-145">On the **Core eDiscovery** page, click **Refresh** to update the status of the reopened case.</span></span> <span data-ttu-id="0842b-146">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="0842b-146">It might take up to 60 minutes for the reopening process to complete.</span></span> 

    <span data-ttu-id="0842b-147">Une fois le processus terminé, l’état du cas passe à **Actif** sur la page **Core eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="0842b-147">When the process is complete, the status of the case is changed to **Active** on the **Core eDiscovery** page.</span></span> 
  
## <a name="delete-a-case"></a><span data-ttu-id="0842b-148">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="0842b-148">Delete a case</span></span>

<span data-ttu-id="0842b-149">Vous pouvez également supprimer des cas eDiscovery principaux et fermés.</span><span class="sxs-lookup"><span data-stu-id="0842b-149">You can also delete active and closed Core eDiscovery cases.</span></span> <span data-ttu-id="0842b-150">Lorsque vous supprimez un cas, toutes les recherches et exportations dans le cas sont supprimées et le cas est supprimé de la liste des cas sur la page **eDiscovery** principale dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0842b-150">When you delete a case, all searches and exports in the case are deleted, and the case is removed from the list of cases on the **Core eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="0842b-151">Vous ne pouvez pas rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="0842b-151">You can't reopen a deleted case.</span></span>

<span data-ttu-id="0842b-152">Avant de pouvoir supprimer un cas (qu’il soit  actif ou fermé), vous devez d’abord supprimer toutes les données eDiscovery associées au cas.</span><span class="sxs-lookup"><span data-stu-id="0842b-152">Before you can delete a case (whether it's active or closed), you must first delete *all* eDiscovery holds associated with the case.</span></span> <span data-ttu-id="0842b-153">Cela inclut la suppression des maintiens avec l’état **« Off**».</span><span class="sxs-lookup"><span data-stu-id="0842b-153">That includes deleting holds with a status of **Off**.</span></span> 

<span data-ttu-id="0842b-154">Pour supprimer une attente eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="0842b-154">To delete an eDiscovery hold:</span></span>

1. <span data-ttu-id="0842b-155">Go the **Holds** tab in the case that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="0842b-155">Go the **Holds** tab in the case that you want to delete.</span></span>

2. <span data-ttu-id="0842b-156">Cliquez sur la attente à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0842b-156">Click the hold that you want to delete.</span></span>

3. <span data-ttu-id="0842b-157">Dans la page volante, cliquez **sur Supprimer la attente.**</span><span class="sxs-lookup"><span data-stu-id="0842b-157">On the flyout page, click **Delete hold**.</span></span>

<span data-ttu-id="0842b-158">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="0842b-158">To delete a case:</span></span>

1. <span data-ttu-id="0842b-159">Dans le Centre de conformité Microsoft 365, cliquez sur **eDiscovery** Core pour afficher la liste des cas  >   eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0842b-159">In the Microsoft 365 compliance center, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="0842b-160">Cliquez sur le nom du cas à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0842b-160">Click the name of the case that you want to delete.</span></span>

3. <span data-ttu-id="0842b-161">Sous **Gérer l’état des cas** dans la page volante, cliquez sur Supprimer le **cas.**</span><span class="sxs-lookup"><span data-stu-id="0842b-161">Under **Manage case status** on the flyout page, click **Delete case**.</span></span>

<span data-ttu-id="0842b-162">Si le cas que vous essayez de supprimer contient toujours des conserves eDiscovery, vous recevrez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0842b-162">If the case you're trying to delete still contains eDiscovery holds, you'll receive an error message.</span></span> <span data-ttu-id="0842b-163">Vous devez supprimer toutes les réserves associées au cas, puis essayer à nouveau de supprimer le cas.</span><span class="sxs-lookup"><span data-stu-id="0842b-163">You'll have to delete all holds associated with the case and then try again to delete the case.</span></span>
