---
title: Configurer la boîte de réception Prioritaire pour tous les membres de votre organisation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 613a845c-4b71-41de-b331-acdcf5b6625d
description: "Découvrez la configuration d'une boîte de réception prioritaire pour tout ou partie des utilisateurs de votre organisation. "
ms.openlocfilehash: f56e85e79fcf17cde89ec3d6094ca757ccf0cc68
ms.sourcegitcommit: 659adf65d88ee44f643c471e6202396f1ffb6576
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "44779928"
---
# <a name="configure-focused-inbox-for-everyone-in-your-organization"></a><span data-ttu-id="c7821-103">Configurez la boîte de réception Prioritaire pour tous les membres de votre organisation</span><span class="sxs-lookup"><span data-stu-id="c7821-103">Configure Focused Inbox for everyone in your organization</span></span>

  <span data-ttu-id="c7821-104">Si vous êtes responsable de la configuration de messagerie pour TOUS LES UTILISATEURS de votre entreprise, cet article s’adresse à vous !</span><span class="sxs-lookup"><span data-stu-id="c7821-104">If you're responsible for configuring how email works for EVERYONE in a business this article is for you!</span></span> <span data-ttu-id="c7821-105">Il explique comment la personnaliser ou la désactiver pour votre entreprise et apporte des réponses aux [questions fréquemment posées](#faq-for-focused-inbox).</span><span class="sxs-lookup"><span data-stu-id="c7821-105">It explains how to customize it or turn it off for your business, and answers [frequently asked questions](#faq-for-focused-inbox).</span></span>  <br/> <span data-ttu-id="c7821-106">Si vous voulez désactiver la boîte de réception Prioritaire uniquement pour vous, consultez l’article [Désactiver la boîte de réception Prioritaire](https://support.microsoft.com/office/f714d94d-9e63-4217-9ccb-6cb2986aa1b2).</span><span class="sxs-lookup"><span data-stu-id="c7821-106">If you would like to turn off Focused Inbox for just yourself, please see [Turn off Focused Inbox](https://support.microsoft.com/office/f714d94d-9e63-4217-9ccb-6cb2986aa1b2).</span></span>  
   
<span data-ttu-id="c7821-107">If you want to be sure that your users receive business-specific email messages, for example, from HR or payroll, you can configure Focused Inbox so these messages reach the Focused view.</span><span class="sxs-lookup"><span data-stu-id="c7821-107">If you want to be sure that your users receive business-specific email messages, for example, from HR or payroll, you can configure Focused Inbox so these messages reach the Focused view.</span></span> <span data-ttu-id="c7821-108">You can also control whether users in your organization see the Focused Inbox in their mailbox.</span><span class="sxs-lookup"><span data-stu-id="c7821-108">You can also control whether users in your organization see the Focused Inbox in their mailbox.</span></span>
  
## <a name="turn-focused-inbox-on-or-off-in-your-organization"></a><span data-ttu-id="c7821-109">Activez ou désactivez la boîte de réception Prioritaire dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="c7821-109">Turn Focused Inbox On or Off in your organization</span></span>

<span data-ttu-id="c7821-110">Pour activer ou désactiver la boîte de réception Prioritaire pour tous les utilisateurs de votre organisation, vous devez utiliser PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c7821-110">You use PowerShell to turn Focused Inbox on or off for everyone in your organization.</span></span> <span data-ttu-id="c7821-111">Vous souhaitez effectuer cette opération dans le Centre d'administration Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="c7821-111">Do you want to do this in the Microsoft 365 admin center?</span></span> <span data-ttu-id="c7821-112">Informez-en notre équipe Ingénierie.</span><span class="sxs-lookup"><span data-stu-id="c7821-112">Let our Engineering team know.</span></span> <span data-ttu-id="c7821-113">**[Votez ici !](https://go.microsoft.com/fwlink/?linkid=862489)**</span><span class="sxs-lookup"><span data-stu-id="c7821-113">**[Vote here!](https://go.microsoft.com/fwlink/?linkid=862489)**</span></span>
  
 <span data-ttu-id="c7821-114">**Pour désactiver la boîte de réception Prioritaire :**</span><span class="sxs-lookup"><span data-stu-id="c7821-114">**To turn off Focused Inbox:**</span></span>
  
<span data-ttu-id="c7821-115">The following PowerShell example turns Focused Inbox **Off** in your organization.</span><span class="sxs-lookup"><span data-stu-id="c7821-115">The following PowerShell example turns Focused Inbox **Off** in your organization.</span></span> <span data-ttu-id="c7821-116">However, it doesn't block the availability of the feature for your users.</span><span class="sxs-lookup"><span data-stu-id="c7821-116">However, it doesn't block the availability of the feature for your users.</span></span> <span data-ttu-id="c7821-117">If they want, they can still re-enable Focused Inbox again on each of their clients.</span><span class="sxs-lookup"><span data-stu-id="c7821-117">If they want, they can still re-enable Focused Inbox again on each of their clients.</span></span> 
  
1. <span data-ttu-id="c7821-118">[Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="c7821-118">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="c7821-119">You need to be assigned permissions before you can perform this procedure or procedures.</span><span class="sxs-lookup"><span data-stu-id="c7821-119">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="c7821-120">To see what permissions you need, see the "Transport rules" entry in [Messaging policy and compliance permissions](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span><span class="sxs-lookup"><span data-stu-id="c7821-120">To see what permissions you need, see the "Transport rules" entry in [Messaging policy and compliance permissions](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span></span>
    
3. <span data-ttu-id="c7821-121">Exécutez l’applet de commande **Get-OrganizationConfig**.</span><span class="sxs-lookup"><span data-stu-id="c7821-121">Run the **Get-OrganizationConfig** cmdlet.</span></span> 
    
 ``` PowerShell
Get-OrganizationConfig
 ```

4. <span data-ttu-id="c7821-122">Recherchez **FocusedInboxOn** pour afficher son paramètre actuel :</span><span class="sxs-lookup"><span data-stu-id="c7821-122">Look for **FocusedInboxOn** to view its current setting:</span></span> 
    
    ![Réponse de PowerShell sur l’état de la boîte de réception Prioritaire.](../../media/419d8caa-89b9-45c5-91d9-8c023297456e.png)
  
5. <span data-ttu-id="c7821-124">Exécutez l'applet de commande suivante pour désactiver la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-124">Run the following cmdlet to turn Focused Inbox off.</span></span>
    
 ``` PowerShell
 Set-OrganizationConfig -FocusedInboxOn $false
 ```

6. <span data-ttu-id="c7821-125">Exécutez de nouveau l’applet de commande **Get-OrganizationConfig** et vous verrez que FocusedInboxOn est défini sur $false, ce qui signifie qu’elle a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="c7821-125">Run the **Get-OrganizationConfig** cmdlet again and you'll see that FocusedInboxOn is set to $false, which means it's been turned off.</span></span> 
    
 <span data-ttu-id="c7821-126">**Pour activer la boîte de réception Prioritaire :**</span><span class="sxs-lookup"><span data-stu-id="c7821-126">**To turn on Focused Inbox:**</span></span>
  
- <span data-ttu-id="c7821-127">À l’étape 5 ci-dessus, exécutez l’applet de commande suivante pour activer la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-127">In Step 5 above, run the following cmdlet to turn Focused Inbox on.</span></span>
    
 ``` PowerShell
 Set-OrganizationConfig -FocusedInboxOn $true
 ```

## <a name="what-do-users-see-after-i-turn-on-focused-inbox"></a><span data-ttu-id="c7821-128">Que voient les utilisateurs une fois la boîte de réception Prioritaire activée ? </span><span class="sxs-lookup"><span data-stu-id="c7821-128">What do users see after I turn on Focused Inbox?</span></span>

<span data-ttu-id="c7821-129">Your users will see the Focused view only after they close and restart Outlook.</span><span class="sxs-lookup"><span data-stu-id="c7821-129">Your users will see the Focused view only after they close and restart Outlook.</span></span> <span data-ttu-id="c7821-130">When they restart Outlook, they'll see a Tip in the Outlook user interface giving them to the option to use the new Focused Inbox.</span><span class="sxs-lookup"><span data-stu-id="c7821-130">When they restart Outlook, they'll see a Tip in the Outlook user interface giving them to the option to use the new Focused Inbox.</span></span>
  
![Image de la boîte de réception Prioritaire lorsqu’un utilisateur ouvre Outlook sur le web pour la première fois.](../../media/f6ef79e7-0f4c-4a23-b6f0-7c15d927b5f0.png)
  
<span data-ttu-id="c7821-132">If you're switching from Clutter to Focused Inbox, they can decide to enable it ("Try it") or dismiss the feature.</span><span class="sxs-lookup"><span data-stu-id="c7821-132">If you're switching from Clutter to Focused Inbox, they can decide to enable it ("Try it") or dismiss the feature.</span></span> <span data-ttu-id="c7821-133">If the user has multiple (supported) clients, they can enable/disable Focused Inbox individually on each one.</span><span class="sxs-lookup"><span data-stu-id="c7821-133">If the user has multiple (supported) clients, they can enable/disable Focused Inbox individually on each one.</span></span> <span data-ttu-id="c7821-134">The tip looks like this:</span><span class="sxs-lookup"><span data-stu-id="c7821-134">The tip looks like this:</span></span>
  
![Une image illustrant l’apparence de la boîte de réception Prioritaire lorsqu’elle est déployée pour vos utilisateurs et qu’Outlook est rouvert.](../../media/c034f969-d650-4333-88f1-dd10ade0a94c.png)
  
<span data-ttu-id="c7821-136">When a user decides to start using Focused Inbox, Clutter gets disabled automatically.</span><span class="sxs-lookup"><span data-stu-id="c7821-136">When a user decides to start using Focused Inbox, Clutter gets disabled automatically.</span></span> <span data-ttu-id="c7821-137">The Clutter folder gets converted into a standard folder, that allows the user to rename or delete it.</span><span class="sxs-lookup"><span data-stu-id="c7821-137">The Clutter folder gets converted into a standard folder, that allows the user to rename or delete it.</span></span>
  
## <a name="turn-focused-inbox-on-or-off-for-specific-users"></a><span data-ttu-id="c7821-138">Activer ou désactiver la boîte de réception Prioritaire pour des utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="c7821-138">Turn Focused Inbox On or Off for specific users</span></span>

<span data-ttu-id="c7821-139">This example turns Focused Inbox **Off** for Tim Matthews in the Contoso organization.</span><span class="sxs-lookup"><span data-stu-id="c7821-139">This example turns Focused Inbox **Off** for Tim Matthews in the Contoso organization.</span></span> <span data-ttu-id="c7821-140">However, it doesn't block the availability of the feature to him.</span><span class="sxs-lookup"><span data-stu-id="c7821-140">However, it doesn't block the availability of the feature to him.</span></span> <span data-ttu-id="c7821-141">If his wants, he can still re-enable Focused Inbox again on each of his clients.</span><span class="sxs-lookup"><span data-stu-id="c7821-141">If his wants, he can still re-enable Focused Inbox again on each of his clients.</span></span> 
  
1. <span data-ttu-id="c7821-142">[Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="c7821-142">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="c7821-143">You need to be assigned permissions before you can perform this procedure or procedures.</span><span class="sxs-lookup"><span data-stu-id="c7821-143">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="c7821-144">To see what permissions you need, see the "Transport rules" entry in the Messaging policy and compliance permissions topic.</span><span class="sxs-lookup"><span data-stu-id="c7821-144">To see what permissions you need, see the "Transport rules" entry in the Messaging policy and compliance permissions topic.</span></span>
    
3. <span data-ttu-id="c7821-145">Exécutez l’applet de commande **Get-FocusedInbox**, par exemple :</span><span class="sxs-lookup"><span data-stu-id="c7821-145">Run the **Get-FocusedInbox** cmdlet, for example:</span></span> 
    
 ``` PowerShell
 Get-FocusedInbox -Identity <tim@contoso.com>
 ```

4. <span data-ttu-id="c7821-146">Recherchez FocusedInboxOn pour afficher son paramètre actuel :</span><span class="sxs-lookup"><span data-stu-id="c7821-146">Look for FocusedInboxOn to view its current setting:</span></span>
    
    ![Réponse de PowerShell sur l’état de la boîte de réception Prioritaire.](../../media/419d8caa-89b9-45c5-91d9-8c023297456e.png)
  
5. <span data-ttu-id="c7821-148">Exécutez l'applet de commande suivante pour désactiver la boîte de réception Prioritaire :</span><span class="sxs-lookup"><span data-stu-id="c7821-148">Run the following cmdlet to turn Focused Inbox off:</span></span>
    
 ``` PowerShell
 Set-FocusedInbox -Identity <tim@contoso.com> -FocusedInboxOn $false
 ```

6. <span data-ttu-id="c7821-149">OU, exécutez l’applet de commande suivante pour l’activer :</span><span class="sxs-lookup"><span data-stu-id="c7821-149">OR, run the following cmdlet to turn it on:</span></span>
    
 ``` PowerShell
 Set-FocusedInbox -Identity <tim@contoso.com> -FocusedInboxOn $true
 ```

## <a name="use-the-ui-to-create-a-transport-rule-to-direct-email-messages-to-the-focused-view-for-all-your-users"></a><span data-ttu-id="c7821-150">Utilisez l’interface utilisateur pour créer une règle de transport permettant de diriger les messages e-mail vers l’affichage Prioritaire pour tous vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c7821-150">Use the UI to create a transport rule to direct email messages to the Focused view for all your users</span></span>

1. <span data-ttu-id="c7821-151">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="c7821-151">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>
    
2. <span data-ttu-id="c7821-152">Accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="c7821-152">Navigate to **mail flow** \> **Rules**.</span></span> <span data-ttu-id="c7821-153">Cliquez sur ![Ajouter icône EAC](../../media/795e5bdd-48bb-433f-8e07-3c7a19f8eca2.gif), puis sélectionnez **Créer une règle...**</span><span class="sxs-lookup"><span data-stu-id="c7821-153">Select ![EAC Add icon](../../media/795e5bdd-48bb-433f-8e07-3c7a19f8eca2.gif) and then select **Create a new rule...**.</span></span> 
    
3. <span data-ttu-id="c7821-154">Après avoir créé la règle, cliquez sur **Enregistrer** pour démarrer la règle.</span><span class="sxs-lookup"><span data-stu-id="c7821-154">After you're done creating the new rule, select **Save** to start the rule.</span></span> 
    
    <span data-ttu-id="c7821-155">L'image suivante présente un exemple permettant de remettre tous les messages des « Ressources Humaines » dans la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-155">The following image shows an example where all messages From "Payroll Department" are to be delivered to the Focused Inbox.</span></span>
    
    ![paie focusedinbox](../../media/focusedinbox-transport-rule.PNG)
  
## <a name="use-powershell-to-create-a-transport-rule-to-direct-email-messages-to-the-focused-view-for-all-your-users"></a><span data-ttu-id="c7821-157">Utilisez PowerShell pour créer une règle de transport permettant de diriger les messages e-mail vers l’affichage Prioritaire pour tous vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c7821-157">Use PowerShell to create a transport rule to direct email messages to the Focused view for all your users</span></span>

1. <span data-ttu-id="c7821-158">[Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="c7821-158">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="c7821-159">You need to be assigned permissions before you can perform this procedure or procedures.</span><span class="sxs-lookup"><span data-stu-id="c7821-159">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="c7821-160">To see what permissions you need, see the "Transport rules" entry in [Messaging policy and compliance permissions](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span><span class="sxs-lookup"><span data-stu-id="c7821-160">To see what permissions you need, see the "Transport rules" entry in [Messaging policy and compliance permissions](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span></span>

3. <span data-ttu-id="c7821-161">Exécutez la commande suivante pour remettre tous les messages du « Service Paie », par exemple, à la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-161">Run the following command to allow all messages from "Payroll Department," for example, to be delivered to the Focused Inbox.</span></span>
    
 ``` PowerShell
 New-TransportRule -Name <name_of_the_rule> -From "Payroll Department" -SetHeaderName "X-MS-Exchange-Organization-BypassFocusedInbox" -SetHeaderValue "true"
 ```

> [!IMPORTANT]
> <span data-ttu-id="c7821-162">Dans cet exemple, « X-MS-Exchange-Organization-BypassFocusedInbox » et « true » sont sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="c7821-162">In this example, both "X-MS-Exchange-Organization-BypassFocusedInbox" and "true" are case sensitive.</span></span>
> <span data-ttu-id="c7821-163">De plus, la boîte de réception Prioritaire respectera l’en-tête X qui contourne le courrier pêle-mêle. Par conséquent, si vous utilisez ce paramètre dans le courrier pêle-mêle, il sera utilisé dans la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-163">Also, Focused Inbox will honor the X-header that bypasses Clutter, so if you use this setting in Clutter, it will be used in Focused Inbox.</span></span> <span data-ttu-id="c7821-164">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](https://go.microsoft.com/fwlink/p/?LinkId=830194).</span><span class="sxs-lookup"><span data-stu-id="c7821-164">For detailed syntax and parameter information, see [New-TransportRule](https://go.microsoft.com/fwlink/p/?LinkId=830194).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="c7821-165">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="c7821-165">How do you know this worked?</span></span>

<span data-ttu-id="c7821-166">Vérifiez les en-têtes des messages e-mail pour déterminer si les messages sont acheminés vers la boîte de réception suite au contournement de la règle de transport Boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-166">You can check email message headers to see if the email messages are landing in the Inbox due to the Focused Inbox transport rule bypass.</span></span> <span data-ttu-id="c7821-167">Sélectionnez un e-mail dans une boîte aux lettres de votre organisation sur laquelle la règle de transport Boîte de réception Prioritaire est appliquée.</span><span class="sxs-lookup"><span data-stu-id="c7821-167">Pick an email message from a mailbox in your organization that has the Focused Inbox transport rule applied.</span></span> <span data-ttu-id="c7821-168">Examinez les en-têtes du message. L’en-tête suivant doit y figurer : **X-MS-Exchange-Organization-BypassFocusedInbox: true**.</span><span class="sxs-lookup"><span data-stu-id="c7821-168">Look at the headers stamped on the message, and you should see the **X-MS-Exchange-Organization-BypassFocusedInbox: true** header.</span></span> <span data-ttu-id="c7821-169">Cela signifie que le contournement fonctionne.</span><span class="sxs-lookup"><span data-stu-id="c7821-169">This means the bypass is working.</span></span> <span data-ttu-id="c7821-170">Consultez l'article [Afficher les informations d'en-tête Internet des messages électroniques](https://go.microsoft.com/fwlink/p/?LinkId=822530) pour plus d'informations sur la façon de rechercher des informations d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="c7821-170">Check out the [View the Internet header information for an email message](https://go.microsoft.com/fwlink/p/?LinkId=822530) article for info on how to find the header information.</span></span> 
 
## <a name="turn-onoff-clutter"></a><span data-ttu-id="c7821-171">Activer/désactiver la fonctionnalité Courrier pêle-mêle</span><span class="sxs-lookup"><span data-stu-id="c7821-171">Turn on/off Clutter</span></span>
 
<span data-ttu-id="c7821-172">We've received reports that Clutter suddenly stopped working for some users.</span><span class="sxs-lookup"><span data-stu-id="c7821-172">We've received reports that Clutter suddenly stopped working for some users.</span></span> <span data-ttu-id="c7821-173">If this happens, you can enable it again for specific users.</span><span class="sxs-lookup"><span data-stu-id="c7821-173">If this happens, you can enable it again for specific users.</span></span> <span data-ttu-id="c7821-174">See [Configure Clutter for your organization](../email/configure-clutter.md).</span><span class="sxs-lookup"><span data-stu-id="c7821-174">See [Configure Clutter for your organization](../email/configure-clutter.md).</span></span>
 
## <a name="faq-for-focused-inbox"></a><span data-ttu-id="c7821-175">FAQ sur la boîte de réception Prioritaire</span><span class="sxs-lookup"><span data-stu-id="c7821-175">FAQ for Focused Inbox</span></span>

<span data-ttu-id="c7821-176">Voici des réponses aux questions fréquemment posées sur la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-176">Here are answers to Frequently Asked Questions about Focused Inbox.</span></span> 

### <a name="can-i-control-how-i-roll-out-focused-inbox-in-my-organization"></a><span data-ttu-id="c7821-177">Puis-je contrôler le déploiement de la boîte de réception Prioritaire au sein de mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="c7821-177">Can I control how I roll out Focused Inbox in my organization?</span></span>

<span data-ttu-id="c7821-178">Yes.</span><span class="sxs-lookup"><span data-stu-id="c7821-178">Yes.</span></span> <span data-ttu-id="c7821-179">You can turn Focused Inbox on or off for your entire organization, or you can turn it on or off for specified users.</span><span class="sxs-lookup"><span data-stu-id="c7821-179">You can turn Focused Inbox on or off for your entire organization, or you can turn it on or off for specified users.</span></span> <span data-ttu-id="c7821-180">See above.</span><span class="sxs-lookup"><span data-stu-id="c7821-180">See above.</span></span>
  
### <a name="is-the-focused-inbox-feature-only-available-for-office-2016-clients"></a><span data-ttu-id="c7821-181">La fonctionnalité boîte de réception Prioritaire est-elle disponible pour les clients Office 2016 ?</span><span class="sxs-lookup"><span data-stu-id="c7821-181">Is the Focused Inbox feature ONLY available for Office 2016 clients?</span></span>

<span data-ttu-id="c7821-182">Oui, seuls les utilisateurs d’Office 2016 sont concernés.</span><span class="sxs-lookup"><span data-stu-id="c7821-182">Yes, only users with Office 2016 are affected.</span></span> <span data-ttu-id="c7821-183">La fonctionnalité ne sera pas rétroportée vers Outlook 2013 ou version précédente.</span><span class="sxs-lookup"><span data-stu-id="c7821-183">The feature is not going to be backported to Outlook 2013 or earlier.</span></span>
  
### <a name="how-long-does-it-take-for-focused-inbox-changes-to-take-place-in-outlook"></a><span data-ttu-id="c7821-184">Combien de temps faut-il pour que les modifications apportées à la boîte de réception Prioritaire s’appliquent à Outlook ?</span><span class="sxs-lookup"><span data-stu-id="c7821-184">How long does it take for Focused Inbox changes to take place in Outlook?</span></span>

<span data-ttu-id="c7821-185">Lorsque vous activez ou désactivez la boîte de réception Prioritaire, les paramètres s’appliquent dès que vos utilisateurs ferment et redémarrent Outlook.</span><span class="sxs-lookup"><span data-stu-id="c7821-185">Once you turn on or turn off Focused Inbox, the settings will take effect once your users close and restart Outlook.</span></span>
  
### <a name="what-happens-to-clutter-once-i-turn-on-focused-inbox"></a><span data-ttu-id="c7821-186">Que devient le courrier pêle-mêle lorsque j’active la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="c7821-186">What happens to Clutter once I turn on Focused Inbox?</span></span>

<span data-ttu-id="c7821-187">After switching, you'll no longer receive less actionable email in the Clutter folder.</span><span class="sxs-lookup"><span data-stu-id="c7821-187">After switching, you'll no longer receive less actionable email in the Clutter folder.</span></span> <span data-ttu-id="c7821-188">Instead, email will be split between the Focused and Other tabs in your inbox.</span><span class="sxs-lookup"><span data-stu-id="c7821-188">Instead, email will be split between the Focused and Other tabs in your inbox.</span></span> <span data-ttu-id="c7821-189">The same algorithm that moved items to the Clutter folder now powers Focused Inbox, meaning that any emails that were set to move to Clutter will now be moved to Other.</span><span class="sxs-lookup"><span data-stu-id="c7821-189">The same algorithm that moved items to the Clutter folder now powers Focused Inbox, meaning that any emails that were set to move to Clutter will now be moved to Other.</span></span> <span data-ttu-id="c7821-190">Any messages already in your Clutter folder will remain there until you decide to delete or move them.</span><span class="sxs-lookup"><span data-stu-id="c7821-190">Any messages already in your Clutter folder will remain there until you decide to delete or move them.</span></span>
  
<span data-ttu-id="c7821-191">Consultez ce billet rédigé par [Tony Redmond](https://www.petri.com/author/tony-redmond), Microsoft MVP : [De quelle façon la boîte de réception Prioritaire remplace-t-elle le courrier pêle-mêle dans Office 365 ?](https://www.petri.com/focused-inbox-office-365)</span><span class="sxs-lookup"><span data-stu-id="c7821-191">Check out this post by [Tony Redmond](https://www.petri.com/author/tony-redmond), Microsoft MVP: [How the Focused Inbox Replaces Clutter Inside Office 365](https://www.petri.com/focused-inbox-office-365).</span></span>
  
### <a name="can-i-keep-users-on-clutter-what-is-microsofts-recommendation-when-it-comes-to-using-clutter-vs-focused-inbox"></a><span data-ttu-id="c7821-192">Puis-je maintenir des utilisateurs sur le courrier pêle-mêle ?</span><span class="sxs-lookup"><span data-stu-id="c7821-192">Can I keep users on Clutter?</span></span> <span data-ttu-id="c7821-193">Microsoft recommande-t-il d'utiliser le courrier pêle-mêle ou la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="c7821-193">What is Microsoft's recommendation when it comes to using Clutter vs Focused Inbox?</span></span>

<span data-ttu-id="c7821-194">Yes, you can keep users on Clutter and disable Focused Inbox, however, eventually Clutter will be fully replaced with Focused Inbox so Microsoft's recommends moving to Focused Inbox now.</span><span class="sxs-lookup"><span data-stu-id="c7821-194">Yes, you can keep users on Clutter and disable Focused Inbox, however, eventually Clutter will be fully replaced with Focused Inbox so Microsoft's recommends moving to Focused Inbox now.</span></span> <span data-ttu-id="c7821-195">To learn more about when you use Clutter with Exchange Online, see this blog post: [Update on Focused Inbox and our plans for Clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448).</span><span class="sxs-lookup"><span data-stu-id="c7821-195">To learn more about when you use Clutter with Exchange Online, see this blog post: [Update on Focused Inbox and our plans for Clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448).</span></span>
  
### <a name="should-i-disable-clutter-for-my-end-users-if-we-are-going-to-move-everyone-to-focused-inbox"></a><span data-ttu-id="c7821-196">Dois-je désactiver le courrier pêle-mêle pour mes utilisateurs finaux si nous migrons tout le monde vers la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="c7821-196">Should I disable Clutter for my end users if we are going to move everyone to Focused Inbox?</span></span>

<span data-ttu-id="c7821-197">No.</span><span class="sxs-lookup"><span data-stu-id="c7821-197">No.</span></span> <span data-ttu-id="c7821-198">It's possible to disable Clutter for a mailbox explicitly by running the Set-Clutter cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7821-198">It's possible to disable Clutter for a mailbox explicitly by running the Set-Clutter cmdlet.</span></span> <span data-ttu-id="c7821-199">However, if you do this, the mailbox owner will see messages that were previously redirected to the Clutter folder remain in the Inbox and they'll have to process those messages until their client is upgraded to a version that supports the Focused Inbox.</span><span class="sxs-lookup"><span data-stu-id="c7821-199">However, if you do this, the mailbox owner will see messages that were previously redirected to the Clutter folder remain in the Inbox and they'll have to process those messages until their client is upgraded to a version that supports the Focused Inbox.</span></span> <span data-ttu-id="c7821-200">It's therefore best not to disable Clutter until the upgraded clients are available.</span><span class="sxs-lookup"><span data-stu-id="c7821-200">It's therefore best not to disable Clutter until the upgraded clients are available.</span></span>
  
### <a name="why-are-there-two-different-cmdlets-for-managing-focused-inbox"></a><span data-ttu-id="c7821-201">Pourquoi existe-t-il deux applets de commande distinctes pour gérer de la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="c7821-201">Why are there two different cmdlets for managing Focused Inbox?</span></span>

<span data-ttu-id="c7821-202">Deux états sont associés à la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c7821-202">There are two states associated with Focused Inbox.</span></span>
  
- <span data-ttu-id="c7821-203">**Niveau organisation** : état de la boîte de réception Prioritaire, et horodatage de la dernière mise à jour associée.</span><span class="sxs-lookup"><span data-stu-id="c7821-203">**Organization Level**: Focused Inbox state, and an associated last update time-stamp.</span></span> 
    
- <span data-ttu-id="c7821-204">**Niveau boîte aux lettres** : état de la boîte de réception Prioritaire, et horodatage de la dernière mise à jour associée.</span><span class="sxs-lookup"><span data-stu-id="c7821-204">**Mailbox Level**: Focused Inbox state, and an associated last update time-stamp</span></span> 
    
### <a name="how-does-outlook-decide-to-show-the-focused-inbox-experience-with-these-two-states"></a><span data-ttu-id="c7821-205">Comment Outlook détermine-t-il l’expérience de boîte de réception Prioritaire affichée avec ces deux états ?</span><span class="sxs-lookup"><span data-stu-id="c7821-205">How does Outlook decide to show the Focused Inbox experience with these two states?</span></span>

<span data-ttu-id="c7821-206">Outlook decides to show the experience by choosing which cmdlet has the latest time stamp.</span><span class="sxs-lookup"><span data-stu-id="c7821-206">Outlook decides to show the experience by choosing which cmdlet has the latest time stamp.</span></span> <span data-ttu-id="c7821-207">By default, both time stamps are "null" and in this case, the feature is enabled.</span><span class="sxs-lookup"><span data-stu-id="c7821-207">By default, both time stamps are "null" and in this case, the feature is enabled.</span></span>
  
### <a name="why-does-the-get-focusedinbox-cmdlet-return-true-when-ive-turned-focused-inbox-off-in-my-organization"></a><span data-ttu-id="c7821-208">Pourquoi l’applet de commande Get-FocusedInbox renvoie « true » alors que j’ai désactivé la boîte de réception Prioritaire au sein de mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="c7821-208">Why does the Get-FocusedInbox cmdlet return "true", when I've turned Focused Inbox off in my organization?</span></span>

<span data-ttu-id="c7821-209">There are two cmdlets for controlling Focused Inbox.</span><span class="sxs-lookup"><span data-stu-id="c7821-209">There are two cmdlets for controlling Focused Inbox.</span></span> <span data-ttu-id="c7821-210">When you run Get-FocusedInbox for a mailbox, it returns the mailbox level state of the feature.</span><span class="sxs-lookup"><span data-stu-id="c7821-210">When you run Get-FocusedInbox for a mailbox, it returns the mailbox level state of the feature.</span></span> <span data-ttu-id="c7821-211">The experience in Outlook is chosen based on which cmdlet state was last modified.</span><span class="sxs-lookup"><span data-stu-id="c7821-211">The experience in Outlook is chosen based on which cmdlet state was last modified.</span></span>
  
### <a name="can-i-run-a-script-to-see-who-has-turned-on-focused-inbox"></a><span data-ttu-id="c7821-212">Puis-je exécuter un script pour voir qui a activé la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="c7821-212">Can I run a script to see who has turned on Focused Inbox?</span></span>

<span data-ttu-id="c7821-213">No, and this is by design.</span><span class="sxs-lookup"><span data-stu-id="c7821-213">No, and this is by design.</span></span> <span data-ttu-id="c7821-214">Focused Inbox enablement is a client side setting, so all the cmdlet can do is tell you if the user's mailbox is eligible for the client experience.</span><span class="sxs-lookup"><span data-stu-id="c7821-214">Focused Inbox enablement is a client side setting, so all the cmdlet can do is tell you if the user's mailbox is eligible for the client experience.</span></span> <span data-ttu-id="c7821-215">It is possible for it to be simultaneously enabled in some clients and disabled in others, for example, enabled in Outlook app and Outlook Mobile but disabled in Outlook on the web.</span><span class="sxs-lookup"><span data-stu-id="c7821-215">It is possible for it to be simultaneously enabled in some clients and disabled in others, for example, enabled in Outlook app and Outlook Mobile but disabled in Outlook on the web.</span></span>
