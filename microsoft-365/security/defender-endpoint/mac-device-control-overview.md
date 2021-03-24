---
title: Contrôle d’appareil pour macOS
description: Découvrez comment configurer Microsoft Defender pour endpoint pour Mac afin de réduire les menaces liées au stockage amovible tel que les périphériques USB.
keywords: microsoft, defender, atp, mac, appareil, contrôle, usb, amovible, média
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
ms.openlocfilehash: f2429002a10fd2d033530d75f261ffd04459c64f
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062406"
---
# <a name="device-control-for-macos"></a><span data-ttu-id="02b3d-104">Contrôle d’appareil pour macOS</span><span class="sxs-lookup"><span data-stu-id="02b3d-104">Device control for macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="02b3d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="02b3d-105">**Applies to:**</span></span>
- [<span data-ttu-id="02b3d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="02b3d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="02b3d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="02b3d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="02b3d-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="02b3d-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="02b3d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="02b3d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="requirements"></a><span data-ttu-id="02b3d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02b3d-110">Requirements</span></span>

<span data-ttu-id="02b3d-111">Le contrôle d’appareil pour macOS présente les conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="02b3d-111">Device control for macOS has the following prerequisites:</span></span>

>[!div class="checklist"]
> - <span data-ttu-id="02b3d-112">Droit au point de terminaison Microsoft Defender (peut être une version d’évaluation)</span><span class="sxs-lookup"><span data-stu-id="02b3d-112">Microsoft Defender for Endpoint entitlement (can be trial)</span></span>
> - <span data-ttu-id="02b3d-113">Version minimale du système d’exploitation : macOS 10.15.4 ou version supérieure</span><span class="sxs-lookup"><span data-stu-id="02b3d-113">Minimum OS version: macOS 10.15.4 or higher</span></span>
> - <span data-ttu-id="02b3d-114">Version minimale du produit : 101.24.59</span><span class="sxs-lookup"><span data-stu-id="02b3d-114">Minimum product version: 101.24.59</span></span>
> - <span data-ttu-id="02b3d-115">Votre appareil doit être en cours d’exécution avec des extensions système (il s’agit de la valeur par défaut sur macOS 11 Big Sur).</span><span class="sxs-lookup"><span data-stu-id="02b3d-115">Your device must be running with system extensions (this is the default on macOS 11 Big Sur).</span></span> 
> 
>   <span data-ttu-id="02b3d-116">Vous pouvez vérifier si votre appareil s’exécute sur des extensions système en exécutant la commande suivante et vérifier qu’il est en cours d’impression `endpoint_security_extension` sur la console :</span><span class="sxs-lookup"><span data-stu-id="02b3d-116">You can check if your device is running on system extensions by running the following command and verify that it is printing `endpoint_security_extension` to the console:</span></span> 
> 
>   ```bash
>   mdatp health --field real_time_protection_subsystem 
>   ```
> - <span data-ttu-id="02b3d-117">Votre appareil doit se trouver dans (précédemment appelé) canal de mise à jour de mise à jour `Beta` `InsiderFast` automatique Microsoft AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="02b3d-117">Your device must be in `Beta` (previously called `InsiderFast`) Microsoft AutoUpdate update channel.</span></span> <span data-ttu-id="02b3d-118">Pour plus d’informations, voir [Déployer les mises à jour de Microsoft Defender pour Endpoint pour Mac.](mac-updates.md)</span><span class="sxs-lookup"><span data-stu-id="02b3d-118">For more information, see [Deploy updates for Microsoft Defender for Endpoint for Mac](mac-updates.md).</span></span>
> 
>   <span data-ttu-id="02b3d-119">Vous pouvez vérifier le canal de mise à jour à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="02b3d-119">You can check the update channel using the following command:</span></span> 
> 
>    ```bash
>    mdatp health --field release_ring 
>    ```
>
>    <span data-ttu-id="02b3d-120">Si la commande ci-dessus n’imprime pas l’une ou l’autre des commandes `Beta` `InsiderFast` ci-dessus, exécutez la commande suivante à partir du Terminal.</span><span class="sxs-lookup"><span data-stu-id="02b3d-120">If the above command does not print either `Beta` or `InsiderFast`, execute the following command from the Terminal.</span></span> <span data-ttu-id="02b3d-121">La mise à jour du canal prend effet lors du prochain démarrage du produit (lors de l’installation de la prochaine mise à jour du produit ou du redémarrage de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="02b3d-121">The channel update takes effect next time the product starts (when the next product update is installed or when the device is rebooted).</span></span> 
> 
>    ```bash
>    defaults write com.microsoft.autoupdate2 ChannelName -string Beta
>    ```
>
>    <span data-ttu-id="02b3d-122">Par ailleurs, si vous êtes dans un environnement géré (JAMF ou Intune), vous pouvez configurer le canal de mise à jour à distance.</span><span class="sxs-lookup"><span data-stu-id="02b3d-122">Alternatively, if you are in a managed environment (JAMF or Intune), you can configure the update channel remotely.</span></span> <span data-ttu-id="02b3d-123">Pour plus d’informations, voir [Déployer les mises à jour de Microsoft Defender pour Endpoint pour Mac.](mac-updates.md)</span><span class="sxs-lookup"><span data-stu-id="02b3d-123">For more information, see [Deploy updates for Microsoft Defender for Endpoint for Mac](mac-updates.md).</span></span> 

## <a name="device-control-policy"></a><span data-ttu-id="02b3d-124">Stratégie de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-124">Device control policy</span></span>

<span data-ttu-id="02b3d-125">Pour configurer le contrôle d’appareil pour macOS, vous devez créer une stratégie qui décrit les restrictions que vous souhaitez mettre en place au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02b3d-125">To configure device control for macOS, you must create a policy that describes the restrictions you want to put in place within your organization.</span></span>

<span data-ttu-id="02b3d-126">La stratégie de contrôle d’appareil est incluse dans le profil de configuration utilisé pour configurer tous les autres paramètres du produit.</span><span class="sxs-lookup"><span data-stu-id="02b3d-126">The device control policy is included in the configuration profile used to configure all other product settings.</span></span> <span data-ttu-id="02b3d-127">Pour plus d’informations, voir [Structure de profil de configuration.](mac-preferences.md#configuration-profile-structure)</span><span class="sxs-lookup"><span data-stu-id="02b3d-127">For more information, see [Configuration profile structure](mac-preferences.md#configuration-profile-structure).</span></span>

<span data-ttu-id="02b3d-128">Dans le profil de configuration, la stratégie de contrôle d’appareil est définie dans la section suivante :</span><span class="sxs-lookup"><span data-stu-id="02b3d-128">Within the configuration profile, the device control policy is defined in the following section:</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-129">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-129">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-130">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-130">**Key**</span></span> | <span data-ttu-id="02b3d-131">deviceControl</span><span class="sxs-lookup"><span data-stu-id="02b3d-131">deviceControl</span></span> |
| <span data-ttu-id="02b3d-132">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-132">**Data type**</span></span> | <span data-ttu-id="02b3d-133">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="02b3d-133">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="02b3d-134">**Comments**</span><span class="sxs-lookup"><span data-stu-id="02b3d-134">**Comments**</span></span> | <span data-ttu-id="02b3d-135">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="02b3d-135">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="02b3d-136">La stratégie de contrôle d’appareil peut être utilisée pour :</span><span class="sxs-lookup"><span data-stu-id="02b3d-136">The device control policy can be used to:</span></span>

- [<span data-ttu-id="02b3d-137">Personnaliser la cible d’URL pour les notifications dues au contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-137">Customize the URL target for notifications raised by device control</span></span>](#customize-url-target-for-notifications-raised-by-device-control)
- [<span data-ttu-id="02b3d-138">Autoriser ou bloquer les appareils amovibles</span><span class="sxs-lookup"><span data-stu-id="02b3d-138">Allow or block removable devices</span></span>](#allow-or-block-removable-devices)

### <a name="customize-url-target-for-notifications-raised-by-device-control"></a><span data-ttu-id="02b3d-139">Personnaliser la cible d’URL pour les notifications du contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-139">Customize URL target for notifications raised by device control</span></span>

<span data-ttu-id="02b3d-140">Lorsque la stratégie de contrôle d’appareil que vous avez mise en place est appliquée sur un appareil (par exemple, l’accès à un périphérique multimédia amovible est restreint), une notification s’affiche pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02b3d-140">When the device control policy that you have put in place is enforced on a device (for example, access to a removable media device is restricted), a notification is displayed to the user.</span></span>

![Notification de contrôle d’appareil](images/mac-device-control-notification.png)

<span data-ttu-id="02b3d-142">Lorsque les utilisateurs finaux cliquent sur cette notification, une page web s’ouvre dans le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="02b3d-142">When end users click this notification, a web page is opened in the default browser.</span></span> <span data-ttu-id="02b3d-143">Vous pouvez configurer l’URL qui est ouverte lorsque les utilisateurs finaux cliquent sur la notification.</span><span class="sxs-lookup"><span data-stu-id="02b3d-143">You can configure the URL that is opened when end users click the notification.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-144">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-144">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-145">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-145">**Key**</span></span> | <span data-ttu-id="02b3d-146">navigationTarget</span><span class="sxs-lookup"><span data-stu-id="02b3d-146">navigationTarget</span></span> |
| <span data-ttu-id="02b3d-147">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-147">**Data type**</span></span> | <span data-ttu-id="02b3d-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02b3d-148">String</span></span> |
| <span data-ttu-id="02b3d-149">**Comments**</span><span class="sxs-lookup"><span data-stu-id="02b3d-149">**Comments**</span></span> | <span data-ttu-id="02b3d-150">S’il n’est pas défini, le produit utilise une URL par défaut pointant vers une page générique expliquant l’action entreprise par le produit.</span><span class="sxs-lookup"><span data-stu-id="02b3d-150">If not defined, the product uses a default URL pointing to a generic page explaining the action taken by the product.</span></span> |

### <a name="allow-or-block-removable-devices"></a><span data-ttu-id="02b3d-151">Autoriser ou bloquer les appareils amovibles</span><span class="sxs-lookup"><span data-stu-id="02b3d-151">Allow or block removable devices</span></span>

<span data-ttu-id="02b3d-152">La section média amovible de la stratégie de contrôle d’appareil est utilisée pour restreindre l’accès aux médias amovibles.</span><span class="sxs-lookup"><span data-stu-id="02b3d-152">The removable media section of the device control policy is used to restrict access to removable media.</span></span> 

> [!NOTE]
> <span data-ttu-id="02b3d-153">Les types de média amovible suivants sont actuellement pris en charge et peuvent être inclus dans la stratégie : les périphériques de stockage USB.</span><span class="sxs-lookup"><span data-stu-id="02b3d-153">The following types of removable media are currently supported and can be included in the policy: USB storage devices.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-154">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-154">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-155">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-155">**Key**</span></span> | <span data-ttu-id="02b3d-156">removableMediaPolicy</span><span class="sxs-lookup"><span data-stu-id="02b3d-156">removableMediaPolicy</span></span> |
| <span data-ttu-id="02b3d-157">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-157">**Data type**</span></span> | <span data-ttu-id="02b3d-158">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="02b3d-158">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="02b3d-159">**Comments**</span><span class="sxs-lookup"><span data-stu-id="02b3d-159">**Comments**</span></span> | <span data-ttu-id="02b3d-160">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="02b3d-160">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="02b3d-161">Cette section de la stratégie est hiérarchique, ce qui permet une flexibilité maximale et couvre un large éventail de cas d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="02b3d-161">This section of the policy is hierarchical, allowing for maximum flexibility and covering a wide range of use cases.</span></span> <span data-ttu-id="02b3d-162">Au niveau supérieur, les fournisseurs sont identifiés par un ID de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02b3d-162">At the top level are vendors, identified by a vendor ID.</span></span> <span data-ttu-id="02b3d-163">Pour chaque fournisseur, il existe des produits, identifiés par un ID de produit.</span><span class="sxs-lookup"><span data-stu-id="02b3d-163">For each vendor, there are products, identified by a product ID.</span></span> <span data-ttu-id="02b3d-164">Enfin, pour chaque produit, il existe des numéros de série qui notent des appareils spécifiques.</span><span class="sxs-lookup"><span data-stu-id="02b3d-164">Finally, for each product there are serial numbers denoting specific devices.</span></span>

```
|-- policy top level 
    |-- vendor 1 
        |-- product 1 
            |-- serial number 1 
            ...
            |-- serial number N 
        ...
        |-- product N 
    ...
    |-- vendor N
```

<span data-ttu-id="02b3d-165">Pour plus d’informations sur la recherche des identificateurs d’appareil, voir [Rechercher des identificateurs d’appareil.](#look-up-device-identifiers)</span><span class="sxs-lookup"><span data-stu-id="02b3d-165">For information on how to find the device identifiers, see [Look up device identifiers](#look-up-device-identifiers).</span></span>

<span data-ttu-id="02b3d-166">La stratégie est évaluée de l’entrée la plus spécifique à la plus générale.</span><span class="sxs-lookup"><span data-stu-id="02b3d-166">The policy is evaluated from the most specific entry to the most general one.</span></span> <span data-ttu-id="02b3d-167">Autrement dit, lorsqu’un appareil est branché, le produit tente de trouver la correspondance la plus spécifique dans la stratégie pour chaque périphérique multimédia amovible et applique les autorisations à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="02b3d-167">Meaning, when a device is plugged in, the product tries to find the most specific match in the policy for each removable media device and apply the permissions at that level.</span></span> <span data-ttu-id="02b3d-168">En l’absence de correspondance, la meilleure correspondance suivante est appliquée, jusqu’à l’autorisation spécifiée au niveau supérieur, qui est la valeur par défaut lorsqu’un appareil ne correspond à aucune autre entrée de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="02b3d-168">If there is no match, then the next best match is applied, all the way to the permission specified at the top level, which is the default when a device does not match any other entry in the policy.</span></span>

#### <a name="policy-enforcement-level"></a><span data-ttu-id="02b3d-169">Niveau d’application de la stratégie</span><span class="sxs-lookup"><span data-stu-id="02b3d-169">Policy enforcement level</span></span>

<span data-ttu-id="02b3d-170">Sous la section Média amovible, il existe une option pour définir le niveau d’application, qui peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="02b3d-170">Under the removable media section, there is an option to set the enforcement level, which can take one of the following values:</span></span>

- <span data-ttu-id="02b3d-171">`audit` - Sous ce niveau d’application, si l’accès à un appareil est restreint, une notification s’affiche pour l’utilisateur, mais l’appareil peut toujours être utilisé.</span><span class="sxs-lookup"><span data-stu-id="02b3d-171">`audit` - Under this enforcement level, if access to a device is restricted, a notification is displayed to the user, however the device can still be used.</span></span> <span data-ttu-id="02b3d-172">Ce niveau d’application peut être utile pour évaluer l’efficacité d’une stratégie.</span><span class="sxs-lookup"><span data-stu-id="02b3d-172">This enforcement level can be useful to evaluate the effectiveness of a policy.</span></span>
- <span data-ttu-id="02b3d-173">`block` - Sous ce niveau d’application, les opérations que l’utilisateur peut effectuer sur l’appareil sont limitées à ce qui est défini dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="02b3d-173">`block` - Under this enforcement level, the operations that the user can perform on the device are limited to what is defined in the policy.</span></span> <span data-ttu-id="02b3d-174">En outre, une notification est alors avertie à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02b3d-174">Furthermore, a notification is raised to the user.</span></span> 

|||
|:---|:---|
| <span data-ttu-id="02b3d-175">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-175">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-176">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-176">**Key**</span></span> | <span data-ttu-id="02b3d-177">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="02b3d-177">enforcementLevel</span></span> |
| <span data-ttu-id="02b3d-178">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-178">**Data type**</span></span> | <span data-ttu-id="02b3d-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="02b3d-179">String</span></span> |
| <span data-ttu-id="02b3d-180">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="02b3d-180">**Possible values**</span></span> | <span data-ttu-id="02b3d-181">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="02b3d-181">audit (default)</span></span> <br/> <span data-ttu-id="02b3d-182">block</span><span class="sxs-lookup"><span data-stu-id="02b3d-182">block</span></span> |

#### <a name="default-permission-level"></a><span data-ttu-id="02b3d-183">Niveau d’autorisation par défaut</span><span class="sxs-lookup"><span data-stu-id="02b3d-183">Default permission level</span></span>

<span data-ttu-id="02b3d-184">Au niveau supérieur de la section média amovible, vous pouvez configurer le niveau d’autorisation par défaut pour les appareils qui ne correspondent à rien d’autre dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="02b3d-184">At the top level of the removable media section, you can configure the default permission level for devices that do not match anything else in the policy.</span></span>

<span data-ttu-id="02b3d-185">Ce paramètre peut être définie sur :</span><span class="sxs-lookup"><span data-stu-id="02b3d-185">This setting can be set to:</span></span>

- <span data-ttu-id="02b3d-186">`none` - Aucune opération ne peut être effectuée sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-186">`none` - No operations can be performed on the device</span></span>
- <span data-ttu-id="02b3d-187">Combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="02b3d-187">A combination of the following values:</span></span>
    - <span data-ttu-id="02b3d-188">`read` - Les opérations de lecture sont autorisées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-188">`read` - Read operations are permitted on the device</span></span>
    - <span data-ttu-id="02b3d-189">`write` - Les opérations d’écriture sont autorisées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-189">`write` - Write operations are permitted on the device</span></span>
    - <span data-ttu-id="02b3d-190">`execute` - Les opérations d’exécution sont autorisées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-190">`execute` - Execute operations are permitted on the device</span></span>

> [!NOTE]
> <span data-ttu-id="02b3d-191">`none`S’il est présent dans le niveau d’autorisation, toutes les autres autorisations ( ou ) sont `read` `write` `execute` ignorées.</span><span class="sxs-lookup"><span data-stu-id="02b3d-191">If `none` is present in the permission level, any other permissions (`read`, `write`, or `execute`) will be ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="02b3d-192">L’autorisation fait uniquement référence à l’exécution des binaires `execute` Mach-O.</span><span class="sxs-lookup"><span data-stu-id="02b3d-192">The `execute` permission only refers to execution of Mach-O binaries.</span></span> <span data-ttu-id="02b3d-193">Il n’inclut pas l’exécution de scripts ou d’autres types de charges utiles.</span><span class="sxs-lookup"><span data-stu-id="02b3d-193">It does not include execution of scripts or other types of payloads.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-194">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-194">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-195">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-195">**Key**</span></span> | <span data-ttu-id="02b3d-196">autorisation</span><span class="sxs-lookup"><span data-stu-id="02b3d-196">permission</span></span> |
| <span data-ttu-id="02b3d-197">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-197">**Data type**</span></span> | <span data-ttu-id="02b3d-198">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02b3d-198">Array of strings</span></span> |
| <span data-ttu-id="02b3d-199">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="02b3d-199">**Possible values**</span></span> | <span data-ttu-id="02b3d-200">aucune</span><span class="sxs-lookup"><span data-stu-id="02b3d-200">none</span></span> <br/> <span data-ttu-id="02b3d-201">read</span><span class="sxs-lookup"><span data-stu-id="02b3d-201">read</span></span> <br/> <span data-ttu-id="02b3d-202">write</span><span class="sxs-lookup"><span data-stu-id="02b3d-202">write</span></span> <br/> <span data-ttu-id="02b3d-203">execute</span><span class="sxs-lookup"><span data-stu-id="02b3d-203">execute</span></span> |

#### <a name="restrict-removable-media-by-vendor-product-and-serial-number"></a><span data-ttu-id="02b3d-204">Restreindre les médias amovibles par fournisseur, produit et numéro de série</span><span class="sxs-lookup"><span data-stu-id="02b3d-204">Restrict removable media by vendor, product, and serial number</span></span>

<span data-ttu-id="02b3d-205">Comme décrit dans [Autoriser](#allow-or-block-removable-devices)ou bloquer les appareils amovibles, les supports amovibles tels que les périphériques USB peuvent être identifiés par l’ID du fournisseur, l’ID de produit et le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="02b3d-205">As described in [Allow or block removable devices](#allow-or-block-removable-devices), removable media such as USB devices can be identified by the vendor ID, product ID, and serial number.</span></span>

<span data-ttu-id="02b3d-206">Au niveau supérieur de la stratégie de média amovible, vous pouvez éventuellement définir des restrictions plus précises au niveau du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02b3d-206">At the top level of the removable media policy, you can optionally define more granular restrictions at the vendor level.</span></span> 

<span data-ttu-id="02b3d-207">Le dictionnaire contient une ou plusieurs entrées, chaque entrée étant `vendors` identifiée par l’ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02b3d-207">The `vendors` dictionary contains one or more entries, with each entry being identified by the vendor ID.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-208">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-208">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-209">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-209">**Key**</span></span> | <span data-ttu-id="02b3d-210">fournisseurs</span><span class="sxs-lookup"><span data-stu-id="02b3d-210">vendors</span></span> |
| <span data-ttu-id="02b3d-211">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-211">**Data type**</span></span> | <span data-ttu-id="02b3d-212">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="02b3d-212">Dictionary (nested preference)</span></span> |

<span data-ttu-id="02b3d-213">Pour chaque fournisseur, vous pouvez spécifier le niveau d’autorisation souhaité pour les appareils de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02b3d-213">For each vendor, you can specify the desired permission level for devices from that vendor.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-214">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-214">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-215">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-215">**Key**</span></span> | <span data-ttu-id="02b3d-216">autorisation</span><span class="sxs-lookup"><span data-stu-id="02b3d-216">permission</span></span> |
| <span data-ttu-id="02b3d-217">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-217">**Data type**</span></span> | <span data-ttu-id="02b3d-218">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02b3d-218">Array of strings</span></span> |
| <span data-ttu-id="02b3d-219">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="02b3d-219">**Possible values**</span></span> | <span data-ttu-id="02b3d-220">Identique au [niveau d’autorisation par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="02b3d-220">Same as [Default permission level](#default-permission-level)</span></span> |

<span data-ttu-id="02b3d-221">En outre, vous pouvez éventuellement spécifier l’ensemble des produits appartenant à ce fournisseur pour lesquels des autorisations plus granulaires sont définies.</span><span class="sxs-lookup"><span data-stu-id="02b3d-221">Furthermore, you can optionally specify the set of products belonging to that vendor for which more granular permissions are defined.</span></span> <span data-ttu-id="02b3d-222">Le dictionnaire contient une ou plusieurs entrées, chaque entrée étant `products` identifiée par l’ID de produit.</span><span class="sxs-lookup"><span data-stu-id="02b3d-222">The `products` dictionary contains one or more entries, with each entry being identified by the product ID.</span></span> 

|||
|:---|:---|
| <span data-ttu-id="02b3d-223">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-223">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-224">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-224">**Key**</span></span> | <span data-ttu-id="02b3d-225">produits</span><span class="sxs-lookup"><span data-stu-id="02b3d-225">products</span></span> |
| <span data-ttu-id="02b3d-226">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-226">**Data type**</span></span> | <span data-ttu-id="02b3d-227">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="02b3d-227">Dictionary (nested preference)</span></span> |

<span data-ttu-id="02b3d-228">Pour chaque produit, vous pouvez spécifier le niveau d’autorisation souhaité pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="02b3d-228">For each product, you can specify the desired permission level for that product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-229">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-229">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-230">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-230">**Key**</span></span> | <span data-ttu-id="02b3d-231">autorisation</span><span class="sxs-lookup"><span data-stu-id="02b3d-231">permission</span></span> |
| <span data-ttu-id="02b3d-232">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-232">**Data type**</span></span> | <span data-ttu-id="02b3d-233">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02b3d-233">Array of strings</span></span> |
| <span data-ttu-id="02b3d-234">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="02b3d-234">**Possible values**</span></span> | <span data-ttu-id="02b3d-235">Identique au [niveau d’autorisation par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="02b3d-235">Same as [Default permission level](#default-permission-level)</span></span> |

<span data-ttu-id="02b3d-236">En outre, vous pouvez spécifier un ensemble facultatif de numéros de série pour lesquels des autorisations plus granulaires sont définies.</span><span class="sxs-lookup"><span data-stu-id="02b3d-236">Furthermore, you can specify an optional set of serial numbers for which more granular permissions are defined.</span></span>

<span data-ttu-id="02b3d-237">Le dictionnaire contient une ou plusieurs entrées, chaque entrée étant `serialNumbers` identifiée par le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="02b3d-237">The `serialNumbers` dictionary contains one or more entries, with each entry being identified by the serial number.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-238">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-238">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-239">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-239">**Key**</span></span> | <span data-ttu-id="02b3d-240">serialNumbers</span><span class="sxs-lookup"><span data-stu-id="02b3d-240">serialNumbers</span></span> |
| <span data-ttu-id="02b3d-241">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-241">**Data type**</span></span> | <span data-ttu-id="02b3d-242">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="02b3d-242">Dictionary (nested preference)</span></span> |

<span data-ttu-id="02b3d-243">Pour chaque numéro de série, vous pouvez spécifier le niveau d’autorisation souhaité.</span><span class="sxs-lookup"><span data-stu-id="02b3d-243">For each serial number, you can specify the desired permission level.</span></span>

|||
|:---|:---|
| <span data-ttu-id="02b3d-244">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="02b3d-244">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="02b3d-245">**Clé**</span><span class="sxs-lookup"><span data-stu-id="02b3d-245">**Key**</span></span> | <span data-ttu-id="02b3d-246">autorisation</span><span class="sxs-lookup"><span data-stu-id="02b3d-246">permission</span></span> |
| <span data-ttu-id="02b3d-247">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02b3d-247">**Data type**</span></span> | <span data-ttu-id="02b3d-248">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="02b3d-248">Array of strings</span></span> |
| <span data-ttu-id="02b3d-249">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="02b3d-249">**Possible values**</span></span> | <span data-ttu-id="02b3d-250">Identique au [niveau d’autorisation par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="02b3d-250">Same as [Default permission level](#default-permission-level)</span></span> |

#### <a name="example-device-control-policy"></a><span data-ttu-id="02b3d-251">Exemple de stratégie de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-251">Example device control policy</span></span>

<span data-ttu-id="02b3d-252">L’exemple suivant montre comment tous les concepts ci-dessus peuvent être combinés en une stratégie de contrôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="02b3d-252">The following example shows how all of the above concepts can be combined into a device control policy.</span></span> <span data-ttu-id="02b3d-253">Dans l’exemple suivant, notez la nature hiérarchique de la stratégie de média amovible.</span><span class="sxs-lookup"><span data-stu-id="02b3d-253">In the following example, note the hierarchical nature of the removable media policy.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"> 
<plist version="1.0"> 
<dict> 
    <key>deviceControl</key> 
    <dict> 
        <key>navigationTarget</key> 
        <string>[custom URL for notifications]</string> 
        <key>removableMediaPolicy</key> 
        <dict> 
            <key>enforcementLevel</key> 
            <string>[enforcement level]</string> <!-- audit / block --> 
            <key>permission</key> 
            <array> 
                <string>[permission]</string> <!-- none / read / write / execute --> 
                <!-- other permissions -->
            </array> 
            <key>vendors</key> 
            <dict> 
                <key>[vendor id]</key> 
                <dict>
                    <key>permission</key> 
                    <array> 
                        <string>[permission]</string> <!-- none / read / write / execute --> 
                        <!-- other permissions -->
                    </array> 
                    <key>products</key> 
                    <dict> 
                        <key>[product id]</key> 
                        <dict> 
                            <key>permission</key> 
                            <array> 
                                <string>[permission]</string> <!-- none / read / write / execute --> 
                                <!-- other permissions -->
                            </array> 
                            <key>serialNumbers</key> 
                            <dict> 
                                <key>[serial-number]</key> 
                                <array> 
                                    <string>[permission]</string> <!-- none / read / write / execute --> 
                                    <!-- other permissions -->
                                </array> 
                                <!-- other serial numbers --> 
                            </dict> 
                        </dict> 
                        <!-- other products --> 
                    </dict> 
                </dict> 
                <!-- other vendors --> 
            </dict> 
        </dict> 
    </dict> 
</dict> 
</plist> 
```

<span data-ttu-id="02b3d-254">Nous avons inclus d’autres exemples de stratégies de contrôle d’appareil dans les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="02b3d-254">We have included more examples of device control policies in the following documents:</span></span>

- [<span data-ttu-id="02b3d-255">Exemples de stratégies de contrôle d’appareil pour Intune</span><span class="sxs-lookup"><span data-stu-id="02b3d-255">Examples of device control policies for Intune</span></span>](mac-device-control-intune.md)
- [<span data-ttu-id="02b3d-256">Exemples de stratégies de contrôle d’appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="02b3d-256">Examples of device control policies for JAMF</span></span>](mac-device-control-jamf.md)

#### <a name="look-up-device-identifiers"></a><span data-ttu-id="02b3d-257">Rechercher des identificateurs d’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-257">Look up device identifiers</span></span>

<span data-ttu-id="02b3d-258">Pour rechercher l’ID du fournisseur, l’ID de produit et le numéro de série d’un périphérique USB :</span><span class="sxs-lookup"><span data-stu-id="02b3d-258">To find the vendor ID, product ID, and serial number of a USB device:</span></span>

1. <span data-ttu-id="02b3d-259">Connectez-vous à un appareil Mac.</span><span class="sxs-lookup"><span data-stu-id="02b3d-259">Log into a Mac device.</span></span>
1. <span data-ttu-id="02b3d-260">Branchez le périphérique USB pour lequel vous souhaitez rechercher les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="02b3d-260">Plug in the USB device for which you want to look up the identifiers.</span></span>
1. <span data-ttu-id="02b3d-261">Dans le menu de niveau supérieur de macOS, sélectionnez **À propos de ce Mac.**</span><span class="sxs-lookup"><span data-stu-id="02b3d-261">In the top-level menu of macOS, select **About This Mac**.</span></span>

    ![À propos de ce Mac](images/mac-device-control-lookup-1.png)

1. <span data-ttu-id="02b3d-263">Sélectionnez **Rapport système**.</span><span class="sxs-lookup"><span data-stu-id="02b3d-263">Select **System Report**.</span></span>

    ![Rapport système](images/mac-device-control-lookup-2.png)

1. <span data-ttu-id="02b3d-265">Dans la colonne de gauche, sélectionnez **USB.**</span><span class="sxs-lookup"><span data-stu-id="02b3d-265">From the left column, select **USB**.</span></span>

    ![Affichage de tous les périphériques USB](images/mac-device-control-lookup-3.png)

1. <span data-ttu-id="02b3d-267">Sous **Arborescence d’appareils USB,** accédez à l’appareil USB que vous avez branché.</span><span class="sxs-lookup"><span data-stu-id="02b3d-267">Under **USB Device Tree**, navigate to the USB device that you plugged in.</span></span>

    ![Détails d’un périphérique USB](images/mac-device-control-lookup-4.png)

1. <span data-ttu-id="02b3d-269">L’ID de fournisseur, l’ID de produit et le numéro de série sont affichés.</span><span class="sxs-lookup"><span data-stu-id="02b3d-269">The vendor ID, product ID, and serial number are displayed.</span></span> <span data-ttu-id="02b3d-270">Lorsque vous ajoutez l’ID fournisseur et l’ID de produit à la stratégie de média amovible, vous devez uniquement ajouter la partie après `0x` .</span><span class="sxs-lookup"><span data-stu-id="02b3d-270">When adding the vendor ID and product ID to the removable media policy, you must only add the part after `0x`.</span></span> <span data-ttu-id="02b3d-271">Par exemple, dans l’image ci-dessous, l’ID du fournisseur `1000` est et l’ID de produit est `090c` .</span><span class="sxs-lookup"><span data-stu-id="02b3d-271">For example, in the below image, vendor ID is `1000` and product ID is `090c`.</span></span>

#### <a name="discover-usb-devices-in-your-organization"></a><span data-ttu-id="02b3d-272">Découvrir les périphériques USB de votre organisation</span><span class="sxs-lookup"><span data-stu-id="02b3d-272">Discover USB devices in your organization</span></span>

<span data-ttu-id="02b3d-273">Vous pouvez afficher les événements de montage, de démontage et de modification de volume provenant de périphériques USB dans Microsoft Defender pour le hunting avancé de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="02b3d-273">You can view mount, unmount, and volume change events originating from USB devices in Microsoft Defender for Endpoint advanced hunting.</span></span> <span data-ttu-id="02b3d-274">Ces événements peuvent être utiles pour identifier une activité d’utilisation suspecte ou effectuer des enquêtes internes.</span><span class="sxs-lookup"><span data-stu-id="02b3d-274">These events can be helpful to identify suspicious usage activity or perform internal investigations.</span></span>

```
DeviceEvents 
    | where ActionType == "UsbDriveMount" or ActionType == "UsbDriveUnmount" or ActionType == "UsbDriveDriveLetterChanged"
    | where DeviceId == "<device ID>"
```

## <a name="device-control-policy-deployment"></a><span data-ttu-id="02b3d-275">Déploiement de stratégie de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="02b3d-275">Device control policy deployment</span></span>

<span data-ttu-id="02b3d-276">La stratégie de contrôle d’appareil doit être incluse en plus des autres paramètres du produit, comme décrit dans Définir les préférences de [Microsoft Defender pour Endpoint pour Mac.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="02b3d-276">The device control policy must be included next to the other product settings, as described in [Set preferences for Microsoft Defender for Endpoint for Mac](mac-preferences.md).</span></span>

<span data-ttu-id="02b3d-277">Ce profil peut être déployé à l’aide des instructions répertoriées dans le déploiement de [profil de configuration.](mac-preferences.md#configuration-profile-deployment)</span><span class="sxs-lookup"><span data-stu-id="02b3d-277">This profile can be deployed using the instructions listed in [Configuration profile deployment](mac-preferences.md#configuration-profile-deployment).</span></span>

## <a name="troubleshooting-tips"></a><span data-ttu-id="02b3d-278">Conseils de dépannage</span><span class="sxs-lookup"><span data-stu-id="02b3d-278">Troubleshooting tips</span></span>

<span data-ttu-id="02b3d-279">Après avoir lancé le profil de configuration via Intune ou JAMF, vous pouvez vérifier s’il a été correctement choisi par le produit en exécutant la commande suivante à partir du Terminal :</span><span class="sxs-lookup"><span data-stu-id="02b3d-279">After pushing the configuration profile through Intune or JAMF, you can check if it was successfully picked up by the product by running the following command from the Terminal:</span></span>

```bash
mdatp device-control removable-media policy list
```

<span data-ttu-id="02b3d-280">Cette commande imprime en sortie standard la stratégie de contrôle d’appareil que le produit utilise.</span><span class="sxs-lookup"><span data-stu-id="02b3d-280">This command will print to standard output the device control policy that the product is using.</span></span> <span data-ttu-id="02b3d-281">Dans le cas où cela imprime, assurez-vous (a) que le profil de configuration a bien été poussée vers votre appareil à partir de la console de gestion et (b) qu’il s’agit d’une stratégie de contrôle d’appareil valide, comme décrit dans ce `Policy is empty` document.</span><span class="sxs-lookup"><span data-stu-id="02b3d-281">In case this prints `Policy is empty`, make sure that (a) the configuration profile has indeed been pushed to your device from the management console, and (b) it is a valid device control policy, as described in this document.</span></span>

<span data-ttu-id="02b3d-282">Sur un appareil sur lequel la stratégie a été correctement livrée et où un ou plusieurs appareils sont branchés, vous pouvez exécuter la commande suivante pour lister tous les appareils et les autorisations effectives qui leur sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="02b3d-282">On a device where the policy has been delivered successfully and where there are one or more devices plugged in, you can run the following command to list all devices and the effective permissions applied to them.</span></span>

```bash
mdatp device-control removable-media devices list
```

<span data-ttu-id="02b3d-283">Exemple de sortie :</span><span class="sxs-lookup"><span data-stu-id="02b3d-283">Example of output:</span></span>

```Output
.Device(s)
|-o Name: Untitled 1, Permission ["read", "execute"]
| |-o Vendor: General "fff0"
| |-o Product: USB Flash Disk "1000"
| |-o Serial number: "04ZSSMHI2O7WBVOA"
| |-o Mount point: "/Volumes/TESTUSB"
```

<span data-ttu-id="02b3d-284">Dans l’exemple ci-dessus, il n’existe qu’un seul périphérique multimédia amovible branché et il dispose d’autorisations et d’autorisations, conformément à la stratégie de contrôle d’appareil qui a été remis à `read` `execute` l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02b3d-284">In the above example, there is only one removable media device plugged in and it has `read` and `execute` permissions, according to the device control policy that was delivered to the device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02b3d-285">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02b3d-285">Related topics</span></span>

- [<span data-ttu-id="02b3d-286">Exemples de stratégies de contrôle d’appareil pour Intune</span><span class="sxs-lookup"><span data-stu-id="02b3d-286">Examples of device control policies for Intune</span></span>](mac-device-control-intune.md)
- [<span data-ttu-id="02b3d-287">Exemples de stratégies de contrôle d’appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="02b3d-287">Examples of device control policies for JAMF</span></span>](mac-device-control-jamf.md)