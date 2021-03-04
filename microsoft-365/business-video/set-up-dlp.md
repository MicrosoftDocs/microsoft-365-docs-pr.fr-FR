---
title: Éviter les pertes de données
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment gérer les stratégies de protection contre la perte de données.
ms.openlocfilehash: 54cd508ef0b0cfcf8b71dc86a4903f77a5354c36
ms.sourcegitcommit: 355bd51ab6a79d5c36a4e4f57df74ae6873eba19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50422062"
---
# <a name="prevent-data-loss-with-dlp"></a><span data-ttu-id="eef4b-103">Empêcher la perte de données avec DLP</span><span class="sxs-lookup"><span data-stu-id="eef4b-103">Prevent data loss with DLP</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3TGvL?autoplay=false]

<span data-ttu-id="eef4b-104">Les stratégies de protection contre la perte de données permettent d’identifier et de protéger les informations sensibles de votre entreprise, telles que les numéros de sécurité sociale ou les dossiers médicaux.</span><span class="sxs-lookup"><span data-stu-id="eef4b-104">Data loss prevention policies help identify and protect your business's sensitive information, such as Social Security numbers or medical records.</span></span> 

## <a name="try-it"></a><span data-ttu-id="eef4b-105">Essayez !</span><span class="sxs-lookup"><span data-stu-id="eef4b-105">Try it!</span></span>

1. <span data-ttu-id="eef4b-106">To get started, go to the [admin center](https://admin.microsoft.com), and select **Setup**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-106">To get started, go to the [admin center](https://admin.microsoft.com), and select **Setup**.</span></span>
1. <span data-ttu-id="eef4b-107">Faites défiler vers le bas **pour configurer la** protection contre la perte de données, puis **sélectionnez Afficher,** puis **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-107">Scroll down to **Set up data loss prevention**, and then select **View**, and then **Manage**.</span></span>
1. <span data-ttu-id="eef4b-108">Pour modifier une stratégie, sélectionnez-la, sélectionnez **Modifier la stratégie,** puis ce qu’il faut modifier.</span><span class="sxs-lookup"><span data-stu-id="eef4b-108">To edit a policy, select it, choose **Edit policy**, then select what to change.</span></span> <span data-ttu-id="eef4b-109">Par exemple, sélectionnez **Emplacements** pour modifier ce qui est analysé.</span><span class="sxs-lookup"><span data-stu-id="eef4b-109">For example, select **Locations** to change what gets scanned.</span></span>
1. <span data-ttu-id="eef4b-110">Pour activer l’analyse du contenu dans Microsoft Teams, activez le bouton bascule en position **Activé,** puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="eef4b-110">To enable scanning for content in Microsoft Teams, turn the toggle switch to the **On** position, and then select **Save**.</span></span>
1. <span data-ttu-id="eef4b-111">Pour modifier les paramètres de stratégie, sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="eef4b-111">To edit policy settings, select **Edit**.</span></span>
1. <span data-ttu-id="eef4b-112">Vous devez définir des règles distinctes qui s’appliquent aux petites et grandes quantités de contenu sensible détecté.</span><span class="sxs-lookup"><span data-stu-id="eef4b-112">You'll need to set separate rules that apply to small and large amounts of sensitive content detected.</span></span> <span data-ttu-id="eef4b-113">Développez votre règle de faible volume.</span><span class="sxs-lookup"><span data-stu-id="eef4b-113">Expand your low volume rule.</span></span> <span data-ttu-id="eef4b-114">Choose **Edit rule**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-114">Choose **Edit rule**.</span></span>
1. <span data-ttu-id="eef4b-115">Examinez vos paramètres et ajustez-les selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="eef4b-115">Review your settings and adjust them as needed.</span></span> <span data-ttu-id="eef4b-116">Par exemple, vous pouvez choisir de personnaliser **le texte** du message électronique et le texte du conseil **de stratégie.**</span><span class="sxs-lookup"><span data-stu-id="eef4b-116">For example, you can choose to **Customize the email text** and **Customize the policy tip text**.</span></span> <span data-ttu-id="eef4b-117">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-117">Select **Save**.</span></span>
1. <span data-ttu-id="eef4b-118">Répétez cette répétition pour la règle de volume élevé.</span><span class="sxs-lookup"><span data-stu-id="eef4b-118">Repeat for the high volume rule.</span></span> <span data-ttu-id="eef4b-119">Sélectionnez **Enregistrer,** puis **Fermez.**</span><span class="sxs-lookup"><span data-stu-id="eef4b-119">Select **Save**, and then **Close**.</span></span>
1. <span data-ttu-id="eef4b-120">Pour créer une stratégie, **sélectionnez Créer une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="eef4b-120">To create a new policy, select **Create a policy**.</span></span>
1. <span data-ttu-id="eef4b-121">Vous pouvez créer une stratégie personnalisée ou commencer par un modèle.</span><span class="sxs-lookup"><span data-stu-id="eef4b-121">You can create a custom policy or start with a template.</span></span> <span data-ttu-id="eef4b-122">Par exemple, pour créer une stratégie  HIPAA, sélectionnez le modèle médical et de santé, puis sélectionnez loi américaine d’assurance maladie **(HIPAA).**</span><span class="sxs-lookup"><span data-stu-id="eef4b-122">For example, to create a HIPAA policy, select the **Medical and health** template, and then select **U.S. Health Insurance Act (HIPAA)**.</span></span> <span data-ttu-id="eef4b-123">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-123">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-124">Entrez un nom et une description pour votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="eef4b-124">Enter a name and description for your policy.</span></span> <span data-ttu-id="eef4b-125">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-125">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-126">Choisissez les emplacements à analyser.</span><span class="sxs-lookup"><span data-stu-id="eef4b-126">Choose the locations to scan.</span></span> <span data-ttu-id="eef4b-127">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-127">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-128">Choisissez le type de contenu que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="eef4b-128">Choose the type of content you want protected.</span></span> <span data-ttu-id="eef4b-129">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-129">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-130">Choisissez ce que vous souhaitez faire si des informations sensibles sont détectées.</span><span class="sxs-lookup"><span data-stu-id="eef4b-130">Choose what you want to happen if sensitive information is detected.</span></span> <span data-ttu-id="eef4b-131">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-131">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-132">Personnalisez vos autorisations d’accès et de remplacement.</span><span class="sxs-lookup"><span data-stu-id="eef4b-132">Customize your access and override permissions.</span></span> <span data-ttu-id="eef4b-133">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-133">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-134">Choisissez quand vous souhaitez que la stratégie prenne effet.</span><span class="sxs-lookup"><span data-stu-id="eef4b-134">Choose when you want the policy to take effect.</span></span> <span data-ttu-id="eef4b-135">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="eef4b-135">Select **Next**.</span></span>
1. <span data-ttu-id="eef4b-136">Examinez vos paramètres, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="eef4b-136">Review your settings, and select **Create**.</span></span> <span data-ttu-id="eef4b-137">Une fois votre stratégie entrée en vigueur, le courrier électronique qui contient les informations sensibles décrites est bloqué et l’expéditeur qui a tenté d’envoyer ces informations voit un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="eef4b-137">After your policy takes effect, email that contains the described sensitive information will be blocked, and the sender who attempted to send that information will see a warning message.</span></span>