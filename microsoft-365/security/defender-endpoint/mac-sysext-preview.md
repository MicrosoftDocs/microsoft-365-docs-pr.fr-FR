---
title: 'Microsoft Defender pour point de terminaison sur Mac : extensions système (prévisualisation)'
description: Cet article contient des instructions pour essayer la fonctionnalité d'extensions système de Microsoft Defender pour Endpoint sur Mac. Cette fonctionnalité est actuellement en prévisualisation publique.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, mac, noyau, système, extensions, contrôle
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: security
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ROBOTS: noindex,nofollow
ms.technology: mde
ms.openlocfilehash: cc148bcc0b2623eaaa8d31ef50708174264fa3b2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934944"
---
# <a name="microsoft-defender-for-endpoint-on-macos---system-extensions-public-preview"></a><span data-ttu-id="85dde-105">Microsoft Defender pour point de terminaison sur macOS : version d'évaluation publique des extensions système)</span><span class="sxs-lookup"><span data-stu-id="85dde-105">Microsoft Defender for Endpoint on macOS - system extensions public preview)</span></span>

<span data-ttu-id="85dde-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="85dde-106">**Applies to:**</span></span>
- [<span data-ttu-id="85dde-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="85dde-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="85dde-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="85dde-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="85dde-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="85dde-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="85dde-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="85dde-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="85dde-111">En adéquation avec l'évolution de macOS, nous préparons une mise à jour defender pour point de terminaison sur Mac qui tire parti des extensions système au lieu des extensions de noyau.</span><span class="sxs-lookup"><span data-stu-id="85dde-111">In alignment with macOS evolution, we are preparing a Defender for Endpoint on Mac update that leverages system extensions instead of kernel extensions.</span></span> <span data-ttu-id="85dde-112">Cette mise à jour s'applique uniquement à macOS Genrer (10.15.4) et aux versions ultérieures de macOS.</span><span class="sxs-lookup"><span data-stu-id="85dde-112">This update will only apply to macOS Catalina (10.15.4) and later versions of macOS.</span></span>

<span data-ttu-id="85dde-113">Cette fonctionnalité est actuellement en prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="85dde-113">This functionality is currently in public preview.</span></span> <span data-ttu-id="85dde-114">Cet article explique comment activer cette fonctionnalité sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="85dde-114">This article describes how to enable this functionality on your device.</span></span> <span data-ttu-id="85dde-115">Vous pouvez tester cette fonctionnalité localement sur votre propre appareil ou la configurer à distance via un outil de gestion.</span><span class="sxs-lookup"><span data-stu-id="85dde-115">You can try out this feature locally on your own device or configure it remotely through a management tool.</span></span>

<span data-ttu-id="85dde-116">Ces étapes supposent que Defender for Endpoint est déjà en cours d'exécution sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="85dde-116">These steps assume you already have Defender for Endpoint running on your device.</span></span> <span data-ttu-id="85dde-117">Pour plus d'informations, voir [cette page](microsoft-defender-endpoint-mac.md).</span><span class="sxs-lookup"><span data-stu-id="85dde-117">For more information, see [this page](microsoft-defender-endpoint-mac.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="85dde-118">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="85dde-118">Known issues</span></span>

- <span data-ttu-id="85dde-119">Nous avons reçu des rapports sur l'extension réseau qui interfère avec l'extension Kerberos d' cesso Apple.</span><span class="sxs-lookup"><span data-stu-id="85dde-119">We’ve received reports of the network extension interfering with the Apple SSO Kerberos extension.</span></span>
- <span data-ttu-id="85dde-120">La version actuelle du produit installe toujours une extension de noyau.</span><span class="sxs-lookup"><span data-stu-id="85dde-120">The current version of the product still installs a kernel extension.</span></span> <span data-ttu-id="85dde-121">L'extension de noyau est uniquement utilisée comme mécanisme de retour et sera supprimée avant que cette fonctionnalité n'atteigne la prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="85dde-121">The kernel extension is only used as a fallback mechanism and will be removed before this feature reaches public preview.</span></span>
- <span data-ttu-id="85dde-122">Nous travaillons toujours sur une version de produit qui se déploie et fonctionne correctement sur macOS 11 Big Sur.</span><span class="sxs-lookup"><span data-stu-id="85dde-122">We're still working on a product version that deploys and functions properly on macOS 11 Big Sur.</span></span>

## <a name="deployment-prerequisites"></a><span data-ttu-id="85dde-123">Conditions préalables au déploiement</span><span class="sxs-lookup"><span data-stu-id="85dde-123">Deployment prerequisites</span></span>

- <span data-ttu-id="85dde-124">Version minimale du système d'exploitation macOS **: 10.15.4**</span><span class="sxs-lookup"><span data-stu-id="85dde-124">Minimum macOS operating system version: **10.15.4**</span></span>
- <span data-ttu-id="85dde-125">Version minimale du produit **: 101.03.73**</span><span class="sxs-lookup"><span data-stu-id="85dde-125">Minimum product version: **101.03.73**</span></span>
- <span data-ttu-id="85dde-126">Votre appareil doit se trouver dans le canal de mise à jour **rapide Insider.**</span><span class="sxs-lookup"><span data-stu-id="85dde-126">Your device must be in the **Insider Fast update channel**.</span></span> <span data-ttu-id="85dde-127">Vous pouvez vérifier le canal de mise à jour à l'aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="85dde-127">You can check the update channel by using the following command:</span></span>

  ```bash
  mdatp health --field release_ring
  ```

  <span data-ttu-id="85dde-128">Si votre appareil n'est pas déjà dans le canal Insider Fast Update, exécutez la commande suivante à partir du Terminal.</span><span class="sxs-lookup"><span data-stu-id="85dde-128">If your device isn't already in the Insider Fast update channel, execute the following command from the Terminal.</span></span> <span data-ttu-id="85dde-129">La mise à jour du canal prend effet au prochain démarrage du produit (lors de l'installation de la prochaine mise à jour du produit ou lors du redémarrage de l'appareil).</span><span class="sxs-lookup"><span data-stu-id="85dde-129">The channel update takes effect the next time the product starts (when the next product update is installed, or when the device is rebooted).</span></span>

  ```bash
  defaults write com.microsoft.autoupdate2 ChannelName -string Beta
  ```

  <span data-ttu-id="85dde-130">Par ailleurs, si vous êtes dans un environnement géré (JAMF ou Intune), vous pouvez configurer le canal de mise à jour à distance.</span><span class="sxs-lookup"><span data-stu-id="85dde-130">Alternatively, if you're in a managed environment (JAMF or Intune), you can configure the update channel remotely.</span></span> <span data-ttu-id="85dde-131">Pour plus d'informations, voir [Déployer les mises à jour de Microsoft Defender pour Endpoint sur Mac : définissez le nom du canal.](mac-updates.md#set-the-channel-name)</span><span class="sxs-lookup"><span data-stu-id="85dde-131">For more information, see [Deploy updates for Microsoft Defender for Endpoint on Mac: Set the channel name](mac-updates.md#set-the-channel-name).</span></span>

## <a name="deployment-steps"></a><span data-ttu-id="85dde-132">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="85dde-132">Deployment steps</span></span>

<span data-ttu-id="85dde-133">Suivez les étapes de déploiement qui correspondent à votre environnement et à votre méthode préférée pour essayer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="85dde-133">Follow the deployment steps that correspond to your environment and your preferred method of trying out this feature.</span></span>

### <a name="manual-deployment"></a><span data-ttu-id="85dde-134">Déploiement manuel</span><span class="sxs-lookup"><span data-stu-id="85dde-134">Manual deployment</span></span>

#### <a name="approve-the-system-extensions-and-enable-the-network-extension"></a><span data-ttu-id="85dde-135">Approuver les extensions système et activer l'extension réseau</span><span class="sxs-lookup"><span data-stu-id="85dde-135">Approve the system extensions and enable the network extension</span></span>

1. <span data-ttu-id="85dde-136">Une fois toutes les conditions préalables au déploiement remplies, redémarrez votre appareil pour lancer le processus d'approbation et d'activation de l'extension système.</span><span class="sxs-lookup"><span data-stu-id="85dde-136">After all deployment prerequisites are met, restart your device to launch the system extension approval and activation process.</span></span>

   <span data-ttu-id="85dde-137">Vous verrez une série d'invites système pour approuver les extensions système Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="85dde-137">You'll see a series of system prompts to approve the Defender for Endpoint system extensions.</span></span> <span data-ttu-id="85dde-138">Vous devez approuver toutes **les** invites de la série, car macOS nécessite une approbation explicite pour chaque extension installée par Defender for Endpoint sur Mac sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="85dde-138">You must approve **all** prompts from the series, because macOS requires an explicit approval for each extension that Defender for Endpoint on Mac installs on the device.</span></span>
   
   <span data-ttu-id="85dde-139">Pour chaque approbation, sélectionnez Ouvrir les préférences **de sécurité,** puis **autorisez** l'extension système à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="85dde-139">For each approval, select **Open Security Preferences** and then select **Allow** to allow the system extension to run.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="85dde-140">Vous devez fermer et rouvrir la **fenêtre** Sécurité des préférences système  >  **& confidentialité** entre les approbations suivantes.</span><span class="sxs-lookup"><span data-stu-id="85dde-140">You must close and reopen the **System Preferences** > **Security & Privacy** window between subsequent approvals.</span></span> <span data-ttu-id="85dde-141">Sinon, macOS n'affichera pas l'approbation suivante.</span><span class="sxs-lookup"><span data-stu-id="85dde-141">Otherwise, macOS will not display the next approval.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="85dde-142">Il y a un délai d'une minute avant que le produit ne revenir à l'extension du noyau.</span><span class="sxs-lookup"><span data-stu-id="85dde-142">There is a one-minute timeout before the product falls back to the kernel extension.</span></span> <span data-ttu-id="85dde-143">Cela garantit que l'appareil est protégé.</span><span class="sxs-lookup"><span data-stu-id="85dde-143">This ensures that the device is protected.</span></span>
   >
   > <span data-ttu-id="85dde-144">Si plus d'une minute s'écoule, redémarrez le daemon en redémarré l'appareil ou en utilisant pour déclencher à nouveau le flux `sudo killall -9 wdavdaemon` d'approbation.</span><span class="sxs-lookup"><span data-stu-id="85dde-144">If more than one minute elapses, restart the daemon by rebooting the device or by using `sudo killall -9 wdavdaemon` to trigger the approval flow again.</span></span>

   ![Fenêtre fenêtre fenêtre d'approbation de l'extension système](images/mac-system-extension-approval.png)

   ![Fenêtre d'approbation de l'extension système](images/mac-system-extension-pref.png)

1. <span data-ttu-id="85dde-147">Une fois les extensions système approuvées, macOS demande une approbation pour autoriser le filtrage du trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="85dde-147">After the system extensions are approved, macOS prompts for an approval to allow network traffic to be filtered.</span></span> <span data-ttu-id="85dde-148">Cliquez sur **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="85dde-148">Click **Allow**.</span></span>

   ![Fenêtre fenêtre d'approbation de l'extension réseau](images/mac-system-extension-filter.png)

#### <a name="grant-full-disk-access-to-the-endpoint-security-system-extension"></a><span data-ttu-id="85dde-150">Accorder un accès disque total à l'extension du système de sécurité des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="85dde-150">Grant Full Disk Access to the Endpoint Security system extension</span></span>

<span data-ttu-id="85dde-151">Ouvrez **l'onglet** Sécurité des préférences système & confidentialité et accordez un accès disque total à l'extension de sécurité du point de  >    >   **terminaison Microsoft Defender.** </span><span class="sxs-lookup"><span data-stu-id="85dde-151">Open the **System Preferences** > **Security & Privacy** > **Privacy** tab and grant **Full Disk Access** to the **Microsoft Defender Endpoint Security Extension**.</span></span>

![Accès disque complet pour l'extension du système de sécurité des points de terminaison](images/mac-system-extension-fda.png)

#### <a name="reboot-your-device"></a><span data-ttu-id="85dde-153">Redémarrer votre appareil</span><span class="sxs-lookup"><span data-stu-id="85dde-153">Reboot your device</span></span>

<span data-ttu-id="85dde-154">Pour que les modifications prennent effet, vous devez redémarrer votre appareil.</span><span class="sxs-lookup"><span data-stu-id="85dde-154">In order for the changes to take effect, you must reboot your device.</span></span>

#### <a name="verify-that-the-system-extensions-are-running"></a><span data-ttu-id="85dde-155">Vérifier que les extensions système sont en cours d'exécution</span><span class="sxs-lookup"><span data-stu-id="85dde-155">Verify that the system extensions are running</span></span>

<span data-ttu-id="85dde-156">À partir du Terminal, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="85dde-156">From the Terminal, run the following command:</span></span>

```bash
mdatp health --field real_time_protection_subsystem
```

<span data-ttu-id="85dde-157">La sortie `endpoint_security_extension` terminal indique que le produit utilise la fonctionnalité d'extensions système.</span><span class="sxs-lookup"><span data-stu-id="85dde-157">Terminal output `endpoint_security_extension` indicates the product is using the system extensions functionality.</span></span>

### <a name="managed-deployment"></a><span data-ttu-id="85dde-158">Déploiement géré</span><span class="sxs-lookup"><span data-stu-id="85dde-158">Managed deployment</span></span>

<span data-ttu-id="85dde-159">Reportez-vous aux nouveaux profils de [configuration pour macOS Fonctionnalité et](mac-sysext-policies.md#jamf) versions plus récentes de macOS : JAMF pour les nouveaux profils de configuration que vous devez déployer pour cette nouvelle fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="85dde-159">Refer to [New configuration profiles for macOS Catalina and newer versions of macOS: JAMF](mac-sysext-policies.md#jamf) for the new configuration profiles you must deploy for this new feature.</span></span>

<span data-ttu-id="85dde-160">En plus de ces profils, veillez à configurer les appareils cibles pour qu'ils soient dans le canal insider de mise à jour rapide, comme décrit dans les conditions [préalables au déploiement.](#deployment-prerequisites)</span><span class="sxs-lookup"><span data-stu-id="85dde-160">In addition to those profiles, make sure to configure the target devices to be in the Insider Fast update channel, as described in [Deployment prerequisites](#deployment-prerequisites).</span></span>

<span data-ttu-id="85dde-161">Sur un appareil où toutes les conditions préalables sont remplies et où les nouveaux profils de configuration ont été déployés, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="85dde-161">On a device where all prerequisites are met and the new configuration profiles have been deployed, run the following command:</span></span>

```bash
$ mdatp health --field real_time_protection_subsystem
```

<span data-ttu-id="85dde-162">Si cette commande est `endpoint_security_extension` imprimée, le produit utilise la fonctionnalité d'extensions système.</span><span class="sxs-lookup"><span data-stu-id="85dde-162">If this command prints `endpoint_security_extension`, the product is using the system extensions functionality.</span></span>

## <a name="validate-basic-scenarios"></a><span data-ttu-id="85dde-163">Valider les scénarios de base</span><span class="sxs-lookup"><span data-stu-id="85dde-163">Validate basic scenarios</span></span>

1. <span data-ttu-id="85dde-164">Testez la détection EICAR (Computer Antivirus Research) de l'European Institute for Computer Antivirus Research.</span><span class="sxs-lookup"><span data-stu-id="85dde-164">Test European Institute for Computer Antivirus Research (EICAR) detection.</span></span> <span data-ttu-id="85dde-165">À partir d'une fenêtre Terminal, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="85dde-165">From a Terminal window, run the following command:</span></span>

   ```bash
   curl -o eicar.txt https://secure.eicar.org/eicar.com.txt
   ```

   <span data-ttu-id="85dde-166">Vérifiez que le fichier EICAR est mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="85dde-166">Verify that the EICAR file is quarantined.</span></span> <span data-ttu-id="85dde-167">Vous pouvez vérifier l'état du fichier dans la page Historique de la protection dans l'interface utilisateur ou à partir d'une ligne de commande à l'aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="85dde-167">You can verify the file's status on the Protection History page in the user interface, or from a command line by using the following command:</span></span>

    ```bash
    mdatp threat list
    ```

2. <span data-ttu-id="85dde-168">Testez le scénario EDR (Endpoint Detection and Response).</span><span class="sxs-lookup"><span data-stu-id="85dde-168">Test the Endpoint Detection and Response (EDR) DIY scenario.</span></span> <span data-ttu-id="85dde-169">À partir d'une fenêtre terminal, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="85dde-169">From a terminal window, run the following command:</span></span>

   ```bash
   curl -o "MDATP MacOS DIY.zip" https://aka.ms/mdatpmacosdiy
   ```

   <span data-ttu-id="85dde-170">Validez que deux alertes ont été ouvertes dans le portail sur la page de l'ordinateur pour les scénarios EICAR et EDR PORTAL.</span><span class="sxs-lookup"><span data-stu-id="85dde-170">Validate that two alerts popped up in the portal on the machine page for EICAR and EDR DIY scenarios.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="85dde-171">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="85dde-171">Frequently asked questions</span></span>

- <span data-ttu-id="85dde-172">Q : Pourquoi est-ce que je le vois `kernel_extension` encore lorsque j'exécute `mdatp health --field real_time_protection_subsystem` ?</span><span class="sxs-lookup"><span data-stu-id="85dde-172">Q: Why am I still seeing `kernel_extension` when I run `mdatp health --field real_time_protection_subsystem`?</span></span>

    <span data-ttu-id="85dde-173">R : Reportez-vous à la section [Conditions préalables au](#deployment-prerequisites) déploiement et vérifiez que toutes les conditions préalables sont remplies.</span><span class="sxs-lookup"><span data-stu-id="85dde-173">A: Refer back to the [Deployment prerequisites](#deployment-prerequisites) section and double-check that all prerequisites are met.</span></span> <span data-ttu-id="85dde-174">Si toutes les conditions préalables sont remplies, redémarrez votre appareil et vérifiez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="85dde-174">If all prerequisites are met, restart your device and check again.</span></span>

- <span data-ttu-id="85dde-175">Q : Quand macOS 11 Big Sur sera-t-il pris en charge ?</span><span class="sxs-lookup"><span data-stu-id="85dde-175">Q: When will macOS 11 Big Sur be supported?</span></span>

    <span data-ttu-id="85dde-176">R : Nous travaillons activement à l'ajout de la prise en charge de macOS 11.</span><span class="sxs-lookup"><span data-stu-id="85dde-176">A: We are actively working on adding support for macOS 11.</span></span> <span data-ttu-id="85dde-177">Nous publierons plus [d'informations](mac-whatsnew.md) sur la page Nouveautés.</span><span class="sxs-lookup"><span data-stu-id="85dde-177">We will post more information to the [What's new](mac-whatsnew.md) page.</span></span>
