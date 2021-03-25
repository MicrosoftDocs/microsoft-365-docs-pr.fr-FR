---
title: Évaluer l’accès contrôlé aux dossiers
description: Découvrez comment l’accès contrôlé aux dossiers peut aider à empêcher les fichiers d’être modifiés par des applications malveillantes.
keywords: Exploit Protection, windows 10, windows defender, ransomware, protéger, évaluer, tester, démonstration, essayer
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
audience: ITPro
author: levinec
ms.author: ellevin
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: e965e1a882dadfb565231074165507a6727b45c1
ms.sourcegitcommit: 8685b0f7d53c99577fa65144ab60295dfa60f46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51218747"
---
# <a name="evaluate-controlled-folder-access"></a><span data-ttu-id="e27fc-104">Évaluer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="e27fc-104">Evaluate controlled folder access</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e27fc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e27fc-105">**Applies to:**</span></span>
- [<span data-ttu-id="e27fc-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e27fc-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="e27fc-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e27fc-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="e27fc-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e27fc-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e27fc-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e27fc-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)


<span data-ttu-id="e27fc-110">[L’accès contrôlé aux](controlled-folders.md) dossiers est une fonctionnalité qui permet de protéger vos documents et fichiers contre toute modification par des applications suspectes ou malveillantes.</span><span class="sxs-lookup"><span data-stu-id="e27fc-110">[Controlled folder access](controlled-folders.md) is a feature that helps protect your documents and files from modification by suspicious or malicious apps.</span></span> <span data-ttu-id="e27fc-111">L’accès contrôlé aux dossiers est pris en charge sur les clients Windows Server 2019 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e27fc-111">Controlled folder access is supported on Windows Server 2019 and Windows 10 clients.</span></span>

<span data-ttu-id="e27fc-112">Il est particulièrement utile pour vous protéger contre les [ransomware](https://www.microsoft.com/wdsi/threats/ransomware) qui tentent de chiffrer vos fichiers et de les maintenir en attente.</span><span class="sxs-lookup"><span data-stu-id="e27fc-112">It is especially useful in helping protect against [ransomware](https://www.microsoft.com/wdsi/threats/ransomware) that attempts to encrypt your files and hold them hostage.</span></span>

<span data-ttu-id="e27fc-113">Cet article vous aide à évaluer l’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="e27fc-113">This article helps you evaluate controlled folder access.</span></span> <span data-ttu-id="e27fc-114">Il explique comment activer le mode audit afin de pouvoir tester la fonctionnalité directement dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e27fc-114">It explains how to enable audit mode so you can test the feature directly in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="e27fc-115">Vous pouvez également consulter le site web du scénario de démonstration microsoft Defender pour point de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que la fonctionnalité fonctionne et voir comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e27fc-115">You can also visit the Microsoft Defender for Endpoint demo scenario website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the feature is working and see how it works.</span></span>

## <a name="use-audit-mode-to-measure-impact"></a><span data-ttu-id="e27fc-116">Utiliser le mode audit pour mesurer l’impact</span><span class="sxs-lookup"><span data-stu-id="e27fc-116">Use audit mode to measure impact</span></span>

<span data-ttu-id="e27fc-117">Activez l’accès contrôlé aux dossiers en  mode audit pour voir un enregistrement de ce qui se serait passé s’il était entièrement activé.</span><span class="sxs-lookup"><span data-stu-id="e27fc-117">Enable the controlled folder access in audit mode to see a record of what *would* have happened if it was fully enabled.</span></span> <span data-ttu-id="e27fc-118">Testez le fonctionnement de la fonctionnalité dans votre organisation pour vous assurer qu’elle n’affecte pas vos applications métier.</span><span class="sxs-lookup"><span data-stu-id="e27fc-118">Test how the feature will work in your organization to ensure it doesn't affect your line-of-business apps.</span></span> <span data-ttu-id="e27fc-119">Vous pouvez également avoir une idée du nombre de tentatives de modification de fichier suspectes qui se produisent généralement sur une certaine période de temps.</span><span class="sxs-lookup"><span data-stu-id="e27fc-119">You can also get an idea of how many suspicious file modification attempts generally occur over a certain period of time.</span></span>

<span data-ttu-id="e27fc-120">Pour activer le mode audit, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="e27fc-120">To enable audit mode, use the following PowerShell cmdlet:</span></span>

```PowerShell
Set-MpPreference -EnableControlledFolderAccess AuditMode
```

> [!TIP]
> <span data-ttu-id="e27fc-121">Si vous souhaitez auditer entièrement le fonctionnement de l’accès contrôlé aux dossiers dans votre organisation, vous devez utiliser un outil de gestion pour déployer ce paramètre sur les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="e27fc-121">If you want to fully audit how controlled folder access will work in your organization, you'll need to use a management tool to deploy this setting to devices in your network(s).</span></span>
<span data-ttu-id="e27fc-122">Vous pouvez également utiliser la stratégie de groupe, Intune, la gestion des périphériques mobiles (MDM) ou Microsoft Endpoint Manager pour configurer et déployer le paramètre, comme décrit dans la rubrique principale d’accès contrôlé aux [dossiers.](controlled-folders.md)</span><span class="sxs-lookup"><span data-stu-id="e27fc-122">You can also use Group Policy, Intune, mobile device management (MDM), or Microsoft Endpoint Manager to configure and deploy the setting, as described in the main [controlled folder access topic](controlled-folders.md).</span></span>

## <a name="review-controlled-folder-access-events-in-windows-event-viewer"></a><span data-ttu-id="e27fc-123">Passer en revue les événements d’accès contrôlé aux dossiers dans l’Observateur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="e27fc-123">Review controlled folder access events in Windows Event Viewer</span></span>

<span data-ttu-id="e27fc-124">Les événements d’accès contrôlé aux dossiers suivants apparaissent dans l’Observateur d’événements Windows sous Le dossier Microsoft/Windows/Windows Defender/Opérationnel.</span><span class="sxs-lookup"><span data-stu-id="e27fc-124">The following controlled folder access events appear in Windows Event Viewer under Microsoft/Windows/Windows Defender/Operational folder.</span></span>

<span data-ttu-id="e27fc-125">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="e27fc-125">Event ID</span></span> | <span data-ttu-id="e27fc-126">Description</span><span class="sxs-lookup"><span data-stu-id="e27fc-126">Description</span></span>
-|-
 <span data-ttu-id="e27fc-127">5007</span><span class="sxs-lookup"><span data-stu-id="e27fc-127">5007</span></span> | <span data-ttu-id="e27fc-128">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="e27fc-128">Event when settings are changed</span></span>
 <span data-ttu-id="e27fc-129">1124</span><span class="sxs-lookup"><span data-stu-id="e27fc-129">1124</span></span> | <span data-ttu-id="e27fc-130">Événement d’accès contrôlé aux dossiers audité</span><span class="sxs-lookup"><span data-stu-id="e27fc-130">Audited controlled folder access event</span></span>
 <span data-ttu-id="e27fc-131">1123</span><span class="sxs-lookup"><span data-stu-id="e27fc-131">1123</span></span> | <span data-ttu-id="e27fc-132">Événement d’accès contrôlé aux dossiers bloqué</span><span class="sxs-lookup"><span data-stu-id="e27fc-132">Blocked controlled folder access event</span></span>

> [!TIP]
> <span data-ttu-id="e27fc-133">Vous pouvez configurer un abonnement [windows Event Forwarding](https://docs.microsoft.com/windows/win32/wec/setting-up-a-source-initiated-subscription) pour collecter les journaux de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="e27fc-133">You can configure a [Windows Event Forwarding subscription](https://docs.microsoft.com/windows/win32/wec/setting-up-a-source-initiated-subscription) to collect the logs centrally.</span></span> 

## <a name="customize-protected-folders-and-apps"></a><span data-ttu-id="e27fc-134">Personnaliser les applications et les dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="e27fc-134">Customize protected folders and apps</span></span>

<span data-ttu-id="e27fc-135">Au cours de votre évaluation, vous pouvez ajouter des fichiers à la liste des dossiers protégés ou autoriser certaines applications à modifier des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e27fc-135">During your evaluation, you may wish to add to the list of protected folders, or allow certain apps to modify files.</span></span>

<span data-ttu-id="e27fc-136">Voir [Protéger les dossiers](controlled-folders.md) importants avec un accès contrôlé aux dossiers pour configurer la fonctionnalité à l’aide des outils de gestion, notamment la stratégie de groupe, PowerShell et les fournisseurs de services de configuration (CSP) DE GESTION.</span><span class="sxs-lookup"><span data-stu-id="e27fc-136">See [Protect important folders with controlled folder access](controlled-folders.md) for configuring the feature with management tools, including Group Policy, PowerShell, and MDM configuration service providers (CSPs).</span></span>

## <a name="see-also"></a><span data-ttu-id="e27fc-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e27fc-137">See also</span></span>

* [<span data-ttu-id="e27fc-138">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="e27fc-138">Protect important folders with controlled folder access</span></span>](controlled-folders.md)
* [<span data-ttu-id="e27fc-139">Évaluer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e27fc-139">Evaluate Microsoft Defender for Endpoint</span></span>](evaluate-mde.md)
* [<span data-ttu-id="e27fc-140">Utiliser le mode audit</span><span class="sxs-lookup"><span data-stu-id="e27fc-140">Use audit mode</span></span>](audit-windows-defender.md)
