---
title: Utiliser des stratégies de protection contre la perte de données pour les applications cloud non Microsoft
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
ms.openlocfilehash: 4bda45a6da6b9626391da37eb9a806b3308c5e7f
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322316"
---
# <a name="use-data-loss-prevention-policies-for-non-microsoft-cloud-apps"></a><span data-ttu-id="79ab6-103">Utiliser des stratégies de protection contre la perte de données pour les applications cloud non Microsoft</span><span class="sxs-lookup"><span data-stu-id="79ab6-103">Use data loss prevention policies for non-Microsoft cloud apps</span></span>

<span data-ttu-id="79ab6-104">Les stratégies de protection contre la perte de données (DLP) pour les applications cloud non Microsoft font partie de la suite Microsoft 365 DLP ; À l’aide de ces fonctionnalités, vous pouvez découvrir et protéger les éléments sensibles dans Microsoft 365 services.</span><span class="sxs-lookup"><span data-stu-id="79ab6-104">Data loss prevention (DLP) policies to non-Microsoft cloud apps are part of the Microsoft 365 DLP suite of features; using these features, you can discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="79ab6-105">Pour plus d’informations sur toutes les offres Microsoft DLP, voir [En savoir plus sur la protection contre la perte de données.](dlp-learn-about-dlp.md)</span><span class="sxs-lookup"><span data-stu-id="79ab6-105">For more information about all Microsoft DLP offerings, see [Learn about data loss prevention](dlp-learn-about-dlp.md).</span></span>

<span data-ttu-id="79ab6-106">Vous pouvez utiliser des stratégies DLP pour les applications cloud non-Microsoft afin de surveiller et de détecter quand des éléments sensibles sont utilisés et partagés via des applications cloud non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79ab6-106">You can use DLP policies to non-Microsoft cloud apps to monitor and detect when sensitive items are used and shared via non-Microsoft cloud apps.</span></span> <span data-ttu-id="79ab6-107">L’utilisation de ces stratégies vous donne la visibilité et le contrôle dont vous avez besoin pour vous assurer qu’elles sont correctement utilisées et protégées, et cela permet d’éviter les comportements risqués qui peuvent les compromettre.</span><span class="sxs-lookup"><span data-stu-id="79ab6-107">Using these policies gives you the visibility and control that you need to ensure that they're correctly used and protected, and it helps prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="79ab6-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="79ab6-108">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="79ab6-109">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="79ab6-109">SKU/subscriptions licensing</span></span>

<span data-ttu-id="79ab6-110">Avant de commencer à utiliser des stratégies DLP pour les applications cloud non Microsoft, confirmez votre abonnement [Microsoft 365 et](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) les modules.</span><span class="sxs-lookup"><span data-stu-id="79ab6-110">Before you start using DLP policies to non-Microsoft cloud apps, confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="79ab6-111">Pour accéder à cette fonctionnalité et l’utiliser, vous devez avoir l’un de ces abonnements ou modules:</span><span class="sxs-lookup"><span data-stu-id="79ab6-111">To access and use this functionality, you must have one of these subscriptions or add-ons:</span></span>

- <span data-ttu-id="79ab6-112">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="79ab6-112">Microsoft 365 E5</span></span>
- <span data-ttu-id="79ab6-113">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="79ab6-113">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="79ab6-114">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="79ab6-114">Microsoft 365 E5 Security</span></span>

### <a name="permissions"></a><span data-ttu-id="79ab6-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="79ab6-115">Permissions</span></span>
<span data-ttu-id="79ab6-116">L’utilisateur qui crée la stratégie DLP doit être :</span><span class="sxs-lookup"><span data-stu-id="79ab6-116">The user who creates the DLP policy should be a:</span></span>
- <span data-ttu-id="79ab6-117">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="79ab6-117">Global administrator</span></span>
- <span data-ttu-id="79ab6-118">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="79ab6-118">Compliance administrator</span></span>
- <span data-ttu-id="79ab6-119">Administrateur des données de conformité</span><span class="sxs-lookup"><span data-stu-id="79ab6-119">Compliance data administrator</span></span>

### <a name="prepare-your-cloud-app-security-environment"></a><span data-ttu-id="79ab6-120">Préparer votre environnement Sécurité des applications cloud de travail</span><span class="sxs-lookup"><span data-stu-id="79ab6-120">Prepare your Cloud App Security environment</span></span>

<span data-ttu-id="79ab6-121">Les stratégies DLP pour les applications cloud non Microsoft utilisent Sécurité des applications cloud fonctionnalités DLP.</span><span class="sxs-lookup"><span data-stu-id="79ab6-121">DLP policies to non-Microsoft cloud apps use Cloud App Security DLP capabilities.</span></span> <span data-ttu-id="79ab6-122">Pour l’utiliser, vous devez préparer votre environnement Sécurité des applications cloud de travail.</span><span class="sxs-lookup"><span data-stu-id="79ab6-122">To use it, you should prepare your Cloud App Security environment.</span></span> <span data-ttu-id="79ab6-123">Pour obtenir des instructions, voir Définir des actions de visibilité, de protection et de gouvernance [instantanées pour vos applications.](/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps)</span><span class="sxs-lookup"><span data-stu-id="79ab6-123">For instructions, see [Set instant visibility, protection, and governance actions for your apps](/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps).</span></span>

### <a name="connect-a-non-microsoft-cloud-app"></a><span data-ttu-id="79ab6-124">Connecter application cloud non-Microsoft</span><span class="sxs-lookup"><span data-stu-id="79ab6-124">Connect a non-Microsoft cloud app</span></span>

<span data-ttu-id="79ab6-125">Pour utiliser la stratégie DLP sur une application cloud non-Microsoft spécifique, l’application doit être connectée à Sécurité des applications cloud.</span><span class="sxs-lookup"><span data-stu-id="79ab6-125">To use DLP policy to a specific non-Microsoft cloud app, the app must be connected to Cloud App Security.</span></span> <span data-ttu-id="79ab6-126">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="79ab6-126">For information, see:</span></span>

- [<span data-ttu-id="79ab6-127">Connecter Box</span><span class="sxs-lookup"><span data-stu-id="79ab6-127">Connect Box</span></span>](/cloud-app-security/connect-box-to-microsoft-cloud-app-security)
- [<span data-ttu-id="79ab6-128">Connecter Dropbox</span><span class="sxs-lookup"><span data-stu-id="79ab6-128">Connect Dropbox</span></span>](/cloud-app-security/connect-dropbox-to-microsoft-cloud-app-security)
- [<span data-ttu-id="79ab6-129">Connecter G-Suite</span><span class="sxs-lookup"><span data-stu-id="79ab6-129">Connect G-Suite</span></span>](/cloud-app-security/connect-google-apps-to-microsoft-cloud-app-security)
- [<span data-ttu-id="79ab6-130">Connecter Salesforce</span><span class="sxs-lookup"><span data-stu-id="79ab6-130">Connect Salesforce</span></span>](/cloud-app-security/connect-salesforce-to-microsoft-cloud-app-security)
- [<span data-ttu-id="79ab6-131">Connecter Cisco Webex</span><span class="sxs-lookup"><span data-stu-id="79ab6-131">Connect Cisco Webex</span></span>](/cloud-app-security/connect-webex-to-microsoft-cloud-app-security)

<span data-ttu-id="79ab6-132">Une fois que vous avez connecté vos applications cloud Sécurité des applications cloud, vous pouvez créer Microsoft 365 stratégies DLP pour elles.</span><span class="sxs-lookup"><span data-stu-id="79ab6-132">After you connect your cloud apps to Cloud App Security, you can create Microsoft 365 DLP policies for them.</span></span>

> [!NOTE]
> <span data-ttu-id="79ab6-133">Il est également possible d’utiliser Microsoft Cloud App Security pour créer des stratégies DLP dans les applications cloud De Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79ab6-133">It's also possible to use Microsoft Cloud App Security to create DLP policies to Microsoft cloud apps.</span></span> <span data-ttu-id="79ab6-134">Toutefois, il est recommandé d’utiliser Microsoft 365 pour créer et gérer des stratégies DLP dans les applications cloud De Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79ab6-134">However, it's recommended to use Microsoft 365 to create and manage DLP policies to Microsoft cloud apps.</span></span>

## <a name="create-a-dlp-policy-to-a-non-microsoft-cloud-app"></a><span data-ttu-id="79ab6-135">Créer une stratégie DLP pour une application cloud non-Microsoft</span><span class="sxs-lookup"><span data-stu-id="79ab6-135">Create a DLP policy to a non-Microsoft cloud app</span></span>

<span data-ttu-id="79ab6-136">Lorsque vous sélectionnez un emplacement pour la stratégie DLP, Microsoft Cloud App Security **emplacement.**</span><span class="sxs-lookup"><span data-stu-id="79ab6-136">When you select a location for the DLP policy, turn on the **Microsoft Cloud App Security** location.</span></span>

- <span data-ttu-id="79ab6-137">Pour sélectionner une application ou une instance spécifique, **sélectionnez Instance.**</span><span class="sxs-lookup"><span data-stu-id="79ab6-137">To select a specific app or instance, select **Choose instance**.</span></span>
- <span data-ttu-id="79ab6-138">Si vous ne sélectionnez pas d’instance, la stratégie utilise toutes les applications connectées dans Microsoft Cloud App Security client.</span><span class="sxs-lookup"><span data-stu-id="79ab6-138">If you don't select an instance, the policy uses all connected apps in your Microsoft Cloud App Security tenant.</span></span>

   ![Emplacements pour appliquer la stratégie](../media/1-dlp-non-microsoft-cloud-app-choose-instance.png)

   ![Box-US et Box-General](../media/2-dlp-non-microsoft-cloud-app-box.png)

<span data-ttu-id="79ab6-141">Vous pouvez choisir différentes actions pour chaque application cloud non-Microsoft prise en charge.</span><span class="sxs-lookup"><span data-stu-id="79ab6-141">You can choose various actions for every supported non-Microsoft cloud app.</span></span> <span data-ttu-id="79ab6-142">Pour chaque application, il existe différentes actions possibles (dépend de l’API de l’application cloud).</span><span class="sxs-lookup"><span data-stu-id="79ab6-142">For every app, there are different possible actions (depends on the cloud app API).</span></span>

![Créer une règle](../media/3-dlp-non-microsoft-cloud-app-create-rule.png)

<span data-ttu-id="79ab6-144">Lorsque vous créez une règle dans la stratégie DLP, vous pouvez sélectionner une action pour les applications cloud autres que Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79ab6-144">When you create a rule in the DLP policy, you can select an action for non-Microsoft cloud apps.</span></span> <span data-ttu-id="79ab6-145">Pour restreindre les applications tierces, **sélectionnez Restreindre les applications tierces.**</span><span class="sxs-lookup"><span data-stu-id="79ab6-145">To restrict third-party apps, select **Restrict Third Party Apps**.</span></span>

![Restreindre les applications tierces](../media/4-dlp-non-microsoft-cloud-app-restrict-third-party-apps.png)

> [!NOTE]
> <span data-ttu-id="79ab6-147">Les stratégies DLP appliquées aux applications non-Microsoft utilisent Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="79ab6-147">DLP policies applied to non-Microsoft apps use Microsoft Cloud App Security.</span></span> <span data-ttu-id="79ab6-148">Lorsque la stratégie DLP pour une application non-Microsoft est créée, la même stratégie est automatiquement créée dans Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="79ab6-148">When the DLP policy for a non-Microsoft app is created, the same policy will be automatically created in Microsoft Cloud App Security.</span></span>

<span data-ttu-id="79ab6-149">Pour plus d’informations sur la création et la configuration des stratégies DLP, voir Créer un test et [régler une stratégie DLP.](./create-test-tune-dlp-policy.md)</span><span class="sxs-lookup"><span data-stu-id="79ab6-149">For information about creating and configuring DLP policies, see [Create test and tune a DLP policy](./create-test-tune-dlp-policy.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="79ab6-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79ab6-150">See Also</span></span>

- [<span data-ttu-id="79ab6-151">Créer un test et régler une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="79ab6-151">Create test and tune a DLP policy</span></span>](./create-test-tune-dlp-policy.md)
- [<span data-ttu-id="79ab6-152">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="79ab6-152">Get started with the default DLP policy</span></span>](./get-started-with-the-default-dlp-policy.md)
- [<span data-ttu-id="79ab6-153">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="79ab6-153">Create a DLP policy from a template</span></span>](./create-a-dlp-policy-from-a-template.md)
