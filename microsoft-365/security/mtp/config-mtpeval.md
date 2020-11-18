---
title: Configurer les piliers de Microsoft 365 Defender pour le laboratoire d’évaluation ou l’environnement pilote
description: Configurez les piliers de Microsoft 365 Defender, tels que Microsoft Defender pour Office 365, Microsoft Defender pour l’identité, la sécurité de l’application Cloud Microsoft et Microsoft Defender pour le point de terminaison, pour votre laboratoire d’évaluation ou votre environnement pilote.
keywords: configurer la version d’évaluation de la protection de Microsoft Threat, configuration de la version d’évaluation de Microsoft Threat Protection, configurer le projet pilote Microsoft Threat Protection, configurer la protection Microsoft contre les menaces, pilier de la protection Microsoft contre les menaces
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dolmont
author: DulceMontemayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-scenario
- m365solution-evalutatemtp
ms.topic: article
ms.openlocfilehash: 240ffd7ec8d46da33c43ec2f9cb50cf59c89f11b
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49131296"
---
# <a name="configure-microsoft-365-defender-pillars-for-your-trial-lab-or-pilot-environment"></a><span data-ttu-id="004c6-104">Configurer les piliers de Microsoft 365 Defender pour votre laboratoire d’évaluation ou votre environnement pilote</span><span class="sxs-lookup"><span data-stu-id="004c6-104">Configure Microsoft 365 Defender pillars for your trial lab or pilot environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="004c6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="004c6-105">**Applies to:**</span></span>
- <span data-ttu-id="004c6-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="004c6-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="004c6-107">La création d’un laboratoire de test Microsoft 365 Defender ou d’un environnement pilote et son déploiement est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="004c6-107">Creating a Microsoft 365 Defender trial lab or pilot environment and deploying it is a three-phase process:</span></span>

|<span data-ttu-id="004c6-108">[![Phase 1 : préparer](../../media/phase-diagrams/prepare.png)](prepare-mtpeval.md)</span><span class="sxs-lookup"><span data-stu-id="004c6-108">[![Phase 1: Prepare](../../media/phase-diagrams/prepare.png)](prepare-mtpeval.md)</span></span><br/>[<span data-ttu-id="004c6-109">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="004c6-109">Phase 1: Prepare</span></span>](prepare-mtpeval.md) |<span data-ttu-id="004c6-110">[![Phase 2 : configurer](../../media/phase-diagrams/setup.png)](setup-mtpeval.md)</span><span class="sxs-lookup"><span data-stu-id="004c6-110">[![Phase 2: Set up](../../media/phase-diagrams/setup.png)](setup-mtpeval.md)</span></span><br/>[<span data-ttu-id="004c6-111">Phase 2 : configurer</span><span class="sxs-lookup"><span data-stu-id="004c6-111">Phase 2: Set up</span></span>](setup-mtpeval.md) |![Phase 3 : intégration](../../media/phase-diagrams/onboard.png)<br/><span data-ttu-id="004c6-113">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="004c6-113">Phase 3: Onboard</span></span> | <span data-ttu-id="004c6-114">[![Retour au pilote](../../media/phase-diagrams/backtopilot.png)](mtp-pilot.md)</span><span class="sxs-lookup"><span data-stu-id="004c6-114">[![Back to pilot](../../media/phase-diagrams/backtopilot.png)](mtp-pilot.md)</span></span><br/>[<span data-ttu-id="004c6-115">Retour au manuel pilote</span><span class="sxs-lookup"><span data-stu-id="004c6-115">Back to pilot playbook</span></span>](mtp-pilot.md) |
|--|--|--|--|
|| |<span data-ttu-id="004c6-116">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="004c6-116">*You are here!*</span></span> | |

<span data-ttu-id="004c6-117">Vous êtes actuellement en phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="004c6-117">You're currently in the configuration phase.</span></span>

<span data-ttu-id="004c6-118">La préparation est essentielle à tout déploiement réussi.</span><span class="sxs-lookup"><span data-stu-id="004c6-118">Preparation is key to any successful deployment.</span></span> <span data-ttu-id="004c6-119">Dans cet article, vous serez guidé sur les points que vous devrez prendre en compte lors de la préparation du déploiement de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="004c6-119">In this article, you'll be guided on the points you'll need to consider as you prepare to deploy Microsoft Defender for Endpoint.</span></span>


## <a name="microsoft-365-defender-pillars"></a><span data-ttu-id="004c6-120">Piliers de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="004c6-120">Microsoft 365 Defender pillars</span></span>
<span data-ttu-id="004c6-121">Microsoft 365 Defender se compose de quatre piliers.</span><span class="sxs-lookup"><span data-stu-id="004c6-121">Microsoft 365 Defender consists of four pillars.</span></span> <span data-ttu-id="004c6-122">Bien qu’un seul pilier puisse déjà fournir de la valeur à la sécurité de votre organisation réseau, l’activation des quatre piliers de Microsoft 365 Defender donnera à votre organisation la plus grande valeur.</span><span class="sxs-lookup"><span data-stu-id="004c6-122">Although one pillar can already provide value to your network organization's security, enabling the four Microsoft 365 Defender pillars will give your organization the most value.</span></span>

![Image of_Microsoft 365 Defender solution for Users, Microsoft Defender for Identity, for Endpoints Microsoft Defender for Endpoint, for Cloud Apps, Microsoft Cloud App Security, and for Data, Microsoft Defender for Office 365](../../media/mtp/m365pillars.png)

<span data-ttu-id="004c6-124">Cette section vous guidera dans la configuration des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="004c6-124">This section will guide you to configure:</span></span>
-   <span data-ttu-id="004c6-125">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="004c6-125">Microsoft Defender for Office 365</span></span>
-   <span data-ttu-id="004c6-126">Microsoft Defender pour identité</span><span class="sxs-lookup"><span data-stu-id="004c6-126">Microsoft Defender for Identity</span></span> 
-   <span data-ttu-id="004c6-127">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="004c6-127">Microsoft Cloud App Security</span></span>
-   <span data-ttu-id="004c6-128">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="004c6-128">Microsoft Defender for Endpoint</span></span>


## <a name="configure-microsoft-defender-for-office-365"></a><span data-ttu-id="004c6-129">Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="004c6-129">Configure Microsoft Defender for Office 365</span></span>

>[!NOTE]
><span data-ttu-id="004c6-130">Ignorez cette étape si vous avez déjà activé l’option Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="004c6-130">Skip this step if you've already enabled Defender for Office 365.</span></span> 

<span data-ttu-id="004c6-131">Il existe un module PowerShell appelé *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* qui permet de déterminer certains de ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="004c6-131">There's a PowerShell Module called the *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* that helps determine some of these settings.</span></span> <span data-ttu-id="004c6-132">Lorsqu’il est exécuté en tant qu’administrateur dans votre client, Get-ORCAReport permet de générer une évaluation du blocage du courrier indésirable, des hameçons et d’autres paramètres d’hygiène des messages.</span><span class="sxs-lookup"><span data-stu-id="004c6-132">When run as an administrator in your tenant, get-ORCAReport will help generate an assessment of the anti-spam, anti-phish, and other message hygiene settings.</span></span> <span data-ttu-id="004c6-133">Vous pouvez télécharger ce module à partir de https://www.powershellgallery.com/packages/ORCA/ .</span><span class="sxs-lookup"><span data-stu-id="004c6-133">You can download this module from https://www.powershellgallery.com/packages/ORCA/.</span></span> 

1. <span data-ttu-id="004c6-134">Accédez à la stratégie de gestion des menaces du [Centre de sécurité & conformité Office 365](https://protection.office.com/homepage)  >  **Threat management**  >  **Policy**.</span><span class="sxs-lookup"><span data-stu-id="004c6-134">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Policy**.</span></span>

   ![Image of_Office 365 sécurité & Centre de conformité gestion des menaces-page de stratégie](../../media/mtp-eval-32.png)
 
2. <span data-ttu-id="004c6-136">Cliquez sur **anti-hameçonnage**, sélectionnez **créer** et renseignez le nom et la description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="004c6-136">Click **Anti-phishing**, select **Create** and fill in the policy name and description.</span></span> <span data-ttu-id="004c6-137">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c6-137">Click **Next**.</span></span>

   ![Page de la stratégie anti-hameçonnage du centre de sécurité & de l’image of_Office 365, dans laquelle vous pouvez nommer votre stratégie](../../media/mtp-eval-33.png)

   > [!NOTE]
   > <span data-ttu-id="004c6-139">Modifiez votre stratégie anti-hameçonnage avancée dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="004c6-139">Edit your Advanced anti-phishing policy in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="004c6-140">Remplacez le **seuil d’hameçonnage avancé** par **2**.</span><span class="sxs-lookup"><span data-stu-id="004c6-140">Change **Advanced Phishing Threshold** to **2 - Aggressive**.</span></span>

3. <span data-ttu-id="004c6-141">Cliquez sur le menu déroulant **Ajouter une condition** , puis sélectionnez vos domaines en tant que domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="004c6-141">Click the **Add a condition** drop-down menu and select your domain(s) as recipient domain.</span></span> <span data-ttu-id="004c6-142">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c6-142">Click **Next**.</span></span>

   ![Page de la stratégie anti-hameçonnage du centre de sécurité & de l’image of_Office 365, dans laquelle vous pouvez ajouter une condition pour son application](../../media/mtp-eval-34.png)
 
4. <span data-ttu-id="004c6-144">Vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="004c6-144">Review your settings.</span></span> <span data-ttu-id="004c6-145">Cliquez sur **créer cette stratégie** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="004c6-145">Click **Create this policy** to confirm.</span></span> 

   ![Image of_Office 365 sécurité & de la page de stratégie anti-hameçonnage du centre de conformité, dans laquelle vous pouvez vérifier vos paramètres et cliquer sur le bouton créer cette stratégie](../../media/mtp-eval-35.png)
 
5. <span data-ttu-id="004c6-147">Sélectionnez **pièces jointes fiables** et sélectionnez l’option Activer la protection avancée contre les menaces **pour SharePoint, OneDrive et Microsoft teams** .</span><span class="sxs-lookup"><span data-stu-id="004c6-147">Select **Safe Attachments** and select the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** option.</span></span>

   ![Image of_Office 365 page Centre de sécurité & conformité, dans laquelle vous pouvez activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams](../../media/mtp-eval-36.png)

6. <span data-ttu-id="004c6-149">Cliquez sur l’icône + pour créer une stratégie de pièces jointes fiables, appliquez-la en tant que domaine de destinataire à vos domaines.</span><span class="sxs-lookup"><span data-stu-id="004c6-149">Click the + icon to create a new safe attachment policy, apply it as recipient domain to your domains.</span></span> <span data-ttu-id="004c6-150">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-150">Click **Save**.</span></span>

   ![Image of_Office 365 page du centre de sécurité & conformité où vous pouvez créer une nouvelle stratégie de pièces jointes fiables](../../media/mtp-eval-37.png)
 
7. <span data-ttu-id="004c6-152">Ensuite, sélectionnez la stratégie de **liens approuvés** , puis cliquez sur l’icône représentant un crayon pour modifier la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="004c6-152">Next, select the **Safe Links** policy, then click the pencil icon to edit the default policy.</span></span>

8. <span data-ttu-id="004c6-153">Assurez-vous que l’option **ne pas suivre lorsque les utilisateurs cliquent sur les liens approuvés** n’est pas sélectionnée, tandis que les autres options sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="004c6-153">Make sure that the **Do not track when users click safe links** option is not selected, while the rest of the options are selected.</span></span> <span data-ttu-id="004c6-154">Pour plus d’informations, voir [paramètres de liens fiables](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp) .</span><span class="sxs-lookup"><span data-stu-id="004c6-154">See [Safe Links settings](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp) for details.</span></span> <span data-ttu-id="004c6-155">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-155">Click **Save**.</span></span> 

   ![Image of_Office 365 page du centre de sécurité & conformité qui indique que l’option ne suit pas lorsque les utilisateurs cliquent sur Safe n’est pas sélectionné](../../media/mtp-eval-38.png)

9. <span data-ttu-id="004c6-157">Sélectionnez ensuite la stratégie **anti-programme malveillant** , sélectionnez la valeur par défaut, puis cliquez sur l’icône représentant un crayon.</span><span class="sxs-lookup"><span data-stu-id="004c6-157">Next select the **Anti-malware** policy, select the default, and choose the pencil icon.</span></span>

10. <span data-ttu-id="004c6-158">Cliquez sur **paramètres** , puis sélectionnez **Oui et utilisez le texte de notification par défaut** pour activer la **réponse de détection de programmes malveillants**.</span><span class="sxs-lookup"><span data-stu-id="004c6-158">Click **Settings** and select **Yes and use the default notification text** to enable **Malware Detection Response**.</span></span> <span data-ttu-id="004c6-159">Activez le **filtre types de pièces jointes courantes** .</span><span class="sxs-lookup"><span data-stu-id="004c6-159">Turn the **Common Attachment Types Filter** on.</span></span> <span data-ttu-id="004c6-160">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-160">Click **Save**.</span></span>

    ![Image of_Office 365 page du centre de sécurité & conformité qui indique que la réponse de détection de programmes malveillants est activée avec notification par défaut et que le filtre de types de pièces jointes courantes est activé](../../media/mtp-eval-39.png)
  
11. <span data-ttu-id="004c6-162">Accédez à [Office 365 Security & Compliance Center](https://protection.office.com/homepage)  >  **Search**  >  **audit log Search** and Turn Auditing on.</span><span class="sxs-lookup"><span data-stu-id="004c6-162">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Search** > **Audit log search** and turn Auditing on.</span></span>

    ![Image of_Office 365 de la page Centre de sécurité & conformité, dans laquelle vous pouvez activer la recherche du journal d’audit](../../media/mtp-eval-40.png)

12. <span data-ttu-id="004c6-164">Intégrez Microsoft Defender pour Office 365 à Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="004c6-164">Integrate Microsoft Defender for Office 365 with Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="004c6-165">Accédez à [Office 365 Security & Compliance Center](https://protection.office.com/homepage)  >  **Threat management**  >  **Explorer Management Explorer** et sélectionnez **Microsoft Defender for Endpoint Settings** dans le coin supérieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="004c6-165">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Explorer** and select **Microsoft Defender for Endpoint Settings** on the upper right corner of the screen.</span></span> <span data-ttu-id="004c6-166">Dans la boîte de dialogue Defender pour la connexion au point de terminaison, activez **connexion à Microsoft Defender pour le point de terminaison**.</span><span class="sxs-lookup"><span data-stu-id="004c6-166">In the Defender for Endpoint connection dialog box, turn on **Connect to Microsoft Defender for Endpoint**.</span></span>

    ![Image of_Office 365 de la page Centre de sécurité & conformité, dans laquelle vous pouvez activer la connexion à Microsoft Defender pour le point de terminaison](../../media/mtp-eval-41.png)

## <a name="configure-microsoft-defender-for-identity"></a><span data-ttu-id="004c6-168">Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="004c6-168">Configure Microsoft Defender for Identity</span></span>

>[!NOTE]
><span data-ttu-id="004c6-169">Ignorez cette étape si vous avez déjà activé Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="004c6-169">Skip this step if you've already enabled Microsoft Defender for Identity</span></span>

1. <span data-ttu-id="004c6-170">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info) > sélectionnez **plus**  >  **de ressources Microsoft Defender pour l’identité**.</span><span class="sxs-lookup"><span data-stu-id="004c6-170">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > select **More Resources** > **Microsoft Defender for Identity**.</span></span>

   ![Page du centre de sécurité image of_Microsoft 365 où il existe une option pour ouvrir Microsoft Defender pour l’identité](../../media/mtp-eval-42.png)

2. <span data-ttu-id="004c6-172">Cliquez sur **créer** pour démarrer l’Assistant Microsoft Defender pour les identités.</span><span class="sxs-lookup"><span data-stu-id="004c6-172">Click **Create** to start the Microsoft Defender for Identity wizard.</span></span> 

   ![Image of_Microsoft Defender for Identity Wizard, dans laquelle vous devez cliquer sur le bouton créer](../../media/mtp-eval-43.png)

3. <span data-ttu-id="004c6-174">Choisissez **fournir un nom d’utilisateur et un mot de passe pour vous connecter à votre forêt Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="004c6-174">Choose **Provide a username and password to connect to your Active Directory forest**.</span></span>  

   ![Image of_Microsoft Defender for Identity welcome page](../../media/mtp-eval-44.png)

4. <span data-ttu-id="004c6-176">Entrez vos informations d’identification locales Active Directory.</span><span class="sxs-lookup"><span data-stu-id="004c6-176">Enter your Active Directory on-premises credentials.</span></span> <span data-ttu-id="004c6-177">Il peut s’agir de n’importe quel compte d’utilisateur qui dispose d’un accès en lecture à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="004c6-177">This can be any user account that has read access to Active Directory.</span></span>

   ![Image of_Microsoft Defender for Identity Directory Services où vous devez placer vos informations d’identification](../../media/mtp-eval-45.png)

5. <span data-ttu-id="004c6-179">Ensuite, choisissez **Télécharger le programme d’installation du capteur** et transférer le fichier vers votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="004c6-179">Next, choose **Download Sensor Setup** and transfer file to your domain controller.</span></span>

   ![Image of_Microsoft Defender pour l’identité, dans laquelle vous pouvez sélectionner l’option Télécharger le capteur de téléchargement](../../media/mtp-eval-46.png)

6. <span data-ttu-id="004c6-181">Exécutez le programme d’installation de Microsoft Defender pour le capteur d’identité et commencez à suivre l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="004c6-181">Execute the Microsoft Defender for Identity Sensor Setup and begin following the wizard.</span></span>

   ![Image of_Microsoft Defender pour l’identité où vous devez cliquer sur suivant pour suivre l’Assistant Microsoft Defender pour le capteur d’identité](../../media/mtp-eval-47.png)
 
7. <span data-ttu-id="004c6-183">Cliquez sur **suivant** dans le type de déploiement du capteur.</span><span class="sxs-lookup"><span data-stu-id="004c6-183">Click **Next** at the sensor deployment type.</span></span>

   ![Image of_Microsoft Defender pour la page identité où vous devez cliquer sur suivant pour accéder à la page suivante](../../media/mtp-eval-48.png)
 
8. <span data-ttu-id="004c6-185">Copiez la clé d’accès, car vous devez l’entrer ensuite dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="004c6-185">Copy the access key because you need to enter it next in the Wizard.</span></span>

   ![Page capteurs d’image of_the où vous devez copier la clé d’accès que vous devez entrer dans la page suivante de l’Assistant de configuration du capteur d’identité de Microsoft Defender](../../media/mtp-eval-49.png)
 
9. <span data-ttu-id="004c6-187">Copiez la clé d’accès dans l’Assistant, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-187">Copy the access key into the Wizard and click **Install**.</span></span> 

   ![Image of_Microsoft Defender pour l’Assistant capteur d’identité où vous devez fournir la clé d’accès, puis cliquez sur le bouton installer.](../../media/mtp-eval-50.png)

10. <span data-ttu-id="004c6-189">Félicitations, vous avez réussi à configurer Microsoft Defender pour l’identité sur votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="004c6-189">Congratulations, you've successfully configured Microsoft Defender for Identity on your domain controller.</span></span>

    ![Image of_Microsoft la fin de l’installation de l’Assistant capteur d’identité où vous devez cliquer sur le bouton Terminer](../../media/mtp-eval-51.png)
 
11. <span data-ttu-id="004c6-191">Sous la section [Microsoft Defender pour les paramètres d’identité](https://go.microsoft.com/fwlink/?linkid=2040449) , sélectionnez \* \* Microsoft Defender pour le point de terminaison \* \*, puis activez le bouton bascule.</span><span class="sxs-lookup"><span data-stu-id="004c6-191">Under the [Microsoft Defender for Identity](https://go.microsoft.com/fwlink/?linkid=2040449) settings section, select \*\*Microsoft Defender for Endpoint \*\*, then turn on the toggle.</span></span> <span data-ttu-id="004c6-192">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-192">Click **Save**.</span></span> 

    ![Image of_the la page Microsoft Defender pour les paramètres d’identité où vous devez activer le basculement Microsoft Defender pour le point de terminaison activé](../../media/mtp-eval-52.png)

>[!NOTE]
><span data-ttu-id="004c6-194">Windows Defender ATP a été rebaptisé Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="004c6-194">Windows Defender ATP has been rebranded as Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="004c6-195">Les modifications apportées à la personnalisation de tous nos portails sont déployées pour la cohérence.</span><span class="sxs-lookup"><span data-stu-id="004c6-195">Rebranding changes across all of our portals are being rolled out the for consistency.</span></span>


## <a name="configure-microsoft-cloud-app-security"></a><span data-ttu-id="004c6-196">Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="004c6-196">Configure Microsoft Cloud App Security</span></span>

>[!NOTE]
><span data-ttu-id="004c6-197">Ignorez cette étape si vous avez déjà activé Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="004c6-197">Skip this step if you've already enabled Microsoft Cloud App Security.</span></span> 

1. <span data-ttu-id="004c6-198">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info)  >  **More Resources**  >  **Microsoft Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="004c6-198">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Cloud App Security**.</span></span>

   ![Page of_Microsoft 365 du centre de sécurité sur lequel vous pouvez voir la carte d’application Cloud de Microsoft et qui doit cliquer sur le bouton ouvrir](../../media/mtp-eval-53.png)

2. <span data-ttu-id="004c6-200">À l’invite informations pour intégrer Microsoft Defender pour identité, sélectionnez **activer l’intégration des données d’identité Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="004c6-200">At the information prompt to integrate Microsoft Defender for Identity, select **Enable Microsoft Defender for Identity data integration**.</span></span>
  
   ![Image of_the informations vous invitant à intégrer Microsoft Defender pour l’identité où vous devez sélectionner le lien activer Microsoft Defender pour l’intégration des données d’identité](../../media/mtp-eval-54.png)

   > [!NOTE]
   > <span data-ttu-id="004c6-202">Si vous ne voyez pas cette invite, cela signifie que votre service Microsoft Defender pour l’intégration des données d’identité a déjà été activé.</span><span class="sxs-lookup"><span data-stu-id="004c6-202">If you don’t see this prompt, it might mean that your Microsoft Defender for Identity data integration has already been enabled.</span></span> <span data-ttu-id="004c6-203">Toutefois, si vous n’êtes pas sûr, contactez votre administrateur informatique pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="004c6-203">However, if you are not sure, contact your IT Administrator to confirm.</span></span> 

3. <span data-ttu-id="004c6-204">Accédez à **paramètres**, activez le bouton **Microsoft Defender for Identity Integration** , puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-204">Go to **Settings**, turn on the **Microsoft Defender for Identity integration** toggle, then click **Save**.</span></span> 

   ![Image of_the page Paramètres où vous devez activer le bouton Microsoft Defender for Identity Integration, puis cliquez sur Enregistrer.](../../media/mtp-eval-55.png)
   
   > [!NOTE]
   > <span data-ttu-id="004c6-206">Pour les nouvelles instances de Microsoft Defender pour les identités, ce bouton d’intégration est activé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="004c6-206">For new Microsoft Defender for Identity instances, this integration toggle is automatically turned on.</span></span> <span data-ttu-id="004c6-207">Vérifiez que votre Microsoft Defender pour l’intégration des identités a été activé avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="004c6-207">Confirm that your Microsoft Defender for Identity integration has been enabled before you proceed to the next step.</span></span>
 
4. <span data-ttu-id="004c6-208">Sous paramètres de découverte du Cloud, sélectionnez **Microsoft Defender pour l’intégration de points de terminaison**, puis activez l’intégration.</span><span class="sxs-lookup"><span data-stu-id="004c6-208">Under the Cloud discovery settings, select **Microsoft Defender for Endpoint integration**, then enable the integration.</span></span> <span data-ttu-id="004c6-209">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="004c6-209">Click **Save**.</span></span>

   ![Image of_the la page Microsoft Defender pour les points de terminaison où la case à cocher bloquer les applications non sanctionnées sous Microsoft Defender pour l’intégration de points de terminaison est sélectionnée.](../../media/mtp-eval-56.png)

5. <span data-ttu-id="004c6-212">Sous paramètres de détection sur le Cloud, sélectionnez enrichissement par l' **utilisateur**, puis activez l’intégration à Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="004c6-212">Under Cloud discovery settings, select **User enrichment**, then enable the integration with Azure Active Directory.</span></span>

   ![Image de la section enrichissement par l’utilisateur dans laquelle la case à cocher enrichir les identificateurs utilisateur enrichis avec des noms d’utilisateur Azure Active Directory est activée](../../media/mtp-eval-57.png)


## <a name="configure-microsoft-defender-for-endpoint"></a><span data-ttu-id="004c6-214">Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="004c6-214">Configure Microsoft Defender for Endpoint</span></span>

>[!NOTE]
><span data-ttu-id="004c6-215">Ignorez cette étape si vous avez déjà activé Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-215">Skip this step if you've already enabled Microsoft Defender for Endpoint.</span></span>

1. <span data-ttu-id="004c6-216">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info)  >  **plus de ressources**  >  **Microsoft Defender Security Center**.</span><span class="sxs-lookup"><span data-stu-id="004c6-216">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Defender Security Center**.</span></span> <span data-ttu-id="004c6-217">Cliquez sur **Ouvrir**. </span><span class="sxs-lookup"><span data-stu-id="004c6-217">Click **Open**.</span></span>

   ![Option du centre de sécurité de l’image of_Microsoft Defender dans la page Centre de sécurité Microsoft 365](../../media/mtp-eval-58.png)
 
2. <span data-ttu-id="004c6-219">Suivez l’Assistant Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-219">Follow the Microsoft Defender for Endpoint wizard.</span></span> <span data-ttu-id="004c6-220">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c6-220">Click **Next**.</span></span> 

   ![Image of_the page d’accueil de l’Assistant Centre de sécurité Microsoft Defender](../../media/mtp-eval-59.png)

3. <span data-ttu-id="004c6-222">Choisissez en fonction de votre emplacement de stockage de données par défaut, de la stratégie de rétention des données, de la taille de l’organisation et du opt-in pour les fonctionnalités d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="004c6-222">Choose based on your preferred data storage location, data retention policy, organization size, and opt-in for preview features.</span></span>

   ![Image of_the page permettant de sélectionner votre pays de stockage des données, la stratégie de rétention et la taille de l’organisation.](../../media/mtp-eval-60.png)
   
   > [!NOTE]
   > <span data-ttu-id="004c6-225">Vous ne pouvez pas modifier par la suite certains paramètres, comme l’emplacement de stockage des données.</span><span class="sxs-lookup"><span data-stu-id="004c6-225">You cannot change some of the settings, like data storage location, afterwards.</span></span> 

   <span data-ttu-id="004c6-226">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c6-226">Click **Next**.</span></span> 

4. <span data-ttu-id="004c6-227">Cliquez sur **Continuer** pour configurer votre client Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-227">Click **Continue** and it will provision your Microsoft Defender for Endpoint tenant.</span></span>

   ![Image of_the page vous invitant à cliquer sur le bouton continuer pour créer votre instance Cloud](../../media/mtp-eval-61.png)

5. <span data-ttu-id="004c6-229">Intégrez vos points de terminaison via les stratégies de groupe, le gestionnaire de points de terminaison Microsoft ou en exécutant un script local vers Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-229">Onboard your endpoints through Group Policies, Microsoft Endpoint Manager or by running a local script to Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="004c6-230">Par souci de simplicité, ce guide utilise le script local.</span><span class="sxs-lookup"><span data-stu-id="004c6-230">For simplicity, this guide uses the local script.</span></span>

6. <span data-ttu-id="004c6-231">Cliquez sur **Télécharger le package** et copiez le script d’intégration à vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-231">Click **Download package** and copy the onboarding script to your endpoint(s).</span></span>

   ![Image of_page invite à cliquer sur le bouton Télécharger le package pour copier le script d’intégration à votre point de terminaison ou aux points de terminaison](../../media/mtp-eval-62.png)

7. <span data-ttu-id="004c6-233">Sur votre point de terminaison, exécutez le script d’intégration en tant qu’administrateur et choisissez Y.</span><span class="sxs-lookup"><span data-stu-id="004c6-233">On your endpoint, run the onboarding script as Administrator and choose Y.</span></span> 

   ![Image of_the CommandLine où vous exécutez le script d’intégration et choisissez Y pour continuer](../../media/mtp-eval-63.png)

8. <span data-ttu-id="004c6-235">Félicitations, vous avez intégré votre premier point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-235">Congratulations, you've onboarded your first endpoint.</span></span>

   ![Image of_the CommandLine où vous recevez la confirmation que vous avez intégrée votre premier point de terminaison.](../../media/mtp-eval-64.png)

9. <span data-ttu-id="004c6-238">Copiez-collez le test de détection à partir de l’Assistant Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-238">Copy-paste the detection test from the Microsoft Defender for Endpoint wizard.</span></span>

   ![Image of_the exécutez une étape de test de détection à partir de laquelle vous devez cliquer sur copier pour copier le script de test de détection que vous devez coller dans l’invite de commandes.](../../media/mtp-eval-65.png)

10. <span data-ttu-id="004c6-240">Copiez le script PowerShell vers une invite de commandes avec élévation de privilèges et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="004c6-240">Copy the PowerShell script to an elevated command prompt and run it.</span></span> 

    ![Image of_command invite où vous devez copier le script PowerShell vers une invite de commandes avec élévation de privilèges et l’exécuter](../../media/mtp-eval-66.png)

11. <span data-ttu-id="004c6-242">Sélectionnez **commencer à utiliser Microsoft Defender pour le point de terminaison** à partir de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="004c6-242">Select **Start using Microsoft Defender for Endpoint** from the Wizard.</span></span>

    ![Image of_the invite de confirmation à partir de l’Assistant où vous devez cliquer sur Démarrer à l’aide de Microsoft Defender for Endpoint](../../media/mtp-eval-67.png)
 
12. <span data-ttu-id="004c6-244">Visitez le [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/).</span><span class="sxs-lookup"><span data-stu-id="004c6-244">Visit the [Microsoft Defender Security Center](https://securitycenter.windows.com/).</span></span> <span data-ttu-id="004c6-245">Accédez à **paramètres** , puis sélectionnez **fonctionnalités avancées**.</span><span class="sxs-lookup"><span data-stu-id="004c6-245">Go to **Settings** and then select **Advanced features**.</span></span> 

    ![Menu des paramètres du centre de sécurité de l’image of_Microsoft Defender dans lequel vous devez sélectionner les fonctionnalités avancées](../../media/mtp-eval-68.png)

13. <span data-ttu-id="004c6-247">Activez l’intégration à **Microsoft Defender pour l’identité**.</span><span class="sxs-lookup"><span data-stu-id="004c6-247">Turn on the integration with **Microsoft Defender for Identity**.</span></span>  

    ![Les fonctionnalités avancées de l’option Centre de sécurité de l’image of_Microsoft Defender, Microsoft Defender for Identity, que vous devez activer](../../media/mtp-eval-69.png)

14. <span data-ttu-id="004c6-249">Activer l’intégration avec **Office 365 Threat Intelligence**.</span><span class="sxs-lookup"><span data-stu-id="004c6-249">Turn on the integration with **Office 365 Threat Intelligence**.</span></span>

    ![Image of_Microsoft Defender Security Center Advanced Features, Office 365 Threat Intelligence option permettez à activer](../../media/mtp-eval-70.png)

15. <span data-ttu-id="004c6-251">Activez l’intégration à la **sécurité des applications Cloud de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="004c6-251">Turn on integration with **Microsoft Cloud App Security**.</span></span>

    ![Image of_Microsoft Defender Security Center Advanced Features, option de sécurité de l’application Cloud Microsoft activer/désactiver](../../media/mtp-eval-71.png)

16. <span data-ttu-id="004c6-253">Faites défiler la liste vers le bas et cliquez sur **enregistrer les préférences** pour confirmer les nouvelles intégrations.</span><span class="sxs-lookup"><span data-stu-id="004c6-253">Scroll down and click **Save preferences** to confirm the new integrations.</span></span>

    ![Image of_Save bouton préférences que vous devez cliquer](../../media/mtp-eval-72.png)

## <a name="start-the-microsoft-365-defender-service"></a><span data-ttu-id="004c6-255">Démarrer le service Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="004c6-255">Start the Microsoft 365 Defender service</span></span>

>[!NOTE]
><span data-ttu-id="004c6-256">À partir du 1er juin 2020, Microsoft active automatiquement les fonctionnalités de Microsoft 365 Defender pour tous les clients éligibles.</span><span class="sxs-lookup"><span data-stu-id="004c6-256">Starting June 1, 2020, Microsoft automatically enables Microsoft 365 Defender features for all eligible tenants.</span></span> <span data-ttu-id="004c6-257">Pour plus d’informations, consultez cet [article de la communauté Microsoft Tech sur l’éligibilité des licences](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/microsoft-threat-protection-will-automatically-turn-on-for/ba-p/1345426) .</span><span class="sxs-lookup"><span data-stu-id="004c6-257">See this [Microsoft Tech Community article on license eligibility](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/microsoft-threat-protection-will-automatically-turn-on-for/ba-p/1345426) for details.</span></span> 


<span data-ttu-id="004c6-258">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/homepage).</span><span class="sxs-lookup"><span data-stu-id="004c6-258">Go to [Microsoft 365 Security Center](https://security.microsoft.com/homepage).</span></span> <span data-ttu-id="004c6-259">Accédez à **paramètres** , puis sélectionnez **Microsoft 365 Defender**.</span><span class="sxs-lookup"><span data-stu-id="004c6-259">Navigate to **Settings** and then select **Microsoft 365 Defender**.</span></span>

![<span data-ttu-id="004c6-260">Image of_Microsoft 365 Defender option capture d’écran de la page Paramètres du centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="004c6-260">Image of_Microsoft 365 Defender option screenshot from the Microsoft 365 Security Center Settings page</span></span> ](../../media/mtp-eval-72b.png) <br>

<span data-ttu-id="004c6-261">Pour obtenir des instructions plus détaillées, consultez la rubrique [activer Microsoft 365 Defender](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="004c6-261">For a more comprehensive guidance, see [Turn on Microsoft 365 Defender](mtp-enable.md).</span></span> 

<span data-ttu-id="004c6-262">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="004c6-262">Congratulations!</span></span> <span data-ttu-id="004c6-263">Vous venez de créer votre laboratoire d’évaluation ou votre environnement pilote Microsoft 365 Defender !</span><span class="sxs-lookup"><span data-stu-id="004c6-263">You've just created your Microsoft 365 Defender trial lab or pilot environment!</span></span> <span data-ttu-id="004c6-264">Vous pouvez désormais vous familiariser avec l’interface utilisateur de Microsoft 365 Defender !</span><span class="sxs-lookup"><span data-stu-id="004c6-264">Now you can familiarize yourself with the Microsoft 365 Defender user interface!</span></span> <span data-ttu-id="004c6-265">Consultez ce que vous pouvez apprendre à partir du guide interactif Microsoft 365 Defender et apprenez à utiliser chaque tableau de bord pour vos tâches de sécurité quotidiennes.</span><span class="sxs-lookup"><span data-stu-id="004c6-265">See what you can learn from the following Microsoft 365 Defender interactive guide and know how to use each dashboard for your day-to-day security operation tasks.</span></span>


>[!VIDEO https://aka.ms/MTP-Interactive-Guide]

<span data-ttu-id="004c6-266">Ensuite, vous pouvez simuler une attaque et voir comment les fonctionnalités du produit croisé détectent, créer des alertes et répondre automatiquement à une attaque en mode fichier sur un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c6-266">Next, you can simulate an attack and see how the cross product capabilities detect, create alerts, and automatically respond to a fileless attack on an endpoint.</span></span>

## <a name="next-step"></a><span data-ttu-id="004c6-267">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="004c6-267">Next step</span></span>
|[<span data-ttu-id="004c6-268">Phase de simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="004c6-268">Attack simulation phase</span></span>](mtp-pilot-simulate.md) | <span data-ttu-id="004c6-269">Exécutez la simulation d’attaque pour votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="004c6-269">Run the attack simulation for your Microsoft 365 Defender pilot environment.</span></span>
|:-------|:-----|
