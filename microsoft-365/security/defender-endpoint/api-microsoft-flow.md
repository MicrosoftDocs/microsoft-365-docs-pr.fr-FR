---
title: Connecteur de flux Microsoft Defender ATP
ms.reviewer: ''
description: Utilisez le connecteur de flux Microsoft Defender ATP pour automatiser la sécurité et créer un flux qui sera déclenché chaque fois qu’une nouvelle alerte se produit sur votre client.
keywords: flux, api pris en charge, api, flux Microsoft, requête, automatisation
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
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6fd210ddfb8e3ab6e4f1f4ffc0635c8b813e3a07
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163386"
---
# <a name="microsoft-power-automate-formerly-microsoft-flow-and-azure-functions"></a><span data-ttu-id="75bd6-104">Microsoft Power Automate (anciennement Microsoft Flow) et Azure Functions</span><span class="sxs-lookup"><span data-stu-id="75bd6-104">Microsoft Power Automate (formerly Microsoft Flow), and Azure Functions</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="75bd6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="75bd6-105">**Applies to:**</span></span>
- [<span data-ttu-id="75bd6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="75bd6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="75bd6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="75bd6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


- <span data-ttu-id="75bd6-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="75bd6-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="75bd6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="75bd6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="75bd6-110">L’automatisation des procédures de sécurité est une exigence standard pour chaque centre des opérations de sécurité moderne.</span><span class="sxs-lookup"><span data-stu-id="75bd6-110">Automating security procedures is a standard requirement for every modern Security Operations Center.</span></span> <span data-ttu-id="75bd6-111">L’absence de cyber-défenseurs professionnels force SOC à travailler de la manière la plus efficace et l’automatisation est une chose à faire.</span><span class="sxs-lookup"><span data-stu-id="75bd6-111">The lack of professional cyber defenders forces SOC to work in the most efficient way and automation is a must.</span></span> <span data-ttu-id="75bd6-112">Microsoft Power Automate prend en charge différents connecteurs qui ont été créés exactement pour cela.</span><span class="sxs-lookup"><span data-stu-id="75bd6-112">Microsoft Power Automate supports different connectors that were built exactly for that.</span></span> <span data-ttu-id="75bd6-113">Vous pouvez créer une automatisation de procédure de bout en bout en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="75bd6-113">You can build an end-to-end procedure automation within a few minutes.</span></span>

<span data-ttu-id="75bd6-114">L’API Microsoft Defender dispose d’un connecteur de flux officiel avec de nombreuses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="75bd6-114">Microsoft Defender API has an official Flow Connector with many capabilities.</span></span>

![Image de modification des informations d’identification1](images/api-flow-0.png)

> [!NOTE]
> <span data-ttu-id="75bd6-116">Pour plus d’informations sur les conditions préalables de licence des connecteurs premium, voir [Licensing for premium connectors](https://docs.microsoft.com/power-automate/triggers-introduction#licensing-for-premium-connectors).</span><span class="sxs-lookup"><span data-stu-id="75bd6-116">For more details about premium connectors licensing prerequisites, see [Licensing for premium connectors](https://docs.microsoft.com/power-automate/triggers-introduction#licensing-for-premium-connectors).</span></span>


## <a name="usage-example"></a><span data-ttu-id="75bd6-117">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="75bd6-117">Usage example</span></span>

<span data-ttu-id="75bd6-118">L’exemple suivant montre comment créer un flux déclenché chaque fois qu’une nouvelle alerte se produit sur votre client.</span><span class="sxs-lookup"><span data-stu-id="75bd6-118">The following example demonstrates how to create a Flow that is triggered any time a new Alert occurs on your tenant.</span></span>

1. <span data-ttu-id="75bd6-119">Connectez-vous [à Microsoft Power Automate.](https://flow.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="75bd6-119">Log in to [Microsoft Power Automate](https://flow.microsoft.com).</span></span>

2. <span data-ttu-id="75bd6-120">Go to **My flows**  >  **New**  >  **Automated-from blank**.</span><span class="sxs-lookup"><span data-stu-id="75bd6-120">Go to **My flows** > **New** > **Automated-from blank**.</span></span>

    ![Image de modification des informations d’identification2](images/api-flow-1.png)

3. <span data-ttu-id="75bd6-122">Choisissez un nom pour votre flux, recherchez « Déclencheurs Microsoft Defender ATP » comme déclencheur, puis sélectionnez le nouveau déclencheur Alertes.</span><span class="sxs-lookup"><span data-stu-id="75bd6-122">Choose a name for your Flow, search for "Microsoft Defender ATP Triggers" as the trigger, and then select the new Alerts trigger.</span></span>

    ![Image de modification des informations d’identification3](images/api-flow-2.png)

<span data-ttu-id="75bd6-124">Vous avez maintenant un flux qui est déclenché chaque fois qu’une nouvelle alerte se produit.</span><span class="sxs-lookup"><span data-stu-id="75bd6-124">Now you have a Flow that is triggered every time a new Alert occurs.</span></span>

![Image de modification des informations d’identification4](images/api-flow-3.png)

<span data-ttu-id="75bd6-126">Il vous suffit maintenant de choisir les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="75bd6-126">All you need to do now is choose your next steps.</span></span>
<span data-ttu-id="75bd6-127">Par exemple, vous pouvez isoler l’appareil si la gravité de l’alerte est élevée et envoyer un e-mail à son sujet.</span><span class="sxs-lookup"><span data-stu-id="75bd6-127">For example, you can isolate the device if the Severity of the Alert is High and send an email about it.</span></span>
<span data-ttu-id="75bd6-128">Le déclencheur d’alerte fournit uniquement l’ID d’alerte et l’ID de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="75bd6-128">The Alert trigger provides only the Alert ID and the Machine ID.</span></span> <span data-ttu-id="75bd6-129">Vous pouvez utiliser le connecteur pour développer ces entités.</span><span class="sxs-lookup"><span data-stu-id="75bd6-129">You can use the connector to expand these entities.</span></span>

### <a name="get-the-alert-entity-using-the-connector"></a><span data-ttu-id="75bd6-130">Obtenir l’entité Alerte à l’aide du connecteur</span><span class="sxs-lookup"><span data-stu-id="75bd6-130">Get the Alert entity using the connector</span></span>

1. <span data-ttu-id="75bd6-131">Choisissez **Microsoft Defender ATP** pour la nouvelle étape.</span><span class="sxs-lookup"><span data-stu-id="75bd6-131">Choose **Microsoft Defender ATP** for the new step.</span></span>

2. <span data-ttu-id="75bd6-132">Choose **Alerts - Get single alert API**.</span><span class="sxs-lookup"><span data-stu-id="75bd6-132">Choose **Alerts - Get single alert API**.</span></span>

3. <span data-ttu-id="75bd6-133">Définissez **l’ID d’alerte** de la dernière étape en tant **qu’entrée.**</span><span class="sxs-lookup"><span data-stu-id="75bd6-133">Set the **Alert ID** from the last step as **Input**.</span></span>

    ![Image de modification des informations d’identification5](images/api-flow-4.png)

### <a name="isolate-the-device-if-the-alerts-severity-is-high"></a><span data-ttu-id="75bd6-135">Isoler l’appareil si la gravité de l’alerte est élevée</span><span class="sxs-lookup"><span data-stu-id="75bd6-135">Isolate the device if the Alert's severity is High</span></span>

1. <span data-ttu-id="75bd6-136">Ajoutez **condition** en tant que nouvelle étape.</span><span class="sxs-lookup"><span data-stu-id="75bd6-136">Add **Condition** as a new step.</span></span>

2. <span data-ttu-id="75bd6-137">Vérifiez si la gravité de **l’alerte est égale à** Élevée.</span><span class="sxs-lookup"><span data-stu-id="75bd6-137">Check if the Alert severity **is equal to** High.</span></span>

   <span data-ttu-id="75bd6-138">Si oui, ajoutez **l’action Microsoft Defender ATP - Isoler l’ordinateur** avec l’ID de l’ordinateur et un commentaire.</span><span class="sxs-lookup"><span data-stu-id="75bd6-138">If yes, add the **Microsoft Defender ATP - Isolate machine** action with the Machine ID and a comment.</span></span>

    ![Image de modification des informations d’identification6](images/api-flow-5.png)

3. <span data-ttu-id="75bd6-140">Ajoutez une nouvelle étape pour l’envoi par courrier électronique de l’alerte et de l’isolation.</span><span class="sxs-lookup"><span data-stu-id="75bd6-140">Add a new step for emailing about the Alert and the Isolation.</span></span> <span data-ttu-id="75bd6-141">Il existe plusieurs connecteurs de messagerie très faciles à utiliser, tels qu’Outlook ou Gmail.</span><span class="sxs-lookup"><span data-stu-id="75bd6-141">There are multiple email connectors that are very easy to use, such as Outlook or Gmail.</span></span>

4. <span data-ttu-id="75bd6-142">Enregistrez votre flux.</span><span class="sxs-lookup"><span data-stu-id="75bd6-142">Save your flow.</span></span>

<span data-ttu-id="75bd6-143">Vous pouvez également créer un **flux programmé** qui exécute des requêtes de recherche avancée, et bien plus encore !</span><span class="sxs-lookup"><span data-stu-id="75bd6-143">You can also create a **scheduled** flow that runs Advanced Hunting queries and much more!</span></span>

## <a name="related-topic"></a><span data-ttu-id="75bd6-144">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="75bd6-144">Related topic</span></span>
- [<span data-ttu-id="75bd6-145">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="75bd6-145">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)
