---
title: Commencer à utiliser la formation à la simulation d’attaque
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser la formation sur la simulation d’attaques pour exécuter des attaques par hameçonnage simulé et par mot de passe dans leurs organisations Microsoft 365 E5 ou Microsoft Defender pour Office 365 Plan 2.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6e344153ef433bc13b16136e584ec4da73fcef6a
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50921347"
---
# <a name="get-started-using-attack-simulation-training"></a><span data-ttu-id="89e93-103">Commencer à utiliser la formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="89e93-103">Get started using Attack simulation training</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="89e93-104">Si votre organisation dispose de Microsoft 365 E5 ou Microsoft Defender [](office-365-ti.md)pour Office 365 Plan 2, qui inclut des fonctionnalités d’examen et de réponse aux menaces, vous pouvez utiliser une formation sur la simulation d’attaques dans le Centre de sécurité Microsoft pour exécuter des scénarios d’attaque réalistes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="89e93-104">If your organization has Microsoft 365 E5 or Microsoft Defender for Office 365 Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack simulation training in the Microsoft Security Center to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="89e93-105">Ces attaques simulées peuvent vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle n’impacte votre ligne de bas de page.</span><span class="sxs-lookup"><span data-stu-id="89e93-105">These simulated attacks can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="89e93-106">Pour en savoir plus, lisez cet article.</span><span class="sxs-lookup"><span data-stu-id="89e93-106">Read this article to learn more.</span></span>

> [!NOTE]
> <span data-ttu-id="89e93-107">L’entraînement de simulation d’attaque remplace l’ancienne expérience du Simulateur d’attaques v1 décrite dans le Simulateur d’attaques dans [Microsoft Defender pour Office 365.](attack-simulator.md)</span><span class="sxs-lookup"><span data-stu-id="89e93-107">Attack simulation training replaces the old Attack Simulator v1 experience that's described in [Attack Simulator in Microsoft Defender for Office 365](attack-simulator.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="89e93-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="89e93-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="89e93-109">Pour ouvrir le Centre de sécurité Microsoft, allez sur <https://security.microsoft.com/> .</span><span class="sxs-lookup"><span data-stu-id="89e93-109">To open the Microsoft Security Center, go to <https://security.microsoft.com/>.</span></span> <span data-ttu-id="89e93-110">Une formation sur la simulation d’attaques est disponible dans la formation sur la simulation d’attaques de **messagerie** et de \> **collaboration.**</span><span class="sxs-lookup"><span data-stu-id="89e93-110">Attack simulation training is available at **Email and collaboration** \> **Attack simulation training**.</span></span> <span data-ttu-id="89e93-111">Pour aller directement à la formation sur la simulation d’attaque, ouvrez <https://security.microsoft.com/attacksimulator> .</span><span class="sxs-lookup"><span data-stu-id="89e93-111">To go directly to Attack simulation training, open <https://security.microsoft.com/attacksimulator>.</span></span>

- <span data-ttu-id="89e93-112">Pour plus d’informations sur la disponibilité de la formation sur la simulation d’attaques dans différents abonnements Microsoft 365, voir la description du service Microsoft Defender pour [Office 365.](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)</span><span class="sxs-lookup"><span data-stu-id="89e93-112">For more information about the availability of Attack simulation training across different Microsoft 365 subscriptions, see [Microsoft Defender for Office 365 service description](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="89e93-113">Des autorisations doivent vous être attribuées dans le Centre de sécurité & conformité ou dans Azure Active Directory avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="89e93-113">You need to be assigned permissions in the Security & Compliance Center or in Azure Active Directory before you can do the procedures in this article.</span></span> <span data-ttu-id="89e93-114">Plus précisément, vous devez être membre de la gestion de l’organisation, de l’administrateur de la sécurité ou de l’un des rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="89e93-114">Specifically, you need to be a member of **Organization Management**, **Security Administrator**, or one of the following roles:</span></span>
  - <span data-ttu-id="89e93-115">**Administrateurs du simulateur d’attaques**: créez et gérez tous les aspects des campagnes de simulation d’attaques.</span><span class="sxs-lookup"><span data-stu-id="89e93-115">**Attack Simulator Administrators**: Create and managed all aspects of attack simulation campaigns.</span></span>
  - <span data-ttu-id="89e93-116">**Auteurs de charge utile du simulateur d’attaques**: créent des charges utiles d’attaque qu’un administrateur peut lancer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="89e93-116">**Attack Simulator Payload Authors**: Create attack payloads that an admin can initiate later.</span></span>

  <span data-ttu-id="89e93-117">Pour plus d’informations, [voir Autorisations dans](permissions-in-the-security-and-compliance-center.md) le Centre de sécurité & conformité ou à [propos des rôles d’administrateur.](../../admin/add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="89e93-117">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) or [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

- <span data-ttu-id="89e93-118">Il n’existe aucune cmdlet PowerShell correspondante pour la formation à la simulation d’attaques.</span><span class="sxs-lookup"><span data-stu-id="89e93-118">There are no corresponding PowerShell cmdlets for Attack simulation training.</span></span>

- <span data-ttu-id="89e93-119">Les données associées à la simulation d’attaque et à la formation sont stockées avec d’autres données client pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="89e93-119">Attack simulation and training related data is stored with other customer data for Microsoft 365 services.</span></span> <span data-ttu-id="89e93-120">Pour plus d’informations, voir emplacements de données [Microsoft 365.](../../enterprise/o365-data-locations.md)</span><span class="sxs-lookup"><span data-stu-id="89e93-120">For more information see [Microsoft 365 data locations](../../enterprise/o365-data-locations.md).</span></span> <span data-ttu-id="89e93-121">La simulation d’attaque est disponible dans les régions suivantes : NAM, APC, EUR, IND, CAN, AUS, FRA, GBR, JPN et KOR.</span><span class="sxs-lookup"><span data-stu-id="89e93-121">Attack simulation is available in the following regions: NAM, APC, EUR, IND, CAN, AUS, FRA, GBR, JPN, and KOR.</span></span>

## <a name="simulations"></a><span data-ttu-id="89e93-122">Simulations</span><span class="sxs-lookup"><span data-stu-id="89e93-122">Simulations</span></span>

<span data-ttu-id="89e93-123">Le *Hameçonnage* est un terme générique qui décrit les attaques par courrier électronique tentant d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="89e93-123">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="89e93-124">*Le hameçonnage* fait partie d’un sous-ensemble de techniques que nous classons en _tant qu’ingénierie sociale._</span><span class="sxs-lookup"><span data-stu-id="89e93-124">*Phishing* is a part of a subset of techniques we classify as _social engineering_.</span></span>

<span data-ttu-id="89e93-125">Dans la formation à la simulation d’attaques, plusieurs types de techniques d’ingénierie sociale sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="89e93-125">In Attack simulation training, multiple types of social engineering techniques are available:</span></span>

- <span data-ttu-id="89e93-126">**Informations d’identification**: une personne malveillante envoie au destinataire un message contenant une URL.</span><span class="sxs-lookup"><span data-stu-id="89e93-126">**Credential harvest**: An attacker sends the recipient a message that contains a URL.</span></span> <span data-ttu-id="89e93-127">Lorsque le destinataire clique sur l’URL, il est redéliqué sur un site web qui affiche généralement une boîte de dialogue qui demande à l’utilisateur son nom d’utilisateur et son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="89e93-127">When the recipient clicks on the URL, they're taken to a website that typically shows a dialog box that asks the user for their username and password.</span></span> <span data-ttu-id="89e93-128">En règle générale, la page de destination est un site web connu pour créer une relation d’confiance avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89e93-128">Typically, the destination page is themed to represent a well-known website in order to build trust in the user.</span></span>

- <span data-ttu-id="89e93-129">**Pièce jointe malveillante**: une personne malveillante envoie au destinataire un message contenant une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="89e93-129">**Malware attachment**: An attacker sends the recipient a message that contains an attachment.</span></span> <span data-ttu-id="89e93-130">Lorsque le destinataire ouvre la pièce jointe, du code arbitraire (par exemple, une macro) est exécuté sur l’appareil de l’utilisateur pour permettre à l’attaquant d’installer du code supplémentaire ou de s’en empêcher.</span><span class="sxs-lookup"><span data-stu-id="89e93-130">When the recipient opens the attachment, arbitrary code (for example, a macro) is run on the user's device to help the attacker install additional code or further entrench themselves.</span></span>

- <span data-ttu-id="89e93-131">**Lien dans la pièce** jointe : il s’agit d’un hybride de la saisie des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="89e93-131">**Link in attachment**: This is a hybrid of a credential harvest.</span></span> <span data-ttu-id="89e93-132">Une personne malveillante envoie au destinataire un message contenant une URL à l’intérieur d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="89e93-132">An attacker sends the recipient a message that contains a URL inside of an attachment.</span></span> <span data-ttu-id="89e93-133">Lorsque le destinataire ouvre la pièce jointe et clique sur l’URL, il est redéliqué sur un site web qui affiche généralement une boîte de dialogue qui demande à l’utilisateur son nom d’utilisateur et son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="89e93-133">When the recipient opens the attachment and clicks on the URL, they're taken to a website that typically shows a dialog box that asks the user for their username and password.</span></span> <span data-ttu-id="89e93-134">En règle générale, la page de destination est un site web connu pour créer une relation d’confiance avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89e93-134">Typically, the destination page is themed to represent a well-known website in order to build trust in the user.</span></span>

- <span data-ttu-id="89e93-135">**Lien vers** un programme malveillant : une personne malveillante envoie au destinataire un message contenant un lien vers une pièce jointe sur un site de partage de fichiers connu (par exemple, SharePoint Online ou Dropbox).</span><span class="sxs-lookup"><span data-stu-id="89e93-135">**Link to malware**: An attacker sends the recipient a message that contains a link to an attachment on a well-known file sharing site (for example, SharePoint Online or Dropbox).</span></span> <span data-ttu-id="89e93-136">Lorsque le destinataire clique sur l’URL, la pièce jointe s’ouvre et un code arbitraire (par exemple, une macro) est exécuté sur l’appareil de l’utilisateur pour aider l’attaquant à installer du code supplémentaire ou à s’en aller.</span><span class="sxs-lookup"><span data-stu-id="89e93-136">When the recipient clicks on the URL, the attachment opens and arbitrary code (for example, a macro) is run on the user's device to help the attacker install additional code or further entrench themselves.</span></span>

- <span data-ttu-id="89e93-137">**Lecteur par URL**: une personne malveillante envoie au destinataire un message contenant une URL.</span><span class="sxs-lookup"><span data-stu-id="89e93-137">**Drive-by-url**: An attacker sends the recipient a messages that contains a URL.</span></span> <span data-ttu-id="89e93-138">Lorsque le destinataire clique sur l’URL, il est dirigé vers un site web qui tente d’exécuter du code d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="89e93-138">When the recipient clicks on the URL, they're taken to a website that tries to run background code.</span></span> <span data-ttu-id="89e93-139">Ce code en arrière-plan tente de collecter des informations sur le destinataire ou de déployer du code arbitraire sur son appareil.</span><span class="sxs-lookup"><span data-stu-id="89e93-139">This background code attempts to gather information about the recipient or deploy arbitrary code on their device.</span></span> <span data-ttu-id="89e93-140">En règle générale, le site web de destination est un site web connu compromis ou un clone d’un site web connu.</span><span class="sxs-lookup"><span data-stu-id="89e93-140">Typically, the destination website is a well-known website that has been compromised or a clone of a well-known website.</span></span> <span data-ttu-id="89e93-141">La connaissance du site web permet de convaincre l’utilisateur que le lien peut être cliqué en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="89e93-141">Familiarity with the website helps convince the user that the link is safe to click.</span></span> <span data-ttu-id="89e93-142">Cette technique est également connue sous le nom d’attaque par trous _d’eau._</span><span class="sxs-lookup"><span data-stu-id="89e93-142">This technique is also known as a _watering hole attack_.</span></span>

> [!NOTE]
> <span data-ttu-id="89e93-143">Vérifiez la disponibilité de l’URL de hameçonnage simulé dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="89e93-143">Check the availability of the simulated phishing URL in your supported web browsers before you use the URL in a phishing campaign.</span></span> <span data-ttu-id="89e93-144">Bien que nous travaillions avec de nombreux fournisseurs de réputation d’URL pour toujours autoriser ces URL de simulation, nous n’avons pas toujours une couverture complète (par exemple, La navigation sécurisée Google).</span><span class="sxs-lookup"><span data-stu-id="89e93-144">While we work with many URL reputation vendors to always allow these simulation URLs, we don't always have full coverage (for example, Google Safe Browsing).</span></span> <span data-ttu-id="89e93-145">La plupart des fournisseurs fournissent des conseils qui vous permettent de toujours autoriser des URL spécifiques (par exemple, <https://support.google.com/chrome/a/answer/7532419> ).</span><span class="sxs-lookup"><span data-stu-id="89e93-145">Most vendors provide guidance that allows you to always allow specific URLs (for example, <https://support.google.com/chrome/a/answer/7532419>).</span></span>

<span data-ttu-id="89e93-146">Les URL utilisées par la formation à la simulation d’attaque sont décrites dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="89e93-146">The URLs that are used by Attack simulation training are described in the following list:</span></span>

- <https://www.mcsharepoint.com>
- <https://www.attemplate.com>
- <https://www.doctricant.com>
- <https://www.mesharepoint.com>
- <https://www.officence.com>
- <https://www.officenced.com>
- <https://www.officences.com>
- <https://www.officentry.com>
- <https://www.officested.com>
- <https://www.prizegives.com>
- <https://www.prizemons.com>
- <https://www.prizewel.com>
- <https://www.prizewings.com>
- <https://www.shareholds.com>
- <https://www.sharepointen.com>
- <https://www.sharepointin.com>
- <https://www.sharepointle.com>
- <https://www.sharesbyte.com>
- <https://www.sharession.com>
- <https://www.sharestion.com>
- <https://www.templateau.com>
- <https://www.templatent.com>
- <https://www.templatern.com>
- <https://www.windocyte.com>

### <a name="create-a-simulation"></a><span data-ttu-id="89e93-147">Créer une simulation</span><span class="sxs-lookup"><span data-stu-id="89e93-147">Create a simulation</span></span>

<span data-ttu-id="89e93-148">Pour obtenir des instructions détaillées sur la création et l’envoi d’une nouvelle simulation, voir [Simuler une attaque par hameçonnage.](attack-simulation-training.md)</span><span class="sxs-lookup"><span data-stu-id="89e93-148">For step by step instructions on how to create and send a new simulation, see [Simulate a phishing attack](attack-simulation-training.md).</span></span>

### <a name="create-a-payload"></a><span data-ttu-id="89e93-149">Créer une charge utile</span><span class="sxs-lookup"><span data-stu-id="89e93-149">Create a payload</span></span>

<span data-ttu-id="89e93-150">Pour obtenir des instructions détaillées sur la création d’une charge utile à utiliser dans une simulation, voir Créer une charge utile personnalisée pour la formation à la [simulation d’attaques.](attack-simulation-training-payloads.md)</span><span class="sxs-lookup"><span data-stu-id="89e93-150">For step by step instructions on how to create a payload for use within a simulation, see [Create a custom payload for Attack simulation training](attack-simulation-training-payloads.md).</span></span>

### <a name="gaining-insights"></a><span data-ttu-id="89e93-151">Obtenir des informations</span><span class="sxs-lookup"><span data-stu-id="89e93-151">Gaining insights</span></span>

<span data-ttu-id="89e93-152">Pour obtenir des instructions détaillées sur la façon d’obtenir des informations sur les rapports, voir Obtenir des informations via une formation à la [simulation d’attaques.](attack-simulation-training-insights.md)</span><span class="sxs-lookup"><span data-stu-id="89e93-152">For step by step instructions on how to gain insights with reporting, see [Gain insights through Attack simulation training](attack-simulation-training-insights.md).</span></span>

> [!NOTE]
> <span data-ttu-id="89e93-153">Le Simulateur d’attaques utilise des liens sécurisés dans Defender pour Office 365 pour suivre en toute sécurité les données de clic pour l’URL du message de charge utile envoyé aux destinataires ciblés d’une campagne de hameçonnage, même si le paramètre Ne pas suivre les clics de l’utilisateur dans les stratégies de liens **sécurisés** est allumé.</span><span class="sxs-lookup"><span data-stu-id="89e93-153">Attack Simulator uses Safe Links in Defender for Office 365 to securely track click data for the URL in the payload message that's sent to targeted recipients of a phishing campaign, even if the **Do not track user clicks** setting in Safe Links policies is turned on.</span></span>