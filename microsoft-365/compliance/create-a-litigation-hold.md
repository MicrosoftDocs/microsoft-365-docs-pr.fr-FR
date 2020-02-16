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
ms.openlocfilehash: d465e2a28b47abc5020480a4a862cbbca1d5e678
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42077725"
---
# <a name="create-a-litigation-hold"></a><span data-ttu-id="3f827-102">Créer une suspension pour litige</span><span class="sxs-lookup"><span data-stu-id="3f827-102">Create a Litigation Hold</span></span>

<span data-ttu-id="3f827-103">Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu des boîtes aux lettres, y compris les éléments supprimés et les versions d’origine des éléments modifiés.</span><span class="sxs-lookup"><span data-stu-id="3f827-103">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items.</span></span> <span data-ttu-id="3f827-104">Lorsque vous placez une boîte aux lettres utilisateur en conservation pour litige, le contenu de la boîte aux lettres d’archivage de l’utilisateur (si elle est activée) est également conservé.</span><span class="sxs-lookup"><span data-stu-id="3f827-104">When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained.</span></span> <span data-ttu-id="3f827-105">Lorsque vous créez une suspension, vous pouvez spécifier une durée de conservation (également appelée *conservation basée sur l’heure*) afin que les éléments supprimés et modifiés soient conservés pendant une période spécifiée, puis supprimés définitivement de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3f827-105">When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox.</span></span> <span data-ttu-id="3f827-106">Vous pouvez également conserver indéfiniment le contenu (appelé *conservation infinie*) ou jusqu’à ce que la conservation pour litige ne soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="3f827-106">Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed.</span></span> <span data-ttu-id="3f827-107">Si vous spécifiez une période de durée de blocage, elle est calculée à partir de la date de réception d’un message ou de la création d’un élément de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3f827-107">If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="3f827-108">Voici ce qui se passe lorsque vous créez une suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="3f827-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="3f827-109">Les éléments définitivement supprimés par l’utilisateur sont conservés dans le dossier éléments récupérables de la boîte aux lettres de l’utilisateur pendant la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="3f827-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="3f827-110">Les éléments purgés du dossier éléments récupérables par l’utilisateur sont conservés pendant la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="3f827-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="3f827-111">Le quota de stockage pour le dossier éléments récupérables est passé de 30 Go à 110 Go.</span><span class="sxs-lookup"><span data-stu-id="3f827-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="3f827-112">Les éléments dans les boîtes aux lettres principale et d’archivage de l’utilisateur sont conservés</span><span class="sxs-lookup"><span data-stu-id="3f827-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="3f827-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3f827-113">Before you begin</span></span>

- <span data-ttu-id="3f827-114">Pour placer une boîte aux lettres Exchange Online en conservation pour litige, une licence Exchange Online plan 2 doit lui être attribuée.</span><span class="sxs-lookup"><span data-stu-id="3f827-114">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license.</span></span> <span data-ttu-id="3f827-115">Si une licence Exchange Online plan 1 est attribuée à une boîte aux lettres, vous devez lui attribuer une licence d’archivage Exchange Online distincte pour la mettre en attente.</span><span class="sxs-lookup"><span data-stu-id="3f827-115">If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="3f827-116">Placement d’une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="3f827-116">Place a mailbox on Litigation Hold</span></span>

<span data-ttu-id="3f827-117">Voici les étapes à suivre pour placer une boîte aux lettres en conservation pour litige à l’aide du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f827-117">Here are the steps to place a mailbox on Litigation Hold using the Exchange admin center.</span></span>

1. <span data-ttu-id="3f827-118">Accédez à [https://outlook.office.com/ecp](https://outlook.office.com/ecp) et connectez-vous à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="3f827-118">Go to [https://outlook.office.com/ecp](https://outlook.office.com/ecp) and sign in using your global administrator account.</span></span>

2. <span data-ttu-id="3f827-119">Cliquez sur **destinataires > boîtes aux lettres** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="3f827-119">Click **Recipients > Mailboxes** in the left navigation pane.</span></span>

3. <span data-ttu-id="3f827-120">Sélectionnez la boîte aux lettres que vous souhaitez placer en conservation pour litige, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3f827-120">Select the mailbox that you want to place on Litigation Hold, and then click **Edit**.</span></span>

4. <span data-ttu-id="3f827-121">Dans la page de propriétés de boîte aux lettres, cliquez sur **Fonctionnalités de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="3f827-121">On the mailbox properties page, click **Mailbox features**.</span></span>
    
5. <span data-ttu-id="3f827-122">Sous **Conservation pour litige : désactivée**, cliquez sur **Activer** pour mettre la boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="3f827-122">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span>
    
6. <span data-ttu-id="3f827-123">Sur la page **conservation pour litige** , entrez les informations facultatives suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f827-123">On the **Litigation hold** page, enter the following optional information:</span></span> 
    
    - <span data-ttu-id="3f827-124">**Durée de la conservation pour litige (jours)** : cette zone permet de créer une conservation basée sur le temps et de spécifier la durée pendant laquelle les éléments de boîte aux lettres sont conservés lorsque la boîte aux lettres est placée en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="3f827-124">**Litigation hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold.</span></span> <span data-ttu-id="3f827-125">La durée est calculée à compter de la date de réception ou de création de l'élément de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3f827-125">The duration is calculated from the date a mailbox item is received or created.</span></span> <span data-ttu-id="3f827-126">Lorsque la durée de la conservation expire pour un élément spécifique, cet élément n’est plus conservé.</span><span class="sxs-lookup"><span data-stu-id="3f827-126">When the hold duration expires for a specific item, that item will no longer be preserved.</span></span> <span data-ttu-id="3f827-127">Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu’à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="3f827-127">If you leave this box blank, items are preserved indefinitely or until the hold is removed.</span></span> <span data-ttu-id="3f827-128">Indiquez la période en nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="3f827-128">Use days to specify the duration.</span></span>
    
    - <span data-ttu-id="3f827-129">**Remarque** : cette zone permet d’informer l’utilisateur que sa boîte aux lettres est en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="3f827-129">**Note** - Use this box to inform the user their mailbox is on Litigation Hold.</span></span> <span data-ttu-id="3f827-130">La note apparaît sur la page informations sur le compte dans la boîte aux lettres de l’utilisateur si elle utilise Outlook 2010 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3f827-130">The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later.</span></span> <span data-ttu-id="3f827-131">Pour accéder à cette page, les utilisateurs peuvent cliquer sur **fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="3f827-131">To access this page, users can click **File** in Outlook.</span></span>
    
    - <span data-ttu-id="3f827-132">**URL** : ce champ permet de diriger l’utilisateur vers un site Web pour plus d’informations sur la conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="3f827-132">**URL** - Use this box to direct the user to a website for more information about Litigation Hold.</span></span> <span data-ttu-id="3f827-133">Cette URL apparaît sur la page informations sur le compte dans la boîte aux lettres de l’utilisateur, si elle utilise Outlook 2010 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3f827-133">This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later.</span></span> <span data-ttu-id="3f827-134">Pour accéder à cette page, les utilisateurs peuvent cliquer sur **fichier** dans Outlook..</span><span class="sxs-lookup"><span data-stu-id="3f827-134">To access this page, users can click **File** in Outlook..</span></span>

7. <span data-ttu-id="3f827-135">Cliquez sur **Enregistrer** sur la page **conservation pour litige** , puis cliquez sur **Enregistrer** dans la page Propriétés de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3f827-135">Click **Save** on the **Litigation hold** page, and then click **Save** on the mailbox properties page.</span></span>

### <a name="create-a-litigation-hold-using-powershell"></a><span data-ttu-id="3f827-136">Création d’une conservation pour litige à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="3f827-136">Create a Litigation Hold using PowerShell</span></span>

<span data-ttu-id="3f827-137">Vous pouvez également créer une conservation pour litige en exécutant la commande suivante dans [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="3f827-137">You can also create a Litigation Hold by running the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):</span></span>

```powershell
Set-Mailbox <username> -LitigationHoldEnabled $true
```

<span data-ttu-id="3f827-138">La commande précédente conserve les éléments indéfiniment, car la durée de la conservation n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3f827-138">The previous command preserves items indefinitely because the hold duration isn't specified.</span></span> <span data-ttu-id="3f827-139">Pour créer une conservation basée sur l’heure, à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3f827-139">To created a time-based hold, using the following command:</span></span>

```powershell
Set-Mailbox <username> -LitigationHoldEnabled $true -LitigationHoldDuration <number of days>
```

<span data-ttu-id="3f827-140">Pour plus d’informations, consultez [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox).</span><span class="sxs-lookup"><span data-stu-id="3f827-140">For more information, see [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox).</span></span>

## <a name="how-does-litigation-hold-work"></a><span data-ttu-id="3f827-141">Comment fonctionne la conservation pour litige ?</span><span class="sxs-lookup"><span data-stu-id="3f827-141">How does Litigation Hold work?</span></span>

<span data-ttu-id="3f827-142">Dans le flux de travail d'éléments supprimés normal, un élément de boîte aux lettres est déplacé dans le sous-dossier Suppressions du dossier Éléments récupérables lorsqu'il est définitivement supprimé (MAJ + SUPPR) ou supprimé du dossier Éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="3f827-142">In the normal deleted item workflow, a mailbox item is moved to the Deletions subfolder in the Recoverable Items folder when a user permanently deletes it (Shift + Delete) or deletes it from the Deleted Items folder.</span></span> <span data-ttu-id="3f827-143">Une stratégie de suppression (balise de rétention configurée avec une action de rétention Supprimer) déplace également les éléments dans le sous-dossier Suppressions à l'expiration de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="3f827-143">A deletion policy (which is a retention tag configured with a Delete retention action) also moves items to the Deletions subfolder when the retention period expires.</span></span> <span data-ttu-id="3f827-144">Lorsqu'un utilisateur purge un élément du dossier Éléments récupérables ou lorsque la période de rétention des éléments supprimés expire, l'élément est déplacé dans le sous-dossier Purges et marqué pour suppression définitive.</span><span class="sxs-lookup"><span data-stu-id="3f827-144">When a user purges an item in the Recoverable Items folder or when the deleted item retention period expires for an item, it's moved to the Purges subfolder in the Recoverable Items folder and marked for permanent deletion.</span></span> <span data-ttu-id="3f827-145">Il sera (purgé) d'Exchange lors du prochain traitement de la boîte aux lettres par l'Assistant Dossier géré.</span><span class="sxs-lookup"><span data-stu-id="3f827-145">It will be purged from Exchange the next time the mailbox is processed by the Managed Folder Assistant (MFA).</span></span>

<span data-ttu-id="3f827-p108">Lorsqu'une boîte aux lettres est placée en conservation pour litige, les éléments dans le sous-dossier Purges sont conservés pendant la durée spécifiée par la conservation pour litige. La durée de conservation est calculée à partir de la date de réception ou de création d'un élément, et correspond à la durée pendant laquelle les éléments du sous-dossier Purges sont conservés. Lorsque la durée de conservation d'un élément du sous-dossier expire, l'élément est marqué pour suppression définitive et supprimé d'Exchange lors du prochain traitement de la boîte aux lettres par l'Assistant Dossier géré. Si une boîte aux lettres est placée en conservation indéfinie, les éléments ne sont jamais purgés du sous-dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="3f827-p108">When a mailbox is placed on Litigation Hold, items in the Purges subfolder are preserved for the hold duration specified by the Litigation Hold. The hold duration is calculated from the original date an item was received or created, and defines how long items in the Purges subfolder are held. When the hold duration expires for an item in the Purges subfolder, the item is marked for permanent deletion and will be purged from Exchange the next time the mailbox is processed by the MFA. If an indefinite hold is placed on a mailbox, items will never be purged from the Purges subfolder.</span></span>

<span data-ttu-id="3f827-150">L'illustration suivante montre les sous-dossiers des dossiers Éléments récupérables et le processus de conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="3f827-150">The following illustration shows the subfolders in the Recoverable Items folders and the hold workflow process.</span></span>

![Cycle de vie de conservation pour litige](../media/LitigationHoldLifeCycle.png)

> [!NOTE]
> <span data-ttu-id="3f827-152">Si une conservation associée à un cas de découverte électronique est placée dans une boîte aux lettres, les éléments purgés sont déplacés du sous-dossier suppressions vers le sous-dossier DiscoveryHolds et sont conservés jusqu’à ce que la boîte aux lettres soit libérée de la conservation eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="3f827-152">If a hold associated with an eDiscovery case is placed on a mailbox, purged items are moved from the Deletions subfolder to the DiscoveryHolds subfolder and are preserved until the mailbox is released from the eDiscovery hold.</span></span>
  
