---
title: Exemples de stratégies de contrôle d’appareil pour JAMF
description: Découvrez comment utiliser des stratégies de contrôle d’appareil à l’aide d’exemples qui peuvent être utilisés avec JAMF.
keywords: microsoft, defender, point de terminaison, atp, mac, appareil, contrôle, usb, amovible, média, jamf
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: security
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
ms.openlocfilehash: 8990979024c033d4142b595d6fef94f7b872e7c9
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187678"
---
# <a name="examples-of-device-control-policies-for-jamf"></a><span data-ttu-id="041a3-104">Exemples de stratégies de contrôle d’appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="041a3-104">Examples of device control policies for JAMF</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="041a3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="041a3-105">**Applies to:**</span></span>
- [<span data-ttu-id="041a3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="041a3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="041a3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="041a3-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="041a3-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="041a3-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="041a3-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="041a3-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="041a3-110">Ce document contient des exemples de stratégies de contrôle d’appareil que vous pouvez personnaliser pour votre propre organisation.</span><span class="sxs-lookup"><span data-stu-id="041a3-110">This document contains examples of device control policies that you can customize for your own organization.</span></span> <span data-ttu-id="041a3-111">Ces exemples s’appliquent si vous utilisez JAMF pour gérer les appareils de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="041a3-111">These examples are applicable if you are using JAMF to manage devices in your enterprise.</span></span>

## <a name="restrict-access-to-all-removable-media"></a><span data-ttu-id="041a3-112">Restreindre l’accès à tous les médias amovibles</span><span class="sxs-lookup"><span data-stu-id="041a3-112">Restrict access to all removable media</span></span>

<span data-ttu-id="041a3-113">L’exemple suivant limite l’accès à tous les médias amovibles.</span><span class="sxs-lookup"><span data-stu-id="041a3-113">The following example restricts access to all removable media.</span></span> <span data-ttu-id="041a3-114">Notez l’autorisation qui est appliquée au niveau supérieur de la stratégie, ce qui signifie que toutes les opérations `none` sur les fichiers seront interdites.</span><span class="sxs-lookup"><span data-stu-id="041a3-114">Note the `none` permission that is applied at the top level of the policy, meaning that all file operations will be prohibited.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"> 
<plist version="1.0"> 
<dict> 
    <key>deviceControl</key> 
    <dict> 
        <key>removableMediaPolicy</key> 
        <dict> 
            <key>enforcementLevel</key> 
            <string>block</string> 
            <key>permission</key> 
            <array> 
                <string>none</string> 
            </array> 
        </dict> 
    </dict> 
</dict> 
</plist>
```

## <a name="set-all-removable-media-to-be-read-only"></a><span data-ttu-id="041a3-115">Définir tous les médias amovibles en lecture seule</span><span class="sxs-lookup"><span data-stu-id="041a3-115">Set all removable media to be read-only</span></span>

<span data-ttu-id="041a3-116">L’exemple suivant configure tous les médias amovibles en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="041a3-116">The following example configures all removable media to be read-only.</span></span> <span data-ttu-id="041a3-117">Notez l’autorisation qui est appliquée au niveau supérieur de la stratégie, ce qui signifie que toutes les opérations d’écriture et `read` d’exécution seront non autorisées.</span><span class="sxs-lookup"><span data-stu-id="041a3-117">Note the `read` permission that is applied at the top level of the policy, meaning that all write and execute operations will be disallowed.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"> 
<plist version="1.0"> 
<dict> 
    <key>deviceControl</key> 
    <dict> 
        <key>removableMediaPolicy</key> 
        <dict> 
            <key>enforcementLevel</key> 
            <string>block</string> 
            <key>permission</key> 
            <array> 
                <string>read</string> 
            </array> 
        </dict> 
    </dict> 
</dict> 
</plist>
```

## <a name="disallow-program-execution-from-removable-media"></a><span data-ttu-id="041a3-118">Ne pas exécuter le programme à partir d’un média amovible</span><span class="sxs-lookup"><span data-stu-id="041a3-118">Disallow program execution from removable media</span></span>

<span data-ttu-id="041a3-119">L’exemple suivant montre comment l’exécution d’un programme à partir d’un média amovible peut être rejetée.</span><span class="sxs-lookup"><span data-stu-id="041a3-119">The following example shows how program execution from removable media can be disallowed.</span></span> <span data-ttu-id="041a3-120">Notez `read` les `write` autorisations qui sont appliquées au niveau supérieur de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="041a3-120">Note the `read` and `write` permissions that are applied at the top level of the policy.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"> 
<plist version="1.0"> 
<dict> 
    <key>deviceControl</key> 
    <dict> 
        <key>removableMediaPolicy</key> 
        <dict> 
            <key>enforcementLevel</key> 
            <string>block</string> 
            <key>permission</key> 
            <array> 
                <string>read</string>
                <string>write</string> 
            </array> 
        </dict> 
    </dict> 
</dict> 
</plist>
```

## <a name="restrict-all-devices-from-specific-vendors"></a><span data-ttu-id="041a3-121">Restreindre tous les appareils de fournisseurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="041a3-121">Restrict all devices from specific vendors</span></span>

<span data-ttu-id="041a3-122">L’exemple suivant limite tous les appareils de fournisseurs spécifiques (dans ce cas identifiés par `fff0` et `4525` ).</span><span class="sxs-lookup"><span data-stu-id="041a3-122">The following example restricts all devices from specific vendors (in this case identified by `fff0` and `4525`).</span></span> <span data-ttu-id="041a3-123">Tous les autres appareils seront illimités, car l’autorisation définie au niveau supérieur de la stratégie répertorie toutes les autorisations possibles (lecture, écriture et exécution).</span><span class="sxs-lookup"><span data-stu-id="041a3-123">All other devices will be unrestricted, since the permission defined at the top level of the policy lists all possible permissions (read, write, and execute).</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"> 
<plist version="1.0"> 
<dict> 
    <key>deviceControl</key> 
    <dict> 
        <key>removableMediaPolicy</key> 
        <dict> 
            <key>enforcementLevel</key> 
            <string>block</string> 
            <key>permission</key> 
            <array> 
                <string>read</string>
                <string>write</string>
                <string>execute</string> 
            </array> 
            <key>vendors</key> 
            <dict> 
                <key>fff0</key> 
                <dict> 
                    <key>permission</key> 
                    <array> 
                        <string>none</string> 
                    </array> 
                </dict> 
                <key>4525</key> 
                <dict> 
                    <key>permission</key> 
                    <array>                         
                        <string>none</string> 
                    </array> 
                </dict> 
            </dict> 
        </dict> 
    </dict> 
</dict> 
</plist> 
```

## <a name="restrict-specific-devices-identified-by-vendor-id-product-id-and-serial-number"></a><span data-ttu-id="041a3-124">Restreindre des appareils spécifiques identifiés par l’ID du fournisseur, l’ID de produit et le numéro de série</span><span class="sxs-lookup"><span data-stu-id="041a3-124">Restrict specific devices identified by vendor ID, product ID, and serial number</span></span>

<span data-ttu-id="041a3-125">L’exemple suivant limite deux appareils spécifiques, identifiés par l’ID du fournisseur, l’ID de produit `fff0` et les numéros de série et `1000` `04ZSSMHI2O7WBVOA` `04ZSSMHI2O7WBVOB` .</span><span class="sxs-lookup"><span data-stu-id="041a3-125">The following example restricts two specific devices, identified by vendor ID `fff0`, product ID `1000`, and serial numbers `04ZSSMHI2O7WBVOA` and `04ZSSMHI2O7WBVOB`.</span></span> <span data-ttu-id="041a3-126">À tous les autres niveaux de la stratégie, les autorisations incluent toutes les valeurs possibles (lecture, écriture et exécution), ce qui signifie que tous les autres appareils seront illimités.</span><span class="sxs-lookup"><span data-stu-id="041a3-126">At all other levels of the policy the permissions include all possible values (read, write, and execute), meaning that all other devices will be unrestricted.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"> 
<plist version="1.0"> 
<dict> 
    <key>deviceControl</key> 
    <dict> 
        <key>removableMediaPolicy</key> 
        <dict> 
            <key>enforcementLevel</key> 
            <string>block</string> 
            <key>permission</key> 
            <array> 
                <string>read</string>
                <string>write</string>
                <string>execute</string>
            </array> 
            <key>vendors</key> 
            <dict> 
                <key>fff0</key> 
                <dict> 
                    <key>permission</key> 
                    <array> 
                        <string>read</string> 
                        <string>write</string>
                        <string>execute</string> 
                    </array> 
                    <key>products</key> 
                    <dict> 
                        <key>1000</key> 
                        <dict> 
                            <key>permission</key> 
                            <array> 
                                <string>read</string> 
                                <string>write</string>
                                <string>execute</string>
                            </array> 
                            <key>serialNumbers</key> 
                            <dict> 
                                <key>04ZSSMHI2O7WBVOA</key> 
                                <array> 
                                  <string>none</string> 
                                </array> 
                                <key>04ZSSMHI2O7WBVOB</key>
                                <array> 
                                  <string>none</string> 
                                </array> 
                            </dict> 
                        </dict> 
                    </dict> 
                </dict>
            </dict> 
        </dict> 
    </dict> 
</dict> 
</plist> 
```

## <a name="related-topics"></a><span data-ttu-id="041a3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="041a3-127">Related topics</span></span>

- [<span data-ttu-id="041a3-128">Vue d’ensemble du contrôle d’appareil pour macOS</span><span class="sxs-lookup"><span data-stu-id="041a3-128">Overview of device control for macOS</span></span>](mac-device-control-overview.md)
