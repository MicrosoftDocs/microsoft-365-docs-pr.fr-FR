---
title: Reconnaitre une notification de conservation
f1.keywords:
- NOCSH
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
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser Advanced eDiscovery pour envoyer et suivre des notifications de mise en attente légale par courrier électronique, et surveiller l’état des obligations.
ms.openlocfilehash: 393d8884a4d4d39056267666fdce6a2754cb582b
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034884"
---
# <a name="acknowledge-a-hold-notification"></a><span data-ttu-id="29f0c-103">Reconnaitre une notification de conservation</span><span class="sxs-lookup"><span data-stu-id="29f0c-103">Acknowledge a hold notification</span></span>

<span data-ttu-id="29f0c-104">Lorsque vous répondez à une demande ou à un examen réglementaire, vous pouvez être tenu d’informer les dépositaires de leur obligation de conserver les informations stockées électroniquement (ESI) et tout document pertinent pour une affaire juridique active ou imminente.</span><span class="sxs-lookup"><span data-stu-id="29f0c-104">When responding to a regulatory request or investigation, you may be required to inform custodians of their obligation to preserve electronically stored information (ESI) and any material that may be relevant to an active or imminent legal matter.</span></span> <span data-ttu-id="29f0c-105">Une fois envoyées, les équipes juridiques doivent savoir que chaque dépositaire a reçu, lu, compris et accepté de suivre les instructions données.</span><span class="sxs-lookup"><span data-stu-id="29f0c-105">Once sent, legal teams must know that each custodian has received, read, understood, and agreed to follow the given instructions.</span></span>

<span data-ttu-id="29f0c-106">Pour réduire le temps, les coûts et l’effort de suivi avec vos dépositaires, Advanced eDiscovery vous permet d’envoyer et de suivre des notifications de conservation légale par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="29f0c-106">To help reduce the time, cost, and effort of following up with your custodians,  Advanced eDiscovery allows you to send and follow up on legal hold notifications through email.</span></span> <span data-ttu-id="29f0c-107">En plus des notifications par courrier électronique, chaque dépositaire aura accès à un portail de conformité individualisé, ce qui permet aux dépositaires d’être tenus informés des modifications apportées à leur statut d’obligation.</span><span class="sxs-lookup"><span data-stu-id="29f0c-107">In addition to email notices, each custodian will have access to an individualized Compliance Portal, allowing custodians to be kept informed of changes to their obligation status.</span></span>

## <a name="email-notifications"></a><span data-ttu-id="29f0c-108">Notifications par e-mail</span><span class="sxs-lookup"><span data-stu-id="29f0c-108">Email notifications</span></span>

<span data-ttu-id="29f0c-109">Une fois qu’une notification de conservation légale a été émise, chaque dépositaire reçoit un e-mail unique et personnalisé contenant votre notification de conservation légale définie et des instructions ajoutées.</span><span class="sxs-lookup"><span data-stu-id="29f0c-109">After a Legal Hold Notification has been issued, each custodian will receive a unique and personalized email containing your defined legal hold notice and added instructions.</span></span> 

> [!TIP]
> <span data-ttu-id="29f0c-110">Découvrez comment utiliser l’éditeur de  [communication](using-communications-editor.md) intégré pour permettre à vos dépositaires de reconnaître leur avis ou d’accéder à leur portail de conformité directement à partir de leur courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="29f0c-110">See how you can use the built-in  [Communication Editor](using-communications-editor.md) to allow your custodians to acknowledge their notice or access their Compliance Portal directly from their email.</span></span>

<span data-ttu-id="29f0c-111">En fonction de la configuration de votre notification de conservation légale, vos dépositaires peuvent recevoir les notifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="29f0c-111">Based on the configuration of your legal hold notification, your custodians may receive the following notices:</span></span> 

- <span data-ttu-id="29f0c-112">**Avis d’émission :** Première notification envoyée à votre dépositaire.</span><span class="sxs-lookup"><span data-stu-id="29f0c-112">**Issuance notice:** The first notice sent to your custodian.</span></span> <span data-ttu-id="29f0c-113">Cet avis contient vos instructions d’émission et l’avis de attente qui est envoyé à la fin de votre message.</span><span class="sxs-lookup"><span data-stu-id="29f0c-113">This notice will contain your issuance instructions and the hold notice appended to the end of your message.</span></span>

- <span data-ttu-id="29f0c-114">**Avis de rappel :** S’il est activé, un avis de rappel est envoyé à vos dépositaires en fonction de la fréquence et de l’intervalle spécifiés.</span><span class="sxs-lookup"><span data-stu-id="29f0c-114">**Reminder notice:** If enabled, a reminder notice will be sent to your custodians based on the specified frequency and interval.</span></span> <span data-ttu-id="29f0c-115">Les rappels continueront d’être envoyés jusqu’à ce que le dépositaire ait reconnu sa notification ou jusqu’à ce que le nombre de rappels soit épuisé.</span><span class="sxs-lookup"><span data-stu-id="29f0c-115">The reminders will continue to be sent either until the custodian has acknowledged their notice or until the number of reminders have been exhausted.</span></span>

- <span data-ttu-id="29f0c-116">**Notification d’escalade :** Si ce dernier est activé, une notification d’escalade est envoyée à votre dépositaire et à son responsable une fois les notifications de rappel épuisées.</span><span class="sxs-lookup"><span data-stu-id="29f0c-116">**Escalation notice:** If enabled, an escalation notice will be sent to your custodian and their manager after the reminder notices have been exhausted.</span></span> <span data-ttu-id="29f0c-117">Le système envoie automatiquement des notifications d’escalade jusqu’à ce que le nombre spécifié d’escalades soit terminé ou jusqu’à ce que le dépositaire reconnaisse sa notification de conservation.</span><span class="sxs-lookup"><span data-stu-id="29f0c-117">The system will automatically send escalation notices until the specified number of escalations have been completed or until the custodian acknowledges their hold notification.</span></span>

- <span data-ttu-id="29f0c-118">**Notification de réédition :** Au cours d’une enquête, si le contenu de l’avis de mise en attente est mis à jour, l’avis mis à jour est automatiquement envoyé au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="29f0c-118">**Reissue notice:** During the course of an investigation, if the contents of the hold notice are updated, then the updated notice will automatically be sent to the custodian.</span></span>

- <span data-ttu-id="29f0c-119">**Avis de publication :** Lorsqu’un dépositaire est libéré du cas, l’avis de publication lui est envoyé.</span><span class="sxs-lookup"><span data-stu-id="29f0c-119">**Release notice:** When a custodian is released from the case, they'll be sent the release notice.</span></span> 

## <a name="compliance-portal"></a><span data-ttu-id="29f0c-120">Portail de conformité</span><span class="sxs-lookup"><span data-stu-id="29f0c-120">Compliance Portal</span></span>

<span data-ttu-id="29f0c-121">En plus des notifications par courrier électronique, chaque dépositaire aura accès à un portail de conformité unique.</span><span class="sxs-lookup"><span data-stu-id="29f0c-121">In addition to the email notifications, each custodian will have access to a unique Compliance Portal.</span></span> <span data-ttu-id="29f0c-122">Par le biais du portail, chaque dépositaire peut afficher, consulter et reconnaître ses notifications de conservation active.</span><span class="sxs-lookup"><span data-stu-id="29f0c-122">Through the portal, each custodian can view, access, and acknowledge their active hold notifications.</span></span>

![Portail de conformité pour un dépositaire](../media/CustodianPortal.jpg)
