---
title: Examiner les entités sur les appareils à l'aide de la réponse en direct dans Microsoft Defender ATP
description: Accéder à un appareil à l'aide d'une connexion shell distante sécurisée pour faire des enquêtes et prendre des mesures de réponse immédiates sur un appareil en temps réel.
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
ms.openlocfilehash: 235df8c84077311444c597b120a19477cfd0986a
ms.sourcegitcommit: 223a36a86753fe9cebee96f05ab4c9a144133677
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51760415"
---
# <a name="investigate-entities-on-devices-using-live-response"></a><span data-ttu-id="89d61-104">Examiner les entités sur les appareils à l'aide de la réponse en direct</span><span class="sxs-lookup"><span data-stu-id="89d61-104">Investigate entities on devices using live response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="89d61-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="89d61-105">**Applies to:**</span></span>
- [<span data-ttu-id="89d61-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="89d61-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="89d61-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="89d61-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="89d61-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="89d61-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="89d61-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="89d61-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="89d61-110">La réponse en direct permet aux équipes d'opérations de sécurité d'accéder instantanément à un appareil (également appelé ordinateur) à l'aide d'une connexion shell distante.</span><span class="sxs-lookup"><span data-stu-id="89d61-110">Live response gives security operations teams instantaneous access to a device (also referred to as a machine) using a remote shell connection.</span></span> <span data-ttu-id="89d61-111">Cela vous donne la puissance d'un travail d'examen approfondi et de prendre des mesures de réponse immédiates pour contenir rapidement des menaces identifiées, en temps réel.</span><span class="sxs-lookup"><span data-stu-id="89d61-111">This gives you the power to do in-depth investigative work and take immediate response actions to promptly contain identified threats—in real time.</span></span> 

<span data-ttu-id="89d61-112">La réponse dynamique est conçue pour améliorer les enquêtes en permettant à votre équipe des opérations de sécurité de collecter des données d'investigation, d'exécuter des scripts, d'envoyer des entités suspectes pour analyse, de corriger les menaces et de chercher de manière proactive les menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="89d61-112">Live response is designed to enhance investigations by enabling your security operations team to collect forensic data, run scripts, send suspicious entities for analysis, remediate threats, and proactively hunt for emerging threats.</span></span><br/><br/>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4qLUW]

<span data-ttu-id="89d61-113">Avec la réponse en direct, les analystes peuvent effectuer toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="89d61-113">With live response, analysts can do all of the following tasks:</span></span>
- <span data-ttu-id="89d61-114">Exécutez des commandes de base et avancées pour faire des investigations sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-114">Run basic and advanced commands to do investigative work on a device.</span></span>
- <span data-ttu-id="89d61-115">Téléchargez des fichiers tels que des exemples de programmes malveillants et les résultats des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="89d61-115">Download files such as malware samples and outcomes of PowerShell scripts.</span></span>
- <span data-ttu-id="89d61-116">Téléchargez des fichiers en arrière-plan (nouveau !).</span><span class="sxs-lookup"><span data-stu-id="89d61-116">Download files in the background (new!).</span></span>
- <span data-ttu-id="89d61-117">Téléchargez un script PowerShell ou un exécutable dans la bibliothèque et exécutez-le sur un appareil à partir d'un niveau client.</span><span class="sxs-lookup"><span data-stu-id="89d61-117">Upload a PowerShell script or executable to the library and run it on a device from a tenant level.</span></span>
- <span data-ttu-id="89d61-118">Prendre ou annuler des actions de correction.</span><span class="sxs-lookup"><span data-stu-id="89d61-118">Take or undo remediation actions.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="89d61-119">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="89d61-119">Before you begin</span></span>

<span data-ttu-id="89d61-120">Avant de lancer une session sur un appareil, veillez à respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="89d61-120">Before you can initiate a session on a device, make sure you fulfill the following requirements:</span></span>

- <span data-ttu-id="89d61-121">**Vérifiez que vous exécutez une version prise en charge de Windows.**</span><span class="sxs-lookup"><span data-stu-id="89d61-121">**Verify that you're running a supported version of Windows**.</span></span> <br/>
<span data-ttu-id="89d61-122">Les appareils doivent être en cours d'exécution dans l'une des versions suivantes de Windows.</span><span class="sxs-lookup"><span data-stu-id="89d61-122">Devices must be running one of the following versions of Windows</span></span>

  - <span data-ttu-id="89d61-123">**Windows 10**</span><span class="sxs-lookup"><span data-stu-id="89d61-123">**Windows 10**</span></span>
    - <span data-ttu-id="89d61-124">[Version 1909 ou](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1909) ultérieure</span><span class="sxs-lookup"><span data-stu-id="89d61-124">[Version 1909](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1909) or later</span></span>  
    - <span data-ttu-id="89d61-125">[Version 1903 avec](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1903) [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)</span><span class="sxs-lookup"><span data-stu-id="89d61-125">[Version 1903](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1903) with [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)</span></span>
    - <span data-ttu-id="89d61-126">[Version 1809 (RS 5)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1809) avec [KB4537818](https://support.microsoft.com/help/4537818/windows-10-update-kb4537818)</span><span class="sxs-lookup"><span data-stu-id="89d61-126">[Version 1809 (RS 5)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1809) with [with KB4537818](https://support.microsoft.com/help/4537818/windows-10-update-kb4537818)</span></span>
    - <span data-ttu-id="89d61-127">[Version 1803 (RS 4)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1803) avec [KB4537795](https://support.microsoft.com/help/4537795/windows-10-update-kb4537795)</span><span class="sxs-lookup"><span data-stu-id="89d61-127">[Version 1803 (RS 4)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1803) with [KB4537795](https://support.microsoft.com/help/4537795/windows-10-update-kb4537795)</span></span>
    - <span data-ttu-id="89d61-128">[Version 1709 (RS 3)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) avec [KB4537816](https://support.microsoft.com/help/4537816/windows-10-update-kb4537816)</span><span class="sxs-lookup"><span data-stu-id="89d61-128">[Version 1709 (RS 3)](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) with [KB4537816](https://support.microsoft.com/help/4537816/windows-10-update-kb4537816)</span></span>
  
  - <span data-ttu-id="89d61-129">**Windows Server 2019 - Applicable uniquement pour la prévisualisation publique**</span><span class="sxs-lookup"><span data-stu-id="89d61-129">**Windows Server 2019 - Only applicable for Public preview**</span></span>
    - <span data-ttu-id="89d61-130">Version 1903 ou (avec [KB4515384)](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)ultérieure</span><span class="sxs-lookup"><span data-stu-id="89d61-130">Version 1903 or (with [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)) later</span></span> 
    - <span data-ttu-id="89d61-131">Version 1809 [(avec KB4537818)](https://support.microsoft.com/en-us/help/4537818/windows-10-update-kb4537818)</span><span class="sxs-lookup"><span data-stu-id="89d61-131">Version 1809 (with [KB4537818](https://support.microsoft.com/en-us/help/4537818/windows-10-update-kb4537818))</span></span>

- <span data-ttu-id="89d61-132">**Activez la réponse en direct à partir de la page paramètres avancés.**</span><span class="sxs-lookup"><span data-stu-id="89d61-132">**Enable live response from the advanced settings page**.</span></span><br>
<span data-ttu-id="89d61-133">Vous devez activer la fonctionnalité de réponse en direct dans la page [Paramètres des fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-133">You'll need to enable the live response capability in the [Advanced features settings](advanced-features.md) page.</span></span>

    >[!NOTE]
    ><span data-ttu-id="89d61-134">Seuls les utilisateurs ayant des rôles d'administrateur global ou de sécurité peuvent modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="89d61-134">Only users with manage security or global admin roles can edit these settings.</span></span>

- <span data-ttu-id="89d61-135">**Activez la réponse en direct pour les serveurs à partir de la page paramètres avancés** (recommandé).</span><span class="sxs-lookup"><span data-stu-id="89d61-135">**Enable live response for servers from the advanced settings page** (recommended).</span></span><br>

    >[!NOTE]
    ><span data-ttu-id="89d61-136">Seuls les utilisateurs ayant des rôles d'administrateur global ou de sécurité peuvent modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="89d61-136">Only users with manage security or global admin roles can edit these settings.</span></span>
    
- <span data-ttu-id="89d61-137">**Assurez-vous que le niveau de correction Automation** est affecté à l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-137">**Ensure that the device has an Automation Remediation level assigned to it**.</span></span><br>
<span data-ttu-id="89d61-138">Vous devez activer, au moins, le niveau de correction minimal pour un groupe d'appareils donné.</span><span class="sxs-lookup"><span data-stu-id="89d61-138">You'll need to enable, at least, the minimum Remediation Level for a given Device Group.</span></span> <span data-ttu-id="89d61-139">Sinon, vous ne pourrez pas établir de session Live Response à un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="89d61-139">Otherwise you won't be able to establish a Live Response session to a member of that group.</span></span>

    <span data-ttu-id="89d61-140">Vous recevrez l'erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="89d61-140">You'll receive the following error:</span></span>

    ![Image du message d'erreur](images/live-response-error.png)

- <span data-ttu-id="89d61-142">**Activer l'exécution de script non signé de réponse en** direct (facultatif).</span><span class="sxs-lookup"><span data-stu-id="89d61-142">**Enable live response unsigned script execution** (optional).</span></span> <br>

    >[!WARNING]
    ><span data-ttu-id="89d61-143">Autoriser l'utilisation de scripts non signés peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="89d61-143">Allowing the use of unsigned scripts may increase your exposure to threats.</span></span>
 
  <span data-ttu-id="89d61-144">L'exécution de scripts non signés n'est pas recommandée, car elle peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="89d61-144">Running unsigned scripts is not recommended as it can increase your exposure to threats.</span></span> <span data-ttu-id="89d61-145">Si vous devez toutefois les utiliser, vous devez activer le paramètre dans la page [Paramètres des fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-145">If you must use them however, you'll need to enable the setting in the [Advanced features settings](advanced-features.md) page.</span></span>
    
- <span data-ttu-id="89d61-146">**Assurez-vous que vous avez les autorisations appropriées.**</span><span class="sxs-lookup"><span data-stu-id="89d61-146">**Ensure that you have the appropriate permissions**.</span></span><br>
    <span data-ttu-id="89d61-147">Seuls les utilisateurs qui ont été mis en service avec les autorisations appropriées peuvent lancer une session.</span><span class="sxs-lookup"><span data-stu-id="89d61-147">Only users who have been provisioned with the appropriate permissions can initiate a session.</span></span> <span data-ttu-id="89d61-148">Pour plus d'informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-148">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="89d61-149">L'option de téléchargement d'un fichier dans la bibliothèque est disponible uniquement pour les personnes ayant les autorisations RBAC appropriées.</span><span class="sxs-lookup"><span data-stu-id="89d61-149">The option to upload a file to the library is only available to those with the appropriate RBAC permissions.</span></span> <span data-ttu-id="89d61-150">Le bouton est grisé pour les utilisateurs ayant uniquement des autorisations déléguées.</span><span class="sxs-lookup"><span data-stu-id="89d61-150">The button is greyed out for users with only delegated permissions.</span></span>

    <span data-ttu-id="89d61-151">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="89d61-151">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="89d61-152">Les autorisations des utilisateurs sont contrôlées par le rôle personnalisé RBAC.</span><span class="sxs-lookup"><span data-stu-id="89d61-152">Users permissions are controlled by RBAC custom role.</span></span> 

## <a name="live-response-dashboard-overview"></a><span data-ttu-id="89d61-153">Vue d'ensemble du tableau de bord de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="89d61-153">Live response dashboard overview</span></span>
<span data-ttu-id="89d61-154">Lorsque vous lancez une session de réponse en direct sur un appareil, un tableau de bord s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="89d61-154">When you initiate a live response session on a device, a dashboard opens.</span></span> <span data-ttu-id="89d61-155">Le tableau de bord fournit des informations sur la session, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="89d61-155">The dashboard provides information about the session such as the following:</span></span> 

- <span data-ttu-id="89d61-156">Qui a créé la session</span><span class="sxs-lookup"><span data-stu-id="89d61-156">Who created the session</span></span>
- <span data-ttu-id="89d61-157">Au début de la session</span><span class="sxs-lookup"><span data-stu-id="89d61-157">When the session started</span></span>
- <span data-ttu-id="89d61-158">Durée de la session</span><span class="sxs-lookup"><span data-stu-id="89d61-158">The duration of the session</span></span>

<span data-ttu-id="89d61-159">Le tableau de bord vous donne également accès à :</span><span class="sxs-lookup"><span data-stu-id="89d61-159">The dashboard also gives you access to:</span></span>
- <span data-ttu-id="89d61-160">Inscription de l’application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="89d61-160">Disconnect session</span></span>
- <span data-ttu-id="89d61-161">Télécharger des fichiers dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89d61-161">Upload files to the library</span></span> 
- <span data-ttu-id="89d61-162">Console de commande</span><span class="sxs-lookup"><span data-stu-id="89d61-162">Command console</span></span>
- <span data-ttu-id="89d61-163">Journal des commandes</span><span class="sxs-lookup"><span data-stu-id="89d61-163">Command log</span></span>


## <a name="initiate-a-live-response-session-on-a-device"></a><span data-ttu-id="89d61-164">Lancer une session de réponse en direct sur un appareil</span><span class="sxs-lookup"><span data-stu-id="89d61-164">Initiate a live response session on a device</span></span> 

1. <span data-ttu-id="89d61-165">Connectez-vous au Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="89d61-165">Sign in to Microsoft Defender Security Center.</span></span>

2. <span data-ttu-id="89d61-166">Accédez à la page de liste des appareils et sélectionnez un appareil à examiner.</span><span class="sxs-lookup"><span data-stu-id="89d61-166">Navigate to the devices list page and select a device to investigate.</span></span> <span data-ttu-id="89d61-167">La page appareils s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="89d61-167">The devices page opens.</span></span>

3. <span data-ttu-id="89d61-168">Lancez la session de réponse en direct en sélectionnant **Lancer la session de réponse en direct.**</span><span class="sxs-lookup"><span data-stu-id="89d61-168">Launch the live response session by selecting **Initiate live response session**.</span></span> <span data-ttu-id="89d61-169">Une console de commande s'affiche.</span><span class="sxs-lookup"><span data-stu-id="89d61-169">A command console is displayed.</span></span> <span data-ttu-id="89d61-170">Patientez pendant que la session se connecte à l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-170">Wait while the session connects to the device.</span></span>

4. <span data-ttu-id="89d61-171">Utilisez les commandes intégrées pour faire des enquêtes.</span><span class="sxs-lookup"><span data-stu-id="89d61-171">Use the built-in commands to do investigative work.</span></span> <span data-ttu-id="89d61-172">Pour plus d'informations, voir [commandes de réponse en direct.](#live-response-commands)</span><span class="sxs-lookup"><span data-stu-id="89d61-172">For more information, see [Live response commands](#live-response-commands).</span></span>

5. <span data-ttu-id="89d61-173">Une fois l'examen terminé, sélectionnez **Déconnecter la session,** puis **confirmez.**</span><span class="sxs-lookup"><span data-stu-id="89d61-173">After completing your investigation, select **Disconnect session**, then select **Confirm**.</span></span>

## <a name="live-response-commands"></a><span data-ttu-id="89d61-174">Commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="89d61-174">Live response commands</span></span>

<span data-ttu-id="89d61-175">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="89d61-175">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="89d61-176">Les autorisations utilisateur sont contrôlées par des rôles personnalisés RBAC.</span><span class="sxs-lookup"><span data-stu-id="89d61-176">User permissions are controlled by RBAC custom roles.</span></span> <span data-ttu-id="89d61-177">Pour plus d'informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-177">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 


>[!NOTE]
><span data-ttu-id="89d61-178">La réponse en direct est un environnement de ligne de commande interactif basé sur le cloud, de ce fait, une expérience de commande spécifique peut varier en temps de réponse en fonction de la qualité du réseau et de la charge système entre l'utilisateur final et l'appareil cible.</span><span class="sxs-lookup"><span data-stu-id="89d61-178">Live response is a cloud-based interactive shell, as such, specific command experience may vary in response time depending on network quality and system load between the end user and the target device.</span></span>

### <a name="basic-commands"></a><span data-ttu-id="89d61-179">Commandes de base</span><span class="sxs-lookup"><span data-stu-id="89d61-179">Basic commands</span></span>

<span data-ttu-id="89d61-180">Les commandes suivantes sont disponibles pour les rôles  d'utilisateur qui ont la possibilité d'exécuter des commandes de réponse en direct de base.</span><span class="sxs-lookup"><span data-stu-id="89d61-180">The following commands are available for user roles that are granted the ability to run **basic** live response commands.</span></span> <span data-ttu-id="89d61-181">Pour plus d'informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-181">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

| <span data-ttu-id="89d61-182">Command</span><span class="sxs-lookup"><span data-stu-id="89d61-182">Command</span></span> | <span data-ttu-id="89d61-183">Description</span><span class="sxs-lookup"><span data-stu-id="89d61-183">Description</span></span> |
|---|---|--- |
|`cd` | <span data-ttu-id="89d61-184">Modifie le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="89d61-184">Changes the current directory.</span></span> | 
|`cls` | <span data-ttu-id="89d61-185">Cette commande permet d'effacer l'écran de la console.</span><span class="sxs-lookup"><span data-stu-id="89d61-185">Clears the console screen.</span></span>  |
|`connect` | <span data-ttu-id="89d61-186">Lance une session de réponse en direct sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-186">Initiates a live response session to the device.</span></span> |
|`connections` | <span data-ttu-id="89d61-187">Affiche toutes les connexions actives.</span><span class="sxs-lookup"><span data-stu-id="89d61-187">Shows all the active connections.</span></span> |
|`dir` | <span data-ttu-id="89d61-188">Affiche une liste de fichiers et de sous-répertoires dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="89d61-188">Shows a list of files and subdirectories in a directory.</span></span> |
|`download <file_path> &` | <span data-ttu-id="89d61-189">Télécharge un fichier en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="89d61-189">Downloads a file in the background.</span></span> |
|`drivers` |  <span data-ttu-id="89d61-190">Affiche tous les pilotes installés sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-190">Shows all drivers installed on the device.</span></span> |
|`fg <command ID>` | <span data-ttu-id="89d61-191">Placez le travail spécifié au premier plan au premier plan, ce qui en fait le travail actuel.</span><span class="sxs-lookup"><span data-stu-id="89d61-191">Place the specified job in the foreground in the foreground, making it the current job.</span></span> <br> <span data-ttu-id="89d61-192">REMARQUE : fg prend un « ID de commande » disponible à partir des travaux, et non d'un piD</span><span class="sxs-lookup"><span data-stu-id="89d61-192">NOTE: fg takes a “command ID” available from jobs, not a PID</span></span> |
|`fileinfo` | <span data-ttu-id="89d61-193">Récupération d’informations sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="89d61-193">Get information about a file.</span></span> |
|`findfile` | <span data-ttu-id="89d61-194">Localise les fichiers d'un nom donné sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-194">Locates files by a given name on the device.</span></span> |
|`getfile <file_path>` | <span data-ttu-id="89d61-195">Télécharge un fichier.</span><span class="sxs-lookup"><span data-stu-id="89d61-195">Downloads a file.</span></span> |
|`help` | <span data-ttu-id="89d61-196">Fournit des informations d'aide pour les commandes de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="89d61-196">Provides help information for live response commands.</span></span> |
|`jobs` | <span data-ttu-id="89d61-197">Indique les travaux en cours d'exécution, leur ID et leur état.</span><span class="sxs-lookup"><span data-stu-id="89d61-197">Shows currently running jobs, their ID and status.</span></span> |
|`persistence` | <span data-ttu-id="89d61-198">Affiche toutes les méthodes de persistance connues sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-198">Shows all known persistence methods on the device.</span></span> |
|`processes` | <span data-ttu-id="89d61-199">Affiche tous les processus en cours d'exécution sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-199">Shows all processes running on the device.</span></span> |
|`registry` | <span data-ttu-id="89d61-200">Affiche les valeurs du Registre.</span><span class="sxs-lookup"><span data-stu-id="89d61-200">Shows registry values.</span></span> |
|`scheduledtasks` | <span data-ttu-id="89d61-201">Affiche toutes les tâches programmées sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-201">Shows all scheduled tasks on the device.</span></span> |
|`services` | <span data-ttu-id="89d61-202">Affiche tous les services sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-202">Shows all services on the device.</span></span> |
|`trace` | <span data-ttu-id="89d61-203">Définit le mode de journalisation du terminal pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="89d61-203">Sets the terminal's logging mode to debug.</span></span> |

### <a name="advanced-commands"></a><span data-ttu-id="89d61-204">Commandes avancées</span><span class="sxs-lookup"><span data-stu-id="89d61-204">Advanced commands</span></span>
<span data-ttu-id="89d61-205">Les commandes suivantes sont disponibles pour les rôles d'utilisateur qui ont la possibilité d'exécuter des **commandes** de réponse en direct avancées.</span><span class="sxs-lookup"><span data-stu-id="89d61-205">The following commands are available for user roles that are granted the ability to run **advanced** live response commands.</span></span> <span data-ttu-id="89d61-206">Pour plus d'informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-206">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

| <span data-ttu-id="89d61-207">Command</span><span class="sxs-lookup"><span data-stu-id="89d61-207">Command</span></span> | <span data-ttu-id="89d61-208">Description</span><span class="sxs-lookup"><span data-stu-id="89d61-208">Description</span></span> |
|---|---|
| `analyze` | <span data-ttu-id="89d61-209">Analyse l'entité avec différents moteurs d'incrimination pour parvenir à un verdict.</span><span class="sxs-lookup"><span data-stu-id="89d61-209">Analyses the entity with various incrimination engines to reach a verdict.</span></span> |
| `run` | <span data-ttu-id="89d61-210">Exécute un script PowerShell à partir de la bibliothèque sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-210">Runs a PowerShell script from the library on the device.</span></span> |
| `library` | <span data-ttu-id="89d61-211">Répertorie les fichiers qui ont été chargés dans la bibliothèque de réponses en direct.</span><span class="sxs-lookup"><span data-stu-id="89d61-211">Lists files that were uploaded to the live response library.</span></span> |
| `putfile` | <span data-ttu-id="89d61-212">Place un fichier de la bibliothèque sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-212">Puts a file from the library to the device.</span></span> <span data-ttu-id="89d61-213">Les fichiers sont enregistrés dans un dossier de travail et supprimés lorsque l'appareil redémarre par défaut.</span><span class="sxs-lookup"><span data-stu-id="89d61-213">Files are saved in a working folder and are deleted when the device restarts by default.</span></span> |
| `remediate` | <span data-ttu-id="89d61-214">Remédie à une entité sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="89d61-214">Remediates an entity on the device.</span></span> <span data-ttu-id="89d61-215">L'action de correction varie en fonction du type d'entité :</span><span class="sxs-lookup"><span data-stu-id="89d61-215">The remediation action will vary depending on the entity type:</span></span><br><span data-ttu-id="89d61-216">- Fichier : supprimer</span><span class="sxs-lookup"><span data-stu-id="89d61-216">- File: delete</span></span><br><span data-ttu-id="89d61-217">- Processus : arrêter, supprimer un fichier image</span><span class="sxs-lookup"><span data-stu-id="89d61-217">- Process: stop, delete image file</span></span><br><span data-ttu-id="89d61-218">- Service : arrêter, supprimer un fichier image</span><span class="sxs-lookup"><span data-stu-id="89d61-218">- Service: stop, delete image file</span></span><br><span data-ttu-id="89d61-219">- Entrée de Registre : supprimer</span><span class="sxs-lookup"><span data-stu-id="89d61-219">- Registry entry: delete</span></span><br><span data-ttu-id="89d61-220">- Tâche programmée : supprimer</span><span class="sxs-lookup"><span data-stu-id="89d61-220">- Scheduled task: remove</span></span><br><span data-ttu-id="89d61-221">- Élément de dossier de démarrage : supprimer un fichier</span><span class="sxs-lookup"><span data-stu-id="89d61-221">- Startup folder item: delete file</span></span> <br> <span data-ttu-id="89d61-222">REMARQUE : cette commande est une commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="89d61-222">NOTE: This command has a prerequisite command.</span></span> <span data-ttu-id="89d61-223">Vous pouvez utiliser la `-auto` commande conjointement pour `remediate` exécuter automatiquement la commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="89d61-223">You can use the `-auto` command in conjunction with `remediate` to automatically run the prerequisite command.</span></span> 
|`undo` | <span data-ttu-id="89d61-224">Restaure une entité qui a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="89d61-224">Restores an entity that was remediated.</span></span> |


## <a name="use-live-response-commands"></a><span data-ttu-id="89d61-225">Utiliser des commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="89d61-225">Use live response commands</span></span>

<span data-ttu-id="89d61-226">Les commandes que vous pouvez utiliser dans la console suivent les mêmes principes que les [commandes Windows.](https://docs.microsoft.com/windows-server/administration/windows-commands/windows-commands#BKMK_c)</span><span class="sxs-lookup"><span data-stu-id="89d61-226">The commands that you can use in the console follow similar principles as [Windows Commands](https://docs.microsoft.com/windows-server/administration/windows-commands/windows-commands#BKMK_c).</span></span>

<span data-ttu-id="89d61-227">Les commandes avancées offrent un ensemble plus robuste d'actions qui vous permettent d'exécuter des actions plus puissantes telles que télécharger et télécharger un fichier, exécuter des scripts sur l'appareil et prendre des mesures correctives sur une entité.</span><span class="sxs-lookup"><span data-stu-id="89d61-227">The advanced commands offer a more robust set of actions that allow you to take more powerful actions such as download and upload a file, run scripts on the device, and take remediation actions on an entity.</span></span>

### <a name="get-a-file-from-the-device"></a><span data-ttu-id="89d61-228">Obtenir un fichier à partir de l'appareil</span><span class="sxs-lookup"><span data-stu-id="89d61-228">Get a file from the device</span></span>

<span data-ttu-id="89d61-229">Pour les scénarios où vous souhaitez obtenir un fichier à partir d'un appareil que vous examinez, vous pouvez utiliser la `getfile` commande.</span><span class="sxs-lookup"><span data-stu-id="89d61-229">For scenarios when you'd like get a file from a device you're investigating, you can use the `getfile` command.</span></span> <span data-ttu-id="89d61-230">Cela vous permet d'enregistrer le fichier à partir de l'appareil pour une investigation plus approfondie.</span><span class="sxs-lookup"><span data-stu-id="89d61-230">This allows you to save the file from the device for further investigation.</span></span>

>[!NOTE]
><span data-ttu-id="89d61-231">Les limites de taille de fichier suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="89d61-231">The following file size limits apply:</span></span>
>- <span data-ttu-id="89d61-232">`getfile` limite : 3 Go</span><span class="sxs-lookup"><span data-stu-id="89d61-232">`getfile` limit: 3 GB</span></span>
>- <span data-ttu-id="89d61-233">`fileinfo` limite : 10 Go</span><span class="sxs-lookup"><span data-stu-id="89d61-233">`fileinfo` limit: 10 GB</span></span>
>- <span data-ttu-id="89d61-234">`library` limite : 250 Mo</span><span class="sxs-lookup"><span data-stu-id="89d61-234">`library` limit: 250 MB</span></span>

### <a name="download-a-file-in-the-background"></a><span data-ttu-id="89d61-235">Télécharger un fichier en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="89d61-235">Download a file in the background</span></span>

<span data-ttu-id="89d61-236">Pour permettre à votre équipe des opérations de sécurité de continuer à examiner un appareil touché, les fichiers peuvent désormais être téléchargés en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="89d61-236">To enable your security operations team to continue investigating an impacted device, files can now be downloaded in the background.</span></span>

- <span data-ttu-id="89d61-237">Pour télécharger un fichier en arrière-plan, dans la console de commande de réponse en direct, tapez `download <file_path> &` .</span><span class="sxs-lookup"><span data-stu-id="89d61-237">To download a file in the background, in the live response command console, type `download <file_path> &`.</span></span>
- <span data-ttu-id="89d61-238">Si vous attendez le téléchargement d'un fichier, vous pouvez le déplacer vers l'arrière-plan à l'aide de Ctrl + Z.</span><span class="sxs-lookup"><span data-stu-id="89d61-238">If you are waiting for a file to be downloaded, you can move it to the background by using Ctrl + Z.</span></span>
- <span data-ttu-id="89d61-239">Pour mettre un téléchargement de fichier au premier plan, dans la console de commande de réponse en direct, tapez `fg <command_id>` .</span><span class="sxs-lookup"><span data-stu-id="89d61-239">To bring a file download to the foreground, in the live response command console, type `fg <command_id>`.</span></span>

<span data-ttu-id="89d61-240">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="89d61-240">Here are some examples:</span></span>


|<span data-ttu-id="89d61-241">Commande</span><span class="sxs-lookup"><span data-stu-id="89d61-241">Command</span></span>  |<span data-ttu-id="89d61-242">Fonction</span><span class="sxs-lookup"><span data-stu-id="89d61-242">What it does</span></span>  |
|---------|---------|
|`Download "C:\windows\some_file.exe" &`     |<span data-ttu-id="89d61-243">Commence à télécharger un fichier nommé *some_file.exe* en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="89d61-243">Starts downloading a file named *some_file.exe* in the background.</span></span>         |
|`fg 1234`     |<span data-ttu-id="89d61-244">Renvoie un téléchargement avec l'ID de commande *1234* au premier plan.</span><span class="sxs-lookup"><span data-stu-id="89d61-244">Returns a download with command ID *1234* to the foreground.</span></span>         |


### <a name="put-a-file-in-the-library"></a><span data-ttu-id="89d61-245">Placer un fichier dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89d61-245">Put a file in the library</span></span>

<span data-ttu-id="89d61-246">La réponse en direct dispose d'une bibliothèque dans laquelle vous pouvez placer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="89d61-246">Live response has a library where you can put files into.</span></span> <span data-ttu-id="89d61-247">La bibliothèque stocke les fichiers (tels que les scripts) qui peuvent être exécutés dans une session de réponse en direct au niveau du client.</span><span class="sxs-lookup"><span data-stu-id="89d61-247">The library stores files (such as scripts) that can be run in a live response session at the tenant level.</span></span>

<span data-ttu-id="89d61-248">La réponse en direct permet aux scripts PowerShell de s'exécuter, mais vous devez d'abord placer les fichiers dans la bibliothèque avant de pouvoir les exécuter.</span><span class="sxs-lookup"><span data-stu-id="89d61-248">Live response allows PowerShell scripts to run, however you must first put the files into the library before you can run them.</span></span> 

<span data-ttu-id="89d61-249">Vous pouvez avoir une collection de scripts PowerShell qui peuvent s'exécuter sur les appareils avec qui vous lancez des sessions de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="89d61-249">You can have a collection of PowerShell scripts that can run on devices that you initiate live response sessions with.</span></span> 

#### <a name="to-upload-a-file-in-the-library"></a><span data-ttu-id="89d61-250">Pour télécharger un fichier dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89d61-250">To upload a file in the library</span></span>

1. <span data-ttu-id="89d61-251">Cliquez **sur Télécharger le fichier dans la bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="89d61-251">Click **Upload file to library**.</span></span> 

2. <span data-ttu-id="89d61-252">Cliquez **sur Parcourir** et sélectionnez le fichier.</span><span class="sxs-lookup"><span data-stu-id="89d61-252">Click **Browse** and select the file.</span></span>

3. <span data-ttu-id="89d61-253">Fournissez une brève description.</span><span class="sxs-lookup"><span data-stu-id="89d61-253">Provide a brief description.</span></span>

4. <span data-ttu-id="89d61-254">Spécifiez si vous souhaitez réécrire un fichier du même nom.</span><span class="sxs-lookup"><span data-stu-id="89d61-254">Specify if you'd like to overwrite a file with the same name.</span></span>

5. <span data-ttu-id="89d61-255">Si vous le souhaitez, connaissez les paramètres nécessaires pour le script, cochez la case des paramètres de script.</span><span class="sxs-lookup"><span data-stu-id="89d61-255">If you'd like to be,  know what parameters are needed for the script, select the script parameters check box.</span></span> <span data-ttu-id="89d61-256">Dans le champ de texte, entrez un exemple et une description.</span><span class="sxs-lookup"><span data-stu-id="89d61-256">In the text field, enter an example and a description.</span></span>

6. <span data-ttu-id="89d61-257">Cliquez sur **Confirmer.**</span><span class="sxs-lookup"><span data-stu-id="89d61-257">Click **Confirm**.</span></span> 

7. <span data-ttu-id="89d61-258">(Facultatif) Pour vérifier que le fichier a été chargé dans la bibliothèque, exécutez la `library` commande.</span><span class="sxs-lookup"><span data-stu-id="89d61-258">(Optional) To verify that the file was uploaded to the library, run the `library` command.</span></span>


### <a name="cancel-a-command"></a><span data-ttu-id="89d61-259">Annuler une commande</span><span class="sxs-lookup"><span data-stu-id="89d61-259">Cancel a command</span></span>
<span data-ttu-id="89d61-260">À tout moment pendant une session, vous pouvez annuler une commande en appuyant sur Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="89d61-260">Anytime during a session, you can cancel a command by pressing CTRL + C.</span></span>  

>[!WARNING]
><span data-ttu-id="89d61-261">L'utilisation de ce raccourci n'arrête pas la commande côté agent.</span><span class="sxs-lookup"><span data-stu-id="89d61-261">Using this shortcut will not stop the command in the agent side.</span></span> <span data-ttu-id="89d61-262">Il annule uniquement la commande dans le portail.</span><span class="sxs-lookup"><span data-stu-id="89d61-262">It will only cancel the command in the portal.</span></span> <span data-ttu-id="89d61-263">Ainsi, la modification des opérations telles que la « correction » peut se poursuivre, pendant l'annulation de la commande.</span><span class="sxs-lookup"><span data-stu-id="89d61-263">So, changing operations such as "remediate" may continue, while the command is canceled.</span></span> 

### <a name="automatically-run-prerequisite-commands"></a><span data-ttu-id="89d61-264">Exécuter automatiquement les commandes prérequises</span><span class="sxs-lookup"><span data-stu-id="89d61-264">Automatically run prerequisite commands</span></span>

<span data-ttu-id="89d61-265">Certaines commandes ont des commandes prérequises à exécuter.</span><span class="sxs-lookup"><span data-stu-id="89d61-265">Some commands have prerequisite commands to run.</span></span> <span data-ttu-id="89d61-266">Si vous n'exécutez pas la commande prérequise, vous obtenez une erreur.</span><span class="sxs-lookup"><span data-stu-id="89d61-266">If you don't run the prerequisite command, you'll get an error.</span></span> <span data-ttu-id="89d61-267">Par exemple, l'exécution `download` de la commande sans `fileinfo` renvoyer d'erreur.</span><span class="sxs-lookup"><span data-stu-id="89d61-267">For example, running the `download` command without `fileinfo` will return an error.</span></span>

<span data-ttu-id="89d61-268">Vous pouvez utiliser l'indicateur automatique pour exécuter automatiquement les commandes prérequises, par exemple :</span><span class="sxs-lookup"><span data-stu-id="89d61-268">You can use the auto flag to automatically run prerequisite commands, for example:</span></span>

```console
getfile c:\Users\user\Desktop\work.txt -auto
```

## <a name="run-a-powershell-script"></a><span data-ttu-id="89d61-269">Exécuter un script PowerShell</span><span class="sxs-lookup"><span data-stu-id="89d61-269">Run a PowerShell script</span></span> 

<span data-ttu-id="89d61-270">Avant de pouvoir exécuter un script PowerShell, vous devez d'abord le télécharger dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="89d61-270">Before you can run a PowerShell script, you must first upload it to the library.</span></span> 

<span data-ttu-id="89d61-271">Après avoir téléchargé le script dans la bibliothèque, utilisez `run` la commande pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="89d61-271">After uploading the script to the library, use the `run` command to run the script.</span></span>

<span data-ttu-id="89d61-272">Si vous envisagez d'utiliser un script non signé dans la session, vous devez activer le paramètre dans la page Paramètres des [fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="89d61-272">If you plan to use an unsigned script in the session, you'll need to enable the setting in the [Advanced features settings](advanced-features.md) page.</span></span>

>[!WARNING]
><span data-ttu-id="89d61-273">Autoriser l'utilisation de scripts non signés peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="89d61-273">Allowing the use of unsigned scripts may increase your exposure to threats.</span></span>

## <a name="apply-command-parameters"></a><span data-ttu-id="89d61-274">Appliquer des paramètres de commande</span><span class="sxs-lookup"><span data-stu-id="89d61-274">Apply command parameters</span></span>

- <span data-ttu-id="89d61-275">Consultez l'aide de la console pour en savoir plus sur les paramètres de commande.</span><span class="sxs-lookup"><span data-stu-id="89d61-275">View the console help to learn about command parameters.</span></span> <span data-ttu-id="89d61-276">Pour en savoir plus sur une commande individuelle, exécutez :</span><span class="sxs-lookup"><span data-stu-id="89d61-276">To learn about an individual command, run:</span></span>
 
    `help <command name>`

- <span data-ttu-id="89d61-277">Lorsque vous appliquez des paramètres aux commandes, notez que les paramètres sont gérés selon un ordre fixe :</span><span class="sxs-lookup"><span data-stu-id="89d61-277">When applying parameters to commands, note that parameters are handled based on a fixed order:</span></span>
 
    `<command name> param1 param2` 

- <span data-ttu-id="89d61-278">Lorsque vous spécifiez des paramètres en dehors de l'ordre fixe, spécifiez le nom du paramètre avec un tiret avant de fournir la valeur :</span><span class="sxs-lookup"><span data-stu-id="89d61-278">When specifying parameters outside of the fixed order, specify the name of the parameter with a hyphen before providing the value:</span></span>
 
    `<command name> -param2_name param2`

- <span data-ttu-id="89d61-279">Lorsque vous utilisez des commandes qui ont des commandes prérequises, vous pouvez utiliser des indicateurs :</span><span class="sxs-lookup"><span data-stu-id="89d61-279">When using commands that have prerequisite commands, you can use flags:</span></span>

    <span data-ttu-id="89d61-280">`<command name> -type file -id <file path> - auto` ou `remediate file <file path> - auto`.</span><span class="sxs-lookup"><span data-stu-id="89d61-280">`<command name> -type file -id <file path> - auto` or `remediate file <file path> - auto`.</span></span>

## <a name="supported-output-types"></a><span data-ttu-id="89d61-281">Types de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="89d61-281">Supported output types</span></span>

<span data-ttu-id="89d61-282">La réponse en direct prend en charge les types de sortie de tableau et de format JSON.</span><span class="sxs-lookup"><span data-stu-id="89d61-282">Live response supports table and JSON format output types.</span></span> <span data-ttu-id="89d61-283">Pour chaque commande, il existe un comportement de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="89d61-283">For each command, there's a default output behavior.</span></span> <span data-ttu-id="89d61-284">Vous pouvez modifier la sortie dans votre format de sortie préféré à l'aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="89d61-284">You can modify the output in your preferred output format using the following commands:</span></span>

- `-output json`
- `-output table`

>[!NOTE]
><span data-ttu-id="89d61-285">Moins de champs sont affichés au format tableau en raison de l'espace limité.</span><span class="sxs-lookup"><span data-stu-id="89d61-285">Fewer fields are shown in table format due to the limited space.</span></span> <span data-ttu-id="89d61-286">Pour voir plus de détails dans la sortie, vous pouvez utiliser la commande de sortie JSON afin que d'autres détails soient affichés.</span><span class="sxs-lookup"><span data-stu-id="89d61-286">To see more details in the output, you can use the JSON output command so that more details are shown.</span></span>

## <a name="supported-output-pipes"></a><span data-ttu-id="89d61-287">Canaux de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="89d61-287">Supported output pipes</span></span>

<span data-ttu-id="89d61-288">La réponse en direct prend en charge le système de sortie vers l'CLI et le fichier.</span><span class="sxs-lookup"><span data-stu-id="89d61-288">Live response supports output piping to CLI and file.</span></span> <span data-ttu-id="89d61-289">L'CLI est le comportement de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="89d61-289">CLI is the default output behavior.</span></span> <span data-ttu-id="89d61-290">Vous pouvez canaliser la sortie vers un fichier à l'aide de la commande suivante : [command] > [filename].txt.</span><span class="sxs-lookup"><span data-stu-id="89d61-290">You can pipe the output to a file using the following command: [command] > [filename].txt.</span></span>  

<span data-ttu-id="89d61-291">Exemple :</span><span class="sxs-lookup"><span data-stu-id="89d61-291">Example:</span></span>

```console
processes > output.txt
```

## <a name="view-the-command-log"></a><span data-ttu-id="89d61-292">Afficher le journal de commandes</span><span class="sxs-lookup"><span data-stu-id="89d61-292">View the command log</span></span>

<span data-ttu-id="89d61-293">Sélectionnez **l'onglet Journal** de commandes pour voir les commandes utilisées sur l'appareil au cours d'une session.</span><span class="sxs-lookup"><span data-stu-id="89d61-293">Select the **Command log** tab to see the commands used on the device during a session.</span></span> <span data-ttu-id="89d61-294">Chaque commande est suivi avec des détails complets tels que :</span><span class="sxs-lookup"><span data-stu-id="89d61-294">Each command is tracked with full details such as:</span></span>
- <span data-ttu-id="89d61-295">ID</span><span class="sxs-lookup"><span data-stu-id="89d61-295">ID</span></span>
- <span data-ttu-id="89d61-296">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="89d61-296">Command line</span></span>
- <span data-ttu-id="89d61-297">Duration</span><span class="sxs-lookup"><span data-stu-id="89d61-297">Duration</span></span>
- <span data-ttu-id="89d61-298">Barre côté état et entrée ou sortie</span><span class="sxs-lookup"><span data-stu-id="89d61-298">Status and input or output side bar</span></span>

## <a name="limitations"></a><span data-ttu-id="89d61-299">Limites</span><span class="sxs-lookup"><span data-stu-id="89d61-299">Limitations</span></span>

- <span data-ttu-id="89d61-300">Les sessions de réponse en direct sont limitées à 25 sessions de réponse en direct à la fois.</span><span class="sxs-lookup"><span data-stu-id="89d61-300">Live response sessions are limited to 25 live response sessions at a time.</span></span>
- <span data-ttu-id="89d61-301">Le délai d'inactivité de la session de réponse en direct est de 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="89d61-301">Live response session inactive timeout value is 30 minutes.</span></span> 
- <span data-ttu-id="89d61-302">Un utilisateur peut démarrer jusqu'à 10 sessions simultanées.</span><span class="sxs-lookup"><span data-stu-id="89d61-302">A user can initiate up to 10 concurrent sessions.</span></span>
- <span data-ttu-id="89d61-303">Un appareil ne peut être connecté qu'à une seule session à la fois.</span><span class="sxs-lookup"><span data-stu-id="89d61-303">A device can only be in one session at a time.</span></span>
- <span data-ttu-id="89d61-304">Les limites de taille de fichier suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="89d61-304">The following file size limits apply:</span></span>
   - <span data-ttu-id="89d61-305">`getfile` limite : 3 Go</span><span class="sxs-lookup"><span data-stu-id="89d61-305">`getfile` limit: 3 GB</span></span>
   - <span data-ttu-id="89d61-306">`fileinfo` limite : 10 Go</span><span class="sxs-lookup"><span data-stu-id="89d61-306">`fileinfo` limit: 10 GB</span></span>
   - <span data-ttu-id="89d61-307">`library` limite : 250 Mo</span><span class="sxs-lookup"><span data-stu-id="89d61-307">`library` limit: 250 MB</span></span>

## <a name="related-article"></a><span data-ttu-id="89d61-308">Article connexe</span><span class="sxs-lookup"><span data-stu-id="89d61-308">Related article</span></span>
- [<span data-ttu-id="89d61-309">Exemples de commande Live response</span><span class="sxs-lookup"><span data-stu-id="89d61-309">Live response command examples</span></span>](live-response-command-examples.md)
