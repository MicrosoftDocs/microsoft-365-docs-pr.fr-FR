---
title: Nouvelle application Microsoft Edge
description: ''
keywords: navigateur, bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 0602d7c6afef6190578268c78994b43ac60d0d2f
ms.sourcegitcommit: 3119b2246001ba06af8264508785352dfb894166
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44820678"
---
# <a name="new-microsoft-edge-app"></a><span data-ttu-id="011be-103">Nouvelle application Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="011be-103">New Microsoft Edge app</span></span>

<span data-ttu-id="011be-104">Le nouveau [navigateur Microsoft Edge](https://www.microsoft.com/edge) offre des performances de qualité internationale en matière de confidentialité, de productivité et de valeur ajoutée pendant que vous parcourez.</span><span class="sxs-lookup"><span data-stu-id="011be-104">The new [Microsoft Edge browser](https://www.microsoft.com/edge) provides world-class performance with more privacy, more productivity, and more value while you browse.</span></span> <span data-ttu-id="011be-105">Microsoft Managed Desktop offre une préversion publique du déploiement du nouveau navigateur Edge dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="011be-105">Microsoft Managed Desktop is offering a public preview of deployment of the new Edge browser in your environment.</span></span>

## <a name="initial-deployment"></a><span data-ttu-id="011be-106">Déploiement initial</span><span class="sxs-lookup"><span data-stu-id="011be-106">Initial deployment</span></span>

<span data-ttu-id="011be-107">Pour migrer vos appareils de bureau gérés Microsoft vers le nouveau navigateur Microsoft Edge, défichierz un ticket de support informatique via le portail de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="011be-107">To migrate your Microsoft Managed Desktop devices to the new Microsoft Edge browser, file an IT Support Ticket through the Microsoft Managed Desktop Portal.</span></span> <span data-ttu-id="011be-108">Nous allons déployer le canal stable Edge dans le groupe de test lorsque vous fichier, puis le déployer dans chaque groupe de déploiement suivant toutes les 24 heures.</span><span class="sxs-lookup"><span data-stu-id="011be-108">We will deploy the Edge Stable channel to the Test Group when you file the ticket, and then deploy it in each subsequent deployment group every 24 hours.</span></span> <span data-ttu-id="011be-109">Pour suspendre le déploiement, fichier autre ticket demandant les opérations à conserver.</span><span class="sxs-lookup"><span data-stu-id="011be-109">To pause the deployment, file another ticket asking Operations to hold.</span></span>

## <a name="updates-to-microsoft-edge"></a><span data-ttu-id="011be-110">Mises à jour de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="011be-110">Updates to Microsoft Edge</span></span>

<span data-ttu-id="011be-111">Microsoft Managed Desktop déploie le [canal stable](https://docs.microsoft.com/deployedge/microsoft-edge-channels#stable-channel) de Microsoft Edge qui est mis à jour automatiquement toutes les six semaines.</span><span class="sxs-lookup"><span data-stu-id="011be-111">Microsoft Managed Desktop deploys the [Stable channel](https://docs.microsoft.com/deployedge/microsoft-edge-channels#stable-channel) of Microsoft Edge which is auto-updated about every six weeks.</span></span> <span data-ttu-id="011be-112">Les mises à jour sur le canal stable sont déployées [progressivement](https://docs.microsoft.com/deployedge/microsoft-edge-update-progressive-rollout) par le groupe de produits Microsoft Edge afin de garantir une meilleure expérience aux clients.</span><span class="sxs-lookup"><span data-stu-id="011be-112">Updates on the Stable channel are rolled out [progressively](https://docs.microsoft.com/deployedge/microsoft-edge-update-progressive-rollout) by the Microsoft Edge product group in order to ensure the best experience for customers.</span></span> <span data-ttu-id="011be-113">Le canal Microsoft Edge bêta n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="011be-113">The Microsoft Edge Beta channel is not currently available.</span></span>

<span data-ttu-id="011be-114">Pour vous assurer que les mises à jour Microsoft Edge sont correctes, ne modifiez pas les [stratégies de mise à jour](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies)Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="011be-114">To ensure that Microsoft Edge updates correctly, do not modify the Microsoft Edge [update policies](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies).</span></span>

## <a name="settings-managed-by-microsoft-managed-desktop"></a><span data-ttu-id="011be-115">Paramètres gérés par le bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="011be-115">Settings managed by Microsoft Managed Desktop</span></span>

<span data-ttu-id="011be-116">Microsoft Managed Desktop a créé un ensemble de stratégies par défaut pour Microsoft Edge afin de sécuriser le navigateur.</span><span class="sxs-lookup"><span data-stu-id="011be-116">Microsoft Managed Desktop has created a default set of policies for Microsoft Edge to secure the browser.</span></span> <span data-ttu-id="011be-117">Les paramètres du navigateur par défaut sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="011be-117">The default browser settings are as follows:</span></span>

### <a name="microsoft-edge-extensions"></a><span data-ttu-id="011be-118">Extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="011be-118">Microsoft Edge extensions</span></span>

<span data-ttu-id="011be-119">La sécurité Baseline de Microsoft Edge sur les périphériques de bureau gérés Microsoft définit deux stratégies pour désactiver toutes les extensions chrome et sécuriser les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="011be-119">The security baseline for Microsoft Edge on Microsoft Managed Desktop devices sets two policies to disable all Chrome extensions and secure end users.</span></span> <span data-ttu-id="011be-120">Pour activer et déployer des extensions dans votre environnement, voir paramètres que vous gérez.</span><span class="sxs-lookup"><span data-stu-id="011be-120">To enable and deploy extensions in your environment, see Settings you manage.</span></span> 

#### <a name="extension-installation-blocklist"></a><span data-ttu-id="011be-121">Blocage de l’installation des extensions</span><span class="sxs-lookup"><span data-stu-id="011be-121">Extension installation blocklist</span></span>
<span data-ttu-id="011be-122">**Valeur par défaut :** Tous les</span><span class="sxs-lookup"><span data-stu-id="011be-122">**Default value:** All</span></span>

<span data-ttu-id="011be-123">Microsoft Managed Desktop définit cette stratégie pour empêcher les extensions chrome d’être installées sur les points de terminaison gérés.</span><span class="sxs-lookup"><span data-stu-id="011be-123">Microsoft Managed Desktop sets this policy to prevent Chrome extensions from being installed on managed endpoints.</span></span> <span data-ttu-id="011be-124">Il existe des risksassociated connus avec le modèle d’extension chrome, notamment la protection contre la perte de données, la confidentialité et d’autres risques qui peuvent compromettre les appareils.</span><span class="sxs-lookup"><span data-stu-id="011be-124">There are known risksassociated with the Chromium extension model including data loss protection, privacy, and other risks that can compromise devices.</span></span> 

#### <a name="allow-user-level-native-messaging-hosts-installed-without-admin-permissions"></a><span data-ttu-id="011be-125">Autoriser les hôtes de messagerie natifs au niveau utilisateur (installés sans autorisations d’administrateur)</span><span class="sxs-lookup"><span data-stu-id="011be-125">Allow user-level native messaging hosts (installed without admin permissions)</span></span>

<span data-ttu-id="011be-126">**Valeur par défaut :** Activation</span><span class="sxs-lookup"><span data-stu-id="011be-126">**Default value:** Disabled</span></span>

<span data-ttu-id="011be-127">Si vous désactivez cette stratégie, Microsoft Edge utilisera uniquement les hôtes de messagerie natif installés au niveau du système.</span><span class="sxs-lookup"><span data-stu-id="011be-127">By disabling this policy, Microsoft Edge will only use native messaging hosts installed on the system level.</span></span> <span data-ttu-id="011be-128">Les hôtes de messagerie natifs font partie des extensions chrome qui permettent au navigateur d’interagir avec d’autres parties du point de terminaison de l’utilisateur, créant ainsi de nombreux problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="011be-128">Native messaging hosts are a part of Chrome extensions which allow for the browser to interact with other parts of user’s endpoint, creating a variety of security concerns.</span></span>  

### <a name="secure-sockets-layer-ssl"></a><span data-ttu-id="011be-129">SSL (Secure Sockets Layer)</span><span class="sxs-lookup"><span data-stu-id="011be-129">Secure Sockets Layer (SSL)</span></span>

#### <a name="minimum-ssl-version"></a><span data-ttu-id="011be-130">Version SSL minimale</span><span class="sxs-lookup"><span data-stu-id="011be-130">Minimum SSL version</span></span>

<span data-ttu-id="011be-131">**Valeur par défaut :** Minimum TLS 1,2 pris en charge</span><span class="sxs-lookup"><span data-stu-id="011be-131">**Default value:** Minimum TLS 1.2 supported</span></span>

<span data-ttu-id="011be-132">Si vous souhaitez utiliser le chiffrement TLS 1,1 moins sécurisé, vous pouvez demander ceci.</span><span class="sxs-lookup"><span data-stu-id="011be-132">If you want to use the less secure TLS 1.1, you can request this.</span></span>

#### <a name="allows-users-to-proceed-from-the-ssl-warning-page"></a><span data-ttu-id="011be-133">Permet aux utilisateurs de continuer à partir de la page d’avertissement SSL</span><span class="sxs-lookup"><span data-stu-id="011be-133">Allows users to proceed from the SSL warning page</span></span>

<span data-ttu-id="011be-134">**Valeur par défaut :** Activation</span><span class="sxs-lookup"><span data-stu-id="011be-134">**Default value:** Disabled</span></span>

<span data-ttu-id="011be-135">Il n’est pas recommandé d’activer ce paramètre, car il permet aux utilisateurs de visiter des sites avec des erreurs SSL.</span><span class="sxs-lookup"><span data-stu-id="011be-135">We don't recommend enabling this setting since it allows users to visit sites with SSL errors.</span></span>

### <a name="microsoft-defender-smart-screen"></a><span data-ttu-id="011be-136">Écran intelligent Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="011be-136">Microsoft Defender Smart Screen</span></span>

#### <a name="configure-microsoft-defender-smartscreen"></a><span data-ttu-id="011be-137">Configurer Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="011be-137">Configure Microsoft Defender SmartScreen</span></span>

<span data-ttu-id="011be-138">**Valeur par défaut :** Activé</span><span class="sxs-lookup"><span data-stu-id="011be-138">**Default value:** Enabled</span></span>

<span data-ttu-id="011be-139">Activé par défaut pour protéger les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="011be-139">Enabled by default to help protect end users.</span></span>

#### <a name="microsoft-defender-smartscreen-prompts-for-sites"></a><span data-ttu-id="011be-140">Invites Microsoft Defender SmartScreen pour les sites</span><span class="sxs-lookup"><span data-stu-id="011be-140">Microsoft Defender SmartScreen prompts for sites</span></span>

<span data-ttu-id="011be-141">**Valeur par défaut :** Activé</span><span class="sxs-lookup"><span data-stu-id="011be-141">**Default value:** Enabled</span></span>

<span data-ttu-id="011be-142">Nous vous déconseillons de désactiver ce paramètre car cela permettrait aux utilisateurs d’ignorer les avertissements et de continuer à des sites potentiellement malveillants.</span><span class="sxs-lookup"><span data-stu-id="011be-142">We do not recommend disabling this setting since that would allow users to ignore warnings and continue to potentially malicious sites.</span></span>

#### <a name="prevent-bypassing-of-microsoft-defender-smartscreen-warnings-about-downloads"></a><span data-ttu-id="011be-143">Empêcher le contournement des avertissements Microsoft Defender SmartScreen concernant les téléchargements</span><span class="sxs-lookup"><span data-stu-id="011be-143">Prevent bypassing of Microsoft Defender SmartScreen warnings about downloads</span></span>

<span data-ttu-id="011be-144">**Valeur par défaut :** Activé</span><span class="sxs-lookup"><span data-stu-id="011be-144">**Default value:** Enabled</span></span>

<span data-ttu-id="011be-145">Nous vous déconseillons de désactiver ce paramètre car cela permettrait aux utilisateurs d’ignorer les avertissements et d’effectuer des téléchargements non vérifiés.</span><span class="sxs-lookup"><span data-stu-id="011be-145">We do not recommend disabling this setting since that would allow users to ignore warnings and complete unverified downloads.</span></span>

### <a name="adobe-flash"></a><span data-ttu-id="011be-146">Adobe Flash</span><span class="sxs-lookup"><span data-stu-id="011be-146">Adobe Flash</span></span>

#### <a name="default-adobe-flash-setting"></a><span data-ttu-id="011be-147">Paramètre Adobe Flash par défaut</span><span class="sxs-lookup"><span data-stu-id="011be-147">Default Adobe Flash setting</span></span>

<span data-ttu-id="011be-148">**Valeur par défaut :** Activation</span><span class="sxs-lookup"><span data-stu-id="011be-148">**Default value:** Disabled</span></span>

<span data-ttu-id="011be-149">Il n’est pas recommandé d’utiliser flash en raison des risques de sécurité associés.</span><span class="sxs-lookup"><span data-stu-id="011be-149">We don't recommend using Flash because of associated security risks.</span></span> <span data-ttu-id="011be-150">Si vous avez encore des processus qui dépendent d’un flash, définissez la stratégie **[PluginsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#pluginsallowedforurls)** pour activer Flash pour les sites qui en ont besoin.</span><span class="sxs-lookup"><span data-stu-id="011be-150">If you still have processes which depend on Flash, set the **[PluginsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#pluginsallowedforurls)** policy to enable Flash for sites which need it.</span></span> <span data-ttu-id="011be-151">Si ne peut pas conserver une liste autorisée de sites pour utiliser Flash, déposez une demande de modification pour modifier la valeur **sur Cliquer pour lire**, ce qui permet aux utilisateurs de choisir le moment approprié pour exécuter Flash.</span><span class="sxs-lookup"><span data-stu-id="011be-151">If can't maintain an allowed list of sites to use Flash, file a change request to change the value to **Click to Play**, which allows users choose when it's appropriate to run Flash.</span></span>

### <a name="password-manager"></a><span data-ttu-id="011be-152">Gestionnaire de mots de passe</span><span class="sxs-lookup"><span data-stu-id="011be-152">Password manager</span></span>

#### <a name="enable-saving-passwords-to-the-password-manager"></a><span data-ttu-id="011be-153">Activer l’enregistrement des mots de passe dans le gestionnaire de mots de passe</span><span class="sxs-lookup"><span data-stu-id="011be-153">Enable saving passwords to the password manager</span></span>

<span data-ttu-id="011be-154">**Valeur par défaut :** Activation</span><span class="sxs-lookup"><span data-stu-id="011be-154">**Default value:** Disabled</span></span>

<span data-ttu-id="011be-155">Nous vous déconseillons d’autoriser les utilisateurs finaux à enregistrer les mots de passe sur leur appareil.</span><span class="sxs-lookup"><span data-stu-id="011be-155">We do not recommend allowing end users to save passwords on their device.</span></span>

### <a name="other-settings"></a><span data-ttu-id="011be-156">Autres paramètres</span><span class="sxs-lookup"><span data-stu-id="011be-156">Other settings</span></span>

#### <a name="enable-site-isolation-for-every-site"></a><span data-ttu-id="011be-157">Activer l’isolation de site pour chaque site</span><span class="sxs-lookup"><span data-stu-id="011be-157">Enable site isolation for every site</span></span>

<span data-ttu-id="011be-158">**Valeur par défaut :** Activé</span><span class="sxs-lookup"><span data-stu-id="011be-158">**Default value:** Enabled</span></span>

<span data-ttu-id="011be-159">Lorsque cette stratégie est activée, les utilisateurs ne peuvent pas désactiver le comportement par défaut dans lequel chaque site s’exécute dans son propre processus.</span><span class="sxs-lookup"><span data-stu-id="011be-159">When this policy is enabled, users can't opt out of the default behavior in which each site runs in its own process.</span></span>

#### <a name="supported-authentication-schemes"></a><span data-ttu-id="011be-160">Modèles d’authentification pris en charge</span><span class="sxs-lookup"><span data-stu-id="011be-160">Supported authentication schemes</span></span>

<span data-ttu-id="011be-161">**Valeur par défaut :** NTLM, Negotiate</span><span class="sxs-lookup"><span data-stu-id="011be-161">**Default value:** NTLM, Negotiate</span></span>

<span data-ttu-id="011be-162">Microsoft Managed Desktop ne prend pas en charge les schémas d’authentification de base ou Digest.</span><span class="sxs-lookup"><span data-stu-id="011be-162">Microsoft Managed Desktop doesn't support Basic or Digest Authentication schemes.</span></span>

#### <a name="automatically-import-another-browsers-data-and-settings-at-first-run"></a><span data-ttu-id="011be-163">Importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="011be-163">Automatically import another browser's data and settings at first run</span></span>

<span data-ttu-id="011be-164">**Valeur par défaut :** Importer automatiquement tous les types de données et les paramètres pris en charge à partir du navigateur par défaut</span><span class="sxs-lookup"><span data-stu-id="011be-164">**Default value:** Automatically import all supported datatypes and settings from the default browser</span></span> 

<span data-ttu-id="011be-165">Une fois cette stratégie appliquée, l’expérience de première exécution ignorera la section d’importation, réduisant ainsi les interactions avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="011be-165">With this policy applied, the First Run Experience will skip the import section, minimizing user interaction.</span></span> <span data-ttu-id="011be-166">Les données de navigateur des versions antérieures de Microsoft Edge seront toujours migrées silencieusement lors de la première exécution, quel que soit ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="011be-166">The browser data from older versions of Microsoft Edge will always be silently migrated at the first run, regardless of this setting.</span></span> 


## <a name="settings-you-manage"></a><span data-ttu-id="011be-167">Paramètres que vous gérez</span><span class="sxs-lookup"><span data-stu-id="011be-167">Settings you manage</span></span>

<span data-ttu-id="011be-168">Vous pouvez déployer n’importe quel paramètre de serveur de pointe non décrit précédemment à l’aide du profil des modèles d’administration dans Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="011be-168">You can deploy any Microsft Edge settings not previously described by using the Administrative Templates profile in Microsoft Intune.</span></span> <span data-ttu-id="011be-169">Pour plus d’informations, reportez-vous à la rubrique [configure Microsoft Edge Policy Settings with Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span><span class="sxs-lookup"><span data-stu-id="011be-169">For details, see [Configure Microsoft Edge policy settings with Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span></span> <span data-ttu-id="011be-170">Si vous souhaitez évaluer une stratégie qui n’est pas actuellement incluse dans les modèles d’administration Microsoft Edge dans Intune, vous pouvez utiliser des paramètres personnalisés pour les appareils Windows 10 dans Intune.</span><span class="sxs-lookup"><span data-stu-id="011be-170">If you want to evaluate a policy that is not currently included in the Microsoft Edge Administrative Templates in Intune you can use custom settings for Windows 10 devices in Intune.</span></span>

### <a name="enabling-specific-chrome-extensions"></a><span data-ttu-id="011be-171">Activation d’extensions de chrome spécifiques</span><span class="sxs-lookup"><span data-stu-id="011be-171">Enabling specific Chrome extensions</span></span>

<span data-ttu-id="011be-172">Le modèle d’administration offre un paramètre permettant de déployer des extensions chrome spécifiques avec Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="011be-172">The Administrative Template offers a setting to deploy particular Chrome extensions with Microsoft Intune.</span></span> <span data-ttu-id="011be-173">Vous pouvez le trouver dans **configuration de l’ordinateur > extensions Microsoft Edge > > autoriser l’installation d’extensions spécifiques**.</span><span class="sxs-lookup"><span data-stu-id="011be-173">You can find it in **Computer Configuration > Microsoft Edge > Extensions > Allow Specific Extensions to be installed**.</span></span>

### <a name="install-extensions-silently"></a><span data-ttu-id="011be-174">Installer les extensions en mode silencieux</span><span class="sxs-lookup"><span data-stu-id="011be-174">Install extensions silently</span></span>

<span data-ttu-id="011be-175">Vous pouvez également utiliser le modèle d’administration pour configurer Microsoft Edge de sorte qu’il installe les extensions sans alerter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="011be-175">You can also use the Administrative Template to set Microsoft Edge to install extensions without alerting the user.</span></span> <span data-ttu-id="011be-176">Vous pouvez le trouver dans **configuration de l’ordinateur > extensions de > Microsoft Edge > contrôler les extensions installées**de manière silencieuse.</span><span class="sxs-lookup"><span data-stu-id="011be-176">You can find it in **Computer Configuration > Microsoft Edge > Extensions > Control which extensions are installed silently**.</span></span>

### <a name="other-common-enterprise-policies"></a><span data-ttu-id="011be-177">Autres stratégies d’entreprise courantes</span><span class="sxs-lookup"><span data-stu-id="011be-177">Other common enterprise policies</span></span>

<span data-ttu-id="011be-178">Microsoft Edge offre un grand nombre de stratégies supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="011be-178">Microsoft Edge offers a great many additional policies.</span></span> <span data-ttu-id="011be-179">Voici quelques-uns des plus courants :</span><span class="sxs-lookup"><span data-stu-id="011be-179">These are some of the more common ones:</span></span>
 
- [<span data-ttu-id="011be-180">Configurer des sites sur la liste de sites d’entreprise et le mode IE</span><span class="sxs-lookup"><span data-stu-id="011be-180">Configure Sites on the Enterprise Site List and IE Mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode-sitelist)
- [<span data-ttu-id="011be-181">Configurer les paramètres de démarrage, de page d’accueil et de nouvelle page d’onglets</span><span class="sxs-lookup"><span data-stu-id="011be-181">Configure start-up, home page, and new tab page settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startup-home-page-and-new-tab-page)
- [<span data-ttu-id="011be-182">Configurer le paramètre de jeu de surf</span><span class="sxs-lookup"><span data-stu-id="011be-182">Configure Surf game setting</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowsurfgame)
- [<span data-ttu-id="011be-183">Configurer les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="011be-183">Configure proxy server settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#proxy-server)

