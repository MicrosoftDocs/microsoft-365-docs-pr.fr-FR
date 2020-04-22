---
title: Utiliser le portail supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 04/18/2016
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: Vous recevez un message d’erreur lorsque vous essayez d’envoyer un message électronique à un destinataire dont l’adresse de messagerie est dans Microsoft 365 ? Si vous pensez que vous ne devriez pas recevoir le message d’erreur, vous pouvez utiliser le portail supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués.
ms.openlocfilehash: 39f2c9335f162f26e8bf07a213236e0e0eefef2a
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43636403"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="95997-104">Utiliser le portail supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués</span><span class="sxs-lookup"><span data-stu-id="95997-104">Use the delist portal to remove yourself from the blocked senders list</span></span>

<span data-ttu-id="95997-105">Vous recevez un message d’erreur lorsque vous essayez d’envoyer un message électronique à un destinataire dont l’adresse de messagerie est dans Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="95997-105">Are you getting an error message when you try to send an email to a recipient whose email address is in Microsoft 365?</span></span> <span data-ttu-id="95997-106">Si vous pensez que vous ne devriez pas recevoir le message d’erreur, vous pouvez utiliser le portail supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="95997-106">If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the blocked senders list.</span></span>

## <a name="what-is-the-blocked-senders-list"></a><span data-ttu-id="95997-107">Qu’est-ce que la liste des expéditeurs bloqués ?</span><span class="sxs-lookup"><span data-stu-id="95997-107">What is the blocked senders list?</span></span>

<span data-ttu-id="95997-108">Microsoft utilise la liste des expéditeurs bloqués pour protéger ses clients contre le courrier indésirable, l'usurpation d'identité et les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="95997-108">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks.</span></span> <span data-ttu-id="95997-109">L’adresse IP de votre serveur de messagerie, autrement dit, l’adresse que votre serveur de messagerie utilise pour s’identifier sur Internet, a été marquée comme une menace potentielle pour Microsoft 365 pour l’une des raisons.</span><span class="sxs-lookup"><span data-stu-id="95997-109">Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Microsoft 365 for one of a variety of reasons.</span></span> <span data-ttu-id="95997-110">Lorsque Microsoft 365 ajoute l’adresse IP à la liste, il empêche toute communication supplémentaire entre l’adresse IP et l’un de nos clients via nos centres de connaissances.</span><span class="sxs-lookup"><span data-stu-id="95997-110">When Microsoft 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>

<span data-ttu-id="95997-111">Vous savez que vous avez été ajouté à la liste si vous recevez une réponse à un courrier électronique incluant une erreur ressemblant à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="95997-111">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>

> <span data-ttu-id="95997-112">550 5.7.606-649 accès refusé, IP d’envoi interdit [_adresse IP_]; Pour demander la suppression de cette liste, https://sender.office.com/ visitez le site et suivez les instructions.</span><span class="sxs-lookup"><span data-stu-id="95997-112">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit https://sender.office.com/ and follow the directions.</span></span> <span data-ttu-id="95997-113">Pour plus d’informations, consultez la rubrique [notifications de non-remise aux messages électroniques dans Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online).</span><span class="sxs-lookup"><span data-stu-id="95997-113">For more information see [Email non-delivery reports in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online).</span></span>

<span data-ttu-id="95997-114">où  _IP address_ est l'adresse IP de l'ordinateur sur lequel s'exécute le serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="95997-114">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span>

### <a name="to-use-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="95997-115">Pour utiliser le portail déliste pour vous supprimer de la liste des expéditeurs bloqués</span><span class="sxs-lookup"><span data-stu-id="95997-115">To use delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="95997-116">Dans un navigateur web, accédez à [https://sender.office.com](https://sender.office.com).</span><span class="sxs-lookup"><span data-stu-id="95997-116">In a web browser, go to [https://sender.office.com](https://sender.office.com).</span></span>

2. <span data-ttu-id="95997-p105">Suivez les instructions de la page. Assurez-vous que vous utilisez l'adresse de messagerie à laquelle le message d'erreur a été envoyé et l'adresse IP qui est spécifiée dans le message d'erreur. Vous ne pouvez entrer qu'une adresse de messagerie et une adresse IP par visite.</span><span class="sxs-lookup"><span data-stu-id="95997-p105">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>

3. <span data-ttu-id="95997-120">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="95997-120">Click **Submit**.</span></span>

    <span data-ttu-id="95997-121">Le portail envoie un courrier électronique à l'adresse de messagerie que vous indiquez.</span><span class="sxs-lookup"><span data-stu-id="95997-121">The portal sends an email to the email address that you supply.</span></span> <span data-ttu-id="95997-122">Le message électronique se présente comme suit : ![capture d’écran du courrier électronique reçu lorsque vous envoyez une demande via le portail supprimer de la liste](../../media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="95997-122">The email will look something like the following: ![Screenshot of email received when you submit a request through the delist portal](../../media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>

4. <span data-ttu-id="95997-123">Cliquez sur le lien de confirmation dans le courrier électronique envoyé par le portail de suppression de la liste.</span><span class="sxs-lookup"><span data-stu-id="95997-123">Click the confirmation link in the email sent to you by the delisting portal.</span></span>

    <span data-ttu-id="95997-124">Vous revenez au portail Supprimer de la liste.</span><span class="sxs-lookup"><span data-stu-id="95997-124">This brings you back to the delist portal.</span></span>

5. <span data-ttu-id="95997-125">Dans le portail Supprimer de la liste, cliquez sur **Supprimer l'adresse IP de la liste**.</span><span class="sxs-lookup"><span data-stu-id="95997-125">In the delist portal, click **Delist IP**.</span></span>

    <span data-ttu-id="95997-126">Une fois que l’adresse IP a été supprimée de la liste des expéditeurs bloqués, les messages électroniques provenant de cette adresse IP seront remis aux destinataires qui utilisent Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95997-126">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Microsoft 365.</span></span> <span data-ttu-id="95997-127">Par conséquent, assurez-vous que vous êtes sûr que les messages envoyés à partir de cette adresse IP ne seront pas injurieux ou malveillants ; dans le cas contraire, l’adresse IP peut être de nouveau bloquée.</span><span class="sxs-lookup"><span data-stu-id="95997-127">So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>

    > [!NOTE]
    > <span data-ttu-id="95997-128">Cette opération peut prendre jusqu’à 24 heures ou les résultats peuvent varier considérablement avant la suppression des restrictions.</span><span class="sxs-lookup"><span data-stu-id="95997-128">It may take up to 24 hours or results can vary widely before restrictions are removed.</span></span>

<span data-ttu-id="95997-129">Consultez la rubrique [créer des listes d’expéditeurs approuvés dans office 365](create-safe-sender-lists-in-office-365.md) et protection contre le [courrier indésirable sortant dans Office 365](outbound-spam-controls.md) pour empêcher la liste de blocage sur IP.</span><span class="sxs-lookup"><span data-stu-id="95997-129">See [Create safe sender lists in Office 365](create-safe-sender-lists-in-office-365.md) and [Outbound spam protection in Office 365](outbound-spam-controls.md) to prevent IP from being blacklisted.</span></span>
