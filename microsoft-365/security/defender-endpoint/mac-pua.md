---
title: Détecter et bloquer les applications potentiellement indésirables avec Microsoft Defender ATP pour Mac
description: Détecter et bloquer les applications potentiellement indésirables (PUA) à l'aide de Microsoft Defender ATP pour Mac.
keywords: microsoft, defender, atp, mac, pua, pus
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: cf61c6a501a53ac03d3c4cc28068f7af4c0f88d6
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51688104"
---
# <a name="detect-and-block-potentially-unwanted-applications-with-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="7f896-104">Détecter et bloquer les applications potentiellement indésirables avec Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="7f896-104">Detect and block potentially unwanted applications with Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7f896-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7f896-105">**Applies to:**</span></span>
- [<span data-ttu-id="7f896-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7f896-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7f896-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7f896-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7f896-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7f896-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="7f896-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7f896-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


<span data-ttu-id="7f896-110">La fonctionnalité de protection des applications potentiellement indésirables (PUA) dans Microsoft Defender for Endpoint sur macOS peut détecter et bloquer les fichiers PUA sur les points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="7f896-110">The potentially unwanted application (PUA) protection feature in Microsoft Defender for Endpoint on macOS can detect and block PUA files on endpoints in your network.</span></span>

<span data-ttu-id="7f896-111">Ces applications ne sont pas considérées comme des virus, des programmes malveillants ou d'autres types de menaces, mais peuvent effectuer des actions sur les points de terminaison qui affectent leurs performances ou leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="7f896-111">These applications are not considered viruses, malware, or other types of threats, but might perform actions on endpoints that adversely affect their performance or use.</span></span> <span data-ttu-id="7f896-112">PuA peut également faire référence à des applications considérées comme de mauvaise réputation.</span><span class="sxs-lookup"><span data-stu-id="7f896-112">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="7f896-113">Ces applications peuvent augmenter le risque d'infection de votre réseau par des programmes malveillants, rendre l'identification des programmes malveillants plus difficile et entraîner une perte de ressources informatiques lors du nettoyage des applications.</span><span class="sxs-lookup"><span data-stu-id="7f896-113">These applications can increase the risk of your network being infected with malware, cause malware infections to be harder to identify, and can waste IT resources in cleaning up the applications.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="7f896-114">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="7f896-114">How it works</span></span>

<span data-ttu-id="7f896-115">Microsoft Defender pour le point de terminaison sur macOS peut détecter et signaler des fichiers PUA.</span><span class="sxs-lookup"><span data-stu-id="7f896-115">Microsoft Defender for Endpoint on macOS can detect and report PUA files.</span></span> <span data-ttu-id="7f896-116">Lorsqu'ils sont configurés en mode de blocage, les fichiers PUA sont placés en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="7f896-116">When configured in blocking mode, PUA files are moved to the quarantine.</span></span>

<span data-ttu-id="7f896-117">Lorsqu'une puA est détectée sur un point de terminaison, Microsoft Defender pour Endpoint sur macOS présente une notification à l'utilisateur, sauf si les notifications ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="7f896-117">When a PUA is detected on an endpoint, Microsoft Defender for Endpoint on macOS presents a notification to the user, unless notifications have been disabled.</span></span> <span data-ttu-id="7f896-118">Le nom de la menace contient le mot « Application ».</span><span class="sxs-lookup"><span data-stu-id="7f896-118">The threat name will contain the word "Application".</span></span>

## <a name="configure-pua-protection"></a><span data-ttu-id="7f896-119">Configurer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="7f896-119">Configure PUA protection</span></span>

<span data-ttu-id="7f896-120">La protection PUA dans Microsoft Defender pour endpoint sur macOS peut être configurée de l'une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f896-120">PUA protection in Microsoft Defender for Endpoint on macOS can be configured in one of the following ways:</span></span>

- <span data-ttu-id="7f896-121">**Désactivé**: la protection PUA est désactivée.</span><span class="sxs-lookup"><span data-stu-id="7f896-121">**Off**: PUA protection is disabled.</span></span>
- <span data-ttu-id="7f896-122">**Audit**: les fichiers PUA sont signalés dans les journaux du produit, mais pas dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7f896-122">**Audit**: PUA files are reported in the product logs, but not in Microsoft Defender Security Center.</span></span> <span data-ttu-id="7f896-123">Aucune notification n'est présentée à l'utilisateur et aucune action n'est prise par le produit.</span><span class="sxs-lookup"><span data-stu-id="7f896-123">No notification is presented to the user and no action is taken by the product.</span></span>
- <span data-ttu-id="7f896-124">**Bloquer**: les fichiers PUA sont signalés dans les journaux du produit et dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7f896-124">**Block**: PUA files are reported in the product logs and in Microsoft Defender Security Center.</span></span> <span data-ttu-id="7f896-125">Une notification est présentée à l'utilisateur et une action est prise par le produit.</span><span class="sxs-lookup"><span data-stu-id="7f896-125">The user is presented with a notification and action is taken by the product.</span></span>

>[!WARNING]
><span data-ttu-id="7f896-126">Par défaut, la protection PUA est configurée en mode **audit.**</span><span class="sxs-lookup"><span data-stu-id="7f896-126">By default, PUA protection is configured in **Audit** mode.</span></span>

<span data-ttu-id="7f896-127">Vous pouvez configurer la façon dont les fichiers PUA sont gérés à partir de la ligne de commande ou de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="7f896-127">You can configure how PUA files are handled from the command line or from the management console.</span></span>

### <a name="use-the-command-line-tool-to-configure-pua-protection"></a><span data-ttu-id="7f896-128">Utilisez l'outil de ligne de commande pour configurer la protection PUA :</span><span class="sxs-lookup"><span data-stu-id="7f896-128">Use the command-line tool to configure PUA protection:</span></span>

<span data-ttu-id="7f896-129">Dans Terminal, exécutez la commande suivante pour configurer la protection PUA :</span><span class="sxs-lookup"><span data-stu-id="7f896-129">In Terminal, execute the following command to configure PUA protection:</span></span>

```bash
mdatp threat policy set --type potentially_unwanted_application --action [off|audit|block]
```

### <a name="use-the-management-console-to-configure-pua-protection"></a><span data-ttu-id="7f896-130">Utilisez la console de gestion pour configurer la protection PUA :</span><span class="sxs-lookup"><span data-stu-id="7f896-130">Use the management console to configure PUA protection:</span></span>

<span data-ttu-id="7f896-131">Dans votre entreprise, vous pouvez configurer la protection PUA à partir d'une console de gestion, telle que JAMF ou Intune, de la même façon que les autres paramètres de produit sont configurés.</span><span class="sxs-lookup"><span data-stu-id="7f896-131">In your enterprise, you can configure PUA protection from a management console, such as JAMF or Intune, similarly to how other product settings are configured.</span></span> <span data-ttu-id="7f896-132">Pour plus d'informations, voir la section [Paramètres](mac-preferences.md#threat-type-settings) du type de menace de la rubrique Définir les préférences de [Microsoft Defender pour Endpoint sur macOS.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="7f896-132">For more information, see the [Threat type settings](mac-preferences.md#threat-type-settings) section of the [Set preferences for Microsoft Defender for Endpoint on macOS](mac-preferences.md) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f896-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f896-133">Related topics</span></span>

- [<span data-ttu-id="7f896-134">Définir des préférences pour Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="7f896-134">Set preferences for Microsoft Defender for Endpoint on macOS</span></span>](mac-preferences.md)
