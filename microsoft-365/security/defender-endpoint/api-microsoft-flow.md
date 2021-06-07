---
title: Connecteur d’Flow Microsoft Defender for Endpoint
ms.reviewer: ''
description: Utilisez Microsoft Defender pour endpoint Flow connecteur pour automatiser la sécurité et créer un flux qui sera déclenché chaque fois qu’une nouvelle alerte se produit sur votre client.
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: dd0cc3c2da134750f905b1f80746d6ec65cc70b2
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769702"
---
# <a name="microsoft-power-automate-formerly-microsoft-flow-and-azure-functions"></a><span data-ttu-id="c8600-104">Microsoft Power Automate (anciennement Microsoft Flow) et Azure Functions</span><span class="sxs-lookup"><span data-stu-id="c8600-104">Microsoft Power Automate (formerly Microsoft Flow), and Azure Functions</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c8600-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c8600-105">**Applies to:**</span></span>
- [<span data-ttu-id="c8600-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c8600-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="c8600-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c8600-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


- <span data-ttu-id="c8600-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c8600-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="c8600-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c8600-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="c8600-110">L’automatisation des procédures de sécurité est une exigence standard pour chaque centre des opérations de sécurité moderne.</span><span class="sxs-lookup"><span data-stu-id="c8600-110">Automating security procedures is a standard requirement for every modern Security Operations Center.</span></span> <span data-ttu-id="c8600-111">L’absence de cyber-défenseurs professionnels force SOC à fonctionner de la manière la plus efficace et l’automatisation est une chose à faire.</span><span class="sxs-lookup"><span data-stu-id="c8600-111">The lack of professional cyber defenders forces SOC to work in the most efficient way and automation is a must.</span></span> <span data-ttu-id="c8600-112">Microsoft Power Automate prend en charge différents connecteurs qui ont été créés exactement pour cela.</span><span class="sxs-lookup"><span data-stu-id="c8600-112">Microsoft Power Automate supports different connectors that were built exactly for that.</span></span> <span data-ttu-id="c8600-113">Vous pouvez créer une automatisation de procédure de bout en bout en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="c8600-113">You can build an end-to-end procedure automation within a few minutes.</span></span>

<span data-ttu-id="c8600-114">L’API Microsoft Defender dispose d’un connecteur Flow officiel avec de nombreuses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c8600-114">Microsoft Defender API has an official Flow Connector with many capabilities.</span></span>

![Image de modification des informations d’identification1](images/api-flow-0.png)

> [!NOTE]
> <span data-ttu-id="c8600-116">Pour plus d’informations sur les conditions préalables de licence des connecteurs premium, voir [Licensing for premium connectors](https://docs.microsoft.com/power-automate/triggers-introduction#licensing-for-premium-connectors).</span><span class="sxs-lookup"><span data-stu-id="c8600-116">For more details about premium connectors licensing prerequisites, see [Licensing for premium connectors](https://docs.microsoft.com/power-automate/triggers-introduction#licensing-for-premium-connectors).</span></span>


## <a name="usage-example"></a><span data-ttu-id="c8600-117">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="c8600-117">Usage example</span></span>

<span data-ttu-id="c8600-118">L’exemple suivant montre comment créer une Flow qui est déclenchée chaque fois qu’une nouvelle alerte se produit sur votre client.</span><span class="sxs-lookup"><span data-stu-id="c8600-118">The following example demonstrates how to create a Flow that is triggered any time a new Alert occurs on your tenant.</span></span>

1. <span data-ttu-id="c8600-119">Connectez-vous [à Microsoft Power Automate](https://flow.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c8600-119">Log in to [Microsoft Power Automate](https://flow.microsoft.com).</span></span>

2. <span data-ttu-id="c8600-120">Go to **My flows**  >  **New**  >  **Automated-from blank**.</span><span class="sxs-lookup"><span data-stu-id="c8600-120">Go to **My flows** > **New** > **Automated-from blank**.</span></span>

    ![Image de modification des informations d’identification2](images/api-flow-1.png)

3. <span data-ttu-id="c8600-122">Choisissez un nom pour votre Flow, recherchez « déclencheurs Microsoft Defender ATP » comme déclencheur, puis sélectionnez le nouveau déclencheur Alertes.</span><span class="sxs-lookup"><span data-stu-id="c8600-122">Choose a name for your Flow, search for "Microsoft Defender ATP Triggers" as the trigger, and then select the new Alerts trigger.</span></span>

    ![Image de modification des informations d’identification3](images/api-flow-2.png)

<span data-ttu-id="c8600-124">Vous avez maintenant une Flow qui est déclenchée chaque fois qu’une nouvelle alerte se produit.</span><span class="sxs-lookup"><span data-stu-id="c8600-124">Now you have a Flow that is triggered every time a new Alert occurs.</span></span>

![Image de modification des informations d’identification4](images/api-flow-3.png)

<span data-ttu-id="c8600-126">Il vous suffit maintenant de choisir les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8600-126">All you need to do now is choose your next steps.</span></span>
<span data-ttu-id="c8600-127">Par exemple, vous pouvez isoler l’appareil si la gravité de l’alerte est élevée et envoyer un e-mail à son sujet.</span><span class="sxs-lookup"><span data-stu-id="c8600-127">For example, you can isolate the device if the Severity of the Alert is High and send an email about it.</span></span>
<span data-ttu-id="c8600-128">Le déclencheur d’alerte fournit uniquement l’ID d’alerte et l’ID de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c8600-128">The Alert trigger provides only the Alert ID and the Machine ID.</span></span> <span data-ttu-id="c8600-129">Vous pouvez utiliser le connecteur pour développer ces entités.</span><span class="sxs-lookup"><span data-stu-id="c8600-129">You can use the connector to expand these entities.</span></span>

### <a name="get-the-alert-entity-using-the-connector"></a><span data-ttu-id="c8600-130">Obtenir l’entité Alerte à l’aide du connecteur</span><span class="sxs-lookup"><span data-stu-id="c8600-130">Get the Alert entity using the connector</span></span>

1. <span data-ttu-id="c8600-131">Choisissez **Microsoft Defender ATP** pour la nouvelle étape.</span><span class="sxs-lookup"><span data-stu-id="c8600-131">Choose **Microsoft Defender ATP** for the new step.</span></span>

2. <span data-ttu-id="c8600-132">Choose **Alerts - Get single alert API**.</span><span class="sxs-lookup"><span data-stu-id="c8600-132">Choose **Alerts - Get single alert API**.</span></span>

3. <span data-ttu-id="c8600-133">Définissez **l’ID d’alerte** de la dernière étape en tant **qu’entrée.**</span><span class="sxs-lookup"><span data-stu-id="c8600-133">Set the **Alert ID** from the last step as **Input**.</span></span>

    ![Image de modification des informations d’identification5](images/api-flow-4.png)

### <a name="isolate-the-device-if-the-alerts-severity-is-high"></a><span data-ttu-id="c8600-135">Isoler l’appareil si la gravité de l’alerte est élevée</span><span class="sxs-lookup"><span data-stu-id="c8600-135">Isolate the device if the Alert's severity is High</span></span>

1. <span data-ttu-id="c8600-136">Ajoutez **condition** en tant que nouvelle étape.</span><span class="sxs-lookup"><span data-stu-id="c8600-136">Add **Condition** as a new step.</span></span>

2. <span data-ttu-id="c8600-137">Vérifiez si la gravité de **l’alerte est égale à** Élevée.</span><span class="sxs-lookup"><span data-stu-id="c8600-137">Check if the Alert severity **is equal to** High.</span></span>

   <span data-ttu-id="c8600-138">Si oui, ajoutez le Microsoft Defender ATP - Isoler l’action **de l’ordinateur** avec l’ID de l’ordinateur et un commentaire.</span><span class="sxs-lookup"><span data-stu-id="c8600-138">If yes, add the **Microsoft Defender ATP - Isolate machine** action with the Machine ID and a comment.</span></span>

    ![Image de modification des informations d’identification6](images/api-flow-5.png)

3. <span data-ttu-id="c8600-140">Ajoutez une nouvelle étape pour l’envoi par courrier électronique de l’alerte et de l’isolation.</span><span class="sxs-lookup"><span data-stu-id="c8600-140">Add a new step for emailing about the Alert and the Isolation.</span></span> <span data-ttu-id="c8600-141">Il existe plusieurs connecteurs de messagerie très faciles à utiliser, tels que Outlook ou Gmail.</span><span class="sxs-lookup"><span data-stu-id="c8600-141">There are multiple email connectors that are very easy to use, such as Outlook or Gmail.</span></span>

4. <span data-ttu-id="c8600-142">Enregistrez votre flux.</span><span class="sxs-lookup"><span data-stu-id="c8600-142">Save your flow.</span></span>

<span data-ttu-id="c8600-143">Vous pouvez également créer un **flux programmé** qui exécute des requêtes de recherche avancée, et bien plus encore !</span><span class="sxs-lookup"><span data-stu-id="c8600-143">You can also create a **scheduled** flow that runs Advanced Hunting queries and much more!</span></span>

## <a name="related-topic"></a><span data-ttu-id="c8600-144">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="c8600-144">Related topic</span></span>
- [<span data-ttu-id="c8600-145">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c8600-145">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)
