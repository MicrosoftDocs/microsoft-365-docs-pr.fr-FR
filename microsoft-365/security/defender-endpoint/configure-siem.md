---
title: Pull detections to your SIEM tools from Microsoft Defender for Endpoint
description: Découvrez comment utiliser l’API REST et configurer les outils de gestion des événements et des informations de sécurité pris en charge pour recevoir et tirer des détections.
keywords: configurer siem, outils de gestion des informations de sécurité et des événements, splunk, arcsight, indicateurs personnalisés, api rest, définitions d’alerte, indicateurs de compromis
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
ms.openlocfilehash: 97a64c8537ff2a6f9948ed6ed056b8aa7379ce69
ms.sourcegitcommit: 1244bbc4a3d150d37980cab153505ca462fa7ddc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51222334"
---
# <a name="pull-detections-to-your-siem-tools"></a><span data-ttu-id="962c3-104">Tirer les détections vers vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="962c3-104">Pull detections to your SIEM tools</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="962c3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="962c3-105">**Applies to:**</span></span>
- [<span data-ttu-id="962c3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="962c3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="962c3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="962c3-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="962c3-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="962c3-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="962c3-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="962c3-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configuresiem-abovefoldlink) 

## <a name="pull-detections-using-security-information-and-events-management-siem-tools"></a><span data-ttu-id="962c3-110">Détections de pull à l’aide des outils de gestion des événements et des informations de sécurité (SIEM)</span><span class="sxs-lookup"><span data-stu-id="962c3-110">Pull detections using security information and events management (SIEM) tools</span></span>

>[!NOTE]
>- <span data-ttu-id="962c3-111">[Microsoft Defender pour l’alerte de point de terminaison](alerts.md) est composé d’une ou plusieurs détections.</span><span class="sxs-lookup"><span data-stu-id="962c3-111">[Microsoft Defender for Endpoint Alert](alerts.md) is composed from one or more detections.</span></span>
>- <span data-ttu-id="962c3-112">[Microsoft Defender pour la détection des points](api-portal-mapping.md) de terminaison est composé de l’événement suspect qui s’est produit sur l’appareil et de ses détails d’alerte associés.</span><span class="sxs-lookup"><span data-stu-id="962c3-112">[Microsoft Defender for Endpoint Detection](api-portal-mapping.md) is composed from the suspicious event occurred on the Device and its related Alert details.</span></span>
><span data-ttu-id="962c3-113">-The Microsoft Defender for Endpoint Alert API is the latest API for alert consumption and contain a detailed list of related evidence for each alert.</span><span class="sxs-lookup"><span data-stu-id="962c3-113">-The Microsoft Defender for Endpoint Alert API is the latest API for alert consumption and contain a detailed list of related evidence for each alert.</span></span> <span data-ttu-id="962c3-114">Pour plus d’informations, voir [Méthodes et propriétés d’alerte et](alerts.md) Liste des [alertes.](get-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="962c3-114">For more information, see [Alert methods and properties](alerts.md) and [List alerts](get-alerts.md).</span></span>

<span data-ttu-id="962c3-115">Defender pour le point de terminaison prend en charge les outils de gestion des événements et des informations de sécurité (SIEM) pour tirer les détections.</span><span class="sxs-lookup"><span data-stu-id="962c3-115">Defender for Endpoint supports security information and event management (SIEM) tools to pull detections.</span></span> <span data-ttu-id="962c3-116">Defender pour le point de terminaison expose les alertes via un point de terminaison HTTPS hébergé dans Azure.</span><span class="sxs-lookup"><span data-stu-id="962c3-116">Defender for Endpoint exposes alerts through an HTTPS endpoint hosted in Azure.</span></span> <span data-ttu-id="962c3-117">Le point de terminaison peut être configuré pour tirer les détections de votre client d’entreprise dans Azure Active Directory (AAD) à l’aide du protocole d’authentification OAuth 2.0 pour une application AAD qui représente le connecteur SIEM spécifique installé dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="962c3-117">The endpoint can be configured to pull detections from your enterprise tenant in Azure Active Directory (AAD) using the OAuth 2.0 authentication protocol for an AAD application that represents the specific SIEM connector installed in your environment.</span></span>

<span data-ttu-id="962c3-118">Defender pour le point de terminaison prend actuellement en charge les outils de solution SIEM spécifiques suivants via un modèle d’intégration SIEM dédié :</span><span class="sxs-lookup"><span data-stu-id="962c3-118">Defender for Endpoint currently supports the following specific SIEM solution tools through a dedicated SIEM integration model:</span></span>

- <span data-ttu-id="962c3-119">IBM QRadar</span><span class="sxs-lookup"><span data-stu-id="962c3-119">IBM QRadar</span></span>
- <span data-ttu-id="962c3-120">Micro Focus ArcSight</span><span class="sxs-lookup"><span data-stu-id="962c3-120">Micro Focus ArcSight</span></span>

<span data-ttu-id="962c3-121">D’autres solutions SIEM (telles que Splunk, RSA NetWitness) sont pris en charge via un modèle d’intégration différent basé sur la nouvelle API d’alerte.</span><span class="sxs-lookup"><span data-stu-id="962c3-121">Other SIEM solutions (such as Splunk, RSA NetWitness) are supported through a different integration model based on the new Alert API.</span></span> <span data-ttu-id="962c3-122">Pour plus d’informations, consultez la page [Application](https://securitycenter.microsoft.com/interoperability/partners) partenaire et sélectionnez la section Informations sur la sécurité et Analyse pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="962c3-122">For more information, view the [Partner application](https://securitycenter.microsoft.com/interoperability/partners) page and select the Security Information and Analytics section for full details.</span></span>

<span data-ttu-id="962c3-123">Pour utiliser l’un de ces outils SIEM pris en charge, vous devez :</span><span class="sxs-lookup"><span data-stu-id="962c3-123">To use either of these supported SIEM tools, you'll need to:</span></span>

- [<span data-ttu-id="962c3-124">Activer l’intégration SIEM dans Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="962c3-124">Enable SIEM integration in Defender for Endpoint</span></span>](enable-siem-integration.md)
- <span data-ttu-id="962c3-125">Configurez l’outil SIEM pris en charge :</span><span class="sxs-lookup"><span data-stu-id="962c3-125">Configure the supported SIEM tool:</span></span>
     - [<span data-ttu-id="962c3-126">Configurer Micro Focus ArcSight pour tirer Defender pour les détections de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="962c3-126">Configure Micro Focus ArcSight to pull Defender for Endpoint detections</span></span>](configure-arcsight.md)
     - <span data-ttu-id="962c3-127">Configurez IBM QRadar pour tirer Defender pour les détections de points de terminaison Pour plus d’informations, voir [le Centre de connaissances IBM.](https://www.ibm.com/support/knowledgecenter/SS42VS_DSM/com.ibm.dsm.doc/c_dsm_guide_MS_Win_Defender_ATP_overview.html?cp=SS42VS_7.3.1)</span><span class="sxs-lookup"><span data-stu-id="962c3-127">Configure IBM QRadar to pull Defender for Endpoint detections For more information, see [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SS42VS_DSM/com.ibm.dsm.doc/c_dsm_guide_MS_Win_Defender_ATP_overview.html?cp=SS42VS_7.3.1).</span></span>

<span data-ttu-id="962c3-128">Pour plus d’informations sur la liste des champs exposés dans l’API de détection, voir Defender pour les champs de détection [de point de terminaison.](api-portal-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="962c3-128">For more information on the list of fields exposed in the Detection API, see [Defender for Endpoint Detection fields](api-portal-mapping.md).</span></span>
