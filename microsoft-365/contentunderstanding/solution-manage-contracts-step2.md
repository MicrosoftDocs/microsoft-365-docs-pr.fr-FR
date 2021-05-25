---
title: Étape 2. Utiliser Microsoft Teams pour créer votre canal de gestion de contrat
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: article
ms.date: ''
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: ''
description: Découvrez comment utiliser Microsoft Teams pour créer votre canal de gestion de contrat à l’aide d’Microsoft 365 solution.
ms.openlocfilehash: 81d5fe34383453b187363b13c21ef47844948193
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52636181"
---
# <a name="step-2-use-microsoft-teams-to-create-your-contract-management-channel"></a><span data-ttu-id="5336b-104">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="5336b-104">Step 2.</span></span> <span data-ttu-id="5336b-105">Utiliser Microsoft Teams pour créer votre canal de gestion de contrat</span><span class="sxs-lookup"><span data-stu-id="5336b-105">Use Microsoft Teams to create your contract management channel</span></span>

<span data-ttu-id="5336b-106">Lorsque votre organisation définit une solution de gestion des contrats, vous avez besoin d’un emplacement central dans lequel les parties prenantes peuvent examiner et gérer les contrats.</span><span class="sxs-lookup"><span data-stu-id="5336b-106">When your organization sets up a contracts management solution, you need a central location in which stakeholders can review and manage contracts.</span></span> <span data-ttu-id="5336b-107">À cet effet, vous pouvez utiliser [Microsoft Teams](https://docs.microsoft.com/microsoftteams/) pour configurer un canal Teams et utiliser les fonctionnalités Teams pour :</span><span class="sxs-lookup"><span data-stu-id="5336b-107">For this purpose, you can use [Microsoft Teams](https://docs.microsoft.com/microsoftteams/) to set up a Teams channel and use the features in Teams to:</span></span>

- <span data-ttu-id="5336b-108">**Créez un emplacement pour que les parties prenantes voient facilement tous les contrats qui nécessitent une action.**</span><span class="sxs-lookup"><span data-stu-id="5336b-108">**Create a location for stakeholders to easily see all contracts that require action.**</span></span> <span data-ttu-id="5336b-109">Par exemple, dans Teams vous pouvez créer un onglet **Contrats** dans le canal de gestion des contrats dans lequel les membres peuvent voir une vue de vignette utile de tous les contrats qui ont besoin d’approbation.</span><span class="sxs-lookup"><span data-stu-id="5336b-109">For example, in Teams you can create a **Contracts** tab in the Contract Management channel in which members can see a useful tile view of all contracts that need approval.</span></span> <span data-ttu-id="5336b-110">Vous pouvez également configurer l’affichage afin que chaque « carte » répertorie les données importantes qui vous intéressent (par exemple, *client,* indépendant et *montant des frais).* </span><span class="sxs-lookup"><span data-stu-id="5336b-110">You can also configure the view so that each "card" lists the important data you care about (such as *Client*, *Contractor*, and *Fee amount*).</span></span>

     ![Onglet Contrats.](../media/content-understanding/tile-view.png)

- <span data-ttu-id="5336b-112">**Avoir un emplacement où les membres peuvent interagir les uns avec les autres et voir les événements importants.**</span><span class="sxs-lookup"><span data-stu-id="5336b-112">**Have a location for members to interact with each other and see important events.**</span></span> <span data-ttu-id="5336b-113">Par exemple, dans Teams, l’onglet **Publications** peut être utilisé pour avoir des conversations, obtenir des mises à jour et voir les actions (par exemple, un membre rejetant un contrat).</span><span class="sxs-lookup"><span data-stu-id="5336b-113">For example, in Teams, the **Posts** tab can be used to have conversations, get updates, and see actions (such as a member rejecting a contract).</span></span> <span data-ttu-id="5336b-114">Lorsqu’un événement s’est produit (par exemple, un nouveau contrat soumis pour approbation), l’onglet **Publications** peut être utilisé non seulement pour l’annoncer, mais aussi pour conserver un enregistrement de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="5336b-114">When something has happened (such as a new contract submitted for approval), the **Posts** tab can be used not only to announce it, but also to keep a record of it.</span></span> <span data-ttu-id="5336b-115">Et si les membres s’abonnez aux notifications, ils sont avertis chaque fois qu’une mise à jour est en cours.</span><span class="sxs-lookup"><span data-stu-id="5336b-115">And if members subscribe to notifications, they'll get notified whenever there's an update.</span></span> 

     ![Onglet Publications.](../media/content-understanding/posts.png)</br> 

- <span data-ttu-id="5336b-117">**Avoir un emplacement pour que les membres voient les contrats approuvés afin de savoir quand ils peuvent être envoyés pour paiement.**</span><span class="sxs-lookup"><span data-stu-id="5336b-117">**Have a location for members to see approved contracts to know when they can be submitted for payment.**</span></span> <span data-ttu-id="5336b-118">Dans Teams, vous pouvez créer <b></b> un canal de paiement qui listera tous les contrats qui devront être soumis au paiement.</span><span class="sxs-lookup"><span data-stu-id="5336b-118">In Teams, you can create a <b>For Payment</b> channel that will list all contracts that will need to be submitted to payment.</span></span> <span data-ttu-id="5336b-119">Vous pouvez facilement étendre cette solution pour écrire ces informations directement dans une application financière tierce (par exemple, Dynamics CRM).</span><span class="sxs-lookup"><span data-stu-id="5336b-119">You can easily extend this solution to instead write this information directly to a third-party financial application (for example, Dynamics CRM).</span></span>

## <a name="attach-your-sharepoint-document-library-to-the-contracts-tab"></a><span data-ttu-id="5336b-120">Joindre votre bibliothèque SharePoint documents à l’onglet Contrats</span><span class="sxs-lookup"><span data-stu-id="5336b-120">Attach your SharePoint document library to the Contracts tab</span></span> 

<span data-ttu-id="5336b-121">Une fois que vous avez créé un onglet **Contrats** dans votre canal de gestion des contrats, vous devez y attacher [SharePoint bibliothèque de documents.](https://support.microsoft.com/office/add-a-sharepoint-page-list-or-document-library-as-a-tab-in-teams-131edef1-455f-4c67-a8ce-efa2ebf25f0b)</span><span class="sxs-lookup"><span data-stu-id="5336b-121">After you create a **Contracts** tab in your Contracts Management channel, you need to [attach your SharePoint document library to it](https://support.microsoft.com/office/add-a-sharepoint-page-list-or-document-library-as-a-tab-in-teams-131edef1-455f-4c67-a8ce-efa2ebf25f0b).</span></span> <span data-ttu-id="5336b-122">La SharePoint de documents que vous souhaitez attacher est celle à laquelle vous avez appliqué votre modèle de SharePoint document Syntex dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5336b-122">The SharePoint document library you want to attach is the one in which you applied your SharePoint Syntex document understanding model to in the previous section.</span></span>

<span data-ttu-id="5336b-123">Une fois que vous avez attaché SharePoint bibliothèque de documents, vous pouvez afficher les contrats classifiés via un affichage de liste par défaut.</span><span class="sxs-lookup"><span data-stu-id="5336b-123">After you attach the SharePoint document library, you'll be able to view any classified contracts through a default list view.</span></span>

   ![Affichage Liste.](../media/content-understanding/list-view.png) 

## <a name="customize-your-contracts-tab-tile-view"></a><span data-ttu-id="5336b-125">Personnaliser l’affichage en mosaïque de l’onglet Contrats</span><span class="sxs-lookup"><span data-stu-id="5336b-125">Customize your Contracts tab tile view</span></span>

> [!NOTE]
> <span data-ttu-id="5336b-126">Cette section fait référence à des exemples de code qui sont contenus dans le [ContractTileFormatting.js](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) sur le fichier qui est inclus dans le référentiel des ressources de la solution de gestion [des contrats.](https://github.com/pnp/syntex-samples/tree/main/scenario%20assets/Contracts%20Management)</span><span class="sxs-lookup"><span data-stu-id="5336b-126">This section references code examples that are contained in the [ContractTileFormatting.json](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) file that is included in the [Contracts Management Solution Assets repository](https://github.com/pnp/syntex-samples/tree/main/scenario%20assets/Contracts%20Management).</span></span>

<span data-ttu-id="5336b-127">Bien Teams vous permet d’afficher vos contrats dans une vue en mosaïque, vous pouvez le personnaliser pour afficher les données de contrat que vous souhaitez rendre visibles dans la carte de contrat.</span><span class="sxs-lookup"><span data-stu-id="5336b-127">While Teams lets you view your contracts in a tile view, you might want to customize it to view the contract data you want to make visible in the contract card.</span></span> <span data-ttu-id="5336b-128">Par exemple, pour l’onglet **Contrats,** il est important que les membres voient le client, le fournisseur et le montant des frais sur la carte de contrat.</span><span class="sxs-lookup"><span data-stu-id="5336b-128">For example, for the **Contracts** tab, it is important for members to see the client, contractor, and fee amount on the contract card.</span></span> <span data-ttu-id="5336b-129">Tous ces champs ont été extraits de chaque contrat via SharePoint modèle Syntex appliqué à votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="5336b-129">All of these fields were extracted from each contract through your SharePoint Syntex model that was applied to your document library.</span></span> <span data-ttu-id="5336b-130">Vous souhaitez également être en mesure de modifier la barre d’en-tête de vignette en différentes couleurs pour chaque état afin que les membres puissent facilement voir où se trouve le contrat dans le processus d’approbation.</span><span class="sxs-lookup"><span data-stu-id="5336b-130">You also want to be able to change the tile header bar to different colors for each status so that members can easily see where the contract is in the approval process.</span></span> <span data-ttu-id="5336b-131">Par exemple, tous les contrats approuvés auront une barre d’en-tête bleue.</span><span class="sxs-lookup"><span data-stu-id="5336b-131">For example, all approved contracts will have a blue header bar.</span></span>

   ![Affichage Liste.](../media/content-understanding/tile.png)

<span data-ttu-id="5336b-133">La vue de vignette personnalisée que vous utilisez nécessite que vous ayiez apporté des modifications au fichier JSON utilisé pour mettre en forme la vue de vignette actuelle.</span><span class="sxs-lookup"><span data-stu-id="5336b-133">The custom tile view you use requires you to make changes to the JSON file used to format the current tile view.</span></span> <span data-ttu-id="5336b-134">Vous pouvez référencer le fichier JSON utilisé pour créer l’affichage de carte enContractTileFormatting.js[fichier on.](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json)</span><span class="sxs-lookup"><span data-stu-id="5336b-134">You can reference the JSON file used to create the card view by looking at the [ContractTileFormatting.json](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) file.</span></span> <span data-ttu-id="5336b-135">Dans les sections suivantes, vous verrez des sections spécifiques du code pour les fonctionnalités qui sont dans les cartes de contrat.</span><span class="sxs-lookup"><span data-stu-id="5336b-135">In the following sections, you'll see specific sections of the code for features that are in the contract cards.</span></span>

<span data-ttu-id="5336b-136">Si vous souhaitez afficher ou modifier le code JSON de votre affichage dans votre canal Teams, dans le canal Teams, sélectionnez le menu déroulant d’affichage, puis sélectionnez Mettre en forme l’affichage **actuel.**</span><span class="sxs-lookup"><span data-stu-id="5336b-136">If you want to see or make changes to the JSON code for your view in your Teams channel, in the Teams channel, select the view drop-down menu, and then select **Format current view**.</span></span>

   ![Format json.](../media/content-understanding/jason-format.png) 

## <a name="card-size-and-shape"></a><span data-ttu-id="5336b-138">Taille et forme de la carte</span><span class="sxs-lookup"><span data-stu-id="5336b-138">Card size and shape</span></span>

<span data-ttu-id="5336b-139">Dans la [ContractTileFormatting.jsdu](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) fichier, consultez la section suivante pour voir le code de mise en forme de la taille et de la forme de la carte.</span><span class="sxs-lookup"><span data-stu-id="5336b-139">In the [ContractTileFormatting.json](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) file, look at the following section to see the code for how the size and shape of the card is formatted.</span></span>

```JSON
                  {
                    "elmType": "div",
                    "style": {
                      "background-color": "#f5f5f5",
                      "padding": "5px",
                      "width": "180px"
                    },
                    "children": [
                      {
                        "elmType": "img",
                        "attributes": {
                          "src": "@thumbnail.large"
                        },
                        "style": {
                          "width": "185px",
                          "height": "248px"
                        }
                      }
```


## <a name="contract-status"></a><span data-ttu-id="5336b-140">État du contrat</span><span class="sxs-lookup"><span data-stu-id="5336b-140">Contract status</span></span>

<span data-ttu-id="5336b-141">Le code suivant vous permet de définir l’état de chaque carte de titre.</span><span class="sxs-lookup"><span data-stu-id="5336b-141">The following code lets you define the status of each title card.</span></span> <span data-ttu-id="5336b-142">Notez que chaque valeur d’état (*Nouveau*, *En révision*, *Approuvé* et Rejeté *)* affiche un code de couleur différent pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5336b-142">Note that each status value (*New*, *In review*, *Approved*, and *Rejected*) will display a different color code for each.</span></span> <span data-ttu-id="5336b-143">Dans la [ContractTileFormatting.jssur le](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) fichier, regardez la section qui définit l’état.</span><span class="sxs-lookup"><span data-stu-id="5336b-143">In the [ContractTileFormatting.json](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) file, look at the section that defines the status.</span></span>

```JSON
          {
            "elmType": "div",
            "children": [
              {
                "elmType": "div",
                "style": {
                  "color": "white",
                  "background-color": "=if([$Status] == 'New', '#00b7c3', if([$Status] == 'In review', '#ffaa44', if([$Status] == 'Approved', '#0078d4', if([$Status] == 'Rejected', '#d13438', '#8378de'))))",
                  "padding": "5px 15px",
                  "height": "auto",
                  "text-transform": "uppercase",
                  "font-size": "12.5px"
                },
                "txtContent": "[$Status]"
              }
```


## <a name="extracted-fields"></a><span data-ttu-id="5336b-144">Champs extraits</span><span class="sxs-lookup"><span data-stu-id="5336b-144">Extracted fields</span></span>

<span data-ttu-id="5336b-145">Chaque carte de contrat affiche trois champs qui ont été extraits pour chaque contrat (*Client*, *Fournisseur* et Montant *des frais*).</span><span class="sxs-lookup"><span data-stu-id="5336b-145">Each contract card will display three fields that were extracted for each contract (*Client*, *Contractor*, and *Fee Amount*).</span></span> <span data-ttu-id="5336b-146">En outre, vous souhaitez également afficher l’heure/la date de classement du fichier par le modèle SharePoint Syntex utilisé pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="5336b-146">Additionally, you also want to display the time/date that the file was classified by the SharePoint Syntex model used to identify it.</span></span> 

<span data-ttu-id="5336b-147">Dans le [ContractTileFormatting.jssur le](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) fichier, les sections suivantes définissent chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="5336b-147">In the [ContractTileFormatting.json](https://github.com/pnp/syntex-samples/blob/main/scenario%20assets/Contracts%20Management/View%20Formatter/ContractTileFormatting.json) file, the following sections define each of these.</span></span>

### <a name="client"></a><span data-ttu-id="5336b-148">Client</span><span class="sxs-lookup"><span data-stu-id="5336b-148">Client</span></span>

<span data-ttu-id="5336b-149">Cette section définit la façon dont « Client » s’affichera sur la carte et utilise la valeur du contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="5336b-149">This section defines how "Client" will display on the card, and uses the value for the specific contract.</span></span>

```JSON
                      {
                        "elmType": "div",
                        "style": {
                          "color": "#767676",
                          "font-size": "12px"
                        },
                        "txtContent": "Client"
                      },
                      {
                        "elmType": "div",
                        "style": {
                          "margin-bottom": "12px",
                          "font-size": "16px",
                          "font-weight": "600"
                        },
                        "txtContent": "[$Client]"
                      },
```

### <a name="contractor"></a><span data-ttu-id="5336b-150">Resoe</span><span class="sxs-lookup"><span data-stu-id="5336b-150">Contractor</span></span>

<span data-ttu-id="5336b-151">Cette section définit la façon dont le « Programme d’entreprise » s’affichera sur la carte et utilise la valeur du contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="5336b-151">This section defines how the "Contractor" will display on the card, and uses the value for the specific contract.</span></span>

```JSON
                      {
                        "elmType": "div",
                        "style": {
                          "color": "#767676",
                          "font-size": "12px"
                        },
                        "txtContent": "Client"
                      },
                      {
                        "elmType": "div",
                        "style": {
                          "margin-bottom": "12px",
                          "font-size": "16px",
                          "font-weight": "600"
                        },
                        "txtContent": "[$Client]"
},
```


### <a name="fee-amount"></a><span data-ttu-id="5336b-152">Montant des frais</span><span class="sxs-lookup"><span data-stu-id="5336b-152">Fee Amount</span></span>

<span data-ttu-id="5336b-153">Cette section définit la façon dont le « montant des frais » s’affichera sur la carte et utilise la valeur du contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="5336b-153">This section defines how the "Fee Amount" will display on the card, and uses the value for the specific contract.</span></span>

```JSON
                      {
                        "elmType": "div",
                        "txtContent": "Fee amount",
                        "style": {
                          "color": "#767676",
                          "font-size": "12px",
                          "margin-bottom": "2px"
                        }
                      },
                      {
                        "elmType": "div",
                        "style": {
                          "margin-bottom": "12px",
                          "font-size": "14px"
                        },
                        "txtContent": "[$FeeAmount]"
                      },
```



### <a name="classification-date"></a><span data-ttu-id="5336b-154">Date de classification</span><span class="sxs-lookup"><span data-stu-id="5336b-154">Classification date</span></span>

<span data-ttu-id="5336b-155">Cette section définit la façon dont « Classification » s’affichera sur la carte et utilise la valeur du contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="5336b-155">This section defines how "Classification" will display on the card, and uses the value for the specific contract.</span></span>

```JSON
                      {
                        "elmType": "div",
                        "txtContent": "Classified",
                        "style": {
                          "color": "#767676",
                          "font-size": "12px",
                          "margin-bottom": "2px"
                        }
                      },
                      {
                        "elmType": "div",
                        "style": {
                          "margin-bottom": "12px",
                          "font-size": "14px"
                        },
                        "txtContent": "[$PrimeLastClassified]"
                      }
```

## <a name="next-step"></a><span data-ttu-id="5336b-156">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5336b-156">Next step</span></span>

[<span data-ttu-id="5336b-157">Étape 3. Utiliser Power Automate pour créer votre flux pour traiter vos contrats</span><span class="sxs-lookup"><span data-stu-id="5336b-157">Step 3. Use Power Automate to create your flow to process your contracts</span></span>](solution-manage-contracts-step3.md)
