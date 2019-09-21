---
title: Expéditeur non vérifié
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/11/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l’expéditeur est bien ce qu’il dit, et marquez les messages suspects comme courrier indésirable.
ms.openlocfilehash: a20dbe070d17499eb1db52a957666d509086bcb8
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079584"
---
# <a name="unverified-sender"></a><span data-ttu-id="7aefb-103">Expéditeur non vérifié</span><span class="sxs-lookup"><span data-stu-id="7aefb-103">Unverified Sender</span></span>

> [!NOTE] 
> <span data-ttu-id="7aefb-104">Ces mises à jour s’exécutent désormais et peuvent ne pas encore être disponibles pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7aefb-104">These updates are rolling out now, and might not be available yet for all users.</span></span>

<span data-ttu-id="7aefb-105">Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l’expéditeur est bien ce qu’il dit, et marquez les messages suspects comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7aefb-105">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7aefb-106">Lorsqu’un message est marqué comme frauduleux de hameçonnage, Outlook.com et Outlook sur le Web affichent un avertissement en haut de la page, mais vous pouvez toujours ouvrir les liens figurant dans le message.</span><span class="sxs-lookup"><span data-stu-id="7aefb-106">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="7aefb-107">Comment puis-je identifier un message suspect dans ma boîte de réception ?</span><span class="sxs-lookup"><span data-stu-id="7aefb-107">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="7aefb-108">Outlook.com et Outlook sur le Web affichent des indicateurs lorsque l’expéditeur d’un message ne peut pas être identifié ou que son identité est différente de ce que vous voyez dans l’adresse de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7aefb-108">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="7aefb-109">Comment gérer les messages qui reçoivent le traitement de l’expéditeur non vérifié</span><span class="sxs-lookup"><span data-stu-id="7aefb-109">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="7aefb-110">Si vous êtes un client Office 365, vous pouvez gérer cette fonctionnalité via le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="7aefb-110">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="7aefb-111">Dans le centre de conformité Office 365 Security &, les administrateurs globaux ou de sécurité peuvent activer ou désactiver la fonctionnalité via la protection contre l’usurpation d’identité dans le cadre de la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="7aefb-111">In the Office 365 Security & Compliance Center, global or security administrators can turn the feature on or off, through anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="7aefb-112">En outre, elle peut être gérée via la cmdlet « Set-Antiphishpolicy permet ».</span><span class="sxs-lookup"><span data-stu-id="7aefb-112">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="7aefb-113">Pour plus d’informations, consultez la rubrique [anti-phishing protection in Office 365](anti-phishing-protection.md) et [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishpolicy?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="7aefb-113">For more details, see [Anti-phishing protection in Office 365](anti-phishing-protection.md) and [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishpolicy?view=exchange-ps).</span></span>

    ![Modification des expéditeurs non authentifiés dans l’interface graphique.](../media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="7aefb-115">Si un administrateur a identifié un faux positif et qu’un expéditeur ne doit pas recevoir le traitement de l’expéditeur non vérifié, il peut effectuer l’une des actions suivantes pour ajouter l’expéditeur à la liste des usurpations d’identité usurpée :</span><span class="sxs-lookup"><span data-stu-id="7aefb-115">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="7aefb-116">Ajoutez la paire de domaines par le biais de la vue d’aide à la décision.</span><span class="sxs-lookup"><span data-stu-id="7aefb-116">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="7aefb-117">Pour plus d’informations, voir procédure pas à pas : usurpation d’information</span><span class="sxs-lookup"><span data-stu-id="7aefb-117">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="7aefb-118">Ajoutez la paire de domaines via l’applet de commande PhishFilterPolicy.</span><span class="sxs-lookup"><span data-stu-id="7aefb-118">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="7aefb-119">Pour plus d’informations, voir Set-PhishFilterPolicy et protection contre la falsification dans Office 365</span><span class="sxs-lookup"><span data-stu-id="7aefb-119">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="7aefb-120">En outre, nous n’appliquons pas le traitement de l’expéditeur non vérifié s’il a été remis à la boîte de réception via une liste verte d’administration, y compris les règles de transport de messagerie (ETR), la liste des domaines approuvés (stratégie anti-spam), la liste des expéditeurs approuvés ou un utilisateur a défini cet utilisateur comme « expéditeur approuvé » dans son utilitaire.</span><span class="sxs-lookup"><span data-stu-id="7aefb-120">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="7aefb-121">Un «  ? » apparaît dans l’image de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="7aefb-121">You see a '?' in the sender image</span></span>

<span data-ttu-id="7aefb-122">Lorsque Outlook.com et Outlook sur le Web ne peuvent pas vérifier l’identité de l’expéditeur à l’aide des techniques d’authentification de messagerie, ils affichent un «  ? » dans la photo de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7aefb-122">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![Le message n’a pas passé la vérification](../media/message-did-not-pass-verification.jpg)

<span data-ttu-id="7aefb-124">Les messages qui ne parvient pas à s’authentifier ne sont pas tous malveillants.</span><span class="sxs-lookup"><span data-stu-id="7aefb-124">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="7aefb-125">Toutefois, vous devez être prudent quant à l’interaction avec les messages qui ne sont pas authentifiés si vous ne reconnaissez pas l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7aefb-125">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="7aefb-126">Ou, si vous reconnaissez un expéditeur qui ne possède pas de «  ? » normalement dans l’image de l’expéditeur, mais que vous le voyez soudainement, cela peut être un signe que l’expéditeur est usurpé.</span><span class="sxs-lookup"><span data-stu-id="7aefb-126">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7aefb-127">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="7aefb-127">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="7aefb-128">Quels critères les Outlook.com et Outlook sur le Web utilisent-ils pour ajouter les propriétés «  ? » et « via » ?</span><span class="sxs-lookup"><span data-stu-id="7aefb-128">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="7aefb-129">Pour le «  ? » de l’image de l’expéditeur : Outlook.com requiert que le message passe l’authentification SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="7aefb-129">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="7aefb-130">Pour plus d’informations, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md) et l' [utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="7aefb-130">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="7aefb-131">Pour la balise via : si le domaine de l’adresse de l’expéditeur est différent du domaine dans la signature DKIM ou SMTP MAIL FROM, Outlook.com affiche le domaine dans l’un de ces deux champs (en préférant la signature DKIM).</span><span class="sxs-lookup"><span data-stu-id="7aefb-131">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="how-do-i-remove-the-"></a><span data-ttu-id="7aefb-132">Comment supprimer le «  ? » ?</span><span class="sxs-lookup"><span data-stu-id="7aefb-132">How do I remove the '?'</span></span>

<span data-ttu-id="7aefb-133">Pour le «  ? » de l’image de l’expéditeur : en tant qu’expéditeur, vous devez authentifier votre message avec SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="7aefb-133">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="7aefb-134">Pour la balise via : en tant qu’expéditeur, vous devez vous assurer que le domaine dans la signature DKIM ou SMTP MAIL FROM est le même que le domaine de l’adresse de provenance ou qu’il s’agit d’un sous-domaine de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7aefb-134">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="7aefb-135">Est-ce que Outlook.com et Outlook sur le Web s’affichent pour chaque message qui ne passe pas l’authentification ?</span><span class="sxs-lookup"><span data-stu-id="7aefb-135">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="7aefb-136">Pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="7aefb-136">Not necessarily.</span></span> <span data-ttu-id="7aefb-137">Outlook.com et Outlook sur le Web peuvent avoir d’autres propriétés dans le message pour authentifier l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7aefb-137">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aefb-138">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="7aefb-138">Related topics</span></span>

[<span data-ttu-id="7aefb-139">Protéger votre compte de messagerie Outlook.com</span><span class="sxs-lookup"><span data-stu-id="7aefb-139">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="7aefb-140">Gérer les abus, le hameçonnage ou l’usurpation d’identité dans Outlook.com</span><span class="sxs-lookup"><span data-stu-id="7aefb-140">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="7aefb-141">Filtrage du courrier indésirable et du courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7aefb-141">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
