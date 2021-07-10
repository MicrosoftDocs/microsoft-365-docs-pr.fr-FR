---
title: Nouveautés de Microsoft Defender pour Point de terminaison sur Mac
description: Découvrez les principales modifications apportées aux versions précédentes de Microsoft Defender pour Endpoint sur Mac.
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, mac, installation, macos, whatsnew
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
ms.openlocfilehash: 841f22421ac81ba447dad70a68c4c7bc95605b16
ms.sourcegitcommit: 7dc3b4dec05299abb4290a6e3d1ebe0fdc622ed7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "53363894"
---
# <a name="whats-new-in-microsoft-defender-for-endpoint-on-mac"></a><span data-ttu-id="64231-104">Nouveautés de Microsoft Defender pour Point de terminaison sur Mac</span><span class="sxs-lookup"><span data-stu-id="64231-104">What's new in Microsoft Defender for Endpoint on Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="64231-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="64231-105">**Applies to:**</span></span>
- [<span data-ttu-id="64231-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="64231-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="64231-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="64231-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="64231-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="64231-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="64231-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="64231-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

> [!IMPORTANT]
> <span data-ttu-id="64231-110">Sur macOS 11 (Big Sur), Microsoft Defender for Endpoint nécessite des profils de configuration supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="64231-110">On macOS 11 (Big Sur), Microsoft Defender for Endpoint requires additional configuration profiles.</span></span> <span data-ttu-id="64231-111">Si vous êtes un client existant en cours de mise à niveau à partir de versions antérieures de macOS, veillez à déployer les profils de configuration supplémentaires répertoriés sur [cette page.](mac-sysext-policies.md)</span><span class="sxs-lookup"><span data-stu-id="64231-111">If you are an existing customer upgrading from earlier versions of macOS, make sure to deploy the additional configuration profiles listed on [this page](mac-sysext-policies.md).</span></span>

## <a name="1013420-20121051134200"></a><span data-ttu-id="64231-112">101.34.20 (20.121051.13420.0)</span><span class="sxs-lookup"><span data-stu-id="64231-112">101.34.20 (20.121051.13420.0)</span></span>

- <span data-ttu-id="64231-113">[Le contrôle d’appareil pour macOS](mac-device-control-overview.md) est désormais disponible en général</span><span class="sxs-lookup"><span data-stu-id="64231-113">[Device control for macOS](mac-device-control-overview.md) is now in general availability</span></span>
- <span data-ttu-id="64231-114">Nous avons résolu un problème dans lequel une analyse rapide n’a pas pu être démarrée à partir du menu d’état sur macOS 11 (Big Sur)</span><span class="sxs-lookup"><span data-stu-id="64231-114">Addressed an issue where a quick scan could not be started from the status menu on macOS 11 (Big Sur)</span></span>
- <span data-ttu-id="64231-115">Autres correctifs de bogue</span><span class="sxs-lookup"><span data-stu-id="64231-115">Other bug fixes</span></span>

## <a name="1013269-20121042132690"></a><span data-ttu-id="64231-116">101.32.69 (20.121042.13269.0)</span><span class="sxs-lookup"><span data-stu-id="64231-116">101.32.69 (20.121042.13269.0)</span></span>

- <span data-ttu-id="64231-117">Nous avons résolu un problème dans lequel l’accès simultané auchain à partir de Microsoft Defender pour endpoint et d’autres applications peut entraîner une altération duchain.</span><span class="sxs-lookup"><span data-stu-id="64231-117">Addressed an issue where concurrent access to the keychain from Microsoft Defender for Endpoint and other applications can lead to keychain corruption.</span></span>

## <a name="1012964-20121042129640"></a><span data-ttu-id="64231-118">101.29.64 (20.121042.12964.0)</span><span class="sxs-lookup"><span data-stu-id="64231-118">101.29.64 (20.121042.12964.0)</span></span>

- <span data-ttu-id="64231-119">À partir de cette version, les menaces détectées lors des analyses antivirus à la demande déclenchées via le client de ligne de commande sont automatiquement corrigés.</span><span class="sxs-lookup"><span data-stu-id="64231-119">Starting with this version, threats detected during on-demand antivirus scans triggered through the command-line client are automatically remediated.</span></span> <span data-ttu-id="64231-120">Les menaces détectées lors des analyses déclenchées via l’interface utilisateur nécessitent toujours une action manuelle.</span><span class="sxs-lookup"><span data-stu-id="64231-120">Threats detected during scans triggered through the user interface still require manual action.</span></span>
- <span data-ttu-id="64231-121">`mdatp diagnostic real-time-protection-statistics` prend désormais en charge deux commutateurs supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="64231-121">`mdatp diagnostic real-time-protection-statistics` now supports two additional switches:</span></span>
  - <span data-ttu-id="64231-122">`--sort`: trie la sortie décroit par nombre total de fichiers analysés</span><span class="sxs-lookup"><span data-stu-id="64231-122">`--sort`: sorts the output descending by total number of files scanned</span></span>
  - <span data-ttu-id="64231-123">`--top N`: affiche les N premiers résultats (fonctionne uniquement si `--sort` elle est également spécifiée)</span><span class="sxs-lookup"><span data-stu-id="64231-123">`--top N`: displays the top N results (only works if `--sort` is also specified)</span></span>
- <span data-ttu-id="64231-124">Améliorations des performances (en particulier lorsque LAXX est utilisée) & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-124">Performance improvements (specifically for when YARN is used) & bug fixes</span></span>

## <a name="1012750-20121022127500"></a><span data-ttu-id="64231-125">101.27.50 (20.121022.12750.0)</span><span class="sxs-lookup"><span data-stu-id="64231-125">101.27.50 (20.121022.12750.0)</span></span>

- <span data-ttu-id="64231-126">Correctif à prendre en compte pour l’expiration du certificat Apple pour macOS Fixz et les version antérieures.</span><span class="sxs-lookup"><span data-stu-id="64231-126">Fix to accommodate for Apple certificate expiration for macOS Catalina and earlier.</span></span> <span data-ttu-id="64231-127">Ce correctif restaure la fonctionnalité gestion & menaces et vulnérabilités (TVM).</span><span class="sxs-lookup"><span data-stu-id="64231-127">This fix restores Threat & Vulnerability Management (TVM) functionality.</span></span>

## <a name="1012569-20121022125690"></a><span data-ttu-id="64231-128">101.25.69 (20.121022.12569.0)</span><span class="sxs-lookup"><span data-stu-id="64231-128">101.25.69 (20.121022.12569.0)</span></span>

- <span data-ttu-id="64231-129">Microsoft Defender pour point de terminaison sur macOS est désormais disponible en prévisualisation pour les clients du gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="64231-129">Microsoft Defender for Endpoint on macOS is now available in preview for US Government customers.</span></span> <span data-ttu-id="64231-130">Pour plus d’informations, [voir Microsoft Defender for Endpoint for US Government customers](gov.md).</span><span class="sxs-lookup"><span data-stu-id="64231-130">For more information, see [Microsoft Defender for Endpoint for US Government customers](gov.md).</span></span>
- <span data-ttu-id="64231-131">Améliorations des performances (en particulier pour la situation d’utilisation de l’application Simulateur XCode) & résolutions de bogues.</span><span class="sxs-lookup"><span data-stu-id="64231-131">Performance improvements (specifically for the situation when the XCode Simulator app is used) & bug fixes.</span></span>

## <a name="1012364-20121021123640"></a><span data-ttu-id="64231-132">101.23.64 (20.121021.12364.0)</span><span class="sxs-lookup"><span data-stu-id="64231-132">101.23.64 (20.121021.12364.0)</span></span>

- <span data-ttu-id="64231-133">Ajout d’une nouvelle option à l’outil en ligne de commande pour afficher les informations sur la dernière analyse à la demande.</span><span class="sxs-lookup"><span data-stu-id="64231-133">Added a new option to the command-line tool to view information about the last on-demand scan.</span></span> <span data-ttu-id="64231-134">Pour afficher des informations sur la dernière analyse à la demande, exécutez `mdatp health --details antivirus`</span><span class="sxs-lookup"><span data-stu-id="64231-134">To view information about the last on-demand scan, run `mdatp health --details antivirus`</span></span>
- <span data-ttu-id="64231-135">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-135">Performance improvements & bug fixes</span></span>

## <a name="1012279-20121012122790"></a><span data-ttu-id="64231-136">101.22.79 (20.121012.12279.0)</span><span class="sxs-lookup"><span data-stu-id="64231-136">101.22.79 (20.121012.12279.0)</span></span>

- <span data-ttu-id="64231-137">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-137">Performance improvements & bug fixes</span></span>

## <a name="1011988-20121011119880"></a><span data-ttu-id="64231-138">101.19.88 (20.121011.11988.0)</span><span class="sxs-lookup"><span data-stu-id="64231-138">101.19.88 (20.121011.11988.0)</span></span>

- <span data-ttu-id="64231-139">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-139">Performance improvements & bug fixes</span></span>

## <a name="1011948-20120121119480"></a><span data-ttu-id="64231-140">101.19.48 (20.120121.11948.0)</span><span class="sxs-lookup"><span data-stu-id="64231-140">101.19.48 (20.120121.11948.0)</span></span>

> [!NOTE]
> <span data-ttu-id="64231-141">L’ancienne syntaxe de l’outil de ligne de commande a été dépréciée avec cette version.</span><span class="sxs-lookup"><span data-stu-id="64231-141">The old command-line tool syntax has been deprecated with this release.</span></span> <span data-ttu-id="64231-142">Pour plus d’informations sur la nouvelle syntaxe, voir [Resources](mac-resources.md#configuring-from-the-command-line).</span><span class="sxs-lookup"><span data-stu-id="64231-142">For information on the new syntax, see [Resources](mac-resources.md#configuring-from-the-command-line).</span></span>

- <span data-ttu-id="64231-143">Ajout d’un nouveau commutateur de ligne de commande pour désactiver l’extension réseau : `mdatp system-extension network-filter disable` .</span><span class="sxs-lookup"><span data-stu-id="64231-143">Added a new command-line switch to disable the network extension: `mdatp system-extension network-filter disable`.</span></span> <span data-ttu-id="64231-144">Cette commande peut être utile pour résoudre les problèmes réseau qui peuvent être liés à Microsoft Defender pour Endpoint sur Mac</span><span class="sxs-lookup"><span data-stu-id="64231-144">This command can be useful to troubleshoot networking issues that could be related to Microsoft Defender for Endpoint on Mac</span></span>
- <span data-ttu-id="64231-145">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-145">Performance improvements & bug fixes</span></span>

## <a name="1011921-20120101119210"></a><span data-ttu-id="64231-146">101.19.21 (20.120101.11921.0)</span><span class="sxs-lookup"><span data-stu-id="64231-146">101.19.21 (20.120101.11921.0)</span></span>

- <span data-ttu-id="64231-147">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-147">Bug fixes</span></span>

## <a name="1011526-20120102115260"></a><span data-ttu-id="64231-148">101.15.26 (20.120102.11526.0)</span><span class="sxs-lookup"><span data-stu-id="64231-148">101.15.26 (20.120102.11526.0)</span></span>

- <span data-ttu-id="64231-149">Amélioration de la fiabilité de l’agent lors de l’exécution sur macOS 11 Big Sur</span><span class="sxs-lookup"><span data-stu-id="64231-149">Improved the reliability of the agent when running on macOS 11 Big Sur</span></span>
- <span data-ttu-id="64231-150">Ajout d’un nouveau commutateur de ligne de commande ( ) pour ignorer les exclusions av lors `--ignore-exclusions` des analyses personnalisées ( `mdatp scan custom` )</span><span class="sxs-lookup"><span data-stu-id="64231-150">Added a new command-line switch (`--ignore-exclusions`) to ignore AV exclusions during custom scans (`mdatp scan custom`)</span></span>
- <span data-ttu-id="64231-151">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-151">Performance improvements & bug fixes</span></span>

## <a name="1011375-20120101113750"></a><span data-ttu-id="64231-152">101.13.75 (20.120101.11375.0)</span><span class="sxs-lookup"><span data-stu-id="64231-152">101.13.75 (20.120101.11375.0)</span></span>

- <span data-ttu-id="64231-153">Conditions supprimées lorsque Microsoft Defender pour le point de terminaison déclenchant un bogue macOS 11 (Big Sur) qui se manifeste en noyau</span><span class="sxs-lookup"><span data-stu-id="64231-153">Removed conditions when Microsoft Defender for Endpoint was triggering a macOS 11 (Big Sur) bug that manifests into a kernel panic</span></span>
- <span data-ttu-id="64231-154">Correction d’une fuite de mémoire dans l’extension système de sécurité des points de terminaison lors de l’exécution sur mac 11 (Big Sur)</span><span class="sxs-lookup"><span data-stu-id="64231-154">Fixed a memory leak in the Endpoint Security system extension when running on mac 11 (Big Sur)</span></span>
- <span data-ttu-id="64231-155">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-155">Bug fixes</span></span>

## <a name="1011072"></a><span data-ttu-id="64231-156">101.10.72</span><span class="sxs-lookup"><span data-stu-id="64231-156">101.10.72</span></span>

- <span data-ttu-id="64231-157">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-157">Bug fixes</span></span>

## <a name="1010961"></a><span data-ttu-id="64231-158">101.09.61</span><span class="sxs-lookup"><span data-stu-id="64231-158">101.09.61</span></span>

- <span data-ttu-id="64231-159">Ajout d’une nouvelle préférence gérée pour [désactiver l’option d’envoi de commentaires](mac-preferences.md#show--hide-option-to-send-feedback)</span><span class="sxs-lookup"><span data-stu-id="64231-159">Added a new managed preference for [disabling the option to send feedback](mac-preferences.md#show--hide-option-to-send-feedback)</span></span>
- <span data-ttu-id="64231-160">L’icône du menu État affiche désormais un état sain lorsque les paramètres du produit sont gérés.</span><span class="sxs-lookup"><span data-stu-id="64231-160">Status menu icon now shows a healthy state when the product settings are managed.</span></span> <span data-ttu-id="64231-161">Auparavant, l’icône du menu d’état affichait un état d’avertissement ou d’erreur, même si les paramètres du produit étaient gérés par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="64231-161">Previously, the status menu icon was displaying a warning or error state, even though the product settings were managed by the administrator</span></span>
- <span data-ttu-id="64231-162">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-162">Performance improvements & bug fixes</span></span>

## <a name="1010950"></a><span data-ttu-id="64231-163">101.09.50</span><span class="sxs-lookup"><span data-stu-id="64231-163">101.09.50</span></span>

- <span data-ttu-id="64231-164">Cette version du produit a été validée sur macOS Big Sur 11 bêta 9</span><span class="sxs-lookup"><span data-stu-id="64231-164">This product version has been validated on macOS Big Sur 11 beta 9</span></span>

- <span data-ttu-id="64231-165">La nouvelle syntaxe de `mdatp` l’outil en ligne de commande est désormais la syntaxe par défaut.</span><span class="sxs-lookup"><span data-stu-id="64231-165">The new syntax for the `mdatp` command-line tool is now the default one.</span></span> <span data-ttu-id="64231-166">Pour plus d’informations sur la nouvelle syntaxe, voir [Resources for Microsoft Defender for Endpoint on macOS](mac-resources.md#configuring-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="64231-166">For more information on the new syntax, see [Resources for Microsoft Defender for Endpoint on macOS](mac-resources.md#configuring-from-the-command-line)</span></span>

  > [!NOTE]
  > <span data-ttu-id="64231-167">L’ancienne syntaxe de l’outil de ligne de commande sera supprimée du produit le **1er janvier 2021.**</span><span class="sxs-lookup"><span data-stu-id="64231-167">The old command-line tool syntax will be removed from the product on **January 1st, 2021**.</span></span>

- <span data-ttu-id="64231-168">Étendu avec un nouveau paramètre ( ) qui permet d’enregistrer les journaux de diagnostic dans `mdatp diagnostic create` `--path [directory]` un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="64231-168">Extended `mdatp diagnostic create` with a new parameter (`--path [directory]`) that allows the diagnostic logs to be saved to a different directory</span></span>
- <span data-ttu-id="64231-169">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-169">Performance improvements & bug fixes</span></span>

## <a name="1010949"></a><span data-ttu-id="64231-170">101.09.49</span><span class="sxs-lookup"><span data-stu-id="64231-170">101.09.49</span></span>

- <span data-ttu-id="64231-171">Améliorations apportées à l’interface utilisateur pour différencier les exclusions gérées par l’administrateur informatique des exclusions définies par l’utilisateur local</span><span class="sxs-lookup"><span data-stu-id="64231-171">User interface improvements to differentiate exclusions that are managed by the IT administrator versus exclusions defined by the local user</span></span>
- <span data-ttu-id="64231-172">Amélioration de l’utilisation du processeur lors des analyses à la demande</span><span class="sxs-lookup"><span data-stu-id="64231-172">Improved CPU utilization during on-demand scans</span></span>
- <span data-ttu-id="64231-173">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-173">Performance improvements & bug fixes</span></span>

## <a name="1010723"></a><span data-ttu-id="64231-174">101.07.23</span><span class="sxs-lookup"><span data-stu-id="64231-174">101.07.23</span></span>

- <span data-ttu-id="64231-175">Ajout de nouveaux champs à la sortie de la vérification de l’état du mode passif et de `mdatp --health` l’ID PEPT groupe</span><span class="sxs-lookup"><span data-stu-id="64231-175">Added new fields to the output of `mdatp --health` for checking the status of passive mode and the EDR group ID</span></span>

  > [!NOTE]
  > <span data-ttu-id="64231-176">`mdatp --health` sera remplacé par `mdatp health` dans une prochaine mise à jour du produit.</span><span class="sxs-lookup"><span data-stu-id="64231-176">`mdatp --health` will be replaced with `mdatp health` in a future product update.</span></span>

- <span data-ttu-id="64231-177">Correction d’un bogue dans lequel l’envoi automatique d’échantillons n’a pas été marqué comme géré dans l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="64231-177">Fixed a bug where automatic sample submission was not marked as managed in the user interface</span></span>
- <span data-ttu-id="64231-178">Ajout de nouveaux paramètres pour contrôler la rétention des éléments dans l’historique d’analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="64231-178">Added new settings for controlling the retention of items in the antivirus scan history.</span></span> <span data-ttu-id="64231-179">Vous pouvez maintenant [spécifier le nombre](mac-preferences.md#antivirus-scan-history-retention-in-days) de jours de rétention des éléments dans l’historique d’analyse et spécifier le nombre maximal d’éléments [dans l’historique d’analyse.](mac-preferences.md#maximum-number-of-items-in-the-antivirus-scan-history)</span><span class="sxs-lookup"><span data-stu-id="64231-179">You can now [specify the number of days to retain items in the scan history](mac-preferences.md#antivirus-scan-history-retention-in-days) and [specify the maximum number of items in the scan history](mac-preferences.md#maximum-number-of-items-in-the-antivirus-scan-history)</span></span>
- <span data-ttu-id="64231-180">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-180">Bug fixes</span></span>

## <a name="1010663"></a><span data-ttu-id="64231-181">101.06.63</span><span class="sxs-lookup"><span data-stu-id="64231-181">101.06.63</span></span>

- <span data-ttu-id="64231-182">Nous avons résolu une régression des performances introduite dans la `101.05.17` version.</span><span class="sxs-lookup"><span data-stu-id="64231-182">Addressed a performance regression introduced in version `101.05.17`.</span></span> <span data-ttu-id="64231-183">La régression a été introduite avec le correctif pour éliminer les noyaux que certains clients ont observés lors de l’accès aux partages SMB.</span><span class="sxs-lookup"><span data-stu-id="64231-183">The regression was introduced with the fix to eliminate the kernel panics some customers have observed when accessing SMB shares.</span></span> <span data-ttu-id="64231-184">Nous avons revenir à ce changement de code et nous sommes en train d’examiner d’autres façons d’éliminer les noyaux.</span><span class="sxs-lookup"><span data-stu-id="64231-184">We have reverted this code change and are investigating alternative ways to eliminate the kernel panics.</span></span>

## <a name="1010517"></a><span data-ttu-id="64231-185">101.05.17</span><span class="sxs-lookup"><span data-stu-id="64231-185">101.05.17</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64231-186">Nous travaillons sur une syntaxe nouvelle et améliorée pour `mdatp` l’outil en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="64231-186">We are working on a new and enhanced syntax for the `mdatp` command-line tool.</span></span> <span data-ttu-id="64231-187">La nouvelle syntaxe est actuellement la valeur par défaut dans les canaux de mise à jour Insider Fast et Insider Slow.</span><span class="sxs-lookup"><span data-stu-id="64231-187">The new syntax is currently the default in the Insider Fast and Insider Slow update channels.</span></span> <span data-ttu-id="64231-188">Nous vous encourageons à vous familiariser avec cette nouvelle syntaxe.</span><span class="sxs-lookup"><span data-stu-id="64231-188">We encourage you to famliliarize yourself with this new syntax.</span></span>
> 
> <span data-ttu-id="64231-189">Nous continuerons à assurer la prise en charge de l’ancienne syntaxe parallèlement à la nouvelle syntaxe et nous fournirons davantage de communication autour du plan de désaprétation de l’ancienne syntaxe dans les mois à venir.</span><span class="sxs-lookup"><span data-stu-id="64231-189">We will continue supporting the old syntax in parallel with the new syntax and will provide more communication around the deprecation plan for the old syntax in the upcoming months.</span></span>

- <span data-ttu-id="64231-190">Nous avons résolu un problème de noyau qui se produisait parfois lors de l’accès aux partages de fichiers SMB</span><span class="sxs-lookup"><span data-stu-id="64231-190">Addressed a kernel panic that occurred sometimes when accessing SMB file shares</span></span>
- <span data-ttu-id="64231-191">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-191">Performance improvements & bug fixes</span></span>

## <a name="1010516"></a><span data-ttu-id="64231-192">101.05.16</span><span class="sxs-lookup"><span data-stu-id="64231-192">101.05.16</span></span>

- <span data-ttu-id="64231-193">Améliorations apportées à la logique d’analyse rapide pour réduire considérablement le nombre de fichiers analysés</span><span class="sxs-lookup"><span data-stu-id="64231-193">Improvements to quick scan logic to significantly reduce the number of scanned files</span></span>
- <span data-ttu-id="64231-194">Ajout de la prise en charge [de lacompletion](mac-resources.md#how-to-enable-autocompletion) automatique pour l’outil en ligne de commande</span><span class="sxs-lookup"><span data-stu-id="64231-194">Added [autocompletion support](mac-resources.md#how-to-enable-autocompletion) for the command-line tool</span></span>
- <span data-ttu-id="64231-195">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-195">Bug fixes</span></span>

## <a name="1010312"></a><span data-ttu-id="64231-196">101.03.12</span><span class="sxs-lookup"><span data-stu-id="64231-196">101.03.12</span></span>

- <span data-ttu-id="64231-197">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-197">Performance improvements & bug fixes</span></span>

## <a name="1010154"></a><span data-ttu-id="64231-198">101.01.54</span><span class="sxs-lookup"><span data-stu-id="64231-198">101.01.54</span></span>

- <span data-ttu-id="64231-199">Améliorations en matière de compatibilité avec Time Machine</span><span class="sxs-lookup"><span data-stu-id="64231-199">Improvements around compatibility with Time Machine</span></span>
- <span data-ttu-id="64231-200">Améliorations en matière d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="64231-200">Accessibility improvements</span></span>
- <span data-ttu-id="64231-201">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-201">Performance improvements & bug fixes</span></span>

## <a name="1010031"></a><span data-ttu-id="64231-202">101.00.31</span><span class="sxs-lookup"><span data-stu-id="64231-202">101.00.31</span></span>

- <span data-ttu-id="64231-203">Amélioration de [l’expérience d’intégration de produit pour les utilisateurs d’Intune](/mem/intune/apps/apps-advanced-threat-protection-macos)</span><span class="sxs-lookup"><span data-stu-id="64231-203">Improved [product onboarding experience for Intune users](/mem/intune/apps/apps-advanced-threat-protection-macos)</span></span>
- <span data-ttu-id="64231-204">Les [exclusions antivirus désormais prise en charge les caractères génériques](mac-exclusions.md#supported-exclusion-types)</span><span class="sxs-lookup"><span data-stu-id="64231-204">Antivirus [exclusions now support wildcards](mac-exclusions.md#supported-exclusion-types)</span></span>
- <span data-ttu-id="64231-205">Ajout de la possibilité de déclencher des analyses antivirus à partir du menu contextuel macOS.</span><span class="sxs-lookup"><span data-stu-id="64231-205">Added the ability to trigger antivirus scans from the macOS contextual menu.</span></span> <span data-ttu-id="64231-206">Vous pouvez maintenant cliquer avec le bouton droit sur un fichier ou un dossier dans finder et sélectionner Analyser **avec Microsoft Defender pour le point de terminaison**</span><span class="sxs-lookup"><span data-stu-id="64231-206">You can now right-click a file or a folder in Finder and select **Scan with Microsoft Defender for Endpoint**</span></span>
- <span data-ttu-id="64231-207">Les rétrogradations de produits sur place sont désormais explicitement interdits par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="64231-207">In-place product downgrades are now explicitly disallowed by the installer.</span></span> <span data-ttu-id="64231-208">Si vous devez rétrograder, désinstallez d’abord la version existante et reconfigurez votre appareil.</span><span class="sxs-lookup"><span data-stu-id="64231-208">If you need to downgrade, first uninstall the existing version and reconfigure your device</span></span>
- <span data-ttu-id="64231-209">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-209">Other performance improvements & bug fixes</span></span>

## <a name="1009027"></a><span data-ttu-id="64231-210">100.90.27</span><span class="sxs-lookup"><span data-stu-id="64231-210">100.90.27</span></span>

- <span data-ttu-id="64231-211">Vous pouvez désormais [définir un canal](mac-updates.md#set-the-channel-name) de mise à jour pour Microsoft Defender pour point de terminaison sur macOS qui est différent du canal de mise à jour à l’échelle du système</span><span class="sxs-lookup"><span data-stu-id="64231-211">You can now [set an update channel](mac-updates.md#set-the-channel-name) for Microsoft Defender for Endpoint on macOS that is different from the system-wide update channel</span></span>
- <span data-ttu-id="64231-212">Icône Nouveau produit</span><span class="sxs-lookup"><span data-stu-id="64231-212">New product icon</span></span>
- <span data-ttu-id="64231-213">Autres améliorations de l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="64231-213">Other user experience improvements</span></span>
- <span data-ttu-id="64231-214">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-214">Bug fixes</span></span>

## <a name="1008692"></a><span data-ttu-id="64231-215">100.86.92</span><span class="sxs-lookup"><span data-stu-id="64231-215">100.86.92</span></span>

- <span data-ttu-id="64231-216">Améliorations en matière de compatibilité avec Time Machine</span><span class="sxs-lookup"><span data-stu-id="64231-216">Improvements around compatibility with Time Machine</span></span>
- <span data-ttu-id="64231-217">Nous avons résolu un problème dans lequel le produit n’était parfois pas en train de nettoyer tous les fichiers pendant `/Library/Application Support/Microsoft/Defender` la désinstallation</span><span class="sxs-lookup"><span data-stu-id="64231-217">Addressed an issue where the product was sometimes not cleaning all files under `/Library/Application Support/Microsoft/Defender` during uninstallation</span></span>
- <span data-ttu-id="64231-218">Réduction de l’utilisation processeur du produit lorsque les produits Microsoft sont mis à jour via la mise à jour automatique Microsoft</span><span class="sxs-lookup"><span data-stu-id="64231-218">Reduced the CPU utilization of the product when Microsoft products are updated through Microsoft AutoUpdate</span></span>
- <span data-ttu-id="64231-219">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-219">Other performance improvements & bug fixes</span></span>

## <a name="1008691"></a><span data-ttu-id="64231-220">100.86.91</span><span class="sxs-lookup"><span data-stu-id="64231-220">100.86.91</span></span>

> [!CAUTION]
> <span data-ttu-id="64231-221">Pour garantir la protection la plus complète pour vos appareils macOS et en adéquation avec l’arrêt par Apple de la distribution de mises à jour de sécurité natives macOS aux versions de système d’exploitation antérieures à [actuel – 2], le déploiement et les mises à jour MDATP pour Mac ne seront plus pris en charge sur macOS Sierra [10.12].</span><span class="sxs-lookup"><span data-stu-id="64231-221">To ensure the most complete protection for your macOS devices and in alignment with Apple stopping delivery of macOS native security updates to OS versions older than [current – 2], MDATP for Mac deployment and updates will no longer be supported on macOS Sierra [10.12].</span></span> <span data-ttu-id="64231-222">Les mises à jour et améliorations de MDATP pour Mac seront apportées aux appareils exécutant les versions Derline [10.15], Mojave [10.14] et High Sierra [10.13].</span><span class="sxs-lookup"><span data-stu-id="64231-222">MDATP for Mac updates and enhancements will be delivered to devices running versions Catalina [10.15], Mojave [10.14], and High Sierra [10.13].</span></span> 
>
> <span data-ttu-id="64231-223">Si vous avez déjà déployé MDATP pour Mac sur vos appareils Sierra [10.12], veuillez mettre à niveau vers la dernière version de macOS afin d’éliminer les risques de perte de protection.</span><span class="sxs-lookup"><span data-stu-id="64231-223">If you already have MDATP for Mac deployed to your Sierra [10.12] devices, please upgrade to the latest macOS version to eliminate risks of losing protection.</span></span>

- <span data-ttu-id="64231-224">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-224">Performance improvements & bug fixes</span></span>

## <a name="1008373"></a><span data-ttu-id="64231-225">100.83.73</span><span class="sxs-lookup"><span data-stu-id="64231-225">100.83.73</span></span>

- <span data-ttu-id="64231-226">Ajout de contrôles pour les administrateurs informatiques autour de la gestion des [exclusions,](mac-preferences.md#exclusion-merge-policy)de la gestion des [paramètres](mac-preferences.md#threat-type-settings-merge-policy)de type de menace et des actions contre [les menaces non prises en charge](mac-preferences.md#disallowed-threat-actions)</span><span class="sxs-lookup"><span data-stu-id="64231-226">Added more controls for IT administrators around [management of exclusions](mac-preferences.md#exclusion-merge-policy), [management of threat type settings](mac-preferences.md#threat-type-settings-merge-policy), and [disallowed threat actions](mac-preferences.md#disallowed-threat-actions)</span></span>
- <span data-ttu-id="64231-227">Lorsque l’accès disque total n’est pas activé sur l’appareil, un avertissement s’affiche désormais dans le menu d’état</span><span class="sxs-lookup"><span data-stu-id="64231-227">When Full Disk Access is not enabled on the device, a warning is now displayed in the status menu</span></span>
- <span data-ttu-id="64231-228">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-228">Performance improvements & bug fixes</span></span>

## <a name="1008260"></a><span data-ttu-id="64231-229">100.82.60</span><span class="sxs-lookup"><span data-stu-id="64231-229">100.82.60</span></span>

- <span data-ttu-id="64231-230">Nous avons résolu un problème dans lequel le produit ne parvient pas à démarrer à la suite d’une mise à jour de définition.</span><span class="sxs-lookup"><span data-stu-id="64231-230">Addressed an issue where the product fails to start following a definition update.</span></span>

## <a name="1008042"></a><span data-ttu-id="64231-231">100.80.42</span><span class="sxs-lookup"><span data-stu-id="64231-231">100.80.42</span></span>

- <span data-ttu-id="64231-232">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-232">Bug fixes</span></span>

## <a name="1007942"></a><span data-ttu-id="64231-233">100.79.42</span><span class="sxs-lookup"><span data-stu-id="64231-233">100.79.42</span></span>

- <span data-ttu-id="64231-234">Correction d’un problème dans lequel Microsoft Defender pour point de terminaison sur Mac interfère parfois avec Time Machine</span><span class="sxs-lookup"><span data-stu-id="64231-234">Fixed an issue where Microsoft Defender for Endpoint on Mac was sometimes interfering with Time Machine</span></span>
- <span data-ttu-id="64231-235">Ajout d’un nouveau commutateur à l’utilitaire de ligne de commande pour tester la connectivité avec le service back-end</span><span class="sxs-lookup"><span data-stu-id="64231-235">Added a new switch to the command-line utility for testing the connectivity with the backend service</span></span>
  ```bash
  mdatp connectivity test
  ```
- <span data-ttu-id="64231-236">Possibilité supplémentaire d’afficher l’historique complet des menaces dans l’interface utilisateur (accessible à partir de l’affichage Historique **de la** protection)</span><span class="sxs-lookup"><span data-stu-id="64231-236">Added ability to view the full threat history in the user interface (can be accessed from the **Protection history** view)</span></span>
- <span data-ttu-id="64231-237">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-237">Performance improvements & bug fixes</span></span>

## <a name="1007215"></a><span data-ttu-id="64231-238">100.72.15</span><span class="sxs-lookup"><span data-stu-id="64231-238">100.72.15</span></span>

- <span data-ttu-id="64231-239">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-239">Bug fixes</span></span>

## <a name="1007099"></a><span data-ttu-id="64231-240">100.70.99</span><span class="sxs-lookup"><span data-stu-id="64231-240">100.70.99</span></span>

- <span data-ttu-id="64231-241">Nous avons résolu un problème qui a une incidence sur la capacité de certains utilisateurs à mettre à niveau vers macOS Ils sont activés lorsque la protection en temps réel est activée.</span><span class="sxs-lookup"><span data-stu-id="64231-241">Addressed an issue that impacts the ability of some users to upgrade to macOS Catalina when real-time protection is enabled.</span></span> <span data-ttu-id="64231-242">Ce problème ponctuel a été provoqué par microsoft Defender pour le verrouillage des fichiers de point de terminaison dans le package de mise à niveau De base lors de l’analyse des menaces, ce qui a entraîné des échecs dans la séquence de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="64231-242">This sporadic issue was caused by Microsoft Defender for Endpoint locking files within Catalina upgrade package while scanning them for threats, which led to failures in the upgrade sequence.</span></span>

## <a name="1006899"></a><span data-ttu-id="64231-243">100.68.99</span><span class="sxs-lookup"><span data-stu-id="64231-243">100.68.99</span></span>

- <span data-ttu-id="64231-244">Ajout de la possibilité de configurer la fonctionnalité antivirus pour qu’elle s’exécute [en mode passif](mac-preferences.md#enable--disable-passive-mode)</span><span class="sxs-lookup"><span data-stu-id="64231-244">Added the ability to configure the antivirus functionality to run in [passive mode](mac-preferences.md#enable--disable-passive-mode)</span></span>
- <span data-ttu-id="64231-245">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-245">Performance improvements & bug fixes</span></span>

## <a name="1006528"></a><span data-ttu-id="64231-246">100.65.28</span><span class="sxs-lookup"><span data-stu-id="64231-246">100.65.28</span></span>

- <span data-ttu-id="64231-247">Prise en charge supplémentaire de macOS</span><span class="sxs-lookup"><span data-stu-id="64231-247">Added support for macOS Catalina</span></span>

  > [!CAUTION]
  > <span data-ttu-id="64231-248">macOS 10.15 (Contrôle) contient de nouvelles améliorations en matière de sécurité et de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="64231-248">macOS 10.15 (Catalina) contains new security and privacy enhancements.</span></span> <span data-ttu-id="64231-249">À partir de cette version, par défaut, les applications ne peuvent pas accéder à certains emplacements sur le disque (par exemple, Documents, Téléchargements, Bureau, etc.) sans consentement explicite.</span><span class="sxs-lookup"><span data-stu-id="64231-249">Beginning with this version, by default, applications are not able to access certain locations on disk (such as Documents, Downloads, Desktop, etc.) without explicit consent.</span></span> <span data-ttu-id="64231-250">En l’absence de ce consentement, Microsoft Defender pour le point de terminaison n’est pas en mesure de protéger entièrement votre appareil.</span><span class="sxs-lookup"><span data-stu-id="64231-250">In the absence of this consent, Microsoft Defender for Endpoint is not able to fully protect your device.</span></span>
  >
  > <span data-ttu-id="64231-251">Le mécanisme d’octroi de ce consentement dépend de la façon dont vous avez déployé Microsoft Defender pour endpoint :</span><span class="sxs-lookup"><span data-stu-id="64231-251">The mechanism for granting this consent depends on how you deployed Microsoft Defender for Endpoint:</span></span>
  >
  > - <span data-ttu-id="64231-252">Pour les déploiements manuels, consultez les instructions mises à jour dans la [rubrique Déploiement](mac-install-manually.md#how-to-allow-full-disk-access) manuel.</span><span class="sxs-lookup"><span data-stu-id="64231-252">For manual deployments, see the updated instructions in the [Manual deployment](mac-install-manually.md#how-to-allow-full-disk-access) topic.</span></span>
  > - <span data-ttu-id="64231-253">Pour les déploiements gérés, consultez les instructions mises à jour dans les rubriques sur le déploiement basé sur [JAMF](mac-install-with-jamf.md) [et Microsoft Intune](mac-install-with-intune.md#create-system-configuration-profiles) de déploiement basé sur jamf.</span><span class="sxs-lookup"><span data-stu-id="64231-253">For managed deployments, see the updated instructions in the [JAMF-based deployment](mac-install-with-jamf.md) and [Microsoft Intune-based deployment](mac-install-with-intune.md#create-system-configuration-profiles) topics.</span></span>

- <span data-ttu-id="64231-254">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="64231-254">Performance improvements & bug fixes</span></span>
