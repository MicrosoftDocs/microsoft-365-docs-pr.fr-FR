---
title: Suppression d’une boîte aux lettres inactive
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
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
ms.custom:
- seo-marvel-apr2020
description: Lorsque vous n’avez plus besoin de conserver le contenu d’une boîte aux lettres inactive Microsoft 365, vous pouvez supprimer définitivement la boîte aux lettres inactive.
ms.openlocfilehash: 94a20bee1ca3d11a193a25efeb6d73f356e1d58d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909924"
---
# <a name="delete-an-inactive-mailbox"></a><span data-ttu-id="ad06b-103">Suppression d’une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="ad06b-103">Delete an inactive mailbox</span></span>

<span data-ttu-id="ad06b-104">Une boîte aux lettres inactive est utilisée pour conserver le courrier électronique d’un ancien employé après qu’il a quitté votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ad06b-104">An inactive mailbox is used to preserve a former employee's email after they leave your organization.</span></span> <span data-ttu-id="ad06b-105">Si vous n'avez plus besoin du contenu d'une boîte aux lettres inactive, vous pouvez le supprimer de façon définitive en supprimant le blocage.</span><span class="sxs-lookup"><span data-stu-id="ad06b-105">When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold.</span></span> <span data-ttu-id="ad06b-106">En outre, il est possible que plusieurs blocages soient placés sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-106">Also, it's possible that multiple holds might be placed on an inactive mailbox.</span></span> <span data-ttu-id="ad06b-107">Par exemple, une boîte aux lettres inactive peut être placée en suspension pour litige et sur une ou plusieurs blocages sur place.</span><span class="sxs-lookup"><span data-stu-id="ad06b-107">For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds.</span></span> <span data-ttu-id="ad06b-108">En outre, une stratégie de rétention (créée dans le centre de sécurité et conformité dans Office 365 ou Microsoft 365) peut être appliquée à la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-108">Additionally, a retention policy (created in the security and compliance center in Office 365 or Microsoft 365) might be applied to the inactive mailbox.</span></span> <span data-ttu-id="ad06b-109">Vous devez supprimer toutes les conservations et stratégies de rétention d’une boîte aux lettres inactive pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="ad06b-109">You have to remove all holds and retention policies from an inactive mailbox to delete it.</span></span> <span data-ttu-id="ad06b-110">Une fois que vous avez supprimé les stratégies de conservation et de rétention, la boîte aux lettres inactive est marquée pour suppression et définitivement supprimée après son traitement.</span><span class="sxs-lookup"><span data-stu-id="ad06b-110">After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ad06b-111">À mesure que nous continuons d’investir de différentes façons pour conserver le contenu des boîtes aux lettres, nous an anvions le retrait des conservations In-Place dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="ad06b-111">As we continue to invest in different ways to preserve mailbox content, we're announcing the retirement of In-Place Holds in the Exchange admin center.</span></span> <span data-ttu-id="ad06b-112">Cela signifie que vous devez utiliser des conservations pour litige et des stratégies de rétention pour créer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-112">That means you should use Litigation Holds and retention policies to create an inactive mailbox.</span></span> <span data-ttu-id="ad06b-113">À compter du 1er juillet 2020, vous ne pourrez plus créer de In-Place en cours d’accès dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ad06b-113">Starting July 1, 2020 you won't be able to create new In-Place Holds in Exchange Online.</span></span> <span data-ttu-id="ad06b-114">Toutefois, vous pourrez toujours modifier la durée d’une In-Place placée sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-114">But you'll still be able to change the hold duration of an In-Place Hold placed on an inactive mailbox.</span></span> <span data-ttu-id="ad06b-115">Toutefois, à compter du 1er octobre 2020, vous ne pourrez pas modifier la durée de la durée de la durée de la période de attente.</span><span class="sxs-lookup"><span data-stu-id="ad06b-115">However, starting October 1, 2020, you won't be able to change the hold duration.</span></span> <span data-ttu-id="ad06b-116">Vous ne pourrez supprimer une boîte aux lettres inactive qu’en supprimant la In-Place de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ad06b-116">You'll only be able to delete an inactive mailbox by removing the In-Place Hold.</span></span> <span data-ttu-id="ad06b-117">Les boîtes aux lettres inactives existantes qui sont en conservation In-Place sont conservées jusqu’à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="ad06b-117">Existing inactive mailboxes that are on In-Place Hold will still be preserved until the hold is removed.</span></span> <span data-ttu-id="ad06b-118">Pour plus d’informations sur le retrait des In-Place, voir [Retrait des outils eDiscovery hérités.](legacy-ediscovery-retirement.md)</span><span class="sxs-lookup"><span data-stu-id="ad06b-118">For more information about the retirement of In-Place Holds, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md).</span></span>
  
<span data-ttu-id="ad06b-119">Consultez la section [Plus d'informations](#more-information) pour obtenir une description de ce qui se produit après la suppression des blocages d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-119">See the [More information](#more-information) section for a description of what happens after holds are removed from an inactive mailbox.</span></span>
  
## <a name="before-you-delete-an-inactive-mailbox"></a><span data-ttu-id="ad06b-120">Avant de supprimer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="ad06b-120">Before you delete an inactive mailbox</span></span>

- <span data-ttu-id="ad06b-121">Vous devez utiliser Exchange Online PowerShell pour supprimer une mise en attente pour litige d’une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-121">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="ad06b-122">Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="ad06b-122">You can't use the Exchange admin center (EAC).</span></span> <span data-ttu-id="ad06b-123">Pour obtenir des instructions, consultez [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="ad06b-123">For step-by-step instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="ad06b-124">Vous pouvez copier le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres avant de supprimer la conservation et de supprimer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-124">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox.</span></span> <span data-ttu-id="ad06b-125">Pour plus d’informations, voir [Restaurer une boîte aux lettres inactive dans Office 365.](restore-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="ad06b-125">For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>

- <span data-ttu-id="ad06b-126">Si vous supprimez la stratégie de conservation ou de rétention d’une boîte aux lettres inactive et que la période de rétention de la boîte aux lettres supprimée (suppression définitive) de la boîte aux lettres a expiré, la boîte aux lettres est définitivement supprimée.</span><span class="sxs-lookup"><span data-stu-id="ad06b-126">If you remove the hold or retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted.</span></span> <span data-ttu-id="ad06b-127">Après sa suppression, elle ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="ad06b-127">After it's deleted, it can't be recovered.</span></span> <span data-ttu-id="ad06b-128">Avant de supprimer la conservation, vérifiez que vous n'avez plus besoin du contenu de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ad06b-128">Before you remove the hold, be sure that you no longer need the contents in the mailbox.</span></span> <span data-ttu-id="ad06b-129">Si vous souhaitez réactiver une boîte aux lettres inactive, vous pouvez la récupérer.</span><span class="sxs-lookup"><span data-stu-id="ad06b-129">If you want to reactivate an inactive mailbox, you can recover it.</span></span> <span data-ttu-id="ad06b-130">Pour plus d’informations, [voir Récupérer une boîte aux lettres inactive dans Office 365.](recover-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="ad06b-130">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>

- <span data-ttu-id="ad06b-131">Pour plus d’informations sur les boîtes aux lettres inactives, voir Boîtes aux lettres [inactives dans Office 365.](inactive-mailboxes-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="ad06b-131">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>

## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="ad06b-132">Étape 1 : Identifier les blocages sur une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="ad06b-132">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="ad06b-133">Comme indiqué précédemment, une conservation pour litige, une In-Place de rétention ou une stratégie de rétention peuvent être placées sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-133">As previously stated, a Litigation Hold, In-Place Hold, or retention policy might be placed on an inactive mailbox.</span></span> <span data-ttu-id="ad06b-134">La première étape consiste à identifier les blocages sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-134">The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="ad06b-135">Exécutez la commande suivante pour afficher les informations de blocage pour toutes les boîtes aux lettres inactives dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ad06b-135">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```powershell
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="ad06b-136">La valeur de **True** pour la propriété **LitigationHoldEnabled** indique que la boîte aux lettres inactive est en suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="ad06b-136">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold.</span></span> <span data-ttu-id="ad06b-137">Si un blocage sur place est placé sur une boîte aux lettres inactive, le GUID du blocage s'affiche comme valeur pour la propriété **InPlaceHolds**.</span><span class="sxs-lookup"><span data-stu-id="ad06b-137">If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property.</span></span> <span data-ttu-id="ad06b-138">Par exemple, les résultats suivants pour deux boîtes aux lettres inactives indiquent qu’une conservation pour litige est placée sur Ann Beebe et qu’une conservation In-Place et une stratégie de rétention sont placées sur Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="ad06b-138">For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that an In-Place Hold and retention policy are placed on Pilar Pinilla.</span></span>
  
```text
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, mbxba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> <span data-ttu-id="ad06b-139">Si un grand nombre de conservations In-Place ou de stratégies de rétention sont placées sur une boîte aux lettres inactive, tous les In-Place de conservation ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="ad06b-139">If a lot of In-Place Holds or retention policies are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed.</span></span> <span data-ttu-id="ad06b-140">Vous pouvez exécuter la commande suivante pour afficher tous les GUID dans la propriété InPlaceHolds :  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="ad06b-140">You can run the following command to display all the GUIDs in the InPlaceHolds property:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
<span data-ttu-id="ad06b-141">Pour plus d’informations sur l’identification des mises en attente, voir Comment identifier le type de mise en attente [placée sur une boîte aux lettres](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="ad06b-141">For more information about identify holds, see [How to identify the type of hold placed on a mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="ad06b-142">Étape 2 : Supprimer une blocage d'une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="ad06b-142">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="ad06b-p109">Après avoir identifié le type de blocage placé sur la boîte aux lettres inactive (et s'il y a plusieurs blocages), l'étape suivante consiste à supprimer les blocages sur la boîte aux lettres. Comme indiqué précédemment, vous devez supprimer tous les blocages pour supprimer définitivement une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p109">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox. As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span>
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="ad06b-145">Supprimer une suspension pour litige</span><span class="sxs-lookup"><span data-stu-id="ad06b-145">Remove a Litigation Hold</span></span>

<span data-ttu-id="ad06b-p110">Comme indiqué précédemment, vous devez utiliser Windows PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive. Vous ne pouvez pas utiliser le CAE. Exécutez la commande suivante pour supprimer une suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p110">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the EAC. Run the following command to remove a Litigation Hold.</span></span>
  
```powershell
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="ad06b-p111">La meilleure façon d'identifier une boîte aux lettres inactive est d'utiliser son nom unique ou sa valeur GUID Exchange. L'une de ces valeurs permet d'empêcher de spécifier par inadvertance la mauvaise boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p111">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-an-inactive-mailbox-from-a-retention-policy"></a><span data-ttu-id="ad06b-151">Supprimer une boîte aux lettres inactive d’une stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="ad06b-151">Remove an inactive mailbox from a retention policy</span></span>

<span data-ttu-id="ad06b-152">La procédure de suppression d’une boîte aux lettres inactive d’une stratégie de rétention Microsoft 365 varie selon que la stratégie de rétention affectée à la boîte aux lettres inactive est explicite ou à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ad06b-152">The procedure to remove an inactive mailbox from a Microsoft 365 retention policy depends whether the retention policy assigned to the inactive mailbox is organization-wide or explicit.</span></span> <span data-ttu-id="ad06b-153">sur le type de stratégie de rétention qui est affecté à la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-153">on the type of retention policy that's assigned to the inactive mailbox.</span></span>

- <span data-ttu-id="ad06b-154">Stratégies de rétention à l’échelle de l’organisation affectées à toutes les boîtes aux lettres de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ad06b-154">Organization-wide retention policies assigned to all mailboxes in the organization.</span></span> <span data-ttu-id="ad06b-155">Utilisez la cmdlet **Get-OrganizationConfig** dans Exchange Online PowerShell pour obtenir des informations sur les stratégies de rétention à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ad06b-155">Use the **Get-OrganizationConfig** cmdlet in Exchange Online PowerShell to get information about organization-wide retention policies.</span></span>

- <span data-ttu-id="ad06b-156">Stratégies de rétention d’emplacement spécifiques affectées à des boîtes aux lettres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ad06b-156">Specific location retention policies assigned to specific mailboxes.</span></span> <span data-ttu-id="ad06b-157">Ce sont des stratégies qui sont affectées aux emplacements de contenu d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ad06b-157">These are policies that are assigned to the content locations of specific users.</span></span> <span data-ttu-id="ad06b-158">Utilisez la cmdlet **Get-Mailbox -IncludeInactiveMailbox** dans Exchange Online PowerShell pour obtenir des informations sur les stratégies de rétention attribuées à des boîtes aux lettres inactives spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ad06b-158">Use the **Get-Mailbox -IncludeInactiveMailbox** cmdlet in Exchange Online PowerShell to get information about retention policies assigned to specific inactive mailboxes.</span></span>

#### <a name="remove-an-inactive-mailbox-from-an-organization-wide-retention-policy"></a><span data-ttu-id="ad06b-159">Supprimer une boîte aux lettres inactive d’une stratégie de rétention à l’échelle de l’organisation</span><span class="sxs-lookup"><span data-stu-id="ad06b-159">Remove an inactive mailbox from an organization-wide retention policy</span></span>

<span data-ttu-id="ad06b-160">Exécutez la commande suivante dans Exchange Online PowerShell pour exclure une boîte aux lettres inactive d’une stratégie de rétention à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ad06b-160">Run the following command in Exchange Online PowerShell to exclude an inactive mailbox from an organization-wide retention policy.</span></span>

```powershell
Set-Mailbox <identity of inactive mailbox> -ExcludeFromOrgHolds <retention policy GUID without prefix or suffix>
```

<span data-ttu-id="ad06b-161">Pour plus d’informations sur l’identification des stratégies de rétention à l’échelle de l’organisation appliquées à une boîte aux lettres inactive et sur l’obtention du GUID d’une stratégie de rétention, consultez la section « Get-OrganizationConfig » dans comment identifier le [type](identify-a-hold-on-an-exchange-online-mailbox.md#get-organizationconfig)de conservation placé sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ad06b-161">For more information identifying organization-wide retention policies applied to an inactive mailbox and obtaining the GUID for a retention policy, see the "Get-OrganizationConfig" section in [How to identify the type of hold placed on a mailbox](identify-a-hold-on-an-exchange-online-mailbox.md#get-organizationconfig).</span></span>

<span data-ttu-id="ad06b-162">Vous pouvez également exécuter la commande suivante pour supprimer la boîte aux lettres inactive de toutes les stratégies à l’échelle de l’organisation :</span><span class="sxs-lookup"><span data-stu-id="ad06b-162">Alternatively, you can run the following command to remove the inactive mailbox from all organization-wide policies:</span></span>

```powershell
Set-Mailbox <identity of inactive mailbox> -ExcludeFromAllOrgHolds
```

#### <a name="remove-an-inactive-mailbox-from-a-specific-location-retention-policy"></a><span data-ttu-id="ad06b-163">Supprimer une boîte aux lettres inactive d’une stratégie de rétention d’emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="ad06b-163">Remove an inactive mailbox from a specific location retention policy</span></span>

<span data-ttu-id="ad06b-164">Exécutez la commande suivante dans [le Centre de sécurité & conformité PowerShell](/powershell/exchange/connect-to-scc-powershell) pour supprimer une boîte aux lettres inactive d’une stratégie de rétention explicite.</span><span class="sxs-lookup"><span data-stu-id="ad06b-164">Run the following command in [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) to remove an inactive mailbox from an explicit retention policy.</span></span>

```powershell
Set-RetentionCompliancePolicy -Identity <retention policy GUID without prefix or suffix> -AddExchangeLocationException <identity of inactive mailbox>
```

<span data-ttu-id="ad06b-165">Pour plus d’informations sur l’identification des stratégies de rétention d’emplacement spécifiques appliquées à une boîte aux lettres inactive et l’obtention du GUID d’une stratégie de rétention, consultez la section « Get-Mailbox » dans Comment identifier le [type](identify-a-hold-on-an-exchange-online-mailbox.md#get-mailbox)de conservation placé sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ad06b-165">For more information identifying specific location retention policies applied to an inactive mailbox and obtaining the GUID for a retention policy, see the "Get-Mailbox" section in [How to identify the type of hold placed on a mailbox](identify-a-hold-on-an-exchange-online-mailbox.md#get-mailbox).</span></span>

### <a name="remove-in-place-holds"></a><span data-ttu-id="ad06b-166">Supprimer des blocages sur place</span><span class="sxs-lookup"><span data-stu-id="ad06b-166">Remove In-Place Holds</span></span>

 <span data-ttu-id="ad06b-167">Il existe deux façons de supprimer un blocage sur place à partir d'une boîte aux lettres inactive :</span><span class="sxs-lookup"><span data-stu-id="ad06b-167">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="ad06b-168">**Supprimez lIn-Place hold .**</span><span class="sxs-lookup"><span data-stu-id="ad06b-168">**Delete the In-Place Hold object**.</span></span> <span data-ttu-id="ad06b-169">Si la boîte aux lettres inactive que vous souhaitez supprimer définitivement est la seule boîte aux lettres source pour une In-Place, vous pouvez simplement supprimer l’objet In-Place hold.</span><span class="sxs-lookup"><span data-stu-id="ad06b-169">If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ad06b-p116">Vous devez désactiver le blocage avant de pouvoir supprimer un objet de blocage sur place. Si vous essayez de supprimer un objet de blocage sur place ayant le blocage activé, vous recevrez un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p116">You have to disable the hold before you can delete an In-Place Hold object. If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="ad06b-172">**Supprimez la boîte aux lettres inactive en tant que boîte aux lettres source d’une In-Place en attente.**</span><span class="sxs-lookup"><span data-stu-id="ad06b-172">**Remove the inactive mailbox as a source mailbox of an In-Place Hold**.</span></span> <span data-ttu-id="ad06b-173">Si vous souhaitez conserver d’autres boîtes aux lettres source pour une In-Place, vous pouvez supprimer la boîte aux lettres inactive de la liste des boîtes aux lettres source et conserver l’objet In-Place Hold.</span><span class="sxs-lookup"><span data-stu-id="ad06b-173">If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span>

#### <a name="delete-an-in-place-hold"></a><span data-ttu-id="ad06b-174">Supprimer une In-Place en attente</span><span class="sxs-lookup"><span data-stu-id="ad06b-174">Delete an In-Place Hold</span></span>

1. <span data-ttu-id="ad06b-p118">Créez une variable qui contient les propriétés du blocage sur place à supprimer. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ad06b-p118">Create a variable that contains the properties of the In-Place Hold that you want to delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

   ```powershell
   $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
   ```

2. <span data-ttu-id="ad06b-177">Désactivez le blocage sur le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ad06b-177">Disable the hold on the In-Place Hold.</span></span>

   ```powershell
   Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
   ```

3. <span data-ttu-id="ad06b-178">Supprimez le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ad06b-178">Delete the In-Place Hold.</span></span>

   ```powershell
   Remove-MailboxSearch $InPlaceHold.Name
   ```

#### <a name="remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="ad06b-179">Supprimer une boîte aux lettres inactive d’une In-Place en attente</span><span class="sxs-lookup"><span data-stu-id="ad06b-179">Remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="ad06b-180">Si le blocage sur place contient un grand nombre de boîtes aux lettres source, il est possible que la boîte aux lettres inactive ne soit pas répertoriée sur la page **Sources** dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="ad06b-180">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC.</span></span> <span data-ttu-id="ad06b-181">Jusqu'à 3 000 boîtes aux lettres s'affichent sur la page **Sources** lorsque vous modifiez un blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ad06b-181">Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold.</span></span> <span data-ttu-id="ad06b-182">Si une boîte aux lettres inactive n’est pas répertoriée dans la page **Sources,** vous pouvez utiliser Exchange Online PowerShell pour la supprimer de la In-Place conserver.</span><span class="sxs-lookup"><span data-stu-id="ad06b-182">If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="ad06b-p120">Créez une variable qui contient les propriétés du blocage sur place placé sur la boîte aux lettres inactive. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ad06b-p120">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```powershell
    $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
    ```

2. <span data-ttu-id="ad06b-185">Vérifiez que la boîte aux lettres inactive est répertoriée comme une boîte aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ad06b-185">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 

   ```powershell
   $InPlaceHold.Sources
   ```

   > [!NOTE]
   > <span data-ttu-id="ad06b-p121">La propriété *Sources* du blocage sur place identifie les boîtes aux lettres source par leurs propriétés *LegacyExchangeDN*. Étant donné que cette propriété identifie les boîtes aux lettres inactives de façon unique, l'utilisation de la propriété *Sources* du blocage sur place permet d'empêcher la suppression de la boîte aux lettres incorrecte. Cela permet également d'éviter les problèmes si deux boîtes aux lettres ont le même alias ou la même adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p121">The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties. Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox. This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 

3. <span data-ttu-id="ad06b-p122">Supprimez la boîte aux lettres inactive dans la liste des boîtes aux lettres sources dans la variable. Veillez à utiliser le **LegacyExchangeDN** de la boîte aux lettres inactive qui est renvoyé par la commande à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p122">Remove the inactive mailbox from the list of source mailboxes in the variable. Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 

    ```powershell
    $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
    ```

    <span data-ttu-id="ad06b-191">Par exemple, la commande suivante supprime la boîte aux lettres inactive pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="ad06b-191">For example, the following command removes the inactive mailbox for Pilar Pinilla.</span></span>

    ```powershell
    $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/ cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
    ```

4. <span data-ttu-id="ad06b-192">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source dans la variable.</span><span class="sxs-lookup"><span data-stu-id="ad06b-192">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>

   ```powershell
   $InPlaceHold.Sources
   ```

5. <span data-ttu-id="ad06b-193">Modifiez le blocage sur place avec la liste mise à jour des boîtes aux lettres source, qui n'inclut pas la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-193">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>

   ```powershell
   Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
   ```

6. <span data-ttu-id="ad06b-194">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ad06b-194">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>

   ```powershell
   Get-MailboxSearch $InPlaceHold.Name | FL Sources
   ```

## <a name="more-information"></a><span data-ttu-id="ad06b-195">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad06b-195">More information</span></span>

- <span data-ttu-id="ad06b-p123">**Une boîte aux lettres inactive est un type de boîte aux lettres supprimée (récupérable).** Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique. Le délai de rétention d'une boîte aux lettres supprimée (récupérable) dans Exchange Online est de 30 jours. Ainsi, la boîte aux lettres peut être récupérée dans les 30 jours qui suivent le moment où elle a été supprimée (récupérable). Après 30 jours, une boîte aux lettres supprimée (récupérable) est marquée pour suppression définitive et ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p123">**An inactive mailbox is a type of soft-deleted mailbox.** In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered within 30 days of being soft-deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span>

- <span data-ttu-id="ad06b-201">**Que se passe-t-il après avoir supprimé la conservation sur une boîte aux lettres inactive ?**</span><span class="sxs-lookup"><span data-stu-id="ad06b-201">**What happens after you remove the hold on an inactive mailbox?**</span></span> <span data-ttu-id="ad06b-202">La boîte aux lettres est traitée comme d'autres boîtes aux lettres supprimées (récupérables) et est marquée pour suppression définitive après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable) de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="ad06b-202">The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 30-day soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="ad06b-203">Ce délai de rétention commence à la date à laquelle la boîte aux lettres a été rendue inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ad06b-203">This retention period starts on the date when the mailbox was first made inactive.</span></span> <span data-ttu-id="ad06b-204">Cette date est connue sous le nom de date de suppression (suppression possible), qui correspond à la date à laquelle le compte d’utilisateur correspondant a été supprimé ou à laquelle la boîte aux lettres Exchange Online a été supprimée avec la cmdlet **Remove-Mailbox.**</span><span class="sxs-lookup"><span data-stu-id="ad06b-204">This date is known as the soft-deleted date, which is the date the corresponding user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet.</span></span> <span data-ttu-id="ad06b-205">La date supprimée (récupérable) n'est pas la date de suppression du blocage.</span><span class="sxs-lookup"><span data-stu-id="ad06b-205">The soft-deleted date isn't the date on which you remove the hold.</span></span>

- <span data-ttu-id="ad06b-p125">**Une boîte aux lettres inactive est-elle définitivement supprimée immédiatement après la suppression de la conservation ?** Si la date supprimée (récupérable) pour une boîte aux lettres inactive est de plus de 30 jours, la boîte aux lettres n'est pas supprimée définitivement dès que vous supprimez la conservation. La boîte aux lettres sera marquée pour suppression définitive et sera supprimée lors de son prochain traitement.</span><span class="sxs-lookup"><span data-stu-id="ad06b-p125">**Is an inactive mailbox permanently deleted immediately after the hold is removed?** If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold. The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span></span>

- <span data-ttu-id="ad06b-209">**Quel est l'impact de la période de rétention de la boîte aux lettres supprimée (récupérable) sur les boîtes aux lettres inactives ?**</span><span class="sxs-lookup"><span data-stu-id="ad06b-209">**How does the soft-deleted mailbox retention period affect inactive mailboxes?**</span></span> <span data-ttu-id="ad06b-210">Si la date supprimée (récupérable) pour une boîte aux lettres inactive se situe plus de 30 jours avant la date de la suppression de la conservation, la boîte aux lettres est marquée pour suppression définitive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-210">If the soft-deleted date for an inactive mailbox is more than 30 days before the date the hold was removed, the mailbox is marked for permanent deletion.</span></span> <span data-ttu-id="ad06b-211">Par contre, si la date supprimée (récupérable) d'une boîte aux lettres inactive se situe dans les 30 derniers jours et que vous supprimez la conservation, vous pouvez récupérer la boîte aux lettres jusqu'à l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable).</span><span class="sxs-lookup"><span data-stu-id="ad06b-211">But if an inactive mailbox has a soft-deleted date within the last 30 days and you remove the hold, you can recover the mailbox up until the soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="ad06b-212">Pour plus d’informations, voir [Supprimer ou restaurer des boîtes aux lettres utilisateur dans Exchange Online.](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes)</span><span class="sxs-lookup"><span data-stu-id="ad06b-212">For details, see [Delete or restore user mailboxes in Exchange Online](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes).</span></span> <span data-ttu-id="ad06b-213">Une fois la période de rétention des boîtes aux lettres supprimée (récupérable) expirée, vous devez suivre les procédures de récupération d’une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ad06b-213">After the soft-deleted mailbox retention period expires, you have to follow the procedures for recovering an inactive mailbox.</span></span> <span data-ttu-id="ad06b-214">Pour plus d’informations, [voir Récupérer une boîte aux lettres inactive dans Office 365.](recover-an-inactive-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="ad06b-214">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>

- <span data-ttu-id="ad06b-215">**Comment afficher des informations sur une boîte aux lettres inactive après la suppression de la conservation ?**</span><span class="sxs-lookup"><span data-stu-id="ad06b-215">**How do you display information about an inactive mailbox after the hold is removed?**</span></span> <span data-ttu-id="ad06b-216">Une fois qu’une boîte aux lettres inactive a été supprimée et que la boîte aux lettres inactive est revenir à une boîte aux lettres supprimée (suppression réverable), elle ne sera pas renvoyée à l’aide du paramètre *InactiveMailboxOnly* avec la cmdlet **Get-Mailbox.**</span><span class="sxs-lookup"><span data-stu-id="ad06b-216">After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet.</span></span> <span data-ttu-id="ad06b-217">Cependant, vous pouvez afficher des informations sur la boîte aux lettres à l'aide de la commande **Get-Mailbox -SoftDeletedMailbox**.</span><span class="sxs-lookup"><span data-stu-id="ad06b-217">But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command.</span></span> <span data-ttu-id="ad06b-218">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ad06b-218">For example:</span></span>

  ```text
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
  ```

  <span data-ttu-id="ad06b-219">Dans l’exemple ci-dessus, la *propriété WhenSoftDeleted* identifie la date supprimée (supprimée (supprimé(s) (supprimé(s) (dans cet exemple) : 30 octobre 2014.</span><span class="sxs-lookup"><span data-stu-id="ad06b-219">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is October 30, 2014.</span></span> <span data-ttu-id="ad06b-220">Si cette boîte aux lettres supprimée (logiciel) était auparavant une boîte aux lettres inactive pour laquelle la boîte aux lettres a été supprimée, elle sera définitivement supprimée 30 jours après la valeur de la propriété *WhenSoftDeleted.*</span><span class="sxs-lookup"><span data-stu-id="ad06b-220">If this soft-deleted mailbox was previously an inactive mailbox for which the hold was removed, it will be permanently deleted 30 days after the value of the *WhenSoftDeleted* property.</span></span> <span data-ttu-id="ad06b-221">Dans ce cas, la boîte aux lettres est définitivement supprimée après le 30 novembre 2014.</span><span class="sxs-lookup"><span data-stu-id="ad06b-221">In this case, the mailbox is permanently deleted after November 30, 2014.</span></span>