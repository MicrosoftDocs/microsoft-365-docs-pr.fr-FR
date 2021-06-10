---
title: Prendre des actions de réponse sur un fichier dans Microsoft Defender pour le point de terminaison
description: Prenez des mesures de réponse sur les alertes liées aux fichiers en arrêtant et en mettre en quarantaine un fichier ou en bloquant un fichier et en vérifiant les détails de l’activité.
keywords: répondre, arrêter et mettre en quarantaine, bloquer un fichier, analyse approfondie
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
ms.openlocfilehash: 1f189956d65e6d08d8e00272ba0d8db3ba59f6d4
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844069"
---
# <a name="take-response-actions-on-a-file"></a><span data-ttu-id="b9041-104">Prendre des mesures de réponse sur un fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-104">Take response actions on a file</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b9041-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b9041-105">**Applies to:**</span></span>
- [<span data-ttu-id="b9041-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b9041-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

[!include[Prerelease information](../../includes/prerelease.md)]

> <span data-ttu-id="b9041-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b9041-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="b9041-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b9041-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-responddile-abovefoldlink)

<span data-ttu-id="b9041-109">Répondez rapidement aux attaques détectées en arrêtant et en bloquant des fichiers ou en bloquant un fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-109">Quickly respond to detected attacks by stopping and quarantining files or blocking a file.</span></span> <span data-ttu-id="b9041-110">Après avoir pris des mesures sur les fichiers, vous pouvez vérifier les détails de l’activité dans le centre de l’action.</span><span class="sxs-lookup"><span data-stu-id="b9041-110">After taking action on files, you can check activity details in the Action center.</span></span>

<span data-ttu-id="b9041-111">Les actions de réponse sont disponibles sur la page de profil détaillée d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-111">Response actions are available on a file's detailed profile page.</span></span> <span data-ttu-id="b9041-112">Une fois sur cette page, vous pouvez basculer entre la nouvelle et l’ancienne mise en page en faisant basculer la **nouvelle page de fichier.**</span><span class="sxs-lookup"><span data-stu-id="b9041-112">Once on this page, you can switch between the new and old page layouts by toggling **new File page**.</span></span> <span data-ttu-id="b9041-113">Le reste de cet article décrit la mise en page la plus nouvelle.</span><span class="sxs-lookup"><span data-stu-id="b9041-113">The rest of this article describes the newer page layout.</span></span>

<span data-ttu-id="b9041-114">Les actions de réponse s’exécutent le long de la partie supérieure de la page de fichiers et incluent :</span><span class="sxs-lookup"><span data-stu-id="b9041-114">Response actions run along the top of the file page, and include:</span></span>

- <span data-ttu-id="b9041-115">Arrêter et mettre en quarantaine le fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-115">Stop and Quarantine File</span></span>
- <span data-ttu-id="b9041-116">Ajouter un indicateur</span><span class="sxs-lookup"><span data-stu-id="b9041-116">Add Indicator</span></span>
- <span data-ttu-id="b9041-117">Télécharger un fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-117">Download file</span></span>
- <span data-ttu-id="b9041-118">Consulter un spécialiste des menaces</span><span class="sxs-lookup"><span data-stu-id="b9041-118">Consult a threat expert</span></span>
- <span data-ttu-id="b9041-119">Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="b9041-119">Action center</span></span>

<span data-ttu-id="b9041-120">Vous pouvez également soumettre des fichiers pour analyse approfondie, afin d’exécuter le fichier dans un bac à sable (sandbox) cloud sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b9041-120">You can also submit files for deep analysis, to run the file in a secure cloud sandbox.</span></span> <span data-ttu-id="b9041-121">Une fois l’analyse terminée, vous obtenez un rapport détaillé qui fournit des informations sur le comportement du fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-121">When the analysis is complete, you'll get a detailed report that provides information about the behavior of the file.</span></span> <span data-ttu-id="b9041-122">Vous pouvez soumettre des fichiers pour analyse approfondie et lire les rapports passés en sélectionnant **l’onglet Analyse** approfondie. Il se trouve sous les cartes d’informations de fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-122">You can submit files for deep analysis and read past reports by selecting the **Deep analysis** tab. It's located below the file information cards.</span></span>

<span data-ttu-id="b9041-123">Certaines actions nécessitent certaines autorisations.</span><span class="sxs-lookup"><span data-stu-id="b9041-123">Some actions require certain permissions.</span></span> <span data-ttu-id="b9041-124">Le tableau suivant décrit l’action que certaines autorisations peuvent prendre sur les fichiers exécutables portables (PE) et non PE :</span><span class="sxs-lookup"><span data-stu-id="b9041-124">The following table describes what action certain permissions can take on portable executable (PE) and non-PE files:</span></span>

| <span data-ttu-id="b9041-125">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b9041-125">Permission</span></span>             | <span data-ttu-id="b9041-126">Fichiers PE</span><span class="sxs-lookup"><span data-stu-id="b9041-126">PE files</span></span> | <span data-ttu-id="b9041-127">Fichiers non PE</span><span class="sxs-lookup"><span data-stu-id="b9041-127">Non-PE files</span></span> |
| :--------------------- | :------: | :----------: |
| <span data-ttu-id="b9041-128">Afficher les données</span><span class="sxs-lookup"><span data-stu-id="b9041-128">View data</span></span>              |     <span data-ttu-id="b9041-129">X</span><span class="sxs-lookup"><span data-stu-id="b9041-129">X</span></span>    |       <span data-ttu-id="b9041-130">X</span><span class="sxs-lookup"><span data-stu-id="b9041-130">X</span></span>      |
| <span data-ttu-id="b9041-131">Examen des alertes</span><span class="sxs-lookup"><span data-stu-id="b9041-131">Alerts investigation</span></span>   | <span data-ttu-id="b9041-132">&#x2611;</span><span class="sxs-lookup"><span data-stu-id="b9041-132">&#x2611;</span></span> |       <span data-ttu-id="b9041-133">X</span><span class="sxs-lookup"><span data-stu-id="b9041-133">X</span></span>      |
| <span data-ttu-id="b9041-134">Base de la réponse en direct</span><span class="sxs-lookup"><span data-stu-id="b9041-134">Live response basic</span></span>    |     <span data-ttu-id="b9041-135">X</span><span class="sxs-lookup"><span data-stu-id="b9041-135">X</span></span>    |       <span data-ttu-id="b9041-136">X</span><span class="sxs-lookup"><span data-stu-id="b9041-136">X</span></span>      |
| <span data-ttu-id="b9041-137">Réponse en direct avancée</span><span class="sxs-lookup"><span data-stu-id="b9041-137">Live response advanced</span></span> | <span data-ttu-id="b9041-138">&#x2611;</span><span class="sxs-lookup"><span data-stu-id="b9041-138">&#x2611;</span></span> |   <span data-ttu-id="b9041-139">&#x2611;</span><span class="sxs-lookup"><span data-stu-id="b9041-139">&#x2611;</span></span>   |

<span data-ttu-id="b9041-140">Pour plus d’informations sur les rôles, voir Créer et gérer des rôles pour le contrôle [d’accès basé sur les rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="b9041-140">For more information on roles, see [Create and manage roles for role-based access control](user-roles.md).</span></span>

## <a name="stop-and-quarantine-files-in-your-network"></a><span data-ttu-id="b9041-141">Arrêter et mettre en quarantaine des fichiers de votre réseau</span><span class="sxs-lookup"><span data-stu-id="b9041-141">Stop and quarantine files in your network</span></span>

<span data-ttu-id="b9041-142">Vous pouvez contenir une attaque dans votre organisation en arrêtant le processus malveillant et en mettre en quarantaine le fichier là où il a été observé.</span><span class="sxs-lookup"><span data-stu-id="b9041-142">You can contain an attack in your organization by stopping the malicious process and quarantining the file where it was observed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9041-143">Vous pouvez uniquement prendre cette action si :</span><span class="sxs-lookup"><span data-stu-id="b9041-143">You can only take this action if:</span></span>
>
> - <span data-ttu-id="b9041-144">L’appareil sur qui vous exécutez l’action Windows 10, version 1703 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b9041-144">The device you're taking the action on is running Windows 10, version 1703 or later</span></span>
> - <span data-ttu-id="b9041-145">Le fichier n’appartient pas aux éditeurs tiers de confiance ou n’est pas signé par Microsoft</span><span class="sxs-lookup"><span data-stu-id="b9041-145">The file does not belong to trusted third-party publishers or not signed by Microsoft</span></span>
> - <span data-ttu-id="b9041-146">Antivirus Microsoft Defender doit au moins être en cours d’exécution en mode passif.</span><span class="sxs-lookup"><span data-stu-id="b9041-146">Microsoft Defender Antivirus must at least be running on Passive mode.</span></span> <span data-ttu-id="b9041-147">Pour plus d’informations, [voir Antivirus Microsoft Defender compatibilité.](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility)</span><span class="sxs-lookup"><span data-stu-id="b9041-147">For more information, see [Microsoft Defender Antivirus compatibility](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility).</span></span>

<span data-ttu-id="b9041-148">L’action Arrêter **et mettre en** quarantaine le fichier inclut l’arrêt des processus en cours d’exécution, la mise en quarantaine des fichiers et la suppression de données persistantes telles que les clés de Registre.</span><span class="sxs-lookup"><span data-stu-id="b9041-148">The **Stop and Quarantine File** action includes stopping running processes, quarantining the files, and deleting persistent data such as registry keys.</span></span>

<span data-ttu-id="b9041-149">Cette action prend effet sur les appareils Windows 10, version 1703 ou ultérieure, où le fichier a été observé au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="b9041-149">This action takes effect on devices with Windows 10, version 1703 or later, where the file was observed in the last 30 days.</span></span>

> [!NOTE]
> <span data-ttu-id="b9041-150">Vous pourrez restaurer le fichier de quarantaine à tout moment.</span><span class="sxs-lookup"><span data-stu-id="b9041-150">You’ll be able to restore the file from quarantine at any time.</span></span>

### <a name="stop-and-quarantine-files"></a><span data-ttu-id="b9041-151">Arrêter et mettre en quarantaine des fichiers</span><span class="sxs-lookup"><span data-stu-id="b9041-151">Stop and quarantine files</span></span>

1. <span data-ttu-id="b9041-152">Sélectionnez le fichier que vous souhaitez arrêter et mettre en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b9041-152">Select the file you want to stop and quarantine.</span></span> <span data-ttu-id="b9041-153">Vous pouvez sélectionner un fichier dans l’un des affichages suivants ou utiliser la zone de recherche :</span><span class="sxs-lookup"><span data-stu-id="b9041-153">You can select a file from any of the following views or use the Search box:</span></span>

   - <span data-ttu-id="b9041-154">**Alertes :** cliquez sur les liens correspondants dans la description ou les détails de la chronologie de l’artefact</span><span class="sxs-lookup"><span data-stu-id="b9041-154">**Alerts** - click the corresponding links from the Description or Details in the Artifact timeline</span></span>
   - <span data-ttu-id="b9041-155">**Zone de recherche** : **sélectionnez Fichier** dans le menu déroulant et entrez le nom du fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-155">**Search box** - select **File** from the drop–down menu and enter the file name</span></span>

   > [!NOTE]
   > <span data-ttu-id="b9041-156">L’action d’arrêt et de mise en quarantaine du fichier est limitée à un maximum de 1 000 appareils.</span><span class="sxs-lookup"><span data-stu-id="b9041-156">The stop and quarantine file action is limited to a maximum of 1000 devices.</span></span> <span data-ttu-id="b9041-157">Pour arrêter un fichier sur un plus grand nombre d’appareils, voir [Ajouter un indicateur pour bloquer ou autoriser un fichier.](#add-indicator-to-block-or-allow-a-file)</span><span class="sxs-lookup"><span data-stu-id="b9041-157">To stop a file on a larger number of devices, see [Add indicator to block or allow file](#add-indicator-to-block-or-allow-a-file).</span></span>

2. <span data-ttu-id="b9041-158">Go to the top bar and select **Stop and Quarantine File**.</span><span class="sxs-lookup"><span data-stu-id="b9041-158">Go to the top bar and select **Stop and Quarantine File**.</span></span>

   ![Image de l’action d’arrêt et de mise en quarantaine du fichier](images/atp-stop-quarantine-file.png)

3. <span data-ttu-id="b9041-160">Spécifiez une raison, puis sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="b9041-160">Specify a reason, then select **Confirm**.</span></span>

   ![Image de la fenêtre modale de fichier d’arrêt et de mise en quarantaine](images/atp-stop-quarantine.png)

   <span data-ttu-id="b9041-162">Le centre de données affiche les informations de soumission :</span><span class="sxs-lookup"><span data-stu-id="b9041-162">The Action center shows the submission information:</span></span>
   
   ![Image du centre de mise en quarantaine et d’arrêt des fichiers](images/atp-stopnquarantine-file.png)

   - <span data-ttu-id="b9041-164">**Heure de soumission** : indique quand l’action a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="b9041-164">**Submission time** - Shows when the action was submitted.</span></span>
   - <span data-ttu-id="b9041-165">**Réussite** : indique le nombre d’appareils sur lequel le fichier a été arrêté et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b9041-165">**Success** - Shows the number of devices where the file has been stopped and quarantined.</span></span>
   - <span data-ttu-id="b9041-166">**Échec :** indique le nombre d’appareils sur lequel l’action a échoué et des détails sur l’échec.</span><span class="sxs-lookup"><span data-stu-id="b9041-166">**Failed** - Shows the number of devices where the action failed and details about the failure.</span></span>
   - <span data-ttu-id="b9041-167">**En attente** : indique le nombre d’appareils dont le fichier n’a pas encore été arrêté et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b9041-167">**Pending** - Shows the number of devices where the file is yet to be stopped and quarantined from.</span></span> <span data-ttu-id="b9041-168">Cela peut prendre du temps lorsque l’appareil est hors connexion ou n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="b9041-168">This can take time for cases when the device is offline or not connected to the network.</span></span>

4. <span data-ttu-id="b9041-169">Sélectionnez l’un des indicateurs d’état pour afficher plus d’informations sur l’action.</span><span class="sxs-lookup"><span data-stu-id="b9041-169">Select any of the status indicators to view more information about the action.</span></span> <span data-ttu-id="b9041-170">Par exemple, **sélectionnez Échec pour** voir où l’action a échoué.</span><span class="sxs-lookup"><span data-stu-id="b9041-170">For example, select **Failed** to see where the action failed.</span></span>

<span data-ttu-id="b9041-171">**Notification sur l’utilisateur de l’appareil**:</span><span class="sxs-lookup"><span data-stu-id="b9041-171">**Notification on device user**:</span></span></br>
<span data-ttu-id="b9041-172">Lorsque le fichier est supprimé d’un appareil, la notification suivante s’affiche :</span><span class="sxs-lookup"><span data-stu-id="b9041-172">When the file is being removed from a device, the following notification is shown:</span></span>

![Image de notification sur l’utilisateur de l’appareil](images/atp-notification-file.png)

<span data-ttu-id="b9041-174">Dans la chronologie de l’appareil, un nouvel événement est ajouté pour chaque appareil où un fichier a été arrêté et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b9041-174">In the device timeline, a new event is added for each device where a file was stopped and quarantined.</span></span>

<span data-ttu-id="b9041-175">Un avertissement s’affiche avant l’implémentation de l’action pour les fichiers largement utilisés dans l’ensemble d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="b9041-175">A warning is shown before the action is implemented for files widely used throughout an organization.</span></span> <span data-ttu-id="b9041-176">Il s’agit de vérifier que l’opération est prévue.</span><span class="sxs-lookup"><span data-stu-id="b9041-176">It's to validate that the operation is intended.</span></span>

## <a name="restore-file-from-quarantine"></a><span data-ttu-id="b9041-177">Restaurer un fichier à partir de la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="b9041-177">Restore file from quarantine</span></span>

<span data-ttu-id="b9041-178">Vous pouvez revenir en quarantaine et supprimer un fichier si vous avez déterminé qu’il est propre après un examen.</span><span class="sxs-lookup"><span data-stu-id="b9041-178">You can roll back and remove a file from quarantine if you’ve determined that it’s clean after an investigation.</span></span> <span data-ttu-id="b9041-179">Exécutez la commande suivante sur chaque appareil sur lequel le fichier a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b9041-179">Run the following command on each device where the file was quarantined.</span></span>

1. <span data-ttu-id="b9041-180">Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="b9041-180">Open an elevated command–line prompt on the device:</span></span>

   1. <span data-ttu-id="b9041-181">Accéder à **Démarrer** et taper _cmd_.</span><span class="sxs-lookup"><span data-stu-id="b9041-181">Go to **Start** and type _cmd_.</span></span>

   1. <span data-ttu-id="b9041-182">Cliquez avec le bouton droit **sur Invite de** commandes et **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="b9041-182">Right–click **Command prompt** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="b9041-183">Entrez la commande suivante, puis appuyez sur **Entrée**:</span><span class="sxs-lookup"><span data-stu-id="b9041-183">Enter the following command, and press **Enter**:</span></span>

   ```powershell
   “%ProgramFiles%\Windows Defender\MpCmdRun.exe” –Restore –Name EUS:Win32/CustomEnterpriseBlock –All
   ```

> [!NOTE]
> <span data-ttu-id="b9041-184">Dans certains scénarios, **threatName** peut apparaître comme : EUS:Win32/CustomEnterpriseBlock!cl.</span><span class="sxs-lookup"><span data-stu-id="b9041-184">In some scenarios, the **ThreatName** may appear as: EUS:Win32/CustomEnterpriseBlock!cl.</span></span>
>
> <span data-ttu-id="b9041-185">Defender for Endpoint restaure tous les fichiers bloqués personnalisés qui ont été mis en quarantaine sur cet appareil au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="b9041-185">Defender for Endpoint will restore all custom blocked files that were quarantined on this device in the last 30 days.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9041-186">Un fichier mis en quarantaine comme menace réseau potentielle peut ne pas être récupérable.</span><span class="sxs-lookup"><span data-stu-id="b9041-186">A file that was quarantined as a potential network threat might not be recoverable.</span></span> <span data-ttu-id="b9041-187">Si un utilisateur tente de restaurer le fichier après sa mise en quarantaine, il se peut que ce fichier ne soit pas accessible.</span><span class="sxs-lookup"><span data-stu-id="b9041-187">If a user attempts to restore the file after quarantine, that file might not be accessible.</span></span> <span data-ttu-id="b9041-188">Cela peut être dû au fait que le système n’a plus d’informations d’identification réseau pour accéder au fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-188">This can be due to the system no longer having network credentials to access the file.</span></span> <span data-ttu-id="b9041-189">En règle générale, cela est le résultat d’une connexion temporaire à un système ou à un dossier partagé et les jetons d’accès ont expiré.</span><span class="sxs-lookup"><span data-stu-id="b9041-189">Typically, this is a result of a temporary log on to a system or shared folder and the access tokens expired.</span></span>

## <a name="download-or-collect-file"></a><span data-ttu-id="b9041-190">Télécharger ou collecter un dossier</span><span class="sxs-lookup"><span data-stu-id="b9041-190">Download or collect file</span></span>

<span data-ttu-id="b9041-191">La sélection **du fichier de téléchargement** dans les actions de réponse vous permet de télécharger une archive locale .zip par mot de passe contenant votre fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-191">Selecting **Download file** from the response actions allows you to download a local, password-protected .zip archive containing your file.</span></span> <span data-ttu-id="b9041-192">Un flyout s’affiche où vous pouvez enregistrer une raison pour télécharger le fichier et définir un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="b9041-192">A flyout will appear where you can record a reason for downloading the file, and set a password.</span></span>

<span data-ttu-id="b9041-193">Par défaut, vous ne pourrez pas télécharger les fichiers en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b9041-193">By default, you will not be able to download files that are in quarantine.</span></span>

![Image de l’action de téléchargement de fichier](images/atp-download-file-action.png)

### <a name="collect-files"></a><span data-ttu-id="b9041-195">Collecter des fichiers</span><span class="sxs-lookup"><span data-stu-id="b9041-195">Collect files</span></span>

<span data-ttu-id="b9041-196">Si un fichier n’est pas déjà stocké par Microsoft Defender pour le point de terminaison, vous ne pouvez pas le télécharger.</span><span class="sxs-lookup"><span data-stu-id="b9041-196">If a file is not already stored by Microsoft Defender for Endpoint, you can't download it.</span></span> <span data-ttu-id="b9041-197">Au lieu de cela, vous verrez un bouton Collecter **le** fichier au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="b9041-197">Instead, you'll see a **Collect file** button in the same location.</span></span> <span data-ttu-id="b9041-198">Si un fichier n’a pas été vu dans l’organisation au cours des 30 derniers **jours,** le fichier de collecte est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b9041-198">If a file hasn't been seen in the organization in the past 30 days, **Collect file** will be disabled.</span></span>
> [!Important]
> <span data-ttu-id="b9041-199">Un fichier mis en quarantaine comme menace réseau potentielle peut ne pas être récupérable.</span><span class="sxs-lookup"><span data-stu-id="b9041-199">A file that was quarantined as a potential network threat might not be recoverable.</span></span> <span data-ttu-id="b9041-200">Si un utilisateur tente de restaurer le fichier après sa mise en quarantaine, il se peut que ce fichier ne soit pas accessible.</span><span class="sxs-lookup"><span data-stu-id="b9041-200">If a user attempts to restore the file after quarantine, that file might not be accessible.</span></span> <span data-ttu-id="b9041-201">Cela peut être dû au fait que le système n’a plus d’informations d’identification réseau pour accéder au fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-201">This can be due to the system no longer having network credentials to access the file.</span></span> <span data-ttu-id="b9041-202">En règle générale, cela est le résultat d’une connexion temporaire à un système ou à un dossier partagé et les jetons d’accès ont expiré.</span><span class="sxs-lookup"><span data-stu-id="b9041-202">Typically, this is a result of a temporary log on to a system or shared folder and the access tokens expired.</span></span>

## <a name="add-indicator-to-block-or-allow-a-file"></a><span data-ttu-id="b9041-203">Ajouter un indicateur pour bloquer ou autoriser un fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-203">Add indicator to block or allow a file</span></span>

<span data-ttu-id="b9041-204">Empêcher toute propagation supplémentaire d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects.</span><span class="sxs-lookup"><span data-stu-id="b9041-204">Prevent further propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span> <span data-ttu-id="b9041-205">Si vous connaissez un fichier exécutable portable (PE) potentiellement malveillant, vous pouvez le bloquer.</span><span class="sxs-lookup"><span data-stu-id="b9041-205">If you know a potentially malicious portable executable (PE) file, you can block it.</span></span> <span data-ttu-id="b9041-206">Cette opération l’empêche d’être lue, écrite ou exécutée sur les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b9041-206">This operation will prevent it from being read, written, or executed on devices in your organization.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="b9041-207">Cette fonctionnalité est disponible si votre organisation utilise Antivirus Microsoft Defender protection cloud est activée.</span><span class="sxs-lookup"><span data-stu-id="b9041-207">This feature is available if your organization uses Microsoft Defender Antivirus and Cloud–delivered protection is enabled.</span></span> <span data-ttu-id="b9041-208">Pour plus d’informations, [voir Manage cloud-delivered protection](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus).</span><span class="sxs-lookup"><span data-stu-id="b9041-208">For more information, see [Manage cloud–delivered protection](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus).</span></span>
>
> - <span data-ttu-id="b9041-209">La version du client anti-programme malveillant doit être 4.18.1901.x ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b9041-209">The Antimalware client version must be 4.18.1901.x or later.</span></span>
> - <span data-ttu-id="b9041-210">Cette fonctionnalité est conçue pour empêcher le téléchargement de programmes malveillants (ou de fichiers potentiellement malveillants) à partir du web.</span><span class="sxs-lookup"><span data-stu-id="b9041-210">This feature is designed to prevent suspected malware (or potentially malicious files) from being downloaded from the web.</span></span> <span data-ttu-id="b9041-211">Il prend actuellement en charge les fichiers exécutables portables(PE), notamment les fichiers _.exe_ et _.dll_ portables.</span><span class="sxs-lookup"><span data-stu-id="b9041-211">It currently supports portable executable (PE) files, including _.exe_ and _.dll_ files.</span></span> <span data-ttu-id="b9041-212">La couverture sera étendue au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="b9041-212">The coverage will be extended over time.</span></span>
> - <span data-ttu-id="b9041-213">Cette action de réponse est disponible pour les appareils Windows 10 version 1703 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b9041-213">This response action is available for devices on Windows 10, version 1703 or later.</span></span>
> - <span data-ttu-id="b9041-214">La fonction autoriser ou bloquer ne peut pas être effectuée sur les fichiers si la classification du fichier existe sur le cache de l’appareil avant l’action autoriser ou bloquer.</span><span class="sxs-lookup"><span data-stu-id="b9041-214">The allow or block function cannot be done on files if the file's classification exists on the device's cache prior to the allow or block action.</span></span>

> [!NOTE]
> <span data-ttu-id="b9041-215">Le fichier PE doit se trouver dans la chronologie de l’appareil pour que vous soyez en mesure d’agir.</span><span class="sxs-lookup"><span data-stu-id="b9041-215">The PE file needs to be in the device timeline for you to be able to take this action.</span></span>
>
> <span data-ttu-id="b9041-216">Il peut y avoir quelques minutes de latence entre le moment où l’action est prise et le fichier réel bloqué.</span><span class="sxs-lookup"><span data-stu-id="b9041-216">There may be a couple of minutes of latency between the time the action is taken and the actual file being blocked.</span></span>

### <a name="enable-the-block-file-feature"></a><span data-ttu-id="b9041-217">Activer la fonctionnalité bloquer le fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-217">Enable the block file feature</span></span>

<span data-ttu-id="b9041-218">Pour commencer à bloquer les fichiers, vous devez d’abord [activer  ](advanced-features.md) la fonctionnalité Bloquer ou autoriser dans Paramètres.</span><span class="sxs-lookup"><span data-stu-id="b9041-218">To start blocking files, you first need to [turn the **Block or allow** feature on](advanced-features.md) in Settings.</span></span>
### <a name="allow-or-block-file"></a><span data-ttu-id="b9041-219">Autoriser ou bloquer un fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-219">Allow or block file</span></span>

<span data-ttu-id="b9041-220">Lorsque vous ajoutez un hachage d’indicateur pour un fichier, vous pouvez choisir de lancer une alerte et de bloquer le fichier chaque fois qu’un appareil de votre organisation tente de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="b9041-220">When you add an indicator hash for a file, you can choose to raise an alert and block the file whenever a device in your organization attempts to run it.</span></span>

<span data-ttu-id="b9041-221">Les fichiers automatiquement bloqués par un indicateur ne s’afficheront pas dans le centre de l’action du fichier, mais les alertes resteront visibles dans la file d’attente des alertes.</span><span class="sxs-lookup"><span data-stu-id="b9041-221">Files automatically blocked by an indicator won't show up in the file's Action center, but the alerts will still be visible in the Alerts queue.</span></span>

<span data-ttu-id="b9041-222">Pour plus [d’informations sur](manage-indicators.md) le blocage et l’augmentation des alertes sur les fichiers, voir gérer les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="b9041-222">See [manage indicators](manage-indicators.md) for more details on blocking and raising alerts on files.</span></span>

<span data-ttu-id="b9041-223">Pour arrêter le blocage d’un fichier, supprimez l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="b9041-223">To stop blocking a file, remove the indicator.</span></span> <span data-ttu-id="b9041-224">Vous pouvez le faire via l’action **Modifier l’indicateur** sur la page de profil du fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-224">You can do so via the **Edit Indicator** action on the file's profile page.</span></span> <span data-ttu-id="b9041-225">Cette action sera visible à la  même position que l’action Ajouter un indicateur, avant que vous n’ajoutiez l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="b9041-225">This action will be visible in the same position as the **Add Indicator** action, before you added the indicator.</span></span>

<span data-ttu-id="b9041-226">Vous pouvez également modifier les indicateurs à partir de la page **Paramètres,** sous **Indicateurs**  >  **de règles.**</span><span class="sxs-lookup"><span data-stu-id="b9041-226">You can also edit indicators from  the **Settings** page, under **Rules** > **Indicators**.</span></span> <span data-ttu-id="b9041-227">Les indicateurs sont répertoriés dans cette zone par le hachage de leur fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-227">Indicators are listed in this area by their file's hash.</span></span>

## <a name="consult-a-threat-expert"></a><span data-ttu-id="b9041-228">Consulter un spécialiste des menaces</span><span class="sxs-lookup"><span data-stu-id="b9041-228">Consult a threat expert</span></span>

<span data-ttu-id="b9041-229">Consultez un expert microsoft en matière de menaces pour obtenir plus d’informations sur un appareil potentiellement compromis ou déjà compromis.</span><span class="sxs-lookup"><span data-stu-id="b9041-229">Consult a Microsoft threat expert for more insights on a potentially compromised device, or already compromised devices.</span></span> <span data-ttu-id="b9041-230">Spécialistes des menaces Microsoft sont en action directement à partir du Centre de sécurité Microsoft Defender pour une réponse précise et opportune.</span><span class="sxs-lookup"><span data-stu-id="b9041-230">Microsoft Threat Experts are engaged directly from within the Microsoft Defender Security Center for timely and accurate response.</span></span> <span data-ttu-id="b9041-231">Les experts fournissent des informations sur un appareil potentiellement compromis et vous aident à comprendre les menaces complexes et les notifications d’attaque ciblée.</span><span class="sxs-lookup"><span data-stu-id="b9041-231">Experts provide insights on a potentially compromised device and help you understand complex threats and targeted attack notifications.</span></span> <span data-ttu-id="b9041-232">Ils peuvent également fournir des informations sur les alertes ou un contexte d’intelligence des menaces que vous voyez sur votre tableau de bord du portail.</span><span class="sxs-lookup"><span data-stu-id="b9041-232">They can also provide information about the alerts or a threat intelligence context that you see on your portal dashboard.</span></span>

<span data-ttu-id="b9041-233">Pour [plus d’informations, consultez un Expert en](/microsoft-365/security/defender-endpoint/configure-microsoft-threat-experts#consult-a-microsoft-threat-expert-about-suspicious-cybersecurity-activities-in-your-organization) menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9041-233">See [Consult a Microsoft Threat Expert](/microsoft-365/security/defender-endpoint/configure-microsoft-threat-experts#consult-a-microsoft-threat-expert-about-suspicious-cybersecurity-activities-in-your-organization) for details.</span></span>

## <a name="check-activity-details-in-action-center"></a><span data-ttu-id="b9041-234">Vérifier les détails de l’activité dans le Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="b9041-234">Check activity details in Action center</span></span>

<span data-ttu-id="b9041-235">Le **centre de données fournit** des informations sur les actions qui ont été entreprises sur un appareil ou un fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-235">The **Action center** provides information on actions that were taken on a device or file.</span></span> <span data-ttu-id="b9041-236">Vous pouvez afficher les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b9041-236">You can view the following details:</span></span>

- <span data-ttu-id="b9041-237">Collection de packages d’examen</span><span class="sxs-lookup"><span data-stu-id="b9041-237">Investigation package collection</span></span>
- <span data-ttu-id="b9041-238">Analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="b9041-238">Antivirus scan</span></span>
- <span data-ttu-id="b9041-239">Restriction d’application</span><span class="sxs-lookup"><span data-stu-id="b9041-239">App restriction</span></span>
- <span data-ttu-id="b9041-240">Isolation de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b9041-240">Device isolation</span></span>

<span data-ttu-id="b9041-241">Tous les autres détails connexes sont également affichés, tels que la date/l’heure de soumission, l’utilisateur à l’envoi et si l’action a réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="b9041-241">All other related details are also shown, such as submission date/time, submitting user, and if the action succeeded or failed.</span></span>

![Image du centre de travail avec des informations](images/action-center-details.png)

## <a name="deep-analysis"></a><span data-ttu-id="b9041-243">Analyse profonde</span><span class="sxs-lookup"><span data-stu-id="b9041-243">Deep analysis</span></span>

<span data-ttu-id="b9041-244">Les enquêtes sur la cybersécurité sont généralement déclenchées par une alerte.</span><span class="sxs-lookup"><span data-stu-id="b9041-244">Cyber security investigations are typically triggered by an alert.</span></span> <span data-ttu-id="b9041-245">Les alertes sont liées à un ou plusieurs fichiers observés qui sont souvent nouveaux ou inconnus.</span><span class="sxs-lookup"><span data-stu-id="b9041-245">Alerts are related to one or more observed files that are often new or unknown.</span></span> <span data-ttu-id="b9041-246">La sélection d’un fichier vous permet d’afficher l’affichage des fichiers dans lequel vous pouvez voir les métadonnées du fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-246">Selecting a file takes you to the file view where you can see the file's metadata.</span></span> <span data-ttu-id="b9041-247">Pour enrichir les données liées au fichier, vous pouvez envoyer le fichier pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="b9041-247">To enrich the data related to the file, you can submit the file for deep analysis.</span></span>

<span data-ttu-id="b9041-248">La fonctionnalité d’analyse approfondie exécute un fichier dans un environnement cloud sécurisé et entièrement instrumenté.</span><span class="sxs-lookup"><span data-stu-id="b9041-248">The Deep analysis feature executes a file in a secure, fully instrumented cloud environment.</span></span> <span data-ttu-id="b9041-249">Les résultats de l’analyse approfondie montrent les activités du fichier, les comportements observés et les artefacts associés, tels que les fichiers supprimés, les modifications du Registre et la communication avec les fai.</span><span class="sxs-lookup"><span data-stu-id="b9041-249">Deep analysis results show the file's activities, observed behaviors, and associated artifacts, such as dropped files, registry modifications, and communication with IPs.</span></span>
<span data-ttu-id="b9041-250">L’analyse approfondie prend actuellement en charge l’analyse complète des fichiers exécutables portables (notamment les fichiers _.exe_ et _.dll_ portables).</span><span class="sxs-lookup"><span data-stu-id="b9041-250">Deep analysis currently supports extensive analysis of portable executable (PE) files (including _.exe_ and _.dll_ files).</span></span>

<span data-ttu-id="b9041-251">L’analyse approfondie d’un fichier prend plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="b9041-251">Deep analysis of a file takes several minutes.</span></span> <span data-ttu-id="b9041-252">Une fois l’analyse de fichier terminée, l’onglet Analyse approfondie se met à jour pour afficher un résumé et la date et l’heure des derniers résultats disponibles.</span><span class="sxs-lookup"><span data-stu-id="b9041-252">Once the file analysis is complete, the Deep Analysis tab will update to display a summary and the date and time of the latest available results.</span></span>

<span data-ttu-id="b9041-253">Le résumé de l’analyse approfondie inclut une liste des comportements *observés,* dont certains peuvent indiquer une activité malveillante, et des éléments *observables,* y compris les IP contactés et les fichiers créés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="b9041-253">The deep analysis summary includes a list of observed *behaviors*, some of which can indicate malicious activity, and *observables*, including contacted IPs and files created on the disk.</span></span> <span data-ttu-id="b9041-254">Si rien n’est trouvé, ces sections affichent un message court.</span><span class="sxs-lookup"><span data-stu-id="b9041-254">If nothing was found, these sections will display a brief message.</span></span>

<span data-ttu-id="b9041-255">Les résultats d’une analyse approfondie sont en correspondance avec les informations sur les menaces et les correspondances génèrent des alertes appropriées.</span><span class="sxs-lookup"><span data-stu-id="b9041-255">Results of deep analysis are matched against threat intelligence and any matches will generate appropriate alerts.</span></span>

<span data-ttu-id="b9041-256">Utilisez la fonctionnalité d’analyse approfondie pour examiner les détails d’un fichier, généralement lors d’un examen d’une alerte ou pour toute autre raison pour laquelle vous suspectez un comportement malveillant.</span><span class="sxs-lookup"><span data-stu-id="b9041-256">Use the deep analysis feature to investigate the details of any file, usually during an investigation of an alert or for any other reason where you suspect malicious behavior.</span></span> <span data-ttu-id="b9041-257">Cette fonctionnalité est disponible dans **l’onglet Analyse** approfondie, sur la page de profil du fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-257">This feature is available within the **Deep analysis** tab, on the file's profile page.</span></span><br/>
<br/>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4aAYy?rel=0]

<span data-ttu-id="b9041-258">**L’envoi** pour analyse approfondie est activé lorsque le fichier est disponible dans la collection d’exemples principal Defender for Endpoint, ou s’il a été observé sur un appareil Windows 10 qui prend en charge l’envoi à une analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="b9041-258">**Submit for deep analysis** is enabled when the file is available in the Defender for Endpoint backend sample collection, or if it was observed on a Windows 10 device that supports submitting to deep analysis.</span></span>

> [!NOTE]
> <span data-ttu-id="b9041-259">Seuls les fichiers Windows 10 peuvent être collectés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b9041-259">Only files from Windows 10 can be automatically collected.</span></span>

<span data-ttu-id="b9041-260">Vous pouvez également soumettre un exemple via le portail du Centre de sécurité [Microsoft](https://www.microsoft.com/security/portal/submission/submit.aspx) si le  fichier n’a pas été observé sur un appareil Windows 10 et attendre que le bouton Envoyer pour analyse approfondie devienne disponible.</span><span class="sxs-lookup"><span data-stu-id="b9041-260">You can also submit a sample through the [Microsoft Security Center Portal](https://www.microsoft.com/security/portal/submission/submit.aspx) if the file wasn't observed on a Windows 10 device, and wait for **Submit for deep analysis** button to become available.</span></span>

> [!NOTE]
> <span data-ttu-id="b9041-261">En raison des flux de traitement principal dans le portail du Centre de sécurité Microsoft, il peut y avoir jusqu’à 10 minutes de latence entre l’envoi de fichiers et la disponibilité de la fonctionnalité d’analyse approfondie dans Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b9041-261">Due to backend processing flows in the Microsoft Security Center Portal, there could be up to 10 minutes of latency between file submission and availability of the deep analysis feature in Defender for Endpoint.</span></span>

<span data-ttu-id="b9041-262">Lorsque l’exemple est collecté, Defender pour point de terminaison exécute le fichier dans un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b9041-262">When the sample is collected, Defender for Endpoint runs the file in a secure environment.</span></span> <span data-ttu-id="b9041-263">Il crée ensuite un rapport détaillé des comportements observés et des artefacts associés, tels que les fichiers déposés sur les appareils, la communication avec les fai et les modifications du Registre.</span><span class="sxs-lookup"><span data-stu-id="b9041-263">It then creates a detailed report of observed behaviors and associated artifacts, such as files dropped on devices, communication to IPs, and registry modifications.</span></span>

### <a name="submit-files-for-deep-analysis"></a><span data-ttu-id="b9041-264">Soumettre des fichiers pour analyse approfondie</span><span class="sxs-lookup"><span data-stu-id="b9041-264">Submit files for deep analysis</span></span>

1. <span data-ttu-id="b9041-265">Sélectionnez le fichier que vous souhaitez soumettre pour une analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="b9041-265">Select the file that you want to submit for deep analysis.</span></span> <span data-ttu-id="b9041-266">Vous pouvez sélectionner ou rechercher un fichier dans l’un des affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="b9041-266">You can select or search a file from any of the following views:</span></span>

    - <span data-ttu-id="b9041-267">Alertes : sélectionnez les liens de fichier dans **la description** ou **les détails** dans la chronologie de l’artefact</span><span class="sxs-lookup"><span data-stu-id="b9041-267">Alerts - select the file links from the **Description** or **Details** in the Artifact timeline</span></span>
    - <span data-ttu-id="b9041-268">**Liste des appareils** : sélectionnez les liens de fichiers dans la **section Description** **ou Détails** de l’appareil **dans l’organisation**</span><span class="sxs-lookup"><span data-stu-id="b9041-268">**Devices list** - select the file links from the **Description** or **Details** in the **Device in organization** section</span></span>
    - <span data-ttu-id="b9041-269">Zone de recherche : **sélectionnez Fichier** dans le menu déroulant et entrez le nom du fichier</span><span class="sxs-lookup"><span data-stu-id="b9041-269">Search box - select **File** from the drop–down menu and enter the file name</span></span>

2. <span data-ttu-id="b9041-270">Dans **l’onglet Analyse approfondie** de l’affichage de fichier, sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="b9041-270">In the **Deep analysis** tab of the file view, select **Submit**.</span></span>

   ![Vous pouvez uniquement envoyer des fichiers PE dans la section Détails du fichier](images/submit-file.png)

   > [!NOTE]
   > <span data-ttu-id="b9041-272">Seuls les fichiers PE sont pris en _charge,.exe_ et _.dll_ fichiers.</span><span class="sxs-lookup"><span data-stu-id="b9041-272">Only PE files are supported, including _.exe_ and _.dll_ files.</span></span>

<span data-ttu-id="b9041-273">Une barre de progression s’affiche et fournit des informations sur les différentes étapes de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b9041-273">A progress bar is displayed and provides information on the different stages of the analysis.</span></span> <span data-ttu-id="b9041-274">Vous pouvez ensuite afficher le rapport une fois l’analyse effectuée.</span><span class="sxs-lookup"><span data-stu-id="b9041-274">You can then view the report when the analysis is done.</span></span>

> [!NOTE]
> <span data-ttu-id="b9041-275">Selon la disponibilité de l’appareil, la durée de collecte des échantillons peut varier.</span><span class="sxs-lookup"><span data-stu-id="b9041-275">Depending on device availability, sample collection time can vary.</span></span> <span data-ttu-id="b9041-276">Il existe un délai d'3 heures pour la collecte d’exemples.</span><span class="sxs-lookup"><span data-stu-id="b9041-276">There is a 3–hour timeout for sample collection.</span></span> <span data-ttu-id="b9041-277">La collecte échoue et l’opération est abandonnée s’il n’y a pas de Windows 10'appareil en ligne à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="b9041-277">The collection will fail and the operation will abort if there is no online Windows 10 device reporting at that time.</span></span> <span data-ttu-id="b9041-278">Vous pouvez soumettre de nouveau des fichiers pour une analyse approfondie afin d’obtenir des données récentes sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-278">You can re–submit files for deep analysis to get fresh data on the file.</span></span>

### <a name="view-deep-analysis-reports"></a><span data-ttu-id="b9041-279">Afficher des rapports d’analyse approfondie</span><span class="sxs-lookup"><span data-stu-id="b9041-279">View deep analysis reports</span></span>

<span data-ttu-id="b9041-280">Consultez le rapport d’analyse approfondie fourni pour afficher des informations plus détaillées sur le fichier que vous avez envoyé.</span><span class="sxs-lookup"><span data-stu-id="b9041-280">View the provided deep analysis report to see more in-depth insights on the file you submitted.</span></span> <span data-ttu-id="b9041-281">Cette fonctionnalité est disponible dans le contexte de l’affichage de fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-281">This feature is available in the file view context.</span></span>

<span data-ttu-id="b9041-282">Vous pouvez afficher le rapport complet qui fournit des détails sur les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="b9041-282">You can view the comprehensive report that provides details on the following sections:</span></span>

- <span data-ttu-id="b9041-283">Behaviors</span><span class="sxs-lookup"><span data-stu-id="b9041-283">Behaviors</span></span>
- <span data-ttu-id="b9041-284">Observables</span><span class="sxs-lookup"><span data-stu-id="b9041-284">Observables</span></span>

<span data-ttu-id="b9041-285">Les détails fournis peuvent vous aider à déterminer s’il existe des indications d’une attaque potentielle.</span><span class="sxs-lookup"><span data-stu-id="b9041-285">The details provided can help you investigate if there are indications of a potential attack.</span></span>

1. <span data-ttu-id="b9041-286">Sélectionnez le fichier que vous avez soumis pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="b9041-286">Select the file you submitted for deep analysis.</span></span>
2. <span data-ttu-id="b9041-287">Sélectionnez **l’onglet Analyse** approfondie. S’il existe des rapports précédents, le résumé du rapport s’affiche dans cet onglet.</span><span class="sxs-lookup"><span data-stu-id="b9041-287">Select the **Deep analysis** tab. If there are any previous reports, the report summary will appear in this tab.</span></span>

    ![Le rapport d’analyse approfondie présente des informations détaillées sur un certain nombre de catégories](images/analysis-results-nothing500.png)

#### <a name="troubleshoot-deep-analysis"></a><span data-ttu-id="b9041-289">Résoudre les problèmes d’analyse approfondie</span><span class="sxs-lookup"><span data-stu-id="b9041-289">Troubleshoot deep analysis</span></span>

<span data-ttu-id="b9041-290">Si vous êtes face à un problème lors de la tentative d’soumission d’un fichier, essayez chacune des étapes de dépannage suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9041-290">If you come across a problem when trying to submit a file, try each of the following troubleshooting steps.</span></span>

1. <span data-ttu-id="b9041-291">Assurez-vous que le fichier en question est un fichier PE.</span><span class="sxs-lookup"><span data-stu-id="b9041-291">Ensure that the file in question is a PE file.</span></span> <span data-ttu-id="b9041-292">Les fichiers PE ont généralement des extensions _.exe_ ou _.dll_ (programmes ou applications exécutables).</span><span class="sxs-lookup"><span data-stu-id="b9041-292">PE files typically have _.exe_ or _.dll_ extensions (executable programs or applications).</span></span>
2. <span data-ttu-id="b9041-293">Assurez-vous que le service a accès au fichier, qu’il existe toujours et qu’il n’a pas été endommagé ou modifié.</span><span class="sxs-lookup"><span data-stu-id="b9041-293">Ensure the service has access to the file, that it still exists, and hasn't been corrupted or modified.</span></span>
3. <span data-ttu-id="b9041-294">Patientez quelques minutes et essayez de soumettre à nouveau le fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-294">Wait a short while and try to submit the file again.</span></span> <span data-ttu-id="b9041-295">La file d’attente est peut-être pleine ou une erreur de communication ou de connexion temporaire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b9041-295">The queue may be full, or there was a temporary connection or communication error.</span></span>
4. <span data-ttu-id="b9041-296">Si la stratégie de collection d’exemples n’est pas configurée, le comportement par défaut consiste à autoriser la collecte d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="b9041-296">If the sample collection policy isn't configured, then the default behavior is to allow sample collection.</span></span> <span data-ttu-id="b9041-297">Si elle est configurée, vérifiez que le paramètre de stratégie autorise la collecte d’exemples avant de soumettre à nouveau le fichier.</span><span class="sxs-lookup"><span data-stu-id="b9041-297">If it's configured, then verify the policy setting allows sample collection before submitting the file again.</span></span> <span data-ttu-id="b9041-298">Lorsque l’exemple de collection est configuré, vérifiez la valeur de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="b9041-298">When sample collection is configured, then check the following registry value:</span></span>

    ```powershell
    Path: HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection
    Name: AllowSampleCollection
    Type: DWORD
    Hexadecimal value :
      Value = 0 – block sample collection
      Value = 1 – allow sample collection
    ```

1. <span data-ttu-id="b9041-299">Modifiez l’unité d’organisation par le biais de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b9041-299">Change the organizational unit through the Group Policy.</span></span> <span data-ttu-id="b9041-300">Pour plus d’informations, [voir Configurer avec la stratégie de groupe.](configure-endpoints-gp.md)</span><span class="sxs-lookup"><span data-stu-id="b9041-300">For more information, see [Configure with Group Policy](configure-endpoints-gp.md).</span></span>
1. <span data-ttu-id="b9041-301">Si ces étapes ne résolvent pas le problème, contactez [winatp@microsoft.com](mailto:winatp@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b9041-301">If these steps do not resolve the issue, contact [winatp@microsoft.com](mailto:winatp@microsoft.com).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9041-302">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9041-302">Related topics</span></span>

- [<span data-ttu-id="b9041-303">Prendre des mesures de réponse sur un appareil</span><span class="sxs-lookup"><span data-stu-id="b9041-303">Take response actions on a device</span></span>](respond-machine-alerts.md)
- [<span data-ttu-id="b9041-304">Examiner des fichiers</span><span class="sxs-lookup"><span data-stu-id="b9041-304">Investigate files</span></span>](investigate-files.md)
