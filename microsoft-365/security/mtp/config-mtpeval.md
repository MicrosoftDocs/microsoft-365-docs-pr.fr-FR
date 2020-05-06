---
title: Configurer les piliers de protection contre les menaces Microsoft pour l’environnement de laboratoire d’évaluation
description: Configurer Microsoft Threat Protection piliers, Office 365 ATP, Azure ATP, Microsoft Cloud App Security et Microsoft Defender ATP pour votre environnement de laboratoire d’évaluation
keywords: configurer la version d’évaluation de la protection de Microsoft contre les menaces, configuration de la version d’évaluation de Microsoft Threat Protection, configurer les piliers de protection de Microsoft contre les menaces
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 68d8f06803d75c3f89cae6fa7998734fd54084ca
ms.sourcegitcommit: 5476c2578400894640ae74bfe8e93c3319f685bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44049508"
---
# <a name="configure-microsoft-threat-protection-pillars-for-your-trial-lab-environment"></a><span data-ttu-id="b9bf3-104">Configurer les piliers de protection contre les menaces Microsoft pour votre environnement de laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="b9bf3-104">Configure Microsoft Threat Protection pillars for your trial lab environment</span></span>

<span data-ttu-id="b9bf3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b9bf3-105">**Applies to:**</span></span>
- <span data-ttu-id="b9bf3-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b9bf3-106">Microsoft Threat Protection</span></span>


<span data-ttu-id="b9bf3-107">La création d’un environnement de laboratoire de test Microsoft Threat Protection et son déploiement est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="b9bf3-107">Creating a Microsoft Threat Protection trial lab environment and deploying it is a three-phase process:</span></span>

<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" >
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval?view=o365-worldwide"> 
        <img src="../../media/prepare.png" alt="Prepare your Microsoft Threat Protection trial lab environment" title="Préparer votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="b9bf3-109">Phase 1 : préparer</a></span><span class="sxs-lookup"><span data-stu-id="b9bf3-109">Phase 1: Prepare </a></span></span><br>
    </td>
     <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/setup-mtpeval?view=o365-worldwide">
        <img src="../../media/setup.png" alt="Set up your Microsoft Threat Protection trial lab environment" title="Configurer votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="b9bf3-111">Phase 2 : configuration</a></span><span class="sxs-lookup"><span data-stu-id="b9bf3-111">Phase 2: Setup </a></span></span><br>
    </td>
    <td align="center" bgcolor="#d5f5e3">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/config-mtpeval?view=o365-worldwide">
        <img src="../../media/config-onboard.png" alt="Configure & Onboard" title="Configurer chaque pilier de protection contre les menaces Microsoft pour votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft et les points de terminaison intégrés" />
      <br/><span data-ttu-id="b9bf3-113">Phase 3 : configurer & Onboard</a></span><span class="sxs-lookup"><span data-stu-id="b9bf3-113">Phase 3: Configure & Onboard </a></span></span><br>
</td>


  </tr>
</table>

<span data-ttu-id="b9bf3-114">Vous êtes actuellement en phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-114">You are currently in the configuration phase.</span></span>


<span data-ttu-id="b9bf3-115">La préparation est essentielle à tout déploiement réussi.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-115">Preparation is key to any successful deployment.</span></span> <span data-ttu-id="b9bf3-116">Dans cet article, vous serez guidé sur les points que vous devrez prendre en compte lors de la préparation du déploiement de Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-116">In this article, you'll be guided on the points you'll need to consider as you prepare to deploy Microsoft Defender ATP.</span></span>


## <a name="microsoft-threat-protection-pillars"></a><span data-ttu-id="b9bf3-117">Pilier de la protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b9bf3-117">Microsoft Threat Protection pillars</span></span>
<span data-ttu-id="b9bf3-118">La protection contre les menaces Microsoft se compose de quatre piliers.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-118">Microsoft Threat Protection consists of four pillars.</span></span> <span data-ttu-id="b9bf3-119">Bien qu’un seul pilier puisse déjà fournir de la valeur à la sécurité de votre organisation réseau, l’activation des quatre piliers de protection de Microsoft contre les menaces permettra à votre organisation de bénéficier de la plus grande valeur.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-119">Although one pillar can already provide value to your network organization's security, enabling the four Microsoft Threat Protection pillars will give your organization the most value.</span></span>

![Image of_page](../../media/mtp-eval-31.png) <br>

<span data-ttu-id="b9bf3-121">Cette section vous guidera dans la configuration des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b9bf3-121">This section will guide you to configure:</span></span>
-   <span data-ttu-id="b9bf3-122">Office 365-Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b9bf3-122">Office 365 Advanced Threat Protection</span></span>
-   <span data-ttu-id="b9bf3-123">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b9bf3-123">Azure Advanced Threat Protection</span></span> 
-   <span data-ttu-id="b9bf3-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9bf3-124">Microsoft Cloud App Security</span></span>
-   <span data-ttu-id="b9bf3-125">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b9bf3-125">Microsoft Defender Advanced Threat Protection</span></span>


## <a name="configure-office-365-advanced-threat-protection"></a><span data-ttu-id="b9bf3-126">Configurer la protection avancée contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="b9bf3-126">Configure Office 365 Advanced Threat Protection</span></span>
>[!NOTE]
><span data-ttu-id="b9bf3-127">Ignorez cette étape si vous avez déjà activé la protection avancée contre les menaces d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-127">Skip this step if you have already enabled Office 365 Advanced Threat Protection.</span></span> 

<span data-ttu-id="b9bf3-128">Il existe un module PowerShell appelé *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* qui permet de déterminer certains de ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-128">There is a PowerShell Module called the *Office 365 Advanced Threat Protection Recommended Configuration Analyzer (ORCA)* that helps determine some of these settings.</span></span> <span data-ttu-id="b9bf3-129">Lorsqu’il est exécuté en tant qu’administrateur dans votre client, Get-ORCAReport permet de générer une évaluation du blocage du courrier indésirable, des hameçons et d’autres paramètres d’hygiène des messages.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-129">When run as an administrator in your tenant, get-ORCAReport will help generate an assessment of the anti-spam, anti-phish, and other message hygiene settings.</span></span> <span data-ttu-id="b9bf3-130">Vous pouvez télécharger ce module à https://www.powershellgallery.com/packages/ORCA/partir de.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-130">You can download this module from https://www.powershellgallery.com/packages/ORCA/.</span></span> 

1. <span data-ttu-id="b9bf3-131">Accédez à la**stratégie**de**gestion** > des menaces du centre > de [sécurité & conformité Office 365](https://protection.office.com/homepage).</span><span class="sxs-lookup"><span data-stu-id="b9bf3-131">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Policy**.</span></span>
<span data-ttu-id="b9bf3-132">![Image of_page](../../media/mtp-eval-32.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-132">![Image of_page](../../media/mtp-eval-32.png)</span></span> <br>
 
2. <span data-ttu-id="b9bf3-133">Cliquez sur **protection contre le hameçonnage ATP**, sélectionnez **créer** et renseignez le nom et la description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-133">Click **ATP anti-phishing**, select **Create** and fill in the policy name and description.</span></span> <span data-ttu-id="b9bf3-134">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-134">Click **Next**.</span></span>
<span data-ttu-id="b9bf3-135">![Image of_page](../../media/mtp-eval-33.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-135">![Image of_page](../../media/mtp-eval-33.png)</span></span> <br>

>[!NOTE]
><span data-ttu-id="b9bf3-136">Modifiez votre stratégie anti-hameçonnage avancée ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-136">Edit your Advanced ATP anti-phishing policy.</span></span> <span data-ttu-id="b9bf3-137">Remplacez le **seuil d’hameçonnage avancé** par **2**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-137">Change **Advanced Phishing Threshold** to **2 - Aggressive**.</span></span>
<br>

3. <span data-ttu-id="b9bf3-138">Cliquez sur le menu déroulant **Ajouter une condition** , puis sélectionnez vos domaines en tant que domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-138">Click the **Add a condition** drop-down menu and select your domain(s) as recipient domain.</span></span> <span data-ttu-id="b9bf3-139">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-139">Click **Next**.</span></span>
<span data-ttu-id="b9bf3-140">![Image of_page](../../media/mtp-eval-34.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-140">![Image of_page](../../media/mtp-eval-34.png)</span></span> <br>
 
4. <span data-ttu-id="b9bf3-141">Vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-141">Review your settings.</span></span> <span data-ttu-id="b9bf3-142">Cliquez sur **créer cette stratégie** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-142">Click **Create this policy** to confirm.</span></span> 
<span data-ttu-id="b9bf3-143">![Image of_page](../../media/mtp-eval-35.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-143">![Image of_page](../../media/mtp-eval-35.png)</span></span> <br>
 
5. <span data-ttu-id="b9bf3-144">Sélectionnez **pièces jointes fiables ATP** et sélectionnez l’option Activer la protection avancée contre les menaces **pour SharePoint, OneDrive et Microsoft teams** .</span><span class="sxs-lookup"><span data-stu-id="b9bf3-144">Select **ATP Safe attachments** and select the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** option.</span></span>  
<span data-ttu-id="b9bf3-145">![Image of_page](../../media/mtp-eval-36.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-145">![Image of_page](../../media/mtp-eval-36.png)</span></span> <br>

6. <span data-ttu-id="b9bf3-146">Cliquez sur l’icône + pour créer une stratégie de pièces jointes fiables, appliquez-la en tant que domaine de destinataire à vos domaines.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-146">Click the + icon to create a new safe attachment policy, apply it as recipient domain to your domains.</span></span> <span data-ttu-id="b9bf3-147">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-147">Click **Save**.</span></span>
<span data-ttu-id="b9bf3-148">![Image of_page](../../media/mtp-eval-37.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-148">![Image of_page](../../media/mtp-eval-37.png)</span></span> <br>
 
7. <span data-ttu-id="b9bf3-149">Ensuite, sélectionnez la stratégie de **liens approuvés ATP** , puis cliquez sur l’icône représentant un crayon pour modifier la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-149">Next, select the **ATP Safe Links** policy, then click the pencil icon to edit the default policy.</span></span>

8. <span data-ttu-id="b9bf3-150">Assurez-vous que l’option **ne pas suivre lorsque les utilisateurs cliquent sur les liens approuvés** n’est pas sélectionnée, tandis que les autres options sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-150">Make sure that the **Do not track when users click safe links** option is not selected, while the rest of the options are selected.</span></span> <span data-ttu-id="b9bf3-151">Pour plus d’informations, voir [paramètres de liens fiables](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp?view=o365-worldwide) .</span><span class="sxs-lookup"><span data-stu-id="b9bf3-151">See [Safe Links settings](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp?view=o365-worldwide) for details.</span></span> <span data-ttu-id="b9bf3-152">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-152">Click **Save**.</span></span> 
<span data-ttu-id="b9bf3-153">![Image of_page](../../media/mtp-eval-38.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-153">![Image of_page](../../media/mtp-eval-38.png)</span></span> <br>

9. <span data-ttu-id="b9bf3-154">Sélectionnez ensuite la stratégie **anti-programme malveillant** , sélectionnez la valeur par défaut, puis cliquez sur l’icône représentant un crayon.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-154">Next select the **Anti-malware** policy, select the default, and choose the pencil icon.</span></span>

10. <span data-ttu-id="b9bf3-155">Cliquez sur **paramètres** , puis sélectionnez **Oui et utilisez le texte de notification par défaut** pour activer la **réponse de détection de programmes malveillants**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-155">Click **Settings** and select **Yes and use the default notification text** to enable **Malware Detection Response**.</span></span> <span data-ttu-id="b9bf3-156">Activez le **filtre types de pièces jointes courantes** .</span><span class="sxs-lookup"><span data-stu-id="b9bf3-156">Turn the **Common Attachment Types Filter** on.</span></span> <span data-ttu-id="b9bf3-157">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-157">Click **Save**.</span></span>
<br><span data-ttu-id="b9bf3-158">![Image of_page](../../media/mtp-eval-39.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-158">![Image of_page](../../media/mtp-eval-39.png)</span></span> <br>
  
11. <span data-ttu-id="b9bf3-159">Accédez à [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Search** > Search**audit log Search** and Turn Auditing on.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-159">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Search** > **Audit log search** and turn Auditing on.</span></span>  
<span data-ttu-id="b9bf3-160">![Image of_page](../../media/mtp-eval-40.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-160">![Image of_page](../../media/mtp-eval-40.png)</span></span> <br>

12. <span data-ttu-id="b9bf3-161">Intégrer la protection avancée contre les menaces Office 365 à Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-161">Integrate Office 365 ATP with Microsoft Defender ATP.</span></span> <span data-ttu-id="b9bf3-162">Accédez à [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > Explorer**Management** > **Explorer** et sélectionnez **WDATP Settings** dans le coin supérieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-162">Navigate to [Office 365 Security & Compliance Center](https://protection.office.com/homepage) > **Threat management** > **Explorer** and select **WDATP Settings** on the upper right corner of the screen.</span></span> <span data-ttu-id="b9bf3-163">Dans la boîte de dialogue connexion Microsoft Defender ATP, activez **connexion à Windows ATP**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-163">In the Microsoft Defender ATP connection dialog box, turn on **Connect to Windows ATP**.</span></span>
<span data-ttu-id="b9bf3-164">![Image of_page](../../media/mtp-eval-41.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-164">![Image of_page](../../media/mtp-eval-41.png)</span></span> <br>

## <a name="configure-azure-advanced-threat-protection"></a><span data-ttu-id="b9bf3-165">Configuration d’Azure protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b9bf3-165">Configure Azure Advanced Threat Protection</span></span>
>[!NOTE]
><span data-ttu-id="b9bf3-166">Ignorez cette étape si vous avez déjà activé Azure protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-166">Skip this step if you have already enabled Azure Advanced Threat Protection</span></span>


1. <span data-ttu-id="b9bf3-167">Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info) > sélectionnez **plus de ressources** > **Azure Advanced Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-167">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > select **More Resources** > **Azure Advanced Threat Protection**.</span></span>
<span data-ttu-id="b9bf3-168">![Image of_page](../../media/mtp-eval-42.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-168">![Image of_page](../../media/mtp-eval-42.png)</span></span> <br>

2. <span data-ttu-id="b9bf3-169">Cliquez sur **créer** pour démarrer l’Assistant protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-169">Click **Create** to start the Azure Advanced Threat Protection wizard.</span></span> 
<br><span data-ttu-id="b9bf3-170">![Image of_page](../../media/mtp-eval-43.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-170">![Image of_page](../../media/mtp-eval-43.png)</span></span> <br>

3. <span data-ttu-id="b9bf3-171">Choisissez **fournir un nom d’utilisateur et un mot de passe pour vous connecter à votre forêt Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-171">Choose **Provide a username and password to connect to your Active Directory forest**.</span></span>  
<span data-ttu-id="b9bf3-172">![Image of_page](../../media/mtp-eval-44.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-172">![Image of_page](../../media/mtp-eval-44.png)</span></span> <br>

4. <span data-ttu-id="b9bf3-173">Entrez vos informations d’identification locales Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-173">Enter your Active Directory on-premises credentials.</span></span> <span data-ttu-id="b9bf3-174">Il peut s’agir de n’importe quel compte d’utilisateur qui dispose d’un accès en lecture à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-174">This can be any user account that has read access to Active Directory.</span></span>
<span data-ttu-id="b9bf3-175">![Image of_page](../../media/mtp-eval-45.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-175">![Image of_page](../../media/mtp-eval-45.png)</span></span> <br>

5. <span data-ttu-id="b9bf3-176">Ensuite, choisissez **Télécharger le programme d’installation du capteur** et transférer le fichier vers votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-176">Next, choose **Download Sensor Setup** and transfer file to your domain controller.</span></span> 
<span data-ttu-id="b9bf3-177">![Image of_page](../../media/mtp-eval-46.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-177">![Image of_page](../../media/mtp-eval-46.png)</span></span> <br>

6. <span data-ttu-id="b9bf3-178">Exécutez le programme d’installation du capteur ATP Azure et commencez à suivre l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-178">Execute the Azure ATP Sensor Setup and begin following the wizard.</span></span>
<br><span data-ttu-id="b9bf3-179">![Image of_page](../../media/mtp-eval-47.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-179">![Image of_page](../../media/mtp-eval-47.png)</span></span> <br>
 
7. <span data-ttu-id="b9bf3-180">Cliquez sur **suivant** dans le type de déploiement du capteur.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-180">Click **Next** at the sensor deployment type.</span></span>
<br><span data-ttu-id="b9bf3-181">![Image of_page](../../media/mtp-eval-48.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-181">![Image of_page](../../media/mtp-eval-48.png)</span></span> <br>
 
8. <span data-ttu-id="b9bf3-182">Copiez la clé d’accès, puis entrez-la dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-182">Copy the access key as you will need to enter it next in the Wizard.</span></span>
<span data-ttu-id="b9bf3-183">![Image of_page](../../media/mtp-eval-49.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-183">![Image of_page](../../media/mtp-eval-49.png)</span></span> <br>
 
9. <span data-ttu-id="b9bf3-184">Copiez la clé d’accès dans l’Assistant, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-184">Copy the access key into the Wizard and click **Install**.</span></span> 
<br><span data-ttu-id="b9bf3-185">![Image of_page](../../media/mtp-eval-50.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-185">![Image of_page](../../media/mtp-eval-50.png)</span></span> <br>

10. <span data-ttu-id="b9bf3-186">Félicitations, vous avez réussi à configurer Azure Advanced Threat Protection sur votre contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-186">Congratulations, you have successfully configured Azure Advanced Threat Protection on your domain controller.</span></span>
<span data-ttu-id="b9bf3-187">![Image of_page](../../media/mtp-eval-51.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-187">![Image of_page](../../media/mtp-eval-51.png)</span></span> <br>
 
11. <span data-ttu-id="b9bf3-188">Sous la section paramètres [Azure Azure ATP](https://go.microsoft.com/fwlink/?linkid=2040449) , sélectionnez **Windows Defender ATP**, puis activez le bouton bascule.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-188">Under the [Azure Azure ATP](https://go.microsoft.com/fwlink/?linkid=2040449) settings section, select **Windows Defender ATP**, then turn the toggle on.</span></span> <span data-ttu-id="b9bf3-189">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-189">Click **Save**.</span></span> 
<span data-ttu-id="b9bf3-190">![Image of_page](../../media/mtp-eval-52.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-190">![Image of_page](../../media/mtp-eval-52.png)</span></span> <br>

>[!NOTE]
><span data-ttu-id="b9bf3-191">Windows Defender ATP a été rebaptisé en tant que Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-191">Windows Defender ATP has been rebranded as Microsoft Defender ATP.</span></span> <span data-ttu-id="b9bf3-192">Les modifications apportées à la personnalisation de tous nos portails sont déployées pour la cohérence.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-192">Rebranding changes across all of our portals are being rolled out the for consistency.</span></span>


## <a name="configure-microsoft-cloud-app-security"></a><span data-ttu-id="b9bf3-193">Configurer la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="b9bf3-193">Configure Microsoft Cloud App Security</span></span>
>[!NOTE]
><span data-ttu-id="b9bf3-194">Ignorez cette étape si vous avez déjà activé Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-194">Skip this step if you have already enabled Microsoft Cloud App Security.</span></span> 

1. <span data-ttu-id="b9bf3-195"> > Accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info)**More Resources** > **Microsoft Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-195">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Cloud App Security**.</span></span>
<span data-ttu-id="b9bf3-196">![Image of_page](../../media/mtp-eval-53.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-196">![Image of_page](../../media/mtp-eval-53.png)</span></span> <br>

2. <span data-ttu-id="b9bf3-197">À l’invite d’informations pour intégrer Azure ATP, sélectionnez **activer l’intégration de données Azure ATP**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-197">At the information prompt to integrate Azure ATP, select **Enable Azure ATP data integration**.</span></span> 
<br><span data-ttu-id="b9bf3-198">![Image of_page](../../media/mtp-eval-54.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-198">![Image of_page](../../media/mtp-eval-54.png)</span></span> <br>

>[!NOTE]
><span data-ttu-id="b9bf3-199">Si vous ne voyez pas cette invite, cela signifie que votre intégration de données ATP Azure a déjà été activée.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-199">If you don’t see this prompt, it might mean that your Azure ATP data integration has already been enabled.</span></span> <span data-ttu-id="b9bf3-200">Toutefois, si vous n’êtes pas sûr, contactez votre administrateur informatique pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-200">However, if you are not sure, contact your IT Administrator to confirm.</span></span> 

3. <span data-ttu-id="b9bf3-201">Accédez à **paramètres**, activez l’option **intégration Azure ATP** activée, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-201">Go to **Settings**, turn the **Azure ATP integration** toggle on, then click **Save**.</span></span> 
<span data-ttu-id="b9bf3-202">![Image of_page](../../media/mtp-eval-55.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-202">![Image of_page](../../media/mtp-eval-55.png)</span></span> <br>
>[!NOTE]
><span data-ttu-id="b9bf3-203">Pour les nouvelles instances Azure ATP, ce bouton d’intégration est activé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-203">For new Azure ATP instances, this integration toggle is automatically turned on.</span></span> <span data-ttu-id="b9bf3-204">Vérifiez que votre intégration Azure ATP a été activée avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-204">Confirm that your Azure ATP integration has been enabled before you proceed to the next step.</span></span>
 
4. <span data-ttu-id="b9bf3-205">Sous paramètres de découverte du Cloud, sélectionnez **intégration de Microsoft Defender ATP**, puis activez l’intégration.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-205">Under the Cloud discovery settings, select **Microsoft Defender ATP integration**, then enable the integration.</span></span> <span data-ttu-id="b9bf3-206">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-206">Click **Save**.</span></span>
<span data-ttu-id="b9bf3-207">![Image of_page](../../media/mtp-eval-56.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-207">![Image of_page](../../media/mtp-eval-56.png)</span></span> <br>

5. <span data-ttu-id="b9bf3-208">Sous paramètres de détection sur le Cloud, sélectionnez enrichissement par l' **utilisateur**, puis activez l’intégration à Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-208">Under Cloud discovery settings, select **User enrichment**, then enable the integration with Azure Active Directory.</span></span>
<span data-ttu-id="b9bf3-209">![Image of_page](../../media/mtp-eval-57.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-209">![Image of_page](../../media/mtp-eval-57.png)</span></span> <br>

## <a name="configure-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="b9bf3-210">Configurer Microsoft Defender-protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b9bf3-210">Configure Microsoft Defender Advanced Threat Protection</span></span>
>[!NOTE]
><span data-ttu-id="b9bf3-211">Ignorez cette étape si vous avez déjà activé la protection avancée contre les menaces Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-211">Skip this step if you have already enabled Microsoft Defender Advanced Threat Protection.</span></span>

1. <span data-ttu-id="b9bf3-212">Accédez > au [Centre de sécurité Microsoft 365](https://security.microsoft.com/info)**plus de ressources** > **Microsoft Defender Security Center**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-212">Navigate to [Microsoft 365 Security Center](https://security.microsoft.com/info) > **More Resources** > **Microsoft Defender Security Center**.</span></span> <span data-ttu-id="b9bf3-213">Cliquez sur **Ouvrir**. </span><span class="sxs-lookup"><span data-stu-id="b9bf3-213">Click **Open**.</span></span>
<br><span data-ttu-id="b9bf3-214">![Image of_page](../../media/mtp-eval-58.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-214">![Image of_page](../../media/mtp-eval-58.png)</span></span> <br>
 
2. <span data-ttu-id="b9bf3-215">Suivez l’Assistant protection avancée contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-215">Follow the Microsoft Defender Advanced Threat Protection wizard.</span></span> <span data-ttu-id="b9bf3-216">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-216">Click **Next**.</span></span> 
<br><span data-ttu-id="b9bf3-217">![Image of_page](../../media/mtp-eval-59.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-217">![Image of_page](../../media/mtp-eval-59.png)</span></span> <br>

3. <span data-ttu-id="b9bf3-218">Choisissez en fonction de votre emplacement de stockage de données par défaut, de la stratégie de rétention des données, de la taille de l’organisation et du opt-in pour les fonctionnalités d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-218">Choose based on your preferred data storage location, data retention policy, organization size, and opt-in for preview features.</span></span> 
<br><span data-ttu-id="b9bf3-219">![Image of_page](../../media/mtp-eval-60.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-219">![Image of_page](../../media/mtp-eval-60.png)</span></span> <br>
>[!NOTE]
><span data-ttu-id="b9bf3-220">Vous ne pouvez pas modifier par la suite certains paramètres, comme l’emplacement de stockage des données.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-220">You cannot change some of the settings, like data storage location, afterwards.</span></span> 
<br>

<span data-ttu-id="b9bf3-221">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-221">Click **Next**.</span></span> 

4. <span data-ttu-id="b9bf3-222">Cliquez sur **Continuer** pour mettre en service votre locataire Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-222">Click **Continue** and it will provision your Microsoft Defender ATP tenant.</span></span>
<br><span data-ttu-id="b9bf3-223">![Image of_page](../../media/mtp-eval-61.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-223">![Image of_page](../../media/mtp-eval-61.png)</span></span> <br>

5. <span data-ttu-id="b9bf3-224">Intégrez vos points de terminaison via les stratégies de groupe, le gestionnaire de points de terminaison Microsoft ou en exécutant un script local vers Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-224">Onboard your endpoints through Group Policies, Microsoft Endpoint Manager or by running a local script to Microsoft Defender ATP.</span></span> <span data-ttu-id="b9bf3-225">Par souci de simplicité, ce guide utilise le script local.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-225">For simplicity, this guide uses the local script.</span></span>

6. <span data-ttu-id="b9bf3-226">Cliquez sur **Télécharger le package** et copiez le script d’intégration à vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-226">Click **Download package** and copy the onboarding script to your endpoint(s).</span></span>  
<br><span data-ttu-id="b9bf3-227">![Image of_page](../../media/mtp-eval-62.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-227">![Image of_page](../../media/mtp-eval-62.png)</span></span> <br>

7. <span data-ttu-id="b9bf3-228">Sur votre point de terminaison, exécutez le script d’intégration en tant qu’administrateur et choisissez Y.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-228">On your endpoint, run the onboarding script as Administrator and choose Y.</span></span>
<br><span data-ttu-id="b9bf3-229">![Image of_page](../../media/mtp-eval-63.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-229">![Image of_page](../../media/mtp-eval-63.png)</span></span> <br>

8. <span data-ttu-id="b9bf3-230">Félicitations, vous avez intégré votre premier point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-230">Congratulations, you have onboarded your first endpoint.</span></span>  
<br>![Image of_page](../../media/mtp-eval-64.png) <br>

9. <span data-ttu-id="b9bf3-232">Copiez-collez le test de détection à partir de l’Assistant Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-232">Copy-paste the detection test from the Microsoft Defender ATP wizard.</span></span>
<br><span data-ttu-id="b9bf3-233">![Image of_page](../../media/mtp-eval-65.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-233">![Image of_page](../../media/mtp-eval-65.png)</span></span> <br>

10. <span data-ttu-id="b9bf3-234">Copiez le script PowerShell vers une invite de commandes avec élévation de privilèges et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-234">Copy the PowerShell script to an elevated command prompt and run it.</span></span> 
<br><span data-ttu-id="b9bf3-235">![Image of_page](../../media/mtp-eval-66.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-235">![Image of_page](../../media/mtp-eval-66.png)</span></span> <br>

11. <span data-ttu-id="b9bf3-236">Sélectionnez **commencer à utiliser Microsoft Defender ATP** à partir de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-236">Select **Start using Microsoft Defender ATP** from the Wizard.</span></span>
<br><span data-ttu-id="b9bf3-237">![Image of_page](../../media/mtp-eval-67.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-237">![Image of_page](../../media/mtp-eval-67.png)</span></span> <br>
 
12. <span data-ttu-id="b9bf3-238">Visitez le [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/).</span><span class="sxs-lookup"><span data-stu-id="b9bf3-238">Visit the [Microsoft Defender Security Center](https://securitycenter.windows.com/).</span></span> <span data-ttu-id="b9bf3-239">Accédez à **paramètres** , puis sélectionnez **fonctionnalités avancées**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-239">Go to **Settings** and then select **Advanced features**.</span></span> 
<br><span data-ttu-id="b9bf3-240">![Image of_page](../../media/mtp-eval-68.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-240">![Image of_page](../../media/mtp-eval-68.png)</span></span> <br>

13. <span data-ttu-id="b9bf3-241">Activer l’intégration avec **Azure Advanced Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-241">Turn on the integration with **Azure Advanced Threat Protection**.</span></span>  
<br><span data-ttu-id="b9bf3-242">![Image of_page](../../media/mtp-eval-69.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-242">![Image of_page](../../media/mtp-eval-69.png)</span></span> <br>

14. <span data-ttu-id="b9bf3-243">Activer l’intégration avec **Office 365 Threat Intelligence**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-243">Turn on the integration with **Office 365 Threat Intelligence**.</span></span>
<br><span data-ttu-id="b9bf3-244">![Image of_page](../../media/mtp-eval-70.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-244">![Image of_page](../../media/mtp-eval-70.png)</span></span> <br>

15. <span data-ttu-id="b9bf3-245">Activez l’intégration à la **sécurité des applications Cloud de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-245">Turn on integration with **Microsoft Cloud App Security**.</span></span>
<br><span data-ttu-id="b9bf3-246">![Image of_page](../../media/mtp-eval-71.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-246">![Image of_page](../../media/mtp-eval-71.png)</span></span> <br>

16. <span data-ttu-id="b9bf3-247">Faites défiler la liste vers le bas et cliquez sur **enregistrer les préférences** pour confirmer les nouvelles intégrations.</span><span class="sxs-lookup"><span data-stu-id="b9bf3-247">Scroll down and click **Save preferences** to confirm the new integrations.</span></span>
<br><span data-ttu-id="b9bf3-248">![Image of_page](../../media/mtp-eval-72.png)</span><span class="sxs-lookup"><span data-stu-id="b9bf3-248">![Image of_page](../../media/mtp-eval-72.png)</span></span> <br>

## <a name="next-steps"></a><span data-ttu-id="b9bf3-249">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b9bf3-249">Next steps</span></span>
<span data-ttu-id="b9bf3-250">[Activez Microsoft Threat Protection](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-enable?view=o365-worldwide#start-using-the-service) , puis [générez une alerte de test](generate-test-alert.md).</span><span class="sxs-lookup"><span data-stu-id="b9bf3-250">[Turn on Microsoft Threat Protection](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-enable?view=o365-worldwide#start-using-the-service) and then [generate a test alert](generate-test-alert.md).</span></span>
