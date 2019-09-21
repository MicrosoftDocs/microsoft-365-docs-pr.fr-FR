---
title: Configurer la stratégie anti-courrier indésirable sortant
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l’envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires.
ms.openlocfilehash: 9c8c2f7e9ff0be02f11fa66409690cbb854d8c56
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079445"
---
# <a name="configure-the-outbound-spam-policy"></a><span data-ttu-id="c41c1-103">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="c41c1-103">Configure the outbound spam policy</span></span>

<span data-ttu-id="c41c1-p101">Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l'envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires. Comme pour le filtrage entrant, le filtrage de courrier indésirable sortant comprend le filtrage de connexion et le filtrage de contenu. Toutefois, les paramètres de filtrage sortant ne peuvent pas être configurés. Si un message sortant est déterminé comme étant du courrier indésirable, il est routé via le pool de remise à risque plus élevé, ce qui réduit la probabilité d'ajout du pool d'IP sortantes normales à une liste rouge. Si un client continue à envoyer du courrier indésirable sortant au service, ses messages sont bloqués. Bien que le filtrage de courrier indésirable sortant ne puisse pas être désactivé ou modifié, vous pouvez configurer plusieurs paramètres de courrier indésirable à l'échelle de l'entreprise via la stratégie de courrier indésirable sortant par défaut.</span><span class="sxs-lookup"><span data-stu-id="c41c1-p101">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients. Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable. If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list. If a customer continues to send outbound spam through the service, they will be blocked from sending messages. Although outbound spam filtering cannot be disabled or changed, you can configure several company-wide outbound spam settings via the default outbound spam policy.</span></span> 
  
<span data-ttu-id="c41c1-109">La vidéo suivante illustre la configuration de la stratégie de courrier indésirable sortant :</span><span class="sxs-lookup"><span data-stu-id="c41c1-109">The following video shows how to configure the outbound spam policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
> [!NOTE]
> <span data-ttu-id="c41c1-110">Pour obtenir les meilleurs résultats de filtrage, le contenu de la vidéo ci-dessus doit être utilisé avec une configuration correcte et une connaissance des [contrôles de courrier indésirable sortants dans Office 365](https://docs.microsoft.com/office365/securitycompliance/outbound-spam-controls).</span><span class="sxs-lookup"><span data-stu-id="c41c1-110">For the best filtering results, the content in the video above should used with a proper setup, and familiarity with [Outbound spam controls in Office 365](https://docs.microsoft.com/office365/securitycompliance/outbound-spam-controls).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c41c1-111">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c41c1-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="c41c1-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="c41c1-112"></span></span>

<span data-ttu-id="c41c1-113">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="c41c1-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="c41c1-114">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="c41c1-114">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="c41c1-115">Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c41c1-115">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="c41c1-116">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="c41c1-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
  
<span data-ttu-id="c41c1-117">La procédure suivante peut également être exécutée par le biais du service PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="c41c1-117">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="c41c1-118">Utilisez la cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) pour vérifier vos paramètres et la cmdlet [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) pour modifier les paramètres de votre stratégie anti-courrier indésirable sortant.</span><span class="sxs-lookup"><span data-stu-id="c41c1-118">Use the [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet to review your settings, and the [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) to edit your outbound spam policy settings.</span></span> <span data-ttu-id="c41c1-119">Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).</span><span class="sxs-lookup"><span data-stu-id="c41c1-119">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).</span></span> <span data-ttu-id="c41c1-120">Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="c41c1-120">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a><span data-ttu-id="c41c1-121">Utiliser le Centre d'administration Exchange (CAE) pour modifier la stratégie de courrier indésirable sortant par défaut</span><span class="sxs-lookup"><span data-stu-id="c41c1-121">Use the EAC to edit the default outbound spam policy</span></span>
<span data-ttu-id="c41c1-122"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="c41c1-122"></span></span>

<span data-ttu-id="c41c1-123">La procédure suivante vous permet de modifier la stratégie de courrier indésirable sortant par défaut :</span><span class="sxs-lookup"><span data-stu-id="c41c1-123">Use the following procedure to edit the default outbound spam policy:</span></span>
  
### <a name="to-configure-the-default-outbound-spam-policy"></a><span data-ttu-id="c41c1-124">Pour configurer la stratégie de courrier indésirable sortant par défaut</span><span class="sxs-lookup"><span data-stu-id="c41c1-124">To configure the default outbound spam policy</span></span>

1. <span data-ttu-id="c41c1-125">Dans le CAE, accédez à **Protection**\> **Courrier indésirable sortant**, puis double-cliquez sur la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="c41c1-125">In the Exchange admin center (EAC), navigate to **Protection** \> **Outbound spam**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="c41c1-126">Sélectionnez l'option de menu **Préférences de courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="c41c1-126">Select the **Outbound spam preferences** menu option.</span></span> 
    
3. <span data-ttu-id="c41c1-127">Cochez les cases suivantes relatives aux messages sortants, puis spécifiez une ou plusieurs adresses de messagerie associées dans la zone de texte connexe (il peut s'agir de listes de distribution si elles se résolvent en tant que destinations SMTP valides) :</span><span class="sxs-lookup"><span data-stu-id="c41c1-127">Select the following check boxes pertaining to outbound messages, and then specify an associated email address or addresses in the accompanying input box (these can be distribution lists if they resolve as valid SMTP destinations):</span></span>
    
1. <span data-ttu-id="c41c1-p104">**Envoyer une copie de tous les messages électroniques sortants suspects à l'adresse ou aux adresses de messagerie suivantes**. Il s'agit de messages marqués comme étant courriers indésirables par le filtre (quelle que soit la valeur SCL). Le filtre ne les rejette pas, mais ils sont routés via le pool de remise à risque plus élevé. S'il y a plusieurs adresses, utilisez un point-virgule pour les séparer. Notez que les destinataires spécifiés recevront les messages en tant qu'adresse Cci (les champs De et À correspondent à l'expéditeur et au destinataire initiaux).</span><span class="sxs-lookup"><span data-stu-id="c41c1-p104">**Send a copy of all suspicious outbound email messages to the following email address or addresses**. These are messages that are marked as spam by the filter (regardless of the SCL rating). They are not rejected by the filter but are routed through the higher risk delivery pool. Separate multiple addresses with a semicolon. Note that the recipients specified will receive the messages as a Blind carbon copy (Bcc) address (the From and To fields are the original sender and recipient).</span></span>
    
2. <span data-ttu-id="c41c1-p105">**Envoyer une notification à l'adresse de messagerie suivante quand un utilisateur est bloqué en relation avec l'envoi de courrier indésirable sortant**. S'il y a plusieurs adresses, utilisez un point-virgule pour les séparer.</span><span class="sxs-lookup"><span data-stu-id="c41c1-p105">**Send a notification to the following email address when a sender is blocked sending outbound spam**. Separate multiple addresses with a semicolon.</span></span>
    
    <span data-ttu-id="c41c1-p106">Quand une quantité importante de courriers indésirables provenant d'un utilisateur en particulier est détectée, cet utilisateur est désactivé et ne peut plus envoyer de messages électroniques. L'administrateur du domaine, spécifié à l'aide de ce paramètre, est informé que l'envoi de messages sortants est bloqué pour cet utilisateur. Pour savoir à quoi ressemble cette notification, voir [Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Pour plus d'informations sur le mode de réactivaction, consultez la rubrique [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="c41c1-p106">When a significant amount of spam is originating from a particular user, the user is disabled from sending email messages. The administrator for the domain, who is specified using this setting, will be informed that outbound messages are blocked for this user. To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>
    
4. <span data-ttu-id="c41c1-p107">Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie par défaut s'affiche dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="c41c1-p107">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="c41c1-141">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="c41c1-141">For more information</span></span>
<span data-ttu-id="c41c1-142"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="c41c1-142"></span></span>

[<span data-ttu-id="c41c1-143">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="c41c1-143">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)
  
[<span data-ttu-id="c41c1-144">FAQ sur la protection contre le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c41c1-144">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

