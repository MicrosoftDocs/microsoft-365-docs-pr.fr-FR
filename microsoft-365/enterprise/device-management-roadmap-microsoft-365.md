---
title: Gestion des appareils mobiles pour Microsoft 365
keywords: Microsoft 365, Microsoft 365 pour entreprise, documentation Microsoft 365, gestion des appareils mobiles, Intune
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
description: Feuille de route de la mise en place de la gestion des appareils pour Microsoft 365.
ms.openlocfilehash: 4c37033898865372fea19ddbb53ec9c8586f27b1
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918965"
---
# <a name="device-management-roadmap-for-microsoft-365"></a><span data-ttu-id="cedf2-104">Gestion des appareils mobiles pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cedf2-104">Device management roadmap for Microsoft 365</span></span>

<span data-ttu-id="cedf2-105">Microsoft 365 entreprise inclut des fonctionnalités pour vous aider à gérer les appareils et leurs applications au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cedf2-105">Microsoft 365 for enterprise includes features to help manage devices, and their apps, within your organization.</span></span> <span data-ttu-id="cedf2-106">La gestion des appareils mobiles vous permet de sécuriser et de protéger les ressources de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cedf2-106">Managing mobile devices helps you secure and protect your organization's resources.</span></span>

<span data-ttu-id="cedf2-107">Il existe deux options de gestion des appareils :</span><span class="sxs-lookup"><span data-stu-id="cedf2-107">There are two options for device management:</span></span>

- [<span data-ttu-id="cedf2-108">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="cedf2-108">Microsoft Intune</span></span>](#microsoft-intune)
- [<span data-ttu-id="cedf2-109">Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="cedf2-109">Basic Mobility and Security</span></span>](#basic-mobility-and-security)

## <a name="microsoft-intune"></a><span data-ttu-id="cedf2-110">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="cedf2-110">Microsoft Intune</span></span>

<span data-ttu-id="cedf2-111">Vous pouvez utiliser Microsoft Intune pour gérer l’accès à votre organisation à l’aide de la gestion des appareils mobiles ou de la gestion des applications mobiles.</span><span class="sxs-lookup"><span data-stu-id="cedf2-111">You can use Microsoft Intune to manage access to your organization using mobile device management or mobile application management.</span></span> <span data-ttu-id="cedf2-112">La gestion des appareils mobiles est le cas lorsque les utilisateurs « inscrivent » leurs appareils dans Intune.</span><span class="sxs-lookup"><span data-stu-id="cedf2-112">Mobile device management is when users "enroll" their devices in Intune.</span></span> <span data-ttu-id="cedf2-113">Une fois qu’un appareil est inscrit, il s’agit d’un appareil géré . par conséquent, il peut recevoir les stratégies, règles et paramètres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cedf2-113">After a device is enrolled, it is a managed device; therefore, it can receive your organization's  policies, rules, and settings.</span></span> <span data-ttu-id="cedf2-114">Par exemple, vous pouvez installer des applications spécifiques, créer une stratégie de mot de passe, installer une connexion VPN, etc.</span><span class="sxs-lookup"><span data-stu-id="cedf2-114">For example, you can install specific apps, create a password policy, install a VPN connection, and more.</span></span>

<span data-ttu-id="cedf2-115">Les utilisateurs ayant leurs propres appareils personnels peuvent ne pas vouloir inscrire leurs appareils ou être gérés par Intune et les stratégies de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cedf2-115">Users with their own personal devices may not want to enroll their devices or be managed by Intune and your organization's policies.</span></span> <span data-ttu-id="cedf2-116">Toutefois, vous devez toujours protéger les ressources et les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cedf2-116">But you still need to protect your organization's resources and data.</span></span> <span data-ttu-id="cedf2-117">Dans ce scénario, vous pouvez protéger vos applications à l’aide de la gestion des applications mobiles.</span><span class="sxs-lookup"><span data-stu-id="cedf2-117">In this scenario, you can protect your apps using mobile application management.</span></span> <span data-ttu-id="cedf2-118">Par exemple, vous pouvez utiliser une stratégie de gestion des applications mobiles qui oblige un utilisateur à entrer un code confidentiel lors de l’accès à SharePoint Online sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cedf2-118">For example, you can use a mobile application management policy that requires a user to enter a PIN when accessing SharePoint Online on the device.</span></span>

<span data-ttu-id="cedf2-119">Vous déterminerez également la façon dont vous allez gérer les appareils personnels et les appareils dont l’organisation est propriétaire.</span><span class="sxs-lookup"><span data-stu-id="cedf2-119">You'll also determine how you're going to manage personal devices and organization-owned devices.</span></span> <span data-ttu-id="cedf2-120">Vous souhaitez peut-être traiter les appareils différemment, en fonction de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="cedf2-120">You might want to treat devices differently, depending on their uses.</span></span>

## <a name="basic-mobility-and-security"></a><span data-ttu-id="cedf2-121">Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="cedf2-121">Basic Mobility and Security</span></span>

<span data-ttu-id="cedf2-122">Il est intégré à Microsoft 365 et vous permet de sécuriser et de gérer les appareils mobiles de vos utilisateurs tels que les iPhone, iPad, Android et téléphones Windows.</span><span class="sxs-lookup"><span data-stu-id="cedf2-122">This is built into Microsoft 365 and helps you secure and manage your users' mobile devices like iPhones, iPads, Androids, and Windows phones.</span></span> <span data-ttu-id="cedf2-123">Vous pouvez créer et gérer des stratégies de sécurité des appareils, réinitialiser un appareil à distance et afficher des rapports détaillés sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="cedf2-123">You can create and manage device security policies, remotely wipe a device, and view detailed device reports.</span></span>

## <a name="choose-between-the-two-options"></a><span data-ttu-id="cedf2-124">Choisir entre les deux options</span><span class="sxs-lookup"><span data-stu-id="cedf2-124">Choose between the two options</span></span>

<span data-ttu-id="cedf2-125">Pour vous aider à mieux évaluer l’option de gestion des appareils la mieux choisie, voir Choisir entre [Basic Mobility Security et Intune.](/office365/securitycompliance/choose-between-mdm-and-intune)</span><span class="sxs-lookup"><span data-stu-id="cedf2-125">To help you better assess which device management option is best for you, see [Choose between Basic Mobility Security and Intune](/office365/securitycompliance/choose-between-mdm-and-intune).</span></span>

<span data-ttu-id="cedf2-126">En fonction de votre évaluation, vous pouvez commencer à gérer vos appareils avec :</span><span class="sxs-lookup"><span data-stu-id="cedf2-126">Based on your assessment, get started managing your devices with:</span></span>

- [<span data-ttu-id="cedf2-127">Intune</span><span class="sxs-lookup"><span data-stu-id="cedf2-127">Intune</span></span>](/mem/intune/fundamentals/planning-guide)
- [<span data-ttu-id="cedf2-128">Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="cedf2-128">Basic Mobility and Security</span></span>](https://support.microsoft.com/office/set-up-basic-mobility-and-security-dd892318-bc44-4eb1-af00-9db5430be3cd)
 
## <a name="identity-and-device-access-recommendations"></a><span data-ttu-id="cedf2-129">Recommandations en matière d’identité et d’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="cedf2-129">Identity and device access recommendations</span></span>

<span data-ttu-id="cedf2-130">Microsoft fournit un ensemble de recommandations sur l’[accès aux appareils et à l’identité](../security/office-365-security/microsoft-365-policies-configurations.md) pour garantir un personnel conforme et productif.</span><span class="sxs-lookup"><span data-stu-id="cedf2-130">Microsoft provides a set of recommendations for [identity and device access](../security/office-365-security/microsoft-365-policies-configurations.md) to ensure a secure and productive workforce.</span></span> <span data-ttu-id="cedf2-131">Pour l’accès aux appareils, utilisez les recommandations et les paramètres des articles suivants :</span><span class="sxs-lookup"><span data-stu-id="cedf2-131">For device access, use the recommendations and settings in these articles:</span></span>

- [<span data-ttu-id="cedf2-132">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="cedf2-132">Prerequisites</span></span>](../security/office-365-security/identity-access-prerequisites.md)
- [<span data-ttu-id="cedf2-133">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="cedf2-133">Common identity and device access policies</span></span>](../security/office-365-security/identity-access-policies.md)

## <a name="how-contoso-did-device-management-for-microsoft-365"></a><span data-ttu-id="cedf2-134">Comment Contoso a fait la gestion des appareils pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cedf2-134">How Contoso did device management for Microsoft 365</span></span>

<span data-ttu-id="cedf2-135">Pour plus d’informations sur la façon dont une entreprise multinationale fictive mais représentative a déployé son infrastructure de gestion des appareils mobiles avec les services cloud de Microsoft 365, voir Gestion des appareils mobiles [pour Contoso.](contoso-mdm.md)</span><span class="sxs-lookup"><span data-stu-id="cedf2-135">For information about how a fictional but representative multi-national business deployed their mobile device management infrastructure with Microsoft 365 cloud services, see [Mobile device management for Contoso](contoso-mdm.md).</span></span>