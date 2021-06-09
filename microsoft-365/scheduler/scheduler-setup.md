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
ms.openlocfilehash: c17cdbbf71359a2725a3b0a145cba5feffd7c853
ms.sourcegitcommit: e1e275eb88153bafddf93327adf8f82318913a8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52809190"
---
# <a name="setting-up-scheduler-for-microsoft-365"></a><span data-ttu-id="3399f-103">Configuration du Scheduler pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3399f-103">Setting up Scheduler for Microsoft 365</span></span>

<span data-ttu-id="3399f-104">Pour configurer le Scheduler pour Microsoft 365, voici les conditions préalables :</span><span class="sxs-lookup"><span data-stu-id="3399f-104">To set up the Scheduler for Microsoft 365, following are the prerequisites:</span></span>

|<span data-ttu-id="3399f-105">**De quoi ai-je besoin ?**</span><span class="sxs-lookup"><span data-stu-id="3399f-105">**What do I need?**</span></span> |<span data-ttu-id="3399f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="3399f-106">**Description**</span></span> |
|-------------------|-------------|
|<span data-ttu-id="3399f-107">Boîte aux lettres Cortana</span><span class="sxs-lookup"><span data-stu-id="3399f-107">Cortana mailbox</span></span> |<span data-ttu-id="3399f-108">Les administrateurs client doivent définir une boîte aux lettres pour qu’elle serve de boîte aux lettres « Cortana » (c’est-à-dire, cortana@yourdomain.com).</span><span class="sxs-lookup"><span data-stu-id="3399f-108">Tenant admins will need to set a mailbox to serve as the “Cortana” mailbox (that is, cortana@yourdomain.com).</span></span>         |
|<span data-ttu-id="3399f-109">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3399f-109">Exchange Online mailbox</span></span> |<span data-ttu-id="3399f-110">Les utilisateurs doivent avoir un Exchange Online et un calendrier</span><span class="sxs-lookup"><span data-stu-id="3399f-110">Users must have an Exchange Online mail and calendar</span></span>         |
|<span data-ttu-id="3399f-111">Licence du scheduleur</span><span class="sxs-lookup"><span data-stu-id="3399f-111">Scheduler license</span></span> |<span data-ttu-id="3399f-112">Pour plus d’informations sur les licences et les tarifs, voir [Scheduler for Microsoft 365](https://www.microsoft.com/microsoft-365/meeting-scheduler-pricing).</span><span class="sxs-lookup"><span data-stu-id="3399f-112">For licensing and pricing information, see [Scheduler for Microsoft 365](https://www.microsoft.com/microsoft-365/meeting-scheduler-pricing).</span></span>        |

## <a name="create-a-mailbox-for-cortana"></a><span data-ttu-id="3399f-113">Créer une boîte aux lettres pour Cortana</span><span class="sxs-lookup"><span data-stu-id="3399f-113">Create a mailbox for Cortana</span></span>
<span data-ttu-id="3399f-114">Une Exchange de votre client fait office de boîte aux lettres Cortana pour que votre client envoie et reçoie des courriers électroniques vers et depuis Cortana.</span><span class="sxs-lookup"><span data-stu-id="3399f-114">An Exchange mailbox in your tenant acts as the Cortana mailbox for your tenant to send and receive emails to and from Cortana.</span></span> <span data-ttu-id="3399f-115">Tous les messages électroniques envoyés à Cortana sont conservés dans la boîte aux lettres Cortana de votre client en fonction de votre stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="3399f-115">All emails sent to Cortana are retained in your tenant’s Cortana mailbox based on your retention policy.</span></span>

- <span data-ttu-id="3399f-116">Utilisez le centre Microsoft 365'administration pour créer une boîte aux lettres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3399f-116">Use the Microsoft 365 admin center to create a user mailbox.</span></span> <span data-ttu-id="3399f-117">Une stratégie de rétention de 30 jours est recommandée.</span><span class="sxs-lookup"><span data-stu-id="3399f-117">A 30-day retention policy is recommended.</span></span> 
- <span data-ttu-id="3399f-118">Utilisez le nom Cortana dans l’adresse SMTP principale de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3399f-118">Use the name Cortana in your mailbox’s primary SMTP address.</span></span> <span data-ttu-id="3399f-119">Des noms tels que « Cortana@yourdomain.com », « CortanaScheduler@contoso.com » ou « Cortana.Scheduler@yourdomain.com » sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="3399f-119">Names such as “Cortana@yourdomain.com,’ ‘CortanaScheduler@contoso.com,’ or ‘Cortana.Scheduler@yourdomain.com’ are recommended.</span></span>

## <a name="designate-the-mailbox-as-the-scheduler-assistant"></a><span data-ttu-id="3399f-120">Désigner la boîte aux lettres en tant qu’Assistant De planification</span><span class="sxs-lookup"><span data-stu-id="3399f-120">Designate the mailbox as the Scheduler Assistant</span></span>

<span data-ttu-id="3399f-121">Une fois qu’une boîte aux lettres unique pour le Scheduler de Cortana a été créée, vous devez désigner la boîte aux lettres Microsoft 365 officiellement.</span><span class="sxs-lookup"><span data-stu-id="3399f-121">After a unique mailbox for Cortana Scheduler has been created, you must designate the mailbox to Microsoft 365 formally.</span></span> <span data-ttu-id="3399f-122">Une fois que vous avez désigné la boîte aux lettres du programmeur Cortana, elle sera disponible pour planifier des réunions au nom de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3399f-122">After you designate the Cortana Scheduler mailbox, it will be available to schedule meetings on behalf of your users.</span></span>

<span data-ttu-id="3399f-123">Pour désigner la boîte aux lettres du Scheduler de Cortana, un administrateur autorisé doit exécuter une commande PowerShell d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="3399f-123">To designate the Cortana Scheduler mailbox, an authorized admin must run a one-line PowerShell command.</span></span> 

1. <span data-ttu-id="3399f-124">Connecter’Microsoft 365 l’espace d’exécuter PowerShell distant pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3399f-124">Connect to Microsoft 365 remote PowerShell run space for your organization.</span></span>
2. <span data-ttu-id="3399f-125">Exécutez le script PowerShell suivant pour désigner la boîte aux lettres du Scheduler :</span><span class="sxs-lookup"><span data-stu-id="3399f-125">Run the following PowerShell script to designate the mailbox for Scheduler:</span></span>

```powershell

Set-mailbox cortana@contoso.com -SchedulerAssistant:$true

```

<span data-ttu-id="3399f-126">Après l’exécution de cette commande « set » sur la boîte aux lettres du Scheduler de Cortana, une nouvelle « PersistedCapability » est définie sur la boîte aux lettres pour noter que cette boîte aux lettres est « SchedulerAssistant ».</span><span class="sxs-lookup"><span data-stu-id="3399f-126">After running this "set" command on the Cortana Scheduler mailbox, a new "PersistedCapability" is set on the mailbox to note that this mailbox is the "SchedulerAssistant".</span></span>

> [!NOTE]
> <span data-ttu-id="3399f-127">Si vous ne l’avez pas déjà fait, suivez ces étapes pour connecter votre organisation à PowerShell : Connecter pour Microsoft 365 [avec PowerShell - Microsoft 365 Entreprise | Documents Microsoft](../enterprise/connect-to-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="3399f-127">Follow these steps to connect your organization to PowerShell if you’ve not done so previously: [Connect to Microsoft 365 with PowerShell - Microsoft 365 Enterprise | Microsoft Docs](../enterprise/connect-to-microsoft-365-powershell.md)</span></span>

<span data-ttu-id="3399f-128">Pour découvrir quelle boîte aux lettres de votre organisation est actuellement définie en tant qu’Assistant De planification de Cortana, exécutez la fonction get :</span><span class="sxs-lookup"><span data-stu-id="3399f-128">To discover which mailbox in your organization is currently set as the Cortana Scheduler assistant, run the get function:</span></span>
 
```powershell

Get-mailbox -Organization contoso.com | where {($_.PersistedCapabilities -like "SchedulerAssistant")}

```

> [!IMPORTANT]
> <span data-ttu-id="3399f-129">La mise en service complète de la boîte aux lettres scheduler peut prendre jusqu’à deux heures pour définir la fonctionnalité SchedulerAssistant.</span><span class="sxs-lookup"><span data-stu-id="3399f-129">It might take up to two hours for the Scheduler mailbox to complete full provisioning to set the SchedulerAssistant capability.</span></span>

## <a name="exchange-online-mailbox"></a><span data-ttu-id="3399f-130">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3399f-130">Exchange Online mailbox</span></span>
<span data-ttu-id="3399f-131">Scheduler est un module Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3399f-131">Scheduler is an add-on to Microsoft 365.</span></span> <span data-ttu-id="3399f-132">Les organisateurs de réunions doivent avoir une boîte Exchange Online et un calendrier pour que le Scheduler fonctionne.</span><span class="sxs-lookup"><span data-stu-id="3399f-132">Meeting organizers must have an Exchange Online mailbox and calendar for Scheduler to work.</span></span>

## <a name="exchange-requirements"></a><span data-ttu-id="3399f-133">Configuration requise pour Exchange</span><span class="sxs-lookup"><span data-stu-id="3399f-133">Exchange requirements</span></span>

<span data-ttu-id="3399f-134">Outre le Programmeur de licences, vous devez avoir l’une des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="3399f-134">In addition to licensing Scheduler, you must have one of the following licenses:</span></span>

- <span data-ttu-id="3399f-135">Microsoft 365 E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="3399f-135">Microsoft 365 E3, A3, E5, A5</span></span>
- <span data-ttu-id="3399f-136">Business Basic, Business, Business Standard, Business Premium</span><span class="sxs-lookup"><span data-stu-id="3399f-136">Business Basic, Business, Business Standard, Business Premium</span></span>
- <span data-ttu-id="3399f-137">Office 365 E1, A1, E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="3399f-137">Office 365 E1, A1, E3, A3, E5, A5</span></span>
- <span data-ttu-id="3399f-138">Business Essentials, Business Premium</span><span class="sxs-lookup"><span data-stu-id="3399f-138">Business Essentials, Business Premium</span></span>
- <span data-ttu-id="3399f-139">Exchange Online Plan 1 ou Plan 2.</span><span class="sxs-lookup"><span data-stu-id="3399f-139">Exchange Online Plan 1 or Plan 2 license.</span></span> 

> [!Note]
> <span data-ttu-id="3399f-140">**Le programme d’Microsoft 365** n’est pas disponible pour les utilisateurs de Office 365 21Vianet en Chine.</span><span class="sxs-lookup"><span data-stu-id="3399f-140">**Scheduler for Microsoft 365** isn't available for users of Office 365 operated by 21Vianet in China.</span></span> <span data-ttu-id="3399f-141">Il n’est pas non plus disponible pour les utilisateurs Microsoft 365 avec le cloud allemand qui utilise le groupe de sécurité des données Allemand Telekom.</span><span class="sxs-lookup"><span data-stu-id="3399f-141">It's also not available for users of Microsoft 365 with the German cloud that uses the data trustee German Telekom.</span></span> <span data-ttu-id="3399f-142">Nous le prenons en charge pour les utilisateurs situés en Allemagne dont les données ne résident pas dans le centre de données allemand.</span><span class="sxs-lookup"><span data-stu-id="3399f-142">It is supported for users in Germany whose data location isn't in the German datacenter.</span></span>
>
><span data-ttu-id="3399f-143">Cette fonctionnalité n’est pas non plus prise en charge pour les utilisateurs du cloud public, notamment GCC, Consumer, GCC de haut niveau ou DoD.</span><span class="sxs-lookup"><span data-stu-id="3399f-143">This feature is also not supported for users of the Government Cloud, including GCC, Consumer, GCC High, or DoD.</span></span>
