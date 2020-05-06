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
description: Découvrez ce qui se passe lorsqu’une enquête ou une casse légale prise en charge par un cas de découverte électronique est fermée ou supprimée.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: f91755e6d2aeba89e795a623cd1268af0a53e675
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44035636"
---
# <a name="close-or-delete-a-case"></a><span data-ttu-id="a1758-103">Fermer ou supprimer un cas</span><span class="sxs-lookup"><span data-stu-id="a1758-103">Close or delete a case</span></span>

<span data-ttu-id="a1758-104">Lorsque le cas juridique ou l’enquête pris en charge par un cas de découverte électronique est terminé, vous pouvez fermer le cas.</span><span class="sxs-lookup"><span data-stu-id="a1758-104">When the legal case or investigation supported by an eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="a1758-105">Voici ce qui se passe lorsque vous fermez un cas :</span><span class="sxs-lookup"><span data-stu-id="a1758-105">Here's what happens when you close a case:</span></span>

- <span data-ttu-id="a1758-106">Si le cas contient des emplacements de contenu en conservation, ceux-ci sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="a1758-106">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="a1758-107">Cela peut entraîner la suppression ou le vidage définitifs du contenu, soit par l’utilisateur, soit par un processus automatisé, tel qu’une stratégie de suppression.</span><span class="sxs-lookup"><span data-stu-id="a1758-107">This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>

- <span data-ttu-id="a1758-108">La fermeture d’un incident ne désactive que les blocages associés à ce cas.</span><span class="sxs-lookup"><span data-stu-id="a1758-108">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="a1758-109">Si d’autres suspensions sont placées sur un emplacement de contenu (comme une conservation pour litige).</span><span class="sxs-lookup"><span data-stu-id="a1758-109">If other holds are place on a content location (such as a Litigation Hold.</span></span> <span data-ttu-id="a1758-110">une stratégie de conservation, ou une suspension d’un autre cas de découverte électronique (eDiscovery), ces conservations seront toujours conservées.</span><span class="sxs-lookup"><span data-stu-id="a1758-110">a Preservation Policy, or a hold from a different eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="a1758-111">Le cas est toujours mentionné sur la page eDiscovery dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="a1758-111">The case is still listed on the eDiscovery page in the Security & Compliance Center.</span></span> <span data-ttu-id="a1758-112">Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.</span><span class="sxs-lookup"><span data-stu-id="a1758-112">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="a1758-113">Vous pouvez modifier un cas après sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="a1758-113">You can edit a case after it's closed.</span></span> <span data-ttu-id="a1758-114">Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="a1758-114">For example, you can add or removing members, create searches, export search results, and prepare search results for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="a1758-115">La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lors de la fermeture d’un cas.</span><span class="sxs-lookup"><span data-stu-id="a1758-115">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="a1758-116">Pour fermer un incident :</span><span class="sxs-lookup"><span data-stu-id="a1758-116">To close a case:</span></span>

1. <span data-ttu-id="a1758-117">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez fermer.</span><span class="sxs-lookup"><span data-stu-id="a1758-117">On the **Advanced eDiscovery** page, select the case that you want to close.</span></span>

2. <span data-ttu-id="a1758-118">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="a1758-118">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="a1758-119">Cliquez sur **Fermer le cas**.</span><span class="sxs-lookup"><span data-stu-id="a1758-119">Click **Close case**.</span></span>

<span data-ttu-id="a1758-120">Pour supprimer un cas :</span><span class="sxs-lookup"><span data-stu-id="a1758-120">To delete a case:</span></span>

1. <span data-ttu-id="a1758-121">Sur la page **Advanced eDiscovery** , sélectionnez le cas que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a1758-121">On the **Advanced eDiscovery** page, select the case that you want to delete.</span></span>

2. <span data-ttu-id="a1758-122">Dans l’onglet **paramètres** , sous **informations**sur le cas, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="a1758-122">On the **Settings** tab, under **Case Information**, click **Select**.</span></span>

3. <span data-ttu-id="a1758-123">Cliquez sur **supprimer le cas**.</span><span class="sxs-lookup"><span data-stu-id="a1758-123">Click **Delete case**.</span></span> 
