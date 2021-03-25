---
title: Résoudre les problèmes de connectivité cloud pour Microsoft Defender ATP pour Linux
ms.reviewer: ''
description: Résoudre les problèmes de connectivité cloud pour Microsoft Defender ATP pour Linux
keywords: microsoft, defender, atp, linux, cloud, connectivité, communication
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
ms.openlocfilehash: c9f8f78f4b3574bfc9848fe8d75f5077427d722b
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187432"
---
# <a name="troubleshoot-cloud-connectivity-issues-for-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="35528-104">Résoudre les problèmes de connectivité cloud pour Microsoft Defender pour Endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="35528-104">Troubleshoot cloud connectivity issues for Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="35528-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="35528-105">**Applies to:**</span></span>
- [<span data-ttu-id="35528-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="35528-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="35528-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="35528-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="35528-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="35528-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="35528-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="35528-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

## <a name="run-the-connectivity-test"></a><span data-ttu-id="35528-110">Exécuter le test de connectivité</span><span class="sxs-lookup"><span data-stu-id="35528-110">Run the connectivity test</span></span>

<span data-ttu-id="35528-111">Pour tester si Defender pour Endpoint pour Linux peut communiquer avec le cloud avec les paramètres réseau actuels, exécutez un test de connectivité à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="35528-111">To test if Defender for Endpoint for Linux can communicate to the cloud with the current network settings, run a connectivity test from the command line:</span></span>

```bash
mdatp connectivity test
```

<span data-ttu-id="35528-112">sortie attendue :</span><span class="sxs-lookup"><span data-stu-id="35528-112">expected output:</span></span>

```output
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

<span data-ttu-id="35528-113">Si le test de connectivité échoue, vérifiez si [](microsoft-defender-endpoint-linux.md#network-connections) l’appareil dispose d’un accès à Internet et si l’un des points de terminaison requis par le produit est bloqué par un proxy ou un pare-feu.</span><span class="sxs-lookup"><span data-stu-id="35528-113">If the connectivity test fails, check if the device has Internet access and if [any of the endpoints required by the product](microsoft-defender-endpoint-linux.md#network-connections) are blocked by a proxy or firewall.</span></span>

<span data-ttu-id="35528-114">Les échecs avec erreur d’erreur 35 ou 60 indiquent le rejet de l’épinglage du certificat.</span><span class="sxs-lookup"><span data-stu-id="35528-114">Failures with curl error 35 or 60, indicate certificate pinning rejection.</span></span> <span data-ttu-id="35528-115">Vérifiez si la connexion est sous inspection SSL ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="35528-115">Please check if the connection is under SSL or HTTPS inspection.</span></span> <span data-ttu-id="35528-116">Si c’est le cas, ajoutez Microsoft Defender pour le point de terminaison à la liste d’accès.</span><span class="sxs-lookup"><span data-stu-id="35528-116">If so, add Microsoft Defender for Endpoint to the allow list.</span></span>

## <a name="troubleshooting-steps-for-environments-without-proxy-or-with-transparent-proxy"></a><span data-ttu-id="35528-117">Étapes de résolution des problèmes pour les environnements sans proxy ou avec proxy transparent</span><span class="sxs-lookup"><span data-stu-id="35528-117">Troubleshooting steps for environments without proxy or with transparent proxy</span></span>

<span data-ttu-id="35528-118">Pour vérifier qu’une connexion n’est pas bloquée dans un environnement sans proxy ou avec un proxy transparent, exécutez la commande suivante dans le terminal :</span><span class="sxs-lookup"><span data-stu-id="35528-118">To test that a connection is not blocked in an environment without a proxy or with a transparent proxy, run the following command in the terminal:</span></span>

```bash
curl -w ' %{url_effective}\n' 'https://x.cp.wd.microsoft.com/api/report' 'https://cdn.x.cp.wd.microsoft.com/ping'
```

<span data-ttu-id="35528-119">La sortie de cette commande doit être similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="35528-119">The output from this command should be similar to:</span></span>

```Output
OK https://x.cp.wd.microsoft.com/api/report
OK https://cdn.x.cp.wd.microsoft.com/ping
```

## <a name="troubleshooting-steps-for-environments-with-static-proxy"></a><span data-ttu-id="35528-120">Étapes de résolution des problèmes pour les environnements avec proxy statique</span><span class="sxs-lookup"><span data-stu-id="35528-120">Troubleshooting steps for environments with static proxy</span></span>

> [!WARNING]
> <span data-ttu-id="35528-121">Pac, WPAD et les proxies authentifiés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="35528-121">PAC, WPAD, and authenticated proxies are not supported.</span></span> <span data-ttu-id="35528-122">Assurez-vous que seul un proxy statique ou transparent est utilisé.</span><span class="sxs-lookup"><span data-stu-id="35528-122">Ensure that only a static proxy or transparent proxy is being used.</span></span>
>
> <span data-ttu-id="35528-123">L’inspection et l’interception des proxies SSL ne sont pas non plus pris en charge pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="35528-123">SSL inspection and intercepting proxies are also not supported for security reasons.</span></span> <span data-ttu-id="35528-124">Configurez une exception pour l’inspection SSL et votre serveur proxy pour transmettre directement les données de Defender for Endpoint for Linux aux URL pertinentes sans interception.</span><span class="sxs-lookup"><span data-stu-id="35528-124">Configure an exception for SSL inspection and your proxy server to directly pass through data from Defender for Endpoint for Linux to the relevant URLs without interception.</span></span> <span data-ttu-id="35528-125">L’ajout de votre certificat d’interception au magasin global n’autorise pas l’interception.</span><span class="sxs-lookup"><span data-stu-id="35528-125">Adding your interception certificate to the global store will not allow for interception.</span></span>

<span data-ttu-id="35528-126">Si un proxy statique est requis, ajoutez un paramètre proxy à la commande ci-dessus, où correspond à l’adresse `proxy_address:port` proxy et au port :</span><span class="sxs-lookup"><span data-stu-id="35528-126">If a static proxy is required, add a proxy parameter to the above command, where `proxy_address:port` correspond to the proxy address and port:</span></span>

```bash
curl -x http://proxy_address:port -w ' %{url_effective}\n' 'https://x.cp.wd.microsoft.com/api/report' 'https://cdn.x.cp.wd.microsoft.com/ping'
```

<span data-ttu-id="35528-127">Veillez à utiliser les mêmes adresse et port proxy que celui configuré dans le `/lib/system/system/mdatp.service` fichier.</span><span class="sxs-lookup"><span data-stu-id="35528-127">Ensure that you use the same proxy address and port as configured in the `/lib/system/system/mdatp.service` file.</span></span> <span data-ttu-id="35528-128">Vérifiez la configuration de votre proxy en cas d’erreurs provenant des commandes ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="35528-128">Check your proxy configuration if there are errors from the above commands.</span></span>

> [!WARNING]
> <span data-ttu-id="35528-129">Le proxy statique ne peut pas être configuré via une variable d’environnement `HTTPS_PROXY` à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="35528-129">The static proxy cannot be configured through a system-wide `HTTPS_PROXY` environment variable.</span></span> <span data-ttu-id="35528-130">Au lieu de cela, `HTTPS_PROXY` assurez-vous qu’elle est correctement définie dans le `/lib/system/system/mdatp.service` fichier.</span><span class="sxs-lookup"><span data-stu-id="35528-130">Instead, ensure that `HTTPS_PROXY` is properly set in the `/lib/system/system/mdatp.service` file.</span></span>

<span data-ttu-id="35528-131">Pour utiliser un proxy statique, le `mdatp.service` fichier doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="35528-131">To use a static proxy, the `mdatp.service` file must be modified.</span></span> <span data-ttu-id="35528-132">Assurez-vous `#` que le début est supprimé pour supprimer lescommant de la ligne suivante `/lib/systemd/system/mdatp.service` :</span><span class="sxs-lookup"><span data-stu-id="35528-132">Ensure the leading `#` is removed to uncomment the following line from `/lib/systemd/system/mdatp.service`:</span></span>

```bash
#Environment="HTTPS_PROXY=http://address:port"
```

<span data-ttu-id="35528-133">Assurez-vous également que l’adresse proxy statique correcte est remplie pour remplacer `address:port` .</span><span class="sxs-lookup"><span data-stu-id="35528-133">Also ensure that the correct static proxy address is filled in to replace `address:port`.</span></span>

<span data-ttu-id="35528-134">Si ce fichier est correct, essayez d’exécutez la commande suivante dans le terminal pour recharger Defender pour endpoint pour Linux et propager le paramètre :</span><span class="sxs-lookup"><span data-stu-id="35528-134">If this file is correct, try running the following command in the terminal to reload Defender for Endpoint for Linux and propagate the setting:</span></span>

```bash
sudo systemctl daemon-reload; sudo systemctl restart mdatp
```

<span data-ttu-id="35528-135">En cas de réussite, tentez un autre test de connectivité à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="35528-135">Upon success, attempt another connectivity test from the command line:</span></span>

```bash
mdatp connectivity test
```

<span data-ttu-id="35528-136">Si le problème persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="35528-136">If the problem persists, contact customer support.</span></span>

## <a name="resources"></a><span data-ttu-id="35528-137">Ressources</span><span class="sxs-lookup"><span data-stu-id="35528-137">Resources</span></span>

- <span data-ttu-id="35528-138">Pour plus d’informations sur la configuration du produit afin qu’il utilise un proxy statique, voir [Configurer Microsoft Defender pour endpoint](linux-static-proxy-configuration.md)pour la découverte de proxy statique.</span><span class="sxs-lookup"><span data-stu-id="35528-138">For more information about how to configure the product to use a static proxy, see [Configure Microsoft Defender for Endpoint for static proxy discovery](linux-static-proxy-configuration.md).</span></span>
