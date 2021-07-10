---
title: Configuration du Scheduler pour Microsoft 365.
ms.author: v-aiyengar
author: AshaIyengar21
manager: serdars
audience: Admin
ms.topic: article
ms.service: scheduler
localization_priority: Normal
description: Configuration du Scheduler pour Microsoft 365.
ms.openlocfilehash: 924b25e3d921f402c97632f7475ed5beea98d5c7
ms.sourcegitcommit: f7fbf45af64c5c0727fd5eaab309d20ad097a483
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "53362545"
---
# <a name="setting-up-scheduler-for-microsoft-365"></a><span data-ttu-id="b9aed-103">Configuration du Planificateur pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b9aed-103">Setting up Scheduler for Microsoft 365</span></span>


<span data-ttu-id="b9aed-104">Pour configurer le Scheduler pour Microsoft 365, voici les conditions préalables :</span><span class="sxs-lookup"><span data-stu-id="b9aed-104">To set up the Scheduler for Microsoft 365, following are the prerequisites:</span></span>

| <span data-ttu-id="b9aed-105">De quoi ai-je besoin ?</span><span class="sxs-lookup"><span data-stu-id="b9aed-105">What do I need?</span></span> | <span data-ttu-id="b9aed-106">Description</span><span class="sxs-lookup"><span data-stu-id="b9aed-106">Description</span></span> |
|-------------------|-------------|
|<span data-ttu-id="b9aed-107">Cortana boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="b9aed-107">Cortana mailbox</span></span> |<span data-ttu-id="b9aed-108">Les administrateurs client doivent définir une boîte aux lettres pour qu’elle serve de boîte aux lettres « Cortana » (c’est-à-dire, cortana@yourdomain.com).</span><span class="sxs-lookup"><span data-stu-id="b9aed-108">Tenant admins will need to set a mailbox to serve as the “Cortana” mailbox (that is, cortana@yourdomain.com).</span></span>         |
|<span data-ttu-id="b9aed-109">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9aed-109">Exchange Online mailbox</span></span> |<span data-ttu-id="b9aed-110">Les utilisateurs doivent avoir un Exchange Online et un calendrier</span><span class="sxs-lookup"><span data-stu-id="b9aed-110">Users must have an Exchange Online mail and calendar</span></span>         |
|<span data-ttu-id="b9aed-111">Licence du scheduleur</span><span class="sxs-lookup"><span data-stu-id="b9aed-111">Scheduler license</span></span> |<span data-ttu-id="b9aed-112">Pour plus d’informations sur les licences et les tarifs, voir [Scheduler for Microsoft 365](https://www.microsoft.com/en-us/microsoft-365/meeting-scheduler-pricing).</span><span class="sxs-lookup"><span data-stu-id="b9aed-112">For licensing and pricing information, see [Scheduler for Microsoft 365](https://www.microsoft.com/en-us/microsoft-365/meeting-scheduler-pricing).</span></span>        |

## <a name="create-a-mailbox-for-cortana"></a><span data-ttu-id="b9aed-113">Créer une boîte aux lettres pour Cortana</span><span class="sxs-lookup"><span data-stu-id="b9aed-113">Create a mailbox for Cortana</span></span>

<span data-ttu-id="b9aed-114">Une Exchange dans votre client agit comme la boîte aux lettres Cortana pour que votre client envoie et reçoit des courriers électroniques vers et depuis Cortana.</span><span class="sxs-lookup"><span data-stu-id="b9aed-114">An Exchange mailbox in your tenant acts as the Cortana mailbox for your tenant to send and receive emails to and from Cortana.</span></span> <span data-ttu-id="b9aed-115">Tous les messages électroniques envoyés Cortana sont conservés dans la boîte aux lettres Cortana de votre client en fonction de votre stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="b9aed-115">All emails sent to Cortana are retained in your tenant’s Cortana mailbox based on your retention policy.</span></span>

- <span data-ttu-id="b9aed-116">Utilisez le Centre d’administration Microsoft 365 pour créer une boîte aux lettres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9aed-116">Use the Microsoft 365 admin center to create a user mailbox.</span></span> <span data-ttu-id="b9aed-117">Une stratégie de rétention de 30 jours est recommandée.</span><span class="sxs-lookup"><span data-stu-id="b9aed-117">A 30-day retention policy is recommended.</span></span> 
- <span data-ttu-id="b9aed-118">Utilisez le nom Cortana dans l’adresse SMTP principale de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="b9aed-118">Use the name Cortana in your mailbox’s primary SMTP address.</span></span> <span data-ttu-id="b9aed-119">Noms tels que « Cortana@yourdomain.com », « CortanaScheduler@contoso.com » ou « Cortana ». Scheduler@yourdomain.com' sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="b9aed-119">Names such as “Cortana@yourdomain.com,’ ‘CortanaScheduler@contoso.com,’ or ‘Cortana.Scheduler@yourdomain.com’ are recommended.</span></span>

## <a name="designate-the-mailbox-as-the-scheduler-assistant"></a><span data-ttu-id="b9aed-120">Désigner la boîte aux lettres en tant qu’Assistant De planification</span><span class="sxs-lookup"><span data-stu-id="b9aed-120">Designate the mailbox as the Scheduler Assistant</span></span>

<span data-ttu-id="b9aed-121">Une fois qu’une boîte aux lettres unique Cortana Scheduler a été créée, vous devez désigner la boîte aux lettres Microsoft 365 officiellement.</span><span class="sxs-lookup"><span data-stu-id="b9aed-121">After a unique mailbox for Cortana Scheduler has been created, you must designate the mailbox to Microsoft 365 formally.</span></span> <span data-ttu-id="b9aed-122">Une fois que vous avez Cortana boîte aux lettres du scheduleur, elle sera disponible pour planifier des réunions au nom de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b9aed-122">After you designate the Cortana Scheduler mailbox, it will be available to schedule meetings on behalf of your users.</span></span>

<span data-ttu-id="b9aed-123">Pour désigner la boîte Cortana scheduler, un administrateur autorisé doit exécuter une commande PowerShell d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="b9aed-123">To designate the Cortana Scheduler mailbox, an authorized admin must run a one-line PowerShell command.</span></span> 

1. <span data-ttu-id="b9aed-124">Connecter’Microsoft 365 l’espace d’exécuter PowerShell distant pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b9aed-124">Connect to Microsoft 365 remote PowerShell run space for your organization.</span></span>

2. <span data-ttu-id="b9aed-125">Exécutez le script PowerShell suivant pour désigner la boîte aux lettres du Scheduler :</span><span class="sxs-lookup"><span data-stu-id="b9aed-125">Run the following PowerShell script to designate the mailbox for Scheduler:</span></span>

    ```powershell
    Set-mailbox cortana@contoso.com -SchedulerAssistant:$true
    ```
    
    <span data-ttu-id="b9aed-126">Après l’exécution de cette commande « set » sur la boîte aux lettres du Cortana Scheduler, une nouvelle « PersistedCapability » est définie sur la boîte aux lettres pour noter que cette boîte aux lettres est « SchedulerAssistant ».</span><span class="sxs-lookup"><span data-stu-id="b9aed-126">After running this "set" command on the Cortana Scheduler mailbox, a new "PersistedCapability" is set on the mailbox to note that this mailbox is the "SchedulerAssistant".</span></span>

> [!NOTE]
> <span data-ttu-id="b9aed-127">Si vous ne l’avez pas fait précédemment, suivez ces étapes pour connecter votre organisation à PowerShell : Connecter à Microsoft 365 [avec PowerShell.](../enterprise/connect-to-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="b9aed-127">Follow these steps to connect your organization to PowerShell if you’ve not done so previously: [Connect to Microsoft 365 with PowerShell](../enterprise/connect-to-microsoft-365-powershell.md).</span></span>

<span data-ttu-id="b9aed-128">Pour découvrir quelle boîte aux lettres de votre organisation est actuellement définie en tant qu’assistant Cortana Scheduler, exécutez la fonction Get :</span><span class="sxs-lookup"><span data-stu-id="b9aed-128">To discover which mailbox in your organization is currently set as the Cortana Scheduler assistant, run the get function:</span></span>

```powershell
Get-mailbox | where {$_.PersistedCapabilities -Match "SchedulerAssistant"}
```

> [!IMPORTANT]
> <span data-ttu-id="b9aed-129">La mise en service complète de la boîte aux lettres scheduler peut prendre jusqu’à deux heures pour définir la fonctionnalité SchedulerAssistant.</span><span class="sxs-lookup"><span data-stu-id="b9aed-129">It might take up to two hours for the Scheduler mailbox to complete full provisioning to set the SchedulerAssistant capability.</span></span>

## <a name="exchange-online-mailbox"></a><span data-ttu-id="b9aed-130">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9aed-130">Exchange Online mailbox</span></span>
<span data-ttu-id="b9aed-131">Une licence De planification est un module Microsoft 365, qui permet à l’organisateur de la réunion de déléguer ses tâches de planification de réunion à son Assistant Planification.</span><span class="sxs-lookup"><span data-stu-id="b9aed-131">A Scheduler license is an add-on to Microsoft 365, that enables the meeting organizer to delegate their meeting scheduling tasks to their Scheduler assistant.</span></span> <span data-ttu-id="b9aed-132">Pour que le Scheduler fonctionne, généralement par le biais Microsoft 365 licence, les organisateurs de réunions nécessitent les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="b9aed-132">For the Scheduler to work, typically through Microsoft 365 license, meeting organizers require the following components:</span></span>

- <span data-ttu-id="b9aed-133">Boîte aux lettres désignée comme boîte aux lettres de l’Assistant Planification</span><span class="sxs-lookup"><span data-stu-id="b9aed-133">A mailbox designated as Scheduler assistant mailbox</span></span>
- <span data-ttu-id="b9aed-134">Licence du scheduleur</span><span class="sxs-lookup"><span data-stu-id="b9aed-134">Scheduler license</span></span>
- <span data-ttu-id="b9aed-135">Exchange Online boîte aux lettres et calendrier</span><span class="sxs-lookup"><span data-stu-id="b9aed-135">Exchange Online mailbox and calendar</span></span>

<span data-ttu-id="b9aed-136">Les participants à la réunion n’ont pas besoin de scheduler Microsoft 365 licence.</span><span class="sxs-lookup"><span data-stu-id="b9aed-136">The meeting attendees do not require Scheduler or Microsoft 365 license.</span></span>

## <a name="scheduler-end-user-license-requirements"></a><span data-ttu-id="b9aed-137">Conditions requises pour la licence de l’utilisateur final du scheduler</span><span class="sxs-lookup"><span data-stu-id="b9aed-137">Scheduler end-user license requirements</span></span>

<span data-ttu-id="b9aed-138">Une licence de scheduler nécessite l’une des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="b9aed-138">A Scheduler license requires one of the following licenses:</span></span>

- <span data-ttu-id="b9aed-139">Microsoft 365 E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="b9aed-139">Microsoft 365 E3, A3, E5, A5</span></span>
- <span data-ttu-id="b9aed-140">Business Basic, Business, Business Standard, Business Premium</span><span class="sxs-lookup"><span data-stu-id="b9aed-140">Business Basic, Business, Business Standard, Business Premium</span></span>
- <span data-ttu-id="b9aed-141">Office 365 E1, A1, E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="b9aed-141">Office 365 E1, A1, E3, A3, E5, A5</span></span>
- <span data-ttu-id="b9aed-142">Business Essentials, Business Premium</span><span class="sxs-lookup"><span data-stu-id="b9aed-142">Business Essentials, Business Premium</span></span>
- <span data-ttu-id="b9aed-143">Exchange Online Plan 1 ou Plan 2.</span><span class="sxs-lookup"><span data-stu-id="b9aed-143">Exchange Online Plan 1 or Plan 2 license.</span></span> 

> [!Note]

> <span data-ttu-id="b9aed-144">Le programme de planification Microsoft 365 est disponible dans les environnements internationaux multi-clients en anglais uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9aed-144">Scheduler for Microsoft 365 is available in worldwide multi-tenant environments in English only.</span></span> <span data-ttu-id="b9aed-145">**Le programme d’Microsoft 365** n’est pas disponible pour les utilisateurs des :</span><span class="sxs-lookup"><span data-stu-id="b9aed-145">**Scheduler for Microsoft 365** isn't available to users of:</span></span>

- <span data-ttu-id="b9aed-146">Microsoft 365 géré par 21Vianet en Chine</span><span class="sxs-lookup"><span data-stu-id="b9aed-146">Microsoft 365 operated by 21Vianet in China</span></span>
- <span data-ttu-id="b9aed-147">Microsoft 365 cloud allemand qui utilise le trustee de données German Telekom</span><span class="sxs-lookup"><span data-stu-id="b9aed-147">Microsoft 365 with German cloud that uses the data trustee German Telekom</span></span>
- <span data-ttu-id="b9aed-148">Cloud pour le secteur public, Cloud de la communauté du secteur public, Consommateur, Cloud de la communauté du secteur public Élevé ou DoD</span><span class="sxs-lookup"><span data-stu-id="b9aed-148">Government cloud including GCC, Consumer, GCC High, or DoD</span></span>

<span data-ttu-id="b9aed-149">Le programme de planification prend en charge les utilisateurs situés en Allemagne dont l’emplacement des données ne se trouve pas dans le centre de données allemand.</span><span class="sxs-lookup"><span data-stu-id="b9aed-149">Scheduler does support users in Germany whose data location is not in the German datacenter.</span></span>
