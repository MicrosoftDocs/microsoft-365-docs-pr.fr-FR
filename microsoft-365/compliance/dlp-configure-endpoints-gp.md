---
title: Appareils Windows 10 intégrés via une stratégie de groupe
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
description: Utilisez la stratégie de groupe pour déployer le package de configuration sur Windows 10 afin qu'ils soient intégrés au service.
ms.openlocfilehash: 284de5169324b6da4038cfe0b50b2f2ffa40e3fd
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893285"
---
# <a name="onboard-windows-10-devices-using-group-policy"></a><span data-ttu-id="90f70-103">Intégrer des Windows 10 à l'aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="90f70-103">Onboard Windows 10 devices using Group Policy</span></span> 

<span data-ttu-id="90f70-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="90f70-104">**Applies to:**</span></span>

- [<span data-ttu-id="90f70-105">Microsoft 365 Protection contre la perte de données (DLP) de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="90f70-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](./endpoint-dlp-learn-about.md)
- <span data-ttu-id="90f70-106">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="90f70-106">Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="90f70-107">Pour utiliser les mises à jour de stratégie de groupe (GP) pour déployer le package, vous devez être sur Windows Server 2008 R2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="90f70-107">To use Group Policy (GP) updates to deploy the package, you must be on Windows Server 2008 R2 or later.</span></span>

> <span data-ttu-id="90f70-108">Pour Windows Server 2019, vous devrez peut-être remplacer NT AUTHORITY\Well-Known-System-Account par NT AUTHORITY\SYSTEM du fichier XML créé par la préférence de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="90f70-108">For Windows Server 2019, you may need to replace NT AUTHORITY\Well-Known-System-Account with NT AUTHORITY\SYSTEM of the XML file that the Group Policy preference creates.</span></span>

## <a name="onboard-devices-using-group-policy"></a><span data-ttu-id="90f70-109">Intégrer des appareils à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="90f70-109">Onboard devices using Group Policy</span></span>

1. <span data-ttu-id="90f70-110">Ouvrez le fichier de package de configuration de .zip de groupe (*DeviceComplianceOnboardingPackage.zip*) que vous avez téléchargé à partir de l'Assistant d'intégration de service.</span><span class="sxs-lookup"><span data-stu-id="90f70-110">Open the GP configuration package .zip file (*DeviceComplianceOnboardingPackage.zip*) that you downloaded from the service onboarding wizard.</span></span> <span data-ttu-id="90f70-111">Vous pouvez également obtenir le package à partir du [Centre de conformité Microsoft](https://compliance.microsoft.com/compliancesettings/deviceonboarding)</span><span class="sxs-lookup"><span data-stu-id="90f70-111">You can also get the package from [Microsoft Compliance center](https://compliance.microsoft.com/compliancesettings/deviceonboarding)</span></span>

2. <span data-ttu-id="90f70-112">Dans le volet de navigation, sélectionnez  >  **Paramètres'intégration de l'appareil.**</span><span class="sxs-lookup"><span data-stu-id="90f70-112">In the navigation pane, select **Settings** > **Device Onboarding**.</span></span>

3. <span data-ttu-id="90f70-113">Dans le **champ Méthode de déploiement,** sélectionnez **Stratégie de groupe.**</span><span class="sxs-lookup"><span data-stu-id="90f70-113">In the **Deployment method** field, select **Group policy**.</span></span>

4. <span data-ttu-id="90f70-114">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="90f70-114">Click **Download package** and save the .zip file.</span></span>

5. <span data-ttu-id="90f70-115">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par l'appareil.</span><span class="sxs-lookup"><span data-stu-id="90f70-115">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="90f70-116">Vous devez avoir un dossier appelé *OptionalParamsPolicy* et le fichier *DeviceComplianceLocalOnboardingScript.cmd*.</span><span class="sxs-lookup"><span data-stu-id="90f70-116">You should have a folder called *OptionalParamsPolicy* and the file *DeviceComplianceLocalOnboardingScript.cmd*.</span></span>

6. <span data-ttu-id="90f70-117">Ouvrez [la Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="90f70-117">Open the [Group Policy Management Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit**.</span></span>

7. <span data-ttu-id="90f70-118">Dans **l'Éditeur de gestion des stratégies** de groupe, allez à **Configuration** ordinateur, puis **Préférences,** puis **paramètres du panneau de configuration.**</span><span class="sxs-lookup"><span data-stu-id="90f70-118">In the **Group Policy Management Editor**, go to **Computer configuration**, then **Preferences**, and then **Control panel settings**.</span></span>

8. <span data-ttu-id="90f70-119">Cliquez avec le bouton droit **sur Tâches programmées,** pointez sur **Nouveau,** puis cliquez sur Tâche immédiate (au moins **Windows 7).**</span><span class="sxs-lookup"><span data-stu-id="90f70-119">Right-click **Scheduled tasks**, point to **New**, and then click **Immediate Task (At least Windows 7)**.</span></span>

9. <span data-ttu-id="90f70-120">Dans la **fenêtre** Tâche qui s'ouvre, allez dans **l'onglet** Général. Sous **Options de sécurité,** **cliquez sur Modifier** l'utilisateur ou le groupe, puis tapez SYSTEM, puis cliquez sur Vérifier **les noms,** **puis OK.**</span><span class="sxs-lookup"><span data-stu-id="90f70-120">In the **Task** window that opens, go to the **General** tab. Under **Security options** click **Change User or Group** and type SYSTEM and then click **Check Names** then **OK**.</span></span> <span data-ttu-id="90f70-121">NT AUTHORITY\SYSTEM apparaît en tant que compte d'utilisateur que la tâche exécutera.</span><span class="sxs-lookup"><span data-stu-id="90f70-121">NT AUTHORITY\SYSTEM appears as the user account the task will run as.</span></span>

10. <span data-ttu-id="90f70-122">Sélectionnez **Exécuter, que l'utilisateur soit** connecté ou non, puis cochez la case Exécuter avec les **privilèges les plus élevés.**</span><span class="sxs-lookup"><span data-stu-id="90f70-122">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check box.</span></span>

11. <span data-ttu-id="90f70-123">Go to the **Actions** tab and click **New...** **Assurez-vous que démarrer un programme** est sélectionné dans le champ **Action.**</span><span class="sxs-lookup"><span data-stu-id="90f70-123">Go to the **Actions** tab and click **New...** Ensure that **Start a program** is selected in the **Action** field.</span></span> <span data-ttu-id="90f70-124">Entrez le nom de fichier et l'emplacement du fichier *WindowsDefenderATPOnboardingScript.cmd* partagé.</span><span class="sxs-lookup"><span data-stu-id="90f70-124">Enter the file name and location of the shared *WindowsDefenderATPOnboardingScript.cmd* file.</span></span>

12. <span data-ttu-id="90f70-125">Cliquez **sur OK** et fermez toutes les fenêtres GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="90f70-125">Click **OK** and close any open GPMC windows.</span></span>


## <a name="offboard-devices-using-group-policy"></a><span data-ttu-id="90f70-126">Appareils de tableau de bord à l'aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="90f70-126">Offboard devices using Group Policy</span></span>
<span data-ttu-id="90f70-127">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="90f70-127">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="90f70-128">Les packages de offboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="90f70-128">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="90f70-129">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d'expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="90f70-129">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

> [!NOTE]
> <span data-ttu-id="90f70-130">Les stratégies d'intégration et deboarding ne doivent pas être déployées sur le même appareil en même temps, sinon cela provoquera des collisions imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="90f70-130">Onboarding and offboarding policies must not be deployed on the same device at the same time, otherwise this will cause unpredictable collisions.</span></span>

1. <span data-ttu-id="90f70-131">Obtenez le package deboarding à partir du [Centre de conformité Microsoft.](https://compliance.microsoft.com/compliancesettings/deviceonboarding)</span><span class="sxs-lookup"><span data-stu-id="90f70-131">Get the offboarding package from [Microsoft Compliance center](https://compliance.microsoft.com/compliancesettings/deviceonboarding).</span></span>

2. <span data-ttu-id="90f70-132">Dans le volet de navigation, sélectionnez **Paramètres**  >  **//Intégration de** l'appareil hors  >  **intégration.**</span><span class="sxs-lookup"><span data-stu-id="90f70-132">In the navigation pane, select **Settings** > **//Device onboarding** > **Offboarding**.</span></span>

3. <span data-ttu-id="90f70-133">Dans le **champ Méthode de déploiement,** sélectionnez **Stratégie de groupe.**</span><span class="sxs-lookup"><span data-stu-id="90f70-133">In the **Deployment method** field, select **Group policy**.</span></span>

4. <span data-ttu-id="90f70-134">Cliquez **sur Télécharger le package** et enregistrez .zip fichier.</span><span class="sxs-lookup"><span data-stu-id="90f70-134">Click **Download package** and save the .zip file.</span></span>

5. <span data-ttu-id="90f70-135">Extrayez le contenu du .zip vers un emplacement partagé en lecture seule accessible par l'appareil.</span><span class="sxs-lookup"><span data-stu-id="90f70-135">Extract the contents of the .zip file to a shared, read-only location that can be accessed by the device.</span></span> <span data-ttu-id="90f70-136">Vous devez avoir un fichier nommé *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span><span class="sxs-lookup"><span data-stu-id="90f70-136">You should have a file named *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd*.</span></span>

6. <span data-ttu-id="90f70-137">Ouvrez [la Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="90f70-137">Open the [Group Policy Management Console](/internet-explorer/ie11-deploy-guide/group-policy-and-group-policy-mgmt-console-ie11) (GPMC), right-click the Group Policy Object (GPO) you want to configure and click **Edit**.</span></span>

7. <span data-ttu-id="90f70-138">Dans **l'Éditeur de gestion des stratégies** de groupe, allez à **Configuration ordinateur,** puis **Préférences,** puis **paramètres du panneau de configuration.**</span><span class="sxs-lookup"><span data-stu-id="90f70-138">In the **Group Policy Management Editor**, go to **Computer configuration,** then **Preferences**, and then **Control panel settings**.</span></span>

8. <span data-ttu-id="90f70-139">Cliquez avec le bouton droit **sur Tâches programmées,** pointez sur **Nouveau,** puis cliquez sur **Tâche immédiate.**</span><span class="sxs-lookup"><span data-stu-id="90f70-139">Right-click **Scheduled tasks**, point to **New**, and then click **Immediate task**.</span></span>

9. <span data-ttu-id="90f70-140">Dans la **fenêtre** Tâche qui s'ouvre, allez dans **l'onglet** Général. Choisissez le compte d'utilisateur SYSTÈME local (BUILTIN\SYSTEM) sous **Options de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="90f70-140">In the **Task** window that opens, go to the **General** tab. Choose the local SYSTEM user account (BUILTIN\SYSTEM) under **Security options**.</span></span>

10. <span data-ttu-id="90f70-141">Sélectionnez **Exécuter, que l'utilisateur soit** connecté ou non, puis cochez la case Exécuter avec les privilèges les plus **élevés.**</span><span class="sxs-lookup"><span data-stu-id="90f70-141">Select **Run whether user is logged on or not** and check the **Run with highest privileges** check-box.</span></span>

11. <span data-ttu-id="90f70-142">Go to the **Actions** tab and click **New...**. **Assurez-vous que démarrer un programme** est sélectionné dans le champ **Action.**</span><span class="sxs-lookup"><span data-stu-id="90f70-142">Go to the **Actions** tab and click **New...**. Ensure that **Start a program** is selected in the **Action** field.</span></span> <span data-ttu-id="90f70-143">Entrez le nom de fichier et l'emplacement du fichier  *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd* partagé.</span><span class="sxs-lookup"><span data-stu-id="90f70-143">Enter the file name and location of the shared  *DeviceComplianceOffboardingScript_valid_until_YYYY-MM-DD.cmd* file.</span></span>

12. <span data-ttu-id="90f70-144">Cliquez **sur OK** et fermez toutes les fenêtres GPMC ouvertes.</span><span class="sxs-lookup"><span data-stu-id="90f70-144">Click **OK** and close any open GPMC windows.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90f70-145">Laboarding empêche l'appareil d'envoyer des données de capteur au portail, mais à partir de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="90f70-145">Offboarding causes the device to stop sending sensor data to the portal but data from the device.</span></span>


## <a name="monitor-device-configuration"></a><span data-ttu-id="90f70-146">Surveiller la configuration de l'appareil</span><span class="sxs-lookup"><span data-stu-id="90f70-146">Monitor device configuration</span></span>
<span data-ttu-id="90f70-147">Avec la stratégie de groupe, il n'existe pas d'option pour surveiller le déploiement des stratégies sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="90f70-147">With Group Policy there isn’t an option to monitor deployment of policies on the devices.</span></span> <span data-ttu-id="90f70-148">La surveillance peut être effectuée directement sur le portail ou à l'aide des différents outils de déploiement.</span><span class="sxs-lookup"><span data-stu-id="90f70-148">Monitoring can be done directly on the portal, or by using the different deployment tools.</span></span>

## <a name="monitor-devices-using-the-portal"></a><span data-ttu-id="90f70-149">Surveiller les appareils à l'aide du portail</span><span class="sxs-lookup"><span data-stu-id="90f70-149">Monitor devices using the portal</span></span>
1. <span data-ttu-id="90f70-150">Go to [Microsoft Compliance center](https://compliance.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="90f70-150">Go to [Microsoft Compliance center](https://compliance.microsoft.com/).</span></span>
2. <span data-ttu-id="90f70-151">Cliquez **sur La liste** Appareils.</span><span class="sxs-lookup"><span data-stu-id="90f70-151">Click **Devices** list.</span></span>
3. <span data-ttu-id="90f70-152">Vérifiez que les appareils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="90f70-152">Verify that devices are appearing.</span></span>

> [!NOTE]
> <span data-ttu-id="90f70-153">L'affichage des appareils dans la liste Appareils peut prendre plusieurs **jours.**</span><span class="sxs-lookup"><span data-stu-id="90f70-153">It can take several days for devices to start showing on the **Devices list**.</span></span> <span data-ttu-id="90f70-154">Cela inclut le temps qu'il faut pour que les stratégies soient distribuées à l'appareil, le temps qu'il faut avant que l'utilisateur se connecte et le temps qu'il faut au point de terminaison pour commencer à créer des rapports.</span><span class="sxs-lookup"><span data-stu-id="90f70-154">This includes the time it takes for the policies to be distributed to the device, the time it takes before the user logs on, and the time it takes for the endpoint to start reporting.</span></span>


## <a name="related-topics"></a><span data-ttu-id="90f70-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90f70-155">Related topics</span></span>
- [<span data-ttu-id="90f70-156">Intégrer Windows 10 appareils à l'aide Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="90f70-156">Onboard Windows 10 devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md)
- [<span data-ttu-id="90f70-157">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="90f70-157">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md)
- [<span data-ttu-id="90f70-158">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="90f70-158">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md)
- [<span data-ttu-id="90f70-159">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="90f70-159">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md)
- [<span data-ttu-id="90f70-160">Exécuter un test de détection sur un microsoft Defender pour les appareils de point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="90f70-160">Run a detection test on a newly onboarded Microsoft Defender for Endpoint devices</span></span>](/windows/security/threat-protection/microsoft-defender-atp/run-detection-test)
- [<span data-ttu-id="90f70-161">Résoudre les problèmes Microsoft Defender Advanced Threat Protection'intégration</span><span class="sxs-lookup"><span data-stu-id="90f70-161">Troubleshoot Microsoft Defender Advanced Threat Protection onboarding issues</span></span>](/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding)