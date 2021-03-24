---
title: Évaluer la protection du réseau
description: Découvrez le fonctionnement de la protection réseau en testant les scénarios courants contre qui elle est protégée.
keywords: Protection du réseau, attaques, site web malveillant, ip, domaine, domaines, évaluer, tester, démonstration
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
ms.openlocfilehash: 41d1c9400720e20185922a97463e776c3ce0d80a
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064193"
---
# <a name="evaluate-network-protection"></a><span data-ttu-id="4f19c-104">Évaluer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="4f19c-104">Evaluate network protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4f19c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4f19c-105">**Applies to:**</span></span>
- [<span data-ttu-id="4f19c-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4f19c-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- - [<span data-ttu-id="4f19c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4f19c-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="4f19c-108">[La protection du](network-protection.md) réseau empêche les employés d’utiliser n’importe quelle application pour accéder à des domaines dangereux qui peuvent héberger des tentatives d’hameçonnage, des attaques et d’autres contenus malveillants sur Internet.</span><span class="sxs-lookup"><span data-stu-id="4f19c-108">[Network protection](network-protection.md) helps prevent employees from using any application to access dangerous domains that may host phishing scams, exploits, and other malicious content on the Internet.</span></span>

<span data-ttu-id="4f19c-109">Cet article vous aide à évaluer la protection du réseau en activant la fonctionnalité et en vous guidant vers un site de test.</span><span class="sxs-lookup"><span data-stu-id="4f19c-109">This article helps you evaluate network protection by enabling the feature and guiding you to a testing site.</span></span> <span data-ttu-id="4f19c-110">Les sites de cet article d’évaluation ne sont pas malveillants.</span><span class="sxs-lookup"><span data-stu-id="4f19c-110">The sites in this evaluation article aren't malicious.</span></span> <span data-ttu-id="4f19c-111">Ce sont des sites web spécialement créés qui prétendent être malveillants.</span><span class="sxs-lookup"><span data-stu-id="4f19c-111">They're specially created websites that pretend to be malicious.</span></span> <span data-ttu-id="4f19c-112">Le site réplique le comportement qui se produit si un utilisateur a visité un site ou un domaine malveillant.</span><span class="sxs-lookup"><span data-stu-id="4f19c-112">The site will replicate the behavior that would happen if a user visited a malicious site or domain.</span></span>

> [!TIP]
> <span data-ttu-id="4f19c-113">Vous pouvez également consulter le site Web Microsoft Defender Testground [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour voir comment fonctionnent les autres fonctionnalités de protection.</span><span class="sxs-lookup"><span data-stu-id="4f19c-113">You can also visit the Microsoft Defender Testground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to see how other protection features work.</span></span>

## <a name="enable-network-protection-in-audit-mode"></a><span data-ttu-id="4f19c-114">Activer la protection réseau en mode audit</span><span class="sxs-lookup"><span data-stu-id="4f19c-114">Enable network protection in audit mode</span></span>

<span data-ttu-id="4f19c-115">Activez la protection réseau en mode audit pour voir les adresses IP et les domaines qui auraient été bloqués.</span><span class="sxs-lookup"><span data-stu-id="4f19c-115">Enable network protection in audit mode to see which IP addresses and domains would have been blocked.</span></span> <span data-ttu-id="4f19c-116">Vous pouvez vous assurer qu’elle n’affecte pas les applications métiers ou qu’elle vous donne une idée de la fréquence des blocages.</span><span class="sxs-lookup"><span data-stu-id="4f19c-116">You can make sure it doesn't affect line-of-business apps, or get an idea of how often blocks occur.</span></span>

1. <span data-ttu-id="4f19c-117">Tapez **powershell** dans le menu Démarrer, cliquez avec le **bouton droit** sur Windows PowerShell puis **sélectionnez Exécuter en tant qu’administrateur**</span><span class="sxs-lookup"><span data-stu-id="4f19c-117">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**</span></span>
2. <span data-ttu-id="4f19c-118">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="4f19c-118">Enter the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -EnableNetworkProtection AuditMode
    ```

### <a name="visit-a-fake-malicious-domain"></a><span data-ttu-id="4f19c-119">Visiter un (faux) domaine malveillant</span><span class="sxs-lookup"><span data-stu-id="4f19c-119">Visit a (fake) malicious domain</span></span>

1. <span data-ttu-id="4f19c-120">Ouvrez Internet Explorer, Google Chrome ou tout autre navigateur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="4f19c-120">Open Internet Explorer, Google Chrome, or any other browser of your choice.</span></span>

1. <span data-ttu-id="4f19c-121">Accédez à [https://smartscreentestratings2.net](https://smartscreentestratings2.net).</span><span class="sxs-lookup"><span data-stu-id="4f19c-121">Go to [https://smartscreentestratings2.net](https://smartscreentestratings2.net).</span></span>

<span data-ttu-id="4f19c-122">La connexion réseau est autorisée et un message de test s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4f19c-122">The network connection will be allowed and a test message will be displayed.</span></span>

![Exemple de notification qui indique connexion bloquée : votre administrateur informatique a empêché la sécurité Windows de bloquer cette connexion réseau.](/microsoft-365/security/defender-endpoint/images/np-notif)

## <a name="review-network-protection-events-in-windows-event-viewer"></a><span data-ttu-id="4f19c-125">Passer en revue les événements de protection réseau dans l’Observateur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="4f19c-125">Review network protection events in Windows Event Viewer</span></span>

<span data-ttu-id="4f19c-126">Pour passer en revue les applications qui auraient été bloquées, ouvrez l’Observateur d’événements et filtrez l’ID d’événement 1125 dans le journal Microsoft-Windows-Windows-Defender/Opérationnel.</span><span class="sxs-lookup"><span data-stu-id="4f19c-126">To review apps that would have been blocked, open Event Viewer and filter for Event ID 1125 in the Microsoft-Windows-Windows-Defender/Operational log.</span></span> <span data-ttu-id="4f19c-127">Le tableau suivant répertorie tous les événements de protection réseau.</span><span class="sxs-lookup"><span data-stu-id="4f19c-127">The following table lists all network protection events.</span></span>

| <span data-ttu-id="4f19c-128">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="4f19c-128">Event ID</span></span> | <span data-ttu-id="4f19c-129">Fournir/Source</span><span class="sxs-lookup"><span data-stu-id="4f19c-129">Provide/Source</span></span> | <span data-ttu-id="4f19c-130">Description</span><span class="sxs-lookup"><span data-stu-id="4f19c-130">Description</span></span> |
|-|-|-|
|<span data-ttu-id="4f19c-131">5007</span><span class="sxs-lookup"><span data-stu-id="4f19c-131">5007</span></span> | <span data-ttu-id="4f19c-132">Windows Defender (opérationnel)</span><span class="sxs-lookup"><span data-stu-id="4f19c-132">Windows Defender (Operational)</span></span> | <span data-ttu-id="4f19c-133">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="4f19c-133">Event when settings are changed</span></span> |
|<span data-ttu-id="4f19c-134">1125</span><span class="sxs-lookup"><span data-stu-id="4f19c-134">1125</span></span> | <span data-ttu-id="4f19c-135">Windows Defender (opérationnel)</span><span class="sxs-lookup"><span data-stu-id="4f19c-135">Windows Defender (Operational)</span></span> | <span data-ttu-id="4f19c-136">Événement lors de l’audit d’une connexion réseau</span><span class="sxs-lookup"><span data-stu-id="4f19c-136">Event when a network connection is audited</span></span> |
|<span data-ttu-id="4f19c-137">1126</span><span class="sxs-lookup"><span data-stu-id="4f19c-137">1126</span></span> | <span data-ttu-id="4f19c-138">Windows Defender (opérationnel)</span><span class="sxs-lookup"><span data-stu-id="4f19c-138">Windows Defender (Operational)</span></span> | <span data-ttu-id="4f19c-139">Événement lors du blocage d’une connexion réseau</span><span class="sxs-lookup"><span data-stu-id="4f19c-139">Event when a network connection is blocked</span></span> |

## <a name="see-also"></a><span data-ttu-id="4f19c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f19c-140">See also</span></span>

* [<span data-ttu-id="4f19c-141">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="4f19c-141">Network protection</span></span>](network-protection.md)
* [<span data-ttu-id="4f19c-142">Activer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="4f19c-142">Enable network protection</span></span>](enable-network-protection.md)
* [<span data-ttu-id="4f19c-143">Résoudre les problèmes de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="4f19c-143">Troubleshoot network protection</span></span>](troubleshoot-np.md)
