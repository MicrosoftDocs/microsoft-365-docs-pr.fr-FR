---
title: Détecter et bloquer les applications potentiellement indésirables avec Microsoft Defender ATP pour Linux
description: Détecter et bloquer les applications potentiellement indésirables (PUA) à l’aide de Microsoft Defender ATP pour Linux.
keywords: microsoft, defender, atp, linux, pua, pus
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: a6f2e2057ca78cb0e1114ed86829cd931dc1cd2b
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587550"
---
# <a name="detect-and-block-potentially-unwanted-applications-with-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="83d91-104">Détecter et bloquer les applications potentiellement indésirables avec Microsoft Defender pour Endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="83d91-104">Detect and block potentially unwanted applications with Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="83d91-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="83d91-105">**Applies to:**</span></span>
- [<span data-ttu-id="83d91-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="83d91-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="83d91-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="83d91-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="83d91-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="83d91-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="83d91-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="83d91-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="83d91-110">La fonctionnalité de protection des applications potentiellement indésirables (PUA) dans Defender for Endpoint for Linux peut détecter et bloquer les fichiers PUA sur les points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="83d91-110">The potentially unwanted application (PUA) protection feature in Defender for Endpoint for Linux can detect and block PUA files on endpoints in your network.</span></span>

<span data-ttu-id="83d91-111">Ces applications ne sont pas considérées comme des virus, des programmes malveillants ou d’autres types de menaces, mais peuvent effectuer des actions sur les points de terminaison qui affectent leurs performances ou leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="83d91-111">These applications are not considered viruses, malware, or other types of threats, but might perform actions on endpoints that adversely affect their performance or use.</span></span> <span data-ttu-id="83d91-112">PuA peut également faire référence à des applications considérées comme de mauvaise réputation.</span><span class="sxs-lookup"><span data-stu-id="83d91-112">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="83d91-113">Ces applications peuvent augmenter le risque d’infection de votre réseau par des programmes malveillants, rendre l’identification des programmes malveillants plus difficile et entraîner une perte de ressources informatiques lors du nettoyage des applications.</span><span class="sxs-lookup"><span data-stu-id="83d91-113">These applications can increase the risk of your network being infected with malware, cause malware infections to be harder to identify, and can waste IT resources in cleaning up the applications.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="83d91-114">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="83d91-114">How it works</span></span>

<span data-ttu-id="83d91-115">Defender pour le point de terminaison pour Linux peut détecter et signaler des fichiers PUA.</span><span class="sxs-lookup"><span data-stu-id="83d91-115">Defender for Endpoint for Linux can detect and report PUA files.</span></span> <span data-ttu-id="83d91-116">Lorsqu’ils sont configurés en mode de blocage, les fichiers PUA sont placés en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="83d91-116">When configured in blocking mode, PUA files are moved to the quarantine.</span></span>

<span data-ttu-id="83d91-117">Lorsqu’une puA est détectée sur un point de terminaison, Defender pour Endpoint pour Linux conserve un enregistrement de l’infection dans l’historique des menaces.</span><span class="sxs-lookup"><span data-stu-id="83d91-117">When a PUA is detected on an endpoint, Defender for Endpoint for Linux keeps a record of the infection in the threat history.</span></span> <span data-ttu-id="83d91-118">L’historique peut être visualisé à partir du portail centre de sécurité Microsoft Defender ou via l’outil `mdatp` en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="83d91-118">The history can be visualized from the Microsoft Defender Security Center portal or through the `mdatp` command-line tool.</span></span> <span data-ttu-id="83d91-119">Le nom de la menace contient le mot « Application ».</span><span class="sxs-lookup"><span data-stu-id="83d91-119">The threat name will contain the word "Application".</span></span>

## <a name="configure-pua-protection"></a><span data-ttu-id="83d91-120">Configurer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="83d91-120">Configure PUA protection</span></span>

<span data-ttu-id="83d91-121">La protection PUA dans Defender for Endpoint pour Linux peut être configurée de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="83d91-121">PUA protection in Defender for Endpoint for Linux can be configured in one of the following ways:</span></span>

- <span data-ttu-id="83d91-122">**Désactivé**: la protection PUA est désactivée.</span><span class="sxs-lookup"><span data-stu-id="83d91-122">**Off**: PUA protection is disabled.</span></span>
- <span data-ttu-id="83d91-123">**Audit**: les fichiers PUA sont signalés dans les journaux du produit, mais pas dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="83d91-123">**Audit**: PUA files are reported in the product logs, but not in Microsoft Defender Security Center.</span></span> <span data-ttu-id="83d91-124">Aucun enregistrement de l’infection n’est stocké dans l’historique des menaces et aucune action n’est prise par le produit.</span><span class="sxs-lookup"><span data-stu-id="83d91-124">No record of the infection is stored in the threat history and no action is taken by the product.</span></span>
- <span data-ttu-id="83d91-125">**Bloquer**: les fichiers PUA sont signalés dans les journaux du produit et dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="83d91-125">**Block**: PUA files are reported in the product logs and in Microsoft Defender Security Center.</span></span> <span data-ttu-id="83d91-126">Un enregistrement de l’infection est stocké dans l’historique des menaces et une action est prise par le produit.</span><span class="sxs-lookup"><span data-stu-id="83d91-126">A record of the infection is stored in the threat history and action is taken by the product.</span></span>

>[!WARNING]
><span data-ttu-id="83d91-127">Par défaut, la protection PUA est configurée en mode **Audit.**</span><span class="sxs-lookup"><span data-stu-id="83d91-127">By default, PUA protection is configured in **Audit** mode.</span></span>

<span data-ttu-id="83d91-128">Vous pouvez configurer la façon dont les fichiers PUA sont gérés à partir de la ligne de commande ou de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="83d91-128">You can configure how PUA files are handled from the command line or from the management console.</span></span>

### <a name="use-the-command-line-tool-to-configure-pua-protection"></a><span data-ttu-id="83d91-129">Utilisez l’outil de ligne de commande pour configurer la protection PUA :</span><span class="sxs-lookup"><span data-stu-id="83d91-129">Use the command-line tool to configure PUA protection:</span></span>

<span data-ttu-id="83d91-130">Dans Terminal, exécutez la commande suivante pour configurer la protection PUA :</span><span class="sxs-lookup"><span data-stu-id="83d91-130">In Terminal, execute the following command to configure PUA protection:</span></span>

```bash
mdatp threat policy set --type potentially_unwanted_application --action [off|audit|block]
```

### <a name="use-the-management-console-to-configure-pua-protection"></a><span data-ttu-id="83d91-131">Utilisez la console de gestion pour configurer la protection PUA :</span><span class="sxs-lookup"><span data-stu-id="83d91-131">Use the management console to configure PUA protection:</span></span>

<span data-ttu-id="83d91-132">Dans votre entreprise, vous pouvez configurer la protection PUA à partir d’une console de gestion, telle qu’Unetem ou Ansible, de la même manière que d’autres paramètres de produit sont configurés.</span><span class="sxs-lookup"><span data-stu-id="83d91-132">In your enterprise, you can configure PUA protection from a management console, such as Puppet or Ansible, similarly to how other product settings are configured.</span></span> <span data-ttu-id="83d91-133">Pour plus d’informations, voir la section [Paramètres du type](linux-preferences.md#threat-type-settings) de menace de l’article Définir les préférences de [Defender pour Endpoint pour Linux.](linux-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="83d91-133">For more information, see the [Threat type settings](linux-preferences.md#threat-type-settings) section of the [Set preferences for Defender for Endpoint for Linux](linux-preferences.md) article.</span></span>

## <a name="related-articles"></a><span data-ttu-id="83d91-134">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="83d91-134">Related articles</span></span>

- [<span data-ttu-id="83d91-135">Définir des préférences pour Defender pour le point de terminaison pour Linux</span><span class="sxs-lookup"><span data-stu-id="83d91-135">Set preferences for Defender for Endpoint for Linux</span></span>](linux-preferences.md)
