---
title: Amélioration de la sécurité Microsoft 365 pour votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/10/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-security-compliance
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce guide de laboratoire de test pour activer des paramètres de sécurité Microsoft 365 supplémentaires pour votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: d51f9ada68969823eadbb4fad55392358a6ddee8
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34072134"
---
# <a name="increased-microsoft-365-security-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="1e57a-103">Amélioration de la sécurité Microsoft 365 pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1e57a-103">Increased Microsoft 365 security for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="1e57a-104">Les instructions de cet article vous permettent de configurer des paramètres supplémentaires de Microsoft 365 pour renforcer la sécurité dans votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="1e57a-104">With the instructions in this article, you configure additional Microsoft 365 settings to increase security in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="1e57a-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1e57a-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="1e57a-107">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1e57a-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="1e57a-108">Si vous souhaitez simplement configurer une sécurité Microsoft 365 accrue de façon légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="1e57a-108">If you just want to configure increased Microsoft 365 security in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="1e57a-109">Si vous souhaitez configurer la sécurité Microsoft 365 améliorée dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1e57a-109">If you want to configure increased Microsoft 365 security in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1e57a-110">Test la sécurité améliorée de Microsoft 365 ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="1e57a-110">Testing increased Microsoft 365 security does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="1e57a-111">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="1e57a-111">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 


## <a name="phase-2-configure-increased-microsoft-365-security"></a><span data-ttu-id="1e57a-112">Phase 2: configuration de la sécurité Microsoft 365 améliorée</span><span class="sxs-lookup"><span data-stu-id="1e57a-112">Phase 2: Configure increased Microsoft 365 security</span></span>

<span data-ttu-id="1e57a-113">Dans cette phase, vous allez activer la sécurité Microsoft 365 améliorée pour votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="1e57a-113">In this phase, you enable increased Microsoft 365 security for your Microsoft 365 Enterprise test environment.</span></span> <span data-ttu-id="1e57a-114">Pour plus d’informations et de paramètres, voir [Configure Your Office 365 client for major Security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span><span class="sxs-lookup"><span data-stu-id="1e57a-114">For additional details and settings, see [Configure your Office 365 tenant for increased security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span></span>

### <a name="configure-sharepoint-online-to-block-apps-that-dont-support-modern-authentication"></a><span data-ttu-id="1e57a-115">Configurer SharePoint Online pour bloquer les applications qui ne prennent pas en charge l’authentification moderne</span><span class="sxs-lookup"><span data-stu-id="1e57a-115">Configure SharePoint Online to block apps that don’t support modern authentication</span></span>

<span data-ttu-id="1e57a-116">Les applications qui ne prennent pas en charge l’authentification moderne ne peuvent pas avoir de [configurations d’identité et d’accès aux appareils](microsoft-365-policies-configurations.md) appliquées, ce qui est un élément important de la sécurisation de votre abonnement Microsoft 365 et de ses biens numériques.</span><span class="sxs-lookup"><span data-stu-id="1e57a-116">Apps that do not support modern authentication cannot have [identity and device access configurations](microsoft-365-policies-configurations.md) applied to them, which is an important element of securing your Microsoft 365 subscription and its digital assets.</span></span> 

1. <span data-ttu-id="1e57a-117">Accédez au centre d’administration Microsoft 365 ([https://portal.microsoft.com](https://portal.microsoft.com)) et connectez-vous à votre abonnement de laboratoire de test Office 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="1e57a-117">Go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)) and sign in to your Office 365 test lab subscription with your global administrator account.</span></span>
    
  - <span data-ttu-id="1e57a-118">Si vous utilisez l’environnement de test Microsoft 365 léger, connectez-vous à partir de votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1e57a-118">If you are using the lightweight Microsoft 365 test environment, sign in from your local computer.</span></span>
    
  - <span data-ttu-id="1e57a-119">Si vous utilisez l’environnement de test d’entreprise simulé de Microsoft 365, utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle CLIENT1, puis connectez-vous à partir de client1.</span><span class="sxs-lookup"><span data-stu-id="1e57a-119">If you are using the simulated enterprise Microsoft 365 test environment, use the [Azure portal](https://portal.azure.com) to connect to the CLIENT1 virtual machine, and then sign in from CLIENT1.</span></span>
 
2. <span data-ttu-id="1e57a-120">Dans le nouvel onglet **Centre d’administration Microsoft 365** , cliquez sur **centres d’administration > SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-120">On the new **Microsoft 365 admin center** tab, click **Admin centers > SharePoint**.</span></span>
3. <span data-ttu-id="1e57a-121">Dans le nouvel onglet **Centre d’administration SharePoint** , cliquez sur **contrôle d’accès**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-121">On the new **SharePoint admin center** tab, click **Access control**.</span></span>
4. <span data-ttu-id="1e57a-122">Sous **applications qui ne prennent pas en charge l’authentification moderne**, cliquez sur **bloquer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-122">Under **Apps that don’t support modern authentication**, click **Block**, and then click **OK**.</span></span>


### <a name="enable-advanced-threat-protection-for-sharepoint-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="1e57a-123">Activer la protection avancée contre les menaces pour SharePoint, OneDrive entreprise et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="1e57a-123">Enable Advanced Threat Protection for SharePoint, OneDrive for Business, and Microsoft Teams</span></span>

<span data-ttu-id="1e57a-124">Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive et Microsoft teams protège votre organisation contre le partage accidentel de fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="1e57a-124">Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span></span>

1. <span data-ttu-id="1e57a-125">Accédez au [Centre de sécurité & de sécurité Office 365](https://protection.office.com) et connectez-vous avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="1e57a-125">Go to the [Office 365 Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span></span>

2. <span data-ttu-id="1e57a-126">Dans le volet de navigation de gauche, sous **gestion des menaces**, choisissez **stratégie _GT_ les pièces jointes fiables**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-126">In the left navigation pane, under **Threat management**, choose **Policy > Safe Attachments**.</span></span> 

3. <span data-ttu-id="1e57a-127">Sélectionnez Activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-127">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

4. <span data-ttu-id="1e57a-128">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-128">Click **Save**.</span></span>


### <a name="enable-anti-malware"></a><span data-ttu-id="1e57a-129">Activer le blocage des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1e57a-129">Enable anti-malware</span></span>

<span data-ttu-id="1e57a-130">Les programmes malveillants sont constitués de virus et de logiciels espions.</span><span class="sxs-lookup"><span data-stu-id="1e57a-130">Malware is comprised of viruses and spyware.</span></span> <span data-ttu-id="1e57a-131">Les virus contaminent d'autres programmes et données, et ils se propagent dans votre ordinateur à la recherche de programmes à infecter.</span><span class="sxs-lookup"><span data-stu-id="1e57a-131">Viruses infect other programs and data, and they spread throughout your computer looking for programs to infect.</span></span> <span data-ttu-id="1e57a-132">Les logiciels espions font référence aux programmes malveillants qui recueillent vos informations personnelles, telles que les informations de connexion et les données personnelles, et les renvoient à l’auteur de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="1e57a-132">Spyware refers to malware that gathers your personal information, such as sign-in information and personal data, and sends it back to the malware author.</span></span> 

<span data-ttu-id="1e57a-133">Office 365 dispose de fonctionnalités intégrées de filtrage des courriers indésirables et des programmes malveillants qui permettent de protéger les messages entrants et sortants des logiciels malveillants et de vous protéger contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1e57a-133">Office 365 has built-in malware and spam filtering capabilities that help protect inbound and outbound messages from malicious software and help protect you from spam.</span></span> <span data-ttu-id="1e57a-134">Pour plus d’informations, consultez la rubrique [anti-spam & protection contre les programmes malveillants dans Office 365](https://docs.microsoft.com/office365/securitycompliance/anti-spam-and-anti-malware-protection)</span><span class="sxs-lookup"><span data-stu-id="1e57a-134">For more information, see [Anti-spam & anti-malware protection in Office 365](https://docs.microsoft.com/office365/securitycompliance/anti-spam-and-anti-malware-protection)</span></span>

<span data-ttu-id="1e57a-135">Pour vérifier que le traitement anti-programme malveillant est effectué sur des fichiers avec des types de fichiers de pièces jointes courants:</span><span class="sxs-lookup"><span data-stu-id="1e57a-135">To ensure that anti-malware processing is being performed on files with common attachment file types:</span></span>

1. <span data-ttu-id="1e57a-136">Cliquez sur le bouton précédent de votre navigateur pour revenir à la page **stratégie** .</span><span class="sxs-lookup"><span data-stu-id="1e57a-136">Click the back button on your browser to get back to the **Policy** page.</span></span>
2. <span data-ttu-id="1e57a-137">Cliquez sur **anti-programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-137">Click **Anti-malware**.</span></span>
3. <span data-ttu-id="1e57a-138">Double-cliquez sur la stratégie nommée **default**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-138">Double-click the policy named **Default**.</span></span>
4. <span data-ttu-id="1e57a-139">Dans la fenêtre **stratégie anti-programme malveillant** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-139">In the **Anti-malware policy** window, click **Settings**.</span></span>
4. <span data-ttu-id="1e57a-140">Sous **Common Attachment types Filter**, cliquez sur **> Save**.</span><span class="sxs-lookup"><span data-stu-id="1e57a-140">Under **Common Attachment Types filter**, click **On > Save**.</span></span>


## <a name="phase-3-examine-the-threat-management-dashboard"></a><span data-ttu-id="1e57a-141">Phase 3: examiner le tableau de bord de gestion des menaces</span><span class="sxs-lookup"><span data-stu-id="1e57a-141">Phase 3: Examine the threat management dashboard</span></span>

<span data-ttu-id="1e57a-142">Office 365 Threat Management peut vous aider à contrôler et à gérer l’accès des appareils mobiles aux données de votre organisation, à protéger votre organisation contre la perte de données et à protéger les messages entrants et sortants contre les logiciels malveillants et le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1e57a-142">Office 365 Threat management can help you control and manage mobile device access to your organization's data, help protect your organization from data loss, and help protect inbound and outbound messages from malicious software and spam.</span></span> <span data-ttu-id="1e57a-143">Vous pouvez également utiliser la gestion des menaces pour protéger la réputation de votre domaine et déterminer si les expéditeurs sont ou non usurpés de manière malveillante les comptes de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="1e57a-143">You also use threat management to protect your domain's reputation and to determine whether or not senders are maliciously spoofing accounts from your domain.</span></span> <span data-ttu-id="1e57a-144">Pour plus d’informations, consultez [la rubrique gestion des menaces dans le centre de sécurité Microsoft 365](https://docs.microsoft.com/office365/securitycompliance/threat-management).</span><span class="sxs-lookup"><span data-stu-id="1e57a-144">For more information, see [Threat management in the Microsoft 365 security center](https://docs.microsoft.com/office365/securitycompliance/threat-management).</span></span>

<!--
### Office 365 Cloud App Security dashboard

Office 365 Cloud App Security, previously known as Office 365 Advanced Security Management, allows you to create policies that monitor for and inform you of suspicious activities in your Office 365 subscription, so that you can investigate and take possible remediation action. For more information, see [Overview of Office 365 Cloud App Security](https://docs.microsoft.com/office365/securitycompliance/office-365-cas-overview).

### Microsoft 365 Secure Score

1. Create a new tab in your browser and go to the [Microsoft 365 security center](https://security.microsoft.com/), and then click **Secure score**.
2. On the **Dashboard tab**, note your current Secure Score and the list of actions in the queue to increase your score.
!-->


## <a name="next-steps"></a><span data-ttu-id="1e57a-145">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1e57a-145">Next steps</span></span>

<span data-ttu-id="1e57a-146">Pour plus d’informations et de liens sur la configuration de ces paramètres en production, voir l’étape [configurer la sécurité accrue pour Microsoft 365](infoprotect-configure-increased-security-office-365.md) de la phase de **protection des informations** .</span><span class="sxs-lookup"><span data-stu-id="1e57a-146">See the [Configure increased security for Microsoft 365](infoprotect-configure-increased-security-office-365.md) step in the **Information protection** phase for information and links to configure these settings in production.</span></span>

<span data-ttu-id="1e57a-147">Découvrez les fonctionnalités et les fonctionnalités de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) supplémentaires dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="1e57a-147">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e57a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e57a-148">See also</span></span>

[<span data-ttu-id="1e57a-149">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1e57a-149">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="1e57a-150">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1e57a-150">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="1e57a-151">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1e57a-151">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)

