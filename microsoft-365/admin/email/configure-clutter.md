---
title: Configurer le courrier non trié pour votre organisation
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 832276bd-d024-47b6-a80a-a6b884907a5b
description: 'Découvrez comment activer ou désactiver la fonctionnalité de courrier non trié pour tous les utilisateurs de votre organisation ou des utilisateurs spécifiques de votre organisation à l’aide d’Exchange PowerShell. '
ms.openlocfilehash: b71fe20133c78974dc7d1c97a061121eded9f221
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43628926"
---
# <a name="configure-clutter-for-your-organization"></a><span data-ttu-id="27ff6-103">Configurer le courrier non trié pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="27ff6-103">Configure Clutter for your organization</span></span>

> [!TIP]
> <span data-ttu-id="27ff6-104">La [boîte de réception prioritaire](../setup/configure-focused-inbox.md) va remplacer le courrier non trié.</span><span class="sxs-lookup"><span data-stu-id="27ff6-104">[Focused Inbox](../setup/configure-focused-inbox.md) is going to replace Clutter.</span></span> <span data-ttu-id="27ff6-105">En savoir plus : [mise à jour sur la boîte de réception prioritaire et nos offres d’encombrement](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448)</span><span class="sxs-lookup"><span data-stu-id="27ff6-105">Learn more: [Update on Focused Inbox and our plans for Clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448)</span></span>
  
<span data-ttu-id="27ff6-106">En tant qu’administrateur, vous pouvez être amené à gérer la fonctionnalité courrier non trié dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="27ff6-106">As an admin, you may have to manage the Clutter feature in Microsoft 365.</span></span> <span data-ttu-id="27ff6-107">Pour activer/désactiver la fonctionnalité courrier non trié pour les utilisateurs de votre organisation, vous devez utiliser Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27ff6-107">To turn the Clutter feature on/off for users in your organization, you must use Exchange PowerShell.</span></span> <span data-ttu-id="27ff6-108">(Les utilisateurs peuvent activer/désactiver ces instructions en procédant comme suit : désactivez [/par courrier non trié dans Outlook](https://support.office.com/article/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c.aspx).)</span><span class="sxs-lookup"><span data-stu-id="27ff6-108">(Individuals can turn it on/off using these instructions: [Turn off/on Clutter in Outlook](https://support.office.com/article/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c.aspx).)</span></span> 
  
<span data-ttu-id="27ff6-109">Pour plus d’informations sur l’utilisation d’Exchange PowerShell, consultez [l’aide de PowerShell avec Exchange Online](https://go.microsoft.com/fwlink/?LinkID=402831) et [Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?LinkID=722415) .</span><span class="sxs-lookup"><span data-stu-id="27ff6-109">Check out [Using PowerShell with Exchange Online](https://go.microsoft.com/fwlink/?LinkID=402831) and [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?LinkID=722415) for details on using Exchange PowerShell.</span></span> <span data-ttu-id="27ff6-110">Vous devez disposer d’un compte qui dispose au moins du rôle d’administrateur de services Exchange et de la possibilité de se connecter à Exchange Online avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27ff6-110">You need to have an account that has at least the Exchange Service administrator role and the ability to connect to Exchange Online with PowerShell.</span></span> 
  
## <a name="turn-clutter-on-using-exchange-powershell"></a><span data-ttu-id="27ff6-111">Activer l’utilisation d’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ff6-111">Turn Clutter on using Exchange PowerShell</span></span>

<span data-ttu-id="27ff6-112">Vous pouvez activer l’encombrement manuel pour une boîte aux lettres en exécutant la cmdlet [Set-désordre](https://go.microsoft.com/fwlink/?LinkID=834446) .</span><span class="sxs-lookup"><span data-stu-id="27ff6-112">You can enable Clutter manually for a mailbox by running the [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) cmdlet.</span></span> <span data-ttu-id="27ff6-113">Vous pouvez également afficher les paramètres de courrier non trié pour les boîtes aux lettres de votre organisation en exécutant la cmdlet [Get-désordre](https://go.microsoft.com/fwlink/?LinkID=834759) .</span><span class="sxs-lookup"><span data-stu-id="27ff6-113">You can also view Clutter settings for mailboxes in your organization by running the [Get-Clutter](https://go.microsoft.com/fwlink/?LinkID=834759) cmdlet.</span></span> 
  
<span data-ttu-id="27ff6-114">Activer le courrier non trié pour un seul utilisateur nommé allie Bellew</span><span class="sxs-lookup"><span data-stu-id="27ff6-114">Turn on Clutter for a single user named Allie Bellew</span></span>
    
`Set-Clutter -Identity "Allie Bellew" -Enable $true`


## <a name="turn-clutter-off-using-exchange-powershell"></a><span data-ttu-id="27ff6-115">Désactiver le courrier non trié à l’aide d’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ff6-115">Turn Clutter off using Exchange PowerShell</span></span>

<span data-ttu-id="27ff6-116">Vous pouvez désactiver l’encombrement manuellement pour une boîte aux lettres en exécutant la cmdlet [Set-désordre](https://go.microsoft.com/fwlink/?LinkID=834446) .</span><span class="sxs-lookup"><span data-stu-id="27ff6-116">You can disable Clutter manually for a mailbox by running the [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) cmdlet.</span></span> <span data-ttu-id="27ff6-117">Vous pouvez également afficher les paramètres de **courrier non trié** pour les boîtes aux lettres de votre organisation en exécutant la cmdlet [Get-désordre](https://go.microsoft.com/fwlink/?LinkID=834759) .</span><span class="sxs-lookup"><span data-stu-id="27ff6-117">You can also view **Clutter** settings for mailboxes in your organization by running the [Get-Clutter](https://go.microsoft.com/fwlink/?LinkID=834759) cmdlet.</span></span> 
  
<span data-ttu-id="27ff6-118">Désactivez la fonctionnalité courrier non trié pour un seul utilisateur nommé allie Bellew :</span><span class="sxs-lookup"><span data-stu-id="27ff6-118">Turn off Clutter for a single user named Allie Bellew:</span></span>
    
`Set-Clutter -Identity "Allie Bellew" -Enable $false`

<span data-ttu-id="27ff6-119">Si vous utilisez PowerShell pour créer vos utilisateurs en bloc, vous devrez exécuter [Set-désordre](https://go.microsoft.com/fwlink/?LinkID=834446) sur la boîte aux lettres de chaque utilisateur pour gérer le courrier non trié.</span><span class="sxs-lookup"><span data-stu-id="27ff6-119">If you use PowerShell to bulk create your users, then you'll need to run [Set-Clutter](https://go.microsoft.com/fwlink/?LinkID=834446) against each user's mailbox to manage Clutter.</span></span> 
  
## <a name="when-does-the-clutter-onoff-switch-appear-to-users-in-outlook-on-the-web"></a><span data-ttu-id="27ff6-120">Quand le commutateur de suppression de l’encombrement est-il visible par les utilisateurs dans Outlook sur le Web ?</span><span class="sxs-lookup"><span data-stu-id="27ff6-120">When does the Clutter on/off switch appear to users in Outlook on the web?</span></span>
<span data-ttu-id="27ff6-121"><a name="bkmk_onoff"> </a></span><span class="sxs-lookup"><span data-stu-id="27ff6-121"><a name="bkmk_onoff"> </a></span></span>

<span data-ttu-id="27ff6-122">En tant qu’administrateur, vous pouvez réactiver le courrier non trié à l’aide d’Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27ff6-122">As an admin, you can re-enable Clutter using Exchange PowerShell.</span></span> <span data-ttu-id="27ff6-123">Une fois cette opération terminée, la boîte de réception prioritaire sera désactivée et l’encombrement sera réactivé.</span><span class="sxs-lookup"><span data-stu-id="27ff6-123">Once this is done, Focused Inbox will be turned off and Clutter will be active again.</span></span> 
  
 <span data-ttu-id="27ff6-124">**Si vous utilisez Outlook sur le Web avec un abonnement Microsoft 365 Business Premium :**</span><span class="sxs-lookup"><span data-stu-id="27ff6-124">**If you're using Outlook on the web with a Microsoft 365 Business Premium subscription:**</span></span>
  
- <span data-ttu-id="27ff6-125">Si l’utilisateur a activé le courrier inactif :</span><span class="sxs-lookup"><span data-stu-id="27ff6-125">If user currently has Clutter enabled:</span></span> 
    
  - <span data-ttu-id="27ff6-126">Les paramètres de courrier non trié apparaissent</span><span class="sxs-lookup"><span data-stu-id="27ff6-126">Clutter settings appear</span></span>
    
- <span data-ttu-id="27ff6-127">Si l’utilisateur a actuellement activé la boîte de réception prioritaire :</span><span class="sxs-lookup"><span data-stu-id="27ff6-127">If user currently has Focused Inbox enabled:</span></span> 
    
  - <span data-ttu-id="27ff6-128">Les paramètres de courrier non trié ne s’affichent pas</span><span class="sxs-lookup"><span data-stu-id="27ff6-128">Clutter settings will not appear</span></span>
    
- <span data-ttu-id="27ff6-129">Si la boîte de réception prioritaire ou prioritaire n’est pas activée :</span><span class="sxs-lookup"><span data-stu-id="27ff6-129">If neither Clutter or Focused Inbox is enabled:</span></span> 
    
  - <span data-ttu-id="27ff6-130">La boîte de réception prioritaire et la boîte de réception prioritaire apparaissent en tant qu’options dans les paramètres de messagerie de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="27ff6-130">Both Clutter and Focused Inbox appear as options in the user's Mail Settings</span></span>
    
 <span data-ttu-id="27ff6-131">**Si vous utilisez Outlook.com :**</span><span class="sxs-lookup"><span data-stu-id="27ff6-131">**If you're using Outlook.com:**</span></span>
  
- <span data-ttu-id="27ff6-132">Si l’utilisateur a activé le courrier inactif :</span><span class="sxs-lookup"><span data-stu-id="27ff6-132">If user currently has Clutter enabled:</span></span> 
    
  - <span data-ttu-id="27ff6-133">Les paramètres de courrier non trié apparaissent</span><span class="sxs-lookup"><span data-stu-id="27ff6-133">Clutter settings appear</span></span>
    
- <span data-ttu-id="27ff6-134">Si l’utilisateur a actuellement activé la boîte de réception prioritaire :</span><span class="sxs-lookup"><span data-stu-id="27ff6-134">If user currently has Focused Inbox enabled:</span></span> 
    
  - <span data-ttu-id="27ff6-135">Les paramètres de courrier non trié ne s’affichent pas</span><span class="sxs-lookup"><span data-stu-id="27ff6-135">Clutter settings will not appear</span></span>
    
- <span data-ttu-id="27ff6-136">Si la boîte de réception prioritaire ou prioritaire n’est pas activée :</span><span class="sxs-lookup"><span data-stu-id="27ff6-136">If neither Clutter or Focused Inbox is enabled:</span></span> 
    
  - <span data-ttu-id="27ff6-137">La boîte de réception prioritaire et la boîte de réception prioritaire apparaissent en tant qu’options dans les paramètres de messagerie de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="27ff6-137">Both Clutter and Focused Inbox appear as options in the user's Mail Settings</span></span>
    
- <span data-ttu-id="27ff6-138">Si la boîte de réception prioritaire est activée par l’utilisateur à un moment donné :</span><span class="sxs-lookup"><span data-stu-id="27ff6-138">If user enabled Focused Inbox at some point in the past:</span></span>
    
  - <span data-ttu-id="27ff6-139">Les paramètres de courrier non trié ne s’afficheront jamais</span><span class="sxs-lookup"><span data-stu-id="27ff6-139">Clutter settings will never appear</span></span>
    
    <span data-ttu-id="27ff6-140">Non</span><span class="sxs-lookup"><span data-stu-id="27ff6-140">Otherwise,</span></span> 
    
  - <span data-ttu-id="27ff6-141">Les paramètres de courrier non trié apparaissent</span><span class="sxs-lookup"><span data-stu-id="27ff6-141">Clutter settings will appear</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="27ff6-142">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="27ff6-142">Related articles</span></span>
<span data-ttu-id="27ff6-143"><a name="bkmk_onoff"> </a></span><span class="sxs-lookup"><span data-stu-id="27ff6-143"><a name="bkmk_onoff"> </a></span></span>

[<span data-ttu-id="27ff6-144">Utiliser le courrier non trié pour trier les messages à priorité basse dans Outlook</span><span class="sxs-lookup"><span data-stu-id="27ff6-144">Use Clutter to sort low priority messages in Outlook</span></span>](https://support.office.com/article/7755ebf5-4585-469b-b1ab-8b12425c6b6b.aspx)
    
[<span data-ttu-id="27ff6-145">Utiliser le courrier non trié pour trier les messages à priorité basse dans Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="27ff6-145">Use Clutter to sort low priority messages in OWA</span></span>](https://support.office.com/article/fe4d64ca-bf73-48f1-91b4-9a659e008bce.aspx)
    
[<span data-ttu-id="27ff6-146">Désactiver la fonctionnalité courrier non trié dans Outlook</span><span class="sxs-lookup"><span data-stu-id="27ff6-146">Turn off Clutter in Outlook</span></span>](https://support.office.com/article/a9c72a77-1bc4-40e6-ba6d-103c1d1aba4c.aspx)
    

