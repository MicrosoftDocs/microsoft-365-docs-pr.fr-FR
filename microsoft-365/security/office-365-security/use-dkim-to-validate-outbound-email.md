---
title: Utiliser DKIM pour le courrier électronique dans votre domaine personnalisé
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 04/05/2021
audience: ITPro
ms.topic: article
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser DKIM (DomainKeys Identified Mail) avec Microsoft 365 pour vous assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine personnalisé.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 12c7609635d9140f2e8efda3f6f1397619ce4790
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52929900"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain"></a><span data-ttu-id="42481-103">Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="42481-103">Use DKIM to validate outbound email sent from your custom domain</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="42481-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="42481-104">**Applies to**</span></span>
- [<span data-ttu-id="42481-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="42481-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="42481-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="42481-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="42481-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="42481-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

 <span data-ttu-id="42481-108">Cet article répertorie les étapes de l’utilisation de DomainKeys Identified Mail (DKIM) avec Microsoft 365 pour vous assurer que les systèmes d’e-mail de destination approuvent les messages sortants envoyés à partir de votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="42481-108">This article lists the steps to use DomainKeys Identified Mail (DKIM) with Microsoft 365 to ensure that destination email systems trust messages sent outbound from your custom domain.</span></span>

<span data-ttu-id="42481-109">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="42481-109">In this article:</span></span>

- [<span data-ttu-id="42481-110">Pourquoi DKIM est plus efficace que SPF seul pour empêcher l’usurpation d’identité malveillante</span><span class="sxs-lookup"><span data-stu-id="42481-110">How DKIM works better than SPF alone to prevent malicious spoofing</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)

- [<span data-ttu-id="42481-111">Procédure de mise à niveau manuelle de vos clés 1024 bits vers les clés de chiffrement DKIM 2048 bits</span><span class="sxs-lookup"><span data-stu-id="42481-111">Steps to manually upgrade your 1024-bit keys to 2048-bit DKIM encryption keys</span></span>](use-dkim-to-validate-outbound-email.md#1024to2048DKIM)

- [<span data-ttu-id="42481-112">Étapes de la configuration manuelle de DKIM</span><span class="sxs-lookup"><span data-stu-id="42481-112">Steps to manually set up DKIM</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)

- [<span data-ttu-id="42481-113">Étapes de configuration de DKIM pour plusieurs domaines personnalisés</span><span class="sxs-lookup"><span data-stu-id="42481-113">Steps to configure DKIM for more than one custom domain</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)

- [<span data-ttu-id="42481-114">Désactivation de la stratégie de signature DKIM pour un domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="42481-114">Disabling the DKIM signing policy for a custom domain</span></span>](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)

- [<span data-ttu-id="42481-115">Comportement par défaut pour DKIM et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42481-115">Default behavior for DKIM and Microsoft 365</span></span>](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)

- <span data-ttu-id="42481-116">Configuration de DKIM permettant à un service tiers d’envoyer des courriers électroniques au nom de votre domaine personnalisé, ou d’usurper ce dernier</span><span class="sxs-lookup"><span data-stu-id="42481-116">[Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)</span></span>

- [<span data-ttu-id="42481-117">Étapes suivantes : après avoir configuré DKIM pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42481-117">Next steps: After you set up DKIM for Microsoft 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)

> [!NOTE]
> <span data-ttu-id="42481-118">Microsoft 365 configure automatiquement DKIM pour les domaines initiaux 'onmicrosoft.com'.</span><span class="sxs-lookup"><span data-stu-id="42481-118">Microsoft 365 automatically sets up DKIM for its initial 'onmicrosoft.com' domains.</span></span> <span data-ttu-id="42481-119">Cela signifie que vous n’avez rien à faire pour configurer DKIM pour les noms de domaine initial (par exemple, litware.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="42481-119">That means you don't need to do anything to set up DKIM for any initial domain names (for example, litware.onmicrosoft.com).</span></span> <span data-ttu-id="42481-120">Pour plus d'informations sur les domaines, consultez l'article [Forum aux questions sur les domaines](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain).</span><span class="sxs-lookup"><span data-stu-id="42481-120">For more information about domains, see [Domains FAQ](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain).</span></span>

<span data-ttu-id="42481-121">DKIM fait partie du trio de méthodes d'authentification (SPF, DKIM et DMARC) qui permet d'empêcher les attaquants d'envoyer des messages qui semblent provenir de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-121">DKIM is one of the trio of Authentication methods (SPF, DKIM and DMARC) that help prevent attackers from sending messages that look like they come from your domain.</span></span>

<span data-ttu-id="42481-p102">DKIM vous permet d'ajouter une signature numérique aux e-mails sortants dans l'en-tête du message. Lorsque vous configurez DKIM, vous autorisez votre domaine à associer son nom à un courrier ou à l’y signer à l'aide d'une authentification de chiffrement. Les systèmes de messagerie qui reçoivent des e-mails de votre domaine peuvent utiliser cette signature numérique pour déterminer si le courrier entrant est légitime.</span><span class="sxs-lookup"><span data-stu-id="42481-p102">DKIM lets you add a digital signature to outbound email messages in the message header. When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message using cryptographic authentication. Email systems that get email from your domain can use this digital signature to help verify whether incoming email is legitimate.</span></span>

<span data-ttu-id="42481-125">À la base, une clé privée chiffre l’en-tête dans le courrier sortant d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-125">In basic, a private key encrypts the header in a domain's outgoing email.</span></span> <span data-ttu-id="42481-126">La clé publique est publiée dans les enregistrements DNS, et les serveurs de réception peuvent utiliser cette clé pour décoder la signature.</span><span class="sxs-lookup"><span data-stu-id="42481-126">The public key is published in the domain's DNS records, and receiving servers can use that key to decode the signature.</span></span> <span data-ttu-id="42481-127">La vérification DKIM permet aux serveurs de réception de confirmer que les courriers viennent vraiment de votre domaine et non d’une personne *usurpant* votre domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-127">DKIM verification helps the receiving servers confirm the mail is really coming from your domain and not someone *spoofing* your domain.</span></span>

> [!TIP]
><span data-ttu-id="42481-p104">Vous pouvez également choisir de n'effectuer aucun réglage DKIM pour votre domaine personnalisé. Si vous ne configurez pas DKIM pour votre domaine personnalisé, Microsoft 365 crée une paire de clés privée et publique, active la signature DKIM, et configure la stratégie par défaut de Microsoft 365 pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="42481-p104">You can choose to do nothing about DKIM for your custom domain too. If you don't set up DKIM for your custom domain, Microsoft 365 creates a private and public key pair, enables DKIM signing, and then configures the Microsoft 365 default policy for your custom domain.</span></span>

 <span data-ttu-id="42481-p105">La configuration DKIM intégrée de Microsoft 365 est une couverture suffisante pour la plupart des clients. Cependant, vous devez configurer manuellement DKIM pour votre domaine personnalisé dans ces circonstances :</span><span class="sxs-lookup"><span data-stu-id="42481-p105">Microsoft-365's built-in DKIM configuration is sufficient coverage for most customers. However, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>

- <span data-ttu-id="42481-132">Vous avez plusieurs domaines personnalisés dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42481-132">You have more than one custom domain in Microsoft 365</span></span>

- <span data-ttu-id="42481-133">Vous allez également configurer DMARC (**recommandé**)</span><span class="sxs-lookup"><span data-stu-id="42481-133">You're going to set up DMARC too (**recommended**)</span></span>

- <span data-ttu-id="42481-134">Vous souhaitez contrôler votre clé privée</span><span class="sxs-lookup"><span data-stu-id="42481-134">You want control over your private key</span></span>

- <span data-ttu-id="42481-135">Vous souhaitez personnaliser vos enregistrements CNAME</span><span class="sxs-lookup"><span data-stu-id="42481-135">You want to customize your CNAME records</span></span>

- <span data-ttu-id="42481-136">Vous souhaitez configurer des clés DKIM pour les e-mails provenant d’un domaine tiers, par exemple, si vous utilisez un programme d’envoi de courrier en nombre tiers.</span><span class="sxs-lookup"><span data-stu-id="42481-136">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>


## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing"></a><span data-ttu-id="42481-137">Pourquoi DKIM est plus efficace que SPF seul pour empêcher l’usurpation d’identité malveillante</span><span class="sxs-lookup"><span data-stu-id="42481-137">How DKIM works better than SPF alone to prevent malicious spoofing</span></span>
<span data-ttu-id="42481-138"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-138"><a name="HowDKIMWorks"> </a></span></span>

<span data-ttu-id="42481-139">SPF ajoute des informations à une enveloppe de message mais DKIM *chiffre* une signature dans l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="42481-139">SPF adds information to a message envelope but DKIM *encrypts* a signature within the message header.</span></span> <span data-ttu-id="42481-140">Lorsque vous transférez un message, des parties de l'enveloppe de ce message peuvent être supprimées par le serveur de transfert.</span><span class="sxs-lookup"><span data-stu-id="42481-140">When you forward a message, portions of that message's envelope can be stripped away by the forwarding server.</span></span> <span data-ttu-id="42481-141">Étant donné que la signature numérique reste dans le message électronique, car elle fait partie de l'en-tête du message, DKIM fonctionne même lorsqu'un message a été transféré, comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="42481-141">Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>

![Diagramme illustrant l'authentification DKIM correcte d'un message envoyé lors de l'échec du contrôle SPF](../../media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)

<span data-ttu-id="42481-p107">Dans cet exemple, si vous aviez publié un seul enregistrement SPF TXT pour votre domaine, le serveur de courrier destinataire pourrait avoir marqué vos e-mails comme courriers indésirables et généré un résultat faux positif. **L’ajout de DKIM dans ce scénario réduit *le signalement de courrier indésirable* faux positif**. Étant donné que DKIM repose à la fois sur le chiffrement de la clé publique et non les adresses IP uniquement pour l’authentification, DKIM représente une forme d’authentification beaucoup plus puissante que SPF. Nous vous recommandons d’utiliser à la fois SPF et DKIM, ainsi que DMARC dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="42481-p107">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result. **The addition of DKIM in this scenario reduces *false positive* spam reporting.** Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF. We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>

> [!TIP]
> <span data-ttu-id="42481-147">DKIM utilise une clé privée pour insérer une signature chiffrée dans les en-têtes du message.</span><span class="sxs-lookup"><span data-stu-id="42481-147">DKIM uses a private key to insert an encrypted signature into the message headers.</span></span> <span data-ttu-id="42481-148">Le domaine qui fournit la signature, aussi appelé domaine sortant, est inséré en tant que valeur du champ **d=** dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="42481-148">The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header.</span></span> <span data-ttu-id="42481-149">Le domaine de vérification, ou le domaine du destinataire, utilise ensuite le champ **d=** pour rechercher la clé publique du système DNS, puis authentifier le message.</span><span class="sxs-lookup"><span data-stu-id="42481-149">The verifying domain, or recipient's domain, then uses the **d=** field to look up the public key from DNS, and authenticate the message.</span></span> <span data-ttu-id="42481-150">Si le message est vérifié, la vérification DKIM a réussi.</span><span class="sxs-lookup"><span data-stu-id="42481-150">If the message is verified, the DKIM check passes.</span></span>


## <a name="steps-to-manually-upgrade-your-1024-bit-keys-to-2048-bit-dkim-encryption-keys"></a><span data-ttu-id="42481-151">Mise à niveau manuelle de vos clés 1024 bits vers les clés de chiffrement DKIM 2048 bits</span><span class="sxs-lookup"><span data-stu-id="42481-151">Steps to manually upgrade your 1024-bit keys to 2048-bit DKIM encryption keys</span></span>
<span data-ttu-id="42481-152"><a name="1024to2048DKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-152"><a name="1024to2048DKIM"> </a></span></span>

> [!NOTE]
> <span data-ttu-id="42481-153">Microsoft 365 configure automatiquement DKIM pour les domaines *onmicrosoft.com*.</span><span class="sxs-lookup"><span data-stu-id="42481-153">Microsoft 365 automatically sets up DKIM for *onmicrosoft.com* domains.</span></span> <span data-ttu-id="42481-154">Aucune étape n’est nécessaire pour utiliser DKIM pour les noms de domaine initiaux (par exemple, litware.*onmicrosoft.com*).</span><span class="sxs-lookup"><span data-stu-id="42481-154">No steps are needed to use DKIM for any initial domain names (like litware.*onmicrosoft.com*).</span></span> <span data-ttu-id="42481-155">Pour plus d'informations sur les domaines, consultez l'article [Forum aux questions sur les domaines](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain).</span><span class="sxs-lookup"><span data-stu-id="42481-155">For more information about domains, see [Domains FAQ](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain).</span></span>

<span data-ttu-id="42481-156">Étant donné que le nombre de bits 1024 et 2048 sont pris en charge pour les clés DKIM, ces instructions vous indiquent comment mettre à niveau votre clé 1024 bits vers 2048 dans [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="42481-156">Since both 1024 and 2048 bitness are supported for DKIM keys, these directions will tell you how to upgrade your 1024-bit key to 2048 in [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="42481-157">Les étapes ci-dessous concernent deux cas d’utilisation ; veuillez choisir celui qui correspond le mieux à votre configuration.</span><span class="sxs-lookup"><span data-stu-id="42481-157">The steps below are for two use-cases, please choose the one that best fits your configuration.</span></span>

- <span data-ttu-id="42481-158">Lorsque vous **avez déjà configuré DKIM**, vous pouvez faire pivoter le nombre de bits en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="42481-158">When you **already have DKIM configured**, you rotate bitness by running the following command:</span></span>

  ```powershell
  Rotate-DkimSigningConfig -KeySize 2048 -Identity {Guid of the existing Signing Config}
  ```

  <span data-ttu-id="42481-159">**ou**</span><span class="sxs-lookup"><span data-stu-id="42481-159">**or**</span></span>

- <span data-ttu-id="42481-160">Pour une **nouvelle implémentation de la fonctionnalité DKIM**, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="42481-160">For a **new implementation of DKIM**, run the following command:</span></span>

  ```powershell
  New-DkimSigningConfig -DomainName <Domain for which config is to be created> -KeySize 2048 -Enabled $true
  ```

<span data-ttu-id="42481-161">Restez connecté à Exchange Online PowerShell pour *vérifier* la configuration en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="42481-161">Stay connected to Exchange Online PowerShell to *verify* the configuration by running the following command:</span></span>

```powershell
Get-DkimSigningConfig -Identity <Domain for which the configuration was set> | Format-List
```

> [!TIP]
> <span data-ttu-id="42481-162">Cette nouvelle clé 2048 bits prend effet sur RotateOnDate et envoie des e-mails avec la clé 1024 bits au niveau intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="42481-162">This new 2048-bit key takes effect on the RotateOnDate, and will send emails with the 1024-bit key in the interim.</span></span> <span data-ttu-id="42481-163">Après quatre jours, vous pouvez à nouveau effectuer un test à l’aide de la touche 2048 bits (autrement dit, une fois que la rotation prend effet sur le deuxième sélecteur).</span><span class="sxs-lookup"><span data-stu-id="42481-163">After four days, you can test again with the 2048-bit key (that is, once the rotation takes effect to the second selector).</span></span>

<span data-ttu-id="42481-164">Si vous voulez faire pivoter vers le deuxième sélecteur, vos options sont a) laisser le service Microsoft 365 faire pivoter le sélecteur et effectuer la mise à niveau vers le nombre de bits 2048 dans les 6 mois, ou b) après 4 jours et confirmation que le nombre de bits 2048 est utilisé, faire pivoter manuellement la deuxième touche du sélecteur en utilisant la cmdlet appropriée répertoriée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="42481-164">If you want to rotate to the second selector, your options are a) let the Microsoft 365 service rotate the selector and upgrade to 2048-bitness within the next 6 months, or b) after 4 days and confirming that 2048-bitness is in use, manually rotate the second selector key by using the appropriate cmdlet listed above.</span></span>

<span data-ttu-id="42481-165">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez les articles suivants : [Rotate-DkimSigningConfig](/powershell/module/exchange/rotate-dkimsigningconfig), [New-DkimSigningConfig](/powershell/module/exchange/new-dkimsigningconfig)et [Get-DkimSigningConfig](/powershell/module/exchange/get-dkimsigningconfig).</span><span class="sxs-lookup"><span data-stu-id="42481-165">For detailed syntax and parameter information, see the following articles: [Rotate-DkimSigningConfig](/powershell/module/exchange/rotate-dkimsigningconfig), [New-DkimSigningConfig](/powershell/module/exchange/new-dkimsigningconfig), and [Get-DkimSigningConfig](/powershell/module/exchange/get-dkimsigningconfig).</span></span>

## <a name="steps-to-manually-set-up-dkim"></a><span data-ttu-id="42481-166">Étapes de la configuration manuelle de DKIM</span><span class="sxs-lookup"><span data-stu-id="42481-166">Steps to manually set up DKIM</span></span>
<span data-ttu-id="42481-167"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-167"><a name="SetUpDKIMO365"> </a></span></span>

<span data-ttu-id="42481-168">Pour configurer DKIM, suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="42481-168">To configure DKIM, you will complete these steps:</span></span>

- [<span data-ttu-id="42481-169">Publication de deux enregistrements CNAME pour votre domaine personnalisé dans le système DNS</span><span class="sxs-lookup"><span data-stu-id="42481-169">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)

- [<span data-ttu-id="42481-170">Activation de la signature DKIM pour votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="42481-170">Enable DKIM signing for your custom domain</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)

### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="42481-171">Publication de deux enregistrements CNAME pour votre domaine dans le système DNS</span><span class="sxs-lookup"><span data-stu-id="42481-171">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="42481-172"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-172"><a name="Publish2CNAME"> </a></span></span>

<span data-ttu-id="42481-173">Pour chaque domaine auquel vous souhaitez ajouter une signature DKIM dans le système DNS, vous devez publier deux enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="42481-173">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records.</span></span>

> [!NOTE]
> <span data-ttu-id="42481-174">Si vous n’avez pas lu l’intégralité de l’article, il est possible que vous ayez manqué les informations de connexion PowerShell qui vous ont été utiles : [Connectez-vous à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="42481-174">If you haven't read the full article, you may have missed this time-saving PowerShell connection information: [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="42481-175">Exécutez les commandes suivantes dans Exchange Online PowerShell pour créer les enregistrements du sélecteur :</span><span class="sxs-lookup"><span data-stu-id="42481-175">Run the following commands in Exchange Online PowerShell to create the selector records:</span></span>

```powershell
New-DkimSigningConfig -DomainName <domain> -Enabled $false
Get-DkimSigningConfig -Identity <domain> | Format-List Selector1CNAME, Selector2CNAME
```

<span data-ttu-id="42481-p112">Si vous avez configuré des domaines personnalisés en plus du domaine initial dans Microsoft 365, vous devez publier deux enregistrements CNAME pour chaque domaine supplémentaire. Par conséquent, si vous avez deux domaines, vous devez publier deux enregistrements CNAME supplémentaires, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="42481-p112">If you have provisioned custom domains in addition to the initial domain in Microsoft 365, you must publish two CNAME records for each additional domain. So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span>

<span data-ttu-id="42481-178">Utilisez le format suivant pour les enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="42481-178">Use the following format for the CNAME records.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42481-179">Si vous êtes l’un de nos clients GCC High, nous calculons _domainGuid_ différemment.</span><span class="sxs-lookup"><span data-stu-id="42481-179">If you are one of our GCC High customers, we calculate _domainGuid_ differently!</span></span> <span data-ttu-id="42481-180">Au lieu de rechercher l’enregistrement MX pour votre _initialDomain_ afin de calculer _domainGuid_, nous le calculons directement à partir du domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="42481-180">Instead of looking up the MX record for your _initialDomain_ to calculate _domainGuid_, instead we calculate it directly from the customized domain.</span></span> <span data-ttu-id="42481-181">Par exemple, si votre domaine personnalisé est « contoso.com », les points étant remplacés par des tirets, votre domainGuid devient « contoso-com ».</span><span class="sxs-lookup"><span data-stu-id="42481-181">For example, if your customized domain is "contoso.com" your domainGuid becomes "contoso-com", any periods are replaced with a dash.</span></span> <span data-ttu-id="42481-182">Par conséquent, quel que soit l’enregistrement MX sur lequel pointe votre initialDomain, vous devez toujours utiliser la méthode ci-dessus pour calculer la domainGuid à utiliser dans vos enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="42481-182">So, regardless of what MX record your initialDomain points to, you'll always use the above method to calculate the domainGuid to use in your CNAME records.</span></span>

```console
Host name:            selector1._domainkey
Points to address or value:    selector1-<domainGUID>._domainkey.<initialDomain>
TTL:                3600

Host name:            selector2._domainkey
Points to address or value:    selector2-<domainGUID>._domainkey.<initialDomain>
TTL:                3600
```

<span data-ttu-id="42481-183">Où :</span><span class="sxs-lookup"><span data-stu-id="42481-183">Where:</span></span>

- <span data-ttu-id="42481-184">Pour Microsoft 365, les sélecteurs seront toujours « selector1 » ou « selector2 ».</span><span class="sxs-lookup"><span data-stu-id="42481-184">For Microsoft 365, the selectors will always be "selector1" or "selector2".</span></span>

- <span data-ttu-id="42481-p114">_domainGUID_ est identique à _domainGUID_ dans l'enregistrement MX personnalisé pour votre domaine personnalisé qui se trouve avant mail.protection.outlook.com. Par exemple, dans cet enregistrement MX pour le domaine contoso.com, l'élément  _domainGUID_ est contoso-com :</span><span class="sxs-lookup"><span data-stu-id="42481-p114">_domainGUID_ is the same as the _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com. For example, in the following MX record for the domain contoso.com, the _domainGUID_ is contoso-com:</span></span>

  > <span data-ttu-id="42481-p115">contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="42481-p115">contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com</span></span>

- <span data-ttu-id="42481-189">_initialDomain_ est le domaine que vous avez utilisé lorsque vous vous êtes inscrit à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="42481-189">_initialDomain_ is the domain that you used when you signed up for Microsoft 365.</span></span> <span data-ttu-id="42481-190">Les domaines initiaux se terminent toujours par onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="42481-190">Initial domains always end in onmicrosoft.com.</span></span> <span data-ttu-id="42481-191">Pour plus d’informations sur la détermination de votre [domaine initial](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain), voir Forum aux questions sur les domaines.</span><span class="sxs-lookup"><span data-stu-id="42481-191">For information about determining your initial domain, see [Domains FAQ](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain).</span></span>

<span data-ttu-id="42481-192">Par exemple, si vous avez un domaine initial cohovineyardandwinery.onmicrosoft.com, ainsi que deux domaines personnalisés cohovineyard.com et cohowinery.com, vous devez configurer deux enregistrements CNAME pour chaque domaine supplémentaire, soit un total de quatre enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="42481-192">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>

```console
Host name:            selector1._domainkey
Points to address or value:    selector1-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:            selector2._domainkey
Points to address or value:    selector2-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:            selector1._domainkey
Points to address or value:    selector1-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:            selector2._domainkey
Points to address or value:    selector2-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600
```

> [!NOTE]
> <span data-ttu-id="42481-193">Il est important de créer le deuxième enregistrement, mais il est possible qu’un seul sélecteur soit disponible au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="42481-193">It's important to create the second record, but only one of the selectors may be available at the time of creation.</span></span> <span data-ttu-id="42481-194">Par essence, le deuxième sélecteur peut pointer vers une adresse qui n’a pas encore été créée.</span><span class="sxs-lookup"><span data-stu-id="42481-194">In essence, the second selector might point to an address that hasn't been created yet.</span></span> <span data-ttu-id="42481-195">Nous vous recommandons de créer le deuxième enregistrement CNAME, car la rotation de votre clé sera transparente.</span><span class="sxs-lookup"><span data-stu-id="42481-195">We still recommended that you create the second CNAME record, because your key rotation will be seamless.</span></span>


### <a name="steps-to-enable-dkim-signing-for-your-custom-domain"></a><span data-ttu-id="42481-196">Étapes d’activation de la signature DKIM pour votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="42481-196">Steps to enable DKIM signing for your custom domain</span></span>
<span data-ttu-id="42481-197"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-197"><a name="EnableDKIMinO365"> </a></span></span>

<span data-ttu-id="42481-p118">Une fois que vous avez publié les enregistrements CNAME dans le système DNS, vous pouvez activer la signature DKIM par l'intermédiaire de Microsoft 365. Vous pouvez effectuer cette action par le biais du centre d'administration Microsoft 365 ou à l'aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42481-p118">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Microsoft 365. You can do this either through the Microsoft 365 admin center or by using PowerShell.</span></span>

#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-admin-center"></a><span data-ttu-id="42481-200">Activation de la signature DKIM pour votre domaine personnalisé par l’intermédiaire du Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="42481-200">To enable DKIM signing for your custom domain through the admin center</span></span>

1. <span data-ttu-id="42481-201">[Connectez-vous à Microsoft 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4) à l’aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="42481-201">[Sign in to Microsoft 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="42481-202">Allez [sur security.microsoft.com ](https://security.microsoft.com)et suivez le chemin ci-dessous..</span><span class="sxs-lookup"><span data-stu-id="42481-202">Go to [security.microsoft.com](https://security.microsoft.com) and follow the path below.</span></span>

3. <span data-ttu-id="42481-203">Sélectionnez **Email & Collaboration > Stratégies et règles > Stratégies de lutte contre les menaces > DKIM**.</span><span class="sxs-lookup"><span data-stu-id="42481-203">Go to **Email & Collaboration > Policies & rules > Threat policies > DKIM**.</span></span>

4. <span data-ttu-id="42481-p119">Sélectionnez le domaine pour lequel vous souhaitez activer DKIM, puis pour **Signer les messages pour ce domaine avec des signatures DKIM**, choisissez **Activer**. Répétez cette étape pour chaque domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="42481-p119">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**. Repeat this step for each custom domain.</span></span>

#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="42481-206">Activation de la signature DKIM pour votre domaine personnalisé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="42481-206">To enable DKIM signing for your custom domain by using PowerShell</span></span>

> [!IMPORTANT]
>:::image type="content" source="../../media/dkim.png" alt-text="Erreur « Aucune touche DKIM enregistrée pour ce domaine ».":::
> <span data-ttu-id="42481-208">Si vous configurez DKIM pour la première fois et que vous voyez l’erreur « Aucune clé DKIM enregistrée pour ce domaine ».</span><span class="sxs-lookup"><span data-stu-id="42481-208">If you are configuring DKIM for the first time and see the error 'No DKIM keys saved for this domain.'</span></span> <span data-ttu-id="42481-209">effectuez la commande de l’étape 2, ci-dessous (par exemple, *Set-DkimSigningConfig -Identity contoso.com -Enabled $true*) pour voir la clé.</span><span class="sxs-lookup"><span data-stu-id="42481-209">complete the command in step 2, below (for example, *Set-DkimSigningConfig -Identity contoso.com -Enabled $true*) to see the key.</span></span>

1. <span data-ttu-id="42481-210">[Connectez-vous à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="42481-210">[Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="42481-211">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="42481-211">Run the following command:</span></span>

   ```powershell
   Set-DkimSigningConfig -Identity <domain> -Enabled $true
   ```

   <span data-ttu-id="42481-212">Où _domain_ est le nom du domaine personnalisé pour lequel vous souhaitez activer la signature DKIM.</span><span class="sxs-lookup"><span data-stu-id="42481-212">Where _domain_ is the name of the custom domain that you want to enable DKIM signing for.</span></span>

   <span data-ttu-id="42481-213">Par exemple, pour le domaine contoso.com :</span><span class="sxs-lookup"><span data-stu-id="42481-213">For example, for the domain contoso.com:</span></span>

   ```powershell
   Set-DkimSigningConfig -Identity contoso.com -Enabled $true
   ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-microsoft-365"></a><span data-ttu-id="42481-214">Confirmation du fait que la signature DKIM est correctement configurée pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42481-214">To Confirm DKIM signing is configured properly for Microsoft 365</span></span>

<span data-ttu-id="42481-p121">Patientez quelques minutes avant de suivre ces étapes permettant de confirmer que vous avez correctement configuré DKIM. Cela donne le temps aux informations DKIM relatives au domaine de se propager dans l’ensemble du réseau.</span><span class="sxs-lookup"><span data-stu-id="42481-p121">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM. This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>

- <span data-ttu-id="42481-217">Envoyez un message à partir d’un compte au sein de votre domaine Microsoft 365 compatible avec DKIM à un autre compte de messagerie, tel qu’outlook.com ou Hotmail.com.</span><span class="sxs-lookup"><span data-stu-id="42481-217">Send a message from an account within your Microsoft 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>

- <span data-ttu-id="42481-p122">N’utilisez pas un compte aol.com à des fins de test. Il est possible qu’AOL ignore la vérification DKIM si la vérification SPF aboutit. Cela annule votre test.</span><span class="sxs-lookup"><span data-stu-id="42481-p122">Do not use an aol.com account for testing purposes. AOL may skip the DKIM check if the SPF check passes. This will nullify your test.</span></span>

- <span data-ttu-id="42481-p123">Ouvrez le message et examinez l’en-tête. Les instructions pour afficher l’en-tête du message varient en fonction de votre client de messagerie. Pour obtenir des instructions sur l’affichage des en-têtes de messages dans Outlook, consultez l’article [Afficher des en-têtes de messages Internet dans Outlook](https://support.microsoft.com/office/cd039382-dc6e-4264-ac74-c048563d212c).</span><span class="sxs-lookup"><span data-stu-id="42481-p123">Open the message and look at the header. Instructions for viewing the header for the message will vary depending on your messaging client. For instructions on viewing message headers in Outlook, see [View internet message headers in Outlook](https://support.microsoft.com/office/cd039382-dc6e-4264-ac74-c048563d212c).</span></span>

  <span data-ttu-id="42481-p124">Le message signé par DKIM contient le domaine et le nom d’hôte que vous avez définis lorsque vous avez publié les entrées CNAME. Le message se présente un peu comme cet exemple :</span><span class="sxs-lookup"><span data-stu-id="42481-p124">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries. The message will look something like this example:</span></span>

  ```console
    From: Example User <example@contoso.com>
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed;
        s=selector1; d=contoso.com; t=1429912795;
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type;
        bh=<body hash>;
        b=<signed field>;
  ```

- <span data-ttu-id="42481-p125">Recherchez l’en-tête des résultats de l’authentification. Bien que chaque service de réception utilise un format légèrement différent pour apposer un cachet sur le courrier entrant, le résultat doit inclure un élément qui ressemble à **DKIM=test** ou **DKIM=OK**.</span><span class="sxs-lookup"><span data-stu-id="42481-p125">Look for the Authentication-Results header. While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span>

## <a name="to-configure-dkim-for-more-than-one-custom-domain"></a><span data-ttu-id="42481-228">Configuration de DKIM pour plusieurs domaines personnalisés</span><span class="sxs-lookup"><span data-stu-id="42481-228">To configure DKIM for more than one custom domain</span></span>
<span data-ttu-id="42481-229"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-229"><a name="DKIMMultiDomain"> </a></span></span>

<span data-ttu-id="42481-230">Si un jour vous décidez d'ajouter un autre domaine personnalisé et que vous souhaitez activer DKIM pour ce nouveau domaine, vous devez effectuer les étapes décrites dans cet article pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-230">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain.</span></span> <span data-ttu-id="42481-231">Plus spécifiquement, réalisez toutes les étapes indiquées dans la section [Configuration manuelle de DKIM](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span><span class="sxs-lookup"><span data-stu-id="42481-231">Specifically, complete all steps in [What you need to do to manually set up DKIM](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>

## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain"></a><span data-ttu-id="42481-232">Désactivation de la stratégie de signature DKIM pour un domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="42481-232">Disabling the DKIM signing policy for a custom domain</span></span>
<span data-ttu-id="42481-233"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-233"><a name="DisableDKIMSigningPolicy"> </a></span></span>

<span data-ttu-id="42481-234">La désactivation de la stratégie de signature ne désactive pas complètement DKIM.</span><span class="sxs-lookup"><span data-stu-id="42481-234">Disabling the signing policy does not completely disable DKIM.</span></span> <span data-ttu-id="42481-235">Après un certain temps, Microsoft 365 applique automatiquement la stratégie par défaut pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-235">After a period of time, Microsoft 365 will automatically apply the default policy for your domain.</span></span> <span data-ttu-id="42481-236">Pour plus d'informations, voir [Comportement par défaut pour DKIM et Microsoft 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span><span class="sxs-lookup"><span data-stu-id="42481-236">For more information, see [Default behavior for DKIM and Microsoft 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>

### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="42481-237">Pour désactiver la stratégie de signature DKIM à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="42481-237">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="42481-238">[Connectez-vous à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="42481-238">[Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="42481-239">Exécutez l’une des commandes suivantes pour chaque domaine pour lequel vous souhaitez désactiver la signature DKIM.</span><span class="sxs-lookup"><span data-stu-id="42481-239">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>

   ```powershell
   $p = Get-DkimSigningConfig -Identity <domain>
   $p[0] | Set-DkimSigningConfig -Enabled $false
   ```

   <span data-ttu-id="42481-240">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="42481-240">For example:</span></span>

   ```powershell
   $p = Get-DkimSigningConfig -Identity contoso.com
   $p[0] | Set-DkimSigningConfig -Enabled $false
   ```

   <span data-ttu-id="42481-241">Ou</span><span class="sxs-lookup"><span data-stu-id="42481-241">Or</span></span>

   ```powershell
   Set-DkimSigningConfig -Identity $p[<number>].Identity -Enabled $false
   ```

   <span data-ttu-id="42481-p128">Où le _nombre_ est l'index de la stratégie. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="42481-p128">Where _number_ is the index of the policy. For example:</span></span>

   ```powershell
   Set-DkimSigningConfig -Identity $p[0].Identity -Enabled $false
   ```

## <a name="default-behavior-for-dkim-and-microsoft-365"></a><span data-ttu-id="42481-244">Comportement par défaut pour DKIM et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42481-244">Default behavior for DKIM and Microsoft 365</span></span>
<span data-ttu-id="42481-245"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-245"><a name="DefaultDKIMbehavior"> </a></span></span>

<span data-ttu-id="42481-p129">Si vous n’activez pas DKIM, Microsoft 365 crée automatiquement une clé publique DKIM 1024 bits pour votre domaine par défaut et la clé privée associée que nous stockons en interne dans notre centre de données. Par défaut, Microsoft 365 utilise une configuration de signature par défaut pour les domaines ne disposant d’aucune stratégie définie. Cela signifie que si vous ne configurez pas DKIM vous-même, Microsoft 365 utilise sa stratégie par défaut et les clés qu’il crée pour activer DKIM sur votre domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-p129">If you do not enable DKIM, Microsoft 365 automatically creates a 1024-bit DKIM public key for your default domain and the associated private key which we store internally in our datacenter. By default, Microsoft 365 uses a default signing configuration for domains that do not have a policy in place. This means that if you do not set up DKIM yourself, Microsoft 365 will use its default policy and keys it creates to enable DKIM for your domain.</span></span>

<span data-ttu-id="42481-249">En outre, si vous désactivez la signature DKIM, après un certain temps, Microsoft 365 applique automatiquement sa stratégie par défaut pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-249">Also, if you disable DKIM signing after enabling it, after a period of time, Microsoft 365 will automatically apply the default policy for your domain.</span></span>

<span data-ttu-id="42481-p130">Dans l’exemple suivant, supposons que DKIM pour fabrikam.com a été activé par Microsoft 365, et pas par l’administrateur du domaine. Cela signifie que les enregistrements CNAME requis n’existent pas dans le système DNS. Les signatures DKIM pour les e-mails provenant de ce domaine se présenteront comme suit :</span><span class="sxs-lookup"><span data-stu-id="42481-p130">In the following example, suppose that DKIM for fabrikam.com was enabled by Microsoft 365, not by the administrator of the domain. This means that the required CNAMEs do not exist in DNS. DKIM signatures for email from this domain will look something like this:</span></span>

```console
From: Second Example <second.example@fabrikam.com>
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed;
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795;
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type;
    bh=<body hash>;
    b=<signed field>;
```

<span data-ttu-id="42481-253">Dans cet exemple, le domaine et le nom d'hôte contiennent les valeurs vers lesquelles l'enregistrement CNAME pointerait si la signature DKIM pour fabrikam.com avait été activée par l'administrateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="42481-253">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator.</span></span> <span data-ttu-id="42481-254">Finalement, chaque message envoyé à partir de Microsoft 365 sera signé avec DKIM.</span><span class="sxs-lookup"><span data-stu-id="42481-254">Eventually, every single message sent from Microsoft 365 will be DKIM-signed.</span></span> <span data-ttu-id="42481-255">Si vous activez DKIM vous-même, le domaine est identique à celui de l’adresse de l’expéditeur, ici fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="42481-255">If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com.</span></span> <span data-ttu-id="42481-256">Dans le cas contraire, DKIM ne s'aligne pas et utilise le domaine initial de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="42481-256">If you don't, it will not align and instead will use your organization's initial domain.</span></span> <span data-ttu-id="42481-257">Pour plus d’informations sur la détermination de votre [domaine initial](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain), voir Forum aux questions sur les domaines.</span><span class="sxs-lookup"><span data-stu-id="42481-257">For information about determining your initial domain, see [Domains FAQ](../../admin/setup/domains-faq.yml#why-do-i-have-an--onmicrosoft-com--domain).</span></span>

## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="42481-258">Configurer DKIM de sorte qu’un service tiers puisse envoyer du courrier au nom de votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="42481-258">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="42481-259"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-259"><a name="SetUp3rdPartyspoof"> </a></span></span>

<span data-ttu-id="42481-p132">Certains fournisseurs de services de messagerie en masse ou de services SaaS vous permettent de configurer des clés DKIM pour les courriers électroniques qui proviennent de leur service. Cela requiert une coordination entre vous-même et le tiers pour configurer les enregistrements DNS nécessaires. Aucune organisation ne le fait exactement de la même manière que les autres. Ainsi, le processus dépend entièrement de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="42481-p132">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service. This requires coordination between yourself and the third-party in order to set up the necessary DNS records. Some third-party servers can have their own CNAME records with different selectors. No two organizations do it exactly the same way. Instead, the process depends entirely on the organization.</span></span>

<span data-ttu-id="42481-265">Un exemple de message montrant un élément DKIM configuré correctement pour contoso.com et bulkemailprovider.com peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="42481-265">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>

```console
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="42481-266">Dans cet exemple, pour obtenir ce résultat :</span><span class="sxs-lookup"><span data-stu-id="42481-266">In this example, in order to achieve this result:</span></span>

1. <span data-ttu-id="42481-267">Le fournisseur de messagerie en masse a attribué à Contoso une clé DKIM publique.</span><span class="sxs-lookup"><span data-stu-id="42481-267">Bulk Email Provider gave Contoso a public DKIM key.</span></span>

2. <span data-ttu-id="42481-268">Contoso a publié la clé DKIM sur son enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="42481-268">Contoso published the DKIM key to its DNS record.</span></span>

3. <span data-ttu-id="42481-p133">Lorsque de l’envoi de courrier électronique, le fournisseur de messagerie en masse signe la clé avec la clé privée correspondante. Ainsi, le fournisseur de messagerie en masse joint la signature DKIM à l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="42481-p133">When sending email, Bulk Email Provider signs the key with the corresponding private key. By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>

4. <span data-ttu-id="42481-271">Les systèmes de messagerie de réception effectuent une vérification DKIM en authentifiant la valeur d=\<domain\>de l'option DKIM-Signature, en la comparant au domaine indiqué dans l'adresse From: (5322.From) du message.</span><span class="sxs-lookup"><span data-stu-id="42481-271">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message.</span></span> <span data-ttu-id="42481-272">Dans cet exemple, les valeurs sont les mêmes :</span><span class="sxs-lookup"><span data-stu-id="42481-272">In this example, the values match:</span></span>

   > <span data-ttu-id="42481-273">sender@**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="42481-273">sender@**contoso.com**</span></span>

   > <span data-ttu-id="42481-274">d=**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="42481-274">d=**contoso.com**</span></span>

## <a name="identify-domains-that-do-not-send-email"></a><span data-ttu-id="42481-275">Identifier les domaines qui n’envoient pas de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="42481-275">Identify domains that do not send email</span></span>

<span data-ttu-id="42481-276">Les organisations doivent indiquer de façon explicite si un domaine n’envoie pas de courrier électronique en spécifiant `v=DKIM1; p=` dans l’enregistrement DKIM de ces domaines.</span><span class="sxs-lookup"><span data-stu-id="42481-276">Organizations should explicitly state if a domain does not send email by specifying `v=DKIM1; p=` in the DKIM record for those domains.</span></span> <span data-ttu-id="42481-277">Cela indique aux serveurs de messagerie qu’il n’existe pas de clé publique valide pour le domaine, et que les courriers électroniques provenant de ce domaine doivent être rejetés.</span><span class="sxs-lookup"><span data-stu-id="42481-277">This advises receiving email servers that there are no valid public keys for the domain, and any email claiming to be from that domain should be rejected.</span></span> <span data-ttu-id="42481-278">Vous devez procéder de la sorte pour chaque domaine et sous-domaine à l’aide d’un DKIM avec caractère générique.</span><span class="sxs-lookup"><span data-stu-id="42481-278">You should do this for each domain and subdomain using a wildcard DKIM.</span></span>

<span data-ttu-id="42481-279">Par exemple, l’enregistrement DKIM se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="42481-279">For example, the DKIM record would look like this:</span></span>

```console
*._domainkey.SubDomainThatShouldntSendMail.contoso.com. TXT "v=DKIM1; p="
```

## <a name="next-steps-after-you-set-up-dkim-for-microsoft-365"></a><span data-ttu-id="42481-280">Étapes suivantes : après avoir configuré DKIM pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42481-280">Next steps: After you set up DKIM for Microsoft 365</span></span>
<span data-ttu-id="42481-281"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="42481-281"><a name="DKIMNextSteps"> </a></span></span>

<span data-ttu-id="42481-282">Bien que DKIM soit conçu pour éviter l’usurpation, DKIM fonctionne mieux avec SPF et DMARC.</span><span class="sxs-lookup"><span data-stu-id="42481-282">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC.</span></span> <span data-ttu-id="42481-283">Une fois que vous avez configuré DKIM, si vous n’avez pas encore configuré SPF, vous devez le faire.</span><span class="sxs-lookup"><span data-stu-id="42481-283">Once you have set up DKIM, if you have not already set up SPF you should do so.</span></span> <span data-ttu-id="42481-284">Pour consulter une brève présentation de SPF et le configurer rapidement, voir [Configurer SPF dans Microsoft 365 pour empêcher l’usurpation d’identité](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="42481-284">For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Microsoft 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="42481-285">Pour consulter des informations plus approfondies sur l’utilisation de SPF par Microsoft 365, la résolution des problèmes et les déploiements non standard tels que les déploiements hybrides, voir [Comment Microsoft 365 utilise SPF (Sender Policy Framework) pour empêcher l’usurpation d’identité](how-office-365-uses-spf-to-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="42481-285">For a more in-depth understanding of how Microsoft 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Microsoft 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="42481-286">Voir [Utiliser DMARC pour valider l’e-mail](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="42481-286">Next, see [Use DMARC to validate email](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="42481-287">[Les en-têtes des messages anti-courrier indésirable](anti-spam-message-headers.md) incluent la syntaxe et les champs d’en-tête utilisés par Microsoft 365 pour les contrôles DKIM.</span><span class="sxs-lookup"><span data-stu-id="42481-287">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Microsoft 365 for DKIM checks.</span></span>

## <a name="more-information"></a><span data-ttu-id="42481-288">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="42481-288">More information</span></span>

<span data-ttu-id="42481-289">Rotation des clés via PowerShell [Rotate-DkimSigningConfig](/powershell/module/exchange/rotate-dkimsigningconfig)</span><span class="sxs-lookup"><span data-stu-id="42481-289">Key rotation via PowerShell [Rotate-DkimSigningConfig](/powershell/module/exchange/rotate-dkimsigningconfig)</span></span>
