---
title: Contrôle d'appareil pour macOS
description: Découvrez comment configurer Microsoft Defender pour endpoint sur Mac afin de réduire les menaces liées au stockage amovible tel que les périphériques USB.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, mac, appareil, contrôle, usb, amovible, média
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
ms.openlocfilehash: 39f8367c34e98c5e9dd11e9716f08e6c9e7fd9c0
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935124"
---
# <a name="device-control-for-macos"></a><span data-ttu-id="ad227-104">Contrôle d'appareil pour macOS</span><span class="sxs-lookup"><span data-stu-id="ad227-104">Device control for macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ad227-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ad227-105">**Applies to:**</span></span>
- [<span data-ttu-id="ad227-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad227-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ad227-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ad227-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="ad227-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ad227-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ad227-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ad227-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="requirements"></a><span data-ttu-id="ad227-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ad227-110">Requirements</span></span>

<span data-ttu-id="ad227-111">Le contrôle d'appareil pour macOS présente les conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad227-111">Device control for macOS has the following prerequisites:</span></span>

>[!div class="checklist"]
> - <span data-ttu-id="ad227-112">Droit au point de terminaison Microsoft Defender (peut être une version d'évaluation)</span><span class="sxs-lookup"><span data-stu-id="ad227-112">Microsoft Defender for Endpoint entitlement (can be trial)</span></span>
> - <span data-ttu-id="ad227-113">Version minimale du système d'exploitation : macOS 10.15.4 ou version supérieure</span><span class="sxs-lookup"><span data-stu-id="ad227-113">Minimum OS version: macOS 10.15.4 or higher</span></span>
> - <span data-ttu-id="ad227-114">Version minimale du produit : 101.24.59</span><span class="sxs-lookup"><span data-stu-id="ad227-114">Minimum product version: 101.24.59</span></span>
> - <span data-ttu-id="ad227-115">Votre appareil doit être en cours d'exécution avec des extensions système (il s'agit de la valeur par défaut sur macOS 11 Big Sur).</span><span class="sxs-lookup"><span data-stu-id="ad227-115">Your device must be running with system extensions (this is the default on macOS 11 Big Sur).</span></span> 
> 
>   <span data-ttu-id="ad227-116">Vous pouvez vérifier si votre appareil est en cours d'exécution sur les extensions système en exécutant la commande suivante et vérifier qu'il est en cours d'impression `endpoint_security_extension` sur la console :</span><span class="sxs-lookup"><span data-stu-id="ad227-116">You can check if your device is running on system extensions by running the following command and verify that it is printing `endpoint_security_extension` to the console:</span></span> 
> 
>   ```bash
>   mdatp health --field real_time_protection_subsystem 
>   ```
> - <span data-ttu-id="ad227-117">Votre appareil doit se trouver dans (précédemment appelé) canal de mise à jour de mise à jour `Beta` `InsiderFast` automatique Microsoft AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="ad227-117">Your device must be in `Beta` (previously called `InsiderFast`) Microsoft AutoUpdate update channel.</span></span> <span data-ttu-id="ad227-118">Pour plus d'informations, voir [Déployer les mises à jour de Microsoft Defender pour Endpoint sur Mac.](mac-updates.md)</span><span class="sxs-lookup"><span data-stu-id="ad227-118">For more information, see [Deploy updates for Microsoft Defender for Endpoint on Mac](mac-updates.md).</span></span>
> 
>   <span data-ttu-id="ad227-119">Vous pouvez vérifier le canal de mise à jour à l'aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ad227-119">You can check the update channel using the following command:</span></span> 
> 
>    ```bash
>    mdatp health --field release_ring 
>    ```
>
>    <span data-ttu-id="ad227-120">Si la commande ci-dessus n'imprime pas l'une ou l'autre des commandes, exécutez `Beta` la commande suivante à partir du `InsiderFast` Terminal.</span><span class="sxs-lookup"><span data-stu-id="ad227-120">If the above command does not print either `Beta` or `InsiderFast`, execute the following command from the Terminal.</span></span> <span data-ttu-id="ad227-121">La mise à jour du canal prend effet lors du prochain démarrage du produit (lors de l'installation de la prochaine mise à jour du produit ou du redémarrage de l'appareil).</span><span class="sxs-lookup"><span data-stu-id="ad227-121">The channel update takes effect next time the product starts (when the next product update is installed or when the device is rebooted).</span></span> 
> 
>    ```bash
>    defaults write com.microsoft.autoupdate2 ChannelName -string Beta
>    ```
>
>    <span data-ttu-id="ad227-122">Par ailleurs, si vous êtes dans un environnement géré (JAMF ou Intune), vous pouvez configurer le canal de mise à jour à distance.</span><span class="sxs-lookup"><span data-stu-id="ad227-122">Alternatively, if you are in a managed environment (JAMF or Intune), you can configure the update channel remotely.</span></span> <span data-ttu-id="ad227-123">Pour plus d'informations, voir [Déployer les mises à jour de Microsoft Defender pour Endpoint sur Mac.](mac-updates.md)</span><span class="sxs-lookup"><span data-stu-id="ad227-123">For more information, see [Deploy updates for Microsoft Defender for Endpoint on Mac](mac-updates.md).</span></span> 

## <a name="device-control-policy"></a><span data-ttu-id="ad227-124">Stratégie de contrôle d'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-124">Device control policy</span></span>

<span data-ttu-id="ad227-125">Pour configurer le contrôle d'appareil pour macOS, vous devez créer une stratégie qui décrit les restrictions que vous souhaitez mettre en place au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ad227-125">To configure device control for macOS, you must create a policy that describes the restrictions you want to put in place within your organization.</span></span>

<span data-ttu-id="ad227-126">La stratégie de contrôle d'appareil est incluse dans le profil de configuration utilisé pour configurer tous les autres paramètres du produit.</span><span class="sxs-lookup"><span data-stu-id="ad227-126">The device control policy is included in the configuration profile used to configure all other product settings.</span></span> <span data-ttu-id="ad227-127">Pour plus d'informations, voir [Structure de profil de configuration.](mac-preferences.md#configuration-profile-structure)</span><span class="sxs-lookup"><span data-stu-id="ad227-127">For more information, see [Configuration profile structure](mac-preferences.md#configuration-profile-structure).</span></span>

<span data-ttu-id="ad227-128">Dans le profil de configuration, la stratégie de contrôle d'appareil est définie dans la section suivante :</span><span class="sxs-lookup"><span data-stu-id="ad227-128">Within the configuration profile, the device control policy is defined in the following section:</span></span>

|<span data-ttu-id="ad227-129">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-129">Section</span></span>|<span data-ttu-id="ad227-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-130">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-131">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-131">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-132">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-132">**Key**</span></span> | <span data-ttu-id="ad227-133">deviceControl</span><span class="sxs-lookup"><span data-stu-id="ad227-133">deviceControl</span></span> |
| <span data-ttu-id="ad227-134">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-134">**Data type**</span></span> | <span data-ttu-id="ad227-135">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="ad227-135">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="ad227-136">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="ad227-136">**Comments**</span></span> | <span data-ttu-id="ad227-137">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="ad227-137">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="ad227-138">La stratégie de contrôle d'appareil peut être utilisée pour :</span><span class="sxs-lookup"><span data-stu-id="ad227-138">The device control policy can be used to:</span></span>

- [<span data-ttu-id="ad227-139">Personnaliser la cible d'URL pour les notifications dues au contrôle d'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-139">Customize the URL target for notifications raised by device control</span></span>](#customize-url-target-for-notifications-raised-by-device-control)
- [<span data-ttu-id="ad227-140">Autoriser ou bloquer les appareils amovibles</span><span class="sxs-lookup"><span data-stu-id="ad227-140">Allow or block removable devices</span></span>](#allow-or-block-removable-devices)

### <a name="customize-url-target-for-notifications-raised-by-device-control"></a><span data-ttu-id="ad227-141">Personnaliser la cible d'URL pour les notifications dues au contrôle d'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-141">Customize URL target for notifications raised by device control</span></span>

<span data-ttu-id="ad227-142">Lorsque la stratégie de contrôle d'appareil que vous avez mise en place est appliquée sur un appareil (par exemple, l'accès à un périphérique multimédia amovible est restreint), une notification s'affiche pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad227-142">When the device control policy that you have put in place is enforced on a device (for example, access to a removable media device is restricted), a notification is displayed to the user.</span></span>

![Notification de contrôle d'appareil](images/mac-device-control-notification.png)

<span data-ttu-id="ad227-144">Lorsque les utilisateurs finaux cliquent sur cette notification, une page web s'ouvre dans le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad227-144">When end users click this notification, a web page is opened in the default browser.</span></span> <span data-ttu-id="ad227-145">Vous pouvez configurer l'URL qui est ouverte lorsque les utilisateurs finaux cliquent sur la notification.</span><span class="sxs-lookup"><span data-stu-id="ad227-145">You can configure the URL that is opened when end users click the notification.</span></span>

|<span data-ttu-id="ad227-146">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-146">Section</span></span>|<span data-ttu-id="ad227-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-147">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-148">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-148">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-149">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-149">**Key**</span></span> | <span data-ttu-id="ad227-150">navigationTarget</span><span class="sxs-lookup"><span data-stu-id="ad227-150">navigationTarget</span></span> |
| <span data-ttu-id="ad227-151">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-151">**Data type**</span></span> | <span data-ttu-id="ad227-152">String</span><span class="sxs-lookup"><span data-stu-id="ad227-152">String</span></span> |
| <span data-ttu-id="ad227-153">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="ad227-153">**Comments**</span></span> | <span data-ttu-id="ad227-154">S'il n'est pas défini, le produit utilise une URL par défaut pointant vers une page générique expliquant l'action entreprise par le produit.</span><span class="sxs-lookup"><span data-stu-id="ad227-154">If not defined, the product uses a default URL pointing to a generic page explaining the action taken by the product.</span></span> |

### <a name="allow-or-block-removable-devices"></a><span data-ttu-id="ad227-155">Autoriser ou bloquer les appareils amovibles</span><span class="sxs-lookup"><span data-stu-id="ad227-155">Allow or block removable devices</span></span>

<span data-ttu-id="ad227-156">La section multimédia amovible de la stratégie de contrôle d'appareil est utilisée pour restreindre l'accès aux médias amovibles.</span><span class="sxs-lookup"><span data-stu-id="ad227-156">The removable media section of the device control policy is used to restrict access to removable media.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad227-157">Les types de média amovible suivants sont actuellement pris en charge et peuvent être inclus dans la stratégie : les périphériques de stockage USB.</span><span class="sxs-lookup"><span data-stu-id="ad227-157">The following types of removable media are currently supported and can be included in the policy: USB storage devices.</span></span>

|<span data-ttu-id="ad227-158">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-158">Section</span></span>|<span data-ttu-id="ad227-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-159">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-160">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-160">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-161">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-161">**Key**</span></span> | <span data-ttu-id="ad227-162">removableMediaPolicy</span><span class="sxs-lookup"><span data-stu-id="ad227-162">removableMediaPolicy</span></span> |
| <span data-ttu-id="ad227-163">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-163">**Data type**</span></span> | <span data-ttu-id="ad227-164">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="ad227-164">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="ad227-165">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="ad227-165">**Comments**</span></span> | <span data-ttu-id="ad227-166">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="ad227-166">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="ad227-167">Cette section de la stratégie est hiérarchique, ce qui permet une flexibilité maximale et couvre un large éventail de cas d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="ad227-167">This section of the policy is hierarchical, allowing for maximum flexibility and covering a wide range of use cases.</span></span> <span data-ttu-id="ad227-168">Au niveau supérieur, les fournisseurs sont identifiés par un ID de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad227-168">At the top level are vendors, identified by a vendor ID.</span></span> <span data-ttu-id="ad227-169">Pour chaque fournisseur, il existe des produits, identifiés par un ID de produit.</span><span class="sxs-lookup"><span data-stu-id="ad227-169">For each vendor, there are products, identified by a product ID.</span></span> <span data-ttu-id="ad227-170">Enfin, pour chaque produit, il existe des numéros de série qui notent des appareils spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ad227-170">Finally, for each product there are serial numbers denoting specific devices.</span></span>

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

<span data-ttu-id="ad227-171">Pour plus d'informations sur la recherche des identificateurs d'appareil, voir [Rechercher des identificateurs d'appareil.](#look-up-device-identifiers)</span><span class="sxs-lookup"><span data-stu-id="ad227-171">For information on how to find the device identifiers, see [Look up device identifiers](#look-up-device-identifiers).</span></span>

<span data-ttu-id="ad227-172">La stratégie est évaluée de l'entrée la plus spécifique à la plus générale.</span><span class="sxs-lookup"><span data-stu-id="ad227-172">The policy is evaluated from the most specific entry to the most general one.</span></span> <span data-ttu-id="ad227-173">Autrement dit, lorsqu'un appareil est branché, le produit tente de trouver la correspondance la plus spécifique dans la stratégie pour chaque périphérique multimédia amovible et applique les autorisations à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="ad227-173">Meaning, when a device is plugged in, the product tries to find the most specific match in the policy for each removable media device and apply the permissions at that level.</span></span> <span data-ttu-id="ad227-174">En l'absence de correspondance, la meilleure correspondance suivante est appliquée, jusqu'à l'autorisation spécifiée au niveau supérieur, qui est la valeur par défaut lorsqu'un appareil ne correspond à aucune autre entrée de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ad227-174">If there is no match, then the next best match is applied, all the way to the permission specified at the top level, which is the default when a device does not match any other entry in the policy.</span></span>

#### <a name="policy-enforcement-level"></a><span data-ttu-id="ad227-175">Niveau d'application de la stratégie</span><span class="sxs-lookup"><span data-stu-id="ad227-175">Policy enforcement level</span></span>

<span data-ttu-id="ad227-176">Sous la section Média amovible, il existe une option pour définir le niveau d'application, qui peut prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad227-176">Under the removable media section, there is an option to set the enforcement level, which can take one of the following values:</span></span>

- <span data-ttu-id="ad227-177">`audit` - Sous ce niveau d'application, si l'accès à un appareil est restreint, une notification s'affiche pour l'utilisateur, mais l'appareil peut toujours être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad227-177">`audit` - Under this enforcement level, if access to a device is restricted, a notification is displayed to the user, however the device can still be used.</span></span> <span data-ttu-id="ad227-178">Ce niveau d'application peut être utile pour évaluer l'efficacité d'une stratégie.</span><span class="sxs-lookup"><span data-stu-id="ad227-178">This enforcement level can be useful to evaluate the effectiveness of a policy.</span></span>
- <span data-ttu-id="ad227-179">`block` - Sous ce niveau d'application, les opérations que l'utilisateur peut effectuer sur l'appareil sont limitées à ce qui est défini dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ad227-179">`block` - Under this enforcement level, the operations that the user can perform on the device are limited to what is defined in the policy.</span></span> <span data-ttu-id="ad227-180">En outre, une notification est alors avertie à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad227-180">Furthermore, a notification is raised to the user.</span></span> 

|<span data-ttu-id="ad227-181">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-181">Section</span></span>|<span data-ttu-id="ad227-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-182">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-183">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-183">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-184">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-184">**Key**</span></span> | <span data-ttu-id="ad227-185">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="ad227-185">enforcementLevel</span></span> |
| <span data-ttu-id="ad227-186">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-186">**Data type**</span></span> | <span data-ttu-id="ad227-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ad227-187">String</span></span> |
| <span data-ttu-id="ad227-188">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ad227-188">**Possible values**</span></span> | <span data-ttu-id="ad227-189">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="ad227-189">audit (default)</span></span> <br/> <span data-ttu-id="ad227-190">block</span><span class="sxs-lookup"><span data-stu-id="ad227-190">block</span></span> |

#### <a name="default-permission-level"></a><span data-ttu-id="ad227-191">Niveau d’autorisation par défaut</span><span class="sxs-lookup"><span data-stu-id="ad227-191">Default permission level</span></span>

<span data-ttu-id="ad227-192">Au niveau supérieur de la section Média amovible, vous pouvez configurer le niveau d'autorisation par défaut pour les appareils qui ne correspondent à rien d'autre dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ad227-192">At the top level of the removable media section, you can configure the default permission level for devices that do not match anything else in the policy.</span></span>

<span data-ttu-id="ad227-193">Ce paramètre peut être définie sur :</span><span class="sxs-lookup"><span data-stu-id="ad227-193">This setting can be set to:</span></span>

- <span data-ttu-id="ad227-194">`none` - Aucune opération ne peut être effectuée sur l'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-194">`none` - No operations can be performed on the device</span></span>
- <span data-ttu-id="ad227-195">Combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad227-195">A combination of the following values:</span></span>
    - <span data-ttu-id="ad227-196">`read` - Les opérations de lecture sont autorisées sur l'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-196">`read` - Read operations are permitted on the device</span></span>
    - <span data-ttu-id="ad227-197">`write` - Les opérations d'écriture sont autorisées sur l'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-197">`write` - Write operations are permitted on the device</span></span>
    - <span data-ttu-id="ad227-198">`execute` - Les opérations d'exécution sont autorisées sur l'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-198">`execute` - Execute operations are permitted on the device</span></span>

> [!NOTE]
> <span data-ttu-id="ad227-199">`none`S'il est présent dans le niveau d'autorisation, toutes les autres autorisations ( ou ) sont `read` `write` `execute` ignorées.</span><span class="sxs-lookup"><span data-stu-id="ad227-199">If `none` is present in the permission level, any other permissions (`read`, `write`, or `execute`) will be ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="ad227-200">L'autorisation fait uniquement référence à l'exécution des binaires `execute` Mach-O.</span><span class="sxs-lookup"><span data-stu-id="ad227-200">The `execute` permission only refers to execution of Mach-O binaries.</span></span> <span data-ttu-id="ad227-201">Il n'inclut pas l'exécution de scripts ou d'autres types de charges utiles.</span><span class="sxs-lookup"><span data-stu-id="ad227-201">It does not include execution of scripts or other types of payloads.</span></span>

|<span data-ttu-id="ad227-202">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-202">Section</span></span>|<span data-ttu-id="ad227-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-203">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-204">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-204">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-205">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-205">**Key**</span></span> | <span data-ttu-id="ad227-206">autorisation</span><span class="sxs-lookup"><span data-stu-id="ad227-206">permission</span></span> |
| <span data-ttu-id="ad227-207">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-207">**Data type**</span></span> | <span data-ttu-id="ad227-208">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="ad227-208">Array of strings</span></span> |
| <span data-ttu-id="ad227-209">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ad227-209">**Possible values**</span></span> | <span data-ttu-id="ad227-210">aucune</span><span class="sxs-lookup"><span data-stu-id="ad227-210">none</span></span> <br/> <span data-ttu-id="ad227-211">read</span><span class="sxs-lookup"><span data-stu-id="ad227-211">read</span></span> <br/> <span data-ttu-id="ad227-212">write</span><span class="sxs-lookup"><span data-stu-id="ad227-212">write</span></span> <br/> <span data-ttu-id="ad227-213">execute</span><span class="sxs-lookup"><span data-stu-id="ad227-213">execute</span></span> |

#### <a name="restrict-removable-media-by-vendor-product-and-serial-number"></a><span data-ttu-id="ad227-214">Restreindre les médias amovibles par fournisseur, produit et numéro de série</span><span class="sxs-lookup"><span data-stu-id="ad227-214">Restrict removable media by vendor, product, and serial number</span></span>

<span data-ttu-id="ad227-215">Comme décrit dans [Autoriser](#allow-or-block-removable-devices)ou bloquer les appareils amovibles, les supports amovibles tels que les périphériques USB peuvent être identifiés par l'ID du fournisseur, l'ID de produit et le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="ad227-215">As described in [Allow or block removable devices](#allow-or-block-removable-devices), removable media such as USB devices can be identified by the vendor ID, product ID, and serial number.</span></span>

<span data-ttu-id="ad227-216">Au niveau supérieur de la stratégie de média amovible, vous pouvez éventuellement définir des restrictions plus précises au niveau du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad227-216">At the top level of the removable media policy, you can optionally define more granular restrictions at the vendor level.</span></span> 

<span data-ttu-id="ad227-217">Le `vendors` dictionnaire contient une ou plusieurs entrées, chaque entrée étant identifiée par l'ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad227-217">The `vendors` dictionary contains one or more entries, with each entry being identified by the vendor ID.</span></span>

|<span data-ttu-id="ad227-218">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-218">Section</span></span>|<span data-ttu-id="ad227-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-219">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-220">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-220">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-221">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-221">**Key**</span></span> | <span data-ttu-id="ad227-222">fournisseurs</span><span class="sxs-lookup"><span data-stu-id="ad227-222">vendors</span></span> |
| <span data-ttu-id="ad227-223">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-223">**Data type**</span></span> | <span data-ttu-id="ad227-224">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="ad227-224">Dictionary (nested preference)</span></span> |

<span data-ttu-id="ad227-225">Pour chaque fournisseur, vous pouvez spécifier le niveau d'autorisation souhaité pour les appareils de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad227-225">For each vendor, you can specify the desired permission level for devices from that vendor.</span></span>

|<span data-ttu-id="ad227-226">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-226">Section</span></span>|<span data-ttu-id="ad227-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-227">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-228">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-228">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-229">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-229">**Key**</span></span> | <span data-ttu-id="ad227-230">autorisation</span><span class="sxs-lookup"><span data-stu-id="ad227-230">permission</span></span> |
| <span data-ttu-id="ad227-231">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-231">**Data type**</span></span> | <span data-ttu-id="ad227-232">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="ad227-232">Array of strings</span></span> |
| <span data-ttu-id="ad227-233">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ad227-233">**Possible values**</span></span> | <span data-ttu-id="ad227-234">Identique au [niveau d'autorisation Par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="ad227-234">Same as [Default permission level](#default-permission-level)</span></span> |

<span data-ttu-id="ad227-235">En outre, vous pouvez éventuellement spécifier l'ensemble des produits appartenant à ce fournisseur pour lesquels des autorisations plus précises sont définies.</span><span class="sxs-lookup"><span data-stu-id="ad227-235">Furthermore, you can optionally specify the set of products belonging to that vendor for which more granular permissions are defined.</span></span> <span data-ttu-id="ad227-236">Le dictionnaire contient une ou plusieurs entrées, chaque entrée étant identifiée par `products` l'ID de produit.</span><span class="sxs-lookup"><span data-stu-id="ad227-236">The `products` dictionary contains one or more entries, with each entry being identified by the product ID.</span></span> 

|<span data-ttu-id="ad227-237">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-237">Section</span></span>|<span data-ttu-id="ad227-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-238">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-239">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-239">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-240">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-240">**Key**</span></span> | <span data-ttu-id="ad227-241">produits</span><span class="sxs-lookup"><span data-stu-id="ad227-241">products</span></span> |
| <span data-ttu-id="ad227-242">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-242">**Data type**</span></span> | <span data-ttu-id="ad227-243">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="ad227-243">Dictionary (nested preference)</span></span> |

<span data-ttu-id="ad227-244">Pour chaque produit, vous pouvez spécifier le niveau d'autorisation souhaité pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="ad227-244">For each product, you can specify the desired permission level for that product.</span></span>

|<span data-ttu-id="ad227-245">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-245">Section</span></span>|<span data-ttu-id="ad227-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-246">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-247">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-247">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-248">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-248">**Key**</span></span> | <span data-ttu-id="ad227-249">autorisation</span><span class="sxs-lookup"><span data-stu-id="ad227-249">permission</span></span> |
| <span data-ttu-id="ad227-250">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-250">**Data type**</span></span> | <span data-ttu-id="ad227-251">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="ad227-251">Array of strings</span></span> |
| <span data-ttu-id="ad227-252">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ad227-252">**Possible values**</span></span> | <span data-ttu-id="ad227-253">Identique au [niveau d'autorisation Par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="ad227-253">Same as [Default permission level](#default-permission-level)</span></span> |

<span data-ttu-id="ad227-254">En outre, vous pouvez spécifier un ensemble facultatif de numéros de série pour lesquels des autorisations plus granulaires sont définies.</span><span class="sxs-lookup"><span data-stu-id="ad227-254">Furthermore, you can specify an optional set of serial numbers for which more granular permissions are defined.</span></span>

<span data-ttu-id="ad227-255">Le `serialNumbers` dictionnaire contient une ou plusieurs entrées, chaque entrée étant identifiée par le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="ad227-255">The `serialNumbers` dictionary contains one or more entries, with each entry being identified by the serial number.</span></span>

|<span data-ttu-id="ad227-256">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-256">Section</span></span>|<span data-ttu-id="ad227-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-257">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-258">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-258">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-259">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-259">**Key**</span></span> | <span data-ttu-id="ad227-260">serialNumbers</span><span class="sxs-lookup"><span data-stu-id="ad227-260">serialNumbers</span></span> |
| <span data-ttu-id="ad227-261">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-261">**Data type**</span></span> | <span data-ttu-id="ad227-262">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="ad227-262">Dictionary (nested preference)</span></span> |

<span data-ttu-id="ad227-263">Pour chaque numéro de série, vous pouvez spécifier le niveau d'autorisation souhaité.</span><span class="sxs-lookup"><span data-stu-id="ad227-263">For each serial number, you can specify the desired permission level.</span></span>

|<span data-ttu-id="ad227-264">Section</span><span class="sxs-lookup"><span data-stu-id="ad227-264">Section</span></span>|<span data-ttu-id="ad227-265">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad227-265">Value</span></span>|
|:---|:---|
| <span data-ttu-id="ad227-266">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ad227-266">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="ad227-267">**Key**</span><span class="sxs-lookup"><span data-stu-id="ad227-267">**Key**</span></span> | <span data-ttu-id="ad227-268">autorisation</span><span class="sxs-lookup"><span data-stu-id="ad227-268">permission</span></span> |
| <span data-ttu-id="ad227-269">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ad227-269">**Data type**</span></span> | <span data-ttu-id="ad227-270">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="ad227-270">Array of strings</span></span> |
| <span data-ttu-id="ad227-271">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ad227-271">**Possible values**</span></span> | <span data-ttu-id="ad227-272">Identique au [niveau d'autorisation Par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="ad227-272">Same as [Default permission level](#default-permission-level)</span></span> |

#### <a name="example-device-control-policy"></a><span data-ttu-id="ad227-273">Exemple de stratégie de contrôle d'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-273">Example device control policy</span></span>

<span data-ttu-id="ad227-274">L'exemple suivant montre comment tous les concepts ci-dessus peuvent être combinés en une stratégie de contrôle d'appareil.</span><span class="sxs-lookup"><span data-stu-id="ad227-274">The following example shows how all of the above concepts can be combined into a device control policy.</span></span> <span data-ttu-id="ad227-275">Dans l'exemple suivant, notez la nature hiérarchique de la stratégie de média amovible.</span><span class="sxs-lookup"><span data-stu-id="ad227-275">In the following example, note the hierarchical nature of the removable media policy.</span></span>

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

<span data-ttu-id="ad227-276">Nous avons inclus d'autres exemples de stratégies de contrôle d'appareil dans les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="ad227-276">We have included more examples of device control policies in the following documents:</span></span>

- [<span data-ttu-id="ad227-277">Exemples de stratégies de contrôle d'appareil pour Intune</span><span class="sxs-lookup"><span data-stu-id="ad227-277">Examples of device control policies for Intune</span></span>](mac-device-control-intune.md)
- [<span data-ttu-id="ad227-278">Exemples de stratégies de contrôle d'appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="ad227-278">Examples of device control policies for JAMF</span></span>](mac-device-control-jamf.md)

#### <a name="look-up-device-identifiers"></a><span data-ttu-id="ad227-279">Rechercher des identificateurs d'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-279">Look up device identifiers</span></span>

<span data-ttu-id="ad227-280">Pour rechercher l'ID du fournisseur, l'ID de produit et le numéro de série d'un périphérique USB :</span><span class="sxs-lookup"><span data-stu-id="ad227-280">To find the vendor ID, product ID, and serial number of a USB device:</span></span>

1. <span data-ttu-id="ad227-281">Connectez-vous à un appareil Mac.</span><span class="sxs-lookup"><span data-stu-id="ad227-281">Log into a Mac device.</span></span>
1. <span data-ttu-id="ad227-282">Branchez le périphérique USB pour lequel vous souhaitez rechercher les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="ad227-282">Plug in the USB device for which you want to look up the identifiers.</span></span>
1. <span data-ttu-id="ad227-283">Dans le menu de niveau supérieur de macOS, sélectionnez **À propos de ce Mac.**</span><span class="sxs-lookup"><span data-stu-id="ad227-283">In the top-level menu of macOS, select **About This Mac**.</span></span>

    ![À propos de ce Mac](images/mac-device-control-lookup-1.png)

1. <span data-ttu-id="ad227-285">Sélectionnez **Rapport système**.</span><span class="sxs-lookup"><span data-stu-id="ad227-285">Select **System Report**.</span></span>

    ![Rapport système](images/mac-device-control-lookup-2.png)

1. <span data-ttu-id="ad227-287">Dans la colonne de gauche, sélectionnez **USB.**</span><span class="sxs-lookup"><span data-stu-id="ad227-287">From the left column, select **USB**.</span></span>

    ![Affichage de tous les périphériques USB](images/mac-device-control-lookup-3.png)

1. <span data-ttu-id="ad227-289">Sous **Arborescence d'appareils USB,** accédez à l'appareil USB que vous avez branché.</span><span class="sxs-lookup"><span data-stu-id="ad227-289">Under **USB Device Tree**, navigate to the USB device that you plugged in.</span></span>

    ![Détails d'un périphérique USB](images/mac-device-control-lookup-4.png)

1. <span data-ttu-id="ad227-291">L'ID du fournisseur, l'ID de produit et le numéro de série sont affichés.</span><span class="sxs-lookup"><span data-stu-id="ad227-291">The vendor ID, product ID, and serial number are displayed.</span></span> <span data-ttu-id="ad227-292">Lorsque vous ajoutez l'ID fournisseur et l'ID de produit à la stratégie de média amovible, vous devez uniquement ajouter la partie après `0x` .</span><span class="sxs-lookup"><span data-stu-id="ad227-292">When adding the vendor ID and product ID to the removable media policy, you must only add the part after `0x`.</span></span> <span data-ttu-id="ad227-293">Par exemple, dans l'image ci-dessous, l'ID du fournisseur `1000` est et l'ID de produit est `090c` .</span><span class="sxs-lookup"><span data-stu-id="ad227-293">For example, in the below image, vendor ID is `1000` and product ID is `090c`.</span></span>

#### <a name="discover-usb-devices-in-your-organization"></a><span data-ttu-id="ad227-294">Découvrir les périphériques USB de votre organisation</span><span class="sxs-lookup"><span data-stu-id="ad227-294">Discover USB devices in your organization</span></span>

<span data-ttu-id="ad227-295">Vous pouvez afficher les événements de montage, de démontage et de modification de volume provenant de périphériques USB dans Microsoft Defender pour le recherche avancée de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ad227-295">You can view mount, unmount, and volume change events originating from USB devices in Microsoft Defender for Endpoint advanced hunting.</span></span> <span data-ttu-id="ad227-296">Ces événements peuvent être utiles pour identifier une activité d'utilisation suspecte ou effectuer des enquêtes internes.</span><span class="sxs-lookup"><span data-stu-id="ad227-296">These events can be helpful to identify suspicious usage activity or perform internal investigations.</span></span>

```
DeviceEvents 
    | where ActionType == "UsbDriveMount" or ActionType == "UsbDriveUnmount" or ActionType == "UsbDriveDriveLetterChanged"
    | where DeviceId == "<device ID>"
```

## <a name="device-control-policy-deployment"></a><span data-ttu-id="ad227-297">Déploiement de stratégie de contrôle d'appareil</span><span class="sxs-lookup"><span data-stu-id="ad227-297">Device control policy deployment</span></span>

<span data-ttu-id="ad227-298">La stratégie de contrôle d'appareil doit être incluse en plus des autres paramètres du produit, comme décrit dans Définir les préférences de [Microsoft Defender pour endpoint sur macOS.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="ad227-298">The device control policy must be included next to the other product settings, as described in [Set preferences for Microsoft Defender for Endpoint on macOS](mac-preferences.md).</span></span>

<span data-ttu-id="ad227-299">Ce profil peut être déployé à l'aide des instructions répertoriées dans le déploiement de [profil de configuration.](mac-preferences.md#configuration-profile-deployment)</span><span class="sxs-lookup"><span data-stu-id="ad227-299">This profile can be deployed using the instructions listed in [Configuration profile deployment](mac-preferences.md#configuration-profile-deployment).</span></span>

## <a name="troubleshooting-tips"></a><span data-ttu-id="ad227-300">Conseils de dépannage</span><span class="sxs-lookup"><span data-stu-id="ad227-300">Troubleshooting tips</span></span>

<span data-ttu-id="ad227-301">Après avoir lancé le profil de configuration via Intune ou JAMF, vous pouvez vérifier s'il a été correctement choisi par le produit en exécutant la commande suivante à partir du Terminal :</span><span class="sxs-lookup"><span data-stu-id="ad227-301">After pushing the configuration profile through Intune or JAMF, you can check if it was successfully picked up by the product by running the following command from the Terminal:</span></span>

```bash
mdatp device-control removable-media policy list
```

<span data-ttu-id="ad227-302">Cette commande imprime en sortie standard la stratégie de contrôle d'appareil que le produit utilise.</span><span class="sxs-lookup"><span data-stu-id="ad227-302">This command will print to standard output the device control policy that the product is using.</span></span> <span data-ttu-id="ad227-303">Dans le cas où cela imprime, assurez-vous (a) que le profil de configuration a bien été poussée sur votre appareil à partir de la console de gestion et (b) qu'il s'agit d'une stratégie de contrôle d'appareil valide, comme décrit dans ce `Policy is empty` document.</span><span class="sxs-lookup"><span data-stu-id="ad227-303">In case this prints `Policy is empty`, make sure that (a) the configuration profile has indeed been pushed to your device from the management console, and (b) it is a valid device control policy, as described in this document.</span></span>

<span data-ttu-id="ad227-304">Sur un appareil sur lequel la stratégie a été correctement livrée et où un ou plusieurs appareils sont branchés, vous pouvez exécuter la commande suivante pour lister tous les appareils et les autorisations effectives qui leur sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="ad227-304">On a device where the policy has been delivered successfully and where there are one or more devices plugged in, you can run the following command to list all devices and the effective permissions applied to them.</span></span>

```bash
mdatp device-control removable-media devices list
```

<span data-ttu-id="ad227-305">Exemple de sortie :</span><span class="sxs-lookup"><span data-stu-id="ad227-305">Example of output:</span></span>

```Output
.Device(s)
|-o Name: Untitled 1, Permission ["read", "execute"]
| |-o Vendor: General "fff0"
| |-o Product: USB Flash Disk "1000"
| |-o Serial number: "04ZSSMHI2O7WBVOA"
| |-o Mount point: "/Volumes/TESTUSB"
```

<span data-ttu-id="ad227-306">Dans l'exemple ci-dessus, il n'existe qu'un seul périphérique multimédia amovible branché et il dispose d'autorisations et d'autorisations, conformément à la stratégie de contrôle d'appareil qui a été remis à `read` `execute` l'appareil.</span><span class="sxs-lookup"><span data-stu-id="ad227-306">In the above example, there is only one removable media device plugged in and it has `read` and `execute` permissions, according to the device control policy that was delivered to the device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad227-307">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad227-307">Related topics</span></span>

- [<span data-ttu-id="ad227-308">Exemples de stratégies de contrôle d'appareil pour Intune</span><span class="sxs-lookup"><span data-stu-id="ad227-308">Examples of device control policies for Intune</span></span>](mac-device-control-intune.md)
- [<span data-ttu-id="ad227-309">Exemples de stratégies de contrôle d'appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="ad227-309">Examples of device control policies for JAMF</span></span>](mac-device-control-jamf.md)
