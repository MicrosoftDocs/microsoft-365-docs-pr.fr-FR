---
title: Amélioration de la sécurité Microsoft 365 pour votre environnement de test Microsoft 365 pour les entreprises
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/09/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-security-compliance
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce guide de laboratoire de test pour activer des paramètres de sécurité Microsoft 365 supplémentaires pour votre environnement de test Microsoft 365.
ms.openlocfilehash: 09a613261bc173cd71e9cc2dd58a32a9547ece21
ms.sourcegitcommit: cd17328baa58448214487e3e68c37590ab9fd08d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48398948"
---
# <a name="increased-microsoft-365-security-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="fcfad-103">Amélioration de la sécurité Microsoft 365 pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="fcfad-103">Increased Microsoft 365 security for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="fcfad-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="fcfad-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="fcfad-105">Les instructions de cet article vous permettent de configurer des paramètres supplémentaires de Microsoft 365 pour renforcer la sécurité dans votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="fcfad-105">With the instructions in this article, you configure additional Microsoft 365 settings to increase security in your Microsoft 365 for enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="fcfad-107">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan visuel de tous les articles de l’ensemble des guides de laboratoire de test de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="fcfad-107">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="fcfad-108">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="fcfad-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="fcfad-109">Si vous souhaitez simplement configurer une sécurité Microsoft 365 accrue de façon légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="fcfad-109">If you just want to configure increased Microsoft 365 security in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="fcfad-110">Si vous souhaitez configurer la sécurité Microsoft 365 améliorée dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fcfad-110">If you want to configure increased Microsoft 365 security in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="fcfad-111">Test la sécurité améliorée de Microsoft 365 ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="fcfad-111">Testing increased Microsoft 365 security does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="fcfad-112">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="fcfad-112">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 

## <a name="phase-2-configure-increased-microsoft-365-security"></a><span data-ttu-id="fcfad-113">Phase 2 : configuration de la sécurité Microsoft 365 améliorée</span><span class="sxs-lookup"><span data-stu-id="fcfad-113">Phase 2: Configure increased Microsoft 365 security</span></span>

<span data-ttu-id="fcfad-114">Dans cette phase, vous allez activer la sécurité Microsoft 365 pour votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="fcfad-114">In this phase, you enable increased Microsoft 365 security for your Microsoft 365 for enterprise test environment.</span></span> <span data-ttu-id="fcfad-115">Pour plus d’informations et de paramètres, consultez [la rubrique Configure Your Client for major Security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span><span class="sxs-lookup"><span data-stu-id="fcfad-115">For additional details and settings, see [Configure your tenant for increased security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span></span>

### <a name="configure-sharepoint-online-to-block-apps-that-dont-support-modern-authentication"></a><span data-ttu-id="fcfad-116">Configurer SharePoint Online pour bloquer les applications qui ne prennent pas en charge l’authentification moderne</span><span class="sxs-lookup"><span data-stu-id="fcfad-116">Configure SharePoint Online to block apps that don't support modern authentication</span></span>

<span data-ttu-id="fcfad-117">Les applications qui ne prennent pas en charge l’authentification moderne ne peuvent pas avoir de [configurations d’identité et d’accès aux appareils](../security/office-365-security/microsoft-365-policies-configurations.md) appliquées, ce qui est un élément important de la sécurisation de votre abonnement Microsoft 365 et de ses biens numériques.</span><span class="sxs-lookup"><span data-stu-id="fcfad-117">Apps that do not support modern authentication cannot have [identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md) applied to them, which is an important element of securing your Microsoft 365 subscription and its digital assets.</span></span> 

1. <span data-ttu-id="fcfad-118">Accédez au centre d’administration Microsoft 365 ( [https://portal.microsoft.com](https://portal.microsoft.com) ) et connectez-vous à votre abonnement de laboratoire de test microsoft 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="fcfad-118">Go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)) and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span></span>
    
  - <span data-ttu-id="fcfad-119">Si vous utilisez l’environnement de test Microsoft 365 léger, connectez-vous à partir de votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fcfad-119">If you are using the lightweight Microsoft 365 test environment, sign in from your local computer.</span></span>
    
  - <span data-ttu-id="fcfad-120">Si vous utilisez l’environnement de test d’entreprise simulé de Microsoft 365, utilisez le [portail Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle CLIENT1, puis connectez-vous à partir de client1.</span><span class="sxs-lookup"><span data-stu-id="fcfad-120">If you are using the simulated enterprise Microsoft 365 test environment, use the [Azure portal](https://portal.azure.com) to connect to the CLIENT1 virtual machine, and then sign in from CLIENT1.</span></span>
 
2. <span data-ttu-id="fcfad-121">Dans le nouvel onglet **Centre d’administration Microsoft 365** , sous **centres d’administration** dans le volet de navigation de gauche, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-121">On the new **Microsoft 365 admin center** tab, under **Admin centers** in the left navigation pane, click **SharePoint**.</span></span>
3. <span data-ttu-id="fcfad-122">Dans le nouvel onglet **Centre d’administration SharePoint** , cliquez sur **stratégies > contrôle d’accès**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-122">On the new **SharePoint admin center** tab, click **Policies > Access control**.</span></span>
4. <span data-ttu-id="fcfad-123">Cliquez sur **applications qui ne prennent pas en charge l’authentification moderne**, sélectionnez **bloquer l’accès**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-123">Click **Apps that don't support modern authentication**, select **Block access**, and then click **Save**.</span></span>


### <a name="enable-advanced-threat-protection-for-sharepoint-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="fcfad-124">Activer la protection avancée contre les menaces pour SharePoint, OneDrive entreprise et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="fcfad-124">Enable Advanced Threat Protection for SharePoint, OneDrive for Business, and Microsoft Teams</span></span>

<span data-ttu-id="fcfad-125">Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive et Microsoft teams protège votre organisation contre le partage accidentel de fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="fcfad-125">Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span></span>

1. <span data-ttu-id="fcfad-126">Accédez au [Centre de sécurité & conformité](https://protection.office.com) et connectez-vous avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="fcfad-126">Go to the [Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span></span>

2. <span data-ttu-id="fcfad-127">Dans le volet de navigation de gauche, sous **gestion des menaces**, cliquez sur **stratégie**, puis sur **pièces jointes approuvées ATP**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-127">In the left navigation pane, under **Threat management**, click **Policy**, and then click **ATP safe attachments**.</span></span> 

3. <span data-ttu-id="fcfad-128">Sous **protéger les fichiers dans SharePoint, OneDrive et Microsoft teams**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-128">Under **Protect files in SharePoint, OneDrive, and Microsoft Teams**.</span></span> <span data-ttu-id="fcfad-129">Sélectionnez Activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-129">select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

4. <span data-ttu-id="fcfad-130">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-130">Click **Save**.</span></span>


### <a name="enable-anti-malware"></a><span data-ttu-id="fcfad-131">Activer le blocage des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fcfad-131">Enable anti-malware</span></span>

<span data-ttu-id="fcfad-132">Les programmes malveillants sont constitués de virus et de logiciels espions.</span><span class="sxs-lookup"><span data-stu-id="fcfad-132">Malware is comprised of viruses and spyware.</span></span> <span data-ttu-id="fcfad-133">Les virus contaminent d'autres programmes et données, et ils se propagent dans votre ordinateur à la recherche de programmes à infecter.</span><span class="sxs-lookup"><span data-stu-id="fcfad-133">Viruses infect other programs and data, and they spread throughout your computer looking for programs to infect.</span></span> <span data-ttu-id="fcfad-134">Les logiciels espions font référence aux programmes malveillants qui recueillent vos informations personnelles, telles que les informations de connexion et les données personnelles, et les renvoient à l’auteur de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="fcfad-134">Spyware refers to malware that gathers your personal information, such as sign-in information and personal data, and sends it back to the malware author.</span></span> 

<span data-ttu-id="fcfad-135">Microsoft 365 dispose de fonctionnalités intégrées de filtrage des courriers indésirables et des programmes malveillants qui permettent de protéger les messages entrants et sortants des logiciels malveillants et de vous protéger contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="fcfad-135">Microsoft 365 has built-in malware and spam filtering capabilities that help protect inbound and outbound messages from malicious software and help protect you from spam.</span></span> <span data-ttu-id="fcfad-136">Pour plus d’informations, consultez la rubrique [anti-spam & la protection contre les programmes malveillants](../security/office-365-security/anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="fcfad-136">For more information, see [Anti-spam & anti-malware protection](../security/office-365-security/anti-spam-and-anti-malware-protection.md).</span></span>

<span data-ttu-id="fcfad-137">Pour vérifier que le traitement anti-programme malveillant est effectué sur des fichiers avec des types de fichiers de pièces jointes courants :</span><span class="sxs-lookup"><span data-stu-id="fcfad-137">To ensure that anti-malware processing is being performed on files with common attachment file types:</span></span>

1. <span data-ttu-id="fcfad-138">Cliquez sur le bouton précédent de votre navigateur pour revenir à la page **stratégie** .</span><span class="sxs-lookup"><span data-stu-id="fcfad-138">Click the back button on your browser to get back to the **Policy** page.</span></span>
2. <span data-ttu-id="fcfad-139">Cliquez sur **anti-programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-139">Click **Anti-malware**.</span></span>
3. <span data-ttu-id="fcfad-140">Double-cliquez sur la stratégie nommée **default**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-140">Double-click the policy named **Default**.</span></span>
4. <span data-ttu-id="fcfad-141">Dans la fenêtre **stratégie anti-programme malveillant** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-141">In the **Anti-malware policy** window, click **Settings**.</span></span>
4. <span data-ttu-id="fcfad-142">Sous **Common Attachment types Filter**, sélectionnez **activé**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-142">Under **Common Attachment Types filter**, select **On**, and then click **Save**.</span></span>


## <a name="phase-3-examine-the-security-dashboard"></a><span data-ttu-id="fcfad-143">Phase 3 : examiner le tableau de bord de sécurité</span><span class="sxs-lookup"><span data-stu-id="fcfad-143">Phase 3: Examine the security dashboard</span></span>

<span data-ttu-id="fcfad-144">La gestion des menaces dans Microsoft 365 vous permet de contrôler et de gérer l’accès des appareils mobiles aux données de votre organisation, de protéger votre organisation contre la perte de données et de protéger les messages entrants et sortants contre les logiciels malveillants et le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="fcfad-144">Threat management in Microsoft 365 can help you control and manage mobile device access to your organization's data, help protect your organization from data loss, and help protect inbound and outbound messages from malicious software and spam.</span></span> <span data-ttu-id="fcfad-145">Vous pouvez également utiliser la gestion des menaces pour protéger la réputation de votre domaine et déterminer si les expéditeurs sont ou non usurpés de manière malveillante les comptes de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="fcfad-145">You also use threat management to protect your domain's reputation and to determine whether or not senders are maliciously spoofing accounts from your domain.</span></span> 

<span data-ttu-id="fcfad-146">Pour afficher le tableau de bord de sécurité :</span><span class="sxs-lookup"><span data-stu-id="fcfad-146">To see the security dashboard:</span></span>

1. <span data-ttu-id="fcfad-147">Si nécessaire, accédez au [Centre de sécurité & conformité](https://protection.office.com) et connectez-vous avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="fcfad-147">If needed, go to the [Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span></span>

2. <span data-ttu-id="fcfad-148">Dans le volet de navigation de gauche, sous **gestion des menaces**, cliquez sur **tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-148">In the left navigation pane, under **Threat management**, click **Dashboard**.</span></span>

<span data-ttu-id="fcfad-149">Examinez attentivement toutes les cartes du tableau de bord pour vous familiariser avec les informations fournies.</span><span class="sxs-lookup"><span data-stu-id="fcfad-149">Take a close look at all the cards on the dashboard to familiarize yourself with the information provided.</span></span>

<span data-ttu-id="fcfad-150">Pour plus d’informations, consultez la rubrique [Security Dashboard](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-dashboard).</span><span class="sxs-lookup"><span data-stu-id="fcfad-150">For more information, see [Security Dashboard](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-dashboard).</span></span>


## <a name="phase-4-examine-microsoft-secure-score"></a><span data-ttu-id="fcfad-151">Phase 4 : examiner le score de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="fcfad-151">Phase 4: Examine Microsoft Secure Score</span></span>

<span data-ttu-id="fcfad-152">Le score de sécurité Microsoft indique votre position de sécurité sous la forme d’un nombre, ce qui indique votre niveau actuel par rapport aux fonctionnalités disponibles dans votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcfad-152">Microsoft Secure Score shows your security posture as a number, which indicates your current level relative to the features that are available in your subscription.</span></span> <span data-ttu-id="fcfad-153">Elle vous fournit également une liste des actions d’amélioration que vous pouvez effectuer pour améliorer votre score.</span><span class="sxs-lookup"><span data-stu-id="fcfad-153">It also gives you a list of improvement actions you can take to improve your score.</span></span>

1. <span data-ttu-id="fcfad-154">Créez un nouvel onglet dans votre navigateur et accédez au [Centre de sécurité Microsoft 365](https://security.microsoft.com/), puis cliquez sur **score sécurisé**.</span><span class="sxs-lookup"><span data-stu-id="fcfad-154">Create a new tab in your browser and go to the [Microsoft 365 security center](https://security.microsoft.com/), and then click **Secure score**.</span></span>
2. <span data-ttu-id="fcfad-155">Sous l’onglet **vue d’ensemble**  , Notez votre score de sécurité actuel et sa comparaison avec la moyenne globale et les abonnements avec un nombre similaire de licences.</span><span class="sxs-lookup"><span data-stu-id="fcfad-155">On the **Overview**  tab, note your current Secure Score and how it compares with the global average and subscriptions with a similar number of licenses.</span></span>
3. <span data-ttu-id="fcfad-156">Dans l’onglet **actions d’amélioration** , consultez la liste des actions que vous pouvez effectuer pour augmenter votre score.</span><span class="sxs-lookup"><span data-stu-id="fcfad-156">On the **Improvement actions** tab, read through the list of actions you can take to increase your score.</span></span>

<span data-ttu-id="fcfad-157">Pour plus d’informations, consultez la rubrique [Microsoft Secure score](https://docs.microsoft.com/microsoft-365/security/mtp/microsoft-secure-score).</span><span class="sxs-lookup"><span data-stu-id="fcfad-157">For more information, see [Microsoft Secure Score](https://docs.microsoft.com/microsoft-365/security/mtp/microsoft-secure-score).</span></span>

## <a name="next-steps"></a><span data-ttu-id="fcfad-158">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fcfad-158">Next steps</span></span>

<span data-ttu-id="fcfad-159">Découvrez les fonctionnalités et les fonctionnalités de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) supplémentaires dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="fcfad-159">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcfad-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcfad-160">See also</span></span>

[<span data-ttu-id="fcfad-161">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="fcfad-161">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="fcfad-162">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="fcfad-162">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="fcfad-163">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="fcfad-163">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
