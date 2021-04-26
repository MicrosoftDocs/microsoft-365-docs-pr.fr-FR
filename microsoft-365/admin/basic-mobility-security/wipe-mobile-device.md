---
title: Effacement d'un appareil mobile dans Basic Mobility and Security
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
description: Utilisez la mobilité et la sécurité de base intégrées pour supprimer des informations des appareils inscrits.
ms.openlocfilehash: 7830a0f4ef609f6465c171ecab2c9e3c48198424
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52023856"
---
# <a name="wipe-a-mobile-device-in-basic-mobility-and-security"></a><span data-ttu-id="2e2f8-103">Effacement d'un appareil mobile dans Basic Mobility and Security</span><span class="sxs-lookup"><span data-stu-id="2e2f8-103">Wipe a mobile device in Basic Mobility and Security</span></span>

<span data-ttu-id="2e2f8-104">Vous pouvez utiliser la mobilité et la sécurité de base intégrées pour Microsoft 365 pour supprimer uniquement les informations organisationnelles, ou pour effectuer une réinitialisation aux paramètres d'usine pour supprimer toutes les informations d'un appareil mobile et les restaurer aux paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-104">You can use built-in Basic Mobility and Security for Microsoft 365 to remove only organizational information, or to perform a factory reset to delete all information from a mobile device and restore it to factory settings.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2e2f8-105">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2e2f8-105">Before you begin</span></span>

<span data-ttu-id="2e2f8-106">Les appareils mobiles peuvent stocker des informations organisationnelles sensibles et fournir l'accès aux ressources Microsoft 365 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-106">Mobile devices can store sensitive organizational information and provide access to your organization's Microsoft 365 resources.</span></span> <span data-ttu-id="2e2f8-107">Pour protéger les informations de votre organisation, vous pouvez réinitialiser ou supprimer des données d'entreprise aux usine :</span><span class="sxs-lookup"><span data-stu-id="2e2f8-107">To help protect your organization's information, you can do Factory reset or Remove company data:</span></span>

- <span data-ttu-id="2e2f8-108">**Réinitialisation** aux usine : supprime toutes les données sur l'appareil mobile d'un utilisateur, y compris les applications installées, les photos et les informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-108">**Factory reset**: Deletes all data on a user's mobile device, including installed applications, photos, and personal information.</span></span> <span data-ttu-id="2e2f8-109">Une fois l'effacement terminé, l'appareil est rétabli à ses paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-109">When the wipe is complete, the device is restored to its factory settings.</span></span>

- <span data-ttu-id="2e2f8-110">**Supprimer des données d'entreprise**: supprime uniquement les données de l'organisation et laisse les applications installées, les photos et les informations personnelles sur l'appareil mobile d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-110">**Remove company data**: Removes only organization data and leaves installed applications, photos, and personal information on a user's mobile device.</span></span>

- <span data-ttu-id="2e2f8-111">**Lorsqu'un appareil est** réinitialisé (réinitialisation d'usine ou suppression des données d'entreprise), l'appareil est supprimé de la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-111">**When a device is wiped (Factory Reset or Remove Company Data)**, the device is removed from the list of managed devices.</span></span>
    
- <span data-ttu-id="2e2f8-112">**Réinitialiser** automatiquement un appareil : vous pouvez configurer une stratégie de mobilité et de sécurité de base qui réinitialise automatiquement un appareil après que l'utilisateur a tenté sans succès d'entrer le mot de passe de l'appareil un certain nombre de fois.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-112">**Automatically reset a device**: You can set up a Basic Mobility and Security policy that automatically factory resets a device after the user unsuccessfully tries to enter the device password a specific number of times.</span></span> <span data-ttu-id="2e2f8-113">Pour ce faire, suivez les étapes de la procédure de création de stratégies de sécurité des appareils [dans la mobilité et la sécurité de base.](create-device-security-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2e2f8-113">To do this, follow the steps in [Create device security policies in basic mobility and security](create-device-security-policies.md).</span></span>
    
- <span data-ttu-id="2e2f8-114">**Si vous souhaitez connaître l'expérience** utilisateur lorsque vous effacez son appareil, voir   [quel est l'impact sur l'utilisateur et l'appareil ?](#whats-the-user-and-device-impact)</span><span class="sxs-lookup"><span data-stu-id="2e2f8-114">**If you want to know the user experience** when you wipe their device, see  [What's the user and device impact?](#whats-the-user-and-device-impact).</span></span>

## <a name="wipe-a-mobile-device"></a><span data-ttu-id="2e2f8-115">Effacer un appareil mobile</span><span class="sxs-lookup"><span data-stu-id="2e2f8-115">Wipe a mobile device</span></span>

1. <span data-ttu-id="2e2f8-116">Go to the [Microsoft 365 admin center](../../admin/admin-overview/about-the-admin-center.md).</span><span class="sxs-lookup"><span data-stu-id="2e2f8-116">Go to the [Microsoft 365 admin center](../../admin/admin-overview/about-the-admin-center.md).</span></span>

2. <span data-ttu-id="2e2f8-117">Tapez Gestion des appareils mobiles dans le champ de recherche, puis sélectionnez **Gestion des** périphériques mobiles dans la liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-117">Type Mobile Device Management into the search field, and select **Mobile Device Management** from the list of results.</span></span>

    :::image type="content" source="../../media/basic-mobility-security/bms-6-mobile-device-management-option.png" alt-text="Option de gestion des appareils mobiles Basic Mobility and Secruity":::

3. <span data-ttu-id="2e2f8-119">Sélectionnez **Gérer les appareils.**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-119">Select **Manage devices**.</span></span>

4. <span data-ttu-id="2e2f8-120">Sélectionnez l’appareil que vous voulez réinitialiser.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-120">Select the device you want to wipe.</span></span>

5. <span data-ttu-id="2e2f8-121">Sélectionnez **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-121">Select **Manage**.</span></span>

6. <span data-ttu-id="2e2f8-122">Sélectionnez le type de réinitialisation à distance que vous voulez effectuer.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-122">Select the type of remote wipe you want to do.</span></span>

    - <span data-ttu-id="2e2f8-123">Pour réinitialiser entièrement l'appareil et restaurer ses paramètres d'usine, sélectionnez **Réinitialiser aux paramètres d'usine.**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-123">To do a full wipe and restore the device to its factory settings, select **Factory reset**.</span></span>
    - <span data-ttu-id="2e2f8-124">Pour effacer et supprimer uniquement les informations de l'organisation Microsoft 365, sélectionnez **Supprimer les données de l'entreprise.**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-124">To do a selective wipe and delete only Microsoft 365 organization information, select **Remove company data**.</span></span>
    - <span data-ttu-id="2e2f8-125">Pour supprimer l'appareil de votre organisation, **sélectionnez Supprimer l'appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-125">To remove the device from your organization, select **Remove device**.</span></span>

7. <span data-ttu-id="2e2f8-126">Cliquez sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-126">Select **Yes** to confirm.</span></span>

## <a name="how-do-i-know-it-worked"></a><span data-ttu-id="2e2f8-127">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="2e2f8-127">How do I know it worked?</span></span>

<span data-ttu-id="2e2f8-128">L'appareil mobile ne figure plus dans la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-128">You no longer see the mobile device in the list of managed devices.</span></span>

## <a name="why-would-you-want-to-wipe-a-device"></a><span data-ttu-id="2e2f8-129">Pourquoi voulez-vous effacer un appareil ?</span><span class="sxs-lookup"><span data-stu-id="2e2f8-129">Why would you want to wipe a device?</span></span>

<span data-ttu-id="2e2f8-130">Effacez un appareil pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="2e2f8-130">Wipe a device for these reasons:</span></span>

- <span data-ttu-id="2e2f8-131">Les appareils mobiles tels que les smartphones et les tablettes sont toujours plus complets.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-131">Mobile devices like smartphones and tablets are becoming more full-featured all the time.</span></span> <span data-ttu-id="2e2f8-132">Cela signifie qu'il est plus facile pour vos utilisateurs de stocker des informations d'entreprise sensibles, telles que des informations d'identification personnelle ou des communications confidentielles, et d'y accéder en libre-service.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-132">This means it’s easier for your users to store sensitive corporate information such as personal identification or confidential communications and access it on the go.</span></span> <span data-ttu-id="2e2f8-133">Si l'un de ces appareils mobiles est perdu ou volé, la wiping de l'appareil peut aider à empêcher que les informations de votre organisation ne se terminent entre de mauvaises mains.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-133">If one of these mobile devices is lost or stolen, wiping the device can help prevent your organization’s information from ending up in the wrong hands.</span></span>
- <span data-ttu-id="2e2f8-134">Lorsqu'un utilisateur quitte l'organisation avec un appareil personnel inscrit à Basic Mobility and Security, vous pouvez empêcher les informations organisationnelles de passer avec cet utilisateur en réinitialisation d'usine.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-134">When a user leaves the organization with a personal device that is enrolled in Basic Mobility and Security, you can help prevent organizational information from going with that user by performing a factory reset.</span></span>
- <span data-ttu-id="2e2f8-135">Si votre organisation fournit des appareils mobiles aux utilisateurs, vous devrez peut-être réaffecter des appareils de temps à autre.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-135">If your organization provides mobile devices to users, you might need to reassign devices from time to time.</span></span> <span data-ttu-id="2e2f8-136">La réinitialisation d'usine sur un appareil avant de l'affecter à un nouvel utilisateur permet de s'assurer que toutes les informations sensibles du propriétaire précédent sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-136">Doing a Factory Reset on a device before assigning it to a new user helps ensures that any sensitive information from the previous owner is deleted.</span></span>

## <a name="whats-the-user-and-device-impact"></a><span data-ttu-id="2e2f8-137">Quel est l'impact sur l'utilisateur et l'appareil ?</span><span class="sxs-lookup"><span data-stu-id="2e2f8-137">What's the user and device impact?</span></span>

<span data-ttu-id="2e2f8-138">La effacement est envoyée immédiatement à l'appareil mobile et l'appareil est marqué comme non conforme dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-138">The wipe is sent immediately to the mobile device and the device is marked as not compliant in Azure active directory.</span></span> <span data-ttu-id="2e2f8-139">Bien que toutes les données sont supprimées lorsqu'un appareil est réinitialisé aux paramètres d'usine par défaut, le tableau suivant décrit le contenu supprimé pour chaque type d'appareil lorsqu'un appareil est supprimé lorsque vous supprimez des données d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-139">While all data is removed when a device is reset to factory defaults, the following table describes what content is removed for each device type when a device when you remove company data.</span></span>

|<span data-ttu-id="2e2f8-140">**Impact sur le contenu**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-140">**Content impact**</span></span>|<span data-ttu-id="2e2f8-141">**iOS 10 et les ultérieures**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-141">**iOS 10 and later**</span></span>|<span data-ttu-id="2e2f8-142">**Android 5 et version ultérieure**</span><span class="sxs-lookup"><span data-stu-id="2e2f8-142">**Android 5 and later**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e2f8-143">Les données d'application Microsoft 365 sont effacées si l'appareil est protégé par les stratégies Intune App Protection.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-143">Microsoft 365 app data is wiped if the device is protected by Intune App Protection policies.</span></span> <span data-ttu-id="2e2f8-144">Les applications ne sont pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-144">The apps aren't removed.</span></span> <span data-ttu-id="2e2f8-145">Pour les appareils non protégés par les stratégies de gestion des applications mobiles (MAM), Outlook et OneDrive ne suppriment pas les données mises en cache.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-145">For devices not protected by Mobile Application Management (MAM) policies, Outlook and OneDrive won't remove cached data.</span></span><br/><span data-ttu-id="2e2f8-146">**Remarque** Pour appliquer des stratégies intune App Protection, vous devez avoir une licence Intune.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-146">**Note** For applying Intune App protection policies you must have an Intune license.</span></span>|<span data-ttu-id="2e2f8-147">Oui</span><span class="sxs-lookup"><span data-stu-id="2e2f8-147">Yes</span></span>|<span data-ttu-id="2e2f8-148">Oui</span><span class="sxs-lookup"><span data-stu-id="2e2f8-148">Yes</span></span>|
|<span data-ttu-id="2e2f8-149">Les paramètres de stratégie appliqués par Basic Mobility and Security aux appareils ne sont plus appliqués ; les utilisateurs peuvent modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-149">Policy settings applied by Basic Mobility and Security to devices are no longer enforced; users can change the settings.</span></span>|<span data-ttu-id="2e2f8-150">Oui</span><span class="sxs-lookup"><span data-stu-id="2e2f8-150">Yes</span></span>|<span data-ttu-id="2e2f8-151">Oui</span><span class="sxs-lookup"><span data-stu-id="2e2f8-151">Yes</span></span>|
|<span data-ttu-id="2e2f8-152">Les profils de messagerie créés par Basic Mobility and Security sont supprimés et les messages électroniques mis en cache sur l'appareil sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-152">Email profiles created by Basic Mobility and Security are removed and cached email on the device is deleted.</span></span>|<span data-ttu-id="2e2f8-153">Oui</span><span class="sxs-lookup"><span data-stu-id="2e2f8-153">Yes</span></span>|<span data-ttu-id="2e2f8-154">N/D</span><span class="sxs-lookup"><span data-stu-id="2e2f8-154">N/A</span></span>|
>[!NOTE]
><span data-ttu-id="2e2f8-155">L'application Portail d'entreprise est disponible dans l'App Store pour iOS et le Play Store pour les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="2e2f8-155">Company Portal app is available at the App Store for iOS and the Play Store for Android devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e2f8-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2f8-156">Related topics</span></span>

[<span data-ttu-id="2e2f8-157">Configurer Mobility + Security</span><span class="sxs-lookup"><span data-stu-id="2e2f8-157">Set up Basic Mobility and Security</span></span>](set-up.md)
