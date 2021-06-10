---
title: Ajouter la prise en charge des e-mails entrants anonymes par IPv6
f1.keywords:
- NOCSH
author: chrisda
ms.author: chrisda
manager: chrisda
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: L’administrateur peut apprendre à configurer la prise en charge du courrier entrant anonyme à partir de sources IPv6 Exchange Online et Exchange Online Protection.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 80fdcc9dcfe3006ef8b21aa19856fe8c0ea3ff70
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52300048"
---
# <a name="add-support-for-anonymous-inbound-email-over-ipv6-in-microsoft-365"></a><span data-ttu-id="b84a1-103">Ajouter la prise en charge du courrier entrant anonyme sur IPv6 dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b84a1-103">Add support for anonymous inbound email over IPv6 in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="b84a1-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b84a1-104">**Applies to**</span></span>
- [<span data-ttu-id="b84a1-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b84a1-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="b84a1-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="b84a1-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="b84a1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b84a1-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="b84a1-108">Microsoft 365 organisations avec des boîtes aux lettres Exchange Online et des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online prendre en charge le courrier entrant anonyme sur IPv6.</span><span class="sxs-lookup"><span data-stu-id="b84a1-108">Microsoft 365 organizations with Exchange Online mailboxes and standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes support anonymous inbound email over IPv6.</span></span> <span data-ttu-id="b84a1-109">Le serveur de messagerie IPv6 source doit répondre aux deux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="b84a1-109">The source IPv6 email server must meet both of the following requirements:</span></span>

- <span data-ttu-id="b84a1-110">L’adresse IPv6 source doit avoir un enregistrement de recherche DNS inverse (PTR) valide qui permet à la destination de trouver le nom de domaine à partir de l’adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="b84a1-110">The source IPv6 address must have a valid reverse DNS lookup (PTR) record that allows the destination to find the domain name from the IPv6 address.</span></span>

- <span data-ttu-id="b84a1-111">L'expéditeur doit répondre aux exigences de l'étape de vérification SPF (définie dans le fichier [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou de l'étape de [vérification DKIM](http://dkim.org/) (définie dans le fichier [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span><span class="sxs-lookup"><span data-stu-id="b84a1-111">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](http://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>

<span data-ttu-id="b84a1-112">Avant que votre organisation puisse recevoir des messages entrants anonymes sur IPv6, un administrateur doit contacter le support Microsoft et le demander.</span><span class="sxs-lookup"><span data-stu-id="b84a1-112">Before your organization can receive anonymous inbound email over IPv6, an admin needs to contact Microsoft support and ask for it.</span></span> <span data-ttu-id="b84a1-113">Pour obtenir des instructions sur l’ouverture d’une demande de support, voir Contacter le support technique pour les [produits d’entreprise - Aide de l’administrateur.](../../business-video/get-help-support.md)</span><span class="sxs-lookup"><span data-stu-id="b84a1-113">For instructions about how to open a support request, see [Contact support for business products - Admin Help](../../business-video/get-help-support.md).</span></span>

<span data-ttu-id="b84a1-114">Une fois que la prise en charge des messages IPv6 entrants anonymes est activée dans votre organisation, le message passe par le filtrage des messages normal fourni par le service.</span><span class="sxs-lookup"><span data-stu-id="b84a1-114">After anonymous inbound IPv6 message support is enabled in your organization, the message will go through the normal message filtering that's provided by the service.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b84a1-115">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="b84a1-115">Troubleshooting</span></span>

- <span data-ttu-id="b84a1-116">Si le serveur de messagerie source n’a pas d’enregistrement de recherche DNS inverse IPv6, les messages sont rejetés avec l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="b84a1-116">If the source email server doesn't have an IPv6 reverse DNS lookup record, the messages will be rejected with the following error:</span></span>

  > <span data-ttu-id="b84a1-117">Service 450 4.7.25 indisponible, l’envoi de l’adresse IPv6 [2a01:111:f200:2004::240] doit avoir un enregistrement DNS inverse.</span><span class="sxs-lookup"><span data-stu-id="b84a1-117">450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.</span></span>

- <span data-ttu-id="b84a1-118">Si l’expéditeur ne passe pas la validation SPF ou DKIM, les messages sont rejetés avec l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="b84a1-118">If the sender doesn't pass SPF or DKIM validation, the messages will be rejected with the following error:</span></span>

  > <span data-ttu-id="b84a1-119">Service 450 4.7.26 indisponible, le message envoyé sur IPv6 [2a01:111:f200:2004::240] doit réussir la validation SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="b84a1-119">450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.</span></span>

- <span data-ttu-id="b84a1-120">Si vous essayez de recevoir des messages IPv6 anonymes avant de vous y rendre, le message sera rejeté avec l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="b84a1-120">If you try to receive anonymous IPv6 messages before you've opted in, the message will be rejected with the following error:</span></span>

  > <span data-ttu-id="b84a1-121">Service 550 5.2.1 indisponible, [contoso.com] n’accepte pas le courrier électronique sur IPv6.</span><span class="sxs-lookup"><span data-stu-id="b84a1-121">550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b84a1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b84a1-122">Related topics</span></span>

[<span data-ttu-id="b84a1-123">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="b84a1-123">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
