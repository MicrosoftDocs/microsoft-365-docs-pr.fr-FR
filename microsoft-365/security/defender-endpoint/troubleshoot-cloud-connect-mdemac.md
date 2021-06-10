---
title: Résoudre les problèmes de connectivité cloud pour Microsoft Defender pour endpoint sur macOS
description: Cette rubrique décrit comment résoudre les problèmes de connectivité cloud pour Microsoft Defender pour endpoint sur macOS
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, mac, installation, déployer, désinstallation, intune, jamf, macos,pératin, mojave, high sierra
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: v-lsaldanha
author: lovina-saldanha
localization_priority: normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 291cd3016dcb4e1a321f39b4d2731ce2068b6544
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935208"
---
# <a name="troubleshoot-cloud-connectivity-issues-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="4dbe1-104">Résoudre les problèmes de connectivité cloud pour Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="4dbe1-104">Troubleshoot cloud connectivity issues for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4dbe1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4dbe1-105">**Applies to:**</span></span>
- [<span data-ttu-id="4dbe1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4dbe1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="4dbe1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4dbe1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="4dbe1-108">**Plateforme** macOS</span><span class="sxs-lookup"><span data-stu-id="4dbe1-108">**Platform** macOS</span></span>

<span data-ttu-id="4dbe1-109">Cette rubrique décrit comment résoudre les problèmes de connectivité cloud pour Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-109">This topic describes how to Troubleshoot cloud connectivity issues for Microsoft Defender for Endpoint on macOS.</span></span>

## <a name="run-the-connectivity-test"></a><span data-ttu-id="4dbe1-110">Exécuter le test de connectivité</span><span class="sxs-lookup"><span data-stu-id="4dbe1-110">Run the connectivity test</span></span>
<span data-ttu-id="4dbe1-111">Pour tester si Defender pour point de terminaison sur Mac peut communiquer avec le cloud avec les paramètres réseau actuels, exécutez un test de connectivité à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="4dbe1-111">To test if Defender for Endpoint on Mac can communicate to the cloud with the current network settings, run a connectivity test from the command line:</span></span>

```Bash
mdatp connectivity test
```

<span data-ttu-id="4dbe1-112">sortie attendue :</span><span class="sxs-lookup"><span data-stu-id="4dbe1-112">expected output:</span></span>
```Bash
Testing connection with https://cdn.x.cp.wd.microsoft.com/ping ... [OK]
Testing connection with https://eu-cdn.x.cp.wd.microsoft.com/ping ... [OK]
Testing connection with https://wu-cdn.x.cp.wd.microsoft.com/ping ... [OK]
Testing connection with https://x.cp.wd.microsoft.com/api/report ... [OK]
Testing connection with https://winatp-gw-cus.microsoft.com/test ... [OK]
Testing connection with https://winatp-gw-eus.microsoft.com/test ... [OK]
Testing connection with https://winatp-gw-weu.microsoft.com/test ... [OK]
Testing connection with https://winatp-gw-neu.microsoft.com/test ... [OK]
Testing connection with https://winatp-gw-ukw.microsoft.com/test ... [OK]
Testing connection with https://winatp-gw-uks.microsoft.com/test ... [OK]
Testing connection with https://eu-v20.events.data.microsoft.com/ping ... [OK]
Testing connection with https://us-v20.events.data.microsoft.com/ping ... [OK]
Testing connection with https://uk-v20.events.data.microsoft.com/ping ... [OK]
Testing connection with https://v20.events.data.microsoft.com/ping ... [OK]
```

<span data-ttu-id="4dbe1-113">Si le test de connectivité échoue, vérifiez si [](microsoft-defender-endpoint-mac.md#network-connections) l’appareil dispose d’un accès à Internet et si l’un des points de terminaison requis par le produit est bloqué par un proxy ou un pare-feu.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-113">If the connectivity test fails, check if the device has Internet access and if [any of the endpoints required by the product](microsoft-defender-endpoint-mac.md#network-connections) are blocked by a proxy or firewall.</span></span>

<span data-ttu-id="4dbe1-114">Les échecs avec erreur d’erreur 35 ou 60 indiquent le rejet de l’épinglage de certificat, ce qui indique un problème potentiel avec l’inspection SSL ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-114">Failures with curl error 35 or 60 indicate certificate pinning rejection, which indicates a potential issue with SSL or HTTPS inspection.</span></span> <span data-ttu-id="4dbe1-115">Consultez les instructions ci-dessous concernant la configuration de l’inspection SSL.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-115">See instructions below regarding SSL inspection configuration.</span></span>

## <a name="troubleshooting-steps-for-environments-without-proxy-or-with-proxy-autoconfig-pac-or-with-web-proxy-autodiscovery-protocol-wpad"></a><span data-ttu-id="4dbe1-116">Étapes de résolution des problèmes pour les environnements sans proxy ou avec la mise en conférence automatique du proxy (PAC) ou avec le protocole WPAD (Web Proxy Autodiscovery Protocol)</span><span class="sxs-lookup"><span data-stu-id="4dbe1-116">Troubleshooting steps for environments without proxy or with Proxy autoconfig (PAC) or with Web Proxy Autodiscovery Protocol (WPAD)</span></span>
<span data-ttu-id="4dbe1-117">Utilisez la procédure suivante pour vérifier qu’une connexion n’est pas bloquée dans un environnement sans proxy ou avec la mise en service automatique du proxy (PAC) ou avec le protocole WPAD (Web Proxy Autodiscovery Protocol).</span><span class="sxs-lookup"><span data-stu-id="4dbe1-117">Use the following procedure to test that a connection is not blocked in an environment without a proxy or with Proxy autoconfig (PAC) or with Web Proxy Autodiscovery Protocol (WPAD).</span></span>

<span data-ttu-id="4dbe1-118">Si un proxy ou un pare-feu bloque le trafic anonyme, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-118">If a proxy or firewall is blocking anonymous traffic, make sure that anonymous traffic is permitted in the previously listed URLs.</span></span>

> [!WARNING]
> <span data-ttu-id="4dbe1-119">Les proxies authentifiés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-119">Authenticated proxies are not supported.</span></span> <span data-ttu-id="4dbe1-120">Assurez-vous que seuls pac, WPAD ou un proxy statique est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-120">Ensure that only PAC, WPAD, or a static proxy is being used.</span></span> <span data-ttu-id="4dbe1-121">L’inspection et l’interception des proxies SSL ne sont pas non plus pris en charge pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-121">SSL inspection and intercepting proxies are also not supported for security reasons.</span></span> <span data-ttu-id="4dbe1-122">Configurez une exception pour l’inspection SSL et votre serveur proxy afin de transmettre directement les données de Microsoft Defender for Endpoint sur macOS aux URL pertinentes sans interception.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-122">Configure an exception for SSL inspection and your proxy server to directly pass through data from Microsoft Defender for Endpoint on macOS to the relevant URLs without interception.</span></span> <span data-ttu-id="4dbe1-123">L’ajout de votre certificat d’interception au magasin global n’autorise pas l’interception.</span><span class="sxs-lookup"><span data-stu-id="4dbe1-123">Adding your interception certificate to the global store will not allow for interception.</span></span>
<span data-ttu-id="4dbe1-124">Pour tester qu’une connexion n’est pas bloquée : dans un navigateur tel que Microsoft Edge pour Mac ou Safari, ouvrez https://x.cp.wd.microsoft.com/api/report et https://cdn.x.cp.wd.microsoft.com/ping .</span><span class="sxs-lookup"><span data-stu-id="4dbe1-124">To test that a connection is not blocked: In a browser such as Microsoft Edge for Mac or Safari open https://x.cp.wd.microsoft.com/api/report and https://cdn.x.cp.wd.microsoft.com/ping.</span></span>

<span data-ttu-id="4dbe1-125">Éventuellement, dans Terminal, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4dbe1-125">Optionally, in Terminal, run the following command:</span></span>

```Bash
curl -w ' %{url_effective}\n' 'https://x.cp.wd.microsoft.com/api/report' 'https://cdn.x.cp.wd.microsoft.com/ping' 
```

<span data-ttu-id="4dbe1-126">La sortie de cette commande doit être similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="4dbe1-126">The output from this command should be similar to:</span></span>
```bash
OK https://x.cp.wd.microsoft.com/api/report
OK https://cdn.x.cp.wd.microsoft.com/ping
```
