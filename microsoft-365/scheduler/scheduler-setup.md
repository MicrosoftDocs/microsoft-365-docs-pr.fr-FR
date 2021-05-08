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
ms.openlocfilehash: 79e1596288836770c720cb312580fc706bb7b95f
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2021
ms.locfileid: "52286191"
---
# <a name="setting-up-scheduler-for-microsoft-365"></a><span data-ttu-id="68cd5-103">Configuration du Scheduler pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="68cd5-103">Setting up Scheduler for Microsoft 365</span></span>

<span data-ttu-id="68cd5-104">Pour configurer le Scheduler pour Microsoft 365, les conditions préalables sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="68cd5-104">To set up the Scheduler for Microsoft 365, following are the prerequisites:</span></span>

|<span data-ttu-id="68cd5-105">**De quoi ai-je besoin ?**</span><span class="sxs-lookup"><span data-stu-id="68cd5-105">**What do I need?**</span></span> |<span data-ttu-id="68cd5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="68cd5-106">**Description**</span></span> |
|-------------------|-------------|
|<span data-ttu-id="68cd5-107">Boîte aux lettres Cortana</span><span class="sxs-lookup"><span data-stu-id="68cd5-107">Cortana mailbox</span></span> |<span data-ttu-id="68cd5-108">Les administrateurs client doivent définir une boîte aux lettres pour qu’elle serve de boîte aux lettres « Cortana » (c’est-à-dire, cortana@yourdomain.com).</span><span class="sxs-lookup"><span data-stu-id="68cd5-108">Tenant admins will need to set a mailbox to serve as the “Cortana” mailbox (that is, cortana@yourdomain.com).</span></span>         |
|<span data-ttu-id="68cd5-109">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="68cd5-109">Exchange Online mailbox</span></span> |<span data-ttu-id="68cd5-110">Les utilisateurs doivent avoir un Exchange Online et le calendrier</span><span class="sxs-lookup"><span data-stu-id="68cd5-110">Users must have an Exchange Online mail and calendar</span></span>         |
|<span data-ttu-id="68cd5-111">Licence du scheduleur</span><span class="sxs-lookup"><span data-stu-id="68cd5-111">Scheduler license</span></span> |<span data-ttu-id="68cd5-112">Pour plus d’informations sur les licences et les tarifs, voir [Scheduler for Microsoft 365](https://www.microsoft.com/microsoft-365/meeting-scheduler-pricing).</span><span class="sxs-lookup"><span data-stu-id="68cd5-112">For licensing and pricing information, see [Scheduler for Microsoft 365](https://www.microsoft.com/microsoft-365/meeting-scheduler-pricing).</span></span>        |

## <a name="create-a-mailbox-for-cortana"></a><span data-ttu-id="68cd5-113">Créer une boîte aux lettres pour Cortana</span><span class="sxs-lookup"><span data-stu-id="68cd5-113">Create a mailbox for Cortana</span></span>
<span data-ttu-id="68cd5-114">Une Exchange de votre client fait office de boîte aux lettres Cortana pour que votre client envoie et reçoie des courriers électroniques vers et depuis Cortana.</span><span class="sxs-lookup"><span data-stu-id="68cd5-114">An Exchange mailbox in your tenant acts as the Cortana mailbox for your tenant to send and receive emails to and from Cortana.</span></span> <span data-ttu-id="68cd5-115">Tous les messages électroniques envoyés à Cortana sont conservés dans la boîte aux lettres Cortana de votre client en fonction de votre stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="68cd5-115">All emails sent to Cortana are retained in your tenant’s Cortana mailbox based on your retention policy.</span></span>

- <span data-ttu-id="68cd5-116">Utilisez le centre Microsoft 365'administration pour créer une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="68cd5-116">Use the Microsoft 365 admin center to create a new mailbox.</span></span> <span data-ttu-id="68cd5-117">Une stratégie de rétention de 30 jours est recommandée.</span><span class="sxs-lookup"><span data-stu-id="68cd5-117">A 30-day retention policy is recommended.</span></span> <span data-ttu-id="68cd5-118">Utilisez le nom Cortana dans l’adresse SMTP principale de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="68cd5-118">Use the name Cortana in your mailbox’s primary SMTP address.</span></span> <span data-ttu-id="68cd5-119">Des noms tels que « Cortana@yourdomain.com », « CortanaScheduler@contoso.com » ou « Cortana.Scheduler@yourdomain.com » sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="68cd5-119">Names such as “Cortana@yourdomain.com,’ ‘CortanaScheduler@contoso.com,’ or ‘Cortana.Scheduler@yourdomain.com’ are recommended.</span></span>
- <span data-ttu-id="68cd5-120">Contactez Microsoft (scheduler_m365@microsoft.com) pour activer votre boîte aux lettres Cortana.</span><span class="sxs-lookup"><span data-stu-id="68cd5-120">Contact Microsoft (scheduler_m365@microsoft.com) to enable your Cortana mailbox.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="68cd5-121">Vous devez contacter Microsoft pour configurer votre boîte aux lettres Cortana afin qu’elle utilise le service Scheduler en scheduler_m365@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="68cd5-121">You must contact Microsoft to configure your Cortana mailbox to use the Scheduler service by emailing scheduler_m365@microsoft.com.</span></span> <span data-ttu-id="68cd5-122">L’activation de votre boîte aux lettres Cortana peut prendre jusqu’à deux semaines.</span><span class="sxs-lookup"><span data-stu-id="68cd5-122">Enabling your Cortana mailbox may take up to two weeks.</span></span>

## <a name="exchange-online-mailbox"></a><span data-ttu-id="68cd5-123">Boîte aux lettres Exchange Online</span><span class="sxs-lookup"><span data-stu-id="68cd5-123">Exchange Online mailbox</span></span>
<span data-ttu-id="68cd5-124">Le programmeur est un module Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="68cd5-124">Scheduler is an add-on to Microsoft 365.</span></span> <span data-ttu-id="68cd5-125">Les organisateurs de réunions doivent avoir une boîte Exchange Online et un calendrier pour que le Scheduler fonctionne.</span><span class="sxs-lookup"><span data-stu-id="68cd5-125">Meeting organizers must have an Exchange Online mailbox and calendar for Scheduler to work.</span></span>

## <a name="exchange-requirements"></a><span data-ttu-id="68cd5-126">Configuration requise pour Exchange</span><span class="sxs-lookup"><span data-stu-id="68cd5-126">Exchange requirements</span></span>

<span data-ttu-id="68cd5-127">Outre le Programmeur de licences, vous devez avoir l’une des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="68cd5-127">In addition to licensing Scheduler, you must have one of the following licenses:</span></span>

- <span data-ttu-id="68cd5-128">Microsoft 365 E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="68cd5-128">Microsoft 365 E3, A3, E5, A5</span></span>
- <span data-ttu-id="68cd5-129">Business Basic, Business, Business Standard, Business Premium</span><span class="sxs-lookup"><span data-stu-id="68cd5-129">Business Basic, Business, Business Standard, Business Premium</span></span>
- <span data-ttu-id="68cd5-130">Office 365 E1, A1, E3, A3, E5, A5</span><span class="sxs-lookup"><span data-stu-id="68cd5-130">Office 365 E1, A1, E3, A3, E5, A5</span></span>
- <span data-ttu-id="68cd5-131">Business Essentials, Business Premium</span><span class="sxs-lookup"><span data-stu-id="68cd5-131">Business Essentials, Business Premium</span></span>
- <span data-ttu-id="68cd5-132">Exchange Online Plan 1 ou Plan 2.</span><span class="sxs-lookup"><span data-stu-id="68cd5-132">Exchange Online Plan 1 or Plan 2 license.</span></span> 

> [!Note]
> <span data-ttu-id="68cd5-133">**Le programme d’Microsoft 365** n’est pas disponible pour les utilisateurs de Office 365 21Vianet en Chine.</span><span class="sxs-lookup"><span data-stu-id="68cd5-133">**Scheduler for Microsoft 365** isn't available for users of Office 365 operated by 21Vianet in China.</span></span> <span data-ttu-id="68cd5-134">Il n’est pas non plus disponible pour les utilisateurs Microsoft 365 avec le cloud allemand qui utilise le groupe de sécurité des données Allemand Telekom.</span><span class="sxs-lookup"><span data-stu-id="68cd5-134">It's also not available for users of Microsoft 365 with the German cloud that uses the data trustee German Telekom.</span></span> <span data-ttu-id="68cd5-135">Nous le prenons en charge pour les utilisateurs situés en Allemagne dont les données ne résident pas dans le centre de données allemand.</span><span class="sxs-lookup"><span data-stu-id="68cd5-135">It is supported for users in Germany whose data location isn't in the German datacenter.</span></span>
>
><span data-ttu-id="68cd5-136">Cette fonctionnalité n’est pas non plus prise en charge pour les utilisateurs du cloud public, notamment GCC, Consumer, GCC de haut niveau ou DoD.</span><span class="sxs-lookup"><span data-stu-id="68cd5-136">This feature is also not supported for users of the Government Cloud, including GCC, Consumer, GCC High, or DoD.</span></span>
