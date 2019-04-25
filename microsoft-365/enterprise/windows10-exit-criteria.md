---
title: 'Phase 3 : Critères de sortie pour l’infrastructure Windows 10 Entreprise'
ms.author: greglin
author: greg-lindsay
manager: laurawi
ms.date: 03/05/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-modern-desktop
- Strat_O365_Enterprise
ms.custom: ''
description: Assurez-vous que votre configuration répond aux critères de Microsoft 365 Entreprise pour Windows 10 Entreprise.
ms.openlocfilehash: 1e8a2e748f42431465c027acbc468f4c5891d320
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289515"
---
# <a name="phase-3-windows-10-enterprise-infrastructure-exit-criteria"></a><span data-ttu-id="01163-103">Phase 3 : Critères de sortie pour l’infrastructure Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="01163-103">Phase 3: Windows 10 Enterprise infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)

<span data-ttu-id="01163-104">Vérifiez que votre infrastructure Windows 10 Entreprise répond aux critères suivants requis et que vous avez décidé ceux qui sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="01163-104">Make sure your Windows 10 Enterprise infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<a name="crit-windows10-step1"></a>
## <a name="required-your-microsoft-365-domains-are-added-and-verified"></a><span data-ttu-id="01163-105">Obligatoire : ajout et vérification de vos domaines Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="01163-105">Required: Your Microsoft 365 domains are added and verified</span></span>

<span data-ttu-id="01163-106">Le locataire Azure AD pour vos abonnements Office 365 et Intune est configuré avec vos noms de domaines Internet (par exemple, contoso.com), plutôt qu’avec un nom de domaine incluant « onmicrosoft.com ».</span><span class="sxs-lookup"><span data-stu-id="01163-106">The Azure AD tenant for your Office 365 and Intune subscriptions are configured with your Internet domain names (such as contoso.com), rather than just a domain name that includes “onmicrosoft.com”.</span></span> 

<span data-ttu-id="01163-p101">Sinon, vous êtes limité concernant les méthodes d’authentification configurables. Par exemple, les authentifications fédérée et directe ne peuvent pas utiliser le nom de domaine « onmicrosoft.com ».</span><span class="sxs-lookup"><span data-stu-id="01163-p101">If you do not do so, you will be limited in the authentication methods that you can configure. For example, pass-through and federated authentication cannot use the “onmicrosoft.com”  domain name.</span></span>

<span data-ttu-id="01163-109">Si nécessaire, l’[Étape 1](windows10-prepare-your-org.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="01163-109">If needed, [Step 1](windows10-prepare-your-org.md) can help you with this requirement.</span></span>

## <a name="optional-your-users-are-added-and-licensed"></a><span data-ttu-id="01163-110">Facultatif : ajout de vos utilisateurs et obtention de licence</span><span class="sxs-lookup"><span data-stu-id="01163-110">Optional: Your users are added and licensed</span></span>

<span data-ttu-id="01163-111">Les comptes correspondant à vos utilisateurs sont ajoutés, soit directement dans votre locataire Azure AD pour vos abonnements Office 365 et Intune, soit à partir de la synchronisation d’annuaires de votre version locale de Windows Server ( Active Directory Domain Services: AD DS).</span><span class="sxs-lookup"><span data-stu-id="01163-111">The accounts corresponding to your users are added, either directly to your Azure AD tenant for your Office 365 and Intune subscriptions, or from directory synchronization from your on-premises Windows Server AD.</span></span>

<span data-ttu-id="01163-112">Une fois que les utilisateurs sont ajoutés, vous pouvez leur attribuer des licences Microsoft 365 Entreprise, soit directement en tant qu’administrateur d’utilisateurs ou administrateur général, soit automatiquement via l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="01163-112">Once the users are added, you can assign them Microsoft 365 Enterprise licenses, either directly as a global or user administrator, or automatically through group membership.</span></span>

<span data-ttu-id="01163-113">Si nécessaire, l’[Étape 1](windows10-prepare-your-org.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="01163-113">If needed, [Step 1](windows10-prepare-your-org.md) can help you with this option.</span></span>

## <a name="optional-diagnostics-are-enabled"></a><span data-ttu-id="01163-114">Facultatif : les diagnostics sont activés</span><span class="sxs-lookup"><span data-stu-id="01163-114">Optional: Diagnostics are enabled</span></span>

<span data-ttu-id="01163-115">Vous avez activé les paramètres de données de diagnostic à l’aide d’une stratégie de groupe, de Microsoft Intune, de l’éditeur du Registre ou à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="01163-115">You have enabled diagnostic data settings using Group Policy, Microsoft Intune, the Registry Editor, or at the command prompt.</span></span>

<span data-ttu-id="01163-116">Si nécessaire, l’[Étape 1](windows10-prepare-your-org.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="01163-116">If needed, [Step 1](windows10-prepare-your-org.md) can help you with this option.</span></span>

<a name="crit-windows10-step2"></a>
## <a name="required-for-in-place-upgrade-created-a-configuration-manager-task-sequence-for-an-operating-system-deployment"></a><span data-ttu-id="01163-117">Obligatoire pour la mise à niveau sur place : création d’une séquence de tâches du Gestionnaire de configuration pour le déploiement d’un système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="01163-117">Required for in-place upgrade: Created a Configuration Manager task sequence for an operating system deployment</span></span>

<span data-ttu-id="01163-118">Pour démarrer une séquence de tâches du Gestionnaire de configuration afin d’effectuer une mise à niveau sur place sur un périphérique exécutant Windows 7 ou Windows 8.1, vous devez avoir :</span><span class="sxs-lookup"><span data-stu-id="01163-118">To start a Configuration Manager task sequence to do an in-place upgrade on a device running Windows 7 or Windows 8.1, you must have:</span></span>

- <span data-ttu-id="01163-119">définir le niveau de données de diagnostic Windows approprié ; et</span><span class="sxs-lookup"><span data-stu-id="01163-119">Set the proper Windows diagnostics data level</span></span>
- <span data-ttu-id="01163-120">Vérifié la préparation de la mise à niveau Windows</span><span class="sxs-lookup"><span data-stu-id="01163-120">Verify the readiness to upgrade Windows</span></span>
- <span data-ttu-id="01163-121">Créé une séquence de tâches du Gestionnaire de configuration qui inclut une collection de périphériques et le déploiement d’un système d’exploitation avec une image de système d’exploitation Windows 10.</span><span class="sxs-lookup"><span data-stu-id="01163-121">Create a Configuration Manager task sequence that includes a device collection and an operating system deployment with a Windows 10 OS image</span></span>

<span data-ttu-id="01163-p102">Une fois ces éléments en place, vous pouvez effectuer des mises à niveau sur place sur les périphériques qui sont prêts à recevoir la mise à niveau de Windows. Pour optimiser Microsoft 365 Entreprise, mettez à niveau autant de périphériques exécutant Windows 7 et Windows 8.1 que possible.</span><span class="sxs-lookup"><span data-stu-id="01163-p102">Once this is in place, you can perform in-place upgrades on devices that are ready to upgrade Windows. To get the maximum benefit out of Microsoft 365 Enterprise, upgrade as many devices running Windows 7 and Windows 8.1 as you can.</span></span> 

<span data-ttu-id="01163-p103">Chaque périphérique exécutant Windows 10 Entreprise peut bénéficier des avantages de la solution intégrée de Microsoft 365 Entreprise. Les autres périphériques exécutant Windows 7 ou Windows 8.1 ne peuvent pas utiliser les technologies associées au cloud, ni les fonctionnalités de sécurité avancée de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="01163-p103">Each device running Windows 10 Enterprise can participate in the benefits of the integrated solution of Microsoft 365 Enterprise. The remaining devices running Windows 7 or Windows 8.1 cannot use the cloud-connected technologies and advanced security features of Windows 10 Enterprise.</span></span>

<span data-ttu-id="01163-126">Si nécessaire, l’[Étape 2](windows10-deploy-inplaceupgrade.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="01163-126">If needed, [Step 2](windows10-deploy-inplaceupgrade.md) can help you with this requirement.</span></span>

<a name="crit-windows10-step3"></a>
## <a name="required-for-new-devices-configured-windows-autopilot"></a><span data-ttu-id="01163-127">Obligatoire pour les nouveaux périphériques : configuration de Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="01163-127">Required for new devices: Configured Windows Autopilot</span></span>

<span data-ttu-id="01163-128">Pour utiliser Windows Autopilot afin de déployer et de personnaliser Windows 10 Entreprise sur un nouveau périphérique, vous devez :</span><span class="sxs-lookup"><span data-stu-id="01163-128">To use Windows Autopilot to deploy and customize Windows 10 Enterprise on a new device, you must have:</span></span>

- <span data-ttu-id="01163-129">Configurer le niveau de données de diagnostic Windows approprié</span><span class="sxs-lookup"><span data-stu-id="01163-129">Set the proper Windows diagnostics data level</span></span>
- <span data-ttu-id="01163-130">Remplir les conditions préalables pour Windows Autopilot, qui incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="01163-130">Completed the prerequisites for Windows Autopilot, which include:</span></span>
   - <span data-ttu-id="01163-131">Inscription du périphérique et personnalisation OOBE</span><span class="sxs-lookup"><span data-stu-id="01163-131">Device registration and OOBE customization</span></span>
   - <span data-ttu-id="01163-132">Insertion de la marque de votre entreprise pour OOBE</span><span class="sxs-lookup"><span data-stu-id="01163-132">Company branding for OOBE</span></span>
   - <span data-ttu-id="01163-133">Inscription automatique de la gestion des appareils mobiles dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="01163-133">MDM auto-enrollment in Microsoft Intune</span></span>
   - <span data-ttu-id="01163-134">Connectivité réseau aux services cloud utilisés par Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="01163-134">Network connectivity to cloud services used by Windows Autopilot</span></span>
- <span data-ttu-id="01163-135">Pré-installation de Windows 10 version 1703 ou ultérieure sur les périphériques</span><span class="sxs-lookup"><span data-stu-id="01163-135">Devices must be pre-installed with Windows 10, version 1703 or later</span></span>
- <span data-ttu-id="01163-136">Sélection du programme de déploiement Windows Autopilot pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="01163-136">Selected the Windows Autopilot Deployment Program for your organization</span></span>

<span data-ttu-id="01163-137">Une fois la configuration de Windows Autopilot terminée, vous pouvez l’utiliser pour configurer et personnaliser Windows 10 Entreprise pour OOBE (out-of-the-box experience) pour :</span><span class="sxs-lookup"><span data-stu-id="01163-137">Once the Windows Autopilot configuration is in place, you can use it to configure and customize Windows 10 Enterprise for the out-of-the-box experience (OOBE) for:</span></span>

- <span data-ttu-id="01163-138">les nouveaux périphériques et</span><span class="sxs-lookup"><span data-stu-id="01163-138">New devices</span></span>
- <span data-ttu-id="01163-139">les périphériques qui ont déjà exécuté une configuration prédéfinie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="01163-139">Devices that have already completed an out-of-box setup in your organization.</span></span> 

<span data-ttu-id="01163-140">Windows Autopilot configure le périphérique et le connecte à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="01163-140">Windows Autopilot configures the device and connects it to Azure AD.</span></span>

<span data-ttu-id="01163-141">Sans Windows Autopilot, vous devez configurer manuellement les nouveaux périphériques, y compris la connexion à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="01163-141">Without Windows Autopilot, you must manually configure new devices, including the connection to Azure AD.</span></span>

<span data-ttu-id="01163-142">Si nécessaire, l’[Étape 3](windows10-deploy-autopilot.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="01163-142">If needed, [Step 3](windows10-deploy-autopilot.md) can help you with this requirement.</span></span>

<a name="crit-windows10-step4"></a>
## <a name="optional-you-are-using-windows-analytics-device-health-to-monitor-your-windows-10-enterprise-based-devices"></a><span data-ttu-id="01163-143">Facultatif : utilisation de la fonctionnalité d’intégrité de l’appareil Windows Analytics pour surveiller vos périphériques basés sur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="01163-143">Optional: You are using Windows Analytics Device Health to monitor your Windows 10 Enterprise-based devices</span></span>

<span data-ttu-id="01163-p104">Vous utilisez les informations de surveillance de l’intégrité des appareils pour détecter et solutionner les problèmes pouvant avoir une incidence sur les utilisateurs finaux. Résoudre rapidement les problèmes des utilisateurs permet de réduire vos coûts du support et de prouver à vos utilisateurs l’engagement de l’équipe informatique lié à Windows 10 Entreprise, ce qui permet de développer l’adoption au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="01163-p104">You used the information in Monitor the health of devices with Device Health to detect and remediate issues affecting end users. Quickly addressing end-user issues can reduce your support costs and demonstrate to your users the IT commitment to Windows 10 Enterprise, which can help drive adoption across your organization.</span></span> 

<span data-ttu-id="01163-146">Si nécessaire, l’[Étape 4](windows10-enable-windows-analytics.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="01163-146">If needed, [Step 4](windows10-enable-windows-analytics.md) can help you with this option.</span></span>

<a name="crit-windows10-step5a"></a>
## <a name="required-you-are-using-windows-defender-antivirus-or-your-own-antimalware-solution"></a><span data-ttu-id="01163-147">Obligatoire : utilisation de l’antivirus Windows Defender ou de votre propre solution anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="01163-147">Required: You are using Windows Defender Antivirus or your own antimalware solution</span></span>

<span data-ttu-id="01163-p105">Vous avez déployé l’antivirus Windows Defender ou votre propre solution antivirus pour protéger vos périphériques exécutant Windows 10 Entreprise contre les programmes malveillants. Si vous avez déployé l’antivirus Windows Defender, vous avez implémenté une méthode de création de rapports, telle que System Center Configuration Manager ou Microsoft Intune, pour surveiller l’activité et les événements antivirus.</span><span class="sxs-lookup"><span data-stu-id="01163-p105">You deployed Windows Defender Antivirus or your own antivirus solution to protect your devices running Windows 10 Enterprise from malicious software. If you deployed Windows Defender Antivirus, you have implemented a reporting method, such as System Center Configuration Manager or Microsoft Intune, to monitor antivirus events and activity.</span></span>

<span data-ttu-id="01163-150">Si nécessaire, l’[Étape 5](windows10-enable-security-features.md#windows10-sec-av) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="01163-150">If needed, [Step 5](windows10-enable-security-features.md#windows10-sec-av) can help you with this requirement.</span></span>

<a name="crit-windows10-step5b"></a>
## <a name="required-you-are-using-windows-defender-exploit-guard"></a><span data-ttu-id="01163-151">Obligatoire : utilisation de Windows Defender Exploit Guard</span><span class="sxs-lookup"><span data-stu-id="01163-151">Required: You are using Windows Defender Exploit Guard</span></span>

<span data-ttu-id="01163-152">Vous avez déployé Windows Defender Exploit Guard pour protéger vos périphériques exécutant Windows 10 Entreprise contre les intrusions et avez implémenté une méthode de création de rapports, telle que System Center Configuration Manager ou Microsoft Intune, pour surveiller les événements et l’activité liés aux intrusions.</span><span class="sxs-lookup"><span data-stu-id="01163-152">You deployed Windows Defender Exploit Guard to protect your devices running Windows 10 Enterprise from intrusion and have implemented a reporting method, such as System Center Configuration Manager or Microsoft Intune, to monitor intrusion events and activity.</span></span>

<span data-ttu-id="01163-153">Si nécessaire, l’[Étape 5](windows10-enable-security-features.md#windows10-sec-eg) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="01163-153">If needed, [Step 5](windows10-enable-security-features.md#windows10-sec-eg) can help you with this requirement.</span></span>

<a name="crit-windows10-step5c"></a>
## <a name="required-you-are-using-windows-defender-advanced-threat-protection-microsoft-365-enterprise-e5-only"></a><span data-ttu-id="01163-154">Obligatoire : utilisation du service Protection avancée contre les menaces Windows Defender (Microsoft 365 Entreprise E5 uniquement)</span><span class="sxs-lookup"><span data-stu-id="01163-154">Required: You are using Windows Defender Advanced Threat Protection (Microsoft 365 Enterprise E5 only)</span></span>

<span data-ttu-id="01163-155">Vous avez déployé le service Protection avancée contre les menaces Windows Defender (ATP) pour détecter, examiner et traiter les menaces avancées contre votre réseau et vos périphériques exécutant Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="01163-155">You deployed Windows Defender Advanced Threat Protection (ATP) to detect, investigate, and respond to advanced threats against your network and devices running Windows 10 Enterprise.</span></span> 

<span data-ttu-id="01163-156">Vous avez éventuellement intégré Windows Defender ATP à d’autres outils pour développer ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="01163-156">Optionally, you have integrated Windows Defender ATP with other tools to expand its capabilities.</span></span>

<span data-ttu-id="01163-157">Si nécessaire, l’[étape 5](windows10-enable-security-features.md#windows10-sec-atp) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="01163-157">If needed, [Step 5](windows10-enable-security-features.md#windows10-sec-atp) can help you with this requirement.</span></span>

## <a name="results-and-next-steps"></a><span data-ttu-id="01163-158">Tests et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="01163-158">Validation and next steps</span></span>

<span data-ttu-id="01163-159">Votre infrastructure Windows 10 Entreprise est prêt à commencer l’installation sur les nouveaux appareils et les mises à niveau sur place sur des appareils exécutant les versions précédentes de Windows et que vous utilisez les fonctionnalités de sécurité clés de Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="01163-159">Your Windows 10 Enterprise infrastructure is ready to begin installation on new devices and upgrades-in-place on devices running previous versions of Windows, and you are using the key security features of Windows 10 Enterprise.</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/O365proplus_icon-small.png)| <span data-ttu-id="01163-160">Si vous suivez les phases suivantes dans le processus de déploiement de bout en bout pour Microsoft 365 Entreprise, la suivante est la [Office 365 ProPlus](office365proplus-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="01163-160">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [Office 365 ProPlus](office365proplus-infrastructure.md).</span></span> |
