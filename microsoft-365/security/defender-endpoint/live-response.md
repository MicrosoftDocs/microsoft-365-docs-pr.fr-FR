---
title: Examiner les entités sur les appareils à l’aide de la réponse en direct dans Microsoft Defender pour le point de terminaison
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
ms.openlocfilehash: d5e48f1e4f6bc2cfaa836d90e24f2ce8ba3f2114
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52845329"
---
# <a name="investigate-entities-on-devices-using-live-response"></a><span data-ttu-id="5a425-104">Examiner les entités sur les appareils à l’aide de la réponse en direct</span><span class="sxs-lookup"><span data-stu-id="5a425-104">Investigate entities on devices using live response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5a425-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5a425-105">**Applies to:**</span></span>
- [<span data-ttu-id="5a425-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5a425-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5a425-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5a425-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="5a425-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="5a425-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="5a425-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5a425-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="5a425-110">La réponse en direct permet aux équipes d’opérations de sécurité d’accéder instantanément à un appareil (également appelé ordinateur) à l’aide d’une connexion shell distante.</span><span class="sxs-lookup"><span data-stu-id="5a425-110">Live response gives security operations teams instantaneous access to a device (also referred to as a machine) using a remote shell connection.</span></span> <span data-ttu-id="5a425-111">Cela vous donne la puissance d’un travail d’examen approfondi et de prendre des mesures de réponse immédiates pour contenir rapidement des menaces identifiées, en temps réel.</span><span class="sxs-lookup"><span data-stu-id="5a425-111">This gives you the power to do in-depth investigative work and take immediate response actions to promptly contain identified threats—in real time.</span></span> 

<span data-ttu-id="5a425-112">La réponse dynamique est conçue pour améliorer les enquêtes en permettant à votre équipe des opérations de sécurité de collecter des données d’investigation, d’exécuter des scripts, d’envoyer des entités suspectes pour analyse, de corriger les menaces et de chercher de manière proactive les menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="5a425-112">Live response is designed to enhance investigations by enabling your security operations team to collect forensic data, run scripts, send suspicious entities for analysis, remediate threats, and proactively hunt for emerging threats.</span></span><br/><br/>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4qLUW]

<span data-ttu-id="5a425-113">Avec la réponse en direct, les analystes peuvent effectuer toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a425-113">With live response, analysts can do all of the following tasks:</span></span>
- <span data-ttu-id="5a425-114">Exécutez des commandes de base et avancées pour faire des investigations sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-114">Run basic and advanced commands to do investigative work on a device.</span></span>
- <span data-ttu-id="5a425-115">Téléchargez des fichiers tels que des exemples de programmes malveillants et les résultats des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a425-115">Download files such as malware samples and outcomes of PowerShell scripts.</span></span>
- <span data-ttu-id="5a425-116">Téléchargez des fichiers en arrière-plan (nouveau !).</span><span class="sxs-lookup"><span data-stu-id="5a425-116">Download files in the background (new!).</span></span>
- <span data-ttu-id="5a425-117">Télécharger un script PowerShell ou un exécutable dans la bibliothèque et exécutez-le sur un appareil à partir d’un niveau client.</span><span class="sxs-lookup"><span data-stu-id="5a425-117">Upload a PowerShell script or executable to the library and run it on a device from a tenant level.</span></span>
- <span data-ttu-id="5a425-118">Prendre ou annuler des actions de correction.</span><span class="sxs-lookup"><span data-stu-id="5a425-118">Take or undo remediation actions.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="5a425-119">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5a425-119">Before you begin</span></span>

<span data-ttu-id="5a425-120">Avant de lancer une session sur un appareil, veillez à respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a425-120">Before you can initiate a session on a device, make sure you fulfill the following requirements:</span></span>

- <span data-ttu-id="5a425-121">**Vérifiez que vous exécutez une version prise en charge de Windows**.</span><span class="sxs-lookup"><span data-stu-id="5a425-121">**Verify that you're running a supported version of Windows**.</span></span> <br/>
<span data-ttu-id="5a425-122">Les appareils doivent être en cours d’exécution dans l’une des versions suivantes Windows</span><span class="sxs-lookup"><span data-stu-id="5a425-122">Devices must be running one of the following versions of Windows</span></span>

  - <span data-ttu-id="5a425-123">**Windows 10**</span><span class="sxs-lookup"><span data-stu-id="5a425-123">**Windows 10**</span></span>
    - <span data-ttu-id="5a425-124">[Version 1909 ou](/windows/whats-new/whats-new-windows-10-version-1909) ultérieure</span><span class="sxs-lookup"><span data-stu-id="5a425-124">[Version 1909](/windows/whats-new/whats-new-windows-10-version-1909) or later</span></span>  
    - <span data-ttu-id="5a425-125">[Version 1903 avec](/windows/whats-new/whats-new-windows-10-version-1903) [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)</span><span class="sxs-lookup"><span data-stu-id="5a425-125">[Version 1903](/windows/whats-new/whats-new-windows-10-version-1903) with [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)</span></span>
    - <span data-ttu-id="5a425-126">[Version 1809 (RS 5)](/windows/whats-new/whats-new-windows-10-version-1809) avec [KB4537818](https://support.microsoft.com/help/4537818/windows-10-update-kb4537818)</span><span class="sxs-lookup"><span data-stu-id="5a425-126">[Version 1809 (RS 5)](/windows/whats-new/whats-new-windows-10-version-1809) with [with KB4537818](https://support.microsoft.com/help/4537818/windows-10-update-kb4537818)</span></span>
    - <span data-ttu-id="5a425-127">[Version 1803 (RS 4)](/windows/whats-new/whats-new-windows-10-version-1803) avec [KB4537795](https://support.microsoft.com/help/4537795/windows-10-update-kb4537795)</span><span class="sxs-lookup"><span data-stu-id="5a425-127">[Version 1803 (RS 4)](/windows/whats-new/whats-new-windows-10-version-1803) with [KB4537795](https://support.microsoft.com/help/4537795/windows-10-update-kb4537795)</span></span>
    - <span data-ttu-id="5a425-128">[Version 1709 (RS 3)](/windows/whats-new/whats-new-windows-10-version-1709) avec [KB4537816](https://support.microsoft.com/help/4537816/windows-10-update-kb4537816)</span><span class="sxs-lookup"><span data-stu-id="5a425-128">[Version 1709 (RS 3)](/windows/whats-new/whats-new-windows-10-version-1709) with [KB4537816](https://support.microsoft.com/help/4537816/windows-10-update-kb4537816)</span></span>
  
  - <span data-ttu-id="5a425-129">**Windows Server 2019 - Applicable uniquement pour la prévisualisation publique**</span><span class="sxs-lookup"><span data-stu-id="5a425-129">**Windows Server 2019 - Only applicable for Public preview**</span></span>
    - <span data-ttu-id="5a425-130">Version 1903 ou (avec [KB4515384)](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)ultérieure</span><span class="sxs-lookup"><span data-stu-id="5a425-130">Version 1903 or (with [KB4515384](https://support.microsoft.com/en-us/help/4515384/windows-10-update-kb4515384)) later</span></span> 
    - <span data-ttu-id="5a425-131">Version 1809 [(avec KB4537818)](https://support.microsoft.com/en-us/help/4537818/windows-10-update-kb4537818)</span><span class="sxs-lookup"><span data-stu-id="5a425-131">Version 1809 (with [KB4537818](https://support.microsoft.com/en-us/help/4537818/windows-10-update-kb4537818))</span></span>

- <span data-ttu-id="5a425-132">**Activez la réponse en direct à partir de la page paramètres avancés.**</span><span class="sxs-lookup"><span data-stu-id="5a425-132">**Enable live response from the advanced settings page**.</span></span><br>
<span data-ttu-id="5a425-133">Vous devez activer la fonctionnalité de réponse en direct dans la page [Paramètres des fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-133">You'll need to enable the live response capability in the [Advanced features settings](advanced-features.md) page.</span></span>

    >[!NOTE]
    ><span data-ttu-id="5a425-134">Seuls les utilisateurs ayant des rôles d’administrateur global ou de sécurité peuvent modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="5a425-134">Only users with manage security or global admin roles can edit these settings.</span></span>

- <span data-ttu-id="5a425-135">**Activez la réponse en direct pour les serveurs à partir de la page paramètres avancés** (recommandé).</span><span class="sxs-lookup"><span data-stu-id="5a425-135">**Enable live response for servers from the advanced settings page** (recommended).</span></span><br>

    >[!NOTE]
    ><span data-ttu-id="5a425-136">Seuls les utilisateurs ayant des rôles d’administrateur global ou de sécurité peuvent modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="5a425-136">Only users with manage security or global admin roles can edit these settings.</span></span>
    
- <span data-ttu-id="5a425-137">**Assurez-vous qu’un niveau de correction Automation** est affecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-137">**Ensure that the device has an Automation Remediation level assigned to it**.</span></span><br>
<span data-ttu-id="5a425-138">Vous devez activer, au moins, le niveau de correction minimal pour un groupe d’appareils donné.</span><span class="sxs-lookup"><span data-stu-id="5a425-138">You'll need to enable, at least, the minimum Remediation Level for a given Device Group.</span></span> <span data-ttu-id="5a425-139">Sinon, vous ne pourrez pas établir une session Live Response à un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="5a425-139">Otherwise you won't be able to establish a Live Response session to a member of that group.</span></span>

    <span data-ttu-id="5a425-140">Vous recevrez l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="5a425-140">You'll receive the following error:</span></span>

    ![Image du message d’erreur](images/live-response-error.png)

- <span data-ttu-id="5a425-142">**Activer l’exécution de script non signé de réponse en** direct (facultatif).</span><span class="sxs-lookup"><span data-stu-id="5a425-142">**Enable live response unsigned script execution** (optional).</span></span> <br>

    >[!WARNING]
    ><span data-ttu-id="5a425-143">Autoriser l’utilisation de scripts non signés peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="5a425-143">Allowing the use of unsigned scripts may increase your exposure to threats.</span></span>
 
  <span data-ttu-id="5a425-144">L’exécution de scripts non signés n’est pas recommandée, car elle peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="5a425-144">Running unsigned scripts is not recommended as it can increase your exposure to threats.</span></span> <span data-ttu-id="5a425-145">Si vous devez toutefois les utiliser, vous devez activer le paramètre dans la page [Paramètres des fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-145">If you must use them however, you'll need to enable the setting in the [Advanced features settings](advanced-features.md) page.</span></span>
    
- <span data-ttu-id="5a425-146">**Assurez-vous que vous avez les autorisations appropriées.**</span><span class="sxs-lookup"><span data-stu-id="5a425-146">**Ensure that you have the appropriate permissions**.</span></span><br>
    <span data-ttu-id="5a425-147">Seuls les utilisateurs qui ont été mis en service avec les autorisations appropriées peuvent lancer une session.</span><span class="sxs-lookup"><span data-stu-id="5a425-147">Only users who have been provisioned with the appropriate permissions can initiate a session.</span></span> <span data-ttu-id="5a425-148">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-148">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="5a425-149">L’option de téléchargement d’un fichier dans la bibliothèque est disponible uniquement pour les personnes ayant les autorisations RBAC appropriées.</span><span class="sxs-lookup"><span data-stu-id="5a425-149">The option to upload a file to the library is only available to those with the appropriate RBAC permissions.</span></span> <span data-ttu-id="5a425-150">Le bouton est grisé pour les utilisateurs ayant uniquement des autorisations déléguées.</span><span class="sxs-lookup"><span data-stu-id="5a425-150">The button is greyed out for users with only delegated permissions.</span></span>

    <span data-ttu-id="5a425-151">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="5a425-151">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="5a425-152">Les autorisations des utilisateurs sont contrôlées par le rôle personnalisé RBAC.</span><span class="sxs-lookup"><span data-stu-id="5a425-152">Users permissions are controlled by RBAC custom role.</span></span> 

## <a name="live-response-dashboard-overview"></a><span data-ttu-id="5a425-153">Vue d’ensemble du tableau de bord de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="5a425-153">Live response dashboard overview</span></span>
<span data-ttu-id="5a425-154">Lorsque vous lancez une session de réponse en direct sur un appareil, un tableau de bord s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5a425-154">When you initiate a live response session on a device, a dashboard opens.</span></span> <span data-ttu-id="5a425-155">Le tableau de bord fournit des informations sur la session, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a425-155">The dashboard provides information about the session such as the following:</span></span> 

- <span data-ttu-id="5a425-156">Qui créé la session</span><span class="sxs-lookup"><span data-stu-id="5a425-156">Who created the session</span></span>
- <span data-ttu-id="5a425-157">Au début de la session</span><span class="sxs-lookup"><span data-stu-id="5a425-157">When the session started</span></span>
- <span data-ttu-id="5a425-158">Durée de la session</span><span class="sxs-lookup"><span data-stu-id="5a425-158">The duration of the session</span></span>

<span data-ttu-id="5a425-159">Le tableau de bord vous donne également accès à :</span><span class="sxs-lookup"><span data-stu-id="5a425-159">The dashboard also gives you access to:</span></span>
- <span data-ttu-id="5a425-160">Inscription de l’application dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5a425-160">Disconnect session</span></span>
- <span data-ttu-id="5a425-161">Télécharger fichiers dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a425-161">Upload files to the library</span></span> 
- <span data-ttu-id="5a425-162">Console de commande</span><span class="sxs-lookup"><span data-stu-id="5a425-162">Command console</span></span>
- <span data-ttu-id="5a425-163">Journal des commandes</span><span class="sxs-lookup"><span data-stu-id="5a425-163">Command log</span></span>


## <a name="initiate-a-live-response-session-on-a-device"></a><span data-ttu-id="5a425-164">Lancer une session de réponse en direct sur un appareil</span><span class="sxs-lookup"><span data-stu-id="5a425-164">Initiate a live response session on a device</span></span> 

1. <span data-ttu-id="5a425-165">Connectez-vous à Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="5a425-165">Sign in to Microsoft Defender Security Center.</span></span>

2. <span data-ttu-id="5a425-166">Accédez à la page de liste des appareils et sélectionnez un appareil à examiner.</span><span class="sxs-lookup"><span data-stu-id="5a425-166">Navigate to the devices list page and select a device to investigate.</span></span> <span data-ttu-id="5a425-167">La page appareils s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5a425-167">The devices page opens.</span></span>

3. <span data-ttu-id="5a425-168">Lancez la session de réponse en direct en sélectionnant **Lancer la session de réponse en direct.**</span><span class="sxs-lookup"><span data-stu-id="5a425-168">Launch the live response session by selecting **Initiate live response session**.</span></span> <span data-ttu-id="5a425-169">Une console de commande s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5a425-169">A command console is displayed.</span></span> <span data-ttu-id="5a425-170">Patientez pendant que la session se connecte à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-170">Wait while the session connects to the device.</span></span>

4. <span data-ttu-id="5a425-171">Utilisez les commandes intégrées pour faire des enquêtes.</span><span class="sxs-lookup"><span data-stu-id="5a425-171">Use the built-in commands to do investigative work.</span></span> <span data-ttu-id="5a425-172">Pour plus d’informations, voir [commandes de réponse en direct.](#live-response-commands)</span><span class="sxs-lookup"><span data-stu-id="5a425-172">For more information, see [Live response commands](#live-response-commands).</span></span>

5. <span data-ttu-id="5a425-173">Une fois l’examen terminé, sélectionnez **Déconnecter la session,** puis **confirmez.**</span><span class="sxs-lookup"><span data-stu-id="5a425-173">After completing your investigation, select **Disconnect session**, then select **Confirm**.</span></span>

## <a name="live-response-commands"></a><span data-ttu-id="5a425-174">Commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="5a425-174">Live response commands</span></span>

<span data-ttu-id="5a425-175">Selon le rôle qui vous a été accordé, vous pouvez exécuter des commandes de réponse en direct de base ou avancées.</span><span class="sxs-lookup"><span data-stu-id="5a425-175">Depending on the role that's been granted to you, you can run basic or advanced live response commands.</span></span> <span data-ttu-id="5a425-176">Les autorisations utilisateur sont contrôlées par des rôles personnalisés RBAC.</span><span class="sxs-lookup"><span data-stu-id="5a425-176">User permissions are controlled by RBAC custom roles.</span></span> <span data-ttu-id="5a425-177">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-177">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 


>[!NOTE]
><span data-ttu-id="5a425-178">La réponse en direct est un environnement de ligne de commande interactif basé sur le cloud, de ce fait, une expérience de commande spécifique peut varier en temps de réponse en fonction de la qualité du réseau et de la charge système entre l’utilisateur final et l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="5a425-178">Live response is a cloud-based interactive shell, as such, specific command experience may vary in response time depending on network quality and system load between the end user and the target device.</span></span>

### <a name="basic-commands"></a><span data-ttu-id="5a425-179">Commandes de base</span><span class="sxs-lookup"><span data-stu-id="5a425-179">Basic commands</span></span>

<span data-ttu-id="5a425-180">Les commandes suivantes sont disponibles pour les rôles d’utilisateur qui ont la possibilité d’exécuter des commandes de réponse **en** direct de base.</span><span class="sxs-lookup"><span data-stu-id="5a425-180">The following commands are available for user roles that are granted the ability to run **basic** live response commands.</span></span> <span data-ttu-id="5a425-181">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-181">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

| <span data-ttu-id="5a425-182">Command</span><span class="sxs-lookup"><span data-stu-id="5a425-182">Command</span></span> | <span data-ttu-id="5a425-183">Description</span><span class="sxs-lookup"><span data-stu-id="5a425-183">Description</span></span> |
|---|---|--- |
|`cd` | <span data-ttu-id="5a425-184">Modifie le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="5a425-184">Changes the current directory.</span></span> | 
|`cls` | <span data-ttu-id="5a425-185">Cette commande permet d’effacer l’écran de la console.</span><span class="sxs-lookup"><span data-stu-id="5a425-185">Clears the console screen.</span></span>  |
|`connect` | <span data-ttu-id="5a425-186">Lance une session de réponse en direct sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-186">Initiates a live response session to the device.</span></span> |
|`connections` | <span data-ttu-id="5a425-187">Affiche toutes les connexions actives.</span><span class="sxs-lookup"><span data-stu-id="5a425-187">Shows all the active connections.</span></span> |
|`dir` | <span data-ttu-id="5a425-188">Affiche une liste de fichiers et de sous-répertoires dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="5a425-188">Shows a list of files and subdirectories in a directory.</span></span> |
|`drivers` |  <span data-ttu-id="5a425-189">Affiche tous les pilotes installés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-189">Shows all drivers installed on the device.</span></span> |
|`fg <command ID>` | <span data-ttu-id="5a425-190">Placez le travail spécifié au premier plan au premier plan, ce qui en fait le travail actuel.</span><span class="sxs-lookup"><span data-stu-id="5a425-190">Place the specified job in the foreground in the foreground, making it the current job.</span></span> <br> <span data-ttu-id="5a425-191">REMARQUE : fg prend un « ID de commande » disponible à partir des travaux, et non d’un piD</span><span class="sxs-lookup"><span data-stu-id="5a425-191">NOTE: fg takes a “command ID” available from jobs, not a PID</span></span> |
|`fileinfo` | <span data-ttu-id="5a425-192">Récupération d’informations sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="5a425-192">Get information about a file.</span></span> |
|`findfile` | <span data-ttu-id="5a425-193">Localise les fichiers d’un nom donné sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-193">Locates files by a given name on the device.</span></span> |
|`getfile <file_path>` | <span data-ttu-id="5a425-194">Télécharge un fichier.</span><span class="sxs-lookup"><span data-stu-id="5a425-194">Downloads a file.</span></span> |
|`help` | <span data-ttu-id="5a425-195">Fournit des informations d’aide pour les commandes de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="5a425-195">Provides help information for live response commands.</span></span> |
|`jobs` | <span data-ttu-id="5a425-196">Indique les travaux en cours d’exécution, leur ID et leur état.</span><span class="sxs-lookup"><span data-stu-id="5a425-196">Shows currently running jobs, their ID and status.</span></span> |
|`persistence` | <span data-ttu-id="5a425-197">Affiche toutes les méthodes de persistance connues sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-197">Shows all known persistence methods on the device.</span></span> |
|`processes` | <span data-ttu-id="5a425-198">Affiche tous les processus en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-198">Shows all processes running on the device.</span></span> |
|`registry` | <span data-ttu-id="5a425-199">Affiche les valeurs du Registre.</span><span class="sxs-lookup"><span data-stu-id="5a425-199">Shows registry values.</span></span> |
|`scheduledtasks` | <span data-ttu-id="5a425-200">Affiche toutes les tâches programmées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-200">Shows all scheduled tasks on the device.</span></span> |
|`services` | <span data-ttu-id="5a425-201">Affiche tous les services sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-201">Shows all services on the device.</span></span> |
|`trace` | <span data-ttu-id="5a425-202">Définit le mode de journalisation du terminal pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="5a425-202">Sets the terminal's logging mode to debug.</span></span> |

### <a name="advanced-commands"></a><span data-ttu-id="5a425-203">Commandes avancées</span><span class="sxs-lookup"><span data-stu-id="5a425-203">Advanced commands</span></span>
<span data-ttu-id="5a425-204">Les commandes suivantes sont disponibles pour les rôles d’utilisateur qui ont la possibilité d’exécuter des **commandes** de réponse en direct avancées.</span><span class="sxs-lookup"><span data-stu-id="5a425-204">The following commands are available for user roles that are granted the ability to run **advanced** live response commands.</span></span> <span data-ttu-id="5a425-205">Pour plus d’informations sur les attributions de rôles, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-205">For more information on role assignments, see [Create and manage roles](user-roles.md).</span></span> 

| <span data-ttu-id="5a425-206">Command</span><span class="sxs-lookup"><span data-stu-id="5a425-206">Command</span></span> | <span data-ttu-id="5a425-207">Description</span><span class="sxs-lookup"><span data-stu-id="5a425-207">Description</span></span> |
|---|---|
| `analyze` | <span data-ttu-id="5a425-208">Analyse l’entité avec différents moteurs d’incrimination pour parvenir à un verdict.</span><span class="sxs-lookup"><span data-stu-id="5a425-208">Analyses the entity with various incrimination engines to reach a verdict.</span></span> |
| `run` | <span data-ttu-id="5a425-209">Exécute un script PowerShell à partir de la bibliothèque sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-209">Runs a PowerShell script from the library on the device.</span></span> |
| `library` | <span data-ttu-id="5a425-210">Répertorie les fichiers qui ont été chargés dans la bibliothèque de réponses en direct.</span><span class="sxs-lookup"><span data-stu-id="5a425-210">Lists files that were uploaded to the live response library.</span></span> |
| `putfile` | <span data-ttu-id="5a425-211">Place un fichier de la bibliothèque sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-211">Puts a file from the library to the device.</span></span> <span data-ttu-id="5a425-212">Les fichiers sont enregistrés dans un dossier de travail et supprimés lorsque l’appareil redémarre par défaut.</span><span class="sxs-lookup"><span data-stu-id="5a425-212">Files are saved in a working folder and are deleted when the device restarts by default.</span></span> |
| `remediate` | <span data-ttu-id="5a425-213">Remédie à une entité sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a425-213">Remediates an entity on the device.</span></span> <span data-ttu-id="5a425-214">L’action de correction varie en fonction du type d’entité :</span><span class="sxs-lookup"><span data-stu-id="5a425-214">The remediation action will vary depending on the entity type:</span></span><br><span data-ttu-id="5a425-215">- Fichier : supprimer</span><span class="sxs-lookup"><span data-stu-id="5a425-215">- File: delete</span></span><br><span data-ttu-id="5a425-216">- Processus : arrêter, supprimer un fichier image</span><span class="sxs-lookup"><span data-stu-id="5a425-216">- Process: stop, delete image file</span></span><br><span data-ttu-id="5a425-217">- Service : arrêter, supprimer un fichier image</span><span class="sxs-lookup"><span data-stu-id="5a425-217">- Service: stop, delete image file</span></span><br><span data-ttu-id="5a425-218">- Entrée de Registre : supprimer</span><span class="sxs-lookup"><span data-stu-id="5a425-218">- Registry entry: delete</span></span><br><span data-ttu-id="5a425-219">- Tâche programmée : supprimer</span><span class="sxs-lookup"><span data-stu-id="5a425-219">- Scheduled task: remove</span></span><br><span data-ttu-id="5a425-220">- Élément de dossier de démarrage : supprimer un fichier</span><span class="sxs-lookup"><span data-stu-id="5a425-220">- Startup folder item: delete file</span></span> <br> <span data-ttu-id="5a425-221">REMARQUE : cette commande est une commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="5a425-221">NOTE: This command has a prerequisite command.</span></span> <span data-ttu-id="5a425-222">Vous pouvez utiliser la `-auto` commande conjointement pour `remediate` exécuter automatiquement la commande prérequise.</span><span class="sxs-lookup"><span data-stu-id="5a425-222">You can use the `-auto` command in conjunction with `remediate` to automatically run the prerequisite command.</span></span> 
|`undo` | <span data-ttu-id="5a425-223">Restaure une entité qui a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="5a425-223">Restores an entity that was remediated.</span></span> |


## <a name="use-live-response-commands"></a><span data-ttu-id="5a425-224">Utiliser des commandes de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="5a425-224">Use live response commands</span></span>

<span data-ttu-id="5a425-225">Les commandes que vous pouvez utiliser dans la console suivent les mêmes principes que [les commandes Windows.](/windows-server/administration/windows-commands/windows-commands#BKMK_c)</span><span class="sxs-lookup"><span data-stu-id="5a425-225">The commands that you can use in the console follow similar principles as [Windows Commands](/windows-server/administration/windows-commands/windows-commands#BKMK_c).</span></span>

<span data-ttu-id="5a425-226">Les commandes avancées offrent un ensemble plus robuste d’actions qui vous permettent d’exécuter des actions plus puissantes telles que télécharger et télécharger un fichier, exécuter des scripts sur l’appareil et prendre des mesures correctives sur une entité.</span><span class="sxs-lookup"><span data-stu-id="5a425-226">The advanced commands offer a more robust set of actions that allow you to take more powerful actions such as download and upload a file, run scripts on the device, and take remediation actions on an entity.</span></span>

### <a name="get-a-file-from-the-device"></a><span data-ttu-id="5a425-227">Obtenir un fichier à partir de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5a425-227">Get a file from the device</span></span>

<span data-ttu-id="5a425-228">Pour les scénarios où vous souhaitez obtenir un fichier à partir d’un appareil que vous examinez, vous pouvez utiliser la `getfile` commande.</span><span class="sxs-lookup"><span data-stu-id="5a425-228">For scenarios when you'd like get a file from a device you're investigating, you can use the `getfile` command.</span></span> <span data-ttu-id="5a425-229">Cela vous permet d’enregistrer le fichier à partir de l’appareil pour une investigation plus approfondie.</span><span class="sxs-lookup"><span data-stu-id="5a425-229">This allows you to save the file from the device for further investigation.</span></span>

>[!NOTE]
><span data-ttu-id="5a425-230">Les limites de taille de fichier suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="5a425-230">The following file size limits apply:</span></span>
>- <span data-ttu-id="5a425-231">`getfile` limite : 3 Go</span><span class="sxs-lookup"><span data-stu-id="5a425-231">`getfile` limit: 3 GB</span></span>
>- <span data-ttu-id="5a425-232">`fileinfo` limite : 10 Go</span><span class="sxs-lookup"><span data-stu-id="5a425-232">`fileinfo` limit: 10 GB</span></span>
>- <span data-ttu-id="5a425-233">`library` limite : 250 Mo</span><span class="sxs-lookup"><span data-stu-id="5a425-233">`library` limit: 250 MB</span></span>

### <a name="download-a-file-in-the-background"></a><span data-ttu-id="5a425-234">Télécharger un fichier en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="5a425-234">Download a file in the background</span></span>

<span data-ttu-id="5a425-235">Pour permettre à votre équipe des opérations de sécurité de continuer à examiner un appareil touché, les fichiers peuvent désormais être téléchargés en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5a425-235">To enable your security operations team to continue investigating an impacted device, files can now be downloaded in the background.</span></span>

- <span data-ttu-id="5a425-236">Pour télécharger un fichier en arrière-plan, dans la console de commande de réponse en direct, tapez `download <file_path> &` .</span><span class="sxs-lookup"><span data-stu-id="5a425-236">To download a file in the background, in the live response command console, type `download <file_path> &`.</span></span>
- <span data-ttu-id="5a425-237">Si vous attendez le téléchargement d’un fichier, vous pouvez le déplacer vers l’arrière-plan à l’aide de Ctrl + Z.</span><span class="sxs-lookup"><span data-stu-id="5a425-237">If you are waiting for a file to be downloaded, you can move it to the background by using Ctrl + Z.</span></span>
- <span data-ttu-id="5a425-238">Pour mettre un téléchargement de fichier au premier plan, dans la console de commande de réponse en direct, tapez `fg <command_id>` .</span><span class="sxs-lookup"><span data-stu-id="5a425-238">To bring a file download to the foreground, in the live response command console, type `fg <command_id>`.</span></span>

<span data-ttu-id="5a425-239">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="5a425-239">Here are some examples:</span></span>


|<span data-ttu-id="5a425-240">Commande</span><span class="sxs-lookup"><span data-stu-id="5a425-240">Command</span></span>  |<span data-ttu-id="5a425-241">Comportement</span><span class="sxs-lookup"><span data-stu-id="5a425-241">What it does</span></span>  |
|---------|---------|
|`getfile "C:\windows\some_file.exe" &`     |<span data-ttu-id="5a425-242">Commence à télécharger un fichier nommé *some_file.exe* en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5a425-242">Starts downloading a file named *some_file.exe* in the background.</span></span>         |
|`fg 1234`     |<span data-ttu-id="5a425-243">Renvoie un téléchargement avec l’ID de commande *1234* au premier plan.</span><span class="sxs-lookup"><span data-stu-id="5a425-243">Returns a download with command ID *1234* to the foreground.</span></span>         |


### <a name="put-a-file-in-the-library"></a><span data-ttu-id="5a425-244">Placer un fichier dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a425-244">Put a file in the library</span></span>

<span data-ttu-id="5a425-245">La réponse en direct dispose d’une bibliothèque dans laquelle vous pouvez placer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="5a425-245">Live response has a library where you can put files into.</span></span> <span data-ttu-id="5a425-246">La bibliothèque stocke les fichiers (tels que les scripts) qui peuvent être exécutés dans une session de réponse en direct au niveau du client.</span><span class="sxs-lookup"><span data-stu-id="5a425-246">The library stores files (such as scripts) that can be run in a live response session at the tenant level.</span></span>

<span data-ttu-id="5a425-247">La réponse en direct permet aux scripts PowerShell de s’exécuter, mais vous devez d’abord placer les fichiers dans la bibliothèque avant de pouvoir les exécuter.</span><span class="sxs-lookup"><span data-stu-id="5a425-247">Live response allows PowerShell scripts to run, however you must first put the files into the library before you can run them.</span></span> 

<span data-ttu-id="5a425-248">Vous pouvez avoir une collection de scripts PowerShell qui peuvent s’exécuter sur les appareils avec qui vous lancez des sessions de réponse en direct.</span><span class="sxs-lookup"><span data-stu-id="5a425-248">You can have a collection of PowerShell scripts that can run on devices that you initiate live response sessions with.</span></span> 

#### <a name="to-upload-a-file-in-the-library"></a><span data-ttu-id="5a425-249">Pour télécharger un fichier dans la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a425-249">To upload a file in the library</span></span>

1. <span data-ttu-id="5a425-250">Cliquez **Télécharger fichier vers la bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="5a425-250">Click **Upload file to library**.</span></span> 

2. <span data-ttu-id="5a425-251">Cliquez **sur Parcourir** et sélectionnez le fichier.</span><span class="sxs-lookup"><span data-stu-id="5a425-251">Click **Browse** and select the file.</span></span>

3. <span data-ttu-id="5a425-252">Fournissez une brève description.</span><span class="sxs-lookup"><span data-stu-id="5a425-252">Provide a brief description.</span></span>

4. <span data-ttu-id="5a425-253">Spécifiez si vous souhaitez réécrire un fichier du même nom.</span><span class="sxs-lookup"><span data-stu-id="5a425-253">Specify if you'd like to overwrite a file with the same name.</span></span>

5. <span data-ttu-id="5a425-254">Si vous le souhaitez, connaissez les paramètres nécessaires pour le script, cochez la case des paramètres de script.</span><span class="sxs-lookup"><span data-stu-id="5a425-254">If you'd like to be,  know what parameters are needed for the script, select the script parameters check box.</span></span> <span data-ttu-id="5a425-255">Dans le champ de texte, entrez un exemple et une description.</span><span class="sxs-lookup"><span data-stu-id="5a425-255">In the text field, enter an example and a description.</span></span>

6. <span data-ttu-id="5a425-256">Cliquez sur **Confirmer.**</span><span class="sxs-lookup"><span data-stu-id="5a425-256">Click **Confirm**.</span></span> 

7. <span data-ttu-id="5a425-257">(Facultatif) Pour vérifier que le fichier a été chargé dans la bibliothèque, exécutez la `library` commande.</span><span class="sxs-lookup"><span data-stu-id="5a425-257">(Optional) To verify that the file was uploaded to the library, run the `library` command.</span></span>


### <a name="cancel-a-command"></a><span data-ttu-id="5a425-258">Annuler une commande</span><span class="sxs-lookup"><span data-stu-id="5a425-258">Cancel a command</span></span>
<span data-ttu-id="5a425-259">À tout moment pendant une session, vous pouvez annuler une commande en appuyant sur Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="5a425-259">Anytime during a session, you can cancel a command by pressing CTRL + C.</span></span>  

>[!WARNING]
><span data-ttu-id="5a425-260">L’utilisation de ce raccourci n’arrête pas la commande côté agent.</span><span class="sxs-lookup"><span data-stu-id="5a425-260">Using this shortcut will not stop the command in the agent side.</span></span> <span data-ttu-id="5a425-261">Il annule uniquement la commande dans le portail.</span><span class="sxs-lookup"><span data-stu-id="5a425-261">It will only cancel the command in the portal.</span></span> <span data-ttu-id="5a425-262">Ainsi, la modification des opérations telles que la « correction » peut se poursuivre, pendant l’annulation de la commande.</span><span class="sxs-lookup"><span data-stu-id="5a425-262">So, changing operations such as "remediate" may continue, while the command is canceled.</span></span> 

## <a name="run-a-powershell-script"></a><span data-ttu-id="5a425-263">Exécuter un script PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a425-263">Run a PowerShell script</span></span> 

<span data-ttu-id="5a425-264">Avant de pouvoir exécuter un script PowerShell, vous devez d’abord le télécharger dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="5a425-264">Before you can run a PowerShell script, you must first upload it to the library.</span></span> 

<span data-ttu-id="5a425-265">Après avoir téléchargé le script dans la bibliothèque, utilisez `run` la commande pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="5a425-265">After uploading the script to the library, use the `run` command to run the script.</span></span>

<span data-ttu-id="5a425-266">Si vous envisagez d’utiliser un script non signé dans la session, vous devez activer le paramètre dans la page Paramètres des [fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="5a425-266">If you plan to use an unsigned script in the session, you'll need to enable the setting in the [Advanced features settings](advanced-features.md) page.</span></span>

>[!WARNING]
><span data-ttu-id="5a425-267">Autoriser l’utilisation de scripts non signés peut augmenter votre exposition aux menaces.</span><span class="sxs-lookup"><span data-stu-id="5a425-267">Allowing the use of unsigned scripts may increase your exposure to threats.</span></span>

## <a name="apply-command-parameters"></a><span data-ttu-id="5a425-268">Appliquer des paramètres de commande</span><span class="sxs-lookup"><span data-stu-id="5a425-268">Apply command parameters</span></span>

- <span data-ttu-id="5a425-269">Consultez l’aide de la console pour en savoir plus sur les paramètres de commande.</span><span class="sxs-lookup"><span data-stu-id="5a425-269">View the console help to learn about command parameters.</span></span> <span data-ttu-id="5a425-270">Pour en savoir plus sur une commande individuelle, exécutez :</span><span class="sxs-lookup"><span data-stu-id="5a425-270">To learn about an individual command, run:</span></span>
 
    `help <command name>`

- <span data-ttu-id="5a425-271">Lorsque vous appliquez des paramètres aux commandes, notez que les paramètres sont gérés selon un ordre fixe :</span><span class="sxs-lookup"><span data-stu-id="5a425-271">When applying parameters to commands, note that parameters are handled based on a fixed order:</span></span>
 
    `<command name> param1 param2` 

- <span data-ttu-id="5a425-272">Lorsque vous spécifiez des paramètres en dehors de l’ordre fixe, spécifiez le nom du paramètre avec un tiret avant de fournir la valeur :</span><span class="sxs-lookup"><span data-stu-id="5a425-272">When specifying parameters outside of the fixed order, specify the name of the parameter with a hyphen before providing the value:</span></span>
 
    `<command name> -param2_name param2`

- <span data-ttu-id="5a425-273">Lorsque vous utilisez des commandes qui ont des commandes prérequises, vous pouvez utiliser des indicateurs :</span><span class="sxs-lookup"><span data-stu-id="5a425-273">When using commands that have prerequisite commands, you can use flags:</span></span>

    <span data-ttu-id="5a425-274">`<command name> -type file -id <file path> - auto` ou `remediate file <file path> - auto`.</span><span class="sxs-lookup"><span data-stu-id="5a425-274">`<command name> -type file -id <file path> - auto` or `remediate file <file path> - auto`.</span></span>

## <a name="supported-output-types"></a><span data-ttu-id="5a425-275">Types de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a425-275">Supported output types</span></span>

<span data-ttu-id="5a425-276">La réponse en direct prend en charge les types de sortie de tableau et de format JSON.</span><span class="sxs-lookup"><span data-stu-id="5a425-276">Live response supports table and JSON format output types.</span></span> <span data-ttu-id="5a425-277">Pour chaque commande, il existe un comportement de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="5a425-277">For each command, there's a default output behavior.</span></span> <span data-ttu-id="5a425-278">Vous pouvez modifier la sortie dans votre format de sortie préféré à l’aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a425-278">You can modify the output in your preferred output format using the following commands:</span></span>

- `-output json`
- `-output table`

>[!NOTE]
><span data-ttu-id="5a425-279">Moins de champs sont affichés au format tableau en raison de l’espace limité.</span><span class="sxs-lookup"><span data-stu-id="5a425-279">Fewer fields are shown in table format due to the limited space.</span></span> <span data-ttu-id="5a425-280">Pour voir plus de détails dans la sortie, vous pouvez utiliser la commande de sortie JSON afin que d’autres détails soient affichés.</span><span class="sxs-lookup"><span data-stu-id="5a425-280">To see more details in the output, you can use the JSON output command so that more details are shown.</span></span>

## <a name="supported-output-pipes"></a><span data-ttu-id="5a425-281">Canaux de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a425-281">Supported output pipes</span></span>

<span data-ttu-id="5a425-282">La réponse en direct prend en charge le système de sortie vers l’CLI et le fichier.</span><span class="sxs-lookup"><span data-stu-id="5a425-282">Live response supports output piping to CLI and file.</span></span> <span data-ttu-id="5a425-283">L’CLI est le comportement de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="5a425-283">CLI is the default output behavior.</span></span> <span data-ttu-id="5a425-284">Vous pouvez canaliser la sortie vers un fichier à l’aide de la commande suivante : [command] > [filename].txt.</span><span class="sxs-lookup"><span data-stu-id="5a425-284">You can pipe the output to a file using the following command: [command] > [filename].txt.</span></span>  

<span data-ttu-id="5a425-285">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5a425-285">Example:</span></span>

```console
processes > output.txt
```

## <a name="view-the-command-log"></a><span data-ttu-id="5a425-286">Afficher le journal de commandes</span><span class="sxs-lookup"><span data-stu-id="5a425-286">View the command log</span></span>

<span data-ttu-id="5a425-287">Sélectionnez **l’onglet Journal** de commandes pour voir les commandes utilisées sur l’appareil au cours d’une session.</span><span class="sxs-lookup"><span data-stu-id="5a425-287">Select the **Command log** tab to see the commands used on the device during a session.</span></span> <span data-ttu-id="5a425-288">Chaque commande est suivi avec des détails complets tels que :</span><span class="sxs-lookup"><span data-stu-id="5a425-288">Each command is tracked with full details such as:</span></span>
- <span data-ttu-id="5a425-289">ID</span><span class="sxs-lookup"><span data-stu-id="5a425-289">ID</span></span>
- <span data-ttu-id="5a425-290">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="5a425-290">Command line</span></span>
- <span data-ttu-id="5a425-291">Durée</span><span class="sxs-lookup"><span data-stu-id="5a425-291">Duration</span></span>
- <span data-ttu-id="5a425-292">Barre côté état et entrée ou sortie</span><span class="sxs-lookup"><span data-stu-id="5a425-292">Status and input or output side bar</span></span>

## <a name="limitations"></a><span data-ttu-id="5a425-293">Limites</span><span class="sxs-lookup"><span data-stu-id="5a425-293">Limitations</span></span>

- <span data-ttu-id="5a425-294">Les sessions de réponse en direct sont limitées à 25 sessions de réponse en direct à la fois.</span><span class="sxs-lookup"><span data-stu-id="5a425-294">Live response sessions are limited to 25 live response sessions at a time.</span></span>
- <span data-ttu-id="5a425-295">Le délai d’inactivité de la session de réponse en direct est de 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="5a425-295">Live response session inactive timeout value is 30 minutes.</span></span> 
- <span data-ttu-id="5a425-296">Un utilisateur peut démarrer jusqu’à 10 sessions simultanées.</span><span class="sxs-lookup"><span data-stu-id="5a425-296">A user can initiate up to 10 concurrent sessions.</span></span>
- <span data-ttu-id="5a425-297">Un appareil ne peut être connecté qu’à une seule session à la fois.</span><span class="sxs-lookup"><span data-stu-id="5a425-297">A device can only be in one session at a time.</span></span>
- <span data-ttu-id="5a425-298">Les limites de taille de fichier suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="5a425-298">The following file size limits apply:</span></span>
   - <span data-ttu-id="5a425-299">`getfile` limite : 3 Go</span><span class="sxs-lookup"><span data-stu-id="5a425-299">`getfile` limit: 3 GB</span></span>
   - <span data-ttu-id="5a425-300">`fileinfo` limite : 10 Go</span><span class="sxs-lookup"><span data-stu-id="5a425-300">`fileinfo` limit: 10 GB</span></span>
   - <span data-ttu-id="5a425-301">`library` limite : 250 Mo</span><span class="sxs-lookup"><span data-stu-id="5a425-301">`library` limit: 250 MB</span></span>

## <a name="related-article"></a><span data-ttu-id="5a425-302">Article connexe</span><span class="sxs-lookup"><span data-stu-id="5a425-302">Related article</span></span>
- [<span data-ttu-id="5a425-303">Exemples de commande Live response</span><span class="sxs-lookup"><span data-stu-id="5a425-303">Live response command examples</span></span>](live-response-command-examples.md)
