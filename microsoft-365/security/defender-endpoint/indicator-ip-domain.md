---
title: Créer des indicateurs pour les IP et URL/domaines
ms.reviewer: ''
description: Créez des indicateurs pour les adresses IPS et les URL/domaines qui définissent la détection, la prévention et l’exclusion des entités.
keywords: ip, url, domaine, gérer, autorisé, bloqué, bloquer, nettoyer, malveillant, hachage de fichier, adresse IP, url, domaine
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: e7dc11fe709a6d04b6309706df90f0ebbc177e25
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52841065"
---
# <a name="create-indicators-for-ips-and-urlsdomains"></a><span data-ttu-id="81c27-104">Créer des indicateurs pour les IP et URL/domaines</span><span class="sxs-lookup"><span data-stu-id="81c27-104">Create indicators for IPs and URLs/domains</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="81c27-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="81c27-105">**Applies to:**</span></span>
- [<span data-ttu-id="81c27-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="81c27-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="81c27-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="81c27-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)



> [!TIP]
> <span data-ttu-id="81c27-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="81c27-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="81c27-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="81c27-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)


<span data-ttu-id="81c27-110">Defender pour le point de terminaison peut bloquer ce que Microsoft considère comme des ADRESSES/URL malveillantes, via Windows Defender SmartScreen pour navigateurs Microsoft et via la Protection du réseau pour les navigateurs non-Microsoft ou les appels effectués en dehors d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="81c27-110">Defender for Endpoint can block what Microsoft deems as malicious IPs/URLs, through Windows Defender SmartScreen for Microsoft browsers, and through Network Protection for non-Microsoft browsers or calls made outside of a browser.</span></span>

<span data-ttu-id="81c27-111">Le jeu de données d’intelligence contre les menaces a été géré par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="81c27-111">The threat intelligence data set for this has been managed by Microsoft.</span></span>

<span data-ttu-id="81c27-112">En créant des indicateurs pour les adresses IP, les URL ou les domaines, vous pouvez désormais autoriser ou bloquer des adresses IP, des URL ou des domaines en fonction de vos propres renseignements sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="81c27-112">By creating indicators for IPs and URLs or domains, you can now allow or block IPs, URLs, or domains based on your own threat intelligence.</span></span> <span data-ttu-id="81c27-113">Pour ce faire, vous pouvez utiliser la page des paramètres ou des groupes d’ordinateurs si vous estez d’après certains groupes plus ou moins à risque que d’autres.</span><span class="sxs-lookup"><span data-stu-id="81c27-113">You can do this through the settings page or by machine groups if you deem certain groups to be more or less at risk than others.</span></span>

> [!NOTE]
> <span data-ttu-id="81c27-114">La notation CIDR (Classless Inter-Domain Routing) pour les adresses IP n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="81c27-114">Classless Inter-Domain Routing (CIDR) notation for IP addresses is not supported.</span></span> 

### <a name="before-you-begin"></a><span data-ttu-id="81c27-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="81c27-115">Before you begin</span></span>
<span data-ttu-id="81c27-116">Il est important de comprendre les conditions préalables suivantes avant de créer des indicateurs pour IPS, URL ou domaines :</span><span class="sxs-lookup"><span data-stu-id="81c27-116">It's important to understand the following prerequisites prior to creating indicators for IPS, URLs, or domains:</span></span>
- <span data-ttu-id="81c27-117">Url/IP allow and block relies on the Defender for Endpoint component Network Protection to be enabled in block mode.</span><span class="sxs-lookup"><span data-stu-id="81c27-117">URL/IP allow and block relies on the Defender for Endpoint component Network Protection to be enabled in block mode.</span></span> <span data-ttu-id="81c27-118">Pour plus d’informations sur la protection du réseau et les instructions de configuration, voir [Activer la protection réseau.](enable-network-protection.md)</span><span class="sxs-lookup"><span data-stu-id="81c27-118">For more information on Network Protection and configuration instructions, see [Enable network protection](enable-network-protection.md).</span></span>
- <span data-ttu-id="81c27-119">La version du client anti-programme malveillant doit être 4.18.1906.x ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="81c27-119">The Antimalware client version must be 4.18.1906.x or later.</span></span> 
- <span data-ttu-id="81c27-120">Pris en charge sur les ordinateurs Windows 10 version 1709 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="81c27-120">Supported on machines on Windows 10, version 1709 or later.</span></span> 
- <span data-ttu-id="81c27-121">**Assurez-vous que les indicateurs réseau personnalisés** sont activés dans Centre de sécurité Microsoft Defender > Paramètres > **fonctionnalités avancées.**</span><span class="sxs-lookup"><span data-stu-id="81c27-121">Ensure that **Custom network indicators** is enabled in **Microsoft Defender Security Center > Settings > Advanced features**.</span></span> <span data-ttu-id="81c27-122">Pour plus d’informations, voir [Fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="81c27-122">For more information, see [Advanced features](advanced-features.md).</span></span>
- <span data-ttu-id="81c27-123">Pour la prise en charge des indicateurs sur iOS, voir [Configurer des indicateurs personnalisés.](/microsoft-365/security/defender-endpoint/ios-configure-features#configure-custom-indicators)</span><span class="sxs-lookup"><span data-stu-id="81c27-123">For support of indicators on iOS, see [Configure custom indicators](/microsoft-365/security/defender-endpoint/ios-configure-features#configure-custom-indicators).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="81c27-124">Seules les IP externes peuvent être ajoutées à la liste d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="81c27-124">Only external IPs can be added to the indicator list.</span></span> <span data-ttu-id="81c27-125">Les indicateurs ne peuvent pas être créés pour les IP internes.</span><span class="sxs-lookup"><span data-stu-id="81c27-125">Indicators cannot be created for internal IPs.</span></span>
> <span data-ttu-id="81c27-126">Pour les scénarios de protection web, nous vous recommandons d’utiliser les fonctionnalités intégrées dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="81c27-126">For web protection scenarios, we recommend using the built-in capabilities in Microsoft Edge.</span></span> <span data-ttu-id="81c27-127">Microsoft Edge utilise la [Protection](network-protection.md) du réseau pour inspecter le trafic réseau et autorise les blocs pour TCP, HTTP et HTTPS (TLS).</span><span class="sxs-lookup"><span data-stu-id="81c27-127">Microsoft Edge leverages [Network Protection](network-protection.md) to inspect network traffic and allows blocks for TCP, HTTP, and HTTPS (TLS).</span></span> <span data-ttu-id="81c27-128">S’il existe des stratégies d’indicateur d’URL en conflit, le chemin d’accès le plus long est appliqué.</span><span class="sxs-lookup"><span data-stu-id="81c27-128">If there are conflicting URL indicator policies, the longer path is applied.</span></span> <span data-ttu-id="81c27-129">Par exemple, la stratégie d’indicateur d’URL `https:\\support.microsoft.com/en-us/office` est prioritaire sur la stratégie d’indicateur d’URL. `https:\\support.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="81c27-129">For example, the URL indicator policy `https:\\support.microsoft.com/en-us/office` takes precedence over the URL indicator policy `https:\\support.microsoft.com`.</span></span>

> [!NOTE]
> <span data-ttu-id="81c27-130">Pour tous les autres processus, les scénarios de protection web tirent parti de la Protection du réseau pour l’inspection et l’application :</span><span class="sxs-lookup"><span data-stu-id="81c27-130">For all other processes, web protection scenarios leverage Network Protection for inspection and enforcement:</span></span> 
> - <span data-ttu-id="81c27-131">L’adresse IP est prise en charge pour les trois protocoles</span><span class="sxs-lookup"><span data-stu-id="81c27-131">IP is supported for all three protocols</span></span>
> - <span data-ttu-id="81c27-132">Seules les adresses IP individuelles sont pris en charge (pas de blocs CIDR ou de plages IP)</span><span class="sxs-lookup"><span data-stu-id="81c27-132">Only single IP addresses are supported (no CIDR blocks or IP ranges)</span></span>
> - <span data-ttu-id="81c27-133">Les URL chiffrées (chemin d’accès complet) ne peuvent être bloquées que sur les navigateurs de première partie (Internet Explorer, Edge)</span><span class="sxs-lookup"><span data-stu-id="81c27-133">Encrypted URLs (full path) can only be blocked on first party browsers (Internet Explorer, Edge)</span></span>
> - <span data-ttu-id="81c27-134">Les URL chiffrées (FQDN uniquement) peuvent être bloquées en dehors des navigateurs de première partie (Internet Explorer, Edge)</span><span class="sxs-lookup"><span data-stu-id="81c27-134">Encrypted URLS (FQDN only) can be blocked outside of first party browsers (Internet Explorer, Edge)</span></span>
> - <span data-ttu-id="81c27-135">Les blocs de chemin d’accès d’URL complète peuvent être appliqués au niveau du domaine et à toutes les URL non chiffrées</span><span class="sxs-lookup"><span data-stu-id="81c27-135">Full URL path blocks can be applied on the domain level and all unencrypted URLs</span></span>
 
> [!NOTE]
> <span data-ttu-id="81c27-136">Il peut y avoir jusqu’à 2 heures de latence (généralement moins) entre le moment où l’action est prise et l’URL et l’ADRESSE IP bloquées.</span><span class="sxs-lookup"><span data-stu-id="81c27-136">There may be up to 2 hours of latency (usually less) between the time the action is taken, and the URL and IP being blocked.</span></span> 

### <a name="create-an-indicator-for-ips-urls-or-domains-from-the-settings-page"></a><span data-ttu-id="81c27-137">Créer un indicateur pour les adresses IP, les URL ou les domaines à partir de la page des paramètres</span><span class="sxs-lookup"><span data-stu-id="81c27-137">Create an indicator for IPs, URLs, or domains from the settings page</span></span>

1. <span data-ttu-id="81c27-138">Dans le volet de navigation, sélectionnez **Paramètres**  >  **indicateurs.**</span><span class="sxs-lookup"><span data-stu-id="81c27-138">In the navigation pane, select **Settings** > **Indicators**.</span></span>  

2. <span data-ttu-id="81c27-139">Sélectionnez **l’onglet Adresses IP ou URL/Domaines.**</span><span class="sxs-lookup"><span data-stu-id="81c27-139">Select the **IP addresses or URLs/Domains** tab.</span></span>

3. <span data-ttu-id="81c27-140">Sélectionnez **Ajouter un élément.**</span><span class="sxs-lookup"><span data-stu-id="81c27-140">Select **Add item**.</span></span>

4. <span data-ttu-id="81c27-141">Spécifiez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="81c27-141">Specify the following details:</span></span>
   - <span data-ttu-id="81c27-142">Indicateur : spécifiez les détails de l’entité et définissez l’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="81c27-142">Indicator - Specify the entity details and define the expiration of the indicator.</span></span>
   - <span data-ttu-id="81c27-143">Action : spécifiez l’action à prendre et fournissez une description.</span><span class="sxs-lookup"><span data-stu-id="81c27-143">Action - Specify the action to be taken and provide a description.</span></span>
   - <span data-ttu-id="81c27-144">Étendue : définir l’étendue du groupe d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="81c27-144">Scope - Define the scope of the machine group.</span></span>

5. <span data-ttu-id="81c27-145">Consultez les détails de l’onglet Résumé, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="81c27-145">Review the details in the Summary tab, then click **Save**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81c27-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81c27-146">Related topics</span></span>
- [<span data-ttu-id="81c27-147">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="81c27-147">Create indicators</span></span>](manage-indicators.md)
- [<span data-ttu-id="81c27-148">Créer des indicateurs pour les fichiers</span><span class="sxs-lookup"><span data-stu-id="81c27-148">Create indicators for files</span></span>](indicator-file.md)
- [<span data-ttu-id="81c27-149">Créer des indicateurs basés sur des certificats</span><span class="sxs-lookup"><span data-stu-id="81c27-149">Create indicators based on certificates</span></span>](indicator-certificates.md)
- [<span data-ttu-id="81c27-150">Gérer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="81c27-150">Manage indicators</span></span>](indicator-manage.md)
