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
description: " "
ms.openlocfilehash: 15b6327809b3557c4d0d90b6c10dc5568ba47f43
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595871"
---
# <a name="close-or-delete-a-case"></a><span data-ttu-id="dcc04-102">Fermer ou supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="dcc04-102">Close or delete a case</span></span>

<span data-ttu-id="dcc04-103">Lorsque le cas juridique ou l’enquête pris en charge par un cas de découverte électronique est terminé, vous pouvez fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="dcc04-103">When the legal case or investigation supported by an eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="dcc04-104">Voici ce qui se passe lorsque vous fermez un cas :</span><span class="sxs-lookup"><span data-stu-id="dcc04-104">Here's what happens when you close a case:</span></span>

- <span data-ttu-id="dcc04-105">Si le cas contient des emplacements de contenu en conservation, ceux-ci sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="dcc04-105">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="dcc04-106">Cela peut entraîner la suppression ou le vidage définitifs du contenu, soit par l’utilisateur, soit par un processus automatisé, tel qu’une stratégie de suppression.</span><span class="sxs-lookup"><span data-stu-id="dcc04-106">This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>

- <span data-ttu-id="dcc04-107">La fermeture d’un incident ne désactive que les blocages associés à ce cas.</span><span class="sxs-lookup"><span data-stu-id="dcc04-107">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="dcc04-108">Si d’autres suspensions sont placées sur un emplacement de contenu (comme une conservation pour litige).</span><span class="sxs-lookup"><span data-stu-id="dcc04-108">If other holds are place on a content location (such as a Litigation Hold.</span></span> <span data-ttu-id="dcc04-109">une stratégie de conservation, ou une suspension d’un autre cas de découverte électronique (eDiscovery), ces conservations seront toujours conservées.</span><span class="sxs-lookup"><span data-stu-id="dcc04-109">a Preservation Policy, or a hold from a different eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="dcc04-110">Le cas est toujours mentionné sur la page eDiscovery dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="dcc04-110">The case is still listed on the eDiscovery page in the Security & Compliance Center.</span></span> <span data-ttu-id="dcc04-111">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="dcc04-111">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="dcc04-112">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="dcc04-112">You can edit a case after it's closed.</span></span> <span data-ttu-id="dcc04-113">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="dcc04-113">For example, you can add or removing members, create searches, export search results, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="dcc04-114">La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lors de la fermeture d’un cas.</span><span class="sxs-lookup"><span data-stu-id="dcc04-114">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="dcc04-115">Pour fermer un incident :</span><span class="sxs-lookup"><span data-stu-id="dcc04-115">To close a case:</span></span>

1. <span data-ttu-id="dcc04-116">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="dcc04-116">On the **Advanced eDiscovery** page, select the case that you want to close.</span></span>

2. <span data-ttu-id="dcc04-117">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="dcc04-117">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="dcc04-118">Cliquez sur **Fermer le cas**.</span><span class="sxs-lookup"><span data-stu-id="dcc04-118">Click **Close case**.</span></span>

<span data-ttu-id="dcc04-119">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="dcc04-119">To delete a case:</span></span>

1. <span data-ttu-id="dcc04-120">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="dcc04-120">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="dcc04-121">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="dcc04-121">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="dcc04-122">Cliquez sur **supprimer le cas**.</span><span class="sxs-lookup"><span data-stu-id="dcc04-122">Click **Delete case**.</span></span> 
