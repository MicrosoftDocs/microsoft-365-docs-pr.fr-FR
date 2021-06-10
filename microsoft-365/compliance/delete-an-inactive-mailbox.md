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
description: Lorsque vous n’avez plus besoin de conserver le contenu d’Microsoft 365 boîte aux lettres inactive, vous pouvez supprimer définitivement la boîte aux lettres inactive.
ms.openlocfilehash: 077a71bfdd82721e0992e5d14073aa037b7cfd1b
ms.sourcegitcommit: d3f8c69519c593b1580cfa7187ce085a99b8a846
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52100823"
---
# <a name="delete-an-inactive-mailbox"></a><span data-ttu-id="7397a-103">Suppression d’une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7397a-103">Delete an inactive mailbox</span></span>

<span data-ttu-id="7397a-104">Une boîte aux lettres inactive est utilisée pour conserver le courrier électronique d’un ancien employé après qu’il a quitté votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7397a-104">An inactive mailbox is used to preserve a former employee's email after they leave your organization.</span></span> <span data-ttu-id="7397a-105">Si vous n'avez plus besoin du contenu d'une boîte aux lettres inactive, vous pouvez le supprimer de façon définitive en supprimant le blocage.</span><span class="sxs-lookup"><span data-stu-id="7397a-105">When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold.</span></span> <span data-ttu-id="7397a-106">En outre, il est possible que plusieurs blocages soient placés sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-106">Also, it's possible that multiple holds might be placed on an inactive mailbox.</span></span> <span data-ttu-id="7397a-107">Par exemple, une boîte aux lettres inactive peut être placée en suspension pour litige et sur une ou plusieurs blocages sur place.</span><span class="sxs-lookup"><span data-stu-id="7397a-107">For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds.</span></span> <span data-ttu-id="7397a-108">En outre, une stratégie de rétention (créée dans le centre de sécurité et conformité dans Office 365 ou Microsoft 365) peut être appliquée à la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-108">Additionally, a retention policy (created in the security and compliance center in Office 365 or Microsoft 365) might be applied to the inactive mailbox.</span></span> <span data-ttu-id="7397a-109">Vous devez supprimer toutes les conservations et stratégies de rétention d’une boîte aux lettres inactive pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="7397a-109">You have to remove all holds and retention policies from an inactive mailbox to delete it.</span></span> <span data-ttu-id="7397a-110">Une fois que vous avez supprimé les stratégies de conservation et de rétention, la boîte aux lettres inactive est marquée pour suppression et définitivement supprimée après son traitement.</span><span class="sxs-lookup"><span data-stu-id="7397a-110">After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7397a-111">À mesure que nous continuons d’investir de différentes façons pour conserver le contenu des boîtes aux lettres, nous anuons le retrait des conservations In-Place dans le Centre d’administration Exchange gestion.</span><span class="sxs-lookup"><span data-stu-id="7397a-111">As we continue to invest in different ways to preserve mailbox content, we're announcing the retirement of In-Place Holds in the Exchange admin center.</span></span> <span data-ttu-id="7397a-112">Cela signifie que vous devez utiliser des conservations pour litige et des stratégies de rétention pour créer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-112">That means you should use Litigation Holds and retention policies to create an inactive mailbox.</span></span> <span data-ttu-id="7397a-113">À compter du 1er juillet 2020, vous ne pourrez plus créer de In-Place de Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7397a-113">Starting July 1, 2020 you won't be able to create new In-Place Holds in Exchange Online.</span></span> <span data-ttu-id="7397a-114">Toutefois, vous pourrez toujours modifier la durée d’une In-Place placée sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-114">But you'll still be able to change the hold duration of an In-Place Hold placed on an inactive mailbox.</span></span> <span data-ttu-id="7397a-115">Toutefois, à compter du 1er octobre 2020, vous ne pourrez pas modifier la durée de la durée de la durée de la période de attente.</span><span class="sxs-lookup"><span data-stu-id="7397a-115">However, starting October 1, 2020, you won't be able to change the hold duration.</span></span> <span data-ttu-id="7397a-116">Vous ne pourrez supprimer une boîte aux lettres inactive qu’en supprimant la In-Place de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7397a-116">You'll only be able to delete an inactive mailbox by removing the In-Place Hold.</span></span> <span data-ttu-id="7397a-117">Les boîtes aux lettres inactives existantes qui sont en conservation In-Place sont conservées jusqu’à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="7397a-117">Existing inactive mailboxes that are on In-Place Hold will still be preserved until the hold is removed.</span></span> <span data-ttu-id="7397a-118">Pour plus d’informations sur le retrait des In-Place, voir [Retrait des outils eDiscovery hérités.](legacy-ediscovery-retirement.md)</span><span class="sxs-lookup"><span data-stu-id="7397a-118">For more information about the retirement of In-Place Holds, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md).</span></span>
  
<span data-ttu-id="7397a-119">Consultez la section [Plus d'informations](#more-information) pour obtenir une description de ce qui se produit après la suppression des blocages d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-119">See the [More information](#more-information) section for a description of what happens after holds are removed from an inactive mailbox.</span></span>
  
## <a name="before-you-delete-an-inactive-mailbox"></a><span data-ttu-id="7397a-120">Avant de supprimer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7397a-120">Before you delete an inactive mailbox</span></span>

- <span data-ttu-id="7397a-121">Vous devez utiliser powershell Exchange Online pour supprimer une attente pour litige d’une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-121">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="7397a-122">Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="7397a-122">You can't use the Exchange admin center (EAC).</span></span> <span data-ttu-id="7397a-123">Pour obtenir des instructions, consultez [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7397a-123">For step-by-step instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="7397a-124">Vous pouvez copier le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres avant de supprimer la conservation et de supprimer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-124">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox.</span></span> <span data-ttu-id="7397a-125">Pour plus d’informations, voir [Restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="7397a-125">For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>

- <span data-ttu-id="7397a-126">Si vous supprimez la stratégie de conservation ou de rétention d’une boîte aux lettres inactive et que la période de rétention de la boîte aux lettres supprimée (suppression temporaire) de la boîte aux lettres a expiré, la boîte aux lettres est définitivement supprimée.</span><span class="sxs-lookup"><span data-stu-id="7397a-126">If you remove the hold or retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted.</span></span> <span data-ttu-id="7397a-127">Après sa suppression, elle ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="7397a-127">After it's deleted, it can't be recovered.</span></span> <span data-ttu-id="7397a-128">Avant de supprimer la conservation, vérifiez que vous n'avez plus besoin du contenu de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7397a-128">Before you remove the hold, be sure that you no longer need the contents in the mailbox.</span></span> <span data-ttu-id="7397a-129">Si vous souhaitez réactiver une boîte aux lettres inactive, vous pouvez la récupérer.</span><span class="sxs-lookup"><span data-stu-id="7397a-129">If you want to reactivate an inactive mailbox, you can recover it.</span></span> <span data-ttu-id="7397a-130">Pour plus d’informations, [voir Récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="7397a-130">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>

- <span data-ttu-id="7397a-131">Pour plus d’informations sur les boîtes aux lettres inactives, consultez [la Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="7397a-131">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>

## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="7397a-132">Étape 1 : Identifier les blocages sur une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7397a-132">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="7397a-133">Comme indiqué précédemment, une conservation pour litige, une In-Place de rétention ou une stratégie de rétention peuvent être placées sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-133">As previously stated, a Litigation Hold, In-Place Hold, or retention policy might be placed on an inactive mailbox.</span></span> <span data-ttu-id="7397a-134">La première étape consiste à identifier les blocages sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-134">The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="7397a-135">Exécutez la commande suivante pour afficher les informations de blocage pour toutes les boîtes aux lettres inactives dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7397a-135">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```powershell
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="7397a-136">La valeur de **True** pour la propriété **LitigationHoldEnabled** indique que la boîte aux lettres inactive est en suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="7397a-136">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold.</span></span> <span data-ttu-id="7397a-137">Si un blocage sur place est placé sur une boîte aux lettres inactive, le GUID du blocage s'affiche comme valeur pour la propriété **InPlaceHolds**.</span><span class="sxs-lookup"><span data-stu-id="7397a-137">If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property.</span></span> <span data-ttu-id="7397a-138">Par exemple, les résultats suivants pour deux boîtes aux lettres inactives indiquent qu’une conservation pour litige est placée sur Ann Beebe et qu’une conservation In-Place et une stratégie de rétention sont placées sur Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="7397a-138">For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that an In-Place Hold and retention policy are placed on Pilar Pinilla.</span></span>
  
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
> <span data-ttu-id="7397a-139">Si un grand nombre In-Place conservations ou stratégies de rétention sont placées sur une boîte aux lettres inactive, tous les In-Place de conservation ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="7397a-139">If a lot of In-Place Holds or retention policies are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed.</span></span> <span data-ttu-id="7397a-140">Vous pouvez exécuter la commande suivante pour afficher tous les GUID dans la propriété InPlaceHolds :  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="7397a-140">You can run the following command to display all the GUIDs in the InPlaceHolds property:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
<span data-ttu-id="7397a-141">Pour plus d’informations sur l’identification des mises en attente, voir Comment identifier le type de mise en attente [placée sur une boîte aux lettres](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="7397a-141">For more information about identify holds, see [How to identify the type of hold placed on a mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="7397a-142">Étape 2 : Supprimer une blocage d'une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7397a-142">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="7397a-p109">Après avoir identifié le type de blocage placé sur la boîte aux lettres inactive (et s'il y a plusieurs blocages), l'étape suivante consiste à supprimer les blocages sur la boîte aux lettres. Comme indiqué précédemment, vous devez supprimer tous les blocages pour supprimer définitivement une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-p109">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox. As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span>
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="7397a-145">Supprimer une suspension pour litige</span><span class="sxs-lookup"><span data-stu-id="7397a-145">Remove a Litigation Hold</span></span>

<span data-ttu-id="7397a-p110">Comme indiqué précédemment, vous devez utiliser Windows PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive. Vous ne pouvez pas utiliser le CAE. Exécutez la commande suivante pour supprimer une suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="7397a-p110">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the EAC. Run the following command to remove a Litigation Hold.</span></span>
  
```powershell
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="7397a-p111">La meilleure façon d'identifier une boîte aux lettres inactive est d'utiliser son nom unique ou sa valeur GUID Exchange. L'une de ces valeurs permet d'empêcher de spécifier par inadvertance la mauvaise boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7397a-p111">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-an-inactive-mailbox-from-a-retention-policy"></a><span data-ttu-id="7397a-151">Supprimer une boîte aux lettres inactive d’une stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="7397a-151">Remove an inactive mailbox from a retention policy</span></span>

<span data-ttu-id="7397a-152">La procédure de suppression d’une boîte aux lettres inactive d’une stratégie Microsoft 365 de rétention dépend de la stratégie de rétention affectée à la boîte aux lettres inactive à l’échelle de l’organisation ou explicite.</span><span class="sxs-lookup"><span data-stu-id="7397a-152">The procedure to remove an inactive mailbox from a Microsoft 365 retention policy depends whether the retention policy assigned to the inactive mailbox is organization-wide or explicit.</span></span> <span data-ttu-id="7397a-153">sur le type de stratégie de rétention qui est affecté à la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-153">on the type of retention policy that's assigned to the inactive mailbox.</span></span>

- <span data-ttu-id="7397a-154">Stratégies de rétention à l’échelle de l’organisation affectées à toutes les boîtes aux lettres de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7397a-154">Organization-wide retention policies assigned to all mailboxes in the organization.</span></span> <span data-ttu-id="7397a-155">Utilisez la cmdlet **Get-OrganizationConfig** dans Exchange Online PowerShell pour obtenir des informations sur les stratégies de rétention à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7397a-155">Use the **Get-OrganizationConfig** cmdlet in Exchange Online PowerShell to get information about organization-wide retention policies.</span></span>

- <span data-ttu-id="7397a-156">Stratégies de rétention d’emplacement spécifiques affectées à des boîtes aux lettres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7397a-156">Specific location retention policies assigned to specific mailboxes.</span></span> <span data-ttu-id="7397a-157">Ce sont des stratégies qui sont affectées aux emplacements de contenu d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7397a-157">These are policies that are assigned to the content locations of specific users.</span></span> <span data-ttu-id="7397a-158">Utilisez la cmdlet **Get-Mailbox -IncludeInactiveMailbox** dans Exchange Online PowerShell pour obtenir des informations sur les stratégies de rétention attribuées à des boîtes aux lettres inactives spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7397a-158">Use the **Get-Mailbox -IncludeInactiveMailbox** cmdlet in Exchange Online PowerShell to get information about retention policies assigned to specific inactive mailboxes.</span></span>

#### <a name="remove-an-inactive-mailbox-from-an-organization-wide-retention-policy"></a><span data-ttu-id="7397a-159">Supprimer une boîte aux lettres inactive d’une stratégie de rétention à l’échelle de l’organisation</span><span class="sxs-lookup"><span data-stu-id="7397a-159">Remove an inactive mailbox from an organization-wide retention policy</span></span>

<span data-ttu-id="7397a-160">Exécutez la commande suivante dans Exchange Online PowerShell pour exclure une boîte aux lettres inactive d’une stratégie de rétention à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7397a-160">Run the following command in Exchange Online PowerShell to exclude an inactive mailbox from an organization-wide retention policy.</span></span>

```powershell
Set-Mailbox <identity of inactive mailbox> -ExcludeFromOrgHolds <retention policy GUID without prefix or suffix>
```

<span data-ttu-id="7397a-161">Pour plus d’informations sur l’identification des stratégies de rétention à l’échelle de l’organisation appliquées à une boîte aux lettres inactive et l’obtention du GUID d’une stratégie de rétention, consultez la section « Get-OrganizationConfig » dans Comment identifier le [type](identify-a-hold-on-an-exchange-online-mailbox.md#get-organizationconfig)de conservation placé sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7397a-161">For more information identifying organization-wide retention policies applied to an inactive mailbox and obtaining the GUID for a retention policy, see the "Get-OrganizationConfig" section in [How to identify the type of hold placed on a mailbox](identify-a-hold-on-an-exchange-online-mailbox.md#get-organizationconfig).</span></span>

<span data-ttu-id="7397a-162">Vous pouvez également exécuter la commande suivante pour supprimer la boîte aux lettres inactive de toutes les stratégies à l’échelle de l’organisation :</span><span class="sxs-lookup"><span data-stu-id="7397a-162">Alternatively, you can run the following command to remove the inactive mailbox from all organization-wide policies:</span></span>

```powershell
Set-Mailbox <identity of inactive mailbox> -ExcludeFromAllOrgHolds
```

#### <a name="remove-an-inactive-mailbox-from-a-specific-location-retention-policy"></a><span data-ttu-id="7397a-163">Supprimer une boîte aux lettres inactive d’une stratégie de rétention d’emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="7397a-163">Remove an inactive mailbox from a specific location retention policy</span></span>

<span data-ttu-id="7397a-164">Exécutez la commande suivante dans [le Centre de sécurité & conformité PowerShell](/powershell/exchange/connect-to-scc-powershell) pour supprimer une boîte aux lettres inactive d’une stratégie de rétention explicite.</span><span class="sxs-lookup"><span data-stu-id="7397a-164">Run the following command in [Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) to remove an inactive mailbox from an explicit retention policy.</span></span>

```powershell
Set-RetentionCompliancePolicy -Identity <retention policy GUID without prefix or suffix> -AddExchangeLocationException <identity of inactive mailbox>
```

<span data-ttu-id="7397a-165">Pour plus d’informations sur l’identification des stratégies de rétention d’emplacement spécifiques appliquées à une boîte aux lettres inactive et l’obtention du GUID d’une stratégie de rétention, consultez la section « Get-Mailbox » dans Comment identifier le [type](identify-a-hold-on-an-exchange-online-mailbox.md#get-mailbox)de conservation placé sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7397a-165">For more information identifying specific location retention policies applied to an inactive mailbox and obtaining the GUID for a retention policy, see the "Get-Mailbox" section in [How to identify the type of hold placed on a mailbox](identify-a-hold-on-an-exchange-online-mailbox.md#get-mailbox).</span></span>

### <a name="remove-in-place-holds"></a><span data-ttu-id="7397a-166">Supprimer des blocages sur place</span><span class="sxs-lookup"><span data-stu-id="7397a-166">Remove In-Place Holds</span></span>

 <span data-ttu-id="7397a-167">Il existe deux façons de supprimer un blocage sur place à partir d'une boîte aux lettres inactive :</span><span class="sxs-lookup"><span data-stu-id="7397a-167">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="7397a-168">**Supprimez lIn-Place hold .**</span><span class="sxs-lookup"><span data-stu-id="7397a-168">**Delete the In-Place Hold object**.</span></span> <span data-ttu-id="7397a-169">Si la boîte aux lettres inactive que vous souhaitez supprimer définitivement est la seule boîte aux lettres source pour une In-Place, vous pouvez simplement supprimer l’objet In-Place hold.</span><span class="sxs-lookup"><span data-stu-id="7397a-169">If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="7397a-p116">Vous devez désactiver le blocage avant de pouvoir supprimer un objet de blocage sur place. Si vous essayez de supprimer un objet de blocage sur place ayant le blocage activé, vous recevrez un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="7397a-p116">You have to disable the hold before you can delete an In-Place Hold object. If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="7397a-172">**Supprimez la boîte aux lettres inactive en tant que boîte aux lettres source d’une In-Place en attente.**</span><span class="sxs-lookup"><span data-stu-id="7397a-172">**Remove the inactive mailbox as a source mailbox of an In-Place Hold**.</span></span> <span data-ttu-id="7397a-173">Si vous souhaitez conserver d’autres boîtes aux lettres source pour une In-Place, vous pouvez supprimer la boîte aux lettres inactive de la liste des boîtes aux lettres source et conserver l’objet In-Place Hold.</span><span class="sxs-lookup"><span data-stu-id="7397a-173">If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span>

#### <a name="delete-an-in-place-hold"></a><span data-ttu-id="7397a-174">Supprimer une In-Place en attente</span><span class="sxs-lookup"><span data-stu-id="7397a-174">Delete an In-Place Hold</span></span>

1. <span data-ttu-id="7397a-p118">Créez une variable qui contient les propriétés du blocage sur place à supprimer. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="7397a-p118">Create a variable that contains the properties of the In-Place Hold that you want to delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

   ```powershell
   $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
   ```

2. <span data-ttu-id="7397a-177">Désactivez le blocage sur le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="7397a-177">Disable the hold on the In-Place Hold.</span></span>

   ```powershell
   Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
   ```

3. <span data-ttu-id="7397a-178">Supprimez le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="7397a-178">Delete the In-Place Hold.</span></span>

   ```powershell
   Remove-MailboxSearch $InPlaceHold.Name
   ```

#### <a name="remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="7397a-179">Supprimer une boîte aux lettres inactive d’une In-Place en attente</span><span class="sxs-lookup"><span data-stu-id="7397a-179">Remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="7397a-180">Si le blocage sur place contient un grand nombre de boîtes aux lettres source, il est possible que la boîte aux lettres inactive ne soit pas répertoriée sur la page **Sources** dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="7397a-180">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC.</span></span> <span data-ttu-id="7397a-181">Jusqu'à 3 000 boîtes aux lettres s'affichent sur la page **Sources** lorsque vous modifiez un blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="7397a-181">Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold.</span></span> <span data-ttu-id="7397a-182">Si une boîte aux lettres inactive n’est pas répertoriée dans la page **Sources,** vous pouvez utiliser Exchange Online PowerShell pour la supprimer de la In-Place en attente.</span><span class="sxs-lookup"><span data-stu-id="7397a-182">If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="7397a-p120">Créez une variable qui contient les propriétés du blocage sur place placé sur la boîte aux lettres inactive. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="7397a-p120">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```powershell
    $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
    ```

2. <span data-ttu-id="7397a-185">Vérifiez que la boîte aux lettres inactive est répertoriée comme une boîte aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="7397a-185">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 

   ```powershell
   $InPlaceHold.Sources
   ```

   > [!NOTE]
   > <span data-ttu-id="7397a-p121">La propriété *Sources* du blocage sur place identifie les boîtes aux lettres source par leurs propriétés *LegacyExchangeDN*. Étant donné que cette propriété identifie les boîtes aux lettres inactives de façon unique, l'utilisation de la propriété *Sources* du blocage sur place permet d'empêcher la suppression de la boîte aux lettres incorrecte. Cela permet également d'éviter les problèmes si deux boîtes aux lettres ont le même alias ou la même adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="7397a-p121">The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties. Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox. This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 

3. <span data-ttu-id="7397a-p122">Supprimez la boîte aux lettres inactive dans la liste des boîtes aux lettres sources dans la variable. Veillez à utiliser le **LegacyExchangeDN** de la boîte aux lettres inactive qui est renvoyé par la commande à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="7397a-p122">Remove the inactive mailbox from the list of source mailboxes in the variable. Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 

    ```powershell
    $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
    ```

    <span data-ttu-id="7397a-191">Par exemple, la commande suivante supprime la boîte aux lettres inactive pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="7397a-191">For example, the following command removes the inactive mailbox for Pilar Pinilla.</span></span>

    ```powershell
    $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/ cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
    ```

4. <span data-ttu-id="7397a-192">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source dans la variable.</span><span class="sxs-lookup"><span data-stu-id="7397a-192">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>

   ```powershell
   $InPlaceHold.Sources
   ```

5. <span data-ttu-id="7397a-193">Modifiez le blocage sur place avec la liste mise à jour des boîtes aux lettres source, qui n'inclut pas la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-193">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>

   ```powershell
   Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
   ```

6. <span data-ttu-id="7397a-194">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="7397a-194">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>

   ```powershell
   Get-MailboxSearch $InPlaceHold.Name | FL Sources
   ```

## <a name="more-information"></a><span data-ttu-id="7397a-195">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7397a-195">More information</span></span>

- <span data-ttu-id="7397a-196">**Une boîte aux lettres inactive est un type de boîte aux lettres supprimée (récupérable).**</span><span class="sxs-lookup"><span data-stu-id="7397a-196">**An inactive mailbox is a type of soft-deleted mailbox.**</span></span> <span data-ttu-id="7397a-197">Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique.</span><span class="sxs-lookup"><span data-stu-id="7397a-197">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period.</span></span> <span data-ttu-id="7397a-198">Une boîte aux lettres précédemment inactive sera disponible en tant que boîte aux lettres supprimée (Exchange Online pendant 183 jours).</span><span class="sxs-lookup"><span data-stu-id="7397a-198">A previously inactive mailbox will be available as a soft-deleted mailbox in Exchange Online for 183 days.</span></span> <span data-ttu-id="7397a-199">Cela signifie que la boîte aux lettres peut être récupérée dans les 183 jours suivant sa suppression (récupérez-la).</span><span class="sxs-lookup"><span data-stu-id="7397a-199">This means that the mailbox can be recovered within 183 days of being soft-deleted.</span></span> <span data-ttu-id="7397a-200">Après 183 jours, une boîte aux lettres supprimée (récupération) est marquée pour suppression définitive et ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="7397a-200">After 183 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span>

- <span data-ttu-id="7397a-201">**Que se passe-t-il après avoir supprimé la conservation sur une boîte aux lettres inactive ?**</span><span class="sxs-lookup"><span data-stu-id="7397a-201">**What happens after you remove the hold on an inactive mailbox?**</span></span> <span data-ttu-id="7397a-202">La boîte aux lettres est traitée comme d’autres boîtes aux lettres supprimées (suppression temporaire) et est marquée pour suppression définitive après l’expiration de la période de rétention de 183 jours.</span><span class="sxs-lookup"><span data-stu-id="7397a-202">The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 183-day soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="7397a-203">Ce délai de rétention commence à la date à laquelle la boîte aux lettres a été rendue inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7397a-203">This retention period starts on the date when the mailbox was first made inactive.</span></span> <span data-ttu-id="7397a-204">Cette date est appelée date de suppression (suppression possible), qui correspond à la date à laquelle le compte d’utilisateur correspondant a été supprimé ou à laquelle la boîte aux lettres Exchange Online a été supprimée avec la cmdlet **Remove-Mailbox.**</span><span class="sxs-lookup"><span data-stu-id="7397a-204">This date is known as the soft-deleted date, which is the date the corresponding user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet.</span></span> <span data-ttu-id="7397a-205">La date supprimée (récupérable) n'est pas la date de suppression du blocage.</span><span class="sxs-lookup"><span data-stu-id="7397a-205">The soft-deleted date isn't the date on which you remove the hold.</span></span>

- <span data-ttu-id="7397a-206">**Une boîte aux lettres inactive est-elle définitivement supprimée immédiatement après la suppression de la conservation ?**</span><span class="sxs-lookup"><span data-stu-id="7397a-206">**Is an inactive mailbox permanently deleted immediately after the hold is removed?**</span></span> <span data-ttu-id="7397a-207">Une boîte aux lettres auparavant inactive sera disponible à l’état supprimé (suppression possible) pendant 183 jours.</span><span class="sxs-lookup"><span data-stu-id="7397a-207">A formerly inactive mailbox will be available in the soft-deleted state for 183 days.</span></span> <span data-ttu-id="7397a-208">Après 183 jours, la boîte aux lettres est marquée pour suppression définitive.</span><span class="sxs-lookup"><span data-stu-id="7397a-208">After 183 days the mailbox will be marked for permanent deletion.</span></span>

- <span data-ttu-id="7397a-209">**Comment afficher des informations sur une boîte aux lettres inactive après la suppression de la conservation ?**</span><span class="sxs-lookup"><span data-stu-id="7397a-209">**How do you display information about an inactive mailbox after the hold is removed?**</span></span> <span data-ttu-id="7397a-210">Une fois qu’une boîte aux lettres inactive a été supprimée et que la boîte aux lettres inactive est revenir à une boîte aux lettres supprimée (suppression réverable), elle ne sera pas renvoyée à l’aide du paramètre *InactiveMailboxOnly* avec la cmdlet **Get-Mailbox.**</span><span class="sxs-lookup"><span data-stu-id="7397a-210">After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet.</span></span> <span data-ttu-id="7397a-211">Cependant, vous pouvez afficher des informations sur la boîte aux lettres à l'aide de la commande **Get-Mailbox -SoftDeletedMailbox**.</span><span class="sxs-lookup"><span data-stu-id="7397a-211">But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command.</span></span> <span data-ttu-id="7397a-212">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7397a-212">For example:</span></span>

  ```text
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox,WasInactiveMailbox,InactiveMailboxRetireTime
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 6/16/2020 1:19:04 AM
  IsInactiveMailbox      : False
  WasInactiveMailbox     : True
  InactiveMailboxRetireTime : 9/30/2020 11:16:23 PM
  ```

  <span data-ttu-id="7397a-213">Dans l’exemple ci-dessus, la *propriété WhenSoftDeleted* identifie la date supprimée (supprimée (supprimé(s) (supprimé(s) (dans cet exemple) : 16 juin 2020.</span><span class="sxs-lookup"><span data-stu-id="7397a-213">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is June 16, 2020.</span></span> <span data-ttu-id="7397a-214">La *propriété WasInactiveMailbox est* répertoriée comme étant une boîte aux lettres `True` inactive.</span><span class="sxs-lookup"><span data-stu-id="7397a-214">The *WasInactiveMailbox* property is listed as `True` because it was previously an inactive mailbox.</span></span> <span data-ttu-id="7397a-215">La boîte aux lettres sera définitivement supprimée 183 jours après le 30 septembre 2020.</span><span class="sxs-lookup"><span data-stu-id="7397a-215">The mailbox will be permanently deleted 183 days after September 30, 2020.</span></span>

