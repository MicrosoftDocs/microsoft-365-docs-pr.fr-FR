---
title: Utiliser des stratégies de protection contre la perte de données pour les applications Cloud non Microsoft (aperçu)
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
description: Découvrez comment utiliser les stratégies DLP pour les applications Cloud non Microsoft.
ms.openlocfilehash: 0b588bf27738a0f9a8078999311294f74e5193c0
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48649655"
---
# <a name="use-data-loss-prevention-policies-for-non-microsoft-cloud-apps-preview"></a><span data-ttu-id="63403-103">Utiliser des stratégies de protection contre la perte de données pour les applications Cloud non Microsoft (aperçu)</span><span class="sxs-lookup"><span data-stu-id="63403-103">Use data loss prevention policies for non-Microsoft cloud apps (preview)</span></span>

<span data-ttu-id="63403-104">Les stratégies de protection contre la perte de données (DLP) pour les applications Cloud non-Microsoft font partie de la suite de fonctionnalités DLP Microsoft 365. à l’aide de ces fonctionnalités, vous pouvez découvrir et protéger des éléments sensibles dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="63403-104">Data loss prevention (DLP) policies to non-Microsoft cloud apps are part of the Microsoft 365 DLP suite of features; using these features, you can discover and protect sensitive items across Microsoft 365 services.</span></span> <span data-ttu-id="63403-105">Pour plus d’informations sur toutes les offres Microsoft DLP, consultez la rubrique [vue d’ensemble de la protection contre la perte de données](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="63403-105">For more information about all Microsoft DLP offerings, see [Overview of data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide).</span></span>

<span data-ttu-id="63403-106">Vous pouvez utiliser les stratégies DLP pour les applications Cloud non-Microsoft pour surveiller et détecter les éléments sensibles utilisés et partagés par les applications Cloud non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63403-106">You can use DLP policies to non-Microsoft cloud apps to monitor and detect when sensitive items are used and shared via non-Microsoft cloud apps.</span></span> <span data-ttu-id="63403-107">L’utilisation de ces stratégies vous offre la visibilité et le contrôle dont vous avez besoin pour vous assurer qu’ils sont correctement utilisés et protégés, et cela permet d’éviter tout comportement risqué susceptible de les compromettre.</span><span class="sxs-lookup"><span data-stu-id="63403-107">Using these policies gives you the visibility and control that you need to ensure that they're correctly used and protected, and it helps prevent risky behavior that might compromise them.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="63403-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="63403-108">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="63403-109">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="63403-109">SKU/subscriptions licensing</span></span>

<span data-ttu-id="63403-110">Avant de commencer à utiliser les stratégies DLP pour les applications Cloud non Microsoft, confirmez votre [abonnement microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="63403-110">Before you start using DLP policies to non-Microsoft cloud apps, confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="63403-111">Pour accéder à cette fonctionnalité et l’utiliser, vous devez disposer de l’un des abonnements ou des modules complémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="63403-111">To access and use this functionality, you must have one of these subscriptions or add-ons:</span></span>

- <span data-ttu-id="63403-112">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="63403-112">Microsoft 365 E5</span></span>
- <span data-ttu-id="63403-113">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="63403-113">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="63403-114">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="63403-114">Microsoft 365 E5 Security</span></span>

### <a name="prepare-your-cloud-app-security-environment"></a><span data-ttu-id="63403-115">Préparer votre environnement de sécurité d’application Cloud</span><span class="sxs-lookup"><span data-stu-id="63403-115">Prepare your Cloud App Security environment</span></span>

<span data-ttu-id="63403-116">Les stratégies DLP pour les applications Cloud non-Microsoft utilisent les fonctionnalités DLP de la sécurité des applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="63403-116">DLP policies to non-Microsoft cloud apps use Cloud App Security DLP capabilities.</span></span> <span data-ttu-id="63403-117">Pour l’utiliser, vous devez préparer votre environnement de sécurité d’application Cloud.</span><span class="sxs-lookup"><span data-stu-id="63403-117">To use it, you should prepare your Cloud App Security environment.</span></span> <span data-ttu-id="63403-118">Pour obtenir des instructions, voir [définir la visibilité instantanée, la protection et les actions de gouvernance pour vos applications](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps).</span><span class="sxs-lookup"><span data-stu-id="63403-118">For instructions, see [Set instant visibility, protection, and governance actions for your apps](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps).</span></span>

### <a name="connect-a-non-microsoft-cloud-app"></a><span data-ttu-id="63403-119">Connecter une application Cloud non-Microsoft</span><span class="sxs-lookup"><span data-stu-id="63403-119">Connect a non-Microsoft cloud app</span></span>

<span data-ttu-id="63403-120">Pour utiliser la stratégie DLP pour une application Cloud non Microsoft spécifique, l’application doit être connectée à la sécurité de l’application Cloud.</span><span class="sxs-lookup"><span data-stu-id="63403-120">To use DLP policy to a specific non-Microsoft cloud app, the app must be connected to Cloud App Security.</span></span> <span data-ttu-id="63403-121">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="63403-121">For information, see:</span></span>

- [<span data-ttu-id="63403-122">Zone de connexion</span><span class="sxs-lookup"><span data-stu-id="63403-122">Connect Box</span></span>](https://docs.microsoft.com/cloud-app-security/connect-box-to-microsoft-cloud-app-security)
- [<span data-ttu-id="63403-123">Connecter Dropbox</span><span class="sxs-lookup"><span data-stu-id="63403-123">Connect Dropbox</span></span>](https://docs.microsoft.com/cloud-app-security/connect-dropbox-to-microsoft-cloud-app-security)
- [<span data-ttu-id="63403-124">Connecter G-suite</span><span class="sxs-lookup"><span data-stu-id="63403-124">Connect G-Suite</span></span>](https://docs.microsoft.com/cloud-app-security/connect-google-apps-to-microsoft-cloud-app-security)
- [<span data-ttu-id="63403-125">Connexion Salesforce</span><span class="sxs-lookup"><span data-stu-id="63403-125">Connect Salesforce</span></span>](https://docs.microsoft.com/cloud-app-security/connect-salesforce-to-microsoft-cloud-app-security)
- [<span data-ttu-id="63403-126">Connexion de Cisco Webex</span><span class="sxs-lookup"><span data-stu-id="63403-126">Connect Cisco Webex</span></span>](https://docs.microsoft.com/cloud-app-security/connect-webex-to-microsoft-cloud-app-security)

<span data-ttu-id="63403-127">Une fois que vous avez connecté vos applications Cloud à la sécurité des applications Cloud, vous pouvez créer des stratégies DLP Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="63403-127">After you connect your cloud apps to Cloud App Security, you can create Microsoft 365 DLP policies for them.</span></span>

>[!NOTE]
><span data-ttu-id="63403-128">Il est également possible d’utiliser Microsoft Cloud App Security pour créer des stratégies DLP sur des applications Cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63403-128">It's also possible to use Microsoft Cloud App Security to create DLP policies to Microsoft cloud apps.</span></span> <span data-ttu-id="63403-129">Toutefois, il est recommandé d’utiliser Microsoft 365 pour créer et gérer des stratégies DLP sur des applications Cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63403-129">However, it's recommended to use Microsoft 365 to create and manage DLP policies to Microsoft cloud apps.</span></span>

## <a name="create-a-dlp-policy-to-a-non-microsoft-cloud-app"></a><span data-ttu-id="63403-130">Créer une stratégie DLP pour une application Cloud non Microsoft</span><span class="sxs-lookup"><span data-stu-id="63403-130">Create a DLP policy to a non-Microsoft cloud app</span></span>

<span data-ttu-id="63403-131">Lorsque vous sélectionnez un emplacement pour la stratégie DLP, activez l’emplacement de sécurité de l' **application Cloud Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="63403-131">When you select a location for the DLP policy, turn on the **Microsoft Cloud App Security** location.</span></span>

- <span data-ttu-id="63403-132">Pour sélectionner une application ou une instance spécifique, sélectionnez **choisir une instance**.</span><span class="sxs-lookup"><span data-stu-id="63403-132">To select a specific app or instance, select **Choose instance**.</span></span>
- <span data-ttu-id="63403-133">Si vous ne sélectionnez pas d’instance, la stratégie utilise toutes les applications connectées de votre client de sécurité Microsoft Cloud App.</span><span class="sxs-lookup"><span data-stu-id="63403-133">If you don't select an instance, the policy uses all connected apps in your Microsoft Cloud App Security tenant.</span></span>

   ![Emplacements auxquels appliquer la stratégie](../media/1-dlp-non-microsoft-cloud-app-choose-instance.png)

   ![Case-US et Box-General](../media/2-dlp-non-microsoft-cloud-app-box.png)

<span data-ttu-id="63403-136">Vous pouvez choisir différentes actions pour toutes les applications Cloud non-Microsoft prises en charge.</span><span class="sxs-lookup"><span data-stu-id="63403-136">You can choose various actions for every supported non-Microsoft cloud app.</span></span> <span data-ttu-id="63403-137">Pour chaque application, il existe différentes actions possibles (en fonction de l’API de l’application Cloud).</span><span class="sxs-lookup"><span data-stu-id="63403-137">For every app, there are different possible actions (depends on the cloud app API).</span></span>

![Créer une règle](../media/3-dlp-non-microsoft-cloud-app-create-rule.png)

<span data-ttu-id="63403-139">Lorsque vous créez une règle dans la stratégie DLP, vous pouvez sélectionner une action pour les applications Cloud non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63403-139">When you create a rule in the DLP policy, you can select an action for non-Microsoft cloud apps.</span></span> <span data-ttu-id="63403-140">Pour restreindre les applications tierces, sélectionnez **restreindre les applications**tierces.</span><span class="sxs-lookup"><span data-stu-id="63403-140">To restrict third-party apps, select **Restrict Third Party Apps**.</span></span>

![Restreindre les applications tierces](../media/4-dlp-non-microsoft-cloud-app-restrict-third-party-apps.png)

<span data-ttu-id="63403-142">Pour plus d’informations sur la création et la configuration des stratégies DLP, voir [Create test and tune a DLP Policy](https://docs.microsoft.com/microsoft-365/compliance/create-test-tune-dlp-policy?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="63403-142">For information about creating and configuring DLP policies, see [Create test and tune a DLP policy](https://docs.microsoft.com/microsoft-365/compliance/create-test-tune-dlp-policy?view=o365-worldwide).</span></span>

## <a name="see-also"></a><span data-ttu-id="63403-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63403-143">See Also</span></span>

- [<span data-ttu-id="63403-144">Créer un test et régler une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="63403-144">Create test and tune a DLP policy</span></span>](https://docs.microsoft.com/microsoft-365/compliance/create-test-tune-dlp-policy?view=o365-worldwide)
- [<span data-ttu-id="63403-145">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="63403-145">Get started with the default DLP policy</span></span>](https://docs.microsoft.com/microsoft-365/compliance/get-started-with-the-default-dlp-policy?view=o365-worldwide)
- [<span data-ttu-id="63403-146">Création d’une stratégie DLP à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="63403-146">Create a DLP policy from a template</span></span>](https://docs.microsoft.com/microsoft-365/compliance/create-a-dlp-policy-from-a-template?view=o365-worldwide)
