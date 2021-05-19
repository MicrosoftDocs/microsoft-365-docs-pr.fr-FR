---
title: Résoudre les problèmes sur Microsoft Defender pour point de terminaison sur iOS
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
ms.openlocfilehash: 82a3fcc58b97f53f584befae77c86e8a18952a23
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52539303"
---
# <a name="troubleshoot-issues-on-microsoft-defender-for-endpoint-on-ios"></a><span data-ttu-id="50c18-104">Résoudre les problèmes sur Microsoft Defender pour point de terminaison sur iOS</span><span class="sxs-lookup"><span data-stu-id="50c18-104">Troubleshoot issues on Microsoft Defender for Endpoint on iOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="50c18-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="50c18-105">**Applies to:**</span></span>
- [<span data-ttu-id="50c18-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="50c18-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="50c18-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="50c18-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="50c18-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="50c18-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="50c18-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="50c18-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="50c18-110">Cette rubrique fournit des informations de dépannage pour vous aider à résoudre les problèmes qui peuvent survenir lorsque vous utilisez Microsoft Defender pour Endpoint sur iOS.</span><span class="sxs-lookup"><span data-stu-id="50c18-110">This topic provides troubleshooting information to help you address issues that may arise as you use Microsoft Defender for Endpoint on iOS.</span></span>



> [!NOTE]
> <span data-ttu-id="50c18-111">Defender pour le point de terminaison sur iOS utiliserait un VPN pour fournir la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="50c18-111">Defender for Endpoint on iOS would use a VPN in order to provide the Web Protection feature.</span></span> <span data-ttu-id="50c18-112">Il ne s’agit pas d’un VPN normal et d’un VPN local/en boucle autonome qui ne prend pas le trafic en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="50c18-112">This is not a regular VPN and is a local/self-looping VPN that does not take traffic outside the device.</span></span>

## <a name="apps-dont-work-when-vpn-is-turned-on"></a><span data-ttu-id="50c18-113">Les applications ne fonctionnent pas lorsque le VPN est allumé</span><span class="sxs-lookup"><span data-stu-id="50c18-113">Apps don't work when VPN is turned on</span></span>
<span data-ttu-id="50c18-114">Certaines applications cessent de fonctionner lorsqu’un VPN actif est détecté.</span><span class="sxs-lookup"><span data-stu-id="50c18-114">There are some apps that stop functioning when an active VPN is detected.</span></span> <span data-ttu-id="50c18-115">Vous pouvez désactiver le VPN pendant la durée d’utilisation de ces applications.</span><span class="sxs-lookup"><span data-stu-id="50c18-115">You can disable the VPN during the time you are using such apps.</span></span> 

<span data-ttu-id="50c18-116">Par défaut, Defender pour le point de terminaison sur iOS inclut et active la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="50c18-116">By default, Defender for Endpoint on iOS includes and enables the web protection feature.</span></span> <span data-ttu-id="50c18-117">[La protection web permet](web-protection-overview.md) de sécuriser les appareils contre les menaces web et de protéger les utilisateurs contre les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="50c18-117">[Web protection](web-protection-overview.md) helps to secure devices against web threats and protect users from phishing attacks.</span></span> <span data-ttu-id="50c18-118">Defender pour le point de terminaison sur iOS utilise un VPN pour fournir cette protection.</span><span class="sxs-lookup"><span data-stu-id="50c18-118">Defender for Endpoint on iOS uses a VPN in order to provide this protection.</span></span> <span data-ttu-id="50c18-119">Notez qu’il s’agit d’un VPN local et, contrairement au VPN traditionnel, le trafic réseau n’est pas envoyé en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="50c18-119">Please note this is a local VPN and unlike traditional VPN, network traffic is not sent outside the device.</span></span>

<span data-ttu-id="50c18-120">Bien qu’il soit activé par défaut, il se peut que vous de soyez dans certains cas dans l’obligation de désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="50c18-120">While enabled by default, there might be some cases that require you to disable VPN.</span></span> <span data-ttu-id="50c18-121">Par exemple, vous souhaitez exécuter certaines applications qui ne fonctionnent pas lorsqu’un VPN est configuré.</span><span class="sxs-lookup"><span data-stu-id="50c18-121">For example, you want to run some apps that do not work when a VPN is configured.</span></span> <span data-ttu-id="50c18-122">Dans ce cas, vous pouvez choisir de désactiver le VPN de l’application sur l’appareil en suivant les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="50c18-122">In such cases, you can choose to disable VPN from the app on the device by following the steps below:</span></span>

1. <span data-ttu-id="50c18-123">Sur votre appareil iOS, ouvrez **l’application Paramètres,** cliquez ou appuyez sur **Général,** puis **sur VPN.**</span><span class="sxs-lookup"><span data-stu-id="50c18-123">On your iOS device, open the **Settings** app, click or tap **General** and then **VPN**.</span></span>
1. <span data-ttu-id="50c18-124">Cliquez ou appuyez sur le bouton « i » de Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="50c18-124">Click or tap the "i" button for Microsoft Defender for Endpoint.</span></span>
1. <span data-ttu-id="50c18-125">Désactivez la **Connecter à la demande** pour désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="50c18-125">Toggle off **Connect On Demand** to disable VPN.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="50c18-126">![Connexion de la connexion VPN à la demande](images/ios-vpn-config.png)</span><span class="sxs-lookup"><span data-stu-id="50c18-126">![VPN config connect on demand](images/ios-vpn-config.png)</span></span>

> [!NOTE]
> <span data-ttu-id="50c18-127">La protection web n’est pas disponible lorsque le VPN est désactivé.</span><span class="sxs-lookup"><span data-stu-id="50c18-127">Web Protection will not be available when VPN is disabled.</span></span> <span data-ttu-id="50c18-128">Pour activer à nouveau la Protection Web, ouvrez l’application Microsoft Defender pour point de terminaison sur l’appareil, puis cliquez ou appuyez sur **Démarrer le VPN.**</span><span class="sxs-lookup"><span data-stu-id="50c18-128">To re-enable Web Protection, open the Microsoft Defender for Endpoint app on the device and click or tap **Start VPN**.</span></span>

## <a name="issues-with-multiple-vpn-profiles"></a><span data-ttu-id="50c18-129">Problèmes avec plusieurs profils VPN</span><span class="sxs-lookup"><span data-stu-id="50c18-129">Issues with multiple VPN profiles</span></span>

<span data-ttu-id="50c18-130">Apple iOS ne prend pas en charge plusieurs VPN à l’échelle de l’appareil pour être actifs simultanément.</span><span class="sxs-lookup"><span data-stu-id="50c18-130">Apple iOS does not support multiple device-wide VPNs to be active simultaneously.</span></span> <span data-ttu-id="50c18-131">Même si plusieurs profils VPN peuvent exister sur l’appareil, un seul VPN peut être actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="50c18-131">While multiple VPN profiles can exist on the device, only one VPN can be active at a time.</span></span>


## <a name="battery-consumption"></a><span data-ttu-id="50c18-132">Consommation de batterie</span><span class="sxs-lookup"><span data-stu-id="50c18-132">Battery consumption</span></span>

<span data-ttu-id="50c18-133">L’utilisation de la batterie par une application est calculée par Apple en fonction d’une multitude de facteurs, notamment l’utilisation du processeur et du réseau.</span><span class="sxs-lookup"><span data-stu-id="50c18-133">The battery usage by an app is computed by Apple based on a multitude of factors including CPU and Network usage.</span></span> <span data-ttu-id="50c18-134">Microsoft Defender pour le point de terminaison utilise un VPN local/loop-back en arrière-plan pour vérifier le trafic web des sites web ou connexions malveillants.</span><span class="sxs-lookup"><span data-stu-id="50c18-134">Microsoft Defender for Endpoint uses a local/loop-back VPN in the background to check web traffic for any malicious websites or connections.</span></span> <span data-ttu-id="50c18-135">Les paquets réseau de n’importe quelle application sont vérifiés et l’utilisation de la batterie de Microsoft Defender for Endpoint est calculée de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="50c18-135">Network packets from any app go through this check and that causes the battery usage of Microsoft Defender for Endpoint to be computed inaccurately.</span></span> <span data-ttu-id="50c18-136">Cela donne une fausse impression à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50c18-136">This gives a false impression to the user.</span></span> <span data-ttu-id="50c18-137">La consommation réelle de batterie de Microsoft Defender pour le point de terminaison est inférieure à ce qui est affiché sur la page Paramètres batterie sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="50c18-137">The actual battery consumption of Microsoft Defender for Endpoint is lesser than what is shown on the Battery Settings page on the device.</span></span> <span data-ttu-id="50c18-138">Cette opération est basée sur des tests effectués sur l’application Microsoft Defender for Endpoint pour comprendre la consommation de batterie.</span><span class="sxs-lookup"><span data-stu-id="50c18-138">This is based on conducted tests done on the Microsoft Defender for Endpoint app to understand battery consumption.</span></span>

<span data-ttu-id="50c18-139">En outre, le VPN utilisé est un VPN local et, contrairement à un VPN traditionnel, le trafic réseau n’est pas envoyé en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="50c18-139">Also the VPN used is a local VPN and unlike a traditional VPN, network traffic is not sent outside the device.</span></span>

## <a name="data-usage"></a><span data-ttu-id="50c18-140">Utilisation des données</span><span class="sxs-lookup"><span data-stu-id="50c18-140">Data usage</span></span>

<span data-ttu-id="50c18-141">Microsoft Defender pour le point de terminaison utilise un VPN local/loopback pour vérifier le trafic web des sites web ou connexions malveillants.</span><span class="sxs-lookup"><span data-stu-id="50c18-141">Microsoft Defender for Endpoint uses a local/loopback VPN to check web traffic for any malicious websites or connections.</span></span> <span data-ttu-id="50c18-142">Pour cette raison, Apple compte de manière incorrecte l’utilisation des données dans Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="50c18-142">Due to this reason Apple accounts data usage to Microsoft Defender for Endpoint inaccurately.</span></span> <span data-ttu-id="50c18-143">L’utilisation réelle des données par Microsoft Defender pour le point de terminaison n’est pas significative et beaucoup moins importante que ce qui est indiqué sur la Paramètres d’utilisation des données sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="50c18-143">The actual data usage by Microsoft Defender for Endpoint is not significant and much less than what is shown on the Data Usage Settings on the device.</span></span>

## <a name="report-unsafe-site"></a><span data-ttu-id="50c18-144">Signaler un site non sécurisé</span><span class="sxs-lookup"><span data-stu-id="50c18-144">Report unsafe site</span></span>

<span data-ttu-id="50c18-145">Les sites web de hameçonnage usurpent l’identité de sites web dignes de confiance dans le but d’obtenir vos informations personnelles ou financières.</span><span class="sxs-lookup"><span data-stu-id="50c18-145">Phishing websites impersonate trustworthy websites for the purpose of obtaining your personal or financial information.</span></span> <span data-ttu-id="50c18-146">Consultez la page [Fournir des commentaires sur la protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) du réseau pour signaler un site web qui pourrait être un site de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="50c18-146">Visit the [Provide feedback about network protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) page to report a website that could be a phishing site.</span></span>

## <a name="malicious-site-detected"></a><span data-ttu-id="50c18-147">Site malveillant détecté</span><span class="sxs-lookup"><span data-stu-id="50c18-147">Malicious site detected</span></span>

<span data-ttu-id="50c18-148">Microsoft Defender pour le point de terminaison vous protège contre le hameçonnage ou d’autres attaques basées sur le web.</span><span class="sxs-lookup"><span data-stu-id="50c18-148">Microsoft Defender for Endpoint protects you against phishing or other web-based attacks.</span></span> <span data-ttu-id="50c18-149">Si un site malveillant est détecté, la connexion est bloquée et une alerte est envoyée au portail centre de sécurité de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="50c18-149">If a malicious site is detected, the connection is blocked and an alert is sent to the organization's Security Center portal.</span></span> <span data-ttu-id="50c18-150">L’alerte inclut le nom de domaine de la connexion, l’adresse IP distante et les détails du périphérique.</span><span class="sxs-lookup"><span data-stu-id="50c18-150">The alert includes the domain name of the connection, remote IP address and the device details.</span></span>

<span data-ttu-id="50c18-151">En outre, une notification s’affiche sur l’appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="50c18-151">In addition, a notification is shown on the iOS device.</span></span> <span data-ttu-id="50c18-152">Appuyer sur la notification ouvre l’écran suivant pour que l’utilisateur examine les détails.</span><span class="sxs-lookup"><span data-stu-id="50c18-152">Tapping on the notification opens the following screen for the user to review the details.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="50c18-153">![Image du site signalée comme notification non sûre](images/ios-phish-alert.png)</span><span class="sxs-lookup"><span data-stu-id="50c18-153">![Image of site reported as unsafe notification](images/ios-phish-alert.png)</span></span>

## <a name="data-and-privacy"></a><span data-ttu-id="50c18-154">Données et confidentialité</span><span class="sxs-lookup"><span data-stu-id="50c18-154">Data and Privacy</span></span>

<span data-ttu-id="50c18-155">Pour plus d’informations sur les données collectées et la confidentialité, voir Informations sur la confidentialité [- Microsoft Defender pour endpoint sur iOS](ios-privacy.md).</span><span class="sxs-lookup"><span data-stu-id="50c18-155">For details about data collected and privacy, see [Privacy Information - Microsoft Defender for Endpoint on iOS](ios-privacy.md).</span></span>

