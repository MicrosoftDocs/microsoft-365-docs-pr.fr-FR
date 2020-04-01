---
title: Ajouter la prise en charge du courrier électronique entrant anonyme sur IPv6
f1.keywords:
- NOCSH
author: chrisda
ms.author: chrisda
manager: chrisda
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
ms.collection:
- M365-security-compliance
description: L’administrateur peut apprendre à configurer la prise en charge des messages électroniques entrants anonymes provenant de sources IPv6 dans Exchange Online et Exchange Online Protection.
ms.openlocfilehash: 67e839249d41381be22bbccf6b09d1616c387c66
ms.sourcegitcommit: 748bc3484b7ccbd65b558f495b6fa42196c3c571
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2020
ms.locfileid: "43083640"
---
# <a name="add-support-for-anonymous-inbound-email-over-ipv6-in-office-365"></a><span data-ttu-id="9156a-103">Ajouter la prise en charge du courrier électronique entrant anonyme sur IPv6 dans Office 365</span><span class="sxs-lookup"><span data-stu-id="9156a-103">Add support for anonymous inbound email over IPv6 in Office 365</span></span>

<span data-ttu-id="9156a-104">Les organisations Office 365 avec des boîtes aux lettres Exchange Online et les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online prennent en charge les messages électroniques entrants anonymes sur IPv6.</span><span class="sxs-lookup"><span data-stu-id="9156a-104">Office 365 organizations with Exchange Online mailboxes and standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes support anonymous inbound email over IPv6.</span></span> <span data-ttu-id="9156a-105">Le serveur de messagerie IPv6 source doit respecter les deux conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9156a-105">The source IPv6 email server must meet both of the following requirements:</span></span>

- <span data-ttu-id="9156a-106">L’adresse IPv6 source doit avoir un enregistrement DNS de recherche inversée (PTR) valide qui permet à la destination de trouver le nom de domaine à partir de l’adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="9156a-106">The source IPv6 address must have a valid reverse DNS lookup (PTR) record that allows the destination to find the domain name from the IPv6 address.</span></span>

- <span data-ttu-id="9156a-107">L'expéditeur doit répondre aux exigences de l'étape de vérification SPF (définie dans le fichier [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou de l'étape de [vérification DKIM](https://dkim.org/) (définie dans le fichier [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span><span class="sxs-lookup"><span data-stu-id="9156a-107">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](https://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>

<span data-ttu-id="9156a-108">Pour que votre organisation puisse recevoir des messages électroniques entrants anonymes sur IPv6, un administrateur doit contacter le support Microsoft et lui demander :</span><span class="sxs-lookup"><span data-stu-id="9156a-108">Before your organization can receive anonymous inbound email over IPv6, an admin needs to contact Microsoft support and ask for it:</span></span>

1. <span data-ttu-id="9156a-109">Ouvrez le centre d’administration Microsoft 365 <https://admin.microsoft.com/adminportal/home> à l’adresse, puis cliquez sur **aide** ( ?).</span><span class="sxs-lookup"><span data-stu-id="9156a-109">Open the Microsoft 365 admin center at <https://admin.microsoft.com/adminportal/home> and click **Help** (?).</span></span>

2. <span data-ttu-id="9156a-110">Dans le menu déroulant **besoin d’aide ?** qui s’affiche, tapez un texte descriptif dans la zone de recherche (par exemple, « demander un message électronique IPv6 entrant anonyme »), puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="9156a-110">In the **Need help?** flyout that appears, type something descriptive in the search box (for example, "request anonymous inbound IPv6 email"), and then press ENTER.</span></span>

3. <span data-ttu-id="9156a-111">Au bas de la page, cliquez sur **contacter le support technique**.</span><span class="sxs-lookup"><span data-stu-id="9156a-111">At the bottom of the page, click **Contact support**.</span></span>

4. <span data-ttu-id="9156a-112">Sur la page **contacter le support technique** qui apparaît, renseignez et vérifiez les informations (faites défiler l’affichage si nécessaire), puis cliquez sur **me contacter**.</span><span class="sxs-lookup"><span data-stu-id="9156a-112">In the **Contact support** page that appears, fill out and verify the information (scroll down as necessary), and then click **Contact me**.</span></span>

<span data-ttu-id="9156a-113">Une fois que la prise en charge des messages IPv6 entrants anonymes est activée dans votre organisation, le message passe par le filtre de messages normal fourni par le service.</span><span class="sxs-lookup"><span data-stu-id="9156a-113">After anonymous inbound IPv6 message support is enabled in your organization, the message will go through the normal message filtering that's provided by the service.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9156a-114">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="9156a-114">Troubleshooting</span></span>

- <span data-ttu-id="9156a-115">Si le serveur de messagerie source ne dispose pas d’un enregistrement de recherche DNS inversée IPv6, les messages seront rejetés avec l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="9156a-115">If the source email server doesn't have an IPv6 reverse DNS lookup record, the messages will be rejected with the following error:</span></span>

  > <span data-ttu-id="9156a-116">450 4.7.25 Service indisponible, envoi de l’adresse IPv6 [2a01:111 : F200:2004 :: 240] doit avoir un enregistrement DNS inverse.</span><span class="sxs-lookup"><span data-stu-id="9156a-116">450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.</span></span>

- <span data-ttu-id="9156a-117">Si l’expéditeur ne passe pas la validation SPF ou DKIM, les messages sont rejetés avec l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="9156a-117">If the sender doesn't pass SPF or DKIM validation, the messages will be rejected with the following error:</span></span>

  > <span data-ttu-id="9156a-118">450 4.7.26 Service indisponible, le message envoyé via IPv6 [2a01:111 : F200:2004 :: 240] doit transmettre la validation SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="9156a-118">450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.</span></span>

- <span data-ttu-id="9156a-119">Si vous tentez de recevoir des messages IPv6 anonymes avant d’avoir choisi, le message sera rejeté avec l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="9156a-119">If you try to receive anonymous IPv6 messages before you've opted in, the message will be rejected with the following error:</span></span>

  > <span data-ttu-id="9156a-120">550 5.2.1 Service indisponible, [contoso.com] n’accepte pas le courrier électronique sur IPv6.</span><span class="sxs-lookup"><span data-stu-id="9156a-120">550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="9156a-121">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="9156a-121">For more information</span></span>

[<span data-ttu-id="9156a-122">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="9156a-122">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
