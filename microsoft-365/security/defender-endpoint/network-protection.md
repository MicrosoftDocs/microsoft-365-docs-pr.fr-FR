---
title: Utiliser la protection réseau pour empêcher les connexions à des sites malveillants
description: Protéger votre réseau en empêchant les utilisateurs d’accéder aux adresses réseau malveillantes et suspectes connues
keywords: Protection du réseau, attaques, site web malveillant, ip, domaine, domaines
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
author: denisebmsft
ms.author: deniseb
ms.reviewer: ''
manager: dansimp
ms.custom: asr
ms.technology: mde
ms.date: 03/08/2021
ms.topic: how-to
ms.openlocfilehash: 2ef3fbeec65be512dfe07f1d533df4d8e9b31532
ms.sourcegitcommit: 437bdbf3f99610869811e80432a59b5f244f7a87
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2021
ms.locfileid: "51644499"
---
# <a name="protect-your-network"></a><span data-ttu-id="49f11-104">Protéger votre réseau</span><span class="sxs-lookup"><span data-stu-id="49f11-104">Protect your network</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="49f11-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="49f11-105">**Applies to:**</span></span>
- [<span data-ttu-id="49f11-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="49f11-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="49f11-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="49f11-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="49f11-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="49f11-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="49f11-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="49f11-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="49f11-110">La protection réseau permet de réduire la surface d’attaque de vos appareils à partir d’événements Basés sur Internet.</span><span class="sxs-lookup"><span data-stu-id="49f11-110">Network protection helps reduce the attack surface of your devices from Internet-based events.</span></span> <span data-ttu-id="49f11-111">Elle empêche les employés d’utiliser n’importe quelle application pour accéder à des domaines dangereux qui peuvent héberger des tentatives d’hameçonnage, des attaques et d’autres contenus malveillants sur Internet.</span><span class="sxs-lookup"><span data-stu-id="49f11-111">It prevents employees from using any application to access dangerous domains that might host phishing scams, exploits, and other malicious content on the Internet.</span></span> <span data-ttu-id="49f11-112">La protection du réseau étend l’étendue de [Microsoft Defender SmartScreen](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) pour bloquer tout le trafic HTTP sortant qui tente de se connecter à des sources de faible réputation (en fonction du domaine ou du nom d’hôte).</span><span class="sxs-lookup"><span data-stu-id="49f11-112">Network protection expands the scope of [Microsoft Defender SmartScreen](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) to block all outbound HTTP(s) traffic that attempts to connect to low-reputation sources (based on the domain or hostname).</span></span>

<span data-ttu-id="49f11-113">La protection réseau est prise en charge sur Windows, à partir de Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="49f11-113">Network protection is supported on Windows, beginning with Windows 10, version 1709.</span></span> 

<span data-ttu-id="49f11-114">Pour plus d’informations sur la façon d’activer la protection réseau, voir [Activer la protection réseau.](enable-network-protection.md)</span><span class="sxs-lookup"><span data-stu-id="49f11-114">For more information about how to enable network protection, see [Enable network protection](enable-network-protection.md).</span></span> <span data-ttu-id="49f11-115">Utilisez la stratégie de groupe, PowerShell ou les CSP mdM pour activer et gérer la protection réseau dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="49f11-115">Use Group Policy, PowerShell, or MDM CSPs to enable and manage network protection in your network.</span></span>

> [!TIP]
> <span data-ttu-id="49f11-116">Consultez le site testground de Microsoft Defender ATP [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour voir comment fonctionne la protection réseau.</span><span class="sxs-lookup"><span data-stu-id="49f11-116">See the Microsoft Defender ATP testground site at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to see how network protection works.</span></span>

<span data-ttu-id="49f11-117">La protection réseau fonctionne mieux avec [Microsoft Defender pour point](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/microsoft-defender-advanced-threat-protection)de terminaison, qui vous fournit des rapports détaillés sur les événements et les blocs Exploit Protection dans le cadre de scénarios d’investigation [d’alerte.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-alerts)</span><span class="sxs-lookup"><span data-stu-id="49f11-117">Network protection works best with [Microsoft Defender for Endpoint](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/microsoft-defender-advanced-threat-protection), which gives you detailed reporting into exploit protection events and blocks as part of [alert investigation scenarios](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-alerts).</span></span>

<span data-ttu-id="49f11-118">Lorsque la protection réseau bloque une connexion, une notification s’affiche à partir du centre de notifications.</span><span class="sxs-lookup"><span data-stu-id="49f11-118">When network protection blocks a connection, a notification is displayed from the Action Center.</span></span> <span data-ttu-id="49f11-119">Votre équipe des opérations de sécurité [peut personnaliser la notification](customize-attack-surface-reduction.md#customize-the-notification) avec les détails et les informations de contact de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="49f11-119">Your security operations team can [customize the notification](customize-attack-surface-reduction.md#customize-the-notification) with your organization's details and contact information.</span></span> <span data-ttu-id="49f11-120">En outre, les règles de réduction de la surface d’attaque individuelles peuvent être activées et personnalisées en fonction de certaines techniques à surveiller.</span><span class="sxs-lookup"><span data-stu-id="49f11-120">In addition, individual attack surface reduction rules can be enabled and customized to suit certain techniques to monitor.</span></span>

<span data-ttu-id="49f11-121">Vous pouvez également utiliser le [mode audit](audit-windows-defender.md) pour évaluer l’impact de la protection réseau sur votre organisation si elle était activée.</span><span class="sxs-lookup"><span data-stu-id="49f11-121">You can also use [audit mode](audit-windows-defender.md) to evaluate how network protection would impact your organization if it were enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f11-122">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="49f11-122">Requirements</span></span>

<span data-ttu-id="49f11-123">La protection réseau nécessite windows 10 Professionnel ou Entreprise, ainsi que la protection en temps réel de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="49f11-123">Network protection requires Windows 10 Pro or Enterprise, and Microsoft Defender Antivirus real-time protection.</span></span>

| <span data-ttu-id="49f11-124">Version de Windows</span><span class="sxs-lookup"><span data-stu-id="49f11-124">Windows version</span></span> | <span data-ttu-id="49f11-125">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="49f11-125">Microsoft Defender Antivirus</span></span> |
|:---|:---|
| <span data-ttu-id="49f11-126">Windows 10 version 1709 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="49f11-126">Windows 10 version 1709 or later</span></span> <p><span data-ttu-id="49f11-127">Windows Server 1803 ou une ultérieure</span><span class="sxs-lookup"><span data-stu-id="49f11-127">Windows Server 1803 or later</span></span> | <span data-ttu-id="49f11-128">[La protection en temps réel](https://docs.microsoft.com/windows/security/threat-protection/configure-real-time-protection-microsoft-defender-antivirus.md) et la protection [cloud](https://docs.microsoft.com/windows/security/threat-protection/enable-cloud-protection-microsoft-defender-antivirus.md) de l’Antivirus Microsoft Defender doivent être activées</span><span class="sxs-lookup"><span data-stu-id="49f11-128">[Microsoft Defender Antivirus real-time protection](https://docs.microsoft.com/windows/security/threat-protection/configure-real-time-protection-microsoft-defender-antivirus.md) and [cloud-delivered protection](https://docs.microsoft.com/windows/security/threat-protection/enable-cloud-protection-microsoft-defender-antivirus.md) must be enabled</span></span> |

<span data-ttu-id="49f11-129">Après avoir activé les services, vous devrez peut-être configurer votre réseau ou votre pare-feu pour autoriser les connexions entre les services et vos appareils (également appelés points de terminaison).</span><span class="sxs-lookup"><span data-stu-id="49f11-129">After you have enabled the services, you might need to configure your network or firewall to allow the connections between the services and your devices (also referred to as endpoints).</span></span>  

- <span data-ttu-id="49f11-130">.smartscreen.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="49f11-130">.smartscreen.microsoft.com</span></span>
- <span data-ttu-id="49f11-131">.smartscreen-prod.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="49f11-131">.smartscreen-prod.microsoft.com</span></span>

## <a name="review-network-protection-events-in-the-microsoft-defender-for-endpoint-security-center"></a><span data-ttu-id="49f11-132">Passer en revue les événements de protection réseau dans le Centre de sécurité Microsoft Defender pour points de terminaison</span><span class="sxs-lookup"><span data-stu-id="49f11-132">Review network protection events in the Microsoft Defender for Endpoint Security Center</span></span>

<span data-ttu-id="49f11-133">Microsoft Defender pour le point de terminaison fournit des rapports détaillés sur les événements et les blocages dans le cadre de ses [scénarios d’investigation d’alerte.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-alerts)</span><span class="sxs-lookup"><span data-stu-id="49f11-133">Microsoft Defender for Endpoint provides detailed reporting into events and blocks as part of its [alert investigation scenarios](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-alerts).</span></span>

<span data-ttu-id="49f11-134">Vous pouvez interroger Microsoft Defender pour obtenir des données de point de terminaison à l’aide du [recherche avancée.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-windows-defender-advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="49f11-134">You can query Microsoft Defender for Endpoint data by using [Advanced hunting](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-windows-defender-advanced-threat-protection).</span></span> <span data-ttu-id="49f11-135">Si vous utilisez le [mode audit,](audit-windows-defender.md)vous pouvez utiliser la recherche avancée pour voir comment les paramètres de protection réseau affecteraient votre environnement s’ils étaient activés.</span><span class="sxs-lookup"><span data-stu-id="49f11-135">If you're using [audit mode](audit-windows-defender.md), you can use advanced hunting to see how network protection settings would affect your environment if they were enabled.</span></span>

<span data-ttu-id="49f11-136">Voici un exemple de requête</span><span class="sxs-lookup"><span data-stu-id="49f11-136">Here is an example query</span></span>

```kusto
DeviceEvents
| where ActionType in ('ExploitGuardNetworkProtectionAudited','ExploitGuardNetworkProtectionBlocked')
```

## <a name="review-network-protection-events-in-windows-event-viewer"></a><span data-ttu-id="49f11-137">Passer en revue les événements de protection réseau dans l’Observateur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="49f11-137">Review network protection events in Windows Event Viewer</span></span>

<span data-ttu-id="49f11-138">Vous pouvez consulter le journal des événements Windows pour voir les événements créés lorsque la protection réseau bloque (ou audite) l’accès à une adresse IP ou un domaine malveillant :</span><span class="sxs-lookup"><span data-stu-id="49f11-138">You can review the Windows event log to see events that are created when network protection blocks (or audits) access to a malicious IP or domain:</span></span>

1. <span data-ttu-id="49f11-139">[Copiez le XML directement.](event-views.md)</span><span class="sxs-lookup"><span data-stu-id="49f11-139">[Copy the XML directly](event-views.md).</span></span>

2. <span data-ttu-id="49f11-140">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="49f11-140">Select **OK**.</span></span>

<span data-ttu-id="49f11-141">Cette procédure crée un affichage personnalisé qui filtre pour afficher uniquement les événements suivants liés à la protection du réseau :</span><span class="sxs-lookup"><span data-stu-id="49f11-141">This procedure creates a custom view that filters to only show the following events related to network protection:</span></span>

| <span data-ttu-id="49f11-142">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="49f11-142">Event ID</span></span> | <span data-ttu-id="49f11-143">Description</span><span class="sxs-lookup"><span data-stu-id="49f11-143">Description</span></span> |
|:---|:---|
| <span data-ttu-id="49f11-144">5007</span><span class="sxs-lookup"><span data-stu-id="49f11-144">5007</span></span> | <span data-ttu-id="49f11-145">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="49f11-145">Event when settings are changed</span></span> |
| <span data-ttu-id="49f11-146">1125</span><span class="sxs-lookup"><span data-stu-id="49f11-146">1125</span></span> | <span data-ttu-id="49f11-147">Événement lorsque la protection du réseau se déclenche en mode audit</span><span class="sxs-lookup"><span data-stu-id="49f11-147">Event when network protection fires in audit mode</span></span> |
| <span data-ttu-id="49f11-148">1126</span><span class="sxs-lookup"><span data-stu-id="49f11-148">1126</span></span> | <span data-ttu-id="49f11-149">Événement lorsque la protection réseau se déclenche en mode blocage</span><span class="sxs-lookup"><span data-stu-id="49f11-149">Event when network protection fires in block mode</span></span> |

## <a name="network-protection-troubleshooting"></a><span data-ttu-id="49f11-150">Résolution des problèmes de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="49f11-150">Network protection troubleshooting</span></span>

<span data-ttu-id="49f11-151">En raison de l’environnement dans lequel la Protection du réseau s’exécute, Microsoft peut ne pas être en mesure de détecter les paramètres proxy du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f11-151">Due to the environment where Network Protection runs, Microsoft might not be able to detect operating system proxy settings.</span></span> <span data-ttu-id="49f11-152">Dans certains cas, les clients de protection du réseau ne peuvent pas accéder au service Cloud.</span><span class="sxs-lookup"><span data-stu-id="49f11-152">In some cases, Network Protection clients are unable to reach Cloud Service.</span></span> <span data-ttu-id="49f11-153">Pour résoudre le problème de connectivité, les clients titulaires d’une licence E5 doivent configurer l’une des clés de Registre Defender suivantes :</span><span class="sxs-lookup"><span data-stu-id="49f11-153">To resolve the connectivity problem, customers with E5 licenses should configure one of the following Defender registry keys:</span></span>

```console
reg add "HKLM\Software\Microsoft\Windows Defender" /v ProxyServer /d "<proxy IP address: Port>" /f
reg add "HKLM\Software\Microsoft\Windows Defender" /v ProxyPacUrl /d "<Proxy PAC url>" /f

```

## <a name="related-articles"></a><span data-ttu-id="49f11-154">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="49f11-154">Related articles</span></span>

- <span data-ttu-id="49f11-155">[Évaluer les niveaux de protection](evaluate-network-protection.md) | Entreprendre un scénario rapide qui illustre le fonctionnement de la fonctionnalité et les événements qui seraient généralement créés.</span><span class="sxs-lookup"><span data-stu-id="49f11-155">[Evaluate network protection](evaluate-network-protection.md) | Undertake a quick scenario that demonstrates how the feature works, and what events would typically be created.</span></span>

- <span data-ttu-id="49f11-156">[Activer la protection réseau](enable-network-protection.md) | Utilisez la stratégie de groupe, PowerShell ou les CSP mdM pour activer et gérer la protection réseau dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="49f11-156">[Enable network protection](enable-network-protection.md) | Use Group Policy, PowerShell, or MDM CSPs to enable and manage network protection in your network.</span></span>
