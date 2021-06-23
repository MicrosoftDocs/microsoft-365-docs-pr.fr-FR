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
ms.openlocfilehash: ad86f77399cfa2a3a780d3fed7e483e3c11bc08d
ms.sourcegitcommit: cd55fe6abe25b1e4f5fbe8295d3a99aebd97ce66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53082899"
---
# <a name="get-started-using-attack-simulation-training"></a><span data-ttu-id="a3c7b-103">Commencer à utiliser la formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="a3c7b-103">Get started using Attack simulation training</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="a3c7b-104">**S’applique** [à Microsoft Defender pour Office 365 plan 2](defender-for-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-104">**Applies to** [Microsoft Defender for Office 365 plan 2](defender-for-office-365.md)</span></span>

<span data-ttu-id="a3c7b-105">Si votre organisation Microsoft 365 E5 ou Microsoft Defender pour Office 365 Plan 2, qui inclut des fonctionnalités d’investigation et de réponse aux [menaces,](office-365-ti.md)vous pouvez utiliser la formation sur la simulation d’attaques dans le portail Microsoft 365 Defender pour exécuter des scénarios d’attaques réalistes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-105">If your organization has Microsoft 365 E5 or Microsoft Defender for Office 365 Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack simulation training in the Microsoft 365 Defender portal to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="a3c7b-106">Ces attaques simulées peuvent vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle n’impacte votre ligne de bas de page.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-106">These simulated attacks can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="a3c7b-107">Pour en savoir plus, lisez cet article.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-107">Read this article to learn more.</span></span>

> [!NOTE]
> <span data-ttu-id="a3c7b-108">L’entraînement de simulation d’attaque remplace l’ancienne expérience du Simulateur d’attaques v1 décrite dans le Simulateur d’attaques [dans Microsoft Defender pour Office 365](attack-simulator.md).</span><span class="sxs-lookup"><span data-stu-id="a3c7b-108">Attack simulation training replaces the old Attack Simulator v1 experience that's described in [Attack Simulator in Microsoft Defender for Office 365](attack-simulator.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a3c7b-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a3c7b-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a3c7b-110">Pour ouvrir le Portail Microsoft 365 Defender, accédez à <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-110">To open the Microsoft 365 Defender portal, go to <https://security.microsoft.com>.</span></span> <span data-ttu-id="a3c7b-111">Une formation sur la simulation d’attaques est disponible dans la formation sur la simulation d’attaques de **messagerie** et de \> **collaboration.**</span><span class="sxs-lookup"><span data-stu-id="a3c7b-111">Attack simulation training is available at **Email and collaboration** \> **Attack simulation training**.</span></span> <span data-ttu-id="a3c7b-112">Pour aller directement à la formation sur la simulation d’attaque, ouvrez <https://security.microsoft.com/attacksimulator> .</span><span class="sxs-lookup"><span data-stu-id="a3c7b-112">To go directly to Attack simulation training, open <https://security.microsoft.com/attacksimulator>.</span></span>

- <span data-ttu-id="a3c7b-113">Pour plus d’informations sur la disponibilité de la formation sur la simulation d’attaques dans différents abonnements Microsoft 365, voir Microsoft Defender pour obtenir [la description Office 365 service.](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-113">For more information about the availability of Attack simulation training across different Microsoft 365 subscriptions, see [Microsoft Defender for Office 365 service description](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="a3c7b-114">Des autorisations doivent vous être attribuées dans le portail Microsoft 365 Defender ou dans Azure Active Directory avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-114">You need to be assigned permissions in the Microsoft 365 Defender portal or in Azure Active Directory before you can do the procedures in this article.</span></span> <span data-ttu-id="a3c7b-115">Plus précisément, vous devez être membre de la gestion de l’organisation, de l’administrateur de la sécurité ou de l’un des rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="a3c7b-115">Specifically, you need to be a member of **Organization Management**, **Security Administrator**, or one of the following roles:</span></span>
  - <span data-ttu-id="a3c7b-116">**Administrateurs du simulateur d’attaques**: créez et gérez tous les aspects des campagnes de simulation d’attaques.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-116">**Attack Simulator Administrators**: Create and managed all aspects of attack simulation campaigns.</span></span>
  - <span data-ttu-id="a3c7b-117">**Auteurs de charge utile du simulateur d’attaques**: créent des charges utiles d’attaque qu’un administrateur peut lancer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-117">**Attack Simulator Payload Authors**: Create attack payloads that an admin can initiate later.</span></span>

  <span data-ttu-id="a3c7b-118">Pour plus d’informations, [voir Autorisations dans](permissions-microsoft-365-security-center.md) le portail Microsoft 365 Defender ou [à propos des rôles d’administrateur.](../../admin/add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-118">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md) or [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

- <span data-ttu-id="a3c7b-119">Il n’existe aucune cmdlet PowerShell correspondante pour la formation à la simulation d’attaques.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-119">There are no corresponding PowerShell cmdlets for Attack simulation training.</span></span>

- <span data-ttu-id="a3c7b-120">Les données associées à la simulation d’attaque et à la formation sont stockées avec d’autres données client pour Microsoft 365 services.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-120">Attack simulation and training related data is stored with other customer data for Microsoft 365 services.</span></span> <span data-ttu-id="a3c7b-121">Pour plus [d’informations, Microsoft 365 des emplacements de données.](../../enterprise/o365-data-locations.md)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-121">For more information see [Microsoft 365 data locations](../../enterprise/o365-data-locations.md).</span></span> <span data-ttu-id="a3c7b-122">La simulation d’attaque est disponible dans les régions suivantes : NAM, APC, EUR, IND, CAN, AUS, FRA, GBR, JPN et KOR.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-122">Attack simulation is available in the following regions: NAM, APC, EUR, IND, CAN, AUS, FRA, GBR, JPN, and KOR.</span></span>

- <span data-ttu-id="a3c7b-123">Depuis le 15 juin 2021, la formation sur la simulation d’attaques est disponible Cloud de la communauté du secteur public.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-123">As of June 15 2021, Attack simulation training is available in GCC.</span></span> <span data-ttu-id="a3c7b-124">Si votre organisation Office 365 Cloud de la communauté du secteur public G5 ou Microsoft Defender pour Office 365 (Plan 2) pour le gouvernement, vous pouvez utiliser une formation sur la simulation d’attaques dans le portail Microsoft 365 Defender pour exécuter des scénarios d’attaque réaliste dans votre organisation, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-124">If your organization has Office 365 G5 GCC or Microsoft Defender for Office 365 (Plan 2) for Government, you can use Attack simulation training in the Microsoft 365 Defender portal to run realistic attack scenarios in your organization as described in this article.</span></span> <span data-ttu-id="a3c7b-125">La formation à la simulation d’attaques n’est pas encore disponible Cloud de la communauté du secteur public environnements Élevé ou DoD.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-125">Attack simulation training is not yet available in GCC High or DoD environments.</span></span>

> [!NOTE]
> <span data-ttu-id="a3c7b-126">La formation à la simulation d’attaques offre un sous-ensemble de fonctionnalités aux clients E3 en tant qu’essai.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-126">Attack simulation training offers a subset of capabilities to E3 customers as a trial.</span></span> <span data-ttu-id="a3c7b-127">L’offre d’évaluation offre la possibilité d’utiliser une charge utile de la campagne de données d’identification et la possibilité de sélectionner des expériences de formation « ISA Phishing » ou « Hameçonnage de marché de masse ».</span><span class="sxs-lookup"><span data-stu-id="a3c7b-127">The trial offering contains the ability to use a Credential Harvest payload and the ability to select 'ISA Phishing' or 'Mass Market Phishing' training experiences.</span></span> <span data-ttu-id="a3c7b-128">Aucune autre fonctionnalité ne fait partie de l’offre d’essai E3.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-128">No other capabilities are part of the E3 trial offering.</span></span>

## <a name="simulations"></a><span data-ttu-id="a3c7b-129">Simulations</span><span class="sxs-lookup"><span data-stu-id="a3c7b-129">Simulations</span></span>

<span data-ttu-id="a3c7b-130">Le *Hameçonnage* est un terme générique qui décrit les attaques par courrier électronique tentant d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-130">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="a3c7b-131">*Le hameçonnage* fait partie d’un sous-ensemble de techniques que nous classons en _tant qu’ingénierie sociale._</span><span class="sxs-lookup"><span data-stu-id="a3c7b-131">*Phishing* is a part of a subset of techniques we classify as _social engineering_.</span></span>

<span data-ttu-id="a3c7b-132">Dans la formation à la simulation d’attaques, plusieurs types de techniques d’ingénierie sociale sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="a3c7b-132">In Attack simulation training, multiple types of social engineering techniques are available:</span></span>

- <span data-ttu-id="a3c7b-133">**Informations d’identification**: une personne malveillante envoie au destinataire un message contenant une URL.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-133">**Credential harvest**: An attacker sends the recipient a message that contains a URL.</span></span> <span data-ttu-id="a3c7b-134">Lorsque le destinataire clique sur l’URL, il est redéliqué sur un site web qui affiche généralement une boîte de dialogue qui demande à l’utilisateur son nom d’utilisateur et son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-134">When the recipient clicks on the URL, they're taken to a website that typically shows a dialog box that asks the user for their username and password.</span></span> <span data-ttu-id="a3c7b-135">En règle générale, la page de destination est un site web connu pour créer une relation d’confiance avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-135">Typically, the destination page is themed to represent a well-known website in order to build trust in the user.</span></span>

- <span data-ttu-id="a3c7b-136">**Pièce jointe malveillante**: une personne malveillante envoie au destinataire un message contenant une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-136">**Malware attachment**: An attacker sends the recipient a message that contains an attachment.</span></span> <span data-ttu-id="a3c7b-137">Lorsque le destinataire ouvre la pièce jointe, du code arbitraire (par exemple, une macro) est exécuté sur l’appareil de l’utilisateur pour permettre à l’attaquant d’installer du code supplémentaire ou de s’en empêcher.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-137">When the recipient opens the attachment, arbitrary code (for example, a macro) is run on the user's device to help the attacker install additional code or further entrench themselves.</span></span>

- <span data-ttu-id="a3c7b-138">**Lien dans la pièce** jointe : il s’agit d’un hybride de la saisie des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-138">**Link in attachment**: This is a hybrid of a credential harvest.</span></span> <span data-ttu-id="a3c7b-139">Une personne malveillante envoie au destinataire un message contenant une URL à l’intérieur d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-139">An attacker sends the recipient a message that contains a URL inside of an attachment.</span></span> <span data-ttu-id="a3c7b-140">Lorsque le destinataire ouvre la pièce jointe et clique sur l’URL, il est redéliqué sur un site web qui affiche généralement une boîte de dialogue qui demande à l’utilisateur son nom d’utilisateur et son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-140">When the recipient opens the attachment and clicks on the URL, they're taken to a website that typically shows a dialog box that asks the user for their username and password.</span></span> <span data-ttu-id="a3c7b-141">En règle générale, la page de destination est un site web connu pour créer une relation d’confiance avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-141">Typically, the destination page is themed to represent a well-known website in order to build trust in the user.</span></span>

- <span data-ttu-id="a3c7b-142">**Lien** vers un programme malveillant : une personne malveillante envoie au destinataire un message contenant un lien vers une pièce jointe sur un site de partage de fichiers connu (par exemple, SharePoint Online ou Dropbox).</span><span class="sxs-lookup"><span data-stu-id="a3c7b-142">**Link to malware**: An attacker sends the recipient a message that contains a link to an attachment on a well-known file sharing site (for example, SharePoint Online or Dropbox).</span></span> <span data-ttu-id="a3c7b-143">Lorsque le destinataire clique sur l’URL, la pièce jointe s’ouvre et un code arbitraire (par exemple, une macro) est exécuté sur l’appareil de l’utilisateur pour aider l’attaquant à installer du code supplémentaire ou à s’en aller.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-143">When the recipient clicks on the URL, the attachment opens and arbitrary code (for example, a macro) is run on the user's device to help the attacker install additional code or further entrench themselves.</span></span>

- <span data-ttu-id="a3c7b-144">**Lecteur par URL**: une personne malveillante envoie au destinataire un message contenant une URL.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-144">**Drive-by-url**: An attacker sends the recipient a messages that contains a URL.</span></span> <span data-ttu-id="a3c7b-145">Lorsque le destinataire clique sur l’URL, il est dirigé vers un site web qui tente d’exécuter du code d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-145">When the recipient clicks on the URL, they're taken to a website that tries to run background code.</span></span> <span data-ttu-id="a3c7b-146">Ce code en arrière-plan tente de collecter des informations sur le destinataire ou de déployer du code arbitraire sur son appareil.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-146">This background code attempts to gather information about the recipient or deploy arbitrary code on their device.</span></span> <span data-ttu-id="a3c7b-147">En règle générale, le site web de destination est un site web connu compromis ou un clone d’un site web connu.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-147">Typically, the destination website is a well-known website that has been compromised or a clone of a well-known website.</span></span> <span data-ttu-id="a3c7b-148">La connaissance du site web permet de convaincre l’utilisateur que le lien peut être cliqué en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-148">Familiarity with the website helps convince the user that the link is safe to click.</span></span> <span data-ttu-id="a3c7b-149">Cette technique est également connue sous le nom d’attaque par trous _d’eau._</span><span class="sxs-lookup"><span data-stu-id="a3c7b-149">This technique is also known as a _watering hole attack_.</span></span>

> [!NOTE]
> <span data-ttu-id="a3c7b-150">Vérifiez la disponibilité de l’URL de hameçonnage simulé dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-150">Check the availability of the simulated phishing URL in your supported web browsers before you use the URL in a phishing campaign.</span></span> <span data-ttu-id="a3c7b-151">Bien que nous travaillions avec de nombreux fournisseurs de réputation d’URL pour toujours autoriser ces URL de simulation, nous n’avons pas toujours une couverture complète (par exemple, Google Coffre Navigation).</span><span class="sxs-lookup"><span data-stu-id="a3c7b-151">While we work with many URL reputation vendors to always allow these simulation URLs, we don't always have full coverage (for example, Google Safe Browsing).</span></span> <span data-ttu-id="a3c7b-152">La plupart des fournisseurs fournissent des conseils qui vous permettent de toujours autoriser des URL spécifiques (par exemple, <https://support.google.com/chrome/a/answer/7532419> ).</span><span class="sxs-lookup"><span data-stu-id="a3c7b-152">Most vendors provide guidance that allows you to always allow specific URLs (for example, <https://support.google.com/chrome/a/answer/7532419>).</span></span>

<span data-ttu-id="a3c7b-153">Les URL utilisées par la formation à la simulation d’attaque sont décrites dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="a3c7b-153">The URLs that are used by Attack simulation training are described in the following list:</span></span>

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

### <a name="create-a-simulation"></a><span data-ttu-id="a3c7b-154">Créer une simulation</span><span class="sxs-lookup"><span data-stu-id="a3c7b-154">Create a simulation</span></span>

<span data-ttu-id="a3c7b-155">Pour obtenir des instructions détaillées sur la création et l’envoi d’une nouvelle simulation, voir [Simuler une attaque par hameçonnage.](attack-simulation-training.md)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-155">For step by step instructions on how to create and send a new simulation, see [Simulate a phishing attack](attack-simulation-training.md).</span></span>

### <a name="create-a-payload"></a><span data-ttu-id="a3c7b-156">Créer une charge utile</span><span class="sxs-lookup"><span data-stu-id="a3c7b-156">Create a payload</span></span>

<span data-ttu-id="a3c7b-157">Pour obtenir des instructions détaillées sur la création d’une charge utile à utiliser dans une simulation, voir Créer une charge utile personnalisée pour la formation à la [simulation d’attaques.](attack-simulation-training-payloads.md)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-157">For step by step instructions on how to create a payload for use within a simulation, see [Create a custom payload for Attack simulation training](attack-simulation-training-payloads.md).</span></span>

### <a name="gaining-insights"></a><span data-ttu-id="a3c7b-158">Obtenir des informations</span><span class="sxs-lookup"><span data-stu-id="a3c7b-158">Gaining insights</span></span>

<span data-ttu-id="a3c7b-159">Pour obtenir des instructions détaillées sur la façon d’obtenir des informations sur les rapports, voir Obtenir des informations via une formation à la [simulation d’attaques.](attack-simulation-training-insights.md)</span><span class="sxs-lookup"><span data-stu-id="a3c7b-159">For step by step instructions on how to gain insights with reporting, see [Gain insights through Attack simulation training](attack-simulation-training-insights.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a3c7b-160">Le Simulateur d’attaques utilise des liens Coffre dans Defender pour Office 365 pour suivre en toute sécurité les données de clic de l’URL dans le message de charge utile envoyé aux destinataires ciblés d’une campagne de hameçonnage, même si le paramètre Ne pas suivre les clics de l’utilisateur dans les **stratégies** de liens Coffre est allumé.</span><span class="sxs-lookup"><span data-stu-id="a3c7b-160">Attack Simulator uses Safe Links in Defender for Office 365 to securely track click data for the URL in the payload message that's sent to targeted recipients of a phishing campaign, even if the **Do not track user clicks** setting in Safe Links policies is turned on.</span></span>
