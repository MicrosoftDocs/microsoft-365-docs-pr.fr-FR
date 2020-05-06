---
title: Quelle est la différence entre courrier indésirable et message électronique en masse ?
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Découvrez la différence entre le courrier indésirable & courrier en bloc. Découvrez également les différentes options disponibles dans Exchange Online & Exchange Online Protection (EOP).
ms.openlocfilehash: 5d9d3b513de64d2a150d9e0a1c94bc5ca746b617
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44036595"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a><span data-ttu-id="9a92f-104">Quelle est la différence entre le courrier indésirable et le courrier en nombre ?</span><span class="sxs-lookup"><span data-stu-id="9a92f-104">What's the difference between junk email and bulk email?</span></span>

<span data-ttu-id="9a92f-105">Les clients Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des clients Exchange Online Protection (EOP) autonomes sans boîte aux lettres Exchange Online demandent parfois : « quelle est la différence entre le courrier indésirable et le courrier électronique en masse ? »</span><span class="sxs-lookup"><span data-stu-id="9a92f-105">Microsoft 365 customers with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) customers without Exchange Online mailboxes sometimes ask: "what's the difference between junk email and bulk email?"</span></span> <span data-ttu-id="9a92f-106">Cette rubrique explique la différence et décrit les contrôles disponibles dans EOP.</span><span class="sxs-lookup"><span data-stu-id="9a92f-106">This topic explains the difference and describes the controls that are available in EOP.</span></span>

- <span data-ttu-id="9a92f-107">Le courrier **indésirable** est du courrier indésirable, qui sont des messages non sollicités et universellement indésirables (lorsqu’ils sont identifiés correctement).</span><span class="sxs-lookup"><span data-stu-id="9a92f-107">**Junk email** is spam, which are unsolicited and universally unwanted messages (when identified correctly).</span></span> <span data-ttu-id="9a92f-108">Par défaut, EOP rejette le courrier indésirable en fonction de la réputation du serveur de messagerie source.</span><span class="sxs-lookup"><span data-stu-id="9a92f-108">By default, the EOP rejects spam based on the reputation of the source email server.</span></span> <span data-ttu-id="9a92f-109">Si un message passe l’inspection IP source, il est envoyé au filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9a92f-109">If a message passes source IP inspection, it's sent to spam filtering.</span></span> <span data-ttu-id="9a92f-110">Si le message est classé comme courrier indésirable par filtrage du courrier indésirable, le message est remis (par défaut) aux destinataires concernés et déplacé vers le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9a92f-110">If the message is classified as spam by spam filtering, the message is (by default) delivered to the intended recipients and moved to their Junk Email folder.</span></span>

  - <span data-ttu-id="9a92f-111">Vous pouvez configurer les actions à effectuer sur le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9a92f-111">You can configure the actions to take on spam filtering verdicts.</span></span> <span data-ttu-id="9a92f-112">Pour obtenir des instructions, consultez la rubrique [configurer des stratégies de blocage du courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9a92f-112">For instructions, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

  - <span data-ttu-id="9a92f-113">Si vous n’êtes pas d’accord avec le filtrage du courrier indésirable, vous pouvez signaler à Microsoft les messages que vous considérez comme courrier indésirable ou non indésirables, comme décrit dans la section [rapports de messages et de fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="9a92f-113">If you disagree with the spam filtering verdict, you can report messages that you consider to be spam or non-spam to Microsoft in several ways, as described in [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

- <span data-ttu-id="9a92f-114">Le **courrier en masse** (également appelé _courrier gris_) est plus difficile à classer.</span><span class="sxs-lookup"><span data-stu-id="9a92f-114">**Bulk email** (also known as _gray mail_), is more difficult to classify.</span></span> <span data-ttu-id="9a92f-115">Tandis que le courrier indésirable est une menace constante, les messages électroniques en masse sont souvent des publicités à usage unique ou des messages marketing.</span><span class="sxs-lookup"><span data-stu-id="9a92f-115">Whereas spam is a constant threat, bulk email is often one-time advertisements or marketing messages.</span></span> <span data-ttu-id="9a92f-116">Certains utilisateurs veulent des messages électroniques en nombre (et en fait, ils se sont délibérément inscrits pour les recevoir), tandis que d’autres utilisateurs considèrent le courrier en masse comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9a92f-116">Some users want bulk email messages (and in fact, they have deliberately signed up to receive them), while other users consider bulk email to be spam.</span></span> <span data-ttu-id="9a92f-117">Par exemple, certains utilisateurs souhaitent recevoir des messages publicitaires de la société Contoso Corporation ou des invitations à une conférence à venir sur la cyber sécurité, tandis que d’autres utilisateurs considèrent ces mêmes messages comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9a92f-117">For example, some users want to receive advertising messages from the Contoso Corporation or invitations to an upcoming conference on cyber security, while other users consider these same messages to be spam.</span></span>

  <span data-ttu-id="9a92f-118">Pour plus d’informations sur la façon dont le courrier en masse est identifié, voir [Bulk Complaint Level (BCL) in Office 365](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="9a92f-118">For more information about how bulk email is identified, see [Bulk complaint level (BCL) in Office 365](bulk-complaint-level-values.md).</span></span>

## <a name="how-to-manage-bulk-email"></a><span data-ttu-id="9a92f-119">Gestion des messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="9a92f-119">How to manage bulk email</span></span>

<span data-ttu-id="9a92f-120">En raison de la réaction mixte au courrier en masse, il n’existe pas de conseils universels qui s’appliquent à chaque organisation.</span><span class="sxs-lookup"><span data-stu-id="9a92f-120">Because of the mixed reaction to bulk email, there isn't universal guidance that applies to every organization.</span></span>

<span data-ttu-id="9a92f-121">Les stratégies de blocage du courrier indésirable ont un seuil BCL par défaut qui est utilisé pour identifier le courrier en nombre comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9a92f-121">Anti-spam polices have a default BCL threshold that's used to identify bulk email as spam.</span></span> <span data-ttu-id="9a92f-122">Les administrateurs peuvent augmenter ou diminuer le seuil.</span><span class="sxs-lookup"><span data-stu-id="9a92f-122">Admins can increase or decrease the threshold.</span></span> <span data-ttu-id="9a92f-123">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a92f-123">For more information, see the following topics:</span></span>

- <span data-ttu-id="9a92f-124">[Configurez les stratégies de blocage du courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9a92f-124">[Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

- [<span data-ttu-id="9a92f-125">Paramètres de la stratégie anti-courrier indésirable EOP</span><span class="sxs-lookup"><span data-stu-id="9a92f-125">EOP anti-spam policy settings</span></span>](recommended-settings-for-eop-and-office365-atp.md#eop-anti-spam-policy-settings)

<span data-ttu-id="9a92f-126">Une autre option facile à oublier : si un utilisateur se plaint de recevoir du courrier en masse, mais que les messages proviennent d’expéditeurs dignes de réputation qui passent le filtrage du courrier indésirable dans EOP, demandez à l’utilisateur de vérifier une option de désinscription dans le message électronique en masse.</span><span class="sxs-lookup"><span data-stu-id="9a92f-126">Another option that's easy to overlook: if a user complains about receiving bulk email, but the messages are from reputable senders that pass spam filtering in EOP, have the user check for a unsubscribe option in the bulk email message.</span></span>
