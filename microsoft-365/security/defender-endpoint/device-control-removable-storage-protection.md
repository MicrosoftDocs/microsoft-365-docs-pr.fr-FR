---
title: Microsoft Defender for Endpoint Device Control Removable Stockage Protection
description: Comprendre les fonctionnalités qui empêchent l’utilisateur ou l’ordinateur ou les deux d’utiliser un support de stockage amovible non autorisé
keywords: support de stockage amovible
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: v-smandalika
author: v-smandalika
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: c9b97c2157ba8090628af23b2ab54cf38f04d8c6
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538386"
---
# <a name="microsoft-defender-for-endpoint-device-control-removable-storage-protection"></a><span data-ttu-id="7d589-104">Microsoft Defender for Endpoint Device Control Removable Stockage Protection</span><span class="sxs-lookup"><span data-stu-id="7d589-104">Microsoft Defender for Endpoint Device Control Removable Storage Protection</span></span>

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="7d589-105">Microsoft Defender pour endpoint Device Control Removable Stockage Protection empêche l’utilisateur ou l’ordinateur ou les deux d’utiliser un support de stockage amovible non autorisé.</span><span class="sxs-lookup"><span data-stu-id="7d589-105">Microsoft Defender for Endpoint Device Control Removable Storage Protection prevents user or machine or both from using unauthorized removable storage media.</span></span>

## <a name="protection-policies"></a><span data-ttu-id="7d589-106">Stratégies de protection</span><span class="sxs-lookup"><span data-stu-id="7d589-106">Protection policies</span></span>

### <a name="device-installation"></a><span data-ttu-id="7d589-107">Installation de l’appareil</span><span class="sxs-lookup"><span data-stu-id="7d589-107">Device installation</span></span>

<span data-ttu-id="7d589-108">**Fonctionnalités** : empêcher l’installation avec ou sans exclusion basée sur différentes propriétés d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7d589-108">**Capabilities** - Prevent installation with or without exclusion based on various device properties.</span></span>

<span data-ttu-id="7d589-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d589-109">**Description**</span></span>
- <span data-ttu-id="7d589-110">Appliqué au niveau de l’ordinateur : la même stratégie s’applique à tout utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7d589-110">Applied at machine level: the same policy applies for any logged on user.</span></span>
- <span data-ttu-id="7d589-111">Prend en charge mem et GPO.</span><span class="sxs-lookup"><span data-stu-id="7d589-111">Supports MEM and GPO.</span></span>
- <span data-ttu-id="7d589-112">Propriétés[d’appareil « pris](#device-properties)en charge » comme répertoriés.</span><span class="sxs-lookup"><span data-stu-id="7d589-112">Supported  ‘[Device Properties](#device-properties)’ as listed.</span></span>
- <span data-ttu-id="7d589-113">Pour plus d’informations Windows, voir Comment contrôler des périphériques USB et d’autres supports amovibles à l’aide de [Microsoft Defender for Endpoint](control-usb-devices-using-intune.md).</span><span class="sxs-lookup"><span data-stu-id="7d589-113">For more information on Windows, see [How to control USB devices and other removable media using Microsoft Defender for Endpoint](control-usb-devices-using-intune.md).</span></span>

<span data-ttu-id="7d589-114">**Plateforme prise en charge** : Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d589-114">**Supported Platform** - Windows 10</span></span>

<span data-ttu-id="7d589-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d589-115">**Description**</span></span>
- <span data-ttu-id="7d589-116">Appliqué au niveau de l’ordinateur : la même stratégie s’applique à tout utilisateur connecté</span><span class="sxs-lookup"><span data-stu-id="7d589-116">Applied at machine level: the same policy applies for any logged on user</span></span>
- <span data-ttu-id="7d589-117">Pour obtenir des informations spécifiques à macOS, voir [Contrôle d’appareil pour macOS.](mac-device-control-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7d589-117">For macOS specific information, see [Device control for macOS](mac-device-control-overview.md).</span></span>
 
<span data-ttu-id="7d589-118">**Plateforme prise en** charge : macOS Contrôle 10.15.4+ (avec extensions système activées)</span><span class="sxs-lookup"><span data-stu-id="7d589-118">**Supported platform** - macOS Catalina 10.15.4+ (with system extensions enabled)</span></span>

### <a name="removable-storage-access-control"></a><span data-ttu-id="7d589-119">Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-119">Removable storage Access Control</span></span>

<span data-ttu-id="7d589-120">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="7d589-120">**Capabilities**</span></span>
- <span data-ttu-id="7d589-121">*Audit* Accès en lecture ou en écriture ou en exécution au stockage amovible en fonction de différentes propriétés d’appareil, avec ou sans exclusion.</span><span class="sxs-lookup"><span data-stu-id="7d589-121">*Audit* Read or Write or Execute access to removable storage based on various device properties, with or without an exclusion.</span></span>
- <span data-ttu-id="7d589-122">*Empêcher* Accès en lecture ou en écriture ou exécution avec ou sans exclusion : autorisez un appareil spécifique en fonction de différentes propriétés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7d589-122">*Prevent* Read or Write or Execute access with or without an exclusion - Allow specific device based on various device properties.</span></span>

<span data-ttu-id="7d589-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d589-123">**Description**</span></span>
- <span data-ttu-id="7d589-124">Appliqué à l’ordinateur ou à l’utilisateur ou aux deux : autorise uniquement des personnes spécifiques qui effectuent un accès en lecture/écriture/exécution à un stockage amovible spécifique sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="7d589-124">Applied at either machine or user or both – only allow specific people performing Read/Write/Execute access to specific removable storage on specific machine.</span></span>
- <span data-ttu-id="7d589-125">Prise en charge de MEM OMA-URI et GPO.</span><span class="sxs-lookup"><span data-stu-id="7d589-125">Support MEM OMA-URI and GPO.</span></span>
- <span data-ttu-id="7d589-126">Propriétés[d’appareil « pris](#device-properties)en charge » comme répertoriés.</span><span class="sxs-lookup"><span data-stu-id="7d589-126">Supported  ‘[Device Properties](#device-properties)’ as listed.</span></span>
- <span data-ttu-id="7d589-127">Pour plus d’Windows, voir [Contrôle d’accès au stockage amovible.](device-control-removable-storage-access-control.md)</span><span class="sxs-lookup"><span data-stu-id="7d589-127">For feature in Windows, see [Removable storage Access Control](device-control-removable-storage-access-control.md).</span></span>

<span data-ttu-id="7d589-128">**Plateforme prise en charge** : Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d589-128">**Supported Platform** - Windows 10</span></span>

<span data-ttu-id="7d589-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d589-129">**Description**</span></span>
- <span data-ttu-id="7d589-130">Appliqué au niveau de l’ordinateur : la même stratégie s’applique à tout utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7d589-130">Applied at machine level: the same policy applies for any logged on user.</span></span>
- <span data-ttu-id="7d589-131">Pour obtenir des informations spécifiques à macOS, voir [Contrôle d’appareil pour macOS.](mac-device-control-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7d589-131">For macOS specific information, see [Device control for macOS](mac-device-control-overview.md).</span></span>
 
<span data-ttu-id="7d589-132">**Plateforme prise en** charge : macOS Contrôle 10.15.4+ (avec extensions système activées)</span><span class="sxs-lookup"><span data-stu-id="7d589-132">**Supported platform** - macOS Catalina 10.15.4+ (with system extensions enabled)</span></span>

### <a name="windows-portable-device-access-control"></a><span data-ttu-id="7d589-133">Windows Contrôle d’accès des appareils portables</span><span class="sxs-lookup"><span data-stu-id="7d589-133">Windows Portable Device Access Control</span></span>

<span data-ttu-id="7d589-134">**Fonctionnalités** : refuser l’accès en lecture ou en écriture à [Windows’appareil portable,](/windows-hardware/drivers/portable/)par exemple : tablette, iPhone.</span><span class="sxs-lookup"><span data-stu-id="7d589-134">**Capabilities** - Deny Read or Write access to any [Windows Portable Device](/windows-hardware/drivers/portable/), for example: Tablet, iPhone.</span></span>

<span data-ttu-id="7d589-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d589-135">**Description**</span></span>
- <span data-ttu-id="7d589-136">Appliqué à l’ordinateur ou à l’utilisateur ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="7d589-136">Applied at either machine or user or both.</span></span>
- <span data-ttu-id="7d589-137">Prise en charge de MEM OMA-URI et GPO.</span><span class="sxs-lookup"><span data-stu-id="7d589-137">Support MEM OMA-URI and GPO.</span></span>

<span data-ttu-id="7d589-138">**Plateforme prise en charge** : Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d589-138">**Supported Platform** - Windows 10</span></span>

### <a name="endpoint-dlp-removable-storage"></a><span data-ttu-id="7d589-139">Point de terminaison de stockage amovible DLP</span><span class="sxs-lookup"><span data-stu-id="7d589-139">Endpoint DLP Removable storage</span></span>

<span data-ttu-id="7d589-140">**Fonctionnalités** : auditer ou avertir ou empêcher un utilisateur de copier un élément ou des informations sur un support amovible ou un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="7d589-140">**Capabilities** - Audit or Warn or Prevent a user from copying an item or information to removable media or USB device.</span></span>

<span data-ttu-id="7d589-141">**Description** : pour plus d’informations sur Windows, consultez la Microsoft 365 protection contre la perte de données de point [de terminaison.](../../compliance/endpoint-dlp-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="7d589-141">**Description** - For more information on Windows, see [Learn about Microsoft 365 Endpoint data loss prevention](../../compliance/endpoint-dlp-learn-about.md).</span></span>

<span data-ttu-id="7d589-142">**Plateforme prise en charge** : Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d589-142">**Supported Platform** - Windows 10</span></span>

### <a name="bitlocker"></a><span data-ttu-id="7d589-143">BitLocker</span><span class="sxs-lookup"><span data-stu-id="7d589-143">BitLocker</span></span> 

<span data-ttu-id="7d589-144">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="7d589-144">**Capabilities**</span></span>
- <span data-ttu-id="7d589-145">Bloquez les données à écrire sur les lecteurs amovibles qui ne sont BitLocker protégé.</span><span class="sxs-lookup"><span data-stu-id="7d589-145">Block data to be written to removable drives that aren't BitLocker protected.</span></span>
- <span data-ttu-id="7d589-146">Bloquer l’accès aux lecteurs amovibles, sauf s’ils ont été chiffrés sur un ordinateur de votre organisation</span><span class="sxs-lookup"><span data-stu-id="7d589-146">Block access to removable drives unless they were encrypted on a computer owned by your organization</span></span>
 
<span data-ttu-id="7d589-147">**Description** - Pour plus d’informations sur Windows, voir [BitLocker – Paramètres](/mem/intune/protect/endpoint-security-disk-encryption-profile-settings).</span><span class="sxs-lookup"><span data-stu-id="7d589-147">**Description** - For more information on Windows, see [BitLocker – Removable Drive Settings](/mem/intune/protect/endpoint-security-disk-encryption-profile-settings).</span></span>

<span data-ttu-id="7d589-148">**Plateforme prise en charge** : Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d589-148">**Supported Platform** - Windows 10</span></span>

## <a name="device-properties"></a><span data-ttu-id="7d589-149">Propriétés des appareils</span><span class="sxs-lookup"><span data-stu-id="7d589-149">Device properties</span></span>

<span data-ttu-id="7d589-150">Microsoft Defender pour endpoint Device Control Removable Stockage Protection vous permet de restreindre l’accès au stockage amovible en fonction des propriétés décrites dans le tableau ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7d589-150">Microsoft Defender for Endpoint Device Control Removable Storage Protection allows you to restrict the removable storage access based on the properties described in the table below:</span></span>


|<span data-ttu-id="7d589-151">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="7d589-151">Property Name</span></span>  |<span data-ttu-id="7d589-152">Stratégies applicables</span><span class="sxs-lookup"><span data-stu-id="7d589-152">Applicable Policies</span></span>  |<span data-ttu-id="7d589-153">S’applique aux systèmes d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7d589-153">Applies to Operating Systems</span></span>  |<span data-ttu-id="7d589-154">Description</span><span class="sxs-lookup"><span data-stu-id="7d589-154">Description</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="7d589-155">Classe Device</span><span class="sxs-lookup"><span data-stu-id="7d589-155">Device Class</span></span>    |     [<span data-ttu-id="7d589-156">Comment contrôler des périphériques USB et d’autres supports amovibles à l’aide de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7d589-156">How to control USB devices and other removable media using Microsoft Defender for Endpoint</span></span>](control-usb-devices-using-intune.md)     |   <span data-ttu-id="7d589-157">Windows</span><span class="sxs-lookup"><span data-stu-id="7d589-157">Windows</span></span>      |  <span data-ttu-id="7d589-158">Pour plus d’informations sur les formats d’ID d’appareil, voir [la classe d’installation de l’appareil.](/windows-hardware/drivers/install/system-defined-device-setup-classes-available-to-vendors)</span><span class="sxs-lookup"><span data-stu-id="7d589-158">For information about Device ID formats, see [device setup class](/windows-hardware/drivers/install/system-defined-device-setup-classes-available-to-vendors).</span></span> <span data-ttu-id="7d589-159">**Remarque**: l’installation de l’appareil peut être appliquée à n’importe quel appareil, pas seulement au stockage amovible.</span><span class="sxs-lookup"><span data-stu-id="7d589-159">**Note**: Device Installation can be applied to any devices, not only Removable storage.</span></span>       |
|<span data-ttu-id="7d589-160">ID principal</span><span class="sxs-lookup"><span data-stu-id="7d589-160">Primary ID</span></span>   |     <span data-ttu-id="7d589-161">Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-161">Removable storage Access Control</span></span>    |   <span data-ttu-id="7d589-162">Windows</span><span class="sxs-lookup"><span data-stu-id="7d589-162">Windows</span></span>      |      <span data-ttu-id="7d589-163">L’ID principal inclut le stockage amovible et le CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="7d589-163">The Primary ID includes removable storage and CD/DVD.</span></span>   |
|<span data-ttu-id="7d589-164">ID d’appareil</span><span class="sxs-lookup"><span data-stu-id="7d589-164">Device ID</span></span>     |  <span data-ttu-id="7d589-165">Comment contrôler les périphériques USB et autres supports amovibles à [l’aide de Microsoft Defender pour endpoint](control-usb-devices-using-intune.md); Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-165">[How to control USB devices and other removable media using Microsoft Defender for Endpoint](control-usb-devices-using-intune.md); Removable storage Access Control</span></span>       |      <span data-ttu-id="7d589-166">Windows</span><span class="sxs-lookup"><span data-stu-id="7d589-166">Windows</span></span>   |    <span data-ttu-id="7d589-167">Pour plus d’informations sur les formats d’ID d’appareil, voir Identificateurs [USB](/windows-hardware/drivers/install/standard-usb-identifiers)standard, par exemple, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07</span><span class="sxs-lookup"><span data-stu-id="7d589-167">For information about Device ID formats, see [Standard USB Identifiers](/windows-hardware/drivers/install/standard-usb-identifiers), for example, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07</span></span>      |
|<span data-ttu-id="7d589-168">ID matériel</span><span class="sxs-lookup"><span data-stu-id="7d589-168">Hardware ID</span></span>     |     <span data-ttu-id="7d589-169">Comment contrôler les périphériques USB et autres supports amovibles à [l’aide de Microsoft Defender pour endpoint](control-usb-devices-using-intune.md); Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-169">[How to control USB devices and other removable media using Microsoft Defender for Endpoint](control-usb-devices-using-intune.md); Removable storage Access Control</span></span>    |     <span data-ttu-id="7d589-170">Windows</span><span class="sxs-lookup"><span data-stu-id="7d589-170">Windows</span></span>    |    <span data-ttu-id="7d589-171">Une chaîne a identifié l’appareil dans le système, par exemple USBSTOR\DiskGeneric_Flash_Disk______8.07 ; **Remarque**: l’ID matériel n’est pas unique ; différents appareils peuvent partager la même valeur.</span><span class="sxs-lookup"><span data-stu-id="7d589-171">A string identified the device in the system, for example, USBSTOR\DiskGeneric_Flash_Disk______8.07; **Note**: Hardware ID is not unique; different devices may share same value.</span></span>|
|<span data-ttu-id="7d589-172">ID d’instance</span><span class="sxs-lookup"><span data-stu-id="7d589-172">Instance ID</span></span>    | <span data-ttu-id="7d589-173">Installation de l’appareil ; Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-173">Device Installation; Removable storage Access Control</span></span>     |     <span data-ttu-id="7d589-174">Windows</span><span class="sxs-lookup"><span data-stu-id="7d589-174">Windows</span></span>    |   <span data-ttu-id="7d589-175">Une chaîne identifie de manière unique l’appareil dans le système, par exemple USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611&0</span><span class="sxs-lookup"><span data-stu-id="7d589-175">A string uniquely identifies the device in the system, for example, USBSTOR\DISK&VEN_GENERIC&PROD_FLASH_DISK&REV_8.07\8735B611&0</span></span>      |
|<span data-ttu-id="7d589-176">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="7d589-176">Friendly Name</span></span>     |     <span data-ttu-id="7d589-177">Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-177">Removable storage Access Control</span></span>    |   <span data-ttu-id="7d589-178">Windows</span><span class="sxs-lookup"><span data-stu-id="7d589-178">Windows</span></span>      |    <span data-ttu-id="7d589-179">Chaîne attachée à l’appareil, par exemple, périphérique USB de disque mémoire générique</span><span class="sxs-lookup"><span data-stu-id="7d589-179">A string attached to the device, for example, Generic Flash Disk USB Device</span></span>     |
|<span data-ttu-id="7d589-180">ID fournisseur/ID de produit</span><span class="sxs-lookup"><span data-stu-id="7d589-180">Vendor ID / Product ID</span></span>     |  <span data-ttu-id="7d589-181">Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-181">Removable storage Access Control</span></span>       |   <span data-ttu-id="7d589-182">Windows Mac</span><span class="sxs-lookup"><span data-stu-id="7d589-182">Windows Mac</span></span>      |     <span data-ttu-id="7d589-183">L’ID de fournisseur est le code fournisseur à quatre chiffres que le comité USB affecte au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7d589-183">Vendor ID is the four-digit vendor code that the USB committee assigns to the vendor.</span></span> <span data-ttu-id="7d589-184">L’ID de produit est le code de produit à quatre chiffres que le fournisseur affecte à l’appareil . Prise en charge des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="7d589-184">Product ID is the four-digit product code that the vendor assigns to the device; Support wildcard.</span></span>    |
|<span data-ttu-id="7d589-185">Serial NumberId</span><span class="sxs-lookup"><span data-stu-id="7d589-185">Serial NumberId</span></span>     |     <span data-ttu-id="7d589-186">Contrôle d’accès au stockage amovible</span><span class="sxs-lookup"><span data-stu-id="7d589-186">Removable storage Access Control</span></span>    |      <span data-ttu-id="7d589-187">Windows Mac</span><span class="sxs-lookup"><span data-stu-id="7d589-187">Windows Mac</span></span>   |     <span data-ttu-id="7d589-188">Par exemple, <SerialNumberId>002324B534BCB431B000058A</SerialNumberId></span><span class="sxs-lookup"><span data-stu-id="7d589-188">For example, <SerialNumberId>002324B534BCB431B000058A</SerialNumberId></span></span>    |

## <a name="related-topic"></a><span data-ttu-id="7d589-189">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="7d589-189">Related topic</span></span>

- [<span data-ttu-id="7d589-190">Contrôle d’appareil amovible Microsoft Defender for Endpoint Stockage Access Control</span><span class="sxs-lookup"><span data-stu-id="7d589-190">Microsoft Defender for Endpoint Device Control Removable Storage Access Control</span></span>](device-control-removable-storage-access-control.md)

