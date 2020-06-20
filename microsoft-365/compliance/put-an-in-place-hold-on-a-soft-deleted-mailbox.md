---
title: Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu.
ms.openlocfilehash: 4dcd6539519675094da9a05c7701b9f8511ce9a1
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44818863"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="aa3ca-103">Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="aa3ca-103">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="aa3ca-104">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-104">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents.</span></span> <span data-ttu-id="aa3ca-105">Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-105">Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa3ca-106">À mesure que nous continuons à investir de différentes manières pour conserver le contenu de la boîte aux lettres, nous annonçaons le retrait des conservations inaltérables dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-106">As we continue to invest in different ways to preserve mailbox content, we're announcing the retirement of In-Place Holds in the Exchange admin center (EAC).</span></span> <span data-ttu-id="aa3ca-107">À partir du 1er juillet 2020 vous ne pourrez pas créer de nouvelles conservations inaltérables dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-107">Starting July 1, 2020 you won't be able to create new In-Place Holds in Exchange Online.</span></span> <span data-ttu-id="aa3ca-108">Toutefois, vous pourrez toujours gérer les conservations inaltérables dans le centre d’administration Exchange ou à l’aide de la cmdlet **Set-MailboxSearch** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-108">But you'll still be able to manage In-Place Holds in the EAC or by using the **Set-MailboxSearch** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="aa3ca-109">Toutefois, à partir du 1er octobre 2020, vous ne pourrez pas gérer les conservations inaltérables.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-109">However, starting October 1, 2020, you won't be able to manage In-Place Holds.</span></span> <span data-ttu-id="aa3ca-110">Vous ne les supprimerez que dans le centre d’administration Exchange ou à l’aide de la cmdlet **Remove-MailboxSearch** .</span><span class="sxs-lookup"><span data-stu-id="aa3ca-110">You'll only be remove them in the EAC or by using the **Remove-MailboxSearch** cmdlet.</span></span> <span data-ttu-id="aa3ca-111">Pour plus d’informations sur le retrait des conservations inaltérables, consultez la rubrique [déclassement des outils eDiscovery hérités](legacy-ediscovery-retirement.md).</span><span class="sxs-lookup"><span data-stu-id="aa3ca-111">For more information about the retirement of In-Place Holds, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md).</span></span>
  
<span data-ttu-id="aa3ca-112">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-112">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted.</span></span> <span data-ttu-id="aa3ca-113">Afterwards, you realize there's information in the mailbox that needs to be preserved.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-113">Afterwards, you realize there's information in the mailbox that needs to be preserved.</span></span> <span data-ttu-id="aa3ca-114">What can you do?</span><span class="sxs-lookup"><span data-stu-id="aa3ca-114">What can you do?</span></span> <span data-ttu-id="aa3ca-115">If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-115">If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox.</span></span> <span data-ttu-id="aa3ca-116">An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-116">An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization.</span></span> <span data-ttu-id="aa3ca-117">The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-117">The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive.</span></span> <span data-ttu-id="aa3ca-118">Une fois la boîte aux lettres inactive, vous pouvez effectuer une recherche dans la boîte aux lettres en utilisant la découverte électronique inaltérable dans Exchange Online, la recherche de contenu dans le centre de sécurité & conformité ou le centre eDiscovery dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-118">After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Security & Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aa3ca-119">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-119">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period.</span></span> <span data-ttu-id="aa3ca-120">The soft-deleted mailbox retention period in Exchange Online is 30 days.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-120">The soft-deleted mailbox retention period in Exchange Online is 30 days.</span></span> <span data-ttu-id="aa3ca-121">This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-121">This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted.</span></span> <span data-ttu-id="aa3ca-122">After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-122">After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="requirements-for-in-place-holds"></a><span data-ttu-id="aa3ca-123">Conditions requises pour les conservations inaltérables</span><span class="sxs-lookup"><span data-stu-id="aa3ca-123">Requirements for In-Place Holds</span></span>

- <span data-ttu-id="aa3ca-124">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-124">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox.</span></span> <span data-ttu-id="aa3ca-125">You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-125">You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 

- <span data-ttu-id="aa3ca-126">Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="aa3ca-126">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

- <span data-ttu-id="aa3ca-127">Exécutez la commande suivante pour obtenir les informations d'identité sur les boîtes aux lettres supprimées (récupérables) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-127">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 

  ```powershell
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="aa3ca-128">Pour plus d’informations sur les boîtes aux lettres inactives, consultez la rubrique [vue d’ensemble des boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="aa3ca-128">For more information about inactive mailboxes, see [Overview of inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>

## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="aa3ca-129">Placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable) pour rendre la boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="aa3ca-129">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>

<span data-ttu-id="aa3ca-130">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-130">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox.</span></span> <span data-ttu-id="aa3ca-131">For more information, see [New-MailboxSearch](https://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa3ca-131">For more information, see [New-MailboxSearch](https://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="aa3ca-132">Créez une variable contenant les propriétés de la boîte aux lettres supprimée (récupérable).</span><span class="sxs-lookup"><span data-stu-id="aa3ca-132">Create a variable that contains the properties of the soft-deleted mailbox.</span></span>

   ```powershell
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > <span data-ttu-id="aa3ca-133">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-133">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox.</span></span> <span data-ttu-id="aa3ca-134">These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-134">These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="aa3ca-135">Create an In-Place Hold and place it on the soft-deleted mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-135">Create an In-Place Hold and place it on the soft-deleted mailbox.</span></span> <span data-ttu-id="aa3ca-136">In this example, no hold duration is specified.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-136">In this example, no hold duration is specified.</span></span> <span data-ttu-id="aa3ca-137">This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-137">This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>

   ```powershell
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```

   <span data-ttu-id="aa3ca-138">You can also specify a hold duration when you create the In-Place Hold.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-138">You can also specify a hold duration when you create the In-Place Hold.</span></span> <span data-ttu-id="aa3ca-139">This example holds items in the inactive mailbox for approximately 7 years.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-139">This example holds items in the inactive mailbox for approximately 7 years.</span></span>

   ```powershell
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. <span data-ttu-id="aa3ca-140">Après un certain temps, exécutez l'une des commandes suivantes pour vérifier que la boîte aux lettres supprimée (récupérable) est une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-140">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>

   ```powershell
   Get-Mailbox -InactiveMailboxOnly
   ```

    <span data-ttu-id="aa3ca-141">Ou</span><span class="sxs-lookup"><span data-stu-id="aa3ca-141">Or</span></span>
    
   ```powershell
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a><span data-ttu-id="aa3ca-142">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="aa3ca-142">More information</span></span>

<span data-ttu-id="aa3ca-143">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox.</span><span class="sxs-lookup"><span data-stu-id="aa3ca-143">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox.</span></span> <span data-ttu-id="aa3ca-144">For more information, see:</span><span class="sxs-lookup"><span data-stu-id="aa3ca-144">For more information, see:</span></span>
  
- [<span data-ttu-id="aa3ca-145">Modifier la durée de conservation pour une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="aa3ca-145">Change the hold duration for an inactive mailbox</span></span>](change-the-hold-duration-for-an-inactive-mailbox.md)

- [<span data-ttu-id="aa3ca-146">Récupérer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="aa3ca-146">Recover an inactive mailbox</span></span>](recover-an-inactive-mailbox.md)

- [<span data-ttu-id="aa3ca-147">Restaurer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="aa3ca-147">Restore an inactive mailbox</span></span>](restore-an-inactive-mailbox.md)

- <span data-ttu-id="aa3ca-148">[Supprimer une boîte aux lettres inactive](delete-an-inactive-mailbox.md) (en supprimant la conservation)</span><span class="sxs-lookup"><span data-stu-id="aa3ca-148">[Delete an inactive mailbox](delete-an-inactive-mailbox.md) (by removing the hold)</span></span>
