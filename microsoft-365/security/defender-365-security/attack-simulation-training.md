---
title: Simuler une attaque par hameçonnage avec Microsoft Defender pour Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.prod: m365-security
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs peuvent apprendre à simuler des attaques par hameçonnage et à former leurs utilisateurs à la prévention du hameçonnage à l’aide de la formation sur la simulation d’attaques dans Microsoft Defender pour Office 365.
ms.technology: mdo
ms.openlocfilehash: 27279f927a15ea94ae84112ffdc23d88ea42d2ff
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51065478"
---
# <a name="simulate-a-phishing-attack"></a><span data-ttu-id="d2aad-103">Simuler une attaque par hameçonnage</span><span class="sxs-lookup"><span data-stu-id="d2aad-103">Simulate a phishing attack</span></span>

<span data-ttu-id="d2aad-104">La formation sur la simulation d’attaques dans Microsoft Defender pour Office 365 vous permet d’exécuter des simulations de cyberattaque anodins sur votre organisation pour tester vos stratégies et pratiques de sécurité, ainsi que pour former vos employés afin qu’ils augmentent leur sensibilisation et diminuent leur tendance aux attaques.</span><span class="sxs-lookup"><span data-stu-id="d2aad-104">Attack simulation training in Microsoft Defender for Office 365 lets you run benign cyberattack simulations on your organization to test your security policies and practices, as well as train your employees to increase their awareness and decrease their susceptibility to attacks.</span></span> <span data-ttu-id="d2aad-105">Cet article vous explique la création d’une attaque par hameçonnage simulée à l’aide d’une formation à la simulation d’attaque.</span><span class="sxs-lookup"><span data-stu-id="d2aad-105">This article walks you through creating  a simulated phishing attack using attack simulation training.</span></span>

<span data-ttu-id="d2aad-106">Pour plus d’informations sur la formation à la simulation d’attaques, voir [Commencer à utiliser la formation sur la simulation d’attaque.](attack-simulation-training-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="d2aad-106">For getting started information about Attack simulation training, see [Get started using Attack simulation training](attack-simulation-training-get-started.md).</span></span>

<span data-ttu-id="d2aad-107">Pour lancer une attaque par hameçonnage simulée, ouvrez le Centre de sécurité [Microsoft 365,](https://security.microsoft.com/)passez à la formation sur la simulation d’attaques par **e-mail & collaboration** et passez à l’onglet \>  [**Simulations.**](https://security.microsoft.com/attacksimulator?viewid=simulations)</span><span class="sxs-lookup"><span data-stu-id="d2aad-107">To launch a simulated phishing attack, open the [Microsoft 365 security center](https://security.microsoft.com/), go to **Email & collaboration** \> **Attack simulation training**, and switch to the [**Simulations**](https://security.microsoft.com/attacksimulator?viewid=simulations) tab.</span></span>

<span data-ttu-id="d2aad-108">Sous **Simulations,** **sélectionnez + Lancer une simulation.**</span><span class="sxs-lookup"><span data-stu-id="d2aad-108">Under **Simulations**, select **+ Launch a simulation**.</span></span>

![Lancer un bouton de simulation dans le Centre de sécurité Microsoft 365](../../media/attack-sim-preview-launch.png)

> [!NOTE]
> <span data-ttu-id="d2aad-110">À tout moment lors de la création de la simulation, vous pouvez enregistrer et fermer pour continuer à configurer la simulation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d2aad-110">At any point during simulation creation, you can save and close to continue configuring the simulation at a later time.</span></span>

## <a name="selecting-a-social-engineering-technique"></a><span data-ttu-id="d2aad-111">Sélection d’une technique d’ingénierie sociale</span><span class="sxs-lookup"><span data-stu-id="d2aad-111">Selecting a social engineering technique</span></span>

<span data-ttu-id="d2aad-112">Sélectionnez parmi 4 techniques différentes, organisées à partir de l’infrastructure&[CK ® MITRE ATT.](https://attack.mitre.org/techniques/enterprise/)</span><span class="sxs-lookup"><span data-stu-id="d2aad-112">Select from 4 different techniques, curated from the [MITRE ATT&CK® framework](https://attack.mitre.org/techniques/enterprise/).</span></span> <span data-ttu-id="d2aad-113">Différentes charges utiles sont disponibles pour différentes techniques :</span><span class="sxs-lookup"><span data-stu-id="d2aad-113">Different payloads are available for different techniques:</span></span>

- <span data-ttu-id="d2aad-114">**La collecte des** informations d’identification tente de collecter des informations d’identification en prenant les utilisateurs vers un site web bien connu avec des zones de saisie pour envoyer un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d2aad-114">**Credential harvest** attempts to collect credentials by taking users to a well-known looking website with input boxes to submit a username and password.</span></span>
- <span data-ttu-id="d2aad-115">**Une pièce jointe malveillante** ajoute une pièce jointe malveillante à un message.</span><span class="sxs-lookup"><span data-stu-id="d2aad-115">**Malware attachment** adds a malicious attachment to a message.</span></span> <span data-ttu-id="d2aad-116">Lorsque l’utilisateur ouvre la pièce jointe, du code arbitraire est exécuté pour aider l’attaquant à compromettre l’appareil de la cible.</span><span class="sxs-lookup"><span data-stu-id="d2aad-116">When the user opens the attachment, arbitrary code is run that will help the attacker compromise the target's device.</span></span>
- <span data-ttu-id="d2aad-117">**Le lien dans la pièce jointe** est un type d’hybride de la saisie des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d2aad-117">**Link in attachment** is a type of credential harvest hybrid.</span></span> <span data-ttu-id="d2aad-118">Un attaquant insère une URL dans une pièce jointe d’un e-mail.</span><span class="sxs-lookup"><span data-stu-id="d2aad-118">An attacker inserts a URL into an email attachment.</span></span> <span data-ttu-id="d2aad-119">L’URL dans la pièce jointe suit la même technique que la saisie des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d2aad-119">The URL within the attachment follows the same technique as credential harvest.</span></span>
- <span data-ttu-id="d2aad-120">**Un lien vers un programme** malveillant exécutera du code arbitraire à partir d’un fichier hébergé sur un service de partage de fichiers connu.</span><span class="sxs-lookup"><span data-stu-id="d2aad-120">**Link to malware** will run some arbitrary code from a file hosted on a well-known file sharing service.</span></span> <span data-ttu-id="d2aad-121">Le message envoyé à l’utilisateur contient un lien vers ce fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="d2aad-121">The message sent to the user will contain a link to this malicious file.</span></span> <span data-ttu-id="d2aad-122">Ouverture du fichier et aide l’attaquant à compromettre l’appareil de la cible.</span><span class="sxs-lookup"><span data-stu-id="d2aad-122">Opening the file and help the attacker compromise the target's device.</span></span>
- <span data-ttu-id="d2aad-123">**L’URL de** lecteur par est l’endroit où l’URL malveillante dans le message conduit l’utilisateur vers un site web familier qui s’exécute en mode silencieux et/ou installe le code de code sur l’appareil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2aad-123">**Drive-by URL** is where the malicious URL in the message takes the user to a familiar-looking website that silently runs and/or installs code code on the user's device.</span></span>

> [!TIP]
> <span data-ttu-id="d2aad-124">Le fait de cliquer sur **Afficher les détails** dans la description de chaque technique permet d’afficher des informations supplémentaires et les étapes de simulation de la technique.</span><span class="sxs-lookup"><span data-stu-id="d2aad-124">Clicking on **View details** within the description of each technique will display further information and the simulation steps for the technique.</span></span>
>
> ![Étapes de simulation pour la recherche d’informations d’identification dans le cadre d’une formation sur la simulation d’attaques dans le Centre de sécurité Microsoft 365](../../media/attack-sim-preview-sim-steps.png)

<span data-ttu-id="d2aad-126">Une fois que vous avez sélectionné la technique et cliqué sur **Suivant,** donnez à votre simulation un nom et éventuellement une description.</span><span class="sxs-lookup"><span data-stu-id="d2aad-126">After you've selected the technique and clicked on **Next**, give your simulation a name and optionally a description.</span></span>

## <a name="selecting-a-payload"></a><span data-ttu-id="d2aad-127">Sélection d’une charge utile</span><span class="sxs-lookup"><span data-stu-id="d2aad-127">Selecting a payload</span></span>

<span data-ttu-id="d2aad-128">Ensuite, vous devez sélectionner une charge utile dans le catalogue de charge utile pré-existant.</span><span class="sxs-lookup"><span data-stu-id="d2aad-128">Next, you'll need to either select a payload from the pre-existing payload catalog.</span></span>

<span data-ttu-id="d2aad-129">Les charges utiles ont un certain nombre de points de données pour vous aider à choisir :</span><span class="sxs-lookup"><span data-stu-id="d2aad-129">Payloads have a number of data points to help you choose:</span></span>

- <span data-ttu-id="d2aad-130">**Le taux de** clics compte le nombre de personnes qui ont cliqué sur cette charge utile.</span><span class="sxs-lookup"><span data-stu-id="d2aad-130">**Click rate** counts how many people clicked this payload.</span></span>
- <span data-ttu-id="d2aad-131">**Le taux de compromission** prévu prévoit le pourcentage de personnes qui seront compromises par cette charge utile en fonction des données historiques de la charge utile pour les clients Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="d2aad-131">**Predicted compromise rate** predicts the percentage of people that will get compromised by this payload based on historical data for the payload across Microsoft Defender for Office 365 customers.</span></span>
- <span data-ttu-id="d2aad-132">**Les simulations lancées** comptent le nombre de fois que cette charge utile a été utilisée dans d’autres simulations.</span><span class="sxs-lookup"><span data-stu-id="d2aad-132">**Simulations launched** counts the number of times this payload was used in other simulations.</span></span>
- <span data-ttu-id="d2aad-133">**La** complexité, disponible par le biais **de filtres,** est calculée en fonction du nombre d’indicateurs au sein de la charge utile ciblée par des indices en tant qu’attaque.</span><span class="sxs-lookup"><span data-stu-id="d2aad-133">**Complexity**, available through **filters**, is calculated based on the number of indicators within the payload that clue targets in on it being an attack.</span></span> <span data-ttu-id="d2aad-134">Plus il y a d’indicateurs, plus la complexité est faible.</span><span class="sxs-lookup"><span data-stu-id="d2aad-134">More indicators lead to lower complexity.</span></span>
- <span data-ttu-id="d2aad-135">**La source,** disponible **via** des filtres, indique si la charge utile a été créée sur votre client ou fait partie du catalogue de charge utile pré-existant de Microsoft (global).</span><span class="sxs-lookup"><span data-stu-id="d2aad-135">**Source**, available through **filters**, indicates whether the payload was created on your tenant or is a part of Microsoft's pre-existing payload catalog (global).</span></span>

![Charge utile sélectionnée dans la formation sur la simulation d’attaques dans le Centre de sécurité Microsoft 365](../../media/attack-sim-preview-select-payload.png)

<span data-ttu-id="d2aad-137">Sélectionnez une charge utile dans la liste pour afficher un aperçu de la charge utile avec des informations supplémentaires à son sujet.</span><span class="sxs-lookup"><span data-stu-id="d2aad-137">Select a payload from the list to see a preview of the payload with additional information about it.</span></span>

<span data-ttu-id="d2aad-138">Si vous souhaitez créer votre propre charge utile, lisez créer une charge utile pour la formation à la [simulation d’attaques.](attack-simulation-training-payloads.md)</span><span class="sxs-lookup"><span data-stu-id="d2aad-138">If you'd like to create your own payload, read [create a payload for attack simulation training](attack-simulation-training-payloads.md).</span></span>

## <a name="audience-targeting"></a><span data-ttu-id="d2aad-139">Ciblage d’audience</span><span class="sxs-lookup"><span data-stu-id="d2aad-139">Audience targeting</span></span>

<span data-ttu-id="d2aad-140">Il est maintenant temps de sélectionner l’audience de cette simulation.</span><span class="sxs-lookup"><span data-stu-id="d2aad-140">Now it's time to select this simulation's audience.</span></span> <span data-ttu-id="d2aad-141">Vous pouvez choisir **d’inclure tous les utilisateurs de votre** organisation ou d’inclure uniquement des utilisateurs et des groupes **spécifiques.**</span><span class="sxs-lookup"><span data-stu-id="d2aad-141">You can choose to **include all users in your organization** or **include only specific users and groups**.</span></span>

<span data-ttu-id="d2aad-142">Lorsque vous choisissez **d’inclure uniquement des utilisateurs et des groupes spécifiques,** vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="d2aad-142">When you choose to **include only specific users and groups** you can either:</span></span>

- <span data-ttu-id="d2aad-143">Ajoutez des utilisateurs, ce qui vous permet de tirer parti de la recherche pour votre client, ainsi que des fonctionnalités avancées de recherche et de filtrage, telles que le ciblage d’utilisateurs qui n’ont pas été ciblés par une simulation au cours des 3 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="d2aad-143">**Add users**, which allows you to leverage search for your tenant, as well as advanced search and filtering capabilities, like targeting users who haven't been targeted by a simulation in the last 3 months.</span></span>
  <span data-ttu-id="d2aad-144">![Filtrage des utilisateurs lors d’une formation sur la simulation d’attaques sur le Centre de sécurité Microsoft 365](../../media/attack-sim-preview-user-targeting.png)</span><span class="sxs-lookup"><span data-stu-id="d2aad-144">![User filtering in attack simulation training on Microsoft 365 security center](../../media/attack-sim-preview-user-targeting.png)</span></span>
- <span data-ttu-id="d2aad-145">**L’importation à partir de CSV** vous permet d’importer un ensemble prédéféré d’utilisateurs pour cette simulation.</span><span class="sxs-lookup"><span data-stu-id="d2aad-145">**Import from CSV** allows you to import a predefined set of users for this simulation.</span></span>

## <a name="assigning-training"></a><span data-ttu-id="d2aad-146">Affectation d’une formation</span><span class="sxs-lookup"><span data-stu-id="d2aad-146">Assigning training</span></span>

<span data-ttu-id="d2aad-147">Nous vous recommandons d’affecter une formation pour chaque simulation, car les employés qui s’entraînent sont moins susceptibles d’être exposés à des attaques similaires.</span><span class="sxs-lookup"><span data-stu-id="d2aad-147">We recommend that you assign training for each simulation, as employees who go through training are less susceptible to similar attacks.</span></span>

<span data-ttu-id="d2aad-148">Vous pouvez choisir de vous attribuer une formation ou de sélectionner vous-même des cours et des modules de formation.</span><span class="sxs-lookup"><span data-stu-id="d2aad-148">You can either choose to have training assigned for you or select training courses and modules yourself.</span></span>

<span data-ttu-id="d2aad-149">Sélectionnez la **date d’échéance de** la formation pour vous assurer que les employés terminent leur formation en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="d2aad-149">Select the **training due date** to make sure employees finish their training in a timely manner.</span></span>

> [!NOTE]
> <span data-ttu-id="d2aad-150">Si vous choisissez de sélectionner vous-même des cours et des modules, vous pourrez toujours voir le contenu recommandé ainsi que tous les cours et modules disponibles.</span><span class="sxs-lookup"><span data-stu-id="d2aad-150">If you choose to select courses and modules yourself, you'll still be able to see the recommended content as well as all available courses and modules.</span></span>
>
> ![Ajout d’une formation recommandée dans le cadre d’une formation sur la simulation d’attaques dans le Centre de sécurité Microsoft 365](../../media/attack-sim-preview-add-training.png)

<span data-ttu-id="d2aad-152">Dans les étapes **suivantes,** vous devrez ajouter des formations si vous avez choisi de la sélectionner vous-même et de personnaliser votre page d’arrivée de formation.</span><span class="sxs-lookup"><span data-stu-id="d2aad-152">In the next steps you'll need to **Add trainings** if you opted to select it yourself, and customize your training landing page.</span></span> <span data-ttu-id="d2aad-153">Vous pourrez afficher un aperçu de la page d’accueil de formation, ainsi que modifier l’en-tête et le corps de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d2aad-153">You'll be able to preview the training landing page, as well as change the header and body of it.</span></span>

## <a name="launch-details-and-review"></a><span data-ttu-id="d2aad-154">Détails du lancement et révision</span><span class="sxs-lookup"><span data-stu-id="d2aad-154">Launch details and review</span></span>

<span data-ttu-id="d2aad-155">Maintenant que tout est configuré, vous pouvez lancer cette simulation immédiatement ou la planifier pour une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d2aad-155">Now that everything is configured, you can launch this simulation immediately or schedule it for a later date.</span></span> <span data-ttu-id="d2aad-156">Vous devrez également choisir quand mettre fin à cette simulation.</span><span class="sxs-lookup"><span data-stu-id="d2aad-156">You will also need to choose when to end this simulation.</span></span> <span data-ttu-id="d2aad-157">Nous arrêterons la capture de l’interaction avec cette simulation au-delà de l’heure sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d2aad-157">We will stop capturing interaction with this simulation past the selected time.</span></span>

<span data-ttu-id="d2aad-158">**Activez la remise de fuseau horaire** de région pour remettre des messages d’attaque simulée à vos employés pendant leurs heures de travail en fonction de leur région.</span><span class="sxs-lookup"><span data-stu-id="d2aad-158">**Enable region aware timezone delivery** to deliver simulated attack messages to your employees during their working hours based on their region.</span></span>

<span data-ttu-id="d2aad-159">Une fois que vous avez terminé, cliquez sur **Suivant** et examinez les détails de votre simulation.</span><span class="sxs-lookup"><span data-stu-id="d2aad-159">Once you're done, click on **Next** and review the details of your simulation.</span></span> <span data-ttu-id="d2aad-160">Cliquez sur **Modifier** sur l’un des composants pour revenir en arrière et modifier les détails qui doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="d2aad-160">Click on **Edit** on any of the parts to go back and change any details that need changing.</span></span> <span data-ttu-id="d2aad-161">Une fois terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="d2aad-161">Once done, click **Submit**.</span></span>