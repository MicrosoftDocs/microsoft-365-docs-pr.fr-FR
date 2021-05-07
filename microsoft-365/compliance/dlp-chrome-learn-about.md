---
title: En savoir plus sur l’extension de la conformité Microsoft.
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: L’extension de la conformité Microsoft étend la surveillance et le contrôle des activités des fichiers et des actions de protection au navigateur Google Chrome
ms.openlocfilehash: c8a5795b3be8b393fd3a934504449bf6db0c2f01
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52113380"
---
# <a name="learn-about-the-microsoft-compliance-extension-preview"></a><span data-ttu-id="5f506-103">En savoir plus sur l’extension de la conformité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f506-103">Learn about the Microsoft Compliance Extension (preview)</span></span>

<span data-ttu-id="5f506-104">[La protection contre la perte de données de point de terminaison](endpoint-dlp-learn-about.md) étend les fonctionnalités de surveillance et de protection des activités de la [Protection contre la perte de données (DLP) de Microsoft 365](dlp-learn-about-dlp.md) aux éléments sensibles sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f506-104">[Endpoint data loss prevention (endpoint DLP)](endpoint-dlp-learn-about.md) extends the activity monitoring and protection capabilities of [Microsoft 365 data loss prevention (DLP)](dlp-learn-about-dlp.md) to sensitive items that are on Windows 10 devices.</span></span> <span data-ttu-id="5f506-105">Une fois que les appareils sont intégrés aux solutions de conformité Microsoft 365, les informations relatives à ce que les utilisateurs font avec les éléments sensibles sont rendues visibles dans [l’Explorateur d’activités](data-classification-activity-explorer.md) et vous pouvez appliquer des actions de protection à ces éléments via [stratégies DLP](create-test-tune-dlp-policy.md).</span><span class="sxs-lookup"><span data-stu-id="5f506-105">Once devices are onboarded into the Microsoft 365 compliance solutions, the information about what users are doing with sensitive items is made visible in [activity explorer](data-classification-activity-explorer.md) and you can enforce protective actions on those items via [DLP policies](create-test-tune-dlp-policy.md).</span></span>

<span data-ttu-id="5f506-106">Une fois l’extension de conformité Microsoft installée sur un appareil Windows 10, les organisations peuvent surveiller quand un utilisateur tente d’accéder à un service cloud ou de charger un élément sensible vers un service cloud à l’aide de Google Chrome et d’appliquer des actions de protection via DLP.</span><span class="sxs-lookup"><span data-stu-id="5f506-106">Once the Microsoft Compliance Extension is installed on a Windows 10 device, organizations can monitor when a user attempts to access or upload a sensitive item to a cloud service using Google Chrome and enforce protective actions via DLP.</span></span>  

## <a name="activities-you-can-monitor-and-take-action-on"></a><span data-ttu-id="5f506-107">Les activités que vous pouvez surveiller et sur lesquels vous pouvez agir</span><span class="sxs-lookup"><span data-stu-id="5f506-107">Activities you can monitor and take action on</span></span>

<span data-ttu-id="5f506-108">L’extension de la conformité Microsoft vous permet d’auditer et de gérer les types d’activités suivants que les utilisateurs prennent sur les appareils exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f506-108">The Microsoft Compliance Extension enables you to audit and manage the following types of activities users take on sensitive items on devices running Windows 10.</span></span>

<span data-ttu-id="5f506-109">activité</span><span class="sxs-lookup"><span data-stu-id="5f506-109">activity</span></span> |<span data-ttu-id="5f506-110">description</span><span class="sxs-lookup"><span data-stu-id="5f506-110">description</span></span>  | <span data-ttu-id="5f506-111">actions de stratégie prises en charge</span><span class="sxs-lookup"><span data-stu-id="5f506-111">supported policy actions</span></span>|
|---------|---------|---------|
|<span data-ttu-id="5f506-112">fichier copié dans le cloud</span><span class="sxs-lookup"><span data-stu-id="5f506-112">file copied to cloud</span></span>  | <span data-ttu-id="5f506-113">Détecte lorsqu'un utilisateur tente de charger un élément sensible dans un domaine de service restreint par le biais du navigateur Chrome.</span><span class="sxs-lookup"><span data-stu-id="5f506-113">Detects when a user attempts to upload a sensitive item to a restricted service domain through the Chrome browser</span></span> |<span data-ttu-id="5f506-114">audit, blocage</span><span class="sxs-lookup"><span data-stu-id="5f506-114">audit, block</span></span>|
|<span data-ttu-id="5f506-115">fichier imprimé</span><span class="sxs-lookup"><span data-stu-id="5f506-115">file printed</span></span>  |<span data-ttu-id="5f506-116">Détecte quand un utilisateur tente d’imprimer un élément sensible ouvert dans le navigateur Chrome sur une imprimante locale ou réseau</span><span class="sxs-lookup"><span data-stu-id="5f506-116">Detects when a user attempts to print a sensitive item that is open in the Chrome browser to a local or network printer</span></span> |<span data-ttu-id="5f506-117">audit, blocage avec remplacement, blocage</span><span class="sxs-lookup"><span data-stu-id="5f506-117">audit, block with override, block</span></span>|
|<span data-ttu-id="5f506-118">Fichier copié dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="5f506-118">file copied to clipboard</span></span> |<span data-ttu-id="5f506-119">Détecte quand un utilisateur tente de copier des informations à partir d’un élément sensible en cours d’affichage dans le navigateur Chrome, puis de les coller dans une autre application, processus ou élément.</span><span class="sxs-lookup"><span data-stu-id="5f506-119">Detects when a user attempts to copy information from a sensitive item that is being viewed in the Chrome browser and then paste it into another app, process, or item.</span></span> |<span data-ttu-id="5f506-120">audit, blocage avec remplacement, blocage</span><span class="sxs-lookup"><span data-stu-id="5f506-120">audit, block with override, block</span></span>|
|<span data-ttu-id="5f506-121">Fichier copié dans un stockage amovible</span><span class="sxs-lookup"><span data-stu-id="5f506-121">file copied to removable storage</span></span>    | <span data-ttu-id="5f506-122">Détecte quand un utilisateur tente de copier un élément ou des informations sensibles d’un élément sensible ouvert dans le navigateur Chrome pour un support amovible ou un périphérique USB</span><span class="sxs-lookup"><span data-stu-id="5f506-122">Detects when a user attempts to copy a sensitive item or information from a sensitive item that is open in the Chrome browser to removable media or USB device</span></span> |<span data-ttu-id="5f506-123">audit, blocage avec remplacement, blocage</span><span class="sxs-lookup"><span data-stu-id="5f506-123">audit, block with override, block</span></span>|
|<span data-ttu-id="5f506-124">fichier copié sur le partage réseau</span><span class="sxs-lookup"><span data-stu-id="5f506-124">file copied to network share</span></span>  |<span data-ttu-id="5f506-125">Détecte quand un utilisateur tente de copier un élément ou des informations sensibles d’un élément sensible ouvert dans le navigateur Chrome vers un partage réseau ou un lecteur réseau mappé.</span><span class="sxs-lookup"><span data-stu-id="5f506-125">Detects when a user attempts to copy a sensitive item or information from a sensitive item that is open in the Chrome browser  to a network share or mapped network drive.</span></span>|<span data-ttu-id="5f506-126">audit, blocage avec remplacement, blocage</span><span class="sxs-lookup"><span data-stu-id="5f506-126">audit, block with override, block</span></span> |

## <a name="deployment-process"></a><span data-ttu-id="5f506-127">Processus de déploiement</span><span class="sxs-lookup"><span data-stu-id="5f506-127">Deployment process</span></span>
1. [<span data-ttu-id="5f506-128">Prise en main des points de terminaison de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="5f506-128">Get started with endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
2. [<span data-ttu-id="5f506-129">Outils et méthodes d’intégration pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="5f506-129">Onboarding tools and methods for Windows 10 devices</span></span>](dlp-configure-endpoints.md)
3. [<span data-ttu-id="5f506-130">Installer l’extension sur vos appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="5f506-130">Install the extension on your Windows 10 devices</span></span>](dlp-chrome-get-started.md)
4. <span data-ttu-id="5f506-131">[Créer ou modifier des stratégies DLP](create-test-tune-dlp-policy.md) qui limitent le chargement vers un service cloud ou l’accès par des actions de navigateurs non autorisé et les appliquent à vos appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="5f506-131">[Create or edit DLP policies](create-test-tune-dlp-policy.md) that restrict upload to cloud service, or access by unallowed browsers actions and apply them to your Windows 10 devices</span></span>

## <a name="next-steps"></a><span data-ttu-id="5f506-132">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5f506-132">Next steps</span></span>

<span data-ttu-id="5f506-133">Consultez [Prise en main de l’extension de la conformité Microsoft](dlp-chrome-get-started.md) pour des procédures et scénarios de déploiement complets.</span><span class="sxs-lookup"><span data-stu-id="5f506-133">See [Get started with the Microsoft Compliance Extension](dlp-chrome-get-started.md) for complete deployment procedures and scenarios.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f506-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f506-134">See also</span></span>

- [<span data-ttu-id="5f506-135">Prise en main de l’extension de la conformité Microsoft</span><span class="sxs-lookup"><span data-stu-id="5f506-135">Get started with Microsoft Compliance Extension</span></span>](dlp-chrome-get-started.md)
- [<span data-ttu-id="5f506-136">Découvrir la protection contre la perte de données des point de terminaison de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5f506-136">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="5f506-137">Prise en main des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="5f506-137">Getting started with Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-getting-started.md)
- [<span data-ttu-id="5f506-138">Utilisation des points de terminaison de protection contre la perte de données Microsoft (préversion)</span><span class="sxs-lookup"><span data-stu-id="5f506-138">Using Microsoft Endpoint data loss prevention</span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="5f506-139">En savoir plus sur la prévention des pertes de données</span><span class="sxs-lookup"><span data-stu-id="5f506-139">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="5f506-140">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="5f506-140">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="5f506-141">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="5f506-141">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="5f506-142">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5f506-142">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)
- [<span data-ttu-id="5f506-143">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="5f506-143">Insider Risk management</span></span>](insider-risk-management.md)
