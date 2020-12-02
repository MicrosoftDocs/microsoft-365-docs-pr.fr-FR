---
title: Sécurité par défaut dans Office 365
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: En savoir plus sur le paramètre sécurisé par défaut dans Exchange Online Protection (EOP)
ms.openlocfilehash: 1a68c14a2d37f1fc3bfb032c4d3ca34c09a89890
ms.sourcegitcommit: 4cbb4ec26f022f5f9d9481f55a8a6ee8406968d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/01/2020
ms.locfileid: "49527768"
---
# <a name="secure-by-default-in-office-365"></a><span data-ttu-id="8ffae-103">Sécurité par défaut dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8ffae-103">Secure by default in Office 365</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]
[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8ffae-104">« Sécurisé par défaut » est un terme utilisé pour définir les paramètres par défaut les plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="8ffae-104">"Secure by default" is a term used to define the default settings that are most secure as possible.</span></span>

<span data-ttu-id="8ffae-105">Toutefois, la sécurité doit être équilibrée en termes de productivité.</span><span class="sxs-lookup"><span data-stu-id="8ffae-105">However, security needs to be balanced with productivity.</span></span> <span data-ttu-id="8ffae-106">Cela peut inclure l’équilibrage entre :</span><span class="sxs-lookup"><span data-stu-id="8ffae-106">This can include balancing across:</span></span>

- <span data-ttu-id="8ffae-107">Convivialité : les paramètres ne doivent pas bénéficier du mode de productivité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ffae-107">Usability: settings should not get in the way of user productivity.</span></span>
- <span data-ttu-id="8ffae-108">Risque : la sécurité peut bloquer des activités importantes.</span><span class="sxs-lookup"><span data-stu-id="8ffae-108">Risk: security might block important activities.</span></span>
- <span data-ttu-id="8ffae-109">Paramètres hérités : il est possible que certaines configurations pour des produits et des fonctionnalités plus anciens doivent être conservées pour des raisons professionnelles, même si les nouveaux paramètres modernes sont améliorés.</span><span class="sxs-lookup"><span data-stu-id="8ffae-109">Legacy settings: Some configurations for older products and features might need to be maintained for business reasons, even if new, modern settings are improved.</span></span>

<span data-ttu-id="8ffae-110">Les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online sont protégées par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="8ffae-110">Microsoft 365 organizations with mailboxes in Exchange Online are protected by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="8ffae-111">Cette protection inclut :</span><span class="sxs-lookup"><span data-stu-id="8ffae-111">This protection includes:</span></span>

1. <span data-ttu-id="8ffae-112">Les messages électroniques avec un programme malveillant suspectés seront automatiquement mis en quarantaine et les destinataires seront avertis.</span><span class="sxs-lookup"><span data-stu-id="8ffae-112">Email with suspected malware will automatically be quarantined and recipients will be notified.</span></span> <span data-ttu-id="8ffae-113">Consultez la rubrique [configure anti-malware Policies in EOP](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8ffae-113">See [Configure anti-malware policies in EOP](configure-anti-malware-policies.md).</span></span>
1. <span data-ttu-id="8ffae-114">Les e-mails de hameçonnage identifiés comme « à fiabilité élevée » seront gérés conformément à l’action de la stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="8ffae-114">Phishing email identified as "high confidence" will be handled according to the anti-spam policy action.</span></span> <span data-ttu-id="8ffae-115">Consultez la rubrique [configurer des stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8ffae-115">See [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="8ffae-116">Étant donné que Microsoft souhaite assurer la sécurité de nos clients par défaut, certains remplacements de locataire ne sont pas appliqués pour les programmes malveillants ou le hameçonnage à haut niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="8ffae-116">Because Microsoft wants to keep our customers secure by default, some tenants overrides are not applied for malware or high confidence phishing.</span></span> <span data-ttu-id="8ffae-117">Ces substitutions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ffae-117">These overrides include:</span></span>

- <span data-ttu-id="8ffae-118">Listes d’expéditeurs autorisés ou listes de domaines autorisés (stratégies anti-courrier indésirable)</span><span class="sxs-lookup"><span data-stu-id="8ffae-118">Allowed sender lists or allowed domain lists (anti-spam policies)</span></span>
- <span data-ttu-id="8ffae-119">Expéditeurs approuvés Outlook</span><span class="sxs-lookup"><span data-stu-id="8ffae-119">Outlook Safe senders</span></span>
- <span data-ttu-id="8ffae-120">Liste d’adresses IP autorisées (filtrage des connexions)</span><span class="sxs-lookup"><span data-stu-id="8ffae-120">IP Allow List (connection filtering)</span></span>

<span data-ttu-id="8ffae-121">Vous trouverez plus d’informations sur ces substitutions dans la [liste créer des listes d’expéditeurs approuvés](create-safe-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="8ffae-121">More information on these overrides can be found in [Create safe sender lists](create-safe-sender-lists-in-office-365.md).</span></span>

<span data-ttu-id="8ffae-122">Sécurisé par défaut il ne s’agit pas d’un paramètre qui peut être activé ou désactivé, mais de la façon dont notre filtrage fonctionne de la manière à ce que les messages potentiellement dangereux ou indésirables soient conservés de vos boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8ffae-122">Secure by default here is not a setting that could be turned on or off, but the way our filtering works out of the box to keep potentially dangerous or unwanted messages out of your mailboxes.</span></span> <span data-ttu-id="8ffae-123">Les logiciels malveillants et le hameçonnage à haut niveau de fiabilité doivent être mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="8ffae-123">Malware and high confidence phishing should be sent to quarantine.</span></span> <span data-ttu-id="8ffae-124">Seuls les administrateurs peuvent gérer les messages mis en quarantaine en tant que programmes malveillants ou hameçonnage à haut niveau de confiance, et ils peuvent également signaler des faux positifs à Microsoft à partir de là.</span><span class="sxs-lookup"><span data-stu-id="8ffae-124">Only admins can manage messages that were quarantined as malware or high confidence phishing and they can also report false positives to Microsoft from there.</span></span> <span data-ttu-id="8ffae-125">Pour plus d’informations, consultez la rubrique [gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans EOP](manage-quarantined-messages-and-files.md) .</span><span class="sxs-lookup"><span data-stu-id="8ffae-125">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md)</span></span>

## <a name="exceptions"></a><span data-ttu-id="8ffae-126">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8ffae-126">Exceptions</span></span>

<span data-ttu-id="8ffae-127">La seule substitution qui permet de contourner le message de hameçonnage pour contourner le filtrage est celle des règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="8ffae-127">The only override that allows high confidence phishing message to bypass filtering is Exchange mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="8ffae-128">Pour utiliser des règles de flux de messagerie pour contourner le filtrage, consultez [la rubrique use mail Flow Rules to Set the SCL in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span><span class="sxs-lookup"><span data-stu-id="8ffae-128">To use mail flow rules to bypass filtering, see [Use mail flow rules to set the SCL in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span></span>

<span data-ttu-id="8ffae-129">Les substitutions doivent être utilisées uniquement pour :</span><span class="sxs-lookup"><span data-stu-id="8ffae-129">Overrides should only be used for:</span></span>

- <span data-ttu-id="8ffae-130">Simulations d’hameçonnage : les attaques simulées peuvent vous aider à identifier les utilisateurs vulnérables avant qu’une attaque réelle n’influe sur votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8ffae-130">Phishing simulations: simulated attacks can help you identify vulnerable users before a real attack impacts your organization.</span></span>
- <span data-ttu-id="8ffae-131">Boîtes aux lettres de sécurité/COP : boîtes aux lettres dédiées utilisées par les équipes de sécurité pour obtenir des messages non filtrés (à la fois bon et mauvais).</span><span class="sxs-lookup"><span data-stu-id="8ffae-131">Security/SecOps mailboxes: dedicated mailboxes used by security teams to get unfiltered messages (both good and bad).</span></span> <span data-ttu-id="8ffae-132">Teams peut ensuite vérifier s’il contient du contenu malveillant.</span><span class="sxs-lookup"><span data-stu-id="8ffae-132">Teams can then review to see if they contain malicious content.</span></span>
- <span data-ttu-id="8ffae-133">Filtres tiers : certains fournisseurs tiers vont recommander de désactiver EOP (SCL =-1) car le filtre tiers gérera le filtrage du courrier.</span><span class="sxs-lookup"><span data-stu-id="8ffae-133">Third-party filters: some third-party vendors will recommend turning off EOP (SCL=-1) as the third-party filter will manage the mail filtering.</span></span> <span data-ttu-id="8ffae-134">Microsoft ne recommande pas de désactiver EOP au fur et à mesure que EOP est requis pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="8ffae-134">Microsoft does not recommend turning off EOP as EOP is required for Defender for Office 365.</span></span> <span data-ttu-id="8ffae-135">Au lieu de cela, nous vous recommandons d’activer le [filtrage amélioré pour les connecteurs](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) à la place.</span><span class="sxs-lookup"><span data-stu-id="8ffae-135">Instead, the recommendation here is to turn on [Enhanced Filtering for Connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) instead.</span></span>
- <span data-ttu-id="8ffae-136">Faux positifs : vous pouvez autoriser certains messages qui sont toujours analysés par Microsoft [via des soumissions d’administration](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="8ffae-136">False positives: you may want to allow certain messages that are still being analyzed by Microsoft [via Admin submissions](admin-submission.md).</span></span> <span data-ttu-id="8ffae-137">Comme pour toutes les substitutions, il est recommandé qu’elles soient temporaires.</span><span class="sxs-lookup"><span data-stu-id="8ffae-137">As with all overrides, it is recommended that they are temporary.</span></span>
