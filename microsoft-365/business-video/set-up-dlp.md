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
ROBOTS: NOINDEX, NOFOLLOW
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
description: Découvrez comment gérer la configuration des stratégies de protection contre la perte de données.
ms.openlocfilehash: 93c06af0203a5eb590d22d86e597d7485d7af238
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49702245"
---
# <a name="prevent-data-loss-with-dlp"></a><span data-ttu-id="b9d3d-103">Prévention des pertes de données avec DLP</span><span class="sxs-lookup"><span data-stu-id="b9d3d-103">Prevent data loss with DLP</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3TGvL?autoplay=false]

<span data-ttu-id="b9d3d-104">Les stratégies de protection contre la perte de données permettent d’identifier et de protéger les informations sensibles de votre entreprise, telles que les numéros de sécurité sociale ou les enregistrements médicaux.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-104">Data loss prevention policies help identify and protect your business's sensitive information, such as Social Security numbers or medical records.</span></span> 

## <a name="try-it"></a><span data-ttu-id="b9d3d-105">Essayez !</span><span class="sxs-lookup"><span data-stu-id="b9d3d-105">Try it!</span></span>

1. <span data-ttu-id="b9d3d-106">Pour commencer, accédez au centre d' [administration](https://admin.microsoft.com), puis sélectionnez **configuration**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-106">To get started, go to the [admin center](https://admin.microsoft.com), and select **Setup**.</span></span>
1. <span data-ttu-id="b9d3d-107">Faites défiler vers le bas pour **configurer la protection contre la perte de données**, puis sélectionnez **Afficher**, puis **gérer**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-107">Scroll down to **Set up data loss prevention**, and then select **View**, and then **Manage**.</span></span>
1. <span data-ttu-id="b9d3d-108">Pour modifier une stratégie, sélectionnez-la, choisissez **modifier la stratégie**, puis sélectionnez les éléments à modifier.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-108">To edit a policy, select it, choose **Edit policy**, then select what to change.</span></span> <span data-ttu-id="b9d3d-109">Par exemple, sélectionnez **emplacements** pour modifier ce qui est analysé.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-109">For example, select **Locations** to change what gets scanned.</span></span>
1. <span data-ttu-id="b9d3d-110">Pour activer l’analyse de contenu dans Microsoft Teams, activez le bouton bascule sur la position **activé** , puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-110">To enable scanning for content in Microsoft Teams, turn the toggle switch to the **On** position, and then select **Save**.</span></span>
1. <span data-ttu-id="b9d3d-111">Pour modifier les paramètres de stratégie, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-111">To edit policy settings, select **Edit**.</span></span>
1. <span data-ttu-id="b9d3d-112">Vous devez définir des règles distinctes qui s’appliquent aux petites et grandes quantités de contenu sensible détectées.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-112">You'll need to set separate rules that apply to small and large amounts of sensitive content detected.</span></span> <span data-ttu-id="b9d3d-113">Développez votre règle de volume faible.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-113">Expand your low volume rule.</span></span> <span data-ttu-id="b9d3d-114">Choisissez **modifier la règle**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-114">Choose **Edit rule**.</span></span>
1. <span data-ttu-id="b9d3d-115">Vérifiez vos paramètres et ajustez-les si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-115">Review your settings and adjust them as needed.</span></span> <span data-ttu-id="b9d3d-116">Par exemple, vous pouvez **personnaliser le texte du message électronique** et **personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-116">For example, you can choose to **Customize the email text** and **Customize the policy tip text**.</span></span> <span data-ttu-id="b9d3d-117">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-117">Select **Save**.</span></span>
1. <span data-ttu-id="b9d3d-118">Répétez l’opération pour la règle de volume élevée.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-118">Repeat for the high volume rule.</span></span> <span data-ttu-id="b9d3d-119">Sélectionnez **Enregistrer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-119">Select **Save**, and then **Close**.</span></span>
1. <span data-ttu-id="b9d3d-120">Pour créer une stratégie, sélectionnez **créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-120">To create a new policy, select **Create a policy**.</span></span>
1. <span data-ttu-id="b9d3d-121">Vous pouvez créer une stratégie personnalisée ou commencer avec un modèle.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-121">You can create a custom policy or start with a template.</span></span> <span data-ttu-id="b9d3d-122">Par exemple, pour créer une stratégie HIPAA, sélectionnez le modèle **Medical and Health** , puis sélectionnez **U.S. Health Insurance Act (HIPAA)**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-122">For example, to create a HIPAA policy, select the **Medical and health** template, and then select **U.S. Health Insurance Act (HIPAA)**.</span></span> <span data-ttu-id="b9d3d-123">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-123">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-124">Entrez un nom et une description pour votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-124">Enter a name and description for your policy.</span></span> <span data-ttu-id="b9d3d-125">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-125">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-126">Choisissez les emplacements à analyser.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-126">Choose the locations to scan.</span></span> <span data-ttu-id="b9d3d-127">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-127">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-128">Choisissez le type de contenu que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-128">Choose the type of content you want protected.</span></span> <span data-ttu-id="b9d3d-129">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-129">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-130">Choisissez ce qui doit se produire en cas de détection d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-130">Choose what you want to happen if sensitive information is detected.</span></span> <span data-ttu-id="b9d3d-131">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-131">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-132">Personnalisez vos autorisations d’accès et de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-132">Customize your access and override permissions.</span></span> <span data-ttu-id="b9d3d-133">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-133">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-134">Choisissez le moment auquel vous souhaitez que la stratégie prenne effet.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-134">Choose when you want the policy to take effect.</span></span> <span data-ttu-id="b9d3d-135">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-135">Select **Next**.</span></span>
1. <span data-ttu-id="b9d3d-136">Vérifiez vos paramètres, puis sélectionnez **créer**.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-136">Review your settings, and select **Create**.</span></span> <span data-ttu-id="b9d3d-137">Une fois que votre stratégie prend effet, le courrier électronique qui contient les informations sensibles décrites est bloqué et l’expéditeur qui a tenté d’envoyer ces informations verra apparaître un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="b9d3d-137">After your policy takes effect, email that contains the described sensitive information will be blocked, and the sender who attempted to send that information will see a warning message.</span></span>