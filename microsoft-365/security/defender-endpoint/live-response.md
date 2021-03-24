---
title: Examiner les entités sur les appareils à l’aide de la réponse en direct dans Microsoft Defender ATP
description: Accéder à un appareil à l’aide d’une connexion shell distante sécurisée pour faire des enquêtes et prendre des mesures de réponse immédiates sur un appareil en temps réel.
keywords: remote, shell, connection, live, response, real-time, command, script, remediate, hunt, export, log, drop, download, file,
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: d992d98b916f5b59b67706b310edefdb37f157b4
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062425"
---
# <a name="investigate-entities-on-devices-using-live-response"></a><span data-ttu-id="e27ca-104">Examiner les entités sur les appareils à l’aide de la réponse en direct</span><span class="sxs-lookup"><span data-stu-id="e27ca-104">Investigate entities on devices using live response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e27ca-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e27ca-105">**Applies to:**</span></span>
- [<span data-ttu-id="e27ca-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e27ca-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="e27ca-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e27ca-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="e27ca-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="e27ca-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="e27ca-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e27ca-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="e27ca-110">La réponse en direct permet aux équipes d’opérations de sécurité d’accéder instantanément à un appareil (également appelé ordinateur) à l’aide d’une connexion Shell distante.</span><span class="sxs-lookup"><span data-stu-id="e27ca-110">Live response gives security operations teams instantaneous access to a device (also referred to as a machine) using a remote shell connection.</span></span> <span data-ttu-id="e27ca-111">Vous avez ainsi la puissance d’un travail d’examen approfondi et d’actions de réponse immédiates pour contenir rapidement des menaces identifiées, en temps réel.</span><span class="sxs-lookup"><span data-stu-id="e27ca-111">This gives you the power to do in-depth investigative work and take immediate response actions to promptly contain identified threats—in real time.</span></span> 

<span data-ttu-id="e27ca-112">La réponse dynamique est conçue pour améliorer les enquêtes en permettant à votre équipe des opérations de sécurité de collecter des données d’investigation, d’exécuter des scripts, d’envoyer des entités suspectes pour analyse, de corriger les menaces et de chercher de manière proactive les menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="e27ca-112">Live response is designed to enhance investigations by enabling your security operations team to collect forensic data, run scripts, send suspicious entities for analysis, remediate threats, and proactively hunt for emerging threats.</span></span><br/><br/>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4qLUW]

<span data-ttu-id="e27ca-113">Avec la réponse en direct, les analystes peuvent effectuer toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e27ca-113">With live response, analysts can do all of the following tasks:</span></span>
- <span data-ttu-id="e27ca-114">Exécutez des commandes de base et avancées pour faire des investigations sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-114">Run basic and advanced commands to do investigative work on a device.</span></span>
- <span data-ttu-id="e27ca-115">Téléchargez des fichiers tels que des exemples de programmes malveillants et les résultats des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e27ca-115">Download files such as malware samples and outcomes of PowerShell scripts.</span></span>
- <span data-ttu-id="e27ca-116">Téléchargez des fichiers en arrière-plan (nouveau !).</span><span class="sxs-lookup"><span data-stu-id="e27ca-116">Download files in the background (new!).</span></span>
- <span data-ttu-id="e27ca-117">Téléchargez un script PowerShell ou un exécutable dans la bibliothèque et exécutez-le sur un appareil à partir d’un niveau client.</span><span class="sxs-lookup"><span data-stu-id="e27ca-117">Upload a PowerShell script or executable to the library and run it on a device from a tenant level.</span></span>
- <span data-ttu-id="e27ca-118">Prendre ou annuler des actions de correction.</span><span class="sxs-lookup"><span data-stu-id="e27ca-118">Take or undo remediation actions.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e27ca-119">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e27ca-119">Before you begin</span></span>

<span data-ttu-id="e27ca-120">Avant de lancer une session sur un appareil, veillez à respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e27ca-120">Before you can initiate a session on a device, make sure you fulfill the following requirements:</span></span>

- <span data-ttu-id="e27ca-121">**Vérifiez que vous exécutez une version prise en charge de Windows.**</span><span class="sxs-lookup"><span data-stu-id="e27ca-121">**Verify that you're running a supported version of Windows**.</span></span> <br/>
<span data-ttu-id="e27ca-122">Les appareils doivent être en cours d’exécution dans l’une des versions suivantes de Windows.</span><span class="sxs-lookup"><span data-stu-id="e27ca-122">Devices must be running one of the following versions of Windows</span></span>

  - <span data-ttu-id="e27ca-123">**Windows 10**</span><span class="sxs-lookup"><span data-stu-id="e27ca-123">**Windows 10**</span></span>
    - <span data-ttu-id="e27ca-124">[Version 1909 ou](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1909) ultérieure</span><span class="sxs-lookup"><span data-stu-id="e27ca-124">[Version 1909](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1909) or later</span></span>  
    - <span data-ttu-id="e27ca-125">[Version 1903 avec](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1903) [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)</span><span class="sxs-lookup"><span data-stu-id="e27ca-125">[Version 1903](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1903) with [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)</span></span>
    - <span data-ttu-id="e27ca-126">[Version 1809 (RS 5)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1809) avec [KB4537818](https://support.microsoft.com/help/4537818/windows-10-update-kb4537818)</span><span class="sxs-lookup"><span data-stu-id="e27ca-126">[Version 1809 (RS 5)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1809) with [with KB4537818](https://support.microsoft.com/help/4537818/windows-10-update-kb4537818)</span></span>
    - <span data-ttu-id="e27ca-127">[Version 1803 (RS 4)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1803) avec [KB4537795](https://support.microsoft.com/help/4537795/windows-10-update-kb4537795)</span><span class="sxs-lookup"><span data-stu-id="e27ca-127">[Version 1803 (RS 4)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1803) with [KB4537795](https://support.microsoft.com/help/4537795/windows-10-update-kb4537795)</span></span>
    - <span data-ttu-id="e27ca-128">[Version 1709 (RS 3)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) avec [KB4537816](https://support.microsoft.com/help/4537816/windows-10-update-kb4537816)</span><span class="sxs-lookup"><span data-stu-id="e27ca-128">[Version 1709 (RS 3)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) with [KB4537816](https://support.microsoft.com/help/4537816/windows-10-update-kb4537816)</span></span>
  
  - <span data-ttu-id="e27ca-129">**Windows Server 2019 : applicable uniquement pour la prévisualisation publique**</span><span class="sxs-lookup"><span data-stu-id="e27ca-129">**Windows Server 2019 - Only applicable for Public preview**</span></span>
    - <span data-ttu-id="e27ca-130">Version 1903 ou (avec [KB4515384)](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)ultérieure</span><span class="sxs-lookup"><span data-stu-id="e27ca-130">Version 1903 or (with [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)) later</span></span> 
    - <span data-ttu-id="e27ca-131">Version 1809 [(avec KB4537818)](https://support.microsoft.com/en-us/help/4537818/windows-10-update-kb4537818)</span><span class="sxs-lookup"><span data-stu-id="e27ca-131">Version 1809 (with [KB4537818](https://support.microsoft.com/en-us/help/4537818/windows-10-update-kb4537818))</span></span>

- <span data-ttu-id="e27ca-132">**Activez la réponse en direct à partir de la page paramètres avancés.**</span><span class="sxs-lookup"><span data-stu-id="e27ca-132">**Enable live response from the advanced settings page**.</span></span><br>
<span data-ttu-id="e27ca-133">Vous devez activer la fonctionnalité de réponse en direct dans la page [Paramètres des fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-133">You'll need to enable the live response capability in the [Advanced features settings](advanced-features.md) page.</span></span>

    >[!NOTE]
    ><span data-ttu-id="e27ca-134">Seuls les utilisateurs ayant des rôles d’administrateur global ou de sécurité peuvent modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="e27ca-134">Only users with manage security or global admin roles can edit these settings.</span></span>

- <span data-ttu-id="e27ca-135">**Activez la réponse en direct pour les serveurs à partir de la page paramètres avancés** (recommandé).</span><span class="sxs-lookup"><span data-stu-id="e27ca-135">**Enable live response for servers from the advanced settings page** (recommended).</span></span><br>

    >[!NOTE]
    ><span data-ttu-id="e27ca-136">Seuls les utilisateurs ayant des rôles d’administrateur global ou de sécurité peuvent modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="e27ca-136">Only users with manage security or global admin roles can edit these settings.</span></span>
    
- <span data-ttu-id="e27ca-137">**Assurez-vous que le niveau de correction Automation** est affecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-137">**Ensure that the device has an Automation Remediation level assigned to it**.</span></span><br>
<span data-ttu-id="e27ca-138">Vous devez activer, au moins, le niveau de correction minimal pour un groupe d’appareils donné.</span><span class="sxs-lookup"><span data-stu-id="e27ca-138">You'll need to enable, at least, the minimum Remediation Level for a given Device Group.</span></span> <span data-ttu-id="e27ca-139">Sinon, vous ne pourrez pas établir une session Live Response à un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="e27ca-139">Otherwise you won't be able to establish a Live Response session to a member of that group.</span></span>

    <span data-ttu-id="e27ca-140">Vous recevrez l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="e27ca-140">You'll receive the following error:</span></span>

    ![Image du message d’erreur](images/live-response-error.png)

- <span data-ttu-id="e27ca-142">**Activer l’exécution de script non signé de réponse en** direct (facultatif).</span><span class="sxs-lookup"><span data-stu-id="e27ca-142">**Enable live response unsigned script execution** (optional).</span></span> <br>

    >[!WARNING]
    ><span data-ttu-id="e27ca-143">Autoriser l’utilisation de scripts non signés peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="e27ca-143">Allowing the use of unsigned scripts may increase your exposure to threats.</span></span>
 
  <span data-ttu-id="e27ca-144">L’exécution de scripts non signés n’est pas recommandée, car elle peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="e27ca-144">Running unsigned scripts is not recommended as it can increase your exposure to threats.</span></span> <span data-ttu-id="e27ca-145">Si vous devez toutefois les utiliser, vous devez activer le paramètre dans la page [Paramètres des fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-145">If you must use them however, you'll need to enable the setting in the [Advanced features settings](advanced-features.md) page.</span></span>
    
- <span data-ttu-id="e27ca-146">**Assurez-vous que vous avez les autorisations appropriées.**</span><span class="sxs-lookup"><span data-stu-id="e27ca-146">**Ensure that you have the appropriate permissions**.</span></span><br>
    <span data-ttu-id="e27ca-147">Seuls les utilisateurs qui ont été mis en service avec les autorisations appropriées peuvent lancer une session.</span><span class="sxs-lookup"><span data-stu-id="e27ca-147">Only users who have been provisioned with the appropriate permissions can initiate a session.</span></span> <span data-ttu-id="e27ca-148">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-148">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="e27ca-149">L’option de téléchargement d’un fichier dans la bibliothèque est disponible uniquement pour les personnes ayant les autorisations RBAC appropriées.</span><span class="sxs-lookup"><span data-stu-id="e27ca-149">The option to upload a file to the library is only available to those with the appropriate RBAC permissions.</span></span> <span data-ttu-id="e27ca-150">Le bouton est grisé pour les utilisateurs ayant uniquement des autorisations déléguées.</span><span class="sxs-lookup"><span data-stu-id="e27ca-150">The button is greyed out for users with only delegated permissions.</span></span>

    <span data-ttu-id="e27ca-151">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="e27ca-151">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="e27ca-152">Les autorisations des utilisateurs sont contrôlées par le rôle personnalisé RBAC.</span><span class="sxs-lookup"><span data-stu-id="e27ca-152">Users permissions are controlled by RBAC custom role.</span></span> 

## <a name="live-response-dashboard-overview"></a><span data-ttu-id="e27ca-153">Vue d’ensemble du tableau de bord de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="e27ca-153">Live response dashboard overview</span></span>
<span data-ttu-id="e27ca-154">Lorsque vous lancez une session de réponse en direct sur un appareil, un tableau de bord s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="e27ca-154">When you initiate a live response session on a device, a dashboard opens.</span></span> <span data-ttu-id="e27ca-155">Le tableau de bord fournit des informations sur la session, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e27ca-155">The dashboard provides information about the session such as the following:</span></span> 

- <span data-ttu-id="e27ca-156">Qui a créé la session</span><span class="sxs-lookup"><span data-stu-id="e27ca-156">Who created the session</span></span>
- <span data-ttu-id="e27ca-157">Au début de la session</span><span class="sxs-lookup"><span data-stu-id="e27ca-157">When the session started</span></span>
- <span data-ttu-id="e27ca-158">Durée de la session</span><span class="sxs-lookup"><span data-stu-id="e27ca-158">The duration of the session</span></span>

<span data-ttu-id="e27ca-159">Le tableau de bord vous donne également accès à :</span><span class="sxs-lookup"><span data-stu-id="e27ca-159">The dashboard also gives you access to:</span></span>
- <span data-ttu-id="e27ca-160">Inscription de l’application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e27ca-160">Disconnect session</span></span>
- <span data-ttu-id="e27ca-161">Télécharger des fichiers dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e27ca-161">Upload files to the library</span></span> 
- <span data-ttu-id="e27ca-162">Console de commande</span><span class="sxs-lookup"><span data-stu-id="e27ca-162">Command console</span></span>
- <span data-ttu-id="e27ca-163">Journal des commandes</span><span class="sxs-lookup"><span data-stu-id="e27ca-163">Command log</span></span>


## <a name="initiate-a-live-response-session-on-a-device"></a><span data-ttu-id="e27ca-164">Lancer une session de réponse en direct sur un appareil</span><span class="sxs-lookup"><span data-stu-id="e27ca-164">Initiate a live response session on a device</span></span> 

1. <span data-ttu-id="e27ca-165">Connectez-vous au Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e27ca-165">Sign in to Microsoft Defender Security Center.</span></span>

2. <span data-ttu-id="e27ca-166">Accédez à la page de liste des appareils et sélectionnez un appareil à examiner.</span><span class="sxs-lookup"><span data-stu-id="e27ca-166">Navigate to the devices list page and select a device to investigate.</span></span> <span data-ttu-id="e27ca-167">La page appareils s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="e27ca-167">The devices page opens.</span></span>

3. <span data-ttu-id="e27ca-168">Lancez la session de réponse en direct en sélectionnant **Lancer la session de réponse en direct.**</span><span class="sxs-lookup"><span data-stu-id="e27ca-168">Launch the live response session by selecting **Initiate live response session**.</span></span> <span data-ttu-id="e27ca-169">Une console de commande s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e27ca-169">A command console is displayed.</span></span> <span data-ttu-id="e27ca-170">Patientez pendant que la session se connecte à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-170">Wait while the session connects to the device.</span></span>

4. <span data-ttu-id="e27ca-171">Utilisez les commandes intégrées pour faire des enquêtes.</span><span class="sxs-lookup"><span data-stu-id="e27ca-171">Use the built-in commands to do investigative work.</span></span> <span data-ttu-id="e27ca-172">Pour plus d’informations, voir [commandes de réponse en direct.](#live-response-commands)</span><span class="sxs-lookup"><span data-stu-id="e27ca-172">For more information, see [Live response commands](#live-response-commands).</span></span>

5. <span data-ttu-id="e27ca-173">Après avoir terminé votre enquête, sélectionnez **Déconnecter la session,** puis sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e27ca-173">After completing your investigation, select **Disconnect session**, then select **Confirm**.</span></span>

## <a name="live-response-commands"></a><span data-ttu-id="e27ca-174">Commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="e27ca-174">Live response commands</span></span>

<span data-ttu-id="e27ca-175">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="e27ca-175">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="e27ca-176">Les autorisations utilisateur sont contrôlées par des rôles personnalisés RBAC.</span><span class="sxs-lookup"><span data-stu-id="e27ca-176">User permissions are controlled by RBAC custom roles.</span></span> <span data-ttu-id="e27ca-177">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-177">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 


>[!NOTE]
><span data-ttu-id="e27ca-178">La réponse en direct est un environnement de ligne de commande interactif basé sur le cloud, de ce fait, une expérience de commande spécifique peut varier en temps de réponse en fonction de la qualité du réseau et de la charge système entre l’utilisateur final et l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="e27ca-178">Live response is a cloud-based interactive shell, as such, specific command experience may vary in response time depending on network quality and system load between the end user and the target device.</span></span>

### <a name="basic-commands"></a><span data-ttu-id="e27ca-179">Commandes de base</span><span class="sxs-lookup"><span data-stu-id="e27ca-179">Basic commands</span></span>

<span data-ttu-id="e27ca-180">Les commandes suivantes sont disponibles pour les rôles  d’utilisateur qui ont la possibilité d’exécuter des commandes de réponse en direct de base.</span><span class="sxs-lookup"><span data-stu-id="e27ca-180">The following commands are available for user roles that are granted the ability to run **basic** live response commands.</span></span> <span data-ttu-id="e27ca-181">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-181">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

| <span data-ttu-id="e27ca-182">Command</span><span class="sxs-lookup"><span data-stu-id="e27ca-182">Command</span></span> | <span data-ttu-id="e27ca-183">Description</span><span class="sxs-lookup"><span data-stu-id="e27ca-183">Description</span></span> |
|---|---|--- |
|`cd` | <span data-ttu-id="e27ca-184">Modifie le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="e27ca-184">Changes the current directory.</span></span> | 
|`cls` | <span data-ttu-id="e27ca-185">Cette commande permet d’effacer l’écran de la console.</span><span class="sxs-lookup"><span data-stu-id="e27ca-185">Clears the console screen.</span></span>  |
|`connect` | <span data-ttu-id="e27ca-186">Lance une session de réponse en direct sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-186">Initiates a live response session to the device.</span></span> |
|`connections` | <span data-ttu-id="e27ca-187">Affiche toutes les connexions actives.</span><span class="sxs-lookup"><span data-stu-id="e27ca-187">Shows all the active connections.</span></span> |
|`dir` | <span data-ttu-id="e27ca-188">Affiche une liste de fichiers et de sous-répertoires dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e27ca-188">Shows a list of files and subdirectories in a directory.</span></span> |
|`download <file_path> &` | <span data-ttu-id="e27ca-189">Télécharge un fichier en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e27ca-189">Downloads a file in the background.</span></span> |
<span data-ttu-id="e27ca-190">drivers</span><span class="sxs-lookup"><span data-stu-id="e27ca-190">drivers</span></span> |  <span data-ttu-id="e27ca-191">Affiche tous les pilotes installés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-191">Shows all drivers installed on the device.</span></span> |
|`fg <command ID>` | <span data-ttu-id="e27ca-192">Renvoie un téléchargement de fichier au premier plan.</span><span class="sxs-lookup"><span data-stu-id="e27ca-192">Returns a file download to the foreground.</span></span> |
|`fileinfo` | <span data-ttu-id="e27ca-193">Récupération d’informations sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="e27ca-193">Get information about a file.</span></span> |
|`findfile` | <span data-ttu-id="e27ca-194">Localise les fichiers sous un nom donné sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-194">Locates files by a given name on the device.</span></span> |
|`help` | <span data-ttu-id="e27ca-195">Fournit des informations d’aide pour les commandes de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="e27ca-195">Provides help information for live response commands.</span></span> |
|`persistence` | <span data-ttu-id="e27ca-196">Affiche toutes les méthodes de persistance connues sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-196">Shows all known persistence methods on the device.</span></span> |
|`processes` | <span data-ttu-id="e27ca-197">Affiche tous les processus en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-197">Shows all processes running on the device.</span></span> |
|`registry` | <span data-ttu-id="e27ca-198">Affiche les valeurs du Registre.</span><span class="sxs-lookup"><span data-stu-id="e27ca-198">Shows registry values.</span></span> |
|`scheduledtasks` | <span data-ttu-id="e27ca-199">Affiche toutes les tâches programmées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-199">Shows all scheduled tasks on the device.</span></span> |
|`services` | <span data-ttu-id="e27ca-200">Affiche tous les services sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-200">Shows all services on the device.</span></span> |
|`trace` | <span data-ttu-id="e27ca-201">Définit le mode de journalisation du terminal pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="e27ca-201">Sets the terminal's logging mode to debug.</span></span> |

### <a name="advanced-commands"></a><span data-ttu-id="e27ca-202">Commandes avancées</span><span class="sxs-lookup"><span data-stu-id="e27ca-202">Advanced commands</span></span>
<span data-ttu-id="e27ca-203">Les commandes suivantes sont disponibles pour les rôles d’utilisateur qui ont la possibilité d’exécuter des **commandes** de réponse en direct avancées.</span><span class="sxs-lookup"><span data-stu-id="e27ca-203">The following commands are available for user roles that are granted the ability to run **advanced** live response commands.</span></span> <span data-ttu-id="e27ca-204">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-204">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

| <span data-ttu-id="e27ca-205">Command</span><span class="sxs-lookup"><span data-stu-id="e27ca-205">Command</span></span> | <span data-ttu-id="e27ca-206">Description</span><span class="sxs-lookup"><span data-stu-id="e27ca-206">Description</span></span> |
|---|---|
| `analyze` | <span data-ttu-id="e27ca-207">Analyse l’entité avec différents moteurs d’incrimination pour parvenir à un verdict.</span><span class="sxs-lookup"><span data-stu-id="e27ca-207">Analyses the entity with various incrimination engines to reach a verdict.</span></span> |
| `getfile` | <span data-ttu-id="e27ca-208">Obtient un fichier de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-208">Gets a file from the device.</span></span> <br> <span data-ttu-id="e27ca-209">REMARQUE : cette commande est une commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="e27ca-209">NOTE: This command has a prerequisite command.</span></span> <span data-ttu-id="e27ca-210">Vous pouvez utiliser la commande conjointement pour exécuter automatiquement la `-auto` `getfile` commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="e27ca-210">You can use the `-auto` command in conjunction with `getfile` to automatically run the prerequisite command.</span></span> |
| `run` | <span data-ttu-id="e27ca-211">Exécute un script PowerShell à partir de la bibliothèque sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-211">Runs a PowerShell script from the library on the device.</span></span> |
| `library` | <span data-ttu-id="e27ca-212">Répertorie les fichiers qui ont été chargés dans la bibliothèque de réponses en direct.</span><span class="sxs-lookup"><span data-stu-id="e27ca-212">Lists files that were uploaded to the live response library.</span></span> |
| `putfile` | <span data-ttu-id="e27ca-213">Place un fichier de la bibliothèque sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-213">Puts a file from the library to the device.</span></span> <span data-ttu-id="e27ca-214">Les fichiers sont enregistrés dans un dossier de travail et supprimés lorsque l’appareil redémarre par défaut.</span><span class="sxs-lookup"><span data-stu-id="e27ca-214">Files are saved in a working folder and are deleted when the device restarts by default.</span></span> |
| `remediate` | <span data-ttu-id="e27ca-215">Remédie à une entité sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e27ca-215">Remediates an entity on the device.</span></span> <span data-ttu-id="e27ca-216">L’action de correction varie en fonction du type d’entité :</span><span class="sxs-lookup"><span data-stu-id="e27ca-216">The remediation action will vary depending on the entity type:</span></span><br><span data-ttu-id="e27ca-217">- Fichier : supprimer</span><span class="sxs-lookup"><span data-stu-id="e27ca-217">- File: delete</span></span><br><span data-ttu-id="e27ca-218">- Processus : arrêter, supprimer un fichier image</span><span class="sxs-lookup"><span data-stu-id="e27ca-218">- Process: stop, delete image file</span></span><br><span data-ttu-id="e27ca-219">- Service : arrêter, supprimer un fichier image</span><span class="sxs-lookup"><span data-stu-id="e27ca-219">- Service: stop, delete image file</span></span><br><span data-ttu-id="e27ca-220">- Entrée de Registre : supprimer</span><span class="sxs-lookup"><span data-stu-id="e27ca-220">- Registry entry: delete</span></span><br><span data-ttu-id="e27ca-221">- Tâche programmée : supprimer</span><span class="sxs-lookup"><span data-stu-id="e27ca-221">- Scheduled task: remove</span></span><br><span data-ttu-id="e27ca-222">- Élément de dossier de démarrage : supprimer un fichier</span><span class="sxs-lookup"><span data-stu-id="e27ca-222">- Startup folder item: delete file</span></span> <br> <span data-ttu-id="e27ca-223">REMARQUE : cette commande est une commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="e27ca-223">NOTE: This command has a prerequisite command.</span></span> <span data-ttu-id="e27ca-224">Vous pouvez utiliser la commande conjointement pour exécuter automatiquement la `-auto` `remediate` commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="e27ca-224">You can use the `-auto` command in conjunction with `remediate` to automatically run the prerequisite command.</span></span> 
|`undo` | <span data-ttu-id="e27ca-225">Restaure une entité qui a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="e27ca-225">Restores an entity that was remediated.</span></span> |


## <a name="use-live-response-commands"></a><span data-ttu-id="e27ca-226">Utiliser des commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="e27ca-226">Use live response commands</span></span>

<span data-ttu-id="e27ca-227">Les commandes que vous pouvez utiliser dans la console suivent les mêmes principes que les [commandes Windows.](https://docs.microsoft.com/windows-server/administration/windows-commands/windows-commands#BKMK_c)</span><span class="sxs-lookup"><span data-stu-id="e27ca-227">The commands that you can use in the console follow similar principles as [Windows Commands](https://docs.microsoft.com/windows-server/administration/windows-commands/windows-commands#BKMK_c).</span></span>

<span data-ttu-id="e27ca-228">Les commandes avancées offrent un ensemble plus robuste d’actions qui vous permettent d’exécuter des actions plus puissantes telles que télécharger et télécharger un fichier, exécuter des scripts sur l’appareil et prendre des mesures correctives sur une entité.</span><span class="sxs-lookup"><span data-stu-id="e27ca-228">The advanced commands offer a more robust set of actions that allow you to take more powerful actions such as download and upload a file, run scripts on the device, and take remediation actions on an entity.</span></span>

### <a name="get-a-file-from-the-device"></a><span data-ttu-id="e27ca-229">Obtenir un fichier à partir de l’appareil</span><span class="sxs-lookup"><span data-stu-id="e27ca-229">Get a file from the device</span></span>

<span data-ttu-id="e27ca-230">Pour les scénarios où vous souhaitez obtenir un fichier à partir d’un appareil que vous examinez, vous pouvez utiliser la `getfile` commande.</span><span class="sxs-lookup"><span data-stu-id="e27ca-230">For scenarios when you'd like get a file from a device you're investigating, you can use the `getfile` command.</span></span> <span data-ttu-id="e27ca-231">Cela vous permet d’enregistrer le fichier à partir de l’appareil pour une investigation plus approfondie.</span><span class="sxs-lookup"><span data-stu-id="e27ca-231">This allows you to save the file from the device for further investigation.</span></span>

>[!NOTE]
><span data-ttu-id="e27ca-232">Les limites de taille de fichier suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="e27ca-232">The following file size limits apply:</span></span>
>- <span data-ttu-id="e27ca-233">`getfile` limite : 3 Go</span><span class="sxs-lookup"><span data-stu-id="e27ca-233">`getfile` limit: 3 GB</span></span>
>- <span data-ttu-id="e27ca-234">`fileinfo` limite : 10 Go</span><span class="sxs-lookup"><span data-stu-id="e27ca-234">`fileinfo` limit: 10 GB</span></span>
>- <span data-ttu-id="e27ca-235">`library` limite : 250 Mo</span><span class="sxs-lookup"><span data-stu-id="e27ca-235">`library` limit: 250 MB</span></span>

### <a name="download-a-file-in-the-background"></a><span data-ttu-id="e27ca-236">Télécharger un fichier en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="e27ca-236">Download a file in the background</span></span>

<span data-ttu-id="e27ca-237">Pour permettre à votre équipe des opérations de sécurité de continuer à examiner un appareil touché, les fichiers peuvent désormais être téléchargés en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e27ca-237">To enable your security operations team to continue investigating an impacted device, files can now be downloaded in the background.</span></span>

- <span data-ttu-id="e27ca-238">Pour télécharger un fichier en arrière-plan, dans la console de commande de réponse en direct, tapez `download <file_path> &` .</span><span class="sxs-lookup"><span data-stu-id="e27ca-238">To download a file in the background, in the live response command console, type `download <file_path> &`.</span></span>
- <span data-ttu-id="e27ca-239">Si vous attendez le téléchargement d’un fichier, vous pouvez le déplacer vers l’arrière-plan à l’aide de Ctrl + Z.</span><span class="sxs-lookup"><span data-stu-id="e27ca-239">If you are waiting for a file to be downloaded, you can move it to the background by using Ctrl + Z.</span></span>
- <span data-ttu-id="e27ca-240">Pour mettre un téléchargement de fichier au premier plan, dans la console de commande de réponse en direct, tapez `fg <command_id>` .</span><span class="sxs-lookup"><span data-stu-id="e27ca-240">To bring a file download to the foreground, in the live response command console, type `fg <command_id>`.</span></span>

<span data-ttu-id="e27ca-241">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="e27ca-241">Here are some examples:</span></span>


|<span data-ttu-id="e27ca-242">Commande</span><span class="sxs-lookup"><span data-stu-id="e27ca-242">Command</span></span>  |<span data-ttu-id="e27ca-243">Fonction</span><span class="sxs-lookup"><span data-stu-id="e27ca-243">What it does</span></span>  |
|---------|---------|
|`Download "C:\windows\some_file.exe" &`     |<span data-ttu-id="e27ca-244">Commence à télécharger un fichier nommé *some_file.exe* en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e27ca-244">Starts downloading a file named *some_file.exe* in the background.</span></span>         |
|`fg 1234`     |<span data-ttu-id="e27ca-245">Renvoie un téléchargement avec l’ID de commande *1234* au premier plan.</span><span class="sxs-lookup"><span data-stu-id="e27ca-245">Returns a download with command ID *1234* to the foreground.</span></span>         |


### <a name="put-a-file-in-the-library"></a><span data-ttu-id="e27ca-246">Placer un fichier dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e27ca-246">Put a file in the library</span></span>

<span data-ttu-id="e27ca-247">La réponse en direct dispose d’une bibliothèque dans laquelle vous pouvez placer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e27ca-247">Live response has a library where you can put files into.</span></span> <span data-ttu-id="e27ca-248">La bibliothèque stocke les fichiers (tels que les scripts) qui peuvent être exécutés dans une session de réponse en direct au niveau du client.</span><span class="sxs-lookup"><span data-stu-id="e27ca-248">The library stores files (such as scripts) that can be run in a live response session at the tenant level.</span></span>

<span data-ttu-id="e27ca-249">La réponse en direct permet aux scripts PowerShell de s’exécuter, mais vous devez d’abord placer les fichiers dans la bibliothèque avant de pouvoir les exécuter.</span><span class="sxs-lookup"><span data-stu-id="e27ca-249">Live response allows PowerShell scripts to run, however you must first put the files into the library before you can run them.</span></span> 

<span data-ttu-id="e27ca-250">Vous pouvez avoir une collection de scripts PowerShell qui peuvent s’exécuter sur les appareils avec qui vous lancez des sessions de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="e27ca-250">You can have a collection of PowerShell scripts that can run on devices that you initiate live response sessions with.</span></span> 

#### <a name="to-upload-a-file-in-the-library"></a><span data-ttu-id="e27ca-251">Pour télécharger un fichier dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e27ca-251">To upload a file in the library</span></span>

1. <span data-ttu-id="e27ca-252">Cliquez **sur Télécharger le fichier dans la bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="e27ca-252">Click **Upload file to library**.</span></span> 

2. <span data-ttu-id="e27ca-253">Cliquez **sur Parcourir** et sélectionnez le fichier.</span><span class="sxs-lookup"><span data-stu-id="e27ca-253">Click **Browse** and select the file.</span></span>

3. <span data-ttu-id="e27ca-254">Fournissez une brève description.</span><span class="sxs-lookup"><span data-stu-id="e27ca-254">Provide a brief description.</span></span>

4. <span data-ttu-id="e27ca-255">Spécifiez si vous souhaitez réécrire un fichier du même nom.</span><span class="sxs-lookup"><span data-stu-id="e27ca-255">Specify if you'd like to overwrite a file with the same name.</span></span>

5. <span data-ttu-id="e27ca-256">Si vous le souhaitez, connaissez les paramètres nécessaires pour le script, cochez la case des paramètres de script.</span><span class="sxs-lookup"><span data-stu-id="e27ca-256">If you'd like to be,  know what parameters are needed for the script, select the script parameters check box.</span></span> <span data-ttu-id="e27ca-257">Dans le champ de texte, entrez un exemple et une description.</span><span class="sxs-lookup"><span data-stu-id="e27ca-257">In the text field, enter an example and a description.</span></span>

6. <span data-ttu-id="e27ca-258">Cliquez **sur Confirmer.**</span><span class="sxs-lookup"><span data-stu-id="e27ca-258">Click **Confirm**.</span></span> 

7. <span data-ttu-id="e27ca-259">(Facultatif) Pour vérifier que le fichier a été chargé dans la bibliothèque, exécutez la `library` commande.</span><span class="sxs-lookup"><span data-stu-id="e27ca-259">(Optional) To verify that the file was uploaded to the library, run the `library` command.</span></span>


### <a name="cancel-a-command"></a><span data-ttu-id="e27ca-260">Annuler une commande</span><span class="sxs-lookup"><span data-stu-id="e27ca-260">Cancel a command</span></span>
<span data-ttu-id="e27ca-261">À tout moment pendant une session, vous pouvez annuler une commande en appuyant sur Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="e27ca-261">Anytime during a session, you can cancel a command by pressing CTRL + C.</span></span>  

>[!WARNING]
><span data-ttu-id="e27ca-262">L’utilisation de ce raccourci n’arrête pas la commande côté agent.</span><span class="sxs-lookup"><span data-stu-id="e27ca-262">Using this shortcut will not stop the command in the agent side.</span></span> <span data-ttu-id="e27ca-263">Il annule uniquement la commande dans le portail.</span><span class="sxs-lookup"><span data-stu-id="e27ca-263">It will only cancel the command in the portal.</span></span> <span data-ttu-id="e27ca-264">Ainsi, la modification des opérations telles que la « correction » peut se poursuivre, pendant l’annulation de la commande.</span><span class="sxs-lookup"><span data-stu-id="e27ca-264">So, changing operations such as "remediate" may continue, while the command is canceled.</span></span> 

### <a name="automatically-run-prerequisite-commands"></a><span data-ttu-id="e27ca-265">Exécuter automatiquement les commandes prérequises</span><span class="sxs-lookup"><span data-stu-id="e27ca-265">Automatically run prerequisite commands</span></span>

<span data-ttu-id="e27ca-266">Certaines commandes ont des commandes prérequises à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e27ca-266">Some commands have prerequisite commands to run.</span></span> <span data-ttu-id="e27ca-267">Si vous n’exécutez pas la commande prérequise, vous obtenez une erreur.</span><span class="sxs-lookup"><span data-stu-id="e27ca-267">If you don't run the prerequisite command, you'll get an error.</span></span> <span data-ttu-id="e27ca-268">Par exemple, l’exécution `download` de la commande sans `fileinfo` renvoyer d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e27ca-268">For example, running the `download` command without `fileinfo` will return an error.</span></span>

<span data-ttu-id="e27ca-269">Vous pouvez utiliser l’indicateur automatique pour exécuter automatiquement les commandes prérequises, par exemple :</span><span class="sxs-lookup"><span data-stu-id="e27ca-269">You can use the auto flag to automatically run prerequisite commands, for example:</span></span>

```console
getfile c:\Users\user\Desktop\work.txt -auto
```

## <a name="run-a-powershell-script"></a><span data-ttu-id="e27ca-270">Exécuter un script PowerShell</span><span class="sxs-lookup"><span data-stu-id="e27ca-270">Run a PowerShell script</span></span> 

<span data-ttu-id="e27ca-271">Avant de pouvoir exécuter un script PowerShell, vous devez d’abord le télécharger dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e27ca-271">Before you can run a PowerShell script, you must first upload it to the library.</span></span> 

<span data-ttu-id="e27ca-272">Après avoir téléchargé le script dans la bibliothèque, utilisez `run` la commande pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="e27ca-272">After uploading the script to the library, use the `run` command to run the script.</span></span>

<span data-ttu-id="e27ca-273">Si vous prévoyez d’utiliser un script non signé dans la session, vous devez activer le paramètre dans la page Paramètres des [fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="e27ca-273">If you plan to use an unsigned script in the session, you'll need to enable the setting in the [Advanced features settings](advanced-features.md) page.</span></span>

>[!WARNING]
><span data-ttu-id="e27ca-274">Autoriser l’utilisation de scripts non signés peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="e27ca-274">Allowing the use of unsigned scripts may increase your exposure to threats.</span></span>

## <a name="apply-command-parameters"></a><span data-ttu-id="e27ca-275">Appliquer des paramètres de commande</span><span class="sxs-lookup"><span data-stu-id="e27ca-275">Apply command parameters</span></span>

- <span data-ttu-id="e27ca-276">Consultez l’aide de la console pour en savoir plus sur les paramètres de commande.</span><span class="sxs-lookup"><span data-stu-id="e27ca-276">View the console help to learn about command parameters.</span></span> <span data-ttu-id="e27ca-277">Pour en savoir plus sur une commande individuelle, exécutez :</span><span class="sxs-lookup"><span data-stu-id="e27ca-277">To learn about an individual command, run:</span></span>
 
    `help <command name>`

- <span data-ttu-id="e27ca-278">Lorsque vous appliquez des paramètres à des commandes, notez que les paramètres sont gérés selon un ordre fixe :</span><span class="sxs-lookup"><span data-stu-id="e27ca-278">When applying parameters to commands, note that parameters are handled based on a fixed order:</span></span>
 
    `<command name> param1 param2` 

- <span data-ttu-id="e27ca-279">Lorsque vous spécifiez des paramètres en dehors de l’ordre fixe, spécifiez le nom du paramètre avec un tiret avant de fournir la valeur :</span><span class="sxs-lookup"><span data-stu-id="e27ca-279">When specifying parameters outside of the fixed order, specify the name of the parameter with a hyphen before providing the value:</span></span>
 
    `<command name> -param2_name param2`

- <span data-ttu-id="e27ca-280">Lorsque vous utilisez des commandes qui ont des commandes prérequises, vous pouvez utiliser des indicateurs :</span><span class="sxs-lookup"><span data-stu-id="e27ca-280">When using commands that have prerequisite commands, you can use flags:</span></span>

    <span data-ttu-id="e27ca-281">`<command name> -type file -id <file path> - auto` ou `remediate file <file path> - auto`.</span><span class="sxs-lookup"><span data-stu-id="e27ca-281">`<command name> -type file -id <file path> - auto` or `remediate file <file path> - auto`.</span></span>

## <a name="supported-output-types"></a><span data-ttu-id="e27ca-282">Types de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="e27ca-282">Supported output types</span></span>

<span data-ttu-id="e27ca-283">La réponse en direct prend en charge les types de sortie de tableau et de format JSON.</span><span class="sxs-lookup"><span data-stu-id="e27ca-283">Live response supports table and JSON format output types.</span></span> <span data-ttu-id="e27ca-284">Pour chaque commande, il existe un comportement de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="e27ca-284">For each command, there's a default output behavior.</span></span> <span data-ttu-id="e27ca-285">Vous pouvez modifier la sortie dans votre format de sortie préféré à l’aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e27ca-285">You can modify the output in your preferred output format using the following commands:</span></span>

- `-output json`
- `-output table`

>[!NOTE]
><span data-ttu-id="e27ca-286">Moins de champs sont affichés au format tableau en raison de l’espace limité.</span><span class="sxs-lookup"><span data-stu-id="e27ca-286">Fewer fields are shown in table format due to the limited space.</span></span> <span data-ttu-id="e27ca-287">Pour voir plus de détails dans la sortie, vous pouvez utiliser la commande de sortie JSON afin que d’autres détails soient affichés.</span><span class="sxs-lookup"><span data-stu-id="e27ca-287">To see more details in the output, you can use the JSON output command so that more details are shown.</span></span>

## <a name="supported-output-pipes"></a><span data-ttu-id="e27ca-288">Canaux de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="e27ca-288">Supported output pipes</span></span>

<span data-ttu-id="e27ca-289">La réponse en direct prend en charge le système de sortie vers l’CLI et le fichier.</span><span class="sxs-lookup"><span data-stu-id="e27ca-289">Live response supports output piping to CLI and file.</span></span> <span data-ttu-id="e27ca-290">L’CLI est le comportement de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="e27ca-290">CLI is the default output behavior.</span></span> <span data-ttu-id="e27ca-291">Vous pouvez canaliser la sortie vers un fichier à l’aide de la commande suivante : [command] > [filename].txt.</span><span class="sxs-lookup"><span data-stu-id="e27ca-291">You can pipe the output to a file using the following command: [command] > [filename].txt.</span></span>  

<span data-ttu-id="e27ca-292">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e27ca-292">Example:</span></span>

```console
processes > output.txt
```

## <a name="view-the-command-log"></a><span data-ttu-id="e27ca-293">Afficher le journal de commandes</span><span class="sxs-lookup"><span data-stu-id="e27ca-293">View the command log</span></span>

<span data-ttu-id="e27ca-294">Sélectionnez **l’onglet Journal** de commandes pour voir les commandes utilisées sur l’appareil au cours d’une session.</span><span class="sxs-lookup"><span data-stu-id="e27ca-294">Select the **Command log** tab to see the commands used on the device during a session.</span></span> <span data-ttu-id="e27ca-295">Chaque commande est suivi avec des détails complets tels que :</span><span class="sxs-lookup"><span data-stu-id="e27ca-295">Each command is tracked with full details such as:</span></span>
- <span data-ttu-id="e27ca-296">ID</span><span class="sxs-lookup"><span data-stu-id="e27ca-296">ID</span></span>
- <span data-ttu-id="e27ca-297">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e27ca-297">Command line</span></span>
- <span data-ttu-id="e27ca-298">Duration</span><span class="sxs-lookup"><span data-stu-id="e27ca-298">Duration</span></span>
- <span data-ttu-id="e27ca-299">Barre côté état et entrée ou sortie</span><span class="sxs-lookup"><span data-stu-id="e27ca-299">Status and input or output side bar</span></span>

## <a name="limitations"></a><span data-ttu-id="e27ca-300">Limites</span><span class="sxs-lookup"><span data-stu-id="e27ca-300">Limitations</span></span>

- <span data-ttu-id="e27ca-301">Les sessions de réponse en direct sont limitées à 10 sessions de réponse en direct à la fois.</span><span class="sxs-lookup"><span data-stu-id="e27ca-301">Live response sessions are limited to 10 live response sessions at a time.</span></span>
- <span data-ttu-id="e27ca-302">L’exécution de commande à grande échelle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e27ca-302">Large-scale command execution is not supported.</span></span>
- <span data-ttu-id="e27ca-303">La valeur du délai d’inactivité de la session de réponse active est de 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="e27ca-303">Live response session inactive timeout value is 5 minutes.</span></span> 
- <span data-ttu-id="e27ca-304">Un utilisateur ne peut lancer qu’une seule session à la fois.</span><span class="sxs-lookup"><span data-stu-id="e27ca-304">A user can only initiate one session at a time.</span></span>
- <span data-ttu-id="e27ca-305">Un appareil ne peut être connecté qu’à une seule session à la fois.</span><span class="sxs-lookup"><span data-stu-id="e27ca-305">A device can only be in one session at a time.</span></span>
- <span data-ttu-id="e27ca-306">Les limites de taille de fichier suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="e27ca-306">The following file size limits apply:</span></span>
   - <span data-ttu-id="e27ca-307">`getfile` limite : 3 Go</span><span class="sxs-lookup"><span data-stu-id="e27ca-307">`getfile` limit: 3 GB</span></span>
   - <span data-ttu-id="e27ca-308">`fileinfo` limite : 10 Go</span><span class="sxs-lookup"><span data-stu-id="e27ca-308">`fileinfo` limit: 10 GB</span></span>
   - <span data-ttu-id="e27ca-309">`library` limite : 250 Mo</span><span class="sxs-lookup"><span data-stu-id="e27ca-309">`library` limit: 250 MB</span></span>

## <a name="related-article"></a><span data-ttu-id="e27ca-310">Article connexe</span><span class="sxs-lookup"><span data-stu-id="e27ca-310">Related article</span></span>
- [<span data-ttu-id="e27ca-311">Exemples de commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="e27ca-311">Live response command examples</span></span>](live-response-command-examples.md)
