---
title: Étape 3. Utiliser Power Automate pour créer votre flux pour traiter vos contrats
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
description: Découvrez comment utiliser les Power Automate créer votre flux pour traiter vos contrats à l’aide d’Microsoft 365 solution.
ms.openlocfilehash: e6c1d1e53363f996241efb2394189853d840c6c2
ms.sourcegitcommit: fa9efab24a84f71fec7d001f2ad8949125fa8eee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53054478"
---
# <a name="step-3-use-power-automate-to-create-your-flow-to-process-your-contracts"></a><span data-ttu-id="21c53-104">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="21c53-104">Step 3.</span></span> <span data-ttu-id="21c53-105">Utiliser Power Automate pour créer votre flux pour traiter vos contrats</span><span class="sxs-lookup"><span data-stu-id="21c53-105">Use Power Automate to create your flow to process your contracts</span></span>

<span data-ttu-id="21c53-106">Vous avez créé votre canal de gestion des contrats et attaché votre SharePoint de documents.</span><span class="sxs-lookup"><span data-stu-id="21c53-106">You've created your Contract Management channel and have attached your SharePoint document library.</span></span> <span data-ttu-id="21c53-107">L’étape suivante consiste à créer un flux Power Automate pour traiter vos contrats que votre modèle SharePoint Syntex identifie et classifie.</span><span class="sxs-lookup"><span data-stu-id="21c53-107">The next step is to create a Power Automate flow to process your contracts that your SharePoint Syntex model identifies and classifies.</span></span> <span data-ttu-id="21c53-108">Vous pouvez réaliser cette étape en [créant un flux Power Automate dans votre bibliothèque SharePoint documents.](https://support.microsoft.com/office/create-a-flow-for-a-list-or-library-in-sharepoint-or-onedrive-a9c3e03b-0654-46af-a254-20252e580d01)</span><span class="sxs-lookup"><span data-stu-id="21c53-108">You can do this step by [creating a Power Automate flow in your SharePoint document library](https://support.microsoft.com/office/create-a-flow-for-a-list-or-library-in-sharepoint-or-onedrive-a9c3e03b-0654-46af-a254-20252e580d01).</span></span>

<span data-ttu-id="21c53-109">Pour votre solution de gestion des contrats, vous souhaitez créer un flux Power Automate pour réaliser les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="21c53-109">For your contracts management solution, you want to create a Power Automate flow to do the following actions:</span></span>

-  <span data-ttu-id="21c53-110">Une fois qu’un contrat a été classé par votre modèle SharePoint Syntex, modifiez l’état du contrat sur **En révision.**</span><span class="sxs-lookup"><span data-stu-id="21c53-110">After a contract has been classified by your SharePoint Syntex model, change the contract status to **In review**.</span></span>
- <span data-ttu-id="21c53-111">Le contrat est ensuite examiné et approuvé ou rejeté.</span><span class="sxs-lookup"><span data-stu-id="21c53-111">The contract is then reviewed and is either approved or rejected.</span></span>
- <span data-ttu-id="21c53-112">Pour les contrats approuvés, les informations de contrat sont publiées dans un onglet pour le traitement des paiements.</span><span class="sxs-lookup"><span data-stu-id="21c53-112">For approved contracts, the contract information is posted to a tab for payment processing.</span></span>
- <span data-ttu-id="21c53-113">Pour les contrats rejetés, l’équipe est avertie pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="21c53-113">For rejected contracts, the team is notified for further analysis.</span></span> 

<span data-ttu-id="21c53-114">Le diagramme suivant illustre le flux Power Automate pour la solution de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="21c53-114">The following diagram shows the Power Automate flow for the contract management solution.</span></span>

![Flow diagramme montrant l’intégralité de la solution.](../media/content-understanding/flow-entire-process.png)

## <a name="prepare-your-contract-for-review"></a><span data-ttu-id="21c53-116">Préparer votre contrat pour révision</span><span class="sxs-lookup"><span data-stu-id="21c53-116">Prepare your contract for review</span></span>

<span data-ttu-id="21c53-117">Lorsqu’un contrat est identifié et classé par votre modèle de SharePoint Syntex document, le flux de Power Automate change d’abord l’état en **In review**.</span><span class="sxs-lookup"><span data-stu-id="21c53-117">When a contract is identified and classified by your SharePoint Syntex document understanding model, the Power Automate flow will first change the status to **In review**.</span></span>

![Mettre à jour l’état.](../media/content-understanding/flow-overview.png)

<span data-ttu-id="21c53-119">Après avoir vérifié le fichier, modifiez la valeur d’état sur **En révision.**</span><span class="sxs-lookup"><span data-stu-id="21c53-119">After checking out the file, change the status value to **In review**.</span></span>

![Dans l’état de l’avis.](../media/content-understanding/in-review.png)

<span data-ttu-id="21c53-121">L’étape suivante consiste à créer une carte adaptative indiquant que le contrat attend une révision et la publie sur le canal de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="21c53-121">The next step is to create an adaptive card stating that the contract is waiting for review and posting it to the Contract Management channel.</span></span>

![Publication de révision de contrat.](../media/content-understanding/contract-approval-post.png)


![Créez une carte adaptative pour révision.](../media/content-understanding/adaptive-card.png)

<span data-ttu-id="21c53-124">Le code suivant est le JSON utilisé pour cette étape dans le Power Automate flux.</span><span class="sxs-lookup"><span data-stu-id="21c53-124">The following code is the JSON used for this step in the Power Automate flow.</span></span>

```JSON
{
"$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
"type": "AdaptiveCard",
"version": "1.0",
"body": [
    {
    "type": "TextBlock",
    "text": "Contract approval request",
    "size": "large",
    "weight": "bolder",
     "wrap": true
    },
        {
            "type": "Container",
            "items": [
                {
                    "type": "FactSet",
                    "spacing": "Large",
                    "facts": [
                        {
                            "title": "Client",
                            "value": "@{triggerOutputs()?['body/Client']}"
                        },
                        {
                            "title": "Contractor",
                            "value": "@{triggerOutputs()?['body/Contractor']}"
                        },
                        {
                            "title": "Fee amount",
                            "value": "@{triggerOutputs()?['body/FeeAmount']}"
                        },
                        {
                            "title": "Date created",
                            "value": "@{triggerOutputs()?['body/Modified']} "
                        },
                        {
                            "title": "Link",
                            "value": "[@{triggerOutputs()?['body/{FilenameWithExtension}']}](@{triggerOutputs()?['body/{Link}']})"
                        }
                    ]
                }
            ]
         },
    {
    "type": "TextBlock",
    "text": "Comment:"
    },
        {
            "type": "Input.Text",
            "placeholder": "Enter comments",
            "id": "acComments"
        }
],
"actions": [
    {
    "type": "Action.Submit",
    "title": "Approve",
    "data": {
        "x": "Approve"
    }
    },
    {
    "type": "Action.Submit",
    "title": "Reject",
    "data": {
        "x": "Reject"
    }
    }
]
}
```


## <a name="conditional-context"></a><span data-ttu-id="21c53-125">Contexte conditionnel</span><span class="sxs-lookup"><span data-stu-id="21c53-125">Conditional context</span></span>

<span data-ttu-id="21c53-126">Dans votre flux, vous devez ensuite créer une condition dans laquelle votre contrat sera [approuvé ou](#if-the-contract-is-approved) [rejeté.](#if-the-contract-is-rejected)</span><span class="sxs-lookup"><span data-stu-id="21c53-126">In your flow, next you need to create a condition in which your contract will be either  [approved](#if-the-contract-is-approved) or [rejected](#if-the-contract-is-rejected).</span></span>

![Conditionnel.](../media/content-understanding/condition.png)

## <a name="if-the-contract-is-approved"></a><span data-ttu-id="21c53-128">Si le contrat est approuvé</span><span class="sxs-lookup"><span data-stu-id="21c53-128">If the contract is approved</span></span>

<span data-ttu-id="21c53-129">Lorsqu’un contrat a été approuvé, les éléments suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="21c53-129">When a contract has been approved, the following things occur:</span></span>

- <span data-ttu-id="21c53-130">Sous **l’onglet Contrats,** l’état de la carte de contrat passe à **Approuvé**.</span><span class="sxs-lookup"><span data-stu-id="21c53-130">On the **Contracts** tab, the status in the contract card will change to **Approved**.</span></span>

   ![État de la carte approuvé.](../media/content-understanding/approved-contracts-tab.png)

- <span data-ttu-id="21c53-132">Dans votre flux, l’état est modifié en **Approuvé**.</span><span class="sxs-lookup"><span data-stu-id="21c53-132">In your flow, the status is changed to **Approved**.</span></span>

   ![Flow statut approuvé.](../media/content-understanding/status-approved.png)

- <span data-ttu-id="21c53-134">Dans cette solution, les données de  contrat sont ajoutées à l’onglet Paiement afin que les paiements soient gérés.</span><span class="sxs-lookup"><span data-stu-id="21c53-134">In this solution, the contract data will be added to the **For Payout** tab so that the payouts can be managed.</span></span> <span data-ttu-id="21c53-135">Ce processus peut être étendu pour permettre au flux de soumettre les contrats en paiement par une application financière tierce (par exemple, Dynamics CRM).</span><span class="sxs-lookup"><span data-stu-id="21c53-135">This process can be extended to allow the flow to submit the contracts for payment by a third-party financial application (for example, Dynamics CRM).</span></span>

   ![Contrat déplacé vers Payer.](../media/content-understanding/for-payout.png)

- <span data-ttu-id="21c53-137">Dans le flux, vous créez l’élément suivant pour déplacer les contrats approuvés vers **l’onglet** Paiement.</span><span class="sxs-lookup"><span data-stu-id="21c53-137">In the flow, you create the following item to move approved contracts to the **For Payout** tab.</span></span>

   ![Flow’élément à déplacer vers Payer.](../media/content-understanding/ready-for-payout.png)

    <span data-ttu-id="21c53-139">Pour obtenir les expressions pour les informations nécessaires à partir de la carte Teams, utilisez les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="21c53-139">To get the expressions for the information needed from the Teams card, use the values shown in the following table.</span></span>
 
    |<span data-ttu-id="21c53-140">Nom</span><span class="sxs-lookup"><span data-stu-id="21c53-140">Name</span></span>     |<span data-ttu-id="21c53-141">Expression</span><span class="sxs-lookup"><span data-stu-id="21c53-141">Expression</span></span> |
    |---------|-----------|
    | <span data-ttu-id="21c53-142">État d’approbation</span><span class="sxs-lookup"><span data-stu-id="21c53-142">Approval state</span></span>  | <span data-ttu-id="21c53-143">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')? ['submitActionId']</span><span class="sxs-lookup"><span data-stu-id="21c53-143">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['submitActionId']</span></span>         |
    | <span data-ttu-id="21c53-144">Approuvé par</span><span class="sxs-lookup"><span data-stu-id="21c53-144">Approved by</span></span>     | <span data-ttu-id="21c53-145">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')? ['responder'] ['displayName']</span><span class="sxs-lookup"><span data-stu-id="21c53-145">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['responder']['displayName']</span></span>        |
    | <span data-ttu-id="21c53-146">Date d’approbation</span><span class="sxs-lookup"><span data-stu-id="21c53-146">Approval date</span></span>     | <span data-ttu-id="21c53-147">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')? ['responseTime']</span><span class="sxs-lookup"><span data-stu-id="21c53-147">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['responseTime']</span></span>         |
    | <span data-ttu-id="21c53-148">Commentaire</span><span class="sxs-lookup"><span data-stu-id="21c53-148">Comment</span></span>     | <span data-ttu-id="21c53-149">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')? ['data'] ['acComments']</span><span class="sxs-lookup"><span data-stu-id="21c53-149">body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['data']['acComments']</span></span>         |
    
    <span data-ttu-id="21c53-150">L’exemple suivant montre comment utiliser la zone de formule dans Power Automate pour écrire une expression.</span><span class="sxs-lookup"><span data-stu-id="21c53-150">The following example shows how to use the formula box in Power Automate to write an expression.</span></span>

   ![Capture d’écran Power Automate montrant une formule d’expression.](../media/content-understanding/expression-formula-power-automate.png)    

- <span data-ttu-id="21c53-152">Une carte adaptative indiquant que le contrat a été approuvé est créée et publiée sur le canal de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="21c53-152">An adaptive card stating that the contract has been approved is created and posted to the Contract Management channel.</span></span>

   ![Approbation de contrat publiée.](../media/content-understanding/adaptive-card-approval.png)

   ![Approbation de carte adaptative.](../media/content-understanding/adaptive-card.png)


   <span data-ttu-id="21c53-155">Le code suivant est le JSON utilisé pour cette étape dans le Power Automate flux.</span><span class="sxs-lookup"><span data-stu-id="21c53-155">The following code is the JSON used for this step in the Power Automate flow.</span></span>

```JSON
{ 
    "type": "AdaptiveCard",
    "body": [
        {
            "type": "Container",
            "style": "emphasis",
            "items": [
                {
                    "type": "ColumnSet",
                    "columns": [
                        {
                            "type": "Column",
                            "items": [
                                {
                                    "type": "TextBlock",
                                    "size": "Large",
                                    "weight": "Bolder",
                                    "text": "CONTRACT APPROVED"
                                }
                            ],
                            "width": "stretch"
                        }
                    ]
                }
            ],
            "bleed": true
        },
        {
            "type": "Container",
            "items": [
                {
                    "type": "FactSet",
                    "spacing": "Large",
                    "facts": [
                        {
                            "title": "Client",
                            "value": "@{triggerOutputs()?['body/Client']}"
                        },
                        {
                            "title": "Contractor",
                            "value": "@{triggerOutputs()?['body/Contractor']}"
                        },
                        {
                            "title": "Fee amount",
                            "value": "@{triggerOutputs()?['body/FeeAmount']}"
                        },
                        {
                            "title": "Approval by",
                            "value": "@{body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['responder']['displayName']}"
                        },
                        {
                            "title": "Approved date",
                            "value": "@{body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['responseTime']}"
                        },
                        {
                            "title": "Approval comment",
                            "value": "@{body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['data']['acComments']}"
                        },
                        {
                            "title": " ",
                            "value": " "
                        },
                        {
                            "title": "Status",
                            "value": "Ready for payout"
                        }
                    ]
                }
            ]
        }
    ],
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "version": "1.2",
    "fallbackText": "This card requires Adaptive Cards v1.2 support to be rendered properly."
}
```

## <a name="if-the-contract-is-rejected"></a><span data-ttu-id="21c53-156">Si le contrat est rejeté</span><span class="sxs-lookup"><span data-stu-id="21c53-156">If the contract is rejected</span></span>

<span data-ttu-id="21c53-157">Lorsqu’un contrat a été rejeté, les éléments suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="21c53-157">When a contract has been rejected, the following things occur:</span></span>

- <span data-ttu-id="21c53-158">Sous l’onglet **Contrats,** l’état de la carte de contrat passe à **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="21c53-158">On the **Contracts** tab, the status in the contract card will change to **Rejected**.</span></span>

   ![État de la carte rejeté.](../media/content-understanding/rejected-contracts-tab.png)

- <span data-ttu-id="21c53-160">Dans votre flux, vous consultez le fichier de contrat, modifiez l’état sur **Rejeté,** puis ré-consultez le fichier.</span><span class="sxs-lookup"><span data-stu-id="21c53-160">In your flow, you check out the contract file, change the status to **Rejected**, and then check the file back in.</span></span>

   ![Flow statut rejeté dans le fichier de contrat.](../media/content-understanding/reject-flow.png)

- <span data-ttu-id="21c53-162">Dans votre flux, vous créez une carte adaptative indiquant que le contrat a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="21c53-162">In your flow, you create an adaptive card stating that the contract has been rejected.</span></span>

   ![Flow’état de la carte adaptative est rejeté.](../media/content-understanding/reject-flow-item.png)

<span data-ttu-id="21c53-164">Le code suivant est le JSON utilisé pour cette étape dans le Power Automate flux.</span><span class="sxs-lookup"><span data-stu-id="21c53-164">The following code is the JSON used for this step in the Power Automate flow.</span></span>

```JSON
{ 
    "type": "AdaptiveCard",
    "body": [
        {
            "type": "Container",
            "style": "attention",
            "items": [
                {
                    "type": "ColumnSet",
                    "columns": [
                        {
                            "type": "Column",
                            "items": [
                                {
                                    "type": "TextBlock",
                                    "size": "Large",
                                    "weight": "Bolder",
                                    "text": "CONTRACT REJECTED"
                                }
                            ],
                            "width": "stretch"
                        }
                    ]
                }
            ],
            "bleed": true
        },
        {
            "type": "Container",
            "items": [
                {
                    "type": "FactSet",
                    "spacing": "Large",
                    "facts": [
                        {
                            "title": "Client",
                            "value": "@{triggerOutputs()?['body/Client']}"
                        },
                        {
                            "title": "Contractor",
                            "value": "@{triggerOutputs()?['body/Contractor']}"
                        },
                        {
                            "title": "Fee amount",
                            "value": "@{triggerOutputs()?['body/FeeAmount']}"
                        },
                        {
                            "title": "Rejected by",
                            "value": "@{body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['responder']['displayName']}"
                        },
                        {
                            "title": "Rejected date",
                            "value": "@{body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['responseTime']}"
                        },
                        {
                            "title": "Comment",
                            "value": "@{body('Post_an_Adaptive_Card_to_a_Teams_channel_and_wait_for_a_response')?['data']['acComments']}"
                        },
                        {
                            "title": " ",
                            "value": " "
                        },
                        {
                            "title": "Status",
                            "value": "Needs review"
                        }
                    ]
                }
            ]
        }
    ],
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "version": "1.2",
    "fallbackText": "This card requires Adaptive Cards v1.2 support to be rendered properly."
}
```

- <span data-ttu-id="21c53-165">La carte est publiée dans le canal de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="21c53-165">The card is posted in the Contract Management channel.</span></span>

   ![Flow carte adaptative à rejeter.](../media/content-understanding/rejected.png)