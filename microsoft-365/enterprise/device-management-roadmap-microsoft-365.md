---
title: Feuille de route de gestion des appareils pour Microsoft 365
keywords: Microsoft 365, Microsoft 365 pour Enterprise, documentation Microsoft 365, gestion des appareils mobiles, Intune
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 08/10/2020
ms.topic: conceptual
f1.keywords:
- NOCSH
ms.prod: microsoft-365-enterprise
ms.service: ''
ms.technology: ''
ms.assetid: fb4182e6-5e78-45d0-9641-d791c4519441
audience: ITPro
ms.custom: microsoft-intune
description: La feuille de route pour configurer la gestion des appareils pour Microsoft 365.
ms.openlocfilehash: 79be47d6bc83c124f2203866986e06181a1f7f3d
ms.sourcegitcommit: ae646779d84e993cf80b1207e76b856a21be5790
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2021
ms.locfileid: "49749538"
---
# <a name="device-management-roadmap-for-microsoft-365"></a><span data-ttu-id="34ecb-104">Feuille de route de gestion des appareils pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="34ecb-104">Device management roadmap for Microsoft 365</span></span>

<span data-ttu-id="34ecb-105">Microsoft 365 for Enterprise inclut des fonctionnalités qui permettent de gérer les appareils et leurs applications au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-105">Microsoft 365 for enterprise includes features to help manage devices, and their apps, within your organization.</span></span> <span data-ttu-id="34ecb-106">La gestion des appareils mobiles vous permet de sécuriser et de protéger les ressources de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-106">Managing mobile devices helps you secure and protect your organization's resources.</span></span>

<span data-ttu-id="34ecb-107">Il existe deux options pour la gestion des appareils :</span><span class="sxs-lookup"><span data-stu-id="34ecb-107">There are two options for device management:</span></span>

- [<span data-ttu-id="34ecb-108">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="34ecb-108">Microsoft Intune</span></span>](#microsoft-intune)
- [<span data-ttu-id="34ecb-109">Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="34ecb-109">Basic Mobility and Security</span></span>](#basic-mobility-and-security)

## <a name="microsoft-intune"></a><span data-ttu-id="34ecb-110">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="34ecb-110">Microsoft Intune</span></span>

<span data-ttu-id="34ecb-111">Vous pouvez utiliser Microsoft Intune pour gérer l’accès à votre organisation à l’aide de la gestion des appareils mobiles ou de la gestion des applications mobiles.</span><span class="sxs-lookup"><span data-stu-id="34ecb-111">You can use Microsoft Intune to manage access to your organization using mobile device management or mobile application management.</span></span> <span data-ttu-id="34ecb-112">La gestion des appareils mobiles s’avère lorsque les utilisateurs « inscrivent » leurs appareils dans Intune.</span><span class="sxs-lookup"><span data-stu-id="34ecb-112">Mobile device management is when users "enroll" their devices in Intune.</span></span> <span data-ttu-id="34ecb-113">Après l’enregistrement d’un appareil, il s’agit d’un appareil géré ; par conséquent, il peut recevoir les stratégies, les règles et les paramètres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-113">After a device is enrolled, it is a managed device; therefore, it can receive your organization's  policies, rules, and settings.</span></span> <span data-ttu-id="34ecb-114">Par exemple, vous pouvez installer des applications spécifiques, créer une stratégie de mot de passe, installer une connexion VPN, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="34ecb-114">For example, you can install specific apps, create a password policy, install a VPN connection, and more.</span></span>

<span data-ttu-id="34ecb-115">Les utilisateurs disposant de leurs propres appareils personnels peuvent ne pas vouloir inscrire leurs appareils ou être gérés par Intune et les stratégies de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-115">Users with their own personal devices may not want to enroll their devices or be managed by Intune and your organization's policies.</span></span> <span data-ttu-id="34ecb-116">Toutefois, vous devez toujours protéger les ressources et les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-116">But you still need to protect your organization's resources and data.</span></span> <span data-ttu-id="34ecb-117">Dans ce scénario, vous pouvez protéger vos applications à l’aide de la gestion des applications mobiles.</span><span class="sxs-lookup"><span data-stu-id="34ecb-117">In this scenario, you can protect your apps using mobile application management.</span></span> <span data-ttu-id="34ecb-118">Par exemple, vous pouvez utiliser une stratégie de gestion des applications mobiles qui exige qu’un utilisateur entre un code confidentiel lors de l’accès à SharePoint Online sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="34ecb-118">For example, you can use a mobile application management policy that requires a user to enter a PIN when accessing SharePoint Online on the device.</span></span>

<span data-ttu-id="34ecb-119">Vous allez également déterminer la manière dont vous allez gérer les appareils personnels et les appareils appartenant à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-119">You'll also determine how you're going to manage personal devices and organization-owned devices.</span></span> <span data-ttu-id="34ecb-120">Vous souhaiterez peut-être traiter les appareils différemment en fonction de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="34ecb-120">You might want to treat devices differently, depending on their uses.</span></span>

## <a name="basic-mobility-and-security"></a><span data-ttu-id="34ecb-121">Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="34ecb-121">Basic Mobility and Security</span></span>

<span data-ttu-id="34ecb-122">Il est intégré à Microsoft 365 et vous aide à sécuriser et gérer les appareils mobiles de vos utilisateurs, tels que les iPhone, les iPad, les Android et les téléphones Windows.</span><span class="sxs-lookup"><span data-stu-id="34ecb-122">This is built into Microsoft 365 and helps you secure and manage your users' mobile devices like iPhones, iPads, Androids, and Windows phones.</span></span> <span data-ttu-id="34ecb-123">Vous pouvez créer et gérer des stratégies de sécurité des appareils, réinitialiser un appareil à distance et afficher des rapports détaillés sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="34ecb-123">You can create and manage device security policies, remotely wipe a device, and view detailed device reports.</span></span>

## <a name="choose-between-the-two-options"></a><span data-ttu-id="34ecb-124">Choisir entre les deux options</span><span class="sxs-lookup"><span data-stu-id="34ecb-124">Choose between the two options</span></span>

<span data-ttu-id="34ecb-125">Pour vous aider à mieux évaluer l’option de gestion des appareils qui vous convient le mieux, voir [Choose between Basic Mobility Security and Intune](https://docs.microsoft.com/office365/securitycompliance/choose-between-mdm-and-intune).</span><span class="sxs-lookup"><span data-stu-id="34ecb-125">To help you better assess which device management option is best for you, see [Choose between Basic Mobility Security and Intune](https://docs.microsoft.com/office365/securitycompliance/choose-between-mdm-and-intune).</span></span>

<span data-ttu-id="34ecb-126">En fonction de votre évaluation, commencez à gérer vos appareils avec :</span><span class="sxs-lookup"><span data-stu-id="34ecb-126">Based on your assessment, get started managing your devices with:</span></span>

- [<span data-ttu-id="34ecb-127">Intune</span><span class="sxs-lookup"><span data-stu-id="34ecb-127">Intune</span></span>](https://docs.microsoft.com/mem/intune/fundamentals/planning-guide)
- [<span data-ttu-id="34ecb-128">Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="34ecb-128">Basic Mobility and Security</span></span>](https://support.microsoft.com/office/set-up-basic-mobility-and-security-dd892318-bc44-4eb1-af00-9db5430be3cd)
 
## <a name="identity-and-device-access-recommendations"></a><span data-ttu-id="34ecb-129">Recommandations en matière d’identité et d’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="34ecb-129">Identity and device access recommendations</span></span>

<span data-ttu-id="34ecb-130">Microsoft fournit un ensemble de recommandations sur l’[accès aux appareils et à l’identité](../security/office-365-security/microsoft-365-policies-configurations.md) pour garantir un personnel conforme et productif.</span><span class="sxs-lookup"><span data-stu-id="34ecb-130">Microsoft provides a set of recommendations for [identity and device access](../security/office-365-security/microsoft-365-policies-configurations.md) to ensure a secure and productive workforce.</span></span> <span data-ttu-id="34ecb-131">Pour l’accès aux appareils, utilisez les recommandations et les paramètres présentés dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="34ecb-131">For device access, use the recommendations and settings in these articles:</span></span>

- [<span data-ttu-id="34ecb-132">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="34ecb-132">Prerequisites</span></span>](../security/office-365-security/identity-access-prerequisites.md)
- [<span data-ttu-id="34ecb-133">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="34ecb-133">Common identity and device access policies</span></span>](../security/office-365-security/identity-access-policies.md)

## <a name="how-contoso-did-device-management-for-microsoft-365"></a><span data-ttu-id="34ecb-134">Comment Contoso a fait la gestion des appareils pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="34ecb-134">How Contoso did device management for Microsoft 365</span></span>

<span data-ttu-id="34ecb-135">Pour plus d’informations sur la façon dont une entreprise multinationale fictive mais représentative a déployé son infrastructure de gestion des appareils mobiles avec les services Cloud de Microsoft 365, consultez la rubrique [Mobile Device Management for contoso](contoso-mdm.md).</span><span class="sxs-lookup"><span data-stu-id="34ecb-135">For information about how a fictional but representative multi-national business deployed their mobile device management infrastructure with Microsoft 365 cloud services, see [Mobile device management for Contoso](contoso-mdm.md).</span></span>
