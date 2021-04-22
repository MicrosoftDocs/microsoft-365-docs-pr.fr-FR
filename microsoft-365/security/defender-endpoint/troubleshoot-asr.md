---
title: Résoudre les problèmes liés aux règles de réduction de la surface d'attaque
description: Ressources et exemple de code pour résoudre les problèmes avec les règles de réduction de la surface d'attaque dans Microsoft Defender for Endpoint.
keywords: résoudre les problèmes, erreur, corriger, windows defender eg, asr, rules, hips, troubleshoot, audit, exclusion, false positive, broken, blocking, Microsoft Defender for Endpoint
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
audience: ITPro
author: denisebmsft
ms.author: deniseb
ms.date: 03/27/2019
ms.reviewer: ''
manager: dansimp
ms.custom: asr
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: 9ff00c706b0fb336c178e227b1cb33eff9e9ebbc
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935220"
---
# <a name="troubleshoot-attack-surface-reduction-rules"></a><span data-ttu-id="13401-104">Résoudre les problèmes de règles de réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="13401-104">Troubleshoot attack surface reduction rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="13401-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="13401-105">**Applies to:**</span></span>
- [<span data-ttu-id="13401-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="13401-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="13401-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="13401-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="13401-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="13401-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="13401-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="13401-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


<span data-ttu-id="13401-110">Lorsque vous utilisez des [règles de réduction de la surface](attack-surface-reduction.md) d'attaque, vous pouvez être face à des problèmes, tels que :</span><span class="sxs-lookup"><span data-stu-id="13401-110">When you use [attack surface reduction rules](attack-surface-reduction.md) you may run into issues, such as:</span></span>

- <span data-ttu-id="13401-111">Une règle bloque un fichier, un processus ou effectue une autre action qu'elle ne devrait pas (faux positif)</span><span class="sxs-lookup"><span data-stu-id="13401-111">A rule blocks a file, process, or performs some other action that it shouldn't (false positive)</span></span>

- <span data-ttu-id="13401-112">Une règle ne fonctionne pas comme décrit, ou ne bloque pas un fichier ou un processus qu'elle doit (faux négatifs)</span><span class="sxs-lookup"><span data-stu-id="13401-112">A rule doesn't work as described, or doesn't block a file or process that it should (false negative)</span></span>

<span data-ttu-id="13401-113">La résolution de ces problèmes se fait en quatre étapes :</span><span class="sxs-lookup"><span data-stu-id="13401-113">There are four steps to troubleshooting these problems:</span></span>

1. [<span data-ttu-id="13401-114">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="13401-114">Confirm prerequisites</span></span>](#confirm-prerequisites)

2. [<span data-ttu-id="13401-115">Utiliser le mode audit pour tester la règle</span><span class="sxs-lookup"><span data-stu-id="13401-115">Use audit mode to test the rule</span></span>](#use-audit-mode-to-test-the-rule)

3. <span data-ttu-id="13401-116">[Ajouter des exclusions pour la règle spécifiée](#add-exclusions-for-a-false-positive) (pour les faux positifs)</span><span class="sxs-lookup"><span data-stu-id="13401-116">[Add exclusions for the specified rule](#add-exclusions-for-a-false-positive) (for false positives)</span></span>

4. [<span data-ttu-id="13401-117">Envoyer les journaux de support</span><span class="sxs-lookup"><span data-stu-id="13401-117">Submit support logs</span></span>](#collect-diagnostic-data-for-file-submissions)

## <a name="confirm-prerequisites"></a><span data-ttu-id="13401-118">Confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="13401-118">Confirm prerequisites</span></span>

<span data-ttu-id="13401-119">Les règles de réduction de la surface d'attaque fonctionnent uniquement sur les appareils qui ont les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="13401-119">Attack surface reduction rules will only work on devices with the following conditions:</span></span>

- <span data-ttu-id="13401-120">Les points de terminaison exécutent Windows 10 Entreprise, version 1709 (également appelé Fall Creators Update).</span><span class="sxs-lookup"><span data-stu-id="13401-120">Endpoints are running Windows 10 Enterprise, version 1709 (also known as the Fall Creators Update).</span></span>

- <span data-ttu-id="13401-121">Les points de terminaison utilisent l'Antivirus Microsoft Defender comme seule application de protection antivirus.</span><span class="sxs-lookup"><span data-stu-id="13401-121">Endpoints are using Microsoft Defender Antivirus as the sole antivirus protection app.</span></span> <span data-ttu-id="13401-122">[L'utilisation d'une autre application antivirus entraîne la désactivation](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility)de Microsoft Defender AV.</span><span class="sxs-lookup"><span data-stu-id="13401-122">[Using any other antivirus app will cause Microsoft Defender AV to disable itself](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility).</span></span>

- <span data-ttu-id="13401-123">[La protection en temps réel](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus) est activée.</span><span class="sxs-lookup"><span data-stu-id="13401-123">[Real-time protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus) is enabled.</span></span>

- <span data-ttu-id="13401-124">Le mode audit n'est pas activé.</span><span class="sxs-lookup"><span data-stu-id="13401-124">Audit mode isn't enabled.</span></span> <span data-ttu-id="13401-125">Utilisez la stratégie de groupe pour définir la règle sur **Désactivé** (valeur : **0**) comme décrit dans Activer les règles de réduction [de la surface d'attaque.](enable-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="13401-125">Use Group Policy to set the rule to **Disabled** (value: **0**) as described in [Enable attack surface reduction rules](enable-attack-surface-reduction.md).</span></span>

<span data-ttu-id="13401-126">Si ces conditions préalables ont toutes été remplies, procédez à l'étape suivante pour tester la règle en mode audit.</span><span class="sxs-lookup"><span data-stu-id="13401-126">If these prerequisites have all been met, proceed to the next step to test the rule in audit mode.</span></span>

## <a name="use-audit-mode-to-test-the-rule"></a><span data-ttu-id="13401-127">Utiliser le mode audit pour tester la règle</span><span class="sxs-lookup"><span data-stu-id="13401-127">Use audit mode to test the rule</span></span>

<span data-ttu-id="13401-128">Vous pouvez consulter le site web de base de test Windows Defender à [l'adresse demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les règles de réduction de la surface d'attaque fonctionnent généralement pour les scénarios et processus pré-configurés sur un appareil, ou vous pouvez utiliser le mode audit, qui permet aux règles de signaler uniquement.</span><span class="sxs-lookup"><span data-stu-id="13401-128">You can visit the Windows Defender Test ground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm attack surface reduction rules are generally working for pre-configured scenarios and processes on a device, or you can use audit mode, which enables rules for reporting only.</span></span>

<span data-ttu-id="13401-129">Suivez ces instructions dans l'outil de démonstration pour voir comment fonctionnent les règles de réduction de [la surface](evaluate-attack-surface-reduction.md) d'attaque afin de tester la règle spécifique avec qui vous rencontrez des problèmes.</span><span class="sxs-lookup"><span data-stu-id="13401-129">Follow these instructions in [Use the demo tool to see how attack surface reduction rules work](evaluate-attack-surface-reduction.md) to test the specific rule you're encountering problems with.</span></span>

1. <span data-ttu-id="13401-130">Activez le mode audit pour la règle spécifique que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="13401-130">Enable audit mode for the specific rule you want to test.</span></span> <span data-ttu-id="13401-131">Utilisez la stratégie de groupe pour définir la règle sur **le mode Audit** (valeur : **2**), comme décrit dans activer les règles de réduction [de la surface d'attaque.](enable-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="13401-131">Use Group Policy to set the rule to **Audit mode** (value: **2**) as described in [Enable attack surface reduction rules](enable-attack-surface-reduction.md).</span></span> <span data-ttu-id="13401-132">Le mode audit permet à la règle de signaler le fichier ou le processus, tout en lui permettant de s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="13401-132">Audit mode allows the rule to report the file or process, but will still allow it to run.</span></span>

2. <span data-ttu-id="13401-133">Effectuez l'activité à l'origine d'un problème (par exemple, ouvrir ou exécuter le fichier ou le processus qui doit être bloqué mais qui est autorisé).</span><span class="sxs-lookup"><span data-stu-id="13401-133">Perform the activity that is causing an issue (for example, open or execute the file or process that should be blocked but is being allowed).</span></span>

3. <span data-ttu-id="13401-134">[Consultez les journaux](attack-surface-reduction.md) des événements de règle de réduction de la surface d'attaque pour voir si la règle aurait bloqué le fichier ou le processus si la règle avait été définie sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="13401-134">[Review the attack surface reduction rule event logs](attack-surface-reduction.md) to see if the rule would have blocked the file or process if the rule had been set to **Enabled**.</span></span>

<span data-ttu-id="13401-135">Si une règle ne bloque pas un fichier ou un processus que vous attendez qu'il bloque, vérifiez d'abord si le mode audit est activé.</span><span class="sxs-lookup"><span data-stu-id="13401-135">If a rule isn't blocking a file or process that you're expecting it should block, first check if audit mode is enabled.</span></span>

<span data-ttu-id="13401-136">Le mode audit a peut-être été activé pour tester une autre fonctionnalité, ou par un script PowerShell automatisé, et n'a peut-être pas été désactivé une fois les tests terminés.</span><span class="sxs-lookup"><span data-stu-id="13401-136">Audit mode may have been enabled for testing another feature, or by an automated PowerShell script, and may not have been disabled after the tests were completed.</span></span>

<span data-ttu-id="13401-137">Si vous avez testé la règle avec l'outil de démonstration et avec le mode audit, et que les règles de réduction de la surface d'attaque fonctionnent sur des scénarios pré-configurés, mais que la règle ne fonctionne pas comme prévu, vous devez passer à l'une des sections suivantes en fonction de votre situation :</span><span class="sxs-lookup"><span data-stu-id="13401-137">If you've tested the rule with the demo tool and with audit mode, and attack surface reduction rules are working on pre-configured scenarios, but the rule isn't working as expected, proceed to either of the following sections based on your situation:</span></span>

1. <span data-ttu-id="13401-138">Si la règle de réduction de la surface d'attaque bloque quelque chose qu'elle ne doit pas bloquer (également appelé faux positif), vous pouvez d'abord ajouter une exclusion de règle de réduction de la [surface d'attaque.](#add-exclusions-for-a-false-positive)</span><span class="sxs-lookup"><span data-stu-id="13401-138">If the attack surface reduction rule is blocking something that it shouldn't block (also known as a false positive), you can [first add an attack surface reduction rule exclusion](#add-exclusions-for-a-false-positive).</span></span>

2. <span data-ttu-id="13401-139">Si la règle de réduction de la surface d'attaque ne bloque pas quelque chose qu'elle doit bloquer (également appelé faux négatif), vous pouvez passer immédiatement à la dernière étape, en collectant des données de [diagnostic](#collect-diagnostic-data-for-file-submissions)et en nous envoyant le problème.</span><span class="sxs-lookup"><span data-stu-id="13401-139">If the attack surface reduction rule isn't blocking something that it should block (also known as a false negative), you can proceed immediately to the last step, [collecting diagnostic data and submitting the issue to us](#collect-diagnostic-data-for-file-submissions).</span></span>

## <a name="add-exclusions-for-a-false-positive"></a><span data-ttu-id="13401-140">Ajouter des exclusions pour un faux positif</span><span class="sxs-lookup"><span data-stu-id="13401-140">Add exclusions for a false positive</span></span>

<span data-ttu-id="13401-141">Si la règle de réduction de la surface d'attaque bloque quelque chose qu'elle ne doit pas bloquer (également appelé faux positif), vous pouvez ajouter des exclusions pour empêcher les règles de réduction de la surface d'attaque d'évaluer les fichiers ou dossiers exclus.</span><span class="sxs-lookup"><span data-stu-id="13401-141">If the attack surface reduction rule is blocking something that it shouldn't block (also known as a false positive), you can add exclusions to prevent attack surface reduction rules from evaluating the excluded files or folders.</span></span>

<span data-ttu-id="13401-142">Pour ajouter une exclusion, voir [Personnaliser la réduction de la surface d'attaque.](customize-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="13401-142">To add an exclusion, see [Customize Attack surface reduction](customize-attack-surface-reduction.md).</span></span>

>[!IMPORTANT]
><span data-ttu-id="13401-143">Vous pouvez spécifier des fichiers et dossiers individuels à exclure, mais vous ne pouvez pas spécifier des règles individuelles.</span><span class="sxs-lookup"><span data-stu-id="13401-143">You can specify individual files and folders to be excluded, but you cannot specify individual rules.</span></span>
><span data-ttu-id="13401-144">Cela signifie que tous les fichiers ou dossiers exclus seront exclus de toutes les règles de la asr.</span><span class="sxs-lookup"><span data-stu-id="13401-144">This means any files or folders that are excluded will be excluded from all ASR rules.</span></span>

## <a name="report-a-false-positive-or-false-negative"></a><span data-ttu-id="13401-145">Signaler un faux positif ou un faux négatif</span><span class="sxs-lookup"><span data-stu-id="13401-145">Report a false positive or false negative</span></span>

<span data-ttu-id="13401-146">Utilisez le Windows Defender d'envoi [web Security Intelligence](https://www.microsoft.com/wdsi/filesubmission) pour signaler un faux négatif ou un faux positif pour la protection du réseau.</span><span class="sxs-lookup"><span data-stu-id="13401-146">Use the [Windows Defender Security Intelligence web-based submission form](https://www.microsoft.com/wdsi/filesubmission) to report a false negative or false positive for network protection.</span></span> <span data-ttu-id="13401-147">Avec un abonnement Windows E5, vous pouvez également fournir un lien vers [n'importe quelle alerte associée.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="13401-147">With a Windows E5 subscription, you can also [provide a link to any associated alert](alerts-queue.md).</span></span>

## <a name="collect-diagnostic-data-for-file-submissions"></a><span data-ttu-id="13401-148">Collecter des données de diagnostic pour les soumissions de fichiers</span><span class="sxs-lookup"><span data-stu-id="13401-148">Collect diagnostic data for file submissions</span></span>

<span data-ttu-id="13401-149">Lorsque vous signalez un problème avec les règles de réduction de la surface d'attaque, vous êtes invité à collecter et soumettre des données de diagnostic qui peuvent être utilisées par le support microsoft et les équipes d'ingénierie pour vous aider à résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="13401-149">When you report a problem with attack surface reduction rules, you're asked to collect and submit diagnostic data that can be used by Microsoft support and engineering teams to help troubleshoot issues.</span></span>

1. <span data-ttu-id="13401-150">Ouvrez une invite de commandes avec élévation de élévation de Windows Defender répertoire :</span><span class="sxs-lookup"><span data-stu-id="13401-150">Open an elevated command prompt and change to the Windows Defender directory:</span></span>

   ```console
   cd "c:\program files\windows defender"
   ```

2. <span data-ttu-id="13401-151">Exécutez cette commande pour générer les journaux de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="13401-151">Run this command to generate the diagnostic logs:</span></span>

   ```console
   mpcmdrun -getfiles
   ```

3. <span data-ttu-id="13401-152">Par défaut, ils sont enregistrés dans `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab` .</span><span class="sxs-lookup"><span data-stu-id="13401-152">By default, they're saved to `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab`.</span></span> <span data-ttu-id="13401-153">Joignez le fichier au formulaire d'envoi.</span><span class="sxs-lookup"><span data-stu-id="13401-153">Attach the file to the submission form.</span></span>

## <a name="related-articles"></a><span data-ttu-id="13401-154">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="13401-154">Related articles</span></span>

- [<span data-ttu-id="13401-155">Règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="13401-155">Attack surface reduction rules</span></span>](attack-surface-reduction.md)

- [<span data-ttu-id="13401-156">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="13401-156">Enable attack surface reduction rules</span></span>](enable-attack-surface-reduction.md)

- [<span data-ttu-id="13401-157">Évaluer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="13401-157">Evaluate attack surface reduction rules</span></span>](evaluate-attack-surface-reduction.md)
