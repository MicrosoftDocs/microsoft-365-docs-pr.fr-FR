---
title: Configurer l’encombrement pour votre organisation
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 832276bd-d024-47b6-a80a-a6b884907a5b
description: 'Découvrez comment activer ou désactiver la fonctionnalité De la fonction Denterr, pour tous les utilisateurs ou des utilisateurs spécifiques de votre organisation, à l’aide d’Exchange PowerShell. '
ms.openlocfilehash: 67267b0865dfcfd6c0ba66d59ce1d0d111d59325
ms.sourcegitcommit: 659adf65d88ee44f643c471e6202396f1ffb6576
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "44780276"
---
# <a name="configure-clutter-for-your-organization"></a><span data-ttu-id="75332-103">Configurer l’encombrement pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="75332-103">Configure Clutter for your organization</span></span>

> [!TIP]
> <span data-ttu-id="75332-104">[La boîte de réception Focused](../setup/configure-focused-inbox.md) remplacera le clutter.</span><span class="sxs-lookup"><span data-stu-id="75332-104">[Focused Inbox](../setup/configure-focused-inbox.md) is going to replace Clutter.</span></span> <span data-ttu-id="75332-105">En savoir plus : Mise à jour de la boîte de réception Focus [et de nos plans pour le clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448)</span><span class="sxs-lookup"><span data-stu-id="75332-105">Learn more: [Update on Focused Inbox and our plans for Clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448)</span></span>
  
<span data-ttu-id="75332-106">En tant qu’administrateur, vous pouvez être dans l’devoir de gérer la fonctionnalité De la pylème dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="75332-106">As an admin, you may have to manage the Clutter feature in Microsoft 365.</span></span> <span data-ttu-id="75332-107">Pour activer/désactiver la fonctionnalité De l’encombrement pour les utilisateurs de votre organisation, vous devez utiliser Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="75332-107">To turn the Clutter feature on/off for users in your organization, you must use Exchange PowerShell.</span></span> <span data-ttu-id="75332-108">(Les individus peuvent l’activer/le désactiver à l’aide des instructions suivantes : Désactiver/activer la fonction De [la pylasse dans Outlook](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c).</span><span class="sxs-lookup"><span data-stu-id="75332-108">(Individuals can turn it on/off using these instructions: [Turn off/on Clutter in Outlook](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c).</span></span>
  
<span data-ttu-id="75332-109">Consultez [l’utilisation de PowerShell avec Exchange Online](https://go.microsoft.com/fwlink/?LinkID=402831) et [connectez-vous](https://go.microsoft.com/fwlink/?LinkID=722415) à Exchange Online PowerShell pour plus d’informations sur l’utilisation d’Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="75332-109">Check out [Using PowerShell with Exchange Online](https://go.microsoft.com/fwlink/?LinkID=402831) and [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?LinkID=722415) for details on using Exchange PowerShell.</span></span> <span data-ttu-id="75332-110">Vous devez avoir un compte ayant au moins le rôle d’administrateur du service Exchange et la possibilité de vous connecter à Exchange Online avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="75332-110">You need to have an account that has at least the Exchange Service administrator role and the ability to connect to Exchange Online with PowerShell.</span></span> 
  
## <a name="turn-clutter-on-using-exchange-powershell"></a><span data-ttu-id="75332-111">Activer le clutter à l’aide d’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="75332-111">Turn Clutter on using Exchange PowerShell</span></span>

<span data-ttu-id="75332-112">Vous pouvez activer l’encombrement manuellement pour une boîte aux lettres en exécutant la cmdlet [Set-Clutter.](https://go.microsoft.com/fwlink/?LinkID=834446)</span><span class="sxs-lookup"><span data-stu-id="75332-112">You can enable Clutter manually for a mailbox by running the [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) cmdlet.</span></span> <span data-ttu-id="75332-113">Vous pouvez également afficher les paramètres de courrier non pylasse pour les boîtes aux lettres de votre organisation en exécutant la cmdlet [Get-Clutter.](https://go.microsoft.com/fwlink/?LinkID=834759)</span><span class="sxs-lookup"><span data-stu-id="75332-113">You can also view Clutter settings for mailboxes in your organization by running the [Get-Clutter](https://go.microsoft.com/fwlink/?LinkID=834759) cmdlet.</span></span> 
  
<span data-ttu-id="75332-114">Activer le clutter pour un seul utilisateur nommé Allie Bellew</span><span class="sxs-lookup"><span data-stu-id="75332-114">Turn on Clutter for a single user named Allie Bellew</span></span>
    
`Set-Clutter -Identity "Allie Bellew" -Enable $true`


## <a name="turn-clutter-off-using-exchange-powershell"></a><span data-ttu-id="75332-115">Désactiver l’encombrement à l’aide d’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="75332-115">Turn Clutter off using Exchange PowerShell</span></span>

<span data-ttu-id="75332-116">Vous pouvez désactiver l’encombrement manuellement pour une boîte aux lettres en exécutant la cmdlet [Set-Clutter.](https://go.microsoft.com/fwlink/?LinkID=834446)</span><span class="sxs-lookup"><span data-stu-id="75332-116">You can disable Clutter manually for a mailbox by running the [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) cmdlet.</span></span> <span data-ttu-id="75332-117">Vous pouvez également afficher les paramètres **de** courrier non plédet pour les boîtes aux lettres de votre organisation en exécutant la cmdlet [Get-Clutter.](https://go.microsoft.com/fwlink/?LinkID=834759)</span><span class="sxs-lookup"><span data-stu-id="75332-117">You can also view **Clutter** settings for mailboxes in your organization by running the [Get-Clutter](https://go.microsoft.com/fwlink/?LinkID=834759) cmdlet.</span></span> 
  
<span data-ttu-id="75332-118">Dés désactiver le clutter pour un seul utilisateur nommé Allie Bellew :</span><span class="sxs-lookup"><span data-stu-id="75332-118">Turn off Clutter for a single user named Allie Bellew:</span></span>
    
`Set-Clutter -Identity "Allie Bellew" -Enable $false`

<span data-ttu-id="75332-119">Si vous utilisez PowerShell pour créer en bloc vos utilisateurs, vous devrez exécuter [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) sur la boîte aux lettres de chaque utilisateur pour gérer le courrier pable.</span><span class="sxs-lookup"><span data-stu-id="75332-119">If you use PowerShell to bulk create your users, then you'll need to run [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) against each user's mailbox to manage Clutter.</span></span> 
  
## <a name="when-does-the-clutter-onoff-switch-appear-to-users-in-outlook-on-the-web"></a><span data-ttu-id="75332-120">Quand le commutateur Clutter on/off s’affiche-t-il pour les utilisateurs dans Outlook sur le web ?</span><span class="sxs-lookup"><span data-stu-id="75332-120">When does the Clutter on/off switch appear to users in Outlook on the web?</span></span>
<span data-ttu-id="75332-121"><a name="bkmk_onoff"> </a></span><span class="sxs-lookup"><span data-stu-id="75332-121"><a name="bkmk_onoff"> </a></span></span>

<span data-ttu-id="75332-122">En tant qu’administrateur, vous pouvez ré-activer l’encombrement à l’aide d’Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="75332-122">As an admin, you can re-enable Clutter using Exchange PowerShell.</span></span> <span data-ttu-id="75332-123">Une fois cette mise à jour effectuée, la boîte de réception Focused est désactivée et le clutter est de nouveau actif.</span><span class="sxs-lookup"><span data-stu-id="75332-123">Once this is done, Focused Inbox will be turned off and Clutter will be active again.</span></span> 
  
 <span data-ttu-id="75332-124">**Si vous utilisez Outlook sur le web avec un abonnement Microsoft 365 Business Premium :**</span><span class="sxs-lookup"><span data-stu-id="75332-124">**If you're using Outlook on the web with a Microsoft 365 Business Premium subscription:**</span></span>
  
- <span data-ttu-id="75332-125">Si le clutter est actuellement activé pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="75332-125">If user currently has Clutter enabled:</span></span> 
    
  - <span data-ttu-id="75332-126">Les paramètres de l’encombrement apparaissent</span><span class="sxs-lookup"><span data-stu-id="75332-126">Clutter settings appear</span></span>
    
- <span data-ttu-id="75332-127">Si la boîte de réception Focus est actuellement activée pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="75332-127">If user currently has Focused Inbox enabled:</span></span> 
    
  - <span data-ttu-id="75332-128">Les paramètres de l’encombrement n’apparaissent pas</span><span class="sxs-lookup"><span data-stu-id="75332-128">Clutter settings will not appear</span></span>
    
- <span data-ttu-id="75332-129">Si ni la boîte de réception De l’encombrement ni la boîte de réception Focused n’est activée :</span><span class="sxs-lookup"><span data-stu-id="75332-129">If neither Clutter or Focused Inbox is enabled:</span></span> 
    
  - <span data-ttu-id="75332-130">La boîte de réception Courrier non courrier et La boîte de réception Focused apparaissent en tant qu’options dans les paramètres de messagerie de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="75332-130">Both Clutter and Focused Inbox appear as options in the user's Mail Settings</span></span>
    
 <span data-ttu-id="75332-131">**Si vous utilisez Outlook.com :**</span><span class="sxs-lookup"><span data-stu-id="75332-131">**If you're using Outlook.com:**</span></span>
  
- <span data-ttu-id="75332-132">Si le clutter est actuellement activé pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="75332-132">If user currently has Clutter enabled:</span></span> 
    
  - <span data-ttu-id="75332-133">Les paramètres de l’encombrement s’affichent</span><span class="sxs-lookup"><span data-stu-id="75332-133">Clutter settings appear</span></span>
    
- <span data-ttu-id="75332-134">Si la boîte de réception Focus est actuellement activée pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="75332-134">If user currently has Focused Inbox enabled:</span></span> 
    
  - <span data-ttu-id="75332-135">Les paramètres de l’encombrement n’apparaissent pas</span><span class="sxs-lookup"><span data-stu-id="75332-135">Clutter settings will not appear</span></span>
    
- <span data-ttu-id="75332-136">Si ni la boîte de réception De l’encombrement, ni la boîte de réception Focused n’est activée :</span><span class="sxs-lookup"><span data-stu-id="75332-136">If neither Clutter or Focused Inbox is enabled:</span></span> 
    
  - <span data-ttu-id="75332-137">La boîte de réception Courrier non courrier et La boîte de réception Focused apparaissent en tant qu’options dans les paramètres de messagerie de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="75332-137">Both Clutter and Focused Inbox appear as options in the user's Mail Settings</span></span>
    
- <span data-ttu-id="75332-138">Si l’utilisateur a activé la boîte de réception Focused à un moment donné dans le passé :</span><span class="sxs-lookup"><span data-stu-id="75332-138">If user enabled Focused Inbox at some point in the past:</span></span>
    
  - <span data-ttu-id="75332-139">Les paramètres de l’encombrement n’apparaîtront jamais</span><span class="sxs-lookup"><span data-stu-id="75332-139">Clutter settings will never appear</span></span>
    
    <span data-ttu-id="75332-140">Dans le cas contraire,</span><span class="sxs-lookup"><span data-stu-id="75332-140">Otherwise,</span></span> 
    
  - <span data-ttu-id="75332-141">Les paramètres de l’encombrement s’affichent</span><span class="sxs-lookup"><span data-stu-id="75332-141">Clutter settings will appear</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="75332-142">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="75332-142">Related articles</span></span>
<span data-ttu-id="75332-143"><a name="bkmk_onoff"> </a></span><span class="sxs-lookup"><span data-stu-id="75332-143"><a name="bkmk_onoff"> </a></span></span>

[<span data-ttu-id="75332-144">Utiliser le clutter pour trier les messages de faible priorité dans Outlook</span><span class="sxs-lookup"><span data-stu-id="75332-144">Use Clutter to sort low priority messages in Outlook</span></span>](https://support.microsoft.com/office/7b50c5db-7704-4e55-8a1b-dfc7bf1eafa0)
    
[<span data-ttu-id="75332-145">Utiliser le clutter pour trier les messages de faible priorité dans OWA</span><span class="sxs-lookup"><span data-stu-id="75332-145">Use Clutter to sort low priority messages in OWA</span></span>](https://support.microsoft.com/office/fe4d64ca-bf73-48f1-91b4-9a659e008bce)
    
[<span data-ttu-id="75332-146">Désactiver l’encombrement dans Outlook</span><span class="sxs-lookup"><span data-stu-id="75332-146">Turn off Clutter in Outlook</span></span>](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c)
    

