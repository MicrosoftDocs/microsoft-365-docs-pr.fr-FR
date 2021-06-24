---
title: Suivi des messages dans le portail Microsoft 365 Defender web
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent utiliser le lien de suivi des messages dans le portail Microsoft 365 Defender pour savoir ce qui est arrivé aux messages.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: f7b6f7b12086e46c6ad93b60e8c510ea533815a1
ms.sourcegitcommit: ebb1c3b4d94058a58344317beb9475c8a2eae9a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53108126"
---
# <a name="message-trace-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="cd63e-103">Suivi des messages dans le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="cd63e-103">Message trace in the Microsoft 365 Defender portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="cd63e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cd63e-104">**Applies to**</span></span>
- [<span data-ttu-id="cd63e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="cd63e-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="cd63e-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="cd63e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="cd63e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cd63e-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="cd63e-108">Le suivi des messages dans le portail Microsoft 365 Defender suit les messages électroniques lors de leur déplacement dans Exchange Online organisation.</span><span class="sxs-lookup"><span data-stu-id="cd63e-108">Message trace in the Microsoft 365 Defender portal follows email messages as they travel through your Exchange Online organization.</span></span> <span data-ttu-id="cd63e-109">Vous pouvez déterminer si un message a été reçu, rejeté, différé ou remis par le service.</span><span class="sxs-lookup"><span data-stu-id="cd63e-109">You can determine if a message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="cd63e-110">Cela indique également les actions entamées par rapport au message avant qu'il atteigne son statut final.</span><span class="sxs-lookup"><span data-stu-id="cd63e-110">It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="cd63e-111">Vous pouvez utiliser les informations du suivi des messages pour répondre efficacement aux questions des utilisateurs sur ce qui est arrivé aux messages, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie.</span><span class="sxs-lookup"><span data-stu-id="cd63e-111">You can use the information from message trace to efficiently answer user questions about what happened to messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

> [!NOTE]
> <span data-ttu-id="cd63e-112">Le suivi des messages dans Microsoft 365 Defender portail est simplement un accès au suivi des messages dans Exchange d’administration.</span><span class="sxs-lookup"><span data-stu-id="cd63e-112">Message trace in the Microsoft 365 Defender portal is just a pass through to Message trace in the Exchange admin center.</span></span> <span data-ttu-id="cd63e-113">Pour plus d’informations, voir [suivi des messages dans le centre d’administration Exchange moderne.](/exchange/monitoring/trace-an-email-message/message-trace-modern-eac)</span><span class="sxs-lookup"><span data-stu-id="cd63e-113">For more information, see [Message trace in the modern Exchange admin center](/exchange/monitoring/trace-an-email-message/message-trace-modern-eac).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="cd63e-114">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="cd63e-114">What do you need to know before you begin?</span></span>

- <span data-ttu-id="cd63e-115">Vous devez être membre des groupes  de  rôles Gestion de l’organisation, Gestion de la conformité ou Service d’Exchange Online pour utiliser le suivi des messages. </span><span class="sxs-lookup"><span data-stu-id="cd63e-115">You need to be a member of the **Organization Management**, **Compliance Management** or **Help Desk** role groups in **Exchange Online** to use message trace.</span></span> <span data-ttu-id="cd63e-116">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="cd63e-116">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="cd63e-117">**Remarques**: l’appartenance au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux _utilisateurs_ les autorisations et autorisations requises pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cd63e-117">**Notes**: Membership in the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="cd63e-118">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd63e-118">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

- <span data-ttu-id="cd63e-119">Le nombre maximal de messages affichés dans les résultats d’un suivi des messages dépend du type de rapport que vous avez sélectionné (voir la section Choisir le [type](/exchange/monitoring/trace-an-email-message/message-trace-modern-eac#choose-report-type) de rapport pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="cd63e-119">The maximum number of messages that are displayed in the results of a message trace depends on the report type you selected (see the [Choose report type](/exchange/monitoring/trace-an-email-message/message-trace-modern-eac#choose-report-type) section for details).</span></span> <span data-ttu-id="cd63e-120">[L’cmdlet Get-HistoricalSearch](/powershell/module/exchange/get-historicalsearch) dans Exchange Online PowerShell ou EOP PowerShell autonome renvoie tous les messages dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="cd63e-120">The [Get-HistoricalSearch](/powershell/module/exchange/get-historicalsearch) cmdlet in Exchange Online PowerShell or standalone EOP PowerShell returns all messages in the results.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="cd63e-121">Ouvrir le suivi des messages</span><span class="sxs-lookup"><span data-stu-id="cd63e-121">Open message trace</span></span>

<span data-ttu-id="cd63e-122">Dans le portail Microsoft 365 Defender ( <https://security.microsoft.com> ), go to Email & **collaboration** Exchange \> **message trace**.</span><span class="sxs-lookup"><span data-stu-id="cd63e-122">In the Microsoft 365 Defender portal (<https://security.microsoft.com>), go to **Email & collaboration** \> **Exchange message trace**.</span></span> <span data-ttu-id="cd63e-123">Ou, pour aller directement à la page de suivi des messages, utilisez <https://admin.exchange.microsoft.com/#/messagetrace> .</span><span class="sxs-lookup"><span data-stu-id="cd63e-123">Or, to go directly to the message trace page, use <https://admin.exchange.microsoft.com/#/messagetrace>.</span></span>

<span data-ttu-id="cd63e-124">À ce stade, le suivi des messages dans le EAC s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="cd63e-124">At this point, message trace in the EAC opens.</span></span> <span data-ttu-id="cd63e-125">Pour plus d’informations, voir [suivi des messages dans le centre d’administration Exchange moderne.](/exchange/monitoring/trace-an-email-message/message-trace-modern-eac)</span><span class="sxs-lookup"><span data-stu-id="cd63e-125">For more information, see [Message trace in the modern Exchange admin center](/exchange/monitoring/trace-an-email-message/message-trace-modern-eac).</span></span>
