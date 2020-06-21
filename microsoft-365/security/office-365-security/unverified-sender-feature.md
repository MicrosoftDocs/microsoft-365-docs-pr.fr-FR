---
title: Expéditeur non vérifié
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Cet article vous guidera, comment empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web.
ms.openlocfilehash: ed317f5673aa37b91e8c5092eb127b8df6be944e
ms.sourcegitcommit: 2acd9ec5e9d150389975e854c7883efc186a9432
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2020
ms.locfileid: "44754831"
---
# <a name="unverified-sender"></a><span data-ttu-id="634b2-103">Expéditeur non vérifié</span><span class="sxs-lookup"><span data-stu-id="634b2-103">Unverified Sender</span></span>

> [!NOTE]
> <span data-ttu-id="634b2-104">Ces mises à jour s’exécutent désormais et peuvent ne pas être disponibles pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="634b2-104">These updates are rolling out now, and might not be available for all users.</span></span> <span data-ttu-id="634b2-105">Cette fonctionnalité est prise en charge pour les utilisateurs d’Enterprise Outlook.com et d’entreprise Outlook Win32.</span><span class="sxs-lookup"><span data-stu-id="634b2-105">This feature is supported for Enterprise Outlook.com and Enterprise Outlook Win32 desktop users.</span></span> <span data-ttu-id="634b2-106">Il n’est pas disponible actuellement pour les utilisateurs d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="634b2-106">It is not currently available for consumer Office 365 users.</span></span>

<span data-ttu-id="634b2-107">Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Office 365 vérifie que les expéditeurs sont bien ceux qu’ils disent être et marquent les messages suspects comme du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="634b2-107">To prevent phishing messages from reaching your mailbox, Office 365 verifies that the senders are who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="634b2-108">Lorsqu’un message est marqué comme une escroquerie de type hameçonnage, Outlook affiche un avertissement en haut de la page, mais tous les liens dans le message peuvent toujours être ouverts.</span><span class="sxs-lookup"><span data-stu-id="634b2-108">When a message is marked as a phishing scam, Outlook displays a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="634b2-109">Comment puis-je identifier un message suspect dans ma boîte de réception ?</span><span class="sxs-lookup"><span data-stu-id="634b2-109">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="634b2-110">Outlook affiche des indicateurs lorsque l’expéditeur d’un message ne peut pas être identifié ou que son identité est différente de ce que vous voyez dans l’adresse de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="634b2-110">Outlook shows indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="634b2-111">Un «  ? » apparaît dans l’image de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="634b2-111">You see a '?' in the sender image</span></span>

<span data-ttu-id="634b2-112">Lorsque Office 365 ne peut pas vérifier l’identité de l’expéditeur à l’aide de techniques d’authentification de messagerie, un «  ? » s’affiche dans l’image de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="634b2-112">When Office 365 can't verify the identity of the sender using email authentication techniques, a '?' is displayed in the sender image.</span></span>

![Le message n’a pas passé la vérification](../../media/message-did-not-pass-verification.jpg)

<span data-ttu-id="634b2-114">Les messages qui ne parvient pas à s’authentifier ne sont pas tous malveillants.</span><span class="sxs-lookup"><span data-stu-id="634b2-114">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="634b2-115">Toutefois, vous devez être prudent quant à l’interaction avec les messages qui ne sont pas authentifiés si vous ne reconnaissez pas l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="634b2-115">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="634b2-116">Ou, si vous reconnaissez un expéditeur qui ne possède pas de «  ? » normalement dans l’image de l’expéditeur, mais que vous le voyez soudainement, cela peut être un signe que l’expéditeur est usurpé.</span><span class="sxs-lookup"><span data-stu-id="634b2-116">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="634b2-117">Comment gérer les messages qui reçoivent le traitement de l’expéditeur non vérifié</span><span class="sxs-lookup"><span data-stu-id="634b2-117">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="634b2-118">Si vous êtes un client Office 365, vous pouvez gérer cette fonctionnalité via le centre de sécurité & conformité d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="634b2-118">If you are an Office 365 customer you can manage this feature through the Office 365 Security & Compliance Center.</span></span>

- <span data-ttu-id="634b2-119">Dans le centre de sécurité & conformité, les administrateurs globaux ou de sécurité peuvent activer ou désactiver la fonctionnalité via la protection contre l’usurpation d’identité dans le cadre de la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="634b2-119">In the Security & Compliance Center, global or security administrators can turn the feature on or off, through anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="634b2-120">En outre, vous pouvez utiliser la cmdlet **Set-antiphishpolicy permet** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="634b2-120">Additionally, you can use the **Set-AntiPhishPolicy** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="634b2-121">Pour plus d’informations, consultez la rubrique [anti-hameçonnage protection dans Office 365](anti-phishing-protection.md) et [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/set-antiphishpolicy).</span><span class="sxs-lookup"><span data-stu-id="634b2-121">For details, see [Anti-phishing protection in Office 365](anti-phishing-protection.md) and [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/set-antiphishpolicy).</span></span>

    ![Modification des expéditeurs non authentifiés dans l’interface graphique.](../../media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="634b2-123">Si un administrateur a identifié un faux positif et qu’un expéditeur ne doit pas recevoir le traitement de l’expéditeur non vérifié, vous pouvez effectuer l’une des actions suivantes pour ajouter l’expéditeur à la liste des usurpations d’identité usurpée :</span><span class="sxs-lookup"><span data-stu-id="634b2-123">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment, one of the following actions can be taken to add the sender to the Spoof Intelligence spoof allow list:</span></span>

  - <span data-ttu-id="634b2-124">Ajoutez la paire de domaines par le biais de la vue d’aide à la décision.</span><span class="sxs-lookup"><span data-stu-id="634b2-124">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="634b2-125">Pour plus d’informations, consultez la [procédure pas à pas : usurpation](walkthrough-spoof-intelligence-insight.md)d’information.</span><span class="sxs-lookup"><span data-stu-id="634b2-125">For details, see [Walkthrough: spoof intelligence insight](walkthrough-spoof-intelligence-insight.md).</span></span>

  - <span data-ttu-id="634b2-126">Ajoutez la paire de domaines via la cmdlet **Set-PhishFilterPolicy** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="634b2-126">Add the domain pair through the **Set-PhishFilterPolicy** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="634b2-127">Pour plus d’informations, reportez-vous à [Set-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-phishfilterpolicy) et à [configurer les stratégies anti-hameçonnage et anti-hameçonnage d’Office 365 ATP](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="634b2-127">For details, see [Set-PhishFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/set-phishfilterpolicy) and [Set up Office 365 ATP anti-phishing and anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

<span data-ttu-id="634b2-128">De plus, nous n’appliquons pas le traitement de l’expéditeur non vérifié si le message a été remis à la boîte de réception via des règles de flux de messagerie (également appelées règles de transport) ou la liste des domaines approuvés (stratégies anti-courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="634b2-128">Additionally, we don't apply the unverified sender treatment if the message was delivered to the Inbox via mail flow rules (also known as transport rules) or the Safe Domain List (anti-spam policies).</span></span>

## <a name="how-to-manage-the-via-tag"></a><span data-ttu-id="634b2-129">Gestion de la balise « via »</span><span class="sxs-lookup"><span data-stu-id="634b2-129">How to manage the 'via' tag</span></span> 

<span data-ttu-id="634b2-130">Si vous êtes un client Office 365, vous pouvez gérer cette fonctionnalité via le centre de sécurité & conformité d’Office 365, de la même manière que vous gérez le traitement des expéditeurs non vérifiés.</span><span class="sxs-lookup"><span data-stu-id="634b2-130">If you are an Office 365 customer you can manage this feature through the Office 365 Security & Compliance center, the same way that you manage the unverified sender treatment.</span></span> <span data-ttu-id="634b2-131">Si vous ajoutez l’expéditeur à la liste d’usurpation d’identité usurpée, le traitement « via » ne sera pas appliqué.</span><span class="sxs-lookup"><span data-stu-id="634b2-131">If you add the sender to the Spoof Intelligence spoof allow list, the 'via' treatment will not be applied.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="634b2-132">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="634b2-132">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-win32-desktop-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="634b2-133">Quels sont les critères utilisés par Outlook.com et le bureau Win32 Outlook pour ajouter les propriétés «  ? » et « via » ?</span><span class="sxs-lookup"><span data-stu-id="634b2-133">What criteria does Outlook.com and Outlook Win32 desktop use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="634b2-134">Pour le «  ? » de l’image de l’expéditeur : Outlook.com nécessite que le message passe l’authentification SPF ou DKIM et reçoit une passe dMarc ou une authentification composite à partir de l’aide à l’usurpation d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="634b2-134">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication and receive either a dmarc pass, or a composite authentication pass from Office 365 Spoof Intelligence.</span></span> <span data-ttu-id="634b2-135">Pour plus d’informations, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md) et l' [utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="634b2-135">For details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="634b2-136">Pour la balise via : si le domaine de l’adresse de l’expéditeur est différent du domaine dans la signature DKIM ou SMTP MAIL FROM, Outlook.com affiche le domaine dans l’un de ces deux champs (en préférant la signature DKIM).</span><span class="sxs-lookup"><span data-stu-id="634b2-136">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="how-do-i-remove-the--without-utilizing-the-spoof-intelligence-spoof-allow-list"></a><span data-ttu-id="634b2-137">Comment supprimer le «  ? » sans utiliser la liste d’usurpation d’identité d’aide à la décision ?</span><span class="sxs-lookup"><span data-stu-id="634b2-137">How do I remove the '?' without utilizing the Spoof Intelligence spoof allow list?</span></span>

<span data-ttu-id="634b2-138">Pour le «  ? » de l’image de l’expéditeur : en tant qu’expéditeur, vous devez authentifier votre message avec SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="634b2-138">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="634b2-139">Pour la balise via : en tant qu’expéditeur, vous devez vous assurer que le domaine dans la signature DKIM ou SMTP MAIL FROM est le même que le domaine de l’adresse de provenance ou qu’il s’agit d’un sous-domaine de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="634b2-139">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="do-outlookcom-and-outlook-win32-desktop-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="634b2-140">Est-ce que Outlook.com et le bureau Win32 d’Outlook indiquent cela pour chaque message qui ne passe pas l’authentification ?</span><span class="sxs-lookup"><span data-stu-id="634b2-140">Do Outlook.com and Outlook Win32 desktop show this for every message that doesn't pass authentication?</span></span>

<span data-ttu-id="634b2-141">Pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="634b2-141">Not necessarily.</span></span> <span data-ttu-id="634b2-142">Office 365 peut avoir d’autres propriétés dans le message pour authentifier l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="634b2-142">Office 365 may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="634b2-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="634b2-143">Related topics</span></span>

[<span data-ttu-id="634b2-144">Protéger votre compte de messagerie Outlook.com</span><span class="sxs-lookup"><span data-stu-id="634b2-144">Help protect your Outlook.com email account</span></span>](https://support.microsoft.com/office/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="634b2-145">Comment traiter le hameçonnage dans Outlook.com</span><span class="sxs-lookup"><span data-stu-id="634b2-145">How to deal with phishing in Outlook.com</span></span>](https://support.microsoft.com/office/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="634b2-146">Filtrage du courrier indésirable et du courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="634b2-146">Filter junk email and spam in Outlook on the web</span></span>](https://support.microsoft.com/office/db786e79-54e2-40cc-904f-d89d57b7f41d)
