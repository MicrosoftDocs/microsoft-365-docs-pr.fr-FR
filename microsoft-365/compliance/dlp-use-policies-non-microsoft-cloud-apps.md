---
title: Utiliser des stratégies de protection contre la perte de données pour les applications cloud non-Microsoft (aperçu)
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser des stratégies dlp pour les applications cloud non Microsoft.
ms.openlocfilehash: 6787add3ef8b2d6ded22bd05c0ff9658c4b7fbfc
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50922080"
---
# <a name="use-data-loss-prevention-policies-for-non-microsoft-cloud-apps-preview"></a><span data-ttu-id="0a2aa-103">Utiliser des stratégies de protection contre la perte de données pour les applications cloud non-Microsoft (aperçu)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-103">Use data loss prevention policies for non-Microsoft cloud apps (preview)</span></span>

<span data-ttu-id="0a2aa-104">Les stratégies de protection contre la perte de données (DLP) pour les applications cloud non Microsoft font partie de la suite de fonctionnalités DLP Microsoft 365 . À l’aide de ces fonctionnalités, vous pouvez découvrir et protéger les éléments sensibles dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-104">Data loss prevention (DLP) policies to non-Microsoft cloud apps are part of the Microsoft 365 DLP suite of features; using these features, you can discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="0a2aa-105">Pour plus d’informations sur toutes les offres Microsoft DLP, voir [Vue d’ensemble de la protection contre la perte de données.](./data-loss-prevention-policies.md?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-105">For more information about all Microsoft DLP offerings, see [Overview of data loss prevention](./data-loss-prevention-policies.md?view=o365-worldwide).</span></span>

<span data-ttu-id="0a2aa-106">Vous pouvez utiliser des stratégies DLP pour les applications cloud non-Microsoft afin de surveiller et de détecter quand des éléments sensibles sont utilisés et partagés via des applications cloud non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-106">You can use DLP policies to non-Microsoft cloud apps to monitor and detect when sensitive items are used and shared via non-Microsoft cloud apps.</span></span> <span data-ttu-id="0a2aa-107">L’utilisation de ces stratégies vous donne la visibilité et le contrôle dont vous avez besoin pour vous assurer qu’elles sont correctement utilisées et protégées, et cela permet d’éviter les comportements risqués qui peuvent les compromettre.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-107">Using these policies gives you the visibility and control that you need to ensure that they're correctly used and protected, and it helps prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0a2aa-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0a2aa-108">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="0a2aa-109">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="0a2aa-109">SKU/subscriptions licensing</span></span>

<span data-ttu-id="0a2aa-110">Avant de commencer à utiliser des stratégies DLP pour les applications cloud non Microsoft, confirmez votre abonnement [Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et les modules.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-110">Before you start using DLP policies to non-Microsoft cloud apps, confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="0a2aa-111">Pour accéder à cette fonctionnalité et l’utiliser, vous devez avoir l’un de ces abonnements ou modules:</span><span class="sxs-lookup"><span data-stu-id="0a2aa-111">To access and use this functionality, you must have one of these subscriptions or add-ons:</span></span>

- <span data-ttu-id="0a2aa-112">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="0a2aa-112">Microsoft 365 E5</span></span>
- <span data-ttu-id="0a2aa-113">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="0a2aa-113">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="0a2aa-114">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="0a2aa-114">Microsoft 365 E5 Security</span></span>

### <a name="prepare-your-cloud-app-security-environment"></a><span data-ttu-id="0a2aa-115">Préparer votre environnement Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="0a2aa-115">Prepare your Cloud App Security environment</span></span>

<span data-ttu-id="0a2aa-116">Les stratégies DLP pour les applications cloud non-Microsoft utilisent les fonctionnalités cloud app security DLP.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-116">DLP policies to non-Microsoft cloud apps use Cloud App Security DLP capabilities.</span></span> <span data-ttu-id="0a2aa-117">Pour l’utiliser, vous devez préparer votre environnement Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-117">To use it, you should prepare your Cloud App Security environment.</span></span> <span data-ttu-id="0a2aa-118">Pour obtenir des instructions, voir Définir des actions de visibilité, de protection et de gouvernance [instantanées pour vos applications.](/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-118">For instructions, see [Set instant visibility, protection, and governance actions for your apps](/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps).</span></span>

### <a name="connect-a-non-microsoft-cloud-app"></a><span data-ttu-id="0a2aa-119">Connecter une application cloud non-Microsoft</span><span class="sxs-lookup"><span data-stu-id="0a2aa-119">Connect a non-Microsoft cloud app</span></span>

<span data-ttu-id="0a2aa-120">Pour utiliser la stratégie DLP sur une application cloud non-Microsoft spécifique, l’application doit être connectée à Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-120">To use DLP policy to a specific non-Microsoft cloud app, the app must be connected to Cloud App Security.</span></span> <span data-ttu-id="0a2aa-121">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="0a2aa-121">For information, see:</span></span>

- [<span data-ttu-id="0a2aa-122">Zone de connexion</span><span class="sxs-lookup"><span data-stu-id="0a2aa-122">Connect Box</span></span>](/cloud-app-security/connect-box-to-microsoft-cloud-app-security)
- [<span data-ttu-id="0a2aa-123">Connecter Dropbox</span><span class="sxs-lookup"><span data-stu-id="0a2aa-123">Connect Dropbox</span></span>](/cloud-app-security/connect-dropbox-to-microsoft-cloud-app-security)
- [<span data-ttu-id="0a2aa-124">Connecter G-Suite</span><span class="sxs-lookup"><span data-stu-id="0a2aa-124">Connect G-Suite</span></span>](/cloud-app-security/connect-google-apps-to-microsoft-cloud-app-security)
- [<span data-ttu-id="0a2aa-125">Connecter Salesforce</span><span class="sxs-lookup"><span data-stu-id="0a2aa-125">Connect Salesforce</span></span>](/cloud-app-security/connect-salesforce-to-microsoft-cloud-app-security)
- [<span data-ttu-id="0a2aa-126">Connecter Cisco Webex</span><span class="sxs-lookup"><span data-stu-id="0a2aa-126">Connect Cisco Webex</span></span>](/cloud-app-security/connect-webex-to-microsoft-cloud-app-security)

<span data-ttu-id="0a2aa-127">Après avoir connecté vos applications cloud à Cloud App Security, vous pouvez créer des stratégies DLP Microsoft 365 pour elles.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-127">After you connect your cloud apps to Cloud App Security, you can create Microsoft 365 DLP policies for them.</span></span>

>[!NOTE]
><span data-ttu-id="0a2aa-128">Il est également possible d’utiliser Microsoft Cloud App Security pour créer des stratégies DLP pour les applications cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-128">It's also possible to use Microsoft Cloud App Security to create DLP policies to Microsoft cloud apps.</span></span> <span data-ttu-id="0a2aa-129">Toutefois, il est recommandé d’utiliser Microsoft 365 pour créer et gérer des stratégies DLP dans les applications cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-129">However, it's recommended to use Microsoft 365 to create and manage DLP policies to Microsoft cloud apps.</span></span>

## <a name="create-a-dlp-policy-to-a-non-microsoft-cloud-app"></a><span data-ttu-id="0a2aa-130">Créer une stratégie DLP pour une application cloud non-Microsoft</span><span class="sxs-lookup"><span data-stu-id="0a2aa-130">Create a DLP policy to a non-Microsoft cloud app</span></span>

<span data-ttu-id="0a2aa-131">Lorsque vous sélectionnez un emplacement pour la stratégie DLP, activer l’emplacement **Microsoft Cloud App Security.**</span><span class="sxs-lookup"><span data-stu-id="0a2aa-131">When you select a location for the DLP policy, turn on the **Microsoft Cloud App Security** location.</span></span>

- <span data-ttu-id="0a2aa-132">Pour sélectionner une application ou une instance spécifique, **sélectionnez Instance.**</span><span class="sxs-lookup"><span data-stu-id="0a2aa-132">To select a specific app or instance, select **Choose instance**.</span></span>
- <span data-ttu-id="0a2aa-133">Si vous ne sélectionnez pas d’instance, la stratégie utilise toutes les applications connectées dans votre client Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-133">If you don't select an instance, the policy uses all connected apps in your Microsoft Cloud App Security tenant.</span></span>

   ![Emplacements pour appliquer la stratégie](../media/1-dlp-non-microsoft-cloud-app-choose-instance.png)

   ![Box-US et Box-General](../media/2-dlp-non-microsoft-cloud-app-box.png)

<span data-ttu-id="0a2aa-136">Vous pouvez choisir différentes actions pour chaque application cloud non-Microsoft prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-136">You can choose various actions for every supported non-Microsoft cloud app.</span></span> <span data-ttu-id="0a2aa-137">Pour chaque application, il existe différentes actions possibles (dépend de l’API de l’application cloud).</span><span class="sxs-lookup"><span data-stu-id="0a2aa-137">For every app, there are different possible actions (depends on the cloud app API).</span></span>

![Créer une règle](../media/3-dlp-non-microsoft-cloud-app-create-rule.png)

<span data-ttu-id="0a2aa-139">Lorsque vous créez une règle dans la stratégie DLP, vous pouvez sélectionner une action pour les applications cloud autres que Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-139">When you create a rule in the DLP policy, you can select an action for non-Microsoft cloud apps.</span></span> <span data-ttu-id="0a2aa-140">Pour restreindre les applications tierces, **sélectionnez Restreindre les applications tierces.**</span><span class="sxs-lookup"><span data-stu-id="0a2aa-140">To restrict third-party apps, select **Restrict Third Party Apps**.</span></span>

![Restreindre les applications tierces](../media/4-dlp-non-microsoft-cloud-app-restrict-third-party-apps.png)

<span data-ttu-id="0a2aa-142">Pour plus d’informations sur la création et la configuration des stratégies DLP, voir Créer un test et [régler une stratégie DLP.](./create-test-tune-dlp-policy.md?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-142">For information about creating and configuring DLP policies, see [Create test and tune a DLP policy](./create-test-tune-dlp-policy.md?view=o365-worldwide).</span></span>

## <a name="see-also"></a><span data-ttu-id="0a2aa-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a2aa-143">See Also</span></span>

- [<span data-ttu-id="0a2aa-144">Créer un test et régler une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="0a2aa-144">Create test and tune a DLP policy</span></span>](./create-test-tune-dlp-policy.md?view=o365-worldwide)
- [<span data-ttu-id="0a2aa-145">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="0a2aa-145">Get started with the default DLP policy</span></span>](./get-started-with-the-default-dlp-policy.md?view=o365-worldwide)
- [<span data-ttu-id="0a2aa-146">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="0a2aa-146">Create a DLP policy from a template</span></span>](./create-a-dlp-policy-from-a-template.md?view=o365-worldwide)