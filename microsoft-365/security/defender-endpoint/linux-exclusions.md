---
title: Configurer et valider des exclusions pour Microsoft Defender pour endpoint sur Linux
description: Fournir et valider des exclusions pour Microsoft Defender pour endpoint sur Linux. Les exclusions peuvent être définies pour les fichiers, dossiers et processus.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, exclusions, analyses, antivirus
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: bd506caa041af2585778fb3ecd7a40562463b17e
ms.sourcegitcommit: 94e64afaf12f3d8813099d8ffa46baba65772763
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52346413"
---
# <a name="configure-and-validate-exclusions-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="d4ebb-105">Configurer et valider des exclusions pour Microsoft Defender pour endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="d4ebb-105">Configure and validate exclusions for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d4ebb-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d4ebb-106">**Applies to:**</span></span>

- [<span data-ttu-id="d4ebb-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d4ebb-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d4ebb-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d4ebb-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="d4ebb-109">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d4ebb-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="d4ebb-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="d4ebb-111">Cet article fournit des informations sur la définition d’exclusions qui s’appliquent aux analyses à la demande, ainsi que sur la protection et la surveillance en temps réel.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-111">This article provides information on how to define exclusions that apply to on-demand scans, and real-time protection and monitoring.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4ebb-112">Les exclusions décrites dans cet article ne s’appliquent pas aux autres fonctionnalités de Defender for Endpoint sur Linux, notamment protection évolutive des points de terminaison (PEPT).</span><span class="sxs-lookup"><span data-stu-id="d4ebb-112">The exclusions described in this article don't apply to other Defender for Endpoint on Linux capabilities, including endpoint detection and response (EDR).</span></span> <span data-ttu-id="d4ebb-113">Les fichiers que vous excluez à l’aide des méthodes décrites dans cet article peuvent toujours déclencher PEPT alertes et autres détections.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-113">Files that you exclude using the methods described in this article can still trigger EDR alerts and other detections.</span></span>

<span data-ttu-id="d4ebb-114">Vous pouvez exclure certains fichiers, dossiers, processus et fichiers ouverts par processus de Defender for Endpoint sur les analyses Linux.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-114">You can exclude certain files, folders, processes, and process-opened files from Defender for Endpoint on Linux scans.</span></span>

<span data-ttu-id="d4ebb-115">Les exclusions peuvent être utiles pour éviter les détections incorrectes sur les fichiers ou les logiciels qui sont uniques ou personnalisés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-115">Exclusions can be useful to avoid incorrect detections on files or software that are unique or customized to your organization.</span></span> <span data-ttu-id="d4ebb-116">Ils peuvent également être utiles pour atténuer les problèmes de performances causés par Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-116">They can also be useful for mitigating performance issues caused by Defender for Endpoint on Linux.</span></span>

> [!WARNING]
> <span data-ttu-id="d4ebb-117">La définition d’exclusions réduit la protection offerte par Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-117">Defining exclusions lowers the protection offered by Defender for Endpoint on Linux.</span></span> <span data-ttu-id="d4ebb-118">Vous devez toujours évaluer les risques associés à l’implémentation d’exclusions, et vous devez exclure uniquement les fichiers dont vous êtes certain qu’ils ne sont pas malveillants.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-118">You should always evaluate the risks that are associated with implementing exclusions, and you should only exclude files that you are confident are not malicious.</span></span>

## <a name="supported-exclusion-types"></a><span data-ttu-id="d4ebb-119">Types d’exclusion pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4ebb-119">Supported exclusion types</span></span>

<span data-ttu-id="d4ebb-120">Le tableau suivant indique les types d’exclusion pris en charge par Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-120">The follow table shows the exclusion types supported by Defender for Endpoint on Linux.</span></span>

<span data-ttu-id="d4ebb-121">Exclusion</span><span class="sxs-lookup"><span data-stu-id="d4ebb-121">Exclusion</span></span> | <span data-ttu-id="d4ebb-122">Définition</span><span class="sxs-lookup"><span data-stu-id="d4ebb-122">Definition</span></span> | <span data-ttu-id="d4ebb-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="d4ebb-123">Examples</span></span>
---|---|---
<span data-ttu-id="d4ebb-124">Extension de fichier</span><span class="sxs-lookup"><span data-stu-id="d4ebb-124">File extension</span></span> | <span data-ttu-id="d4ebb-125">Tous les fichiers avec l’extension, n’importe où sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="d4ebb-125">All files with the extension, anywhere on the device</span></span> | `.test`
<span data-ttu-id="d4ebb-126">Fichier</span><span class="sxs-lookup"><span data-stu-id="d4ebb-126">File</span></span> | <span data-ttu-id="d4ebb-127">Un fichier spécifique identifié par le chemin d’accès complet</span><span class="sxs-lookup"><span data-stu-id="d4ebb-127">A specific file identified by the full path</span></span> | `/var/log/test.log`<br/>`/var/log/*.log`<br/>`/var/log/install.?.log`
<span data-ttu-id="d4ebb-128">Dossier</span><span class="sxs-lookup"><span data-stu-id="d4ebb-128">Folder</span></span> | <span data-ttu-id="d4ebb-129">Tous les fichiers sous le dossier spécifié (de manière récursive)</span><span class="sxs-lookup"><span data-stu-id="d4ebb-129">All files under the specified folder (recursively)</span></span> | `/var/log/`<br/>`/var/*/`
<span data-ttu-id="d4ebb-130">Processus</span><span class="sxs-lookup"><span data-stu-id="d4ebb-130">Process</span></span> | <span data-ttu-id="d4ebb-131">Un processus spécifique (spécifié par le chemin d’accès complet ou le nom de fichier) et tous les fichiers ouverts par celui-ci</span><span class="sxs-lookup"><span data-stu-id="d4ebb-131">A specific process (specified either by the full path or file name) and all files opened by it</span></span> | `/bin/cat`<br/>`cat`<br/>`c?t`

> [!IMPORTANT]
> <span data-ttu-id="d4ebb-132">Les chemins ci-dessus doivent être des liens durs, et non symboliques, pour être correctement exclus.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-132">The paths above must be hard links, not symbolic links, in order to be successfully excluded.</span></span> <span data-ttu-id="d4ebb-133">Vous pouvez vérifier si un chemin d’accès est un lien symbolique en exécutant `file <path-name>` .</span><span class="sxs-lookup"><span data-stu-id="d4ebb-133">You can check if a path is a symbolic link by running `file <path-name>`.</span></span>

<span data-ttu-id="d4ebb-134">Les exclusions de fichiers, de dossiers et de processus prisent en charge les caractères génériques suivants :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-134">File, folder, and process exclusions support the following wildcards:</span></span>

<span data-ttu-id="d4ebb-135">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="d4ebb-135">Wildcard</span></span> | <span data-ttu-id="d4ebb-136">Description</span><span class="sxs-lookup"><span data-stu-id="d4ebb-136">Description</span></span> | <span data-ttu-id="d4ebb-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="d4ebb-137">Example</span></span> | <span data-ttu-id="d4ebb-138">Correspondances</span><span class="sxs-lookup"><span data-stu-id="d4ebb-138">Matches</span></span> | <span data-ttu-id="d4ebb-139">Ne correspond pas</span><span class="sxs-lookup"><span data-stu-id="d4ebb-139">Does not match</span></span>
---|---|---|---|---
\* |    <span data-ttu-id="d4ebb-140">Correspond à n’importe quel nombre de caractères, y compris aucun (notez que lorsque ce caractère générique est utilisé à l’intérieur d’un chemin d’accès, il ne remplace qu’un seul dossier)</span><span class="sxs-lookup"><span data-stu-id="d4ebb-140">Matches any number of any characters including none (note that when this wildcard is used inside a path it will substitute only one folder)</span></span> | `/var/\*/\*.log` | `/var/log/system.log` | `/var/log/nested/system.log`
<span data-ttu-id="d4ebb-141">?</span><span class="sxs-lookup"><span data-stu-id="d4ebb-141">?</span></span> | <span data-ttu-id="d4ebb-142">Correspond à n’importe quel caractère</span><span class="sxs-lookup"><span data-stu-id="d4ebb-142">Matches any single character</span></span> | `file?.log` | `file1.log`<br/>`file2.log` | `file123.log`

## <a name="how-to-configure-the-list-of-exclusions"></a><span data-ttu-id="d4ebb-143">Comment configurer la liste des exclusions</span><span class="sxs-lookup"><span data-stu-id="d4ebb-143">How to configure the list of exclusions</span></span>

### <a name="from-the-management-console"></a><span data-ttu-id="d4ebb-144">À partir de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="d4ebb-144">From the management console</span></span>

<span data-ttu-id="d4ebb-145">Pour plus d’informations sur la configuration des exclusions à partir d’Une autre console de gestion, Ansible ou d’une autre console de gestion, voir Définir les préférences de [Defender pour Endpoint sur Linux.](linux-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="d4ebb-145">For more information on how to configure exclusions from Puppet, Ansible, or another management console, see [Set preferences for Defender for Endpoint on Linux](linux-preferences.md).</span></span>

### <a name="from-the-command-line"></a><span data-ttu-id="d4ebb-146">À partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d4ebb-146">From the command line</span></span>

<span data-ttu-id="d4ebb-147">Exécutez la commande suivante pour voir les commutateurs disponibles pour la gestion des exclusions :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-147">Run the following command to see the available switches for managing exclusions:</span></span>

```bash
mdatp exclusion
```

> [!TIP]
> <span data-ttu-id="d4ebb-148">Lorsque vous configurez des exclusions avec des caractères génériques, insérez le paramètre entre guillemets doubles pour empêcher le globbing.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-148">When configuring exclusions with wildcards, enclose the parameter in double-quotes to prevent globbing.</span></span>

<span data-ttu-id="d4ebb-149">Exemples :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-149">Examples:</span></span>

- <span data-ttu-id="d4ebb-150">Ajoutez une exclusion pour une extension de fichier :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-150">Add an exclusion for a file extension:</span></span>

    ```bash
    mdatp exclusion extension add --name .txt
    ```
    ```Output
    Extension exclusion configured successfully
    ```

- <span data-ttu-id="d4ebb-151">Ajoutez une exclusion pour un fichier :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-151">Add an exclusion for a file:</span></span>

    ```bash
    mdatp exclusion file add --path /var/log/dummy.log
    ```
    ```Output
    File exclusion configured successfully
    ```

- <span data-ttu-id="d4ebb-152">Ajoutez une exclusion pour un dossier :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-152">Add an exclusion for a folder:</span></span>

    ```bash
    mdatp exclusion folder add --path /var/log/
    ```
    ```Output
    Folder exclusion configured successfully
    ```

- <span data-ttu-id="d4ebb-153">Ajoutez une exclusion pour un dossier contenant un caractère générique :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-153">Add an exclusion for a folder with a wildcard in it:</span></span>

    ```bash
    mdatp exclusion folder add --path "/var/*/"
    ```

    > [!NOTE]
    > <span data-ttu-id="d4ebb-154">Cela exclut uniquement les chemins d’accès d’un niveau inférieur *à /var/*, mais pas les dossiers qui sont imbrmbrés plus profondément ; par exemple, */var/this-subfolder/but-not-this-subfolder*.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-154">This will only exclude paths one level below */var/*, but not folders which are more deeply nested; for example, */var/this-subfolder/but-not-this-subfolder*.</span></span>
    
    ```bash
    mdatp exclusion folder add --path "/var/"
    ```
    > [!NOTE]
    > <span data-ttu-id="d4ebb-155">Cela exclut tous les chemins dont le parent *est /var/*; par exemple, */var/this-subfolder/and-this-subfolder-as-well*.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-155">This will exclude all paths whose parent is */var/*; for example, */var/this-subfolder/and-this-subfolder-as-well*.</span></span>

    ```Output
    Folder exclusion configured successfully
    ```

- <span data-ttu-id="d4ebb-156">Ajoutez une exclusion pour un processus :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-156">Add an exclusion for a process:</span></span>

    ```bash
    mdatp exclusion process add --name cat
    ```
    ```Output    
    Process exclusion configured successfully
    ```

## <a name="validate-exclusions-lists-with-the-eicar-test-file"></a><span data-ttu-id="d4ebb-157">Valider les listes d’exclusions avec le fichier de test EICAR</span><span class="sxs-lookup"><span data-stu-id="d4ebb-157">Validate exclusions lists with the EICAR test file</span></span>

<span data-ttu-id="d4ebb-158">Vous pouvez vérifier que vos listes d’exclusions fonctionnent à l’aide `curl` du téléchargement d’un fichier de test.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-158">You can validate that your exclusion lists are working by using `curl` to download a test file.</span></span>

<span data-ttu-id="d4ebb-159">Dans l’extrait de code Bash suivant, remplacez-le par un fichier conforme `test.txt` à vos règles d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-159">In the following Bash snippet, replace `test.txt` with a file that conforms to your exclusion rules.</span></span> <span data-ttu-id="d4ebb-160">Par exemple, si vous avez exclu `.testing` l’extension, `test.txt` remplacez par `test.testing` .</span><span class="sxs-lookup"><span data-stu-id="d4ebb-160">For example, if you have excluded the `.testing` extension, replace `test.txt` with `test.testing`.</span></span> <span data-ttu-id="d4ebb-161">Si vous testez un chemin d’accès, veillez à exécuter la commande dans ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-161">If you are testing a path, ensure that you run the command within that path.</span></span>

```bash
curl -o test.txt https://www.eicar.org/download/eicar.com.txt
```

<span data-ttu-id="d4ebb-162">Si Defender pour point de terminaison sur Linux signale un programme malveillant, la règle ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-162">If Defender for Endpoint on Linux reports malware, then the rule is not working.</span></span> <span data-ttu-id="d4ebb-163">Si aucun programme malveillant n’est détecté et que le fichier téléchargé existe, l’exclusion fonctionne.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-163">If there is no report of malware, and the downloaded file exists, then the exclusion is working.</span></span> <span data-ttu-id="d4ebb-164">Vous pouvez ouvrir le fichier pour vérifier que le contenu est identique à ce qui est décrit sur le site web du fichier [de test EICAR.](http://2016.eicar.org/86-0-Intended-use.html)</span><span class="sxs-lookup"><span data-stu-id="d4ebb-164">You can open the file to confirm that the contents are the same as what is described on the [EICAR test file website](http://2016.eicar.org/86-0-Intended-use.html).</span></span>

<span data-ttu-id="d4ebb-165">Si vous n’avez pas accès à Internet, vous pouvez créer votre propre fichier de test EICAR.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-165">If you do not have Internet access, you can create your own EICAR test file.</span></span> <span data-ttu-id="d4ebb-166">Écrivez la chaîne EICAR dans un nouveau fichier texte avec la commande Bash suivante :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-166">Write the EICAR string to a new text file with the following Bash command:</span></span>

```bash
echo 'X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*' > test.txt
```

<span data-ttu-id="d4ebb-167">Vous pouvez également copier la chaîne dans un fichier texte vierge et essayer de l’enregistrer avec le nom de fichier ou dans le dossier que vous tentez d’exclure.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-167">You can also copy the string into a blank text file and attempt to save it with the file name or in the folder you are attempting to exclude.</span></span>

## <a name="allow-threats"></a><span data-ttu-id="d4ebb-168">Autoriser les menaces</span><span class="sxs-lookup"><span data-stu-id="d4ebb-168">Allow threats</span></span>

<span data-ttu-id="d4ebb-169">En plus d’exclure certains contenus de l’analyse, vous pouvez également configurer le produit pour qu’il ne détecte pas certaines classes de menaces (identifiées par le nom de la menace).</span><span class="sxs-lookup"><span data-stu-id="d4ebb-169">In addition to excluding certain content from being scanned, you can also configure the product not to detect some classes of threats (identified by the threat name).</span></span> <span data-ttu-id="d4ebb-170">Vous devez faire preuve de prudence lors de l’utilisation de cette fonctionnalité, car elle peut laisser votre appareil non protégé.</span><span class="sxs-lookup"><span data-stu-id="d4ebb-170">You should exercise caution when using this functionality, as it can leave your device unprotected.</span></span>

<span data-ttu-id="d4ebb-171">Pour ajouter un nom de menace à la liste autorisée, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-171">To add a threat name to the allowed list, execute the following command:</span></span>

```bash
mdatp threat allowed add --name [threat-name]
```

<span data-ttu-id="d4ebb-172">Le nom de la menace associé à une détection sur votre appareil peut être obtenu à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-172">The threat name associated with a detection on your device can be obtained using the following command:</span></span>

```bash
mdatp threat list
```

<span data-ttu-id="d4ebb-173">Par exemple, pour ajouter (le nom de menace associé à la détection EICAR) à la liste `EICAR-Test-File (not a virus)` autorisée, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d4ebb-173">For example, to add `EICAR-Test-File (not a virus)` (the threat name associated with the EICAR detection) to the allowed list, execute the following command:</span></span>

```bash
mdatp threat allowed add --name "EICAR-Test-File (not a virus)"
```
