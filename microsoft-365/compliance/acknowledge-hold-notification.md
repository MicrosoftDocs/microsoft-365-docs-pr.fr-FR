---
title: Accuser réception des notifications de blocage
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1a627a0927d6ffa2244e9f3580867379ff1fbdc5
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078983"
---
# <a name="acknowledge-a-hold-notification"></a><span data-ttu-id="00193-102">Reconnaitre une notification de conservation</span><span class="sxs-lookup"><span data-stu-id="00193-102">Acknowledge a hold notification</span></span> 
<span data-ttu-id="00193-103">Lors de la réponse à une demande réglementaire ou à une enquête, il se peut que vous deviez informer les dépositaires de leur obligation de conserver les informations stockées électroniquement (ESI), ainsi que tout matériel pouvant être pertinent pour une question juridique active ou imminente.</span><span class="sxs-lookup"><span data-stu-id="00193-103">When responding to a regulatory request or investigation, you may be required to  inform custodians of their obligation to preserve electronically stored information (ESI) as well as any material that may be relevant to an active or imminent legal matter.</span></span> <span data-ttu-id="00193-104">Une fois envoyés, les équipes juridiques doivent savoir que chaque dépositaire a reçu, lu et compris, et qu’il est convenu de respecter les instructions données.</span><span class="sxs-lookup"><span data-stu-id="00193-104">Once sent, legal teams must know that each custodian has received, read, and understood, and agreed to comply with the given instructions.</span></span>

<span data-ttu-id="00193-105">Pour vous aider à réduire le temps, les coûts et les efforts de suivi des dépositaires, Advanced eDiscovery vous permet d’envoyer et de suivre les notifications de conservation légale par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="00193-105">To help reduce the time, cost, and effort of following up with your custodians,  Advanced eDiscovery allows you to send and follow-up on legal hold notifications through email.</span></span> <span data-ttu-id="00193-106">Outre les notifications par courrier électronique, chaque dépositaire aura également accès à un portail de conformité individualisé, ce qui permettra aux dépositaires d’être informés des modifications apportées à leur statut d’obligation.</span><span class="sxs-lookup"><span data-stu-id="00193-106">In addition to email notices, each custodian will also have access to an individualized Compliance Portal, allowing custodians to be kept informed of changes to their obligation status.</span></span>

## <a name="email-notifications"></a><span data-ttu-id="00193-107">Notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="00193-107">Email notifications</span></span>
<span data-ttu-id="00193-108">Une fois qu’une notification de conservation légale a été émise, chaque dépositaire reçoit un message électronique unique et personnalisé contenant votre notification de mise en attente légale définie et vous avez ajouté des instructions.</span><span class="sxs-lookup"><span data-stu-id="00193-108">Once a Legal Hold Notification has been issued, each custodian will receive a unique and personalized email containing your defined legal hold notice and added instructions.</span></span> 

> [!Tip] 
> <span data-ttu-id="00193-109">Découvrez comment vous pouvez utiliser l' [éditeur de communication](using-communications-editor.md) intégré pour permettre à vos dépositaires de reconnaître leur notification ou d’accéder à leur portail de conformité directement à partir de leur courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="00193-109">See how you can use the built-in  [Communication Editor](using-communications-editor.md) to allow your custodians to acknowledge their notice or access their Compliance Portal directly from their email.</span></span>

<span data-ttu-id="00193-110">En fonction de la configuration de votre notification de conservation légale, vos dépositaires peuvent recevoir les notifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="00193-110">Based on the configuration of your legal hold notification, your custodians may receive the following notices:</span></span> 

- <span data-ttu-id="00193-111">**Notice d’émission** -il s’agit de la première notification envoyée à votre dépositaire.</span><span class="sxs-lookup"><span data-stu-id="00193-111">**Issuance notice** - This is the first notice sent to your custodian.</span></span> <span data-ttu-id="00193-112">Cela contiendra vos instructions d’émission, ainsi que la notification de suspension ajoutée à la fin de votre message.</span><span class="sxs-lookup"><span data-stu-id="00193-112">This will contain your issuance instructions as well as the hold notice appended to the end of your message.</span></span>

- <span data-ttu-id="00193-113">**Notice de rappel** : si cette option est activée, un avis de rappel est envoyé à vos dépositaires en fonction de la fréquence et de l’intervalle spécifiés.</span><span class="sxs-lookup"><span data-stu-id="00193-113">**Reminder notice** - If enabled, a reminder notice will be sent to your custodians based on the specified frequency and interval.</span></span> <span data-ttu-id="00193-114">Les rappels continueront d’être envoyés jusqu’à ce que le dépositaire ait accusé réception de leur avis ou jusqu’à ce que le nombre de rappels soit épuisé.</span><span class="sxs-lookup"><span data-stu-id="00193-114">The reminders will continue to be sent either until the custodian has acknowledged their notice or until the number of reminders have been exhausted.</span></span>

- <span data-ttu-id="00193-115">**Notification d’escalade** : si cette option est activée, une notification d’escalade est envoyée à votre dépositaire et à son responsable une fois que les notifications de rappel ont été épuisées.</span><span class="sxs-lookup"><span data-stu-id="00193-115">**Escalation notice** - If enabled, an escalation notice will be sent to your custodian and their manager after the reminder notices have been exhausted.</span></span> <span data-ttu-id="00193-116">Le système enverra automatiquement des notifications d’escalade jusqu’à ce que les escalades affectées soient terminées ou jusqu’à ce que le dépositaire confirme sa notification de suspension.</span><span class="sxs-lookup"><span data-stu-id="00193-116">The system will automatically send escalation notices until the alloted escalations have been completed or until the custodian acknowledges their hold notification.</span></span>

- <span data-ttu-id="00193-117">**Relancer l’avis** : pendant une enquête, si le contenu de la notification de mise en attente est mis à jour, l’avis mis à jour est automatiquement envoyé au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="00193-117">**Re-issue notice** - During the course of an investigation, if the contents of the hold notice are updated, then the updated notice will automatically be sent to the custodian.</span></span>

- <span data-ttu-id="00193-118">**Avertissement de publication** : lorsqu’un dépositaire est publié à partir de l’incident, il reçoit l’avis de publication.</span><span class="sxs-lookup"><span data-stu-id="00193-118">**Release notice** - When a custodian is released from the case, they will be sent the release notice.</span></span> 

## <a name="compliance-portal"></a><span data-ttu-id="00193-119">Portail de conformité</span><span class="sxs-lookup"><span data-stu-id="00193-119">Compliance Portal</span></span>
<span data-ttu-id="00193-120">En plus des notifications par courrier électronique, chaque dépositaire aura également accès à un portail de conformité unique.</span><span class="sxs-lookup"><span data-stu-id="00193-120">In addition to the email notifications, each custodian will also have access to a unique Compliance Portal.</span></span> <span data-ttu-id="00193-121">Par le biais du portail, chaque dépositaire pourra consulter les notifications de blocage actives, y accéder et les reconnaître.</span><span class="sxs-lookup"><span data-stu-id="00193-121">Through the portal, each custodian will be able to view, access, and acknowledge their active hold notifications.</span></span>

![Portail de conformité pour un dépositaire](media/CustodianPortal.jpg)
