---
title: Sécurité accrue Microsoft 365 pour votre environnement de test Microsoft 365 entreprise
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
description: Utilisez ce guide de laboratoire de test pour activer des paramètres Microsoft 365 de sécurité supplémentaires que Microsoft 365 pour l’environnement de test d’entreprise.
ms.openlocfilehash: d1bff8b736e5074f621a173d206f7c5f77841b25
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51198350"
---
# <a name="increased-microsoft-365-security-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="0b98a-103">Sécurité accrue Microsoft 365 pour votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="0b98a-103">Increased Microsoft 365 security for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="0b98a-104">*Ce Guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="0b98a-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="0b98a-105">Avec les instructions de cet article, vous configurez des paramètres de Microsoft 365 supplémentaires pour renforcer la sécurité dans votre environnement de test Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="0b98a-105">With the instructions in this article, you configure additional Microsoft 365 settings to increase security in your Microsoft 365 for enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="0b98a-107">Cliquez [ici](../downloads/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan visuel de tous les articles de l’ensemble des guides de laboratoire de test de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="0b98a-107">Click [here](../downloads/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="0b98a-108">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="0b98a-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="0b98a-109">Si vous souhaitez simplement configurer une sécurité Microsoft 365 plus légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="0b98a-109">If you just want to configure increased Microsoft 365 security in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="0b98a-110">Si vous souhaitez configurer une sécurité Microsoft 365 plus grande dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="0b98a-110">If you want to configure increased Microsoft 365 security in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="0b98a-111">Le test d’une sécurité accrue Microsoft 365 ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="0b98a-111">Testing increased Microsoft 365 security does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="0b98a-112">Il est fourni ici en tant qu’option afin que vous pouvez tester la gestion automatisée des licences et l’appartenance à un groupe et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="0b98a-112">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 

## <a name="phase-2-configure-increased-microsoft-365-security"></a><span data-ttu-id="0b98a-113">Phase 2 : Configuration d’une sécurité Microsoft 365 plus grande</span><span class="sxs-lookup"><span data-stu-id="0b98a-113">Phase 2: Configure increased Microsoft 365 security</span></span>

<span data-ttu-id="0b98a-114">Dans cette phase, vous activez une sécurité Microsoft 365 plus grande pour votre Microsoft 365 environnement de test d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0b98a-114">In this phase, you enable increased Microsoft 365 security for your Microsoft 365 for enterprise test environment.</span></span> <span data-ttu-id="0b98a-115">Pour plus d’informations et de paramètres, voir [Configurer votre client pour une sécurité accrue.](/office365/securitycompliance/tenant-wide-setup-for-increased-security)</span><span class="sxs-lookup"><span data-stu-id="0b98a-115">For additional details and settings, see [Configure your tenant for increased security](/office365/securitycompliance/tenant-wide-setup-for-increased-security).</span></span>

### <a name="configure-sharepoint-online-to-block-apps-that-dont-support-modern-authentication"></a><span data-ttu-id="0b98a-116">Configurer SharePoint Online pour bloquer les applications qui ne permettent pas l’authentification moderne</span><span class="sxs-lookup"><span data-stu-id="0b98a-116">Configure SharePoint Online to block apps that don't support modern authentication</span></span>

<span data-ttu-id="0b98a-117">Les applications qui ne permettent pas l’authentification moderne ne peuvent pas avoir de configurations d’identité et d’accès aux appareils qui leur sont [appliquées,](../security/office-365-security/microsoft-365-policies-configurations.md) ce qui est un élément important de la sécurisation de votre abonnement Microsoft 365 et de ses biens numériques.</span><span class="sxs-lookup"><span data-stu-id="0b98a-117">Apps that do not support modern authentication cannot have [identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md) applied to them, which is an important element of securing your Microsoft 365 subscription and its digital assets.</span></span> 

1. <span data-ttu-id="0b98a-118">Go to the Microsoft 365 admin center ( [https://portal.microsoft.com](https://portal.microsoft.com) ) and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span><span class="sxs-lookup"><span data-stu-id="0b98a-118">Go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)) and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span></span>
    
  - <span data-ttu-id="0b98a-119">Si vous utilisez l’environnement de test Microsoft 365 léger, connectez-vous à partir de votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0b98a-119">If you are using the lightweight Microsoft 365 test environment, sign in from your local computer.</span></span>
    
  - <span data-ttu-id="0b98a-120">Si vous utilisez l’environnement de test Microsoft 365 entreprise simulée, utilisez le portail [Azure](https://portal.azure.com) pour vous connecter à la machine virtuelle CLIENT1, puis connectez-vous à partir de CLIENT1.</span><span class="sxs-lookup"><span data-stu-id="0b98a-120">If you are using the simulated enterprise Microsoft 365 test environment, use the [Azure portal](https://portal.azure.com) to connect to the CLIENT1 virtual machine, and then sign in from CLIENT1.</span></span>
 
2. <span data-ttu-id="0b98a-121">Sous le nouvel **onglet Microsoft 365 centre**  d’administration, sous Centres d’administration dans le volet de navigation de gauche, cliquez **sur SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="0b98a-121">On the new **Microsoft 365 admin center** tab, under **Admin centers** in the left navigation pane, click **SharePoint**.</span></span>
3. <span data-ttu-id="0b98a-122">Sous le nouvel **onglet SharePoint’administration,** cliquez sur **Stratégies > contrôle d’accès.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-122">On the new **SharePoint admin center** tab, click **Policies > Access control**.</span></span>
4. <span data-ttu-id="0b98a-123">Cliquez **sur Applications qui ne permettent pas l’authentification** moderne, **sélectionnez** Bloquer l’accès, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-123">Click **Apps that don't support modern authentication**, select **Block access**, and then click **Save**.</span></span>


### <a name="enable-defender-for-office-365-for-sharepoint-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="0b98a-124">Activer Defender pour Office 365 pour SharePoint, OneDrive Entreprise et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0b98a-124">Enable Defender for Office 365 for SharePoint, OneDrive for Business, and Microsoft Teams</span></span>

<span data-ttu-id="0b98a-125">Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span><span class="sxs-lookup"><span data-stu-id="0b98a-125">Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span></span>

1. <span data-ttu-id="0b98a-126">Go to the [Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span><span class="sxs-lookup"><span data-stu-id="0b98a-126">Go to the [Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span></span>

2. <span data-ttu-id="0b98a-127">Dans le volet de navigation de gauche, sous Gestion des **menaces,** cliquez sur **Stratégie,** puis cliquez sur **Pièces jointes sécurisées.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-127">In the left navigation pane, under **Threat management**, click **Policy**, and then click **Safe Attachments**.</span></span> 

3. <span data-ttu-id="0b98a-128">Sous **Protéger les fichiers dans SharePoint, OneDrive et Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="0b98a-128">Under **Protect files in SharePoint, OneDrive, and Microsoft Teams**.</span></span> <span data-ttu-id="0b98a-129">sélectionnez **Activer LAP pour SharePoint, OneDrive et Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="0b98a-129">select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

4. <span data-ttu-id="0b98a-130">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0b98a-130">Click **Save**.</span></span>


### <a name="enable-anti-malware"></a><span data-ttu-id="0b98a-131">Activer la protection contre les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="0b98a-131">Enable anti-malware</span></span>

<span data-ttu-id="0b98a-132">Les programmes malveillants sont constitués de virus et de logiciels espions.</span><span class="sxs-lookup"><span data-stu-id="0b98a-132">Malware is comprised of viruses and spyware.</span></span> <span data-ttu-id="0b98a-133">Les virus contaminent d'autres programmes et données, et ils se propagent dans votre ordinateur à la recherche de programmes à infecter.</span><span class="sxs-lookup"><span data-stu-id="0b98a-133">Viruses infect other programs and data, and they spread throughout your computer looking for programs to infect.</span></span> <span data-ttu-id="0b98a-134">Les logiciels espions font référence à des programmes malveillants qui collectent vos informations personnelles, telles que des informations de connectez-vous et des données personnelles, et les renvoient à l’auteur du programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="0b98a-134">Spyware refers to malware that gathers your personal information, such as sign-in information and personal data, and sends it back to the malware author.</span></span> 

<span data-ttu-id="0b98a-135">Microsoft 365 dispose de fonctionnalités intégrées de filtrage des programmes malveillants et du courrier indésirable qui vous aident à protéger les messages entrants et sortants contre les logiciels malveillants et à vous protéger contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="0b98a-135">Microsoft 365 has built-in malware and spam filtering capabilities that help protect inbound and outbound messages from malicious software and help protect you from spam.</span></span> <span data-ttu-id="0b98a-136">Pour plus d’informations, consultez [la & protection anti-programme malveillant.](../security/office-365-security/anti-spam-and-anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="0b98a-136">For more information, see [Anti-spam & anti-malware protection](../security/office-365-security/anti-spam-and-anti-malware-protection.md).</span></span>

<span data-ttu-id="0b98a-137">Pour vous assurer que le traitement anti-programme malveillant est effectué sur des fichiers avec des types de fichiers de pièces jointes courants :</span><span class="sxs-lookup"><span data-stu-id="0b98a-137">To ensure that anti-malware processing is being performed on files with common attachment file types:</span></span>

1. <span data-ttu-id="0b98a-138">Cliquez sur le bouton Retour de votre navigateur pour revenir à la page **Stratégie.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-138">Click the back button on your browser to get back to the **Policy** page.</span></span>
2. <span data-ttu-id="0b98a-139">Cliquez **sur Anti-programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-139">Click **Anti-malware**.</span></span>
3. <span data-ttu-id="0b98a-140">Double-cliquez sur la stratégie nommée **Default**.</span><span class="sxs-lookup"><span data-stu-id="0b98a-140">Double-click the policy named **Default**.</span></span>
4. <span data-ttu-id="0b98a-141">Dans la **fenêtre stratégie anti-programme** malveillant, cliquez **sur Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="0b98a-141">In the **Anti-malware policy** window, click **Settings**.</span></span>
4. <span data-ttu-id="0b98a-142">Sous **Filtre Types de pièces jointes courants,** **sélectionnez Sur,** puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-142">Under **Common Attachment Types filter**, select **On**, and then click **Save**.</span></span>


## <a name="phase-3-examine-the-security-dashboard"></a><span data-ttu-id="0b98a-143">Phase 3 : Examiner le tableau de bord de sécurité</span><span class="sxs-lookup"><span data-stu-id="0b98a-143">Phase 3: Examine the security dashboard</span></span>

<span data-ttu-id="0b98a-144">La gestion des menaces dans Microsoft 365 peut vous aider à contrôler et gérer l’accès des appareils mobiles aux données de votre organisation, à protéger votre organisation contre la perte de données et à protéger les messages entrants et sortants contre les logiciels malveillants et le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="0b98a-144">Threat management in Microsoft 365 can help you control and manage mobile device access to your organization's data, help protect your organization from data loss, and help protect inbound and outbound messages from malicious software and spam.</span></span> <span data-ttu-id="0b98a-145">Vous utilisez également la gestion des menaces pour protéger la réputation de votre domaine et pour déterminer si les expéditeurs usurpent des comptes malveillants à partir de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="0b98a-145">You also use threat management to protect your domain's reputation and to determine whether or not senders are maliciously spoofing accounts from your domain.</span></span> 

<span data-ttu-id="0b98a-146">Pour voir le tableau de bord de sécurité :</span><span class="sxs-lookup"><span data-stu-id="0b98a-146">To see the security dashboard:</span></span>

1. <span data-ttu-id="0b98a-147">Si nécessaire, go to the [Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span><span class="sxs-lookup"><span data-stu-id="0b98a-147">If needed, go to the [Security & Compliance Center](https://protection.office.com) and sign in with your global administrator account.</span></span>

2. <span data-ttu-id="0b98a-148">Dans le volet de navigation de gauche, sous **Gestion des menaces,** cliquez sur **Tableau de bord.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-148">In the left navigation pane, under **Threat management**, click **Dashboard**.</span></span>

<span data-ttu-id="0b98a-149">Regardez attentivement toutes les cartes du tableau de bord pour vous familiariser avec les informations fournies.</span><span class="sxs-lookup"><span data-stu-id="0b98a-149">Take a close look at all the cards on the dashboard to familiarize yourself with the information provided.</span></span>

<span data-ttu-id="0b98a-150">Pour plus d’informations, voir [Tableau de bord de sécurité.](../security/office-365-security/security-dashboard.md)</span><span class="sxs-lookup"><span data-stu-id="0b98a-150">For more information, see [Security Dashboard](../security/office-365-security/security-dashboard.md).</span></span>


## <a name="phase-4-examine-microsoft-secure-score"></a><span data-ttu-id="0b98a-151">Phase 4 : Examiner le score de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="0b98a-151">Phase 4: Examine Microsoft Secure Score</span></span>

<span data-ttu-id="0b98a-152">Le degré de sécurisation Microsoft indique votre posture de sécurité sous la forme d’un nombre, ce qui indique votre niveau actuel par rapport aux fonctionnalités disponibles dans votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b98a-152">Microsoft Secure Score shows your security posture as a number, which indicates your current level relative to the features that are available in your subscription.</span></span> <span data-ttu-id="0b98a-153">Il fournit également une liste des actions d’amélioration que vous pouvez prendre pour améliorer votre score.</span><span class="sxs-lookup"><span data-stu-id="0b98a-153">It also gives you a list of improvement actions you can take to improve your score.</span></span>

1. <span data-ttu-id="0b98a-154">Créez un onglet dans votre navigateur et allez dans le centre [de sécurité Microsoft 365,](https://security.microsoft.com/)puis cliquez sur **Score de sécurisation.**</span><span class="sxs-lookup"><span data-stu-id="0b98a-154">Create a new tab in your browser and go to the [Microsoft 365 security center](https://security.microsoft.com/), and then click **Secure score**.</span></span>
2. <span data-ttu-id="0b98a-155">Sous **l’onglet**  Vue d’ensemble, notez votre score de sécurisation actuel et sa comparaison avec la moyenne globale et les abonnements avec un nombre de licences similaire.</span><span class="sxs-lookup"><span data-stu-id="0b98a-155">On the **Overview**  tab, note your current Secure Score and how it compares with the global average and subscriptions with a similar number of licenses.</span></span>
3. <span data-ttu-id="0b98a-156">Sous **l’onglet Actions** d’amélioration, lisez la liste des actions que vous pouvez prendre pour augmenter votre score.</span><span class="sxs-lookup"><span data-stu-id="0b98a-156">On the **Improvement actions** tab, read through the list of actions you can take to increase your score.</span></span>

<span data-ttu-id="0b98a-157">Pour plus d’informations, voir [Le Score de sécurité Microsoft.](../security/defender/microsoft-secure-score.md)</span><span class="sxs-lookup"><span data-stu-id="0b98a-157">For more information, see [Microsoft Secure Score](../security/defender/microsoft-secure-score.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="0b98a-158">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="0b98a-158">Next steps</span></span>

<span data-ttu-id="0b98a-159">Explorez [d’autres fonctionnalités de protection](m365-enterprise-test-lab-guides.md#information-protection) des informations dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="0b98a-159">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b98a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b98a-160">See also</span></span>

[<span data-ttu-id="0b98a-161">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="0b98a-161">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="0b98a-162">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="0b98a-162">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="0b98a-163">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0b98a-163">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)