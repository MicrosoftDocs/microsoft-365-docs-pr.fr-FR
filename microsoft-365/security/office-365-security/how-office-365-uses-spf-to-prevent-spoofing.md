---
title: Comment Office 365 utilise SPF (Sender Policy Framework) pour éviter l’usurpation
f1.keywords:
- CSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/15/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
ms.collection:
- M365-security-compliance
description: "Résumé : Cet article décrit comment Office 365 utilise l'enregistrement TXT SPF (Sender Policy Framework) dans le système DNS pour s'assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine personnalisé. Cela s'applique aux messages sortants envoyés à partir d'Office 365. Les messages envoyés à partir d'Office 365 à un destinataire d'Office 365 passent toujours par SPF."
ms.openlocfilehash: f02219b19af592f9ad27ea963cb07a260c09327f
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599191"
---
# <a name="how-office-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a><span data-ttu-id="f170b-105">Comment Office 365 utilise SPF (Sender Policy Framework) pour éviter l’usurpation</span><span class="sxs-lookup"><span data-stu-id="f170b-105">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>

 <span data-ttu-id="f170b-p102">**Résumé :** Cet article décrit comment Office 365 utilise l'enregistrement TXT SPF (Sender Policy Framework) dans le système DNS pour s'assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine personnalisé. Cela s'applique aux messages sortants envoyés à partir d'Office 365. Les messages envoyés à partir d'Office 365 à un destinataire d'Office 365 passent toujours par SPF.</span><span class="sxs-lookup"><span data-stu-id="f170b-p102">**Summary:** This article describes how Office 365 uses the Sender Policy Framework (SPF) TXT record in DNS to ensure that destination email systems trust messages sent from your custom domain. This applies to outbound mail sent from Office 365. Messages sent from Office 365 to a recipient within Office 365 will always pass SPF.</span></span>

<span data-ttu-id="f170b-p103">Un enregistrement TXT SPF est un enregistrement DNS qui permet d'éviter l' usurpation et le hameçonnage en vérifiant le nom du domaine à partir duquel les messages électroniques sont envoyés. SPF valide l'origine des messages électroniques en vérifiant l'adresse IP de l'expéditeur par rapport à celle du prétendu propriétaire du domaine d'expédition.</span><span class="sxs-lookup"><span data-stu-id="f170b-p103">An SPF TXT record is a DNS record that helps prevent spoofing and phishing by verifying the domain name from which email messages are sent. SPF validates the origin of email messages by verifying the IP address of the sender against the alleged owner of the sending domain.</span></span>

> [!NOTE]
> <span data-ttu-id="f170b-p104">Les types d'enregistrement SPF ont été déconseillés par le groupe de travail IETF (Internet Engineering Task Force) en 2014. À la place, veillez à utiliser des enregistrements TXT dans le système DNS pour publier vos informations SPF. Le reste de cet article utilise le terme « enregistrement TXT SPF » pour plus de clarté.</span><span class="sxs-lookup"><span data-stu-id="f170b-p104">SPF record types were deprecated by the Internet Engineering Task Force (IETF) in 2014. Instead, ensure that you use TXT records in DNS to publish your SPF information. The rest of this article uses the term SPF TXT record for clarity.</span></span>

<span data-ttu-id="f170b-114">Les administrateurs de domaine publient des informations SPF dans les enregistrements TXT au sein du système DNS.</span><span class="sxs-lookup"><span data-stu-id="f170b-114">Domain administrators publish SPF information in TXT records in DNS.</span></span> <span data-ttu-id="f170b-115">Les informations SPF identifient les serveurs de messagerie sortants autorisés.</span><span class="sxs-lookup"><span data-stu-id="f170b-115">The SPF information identifies authorized outbound email servers.</span></span> <span data-ttu-id="f170b-116">Les systèmes de messagerie électronique de destination vérifient que les messages proviennent de serveurs de messagerie sortants autorisés.</span><span class="sxs-lookup"><span data-stu-id="f170b-116">Destination email systems verify that messages originate from authorized outbound email servers.</span></span> <span data-ttu-id="f170b-117">Si vous êtes déjà familiarisé avec SPF ou si vous disposez d’un déploiement simple et que vous avez simplement besoin de connaître les éléments à inclure dans votre enregistrement TXT SPF au sein du système DNS pour Office 365, vous pouvez accéder à [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="f170b-117">If you are already familiar with SPF, or you have a simple deployment, and just need to know what to include in your SPF TXT record in DNS for Office 365, you can go to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="f170b-118">Si vous ne disposez pas d’un déploiement entièrement hébergé par Office 365, ou que vous souhaitez obtenir plus d’informations sur le fonctionnement de SPF ou sur la façon de dépanner SPF pour Office 365, poursuivez votre lecture.</span><span class="sxs-lookup"><span data-stu-id="f170b-118">If you do not have a deployment that is fully-hosted in Office 365, or you want more information about how SPF works or how to troubleshoot SPF for Office 365, keep reading.</span></span>

> [!NOTE]
> <span data-ttu-id="f170b-119">Auparavant, vous deviez ajouter un autre enregistrement TXT SPF à votre domaine personnalisé si vous utilisiez également SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="f170b-119">Previously, you had to add a different SPF TXT record to your custom domain if you also used SharePoint Online.</span></span> <span data-ttu-id="f170b-120">Cela n'est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f170b-120">This is no longer required.</span></span> <span data-ttu-id="f170b-121">Ce changement doit réduire le risque que les messages de notification SharePoint Online terminent dans le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f170b-121">This change should reduce the risk of SharePoint Online notification messages ending up in the Junk Email folder.</span></span> <span data-ttu-id="f170b-122">Vous n’avez pas besoin d’apporter des modifications immédiatement, mais si vous recevez l’erreur « Trop de recherches », modifiez votre enregistrement TXT SPF comme décrit dans l’article [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="f170b-122">You do not need to make any changes immediately, but if you receive the "too many lookups" error, modify your SPF TXT record as described in [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span>

## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-office-365"></a><span data-ttu-id="f170b-123">Fonctionnement de SPF pour éviter l’usurpation et le hameçonnage dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-123">How SPF works to prevent spoofing and phishing in Office 365</span></span>
<span data-ttu-id="f170b-124"><a name="HowSPFWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-124"><a name="HowSPFWorks"> </a></span></span>

<span data-ttu-id="f170b-p107">SPF détermine si un expéditeur est autorisé à envoyer des messages au nom d'un domaine. Si l'expéditeur n'y est pas autorisé, autrement dit, si la vérification SPF du message électronique échoue sur le serveur de réception, la stratégie de courrier indésirable configurée sur ce serveur détermine l'action à entreprendre avec le message.</span><span class="sxs-lookup"><span data-stu-id="f170b-p107">SPF determines whether or not a sender is permitted to send on behalf of a domain. If the sender is not permitted to do so, that is, if the email fails the SPF check on the receiving server, the spam policy configured on that server determines what to do with the message.</span></span>

<span data-ttu-id="f170b-p108">Chaque enregistrement TXT SPF contient trois parties : la déclaration indiquant qu'il s'agit d'un enregistrement TXT SPF, les adresses IP qui sont autorisées à envoyer des messages à partir de votre domaine et les domaines externes pouvant envoyer des messages au nom de votre domaine, ainsi qu'une règle de mise en œuvre. Ces trois éléments sont obligatoires pour un enregistrement TXT SPF valide. Cet article décrit la façon dont vous devez créer votre enregistrement TXT SPF et fournit les meilleures pratiques pour utiliser ces services dans Office 365. Des liens vers des instructions sur l'utilisation de votre bureau d'enregistrement de domaine pour publier votre enregistrement dans DNS sont également disponibles.</span><span class="sxs-lookup"><span data-stu-id="f170b-p108">Each SPF TXT record contains three parts: the declaration that it is an SPF TXT record, the IP addresses that are allowed to send mail from your domain and the external domains that can send on your domain's behalf, and an enforcement rule. You need all three in a valid SPF TXT record. This article describes how you form your SPF TXT record and provides best practices for working with the services in Office 365. Links to instructions on working with your domain registrar to publish your record to DNS are also provided.</span></span>

### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a><span data-ttu-id="f170b-131">Concepts de base SPF : adresses IP autorisées à envoyer des messages à partir de votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="f170b-131">SPF basics: IP addresses allowed to send from your custom domain</span></span>
<span data-ttu-id="f170b-132"><a name="SPFBasicsIPaddresses"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-132"><a name="SPFBasicsIPaddresses"> </a></span></span>

<span data-ttu-id="f170b-133">Examinez la syntaxe de base pour une règle SPF :</span><span class="sxs-lookup"><span data-stu-id="f170b-133">Take a look at the basic syntax for an SPF rule:</span></span>

<span data-ttu-id="f170b-134">v=spf1 \<IP\> \<règle de mise en œuvre\></span><span class="sxs-lookup"><span data-stu-id="f170b-134">v=spf1 \<IP\> \<enforcement rule\></span></span>

<span data-ttu-id="f170b-135">Par exemple, supposons que la règle SPF suivante existe pour contoso.com :</span><span class="sxs-lookup"><span data-stu-id="f170b-135">For example, let's say the following SPF rule exists for contoso.com:</span></span>

<span data-ttu-id="f170b-136">v=spf1 \<adresse IP 1\> \<adresse IP 2\> \<adresse IP 3\> \<règle de mise en œuvre\></span><span class="sxs-lookup"><span data-stu-id="f170b-136">v=spf1 \<IP address #1\> \<IP address #2\> \<IP address #3\> \<enforcement rule\></span></span>

<span data-ttu-id="f170b-137">Dans cet exemple, la règle SPF demande au serveur de messagerie de réception d'accepter uniquement les messages provenant de ces adresses IP pour le domaine contoso.com :</span><span class="sxs-lookup"><span data-stu-id="f170b-137">In this example, the SPF rule instructs the receiving email server to only accept mail from these IP addresses for the domain contoso.com:</span></span>

- <span data-ttu-id="f170b-138">Adresse IP 1</span><span class="sxs-lookup"><span data-stu-id="f170b-138">IP address #1</span></span>

- <span data-ttu-id="f170b-139">Adresse IP 2</span><span class="sxs-lookup"><span data-stu-id="f170b-139">IP address #2</span></span>

- <span data-ttu-id="f170b-140">Adresse IP 3</span><span class="sxs-lookup"><span data-stu-id="f170b-140">IP address #3</span></span>

<span data-ttu-id="f170b-p109">Cette règle SPF indique au serveur de messagerie de réception que si un message provient de contoso.com, mais pas de l'une de ces trois adresses IP, le serveur de réception doit appliquer la règle de mise en œuvre au message. La règle de mise en œuvre est généralement l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f170b-p109">This SPF rule tells the receiving email server that if a message comes from contoso.com, but not from one of these three IP addresses, the receiving server should apply the enforcement rule to the message. The enforcement rule is usually one of these options:</span></span>

- <span data-ttu-id="f170b-p110">**Échec sévère.** Marquez « échec sévère » dans l'enveloppe du message, puis suivez la stratégie de courrier indésirable configurée du serveur de réception pour ce type de message.</span><span class="sxs-lookup"><span data-stu-id="f170b-p110">**Hard fail.** Mark the message with 'hard fail' in the message envelope and then follow the receiving server's configured spam policy for this type of message.</span></span>

- <span data-ttu-id="f170b-p111">**Échec partiel.** Marquez « échec partiel » dans l'enveloppe du message. En règle générale, les serveurs de messagerie sont configurés pour remettre ce type de message. La plupart des utilisateurs finaux ne voient pas cette marque.</span><span class="sxs-lookup"><span data-stu-id="f170b-p111">**Soft fail.** Mark the message with 'soft fail' in the message envelope. Typically, email servers are configured to deliver these messages anyway. Most end users do not see this mark.</span></span>

- <span data-ttu-id="f170b-p112">**Neutre.** Ne faites rien, autrement dit, ne marquez pas l'enveloppe du message. Cette marque est généralement réservée à des fins de test et est rarement utilisée.</span><span class="sxs-lookup"><span data-stu-id="f170b-p112">**Neutral.** Do nothing, that is, do not mark the message envelope. This is usually reserved for testing purposes and is rarely used.</span></span>

<span data-ttu-id="f170b-p113">Les exemples suivants montrent comment SPF fonctionne dans plusieurs situations différentes. Dans ces exemples, contoso.com est l’expéditeur et woodgrovebank.com est le destinataire.</span><span class="sxs-lookup"><span data-stu-id="f170b-p113">The following examples show how SPF works in different situations. In these examples, contoso.com is the sender and woodgrovebank.com is the receiver.</span></span>

### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a><span data-ttu-id="f170b-154">Exemple 1 : authentification de messagerie d’un message envoyé directement de l’expéditeur au destinataire</span><span class="sxs-lookup"><span data-stu-id="f170b-154">Example 1: Email authentication of a message sent directly from sender to receiver</span></span>
<span data-ttu-id="f170b-155"><a name="spfExample1"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-155"><a name="spfExample1"> </a></span></span>

<span data-ttu-id="f170b-156">SPF fonctionne de manière optimale lorsque le chemin entre l'expéditeur et le destinataire est direct, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f170b-156">SPF works best when the path from sender to receiver is direct, for example:</span></span>

![Diagramme illustrant comment SPF authentifie le courrier électronique lorsqu'il est envoyé directement d'un serveur à l'autre.](../media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)

<span data-ttu-id="f170b-158">Quand woodgrovebank.com reçoit le message, si l'adresse IP 1 se trouve dans l'enregistrement TXT SPF pour contoso.com, le message passe la vérification SPF et est authentifié.</span><span class="sxs-lookup"><span data-stu-id="f170b-158">When woodgrovebank.com receives the message, if IP address #1 is in the SPF TXT record for contoso.com, the message passes the SPF check and is authenticated.</span></span>

### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a><span data-ttu-id="f170b-159">Exemple 2 : l’adresse d’expéditeur falsifiée ne passe pas la vérification SPF</span><span class="sxs-lookup"><span data-stu-id="f170b-159">Example 2: Spoofed sender address fails the SPF check</span></span>
<span data-ttu-id="f170b-160"><a name="spfExample2"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-160"><a name="spfExample2"> </a></span></span>

<span data-ttu-id="f170b-161">Supposons qu'un auteur de hameçonnage trouve un moyen d'usurper contoso.com :</span><span class="sxs-lookup"><span data-stu-id="f170b-161">Suppose a phisher finds a way to spoof contoso.com:</span></span>

![Diagramme illustrant la façon dont SPF authentifie le courrier électronique envoyé à partir d'un serveur falsifié.](../media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)

<span data-ttu-id="f170b-163">Étant donné que l'adresse IP 12 n'est pas dans l'enregistrement TXT SPF de contoso.com, le message ne passe pas la vérification SPF et le destinataire peut choisir de le marquer comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f170b-163">Since IP address #12 is not in contoso.com's SPF TXT record, the message fails the SPF check and the receiver may choose to mark it as spam.</span></span>

### <a name="example-3-spf-and-forwarded-messages"></a><span data-ttu-id="f170b-164">Exemple 3 : messages transférés et SPF</span><span class="sxs-lookup"><span data-stu-id="f170b-164">Example 3: SPF and forwarded messages</span></span>
<span data-ttu-id="f170b-165"><a name="spfExample3"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-165"><a name="spfExample3"> </a></span></span>

<span data-ttu-id="f170b-p114">SPF présente un désavantage qui réside dans le fait qu'il ne fonctionne pas lorsqu'un message électronique a été transféré. Par exemple, supposons que l'utilisateur woodgrovebank.com a défini une règle de transfert pour envoyer tous les messages électroniques vers un compte outlook.com :</span><span class="sxs-lookup"><span data-stu-id="f170b-p114">One drawback of SPF is that it doesn't work when an email has been forwarded. For example, suppose the user at woodgrovebank.com has set up a forwarding rule to send all email to an outlook.com account:</span></span>

![Diagramme indiquant comment SPF ne peut pas authentifier le courrier électronique lorsque le message est transféré.](../media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)

<span data-ttu-id="f170b-p115">Le message passe d'abord la vérification SPF sur woodgrovebank.com mais il échoue lors de la vérification SPF sur outlook.com, car l'adresse IP 25 ne figure pas dans l'enregistrement TXT SPF de contoso.com. Outlook.com peut ensuite marquer le message comme courrier indésirable. Pour contourner ce problème, utilisez SPF avec d'autres méthodes d'authentification de courrier électronique, comme DKIM et DMARC.</span><span class="sxs-lookup"><span data-stu-id="f170b-p115">The message originally passes the SPF check at woodgrovebank.com but it fails the SPF check at outlook.com because IP #25 is not in contoso.com's SPF TXT record. Outlook.com might then mark the message as spam. To work around this problem, use SPF in conjunction with other email authentication methods such as DKIM and DMARC.</span></span>

### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a><span data-ttu-id="f170b-172">Concepts de base SPF : intégration de domaines tiers pouvant envoyer des messages au nom de votre domaine</span><span class="sxs-lookup"><span data-stu-id="f170b-172">SPF basics: Including third-party domains that can send mail on behalf of your domain</span></span>
<span data-ttu-id="f170b-173"><a name="SPFBasicsIncludes"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-173"><a name="SPFBasicsIncludes"> </a></span></span>

<span data-ttu-id="f170b-p116">En plus des adresses IP, vous pouvez également configurer votre enregistrement TXT SPF pour inclure des domaines en tant qu'expéditeurs. Ces domaines sont ajoutés à l'enregistrement TXT SPF comme des instructions « Include ». Par exemple, contoso.com souhaite peut-être inclure toutes les adresses IP des serveurs de messagerie à partir de contoso.net et de contoso.org qu'il possède également. Pour ce faire, contoso.com publie un enregistrement TXT SPF qui ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="f170b-p116">In addition to IP addresses, you can also configure your SPF TXT record to include domains as senders. These are added to the SPF TXT record as "include" statements. For example, contoso.com might want to include all of the IP addresses of the mail servers from contoso.net and contoso.org which it also owns. To do this, contoso.com publishes an SPF TXT record that looks like this:</span></span>

```text
v=spf1 include:contoso.net include:contoso.org -all
```

<span data-ttu-id="f170b-178">Lorsque le serveur de réception voit cet enregistrement dans le DNS, il effectue également une recherche DNS sur l’enregistrement TXT SPF pour contoso.net, puis sur contoso.org. S’il trouve une instruction include supplémentaire dans les enregistrements pour contoso.net ou contoso.org, il suit également ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="f170b-178">When the receiving server sees this record in DNS, it also performs a DNS lookup on the SPF TXT record for contoso.net and then for contoso.org. If it finds an additional include statement within the records for contoso.net or contoso.org, it will follow those too.</span></span> <span data-ttu-id="f170b-179">Afin d’empêcher le refus d’attaque de service, le nombre maximal de recherches DNS pour un seul message est de 10.</span><span class="sxs-lookup"><span data-stu-id="f170b-179">In order to help prevent denial of service attacks, the maximum number of DNS lookups for a single email message is 10.</span></span> <span data-ttu-id="f170b-180">Chaque instruction Include représente une recherche DNS supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f170b-180">Each include statement represents an additional DNS lookup.</span></span> <span data-ttu-id="f170b-181">Si un message dépasse la limite de 10, le message échoue lors de la vérification SPF.</span><span class="sxs-lookup"><span data-stu-id="f170b-181">If a message exceeds the 10 limit, the message fails SPF.</span></span> <span data-ttu-id="f170b-182">Une fois qu’un message atteint cette limite, en fonction de la configuration du serveur de réception, l’expéditeur peut recevoir un message indiquant que le message a été généré « trop de recherches » ou que le « nombre maximal de tronçons pour le message a été dépassé » (ce qui peut se produire lorsque le les recherches sont en boucle et dépasse le délai d’attente DNS.</span><span class="sxs-lookup"><span data-stu-id="f170b-182">Once a message reaches this limit, depending on the way the receiving server is configured, the sender may get a message that says the message generated "too many lookups" or that the "maximum hop count for the message has been exceeded" (which can happen when the lookups loop and surpass the DNS timeout).</span></span> <span data-ttu-id="f170b-183">Pour savoir comment éviter cette situation, voir [Résolution des problèmes : meilleures pratiques pour SPF dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span><span class="sxs-lookup"><span data-stu-id="f170b-183">For tips on how to avoid this, see [Troubleshooting: Best practices for SPF in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span></span>

## <a name="requirements-for-your-spf-txt-record-and-office-365"></a><span data-ttu-id="f170b-184">Configuration requise pour votre enregistrement TXT SPF et Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-184">Requirements for your SPF TXT record and Office 365</span></span>
<span data-ttu-id="f170b-185"><a name="SPFReqsinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-185"><a name="SPFReqsinO365"> </a></span></span>

<span data-ttu-id="f170b-p118">Si vous avez configuré la messagerie lors de la configuration d'Office 365, vous avez déjà créé un enregistrement TXT SPF qui identifie les serveurs de messagerie Microsoft en tant que source légitime de messagerie pour votre domaine. Cet enregistrement ressemble probablement à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="f170b-p118">If you set up mail when you set up Office 365, you already created an SPF TXT record that identifies the Microsoft messaging servers as a legitimate source of mail for your domain. This record probably looks like this:</span></span>

```text
v=spf1 include:spf.protection.outlook.com -all
```

<span data-ttu-id="f170b-188">Si vous êtes un client Office 365 entièrement hébergé, autrement dit, si vous n'avez aucun serveur de messagerie local qui envoie du courrier sortant, il s'agit du seul enregistrement TXT SPF que vous devez publier pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="f170b-188">If you're a fully-hosted Office 365 customer, that is, you have no on-premises mail servers that send outbound mail, this is the only SPF TXT record that you need to publish for Office 365.</span></span>

<span data-ttu-id="f170b-189">Si vous disposez d'un déploiement hybride (autrement dit, avec quelques boîtes aux lettres locales et d'autres hébergées dans Office 365), ou que vous êtes un client autonome Exchange Online Protection (EOP) (autrement dit, votre organisation utilise EOP pour protéger vos boîtes aux lettres locales), vous devez ajouter l'adresse IP sortante pour tous vos serveurs de messagerie Edge locaux à l'enregistrement TXT SPF dans DNS.</span><span class="sxs-lookup"><span data-stu-id="f170b-189">If you have a hybrid deployment (that is, you have some mailboxes on-premises and some hosted in Office 365), or if you're an Exchange Online Protection (EOP) standalone customer (that is, your organization uses EOP to protect your on-premises mailboxes), you should add the outbound IP address for each of your on-premises edge mail servers to the SPF TXT record in DNS.</span></span>

## <a name="form-your-spf-txt-record-for-office-365"></a><span data-ttu-id="f170b-190">Formuler votre enregistrement TXT SPF pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-190">Form your SPF TXT record for Office 365</span></span>
<span data-ttu-id="f170b-191"><a name="FormYourSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-191"><a name="FormYourSPF"> </a></span></span>

<span data-ttu-id="f170b-p119">Utilisez les informations de syntaxe de cet article afin de formuler l'enregistrement TXT SPF pour votre domaine personnalisé. Bien qu'il existe des options de syntaxe qui ne sont pas mentionnées ici, il s'agit des options les plus fréquemment utilisées. Une fois que vous avez formulé votre enregistrement, vous devez le mettre à jour auprès de votre bureau d'enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="f170b-p119">Use the syntax information in this article to form the SPF TXT record for your custom domain. Although there are other syntax options that are not mentioned here, these are the most commonly used options. Once you have formed your record, you need to update the record at your domain registrar.</span></span>

<span data-ttu-id="f170b-195">Pour plus d'informations sur les domaines que vous devez inclure pour Office 365, voir [Enregistrements DNS externes pour Office 365](https://docs.microsoft.com/office365/enterprise/external-domain-name-system-records).</span><span class="sxs-lookup"><span data-stu-id="f170b-195">For information about the domains you will need to include for Office 365, see [External DNS records required for SPF](https://docs.microsoft.com/office365/enterprise/external-domain-name-system-records).</span></span> <span data-ttu-id="f170b-196">Utilisez les [instructions pas à pas](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider#add-a-txt-record-for-spf-to-help-prevent-email-spam) pour mettre à jour les enregistrements SPF (TXT) dans votre bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="f170b-196">Use the [step-by-step instructions](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider#add-a-txt-record-for-spf-to-help-prevent-email-spam) for updating SPF (TXT) records for your domain registrar.</span></span>

### <a name="spf-txt-record-syntax-for-office-365"></a><span data-ttu-id="f170b-197">Syntaxe d’enregistrement TXT SPF pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-197">SPF TXT record syntax for Office 365</span></span>
<span data-ttu-id="f170b-198"><a name="SPFSyntaxO365"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-198"><a name="SPFSyntaxO365"> </a></span></span>

<span data-ttu-id="f170b-199">Un enregistrement TXT SPF standard pour Office 365 comporte la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f170b-199">A typical SPF TXT record for Office 365 has the following syntax:</span></span>

```text
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

<span data-ttu-id="f170b-200">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f170b-200">For example:</span></span>

```text
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

<span data-ttu-id="f170b-201">où :</span><span class="sxs-lookup"><span data-stu-id="f170b-201">where:</span></span>

- <span data-ttu-id="f170b-p121">**v=spf1** est obligatoire. Cet élément définit l'enregistrement TXT en tant qu'enregistrement TXT SPF.</span><span class="sxs-lookup"><span data-stu-id="f170b-p121">**v=spf1** is required. This defines the TXT record as an SPF TXT record.</span></span>

- <span data-ttu-id="f170b-p122">**IP4** indique que vous utilisez des adresses IP de version 4. **ip6** indique que vous utilisez des adresses IP de version 6. Si vous utilisez des adresses IP IPv6, remplacez **ip4** par **ip6** dans les exemples de cet article. Vous pouvez également spécifier des plages d'adresses IP à l'aide de la notation CIDR, par exemple **ip4:192.168.0.1/26**.</span><span class="sxs-lookup"><span data-stu-id="f170b-p122">**ip4** indicates that you are using IP version 4 addresses. **ip6** indicates that you are using IP version 6 addresses. If you are using IPv6 IP addresses, replace **ip4** with **ip6** in the examples in this article. You can also specify IP address ranges using CIDR notation, for example **ip4:192.168.0.1/26**.</span></span>

- <span data-ttu-id="f170b-p123">_IP address_ est l'adresse IP à ajouter à l'enregistrement TXT SPF. En règle générale, il s'agit de l'adresse IP du serveur de messagerie sortant pour votre organisation. Vous pouvez répertorier plusieurs serveurs de messagerie sortants. Pour plus d'informations, consultez la section [Exemple : enregistrement TXT SPF pour plusieurs serveurs de messagerie locaux sortants et Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365).</span><span class="sxs-lookup"><span data-stu-id="f170b-p123">_IP address_ is the IP address that you want to add to the SPF TXT record. Usually, this is the IP address of the outbound mail server for your organization. You can list multiple outbound mail servers. For more information, see [Example: SPF TXT record for multiple outbound on-premises mail servers and Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365).</span></span>

- <span data-ttu-id="f170b-p124">_domain name_ est le domaine que vous souhaitez ajouter en tant qu'expéditeur légitime. Pour obtenir la liste de noms de domaine que vous devez inclure pour Office 365, voir [Enregistrements DNS externes pour Office 365](https://docs.microsoft.com/office365/enterprise/external-domain-name-system-records).</span><span class="sxs-lookup"><span data-stu-id="f170b-p124">_domain name_ is the domain you want to add as a legitimate sender. For a list of domain names you should include for Office 365, see [External DNS records required for SPF](https://docs.microsoft.com/office365/enterprise/external-domain-name-system-records).</span></span>

- <span data-ttu-id="f170b-214">La règle de mise en œuvre est généralement l'une des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="f170b-214">Enforcement rule is usually one of the following:</span></span>

  - <span data-ttu-id="f170b-215">-all</span><span class="sxs-lookup"><span data-stu-id="f170b-215">-all</span></span>

    <span data-ttu-id="f170b-p125">Indique un échec sévère. Si vous connaissez toutes les adresses IP autorisées pour votre domaine, répertoriez-les dans l'enregistrement TXT SPF et utilisez le qualificateur -all (échec sévère). En outre, si vous utilisez uniquement SPF, c'est-à-dire que vous n'utilisez pas DMARC ou DKIM, vous devez utiliser le qualificateur -all. Nous vous recommandons de toujours utiliser ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="f170b-p125">Indicates hard fail. If you know all of the authorized IP addresses for your domain, list them in the SPF TXT record and use the -all (hard fail) qualifier. Also, if you are only using SPF, that is, you are not using DMARC or DKIM, you should use the -all qualifier. We recommend that you use always this qualifier.</span></span>

  - <span data-ttu-id="f170b-220">~all</span><span class="sxs-lookup"><span data-stu-id="f170b-220">~all</span></span>

    <span data-ttu-id="f170b-p126">Indique un échec partiel. Si vous n'êtes pas sûr de disposer de la liste complète des adresses IP, utilisez le qualificateur ~all (échec partiel). En outre, si vous utilisez DMARC avec p=quarantine ou p=reject, vous pouvez utiliser ~all. Dans le cas contraire, utilisez -all.</span><span class="sxs-lookup"><span data-stu-id="f170b-p126">Indicates soft fail. If you're not sure that you have the complete list of IP addresses, then you should use the ~all (soft fail) qualifier. Also, if you are using DMARC with p=quarantine or p=reject, then you can use ~all. Otherwise, use -all.</span></span>

  - <span data-ttu-id="f170b-225">?all</span><span class="sxs-lookup"><span data-stu-id="f170b-225">?all</span></span>

    <span data-ttu-id="f170b-p127">Indique un résultat neutre. Il est utilisé lors des essais SPF. Nous vous déconseillons d’utiliser ce qualificatif dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="f170b-p127">Indicates neutral. This is used when testing SPF. We do not recommend that you use this qualifier in your live deployment.</span></span>

### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-office-365"></a><span data-ttu-id="f170b-229">Exemple : enregistrement TXT SPF à utiliser quand tous vos messages sont envoyés par Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-229">Example: SPF TXT record to use when all of your mail is sent by Office 365</span></span>
<span data-ttu-id="f170b-230"><a name="ExampleSPFNoSP"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-230"><a name="ExampleSPFNoSP"> </a></span></span>

<span data-ttu-id="f170b-231">Si tous vos messages sont envoyés par Office 365, utilisez les indications suivantes dans votre enregistrement TXT SPF :</span><span class="sxs-lookup"><span data-stu-id="f170b-231">If all of your mail is sent by Office 365, use this in your SPF TXT record:</span></span>

```text
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-office-365"></a><span data-ttu-id="f170b-232">Exemple : enregistrement TXT SPF pour un scénario hybride avec un serveur Exchange local et Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-232">Example: SPF TXT record for a hybrid scenario with one on-premises Exchange Server and Office 365</span></span>
<span data-ttu-id="f170b-233"><a name="ExampleSPFHybridOneExchangeServer"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-233"><a name="ExampleSPFHybridOneExchangeServer"> </a></span></span>

<span data-ttu-id="f170b-234">Dans un environnement hybride, si l'adresse IP du serveur Exchange local est 192.168.0.1, afin de définir la règle de mise en œuvre SPF sur échec sévère, formez l'enregistrement TXT SPF comme suit :</span><span class="sxs-lookup"><span data-stu-id="f170b-234">In a hybrid environment, if the IP address of your on-premises Exchange Server is 192.168.0.1, in order to set the SPF enforcement rule to hard fail, form the SPF TXT record as follows:</span></span>

```text
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-office-365"></a><span data-ttu-id="f170b-235">Exemple : enregistrement TXT SPF pour plusieurs serveurs de messagerie locaux sortants et Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-235">Example: SPF TXT record for multiple outbound on-premises mail servers and Office 365</span></span>
<span data-ttu-id="f170b-236"><a name="ExampleSPFMultipleMailServerO365"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-236"><a name="ExampleSPFMultipleMailServerO365"> </a></span></span>

<span data-ttu-id="f170b-p128">Si vous avez plusieurs serveurs de messagerie sortants, ajoutez l'adresse IP de chaque serveur de messagerie dans l'enregistrement TXT SPF et séparez chaque adresse IP par un espace suivi par une instruction « ip4: ». Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f170b-p128">If you have multiple outbound mail servers, include the IP address for each mail server in the SPF TXT record and separate each IP address with a space followed by an "ip4:" statement. For example:</span></span>

```text
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-office-365"></a><span data-ttu-id="f170b-239">Étapes suivantes : configurer SPF pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-239">Next steps: Set up SPF for Office 365</span></span>
<span data-ttu-id="f170b-240"><a name="SPFNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-240"><a name="SPFNextSteps"> </a></span></span>

<span data-ttu-id="f170b-241">Une fois que vous avez formulé votre enregistrement TXT SPF, suivez la procédure décrite dans l’article [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) pour l’ajouter à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f170b-241">Once you have formulated your SPF TXT record, follow the steps in [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) to add it to your domain.</span></span>

<span data-ttu-id="f170b-p129">Bien que SPF soit conçu pour éviter l'usurpation, il existe des techniques d'usurpation contre lesquelles SPF ne peut pas vous protéger. Afin de vous protéger contre ces techniques, une fois que vous avez configuré SPF, vous devez également configurer DKIM et DMARC pour Office 365. Consultez [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md) pour commencer. Ensuite, consultez la rubrique [Utiliser DMARC pour valider les e-mails dans Office 365](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="f170b-p129">Although SPF is designed to help prevent spoofing, but there are spoofing techniques that SPF cannot protect against. In order to protect against these, once you have set up SPF, you should also configure DKIM and DMARC for Office 365. To get started, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span>

## <a name="troubleshooting-best-practices-for-spf-in-office-365"></a><span data-ttu-id="f170b-246">Résolution des problèmes : Meilleures pratiques pour SPF dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-246">Troubleshooting: Best practices for SPF in Office 365</span></span>
<span data-ttu-id="f170b-247"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-247"><a name="SPFTroubleshoot"> </a></span></span>

<span data-ttu-id="f170b-p130">Vous ne pouvez créer qu'un seul enregistrement TXT SPF pour votre domaine personnalisé. La création de plusieurs enregistrements entraîne une situation alternée et l'échec de SPF. Pour éviter cela, vous pouvez créer des enregistrements distincts pour chaque sous-domaine. Par exemple, créez un enregistrement pour contoso.com et un autre enregistrement pour bulkmail.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="f170b-p130">You can only create one SPF TXT record for your custom domain. Creating multiple records causes a round robin situation and SPF will fail. To avoid this, you can create separate records for each subdomain. For example, create one record for contoso.com and another record for bulkmail.contoso.com.</span></span>

<span data-ttu-id="f170b-p131">Si un message électronique provoque plus de 10 recherches DNS avant sa livraison, le serveur de messagerie de réception répond avec une erreur permanente, également appelée  _permerror_, et génère l'échec du message lors de la vérification SPF. Le serveur de réception peut également répondre avec une notification d'échec de remise qui contient une erreur semblable à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="f170b-p131">If an email message causes more than 10 DNS lookups before it is delivered, the receiving mail server will respond with a permanent error, also called a  _permerror_, and cause the message to fail the SPF check. The receiving server may also respond with a non-delivery report (NDR) that contains an error similar to these:</span></span>

- <span data-ttu-id="f170b-254">Le message a dépassé le nombre de sauts.</span><span class="sxs-lookup"><span data-stu-id="f170b-254">The message exceeded the hop count.</span></span>

- <span data-ttu-id="f170b-255">Le message a demandé trop de recherches.</span><span class="sxs-lookup"><span data-stu-id="f170b-255">The message required too many lookups.</span></span>

## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-office-365"></a><span data-ttu-id="f170b-256">Éviter l'erreur « Trop de recherches » lorsque vous utilisez des domaines tiers avec Office 365</span><span class="sxs-lookup"><span data-stu-id="f170b-256">Avoiding the "too many lookups" error when you use third-party domains with Office 365</span></span>
<span data-ttu-id="f170b-257"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-257"><a name="SPFTroubleshoot"> </a></span></span>

<span data-ttu-id="f170b-p132">Certains enregistrements TXT SPF pour les domaines tiers indiquent au serveur de réception d'effectuer un nombre élevé de recherches DNS. Par exemple, au moment de la rédaction, Salesforce.com contient 5 instructions Include dans son enregistrement :</span><span class="sxs-lookup"><span data-stu-id="f170b-p132">Some SPF TXT records for third-party domains direct the receiving server to perform a large number of DNS lookups. For example, at the time of this writing, Salesforce.com contains 5 include statements in its record:</span></span>

```text
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

<span data-ttu-id="f170b-p133">Pour éviter l'erreur, vous pouvez implémenter une stratégie selon laquelle toute personne envoyant des messages électroniques en bloc, par exemple, doit utiliser un sous-domaine spécialement à cette fin. Ensuite, définissez un autre enregistrement TXT SPF pour le sous-domaine comprenant la messagerie électronique en bloc.</span><span class="sxs-lookup"><span data-stu-id="f170b-p133">To avoid the error, you can implement a policy where anyone sending bulk email, for example, has to use a subdomain specifically for this purpose. You then define a different SPF TXT record for the subdomain that includes the bulk email.</span></span>

 <span data-ttu-id="f170b-p134">Dans certains cas, comme dans l'exemple salesforce.com, vous devez utiliser le domaine dans votre enregistrement TXT SPF, mais dans d'autres cas, le domaine tiers a peut-être déjà créé un sous-domaine pour votre utilisation. Par exemple, exacttarget.com a créé un sous-domaine que vous devez utiliser pour votre enregistrement TXT SPF :</span><span class="sxs-lookup"><span data-stu-id="f170b-p134">In some cases, like the salesforce.com example, you have to use the domain in your SPF TXT record, but in other cases, the third-party may have already created a subdomain for you to use for this purpose. For example, exacttarget.com has created a subdomain that you need to use for your SPF TXT record:</span></span>

```text
cust-spf.exacttarget.com
```

<span data-ttu-id="f170b-264">Lorsque vous incluez des domaines tiers dans votre enregistrement TXT SPF, vous devez vérifier auprès du tiers le domaine ou le sous-domaine à utiliser pour éviter d'atteindre la limite de 10 recherches.</span><span class="sxs-lookup"><span data-stu-id="f170b-264">When you include third-party domains in your SPF TXT record, you need to confirm with the third-party which domain or subdomain to use in order to avoid running into the 10 lookup limit.</span></span>

## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a><span data-ttu-id="f170b-265">Comment afficher votre enregistrement TXT SPF et déterminer le nombre de recherches nécessaires</span><span class="sxs-lookup"><span data-stu-id="f170b-265">How to view your current SPF TXT record and determine the number of lookups that it requires</span></span>
<span data-ttu-id="f170b-266"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-266"><a name="SPFTroubleshoot"> </a></span></span>

<span data-ttu-id="f170b-p135">Vous pouvez utiliser nslookup pour afficher vos enregistrements DNS, y compris votre enregistrement TXT SPF. Sinon, si vous préférez, il existe plusieurs outils gratuits en ligne que vous pouvez utiliser pour afficher le contenu de votre enregistrement TXT SPF. En consultant votre enregistrement TXT SPF et en suivant la chaîne d'instructions Include et de redirections, vous pouvez déterminer le nombre de recherches DNS dont l'enregistrement a besoin. Certains outils en ligne peuvent même compter et afficher ces recherches pour vous. Le fait d'assurer le suivi de cette donnée permettra d'éviter que les messages envoyés depuis votre organisation ne déclenchent une erreur permanente, appelée permerror, sur le serveur de réception.</span><span class="sxs-lookup"><span data-stu-id="f170b-p135">You can use nslookup to view your DNS records, including your SPF TXT record. Or, if you prefer, there are a number of free, online tools available that you can use to view the contents of your SPF TXT record. By looking at your SPF TXT record and following the chain of include statements and redirects, you can determine how many DNS lookups the record requires. Some online tools will even count and display these lookups for you. Keeping track of this number will help prevent messages sent from your organization from triggering a permanent error, called a permerror, from the receiving server.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="f170b-272">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="f170b-272">For more information</span></span>
<span data-ttu-id="f170b-273"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="f170b-273"><a name="SPFTroubleshoot"> </a></span></span>

<span data-ttu-id="f170b-274">Besoin d'aide pour ajouter l'enregistrement TXT SPF ?</span><span class="sxs-lookup"><span data-stu-id="f170b-274">Need help adding the SPF TXT record?</span></span> <span data-ttu-id="f170b-275">Lisez l’article [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider#add-a-txt-record-for-spf-to-help-prevent-email-spam) pour obtenir des informations détaillées sur l’utilisation de l’infrastructure des stratégies d’expéditeur avec votre domaine personnalisé dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="f170b-275">Read the article [Create DNS records at any DNS hosting provider for Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider#add-a-txt-record-for-spf-to-help-prevent-email-spam) for detailed information about usage of Sender Policy Framework with your custom domain in Office 365.</span></span> <span data-ttu-id="f170b-276">Les [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md) incluent la syntaxe et les champs d'en-tête utilisés par Office 365 pour les vérifications SPF.</span><span class="sxs-lookup"><span data-stu-id="f170b-276">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for SPF checks.</span></span>


