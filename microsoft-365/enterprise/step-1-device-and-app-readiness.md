---
title: 'Étape 1 : disponibilité des applications et des périphériques'
ms.author: jogruszc
author: JGruszczyk
manager: jemed
ms.date: 09/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Apprenez à évaluer la disponibilité des applications et des périphériques et dans l’environnement.
ms.openlocfilehash: a9fa85ea37de06399aa2264b09c61e588edc2107
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867487"
---
# <a name="step-1-device-and-app-readiness"></a><span data-ttu-id="341e3-103">Étape 1 : disponibilité des applications et des périphériques</span><span class="sxs-lookup"><span data-stu-id="341e3-103">Step 1: Device and App Readiness</span></span>

<span data-ttu-id="341e3-104">Commencez votre projet de déploiement d’ordinateurs de bureau par un inventaire de vos périphériques et applications, puis classez-les par ordre de priorité. Testez les périphériques et les applications privilégiés, puis faites les corrections nécessaires en vue du déploiement.</span><span class="sxs-lookup"><span data-stu-id="341e3-104">Begin your desktop deployment project with an inventory of your devices and apps, prioritize what you to move forward, test prioritized apps and devices, then remediate what’s needed to get ready for deployment.</span></span>

![](media/step-1-device-and-app-readiness-media/step-1-device-and-app-readiness-media-1.png)

<table>
<thead>
<td><img src="media/desktop-deployment-center-home-media/desktop-deployment-center-home-media-3.png" alt="Step 1" height="130" width="130" /></td>
<td><p><span data-ttu-id="341e3-105"><strong>Étape 1 : disponibilité des applications et des périphériques</strong></span><span class="sxs-lookup"><span data-stu-id="341e3-105"><strong>Step 1: Device and App Readiness</strong></span></span></p>
<p><span data-ttu-id="341e3-106">Commencez votre projet de déploiement d’ordinateurs de bureau par un inventaire de vos périphériques et applications, puis classez-les par ordre de priorité. Testez les périphériques et les applications privilégiés, puis faites les corrections nécessaires en vue du déploiement.</span><span class="sxs-lookup"><span data-stu-id="341e3-106">Begin your desktop deployment project with an inventory of your devices and apps, prioritize what you to move forward, test prioritized apps and devices, then remediate what’s needed to get ready for deployment.</span></span></p></td>
<td><a href="https://aka.ms/ddev1" target="_blank"><img src="media/desktop-deployment-center-home-media/desktop-deployment-center-home-media-14.png" alt="Step 1" height="120" width="213" /></a></td>
</thead>
</table>

>[!NOTE]
><span data-ttu-id="341e3-p101">La disponibilité des applications et des périphériques est la première étape de notre processus de déploiement recommandé en couvrant les aspects holistiques de la compatibilité du matériel et des applications. Pour afficher l’ensemble du processus de déploiement d’ordinateurs de bureau, visitez le [centre de déploiement moderne d’ordinateurs de bureau](https://aka.ms/HowToShift).</span><span class="sxs-lookup"><span data-stu-id="341e3-p101">Device and App Readiness is the first step in our recommended deployment process wheel by covering the holistic aspects of application and hardware compatibility. To see the full desktop deployment process, visit the [Modern Desktop Deployment Center](https://aka.ms/HowToShift).</span></span>
>

<span data-ttu-id="341e3-p102">La compatibilité du matériel et des applications était autrefois un obstacle majeur à la mise à niveau des ordinateurs de bureau des utilisateurs. La bonne nouvelle lorsque vous planifiez votre déploiement vers Windows 10 et Office 365 ProPlus est que la grande majorité des applications créées au cours des 10 dernières années s’exécute sur Windows 10, et les compléments COM et les macros VBA utilisés par votre organisation sur les versions d’Office remontant jusqu’à Office 2010 continueront de fonctionner avec les dernières versions d’Office, sans modification.</span><span class="sxs-lookup"><span data-stu-id="341e3-p102">In the past, a major hurdle to upgrading the users’ desktops is application and hardware compatibility. The good news as you plan your shift to Windows 10 and Office 365 ProPlus, is just about any application written in the last 10 years will run on Windows 10, and any COM add-ins and VBA macros your organization used on versions of Office dating back to Office 2010, will continue to work on the latest versions of Office, without modification.</span></span>

<span data-ttu-id="341e3-111">Cela étant dit, selon la taille et l’âge de votre organisation, vérifier la compatibilité du matériel et des applications est probablement toujours une étape essentielle initiale de notre processus de déploiement de 8 étapes recommandé.</span><span class="sxs-lookup"><span data-stu-id="341e3-111">That said, depending on the size and age of your organization, verifying application and hardware compatibility is likely still an essential initial step in our recommended 8-phase deployment process.</span></span>

<span data-ttu-id="341e3-112">Dans cet article, nous vous présentons cette première phase (disponibilité des applications et des périphériques) utilisant le nouvel outil de préparation de mise à niveau Windows Analytics, une solution informatique intelligente livrée avec votre licence Windows.</span><span class="sxs-lookup"><span data-stu-id="341e3-112">In this article we take you through that first phase – Device and App Readiness – using the new Windows Analytics Upgrade Readiness tool, an intelligent cloud-based solution available with your Windows license.</span></span>

<span data-ttu-id="341e3-113">Si Windows Analytics n’est actuellement pas configuré pour votre environnement ou si vous souhaitez télécharger une version d’évaluation, accédez à la [page Windows Analytics](http://www.aka.ms/windowsanalytics) et lancez-vous.</span><span class="sxs-lookup"><span data-stu-id="341e3-113">If you don’t currently have Windows Analytics set up for your environment or would like to sign up for a trial, go the [Windows Analytics page](http://www.aka.ms/windowsanalytics) and get started.</span></span>

## <a name="recommended-tool-windows-analytics-upgrade-readiness"></a><span data-ttu-id="341e3-114">Outil recommandé : préparation de mise à niveau Windows Analytics</span><span class="sxs-lookup"><span data-stu-id="341e3-114">Recommended Tool: Windows Analytics Upgrade Readiness</span></span>

<span data-ttu-id="341e3-p103">L’outil de préparation de mise à niveau Windows Analytics offre de nombreux avantages par rapport aux systèmes de gestion d’ordinateurs de bureau classiques. C’est l’outil que nous recommandons. Il est sans agent ; il vous guide à travers les actions à exécuter ; et il utilise les informations de compatibilité du pilote et des applications recueillies via la mise à niveau de centaines de millions de PC grand public, afin de vous offrir une évaluation détaillée, identifiant les problèmes de compatibilité qui peuvent empêcher la mise à niveau avec des liens vers les correctifs suggérés et connus par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="341e3-p103">Windows Analytics Upgrade Readiness offers many advantages over traditional desktop management systems and is our recommended tool. It is agentless; it guides you through what needs to be done; and, it makes use of application and driver compatibility information gathered through the upgrade of hundreds of millions of consumer PCs, to give you a detailed assessment, identifying compatibility issues that might block your upgrade, with links to suggested fixes known to Microsoft.</span></span>

<span data-ttu-id="341e3-p104">Pour configurer l’outil de préparation de mise à niveau Windows Analytics, vous devez tout d’abord configurer un abonnement Azure et y inclure un espace de travail Azure Log Analytics. Une fois que le service de préparation de mise à niveau Windows Analytics est en cours d’exécution, vous pouvez inscrire n’importe quel périphérique connecté à Internet et exécutant Windows 7 SP1 ou une version plus récente via les paramètres de stratégie de groupe. C’est aussi simple que cela. Il n’y a aucun agent à déployer et le flux de travail visuel de l’outil de préparation de mise à niveau Windows Analytics vous guide du pilote au déploiement en production. Si vous le souhaitez, vous pouvez exporter des données de l’outil de préparation de mise à niveau Windows Analytics vers des outils de déploiement de logiciels tels que System Center Configuration Manager, directement vers des PC cibles et créer des collections de sites dès que celles-ci sont prêtes pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="341e3-p104">To set up Window Analytics Upgrade Readiness you’ll first need to set up an Azure subscription and include an Azure Log Analytics workspace to that. Once you have the Windows Analytics Upgrade Readiness service running, you can then enroll any Internet-connected Windows 7 SP1 or newer device via Group Policy settings. It’s that simple. There are no agents to deploy, and Windows Analytics Upgrade Readiness’s visual workflow guides you from pilot to production deployment. If you wish, you can export data from Windows Analytics Upgrade Readiness to software deployment tools such as System Center Configuration Manager, to target PCs directly and build collections as they become ready for deployment.</span></span>

## <a name="device-and-app-readiness-process"></a><span data-ttu-id="341e3-122">Processus de disponibilité des applications et des périphériques</span><span class="sxs-lookup"><span data-stu-id="341e3-122">Device and App Readiness Process</span></span>

<span data-ttu-id="341e3-p105">La disponibilité des applications et des périphériques comprend quatre étapes : 1. Inventaire, 2. Hiérarchisation, 3. Test et 4. Mesures correctives. Examinons chacune d’entre elles.</span><span class="sxs-lookup"><span data-stu-id="341e3-p105">Device and App Readiness compromises four steps: 1. Inventory, 2. Prioritize, 3. Test, 4. Remediate. Let’s look at each of these in turn.</span></span>

### <a name="1-inventory"></a><span data-ttu-id="341e3-p106">1\. Inventaire</span><span class="sxs-lookup"><span data-stu-id="341e3-p106">1\. Inventory</span></span>

<span data-ttu-id="341e3-131">Le service de préparation de mise à niveau Windows Analytics utilise un processus sans agent pour faire l’inventaire des ordinateurs, des applications et des compléments Office au sein de votre parc d’ordinateurs de bureau.</span><span class="sxs-lookup"><span data-stu-id="341e3-131">Windows Analytics Upgrade Readiness service uses an agent-less process to inventory the computers, applications and Office add-ins across your desktop estate.</span></span>

![](media/step-1-device-and-app-readiness-media/step-1-device-and-app-readiness-media-3.png)

<span data-ttu-id="341e3-132">Il fournit également des rapports sur les applications et les sites Internet très régulièrement consultés, et les emplacements intranet pour vous aider avec les tests de compatibilité ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="341e3-132">It also provides reports on highly visited Internet sites, apps and Intranet locations to help you with compatibility testing later.</span></span>

![](media/step-1-device-and-app-readiness-media/step-1-device-and-app-readiness-media-4.png)

### <a name="2-prioritize"></a><span data-ttu-id="341e3-p107">2\. Hiérarchisation</span><span class="sxs-lookup"><span data-stu-id="341e3-p107">2\. Prioritize</span></span>

<span data-ttu-id="341e3-135">Avec l’inventaire, l’outil de préparation de mise à niveau Windows Analytics vous aide à identifier et à hiérarchiser les applications et le matériel les plus fréquemment utilisés dans votre organisation et les tâches à prioriser pour débloquer autant de PC que possible pour le déploiement,</span><span class="sxs-lookup"><span data-stu-id="341e3-135">With inventory taken, Windows Analytics Upgrade Readiness helps you to identify and prioritize the most common apps and hardware used in your organization, and what to focus on to unblock as many PCs as possible for deployment,</span></span>

![](media/step-1-device-and-app-readiness-media/step-1-device-and-app-readiness-media-5.png)

<span data-ttu-id="341e3-136">en fournissant également des conseils pour vous aider à évaluer les mises à jour nécessaires pour résoudre les problèmes lors de l’étape suivante : test.</span><span class="sxs-lookup"><span data-stu-id="341e3-136">also providing guidance to help you assess the updates are necessary to resolve issues during the next step: testing.</span></span>

### <a name="3-testing"></a><span data-ttu-id="341e3-p108">3\. Test</span><span class="sxs-lookup"><span data-stu-id="341e3-p108">3\. Testing</span></span>

<span data-ttu-id="341e3-p109">Vous constaterez que la plupart des applications, des pilotes et des compléments répertoriés fonctionnent tel quel. Pour les éléments pour lesquels l’outil de préparation de mise à niveau Windows Analytics a identifié des problèmes, cet outil vous fournit des informations connues, notamment où trouver des mises à jour de version pour résoudre les problèmes de compatibilité. Au lieu de consacrer du temps et des ressources à tenter de résoudre des problèmes complexes sur des applications non essentielles, des applications faiblement déployées et des périphériques plus anciens, invitez les utilisateurs à retirer et à remplacer ces éléments.</span><span class="sxs-lookup"><span data-stu-id="341e3-p109">You will find that most of the applications, drivers, and add-ins inventoried, will work as-is. For items Windows Analytics Upgrade Readiness assesses to have issues, it provides you with known information, including where to find version updates to resolve compatibility problems. Rather than devoting time and resource resolving complex issues in non-critical, sparsely deployed applications and older devices, you may choose instead to work with users to retire and replace these items.</span></span>

<span data-ttu-id="341e3-p110">Vous pouvez aussi utiliser l’outil de préparation de mise à niveau Windows Analytics pour évaluer les problèmes de compatibilité sur navigateur, identifier les applications et sites web consultés par les utilisateurs utilisant encore les contrôles ActiveX, Browser Helper Objects, VBScript ou d’autres technologies héritées non prises en charge par le navigateur Microsoft Edge. Les utilisateurs devront quand même utiliser Internet Explorer 11 pour ces sites et vous pouvez les ajouter à la [liste de sites du mode Entreprise](https://docs.microsoft.com/fr-FR/microsoft-edge/deploy/emie-to-improve-compatibility) à l’aide du gestionnaire de listes de sites du mode Entreprise.</span><span class="sxs-lookup"><span data-stu-id="341e3-p110">You can use Windows Analytics Upgrade Readiness to assess browser-based compatibility issues too, identifying websites and web apps accessed by users still using ActiveX controls, Browser Helper Objects, VBScript, or other legacy technology not supported by the Microsoft Edge browser. Your users will still need to use Internet Explorer 11 for these sites, and you can add them to the [Enterprise Mode site list](https://docs.microsoft.com/fr-FR/microsoft-edge/deploy/emie-to-improve-compatibility), using the Enterprise Mode Site List Manager.</span></span>

<span data-ttu-id="341e3-144">En outre, pour vous aider dans votre migration vers Office 365 ProPlus, vous pouvez utiliser le [Kit de ressources de préparation pour Office](https://docs.microsoft.com/fr-FR/deployoffice/use-the-readiness-toolkit-to-assess-application-compatibility-for-office-365-pro) pour tester la compatibilité de vos compléments et des macros Microsoft Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="341e3-144">Additionally, to assist in your move to Office 365 ProPlus, you may wish to make use of the [Readiness Toolkit for Office](https://docs.microsoft.com/fr-FR/deployoffice/use-the-readiness-toolkit-to-assess-application-compatibility-for-office-365-pro) to test the compatibility of your add-ins and Microsoft Visual Basic for Applications (VBA) macros.</span></span>

![](media/step-1-device-and-app-readiness-media/step-1-device-and-app-readiness-media-6.png)

### <a name="4-remediation"></a><span data-ttu-id="341e3-p111">4\. Mesures correctives</span><span class="sxs-lookup"><span data-stu-id="341e3-p111">4\. Remediation</span></span>

<span data-ttu-id="341e3-p112">La phase finale de la disponibilité des applications et des périphériques consiste à « corriger ». Ici, vous allez collecter les packages de pilotes et de logiciels requis et vous allez les utiliser pour remplacer ou mettre à jour les versions antérieures dans le cadre du processus de déploiement.</span><span class="sxs-lookup"><span data-stu-id="341e3-p112">As the final phase of device and app readiness is to ‘remediate’. Here you’ll want to collect the required software or driver packages; you are going to use these to supersede or update older versions as part of the deployment process.</span></span>

![](media/step-1-device-and-app-readiness-media/step-1-device-and-app-readiness-media-7.png)

<span data-ttu-id="341e3-p113">À mesure que vous avancez dans la liste et que vous corrigez les problèmes, vous observez que de plus en plus de PC deviennent « Prêt pour le déploiement ». Cela signifie que les pilotes et les applications sur les PC sont indiqués comme étant compatibles avec la version de Windows 10 que vous ciblez pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="341e3-p113">As you work through the list remediating issues, you’ll see that more and more PCs become “Ready for Deployment”. This means that both the drivers and apps on the PCs are noted as compatible with the version of Windows 10 you are targeting for deployment.</span></span>

## <a name="continued-use-of-telemetry-tools"></a><span data-ttu-id="341e3-151">Utilisation en continu des outils de télémétrie</span><span class="sxs-lookup"><span data-stu-id="341e3-151">Continued use of telemetry tools</span></span>

<span data-ttu-id="341e3-p114">L’outil de préparation de mise à niveau Windows Analytics n’est pas simplement un outil pour migrer vers Windows 10 et Office 365 ProPlus. Une fois que vos ordinateurs de bureau exécutent Windows 10 et Office 365, vous pouvez l’utiliser pour vous aider à maintenir votre déploiement et à gérer les mises à jour de fonctionnalités semi-annuelles afin de rester à jour.</span><span class="sxs-lookup"><span data-stu-id="341e3-p114">Windows Analytics Upgrade Readiness isn’t just a tool to help you shift to Windows 10 and Office 365 ProPlus. Once you have desktops running on Windows 10 and Office 365 you can use it to help maintain your deployment and manage semi-annual Feature Updates so that you can stay current.</span></span>

## <a name="next-step"></a><span data-ttu-id="341e3-154">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="341e3-154">Next Step</span></span> 

## <a name="step-2-directory-and-network-readinesshttpsakamsmdd2"></a>[<span data-ttu-id="341e3-155">Étape 2 : disponibilité des répertoires et des réseaux</span><span class="sxs-lookup"><span data-stu-id="341e3-155">Step 2: Directory and Network Readiness</span></span>](https://aka.ms/mdd2)