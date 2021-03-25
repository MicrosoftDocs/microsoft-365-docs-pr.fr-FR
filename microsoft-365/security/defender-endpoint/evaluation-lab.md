---
title: Laboratoire d’évaluation de Microsoft Defender for Endpoint
description: Découvrez les fonctionnalités de Microsoft Defender pour les points de terminaison, exécutez des simulations d’attaques et découvrez comment il empêche, détecte et remédie aux menaces.
keywords: évaluer mdatp, évaluation, atelier, simulation, windows 10, windows server 2019, laboratoire d’évaluation
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
ms.openlocfilehash: ead616b7af3df05f4c0c5755ad779f0251555734
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51066545"
---
# <a name="microsoft-defender-for-endpoint-evaluation-lab"></a><span data-ttu-id="d110d-104">Laboratoire d’évaluation de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d110d-104">Microsoft Defender for Endpoint evaluation lab</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d110d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d110d-105">**Applies to:**</span></span>
- [<span data-ttu-id="d110d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d110d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="d110d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d110d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="d110d-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d110d-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d110d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d110d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)


<span data-ttu-id="d110d-110">La conduite d’une évaluation complète du produit de sécurité peut être un processus complexe nécessitant une configuration fastidieuse de l’environnement et de l’appareil avant qu’une simulation d’attaque de bout en bout puisse réellement être effectuée.</span><span class="sxs-lookup"><span data-stu-id="d110d-110">Conducting a comprehensive security product evaluation can be a complex process requiring cumbersome environment and device configuration before an end-to-end attack simulation can actually be done.</span></span> <span data-ttu-id="d110d-111">L’ajout de la complexité est la difficulté de suivre l’endroit où les activités de simulation, les alertes et les résultats sont reflétés au cours de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="d110d-111">Adding to the complexity is the challenge of tracking where the simulation activities, alerts, and results are reflected during the evaluation.</span></span>

<span data-ttu-id="d110d-112">Le laboratoire d’évaluation de Microsoft Defender pour points de terminaison est conçu pour éliminer la complexité de la configuration des appareils et de l’environnement afin de pouvoir vous concentrer sur l’évaluation des fonctionnalités de la plateforme, l’exécution de simulations et l’utilisation des fonctionnalités de prévention, de détection et de correction.</span><span class="sxs-lookup"><span data-stu-id="d110d-112">The Microsoft Defender for Endpoint evaluation lab is designed to eliminate the complexities of device and environment configuration so that you can  focus on evaluating the capabilities of the platform, running simulations, and seeing the prevention, detection, and remediation features in action.</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4qLUM]

<span data-ttu-id="d110d-113">Grâce à l’expérience de mise en place simplifiée, vous pouvez vous concentrer sur l’exécution de vos propres scénarios de test et des simulations pré-réalisées pour voir les résultats de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d110d-113">With the simplified set-up experience, you can focus on running your own test scenarios and the pre-made simulations to see how Defender for Endpoint performs.</span></span> 

<span data-ttu-id="d110d-114">Vous disposez d’un accès complet aux fonctionnalités puissantes de la plateforme, telles que les enquêtes automatisées, le recherche avancée et l’analyse des menaces, ce qui vous permet de tester la pile de protection complète de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d110d-114">You'll have full access to the powerful capabilities of the platform such as automated investigations, advanced hunting, and threat analytics, allowing you to test the comprehensive protection stack that Defender for Endpoint offers.</span></span> 

<span data-ttu-id="d110d-115">Vous pouvez ajouter des appareils Windows 10 ou Windows Server 2019 pré-configurés pour avoir les dernières versions du système d’exploitation et les composants de sécurité en place, ainsi qu’Office 2019 Standard installé.</span><span class="sxs-lookup"><span data-stu-id="d110d-115">You can add Windows 10 or Windows Server 2019 devices that come pre-configured to have the latest OS versions and the right security components in place as well as Office 2019 Standard installed.</span></span>

<span data-ttu-id="d110d-116">Vous pouvez également installer des simulateurs de menaces.</span><span class="sxs-lookup"><span data-stu-id="d110d-116">You can also install threat simulators.</span></span> <span data-ttu-id="d110d-117">Defender pour le point de terminaison s’est associé à des plateformes de simulation de menaces de pointe pour vous aider à tester les fonctionnalités de Defender for Endpoint sans avoir à quitter le portail.</span><span class="sxs-lookup"><span data-stu-id="d110d-117">Defender for Endpoint has partnered with industry leading threat simulation platforms to help you test out the Defender for Endpoint capabilities without having to leave the portal.</span></span>

 <span data-ttu-id="d110d-118">Installez votre simulateur préféré, exécutez des scénarios dans le laboratoire d’évaluation et voyez instantanément les résultats de la plateforme, le tout disponible sans frais supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d110d-118">Install your preferred simulator, run scenarios within the evaluation lab, and instantly see how the platform performs - all conveniently available at no extra cost to you.</span></span> <span data-ttu-id="d110d-119">Vous aurez également un accès pratique à un large éventail de simulations que vous pouvez accéder et exécuter à partir du catalogue de simulations.</span><span class="sxs-lookup"><span data-stu-id="d110d-119">You'll also have convenient access to wide array of simulations which you can access and run from the simulations catalog.</span></span>
    

## <a name="before-you-begin"></a><span data-ttu-id="d110d-120">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d110d-120">Before you begin</span></span>
<span data-ttu-id="d110d-121">Vous devez satisfaire [](minimum-requirements.md#licensing-requirements) aux exigences de licence ou avoir accès en version d’évaluation à Microsoft Defender for Endpoint pour accéder au laboratoire d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="d110d-121">You'll need to fulfill the [licensing requirements](minimum-requirements.md#licensing-requirements) or have trial access to Microsoft Defender for Endpoint to access the evaluation lab.</span></span>

<span data-ttu-id="d110d-122">Vous devez avoir **les autorisations Gérer les paramètres** de sécurité pour :</span><span class="sxs-lookup"><span data-stu-id="d110d-122">You must have **Manage security settings** permissions to:</span></span>
- <span data-ttu-id="d110d-123">Créer l’atelier</span><span class="sxs-lookup"><span data-stu-id="d110d-123">Create the lab</span></span>
- <span data-ttu-id="d110d-124">Créer des appareils</span><span class="sxs-lookup"><span data-stu-id="d110d-124">Create devices</span></span>
- <span data-ttu-id="d110d-125">Réinitialiser le mot de passe</span><span class="sxs-lookup"><span data-stu-id="d110d-125">Reset password</span></span>
- <span data-ttu-id="d110d-126">Créer des simulations</span><span class="sxs-lookup"><span data-stu-id="d110d-126">Create simulations</span></span> 
 
<span data-ttu-id="d110d-127">Si vous avez activé le contrôle d’accès basé sur un rôle (RBAC) et créé au moins un groupe d’ordinateurs, les utilisateurs doivent avoir accès à tous les groupes d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="d110d-127">If you enabled role-based access control (RBAC) and created at least a one machine group, users must have access to All machine groups.</span></span>

<span data-ttu-id="d110d-128">Pour plus d’informations, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="d110d-128">For more information, see [Create and manage roles](user-roles.md).</span></span>

<span data-ttu-id="d110d-129">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d110d-129">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d110d-130">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d110d-130">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-main-abovefoldlink)


## <a name="get-started-with-the-lab"></a><span data-ttu-id="d110d-131">Mise en place de l’atelier</span><span class="sxs-lookup"><span data-stu-id="d110d-131">Get started with the lab</span></span>
<span data-ttu-id="d110d-132">Vous pouvez accéder à l’atelier à partir du menu.</span><span class="sxs-lookup"><span data-stu-id="d110d-132">You can access the lab from the menu.</span></span> <span data-ttu-id="d110d-133">Dans le menu de navigation, sélectionnez **Évaluation et didacticiels > laboratoire d’évaluation.**</span><span class="sxs-lookup"><span data-stu-id="d110d-133">In the navigation menu, select **Evaluation and tutorials > Evaluation lab**.</span></span>

![Image de l’atelier d’évaluation dans le menu](images/evaluation-lab-menu.png)

>[!NOTE]
>- <span data-ttu-id="d110d-135">Chaque environnement est mis en service avec un ensemble limité de périphériques de test.</span><span class="sxs-lookup"><span data-stu-id="d110d-135">Each environment is provisioned with a limited set of test devices.</span></span>
>- <span data-ttu-id="d110d-136">Selon le type de structure d’environnement que vous sélectionnez, les appareils seront disponibles pour le nombre d’heures spécifié à partir du jour de l’activation.</span><span class="sxs-lookup"><span data-stu-id="d110d-136">Depending the type of environment structure you select, devices will be available for the specified number of hours from the day of activation.</span></span>
>- <span data-ttu-id="d110d-137">Lorsque vous avez utilisé les appareils mis en service, aucun nouvel appareil n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="d110d-137">When you've used up the provisioned devices, no new devices are provided.</span></span> <span data-ttu-id="d110d-138">Un appareil supprimé n’actualise pas le nombre de périphériques de test disponibles.</span><span class="sxs-lookup"><span data-stu-id="d110d-138">A deleted device does not refresh the available test device count.</span></span>
>- <span data-ttu-id="d110d-139">Étant donné les ressources limitées, il est conseillé d’utiliser les appareils avec soin.</span><span class="sxs-lookup"><span data-stu-id="d110d-139">Given the limited resources, it’s advisable to use the devices carefully.</span></span>

<span data-ttu-id="d110d-140">Vous avez déjà un atelier ?</span><span class="sxs-lookup"><span data-stu-id="d110d-140">Already have a lab?</span></span> <span data-ttu-id="d110d-141">Veillez à activer les nouveaux simulateurs de menaces et à avoir des appareils actifs.</span><span class="sxs-lookup"><span data-stu-id="d110d-141">Make sure to enable the new threat simulators and have active devices.</span></span>

## <a name="setup-the-evaluation-lab"></a><span data-ttu-id="d110d-142">Configurer le laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="d110d-142">Setup the evaluation lab</span></span>

1. <span data-ttu-id="d110d-143">Dans le volet de navigation, sélectionnez Le laboratoire d’évaluation et **didacticiels**  >  d’évaluation, puis le laboratoire **d’installation.**</span><span class="sxs-lookup"><span data-stu-id="d110d-143">In the navigation pane, select **Evaluation and tutorials** > **Evaluation lab**, then select **Setup lab**.</span></span>

    ![Image de la page d’accueil du laboratoire d’évaluation](images/evaluation-lab-setup.png)

2. <span data-ttu-id="d110d-145">En fonction de vos besoins d’évaluation, vous pouvez choisir de configurer un environnement avec moins d’appareils pendant une période plus longue ou plus d’appareils sur une période plus courte.</span><span class="sxs-lookup"><span data-stu-id="d110d-145">Depending on your evaluation needs, you can choose to setup an environment with fewer devices for a longer period or more devices for a shorter period.</span></span> <span data-ttu-id="d110d-146">Sélectionnez votre configuration d’atelier préférée, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="d110d-146">Select your preferred lab configuration then select **Next**.</span></span>

    ![Image des options de configuration de l’atelier](images/lab-creation-page.png) 


3. <span data-ttu-id="d110d-148">(Facultatif) Vous pouvez choisir d’installer des simulateurs de menaces dans l’atelier.</span><span class="sxs-lookup"><span data-stu-id="d110d-148">(Optional) You can choose to install threat simulators in the lab.</span></span> 

    ![Image de l’agent des simulateurs d’installation](images/install-agent.png)

    >[!IMPORTANT]
    ><span data-ttu-id="d110d-150">Vous devez d’abord accepter et donner votre consentement aux conditions générales et aux déclarations de partage d’informations.</span><span class="sxs-lookup"><span data-stu-id="d110d-150">You'll first need to accept and provide consent to the terms and information sharing statements.</span></span> 

4. <span data-ttu-id="d110d-151">Sélectionnez l’agent de simulation de menace que vous souhaitez utiliser et entrez vos détails.</span><span class="sxs-lookup"><span data-stu-id="d110d-151">Select the threat simulation agent you'd like to use and enter your details.</span></span> <span data-ttu-id="d110d-152">Vous pouvez également choisir d’installer des simulateurs de menaces ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d110d-152">You can also choose to install threat simulators at a later time.</span></span> <span data-ttu-id="d110d-153">Si vous choisissez d’installer des agents de simulation de menace lors de l’installation de l’atelier, vous profitez de leur installation pratique sur les appareils que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="d110d-153">If you choose to install threat simulation agents during the lab setup, you'll enjoy the benefit of having them conveniently installed on the devices you add.</span></span>  
    
    ![Image de la page récapitulatif](images/lab-setup-summary.png)

5.  <span data-ttu-id="d110d-155">Examinez le résumé et sélectionnez **Le laboratoire d’installation.**</span><span class="sxs-lookup"><span data-stu-id="d110d-155">Review the summary and select **Setup lab**.</span></span>  

<span data-ttu-id="d110d-156">Une fois le processus de configuration de l’atelier terminé, vous pouvez ajouter des appareils et exécuter des simulations.</span><span class="sxs-lookup"><span data-stu-id="d110d-156">After the lab setup process is complete, you can add devices and run simulations.</span></span> 


## <a name="add-devices"></a><span data-ttu-id="d110d-157">Ajouter des appareils</span><span class="sxs-lookup"><span data-stu-id="d110d-157">Add devices</span></span>
<span data-ttu-id="d110d-158">Lorsque vous ajoutez un appareil à votre environnement, Defender pour le point de terminaison configure un appareil bien configuré avec des détails de connexion.</span><span class="sxs-lookup"><span data-stu-id="d110d-158">When you add a device to your environment, Defender for Endpoint sets up a well-configured device with connection details.</span></span> <span data-ttu-id="d110d-159">Vous pouvez ajouter des appareils Windows 10 ou Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="d110d-159">You can add Windows 10 or Windows Server 2019 devices.</span></span>

<span data-ttu-id="d110d-160">L’appareil sera configuré avec la version la plus à jour du système d’exploitation et d’Office 2019 Standard, ainsi que d’autres applications telles que Java, Python et SysIntenals.</span><span class="sxs-lookup"><span data-stu-id="d110d-160">The device will be configured with the most up-to-date version of the OS and Office 2019 Standard as well as other apps such as Java, Python, and SysIntenals.</span></span> 

   >[!TIP]
   > <span data-ttu-id="d110d-161">Vous avez besoin de plus d’appareils dans votre atelier ?</span><span class="sxs-lookup"><span data-stu-id="d110d-161">Need more devices in your lab?</span></span> <span data-ttu-id="d110d-162">Envoyez un ticket de support pour que votre demande soit examinée par l’équipe Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d110d-162">Submit a support ticket to have your request reviewed by the Defender for Endpoint team.</span></span> 

<span data-ttu-id="d110d-163">Si vous avez choisi d’ajouter un simulateur de menaces lors de l’installation de l’atelier, l’agent de simulateur de menaces sera installé sur tous les appareils que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="d110d-163">If you chose to add a threat simulator during the lab setup, all devices will have the threat simulator agent installed in the devices that you add.</span></span>

<span data-ttu-id="d110d-164">L’appareil est automatiquement intégré à votre client avec les composants de sécurité Windows recommandés, sous et en mode audit, sans aucun effort de votre côté.</span><span class="sxs-lookup"><span data-stu-id="d110d-164">The device will automatically be onboarded to your tenant with the recommended Windows security components turned on and in audit mode - with no effort on your side.</span></span> 

<span data-ttu-id="d110d-165">Les composants de sécurité suivants sont pré-configurés dans les périphériques de test :</span><span class="sxs-lookup"><span data-stu-id="d110d-165">The following security components are pre-configured in the test devices:</span></span>

- [<span data-ttu-id="d110d-166">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="d110d-166">Attack surface reduction</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard)
- [<span data-ttu-id="d110d-167">Bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="d110d-167">Block at first sight</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-block-at-first-sight-microsoft-defender-antivirus)
- [<span data-ttu-id="d110d-168">Accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="d110d-168">Controlled folder access</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/controlled-folders-exploit-guard)
- [<span data-ttu-id="d110d-169">Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="d110d-169">Exploit protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/enable-exploit-protection)
- [<span data-ttu-id="d110d-170">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="d110d-170">Network protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/network-protection-exploit-guard)
- [<span data-ttu-id="d110d-171">Détection d’applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="d110d-171">Potentially unwanted application detection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus)
- [<span data-ttu-id="d110d-172">Protection cloud</span><span class="sxs-lookup"><span data-stu-id="d110d-172">Cloud-delivered protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/utilize-microsoft-cloud-protection-microsoft-defender-antivirus)
- [<span data-ttu-id="d110d-173">Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="d110d-173">Microsoft Defender SmartScreen</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)

>[!NOTE]
> <span data-ttu-id="d110d-174">L’Antivirus Microsoft Defender sera en cours (pas en mode audit).</span><span class="sxs-lookup"><span data-stu-id="d110d-174">Microsoft Defender Antivirus will be on (not in audit mode).</span></span> <span data-ttu-id="d110d-175">Si l’Antivirus Microsoft Defender vous empêche d’utiliser votre simulation, vous pouvez désactiver la protection en temps réel sur l’appareil via la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="d110d-175">If Microsoft Defender Antivirus blocks you from running your simulation, you can turn off real-time protection on the device through Windows Security.</span></span> <span data-ttu-id="d110d-176">Pour plus d’informations, [voir Configure always-on protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus).</span><span class="sxs-lookup"><span data-stu-id="d110d-176">For more information, see [Configure always-on protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus).</span></span>

<span data-ttu-id="d110d-177">Les paramètres d’examen automatisé dépendent des paramètres du client.</span><span class="sxs-lookup"><span data-stu-id="d110d-177">Automated investigation settings will be dependent on tenant settings.</span></span> <span data-ttu-id="d110d-178">Elle sera configurée pour être semi-automatisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d110d-178">It will be configured to be semi-automated by default.</span></span> <span data-ttu-id="d110d-179">Pour plus d’informations, voir [Vue d’ensemble des enquêtes automatisées.](automated-investigations.md)</span><span class="sxs-lookup"><span data-stu-id="d110d-179">For more information, see [Overview of Automated investigations](automated-investigations.md).</span></span>

>[!NOTE]
><span data-ttu-id="d110d-180">La connexion aux périphériques de test est effectuée à l’aide de RDP.</span><span class="sxs-lookup"><span data-stu-id="d110d-180">The connection to the test devices is done using RDP.</span></span> <span data-ttu-id="d110d-181">Assurez-vous que vos paramètres de pare-feu autorisent les connexions RDP.</span><span class="sxs-lookup"><span data-stu-id="d110d-181">Make sure that your firewall settings allow RDP connections.</span></span>

1. <span data-ttu-id="d110d-182">Dans le tableau de bord, **sélectionnez Ajouter un appareil.**</span><span class="sxs-lookup"><span data-stu-id="d110d-182">From the dashboard, select **Add device**.</span></span> 

2. <span data-ttu-id="d110d-183">Choisissez le type d’appareil à ajouter.</span><span class="sxs-lookup"><span data-stu-id="d110d-183">Choose the type of device to add.</span></span> <span data-ttu-id="d110d-184">Vous pouvez choisir d’ajouter Windows 10 ou Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="d110d-184">You can choose to add Windows 10 or Windows Server 2019.</span></span>

    ![Image de la configuration de l’atelier avec les options d’appareil](images/add-machine-options.png)


    >[!NOTE]
    ><span data-ttu-id="d110d-186">En cas de problème lors du processus de création de l’appareil, vous serez averti et vous devrez envoyer une nouvelle demande.</span><span class="sxs-lookup"><span data-stu-id="d110d-186">If something goes wrong with the device creation process, you'll be notified and you'll need to submit a new request.</span></span> <span data-ttu-id="d110d-187">Si la création de l’appareil échoue, elle n’est pas comptabilisée dans le quota autorisé global.</span><span class="sxs-lookup"><span data-stu-id="d110d-187">If the device creation fails, it will not be counted against the overall allowed quota.</span></span> 

3. <span data-ttu-id="d110d-188">Les détails de connexion sont affichés.</span><span class="sxs-lookup"><span data-stu-id="d110d-188">The connection details are displayed.</span></span> <span data-ttu-id="d110d-189">Sélectionnez **Copier** pour enregistrer le mot de passe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d110d-189">Select **Copy** to save the password for the device.</span></span>

    >[!NOTE]
    ><span data-ttu-id="d110d-190">Le mot de passe n’est affiché qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="d110d-190">The password is only displayed once.</span></span> <span data-ttu-id="d110d-191">N’oubliez pas de l’enregistrer pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d110d-191">Be sure to save it for later use.</span></span>

    ![Image de l’appareil ajouté avec les détails de connexion](images/add-machine-eval-lab.png)

4. <span data-ttu-id="d110d-193">La mise en place de l’appareil commence.</span><span class="sxs-lookup"><span data-stu-id="d110d-193">Device set up begins.</span></span> <span data-ttu-id="d110d-194">Cela peut prendre jusqu’à 30 minutes environ.</span><span class="sxs-lookup"><span data-stu-id="d110d-194">This can take up to approximately 30 minutes.</span></span> 

5. <span data-ttu-id="d110d-195">Consultez l’état des périphériques de test, les niveaux de risque et d’exposition, ainsi que l’état des installations de simulateur en sélectionnant **l’onglet Appareils.**</span><span class="sxs-lookup"><span data-stu-id="d110d-195">See the status of test devices, the risk and exposure levels, and the status of simulator installations by selecting the **Devices** tab.</span></span> 

    ![Image de l’onglet Appareils](images/machines-tab.png)
    

    >[!TIP]
    ><span data-ttu-id="d110d-197">Dans la colonne **État du** simulateur, vous pouvez pointer sur l’icône d’informations pour connaître l’état d’installation d’un agent.</span><span class="sxs-lookup"><span data-stu-id="d110d-197">In the **Simulator status** column, you can hover over the information icon to know the installation status of an agent.</span></span>



## <a name="simulate-attack-scenarios"></a><span data-ttu-id="d110d-198">Simuler des scénarios d’attaque</span><span class="sxs-lookup"><span data-stu-id="d110d-198">Simulate attack scenarios</span></span>
<span data-ttu-id="d110d-199">Utilisez les périphériques de test pour exécuter vos propres simulations d’attaques en vous y connectant.</span><span class="sxs-lookup"><span data-stu-id="d110d-199">Use the test devices to run your own attack simulations by connecting to them.</span></span> 

<span data-ttu-id="d110d-200">Vous pouvez simuler des scénarios d’attaque à l’aide des outils suivants :</span><span class="sxs-lookup"><span data-stu-id="d110d-200">You can simulate attack scenarios using:</span></span>
- <span data-ttu-id="d110d-201">Scénarios d’attaque « Faire [vous-même »](https://securitycenter.windows.com/tutorials)</span><span class="sxs-lookup"><span data-stu-id="d110d-201">The ["Do It Yourself" attack scenarios](https://securitycenter.windows.com/tutorials)</span></span>
- <span data-ttu-id="d110d-202">Simulateurs de menaces</span><span class="sxs-lookup"><span data-stu-id="d110d-202">Threat simulators</span></span>

<span data-ttu-id="d110d-203">Vous pouvez également utiliser la recherche [avancée pour](advanced-hunting-query-language.md) interroger les données et l’analyse des [menaces](threat-analytics.md) afin d’afficher des rapports sur les menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="d110d-203">You can also use [Advanced hunting](advanced-hunting-query-language.md) to query data and [Threat analytics](threat-analytics.md) to view reports about emerging threats.</span></span>

### <a name="do-it-yourself-attack-scenarios"></a><span data-ttu-id="d110d-204">Scénarios d’attaques do-it-yourself</span><span class="sxs-lookup"><span data-stu-id="d110d-204">Do-it-yourself attack scenarios</span></span>
<span data-ttu-id="d110d-205">Si vous recherchez une simulation pré-réalisée, vous pouvez utiliser nos [scénarios](https://securitycenter.windows.com/tutorials)d’attaque « Faites-le vous-même ».</span><span class="sxs-lookup"><span data-stu-id="d110d-205">If you are looking for a pre-made simulation, you can use our ["Do It Yourself" attack scenarios](https://securitycenter.windows.com/tutorials).</span></span> <span data-ttu-id="d110d-206">Ces scripts sont sûrs, documentés et faciles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d110d-206">These scripts are safe, documented, and easy to use.</span></span> <span data-ttu-id="d110d-207">Ces scénarios reflèteront les fonctionnalités de Defender for Endpoint et vous feront découvrir l’expérience d’investigation.</span><span class="sxs-lookup"><span data-stu-id="d110d-207">These scenarios will reflect Defender for Endpoint capabilities and walk you through investigation experience.</span></span>


>[!NOTE]
><span data-ttu-id="d110d-208">La connexion aux périphériques de test est effectuée à l’aide de RDP.</span><span class="sxs-lookup"><span data-stu-id="d110d-208">The connection to the test devices is done using RDP.</span></span> <span data-ttu-id="d110d-209">Assurez-vous que vos paramètres de pare-feu autorisent les connexions RDP.</span><span class="sxs-lookup"><span data-stu-id="d110d-209">Make sure that your firewall settings allow RDP connections.</span></span>

1. <span data-ttu-id="d110d-210">Connectez-vous à votre appareil et exécutez une simulation d’attaque en sélectionnant **Se connecter.**</span><span class="sxs-lookup"><span data-stu-id="d110d-210">Connect to your device and run an attack simulation by selecting **Connect**.</span></span> 

    ![Image du bouton de connexion pour les périphériques de test](images/test-machine-table.png)

2. <span data-ttu-id="d110d-212">Enregistrez le fichier RDP et lancez-le en sélectionnant **Se connecter.**</span><span class="sxs-lookup"><span data-stu-id="d110d-212">Save the RDP file and launch it by selecting **Connect**.</span></span>

    ![Image de la connexion bureau à distance](images/remote-connection.png)

    >[!NOTE]
    ><span data-ttu-id="d110d-214">Si vous n’avez pas de copie du mot de passe enregistrée lors  de la configuration initiale, vous pouvez réinitialiser le mot de passe en sélectionnant Réinitialiser le mot de passe dans le menu : Image de réinitialisation du mot ![ de passe](images/reset-password-test-machine.png)</span><span class="sxs-lookup"><span data-stu-id="d110d-214">If you don't have a copy of the password saved during the initial setup, you can reset the password by selecting **Reset password** from the menu: ![Image of reset password](images/reset-password-test-machine.png)</span></span><br>
    > <span data-ttu-id="d110d-215">L’appareil change son état en « Exécution de la réinitialisation du mot de passe », puis votre nouveau mot de passe vous sera présenté dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="d110d-215">The device will change it’s state to “Executing password reset", then you’ll be presented with your new password in a few minutes.</span></span>

3. <span data-ttu-id="d110d-216">Entrez le mot de passe qui a été affiché lors de l’étape de création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d110d-216">Enter the password that was displayed during the device creation step.</span></span> 

   ![Image de la fenêtre pour entrer les informations d’identification](images/enter-password.png)

4. <span data-ttu-id="d110d-218">Exécutez des simulations d’attaques par vous-même sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d110d-218">Run Do-it-yourself attack simulations on the device.</span></span> 


### <a name="threat-simulator-scenarios"></a><span data-ttu-id="d110d-219">Scénarios de simulateur de menaces</span><span class="sxs-lookup"><span data-stu-id="d110d-219">Threat simulator scenarios</span></span>
<span data-ttu-id="d110d-220">Si vous avez choisi d’installer l’un des simulateurs de menaces pris en charge pendant l’installation de l’atelier, vous pouvez exécuter les simulations intégrées sur les périphériques de laboratoire d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="d110d-220">If you chose to install any of the supported threat simulators during the lab setup, you can run the built-in simulations on the evaluation lab devices.</span></span> 


<span data-ttu-id="d110d-221">L’exécution de simulations de menaces à l’aide de plateformes tierces est un bon moyen d’évaluer microsoft Defender pour les fonctionnalités de point de terminaison dans les limites d’un environnement de laboratoire.</span><span class="sxs-lookup"><span data-stu-id="d110d-221">Running threat simulations using third-party platforms is a good way to evaluate Microsoft Defender for Endpoint capabilities within the confines of a lab environment.</span></span>

>[!NOTE]
><span data-ttu-id="d110d-222">Avant d’exécuter des simulations, assurez-vous que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="d110d-222">Before you can run simulations, ensure the following requirements are met:</span></span>
>- <span data-ttu-id="d110d-223">Les appareils doivent être ajoutés au laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="d110d-223">Devices must be added to the evaluation lab</span></span>
>- <span data-ttu-id="d110d-224">Les simulateurs de menaces doivent être installés dans le laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="d110d-224">Threat simulators must be installed in the evaluation lab</span></span>

1. <span data-ttu-id="d110d-225">Dans le portail, **sélectionnez Créer une simulation.**</span><span class="sxs-lookup"><span data-stu-id="d110d-225">From the portal select **Create simulation**.</span></span>

2. <span data-ttu-id="d110d-226">Sélectionnez un simulateur de menaces.</span><span class="sxs-lookup"><span data-stu-id="d110d-226">Select a threat simulator.</span></span>

    ![Image de la sélection du simulateur de menaces](images/select-simulator.png)

3. <span data-ttu-id="d110d-228">Choisissez une simulation ou parcourez la galerie de simulations pour parcourir les simulations disponibles.</span><span class="sxs-lookup"><span data-stu-id="d110d-228">Choose a simulation or look through the simulation gallery to browse through the available simulations.</span></span> 

    <span data-ttu-id="d110d-229">Vous pouvez obtenir la galerie de simulations à partir de :</span><span class="sxs-lookup"><span data-stu-id="d110d-229">You can get to the simulation gallery from:</span></span>
    - <span data-ttu-id="d110d-230">Tableau de bord d’évaluation principal dans la **vignette Vue d’ensemble simulations** ou</span><span class="sxs-lookup"><span data-stu-id="d110d-230">The main evaluation dashboard in the **Simulations overview** tile or</span></span>
    - <span data-ttu-id="d110d-231">En naviguant à partir du volet de navigation Évaluation et didacticiels  >  **Simulation & didacticiels,** puis sélectionnez Le catalogue **simulations**.</span><span class="sxs-lookup"><span data-stu-id="d110d-231">By navigating from the navigation pane **Evaluation and tutorials** > **Simulation & tutorials**, then select **Simulations catalog**.</span></span>

4. <span data-ttu-id="d110d-232">Sélectionnez les appareils sur lequel vous souhaitez exécuter la simulation.</span><span class="sxs-lookup"><span data-stu-id="d110d-232">Select the devices where you'd like to run the simulation on.</span></span>

5. <span data-ttu-id="d110d-233">Sélectionnez **Créer une simulation.**</span><span class="sxs-lookup"><span data-stu-id="d110d-233">Select **Create simulation**.</span></span>

6. <span data-ttu-id="d110d-234">Affichez la progression d’une simulation en sélectionnant **l’onglet Simulations.** Afficher l’état de simulation, les alertes actives et d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="d110d-234">View the progress of a simulation by selecting the **Simulations** tab. View the simulation state, active alerts, and other details.</span></span> 

    ![Image de l’onglet Simulations](images/simulations-tab.png)
    
<span data-ttu-id="d110d-236">Après avoir lancé vos simulations, nous vous encourageons à parcourir la barre de progression de l’atelier et à explorer Microsoft Defender pour le point de terminaison qui a déclenché une investigation et une correction **automatisées.**</span><span class="sxs-lookup"><span data-stu-id="d110d-236">After running your simulations, we encourage you to walk through the lab progress bar and explore **Microsoft Defender for Endpoint triggered an automated investigation and remediation**.</span></span> <span data-ttu-id="d110d-237">Consultez les preuves collectées et analysées par la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d110d-237">Check out the evidence collected and analyzed by the feature.</span></span>

<span data-ttu-id="d110d-238">Recherchez des preuves d’attaque par le biais d’un recherche avancée à l’aide du langage de requête enrichi et de la télémétrie brute, puis consultez certaines menaces mondiales documentées dans l’analyse des menaces.</span><span class="sxs-lookup"><span data-stu-id="d110d-238">Hunt for attack evidence through advanced hunting by using the rich query language and raw telemetry and check out some world-wide threats documented in Threat analytics.</span></span>


## <a name="simulation-gallery"></a><span data-ttu-id="d110d-239">Galerie de simulations</span><span class="sxs-lookup"><span data-stu-id="d110d-239">Simulation gallery</span></span>
<span data-ttu-id="d110d-240">Microsoft Defender pour le point de terminaison s’est associé à différentes plateformes de simulation de menaces pour vous donner un accès pratique pour tester les fonctionnalités de la plateforme directement à partir du portail.</span><span class="sxs-lookup"><span data-stu-id="d110d-240">Microsoft Defender for Endpoint has partnered with various threat simulation platforms to give you convenient access to test the capabilities of the platform right from the within the portal.</span></span> 

<span data-ttu-id="d110d-241">Affichez toutes les simulations disponibles en allant dans le catalogue **Simulations et** didacticiels  >  **Simulations** à partir du menu.</span><span class="sxs-lookup"><span data-stu-id="d110d-241">View all the available simulations by going to  **Simulations and tutorials** > **Simulations catalog**  from the menu.</span></span> 

<span data-ttu-id="d110d-242">Une liste d’agents de simulation de menace tiers pris en charge est répertoriée, et des types spécifiques de simulations ainsi que des descriptions détaillées sont fournis dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="d110d-242">A list of supported third-party threat simulation agents are listed, and specific types of simulations along with detailed descriptions are provided on the catalog.</span></span> 

<span data-ttu-id="d110d-243">Vous pouvez facilement exécuter n’importe quelle simulation disponible directement à partir du catalogue.</span><span class="sxs-lookup"><span data-stu-id="d110d-243">You can conveniently run any available simulation right from the catalog.</span></span>  


![Image du catalogue de simulations](images/simulations-catalog.png)

<span data-ttu-id="d110d-245">Chaque simulation est livré avec une description détaillée du scénario d’attaque et des références telles que les techniques d’attaque MITRE utilisées et des exemples de requêtes de recherche avancée que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="d110d-245">Each simulation comes with an in-depth description of the attack scenario and references such as the MITRE attack techniques used and sample Advanced hunting queries you run.</span></span>

<span data-ttu-id="d110d-246">**Exemples :** 
 ![ Image de description de simulation détaillée1](images/simulation-details-aiq.png)</span><span class="sxs-lookup"><span data-stu-id="d110d-246">**Examples:**
![Image of simulation description details1](images/simulation-details-aiq.png)</span></span>


![Image de description de simulation détaillée2](images/simulation-details-sb.png)


## <a name="evaluation-report"></a><span data-ttu-id="d110d-248">Rapport d’évaluation</span><span class="sxs-lookup"><span data-stu-id="d110d-248">Evaluation report</span></span>
<span data-ttu-id="d110d-249">Les rapports de laboratoire résument les résultats des simulations effectuées sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="d110d-249">The lab reports summarize the results of the simulations conducted on the devices.</span></span>

![Image du rapport d’évaluation](images/eval-report.png)

<span data-ttu-id="d110d-251">En un coup d’œil, vous pourrez rapidement voir :</span><span class="sxs-lookup"><span data-stu-id="d110d-251">At a glance, you'll quickly be able to see:</span></span>
- <span data-ttu-id="d110d-252">Incidents déclenchés</span><span class="sxs-lookup"><span data-stu-id="d110d-252">Incidents that were triggered</span></span>
- <span data-ttu-id="d110d-253">Alertes générées</span><span class="sxs-lookup"><span data-stu-id="d110d-253">Generated alerts</span></span>
- <span data-ttu-id="d110d-254">Évaluations du niveau d’exposition</span><span class="sxs-lookup"><span data-stu-id="d110d-254">Assessments on exposure level</span></span> 
- <span data-ttu-id="d110d-255">Catégories de menaces observées</span><span class="sxs-lookup"><span data-stu-id="d110d-255">Threat categories observed</span></span>
- <span data-ttu-id="d110d-256">Sources de détection</span><span class="sxs-lookup"><span data-stu-id="d110d-256">Detection sources</span></span>
- <span data-ttu-id="d110d-257">Enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="d110d-257">Automated investigations</span></span>


## <a name="provide-feedback"></a><span data-ttu-id="d110d-258">Envoyer des commentaires</span><span class="sxs-lookup"><span data-stu-id="d110d-258">Provide feedback</span></span>
<span data-ttu-id="d110d-259">Vos commentaires nous aident à mieux protéger votre environnement contre les attaques avancées.</span><span class="sxs-lookup"><span data-stu-id="d110d-259">Your feedback helps us get better in protecting your environment from advanced attacks.</span></span> <span data-ttu-id="d110d-260">Partagez votre expérience et vos impressions à partir des fonctionnalités du produit et des résultats d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="d110d-260">Share your experience and impressions from product capabilities and evaluation results.</span></span>

<span data-ttu-id="d110d-261">Faites-nous part de vos commentaires en sélectionnant **Fournir des commentaires.**</span><span class="sxs-lookup"><span data-stu-id="d110d-261">Let us know what you think, by selecting **Provide feedback**.</span></span>

![Image de commentaires](images/send-us-feedback-eval-lab.png)
