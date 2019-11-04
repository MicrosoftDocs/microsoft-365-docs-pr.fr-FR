---
title: Utiliser le service DKIM pour les e-mails dans votre domaine personnalisé dans Office 365, 2 048 bits, 1 024 bits, procédure, mode de fonctionnement, SPF, DMARC
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 10/8/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
ms.collection:
- M365-security-compliance
description: 'Résumé : Cet article décrit comment utiliser DKIM (DomainKeys Identified Mail) avec Office 365 pour vous assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine personnalisé.'
ms.openlocfilehash: 07cb90684bbbba4851697020ceac4756381f8b55
ms.sourcegitcommit: 333ecfb8bfeb34f9f08d82d295b40d37de6ba8b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/29/2019
ms.locfileid: "37772238"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a><span data-ttu-id="b1aae-103">Utiliser DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-103">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>

 <span data-ttu-id="b1aae-104">**Résumé :** cet article décrit comment utiliser DKIM (DomainKeys Identified Mail) avec Office 365 pour vous assurer que les systèmes de messagerie de destination approuvent les messages sortants envoyés à partir de votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b1aae-104">**Summary:** This article describes how you use DomainKeys Identified Mail (DKIM) with Office 365 to ensure that destination email systems trust messages sent outbound from your custom domain.</span></span>
  
<span data-ttu-id="b1aae-105">Vous devez utiliser DKIM en plus de SPF et DMARC pour empêcher les usurpateurs d’envoyer des messages qui semblent provenir de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="b1aae-105">You should use DKIM in addition to SPF and DMARC to help prevent spoofers from sending messages that look like they are coming from your domain.</span></span> <span data-ttu-id="b1aae-106">DKIM vous permet d'ajouter une signature numérique aux messages électroniques sortants dans l'en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="b1aae-106">DKIM lets you add a digital signature to outbound email messages in the message header.</span></span> <span data-ttu-id="b1aae-107">Cela peut paraître compliqué, mais ce n’est vraiment pas le cas.</span><span class="sxs-lookup"><span data-stu-id="b1aae-107">It may sound complicated, but it's really not.</span></span> <span data-ttu-id="b1aae-108">Lorsque vous configurez DKIM, vous autorisez votre domaine à associer ou signer son nom à un message électronique à l’aide d’une authentification de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="b1aae-108">When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message by using cryptographic authentication.</span></span> <span data-ttu-id="b1aae-109">Les systèmes de messagerie qui reçoivent des messages électroniques de votre domaine peuvent utiliser cette signature numérique pour déterminer si le courrier entrant est légitime.</span><span class="sxs-lookup"><span data-stu-id="b1aae-109">Email systems that receive email from your domain can use this digital signature to help determine if incoming email that they receive is legitimate.</span></span>
  
<span data-ttu-id="b1aae-110">En bref, vous utilisez une clé privée pour chiffrer l’en-tête du message électronique sortant de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="b1aae-110">Basically, you use a private key to encrypt the header in your domain's outgoing email.</span></span> <span data-ttu-id="b1aae-111">Vous publiez une clé publique sur les enregistrements DNS de votre domaine que les serveurs de réception peuvent utiliser pour décoder la signature.</span><span class="sxs-lookup"><span data-stu-id="b1aae-111">You publish a public key to your domain's DNS records that receiving servers can then use to decode the signature.</span></span> <span data-ttu-id="b1aae-112">Ils utilisent la clé publique pour vérifier que les messages sont réellement envoyés par vous et pas par une personne qui tente d'*usurper* votre domaine.</span><span class="sxs-lookup"><span data-stu-id="b1aae-112">They use the public key to verify that the messages are really coming from you and not coming from someone *spoofing* your domain.</span></span>
  
<span data-ttu-id="b1aae-113">Office 365 configure automatiquement DKIM pour les domaines initiaux 'onmicrosoft.com'.</span><span class="sxs-lookup"><span data-stu-id="b1aae-113">Office 365 automatically sets up DKIM for its initial 'onmicrosoft.com' domains.</span></span> <span data-ttu-id="b1aae-114">Cela signifie que vous n’avez rien à faire pour configurer DKIM pour les noms de domaine initial (ex.</span><span class="sxs-lookup"><span data-stu-id="b1aae-114">That means you don't need to do anything to set up DKIM for any initial domain names (ex.</span></span> <span data-ttu-id="b1aae-115">litware.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="b1aae-115">litware.onmicrosoft.com).</span></span> <span data-ttu-id="b1aae-116">Pour plus d'informations sur les domaines, consultez l'article [Forum aux questions sur les domaines](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="b1aae-116">For more information about domains, see [Domains FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>

<span data-ttu-id="b1aae-117">Vous pouvez également choisir de n'effectuer aucun réglage DKIM pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b1aae-117">You can choose to do nothing about DKIM for your custom domain too.</span></span> <span data-ttu-id="b1aae-118">Si vous ne configurez pas DKIM, Office 365 crée une paire de clés privée et publique, active la signature DKIM et configure la stratégie par défaut d'Office 365 pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b1aae-118">If you don't set up DKIM for your custom domain, Office 365 creates a private and public key pair, enables DKIM signing, and then configures the Office 365 default policy for your custom domain.</span></span> <span data-ttu-id="b1aae-119">Bien que cela soit suffisant pour la plupart des clients Office 365, vous devez configurer manuellement DKIM pour votre domaine personnalisé dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1aae-119">While this is sufficient coverage for most Office 365 customers, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>
  
- <span data-ttu-id="b1aae-120">Vous avez plusieurs domaines personnalisés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-120">You have more than one custom domain in Office 365</span></span>

- <span data-ttu-id="b1aae-121">Vous envisagez de configurer DMARC également (recommandé)</span><span class="sxs-lookup"><span data-stu-id="b1aae-121">You're going to set up DMARC too (recommended)</span></span>

- <span data-ttu-id="b1aae-122">Vous souhaitez contrôler votre clé privée</span><span class="sxs-lookup"><span data-stu-id="b1aae-122">You want control over your private key</span></span>

- <span data-ttu-id="b1aae-123">Vous souhaitez personnaliser vos enregistrements CNAME</span><span class="sxs-lookup"><span data-stu-id="b1aae-123">You want to customize your CNAME records</span></span>

- <span data-ttu-id="b1aae-124">Vous souhaitez configurer des clés DKIM pour les e-mails provenant d’un domaine tiers, par exemple, si vous utilisez un programme d’envoi de courrier en nombre tiers.</span><span class="sxs-lookup"><span data-stu-id="b1aae-124">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>

<span data-ttu-id="b1aae-125">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="b1aae-125">In this article:</span></span>
  
- [<span data-ttu-id="b1aae-126">Pourquoi DKIM est plus efficace que SPF seul pour empêcher l’usurpation d’identité malveillante dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-126">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)

- [<span data-ttu-id="b1aae-127">Mise à niveau manuelle de vos clés 1024 bits vers les clés de chiffrement DKIM 2048 bits</span><span class="sxs-lookup"><span data-stu-id="b1aae-127">Manually upgrade your 1024-bit keys to 2048-bit DKIM encryption keys</span></span>](use-dkim-to-validate-outbound-email.md#1024to2048DKIM)

- [<span data-ttu-id="b1aae-128">Étapes nécessaires pour configurer manuellement DKIM dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-128">Steps you need to do to manually set up DKIM in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)

- [<span data-ttu-id="b1aae-129">Configuration de DKIM pour plusieurs domaines personnalisés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-129">To configure DKIM for more than one custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)

- <span data-ttu-id="b1aae-130">Désactivation de la stratégie de signature DKIM pour un domaine personnalisé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-130">[Disabling the DKIM signing policy for a custom domain in Office 365](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)</span></span>

- <span data-ttu-id="b1aae-131">Comportement par défaut pour DKIM et Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-131">[Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)</span></span>

- <span data-ttu-id="b1aae-132">Configuration de DKIM permettant à un service tiers d’envoyer des courriers électroniques au nom de votre domaine personnalisé, ou d’usurper ce dernier</span><span class="sxs-lookup"><span data-stu-id="b1aae-132">[Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)</span></span>

- [<span data-ttu-id="b1aae-133">Étapes suivantes : après avoir configuré DKIM pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-133">Next steps: After you set up DKIM for Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)

> [!NOTE]
> <span data-ttu-id="b1aae-134">Microsoft 365 prend en charge l’utilisateur de l’option DKIM 1024 ou 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="b1aae-134">Microsoft 365 supports the user of either 1024- or 2048-bit DKIM.</span></span> <span data-ttu-id="b1aae-135">Si vous utilisez 1024 et que vous voulez configurer le processus DKIM 2048 bits, restez attentif aux étapes de la rotation de votre configuration de signature DKIM dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b1aae-135">If you're using 1024- and want to configure 2048-bit DKIM stay tuned for steps to rotate your DKIM signing configuration in this article.</span></span> <span data-ttu-id="b1aae-136">À la fin de l’année 2019, Microsoft prendra en charge les clés 2048 bits par défaut pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="b1aae-136">By the end of 2019, Microsoft will support 2048-bit keys by default, for all customers.</span></span> 

## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a><span data-ttu-id="b1aae-137">Pourquoi DKIM est plus efficace que SPF seul pour empêcher l’usurpation d’identité malveillant dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-137">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>
<span data-ttu-id="b1aae-138"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-138"><a name="HowDKIMWorks"> </a></span></span>

<span data-ttu-id="b1aae-p106">SPF ajoute des informations à une enveloppe de message, mais DKIM chiffre réellement une signature dans l’en-tête du message. Lorsque vous transférez un message, des parties de l’enveloppe de ce message peuvent être supprimées par le serveur de transfert. Étant donné que la signature numérique reste dans le message électronique, car elle fait partie de l’en-tête du message, DKIM fonctionne même lorsqu’un message a été transféré, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p106">SPF adds information to a message envelope but DKIM actually encrypts a signature within the message header. When you forward a message, portions of that message's envelope can be stripped away by the forwarding server. Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>
  
![Diagramme illustrant l’authentification DKIM correcte d’un message envoyé lors de l’échec du contrôle SPF](../media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
<span data-ttu-id="b1aae-p107">Dans cet exemple, si vous aviez publié un seul enregistrement SPF TXT pour votre domaine, le serveur de messagerie du destinataire pourrait avoir marqué vos messages électroniques comme du courrier indésirable et généré un résultat faux positif. L’ajout de DKIM dans ce scénario réduit le signalement de courrier indésirable faux positif. Étant donné que DKIM repose à la fois sur le chiffrement de clé publique et les adresses IP pour l’authentification, DKIM représente une forme d’authentification beaucoup plus puissante que SPF. Nous vous recommandons d’utiliser à la fois SPF, DKIM et DMARC dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p107">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result. The addition of DKIM in this scenario reduces false positive spam reporting. Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF. We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>
  
<span data-ttu-id="b1aae-p108">Détail important : DKIM utilise une clé privée pour insérer une signature chiffrée dans les en-têtes du message. Le domaine qui fournit la signature, aussi appelé domaine sortant, est inséré en tant que valeur du champ **d=** dans l’en-tête. Le domaine qui réalise la vérification, aussi appelé domaine du destinataire, utilise ensuite le champ **d=** pour rechercher la clé publique du système DNS et authentifier le message. Si le message est vérifié, la vérification DKIM a réussi.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p108">The nitty gritty: DKIM uses a private key to insert an encrypted signature into the message headers. The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header. The verifying domain, or recipient's domain, then use the **d=** field to look up the public key from DNS and authenticate the message. If the message is verified, the DKIM check passes.</span></span> 

## <a name="manually-upgrade-your-1024-bit-keys-to-2048-bit-dkim-encryption-keys"></a><span data-ttu-id="b1aae-151">Mise à niveau manuelle de vos clés 1024 bits vers les clés de chiffrement DKIM 2048 bits</span><span class="sxs-lookup"><span data-stu-id="b1aae-151">Manually upgrade your 1024-bit keys to 2048-bit DKIM encryption keys</span></span>
<span data-ttu-id="b1aae-152"><a name="1024to2048DKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-152"><a name="1024to2048DKIM"> </a></span></span>

<span data-ttu-id="b1aae-153">Étant donné que le nombre de bits 1024 et 2048 sont pris en charge pour les clés DKIM, ces instructions vous indiquent comment mettre à niveau votre clé 1024 bits vers 2048.</span><span class="sxs-lookup"><span data-stu-id="b1aae-153">Since both 1024 and 2048 bitness are supported for DKIM keys, these directions will tell you how to upgrade your 1024-bit key to 2048.</span></span> <span data-ttu-id="b1aae-154">Les étapes ci-dessous concernent deux cas d’utilisation ; veuillez choisir celui qui correspond le mieux à votre configuration.</span><span class="sxs-lookup"><span data-stu-id="b1aae-154">The steps below are for two use-cases, please choose the one that best fits your configuration.</span></span>

1. <span data-ttu-id="b1aae-155">Lorsque vous **avez déjà configuré DKIM**, vous pouvez faire pivoter le nombre de bits comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1aae-155">When you **already have DKIM configured**, you rotate bitness as follows:</span></span>
    1. <span data-ttu-id="b1aae-156">[Connectez-vous aux charges de travail Office 365 via PowerShell](https://docs.microsoft.com/fr-FR/office365/enterprise/powershell/connect-to-all-office-365-services-in-a-single-windows-powershell-window).</span><span class="sxs-lookup"><span data-stu-id="b1aae-156">[Connect to Office 365 workloads via PowerShell](https://docs.microsoft.com/fr-FR/office365/enterprise/powershell/connect-to-all-office-365-services-in-a-single-windows-powershell-window).</span></span> <span data-ttu-id="b1aae-157">(L’applet de commande provient d’Exchange Online.)</span><span class="sxs-lookup"><span data-stu-id="b1aae-157">(The cmdlet comes from Exchange Online.)</span></span>
    1. <span data-ttu-id="b1aae-158">Exécutez ensuite la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="b1aae-158">And then execute the following cmdlet:</span></span>

<span data-ttu-id="b1aae-159">&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Rotate-DkimSigningConfig -KeySize 2048 -Identity {Guid of the existing Signing Config}`</span><span class="sxs-lookup"><span data-stu-id="b1aae-159">&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Rotate-DkimSigningConfig -KeySize 2048 -Identity {Guid of the existing Signing Config}`</span></span>

1. <span data-ttu-id="b1aae-160">Ou pour une **nouvelle implémentation de DKIM** :</span><span class="sxs-lookup"><span data-stu-id="b1aae-160">Or for a **new implementation of DKIM**:</span></span>
    1. <span data-ttu-id="b1aae-161">[Connectez-vous aux charges de travail Office 365 via PowerShell](https://docs.microsoft.com/fr-FR/office365/enterprise/powershell/connect-to-all-office-365-services-in-a-single-windows-powershell-window).</span><span class="sxs-lookup"><span data-stu-id="b1aae-161">[Connect to Office 365 workloads via PowerShell](https://docs.microsoft.com/fr-FR/office365/enterprise/powershell/connect-to-all-office-365-services-in-a-single-windows-powershell-window).</span></span> <span data-ttu-id="b1aae-162">(Il s’agit d’une cmdlet Exchange Online).</span><span class="sxs-lookup"><span data-stu-id="b1aae-162">(This is an Exchange Online cmdlet.)</span></span>
    1. <span data-ttu-id="b1aae-163">Saisissez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="b1aae-163">Execute the following cmdlet:</span></span>

<span data-ttu-id="b1aae-164">&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `New-DkimSigningConfig -DomainName {Domain for which config is to be created} -KeySize 2048 -Enabled $True`</span><span class="sxs-lookup"><span data-stu-id="b1aae-164">&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `New-DkimSigningConfig -DomainName {Domain for which config is to be created} -KeySize 2048 -Enabled $True`</span></span>

<span data-ttu-id="b1aae-165">Restez connecté à Office 365 pour *vérifier* la configuration.</span><span class="sxs-lookup"><span data-stu-id="b1aae-165">Stay connected to Office 365 to *verify* the configuration.</span></span>

2. <span data-ttu-id="b1aae-166">Exécutez la cmdlet :</span><span class="sxs-lookup"><span data-stu-id="b1aae-166">Execute the cmdlet:</span></span>

<span data-ttu-id="b1aae-167">&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `Get-DkimSigningConfig | fl`</span><span class="sxs-lookup"><span data-stu-id="b1aae-167">&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `Get-DkimSigningConfig | fl`</span></span>

> [!TIP]
><span data-ttu-id="b1aae-168">Cette nouvelle clé 2048 bits prend effet sur RotateOnDate et envoie des e-mails avec la clé 1024 bits au niveau intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="b1aae-168">This new 2048-bit key takes effect on the RotateOnDate, and will send emails with the 1024-bit key in the interim.</span></span> <span data-ttu-id="b1aae-169">Après quatre jours, vous pouvez à nouveau effectuer un test à l’aide de la touche 2048 bits (autrement dit, une fois que la rotation prend effet sur le deuxième sélecteur).</span><span class="sxs-lookup"><span data-stu-id="b1aae-169">After four days, you can test again with the 2048-bit key (that is, once the rotation takes effect to the second selector).</span></span> 

<span data-ttu-id="b1aae-170">Si vous voulez faire pivoter vers le deuxième sélecteur, vos options sont a) laisser le service Office 365 faire pivoter le sélecteur et effectuer la mise à niveau vers le nombre de bits 2048 dans les 6 mois, ou b) après 4 jours et confirmation que le nombre de bits 2048 est utilisé, faire pivoter manuellement la deuxième touche du sélecteur en utilisant la cmdlet appropriée répertoriée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b1aae-170">If you want to rotate to the second selector, your options are a) let the Office 365 service rotate the selector and upgrade to 2048-bitness within the next 6 months, or b) after 4 days and confirming that 2048-bitness is in use, manually rotate the second selector key by using the appropriate cmdlet listed above.</span></span>

## <a name="steps-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a><span data-ttu-id="b1aae-171">Étapes nécessaires pour configurer manuellement DKIM dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-171">Steps you need to do to manually set up DKIM in Office 365</span></span>
<span data-ttu-id="b1aae-172"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-172"><a name="SetUpDKIMO365"> </a></span></span>

<span data-ttu-id="b1aae-173">Pour configurer DKIM, suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b1aae-173">To configure DKIM, you will complete these steps:</span></span>
  
- [<span data-ttu-id="b1aae-174">Publication de deux enregistrements CNAME pour votre domaine personnalisé dans le système DNS</span><span class="sxs-lookup"><span data-stu-id="b1aae-174">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)

- [<span data-ttu-id="b1aae-175">Activation de la signature DKIM pour votre domaine personnalisé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-175">Enable DKIM signing for your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)

### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="b1aae-176">Publication de deux enregistrements CNAME pour votre domaine dans le système DNS</span><span class="sxs-lookup"><span data-stu-id="b1aae-176">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="b1aae-177"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-177"><a name="Publish2CNAME"> </a></span></span>

<span data-ttu-id="b1aae-178">Pour chaque domaine auquel vous souhaitez ajouter une signature DKIM dans le système DNS, vous devez publier deux enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="b1aae-178">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records.</span></span> 

<span data-ttu-id="b1aae-179">Exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1aae-179">Run the following commands:</span></span>

```powershell
    New-DkimSigningConfig -DomainName <domain> -Enabled $false   
    Get-DkimSigningConfig -Identity <domain> | fl Selector1CNAME, Selector2CNAME
```

<span data-ttu-id="b1aae-180">Créer des CNAMes référencés dans une sortie de commande Get-DkimSigningConfig</span><span class="sxs-lookup"><span data-stu-id="b1aae-180">Create CNAMEs referenced in Get-DkimSigningConfig output</span></span>

```powershell
    Set-DkimSigningConfig -Identity <domain> -Enabled $true
```
<span data-ttu-id="b1aae-181">Les enregistrements CNAME dans votre DNS pointent vers des enregistrements TXT DKIM qui existent déjà dans le DNS sur les serveurs DNS Microsoft pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1aae-181">The CNAME records in your DNS will point to already created A records that exist in DNS on the Microsoft DNS servers for Office 365.</span></span>
  
<span data-ttu-id="b1aae-p113">Office 365 effectue une rotation automatique des clés à l’aide des deux enregistrements que vous établissez. Si vous avez configuré des domaines personnalisés en plus du domaine initial dans Office 365, vous devez publier deux enregistrements CNAME pour chaque domaine supplémentaire. Par conséquent, si vous avez deux domaines, vous devez publier deux enregistrements CNAME supplémentaires, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p113">Office 365 performs automatic key rotation using the two records that you establish. If you have provisioned custom domains in addition to the initial domain in Office 365, you must publish two CNAME records for each additional domain. So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span>
  
<span data-ttu-id="b1aae-185">Utilisez le format suivant pour les enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="b1aae-185">Use the following format for the CNAME records.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1aae-186">Si vous êtes l’un de nos clients GCC High, nous calculons _domainGuid_ différemment.</span><span class="sxs-lookup"><span data-stu-id="b1aae-186">If you are one of our GCC High customers, we calculate _domainGuid_ differently!</span></span> <span data-ttu-id="b1aae-187">Au lieu de rechercher l’enregistrement MX pour votre _initialDomain_ afin de calculer _domainGuid_, nous le calculons directement à partir du domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b1aae-187">Instead of looking up the MX record for your _initialDomain_ to calculate _domainGuid_, instead we calculate it directly from the customized domain.</span></span> <span data-ttu-id="b1aae-188">Par exemple, si votre domaine personnalisé est « contoso.com », les points étant remplacés par des tirets, votre domainGuid devient « contoso-com ».</span><span class="sxs-lookup"><span data-stu-id="b1aae-188">For example, if your customized domain is "contoso.com" your domainGuid becomes "contoso-com", any periods are replaced with a dash.</span></span> <span data-ttu-id="b1aae-189">Par conséquent, quel que soit l’enregistrement MX sur lequel pointe votre initialDomain, vous devez toujours utiliser la méthode ci-dessus pour calculer la domainGuid à utiliser dans vos enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="b1aae-189">So, regardless of what MX record your initialDomain points to, you’ll always use the above method to calculate the domainGuid to use in your CNAME records.</span></span>

```text
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

<span data-ttu-id="b1aae-190">Où :</span><span class="sxs-lookup"><span data-stu-id="b1aae-190">Where:</span></span>
  
- <span data-ttu-id="b1aae-191">Pour Office 365, les sélecteurs seront toujours « selector1 » ou « selector2 ».</span><span class="sxs-lookup"><span data-stu-id="b1aae-191">For Office 365, the selectors will always be "selector1" or "selector2".</span></span>

- <span data-ttu-id="b1aae-192">_domainGUID_ est identique à  _domainGUID_ dans l’enregistrement MX personnalisé pour votre domaine personnalisé figurant devant mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="b1aae-192">_domainGUID_ is the same as the _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com.</span></span> <span data-ttu-id="b1aae-193">Par exemple, dans l’enregistrement MX suivant pour le domaine contoso.com, le _domainGUID_ est contoso-com :</span><span class="sxs-lookup"><span data-stu-id="b1aae-193">For example, in the following MX record for the domain contoso.com, the _domainGUID_ is contoso-com:</span></span> 
    
    ```text
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- <span data-ttu-id="b1aae-194">_initialDomain_ est le domaine que vous avez utilisé lorsque vous vous êtes inscrit à Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1aae-194">_initialDomain_ is the domain that you used when you signed up for Office 365.</span></span> <span data-ttu-id="b1aae-195">Les domaines initiaux se terminent toujours par onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="b1aae-195">Initial domains always end in onmicrosoft.com.</span></span> <span data-ttu-id="b1aae-196">Pour plus d’informations sur la détermination de votre [domaine initial](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain), voir Forum aux questions sur les domaines.</span><span class="sxs-lookup"><span data-stu-id="b1aae-196">For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>

<span data-ttu-id="b1aae-197">Par exemple, si vous avez un domaine initial cohovineyardandwinery.onmicrosoft.com, ainsi que deux domaines personnalisés cohovineyard.com et cohowinery.com, vous devez configurer deux enregistrements CNAME pour chaque domaine supplémentaire, soit un total de quatre enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="b1aae-197">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>
  
```text
Host name:          selector1._domainkey
Points to address or value: selector1-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector1._domainkey
Points to address or value: selector1-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a><span data-ttu-id="b1aae-198">Activation de la signature DKIM pour votre domaine personnalisé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-198">Enable DKIM signing for your custom domain in Office 365</span></span>
<span data-ttu-id="b1aae-199"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-199"><a name="EnableDKIMinO365"> </a></span></span>

<span data-ttu-id="b1aae-200">Une fois que vous avez publié les enregistrements CNAME dans le système DNS, vous êtes prêt à activer la signature DKIM par l’intermédiaire d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1aae-200">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Office 365.</span></span> <span data-ttu-id="b1aae-201">Vous pouvez effectuer cette action par le biais du Centre d’administration Microsoft 365 ou à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1aae-201">You can do this either through the Microsoft 365 admin center or by using PowerShell.</span></span>
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-admin-center"></a><span data-ttu-id="b1aae-202">Activation de la signature DKIM pour votre domaine personnalisé par l’intermédiaire du Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="b1aae-202">To enable DKIM signing for your custom domain through the admin center</span></span>

1. <span data-ttu-id="b1aae-203">[Connectez-vous à Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) à l’aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="b1aae-203">[Sign in to Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span> 

2. <span data-ttu-id="b1aae-204">Sélectionnez l’icône du lanceur d’applications située en haut à gauche et choisissez **Administrateur**.</span><span class="sxs-lookup"><span data-stu-id="b1aae-204">Select the app launcher icon in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="b1aae-205">Dans le volet de navigation en bas à gauche, développez **Administrateur** et choisissez **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="b1aae-205">In the lower-left navigation, expand **Admin** and choose **Exchange**.</span></span>

4. <span data-ttu-id="b1aae-206">Accédez à **Protection** > \>dkim\*\*.</span><span class="sxs-lookup"><span data-stu-id="b1aae-206">Go to **Protection** \> **dkim**.</span></span>

5. <span data-ttu-id="b1aae-p118">Sélectionnez le domaine pour lequel vous souhaitez activer DKIM, puis pour **Signer les messages pour ce domaine avec des signatures DKIM**, choisissez **Activer**. Répétez cette étape pour chaque domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p118">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**. Repeat this step for each custom domain.</span></span>

#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="b1aae-209">Activation de la signature DKIM pour votre domaine personnalisé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1aae-209">To enable DKIM signing for your custom domain by using PowerShell</span></span>

1. <span data-ttu-id="b1aae-210">[Connectez-vous à Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1aae-210">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>

2. <span data-ttu-id="b1aae-211">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1aae-211">Run the following command:</span></span>

    ```powershell
    Set-DkimSigningConfig -Identity <domain> -Enabled $true
    ```

   <span data-ttu-id="b1aae-212">Où _domain_ est le nom du domaine personnalisé pour lequel vous souhaitez activer la signature DKIM.</span><span class="sxs-lookup"><span data-stu-id="b1aae-212">Where _domain_ is the name of the custom domain that you want to enable DKIM signing for.</span></span> 

   <span data-ttu-id="b1aae-213">Par exemple, pour le domaine contoso.com :</span><span class="sxs-lookup"><span data-stu-id="b1aae-213">For example, for the domain contoso.com:</span></span>
   
   ```powershell
    Set-DkimSigningConfig -Identity contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a><span data-ttu-id="b1aae-214">Confirmation du fait que la signature DKIM est correctement configurée pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-214">To Confirm DKIM signing is configured properly for Office 365</span></span>

<span data-ttu-id="b1aae-p119">Patientez quelques minutes avant de suivre ces étapes permettant de confirmer que vous avez correctement configuré DKIM. Cela donne le temps aux informations DKIM relatives au domaine de se propager dans l’ensemble du réseau.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p119">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM. This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>
  
- <span data-ttu-id="b1aae-217">Envoyez un message à partir d’un compte au sein de votre domaine Office 365 compatible avec DKIM à un autre compte de messagerie, tel qu’outlook.com ou Hotmail.com.</span><span class="sxs-lookup"><span data-stu-id="b1aae-217">Send a message from an account within your Office 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>

- <span data-ttu-id="b1aae-p120">N’utilisez pas un compte aol.com à des fins de test. Il est possible qu’AOL ignore la vérification DKIM si la vérification SPF aboutit. Cela annule votre test.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p120">Do not use an aol.com account for testing purposes. AOL may skip the DKIM check if the SPF check passes. This will nullify your test.</span></span>

- <span data-ttu-id="b1aae-p121">Ouvrez le message et examinez l’en-tête. Les instructions pour afficher l’en-tête du message varient en fonction de votre client de messagerie. Pour obtenir des instructions sur l’affichage des en-têtes de messages dans Outlook, consultez l’article [](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C)Afficher des en-têtes de messages électroniqueshttps://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p121">Open the message and look at the header. Instructions for viewing the header for the message will vary depending on your messaging client. For instructions on viewing message headers in Outlook, see [View e-mail message headers](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span></span>

  <span data-ttu-id="b1aae-p122">Le message signé par DKIM contient le domaine et le nom d’hôte que vous avez définis lorsque vous avez publié les entrées CNAME. Le message se présente un peu comme cet exemple :</span><span class="sxs-lookup"><span data-stu-id="b1aae-p122">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries. The message will look something like this example:</span></span>
    
    ```text
    From: Example User <example@contoso.com>
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed;
        s=selector1; d=contoso.com; t=1429912795;
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type;
        bh=<body hash>;
        b=<signed field>;
    ```

- <span data-ttu-id="b1aae-p123">Recherchez l’en-tête des résultats de l’authentification. Bien que chaque service de réception utilise un format légèrement différent pour apposer un cachet sur le courrier entrant, le résultat doit inclure un élément qui ressemble à **DKIM=test** ou **DKIM=OK**.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p123">Look for the Authentication-Results header. While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span>

## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a><span data-ttu-id="b1aae-228">Configuration de DKIM pour plusieurs domaines personnalisés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-228">To configure DKIM for more than one custom domain in Office 365</span></span>
<span data-ttu-id="b1aae-229"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-229"><a name="DKIMMultiDomain"> </a></span></span>

<span data-ttu-id="b1aae-p124">Si un jour vous décidez d’ajouter un autre domaine personnalisé et que vous souhaitez activer DKIM pour ce nouveau domaine, vous devez effectuer les étapes décrites dans cet article pour chaque domaine. Plus spécifiquement, réalisez toutes les étapes indiquées dans la section [Configuration manuelle de DKIM dans Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span><span class="sxs-lookup"><span data-stu-id="b1aae-p124">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain. Specifically, complete all steps in [What you need to do to manually set up DKIM in Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a><span data-ttu-id="b1aae-232">Désactivation de la stratégie de signature DKIM pour un domaine personnalisé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-232">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>
<span data-ttu-id="b1aae-233"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-233"><a name="DisableDKIMSigningPolicy"> </a></span></span>

<span data-ttu-id="b1aae-p125">La désactivation de la stratégie de signature ne désactive pas complètement DKIM. Après un certain temps, Office 365 applique automatiquement la stratégie Office 365 par défaut pour votre domaine. Pour plus d’informations, voir [Comportement par défaut pour Exchange Online Protection (EOP) et Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span><span class="sxs-lookup"><span data-stu-id="b1aae-p125">Disabling the signing policy does not completely disable DKIM. After a period of time, Office 365 will automatically apply the default Office 365 policy for your domain. For more information, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="b1aae-237">Pour désactiver la stratégie de signature DKIM à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1aae-237">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="b1aae-238">[Connectez-vous à Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1aae-238">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>

2. <span data-ttu-id="b1aae-239">Exécutez l’une des commandes suivantes pour chaque domaine pour lequel vous souhaitez désactiver la signature DKIM.</span><span class="sxs-lookup"><span data-stu-id="b1aae-239">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>
    
    ```powershell
    $p = Get-DkimSigningConfig -Identity <domain>
    $p[0] | Set-DkimSigningConfig -Enabled $false
    ```
   
   <span data-ttu-id="b1aae-240">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1aae-240">For example:</span></span>
    
    ```powershell
    $p = Get-DkimSigningConfig -Identity contoso.com
    $p[0] | Set-DkimSigningConfig -Enabled $false
    ```

   <span data-ttu-id="b1aae-241">Ou</span><span class="sxs-lookup"><span data-stu-id="b1aae-241">Or</span></span>
    
    ```powershell
    Set-DkimSigningConfig -Identity $p[<number>].Identity -Enabled $false
    ```

    <span data-ttu-id="b1aae-242">Où _number_ est l’index de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b1aae-242">Where _number_ is the index of the policy.</span></span> <span data-ttu-id="b1aae-243">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1aae-243">For example:</span></span>
    
    ```powershell
    Set-DkimSigningConfig -Identity $p[0].Identity -Enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a><span data-ttu-id="b1aae-244">Comportement par défaut pour DKIM et Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-244">Default behavior for DKIM and Office 365</span></span>
<span data-ttu-id="b1aae-245"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-245"><a name="DefaultDKIMbehavior"> </a></span></span>

<span data-ttu-id="b1aae-246">Si vous n’activez pas DKIM, Office 365 crée automatiquement une clé publique DKIM 1024 bits pour votre domaine par défaut et la clé privée associée que nous stockons en interne dans notre centre de données.</span><span class="sxs-lookup"><span data-stu-id="b1aae-246">If you do not enable DKIM, Office 365 automatically creates a 1024-bit DKIM public key for your default domain and the associated private key which we store internally in our datacenter.</span></span> <span data-ttu-id="b1aae-247">Par défaut, Office 365 utilise une configuration de signature par défaut pour les domaines ne disposant d’aucune stratégie définie.</span><span class="sxs-lookup"><span data-stu-id="b1aae-247">By default, Office 365 uses a default signing configuration for domains that do not have a policy in place.</span></span> <span data-ttu-id="b1aae-248">Cela signifie que si vous ne configurez pas DKIM vous-même, Office 365 utilise sa stratégie par défaut et les clés qu’il crée pour activer DKIM sur votre domaine.</span><span class="sxs-lookup"><span data-stu-id="b1aae-248">This means that if you do not set up DKIM yourself, Office 365 will use its default policy and keys it creates in order to enable DKIM for your domain.</span></span>
  
<span data-ttu-id="b1aae-249">En outre, si vous désactivez la signature DKIM, après un certain temps, Office 365 applique automatiquement sa stratégie par défaut pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="b1aae-249">Also, if you disable DKIM signing after enabling it, after a period of time, Office 365 will automatically apply the Office 365 default policy for your domain.</span></span>
  
<span data-ttu-id="b1aae-p128">Dans l’exemple suivant, supposons que DKIM pour fabrikam.com a été activé par Office 365 et pas par l’administrateur du domaine. Cela signifie que les enregistrements CNAME requis n’existent pas dans le système DNS. Les signatures DKIM pour les courriers électroniques provenant de ce domaine se présenteront comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1aae-p128">In the following example, suppose that DKIM for fabrikam.com was enabled by Office 365, not by the administrator of the domain. This means that the required CNAMEs do not exist in DNS. DKIM signatures for email from this domain will look something like this:</span></span>
  
```text
From: Second Example <second.example@fabrikam.com>
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed;
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795;
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type;
    bh=<body hash>;
    b=<signed field>;
```

<span data-ttu-id="b1aae-p129">Dans cet exemple, le domaine et le nom d’hôte contiennent les valeurs vers lesquelles l’enregistrement CNAME pointerait si la signature DKIM pour fabrikam.com avait été activée par l’administrateur du domaine. Au bout d’un certain temps, chaque message envoyé à partir d’Office 365 comportera une signature DKIM. Si vous activez DKIM vous-même, le domaine est identique à celui de l’adresse de l’expéditeur, ici fabrikam.com. Dans le cas contraire, DKIM ne s’aligne pas et utilise le domaine initial de votre organisation. Pour plus d’informations sur la façon de déterminer votre domaine initial, consultez la rubrique [](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)Forum aux questions sur les domaineshttps://support.office.com/fr-fr/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p129">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator. Eventually, every single message sent from Office 365 will be DKIM-signed. If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com. If you don't, it will not align and instead will use your organization's initial domain. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="b1aae-258">Configurer DKIM de sorte qu’un service tiers puisse envoyer du courrier au nom de votre domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="b1aae-258">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="b1aae-259"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-259"><a name="SetUp3rdPartyspoof"> </a></span></span>

<span data-ttu-id="b1aae-p130">Certains fournisseurs de services de messagerie en masse ou de services SaaS vous permettent de configurer des clés DKIM pour les courriers électroniques qui proviennent de leur service. Cela requiert une coordination entre vous-même et le tiers pour configurer les enregistrements DNS nécessaires. Aucune organisation ne le fait exactement de la même manière que les autres. Ainsi, le processus dépend entièrement de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p130">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service. This requires coordination between yourself and the third-party in order to set up the necessary DNS records. No two organizations do it exactly the same way. Instead, the process depends entirely on the organization.</span></span>
  
<span data-ttu-id="b1aae-264">Un exemple de message montrant un élément DKIM configuré correctement pour contoso.com et bulkemailprovider.com peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1aae-264">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>
  
```text
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="b1aae-265">Dans cet exemple, pour obtenir ce résultat :</span><span class="sxs-lookup"><span data-stu-id="b1aae-265">In this example, in order to achieve this result:</span></span>
  
1. <span data-ttu-id="b1aae-266">Le fournisseur de messagerie en masse a attribué à Contoso une clé DKIM publique.</span><span class="sxs-lookup"><span data-stu-id="b1aae-266">Bulk Email Provider gave Contoso a public DKIM key.</span></span>

2. <span data-ttu-id="b1aae-267">Contoso a publié la clé DKIM sur son enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="b1aae-267">Contoso published the DKIM key to its DNS record.</span></span>

3. <span data-ttu-id="b1aae-p131">Lorsque de l’envoi de courrier électronique, le fournisseur de messagerie en masse signe la clé avec la clé privée correspondante. Ainsi, le fournisseur de messagerie en masse joint la signature DKIM à l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="b1aae-p131">When sending email, Bulk Email Provider signs the key with the corresponding private key. By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>

4. <span data-ttu-id="b1aae-p132">Les systèmes de messagerie de réception effectuent une vérification DKIM en authentifiant la valeur d=<domaine> de l’option DKIM-Signature, en la comparant au domaine indiqué dans l’adresse From: (5322.From) du message. Dans cet exemple, les valeurs sont les mêmes :</span><span class="sxs-lookup"><span data-stu-id="b1aae-p132">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message. In this example, the values match:</span></span>

    <span data-ttu-id="b1aae-272">sender@**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="b1aae-272">sender@**contoso.com**</span></span>

    <span data-ttu-id="b1aae-273">d=**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="b1aae-273">d=**contoso.com**</span></span>

## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a><span data-ttu-id="b1aae-274">Étapes suivantes : après avoir configuré DKIM pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b1aae-274">Next steps: After you set up DKIM for Office 365</span></span>
<span data-ttu-id="b1aae-275"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="b1aae-275"><a name="DKIMNextSteps"> </a></span></span>

<span data-ttu-id="b1aae-276">Bien que DKIM soit conçu pour éviter l’usurpation, DKIM fonctionne mieux avec SPF et DMARC.</span><span class="sxs-lookup"><span data-stu-id="b1aae-276">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC.</span></span> <span data-ttu-id="b1aae-277">Une fois que vous avez configuré DKIM, si vous n’avez pas encore configuré SPF, vous devez le faire.</span><span class="sxs-lookup"><span data-stu-id="b1aae-277">Once you have set up DKIM, if you have not already set up SPF you should do so.</span></span> <span data-ttu-id="b1aae-278">Pour consulter une brève présentation de SPF et le configurer rapidement, voir [Configurer SPF dans Office 365 pour empêcher l’usurpation d’identité](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span><span class="sxs-lookup"><span data-stu-id="b1aae-278">For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="b1aae-279">Pour consulter des informations plus approfondies sur l’utilisation de SPF par Office 365, la résolution des problèmes et les déploiements non standard tels que les déploiements hybrides, voir Comment Office 365 utilise SPF (Sender Policy Framework) pour empêcher l’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="b1aae-279">For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="b1aae-280">voir Utiliser DMARC pour valider les e-mails dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1aae-280">Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="b1aae-281">[ comprend la syntaxe et les champs d’en-tête utilisés par Office 365 pour les vérifications DMARC.</span><span class="sxs-lookup"><span data-stu-id="b1aae-281">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DKIM checks.</span></span>
