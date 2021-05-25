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
description: Découvrez comment utiliser Power Automate créer votre flux pour traiter vos contrats à l’aide d’Microsoft 365 solution.
ms.openlocfilehash: 0ddcbeff6c8bd119850e3e4ea45db2513e774433
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52636253"
---
# <a name="step-3-use-power-automate-to-create-your-flow-to-process-your-contracts"></a><span data-ttu-id="e759b-104">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="e759b-104">Step 3.</span></span> <span data-ttu-id="e759b-105">Utiliser Power Automate pour créer votre flux pour traiter vos contrats</span><span class="sxs-lookup"><span data-stu-id="e759b-105">Use Power Automate to create your flow to process your contracts</span></span>

<span data-ttu-id="e759b-106">Vous avez créé votre canal de gestion des contrats et attaché votre SharePoint de documents.</span><span class="sxs-lookup"><span data-stu-id="e759b-106">You've created your Contract Management channel and have attached your SharePoint document library.</span></span> <span data-ttu-id="e759b-107">L’étape suivante consiste à créer un flux Power Automate pour traiter vos contrats que votre modèle syntex SharePoint identifie et classifie.</span><span class="sxs-lookup"><span data-stu-id="e759b-107">The next step is to create a Power Automate flow to process your contracts that your SharePoint Syntex model identifies and classifies.</span></span> <span data-ttu-id="e759b-108">Vous pouvez réaliser cette étape en [créant un flux Power Automate dans votre bibliothèque SharePoint documents.](https://support.microsoft.com/office/create-a-flow-for-a-list-or-library-in-sharepoint-or-onedrive-a9c3e03b-0654-46af-a254-20252e580d01)</span><span class="sxs-lookup"><span data-stu-id="e759b-108">You can do this step by [creating a Power Automate flow in your SharePoint document library](https://support.microsoft.com/office/create-a-flow-for-a-list-or-library-in-sharepoint-or-onedrive-a9c3e03b-0654-46af-a254-20252e580d01).</span></span>

<span data-ttu-id="e759b-109">Pour votre solution de gestion des contrats, vous souhaitez créer un flux Power Automate pour réaliser les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e759b-109">For your contracts management solution, you want to create a Power Automate flow to do the following actions:</span></span>

-  <span data-ttu-id="e759b-110">Une fois qu’un contrat a été classé par SharePoint modèle Syntex, modifiez l’état du contrat en **In review**.</span><span class="sxs-lookup"><span data-stu-id="e759b-110">After a contract has been classified by your SharePoint Syntex model, change the contract status to **In review**.</span></span>
- <span data-ttu-id="e759b-111">Le contrat est ensuite examiné et approuvé ou rejeté.</span><span class="sxs-lookup"><span data-stu-id="e759b-111">The contract is then reviewed and is either approved or rejected.</span></span>
- <span data-ttu-id="e759b-112">Pour les contrats approuvés, les informations sur le contrat sont publiées dans un onglet pour le traitement des paiements.</span><span class="sxs-lookup"><span data-stu-id="e759b-112">For approved contracts, the contract information is posted to a tab for payment processing.</span></span>
- <span data-ttu-id="e759b-113">Pour les contrats rejetés, l’équipe est avertie pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="e759b-113">For rejected contracts, the team is notified for further analysis.</span></span> 

<span data-ttu-id="e759b-114">Le diagramme suivant illustre le flux Power Automate pour la solution de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="e759b-114">The following diagram shows the Power Automate flow for the contract management solution.</span></span>

![Flow diagramme montrant l’intégralité de la solution.](../media/content-understanding/flow-entire-process.png)

## <a name="prepare-your-contract-for-review"></a><span data-ttu-id="e759b-116">Préparer votre contrat pour révision</span><span class="sxs-lookup"><span data-stu-id="e759b-116">Prepare your contract for review</span></span>

<span data-ttu-id="e759b-117">Lorsqu’un contrat est identifié et classé par votre modèle SharePoint document Syntex, le flux Power Automate change d’abord l’état en **In review**.</span><span class="sxs-lookup"><span data-stu-id="e759b-117">When a contract is identified and classified by your SharePoint Syntex document understanding model, the Power Automate flow will first change the status to **In review**.</span></span>

![Mettre à jour l’état.](../media/content-understanding/flow-overview.png)

<span data-ttu-id="e759b-119">Après avoir vérifié le fichier, modifiez la valeur d’état sur **En révision.**</span><span class="sxs-lookup"><span data-stu-id="e759b-119">After checking out the file, change the status value to **In review**.</span></span>

![Dans l’état de l’avis.](../media/content-understanding/in-review.png)

<span data-ttu-id="e759b-121">L’étape suivante consiste à créer une carte adaptative indiquant que le contrat attend une révision et la publie sur le canal de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="e759b-121">The next step is to create an adaptive card stating that the contract is waiting for review and posting it to the Contract Management channel.</span></span>

![Publication de révision de contrat.](../media/content-understanding/contract-approval-post.png)


![Créez une carte adaptative pour révision.](../media/content-understanding/adaptive-card.png)

<span data-ttu-id="e759b-124">Le code suivant est le JSON utilisé pour cette étape dans le Power Automate flux.</span><span class="sxs-lookup"><span data-stu-id="e759b-124">The following code is the JSON used for this step in the Power Automate flow.</span></span>

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


## <a name="conditional"></a><span data-ttu-id="e759b-125">Conditionnel</span><span class="sxs-lookup"><span data-stu-id="e759b-125">Conditional</span></span>

<span data-ttu-id="e759b-126">Dans votre flux, vous devez ensuite créer une condition dans laquelle votre contrat sera approuvé ou rejeté.</span><span class="sxs-lookup"><span data-stu-id="e759b-126">In your flow, next you need to create a condition in which your contract will be either  approved or rejected.</span></span>

![Conditionnel.](../media/content-understanding/condition.png)

## <a name="if-the-contract-is-approved"></a><span data-ttu-id="e759b-128">Si le contrat est approuvé</span><span class="sxs-lookup"><span data-stu-id="e759b-128">If the contract is approved</span></span>

<span data-ttu-id="e759b-129">Lorsqu’un contrat a été approuvé, les éléments suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="e759b-129">When a contract has been approved, the following things occur:</span></span>

- <span data-ttu-id="e759b-130">Sous l’onglet **Contrats,** l’état de la carte de contrat passe à **Approuvé**.</span><span class="sxs-lookup"><span data-stu-id="e759b-130">On the **Contracts** tab, the status in the contract card will change to **Approved**.</span></span>

   ![État de la carte approuvé.](../media/content-understanding/approved-contracts-tab.png)

- <span data-ttu-id="e759b-132">Dans votre flux, l’état est modifié en **Approuvé**.</span><span class="sxs-lookup"><span data-stu-id="e759b-132">In your flow, the status is changed to **Approved**.</span></span>

   ![Flow statut approuvé.](../media/content-understanding/status-approved.png)

- <span data-ttu-id="e759b-134">Dans cette solution, les données de  contrat sont ajoutées à l’onglet Paiement afin que les paiements soient gérés.</span><span class="sxs-lookup"><span data-stu-id="e759b-134">In this solution, the contract data will be added to the **For Payout** tab so that the payouts can be managed.</span></span> <span data-ttu-id="e759b-135">Ce processus peut être étendu pour permettre au flux de soumettre les contrats en paiement par une application financière tierce (par exemple, Dynamics CRM).</span><span class="sxs-lookup"><span data-stu-id="e759b-135">This process can be extended to allow the flow to submit the contracts for payment by a third-party financial application (for example, Dynamics CRM).</span></span>

   ![Contrat déplacé vers Payer.](../media/content-understanding/for-payout.png)

- <span data-ttu-id="e759b-137">Dans le flux, vous créez l’élément suivant pour déplacer les contrats approuvés vers **l’onglet** Paiement.</span><span class="sxs-lookup"><span data-stu-id="e759b-137">In the flow, you create the following item to move approved contracts to the **For Payout** tab.</span></span>

   ![Flow’élément à déplacer vers Payer.](../media/content-understanding/ready-for-payout.png)

- <span data-ttu-id="e759b-139">Une carte adaptative indiquant que le contrat a été approuvé est créée et publiée sur le canal de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="e759b-139">An adaptive card stating that the contract has been approved is created and posted to the Contract Management channel.</span></span>

   ![Approbation de contrat publiée.](../media/content-understanding/adaptive-card-approval.png)

   ![Approbation de carte adaptative.](../media/content-understanding/adaptive-card.png)


   <span data-ttu-id="e759b-142">Le code suivant est le JSON utilisé pour cette étape dans le Power Automate flux.</span><span class="sxs-lookup"><span data-stu-id="e759b-142">The following code is the JSON used for this step in the Power Automate flow.</span></span>

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

## <a name="if-the-contract-is-rejected"></a><span data-ttu-id="e759b-143">Si le contrat est rejeté</span><span class="sxs-lookup"><span data-stu-id="e759b-143">If the contract is rejected</span></span>

<span data-ttu-id="e759b-144">Lorsqu’un contrat a été rejeté, les choses suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="e759b-144">When a contract has been rejected, the following things occur:</span></span>

- <span data-ttu-id="e759b-145">Sous l’onglet **Contrats,** l’état de la carte de contrat passe à **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="e759b-145">On the **Contracts** tab, the status in the contract card will change to **Rejected**.</span></span>

   ![État de la carte rejeté.](../media/content-understanding/rejected-contracts-tab.png)

- <span data-ttu-id="e759b-147">Dans votre flux, vous consultez le fichier de contrat, modifiez l’état sur **Rejeté,** puis ré-consultez le fichier.</span><span class="sxs-lookup"><span data-stu-id="e759b-147">In your flow, you check out the contract file, change the status to **Rejected**, and then check the file back in.</span></span>

   ![Flow statut rejeté.](../media/content-understanding/reject-flow.png)

- <span data-ttu-id="e759b-149">Dans votre flux, vous créez une carte adaptative indiquant que le contrat a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="e759b-149">In your flow, you create an adaptive card stating that the contract has been rejected.</span></span>

   ![Flow statut rejeté.](../media/content-understanding/reject-flow-item.png)

<span data-ttu-id="e759b-151">Le code suivant est le JSON utilisé pour cette étape dans le Power Automate flux.</span><span class="sxs-lookup"><span data-stu-id="e759b-151">The following code is the JSON used for this step in the Power Automate flow.</span></span>

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

- <span data-ttu-id="e759b-152">La carte est publiée dans le canal de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="e759b-152">The card is posted in the Contract Management channel.</span></span>

   ![Flow carte adaptative à rejeter.](../media/content-understanding/rejected.png)