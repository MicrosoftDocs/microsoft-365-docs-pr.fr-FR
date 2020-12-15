---
title: Créer une charge utile pour la formation à la simulation d’attaque
ms.author: daniha
author: danihalfin
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
description: Les administrateurs peuvent apprendre à créer des charges utiles personnalisées pour la formation à la simulation d’attaque dans Microsoft Defender pour Office 365.
ms.openlocfilehash: c42090634f6fa9500ae4c3e781b49b607ee928f5
ms.sourcegitcommit: 1a9f0f878c045e1ddd59088ca2a94397605a242a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49667503"
---
# <a name="create-a-custom-payload-for-attack-simulation-training"></a><span data-ttu-id="e3af7-103">Créer une charge personnalisée pour une formation à la simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="e3af7-103">Create a custom payload for Attack simulation training</span></span>

<span data-ttu-id="e3af7-104">Microsoft offre un catalogue de charges utiles robuste pour les différentes techniques d’ingénierie sociale à associer à votre formation à la simulation d’attaque.</span><span class="sxs-lookup"><span data-stu-id="e3af7-104">Microsoft offers a robust payload catalog for various social engineering techniques to pair with your attack simulation training.</span></span> <span data-ttu-id="e3af7-105">Toutefois, vous pouvez créer des charges utiles personnalisées qui fonctionneront mieux pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e3af7-105">However, you might want to create custom payloads that will work better for your organization.</span></span> <span data-ttu-id="e3af7-106">Cet article explique comment créer une charge utile dans la formation à la simulation d’attaque dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="e3af7-106">This article describes how to create a payload in Attack simulation training in Microsoft Defender for Office 365.</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="e3af7-107">Vous pouvez créer une charge utile en cliquant sur **créer une charge utile** dans l' [onglet **charge utile** dédiée](https://security.microsoft.com/attacksimulator?viewid=payload) ou dans l' [Assistant Création de simulation](attack-simulation-training.md#selecting-a-payload).</span><span class="sxs-lookup"><span data-stu-id="e3af7-107">You can create a payload by clicking on **Create a payload** in either the [dedicated **Payloads** tab](https://security.microsoft.com/attacksimulator?viewid=payload) or within the [simulation creation wizard](attack-simulation-training.md#selecting-a-payload).</span></span>

<span data-ttu-id="e3af7-108">La première étape de l’Assistant vous permet de sélectionner un type de charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-108">The first step in the wizard will have you select a payload type.</span></span> <span data-ttu-id="e3af7-109">**Actuellement, seul le courrier électronique est disponible**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-109">**Currently, only email is available**.</span></span>

<span data-ttu-id="e3af7-110">Ensuite, sélectionnez une technique associée.</span><span class="sxs-lookup"><span data-stu-id="e3af7-110">Next, select an associated technique.</span></span> <span data-ttu-id="e3af7-111">Pour plus d’informations sur les techniques, consultez la rubrique relative à [la sélection d’une technique d’ingénierie sociale](attack-simulation-training.md#selecting-a-social-engineering-technique).</span><span class="sxs-lookup"><span data-stu-id="e3af7-111">See more details on techniques at [Selecting a social engineering technique](attack-simulation-training.md#selecting-a-social-engineering-technique).</span></span>

<span data-ttu-id="e3af7-112">Dans l’étape suivante, nommez votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-112">In the next step name your payload.</span></span> <span data-ttu-id="e3af7-113">Vous pouvez également lui donner une description.</span><span class="sxs-lookup"><span data-stu-id="e3af7-113">Optionally, you can give it a description.</span></span>

## <a name="configure-payload"></a><span data-ttu-id="e3af7-114">Configurer la charge utile</span><span class="sxs-lookup"><span data-stu-id="e3af7-114">Configure payload</span></span>

<span data-ttu-id="e3af7-115">À présent, il est temps de créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-115">Now it's time to build your payload.</span></span> <span data-ttu-id="e3af7-116">Entrez le nom de l’expéditeur, l’adresse de messagerie et l’objet de l’e-mail dans la section **informations sur l’expéditeur** .</span><span class="sxs-lookup"><span data-stu-id="e3af7-116">Input the sender's name, email address, and the email's subject in the **Sender details** section.</span></span> <span data-ttu-id="e3af7-117">Sélectionnez une URL de hameçonnage dans la liste fournie.</span><span class="sxs-lookup"><span data-stu-id="e3af7-117">Pick a phishing URL from the the provided list.</span></span> <span data-ttu-id="e3af7-118">Cette URL sera ensuite incorporée dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="e3af7-118">This URL will later be embedded into the body of the message.</span></span>

> [!TIP]
> <span data-ttu-id="e3af7-119">Vous pouvez choisir un message électronique interne pour l’expéditeur de votre charge utile, ce qui fera apparaître la charge utile comme provenant d’un autre employé de la société.</span><span class="sxs-lookup"><span data-stu-id="e3af7-119">You can choose an internal email for your payload's sender, which will make the payload appear as coming from another employee of the company.</span></span> <span data-ttu-id="e3af7-120">Cela augmentera la sensibilité à la charge utile et permettra de sensibiliser les employés sur le risque de menaces internes.</span><span class="sxs-lookup"><span data-stu-id="e3af7-120">This will increase susceptibility to the payload and will help educate employees on the risk of internal threats.</span></span>

<span data-ttu-id="e3af7-121">Un éditeur de texte enrichi est disponible pour créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-121">A rich text editor is available to create your payload.</span></span> <span data-ttu-id="e3af7-122">Vous pouvez également importer un courrier électronique que vous avez créé à l’avance.</span><span class="sxs-lookup"><span data-stu-id="e3af7-122">You can also import an email that you've created beforehand.</span></span> <span data-ttu-id="e3af7-123">Lorsque vous créez le corps du message, tirez parti des **balises dynamiques** pour personnaliser le courrier électronique à vos cibles.</span><span class="sxs-lookup"><span data-stu-id="e3af7-123">As you create the body of the email, take advantage of the **dynamic tags** to personalize the email to your targets.</span></span> <span data-ttu-id="e3af7-124">Cliquez sur **lien d’hameçonnage** pour ajouter l’URL d’hameçonnage précédemment sélectionnée dans le corps du message.</span><span class="sxs-lookup"><span data-stu-id="e3af7-124">Click **Phishing link** to add the previously selected phishing URL into the body of the message.</span></span>

![Lien de hameçonnage et balises dynamiques mises en surbrillance dans la création de charge utile pour Microsoft Defender pour Office 365](../../media/attack-sim-preview-payload-email-body.png)

> [!TIP]
> <span data-ttu-id="e3af7-126">Pour gagner du temps, activez ou désactivez la case à cocher **remplacer tous les liens du message électronique par le lien hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-126">To save time, toggle on the option to **replace all links in the email message with the phishing link**.</span></span>

<span data-ttu-id="e3af7-127">Une fois que vous avez fini de créer la charge utile à votre convenance, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-127">Once you're done building the payload to your liking, click **Next**.</span></span>

## <a name="adding-indicators"></a><span data-ttu-id="e3af7-128">Ajout d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="e3af7-128">Adding indicators</span></span>

<span data-ttu-id="e3af7-129">Les indicateurs permettent aux employés de suivre la simulation d’attaque de comprendre l’indice qu’ils peuvent rechercher dans les attaques futures.</span><span class="sxs-lookup"><span data-stu-id="e3af7-129">Indicators will help employees going through the attack simulation understand clue they can look for in future attacks.</span></span> <span data-ttu-id="e3af7-130">Pour commencer, cliquez sur **Ajouter un indicateur**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-130">To start, click **Add indicator**.</span></span>

<span data-ttu-id="e3af7-131">Sélectionnez un indicateur que vous souhaitez utiliser dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e3af7-131">Select an indicator you'd like to use from the drop-down list.</span></span> <span data-ttu-id="e3af7-132">Cette liste est organisée pour contenir les indices les plus courants qui apparaissent dans les messages électroniques de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e3af7-132">This list is curated to contain the most common clues that appear in phishing email messages.</span></span> <span data-ttu-id="e3af7-133">Une fois que vous avez sélectionné, vérifiez que le positionnement de l’indicateur est défini sur **dans le corps de l’e-mail** , puis cliquez sur **Sélectionner le texte**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-133">Once selected, make sure the indicator placement is set to **From the body of the email** and click on **Select text**.</span></span> <span data-ttu-id="e3af7-134">Mettez en surbrillance la partie de la charge utile où cet indicateur s’affiche, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-134">Highlight the portion of your payload where this indicator appears and click **Select**.</span></span>

![Texte mis en surbrillance dans le corps du message à ajouter à un indicateur dans la formation à la simulation d’attaque](../../media/attack-sim-preview-select-text.png)

<span data-ttu-id="e3af7-136">Ajoutez une description personnalisée pour décrire l’indicateur et cliquez dans le cadre d’aperçu de l’indicateur pour afficher un aperçu de votre indicateur.</span><span class="sxs-lookup"><span data-stu-id="e3af7-136">Add a custom description to describe the indicator and click within the indicator preview frame to see a preview of your indicator.</span></span> <span data-ttu-id="e3af7-137">Une fois l’opération terminée, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-137">Once done, click **Add**.</span></span> <span data-ttu-id="e3af7-138">Répétez ces étapes jusqu’à ce que vous ayez abordé tous les indicateurs de votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-138">Repeat these steps until you've covered all indicators in your payload.</span></span>

## <a name="review-payload"></a><span data-ttu-id="e3af7-139">Examiner la charge utile</span><span class="sxs-lookup"><span data-stu-id="e3af7-139">Review payload</span></span>

<span data-ttu-id="e3af7-140">Vous avez fini de créer votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-140">You're done building your payload.</span></span> <span data-ttu-id="e3af7-141">À présent, il est temps de passer en revue les détails et d’afficher un aperçu de votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-141">Now it's time to review the details and see a preview of your payload.</span></span> <span data-ttu-id="e3af7-142">L’aperçu inclut tous les indicateurs que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="e3af7-142">The preview will include all indicators that you've created.</span></span> <span data-ttu-id="e3af7-143">Vous pouvez modifier chaque partie de la charge utile à partir de cette étape.</span><span class="sxs-lookup"><span data-stu-id="e3af7-143">You can edit each part of the payload from this step.</span></span> <span data-ttu-id="e3af7-144">Une fois satisfait, **envoyez** votre charge utile.</span><span class="sxs-lookup"><span data-stu-id="e3af7-144">Once satisfied, **Submit** your payload.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3af7-145">Les charges utiles que vous avez créées auront comme source le **client** .</span><span class="sxs-lookup"><span data-stu-id="e3af7-145">Payloads that you've created will have **Tenant** as their source.</span></span> <span data-ttu-id="e3af7-146">Lors de la sélection des charges utiles, veillez à ne pas filtrer le **client**.</span><span class="sxs-lookup"><span data-stu-id="e3af7-146">When selecting payloads, make sure that you don't filter out **Tenant**.</span></span>
