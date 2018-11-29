---
title: Déployer Windows 10 Entreprise pour les appareils existants en tant que mise à niveau inaltérable
description: Fournit des instructions sur la configuration et le déploiement d’une image d’entreprise de 10 Windows à l’aide de System Center Configuration Manager en tant qu’une mise à niveau sur place.
keywords: Déploiement de documentation, Windows 10 entreprise, Microsoft 365, Microsoft 365 pour entreprises, Microsoft 365, mise à niveau sur place, Gestionnaire de Configuration, System Center Configuration Manager
author: greg-lindsay
localization_priority: Normal
audience: microsoft-business
ms.prod: microsoft-365-enterprise
ms.topic: article
ms.date: 08/30/2018
ms.author: greglin
ms.openlocfilehash: 3df76c0de7b5a8b12c063113c79f9efa4e33b4c1
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867361"
---
# <a name="step-2-deploy-windows-10-enterprise-for-existing-devices-as-an-in-place-upgrade"></a><span data-ttu-id="e9d94-104">Étape 2 : Déployer Windows 10 Entreprise pour les appareils existants en tant que mise à niveau inaltérable</span><span class="sxs-lookup"><span data-stu-id="e9d94-104">Step 2: Deploy Windows 10 Enterprise for existing devices as an in-place upgrade</span></span>

<span data-ttu-id="e9d94-105">*Cet article s'applique à la fois aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="e9d94-105">*This article applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)

<span data-ttu-id="e9d94-p101">Le chemin d’accès plus simple pour mettre à niveau des ordinateurs en cours d’exécution Windows 7 ou Windows 8.1 à 10 Windows est une mise à niveau sur place. Vous pouvez utiliser une séquence de tâches System Center Configuration Manager (Gestionnaire de Configuration) pour automatiser complètement le processus.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p101">The simplest path to upgrade PCs currently running Windows 7 or Windows 8.1 to Windows 10 is through an in-place upgrade. You can use a System Center Configuration Manager (Configuration Manager) task sequence to completely automate the process.</span></span> 

<span data-ttu-id="e9d94-p102">Si vous avez des ordinateurs exécutant Windows 7 ou Windows 8.1, nous vous recommandons de ce chemin d’accès si votre organisation déploie Windows 10. Il s’appuie sur le programme d’installation de Windows (Setup.exe) pour effectuer une mise à niveau sur place, qui conserve automatiquement toutes les données, les paramètres et les applications, et les pilotes de la version de système d’exploitation existant. Cela nécessite le moindre effort informatique, car il n’est pas nécessaire pour l’infrastructure de déploiement complexes.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p102">If you have existing computers running Windows 7 or Windows 8.1, we recommend this path if your organization is deploying Windows 10. This leverages the Windows installation program (Setup.exe) to perform an in-place upgrade, which automatically preserves all data, settings, applications, and drivers from the existing operating system version. This requires the least IT effort, because there is no need for any complex deployment infrastructure.</span></span>

<span data-ttu-id="e9d94-111">Suivez ces étapes pour configurer et déployer une image d’entreprise de 10 Windows à l’aide du Gestionnaire de Configuration en tant qu’une mise à niveau sur place.</span><span class="sxs-lookup"><span data-stu-id="e9d94-111">Follow these steps to configure and deploy a Windows 10 Enterprise image using Configuration Manager as an in-place upgrade.</span></span>

## <a name="part-1-verify-readiness-to-upgrade-windows"></a><span data-ttu-id="e9d94-112">Partie 1 : Vérifier l’état de mise à niveau de Windows</span><span class="sxs-lookup"><span data-stu-id="e9d94-112">Part 1: Verify readiness to upgrade Windows</span></span>

<span data-ttu-id="e9d94-p103">Tout d’abord, utilisez la fonctionnalité de mise à niveau de préparation d’Analytique Windows pour fournir insights puissants et des recommandations sur les ordinateurs, des applications et des pilotes de votre organisation, par n° gratuitement et sans conditions d’infrastructure supplémentaires requises. Ce nouveau service vous guide tout au long de mise à niveau et la fonctionnalité de projets de mise à jour à l’aide d’un flux de travail basé sur les pratiques recommandée de Microsoft. Données d’inventaire à jour vous permet d’équilibre des coûts et les risques dans vos projets de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p103">First, use the Upgrade Readiness capability of Windows Analytics to provide powerful insights and recommendations about the computers, applications, and drivers in your organization, at no extra cost and without additional infrastructure requirements. This new service guides you through upgrade and feature update projects using a workflow based on Microsoft recommended practices. Up-to-date inventory data allows you to balance cost and risk in your upgrade projects.</span></span>

<span data-ttu-id="e9d94-116">Pour plus d’informations, mise en route, utilisation, et résoudre les problèmes de mise à niveau de préparation, voir [Windows de gérer les mises à niveau avec la mise à niveau de disponibilité](https://docs.microsoft.com/windows/deployment/upgrade/manage-windows-upgrades-with-upgrade-readiness) .</span><span class="sxs-lookup"><span data-stu-id="e9d94-116">See [Manage Windows upgrades with Upgrade Readiness](https://docs.microsoft.com/windows/deployment/upgrade/manage-windows-upgrades-with-upgrade-readiness) to learn more, get started, use, and troubleshoot Upgrade Readiness.</span></span>

<span data-ttu-id="e9d94-p104">Ensuite, suivez le guide pour utiliser System Center Configuration Manager (branche actuels) mise à niveau de Windows 7 ou version ultérieure vers Windows 10. Comme avec tout déploiement à haut risque, nous vous recommandons de sauvegarder les données utilisateur avant de continuer. Stockage en nuage OneDrive est prêt à être utilisé pour les utilisateurs sous licence Microsoft 365 et peut servir à stocker leurs fichiers. Pour plus d’informations, voir le [guide de démarrage rapide de OneDrive](https://aka.ms/ODfBquickstartguide). Pour accéder à cette page, vous devez vous connecter tant qu’administrateur du client ou un administrateur global dans un client Office 365 ou Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p104">Next, follow the guide to use System Center Configuration Manager (Current Branch) to upgrade Windows 7 or later operating system to Windows 10. As with any high-risk deployment, we recommend backing up user data before proceeding. OneDrive cloud storage is ready to use for licensed Microsoft 365 users and can be used to securely store their files. For more info, see [OneDrive quick start guide](https://aka.ms/ODfBquickstartguide). To access this page, you must sign in as a tenant admin or global admin in an Office 365 or Microsoft 365 tenant.</span></span>

<span data-ttu-id="e9d94-122">Pour obtenir la liste des versions du Gestionnaire de Configuration et les versions du client Windows 10 correspondantes qui sont pris en charge, voir [prise en charge pour Windows 10 pour System Center Configuration Manager](https://aka.ms/supportforwin10sccm).</span><span class="sxs-lookup"><span data-stu-id="e9d94-122">For a list of Configuration Manager versions and the corresponding Windows 10 client versions that are supported, see [Support for Windows 10 for System Center Configuration Manager](https://aka.ms/supportforwin10sccm).</span></span>

<span data-ttu-id="e9d94-123">**Pour vérifier l’état de mise à niveau de Windows**</span><span class="sxs-lookup"><span data-stu-id="e9d94-123">**To verify readiness to upgrade Windows**</span></span>

<span data-ttu-id="e9d94-124">Passez en revue ces configurations requises avant de commencer votre déploiement de Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="e9d94-124">Review these requirements before starting your Windows 10 deployment:</span></span>

- <span data-ttu-id="e9d94-p105">**Éditions Windows éligibles pour la mise à niveau** - vos périphériques doivent être en cours d’exécution éditions de Windows 7 ou Windows 8.1 qui sont éligibles pour la mise à niveau vers Windows 10 Enterprise. Pour une liste des versions prises en charge, voir [Windows 10 mise à niveau](https://aka.ms/win10upgradepaths).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p105">**Windows editions eligible for upgrade** - Your devices must be running editions of Windows 7 or Windows 8.1 that are eligible for upgrade to Windows 10 Enterprise. For a list of supported editions, see [Windows 10 upgrade paths](https://aka.ms/win10upgradepaths).</span></span> 
- <span data-ttu-id="e9d94-p106">Les **périphériques pris en charge** - la plupart des ordinateurs qui sont compatibles avec Windows 8.1 sera compatible avec Windows 10. Vous devrez peut-être installer les pilotes mis à jour dans Windows 10 pour vos périphériques fonctionne correctement. Pour plus d’informations, consultez la rubrique [spécifications Windows 10](https://aka.ms/windows10specifications) .</span><span class="sxs-lookup"><span data-stu-id="e9d94-p106">**Supported devices** - Most computers that are compatible with Windows 8.1 will be compatible with Windows 10. You may need to install updated drivers in Windows 10 for your devices to properly function. See [Windows 10 specifications](https://aka.ms/windows10specifications) for more info.</span></span>
- <span data-ttu-id="e9d94-130">**Préparation au déploiement** - Vérifiez que vous avez les éléments suivants avant de commencer la configuration du déploiement :</span><span class="sxs-lookup"><span data-stu-id="e9d94-130">**Deployment preparation** - Make sure you have the following before you start configuring the deployment:</span></span>
    - <span data-ttu-id="e9d94-p107">Support d’installation Windows 10 - le support d’installation doit se trouver sur un lecteur distinct, avec la norme ISO déjà montée. Vous pouvez obtenir l’ISO de [Téléchargements pour abonnés MSDN](https://aka.ms/msdn-subscriber-downloads) ou à partir du [Centre de gestion des licences en Volume](https://aka.ms/mvlsc).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p107">Windows 10 installation media - The installation media must be located on a separate drive, with the ISO already mounted. You can obtain the ISO from [MSDN Subscriber Downloads](https://aka.ms/msdn-subscriber-downloads) or from the [Volume Licensing Service Center](https://aka.ms/mvlsc).</span></span>
    - <span data-ttu-id="e9d94-p108">Sauvegardes de données de l’utilisateur, bien que les données utilisateur seront migrées dans la mise à niveau, meilleure pratique consiste à configurer un scénario de sauvegarde. Par exemple, exporter toutes les données utilisateur à un compte de OneDrive, un disque mémoire flash USB chiffrés BitLocker To Go ou un serveur de fichiers réseau. Pour plus d’informations, voir [sauvegarder ou transférer des données dans Windows](https://aka.ms/backuptransferdatawindows).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p108">Backups of user data - Although user data will be migrated in the upgrade, best practice is to configure a backup scenario. For example, export all user data to a OneDrive account, BitLocker To Go-encrypted USB flash drive, or network file server. For more information, see [Back up or transfer data in Windows](https://aka.ms/backuptransferdatawindows).</span></span>
- <span data-ttu-id="e9d94-p109">**Préparation de l’environnement** - vous allez utiliser une structure de serveur de gestionnaire de Configuration existante pour préparer le déploiement du système d’exploitation. Outre la configuration de base, les configurations suivantes doivent être effectuées dans l’environnement de gestionnaire de Configuration :</span><span class="sxs-lookup"><span data-stu-id="e9d94-p109">**Environment preparation** - You will use an existing Configuration Manager server structure to prepare for operating system deployment. In addition to the base setup, the following configurations should be made in the Configuration Manager environment:</span></span>
    1. <span data-ttu-id="e9d94-138">[Étendre le schéma Active Directory](https://aka.ms/extendadschema) et [créer un conteneur de gestion du système](https://aka.ms/createsysmancontainer).</span><span class="sxs-lookup"><span data-stu-id="e9d94-138">[Extend the Active Directory Schema](https://aka.ms/extendadschema) and [create a System Management container](https://aka.ms/createsysmancontainer).</span></span>
    2. <span data-ttu-id="e9d94-p110">Forêt Active Directory d’activer la découverte et la découverte de système Active Directory. Pour plus d’informations, voir [configurer des méthodes de découverte de System Center Configuration Manager](https://aka.ms/configurediscoverymethods).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p110">Enable Active Directory Forest Discovery and Active Directory System Discovery. For more info, see [Configure discovery methods for System Center Configuration Manager](https://aka.ms/configurediscoverymethods).</span></span>
    3. <span data-ttu-id="e9d94-p111">Créer des limites de plage IP et le groupe de limite pour l’affectation de site et de contenu. Pour plus d’informations, voir [définir des limites du site et les groupes de limite de System Center Configuration Manager](https://aka.ms/definesiteboundaries).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p111">Create IP range boundaries and boundary group for content and site assignment. For more info, see [Define site boundaries and boundary groups for System Center Configuration Manager](https://aka.ms/definesiteboundaries).</span></span>
    4. <span data-ttu-id="e9d94-p112">Ajouter et configurer le Gestionnaire de Configuration de reporting services point de rôle. Pour plus d’informations, voir [Configuration de création de rapports dans le Gestionnaire de Configuration](https://aka.ms/configurereporting).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p112">Add and configure the Configuration Manager reporting services point role. For more info, see [Configuring Reporting in Configuration Manager](https://aka.ms/configurereporting).</span></span>
    5. <span data-ttu-id="e9d94-145">Créez une structure de dossiers de système de fichier pour les packages.</span><span class="sxs-lookup"><span data-stu-id="e9d94-145">Create a file system folder structure for packages.</span></span>
    6. <span data-ttu-id="e9d94-146">Créez une structure de dossier console Gestionnaire de Configuration pour les packages.</span><span class="sxs-lookup"><span data-stu-id="e9d94-146">Create a Configuration Manager console folder structure for packages.</span></span>
    7. <span data-ttu-id="e9d94-147">Installez les mises à jour de System Center Configuration Manager (branche actuels) et des conditions préalables de Windows 10 supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e9d94-147">Install System Center Configuration Manager (Current Branch) updates and any additional Windows 10 prerequisites.</span></span>

## <a name="part-2-add-a-windows-10-os-image-using-configuration-manager"></a><span data-ttu-id="e9d94-148">Partie 2 : Ajouter une image de système d’exploitation Windows 10 à l’aide du Gestionnaire de Configuration</span><span class="sxs-lookup"><span data-stu-id="e9d94-148">Part 2: Add a Windows 10 OS image using Configuration Manager</span></span>
<span data-ttu-id="e9d94-p113">Maintenant, vous devez créer un package de mise à niveau de système d’exploitation contenant le support d’installation Windows 10 complète. Dans les étapes suivantes, vous allez utiliser le Gestionnaire de Configuration pour créer un package de mise à niveau pour Windows 10 entreprise x64.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p113">Now you'll need to create an operating system upgrade package that contains the full Windows 10 installation media. In the following steps, you’ll use Configuration Manager to create an upgrade package for Windows 10 Enterprise x64.</span></span>

<span data-ttu-id="e9d94-151">**Pour ajouter une image de système d’exploitation Windows 10 à l’aide du Gestionnaire de Configuration**</span><span class="sxs-lookup"><span data-stu-id="e9d94-151">**To add a Windows 10 OS image using Configuration Manager**</span></span>

1. <span data-ttu-id="e9d94-152">À l’aide de la console Configuration Manager, dans l’espace de travail de **Bibliothèque** , cliquez sur le nœud de **Packages de mise à niveau du système d’exploitation** , puis sélectionnez **Ajouter un Package de mise à niveau système d’exploitation**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-152">Using the Configuration Manager console, in the **Software Library** workspace, right-click the **Operating System Upgrade Packages** node, and then select **Add Operating System Upgrade Package**.</span></span>
2. <span data-ttu-id="e9d94-153">Dans la page de la **Source de données** , spécifiez le chemin d’accès UNC du support Windows 10 entreprise x64, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-153">On the **Data Source** page, specify the UNC path to the Windows 10 Enterprise x64 media, and then select **Next**.</span></span>
3. <span data-ttu-id="e9d94-154">Dans la page **Général** , spécifiez **la mise à niveau Windows 10 entreprise x64**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-154">On the **General** page, specify **Windows 10 Enterprise x64 Upgrade**, and then select **Next**.</span></span> 
4. <span data-ttu-id="e9d94-155">Dans la page **Résumé** , cliquez sur **suivant**, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-155">On the **Summary** page, select **Next**, and then select **Close**.</span></span> 
5. <span data-ttu-id="e9d94-156">Avec le bouton droit le package de **mise à jour Windows 10 entreprise x64** créé, puis sélectionnez **Distribuer le contenu**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-156">Right-click the created **Windows 10 Enterprise x64 Update** package, and then select **Distribute Content**.</span></span> 
6. <span data-ttu-id="e9d94-157">Choisissez votre point de distribution.</span><span class="sxs-lookup"><span data-stu-id="e9d94-157">Choose your distribution point.</span></span>

## <a name="part-3-configure-deployment-settings"></a><span data-ttu-id="e9d94-158">Partie 3 : Configurer les paramètres de déploiement</span><span class="sxs-lookup"><span data-stu-id="e9d94-158">Part 3: Configure deployment settings</span></span>
<span data-ttu-id="e9d94-p114">Dans cette étape, vous allez configurer une séquence de tâches de mise à niveau qui contient les paramètres pour la mise à niveau Windows 10. Vous pouvez ensuite identifier les périphériques pour mettre à niveau et déployer la séquence de tâches sur ces périphériques.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p114">In this step, you'll configure an upgrade task sequence that contains the settings for the Windows 10 upgrade. You'll then identify the devices to upgrade, and then deploy the task sequence to those devices.</span></span>

### <a name="create-a-task-sequence"></a><span data-ttu-id="e9d94-161">Créer une séquence de tâches</span><span class="sxs-lookup"><span data-stu-id="e9d94-161">Create a task sequence</span></span>
<span data-ttu-id="e9d94-162">Pour créer une séquence de tâches de mise à niveau, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9d94-162">To create an upgrade task sequence, perform the following steps:</span></span>
  
1. <span data-ttu-id="e9d94-163">Dans la console Configuration Manager, dans l’espace de travail **Bibliothèque logicielle** , développez les **systèmes d’exploitation**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-163">In the Configuration Manager console, in the **Software Library** workspace, expand **Operating Systems**.</span></span> 
2. <span data-ttu-id="e9d94-164">Cliquez sur le nœud **Séquences de tâches** , puis sélectionnez **Créer une séquence de tâches**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-164">Right-click the **Task Sequences** node, and then select **Create Task Sequence**.</span></span>
3. <span data-ttu-id="e9d94-165">Dans la page **créer une nouvelle séquence de tâches** , sélectionnez **mettre à niveau un système d’exploitation à partir du package de mise à niveau**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-165">On the **Create a new task sequence** page, select **Upgrade an operating system from upgrade package**, and then select **Next**.</span></span>
4. <span data-ttu-id="e9d94-166">Dans la page **Informations de séquence de tâches** , spécifiez **Windows 10 entreprise x64 mise à niveau**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-166">On the **Task Sequence Information** page, specify **Windows 10 Enterprise x64 Upgrade**, and then select **Next**.</span></span>
5. <span data-ttu-id="e9d94-167">Dans la page **mise à niveau du système d’exploitation Windows** , sélectionnez **Parcourir** et choisissez **package de mise à niveau du système d’exploitation de la mise à niveau Windows 10 entreprise x64**, sélectionnez **OK**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-167">On the **Upgrade the Windows operating system** page, select **Browse** and choose the **Windows 10 Enterprise x64 Upgrade operating system upgrade package**, select **OK**, and then select **Next**.</span></span>
6. <span data-ttu-id="e9d94-168">Continuez à faire défiler les pages restantes de l’Assistant, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-168">Continue through the remaining wizard pages, and then select **Close**.</span></span>

### <a name="create-a-device-collection"></a><span data-ttu-id="e9d94-169">Créer une collection de périphérique</span><span class="sxs-lookup"><span data-stu-id="e9d94-169">Create a device collection</span></span>
<span data-ttu-id="e9d94-170">Après avoir créé la séquence de tâches de mise à niveau, vous devez créer une collection qui contient les périphériques que sera mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="e9d94-170">After you create the upgrade task sequence, you'll need to create a collection that contains the devices you will upgrade.</span></span>

> [!NOTE]
> <span data-ttu-id="e9d94-p115">Utilisez les paramètres suivants pour tester le déploiement sur un seul périphérique. Vous pouvez utiliser des règles d’adhésion différents pour inclure des groupes de périphériques lorsque vous êtes prêt. Pour plus d’informations, voir [comment créer des collections dans System Center Configuration Manager](https://aka.ms/sccm-create-collections).</span><span class="sxs-lookup"><span data-stu-id="e9d94-p115">Use the following settings to test the deployment on a single device. You can use different membership rules to include groups of devices when you are ready. For more info, see [How to create collections in System Center Configuration Manager](https://aka.ms/sccm-create-collections).</span></span>

1. <span data-ttu-id="e9d94-174">Dans la console Configuration Manager, dans l’espace de travail **actifs et conformité** , avec le bouton droit de **Collections de périphérique**, puis sélectionnez **Créer une Collection de périphérique**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-174">In the Configuration Manager console, in the **Assets and Compliance** workspace, right-click **Device Collections**, and then select **Create Device Collection**.</span></span> 
2. <span data-ttu-id="e9d94-175">Dans l’Assistant créer une Collection de périphérique, dans la page **Général** , entrez les paramètres suivants, puis cliquez sur **suivant**:</span><span class="sxs-lookup"><span data-stu-id="e9d94-175">In the Create Device Collection wizard, on the **General** page, enter the following settings and then select **Next**:</span></span>
    - <span data-ttu-id="e9d94-176">Nom : Mise à niveau de l’entreprise x64 Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9d94-176">Name: Windows 10 Enterprise x64 Upgrade</span></span>
    - <span data-ttu-id="e9d94-177">Limitation de Collection : Tous les systèmes</span><span class="sxs-lookup"><span data-stu-id="e9d94-177">Limiting Collection: All Systems</span></span>
3. <span data-ttu-id="e9d94-178">Dans la page **Règles d’adhésion** , sélectionnez **Ajouter une règle** > **règle directe** pour lancer l’Assistant Création d’une règle d’appartenance directe.</span><span class="sxs-lookup"><span data-stu-id="e9d94-178">On the **Membership Rules** page, select **Add Rule** > **Direct rule** to launch the Create Direct Membership Rule Wizard.</span></span>
4. <span data-ttu-id="e9d94-179">Dans la page **Bienvenue** de l’Assistant Création d’une règle d’appartenance directe, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-179">On the **Welcome** page of the Create Direct Membership Rule Wizard, select **Next**.</span></span>
5. <span data-ttu-id="e9d94-180">Dans la page **Rechercher des ressources** , entrez les paramètres suivants, en remplaçant l’espace réservé du texte de la **valeur** par le nom de l’appareil que vous mettez à niveau :</span><span class="sxs-lookup"><span data-stu-id="e9d94-180">On the **Search for Resources** page, enter the following settings, replacing the placeholder **Value** text with the name of the device you are upgrading:</span></span> 
    - <span data-ttu-id="e9d94-181">Classe de ressource : Ressource du système</span><span class="sxs-lookup"><span data-stu-id="e9d94-181">Resource Class: System Resource</span></span>
    - <span data-ttu-id="e9d94-182">Nom d’attribut : nom</span><span class="sxs-lookup"><span data-stu-id="e9d94-182">Attribute Name: Name</span></span>
    - <span data-ttu-id="e9d94-183">Valeur : *PC0003*</span><span class="sxs-lookup"><span data-stu-id="e9d94-183">Value: *PC0003*</span></span>
6. <span data-ttu-id="e9d94-184">Dans la page **Sélectionner des ressources** , sélectionnez votre périphérique et cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-184">On the **Select Resources** page, select your device, and select **Next**.</span></span>
7. <span data-ttu-id="e9d94-185">Terminez l’Assistant créer une règle d’appartenance directe et l’Assistant Création de Collection de périphérique.</span><span class="sxs-lookup"><span data-stu-id="e9d94-185">Complete the Create Direct Membership Rule wizard and the Create Device Collection Wizard.</span></span>  
8. <span data-ttu-id="e9d94-p116">Passez en revue la collection de mise à niveau Windows 10 entreprise x64. Ne continuez pas jusqu'à ce que vous voyiez les ordinateurs ajouté au cours de la collection.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p116">Review the Windows 10 Enterprise x64 Upgrade collection. Do not continue until you see the machines you added in the collection.</span></span>

### <a name="create-an-operating-system-deployment"></a><span data-ttu-id="e9d94-188">Créer un déploiement de système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e9d94-188">Create an operating system deployment</span></span>
<span data-ttu-id="e9d94-189">Suivez ces étapes pour créer un déploiement de la séquence de tâches.</span><span class="sxs-lookup"><span data-stu-id="e9d94-189">Follow these steps to create a deployment for the task sequence.</span></span>

1. <span data-ttu-id="e9d94-190">Dans la console Configuration Manager, dans l’espace de travail **Bibliothèque logicielle** , avec le bouton droit de la séquence de tâches que vous avez créé dans une étape précédente, puis sélectionnez **déployer**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-190">In the Configuration Manager console, in the **Software Library** workspace, right-click the task sequence you created in a previous step, and then select **Deploy**.</span></span>
2. <span data-ttu-id="e9d94-191">Dans la page **Général** , sélectionnez la collection **Windows 10 entreprise x64 mise à niveau** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-191">On the **General** page, select the **Windows 10 Enterprise x64 Upgrade** collection, and then select **Next**.</span></span>
3. <span data-ttu-id="e9d94-192">Dans la page de **contenu** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-192">On the **Content** page, select **Next**.</span></span>
4. <span data-ttu-id="e9d94-193">Dans la page **Paramètres de déploiement** , sélectionnez les paramètres suivants, puis cliquez sur **suivant**:</span><span class="sxs-lookup"><span data-stu-id="e9d94-193">On the **Deployment Settings** page, select the following settings, and then select **Next**:</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9d94-p117">Pour ce déploiement de test, vous pouvez définir l’objectif à **disponible**, ce qui nécessite l’intervention de l’utilisateur pour démarrer le déploiement. Dans un environnement de production, vous pouvez souhaiter automatiser le déploiement à l’aide de l’objectif requis, qui consiste à configurer des options supplémentaires telles que la planification lorsque le déploiement est exécuté.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p117">For this test deployment, you'll set the purpose to **Available**, which requires user intervention to start the deployment. In a production environment, you may wish to automate the deployment using the Required purpose, which involves configuring additional options such as scheduling when the deployment is run.</span></span> 

    - <span data-ttu-id="e9d94-196">Action : installer</span><span class="sxs-lookup"><span data-stu-id="e9d94-196">Action: Install</span></span>
    - <span data-ttu-id="e9d94-197">Objectif : disponible</span><span class="sxs-lookup"><span data-stu-id="e9d94-197">Purpose: Available</span></span>

5. <span data-ttu-id="e9d94-198">Dans la page **planification** , acceptez les paramètres par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-198">On the **Scheduling** page, accept the default settings, and then select **Next**.</span></span>
6. <span data-ttu-id="e9d94-199">Dans la page de **l’Expérience utilisateur** , acceptez les paramètres par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-199">On the **User Experience** page, accept the default settings, and then select **Next**.</span></span>
7. <span data-ttu-id="e9d94-200">Dans la page **alertes** , acceptez les paramètres par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-200">On the **Alerts** page, accept the default settings, and then select **Next**.</span></span>
8. <span data-ttu-id="e9d94-201">Dans la page **Résumé** , cliquez sur **suivant**, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-201">On the **Summary** page, select **Next**, and then select **Close**.</span></span>

## <a name="part-5-start-the-windows-10-upgrade-task-sequence"></a><span data-ttu-id="e9d94-202">Partie 5 : Séquence de mise à niveau de tâche démarrer les 10 Windows</span><span class="sxs-lookup"><span data-stu-id="e9d94-202">Part 5: Start the Windows 10 upgrade task sequence</span></span>
<span data-ttu-id="e9d94-203">Procédez comme suit pour démarrer la séquence de tâches Windows 10 mise à niveau sur l’appareil que vous mettez à niveau.</span><span class="sxs-lookup"><span data-stu-id="e9d94-203">Follow these steps to start the Windows 10 Upgrade task sequence on the device that you are upgrading.</span></span>
 
1. <span data-ttu-id="e9d94-204">Ouvrez une session sur l’ordinateur Windows et démarrer le **Centre de logiciels**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-204">Log on to the Windows computer and start **Software Center**.</span></span>
2. <span data-ttu-id="e9d94-205">Sélectionnez la séquence de tâches que vous avez créée dans une étape précédente, puis sélectionnez **installer**.</span><span class="sxs-lookup"><span data-stu-id="e9d94-205">Select the task sequence that you created in a previous step, and then select **Install**.</span></span>
3. <span data-ttu-id="e9d94-206">Au début de la séquence de tâches, il démarre automatiquement le processus de mise à niveau sur place en appelant le programme d’installation de Windows (Setup.exe) avec les paramètres de ligne de commande nécessaires pour effectuer une mise à niveau automatisée qui conserve toutes les données, les paramètres, les applications, et pilotes.</span><span class="sxs-lookup"><span data-stu-id="e9d94-206">When the task sequence begins, it automatically initiates the in-place upgrade process by invoking the Windows setup program (Setup.exe) with the necessary command-line parameters to perform an automated upgrade, which preserves all data, settings, apps, and drivers.</span></span>
4. <span data-ttu-id="e9d94-207">Une fois que la séquence de tâches se termine correctement, l’ordinateur sera être entièrement mis à niveau vers Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e9d94-207">After the task sequence completes successfully, the computer will be fully upgraded to Windows 10.</span></span>

<span data-ttu-id="e9d94-p118">Si vous rencontrez des problèmes lors de l’utilisation de Windows 10 dans un environnement d’entreprise, vous pouvez consulter les [principales solutions Support Microsoft pour les problèmes les plus courants](https://docs.microsoft.com/windows/client-management/windows-10-support-solutions). Ces ressources incluent des articles de la Base de connaissances, des mises à jour et des articles de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p118">If you experience issues when using Windows 10 in an enterprise environment, you can consult [top Microsoft Support solutions for the most common issues](https://docs.microsoft.com/windows/client-management/windows-10-support-solutions). These resources include KB articles, updates, and library articles.</span></span>

<span data-ttu-id="e9d94-p119">Lors du déploiement de mises à jour au sein de votre organisation, utilisez la fonctionnalité de conformité de mise à jour de Windows Analytique pour fournir une vue globale de conformité de la mise à jour, mise à jour la progression du déploiement et pour les appareils Windows 10 de dépannage des échecs du système d’exploitation. Ce nouveau service utilise les données de diagnostic, y compris la progression de l’installation, configuration de la mise à jour Windows et d’autres informations à fournir ces informations, à no gratuitement et sans conditions d’infrastructure supplémentaires requises. Si elle est utilisée avec la mise à jour de Windows pour les professionnels ou d’autres outils de gestion, vous pouvez être assuré que vos périphériques sont mises à jour correctement.</span><span class="sxs-lookup"><span data-stu-id="e9d94-p119">During the rollout of updates across your organization, use the Update Compliance capability of Windows Analytics to provide a holistic view of OS update compliance, update deployment progress, and failure troubleshooting for Windows 10 devices. This new service uses diagnostic data including installation progress, Windows Update configuration and other information to provide such insights, at no extra cost and without additional infrastructure requirements. Whether it's used with Windows Update for Business or other management tools, you can be assured that your devices are properly updated.</span></span>

<span data-ttu-id="e9d94-213">Voir [Moniteur des mises à jour Windows et Windows Defender Antivirus avec la conformité de la mise à jour](https://docs.microsoft.com/windows/deployment/update/update-compliance-monitor) pour en savoir plus, mise en route et utiliser la conformité de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e9d94-213">See [Monitor Windows Updates and Windows Defender Antivirus with Update Compliance](https://docs.microsoft.com/windows/deployment/update/update-compliance-monitor) to learn more, get started, and use Update Compliance.</span></span>

<span data-ttu-id="e9d94-214">Comme point de contrôle intermédiaire, consultez les [critères de sortie](windows10-exit-criteria.md#crit-windows10-step2) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="e9d94-214">As an interim checkpoint, you can see the [exit criteria](windows10-exit-criteria.md#crit-windows10-step2) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="e9d94-215">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e9d94-215">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="e9d94-216">Déployer Windows 10 Entreprise pour des nouveaux appareils avec Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="e9d94-216">Deploy Windows 10 Enterprise for new devices with Windows Autopilot</span></span>](windows10-deploy-autopilot.md) |



<!--

| Phases | Description |
|:--- |:--- |
| [Phase 1: Consideration phase](#phase-1-consideration-phase) | TBD |
| [Phase 2: Testing phase](#phase-2-testing-phase) | TBD |
| [Phase 3: Deployment phase](#phase-3-deployment-phase) | TBD |

## Phase 1: Consideration phase
Before upgrading an OS in an enterprise environment, take the following technical aspects into account:
* [Infrastructure](#step-1-infrastructure)
* [Apps](#step-2-apps)
* [Governance and business processes](#step-3-governance-and-business-processes)

This guide is meant only to provide Microsoft's best recommendations around these assumptions by providing links to existing documentation.

### Step 1: Infrastructure
Consider your organization's collection of hardware, software, policies, networks, and other related technologies as part of the deployment process.

For in-place upgrade with Configuration Manager, these are the infrastructure you need to take into account:

#### Group Policy
Windows 10 introduces many new features and removes and changes many others in Windows 7 and 8.1, including new Group Policy settings which you need to test and implement as part of a Windows 10 migration. Use the examples from the following resources to assess current group policies for Windows, including Group Policy Objects in the Active Directory structure:
* [Manage Windows 10 with administrative templates](https://go.microsoft.com/fwlink/?linkid=860226) - Get step-by-step info on how to manage Windows 10 with administrative templates
* [Group Policy settings that apply to Windows 10](https://docs.microsoft.com/windows/client-management/group-policies-for-enterprise-and-education-editions) - Find out which Group Policy settings apply only to Windows 10 Enterprise

> [!NOTE]
> If you are considering moving to modern management by using MDM instead of Group Policy to manage device configurations, you can start by using the [MDM Migration Analysis Tool (MMAT)](https://github.com/WindowsDeviceManagement/MMAT) to determine what Group Policies are set on the device and report the corresponding settings, if available.

#### Data management
Although in-place upgrades shouldn’t affect user data and apps, a best practice is to configure a backup scenario and back up user data. For example, export all user data to a OneDrive for Business account, BitLocker To Go-encrypted USB flash drive, or network file server. For more details, see:
* [How to back up or transfer your data on a Windows-based computer](https://go.microsoft.com/fwlink/?linkid=860230) - Get step-by-step info on how to manually back up your personal files and settings.
* [Redirect known folders to OneDrive for Business](https://go.microsoft.com/fwlink/?linkid=846620) - Learn how to set a policy at the domain level to make sure users all sync to the same folder when they install the OneDrive sync client and how you can set additional policies to redirect the Documents folder to that sync location.

#### System Center Configuration Manager
This guide assumes you are following Microsoft recommendations and have one of the following versions of System Center Configuration Manager 2012 onward:
* System Center 2012 Configuration Manager with SP2
* System Center 2012, 2012 R2 Configuration Manager with SP1, Current Branch, 1706
    * [Run an in-place upgrade to the latest Configuration Manager](https://go.microsoft.com/fwlink/?linkid=839406)
    * [Updates for Configuration Manager](https://go.microsoft.com/fwlink/?linkid=620343)
* Core Configuration Manager configuration:
    * CONFIGURATION MANAGER accounts
    * Active Directory permissions
    * Source folder structure
    * Active Directory schema
* Configure the following [necessary Configuration Manager components for Windows 10 deployment](https://go.microsoft.com/fwlink/?linkid=860245):
    * **State migration point** - Stores user state migration data during computer replace scenarios
    * **Distribution point** - Stores all packages in Configuration Manager
    * **Software update point** - Updates an OS as part of the deployment process
    * **Reporting services point** - Monitors the OS deployment process
    * **Boot images** - Are Windows Preinstallation Environment (PE) images used by Configuration Manager to start deployments
    * **OS images** - Denotes the production deployment image (mounted OS)
    * **OS installers** - Creates reference images using Microsoft Deployment Toolkit (MDT) Light Touch
    * **Drivers** - Denotes a repository of managed device drivers
    * **Task Sequence** - Is delivered automatically to the client as a policy

#### Network bandwidth
This guide assumes you have enough network bandwidth to support the deployment of Windows 10 Enterprise and Office 365 ProPlus as a unit. As a bundle, network bandwidth is a significant factor.

#### Client machines and in-place upgrade scenario
* Disk encryption - Third-party disk encryption isn't supported in an in-place upgrade scenario.
* User profiles - Only the standard user profile type is supported.
* Legacy BIOS to Unified Extensible Firmware Interface (UEFI) booting - Changing from legacy BIOS to UEFI booting isn't supported.
* Dual-boot - This scenario is not covered in the guide. If you have the FastTrack Benefit, it only covers devices running a single OS.
* Virtual desktop infrastructure (VDI) environments - This scenario is not covered in the guide. If you have the FastTrack Benefit, it doesn't cover configuration or deployment on VDI environments.
* x64 and x86 - Changing from a 32-bit OS to a 64-bit isn't supported. For more info, see [Windows 10 deployment scenario > In-place upgrade](https://docs.microsoft.com/windows/deployment/windows-10-deployment-scenarios#in-place-upgrade).

### Step 2: Apps

#### Security
Security clients (like antivirus, anti-malware, and anti-spam) are typically found on all PCs within an organization. Because these programs hook into the deeper levels of the OS, you may need to perform a compatibility assessment before starting any Windows 10 migrations. You may need to upgrade, reconfigure, or even replace Some software. Not performing this assessment can lead to:
* Native app compatibility checks failing and preventing an in-place upgrade from starting.
* Broken functionality in the security software.
* Instability after upgrading to Windows 10 (like crashing and reduced performance)

**Antivirus**

Assess current antivirus software. Windows 10 comes with Windows Defender Antivirus to protect devices from malware, viruses, and security threats. We recommend Windows Defender Antivirus. To enable Windows Defender Antivirus, see [Windows Defender Antivirus](windows10-enable-security-features.md#windows-defender-antivirus) and [Protect devices with Windows Defender Antivirus](https://go.microsoft.com/fwlink/?linkid=860254).

To learn about antivirus solutions from other providers, see [Consumer antivirus software providers for Windows](https://go.microsoft.com/fwlink/?linkid=67345).

#### App readiness
Each Windows 10 release provides improved app compatibility. However, some apps may not be compatible. Depending on the app, you may need to only do a simple upgrade or configuration update before upgrading to Windows 10. In other circumstances, you may need to remove an app entirely.

Be sure to assess business critical apps and understand the impact of upgrading to the next OS. Prioritize the workloads that impact the least number of people during deployment. 

See the following Upgrade Readiness resources to help with app inventory, driver compatibility issues, and usage information:
* [Manage Windows Upgrades with Upgrade Readiness](https://go.microsoft.com/fwlink/?linkid=860255) - Learn about the tools to help you plan and manage the upgrade process end to end, which allow you to adopt new Windows releases more quickly.
* [Configure Windows diagnostic data](https://go.microsoft.com/fwlink/?linkid=859970) - Find out about the importance of Windows diagnostic data and how Microsoft protects that data.

> [!NOTE]
> Upgrade Readiness may not be able to assess compatibility for custom and line-of-business (LOB) apps in an organization.

#### Language packs
In-place upgrades have have limitations when it comes to language packs. The language stays consistent throughout the upgrade. Verify the language version and make sure it stays consistent. For example, Windows 7 with English as the default won’t change when upgraded to Windows 10. For more info, see:
* [Default language pack on your OS](https://go.microsoft.com/fwlink/?linkid=860282)
* [Finding language packs on each Windows 10 deployment](https://go.microsoft.com/fwlink/?linkid=860283)

For a Microsoft 365 powered device, you'll also need to download Office 365 ProPlus language packs that applies to the client. These come in 32-bit (x86) or 64-bit (x64). A specific language must be installed as the default. You can install other languages later. For more info, see:
* [Choose between 64-bit or 32-bit version of Office](https://go.microsoft.com/fwlink/?linkid=862361) - Helps you decide which version of Office is right for you.
* [Language accessory pack for Office](https://go.microsoft.com/fwlink/?linkid=860280) - Follow the steps to install the language accessory pack for Office.
* [Add an additional language pack](https://go.microsoft.com/fwlink/?linkid=860281) - Get step-by-step info on adding a language or setting language preferences in Office.

### Step 3: Governance and business processes

#### Windows as a service
Windows 10 introduced the concept of Windows as a service. This greatly changes the frequency and style of updates to Windows. Instead of new versions being released every 3-5 years, a more incremental model is used where two smaller updates (Feature Updates) are released yearly. For more info, see:
* [Windows as a service on the Windows IT Pro Center](https://www.microsoft.com/itpro/windows-10/windows-as-a-service)
* [Overview of Windows as a service](https://go.microsoft.com/fwlink/?linkid=860288)
* [Update Windows 10 in the enterprise](https://go.microsoft.com/fwlink/?linkid=860285)

#### Pilot users and deployment rings
Be sure to have a pilot group of users selected from different parts of the business. If you have Microsoft 365 powered devices, Windows 10 and Office 365 ProPlus users should be in these deployment rings. This affects future Windows updates as well (including features and quality). You need to create and edit device collections by deployment rings to help minimize the effect on network bandwidth and simplify future updates. 

For the group of pilot users, create a device collection on Configuration Manager. The list of devices should correspond to the list of the first users upgraded to Windows 10. 

**Windows 10 deployment rings**

There are three servicing channels for OS deployment rings:
* Windows Insider Program - Provides organizations with the opportunity to test and provide feedback on features that are shipped in the next feature update.
* Semi-Annual Channel - Provides new functionality with twice-per-year feature update releases. Organizations can choose when to deploy updates from the Semi-Annual Channel.
* Long-Term Servicing Channel (LTSC) - Used for specialized devices and receives new feature releases about every three years.

For more info, see:
* [Windows Insider Program, Semi-Annual Channel, and Long-Term Servicing Channel](https://go.microsoft.com/fwlink/?linkid=860293)
* [Build deployment rings for Windows 10 updates](https://go.microsoft.com/fwlink/?linkid=860294)
* [Manage software updates using Intune in Azure Portal](https://docs.microsoft.com/intune/windows-update-for-business-configure)

**Office 365 ProPlus**

For Microsoft 365 powered devices, you must also be able to support the six-month update channel for both IT and business users. One way to do so is to have three groups:
* Current Channel
* Deferred Channel
* First-release for Deferred Channel

Each group has different configuration files, as users from the Current Channel are used as a pilot to test earlier updates. For more info, see:
* [Update process for Office 365 ProPlus](https://go.microsoft.com/fwlink/?linkid=860299)
* [Manage updates to Office 365 ProPlus](https://go.microsoft.com/fwlink/?linkid=860300)
* [Configure update settings for Office 365 ProPlus](https://go.microsoft.com/fwlink/?linkid=860301)
* [Update channels for Office 365 ProPlus](https://go.microsoft.com/fwlink/?linkid=860302)
* [Version and build numbers of update channel releases](https://go.microsoft.com/fwlink/?linkid=860304)

For more info, see [Phase 4: Office 365 ProPlus infrastructure for Microsoft 365 Enterprise](office365proplus-infrastructure.md).

## Phase 2: Testing phase
Once you've completed the scenarios and requirements in [Step 1: Consideration phase](#step-1-consideration-phase), you can move to this stage.
* [Networking](#step-1-networking)
* [Identity](#step-2-identity)
* [Client readiness](#step-3-client-readiness)
* [System Center Configuration Manager](#step-4-system-center-configuration-manager)
* [Diagnostic data](#step-5-diagnostic-data)

### Step 1: Networking
Ports to the client need to be opened for Office 365 ProPlus (for a Microsoft 365 powered device) and Configuration Manager. For more details about setting up your Microsoft 365 Enterprise networking infrastructure, see [Phase 1: Networking](networking-infrastructure.md).

When setting up your networking infrastructure as part your in-place upgrade, make sure you complete these steps:
1. Read the best practices for [network planning and improving migration performance for Office 365](http://go.microsoft.com/fwlink/?LinkId=733655).
2. [Plan for network devices that connect to Office 365 services](http://go.microsoft.com/fwlink/?LinkId=733652).
3. [Review network impact of directory synchronization](http://go.microsoft.com/fwlink/?LinkId=733652).
4. Calculate the number of clients to use per IP address and understand [Network Address Translation (NAT) support with Office 365](http://go.microsoft.com/fwlink/?LinkId=733653) and how it impacts the number of users and client devices you can serve with a single IP address.
5. If your organization restricts computers on your network from connecting to the Internet, you'll need to understand the [endpoints (fully qualified domain names (FQDNs), ports, URLs, IPv4, and IPv6 address ranges)](http://go.microsoft.com/fwlink/?LinkID=280129) that you should include in your outbound allow lists to ensure your computers can successfully use Office 365 services.
6. [Create domain name system records for Office 365 at any Domain Name System hosting provider](http://go.microsoft.com/fwlink/?LinkId=733656).
7. [Reduce mail exchange (MX) DNS record time to live (TTL) value](http://go.microsoft.com/fwlink/?LinkId=733656).

### Step 2: Identity
Intelligent security for Microsoft 365 Enterprise, in which the right users have access to the right resources with an appropriate level of access, begins with identity management. For more details about setting up your Microsoft 365 Enterprise identity infrastructure, see [Phase 2: Identity](identity-infrastructure.md).

When setting up your identity infrastructure as part of your in-place upgrade, make sure you complete these tasks:
1. [Add a domain and users to Office 365](http://go.microsoft.com/fwlink/?LinkID=526338).
2. [Install and run the Office 365 IdFix tool](http://go.microsoft.com/fwlink/?LinkId=733662), which scans your on-premises Active Directory environment and identifies problems that might impact directory synchronization and slow your migration to Office 365.
3. Configure Active Directory for directory synchronization with Office 365 and [integrate on-premises directories with Azure AD](http://go.microsoft.com/fwlink/?LinkId=733661).
4. [Prepare to provision users through directory synchronization to Office 365](http://go.microsoft.com/fwlink/?LinkId=733659).
5. Know the [prerequisites for Azure AD Connect](http://go.microsoft.com/fwlink/?LinkId=733663), then install and run the Azure AD Connect tool to synchronize your on-premises Active Directory to the Azure AD service used by Office 365.
6. Determine custom installation of Azure AD Connect (full version of SQL Server for directory synchronization, if required).
7. [Integrate your on-premises identities with Azure AD](http://go.microsoft.com/fwlink/?LinkID=733485).
8. [Sync a list of required attributes with AD Connect](https://go.microsoft.com/fwlink/?linkid=860363) to get all the features in Office 365 and Windows 10.
9. Activate Windows 10 Enterprise licenses, which are checked based on Azure AD credentials.

    This provides a systematic way to assign licenses to end users and groups in your organization. For more info, see [Windows 10 Subscription Activation](https://go.microsoft.com/fwlink/?linkid=860365) and [Deploy Windows 10 licenses](https://go.microsoft.com/fwlink/?linkid=860367).

### Step 3: Client readiness

#### System requirements for Office 365
Confirm that Windows 10 works with Office 365. Be sure you're using the latest OS version and browsers with Office 365 and have updated them with the latest service packs. For more info on Office requirements, see [System requirements for Office](http://go.microsoft.com/fwlink/?LinkID=394412).

### Step 4: System Center Configuration Manager
See [System Center Configuration Manager](#system-center-configuration-manager).

### Step 5: Diagnostic data
Microsoft uses diagnostic data to help keep Windows devices secure by identifying malware trends and other threats and to help us improve the quality of Windows and Microsoft services. You must ensure that the diagnostics service is enabled at a minimum level of Basic on all endpoints in your organization. **By default, this service is enabled and set to the Enhanced level.** However, it’s good practice to check and ensure that they are receiving sensor data. Setting levels through policies overrides device-level settings. 

**Windows 10 operating system diagnostic data levels**

You can configure your operating system diagnostic data settings using the management tools you’re already using, such as Group Policy, MDM, or Windows Provisioning. You can also manually change your settings using Registry Editor. Setting your diagnostic data levels through a management policy overrides any device level settings.

Use the appropriate value in the table below when you configure the management policy.

| Level | Data gathered | Value |
|:--- |:--- |:--- |
| Security | Security data only. | 0 |
| Basic | Security data, and basic system and quality data. | 1 |
| Enhanced | Security data, basic system and quality data, and enhanced insights and advanced reliability data. | 2 |
| Full | Security data, basic system and quality data, enhanced insights and advanced reliability data, and full diagnostics data. | 3 |

You can enable diagnostics data through these methods:
* Microsoft Intune - If you plan to use Intune to manage your devices, you can create a configuration policy to enable diagnostic data by configuring the <a href="https://docs.microsoft.com/windows/client-management/mdm/policy-csp-system#system-allowtelemetry" target="blank">SystemAllowTelemetry</a> system policy. For more info on setting up configuration policies, see [Manage settings and features on your devices with Microsoft Intune policies](https://aka.ms/intuneconfigpolicies).
* Registry Editor - You can use the Registry Editor to manually enable diagnostic data on each device in your organization, or write a script to edit the registry. If a management policy already exists, such as Group Policy or MDM, it will override this registry setting.
* Group Policy - If you do not plan to enroll devices in Intune, you can use a Group Policy object to set your organization’s diagnostic data level.
* Command prompt - You can set Windows 10 diagnostics data and service to automatically start with the command prompt. This method is best if you are testing the service on only a few devices. Enabling the service to start automatically with this command will not configure the diagnostic data level. If you have not configured a diagnostic data level using management tools, the service will operate with the default Enhanced level.

See [Configure Windows diagnostic data in your organization](https://docs.microsoft.com/windows/configuration/configure-windows-diagnostic-data-in-your-organization) to learn more about Windows diagnostic data and how you can enable it based on the method that you choose.

## Phase 3: Deployment phase
When ready, complete these:
* [In-place upgrade to Windows 10 Enterprise](#31-in-place-upgrade-to-windows-10-enterprise)
* [Windows Defender Antivirus](#32-windows-defender-antivirus)

### Step 1: In-place upgrade to Windows 10 Enterprise
1. Integrate System Center Configuration Manager with Microsoft Deployment Tool.

    Be sure to use the Microsoft Deployment Toolkit (MDT) in conjunction with Configuration Manager when deploying an updated version of Windows 10. MDT brings Zero Touch Installation and Light Touch Installation enhancements to help with deployments at no cost to the customer. For more info, see:
    * [Download the latest MDT](https://go.microsoft.com/fwlink/?linkid=860465)
    * [Deploy Windows 10 with the Microsoft Deployment Toolkit](https://go.microsoft.com/fwlink/?linkid=860466)

2. Prepare for zero touch installation.

    As part of zero touch installation, you are responsible for preparing the following:
    * Configuration Manager service accounts
    * Active Directory permissions
    * Source folder structure

    Then, [integrate Configuration Manager with MDT](https://go.microsoft.com/fwlink/?linkid=860035).

3. Create a custom Windows Preinstallation Environment boot image.

    Windows Preinstallation Environment (PE) is a pre-installation environment required for OS deployments. It’s used to prepare a client machine for Windows installation, to copy disk images from a network file server, and to initiate Windows Setup. It’s used for Windows 10 Enterprise editions. For more info, see:
    * [Overview of Windows PE](https://go.microsoft.com/fwlink/?linkid=860468)
    * [Windows PE features, hardware requirements, and limitations](https://go.microsoft.com/fwlink/?linkid=860469)
    * [Create a custom Windows PE boot image with Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860470)

4. Add a Windows 10 OS upgrade image.

    You need to create a Windows 10 reference image with MDT (as needed). Reference images are the foundation of what each of the client machine’s OS looks like. The image should be in a separate folder located with the already-mounted ISO file. The task sequence looks for and then runs “setup.exe”. 

    Follow the steps to create and add a Windows 10 OS upgrade image on Configuration Manager:
    * [Create a Windows 10 reference image](https://go.microsoft.com/fwlink/?linkid=860500)
    * [Add a Windows 10 OS image using Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860501)

5. Create an app to deploy with Windows 10.

    For a Microsoft 365 powered device, you can deploy Office 365 ProPlus with Windows 10 Enterprise using Configuration Manager. You can also add other apps as needed.

    To deploy Office 365 ProPlus, follow the steps in [Phase 4: Office 365 ProPlus infrastructure for Microsoft 365 Enterprise](office365proplus-infrastructure.md). During this phase, make sure you complete these steps:
    
    1. Download the Office 2016 Deployment Tool (ODT) in conjunction with Configuration Manager to help with Office 365 ProPlus deployments. 
    2. Edit the configuration XML file to fit specific deployment needs (like version, language, and product element). 
    
    You can then create apps with Configuration Manager. For more info, see:
    * [Configuration options for ODT](https://go.microsoft.com/fwlink/?linkid=860504)
    * [Create apps in Configuration Manager](https://go.microsoft.com/fwlink/?linkid=761079)
    * [Deploy Office 365 ProPlus with Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860506)

6. Add drivers to a Windows 10 deployment using Windows PE.

    Network drivers need to be created for both Windows PE and Windows 10 to connect deployment shares and storage drivers with local storage on a client computer. Use Configuration Manager to create these drivers required for deployment. For more info, see [Add drivers to a Windows 10 deployment with Windows PE using Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860036).

7. Create a task sequence.

    A task sequence (a collection of commands) is required for MDT Lite Touch Installation (LTI). You need to create and then edit the task sequence for optimal deployment experience. One of the configurations enable support for Unified Extensible Firmware Interface (UEFI). The UEFI environment is a minimal boot OS where devices are booted and the Windows 10 OS runs. For more info, see:
    * [Overview of Windows Boot Manager](https://go.microsoft.com/fwlink/?linkid=860696)
    * [Create the task sequence in Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860697)

8. Finalize the OS configuration for Windows 10 deployment.

    **To finalize the OS configuration**

    1. Enable MDT monitoring
    2. Create and share the Logs folder
    3. Configure the rules
    4. Distribute content to the distribution point (a server running Configuration Manager)
    5. Create a deployment for the task sequence

   For more info, see [Finalize OS configuration with Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860697).

9. Deploy the Windows 10 Enterprise image to a UEFI machine.

    For more info, see [Deploy Windows 10 using Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860697).

10. Monitor the Windows 10 deployment.

    Use Configuration Manager and MDT to monitor your deployment. Deployment Workbench enables access to the computer remotely using the Diagnostics and Recovery Toolset (DaRT) (optional). Deployments can be monitored in Configuration Manager. For more info, see [Monitor the Windows 10 deployment with Configuration Manager](https://go.microsoft.com/fwlink/?linkid=860705).

### Step 2: Windows Defender Antivirus
See [Enable Windows 10 Enterprise security features > Windows Defender Antivirus](windows10-enable-security-features.md#windows-defender-antivirus)

-->
