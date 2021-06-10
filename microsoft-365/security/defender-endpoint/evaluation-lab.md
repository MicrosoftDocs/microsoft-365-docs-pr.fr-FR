---
title: Laboratoire d’évaluation de Microsoft Defender for Endpoint
description: Découvrez les fonctionnalités de Microsoft Defender pour les points de terminaison, exécutez des simulations d’attaques et découvrez comment il empêche, détecte et remédie aux menaces.
keywords: évaluer Microsoft Defender pour le point de terminaison, évaluation, laboratoire, simulation, windows 10, windows server 2019, laboratoire d’évaluation
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-evalutatemtp
ms.topic: article
ms.technology: mde
ms.openlocfilehash: c785dbb759afe77b14f41985b9f451a4ec52e29f
ms.sourcegitcommit: 83df0be7144c9c5d606f70b4efa65369e86693d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52778232"
---
# <a name="microsoft-defender-for-endpoint-evaluation-lab"></a><span data-ttu-id="30aa6-104">Laboratoire d’évaluation de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="30aa6-104">Microsoft Defender for Endpoint evaluation lab</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="30aa6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="30aa6-105">**Applies to:**</span></span>
- [<span data-ttu-id="30aa6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="30aa6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="30aa6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="30aa6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="30aa6-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="30aa6-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="30aa6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="30aa6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)


<span data-ttu-id="30aa6-110">La conduite d’une évaluation complète du produit de sécurité peut être un processus complexe nécessitant une configuration fastidieuse de l’environnement et de l’appareil avant qu’une simulation d’attaque de bout en bout puisse réellement être effectuée.</span><span class="sxs-lookup"><span data-stu-id="30aa6-110">Conducting a comprehensive security product evaluation can be a complex process requiring cumbersome environment and device configuration before an end-to-end attack simulation can actually be done.</span></span> <span data-ttu-id="30aa6-111">L’ajout de la complexité est la difficulté de suivre l’endroit où les activités de simulation, les alertes et les résultats sont reflétés au cours de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-111">Adding to the complexity is the challenge of tracking where the simulation activities, alerts, and results are reflected during the evaluation.</span></span>

<span data-ttu-id="30aa6-112">Le laboratoire d’évaluation de Microsoft Defender pour points de terminaison est conçu pour éliminer la complexité de la configuration des appareils et de l’environnement afin de pouvoir vous concentrer sur l’évaluation des fonctionnalités de la plateforme, l’exécution de simulations et l’utilisation des fonctionnalités de prévention, de détection et de correction.</span><span class="sxs-lookup"><span data-stu-id="30aa6-112">The Microsoft Defender for Endpoint evaluation lab is designed to eliminate the complexities of device and environment configuration so that you can  focus on evaluating the capabilities of the platform, running simulations, and seeing the prevention, detection, and remediation features in action.</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4qLUM]

<span data-ttu-id="30aa6-113">Grâce à l’expérience de mise en place simplifiée, vous pouvez vous concentrer sur l’exécution de vos propres scénarios de test et des simulations pré-réalisées pour voir les résultats de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="30aa6-113">With the simplified set-up experience, you can focus on running your own test scenarios and the pre-made simulations to see how Defender for Endpoint performs.</span></span> 

<span data-ttu-id="30aa6-114">Vous disposez d’un accès complet aux fonctionnalités puissantes de la plateforme, telles que les enquêtes automatisées, le recherche avancée et l’analyse des menaces, ce qui vous permet de tester la pile de protection complète de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="30aa6-114">You'll have full access to the powerful capabilities of the platform such as automated investigations, advanced hunting, and threat analytics, allowing you to test the comprehensive protection stack that Defender for Endpoint offers.</span></span> 

<span data-ttu-id="30aa6-115">Vous pouvez ajouter des appareils Windows 10 ou Windows Server 2019 pré-configurés pour que les versions de système d’exploitation les plus récentes et les composants de sécurité en place, ainsi que Office 2019 Standard soit installé.</span><span class="sxs-lookup"><span data-stu-id="30aa6-115">You can add Windows 10 or Windows Server 2019 devices that come pre-configured to have the latest OS versions and the right security components in place as well as Office 2019 Standard installed.</span></span>

<span data-ttu-id="30aa6-116">Vous pouvez également installer des simulateurs de menaces.</span><span class="sxs-lookup"><span data-stu-id="30aa6-116">You can also install threat simulators.</span></span> <span data-ttu-id="30aa6-117">Defender pour le point de terminaison s’est associé à des plateformes de simulation de menaces de pointe pour vous aider à tester les fonctionnalités de Defender for Endpoint sans avoir à quitter le portail.</span><span class="sxs-lookup"><span data-stu-id="30aa6-117">Defender for Endpoint has partnered with industry leading threat simulation platforms to help you test out the Defender for Endpoint capabilities without having to leave the portal.</span></span>

 <span data-ttu-id="30aa6-118">Installez votre simulateur préféré, exécutez des scénarios dans le laboratoire d’évaluation et voyez instantanément les résultats de la plateforme, le tout disponible sans frais supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="30aa6-118">Install your preferred simulator, run scenarios within the evaluation lab, and instantly see how the platform performs - all conveniently available at no extra cost to you.</span></span> <span data-ttu-id="30aa6-119">Vous aurez également un accès pratique à un large éventail de simulations que vous pouvez accéder et exécuter à partir du catalogue de simulations.</span><span class="sxs-lookup"><span data-stu-id="30aa6-119">You'll also have convenient access to wide array of simulations which you can access and run from the simulations catalog.</span></span>
    

## <a name="before-you-begin"></a><span data-ttu-id="30aa6-120">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="30aa6-120">Before you begin</span></span>
<span data-ttu-id="30aa6-121">Vous devez satisfaire [](minimum-requirements.md#licensing-requirements) aux exigences de licence ou avoir accès en version d’évaluation à Microsoft Defender for Endpoint pour accéder au laboratoire d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-121">You'll need to fulfill the [licensing requirements](minimum-requirements.md#licensing-requirements) or have trial access to Microsoft Defender for Endpoint to access the evaluation lab.</span></span>

<span data-ttu-id="30aa6-122">Vous devez avoir **les autorisations Gérer les paramètres** de sécurité pour :</span><span class="sxs-lookup"><span data-stu-id="30aa6-122">You must have **Manage security settings** permissions to:</span></span>
- <span data-ttu-id="30aa6-123">Créer l’atelier</span><span class="sxs-lookup"><span data-stu-id="30aa6-123">Create the lab</span></span>
- <span data-ttu-id="30aa6-124">Créer des appareils</span><span class="sxs-lookup"><span data-stu-id="30aa6-124">Create devices</span></span>
- <span data-ttu-id="30aa6-125">Réinitialiser le mot de passe</span><span class="sxs-lookup"><span data-stu-id="30aa6-125">Reset password</span></span>
- <span data-ttu-id="30aa6-126">Créer des simulations</span><span class="sxs-lookup"><span data-stu-id="30aa6-126">Create simulations</span></span> 
 
<span data-ttu-id="30aa6-127">Si vous avez activé le contrôle d’accès basé sur un rôle (RBAC) et créé au moins un groupe d’ordinateurs, les utilisateurs doivent avoir accès à tous les groupes d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="30aa6-127">If you enabled role-based access control (RBAC) and created at least a one machine group, users must have access to All machine groups.</span></span>

<span data-ttu-id="30aa6-128">Pour plus d’informations, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="30aa6-128">For more information, see [Create and manage roles](user-roles.md).</span></span>

<span data-ttu-id="30aa6-129">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="30aa6-129">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="30aa6-130">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="30aa6-130">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-main-abovefoldlink)


## <a name="get-started-with-the-lab"></a><span data-ttu-id="30aa6-131">Mise en place de l’atelier</span><span class="sxs-lookup"><span data-stu-id="30aa6-131">Get started with the lab</span></span>
<span data-ttu-id="30aa6-132">Vous pouvez accéder à l’atelier à partir du menu.</span><span class="sxs-lookup"><span data-stu-id="30aa6-132">You can access the lab from the menu.</span></span> <span data-ttu-id="30aa6-133">Dans le menu de navigation, sélectionnez **Évaluation et didacticiels > laboratoire d’évaluation.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-133">In the navigation menu, select **Evaluation and tutorials > Evaluation lab**.</span></span>

![Image de l’atelier d’évaluation dans le menu](images/evaluation-lab-menu.png)

>[!NOTE]
>- <span data-ttu-id="30aa6-135">Selon le type de structure d’environnement que vous sélectionnez, les appareils seront disponibles pour le nombre d’heures spécifié à partir du jour de l’activation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-135">Depending the type of environment structure you select, devices will be available for the specified number of hours from the day of activation.</span></span>
>- <span data-ttu-id="30aa6-136">Chaque environnement est mis en service avec un ensemble limité de périphériques de test.</span><span class="sxs-lookup"><span data-stu-id="30aa6-136">Each environment is provisioned with a limited set of test devices.</span></span> <span data-ttu-id="30aa6-137">Lorsque vous avez utilisé les appareils mis en service et que vous les avez supprimés, vous pouvez demander d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="30aa6-137">When you've used up the provisioned devices and have deleted them, you can request for more devices.</span></span> 
>- <span data-ttu-id="30aa6-138">Vous pouvez demander des ressources d’atelier une fois par mois.</span><span class="sxs-lookup"><span data-stu-id="30aa6-138">You can request for lab resources once a month.</span></span> 

<span data-ttu-id="30aa6-139">Vous avez déjà un atelier ?</span><span class="sxs-lookup"><span data-stu-id="30aa6-139">Already have a lab?</span></span> <span data-ttu-id="30aa6-140">Veillez à activer les nouveaux simulateurs de menaces et à avoir des appareils actifs.</span><span class="sxs-lookup"><span data-stu-id="30aa6-140">Make sure to enable the new threat simulators and have active devices.</span></span>

## <a name="setup-the-evaluation-lab"></a><span data-ttu-id="30aa6-141">Configurer le laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="30aa6-141">Setup the evaluation lab</span></span>

1. <span data-ttu-id="30aa6-142">Dans le volet de navigation, sélectionnez **Évaluation et didacticiels**  >  **Laboratoire** d’évaluation, puis sélectionnez **Laboratoire d’installation.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-142">In the navigation pane, select **Evaluation and tutorials** > **Evaluation lab**, then select **Setup lab**.</span></span>

    ![Image de la page d’accueil du laboratoire d’évaluation](images/evaluation-lab-setup.png)

2. <span data-ttu-id="30aa6-144">En fonction de vos besoins d’évaluation, vous pouvez choisir de configurer un environnement avec moins d’appareils pendant une période plus longue ou plus d’appareils sur une période plus courte.</span><span class="sxs-lookup"><span data-stu-id="30aa6-144">Depending on your evaluation needs, you can choose to setup an environment with fewer devices for a longer period or more devices for a shorter period.</span></span> <span data-ttu-id="30aa6-145">Sélectionnez votre configuration d’atelier préférée, puis **sélectionnez Suivant.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-145">Select your preferred lab configuration then select **Next**.</span></span>

    ![Image des options de configuration de l’atelier](images/lab-creation-page.png) 


3. <span data-ttu-id="30aa6-147">(Facultatif) Vous pouvez choisir d’installer des simulateurs de menaces dans l’atelier.</span><span class="sxs-lookup"><span data-stu-id="30aa6-147">(Optional) You can choose to install threat simulators in the lab.</span></span> 

    ![Image de l’agent des simulateurs d’installation](images/install-agent.png)

    >[!IMPORTANT]
    ><span data-ttu-id="30aa6-149">Vous devez d’abord accepter et donner votre consentement aux conditions générales et aux déclarations de partage d’informations.</span><span class="sxs-lookup"><span data-stu-id="30aa6-149">You'll first need to accept and provide consent to the terms and information sharing statements.</span></span> 

4. <span data-ttu-id="30aa6-150">Sélectionnez l’agent de simulation de menace que vous souhaitez utiliser et entrez vos détails.</span><span class="sxs-lookup"><span data-stu-id="30aa6-150">Select the threat simulation agent you'd like to use and enter your details.</span></span> <span data-ttu-id="30aa6-151">Vous pouvez également choisir d’installer des simulateurs de menaces ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="30aa6-151">You can also choose to install threat simulators at a later time.</span></span> <span data-ttu-id="30aa6-152">Si vous choisissez d’installer des agents de simulation de menace lors de l’installation de l’atelier, vous profitez de leur installation pratique sur les appareils que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="30aa6-152">If you choose to install threat simulation agents during the lab setup, you'll enjoy the benefit of having them conveniently installed on the devices you add.</span></span>  
    
    ![Image de la page récapitulatif](images/lab-setup-summary.png)

5.  <span data-ttu-id="30aa6-154">Examinez le résumé et sélectionnez **Le laboratoire d’installation.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-154">Review the summary and select **Setup lab**.</span></span>  

<span data-ttu-id="30aa6-155">Une fois le processus de configuration de l’atelier terminé, vous pouvez ajouter des appareils et exécuter des simulations.</span><span class="sxs-lookup"><span data-stu-id="30aa6-155">After the lab setup process is complete, you can add devices and run simulations.</span></span> 


## <a name="add-devices"></a><span data-ttu-id="30aa6-156">Ajouter des appareils</span><span class="sxs-lookup"><span data-stu-id="30aa6-156">Add devices</span></span>
<span data-ttu-id="30aa6-157">Lorsque vous ajoutez un appareil à votre environnement, Defender pour le point de terminaison configure un appareil bien configuré avec des détails de connexion.</span><span class="sxs-lookup"><span data-stu-id="30aa6-157">When you add a device to your environment, Defender for Endpoint sets up a well-configured device with connection details.</span></span> <span data-ttu-id="30aa6-158">Vous pouvez ajouter des Windows 10 ou des Windows server 2019.</span><span class="sxs-lookup"><span data-stu-id="30aa6-158">You can add Windows 10 or Windows Server 2019 devices.</span></span>

<span data-ttu-id="30aa6-159">L’appareil sera configuré avec la version la plus récente du système d’exploitation et de Office 2019 Standard, ainsi que d’autres applications telles que Java, Python et SysIntenals.</span><span class="sxs-lookup"><span data-stu-id="30aa6-159">The device will be configured with the most up-to-date version of the OS and Office 2019 Standard as well as other apps such as Java, Python, and SysIntenals.</span></span> 

<span data-ttu-id="30aa6-160">Si vous avez choisi d’ajouter un simulateur de menaces lors de l’installation de l’atelier, l’agent de simulateur de menaces sera installé sur tous les appareils que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="30aa6-160">If you chose to add a threat simulator during the lab setup, all devices will have the threat simulator agent installed in the devices that you add.</span></span>

<span data-ttu-id="30aa6-161">L’appareil est automatiquement intégré à votre client avec les composants de sécurité Windows recommandés, qui sont allumés et en mode audit, sans aucun effort de votre part.</span><span class="sxs-lookup"><span data-stu-id="30aa6-161">The device will automatically be onboarded to your tenant with the recommended Windows security components turned on and in audit mode - with no effort on your side.</span></span> 

<span data-ttu-id="30aa6-162">Les composants de sécurité suivants sont pré-configurés dans les périphériques de test :</span><span class="sxs-lookup"><span data-stu-id="30aa6-162">The following security components are pre-configured in the test devices:</span></span>

- [<span data-ttu-id="30aa6-163">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="30aa6-163">Attack surface reduction</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard)
- [<span data-ttu-id="30aa6-164">Bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="30aa6-164">Block at first sight</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-block-at-first-sight-microsoft-defender-antivirus)
- [<span data-ttu-id="30aa6-165">Accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="30aa6-165">Controlled folder access</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/controlled-folders-exploit-guard)
- [<span data-ttu-id="30aa6-166">Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="30aa6-166">Exploit protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/enable-exploit-protection)
- [<span data-ttu-id="30aa6-167">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="30aa6-167">Network protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/network-protection-exploit-guard)
- [<span data-ttu-id="30aa6-168">Détection d’applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="30aa6-168">Potentially unwanted application detection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus)
- [<span data-ttu-id="30aa6-169">Protection cloud</span><span class="sxs-lookup"><span data-stu-id="30aa6-169">Cloud-delivered protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/utilize-microsoft-cloud-protection-microsoft-defender-antivirus)
- [<span data-ttu-id="30aa6-170">Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="30aa6-170">Microsoft Defender SmartScreen</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)

>[!NOTE]
> <span data-ttu-id="30aa6-171">Antivirus Microsoft Defender sera en cours (pas en mode audit).</span><span class="sxs-lookup"><span data-stu-id="30aa6-171">Microsoft Defender Antivirus will be on (not in audit mode).</span></span> <span data-ttu-id="30aa6-172">Si Antivirus Microsoft Defender vous empêche d’utiliser votre simulation, vous pouvez désactiver la protection en temps réel sur l’appareil via Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="30aa6-172">If Microsoft Defender Antivirus blocks you from running your simulation, you can turn off real-time protection on the device through Windows Security.</span></span> <span data-ttu-id="30aa6-173">Pour plus d’informations, [voir Configure always-on protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus).</span><span class="sxs-lookup"><span data-stu-id="30aa6-173">For more information, see [Configure always-on protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus).</span></span>

<span data-ttu-id="30aa6-174">Les paramètres d’examen automatisé dépendent des paramètres du client.</span><span class="sxs-lookup"><span data-stu-id="30aa6-174">Automated investigation settings will be dependent on tenant settings.</span></span> <span data-ttu-id="30aa6-175">Elle sera configurée pour être semi-automatisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="30aa6-175">It will be configured to be semi-automated by default.</span></span> <span data-ttu-id="30aa6-176">Pour plus d’informations, voir [Vue d’ensemble des enquêtes automatisées.](automated-investigations.md)</span><span class="sxs-lookup"><span data-stu-id="30aa6-176">For more information, see [Overview of Automated investigations](automated-investigations.md).</span></span>

>[!NOTE]
><span data-ttu-id="30aa6-177">La connexion aux périphériques de test est effectuée à l’aide de RDP.</span><span class="sxs-lookup"><span data-stu-id="30aa6-177">The connection to the test devices is done using RDP.</span></span> <span data-ttu-id="30aa6-178">Assurez-vous que vos paramètres de pare-feu autorisent les connexions RDP.</span><span class="sxs-lookup"><span data-stu-id="30aa6-178">Make sure that your firewall settings allow RDP connections.</span></span>

1. <span data-ttu-id="30aa6-179">Dans le tableau de bord, **sélectionnez Ajouter un appareil.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-179">From the dashboard, select **Add device**.</span></span> 

2. <span data-ttu-id="30aa6-180">Choisissez le type d’appareil à ajouter.</span><span class="sxs-lookup"><span data-stu-id="30aa6-180">Choose the type of device to add.</span></span> <span data-ttu-id="30aa6-181">Vous pouvez choisir d’ajouter Windows 10 ou Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="30aa6-181">You can choose to add Windows 10 or Windows Server 2019.</span></span>

    ![Image de la configuration de l’atelier avec les options d’appareil](images/add-machine-options.png)


    >[!NOTE]
    ><span data-ttu-id="30aa6-183">En cas de problème lors du processus de création de l’appareil, vous serez averti et vous devrez envoyer une nouvelle demande.</span><span class="sxs-lookup"><span data-stu-id="30aa6-183">If something goes wrong with the device creation process, you'll be notified and you'll need to submit a new request.</span></span> <span data-ttu-id="30aa6-184">Si la création de l’appareil échoue, elle n’est pas comptabilisée dans le quota autorisé global.</span><span class="sxs-lookup"><span data-stu-id="30aa6-184">If the device creation fails, it will not be counted against the overall allowed quota.</span></span> 

3. <span data-ttu-id="30aa6-185">Les détails de connexion sont affichés.</span><span class="sxs-lookup"><span data-stu-id="30aa6-185">The connection details are displayed.</span></span> <span data-ttu-id="30aa6-186">Sélectionnez **Copier** pour enregistrer le mot de passe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30aa6-186">Select **Copy** to save the password for the device.</span></span>

    >[!NOTE]
    ><span data-ttu-id="30aa6-187">Le mot de passe n’est affiché qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="30aa6-187">The password is only displayed once.</span></span> <span data-ttu-id="30aa6-188">N’oubliez pas de l’enregistrer pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="30aa6-188">Be sure to save it for later use.</span></span>

    ![Image de l’appareil ajouté avec les détails de connexion](images/add-machine-eval-lab.png)

4. <span data-ttu-id="30aa6-190">La mise en place de l’appareil commence.</span><span class="sxs-lookup"><span data-stu-id="30aa6-190">Device set up begins.</span></span> <span data-ttu-id="30aa6-191">Cela peut prendre jusqu’à 30 minutes environ.</span><span class="sxs-lookup"><span data-stu-id="30aa6-191">This can take up to approximately 30 minutes.</span></span> 

5. <span data-ttu-id="30aa6-192">Consultez l’état des périphériques de test, les niveaux de risque et d’exposition, ainsi que l’état des installations de simulateur en sélectionnant **l’onglet Appareils.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-192">See the status of test devices, the risk and exposure levels, and the status of simulator installations by selecting the **Devices** tab.</span></span> 

    ![Image de l’onglet Appareils](images/machines-tab.png)
    

    > [!TIP]
    > <span data-ttu-id="30aa6-194">Dans la colonne **État du** simulateur, vous pouvez pointer sur l’icône d’informations pour connaître l’état d’installation d’un agent.</span><span class="sxs-lookup"><span data-stu-id="30aa6-194">In the **Simulator status** column, you can hover over the information icon to know the installation status of an agent.</span></span>

## <a name="request-for-more-devices"></a><span data-ttu-id="30aa6-195">Demander plus d’appareils</span><span class="sxs-lookup"><span data-stu-id="30aa6-195">Request for more devices</span></span>
<span data-ttu-id="30aa6-196">Lorsque tous les appareils existants sont utilisés et supprimés, vous pouvez demander d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="30aa6-196">When all existing devices are used and deleted, you can request for more devices.</span></span> <span data-ttu-id="30aa6-197">Vous pouvez demander des ressources d’atelier une fois par mois.</span><span class="sxs-lookup"><span data-stu-id="30aa6-197">You can request for lab resources once a month.</span></span> 


1. <span data-ttu-id="30aa6-198">Dans le tableau de bord du laboratoire d’évaluation, **sélectionnez Demander plus d’appareils.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-198">From the evaluation lab dashboard, select **Request for more devices**.</span></span>

   ![Image de demande pour plus d’appareils](images/request-more-devices.png)

2. <span data-ttu-id="30aa6-200">Choisissez votre configuration.</span><span class="sxs-lookup"><span data-stu-id="30aa6-200">Choose your configuration.</span></span> 
3. <span data-ttu-id="30aa6-201">Envoyez la demande.</span><span class="sxs-lookup"><span data-stu-id="30aa6-201">Submit the request.</span></span> 

<span data-ttu-id="30aa6-202">Lorsque la demande est envoyée avec succès, vous verrez une bannière de confirmation verte et la date de la dernière soumission.</span><span class="sxs-lookup"><span data-stu-id="30aa6-202">When the request is submitted successfully you'll see a green confirmation banner and the date of the last submission.</span></span>
 
<span data-ttu-id="30aa6-203">Vous pouvez trouver l’état de votre demande dans l’onglet **Actions** de l’utilisateur, qui sera approuvé dans quelques heures.</span><span class="sxs-lookup"><span data-stu-id="30aa6-203">You can find the status of your request in the **User Actions** tab, which will be approved in a matter of hours.</span></span>

<span data-ttu-id="30aa6-204">Une fois approuvés, les appareils demandés sont ajoutés à votre atelier et vous pouvez en créer d’autres.</span><span class="sxs-lookup"><span data-stu-id="30aa6-204">When approved, the requested devices will be added to your lab set up and you’ll be able to create more devices.</span></span> 


> [!TIP]
> <span data-ttu-id="30aa6-205">Pour en savoir plus sur votre atelier, n’oubliez pas de consulter notre bibliothèque de simulations.</span><span class="sxs-lookup"><span data-stu-id="30aa6-205">To get more out of your lab, don’t forget to check out our simulations library.</span></span>

## <a name="simulate-attack-scenarios"></a><span data-ttu-id="30aa6-206">Simuler des scénarios d’attaque</span><span class="sxs-lookup"><span data-stu-id="30aa6-206">Simulate attack scenarios</span></span>
<span data-ttu-id="30aa6-207">Utilisez les périphériques de test pour exécuter vos propres simulations d’attaques en vous y connectant.</span><span class="sxs-lookup"><span data-stu-id="30aa6-207">Use the test devices to run your own attack simulations by connecting to them.</span></span> 

<span data-ttu-id="30aa6-208">Vous pouvez simuler des scénarios d’attaque à l’aide des outils suivants :</span><span class="sxs-lookup"><span data-stu-id="30aa6-208">You can simulate attack scenarios using:</span></span>
- <span data-ttu-id="30aa6-209">Scénarios [d’attaque « Faites-le vous-même »](https://securitycenter.windows.com/tutorials)</span><span class="sxs-lookup"><span data-stu-id="30aa6-209">The ["Do It Yourself" attack scenarios](https://securitycenter.windows.com/tutorials)</span></span>
- <span data-ttu-id="30aa6-210">Simulateurs de menaces</span><span class="sxs-lookup"><span data-stu-id="30aa6-210">Threat simulators</span></span>

<span data-ttu-id="30aa6-211">Vous pouvez également utiliser le service [de recherche avancée](advanced-hunting-query-language.md) pour interroger les données et l’analyse des [menaces](threat-analytics.md) afin d’afficher des rapports sur les menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="30aa6-211">You can also use [Advanced hunting](advanced-hunting-query-language.md) to query data and [Threat analytics](threat-analytics.md) to view reports about emerging threats.</span></span>

### <a name="do-it-yourself-attack-scenarios"></a><span data-ttu-id="30aa6-212">Scénarios d’attaques do-it-yourself</span><span class="sxs-lookup"><span data-stu-id="30aa6-212">Do-it-yourself attack scenarios</span></span>
<span data-ttu-id="30aa6-213">Si vous recherchez une simulation pré-réalisée, vous pouvez utiliser nos [scénarios](https://securitycenter.windows.com/tutorials)d’attaque « Faites-le vous-même ».</span><span class="sxs-lookup"><span data-stu-id="30aa6-213">If you are looking for a pre-made simulation, you can use our ["Do It Yourself" attack scenarios](https://securitycenter.windows.com/tutorials).</span></span> <span data-ttu-id="30aa6-214">Ces scripts sont sûrs, documentés et faciles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="30aa6-214">These scripts are safe, documented, and easy to use.</span></span> <span data-ttu-id="30aa6-215">Ces scénarios reflèteront les fonctionnalités de Defender for Endpoint et vous feront découvrir l’expérience d’investigation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-215">These scenarios will reflect Defender for Endpoint capabilities and walk you through investigation experience.</span></span>


>[!NOTE]
><span data-ttu-id="30aa6-216">La connexion aux périphériques de test est effectuée à l’aide de RDP.</span><span class="sxs-lookup"><span data-stu-id="30aa6-216">The connection to the test devices is done using RDP.</span></span> <span data-ttu-id="30aa6-217">Assurez-vous que vos paramètres de pare-feu autorisent les connexions RDP.</span><span class="sxs-lookup"><span data-stu-id="30aa6-217">Make sure that your firewall settings allow RDP connections.</span></span>

1. <span data-ttu-id="30aa6-218">Connecter sur votre appareil et exécutez une simulation d’attaque en **sélectionnant Connecter**.</span><span class="sxs-lookup"><span data-stu-id="30aa6-218">Connect to your device and run an attack simulation by selecting **Connect**.</span></span> 

    ![Image du bouton de connexion pour les périphériques de test](images/test-machine-table.png)

2. <span data-ttu-id="30aa6-220">Enregistrez le fichier RDP et lancez-le en sélectionnant **Connecter**.</span><span class="sxs-lookup"><span data-stu-id="30aa6-220">Save the RDP file and launch it by selecting **Connect**.</span></span>

    ![Image de la connexion bureau à distance](images/remote-connection.png)

    >[!NOTE]
    ><span data-ttu-id="30aa6-222">Si vous n’avez pas de copie du mot de passe enregistrée lors  de la configuration initiale, vous pouvez réinitialiser le mot de passe en sélectionnant Réinitialiser le mot de passe dans le menu : Image de réinitialisation du mot ![ de passe](images/reset-password-test-machine.png)</span><span class="sxs-lookup"><span data-stu-id="30aa6-222">If you don't have a copy of the password saved during the initial setup, you can reset the password by selecting **Reset password** from the menu: ![Image of reset password](images/reset-password-test-machine.png)</span></span><br>
    > <span data-ttu-id="30aa6-223">L’appareil change son état en « Exécution de la réinitialisation du mot de passe », puis votre nouveau mot de passe vous sera présenté dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="30aa6-223">The device will change it’s state to “Executing password reset", then you’ll be presented with your new password in a few minutes.</span></span>

3. <span data-ttu-id="30aa6-224">Entrez le mot de passe qui a été affiché lors de l’étape de création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30aa6-224">Enter the password that was displayed during the device creation step.</span></span> 

   ![Image de la fenêtre pour entrer les informations d’identification](images/enter-password.png)

4. <span data-ttu-id="30aa6-226">Exécutez des simulations d’attaques par vous-même sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30aa6-226">Run Do-it-yourself attack simulations on the device.</span></span> 


### <a name="threat-simulator-scenarios"></a><span data-ttu-id="30aa6-227">Scénarios de simulateur de menaces</span><span class="sxs-lookup"><span data-stu-id="30aa6-227">Threat simulator scenarios</span></span>
<span data-ttu-id="30aa6-228">Si vous avez choisi d’installer l’un des simulateurs de menaces pris en charge pendant l’installation de l’atelier, vous pouvez exécuter les simulations intégrées sur les périphériques du laboratoire d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-228">If you chose to install any of the supported threat simulators during the lab setup, you can run the built-in simulations on the evaluation lab devices.</span></span> 


<span data-ttu-id="30aa6-229">L’exécution de simulations de menaces à l’aide de plateformes tierces est un bon moyen d’évaluer microsoft Defender pour les fonctionnalités de point de terminaison dans les limites d’un environnement de laboratoire.</span><span class="sxs-lookup"><span data-stu-id="30aa6-229">Running threat simulations using third-party platforms is a good way to evaluate Microsoft Defender for Endpoint capabilities within the confines of a lab environment.</span></span>

>[!NOTE]
><span data-ttu-id="30aa6-230">Avant d’exécuter des simulations, assurez-vous que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="30aa6-230">Before you can run simulations, ensure the following requirements are met:</span></span>
>- <span data-ttu-id="30aa6-231">Les appareils doivent être ajoutés au laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="30aa6-231">Devices must be added to the evaluation lab</span></span>
>- <span data-ttu-id="30aa6-232">Les simulateurs de menaces doivent être installés dans le laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="30aa6-232">Threat simulators must be installed in the evaluation lab</span></span>

1. <span data-ttu-id="30aa6-233">Dans le portail, **sélectionnez Créer une simulation.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-233">From the portal select **Create simulation**.</span></span>

2. <span data-ttu-id="30aa6-234">Sélectionnez un simulateur de menaces.</span><span class="sxs-lookup"><span data-stu-id="30aa6-234">Select a threat simulator.</span></span>

    ![Image de la sélection du simulateur de menaces](images/select-simulator.png)

3. <span data-ttu-id="30aa6-236">Choisissez une simulation ou parcourez la galerie de simulations pour parcourir les simulations disponibles.</span><span class="sxs-lookup"><span data-stu-id="30aa6-236">Choose a simulation or look through the simulation gallery to browse through the available simulations.</span></span> 

    <span data-ttu-id="30aa6-237">Vous pouvez obtenir la galerie de simulations à partir de :</span><span class="sxs-lookup"><span data-stu-id="30aa6-237">You can get to the simulation gallery from:</span></span>
    - <span data-ttu-id="30aa6-238">Tableau de bord d’évaluation principal dans la **vignette de vue d’ensemble simulations** ou</span><span class="sxs-lookup"><span data-stu-id="30aa6-238">The main evaluation dashboard in the **Simulations overview** tile or</span></span>
    - <span data-ttu-id="30aa6-239">En naviguant à partir du volet de navigation Évaluation et didacticiels  >  **Simulation & didacticiels,** puis sélectionnez Le catalogue **simulations**.</span><span class="sxs-lookup"><span data-stu-id="30aa6-239">By navigating from the navigation pane **Evaluation and tutorials** > **Simulation & tutorials**, then select **Simulations catalog**.</span></span>

4. <span data-ttu-id="30aa6-240">Sélectionnez les appareils sur lequel vous souhaitez exécuter la simulation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-240">Select the devices where you'd like to run the simulation on.</span></span>

5. <span data-ttu-id="30aa6-241">Sélectionnez **Créer une simulation.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-241">Select **Create simulation**.</span></span>

6. <span data-ttu-id="30aa6-242">Affichez la progression d’une simulation en sélectionnant **l’onglet Simulations.** Afficher l’état de simulation, les alertes actives et d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="30aa6-242">View the progress of a simulation by selecting the **Simulations** tab. View the simulation state, active alerts, and other details.</span></span> 

    ![Image de l’onglet Simulations](images/simulations-tab.png)
    
<span data-ttu-id="30aa6-244">Après avoir lancé vos simulations, nous vous encourageons à parcourir la barre de progression de l’atelier et à explorer Microsoft Defender for Endpoint qui a déclenché une investigation et une correction **automatisées.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-244">After running your simulations, we encourage you to walk through the lab progress bar and explore **Microsoft Defender for Endpoint triggered an automated investigation and remediation**.</span></span> <span data-ttu-id="30aa6-245">Consultez les preuves collectées et analysées par la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="30aa6-245">Check out the evidence collected and analyzed by the feature.</span></span>

<span data-ttu-id="30aa6-246">Recherchez des preuves d’attaque par le biais d’une recherche avancée à l’aide du langage de requête enrichi et de la télémétrie brute, puis consultez certaines menaces mondiales documentées dans l’analyse des menaces.</span><span class="sxs-lookup"><span data-stu-id="30aa6-246">Hunt for attack evidence through advanced hunting by using the rich query language and raw telemetry and check out some world-wide threats documented in Threat analytics.</span></span>


## <a name="simulation-gallery"></a><span data-ttu-id="30aa6-247">Galerie de simulations</span><span class="sxs-lookup"><span data-stu-id="30aa6-247">Simulation gallery</span></span>
<span data-ttu-id="30aa6-248">Microsoft Defender pour le point de terminaison s’est associé à différentes plateformes de simulation de menaces pour vous donner un accès pratique pour tester les fonctionnalités de la plateforme directement à partir du portail.</span><span class="sxs-lookup"><span data-stu-id="30aa6-248">Microsoft Defender for Endpoint has partnered with various threat simulation platforms to give you convenient access to test the capabilities of the platform right from the within the portal.</span></span> 

<span data-ttu-id="30aa6-249">Affichez toutes les simulations disponibles en allant dans le catalogue **Simulations et** didacticiels  >  **Simulations** à partir du menu.</span><span class="sxs-lookup"><span data-stu-id="30aa6-249">View all the available simulations by going to  **Simulations and tutorials** > **Simulations catalog**  from the menu.</span></span> 

<span data-ttu-id="30aa6-250">Une liste d’agents de simulation de menace tiers pris en charge est répertoriée, et des types spécifiques de simulations ainsi que des descriptions détaillées sont fournis dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="30aa6-250">A list of supported third-party threat simulation agents are listed, and specific types of simulations along with detailed descriptions are provided on the catalog.</span></span> 

<span data-ttu-id="30aa6-251">Vous pouvez facilement exécuter n’importe quelle simulation disponible directement à partir du catalogue.</span><span class="sxs-lookup"><span data-stu-id="30aa6-251">You can conveniently run any available simulation right from the catalog.</span></span>  


![Image du catalogue de simulations](images/simulations-catalog.png)

<span data-ttu-id="30aa6-253">Chaque simulation est livré avec une description détaillée du scénario d’attaque et des références telles que les techniques d’attaque MITRE utilisées et des exemples de requêtes de recherche avancée que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="30aa6-253">Each simulation comes with an in-depth description of the attack scenario and references such as the MITRE attack techniques used and sample Advanced hunting queries you run.</span></span>

<span data-ttu-id="30aa6-254">**Exemples :** 
 ![ Image de description de simulation détaillée1](images/simulation-details-aiq.png)</span><span class="sxs-lookup"><span data-stu-id="30aa6-254">**Examples:**
![Image of simulation description details1](images/simulation-details-aiq.png)</span></span>


![Image de description de simulation détaillée2](images/simulation-details-sb.png)


## <a name="evaluation-report"></a><span data-ttu-id="30aa6-256">Rapport d’évaluation</span><span class="sxs-lookup"><span data-stu-id="30aa6-256">Evaluation report</span></span>
<span data-ttu-id="30aa6-257">Les rapports de laboratoire résument les résultats des simulations effectuées sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="30aa6-257">The lab reports summarize the results of the simulations conducted on the devices.</span></span>

![Image du rapport d’évaluation](images/eval-report.png)

<span data-ttu-id="30aa6-259">En un coup d’œil, vous pourrez rapidement voir :</span><span class="sxs-lookup"><span data-stu-id="30aa6-259">At a glance, you'll quickly be able to see:</span></span>
- <span data-ttu-id="30aa6-260">Incidents déclenchés</span><span class="sxs-lookup"><span data-stu-id="30aa6-260">Incidents that were triggered</span></span>
- <span data-ttu-id="30aa6-261">Alertes générées</span><span class="sxs-lookup"><span data-stu-id="30aa6-261">Generated alerts</span></span>
- <span data-ttu-id="30aa6-262">Évaluations du niveau d’exposition</span><span class="sxs-lookup"><span data-stu-id="30aa6-262">Assessments on exposure level</span></span> 
- <span data-ttu-id="30aa6-263">Catégories de menaces observées</span><span class="sxs-lookup"><span data-stu-id="30aa6-263">Threat categories observed</span></span>
- <span data-ttu-id="30aa6-264">Sources de détection</span><span class="sxs-lookup"><span data-stu-id="30aa6-264">Detection sources</span></span>
- <span data-ttu-id="30aa6-265">Enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="30aa6-265">Automated investigations</span></span>


## <a name="provide-feedback"></a><span data-ttu-id="30aa6-266">Envoyer des commentaires</span><span class="sxs-lookup"><span data-stu-id="30aa6-266">Provide feedback</span></span>
<span data-ttu-id="30aa6-267">Vos commentaires nous aident à mieux protéger votre environnement contre les attaques avancées.</span><span class="sxs-lookup"><span data-stu-id="30aa6-267">Your feedback helps us get better in protecting your environment from advanced attacks.</span></span> <span data-ttu-id="30aa6-268">Partagez votre expérience et vos impressions à partir des fonctionnalités du produit et des résultats d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="30aa6-268">Share your experience and impressions from product capabilities and evaluation results.</span></span>

<span data-ttu-id="30aa6-269">Faites-nous part de vos commentaires en sélectionnant **Fournir des commentaires.**</span><span class="sxs-lookup"><span data-stu-id="30aa6-269">Let us know what you think, by selecting **Provide feedback**.</span></span>

![Image de commentaires](images/send-us-feedback-eval-lab.png)
