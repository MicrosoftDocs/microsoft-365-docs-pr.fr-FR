---
title: Résolution des problèmes de messages envoyés à Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
description: Cet article fournit des informations de dépannage pour les expéditeurs qui rencontrent des problèmes lors de l'envoi d'e-mail à des boîtes de réception dans Office 365 et les meilleures pratiques pour l'envoi de courrier en nombre à des clients Office 365.
ms.openlocfilehash: b87b0745c95cd043987f49ed7f21118339d3e592
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38030698"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a><span data-ttu-id="63b73-103">Résolution des problèmes de messages envoyés à Office 365</span><span class="sxs-lookup"><span data-stu-id="63b73-103">Troubleshooting mail sent to Office 365</span></span>

<span data-ttu-id="63b73-104">Cet article fournit des informations de dépannage pour les expéditeurs qui rencontrent des problèmes lors de l’envoi d’e-mail à des boîtes de réception dans Office 365 et les meilleures pratiques pour l’envoi de courrier en nombre à des clients Office 365.</span><span class="sxs-lookup"><span data-stu-id="63b73-104">This article provides troubleshooting information for senders who are experiencing issues when trying to send email to inboxes in Office 365 and best practices for bulk mailing to Office 365 customers.</span></span>

## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a><span data-ttu-id="63b73-105">Résolution de problèmes courants liés à la remise de courrier à Office 365</span><span class="sxs-lookup"><span data-stu-id="63b73-105">Troubleshooting common problems with mail delivery to Office 365</span></span>

<span data-ttu-id="63b73-106">Choisissez un de ces problèmes fréquemment rencontrés.</span><span class="sxs-lookup"><span data-stu-id="63b73-106">Choose from one of these commonly encountered issues.</span></span>

- [<span data-ttu-id="63b73-107">Vous gérez la réputation de l'expéditeur de votre IP et domaine ?</span><span class="sxs-lookup"><span data-stu-id="63b73-107">Are you managing your IP and domain's sending reputation?</span></span>](#are-you-managing-your-ip-and-domains-sending-reputation)

- [<span data-ttu-id="63b73-108">Vous envoyez des e-mails depuis de nouvelles adresses IP ?</span><span class="sxs-lookup"><span data-stu-id="63b73-108">Are you sending email from new IP addresses?</span></span>](#are-you-sending-email-from-new-ip-addresses)

- [<span data-ttu-id="63b73-109">Confirmer que votre DNS est configuré correctement</span><span class="sxs-lookup"><span data-stu-id="63b73-109">Confirm that your DNS is set up correctly</span></span>](#confirm-that-your-dns-is-set-up-correctly)

- [<span data-ttu-id="63b73-110">Vérifier que vous ne vous annoncez pas sous la forme d'une adresse IP non routable</span><span class="sxs-lookup"><span data-stu-id="63b73-110">Ensure that you do not advertise yourself as a non-routable IP</span></span>](#ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip)

- [<span data-ttu-id="63b73-111">Vous avez reçu une notification d'échec de remise lors de l'envoi de messages électroniques à un utilisateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="63b73-111">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>](#you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365)

- [<span data-ttu-id="63b73-112">Mon e-mail s'est retrouvé dans le dossier du courrier indésirable du destinataire dans EOP</span><span class="sxs-lookup"><span data-stu-id="63b73-112">My email landed in the recipient's junk folder in EOP</span></span>](#my-email-landed-in-the-recipients-junk-folder-in-eop)

- [<span data-ttu-id="63b73-113">Le trafic provenant de mon adresse IP est limité par EOP</span><span class="sxs-lookup"><span data-stu-id="63b73-113">Traffic from my IP address is throttled by EOP</span></span>](#traffic-from-my-ip-address-is-throttled-by-eop)

### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a><span data-ttu-id="63b73-114">Vous gérez la réputation de l’expéditeur de votre IP et domaine ?</span><span class="sxs-lookup"><span data-stu-id="63b73-114">Are you managing your IP and domain's sending reputation?</span></span>

<span data-ttu-id="63b73-p101">Les technologies de filtrage EOP sont conçues pour fournir des protections contre le courrier indésirable pour Microsoft Office 365 ainsi que d’autres produits Microsoft tels que Exchange Server, Microsoft Office Outlook et Windows Live Mail. Nous tirons également parti de SPF, DKIM et DMARC ; des technologies d’authentification de messagerie qui aident à résoudre le problème d’usurpation et d’hameçonnage en vérifiant que le domaine qui envoie l’e-mail est autorisé à le faire. Le filtrage EOP est affecté par de nombreux facteurs liés à l’IP d’envoi, le domaine, l’authentification, la précision de la liste, les taux de plaintes, le contenu, etc. Parmi ces facteurs, l’un des facteurs principaux responsable de la baisse de réputation d’un expéditeur et sa capacité à remettre un e-mail est son taux de plainte de courrier indésirable. </span><span class="sxs-lookup"><span data-stu-id="63b73-p101">EOP filtering technologies are designed to provide anti-spam protections for Microsoft Office 365 as well as other Microsoft products like Exchange Server, Microsoft Office Outlook, and Windows Live Mail. We also leverage SPF, DKIM, and DMARC; email authentication technologies that help address the problem of spoofing and phishing by verifying that the domain sending the email is authorized to do so. EOP filtering is influenced by a number of factors related to the sending IP, domain, authentication, list accuracy, complaint rates, content and more. Of these, one of the principal factors in driving down a sender's reputation and their ability to deliver email is their junk email complaint rate.</span></span>

### <a name="are-you-sending-email-from-new-ip-addresses"></a><span data-ttu-id="63b73-119">Vous envoyez des e-mails depuis de nouvelles adresses IP ?</span><span class="sxs-lookup"><span data-stu-id="63b73-119">Are you sending email from new IP addresses?</span></span>

<span data-ttu-id="63b73-p102">Les adresses IP qui n’ont pas été utilisées précédemment pour envoyer des e-mails n’ont généralement pas de réputation créée dans nos systèmes. Par conséquent, les e-mails provenant de nouvelles adresses IP ont plus tendance à rencontrer des problèmes de remise. Une fois que l’adresse IP a créé une réputation de non envoi de courrier indésirable, EOP permet généralement une meilleure expérience de remise des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="63b73-p102">IP addresses not previously used to send email typically don't have any reputation built up in our systems. As a result, emails from new IPs are more likely to experience delivery issues. Once the IP has built a reputation for not sending spam, EOP will typically allow for a better email delivery experience.</span></span>

<span data-ttu-id="63b73-p103">Les nouvelles adresses IP qui sont ajoutées pour des domaines authentifiés sous des enregistrements SPF existants bénéficient généralement de l’avantage d’hériter de la réputation d’envoi du domaine. Si votre domaine a une bonne réputation d’envoi, les nouvelles adresses IP peuvent expérimenter un temps de montée en puissance plus rapide. Une nouvelle adresse IP pourra être entièrement augmentée au bout de quelques semaines ou plus tôt selon le volume, la précision de la liste et les taux de plaintes de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="63b73-p103">New IPs that are added for domains that are authenticated under existing SPF records typically experience the added benefit of inheriting some of the domain's sending reputation. If your domain has a good sending reputation new IPs may experience a faster ramp up time. A new IP can expect to be fully ramped within a couple of weeks or sooner depending on volume, list accuracy, and junk email complaint rates.</span></span>

### <a name="confirm-that-your-dns-is-set-up-correctly"></a><span data-ttu-id="63b73-126">Confirmer que votre DNS est configuré correctement</span><span class="sxs-lookup"><span data-stu-id="63b73-126">Confirm that your DNS is set up correctly</span></span>

<span data-ttu-id="63b73-127">Pour savoir comment créer et gérer des enregistrements DNS, y compris l’enregistrement MX requis pour le routage du courrier, vous devez contacter votre fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="63b73-127">For instructions about how to create and maintain DNS records, including the MX record required for mail routing, you will need to contact your DNS hosting provider.</span></span>

### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a><span data-ttu-id="63b73-128">Vérifier que vous ne vous annoncez pas sous la forme d’une adresse IP non routable</span><span class="sxs-lookup"><span data-stu-id="63b73-128">Ensure that you do not advertise yourself as a non-routable IP</span></span>

<span data-ttu-id="63b73-p104">Il se peut que nous n’acceptions pas les e-mails provenant d’expéditeurs dont la recherche DNS inversée a échoué. Dans certains cas, des expéditeurs légitimes s’annoncent de façon incorrecte sous la forme d’une adresse IP routable non Internet lorsqu’ils tentent d’ouvrir une connexion à EOP. Les adresses IP réservées pour le réseau privé (non routable) incluent :</span><span class="sxs-lookup"><span data-stu-id="63b73-p104">We may not accept email from senders who fail a reverse-DNS lookup. In some cases, legitimate senders advertise themselves incorrectly as a non-internet routable IP when attempting to open a connection to EOP. IP addresses that are reserved for private (non-routable) networking include:</span></span>

- <span data-ttu-id="63b73-132">192.168.0.0/16 (ou 192.168.0.0 - 192.168.255.255)</span><span class="sxs-lookup"><span data-stu-id="63b73-132">192.168.0.0/16 (or 192.168.0.0 - 192.168.255.255)</span></span>

- <span data-ttu-id="63b73-133">10.0.0.0/8 (ou 10.0.0.0 - 10.255.255.255)</span><span class="sxs-lookup"><span data-stu-id="63b73-133">10.0.0.0/8 (or 10.0.0.0 - 10.255.255.255)</span></span>

- <span data-ttu-id="63b73-134">172.16.0.0/11 (ou 172.16.0.0 - 172.31.255.255)</span><span class="sxs-lookup"><span data-stu-id="63b73-134">172.16.0.0/11 (or 172.16.0.0 - 172.31.255.255)</span></span>

### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a><span data-ttu-id="63b73-135">Vous avez reçu une notification d’échec de remise lors de l’envoi d’un message électronique à un utilisateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="63b73-135">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>

<span data-ttu-id="63b73-p105">Certains problèmes de remise sont dus au blocage de l'adresse IP de l'expéditeur par Microsoft ou à l'identification du compte d'utilisateur comme expéditeur interdit en raison des activité de courrier indésirable précédentes. Si vous pensez que vous avez reçu la notification d'échec de remise par erreur, suivez d'abord toutes les instructions indiquées dans le message de notification d'échec de remise pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="63b73-p105">Some delivery issues are the result of the sender's IP address being blocked by Microsoft or because the user account is identified as banned sender due to previous spam activity. If you believe that you have received the NDR in error, first follow any instructions in the NDR message to resolve the issue.</span></span>

<span data-ttu-id="63b73-138">Pour plus d'informations sur l'erreur que vous avez reçue, consultez la liste complète des codes d'erreur SMTP dans [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](https://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span><span class="sxs-lookup"><span data-stu-id="63b73-138">For more information about the error you received, see the complete list of SMTP error codes in [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](https://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span></span>

 <span data-ttu-id="63b73-139">Par exemple, si vous recevez la notification d'échec de remise suivante, elle indique que l'adresse IP d'envoi a été bloquée par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63b73-139">For example, if you receive the following NDR, it indicates that the sending IP address was blocked by Microsoft.</span></span>

 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`

<span data-ttu-id="63b73-140">Pour demander la suppression de cette liste, vous pouvez [Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span><span class="sxs-lookup"><span data-stu-id="63b73-140">To request removal from this list, you can [Use the delist portal to remove yourself from the Office 365 blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>

### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a><span data-ttu-id="63b73-141">Mon e-mail s'est retrouvé dans le dossier du courrier indésirable du destinataire dans EOP</span><span class="sxs-lookup"><span data-stu-id="63b73-141">My email landed in the recipient's junk folder in EOP</span></span>

<span data-ttu-id="63b73-p106">Si un message a été incorrectement identifié comme courrier indésirable par EOP, vous pouvez collaborer avec le destinataire pour envoyer ce faux positif à l’équipe d’analyse du courrier indésirable de Microsoft. Selon les résultats de l’analyse, les règles de filtrage de contenu du courrier indésirable du service peuvent être ajustées pour autoriser le message. Vous utilisez la messagerie pour envoyer à Microsoft des messages qui ne devraient pas être classés comme courrier indésirable. Ce faisant, veillez à respecter les étapes de la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="63b73-p106">If a message was incorrectly identified as spam by EOP, you can work with the recipient to submit this false positive message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message. Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through. You use email to submit messages to Microsoft that should not be classified as spam. When doing so, be sure to use the steps in the following procedure.</span></span>

### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a><span data-ttu-id="63b73-146">Pour utiliser du courrier électronique pour soumettre des messages faux positifs à l’équipe d’analyse du courrier indésirable de Microsoft</span><span class="sxs-lookup"><span data-stu-id="63b73-146">To use email to submit false positive messages to the Microsoft Spam Analysis Team</span></span>

1. <span data-ttu-id="63b73-147">Enregistrez le message que vous voulez envoyer comme courrier non indésirable.</span><span class="sxs-lookup"><span data-stu-id="63b73-147">Save the message you want to submit as non-spam.</span></span>

2. <span data-ttu-id="63b73-148">Créez un message vide et joignez à ce message le courrier non indésirable.</span><span class="sxs-lookup"><span data-stu-id="63b73-148">Create a new, blank message and attach the non-spam message to it.</span></span>

    <span data-ttu-id="63b73-149">Vous pouvez joindre plusieurs messages non indésirables, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="63b73-149">You can attach multiple non-spam messages if needed.</span></span>

3. <span data-ttu-id="63b73-150">Copiez et collez la ligne d'objet du message d'origine dans la ligne d'objet du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="63b73-150">Copy and paste the original message subject line into the new message subject line.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="63b73-151">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="63b73-151">Leave the body of the new message empty.</span></span>

4. <span data-ttu-id="63b73-152">Adressez votre nouveau message à [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="63b73-152">Send your new message to [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span></span>

### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a><span data-ttu-id="63b73-153">Le trafic provenant de mon adresse IP est limité par EOP</span><span class="sxs-lookup"><span data-stu-id="63b73-153">Traffic from my IP address is throttled by EOP</span></span>

<span data-ttu-id="63b73-154">Si vous recevez une notification d'échec de remise d'EOP, cela indique que votre adresse IP est limitée par EOP, par exemple :</span><span class="sxs-lookup"><span data-stu-id="63b73-154">If you receive an NDR from EOP that indicates that your IP address is being throttled by EOP, for example:</span></span>

 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`

<span data-ttu-id="63b73-p107">Vous avez reçu une notification d'échec de remise car une activité suspecte a été détectée sur l'adresse IP et a été restreinte temporairement le temps d'effectuer des évaluations supplémentaires. Si la suspicion est désactivée au cours de l'évaluation, cette restriction est bientôt levée.</span><span class="sxs-lookup"><span data-stu-id="63b73-p107">You received the NDR because suspicious activity has been detected from the IP address and it has been temporarily restricted while it is being further evaluated. If the suspicion is cleared through evaluation, this restriction will be lifted shortly.</span></span>

### <a name="i-cant-receive-email-from-senders-in-office-365"></a><span data-ttu-id="63b73-157">Je ne reçois pas les e-mails provenant d’expéditeurs dans Office 365</span><span class="sxs-lookup"><span data-stu-id="63b73-157">I can't receive email from senders in Office 365</span></span>

 <span data-ttu-id="63b73-158">Afin de recevoir des messages de la part de nos utilisateurs, assurez-vous que votre réseau autorise les connexions provenant des adresses IP utilisées par EOP dans nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="63b73-158">In order to receive messages from our users, make sure your network allows connections from the IP addresses that EOP uses in our datacenters.</span></span> <span data-ttu-id="63b73-159">Pour plus d’informations, consultez la rubrique [Exchange Online Protection IP addresses](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges).</span><span class="sxs-lookup"><span data-stu-id="63b73-159">For more information, see [Exchange Online Protection IP addresses](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges).</span></span>

## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a><span data-ttu-id="63b73-160">Meilleures pratiques pour l’envoi en bloc d’e-mails aux utilisateurs d’Office 365</span><span class="sxs-lookup"><span data-stu-id="63b73-160">Best practices for bulk emailing to Office 365 users</span></span>

<span data-ttu-id="63b73-161">Si vous menez souvent des campagnes d’envoi en bloc d’e-mails aux utilisateurs d’Office 365 et souhaitez vous assurer que vos e-mails arrivent de manière sûre et opportune, suivez les conseils fournis dans cette section.</span><span class="sxs-lookup"><span data-stu-id="63b73-161">If you often conduct bulk email campaigns to Office 365 users and want to ensure that your emails arrive in a safe and timely manner, follow the tips in this section.</span></span>

### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a><span data-ttu-id="63b73-162">Vérifier que le champ De : indique le nom de la personne qui envoie le message</span><span class="sxs-lookup"><span data-stu-id="63b73-162">Ensure that the From: name reflects who is sending the message</span></span>

<span data-ttu-id="63b73-p109">L'Objet doit être un bref résumé du contenu du message, et le corps du message doit clairement et brièvement indiquer l'objet de l'offre, du service ou du produit. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="63b73-p109">The Subject should be a brief summary of what the message is about, and the message body should clearly and succinctly indicate what the offering, service, or product is about. For example:</span></span>

<span data-ttu-id="63b73-165">Correct :</span><span class="sxs-lookup"><span data-stu-id="63b73-165">Correct:</span></span>

> <span data-ttu-id="63b73-166">De : marketing@shoppershandbag.com</span><span class="sxs-lookup"><span data-stu-id="63b73-166">From: marketing@shoppershandbag.com</span></span> <br/> <span data-ttu-id="63b73-167">Objet : catalogue mis à jour pour la saison de Noël !</span><span class="sxs-lookup"><span data-stu-id="63b73-167">Subject: Updated catalog for the Christmas season!</span></span>

<span data-ttu-id="63b73-168">Incorrect :</span><span class="sxs-lookup"><span data-stu-id="63b73-168">Incorrect:</span></span>

> <span data-ttu-id="63b73-169">De : someone@outlook.com</span><span class="sxs-lookup"><span data-stu-id="63b73-169">From: someone@outlook.com</span></span> <br/> <span data-ttu-id="63b73-170">Objet : Catalogues</span><span class="sxs-lookup"><span data-stu-id="63b73-170">Subject: Catalogs</span></span>

<span data-ttu-id="63b73-171">Plus vous vous présentez et décrivez ce que vous faites de façon claire, moins vos courriers seront bloqués par la plupart des filtres anti-spam.</span><span class="sxs-lookup"><span data-stu-id="63b73-171">The easier you make it for people to know who you are and what you are doing, the less difficulty you will have delivering through most spam filters.</span></span>

### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a><span data-ttu-id="63b73-172">Toujours inclure une option de désinscription dans les e-mails de campagne</span><span class="sxs-lookup"><span data-stu-id="63b73-172">Always include an unsubscribe option in campaign emails</span></span>

<span data-ttu-id="63b73-p110">Les e-mails de marketing, notamment les bulletins d'informations, doivent toujours inclure une option permettant de se désinscrire pour ne plus recevoir de futurs e-mails. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="63b73-p110">Marketing emails, especially newsletters, should always include a way of unsubscribing from future emails. For example:</span></span>

 `This email was sent to example@contoso.com by sender@fabrikam.com.`

 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`

<span data-ttu-id="63b73-p111">Certains expéditeurs incluent cette option en demandant aux destinataires d'envoyer un e-mail à un certain alias avec « Se désabonner » dans l'objet. Cela n'est pas préférable à l'exemple en un seul clic ci-dessus. Si vous choisissez de demander aux destinataires d'envoyer un message, assurez-vous que lorsqu'ils cliquent sur le lien, tous les champs requis sont renseignés au préalable.</span><span class="sxs-lookup"><span data-stu-id="63b73-p111">Some senders include this option by requiring recipients to send an email to a certain alias with "Unsubscribe" in the subject. This is not preferable to the one-click example above. If you do choose to require recipients to send a mail, ensure that when they click the link, all the required fields are pre-populated.</span></span>

### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a><span data-ttu-id="63b73-178">Utiliser l’option de contrôle de consentement double pour l’enregistrement à des e-mails de marketing ou à des bulletins d’informations</span><span class="sxs-lookup"><span data-stu-id="63b73-178">Use the double opt-in option for marketing email or newsletter registration</span></span>

<span data-ttu-id="63b73-p112">Cette pratique est recommandée par le secteur si votre entreprise requiert que les utilisateurs enregistrent leurs informations de contact ou les y encourage pour accéder à vos produits ou services. Certaines sociétés ont pris l'habitude d'inscrire automatiquement leurs utilisateurs pour les e-mails de marketing ou les bulletins d'informations électroniques lors du processus d'enregistrement. Néanmoins, cela est considéré comme une pratique marketing discutables dans le monde du filtrage des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="63b73-p112">This industry best practice is recommended if your company requires or encourages users to register their contact information in order to access your product or services. Some companies make it a practice to automatically sign up their users for marketing emails or e-newsletters during the registration process, but this is considered a questionable marketing practice in the world of email filtering.</span></span>

<span data-ttu-id="63b73-181">Au cours du processus d'enregistrement, si la case à cocher « Oui, merci de m'envoyer votre bulletin d'informations » ou « Oui, merci de m'envoyer les offres spéciales » est sélectionnée par défaut, les utilisateurs qui ne font pas assez attention risquent de s'inscrire par inadvertance aux e-mails de marketing ou aux bulletins d'informations qu'ils ne souhaitent pas recevoir.</span><span class="sxs-lookup"><span data-stu-id="63b73-181">During the registration process, if the "Yes, please send me your newsletter" or "Yes, please send me special offers" checkbox is selected by default, users who do not pay close attention may unintentionally sign up for marketing email or newsletters that they do not want to receive.</span></span>

 <span data-ttu-id="63b73-p113">Nous vous recommandons l'option de contrôle de consentement double à la place, ce qui signifie que la case à cocher pour les e-mails de marketing ou les bulletins d'informations est désactivée par défaut. En outre, une fois que le formulaire d'inscription a été envoyé, un e-mail de vérification est envoyé à l'utilisateur avec une URL qui leur permet de confirmer leur décision de recevoir des e-mails de marketing.</span><span class="sxs-lookup"><span data-stu-id="63b73-p113">We recommend the double opt-in option instead, which means that the checkbox for marketing emails or newsletters is unchecked by default. Additionally, once the registration form has been submitted, a verification email is sent to the user with a URL that allows them to confirm their decision to receive marketing emails.</span></span>

 <span data-ttu-id="63b73-184">Cela permet de garantir que seuls les utilisateurs qui souhaitent recevoir des e-mails de marketing sont inscrits pour les e-mails, en désactivant ensuite l'entreprise émettrice de toute pratique discutable.</span><span class="sxs-lookup"><span data-stu-id="63b73-184">This helps ensure that only those users who want to receive marketing email are signed up for the emails, subsequently clearing the sending company of any questionable email marketing practices.</span></span>

### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a><span data-ttu-id="63b73-185">Vérifier que le contenu des messages électroniques est transparent et qu’il est possible de le suivre</span><span class="sxs-lookup"><span data-stu-id="63b73-185">Ensure that email message content is transparent and traceable</span></span>

<span data-ttu-id="63b73-p114">La façon dont les e-mails sont envoyés est aussi importante que leur contenu. Lorsque vous créez le contenu d’un e-mail, utilisez les meilleures pratiques suivantes pour vous assurer que vos e-mails ne seront pas signalés par des services de filtrage des messages électroniques :</span><span class="sxs-lookup"><span data-stu-id="63b73-p114">Just as important as the way the emails are sent is the content they contain. When creating email content, use the following best practices to ensure that your emails will not be flagged by email filtering services:</span></span>

- <span data-ttu-id="63b73-188">Lorsque le message de l'e-mail demande aux destinataires d'ajouter l'expéditeur au carnet d'adresses, il doit clairement indiquer qu'une telle action ne constitue pas une garantie de remise.</span><span class="sxs-lookup"><span data-stu-id="63b73-188">When the email message requests that recipients add the sender to the address book, it should clearly state that such action is not a guarantee of delivery.</span></span>

- <span data-ttu-id="63b73-p115">Les redirections incluses dans le corps du message doivent être similaires et cohérentes et non multiples et variées. Une redirection dans ce contexte est tout élément qui pointe en dehors du message, comme des liens et des documents. Si vous avez de très nombreux liens Se désabonner ou Mettre à jour le profil, ils doivent tous pointer vers le même domaine. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="63b73-p115">Redirects included in the body of the message should be similar and consistent, and not multiple and varied. A redirect in this context is anything that points away from the message, such as links and documents. If you have a lot of advertising or Unsubscribe links or Update the Profile links, they should all point to the same domain. For example:</span></span>

  <span data-ttu-id="63b73-193">Correct :</span><span class="sxs-lookup"><span data-stu-id="63b73-193">Correct:</span></span>

  `unsubscribe.bulkmailer.com`

  `profile.bulkmailer.com`

  `options.bulkmailer.com`

  <span data-ttu-id="63b73-194">Incorrect :</span><span class="sxs-lookup"><span data-stu-id="63b73-194">Incorrect:</span></span>

  `unsubscribe.bulkmailer.com`

  `profiles.excite.com`

  `options.yahoo.com`

- <span data-ttu-id="63b73-195">Évitez les images et les pièces jointes volumineuses, ou les messages contenant uniquement une image.</span><span class="sxs-lookup"><span data-stu-id="63b73-195">Avoid content with large images and attachments, or messages that are solely composed of an image.</span></span>

- <span data-ttu-id="63b73-196">Vos paramètres publics de confidentialité ou P3P doivent signaler clairement la présence des pixels de suivi (bogues ou balises web).</span><span class="sxs-lookup"><span data-stu-id="63b73-196">Your public privacy or P3P settings should clearly state the presence of tracking pixels (web bugs or beacons).</span></span>

### <a name="remove-incorrect-email-aliases-from-your-databases"></a><span data-ttu-id="63b73-197">Supprimer les alias de messagerie incorrects de vos bases de données</span><span class="sxs-lookup"><span data-stu-id="63b73-197">Remove incorrect email aliases from your databases</span></span>

<span data-ttu-id="63b73-p116">Les alias de messagerie de votre base de données qui créent un renvoi sont inutiles et exposent vos messages électroniques sortants à des risques d’examen approfondi par les services de filtrage de courrier électronique. Assurez-vous que votre base de données de messagerie est à jour.</span><span class="sxs-lookup"><span data-stu-id="63b73-p116">Any email alias in your database that creates a bounce-back is unnecessary and puts your outbound emails at risk for further scrutiny by email filtering services. Ensure that your email database is up-to-date.</span></span>
