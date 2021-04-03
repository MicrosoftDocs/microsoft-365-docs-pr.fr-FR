---
title: Microsoft Defender pour point de terminaison Mac
ms.reviewer: ''
description: Découvrez comment installer, configurer, mettre à jour et utiliser Microsoft Defender pour Endpoint pour Mac.
keywords: microsoft, defender, atp, mac, installation, déployer, désinstallation, intune, jamf, macos, big sur, magasin, mojave, mde pour mac
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
ms.openlocfilehash: 22d35a42eb7fb7eadbba686c292729772951c05c
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500688"
---
# <a name="microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="4a980-104">Microsoft Defender pour point de terminaison Mac</span><span class="sxs-lookup"><span data-stu-id="4a980-104">Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4a980-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4a980-105">**Applies to:**</span></span>
- [<span data-ttu-id="4a980-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4a980-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="4a980-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4a980-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="4a980-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="4a980-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="4a980-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="4a980-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="4a980-110">Cette rubrique décrit comment installer, configurer, mettre à jour et utiliser Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="4a980-110">This topic describes how to install, configure, update, and use Defender for Endpoint for Mac.</span></span>

> [!CAUTION]
> <span data-ttu-id="4a980-111">L’exécution d’autres produits de protection de point de terminaison tiers avec Microsoft Defender pour Endpoint pour Mac est susceptible de provoquer des problèmes de performances et des effets secondaires imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="4a980-111">Running other third-party endpoint protection products alongside Microsoft Defender for Endpoint for Mac is likely to lead to performance problems and unpredictable side effects.</span></span> <span data-ttu-id="4a980-112">Si la protection des points de terminaison non-Microsoft est une exigence absolue dans votre environnement, vous pouvez toujours tirer parti en toute sécurité de la fonctionnalité Defender pour point de terminaison pour Mac EDR après avoir configuré la fonctionnalité antivirus pour qu’elle s’exécute en [mode passif.](mac-preferences.md#enable--disable-passive-mode)</span><span class="sxs-lookup"><span data-stu-id="4a980-112">If non-Microsoft endpoint protection is an absolute requirement in your environment, you can still safely take advantage of Defender for Endpoint for Mac EDR functionality after configuring the antivirus functionality to run in [Passive mode](mac-preferences.md#enable--disable-passive-mode).</span></span>

## <a name="whats-new-in-the-latest-release"></a><span data-ttu-id="4a980-113">Nouveautés de la dernière version</span><span class="sxs-lookup"><span data-stu-id="4a980-113">What’s new in the latest release</span></span>

[<span data-ttu-id="4a980-114">Nouveautés dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4a980-114">What's new in Microsoft Defender for Endpoint</span></span>](whats-new-in-microsoft-defender-atp.md)

[<span data-ttu-id="4a980-115">Nouveautés de Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="4a980-115">What's new in Microsoft Defender for Endpoint for Mac</span></span>](mac-whatsnew.md)

> [!TIP]
> <span data-ttu-id="4a980-116">Si vous avez des commentaires que vous souhaitez partager, envoyez-le en ouvrant Microsoft Defender pour Endpoint pour Mac sur votre appareil et en naviguant vers l’aide pour envoyer  >  **des commentaires.**</span><span class="sxs-lookup"><span data-stu-id="4a980-116">If you have any feedback that you would like to share, submit it by opening Microsoft Defender for Endpoint for Mac on your device and navigating to **Help** > **Send feedback**.</span></span>

<span data-ttu-id="4a980-117">Pour obtenir les dernières fonctionnalités, y compris les fonctionnalités de prévisualisation (telles que la détection et la réponse des points de terminaison pour vos appareils Mac), configurez votre appareil macOS exécutant Microsoft Defender pour endpoint comme un appareil « Insider ».</span><span class="sxs-lookup"><span data-stu-id="4a980-117">To get the latest features, including preview capabilities (such as endpoint detection and response for your Mac devices), configure your macOS device running Microsoft Defender for Endpoint to be an "Insider" device.</span></span>

## <a name="how-to-install-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="4a980-118">Comment installer Microsoft Defender pour endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="4a980-118">How to install Microsoft Defender for Endpoint for Mac</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4a980-119">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="4a980-119">Prerequisites</span></span>

- <span data-ttu-id="4a980-120">Abonnement a Defender for Endpoint et accès au portail Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4a980-120">A Defender for Endpoint subscription and access to the Microsoft Defender Security Center portal</span></span>
- <span data-ttu-id="4a980-121">Expérience de niveau débutant dans les scripts macOS et BASH</span><span class="sxs-lookup"><span data-stu-id="4a980-121">Beginner-level experience in macOS and BASH scripting</span></span>
- <span data-ttu-id="4a980-122">Privilèges d’administration sur l’appareil (en cas de déploiement manuel)</span><span class="sxs-lookup"><span data-stu-id="4a980-122">Administrative privileges on the device (in case of manual deployment)</span></span>

### <a name="installation-instructions"></a><span data-ttu-id="4a980-123">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="4a980-123">Installation instructions</span></span>

<span data-ttu-id="4a980-124">Vous pouvez utiliser plusieurs méthodes et outils de déploiement pour installer et configurer Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="4a980-124">There are several methods and deployment tools that you can use to install and configure Defender for Endpoint for Mac.</span></span>

- <span data-ttu-id="4a980-125">Outils de gestion tiers :</span><span class="sxs-lookup"><span data-stu-id="4a980-125">Third-party management tools:</span></span>
    - [<span data-ttu-id="4a980-126">Déploiement basé sur Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="4a980-126">Microsoft Intune-based deployment</span></span>](mac-install-with-intune.md)
    - [<span data-ttu-id="4a980-127">Déploiement basé sur JAMF</span><span class="sxs-lookup"><span data-stu-id="4a980-127">JAMF-based deployment</span></span>](mac-install-with-jamf.md)
    - [<span data-ttu-id="4a980-128">Autres produits MDM</span><span class="sxs-lookup"><span data-stu-id="4a980-128">Other MDM products</span></span>](mac-install-with-other-mdm.md)

- <span data-ttu-id="4a980-129">Outil en ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="4a980-129">Command-line tool:</span></span>
    - [<span data-ttu-id="4a980-130">Déploiement manuel</span><span class="sxs-lookup"><span data-stu-id="4a980-130">Manual deployment</span></span>](mac-install-manually.md)

### <a name="system-requirements"></a><span data-ttu-id="4a980-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a980-131">System requirements</span></span>

<span data-ttu-id="4a980-132">Les trois plus récentes publication majeures de macOS sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4a980-132">The three most recent major releases of macOS are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a980-133">Sur macOS 11 (Big Sur), Microsoft Defender for Endpoint nécessite des profils de configuration supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4a980-133">On macOS 11 (Big Sur), Microsoft Defender for Endpoint requires additional configuration profiles.</span></span> <span data-ttu-id="4a980-134">Si vous êtes un client existant en cours de mise à niveau à partir de versions antérieures de macOS, veillez à déployer les profils de configuration supplémentaires répertoriés dans les nouveaux profils de configuration pour macOS Et les versions plus récentes de [macOS.](mac-sysext-policies.md)</span><span class="sxs-lookup"><span data-stu-id="4a980-134">If you are an existing customer upgrading from earlier versions of macOS, make sure to deploy the additional configuration profiles listed on [New configuration profiles for macOS Catalina and newer versions of macOS](mac-sysext-policies.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a980-135">La prise en charge de macOS 10.13 (High Sierra) n’est plus prise en charge depuis le 15 février 2021.</span><span class="sxs-lookup"><span data-stu-id="4a980-135">Support for macOS 10.13 (High Sierra) has been discontinued as of February 15th, 2021.</span></span>

- <span data-ttu-id="4a980-136">11 (Big Sur), 10.15 (Domaine), 10.14 (Mojave)</span><span class="sxs-lookup"><span data-stu-id="4a980-136">11 (Big Sur), 10.15 (Catalina), 10.14 (Mojave)</span></span>
- <span data-ttu-id="4a980-137">Espace disque : 1 Go</span><span class="sxs-lookup"><span data-stu-id="4a980-137">Disk space: 1GB</span></span>

<span data-ttu-id="4a980-138">Les versions bêta de macOS ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4a980-138">Beta versions of macOS are not supported.</span></span>

<span data-ttu-id="4a980-139">Après avoir activé le service, vous devrez peut-être configurer votre réseau ou votre pare-feu pour autoriser les connexions sortantes entre celui-ci et vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="4a980-139">After you've enabled the service, you may need to configure your network or firewall to allow outbound connections between it and your endpoints.</span></span>

### <a name="licensing-requirements"></a><span data-ttu-id="4a980-140">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="4a980-140">Licensing requirements</span></span>

<span data-ttu-id="4a980-141">Microsoft Defender pour endpoint pour Mac nécessite l’une des offres de licence en volume Microsoft suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a980-141">Microsoft Defender for Endpoint for Mac requires one of the following Microsoft Volume Licensing offers:</span></span>

- <span data-ttu-id="4a980-142">Microsoft 365 E5 (M365 E5)</span><span class="sxs-lookup"><span data-stu-id="4a980-142">Microsoft 365 E5 (M365 E5)</span></span>
- <span data-ttu-id="4a980-143">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="4a980-143">Microsoft 365 E5 Security</span></span>
- <span data-ttu-id="4a980-144">Microsoft 365 A5 (M365 A5)</span><span class="sxs-lookup"><span data-stu-id="4a980-144">Microsoft 365 A5 (M365 A5)</span></span>

> [!NOTE]
> <span data-ttu-id="4a980-145">Les utilisateurs titulaires d’une licence éligible peuvent utiliser Microsoft Defender pour endpoint sur cinq appareils simultanés au plus.</span><span class="sxs-lookup"><span data-stu-id="4a980-145">Eligible licensed users may use Microsoft Defender for Endpoint on up to five concurrent devices.</span></span>
> <span data-ttu-id="4a980-146">Microsoft Defender pour le point de terminaison est également disponible à l’achat auprès d’un fournisseur de solutions Cloud (CSP).</span><span class="sxs-lookup"><span data-stu-id="4a980-146">Microsoft Defender for Endpoint is also available for purchase from a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="4a980-147">Lorsqu’elle est achetée via un programme CSP, elle ne nécessite pas d’offres de licence en volume Microsoft répertoriées.</span><span class="sxs-lookup"><span data-stu-id="4a980-147">When purchased via a CSP, it does not require Microsoft Volume Licensing offers listed.</span></span>

### <a name="network-connections"></a><span data-ttu-id="4a980-148">Connexions réseau</span><span class="sxs-lookup"><span data-stu-id="4a980-148">Network connections</span></span>

<span data-ttu-id="4a980-149">La feuille de calcul téléchargeable suivante répertorie les services et les URL associées à qui votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="4a980-149">The following downloadable spreadsheet lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="4a980-150">Vous devez vous assurer qu’il n’existe aucune règle de pare-feu ou de  filtrage réseau qui refuserait l’accès à ces URL, ou que vous devrez peut-être créer une règle d’autoriser spécifiquement pour eux.</span><span class="sxs-lookup"><span data-stu-id="4a980-150">You should ensure that there are no firewall or network filtering rules that would deny access to these URLs, or you may need to create an *allow* rule specifically for them.</span></span>



|<span data-ttu-id="4a980-151">**Liste de feuilles de calcul de domaines**</span><span class="sxs-lookup"><span data-stu-id="4a980-151">**Spreadsheet of domains list**</span></span>|<span data-ttu-id="4a980-152">**Description**</span><span class="sxs-lookup"><span data-stu-id="4a980-152">**Description**</span></span>|
|:-----|:-----|
|![Image miniature de la feuille de calcul DES URL de Microsoft Defender pour les points de terminaison](images/mdatp-urls.png)<br/>  | <span data-ttu-id="4a980-154">Feuille de calcul d’enregistrements DNS spécifiques pour les emplacements de service, les emplacements géographiques et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4a980-154">Spreadsheet of specific DNS records for service locations, geographic locations, and OS.</span></span> <br><br><span data-ttu-id="4a980-155">Téléchargez la feuille de calcul [ ici :mdatp-urls.xlsx](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx).</span><span class="sxs-lookup"><span data-stu-id="4a980-155">Download the spreadsheet here: [mdatp-urls.xlsx](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx).</span></span>

<span data-ttu-id="4a980-156">Microsoft Defender pour le point de terminaison peut découvrir un serveur proxy à l’aide des méthodes de découverte suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a980-156">Microsoft Defender for Endpoint can discover a proxy server by using the following discovery methods:</span></span>
- <span data-ttu-id="4a980-157">Proxy autoconfig (PAC)</span><span class="sxs-lookup"><span data-stu-id="4a980-157">Proxy autoconfig (PAC)</span></span>
- <span data-ttu-id="4a980-158">WPAD (Web Proxy Autodiscovery Protocol)</span><span class="sxs-lookup"><span data-stu-id="4a980-158">Web Proxy Autodiscovery Protocol (WPAD)</span></span>
- <span data-ttu-id="4a980-159">Configuration manuelle du proxy statique</span><span class="sxs-lookup"><span data-stu-id="4a980-159">Manual static proxy configuration</span></span>

<span data-ttu-id="4a980-160">Si un proxy ou un pare-feu bloque le trafic anonyme, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="4a980-160">If a proxy or firewall is blocking anonymous traffic, make sure that anonymous traffic is permitted in the previously listed URLs.</span></span>

> [!WARNING]
> <span data-ttu-id="4a980-161">Les proxies authentifiés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4a980-161">Authenticated proxies are not supported.</span></span> <span data-ttu-id="4a980-162">Assurez-vous que seuls pac, WPAD ou un proxy statique est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4a980-162">Ensure that only PAC, WPAD, or a static proxy is being used.</span></span>
>
> <span data-ttu-id="4a980-163">L’inspection et l’interception des proxies SSL ne sont pas non plus pris en charge pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4a980-163">SSL inspection and intercepting proxies are also not supported for security reasons.</span></span> <span data-ttu-id="4a980-164">Configurez une exception pour l’inspection SSL et votre serveur proxy afin de transmettre directement les données de Microsoft Defender pour Endpoint pour Mac aux URL pertinentes sans interception.</span><span class="sxs-lookup"><span data-stu-id="4a980-164">Configure an exception for SSL inspection and your proxy server to directly pass through data from Microsoft Defender for Endpoint for Mac to the relevant URLs without interception.</span></span> <span data-ttu-id="4a980-165">L’ajout de votre certificat d’interception au magasin global n’autorise pas l’interception.</span><span class="sxs-lookup"><span data-stu-id="4a980-165">Adding your interception certificate to the global store will not allow for interception.</span></span>

<span data-ttu-id="4a980-166">Pour vérifier qu’une connexion n’est pas bloquée, [https://x.cp.wd.microsoft.com/api/report](https://x.cp.wd.microsoft.com/api/report) ouvrez-la [https://cdn.x.cp.wd.microsoft.com/ping](https://cdn.x.cp.wd.microsoft.com/ping) et dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="4a980-166">To test that a connection is not blocked, open [https://x.cp.wd.microsoft.com/api/report](https://x.cp.wd.microsoft.com/api/report) and [https://cdn.x.cp.wd.microsoft.com/ping](https://cdn.x.cp.wd.microsoft.com/ping) in a browser.</span></span>

<span data-ttu-id="4a980-167">Si vous préférez la ligne de commande, vous pouvez également vérifier la connexion en exécutant la commande suivante dans Terminal :</span><span class="sxs-lookup"><span data-stu-id="4a980-167">If you prefer the command line, you can also check the connection by running the following command in Terminal:</span></span>

```bash
curl -w ' %{url_effective}\n' 'https://x.cp.wd.microsoft.com/api/report' 'https://cdn.x.cp.wd.microsoft.com/ping'
```

<span data-ttu-id="4a980-168">La sortie de cette commande doit être similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="4a980-168">The output from this command should be similar to the following:</span></span>

 `OK https://x.cp.wd.microsoft.com/api/report`

 `OK https://cdn.x.cp.wd.microsoft.com/ping`

> [!CAUTION]
> <span data-ttu-id="4a980-169">Nous vous recommandons de conserver la [Protection de l’intégrité](https://support.apple.com/en-us/HT204899) du système (SIP) activée sur les appareils clients.</span><span class="sxs-lookup"><span data-stu-id="4a980-169">We recommend that you keep [System Integrity Protection](https://support.apple.com/en-us/HT204899) (SIP) enabled on client devices.</span></span> <span data-ttu-id="4a980-170">SIP est une fonctionnalité de sécurité macOS intégrée qui empêche toute falsification de bas niveau avec le système d’exploitation et est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a980-170">SIP is a built-in macOS security feature that prevents low-level tampering with the OS, and is enabled by default.</span></span>

<span data-ttu-id="4a980-171">Une fois Que Microsoft Defender pour le point de terminaison est installé, la connectivité peut être validée en exécutant la commande suivante dans Terminal :</span><span class="sxs-lookup"><span data-stu-id="4a980-171">Once Microsoft Defender for Endpoint is installed, connectivity can be validated by running the following command in Terminal:</span></span>
```bash
mdatp connectivity test
```

## <a name="how-to-update-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="4a980-172">Comment mettre à jour Microsoft Defender pour endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="4a980-172">How to update Microsoft Defender for Endpoint for Mac</span></span>

<span data-ttu-id="4a980-173">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4a980-173">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span> <span data-ttu-id="4a980-174">Pour mettre à jour Microsoft Defender pour Endpoint pour Mac, un programme nommé Microsoft AutoUpdate (MAU) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4a980-174">To update Microsoft Defender for Endpoint for Mac, a program named Microsoft AutoUpdate (MAU) is used.</span></span> <span data-ttu-id="4a980-175">Pour plus d’informations, voir [Déployer les mises à jour de Microsoft Defender pour Endpoint pour Mac.](mac-updates.md)</span><span class="sxs-lookup"><span data-stu-id="4a980-175">To learn more, see [Deploy updates for Microsoft Defender for Endpoint for Mac](mac-updates.md).</span></span>

## <a name="how-to-configure-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="4a980-176">Comment configurer Microsoft Defender pour endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="4a980-176">How to configure Microsoft Defender for Endpoint for Mac</span></span>

<span data-ttu-id="4a980-177">Des instructions sur la configuration du produit dans les environnements d’entreprise sont disponibles dans Définir les préférences de [Microsoft Defender pour Endpoint pour Mac.](mac-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="4a980-177">Guidance for how to configure the product in enterprise environments is available in [Set preferences for Microsoft Defender for Endpoint for Mac](mac-preferences.md).</span></span>

## <a name="macos-kernel-and-system-extensions"></a><span data-ttu-id="4a980-178">Noyau macOS et extensions système</span><span class="sxs-lookup"><span data-stu-id="4a980-178">macOS kernel and system extensions</span></span>

<span data-ttu-id="4a980-179">En adéquation avec l’évolution de macOS, nous préparons une mise à jour de Microsoft Defender pour Endpoint pour Mac qui tire parti des extensions système au lieu des extensions de noyau.</span><span class="sxs-lookup"><span data-stu-id="4a980-179">In alignment with macOS evolution, we are preparing a Microsoft Defender for Endpoint for Mac update that leverages system extensions instead of kernel extensions.</span></span> <span data-ttu-id="4a980-180">Pour plus d’informations, voir Nouveautés de [Microsoft Defender pour Endpoint pour Mac.](mac-whatsnew.md)</span><span class="sxs-lookup"><span data-stu-id="4a980-180">For relevant details, see [What's new in Microsoft Defender for Endpoint for Mac](mac-whatsnew.md).</span></span>

## <a name="resources"></a><span data-ttu-id="4a980-181">Ressources</span><span class="sxs-lookup"><span data-stu-id="4a980-181">Resources</span></span>

- <span data-ttu-id="4a980-182">Pour plus d’informations sur la journalisation, la désinstallation ou d’autres rubriques, voir [Resources for Microsoft Defender for Endpoint for Mac](mac-resources.md).</span><span class="sxs-lookup"><span data-stu-id="4a980-182">For more information about logging, uninstalling, or other topics, see [Resources for Microsoft Defender for Endpoint for Mac](mac-resources.md).</span></span>

- <span data-ttu-id="4a980-183">[Confidentialité pour Microsoft Defender pour point de terminaison pour Mac.](mac-privacy.md)</span><span class="sxs-lookup"><span data-stu-id="4a980-183">[Privacy for Microsoft Defender for Endpoint for Mac](mac-privacy.md).</span></span>
