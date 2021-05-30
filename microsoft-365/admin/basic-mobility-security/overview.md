---
title: Vue d’ensemble de la mobilité et de la sécurité de base pour Microsoft 365
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
search.appverid:
- MET150
description: Utilisez Basic Mobility and Security pour définir des stratégies de sécurité des appareils et des règles d’accès.
ms.openlocfilehash: 37be420a4b9499da3d1290b8b6a898b9fcb09c5b
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706309"
---
# <a name="overview-of-basic-mobility-and-security-for-microsoft-365"></a><span data-ttu-id="40abc-103">Vue d’ensemble de la mobilité et de la sécurité de base pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="40abc-103">Overview of Basic Mobility and Security for Microsoft 365</span></span>

<span data-ttu-id="40abc-104">Vous pouvez gérer et sécuriser les appareils mobiles lorsqu’ils sont connectés à votre organisation Microsoft 365 à l’aide de Basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="40abc-104">You can manage and secure mobile devices when they're connected to your Microsoft 365 organization by using Basic Mobility and Security.</span></span> <span data-ttu-id="40abc-105">Les appareils mobiles, tels que les smartphones et les tablettes, utilisés pour accéder à la messagerie, au calendrier, aux contacts et aux documents professionnels donnent aux employés la possibilité d’effectuer leur travail partout, à tout moment.</span><span class="sxs-lookup"><span data-stu-id="40abc-105">Mobile devices like smartphones and tablets that are used to access work email, calendar, contacts, and documents play a big part in making sure that employees get their work done anytime, from anywhere.</span></span> <span data-ttu-id="40abc-106">Il est donc essentiel de protéger les informations de votre organisation lorsque des personnes utilisent des appareils.</span><span class="sxs-lookup"><span data-stu-id="40abc-106">So it’s critical that you help protect your organization's information when people use devices.</span></span> <span data-ttu-id="40abc-107">Vous pouvez utiliser la mobilité et la sécurité de base pour définir des stratégies de sécurité des appareils et des règles d’accès, et pour effacer les appareils mobiles en cas de perte ou de vol.</span><span class="sxs-lookup"><span data-stu-id="40abc-107">You can use Basic Mobility and Security to set device security policies and access rules, and to wipe mobile devices if they’re lost or stolen.</span></span>

:::image type="content" source="../../media/basic-mobility-security/bms-3-setup.png" alt-text="Configuration de base de la mobilité et de la sécurité":::

## <a name="what-types-of-devices-can-you-manage"></a><span data-ttu-id="40abc-109">Quels types d’appareils pouvez-vous gérer ?</span><span class="sxs-lookup"><span data-stu-id="40abc-109">What types of devices can you manage?</span></span>

<span data-ttu-id="40abc-110">Vous pouvez utiliser la mobilité et la sécurité de base pour gérer de nombreux types d’appareils mobiles tels que Windows Phone, Android, iPhone et iPad.</span><span class="sxs-lookup"><span data-stu-id="40abc-110">You can use Basic Mobility and Security to manage many types of mobile devices like Windows Phone, Android, iPhone, and iPad.</span></span> <span data-ttu-id="40abc-111">Pour gérer les appareils mobiles utilisés par les membres de votre organisation, chaque personne doit avoir une licence Microsoft 365 applicable et son appareil doit être inscrit à Basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="40abc-111">To manage mobile devices used by people in your organization, each person must have an applicable Microsoft 365 license and their device must be enrolled in Basic Mobility and Security.</span></span>

<span data-ttu-id="40abc-112">Pour voir ce que Basic Mobility and Security prend en charge pour chaque type d’appareil, voir [Fonctionnalités de basic Mobility and Security](capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="40abc-112">To see what Basic Mobility and Security supports for each type of device, see [Capabilities of Basic Mobility and Security](capabilities.md).</span></span>

## <a name="setup-steps-for-basic-mobility-and-security"></a><span data-ttu-id="40abc-113">Étapes de configuration de Basic Mobility and Security</span><span class="sxs-lookup"><span data-stu-id="40abc-113">Setup steps for Basic Mobility and Security</span></span>

<span data-ttu-id="40abc-114">Un administrateur Microsoft 365 global doit effectuer les étapes suivantes pour activer et configurer Basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="40abc-114">A Microsoft 365 global admin must complete the following steps to activate and set up Basic Mobility and Security.</span></span> <span data-ttu-id="40abc-115">Pour obtenir la procédure détaillée, suivez les instructions de [la procédure Set up Basic Mobility and Security](set-up.md).</span><span class="sxs-lookup"><span data-stu-id="40abc-115">For detailed steps, follow the guidance in [Set up Basic Mobility and Security](set-up.md).</span></span> 

<span data-ttu-id="40abc-116">Voici un résumé des étapes :</span><span class="sxs-lookup"><span data-stu-id="40abc-116">Here's a summary of the steps:</span></span>

<span data-ttu-id="40abc-117">**Étape 1 :** Activez Basic Mobility and Security en suivant les étapes de la procédure  [Set up Basic Mobility and Security](set-up.md).</span><span class="sxs-lookup"><span data-stu-id="40abc-117">**Step 1:** Activate Basic Mobility and Security by following steps in the [Set up Basic Mobility and Security](set-up.md).</span></span>

<span data-ttu-id="40abc-118">**Étape 2 :** Configurer La mobilité et la sécurité de base en créant, par exemple, un certificat APNs pour gérer les appareils iOS et en ajoutant un enregistrement DNS (Domain Name System) pour votre domaine afin de prendre en charge Windows téléphones.</span><span class="sxs-lookup"><span data-stu-id="40abc-118">**Step 2:** Set up Basic Mobility and Security by, for example, creating an APNs certificate to manage iOS devices and adding a Domain Name System (DNS) record for your domain to support Windows phones.</span></span>

<span data-ttu-id="40abc-119">**Étape 3 :** Créez des stratégies d’appareil et appliquez-les à des groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="40abc-119">**Step 3:** Create device policies and apply them to groups of users.</span></span> <span data-ttu-id="40abc-120">Lorsque vous faites cela, vos utilisateurs obtiennent un message d’inscription sur leur appareil, et une fois l’inscription terminée, leurs appareils sont limités par les stratégies que vous avez définies pour eux.</span><span class="sxs-lookup"><span data-stu-id="40abc-120">When you do this, your users get an enrollment message on their device, and when they've completed enrollment, their devices are restricted by the policies you've set up for them.</span></span> <span data-ttu-id="40abc-121">Pour plus d’informations, voir [Inscrire votre appareil mobile à l’aide de Basic Mobility and Security](enroll-your-mobile-device.md).</span><span class="sxs-lookup"><span data-stu-id="40abc-121">For more info, see [Enroll your mobile device using Basic Mobility and Security](enroll-your-mobile-device.md).</span></span> 

:::image type="content" source="../../media/basic-mobility-security/bms-4-policy.png" alt-text="Paramètres de stratégie de sécurité et de mobilité de base":::

## <a name="device-management-tasks"></a><span data-ttu-id="40abc-123">Tâches de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="40abc-123">Device management tasks</span></span>

<span data-ttu-id="40abc-124">Une fois que vous avez installé Basic Mobility and Security et que vos utilisateurs ont inscrit leurs appareils, vous pouvez gérer les appareils, bloquer l’accès ou effacer un appareil, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="40abc-124">After you've got Basic Mobility and Security set up and your users have enrolled their devices, you can manage the devices, block access, or wipe a device, if necessary.</span></span> <span data-ttu-id="40abc-125">Pour en savoir plus sur certaines tâches courantes de gestion des [appareils,](manage-enrolled-devices.md)notamment sur l’endroit où effectuer les tâches, voir Gérer les appareils inscrits dans Gestion des appareils mobiles pour Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="40abc-125">To learn more about some common device management tasks, including where to complete the tasks, see [Manage devices enrolled in Mobile Device Management for Microsoft 365](manage-enrolled-devices.md).</span></span>

## <a name="other-ways-to-manage-devices-and-apps"></a><span data-ttu-id="40abc-126">Autres façons de gérer les appareils et les applications</span><span class="sxs-lookup"><span data-stu-id="40abc-126">Other ways to manage devices and apps</span></span>

<span data-ttu-id="40abc-127">Si vous avez simplement besoin de la gestion des applications mobiles (MAM), par exemple pour les personnes mettant à jour des projets de travail sur leurs propres appareils, Intune propose une autre option en plus de l’inscription et de la gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="40abc-127">If you just need mobile app management (MAM), perhaps for people updating work projects on their own devices, Intune provides another option besides enrolling and managing devices.</span></span> <span data-ttu-id="40abc-128">Un abonnement Intune vous permet de configurer des stratégies MAM à l’aide du portail Azure, même si les appareils des personnes ne sont pas inscrits dans Intune.</span><span class="sxs-lookup"><span data-stu-id="40abc-128">An Intune subscription allows you to set up MAM policies by using the Azure portal, even if people's devices aren't enrolled in Intune.</span></span> <span data-ttu-id="40abc-129">Pour plus d’informations, voir [vue d’ensemble des stratégies de protection des applications.](/mem/intune/apps/app-protection-policy)</span><span class="sxs-lookup"><span data-stu-id="40abc-129">For more info, see [App protection policies overview](/mem/intune/apps/app-protection-policy).</span></span>

## <a name="related-content"></a><span data-ttu-id="40abc-130">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="40abc-130">Related content</span></span>

<span data-ttu-id="40abc-131">[Configurer la mobilité et la sécurité de](set-up.md) base (article)</span><span class="sxs-lookup"><span data-stu-id="40abc-131">[Set up Basic Mobility and Security](set-up.md) (article)</span></span>\
<span data-ttu-id="40abc-132">[Inscrire votre appareil mobile à l’aide de Basic Mobility and Security](enroll-your-mobile-device.md) (article)</span><span class="sxs-lookup"><span data-stu-id="40abc-132">[Enroll your mobile device using Basic Mobility and Security](enroll-your-mobile-device.md) (article)</span></span>\
<span data-ttu-id="40abc-133">[Gérer les appareils inscrits à Gestion des](manage-enrolled-devices.md) appareils mobiles pour Microsoft 365 (article)</span><span class="sxs-lookup"><span data-stu-id="40abc-133">[Manage devices enrolled in Mobile Device Management for Microsoft 365](manage-enrolled-devices.md) (article)</span></span>\
<span data-ttu-id="40abc-134">[Obtenir des détails sur les appareils gérés par Basic Mobility and Security](get-details-about-managed-devices.md) (article)</span><span class="sxs-lookup"><span data-stu-id="40abc-134">[Get details about devices managed by Basic Mobility and Security](get-details-about-managed-devices.md) (article)</span></span>