---
title: Configurer les piliers de la protection contre les menaces Microsoft pour le laboratoire d’évaluation ou l’environnement pilote
description: Configurez les piliers de protection de Microsoft contre les menaces, comme Office 365 ATP, Azure ATP, Microsoft Cloud App Security et Microsoft Defender ATP, pour votre laboratoire d’évaluation ou votre environnement pilote.
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
- m365solution-evalutatemtp
ms.topic: article
ms.openlocfilehash: 79e141ad85eecab827e0caa98fe022f88335c671
ms.sourcegitcommit: 9d8d071659e662c266b101377e24549963e43fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "48368148"
---
# <a name="configure-microsoft-threat-protection-pillars-for-your-trial-lab-or-pilot-environment"></a><span data-ttu-id="a7f5b-104">Configurer les piliers de protection contre les menaces Microsoft pour votre laboratoire d’évaluation ou votre environnement pilote</span><span class="sxs-lookup"><span data-stu-id="a7f5b-104">Configure Microsoft Threat Protection pillars for your trial lab or pilot environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a7f5b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a7f5b-105">**Applies to:**</span></span>
- <span data-ttu-id="a7f5b-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a7f5b-106">Microsoft Threat Protection</span></span>


<span data-ttu-id="a7f5b-107">La création d’un laboratoire de test Microsoft Threat Protection ou d’un environnement pilote et son déploiement est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="a7f5b-107">Creating a Microsoft Threat Protection trial lab or pilot environment and deploying it is a three-phase process:</span></span>

<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" >
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval?view=o365-worldwide"> 
        <img src="../../media/prepare.png" alt="Prepare your Microsoft Threat Protection trial lab or pilot environment" title="Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection" />
      <br/><span data-ttu-id="a7f5b-109">Phase 1 : préparer </a></span><span class="sxs-lookup"><span data-stu-id="a7f5b-109">Phase 1: Prepare </a></span></span><br>
    </td>
     <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/setup-mtpeval?view=o365-worldwide">
        <img src="../../media/setup.png" alt="Set up your Microsoft Threat Protection trial lab or pilot environment" title="Configuration de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection" />
      <br/><span data-ttu-id="a7f5b-111">Phase 2 : configuration </a></span><span class="sxs-lookup"><span data-stu-id="a7f5b-111">Phase 2: Setup </a></span></span><br>
    </td>
    <td align="center" bgcolor="#d5f5e3">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/config-mtpeval?view=o365-worldwide">
        <img src="../../media/config-onboard.png" alt="Configure & Onboard" title="Configurez chaque pilier de protection contre les menaces Microsoft pour votre laboratoire d’évaluation de la protection contre les menaces Microsoft ou votre environnement pilote et vos points de terminaison intégrés." />
      <br/><span data-ttu-id="a7f5b-113">Phase 3 : configurer & Onboard </a></span><span class="sxs-lookup"><span data-stu-id="a7f5b-113">Phase 3: Configure & Onboard </a></span></span><br>
</td>
  </tr>
</table>

<span data-ttu-id="a7f5b-114">Vous êtes actuellement en phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-114">You're currently in the configuration phase.</span></span>


<span data-ttu-id="a7f5b-115">La préparation est essentielle à tout déploiement réussi.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-115">Preparation is key to any successful deployment.</span></span> <span data-ttu-id="a7f5b-116">Dans cet article, vous serez guidé sur les points que vous devrez prendre en compte lors de la préparation du déploiement de Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-116">In this article, you'll be guided on the points you'll need to consider as you prepare to deploy Microsoft Defender ATP.</span></span>


## <a name="microsoft-threat-protection-pillars"></a><span data-ttu-id="a7f5b-117">Pilier de la protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a7f5b-117">Microsoft Threat Protection pillars</span></span>
<span data-ttu-id="a7f5b-118">La protection contre les menaces Microsoft se compose de quatre piliers.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-118">Microsoft Threat Protection consists of four pillars.</span></span> <span data-ttu-id="a7f5b-119">Bien qu’un seul pilier puisse déjà fournir de la valeur à la sécurité de votre organisation réseau, l’activation des quatre piliers de protection de Microsoft contre les menaces permettra à votre organisation de bénéficier de la plus grande valeur.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-119">Although one pillar can already provide value to your network organization's security, enabling the four Microsoft Threat Protection pillars will give your organization the most value.</span></span>

![<span data-ttu-id="a7f5b-120">Solution d’image of_Microsoft de protection contre les menaces pour les utilisateurs, Azure Advanced Threat Protection, pour les points de terminaison Microsoft Defender Advanced Threat Protection, pour les applications Cloud, Microsoft Cloud App Security et for Data, Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a7f5b-120">Image of_Microsoft Threat Protection solution for users, Azure Advanced Threat Protection, for endpoints Microsoft Defender Advanced Threat Protection, for cloud apps, Microsoft Cloud App Security, and for data, Office 365 Advanced Threat Protection</span></span>  ](../../media/mtp-eval-31.png)

<span data-ttu-id="a7f5b-121">Cette section vous guidera dans la configuration des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a7f5b-121">This section will guide you to configure:</span></span>
-   <span data-ttu-id="a7f5b-122">Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a7f5b-122">Office 365 Advanced Threat Protection</span></span>
-   <span data-ttu-id="a7f5b-123">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a7f5b-123">Azure Advanced Threat Protection</span></span> 
-   <span data-ttu-id="a7f5b-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a7f5b-124">Microsoft Cloud App Security</span></span>
-   <span data-ttu-id="a7f5b-125">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a7f5b-125">Microsoft Defender Advanced Threat Protection</span></span>


## <a name="configure-office-365-advanced-threat-protection"></a><span data-ttu-id="a7f5b-126">Configurer la protection avancée contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="a7f5b-126">Configure Office 365 Advanced Threat Protection</span></span>

>[!NOTE]
><span data-ttu-id="a7f5b-127">Ignorez cette étape si vous avez déjà activé la protection avancée contre les menaces d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-127">Skip this step if you've already enabled Office 365 Advanced Threat Protection.</span></span> 

<span data-ttu-id="a7f5b-128">Il existe un module PowerShell appelé *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* qui permet de déterminer certains de ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-128">There's a PowerShell Module called the *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* that helps determine some of these settings.</span></span> <span data-ttu-id="a7f5b-129">Lorsqu’il est exécuté en tant qu’administrateur dans votre client, Get-ORCAReport permet de générer une évaluation du blocage du courrier indésirable, des hameçons et d’autres paramètres d’hygiène des messages.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-129">When run as an administrator in your tenant, get-ORCAReport will help generate an assessment of the anti-spam, anti-phish, and other message hygiene settings.</span></span> <span data-ttu-id="a7f5b-130">Vous pouvez télécharger ce module à partir de https://www.powershellgallery.com/packages/ORCA/ .</span><span class="sxs-lookup"><span data-stu-id="a7f5b-130">You can download this module from https://www.powershellgallery.com/packages/ORCA/.</span></span> 

1. <span data-ttu-id="a7f5b-131">Accédez à la stratégie de gestion des menaces du [Centre de sécurité & conformité Office 365](https://protection.office.com/homepage)  >  **Threat management**  >  **Policy**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-131">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Policy**.</span></span>

   ![Image of_Office 365 sécurité & Centre de conformité gestion des menaces-page de stratégie](../../media/mtp-eval-32.png)
 
2. <span data-ttu-id="a7f5b-133">Cliquez sur **protection contre le hameçonnage ATP**, sélectionnez **créer** et renseignez le nom et la description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-133">Click **ATP anti-phishing**, select **Create** and fill in the policy name and description.</span></span> <span data-ttu-id="a7f5b-134">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-134">Click **Next**.</span></span>

   ![Page de la stratégie anti-hameçonnage du centre de sécurité & de l’image of_Office 365, dans laquelle vous pouvez nommer votre stratégie](../../media/mtp-eval-33.png)

   > [!NOTE]
   > <span data-ttu-id="a7f5b-136">Modifiez votre stratégie anti-hameçonnage avancée ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-136">Edit your Advanced ATP anti-phishing policy.</span></span> <span data-ttu-id="a7f5b-137">Remplacez le **seuil d’hameçonnage avancé** par **2**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-137">Change **Advanced Phishing Threshold** to **2 - Aggressive**.</span></span>

3. <span data-ttu-id="a7f5b-138">Cliquez sur le menu déroulant **Ajouter une condition** , puis sélectionnez vos domaines en tant que domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-138">Click the **Add a condition** drop-down menu and select your domain(s) as recipient domain.</span></span> <span data-ttu-id="a7f5b-139">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-139">Click **Next**.</span></span>

   ![Page de la stratégie anti-hameçonnage du centre de sécurité & de l’image of_Office 365, dans laquelle vous pouvez ajouter une condition pour son application](../../media/mtp-eval-34.png)
 
4. <span data-ttu-id="a7f5b-141">Vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-141">Review your settings.</span></span> <span data-ttu-id="a7f5b-142">Cliquez sur **créer cette stratégie** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-142">Click **Create this policy** to confirm.</span></span> 

   ![Image of_Office 365 sécurité & de la page de stratégie anti-hameçonnage du centre de conformité, dans laquelle vous pouvez vérifier vos paramètres et cliquer sur le bouton créer cette stratégie](../../media/mtp-eval-35.png)
 
5. <span data-ttu-id="a7f5b-144">Sélectionnez **pièces jointes fiables ATP** et sélectionnez l’option Activer la protection avancée contre les menaces **pour SharePoint, OneDrive et Microsoft teams** .</span><span class="sxs-lookup"><span data-stu-id="a7f5b-144">Select **ATP Safe attachments** and select the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** option.</span></span>

   ![Image of_Office 365 page Centre de sécurité & conformité, dans laquelle vous pouvez activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams](../../media/mtp-eval-36.png)

6. <span data-ttu-id="a7f5b-146">Cliquez sur l’icône + pour créer une stratégie de pièces jointes fiables, appliquez-la en tant que domaine de destinataire à vos domaines.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-146">Click the + icon to create a new safe attachment policy, apply it as recipient domain to your domains.</span></span> <span data-ttu-id="a7f5b-147">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-147">Click **Save**.</span></span>

   ![Image of_Office 365 page du centre de sécurité & conformité où vous pouvez créer une nouvelle stratégie de pièces jointes fiables](../../media/mtp-eval-37.png)
 
7. <span data-ttu-id="a7f5b-149">Ensuite, sélectionnez la stratégie de **liens approuvés ATP** , puis cliquez sur l’icône représentant un crayon pour modifier la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-149">Next, select the **ATP Safe Links** policy, then click the pencil icon to edit the default policy.</span></span>

8. <span data-ttu-id="a7f5b-150">Assurez-vous que l’option **ne pas suivre lorsque les utilisateurs cliquent sur les liens approuvés** n’est pas sélectionnée, tandis que les autres options sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-150">Make sure that the **Do not track when users click safe links** option is not selected, while the rest of the options are selected.</span></span> <span data-ttu-id="a7f5b-151">Pour plus d’informations, voir [paramètres de liens fiables](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp) .</span><span class="sxs-lookup"><span data-stu-id="a7f5b-151">See [Safe Links settings](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp) for details.</span></span> <span data-ttu-id="a7f5b-152">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-152">Click **Save**.</span></span> 

   ![Image of_Office 365 page du centre de sécurité & conformité qui indique que l’option ne suit pas lorsque les utilisateurs cliquent sur Safe n’est pas sélectionné](../../media/mtp-eval-38.png)

9. <span data-ttu-id="a7f5b-154">Sélectionnez ensuite la stratégie **anti-programme malveillant** , sélectionnez la valeur par défaut, puis cliquez sur l’icône représentant un crayon.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-154">Next select the **Anti-malware** policy, select the default, and choose the pencil icon.</span></span>

10. <span data-ttu-id="a7f5b-155">Cliquez sur **paramètres** , puis sélectionnez **Oui et utilisez le texte de notification par défaut** pour activer la **réponse de détection de programmes malveillants**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-155">Click **Settings** and select **Yes and use the default notification text** to enable **Malware Detection Response**.</span></span> <span data-ttu-id="a7f5b-156">Activez le **filtre types de pièces jointes courantes** .</span><span class="sxs-lookup"><span data-stu-id="a7f5b-156">Turn the **Common Attachment Types Filter** on.</span></span> <span data-ttu-id="a7f5b-157">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-157">Click **Save**.</span></span>

    ![Image of_Office 365 page du centre de sécurité & conformité qui indique que la réponse de détection de programmes malveillants est activée avec notification par défaut et que le filtre de types de pièces jointes courantes est activé](../../media/mtp-eval-39.png)
  
11. <span data-ttu-id="a7f5b-159">Accédez à [Office 365 Security & Compliance Center](https://protection.office.com/homepage)  >  **Search**  >  **audit log Search** and Turn Auditing on.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-159">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Search** > **Audit log search** and turn Auditing on.</span></span>

    ![Image of_Office 365 de la page Centre de sécurité & conformité, dans laquelle vous pouvez activer la recherche du journal d’audit](../../media/mtp-eval-40.png)

12. <span data-ttu-id="a7f5b-161">Intégrer la protection avancée contre les menaces Office 365 à Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-161">Integrate Office 365 ATP with Microsoft Defender ATP.</span></span> <span data-ttu-id="a7f5b-162">Accédez à [Office 365 Security & Compliance Center](https://protection.office.com/homepage)  >  **Threat management**  >  **Explorer Management Explorer** et sélectionnez **WDATP Settings** dans le coin supérieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-162">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Explorer** and select **WDATP Settings** on the upper right corner of the screen.</span></span> <span data-ttu-id="a7f5b-163">Dans la boîte de dialogue connexion Microsoft Defender ATP, activez **connexion à Windows ATP**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-163">In the Microsoft Defender ATP connection dialog box, turn on **Connect to Windows ATP**.</span></span>

    ![Image of_Office 365 page du centre de sécurité & conformité où vous pouvez activer la connexion ATP Windows Defender sur](../../media/mtp-eval-41.png)

## <a name="configure-azure-advanced-threat-protection"></a><span data-ttu-id="a7f5b-165">Configuration d’Azure protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a7f5b-165">Configure Azure Advanced Threat Protection</span></span>

>[!NOTE]
><span data-ttu-id="a7f5b-166">Ignorez cette étape si vous avez déjà activé Azure Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-166">Skip this step if you've already enabled Azure Advanced Threat Protection</span></span>

1. <span data-ttu-id="a7f5b-167">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info) > sélectionnez **plus de ressources**  >  **Azure Advanced Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-167">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > select **More Resources** > **Azure Advanced Threat Protection**.</span></span>

   ![Page du centre de sécurité image of_Microsoft 365 où il existe une option pour ouvrir Azure protection avancée contre les menaces](../../media/mtp-eval-42.png)

2. <span data-ttu-id="a7f5b-169">Cliquez sur **créer** pour démarrer l’Assistant protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-169">Click **Create** to start the Azure Advanced Threat Protection wizard.</span></span> 

   ![Image of_Azure page de l’Assistant protection avancée contre les menaces dans laquelle vous devez cliquer sur le bouton créer](../../media/mtp-eval-43.png)

3. <span data-ttu-id="a7f5b-171">Choisissez **fournir un nom d’utilisateur et un mot de passe pour vous connecter à votre forêt Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-171">Choose **Provide a username and password to connect to your Active Directory forest**.</span></span>  

   ![Page d’accueil image of_Azure Advanced Threat Protection](../../media/mtp-eval-44.png)

4. <span data-ttu-id="a7f5b-173">Entrez vos informations d’identification locales Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-173">Enter your Active Directory on-premises credentials.</span></span> <span data-ttu-id="a7f5b-174">Il peut s’agir de n’importe quel compte d’utilisateur qui dispose d’un accès en lecture à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-174">This can be any user account that has read access to Active Directory.</span></span>

   ![Image of_Azure page services d’annuaire de protection avancée contre les menaces dans laquelle vous devez placer vos informations d’identification](../../media/mtp-eval-45.png)

5. <span data-ttu-id="a7f5b-176">Ensuite, choisissez **Télécharger le programme d’installation du capteur** et transférer le fichier vers votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-176">Next, choose **Download Sensor Setup** and transfer file to your domain controller.</span></span>

   ![Image of_Azure page protection avancée contre les menaces dans laquelle vous pouvez sélectionner l’option Télécharger le capteur de téléchargement](../../media/mtp-eval-46.png)

6. <span data-ttu-id="a7f5b-178">Exécutez le programme d’installation du capteur ATP Azure et commencez à suivre l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-178">Execute the Azure ATP Sensor Setup and begin following the wizard.</span></span>

   ![Image of_Azure page protection avancée contre les menaces dans laquelle vous devez cliquer sur suivant pour suivre l’Assistant capteur ATP Azure](../../media/mtp-eval-47.png)
 
7. <span data-ttu-id="a7f5b-180">Cliquez sur **suivant** dans le type de déploiement du capteur.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-180">Click **Next** at the sensor deployment type.</span></span>

   ![Image of_Azure page protection avancée contre les menaces, dans laquelle vous devez cliquer sur suivant pour accéder à la page suivante](../../media/mtp-eval-48.png)
 
8. <span data-ttu-id="a7f5b-182">Copiez la clé d’accès, car vous devez l’entrer ensuite dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-182">Copy the access key because you need to enter it next in the Wizard.</span></span>

   ![Page capteurs d’image of_the où vous devez copier la clé d’accès que vous devez entrer dans la page suivante de l’Assistant Configuration du capteur ATP Azure](../../media/mtp-eval-49.png)
 
9. <span data-ttu-id="a7f5b-184">Copiez la clé d’accès dans l’Assistant, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-184">Copy the access key into the Wizard and click **Install**.</span></span> 

   ![Image of_Azure page de l’Assistant capteur Azure ATP protection avancée contre les menaces, dans laquelle vous devez fournir la clé d’accès, puis cliquez sur le bouton installer](../../media/mtp-eval-50.png)

10. <span data-ttu-id="a7f5b-186">Félicitations, vous avez réussi à configurer Azure Advanced Threat Protection sur votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-186">Congratulations, you've successfully configured Azure Advanced Threat Protection on your domain controller.</span></span>

    ![Image of_Azure l’installation de l’Assistant capteur Azure ATP de protection avancée contre les menaces à partir de laquelle vous devez cliquer sur le bouton Terminer](../../media/mtp-eval-51.png)
 
11. <span data-ttu-id="a7f5b-188">Sous la section paramètres [Azure Azure ATP](https://go.microsoft.com/fwlink/?linkid=2040449) , sélectionnez **Windows Defender ATP**, puis activez le bouton bascule.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-188">Under the [Azure Azure ATP](https://go.microsoft.com/fwlink/?linkid=2040449) settings section, select **Windows Defender ATP**, then turn on the toggle.</span></span> <span data-ttu-id="a7f5b-189">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-189">Click **Save**.</span></span> 

    ![Image of_the page des paramètres Azure Azure ATP, dans laquelle vous devez activer le bouton bascule Windows Defender ATP activé](../../media/mtp-eval-52.png)

>[!NOTE]
><span data-ttu-id="a7f5b-191">Windows Defender ATP a été rebaptisé en tant que Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-191">Windows Defender ATP has been rebranded as Microsoft Defender ATP.</span></span> <span data-ttu-id="a7f5b-192">Les modifications apportées à la personnalisation de tous nos portails sont déployées pour la cohérence.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-192">Rebranding changes across all of our portals are being rolled out the for consistency.</span></span>


## <a name="configure-microsoft-cloud-app-security"></a><span data-ttu-id="a7f5b-193">Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7f5b-193">Configure Microsoft Cloud App Security</span></span>

>[!NOTE]
><span data-ttu-id="a7f5b-194">Ignorez cette étape si vous avez déjà activé Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-194">Skip this step if you've already enabled Microsoft Cloud App Security.</span></span> 

1. <span data-ttu-id="a7f5b-195">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info)  >  **More Resources**  >  **Microsoft Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-195">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Cloud App Security**.</span></span>

   ![Page of_Microsoft 365 du centre de sécurité sur lequel vous pouvez voir la carte d’application Cloud de Microsoft et qui doit cliquer sur le bouton ouvrir](../../media/mtp-eval-53.png)

2. <span data-ttu-id="a7f5b-197">À l’invite d’informations pour intégrer Azure ATP, sélectionnez **activer l’intégration de données Azure ATP**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-197">At the information prompt to integrate Azure ATP, select **Enable Azure ATP data integration**.</span></span>
  
   ![Image of_the informations vous invitant à intégrer Azure ATP où vous devez sélectionner le lien activer l’intégration de données DAV Azure](../../media/mtp-eval-54.png)

   > [!NOTE]
   > <span data-ttu-id="a7f5b-199">Si vous ne voyez pas cette invite, cela signifie que votre intégration de données ATP Azure a déjà été activée.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-199">If you don’t see this prompt, it might mean that your Azure ATP data integration has already been enabled.</span></span> <span data-ttu-id="a7f5b-200">Toutefois, si vous n’êtes pas sûr, contactez votre administrateur informatique pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-200">However, if you are not sure, contact your IT Administrator to confirm.</span></span> 

3. <span data-ttu-id="a7f5b-201">Accédez à **paramètres**, activez le bouton d' **intégration Azure ATP** , puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-201">Go to **Settings**, turn on the **Azure ATP integration** toggle, then click **Save**.</span></span> 

   ![Page Paramètres de of_the des images où vous devez activer le bouton d’intégration Azure ATP, puis cliquer sur Enregistrer](../../media/mtp-eval-55.png)
   
   > [!NOTE]
   > <span data-ttu-id="a7f5b-203">Pour les nouvelles instances Azure ATP, ce bouton d’intégration est activé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-203">For new Azure ATP instances, this integration toggle is automatically turned on.</span></span> <span data-ttu-id="a7f5b-204">Vérifiez que votre intégration Azure ATP a été activée avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-204">Confirm that your Azure ATP integration has been enabled before you proceed to the next step.</span></span>
 
4. <span data-ttu-id="a7f5b-205">Sous paramètres de découverte du Cloud, sélectionnez **intégration de Microsoft Defender ATP**, puis activez l’intégration.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-205">Under the Cloud discovery settings, select **Microsoft Defender ATP integration**, then enable the integration.</span></span> <span data-ttu-id="a7f5b-206">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-206">Click **Save**.</span></span>

   ![Image of_the page Microsoft Defender ATP disponible où la case à cocher bloquer les applications non sanctionnées sous intégration de Microsoft Defender ATP est sélectionnée.](../../media/mtp-eval-56.png)

5. <span data-ttu-id="a7f5b-209">Sous paramètres de détection sur le Cloud, sélectionnez enrichissement par l' **utilisateur**, puis activez l’intégration à Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-209">Under Cloud discovery settings, select **User enrichment**, then enable the integration with Azure Active Directory.</span></span>

   ![Image de la section enrichissement par l’utilisateur dans laquelle la case à cocher enrichir les identificateurs utilisateur enrichis avec des noms d’utilisateur Azure Active Directory est activée](../../media/mtp-eval-57.png)


## <a name="configure-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="a7f5b-211">Configurer Microsoft Defender-protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a7f5b-211">Configure Microsoft Defender Advanced Threat Protection</span></span>

>[!NOTE]
><span data-ttu-id="a7f5b-212">Ignorez cette étape si vous avez déjà activé la protection avancée contre les menaces Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-212">Skip this step if you've already enabled Microsoft Defender Advanced Threat Protection.</span></span>

1. <span data-ttu-id="a7f5b-213">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info)  >  **plus de ressources**  >  **Microsoft Defender Security Center**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-213">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Defender Security Center**.</span></span> <span data-ttu-id="a7f5b-214">Cliquez sur **Ouvrir**. </span><span class="sxs-lookup"><span data-stu-id="a7f5b-214">Click **Open**.</span></span>

   ![Option du centre de sécurité de l’image of_Microsoft Defender dans la page Centre de sécurité Microsoft 365](../../media/mtp-eval-58.png)
 
2. <span data-ttu-id="a7f5b-216">Suivez l’Assistant protection avancée contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-216">Follow the Microsoft Defender Advanced Threat Protection wizard.</span></span> <span data-ttu-id="a7f5b-217">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-217">Click **Next**.</span></span> 

   ![Image of_the page d’accueil de l’Assistant Centre de sécurité Microsoft Defender](../../media/mtp-eval-59.png)

3. <span data-ttu-id="a7f5b-219">Choisissez en fonction de votre emplacement de stockage de données par défaut, de la stratégie de rétention des données, de la taille de l’organisation et du opt-in pour les fonctionnalités d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-219">Choose based on your preferred data storage location, data retention policy, organization size, and opt-in for preview features.</span></span>

   ![Image of_the page permettant de sélectionner votre pays de stockage des données, la stratégie de rétention et la taille de l’organisation.](../../media/mtp-eval-60.png)
   
   > [!NOTE]
   > <span data-ttu-id="a7f5b-222">Vous ne pouvez pas modifier par la suite certains paramètres, comme l’emplacement de stockage des données.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-222">You cannot change some of the settings, like data storage location, afterwards.</span></span> 

   <span data-ttu-id="a7f5b-223">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-223">Click **Next**.</span></span> 

4. <span data-ttu-id="a7f5b-224">Cliquez sur **Continuer** pour mettre en service votre locataire Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-224">Click **Continue** and it will provision your Microsoft Defender ATP tenant.</span></span>

   ![Image of_the page vous invitant à cliquer sur le bouton continuer pour créer votre instance Cloud](../../media/mtp-eval-61.png)

5. <span data-ttu-id="a7f5b-226">Intégrez vos points de terminaison via les stratégies de groupe, le gestionnaire de points de terminaison Microsoft ou en exécutant un script local vers Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-226">Onboard your endpoints through Group Policies, Microsoft Endpoint Manager or by running a local script to Microsoft Defender ATP.</span></span> <span data-ttu-id="a7f5b-227">Par souci de simplicité, ce guide utilise le script local.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-227">For simplicity, this guide uses the local script.</span></span>

6. <span data-ttu-id="a7f5b-228">Cliquez sur **Télécharger le package** et copiez le script d’intégration à vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-228">Click **Download package** and copy the onboarding script to your endpoint(s).</span></span>

   ![Image of_page invite à cliquer sur le bouton Télécharger le package pour copier le script d’intégration à votre point de terminaison ou aux points de terminaison](../../media/mtp-eval-62.png)

7. <span data-ttu-id="a7f5b-230">Sur votre point de terminaison, exécutez le script d’intégration en tant qu’administrateur et choisissez Y.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-230">On your endpoint, run the onboarding script as Administrator and choose Y.</span></span> 

   ![Image of_the CommandLine où vous exécutez le script d’intégration et choisissez Y pour continuer](../../media/mtp-eval-63.png)

8. <span data-ttu-id="a7f5b-232">Félicitations, vous avez intégré votre premier point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-232">Congratulations, you've onboarded your first endpoint.</span></span>

   ![Image of_the CommandLine où vous recevez la confirmation que vous avez intégrée votre premier point de terminaison.](../../media/mtp-eval-64.png)

9. <span data-ttu-id="a7f5b-235">Copiez-collez le test de détection à partir de l’Assistant Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-235">Copy-paste the detection test from the Microsoft Defender ATP wizard.</span></span>

   ![Image of_the exécutez une étape de test de détection à partir de laquelle vous devez cliquer sur copier pour copier le script de test de détection que vous devez coller dans l’invite de commandes.](../../media/mtp-eval-65.png)

10. <span data-ttu-id="a7f5b-237">Copiez le script PowerShell vers une invite de commandes avec élévation de privilèges et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-237">Copy the PowerShell script to an elevated command prompt and run it.</span></span> 

    ![Image of_command invite où vous devez copier le script PowerShell vers une invite de commandes avec élévation de privilèges et l’exécuter](../../media/mtp-eval-66.png)

11. <span data-ttu-id="a7f5b-239">Sélectionnez **commencer à utiliser Microsoft Defender ATP** à partir de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-239">Select **Start using Microsoft Defender ATP** from the Wizard.</span></span>

    ![Image of_the invite de confirmation à partir de l’Assistant où vous devez cliquer sur Démarrer à l’aide de Microsoft Defender ATP](../../media/mtp-eval-67.png)
 
12. <span data-ttu-id="a7f5b-241">Visitez le [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/).</span><span class="sxs-lookup"><span data-stu-id="a7f5b-241">Visit the [Microsoft Defender Security Center](https://securitycenter.windows.com/).</span></span> <span data-ttu-id="a7f5b-242">Accédez à **paramètres** , puis sélectionnez **fonctionnalités avancées**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-242">Go to **Settings** and then select **Advanced features**.</span></span> 

    ![Menu des paramètres du centre de sécurité de l’image of_Microsoft Defender dans lequel vous devez sélectionner les fonctionnalités avancées](../../media/mtp-eval-68.png)

13. <span data-ttu-id="a7f5b-244">Activer l’intégration avec **Azure Advanced Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-244">Turn on the integration with **Azure Advanced Threat Protection**.</span></span>  

    ![Options avancées du centre de sécurité d’image of_Microsoft Defender, option de protection avancée contre les menaces](../../media/mtp-eval-69.png)

14. <span data-ttu-id="a7f5b-246">Activer l’intégration avec **Office 365 Threat Intelligence**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-246">Turn on the integration with **Office 365 Threat Intelligence**.</span></span>

    ![Image of_Microsoft Defender Security Center Advanced Features, Office 365 Threat Intelligence option permettez à activer](../../media/mtp-eval-70.png)

15. <span data-ttu-id="a7f5b-248">Activez l’intégration à la **sécurité des applications Cloud de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-248">Turn on integration with **Microsoft Cloud App Security**.</span></span>

    ![Image of_Microsoft Defender Security Center Advanced Features, option de sécurité de l’application Cloud Microsoft activer/désactiver](../../media/mtp-eval-71.png)

16. <span data-ttu-id="a7f5b-250">Faites défiler la liste vers le bas et cliquez sur **enregistrer les préférences** pour confirmer les nouvelles intégrations.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-250">Scroll down and click **Save preferences** to confirm the new integrations.</span></span>

    ![Image of_Save bouton préférences que vous devez cliquer](../../media/mtp-eval-72.png)

## <a name="start-the-microsoft-threat-protection-service"></a><span data-ttu-id="a7f5b-252">Démarrer le service de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7f5b-252">Start the Microsoft Threat Protection service</span></span>

>[!NOTE]
><span data-ttu-id="a7f5b-253">À partir du 1er juin 2020, Microsoft active automatiquement les fonctionnalités de protection contre les menaces Microsoft pour tous les clients éligibles.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-253">Starting June 1, 2020, Microsoft automatically enables Microsoft Threat Protection features for all eligible tenants.</span></span> <span data-ttu-id="a7f5b-254">Pour plus d’informations, consultez cet [article de la communauté Microsoft Tech sur l’éligibilité des licences](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/microsoft-threat-protection-will-automatically-turn-on-for/ba-p/1345426) .</span><span class="sxs-lookup"><span data-stu-id="a7f5b-254">See this [Microsoft Tech Community article on license eligibility](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/microsoft-threat-protection-will-automatically-turn-on-for/ba-p/1345426) for details.</span></span> 


<span data-ttu-id="a7f5b-255">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/homepage).</span><span class="sxs-lookup"><span data-stu-id="a7f5b-255">Go to [Microsoft 365 Security Center](https://security.microsoft.com/homepage).</span></span> <span data-ttu-id="a7f5b-256">Accédez à **paramètres** , puis sélectionnez **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-256">Navigate to **Settings** and then select **Microsoft Threat Protection**.</span></span>

![<span data-ttu-id="a7f5b-257">Capture d’écran des options d’image of_Microsoft protection contre les menaces à partir de la page Paramètres du centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a7f5b-257">Image of_Microsoft Threat Protection option screenshot from the Microsoft 365 Security Center Settings page</span></span> ](../../media/mtp-eval-72b.png) <br>

<span data-ttu-id="a7f5b-258">Pour obtenir des instructions plus détaillées, consultez la rubrique [activer la protection contre les menaces Microsoft](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5b-258">For a more comprehensive guidance, see [Turn on Microsoft Threat Protection](mtp-enable.md).</span></span> 

<span data-ttu-id="a7f5b-259">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="a7f5b-259">Congratulations!</span></span> <span data-ttu-id="a7f5b-260">Vous venez de créer votre laboratoire d’évaluation ou votre environnement pilote Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-260">You've just created your Microsoft Threat Protection trial lab or pilot environment!</span></span> <span data-ttu-id="a7f5b-261">Vous pouvez désormais vous familiariser avec l’interface utilisateur de la protection contre les menaces Microsoft !</span><span class="sxs-lookup"><span data-stu-id="a7f5b-261">Now you can familiarize yourself with the Microsoft Threat Protection user interface!</span></span> <span data-ttu-id="a7f5b-262">Consultez ce que vous pouvez apprendre à partir du guide interactif de Microsoft Threat Protection suivant et apprenez à utiliser chaque tableau de bord pour vos tâches de sécurité quotidiennes.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-262">See what you can learn from the following Microsoft Threat Protection interactive guide and know how to use each dashboard for your day-to-day security operation tasks.</span></span>


>[!VIDEO https://aka.ms/MTP-Interactive-Guide]

<span data-ttu-id="a7f5b-263">Ensuite, vous pouvez simuler une attaque et voir comment les fonctionnalités du produit croisé détectent, créer des alertes et répondre automatiquement à une attaque en mode fichier sur un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-263">Next, you can simulate an attack and see how the cross product capabilities detect, create alerts, and automatically respond to a fileless attack on an endpoint.</span></span>

## <a name="next-step"></a><span data-ttu-id="a7f5b-264">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a7f5b-264">Next step</span></span>
|<span data-ttu-id="a7f5b-265">![Phase de simulation d’attaque](../../media/mtp/run-sim.png)</span><span class="sxs-lookup"><span data-stu-id="a7f5b-265">![Attack simulation phase](../../media/mtp/run-sim.png)</span></span> <br>[<span data-ttu-id="a7f5b-266">Phase de simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="a7f5b-266">Attack simulation phase</span></span>](mtp-pilot-simulate.md) | <span data-ttu-id="a7f5b-267">Exécutez la simulation d’attaque pour votre environnement pilote Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="a7f5b-267">Run the attack simulation for your Microsoft Threat Protection pilot environment.</span></span>
|:-------|:-----|
