---
title: Périphériques Windows 10 embarqués via la stratégie de groupe
f1.keywords: NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Utilisez la stratégie de groupe pour déployer le package de configuration sur les appareils Windows 10 afin qu’ils soient intégrés au service.
ms.openlocfilehash: a9e91f41b6e86e9f75d79d420c0ee830f1e3acf3
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769414"
---
# <a name="onboard-windows-10-devices-using-group-policy"></a><span data-ttu-id="39e8e-103">Périphériques Windows 10 embarqués à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="39e8e-103">Onboard Windows 10 devices using Group Policy</span></span> 

<span data-ttu-id="39e8e-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="39e8e-104">**Applies to:**</span></span>

- [<span data-ttu-id="39e8e-105">Microsoft 365 protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="39e8e-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)
- <span data-ttu-id="39e8e-106">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="39e8e-106">Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="39e8e-107">Pour utiliser les mises à jour de la stratégie de groupe pour déployer le package, vous devez être sur Windows Server 2008 R2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="39e8e-107">To use Group Policy (GP) updates to deploy the package, you must be on Windows Server 2008 R2 or later.</span></span>

> <span data-ttu-id="39e8e-108">Pour Windows Server 2019, il se peut que vous deviez remplacer NT AUTHORITY\Well-Known-System-Account par NT AUTHORITY\SYSTEM du fichier XML créé par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="39e8e-108">For Windows Server 2019, you may need to replace NT AUTHORITY\Well-Known-System-Account with NT AUTHORITY\SYSTEM of the XML file that the Group Policy preference creates.</span></span>

## <a name="onboard-devices-using-group-policy"></a><span data-ttu-id="39e8e-109">Périphériques intégrés à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="39e8e-109">Onboard devices using Group Policy</span></span>

1. <span data-ttu-id="39e8e-110">Ouvrez le fichier Package. zip de la configuration GP ( *DeviceComplianceOnboardingPackage.zip* ) que vous avez téléchargé à partir de l’Assistant d’intégration de service.</span><span class="sxs-lookup"><span data-stu-id="39e8e-110">Open the GP configuration package .zip file ( *DeviceComplianceOnboardingPackage.zip* ) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="39e8e-111">Vous pouvez également obtenir le package à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com/compliancesettings/deviceonboarding)</span><span class="sxs-lookup"><span data-stu-id="39e8e-111">You can also get the package from [Microsoft Compliance center](https://compliance.microsoft.com/compliancesettings/deviceonboarding)</span></span>

2. <span data-ttu-id="39e8e-112">Dans le volet de navigation, sélectionnez **paramètres** d’intégration de l'  >  **appareil** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-112">In the navigation pane, select **Settings** > **Device Onboarding** .</span></span>

3. <span data-ttu-id="39e8e-113">Dans le champ **méthode de déploiement** , sélectionnez stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-113">In the **Deployment method** field, select **Group policy** .</span></span>

4. <span data-ttu-id="39e8e-114">Cliquez sur **Télécharger le package** et enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="39e8e-114">Click **Download package** and save the .zip file.</span></span>

5. <span data-ttu-id="39e8e-115">Extrayez le contenu du fichier. zip vers un emplacement partagé en lecture seule accessible par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="39e8e-115">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="39e8e-116">Vous devez avoir un dossier nommé *OptionalParamsPolicy* et le fichier *DeviceComplianceLocalOnboardingScript. cmd* .</span><span class="sxs-lookup"><span data-stu-id="39e8e-116">You should have a folder called *OptionalParamsPolicy* and the file *DeviceComplianceLocalOnboardingScript.cmd* .</span></span>

6. <span data-ttu-id="39e8e-117">Ouvrez la [console de gestion des stratégies de groupe](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), cliquez avec le bouton droit sur l’objet de stratégie de groupe (GPO) que vous souhaitez configurer, puis cliquez sur **modifier** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-117">Open the [Group Policy Management Console](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit** .</span></span>

7. <span data-ttu-id="39e8e-118">Dans l' **éditeur de gestion des stratégies de groupe** , accédez à configuration de l’ordinateur, puis **Préférences** , puis **paramètres du panneau** de **configuration** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-118">In the **Group Policy Management Editor** , go to **Computer configuration** , then **Preferences** , and then **Control panel settings** .</span></span>

8. <span data-ttu-id="39e8e-119">Cliquez avec le bouton droit sur **tâches planifiées** , pointez sur **nouveau** , puis cliquez sur **tâche immédiate (au moins Windows 7)** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-119">Right-click **Scheduled tasks** , point to **New** , and then click **Immediate Task (At least Windows 7)** .</span></span>

9. <span data-ttu-id="39e8e-120">Dans la fenêtre **tâche** qui s’ouvre, accédez à l’onglet **général** . Sous **options de sécurité** , cliquez sur **modifier l’utilisateur ou le groupe** et tapez le système, puis cliquez sur vérifier les **noms** , puis sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-120">In the **Task** window that opens, go to the **General** tab. Under **Security options** click **Change User or Group** and type SYSTEM and then click **Check Names** then **OK** .</span></span> <span data-ttu-id="39e8e-121">NT AUTHORITY\SYSTEM apparaît en tant que compte d’utilisateur sous lequel la tâche s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="39e8e-121">NT AUTHORITY\SYSTEM appears as the user account the task will run as.</span></span>

10. <span data-ttu-id="39e8e-122">Sélectionnez **exécuter si l’utilisateur est connecté ou non** et activez la case à cocher **exécuter avec les privilèges les plus élevés** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-122">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check box.</span></span>

11. <span data-ttu-id="39e8e-123">Accédez à l’onglet **actions** , puis cliquez sur **nouveau...** Assurez-vous que l’option **Démarrer un programme** est sélectionnée dans le champ **action** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-123">Go to the **Actions** tab and click **New...** Ensure that **Start a program** is selected in the **Action** field.</span></span> <span data-ttu-id="39e8e-124">Entrez le nom de fichier et l’emplacement du fichier *WindowsDefenderATPOnboardingScript. cmd* partagé.</span><span class="sxs-lookup"><span data-stu-id="39e8e-124">Enter the file name and location of the shared *WindowsDefenderATPOnboardingScript.cmd* file.</span></span>

12. <span data-ttu-id="39e8e-125">Cliquez sur **OK** et fermez toutes les fenêtres de la console GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="39e8e-125">Click **OK** and close any open GPMC windows.</span></span>


## <a name="offboard-devices-using-group-policy"></a><span data-ttu-id="39e8e-126">Appareils débarquement à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="39e8e-126">Offboard devices using Group Policy</span></span>
<span data-ttu-id="39e8e-127">Pour des raisons de sécurité, le package utilisé pour les appareils débarquement expire 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="39e8e-127">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="39e8e-128">Les packages par débarquement expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="39e8e-128">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="39e8e-129">Lors du téléchargement d’un package par débarquement, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="39e8e-129">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="39e8e-130">Les stratégies d’intégration et de par débarquement ne doivent pas être déployées sur le même appareil simultanément, sinon cette opération entraîne des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="39e8e-130">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="39e8e-131">Obtenir le package par débarquement à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com/compliancesettings/deviceonboarding).</span><span class="sxs-lookup"><span data-stu-id="39e8e-131">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com/compliancesettings/deviceonboarding).</span></span>

2. <span data-ttu-id="39e8e-132">Dans le volet de navigation, sélectionnez **paramètres**  >  **//Device** de l’intégration de  >  **par débarquement** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-132">In the navigation pane, select **Settings** > **//Device onboarding** > **Offboarding** .</span></span>

3. <span data-ttu-id="39e8e-133">Dans le champ **méthode de déploiement** , sélectionnez stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-133">In the **Deployment method** field, select **Group policy** .</span></span>

4. <span data-ttu-id="39e8e-134">Cliquez sur **Télécharger le package** et enregistrez le fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="39e8e-134">Click **Download package** and save the .zip file.</span></span>

5. <span data-ttu-id="39e8e-135">Extrayez le contenu du fichier. zip vers un emplacement partagé en lecture seule accessible par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="39e8e-135">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="39e8e-136">Vous devez avoir un fichier nommé *DeviceComplianceOffboardingScript_valid_until_YYYY-mm-dd. cmd* .</span><span class="sxs-lookup"><span data-stu-id="39e8e-136">You should have a file named *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd* .</span></span>

6. <span data-ttu-id="39e8e-137">Ouvrez la [console de gestion des stratégies de groupe](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), cliquez avec le bouton droit sur l’objet de stratégie de groupe (GPO) que vous souhaitez configurer, puis cliquez sur **modifier** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-137">Open the [Group Policy Management Console](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit** .</span></span>

7. <span data-ttu-id="39e8e-138">Dans l' **éditeur de gestion des stratégies de groupe** , accédez à configuration de l' **ordinateur,** puis **Préférences** , puis **paramètres du panneau** de configuration.</span><span class="sxs-lookup"><span data-stu-id="39e8e-138">In the **Group Policy Management Editor** , go to **Computer configuration,** then **Preferences** , and then **Control panel settings** .</span></span>

8. <span data-ttu-id="39e8e-139">Cliquez avec le bouton droit sur **tâches planifiées** , pointez sur **nouveau** , puis cliquez sur **tâche immédiate** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-139">Right-click **Scheduled tasks** , point to **New** , and then click **Immediate task** .</span></span>

9. <span data-ttu-id="39e8e-140">Dans la fenêtre **tâche** qui s’ouvre, accédez à l’onglet **général** . Sélectionnez le compte d’utilisateur du système local (BUILTIN\SYSTEM) sous **options de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-140">In the **Task** window that opens, go to the **General** tab. Choose the local SYSTEM user account (BUILTIN\SYSTEM) under **Security options** .</span></span>

10. <span data-ttu-id="39e8e-141">Sélectionnez **exécuter si l’utilisateur est connecté ou non** et activez la case à cocher **exécuter avec les privilèges les plus élevés** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-141">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check-box.</span></span>

11. <span data-ttu-id="39e8e-142">Accédez à l’onglet **actions** , puis cliquez sur **nouveau.** ... Assurez-vous que l’option **Démarrer un programme** est sélectionnée dans le champ **action** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-142">Go to the **Actions** tab and click **New...** . Ensure that **Start a program** is selected in the **Action** field.</span></span> <span data-ttu-id="39e8e-143">Entrez le nom de fichier et l’emplacement du fichier partagé  *DeviceComplianceOffboardingScript_valid_until_YYYY-mm-dd. cmd* partagé.</span><span class="sxs-lookup"><span data-stu-id="39e8e-143">Enter the file name and location of the shared  *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd* file.</span></span>

12. <span data-ttu-id="39e8e-144">Cliquez sur **OK** et fermez toutes les fenêtres de la console GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="39e8e-144">Click **OK** and close any open GPMC windows.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39e8e-145">Par débarquement entraîne l’arrêt de l’appareil à envoyer les données de capteur au portail, mais les données de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="39e8e-145">Offboarding causes the device to stop sending sensor data to the portal but data from the device.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="39e8e-146">Surveiller la configuration de l’appareil</span><span class="sxs-lookup"><span data-stu-id="39e8e-146">Monitor device configuration</span></span>
<span data-ttu-id="39e8e-147">La stratégie de groupe ne permet pas de surveiller le déploiement des stratégies sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="39e8e-147">With Group Policy there isn’t an option to monitor deployment of policies on the devices.</span></span> <span data-ttu-id="39e8e-148">La surveillance peut être réalisée directement sur le portail ou à l’aide des différents outils de déploiement.</span><span class="sxs-lookup"><span data-stu-id="39e8e-148">Monitoring can be done directly on the portal, or by using the different deployment tools.</span></span>

## <a name="monitor-devices-using-the-portal"></a><span data-ttu-id="39e8e-149">Surveiller des périphériques à l’aide du portail</span><span class="sxs-lookup"><span data-stu-id="39e8e-149">Monitor devices using the portal</span></span>
1. <span data-ttu-id="39e8e-150">Accédez au [Centre de conformité Microsoft](https://compliance.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="39e8e-150">Go to [Microsoft Compliance center](https://compliance.microsoft.com/).</span></span>
2. <span data-ttu-id="39e8e-151">Cliquez sur liste des **appareils** .</span><span class="sxs-lookup"><span data-stu-id="39e8e-151">Click **Devices** list.</span></span>
3. <span data-ttu-id="39e8e-152">Vérifiez que les appareils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="39e8e-152">Verify that devices are appearing.</span></span>

> [!NOTE]
> <span data-ttu-id="39e8e-153">Le démarrage de l’affichage sur la **liste des appareils** peut prendre plusieurs jours.</span><span class="sxs-lookup"><span data-stu-id="39e8e-153">It can take several days for devices to start showing on the **Devices list** .</span></span> <span data-ttu-id="39e8e-154">Cela inclut le temps nécessaire à la distribution des stratégies sur l’appareil, le temps nécessaire avant l’ouverture de session de l’utilisateur et le temps nécessaire pour que le point de terminaison commence à créer des rapports.</span><span class="sxs-lookup"><span data-stu-id="39e8e-154">This includes the time it takes for the policies to be distributed to the device, the time it takes before the user logs on, and the time it takes for the endpoint to start reporting.</span></span>


## <a name="related-topics"></a><span data-ttu-id="39e8e-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39e8e-155">Related topics</span></span>
- [<span data-ttu-id="39e8e-156">Appareils intégrés Windows 10 à l’aide du gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="39e8e-156">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="39e8e-157">Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="39e8e-157">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="39e8e-158">Périphériques Windows 10 embarqués à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="39e8e-158">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="39e8e-159">Périphériques VDI (Virtual Desktop Infrastructure) non persistants</span><span class="sxs-lookup"><span data-stu-id="39e8e-159">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="39e8e-160">Exécuter un test de détection sur un périphérique récemment ATP Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="39e8e-160">Run a detection test on a newly onboarded Microsoft Defender ATP devices</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/run-detection-test)
- [<span data-ttu-id="39e8e-161">Résoudre les problèmes d’intégration de la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="39e8e-161">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)
