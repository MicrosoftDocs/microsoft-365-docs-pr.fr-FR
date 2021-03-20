---
title: Résolution des problèmes d’e-mails envoyés à Microsoft 365
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
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Cet article fournit des informations de dépannage pour les problèmes d’envoi de courrier électronique à des boîtes de réception dans Microsoft 365 & meilleures pratiques en matière de publipostage en bloc pour les clients Microsoft 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 5cebb5ab3f5f4adf321e9c7992fcc5efe40ac2a2
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50908149"
---
# <a name="troubleshooting-mail-sent-to-microsoft-365"></a><span data-ttu-id="2787d-103">Résolution des problèmes d’e-mails envoyés à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2787d-103">Troubleshooting mail sent to Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="2787d-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2787d-104">**Applies to**</span></span>
- [<span data-ttu-id="2787d-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="2787d-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="2787d-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="2787d-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)

<span data-ttu-id="2787d-107">Cet article fournit des informations de dépannage pour les expéditeurs qui rencontrent des problèmes lors de la tentative d’envoi de messages électroniques dans les boîtes de réception dans Microsoft 365 et les meilleures pratiques pour l’envoi en bloc de messages aux clients.</span><span class="sxs-lookup"><span data-stu-id="2787d-107">This article provides troubleshooting information for senders who are experiencing issues when trying to send email to inboxes in Microsoft 365 and best practices for bulk mailing to customers.</span></span>

## <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a><span data-ttu-id="2787d-108">Vous gérez la réputation de l’expéditeur de votre IP et domaine ?</span><span class="sxs-lookup"><span data-stu-id="2787d-108">Are you managing your IP and domain's sending reputation?</span></span>

<span data-ttu-id="2787d-109">Les technologies de filtrage EOP sont conçues pour fournir une protection contre le courrier indésirable pour Microsoft 365 ainsi que d’autres produits Microsoft tels que Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2787d-109">EOP filtering technologies are designed to provide anti-spam protection for Microsoft 365 as well as other Microsoft products like Exchange Server.</span></span> <span data-ttu-id="2787d-110">Nous tirons également parti de SPF, DKIM et DMARC ; des technologies d'authentification de messagerie qui aident à résoudre le problème d'usurpation et d'hameçonnage en vérifiant que le domaine qui envoie l'e-mail est autorisé à le faire.</span><span class="sxs-lookup"><span data-stu-id="2787d-110">We also leverage SPF, DKIM, and DMARC; email authentication technologies that help address the problem of spoofing and phishing by verifying that the domain sending the email is authorized to do so.</span></span> <span data-ttu-id="2787d-111">Le filtrage EOP est affecté par de nombreux facteurs liés à l'IP d'envoi, le domaine, l'authentification, la précision de la liste, les taux de plaintes, le contenu, etc.</span><span class="sxs-lookup"><span data-stu-id="2787d-111">EOP filtering is influenced by a number of factors related to the sending IP, domain, authentication, list accuracy, complaint rates, content and more.</span></span> <span data-ttu-id="2787d-112">Parmi ces facteurs, l'un des facteurs principaux responsable de la baisse de réputation d'un expéditeur et sa capacité à remettre un e-mail est son taux de plainte de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="2787d-112">Of these, one of the principal factors in driving down a sender's reputation and their ability to deliver email is their junk email complaint rate.</span></span>

## <a name="are-you-sending-email-from-new-ip-addresses"></a><span data-ttu-id="2787d-113">Vous envoyez des e-mails depuis de nouvelles adresses IP ?</span><span class="sxs-lookup"><span data-stu-id="2787d-113">Are you sending email from new IP addresses?</span></span>

<span data-ttu-id="2787d-p102">Les adresses IP qui n’ont pas été utilisées précédemment pour envoyer des e-mails n’ont généralement pas de réputation créée dans nos systèmes. Par conséquent, les e-mails provenant de nouvelles adresses IP ont plus tendance à rencontrer des problèmes de remise. Une fois que l’adresse IP a créé une réputation de non envoi de courrier indésirable, EOP permet généralement une meilleure expérience de remise des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="2787d-p102">IP addresses not previously used to send email typically don't have any reputation built up in our systems. As a result, emails from new IPs are more likely to experience delivery issues. Once the IP has built a reputation for not sending spam, EOP will typically allow for a better email delivery experience.</span></span>

<span data-ttu-id="2787d-p103">Les nouvelles adresses IP qui sont ajoutées pour des domaines authentifiés sous des enregistrements SPF existants bénéficient généralement de l’avantage d’hériter de la réputation d’envoi du domaine. Si votre domaine a une bonne réputation d’envoi, les nouvelles adresses IP peuvent expérimenter un temps de montée en puissance plus rapide. Une nouvelle adresse IP pourra être entièrement augmentée au bout de quelques semaines ou plus tôt selon le volume, la précision de la liste et les taux de plaintes de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="2787d-p103">New IPs that are added for domains that are authenticated under existing SPF records typically experience the added benefit of inheriting some of the domain's sending reputation. If your domain has a good sending reputation new IPs may experience a faster ramp up time. A new IP can expect to be fully ramped within a couple of weeks or sooner depending on volume, list accuracy, and junk email complaint rates.</span></span>

## <a name="confirm-that-your-dns-is-set-up-correctly"></a><span data-ttu-id="2787d-120">Confirmer que votre DNS est configuré correctement</span><span class="sxs-lookup"><span data-stu-id="2787d-120">Confirm that your DNS is set up correctly</span></span>

<span data-ttu-id="2787d-121">Pour savoir comment créer et gérer des enregistrements DNS, y compris l’enregistrement MX requis pour le routage du courrier, vous devez contacter votre fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="2787d-121">For instructions about how to create and maintain DNS records, including the MX record required for mail routing, you will need to contact your DNS hosting provider.</span></span>

## <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a><span data-ttu-id="2787d-122">Vérifier que vous ne vous annoncez pas sous la forme d’une adresse IP non routable</span><span class="sxs-lookup"><span data-stu-id="2787d-122">Ensure that you do not advertise yourself as a non-routable IP</span></span>

<span data-ttu-id="2787d-p104">Il se peut que nous n’acceptions pas les e-mails provenant d’expéditeurs dont la recherche DNS inversée a échoué. Dans certains cas, des expéditeurs légitimes s’annoncent de façon incorrecte sous la forme d’une adresse IP routable non Internet lorsqu’ils tentent d’ouvrir une connexion à EOP. Les adresses IP réservées pour le réseau privé (non routable) incluent :</span><span class="sxs-lookup"><span data-stu-id="2787d-p104">We may not accept email from senders who fail a reverse-DNS lookup. In some cases, legitimate senders advertise themselves incorrectly as a non-internet routable IP when attempting to open a connection to EOP. IP addresses that are reserved for private (non-routable) networking include:</span></span>

- <span data-ttu-id="2787d-126">192.168.0.0/16 (ou 192.168.0.0 - 192.168.255.255)</span><span class="sxs-lookup"><span data-stu-id="2787d-126">192.168.0.0/16 (or 192.168.0.0 - 192.168.255.255)</span></span>
- <span data-ttu-id="2787d-127">10.0.0.0/8 (ou 10.0.0.0 - 10.255.255.255)</span><span class="sxs-lookup"><span data-stu-id="2787d-127">10.0.0.0/8 (or 10.0.0.0 - 10.255.255.255)</span></span>
- <span data-ttu-id="2787d-128">172.16.0.0/11 (ou 172.16.0.0 - 172.31.255.255)</span><span class="sxs-lookup"><span data-stu-id="2787d-128">172.16.0.0/11 (or 172.16.0.0 - 172.31.255.255)</span></span>

## <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a><span data-ttu-id="2787d-129">Vous avez reçu une rapport de non-remise (NDR) lors de l’envoi de courriers électroniques à un utilisateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2787d-129">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>

<span data-ttu-id="2787d-p105">Certains problèmes de remise sont dus au blocage de l'adresse IP de l'expéditeur par Microsoft ou à l'identification du compte d'utilisateur comme expéditeur interdit en raison des activité de courrier indésirable précédentes. Si vous pensez que vous avez reçu la notification d'échec de remise par erreur, suivez d'abord toutes les instructions indiquées dans le message de notification d'échec de remise pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="2787d-p105">Some delivery issues are the result of the sender's IP address being blocked by Microsoft or because the user account is identified as banned sender due to previous spam activity. If you believe that you have received the NDR in error, first follow any instructions in the NDR message to resolve the issue.</span></span>

<span data-ttu-id="2787d-132">Pour plus d’informations sur l’erreur que vous avez reçue, consultez la liste des codes d’erreur dans les rapports de [non-remise](/exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online)de courrier électronique dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2787d-132">For more information about the error you received, see the list of error codes in [Email non-delivery reports in Exchange Online](/exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online).</span></span>

 <span data-ttu-id="2787d-133">Par exemple, si vous recevez la NDR suivante, cela indique que l’adresse IP d’envoi a été bloquée par Microsoft :</span><span class="sxs-lookup"><span data-stu-id="2787d-133">For example, if you receive the following NDR, it indicates that the sending IP address was blocked by Microsoft:</span></span>

 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`

<span data-ttu-id="2787d-134">Pour demander la suppression de cette liste, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des [expéditeurs bloqués.](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)</span><span class="sxs-lookup"><span data-stu-id="2787d-134">To request removal from this list, you can [Use the delist portal to remove yourself from the blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>

## <a name="my-email-landed-in-the-recipients-junk-email-folder"></a><span data-ttu-id="2787d-135">Mon courrier électronique a été envoyé dans le dossier Courrier indésirable du destinataire</span><span class="sxs-lookup"><span data-stu-id="2787d-135">My email landed in the recipient's Junk Email folder</span></span>

<span data-ttu-id="2787d-136">Si un message a été incorrectement identifié comme courrier indésirable par EOP, vous pouvez collaborer avec le destinataire pour envoyer ce faux positif à l'équipe d'analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2787d-136">If a message was incorrectly identified as spam by EOP, you can work with the recipient to submit this false positive message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message.</span></span> <span data-ttu-id="2787d-137">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="2787d-137">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a><span data-ttu-id="2787d-138">Le trafic provenant de mon adresse IP est limité par EOP</span><span class="sxs-lookup"><span data-stu-id="2787d-138">Traffic from my IP address is throttled by EOP</span></span>

<span data-ttu-id="2787d-139">Si vous recevez une notification d'échec de remise d'EOP, cela indique que votre adresse IP est limitée par EOP, par exemple :</span><span class="sxs-lookup"><span data-stu-id="2787d-139">If you receive an NDR from EOP that indicates that your IP address is being throttled by EOP, for example:</span></span>

 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`

<span data-ttu-id="2787d-p107">Vous avez reçu une notification d'échec de remise car une activité suspecte a été détectée sur l'adresse IP et a été restreinte temporairement le temps d'effectuer des évaluations supplémentaires. Si la suspicion est désactivée au cours de l'évaluation, cette restriction est bientôt levée.</span><span class="sxs-lookup"><span data-stu-id="2787d-p107">You received the NDR because suspicious activity has been detected from the IP address and it has been temporarily restricted while it is being further evaluated. If the suspicion is cleared through evaluation, this restriction will be lifted shortly.</span></span>

## <a name="i-cant-receive-email-from-senders-in-microsoft-365"></a><span data-ttu-id="2787d-142">Je ne peux pas recevoir de courrier électronique d’expéditeurs dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2787d-142">I can't receive email from senders in Microsoft 365</span></span>

 <span data-ttu-id="2787d-143">Afin de recevoir des messages de la part de nos utilisateurs, assurez-vous que votre réseau autorise les connexions provenant des adresses IP utilisées par EOP dans nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="2787d-143">In order to receive messages from our users, make sure your network allows connections from the IP addresses that EOP uses in our datacenters.</span></span> <span data-ttu-id="2787d-144">Pour plus d’informations, [consultez les adresses IP d’Exchange Online Protection.](../../enterprise/urls-and-ip-address-ranges.md)</span><span class="sxs-lookup"><span data-stu-id="2787d-144">For more information, see [Exchange Online Protection IP addresses](../../enterprise/urls-and-ip-address-ranges.md).</span></span>

## <a name="best-practices-for-bulk-emailing-to-microsoft-365-users"></a><span data-ttu-id="2787d-145">Meilleures pratiques pour l’envoi en bloc d’e-mails aux utilisateurs de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2787d-145">Best practices for bulk emailing to Microsoft 365 users</span></span>

<span data-ttu-id="2787d-146">Si vous effectuez souvent des campagnes de courrier en bloc pour les utilisateurs de Microsoft 365 et que vous souhaitez vous assurer que vos messages électroniques arrivent en toute sécurité et en temps voulu, suivez les conseils de cette section.</span><span class="sxs-lookup"><span data-stu-id="2787d-146">If you often conduct bulk email campaigns to Microsoft 365 users and want to ensure that your emails arrive in a safe and timely manner, follow the tips in this section.</span></span>

### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a><span data-ttu-id="2787d-147">S’assurer que le nom de l’envoi reflète la personne qui envoie le message</span><span class="sxs-lookup"><span data-stu-id="2787d-147">Ensure that the From name reflects who is sending the message</span></span>

<span data-ttu-id="2787d-p109">L'Objet doit être un bref résumé du contenu du message, et le corps du message doit clairement et brièvement indiquer l'objet de l'offre, du service ou du produit. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2787d-p109">The Subject should be a brief summary of what the message is about, and the message body should clearly and succinctly indicate what the offering, service, or product is about. For example:</span></span>

<span data-ttu-id="2787d-150">Correct :</span><span class="sxs-lookup"><span data-stu-id="2787d-150">Correct:</span></span>

> <span data-ttu-id="2787d-151">De : marketing@shoppershandbag.com</span><span class="sxs-lookup"><span data-stu-id="2787d-151">From: marketing@shoppershandbag.com</span></span> <br> <span data-ttu-id="2787d-152">Objet : Catalogue mis à jour pour la période de Noël !</span><span class="sxs-lookup"><span data-stu-id="2787d-152">Subject: Updated catalog for the Christmas season!</span></span>

<span data-ttu-id="2787d-153">Incorrect :</span><span class="sxs-lookup"><span data-stu-id="2787d-153">Incorrect:</span></span>

> <span data-ttu-id="2787d-154">De : someone@outlook.com</span><span class="sxs-lookup"><span data-stu-id="2787d-154">From: someone@outlook.com</span></span> <br> <span data-ttu-id="2787d-155">Objet : Catalogues</span><span class="sxs-lookup"><span data-stu-id="2787d-155">Subject: Catalogs</span></span>

<span data-ttu-id="2787d-156">Plus vous vous présentez et décrivez ce que vous faites de façon claire, moins vos courriers seront bloqués par la plupart des filtres anti-spam.</span><span class="sxs-lookup"><span data-stu-id="2787d-156">The easier you make it for people to know who you are and what you are doing, the less difficulty you will have delivering through most spam filters.</span></span>

### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a><span data-ttu-id="2787d-157">Toujours inclure une option de désinscription dans les e-mails de campagne</span><span class="sxs-lookup"><span data-stu-id="2787d-157">Always include an unsubscribe option in campaign emails</span></span>

<span data-ttu-id="2787d-p110">Les e-mails de marketing, notamment les bulletins d'informations, doivent toujours inclure une option permettant de se désinscrire pour ne plus recevoir de futurs e-mails. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2787d-p110">Marketing emails, especially newsletters, should always include a way of unsubscribing from future emails. For example:</span></span>

 `This email was sent to example@contoso.com by sender@fabrikam.com.`

 `Update Profile/Email Address | Instant removal with SafeUnsubscribe&trade; | Privacy Policy`

<span data-ttu-id="2787d-p111">Certains expéditeurs incluent cette option en demandant aux destinataires d'envoyer un e-mail à un certain alias avec « Se désabonner » dans l'objet. Cela n'est pas préférable à l'exemple en un seul clic ci-dessus. Si vous choisissez de demander aux destinataires d'envoyer un message, assurez-vous que lorsqu'ils cliquent sur le lien, tous les champs requis sont renseignés au préalable.</span><span class="sxs-lookup"><span data-stu-id="2787d-p111">Some senders include this option by requiring recipients to send an email to a certain alias with "Unsubscribe" in the subject. This is not preferable to the one-click example above. If you do choose to require recipients to send a mail, ensure that when they click the link, all the required fields are pre-populated.</span></span>

### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a><span data-ttu-id="2787d-163">Utiliser l’option de contrôle de consentement double pour l’enregistrement à des e-mails de marketing ou à des bulletins d’informations</span><span class="sxs-lookup"><span data-stu-id="2787d-163">Use the double opt-in option for marketing email or newsletter registration</span></span>

<span data-ttu-id="2787d-p112">Cette pratique est recommandée par le secteur si votre entreprise requiert que les utilisateurs enregistrent leurs informations de contact ou les y encourage pour accéder à vos produits ou services. Certaines sociétés ont pris l'habitude d'inscrire automatiquement leurs utilisateurs pour les e-mails de marketing ou les bulletins d'informations électroniques lors du processus d'enregistrement. Néanmoins, cela est considéré comme une pratique marketing discutables dans le monde du filtrage des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="2787d-p112">This industry best practice is recommended if your company requires or encourages users to register their contact information in order to access your product or services. Some companies make it a practice to automatically sign up their users for marketing emails or e-newsletters during the registration process, but this is considered a questionable marketing practice in the world of email filtering.</span></span>

<span data-ttu-id="2787d-166">Au cours du processus d'enregistrement, si la case à cocher « Oui, merci de m'envoyer votre bulletin d'informations » ou « Oui, merci de m'envoyer les offres spéciales » est sélectionnée par défaut, les utilisateurs qui ne font pas assez attention risquent de s'inscrire par inadvertance aux e-mails de marketing ou aux bulletins d'informations qu'ils ne souhaitent pas recevoir.</span><span class="sxs-lookup"><span data-stu-id="2787d-166">During the registration process, if the "Yes, please send me your newsletter" or "Yes, please send me special offers" checkbox is selected by default, users who do not pay close attention may unintentionally sign up for marketing email or newsletters that they do not want to receive.</span></span>

 <span data-ttu-id="2787d-p113">Nous vous recommandons l'option de contrôle de consentement double à la place, ce qui signifie que la case à cocher pour les e-mails de marketing ou les bulletins d'informations est désactivée par défaut. En outre, une fois que le formulaire d'inscription a été envoyé, un e-mail de vérification est envoyé à l'utilisateur avec une URL qui leur permet de confirmer leur décision de recevoir des e-mails de marketing.</span><span class="sxs-lookup"><span data-stu-id="2787d-p113">We recommend the double opt-in option instead, which means that the checkbox for marketing emails or newsletters is unchecked by default. Additionally, once the registration form has been submitted, a verification email is sent to the user with a URL that allows them to confirm their decision to receive marketing emails.</span></span>

 <span data-ttu-id="2787d-169">Cela permet de garantir que seuls les utilisateurs qui souhaitent recevoir des e-mails de marketing sont inscrits pour les e-mails, en désactivant ensuite l'entreprise émettrice de toute pratique discutable.</span><span class="sxs-lookup"><span data-stu-id="2787d-169">This helps ensure that only those users who want to receive marketing email are signed up for the emails, subsequently clearing the sending company of any questionable email marketing practices.</span></span>

### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a><span data-ttu-id="2787d-170">Vérifier que le contenu des messages électroniques est transparent et qu’il est possible de le suivre</span><span class="sxs-lookup"><span data-stu-id="2787d-170">Ensure that email message content is transparent and traceable</span></span>

<span data-ttu-id="2787d-p114">La façon dont les e-mails sont envoyés est aussi importante que leur contenu. Lorsque vous créez le contenu d’un e-mail, utilisez les meilleures pratiques suivantes pour vous assurer que vos e-mails ne seront pas signalés par des services de filtrage des messages électroniques :</span><span class="sxs-lookup"><span data-stu-id="2787d-p114">Just as important as the way the emails are sent is the content they contain. When creating email content, use the following best practices to ensure that your emails will not be flagged by email filtering services:</span></span>

- <span data-ttu-id="2787d-173">Lorsque le message de l'e-mail demande aux destinataires d'ajouter l'expéditeur au carnet d'adresses, il doit clairement indiquer qu'une telle action ne constitue pas une garantie de remise.</span><span class="sxs-lookup"><span data-stu-id="2787d-173">When the email message requests that recipients add the sender to the address book, it should clearly state that such action is not a guarantee of delivery.</span></span>

- <span data-ttu-id="2787d-p115">Les redirections incluses dans le corps du message doivent être similaires et cohérentes et non multiples et variées. Une redirection dans ce contexte est tout élément qui pointe en dehors du message, comme des liens et des documents. Si vous avez de très nombreux liens Se désabonner ou Mettre à jour le profil, ils doivent tous pointer vers le même domaine. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2787d-p115">Redirects included in the body of the message should be similar and consistent, and not multiple and varied. A redirect in this context is anything that points away from the message, such as links and documents. If you have a lot of advertising or Unsubscribe links or Update the Profile links, they should all point to the same domain. For example:</span></span>

  <span data-ttu-id="2787d-178">Correct (tous les domaines sont identiques) :</span><span class="sxs-lookup"><span data-stu-id="2787d-178">Correct (all domains are the same):</span></span>

  `unsubscribe.bulkmailer.com`

  `profile.bulkmailer.com`

  `options.bulkmailer.com`

  <span data-ttu-id="2787d-179">Incorrect (tous les domaines sont différents) :</span><span class="sxs-lookup"><span data-stu-id="2787d-179">Incorrect (all domains are different):</span></span>

  `unsubscribe.bulkmailer.com`

  `profile.excite.com`

  `options.yahoo.com`

- <span data-ttu-id="2787d-180">Évitez les images et les pièces jointes volumineuses, ou les messages contenant uniquement une image.</span><span class="sxs-lookup"><span data-stu-id="2787d-180">Avoid content with large images and attachments, or messages that are solely composed of an image.</span></span>

- <span data-ttu-id="2787d-181">Vos paramètres publics de confidentialité ou P3P doivent signaler clairement la présence des pixels de suivi (bogues ou balises web).</span><span class="sxs-lookup"><span data-stu-id="2787d-181">Your public privacy or P3P settings should clearly state the presence of tracking pixels (web bugs or beacons).</span></span>

### <a name="remove-incorrect-email-aliases-from-your-databases"></a><span data-ttu-id="2787d-182">Supprimer les alias de messagerie incorrects de vos bases de données</span><span class="sxs-lookup"><span data-stu-id="2787d-182">Remove incorrect email aliases from your databases</span></span>

<span data-ttu-id="2787d-p116">Les alias de messagerie de votre base de données qui créent un renvoi sont inutiles et exposent vos messages électroniques sortants à des risques d’examen approfondi par les services de filtrage de courrier électronique. Assurez-vous que votre base de données de messagerie est à jour.</span><span class="sxs-lookup"><span data-stu-id="2787d-p116">Any email alias in your database that creates a bounce-back is unnecessary and puts your outbound emails at risk for further scrutiny by email filtering services. Ensure that your email database is up-to-date.</span></span>