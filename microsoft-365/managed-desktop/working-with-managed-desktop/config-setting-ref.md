---
title: Référence des paramètres configurables pour le bureau géré Microsoft
description: Définition des catégories pour les paramètres configurables dans le bureau géré Microsoft
keywords: Microsoft maNaged Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: trudyha
ms.localizationpriority: normal
ms.date: 2/14/2019
ms.openlocfilehash: 1f0301f8660fd7ff60bd347d0d7b88c629d79453
ms.sourcegitcommit: 59bc66eaa2575bad8ecb34d45b1172cda23a729b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "30051095"
---
# <a name="configurable-settings-reference---microsoft-managed-desktop"></a><span data-ttu-id="bdd96-104">Référence des paramètres configurables-bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="bdd96-104">Configurable settings reference - Microsoft Managed Desktop</span></span>

<span data-ttu-id="bdd96-p101">Cette rubrique répertorie les catégories de paramètres que les clients peuvent configurer avec le bureau géré Microsoft. Chaque catégorie de paramètres comprend des informations sur les exigences, les meilleures pratiques et la personnalisation de la catégorie de paramètres.</span><span class="sxs-lookup"><span data-stu-id="bdd96-p101">This topic lists the settings categories that customers can configure with Microsoft Managed Desktop. Each setting category includes info on requirements, best practices, and how to customize the setting category.</span></span> 

## <a name="desktop-background-picture"></a><span data-ttu-id="bdd96-107">Image d'arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="bdd96-107">Desktop background picture</span></span>
<span data-ttu-id="bdd96-p102">Vous pouvez personnaliser l'image d'arrière-plan du Bureau pour les appareils de bureau gérés Microsoft dans votre organisation. Vous pouvez l'utiliser pour appliquer une marque de société ou une promotion</span><span class="sxs-lookup"><span data-stu-id="bdd96-p102">You can customize the desktop background picture for Microsoft Managed Desktop devices in your organization. You might use this to apply a company brand or marketing</span></span> 

### <a name="requirements"></a><span data-ttu-id="bdd96-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdd96-110">Requirements</span></span>

<span data-ttu-id="bdd96-111">Ces conditions doivent être remplies pour une image d'arrière-plan de bureau:</span><span class="sxs-lookup"><span data-stu-id="bdd96-111">These requirements must be met for a desktop background picture:</span></span>
- <span data-ttu-id="bdd96-112">Format de fichier image-. jpg, JPEG ou. png</span><span class="sxs-lookup"><span data-stu-id="bdd96-112">Picture file format - .jpg, jpeg, or .png</span></span>
- <span data-ttu-id="bdd96-113">Emplacement des fichiers: héberger sur un emplacement HTTPS sécurisé (https) approuvé.</span><span class="sxs-lookup"><span data-stu-id="bdd96-113">File location - Host on a trusted secure http (https) location.</span></span> 
- <span data-ttu-id="bdd96-114">Non autorisé-les emplacements http et de partage de fichiers (UNC) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bdd96-114">Not allowed - Http and file share (unc) locations are not supported.</span></span> 

### <a name="customize-and-deploy-desktop-background-picture"></a><span data-ttu-id="bdd96-115">Personnaliser et déployer une image d'arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="bdd96-115">Customize and deploy desktop background picture</span></span>

<span data-ttu-id="bdd96-116">**Pour ajouter une image d'arrière-plan personnalisée du Bureau**</span><span class="sxs-lookup"><span data-stu-id="bdd96-116">**To add a custom desktop background picture**</span></span>
1. <span data-ttu-id="bdd96-117">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="bdd96-117">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="bdd96-118">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-118">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="bdd96-119">Dans espace de travail **configurable** , sélectionnez **image d'arrière-plan du Bureau**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-119">In **Configurable** workspace, select **Desktop background picture**.</span></span> 
4. <span data-ttu-id="bdd96-120">Entrez l'emplacement de l'image que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="bdd96-120">Enter the location of the picture you want to use.</span></span> 
5. <span data-ttu-id="bdd96-121">Sélectionnez **stage Deployment** pour enregistrer vos modifications et les déployer sur l'anneau de test.</span><span class="sxs-lookup"><span data-stu-id="bdd96-121">Select **Stage deployment** to save your changes and deploy them to the Test ring.</span></span> 

## <a name="browser-start-pages"></a><span data-ttu-id="bdd96-122">Pages de démarrage du navigateur</span><span class="sxs-lookup"><span data-stu-id="bdd96-122">Browser start pages</span></span>
<span data-ttu-id="bdd96-p103">Les pages de démarrage de navigateur s'ouvrent dans des onglets individuels lorsque les utilisateurs démarrent Microsoft Edge. Si vous souhaitez que vos utilisateurs puissent facilement ouvrir un ensemble de sites qu'ils utilisent fréquemment, ajoutez une page de démarrage de navigateur pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="bdd96-p103">Browser start pages open in individual tabs when your users start Microsoft Edge. If you want to make it easy for your users to open a set of sites that they use frequently, add a browser start page for each site.</span></span> 

### <a name="requirements"></a><span data-ttu-id="bdd96-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdd96-125">Requirements</span></span>

<span data-ttu-id="bdd96-p104">Vous devez indiquer le nom de domaine complet (FQDN) pour les sites intranet ou Internet pour les pages de démarrage de votre navigateur. Si des sites internes sont configurés, indiquez aux utilisateurs que l'accès à ces sites est uniquement autorisé lorsqu'ils sont connectés au réseau interne au bureau ou lorsqu'ils sont connectés à l'aide d'une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="bdd96-p104">You must provide the fully qualified domain name (FQDN) for intranet or Internet sites for your browser start pages. If internal sites are configured, let users know that access to these sites is only allowed when connected to the internal network when in the office, or when connected with a VPN connection.</span></span> 

### <a name="customize-and-deploy-browser-start-pages"></a><span data-ttu-id="bdd96-128">Personnaliser et déployer des pages de démarrage de navigateur</span><span class="sxs-lookup"><span data-stu-id="bdd96-128">Customize and deploy browser start pages</span></span>

<span data-ttu-id="bdd96-129">**Pour ajouter une page de démarrage de navigateur**</span><span class="sxs-lookup"><span data-stu-id="bdd96-129">**To add a browser start page**</span></span>
1. <span data-ttu-id="bdd96-130">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="bdd96-130">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="bdd96-131">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-131">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="bdd96-132">Dans espace de travail **configurable** , sélectionnez **pages de démarrage du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-132">In **Configurable** workspace, select **Browser start pages**.</span></span> 
4. <span data-ttu-id="bdd96-133">Sélectionnez **Ajouter une page de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-133">Select **Add start page**.</span></span>
5. <span data-ttu-id="bdd96-134">Dans **Ajouter la page de démarrage du navigateur**, entrez l'URL du site que vous souhaitez utiliser, puis sélectionnez **Ajouter une page de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-134">On **Add browser start page**, enter the URL for the site you want to use, and then select **Add start page**.</span></span> 
6. <span data-ttu-id="bdd96-135">Répétez les étapes 1-5 pour les pages de démarrage de navigateur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bdd96-135">Repeat steps 1-5 for additional browser start pages.</span></span> 
7. <span data-ttu-id="bdd96-136">Sélectionnez **stage Deployment** pour enregistrer vos modifications et les déployer sur l'anneau de test.</span><span class="sxs-lookup"><span data-stu-id="bdd96-136">Select **Stage deployment** to save your changes and deploy them to the Test ring.</span></span>

## <a name="enterprise-mode-site-list-location"></a><span data-ttu-id="bdd96-137">Emplacement de la liste de sites en mode entreprise</span><span class="sxs-lookup"><span data-stu-id="bdd96-137">Enterprise mode site list location</span></span>

<span data-ttu-id="bdd96-p105">Si vous avez des sites Web et des applications spécifiques dont vous connaissez qu'il existe des problèmes de compatibilité avec Microsoft Edge, vous pouvez utiliser la liste des sites en mode entreprise pour que les sites Web s'ouvrent automatiquement à l'aide d'Internet Explorer 11. En outre, si vous savez que vos sites intranet ne fonctionnent pas correctement avec Microsoft Edge, vous pouvez configurer tous les sites intranet pour qu'ils s'ouvrent automatiquement à l'aide d'Internet Explorer 11. L'utilisation du mode entreprise signifie que vous pouvez continuer à utiliser Microsoft Edge comme navigateur par défaut, tout en vous assurant que vos applications continuent de fonctionner sur Internet Explorer 11. Pour plus d'informations sur les listes de sites en mode entreprise, consultez la rubrique [Enterprise mode and Enterprise mode site lists](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode).</span><span class="sxs-lookup"><span data-stu-id="bdd96-p105">If you have specific websites and apps that you know have compatibility problems with Microsoft Edge, you can use the Enterprise Mode site list so that the websites automatically open using Internet Explorer 11. Also, if you know that your intranet sites aren't going to work correctly with Microsoft Edge, you can set all intranet sites to open using Internet Explorer 11 automatically. Using Enterprise Mode means that you can continue to use Microsoft Edge as your default browser, while also ensuring that your apps continue working on Internet Explorer 11. For more information on enterprise mode site lists,see [Enterprise Mode and Enterprise Mode Site Lists](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode).</span></span> 

<span data-ttu-id="bdd96-142">Vous pouvez spécifier un emplacement https://ou l'emplacement d'un partage interne où vous avez hébergé votre liste de sites en mode entreprise.</span><span class="sxs-lookup"><span data-stu-id="bdd96-142">You can specify an https:// location, or the location for an internal share where you’ve hosted your enterprise mode site list.</span></span> 

### <a name="requirements"></a><span data-ttu-id="bdd96-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdd96-143">Requirements</span></span>

<span data-ttu-id="bdd96-144">Ces exigences doivent être satisfaites pour le fichier de liste de sites en mode entreprise:</span><span class="sxs-lookup"><span data-stu-id="bdd96-144">These requirements must be met for the enterprise mode site list file:</span></span>
- <span data-ttu-id="bdd96-145">Format de fichier: fichier XML qui répond aux [exigences de fichier](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#site-list-xml-file)</span><span class="sxs-lookup"><span data-stu-id="bdd96-145">File format - XML file that meets [file requirements](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#site-list-xml-file)</span></span>
- <span data-ttu-id="bdd96-146">Emplacement des fichiers: fichier hôte sur un emplacement https interne.</span><span class="sxs-lookup"><span data-stu-id="bdd96-146">File location - Host file on an internal https location.</span></span> 
- <span data-ttu-id="bdd96-147">Non autorisé-l'hébergement sur un partage de fichiers interne, comme *//ShareName*, n'est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="bdd96-147">Not allowed - Hosting on an internal file share, like *//sharename*, is not allowed</span></span>

### <a name="best-practices"></a><span data-ttu-id="bdd96-148">Meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="bdd96-148">Best practices</span></span>

<span data-ttu-id="bdd96-149">Ces meilleures pratiques sont proposées pour aider les clients à prendre des décisions pour moderniser leur infrastructure informatique:</span><span class="sxs-lookup"><span data-stu-id="bdd96-149">These best practices are offered to help customers make decisions to modernize their IT infrastructure:</span></span>
- <span data-ttu-id="bdd96-p106">**Choisir un nombre limité de sites** : Microsoft Managed Desktop utilise Microsoft Edge comme navigateur favori pour améliorer la sécurité globale pour votre organisation et la convivialité de vos utilisateurs. La plupart des sites de cette liste sont destinés aux applications Web héritées qui ont besoin d'une version plus ancienne d'un navigateur qui n'inclut pas autant de fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bdd96-p106">**Choose a limited number of sites** – Microsoft Managed Desktop uses Microsoft Edge as the preferred browser to improve overall security for your organization and usability for your users. Most sites in this list are for legacy web apps that need an older version of a browser that will not include as many security features.</span></span> 
- <span data-ttu-id="bdd96-p107">Songez à utiliser un **autre** site ou une application Web qui ne nécessite pas un navigateur plus ancien. Vous pouvez également mettre à jour le site afin qu'il puisse utiliser des navigateurs plus récents. Les navigateurs plus récents utilisent la technologie la plus récente et contribuent à l'amélioration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="bdd96-p107">**Consider an alternate** – Consider a different site, or web app that doesn’t require an older browser. Or, consider updating the site so that it can use newer browsers. Newer browsers use the latest technology and help improve security.</span></span>

### <a name="customize-and-deploy-enterprise-site-mode-list-location"></a><span data-ttu-id="bdd96-155">Personnaliser et déployer l'emplacement de liste en mode site d'entreprise</span><span class="sxs-lookup"><span data-stu-id="bdd96-155">Customize and deploy Enterprise site mode list location</span></span>

<span data-ttu-id="bdd96-156">**Pour ajouter un emplacement de liste en mode site d'entreprise**</span><span class="sxs-lookup"><span data-stu-id="bdd96-156">**To add an enterprise site mode list location**</span></span>

1.  <span data-ttu-id="bdd96-157">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="bdd96-157">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2.  <span data-ttu-id="bdd96-158">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-158">Under **Settings**, select **Configurable**.</span></span>
3.  <span data-ttu-id="bdd96-159">Dans espace de travail **configurable** , sélectionnez l'emplacement de la **liste de sites en mode entreprise**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-159">In **Configurable** workspace, select **Enterprise mode site list location**.</span></span> 
4.  <span data-ttu-id="bdd96-160">Entrez l'emplacement https de votre liste de sites.</span><span class="sxs-lookup"><span data-stu-id="bdd96-160">Enter the https location for your site list.</span></span> 
5.  <span data-ttu-id="bdd96-161">Sélectionnez **stage Deployment** pour enregistrer vos modifications et les déployer sur l'anneau de test.</span><span class="sxs-lookup"><span data-stu-id="bdd96-161">Select **Stage deployment** to save your changes and deploy them to the Test ring.</span></span>

## <a name="trusted-sites"></a><span data-ttu-id="bdd96-162">Sites de confiance</span><span class="sxs-lookup"><span data-stu-id="bdd96-162">Trusted sites</span></span>

<span data-ttu-id="bdd96-p108">Les sites de confiance vous permettent de personnaliser les zones de sécurité ou d'utiliser un site, pour différents sites. Les zones de sécurité sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="bdd96-p108">Trusted sites allow you to customize security zones, or where a site can be used, for different sites. Security zones include:</span></span> 
- <span data-ttu-id="bdd96-165">Zone 1 – zone Intranet local</span><span class="sxs-lookup"><span data-stu-id="bdd96-165">Zone 1 – Local Intranet zone</span></span>
- <span data-ttu-id="bdd96-166">Zone 2: zone sites de confiance</span><span class="sxs-lookup"><span data-stu-id="bdd96-166">Zone 2 – Trusted sites zone</span></span>
- <span data-ttu-id="bdd96-167">Zone 3 – zone Internet</span><span class="sxs-lookup"><span data-stu-id="bdd96-167">Zone 3 – Internet zone</span></span>
- <span data-ttu-id="bdd96-168">Zone 4 – zone sites sensibles</span><span class="sxs-lookup"><span data-stu-id="bdd96-168">Zone 4 – Restricted Sites zone</span></span>

### <a name="requirements"></a><span data-ttu-id="bdd96-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdd96-169">Requirements</span></span>

<span data-ttu-id="bdd96-170">Fournissez le nom de domaine complet (FQDN) pour les sites intranet ou Internet de chaque site approuvé.</span><span class="sxs-lookup"><span data-stu-id="bdd96-170">Provide the fully qualified domain name (FQDN) for intranet or Internet sites for each trusted site.</span></span> 

### <a name="customize-and-deploy-trusted-sites"></a><span data-ttu-id="bdd96-171">Personnaliser et déployer des sites de confiance</span><span class="sxs-lookup"><span data-stu-id="bdd96-171">Customize and deploy trusted sites</span></span>

<span data-ttu-id="bdd96-172">**Pour ajouter un site de confiance**</span><span class="sxs-lookup"><span data-stu-id="bdd96-172">**To add a trusted site**</span></span>

1. <span data-ttu-id="bdd96-173">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="bdd96-173">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="bdd96-174">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-174">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="bdd96-175">Dans espace de travail **configurable** , sélectionnez **sites de confiance**, puis **Ajouter un site approuvé**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-175">In **Configurable** workspace, select **Trusted sites**, and then select **Add trusted site**.</span></span> 
4. <span data-ttu-id="bdd96-176">Sur **Ajouter un site approuvé**, entrez l'URL, choisissez une zone de sécurité, puis sélectionnez **Ajouter un site approuvé**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-176">On **Add trusted site**, enter the URL, choose a security zone, and then select **Add trusted site**.</span></span> 
5. <span data-ttu-id="bdd96-177">Répétez les étapes 1-4 pour chaque site approuvé que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="bdd96-177">Repeat steps 1-4 for each trusted site you want to add.</span></span> 
6. <span data-ttu-id="bdd96-178">Sélectionnez **stage Deployment** pour enregistrer vos modifications et les déployer sur l'anneau de test.</span><span class="sxs-lookup"><span data-stu-id="bdd96-178">Select **Stage deployment** to save your changes and deploy them to the Test ring.</span></span>

<span data-ttu-id="bdd96-179">**Pour supprimer un site approuvé**</span><span class="sxs-lookup"><span data-stu-id="bdd96-179">**To remove a trusted site**</span></span>

1. <span data-ttu-id="bdd96-180">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="bdd96-180">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="bdd96-181">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-181">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="bdd96-182">Dans espace de travail **configurable** , sélectionnez **sites de confiance**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-182">In **Configurable** workspace, select **Trusted sites**.</span></span> 
4. <span data-ttu-id="bdd96-183">Sélectionnez le site que vous souhaitez supprimer, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-183">Select the site that you want to delete, and then select **Delete**.</span></span> 
5. <span data-ttu-id="bdd96-184">Répétez les étapes 1-4 pour chaque site approuvé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bdd96-184">Repeat steps 1-4 for each trusted site you want to delete.</span></span> 
6. <span data-ttu-id="bdd96-185">Sélectionnez **stage Deployment** pour enregistrer vos modifications et les déployer sur l'anneau de test.</span><span class="sxs-lookup"><span data-stu-id="bdd96-185">Select **Stage deployment** to save your changes and deploy them to the Test ring.</span></span>

## <a name="proxy"></a><span data-ttu-id="bdd96-186">Proxy.</span><span class="sxs-lookup"><span data-stu-id="bdd96-186">Proxy</span></span>
<span data-ttu-id="bdd96-p109">Vous pouvez gérer les paramètres de proxy réseau pour votre organisation. Ajoutez votre serveur proxy et votre numéro de port, puis ajoutez les exceptions de votre site proxy. Microsoft maNaged Desktop inclut un ensemble d'exceptions de proxy par défaut qui sont requises pour le fonctionnement du service. La liste d'exclusion par défaut ne peut être modifiée que par le service bureau géré Microsoft.  Pour plus d'informations, consultez la rubrique [Configuration réseau pour Microsoft Managed Desktop](../get-ready/network.md).</span><span class="sxs-lookup"><span data-stu-id="bdd96-p109">You can manage network proxy settings for your organization. Add your proxy server and port number, and then add your proxy site exceptions. Microsoft Managed Desktop includes a set of default proxy exceptions that are required for the service to operate. The default exclusion list may only be modified by the Microsoft Managed Desktop service.  For more information, see [Network configuration for Microsoft Managed Desktop](../get-ready/network.md).</span></span> 

<span data-ttu-id="bdd96-192">Les exceptions de site proxy que vous ajoutez dans le portail de bureau géré Microsoft sont ajoutées aux exceptions de proxy par défaut fournies avec le service bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bdd96-192">The proxy site exceptions that you add in the Microsoft Managed Desktop portal are added to the default proxy exceptions included with Microsoft Managed Desktop service.</span></span> 

> [!NOTE]
> <span data-ttu-id="bdd96-p110">La mise à jour de la liste des exceptions de proxy par défaut est toujours prioritaire sur les déploiements des clients. Cela signifie que votre déploiement intermédiaire sera suspendu s'il existe un déploiement pour la liste des exceptions de proxy par défaut.</span><span class="sxs-lookup"><span data-stu-id="bdd96-p110">Updating the default proxy exception list is always prioritized over customer deployments. This means that your staged deployment will be paused if there is a deployment for the default proxy exception list.</span></span>  

### <a name="requirements"></a><span data-ttu-id="bdd96-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdd96-195">Requirements</span></span>

<span data-ttu-id="bdd96-196">Ces exigences doivent être satisfaites pour les exceptions de serveur proxy et de site proxy:</span><span class="sxs-lookup"><span data-stu-id="bdd96-196">These requirements must be met for proxy server and proxy site exceptions:</span></span>
- <span data-ttu-id="bdd96-197">Doit être une adresse de serveur et un numéro de port valides</span><span class="sxs-lookup"><span data-stu-id="bdd96-197">Must be a valid server address and port number</span></span>
- <span data-ttu-id="bdd96-198">Les URL doivent être un site http valide</span><span class="sxs-lookup"><span data-stu-id="bdd96-198">URLs must be a valid http site</span></span> 

### <a name="customize-and-deploy-proxies"></a><span data-ttu-id="bdd96-199">Personnaliser et déployer des proxys</span><span class="sxs-lookup"><span data-stu-id="bdd96-199">Customize and deploy proxies</span></span>

<span data-ttu-id="bdd96-200">**Pour ajouter une exception de site proxy individuelle**</span><span class="sxs-lookup"><span data-stu-id="bdd96-200">**To add an individual proxy site exception**</span></span>

1. <span data-ttu-id="bdd96-201">Se connecter au [portail d'administration de bureau géré Microsoft](http://aka.ms/mwaasportal)</span><span class="sxs-lookup"><span data-stu-id="bdd96-201">Sign in to [Microsoft Managed Desktop Admin portal](http://aka.ms/mwaasportal)</span></span>
2. <span data-ttu-id="bdd96-202">Sous **paramètres**, sélectionnez **configurable**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-202">Under **Settings**, select **Configurable**.</span></span>
3. <span data-ttu-id="bdd96-203">Dans espace de travail **configurable** , sélectionnez **proxy**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-203">In **Configurable** workspace, select **Proxy**.</span></span> 
4. <span data-ttu-id="bdd96-204">Entrez l' **adresse** et le **numéro de port** de votre serveur proxy, puis sélectionnez Ajouter une exception de **proxy**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-204">Enter the **Address** and **Port number** for you proxy server, and then select **Add proxy exception**.</span></span> 
5. <span data-ttu-id="bdd96-205">Entrez l'URL d'un site http valide, puis sélectionnez **Ajouter une exception de proxy**.</span><span class="sxs-lookup"><span data-stu-id="bdd96-205">Enter the URL of a valid http site, and then select **Add proxy exception**.</span></span> 
6. <span data-ttu-id="bdd96-206">Répétez les étapes 1-5 pour chaque site approuvé que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="bdd96-206">Repeat steps 1-5 for each trusted site you want to add.</span></span> 
7. <span data-ttu-id="bdd96-207">Sélectionnez **stage Deployment** pour enregistrer vos modifications et les déployer sur l'anneau de test.</span><span class="sxs-lookup"><span data-stu-id="bdd96-207">Select **Stage deployment** to save your changes and deploy them to the Test ring.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdd96-208">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="bdd96-208">Additional resources</span></span>
- [<span data-ttu-id="bdd96-209">Vue d'ensemble des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="bdd96-209">Configurable settings overview</span></span>](config-setting-overview.md) 
- [<span data-ttu-id="bdd96-210">Déployer des paramètres configurables</span><span class="sxs-lookup"><span data-stu-id="bdd96-210">Deploy configurable settings</span></span>](config-setting-deploy.md)