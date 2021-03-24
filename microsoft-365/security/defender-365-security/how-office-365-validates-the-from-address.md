---
title: Comment EOP valide l’adresse De pour empêcher le hameçonnage
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les types d’adresses de messagerie acceptées ou rejetées par Exchange Online Protection (EOP) et Outlook.com pour empêcher le hameçonnage.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 5a02313bf8c36fe0be91340e421c69a8dc5c0842
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063358"
---
# <a name="how-eop-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="896e5-103">Comment EOP valide l’adresse De pour empêcher le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="896e5-103">How EOP validates the From address to prevent phishing</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="896e5-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="896e5-104">**Applies to**</span></span>
- [<span data-ttu-id="896e5-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="896e5-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="896e5-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="896e5-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="896e5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="896e5-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="896e5-108">Les attaques par hameçonnage sont une menace constante pour toute organisation de messagerie.</span><span class="sxs-lookup"><span data-stu-id="896e5-108">Phishing attacks are a constant threat to any email organization.</span></span> <span data-ttu-id="896e5-109">Outre l’utilisation d’adresses e-mail d’expéditeur falsifiées [(falsifiées),](anti-spoofing-protection.md)les personnes malveillantes utilisent souvent des valeurs dans l’adresse De qui ne respectent pas les normes Internet.</span><span class="sxs-lookup"><span data-stu-id="896e5-109">In addition to using [spoofed (forged) sender email addresses](anti-spoofing-protection.md), attackers often use values in the From address that violate internet standards.</span></span> <span data-ttu-id="896e5-110">Pour éviter ce type d’hameçonnage, Exchange Online Protection (EOP) et Outlook.com requièrent désormais que les messages entrants incluent une adresse de provenance conforme À la norme RFC, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="896e5-110">To help prevent this type of phishing, Exchange Online Protection (EOP) and Outlook.com now require inbound messages to include an RFC-compliant From address as described in this article.</span></span> <span data-ttu-id="896e5-111">Cette application a été activée en novembre 2017.</span><span class="sxs-lookup"><span data-stu-id="896e5-111">This enforcement was enabled in November 2017.</span></span>

<span data-ttu-id="896e5-112">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="896e5-112">**Notes**:</span></span>

- <span data-ttu-id="896e5-113">Si vous recevez régulièrement des messages électroniques provenant d’organisations dont les adresses ont été mal renseignées, comme décrit dans cet article, encouragez ces organisations à mettre à jour leurs serveurs de messagerie pour se conformer aux normes de sécurité modernes.</span><span class="sxs-lookup"><span data-stu-id="896e5-113">If you regularly receive email from organizations that have malformed From addresses as described in this article, encourage these organizations to update their email servers to comply with modern security standards.</span></span>

- <span data-ttu-id="896e5-114">Le champ Expéditeur associé (utilisé par les listes d’envoi de la part de et de publipostage) n’est pas affecté par ces exigences.</span><span class="sxs-lookup"><span data-stu-id="896e5-114">The related Sender field (used by Send on Behalf and mailing lists) isn't affected by these requirements.</span></span> <span data-ttu-id="896e5-115">Pour plus d’informations, consultez le billet de blog suivant : Que voulons-nous dire lorsque nous faisons référence à l'« expéditeur » [d’un e-mail ?](/archive/blogs/tzink/what-do-we-mean-when-we-refer-to-the-sender-of-an-email)</span><span class="sxs-lookup"><span data-stu-id="896e5-115">For more information, see the following blog post: [What do we mean when we refer to the 'sender' of an email?](/archive/blogs/tzink/what-do-we-mean-when-we-refer-to-the-sender-of-an-email).</span></span>

## <a name="an-overview-of-email-message-standards"></a><span data-ttu-id="896e5-116">Vue d’ensemble des normes de message électronique</span><span class="sxs-lookup"><span data-stu-id="896e5-116">An overview of email message standards</span></span>

<span data-ttu-id="896e5-117">Un message électronique SMTP standard est constitué d’une *enveloppe de message* et d’un contenu de message.</span><span class="sxs-lookup"><span data-stu-id="896e5-117">A standard SMTP email message consists of a *message envelope* and message content.</span></span> <span data-ttu-id="896e5-118">L’enveloppe de message contient les informations requises pour transmettre et remettre le message entre des serveurs SMTP.</span><span class="sxs-lookup"><span data-stu-id="896e5-118">The message envelope contains information that's required for transmitting and delivering the message between SMTP servers.</span></span> <span data-ttu-id="896e5-119">Le contenu du message comporte les champs d’en-tête de message (collectivement appelés l’*en-tête de message*) et le corps du message.</span><span class="sxs-lookup"><span data-stu-id="896e5-119">The message content contains message header fields (collectively called the *message header*) and the message body.</span></span> <span data-ttu-id="896e5-120">L’enveloppe de message est décrite dans [la RFC 5321](https://tools.ietf.org/html/rfc5321)et l’en-tête du message est décrit dans [la RFC 5322](https://tools.ietf.org/html/rfc5322).</span><span class="sxs-lookup"><span data-stu-id="896e5-120">The message envelope is described in [RFC 5321](https://tools.ietf.org/html/rfc5321), and the message header is described in [RFC 5322](https://tools.ietf.org/html/rfc5322).</span></span> <span data-ttu-id="896e5-121">Les destinataires ne voient jamais l’enveloppe de message réelle, car elle est générée par le processus de transmission du message et ne fait pas réellement partie du message.</span><span class="sxs-lookup"><span data-stu-id="896e5-121">Recipients never see the actual message envelope because it's generated by the message transmission process, and it isn't actually part of the message.</span></span>

- <span data-ttu-id="896e5-122">L’adresse (également appelée adresse MAIL FROM, expéditeur P1 ou expéditeur d’enveloppe) est l’adresse de messagerie utilisée dans la `5321.MailFrom` transmission SMTP du message. </span><span class="sxs-lookup"><span data-stu-id="896e5-122">The `5321.MailFrom` address (also known as the **MAIL FROM** address, P1 sender, or envelope sender) is the email address that's used in the SMTP transmission of the message.</span></span> <span data-ttu-id="896e5-123">Cette adresse de messagerie est généralement enregistrée dans le champ **d’en-tête Return-Path** dans l’en-tête du message (bien qu’il soit possible pour l’expéditeur de désigner une autre adresse de messagerie **Return-Path).**</span><span class="sxs-lookup"><span data-stu-id="896e5-123">This email address is typically recorded in the **Return-Path** header field in the message header (although it's possible for the sender to designate a different **Return-Path** email address).</span></span>

- <span data-ttu-id="896e5-124">L’adresse e-mail (également appelée adresse de provenance ou expéditeur P2) est l’adresse de messagerie dans le champ d’en-tête De et l’adresse de messagerie de l’expéditeur qui s’affiche dans les clients de `5322.From` messagerie. </span><span class="sxs-lookup"><span data-stu-id="896e5-124">The `5322.From` (also known as the From address or P2 sender) is the email address in the **From** header field, and is the sender's email address that's displayed in email clients.</span></span> <span data-ttu-id="896e5-125">L’adresse de provenance est au centre des exigences de cet article.</span><span class="sxs-lookup"><span data-stu-id="896e5-125">The From address is the focus of the requirements in this article.</span></span>

<span data-ttu-id="896e5-126">L’adresse De est définie en détail sur plusieurs RFC (par exemple, les sections RFC 5322 3.2.3, 3.4 et 3.4.1 et [RFC 3696](https://tools.ietf.org/html/rfc3696)).</span><span class="sxs-lookup"><span data-stu-id="896e5-126">The From address is defined in detail across several RFCs (for example, RFC 5322 sections 3.2.3, 3.4, and 3.4.1, and [RFC 3696](https://tools.ietf.org/html/rfc3696)).</span></span> <span data-ttu-id="896e5-127">Il existe de nombreuses variantes sur l’adressan et ce qui est considéré comme valide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="896e5-127">There are many variations on addressing and what's considered valid or invalid.</span></span> <span data-ttu-id="896e5-128">Pour des raisons de simplicité, nous vous recommandons le format et les définitions suivants :</span><span class="sxs-lookup"><span data-stu-id="896e5-128">To keep it simple, we recommend the following format and definitions:</span></span>

`From: "Display Name" <EmailAddress>`

- <span data-ttu-id="896e5-129">**Nom complet**: expression facultative qui décrit le propriétaire de l’adresse e-mail.</span><span class="sxs-lookup"><span data-stu-id="896e5-129">**Display Name**: An optional phrase that describes the owner of the email address.</span></span>

  - <span data-ttu-id="896e5-130">Nous vous recommandons de toujours entourer le nom complet de guillemets doubles (« ) comme illustré.</span><span class="sxs-lookup"><span data-stu-id="896e5-130">We recommend that you always enclose the display name in double quotation marks (") as shown.</span></span> <span data-ttu-id="896e5-131">Si le nom complet contient  une virgule, vous devez mettre la chaîne entre guillemets doubles par RFC 5322.</span><span class="sxs-lookup"><span data-stu-id="896e5-131">If the display name contains a comma, you _must_ enclose the string in double quotation marks per RFC 5322.</span></span>
  - <span data-ttu-id="896e5-132">Si l’adresse De comprend un nom d’affichage, la valeur EmailAddress doit être entre crochets (< >) comme illustré.</span><span class="sxs-lookup"><span data-stu-id="896e5-132">If the From address includes a display name, the EmailAddress value must be enclosed in angle brackets (< >) as shown.</span></span>
  - <span data-ttu-id="896e5-133">Microsoft recommande vivement d’insérer un espace entre le nom complet et l’adresse e-mail.</span><span class="sxs-lookup"><span data-stu-id="896e5-133">Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>

- <span data-ttu-id="896e5-134">**EmailAddress**: une adresse de messagerie utilise le format `local-part@domain` :</span><span class="sxs-lookup"><span data-stu-id="896e5-134">**EmailAddress**: An email address uses the format `local-part@domain`:</span></span>

  - <span data-ttu-id="896e5-135">**partie locale :** chaîne qui identifie la boîte aux lettres associée à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="896e5-135">**local-part**: A string that identifies the mailbox associated with the address.</span></span> <span data-ttu-id="896e5-136">Cette valeur est unique dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="896e5-136">This value is unique within the domain.</span></span> <span data-ttu-id="896e5-137">Souvent, le nom d’utilisateur ou le GUID du propriétaire de la boîte aux lettres est utilisé.</span><span class="sxs-lookup"><span data-stu-id="896e5-137">Often, the mailbox owner's username or GUID is used.</span></span>
  - <span data-ttu-id="896e5-138">**domaine**: nom de domaine complet (FQDN) du serveur de messagerie qui héberge la boîte aux lettres identifiée par la partie locale de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="896e5-138">**domain**: The fully qualified domain name (FQDN) of the email server that hosts the mailbox identified by the local-part of the email address.</span></span>

  <span data-ttu-id="896e5-139">Voici quelques considérations supplémentaires pour la valeur EmailAddress :</span><span class="sxs-lookup"><span data-stu-id="896e5-139">These are some additional considerations for the EmailAddress value:</span></span>

  - <span data-ttu-id="896e5-140">Une seule adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="896e5-140">Only one email address.</span></span>
  - <span data-ttu-id="896e5-141">Nous vous recommandons de ne pas séparer les crochets pointants par des espaces.</span><span class="sxs-lookup"><span data-stu-id="896e5-141">We recommend that you do not separate the angle brackets with spaces.</span></span>
  - <span data-ttu-id="896e5-142">N’incluez pas de texte supplémentaire après l’adresse e-mail.</span><span class="sxs-lookup"><span data-stu-id="896e5-142">Don't include additional text after the email address.</span></span>

## <a name="examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="896e5-143">Exemples d’adresses De valides et non valides</span><span class="sxs-lookup"><span data-stu-id="896e5-143">Examples of valid and invalid From addresses</span></span>

<span data-ttu-id="896e5-144">Les adresses de messagerie De suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="896e5-144">The following From email addresses are valid:</span></span>

- `From: sender@contoso.com`

- `From: <sender@contoso.com>`

- <span data-ttu-id="896e5-145">`From: < sender@contoso.com >` (Non recommandé, car il existe des espaces entre les crochets et l’adresse e-mail.)</span><span class="sxs-lookup"><span data-stu-id="896e5-145">`From: < sender@contoso.com >` (Not recommended because there are spaces between the angle brackets and the email address.)</span></span>

- `From: "Sender, Example" <sender.example@contoso.com>`

- `From: "Microsoft 365" <sender@contoso.com>`

- <span data-ttu-id="896e5-146">`From: Microsoft 365 <sender@contoso.com>` (Non recommandé, car le nom complet n’est pas entouré de guillemets doubles.)</span><span class="sxs-lookup"><span data-stu-id="896e5-146">`From: Microsoft 365 <sender@contoso.com>` (Not recommended because the display name is not enclosed in double quotation marks.)</span></span>

<span data-ttu-id="896e5-147">Les adresses de messagerie De suivantes ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="896e5-147">The following From email addresses are invalid:</span></span>

- <span data-ttu-id="896e5-148">**Adresse De non :** certains messages automatisés n’incluent pas d’adresse de provenance.</span><span class="sxs-lookup"><span data-stu-id="896e5-148">**No From address**: Some automated messages don't include a From address.</span></span> <span data-ttu-id="896e5-149">Dans le passé, lorsque Microsoft 365 ou Outlook.com recevait un message sans adresse de provenance, le service ajoutait l’adresse De : par défaut suivante pour rendre le message livrable :</span><span class="sxs-lookup"><span data-stu-id="896e5-149">In the past, when Microsoft 365 or Outlook.com received a message without a From address, the service added the following default From: address to make the message deliverable:</span></span>

  `From: <>`

  <span data-ttu-id="896e5-150">À présent, les messages dont l’adresse de provenance est vide ne sont plus acceptés.</span><span class="sxs-lookup"><span data-stu-id="896e5-150">Now, messages with a blank From address are no longer accepted.</span></span>

- <span data-ttu-id="896e5-151">`From: Microsoft 365 sender@contoso.com` (Le nom complet est présent, mais l’adresse e-mail n’est pas entre crochets.)</span><span class="sxs-lookup"><span data-stu-id="896e5-151">`From: Microsoft 365 sender@contoso.com` (The display name is present, but the email address is not enclosed in angle brackets.)</span></span>

- <span data-ttu-id="896e5-152">`From: "Microsoft 365" <sender@contoso.com> (Sent by a process)` (Texte après l’adresse e-mail.)</span><span class="sxs-lookup"><span data-stu-id="896e5-152">`From: "Microsoft 365" <sender@contoso.com> (Sent by a process)` (Text after the email address.)</span></span>

- <span data-ttu-id="896e5-153">`From: Sender, Example <sender.example@contoso.com>` (Le nom complet contient une virgule, mais n’est pas entre guillemets doubles.)</span><span class="sxs-lookup"><span data-stu-id="896e5-153">`From: Sender, Example <sender.example@contoso.com>` (The display name contains a comma, but is not enclosed in double quotation marks.)</span></span>

- <span data-ttu-id="896e5-154">`From: "Microsoft 365 <sender@contoso.com>"` (La valeur entière est incorrectement entourée de guillemets doubles.)</span><span class="sxs-lookup"><span data-stu-id="896e5-154">`From: "Microsoft 365 <sender@contoso.com>"` (The whole value is incorrectly enclosed in double quotation marks.)</span></span>

- <span data-ttu-id="896e5-155">`From: "Microsoft 365 <sender@contoso.com>" sender@contoso.com` (Le nom complet est présent, mais l’adresse e-mail n’est pas entre crochets.)</span><span class="sxs-lookup"><span data-stu-id="896e5-155">`From: "Microsoft 365 <sender@contoso.com>" sender@contoso.com` (The display name is present, but the email address is not enclosed in angle brackets.)</span></span>

- <span data-ttu-id="896e5-156">`From: Microsoft 365<sender@contoso.com>` (Aucun espace entre le nom d’affichage et le crochet angle gauche.)</span><span class="sxs-lookup"><span data-stu-id="896e5-156">`From: Microsoft 365<sender@contoso.com>` (No space between the display name and the left angle bracket.)</span></span>

- <span data-ttu-id="896e5-157">`From: "Microsoft 365"<sender@contoso.com>` (Aucun espace entre les guillemets fermants et le crochet angle gauche.)</span><span class="sxs-lookup"><span data-stu-id="896e5-157">`From: "Microsoft 365"<sender@contoso.com>` (No space between the closing double quotation mark and the left angle bracket.)</span></span>

## <a name="suppress-auto-replies-to-your-custom-domain"></a><span data-ttu-id="896e5-158">Supprimer les réponses automatiques à votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="896e5-158">Suppress auto-replies to your custom domain</span></span>

<span data-ttu-id="896e5-159">Vous ne pouvez pas utiliser la valeur pour `From: <>` supprimer les réponses automatiques.</span><span class="sxs-lookup"><span data-stu-id="896e5-159">You can't use the value `From: <>` to suppress auto-replies.</span></span> <span data-ttu-id="896e5-160">Au lieu de cela, vous devez configurer un enregistrement MX null pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="896e5-160">Instead, you need to set up a null MX record for your custom domain.</span></span> <span data-ttu-id="896e5-161">Les réponses automatiques (et toutes les réponses) sont supprimées naturellement, car il n’existe aucune adresse publiée à qui le serveur répondant peut envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="896e5-161">Auto-replies (and all replies) are naturally suppressed because there is no published address that the responding server can send messages to.</span></span>

- <span data-ttu-id="896e5-162">Choisissez un domaine de messagerie qui ne peut pas recevoir de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="896e5-162">Choose an email domain that can't receive email.</span></span> <span data-ttu-id="896e5-163">Par exemple, si votre domaine principal est contoso.com, vous pouvez choisir noreply.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="896e5-163">For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>

- <span data-ttu-id="896e5-164">L’enregistrement MX null pour ce domaine se compose d’un point unique.</span><span class="sxs-lookup"><span data-stu-id="896e5-164">The null MX record for this domain consists of a single period.</span></span>

<span data-ttu-id="896e5-165">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="896e5-165">For example:</span></span>

```text
noreply.contoso.com IN MX .
```

<span data-ttu-id="896e5-166">Pour plus d’informations sur la configuration des enregistrements MX, voir Créer des enregistrements DNS chez un fournisseur d’hébergement [DNS pour Microsoft 365.](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span><span class="sxs-lookup"><span data-stu-id="896e5-166">For more information about setting up MX records, see [Create DNS records at any DNS hosting provider for Microsoft 365](../../admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span>

<span data-ttu-id="896e5-167">Pour plus d’informations sur la publication d’un MX null, voir [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="896e5-167">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>

## <a name="override-from-address-enforcement"></a><span data-ttu-id="896e5-168">Remplacer l’application de l’adresse</span><span class="sxs-lookup"><span data-stu-id="896e5-168">Override From address enforcement</span></span>

<span data-ttu-id="896e5-169">Pour contourner les exigences d’adresse De pour le courrier entrant, vous pouvez utiliser la liste d’adresses IP (filtrage des connexions) ou les règles de flux de messagerie (également appelées règles de transport) comme décrit dans Créer des listes d’expéditeurs sûrs dans [Microsoft 365.](create-safe-sender-lists-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="896e5-169">To bypass the From address requirements for inbound email, you can use the IP Allow List (connection filtering) or mail flow rules (also known as transport rules) as described in [Create safe sender lists in Microsoft 365](create-safe-sender-lists-in-office-365.md).</span></span>

<span data-ttu-id="896e5-170">Vous ne pouvez pas remplacer les exigences d’adresse de provenance pour les messages sortants que vous envoyez à partir de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="896e5-170">You can't override the From address requirements for outbound email that you send from Microsoft 365.</span></span> <span data-ttu-id="896e5-171">En outre, Outlook.com n’autorise pas les remplacements de quelque type que ce soit, même par le biais de la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="896e5-171">In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span>

## <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-microsoft-365"></a><span data-ttu-id="896e5-172">Autres méthodes de prévention et de protection contre les cybercriminels dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="896e5-172">Other ways to prevent and protect against cybercrimes in Microsoft 365</span></span>

<span data-ttu-id="896e5-173">Pour plus d’informations sur la façon de renforcer votre organisation contre le hameçonnage, le courrier indésirable, les violations de données et d’autres menaces, voir les 10 principales façons de sécuriser les [plans Microsoft 365](../../admin/security-and-compliance/secure-your-business-data.md)pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="896e5-173">For more information on how you can strengthen your organization against phishing, spam, data breaches, and other threats, see [Top 10 ways to secure Microsoft 365 for business plans](../../admin/security-and-compliance/secure-your-business-data.md).</span></span>