---
title: Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles
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
description: Utilisez les outils de gestion des appareils mobiles pour déployer le package de configuration sur les appareils afin qu’ils soient intégrés au service.
ms.openlocfilehash: 1ad1115308257fa3ce63f10edebb9129638fd52f
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50917990"
---
# <a name="onboard-windows-10-devices-using-mobile-device-management-tools"></a><span data-ttu-id="55f08-103">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="55f08-103">Onboard Windows 10 devices using Mobile Device Management tools</span></span>

<span data-ttu-id="55f08-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="55f08-104">**Applies to:**</span></span>

- [<span data-ttu-id="55f08-105">Protection contre la perte de données de point de terminaison Microsoft 365 (DLP)</span><span class="sxs-lookup"><span data-stu-id="55f08-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](./endpoint-dlp-learn-about.md)

<span data-ttu-id="55f08-106">Vous pouvez utiliser des solutions de gestion des périphériques mobiles (MDM) pour configurer des appareils.</span><span class="sxs-lookup"><span data-stu-id="55f08-106">You can use mobile device management (MDM) solutions to configure devices.</span></span> <span data-ttu-id="55f08-107">La protection contre la perte de données de point de terminaison Microsoft 365 prend en charge les appareils mobiles en fournissant OMA-URIs pour créer des stratégies pour gérer les appareils.</span><span class="sxs-lookup"><span data-stu-id="55f08-107">Microsoft 365 Endpoint data loss prevention supports MDMs by providing OMA-URIs to create policies to manage devices.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="55f08-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="55f08-108">Before you begin</span></span>
<span data-ttu-id="55f08-109">Si vous utilisez Microsoft Intune, l’appareil doit être inscrit à la gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="55f08-109">If you're using Microsoft Intune, you must have the device MDM Enrolled.</span></span> <span data-ttu-id="55f08-110">Dans le cas contraire, les paramètres ne seront pas appliqués correctement.</span><span class="sxs-lookup"><span data-stu-id="55f08-110">Otherwise, settings will not be applied successfully.</span></span> 

<span data-ttu-id="55f08-111">Pour plus d’informations sur l’activation de la gestion des périphériques multi-appareils avec Microsoft Intune, voir Inscription des appareils [(Microsoft Intune).](/mem/intune/enrollment/device-enrollment)</span><span class="sxs-lookup"><span data-stu-id="55f08-111">For more information on enabling MDM with Microsoft Intune, see [Device enrollment (Microsoft Intune)](/mem/intune/enrollment/device-enrollment).</span></span>

## <a name="onboard-devices-using-microsoft-intune"></a><span data-ttu-id="55f08-112">Intégrer des appareils à l’aide de Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="55f08-112">Onboard devices using Microsoft Intune</span></span>

<span data-ttu-id="55f08-113">Suivez les instructions [d’Intune.](/intune/advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="55f08-113">Follow the instructions from [Intune](/intune/advanced-threat-protection).</span></span>

> [!NOTE]
> - <span data-ttu-id="55f08-114">La **stratégie État d’état d’état des appareils** intégrés utilise des propriétés en lecture seule et ne peut pas être corrigé.</span><span class="sxs-lookup"><span data-stu-id="55f08-114">The **Health Status for onboarded devices** policy uses read-only properties and can't be remediated.</span></span>

## <a name="offboard-and-monitor-devices-using-mobile-device-management-tools"></a><span data-ttu-id="55f08-115">Utiliser les outils de gestion des périphériques mobiles pour les appareils mobiles pour les hors-bord et les surveiller</span><span class="sxs-lookup"><span data-stu-id="55f08-115">Offboard and monitor devices using Mobile Device Management tools</span></span>

<span data-ttu-id="55f08-116">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="55f08-116">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="55f08-117">Les packages deboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="55f08-117">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="55f08-118">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="55f08-118">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="55f08-119">Les stratégies d’intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="55f08-119">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="55f08-120">Obtenez le package de mise hors programme à partir du [Centre de conformité Microsoft.](https://compliance.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="55f08-120">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com/).</span></span>

2. <span data-ttu-id="55f08-121">Dans le volet de navigation, sélectionnez **Paramètres**  >  **Intégration de l’appareil**  >  **hors intégration.**</span><span class="sxs-lookup"><span data-stu-id="55f08-121">In the navigation pane, select **Settings** > **Device onboarding** > **Offboarding**.</span></span>

3. <span data-ttu-id="55f08-122">Dans le **champ Méthode de déploiement,** sélectionnez **Gestion des périphériques mobiles / Microsoft Intune**.</span><span class="sxs-lookup"><span data-stu-id="55f08-122">In the **Deployment method** field, select **Mobile Device Management / Microsoft Intune**.</span></span>
    
4. <span data-ttu-id="55f08-123">Cliquez **sur Télécharger le package,** puis enregistrez le fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="55f08-123">Click **Download package**, and save the .zip file.</span></span>

5. <span data-ttu-id="55f08-124">Extrayez le contenu du fichier .zip vers un emplacement partagé en lecture seule accessible par les administrateurs réseau qui déploieront le package.</span><span class="sxs-lookup"><span data-stu-id="55f08-124">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the network administrators who will deploy the package.</span></span> <span data-ttu-id="55f08-125">Vous devez avoir un fichier nommé *DeviceCompliance_valid_until_YYYY-MM-DD.offboarding*.</span><span class="sxs-lookup"><span data-stu-id="55f08-125">You should have a file named *DeviceCompliance_valid_until_YYYY-MM-DD.offboarding*.</span></span>

6. <span data-ttu-id="55f08-126">Utilisez la stratégie de configuration personnalisée Microsoft Intune pour déployer les paramètres OMA-URI pris en charge suivants.</span><span class="sxs-lookup"><span data-stu-id="55f08-126">Use the Microsoft Intune custom configuration policy to deploy the following supported OMA-URI settings.</span></span>

      <span data-ttu-id="55f08-127">OMA-URI : ./Device/Vendor/MSFT/WindowsAdvancedThreatProtection/Offboarding</span><span class="sxs-lookup"><span data-stu-id="55f08-127">OMA-URI: ./Device/Vendor/MSFT/WindowsAdvancedThreatProtection/Offboarding</span></span>      
      <span data-ttu-id="55f08-128">Type de date : Chaîne</span><span class="sxs-lookup"><span data-stu-id="55f08-128">Date type: String</span></span>      
      <span data-ttu-id="55f08-129">Valeur : [Copier et coller la valeur à partir du contenu du fichier DeviceCompliance_valid_until_YYYY-MM-DD.offboarding]</span><span class="sxs-lookup"><span data-stu-id="55f08-129">Value: [Copy and paste the value from the content of the DeviceCompliance_valid_until_YYYY-MM-DD.offboarding file]</span></span>

<span data-ttu-id="55f08-130">Pour plus d’informations sur les paramètres de stratégie Microsoft Intune, voir les paramètres de stratégie [Windows 10 dans Microsoft Intune.](/intune/deploy-use/windows-10-policy-settings-in-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="55f08-130">For more information on Microsoft Intune policy settings see, [Windows 10 policy settings in Microsoft Intune](/intune/deploy-use/windows-10-policy-settings-in-microsoft-intune).</span></span>

> [!NOTE]
> <span data-ttu-id="55f08-131">La **stratégie État d’état d’état des** appareils déboardés utilise des propriétés en lecture seule et ne peut pas être corrigé.</span><span class="sxs-lookup"><span data-stu-id="55f08-131">The **Health Status for offboarded devices** policy uses read-only properties and can't be remediated.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55f08-132">Laboarding empêche l’appareil d’envoyer des données de capteur au portail, mais les données de l’appareil, y compris la référence aux alertes qu’il a eues, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="55f08-132">Offboarding causes the device to stop sending sensor data to the portal but data from the device, including reference to any alerts it has had will be retained for up to 6 months.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55f08-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55f08-133">Related topics</span></span>
- [<span data-ttu-id="55f08-134">Intégrer des appareils Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="55f08-134">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md)
- [<span data-ttu-id="55f08-135">Intégrer des appareils Windows 10 à l’aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="55f08-135">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="55f08-136">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="55f08-136">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="55f08-137">Intégrer les ordinateurs virtuels d’infrastructure de bureau virtuel (VDI) non persistants.</span><span class="sxs-lookup"><span data-stu-id="55f08-137">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="55f08-138">Résoudre les problèmes d’intégration de la Protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="55f08-138">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)