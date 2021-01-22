---
title: Créer une charge utile pour la formation à la simulation d’attaques
ms.author: daniha
author: danihalfin
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.prod: m365-security
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs peuvent apprendre à créer des charges utiles personnalisées pour la formation à la simulation d’attaques dans Microsoft Defender pour Office 365.
ms.technology: mdo
ms.openlocfilehash: 6cc5dd4a48ab89193133cfaf823d0a1b1868fa79
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49929189"
---
# <a name="create-a-custom-payload-for-attack-simulation-training"></a><span data-ttu-id="a70e2-103">Créer une charge personnalisée pour une formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="a70e2-103">Create a custom payload for Attack simulation training</span></span>

<span data-ttu-id="a70e2-104">Microsoft offre un catalogue de charges utiles robuste pour diverses techniques d’ingénierie sociale à jumeler avec votre formation à la simulation d’attaques.</span><span class="sxs-lookup"><span data-stu-id="a70e2-104">Microsoft offers a robust payload catalog for various social engineering techniques to pair with your attack simulation training.</span></span> <span data-ttu-id="a70e2-105">Toutefois, vous pouvez créer des charges utiles personnalisées qui fonctionneront mieux pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a70e2-105">However, you might want to create custom payloads that will work better for your organization.</span></span> <span data-ttu-id="a70e2-106">Cet article explique comment créer une charge utile dans une formation sur la simulation d’attaques dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="a70e2-106">This article describes how to create a payload in Attack simulation training in Microsoft Defender for Office 365.</span></span>

<span data-ttu-id="a70e2-107">Vous pouvez créer une charge  utile en cliquant sur Créer une charge utile dans l’onglet [ **Charge utile**](https://security.microsoft.com/attacksimulator?viewid=payload) dédiée ou dans l’Assistant création [de simulation.](attack-simulation-training.md#selecting-a-payload)</span><span class="sxs-lookup"><span data-stu-id="a70e2-107">You can create a payload by clicking on **Create a payload** in either the [dedicated **Payloads** tab](https://security.microsoft.com/attacksimulator?viewid=payload) or within the [simulation creation wizard](attack-simulation-training.md#selecting-a-payload).</span></span>

<span data-ttu-id="a70e2-108">La première étape de l’Assistant consiste à sélectionner un type de charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-108">The first step in the wizard will have you select a payload type.</span></span> <span data-ttu-id="a70e2-109">**Actuellement, seul le courrier électronique est disponible.**</span><span class="sxs-lookup"><span data-stu-id="a70e2-109">**Currently, only email is available**.</span></span>

<span data-ttu-id="a70e2-110">Ensuite, sélectionnez une technique associée.</span><span class="sxs-lookup"><span data-stu-id="a70e2-110">Next, select an associated technique.</span></span> <span data-ttu-id="a70e2-111">Pour plus d’informations sur les techniques, voir la sélection [d’une technique d’ingénierie sociale.](attack-simulation-training.md#selecting-a-social-engineering-technique)</span><span class="sxs-lookup"><span data-stu-id="a70e2-111">See more details on techniques at [Selecting a social engineering technique](attack-simulation-training.md#selecting-a-social-engineering-technique).</span></span>

<span data-ttu-id="a70e2-112">Dans l’étape suivante, nommez votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-112">In the next step name your payload.</span></span> <span data-ttu-id="a70e2-113">Si vous le souhaitez, vous pouvez lui donner une description.</span><span class="sxs-lookup"><span data-stu-id="a70e2-113">Optionally, you can give it a description.</span></span>

## <a name="configure-payload"></a><span data-ttu-id="a70e2-114">Configurer la charge utile</span><span class="sxs-lookup"><span data-stu-id="a70e2-114">Configure payload</span></span>

<span data-ttu-id="a70e2-115">Il est maintenant temps de créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-115">Now it's time to build your payload.</span></span> <span data-ttu-id="a70e2-116">Dans la section **Détails** de l’expéditeur, entrer le nom, l’adresse e-mail et l’objet de l’e-mail de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a70e2-116">Input the sender's name, email address, and the email's subject in the **Sender details** section.</span></span> <span data-ttu-id="a70e2-117">Sélectionnez une URL de hameçonnage dans la liste fournie.</span><span class="sxs-lookup"><span data-stu-id="a70e2-117">Pick a phishing URL from the provided list.</span></span> <span data-ttu-id="a70e2-118">Cette URL sera incorporée ultérieurement dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="a70e2-118">This URL will later be embedded into the body of the message.</span></span>

> [!TIP]
> <span data-ttu-id="a70e2-119">Vous pouvez choisir un courrier électronique interne pour l’expéditeur de votre charge utile, ce qui fait apparaître la charge utile comme provenant d’un autre employé de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a70e2-119">You can choose an internal email for your payload's sender, which will make the payload appear as coming from another employee of the company.</span></span> <span data-ttu-id="a70e2-120">Cela augmente la sensibilité à la charge utile et aide à informer les employés sur les risques de menaces internes.</span><span class="sxs-lookup"><span data-stu-id="a70e2-120">This will increase susceptibility to the payload and will help educate employees on the risk of internal threats.</span></span>

<span data-ttu-id="a70e2-121">Un éditeur de texte enrichi est disponible pour créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-121">A rich text editor is available to create your payload.</span></span> <span data-ttu-id="a70e2-122">Vous pouvez également importer un e-mail que vous avez créé au préalable.</span><span class="sxs-lookup"><span data-stu-id="a70e2-122">You can also import an email that you've created beforehand.</span></span> <span data-ttu-id="a70e2-123">Lorsque vous créez le corps de  l’e-mail, tirez parti des balises dynamiques pour personnaliser l’e-mail sur vos cibles.</span><span class="sxs-lookup"><span data-stu-id="a70e2-123">As you create the body of the email, take advantage of the **dynamic tags** to personalize the email to your targets.</span></span> <span data-ttu-id="a70e2-124">Cliquez **sur le lien Hameçonnage** pour ajouter l’URL de hameçonnage précédemment sélectionnée dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="a70e2-124">Click **Phishing link** to add the previously selected phishing URL into the body of the message.</span></span>

![Lien de hameçonnage et balises dynamiques mises en évidence dans la création de charge utile pour Microsoft Defender pour Office 365](../../media/attack-sim-preview-payload-email-body.png)

> [!TIP]
> <span data-ttu-id="a70e2-126">Pour gagner du temps, basculez sur l’option de remplacement de tous les liens du message électronique par le **lien de hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="a70e2-126">To save time, toggle on the option to **replace all links in the email message with the phishing link**.</span></span>

<span data-ttu-id="a70e2-127">Une fois que vous avez terminé de créer la charge utile à votre convenance, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a70e2-127">Once you're done building the payload to your liking, click **Next**.</span></span>

## <a name="adding-indicators"></a><span data-ttu-id="a70e2-128">Ajout d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="a70e2-128">Adding indicators</span></span>

<span data-ttu-id="a70e2-129">Les indicateurs aideront les employés qui traversent la simulation d’attaque à comprendre l’indice qu’ils peuvent rechercher dans les futures attaques.</span><span class="sxs-lookup"><span data-stu-id="a70e2-129">Indicators will help employees going through the attack simulation understand the clue they can look for in future attacks.</span></span> <span data-ttu-id="a70e2-130">Pour commencer, cliquez sur **Ajouter un indicateur.**</span><span class="sxs-lookup"><span data-stu-id="a70e2-130">To start, click **Add indicator**.</span></span>

<span data-ttu-id="a70e2-131">Sélectionnez un indicateur que vous souhaitez utiliser dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="a70e2-131">Select an indicator you'd like to use from the drop-down list.</span></span> <span data-ttu-id="a70e2-132">Cette liste est organisée pour contenir les indices les plus courants qui apparaissent dans les messages électroniques de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a70e2-132">This list is curated to contain the most common clues that appear in phishing email messages.</span></span> <span data-ttu-id="a70e2-133">Une fois sélectionné, assurez-vous que le placement de l’indicateur est définie sur À partir du corps de l’e-mail **et** cliquez sur Sélectionner **du texte**.</span><span class="sxs-lookup"><span data-stu-id="a70e2-133">Once selected, make sure the indicator placement is set to **From the body of the email** and click on **Select text**.</span></span> <span data-ttu-id="a70e2-134">Sélectionnez la partie de votre charge utile où cet indicateur apparaît, puis cliquez sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="a70e2-134">Highlight the portion of your payload where this indicator appears and click **Select**.</span></span>

![Texte mis en surbrillant dans le corps du message à ajouter à un indicateur dans une formation de simulation d’attaque](../../media/attack-sim-preview-select-text.png)

<span data-ttu-id="a70e2-136">Ajoutez une description personnalisée pour décrire l’indicateur et cliquez dans le cadre d’aperçu de l’indicateur pour afficher un aperçu de votre indicateur.</span><span class="sxs-lookup"><span data-stu-id="a70e2-136">Add a custom description to describe the indicator and click within the indicator preview frame to see a preview of your indicator.</span></span> <span data-ttu-id="a70e2-137">Une fois terminé, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a70e2-137">Once done, click **Add**.</span></span> <span data-ttu-id="a70e2-138">Répétez ces étapes jusqu’à ce que vous avez couvert tous les indicateurs de votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-138">Repeat these steps until you've covered all indicators in your payload.</span></span>

## <a name="review-payload"></a><span data-ttu-id="a70e2-139">Examiner la charge utile</span><span class="sxs-lookup"><span data-stu-id="a70e2-139">Review payload</span></span>

<span data-ttu-id="a70e2-140">Vous avez terminé de créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-140">You're done building your payload.</span></span> <span data-ttu-id="a70e2-141">Il est maintenant temps de passer en revue les détails et d’afficher un aperçu de votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-141">Now it's time to review the details and see a preview of your payload.</span></span> <span data-ttu-id="a70e2-142">L’aperçu inclut tous les indicateurs que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="a70e2-142">The preview will include all indicators that you've created.</span></span> <span data-ttu-id="a70e2-143">Vous pouvez modifier chaque partie de la charge utile à partir de cette étape.</span><span class="sxs-lookup"><span data-stu-id="a70e2-143">You can edit each part of the payload from this step.</span></span> <span data-ttu-id="a70e2-144">Une fois satisfait, vous pouvez **soumettre** votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="a70e2-144">Once satisfied, you can **Submit** your payload.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a70e2-145">Les charges utiles que vous avez créées auront **le client** comme source.</span><span class="sxs-lookup"><span data-stu-id="a70e2-145">Payloads that you've created will have **Tenant** as their source.</span></span> <span data-ttu-id="a70e2-146">Lorsque vous sélectionnez des charges utiles, veillez à ne pas filtrer le **client.**</span><span class="sxs-lookup"><span data-stu-id="a70e2-146">When selecting payloads, make sure that you don't filter out **Tenant**.</span></span>

## <a name="related-links"></a><span data-ttu-id="a70e2-147">Liens associés</span><span class="sxs-lookup"><span data-stu-id="a70e2-147">Related links</span></span>

[<span data-ttu-id="a70e2-148">Commencer à utiliser la formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="a70e2-148">Get started using Attack simulation training</span></span>](attack-simulation-training-get-started.md)

[<span data-ttu-id="a70e2-149">Créer une simulation d’attaque par hameçonnage</span><span class="sxs-lookup"><span data-stu-id="a70e2-149">Create a phishing attack simulation</span></span>](attack-simulation-training.md)

[<span data-ttu-id="a70e2-150">Découvrez les formations à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="a70e2-150">Gain insights through Attack simulation training</span></span>](attack-simulation-training-insights.md)
