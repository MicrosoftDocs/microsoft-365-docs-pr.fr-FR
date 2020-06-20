---
title: Suppression d’une boîte aux lettres inactive
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
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
ms.openlocfilehash: 05357ce1b3e10394854844f15ec6a18c1c427d5b
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817893"
---
# <a name="delete-an-inactive-mailbox"></a><span data-ttu-id="a88c9-103">Suppression d’une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="a88c9-103">Delete an inactive mailbox</span></span>

<span data-ttu-id="a88c9-104">Une boîte aux lettres inactive est utilisée pour conserver le courrier électronique d'un ancien employé une fois qu'il quitte votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a88c9-104">An inactive mailbox is used to preserve a former employee's email after he or she leaves your organization.</span></span> <span data-ttu-id="a88c9-105">Si vous n'avez plus besoin du contenu d'une boîte aux lettres inactive, vous pouvez le supprimer de façon définitive en supprimant le blocage.</span><span class="sxs-lookup"><span data-stu-id="a88c9-105">When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold.</span></span> <span data-ttu-id="a88c9-106">En outre, il est possible que plusieurs blocages soient placés sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-106">Also, it's possible that multiple holds might be placed on an inactive mailbox.</span></span> <span data-ttu-id="a88c9-107">Par exemple, une boîte aux lettres inactive peut être placée en suspension pour litige et sur une ou plusieurs blocages sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-107">For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds.</span></span> <span data-ttu-id="a88c9-108">En outre, une stratégie de rétention (créée dans le centre de sécurité et de conformité dans Office 365 ou Microsoft 365) peut être appliquée à la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-108">Additionally, a retention policy (created in the security and compliance center in Office 365 or Microsoft 365) might be applied to the inactive mailbox.</span></span> <span data-ttu-id="a88c9-109">Vous devez supprimer toutes les suspensions et stratégies de rétention d’une boîte aux lettres inactive pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="a88c9-109">You have to remove all holds and retention policies from an inactive mailbox to delete it.</span></span> <span data-ttu-id="a88c9-110">Une fois que vous avez supprimé les suspensions et les stratégies de rétention, la boîte aux lettres inactive est marquée pour suppression et est définitivement supprimée après traitement.</span><span class="sxs-lookup"><span data-stu-id="a88c9-110">After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a88c9-111">À mesure que nous continuons à investir de différentes manières pour conserver le contenu de la boîte aux lettres, nous annonçaons le retrait des conservations inaltérables dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="a88c9-111">As we continue to invest in different ways to preserve mailbox content, we're announcing the retirement of In-Place Holds in the Exchange admin center.</span></span> <span data-ttu-id="a88c9-112">Cela signifie que vous devez utiliser des conservations pour litige et des stratégies de rétention pour créer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-112">That means you should use Litigation Holds and retention policies to create an inactive mailbox.</span></span> <span data-ttu-id="a88c9-113">À partir du 1er juillet 2020 vous ne pourrez pas créer de nouvelles conservations inaltérables dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a88c9-113">Starting July 1, 2020 you won't be able to create new In-Place Holds in Exchange Online.</span></span> <span data-ttu-id="a88c9-114">Toutefois, vous pourrez toujours modifier la durée de conservation d’un blocage sur place placé sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-114">But you'll still be able to change the hold duration of an In-Place Hold placed on an inactive mailbox.</span></span> <span data-ttu-id="a88c9-115">Toutefois, à partir du 1er octobre 2020, vous ne pourrez pas modifier la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="a88c9-115">However, starting October 1, 2020, you won't be able to change the hold duration.</span></span> <span data-ttu-id="a88c9-116">Vous ne pourrez supprimer une boîte aux lettres inactive qu’en supprimant la conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="a88c9-116">You'll only be able to delete an inactive mailbox by removing the In-Place Hold.</span></span> <span data-ttu-id="a88c9-117">Les boîtes aux lettres inactives existantes qui sont en conservation inaltérable resteront conservées jusqu’à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="a88c9-117">Existing inactive mailboxes that are on In-Place Hold will still be preserved until the hold is removed.</span></span> <span data-ttu-id="a88c9-118">Pour plus d’informations sur le retrait des conservations inaltérables, consultez la rubrique [déclassement des outils eDiscovery hérités](legacy-ediscovery-retirement.md).</span><span class="sxs-lookup"><span data-stu-id="a88c9-118">For more information about the retirement of In-Place Holds, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md).</span></span>
  
<span data-ttu-id="a88c9-119">Consultez la section [Plus d'informations](#more-information) pour obtenir une description de ce qui se produit après la suppression des blocages d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-119">See the [More information](#more-information) section for a description of what happens after holds are removed from an inactive mailbox.</span></span>
  
## <a name="before-you-delete-an-inactive-mailbox"></a><span data-ttu-id="a88c9-120">Avant de supprimer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="a88c9-120">Before you delete an inactive mailbox</span></span>

- <span data-ttu-id="a88c9-121">Vous devez utiliser Exchange Online PowerShell pour supprimer une suspension pour litige d’une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-121">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="a88c9-122">Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="a88c9-122">You can't use the Exchange admin center (EAC).</span></span> <span data-ttu-id="a88c9-123">Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="a88c9-123">For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span></span> <span data-ttu-id="a88c9-124">Vous pouvez utiliser Exchange Online PowerShell ou le centre d’administration Exchange pour supprimer un blocage sur place d’une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-124">You can use Exchange Online PowerShell or the EAC to remove an In-Place Hold from an inactive mailbox.</span></span> 
    
- <span data-ttu-id="a88c9-125">Vous pouvez copier le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres avant de supprimer la conservation et de supprimer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-125">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox.</span></span> <span data-ttu-id="a88c9-126">Pour plus d’informations, consultez la rubrique [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="a88c9-126">For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="a88c9-127">Si vous supprimez la stratégie de blocage ou de rétention d’une boîte aux lettres inactive et que la période de rétention de boîte aux lettres supprimée (récupérable) a expiré, la boîte aux lettres sera définitivement supprimée.</span><span class="sxs-lookup"><span data-stu-id="a88c9-127">If you remove the hold or retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted.</span></span> <span data-ttu-id="a88c9-128">Après sa suppression, elle ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="a88c9-128">After it's deleted, it can't be recovered.</span></span> <span data-ttu-id="a88c9-129">Avant de supprimer la conservation, vérifiez que vous n'avez plus besoin du contenu de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a88c9-129">Before you remove the hold, be sure that you no longer need the contents in the mailbox.</span></span> <span data-ttu-id="a88c9-130">Si vous souhaitez réactiver une boîte aux lettres inactive, vous pouvez la récupérer.</span><span class="sxs-lookup"><span data-stu-id="a88c9-130">If you want to re-activate an inactive mailbox, you can recover it.</span></span> <span data-ttu-id="a88c9-131">Pour plus d’informations, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="a88c9-131">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="a88c9-132">Pour plus d’informations sur les boîtes aux lettres inactives, consultez la rubrique [inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="a88c9-132">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="a88c9-133">Étape 1 : Identifier les blocages sur une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="a88c9-133">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="a88c9-134">Comme indiqué précédemment, la conservation pour litige, la conservation inaltérable ou la stratégie de rétention peuvent être placées sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-134">As previously stated, a Litigation Hold, In-Place Hold, or retention policy might be placed on an inactive mailbox.</span></span> <span data-ttu-id="a88c9-135">La première étape consiste à identifier les blocages sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-135">The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="a88c9-136">Exécutez la commande suivante pour afficher les informations de blocage pour toutes les boîtes aux lettres inactives dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a88c9-136">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```powershell
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="a88c9-137">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold.</span><span class="sxs-lookup"><span data-stu-id="a88c9-137">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold.</span></span> <span data-ttu-id="a88c9-138">If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property.</span><span class="sxs-lookup"><span data-stu-id="a88c9-138">If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property.</span></span> <span data-ttu-id="a88c9-139">For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that two In-Place Holds are placed on Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="a88c9-139">For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that two In-Place Holds are placed on Pilar Pinilla.</span></span> 
  
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
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> <span data-ttu-id="a88c9-140">Si un grand nombre de blocages sur place est placé sur une boîte aux lettres inactive, tous les GUID de blocage sur place ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="a88c9-140">If a lot of In-Place Holds are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed.</span></span> <span data-ttu-id="a88c9-141">Vous pouvez exécuter la commande suivante pour afficher tous les GUID de conservation inaltérable :`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="a88c9-141">You can run the following command to display all the In-Place Hold GUIDs:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="a88c9-142">Étape 2 : Supprimer une blocage d'une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="a88c9-142">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="a88c9-143">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox.</span><span class="sxs-lookup"><span data-stu-id="a88c9-143">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox.</span></span> <span data-ttu-id="a88c9-144">As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="a88c9-144">As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span> 
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="a88c9-145">Supprimer une suspension pour litige</span><span class="sxs-lookup"><span data-stu-id="a88c9-145">Remove a Litigation Hold</span></span>

<span data-ttu-id="a88c9-146">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="a88c9-146">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="a88c9-147">You can't use the EAC.</span><span class="sxs-lookup"><span data-stu-id="a88c9-147">You can't use the EAC.</span></span> <span data-ttu-id="a88c9-148">Run the following command to remove a Litigation Hold.</span><span class="sxs-lookup"><span data-stu-id="a88c9-148">Run the following command to remove a Litigation Hold.</span></span>
  
```powershell
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="a88c9-149">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value.</span><span class="sxs-lookup"><span data-stu-id="a88c9-149">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value.</span></span> <span data-ttu-id="a88c9-150">Using one of these values helps prevent accidentally specifying the wrong mailbox.</span><span class="sxs-lookup"><span data-stu-id="a88c9-150">Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-in-place-holds"></a><span data-ttu-id="a88c9-151">Supprimer des blocages sur place</span><span class="sxs-lookup"><span data-stu-id="a88c9-151">Remove In-Place Holds</span></span>

 <span data-ttu-id="a88c9-152">Il existe deux façons de supprimer un blocage sur place à partir d'une boîte aux lettres inactive :</span><span class="sxs-lookup"><span data-stu-id="a88c9-152">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="a88c9-153">**Supprimer l’objet de conservation** inaltérable Si la boîte aux lettres inactive que vous souhaitez supprimer définitivement est la seule boîte aux lettres source pour une conservation inaltérable, vous pouvez simplement supprimer l’objet de blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-153">**Delete the In-Place Hold object** If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="a88c9-154">You have to disable the hold before you can delete an In-Place Hold object.</span><span class="sxs-lookup"><span data-stu-id="a88c9-154">You have to disable the hold before you can delete an In-Place Hold object.</span></span> <span data-ttu-id="a88c9-155">If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span><span class="sxs-lookup"><span data-stu-id="a88c9-155">If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="a88c9-156">**Supprimer la boîte aux lettres inactive comme boîte aux lettres source d'une conservation inaltérable** Si vous souhaitez conserver d'autres boîtes aux lettres sources pour une conservation inaltérable, vous pouvez supprimer la boîte aux lettres inactive de la liste des boîtes aux lettres sources et conserver l'objet de conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="a88c9-156">**Remove the inactive mailbox as a source mailbox of an In-Place Hold** If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span> 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a><span data-ttu-id="a88c9-157">Utiliser le Centre d'administration Exchange (CAE) pour supprimer un blocage sur place</span><span class="sxs-lookup"><span data-stu-id="a88c9-157">Use the EAC to delete an In-Place Hold</span></span>

1. <span data-ttu-id="a88c9-158">If you know the name of the In-Place Hold that you want to delete, you can go to the next step.</span><span class="sxs-lookup"><span data-stu-id="a88c9-158">If you know the name of the In-Place Hold that you want to delete, you can go to the next step.</span></span> <span data-ttu-id="a88c9-159">Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox that you want to permanently delete.</span><span class="sxs-lookup"><span data-stu-id="a88c9-159">Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox that you want to permanently delete.</span></span> <span data-ttu-id="a88c9-160">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="a88c9-160">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
   ```powershell
   Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
   ```

2. <span data-ttu-id="a88c9-161">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span><span class="sxs-lookup"><span data-stu-id="a88c9-161">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="a88c9-162">Sélectionnez la conservation inaltérable à supprimer, puis cliquez sur **modifier** l' ![ icône modifier ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) .</span><span class="sxs-lookup"><span data-stu-id="a88c9-162">Select the In-Place Hold you want to delete, and then click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="a88c9-163">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="a88c9-163">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span></span>
    
5. <span data-ttu-id="a88c9-164">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span><span class="sxs-lookup"><span data-stu-id="a88c9-164">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](../media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>
    
6. <span data-ttu-id="a88c9-165">Dans le message d'avertissement, cliquez sur **Oui** pour supprimer le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-165">On the warning, click **Yes** to delete the In-Place Hold.</span></span> 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a><span data-ttu-id="a88c9-166">Utiliser Exchange Online PowerShell pour supprimer une conservation inaltérable</span><span class="sxs-lookup"><span data-stu-id="a88c9-166">Use Exchange Online PowerShell to delete an In-Place Hold</span></span>

1. <span data-ttu-id="a88c9-167">Create a variable that contains the properties of the In-Place Hold that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="a88c9-167">Create a variable that contains the properties of the In-Place Hold that you want to delete.</span></span> <span data-ttu-id="a88c9-168">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="a88c9-168">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
   ```powershell
   $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
   ```

2. <span data-ttu-id="a88c9-169">Désactivez le blocage sur le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-169">Disable the hold on the In-Place Hold.</span></span>
    
   ```powershell
   Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
   ```

3. <span data-ttu-id="a88c9-170">Supprimez le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-170">Delete the In-Place Hold.</span></span>
    
   ```powershell
   Remove-MailboxSearch $InPlaceHold.Name
   ```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="a88c9-171">Utilisez le CAE pour supprimer une boîte aux lettres inactive d'un blocage sur place</span><span class="sxs-lookup"><span data-stu-id="a88c9-171">Use the EAC to remove an inactive mailbox from an In-Place Hold</span></span>

1. <span data-ttu-id="a88c9-172">If you know the name of the In-Place Hold that's placed on the inactive mailbox, you can go to the next step.</span><span class="sxs-lookup"><span data-stu-id="a88c9-172">If you know the name of the In-Place Hold that's placed on the inactive mailbox, you can go to the next step.</span></span> <span data-ttu-id="a88c9-173">Otherwise, run the following command to get the name of the In-Place Hold placed on the mailbox.</span><span class="sxs-lookup"><span data-stu-id="a88c9-173">Otherwise, run the following command to get the name of the In-Place Hold placed on the mailbox.</span></span> <span data-ttu-id="a88c9-174">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="a88c9-174">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
   ```powershell
   Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
   ```

2. <span data-ttu-id="a88c9-175">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span><span class="sxs-lookup"><span data-stu-id="a88c9-175">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="a88c9-176">Sélectionnez le blocage sur place placé sur la boîte aux lettres inactive, puis cliquez sur **modifier** l' ![ icône modifier ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) .</span><span class="sxs-lookup"><span data-stu-id="a88c9-176">Select the In-Place Hold that is placed on the inactive mailbox, and then click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="a88c9-177">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span><span class="sxs-lookup"><span data-stu-id="a88c9-177">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span></span>
    
5. <span data-ttu-id="a88c9-178">Dans la liste des boîtes aux lettres source, cliquez sur le nom de la boîte aux lettres inactive à supprimer, puis cliquez sur **Supprimer**![Icône Suppression](../media/adf01106-cc79-475c-8673-065371c1897b.gif).</span><span class="sxs-lookup"><span data-stu-id="a88c9-178">In the list of source mailboxes, click the name of the inactive mailbox that you want to remove, and then click **Remove**![Remove icon](../media/adf01106-cc79-475c-8673-065371c1897b.gif).</span></span>
    
6. <span data-ttu-id="a88c9-179">Click **Save** to save the change.</span><span class="sxs-lookup"><span data-stu-id="a88c9-179">Click **Save** to save the change.</span></span> <span data-ttu-id="a88c9-180">A message is displayed saying the operation was successfully completed.</span><span class="sxs-lookup"><span data-stu-id="a88c9-180">A message is displayed saying the operation was successfully completed.</span></span> 
    
7. <span data-ttu-id="a88c9-181">Répétez les étapes 1 à 6 pour supprimer d'autres blocages sur place placés sur la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-181">Repeat steps 1 through 6 to remove other In-Place Holds placed on the inactive mailbox.</span></span>
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="a88c9-182">Utiliser Exchange Online PowerShell pour supprimer une boîte aux lettres inactive d’une conservation inaltérable</span><span class="sxs-lookup"><span data-stu-id="a88c9-182">Use Exchange Online PowerShell to remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="a88c9-183">Si le blocage sur place contient un grand nombre de boîtes aux lettres source, il est possible que la boîte aux lettres inactive ne soit pas répertoriée sur la page **Sources** dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="a88c9-183">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC.</span></span> <span data-ttu-id="a88c9-184">Jusqu'à 3 000 boîtes aux lettres s'affichent sur la page **Sources** lorsque vous modifiez un blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-184">Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold.</span></span> <span data-ttu-id="a88c9-185">Si une boîte aux lettres inactive n’est pas affichée sur la page **sources** , vous pouvez utiliser Exchange Online PowerShell pour la supprimer de la conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="a88c9-185">If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="a88c9-186">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="a88c9-186">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox.</span></span> <span data-ttu-id="a88c9-187">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="a88c9-187">Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
    ```powershell
    $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
    ```

2. <span data-ttu-id="a88c9-188">Vérifiez que la boîte aux lettres inactive est répertoriée comme une boîte aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-188">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 
    
   ```powershell
   $InPlaceHold.Sources
   ```

   <span data-ttu-id="a88c9-189">**Remarque :** La propriété *sources* de la conservation inaltérable identifie les boîtes aux lettres source en fonction de leurs propriétés *legacyExchangeDN* .</span><span class="sxs-lookup"><span data-stu-id="a88c9-189">**Note:** The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties.</span></span> <span data-ttu-id="a88c9-190">Étant donné que cette propriété identifie les boîtes aux lettres inactives de façon unique, l'utilisation de la propriété *Sources* du blocage sur place permet d'empêcher la suppression de la boîte aux lettres incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a88c9-190">Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox.</span></span> <span data-ttu-id="a88c9-191">Cela permet également d'éviter les problèmes si deux boîtes aux lettres ont le même alias ou la même adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="a88c9-191">This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 
   
3. <span data-ttu-id="a88c9-192">Remove the inactive mailbox from the list of source mailboxes in the variable.</span><span class="sxs-lookup"><span data-stu-id="a88c9-192">Remove the inactive mailbox from the list of source mailboxes in the variable.</span></span> <span data-ttu-id="a88c9-193">Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span><span class="sxs-lookup"><span data-stu-id="a88c9-193">Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 
    
    ```powershell
    $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
    ```

    <span data-ttu-id="a88c9-194">Par exemple, la commande suivante supprime la boîte aux lettres inactive pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="a88c9-194">For example, the following command removes the inactive mailbox for Pilar Pinilla.</span></span>
    
    ```powershell
    $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/ cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
    ```

4. <span data-ttu-id="a88c9-195">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source dans la variable.</span><span class="sxs-lookup"><span data-stu-id="a88c9-195">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>
    
   ```powershell
   $InPlaceHold.Sources
   ```

5. <span data-ttu-id="a88c9-196">Modifiez le blocage sur place avec la liste mise à jour des boîtes aux lettres source, qui n'inclut pas la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-196">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>
    
   ```powershell
   Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
   ```

6. <span data-ttu-id="a88c9-197">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="a88c9-197">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>
    
   ```powershell
   Get-MailboxSearch $InPlaceHold.Name | FL Sources
   ```

## <a name="more-information"></a><span data-ttu-id="a88c9-198">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a88c9-198">More information</span></span>

- <span data-ttu-id="a88c9-199">**An inactive mailbox is a type of soft-deleted mailbox.**</span><span class="sxs-lookup"><span data-stu-id="a88c9-199">**An inactive mailbox is a type of soft-deleted mailbox.**</span></span> <span data-ttu-id="a88c9-200">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period.</span><span class="sxs-lookup"><span data-stu-id="a88c9-200">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period.</span></span> <span data-ttu-id="a88c9-201">The soft-deleted mailbox retention period in Exchange Online is 30 days.</span><span class="sxs-lookup"><span data-stu-id="a88c9-201">The soft-deleted mailbox retention period in Exchange Online is 30 days.</span></span> <span data-ttu-id="a88c9-202">This means that the mailbox can be recovered within 30 days of being soft-deleted.</span><span class="sxs-lookup"><span data-stu-id="a88c9-202">This means that the mailbox can be recovered within 30 days of being soft-deleted.</span></span> <span data-ttu-id="a88c9-203">After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span><span class="sxs-lookup"><span data-stu-id="a88c9-203">After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span> 
    
- <span data-ttu-id="a88c9-204">**Que se passe-t-il après avoir supprimé la conservation sur une boîte aux lettres inactive ?**</span><span class="sxs-lookup"><span data-stu-id="a88c9-204">**What happens after you remove the hold on an inactive mailbox?**</span></span> <span data-ttu-id="a88c9-205">La boîte aux lettres est traitée comme d'autres boîtes aux lettres supprimées (récupérables) et est marquée pour suppression définitive après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable) de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a88c9-205">The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 30-day soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="a88c9-206">Ce délai de rétention commence à la date à laquelle la boîte aux lettres a été rendue inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="a88c9-206">This retention period starts on the date when the mailbox was first made inactive.</span></span> <span data-ttu-id="a88c9-207">Cette date est appelée date de suppression récupérable, qui correspond à la date à laquelle le compte d’utilisateur correspondant a été supprimé ou lorsque la boîte aux lettres Exchange Online a été supprimée à l’aide de la cmdlet **Remove-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="a88c9-207">This date is known as the soft-deleted date, which is the date the corresponding user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet.</span></span> <span data-ttu-id="a88c9-208">La date supprimée (récupérable) n'est pas la date de suppression du blocage.</span><span class="sxs-lookup"><span data-stu-id="a88c9-208">The soft-deleted date isn't the date on which you remove the hold.</span></span> 
    
- <span data-ttu-id="a88c9-209">**Is an inactive mailbox permanently deleted immediately after the hold is removed?**</span><span class="sxs-lookup"><span data-stu-id="a88c9-209">**Is an inactive mailbox permanently deleted immediately after the hold is removed?**</span></span> <span data-ttu-id="a88c9-210">If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold.</span><span class="sxs-lookup"><span data-stu-id="a88c9-210">If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold.</span></span> <span data-ttu-id="a88c9-211">The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span><span class="sxs-lookup"><span data-stu-id="a88c9-211">The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span></span> 
    
- <span data-ttu-id="a88c9-212">**Quel est l'impact de la période de rétention de la boîte aux lettres supprimée (récupérable) sur les boîtes aux lettres inactives ?**</span><span class="sxs-lookup"><span data-stu-id="a88c9-212">**How does the soft-deleted mailbox retention period affect inactive mailboxes?**</span></span> <span data-ttu-id="a88c9-213">Si la date supprimée (récupérable) pour une boîte aux lettres inactive se situe plus de 30 jours avant la date de la suppression de la conservation, la boîte aux lettres est marquée pour suppression définitive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-213">If the soft-deleted date for an inactive mailbox is more than 30 days before the date the hold was removed, the mailbox is marked for permanent deletion.</span></span> <span data-ttu-id="a88c9-214">Par contre, si la date supprimée (récupérable) d'une boîte aux lettres inactive se situe dans les 30 derniers jours et que vous supprimez la conservation, vous pouvez récupérer la boîte aux lettres jusqu'à l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable).</span><span class="sxs-lookup"><span data-stu-id="a88c9-214">But if an inactive mailbox has a soft-deleted date within the last 30 days and you remove the hold, you can recover the mailbox up until the soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="a88c9-215">Pour plus d’informations, consultez la rubrique [supprimer ou restaurer des boîtes aux lettres utilisateur dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835).</span><span class="sxs-lookup"><span data-stu-id="a88c9-215">For details, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835).</span></span> <span data-ttu-id="a88c9-216">Après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable), vous devez suivre les procédures de récupération d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="a88c9-216">After the soft-deleted mailbox retention period expires, you have follow the procedures for recovering an inactive mailbox.</span></span> <span data-ttu-id="a88c9-217">Pour plus d’informations, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="a88c9-217">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="a88c9-218">**Comment afficher des informations sur une boîte aux lettres inactive après la suppression de la conservation ?**</span><span class="sxs-lookup"><span data-stu-id="a88c9-218">**How do you display information about an inactive mailbox after the hold is removed?**</span></span> <span data-ttu-id="a88c9-219">Après la suppression d’une conservation et la restauration de la boîte aux lettres inactive vers une boîte aux lettres supprimée (récupérable), elle n’est pas renvoyée à l’aide du paramètre *InactiveMailboxOnly* avec la cmdlet **Get-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="a88c9-219">After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet.</span></span> <span data-ttu-id="a88c9-220">Cependant, vous pouvez afficher des informations sur la boîte aux lettres à l'aide de la commande **Get-Mailbox -SoftDeletedMailbox**.</span><span class="sxs-lookup"><span data-stu-id="a88c9-220">But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command.</span></span> <span data-ttu-id="a88c9-221">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a88c9-221">For example:</span></span> 
    
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

  <span data-ttu-id="a88c9-222">Dans l’exemple ci-dessus, la propriété *WhenSoftDeleted* identifie la date supprimée (récupérable), qui, dans cet exemple, est le 30 octobre 2014.</span><span class="sxs-lookup"><span data-stu-id="a88c9-222">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is October 30, 2014.</span></span> <span data-ttu-id="a88c9-223">Si cette boîte aux lettres supprimée (récupérable) était auparavant une boîte aux lettres inactive pour laquelle la conservation a été supprimée, elle sera définitivement supprimée 30 jours après la valeur de la propriété *WhenSoftDeleted* .</span><span class="sxs-lookup"><span data-stu-id="a88c9-223">If this soft-deleted mailbox was previously an inactive mailbox for which the hold was removed, it will be permanently deleted 30 days after the value of the *WhenSoftDeleted* property.</span></span> <span data-ttu-id="a88c9-224">Dans ce cas, la boîte aux lettres est définitivement supprimée après le 30 novembre 2014.</span><span class="sxs-lookup"><span data-stu-id="a88c9-224">In this case, the mailbox is permanently deleted after November 30, 2014.</span></span>

