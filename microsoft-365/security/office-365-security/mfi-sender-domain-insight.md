---
title: Informations sur la correction du domaine de l’expéditeur
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur la rubrique Fix sender Domain Insight dans le tableau de bord du flux de messagerie dans le centre de sécurité & Compliance Center.
ms.openlocfilehash: c4cf4a87ad770325ca6ad2f0b87ac8ce52c345c2
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44818830"
---
# <a name="fix-sender-domain-insight"></a><span data-ttu-id="f8563-103">Informations sur la correction du domaine de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="f8563-103">Fix sender domain insight</span></span>

<span data-ttu-id="f8563-104">Microsoft 365 nécessite des messages envoyés à partir d’environnements de messagerie internes locaux à Microsoft 365 pour répondre à certains critères de sécurité :</span><span class="sxs-lookup"><span data-stu-id="f8563-104">Microsoft 365 requires messages sending from internal on-premises email environments to Microsoft 365 to meet certain security criteria:</span></span>

- <span data-ttu-id="f8563-105">Vous avez créé un connecteur entrant dans Microsoft 365 pour authentifier les connexions SMTP à partir de votre serveur de messagerie local à l’aide de l’adresse IP source ou d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="f8563-105">You've created an inbound connector in Microsoft 365 to authenticate SMTP connections from your on-premises email server by using the source IP address or a certificate.</span></span>

- <span data-ttu-id="f8563-106">Vous avez configuré votre serveur de messagerie local de sorte qu’il relaie le courrier électronique via Microsoft 365 vers le monde externe.</span><span class="sxs-lookup"><span data-stu-id="f8563-106">You've configured your on-premises email server to relay email via Microsoft 365 to external world.</span></span>

- <span data-ttu-id="f8563-107">Dans votre configuration, l’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="f8563-107">In your configuration, one of the following statements is true:</span></span>

  - <span data-ttu-id="f8563-108">Le domaine de messagerie de l’expéditeur est enregistré dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8563-108">The sender's email domain is registered in your organization.</span></span> <span data-ttu-id="f8563-109">Pour plus d’informations, consultez l’article Ajouter un domaine à Office 365.</span><span class="sxs-lookup"><span data-stu-id="f8563-109">For more information, see Add Domains in Office 365.</span></span>

  - <span data-ttu-id="f8563-110">Votre serveur de messagerie local est configuré pour utiliser un certificat pour envoyer un message électronique à Microsoft 365, le certificat contient ou correspond exactement à un nom de domaine que vous avez enregistré dans Microsoft 365, et vous avez créé un connecteur basé sur un certificat dans Microsoft 365 avec ce domaine.</span><span class="sxs-lookup"><span data-stu-id="f8563-110">Your on-premises email server is configured to use a certificate to send email to Microsoft 365, the certificate contains or exactly matches a domain name that you've registered in Microsoft 365, and you've created a certificate based connector in Microsoft 365 with that domain.</span></span> 

<span data-ttu-id="f8563-111">Les messages qui ne répondent pas aux critères ne sont pas attribués à l’organisation et peuvent être rejetés.</span><span class="sxs-lookup"><span data-stu-id="f8563-111">Messages that don't meet the criteria will not be attributed to the organization and could be rejected.</span></span>

<span data-ttu-id="f8563-112">L’article **Fix sender Domain** Insight affiche les messages électroniques provenant de votre environnement local qui ne répondent pas aux critères, vous permet d’identifier les ordinateurs et les comptes d’utilisateur potentiellement compromis dans votre environnement de messagerie local et vous aide à prendre des mesures correctives.</span><span class="sxs-lookup"><span data-stu-id="f8563-112">The **Fix sender domain** insight shows you email from your on-premises environment that doesn't meet the criteria, helps you to identify potentially compromised machines and user accounts in your on-premises email environment, and helps you to take remediation actions.</span></span>

![Le tableau de bord des expéditeurs du tableau de bord du flux de messagerie dans le centre de sécurité & conformité](../../media/sender-domain-insight-selected.png)

<span data-ttu-id="f8563-114">Lorsque vous cliquez sur **afficher les détails**, vous êtes dirigé vers un autre widget avec plus de détails, comme illustré dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="f8563-114">When you click **View details**, you are taken to another widget with more details as shown in the following diagram:</span></span>

![Le widget détails de la solution Fix sender Domain Insight](../../media/sender-domain-view-details.png)

<span data-ttu-id="f8563-116">Vous verrez le connecteur entrant qui a été utilisé pour livrer les messages à Office 365.</span><span class="sxs-lookup"><span data-stu-id="f8563-116">You'll see the inbound connector that was used to deliver the messages to Office 365.</span></span> <span data-ttu-id="f8563-117">Vous pouvez également cliquer sur **afficher un exemple d’ID de message** pour afficher les détails des messages qui ont été envoyés à partir de votre environnement de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="f8563-117">You can also click **view sample message IDs** to see details for the messages that were sent from your on-premises email environment.</span></span> <span data-ttu-id="f8563-118">Étant donné que ces messages ont été rejetés par Office 365, vous ne pouvez pas utiliser le suivi des messages, mais vous pouvez utiliser l’exemple d’ID de message pour suivre les messages dans votre environnement de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="f8563-118">Because these messages were rejected by Office 365, you can't use message trace, but you can use the sample message ids to track the messages in your on-premises email environment.</span></span>

![Afficher des exemples d’ID de message dans la fenêtre Fix sender Domain Insight](../../media/sender-domain-view-sample-message-ids.png)

## <a name="related-topics"></a><span data-ttu-id="f8563-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8563-120">Related topics</span></span>

<span data-ttu-id="f8563-121">Pour plus d’informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f8563-121">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
