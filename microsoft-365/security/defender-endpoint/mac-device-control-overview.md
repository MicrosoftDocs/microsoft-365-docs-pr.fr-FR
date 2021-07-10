---
title: Contrôle d’appareil pour macOS
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
ms.openlocfilehash: 5cb819daa11a50ef54c758a6aa696a5fc645029c
ms.sourcegitcommit: 7dc3b4dec05299abb4290a6e3d1ebe0fdc622ed7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "53363978"
---
# <a name="device-control-for-macos"></a><span data-ttu-id="8fdbd-104">Contrôle d’appareil pour macOS</span><span class="sxs-lookup"><span data-stu-id="8fdbd-104">Device control for macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="8fdbd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-105">**Applies to:**</span></span>
- [<span data-ttu-id="8fdbd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8fdbd-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="8fdbd-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8fdbd-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="8fdbd-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8fdbd-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8fdbd-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="requirements"></a><span data-ttu-id="8fdbd-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="8fdbd-110">Requirements</span></span>

<span data-ttu-id="8fdbd-111">Le contrôle d’appareil pour macOS présente les conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-111">Device control for macOS has the following prerequisites:</span></span>

>[!div class="checklist"]
> - <span data-ttu-id="8fdbd-112">Droit au point de terminaison Microsoft Defender (peut être une version d’évaluation)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-112">Microsoft Defender for Endpoint entitlement (can be trial)</span></span>
> - <span data-ttu-id="8fdbd-113">Version minimale du système d’exploitation : macOS 11 ou version supérieure</span><span class="sxs-lookup"><span data-stu-id="8fdbd-113">Minimum OS version: macOS 11 or higher</span></span>
> - <span data-ttu-id="8fdbd-114">Version minimale du produit : 101.34.20</span><span class="sxs-lookup"><span data-stu-id="8fdbd-114">Minimum product version: 101.34.20</span></span>

## <a name="device-control-policy"></a><span data-ttu-id="8fdbd-115">Stratégie de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-115">Device control policy</span></span>

<span data-ttu-id="8fdbd-116">Pour configurer le contrôle d’appareil pour macOS, vous devez créer une stratégie qui décrit les restrictions que vous souhaitez mettre en place au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-116">To configure device control for macOS, you must create a policy that describes the restrictions you want to put in place within your organization.</span></span>

<span data-ttu-id="8fdbd-117">La stratégie de contrôle d’appareil est incluse dans le profil de configuration utilisé pour configurer tous les autres paramètres du produit.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-117">The device control policy is included in the configuration profile used to configure all other product settings.</span></span> <span data-ttu-id="8fdbd-118">Pour plus d’informations, voir [Structure de profil de configuration.](mac-preferences.md#configuration-profile-structure)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-118">For more information, see [Configuration profile structure](mac-preferences.md#configuration-profile-structure).</span></span>

<span data-ttu-id="8fdbd-119">Dans le profil de configuration, la stratégie de contrôle d’appareil est définie dans la section suivante :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-119">Within the configuration profile, the device control policy is defined in the following section:</span></span>

|<span data-ttu-id="8fdbd-120">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-120">Section</span></span>|<span data-ttu-id="8fdbd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-121">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-122">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-122">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-123">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-123">**Key**</span></span> | <span data-ttu-id="8fdbd-124">deviceControl</span><span class="sxs-lookup"><span data-stu-id="8fdbd-124">deviceControl</span></span> |
| <span data-ttu-id="8fdbd-125">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-125">**Data type**</span></span> | <span data-ttu-id="8fdbd-126">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-126">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8fdbd-127">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-127">**Comments**</span></span> | <span data-ttu-id="8fdbd-128">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-128">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="8fdbd-129">La stratégie de contrôle d’appareil peut être utilisée pour :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-129">The device control policy can be used to:</span></span>

- [<span data-ttu-id="8fdbd-130">Personnaliser la cible d’URL pour les notifications dues au contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-130">Customize the URL target for notifications raised by device control</span></span>](#customize-url-target-for-notifications-raised-by-device-control)
- [<span data-ttu-id="8fdbd-131">Autoriser ou bloquer les appareils amovibles</span><span class="sxs-lookup"><span data-stu-id="8fdbd-131">Allow or block removable devices</span></span>](#allow-or-block-removable-devices)

### <a name="customize-url-target-for-notifications-raised-by-device-control"></a><span data-ttu-id="8fdbd-132">Personnaliser la cible d’URL pour les notifications dues au contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-132">Customize URL target for notifications raised by device control</span></span>

<span data-ttu-id="8fdbd-133">Lorsque la stratégie de contrôle d’appareil que vous avez mise en place est appliquée sur un appareil (par exemple, l’accès à un périphérique multimédia amovible est restreint), une notification s’affiche pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-133">When the device control policy that you have put in place is enforced on a device (for example, access to a removable media device is restricted), a notification is displayed to the user.</span></span>

![Notification de contrôle d’appareil](images/mac-device-control-notification.png)

<span data-ttu-id="8fdbd-135">Lorsque les utilisateurs finaux cliquent sur cette notification, une page web s’ouvre dans le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-135">When end users click this notification, a web page is opened in the default browser.</span></span> <span data-ttu-id="8fdbd-136">Vous pouvez configurer l’URL qui est ouverte lorsque les utilisateurs finaux cliquent sur la notification.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-136">You can configure the URL that is opened when end users click the notification.</span></span>

|<span data-ttu-id="8fdbd-137">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-137">Section</span></span>|<span data-ttu-id="8fdbd-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-138">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-139">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-139">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-140">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-140">**Key**</span></span> | <span data-ttu-id="8fdbd-141">navigationTarget</span><span class="sxs-lookup"><span data-stu-id="8fdbd-141">navigationTarget</span></span> |
| <span data-ttu-id="8fdbd-142">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-142">**Data type**</span></span> | <span data-ttu-id="8fdbd-143">String</span><span class="sxs-lookup"><span data-stu-id="8fdbd-143">String</span></span> |
| <span data-ttu-id="8fdbd-144">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-144">**Comments**</span></span> | <span data-ttu-id="8fdbd-145">S’il n’est pas défini, le produit utilise une URL par défaut pointant vers une page générique expliquant l’action entreprise par le produit.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-145">If not defined, the product uses a default URL pointing to a generic page explaining the action taken by the product.</span></span> |

### <a name="allow-or-block-removable-devices"></a><span data-ttu-id="8fdbd-146">Autoriser ou bloquer les appareils amovibles</span><span class="sxs-lookup"><span data-stu-id="8fdbd-146">Allow or block removable devices</span></span>

<span data-ttu-id="8fdbd-147">La section média amovible de la stratégie de contrôle d’appareil est utilisée pour restreindre l’accès aux médias amovibles.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-147">The removable media section of the device control policy is used to restrict access to removable media.</span></span> 

> [!NOTE]
> <span data-ttu-id="8fdbd-148">Les types de média amovible suivants sont actuellement pris en charge et peuvent être inclus dans la stratégie : les périphériques de stockage USB.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-148">The following types of removable media are currently supported and can be included in the policy: USB storage devices.</span></span>

|<span data-ttu-id="8fdbd-149">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-149">Section</span></span>|<span data-ttu-id="8fdbd-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-150">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-151">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-151">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-152">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-152">**Key**</span></span> | <span data-ttu-id="8fdbd-153">removableMediaPolicy</span><span class="sxs-lookup"><span data-stu-id="8fdbd-153">removableMediaPolicy</span></span> |
| <span data-ttu-id="8fdbd-154">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-154">**Data type**</span></span> | <span data-ttu-id="8fdbd-155">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-155">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8fdbd-156">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-156">**Comments**</span></span> | <span data-ttu-id="8fdbd-157">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-157">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="8fdbd-158">Cette section de la stratégie est hiérarchique, ce qui permet une flexibilité maximale et couvre un large éventail de cas d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-158">This section of the policy is hierarchical, allowing for maximum flexibility and covering a wide range of use cases.</span></span> <span data-ttu-id="8fdbd-159">Au niveau supérieur, les fournisseurs sont identifiés par un ID de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-159">At the top level are vendors, identified by a vendor ID.</span></span> <span data-ttu-id="8fdbd-160">Pour chaque fournisseur, il existe des produits, identifiés par un ID de produit.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-160">For each vendor, there are products, identified by a product ID.</span></span> <span data-ttu-id="8fdbd-161">Enfin, pour chaque produit, il existe des numéros de série qui notent des appareils spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-161">Finally, for each product there are serial numbers denoting specific devices.</span></span>

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

<span data-ttu-id="8fdbd-162">Pour plus d’informations sur la recherche des identificateurs d’appareil, voir [Rechercher des identificateurs d’appareil.](#look-up-device-identifiers)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-162">For information on how to find the device identifiers, see [Look up device identifiers](#look-up-device-identifiers).</span></span>

<span data-ttu-id="8fdbd-163">La stratégie est évaluée de l’entrée la plus spécifique à la plus générale.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-163">The policy is evaluated from the most specific entry to the most general one.</span></span> <span data-ttu-id="8fdbd-164">Autrement dit, lorsqu’un appareil est branché, le produit tente de trouver la correspondance la plus spécifique dans la stratégie pour chaque périphérique multimédia amovible et applique les autorisations à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-164">Meaning, when a device is plugged in, the product tries to find the most specific match in the policy for each removable media device and apply the permissions at that level.</span></span> <span data-ttu-id="8fdbd-165">En l’absence de correspondance, la meilleure correspondance suivante est appliquée, jusqu’à l’autorisation spécifiée au niveau supérieur, qui est la valeur par défaut lorsqu’un appareil ne correspond à aucune autre entrée de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-165">If there is no match, then the next best match is applied, all the way to the permission specified at the top level, which is the default when a device does not match any other entry in the policy.</span></span>

#### <a name="policy-enforcement-level"></a><span data-ttu-id="8fdbd-166">Niveau d’application de la stratégie</span><span class="sxs-lookup"><span data-stu-id="8fdbd-166">Policy enforcement level</span></span>

<span data-ttu-id="8fdbd-167">Sous la section Média amovible, il existe une option pour définir le niveau d’application, qui peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-167">Under the removable media section, there is an option to set the enforcement level, which can take one of the following values:</span></span>

- <span data-ttu-id="8fdbd-168">`audit` - Sous ce niveau d’application, si l’accès à un appareil est restreint, une notification s’affiche pour l’utilisateur, mais l’appareil peut toujours être utilisé.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-168">`audit` - Under this enforcement level, if access to a device is restricted, a notification is displayed to the user, however the device can still be used.</span></span> <span data-ttu-id="8fdbd-169">Ce niveau d’application peut être utile pour évaluer l’efficacité d’une stratégie.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-169">This enforcement level can be useful to evaluate the effectiveness of a policy.</span></span>
- <span data-ttu-id="8fdbd-170">`block` - Sous ce niveau d’application, les opérations que l’utilisateur peut effectuer sur l’appareil sont limitées à ce qui est défini dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-170">`block` - Under this enforcement level, the operations that the user can perform on the device are limited to what is defined in the policy.</span></span> <span data-ttu-id="8fdbd-171">En outre, une notification est alors avertie à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-171">Furthermore, a notification is raised to the user.</span></span> 

> [!NOTE] 
> <span data-ttu-id="8fdbd-172">Par défaut, le niveau d’application est définie sur `audit` .</span><span class="sxs-lookup"><span data-stu-id="8fdbd-172">By default, the enforcement level is set to `audit`.</span></span> 

|<span data-ttu-id="8fdbd-173">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-173">Section</span></span>|<span data-ttu-id="8fdbd-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-174">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-175">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-175">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-176">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-176">**Key**</span></span> | <span data-ttu-id="8fdbd-177">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="8fdbd-177">enforcementLevel</span></span> |
| <span data-ttu-id="8fdbd-178">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-178">**Data type**</span></span> | <span data-ttu-id="8fdbd-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8fdbd-179">String</span></span> |
| <span data-ttu-id="8fdbd-180">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-180">**Possible values**</span></span> | <span data-ttu-id="8fdbd-181">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-181">audit (default)</span></span> <br/> <span data-ttu-id="8fdbd-182">block</span><span class="sxs-lookup"><span data-stu-id="8fdbd-182">block</span></span> |

#### <a name="default-permission-level"></a><span data-ttu-id="8fdbd-183">Niveau d’autorisation par défaut</span><span class="sxs-lookup"><span data-stu-id="8fdbd-183">Default permission level</span></span>

<span data-ttu-id="8fdbd-184">Au niveau supérieur de la section Média amovible, vous pouvez configurer le niveau d’autorisation par défaut pour les appareils qui ne correspondent à rien d’autre dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-184">At the top level of the removable media section, you can configure the default permission level for devices that do not match anything else in the policy.</span></span>

<span data-ttu-id="8fdbd-185">Ce paramètre peut être définie sur :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-185">This setting can be set to:</span></span>

- <span data-ttu-id="8fdbd-186">`none` - Aucune opération ne peut être effectuée sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-186">`none` - No operations can be performed on the device</span></span>
- <span data-ttu-id="8fdbd-187">Combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-187">A combination of the following values:</span></span>
    - <span data-ttu-id="8fdbd-188">`read` - Les opérations de lecture sont autorisées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-188">`read` - Read operations are permitted on the device</span></span>
    - <span data-ttu-id="8fdbd-189">`write` - Les opérations d’écriture sont autorisées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-189">`write` - Write operations are permitted on the device</span></span>
    - <span data-ttu-id="8fdbd-190">`execute` - Les opérations d’exécution sont autorisées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-190">`execute` - Execute operations are permitted on the device</span></span>

> [!NOTE]
> <span data-ttu-id="8fdbd-191">`none`S’il est présent dans le niveau d’autorisation, toutes les autres autorisations ( ou ) sont `read` `write` `execute` ignorées.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-191">If `none` is present in the permission level, any other permissions (`read`, `write`, or `execute`) will be ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="8fdbd-192">L’autorisation fait uniquement référence à l’exécution des binaires `execute` Mach-O.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-192">The `execute` permission only refers to execution of Mach-O binaries.</span></span> <span data-ttu-id="8fdbd-193">Il n’inclut pas l’exécution de scripts ou d’autres types de charges utiles.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-193">It does not include execution of scripts or other types of payloads.</span></span>

|<span data-ttu-id="8fdbd-194">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-194">Section</span></span>|<span data-ttu-id="8fdbd-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-195">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-196">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-196">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-197">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-197">**Key**</span></span> | <span data-ttu-id="8fdbd-198">autorisation</span><span class="sxs-lookup"><span data-stu-id="8fdbd-198">permission</span></span> |
| <span data-ttu-id="8fdbd-199">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-199">**Data type**</span></span> | <span data-ttu-id="8fdbd-200">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="8fdbd-200">Array of strings</span></span> |
| <span data-ttu-id="8fdbd-201">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-201">**Possible values**</span></span> | <span data-ttu-id="8fdbd-202">aucune</span><span class="sxs-lookup"><span data-stu-id="8fdbd-202">none</span></span> <br/> <span data-ttu-id="8fdbd-203">read</span><span class="sxs-lookup"><span data-stu-id="8fdbd-203">read</span></span> <br/> <span data-ttu-id="8fdbd-204">write</span><span class="sxs-lookup"><span data-stu-id="8fdbd-204">write</span></span> <br/> <span data-ttu-id="8fdbd-205">execute</span><span class="sxs-lookup"><span data-stu-id="8fdbd-205">execute</span></span> |

#### <a name="restrict-removable-media-by-vendor-product-and-serial-number"></a><span data-ttu-id="8fdbd-206">Restreindre les médias amovibles par fournisseur, produit et numéro de série</span><span class="sxs-lookup"><span data-stu-id="8fdbd-206">Restrict removable media by vendor, product, and serial number</span></span>

<span data-ttu-id="8fdbd-207">Comme décrit dans [Autoriser](#allow-or-block-removable-devices)ou bloquer les appareils amovibles, les supports amovibles tels que les périphériques USB peuvent être identifiés par l’ID du fournisseur, l’ID de produit et le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-207">As described in [Allow or block removable devices](#allow-or-block-removable-devices), removable media such as USB devices can be identified by the vendor ID, product ID, and serial number.</span></span>

<span data-ttu-id="8fdbd-208">Au niveau supérieur de la stratégie de média amovible, vous pouvez éventuellement définir des restrictions plus précises au niveau du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-208">At the top level of the removable media policy, you can optionally define more granular restrictions at the vendor level.</span></span> 

<span data-ttu-id="8fdbd-209">Le `vendors` dictionnaire contient une ou plusieurs entrées, chaque entrée étant identifiée par l’ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-209">The `vendors` dictionary contains one or more entries, with each entry being identified by the vendor ID.</span></span>

|<span data-ttu-id="8fdbd-210">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-210">Section</span></span>|<span data-ttu-id="8fdbd-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-211">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-212">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-212">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-213">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-213">**Key**</span></span> | <span data-ttu-id="8fdbd-214">fournisseurs</span><span class="sxs-lookup"><span data-stu-id="8fdbd-214">vendors</span></span> |
| <span data-ttu-id="8fdbd-215">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-215">**Data type**</span></span> | <span data-ttu-id="8fdbd-216">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-216">Dictionary (nested preference)</span></span> |

<span data-ttu-id="8fdbd-217">Pour chaque fournisseur, vous pouvez spécifier le niveau d’autorisation souhaité pour les appareils de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-217">For each vendor, you can specify the desired permission level for devices from that vendor.</span></span>

|<span data-ttu-id="8fdbd-218">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-218">Section</span></span>|<span data-ttu-id="8fdbd-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-219">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-220">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-220">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-221">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-221">**Key**</span></span> | <span data-ttu-id="8fdbd-222">autorisation</span><span class="sxs-lookup"><span data-stu-id="8fdbd-222">permission</span></span> |
| <span data-ttu-id="8fdbd-223">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-223">**Data type**</span></span> | <span data-ttu-id="8fdbd-224">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="8fdbd-224">Array of strings</span></span> |
| <span data-ttu-id="8fdbd-225">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-225">**Possible values**</span></span> | <span data-ttu-id="8fdbd-226">Identique au [niveau d’autorisation Par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-226">Same as [Default permission level](#default-permission-level)</span></span> |

<span data-ttu-id="8fdbd-227">En outre, vous pouvez éventuellement spécifier l’ensemble des produits appartenant à ce fournisseur pour lesquels des autorisations plus granulaires sont définies.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-227">Furthermore, you can optionally specify the set of products belonging to that vendor for which more granular permissions are defined.</span></span> <span data-ttu-id="8fdbd-228">Le dictionnaire contient une ou plusieurs entrées, chaque entrée étant identifiée par `products` l’ID de produit.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-228">The `products` dictionary contains one or more entries, with each entry being identified by the product ID.</span></span> 

|<span data-ttu-id="8fdbd-229">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-229">Section</span></span>|<span data-ttu-id="8fdbd-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-230">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-231">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-231">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-232">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-232">**Key**</span></span> | <span data-ttu-id="8fdbd-233">produits</span><span class="sxs-lookup"><span data-stu-id="8fdbd-233">products</span></span> |
| <span data-ttu-id="8fdbd-234">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-234">**Data type**</span></span> | <span data-ttu-id="8fdbd-235">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-235">Dictionary (nested preference)</span></span> |

<span data-ttu-id="8fdbd-236">Pour chaque produit, vous pouvez spécifier le niveau d’autorisation souhaité pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-236">For each product, you can specify the desired permission level for that product.</span></span>

|<span data-ttu-id="8fdbd-237">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-237">Section</span></span>|<span data-ttu-id="8fdbd-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-238">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-239">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-239">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-240">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-240">**Key**</span></span> | <span data-ttu-id="8fdbd-241">autorisation</span><span class="sxs-lookup"><span data-stu-id="8fdbd-241">permission</span></span> |
| <span data-ttu-id="8fdbd-242">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-242">**Data type**</span></span> | <span data-ttu-id="8fdbd-243">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="8fdbd-243">Array of strings</span></span> |
| <span data-ttu-id="8fdbd-244">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-244">**Possible values**</span></span> | <span data-ttu-id="8fdbd-245">Identique au [niveau d’autorisation Par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-245">Same as [Default permission level](#default-permission-level)</span></span> |

<span data-ttu-id="8fdbd-246">En outre, vous pouvez spécifier un ensemble facultatif de numéros de série pour lesquels des autorisations plus granulaires sont définies.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-246">Furthermore, you can specify an optional set of serial numbers for which more granular permissions are defined.</span></span>

<span data-ttu-id="8fdbd-247">Le dictionnaire contient une ou plusieurs entrées, chaque entrée étant `serialNumbers` identifiée par le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-247">The `serialNumbers` dictionary contains one or more entries, with each entry being identified by the serial number.</span></span>

|<span data-ttu-id="8fdbd-248">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-248">Section</span></span>|<span data-ttu-id="8fdbd-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-249">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-250">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-250">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-251">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-251">**Key**</span></span> | <span data-ttu-id="8fdbd-252">serialNumbers</span><span class="sxs-lookup"><span data-stu-id="8fdbd-252">serialNumbers</span></span> |
| <span data-ttu-id="8fdbd-253">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-253">**Data type**</span></span> | <span data-ttu-id="8fdbd-254">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-254">Dictionary (nested preference)</span></span> |

<span data-ttu-id="8fdbd-255">Pour chaque numéro de série, vous pouvez spécifier le niveau d’autorisation souhaité.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-255">For each serial number, you can specify the desired permission level.</span></span>

|<span data-ttu-id="8fdbd-256">Section</span><span class="sxs-lookup"><span data-stu-id="8fdbd-256">Section</span></span>|<span data-ttu-id="8fdbd-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fdbd-257">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8fdbd-258">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-258">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8fdbd-259">**Key**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-259">**Key**</span></span> | <span data-ttu-id="8fdbd-260">autorisation</span><span class="sxs-lookup"><span data-stu-id="8fdbd-260">permission</span></span> |
| <span data-ttu-id="8fdbd-261">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-261">**Data type**</span></span> | <span data-ttu-id="8fdbd-262">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="8fdbd-262">Array of strings</span></span> |
| <span data-ttu-id="8fdbd-263">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-263">**Possible values**</span></span> | <span data-ttu-id="8fdbd-264">Identique au [niveau d’autorisation Par défaut](#default-permission-level)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-264">Same as [Default permission level](#default-permission-level)</span></span> |

#### <a name="example-device-control-policy"></a><span data-ttu-id="8fdbd-265">Exemple de stratégie de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-265">Example device control policy</span></span>

<span data-ttu-id="8fdbd-266">L’exemple suivant montre comment tous les concepts ci-dessus peuvent être combinés en une stratégie de contrôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-266">The following example shows how all of the above concepts can be combined into a device control policy.</span></span> <span data-ttu-id="8fdbd-267">Dans l’exemple suivant, notez la nature hiérarchique de la stratégie de média amovible.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-267">In the following example, note the hierarchical nature of the removable media policy.</span></span>

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

<span data-ttu-id="8fdbd-268">Nous avons inclus d’autres exemples de stratégies de contrôle d’appareil dans les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-268">We have included more examples of device control policies in the following documents:</span></span>

- [<span data-ttu-id="8fdbd-269">Exemples de stratégies de contrôle d’appareil pour Intune</span><span class="sxs-lookup"><span data-stu-id="8fdbd-269">Examples of device control policies for Intune</span></span>](mac-device-control-intune.md)
- [<span data-ttu-id="8fdbd-270">Exemples de stratégies de contrôle d’appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="8fdbd-270">Examples of device control policies for JAMF</span></span>](mac-device-control-jamf.md)

#### <a name="look-up-device-identifiers"></a><span data-ttu-id="8fdbd-271">Rechercher des identificateurs d’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-271">Look up device identifiers</span></span>

<span data-ttu-id="8fdbd-272">Pour rechercher l’ID du fournisseur, l’ID de produit et le numéro de série d’un périphérique USB :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-272">To find the vendor ID, product ID, and serial number of a USB device:</span></span>

1. <span data-ttu-id="8fdbd-273">Connectez-vous à un appareil Mac.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-273">Log into a Mac device.</span></span>
1. <span data-ttu-id="8fdbd-274">Branchez le périphérique USB pour lequel vous souhaitez rechercher les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-274">Plug in the USB device for which you want to look up the identifiers.</span></span>
1. <span data-ttu-id="8fdbd-275">Dans le menu de niveau supérieur de macOS, sélectionnez **À propos de ce Mac.**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-275">In the top-level menu of macOS, select **About This Mac**.</span></span>

    ![À propos de ce Mac](images/mac-device-control-lookup-1.png)

1. <span data-ttu-id="8fdbd-277">Sélectionnez **Rapport système**.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-277">Select **System Report**.</span></span>

    ![Rapport système](images/mac-device-control-lookup-2.png)

1. <span data-ttu-id="8fdbd-279">Dans la colonne de gauche, sélectionnez **USB.**</span><span class="sxs-lookup"><span data-stu-id="8fdbd-279">From the left column, select **USB**.</span></span>

    ![Affichage de tous les périphériques USB](images/mac-device-control-lookup-3.png)

1. <span data-ttu-id="8fdbd-281">Sous **Arborescence d’appareils USB,** accédez à l’appareil USB que vous avez branché.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-281">Under **USB Device Tree**, navigate to the USB device that you plugged in.</span></span>

    ![Détails d’un périphérique USB](images/mac-device-control-lookup-4.png)

1. <span data-ttu-id="8fdbd-283">L’ID de fournisseur, l’ID de produit et le numéro de série sont affichés.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-283">The vendor ID, product ID, and serial number are displayed.</span></span> <span data-ttu-id="8fdbd-284">Lorsque vous ajoutez l’ID fournisseur et l’ID de produit à la stratégie de média amovible, vous devez uniquement ajouter la partie après `0x` .</span><span class="sxs-lookup"><span data-stu-id="8fdbd-284">When adding the vendor ID and product ID to the removable media policy, you must only add the part after `0x`.</span></span> <span data-ttu-id="8fdbd-285">Par exemple, dans l’image ci-dessous, l’ID du fournisseur `1000` est et l’ID de produit est `090c` .</span><span class="sxs-lookup"><span data-stu-id="8fdbd-285">For example, in the below image, vendor ID is `1000` and product ID is `090c`.</span></span>

#### <a name="discover-usb-devices-in-your-organization"></a><span data-ttu-id="8fdbd-286">Découvrir les périphériques USB de votre organisation</span><span class="sxs-lookup"><span data-stu-id="8fdbd-286">Discover USB devices in your organization</span></span>

<span data-ttu-id="8fdbd-287">Vous pouvez afficher les événements de montage, de démontage et de modification de volume provenant de périphériques USB dans Microsoft Defender pour le recherche avancée de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-287">You can view mount, unmount, and volume change events originating from USB devices in Microsoft Defender for Endpoint advanced hunting.</span></span> <span data-ttu-id="8fdbd-288">Ces événements peuvent être utiles pour identifier une activité d’utilisation suspecte ou effectuer des enquêtes internes.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-288">These events can be helpful to identify suspicious usage activity or perform internal investigations.</span></span>

```
DeviceEvents 
    | where ActionType == "UsbDriveMounted" or ActionType == "UsbDriveUnmounted" or ActionType == "UsbDriveDriveLetterChanged"
    | where DeviceId == "<device ID>"
```

## <a name="device-control-policy-deployment"></a><span data-ttu-id="8fdbd-289">Déploiement de stratégie de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="8fdbd-289">Device control policy deployment</span></span>

<span data-ttu-id="8fdbd-290">La stratégie de contrôle d’appareil doit être incluse en plus des autres paramètres du produit, comme décrit dans Définir les préférences de [Microsoft Defender pour endpoint sur macOS.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-290">The device control policy must be included next to the other product settings, as described in [Set preferences for Microsoft Defender for Endpoint on macOS](mac-preferences.md).</span></span>

<span data-ttu-id="8fdbd-291">Ce profil peut être déployé à l’aide des instructions répertoriées dans le déploiement de [profil de configuration.](mac-preferences.md#configuration-profile-deployment)</span><span class="sxs-lookup"><span data-stu-id="8fdbd-291">This profile can be deployed using the instructions listed in [Configuration profile deployment](mac-preferences.md#configuration-profile-deployment).</span></span>

## <a name="troubleshooting-tips"></a><span data-ttu-id="8fdbd-292">Conseils de dépannage</span><span class="sxs-lookup"><span data-stu-id="8fdbd-292">Troubleshooting tips</span></span>

<span data-ttu-id="8fdbd-293">Après avoir lancé le profil de configuration via Intune ou JAMF, vous pouvez vérifier s’il a été correctement choisi par le produit en exécutant la commande suivante à partir du Terminal :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-293">After pushing the configuration profile through Intune or JAMF, you can check if it was successfully picked up by the product by running the following command from the Terminal:</span></span>

```bash
mdatp device-control removable-media policy list
```

<span data-ttu-id="8fdbd-294">Cette commande imprime en sortie standard la stratégie de contrôle d’appareil que le produit utilise.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-294">This command will print to standard output the device control policy that the product is using.</span></span> <span data-ttu-id="8fdbd-295">Dans le cas où cela imprime, assurez-vous (a) que le profil de configuration a bien été poussée sur votre appareil à partir de la console de gestion et (b) qu’il s’agit d’une stratégie de contrôle d’appareil valide, comme décrit dans ce `Policy is empty` document.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-295">In case this prints `Policy is empty`, make sure that (a) the configuration profile has indeed been pushed to your device from the management console, and (b) it is a valid device control policy, as described in this document.</span></span>

<span data-ttu-id="8fdbd-296">Sur un appareil sur lequel la stratégie a été correctement livrée et où un ou plusieurs appareils sont branchés, vous pouvez exécuter la commande suivante pour lister tous les appareils et les autorisations effectives qui leur sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-296">On a device where the policy has been delivered successfully and where there are one or more devices plugged in, you can run the following command to list all devices and the effective permissions applied to them.</span></span>

```bash
mdatp device-control removable-media devices list
```

<span data-ttu-id="8fdbd-297">Exemple de sortie :</span><span class="sxs-lookup"><span data-stu-id="8fdbd-297">Example of output:</span></span>

```Output
.Device(s)
|-o Name: Untitled 1, Permission ["read", "execute"]
| |-o Vendor: General "fff0"
| |-o Product: USB Flash Disk "1000"
| |-o Serial number: "04ZSSMHI2O7WBVOA"
| |-o Mount point: "/Volumes/TESTUSB"
```

<span data-ttu-id="8fdbd-298">Dans l’exemple ci-dessus, il n’existe qu’un seul périphérique multimédia amovible branché et il dispose d’autorisations et d’autorisations, conformément à la stratégie de contrôle d’appareil qui a été remis à `read` `execute` l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8fdbd-298">In the above example, there is only one removable media device plugged in and it has `read` and `execute` permissions, according to the device control policy that was delivered to the device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fdbd-299">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fdbd-299">Related topics</span></span>

- [<span data-ttu-id="8fdbd-300">Exemples de stratégies de contrôle d’appareil pour Intune</span><span class="sxs-lookup"><span data-stu-id="8fdbd-300">Examples of device control policies for Intune</span></span>](mac-device-control-intune.md)
- [<span data-ttu-id="8fdbd-301">Exemples de stratégies de contrôle d’appareil pour JAMF</span><span class="sxs-lookup"><span data-stu-id="8fdbd-301">Examples of device control policies for JAMF</span></span>](mac-device-control-jamf.md)
