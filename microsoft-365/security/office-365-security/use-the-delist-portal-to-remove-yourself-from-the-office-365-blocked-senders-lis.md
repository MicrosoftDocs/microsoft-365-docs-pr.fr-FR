---
title: Supprimez-vous de la liste des expéditeurs bloqués
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 04/18/2016
audience: ITPro
ms.topic: troubleshooting
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez apprendre à utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Microsoft 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: aef3a5946dee9df7d12232c179f23386db459e06
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50921107"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="d9669-103">Utiliser le portail Retirer d’une liste pour vous supprimer de la liste des expéditeurs bloqués</span><span class="sxs-lookup"><span data-stu-id="d9669-103">Use the delist portal to remove yourself from the blocked senders list</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="d9669-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d9669-104">**Applies to**</span></span>
- [<span data-ttu-id="d9669-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="d9669-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="d9669-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="d9669-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="d9669-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d9669-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="d9669-108">Recevez-vous un message d’erreur lorsque vous essayez d’envoyer un courrier électronique à un destinataire dont l’adresse de messagerie se trouve dans Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="d9669-108">Are you getting an error message when you try to send an email to a recipient whose email address is in Microsoft 365?</span></span> <span data-ttu-id="d9669-109">Si vous pensez ne pas recevoir le message d’erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="d9669-109">If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the blocked senders list.</span></span>

## <a name="what-is-the-blocked-senders-list"></a><span data-ttu-id="d9669-110">Qu’est-ce que la liste des expéditeurs bloqués ?</span><span class="sxs-lookup"><span data-stu-id="d9669-110">What is the blocked senders list?</span></span>

<span data-ttu-id="d9669-111">Microsoft utilise la liste des expéditeurs bloqués pour protéger ses clients contre le courrier indésirable, l'usurpation d'identité et les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="d9669-111">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks.</span></span> <span data-ttu-id="d9669-112">L’adresse IP de votre serveur de messagerie, c’est-à-dire l’adresse que votre serveur de messagerie utilise pour s’identifier sur Internet, a été marquée comme une menace potentielle pour Microsoft 365 pour diverses raisons.</span><span class="sxs-lookup"><span data-stu-id="d9669-112">Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Microsoft 365 for one of a variety of reasons.</span></span> <span data-ttu-id="d9669-113">Lorsque Microsoft 365 ajoute l’adresse IP à la liste, il empêche toute communication supplémentaire entre l’adresse IP et l’un de nos clients via nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="d9669-113">When Microsoft 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>

<span data-ttu-id="d9669-114">Vous savez que vous avez été ajouté à la liste si vous recevez une réponse à un courrier électronique incluant une erreur ressemblant à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d9669-114">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>

> <span data-ttu-id="d9669-115">550 5.7.606-649 Accès refusé, adresse _IP_ d’envoi interdite [ adresse IP ]; Pour demander la suppression de cette liste, visitez <https://sender.office.com/> et suivez les instructions.</span><span class="sxs-lookup"><span data-stu-id="d9669-115">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit <https://sender.office.com/> and follow the directions.</span></span> <span data-ttu-id="d9669-116">Pour plus d’informations, [consultez les rapports de non-remise par courrier électronique dans Exchange Online.](/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online)</span><span class="sxs-lookup"><span data-stu-id="d9669-116">For more information see [Email non-delivery reports in Exchange Online](/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online).</span></span>

<span data-ttu-id="d9669-117">où  _IP address_ est l'adresse IP de l'ordinateur sur lequel s'exécute le serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d9669-117">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span>

### <a name="to-use-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="d9669-118">Pour utiliser le portail supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués</span><span class="sxs-lookup"><span data-stu-id="d9669-118">To use delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="d9669-119">Dans un navigateur web, accédez à <https://sender.office.com>.</span><span class="sxs-lookup"><span data-stu-id="d9669-119">In a web browser, go to <https://sender.office.com>.</span></span>

2. <span data-ttu-id="d9669-p104">Suivez les instructions de la page. Assurez-vous que vous utilisez l'adresse de messagerie à laquelle le message d'erreur a été envoyé et l'adresse IP qui est spécifiée dans le message d'erreur. Vous ne pouvez entrer qu'une adresse de messagerie et une adresse IP par visite.</span><span class="sxs-lookup"><span data-stu-id="d9669-p104">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>

3. <span data-ttu-id="d9669-123">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="d9669-123">Click **Submit**.</span></span>

    <span data-ttu-id="d9669-124">Le portail envoie un courrier électronique à l'adresse de messagerie que vous indiquez.</span><span class="sxs-lookup"><span data-stu-id="d9669-124">The portal sends an email to the email address that you supply.</span></span> <span data-ttu-id="d9669-125">L’e-mail ressemblera à ce qui suit : Capture d’écran du courrier électronique reçu lorsque vous envoyez une demande ![ via le portail Delist](../../media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="d9669-125">The email will look something like the following: ![Screenshot of email received when you submit a request through the delist portal](../../media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>

4. <span data-ttu-id="d9669-126">Cliquez sur le lien de confirmation dans le courrier électronique envoyé par le portail de suppression de la liste.</span><span class="sxs-lookup"><span data-stu-id="d9669-126">Click the confirmation link in the email sent to you by the delisting portal.</span></span>

    <span data-ttu-id="d9669-127">Vous revenez au portail Supprimer de la liste.</span><span class="sxs-lookup"><span data-stu-id="d9669-127">This brings you back to the delist portal.</span></span>

5. <span data-ttu-id="d9669-128">Dans le portail Supprimer de la liste, cliquez sur **Supprimer l'adresse IP de la liste**.</span><span class="sxs-lookup"><span data-stu-id="d9669-128">In the delist portal, click **Delist IP**.</span></span>

    <span data-ttu-id="d9669-129">Une fois l’adresse IP supprimée de la liste des expéditeurs bloqués, les messages électroniques provenant de cette adresse IP sont remis aux destinataires qui utilisent Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d9669-129">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Microsoft 365.</span></span> <span data-ttu-id="d9669-130">Assurez-vous donc que les messages électroniques envoyés à partir de cette adresse IP ne seront pas abusifs ou malveillants ; Dans le cas contraire, l’adresse IP risque d’être de nouveau bloquée.</span><span class="sxs-lookup"><span data-stu-id="d9669-130">So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9669-131">Cela peut prendre jusqu’à 24 heures ou les résultats peuvent varier considérablement avant la suppression des restrictions.</span><span class="sxs-lookup"><span data-stu-id="d9669-131">It may take up to 24 hours or results can vary widely before restrictions are removed.</span></span>

<span data-ttu-id="d9669-132">Voir [Créer des listes d’expéditeurs](create-safe-sender-lists-in-office-365.md) sûrs dans EOP et la protection contre le courrier indésirable sortant dans [EOP](outbound-spam-controls.md) pour empêcher le blocage d’une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="d9669-132">See [Create safe sender lists in EOP](create-safe-sender-lists-in-office-365.md) and [Outbound spam protection in EOP](outbound-spam-controls.md) to prevent an IP from being blocked.</span></span>