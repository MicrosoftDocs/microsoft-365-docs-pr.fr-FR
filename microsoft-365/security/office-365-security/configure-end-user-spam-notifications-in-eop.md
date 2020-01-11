---
title: Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: Vous pouvez configurer les notifications de courrier indésirable à l'utilisateur final pour la stratégie de filtrage de contenu par défaut à l'échelle de l'entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines.
ms.openlocfilehash: ea65081b1b312af3ee15335721ec042dc9d3b1da
ms.sourcegitcommit: 40e83b22b74db8e37d65e0988d4c11de3aa541b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/10/2020
ms.locfileid: "41022000"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a><span data-ttu-id="5a9c3-103">Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP</span><span class="sxs-lookup"><span data-stu-id="5a9c3-103">Configure end-user spam notifications in EOP</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5a9c3-104">Cette rubrique s'adresse aux clients autonomes Exchange Online Protection (EOP) qui protègent les boîtes aux lettres sur site.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-104">This topic is for Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes.</span></span> <span data-ttu-id="5a9c3-105">Les clients Exchange Online qui protègent les boîtes aux lettres hébergées dans le Cloud doivent plutôt lire la rubrique suivante : [configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="5a9c3-105">Exchange Online customers who are protecting cloud-hosted mailboxes should read the following topic instead: [Configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span></span> 
  
<span data-ttu-id="5a9c3-106">Vous pouvez configurer des notifications de courrier indésirable pour l’utilisateur final pour la stratégie de filtrage du courrier indésirable par défaut à l’échelle de l’entreprise ou pour des stratégies personnalisées</span><span class="sxs-lookup"><span data-stu-id="5a9c3-106">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies.</span></span> <span data-ttu-id="5a9c3-107">L’activation des messages de notification de courrier indésirable de l’utilisateur final permet aux utilisateurs de gérer leurs propres messages indésirables mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-107">Enabling end-user spam notification messages lets your users manage their own spam-quarantined messages.</span></span> 
  
<span data-ttu-id="5a9c3-p103">Les notifications de courrier indésirable à l'utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l'utilisateur final au cours d'une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="5a9c3-110">Après la réception d’un message de notification, les utilisateurs finaux peuvent choisir l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a9c3-110">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="5a9c3-111">**Bloquer l’expéditeur** si vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-111">**Block Sender** if you want Office 365 to add the sender to your blocked senders list.</span></span>

<span data-ttu-id="5a9c3-112">**Release** si le message n’est pas un courrier indésirable et que vous souhaitez qu’Office 365 envoie le message à votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-112">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="5a9c3-113">**Passez en revue** pour accéder au portail de mise en quarantaine dans le centre de sécurité et conformité si vous souhaitez effectuer d’autres actions, telles que l’aperçu ou la publication.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-113">**Review** to navigate to the Quarantine Portal within the Security and Compliance Center if you want to take other actions, such as Preview or Release.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="5a9c3-114">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5a9c3-114">What do you need to know before you begin?</span></span>
<span data-ttu-id="5a9c3-115"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="5a9c3-115"></span></span>

<span data-ttu-id="5a9c3-116">Durée d’exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="5a9c3-116">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="5a9c3-p104">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Blocage du courrier indésirable » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="5a9c3-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
  
<span data-ttu-id="5a9c3-119">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="5a9c3-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="5a9c3-120">Utiliser le Centre d’administration Exchange (CAE) pour configurer les notifications de courrier indésirable à l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="5a9c3-120">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="5a9c3-121">Dans le centre d’administration Exchange, accédez à **protection** > **anti-spam Filter**.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-121">In the Exchange Admin Center (EAC), navigate to **Protection** > **Spam filter**.</span></span>
    
2. <span data-ttu-id="5a9c3-122">Sélectionnez la stratégie de filtrage de contenu pour laquelle vous voulez activer les notifications de courrier indésirable à l'utilisateur final (elles sont désactivées par défaut).</span><span class="sxs-lookup"><span data-stu-id="5a9c3-122">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="5a9c3-123">Dans le volet de droite, dans lequel apparaissent des informations récapitulatives sur votre stratégie, cliquez sur le lien **Configurer les notifications de courrier indésirable à l'utilisateur final**.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-123">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="5a9c3-124">Dans la boîte de dialogue, vous pouvez configurer les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a9c3-124">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="5a9c3-p105">**Activer les notifications de courrier indésirable à l'utilisateur final** Cochez cette case pour activer les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. (À l'inverse, si la stratégie est activée, vous pouvez décocher cette case pour désactiver les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.)</span><span class="sxs-lookup"><span data-stu-id="5a9c3-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="5a9c3-p106">**Envoyer des notifications de courrier indésirable à l'utilisateur final tous les (jours)** Spécifiez la fréquence d'envoi des notifications de courrier indésirable à l'utilisateur final. La valeur par défaut est 3 jours. Vous pouvez indiquer une valeur comprise entre 1 et 15 jours. Par exemple, si vous spécifiez 7 jours, la notification inclura la liste de tous les messages destinés à cet utilisateur au cours des 7 derniers jours qui ont été mis en quarantaine à la place.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="5a9c3-131">**Langue de la notification** Dans la liste déroulante, sélectionnez la langue dans laquelle écrire les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-131">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="5a9c3-p107">Cliquez sur **Enregistrer**. Un récapitulatif de vos paramètres de stratégie de filtrage de contenu, y compris vos paramètres de notification de courrier indésirable à l'utilisateur final, apparaît dans le volet de droite.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-p107">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="5a9c3-p108">Les notifications de courrier indésirable à l'utilisateur final ne sont opérationnelles que pour les stratégies de filtrage de contenu activées. >  Les notifications de courrier indésirable pour l'utilisateur final sont envoyées uniquement une fois par jour. Le délai de remise de la notification ne peut pas être garanti pour chaque client et n'est pas configurable.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-p108">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="5a9c3-137">**Conseil :** si vous voulez tester les notifications de courrier indésirable destinées aux utilisateurs finals en les envoyant à un ensemble limité d'utilisateurs avant de les implémenter totalement, créez une stratégie de filtrage de contenu personnalisée autorisant ces notifications de courrier indésirable pour les domaines dans lesquels les utilisateurs résident.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-137">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside.</span></span> <span data-ttu-id="5a9c3-138">Ensuite, dans le centre d’administration Exchange, sous **règles de flux \> de messagerie**, créez une règle de flux de messagerie (également appelée règle de transport) pour bloquer les messages de Quarantine@messaging.microsoft.com (adresse de messagerie qui envoie des notifications) avec des exceptions pour les utilisateurs qui doivent recevoir les notifications.</span><span class="sxs-lookup"><span data-stu-id="5a9c3-138">Then, in the EAC, under **Mail flow \> rules**, create a mail flow rule (also known as a transport rule) to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications.</span></span> <span data-ttu-id="5a9c3-139">L'image suivante représente un exemple de création d'exception pour deux utilisateurs (SaraD et AlexD) du domaine Contoso.com :</span><span class="sxs-lookup"><span data-stu-id="5a9c3-139">The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](../media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="5a9c3-141">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="5a9c3-141">For more information</span></span>

[<span data-ttu-id="5a9c3-142">Configurer vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="5a9c3-142">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
