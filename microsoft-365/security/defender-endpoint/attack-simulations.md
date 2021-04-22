---
title: Expérience de Microsoft Defender pour point de terminaison par le biais d'attaques simulées
description: Exécutez les simulations de scénario d'attaque fournies pour découvrir comment Microsoft Defender pour point de terminaison peut détecter, examiner et répondre aux violations.
keywords: test, scénario, attaque, simulation, simulation, course, Microsoft Defender pour point de terminaison
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 11/20/2018
ms.technology: mde
ms.openlocfilehash: 6ecbf98c81b1f68e42f39269809592fb446e6036
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934380"
---
# <a name="experience-microsoft-defender-for-endpoint-through-simulated-attacks"></a><span data-ttu-id="abd37-104">Expérience de Microsoft Defender pour point de terminaison par le biais d'attaques simulées</span><span class="sxs-lookup"><span data-stu-id="abd37-104">Experience Microsoft Defender for Endpoint through simulated attacks</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="abd37-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="abd37-105">**Applies to:**</span></span>
- [<span data-ttu-id="abd37-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="abd37-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="abd37-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="abd37-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="abd37-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="abd37-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="abd37-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="abd37-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-attacksimulations-abovefoldlink)

>[!TIP]
>- <span data-ttu-id="abd37-110">Découvrez les dernières améliorations apportées à Microsoft Defender pour point de terminaison : Nouveautés [de Defender pour Point de terminaison .](https://cloudblogs.microsoft.com/microsoftsecure/2018/11/15/whats-new-in-windows-defender-atp/)</span><span class="sxs-lookup"><span data-stu-id="abd37-110">Learn about the latest enhancements in Microsoft Defender for Endpoint: [What's new in Defender for Endpoint?](https://cloudblogs.microsoft.com/microsoftsecure/2018/11/15/whats-new-in-windows-defender-atp/).</span></span>
>- <span data-ttu-id="abd37-111">Defender pour le point de terminaison a démontré les fonctionnalités d'optique et de détection de pointe du secteur dans l'évaluation MITRE récente.</span><span class="sxs-lookup"><span data-stu-id="abd37-111">Defender for Endpoint demonstrated industry-leading optics and detection capabilities in the recent MITRE evaluation.</span></span> <span data-ttu-id="abd37-112">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span><span class="sxs-lookup"><span data-stu-id="abd37-112">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span></span>

<span data-ttu-id="abd37-113">Vous souhaitez peut-être faire l'expérience de Defender for Endpoint avant d'intégrer plusieurs appareils au service.</span><span class="sxs-lookup"><span data-stu-id="abd37-113">You might want to experience Defender for Endpoint before you onboard more than a few devices to the service.</span></span> <span data-ttu-id="abd37-114">Pour ce faire, vous pouvez exécuter des simulations d'attaques contrôlées sur quelques périphériques de test.</span><span class="sxs-lookup"><span data-stu-id="abd37-114">To do this, you can run controlled attack simulations on a few test devices.</span></span> <span data-ttu-id="abd37-115">Après avoir réalisé les attaques simulées, vous pouvez examiner la façon dont Defender pour le point de terminaison fait face à une activité malveillante et découvrir comment elle permet une réponse efficace.</span><span class="sxs-lookup"><span data-stu-id="abd37-115">After running the simulated attacks, you can review how Defender for Endpoint surfaces malicious activity and explore how it enables an efficient response.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="abd37-116">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="abd37-116">Before you begin</span></span>

<span data-ttu-id="abd37-117">Pour exécuter l'une des simulations fournies, vous avez besoin d'au moins [un appareil intégré.](onboard-configure.md)</span><span class="sxs-lookup"><span data-stu-id="abd37-117">To run any of the provided simulations, you need at least [one onboarded device](onboard-configure.md).</span></span> 

<span data-ttu-id="abd37-118">Lisez le document pas à pas fourni avec chaque scénario d'attaque.</span><span class="sxs-lookup"><span data-stu-id="abd37-118">Read the walkthrough document provided with each attack scenario.</span></span> <span data-ttu-id="abd37-119">Chaque document inclut les exigences en matière de système d'exploitation et d'application, ainsi que des instructions détaillées propres à un scénario d'attaque.</span><span class="sxs-lookup"><span data-stu-id="abd37-119">Each document includes OS and application requirements as well as detailed instructions that are specific to an attack scenario.</span></span>

## <a name="run-a-simulation"></a><span data-ttu-id="abd37-120">Exécuter une simulation</span><span class="sxs-lookup"><span data-stu-id="abd37-120">Run a simulation</span></span>

1. <span data-ttu-id="abd37-121">Dans **les**  >  **simulations d'& didacticiels,** sélectionnez les scénarios d'attaque disponibles que vous souhaitez simuler :</span><span class="sxs-lookup"><span data-stu-id="abd37-121">In **Help** > **Simulations & tutorials**, select which of the available attack scenarios you would like to simulate:</span></span>

   - <span data-ttu-id="abd37-122">**Scénario 1 : le document abandonne la porte dérobée** : simule la remise d'un document leurre d'ingénierie sociale.</span><span class="sxs-lookup"><span data-stu-id="abd37-122">**Scenario 1: Document drops backdoor** - simulates delivery of a socially engineered lure document.</span></span> <span data-ttu-id="abd37-123">Le document lance une porte dérobée spécialement conçue pour donner le contrôle aux attaquants.</span><span class="sxs-lookup"><span data-stu-id="abd37-123">The document launches a specially crafted backdoor that gives attackers control.</span></span>

   - <span data-ttu-id="abd37-124">**Scénario 2** : script PowerShell dans une attaque sans fichier : simule une attaque sans fichier qui s'appuie sur PowerShell, présentant la réduction de la surface d'attaque et la détection de l'apprentissage de l'activité de mémoire malveillante.</span><span class="sxs-lookup"><span data-stu-id="abd37-124">**Scenario 2: PowerShell script in fileless attack** - simulates a fileless attack that relies on PowerShell, showcasing attack surface reduction and device learning detection of malicious memory activity.</span></span>
    
   - <span data-ttu-id="abd37-125">**Scénario 3 : réponse** automatisée aux incidents : déclenche une enquête automatisée, qui recherche et remédie automatiquement aux artefacts de violation pour mettre à l'échelle votre capacité de réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="abd37-125">**Scenario 3: Automated incident response** - triggers automated investigation, which automatically hunts for and remediates breach artifacts to scale your incident response capacity.</span></span>

2. <span data-ttu-id="abd37-126">Téléchargez et lisez le document de la walkthrough correspondant fourni avec votre scénario sélectionné.</span><span class="sxs-lookup"><span data-stu-id="abd37-126">Download and read the corresponding walkthrough document provided with your selected scenario.</span></span>

3. <span data-ttu-id="abd37-127">Téléchargez le fichier de simulation ou copiez le script de simulation en naviguant vers l'aide  >  **simulations & didacticiels**.</span><span class="sxs-lookup"><span data-stu-id="abd37-127">Download the simulation file or copy the simulation script by navigating to **Help** > **Simulations & tutorials**.</span></span> <span data-ttu-id="abd37-128">Vous pouvez choisir de télécharger le fichier ou le script sur le périphérique de test, mais ce n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="abd37-128">You can choose to download the file or script on the test device but it's not mandatory.</span></span>

4. <span data-ttu-id="abd37-129">Exécutez le fichier ou le script de simulation sur le périphérique de test comme indiqué dans le document pas à pas.</span><span class="sxs-lookup"><span data-stu-id="abd37-129">Run the simulation file or script on the test device as instructed in the walkthrough document.</span></span>

> [!NOTE]
> <span data-ttu-id="abd37-130">Les fichiers ou scripts de simulation imitent l'activité d'attaque, mais sont en réalité anodins et ne compromettent pas ou ne compromettent pas le périphérique de test.</span><span class="sxs-lookup"><span data-stu-id="abd37-130">Simulation files or scripts mimic attack activity but are actually benign and will not harm or compromise the test device.</span></span>
> 
> 
> <span data-ttu-id="abd37-131">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="abd37-131">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="abd37-132">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="abd37-132">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-attacksimulations-belowfoldlink)


## <a name="related-topics"></a><span data-ttu-id="abd37-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abd37-133">Related topics</span></span>

- [<span data-ttu-id="abd37-134">Intégration des appareils</span><span class="sxs-lookup"><span data-stu-id="abd37-134">Onboard devices</span></span>](onboard-configure.md)
- [<span data-ttu-id="abd37-135">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="abd37-135">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
