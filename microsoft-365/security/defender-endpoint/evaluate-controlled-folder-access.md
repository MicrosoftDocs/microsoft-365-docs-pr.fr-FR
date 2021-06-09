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
author: dansimp
ms.author: dansimp
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 15ea4696052a6c987314e3c7b0dd282a49ed4df8
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842913"
---
# <a name="evaluate-controlled-folder-access"></a><span data-ttu-id="d32c8-104">Évaluer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="d32c8-104">Evaluate controlled folder access</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d32c8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d32c8-105">**Applies to:**</span></span>
- [<span data-ttu-id="d32c8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d32c8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="d32c8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d32c8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="d32c8-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d32c8-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d32c8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d32c8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)


<span data-ttu-id="d32c8-110">[L’accès contrôlé aux](controlled-folders.md) dossiers est une fonctionnalité qui permet de protéger vos documents et fichiers contre toute modification par des applications suspectes ou malveillantes.</span><span class="sxs-lookup"><span data-stu-id="d32c8-110">[Controlled folder access](controlled-folders.md) is a feature that helps protect your documents and files from modification by suspicious or malicious apps.</span></span> <span data-ttu-id="d32c8-111">L’accès contrôlé aux dossiers est pris en charge Windows Server 2019 et Windows 10 clients.</span><span class="sxs-lookup"><span data-stu-id="d32c8-111">Controlled folder access is supported on Windows Server 2019 and Windows 10 clients.</span></span>

<span data-ttu-id="d32c8-112">Il est particulièrement utile pour vous protéger contre les [ransomware](https://www.microsoft.com/wdsi/threats/ransomware) qui tentent de chiffrer vos fichiers et de les maintenir en attente.</span><span class="sxs-lookup"><span data-stu-id="d32c8-112">It is especially useful in helping protect against [ransomware](https://www.microsoft.com/wdsi/threats/ransomware) that attempts to encrypt your files and hold them hostage.</span></span>

<span data-ttu-id="d32c8-113">Cet article vous aide à évaluer l’accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="d32c8-113">This article helps you evaluate controlled folder access.</span></span> <span data-ttu-id="d32c8-114">Il explique comment activer le mode audit afin de pouvoir tester la fonctionnalité directement dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d32c8-114">It explains how to enable audit mode so you can test the feature directly in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="d32c8-115">Vous pouvez également consulter le site web du scénario de démonstration microsoft Defender pour point de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que la fonctionnalité fonctionne et voir comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="d32c8-115">You can also visit the Microsoft Defender for Endpoint demo scenario website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the feature is working and see how it works.</span></span>

## <a name="use-audit-mode-to-measure-impact"></a><span data-ttu-id="d32c8-116">Utiliser le mode audit pour mesurer l’impact</span><span class="sxs-lookup"><span data-stu-id="d32c8-116">Use audit mode to measure impact</span></span>

<span data-ttu-id="d32c8-117">Activez l’accès contrôlé aux dossiers en  mode audit pour voir un enregistrement de ce qui se serait passé s’il était entièrement activé.</span><span class="sxs-lookup"><span data-stu-id="d32c8-117">Enable the controlled folder access in audit mode to see a record of what *would* have happened if it was fully enabled.</span></span> <span data-ttu-id="d32c8-118">Testez le fonctionnement de la fonctionnalité dans votre organisation pour vous assurer qu’elle n’affecte pas vos applications métier.</span><span class="sxs-lookup"><span data-stu-id="d32c8-118">Test how the feature will work in your organization to ensure it doesn't affect your line-of-business apps.</span></span> <span data-ttu-id="d32c8-119">Vous pouvez également avoir une idée du nombre de tentatives de modification de fichier suspectes qui se produisent généralement sur une certaine période de temps.</span><span class="sxs-lookup"><span data-stu-id="d32c8-119">You can also get an idea of how many suspicious file modification attempts generally occur over a certain period of time.</span></span>

<span data-ttu-id="d32c8-120">Pour activer le mode audit, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="d32c8-120">To enable audit mode, use the following PowerShell cmdlet:</span></span>

```PowerShell
Set-MpPreference -EnableControlledFolderAccess AuditMode
```

> [!TIP]
> <span data-ttu-id="d32c8-121">Si vous souhaitez auditer entièrement le fonctionnement de l’accès contrôlé aux dossiers dans votre organisation, vous devez utiliser un outil de gestion pour déployer ce paramètre sur les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="d32c8-121">If you want to fully audit how controlled folder access will work in your organization, you'll need to use a management tool to deploy this setting to devices in your network(s).</span></span>
<span data-ttu-id="d32c8-122">Vous pouvez également utiliser une stratégie de groupe, Intune, la gestion des périphériques mobiles (MDM) ou des Microsoft Endpoint Manager pour configurer et déployer le paramètre, comme décrit dans la rubrique principale d’accès contrôlé aux [dossiers.](controlled-folders.md)</span><span class="sxs-lookup"><span data-stu-id="d32c8-122">You can also use Group Policy, Intune, mobile device management (MDM), or Microsoft Endpoint Manager to configure and deploy the setting, as described in the main [controlled folder access topic](controlled-folders.md).</span></span>

## <a name="review-controlled-folder-access-events-in-windows-event-viewer"></a><span data-ttu-id="d32c8-123">Passer en revue les événements d’accès contrôlé aux dossiers dans Windows’observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="d32c8-123">Review controlled folder access events in Windows Event Viewer</span></span>

<span data-ttu-id="d32c8-124">Les événements d’accès contrôlé aux dossiers suivants apparaissent dans Windows’Observateur d’événements sous Microsoft/Windows/Windows Defender/Opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d32c8-124">The following controlled folder access events appear in Windows Event Viewer under Microsoft/Windows/Windows Defender/Operational folder.</span></span>

<span data-ttu-id="d32c8-125">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="d32c8-125">Event ID</span></span> | <span data-ttu-id="d32c8-126">Description</span><span class="sxs-lookup"><span data-stu-id="d32c8-126">Description</span></span>
-|-
 <span data-ttu-id="d32c8-127">5007</span><span class="sxs-lookup"><span data-stu-id="d32c8-127">5007</span></span> | <span data-ttu-id="d32c8-128">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="d32c8-128">Event when settings are changed</span></span>
 <span data-ttu-id="d32c8-129">1124</span><span class="sxs-lookup"><span data-stu-id="d32c8-129">1124</span></span> | <span data-ttu-id="d32c8-130">Événement d’accès contrôlé aux dossiers audité</span><span class="sxs-lookup"><span data-stu-id="d32c8-130">Audited controlled folder access event</span></span>
 <span data-ttu-id="d32c8-131">1123</span><span class="sxs-lookup"><span data-stu-id="d32c8-131">1123</span></span> | <span data-ttu-id="d32c8-132">Événement d’accès contrôlé aux dossiers bloqué</span><span class="sxs-lookup"><span data-stu-id="d32c8-132">Blocked controlled folder access event</span></span>

> [!TIP]
> <span data-ttu-id="d32c8-133">Vous pouvez configurer un abonnement [au Windows de](/windows/win32/wec/setting-up-a-source-initiated-subscription) l’événement pour collecter les journaux de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="d32c8-133">You can configure a [Windows Event Forwarding subscription](/windows/win32/wec/setting-up-a-source-initiated-subscription) to collect the logs centrally.</span></span> 

## <a name="customize-protected-folders-and-apps"></a><span data-ttu-id="d32c8-134">Personnaliser les applications et les dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="d32c8-134">Customize protected folders and apps</span></span>

<span data-ttu-id="d32c8-135">Au cours de votre évaluation, vous pouvez ajouter des fichiers à la liste des dossiers protégés ou autoriser certaines applications à modifier des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d32c8-135">During your evaluation, you may wish to add to the list of protected folders, or allow certain apps to modify files.</span></span>

<span data-ttu-id="d32c8-136">Voir [Protéger les dossiers](controlled-folders.md) importants avec accès contrôlé aux dossiers pour configurer la fonctionnalité à l’aide d’outils de gestion, y compris la stratégie de groupe, PowerShell et les fournisseurs de services de configuration (CSP) DE GESTION.</span><span class="sxs-lookup"><span data-stu-id="d32c8-136">See [Protect important folders with controlled folder access](controlled-folders.md) for configuring the feature with management tools, including Group Policy, PowerShell, and MDM configuration service providers (CSPs).</span></span>

## <a name="see-also"></a><span data-ttu-id="d32c8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d32c8-137">See also</span></span>

* [<span data-ttu-id="d32c8-138">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="d32c8-138">Protect important folders with controlled folder access</span></span>](controlled-folders.md)
* [<span data-ttu-id="d32c8-139">Évaluer Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d32c8-139">Evaluate Microsoft Defender for Endpoint</span></span>](evaluate-mde.md)
* [<span data-ttu-id="d32c8-140">Utiliser le mode Audit</span><span class="sxs-lookup"><span data-stu-id="d32c8-140">Use audit mode</span></span>](audit-windows-defender.md)
