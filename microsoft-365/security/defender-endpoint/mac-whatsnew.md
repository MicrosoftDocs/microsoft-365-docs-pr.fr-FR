---
title: Nouveautés de Microsoft Defender pour Endpoint pour Mac
description: Découvrez les principales modifications apportées aux versions précédentes de Microsoft Defender pour Endpoint pour Mac.
keywords: microsoft, defender, atp, mac, installation, macos, whatsnew
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
ms.technology: mde
ms.openlocfilehash: be906baca3a54183e22fa3b4ee424a9d8fc6957a
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51198692"
---
# <a name="whats-new-in-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="2c459-104">Nouveautés de Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="2c459-104">What's new in Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2c459-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2c459-105">**Applies to:**</span></span>
- [<span data-ttu-id="2c459-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2c459-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2c459-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2c459-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="2c459-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2c459-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2c459-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2c459-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

> [!IMPORTANT]
> <span data-ttu-id="2c459-110">Sur macOS 11 (Big Sur), Microsoft Defender for Endpoint nécessite des profils de configuration supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2c459-110">On macOS 11 (Big Sur), Microsoft Defender for Endpoint requires additional configuration profiles.</span></span> <span data-ttu-id="2c459-111">Si vous êtes un client existant en cours de mise à niveau à partir de versions antérieures de macOS, veillez à déployer les profils de configuration supplémentaires répertoriés sur [cette page.](mac-sysext-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2c459-111">If you are an existing customer upgrading from earlier versions of macOS, make sure to deploy the additional configuration profiles listed on [this page](mac-sysext-policies.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c459-112">La prise en charge de macOS 10.13 (High Sierra) ne sera plus prise en charge le 15 février 2021.</span><span class="sxs-lookup"><span data-stu-id="2c459-112">Support for macOS 10.13 (High Sierra) will be discontinued on February 15th, 2021.</span></span>

## <a name="1012279-20121012122790"></a><span data-ttu-id="2c459-113">101.22.79 (20.121012.12279.0)</span><span class="sxs-lookup"><span data-stu-id="2c459-113">101.22.79 (20.121012.12279.0)</span></span>

- <span data-ttu-id="2c459-114">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-114">Performance improvements & bug fixes</span></span>

## <a name="1011988-20121011119880"></a><span data-ttu-id="2c459-115">101.19.88 (20.121011.11988.0)</span><span class="sxs-lookup"><span data-stu-id="2c459-115">101.19.88 (20.121011.11988.0)</span></span>

- <span data-ttu-id="2c459-116">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-116">Performance improvements & bug fixes</span></span>

## <a name="1011948-20120121119480"></a><span data-ttu-id="2c459-117">101.19.48 (20.120121.11948.0)</span><span class="sxs-lookup"><span data-stu-id="2c459-117">101.19.48 (20.120121.11948.0)</span></span>

> [!NOTE]
> <span data-ttu-id="2c459-118">L’ancienne syntaxe de l’outil de ligne de commande a été dépréciée avec cette version.</span><span class="sxs-lookup"><span data-stu-id="2c459-118">The old command-line tool syntax has been deprecated with this release.</span></span> <span data-ttu-id="2c459-119">Pour plus d’informations sur la nouvelle syntaxe, voir [Resources](mac-resources.md#configuring-from-the-command-line).</span><span class="sxs-lookup"><span data-stu-id="2c459-119">For information on the new syntax, see [Resources](mac-resources.md#configuring-from-the-command-line).</span></span>

- <span data-ttu-id="2c459-120">Ajout d’un nouveau commutateur de ligne de commande pour désactiver l’extension réseau : `mdatp system-extension network-filter disable` .</span><span class="sxs-lookup"><span data-stu-id="2c459-120">Added a new command-line switch to disable the network extension: `mdatp system-extension network-filter disable`.</span></span> <span data-ttu-id="2c459-121">Cette commande peut être utile pour résoudre les problèmes réseau qui peuvent être liés à Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="2c459-121">This command can be useful to troubleshoot networking issues that could be related to Microsoft Defender for Endpoint for Mac</span></span>
- <span data-ttu-id="2c459-122">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-122">Performance improvements & bug fixes</span></span>

## <a name="1011921-20120101119210"></a><span data-ttu-id="2c459-123">101.19.21 (20.120101.11921.0)</span><span class="sxs-lookup"><span data-stu-id="2c459-123">101.19.21 (20.120101.11921.0)</span></span>

- <span data-ttu-id="2c459-124">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-124">Bug fixes</span></span>

## <a name="1011526-20120102115260"></a><span data-ttu-id="2c459-125">101.15.26 (20.120102.11526.0)</span><span class="sxs-lookup"><span data-stu-id="2c459-125">101.15.26 (20.120102.11526.0)</span></span>

- <span data-ttu-id="2c459-126">Amélioration de la fiabilité de l’agent lors de l’exécution sur macOS 11 Big Sur</span><span class="sxs-lookup"><span data-stu-id="2c459-126">Improved the reliability of the agent when running on macOS 11 Big Sur</span></span>
- <span data-ttu-id="2c459-127">Ajout d’un nouveau commutateur de ligne de commande ( ) pour ignorer les exclusions antivirus lors des `--ignore-exclusions` analyses personnalisées ( `mdatp scan custom` )</span><span class="sxs-lookup"><span data-stu-id="2c459-127">Added a new command-line switch (`--ignore-exclusions`) to ignore AV exclusions during custom scans (`mdatp scan custom`)</span></span>
- <span data-ttu-id="2c459-128">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-128">Performance improvements & bug fixes</span></span>

## <a name="1011375-20120101113750"></a><span data-ttu-id="2c459-129">101.13.75 (20.120101.11375.0)</span><span class="sxs-lookup"><span data-stu-id="2c459-129">101.13.75 (20.120101.11375.0)</span></span>

- <span data-ttu-id="2c459-130">Conditions supprimées lorsque Microsoft Defender pour le point de terminaison déclenchant un bogue macOS 11 (Big Sur) qui se manifeste en noyau</span><span class="sxs-lookup"><span data-stu-id="2c459-130">Removed conditions when Microsoft Defender for Endpoint was triggering a macOS 11 (Big Sur) bug that manifests into a kernel panic</span></span>
- <span data-ttu-id="2c459-131">Correction d’une fuite de mémoire dans l’extension du système de sécurité des points de terminaison lors de l’exécution sur mac 11 (Big Sur)</span><span class="sxs-lookup"><span data-stu-id="2c459-131">Fixed a memory leak in the Endpoint Security system extension when running on mac 11 (Big Sur)</span></span>
- <span data-ttu-id="2c459-132">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-132">Bug fixes</span></span>

## <a name="1011072"></a><span data-ttu-id="2c459-133">101.10.72</span><span class="sxs-lookup"><span data-stu-id="2c459-133">101.10.72</span></span>

- <span data-ttu-id="2c459-134">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-134">Bug fixes</span></span>

## <a name="1010961"></a><span data-ttu-id="2c459-135">101.09.61</span><span class="sxs-lookup"><span data-stu-id="2c459-135">101.09.61</span></span>

- <span data-ttu-id="2c459-136">Ajout d’une nouvelle préférence gérée pour [désactiver l’option d’envoi de commentaires](mac-preferences.md#show--hide-option-to-send-feedback)</span><span class="sxs-lookup"><span data-stu-id="2c459-136">Added a new managed preference for [disabling the option to send feedback](mac-preferences.md#show--hide-option-to-send-feedback)</span></span>
- <span data-ttu-id="2c459-137">L’icône du menu État affiche désormais un état sain lorsque les paramètres du produit sont gérés.</span><span class="sxs-lookup"><span data-stu-id="2c459-137">Status menu icon now shows a healthy state when the product settings are managed.</span></span> <span data-ttu-id="2c459-138">Auparavant, l’icône du menu d’état affichait un état d’avertissement ou d’erreur, même si les paramètres du produit étaient gérés par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2c459-138">Previously, the status menu icon was displaying a warning or error state, even though the product settings were managed by the administrator</span></span>
- <span data-ttu-id="2c459-139">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-139">Performance improvements & bug fixes</span></span>

## <a name="1010950"></a><span data-ttu-id="2c459-140">101.09.50</span><span class="sxs-lookup"><span data-stu-id="2c459-140">101.09.50</span></span>

- <span data-ttu-id="2c459-141">Cette version du produit a été validée sur macOS Big Sur 11 bêta 9</span><span class="sxs-lookup"><span data-stu-id="2c459-141">This product version has been validated on macOS Big Sur 11 beta 9</span></span>

- <span data-ttu-id="2c459-142">La nouvelle syntaxe de `mdatp` l’outil en ligne de commande est désormais la syntaxe par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c459-142">The new syntax for the `mdatp` command-line tool is now the default one.</span></span> <span data-ttu-id="2c459-143">Pour plus d’informations sur la nouvelle syntaxe, voir [Resources for Microsoft Defender for Endpoint for Mac](mac-resources.md#configuring-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="2c459-143">For more information on the new syntax, see [Resources for Microsoft Defender for Endpoint for Mac](mac-resources.md#configuring-from-the-command-line)</span></span>

  > [!NOTE]
  > <span data-ttu-id="2c459-144">L’ancienne syntaxe de l’outil de ligne de commande sera supprimée du produit le **1er janvier 2021.**</span><span class="sxs-lookup"><span data-stu-id="2c459-144">The old command-line tool syntax will be removed from the product on **January 1st, 2021**.</span></span>

- <span data-ttu-id="2c459-145">Étendu avec un nouveau paramètre ( ) qui permet d’enregistrer les journaux de diagnostic dans `mdatp diagnostic create` `--path [directory]` un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="2c459-145">Extended `mdatp diagnostic create` with a new parameter (`--path [directory]`) that allows the diagnostic logs to be saved to a different directory</span></span>
- <span data-ttu-id="2c459-146">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-146">Performance improvements & bug fixes</span></span>

## <a name="1010949"></a><span data-ttu-id="2c459-147">101.09.49</span><span class="sxs-lookup"><span data-stu-id="2c459-147">101.09.49</span></span>

- <span data-ttu-id="2c459-148">Améliorations apportées à l’interface utilisateur pour différencier les exclusions gérées par l’administrateur informatique des exclusions définies par l’utilisateur local</span><span class="sxs-lookup"><span data-stu-id="2c459-148">User interface improvements to differentiate exclusions that are managed by the IT administrator versus exclusions defined by the local user</span></span>
- <span data-ttu-id="2c459-149">Amélioration de l’utilisation du processeur lors des analyses à la demande</span><span class="sxs-lookup"><span data-stu-id="2c459-149">Improved CPU utilization during on-demand scans</span></span>
- <span data-ttu-id="2c459-150">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-150">Performance improvements & bug fixes</span></span>

## <a name="1010723"></a><span data-ttu-id="2c459-151">101.07.23</span><span class="sxs-lookup"><span data-stu-id="2c459-151">101.07.23</span></span>

- <span data-ttu-id="2c459-152">Ajout de nouveaux champs à la sortie de la vérification de l’état du mode passif et de l’ID de groupe `mdatp --health` EDR</span><span class="sxs-lookup"><span data-stu-id="2c459-152">Added new fields to the output of `mdatp --health` for checking the status of passive mode and the EDR group ID</span></span>

  > [!NOTE]
  > <span data-ttu-id="2c459-153">`mdatp --health` sera remplacé par `mdatp health` dans une prochaine mise à jour du produit.</span><span class="sxs-lookup"><span data-stu-id="2c459-153">`mdatp --health` will be replaced with `mdatp health` in a future product update.</span></span>

- <span data-ttu-id="2c459-154">Correction d’un bogue dans lequel l’envoi automatique d’échantillons n’a pas été marqué comme géré dans l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="2c459-154">Fixed a bug where automatic sample submission was not marked as managed in the user interface</span></span>
- <span data-ttu-id="2c459-155">Ajout de nouveaux paramètres pour contrôler la rétention des éléments dans l’historique d’analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="2c459-155">Added new settings for controlling the retention of items in the antivirus scan history.</span></span> <span data-ttu-id="2c459-156">Vous pouvez désormais [spécifier le nombre](mac-preferences.md#antivirus-scan-history-retention-in-days) de jours de rétention des éléments dans l’historique d’analyse et spécifier le nombre maximal d’éléments [dans l’historique d’analyse.](mac-preferences.md#maximum-number-of-items-in-the-antivirus-scan-history)</span><span class="sxs-lookup"><span data-stu-id="2c459-156">You can now [specify the number of days to retain items in the scan history](mac-preferences.md#antivirus-scan-history-retention-in-days) and [specify the maximum number of items in the scan history](mac-preferences.md#maximum-number-of-items-in-the-antivirus-scan-history)</span></span>
- <span data-ttu-id="2c459-157">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-157">Bug fixes</span></span>

## <a name="1010663"></a><span data-ttu-id="2c459-158">101.06.63</span><span class="sxs-lookup"><span data-stu-id="2c459-158">101.06.63</span></span>

- <span data-ttu-id="2c459-159">Nous avons résolu une régression des performances introduite dans la version `101.05.17` .</span><span class="sxs-lookup"><span data-stu-id="2c459-159">Addressed a performance regression introduced in version `101.05.17`.</span></span> <span data-ttu-id="2c459-160">La régression a été introduite avec le correctif pour éliminer les noyaux observés par certains clients lors de l’accès aux partages SMB.</span><span class="sxs-lookup"><span data-stu-id="2c459-160">The regression was introduced with the fix to eliminate the kernel panics some customers have observed when accessing SMB shares.</span></span> <span data-ttu-id="2c459-161">Nous avons revenir à ce changement de code et nous sommes en train d’examiner d’autres façons d’éliminer les noyaux.</span><span class="sxs-lookup"><span data-stu-id="2c459-161">We have reverted this code change and are investigating alternative ways to eliminate the kernel panics.</span></span>

## <a name="1010517"></a><span data-ttu-id="2c459-162">101.05.17</span><span class="sxs-lookup"><span data-stu-id="2c459-162">101.05.17</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c459-163">Nous travaillons sur une syntaxe nouvelle et améliorée pour `mdatp` l’outil en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2c459-163">We are working on a new and enhanced syntax for the `mdatp` command-line tool.</span></span> <span data-ttu-id="2c459-164">La nouvelle syntaxe est actuellement la valeur par défaut dans les canaux de mise à jour Insider Fast et Insider Slow.</span><span class="sxs-lookup"><span data-stu-id="2c459-164">The new syntax is currently the default in the Insider Fast and Insider Slow update channels.</span></span> <span data-ttu-id="2c459-165">Nous vous encourageons à vous familiariser avec cette nouvelle syntaxe.</span><span class="sxs-lookup"><span data-stu-id="2c459-165">We encourage you to famliliarize yourself with this new syntax.</span></span>
> 
> <span data-ttu-id="2c459-166">Nous continuerons à la prise en charge de l’ancienne syntaxe parallèlement à la nouvelle syntaxe et nous fournirons une meilleure communication autour du plan de désaprétation de l’ancienne syntaxe dans les mois à venir.</span><span class="sxs-lookup"><span data-stu-id="2c459-166">We will continue supporting the old syntax in parallel with the new syntax and will provide more communication around the deprecation plan for the old syntax in the upcoming months.</span></span>

- <span data-ttu-id="2c459-167">Nous avons résolu un problème de noyau qui se produisait parfois lors de l’accès aux partages de fichiers SMB</span><span class="sxs-lookup"><span data-stu-id="2c459-167">Addressed a kernel panic that occurred sometimes when accessing SMB file shares</span></span>
- <span data-ttu-id="2c459-168">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-168">Performance improvements & bug fixes</span></span>

## <a name="1010516"></a><span data-ttu-id="2c459-169">101.05.16</span><span class="sxs-lookup"><span data-stu-id="2c459-169">101.05.16</span></span>

- <span data-ttu-id="2c459-170">Améliorations apportées à la logique d’analyse rapide pour réduire considérablement le nombre de fichiers analysés</span><span class="sxs-lookup"><span data-stu-id="2c459-170">Improvements to quick scan logic to significantly reduce the number of scanned files</span></span>
- <span data-ttu-id="2c459-171">Ajout de la prise en charge [de lacompletion](mac-resources.md#how-to-enable-autocompletion) automatique pour l’outil en ligne de commande</span><span class="sxs-lookup"><span data-stu-id="2c459-171">Added [autocompletion support](mac-resources.md#how-to-enable-autocompletion) for the command-line tool</span></span>
- <span data-ttu-id="2c459-172">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-172">Bug fixes</span></span>

## <a name="1010312"></a><span data-ttu-id="2c459-173">101.03.12</span><span class="sxs-lookup"><span data-stu-id="2c459-173">101.03.12</span></span>

- <span data-ttu-id="2c459-174">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-174">Performance improvements & bug fixes</span></span>

## <a name="1010154"></a><span data-ttu-id="2c459-175">101.01.54</span><span class="sxs-lookup"><span data-stu-id="2c459-175">101.01.54</span></span>

- <span data-ttu-id="2c459-176">Améliorations en matière de compatibilité avec Time Machine</span><span class="sxs-lookup"><span data-stu-id="2c459-176">Improvements around compatibility with Time Machine</span></span>
- <span data-ttu-id="2c459-177">Améliorations en matière d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="2c459-177">Accessibility improvements</span></span>
- <span data-ttu-id="2c459-178">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-178">Performance improvements & bug fixes</span></span>

## <a name="1010031"></a><span data-ttu-id="2c459-179">101.00.31</span><span class="sxs-lookup"><span data-stu-id="2c459-179">101.00.31</span></span>

- <span data-ttu-id="2c459-180">Amélioration de [l’expérience d’intégration de produit pour les utilisateurs d’Intune](https://docs.microsoft.com/mem/intune/apps/apps-advanced-threat-protection-macos)</span><span class="sxs-lookup"><span data-stu-id="2c459-180">Improved [product onboarding experience for Intune users](https://docs.microsoft.com/mem/intune/apps/apps-advanced-threat-protection-macos)</span></span>
- <span data-ttu-id="2c459-181">Les [exclusions antivirus désormais prise en charge les caractères génériques](mac-exclusions.md#supported-exclusion-types)</span><span class="sxs-lookup"><span data-stu-id="2c459-181">Antivirus [exclusions now support wildcards](mac-exclusions.md#supported-exclusion-types)</span></span>
- <span data-ttu-id="2c459-182">Ajout de la possibilité de déclencher des analyses antivirus à partir du menu contextuel macOS.</span><span class="sxs-lookup"><span data-stu-id="2c459-182">Added the ability to trigger antivirus scans from the macOS contextual menu.</span></span> <span data-ttu-id="2c459-183">Vous pouvez maintenant cliquer avec le bouton droit sur un fichier ou un dossier dans finder et sélectionner Analyser **avec Microsoft Defender pour le point de terminaison**</span><span class="sxs-lookup"><span data-stu-id="2c459-183">You can now right-click a file or a folder in Finder and select **Scan with Microsoft Defender for Endpoint**</span></span>
- <span data-ttu-id="2c459-184">Les rétrogradations de produits sur place sont désormais explicitement interdits par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="2c459-184">In-place product downgrades are now explicitly disallowed by the installer.</span></span> <span data-ttu-id="2c459-185">Si vous devez rétrograder, désinstallez d’abord la version existante et reconfigurez votre appareil.</span><span class="sxs-lookup"><span data-stu-id="2c459-185">If you need to downgrade, first uninstall the existing version and reconfigure your device</span></span>
- <span data-ttu-id="2c459-186">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-186">Other performance improvements & bug fixes</span></span>

## <a name="1009027"></a><span data-ttu-id="2c459-187">100.90.27</span><span class="sxs-lookup"><span data-stu-id="2c459-187">100.90.27</span></span>

- <span data-ttu-id="2c459-188">Vous pouvez désormais [définir un canal](mac-updates.md#set-the-channel-name) de mise à jour pour Microsoft Defender pour Point de terminaison pour Mac différent du canal de mise à jour à l’échelle du système</span><span class="sxs-lookup"><span data-stu-id="2c459-188">You can now [set an update channel](mac-updates.md#set-the-channel-name) for Microsoft Defender for Endpoint for Mac that is different from the system-wide update channel</span></span>
- <span data-ttu-id="2c459-189">Icône Nouveau produit</span><span class="sxs-lookup"><span data-stu-id="2c459-189">New product icon</span></span>
- <span data-ttu-id="2c459-190">Autres améliorations de l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="2c459-190">Other user experience improvements</span></span>
- <span data-ttu-id="2c459-191">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-191">Bug fixes</span></span>

## <a name="1008692"></a><span data-ttu-id="2c459-192">100.86.92</span><span class="sxs-lookup"><span data-stu-id="2c459-192">100.86.92</span></span>

- <span data-ttu-id="2c459-193">Améliorations en matière de compatibilité avec Time Machine</span><span class="sxs-lookup"><span data-stu-id="2c459-193">Improvements around compatibility with Time Machine</span></span>
- <span data-ttu-id="2c459-194">Nous avons résolu un problème dans lequel le produit n’était parfois pas en train de nettoyer tous les fichiers pendant `/Library/Application Support/Microsoft/Defender` la désinstallation</span><span class="sxs-lookup"><span data-stu-id="2c459-194">Addressed an issue where the product was sometimes not cleaning all files under `/Library/Application Support/Microsoft/Defender` during uninstallation</span></span>
- <span data-ttu-id="2c459-195">Réduction de l’utilisation processeur du produit lorsque les produits Microsoft sont mis à jour via la mise à jour automatique Microsoft</span><span class="sxs-lookup"><span data-stu-id="2c459-195">Reduced the CPU utilization of the product when Microsoft products are updated through Microsoft AutoUpdate</span></span>
- <span data-ttu-id="2c459-196">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-196">Other performance improvements & bug fixes</span></span>

## <a name="1008691"></a><span data-ttu-id="2c459-197">100.86.91</span><span class="sxs-lookup"><span data-stu-id="2c459-197">100.86.91</span></span>

> [!CAUTION]
> <span data-ttu-id="2c459-198">Pour garantir la protection la plus complète pour vos appareils macOS et en adéquation avec l’arrêt par Apple de la distribution de mises à jour de sécurité natives macOS aux versions de système d’exploitation antérieures à [actuel – 2], le déploiement et les mises à jour MDATP pour Mac ne seront plus pris en charge sur macOS Sierra [10.12].</span><span class="sxs-lookup"><span data-stu-id="2c459-198">To ensure the most complete protection for your macOS devices and in alignment with Apple stopping delivery of macOS native security updates to OS versions older than [current – 2], MDATP for Mac deployment and updates will no longer be supported on macOS Sierra [10.12].</span></span> <span data-ttu-id="2c459-199">Les mises à jour et améliorations de MDATP pour Mac seront apportées aux appareils exécutant les versions Derline [10.15], Mojave [10.14] et High Sierra [10.13].</span><span class="sxs-lookup"><span data-stu-id="2c459-199">MDATP for Mac updates and enhancements will be delivered to devices running versions Catalina [10.15], Mojave [10.14], and High Sierra [10.13].</span></span> 
>
> <span data-ttu-id="2c459-200">Si vous avez déjà déployé MDATP pour Mac sur vos appareils Sierra [10.12], veuillez mettre à niveau vers la dernière version de macOS afin d’éliminer les risques de perte de protection.</span><span class="sxs-lookup"><span data-stu-id="2c459-200">If you already have MDATP for Mac deployed to your Sierra [10.12] devices, please upgrade to the latest macOS version to eliminate risks of losing protection.</span></span>

- <span data-ttu-id="2c459-201">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-201">Performance improvements & bug fixes</span></span>

## <a name="1008373"></a><span data-ttu-id="2c459-202">100.83.73</span><span class="sxs-lookup"><span data-stu-id="2c459-202">100.83.73</span></span>

- <span data-ttu-id="2c459-203">Ajout de contrôles pour les administrateurs informatiques autour de la gestion des [exclusions,](mac-preferences.md#exclusion-merge-policy)de la gestion des [paramètres](mac-preferences.md#threat-type-settings-merge-policy)de type de menace et des actions contre [les menaces non prises en charge](mac-preferences.md#disallowed-threat-actions)</span><span class="sxs-lookup"><span data-stu-id="2c459-203">Added more controls for IT administrators around [management of exclusions](mac-preferences.md#exclusion-merge-policy), [management of threat type settings](mac-preferences.md#threat-type-settings-merge-policy), and [disallowed threat actions](mac-preferences.md#disallowed-threat-actions)</span></span>
- <span data-ttu-id="2c459-204">Lorsque l’accès disque total n’est pas activé sur l’appareil, un avertissement s’affiche désormais dans le menu d’état</span><span class="sxs-lookup"><span data-stu-id="2c459-204">When Full Disk Access is not enabled on the device, a warning is now displayed in the status menu</span></span>
- <span data-ttu-id="2c459-205">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-205">Performance improvements & bug fixes</span></span>

## <a name="1008260"></a><span data-ttu-id="2c459-206">100.82.60</span><span class="sxs-lookup"><span data-stu-id="2c459-206">100.82.60</span></span>

- <span data-ttu-id="2c459-207">Nous avons résolu un problème dans lequel le produit ne parvient pas à démarrer à la suite d’une mise à jour de définition.</span><span class="sxs-lookup"><span data-stu-id="2c459-207">Addressed an issue where the product fails to start following a definition update.</span></span>

## <a name="1008042"></a><span data-ttu-id="2c459-208">100.80.42</span><span class="sxs-lookup"><span data-stu-id="2c459-208">100.80.42</span></span>

- <span data-ttu-id="2c459-209">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-209">Bug fixes</span></span>

## <a name="1007942"></a><span data-ttu-id="2c459-210">100.79.42</span><span class="sxs-lookup"><span data-stu-id="2c459-210">100.79.42</span></span>

- <span data-ttu-id="2c459-211">Correction d’un problème dans lequel Microsoft Defender pour Point de terminaison pour Mac interfère parfois avec Time Machine</span><span class="sxs-lookup"><span data-stu-id="2c459-211">Fixed an issue where Microsoft Defender for Endpoint for Mac was sometimes interfering with Time Machine</span></span>
- <span data-ttu-id="2c459-212">Ajout d’un nouveau commutateur à l’utilitaire de ligne de commande pour tester la connectivité avec le service back-end</span><span class="sxs-lookup"><span data-stu-id="2c459-212">Added a new switch to the command-line utility for testing the connectivity with the backend service</span></span>
  ```bash
  mdatp connectivity test
  ```
- <span data-ttu-id="2c459-213">Possibilité supplémentaire d’afficher l’historique complet des menaces dans l’interface utilisateur (accessible à partir de l’affichage Historique **de la** protection)</span><span class="sxs-lookup"><span data-stu-id="2c459-213">Added ability to view the full threat history in the user interface (can be accessed from the **Protection history** view)</span></span>
- <span data-ttu-id="2c459-214">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-214">Performance improvements & bug fixes</span></span>

## <a name="1007215"></a><span data-ttu-id="2c459-215">100.72.15</span><span class="sxs-lookup"><span data-stu-id="2c459-215">100.72.15</span></span>

- <span data-ttu-id="2c459-216">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-216">Bug fixes</span></span>

## <a name="1007099"></a><span data-ttu-id="2c459-217">100.70.99</span><span class="sxs-lookup"><span data-stu-id="2c459-217">100.70.99</span></span>

- <span data-ttu-id="2c459-218">Nous avons résolu un problème qui a une incidence sur la capacité de certains utilisateurs à mettre à niveau vers macOS Ils sont activés lorsque la protection en temps réel est activée.</span><span class="sxs-lookup"><span data-stu-id="2c459-218">Addressed an issue that impacts the ability of some users to upgrade to macOS Catalina when real-time protection is enabled.</span></span> <span data-ttu-id="2c459-219">Ce problème ponctuel a été provoqué par microsoft Defender pour le verrouillage des fichiers de point de terminaison dans le package de mise à niveau De base lors de l’analyse des menaces, ce qui a entraîné des échecs dans la séquence de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="2c459-219">This sporadic issue was caused by Microsoft Defender for Endpoint locking files within Catalina upgrade package while scanning them for threats, which led to failures in the upgrade sequence.</span></span>

## <a name="1006899"></a><span data-ttu-id="2c459-220">100.68.99</span><span class="sxs-lookup"><span data-stu-id="2c459-220">100.68.99</span></span>

- <span data-ttu-id="2c459-221">Ajout de la possibilité de configurer la fonctionnalité antivirus pour qu’elle s’exécute [en mode passif](mac-preferences.md#enable--disable-passive-mode)</span><span class="sxs-lookup"><span data-stu-id="2c459-221">Added the ability to configure the antivirus functionality to run in [passive mode](mac-preferences.md#enable--disable-passive-mode)</span></span>
- <span data-ttu-id="2c459-222">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-222">Performance improvements & bug fixes</span></span>

## <a name="1006528"></a><span data-ttu-id="2c459-223">100.65.28</span><span class="sxs-lookup"><span data-stu-id="2c459-223">100.65.28</span></span>

- <span data-ttu-id="2c459-224">Prise en charge supplémentaire de macOS</span><span class="sxs-lookup"><span data-stu-id="2c459-224">Added support for macOS Catalina</span></span>

  > [!CAUTION]
  > <span data-ttu-id="2c459-225">macOS 10.15 (Contrôle) contient de nouvelles améliorations en matière de sécurité et de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="2c459-225">macOS 10.15 (Catalina) contains new security and privacy enhancements.</span></span> <span data-ttu-id="2c459-226">À partir de cette version, par défaut, les applications ne peuvent pas accéder à certains emplacements sur disque (par exemple, Documents, Téléchargements, Bureau, etc.) sans consentement explicite.</span><span class="sxs-lookup"><span data-stu-id="2c459-226">Beginning with this version, by default, applications are not able to access certain locations on disk (such as Documents, Downloads, Desktop, etc.) without explicit consent.</span></span> <span data-ttu-id="2c459-227">En l’absence de ce consentement, Microsoft Defender pour le point de terminaison n’est pas en mesure de protéger entièrement votre appareil.</span><span class="sxs-lookup"><span data-stu-id="2c459-227">In the absence of this consent, Microsoft Defender for Endpoint is not able to fully protect your device.</span></span>
  >
  > <span data-ttu-id="2c459-228">Le mécanisme d’octroi de ce consentement dépend de la façon dont vous avez déployé Microsoft Defender pour endpoint :</span><span class="sxs-lookup"><span data-stu-id="2c459-228">The mechanism for granting this consent depends on how you deployed Microsoft Defender for Endpoint:</span></span>
  >
  > - <span data-ttu-id="2c459-229">Pour les déploiements manuels, consultez les instructions mises à jour dans la [rubrique Déploiement](mac-install-manually.md#how-to-allow-full-disk-access) manuel.</span><span class="sxs-lookup"><span data-stu-id="2c459-229">For manual deployments, see the updated instructions in the [Manual deployment](mac-install-manually.md#how-to-allow-full-disk-access) topic.</span></span>
  > - <span data-ttu-id="2c459-230">Pour les déploiements gérés, consultez les instructions mises à jour dans les rubriques sur le déploiement basé sur [JAMF](mac-install-with-jamf.md) et [microsoft Intune.](mac-install-with-intune.md#create-system-configuration-profiles)</span><span class="sxs-lookup"><span data-stu-id="2c459-230">For managed deployments, see the updated instructions in the [JAMF-based deployment](mac-install-with-jamf.md) and [Microsoft Intune-based deployment](mac-install-with-intune.md#create-system-configuration-profiles) topics.</span></span>

- <span data-ttu-id="2c459-231">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="2c459-231">Performance improvements & bug fixes</span></span>
