---
title: Configurer les Microsoft 365 Defender pour le laboratoire d’essai ou l’environnement pilote
description: Configurez Microsoft 365 Defender piliers, tels que Microsoft Defender pour Office 365, Microsoft Defender pour l’identité, Microsoft Cloud App Security et Microsoft Defender pour endpoint, pour votre laboratoire d’évaluation ou votre environnement pilote.
keywords: configurer Microsoft 365 Defender d’essai, Microsoft 365 Defender d’essai, configurer Microsoft 365 Defender projet pilote, configurer Microsoft 365 Defender piliers, Microsoft 365 Defender piliers
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-scenario
- m365solution-evalutatemtp
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: e50210f02d14be33c357517515d456318aac4bb6
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229778"
---
# <a name="configure-microsoft-365-defender-pillars-for-your-trial-lab-or-pilot-environment"></a><span data-ttu-id="48b3f-104">Configurer les Microsoft 365 Defender pour votre laboratoire d’essai ou votre environnement pilote</span><span class="sxs-lookup"><span data-stu-id="48b3f-104">Configure Microsoft 365 Defender pillars for your trial lab or pilot environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="48b3f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="48b3f-105">**Applies to:**</span></span>
- <span data-ttu-id="48b3f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="48b3f-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="48b3f-107">La création d Microsoft 365 Defender laboratoire d’évaluation ou d’un environnement pilote et son déploiement sont un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="48b3f-107">Creating a Microsoft 365 Defender trial lab or pilot environment and deploying it is a three-phase process:</span></span>

|<span data-ttu-id="48b3f-108">[![Phase 1 : préparation](../../media/phase-diagrams/prepare.png)](prepare-m365d-eval.md)</span><span class="sxs-lookup"><span data-stu-id="48b3f-108">[![Phase 1: Prepare](../../media/phase-diagrams/prepare.png)](prepare-m365d-eval.md)</span></span><br/>[<span data-ttu-id="48b3f-109">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="48b3f-109">Phase 1: Prepare</span></span>](prepare-m365d-eval.md) |<span data-ttu-id="48b3f-110">[![Phase 2 : configuration](../../media/phase-diagrams/setup.png)](setup-m365deval.md)</span><span class="sxs-lookup"><span data-stu-id="48b3f-110">[![Phase 2: Set up](../../media/phase-diagrams/setup.png)](setup-m365deval.md)</span></span><br/>[<span data-ttu-id="48b3f-111">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="48b3f-111">Phase 2: Set up</span></span>](setup-m365deval.md) |![Phase 3 : intégration](../../media/phase-diagrams/onboard.png)<br/><span data-ttu-id="48b3f-113">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="48b3f-113">Phase 3: Onboard</span></span> | <span data-ttu-id="48b3f-114">[![Retour au pilote](../../media/phase-diagrams/backtopilot.png)](m365d-pilot.md)</span><span class="sxs-lookup"><span data-stu-id="48b3f-114">[![Back to pilot](../../media/phase-diagrams/backtopilot.png)](m365d-pilot.md)</span></span><br/>[<span data-ttu-id="48b3f-115">Retour au manuel pilote</span><span class="sxs-lookup"><span data-stu-id="48b3f-115">Back to pilot playbook</span></span>](m365d-pilot.md) |
|--|--|--|--|
|| |<span data-ttu-id="48b3f-116">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="48b3f-116">*You are here!*</span></span> | |

<span data-ttu-id="48b3f-117">Vous êtes actuellement en phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="48b3f-117">You're currently in the configuration phase.</span></span>

<span data-ttu-id="48b3f-118">La préparation est essentielle pour tout déploiement réussi.</span><span class="sxs-lookup"><span data-stu-id="48b3f-118">Preparation is key to any successful deployment.</span></span> <span data-ttu-id="48b3f-119">Dans cet article, vous serez guidé sur les points que vous devrez prendre en compte lorsque vous préparerez le déploiement de Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="48b3f-119">In this article, you'll be guided on the points you'll need to consider as you prepare to deploy Microsoft Defender for Endpoint.</span></span>

## <a name="microsoft-365-defender-pillars"></a><span data-ttu-id="48b3f-120">Microsoft 365 Defender piliers</span><span class="sxs-lookup"><span data-stu-id="48b3f-120">Microsoft 365 Defender pillars</span></span>
<span data-ttu-id="48b3f-121">Microsoft 365 Defender se compose de quatre piliers.</span><span class="sxs-lookup"><span data-stu-id="48b3f-121">Microsoft 365 Defender consists of four pillars.</span></span> <span data-ttu-id="48b3f-122">Bien qu’un pilier puisse déjà apporter une valeur ajoutée à la sécurité de votre organisation réseau, l’activation des quatre piliers Microsoft 365 Defender sera la valeur la plus importante pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="48b3f-122">Although one pillar can already provide value to your network organization's security, enabling the four Microsoft 365 Defender pillars will give your organization the most value.</span></span>

![Image of_Microsoft solution 365 Defender pour les utilisateurs, Microsoft Defender pour l’identité, pour les points de terminaison Microsoft Defender pour endpoint, pour les applications cloud, Microsoft Cloud App Security et pour les données, Microsoft Defender pour Office 365](../../media/mtp/m365pillars.png)

<span data-ttu-id="48b3f-124">Cette section vous guide pour configurer :</span><span class="sxs-lookup"><span data-stu-id="48b3f-124">This section will guide you to configure:</span></span>

- <span data-ttu-id="48b3f-125">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="48b3f-125">Microsoft Defender for Office 365</span></span>
- <span data-ttu-id="48b3f-126">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="48b3f-126">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="48b3f-127">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="48b3f-127">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="48b3f-128">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="48b3f-128">Microsoft Defender for Endpoint</span></span>

## <a name="configure-microsoft-defender-for-office-365"></a><span data-ttu-id="48b3f-129">Configurer Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="48b3f-129">Configure Microsoft Defender for Office 365</span></span>

> [!NOTE]
> <span data-ttu-id="48b3f-130">Ignorez cette étape si vous avez déjà activé Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="48b3f-130">Skip this step if you've already enabled Defender for Office 365.</span></span>

<span data-ttu-id="48b3f-131">Il existe un module PowerShell appelé *ORCA (Advanced Threat Protection Recommended Configuration Analyzer) Office 365* qui vous aide à déterminer certains de ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="48b3f-131">There's a PowerShell Module called the *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* that helps determine some of these settings.</span></span> <span data-ttu-id="48b3f-132">Lorsqu’il est exécuté en tant qu’administrateur dans votre client, get-ORCAReport vous aide à générer une évaluation des paramètres d’hygiène des messages anti-courrier indésirable, anti-hameçonnage et autres.</span><span class="sxs-lookup"><span data-stu-id="48b3f-132">When run as an administrator in your tenant, get-ORCAReport will help generate an assessment of the anti-spam, anti-phish, and other message hygiene settings.</span></span> <span data-ttu-id="48b3f-133">Vous pouvez télécharger ce module à partir https://www.powershellgallery.com/packages/ORCA/ de .</span><span class="sxs-lookup"><span data-stu-id="48b3f-133">You can download this module from https://www.powershellgallery.com/packages/ORCA/.</span></span>

1. <span data-ttu-id="48b3f-134">Accédez à [Office 365 stratégie de gestion des menaces & du Centre](https://protection.office.com/homepage)de sécurité et  >    >  **conformité.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-134">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Policy**.</span></span>

   ![Image of_Office page de stratégie de gestion des menaces du Centre de sécurité & conformité 365](../../media/mtp-eval-32.png)

2. <span data-ttu-id="48b3f-136">Cliquez **sur Anti-hameçonnage,** **sélectionnez Créer** et remplir le nom et la description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="48b3f-136">Click **Anti-phishing**, select **Create** and fill in the policy name and description.</span></span> <span data-ttu-id="48b3f-137">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-137">Click **Next**.</span></span>

   ![Image of_Office page de stratégie anti-hameçonnage du Centre de sécurité & conformité 365 dans laquelle vous pouvez nommer votre stratégie](../../media/mtp-eval-33.png)

   > [!NOTE]
   > <span data-ttu-id="48b3f-139">Modifiez votre stratégie anti-hameçonnage avancée dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="48b3f-139">Edit your Advanced anti-phishing policy in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="48b3f-140">Modifiez **le seuil de hameçonnage** avancé **sur 2 - Agressif**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-140">Change **Advanced Phishing Threshold** to **2 - Aggressive**.</span></span>

3. <span data-ttu-id="48b3f-141">Cliquez sur le menu déroulant Ajouter une **condition** et sélectionnez vos domaines comme domaine de destinataire.</span><span class="sxs-lookup"><span data-stu-id="48b3f-141">Click the **Add a condition** drop-down menu and select your domain(s) as recipient domain.</span></span> <span data-ttu-id="48b3f-142">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-142">Click **Next**.</span></span>

   ![Image of_Office page de stratégie anti-hameçonnage du Centre de sécurité & conformité 365 dans laquelle vous pouvez ajouter une condition pour son application](../../media/mtp-eval-34.png)

4. <span data-ttu-id="48b3f-144">Examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="48b3f-144">Review your settings.</span></span> <span data-ttu-id="48b3f-145">Cliquez **sur Créer cette stratégie pour** confirmer.</span><span class="sxs-lookup"><span data-stu-id="48b3f-145">Click **Create this policy** to confirm.</span></span>

   ![Image of_Office page de stratégie anti-hameçonnage du Centre de sécurité & et conformité 365 365 dans laquelle vous pouvez passer en revue vos paramètres et cliquer sur le bouton Créer cette stratégie](../../media/mtp-eval-35.png)

5. <span data-ttu-id="48b3f-147">Sélectionnez **Coffre pièces jointes** et l’option Activer la SharePoint **de SharePoint, OneDrive et Microsoft Teams** de saisie.</span><span class="sxs-lookup"><span data-stu-id="48b3f-147">Select **Safe Attachments** and select the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** option.</span></span>

   ![Image of_Office page du Centre de sécurité & conformité 365 dans laquelle vous pouvez activer la protection contre les SharePoint, les OneDrive et les Microsoft Teams](../../media/mtp-eval-36.png)

6. <span data-ttu-id="48b3f-149">Cliquez sur l’icône + pour créer une stratégie de pièces jointes sécurisées, puis appliquez-la en tant que domaine de destinataire à vos domaines.</span><span class="sxs-lookup"><span data-stu-id="48b3f-149">Click the + icon to create a new safe attachment policy, apply it as recipient domain to your domains.</span></span> <span data-ttu-id="48b3f-150">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-150">Click **Save**.</span></span>

   ![Image of_Office page du Centre de sécurité & conformité 365 dans laquelle vous pouvez créer une stratégie de pièces jointes sécurisées](../../media/mtp-eval-37.png)

7. <span data-ttu-id="48b3f-152">Ensuite, sélectionnez la **stratégie Coffre liens,** puis cliquez sur l’icône de crayon pour modifier la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="48b3f-152">Next, select the **Safe Links** policy, then click the pencil icon to edit the default policy.</span></span>

8. <span data-ttu-id="48b3f-153">Assurez-vous que l’option Ne pas **me** suivre lorsque les utilisateurs cliquent sur l’option Liens sécurisés n’est pas sélectionnée, tandis que les autres options sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="48b3f-153">Make sure that the **Do not track when users click safe links** option is not selected, while the rest of the options are selected.</span></span> <span data-ttu-id="48b3f-154">Pour [plus d Coffre, voir les paramètres](/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365) des liens.</span><span class="sxs-lookup"><span data-stu-id="48b3f-154">See [Safe Links settings](/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365) for details.</span></span> <span data-ttu-id="48b3f-155">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-155">Click **Save**.</span></span>

   ![Image of_Office page du Centre de sécurité & conformité 365 qui indique que l’option Ne pas suivre quand les utilisateurs cliquent sur la sécurité n’est pas sélectionnée](../../media/mtp-eval-38.png)

9. <span data-ttu-id="48b3f-157">Sélectionnez ensuite la **stratégie anti-programme** malveillant, sélectionnez la stratégie par défaut, puis choisissez l’icône de crayon.</span><span class="sxs-lookup"><span data-stu-id="48b3f-157">Next select the **Anti-malware** policy, select the default, and choose the pencil icon.</span></span>

10. <span data-ttu-id="48b3f-158">Cliquez **Paramètres** sélectionnez Oui et **utilisez le texte** de notification par défaut pour activer la réponse de détection de **programmes malveillants.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-158">Click **Settings** and select **Yes and use the default notification text** to enable **Malware Detection Response**.</span></span> <span data-ttu-id="48b3f-159">Activer le **filtre Types de pièces jointes courants.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-159">Turn the **Common Attachment Types Filter** on.</span></span> <span data-ttu-id="48b3f-160">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-160">Click **Save**.</span></span>

    ![Image of_Office 365 Security & Compliance Center qui indique que la réponse de détection de programmes malveillants est allumée avec la notification par défaut et que le filtre des types de pièces jointes courants est allumé](../../media/mtp-eval-39.png)

11. <span data-ttu-id="48b3f-162">Accédez à [Office 365 recherche dans](https://protection.office.com/homepage)& du journal d’audit du Centre de sécurité et conformité et activer  >    >   l’audit.</span><span class="sxs-lookup"><span data-stu-id="48b3f-162">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Search** > **Audit log search** and turn Auditing on.</span></span>

    ![Image of_Office 365 Security & Compliance Center où vous pouvez activer la recherche dans le journal d’audit](../../media/mtp-eval-40.png)

12. <span data-ttu-id="48b3f-164">Intégrez Microsoft Defender pour Office 365 microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="48b3f-164">Integrate Microsoft Defender for Office 365 with Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="48b3f-165">Accédez [à Office 365 l&](https://protection.office.com/homepage)de gestion des menaces du Centre de sécurité et conformité et sélectionnez Microsoft Defender pour le point de terminaison Paramètres dans le coin supérieur droit  >    >   de l’écran. </span><span class="sxs-lookup"><span data-stu-id="48b3f-165">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Explorer** and select **Microsoft Defender for Endpoint Settings** on the upper right corner of the screen.</span></span> <span data-ttu-id="48b3f-166">Dans la boîte de dialogue de connexion Defender pour point de terminaison, Connecter **à Microsoft Defender pour le point de terminaison.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-166">In the Defender for Endpoint connection dialog box, turn on **Connect to Microsoft Defender for Endpoint**.</span></span>

    ![Image of_Office page du Centre de sécurité & conformité 365 dans laquelle vous pouvez activer la connexion Microsoft Defender pour le point de terminaison](../../media/mtp-eval-41.png)

## <a name="configure-microsoft-defender-for-identity"></a><span data-ttu-id="48b3f-168">Configurer Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="48b3f-168">Configure Microsoft Defender for Identity</span></span>

> [!NOTE]
> <span data-ttu-id="48b3f-169">Ignorez cette étape si vous avez déjà activé Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="48b3f-169">Skip this step if you've already enabled Microsoft Defender for Identity</span></span>

1. <span data-ttu-id="48b3f-170">Accédez à [Microsoft 365 Centre de](https://security.microsoft.com/info) sécurité > sélectionnez Plus de **ressources** Microsoft Defender  >  **pour l’identité.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-170">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > select **More Resources** > **Microsoft Defender for Identity**.</span></span>

   ![Image of_Microsoft page du Centre de sécurité 365 dans laquelle il existe une option pour ouvrir Microsoft Defender pour l’identité](../../media/mtp-eval-42.png)

2. <span data-ttu-id="48b3f-172">Cliquez **sur Créer** pour démarrer l’Assistant Microsoft Defender pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="48b3f-172">Click **Create** to start the Microsoft Defender for Identity wizard.</span></span>

   ![Image of_Microsoft page de l’Assistant Defender pour l’identité où vous devez cliquer sur le bouton Créer](../../media/mtp-eval-43.png)

3. <span data-ttu-id="48b3f-174">Choisissez **Fournir un nom d’utilisateur et un mot de passe pour vous connecter à votre forêt Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-174">Choose **Provide a username and password to connect to your Active Directory forest**.</span></span>

   ![Image of_Microsoft page d’accueil de Defender for Identity](../../media/mtp-eval-44.png)

4. <span data-ttu-id="48b3f-176">Entrez vos informations d’identification actives sur site.</span><span class="sxs-lookup"><span data-stu-id="48b3f-176">Enter your Active Directory on-premises credentials.</span></span> <span data-ttu-id="48b3f-177">Il peut s’y trouver n’importe quel compte d’utilisateur qui dispose d’un accès en lecture à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48b3f-177">This can be any user account that has read access to Active Directory.</span></span>

   ![Image of_Microsoft page Defender for Identity Directory services où vous devez placer vos informations d’identification](../../media/mtp-eval-45.png)

5. <span data-ttu-id="48b3f-179">Ensuite, **sélectionnez Télécharger le programme d’installation du** capteur et transférer le fichier vers votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="48b3f-179">Next, choose **Download Sensor Setup** and transfer file to your domain controller.</span></span>

   ![Image of_Microsoft page Defender for Identity dans laquelle vous pouvez sélectionner Télécharger le programme d’installation du capteur](../../media/mtp-eval-46.png)

6. <span data-ttu-id="48b3f-181">Exécutez le programme d’installation de Microsoft Defender for Identity Sensor et commencez à suivre l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="48b3f-181">Execute the Microsoft Defender for Identity Sensor Setup and begin following the wizard.</span></span>

   ![Image of_Microsoft page Defender pour l’identité dans laquelle vous devez cliquer en suivant l’Assistant Capteur Microsoft Defender pour l’identité](../../media/mtp-eval-47.png)

7. <span data-ttu-id="48b3f-183">Cliquez **sur Suivant** au niveau du type de déploiement du capteur.</span><span class="sxs-lookup"><span data-stu-id="48b3f-183">Click **Next** at the sensor deployment type.</span></span>

   ![Image of_Microsoft page Defender pour l’identité où vous devez cliquer en suivant pour passer à la page suivante](../../media/mtp-eval-48.png)

8. <span data-ttu-id="48b3f-185">Copiez la touche d’accès rapide, car vous devez la saisir ensuite dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="48b3f-185">Copy the access key because you need to enter it next in the Wizard.</span></span>

   ![Page of_the capteurs d’image où vous devez copier la touche d’accès rapide que vous devez entrer dans la prochaine page de l’Assistant Configuration du capteur Microsoft Defender pour l’identité](../../media/mtp-eval-49.png)

9. <span data-ttu-id="48b3f-187">Copiez la touche d’accès rapide dans l’Assistant, puis cliquez sur **Installer.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-187">Copy the access key into the Wizard and click **Install**.</span></span>

   ![Image of_Microsoft’Assistant Capteur d’identité dans laquelle vous devez fournir la touche d’accès rapide, puis cliquer sur le bouton d’installation](../../media/mtp-eval-50.png)

10. <span data-ttu-id="48b3f-189">Félicitations, vous avez correctement configuré Microsoft Defender pour l’identité sur votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="48b3f-189">Congratulations, you've successfully configured Microsoft Defender for Identity on your domain controller.</span></span>

    ![Image of_Microsoft l’installation de l’Assistant Capteur d’identité, où vous devez cliquer sur le bouton Terminer](../../media/mtp-eval-51.png)

11. <span data-ttu-id="48b3f-191">Sous la section [Paramètres de Microsoft Defender pour](https://go.microsoft.com/fwlink/?linkid=2040449) l’identité, sélectionnez \*\*Microsoft Defender pour le point de terminaison \*\*, puis activer le basculement.</span><span class="sxs-lookup"><span data-stu-id="48b3f-191">Under the [Microsoft Defender for Identity](https://go.microsoft.com/fwlink/?linkid=2040449) settings section, select \*\*Microsoft Defender for Endpoint \*\*, then turn on the toggle.</span></span> <span data-ttu-id="48b3f-192">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-192">Click **Save**.</span></span>

    ![Image of_the page des paramètres de Microsoft Defender pour l’identité dans laquelle vous devez activer le basculement De Microsoft Defender pour le point de terminaison](../../media/mtp-eval-52.png)

## <a name="configure-microsoft-cloud-app-security"></a><span data-ttu-id="48b3f-194">Configurer Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="48b3f-194">Configure Microsoft Cloud App Security</span></span>

> [!NOTE]
> <span data-ttu-id="48b3f-195">Ignorez cette étape si vous avez déjà activé Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="48b3f-195">Skip this step if you've already enabled Microsoft Cloud App Security.</span></span>

1. <span data-ttu-id="48b3f-196">Accédez à [Microsoft 365 centre de sécurité Plus](https://security.microsoft.com/info)de  >  **ressources**  >  **Microsoft Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-196">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Cloud App Security**.</span></span>

   ![Image of_Microsoft page centre de sécurité 365 dans laquelle vous pouvez voir la carte Microsoft Cloud App et qui doit cliquer sur le bouton d’ouverture](../../media/mtp-eval-53.png)

2. <span data-ttu-id="48b3f-198">À l’invite d’informations pour intégrer Microsoft Defender pour l’identité, sélectionnez **Activer Microsoft Defender pour l’intégration des données d’identité.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-198">At the information prompt to integrate Microsoft Defender for Identity, select **Enable Microsoft Defender for Identity data integration**.</span></span>

   ![Image of_the’invite d’informations pour intégrer Microsoft Defender pour l’identité où vous devez sélectionner le lien Activer Microsoft Defender pour l’intégration des données d’identité](../../media/mtp-eval-54.png)

   > [!NOTE]
   > <span data-ttu-id="48b3f-200">Si vous ne voyez pas cette invite, cela peut signifier que l’intégration des données microsoft Defender pour l’identité a déjà été activée.</span><span class="sxs-lookup"><span data-stu-id="48b3f-200">If you don’t see this prompt, it might mean that your Microsoft Defender for Identity data integration has already been enabled.</span></span> <span data-ttu-id="48b3f-201">Toutefois, si vous n’êtes pas sûr, contactez votre administrateur informatique pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="48b3f-201">However, if you are not sure, contact your IT Administrator to confirm.</span></span>

3. <span data-ttu-id="48b3f-202">Go to **Paramètres,** turn on the **Microsoft Defender for Identity integration** toggle, then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-202">Go to **Settings**, turn on the **Microsoft Defender for Identity integration** toggle, then click **Save**.</span></span>

   ![Image of_the page des paramètres dans laquelle vous devez activer le bouton bascule d’intégration Microsoft Defender pour l’identité, puis cliquez sur Enregistrer](../../media/mtp-eval-55.png)

   > [!NOTE]
   > <span data-ttu-id="48b3f-204">Pour les nouvelles instances de Microsoft Defender pour l’identité, ce basculement d’intégration est automatiquement allumé.</span><span class="sxs-lookup"><span data-stu-id="48b3f-204">For new Microsoft Defender for Identity instances, this integration toggle is automatically turned on.</span></span> <span data-ttu-id="48b3f-205">Confirmez que l’intégration de Microsoft Defender for Identity a été activée avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="48b3f-205">Confirm that your Microsoft Defender for Identity integration has been enabled before you proceed to the next step.</span></span>

4. <span data-ttu-id="48b3f-206">Sous les paramètres de découverte cloud, sélectionnez **Microsoft Defender pour l’intégration de point** de terminaison, puis activez l’intégration.</span><span class="sxs-lookup"><span data-stu-id="48b3f-206">Under the Cloud discovery settings, select **Microsoft Defender for Endpoint integration**, then enable the integration.</span></span> <span data-ttu-id="48b3f-207">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-207">Click **Save**.</span></span>

   ![Image of_the page Microsoft Defender pour point de terminaison dans laquelle la case à cocher Bloquer les applications non sélectionnées sous Microsoft Defender pour l’intégration de point de terminaison est sélectionnée.](../../media/mtp-eval-56.png)

5. <span data-ttu-id="48b3f-210">Sous Paramètres de découverte cloud, sélectionnez **Enrichissement de** l’utilisateur, puis activez l’intégration avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48b3f-210">Under Cloud discovery settings, select **User enrichment**, then enable the integration with Azure Active Directory.</span></span>

   ![Image de la section Enrichissement d’utilisateurs dans laquelle la case à cocher Enrichissement d’utilisateurs découverts Azure Active Directory des noms d’utilisateurs est cocher](../../media/mtp-eval-57.png)

## <a name="configure-microsoft-defender-for-endpoint"></a><span data-ttu-id="48b3f-212">Configurer Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="48b3f-212">Configure Microsoft Defender for Endpoint</span></span>

> [!NOTE]
> <span data-ttu-id="48b3f-213">Ignorez cette étape si vous avez déjà activé Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="48b3f-213">Skip this step if you've already enabled Microsoft Defender for Endpoint.</span></span>

1. <span data-ttu-id="48b3f-214">Accédez à [Microsoft 365 centre de sécurité Plus](https://security.microsoft.com/info)de  >  **ressources**  >  **Centre de sécurité Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-214">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Defender Security Center**.</span></span> <span data-ttu-id="48b3f-215">Cliquez sur **Ouvrir**. </span><span class="sxs-lookup"><span data-stu-id="48b3f-215">Click **Open**.</span></span>

   ![Image of_Microsoft’option Centre de sécurité Defender dans la page centre Microsoft 365 sécurité](../../media/mtp-eval-58.png)

2. <span data-ttu-id="48b3f-217">Suivez l’Assistant Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="48b3f-217">Follow the Microsoft Defender for Endpoint wizard.</span></span> <span data-ttu-id="48b3f-218">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-218">Click **Next**.</span></span>

   ![Image of_the Centre de sécurité Microsoft Defender page de l’Assistant d’accueil](../../media/mtp-eval-59.png)

3. <span data-ttu-id="48b3f-220">Choisissez en fonction de votre emplacement de stockage de données préféré, de votre stratégie de rétention des données, de la taille de l’organisation et de votre choix pour les fonctionnalités de prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="48b3f-220">Choose based on your preferred data storage location, data retention policy, organization size, and opt-in for preview features.</span></span>

   ![Image of_the page pour sélectionner votre pays de stockage de données, votre stratégie de rétention et la taille de votre organisation.](../../media/mtp-eval-60.png)

   > [!NOTE]
   > <span data-ttu-id="48b3f-223">Vous ne pouvez pas modifier certains paramètres, tels que l’emplacement de stockage des données, par la suite.</span><span class="sxs-lookup"><span data-stu-id="48b3f-223">You cannot change some of the settings, like data storage location, afterwards.</span></span>

   <span data-ttu-id="48b3f-224">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-224">Click **Next**.</span></span>

4. <span data-ttu-id="48b3f-225">Cliquez **sur Continuer** pour mettre en service votre client Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="48b3f-225">Click **Continue** and it will provision your Microsoft Defender for Endpoint tenant.</span></span>

   ![Image of_the page vous invite à cliquer sur le bouton Continuer pour créer votre instance cloud](../../media/mtp-eval-61.png)

5. <span data-ttu-id="48b3f-227">Intégrer vos points de terminaison via des stratégies de groupe, Microsoft Endpoint Manager ou en exécutant un script local dans Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="48b3f-227">Onboard your endpoints through Group Policies, Microsoft Endpoint Manager or by running a local script to Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="48b3f-228">Par souci de simplicité, ce guide utilise le script local.</span><span class="sxs-lookup"><span data-stu-id="48b3f-228">For simplicity, this guide uses the local script.</span></span>

6. <span data-ttu-id="48b3f-229">Cliquez **sur Télécharger le package** et copiez le script d’intégration sur vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="48b3f-229">Click **Download package** and copy the onboarding script to your endpoint(s).</span></span>

   ![Image of_page vous invite à cliquer sur le bouton Télécharger le package pour copier le script d’intégration sur vos points de terminaison ou points de terminaison](../../media/mtp-eval-62.png)

7. <span data-ttu-id="48b3f-231">Sur votre point de terminaison, exécutez le script d’intégration en tant qu’administrateur et choisissez Y.</span><span class="sxs-lookup"><span data-stu-id="48b3f-231">On your endpoint, run the onboarding script as Administrator and choose Y.</span></span>

   ![Image of_the ligne de commande dans laquelle vous exécutez le script d’intégration et choisissez Y pour continuer](../../media/mtp-eval-63.png)

8. <span data-ttu-id="48b3f-233">Félicitations, vous avez intégré votre premier point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="48b3f-233">Congratulations, you've onboarded your first endpoint.</span></span>

   ![Image of_the ligne de commande dans laquelle vous obtenez la confirmation que vous avez intégré votre premier point de terminaison.](../../media/mtp-eval-64.png)

9. <span data-ttu-id="48b3f-236">Copiez-collez le test de détection à partir de l’Assistant Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="48b3f-236">Copy-paste the detection test from the Microsoft Defender for Endpoint wizard.</span></span>

   ![Image of_the exécuter une étape de test de détection dans laquelle vous devez cliquer sur Copier pour copier le script de test de détection à coller dans l’invite de commandes](../../media/mtp-eval-65.png)

10. <span data-ttu-id="48b3f-238">Copiez le script PowerShell dans une invite de commandes avec élévation de niveaux et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="48b3f-238">Copy the PowerShell script to an elevated command prompt and run it.</span></span>

    ![Image of_command’invite de commandes où vous devez copier le script PowerShell dans une invite de commandes avec élévation de élévation de niveaux et l’exécuter](../../media/mtp-eval-66.png)

11. <span data-ttu-id="48b3f-240">Sélectionnez **Démarrer à l’aide de Microsoft Defender pour le point de terminaison à partir** de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="48b3f-240">Select **Start using Microsoft Defender for Endpoint** from the Wizard.</span></span>

    ![Image of_the’invite de confirmation à partir de l’Assistant où vous devez cliquer sur Démarrer à l’aide de Microsoft Defender pour le point de terminaison](../../media/mtp-eval-67.png)

12. <span data-ttu-id="48b3f-242">Visitez le [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/).</span><span class="sxs-lookup"><span data-stu-id="48b3f-242">Visit the [Microsoft Defender Security Center](https://securitycenter.windows.com/).</span></span> <span data-ttu-id="48b3f-243">Go to **Paramètres** and then select **Advanced features**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-243">Go to **Settings** and then select **Advanced features**.</span></span>

    ![Image of_Microsoft du centre de sécurité Defender Paramètres dans lequel vous devez sélectionner les fonctionnalités avancées](../../media/mtp-eval-68.png)

13. <span data-ttu-id="48b3f-245">Activer l’intégration avec **Microsoft Defender pour l’identité.**</span><span class="sxs-lookup"><span data-stu-id="48b3f-245">Turn on the integration with **Microsoft Defender for Identity**.</span></span>

    ![Image of_Microsoft fonctionnalités avancées du Centre de sécurité Defender, bascule de l’option Microsoft Defender pour l’identité que vous devez activer](../../media/mtp-eval-69.png)

14. <span data-ttu-id="48b3f-247">Activer l’intégration avec **Office 365 Threat Intelligence**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-247">Turn on the integration with **Office 365 Threat Intelligence**.</span></span>

    ![Image of_Microsoft fonctionnalités avancées du Centre de sécurité Defender, Office 365'option Threat Intelligence que vous devez activer](../../media/mtp-eval-70.png)

15. <span data-ttu-id="48b3f-249">Activer l’intégration avec **Microsoft Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-249">Turn on integration with **Microsoft Cloud App Security**.</span></span>

    ![Image of_Microsoft fonctionnalités avancées du Centre de sécurité Defender, Microsoft Cloud App Security d’option que vous devez activer](../../media/mtp-eval-71.png)

16. <span data-ttu-id="48b3f-251">Faites défiler vers le bas et cliquez **sur Enregistrer les préférences** pour confirmer les nouvelles intégrations.</span><span class="sxs-lookup"><span data-stu-id="48b3f-251">Scroll down and click **Save preferences** to confirm the new integrations.</span></span>

    ![Bouton of_Save des préférences de l’image que vous devez cliquer](../../media/mtp-eval-72.png)

## <a name="start-the-microsoft-365-defender-service"></a><span data-ttu-id="48b3f-253">Démarrer le service Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="48b3f-253">Start the Microsoft 365 Defender service</span></span>

> [!NOTE]
> <span data-ttu-id="48b3f-254">À compter du 1er juin 2020, Microsoft active automatiquement les fonctionnalités Microsoft 365 Defender pour tous les clients éligibles.</span><span class="sxs-lookup"><span data-stu-id="48b3f-254">Starting June 1, 2020, Microsoft automatically enables Microsoft 365 Defender features for all eligible tenants.</span></span> <span data-ttu-id="48b3f-255">Consultez cet [article microsoft Tech Community sur l’éligibilité](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/microsoft-threat-protection-will-automatically-turn-on-for/ba-p/1345426) aux licences pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="48b3f-255">See this [Microsoft Tech Community article on license eligibility](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/microsoft-threat-protection-will-automatically-turn-on-for/ba-p/1345426) for details.</span></span>

<span data-ttu-id="48b3f-256">Go to [Microsoft 365 Security Center](https://security.microsoft.com/homepage).</span><span class="sxs-lookup"><span data-stu-id="48b3f-256">Go to [Microsoft 365 Security Center](https://security.microsoft.com/homepage).</span></span> <span data-ttu-id="48b3f-257">Accédez **à Paramètres** puis sélectionnez **Microsoft 365 Defender**.</span><span class="sxs-lookup"><span data-stu-id="48b3f-257">Navigate to **Settings** and then select **Microsoft 365 Defender**.</span></span>

![Image of_Microsoft’option 365 Defender à partir de la page Microsoft 365 de sécurité Paramètres de sécurité](../../media/mtp-eval-72b.png)

<span data-ttu-id="48b3f-259">Pour obtenir des instructions plus complètes, voir [Activer Microsoft 365 Defender](m365d-enable.md).</span><span class="sxs-lookup"><span data-stu-id="48b3f-259">For a more comprehensive guidance, see [Turn on Microsoft 365 Defender](m365d-enable.md).</span></span>

<span data-ttu-id="48b3f-260">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="48b3f-260">Congratulations!</span></span> <span data-ttu-id="48b3f-261">Vous viennent de créer votre laboratoire d Microsoft 365 Defender d’essai ou votre environnement pilote !</span><span class="sxs-lookup"><span data-stu-id="48b3f-261">You've just created your Microsoft 365 Defender trial lab or pilot environment!</span></span> <span data-ttu-id="48b3f-262">Vous pouvez maintenant vous familiariser avec l’interface Microsoft 365 Defender’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48b3f-262">Now you can familiarize yourself with the Microsoft 365 Defender user interface!</span></span> <span data-ttu-id="48b3f-263">Découvrez ce que vous pouvez apprendre à partir du guide Microsoft 365 Defender interactif et découvrez comment utiliser chaque tableau de bord pour vos tâches quotidiennes d’opération de sécurité.</span><span class="sxs-lookup"><span data-stu-id="48b3f-263">See what you can learn from the following Microsoft 365 Defender interactive guide and know how to use each dashboard for your day-to-day security operation tasks.</span></span>

[<span data-ttu-id="48b3f-264">Consulter le guide interactif</span><span class="sxs-lookup"><span data-stu-id="48b3f-264">Check out the interactive guide</span></span>](https://aka.ms/MTP-Interactive-Guide)

<span data-ttu-id="48b3f-265">Ensuite, vous pouvez simuler une attaque et voir comment les fonctionnalités entre produits détectent, créent des alertes et répondent automatiquement à une attaque sans fichier sur un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="48b3f-265">Next, you can simulate an attack and see how the cross product capabilities detect, create alerts, and automatically respond to a fileless attack on an endpoint.</span></span>

## <a name="next-step"></a><span data-ttu-id="48b3f-266">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="48b3f-266">Next step</span></span>

- <span data-ttu-id="48b3f-267">[Générez une alerte de test](generate-test-alert.md) : exécutez une simulation d’attaque dans Microsoft 365 Defender laboratoire d’essai.</span><span class="sxs-lookup"><span data-stu-id="48b3f-267">[Generate a test alert](generate-test-alert.md) - Run an attack simulation in your Microsoft 365 Defender trial lab.</span></span>
