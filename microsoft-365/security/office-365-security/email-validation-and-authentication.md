---
title: Authentification de messagerie électronique dans Microsoft 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
- Strat_O365_IP
ms.custom: TopSMBIssues
localization_priority: Priority
description: Les administrateurs peuvent découvrir comment les services Exchange Online et Exchange Online Protection (EOP) utilisent l’authentification de messagerie électronique (SPF, DKIM et DMARC) pour empêcher l’usurpation d’identité, le hameçonnage et le courrier indésirable.
ms.openlocfilehash: c79a75f1ae520a0c4f885c923b4a56cdb0f7fb87
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44209498"
---
# <a name="email-authentication-in-eop"></a><span data-ttu-id="f8fa3-103">Authentification de messagerie électronique dans EOP</span><span class="sxs-lookup"><span data-stu-id="f8fa3-103">Email authentication in EOP</span></span>

<span data-ttu-id="f8fa3-104">L’authentification de messagerie électronique (également appelée validation du courrier électronique) est un ensemble de normes qui tente de bloquer l’usurpation d’identité (messages électroniques provenant de faux expéditeurs).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-104">Email authentication (also known as email validation) is a group of standards that tries to stop spoofing (email messages from forged senders).</span></span> <span data-ttu-id="f8fa3-105">Dans les organisations Microsoft 365 disposant de boîtes aux lettres dans Exchange Online et les organisations autonomes Exchange Online Protection (EOP) sans boîtes aux lettres Exchange Online, EOP utilise ces normes pour vérifier l’e-mail entrant :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-105">In Microsoft 365 organizations with mailboxes in Exchange Online, and standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP uses these standards to verify inbound email:</span></span>

- [<span data-ttu-id="f8fa3-106">SPF</span><span class="sxs-lookup"><span data-stu-id="f8fa3-106">SPF</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)

- [<span data-ttu-id="f8fa3-107">DKIM</span><span class="sxs-lookup"><span data-stu-id="f8fa3-107">DKIM</span></span>](support-for-validation-of-dkim-signed-messages.md)

- [<span data-ttu-id="f8fa3-108">DMARC</span><span class="sxs-lookup"><span data-stu-id="f8fa3-108">DMARC</span></span>](use-dmarc-to-validate-email.md)

<span data-ttu-id="f8fa3-109">L’authentification de messagerie électronique vérifie que les messages électroniques d’un expéditeur (par exemple, laura@contoso.com) sont légitimes et proviennent de sources attendues pour ce domaine de courrier électronique (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-109">Email authentication verifies that email messages from a sender (for example, laura@contoso.com) are legitimate and come from expected sources for that email domain (for example, contoso.com.)</span></span>

<span data-ttu-id="f8fa3-110">Le reste de cette rubrique explique comment fonctionnent ces technologies et comment EOP les utilise pour vérifier le courrier électronique entrant.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-110">The rest of this topic explains how these technologies work, and how EOP uses them to check inbound email.</span></span>

## <a name="use-email-authentication-to-help-prevent-spoofing"></a><span data-ttu-id="f8fa3-111">Utilisez l’authentification de messagerie électronique pour empêcher l’usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="f8fa3-111">Use email authentication to help prevent spoofing</span></span>

<span data-ttu-id="f8fa3-112">DMARC empêche l’usurpation d’identité en examinant l’adresse **DE** dans les messages (l’adresse de messagerie électronique de l’expéditeur que les utilisateurs voient dans leur client de messagerie).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-112">DMARC prevents spoofing by examining the **From** address in messages (the sender email address that users see in their email client).</span></span> <span data-ttu-id="f8fa3-113">Les organisations de messagerie électronique de destination peuvent également vérifier que le domaine de messagerie électronique a franchi les protocoles SPF ou DKIM, ce qui signifie qu’il a été authentifié et n’est donc pas falsifié.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-113">Destination email organizations can also verify that the email domain has passed SPF or DKIM, which means that the domain has been authenticated and is therefore not spoofed.</span></span> 

<span data-ttu-id="f8fa3-114">Toutefois, le problème réside dans le fait que les enregistrements SPF, DKIM et DMARC dans DNS pour l’authentification de messagerie électronique (collectivement appelées stratégies d’authentification de messagerie électronique) sont complètement facultatifs.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-114">However, the problem is that SPF, DKIM, and DMARC records in DNS for email authentication (collectively known as email authentication policies) are completely optional.</span></span> <span data-ttu-id="f8fa3-115">Dès lors, si les domaines dotés de stratégies d’authentification de messagerie électronique fortes, tels que microsoft.com et skype.com, sont protégés contre l’usurpation d’identité, des domaines dont les stratégies d’authentification de messagerie électronique sont plus faibles, voire inexistantes, constituent des cibles idéales pour de telles usurpations.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-115">Therefore, while domains with strong email authentication policies like microsoft.com and skype.com are protected from spoofing, domains that publish weaker email authentication policies, or no policy at all, are prime targets for being spoofed.</span></span>

<span data-ttu-id="f8fa3-116">Depuis le mois de mars 2018, seuls 9 % des domaines des entreprises figurant au classement Fortune 500 ont publié des stratégies d’authentification de messagerie électronique fortes.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-116">As of March 2018, only 9% of domains of companies in the Fortune 500 publish strong email authentication policies.</span></span> <span data-ttu-id="f8fa3-117">Les 91 % d'entreprises restantes peuvent être usurpées par un intrus.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-117">The remaining 91% of companies might be spoofed by a attacker.</span></span> <span data-ttu-id="f8fa3-118">À moins qu'un autre mécanisme de filtrage de messagerie électronique ne soit en place, le courrier électronique provenant d'expéditeurs usurpés dans ces domaines peut être transmis aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-118">Unless some other email filtering mechanism is in-place, email from spoofed senders in these domains might be delivered to users.</span></span>

![Stratégies DMARC des entreprises du classement Fortune 500](../../media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)

<span data-ttu-id="f8fa3-120">La proportion de petites et moyennes entreprises non reprises au classement Fortune 500 et qui publient des stratégies d’authentification de messagerie électronique fortes est plus faible, et plus faible encore pour les domaines situés en dehors de l’Amérique du Nord et de l’Europe occidentale.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-120">The proportion of small-to-medium sized companies that are not in the Fortune 500 that publish strong email authentication policies is smaller, and smaller still for email domains that are outside of North America and western Europe.</span></span>

<span data-ttu-id="f8fa3-121">Le problème est de taille car, si les entreprises ne sont peut-être pas informées des mécanismes d’authentification de messagerie électronique, les intrus les maîtrisent parfaitement et profitent de ces lacunes.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-121">This is a big problem because while enterprises may not be aware of how email authentication works, attackers fully understand and take advantage it.</span></span> <span data-ttu-id="f8fa3-122">Le hameçonnage est si problématique et l’adoption de stratégies d’authentification de messagerie électronique fortes si limitée que Microsoft Corporation utilise une *authentification implicite messagerie électronique* pour vérifier le courrier entrant.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-122">Because phishing is such a problem, and because of the limited adoption of strong email authentication policies, Microsoft uses *implicit email authentication* to check inbound email.</span></span>

<span data-ttu-id="f8fa3-123">L’authentification implicite de messagerie électronique est basée sur de nombreuses extensions de stratégies d’authentification de messagerie électronique classiques.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-123">Implicit email authentication is built on numerous extensions to regular email authentication policies.</span></span> <span data-ttu-id="f8fa3-124">Ces extensions incluent la réputation de l’expéditeur, l’historique de l’expéditeur, l’historique du destinataire, l’analyse comportementale et d’autres techniques avancées.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-124">These extensions include sender reputation, sender history, recipient history, behavioral analysis, and other advanced techniques.</span></span> <span data-ttu-id="f8fa3-125">Un message provenant d’un domaine n’utilisant pas d’authentification de messagerie électronique est marqué comme une usurpation d’identité, sauf s’il contient d’autres signaux indiquant sa légitimité.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-125">A message sent from a domain that doesn't use email authentication policies will be marked as spoof unless it contains other signals to indicate that it's legitimate.</span></span>

<span data-ttu-id="f8fa3-126">Pour lire l’annonce générale de Microsoft Corporation, voir [A Sea of Phish Part 2 – Enhanced Anti-spoofing in Microsoft 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-126">To see Microsoft's general announcement, see [A Sea of Phish Part 2 - Enhanced Anti-spoofing in Microsoft 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).</span></span>

## <a name="composite-authentication"></a><span data-ttu-id="f8fa3-127">Authentification composite</span><span class="sxs-lookup"><span data-stu-id="f8fa3-127">Composite authentication</span></span>

<span data-ttu-id="f8fa3-128">Si les filtrages SPF, DKIM et DMARC sont utiles en soi, ils ne communiquent pas suffisamment l’état d’authentification quand un message n’a pas d’enregistrement d’authentification explicite.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-128">While SPF, DKIM, and DMARC are all useful by themselves, they don't communicate enough authentication status in the event a message has no explicit authentication records.</span></span> <span data-ttu-id="f8fa3-129">C’est pourquoi Microsoft Corporation a développé un algorithme pour l’authentification implicite de messagerie électronique combinant plusieurs signaux en une valeur unique appelée _Authentification composite_, abrégée en compauth.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-129">Therefore, Microsoft has developed an algorithm for implicit email authentication that combines multiple signals into a single value called _composite authentication_, or compauth for short.</span></span> <span data-ttu-id="f8fa3-130">La valeur compauth est estampillée dans l’en-tête **Authentication-Results**, à l’intérieur des en-têtes de message.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-130">The compauth value is stamped into the **Authentication-Results** header in the message headers.</span></span>

> <span data-ttu-id="f8fa3-131">Authentication-Results :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-131">Authentication-Results:</span></span><br/><span data-ttu-id="f8fa3-132">&nbsp;&nbsp;&nbsp;compauth=\<échec | transmise | softpass | aucune\> raison=\<yyy\></span><span class="sxs-lookup"><span data-stu-id="f8fa3-132">&nbsp;&nbsp;&nbsp;compauth=\<fail | pass | softpass | none\> reason=\<yyy\></span></span>

<span data-ttu-id="f8fa3-133">Ces valeurs sont expliquées dans [En-tête de message d’authentification-résultats](anti-spam-message-headers.md#authentication-results-message-header).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-133">These values are explained at [Authentication-results message header](anti-spam-message-headers.md#authentication-results-message-header).</span></span>

<span data-ttu-id="f8fa3-134">En examinant les en-têtes de message, les administrateurs ou même les utilisateurs finaux peuvent déterminer comment Microsoft 365 a déterminé que l'expéditeur est usurpé.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-134">By examining the message headers, admins or even end users can determine how Microsoft 365 determined that the sender is spoofed.</span></span>

## <a name="why-email-authentication-is-not-always-enough-to-stop-spoofing"></a><span data-ttu-id="f8fa3-135">Pourquoi l’authentification messagerie électronique ne suffit pas toujours pour empêcher l’usurpation</span><span class="sxs-lookup"><span data-stu-id="f8fa3-135">Why email authentication is not always enough to stop spoofing</span></span>

<span data-ttu-id="f8fa3-136">Le fait de se fier uniquement aux enregistrements d'authentification de messagerie électronique pour déterminer si un message entrant est usurpé présente les limites suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-136">Relying only on email authentication records to determine if an incoming message is spoofed has the following limitations:</span></span>

- <span data-ttu-id="f8fa3-137">Il se peut que le domaine d’envoi ne dispose pas des enregistrements DNS requis ou que les enregistrements soient mal configurés.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-137">The sending domain might lack the required DNS records, or the records are incorrectly configured.</span></span>

- <span data-ttu-id="f8fa3-138">Le domaine source a correctement configuré les enregistrements DNS, mais ce domaine ne correspond pas au domaine dans l’adresse De.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-138">The source domain has correctly configured DNS records, but that domain doesn't match the domain in the From address.</span></span> <span data-ttu-id="f8fa3-139">SPF et DKIM n'exigent pas que le domaine soit utilisé dans l'adresse De.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-139">SPF and DKIM don't require the domain to be used in the From address.</span></span> <span data-ttu-id="f8fa3-140">Les intrus ou services légitimes peuvent enregistrer un domaine, configurer SPF et DKIM pour le domaine, utiliser un domaine totalement différent dans l’adresse De, et ce message franchira SPF et DKIM.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-140">Attackers or legitimate services can register a domain, configure SPF and DKIM for the domain, use a completely different domain in the From address, and that message will pass SPF and DKIM.</span></span>

<span data-ttu-id="f8fa3-141">L’authentification composite peut résoudre ces limites en transférant les messages qui, autrement, échoueraient aux contrôles d'authentification de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-141">Composite authentication can address these limitations by passing messages that would otherwise fail email authentication checks.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fa3-142">Comme décrit précédemment, l’authentification implicite de messagerie électronique utilise plusieurs signaux pour déterminer si un message est légitime.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-142">As described earlier, implicit email authentication uses multiple signals to determine if a message is legitimate.</span></span> <span data-ttu-id="f8fa3-143">Par souci de simplicité, les exemples suivants se concentrent sur les résultats d’authentification de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-143">For simplicity, the following examples concentrate on email authentication results.</span></span> <span data-ttu-id="f8fa3-144">D’autres facteurs d’intelligence en aval peuvent identifier les messages qui franchissent l’authentification de messagerie électronique comme étant usurpés, ou les messages qui échouent à l'authentification de messagerie électronique comme étant légitimes.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-144">Other back-end intelligence factors could identify messages that pass email authentication as spoofed, or messages that fail email email authentication as legitimate.</span></span>

<span data-ttu-id="f8fa3-145">Par exemple, le domaine fabrikam.com ne disposent pas d’enregistrements SPF, DKIM ou DMARC.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-145">For example, the fabrikam.com domain has no SPF, DKIM, or DMARC records.</span></span> <span data-ttu-id="f8fa3-146">Les messages en provenance des expéditeurs du domaine fabrikam.com peuvent échouer à l'authentification composite (notez la valeur `compauth` et la raison) :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-146">Messages from senders in the fabrikam.com domain can fail composite authentication (note the `compauth` value and reason):</span></span>

```text
Authentication-Results: spf=none (sender IP is 10.2.3.4)
  smtp.mailfrom=fabrikam.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=fabrikam.com; compauth=fail reason=001
From: chris@fabrikam.com
To: michelle@contoso.com
```

<span data-ttu-id="f8fa3-147">Si fabrikam.com configure un SPF sans enregistrement DKIM, le message peut franchir l'authentification composite, car le domaine qui a franchi le SPF est aligné avec le domaine de l'adresse De :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-147">If fabrikam.com configures an SPF without a DKIM record, the message can pass composite authentication, because the domain that passed SPF is aligned with the domain in the From address:</span></span>

```text
Authentication-Results: spf=pass (sender IP is 10.2.3.4)
  smtp.mailfrom=fabrikam.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=fabrikam.com; compauth=pass reason=109
From: chris@fabrikam.com
To: michelle@contoso.com
```

<span data-ttu-id="f8fa3-148">Si fabrikam.com configure un DKIM sans enregistrement SPF, le message peut franchir l'authentification composite, car le domaine dans la signature DKIM franchie est aligné avec le domaine dans l'adresse De :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-148">If fabrikam.com configures a DKIM record without an SPF record, the message can pass composite authentication, because the domain in the passed DKIM signature is aligned with the domain in the From address:</span></span>

```text
Authentication-Results: spf=none (sender IP is 10.2.3.4)
  smtp.mailfrom=fabrikam.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.fabrikam.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=fabrikam.com; compauth=pass reason=109
From: chris@fabrikam.com
To: michelle@contoso.com
```

<span data-ttu-id="f8fa3-149">Si le domaine dans SPF ou la signature DKIM ne s'aligne pas avec le domaine dans l'adresse De, le message peut échouer à l'authentification composite :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-149">If the domain in SPF or the DKIM signature don't align with the domain in the From address, the message can fail composite authentication:</span></span>

```text
Authentication-Results: spf=none (sender IP is 192.168.1.8)
  smtp.mailfrom=maliciousdomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousdomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: chris@contoso.com
To: michelle@fabrikam.com
```

## <a name="solutions-for-legitimate-senders-who-are-sending-unauthenticated-email"></a><span data-ttu-id="f8fa3-150">Solutions pour les expéditeurs légitimes qui envoient du courrier électronique non authentifié</span><span class="sxs-lookup"><span data-stu-id="f8fa3-150">Solutions for legitimate senders who are sending unauthenticated email</span></span>

<span data-ttu-id="f8fa3-151">Microsoft 365 conserve la trace des contacts qui envoient du courrier électronique non authentifié à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-151">Microsoft 365 keeps track of who is sending unauthenticated email to your organization.</span></span> <span data-ttu-id="f8fa3-152">Si le service considère que l’expéditeur n’est pas légitime, il le marque comme échec d'authentification composite.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-152">If the service thinks the sender is not legitimate, it will mark it as a composite authentication failure.</span></span> <span data-ttu-id="f8fa3-153">Pour éviter cela, vous pouvez utiliser les recommandations de cette section.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-153">To avoid this, you can use the recommendations in this section.</span></span>

### <a name="configure-email-authentication-for-domains-you-own"></a><span data-ttu-id="f8fa3-154">Configurez l’authentification de messagerie électronique pour les domaines que vous possédez</span><span class="sxs-lookup"><span data-stu-id="f8fa3-154">Configure email authentication for domains you own</span></span>

<span data-ttu-id="f8fa3-155">Vous pouvez utiliser cette méthode pour résoudre l’usurpation d’identité intra-organisationnelle et inter-domaines dans les cas où vous êtes propriétaire ou interagissez avec plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-155">You can use this method to resolve intra-org spoofing and cross-domain spoofing in cases where you own or interact with multiple tenants.</span></span> <span data-ttu-id="f8fa3-156">Cela aide également à résoudre l’usurpation inter-domaines lorsque vous envoyez du courrier à d’autres clients dans Microsoft 365 ou à des tiers hébergés par d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-156">It also helps resolve cross-domain spoofing where you send to other customers within Microsoft 365 or third parties that are hosted by other providers.</span></span>

- <span data-ttu-id="f8fa3-157">[Configurez des enregistrements SPF](set-up-spf-in-office-365-to-help-prevent-spoofing.md) pour vos domaines.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-157">[Configure SPF records](set-up-spf-in-office-365-to-help-prevent-spoofing.md) for your domains.</span></span>

- <span data-ttu-id="f8fa3-158">[Configurez des enregistrements DKIM](use-dkim-to-validate-outbound-email.md) pour vos domaines principaux.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-158">[Configure DKIM records](use-dkim-to-validate-outbound-email.md) for your primary domains.</span></span>

- <span data-ttu-id="f8fa3-159">[Pensez à configurer des enregistrements DMARC](use-dmarc-to-validate-email.md) pour votre domaine afin de déterminer qui sont vos expéditeurs légitimes.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-159">[Consider setting up DMARC records](use-dmarc-to-validate-email.md) for your domain to determine your legitimate senders.</span></span>

<span data-ttu-id="f8fa3-160">Microsoft Corporation ne fournit pas de directives d’implémentation détaillées pour les enregistrements SPF, DKIM et DMARC.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-160">Microsoft doesn't provide detailed implementation guidelines for SPF, DKIM, and DMARC records.</span></span> <span data-ttu-id="f8fa3-161">Toutefois, de nombreuses informations sont disponibles en ligne.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-161">However, there's a lot of information available online.</span></span> <span data-ttu-id="f8fa3-162">Il existe également des sociétés tierces spécialisées dans l’aide à la configuration d’enregistrements d’authentification de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-162">There are also 3rd party companies dedicated to helping your organization set up email authentication records.</span></span>

#### <a name="you-dont-know-all-sources-for-your-email"></a><span data-ttu-id="f8fa3-163">Vous ne connaissez pas toutes les sources de votre courrier électronique</span><span class="sxs-lookup"><span data-stu-id="f8fa3-163">You don't know all sources for your email</span></span>

<span data-ttu-id="f8fa3-164">De nombreux domaines ne publient pas d’enregistrements SPF parce qu’ils ne connaissent pas toutes les sources de messagerie pour les messages de leur domaine.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-164">Many domains don't publish SPF records because they don't know all of the email sources for messages in their domain.</span></span> <span data-ttu-id="f8fa3-165">Commencez par publier un enregistrement SPF qui contient toutes les sources de messagerie électronique que vous connaissez (en particulier l'endroit où se situe le trafic de votre entreprise), et publiez la stratégie SPF neutre `?all`.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-165">Start by publishing an SPF record that contains all of the email sources you know about (especially where your corporate traffic is located), and publish the neutral SPF policy `?all`.</span></span> <span data-ttu-id="f8fa3-166">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-166">For example:</span></span>

```text
fabrikam.com IN TXT "v=spf1 include:spf.fabrikam.com ?all"
```

<span data-ttu-id="f8fa3-167">Cet exemple signifie que le courrier électronique provenant de l'infrastructure de votre entreprise franchira l’authentification de courrier électronique, mais que le courrier électronique provenant de sources inconnues reviendra au mode neutre.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-167">This example means that email from your corporate infrastructure will pass email authentication, but email from unknown sources will fall back to neutral.</span></span>

<span data-ttu-id="f8fa3-168">Microsoft 365 traite le courrier électronique entrant provenant de l’infrastructure de votre entreprise comme étant authentifié, mais le courrier électronique provenant de sources non identifiées peut toujours être marqué comme usurpant une identité (selon que Microsoft 365 peut l’authentifier de manière implicite ou non).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-168">Microsoft 365 will treat inbound email from your corporate infrastructure as authenticated, but email from unidentified sources might still be marked as spoof (depending upon whether Microsoft 365 can implicitly authenticate it).</span></span> <span data-ttu-id="f8fa3-169">Cela constitue cependant toujours une amélioration par rapport à tout le courrier électronique que Microsoft 365 marque comme usurpant une identité.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-169">However, this is still an improvement from all email being marked as spoof by Microsoft 365.</span></span>

<span data-ttu-id="f8fa3-170">Une fois que vous avez commencé à utiliser une stratégie de secours SPF de `?all`, vous pouvez progressivement découvrir et inclure d’autres sources de messagerie électronique pour vos messages, puis mettre à jour votre enregistrement SPF avec une stratégie plus stricte.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-170">Once you've gotten started with an SPF fallback policy of `?all`, you can gradually discover and include more email sources for your messages, and then update your SPF record with a stricter policy.</span></span>

### <a name="use-spoof-intelligence-to-configure-permitted-senders-of-unauthenticated-email"></a><span data-ttu-id="f8fa3-171">Utiliser la veille contre l’usurpation d’identité pour configurer les expéditeurs autorisés de courrier électronique non authentifié.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-171">Use spoof intelligence to configure permitted senders of unauthenticated email</span></span>

<span data-ttu-id="f8fa3-172">Vous pouvez également utiliser la [veille contre l’usurpation d’identité](learn-about-spoof-intelligence.md) pour autoriser des expéditeurs à transmettre des messages non authentifiés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-172">You can also use [spoof intelligence](learn-about-spoof-intelligence.md) to permit senders to transmit unauthenticated messages to your organization.</span></span>

<span data-ttu-id="f8fa3-173">Pour les domaines externes, l’utilisateur usurpé est le domaine dans l’adresse De, tandis que l’infrastructure d’envoi est soit l’adresse IP source (divisée en /24 plages CIDR), soit le domaine de l’organisation de l’enregistrement DNS inversé (PTR).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-173">For external domains, the spoofed user is the domain in the From address, while the sending infrastructure is either the source IP address (divided up into /24 CIDR ranges), or the organizational domain of the reverse DNS (PTR) record.</span></span>

<span data-ttu-id="f8fa3-174">Dans la capture d’écran ci-dessous, l’adresse IP source peut être 131.107.18.4 avec l’enregistrement PTR outbound.mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-174">In the screenshot below, the source IP might be 131.107.18.4 with the PTR record outbound.mail.protection.outlook.com.</span></span> <span data-ttu-id="f8fa3-175">Il s’affiche sous la forme outlook.com pour l’infrastructure d’envoi.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-175">This would show up as outlook.com for the sending infrastructure.</span></span>

<span data-ttu-id="f8fa3-176">Pour autoriser cet expéditeur à envoyer un courrier non authentifié, remplacez **Non** par **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-176">To permit this sender to send unauthenticated email, change the **No** to a **Yes**.</span></span>

![Définition des expéditeurs autorisés par la paramètre](../../media/d4334921-d820-4334-8217-788279701e94.jpg)

### <a name="create-an-allow-entry-for-the-senderrecipient-pair"></a><span data-ttu-id="f8fa3-178">Créer une entrée d’autorisation pour la paire expéditeur/destinataire</span><span class="sxs-lookup"><span data-stu-id="f8fa3-178">Create an allow entry for the sender/recipient pair</span></span>

<span data-ttu-id="f8fa3-179">Pour contourner le filtrage du courrier indésirable, certaines parties du filtrage du hameçonnage, et non le filtrage des programmes malveillants pour des expéditeurs spécifiques, consultez la rubrique [Créer des listes d’expéditeurs sûrs dans Microsoft 365](create-safe-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-179">To bypass spam filtering, some parts of phish filtering, but not malware filtering for specific senders, see [Create safe sender lists in Microsoft 365](create-safe-sender-lists-in-office-365.md).</span></span>

### <a name="ask-the-sender-to-configure-email-authentication-for-domains-you-dont-own"></a><span data-ttu-id="f8fa3-180">Demandez à l’expéditeur de configurer l’authentification de courrier électronique pour les domaines que vous ne possédez pas</span><span class="sxs-lookup"><span data-stu-id="f8fa3-180">Ask the sender to configure email authentication for domains you don't own</span></span>

<span data-ttu-id="f8fa3-181">En raison du problème de courrier indésirable et de hameçonnage, Microsoft Corporation recommande l'authentification de courrier électronique pour toutes les organisations de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-181">Because of the problem of spam and phishing, Microsoft recommends email authentication for all email organizations.</span></span> <span data-ttu-id="f8fa3-182">Au lieu de configurer les remplacements manuels au sein de votre organisation, vous pouvez demander à un administrateur du domaine d’envoi de configurer ses enregistrements d'authentification de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-182">Instead of configuring manual overrides in your organization, you can ask an admin in the sending domain to configure their email authentication records.</span></span>

- <span data-ttu-id="f8fa3-183">Même si, par le passé, ils n'avaient pas besoin de publier des enregistrements d'authentification de courrier électronique dans le passé, ils doivent le faire s'ils envoient du courrier électronique à Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-183">Even if they didn't need to publish email authentication records in the past, they should do so if they send email to Microsoft.</span></span>

- <span data-ttu-id="f8fa3-184">Configurez SPF pour publier les adresses IP d’envoi du domaine et configurez DKIM (si disponible) pour signer numériquement les messages.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-184">Set up SPF to publish the domain's sending IP addresses, and set up DKIM (if available) to digitally sign messages.</span></span> <span data-ttu-id="f8fa3-185">Vous devez également envisager de configurer des enregistrements DMARC.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-185">They should also consider setting up DMARC records.</span></span>

- <span data-ttu-id="f8fa3-186">S’ils utilisent des expéditeurs en bloc pour envoyer du courrier électronique en leur nom, vérifiez que le domaine dans l'adresse De (s'il leur appartient) s'aligne sur le domaine qui franchit les protocoles SPF ou DMARC.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-186">If they use bulk senders to send email on their behalf, verify that the domain in the From address (if it belongs to them) aligns with the domain that passes SPF or DMARC.</span></span>

- <span data-ttu-id="f8fa3-187">Vérifiez que les emplacements suivants (s’ils sont utilisés) sont inclus dans l’enregistrement SPF :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-187">Verify the following locations (if they use them) are included in the SPF record:</span></span>
  
  - <span data-ttu-id="f8fa3-188">Serveurs de messagerie électronique locaux.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-188">On-premises email servers.</span></span>
  - <span data-ttu-id="f8fa3-189">Courrier électronique envoyé à partir d’un fournisseur Software as-a-service (Logiciel en tant que service).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-189">Email sent from a software-as-a-service (SaaS) provider.</span></span>
  - <span data-ttu-id="f8fa3-190">Courrier électronique envoyé à partir d’un service d’hébergement Cloud (Microsoft Azure, GoDaddy, Rackspace, services Web Amazon, etc.).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-190">Email sent from a cloud-hosting service (Microsoft Azure, GoDaddy, Rackspace, Amazon Web Services, etc.).</span></span>

- <span data-ttu-id="f8fa3-191">Pour les petits domaines hébergés par un fournisseur de services Internet, configurez l’enregistrement SPF selon les instructions du fournisseur de services Internet.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-191">For small domains that are hosted by an ISP, configure the SPF record according to the instructions from the ISP.</span></span>

<span data-ttu-id="f8fa3-192">S’il peut être difficile au début d’obtenir des domaines d’envoi qu’ils s’authentifient, avec le temps, à mesure que de plus en plus de filtres de courrier considéreront leurs e-mails comme indésirables, voire les rejetteront, ils seront amenés à configurer les enregistrements appropriés pour améliorer la remise.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-192">While it may be difficult at first to get sending domains to authenticate, over time, as more and more email filters start junking or even rejecting their email, it will cause them to set up the proper records to ensure better delivery.</span></span> <span data-ttu-id="f8fa3-193">En outre, leur participation peut contribuer à la lutte contre le hameçonnage et peut réduire la possibilité de hameçonnage au sein de leur organisation ou des organisations auxquelles ils envoient du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-193">Also, their participation can help in the fight against phishing, and can reduce the possibility of phishing in their organization or organizations that they send email to.</span></span>

#### <a name="information-for-infrastructure-providers-isps-esps-or-cloud-hosting-services"></a><span data-ttu-id="f8fa3-194">Informations pour les fournisseurs d’infrastructure (FSI – Fournisseurs de services Internet, ESP – Fournisseur de services de messagerie électronique ou services d’hébergement Cloud)</span><span class="sxs-lookup"><span data-stu-id="f8fa3-194">Information for infrastructure providers (ISPs, ESPs, or cloud hosting services)</span></span>

<span data-ttu-id="f8fa3-195">Si vous hébergez le courrier électronique d'un domaine ou fournissez une infrastructure d'hébergement qui peut envoyer du courrier électronique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f8fa3-195">If you host a domain's email or provide hosting infrastructure that can send email, you should do the following steps:</span></span>

- <span data-ttu-id="f8fa3-196">Veillez à ce que vos clients disposent d'une documentation expliquant comment ils doivent configurer leurs enregistrements SPF</span><span class="sxs-lookup"><span data-stu-id="f8fa3-196">Ensure your customers have documentation that explains how your customers should configure their SPF records</span></span>

- <span data-ttu-id="f8fa3-197">Pensez à apposer des signatures DKIM sur le courrier électronique sortant, même si le client ne les a pas explicitement configurées (signer avec un domaine par défaut).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-197">Consider signing DKIM-signatures on outbound email, even if the customer doesn't explicitly set it up (sign with a default domain).</span></span> <span data-ttu-id="f8fa3-198">Vous pouvez même signer deux fois le courrier avec des signatures DKIM (une fois avec le domaine du client s’il l’a configuré, et une seconde fois avec la signature DKIM de votre organisation).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-198">You can even double-sign the email with DKIM signatures (once with the customer's domain if they have set it up, and a second time with your company's DKIM signature)</span></span>

<span data-ttu-id="f8fa3-199">La remise à Microsoft Corporation n’est nullement garantie, même si vous authentifiez le courrier électronique provenant de votre plateforme, mais cela garantit au moins que Microsoft ne considèrera pas votre envoi comme du courrier indésirable parce qu’il n’est pas authentifié.</span><span class="sxs-lookup"><span data-stu-id="f8fa3-199">Deliverability to Microsoft is not guaranteed even if you authenticate email originating from your platform, but at least it ensures that Microsoft does not junk your email because it isn't authenticated.</span></span>

<span data-ttu-id="f8fa3-200">Pour plus d’informations sur les meilleures pratiques des fournisseurs de services, voir le document [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).</span><span class="sxs-lookup"><span data-stu-id="f8fa3-200">For more details on service providers best practices, see [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).</span></span>
