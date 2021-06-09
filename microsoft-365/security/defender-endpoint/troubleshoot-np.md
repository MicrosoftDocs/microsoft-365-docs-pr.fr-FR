---
title: Résoudre les problèmes liés à la protection du réseau
description: Ressources et exemple de code pour résoudre les problèmes avec la protection réseau dans Microsoft Defender for Endpoint.
keywords: résoudre les problèmes, erreur, corriger, windows defender eg, asr, rules, hips, troubleshoot, audit, exclusion, false positive, broken, blocking, Microsoft Defender for Endpoint
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
author: dansimp
ms.author: dansimp
ms.reviewer: oogunrinde
manager: dansimp
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 481a8f15d6a41bda8dc866ce40d98c4f3717223d
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844055"
---
# <a name="troubleshoot-network-protection"></a><span data-ttu-id="9aa5f-104">Résoudre les problèmes de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="9aa5f-104">Troubleshoot network protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9aa5f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9aa5f-105">**Applies to:**</span></span>
- [<span data-ttu-id="9aa5f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9aa5f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9aa5f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9aa5f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="9aa5f-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="9aa5f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9aa5f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


<span data-ttu-id="9aa5f-110">Lorsque vous utilisez [la protection réseau,](network-protection.md) vous pouvez rencontrer des problèmes, tels que :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-110">When you use [Network protection](network-protection.md) you may encounter issues, such as:</span></span>

- <span data-ttu-id="9aa5f-111">La protection du réseau bloque un site web sécurisé (faux positif)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-111">Network protection blocks a website that is safe (false positive)</span></span>
- <span data-ttu-id="9aa5f-112">La protection du réseau ne parvient pas à bloquer un site web malveillant suspect ou connu (faux négatif)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-112">Network protection fails to block a suspicious or known malicious website (false negative)</span></span>

<span data-ttu-id="9aa5f-113">La résolution de ces problèmes se fait en quatre étapes :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-113">There are four steps to troubleshooting these problems:</span></span>

1. <span data-ttu-id="9aa5f-114">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9aa5f-114">Confirm prerequisites</span></span>
2. <span data-ttu-id="9aa5f-115">Utiliser le mode audit pour tester la règle</span><span class="sxs-lookup"><span data-stu-id="9aa5f-115">Use audit mode to test the rule</span></span>
3. <span data-ttu-id="9aa5f-116">Ajouter des exclusions pour la règle spécifiée (pour les faux positifs)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-116">Add exclusions for the specified rule (for false positives)</span></span>
4. <span data-ttu-id="9aa5f-117">Envoyer les journaux de support</span><span class="sxs-lookup"><span data-stu-id="9aa5f-117">Submit support logs</span></span>

## <a name="confirm-prerequisites"></a><span data-ttu-id="9aa5f-118">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9aa5f-118">Confirm prerequisites</span></span>

<span data-ttu-id="9aa5f-119">La protection réseau ne fonctionne que sur les appareils qui ont les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-119">Network protection will only work on devices with the following conditions:</span></span>

>[!div class="checklist"]
> - <span data-ttu-id="9aa5f-120">Les points de terminaison Windows 10 Professionnel ou Enterprise version 1709 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-120">Endpoints are running Windows 10 Pro or Enterprise edition, version 1709 or higher.</span></span>
> - <span data-ttu-id="9aa5f-121">Les points de terminaison utilisent Antivirus Microsoft Defender comme seule application de protection antivirus.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-121">Endpoints are using Microsoft Defender Antivirus as the sole antivirus protection app.</span></span> <span data-ttu-id="9aa5f-122">[Découvrez ce qui se produit lorsque vous utilisez une solution antivirus non-Microsoft.](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-122">[See what happens when you are using a non-Microsoft antivirus solution](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility).</span></span>
> - <span data-ttu-id="9aa5f-123">[La protection en temps réel](/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus) est activée.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-123">[Real-time protection](/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus) is enabled.</span></span>
> - <span data-ttu-id="9aa5f-124">[La protection cloud](/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) est activée.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-124">[Cloud-delivered protection](/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) is enabled.</span></span>
> - <span data-ttu-id="9aa5f-125">Le mode audit n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-125">Audit mode is not enabled.</span></span> <span data-ttu-id="9aa5f-126">Utilisez [la stratégie de](enable-network-protection.md#group-policy) groupe pour définir la règle sur **Désactivé** (valeur : **0**).</span><span class="sxs-lookup"><span data-stu-id="9aa5f-126">Use [Group Policy](enable-network-protection.md#group-policy) to set the rule to **Disabled** (value: **0**).</span></span>

## <a name="use-audit-mode"></a><span data-ttu-id="9aa5f-127">Utiliser le mode Audit</span><span class="sxs-lookup"><span data-stu-id="9aa5f-127">Use audit mode</span></span>

<span data-ttu-id="9aa5f-128">Vous pouvez activer la protection réseau en mode audit, puis visiter un site web que nous avons créé pour rétrograder la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-128">You can enable network protection in audit mode and then visit a website that we've created to demo the feature.</span></span> <span data-ttu-id="9aa5f-129">Toutes les connexions de site web sont autorisées par la protection réseau, mais un événement est enregistré pour indiquer toute connexion qui aurait été bloquée si la protection du réseau était activée.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-129">All website connections will be allowed by network protection but an event will be logged to indicate any connection that would have been blocked if network protection was enabled.</span></span>

1. <span data-ttu-id="9aa5f-130">Définissez la protection réseau sur **le mode Audit.**</span><span class="sxs-lookup"><span data-stu-id="9aa5f-130">Set network protection to **Audit mode**.</span></span>

   ```PowerShell
   Set-MpPreference -EnableNetworkProtection AuditMode
   ```

2. <span data-ttu-id="9aa5f-131">Effectuez l’activité de connexion à l’origine d’un problème (par exemple, essayez de visiter le site ou de vous connecter à l’adresse IP que vous bloquez ou ne voulez pas bloquer).</span><span class="sxs-lookup"><span data-stu-id="9aa5f-131">Perform the connection activity that is causing an issue (for example, attempt to visit the site, or connect to the IP address you do or don't want to block).</span></span>

3. <span data-ttu-id="9aa5f-132">[Consultez les journaux des événements](network-protection.md#review-network-protection-events-in-windows-event-viewer) de protection réseau pour voir si la fonctionnalité aurait bloqué la connexion si elle avait été définie **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="9aa5f-132">[Review the network protection event logs](network-protection.md#review-network-protection-events-in-windows-event-viewer) to see if the feature would have blocked the connection if it had been set to **Enabled**.</span></span>
   
   <span data-ttu-id="9aa5f-133">Si la protection réseau ne bloque pas une connexion que vous attendez qu’elle bloque, activez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-133">If network protection is not blocking a connection that you are expecting it should block, enable the feature.</span></span>

   ```PowerShell
   Set-MpPreference -EnableNetworkProtection Enabled
   ```

## <a name="report-a-false-positive-or-false-negative"></a><span data-ttu-id="9aa5f-134">Signaler un faux positif ou un faux négatif</span><span class="sxs-lookup"><span data-stu-id="9aa5f-134">Report a false positive or false negative</span></span>

<span data-ttu-id="9aa5f-135">Si vous avez testé la fonctionnalité avec le site de démonstration et le mode audit, et que la protection du réseau fonctionne sur des scénarios pré-configurés, mais ne fonctionne pas comme prévu pour une connexion spécifique, utilisez le formulaire d’envoi [web Windows Defender Security Intelligence](https://www.microsoft.com/wdsi/filesubmission) pour signaler un faux négatif ou un faux positif pour la protection du réseau.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-135">If you've tested the feature with the demo site and with audit mode, and network protection is working on pre-configured scenarios, but is not working as expected for a specific connection, use the [Windows Defender Security Intelligence web-based submission form](https://www.microsoft.com/wdsi/filesubmission) to report a false negative or false positive for network protection.</span></span> <span data-ttu-id="9aa5f-136">Avec un abonnement E5, vous pouvez également fournir un [lien vers n’importe quelle alerte associée.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-136">With an E5 subscription, you can also [provide a link to any associated alert](alerts-queue.md).</span></span>

<span data-ttu-id="9aa5f-137">Voir [Adresse faux positifs/négatifs dans Microsoft Defender pour le point de terminaison.](defender-endpoint-false-positives-negatives.md)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-137">See [Address false positives/negatives in Microsoft Defender for Endpoint](defender-endpoint-false-positives-negatives.md).</span></span>

## <a name="exclude-website-from-network-protection-scope"></a><span data-ttu-id="9aa5f-138">Exclure le site web de l’étendue de protection réseau</span><span class="sxs-lookup"><span data-stu-id="9aa5f-138">Exclude website from network protection scope</span></span>

<span data-ttu-id="9aa5f-139">Pour autoriser le site web bloqué (faux positif), ajoutez son URL à la [liste des sites de confiance.](https://blogs.msdn.microsoft.com/asiatech/2014/08/19/how-to-add-web-sites-to-trusted-sites-via-gpo-from-dc-installed-ie10-or-higher-ie-version/)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-139">To allow the website that is being blocked (false positive), add its URL to the [list of trusted sites](https://blogs.msdn.microsoft.com/asiatech/2014/08/19/how-to-add-web-sites-to-trusted-sites-via-gpo-from-dc-installed-ie10-or-higher-ie-version/).</span></span> <span data-ttu-id="9aa5f-140">Les ressources Web de cette liste contournent la vérification de la protection réseau.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-140">Web resources from this list bypass the network protection check.</span></span>

## <a name="collect-diagnostic-data-for-file-submissions"></a><span data-ttu-id="9aa5f-141">Collecter des données de diagnostic pour les soumissions de fichiers</span><span class="sxs-lookup"><span data-stu-id="9aa5f-141">Collect diagnostic data for file submissions</span></span>

<span data-ttu-id="9aa5f-142">Lorsque vous signalez un problème avec la protection du réseau, vous êtes invité à collecter et à envoyer des données de diagnostic qui peuvent être utilisées par le support microsoft et les équipes d’ingénierie pour vous aider à résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-142">When you report a problem with network protection, you are asked to collect and submit diagnostic data that can be used by Microsoft support and engineering teams to help troubleshoot issues.</span></span>

1. <span data-ttu-id="9aa5f-143">Ouvrez une invite de commandes avec élévation de élévation de Windows Defender répertoire :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-143">Open an elevated command prompt and change to the Windows Defender directory:</span></span>

   ```console
   cd c:\program files\windows defender
   ```

2. <span data-ttu-id="9aa5f-144">Exécutez cette commande pour générer les journaux de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-144">Run this command to generate the diagnostic logs:</span></span>

   ```console
   mpcmdrun -getfiles
   ```

3. <span data-ttu-id="9aa5f-145">Joignez le fichier au formulaire d’envoi.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-145">Attach the file to the submission form.</span></span> <span data-ttu-id="9aa5f-146">Par défaut, les journaux de diagnostic sont enregistrés sur `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab` .</span><span class="sxs-lookup"><span data-stu-id="9aa5f-146">By default, diagnostic logs are saved at `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab`.</span></span> 

## <a name="resolve-connectivity-issues-with-network-protection-for-e5-customers"></a><span data-ttu-id="9aa5f-147">Résoudre les problèmes de connectivité avec la protection réseau (pour les clients E5)</span><span class="sxs-lookup"><span data-stu-id="9aa5f-147">Resolve connectivity issues with network protection (for E5 customers)</span></span>

<span data-ttu-id="9aa5f-148">En raison de l’environnement dans lequel la protection réseau s’exécute, Microsoft ne peut pas voir les paramètres de proxy de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-148">Due to the environment where network protection runs, Microsoft is unable to see your operating system proxy settings.</span></span> <span data-ttu-id="9aa5f-149">Dans certains cas, les clients de protection réseau ne peuvent pas accéder au service cloud.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-149">In some cases, network protection clients are unable to reach the cloud service.</span></span> <span data-ttu-id="9aa5f-150">Pour résoudre les problèmes de connectivité avec la protection réseau, configurez l’une des clés de Registre suivantes afin que la protection réseau soit informé de la configuration du proxy :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-150">To resolve connectivity issues with network protection, configure one of the following registry keys so that network protection becomes aware of the proxy configuration:</span></span>

```powershell
reg add "HKLM\Software\Microsoft\Windows Defender" /v ProxyServer /d "<proxy IP address: Port>" /f
```

<span data-ttu-id="9aa5f-151">---OR---</span><span class="sxs-lookup"><span data-stu-id="9aa5f-151">---OR---</span></span>


```powershell
reg add "HKLM\Software\Microsoft\Windows Defender" /v ProxyPacUrl /d "<Proxy PAC url>" /f
```

<span data-ttu-id="9aa5f-152">Vous pouvez configurer la clé de Registre à l’aide de PowerShell, Microsoft Endpoint Manager ou d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9aa5f-152">You can configure the registry key by using PowerShell, Microsoft Endpoint Manager, or Group Policy.</span></span> <span data-ttu-id="9aa5f-153">Voici quelques ressources pour vous aider :</span><span class="sxs-lookup"><span data-stu-id="9aa5f-153">Here are some resources to help:</span></span>
- [<span data-ttu-id="9aa5f-154">Working with Registry Keys</span><span class="sxs-lookup"><span data-stu-id="9aa5f-154">Working with Registry Keys</span></span>](/powershell/scripting/samples/working-with-registry-keys)
- [<span data-ttu-id="9aa5f-155">Configurer les paramètres client personnalisés pour Endpoint Protection</span><span class="sxs-lookup"><span data-stu-id="9aa5f-155">Configure custom client settings for Endpoint Protection</span></span>](/mem/configmgr/protect/deploy-use/endpoint-protection-configure-client)
- [<span data-ttu-id="9aa5f-156">Utiliser les paramètres de stratégie de groupe pour gérer les Endpoint Protection</span><span class="sxs-lookup"><span data-stu-id="9aa5f-156">Use Group Policy settings to manage Endpoint Protection</span></span>](/mem/configmgr/protect/deploy-use/endpoint-protection-group-policies)

## <a name="see-also"></a><span data-ttu-id="9aa5f-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aa5f-157">See also</span></span>

- [<span data-ttu-id="9aa5f-158">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="9aa5f-158">Network protection</span></span>](network-protection.md)
- [<span data-ttu-id="9aa5f-159">Évaluer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="9aa5f-159">Evaluate network protection</span></span>](evaluate-network-protection.md)
- [<span data-ttu-id="9aa5f-160">Activer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="9aa5f-160">Enable network protection</span></span>](enable-network-protection.md)
- [<span data-ttu-id="9aa5f-161">Corriger les faux positifs/négatifs dans Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9aa5f-161">Address false positives/negatives in Defender for Endpoint</span></span>](defender-endpoint-false-positives-negatives.md)
