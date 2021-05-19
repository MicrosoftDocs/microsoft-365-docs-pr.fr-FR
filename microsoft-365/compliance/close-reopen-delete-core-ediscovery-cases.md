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
ms.openlocfilehash: 8a54d5c8f93d36351538bc235a6dbeaaa602c3e9
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52532445"
---
# <a name="close-reopen-and-delete-a-core-ediscovery-case"></a><span data-ttu-id="d24a7-104">Fermer, rouvrir et supprimer un cas core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d24a7-104">Close, reopen, and delete a Core eDiscovery case</span></span>

<span data-ttu-id="d24a7-105">Cet article explique comment fermer, rouvrir et supprimer des cas eDiscovery principaux Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d24a7-105">This article describes how to close, reopen, and delete Core eDiscovery cases in Microsoft 365.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="d24a7-106">Fermer un cas</span><span class="sxs-lookup"><span data-stu-id="d24a7-106">Close a case</span></span>

<span data-ttu-id="d24a7-107">Lorsque le dossier juridique ou l’examen pris en charge par un cas eDiscovery principal est terminé, vous pouvez fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="d24a7-107">When the legal case or investigation supported by a Core eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="d24a7-108">Voici ce qui se produit lorsque vous fermez un cas :</span><span class="sxs-lookup"><span data-stu-id="d24a7-108">Here's what happens when you close a case:</span></span>
  
- <span data-ttu-id="d24a7-109">Si le cas contient des cas de découverte électronique, ils sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="d24a7-109">If the case contains any eDiscovery holds, they will be turned off.</span></span> <span data-ttu-id="d24a7-110">Une fois la attente désactivée, une période de grâce de 30 jours (appelée attente différée) est appliquée aux emplacements de contenu qui étaient en attente.</span><span class="sxs-lookup"><span data-stu-id="d24a7-110">After the hold is turned off, a 30-day grace period (called a *delay hold*) is applied to content locations that were on hold.</span></span> <span data-ttu-id="d24a7-111">Cela permet d’empêcher la suppression immédiate du contenu et offre aux administrateurs la possibilité de rechercher et de restaurer du contenu avant qu’il ne soit définitivement supprimé après l’expiration de la période d’attente.</span><span class="sxs-lookup"><span data-stu-id="d24a7-111">This helps prevent content from being immediately deleted and provides admins the opportunity to search for and restore content before it may be permanently deleted after the delay hold period expires.</span></span> <span data-ttu-id="d24a7-112">Pour plus d’informations, voir [Suppression d’emplacements de contenu d’une attente eDiscovery.](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold)</span><span class="sxs-lookup"><span data-stu-id="d24a7-112">For more information, see [Removing content locations from an eDiscovery hold](create-ediscovery-holds.md#removing-content-locations-from-an-ediscovery-hold).</span></span>

- <span data-ttu-id="d24a7-113">La fermeture d’un cas désactive uniquement les conservations associées à ce cas.</span><span class="sxs-lookup"><span data-stu-id="d24a7-113">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="d24a7-114">Si d’autres conservations sont placées sur un emplacement de contenu (par exemple, une conservation pour litige, une stratégie de rétention ou une conservation à partir d’un autre cas core eDiscovery), ces conservations sont conservées.</span><span class="sxs-lookup"><span data-stu-id="d24a7-114">If other holds are placed on a content location (such as a Litigation Hold, a retention policy, or a hold from a different Core eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="d24a7-115">Le cas est toujours répertorié sur la page Core eDiscovery dans le centre Microsoft 365 conformité.</span><span class="sxs-lookup"><span data-stu-id="d24a7-115">The case is still listed on the Core eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="d24a7-116">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="d24a7-116">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="d24a7-117">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="d24a7-117">You can edit a case after it's closed.</span></span> <span data-ttu-id="d24a7-118">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches et exporter des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="d24a7-118">For example, you can add or remove members, create searches, and export search results.</span></span> <span data-ttu-id="d24a7-119">La principale différence entre les cas actifs et fermés est que les cas de découverte électronique sont désactivés lorsqu’un cas est fermé.</span><span class="sxs-lookup"><span data-stu-id="d24a7-119">The primary difference between active and closed cases is that eDiscovery holds are turned off when a case is closed.</span></span>

<span data-ttu-id="d24a7-120">Pour fermer un cas :</span><span class="sxs-lookup"><span data-stu-id="d24a7-120">To close a case:</span></span>
  
1. <span data-ttu-id="d24a7-121">Dans le centre Microsoft 365 conformité, cliquez sur **eDiscovery** Core pour afficher la liste des cas  >   eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d24a7-121">In the Microsoft 365 compliance center, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="d24a7-122">Cliquez sur le nom du cas que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="d24a7-122">Click the name of the case that you want to close.</span></span>

   ![Fermer le cas sur la page d’accueil du cas](../media/eDiscoveryCaseHomePage.png)

3. <span data-ttu-id="d24a7-124">Dans la page d’accueil, sous **État,** cliquez **sur Fermer le cas.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-124">On the home page, under **Status**, click **Close case**.</span></span>

    <span data-ttu-id="d24a7-125">Un avertissement s’affiche et vous avertit que les mises en cause associées au cas seront désactivées.</span><span class="sxs-lookup"><span data-stu-id="d24a7-125">A warning is displayed saying that the holds associated with the case will be turned off.</span></span>

4. <span data-ttu-id="d24a7-126">Cliquez **sur Oui** pour fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="d24a7-126">Click **Yes** to close the case.</span></span>

    <span data-ttu-id="d24a7-127">L’état de la page d’accueil du cas passe de **Actif** à **Fermeture.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-127">The status on the case home page is changed from **Active** to **Closing**.</span></span>

5. <span data-ttu-id="d24a7-128">Dans la page **Core eDiscovery,** cliquez sur **Actualiser** pour mettre à jour l’état du cas fermé.</span><span class="sxs-lookup"><span data-stu-id="d24a7-128">On the **Core eDiscovery** page, click **Refresh** to update the status of the closed case.</span></span> <span data-ttu-id="d24a7-129">L’exécution du processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="d24a7-129">It might take up to 60 minutes for the closing process to complete.</span></span>

    <span data-ttu-id="d24a7-130">Une fois le processus terminé, l’état du cas passe à **Fermé** sur la page **Core eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-130">When the process is complete, the status of the case is changed to **Closed** on the **Core eDiscovery** page.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="d24a7-131">Rouvrir un cas fermé</span><span class="sxs-lookup"><span data-stu-id="d24a7-131">Reopen a closed case</span></span>

<span data-ttu-id="d24a7-132">Lorsque vous rouvrez un cas, les cas de découverte électronique mis en place lors de la fermeture ne sont pas automatiquement rétablis.</span><span class="sxs-lookup"><span data-stu-id="d24a7-132">When you reopen a case, any eDiscovery holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="d24a7-133">Une fois le cas rouvert, vous devez vous rendre sur la page **Dentes** et activer les précédentes.</span><span class="sxs-lookup"><span data-stu-id="d24a7-133">After the case is reopened, you'll have to go to the **Holds** page and turn on the previous holds.</span></span> <span data-ttu-id="d24a7-134">Pour activer une conservation, sélectionnez-la pour afficher la page de menu volant, puis réglez la bascule **État** sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="d24a7-134">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>
  
1. <span data-ttu-id="d24a7-135">Dans le centre Microsoft 365 conformité, cliquez sur **eDiscovery** Core pour afficher la liste des cas  >   eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d24a7-135">In the Microsoft 365 compliance center, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="d24a7-136">Cliquez sur le nom du cas que vous souhaitez rouvrir.</span><span class="sxs-lookup"><span data-stu-id="d24a7-136">Click the name of the case that you want to reopen.</span></span>

   ![Rouvrir un cas fermé](../media/eDiscoveryCaseHomePageReopen.png)

3. <span data-ttu-id="d24a7-138">Dans la page d’accueil, sous **État,** cliquez **sur Rouvrir le cas.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-138">On the home page, under **Status**, click **Reopen case**.</span></span>

    <span data-ttu-id="d24a7-139">Un avertissement s’affiche pour vous dire que les mises en place associées au cas lors de sa fermeture ne seront pas automatiquement allumées.</span><span class="sxs-lookup"><span data-stu-id="d24a7-139">A warning is displayed saying that the holds that were associated with the case when it was closed won't be turned on automatically.</span></span>

4. <span data-ttu-id="d24a7-140">Cliquez **sur Oui** pour rouvrir le cas.</span><span class="sxs-lookup"><span data-stu-id="d24a7-140">Click **Yes** to reopen the case.</span></span>

    <span data-ttu-id="d24a7-141">L’état de la page volante de la page d’accueil du cas passe de **Fermé** à **Actif.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-141">The status on the case home page flyout page is changed from **Closed** to **Active**.</span></span>

5. <span data-ttu-id="d24a7-142">Dans la page **Core eDiscovery,** cliquez sur **Actualiser** pour mettre à jour l’état du cas rouvert.</span><span class="sxs-lookup"><span data-stu-id="d24a7-142">On the **Core eDiscovery** page, click **Refresh** to update the status of the reopened case.</span></span> <span data-ttu-id="d24a7-143">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="d24a7-143">It might take up to 60 minutes for the reopening process to complete.</span></span> 

    <span data-ttu-id="d24a7-144">Une fois le processus terminé, l’état du cas passe à **Actif** sur la page **Core eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-144">When the process is complete, the status of the case is changed to **Active** on the **Core eDiscovery** page.</span></span>

6. <span data-ttu-id="d24a7-145">(Facultatif) Pour activer les attentes associées au  cas rouvert, sélectionnez l’onglet Attentes, sélectionnez une attente, puis cochez la case sous État sur la page de la boîte aux lettres de la boîte aux lettres. </span><span class="sxs-lookup"><span data-stu-id="d24a7-145">(Optional) To turn on any holds associated with the reopened case, go to **Holds** tab, select a hold, and then select the checkbox under **Status** on the hold flyout page.</span></span>
  
## <a name="delete-a-case"></a><span data-ttu-id="d24a7-146">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="d24a7-146">Delete a case</span></span>

<span data-ttu-id="d24a7-147">Vous pouvez également supprimer des cas eDiscovery principaux et fermés.</span><span class="sxs-lookup"><span data-stu-id="d24a7-147">You can also delete active and closed Core eDiscovery cases.</span></span> <span data-ttu-id="d24a7-148">Lorsque vous supprimez un cas, toutes les recherches et exportations dans le cas sont supprimées et le cas est supprimé de la liste des cas sur la page **eDiscovery** principale dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d24a7-148">When you delete a case, all searches and exports in the case are deleted, and the case is removed from the list of cases on the **Core eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="d24a7-149">Vous ne pouvez pas rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="d24a7-149">You can't reopen a deleted case.</span></span>

<span data-ttu-id="d24a7-150">Avant de supprimer un cas (qu’il soit actif  ou fermé), vous devez d’abord supprimer toutes les actualités eDiscovery associées au cas.</span><span class="sxs-lookup"><span data-stu-id="d24a7-150">Before you can delete a case (whether it's active or closed), you must first delete *all* eDiscovery holds associated with the case.</span></span> <span data-ttu-id="d24a7-151">Cela inclut la suppression des maintiens avec l’état **« Off**».</span><span class="sxs-lookup"><span data-stu-id="d24a7-151">That includes deleting holds with a status of **Off**.</span></span> 

<span data-ttu-id="d24a7-152">Pour supprimer une attente eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="d24a7-152">To delete an eDiscovery hold:</span></span>

1. <span data-ttu-id="d24a7-153">Go the **Holds** tab in the case that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="d24a7-153">Go the **Holds** tab in the case that you want to delete.</span></span>

2. <span data-ttu-id="d24a7-154">Sélectionnez la attente à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d24a7-154">Select the hold that you want to delete.</span></span>

3. <span data-ttu-id="d24a7-155">Dans la page volante, cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-155">On the flyout page, click **Delete**.</span></span>

      ![Supprimer une attente eDiscovery](../media/DeleteeDiscoveryHold.png)

<span data-ttu-id="d24a7-157">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="d24a7-157">To delete a case:</span></span>

1. <span data-ttu-id="d24a7-158">Dans le centre Microsoft 365 conformité, cliquez sur **eDiscovery** Core pour afficher la liste des cas  >   eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d24a7-158">In the Microsoft 365 compliance center, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="d24a7-159">Cliquez sur le nom du cas à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d24a7-159">Click the name of the case that you want to delete.</span></span>

3. <span data-ttu-id="d24a7-160">Dans la page d’accueil du cas, sous **État,** cliquez **sur Supprimer le cas.**</span><span class="sxs-lookup"><span data-stu-id="d24a7-160">On the case home page, under **Status**, click **Delete case**.</span></span>

      ![Supprimer un cas](../media/eDiscoveryCaseHomePageDelete.png)

<span data-ttu-id="d24a7-162">Si le cas que vous essayez de supprimer contient toujours des conserves eDiscovery, vous recevrez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d24a7-162">If the case you're trying to delete still contains eDiscovery holds, you'll receive an error message.</span></span> <span data-ttu-id="d24a7-163">Vous devez supprimer toutes les réserves associées au cas, puis essayer à nouveau de supprimer le cas.</span><span class="sxs-lookup"><span data-stu-id="d24a7-163">You'll have to delete all holds associated with the case and then try again to delete the case.</span></span>
