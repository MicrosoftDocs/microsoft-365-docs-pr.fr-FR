---
title: Résoudre les problèmes liés à la protection du réseau
description: Ressources et exemple de code pour résoudre les problèmes avec la protection réseau dans Microsoft Defender for Endpoint.
keywords: résoudre les problèmes, erreur, corriger, windows defender eg, asr, rules, hips, troubleshoot, audit, exclusion, false positive, broken, blocking, microsoft defender for endpoint, microsoft defender advanced threat protection
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
author: dansimp
ms.author: dansimp
ms.date: 01/26/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 34bebddcf052a643529f1d2b8a8a869a0ffe4a91
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51183817"
---
# <a name="troubleshoot-network-protection"></a><span data-ttu-id="a7bb8-104">Résoudre les problèmes de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="a7bb8-104">Troubleshoot network protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="a7bb8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a7bb8-105">**Applies to:**</span></span>
- [<span data-ttu-id="a7bb8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a7bb8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="a7bb8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a7bb8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="a7bb8-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="a7bb8-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="a7bb8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


<span data-ttu-id="a7bb8-110">Lorsque vous utilisez [la protection réseau,](network-protection.md) vous pouvez rencontrer des problèmes, tels que :</span><span class="sxs-lookup"><span data-stu-id="a7bb8-110">When you use [Network protection](network-protection.md) you may encounter issues, such as:</span></span>

- <span data-ttu-id="a7bb8-111">La protection du réseau bloque un site web sécurisé (faux positif)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-111">Network protection blocks a website that is safe (false positive)</span></span>
- <span data-ttu-id="a7bb8-112">La protection du réseau ne parvient pas à bloquer un site web malveillant suspect ou connu (faux négatif)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-112">Network protection fails to block a suspicious or known malicious website (false negative)</span></span>

<span data-ttu-id="a7bb8-113">La résolution de ces problèmes se fait en quatre étapes :</span><span class="sxs-lookup"><span data-stu-id="a7bb8-113">There are four steps to troubleshooting these problems:</span></span>

1. <span data-ttu-id="a7bb8-114">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="a7bb8-114">Confirm prerequisites</span></span>
2. <span data-ttu-id="a7bb8-115">Utiliser le mode audit pour tester la règle</span><span class="sxs-lookup"><span data-stu-id="a7bb8-115">Use audit mode to test the rule</span></span>
3. <span data-ttu-id="a7bb8-116">Ajouter des exclusions pour la règle spécifiée (pour les faux positifs)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-116">Add exclusions for the specified rule (for false positives)</span></span>
4. <span data-ttu-id="a7bb8-117">Envoyer les journaux de support</span><span class="sxs-lookup"><span data-stu-id="a7bb8-117">Submit support logs</span></span>

## <a name="confirm-prerequisites"></a><span data-ttu-id="a7bb8-118">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="a7bb8-118">Confirm prerequisites</span></span>

<span data-ttu-id="a7bb8-119">La protection réseau ne fonctionne que sur les appareils qui ont les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7bb8-119">Network protection will only work on devices with the following conditions:</span></span>

>[!div class="checklist"]
> - <span data-ttu-id="a7bb8-120">Les points de terminaison exécutent Windows 10 Professionnel ou Entreprise, version 1709 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-120">Endpoints are running Windows 10 Pro or Enterprise edition, version 1709 or higher.</span></span>
> - <span data-ttu-id="a7bb8-121">Les points de terminaison utilisent l’Antivirus Microsoft Defender comme seule application de protection antivirus.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-121">Endpoints are using Microsoft Defender Antivirus as the sole antivirus protection app.</span></span> <span data-ttu-id="a7bb8-122">[Découvrez ce qui se produit lorsque vous utilisez une solution antivirus non-Microsoft.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-122">[See what happens when you are using a non-Microsoft antivirus solution](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility).</span></span>
> - <span data-ttu-id="a7bb8-123">[La protection en temps réel](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus) est activée.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-123">[Real-time protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus) is enabled.</span></span>
> - <span data-ttu-id="a7bb8-124">[La protection cloud](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) est activée.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-124">[Cloud-delivered protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) is enabled.</span></span>
> - <span data-ttu-id="a7bb8-125">Le mode audit n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-125">Audit mode is not enabled.</span></span> <span data-ttu-id="a7bb8-126">Utilisez [la stratégie de](enable-network-protection.md#group-policy) groupe pour définir la règle sur **Désactivé** (valeur : **0**).</span><span class="sxs-lookup"><span data-stu-id="a7bb8-126">Use [Group Policy](enable-network-protection.md#group-policy) to set the rule to **Disabled** (value: **0**).</span></span>

## <a name="use-audit-mode"></a><span data-ttu-id="a7bb8-127">Utiliser le mode audit</span><span class="sxs-lookup"><span data-stu-id="a7bb8-127">Use audit mode</span></span>

<span data-ttu-id="a7bb8-128">Vous pouvez activer la protection réseau en mode audit, puis visiter un site web que nous avons créé pour faire une démonstration de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-128">You can enable network protection in audit mode and then visit a website that we've created to demo the feature.</span></span> <span data-ttu-id="a7bb8-129">Toutes les connexions de site web sont autorisées par la protection réseau, mais un événement est enregistré pour indiquer toute connexion qui aurait été bloquée si la protection du réseau était activée.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-129">All website connections will be allowed by network protection but an event will be logged to indicate any connection that would have been blocked if network protection was enabled.</span></span>

1. <span data-ttu-id="a7bb8-130">Définissez la protection réseau sur **le mode Audit.**</span><span class="sxs-lookup"><span data-stu-id="a7bb8-130">Set network protection to **Audit mode**.</span></span>

   ```PowerShell
   Set-MpPreference -EnableNetworkProtection AuditMode
   ```

2. <span data-ttu-id="a7bb8-131">Effectuez l’activité de connexion à l’origine d’un problème (par exemple, essayez de visiter le site ou de vous connecter à l’adresse IP que vous bloquez ou ne voulez pas bloquer).</span><span class="sxs-lookup"><span data-stu-id="a7bb8-131">Perform the connection activity that is causing an issue (for example, attempt to visit the site, or connect to the IP address you do or don't want to block).</span></span>

3. <span data-ttu-id="a7bb8-132">[Consultez les journaux des événements](network-protection.md#review-network-protection-events-in-windows-event-viewer) de protection réseau pour voir si la fonctionnalité aurait bloqué la connexion si elle avait été définie **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="a7bb8-132">[Review the network protection event logs](network-protection.md#review-network-protection-events-in-windows-event-viewer) to see if the feature would have blocked the connection if it had been set to **Enabled**.</span></span>
   
   <span data-ttu-id="a7bb8-133">Si la protection du réseau ne bloque pas une connexion que vous attendez qu’elle bloque, activez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-133">If network protection is not blocking a connection that you are expecting it should block, enable the feature.</span></span>

   ```PowerShell
   Set-MpPreference -EnableNetworkProtection Enabled
   ```

## <a name="report-a-false-positive-or-false-negative"></a><span data-ttu-id="a7bb8-134">Signaler un faux positif ou un faux négatif</span><span class="sxs-lookup"><span data-stu-id="a7bb8-134">Report a false positive or false negative</span></span>

<span data-ttu-id="a7bb8-135">Si vous avez testé la fonctionnalité avec le site de démonstration et le mode audit, et que la protection du réseau fonctionne sur des scénarios pré-configurés, mais ne fonctionne pas comme prévu pour une connexion spécifique, utilisez le formulaire d’envoi [web Windows Defender Security Intelligence](https://www.microsoft.com/wdsi/filesubmission) pour signaler un faux négatif ou un faux positif pour la protection du réseau.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-135">If you've tested the feature with the demo site and with audit mode, and network protection is working on pre-configured scenarios, but is not working as expected for a specific connection, use the [Windows Defender Security Intelligence web-based submission form](https://www.microsoft.com/wdsi/filesubmission) to report a false negative or false positive for network protection.</span></span> <span data-ttu-id="a7bb8-136">Avec un abonnement E5, vous pouvez également fournir un [lien vers n’importe quelle alerte associée.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-136">With an E5 subscription, you can also [provide a link to any associated alert](alerts-queue.md).</span></span>

<span data-ttu-id="a7bb8-137">Voir [Adresse faux positifs/négatifs dans Microsoft Defender pour le point de terminaison.](defender-endpoint-false-positives-negatives.md)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-137">See [Address false positives/negatives in Microsoft Defender for Endpoint](defender-endpoint-false-positives-negatives.md).</span></span>

## <a name="exclude-website-from-network-protection-scope"></a><span data-ttu-id="a7bb8-138">Exclure le site web de l’étendue de protection réseau</span><span class="sxs-lookup"><span data-stu-id="a7bb8-138">Exclude website from network protection scope</span></span>

<span data-ttu-id="a7bb8-139">Pour autoriser le site web bloqué (faux positif), ajoutez son URL à la [liste des sites de confiance.](https://blogs.msdn.microsoft.com/asiatech/2014/08/19/how-to-add-web-sites-to-trusted-sites-via-gpo-from-dc-installed-ie10-or-higher-ie-version/)</span><span class="sxs-lookup"><span data-stu-id="a7bb8-139">To allow the website that is being blocked (false positive), add its URL to the [list of trusted sites](https://blogs.msdn.microsoft.com/asiatech/2014/08/19/how-to-add-web-sites-to-trusted-sites-via-gpo-from-dc-installed-ie10-or-higher-ie-version/).</span></span> <span data-ttu-id="a7bb8-140">Les ressources Web de cette liste contournent la vérification de la protection réseau.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-140">Web resources from this list bypass the network protection check.</span></span>

## <a name="collect-diagnostic-data-for-file-submissions"></a><span data-ttu-id="a7bb8-141">Collecter des données de diagnostic pour les soumissions de fichiers</span><span class="sxs-lookup"><span data-stu-id="a7bb8-141">Collect diagnostic data for file submissions</span></span>

<span data-ttu-id="a7bb8-142">Lorsque vous signalez un problème avec la protection du réseau, vous êtes invité à collecter et à envoyer des données de diagnostic qui peuvent être utilisées par le support microsoft et les équipes d’ingénierie pour vous aider à résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-142">When you report a problem with network protection, you are asked to collect and submit diagnostic data that can be used by Microsoft support and engineering teams to help troubleshoot issues.</span></span>

1. <span data-ttu-id="a7bb8-143">Ouvrez une invite de commandes avec élévation de élévation de Windows Defender répertoire :</span><span class="sxs-lookup"><span data-stu-id="a7bb8-143">Open an elevated command prompt and change to the Windows Defender directory:</span></span>

   ```console
   cd c:\program files\windows defender
   ```

2. <span data-ttu-id="a7bb8-144">Exécutez cette commande pour générer les journaux de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="a7bb8-144">Run this command to generate the diagnostic logs:</span></span>

   ```console
   mpcmdrun -getfiles
   ```

3. <span data-ttu-id="a7bb8-145">Par défaut, ils sont enregistrés dans C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-145">By default, they are saved to C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab.</span></span> <span data-ttu-id="a7bb8-146">Joignez le fichier au formulaire d’envoi.</span><span class="sxs-lookup"><span data-stu-id="a7bb8-146">Attach the file to the submission form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7bb8-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7bb8-147">Related topics</span></span>

- [<span data-ttu-id="a7bb8-148">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="a7bb8-148">Network protection</span></span>](network-protection.md)
- [<span data-ttu-id="a7bb8-149">Évaluer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="a7bb8-149">Evaluate network protection</span></span>](evaluate-network-protection.md)
- [<span data-ttu-id="a7bb8-150">Activer la protection réseau</span><span class="sxs-lookup"><span data-stu-id="a7bb8-150">Enable network protection</span></span>](enable-network-protection.md)
- [<span data-ttu-id="a7bb8-151">Corriger les faux positifs/négatifs dans Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a7bb8-151">Address false positives/negatives in Defender for Endpoint</span></span>](defender-endpoint-false-positives-negatives.md)
