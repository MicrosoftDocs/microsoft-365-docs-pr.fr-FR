---
title: FAQ sur la protection contre l’usurpation d’identité
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: troubleshooting
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs peuvent consulter les questions fréquemment posées et leurs réponses sur la protection contre l’usurpation d’adresse dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: a5843ee7f791fbc2c37914194b153fdd05866d0a
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51065537"
---
# <a name="anti-spoofing-protection-faq"></a><span data-ttu-id="dd6dd-103">FAQ sur la protection contre l’usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="dd6dd-103">Anti-spoofing protection FAQ</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="dd6dd-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="dd6dd-104">**Applies to**</span></span>
- [<span data-ttu-id="dd6dd-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="dd6dd-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="dd6dd-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="dd6dd-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="dd6dd-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dd6dd-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="dd6dd-108">Cet article fournit des questions fréquemment posées et des réponses sur la protection contre l’usurpation d’adresses pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou les organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-108">This article provides frequently asked questions and answers about anti-spoofing protection for Microsoft 365 organizations with mailboxes in Exchange Online, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span>

<span data-ttu-id="dd6dd-109">Pour obtenir des questions et des réponses sur la protection anti-courrier indésirable, consultez la faq sur la [protection anti-courrier indésirable.](anti-spam-protection-faq.md)</span><span class="sxs-lookup"><span data-stu-id="dd6dd-109">For questions and answers about anti-spam protection, see [Anti-spam protection FAQ](anti-spam-protection-faq.md).</span></span>

<span data-ttu-id="dd6dd-110">Pour obtenir des questions et des réponses sur la protection anti-programme malveillant, consultez la faq sur la [protection anti-programme malveillant.](anti-malware-protection-faq-eop.md)</span><span class="sxs-lookup"><span data-stu-id="dd6dd-110">For questions and answers about anti-malware protection, see [Anti-malware protection FAQ](anti-malware-protection-faq-eop.md)</span></span>

## <a name="why-did-microsoft-choose-to-junk-unauthenticated-inbound-email"></a><span data-ttu-id="dd6dd-111">Pourquoi Microsoft a-t-il choisi de courrier indésirable entrant non authentifié ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-111">Why did Microsoft choose to junk unauthenticated inbound email?</span></span>

<span data-ttu-id="dd6dd-112">Microsoft estime que le risque de continuer à autoriser les messages entrants non authentifiés est plus élevé que le risque de perdre des messages entrants légitimes.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-112">Microsoft believes that the risk of continuing to allow unauthenticated inbound email is higher than the risk of losing legitimate inbound email.</span></span>

## <a name="does-junking-unauthenticated-inbound-email-cause-legitimate-email-to-be-marked-as-spam"></a><span data-ttu-id="dd6dd-113">Le courrier indésirable entrant non authentifié entraîne-t-il la marque du courrier légitime comme courrier indésirable ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-113">Does junking unauthenticated inbound email cause legitimate email to be marked as spam?</span></span>

<span data-ttu-id="dd6dd-114">Lorsque Microsoft a activé cette fonctionnalité en 2018, certains faux positifs se sont produits (les messages de qualité ont été marqués comme faux).</span><span class="sxs-lookup"><span data-stu-id="dd6dd-114">When Microsoft enabled this feature in 2018, some false positives happened (good messages were marked as bad).</span></span> <span data-ttu-id="dd6dd-115">Toutefois, au fil du temps, les expéditeurs se sont ajustés aux exigences.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-115">However, over time, senders adjusted to the requirements.</span></span> <span data-ttu-id="dd6dd-116">Le nombre de messages qui ont été identifiés comme usurpés est devenu négligeable pour la plupart des chemins d’accès aux e-mails.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-116">The number of messages that were misidentified as spoofed became negligible for most email paths.</span></span>

<span data-ttu-id="dd6dd-117">Microsoft lui-même a d’abord adopté les nouvelles exigences d’authentification du courrier électronique plusieurs semaines avant de le déployer pour les clients.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-117">Microsoft itself first adopted the new email authentication requirements several weeks before deploying it to customers.</span></span> <span data-ttu-id="dd6dd-118">S’il y a eu des perturbations au début, elles ont progressivement diminué.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-118">While there was disruption at first, it gradually declined.</span></span>

## <a name="is-spoof-intelligence-available-to-microsoft-365-customers-without-defender-for-office-365"></a><span data-ttu-id="dd6dd-119">La veille contre l’usurpation d’informations est-elle disponible pour les clients Microsoft 365 sans Defender pour Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-119">Is spoof intelligence available to Microsoft 365 customers without Defender for Office 365?</span></span>

<span data-ttu-id="dd6dd-120">Oui.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-120">Yes.</span></span> <span data-ttu-id="dd6dd-121">Depuis octobre 2018, la veille contre l’usurpation d’adresse est disponible pour toutes les organisations ayant des boîtes aux lettres dans Exchange Online et les organisations EOP autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-121">As of October 2018, spoof intelligence is available to all organizations with mailboxes in Exchange Online, and standalone EOP organizations without Exchange Online mailboxes.</span></span>

## <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a><span data-ttu-id="dd6dd-122">Comment signaler des messages comme étant ou n’étant pas du courrier indésirable à Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-122">How can I report spam or non-spam messages back to Microsoft?</span></span>

<span data-ttu-id="dd6dd-123">Voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="dd6dd-123">See [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="im-an-admin-and-i-dont-know-all-of-sources-for-messages-in-my-email-domain"></a><span data-ttu-id="dd6dd-124">Je suis un administrateur et je ne sais pas toutes les sources de messages dans mon domaine de messagerie !</span><span class="sxs-lookup"><span data-stu-id="dd6dd-124">I'm an admin and I don't know all of sources for messages in my email domain!</span></span>

<span data-ttu-id="dd6dd-125">See [You don’t know all sources for your email](email-validation-and-authentication.md#you-dont-know-all-sources-for-your-email).</span><span class="sxs-lookup"><span data-stu-id="dd6dd-125">See [You don't know all sources for your email](email-validation-and-authentication.md#you-dont-know-all-sources-for-your-email).</span></span>

## <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization"></a><span data-ttu-id="dd6dd-126">Que se passe-t-il si je désactive la protection contre l’usurpation d’accès pour mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-126">What happens if I disable anti-spoofing protection for my organization?</span></span>

<span data-ttu-id="dd6dd-127">Nous vous déconseillons de désactiver la protection contre l’usurpation d’usurpation d’accès.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-127">We do not recommend disabling anti-spoofing protection.</span></span> <span data-ttu-id="dd6dd-128">La désactivation de la protection permettra de remettre davantage de messages de hameçonnage et de courrier indésirable dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-128">Disabling the protection will allow more phishing and spam messages to be delivered in your organization.</span></span> <span data-ttu-id="dd6dd-129">Tout le hameçonnage n’est pas une usurpation d’informations, et tous les messages usurpés ne seront pas manqués.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-129">Not all phishing is spoofing, and not all spoofed messages will be missed.</span></span> <span data-ttu-id="dd6dd-130">Toutefois, votre risque sera plus élevé.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-130">However, your risk will be higher.</span></span>

<span data-ttu-id="dd6dd-131">À présent que le filtrage amélioré pour les [connecteurs](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) est disponible, nous vous déconseillons de la mettre hors service de protection contre l’usurpation d’adresse lorsque votre courrier électronique est acheminé via un autre service avant EOP.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-131">Now that [Enhanced Filtering for Connectors](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) is available, we no longer recommended turning off anti-spoofing protection when your email is routed through another service before EOP.</span></span>

## <a name="does-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a><span data-ttu-id="dd6dd-132">La protection contre l’usurpation d’usurpation signifie-t-elle que je suis protégé contre tout hameçonnage ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-132">Does anti-spoofing protection mean I will be protected from all phishing?</span></span>

<span data-ttu-id="dd6dd-133">Malheureusement, non.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-133">Unfortunately, no.</span></span> <span data-ttu-id="dd6dd-134">Les attaquants s’adaptent pour utiliser d’autres techniques (par exemple, les comptes compromis ou les comptes dans les services de messagerie gratuits).</span><span class="sxs-lookup"><span data-stu-id="dd6dd-134">Attackers will adapt to use other techniques (for example, compromised accounts or accounts in free email services).</span></span> <span data-ttu-id="dd6dd-135">Toutefois, la protection anti-hameçonnage fonctionne beaucoup mieux pour détecter ces autres types de méthodes de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-135">However, anti-phishing protection works much better to detect these other types of phishing methods.</span></span> <span data-ttu-id="dd6dd-136">Les couches de protection dans EOP sont conçues pour fonctionner ensemble et s’appuyer les unes sur les autres.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-136">The protection layers in EOP are designed work together and build on top of each other.</span></span>

## <a name="do-other-large-email-services-block-unauthenticated-inbound-email"></a><span data-ttu-id="dd6dd-137">D’autres services de messagerie de grande taille bloquent-ils les messages entrants non authentifiés ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-137">Do other large email services block unauthenticated inbound email?</span></span>

<span data-ttu-id="dd6dd-138">Presque tous les grands services de messagerie implémentent des vérifications SPF, DKIM et DMARC traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-138">Nearly all large email services implement traditional SPF, DKIM, and DMARC checks.</span></span> <span data-ttu-id="dd6dd-139">Certains services ont d’autres contrôles plus stricts, mais peu vont jusqu’à EOP pour bloquer les messages électroniques non authentifiés et les traiter comme des messages usurpés.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-139">Some services have other, more strict checks, but few go as far as EOP to block unauthenticated email and treat them as spoofed messages.</span></span> <span data-ttu-id="dd6dd-140">Toutefois, le secteur prend davantage en compte les problèmes de courrier électronique non authentifié, en particulier en raison du problème de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-140">However, the industry is becoming more aware about issues with unauthenticated email, particularly because of the problem of phishing.</span></span>

## <a name="do-i-still-need-to-enable-the-advanced-spam-filter-setting-spf-record-hard-fail-_markasspamspfrecordhardfail_-if-i-enable-anti-spoofing"></a><span data-ttu-id="dd6dd-141">Dois-je toujours activer le paramètre Filtre avancé du courrier indésirable « Enregistrement SPF : échec en dur » (_MarkAsSpamSpfRecordHardFail_) si j’active la détection d’usurpation d’adresses ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-141">Do I still need to enable the Advanced Spam Filter setting "SPF record: hard fail" (_MarkAsSpamSpfRecordHardFail_) if I enable anti-spoofing?</span></span>

<span data-ttu-id="dd6dd-142">Non.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-142">No.</span></span> <span data-ttu-id="dd6dd-143">Ce paramètre ASF n’est plus requis.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-143">This ASF setting is no longer required.</span></span> <span data-ttu-id="dd6dd-144">La protection contre l’usurpation d’usurpation tient compte à la fois des pannes de SPF et d’un ensemble de critères beaucoup plus large.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-144">Anti-spoofing protection considers both SPF hard fails and a much wider set of criteria.</span></span> <span data-ttu-id="dd6dd-145">Si vous avez activé la détection d’usurpation d’identité et l’option **Enregistrement SPF : échec sévère** (_MarkAsSpamSpfRecordHardFail_), vous obtiendrez probablement davantage de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-145">If you have anti-spoofing enabled and the **SPF record: hard fail** (_MarkAsSpamSpfRecordHardFail_) turned on, you will probably get more false positives.</span></span>

<span data-ttu-id="dd6dd-146">Nous vous recommandons de désactiver cette fonctionnalité, car elle n’offre pratiquement aucun avantage supplémentaire pour la détection du courrier indésirable ou du hameçonnage, et générerait à la place principalement des faux positifs.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-146">We recommend that you disable this feature as it provides almost no additional benefit for detecting spam or phishing message, and would instead generate mostly false positives.</span></span> <span data-ttu-id="dd6dd-147">Pour plus d’informations, consultez les paramètres de filtrage avancé du courrier indésirable [(ASF) dans EOP.](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="dd6dd-147">For more information, see [Advanced Spam Filter (ASF) settings in EOP](advanced-spam-filtering-asf-options.md).</span></span>

## <a name="does-sender-rewriting-scheme-help-fix-forwarded-email"></a><span data-ttu-id="dd6dd-148">Le modèle de réécriture des expéditeurs aide-t-il à corriger le courrier électronique transmis ?</span><span class="sxs-lookup"><span data-stu-id="dd6dd-148">Does Sender Rewriting Scheme help fix forwarded email?</span></span>

<span data-ttu-id="dd6dd-149">Schéma de réécriture de l’expéditeur ne résout que partiellement le problème du courrier transféré.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-149">SRS only partially fixes the problem of forwarded email.</span></span> <span data-ttu-id="dd6dd-150">La réécriture du message SMTP **MAIL FROM**, SRS permet de s’assurer que le message transmis passe SPF à la destination suivante.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-150">By rewriting the SMTP **MAIL FROM**, SRS can ensure that the forwarded message passes SPF at the next destination.</span></span> <span data-ttu-id="dd6dd-151">Toutefois, étant donné que la prévention  de l’usurpation d’adresse est basée sur l’adresse De en combinaison avec le domaine de signature **MAIL FROM** ou DKIM (ou d’autres signaux), il ne suffit pas d’empêcher le courrier électronique transmis par SRS d’être marqué comme usurpé.</span><span class="sxs-lookup"><span data-stu-id="dd6dd-151">However, because anti-spoofing is based upon the **From** address in combination with the **MAIL FROM** or DKIM-signing domain (or other signals), it's not enough to prevent SRS forwarded email from being marked as spoofed.</span></span>