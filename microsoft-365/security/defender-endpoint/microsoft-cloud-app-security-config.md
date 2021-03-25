---
title: Configurer l’intégration de Microsoft Cloud App Security
ms.reviewer: ''
description: Découvrez comment activer les paramètres pour activer l’intégration de Microsoft Defender for Endpoint à Microsoft Cloud App Security.
keywords: cloud, application, sécurité, paramètres, intégration, découverte, rapport
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
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: f5e2919ae3fcbbb443f6d160c68633ee3427ae5a
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187528"
---
# <a name="configure-microsoft-cloud-app-security-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="2dd62-104">Configurer Microsoft Cloud App Security dans Microsoft Defender pour endpoint</span><span class="sxs-lookup"><span data-stu-id="2dd62-104">Configure Microsoft Cloud App Security in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2dd62-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2dd62-105">**Applies to:**</span></span>
- [<span data-ttu-id="2dd62-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2dd62-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2dd62-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2dd62-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="2dd62-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2dd62-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2dd62-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2dd62-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="2dd62-110">Pour tirer parti des signaux de découverte d’application cloud Microsoft Defender for Endpoint, activer l’intégration de Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="2dd62-110">To benefit from Microsoft Defender for Endpoint cloud app discovery signals, turn on Microsoft Cloud App Security integration.</span></span>

>[!NOTE]
><span data-ttu-id="2dd62-111">Cette fonctionnalité sera disponible avec une licence E5 pour [Enterprise Mobility + Security](https://www.microsoft.com/cloud-platform/enterprise-mobility-security) sur les appareils exécutant Windows 10, version 1709 (os Build 16299.1085 avec [KB4493441](https://support.microsoft.com/help/4493441)), Windows 10, version 1803 (os build 17134.704 avec [KB4493464](https://support.microsoft.com/help/4493464)), Windows 10, version 1809 (os build 17763.379 avec [KB4489899)](https://support.microsoft.com/help/4489899)ou versions ultérieures de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2dd62-111">This feature will be available with an E5 license for [Enterprise Mobility + Security](https://www.microsoft.com/cloud-platform/enterprise-mobility-security) on devices running Windows 10, version 1709 (OS Build 16299.1085 with [KB4493441](https://support.microsoft.com/help/4493441)), Windows 10, version 1803 (OS Build 17134.704 with [KB4493464](https://support.microsoft.com/help/4493464)), Windows 10, version 1809 (OS Build 17763.379 with [KB4489899](https://support.microsoft.com/help/4489899)) or later Windows 10 versions.</span></span>

> <span data-ttu-id="2dd62-112">Consultez [l’intégration de Microsoft Defender for Endpoint avec Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/mde-integration) pour une intégration détaillée de Microsoft Defender for Endpoint avec Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="2dd62-112">See [Microsoft Defender for Endpoint integration with Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/mde-integration) for detailed integration of Microsoft Defender for Endpoint with Microsoft Cloud App Security.</span></span> 

## <a name="enable-microsoft-cloud-app-security-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="2dd62-113">Activer Microsoft Cloud App Security dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2dd62-113">Enable Microsoft Cloud App Security in Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="2dd62-114">Dans le volet de navigation, sélectionnez **Préférences configurer les**  >  **fonctionnalités avancées.**</span><span class="sxs-lookup"><span data-stu-id="2dd62-114">In the navigation pane, select **Preferences setup** > **Advanced features**.</span></span>
2. <span data-ttu-id="2dd62-115">Sélectionnez **Microsoft Cloud App Security et** basculez sur **Le.**</span><span class="sxs-lookup"><span data-stu-id="2dd62-115">Select **Microsoft Cloud App Security** and switch the toggle to **On**.</span></span>
3. <span data-ttu-id="2dd62-116">Cliquez **sur Enregistrer les préférences.**</span><span class="sxs-lookup"><span data-stu-id="2dd62-116">Click **Save preferences**.</span></span>

<span data-ttu-id="2dd62-117">Une fois activé, Microsoft Defender pour le point de terminaison démarre immédiatement le transmission des signaux de découverte vers Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="2dd62-117">Once activated, Microsoft Defender for Endpoint will immediately start forwarding discovery signals to Cloud App Security.</span></span>

## <a name="view-the-data-collected"></a><span data-ttu-id="2dd62-118">Afficher les données collectées</span><span class="sxs-lookup"><span data-stu-id="2dd62-118">View the data collected</span></span>

<span data-ttu-id="2dd62-119">Pour afficher et accéder aux données du point de terminaison Microsoft Defender dans Microsoft Cloud Apps Security, voir Examiner les appareils [dans Cloud App Security.](https://docs.microsoft.com/cloud-app-security/mde-integration#investigate-devices-in-cloud-app-security)</span><span class="sxs-lookup"><span data-stu-id="2dd62-119">To view and access Microsoft Defender for Endpoint data in Microsoft Cloud Apps Security, see [Investigate devices in Cloud App Security](https://docs.microsoft.com/cloud-app-security/mde-integration#investigate-devices-in-cloud-app-security).</span></span>


<span data-ttu-id="2dd62-120">Pour plus d’informations sur la découverte dans le cloud, voir [Working with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span><span class="sxs-lookup"><span data-stu-id="2dd62-120">For more information about cloud discovery, see [Working with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>

<span data-ttu-id="2dd62-121">Si vous souhaitez essayer Microsoft Cloud App Security, consultez La version d’essai [de Microsoft Cloud App Security.](https://signup.microsoft.com/Signup?OfferId=757c4c34-d589-46e4-9579-120bba5c92ed&ali=1)</span><span class="sxs-lookup"><span data-stu-id="2dd62-121">If you're interested in trying Microsoft Cloud App Security, see [Microsoft Cloud App Security Trial](https://signup.microsoft.com/Signup?OfferId=757c4c34-d589-46e4-9579-120bba5c92ed&ali=1).</span></span>

## <a name="related-topic"></a><span data-ttu-id="2dd62-122">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="2dd62-122">Related topic</span></span>
- [<span data-ttu-id="2dd62-123">Intégration de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="2dd62-123">Microsoft Cloud App Security integration</span></span>](microsoft-cloud-app-security-integration.md)
