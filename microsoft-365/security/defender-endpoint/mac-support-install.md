---
title: Résoudre les problèmes d'installation de Microsoft Defender pour Endpoint pour Mac
description: Résolution des problèmes d'installation dans Microsoft Defender pour Point de terminaison pour Mac.
keywords: microsoft, defender, atp, mac, install
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
ms.openlocfilehash: d2ad3160c9f36a27dc98f44365433de5f8b26bb2
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51861430"
---
# <a name="troubleshoot-installation-issues-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="55cc1-104">Résoudre les problèmes d'installation de Microsoft Defender pour endpoint sur macOS</span><span class="sxs-lookup"><span data-stu-id="55cc1-104">Troubleshoot installation issues for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="55cc1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="55cc1-105">**Applies to:**</span></span>

- [<span data-ttu-id="55cc1-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="55cc1-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="55cc1-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="55cc1-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="55cc1-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="55cc1-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="55cc1-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="55cc1-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="55cc1-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="55cc1-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="installation-failed"></a><span data-ttu-id="55cc1-111">Échec de l'installation</span><span class="sxs-lookup"><span data-stu-id="55cc1-111">Installation failed</span></span>

<span data-ttu-id="55cc1-112">Pour l'installation manuelle, la page Résumé de l'Assistant d'installation indique : « Une erreur s'est produite lors de l'installation.</span><span class="sxs-lookup"><span data-stu-id="55cc1-112">For manual installation, the Summary page of the installation wizard says, "An error occurred during installation.</span></span> <span data-ttu-id="55cc1-113">Le programme d'installation a rencontré une erreur qui a provoqué l'échec de l'installation.</span><span class="sxs-lookup"><span data-stu-id="55cc1-113">The Installer encountered an error that caused the installation to fail.</span></span> <span data-ttu-id="55cc1-114">Contactez le fabricant du logiciel pour obtenir de l'aide. »</span><span class="sxs-lookup"><span data-stu-id="55cc1-114">Contact the software manufacturer for assistance."</span></span> <span data-ttu-id="55cc1-115">Pour les déploiements mdm, il s'affiche également comme un échec d'installation générique.</span><span class="sxs-lookup"><span data-stu-id="55cc1-115">For MDM deployments, it displays as a generic installation failure as well.</span></span>

<span data-ttu-id="55cc1-116">Bien que nous n'affichions pas une erreur exacte à l'utilisateur final, nous tenez un fichier journal avec la progression de l'installation dans `/Library/Logs/Microsoft/mdatp/install.log` .</span><span class="sxs-lookup"><span data-stu-id="55cc1-116">While we do not display an exact error to the end user, we keep a log file with installation progress in `/Library/Logs/Microsoft/mdatp/install.log`.</span></span> <span data-ttu-id="55cc1-117">Chaque session d'installation s'y connecte.</span><span class="sxs-lookup"><span data-stu-id="55cc1-117">Each installation session appends to this log file.</span></span> <span data-ttu-id="55cc1-118">Vous pouvez utiliser la `sed` sortie de la dernière session d'installation uniquement :</span><span class="sxs-lookup"><span data-stu-id="55cc1-118">You can use `sed` to output the last installation session only:</span></span>

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

<span data-ttu-id="55cc1-119">Dans cet exemple, la raison réelle est précédée du `[ERROR]` préfixe .</span><span class="sxs-lookup"><span data-stu-id="55cc1-119">In this example, the actual reason is prefixed with `[ERROR]`.</span></span>
<span data-ttu-id="55cc1-120">L'installation a échoué car une mise à niveau vers une version antérieure entre ces versions n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="55cc1-120">The installation failed because a downgrade between these versions is not supported.</span></span>

## <a name="mdatp-install-log-missing-or-not-updated"></a><span data-ttu-id="55cc1-121">Journal d'installation MDATP manquant ou non mis à jour</span><span class="sxs-lookup"><span data-stu-id="55cc1-121">MDATP install log missing or not updated</span></span>

<span data-ttu-id="55cc1-122">Dans de rares cas, l'installation ne laisse aucune trace dans le fichier /Library/Logs/Microsoft/mdatp/install.log de MDATP.</span><span class="sxs-lookup"><span data-stu-id="55cc1-122">In rare cases, installation leaves no trace in MDATP's /Library/Logs/Microsoft/mdatp/install.log file.</span></span>
<span data-ttu-id="55cc1-123">Vous pouvez vérifier qu'une installation s'est produite et analyser les erreurs possibles en interrogeant les journaux macOS (cela est utile dans le déploiement mdm, lorsqu'il n'y a pas d'interface utilisateur client).</span><span class="sxs-lookup"><span data-stu-id="55cc1-123">You can verify that an installation happened and analyze possible errors by querying macOS logs (this is helpful in MDM deployment, when there is no client UI).</span></span> <span data-ttu-id="55cc1-124">Nous vous recommandons d'utiliser une fenêtre de temps étroite pour exécuter une requête et de filtrer par nom de processus de journalisation, car il y aura une quantité considérable d'informations.</span><span class="sxs-lookup"><span data-stu-id="55cc1-124">We recommend that you use a narrow time window to run a query, and that you filter by the logging process name, as there will be a huge amount of information.</span></span>

```bash
grep '^2020-03-11 13:08' /var/log/install.log
```
```Output
log show --start '2020-03-11 13:00:00' --end '2020-03-11 13:08:50' --info --debug --source --predicate 'processImagePath CONTAINS[C] "install"' --style syslog
```
