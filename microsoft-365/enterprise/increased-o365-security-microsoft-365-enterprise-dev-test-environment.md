---
title: Sécurité Office 365 accrue pour votre environnement de test Microsoft 365 Entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/16/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce Guide de laboratoire de Test pour activer les paramètres de sécurité Office 365 supplémentaires à votre environnement de test Microsoft 365 pour entreprises.
ms.openlocfilehash: 62cf2347d3e003e9368c987912e7748029241501
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867106"
---
# <a name="increased-office-365-security-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="fd93f-103">Sécurité Office 365 accrue pour votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fd93f-103">Increased Office 365 security for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="fd93f-104">Les instructions de cet article, configurer les paramètres Office 365 supplémentaires pour renforcer la sécurité dans votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="fd93f-104">With the instructions in this article, you configure additional Office 365 settings to increase security in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="fd93f-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="fd93f-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="fd93f-107">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="fd93f-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="fd93f-108">Si vous souhaitez simplement configurer une meilleure sécurité Office 365 dans une solution légère avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="fd93f-108">If you just want to configure increased Office 365 security in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="fd93f-109">Si vous souhaitez configurer une meilleure sécurité Office 365 dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fd93f-109">If you want to configure increased Office 365 security in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="fd93f-p101">Test de renforcement de la sécurité Office 365 ne nécessite pas l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option afin que vous puissiez licences automatisé et l’appartenance au groupe de test et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="fd93f-p101">Testing increased Office 365 security does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 


## <a name="phase-2-configure-increased-office-365-security"></a><span data-ttu-id="fd93f-112">Phase 2 : Configurer une meilleure sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="fd93f-112">Phase 2: Configure increased Office 365 security</span></span>

<span data-ttu-id="fd93f-p102">Durant cette phase, vous activez une meilleure sécurité Office 365 pour votre environnement de test Microsoft 365 pour entreprises. Pour plus d’informations et les paramètres, consultez [configurer votre client Office 365 pour accroître la sécurité](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span><span class="sxs-lookup"><span data-stu-id="fd93f-p102">In this phase, you enable increased Office 365 security for your Microsoft 365 Enterprise test environment. For additional details and settings, see [Configure your Office 365 tenant for increased security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span></span>

### <a name="configure-sharepoint-online-to-block-apps-that-dont-support-modern-authentication"></a><span data-ttu-id="fd93f-115">Configurer SharePoint Online pour bloquer les applications qui ne prennent pas en charge l’authentification moderne</span><span class="sxs-lookup"><span data-stu-id="fd93f-115">Configure SharePoint Online to block apps that don’t support modern authentication</span></span>

<span data-ttu-id="fd93f-116">Les applications qui ne prennent pas en charge l’authentification moderne ne peut pas avoir d' [identité et périphérique d’accès aux configurations](microsoft-365-policies-configurations.md) appliquée, qui est un élément important de sécuriser votre abonnement Microsoft 365 et ses actifs numériques.</span><span class="sxs-lookup"><span data-stu-id="fd93f-116">Apps that do not support modern authentication cannot have [identity and device access configurations](microsoft-365-policies-configurations.md) applied to them, which is an important element of securing your Microsoft 365 subscription and its digital assets.</span></span> 

1. <span data-ttu-id="fd93f-117">Accédez au portail Office ([https://office.com](https://office.com)) et se connecter à votre abonnement d’évaluation d’Office 365 avec votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="fd93f-117">Go to the Office portal ([https://office.com](https://office.com)) and sign in to your Office 365 trial subscription with your global administrator account.</span></span>
    
  - <span data-ttu-id="fd93f-118">Si vous utilisez l’environnement de test Microsoft 365 léger, connectez-vous à partir de votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fd93f-118">If you are using the lightweight Microsoft 365 test environment, sign in from your local computer.</span></span>
    
  - <span data-ttu-id="fd93f-119">Si vous utilisez l’environnement de test simulé entreprise Microsoft 365, utilisez le [portail Azure](https://portal.azure.com) pour se connecter à l’ordinateur virtuel CLIENT1 et puis se connecter à partir de CLIENT1.</span><span class="sxs-lookup"><span data-stu-id="fd93f-119">If you are using the simulated enterprise Microsoft 365 test environment, use the [Azure portal](https://portal.azure.com) to connect to the CLIENT1 virtual machine, and then sign in from CLIENT1.</span></span>
 
2. <span data-ttu-id="fd93f-120">Sous l’onglet **Centre d’administration Microsoft 365** , cliquez sur **Admin**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-120">From the **Microsoft 365 admin center** tab, click **Admin**.</span></span>
3. <span data-ttu-id="fd93f-121">Dans l’onglet **Centre d’administration Microsoft 365** nouveau, cliquez sur **centres d’administration > SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-121">On the new **Microsoft 365 admin center** tab, click **Admin centers > SharePoint**.</span></span>
4. <span data-ttu-id="fd93f-122">Dans l’onglet nouveau **Centre d’administration SharePoint** , cliquez sur **le contrôle d’accès**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-122">On the new **SharePoint admin center** tab, click **Access control**.</span></span>
5. <span data-ttu-id="fd93f-123">Sous **applications qui ne prennent en charge l’authentification moderne**, cliquez sur **Bloquer**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-123">Under **Apps that don’t support modern authentication**, click **Block**, and then click **OK**.</span></span>


### <a name="enable-advanced-threat-protection-for-sharepoint-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="fd93f-124">Activer les avancées de protection contre les menaces) pour SharePoint, OneDrive entreprise et les équipes Microsoft</span><span class="sxs-lookup"><span data-stu-id="fd93f-124">Enable Advanced Threat Protection) for SharePoint, OneDrive for Business, and Microsoft Teams</span></span>

<span data-ttu-id="fd93f-p103">Office 365 Advanced Threat Protection (DAV) est une fonctionnalité d’Exchange Online Protection (EOP) qui permet de conserver des programmes malveillants en dehors de votre courrier électronique. Avec DAV, vous créez des stratégies dans le centre d’administration Exchange (CAE) ou de la sécurité & centre de conformité qui permettent de garantir vos utilisateurs accéder uniquement des liens ou des pièces jointes dans les messages électroniques qui sont identifiés comme non malveillant. Pour plus d’informations, voir [protection contre les menaces avancées pour les pièces jointes fiables et les liens sécurisés](https://docs.microsoft.com/office365/securitycompliance/office-365-atp).</span><span class="sxs-lookup"><span data-stu-id="fd93f-p103">Office 365 Advanced Threat Protection (ATP) is a feature of Exchange Online Protection (EOP) that helps keep malware out of your email. With ATP, you create policies in the Exchange Admin center (EAC) or the Security & Compliance center that help ensure your users access only links or attachments in emails that are identified as not malicious. For more information, see [Advanced threat protection for safe attachments and safe links](https://docs.microsoft.com/office365/securitycompliance/office-365-atp).</span></span>

1. <span data-ttu-id="fd93f-128">Dans l’onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **centres d’administration > sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-128">On the **Microsoft 365 admin center** tab of your browser, click **Admin centers > Security & Compliance**.</span></span>
2. <span data-ttu-id="fd93f-129">Dans l’onglet **sécurité et conformité** nouveau, cliquez sur **Gestion des menaces > stratégie**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-129">On the new **Security & Compliance** tab, click **Threat management > Policy**.</span></span>
3. <span data-ttu-id="fd93f-130">Cliquez sur **les pièces jointes fiables DAV**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-130">Click **ATP safe attachments**.</span></span>
4. <span data-ttu-id="fd93f-131">Dans le volet **pièces jointes fiables** , sélectionnez **Activer DAV pour SharePoint, OneDrive et les équipes Microsoft**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-131">In the **Safe attachments** pane, select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**, and then click **Save**.</span></span>

### <a name="enable-anti-malware"></a><span data-ttu-id="fd93f-132">Activer les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fd93f-132">Enable anti-malware</span></span>

<span data-ttu-id="fd93f-p104">Programme malveillant est composé des virus et logiciels espions. Virus infectent autres programmes et des données, et ils répandent dans votre ordinateur que vous recherchez des programmes d’infection. Logiciels espions fait référence aux logiciels malveillants qui rassemble vos informations personnelles, telles que des données personnelles et les informations de connexion et l’envoie à l’auteur de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="fd93f-p104">Malware is comprised of viruses and spyware. Viruses infect other programs and data, and they spread throughout your computer looking for programs to infect. Spyware refers to malware that gathers your personal information, such as sign-in information and personal data, and sends it back to the malware author.</span></span> 

<span data-ttu-id="fd93f-p105">Office 365 offre des programmes malveillants intégrée et les fonctionnalités qui permettent de protéger les messages entrants et sortants contre les logiciels malveillants et vous protéger contre le courrier indésirable de filtrage du courrier indésirable. Pour plus d’informations, consultez la rubrique [protection contre le courrier indésirable et anti-programme malveillant dans Office 365](https://docs.microsoft.com/office365/securitycompliance/anti-spam-and-anti-malware-protection)</span><span class="sxs-lookup"><span data-stu-id="fd93f-p105">Office 365 has built-in malware and spam filtering capabilities that help protect inbound and outbound messages from malicious software and help protect you from spam. For more information, see [Anti-spam & anti-malware protection in Office 365](https://docs.microsoft.com/office365/securitycompliance/anti-spam-and-anti-malware-protection)</span></span>

<span data-ttu-id="fd93f-138">Pour vous assurer que traitement anti-programme malveillant est en cours d’exécution sur les fichiers de types de fichiers courants :</span><span class="sxs-lookup"><span data-stu-id="fd93f-138">To ensure that anti-malware processing is being performed on files with common attachment file types:</span></span>

1. <span data-ttu-id="fd93f-139">Cliquez sur le bouton de retour de votre navigateur pour revenir à la page de **stratégie** .</span><span class="sxs-lookup"><span data-stu-id="fd93f-139">Click the back button on your browser to get back to the **Policy** page.</span></span>
2. <span data-ttu-id="fd93f-140">Cliquez sur **contre les programmes malveillants**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-140">Click **Anti-malware**.</span></span>
3. <span data-ttu-id="fd93f-141">Double-cliquez sur la stratégie **par défaut**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-141">Double-click the policy named **Default**.</span></span>
4. <span data-ttu-id="fd93f-142">Dans la fenêtre **stratégie anti-programme malveillant** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-142">In the **Anti-malware policy** window, click **Settings**.</span></span>
4. <span data-ttu-id="fd93f-143">Sous **filtre de pièce jointe courants**, cliquez sur **sur > Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-143">Under **Common Attachment Types filter**, click **On > Save**.</span></span>


## <a name="phase-3-examine-office-365-security-tools-and-logs"></a><span data-ttu-id="fd93f-144">Phase 3 : Examiner les journaux et les outils de sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="fd93f-144">Phase 3: Examine Office 365 security tools and logs</span></span>

<span data-ttu-id="fd93f-145">Durant cette phase, vous examinez les services intégrés qui vous informent sur les événements de sécurité et mesurent vos défenses globale.</span><span class="sxs-lookup"><span data-stu-id="fd93f-145">In this phase, you look at built-in services that inform you about security events and measure your overall security posture.</span></span>

### <a name="threat-management-dashboard"></a><span data-ttu-id="fd93f-146">Tableau de bord de gestion des menaces</span><span class="sxs-lookup"><span data-stu-id="fd93f-146">Threat management dashboard</span></span>

<span data-ttu-id="fd93f-p106">Gestion des menaces Office 365 peut vous aider à contrôler et gérer l’accès d’appareil mobile aux données de votre organisation, protéger votre organisation contre la perte de données et protéger les messages entrants et sortants à partir du courrier indésirable et les logiciels malveillants. Vous utilisez également threat management pour protéger la réputation de votre domaine et pour déterminer si les expéditeurs sont à des fins malveillantes usurpation de comptes à partir de votre domaine. Pour plus d’informations, voir [Gestion des menaces de la sécurité pour Microsoft Office 365 et le centre de conformité](https://docs.microsoft.com/office365/securitycompliance/threat-management).</span><span class="sxs-lookup"><span data-stu-id="fd93f-p106">Office 365 Threat management can help you control and manage mobile device access to your organization's data, help protect your organization from data loss, and help protect inbound and outbound messages from malicious software and spam. You also use threat management to protect your domain's reputation and to determine whether or not senders are maliciously spoofing accounts from your domain. For more information, see [Threat management in the Office 365 Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/threat-management).</span></span>

<span data-ttu-id="fd93f-150">Utilisez ces étapes pour afficher le tableau de bord de gestion Office 365 menace :</span><span class="sxs-lookup"><span data-stu-id="fd93f-150">Use these steps to view the Office 365 Threat management dashboard:</span></span>

1. <span data-ttu-id="fd93f-151">Dans l’onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **centres d’administration > sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-151">On the **Microsoft 365 admin center** tab of your browser, click **Admin centers > Security & Compliance**.</span></span>
2. <span data-ttu-id="fd93f-152">Dans l’onglet **sécurité et conformité** nouveau, cliquez sur **Gestion des menaces > tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-152">On the new **Security & Compliance** tab, click **Threat management > Dashboard**.</span></span>
3. <span data-ttu-id="fd93f-153">Dans l’onglet nouveau **tableau de bord** dans votre navigateur, notez l’évolution des programmes malveillants, insights et autres sections du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="fd93f-153">On the new **Dashboard** tab in your browser, note the malware trends, insights, and other sections of the dashboard.</span></span>

### <a name="office-365-cloud-app-security-dashboard"></a><span data-ttu-id="fd93f-154">Tableau de bord de sécurité des applications dans le nuage Office 365</span><span class="sxs-lookup"><span data-stu-id="fd93f-154">Office 365 Cloud App Security dashboard</span></span>

<span data-ttu-id="fd93f-p107">Office 365 Cloud application sécurité, anciennement appelé Office 365 gestion avancée de sécurité, vous permet de créer des stratégies pour surveiller et vous informent des activités suspectes dans votre abonnement Office 365, afin que vous pouvez examiner et prendre possibles mesures correctives. Pour plus d’informations, voir [Vue d’ensemble d’Office 365 Cloud Application Security](https://docs.microsoft.com/office365/securitycompliance/office-365-cas-overview).</span><span class="sxs-lookup"><span data-stu-id="fd93f-p107">Office 365 Cloud App Security, previously known as Office 365 Advanced Security Management, allows you to create policies that monitor for and inform you of suspicious activities in your Office 365 subscription, so that you can investigate and take possible remediation action. For more information, see [Overview of Office 365 Cloud App Security](https://docs.microsoft.com/office365/securitycompliance/office-365-cas-overview).</span></span>

1. <span data-ttu-id="fd93f-157">Dans l’onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **centres d’administration > sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-157">On the **Microsoft 365 admin center** tab of your browser, click **Admin centers > Security & Compliance**.</span></span>
2. <span data-ttu-id="fd93f-158">Dans l’onglet **sécurité et conformité** nouveau, cliquez sur **alertes > Gestion avancée des alertes > accédez à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-158">On the new **Security & Compliance** tab, click **Alerts > Manage advanced alerts > Go to Office 365 Cloud App Security**.</span></span>
3. <span data-ttu-id="fd93f-159">Sous l’onglet **Sécurité du nuage application** nouvelle, notez l’affichage de tableau de bord et la liste des stratégies par défaut qui analyser pour les différentes activités dans votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="fd93f-159">On the new **Cloud App Security** tab, note the dashboard view and the list of default policies that that monitor for various activities in your Office 365 subscription.</span></span>
4. <span data-ttu-id="fd93f-160">Cliquez sur l’icône de tableau de bord pour consulter un résumé des activités de sécurité des applications dans le nuage sont suivis.</span><span class="sxs-lookup"><span data-stu-id="fd93f-160">Click the dashboard icon to see a summary of Cloud App Security activities that are being tracked.</span></span>
5. <span data-ttu-id="fd93f-161">Cliquez sur **examiner** (l’icône LUNETTES), puis sur **journal d’activité** pour voir la liste des connexions récentes et autres activités.</span><span class="sxs-lookup"><span data-stu-id="fd93f-161">Click **Investigate** (the eyeglasses icon) and then **Activity log** to see the list of recent sign-ins and other activities.</span></span>

### <a name="secure-score"></a><span data-ttu-id="fd93f-162">Sécuriser le Score</span><span class="sxs-lookup"><span data-stu-id="fd93f-162">Secure Score</span></span>

1. <span data-ttu-id="fd93f-163">Créer un nouvel onglet dans votre navigateur et accédez à **securescore.office.com**.</span><span class="sxs-lookup"><span data-stu-id="fd93f-163">Create a new tab in your browser and go to **securescore.office.com**.</span></span>
2. <span data-ttu-id="fd93f-164">Sous l' **onglet tableau de bord**, notez votre Score Secure actuel et la liste des actions dans la file d’attente pour augmenter votre score.</span><span class="sxs-lookup"><span data-stu-id="fd93f-164">On the **Dashboard tab**, note your current Secure Score and the list of actions in the queue to increase your score.</span></span>

<span data-ttu-id="fd93f-165">Voir l’étape de [configuration d’accroître la sécurité pour Office 365](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md) dans la phase de **protection des informations** pour des informations et des liens pour configurer ces paramètres en production.</span><span class="sxs-lookup"><span data-stu-id="fd93f-165">See the [Configure increased security for Office 365](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md) step in the **Information protection** phase for information and links to configure these settings in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="fd93f-166">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="fd93f-166">Next step</span></span>

<span data-ttu-id="fd93f-167">Explorez les fonctionnalités supplémentaires de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) et fonctionnalités dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="fd93f-167">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd93f-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd93f-168">See also</span></span>

[<span data-ttu-id="fd93f-169">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fd93f-169">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="fd93f-170">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fd93f-170">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="fd93f-171">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fd93f-171">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)

