---
title: Valeurs de niveau de réclamation en bloc
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les valeurs de niveau de conformité en bloc utilisées dans Exchange Online Protection (EOP).
ms.openlocfilehash: d59bb152de075bb807e3cae72839fe459d7da40f
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48203526"
---
# <a name="bulk-complaint-level-bcl-in-eop"></a><span data-ttu-id="7808c-103">Niveau de réclamation en bloc (BCL) dans EOP</span><span class="sxs-lookup"><span data-stu-id="7808c-103">Bulk complaint level (BCL) in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="7808c-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online, EOP affecte un niveau de conformité en bloc (BCL) aux messages entrants provenant de publipostages en bloc.</span><span class="sxs-lookup"><span data-stu-id="7808c-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP assigns a bulk compliant level (BCL) to inbound messages from bulk mailers.</span></span> <span data-ttu-id="7808c-105">La bibliothèque de BCL est ajoutée au message dans un en-tête X et est similaire au [seuil de probabilité de courrier indésirable (SCL)](spam-confidence-levels.md) utilisé pour identifier les messages comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7808c-105">The BCL is added to the message in an X-header and is similar to the [spam confidence level (SCL)](spam-confidence-levels.md) that's used to identify messages as spam.</span></span> <span data-ttu-id="7808c-106">Une BCL plus élevée indique qu’un message en bloc est plus susceptible de générer des plaintes (et, par conséquent, plus vraisemblablement un courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="7808c-106">A higher BCL indicates a bulk message is more likely to generate complaints (and is therefore more likely to be spam).</span></span> <span data-ttu-id="7808c-107">Microsoft utilise des sources internes et tierces pour identifier le courrier en nombre et déterminer le BCL approprié.</span><span class="sxs-lookup"><span data-stu-id="7808c-107">Microsoft uses both internal and third party sources to identify bulk mail and determine the appropriate BCL.</span></span>

<span data-ttu-id="7808c-108">Les expéditeurs de courriers électroniques varient en fonction de leurs modèles d’envoi, de création de contenu et d’acquisition de destinataires.</span><span class="sxs-lookup"><span data-stu-id="7808c-108">Bulk mailers vary in their sending patterns, content creation, and recipient acquisition practices.</span></span> <span data-ttu-id="7808c-109">Les expéditeurs de courriers en bloc envoient des messages pertinents avec le contenu pertinent à leurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="7808c-109">Good bulk mailers send desired messages with relevant content to their subscribers.</span></span> <span data-ttu-id="7808c-110">Ces messages entraînent peu de réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="7808c-110">These messages generate few complaints from recipients.</span></span> <span data-ttu-id="7808c-111">D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="7808c-111">Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients.</span></span> <span data-ttu-id="7808c-112">Les messages provenant d’un expéditeur de courrier indésirable sont connus sous le nom de courrier en nombre ou de courrier gris.</span><span class="sxs-lookup"><span data-stu-id="7808c-112">Messages from a bulk mailer are known as bulk mail or gray mail.</span></span>

 <span data-ttu-id="7808c-113">Le filtrage du courrier indésirable marque les messages en tant que **courrier en masse** en fonction du seuil BCL (valeur par défaut ou valeur que vous spécifiez) et prend l’action spécifiée sur le message (l’action par défaut consiste à envoyer le message vers le dossier de courrier indésirable du destinataire).</span><span class="sxs-lookup"><span data-stu-id="7808c-113">Spam filtering marks messages as **Bulk email** based on the BCL threshold (the default value or a value you specify) and takes the specified action on the message (the default action is deliver the message to the recipient's Junk Email folder).</span></span> <span data-ttu-id="7808c-114">Pour plus d’informations, consultez la rubrique [configurer des stratégies anti-courrier](configure-your-spam-filter-policies.md) indésirable et [quelle est la différence entre courrier indésirable et courrier électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span><span class="sxs-lookup"><span data-stu-id="7808c-114">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md) and [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span></span>

<span data-ttu-id="7808c-115">Les seuils BCL sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7808c-115">The BCL thresholds are described in the following table.</span></span>

****

|<span data-ttu-id="7808c-116">BCL</span><span class="sxs-lookup"><span data-stu-id="7808c-116">BCL</span></span>|<span data-ttu-id="7808c-117">Description</span><span class="sxs-lookup"><span data-stu-id="7808c-117">Description</span></span>|
|:---:|---|
|<span data-ttu-id="7808c-118">0</span><span class="sxs-lookup"><span data-stu-id="7808c-118">0</span></span>|<span data-ttu-id="7808c-119">Le message ne provient pas d'un expéditeur en bloc.</span><span class="sxs-lookup"><span data-stu-id="7808c-119">The message isn't from a bulk sender.</span></span>|
|<span data-ttu-id="7808c-120">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="7808c-120">1, 2, 3</span></span>|<span data-ttu-id="7808c-121">Le message provient d'un expéditeur en bloc qui génère peu de réclamations.</span><span class="sxs-lookup"><span data-stu-id="7808c-121">The message is from a bulk sender that generates few complaints.</span></span>|
|<span data-ttu-id="7808c-122">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="7808c-122">4, 5, 6, 7</span></span>|<span data-ttu-id="7808c-123">Le message provient d'un expéditeur en bloc qui génère un nombre moyen de réclamations.</span><span class="sxs-lookup"><span data-stu-id="7808c-123">The message is from a bulk sender that generates a mixed number of complaints.</span></span>|
|<span data-ttu-id="7808c-124">8, 9</span><span class="sxs-lookup"><span data-stu-id="7808c-124">8, 9</span></span>|<span data-ttu-id="7808c-125">Le message provient d’un expéditeur en bloc qui génère un grand nombre de réclamations.</span><span class="sxs-lookup"><span data-stu-id="7808c-125">The message is from a bulk sender that generates a high number of complaints.</span></span>|
|
