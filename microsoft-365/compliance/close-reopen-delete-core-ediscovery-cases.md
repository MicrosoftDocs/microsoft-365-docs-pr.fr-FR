---
title: Fermer, rouvrir et supprimer des cas de découverte électronique principaux
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
description: Cet article explique comment gérer les cas de découverte électronique principaux. Cela inclut la fermeture d’un cas, la réouverture d’un incident fermé et la suppression d’un cas.
ms.openlocfilehash: 41ba622a58b0abb5ce668e6d94d89b1694a328c9
ms.sourcegitcommit: bd51f626f0c7788c2a3cf89deee25264659aebd5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "43551389"
---
# <a name="close-reopen-and-delete-a-core-ediscovery-case"></a><span data-ttu-id="ce66e-104">Fermer, rouvrir et supprimer un cas de découverte électronique principale</span><span class="sxs-lookup"><span data-stu-id="ce66e-104">Close, reopen, and delete a Core eDiscovery case</span></span>

<span data-ttu-id="ce66e-105">Cet article explique comment fermer, rouvrir et supprimer des cas de découverte électronique principaux dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ce66e-105">This article describes how to close, reopen, and delete Core eDiscovery cases in Microsoft 365.</span></span>

## <a name="close-a-case"></a><span data-ttu-id="ce66e-106">Fermer un incident</span><span class="sxs-lookup"><span data-stu-id="ce66e-106">Close a case</span></span>

<span data-ttu-id="ce66e-107">Lorsque le cas juridique ou l’enquête pris en charge par un cas de découverte électronique de base est terminé, vous pouvez fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="ce66e-107">When the legal case or investigation supported by a Core eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="ce66e-108">Voici ce qui se passe lorsque vous fermez un cas :</span><span class="sxs-lookup"><span data-stu-id="ce66e-108">Here's what happens when you close a case:</span></span>
  
- <span data-ttu-id="ce66e-109">Si le cas contient des emplacements de contenu sur le blocage de la découverte électronique, ces conservations seront désactivées.</span><span class="sxs-lookup"><span data-stu-id="ce66e-109">If the case contains any content locations on eDiscovery hold, those holds will be turned off.</span></span> <span data-ttu-id="ce66e-110">Cela peut entraîner la suppression ou le vidage définitifs du contenu, soit par l’utilisateur, soit par un processus automatisé, tel qu’une stratégie de suppression.</span><span class="sxs-lookup"><span data-stu-id="ce66e-110">This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>

- <span data-ttu-id="ce66e-111">La fermeture d’un incident ne désactive que les blocages associés à ce cas.</span><span class="sxs-lookup"><span data-stu-id="ce66e-111">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="ce66e-112">Si d’autres suspensions sont placées sur un emplacement de contenu (comme une suspension pour litige, une stratégie de rétention ou une conservation d’un autre cas de découverte électronique de base), ces conservations seront conservées.</span><span class="sxs-lookup"><span data-stu-id="ce66e-112">If other holds are placed on a content location (such as a Litigation Hold, a retention policy, or a hold from a different Core eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="ce66e-113">Le cas est toujours mentionné sur la page de découverte électronique principale dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ce66e-113">The case is still listed on the Core eDiscovery page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ce66e-114">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="ce66e-114">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="ce66e-115">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="ce66e-115">You can edit a case after it's closed.</span></span> <span data-ttu-id="ce66e-116">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches et exporter des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="ce66e-116">For example, you can add or removing members, create searches, and export search results.</span></span> <span data-ttu-id="ce66e-117">La principale différence entre les cas actifs et fermés est que les conservations eDiscovery sont désactivées lors de la fermeture d’un cas.</span><span class="sxs-lookup"><span data-stu-id="ce66e-117">The primary difference between active and closed cases is that eDiscovery holds are turned off when a case is closed.</span></span>

<span data-ttu-id="ce66e-118">Pour fermer un incident :</span><span class="sxs-lookup"><span data-stu-id="ce66e-118">To close a case:</span></span>
  
1. <span data-ttu-id="ce66e-119">Dans l’entrée de conformité Microsoft 365, cliquez sur**Centre** de **découverte électronique** > pour afficher la liste des cas eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ce66e-119">In the Microsoft 365 compliance enter, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="ce66e-120">Cliquez sur le nom de l’incident que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="ce66e-120">Click the name of the case that you want to close.</span></span>

    <span data-ttu-id="ce66e-121">La page flyout **gérer ce cas** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ce66e-121">The **Manage this case** flyout page is displayed.</span></span>

3. <span data-ttu-id="ce66e-122">Sous **Manage case Status**, cliquez sur **Close case**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-122">Under **Manage case status**, click **Close case**.</span></span>

    <span data-ttu-id="ce66e-123">Un avertissement s’affiche indiquant que les conservations associées à la casse seront désactivées.</span><span class="sxs-lookup"><span data-stu-id="ce66e-123">A warning is displayed saying that the holds associated with the case will be turned off.</span></span>

4. <span data-ttu-id="ce66e-124">Cliquez sur **Oui** pour fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="ce66e-124">Click **Yes** to close the case.</span></span>

    <span data-ttu-id="ce66e-125">L’état de la page flyout **gérer ce cas** passe de **actif** à **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-125">The status on the **Manage this case** flyout page is changed from **Active** to **Closing**.</span></span>

5. <span data-ttu-id="ce66e-126">Fermez la page **gérer ce cas** .</span><span class="sxs-lookup"><span data-stu-id="ce66e-126">Close the **Manage this case** page.</span></span>

6. <span data-ttu-id="ce66e-127">Sur la page de **découverte électronique principale** , cliquez sur **Actualiser** pour mettre à jour l’état du cas fermé.</span><span class="sxs-lookup"><span data-stu-id="ce66e-127">On the **Core eDiscovery** page, click **Refresh** to update the status of the closed case.</span></span> <span data-ttu-id="ce66e-128">Le processus de clôture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="ce66e-128">It might take up to 60 minutes for the closing process to complete.</span></span>

    <span data-ttu-id="ce66e-129">Une fois le processus terminé, l’état du cas est modifié sur **fermé** dans la page de **découverte électronique principale** .</span><span class="sxs-lookup"><span data-stu-id="ce66e-129">When the process is complete, the status of the case is changed to **Closed** on the **Core eDiscovery** page.</span></span> <span data-ttu-id="ce66e-130">Cliquez de nouveau sur le nom de l’incident pour afficher la page de démarrage **gérer cet incident** , qui contient des informations sur la date et l’auteur de la fermeture du dossier.</span><span class="sxs-lookup"><span data-stu-id="ce66e-130">Click the name of the case again to display the **Manage this case** flyout page, which contains information about when the case was closed and who closed it.</span></span>

## <a name="reopen-a-closed-case"></a><span data-ttu-id="ce66e-131">Rouvrir un litige clos</span><span class="sxs-lookup"><span data-stu-id="ce66e-131">Reopen a closed case</span></span>

<span data-ttu-id="ce66e-132">Lorsque vous rouvrez un cas, les conservations de découverte électronique qui étaient en place lors de la fermeture de l’incident ne sont pas automatiquement rétablis.</span><span class="sxs-lookup"><span data-stu-id="ce66e-132">When you reopen a case, any eDiscovery holds that were in place when the case was closed won't be automatically reinstated.</span></span> <span data-ttu-id="ce66e-133">Une fois le cas rouvert, vous devez accéder à la page **suspensions** et activer les suspensions précédentes.</span><span class="sxs-lookup"><span data-stu-id="ce66e-133">After the case is reopened, you'll have to go to the **Holds** page and turn on the previous holds.</span></span> <span data-ttu-id="ce66e-134">Pour activer une suspension, sélectionnez-la pour afficher la page de menu volant, puis définissez la bascule d' **État** sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-134">To turn on a hold, select it to display the flyout page, and then set the **Status** toggle to **On**.</span></span>
  
1. <span data-ttu-id="ce66e-135">Dans l’entrée de conformité Microsoft 365, cliquez sur**Centre** de **découverte électronique** > pour afficher la liste des cas eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ce66e-135">In the Microsoft 365 compliance enter, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="ce66e-136">Cliquez sur le nom de l’incident à rouvrir.</span><span class="sxs-lookup"><span data-stu-id="ce66e-136">Click the name of the case that you want to reopen.</span></span>

    <span data-ttu-id="ce66e-137">La page flyout **gérer ce cas** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ce66e-137">The **Manage this case** flyout page is displayed.</span></span> 

3. <span data-ttu-id="ce66e-138">Sous **gérer le statut du cas**, cliquez sur **rouvrir le cas**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-138">Under **Manage case status**, click **Reopen case**.</span></span>

    <span data-ttu-id="ce66e-139">Un avertissement s’affiche indiquant que les conservations associées à la casse lorsqu’elle a été fermée ne sont pas activées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ce66e-139">A warning is displayed saying that the holds that were associated with the case when it was closed won't be turned on automatically.</span></span>

4. <span data-ttu-id="ce66e-140">Cliquez sur **Oui** pour rouvrir le cas.</span><span class="sxs-lookup"><span data-stu-id="ce66e-140">Click **Yes** to reopen the case.</span></span>

    <span data-ttu-id="ce66e-141">L’état de la page flyout **gérer ce cas** passe de **fermé** à **actif**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-141">The status on the **Manage this case** flyout page is changed from **Closed** to **Active**.</span></span>

5. <span data-ttu-id="ce66e-142">Fermez la page **gérer ce cas** .</span><span class="sxs-lookup"><span data-stu-id="ce66e-142">Close the **Manage this case** page.</span></span> 

6. <span data-ttu-id="ce66e-143">Sur la page de **découverte électronique principale** , cliquez sur **Actualiser** pour mettre à jour l’état du cas rouvert.</span><span class="sxs-lookup"><span data-stu-id="ce66e-143">On the **Core eDiscovery** page, click **Refresh** to update the status of the reopened case.</span></span> <span data-ttu-id="ce66e-144">Le processus de réouverture peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="ce66e-144">It might take up to 60 minutes for the reopening process to complete.</span></span> 

    <span data-ttu-id="ce66e-145">Une fois le processus terminé, l’état du cas est modifié sur **actif** sur la page de **découverte électronique principale** .</span><span class="sxs-lookup"><span data-stu-id="ce66e-145">When the process is complete, the status of the case is changed to **Active** on the **Core eDiscovery** page.</span></span> 
  
## <a name="delete-a-case"></a><span data-ttu-id="ce66e-146">Supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="ce66e-146">Delete a case</span></span>

<span data-ttu-id="ce66e-147">Vous pouvez également supprimer des cas eDiscovery principaux en cours et fermés.</span><span class="sxs-lookup"><span data-stu-id="ce66e-147">You can also delete active and closed Core eDiscovery cases.</span></span> <span data-ttu-id="ce66e-148">Lorsque vous supprimez une demande de devis, toutes les recherches et exportations sont supprimées et le cas est supprimé de la liste des cas de la page de **découverte électronique principale** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ce66e-148">When you delete a case, all searches and exports in the case are deleted, and the case is removed from the list of cases on the **Core eDiscovery** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ce66e-149">Vous ne pouvez pas rouvrir un cas supprimé.</span><span class="sxs-lookup"><span data-stu-id="ce66e-149">You can't reopen a deleted case.</span></span>

<span data-ttu-id="ce66e-150">Avant de pouvoir supprimer un incident (qu’il soit actif ou fermé), vous devez d’abord supprimer *toutes les* conservations eDiscovery associées à la casse.</span><span class="sxs-lookup"><span data-stu-id="ce66e-150">Before you can delete a case (whether it's active or closed), you must first delete *all* eDiscovery holds associated with the case.</span></span> <span data-ttu-id="ce66e-151">Cela inclut la suppression des blocages dont l’État est **off**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-151">That includes deleting holds with a status of **Off**.</span></span> 

<span data-ttu-id="ce66e-152">Pour supprimer une conservation eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="ce66e-152">To delete an eDiscovery hold:</span></span>

1. <span data-ttu-id="ce66e-153">Accédez à l’onglet **suspensions** dans le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="ce66e-153">Go the **Holds** tab in the case that you want to delete.</span></span>

2. <span data-ttu-id="ce66e-154">Cliquez sur la conservation que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="ce66e-154">Click the hold that you want to delete.</span></span>

3. <span data-ttu-id="ce66e-155">Sur la page de la fenêtre volante, cliquez sur **Supprimer la conservation**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-155">On the flyout page, click **Delete hold**.</span></span>

<span data-ttu-id="ce66e-156">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="ce66e-156">To delete a case:</span></span>

1. <span data-ttu-id="ce66e-157">Dans l’entrée de conformité Microsoft 365, cliquez sur**Centre** de **découverte électronique** > pour afficher la liste des cas eDiscovery principaux dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ce66e-157">In the Microsoft 365 compliance enter, click **eDiscovery** > **Core** to display the list of Core eDiscovery cases in your organization.</span></span>

2. <span data-ttu-id="ce66e-158">Cliquez sur le nom de la demande de devis que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="ce66e-158">Click the name of the case that you want to delete.</span></span>

3. <span data-ttu-id="ce66e-159">Sous **Manage case Status** sur la page de menu volant, cliquez sur **Delete case**.</span><span class="sxs-lookup"><span data-stu-id="ce66e-159">Under **Manage case status** on the flyout page, click **Delete case**.</span></span>

<span data-ttu-id="ce66e-160">Si le cas que vous essayez de supprimer contient toujours des conservations eDiscovery, vous recevrez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ce66e-160">If the case you're trying to delete still contains eDiscovery holds, you'll receive an error message.</span></span> <span data-ttu-id="ce66e-161">Vous devrez supprimer toutes les conservations associées au cas, puis réessayer de supprimer le cas.</span><span class="sxs-lookup"><span data-stu-id="ce66e-161">You'll have to delete all holds associated with the case and then try again to delete the case.</span></span>
