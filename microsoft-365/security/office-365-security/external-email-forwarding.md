---
title: Configuration et contrôle du transfert de messages externes, du transfert automatique, de l’accès 5.7.520 refusé, de la désactivation du transfert externe, votre administrateur a désactivé le transfert externe, stratégie anti-courrier indésirable sortant
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/01/2020
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: .
ms.openlocfilehash: 88c3dae4f5a6786fe4eddea0d5e1c61dda837a87
ms.sourcegitcommit: 5b769f74bcc76ac8d38aad815d1728824783cd9f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "45080112"
---
# <a name="configuring-external-email-forwarding-in-office-365"></a><span data-ttu-id="65d92-103">Configuration du transfert de messages électroniques externes dans Office 365</span><span class="sxs-lookup"><span data-stu-id="65d92-103">Configuring external email forwarding in Office 365</span></span>

<span data-ttu-id="65d92-104">Le transfert externe est contrôlé par la *stratégie anti-courrier indésirable sortant* et l’étendue aux utilisateurs en fonction du paramètre configuré.</span><span class="sxs-lookup"><span data-stu-id="65d92-104">External forwarding is controlled by the *outbound anti-spam policy* and scoped to users based on the configured setting.</span></span> <span data-ttu-id="65d92-105">Actuellement, 3 les paramètres sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="65d92-105">Currently 3 settings are supported:</span></span>

- <span data-ttu-id="65d92-106">**Automatique** : dans ce mode, le système est chargé de décider si un message transféré est autorisé ou non.</span><span class="sxs-lookup"><span data-stu-id="65d92-106">**Automatic** – In this mode the system is responsible for deciding if a forwarded message is allowed or not.</span></span>  <span data-ttu-id="65d92-107">Il s’agit du mode par défaut et, dans ce mode, le système bloque le transfert externe automatique.</span><span class="sxs-lookup"><span data-stu-id="65d92-107">This is the default mode and in this mode the system will block automatic external forwarding.</span></span>

- <span data-ttu-id="65d92-108">**Activé – le** transfert externe automatique est autorisé et non restreint.</span><span class="sxs-lookup"><span data-stu-id="65d92-108">**On** – Automatic external forwarding is allowed and not restricted.</span></span>

- <span data-ttu-id="65d92-109">**Off** : le transfert externe automatique est désactivé et entraîne une notification d’échec de remise à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="65d92-109">**Off** – Automatic external forwarding is disabled and will result in a Non-delivery report (NDR) to the end user.</span></span>

<span data-ttu-id="65d92-110">Pour plus d’informations sur la configuration de ces paramètres, voir [configurer le filtrage du courrier indésirable sortant dans EOP](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-the-outbound-spam-policy?view=o365-worldwide) .</span><span class="sxs-lookup"><span data-stu-id="65d92-110">See [Configure outbound spam filtering in EOP](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-the-outbound-spam-policy?view=o365-worldwide) for more information on how to configure these settings.</span></span>

## <a name="controlling-external-email-forwarding"></a><span data-ttu-id="65d92-111">Contrôle du transfert du courrier électronique externe</span><span class="sxs-lookup"><span data-stu-id="65d92-111">Controlling external email forwarding</span></span>

<span data-ttu-id="65d92-112">En tant qu’administrateur d’une organisation, vous pouvez avoir des exigences en matière d’entreprise pour limiter ou contrôler qui est en mesure de transférer automatiquement des courriers électroniques à l’aide de règles de boîte de réception ou de l’envoi SMTP, en dehors de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="65d92-112">As an admin of an organization you may have company requirements to restrict or control who is able to automatically forward emails using inbox rules, or SMTP forwarding, outside of the organization.</span></span> <span data-ttu-id="65d92-113">Le transfert du courrier peut être une fonctionnalité utile, mais peut également présenter un risque grâce à une divulgation potentielle d’informations, même en fournissant des informations aux attaquants qui peuvent être exploités pour attaquer l’organisation ou ses partenaires.</span><span class="sxs-lookup"><span data-stu-id="65d92-113">Email forwarding can be a useful feature, but can also pose a risk through the potential disclosure of information, even by providing information to attackers that can be leveraged to attack the organization or its partners.</span></span>

<span data-ttu-id="65d92-114">Office 365 n’autorise pas le transfert externe automatique par les règles de boîte de réception ou la configuration des boîtes aux lettres, qui fournit une stratégie par défaut sécurisée.</span><span class="sxs-lookup"><span data-stu-id="65d92-114">Office 365 doesn't allow automatic external forwarding by either Inbox rules or mail box configuration, which provides a secure default policy.</span></span> <span data-ttu-id="65d92-115">Toutefois, l’administrateur peut modifier ces paramètres pour tous les utilisateurs de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="65d92-115">However, the admin can modify these settings for all, or some, users in the organization.</span></span> <span data-ttu-id="65d92-116">Le transfert de messages entre les utilisateurs internes n’est pas affecté par une telle modification.</span><span class="sxs-lookup"><span data-stu-id="65d92-116">Forwarding messages between internal users isn't affected by such a modification.</span></span>

> [!NOTE]
> <span data-ttu-id="65d92-117">La désactivation du transfert automatique vers des adresses externes dans Office 365 est effectuée en phases avec des détails communiqués via des publications du [Centre de messages](https://admin.microsoft.com/Adminportal/Home?source=applauncher&ref=/MessageCenter) .</span><span class="sxs-lookup"><span data-stu-id="65d92-117">Disabling automatic forwarding to external addresses in Office 365 is being rolled out in phases with details communicated via [Message Center](https://admin.microsoft.com/Adminportal/Home?source=applauncher&ref=/MessageCenter) posts.</span></span> <span data-ttu-id="65d92-118">Pour aider les administrateurs à se préparer à ces modifications, demandez-leur de modifier les stratégies à l’avance afin de s’assurer que les utilisateurs ne sont pas perturbés.</span><span class="sxs-lookup"><span data-stu-id="65d92-118">To help administrators prepare for these changes have them modify policies ahead of time to ensure there is no disruption to their users.</span></span>

<span data-ttu-id="65d92-119">Vous trouverez plus d’informations sur les utilisateurs qui utilisent le transfert automatique (règles de boîte de réception ou le transfert SMTP) dans votre organisation dans le [rapport de messages transférés automatiquement](https://docs.microsoft.com/microsoft-365/security/office-365-security/mfi-auto-forwarded-messages-report?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="65d92-119">More information about users that are using automatic forwarding (inbox rules or SMTP forwarding) in your organization can be found in the [auto-forwarded messages report](https://docs.microsoft.com/microsoft-365/security/office-365-security/mfi-auto-forwarded-messages-report?view=o365-worldwide).</span></span>

## <a name="the-blocked-email-forwarding-message"></a><span data-ttu-id="65d92-120">Message de transfert de courrier électronique bloqué</span><span class="sxs-lookup"><span data-stu-id="65d92-120">The blocked email forwarding message</span></span>

<span data-ttu-id="65d92-121">Lorsqu’un message est détecté comme étant automatiquement transféré et que la stratégie d’organisation *bloque* cette activité, une notification d’échec de **remise (NDR)** est renvoyée à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="65d92-121">When a message is detected as automatically forwarded and the organizational policy *blocks* that activity a **Non-delivery report (NDR)** will be generated back to the end user.</span></span> <span data-ttu-id="65d92-122">Le rapport indiquera que le message n’a pas été remis.</span><span class="sxs-lookup"><span data-stu-id="65d92-122">The report will indicate the message was not delivered.</span></span> <span data-ttu-id="65d92-123">Le rapport de non-remise aura le format suivant :</span><span class="sxs-lookup"><span data-stu-id="65d92-123">The NDR will have the following format:</span></span> 

`5.7.520 Access Denied – Your administrator has disabled external forwarding – AS(XXXX)`
