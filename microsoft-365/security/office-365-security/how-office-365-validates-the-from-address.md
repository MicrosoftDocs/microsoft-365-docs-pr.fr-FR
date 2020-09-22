---
title: Comment EOP valide l’adresse de pour empêcher le hameçonnage
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les types d’adresses de messagerie qui sont acceptés ou refusés par Exchange Online Protection (EOP) et Outlook.com afin d’empêcher le hameçonnage.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: e0afd05c80bb4de665d23b17c7089631dad93c78
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48196058"
---
# <a name="how-eop-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="5583b-103">Comment EOP valide l’adresse de pour empêcher le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="5583b-103">How EOP validates the From address to prevent phishing</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="5583b-104">Les attaques par hameçonnage représentent une menace constante pour toute organisation de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-104">Phishing attacks are a constant threat to any email organization.</span></span> <span data-ttu-id="5583b-105">En plus des [adresses de messagerie d’expéditeur usurpées (falsifiées)](anti-spoofing-protection.md), les agresseurs utilisent souvent des valeurs de l’adresse de provenance qui enfreignent les normes Internet.</span><span class="sxs-lookup"><span data-stu-id="5583b-105">In addition to using [spoofed (forged) sender email addresses](anti-spoofing-protection.md), attackers often use values in the From address that violate internet standards.</span></span> <span data-ttu-id="5583b-106">Pour éviter ce type de hameçonnage, Exchange Online Protection (EOP) et Outlook.com requièrent désormais que les messages entrants incluent une adresse d’adresse conforme à la RFC, comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5583b-106">To help prevent this type of phishing, Exchange Online Protection (EOP) and Outlook.com now require inbound messages to include an RFC-compliant From address as described in this topic.</span></span> <span data-ttu-id="5583b-107">Cette mise en œuvre a été activée en novembre 2017.</span><span class="sxs-lookup"><span data-stu-id="5583b-107">This enforcement was enabled in November 2017.</span></span>

<span data-ttu-id="5583b-108">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="5583b-108">**Notes**:</span></span>

- <span data-ttu-id="5583b-109">Si vous recevez régulièrement du courrier électronique d’organisations qui ont des adresses de provenance incorrectes, comme décrit dans cette rubrique, encouragez ces organisations à mettre à jour leurs serveurs de messagerie afin de se conformer aux normes de sécurité modernes.</span><span class="sxs-lookup"><span data-stu-id="5583b-109">If you regularly receive email from organizations that have malformed From addresses as described in this topic, encourage these organizations to update their email servers to comply with modern security standards.</span></span>

- <span data-ttu-id="5583b-110">Le champ expéditeur associé (utilisé par envoyer de la part de et des listes de publipostage) n’est pas affecté par ces exigences.</span><span class="sxs-lookup"><span data-stu-id="5583b-110">The related Sender field (used by Send on Behalf and mailing lists) isn't affected by these requirements.</span></span> <span data-ttu-id="5583b-111">Pour plus d’informations, consultez le billet de blog suivant : qu’est- [ce que nous voulons dire lorsque nous faisons référence à l’expéditeur d’un message électronique ?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/).</span><span class="sxs-lookup"><span data-stu-id="5583b-111">For more information, see the following blog post: [What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/).</span></span>

## <a name="an-overview-of-email-message-standards"></a><span data-ttu-id="5583b-112">Vue d’ensemble des standards des messages électroniques</span><span class="sxs-lookup"><span data-stu-id="5583b-112">An overview of email message standards</span></span>

<span data-ttu-id="5583b-113">Un message électronique SMTP standard est constitué d’une *enveloppe de message* et d’un contenu de message.</span><span class="sxs-lookup"><span data-stu-id="5583b-113">A standard SMTP email message consists of a *message envelope* and message content.</span></span> <span data-ttu-id="5583b-114">L’enveloppe de message contient les informations requises pour la transmission et la remise du message entre les serveurs SMTP.</span><span class="sxs-lookup"><span data-stu-id="5583b-114">The message envelope contains information that's required for transmitting and delivering the message between SMTP servers.</span></span> <span data-ttu-id="5583b-115">Le contenu du message comporte les champs d’en-tête de message (collectivement appelés l’*en-tête de message*) et le corps du message.</span><span class="sxs-lookup"><span data-stu-id="5583b-115">The message content contains message header fields (collectively called the *message header*) and the message body.</span></span> <span data-ttu-id="5583b-116">L’enveloppe de message est décrite dans la [norme rfc 5321](https://tools.ietf.org/html/rfc5321)et l’en-tête de message est décrit dans la [spécification RFC 5322](https://tools.ietf.org/html/rfc5322).</span><span class="sxs-lookup"><span data-stu-id="5583b-116">The message envelope is described in [RFC 5321](https://tools.ietf.org/html/rfc5321), and the message header is described in [RFC 5322](https://tools.ietf.org/html/rfc5322).</span></span> <span data-ttu-id="5583b-117">Les destinataires ne voient jamais l’enveloppe de message réelle, car elle est générée par le processus de transmission des messages, et elle ne fait pas partie du message.</span><span class="sxs-lookup"><span data-stu-id="5583b-117">Recipients never see the actual message envelope because it's generated by the message transmission process, and it isn't actually part of the message.</span></span>

- <span data-ttu-id="5583b-118">L' `5321.MailFrom` adresse (également appelée adresse **de messagerie de** l’expéditeur, expéditeur P1 ou expéditeur de l’enveloppe) est l’adresse de messagerie utilisée dans la transmission SMTP du message.</span><span class="sxs-lookup"><span data-stu-id="5583b-118">The `5321.MailFrom` address (also known as the **MAIL FROM** address, P1 sender, or envelope sender) is the email address that's used in the SMTP transmission of the message.</span></span> <span data-ttu-id="5583b-119">Cette adresse de messagerie est généralement enregistrée dans le champ d’en-tête de **retour** de l’en-tête du message (bien que l’expéditeur ait la possibilité de désigner une autre adresse de messagerie de **chemin d’accès** ).</span><span class="sxs-lookup"><span data-stu-id="5583b-119">This email address is typically recorded in the **Return-Path** header field in the message header (although it's possible for the sender to designate a different **Return-Path** email address).</span></span>

- <span data-ttu-id="5583b-120">Le `5322.From` (également appelé l’adresse de l’expéditeur ou l’expéditeur P2) est l’adresse de messagerie dans le champ de l’en-tête **de** , et est l’adresse de messagerie de l’expéditeur affichée dans les clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-120">The `5322.From` (also known as the From address or P2 sender) is the email address in the **From** header field, and is the sender's email address that's displayed in email clients.</span></span> <span data-ttu-id="5583b-121">L’adresse de provenance est l’élément de la configuration requise dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5583b-121">The From address is the focus of the requirements in this topic.</span></span>

<span data-ttu-id="5583b-122">L’adresse de l’adresse est définie en détail dans plusieurs RFC (par exemple, les sections de la norme RFC 5322 3.2.3, 3,4 et 3.4.1, et la [norme rfc 3696](https://tools.ietf.org/html/rfc3696)).</span><span class="sxs-lookup"><span data-stu-id="5583b-122">The From address is defined in detail across several RFCs (for example, RFC 5322 sections 3.2.3, 3.4, and 3.4.1, and [RFC 3696](https://tools.ietf.org/html/rfc3696)).</span></span> <span data-ttu-id="5583b-123">Il existe de nombreuses variantes de l’adressage et ce qui est considéré comme valide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="5583b-123">There are many variations on addressing and what's considered valid or invalid.</span></span> <span data-ttu-id="5583b-124">Pour simplifier, nous vous recommandons de suivre le format et les définitions suivants :</span><span class="sxs-lookup"><span data-stu-id="5583b-124">To keep it simple, we recommend the following format and definitions:</span></span>

`From: "Display Name" <EmailAddress>`

- <span data-ttu-id="5583b-125">**Nom d’affichage**: expression facultative qui décrit le propriétaire de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-125">**Display Name**: An optional phrase that describes the owner of the email address.</span></span>

  - <span data-ttu-id="5583b-126">Nous vous recommandons de toujours placer le nom d’affichage entre guillemets doubles ("), comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5583b-126">We recommend that you always enclose the display name in double quotation marks (") as shown.</span></span> <span data-ttu-id="5583b-127">Si le nom complet contient une virgule, vous _devez_ placer la chaîne entre guillemets doubles par RFC 5322.</span><span class="sxs-lookup"><span data-stu-id="5583b-127">If the display name contains a comma, you _must_ enclose the string in double quotation marks per RFC 5322.</span></span>
  - <span data-ttu-id="5583b-128">Si l’adresse de l’adresse contient un nom d’affichage, la valeur EmailAddress doit être placée entre chevrons (< >) comme illustré.</span><span class="sxs-lookup"><span data-stu-id="5583b-128">If the From address includes a display name, the EmailAddress value must be enclosed in angle brackets (< >) as shown.</span></span>
  - <span data-ttu-id="5583b-129">Microsoft recommande vivement d’insérer un espace entre le nom d’affichage et l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-129">Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>

- <span data-ttu-id="5583b-130">**EmailAddress**: une adresse de messagerie utilise le format `local-part@domain` suivant :</span><span class="sxs-lookup"><span data-stu-id="5583b-130">**EmailAddress**: An email address uses the format `local-part@domain`:</span></span>

  - <span data-ttu-id="5583b-131">**local-part**: une chaîne qui identifie la boîte aux lettres associée à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5583b-131">**local-part**: A string that identifies the mailbox associated with the address.</span></span> <span data-ttu-id="5583b-132">Cette valeur est unique au sein du domaine.</span><span class="sxs-lookup"><span data-stu-id="5583b-132">This value is unique within the domain.</span></span> <span data-ttu-id="5583b-133">Souvent, le nom d’utilisateur ou le GUID du propriétaire de la boîte aux lettres est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5583b-133">Often, the mailbox owner's username or GUID is used.</span></span>
  - <span data-ttu-id="5583b-134">**domaine**: nom de domaine complet (FQDN) du serveur de messagerie qui héberge la boîte aux lettres identifiée par la partie locale de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-134">**domain**: The fully qualified domain name (FQDN) of the email server that hosts the mailbox identified by the local-part of the email address.</span></span>

  <span data-ttu-id="5583b-135">Voici quelques considérations supplémentaires pour la valeur EmailAddress :</span><span class="sxs-lookup"><span data-stu-id="5583b-135">These are some additional considerations for the EmailAddress value:</span></span>

  - <span data-ttu-id="5583b-136">Une seule adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-136">Only one email address.</span></span>
  - <span data-ttu-id="5583b-137">Nous vous recommandons de ne pas séparer les chevrons avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="5583b-137">We recommend that you do not separate the angle brackets with spaces.</span></span>
  - <span data-ttu-id="5583b-138">N’incluez pas de texte supplémentaire après l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5583b-138">Don't include additional text after the email address.</span></span>

## <a name="examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="5583b-139">Exemples d’adresses valides et non valides</span><span class="sxs-lookup"><span data-stu-id="5583b-139">Examples of valid and invalid From addresses</span></span>

<span data-ttu-id="5583b-140">Les adresses de messagerie suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="5583b-140">The following From email addresses are valid:</span></span>

- `From: sender@contoso.com`

- `From: <sender@contoso.com>`

- <span data-ttu-id="5583b-141">`From: < sender@contoso.com >` (Non recommandé, car il y a des espaces entre les chevrons et l’adresse de messagerie.)</span><span class="sxs-lookup"><span data-stu-id="5583b-141">`From: < sender@contoso.com >` (Not recommended because there are spaces between the angle brackets and the email address.)</span></span>

- `From: "Sender, Example" <sender.example@contoso.com>`

- `From: "Microsoft 365" <sender@contoso.com>`

- <span data-ttu-id="5583b-142">`From: Microsoft 365 <sender@contoso.com>` (Non recommandé, car le nom d’affichage n’est pas entouré de guillemets doubles.)</span><span class="sxs-lookup"><span data-stu-id="5583b-142">`From: Microsoft 365 <sender@contoso.com>` (Not recommended because the display name is not enclosed in double quotation marks.)</span></span>

<span data-ttu-id="5583b-143">Les adresses de messagerie suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="5583b-143">The following From email addresses are invalid:</span></span>

- <span data-ttu-id="5583b-144">**Non de l’adresse**: certains messages automatisés n’incluent pas d’adresse de provenance.</span><span class="sxs-lookup"><span data-stu-id="5583b-144">**No From address**: Some automated messages don't include a From address.</span></span> <span data-ttu-id="5583b-145">Dans le passé, lorsque Microsoft 365 ou Outlook.com a reçu un message sans adresse de provenance, le service a ajouté la valeur par défaut suivante de : adresse pour que le message soit remis :</span><span class="sxs-lookup"><span data-stu-id="5583b-145">In the past, when Microsoft 365 or Outlook.com received a message without a From address, the service added the following default From: address to make the message deliverable:</span></span>

  `From: <>`

  <span data-ttu-id="5583b-146">Désormais, les messages dont l’adresse est vide à partir de ne sont plus acceptés.</span><span class="sxs-lookup"><span data-stu-id="5583b-146">Now, messages with a blank From address are no longer accepted.</span></span>

- <span data-ttu-id="5583b-147">`From: Microsoft 365 sender@contoso.com` (Le nom complet est présent, mais l’adresse de messagerie n’est pas entourée de crochets pointus.)</span><span class="sxs-lookup"><span data-stu-id="5583b-147">`From: Microsoft 365 sender@contoso.com` (The display name is present, but the email address is not enclosed in angle brackets.)</span></span>

- <span data-ttu-id="5583b-148">`From: "Microsoft 365" <sender@contoso.com> (Sent by a process)` (Texte après l’adresse de messagerie.)</span><span class="sxs-lookup"><span data-stu-id="5583b-148">`From: "Microsoft 365" <sender@contoso.com> (Sent by a process)` (Text after the email address.)</span></span>

- <span data-ttu-id="5583b-149">`From: Sender, Example <sender.example@contoso.com>` (Le nom complet contient une virgule, mais n’est pas entouré de guillemets doubles.)</span><span class="sxs-lookup"><span data-stu-id="5583b-149">`From: Sender, Example <sender.example@contoso.com>` (The display name contains a comma, but is not enclosed in double quotation marks.)</span></span>

- <span data-ttu-id="5583b-150">`From: "Microsoft 365 <sender@contoso.com>"` (La valeur entière est placée de manière incorrecte entre guillemets doubles.)</span><span class="sxs-lookup"><span data-stu-id="5583b-150">`From: "Microsoft 365 <sender@contoso.com>"` (The whole value is incorrectly enclosed in double quotation marks.)</span></span>

- <span data-ttu-id="5583b-151">`From: "Microsoft 365 <sender@contoso.com>" sender@contoso.com` (Le nom complet est présent, mais l’adresse de messagerie n’est pas entourée de crochets pointus.)</span><span class="sxs-lookup"><span data-stu-id="5583b-151">`From: "Microsoft 365 <sender@contoso.com>" sender@contoso.com` (The display name is present, but the email address is not enclosed in angle brackets.)</span></span>

- <span data-ttu-id="5583b-152">`From: Microsoft 365<sender@contoso.com>` (Pas d’espace entre le nom d’affichage et le crochet pointu gauche.)</span><span class="sxs-lookup"><span data-stu-id="5583b-152">`From: Microsoft 365<sender@contoso.com>` (No space between the display name and the left angle bracket.)</span></span>

- <span data-ttu-id="5583b-153">`From: "Microsoft 365"<sender@contoso.com>` (Aucun espace entre les guillemets doubles de fermeture et le crochet pointu gauche.)</span><span class="sxs-lookup"><span data-stu-id="5583b-153">`From: "Microsoft 365"<sender@contoso.com>` (No space between the closing double quotation mark and the left angle bracket.)</span></span>

## <a name="suppress-auto-replies-to-your-custom-domain"></a><span data-ttu-id="5583b-154">Supprimer les réponses automatiques à votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="5583b-154">Suppress auto-replies to your custom domain</span></span>

<span data-ttu-id="5583b-155">Vous ne pouvez pas utiliser la valeur `From: <>` pour supprimer les réponses automatiques.</span><span class="sxs-lookup"><span data-stu-id="5583b-155">You can't use the value `From: <>` to suppress auto-replies.</span></span> <span data-ttu-id="5583b-156">Au lieu de cela, vous devez configurer un enregistrement MX null pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5583b-156">Instead, you need to set up a null MX record for your custom domain.</span></span> <span data-ttu-id="5583b-157">Les réponses automatiques (et toutes les réponses) sont naturellement supprimées, car il n’existe aucune adresse publiée à laquelle le serveur de réponse peut envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="5583b-157">Auto-replies (and all replies) are naturally suppressed because there is no published address that the responding server can send messages to.</span></span>

- <span data-ttu-id="5583b-158">Choisissez un domaine de messagerie qui ne peut pas recevoir de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5583b-158">Choose an email domain that can't receive email.</span></span> <span data-ttu-id="5583b-159">Par exemple, si votre domaine principal est contoso.com, vous pouvez choisir noreply.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5583b-159">For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>

- <span data-ttu-id="5583b-160">L’enregistrement MX null de ce domaine se compose d’un seul point.</span><span class="sxs-lookup"><span data-stu-id="5583b-160">The null MX record for this domain consists of a single period.</span></span>

<span data-ttu-id="5583b-161">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5583b-161">For example:</span></span>

```text
noreply.contoso.com IN MX .
```

<span data-ttu-id="5583b-162">Pour plus d’informations sur la configuration des enregistrements MX, consultez la rubrique [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Microsoft 365](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5583b-162">For more information about setting up MX records, see [Create DNS records at any DNS hosting provider for Microsoft 365](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span>

<span data-ttu-id="5583b-163">Pour plus d’informations sur la publication d’une valeur null MX, voir [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="5583b-163">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>

## <a name="override-from-address-enforcement"></a><span data-ttu-id="5583b-164">Remplacer l’application de l’adresse</span><span class="sxs-lookup"><span data-stu-id="5583b-164">Override From address enforcement</span></span>

<span data-ttu-id="5583b-165">Pour ignorer l’adresse requise pour le courrier électronique entrant, vous pouvez utiliser la liste d’adresses IP autorisées (filtrage des connexions) ou les règles de flux de messagerie (également appelées règles de transport), comme décrit dans [Create Safe sender Lists in Microsoft 365](create-safe-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="5583b-165">To bypass the From address requirements for inbound email, you can use the IP Allow List (connection filtering) or mail flow rules (also known as transport rules) as described in [Create safe sender lists in Microsoft 365](create-safe-sender-lists-in-office-365.md).</span></span>

<span data-ttu-id="5583b-166">Vous ne pouvez pas remplacer l’adresse requise pour le courrier électronique sortant que vous envoyez à partir de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5583b-166">You can't override the From address requirements for outbound email that you send from Microsoft 365.</span></span> <span data-ttu-id="5583b-167">De plus, Outlook.com n’autorisera pas les remplacements, même via la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5583b-167">In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span>

## <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-microsoft-365"></a><span data-ttu-id="5583b-168">Autres moyens de prévenir et de protéger contre les cybercriminels dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5583b-168">Other ways to prevent and protect against cybercrimes in Microsoft 365</span></span>

<span data-ttu-id="5583b-169">Pour plus d’informations sur la façon dont vous pouvez renforcer votre organisation contre le hameçonnage, le courrier indésirable, les violations de données et d’autres menaces, consultez les [10 meilleures façons de sécuriser les plans Microsoft 365 pour les entreprises](../../admin/security-and-compliance/secure-your-business-data.md).</span><span class="sxs-lookup"><span data-stu-id="5583b-169">For more information on how you can strengthen your organization against phishing, spam, data breaches, and other threats, see [Top 10 ways to secure Microsoft 365 for business plans](../../admin/security-and-compliance/secure-your-business-data.md).</span></span>
