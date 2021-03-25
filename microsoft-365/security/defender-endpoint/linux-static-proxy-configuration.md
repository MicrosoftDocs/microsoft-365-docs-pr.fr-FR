---
title: Microsoft Defender ATP pour la découverte de proxy statique Linux
ms.reviewer: ''
description: Décrit comment configurer Microsoft Defender ATP pour la découverte de proxy statique.
keywords: microsoft, defender, atp, linux, installation, proxy
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
ms.openlocfilehash: 461c728f6b61aa407d76e3674ba3339027c21a25
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187456"
---
# <a name="configure-microsoft-defender-for-endpoint-for-linux-for-static-proxy-discovery"></a><span data-ttu-id="3003e-104">Configurer Microsoft Defender pour endpoint pour Linux pour la découverte de proxy statique</span><span class="sxs-lookup"><span data-stu-id="3003e-104">Configure Microsoft Defender for Endpoint for Linux for static proxy discovery</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="3003e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3003e-105">**Applies to:**</span></span>
- [<span data-ttu-id="3003e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3003e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3003e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3003e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3003e-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3003e-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="3003e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3003e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="3003e-110">Microsoft Defender ATP peut découvrir un serveur proxy à l’aide de la ```HTTPS_PROXY``` variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="3003e-110">Microsoft Defender ATP can discover a proxy server using the ```HTTPS_PROXY``` environment variable.</span></span> <span data-ttu-id="3003e-111">Ce paramètre doit être configuré **à** la fois au moment de l’installation et après l’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="3003e-111">This setting must be configured **both** at installation time and after the product has been installed.</span></span>

## <a name="installation-time-configuration"></a><span data-ttu-id="3003e-112">Configuration de l’heure d’installation</span><span class="sxs-lookup"><span data-stu-id="3003e-112">Installation time configuration</span></span>

<span data-ttu-id="3003e-113">Lors de l’installation, ```HTTPS_PROXY``` la variable d’environnement doit être transmise au gestionnaire de package.</span><span class="sxs-lookup"><span data-stu-id="3003e-113">During installation, the ```HTTPS_PROXY``` environment variable must be passed to the package manager.</span></span> <span data-ttu-id="3003e-114">Le gestionnaire de package peut lire cette variable de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="3003e-114">The package manager can read this variable in any of the following ways:</span></span>

- <span data-ttu-id="3003e-115">La ```HTTPS_PROXY``` variable est définie avec la ligne suivante ```/etc/environment``` :</span><span class="sxs-lookup"><span data-stu-id="3003e-115">The ```HTTPS_PROXY``` variable is defined in ```/etc/environment``` with the following line:</span></span>

    ```bash
    HTTPS_PROXY="http://proxy.server:port/"
    ```

- <span data-ttu-id="3003e-116">La `HTTPS_PROXY` variable est définie dans la configuration globale du gestionnaire de packages.</span><span class="sxs-lookup"><span data-stu-id="3003e-116">The `HTTPS_PROXY` variable is defined in the package manager global configuration.</span></span> <span data-ttu-id="3003e-117">Par exemple, dans Ubuntu 18.04, vous pouvez ajouter la ligne suivante à `/etc/apt/apt.conf.d/proxy.conf` :</span><span class="sxs-lookup"><span data-stu-id="3003e-117">For example, in Ubuntu 18.04, you can add the following line to `/etc/apt/apt.conf.d/proxy.conf`:</span></span>
  
    ```bash
    Acquire::https::Proxy "http://proxy.server:port/";
    ```

    > [!CAUTION]
    > <span data-ttu-id="3003e-118">Notez que deux méthodes ci-dessus peuvent définir le proxy à utiliser pour d’autres applications sur votre système.</span><span class="sxs-lookup"><span data-stu-id="3003e-118">Note that above two methods could define the proxy to use for other applications on your system.</span></span> <span data-ttu-id="3003e-119">Utilisez cette méthode avec précaution, ou uniquement s’il s’agit d’une configuration globale.</span><span class="sxs-lookup"><span data-stu-id="3003e-119">Use this method with caution, or only if this is meant to be a generally global configuration.</span></span>
  
- <span data-ttu-id="3003e-120">La variable est précédée des commandes `HTTPS_PROXY` d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="3003e-120">The `HTTPS_PROXY` variable is prepended to the installation or uninstallation commands.</span></span> <span data-ttu-id="3003e-121">Par exemple, avec le gestionnaire de package APT, prédépender la variable comme suit lors de l’installation de Microsoft Defender pour Endpoint :</span><span class="sxs-lookup"><span data-stu-id="3003e-121">For example, with the APT package manager, prepend the variable as follows when installing Microsoft Defender for Endpoint:</span></span> 

    ```bash  
    HTTPS_PROXY="http://proxy.server:port/" apt install mdatp
    ```

    > [!NOTE]
    > <span data-ttu-id="3003e-122">N’ajoutez pas de sudo entre la définition de variable d’environnement et apt, sinon la variable ne sera pas propagée.</span><span class="sxs-lookup"><span data-stu-id="3003e-122">Do not add sudo between the environment variable definition and apt, otherwise the variable will not be propagated.</span></span>

<span data-ttu-id="3003e-123">La `HTTPS_PROXY` variable d’environnement peut être définie de la même manière lors de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="3003e-123">The `HTTPS_PROXY` environment variable may similarly be defined during uninstallation.</span></span>

<span data-ttu-id="3003e-124">Notez que l’installation et la désinstallation ne échouent pas nécessairement si un proxy est requis mais non configuré.</span><span class="sxs-lookup"><span data-stu-id="3003e-124">Note that installation and uninstallation will not necessarily fail if a proxy is required but not configured.</span></span> <span data-ttu-id="3003e-125">Toutefois, la télémétrie n’est pas envoyée et l’opération peut prendre beaucoup plus de temps en raison de délai d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="3003e-125">However, telemetry will not be submitted, and the operation could take much longer due to network timeouts.</span></span>

## <a name="post-installation-configuration"></a><span data-ttu-id="3003e-126">Configuration post-installation</span><span class="sxs-lookup"><span data-stu-id="3003e-126">Post installation configuration</span></span>
  
<span data-ttu-id="3003e-127">Après l’installation, `HTTPS_PROXY` la variable d’environnement doit être définie dans le fichier de service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="3003e-127">After installation, the `HTTPS_PROXY` environment variable must be defined in the Defender for Endpoint service file.</span></span> <span data-ttu-id="3003e-128">Pour ce faire, ouvrez dans `/lib/systemd/system/mdatp.service` un éditeur de texte lors de l’exécution en tant qu’utilisateur racine.</span><span class="sxs-lookup"><span data-stu-id="3003e-128">To do this, open `/lib/systemd/system/mdatp.service` in a text editor while running as the root user.</span></span> <span data-ttu-id="3003e-129">Vous pouvez ensuite propager la variable au service de deux manières :</span><span class="sxs-lookup"><span data-stu-id="3003e-129">You can then propagate the variable to the service in one of two ways:</span></span>

- <span data-ttu-id="3003e-130">Décompressez la ligne `#Environment="HTTPS_PROXY=http://address:port"` et spécifiez votre adresse proxy statique.</span><span class="sxs-lookup"><span data-stu-id="3003e-130">Uncomment the line `#Environment="HTTPS_PROXY=http://address:port"` and specify your static proxy address.</span></span>

- <span data-ttu-id="3003e-131">Ajoutez une ligne `EnvironmentFile=/path/to/env/file` .</span><span class="sxs-lookup"><span data-stu-id="3003e-131">Add a line `EnvironmentFile=/path/to/env/file`.</span></span> <span data-ttu-id="3003e-132">Ce chemin d’accès peut pointer vers ou un fichier personnalisé, lequel doit `/etc/environment` ajouter la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="3003e-132">This path can point to `/etc/environment` or a custom file, either of which needs to add the following line:</span></span>
  
    ```bash
    HTTPS_PROXY="http://proxy.server:port/"
    ```

<span data-ttu-id="3003e-133">Après avoir modifié le `mdatp.service` fichier, enregistrez-le et fermez-le.</span><span class="sxs-lookup"><span data-stu-id="3003e-133">After modifying the `mdatp.service` file, save and close it.</span></span> <span data-ttu-id="3003e-134">Redémarrez le service afin que les modifications soient appliquées.</span><span class="sxs-lookup"><span data-stu-id="3003e-134">Restart the service so the changes can be applied.</span></span> <span data-ttu-id="3003e-135">Dans Ubuntu, cela implique deux commandes :</span><span class="sxs-lookup"><span data-stu-id="3003e-135">In Ubuntu, this involves two commands:</span></span>  

```bash
systemctl daemon-reload; systemctl restart mdatp
```
