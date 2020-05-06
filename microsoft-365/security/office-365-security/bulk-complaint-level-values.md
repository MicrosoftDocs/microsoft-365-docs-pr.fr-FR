---
title: Valeurs BCL
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/23/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: En savoir plus sur les valeurs de niveau de conformité en bloc dans Office 365.
ms.openlocfilehash: 82c006f05ce3d37ff23ca1e522b653bd26efeed8
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44035567"
---
# <a name="bulk-complaint-level-bcl-in-office-365"></a><span data-ttu-id="f928d-103">Niveau de réclamation en bloc (BCL) dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f928d-103">Bulk complaint level (BCL) in Office 365</span></span>

<span data-ttu-id="f928d-104">Les expéditeurs de courriers électroniques varient en fonction de leurs modèles d’envoi, de création de contenu et d’acquisition de destinataires.</span><span class="sxs-lookup"><span data-stu-id="f928d-104">Bulk mailers vary in their sending patterns, content creation, and recipient acquisition practices.</span></span> <span data-ttu-id="f928d-105">Certains sont des expéditeurs de publipostage en bloc qui envoient des messages désirés avec du contenu pertinent à leurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="f928d-105">Some are good bulk mailers that send desired messages with relevant content to their subscribers.</span></span> <span data-ttu-id="f928d-106">Ces messages entraînent peu de réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="f928d-106">These messages generate few complaints from recipients.</span></span> <span data-ttu-id="f928d-107">D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="f928d-107">Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients.</span></span> <span data-ttu-id="f928d-108">Les messages provenant d’un expéditeur de courrier indésirable sont connus sous le nom de courrier en nombre ou de courrier gris.</span><span class="sxs-lookup"><span data-stu-id="f928d-108">Messages from a bulk mailer is known as bulk mail or gray mail.</span></span>

<span data-ttu-id="f928d-109">Pour distinguer les messages provenant de différents types de publipostages en bloc, le courrier électronique entrant en vrac (Exchange Online ou autonome Exchange Online Protection (EOP) sans boîte aux lettres Exchange Online) reçoit un niveau de réclamation en bloc (BCL) qui est ajouté au message dans un en-tête X.</span><span class="sxs-lookup"><span data-stu-id="f928d-109">To distinguish messages from different types of bulk mailers, inbound email from bulk mailers (Exchange Online or standalone Exchange Online Protection (EOP) without Exchange Online mailboxes) is assigned a bulk complaint level (BCL) that's added to the message in an X-header.</span></span> <span data-ttu-id="f928d-110">Le BCL est similaire au [seuil de probabilité de courrier indésirable (SCL)](spam-confidence-levels.md) utilisé pour identifier les messages comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f928d-110">The BCL is similar to the [spam confidence level (SCL)](spam-confidence-levels.md) that's used to identify messages as spam.</span></span> <span data-ttu-id="f928d-111">Une BCL plus élevée indique qu’un message en bloc est plus susceptible de générer des plaintes (et, par conséquent, plus vraisemblablement un courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="f928d-111">A higher BCL indicates a bulk message is more likely to generate complaints (and is therefore more likely to be spam).</span></span> <span data-ttu-id="f928d-112">Microsoft utilise des sources internes et tierces pour identifier le courrier en nombre et déterminer le BCL approprié.</span><span class="sxs-lookup"><span data-stu-id="f928d-112">Microsoft uses both internal and third party sources to identify bulk mail and determine the appropriate BCL.</span></span>

 <span data-ttu-id="f928d-113">Le filtrage du courrier indésirable marque les messages en tant que **courrier en masse** en fonction du seuil BCL (valeur par défaut ou valeur que vous spécifiez) et prend l’action spécifiée sur le message (l’action par défaut consiste à envoyer le message vers le dossier de courrier indésirable du destinataire).</span><span class="sxs-lookup"><span data-stu-id="f928d-113">Spam filtering marks messages as **Bulk email** based on the BCL threshold (the default value or a value you specify) and takes the specified action on the message (the default action is deliver the message to the recipient's Junk Email folder).</span></span> <span data-ttu-id="f928d-114">Pour plus d’informations, consultez la rubrique [configurer des stratégies anti-courrier](configure-your-spam-filter-policies.md) indésirable et [quelle est la différence entre courrier indésirable et courrier électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span><span class="sxs-lookup"><span data-stu-id="f928d-114">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md) and [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span></span>

<span data-ttu-id="f928d-115">Les seuils BCL sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f928d-115">The BCL thresholds are described in the following table.</span></span>

|||
|:---:|---|
|<span data-ttu-id="f928d-116">**BCL**</span><span class="sxs-lookup"><span data-stu-id="f928d-116">**BCL**</span></span>|<span data-ttu-id="f928d-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="f928d-117">**Description**</span></span>|
|<span data-ttu-id="f928d-118">0</span><span class="sxs-lookup"><span data-stu-id="f928d-118">0</span></span>|<span data-ttu-id="f928d-119">Le message ne provient pas d'un expéditeur en bloc.</span><span class="sxs-lookup"><span data-stu-id="f928d-119">The message isn't from a bulk sender.</span></span>|
|<span data-ttu-id="f928d-120">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="f928d-120">1, 2, 3</span></span>|<span data-ttu-id="f928d-121">Le message provient d'un expéditeur en bloc qui génère peu de réclamations.</span><span class="sxs-lookup"><span data-stu-id="f928d-121">The message is from a bulk sender that generates few complaints.</span></span>|
|<span data-ttu-id="f928d-122">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="f928d-122">4, 5, 6, 7</span></span>|<span data-ttu-id="f928d-123">Le message provient d'un expéditeur en bloc qui génère un nombre moyen de réclamations.</span><span class="sxs-lookup"><span data-stu-id="f928d-123">The message is from a bulk sender that generates a mixed number of complaints.</span></span>|
|<span data-ttu-id="f928d-124">8, 9</span><span class="sxs-lookup"><span data-stu-id="f928d-124">8, 9</span></span>|<span data-ttu-id="f928d-125">Le message provient d’un expéditeur en bloc qui génère un grand nombre de réclamations.</span><span class="sxs-lookup"><span data-stu-id="f928d-125">The message is from a bulk sender that generates a high number of complaints.</span></span>|
|
