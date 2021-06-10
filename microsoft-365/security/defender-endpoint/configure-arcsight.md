---
title: Configurer Micro Focus ArcSight pour tirer Microsoft Defender pour les détections de points de terminaison
description: Configurer Micro Focus ArcSight pour recevoir et tirer des détections à partir de Centre de sécurité Microsoft Defender
keywords: configurer Micro Focus ArcSight, outils de gestion des informations de sécurité et des événements, arcsight
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
ms.openlocfilehash: a52f810647c387c5a5726b9d31998c34add4092e
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166184"
---
# <a name="configure-micro-focus-arcsight-to-pull-defender-for-endpoint-detections"></a><span data-ttu-id="ed358-104">Configurer Micro Focus ArcSight pour tirer Defender pour les détections de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ed358-104">Configure Micro Focus ArcSight to pull Defender for Endpoint detections</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ed358-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ed358-105">**Applies to:**</span></span>
- [<span data-ttu-id="ed358-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ed358-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ed358-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ed358-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="ed358-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="ed358-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ed358-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ed358-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configurearcsight-abovefoldlink) 

<span data-ttu-id="ed358-110">Vous devez installer et configurer certains fichiers et outils pour utiliser Micro Focus ArcSight afin qu’il puisse tirer Defender pour les détections de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ed358-110">You'll need to install and configure some files and tools to use Micro Focus ArcSight so that it can pull Defender for Endpoint detections.</span></span>

>[!Note]
>- <span data-ttu-id="ed358-111">[Defender pour l’alerte de point de terminaison](alerts.md) se compose d’une ou de plusieurs détections</span><span class="sxs-lookup"><span data-stu-id="ed358-111">[Defender for Endpoint Alert](alerts.md) is composed from one or more detections</span></span>
>- <span data-ttu-id="ed358-112">[Defender for Endpoint Detection est](api-portal-mapping.md) composé de l’événement suspect qui s’est produit sur l’appareil et de ses détails d’alerte associés.</span><span class="sxs-lookup"><span data-stu-id="ed358-112">[Defender for Endpoint Detection](api-portal-mapping.md) is composed from the suspicious event occurred on the Device and its related Alert details.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ed358-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ed358-113">Before you begin</span></span>

<span data-ttu-id="ed358-114">La configuration de l’outil Micro Focus ArcSight Connector nécessite plusieurs fichiers de configuration pour qu’il tire et pare les détections à partir de votre application Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="ed358-114">Configuring the Micro Focus ArcSight Connector tool requires several configuration files for it to pull and parse detections from your Azure Active Directory (AAD) application.</span></span>

<span data-ttu-id="ed358-115">Cette section vous guide dans l’obtention des informations nécessaires pour définir et utiliser correctement les fichiers de configuration requis.</span><span class="sxs-lookup"><span data-stu-id="ed358-115">This section guides you in getting the necessary information to set and use the required configuration files correctly.</span></span>

- <span data-ttu-id="ed358-116">Assurez-vous que vous avez activé la fonctionnalité d’intégration SIEM à partir **Paramètres** menu.</span><span class="sxs-lookup"><span data-stu-id="ed358-116">Make sure you have enabled the SIEM integration feature from the **Settings** menu.</span></span> <span data-ttu-id="ed358-117">Pour plus d’informations, voir [Enable SIEM integration in Defender for Endpoint](enable-siem-integration.md).</span><span class="sxs-lookup"><span data-stu-id="ed358-117">For more information, see [Enable SIEM integration in Defender for Endpoint](enable-siem-integration.md).</span></span>

- <span data-ttu-id="ed358-118">Préparez le fichier que vous avez enregistré en activant la fonctionnalité d’intégration SIEM.</span><span class="sxs-lookup"><span data-stu-id="ed358-118">Have the file you saved from enabling the SIEM integration feature ready.</span></span> <span data-ttu-id="ed358-119">Vous devez obtenir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed358-119">You'll need to get the following values:</span></span>
  - <span data-ttu-id="ed358-120">URL d’actualisation du jeton OAuth 2.0</span><span class="sxs-lookup"><span data-stu-id="ed358-120">OAuth 2.0 Token refresh URL</span></span>
  - <span data-ttu-id="ed358-121">OAuth 2.0 Client ID</span><span class="sxs-lookup"><span data-stu-id="ed358-121">OAuth 2.0 Client ID</span></span>
  - <span data-ttu-id="ed358-122">OAuth 2.0 Client Secret</span><span class="sxs-lookup"><span data-stu-id="ed358-122">OAuth 2.0 Client secret</span></span>

- <span data-ttu-id="ed358-123">Préparez les fichiers de configuration suivants :</span><span class="sxs-lookup"><span data-stu-id="ed358-123">Have the following configuration files ready:</span></span>
  - <span data-ttu-id="ed358-124">WDATP-connector.properties</span><span class="sxs-lookup"><span data-stu-id="ed358-124">WDATP-connector.properties</span></span>
  - <span data-ttu-id="ed358-125">WDATP-connector.jsonparser.properties</span><span class="sxs-lookup"><span data-stu-id="ed358-125">WDATP-connector.jsonparser.properties</span></span>

    <span data-ttu-id="ed358-126">Vous ariez enregistré un fichier .zip qui contient ces deux fichiers lorsque vous avez choisi Micro Focus ArcSight comme type SIEM que vous utilisez dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ed358-126">You would have saved a .zip file which contains these two files when you chose Micro Focus ArcSight as the SIEM type you use in your organization.</span></span>

- <span data-ttu-id="ed358-127">Veillez à générer les jetons suivants et à les préparer :</span><span class="sxs-lookup"><span data-stu-id="ed358-127">Make sure you generate the following tokens and have them ready:</span></span>
  - <span data-ttu-id="ed358-128">Access token (Jeton d’accès)</span><span class="sxs-lookup"><span data-stu-id="ed358-128">Access token</span></span>
  - <span data-ttu-id="ed358-129">Jeton d’actualisation</span><span class="sxs-lookup"><span data-stu-id="ed358-129">Refresh token</span></span>

  <span data-ttu-id="ed358-130">Vous pouvez générer ces jetons à partir de la section de configuration de **l’intégration SIEM** du portail.</span><span class="sxs-lookup"><span data-stu-id="ed358-130">You can generate these tokens from the **SIEM integration** setup section of the portal.</span></span>

## <a name="install-and-configure-micro-focus-arcsight-flexconnector"></a><span data-ttu-id="ed358-131">Installer et configurer Micro Focus ArcSight FlexConnector</span><span class="sxs-lookup"><span data-stu-id="ed358-131">Install and configure Micro Focus ArcSight FlexConnector</span></span>

<span data-ttu-id="ed358-132">Les étapes suivantes supposent que vous avez effectué toutes les étapes requises dans [Avant de commencer.](#before-you-begin)</span><span class="sxs-lookup"><span data-stu-id="ed358-132">The following steps assume that you have completed all the required steps in [Before you begin](#before-you-begin).</span></span>

1. <span data-ttu-id="ed358-133">Installez le dernier programme d’installation Windows 32 bits de FlexConnector.</span><span class="sxs-lookup"><span data-stu-id="ed358-133">Install the latest 32-bit Windows FlexConnector installer.</span></span> <span data-ttu-id="ed358-134">Vous pouvez le trouver dans le centre logiciel HPE.</span><span class="sxs-lookup"><span data-stu-id="ed358-134">You can find this in the HPE Software center.</span></span> <span data-ttu-id="ed358-135">L’outil est généralement installé à l’emplacement par défaut suivant : `C:\Program Files\ArcSightFlexConnectors\current\bin` .</span><span class="sxs-lookup"><span data-stu-id="ed358-135">The tool is typically installed in the following default location: `C:\Program Files\ArcSightFlexConnectors\current\bin`.</span></span></br></br><span data-ttu-id="ed358-136">Vous pouvez choisir où enregistrer l’outil, par exemple C : \\ *folder_location*\current\bin *où folder_location* représente l’emplacement d’installation.</span><span class="sxs-lookup"><span data-stu-id="ed358-136">You can choose where to save the tool, for example C:\\*folder_location*\current\bin where *folder_location* represents the installation location.</span></span>

2. <span data-ttu-id="ed358-137">Suivez l’Assistant Installation à travers les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed358-137">Follow the installation wizard through the following tasks:</span></span>
   - <span data-ttu-id="ed358-138">Introduction</span><span class="sxs-lookup"><span data-stu-id="ed358-138">Introduction</span></span>
   - <span data-ttu-id="ed358-139">Choose Install Folder</span><span class="sxs-lookup"><span data-stu-id="ed358-139">Choose Install Folder</span></span>
   - <span data-ttu-id="ed358-140">Choose Install Set</span><span class="sxs-lookup"><span data-stu-id="ed358-140">Choose Install Set</span></span>
   - <span data-ttu-id="ed358-141">Choose Shortcut Folder</span><span class="sxs-lookup"><span data-stu-id="ed358-141">Choose Shortcut Folder</span></span>
   - <span data-ttu-id="ed358-142">Résumé de la pré-installation</span><span class="sxs-lookup"><span data-stu-id="ed358-142">Pre-Installation Summary</span></span>
   - <span data-ttu-id="ed358-143">Installation...</span><span class="sxs-lookup"><span data-stu-id="ed358-143">Installing...</span></span>

   <span data-ttu-id="ed358-144">Vous pouvez conserver les valeurs par défaut pour chacune de ces tâches ou modifier la sélection en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ed358-144">You can keep the default values for each of these tasks or modify the selection to suit your requirements.</span></span>

3. <span data-ttu-id="ed358-145">Ouvrez l’Explorateur de fichiers et recherchez les deux fichiers de configuration que vous avez enregistrés lorsque vous avez activé la fonctionnalité d’intégration SIEM.</span><span class="sxs-lookup"><span data-stu-id="ed358-145">Open File Explorer and locate the two configuration files you saved when you enabled the SIEM integration feature.</span></span> <span data-ttu-id="ed358-146">Placez les deux fichiers à l’emplacement d’installation de FlexConnector, par exemple :</span><span class="sxs-lookup"><span data-stu-id="ed358-146">Put the two files in the FlexConnector installation location, for example:</span></span>

   - <span data-ttu-id="ed358-147">WDATP-connector.jsonparser.properties : C: \\ *folder_location*\current\user\agent\flexagent</span><span class="sxs-lookup"><span data-stu-id="ed358-147">WDATP-connector.jsonparser.properties: C:\\*folder_location*\current\user\agent\flexagent</span></span>\

   - <span data-ttu-id="ed358-148">WDATP-connector.properties: C: \\ *folder_location*\current\user\agent\flexagent</span><span class="sxs-lookup"><span data-stu-id="ed358-148">WDATP-connector.properties: C:\\*folder_location*\current\user\agent\flexagent</span></span>\

   > [!NOTE]
   > 
   > <span data-ttu-id="ed358-149">Vous devez placer les fichiers de configuration à cet emplacement, où *folder_location* représente l’emplacement où vous avez installé l’outil.</span><span class="sxs-lookup"><span data-stu-id="ed358-149">You must put the configuration files in this location, where *folder_location* represents the location where you installed the tool.</span></span>

4. <span data-ttu-id="ed358-150">Une fois l’installation du connecteur principal terminée, la fenêtre d’installation du connecteur s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ed358-150">After the installation of the core connector completes, the Connector Setup window opens.</span></span> <span data-ttu-id="ed358-151">Dans la fenêtre d’installation du connecteur, **sélectionnez Ajouter un connecteur.**</span><span class="sxs-lookup"><span data-stu-id="ed358-151">In the Connector Setup window, select **Add a Connector**.</span></span>

5. <span data-ttu-id="ed358-152">Select Type: **ArcSight FlexConnector REST** and click **Next**.</span><span class="sxs-lookup"><span data-stu-id="ed358-152">Select Type: **ArcSight FlexConnector REST** and click **Next**.</span></span>

6. <span data-ttu-id="ed358-153">Tapez les informations suivantes dans le formulaire de détails des paramètres.</span><span class="sxs-lookup"><span data-stu-id="ed358-153">Type the following information in the parameter details form.</span></span> <span data-ttu-id="ed358-154">Toutes les autres valeurs du formulaire sont facultatives et peuvent être laissées vides.</span><span class="sxs-lookup"><span data-stu-id="ed358-154">All other values in the form are optional and can be left blank.</span></span>

   <table>
    <tbody style="vertical-align:top;">
    <tr>
    <th><span data-ttu-id="ed358-155">Champ</span><span class="sxs-lookup"><span data-stu-id="ed358-155">Field</span></span></th>
    <th><span data-ttu-id="ed358-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed358-156">Value</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="ed358-157">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="ed358-157">Configuration File</span></span></td>
    <td><span data-ttu-id="ed358-158">Tapez le nom du fichier de propriétés client.</span><span class="sxs-lookup"><span data-stu-id="ed358-158">Type in the name of the client property file.</span></span> <span data-ttu-id="ed358-159">Le nom doit correspondre au fichier fourni dans la .zip que vous avez téléchargée.</span><span class="sxs-lookup"><span data-stu-id="ed358-159">The name must match the file provided in the .zip that you downloaded.</span></span>
<span data-ttu-id="ed358-160">Par exemple, si le fichier de configuration dans le répertoire flexagent est nommé &quot; &quot;WDATP-Connector.jsonparser.properties , vous devez taper &quot; &quot; &quot; WDATP-Connector comme nom du fichier de &quot; propriétés du client.</span><span class="sxs-lookup"><span data-stu-id="ed358-160">For example, if the configuration file in &quot;flexagent&quot; directory is named &quot;WDATP-Connector.jsonparser.properties&quot;, you must type &quot;WDATP-Connector&quot; as the name of the client property file.</span></span></td>
    </tr>
    <td><span data-ttu-id="ed358-161">URL des événements</span><span class="sxs-lookup"><span data-stu-id="ed358-161">Events URL</span></span></td>
    <td><span data-ttu-id="ed358-162">Selon l’emplacement de votre centre de données, sélectionnez l’URL de l’UE ou des États-Unis :</span><span class="sxs-lookup"><span data-stu-id="ed358-162">Depending on the location of your datacenter, select either the EU or the US URL:</span></span> </br></br> <span data-ttu-id="ed358-163"><b>Pour l’UE</b>: https:// <i></i> wdatp-alertexporter-eu.windows.com/api/alerts/?sinceTimeUtc=$START_AT_TIME</span><span class="sxs-lookup"><span data-stu-id="ed358-163"><b>For EU</b>:  https://<i></i>wdatp-alertexporter-eu.windows.com/api/alerts/?sinceTimeUtc=$START_AT_TIME</span></span> <br>
   </br><span data-ttu-id="ed358-164"><b>Pour les</b> États-Https:// <i></i> :tp-alertexporter-us.windows.com/api/alerts/?sinceTimeUtc=$START_AT_TIME</span><span class="sxs-lookup"><span data-stu-id="ed358-164"><b>For US:</b> https://<i></i>wdatp-alertexporter-us.windows.com/api/alerts/?sinceTimeUtc=$START_AT_TIME</span></span> <br> <br> <span data-ttu-id="ed358-165"><b>For UK</b>: https:// <i></i> wdatp-alertexporter-uk.windows.com/api/alerts/?sinceTimeUtc=$START_AT_TIME</span><span class="sxs-lookup"><span data-stu-id="ed358-165"><b>For UK</b>:  https://<i></i>wdatp-alertexporter-uk.windows.com/api/alerts/?sinceTimeUtc=$START_AT_TIME</span></span></td>
    <tr>
    <td><span data-ttu-id="ed358-166">Type d’authentification</span><span class="sxs-lookup"><span data-stu-id="ed358-166">Authentication Type</span></span></td>
    <td><span data-ttu-id="ed358-167">OAuth 2</span><span class="sxs-lookup"><span data-stu-id="ed358-167">OAuth 2</span></span></td>
    </tr>
    <td><span data-ttu-id="ed358-168">Fichier de propriétés du client OAuth 2</span><span class="sxs-lookup"><span data-stu-id="ed358-168">OAuth 2 Client Properties file</span></span></td>
    <td><span data-ttu-id="ed358-169">Accédez à l’emplacement du <em>fichier wdatp-connector.properties.</em></span><span class="sxs-lookup"><span data-stu-id="ed358-169">Browse to the location of the <em>wdatp-connector.properties</em> file.</span></span> <span data-ttu-id="ed358-170">Le nom doit correspondre au fichier fourni dans la .zip que vous avez téléchargée.</span><span class="sxs-lookup"><span data-stu-id="ed358-170">The name must match the file provided in the .zip that you downloaded.</span></span></td>
    <tr>
    <td><span data-ttu-id="ed358-171">Jeton d’actualisation</span><span class="sxs-lookup"><span data-stu-id="ed358-171">Refresh Token</span></span></td>
    <td><span data-ttu-id="ed358-172">Vous pouvez obtenir un jeton d’actualisation de deux manières : en générant un jeton d’actualisation à partir de la page des <b>paramètres SIEM</b> ou en utilisant l’outil restutil.</span><span class="sxs-lookup"><span data-stu-id="ed358-172">You can obtain a refresh token in two ways: by generating a refresh token from the <b>SIEM settings</b> page or using the restutil tool.</span></span> <br><br> <span data-ttu-id="ed358-173">Pour plus d’informations sur la génération d’un jeton d’actualisation à partir de la configuration <b>préférences,</b> voir Activer l’intégration <a href="enable-siem-integration.md" data-raw-source="[Enable SIEM integration in Defender for Endpoint](enable-siem-integration.md)">SIEM dans Defender for Endpoint</a>.</span><span class="sxs-lookup"><span data-stu-id="ed358-173">For more information on generating a refresh token from the <b>Preferences setup</b> , see <a href="enable-siem-integration.md" data-raw-source="[Enable SIEM integration in Defender for Endpoint](enable-siem-integration.md)">Enable SIEM integration in Defender for Endpoint</a>.</span></span> </br> </br><span data-ttu-id="ed358-174"><b>Obtenez votre jeton d’actualisation à l’aide de l’outil restutil :</b> </span><span class="sxs-lookup"><span data-stu-id="ed358-174"><b>Get your refresh token using the restutil tool:</b> </span></span></br> <span data-ttu-id="ed358-175">a.</span><span class="sxs-lookup"><span data-stu-id="ed358-175">a.</span></span> <span data-ttu-id="ed358-176">Ouvrez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="ed358-176">Open a command prompt.</span></span> <span data-ttu-id="ed358-177">Accédez à C:\<em>folder_location</em>\current\bin <em>où folder_location</em> représente l’emplacement où vous avez installé l’outil.</span><span class="sxs-lookup"><span data-stu-id="ed358-177">Navigate to C:\<em>folder_location</em>\current\bin where <em>folder_location</em> represents the location where you installed the tool.</span></span> </br></br> <span data-ttu-id="ed358-178">b.</span><span class="sxs-lookup"><span data-stu-id="ed358-178">b.</span></span> <span data-ttu-id="ed358-179">Type : <code>arcsight restutil token -config</code> à partir du répertoire bin. Par exemple : <b>arcsight restutil boxtoken -proxy proxy.location.hp.com:8080</b> fenêtre de navigateur Web s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ed358-179">Type: <code>arcsight restutil token -config</code> from the bin directory.For example: <b>arcsight restutil boxtoken -proxy proxy.location.hp.com:8080</b> A Web browser window will open.</span></span> </br> </br><span data-ttu-id="ed358-180">c.</span><span class="sxs-lookup"><span data-stu-id="ed358-180">c.</span></span> <span data-ttu-id="ed358-181">Tapez vos informations d’identification, puis cliquez sur le champ mot de passe pour que la page soit redirigée.</span><span class="sxs-lookup"><span data-stu-id="ed358-181">Type in your credentials then click on the password field to let the page redirect.</span></span> <span data-ttu-id="ed358-182">Dans l’invite de connexion, entrez vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="ed358-182">In the login prompt, enter your credentials.</span></span> </br> </br><span data-ttu-id="ed358-183">d.</span><span class="sxs-lookup"><span data-stu-id="ed358-183">d.</span></span> <span data-ttu-id="ed358-184">Un jeton d’actualisation est affiché dans l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="ed358-184">A refresh token is shown in the command prompt.</span></span> </br></br> <span data-ttu-id="ed358-185">e.</span><span class="sxs-lookup"><span data-stu-id="ed358-185">e.</span></span> <span data-ttu-id="ed358-186">Copiez-le et collez-le dans <b>le champ Jeton d’actualisation.</b></span><span class="sxs-lookup"><span data-stu-id="ed358-186">Copy and paste it into the <b>Refresh Token</b> field.</span></span>
    </td>
    </tr>
    </tr>
    </table><br/>
    
7. <span data-ttu-id="ed358-187">Une fenêtre de navigateur est ouverte par le connecteur.</span><span class="sxs-lookup"><span data-stu-id="ed358-187">A browser window is opened by the connector.</span></span> <span data-ttu-id="ed358-188">Connectez-vous avec vos informations d’identification d’application.</span><span class="sxs-lookup"><span data-stu-id="ed358-188">Login with your application credentials.</span></span> <span data-ttu-id="ed358-189">Une fois que vous vous êtes connecter, vous êtes invité à accorder l’autorisation à votre client OAuth2.</span><span class="sxs-lookup"><span data-stu-id="ed358-189">After you log in, you'll be asked to give permission to your OAuth2 Client.</span></span> <span data-ttu-id="ed358-190">Vous devez accorder des autorisations à votre client OAuth 2 pour que la configuration du connecteur puisse s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="ed358-190">You must give permission to your OAuth 2 Client so that the connector configuration can authenticate.</span></span>

   <span data-ttu-id="ed358-191"><code>redirect_uri</code>S’il s’agit d’une URL https, vous serez redirigé vers une URL sur l’hôte local.</span><span class="sxs-lookup"><span data-stu-id="ed358-191">If the <code>redirect_uri</code> is a https URL, you'll be redirected to a URL on the local host.</span></span> <span data-ttu-id="ed358-192">Vous verrez une page qui vous demande d’faire confiance au certificat fourni par le connecteur en cours d’exécution sur l’hôte local.</span><span class="sxs-lookup"><span data-stu-id="ed358-192">You'll see a page that requests for you to trust the certificate supplied by the connector running on the local host.</span></span> <span data-ttu-id="ed358-193">Vous devez faire confiance à ce certificat si l’redirect_uri est un https.</span><span class="sxs-lookup"><span data-stu-id="ed358-193">You'll need to trust this certificate if the redirect_uri is a https.</span></span>
   
   <span data-ttu-id="ed358-194">Toutefois, si vous spécifiez une URL http pour redirect_uri, vous n’avez pas besoin de donner votre consentement pour l’approbation du certificat.</span><span class="sxs-lookup"><span data-stu-id="ed358-194">If however you specify a http URL for the redirect_uri, you do not need to provide consent in trusting the certificate.</span></span>

8. <span data-ttu-id="ed358-195">Poursuivez l’installation du connecteur en revenant à la fenêtre d’installation du connecteur Micro Focus ArcSight.</span><span class="sxs-lookup"><span data-stu-id="ed358-195">Continue with the connector setup by returning to the Micro Focus ArcSight Connector Setup window.</span></span>

9. <span data-ttu-id="ed358-196">Sélectionnez **le Gestionnaire ArcSight (chiffré)** comme destination, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-196">Select the **ArcSight Manager (encrypted)** as the destination and click **Next**.</span></span>

10. <span data-ttu-id="ed358-197">Tapez l’adresse IP/nom d’hôte de destination dans **le nom** d’hôte du gestionnaire et vos informations d’identification dans le formulaire de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ed358-197">Type in the destination IP/hostname in **Manager Hostname** and your credentials in the parameters form.</span></span> <span data-ttu-id="ed358-198">Toutes les autres valeurs du formulaire doivent être conservées avec les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed358-198">All other values in the form should be retained with the default values.</span></span> <span data-ttu-id="ed358-199">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-199">Click **Next**.</span></span>

11. <span data-ttu-id="ed358-200">Tapez un nom pour le connecteur dans le formulaire de détails du connecteur.</span><span class="sxs-lookup"><span data-stu-id="ed358-200">Type in a name for the connector in the connector details form.</span></span> <span data-ttu-id="ed358-201">Toutes les autres valeurs du formulaire sont facultatives et peuvent être laissées vides.</span><span class="sxs-lookup"><span data-stu-id="ed358-201">All other values in the form are optional and can be left blank.</span></span> <span data-ttu-id="ed358-202">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-202">Click **Next**.</span></span>

12. <span data-ttu-id="ed358-203">La fenêtre d’importation du certificat esM Manager s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ed358-203">The ESM Manager import certificate window is shown.</span></span> <span data-ttu-id="ed358-204">Sélectionnez **Importer le certificat vers le connecteur à partir de la destination,** puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ed358-204">Select **Import the certificate to connector from destination** and click **Next**.</span></span> <span data-ttu-id="ed358-205">La **fenêtre Résumé du connecteur** d’ajout s’affiche et le certificat est importé.</span><span class="sxs-lookup"><span data-stu-id="ed358-205">The **Add connector Summary** window is displayed and the certificate is imported.</span></span>

13. <span data-ttu-id="ed358-206">Vérifiez que les détails dans la fenêtre Résumé du **connecteur** d’ajout sont corrects, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-206">Verify that the details in the **Add connector Summary** window is correct, then click **Next**.</span></span>

14. <span data-ttu-id="ed358-207">Sélectionnez **Installer en tant que service,** puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ed358-207">Select **Install as a service** and click **Next**.</span></span>

15. <span data-ttu-id="ed358-208">Tapez un nom dans le **champ Nom interne du** service.</span><span class="sxs-lookup"><span data-stu-id="ed358-208">Type a name in the **Service Internal Name** field.</span></span> <span data-ttu-id="ed358-209">Toutes les autres valeurs du formulaire peuvent être conservées avec les valeurs par défaut ou laissées vides.</span><span class="sxs-lookup"><span data-stu-id="ed358-209">All other values in the form can be retained with the default values or left blank .</span></span> <span data-ttu-id="ed358-210">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-210">Click **Next**.</span></span>

16. <span data-ttu-id="ed358-211">Tapez les paramètres du service, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ed358-211">Type in the service parameters and click **Next**.</span></span> <span data-ttu-id="ed358-212">Une fenêtre avec le **résumé du service d’installation** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ed358-212">A window with the **Install Service Summary** is shown.</span></span> <span data-ttu-id="ed358-213">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-213">Click **Next**.</span></span>

17. <span data-ttu-id="ed358-214">Terminez l’installation en **sélectionnant Exit** et **Next**.</span><span class="sxs-lookup"><span data-stu-id="ed358-214">Finish the installation by selecting **Exit** and **Next**.</span></span>

## <a name="install-and-configure-the-micro-focus-arcsight-console"></a><span data-ttu-id="ed358-215">Installer et configurer la console Micro Focus ArcSight</span><span class="sxs-lookup"><span data-stu-id="ed358-215">Install and configure the Micro Focus ArcSight console</span></span>

1. <span data-ttu-id="ed358-216">Suivez l’Assistant Installation à travers les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed358-216">Follow the installation wizard through the following tasks:</span></span>
   - <span data-ttu-id="ed358-217">Introduction</span><span class="sxs-lookup"><span data-stu-id="ed358-217">Introduction</span></span>
   - <span data-ttu-id="ed358-218">Contrat de licence</span><span class="sxs-lookup"><span data-stu-id="ed358-218">License Agreement</span></span>
   - <span data-ttu-id="ed358-219">Avis spécial</span><span class="sxs-lookup"><span data-stu-id="ed358-219">Special Notice</span></span>
   - <span data-ttu-id="ed358-220">Choisir le répertoire d’installation ArcSight</span><span class="sxs-lookup"><span data-stu-id="ed358-220">Choose ArcSight installation directory</span></span>
   - <span data-ttu-id="ed358-221">Choose Shortcut Folder</span><span class="sxs-lookup"><span data-stu-id="ed358-221">Choose Shortcut Folder</span></span>
   - <span data-ttu-id="ed358-222">Résumé de la pré-installation</span><span class="sxs-lookup"><span data-stu-id="ed358-222">Pre-Installation Summary</span></span>

2. <span data-ttu-id="ed358-223">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="ed358-223">Click **Install**.</span></span> <span data-ttu-id="ed358-224">Une fois l’installation terminée, l’Assistant Configuration de la console ArcSight s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ed358-224">After the installation completes, the ArcSight Console Configuration Wizard opens.</span></span>

3. <span data-ttu-id="ed358-225">Tapez localhost dans **le nom d’hôte** du gestionnaire et 8443 dans **le port du gestionnaire,** puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed358-225">Type localhost in **Manager Host Name** and 8443 in **Manager Port** then click **Next**.</span></span>

4. <span data-ttu-id="ed358-226">Sélectionnez **Utiliser la connexion directe,** puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ed358-226">Select **Use direct connection**, then click **Next**.</span></span>

5. <span data-ttu-id="ed358-227">Sélectionnez **Authentification par mot de** passe, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ed358-227">Select **Password Based Authentication**, then click **Next**.</span></span>

6. <span data-ttu-id="ed358-228">Sélectionnez **Il s’agit d’une installation utilisateur unique. (Recommandé),** puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ed358-228">Select **This is a single user installation. (Recommended)**, then click **Next**.</span></span>

7. <span data-ttu-id="ed358-229">Cliquez **sur Terminé** pour quitter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ed358-229">Click **Done** to quit the installer.</span></span>

8. <span data-ttu-id="ed358-230">Connectez-vous à la console Micro Focus ArcSight.</span><span class="sxs-lookup"><span data-stu-id="ed358-230">Login to the Micro Focus ArcSight console.</span></span>

9. <span data-ttu-id="ed358-231">Accédez à **l’ensemble de canaux actifs**  >  **Nouveau produit**  >  **d’appareil**  >  **condition.**</span><span class="sxs-lookup"><span data-stu-id="ed358-231">Navigate to **Active channel set** > **New Condition** > **Device** > **Device Product**.</span></span>

10. <span data-ttu-id="ed358-232">Définir **le produit de l’appareil = Microsoft Defender ATP**.</span><span class="sxs-lookup"><span data-stu-id="ed358-232">Set **Device Product = Microsoft Defender ATP**.</span></span> <span data-ttu-id="ed358-233">Une fois que vous avez vérifié que les événements sont en cours de flux vers l’outil, arrêtez à nouveau le processus et Windows Services et démarrez le REST ArcSight FlexConnector.</span><span class="sxs-lookup"><span data-stu-id="ed358-233">When you've verified that events are flowing to the tool, stop the process again and go to Windows Services and start the ArcSight FlexConnector REST.</span></span>

<span data-ttu-id="ed358-234">Vous pouvez désormais exécuter des requêtes dans la console Micro Focus ArcSight.</span><span class="sxs-lookup"><span data-stu-id="ed358-234">You can now run queries in the Micro Focus ArcSight console.</span></span>

<span data-ttu-id="ed358-235">Les détections defender pour les points de terminaison apparaissent en tant qu’événements discrets, avec « Microsoft » comme fournisseur et « Windows Defender ATP » comme nom d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ed358-235">Defender for Endpoint detections will appear as discrete events, with "Microsoft” as the vendor and “Windows Defender ATP” as the device name.</span></span>


## <a name="troubleshooting-micro-focus-arcsight-connection"></a><span data-ttu-id="ed358-236">Résolution des problèmes de connexion Micro Focus ArcSight</span><span class="sxs-lookup"><span data-stu-id="ed358-236">Troubleshooting Micro Focus ArcSight connection</span></span>

<span data-ttu-id="ed358-237">**Problème :** Échec de l’actualisation du jeton.</span><span class="sxs-lookup"><span data-stu-id="ed358-237">**Problem:** Failed to refresh the token.</span></span> <span data-ttu-id="ed358-238">Vous pouvez trouver le journal situé dans C: \\ *folder_location*  \current\logs où folder_location représente l’emplacement où vous avez installé l’outil.</span><span class="sxs-lookup"><span data-stu-id="ed358-238">You can find the log located in C:\\*folder_location*\current\logs where *folder_location* represents the location where you installed the tool.</span></span> <span data-ttu-id="ed358-239">Ouvrez _agent.log_ et recherchez `ERROR/FATAL/WARN` .</span><span class="sxs-lookup"><span data-stu-id="ed358-239">Open _agent.log_ and look for `ERROR/FATAL/WARN`.</span></span>

<span data-ttu-id="ed358-240">**Symptôme :** Vous obtenez le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="ed358-240">**Symptom:** You get the following error message:</span></span>

`Failed to refresh the token. Set reauthenticate to true: com.arcsight.common.al.e: Failed to refresh access token: status=HTTP/1.1 400 Bad Request FATAL EXCEPTION: Could not refresh the access token`

<span data-ttu-id="ed358-241">**Solution :**</span><span class="sxs-lookup"><span data-stu-id="ed358-241">**Solution:**</span></span>

1. <span data-ttu-id="ed358-242">Arrêtez le processus en cliquant sur Ctrl + C dans la fenêtre Connecteur.</span><span class="sxs-lookup"><span data-stu-id="ed358-242">Stop the process by clicking Ctrl + C on the Connector window.</span></span> <span data-ttu-id="ed358-243">Cliquez **sur Y** lorsque vous avez demandé « Terminer le travail par lots Y/N ? ».</span><span class="sxs-lookup"><span data-stu-id="ed358-243">Click **Y** when asked "Terminate batch job Y/N?".</span></span>

2. <span data-ttu-id="ed358-244">Accédez au dossier dans lequel vous avez stocké le fichier WDATP-connector.properties et modifiez-le pour ajouter la valeur suivante `reauthenticate=true` :</span><span class="sxs-lookup"><span data-stu-id="ed358-244">Navigate to the folder where you stored the WDATP-connector.properties file and edit it to add the following value: `reauthenticate=true`.</span></span>

3. <span data-ttu-id="ed358-245">Redémarrez le connecteur en exécutant la commande suivante : `arcsight.bat connectors` .</span><span class="sxs-lookup"><span data-stu-id="ed358-245">Restart the connector by running the following command: `arcsight.bat connectors`.</span></span>

   <span data-ttu-id="ed358-246">Une fenêtre de navigateur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ed358-246">A browser window appears.</span></span> <span data-ttu-id="ed358-247">Autorisez-le à s’exécuter, il doit disparaître et le connecteur doit maintenant être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ed358-247">Allow it to run, it should disappear, and the connector should now be running.</span></span>

> [!NOTE]
> <span data-ttu-id="ed358-248">Vérifiez que le connecteur est en cours d’exécution en arrêtant à nouveau le processus.</span><span class="sxs-lookup"><span data-stu-id="ed358-248">Verify that the connector is running by stopping the process again.</span></span> <span data-ttu-id="ed358-249">Ensuite, démarrez à nouveau le connecteur et aucune fenêtre de navigateur ne doit s’apparaître.</span><span class="sxs-lookup"><span data-stu-id="ed358-249">Then start the connector again, and no browser window should appear.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed358-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed358-250">Related topics</span></span>
- [<span data-ttu-id="ed358-251">Activer l’intégration SIEM dans Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="ed358-251">Enable SIEM integration in Defender for Endpoint</span></span>](enable-siem-integration.md)
- [<span data-ttu-id="ed358-252">Tirer les détections vers vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="ed358-252">Pull detections to your SIEM tools</span></span>](/windows/security/threat-protection/microsoft-defender-atp/configure-siem)
- [<span data-ttu-id="ed358-253">Détections pull Defender pour les points de terminaison à l’aide de l’API REST</span><span class="sxs-lookup"><span data-stu-id="ed358-253">Pull Defender for Endpoint detections using REST API</span></span>](pull-alerts-using-rest-api.md)
- [<span data-ttu-id="ed358-254">Résoudre des problèmes d’intégration de l’outil SIEM</span><span class="sxs-lookup"><span data-stu-id="ed358-254">Troubleshoot SIEM tool integration issues</span></span>](troubleshoot-siem.md)
