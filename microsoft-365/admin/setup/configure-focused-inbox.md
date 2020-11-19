---
title: Configurer la boîte de réception Prioritaire pour tous les membres de votre organisation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
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
ms.openlocfilehash: 76a449295b7a2ad0cc1c82488a131a3a89fe41fc
ms.sourcegitcommit: 2d3e85173c65a9e0ce92624a80ed7a9839f5b8bd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49123428"
---
# <a name="configure-focused-inbox-for-everyone-in-your-organization"></a><span data-ttu-id="e577b-103">Configurez la boîte de réception Prioritaire pour tous les membres de votre organisation</span><span class="sxs-lookup"><span data-stu-id="e577b-103">Configure Focused Inbox for everyone in your organization</span></span>

  <span data-ttu-id="e577b-104">Si vous êtes responsable de la configuration de messagerie pour TOUS LES UTILISATEURS de votre entreprise, cet article s’adresse à vous !</span><span class="sxs-lookup"><span data-stu-id="e577b-104">If you're responsible for configuring how email works for EVERYONE in a business this article is for you!</span></span> <span data-ttu-id="e577b-105">Il explique comment la personnaliser ou la désactiver pour votre entreprise et apporte des réponses aux [questions fréquemment posées](#faq-for-focused-inbox).</span><span class="sxs-lookup"><span data-stu-id="e577b-105">It explains how to customize it or turn it off for your business, and answers [frequently asked questions](#faq-for-focused-inbox).</span></span>  <br/> <span data-ttu-id="e577b-106">Si vous voulez désactiver la boîte de réception Prioritaire uniquement pour vous, consultez l’article [Désactiver la boîte de réception Prioritaire](https://support.microsoft.com/office/f714d94d-9e63-4217-9ccb-6cb2986aa1b2).</span><span class="sxs-lookup"><span data-stu-id="e577b-106">If you would like to turn off Focused Inbox for just yourself, please see [Turn off Focused Inbox](https://support.microsoft.com/office/f714d94d-9e63-4217-9ccb-6cb2986aa1b2).</span></span>  

<span data-ttu-id="e577b-p102">Si vous souhaitez que vos utilisateurs reçoivent les e-mails spécifiques à l’entreprise, comme les e-mails des services Ressources humaines et Paie, vous pouvez configurer la boîte de réception Prioritaire pour que ceux-ci apparaissent dans l’affichage Prioritaire. Vous pouvez également faire apparaître la boîte de réception Prioritaire dans les boîtes aux lettres des utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e577b-p102">If you want to be sure that your users receive business-specific email messages, for example, from HR or payroll, you can configure Focused Inbox so these messages reach the Focused view. You can also control whether users in your organization see the Focused Inbox in their mailbox.</span></span>
  
## <a name="turn-focused-inbox-on-or-off-in-your-organization"></a><span data-ttu-id="e577b-109">Activez ou désactivez la boîte de réception Prioritaire dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="e577b-109">Turn Focused Inbox On or Off in your organization</span></span>

<span data-ttu-id="e577b-110">Pour activer ou désactiver la boîte de réception Prioritaire pour tous les utilisateurs de votre organisation, vous devez utiliser PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e577b-110">You use PowerShell to turn Focused Inbox on or off for everyone in your organization.</span></span> <span data-ttu-id="e577b-111">Vous souhaitez effectuer cette opération dans le Centre d'administration Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="e577b-111">Do you want to do this in the Microsoft 365 admin center?</span></span> <span data-ttu-id="e577b-112">Informez-en notre équipe Ingénierie.</span><span class="sxs-lookup"><span data-stu-id="e577b-112">Let our Engineering team know.</span></span> <span data-ttu-id="e577b-113">**[Votez ici !](https://go.microsoft.com/fwlink/?linkid=862489)**</span><span class="sxs-lookup"><span data-stu-id="e577b-113">**[Vote here!](https://go.microsoft.com/fwlink/?linkid=862489)**</span></span>
  
 <span data-ttu-id="e577b-114">**Pour désactiver la boîte de réception Prioritaire :**</span><span class="sxs-lookup"><span data-stu-id="e577b-114">**To turn off Focused Inbox:**</span></span>
  
<span data-ttu-id="e577b-p104">L’exemple PowerShell suivant **désactive** la boîte de réception Prioritaire au sein de votre organisation. Mais cela n’empêche pas vos utilisateurs d’y accéder. S’ils le souhaitent, ils peuvent toujours réactiver la boîte de réception Prioritaire sur chacun de leurs clients. </span><span class="sxs-lookup"><span data-stu-id="e577b-p104">The following PowerShell example turns Focused Inbox **Off** in your organization. However, it doesn't block the availability of the feature for your users. If they want, they can still re-enable Focused Inbox again on each of their clients.</span></span> 
  
1. <span data-ttu-id="e577b-118">[Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="e577b-118">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>

2. <span data-ttu-id="e577b-p105">Pour effectuer ces procédures, vous devez disposer des autorisations appropriées. Pour connaître les autorisations requises, reportez-vous à l'entrée « Règles de transport » de [Autorisations relatives à la conformité et à la stratégie de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span><span class="sxs-lookup"><span data-stu-id="e577b-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Messaging policy and compliance permissions](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span></span>

3. <span data-ttu-id="e577b-121">Exécutez l’applet de commande **Get-OrganizationConfig**.</span><span class="sxs-lookup"><span data-stu-id="e577b-121">Run the **Get-OrganizationConfig** cmdlet.</span></span> 

 ``` PowerShell
Get-OrganizationConfig
 ```

4. <span data-ttu-id="e577b-122">Recherchez **FocusedInboxOn** pour afficher son paramètre actuel :</span><span class="sxs-lookup"><span data-stu-id="e577b-122">Look for **FocusedInboxOn** to view its current setting:</span></span> 

    ![Réponse de PowerShell sur l’état de la boîte de réception Prioritaire.](../../media/419d8caa-89b9-45c5-91d9-8c023297456e.png)
  
5. <span data-ttu-id="e577b-124">Exécutez l'applet de commande suivante pour désactiver la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-124">Run the following cmdlet to turn Focused Inbox off.</span></span>

 ``` PowerShell
 Set-OrganizationConfig -FocusedInboxOn $false
 ```

6. <span data-ttu-id="e577b-125">Exécutez de nouveau l’applet de commande **Get-OrganizationConfig** et vous verrez que FocusedInboxOn est défini sur $false, ce qui signifie qu’elle a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="e577b-125">Run the **Get-OrganizationConfig** cmdlet again and you'll see that FocusedInboxOn is set to $false, which means it's been turned off.</span></span> 

 <span data-ttu-id="e577b-126">**Pour activer la boîte de réception Prioritaire :**</span><span class="sxs-lookup"><span data-stu-id="e577b-126">**To turn on Focused Inbox:**</span></span>
  
- <span data-ttu-id="e577b-127">À l’étape 5 ci-dessus, exécutez l’applet de commande suivante pour activer la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-127">In Step 5 above, run the following cmdlet to turn Focused Inbox on.</span></span>

 ``` PowerShell
 Set-OrganizationConfig -FocusedInboxOn $true
 ```

## <a name="what-do-users-see-after-i-turn-on-focused-inbox"></a><span data-ttu-id="e577b-128">Que voient les utilisateurs une fois la boîte de réception Prioritaire activée ? </span><span class="sxs-lookup"><span data-stu-id="e577b-128">What do users see after I turn on Focused Inbox?</span></span>

<span data-ttu-id="e577b-p106">Vos utilisateurs ne verront l’affichage Prioritaire qu’après avoir fermé et redémarré Outlook. Un conseil leur donnant la possibilité d’utiliser la nouvelle boîte de réception Prioritaire apparaît alors dans l’interface utilisateur d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="e577b-p106">Your users will see the Focused view only after they close and restart Outlook. When they restart Outlook, they'll see a Tip in the Outlook user interface giving them to the option to use the new Focused Inbox.</span></span>
  
![Image de la boîte de réception Prioritaire lorsqu’un utilisateur ouvre Outlook sur le web pour la première fois.](../../media/f6ef79e7-0f4c-4a23-b6f0-7c15d927b5f0.png)
  
<span data-ttu-id="e577b-p107">Si vous passez du Courrier pêle-mêle à la boîte de réception Prioritaire, ils peuvent décider d'activer (« Essayer ») ou d'ignorer la fonctionnalité. Si l'utilisateur dispose de plusieurs clients (pris en charge), ils peuvent activer/désactiver la boîte de réception Prioritaire individuellement dans chacun d'eux. Le conseil se présente ainsi :</span><span class="sxs-lookup"><span data-stu-id="e577b-p107">If you're switching from Clutter to Focused Inbox, they can decide to enable it ("Try it") or dismiss the feature. If the user has multiple (supported) clients, they can enable/disable Focused Inbox individually on each one. The tip looks like this:</span></span>
  
![Une image illustrant l’apparence de la boîte de réception Prioritaire lorsqu’elle est déployée pour vos utilisateurs et qu’Outlook est rouvert.](../../media/c034f969-d650-4333-88f1-dd10ade0a94c.png)
  
<span data-ttu-id="e577b-p108">Lorsqu’un utilisateur décide d’utiliser la boîte de réception Prioritaire, Courrier pêle-mêle est désactivé automatiquement. Le dossier Courrier pêle-mêle est converti en un dossier standard que l’utilisateur peut renommer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="e577b-p108">When a user decides to start using Focused Inbox, Clutter gets disabled automatically. The Clutter folder gets converted into a standard folder, that allows the user to rename or delete it.</span></span>
  
## <a name="turn-focused-inbox-on-or-off-for-specific-users"></a><span data-ttu-id="e577b-138">Activer ou désactiver la boîte de réception Prioritaire pour des utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="e577b-138">Turn Focused Inbox On or Off for specific users</span></span>

<span data-ttu-id="e577b-p109">Cet exemple **désactive** la boîte de réception Prioritaire pour Tim Matthews, de l’organisation Contoso. Mais cela ne l’empêche pas d’y accéder. S’il le souhaite, il peut toujours réactiver la boîte de réception Prioritaire sur chacun de ses clients.</span><span class="sxs-lookup"><span data-stu-id="e577b-p109">This example turns Focused Inbox **Off** for Tim Matthews in the Contoso organization. However, it doesn't block the availability of the feature to him. If his wants, he can still re-enable Focused Inbox again on each of his clients.</span></span> 
  
1. <span data-ttu-id="e577b-142">[Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="e577b-142">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>

2. <span data-ttu-id="e577b-p110">Pour effectuer ces procédures, vous devez disposer des autorisations appropriées. Pour connaître les autorisations requises, reportez-vous à l’entrée « Règles de transport » de la rubrique Autorisations relatives à la conformité et à la stratégie de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e577b-p110">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the Messaging policy and compliance permissions topic.</span></span>

3. <span data-ttu-id="e577b-145">Exécutez l’applet de commande **Get-FocusedInbox**, par exemple :</span><span class="sxs-lookup"><span data-stu-id="e577b-145">Run the **Get-FocusedInbox** cmdlet, for example:</span></span> 

 ``` PowerShell
 Get-FocusedInbox -Identity <tim@contoso.com>
 ```

4. <span data-ttu-id="e577b-146">Recherchez FocusedInboxOn pour afficher son paramètre actuel :</span><span class="sxs-lookup"><span data-stu-id="e577b-146">Look for FocusedInboxOn to view its current setting:</span></span>

    ![Réponse de PowerShell sur l’état de la boîte de réception Prioritaire.](../../media/419d8caa-89b9-45c5-91d9-8c023297456e.png)
  
5. <span data-ttu-id="e577b-148">Exécutez l'applet de commande suivante pour désactiver la boîte de réception Prioritaire :</span><span class="sxs-lookup"><span data-stu-id="e577b-148">Run the following cmdlet to turn Focused Inbox off:</span></span>

 ``` PowerShell
 Set-FocusedInbox -Identity <tim@contoso.com> -FocusedInboxOn $false
 ```

6. <span data-ttu-id="e577b-149">OU, exécutez l’applet de commande suivante pour l’activer :</span><span class="sxs-lookup"><span data-stu-id="e577b-149">OR, run the following cmdlet to turn it on:</span></span>

 ``` PowerShell
 Set-FocusedInbox -Identity <tim@contoso.com> -FocusedInboxOn $true
 ```

## <a name="use-the-ui-to-create-a-transport-rule-to-direct-email-messages-to-the-focused-view-for-all-your-users"></a><span data-ttu-id="e577b-150">Utilisez l’interface utilisateur pour créer une règle de transport permettant de diriger les messages e-mail vers l’affichage Prioritaire pour tous vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e577b-150">Use the UI to create a transport rule to direct email messages to the Focused view for all your users</span></span>

1. <span data-ttu-id="e577b-151">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="e577b-151">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>

2. <span data-ttu-id="e577b-152">Accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="e577b-152">Navigate to **mail flow** \> **Rules**.</span></span> <span data-ttu-id="e577b-153">Cliquez sur ![Ajouter icône EAC](../../media/795e5bdd-48bb-433f-8e07-3c7a19f8eca2.gif), puis sélectionnez **Créer une règle...**</span><span class="sxs-lookup"><span data-stu-id="e577b-153">Select ![EAC Add icon](../../media/795e5bdd-48bb-433f-8e07-3c7a19f8eca2.gif) and then select **Create a new rule...**.</span></span> 

3. <span data-ttu-id="e577b-154">Après avoir créé la règle, cliquez sur **Enregistrer** pour démarrer la règle.</span><span class="sxs-lookup"><span data-stu-id="e577b-154">After you're done creating the new rule, select **Save** to start the rule.</span></span>

    <span data-ttu-id="e577b-155">L'image suivante présente un exemple permettant de remettre tous les messages des « Ressources Humaines » dans la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-155">The following image shows an example where all messages From "Payroll Department" are to be delivered to the Focused Inbox.</span></span>

    ![paie focusedinbox](../../media/focusedinbox-transport-rule.PNG)

> [!NOTE]
> <span data-ttu-id="e577b-157">Dans cet exemple, le texte de la valeur de l’en-tête du message est **X-MS-Exchange-Organization-BypassFocusedInbox**.</span><span class="sxs-lookup"><span data-stu-id="e577b-157">The message header value text in this example is, **X-MS-Exchange-Organization-BypassFocusedInbox**.</span></span>
  
## <a name="use-powershell-to-create-a-transport-rule-to-direct-email-messages-to-the-focused-view-for-all-your-users"></a><span data-ttu-id="e577b-158">Utilisez PowerShell pour créer une règle de transport permettant de diriger les messages e-mail vers l’affichage Prioritaire pour tous vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e577b-158">Use PowerShell to create a transport rule to direct email messages to the Focused view for all your users</span></span>

1. <span data-ttu-id="e577b-159">[Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="e577b-159">[Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>

2. <span data-ttu-id="e577b-p112">Pour effectuer ces procédures, vous devez disposer des autorisations appropriées. Pour connaître les autorisations requises, reportez-vous à l'entrée « Règles de transport » de [Autorisations relatives à la conformité et à la stratégie de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span><span class="sxs-lookup"><span data-stu-id="e577b-p112">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Messaging policy and compliance permissions](https://go.microsoft.com/fwlink/p/?LinkId=829796).</span></span>

3. <span data-ttu-id="e577b-162">Exécutez la commande suivante pour remettre tous les messages du « Service Paie », par exemple, à la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-162">Run the following command to allow all messages from "Payroll Department," for example, to be delivered to the Focused Inbox.</span></span>

 ``` PowerShell
 New-TransportRule -Name <name_of_the_rule> -From "Payroll Department" -SetHeaderName "X-MS-Exchange-Organization-BypassFocusedInbox" -SetHeaderValue "true"
 ```

> [!IMPORTANT]
> <span data-ttu-id="e577b-163">Dans cet exemple, « X-MS-Exchange-Organization-BypassFocusedInbox » et « true » sont sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e577b-163">In this example, both "X-MS-Exchange-Organization-BypassFocusedInbox" and "true" are case sensitive.</span></span>
> <span data-ttu-id="e577b-164">De plus, la boîte de réception Prioritaire respectera l’en-tête X qui contourne le courrier pêle-mêle. Par conséquent, si vous utilisez ce paramètre dans le courrier pêle-mêle, il sera utilisé dans la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-164">Also, Focused Inbox will honor the X-header that bypasses Clutter, so if you use this setting in Clutter, it will be used in Focused Inbox.</span></span> <span data-ttu-id="e577b-165">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-TransportRule](https://go.microsoft.com/fwlink/p/?LinkId=830194).</span><span class="sxs-lookup"><span data-stu-id="e577b-165">For detailed syntax and parameter information, see [New-TransportRule](https://go.microsoft.com/fwlink/p/?LinkId=830194).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e577b-166">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="e577b-166">How do you know this worked?</span></span>

<span data-ttu-id="e577b-167">Vérifiez les en-têtes des messages e-mail pour déterminer si les messages sont acheminés vers la boîte de réception suite au contournement de la règle de transport Boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-167">You can check email message headers to see if the email messages are landing in the Inbox due to the Focused Inbox transport rule bypass.</span></span> <span data-ttu-id="e577b-168">Sélectionnez un e-mail dans une boîte aux lettres de votre organisation sur laquelle la règle de transport Boîte de réception Prioritaire est appliquée.</span><span class="sxs-lookup"><span data-stu-id="e577b-168">Pick an email message from a mailbox in your organization that has the Focused Inbox transport rule applied.</span></span> <span data-ttu-id="e577b-169">Examinez les en-têtes du message. L’en-tête suivant doit y figurer : **X-MS-Exchange-Organization-BypassFocusedInbox: true**.</span><span class="sxs-lookup"><span data-stu-id="e577b-169">Look at the headers stamped on the message, and you should see the **X-MS-Exchange-Organization-BypassFocusedInbox: true** header.</span></span> <span data-ttu-id="e577b-170">Cela signifie que le contournement fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e577b-170">This means the bypass is working.</span></span> <span data-ttu-id="e577b-171">Consultez l'article [Afficher les informations d'en-tête Internet des messages électroniques](https://go.microsoft.com/fwlink/p/?LinkId=822530) pour plus d'informations sur la façon de rechercher des informations d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="e577b-171">Check out the [View the Internet header information for an email message](https://go.microsoft.com/fwlink/p/?LinkId=822530) article for info on how to find the header information.</span></span>

## <a name="turn-onoff-clutter"></a><span data-ttu-id="e577b-172">Activer/désactiver la fonctionnalité Courrier pêle-mêle</span><span class="sxs-lookup"><span data-stu-id="e577b-172">Turn on/off Clutter</span></span>

<span data-ttu-id="e577b-p115">Nous avons reçu des indications selon lesquelles le Courrier pêle-mêle a soudainement cessé de fonctionner pour certains utilisateurs. Dans ce cas, vous pouvez le réactiver pour des utilisateurs spécifiques. Voir [Configurer le Courrier pêle-mêle pour votre organisation](../email/configure-clutter.md).</span><span class="sxs-lookup"><span data-stu-id="e577b-p115">We've received reports that Clutter suddenly stopped working for some users. If this happens, you can enable it again for specific users. See [Configure Clutter for your organization](../email/configure-clutter.md).</span></span>

## <a name="faq-for-focused-inbox"></a><span data-ttu-id="e577b-176">FAQ sur la boîte de réception Prioritaire</span><span class="sxs-lookup"><span data-stu-id="e577b-176">FAQ for Focused Inbox</span></span>

<span data-ttu-id="e577b-177">Voici des réponses aux questions fréquemment posées sur la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-177">Here are answers to Frequently Asked Questions about Focused Inbox.</span></span>

### <a name="can-i-control-how-i-roll-out-focused-inbox-in-my-organization"></a><span data-ttu-id="e577b-178">Puis-je contrôler le déploiement de la boîte de réception Prioritaire au sein de mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="e577b-178">Can I control how I roll out Focused Inbox in my organization?</span></span>

<span data-ttu-id="e577b-p116">Oui. Vous pouvez activer ou désactiver la boîte de réception Prioritaire pour l’ensemble de votre organisation ou pour des utilisateurs spécifiques. Voir ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e577b-p116">Yes. You can turn Focused Inbox on or off for your entire organization, or you can turn it on or off for specified users. See above.</span></span>
  
### <a name="is-the-focused-inbox-feature-only-available-for-office-2016-clients"></a><span data-ttu-id="e577b-182">La fonctionnalité boîte de réception Prioritaire est-elle disponible pour les clients Office 2016 ?</span><span class="sxs-lookup"><span data-stu-id="e577b-182">Is the Focused Inbox feature ONLY available for Office 2016 clients?</span></span>

<span data-ttu-id="e577b-183">Oui, seuls les utilisateurs d’Office 2016 sont concernés.</span><span class="sxs-lookup"><span data-stu-id="e577b-183">Yes, only users with Office 2016 are affected.</span></span> <span data-ttu-id="e577b-184">La fonctionnalité ne sera pas rétroportée vers Outlook 2013 ou version précédente.</span><span class="sxs-lookup"><span data-stu-id="e577b-184">The feature is not going to be backported to Outlook 2013 or earlier.</span></span>
  
### <a name="how-long-does-it-take-for-focused-inbox-changes-to-take-place-in-outlook"></a><span data-ttu-id="e577b-185">Combien de temps faut-il pour que les modifications apportées à la boîte de réception Prioritaire s’appliquent à Outlook ?</span><span class="sxs-lookup"><span data-stu-id="e577b-185">How long does it take for Focused Inbox changes to take place in Outlook?</span></span>

<span data-ttu-id="e577b-186">Lorsque vous activez ou désactivez la boîte de réception Prioritaire, les paramètres s’appliquent dès que vos utilisateurs ferment et redémarrent Outlook.</span><span class="sxs-lookup"><span data-stu-id="e577b-186">Once you turn on or turn off Focused Inbox, the settings will take effect once your users close and restart Outlook.</span></span>
  
### <a name="what-happens-to-clutter-once-i-turn-on-focused-inbox"></a><span data-ttu-id="e577b-187">Que devient le courrier pêle-mêle lorsque j’active la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="e577b-187">What happens to Clutter once I turn on Focused Inbox?</span></span>

<span data-ttu-id="e577b-p118">Après avoir effectué la transition, vous ne recevrez plus d’e-mails moins actionables dans le dossier Courrier pêle-mêle. Au lieu de cela, les e-mails seront répartis entre les onglets Prioritaire et Autres dans votre boîte de réception. Le même algorithme qui déplaçait les éléments vers le dossier Courrier pêle-mêle est utilisé pour la fonctionnalité Boîte de réception Prioritaire. Cela signifie que les e-mails qui étaient auparavant paramétrés pour être déplacés dans le dossier Courrier pêle-mêle seront déplacés dans la boîte de réception Autres. Tous les e-mails déjà présents dans votre dossier Courrier pêle-mêle y resteront tant que vous n’aurez pas décidé de les supprimer ou de les déplacer.</span><span class="sxs-lookup"><span data-stu-id="e577b-p118">After switching, you'll no longer receive less actionable email in the Clutter folder. Instead, email will be split between the Focused and Other tabs in your inbox. The same algorithm that moved items to the Clutter folder now powers Focused Inbox, meaning that any emails that were set to move to Clutter will now be moved to Other. Any messages already in your Clutter folder will remain there until you decide to delete or move them.</span></span>
  
<span data-ttu-id="e577b-192">Consultez ce billet rédigé par [Tony Redmond](https://www.petri.com/author/tony-redmond), Microsoft MVP : [De quelle façon la boîte de réception Prioritaire remplace-t-elle le courrier pêle-mêle dans Office 365 ?](https://www.petri.com/focused-inbox-office-365)</span><span class="sxs-lookup"><span data-stu-id="e577b-192">Check out this post by [Tony Redmond](https://www.petri.com/author/tony-redmond), Microsoft MVP: [How the Focused Inbox Replaces Clutter Inside Office 365](https://www.petri.com/focused-inbox-office-365).</span></span>
  
### <a name="can-i-keep-users-on-clutter-what-is-microsofts-recommendation-when-it-comes-to-using-clutter-vs-focused-inbox"></a><span data-ttu-id="e577b-193">Puis-je maintenir des utilisateurs sur le courrier pêle-mêle ?</span><span class="sxs-lookup"><span data-stu-id="e577b-193">Can I keep users on Clutter?</span></span> <span data-ttu-id="e577b-194">Microsoft recommande-t-il d'utiliser le courrier pêle-mêle ou la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="e577b-194">What is Microsoft's recommendation when it comes to using Clutter vs Focused Inbox?</span></span>

<span data-ttu-id="e577b-p120">Oui, vous pouvez maintenir des utilisateurs sur le courrier pêle-mêle et désactiver la boîte de réception Prioritaire. Toutefois, à terme, le courrier pêle-mêle finira par être remplacé par la boîte de réception Prioritaire, par conséquent Microsoft vous recommande de migrer vers la boîte de réception Prioritaire dès maintenant. Pour en savoir plus sur quand utiliser la fonctionnalité Courrier pêle-mêle avec Exchange Online, consultez ce billet de blog : [Mise à jour sur la boîte de réception Prioritaire et nos projets pour le courrier pêle-mêle](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448).</span><span class="sxs-lookup"><span data-stu-id="e577b-p120">Yes, you can keep users on Clutter and disable Focused Inbox, however, eventually Clutter will be fully replaced with Focused Inbox so Microsoft's recommends moving to Focused Inbox now. To learn more about when you use Clutter with Exchange Online, see this blog post: [Update on Focused Inbox and our plans for Clutter](https://techcommunity.microsoft.com/t5/Outlook-Blog/Update-on-Focused-Inbox-and-our-plans-for-Clutter/ba-p/136448).</span></span>
  
### <a name="should-i-disable-clutter-for-my-end-users-if-we-are-going-to-move-everyone-to-focused-inbox"></a><span data-ttu-id="e577b-197">Dois-je désactiver le courrier pêle-mêle pour mes utilisateurs finaux si nous migrons tout le monde vers la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="e577b-197">Should I disable Clutter for my end users if we are going to move everyone to Focused Inbox?</span></span>

<span data-ttu-id="e577b-p121">Non. Il est possible de désactiver le courrier pêle-mêle sur une boîte aux lettres explicite en exécutant l'applet de commande Set-Clutter. En revanche, dans ce cas, les messages précédemment redirigés vers le dossier Courrier pêle-mêle resteront dans la boîte de réception et le propriétaire de la boîte aux lettres devra les traiter en attendant que son client soit mis à niveau vers une version prenant en charge la fonctionnalité Boîte de réception Prioritaire. Il est donc préférable de ne pas désactiver le courrier pêle-mêle avant que les clients mis à niveau soient disponibles.</span><span class="sxs-lookup"><span data-stu-id="e577b-p121">No. It's possible to disable Clutter for a mailbox explicitly by running the Set-Clutter cmdlet. However, if you do this, the mailbox owner will see messages that were previously redirected to the Clutter folder remain in the Inbox and they'll have to process those messages until their client is upgraded to a version that supports the Focused Inbox. It's therefore best not to disable Clutter until the upgraded clients are available.</span></span>
  
### <a name="why-are-there-two-different-cmdlets-for-managing-focused-inbox"></a><span data-ttu-id="e577b-202">Pourquoi existe-t-il deux applets de commande distinctes pour gérer de la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="e577b-202">Why are there two different cmdlets for managing Focused Inbox?</span></span>

<span data-ttu-id="e577b-203">Deux états sont associés à la boîte de réception Prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e577b-203">There are two states associated with Focused Inbox.</span></span>
  
- <span data-ttu-id="e577b-204">**Niveau organisation** : état de la boîte de réception Prioritaire, et horodatage de la dernière mise à jour associée.</span><span class="sxs-lookup"><span data-stu-id="e577b-204">**Organization Level**: Focused Inbox state, and an associated last update time-stamp.</span></span>

- <span data-ttu-id="e577b-205">**Niveau boîte aux lettres** : état de la boîte de réception Prioritaire, et horodatage de la dernière mise à jour associée.</span><span class="sxs-lookup"><span data-stu-id="e577b-205">**Mailbox Level**: Focused Inbox state, and an associated last update time-stamp</span></span> 

### <a name="how-does-outlook-decide-to-show-the-focused-inbox-experience-with-these-two-states"></a><span data-ttu-id="e577b-206">Comment Outlook détermine-t-il l’expérience de boîte de réception Prioritaire affichée avec ces deux états ?</span><span class="sxs-lookup"><span data-stu-id="e577b-206">How does Outlook decide to show the Focused Inbox experience with these two states?</span></span>

<span data-ttu-id="e577b-p122">Outlook choisit l’applet de commande dont l’horodatage est le plus récent. Par défaut, les deux horodatages sont « null », auquel cas la fonctionnalité est activée.</span><span class="sxs-lookup"><span data-stu-id="e577b-p122">Outlook decides to show the experience by choosing which cmdlet has the latest time stamp. By default, both time stamps are "null" and in this case, the feature is enabled.</span></span>
  
### <a name="why-does-the-get-focusedinbox-cmdlet-return-true-when-ive-turned-focused-inbox-off-in-my-organization"></a><span data-ttu-id="e577b-209">Pourquoi l’applet de commande Get-FocusedInbox renvoie « true » alors que j’ai désactivé la boîte de réception Prioritaire au sein de mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="e577b-209">Why does the Get-FocusedInbox cmdlet return "true", when I've turned Focused Inbox off in my organization?</span></span>

<span data-ttu-id="e577b-p123">Deux applets de commande permettent de contrôler la boîte de réception Prioritaire. Lorsque vous exécutez Get-FocusedInbox pour une boîte aux lettres, l’état Niveau boîte aux lettres de la fonctionnalité est renvoyé. L’expérience Outlook choisie dépend du dernier état d’applet de commande qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="e577b-p123">There are two cmdlets for controlling Focused Inbox. When you run Get-FocusedInbox for a mailbox, it returns the mailbox level state of the feature. The experience in Outlook is chosen based on which cmdlet state was last modified.</span></span>
  
### <a name="can-i-run-a-script-to-see-who-has-turned-on-focused-inbox"></a><span data-ttu-id="e577b-213">Puis-je exécuter un script pour voir qui a activé la boîte de réception Prioritaire ?</span><span class="sxs-lookup"><span data-stu-id="e577b-213">Can I run a script to see who has turned on Focused Inbox?</span></span>

<span data-ttu-id="e577b-p124">Non et c’est tout à fait normal. L’activation de la boîte de réception Prioritaire est en effet un paramètre côté client. De ce fait, tout ce que l’applet de commande peut faire, c’est vous indiquer si la boîte aux lettres de l’utilisateur est éligible pour l’expérience client. Il est possible qu’elle soit simultanément activée dans certains clients et désactivée dans d’autres, par exemple, activée dans les applications Outlook et Outlook Mobile, mais désactivée dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="e577b-p124">No, and this is by design. Focused Inbox enablement is a client side setting, so all the cmdlet can do is tell you if the user's mailbox is eligible for the client experience. It is possible for it to be simultaneously enabled in some clients and disabled in others, for example, enabled in Outlook app and Outlook Mobile but disabled in Outlook on the web.</span></span>
