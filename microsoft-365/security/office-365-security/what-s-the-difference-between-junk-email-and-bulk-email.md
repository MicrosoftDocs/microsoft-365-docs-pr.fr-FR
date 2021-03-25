---
title: Quelle &apos; est la différence entre le courrier indésirable et le courrier en masse ?
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent découvrir les différences entre le courrier indésirable (courrier indésirable) et le courrier en masse (courrier gris) dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: fc9c94946c3da2f9a14f45070a86c557a5c7dc85
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204938"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email-in-eop"></a><span data-ttu-id="81e5c-103">Quelle est la différence entre le courrier indésirable et le courrier en masse dans EOP ?</span><span class="sxs-lookup"><span data-stu-id="81e5c-103">What's the difference between junk email and bulk email in EOP?</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="81e5c-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="81e5c-104">**Applies to**</span></span>
- [<span data-ttu-id="81e5c-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="81e5c-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="81e5c-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="81e5c-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="81e5c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="81e5c-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="81e5c-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, les clients se demandent parfois : « Quelle est la différence entre le courrier indésirable et le courrier en masse ? »</span><span class="sxs-lookup"><span data-stu-id="81e5c-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, customers sometimes ask: "what's the difference between junk email and bulk email?"</span></span> <span data-ttu-id="81e5c-109">Cette rubrique explique la différence et décrit les contrôles disponibles dans EOP.</span><span class="sxs-lookup"><span data-stu-id="81e5c-109">This topic explains the difference and describes the controls that are available in EOP.</span></span>

- <span data-ttu-id="81e5c-110">**Le courrier indésirable** est du courrier indésirable, qui est un message non sollicité et universellement indésirable (s’il est correctement identifié).</span><span class="sxs-lookup"><span data-stu-id="81e5c-110">**Junk email** is spam, which are unsolicited and universally unwanted messages (when identified correctly).</span></span> <span data-ttu-id="81e5c-111">Par défaut, EOP rejette le courrier indésirable en fonction de la réputation du serveur de messagerie source.</span><span class="sxs-lookup"><span data-stu-id="81e5c-111">By default, the EOP rejects spam based on the reputation of the source email server.</span></span> <span data-ttu-id="81e5c-112">Si un message réussit l’inspection de l’adresse IP source, il est envoyé au filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81e5c-112">If a message passes source IP inspection, it's sent to spam filtering.</span></span> <span data-ttu-id="81e5c-113">Si le message est classé comme courrier indésirable par filtrage du courrier indésirable, le message est remis (par défaut) aux destinataires prévus et déplacé vers son dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81e5c-113">If the message is classified as spam by spam filtering, the message is (by default) delivered to the intended recipients and moved to their Junk Email folder.</span></span>

  - <span data-ttu-id="81e5c-114">Vous pouvez configurer les actions à prendre sur les verdicts de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81e5c-114">You can configure the actions to take on spam filtering verdicts.</span></span> <span data-ttu-id="81e5c-115">Pour obtenir des instructions, voir [Configurer des stratégies anti-courrier indésirable dans EOP.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="81e5c-115">For instructions, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

  - <span data-ttu-id="81e5c-116">Si vous n’êtes pas d’accord avec le verdict de filtrage du courrier indésirable, vous pouvez signaler les messages que vous considérez comme courrier indésirable ou non indésirable à Microsoft de plusieurs manières, comme décrit dans Signaler les messages et les fichiers à [Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="81e5c-116">If you disagree with the spam filtering verdict, you can report messages that you consider to be spam or non-spam to Microsoft in several ways, as described in [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

- <span data-ttu-id="81e5c-117">**Les messages électroniques** en nombre (également appelés _messages_ gris) sont plus difficiles à classer.</span><span class="sxs-lookup"><span data-stu-id="81e5c-117">**Bulk email** (also known as _gray mail_), is more difficult to classify.</span></span> <span data-ttu-id="81e5c-118">Alors que le courrier indésirable est une menace constante, les courriers électroniques en masse sont souvent des publicités ou des messages marketing.</span><span class="sxs-lookup"><span data-stu-id="81e5c-118">Whereas spam is a constant threat, bulk email is often one-time advertisements or marketing messages.</span></span> <span data-ttu-id="81e5c-119">Certains utilisateurs souhaitent des messages électroniques en nombre (et en fait, ils se sont délibérément inscrits pour les recevoir), tandis que d’autres considèrent les messages électroniques en masse comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81e5c-119">Some users want bulk email messages (and in fact, they have deliberately signed up to receive them), while other users consider bulk email to be spam.</span></span> <span data-ttu-id="81e5c-120">Par exemple, certains utilisateurs souhaitent recevoir des messages publicitaires de Contoso Corporation ou des invitations à une conférence à venir sur la cybersécurité, tandis que d’autres considèrent ces mêmes messages comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81e5c-120">For example, some users want to receive advertising messages from the Contoso Corporation or invitations to an upcoming conference on cyber security, while other users consider these same messages to be spam.</span></span>

  <span data-ttu-id="81e5c-121">Pour plus d’informations sur la façon dont les messages électroniques en nombre sont identifiés, voir Le niveau de réclamation en bloc [(BCL) dans EOP.](bulk-complaint-level-values.md)</span><span class="sxs-lookup"><span data-stu-id="81e5c-121">For more information about how bulk email is identified, see [Bulk complaint level (BCL) in EOP](bulk-complaint-level-values.md).</span></span>

## <a name="how-to-manage-bulk-email"></a><span data-ttu-id="81e5c-122">Gestion des messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="81e5c-122">How to manage bulk email</span></span>

<span data-ttu-id="81e5c-123">En raison de la réaction mixte aux messages électroniques en masse, il n’existe pas d’instructions universelles qui s’appliquent à chaque organisation.</span><span class="sxs-lookup"><span data-stu-id="81e5c-123">Because of the mixed reaction to bulk email, there isn't universal guidance that applies to every organization.</span></span>

<span data-ttu-id="81e5c-124">Les polices anti-courrier indésirable ont un seuil BCL par défaut qui est utilisé pour identifier les messages électroniques en masse comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81e5c-124">Anti-spam polices have a default BCL threshold that's used to identify bulk email as spam.</span></span> <span data-ttu-id="81e5c-125">Les administrateurs peuvent augmenter ou diminuer le seuil.</span><span class="sxs-lookup"><span data-stu-id="81e5c-125">Admins can increase or decrease the threshold.</span></span> <span data-ttu-id="81e5c-126">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="81e5c-126">For more information, see the following topics:</span></span>

- <span data-ttu-id="81e5c-127">[Configurer des stratégies anti-courrier indésirable dans EOP.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="81e5c-127">[Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

- [<span data-ttu-id="81e5c-128">Paramètres de stratégie anti-courrier indésirable EOP</span><span class="sxs-lookup"><span data-stu-id="81e5c-128">EOP anti-spam policy settings</span></span>](recommended-settings-for-eop-and-office365.md#eop-anti-spam-policy-settings)

<span data-ttu-id="81e5c-129">Une autre option facile à ignorer : si un utilisateur se plaindra de recevoir des messages électroniques en masse, mais que les messages sont des expéditeurs dignes de confiance qui passent le filtrage du courrier indésirable dans EOP, l’utilisateur doit vérifier qu’une option de désabonnement est disponible dans le message électronique en masse.</span><span class="sxs-lookup"><span data-stu-id="81e5c-129">Another option that's easy to overlook: if a user complains about receiving bulk email, but the messages are from reputable senders that pass spam filtering in EOP, have the user check for a unsubscribe option in the bulk email message.</span></span>
