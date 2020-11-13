---
title: Services pour les non-clients envoyant des courriers électroniques à Microsoft 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 19fd3e0f-8dbf-4049-a810-2c8ee6cefd48
ms.collection:
- M365-security-compliance
description: Pour préserver la confiance des utilisateurs dans l'utilisation de la messagerie électronique, Microsoft a mis en place diverses stratégies et technologies pour aider à protéger ses utilisateurs.
ms.openlocfilehash: 478f94d2ed1a03253168486d48fb2b2df57a6a5e
ms.sourcegitcommit: 9546708a5506fdbadbfe2500cbf1bd1aeaec6fcb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2020
ms.locfileid: "49021024"
---
# <a name="services-for-non-customers-sending-mail-to-microsoft-365"></a><span data-ttu-id="554b4-103">Services pour les non-clients envoyant des courriers électroniques à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="554b4-103">Services for non-customers sending mail to Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="554b4-104">L'utilisation abusive de la messagerie électronique, les courriers indésirables et les e-mails frauduleux (hameçonnage) continuent à peser sur l'ensemble de l'écosystème de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="554b4-104">Email abuse, junk email, and fraudulent emails (phishing) continue to burden the entire email ecosystem.</span></span> <span data-ttu-id="554b4-105">Pour faciliter la gestion de l’approbation des utilisateurs dans l’utilisation de la messagerie, Microsoft a mis en place différentes stratégies et technologies afin de protéger les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="554b4-105">To help maintain user trust in the use of email, Microsoft has put various policies and technologies in place to help protect our users.</span></span> <span data-ttu-id="554b4-106">Cependant, Microsoft comprend que les e-mails légitimes ne doivent pas être affectés négativement.</span><span class="sxs-lookup"><span data-stu-id="554b4-106">However, Microsoft understands that legitimate email should not be negatively affected.</span></span> <span data-ttu-id="554b4-107">Par conséquent, nous avons établi une suite de services pour aider les expéditeurs à améliorer leur capacité à livrer des courriers électroniques aux utilisateurs de Microsoft 365 en gérant leur réputation d’envoi de manière proactive.</span><span class="sxs-lookup"><span data-stu-id="554b4-107">Therefore, we have established a suite of services to help senders improve their ability to deliver email to Microsoft 365 users by proactively managing their sending reputation.</span></span>

<span data-ttu-id="554b4-108">Cette vue d’ensemble fournit des informations sur les avantages que nous fournissons à votre organisation, même si vous n’êtes pas un client.</span><span class="sxs-lookup"><span data-stu-id="554b4-108">This overview provides information about benefits we provide to your organization even if you aren't a customer.</span></span>

## <a name="sender-solutions"></a><span data-ttu-id="554b4-109">Solutions de l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="554b4-109">Sender solutions</span></span>

****

|<span data-ttu-id="554b4-110">Service</span><span class="sxs-lookup"><span data-stu-id="554b4-110">Service</span></span>|<span data-ttu-id="554b4-111">Avantages</span><span class="sxs-lookup"><span data-stu-id="554b4-111">Benefits</span></span>|
|---|---|
|<span data-ttu-id="554b4-112">Ce contenu d'aide en ligne</span><span class="sxs-lookup"><span data-stu-id="554b4-112">This online help content</span></span>|<span data-ttu-id="554b4-113">Fournit :</span><span class="sxs-lookup"><span data-stu-id="554b4-113">Provides:</span></span> <ul><li><span data-ttu-id="554b4-114">Point de départ pour toutes les questions relatives à la remise des communications aux utilisateurs EOP.</span><span class="sxs-lookup"><span data-stu-id="554b4-114">A starting point for any questions related to delivering communications to EOP users.</span></span></li><li><span data-ttu-id="554b4-115">Comprend un guide en ligne simple avec nos stratégies et exigences.</span><span class="sxs-lookup"><span data-stu-id="554b4-115">Includes a simple online guide with our policies and requirements.</span></span></li><li><span data-ttu-id="554b4-116">Vue d’ensemble des filtres de courrier indésirable et des technologies d’authentification employés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="554b4-116">An overview of the junk email filters and authentication technologies employed by Microsoft.</span></span></li><ul>|
|[<span data-ttu-id="554b4-117">Support technique Microsoft</span><span class="sxs-lookup"><span data-stu-id="554b4-117">Microsoft support</span></span>](#microsoft-support)|<span data-ttu-id="554b4-118">Offre un support autonome et de transmission à une instance supérieure pour les problèmes de remise.</span><span class="sxs-lookup"><span data-stu-id="554b4-118">Provides self-help and escalation support for delivery issues.</span></span>|
|[<span data-ttu-id="554b4-119">Portail d’adresses IP de blocage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="554b4-119">Anti-Spam IP Delist Portal</span></span>](#anti-spam-ip-delist-portal)|<span data-ttu-id="554b4-p102">Un outil permettant d'envoyer une demande de suppression d'adresse IP de la liste. Avant d'envoyer cette demande, il incombe à l'expéditeur de s'assurer que tout autre courrier provenant de l'adresse IP en question n'est pas abusif ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="554b4-p102">A tool to submit IP delist request. Before submitting this request it is the sender's responsibility to ensure that any further mail originating from the IP in question is not abusive or malicious.</span></span>|
|[<span data-ttu-id="554b4-122">Création de rapport de courrier indésirable et de mauvaise utilisation pour le courrier indésirable provenant d'Exchange Online</span><span class="sxs-lookup"><span data-stu-id="554b4-122">Abuse and spam reporting for junk email originating from Exchange Online</span></span>](#abuse-and-spam-reporting-for-junk-email-originating-from-exchange-online)|<span data-ttu-id="554b4-123">Empêche l’envoi de courrier indésirable et d’autres messages indésirables à partir d’Exchange Online et le désordre sur Internet et votre système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="554b4-123">Keeps spam and other unwanted mail from being sent from Exchange Online and cluttering up the internet and your mail system.</span></span>|
|

## <a name="microsoft-support"></a><span data-ttu-id="554b4-124">Support technique Microsoft</span><span class="sxs-lookup"><span data-stu-id="554b4-124">Microsoft support</span></span>

<span data-ttu-id="554b4-125">Microsoft offre plusieurs options de prise en charge pour les personnes qui rencontrent des problèmes pour envoyer des messages à des destinataires Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="554b4-125">Microsoft offers several support options for people having trouble sending mail to Microsoft 365 recipients.</span></span> <span data-ttu-id="554b4-126">Nous vous recommandons d'effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="554b4-126">We recommend that you:</span></span>

- <span data-ttu-id="554b4-127">Suivez les instructions fournies dans les rapports de non-remise que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="554b4-127">Follow the instructions in any non-delivery report you receive.</span></span>

- <span data-ttu-id="554b4-128">Consultez les problèmes les plus courants que rencontrent les non clients dans [Résolution des problèmes de messages envoyés à Office 365](troubleshooting-mail-sent-to-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="554b4-128">Check out the most common problems that non-customers encounter in [Troubleshooting mail sent to Office 365](troubleshooting-mail-sent-to-office-365.md).</span></span>

- <span data-ttu-id="554b4-129">Utilisez le [portail délister Microsoft 365](https://sender.office.com) pour soumettre une demande de suppression de votre adresse IP de la liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="554b4-129">Use the [Microsoft 365 delist portal](https://sender.office.com) to submit a request to have your IP removed from the blocked sender's list.</span></span>

- <span data-ttu-id="554b4-130">Lisez les [forums de la communauté Microsoft](https://community.office365.com/f/).</span><span class="sxs-lookup"><span data-stu-id="554b4-130">Read the [Microsoft community forums](https://community.office365.com/f/).</span></span>

- <span data-ttu-id="554b4-131">Contactez le client auquel vous essayez d’envoyer un courrier électronique à l’aide d’une autre méthode et demandez-lui de contacter le support Microsoft et d’ouvrir un ticket de support en votre nom.</span><span class="sxs-lookup"><span data-stu-id="554b4-131">Contact the customer you're trying to email using another method and ask them to contact Microsoft Support and open a support ticket on your behalf.</span></span> <span data-ttu-id="554b4-132">Dans certains cas, pour des raisons juridiques, le support Microsoft doit communiquer directement avec l'expéditeur qui possède l'espace IP qui est bloqué.</span><span class="sxs-lookup"><span data-stu-id="554b4-132">In some cases, for legal reasons, Microsoft Support must communicate directly with the sender who owns the IP space that is being blocked.</span></span> <span data-ttu-id="554b4-133">Toutefois, les personnes qui ne sont pas des clients ne peuvent généralement pas demander de tickets d'assistance.</span><span class="sxs-lookup"><span data-stu-id="554b4-133">However, non-customers typically can't open support tickets.</span></span>

  <span data-ttu-id="554b4-134">Pour plus d'informations sur le support technique de Microsoft pour Office 365, voir [Prise en charge](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/support).</span><span class="sxs-lookup"><span data-stu-id="554b4-134">For more information about Microsoft Technical support for Office 365, see [Support](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/support).</span></span>

## <a name="anti-spam-ip-delist-portal"></a><span data-ttu-id="554b4-135">Portail d’adresses IP de blocage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="554b4-135">Anti-Spam IP Delist Portal</span></span>

<span data-ttu-id="554b4-136">Il s’agit d’un portail libre-service que vous pouvez utiliser pour vous supprimer de la liste des expéditeurs bloqués Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="554b4-136">This is a self-service portal you can use to remove yourself from the Microsoft 365 blocked senders list.</span></span> <span data-ttu-id="554b4-137">Utilisez ce portail si vous recevez un message d’erreur lorsque vous essayez d’envoyer un message électronique à un destinataire dont l’adresse de messagerie est dans Microsoft 365 et que vous ne pensez pas être.</span><span class="sxs-lookup"><span data-stu-id="554b4-137">Use this portal if you are you getting an error message when you try to send an email to a recipient whose email address is in Microsoft 365 and you don't think you should be.</span></span> <span data-ttu-id="554b4-138">Pour plus d'informations, voir [Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span><span class="sxs-lookup"><span data-stu-id="554b4-138">For more information, see [Use the delist portal to remove yourself from the blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>

## <a name="abuse-and-spam-reporting-for-junk-email-originating-from-exchange-online"></a><span data-ttu-id="554b4-139">Création de rapport de courrier indésirable et de mauvaise utilisation pour le courrier indésirable provenant d'Exchange Online</span><span class="sxs-lookup"><span data-stu-id="554b4-139">Abuse and spam reporting for junk email originating from Exchange Online</span></span>

<span data-ttu-id="554b4-140">Parfois, Microsoft365 est utilisé par des tiers pour envoyer des courriers indésirables, en violation de nos conditions d’utilisation et de notre stratégie.</span><span class="sxs-lookup"><span data-stu-id="554b4-140">Sometimes Microsoft365 is used by third parties to send junk email, in violation of our terms of use and policy.</span></span> <span data-ttu-id="554b4-141">Si vous recevez un courrier indésirable d’Office 365, vous pouvez signaler ces messages à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="554b4-141">If you receive any junk email from Office 365, you can report these messages to Microsoft.</span></span> <span data-ttu-id="554b4-142">Pour obtenir des instructions, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="554b4-142">For instructions, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>
