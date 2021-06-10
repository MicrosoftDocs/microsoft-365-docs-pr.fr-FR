---
title: Résoudre les problèmes d’installation de Microsoft Defender pour Endpoint sur Mac
description: Résolution des problèmes d’installation dans Microsoft Defender pour point de terminaison sur Mac.
keywords: microsoft, defender, Microsoft Defender for Endpoint, mac, install
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
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 5166de3a7c7017979a93ac7026636ba24671892e
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935148"
---
# <a name="troubleshoot-installation-issues-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="8ac55-104">Résoudre les problèmes d’installation de Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="8ac55-104">Troubleshoot installation issues for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8ac55-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8ac55-105">**Applies to:**</span></span>

- [<span data-ttu-id="8ac55-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="8ac55-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="8ac55-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8ac55-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="8ac55-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8ac55-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="8ac55-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8ac55-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8ac55-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8ac55-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="installation-failed"></a><span data-ttu-id="8ac55-111">Échec de l’installation</span><span class="sxs-lookup"><span data-stu-id="8ac55-111">Installation failed</span></span>

<span data-ttu-id="8ac55-112">Pour l’installation manuelle, la page Résumé de l’Assistant d’installation indique : « Une erreur s’est produite lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="8ac55-112">For manual installation, the Summary page of the installation wizard says, "An error occurred during installation.</span></span> <span data-ttu-id="8ac55-113">Le programme d’installation a rencontré une erreur qui a provoqué l’échec de l’installation.</span><span class="sxs-lookup"><span data-stu-id="8ac55-113">The Installer encountered an error that caused the installation to fail.</span></span> <span data-ttu-id="8ac55-114">Contactez le fabricant du logiciel pour obtenir de l’aide. »</span><span class="sxs-lookup"><span data-stu-id="8ac55-114">Contact the software manufacturer for assistance."</span></span> <span data-ttu-id="8ac55-115">Pour les déploiements mdm, il s’affiche également comme un échec d’installation générique.</span><span class="sxs-lookup"><span data-stu-id="8ac55-115">For MDM deployments, it displays as a generic installation failure as well.</span></span>

<span data-ttu-id="8ac55-116">Bien que nous n’affichions pas une erreur exacte à l’utilisateur final, nous tenez un fichier journal avec la progression de l’installation dans `/Library/Logs/Microsoft/mdatp/install.log` .</span><span class="sxs-lookup"><span data-stu-id="8ac55-116">While we do not display an exact error to the end user, we keep a log file with installation progress in `/Library/Logs/Microsoft/mdatp/install.log`.</span></span> <span data-ttu-id="8ac55-117">Chaque session d’installation s’y connecte.</span><span class="sxs-lookup"><span data-stu-id="8ac55-117">Each installation session appends to this log file.</span></span> <span data-ttu-id="8ac55-118">Vous pouvez utiliser la `sed` sortie de la dernière session d’installation uniquement :</span><span class="sxs-lookup"><span data-stu-id="8ac55-118">You can use `sed` to output the last installation session only:</span></span>

```bash
sed -n 'H; /^preinstall com.microsoft.wdav begin/h; ${g;p;}' /Library/Logs/Microsoft/mdatp/install.log
```
```Output
preinstall com.microsoft.wdav begin [2020-03-11 13:08:49 -0700] 804
INSTALLER_SECURE_TEMP=/Library/InstallerSandboxes/.PKInstallSandboxManager/CB509765-70FC-4679-866D-8A14AD3F13CC.activeSandbox/89FA879B-971B-42BF-B4EA-7F5BB7CB5695
correlation id=CB509765-70FC-4679-866D-8A14AD3F13CC
[ERROR] Downgrade from 100.88.54 to 100.87.80 is not permitted
preinstall com.microsoft.wdav end [2020-03-11 13:08:49 -0700] 804 => 1
```

<span data-ttu-id="8ac55-119">Dans cet exemple, la raison réelle est précédée du `[ERROR]` préfixe .</span><span class="sxs-lookup"><span data-stu-id="8ac55-119">In this example, the actual reason is prefixed with `[ERROR]`.</span></span>
<span data-ttu-id="8ac55-120">L’installation a échoué car une mise à niveau vers une version antérieure entre ces versions n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8ac55-120">The installation failed because a downgrade between these versions is not supported.</span></span>

## <a name="mdatp-install-log-missing-or-not-updated"></a><span data-ttu-id="8ac55-121">MDATP journal d’installation manquant ou non mis à jour</span><span class="sxs-lookup"><span data-stu-id="8ac55-121">MDATP install log missing or not updated</span></span>

<span data-ttu-id="8ac55-122">Dans de rares cas, l’installation ne laisse aucune trace dans MDATP fichier /Library/Logs/Microsoft/mdatp/install.log.</span><span class="sxs-lookup"><span data-stu-id="8ac55-122">In rare cases, installation leaves no trace in MDATP's /Library/Logs/Microsoft/mdatp/install.log file.</span></span>
<span data-ttu-id="8ac55-123">Vous pouvez vérifier qu’une installation s’est produite et analyser les erreurs possibles en interrogeant les journaux macOS (cela est utile dans le déploiement mdm, lorsqu’il n’y a pas d’interface utilisateur client).</span><span class="sxs-lookup"><span data-stu-id="8ac55-123">You can verify that an installation happened and analyze possible errors by querying macOS logs (this is helpful in MDM deployment, when there is no client UI).</span></span> <span data-ttu-id="8ac55-124">Nous vous recommandons d’utiliser une fenêtre de temps étroite pour exécuter une requête et de filtrer par nom de processus de journalisation, car il y aura une quantité considérable d’informations.</span><span class="sxs-lookup"><span data-stu-id="8ac55-124">We recommend that you use a narrow time window to run a query, and that you filter by the logging process name, as there will be a huge amount of information.</span></span>

```bash
grep '^2020-03-11 13:08' /var/log/install.log
```
```Output
log show --start '2020-03-11 13:00:00' --end '2020-03-11 13:08:50' --info --debug --source --predicate 'processImagePath CONTAINS[C] "install"' --style syslog
```
