---
title: Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 7/16/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à acheminer le courrier indésirable vers les dossiers de courrier indésirable de l’utilisateur dans Exchange Online Protection.
ms.openlocfilehash: f47b7821fd6cceb02501c559a0a776c4cdaf315f
ms.sourcegitcommit: ba223b4fd069fc6fd09c2a2e34c770a18bc7b2a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2019
ms.locfileid: "39866766"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="e075d-103">Vérification de l’acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur</span><span class="sxs-lookup"><span data-stu-id="e075d-103">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e075d-p101">Cette rubrique s'applique uniquement aux clients Exchange Online Protection (EOP) qui hébergent des boîtes aux lettres localement dans un déploiement hybride. Les clients Exchange Online dont les boîtes aux lettres sont entièrement hébergées dans Office 365 n'ont pas besoin d'exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="e075d-p101">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment. Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span>

<span data-ttu-id="e075d-106">L'action anti-courrier indésirable par défaut pour les clients EOP consiste à déplacer les messages identifiés comme tels vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="e075d-106">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder.</span></span> <span data-ttu-id="e075d-107">Pour que cette action fonctionne avec les boîtes aux lettres locales, vous devez configurer des règles de flux de messagerie Exchange (également appelées règles de transport) sur vos serveurs Edge ou Hub sur site afin de détecter les en-têtes de courrier indésirable ajoutés par EOP.</span><span class="sxs-lookup"><span data-stu-id="e075d-107">In order for this action to work with on-premises mailboxes, you must configure Exchange mail flow rules (also known as transport rules) on your on-premises Edge or Hub servers to detect spam headers added by EOP.</span></span> <span data-ttu-id="e075d-108">Ces règles de flux de messagerie définissent le seuil de probabilité de courrier indésirable (SCL) utilisé par la propriété SclJunkThreshold de l’applet de commande Set-OrganizationConfig pour déplacer le courrier indésirable dans le dossier courrier indésirable de chaque boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e075d-108">These mail flow rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span>

### <a name="to-add-mail-flow-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="e075d-109">Pour ajouter des règles de flux de messagerie afin de vous assurer que le courrier indésirable est déplacé vers le dossier courrier indésirable à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e075d-109">To add mail flow rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="e075d-p103">Accédez au Environnement de ligne de commande Exchange Management Shell de votre serveur Exchange local. Pour apprendre à ouvrir l'environnement de ligne de commande Environnement de ligne de commande Exchange Management Shell dans votre organisation Exchange locale, reportez-vous à **Open the Shell**.</span><span class="sxs-lookup"><span data-stu-id="e075d-p103">Access the Exchange Management Shell for your on-premises Exchange server. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>

2. <span data-ttu-id="e075d-112">Exécutez la commande suivante pour router le courrier indésirable filtré sur le contenu dans le dossier Courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="e075d-112">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>

   ```Powershell
   New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
   ```

   <span data-ttu-id="e075d-113">Où _NameForRule_ est le nom de la nouvelle règle, par exemple JunkContentFilteredMail.</span><span class="sxs-lookup"><span data-stu-id="e075d-113">Where _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span>

3. <span data-ttu-id="e075d-114">Exécutez la commande suivante pour router les messages marqués en tant que courrier indésirable avant qu’ils atteignent le filtre de contenu dans le dossier Courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="e075d-114">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>

   ```Powershell
   New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
   ```

   <span data-ttu-id="e075d-115">Où _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailBeforeReachingContentFilter.</span><span class="sxs-lookup"><span data-stu-id="e075d-115">Where _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span>

4. <span data-ttu-id="e075d-116">Exécutez la commande suivante pour vous assurer que les messages provenant des expéditeurs d'une liste rouge dans la stratégie de filtre de courrier indésirable, telle que la liste d' **expéditeurs bloqués**, sont acheminés vers le dossier Courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="e075d-116">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span>

   ```Powershell
   New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
   ```

   <span data-ttu-id="e075d-117">Où _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailInSenderBlockList.</span><span class="sxs-lookup"><span data-stu-id="e075d-117">Where _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span>

<span data-ttu-id="e075d-p104">Si vous ne souhaitez pas utiliser l'action **Déplacer le message dans le dossier Courrier indésirable**, vous pouvez choisir une autre action parmi vos stratégies de filtrage de contenu dans le Centre d'administration Exchange. Pour plus d'informations, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur ces champs dans l'en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="e075d-p104">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>

> [!TIP]
> <span data-ttu-id="e075d-121">Si vous ne souhaitez pas utiliser l’action **déplacer le message vers le dossier courrier indésirable** , vous pouvez choisir une autre action dans vos stratégies de filtrage de contenu dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="e075d-121">If you don't want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="e075d-122">Pour plus d'informations, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e075d-122">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="e075d-123">Pour plus d'informations sur ces champs dans l'en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="e075d-123">For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e075d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e075d-124">See also</span></span>

[<span data-ttu-id="e075d-125">New-TransportRule</span><span class="sxs-lookup"><span data-stu-id="e075d-125">New-TransportRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-transportrule)
