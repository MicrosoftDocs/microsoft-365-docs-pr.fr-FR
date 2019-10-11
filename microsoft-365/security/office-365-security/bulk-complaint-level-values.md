---
title: Valeurs de niveau de réclamation en bloc, expéditeurs de courrier indésirable, niveaux BCL, fonctionnement de BCL, indices BCL, courrier indésirable, en-tête de courrier indésirable, filtrage du courrier en nombre
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
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
description: Découvrez les valeurs de niveau de courrier en bloc (BCL) dans Office 365.
ms.openlocfilehash: 6f9314a5b96dbd641e461dfb564ed8605372a949
ms.sourcegitcommit: b0396171d24c6298b809b43bb109d3afed4de5b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "37451096"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="1f215-103">Valeurs BCL</span><span class="sxs-lookup"><span data-stu-id="1f215-103">Bulk Complaint Level values</span></span>

<span data-ttu-id="1f215-104">Les vers de publipostage en bloc ont des modèles d'envoi différents, ainsi que des pratiques de création de contenu et d'acquisition de liste variées.</span><span class="sxs-lookup"><span data-stu-id="1f215-104">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices.</span></span> <span data-ttu-id="1f215-105">Certains sont de bons vers de publipostage en bloc et envoient des messages désirés comportant un contenu pertinent à leurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="1f215-105">Some are good bulk mailers that send wanted messages with relevant content to their subscribers.</span></span> <span data-ttu-id="1f215-106">Ces messages entraînent peu de réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="1f215-106">These messages generate few complaints from recipients.</span></span> <span data-ttu-id="1f215-107">D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="1f215-107">Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients.</span></span>

<span data-ttu-id="1f215-108">Pour distinguer ces types de vers de publipostage en bloc, une évaluation BCL (Bulk Complaint Level) est réalisée sur les messages qui en proviennent.</span><span class="sxs-lookup"><span data-stu-id="1f215-108">To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating.</span></span> <span data-ttu-id="1f215-109">Les évaluations BCL vont de 1 à 9 selon la probabilité de réclamations dues au ver de publipostage en bloc.</span><span class="sxs-lookup"><span data-stu-id="1f215-109">BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints.</span></span> <span data-ttu-id="1f215-110">Un expéditeur disposant d'une évaluation BCL de 9 peut entraîner un grand nombre de réclamations de la part des destinataires, tandis qu'un autre expéditeur ayant une évaluation BCL de 3 n'en générera probablement pas beaucoup.</span><span class="sxs-lookup"><span data-stu-id="1f215-110">A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints.</span></span> <span data-ttu-id="1f215-111">Microsoft utilise des sources internes et tierces pour identifier le courrier en masse et déterminer l'évaluation BCL appropriée.</span><span class="sxs-lookup"><span data-stu-id="1f215-111">Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL.</span></span> <span data-ttu-id="1f215-112">Pour plus d'informations sur cet en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="1f215-112">For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>

<span data-ttu-id="1f215-113">Dans la mesure où un expéditeur de courrier en nombre avec une note de 9 est susceptible de générer des plaintes, le BCL par défaut est 7.</span><span class="sxs-lookup"><span data-stu-id="1f215-113">Since a bulk mailer with a rating of 9 is likely to generate complaints, the default BCL is 7.</span></span> <span data-ttu-id="1f215-114">Cela signifie que les courriers en masse seront acceptés jusqu’à ce que le niveau de réclamation de 7 et que le courrier ne soit accepté par la suite.</span><span class="sxs-lookup"><span data-stu-id="1f215-114">This means that bulk mails will be accepted until the complaint level of 7 and mail won't be accepted thereafter.</span></span> <span data-ttu-id="1f215-115">Plus le taux est faible, moins le courrier en masse est accepté.</span><span class="sxs-lookup"><span data-stu-id="1f215-115">The lower the rating, the less bulk mail is accepted.</span></span> <span data-ttu-id="1f215-116">Si vos utilisateurs sont, et que leur travail est, confidentiel à envoyer du courrier en nombre et que votre BCL est défini sur 4, aucun courrier en masse avec une BCL plus élevée ne sera accepté.</span><span class="sxs-lookup"><span data-stu-id="1f215-116">If your users are, and their work is, sensitive to bulk mail, and your BCL is set to 4, then no bulk mail with a higher BCL than 4 will be accepted.</span></span>

<span data-ttu-id="1f215-117">Vous pouvez vous servir des valeurs BCL pour définir le niveau de filtrage en bloc souhaité pour votre organisation en suivant les étapes décrites dans la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1f215-117">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="1f215-118">Le tableau suivant décrit les valeurs BCL actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="1f215-118">The following table describes the BCL values that are currently in use.</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f215-119">**Valeur BCL**</span><span class="sxs-lookup"><span data-stu-id="1f215-119">**BCL Value**</span></span>|<span data-ttu-id="1f215-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="1f215-120">**Description**</span></span>|
|<span data-ttu-id="1f215-121">0</span><span class="sxs-lookup"><span data-stu-id="1f215-121">0</span></span>|<span data-ttu-id="1f215-122">Le message ne provient pas d'un expéditeur en bloc.</span><span class="sxs-lookup"><span data-stu-id="1f215-122">The message isn't from a bulk sender.</span></span>|
|<span data-ttu-id="1f215-123">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="1f215-123">1, 2, 3</span></span>|<span data-ttu-id="1f215-124">Le message provient d'un expéditeur en bloc qui génère peu de réclamations.</span><span class="sxs-lookup"><span data-stu-id="1f215-124">The message is from a bulk sender that generates few complaints.</span></span>|
|<span data-ttu-id="1f215-125">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="1f215-125">4, 5, 6, 7</span></span>|<span data-ttu-id="1f215-126">Le message provient d'un expéditeur en bloc qui génère un nombre moyen de réclamations.</span><span class="sxs-lookup"><span data-stu-id="1f215-126">The message is from a bulk sender that generates a mixed number of complaints.</span></span>|
|<span data-ttu-id="1f215-127">8, 9</span><span class="sxs-lookup"><span data-stu-id="1f215-127">8, 9</span></span>|<span data-ttu-id="1f215-128">Le message provient d'un expéditeur en bloc qui génère un grand nombre de réclamations</span><span class="sxs-lookup"><span data-stu-id="1f215-128">The message is from a bulk sender that generates a high number of complaints</span></span>|
