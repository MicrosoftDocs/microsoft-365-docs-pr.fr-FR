---
title: Créer une charge utile pour la formation à la simulation d’attaques
ms.author: daniha
author: danihalfin
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs peuvent apprendre à créer des charges utiles personnalisées pour la formation à la simulation d’attaques dans Microsoft Defender pour Office 365.
ms.openlocfilehash: 86a962dc3117708ac71195b9efc336fa30c573dd
ms.sourcegitcommit: 99a7354e6a6b4d9d5202674ef57852d52a43fef6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/20/2021
ms.locfileid: "49908340"
---
# <a name="create-a-custom-payload-for-attack-simulation-training"></a><span data-ttu-id="4d565-103">Créer une charge personnalisée pour une formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="4d565-103">Create a custom payload for Attack simulation training</span></span>

<span data-ttu-id="4d565-104">Microsoft offre un catalogue de charges utiles robuste pour diverses techniques d’ingénierie sociale à jumeler avec votre formation à la simulation d’attaques.</span><span class="sxs-lookup"><span data-stu-id="4d565-104">Microsoft offers a robust payload catalog for various social engineering techniques to pair with your attack simulation training.</span></span> <span data-ttu-id="4d565-105">Toutefois, vous pouvez créer des charges utiles personnalisées qui fonctionneront mieux pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4d565-105">However, you might want to create custom payloads that will work better for your organization.</span></span> <span data-ttu-id="4d565-106">Cet article explique comment créer une charge utile dans la formation sur la simulation d’attaques dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="4d565-106">This article describes how to create a payload in Attack simulation training in Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="4d565-107">Vous pouvez créer une charge  utile en cliquant sur Créer une charge utile dans l’onglet [ **Charge utile**](https://security.microsoft.com/attacksimulator?viewid=payload) dédiée ou dans l’Assistant création [de simulation.](attack-simulation-training.md#selecting-a-payload)</span><span class="sxs-lookup"><span data-stu-id="4d565-107">You can create a payload by clicking on **Create a payload** in either the [dedicated **Payloads** tab](https://security.microsoft.com/attacksimulator?viewid=payload) or within the [simulation creation wizard](attack-simulation-training.md#selecting-a-payload).</span></span>

<span data-ttu-id="4d565-108">La première étape de l’Assistant vous permettra de sélectionner un type de charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-108">The first step in the wizard will have you select a payload type.</span></span> <span data-ttu-id="4d565-109">**Actuellement, seul le courrier électronique est disponible.**</span><span class="sxs-lookup"><span data-stu-id="4d565-109">**Currently, only email is available**.</span></span>

<span data-ttu-id="4d565-110">Ensuite, sélectionnez une technique associée.</span><span class="sxs-lookup"><span data-stu-id="4d565-110">Next, select an associated technique.</span></span> <span data-ttu-id="4d565-111">Pour plus d’informations sur les techniques, voir [la sélection d’une technique d’ingénierie sociale.](attack-simulation-training.md#selecting-a-social-engineering-technique)</span><span class="sxs-lookup"><span data-stu-id="4d565-111">See more details on techniques at [Selecting a social engineering technique](attack-simulation-training.md#selecting-a-social-engineering-technique).</span></span>

<span data-ttu-id="4d565-112">À l’étape suivante, nommez votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-112">In the next step name your payload.</span></span> <span data-ttu-id="4d565-113">Si vous le souhaitez, vous pouvez lui donner une description.</span><span class="sxs-lookup"><span data-stu-id="4d565-113">Optionally, you can give it a description.</span></span>

## <a name="configure-payload"></a><span data-ttu-id="4d565-114">Configurer la charge utile</span><span class="sxs-lookup"><span data-stu-id="4d565-114">Configure payload</span></span>

<span data-ttu-id="4d565-115">Il est maintenant temps de créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-115">Now it's time to build your payload.</span></span> <span data-ttu-id="4d565-116">Dans la section Détails de l’expéditeur, entrer le nom de l’expéditeur, l’adresse e-mail et l’objet **de l’e-mail.**</span><span class="sxs-lookup"><span data-stu-id="4d565-116">Input the sender's name, email address, and the email's subject in the **Sender details** section.</span></span> <span data-ttu-id="4d565-117">Sélectionnez une URL de hameçonnage dans la liste fournie.</span><span class="sxs-lookup"><span data-stu-id="4d565-117">Pick a phishing URL from the provided list.</span></span> <span data-ttu-id="4d565-118">Cette URL sera incorporée ultérieurement dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="4d565-118">This URL will later be embedded into the body of the message.</span></span>

> [!TIP]
> <span data-ttu-id="4d565-119">Vous pouvez choisir un courrier électronique interne pour l’expéditeur de votre charge utile, ce qui fait apparaître la charge utile comme provenant d’un autre employé de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="4d565-119">You can choose an internal email for your payload's sender, which will make the payload appear as coming from another employee of the company.</span></span> <span data-ttu-id="4d565-120">Cela augmente la sensibilité à la charge utile et aide à informer les employés sur les risques de menaces internes.</span><span class="sxs-lookup"><span data-stu-id="4d565-120">This will increase susceptibility to the payload and will help educate employees on the risk of internal threats.</span></span>

<span data-ttu-id="4d565-121">Un éditeur de texte enrichi est disponible pour créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-121">A rich text editor is available to create your payload.</span></span> <span data-ttu-id="4d565-122">Vous pouvez également importer un e-mail que vous avez créé au préalable.</span><span class="sxs-lookup"><span data-stu-id="4d565-122">You can also import an email that you've created beforehand.</span></span> <span data-ttu-id="4d565-123">Lorsque vous créez le corps de  l’e-mail, tirez parti des balises dynamiques pour personnaliser l’e-mail sur vos cibles.</span><span class="sxs-lookup"><span data-stu-id="4d565-123">As you create the body of the email, take advantage of the **dynamic tags** to personalize the email to your targets.</span></span> <span data-ttu-id="4d565-124">Cliquez **sur le lien Hameçonnage** pour ajouter l’URL de hameçonnage précédemment sélectionnée dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="4d565-124">Click **Phishing link** to add the previously selected phishing URL into the body of the message.</span></span>

![Lien de hameçonnage et balises dynamiques mises en évidence dans la création de charge utile pour Microsoft Defender pour Office 365](../../media/attack-sim-preview-payload-email-body.png)

> [!TIP]
> <span data-ttu-id="4d565-126">Pour gagner du temps, basculez sur l’option de remplacement de tous les liens du message électronique par le **lien de hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="4d565-126">To save time, toggle on the option to **replace all links in the email message with the phishing link**.</span></span>

<span data-ttu-id="4d565-127">Une fois que vous avez terminé de créer la charge utile à votre convenance, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4d565-127">Once you're done building the payload to your liking, click **Next**.</span></span>

## <a name="adding-indicators"></a><span data-ttu-id="4d565-128">Ajout d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="4d565-128">Adding indicators</span></span>

<span data-ttu-id="4d565-129">Les indicateurs aideront les employés qui traversent la simulation d’attaque à comprendre l’indice qu’ils peuvent rechercher dans les futures attaques.</span><span class="sxs-lookup"><span data-stu-id="4d565-129">Indicators will help employees going through the attack simulation understand the clue they can look for in future attacks.</span></span> <span data-ttu-id="4d565-130">Pour commencer, cliquez sur **Ajouter un indicateur.**</span><span class="sxs-lookup"><span data-stu-id="4d565-130">To start, click **Add indicator**.</span></span>

<span data-ttu-id="4d565-131">Sélectionnez un indicateur que vous souhaitez utiliser dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="4d565-131">Select an indicator you'd like to use from the drop-down list.</span></span> <span data-ttu-id="4d565-132">Cette liste est organisée pour contenir les indices les plus courants qui apparaissent dans les messages électroniques de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4d565-132">This list is curated to contain the most common clues that appear in phishing email messages.</span></span> <span data-ttu-id="4d565-133">Une fois sélectionné, assurez-vous que le placement de l’indicateur est définie sur À partir du corps de l’e-mail **et** cliquez sur Sélectionner **du texte**.</span><span class="sxs-lookup"><span data-stu-id="4d565-133">Once selected, make sure the indicator placement is set to **From the body of the email** and click on **Select text**.</span></span> <span data-ttu-id="4d565-134">Sélectionnez la partie de votre charge utile où cet indicateur apparaît, puis cliquez sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="4d565-134">Highlight the portion of your payload where this indicator appears and click **Select**.</span></span>

![Texte mis en surbrillant dans le corps du message à ajouter à un indicateur dans une formation de simulation d’attaque](../../media/attack-sim-preview-select-text.png)

<span data-ttu-id="4d565-136">Ajoutez une description personnalisée pour décrire l’indicateur et cliquez dans le cadre d’aperçu de l’indicateur pour afficher un aperçu de votre indicateur.</span><span class="sxs-lookup"><span data-stu-id="4d565-136">Add a custom description to describe the indicator and click within the indicator preview frame to see a preview of your indicator.</span></span> <span data-ttu-id="4d565-137">Une fois terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4d565-137">Once done, click **Add**.</span></span> <span data-ttu-id="4d565-138">Répétez ces étapes jusqu’à ce que vous avez couvert tous les indicateurs de votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-138">Repeat these steps until you've covered all indicators in your payload.</span></span>

## <a name="review-payload"></a><span data-ttu-id="4d565-139">Examiner la charge utile</span><span class="sxs-lookup"><span data-stu-id="4d565-139">Review payload</span></span>

<span data-ttu-id="4d565-140">Vous avez terminé de créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-140">You're done building your payload.</span></span> <span data-ttu-id="4d565-141">Il est maintenant temps de passer en revue les détails et d’afficher un aperçu de votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-141">Now it's time to review the details and see a preview of your payload.</span></span> <span data-ttu-id="4d565-142">La prévisualisation inclut tous les indicateurs que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="4d565-142">The preview will include all indicators that you've created.</span></span> <span data-ttu-id="4d565-143">Vous pouvez modifier chaque partie de la charge utile à partir de cette étape.</span><span class="sxs-lookup"><span data-stu-id="4d565-143">You can edit each part of the payload from this step.</span></span> <span data-ttu-id="4d565-144">Une fois satisfait, vous pouvez **soumettre votre** charge utile.</span><span class="sxs-lookup"><span data-stu-id="4d565-144">Once satisfied, you can **Submit** your payload.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d565-145">Les charges utiles que vous avez créées auront **le client** comme source.</span><span class="sxs-lookup"><span data-stu-id="4d565-145">Payloads that you've created will have **Tenant** as their source.</span></span> <span data-ttu-id="4d565-146">Lorsque vous sélectionnez des charges utiles, veillez à ne pas filtrer le **client.**</span><span class="sxs-lookup"><span data-stu-id="4d565-146">When selecting payloads, make sure that you don't filter out **Tenant**.</span></span>

## <a name="related-links"></a><span data-ttu-id="4d565-147">Liens associés</span><span class="sxs-lookup"><span data-stu-id="4d565-147">Related links</span></span>

[<span data-ttu-id="4d565-148">Commencer à utiliser la formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="4d565-148">Get started using Attack simulation training</span></span>](attack-simulation-training-get-started.md)

[<span data-ttu-id="4d565-149">Créer une simulation d’attaque par hameçonnage</span><span class="sxs-lookup"><span data-stu-id="4d565-149">Create a phishing attack simulation</span></span>](attack-simulation-training.md)

[<span data-ttu-id="4d565-150">Découvrez les formations à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="4d565-150">Gain insights through Attack simulation training</span></span>](attack-simulation-training-insights.md)
