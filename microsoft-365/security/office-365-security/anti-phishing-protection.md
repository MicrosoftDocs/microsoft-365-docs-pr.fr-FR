---
title: Protection anti-hameçonnage
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
- MET150
ms.assetid: 75af74b2-c7ea-4556-a912-8c48e07271d3
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- TopSMBIssues
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur les fonctionnalités de protection anti-hameçonnage dans Exchange Online Protection (EOP) et Office 365 Advanced Threat Protection (Office 365 ATP).
ms.openlocfilehash: ca8b41c46a2d903edf0beae1de2334bd8c8d1e78
ms.sourcegitcommit: 9a764c2aed7338c37f6e92f5fb487f02b3c4dfa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48446962"
---
# <a name="anti-phishing-protection-in-microsoft-365"></a><span data-ttu-id="6201e-103">Protection anti-hameçonnage dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6201e-103">Anti-phishing protection in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="6201e-104">Le *Hameçonnage* est une attaque par courrier électronique qui tente d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="6201e-104">*Phishing* is an email attack that tries to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="6201e-105">Il existe des catégories spécifiques de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6201e-105">There are specific categories of phishing.</span></span> <span data-ttu-id="6201e-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6201e-106">For example:</span></span>

- <span data-ttu-id="6201e-107">Le **Spear Phishing** de la sonde utilise du contenu personnalisé qui est spécifiquement adapté aux destinataires ciblés (en général, après la reconnaissance des destinataires par l’agresseur).</span><span class="sxs-lookup"><span data-stu-id="6201e-107">**Spear phishing** uses focused, customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

- <span data-ttu-id="6201e-108">La **baleine** est dirigée vers des cadres ou d’autres objectifs de grande valeur au sein d’une organisation pour un maximum d’effets.</span><span class="sxs-lookup"><span data-stu-id="6201e-108">**Whaling** is directed at executives or other high value targets within an organization for maximum effect.</span></span>

- <span data-ttu-id="6201e-109">La compromission de la **messagerie professionnelle (bec)** utilise des expéditeurs falsifiés (des responsables financiers, des clients, des partenaires approuvés, etc.) pour inciter les destinataires à approuver les paiements, transférer des fonds ou révéler des données client.</span><span class="sxs-lookup"><span data-stu-id="6201e-109">**Business email compromise (BEC)** uses forged trusted senders (financial officers, customers, trusted partners, etc.) to trick recipients into approving payments, transferring funds, or revealing customer data.</span></span>

- <span data-ttu-id="6201e-110">**Ransomware** qui chiffre vos données et demande un paiement pour les déchiffrer presque toujours dans les messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6201e-110">**Ransomware** that encrypts your data and demands payment to decrypt it almost always starts out in phishing messages.</span></span> <span data-ttu-id="6201e-111">La protection anti-hameçonnage ne peut pas vous aider à déchiffrer les fichiers chiffrés, mais elle peut vous aider à détecter les messages de hameçonnage initiaux associés à la campagne de ransomware.</span><span class="sxs-lookup"><span data-stu-id="6201e-111">Anti-phishing protection can't help you decrypt encrypted files, but it can help detect the initial phishing messages that are associated with the ransomware campaign.</span></span> <span data-ttu-id="6201e-112">Pour plus d’informations sur la récupération d’une attaque par ransomware, consultez [la rubrique relative à la récupération à partir d’une attaque par ransomware dans Microsoft 365](recover-from-ransomware.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-112">For more information about recovering from a ransomware attack, see [Recover from a ransomware attack in Microsoft 365](recover-from-ransomware.md).</span></span>

<span data-ttu-id="6201e-113">Avec la complexité croissante des attaques, il est même difficile pour les utilisateurs formés d’identifier les messages de hameçonnage sophistiqués.</span><span class="sxs-lookup"><span data-stu-id="6201e-113">With the growing complexity of attacks, it's even difficult for trained users to identify sophisticated phishing messages.</span></span> <span data-ttu-id="6201e-114">Heureusement, Exchange Online Protection (EOP) et les fonctionnalités supplémentaires d’Office 365 Advanced Threat Protection (Office 365 ATP) peuvent vous aider.</span><span class="sxs-lookup"><span data-stu-id="6201e-114">Fortunately, Exchange Online Protection (EOP) and the additional features in Office 365 Advanced Threat Protection (Office 365 ATP) can help.</span></span>

## <a name="anti-phishing-protection-in-eop"></a><span data-ttu-id="6201e-115">Protection anti-hameçonnage dans EOP</span><span class="sxs-lookup"><span data-stu-id="6201e-115">Anti-phishing protection in EOP</span></span>

<span data-ttu-id="6201e-116">EOP (les organisations Microsoft 365 sans ATP) contient des fonctionnalités qui peuvent vous aider à protéger votre organisation contre les menaces de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="6201e-116">EOP (that is, Microsoft 365 organizations without ATP) contains features that can help protect your organization from phishing threats:</span></span>

- <span data-ttu-id="6201e-117">**Veille contre l’usurpation d’identité** : passez en revue les messages usurpant une identité provenant des expéditeurs dans les domaines internes et externes, et autorisez ou bloquez ces expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="6201e-117">**Spoof intelligence**: Review spoofed messages from senders in internal and external domains, and allow or block those senders.</span></span> <span data-ttu-id="6201e-118">Pour plus d’informations, consultez la rubrique [configure usurpation Intelligence in EOP](learn-about-spoof-intelligence.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-118">For more information, see [Configure spoof intelligence in EOP](learn-about-spoof-intelligence.md).</span></span>

- <span data-ttu-id="6201e-119">**Stratégies de détection d’hameçonnage dans EOP**: activation ou désactivation de l’intelligence des usurpations, activation ou désactivation de l’identification des expéditeurs non authentifiés dans Outlook, et spécification de l’action pour les expéditeurs usurpés bloqués (déplacer vers le dossier courrier indésirable ou mise en quarantaine).</span><span class="sxs-lookup"><span data-stu-id="6201e-119">**Anti-phishing policies in EOP**: Turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and specify the action for blocked spoofed senders (move to Junk Email folder or quarantine).</span></span> <span data-ttu-id="6201e-120">Pour plus d’informations, consultez la rubrique [configure anti-phishing Policies in EOP](configure-anti-phishing-policies-eop.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-120">For more information, see [Configure anti-phishing policies in EOP](configure-anti-phishing-policies-eop.md).</span></span>

- <span data-ttu-id="6201e-121">**Authentification de messagerie implicite**: EOP améliore les vérifications d’authentification de messagerie standard pour le courrier électronique entrant ([SPF](set-up-spf-in-office-365-to-help-prevent-spoofing.md), [DKIM](use-dkim-to-validate-outbound-email.md)et [DMARC](use-dmarc-to-validate-email.md)), avec la réputation de l’expéditeur, l’historique des destinataires, l’analyse comportementale et d’autres techniques avancées pour identifier les expéditeurs falsifiés.</span><span class="sxs-lookup"><span data-stu-id="6201e-121">**Implicit email authentication**: EOP enhances standard email authentication checks for inbound email ([SPF](set-up-spf-in-office-365-to-help-prevent-spoofing.md), [DKIM](use-dkim-to-validate-outbound-email.md), and [DMARC](use-dmarc-to-validate-email.md)) with sender reputation, sender history, recipient history, behavioral analysis, and other advanced techniques to help identify forged senders.</span></span> <span data-ttu-id="6201e-122">Si vous souhaitez en savoir plus, consultez la page [Authentification de messagerie électronique dans Microsoft 365](email-validation-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-122">For more information, see [Email authentication in Microsoft 365](email-validation-and-authentication.md).</span></span>

## <a name="additional-anti-phishing-protection-in-office-365-atp"></a><span data-ttu-id="6201e-123">Protection supplémentaire contre le hameçonnage dans Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="6201e-123">Additional anti-phishing protection in Office 365 ATP</span></span>

<span data-ttu-id="6201e-124">Office 365 - Protection avancée contre les menaces inclut des fonctionnalités anti-hameçonnage supplémentaires et plus avancées :</span><span class="sxs-lookup"><span data-stu-id="6201e-124">Office 365 ATP contains additional and more advanced anti-phishing features:</span></span>

- <span data-ttu-id="6201e-125">**Stratégies anti-hameçonnage ATP**: créez de nouvelles stratégies personnalisées, configurez les paramètres d’emprunt d’identité (protéger les utilisateurs et les domaines de l’emprunt d’identité), les paramètres d’intelligence de boîte aux lettres et les seuils de phishing avancés ajustables.</span><span class="sxs-lookup"><span data-stu-id="6201e-125">**ATP anti-phishing policies**: Create new custom policies, configure anti-impersonation settings (protect users and domains from impersonation), mailbox intelligence settings, and adjustable advanced phishing thresholds.</span></span> <span data-ttu-id="6201e-126">Pour plus d’informations, reportez-vous à la rubrique [configure ATP anti-phishing Policies in Microsoft 365](configure-atp-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-126">For more information, see [Configure ATP anti-phishing policies in Microsoft 365](configure-atp-anti-phishing-policies.md).</span></span> <span data-ttu-id="6201e-127">Pour plus d’informations sur les différences entre les stratégies anti-hameçonnage et les stratégies anti-hameçonnage ATP, consultez la rubrique [anti-phishing Policies in Microsoft 365](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-127">For more information about the differences between anti-phishing policies and ATP anti-phishing policies, see [Anti-phishing policies in Microsoft 365](set-up-anti-phishing-policies.md).</span></span>

- <span data-ttu-id="6201e-128">**Vues de campagne**: l’apprentissage automatique et d’autres heuristiques identifient et analysent les messages impliqués dans des attaques de hameçonnage coordonné contre l’ensemble du service et de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6201e-128">**Campaign Views**: Machine learning and other heuristics identify and analyze messages that are involved in coordinated phishing attacks against the entire service and your organization.</span></span> <span data-ttu-id="6201e-129">Pour plus d’informations, voir [campagne views in Office 365 DAV](campaigns.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-129">For more information, see [Campaign Views in Office 365 ATP](campaigns.md).</span></span>

- <span data-ttu-id="6201e-130">**Simulateur d’attaque**: les administrateurs peuvent créer des messages d’hameçonnage factices et les envoyer à des utilisateurs internes en tant qu’outil d’éducation.</span><span class="sxs-lookup"><span data-stu-id="6201e-130">**Attack simulator**: Admins can create fake phishing messages and send them to internal users as an education tool.</span></span> <span data-ttu-id="6201e-131">Pour plus d’informations, reportez-vous à la rubrique [Attack Simulator in Office 365 ATP](attack-simulator.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-131">For more information, see [Attack Simulator in Office 365 ATP](attack-simulator.md).</span></span>

## <a name="other-anti-phishing-resources"></a><span data-ttu-id="6201e-132">Autres ressources anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="6201e-132">Other anti-phishing resources</span></span>

- <span data-ttu-id="6201e-133">Pour les utilisateurs finaux : [Protégez-vous des schémas de hameçonnage et d’autres formes de fraude en ligne](https://support.microsoft.com/office/be0de46a-29cd-4c59-aaaf-136cf177d593).</span><span class="sxs-lookup"><span data-stu-id="6201e-133">For end users: [Protect yourself from phishing schemes and other forms of online fraud](https://support.microsoft.com/office/be0de46a-29cd-4c59-aaaf-136cf177d593).</span></span>

- <span data-ttu-id="6201e-134">[Comment Microsoft 365 valide l’adresse de pour empêcher le hameçonnage](how-office-365-validates-the-from-address.md).</span><span class="sxs-lookup"><span data-stu-id="6201e-134">[How Microsoft 365 validates the From address to prevent phishing](how-office-365-validates-the-from-address.md).</span></span>
