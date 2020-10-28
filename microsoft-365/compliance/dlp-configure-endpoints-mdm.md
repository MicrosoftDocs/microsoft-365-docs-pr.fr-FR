---
title: Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles
f1.keywords: NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Utilisez les outils de gestion des appareils mobiles pour déployer le package de configuration sur les appareils de sorte qu’ils soient intégrés au service.
ms.openlocfilehash: 1480c918589a1f00e00ceb1233e9a62887ccff32
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769434"
---
# <a name="onboard-windows-10-devices-using-mobile-device-management-tools"></a><span data-ttu-id="e853c-103">Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="e853c-103">Onboard Windows 10 devices using Mobile Device Management tools</span></span>

<span data-ttu-id="e853c-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e853c-104">**Applies to:**</span></span>

- [<span data-ttu-id="e853c-105">Microsoft 365 protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="e853c-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)

<span data-ttu-id="e853c-106">Vous pouvez utiliser les solutions MDM (Mobile Device Management) pour configurer des appareils.</span><span class="sxs-lookup"><span data-stu-id="e853c-106">You can use mobile device management (MDM) solutions to configure devices.</span></span> <span data-ttu-id="e853c-107">Microsoft 365 Endpoint Data Loss Prevention prend en charge MDMs en fournissant OMA-URIs pour créer des stratégies de gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="e853c-107">Microsoft 365 Endpoint data loss prevention supports MDMs by providing OMA-URIs to create policies to manage devices.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="e853c-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e853c-108">Before you begin</span></span>
<span data-ttu-id="e853c-109">Si vous utilisez Microsoft Intune, vous devez avoir déployé Device MDM.</span><span class="sxs-lookup"><span data-stu-id="e853c-109">If you're using Microsoft Intune, you must have the device MDM Enrolled.</span></span> <span data-ttu-id="e853c-110">Dans le cas contraire, les paramètres ne seront pas appliqués.</span><span class="sxs-lookup"><span data-stu-id="e853c-110">Otherwise, settings will not be applied successfully.</span></span> 

<span data-ttu-id="e853c-111">Pour plus d’informations sur l’activation de MDM avec Microsoft Intune, reportez-vous à la rubrique [inscrire des appareils (Microsoft Intune)](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment).</span><span class="sxs-lookup"><span data-stu-id="e853c-111">For more information on enabling MDM with Microsoft Intune, see [Device enrollment (Microsoft Intune)](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment).</span></span>

## <a name="onboard-devices-using-microsoft-intune"></a><span data-ttu-id="e853c-112">Périphériques intégrés à l’aide de Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="e853c-112">Onboard devices using Microsoft Intune</span></span>

<span data-ttu-id="e853c-113">Suivez les instructions de [Intune](https://docs.microsoft.com/intune/advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="e853c-113">Follow the instructions from [Intune](https://docs.microsoft.com/intune/advanced-threat-protection).</span></span>

> [!NOTE]
> - <span data-ttu-id="e853c-114">L' **État d’intégrité de la stratégie des appareils intégrés** utilise des propriétés en lecture seule et ne peut pas être résolu.</span><span class="sxs-lookup"><span data-stu-id="e853c-114">The **Health Status for onboarded devices** policy uses read-only properties and can't be remediated.</span></span>

## <a name="offboard-and-monitor-devices-using-mobile-device-management-tools"></a><span data-ttu-id="e853c-115">Débarquement et surveillance des périphériques à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="e853c-115">Offboard and monitor devices using Mobile Device Management tools</span></span>

<span data-ttu-id="e853c-116">Pour des raisons de sécurité, le package utilisé pour les appareils débarquement expire 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e853c-116">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="e853c-117">Les packages par débarquement expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="e853c-117">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="e853c-118">Lors du téléchargement d’un package par débarquement, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="e853c-118">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="e853c-119">Les stratégies d’intégration et de par débarquement ne doivent pas être déployées sur le même appareil simultanément, sinon cette opération entraîne des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="e853c-119">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="e853c-120">Obtenir le package par débarquement à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="e853c-120">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com/).</span></span>

2. <span data-ttu-id="e853c-121">Dans le volet de navigation, sélectionnez **paramètres** d'  >  **intégration d’appareil**  >  **par débarquement** .</span><span class="sxs-lookup"><span data-stu-id="e853c-121">In the navigation pane, select **Settings** > **Device onboarding** > **Offboarding** .</span></span>

3. <span data-ttu-id="e853c-122">Dans le champ **méthode de déploiement** , sélectionnez gestion des **appareils mobiles/Microsoft Intune** .</span><span class="sxs-lookup"><span data-stu-id="e853c-122">In the **Deployment method** field, select **Mobile Device Management / Microsoft Intune** .</span></span>
    
4. <span data-ttu-id="e853c-123">Cliquez sur **Télécharger le package** , puis enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="e853c-123">Click **Download package** , and save the .zip file.</span></span>

5. <span data-ttu-id="e853c-124">Extrayez le contenu du fichier. zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="e853c-124">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="e853c-125">Vous devez avoir un fichier nommé *DeviceCompliance_valid_until_YYYY-mm-dd. par débarquement* .</span><span class="sxs-lookup"><span data-stu-id="e853c-125">You should have a file named *DeviceCompliance_valid_until_YYYY-MM-DD.offboarding* .</span></span>

6. <span data-ttu-id="e853c-126">Utilisez la stratégie de configuration personnalisée Microsoft Intune pour déployer les paramètres OMA-URI pris en charge suivants.</span><span class="sxs-lookup"><span data-stu-id="e853c-126">Use the Microsoft Intune custom configuration policy to deploy the following supported OMA-URI settings.</span></span>

      <span data-ttu-id="e853c-127">OMA-URI :./Device/Vendor/MSFT/WindowsAdvancedThreatProtection/Offboarding</span><span class="sxs-lookup"><span data-stu-id="e853c-127">OMA-URI: ./Device/Vendor/MSFT/WindowsAdvancedThreatProtection/Offboarding</span></span>      
      <span data-ttu-id="e853c-128">Type de date : chaîne</span><span class="sxs-lookup"><span data-stu-id="e853c-128">Date type: String</span></span>      
      <span data-ttu-id="e853c-129">Valeur : [copiez et collez la valeur à partir du contenu du fichier DeviceCompliance_valid_until_YYYY-MM-DD. par débarquement]</span><span class="sxs-lookup"><span data-stu-id="e853c-129">Value: [Copy and paste the value from the content of the DeviceCompliance_valid_until_YYYY-MM-DD.offboarding file]</span></span>

<span data-ttu-id="e853c-130">Pour plus d’informations sur les paramètres de stratégie Microsoft Intune, voir [paramètres de stratégie Windows 10 dans Microsoft Intune](https://docs.microsoft.com/intune/deploy-use/windows-10-policy-settings-in-microsoft-intune).</span><span class="sxs-lookup"><span data-stu-id="e853c-130">For more information on Microsoft Intune policy settings see, [Windows 10 policy settings in Microsoft Intune](https://docs.microsoft.com/intune/deploy-use/windows-10-policy-settings-in-microsoft-intune).</span></span>

> [!NOTE]
> <span data-ttu-id="e853c-131">L' **État d’intégrité de la stratégie périphériques offboarded** utilise des propriétés en lecture seule et ne peut pas être résolue.</span><span class="sxs-lookup"><span data-stu-id="e853c-131">The **Health Status for offboarded devices** policy uses read-only properties and can't be remediated.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e853c-132">Par débarquement entraîne l’arrêt de l’envoi des données de capteur au portail, mais les données de l’appareil, y compris la référence à toutes les alertes qu’il a subi, seront conservées pendant 6 mois maximum.</span><span class="sxs-lookup"><span data-stu-id="e853c-132">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e853c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e853c-133">Related topics</span></span>
- [<span data-ttu-id="e853c-134">Périphériques Windows 10 embarqués à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e853c-134">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="e853c-135">Appareils intégrés Windows 10 à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="e853c-135">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="e853c-136">Périphériques Windows 10 embarqués à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="e853c-136">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="e853c-137">Périphériques VDI (Virtual Desktop Infrastructure) non persistants</span><span class="sxs-lookup"><span data-stu-id="e853c-137">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="e853c-138">Résoudre les problèmes d’intégration de la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="e853c-138">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)
