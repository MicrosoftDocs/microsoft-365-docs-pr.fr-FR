---
title: Simulation d’une attaque par hameçonnage avec Microsoft Defender pour Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
description: Les administrateurs peuvent apprendre à simuler des attaques par hameçonnage et former leurs utilisateurs à la prévention du hameçonnage à l’aide de la formation à la simulation d’attaque de Microsoft Defender pour Office 365.
ms.openlocfilehash: 3707041067fd76ee9535d0dccf5cdfcb9d74fbd7
ms.sourcegitcommit: 1a9f0f878c045e1ddd59088ca2a94397605a242a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49667556"
---
# <a name="simulate-a-phishing-attack"></a><span data-ttu-id="2a97b-103">Simulation d’une attaque par hameçonnage</span><span class="sxs-lookup"><span data-stu-id="2a97b-103">Simulate a phishing attack</span></span>

<span data-ttu-id="2a97b-104">La formation sur la simulation d’attaque de Microsoft Defender pour Office 365 vous permet d’exécuter des simulations Cyber inoffensives sur votre organisation afin de tester vos stratégies et pratiques de sécurité, ainsi que de former vos employés à améliorer leur sensibilisation et à réduire leur susceptibilité aux attaques.</span><span class="sxs-lookup"><span data-stu-id="2a97b-104">Attack simulator training in Microsoft Defender for Office 365 lets you run benign cyberattack simulations on your organization to test your security policies and practices, as well as train your employees to increase their awareness and decrease their susceptibility to attacks.</span></span> <span data-ttu-id="2a97b-105">Cet article vous guide tout au long de la création d’une attaque par hameçonnage simulée à l’aide d’une formation sur une simulation d’attaque.</span><span class="sxs-lookup"><span data-stu-id="2a97b-105">This article walks you through creating  a simulated phishing attack using attack simulator training.</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="2a97b-106">Pour lancer une attaque par hameçonnage simulée, ouvrez le [Centre de sécurité Microsoft 365](https://security.microsoft.com/), accédez à **messagerie &** \> **simulateur d’attaque** de collaboration et basculez vers l’onglet [**simulations**](https://security.microsoft.com/attacksimulator?viewid=simulations) .</span><span class="sxs-lookup"><span data-stu-id="2a97b-106">To launch a simulated phishing attack, open the [Microsoft 365 security center](https://security.microsoft.com/), go to **Email & collaboration** \> **Attack simulator**, and switch to the [**Simulations**](https://security.microsoft.com/attacksimulator?viewid=simulations) tab.</span></span>

<span data-ttu-id="2a97b-107">Sous **simulations**, sélectionnez **+ lancer une simulation**.</span><span class="sxs-lookup"><span data-stu-id="2a97b-107">Under **Simulations**, select **+ Launch a simulation**.</span></span>

![Lancer un bouton de simulation dans le centre de sécurité Microsoft 365](../../media/attack-sim-preview-launch.png)

> [!NOTE]
> <span data-ttu-id="2a97b-109">À tout moment pendant la création de la simulation, vous pouvez enregistrer et fermer pour poursuivre la configuration de la simulation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2a97b-109">At any point during simulation creation, you can save and close to continue configuring the simulation at a later time.</span></span>

## <a name="selecting-a-social-engineering-technique"></a><span data-ttu-id="2a97b-110">Sélection d’une technique d’ingénierie sociale</span><span class="sxs-lookup"><span data-stu-id="2a97b-110">Selecting a social engineering technique</span></span>

<span data-ttu-id="2a97b-111">Vous avez le choix entre 4 techniques différentes, organisée à partir de la [Mitre ATT&CK® Framework](https://attack.mitre.org/techniques/enterprise/).</span><span class="sxs-lookup"><span data-stu-id="2a97b-111">Select from 4 different techniques, curated from the [MITRE ATT&CK® framework](https://attack.mitre.org/techniques/enterprise/).</span></span> <span data-ttu-id="2a97b-112">Différentes charges utiles sont disponibles pour différentes techniques :</span><span class="sxs-lookup"><span data-stu-id="2a97b-112">Different payloads are available for different techniques:</span></span>

- <span data-ttu-id="2a97b-113">La collecte des **informations d’identification** tente de collecter les informations d’identification en mettant les utilisateurs à un site Web de présentation bien connu avec des zones de saisie pour envoyer un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2a97b-113">**Credential harvest** attempts to collect credentials by taking users to a well-known looking website with input boxes to submit a username and password.</span></span>
- <span data-ttu-id="2a97b-114">Une **pièce jointe malveillante** ajoute une pièce jointe malveillante à un message.</span><span class="sxs-lookup"><span data-stu-id="2a97b-114">**Malware attachment** adds a malicious attachment to a message.</span></span> <span data-ttu-id="2a97b-115">Lorsque l’utilisateur ouvre la pièce jointe, du code arbitraire est exécuté, ce qui permet à l’agresseur de compromettre l’appareil de la cible.</span><span class="sxs-lookup"><span data-stu-id="2a97b-115">When the user opens the attachment, arbitrary code is run that will help the attacker compromise the target's device.</span></span>
- <span data-ttu-id="2a97b-116">Le **lien dans la pièce jointe** est un type hybride de collecte des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="2a97b-116">**Link in attachment** is a type of credential harvest hybrid.</span></span> <span data-ttu-id="2a97b-117">Un agresseur insère une URL dans une pièce jointe de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="2a97b-117">An attacker inserts a URL into an email attachment.</span></span> <span data-ttu-id="2a97b-118">L’URL dans la pièce jointe suit la même technique que la collecte des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="2a97b-118">The URL within the attachment follows the same technique as credential harvest.</span></span>
- <span data-ttu-id="2a97b-119">Un **lien vers un programme malveillant** exécute un code arbitraire à partir d’un fichier hébergé sur un service de partage de fichiers connu.</span><span class="sxs-lookup"><span data-stu-id="2a97b-119">**Link to malware** will run some arbitrary code from a file hosted on a well-known file sharing service.</span></span> <span data-ttu-id="2a97b-120">Le message envoyé à l’utilisateur contient un lien vers ce fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="2a97b-120">The message sent to the user will contain a link to this malicious file.</span></span> <span data-ttu-id="2a97b-121">Ouvrir le fichier et aider l’agresseur à compromettre l’appareil de la cible.</span><span class="sxs-lookup"><span data-stu-id="2a97b-121">Opening the file and help the attacker compromise the target's device.</span></span>

> [!TIP]
> <span data-ttu-id="2a97b-122">En cliquant sur **afficher les détails** dans la description de chaque technique, vous affichez des informations supplémentaires et les étapes de simulation de la technique.</span><span class="sxs-lookup"><span data-stu-id="2a97b-122">Clicking on **View details** within the description of each technique will display further information and the simulation steps for the technique.</span></span>
>
> ![Étapes de simulation pour la collecte des informations d’identification dans le centre de sécurité de Microsoft 365](../../media/attack-sim-preview-sim-steps.png)

<span data-ttu-id="2a97b-124">Une fois que vous avez sélectionné la technique et cliqué sur **suivant**, donnez un nom à votre simulation et éventuellement une description.</span><span class="sxs-lookup"><span data-stu-id="2a97b-124">After you've selected the technique and clicked on **Next**, give your simulation a name and optionally a description.</span></span>

## <a name="selecting-a-payload"></a><span data-ttu-id="2a97b-125">Sélection d’une charge utile</span><span class="sxs-lookup"><span data-stu-id="2a97b-125">Selecting a payload</span></span>

<span data-ttu-id="2a97b-126">Ensuite, vous devez sélectionner une charge utile dans le catalogue de charge utile préexistant.</span><span class="sxs-lookup"><span data-stu-id="2a97b-126">Next, you'll need to either select a payload from the pre-existing payload catalog.</span></span>

<span data-ttu-id="2a97b-127">Les charges utiles comportent un certain nombre de points de données pour vous aider à choisir :</span><span class="sxs-lookup"><span data-stu-id="2a97b-127">Payloads have a number of data points to help you choose:</span></span>

- <span data-ttu-id="2a97b-128">**Cliquer sur** le nombre de taux indique combien de personnes ont cliqué sur cette charge utile.</span><span class="sxs-lookup"><span data-stu-id="2a97b-128">**Click rate** counts how many people clicked this payload.</span></span>
- <span data-ttu-id="2a97b-129">**Taux de compromissions prévues** prédit le pourcentage de personnes qui seront compromises par cette charge utile en fonction des données historiques de la charge utile pour les clients de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="2a97b-129">**Predicted compromise rate** predicts the percentage of people that will get compromised by this payload based on historical data for the payload across Microsoft Defender for Office 365 customers.</span></span>
- <span data-ttu-id="2a97b-130">**Simulations lancées** compte le nombre de fois que cette charge utile a été utilisée dans d’autres simulations.</span><span class="sxs-lookup"><span data-stu-id="2a97b-130">**Simulations launched** counts the number of times this payload was used in other simulations.</span></span>
- <span data-ttu-id="2a97b-131">La **complexité**, disponible par le biais de **filtres**, est calculée en fonction du nombre d’indicateurs au sein de la charge utile qui permettent aux cibles de l’informatique d’être une attaque.</span><span class="sxs-lookup"><span data-stu-id="2a97b-131">**Complexity**, available through **filters**, is calculated based on the number of indicators within the payload that clue targets in on it being an attack.</span></span> <span data-ttu-id="2a97b-132">Un plus grand nombre d’indicateurs entraîne une complexité moindre.</span><span class="sxs-lookup"><span data-stu-id="2a97b-132">More indicators lead to lower complexity.</span></span>
- <span data-ttu-id="2a97b-133">**Source**, disponible par le biais de **filtres**, indique si la charge utile a été créée sur votre client ou fait partie du catalogue de charge utile préexistant de Microsoft (Global).</span><span class="sxs-lookup"><span data-stu-id="2a97b-133">**Source**, available through **filters**, indicates whether the payload was created on your tenant or is a part of Microsoft's pre-existing payload catalog (global).</span></span>

![Charge utile sélectionnée lors de la formation à la simulation d’attaque dans le centre de sécurité Microsoft 365](../../media/attack-sim-preview-select-payload.png)

<span data-ttu-id="2a97b-135">Sélectionnez une charge utile dans la liste pour afficher un aperçu de la charge utile avec des informations supplémentaires le concernant.</span><span class="sxs-lookup"><span data-stu-id="2a97b-135">Select a payload from the list to see a preview of the payload with additional information about it.</span></span>

<span data-ttu-id="2a97b-136">Si vous souhaitez créer votre propre charge utile, lisez [Create a Payload for Attack Simulation Training](attack-simulation-training-payloads.md).</span><span class="sxs-lookup"><span data-stu-id="2a97b-136">If you'd like to create your own payload, read [create a payload for attack simulation training](attack-simulation-training-payloads.md).</span></span>

## <a name="audience-targeting"></a><span data-ttu-id="2a97b-137">Ciblage d’audience</span><span class="sxs-lookup"><span data-stu-id="2a97b-137">Audience targeting</span></span>

<span data-ttu-id="2a97b-138">À présent, il est temps de sélectionner l’audience de cette simulation.</span><span class="sxs-lookup"><span data-stu-id="2a97b-138">Now it's time to select this simulation's audience.</span></span> <span data-ttu-id="2a97b-139">Vous pouvez choisir d' **inclure tous les utilisateurs de votre organisation** ou d' **inclure uniquement des utilisateurs et des groupes spécifiques**.</span><span class="sxs-lookup"><span data-stu-id="2a97b-139">You can choose to **include all users in your organization** or **include only specific users and groups**.</span></span>

<span data-ttu-id="2a97b-140">Lorsque vous choisissez d' **inclure uniquement des utilisateurs et des groupes spécifiques,** vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="2a97b-140">When you choose to **include only specific users and groups** you can either:</span></span>

- <span data-ttu-id="2a97b-141">**Ajoutez des utilisateurs**, ce qui vous permet d’utiliser la recherche pour votre client, ainsi que les fonctionnalités avancées de recherche et de filtrage, telles que le ciblage des utilisateurs qui n’ont pas été ciblés par une simulation au cours des 3 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="2a97b-141">**Add users**, which allows you to leverage search for your tenant, as well as advanced search and filtering capabilities, like targeting users who haven't been targeted by a simulation in the last 3 months.</span></span>
  <span data-ttu-id="2a97b-142">![Filtrage des utilisateurs dans formation à la simulation d’attaque sur le centre de sécurité Microsoft 365](../../media/attack-sim-preview-user-targeting.png)</span><span class="sxs-lookup"><span data-stu-id="2a97b-142">![User filtering in attack simulation training on Microsoft 365 security center](../../media/attack-sim-preview-user-targeting.png)</span></span>
- <span data-ttu-id="2a97b-143">**Importer à partir de CSV** vous permet d’importer un ensemble prédéfini d’utilisateurs pour cette simulation.</span><span class="sxs-lookup"><span data-stu-id="2a97b-143">**Import from CSV** allows you to import a predefined set of users for this simulation.</span></span>

## <a name="assigning-training"></a><span data-ttu-id="2a97b-144">Affectation d’une formation</span><span class="sxs-lookup"><span data-stu-id="2a97b-144">Assigning training</span></span>

<span data-ttu-id="2a97b-145">Nous vous recommandons d’attribuer une formation à chaque simulation, car les employés qui passent par la formation sont moins exposés aux attaques similaires.</span><span class="sxs-lookup"><span data-stu-id="2a97b-145">We recommend that you assign training for each simulation, as employees who go through training are less susceptible to similar attacks.</span></span>

<span data-ttu-id="2a97b-146">Vous pouvez choisir de recevoir une formation ou sélectionner des cours de formation et des modules vous-même.</span><span class="sxs-lookup"><span data-stu-id="2a97b-146">You can either choose to have training assigned for you or select training courses and modules yourself.</span></span>

<span data-ttu-id="2a97b-147">Sélectionnez la **Date d’échéance** de la formation pour vous assurer que les employés terminent leur formation en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="2a97b-147">Select the **training due date** to make sure employees finish their training in a timely manner.</span></span>

> [!NOTE]
> <span data-ttu-id="2a97b-148">Si vous choisissez de sélectionner des cours et des modules vous-même, vous pourrez toujours voir le contenu recommandé, ainsi que tous les cours et modules disponibles.</span><span class="sxs-lookup"><span data-stu-id="2a97b-148">If you choose to select courses and modules yourself, you'll still be able to see the recommended content as well as all available courses and modules.</span></span>
>
> ![Ajout de formations recommandées lors de la formation à la simulation d’attaque dans le centre de sécurité Microsoft 365](../../media/attack-sim-preview-add-training.png)

<span data-ttu-id="2a97b-150">Dans les étapes suivantes, vous devrez **Ajouter des formations** si vous avez choisi de le sélectionner vous-même et personnalisez votre page d’accueil de formation.</span><span class="sxs-lookup"><span data-stu-id="2a97b-150">In the next steps you'll need to **Add trainings** if you opted to select it yourself, and customize your training landing page.</span></span> <span data-ttu-id="2a97b-151">Vous pouvez afficher un aperçu de la page d’accueil de la formation, ainsi que modifier l’en-tête et le corps de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="2a97b-151">You'll be able to preview the training landing page, as well as change the header and body of it.</span></span>

## <a name="launch-details-and-review"></a><span data-ttu-id="2a97b-152">Détails du lancement et révision</span><span class="sxs-lookup"><span data-stu-id="2a97b-152">Launch details and review</span></span>

<span data-ttu-id="2a97b-153">Maintenant que tout est configuré, vous pouvez lancer cette simulation immédiatement ou la planifier à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2a97b-153">Now that everything is configured, you can launch this simulation immediately or schedule it for a later date.</span></span> <span data-ttu-id="2a97b-154">Vous devrez également choisir quand mettre fin à cette simulation.</span><span class="sxs-lookup"><span data-stu-id="2a97b-154">You will also need to choose when to end this simulation.</span></span> <span data-ttu-id="2a97b-155">Nous allons arrêter de capturer l’interaction avec cette simulation au-delà de la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2a97b-155">We will stop capturing interaction with this simulation past the selected time.</span></span>

<span data-ttu-id="2a97b-156">**Activer la fourniture de fuseau horaire prenant en charge la région** pour transmettre des messages d’attaque simulés à vos employés pendant leurs heures de travail en fonction de leur région.</span><span class="sxs-lookup"><span data-stu-id="2a97b-156">**Enable region aware timezone delivery** to deliver simulated attack messages to your employees during their working hours based on their region.</span></span>

<span data-ttu-id="2a97b-157">Une fois que vous avez fini, cliquez sur **suivant** et examinez les détails de votre simulation.</span><span class="sxs-lookup"><span data-stu-id="2a97b-157">Once you're done, click on **Next** and review the details of your simulation.</span></span> <span data-ttu-id="2a97b-158">Cliquez sur **modifier** sur l’un des composants pour revenir en arrière et modifier les détails à modifier.</span><span class="sxs-lookup"><span data-stu-id="2a97b-158">Click on **Edit** on any of the parts to go back and change any details that need changing.</span></span> <span data-ttu-id="2a97b-159">Une fois l’opération terminée, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="2a97b-159">Once done, click **Submit**.</span></span>
