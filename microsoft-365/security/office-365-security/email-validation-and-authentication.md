---
title: Authentification de messagerie électronique dans Microsoft 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
- Strat_O365_IP
ms.custom: TopSMBIssues
localization_priority: Priority
description: Les administrateurs peuvent découvrir comment EOP utilise l’authentification de messagerie électronique (SPF, DKIM et DMARC) pour empêcher l’usurpation d’identité, le hameçonnage et les courriers indésirables.
ms.openlocfilehash: 1e4ad82dd1c57e089b36e39afde346c47043c546
ms.sourcegitcommit: eb905c5b4d7e71fc930a207357295b0160c4f065
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2020
ms.locfileid: "48137046"
---
# <a name="email-authentication-in-eop"></a><span data-ttu-id="8945f-103">Authentification de messagerie électronique dans EOP</span><span class="sxs-lookup"><span data-stu-id="8945f-103">Email authentication in EOP</span></span>

<span data-ttu-id="8945f-104">L’authentification de messagerie électronique (également appelée validation du courrier électronique) est un ensemble de normes qui tente de bloquer l’usurpation d’identité (messages électroniques provenant de faux expéditeurs).</span><span class="sxs-lookup"><span data-stu-id="8945f-104">Email authentication (also known as email validation) is a group of standards that tries to stop spoofing (email messages from forged senders).</span></span> <span data-ttu-id="8945f-105">Dans toutes les organisations Microsoft 365, EOP utilise ces normes pour vérifier les e-mails entrants :</span><span class="sxs-lookup"><span data-stu-id="8945f-105">In all Microsoft 365 organizations, EOP uses these standards to verify inbound email:</span></span>

- [<span data-ttu-id="8945f-106">SPF</span><span class="sxs-lookup"><span data-stu-id="8945f-106">SPF</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/set-up-spf-in-office-365-to-help-prevent-spoofing?view=o365-worldwide)

- [<span data-ttu-id="8945f-107">DKIM</span><span class="sxs-lookup"><span data-stu-id="8945f-107">DKIM</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/use-dkim-to-validate-outbound-email?view=o365-worldwide)

- [<span data-ttu-id="8945f-108">DMARC</span><span class="sxs-lookup"><span data-stu-id="8945f-108">DMARC</span></span>](use-dmarc-to-validate-email.md)

<span data-ttu-id="8945f-109">L’authentification de messagerie électronique vérifie que les messages électroniques d’un expéditeur (par exemple, laura@contoso.com) sont légitimes et proviennent de sources attendues pour ce domaine de courrier électronique (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="8945f-109">Email authentication verifies that email messages from a sender (for example, laura@contoso.com) are legitimate and come from expected sources for that email domain (for example, contoso.com.)</span></span>

<span data-ttu-id="8945f-110">Le reste de cette rubrique explique comment fonctionnent ces technologies et comment EOP les utilise pour vérifier les e-mail entrant.</span><span class="sxs-lookup"><span data-stu-id="8945f-110">The rest of this article explains how these technologies work, and how EOP uses them to check inbound email.</span></span>

## <a name="use-email-authentication-to-help-prevent-spoofing"></a><span data-ttu-id="8945f-111">Utilisez l’authentification de messagerie électronique pour empêcher l’usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="8945f-111">Use email authentication to help prevent spoofing</span></span>

<span data-ttu-id="8945f-112">DMARC empêche l’usurpation d’identité en examinant l’adresse **de provenance** dans les messages.</span><span class="sxs-lookup"><span data-stu-id="8945f-112">DMARC prevents spoofing by examining the **From** address in messages.</span></span> <span data-ttu-id="8945f-113">L’adresse **de provenance** est l’adresse e-mail de l’expéditeur que les utilisateurs voient dans leur client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8945f-113">The **From** address is the sender's email address that users see in their email client.</span></span> <span data-ttu-id="8945f-114">Les organisations de messagerie de destination peuvent également vérifier que le domaine de messagerie a réussi les vérifications SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="8945f-114">Destination email organizations can also verify that the email domain has passed SPF or DKIM.</span></span> <span data-ttu-id="8945f-115">En d’autres termes, le domaine a été authentifié et, par conséquent, l’adresse de messagerie de l’expéditeur n’est pas usurpée.</span><span class="sxs-lookup"><span data-stu-id="8945f-115">In other words, the domain has been authenticated and therefore the sender's email address is not spoofed.</span></span>

<span data-ttu-id="8945f-116">Toutefois, les enregistrements DNS pour SPF, DKIM et DMARC (appelés stratégies d’authentification de messagerie électronique) sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="8945f-116">However, DNS records for SPF, DKIM, and DMARC (collectively known as email authentication policies) are optional.</span></span> <span data-ttu-id="8945f-117">Les domaines dotés de stratégies d’authentification de messagerie électronique fortes telles que microsoft.com et skype.com sont protégés contre l’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="8945f-117">Domains with strong email authentication policies like microsoft.com and skype.com are protected from spoofing.</span></span> <span data-ttu-id="8945f-118">Certains domaines qui ont des stratégies d’authentification de messagerie électronique plus faibles ,ou qui n’en ont aucune, ont beaucoup plus de chances d’être usurpés.</span><span class="sxs-lookup"><span data-stu-id="8945f-118">But domains with weaker email authentication policies, or no policy at all, are prime targets for being spoofed.</span></span>

<span data-ttu-id="8945f-119">Depuis le mois de mars 2018, seuls 9 % des domaines des entreprises figurant au classement Fortune 500 ont publié des stratégies d’authentification de messagerie électronique fortes.</span><span class="sxs-lookup"><span data-stu-id="8945f-119">As of March 2018, only 9% of domains of companies in the Fortune 500 publish strong email authentication policies.</span></span> <span data-ttu-id="8945f-120">Les 91 % d'entreprises restantes peuvent être usurpées par un intrus.</span><span class="sxs-lookup"><span data-stu-id="8945f-120">The remaining 91% of companies might be spoofed by an attacker.</span></span> <span data-ttu-id="8945f-121">À moins qu'un autre mécanisme de filtrage de messagerie électronique ne soit en place, le courrier électronique provenant d'expéditeurs usurpés dans ces domaines peut être transmis aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8945f-121">Unless some other email filtering mechanism is in-place, email from spoofed senders in these domains might be delivered to users.</span></span>

![Stratégies DMARC des entreprises du classement Fortune 500](../../media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)

<span data-ttu-id="8945f-123">La part de petites et moyennes entreprises qui publient des stratégies d’authentification de messagerie électronique renforcées est plus petite.</span><span class="sxs-lookup"><span data-stu-id="8945f-123">The proportion of small-to-medium sized companies that publish strong email authentication policies is smaller.</span></span> <span data-ttu-id="8945f-124">Ce nombre est encore plus petit pour les domaines de messagerie électronique situés hors Amérique du Nord et Europe de l’Ouest.</span><span class="sxs-lookup"><span data-stu-id="8945f-124">And the number is even smaller for email domains outside North America and western Europe.</span></span>

<span data-ttu-id="8945f-125">L’absence de stratégies d’authentification fortes est un problème fréquent.</span><span class="sxs-lookup"><span data-stu-id="8945f-125">Lack of strong email authentication policies is a large problem.</span></span> <span data-ttu-id="8945f-126">Si les organisations ne comprennent pas le fonctionnement de l’authentification de messagerie électronique, les intrus, eux, en tire parti grâce à leur parfaite compréhension.</span><span class="sxs-lookup"><span data-stu-id="8945f-126">W while organizations might not understand how email authentication works, attackers fully understand, and they take advantage.</span></span> <span data-ttu-id="8945f-127">En raison de problèmes d’hameçonnage et du faible taux d’adoption de stratégies d’authentification fortes, Microsoft utilise l’*authentification de courrier implicite* pour vérifier les courriers entrants.</span><span class="sxs-lookup"><span data-stu-id="8945f-127">Because of phishing concerns and the limited adoption of strong email authentication policies, Microsoft uses *implicit email authentication* to check inbound email.</span></span>

<span data-ttu-id="8945f-128">L’authentification de courrier implicite est une extension de stratégies d’authentification de messagerie électronique classiques.</span><span class="sxs-lookup"><span data-stu-id="8945f-128">Implicit email authentication is an extension of regular email authentication policies.</span></span> <span data-ttu-id="8945f-129">Ces extensions incluent : la réputation de l’expéditeur, l’historique de l’expéditeur, l’historique du destinataire, l’analyse comportementale et d’autres techniques avancées.</span><span class="sxs-lookup"><span data-stu-id="8945f-129">These extensions include: sender reputation, sender history, recipient history, behavioral analysis, and other advanced techniques.</span></span> <span data-ttu-id="8945f-130">En l’absence d’autres signaux de ces extensions, les messages envoyés depuis des domaines qui n’utilisent pas de stratégie d’authentification de messagerie électronique sont marqués comme provenant d’usurpateurs.</span><span class="sxs-lookup"><span data-stu-id="8945f-130">In the absence of other signals from these extensions, messages sent from domains that don't use email authentication policies will be marked as spoof.</span></span>

<span data-ttu-id="8945f-131">Pour lire l’annonce générale de Microsoft Corporation, voir [A Sea of Phish Part 2 – Enhanced Anti-spoofing in Microsoft 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).</span><span class="sxs-lookup"><span data-stu-id="8945f-131">To see Microsoft's general announcement, see [A Sea of Phish Part 2 - Enhanced Anti-spoofing in Microsoft 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).</span></span>

## <a name="composite-authentication"></a><span data-ttu-id="8945f-132">Authentification composite</span><span class="sxs-lookup"><span data-stu-id="8945f-132">Composite authentication</span></span>

<span data-ttu-id="8945f-133">Si un domaine ne dispose pas d’enregistrements SPF, DKIM et DMARC traditionnels, ces vérifications n’indiquent pas assez d’informations sur l’état d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8945f-133">If a domain doesn't have traditional SPF, DKIM, and DMARC records, those record checks don't communicate enough authentication status information.</span></span> <span data-ttu-id="8945f-134">Par conséquent, Microsoft a développé un algorithme pour l’authentification de courrier implicite.</span><span class="sxs-lookup"><span data-stu-id="8945f-134">Therefore, Microsoft has developed an algorithm for implicit email authentication.</span></span> <span data-ttu-id="8945f-135">Cet algorithme combine plusieurs signaux dans une valeur unique appelée l’_authentification composite_, ou `compauth`.</span><span class="sxs-lookup"><span data-stu-id="8945f-135">This algorithm combines multiple signals into a single value called _composite authentication_, or `compauth` for short.</span></span> <span data-ttu-id="8945f-136">La valeur `compauth` est marquée dans l’en-tête **Authentication-Results**, à l’intérieur des en-têtes de message.</span><span class="sxs-lookup"><span data-stu-id="8945f-136">The `compauth` value is stamped into the **Authentication-Results** header in the message headers.</span></span>

```text
Authentication-Results:
   compauth=<fail | pass | softpass | none> reason=<yyy>
```

<span data-ttu-id="8945f-137">Ces valeurs sont expliquées dans [En-tête de message d’authentification-résultats](anti-spam-message-headers.md#authentication-results-message-header).</span><span class="sxs-lookup"><span data-stu-id="8945f-137">These values are explained at [Authentication-results message header](anti-spam-message-headers.md#authentication-results-message-header).</span></span>

<span data-ttu-id="8945f-138">En examinant les en-têtes de message, les administrateurs ou même les utilisateurs finaux peuvent déterminer comment Microsoft 365 a déterminé que l'expéditeur est usurpé.</span><span class="sxs-lookup"><span data-stu-id="8945f-138">By examining the message headers, admins or even end users can determine how Microsoft 365 determined that the sender is spoofed.</span></span>

## <a name="why-email-authentication-is-not-always-enough-to-stop-spoofing"></a><span data-ttu-id="8945f-139">Pourquoi l’authentification messagerie électronique ne suffit pas toujours pour empêcher l’usurpation</span><span class="sxs-lookup"><span data-stu-id="8945f-139">Why email authentication is not always enough to stop spoofing</span></span>

<span data-ttu-id="8945f-140">Le fait de se fier uniquement aux enregistrements d'authentification de messagerie électronique pour déterminer si un message entrant est usurpé présente les limites suivantes :</span><span class="sxs-lookup"><span data-stu-id="8945f-140">Relying only on email authentication records to determine if an incoming message is spoofed has the following limitations:</span></span>

- <span data-ttu-id="8945f-141">Il se peut que le domaine d’envoi ne dispose pas des enregistrements DNS requis ou que les enregistrements soient mal configurés.</span><span class="sxs-lookup"><span data-stu-id="8945f-141">The sending domain might lack the required DNS records, or the records are incorrectly configured.</span></span>

- <span data-ttu-id="8945f-142">Le domaine source a correctement configuré les enregistrements DNS, mais ce domaine ne correspond pas au domaine dans l’adresse De.</span><span class="sxs-lookup"><span data-stu-id="8945f-142">The source domain has correctly configured DNS records, but that domain doesn't match the domain in the From address.</span></span> <span data-ttu-id="8945f-143">SPF et DKIM n'exigent pas que le domaine soit utilisé dans l'adresse De.</span><span class="sxs-lookup"><span data-stu-id="8945f-143">SPF and DKIM don't require the domain to be used in the From address.</span></span> <span data-ttu-id="8945f-144">Les intrus ou services légitimes peuvent enregistrer un domaine, configurer SPF et DKIM pour le domaine, et utiliser un domaine totalement différent dans l’adresse l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8945f-144">Attackers or legitimate services can register a domain, configure SPF and DKIM for the domain, and use a completely different domain in the From address.</span></span> <span data-ttu-id="8945f-145">Les messages provenant d’expéditeurs de ce domaine réussissent les vérifications SPF et DKIM.</span><span class="sxs-lookup"><span data-stu-id="8945f-145">Messages from senders in this domain will pass SPF and DKIM.</span></span>

<span data-ttu-id="8945f-146">L’authentification composite peut résoudre ces limites en transférant les messages qui, autrement, échoueraient aux contrôles d'authentification de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="8945f-146">Composite authentication can address these limitations by passing messages that would otherwise fail email authentication checks.</span></span>

<span data-ttu-id="8945f-147">Par souci de simplicité, les exemples suivants se concentrent sur les résultats d’authentification de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="8945f-147">For simplicity, the following examples concentrate on email authentication results.</span></span> <span data-ttu-id="8945f-148">D’autres facteurs d’intelligence en aval peuvent identifier les messages qui franchissent l’authentification de messagerie électronique comme étant usurpés, ou les messages qui échouent à l'authentification de messagerie électronique comme étant légitimes.</span><span class="sxs-lookup"><span data-stu-id="8945f-148">Other back-end intelligence factors could identify messages that pass email authentication as spoofed, or messages that fail email email authentication as legitimate.</span></span>

<span data-ttu-id="8945f-149">Par exemple, le domaine fabrikam.com ne disposent pas d’enregistrements SPF, DKIM ou DMARC.</span><span class="sxs-lookup"><span data-stu-id="8945f-149">For example, the fabrikam.com domain has no SPF, DKIM, or DMARC records.</span></span> <span data-ttu-id="8945f-150">Les messages en provenance des expéditeurs du domaine fabrikam.com peuvent échouer à l'authentification composite (notez la valeur `compauth` et la raison) :</span><span class="sxs-lookup"><span data-stu-id="8945f-150">Messages from senders in the fabrikam.com domain can fail composite authentication (note the `compauth` value and reason):</span></span>

```text
Authentication-Results: spf=none (sender IP is 10.2.3.4)
  smtp.mailfrom=fabrikam.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=fabrikam.com; compauth=fail reason=001
From: chris@fabrikam.com
To: michelle@contoso.com
```

<span data-ttu-id="8945f-151">Si fabrikam.com configure un SPF sans enregistrement DKIM, le message peut réussir l’authentification composite.</span><span class="sxs-lookup"><span data-stu-id="8945f-151">If fabrikam.com configures an SPF without a DKIM record, the message can pass composite authentication.</span></span> <span data-ttu-id="8945f-152">Le domaine ayant réussi les vérifications SPF est aligné sur le domaine de l’adresse de l’expéditeur :</span><span class="sxs-lookup"><span data-stu-id="8945f-152">The domain that passed SPF checks is aligned with the domain in the From address:</span></span>

```text
Authentication-Results: spf=pass (sender IP is 10.2.3.4)
  smtp.mailfrom=fabrikam.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=fabrikam.com; compauth=pass reason=109
From: chris@fabrikam.com
To: michelle@contoso.com
```

<span data-ttu-id="8945f-153">Si fabrikam.com configure un DKIM sans enregistrement SPF, le message peut réussir l’authentification composite.</span><span class="sxs-lookup"><span data-stu-id="8945f-153">If fabrikam.com configures a DKIM record without an SPF record, the message can pass composite authentication.</span></span> <span data-ttu-id="8945f-154">Le domaine dans la signature DKIM est aligné sur le domaine de l’adresse de l’expéditeur :</span><span class="sxs-lookup"><span data-stu-id="8945f-154">The domain in the DKIM signature is aligned with the domain in the From address:</span></span>

```text
Authentication-Results: spf=none (sender IP is 10.2.3.4)
  smtp.mailfrom=fabrikam.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.fabrikam.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=fabrikam.com; compauth=pass reason=109
From: chris@fabrikam.com
To: michelle@contoso.com
```

<span data-ttu-id="8945f-155">Si le domaine dans SPF ou si la signature DKIM ne s'alignent pas sur le domaine de l'adresse de l’expéditeur, le message peut échouer à l'authentification composite :</span><span class="sxs-lookup"><span data-stu-id="8945f-155">If the domain in SPF or the DKIM signature doesn't align with the domain in the From address, the message can fail composite authentication:</span></span>

```text
Authentication-Results: spf=none (sender IP is 192.168.1.8)
  smtp.mailfrom=maliciousdomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousdomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: chris@contoso.com
To: michelle@fabrikam.com
```

## <a name="solutions-for-legitimate-senders-who-are-sending-unauthenticated-email"></a><span data-ttu-id="8945f-156">Solutions pour les expéditeurs légitimes qui envoient du courrier électronique non authentifié</span><span class="sxs-lookup"><span data-stu-id="8945f-156">Solutions for legitimate senders who are sending unauthenticated email</span></span>

<span data-ttu-id="8945f-157">Microsoft 365 conserve la trace des contacts qui envoient du courrier électronique non authentifié à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8945f-157">Microsoft 365 keeps track of who is sending unauthenticated email to your organization.</span></span> <span data-ttu-id="8945f-158">Si le service considère que l’expéditeur n’est pas légitime, il indique un échec à l’authentification composite sur les messages de cet expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8945f-158">If the service thinks the sender is not legitimate, it will mark messages from this sender as a composite authentication failure.</span></span> <span data-ttu-id="8945f-159">Pour éviter cette décision, vous pouvez utiliser les recommandations de cette section.</span><span class="sxs-lookup"><span data-stu-id="8945f-159">To avoid this verdict, you can use the recommendations in this section.</span></span>

### <a name="configure-email-authentication-for-domains-you-own"></a><span data-ttu-id="8945f-160">Configurez l’authentification de messagerie électronique pour les domaines que vous possédez</span><span class="sxs-lookup"><span data-stu-id="8945f-160">Configure email authentication for domains you own</span></span>

<span data-ttu-id="8945f-161">Vous pouvez utiliser cette méthode pour résoudre l’usurpation d’identité intra-organisationnelle et inter-domaines dans les cas où vous êtes propriétaire ou interagissez avec plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="8945f-161">You can use this method to resolve intra-org spoofing and cross-domain spoofing in cases where you own or interact with multiple tenants.</span></span> <span data-ttu-id="8945f-162">Cela aide également à résoudre l’usurpation inter-domaines lorsque vous envoyez du courrier à d’autres clients dans Microsoft 365 ou à des tiers hébergés par d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="8945f-162">It also helps resolve cross-domain spoofing where you send to other customers within Microsoft 365 or third parties that are hosted by other providers.</span></span>

- <span data-ttu-id="8945f-163">[Configurez des enregistrements SPF](set-up-spf-in-office-365-to-help-prevent-spoofing.md) pour vos domaines.</span><span class="sxs-lookup"><span data-stu-id="8945f-163">[Configure SPF records](set-up-spf-in-office-365-to-help-prevent-spoofing.md) for your domains.</span></span>

- <span data-ttu-id="8945f-164">[Configurez des enregistrements DKIM](use-dkim-to-validate-outbound-email.md) pour vos domaines principaux.</span><span class="sxs-lookup"><span data-stu-id="8945f-164">[Configure DKIM records](use-dkim-to-validate-outbound-email.md) for your primary domains.</span></span>

- <span data-ttu-id="8945f-165">[Pensez à configurer des enregistrements DMARC](use-dmarc-to-validate-email.md) pour votre domaine afin de déterminer qui sont vos expéditeurs légitimes.</span><span class="sxs-lookup"><span data-stu-id="8945f-165">[Consider setting up DMARC records](use-dmarc-to-validate-email.md) for your domain to determine your legitimate senders.</span></span>

<span data-ttu-id="8945f-166">Microsoft Corporation ne fournit pas de directives d’implémentation détaillées pour les enregistrements SPF, DKIM et DMARC.</span><span class="sxs-lookup"><span data-stu-id="8945f-166">Microsoft doesn't provide detailed implementation guidelines for SPF, DKIM, and DMARC records.</span></span> <span data-ttu-id="8945f-167">Cependant, de nombreuses informations sont disponibles en ligne.</span><span class="sxs-lookup"><span data-stu-id="8945f-167">However, there's many information available online.</span></span> <span data-ttu-id="8945f-168">Il existe également des sociétés tierces spécialisées dans l’aide à la configuration d’enregistrements d’authentification de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="8945f-168">There are also third party companies dedicated to helping your organization setup email authentication records.</span></span>

#### <a name="you-dont-know-all-sources-for-your-email"></a><span data-ttu-id="8945f-169">Vous ne connaissez pas toutes les sources de votre courrier électronique</span><span class="sxs-lookup"><span data-stu-id="8945f-169">You don't know all sources for your email</span></span>

<span data-ttu-id="8945f-170">De nombreux domaines ne publient pas d’enregistrements SPF parce qu’ils ne connaissent pas toutes les sources de messagerie pour les messages de leur domaine.</span><span class="sxs-lookup"><span data-stu-id="8945f-170">Many domains don't publish SPF records because they don't know all of the email sources for messages in their domain.</span></span> <span data-ttu-id="8945f-171">Commencez par publier un enregistrement SPF qui contient toutes les sources de messagerie électronique que vous connaissez (en particulier l'endroit où se situe le trafic de votre entreprise), et publiez la stratégie SPF neutre `?all`.</span><span class="sxs-lookup"><span data-stu-id="8945f-171">Start by publishing an SPF record that contains all of the email sources you know about (especially where your corporate traffic is located), and publish the neutral SPF policy `?all`.</span></span> <span data-ttu-id="8945f-172">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8945f-172">For example:</span></span>

```text
fabrikam.com IN TXT "v=spf1 include:spf.fabrikam.com ?all"
```

<span data-ttu-id="8945f-173">Cet exemple signifie que le courrier électronique provenant de l'infrastructure de votre entreprise franchira l’authentification de courrier électronique, mais que le courrier électronique provenant de sources inconnues reviendra au mode neutre.</span><span class="sxs-lookup"><span data-stu-id="8945f-173">This example means that email from your corporate infrastructure will pass email authentication, but email from unknown sources will fall back to neutral.</span></span>

<span data-ttu-id="8945f-174">Microsoft 365 traite les messages entrants de votre infrastructure d’entreprise comme authentifiés.</span><span class="sxs-lookup"><span data-stu-id="8945f-174">Microsoft 365 will treat inbound email from your corporate infrastructure as authenticated.</span></span> <span data-ttu-id="8945f-175">Les messages électroniques provenant de sources non identifiées peuvent rester marqués comme usurpés si l’authentification implicite échoue.</span><span class="sxs-lookup"><span data-stu-id="8945f-175">Email from unidentified sources might still be marked as spoof if it fails implicit authentication.</span></span> <span data-ttu-id="8945f-176">Cela constitue cependant toujours une amélioration par rapport à tout le courrier électronique que Microsoft 365 marque comme usurpant une identité.</span><span class="sxs-lookup"><span data-stu-id="8945f-176">However, this is still an improvement from all email being marked as spoof by Microsoft 365.</span></span>

<span data-ttu-id="8945f-177">Une fois que vous avez commencé à utiliser une stratégie de secours SPF de `?all`, vous pouvez progressivement découvrir et inclure d’autres sources de messagerie électronique pour vos messages, puis mettre à jour votre enregistrement SPF avec une stratégie plus stricte.</span><span class="sxs-lookup"><span data-stu-id="8945f-177">Once you've gotten started with an SPF fallback policy of `?all`, you can gradually discover and include more email sources for your messages, and then update your SPF record with a stricter policy.</span></span>

### <a name="use-spoof-intelligence-to-configure-permitted-senders-of-unauthenticated-email"></a><span data-ttu-id="8945f-178">Utiliser la veille contre l’usurpation d’identité pour configurer les expéditeurs autorisés de courrier électronique non authentifié.</span><span class="sxs-lookup"><span data-stu-id="8945f-178">Use spoof intelligence to configure permitted senders of unauthenticated email</span></span>

<span data-ttu-id="8945f-179">Vous pouvez également utiliser la [veille contre l’usurpation d’identité](learn-about-spoof-intelligence.md) pour autoriser des expéditeurs à transmettre des messages non authentifiés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8945f-179">You can also use [spoof intelligence](learn-about-spoof-intelligence.md) to permit senders to transmit unauthenticated messages to your organization.</span></span>

<span data-ttu-id="8945f-180">Pour les domaines externes, l’utilisateur usurpé est le domaine dans l’adresse De, tandis que l’infrastructure d’envoi est soit l’adresse IP source (divisée en /24 plages CIDR), soit le domaine de l’organisation de l’enregistrement DNS inversé (PTR).</span><span class="sxs-lookup"><span data-stu-id="8945f-180">For external domains, the spoofed user is the domain in the From address, while the sending infrastructure is either the source IP address (divided up into /24 CIDR ranges), or the organizational domain of the reverse DNS (PTR) record.</span></span>

<span data-ttu-id="8945f-181">Dans la capture d’écran ci-dessous, l’adresse IP source peut être 131.107.18.4 avec l’enregistrement PTR outbound.mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="8945f-181">In the screenshot below, the source IP might be 131.107.18.4 with the PTR record outbound.mail.protection.outlook.com.</span></span> <span data-ttu-id="8945f-182">Il s’affiche sous la forme outlook.com pour l’infrastructure d’envoi.</span><span class="sxs-lookup"><span data-stu-id="8945f-182">This would show up as outlook.com for the sending infrastructure.</span></span>

<span data-ttu-id="8945f-183">Pour autoriser cet expéditeur à envoyer un courrier non authentifié, remplacez **Non** par **Oui**.</span><span class="sxs-lookup"><span data-stu-id="8945f-183">To permit this sender to send unauthenticated email, change the **No** to a **Yes**.</span></span>

![Définition des expéditeurs autorisés par la paramètre](../../media/d4334921-d820-4334-8217-788279701e94.jpg)

### <a name="create-an-allow-entry-for-the-senderrecipient-pair"></a><span data-ttu-id="8945f-185">Créer une entrée d’autorisation pour la paire expéditeur/destinataire</span><span class="sxs-lookup"><span data-stu-id="8945f-185">Create an allow entry for the sender/recipient pair</span></span>

<span data-ttu-id="8945f-186">Pour contourner le filtrage du courrier indésirable, certaines parties du filtrage du hameçonnage, et non le filtrage des programmes malveillants pour des expéditeurs spécifiques, consultez la rubrique [Créer des listes d’expéditeurs sûrs dans Microsoft 365](create-safe-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="8945f-186">To bypass spam filtering, some parts of phish filtering, but not malware filtering for specific senders, see [Create safe sender lists in Microsoft 365](create-safe-sender-lists-in-office-365.md).</span></span>

### <a name="ask-the-sender-to-configure-email-authentication-for-domains-you-dont-own"></a><span data-ttu-id="8945f-187">Demandez à l’expéditeur de configurer l’authentification de courrier électronique pour les domaines que vous ne possédez pas</span><span class="sxs-lookup"><span data-stu-id="8945f-187">Ask the sender to configure email authentication for domains you don't own</span></span>

<span data-ttu-id="8945f-188">En raison du problème de courrier indésirable et de hameçonnage, Microsoft Corporation recommande l'authentification de courrier électronique pour toutes les organisations de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="8945f-188">Because of the problem of spam and phishing, Microsoft recommends email authentication for all email organizations.</span></span> <span data-ttu-id="8945f-189">Au lieu de configurer les remplacements manuels au sein de votre organisation, vous pouvez demander à un administrateur du domaine d’envoi de configurer ses enregistrements d'authentification de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8945f-189">Instead of configuring manual overrides in your organization, you can ask an admin in the sending domain to configure their email authentication records.</span></span>

- <span data-ttu-id="8945f-190">Même si, par le passé, ils n'avaient pas besoin de publier des enregistrements d'authentification de courrier électronique dans le passé, ils doivent le faire s'ils envoient du courrier électronique à Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="8945f-190">Even if they didn't need to publish email authentication records in the past, they should do so if they send email to Microsoft.</span></span>

- <span data-ttu-id="8945f-191">Configurez SPF pour publier les adresses IP d’envoi du domaine et configurez DKIM (si disponible) pour signer numériquement les messages.</span><span class="sxs-lookup"><span data-stu-id="8945f-191">Set up SPF to publish the domain's sending IP addresses, and set up DKIM (if available) to digitally sign messages.</span></span> <span data-ttu-id="8945f-192">Vous devez également envisager de configurer des enregistrements DMARC.</span><span class="sxs-lookup"><span data-stu-id="8945f-192">They should also consider setting up DMARC records.</span></span>

- <span data-ttu-id="8945f-193">S’ils utilisent des expéditeurs en bloc pour envoyer du courrier électronique en leur nom, vérifiez que le domaine dans l'adresse De (s'il leur appartient) s'aligne sur le domaine qui franchit les protocoles SPF ou DMARC.</span><span class="sxs-lookup"><span data-stu-id="8945f-193">If they use bulk senders to send email on their behalf, verify that the domain in the From address (if it belongs to them) aligns with the domain that passes SPF or DMARC.</span></span>

- <span data-ttu-id="8945f-194">Vérifiez que les emplacements suivants (s’ils sont utilisés) sont inclus dans l’enregistrement SPF :</span><span class="sxs-lookup"><span data-stu-id="8945f-194">Verify the following locations (if they use them) are included in the SPF record:</span></span>
  
  - <span data-ttu-id="8945f-195">Serveurs de messagerie électronique locaux.</span><span class="sxs-lookup"><span data-stu-id="8945f-195">On-premises email servers.</span></span>
  - <span data-ttu-id="8945f-196">Courrier électronique envoyé à partir d’un fournisseur Software as-a-service (Logiciel en tant que service).</span><span class="sxs-lookup"><span data-stu-id="8945f-196">Email sent from a software-as-a-service (SaaS) provider.</span></span>
  - <span data-ttu-id="8945f-197">Courrier électronique envoyé à partir d’un service d’hébergement Cloud (Microsoft Azure, GoDaddy, Rackspace, services Web Amazon, etc.).</span><span class="sxs-lookup"><span data-stu-id="8945f-197">Email sent from a cloud-hosting service (Microsoft Azure, GoDaddy, Rackspace, Amazon Web Services, etc.).</span></span>

- <span data-ttu-id="8945f-198">Pour les petits domaines hébergés par un fournisseur de services Internet, configurez l’enregistrement SPF selon les instructions du fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="8945f-198">For small domains that are hosted by an ISP, configure the SPF record according to the instructions from the ISP.</span></span>

<span data-ttu-id="8945f-199">S’il peut être difficile au début d’obtenir des domaines d’envoi qu’ils s’authentifient, avec le temps, à mesure que de plus en plus de filtres de courrier considéreront leurs e-mails comme indésirables, voire les rejetteront, ils seront amenés à configurer les enregistrements appropriés pour améliorer la remise.</span><span class="sxs-lookup"><span data-stu-id="8945f-199">While it may be difficult at first to get sending domains to authenticate, over time, as more and more email filters start junking or even rejecting their email, it will cause them to set up the proper records to ensure better delivery.</span></span> <span data-ttu-id="8945f-200">En outre, leur participation peut contribuer à la lutte contre le hameçonnage et peut réduire la possibilité de hameçonnage au sein de leur organisation ou des organisations auxquelles ils envoient du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8945f-200">Also, their participation can help in the fight against phishing, and can reduce the possibility of phishing in their organization or organizations that they send email to.</span></span>

#### <a name="information-for-infrastructure-providers-isps-esps-or-cloud-hosting-services"></a><span data-ttu-id="8945f-201">Informations pour les fournisseurs d’infrastructure (FSI – Fournisseurs de services Internet, ESP – Fournisseur de services de messagerie électronique ou services d’hébergement Cloud)</span><span class="sxs-lookup"><span data-stu-id="8945f-201">Information for infrastructure providers (ISPs, ESPs, or cloud hosting services)</span></span>

<span data-ttu-id="8945f-202">Si vous hébergez le courrier électronique d'un domaine ou fournissez une infrastructure d'hébergement qui peut envoyer du courrier électronique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8945f-202">If you host a domain's email or provide hosting infrastructure that can send email, you should do the following steps:</span></span>

- <span data-ttu-id="8945f-203">Veillez à ce que vos clients disposent d'une documentation expliquant comment ils doivent configurer leurs enregistrements SPF</span><span class="sxs-lookup"><span data-stu-id="8945f-203">Ensure your customers have documentation that explains how your customers should configure their SPF records</span></span>

- <span data-ttu-id="8945f-204">Pensez à apposer des signatures DKIM sur le courrier électronique sortant, même si le client ne les a pas explicitement configurées (signer avec un domaine par défaut).</span><span class="sxs-lookup"><span data-stu-id="8945f-204">Consider signing DKIM-signatures on outbound email, even if the customer doesn't explicitly set it up (sign with a default domain).</span></span> <span data-ttu-id="8945f-205">Vous pouvez même signer deux fois le courrier avec des signatures DKIM (une fois avec le domaine du client s’il l’a configuré, et une seconde fois avec la signature DKIM de votre organisation).</span><span class="sxs-lookup"><span data-stu-id="8945f-205">You can even double-sign the email with DKIM signatures (once with the customer's domain if they have set it up, and a second time with your company's DKIM signature)</span></span>

<span data-ttu-id="8945f-206">La remise à Microsoft Corporation n’est nullement garantie, même si vous authentifiez le courrier électronique provenant de votre plateforme, mais cela garantit au moins que Microsoft ne considèrera pas votre envoi comme du courrier indésirable parce qu’il n’est pas authentifié.</span><span class="sxs-lookup"><span data-stu-id="8945f-206">Deliverability to Microsoft is not guaranteed even if you authenticate email originating from your platform, but at least it ensures that Microsoft does not junk your email because it isn't authenticated.</span></span>

## <a name="related-links"></a><span data-ttu-id="8945f-207">Liens connexes</span><span class="sxs-lookup"><span data-stu-id="8945f-207">Related links</span></span>

<span data-ttu-id="8945f-208">Pour plus d’informations sur de meilleures utilisations des fournisseurs de services, voir le document [Les meilleures pratiques des fournisseurs de services de messagerie mobile M3AAWG](https://www.m3aawg.org/sites/default/files/m3aawg-mobile-messaging-best-practices-service-providers-2015-08_0.pdf).</span><span class="sxs-lookup"><span data-stu-id="8945f-208">For more information about service providers best practices, see [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/m3aawg-mobile-messaging-best-practices-service-providers-2015-08_0.pdf).</span></span>

<span data-ttu-id="8945f-209">Découvrez comment Office 365 utilise SPF et prend en charge la validation DKIM :</span><span class="sxs-lookup"><span data-stu-id="8945f-209">Learn how Office 365 uses SPF and supports DKIM validation:</span></span>

- [<span data-ttu-id="8945f-210">En savoir plus sur SPF</span><span class="sxs-lookup"><span data-stu-id="8945f-210">More about SPF</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)

- [<span data-ttu-id="8945f-211">En savoir plus sur DKIM</span><span class="sxs-lookup"><span data-stu-id="8945f-211">More about DKIM</span></span>](support-for-validation-of-dkim-signed-messages.md)
