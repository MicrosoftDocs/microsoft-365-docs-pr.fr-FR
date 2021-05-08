---
title: Résoudre les problèmes sur Microsoft Defender pour le point de terminaison sur Android
description: Résoudre les problèmes de Microsoft Defender pour point de terminaison sur Android
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, mde, android, cloud, connectivité, communication
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
ms.openlocfilehash: 18afd4aa160ec345839d23719d1b3fcce21654ec
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52246355"
---
# <a name="troubleshooting-issues-on-microsoft-defender-for-endpoint-on-android"></a><span data-ttu-id="f87be-104">Résolution des problèmes sur Microsoft Defender pour point de terminaison sur Android</span><span class="sxs-lookup"><span data-stu-id="f87be-104">Troubleshooting issues on Microsoft Defender for Endpoint on Android</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f87be-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f87be-105">**Applies to:**</span></span>
- [<span data-ttu-id="f87be-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f87be-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f87be-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f87be-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f87be-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f87be-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f87be-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f87be-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="f87be-110">Lors de l’intégration d’un appareil, vous pouvez voir des problèmes de connectez-vous après l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="f87be-110">When onboarding a device, you might see sign in issues after the app is installed.</span></span>

<span data-ttu-id="f87be-111">Lors de l’intégration, vous pouvez rencontrer des problèmes de connectez-vous après l’installation de l’application sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="f87be-111">During onboarding, you might encounter sign in issues after the app is installed on your device.</span></span>

<span data-ttu-id="f87be-112">Cet article fournit des solutions pour vous aider à résoudre les problèmes d' sign-on.</span><span class="sxs-lookup"><span data-stu-id="f87be-112">This article provides solutions to help address the sign-on issues.</span></span>  

## <a name="sign-in-failed---unexpected-error"></a><span data-ttu-id="f87be-113">Échec de la signature : erreur inattendue</span><span class="sxs-lookup"><span data-stu-id="f87be-113">Sign in failed - unexpected error</span></span>
<span data-ttu-id="f87be-114">**Échec de la signature : erreur** *inattendue, essayez ultérieurement*</span><span class="sxs-lookup"><span data-stu-id="f87be-114">**Sign in failed:** *Unexpected error, try later*</span></span>

![Image de l’erreur d’échec de la signature - Erreur inattendue](images/f9c3bad127d636c1f150d79814f35d4c.png)

<span data-ttu-id="f87be-116">**Message:**</span><span class="sxs-lookup"><span data-stu-id="f87be-116">**Message:**</span></span>

<span data-ttu-id="f87be-117">Erreur inattendue, essayez ultérieurement</span><span class="sxs-lookup"><span data-stu-id="f87be-117">Unexpected error, try later</span></span>

<span data-ttu-id="f87be-118">**Cause :**</span><span class="sxs-lookup"><span data-stu-id="f87be-118">**Cause:**</span></span>

<span data-ttu-id="f87be-119">Une version antérieure de l’application « Microsoft Authenticator » est installée sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="f87be-119">You have an older version of "Microsoft Authenticator" app installed on your device.</span></span>

<span data-ttu-id="f87be-120">**Solution :**</span><span class="sxs-lookup"><span data-stu-id="f87be-120">**Solution:**</span></span>

<span data-ttu-id="f87be-121">Installer la dernière version et [les](https://play.google.com/store/apps/details?androidid=com.azure.authenticator) Microsoft Authenticator à partir de Google Play Store et essayer à nouveau</span><span class="sxs-lookup"><span data-stu-id="f87be-121">Install latest version and of [Microsoft Authenticator](https://play.google.com/store/apps/details?androidid=com.azure.authenticator) from Google Play Store and try again</span></span>

## <a name="sign-in-failed---invalid-license"></a><span data-ttu-id="f87be-122">Échec de la signature - Licence non valide</span><span class="sxs-lookup"><span data-stu-id="f87be-122">Sign in failed - invalid license</span></span>

<span data-ttu-id="f87be-123">**Échec de la signature : licence** non *valide, contactez l’administrateur*</span><span class="sxs-lookup"><span data-stu-id="f87be-123">**Sign in failed:** *Invalid license, please contact administrator*</span></span>

![Image de l’échec de la connectez-vous. Contactez l’administrateur](images/920e433f440fa1d3d298e6a2a43d4811.png)

<span data-ttu-id="f87be-125">**Message : licence** *non valide, contactez l’administrateur*</span><span class="sxs-lookup"><span data-stu-id="f87be-125">**Message:** *Invalid license, please contact administrator*</span></span>

<span data-ttu-id="f87be-126">**Cause :**</span><span class="sxs-lookup"><span data-stu-id="f87be-126">**Cause:**</span></span>

<span data-ttu-id="f87be-127">Vous n’avez pas Microsoft 365 licence attribuée ou votre organisation n’en a pas pour Microsoft 365 Entreprise abonnement.</span><span class="sxs-lookup"><span data-stu-id="f87be-127">You do not have Microsoft 365 license assigned, or your organization does not have a license for Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="f87be-128">**Solution :**</span><span class="sxs-lookup"><span data-stu-id="f87be-128">**Solution:**</span></span>

<span data-ttu-id="f87be-129">Contactez votre administrateur pour obtenir de l'aide.</span><span class="sxs-lookup"><span data-stu-id="f87be-129">Contact your administrator for help.</span></span>

## <a name="report-unsafe-site"></a><span data-ttu-id="f87be-130">Signaler un site non sécurisé</span><span class="sxs-lookup"><span data-stu-id="f87be-130">Report unsafe site</span></span>

<span data-ttu-id="f87be-131">Les sites web de hameçonnage usurpent l’identité de sites web dignes de confiance dans le but d’obtenir vos informations personnelles ou financières.</span><span class="sxs-lookup"><span data-stu-id="f87be-131">Phishing websites impersonate trustworthy websites for the purpose of obtaining your personal or financial information.</span></span> <span data-ttu-id="f87be-132">Consultez la page [Fournir des commentaires sur la protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) du réseau si vous souhaitez signaler un site web qui pourrait être un site de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="f87be-132">Visit the [Provide feedback about network protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) page if you want to report a website that could be a phishing site.</span></span>

## <a name="phishing-pages-arent-blocked-on-some-oem-devices"></a><span data-ttu-id="f87be-133">Les pages de hameçonnage ne sont pas bloquées sur certains appareils OEM</span><span class="sxs-lookup"><span data-stu-id="f87be-133">Phishing pages aren't blocked on some OEM devices</span></span>

<span data-ttu-id="f87be-134">**S’applique à :** OEM spécifiques uniquement</span><span class="sxs-lookup"><span data-stu-id="f87be-134">**Applies to:** Specific OEMs only</span></span>

-   <span data-ttu-id="f87be-135">**Érmi**</span><span class="sxs-lookup"><span data-stu-id="f87be-135">**Xiaomi**</span></span>

<span data-ttu-id="f87be-136">L’hameçonnage et les menaces web dangereuses détectées par Defender pour Endpoint pour Android ne sont pas bloqués sur certains appareils.</span><span class="sxs-lookup"><span data-stu-id="f87be-136">Phishing and harmful web threats that are detected by Defender for Endpoint for Android are not blocked on some Xiaomi devices.</span></span> <span data-ttu-id="f87be-137">Les fonctionnalités suivantes ne fonctionnent pas sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="f87be-137">The following functionality doesn't work on these devices.</span></span>

![Image du site signalé comme dangereux](images/0c04975c74746a5cdb085e1d9386e713.png)


<span data-ttu-id="f87be-139">**Cause :**</span><span class="sxs-lookup"><span data-stu-id="f87be-139">**Cause:**</span></span>

<span data-ttu-id="f87be-140">Les appareils Demi incluent un nouveau modèle d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="f87be-140">Xiaomi devices include a new permission model.</span></span> <span data-ttu-id="f87be-141">Cela empêche Defender pour point de terminaison pour Android d’afficher des fenêtres pop-up alors qu’elle s’exécute en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f87be-141">This prevents Defender for Endpoint for Android from displaying pop-up windows while it runs in the background.</span></span>

<span data-ttu-id="f87be-142">Autorisation d’appareils : « Afficher les fenêtres pop-up en cours d’exécution en arrière-plan ».</span><span class="sxs-lookup"><span data-stu-id="f87be-142">Xiaomi devices permission: "Display pop-up windows while running in the background."</span></span>

![Image du paramètre de fenêtre pop-up](images/6e48e7b29daf50afddcc6c8c7d59fd64.png)

<span data-ttu-id="f87be-144">**Solution :**</span><span class="sxs-lookup"><span data-stu-id="f87be-144">**Solution:**</span></span>

<span data-ttu-id="f87be-145">Activez l’autorisation requise sur les appareils DeMi.</span><span class="sxs-lookup"><span data-stu-id="f87be-145">Enable the required permission on Xiaomi devices.</span></span>

- <span data-ttu-id="f87be-146">Afficher les fenêtres pop-up en cours d’exécution en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f87be-146">Display pop-up windows while running in the background.</span></span>
