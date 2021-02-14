---
title: Créer une suspension pour litige
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
description: Découvrez comment placer une boîte aux lettres en attente pour litige, en conservant tout le contenu de la boîte aux lettres au cours d’un examen.
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
ms.openlocfilehash: 4bcb857095a63c06caa6e9762496ca74afeead04
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47546986"
---
# <a name="create-a-litigation-hold"></a><span data-ttu-id="88088-103">Créer une suspension pour litige</span><span class="sxs-lookup"><span data-stu-id="88088-103">Create a Litigation Hold</span></span>

<span data-ttu-id="88088-104">Vous pouvez placer une boîte aux lettres en attente pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions d’origine des éléments modifiés.</span><span class="sxs-lookup"><span data-stu-id="88088-104">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items.</span></span> <span data-ttu-id="88088-105">Lorsque vous placez une boîte aux lettres utilisateur en attente pour litige, le contenu de la boîte aux lettres d’archivage de l’utilisateur (si elle est activée) est également conservé.</span><span class="sxs-lookup"><span data-stu-id="88088-105">When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained.</span></span> <span data-ttu-id="88088-106">Lorsque vous créez une attente, vous pouvez spécifier une durée de la rétention (également appelée « attente basée sur le temps *)* afin que les éléments supprimés et modifiés soient conservés pendant une période spécifiée, puis supprimés définitivement de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="88088-106">When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox.</span></span> <span data-ttu-id="88088-107">Sinon, vous pouvez simplement conserver le contenu indéfiniment (appelé « attente infinie *»*) ou jusqu’à la suppression de la attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="88088-107">Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed.</span></span> <span data-ttu-id="88088-108">Si vous spécifiez une période de attente, elle est calculée à partir de la date de réception d’un message ou de la création d’un élément de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="88088-108">If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="88088-109">Voici ce qui se produit lorsque vous créez une attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="88088-109">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="88088-110">Les éléments supprimés définitivement par l’utilisateur sont conservés dans le dossier Éléments récupérables de la boîte aux lettres de l’utilisateur pendant toute la durée de la rétention.</span><span class="sxs-lookup"><span data-stu-id="88088-110">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="88088-111">Les éléments purgés du dossier Éléments récupérables par l’utilisateur sont conservés pendant toute la durée de la rétention.</span><span class="sxs-lookup"><span data-stu-id="88088-111">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="88088-112">Le quota de stockage pour le dossier Éléments récupérables est augmenté de 30 Go à 110 Go.</span><span class="sxs-lookup"><span data-stu-id="88088-112">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="88088-113">Les éléments des boîtes aux lettres principale et d’archivage de l’utilisateur sont conservés</span><span class="sxs-lookup"><span data-stu-id="88088-113">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="assign-an-exchange-online-plan-2-license"></a><span data-ttu-id="88088-114">Attribuer une licence Exchange Online Plan 2</span><span class="sxs-lookup"><span data-stu-id="88088-114">Assign an Exchange Online Plan 2 license</span></span>

- <span data-ttu-id="88088-115">Pour placer une boîte aux lettres Exchange Online en attente pour litige, une licence Exchange Online Plan 2 doit lui être attribuée.</span><span class="sxs-lookup"><span data-stu-id="88088-115">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license.</span></span> <span data-ttu-id="88088-116">Si une boîte aux lettres se voit attribuer une licence Exchange Online Plan 1, vous devez lui attribuer une licence Archivage Exchange Online pour la placer en attente.</span><span class="sxs-lookup"><span data-stu-id="88088-116">If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="88088-117">Placement d’une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="88088-117">Place a mailbox on Litigation Hold</span></span>

<span data-ttu-id="88088-118">Voici les étapes à suivre pour placer une boîte aux lettres en attente pour litige à l’aide du Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="88088-118">Here are the steps to place a mailbox on Litigation Hold using the Exchange admin center.</span></span>

1. <span data-ttu-id="88088-119">Go to [https://outlook.office.com/ecp](https://outlook.office.com/ecp) and sign in using your global administrator account.</span><span class="sxs-lookup"><span data-stu-id="88088-119">Go to [https://outlook.office.com/ecp](https://outlook.office.com/ecp) and sign in using your global administrator account.</span></span>

2. <span data-ttu-id="88088-120">Cliquez **sur Destinataires > boîtes aux lettres** dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="88088-120">Click **Recipients > Mailboxes** in the left navigation pane.</span></span>

3. <span data-ttu-id="88088-121">Sélectionnez la boîte aux lettres que vous souhaitez placer en attente pour litige, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="88088-121">Select the mailbox that you want to place on Litigation Hold, and then click **Edit**.</span></span>

4. <span data-ttu-id="88088-122">Dans la page de propriétés de boîte aux lettres, cliquez sur **Fonctionnalités de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="88088-122">On the mailbox properties page, click **Mailbox features**.</span></span>
    
5. <span data-ttu-id="88088-123">Sous **Conservation pour litige : désactivée**, cliquez sur **Activer** pour mettre la boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="88088-123">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span>
    
6. <span data-ttu-id="88088-124">Dans la page **De attente pour** litige, entrez les informations facultatives suivantes :</span><span class="sxs-lookup"><span data-stu-id="88088-124">On the **Litigation hold** page, enter the following optional information:</span></span> 
    
    - <span data-ttu-id="88088-125">Durée de la mise en attente **pour litige (jours)** : cette zone vous indique la durée de la mise en attente des éléments de boîte aux lettres lorsque la boîte aux lettres est placée en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="88088-125">**Litigation hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold.</span></span> <span data-ttu-id="88088-126">La durée est calculée à compter de la date de réception ou de création de l'élément de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="88088-126">The duration is calculated from the date a mailbox item is received or created.</span></span> <span data-ttu-id="88088-127">Lorsque la durée de la conservation d’un élément spécifique expire, cet élément n’est plus conservé.</span><span class="sxs-lookup"><span data-stu-id="88088-127">When the hold duration expires for a specific item, that item will no longer be preserved.</span></span> <span data-ttu-id="88088-128">Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu’à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="88088-128">If you leave this box blank, items are preserved indefinitely or until the hold is removed.</span></span> <span data-ttu-id="88088-129">Indiquez la période en nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="88088-129">Use days to specify the duration.</span></span>
    
    - <span data-ttu-id="88088-130">**Remarque** : cette zone de message informe l’utilisateur que sa boîte aux lettres est en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="88088-130">**Note** - Use this box to inform the user their mailbox is on Litigation Hold.</span></span> <span data-ttu-id="88088-131">La note s’affiche sur la page Informations sur le compte dans la boîte aux lettres de l’utilisateur s’il utilise Outlook 2010 ou une ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88088-131">The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later.</span></span> <span data-ttu-id="88088-132">Pour accéder à cette page, les utilisateurs peuvent cliquer **sur Fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="88088-132">To access this page, users can click **File** in Outlook.</span></span>
    
    - <span data-ttu-id="88088-133">**URL** : cette zone vous aide à diriger l’utilisateur vers un site web pour plus d’informations sur la mise en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="88088-133">**URL** - Use this box to direct the user to a website for more information about Litigation Hold.</span></span> <span data-ttu-id="88088-134">Cette URL s’affiche sur la page Informations sur le compte dans la boîte aux lettres de l’utilisateur s’il utilise Outlook 2010 ou une édition ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88088-134">This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later.</span></span> <span data-ttu-id="88088-135">Pour accéder à cette page, les utilisateurs peuvent cliquer **sur Fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="88088-135">To access this page, users can click **File** in Outlook..</span></span>

7. <span data-ttu-id="88088-136">Cliquez **sur Enregistrer** sur la page De **attente** pour litige, puis **sur** Enregistrer sur la page des propriétés de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="88088-136">Click **Save** on the **Litigation hold** page, and then click **Save** on the mailbox properties page.</span></span>

### <a name="create-a-litigation-hold-using-powershell"></a><span data-ttu-id="88088-137">Créer une attente pour litige à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="88088-137">Create a Litigation Hold using PowerShell</span></span>

<span data-ttu-id="88088-138">Vous pouvez également créer une mise en attente pour litige en exécutant la commande suivante [dans Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="88088-138">You can also create a Litigation Hold by running the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell):</span></span>

```powershell
Set-Mailbox <username> -LitigationHoldEnabled $true
```

<span data-ttu-id="88088-139">La commande précédente conserve les éléments indéfiniment, car la durée de la conservation n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="88088-139">The previous command preserves items indefinitely because the hold duration isn't specified.</span></span> <span data-ttu-id="88088-140">Pour créer une attente basée sur le temps, à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="88088-140">To created a time-based hold, using the following command:</span></span>

```powershell
Set-Mailbox <username> -LitigationHoldEnabled $true -LitigationHoldDuration <number of days>
```

<span data-ttu-id="88088-141">Pour plus d’informations, consultez [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/set-mailbox).</span><span class="sxs-lookup"><span data-stu-id="88088-141">For more information, see [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/set-mailbox).</span></span>

## <a name="how-does-litigation-hold-work"></a><span data-ttu-id="88088-142">Comment fonctionne la conservation pour litige ?</span><span class="sxs-lookup"><span data-stu-id="88088-142">How does Litigation Hold work?</span></span>

<span data-ttu-id="88088-143">Dans le flux de travail d'éléments supprimés normal, un élément de boîte aux lettres est déplacé dans le sous-dossier Suppressions du dossier Éléments récupérables lorsqu'il est définitivement supprimé (MAJ + SUPPR) ou supprimé du dossier Éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="88088-143">In the normal deleted item workflow, a mailbox item is moved to the Deletions subfolder in the Recoverable Items folder when a user permanently deletes it (Shift + Delete) or deletes it from the Deleted Items folder.</span></span> <span data-ttu-id="88088-144">Une stratégie de suppression (balise de rétention configurée avec une action de rétention Supprimer) déplace également les éléments dans le sous-dossier Suppressions à l'expiration de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="88088-144">A deletion policy (which is a retention tag configured with a Delete retention action) also moves items to the Deletions subfolder when the retention period expires.</span></span> <span data-ttu-id="88088-145">Lorsqu'un utilisateur purge un élément du dossier Éléments récupérables ou lorsque la période de rétention des éléments supprimés expire, l'élément est déplacé dans le sous-dossier Purges et marqué pour suppression définitive.</span><span class="sxs-lookup"><span data-stu-id="88088-145">When a user purges an item in the Recoverable Items folder or when the deleted item retention period expires for an item, it's moved to the Purges subfolder in the Recoverable Items folder and marked for permanent deletion.</span></span> <span data-ttu-id="88088-146">Il sera (purgé) d'Exchange lors du prochain traitement de la boîte aux lettres par l'Assistant Dossier géré.</span><span class="sxs-lookup"><span data-stu-id="88088-146">It will be purged from Exchange the next time the mailbox is processed by the Managed Folder Assistant (MFA).</span></span>

<span data-ttu-id="88088-p108">Lorsqu'une boîte aux lettres est placée en conservation pour litige, les éléments dans le sous-dossier Purges sont conservés pendant la durée spécifiée par la conservation pour litige. La durée de conservation est calculée à partir de la date de réception ou de création d'un élément, et correspond à la durée pendant laquelle les éléments du sous-dossier Purges sont conservés. Lorsque la durée de conservation d'un élément du sous-dossier expire, l'élément est marqué pour suppression définitive et supprimé d'Exchange lors du prochain traitement de la boîte aux lettres par l'Assistant Dossier géré. Si une boîte aux lettres est placée en conservation indéfinie, les éléments ne sont jamais purgés du sous-dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="88088-p108">When a mailbox is placed on Litigation Hold, items in the Purges subfolder are preserved for the hold duration specified by the Litigation Hold. The hold duration is calculated from the original date an item was received or created, and defines how long items in the Purges subfolder are held. When the hold duration expires for an item in the Purges subfolder, the item is marked for permanent deletion and will be purged from Exchange the next time the mailbox is processed by the MFA. If an indefinite hold is placed on a mailbox, items will never be purged from the Purges subfolder.</span></span>

<span data-ttu-id="88088-151">L'illustration suivante montre les sous-dossiers des dossiers Éléments récupérables et le processus de conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="88088-151">The following illustration shows the subfolders in the Recoverable Items folders and the hold workflow process.</span></span>

![Cycle de vie de la attente pour litige](../media/LitigationHoldLifeCycle.png)

> [!NOTE]
> <span data-ttu-id="88088-153">Si une conservation associée à un cas eDiscovery est placée sur une boîte aux lettres, les éléments purgés sont déplacés du sous-dossier Suppressions vers le sous-dossier DiscoveryHolds et sont conservés jusqu’à ce que la boîte aux lettres soit libérée de la conservation eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="88088-153">If a hold associated with an eDiscovery case is placed on a mailbox, purged items are moved from the Deletions subfolder to the DiscoveryHolds subfolder and are preserved until the mailbox is released from the eDiscovery hold.</span></span>
  
