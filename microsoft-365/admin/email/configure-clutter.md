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
description: 'Découvrez comment activer ou désactiver la fonctionnalité De la fonction De la fonction De pylène pour tous les utilisateurs ou des utilisateurs spécifiques de votre organisation, à l’aide Exchange PowerShell. '
ms.openlocfilehash: 059fb8e626a0b05e0224fc89931453aaae43be0b
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706109"
---
# <a name="configure-clutter-for-your-organization"></a><span data-ttu-id="aeea5-103">Configurer l’encombrement pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="aeea5-103">Configure Clutter for your organization</span></span>

> [!TIP]
> <span data-ttu-id="aeea5-104">[La boîte de réception Focused](../setup/configure-focused-inbox.md) va remplacer l’encombrement.</span><span class="sxs-lookup"><span data-stu-id="aeea5-104">[Focused Inbox](../setup/configure-focused-inbox.md) is going to replace Clutter.</span></span> <span data-ttu-id="aeea5-105">En savoir plus : Mise à jour sur la boîte de réception [Focused et nos plans pour le clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448)</span><span class="sxs-lookup"><span data-stu-id="aeea5-105">Learn more: [Update on Focused Inbox and our plans for Clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448)</span></span>
  
<span data-ttu-id="aeea5-106">En tant qu’administrateur, vous pouvez être dans l’devoir de gérer la fonctionnalité De p Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="aeea5-106">As an admin, you may have to manage the Clutter feature in Microsoft 365.</span></span> <span data-ttu-id="aeea5-107">Pour activer/désactiver la fonctionnalité De l’encombrement pour les utilisateurs de votre organisation, vous devez utiliser Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeea5-107">To turn the Clutter feature on/off for users in your organization, you must use Exchange PowerShell.</span></span> <span data-ttu-id="aeea5-108">(Les individus peuvent l’activer/le désactiver à l’aide des instructions suivantes : [Désactiver/activer le](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c)clutter dans Outlook .</span><span class="sxs-lookup"><span data-stu-id="aeea5-108">(Individuals can turn it on/off using these instructions: [Turn off/on Clutter in Outlook](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c).</span></span>
  
<span data-ttu-id="aeea5-109">Découvrez comment [utiliser PowerShell avec Exchange Online](/powershell/exchange/exchange-online-powershell) et Connecter pour Exchange Online [PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) pour plus d’informations sur l’utilisation Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeea5-109">Check out [Using PowerShell with Exchange Online](/powershell/exchange/exchange-online-powershell) and [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) for details on using Exchange PowerShell.</span></span> <span data-ttu-id="aeea5-110">Vous devez avoir un compte qui dispose au moins du rôle d’administrateur Exchange service et de la possibilité de se connecter à Exchange Online avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeea5-110">You need to have an account that has at least the Exchange Service administrator role and the ability to connect to Exchange Online with PowerShell.</span></span> 
  
## <a name="turn-clutter-on-using-exchange-powershell"></a><span data-ttu-id="aeea5-111">Activer le clutter à l’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="aeea5-111">Turn Clutter on using Exchange PowerShell</span></span>

<span data-ttu-id="aeea5-112">Vous pouvez activer l’encombrement manuellement pour une boîte aux lettres en exécutant la cmdlet [Set-Clutter.](/powershell/module/exchange/set-clutter)</span><span class="sxs-lookup"><span data-stu-id="aeea5-112">You can enable Clutter manually for a mailbox by running the [Set-Clutter](/powershell/module/exchange/set-clutter) cmdlet.</span></span> <span data-ttu-id="aeea5-113">Vous pouvez également afficher les paramètres de courrier non plédet pour les boîtes aux lettres de votre organisation en exécutant la cmdlet [Get-Clutter.](/powershell/module/exchange/get-clutter)</span><span class="sxs-lookup"><span data-stu-id="aeea5-113">You can also view Clutter settings for mailboxes in your organization by running the [Get-Clutter](/powershell/module/exchange/get-clutter) cmdlet.</span></span> 
  
<span data-ttu-id="aeea5-114">Activer le clutter pour un seul utilisateur nommé Allie Bellew</span><span class="sxs-lookup"><span data-stu-id="aeea5-114">Turn on Clutter for a single user named Allie Bellew</span></span>
    
`Set-Clutter -Identity "Allie Bellew" -Enable $true`


## <a name="turn-clutter-off-using-exchange-powershell"></a><span data-ttu-id="aeea5-115">Désactiver l’encombrement à l’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="aeea5-115">Turn Clutter off using Exchange PowerShell</span></span>

<span data-ttu-id="aeea5-116">Vous pouvez désactiver l’encombrement manuellement pour une boîte aux lettres en exécutant la cmdlet [Set-Clutter.](/powershell/module/exchange/set-clutter)</span><span class="sxs-lookup"><span data-stu-id="aeea5-116">You can disable Clutter manually for a mailbox by running the [Set-Clutter](/powershell/module/exchange/set-clutter) cmdlet.</span></span> <span data-ttu-id="aeea5-117">Vous pouvez également afficher les paramètres **de** courrier non pylasse pour les boîtes aux lettres de votre organisation en exécutant la cmdlet [Get-Clutter.](/powershell/module/exchange/get-clutter)</span><span class="sxs-lookup"><span data-stu-id="aeea5-117">You can also view **Clutter** settings for mailboxes in your organization by running the [Get-Clutter](/powershell/module/exchange/get-clutter) cmdlet.</span></span> 
  
<span data-ttu-id="aeea5-118">Dés désactiver le clutter pour un seul utilisateur nommé Allie Bellew :</span><span class="sxs-lookup"><span data-stu-id="aeea5-118">Turn off Clutter for a single user named Allie Bellew:</span></span>
    
`Set-Clutter -Identity "Allie Bellew" -Enable $false`

<span data-ttu-id="aeea5-119">Si vous utilisez PowerShell pour créer en bloc vos utilisateurs, vous devrez exécuter [Set-Clutter](/powershell/module/exchange/set-clutter) sur la boîte aux lettres de chaque utilisateur pour gérer le courrier pable.</span><span class="sxs-lookup"><span data-stu-id="aeea5-119">If you use PowerShell to bulk create your users, then you'll need to run [Set-Clutter](/powershell/module/exchange/set-clutter) against each user's mailbox to manage Clutter.</span></span> 
  
## <a name="when-does-the-clutter-onoff-switch-appear-to-users-in-outlook-on-the-web"></a><span data-ttu-id="aeea5-120">Quand le commutateur Clutter on/off s’affiche-t-il pour les utilisateurs Outlook sur le web ?</span><span class="sxs-lookup"><span data-stu-id="aeea5-120">When does the Clutter on/off switch appear to users in Outlook on the web?</span></span>
<span data-ttu-id="aeea5-121"><a name="bkmk_onoff"> </a></span><span class="sxs-lookup"><span data-stu-id="aeea5-121"><a name="bkmk_onoff"> </a></span></span>

<span data-ttu-id="aeea5-122">En tant qu’administrateur, vous pouvez ré-activer le clutter à l’aide Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeea5-122">As an admin, you can re-enable Clutter using Exchange PowerShell.</span></span> <span data-ttu-id="aeea5-123">Une fois cette mise à jour effectuée, la boîte de réception Focused est désactivée et le clutter est de nouveau actif.</span><span class="sxs-lookup"><span data-stu-id="aeea5-123">Once this is done, Focused Inbox will be turned off and Clutter will be active again.</span></span> 
  
 <span data-ttu-id="aeea5-124">**Si vous utilisez Outlook sur le web avec un abonnement Microsoft 365 Business Premium :**</span><span class="sxs-lookup"><span data-stu-id="aeea5-124">**If you're using Outlook on the web with a Microsoft 365 Business Premium subscription:**</span></span>
  
- <span data-ttu-id="aeea5-125">Si le clutter est actuellement activé pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="aeea5-125">If user currently has Clutter enabled:</span></span> 
    
  - <span data-ttu-id="aeea5-126">Les paramètres de l’encombrement s’affichent</span><span class="sxs-lookup"><span data-stu-id="aeea5-126">Clutter settings appear</span></span>
    
- <span data-ttu-id="aeea5-127">Si la boîte de réception Focus est actuellement activée pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="aeea5-127">If user currently has Focused Inbox enabled:</span></span> 
    
  - <span data-ttu-id="aeea5-128">Les paramètres de l’encombrement n’apparaissent pas</span><span class="sxs-lookup"><span data-stu-id="aeea5-128">Clutter settings will not appear</span></span>
    
- <span data-ttu-id="aeea5-129">Si ni la boîte de réception De l’encombrement ni la boîte de réception Focused n’est activée :</span><span class="sxs-lookup"><span data-stu-id="aeea5-129">If neither Clutter or Focused Inbox is enabled:</span></span> 
    
  - <span data-ttu-id="aeea5-130">La boîte de réception Courrier non paginé et la boîte de réception Focus apparaissent en tant qu’options dans le courrier électronique de l’Paramètres</span><span class="sxs-lookup"><span data-stu-id="aeea5-130">Both Clutter and Focused Inbox appear as options in the user's Mail Settings</span></span>
    
 <span data-ttu-id="aeea5-131">**Si vous utilisez Outlook.com :**</span><span class="sxs-lookup"><span data-stu-id="aeea5-131">**If you're using Outlook.com:**</span></span>
  
- <span data-ttu-id="aeea5-132">Si le clutter est actuellement activé pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="aeea5-132">If user currently has Clutter enabled:</span></span> 
    
  - <span data-ttu-id="aeea5-133">Les paramètres de l’encombrement s’affichent</span><span class="sxs-lookup"><span data-stu-id="aeea5-133">Clutter settings appear</span></span>
    
- <span data-ttu-id="aeea5-134">Si la boîte de réception Focus est actuellement activée pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="aeea5-134">If user currently has Focused Inbox enabled:</span></span> 
    
  - <span data-ttu-id="aeea5-135">Les paramètres de l’encombrement n’apparaissent pas</span><span class="sxs-lookup"><span data-stu-id="aeea5-135">Clutter settings will not appear</span></span>
    
- <span data-ttu-id="aeea5-136">Si ni la boîte de réception De l’encombrement ni la boîte de réception Focused n’est activée :</span><span class="sxs-lookup"><span data-stu-id="aeea5-136">If neither Clutter or Focused Inbox is enabled:</span></span> 
    
  - <span data-ttu-id="aeea5-137">La boîte de réception Courrier non paginé et la boîte de réception Focus apparaissent en tant qu’options dans le courrier électronique de l’Paramètres</span><span class="sxs-lookup"><span data-stu-id="aeea5-137">Both Clutter and Focused Inbox appear as options in the user's Mail Settings</span></span>
    
- <span data-ttu-id="aeea5-138">Si l’utilisateur a activé la boîte de réception Focus à un moment donné dans le passé :</span><span class="sxs-lookup"><span data-stu-id="aeea5-138">If user enabled Focused Inbox at some point in the past:</span></span>
    
  - <span data-ttu-id="aeea5-139">Les paramètres de l’encombrement n’apparaissent jamais</span><span class="sxs-lookup"><span data-stu-id="aeea5-139">Clutter settings will never appear</span></span>
    
    <span data-ttu-id="aeea5-140">Dans le cas contraire,</span><span class="sxs-lookup"><span data-stu-id="aeea5-140">Otherwise,</span></span> 
    
  - <span data-ttu-id="aeea5-141">Les paramètres de l’encombrement s’affichent</span><span class="sxs-lookup"><span data-stu-id="aeea5-141">Clutter settings will appear</span></span>
    
## <a name="related-content"></a><span data-ttu-id="aeea5-142">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="aeea5-142">Related content</span></span>

<span data-ttu-id="aeea5-143">[Utiliser le clutter pour trier les messages de](https://support.microsoft.com/office/7b50c5db-7704-4e55-8a1b-dfc7bf1eafa0) faible priorité dans Outlook (article)</span><span class="sxs-lookup"><span data-stu-id="aeea5-143">[Use Clutter to sort low priority messages in Outlook](https://support.microsoft.com/office/7b50c5db-7704-4e55-8a1b-dfc7bf1eafa0) (article)</span></span>\
<span data-ttu-id="aeea5-144">[Utiliser le clutter pour trier les messages de](https://support.microsoft.com/office/fe4d64ca-bf73-48f1-91b4-9a659e008bce) faible priorité dans OWA (article)</span><span class="sxs-lookup"><span data-stu-id="aeea5-144">[Use Clutter to sort low priority messages in OWA](https://support.microsoft.com/office/fe4d64ca-bf73-48f1-91b4-9a659e008bce) (article)</span></span>\
<span data-ttu-id="aeea5-145">[Désactiver l’encombrement dans Outlook](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c) (article)</span><span class="sxs-lookup"><span data-stu-id="aeea5-145">[Turn off Clutter in Outlook](https://support.microsoft.com/office/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c) (article)</span></span>
