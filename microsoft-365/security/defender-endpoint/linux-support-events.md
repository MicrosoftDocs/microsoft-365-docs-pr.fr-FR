---
title: Résoudre les problèmes d’événements ou d’alertes manquants pour Microsoft Defender pour endpoint sur Linux
description: Résoudre les problèmes d’événements ou d’alertes manquants dans Microsoft Defender pour Endpoint sur Linux.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, événements
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
mms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 7de216c1397a7cc4806af8221257eeedd2290830
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933312"
---
# <a name="troubleshoot-missing-events-or-alerts-issues-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="04fed-104">Résoudre les problèmes d’événements ou d’alertes manquants pour Microsoft Defender pour endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="04fed-104">Troubleshoot missing events or alerts issues for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="04fed-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="04fed-105">**Applies to:**</span></span>

- [<span data-ttu-id="04fed-106">Microsoft Defender pour point de terminaison Linux</span><span class="sxs-lookup"><span data-stu-id="04fed-106">Microsoft Defender for Endpoint on Linux</span></span>](microsoft-defender-endpoint-linux.md)

<span data-ttu-id="04fed-107">Cet article fournit quelques étapes générales pour atténuer les événements ou alertes manquants dans le portail [du centre de](https://securitycenter.windows.com/) sécurité.</span><span class="sxs-lookup"><span data-stu-id="04fed-107">This article provides some general steps to mitigate missing events or alerts in the [security center](https://securitycenter.windows.com/) portal.</span></span>

<span data-ttu-id="04fed-108">Une **fois que Microsoft Defender pour le point** de terminaison a été correctement installé sur un appareil, une _page_ d’appareil est générée dans le portail.</span><span class="sxs-lookup"><span data-stu-id="04fed-108">Once **Microsoft Defender for Endpoint** has been installed properly on a device, a _device page_ will be generated in the portal.</span></span> <span data-ttu-id="04fed-109">Vous pouvez passer en revue tous les événements enregistrés dans l’onglet Chronologie de la page de l’appareil ou dans la page de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="04fed-109">You can review all recorded events in the timeline tab in the device page, or in advanced hunting page.</span></span> <span data-ttu-id="04fed-110">Cette section permet de résoudre les problèmes de certains événements attendus ou de tous.</span><span class="sxs-lookup"><span data-stu-id="04fed-110">This section troubleshoots the case of some or all expected events are missing.</span></span>
<span data-ttu-id="04fed-111">Par exemple, si tous _les événements CreatedFile_ sont manquants.</span><span class="sxs-lookup"><span data-stu-id="04fed-111">For instance, if all _CreatedFile_ events are missing.</span></span>

## <a name="missing-network-and-login-events"></a><span data-ttu-id="04fed-112">Événements réseau et de connexion manquants</span><span class="sxs-lookup"><span data-stu-id="04fed-112">Missing network and login events</span></span>

<span data-ttu-id="04fed-113">Microsoft Defender pour le point de terminaison a utilisé `audit` l’infrastructure linux pour suivre l’activité réseau et de connexion.</span><span class="sxs-lookup"><span data-stu-id="04fed-113">Microsoft Defender for Endpoint utilized `audit` framework from linux to track network and login activity.</span></span>

1. <span data-ttu-id="04fed-114">Assurez-vous que l’infrastructure d’audit fonctionne.</span><span class="sxs-lookup"><span data-stu-id="04fed-114">Make sure audit framework is working.</span></span>

    ```bash
    service auditd status
    ```

    <span data-ttu-id="04fed-115">sortie attendue :</span><span class="sxs-lookup"><span data-stu-id="04fed-115">expected output:</span></span>

    ```output
    ● auditd.service - Security Auditing Service
    Loaded: loaded (/usr/lib/systemd/system/auditd.service; enabled; vendor preset: enabled)
    Active: active (running) since Mon 2020-12-21 10:48:02 IST; 2 weeks 0 days ago
        Docs: man:auditd(8)
            https://github.com/linux-audit/audit-documentation
    Process: 16689 ExecStartPost=/sbin/augenrules --load (code=exited, status=1/FAILURE)
    Process: 16665 ExecStart=/sbin/auditd (code=exited, status=0/SUCCESS)
    Main PID: 16666 (auditd)
        Tasks: 25
    CGroup: /system.slice/auditd.service
            ├─16666 /sbin/auditd
            ├─16668 /sbin/audispd
            ├─16670 /usr/sbin/sedispatch
            └─16671 /opt/microsoft/mdatp/sbin/mdatp_audisp_plugin -d
    ```

2. <span data-ttu-id="04fed-116">Si `auditd` elle est marquée comme arrêtée, démarrez-la.</span><span class="sxs-lookup"><span data-stu-id="04fed-116">If `auditd` is marked as stopped, start it.</span></span>

    ```bash
    service auditd start
    ```

<span data-ttu-id="04fed-117">**Sur les systèmes SLES,** l’audit SYSCALL peut être désactivé par défaut et peut être tenu compte des `auditd` événements manquants.</span><span class="sxs-lookup"><span data-stu-id="04fed-117">**On SLES** systems, SYSCALL auditing in `auditd` might be disabled by default and can be accounted for missing events.</span></span>

1. <span data-ttu-id="04fed-118">Pour vérifier que l’audit SYSCALL n’est pas désactivé, listez les règles d’audit actuelles :</span><span class="sxs-lookup"><span data-stu-id="04fed-118">To validate that SYSCALL auditing is not disabled, list the current audit rules:</span></span>

    ```bash
    sudo auditctl -l
    ```

    <span data-ttu-id="04fed-119">si la ligne suivante est présente, supprimez-la ou modifiez-la pour permettre à Microsoft Defender for Endpoint de suivre des SYSCALL spécifiques.</span><span class="sxs-lookup"><span data-stu-id="04fed-119">if the following line is present, remove it or edit it to enable Microsoft Defender for Endpoint to track specific SYSCALLs.</span></span>

    ```output
    -a task, never
    ```

    <span data-ttu-id="04fed-120">les règles d’audit se trouvent à `/etc/audit/rules.d/audit.rules` l’emplacement .</span><span class="sxs-lookup"><span data-stu-id="04fed-120">audit rules are located at `/etc/audit/rules.d/audit.rules`.</span></span>

## <a name="missing-file-events"></a><span data-ttu-id="04fed-121">Événements de fichier manquants</span><span class="sxs-lookup"><span data-stu-id="04fed-121">Missing file events</span></span>

<span data-ttu-id="04fed-122">Les événements de fichier sont collectés avec `fanotify` l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="04fed-122">File events are collected with `fanotify` framework.</span></span> <span data-ttu-id="04fed-123">Si certains événements de fichier ou tous sont manquants, assurez-vous qu’il est activé sur l’appareil et que le système `fanotify` de fichiers est pris en [charge.](microsoft-defender-endpoint-linux.md#system-requirements)</span><span class="sxs-lookup"><span data-stu-id="04fed-123">In case some or all file events are missing, make sure `fanotify` is enabled on the device and that the file system is [supported](microsoft-defender-endpoint-linux.md#system-requirements).</span></span>

<span data-ttu-id="04fed-124">List the filesystems on the machine with:</span><span class="sxs-lookup"><span data-stu-id="04fed-124">List the filesystems on the machine with:</span></span>

```bash
df -Th
```
