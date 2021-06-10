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
ms.topic: how-to
ms.openlocfilehash: b6b664d471e238e2feb1e1aedd100c1299fc5bbe
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844261"
---
# <a name="protect-your-network"></a><span data-ttu-id="87330-104">Protéger votre réseau</span><span class="sxs-lookup"><span data-stu-id="87330-104">Protect your network</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="87330-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="87330-105">**Applies to:**</span></span>
- [<span data-ttu-id="87330-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="87330-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="87330-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="87330-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="87330-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="87330-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="87330-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="87330-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="87330-110">La protection réseau permet de réduire la surface d’attaque de vos appareils à partir d’événements Basés sur Internet.</span><span class="sxs-lookup"><span data-stu-id="87330-110">Network protection helps reduce the attack surface of your devices from Internet-based events.</span></span> <span data-ttu-id="87330-111">Elle empêche les employés d’utiliser n’importe quelle application pour accéder à des domaines dangereux qui peuvent héberger des tentatives d’hameçonnage, des attaques et d’autres contenus malveillants sur Internet.</span><span class="sxs-lookup"><span data-stu-id="87330-111">It prevents employees from using any application to access dangerous domains that might host phishing scams, exploits, and other malicious content on the Internet.</span></span> <span data-ttu-id="87330-112">La protection du réseau étend l’étendue des [Microsoft Defender SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) pour bloquer tout le trafic HTTP sortant qui tente de se connecter à des sources de réputation faible (basées sur le domaine ou le nom d’hôte).</span><span class="sxs-lookup"><span data-stu-id="87330-112">Network protection expands the scope of [Microsoft Defender SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) to block all outbound HTTP(s) traffic that attempts to connect to low-reputation sources (based on the domain or hostname).</span></span>

<span data-ttu-id="87330-113">La protection réseau est prise en charge Windows, à partir Windows 10 version 1709.</span><span class="sxs-lookup"><span data-stu-id="87330-113">Network protection is supported on Windows, beginning with Windows 10, version 1709.</span></span> <span data-ttu-id="87330-114">La protection réseau n’est pas encore prise en charge sur d’autres systèmes d’exploitation, mais la protection web est prise en charge à l’aide du nouveau Microsoft Edge basé sur Chromium.</span><span class="sxs-lookup"><span data-stu-id="87330-114">Network protection is not yet supported on other operating systems, but web protection is supported using the new Microsoft Edge based on Chromium.</span></span> <span data-ttu-id="87330-115">Pour en savoir plus, consultez [La protection Web.](web-protection-overview.md)</span><span class="sxs-lookup"><span data-stu-id="87330-115">To learn more, see [Web protection](web-protection-overview.md).</span></span>

<span data-ttu-id="87330-116">La protection du réseau étend la protection dans [la protection Web](web-protection-overview.md) au niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="87330-116">Network protection extends the protection in [Web protection](web-protection-overview.md) to the operating system level.</span></span> <span data-ttu-id="87330-117">Il fournit des fonctionnalités de protection web dans Edge à d’autres navigateurs et applications non-navigateur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87330-117">It provides web protection functionality in Edge to other supported browsers and non-browser applications.</span></span> <span data-ttu-id="87330-118">En outre, la protection réseau offre une visibilité et un blocage des indicateurs de compromission (IOCs) lorsqu’elle est utilisée avec la détection et la réponse des [points de terminaison.](overview-endpoint-detection-response.md)</span><span class="sxs-lookup"><span data-stu-id="87330-118">In addition, network protection provides visibility and blocking of indicators of compromise (IOCs) when used with [Endpoint detection and response](overview-endpoint-detection-response.md).</span></span> <span data-ttu-id="87330-119">Par exemple, la protection du réseau fonctionne avec vos [indicateurs personnalisés.](manage-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="87330-119">For example, network protection works with your [custom indicators](manage-indicators.md).</span></span>

<span data-ttu-id="87330-120">Pour plus d’informations sur la façon d’activer la protection réseau, voir [Activer la protection réseau.](enable-network-protection.md)</span><span class="sxs-lookup"><span data-stu-id="87330-120">For more information about how to enable network protection, see [Enable network protection](enable-network-protection.md).</span></span> <span data-ttu-id="87330-121">Utilisez la stratégie de groupe, PowerShell ou les CSP mdM pour activer et gérer la protection réseau dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="87330-121">Use Group Policy, PowerShell, or MDM CSPs to enable and manage network protection in your network.</span></span>

> [!TIP]
> <span data-ttu-id="87330-122">Consultez le site testground de Microsoft Defender for Endpoint [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour voir comment fonctionne la protection réseau.</span><span class="sxs-lookup"><span data-stu-id="87330-122">See the Microsoft Defender for Endpoint testground site at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to see how network protection works.</span></span>

<span data-ttu-id="87330-123">La protection réseau fonctionne mieux avec [Microsoft Defender pour point](microsoft-defender-endpoint.md)de terminaison, qui vous fournit des rapports détaillés sur les événements et les blocs Exploit Protection dans le cadre de scénarios d’investigation [d’alerte.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="87330-123">Network protection works best with [Microsoft Defender for Endpoint](microsoft-defender-endpoint.md), which gives you detailed reporting into exploit protection events and blocks as part of [alert investigation scenarios](investigate-alerts.md).</span></span>

<span data-ttu-id="87330-124">Lorsque la protection réseau bloque une connexion, une notification s’affiche à partir du centre de notifications.</span><span class="sxs-lookup"><span data-stu-id="87330-124">When network protection blocks a connection, a notification is displayed from the Action Center.</span></span> <span data-ttu-id="87330-125">Votre équipe des opérations de sécurité [peut personnaliser la notification](customize-attack-surface-reduction.md#customize-the-notification) avec les détails et les informations de contact de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="87330-125">Your security operations team can [customize the notification](customize-attack-surface-reduction.md#customize-the-notification) with your organization's details and contact information.</span></span> <span data-ttu-id="87330-126">En outre, les règles de réduction de la surface d’attaque individuelles peuvent être activées et personnalisées en fonction de certaines techniques à surveiller.</span><span class="sxs-lookup"><span data-stu-id="87330-126">In addition, individual attack surface reduction rules can be enabled and customized to suit certain techniques to monitor.</span></span>

<span data-ttu-id="87330-127">Vous pouvez également utiliser le [mode audit](audit-windows-defender.md) pour évaluer l’impact de la protection réseau sur votre organisation si elle était activée.</span><span class="sxs-lookup"><span data-stu-id="87330-127">You can also use [audit mode](audit-windows-defender.md) to evaluate how network protection would impact your organization if it were enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="87330-128">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="87330-128">Requirements</span></span>

<span data-ttu-id="87330-129">La protection réseau nécessite Windows 10 Professionnel ou Enterprise, et Antivirus Microsoft Defender protection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="87330-129">Network protection requires Windows 10 Pro or Enterprise, and Microsoft Defender Antivirus real-time protection.</span></span>

| <span data-ttu-id="87330-130">Version de Windows</span><span class="sxs-lookup"><span data-stu-id="87330-130">Windows version</span></span> | <span data-ttu-id="87330-131">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="87330-131">Microsoft Defender Antivirus</span></span> |
|:---|:---|
| <span data-ttu-id="87330-132">Windows 10 version 1709 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="87330-132">Windows 10 version 1709 or later</span></span> <p><span data-ttu-id="87330-133">Windows Serveur 1803 ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="87330-133">Windows Server 1803 or later</span></span> | <span data-ttu-id="87330-134">[Antivirus Microsoft Defender protection en temps réel](configure-real-time-protection-microsoft-defender-antivirus.md) et la [protection](enable-cloud-protection-microsoft-defender-antivirus.md) cloud doivent être activées</span><span class="sxs-lookup"><span data-stu-id="87330-134">[Microsoft Defender Antivirus real-time protection](configure-real-time-protection-microsoft-defender-antivirus.md) and [cloud-delivered protection](enable-cloud-protection-microsoft-defender-antivirus.md) must be enabled</span></span> |

<span data-ttu-id="87330-135">Après avoir activé les services, vous devrez peut-être configurer votre réseau ou votre pare-feu pour autoriser les connexions entre les services et vos appareils (également appelés points de terminaison).</span><span class="sxs-lookup"><span data-stu-id="87330-135">After you have enabled the services, you might need to configure your network or firewall to allow the connections between the services and your devices (also referred to as endpoints).</span></span>  

- `.smartscreen.microsoft.com`
- `.smartscreen-prod.microsoft.com`

## <a name="review-network-protection-events-in-the-microsoft-defender-for-endpoint-security-center"></a><span data-ttu-id="87330-136">Passer en revue les événements de protection réseau dans le Centre de sécurité Microsoft Defender pour points de terminaison</span><span class="sxs-lookup"><span data-stu-id="87330-136">Review network protection events in the Microsoft Defender for Endpoint Security Center</span></span>

<span data-ttu-id="87330-137">Microsoft Defender pour le point de terminaison fournit des rapports détaillés sur les événements et les blocages dans le cadre de ses [scénarios d’investigation d’alerte.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="87330-137">Microsoft Defender for Endpoint provides detailed reporting into events and blocks as part of its [alert investigation scenarios](investigate-alerts.md).</span></span>

<span data-ttu-id="87330-138">Vous pouvez interroger Microsoft Defender pour obtenir des données de point de terminaison à l’aide de [la recherche avancée.](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="87330-138">You can query Microsoft Defender for Endpoint data by using [advanced hunting](advanced-hunting-overview.md).</span></span> <span data-ttu-id="87330-139">Si vous utilisez le [mode audit,](audit-windows-defender.md)vous pouvez utiliser la recherche avancée pour voir comment les paramètres de protection réseau affecteraient votre environnement s’ils étaient activés.</span><span class="sxs-lookup"><span data-stu-id="87330-139">If you're using [audit mode](audit-windows-defender.md), you can use advanced hunting to see how network protection settings would affect your environment if they were enabled.</span></span>

<span data-ttu-id="87330-140">Voici un exemple de requête</span><span class="sxs-lookup"><span data-stu-id="87330-140">Here is an example query</span></span>

```kusto
DeviceEvents
| where ActionType in ('ExploitGuardNetworkProtectionAudited','ExploitGuardNetworkProtectionBlocked')
```

## <a name="review-network-protection-events-in-windows-event-viewer"></a><span data-ttu-id="87330-141">Passer en revue les événements de protection réseau dans Windows’observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="87330-141">Review network protection events in Windows Event Viewer</span></span>

<span data-ttu-id="87330-142">Vous pouvez consulter le journal Windows événements pour voir les événements créés lorsque la protection réseau bloque (ou audite) l’accès à une adresse IP ou un domaine malveillant :</span><span class="sxs-lookup"><span data-stu-id="87330-142">You can review the Windows event log to see events that are created when network protection blocks (or audits) access to a malicious IP or domain:</span></span>

1. <span data-ttu-id="87330-143">[Copiez le XML directement.](event-views.md)</span><span class="sxs-lookup"><span data-stu-id="87330-143">[Copy the XML directly](event-views.md).</span></span>

2. <span data-ttu-id="87330-144">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="87330-144">Select **OK**.</span></span>

<span data-ttu-id="87330-145">Cette procédure crée un affichage personnalisé qui filtre pour afficher uniquement les événements suivants liés à la protection du réseau :</span><span class="sxs-lookup"><span data-stu-id="87330-145">This procedure creates a custom view that filters to only show the following events related to network protection:</span></span>

| <span data-ttu-id="87330-146">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="87330-146">Event ID</span></span> | <span data-ttu-id="87330-147">Description</span><span class="sxs-lookup"><span data-stu-id="87330-147">Description</span></span> |
|:---|:---|
| <span data-ttu-id="87330-148">5007</span><span class="sxs-lookup"><span data-stu-id="87330-148">5007</span></span> | <span data-ttu-id="87330-149">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="87330-149">Event when settings are changed</span></span> |
| <span data-ttu-id="87330-150">1125</span><span class="sxs-lookup"><span data-stu-id="87330-150">1125</span></span> | <span data-ttu-id="87330-151">Événement lorsque la protection du réseau se déclenche en mode audit</span><span class="sxs-lookup"><span data-stu-id="87330-151">Event when network protection fires in audit mode</span></span> |
| <span data-ttu-id="87330-152">1126</span><span class="sxs-lookup"><span data-stu-id="87330-152">1126</span></span> | <span data-ttu-id="87330-153">Événement lorsque la protection réseau se déclenche en mode blocage</span><span class="sxs-lookup"><span data-stu-id="87330-153">Event when network protection fires in block mode</span></span> |

## <a name="considerations-for-windows-virtual-desktop-running-windows-10-enterprise-multi-session"></a><span data-ttu-id="87330-154">Considérations à prendre en compte Windows de bureau virtuel s’exécutant Windows 10 Entreprise multisess session</span><span class="sxs-lookup"><span data-stu-id="87330-154">Considerations for Windows virtual desktop running Windows 10 Enterprise Multi-Session</span></span>

<span data-ttu-id="87330-155">En raison de la nature multi-utilisateur de Windows 10 Entreprise, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="87330-155">Due to the multi-user nature of Windows 10 Enterprise, keep the following points in mind:</span></span>

1. <span data-ttu-id="87330-156">La protection réseau est une fonctionnalité à l’échelle de l’appareil qui ne peut pas être ciblée sur des sessions utilisateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="87330-156">Network protection is a device-wide feature and cannot be targeted to specific user sessions.</span></span>

2. <span data-ttu-id="87330-157">Les stratégies de filtrage de contenu Web sont également à l’échelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="87330-157">Web content filtering policies are also device wide.</span></span>

3. <span data-ttu-id="87330-158">Si vous devez différencier les groupes d’utilisateurs, envisagez de créer des Windows et des affectations d’hôtes Virtual Desktop distincts.</span><span class="sxs-lookup"><span data-stu-id="87330-158">If you need to differentiate between user groups, consider creating separate Windows Virtual Desktop host pools and assignments.</span></span>

4. <span data-ttu-id="87330-159">Testez la protection réseau en mode audit pour évaluer son comportement avant de le déployer.</span><span class="sxs-lookup"><span data-stu-id="87330-159">Test network protection in audit mode to assess its behavior before rolling out.</span></span> 

5. <span data-ttu-id="87330-160">Envisagez de re resserger votre déploiement si vous avez un grand nombre d’utilisateurs ou un grand nombre de sessions multi-utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="87330-160">Consider resizing your deployment if you have a large number of users or a large number of multi-user sessions.</span></span>

### <a name="alternative-option-for-network-protection"></a><span data-ttu-id="87330-161">Autre option pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="87330-161">Alternative option for network protection</span></span>

<span data-ttu-id="87330-162">Pour Windows 10 Entreprise multisession 1909 et plus, utilisé dans Windows Virtual Desktop sur Azure, la protection réseau pour Microsoft Edge peut être activée à l’aide de la méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="87330-162">For Windows 10 Enterprise Multi-Session 1909 and up, used in Windows Virtual Desktop on Azure, network protection for Microsoft Edge can be enabled using the following method:</span></span>

1. <span data-ttu-id="87330-163">Utilisez [Activer la protection réseau et](enable-network-protection.md) suivez les instructions pour appliquer votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="87330-163">Use [Turn on network protection](enable-network-protection.md) and follow the instructions to apply your policy.</span></span>

2. <span data-ttu-id="87330-164">Exécutez la commande PowerShell suivante : `Set-MpPreference -AllowNetworkProtectionOnWinServer 1`</span><span class="sxs-lookup"><span data-stu-id="87330-164">Execute the following PowerShell command: `Set-MpPreference -AllowNetworkProtectionOnWinServer 1`</span></span>

## <a name="network-protection-troubleshooting"></a><span data-ttu-id="87330-165">Résolution des problèmes de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="87330-165">Network protection troubleshooting</span></span>

<span data-ttu-id="87330-166">En raison de l’environnement dans lequel la Protection du réseau s’exécute, Microsoft peut ne pas être en mesure de détecter les paramètres proxy du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="87330-166">Due to the environment where Network Protection runs, Microsoft might not be able to detect operating system proxy settings.</span></span> <span data-ttu-id="87330-167">Dans certains cas, les clients de protection réseau ne peuvent pas accéder au service Cloud.</span><span class="sxs-lookup"><span data-stu-id="87330-167">In some cases, network protection clients are unable to reach Cloud Service.</span></span> <span data-ttu-id="87330-168">Pour résoudre le problème de connectivité, les clients titulaires d’une licence E5 doivent configurer l’une des clés de Registre Defender suivantes :</span><span class="sxs-lookup"><span data-stu-id="87330-168">To resolve the connectivity problem, customers with E5 licenses should configure one of the following Defender registry keys:</span></span>

```console
reg add "HKLM\Software\Microsoft\Windows Defender" /v ProxyServer /d "<proxy IP address: Port>" /f
reg add "HKLM\Software\Microsoft\Windows Defender" /v ProxyPacUrl /d "<Proxy PAC url>" /f

```

## <a name="related-articles"></a><span data-ttu-id="87330-169">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="87330-169">Related articles</span></span>

- <span data-ttu-id="87330-170">[Évaluer les niveaux de protection](evaluate-network-protection.md) | Entreprendre un scénario rapide qui illustre le fonctionnement de la fonctionnalité et les événements qui seraient généralement créés.</span><span class="sxs-lookup"><span data-stu-id="87330-170">[Evaluate network protection](evaluate-network-protection.md) | Undertake a quick scenario that demonstrates how the feature works, and what events would typically be created.</span></span>

- <span data-ttu-id="87330-171">[Activer la protection réseau](enable-network-protection.md) | Utilisez la stratégie de groupe, PowerShell ou les CSP mdM pour activer et gérer la protection réseau dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="87330-171">[Enable network protection](enable-network-protection.md) | Use Group Policy, PowerShell, or MDM CSPs to enable and manage network protection in your network.</span></span>
