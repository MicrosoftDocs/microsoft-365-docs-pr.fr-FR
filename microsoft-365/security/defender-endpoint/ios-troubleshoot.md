---
title: Résoudre les problèmes et trouver des réponses sur les QUESTIONS liées à Microsoft Defender for Endpoint sur iOS
description: Résolution des problèmes et FAQ - Microsoft Defender pour point de terminaison sur iOS
keywords: microsoft, defender, Microsoft Defender for Endpoint, ios, troubleshoot, faq, how to
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 2f9d56b7e72befb8acddf6d9f810a7ba5cec1083
ms.sourcegitcommit: 5377b00703b6f559092afe44fb61462e97968a60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52694364"
---
# <a name="troubleshoot-issues-and-find-answers-to-faqs-on-microsoft-defender-for-endpoint-on-ios"></a><span data-ttu-id="3c52a-104">Résoudre les problèmes et trouver des réponses aux QUESTIONS sur Microsoft Defender pour le point de terminaison sur iOS</span><span class="sxs-lookup"><span data-stu-id="3c52a-104">Troubleshoot issues and find answers to FAQs on Microsoft Defender for Endpoint on iOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3c52a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3c52a-105">**Applies to:**</span></span>
- [<span data-ttu-id="3c52a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3c52a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3c52a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3c52a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3c52a-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="3c52a-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="3c52a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3c52a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="3c52a-110">Cette rubrique fournit des informations de dépannage pour vous aider à résoudre les problèmes qui peuvent survenir lorsque vous utilisez Microsoft Defender pour Endpoint sur iOS.</span><span class="sxs-lookup"><span data-stu-id="3c52a-110">This topic provides troubleshooting information to help you address issues that may arise as you use Microsoft Defender for Endpoint on iOS.</span></span>



> [!NOTE]
> <span data-ttu-id="3c52a-111">Defender pour le point de terminaison sur iOS utiliserait un VPN pour fournir la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="3c52a-111">Defender for Endpoint on iOS would use a VPN in order to provide the Web Protection feature.</span></span> <span data-ttu-id="3c52a-112">Il ne s’agit pas d’un VPN normal et d’un VPN local/en boucle autonome qui ne prend pas le trafic en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c52a-112">This is not a regular VPN and is a local/self-looping VPN that does not take traffic outside the device.</span></span>

## <a name="apps-dont-work-when-vpn-is-turned-on"></a><span data-ttu-id="3c52a-113">Les applications ne fonctionnent pas lorsque le VPN est allumé</span><span class="sxs-lookup"><span data-stu-id="3c52a-113">Apps don't work when VPN is turned on</span></span>
<span data-ttu-id="3c52a-114">Certaines applications cessent de fonctionner lorsqu’un VPN actif est détecté.</span><span class="sxs-lookup"><span data-stu-id="3c52a-114">There are some apps that stop functioning when an active VPN is detected.</span></span> <span data-ttu-id="3c52a-115">Vous pouvez désactiver le VPN pendant la durée d’utilisation de ces applications.</span><span class="sxs-lookup"><span data-stu-id="3c52a-115">You can disable the VPN during the time you are using such apps.</span></span> 

<span data-ttu-id="3c52a-116">Par défaut, Defender pour le point de terminaison sur iOS inclut et active la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="3c52a-116">By default, Defender for Endpoint on iOS includes and enables the web protection feature.</span></span> <span data-ttu-id="3c52a-117">[La protection web permet](web-protection-overview.md) de sécuriser les appareils contre les menaces web et de protéger les utilisateurs contre les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="3c52a-117">[Web protection](web-protection-overview.md) helps to secure devices against web threats and protect users from phishing attacks.</span></span> <span data-ttu-id="3c52a-118">Defender pour le point de terminaison sur iOS utilise un VPN pour fournir cette protection.</span><span class="sxs-lookup"><span data-stu-id="3c52a-118">Defender for Endpoint on iOS uses a VPN in order to provide this protection.</span></span> <span data-ttu-id="3c52a-119">Notez qu’il s’agit d’un VPN local et, contrairement au VPN traditionnel, le trafic réseau n’est pas envoyé à l’extérieur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c52a-119">Please note this is a local VPN and unlike traditional VPN, network traffic is not sent outside the device.</span></span>

<span data-ttu-id="3c52a-120">Bien qu’il soit activé par défaut, il se peut que vous de soyez dans certains cas dans l’obligation de désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="3c52a-120">While enabled by default, there might be some cases that require you to disable VPN.</span></span> <span data-ttu-id="3c52a-121">Par exemple, vous souhaitez exécuter certaines applications qui ne fonctionnent pas lorsqu’un VPN est configuré.</span><span class="sxs-lookup"><span data-stu-id="3c52a-121">For example, you want to run some apps that do not work when a VPN is configured.</span></span> <span data-ttu-id="3c52a-122">Dans ce cas, vous pouvez choisir de désactiver le VPN de l’application sur l’appareil en suivant les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="3c52a-122">In such cases, you can choose to disable VPN from the app on the device by following the steps below:</span></span>

1. <span data-ttu-id="3c52a-123">Sur votre appareil iOS, ouvrez **l’application Paramètres,** cliquez ou appuyez sur **Général,** puis **sur VPN.**</span><span class="sxs-lookup"><span data-stu-id="3c52a-123">On your iOS device, open the **Settings** app, click or tap **General** and then **VPN**.</span></span>
1. <span data-ttu-id="3c52a-124">Cliquez ou appuyez sur le bouton « i » de Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3c52a-124">Click or tap the "i" button for Microsoft Defender for Endpoint.</span></span>
1. <span data-ttu-id="3c52a-125">Désactivez la **Connecter à la demande** pour désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="3c52a-125">Toggle off **Connect On Demand** to disable VPN.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="3c52a-126">![Connexion de la connexion VPN à la demande](images/ios-vpn-config.png)</span><span class="sxs-lookup"><span data-stu-id="3c52a-126">![VPN config connect on demand](images/ios-vpn-config.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3c52a-127">La protection web n’est pas disponible lorsque le VPN est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3c52a-127">Web Protection will not be available when VPN is disabled.</span></span> <span data-ttu-id="3c52a-128">Pour activer à nouveau la Protection Web, ouvrez l’application Microsoft Defender pour point de terminaison sur l’appareil, puis cliquez ou appuyez sur **Démarrer le VPN.**</span><span class="sxs-lookup"><span data-stu-id="3c52a-128">To re-enable Web Protection, open the Microsoft Defender for Endpoint app on the device and click or tap **Start VPN**.</span></span>

## <a name="issues-with-multiple-vpn-profiles"></a><span data-ttu-id="3c52a-129">Problèmes avec plusieurs profils VPN</span><span class="sxs-lookup"><span data-stu-id="3c52a-129">Issues with multiple VPN profiles</span></span>

<span data-ttu-id="3c52a-130">Apple iOS ne prend pas en **charge** plusieurs VPN à l’échelle de l’appareil pour être actifs simultanément.</span><span class="sxs-lookup"><span data-stu-id="3c52a-130">Apple iOS does not support multiple **device-wide** VPNs to be active simultaneously.</span></span> <span data-ttu-id="3c52a-131">Même si plusieurs profils VPN peuvent exister sur l’appareil, un seul VPN peut être actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="3c52a-131">While multiple VPN profiles can exist on the device, only one VPN can be active at a time.</span></span>

<span data-ttu-id="3c52a-132">Le VPN Microsoft Defender pour point de terminaison peut co-exister avec d’autres VPN configurés comme par application ou *« Personnel*». </span><span class="sxs-lookup"><span data-stu-id="3c52a-132">Microsoft Defender for Endpoint VPN can co-exist with other VPNs that are configured as *per-app* or *"Personal"*.</span></span>

## <a name="battery-consumption"></a><span data-ttu-id="3c52a-133">Consommation de batterie</span><span class="sxs-lookup"><span data-stu-id="3c52a-133">Battery consumption</span></span>

<span data-ttu-id="3c52a-134">Dans l’Paramètres, iOS affiche uniquement l’utilisation de la batterie des applications visibles par l’utilisateur pendant une durée spécifique.</span><span class="sxs-lookup"><span data-stu-id="3c52a-134">In the Settings app, iOS only shows battery usage of apps that are visible to the user for a specific duration of time.</span></span> <span data-ttu-id="3c52a-135">L’utilisation de la batterie par les applications affichées à l’écran ne dure que pendant cette durée et est calculée par iOS en fonction d’une multitude de facteurs, notamment l’utilisation du processeur et du réseau.</span><span class="sxs-lookup"><span data-stu-id="3c52a-135">The battery usage by apps shown on the screen are only for that time duration and is computed by iOS based on a multitude of factors including CPU and Network usage.</span></span> <span data-ttu-id="3c52a-136">Microsoft Defender pour le point de terminaison utilise un VPN local/de bouc-back en arrière-plan pour vérifier le trafic web des sites web ou connexions malveillants.</span><span class="sxs-lookup"><span data-stu-id="3c52a-136">Microsoft Defender for Endpoint uses a local/loop-back VPN in the background to check web traffic for any malicious websites or connections.</span></span> <span data-ttu-id="3c52a-137">Les paquets réseau de n’importe quelle application sont vérifiés et l’utilisation de la batterie de Microsoft Defender for Endpoint est calculée de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="3c52a-137">Network packets from any app go through this check and that causes the battery usage of Microsoft Defender for Endpoint to be computed inaccurately.</span></span> <span data-ttu-id="3c52a-138">La consommation réelle de batterie de Microsoft Defender pour le point de terminaison est beaucoup moins élevée que celle affichée sur la page Paramètres batterie sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c52a-138">The actual battery consumption of Microsoft Defender for Endpoint is much less than what is shown on the Battery Settings page on the device.</span></span>

<span data-ttu-id="3c52a-139">En moyenne, l’utilisation quotidienne de la batterie par Microsoft Defender pour le point de terminaison s’exécutant en arrière-plan représente environ **8,81 %** de la batterie globale consommée au cours de ce jour.</span><span class="sxs-lookup"><span data-stu-id="3c52a-139">On an average, per-day battery usage by Microsoft Defender for Endpoint running on the background is **approximately 8.81% of overall battery consumed in that day**.</span></span> <span data-ttu-id="3c52a-140">Cette mesure est signalée par Apple en fonction de l’utilisation réelle de Microsoft Defender pour Endpoint sur les appareils des utilisateurs finaux et, pour des raisons mentionnées ci-dessus, peut également être liée à d’autres applications qui ont une activité réseau.</span><span class="sxs-lookup"><span data-stu-id="3c52a-140">This metric is reported by Apple based on actual usage of Microsoft Defender for Endpoint on end-user devices and due to reasons mentioned above can also be accounted to other apps that have network activity.</span></span>

<span data-ttu-id="3c52a-141">En outre, le VPN utilisé est un VPN local et, contrairement à un VPN traditionnel, le trafic réseau n’est pas envoyé en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c52a-141">Also, the VPN used is a local VPN and unlike a traditional VPN, network traffic is not sent outside the device.</span></span>

## <a name="data-usage"></a><span data-ttu-id="3c52a-142">Utilisation des données</span><span class="sxs-lookup"><span data-stu-id="3c52a-142">Data usage</span></span>

<span data-ttu-id="3c52a-143">Microsoft Defender pour le point de terminaison utilise un VPN local/loopback pour vérifier le trafic web des sites web ou connexions malveillants.</span><span class="sxs-lookup"><span data-stu-id="3c52a-143">Microsoft Defender for Endpoint uses a local/loopback VPN to check web traffic for any malicious websites or connections.</span></span> <span data-ttu-id="3c52a-144">Pour cette raison, l’utilisation des données de Microsoft Defender pour les points de terminaison peut être incorrectement expliquée.</span><span class="sxs-lookup"><span data-stu-id="3c52a-144">Due to this reason, Microsoft Defender for Endpoint data usage can be inaccurately accounted for.</span></span> <span data-ttu-id="3c52a-145">L’utilisation réelle des données par Microsoft Defender pour le point de terminaison n’est pas significative et inférieure à ce qui est indiqué sur la Paramètres d’utilisation des données sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c52a-145">The actual data usage by Microsoft Defender for Endpoint is not significant and lesser than what is shown on the Data Usage Settings on the device.</span></span>

## <a name="report-unsafe-site"></a><span data-ttu-id="3c52a-146">Signaler un site non sécurisé</span><span class="sxs-lookup"><span data-stu-id="3c52a-146">Report unsafe site</span></span>

<span data-ttu-id="3c52a-147">Les sites web de hameçonnage usurpent l’identité de sites web dignes de confiance dans le but d’obtenir vos informations personnelles ou financières.</span><span class="sxs-lookup"><span data-stu-id="3c52a-147">Phishing websites impersonate trustworthy websites for the purpose of obtaining your personal or financial information.</span></span> <span data-ttu-id="3c52a-148">Consultez la page [Fournir des commentaires sur la protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) du réseau pour signaler un site web qui pourrait être un site de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="3c52a-148">Visit the [Provide feedback about network protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) page to report a website that could be a phishing site.</span></span>

## <a name="malicious-site-detected"></a><span data-ttu-id="3c52a-149">Site malveillant détecté</span><span class="sxs-lookup"><span data-stu-id="3c52a-149">Malicious site detected</span></span>

<span data-ttu-id="3c52a-150">Microsoft Defender pour le point de terminaison vous protège contre le hameçonnage ou d’autres attaques basées sur le web.</span><span class="sxs-lookup"><span data-stu-id="3c52a-150">Microsoft Defender for Endpoint protects you against phishing or other web-based attacks.</span></span> <span data-ttu-id="3c52a-151">Si un site malveillant est détecté, la connexion est bloquée et une alerte est envoyée au portail centre de sécurité de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3c52a-151">If a malicious site is detected, the connection is blocked and an alert is sent to the organization's Security Center portal.</span></span> <span data-ttu-id="3c52a-152">L’alerte inclut le nom de domaine de la connexion, l’adresse IP distante et les détails du périphérique.</span><span class="sxs-lookup"><span data-stu-id="3c52a-152">The alert includes the domain name of the connection, remote IP address and the device details.</span></span>

<span data-ttu-id="3c52a-153">En outre, une notification s’affiche sur l’appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="3c52a-153">In addition, a notification is shown on the iOS device.</span></span> <span data-ttu-id="3c52a-154">Appuyer sur la notification ouvre l’écran suivant pour que l’utilisateur examine les détails.</span><span class="sxs-lookup"><span data-stu-id="3c52a-154">Tapping on the notification opens the following screen for the user to review the details.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="3c52a-155">![Image du site signalée comme notification non sûre](images/ios-phish-alert.png)</span><span class="sxs-lookup"><span data-stu-id="3c52a-155">![Image of site reported as unsafe notification](images/ios-phish-alert.png)</span></span>

## <a name="data-and-privacy"></a><span data-ttu-id="3c52a-156">Données et confidentialité</span><span class="sxs-lookup"><span data-stu-id="3c52a-156">Data and Privacy</span></span>

<span data-ttu-id="3c52a-157">Pour plus d’informations sur les données collectées et la confidentialité, voir Informations sur la confidentialité - Microsoft Defender pour point de [terminaison sur iOS](ios-privacy.md).</span><span class="sxs-lookup"><span data-stu-id="3c52a-157">For details about data collected and privacy, see [Privacy Information - Microsoft Defender for Endpoint on iOS](ios-privacy.md).</span></span>

