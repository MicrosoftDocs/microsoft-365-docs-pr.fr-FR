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
ms.openlocfilehash: f44dc509e28c19c320418c28dda6146331669cde
ms.sourcegitcommit: 8b0718f5607ab509092cb80bda854010d885c54f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53314475"
---
# <a name="setting-up-scheduler-for-microsoft-365"></a><span data-ttu-id="87807-103">Configuration du Planificateur pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="87807-103">Setting up Scheduler for Microsoft 365</span></span>


<span data-ttu-id="87807-104">Pour configurer le Scheduler pour Microsoft 365, voici les conditions préalables :</span><span class="sxs-lookup"><span data-stu-id="87807-104">To set up the Scheduler for Microsoft 365, following are the prerequisites:</span></span>

| <span data-ttu-id="87807-105">De quoi ai-je besoin ?</span><span class="sxs-lookup"><span data-stu-id="87807-105">What do I need?</span></span> | <span data-ttu-id="87807-106">Description</span><span class="sxs-lookup"><span data-stu-id="87807-106">Description</span></span> |
|-------------------|-------------|
|<span data-ttu-id="87807-107">Cortana boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="87807-107">Cortana mailbox</span></span> |<span data-ttu-id="87807-108">Les administrateurs client doivent définir une boîte aux lettres pour qu’elle serve de boîte aux lettres « Cortana » (c’est-à-dire, cortana@yourdomain.com).</span><span class="sxs-lookup"><span data-stu-id="87807-108">Tenant admins will need to set a mailbox to serve as the “Cortana” mailbox (that is, cortana@yourdomain.com).</span></span>         |
|<span data-ttu-id="87807-109">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="87807-109">Exchange Online mailbox</span></span> |<span data-ttu-id="87807-110">Les utilisateurs doivent avoir un Exchange Online et un calendrier</span><span class="sxs-lookup"><span data-stu-id="87807-110">Users must have an Exchange Online mail and calendar</span></span>         |
|<span data-ttu-id="87807-111">Licence du scheduleur</span><span class="sxs-lookup"><span data-stu-id="87807-111">Scheduler license</span></span> |<span data-ttu-id="87807-112">Pour plus d’informations sur les licences et les tarifs, voir [Scheduler for Microsoft 365](https://www.microsoft.com/en-us/microsoft-365/meeting-scheduler-pricing).</span><span class="sxs-lookup"><span data-stu-id="87807-112">For licensing and pricing information, see [Scheduler for Microsoft 365](https://www.microsoft.com/en-us/microsoft-365/meeting-scheduler-pricing).</span></span>        |

## <a name="create-a-mailbox-for-cortana"></a><span data-ttu-id="87807-113">Créer une boîte aux lettres pour Cortana</span><span class="sxs-lookup"><span data-stu-id="87807-113">Create a mailbox for Cortana</span></span>

<span data-ttu-id="87807-114">Une Exchange dans votre client agit comme la boîte aux lettres Cortana pour que votre client envoie et reçoit des courriers électroniques vers et depuis Cortana.</span><span class="sxs-lookup"><span data-stu-id="87807-114">An Exchange mailbox in your tenant acts as the Cortana mailbox for your tenant to send and receive emails to and from Cortana.</span></span> <span data-ttu-id="87807-115">Tous les messages électroniques envoyés Cortana sont conservés dans la boîte aux lettres Cortana de votre client en fonction de votre stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="87807-115">All emails sent to Cortana are retained in your tenant’s Cortana mailbox based on your retention policy.</span></span>

- <span data-ttu-id="87807-116">Utilisez le Centre d’administration Microsoft 365 pour créer une boîte aux lettres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87807-116">Use the Microsoft 365 admin center to create a user mailbox.</span></span> <span data-ttu-id="87807-117">Une stratégie de rétention de 30 jours est recommandée.</span><span class="sxs-lookup"><span data-stu-id="87807-117">A 30-day retention policy is recommended.</span></span> 
- <span data-ttu-id="87807-118">Utilisez le nom Cortana dans l’adresse SMTP principale de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="87807-118">Use the name Cortana in your mailbox’s primary SMTP address.</span></span> <span data-ttu-id="87807-119">Noms tels que « Cortana@yourdomain.com », « CortanaScheduler@contoso.com » ou « Cortana ». Scheduler@yourdomain.com' sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="87807-119">Names such as “Cortana@yourdomain.com,’ ‘CortanaScheduler@contoso.com,’ or ‘Cortana.Scheduler@yourdomain.com’ are recommended.</span></span>

## <a name="designate-the-mailbox-as-the-scheduler-assistant"></a><span data-ttu-id="87807-120">Désigner la boîte aux lettres en tant qu’Assistant De planification</span><span class="sxs-lookup"><span data-stu-id="87807-120">Designate the mailbox as the Scheduler Assistant</span></span>

<span data-ttu-id="87807-121">Une fois qu’une boîte aux lettres unique Cortana Scheduler a été créée, vous devez désigner la boîte aux lettres Microsoft 365 officiellement.</span><span class="sxs-lookup"><span data-stu-id="87807-121">After a unique mailbox for Cortana Scheduler has been created, you must designate the mailbox to Microsoft 365 formally.</span></span> <span data-ttu-id="87807-122">Une fois que vous avez Cortana boîte aux lettres du scheduleur, elle sera disponible pour planifier des réunions au nom de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="87807-122">After you designate the Cortana Scheduler mailbox, it will be available to schedule meetings on behalf of your users.</span></span>

<span data-ttu-id="87807-123">Pour désigner la boîte Cortana scheduler, un administrateur autorisé doit exécuter une commande PowerShell d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="87807-123">To designate the Cortana Scheduler mailbox, an authorized admin must run a one-line PowerShell command.</span></span> 

1. <span data-ttu-id="87807-124">Connecter’Microsoft 365 l’espace d’exécuter PowerShell distant pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="87807-124">Connect to Microsoft 365 remote PowerShell run space for your organization.</span></span>

2. <span data-ttu-id="87807-125">Exécutez le script PowerShell suivant pour désigner la boîte aux lettres du Scheduler :</span><span class="sxs-lookup"><span data-stu-id="87807-125">Run the following PowerShell script to designate the mailbox for Scheduler:</span></span>

    ```powershell
    Set-mailbox cortana@contoso.com -SchedulerAssistant:$true
    ```
    
    <span data-ttu-id="87807-126">Après l’exécution de cette commande « set » sur la boîte aux lettres du Cortana Scheduler, une nouvelle « PersistedCapability » est définie sur la boîte aux lettres pour noter que cette boîte aux lettres est « SchedulerAssistant ».</span><span class="sxs-lookup"><span data-stu-id="87807-126">After running this "set" command on the Cortana Scheduler mailbox, a new "PersistedCapability" is set on the mailbox to note that this mailbox is the "SchedulerAssistant".</span></span>

> [!NOTE]
> <span data-ttu-id="87807-127">Si vous ne l’avez pas fait précédemment, suivez ces étapes pour connecter votre organisation à PowerShell : Connecter à Microsoft 365 [avec PowerShell.](../enterprise/connect-to-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="87807-127">Follow these steps to connect your organization to PowerShell if you’ve not done so previously: [Connect to Microsoft 365 with PowerShell](../enterprise/connect-to-microsoft-365-powershell.md).</span></span>

<span data-ttu-id="87807-128">Pour découvrir quelle boîte aux lettres de votre organisation est actuellement définie en tant qu’assistant Cortana Scheduler, exécutez la fonction Get :</span><span class="sxs-lookup"><span data-stu-id="87807-128">To discover which mailbox in your organization is currently set as the Cortana Scheduler assistant, run the get function:</span></span>

```powershell
Get-mailbox | where {$_.PersistedCapabilities -Match "SchedulerAssistant"}
```

> [!IMPORTANT]
> <span data-ttu-id="87807-129">La mise en service complète de la boîte aux lettres scheduler peut prendre jusqu’à deux heures pour définir la fonctionnalité SchedulerAssistant.</span><span class="sxs-lookup"><span data-stu-id="87807-129">It might take up to two hours for the Scheduler mailbox to complete full provisioning to set the SchedulerAssistant capability.</span></span>

## <a name="exchange-online-mailbox"></a><span data-ttu-id="87807-130">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="87807-130">Exchange Online mailbox</span></span>

<span data-ttu-id="87807-131">Scheduler est un module Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="87807-131">Scheduler is an add-on to Microsoft 365.</span></span> <span data-ttu-id="87807-132">Les organisateurs de réunion doivent avoir une boîte Exchange Online et un calendrier pour que le Scheduler fonctionne.</span><span class="sxs-lookup"><span data-stu-id="87807-132">Meeting organizers must have an Exchange Online mailbox and calendar for Scheduler to work.</span></span>

## <a name="exchange-requirements"></a><span data-ttu-id="87807-133">Configuration requise pour Exchange</span><span class="sxs-lookup"><span data-stu-id="87807-133">Exchange requirements</span></span>

<span data-ttu-id="87807-134">Outre le Programmeur de licences, vous devez avoir l’une des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="87807-134">In addition to licensing Scheduler, you must have one of the following licenses:</span></span>

- <span data-ttu-id="87807-135">Microsoft 365 E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="87807-135">Microsoft 365 E3, A3, E5, A5</span></span>
- <span data-ttu-id="87807-136">Business Basic, Business, Business Standard, Business Premium</span><span class="sxs-lookup"><span data-stu-id="87807-136">Business Basic, Business, Business Standard, Business Premium</span></span>
- <span data-ttu-id="87807-137">Office 365 E1, A1, E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="87807-137">Office 365 E1, A1, E3, A3, E5, A5</span></span>
- <span data-ttu-id="87807-138">Business Essentials, Business Premium</span><span class="sxs-lookup"><span data-stu-id="87807-138">Business Essentials, Business Premium</span></span>
- <span data-ttu-id="87807-139">Exchange Online Plan 1 ou Plan 2.</span><span class="sxs-lookup"><span data-stu-id="87807-139">Exchange Online Plan 1 or Plan 2 license.</span></span> 

> [!Note]
> <span data-ttu-id="87807-140">**Le programme d’Microsoft 365** est actuellement disponible pour les clients internationaux multi-clients, en anglais uniquement.</span><span class="sxs-lookup"><span data-stu-id="87807-140">**Scheduler for Microsoft 365** is currently available for worldwide multi-tenants, in English only.</span></span></br>
>
> <span data-ttu-id="87807-141">Il n’est pas disponible pour les utilisateurs de Office 365 gérés par 21Vianet en Chine ou les utilisateurs de Microsoft 365 avec le cloud allemand qui utilise le groupe de sécurité des données Allemand Telekom.</span><span class="sxs-lookup"><span data-stu-id="87807-141">It is not available for users of Office 365 operated by 21Vianet in China or users of Microsoft 365 with the German cloud that uses the data trustee German Telekom.</span></span> <span data-ttu-id="87807-142">Nous le prenons en charge pour les utilisateurs situés en Allemagne dont les données ne résident pas dans le centre de données allemand.</span><span class="sxs-lookup"><span data-stu-id="87807-142">It is supported for users in Germany whose data location isn't in the German datacenter.</span></span>
>
> <span data-ttu-id="87807-143">Cette fonctionnalité n’est pas non plus prise en charge pour les utilisateurs du cloud public, notamment GCC, Consumer, GCC de haut niveau ou DoD.</span><span class="sxs-lookup"><span data-stu-id="87807-143">This feature is also not supported for users of the Government Cloud, including GCC, Consumer, GCC High, or DoD.</span></span>
