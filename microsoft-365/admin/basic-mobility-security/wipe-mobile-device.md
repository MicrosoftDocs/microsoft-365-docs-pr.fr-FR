---
title: Réinitialiser un appareil mobile dans la sécurité et la mobilité de base
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
description: Utilisez la sécurité et la mobilité de base intégrées pour supprimer les informations des périphériques.
ms.openlocfilehash: 4627b0cb2d0963ae724c425a6a7ea6279f271856
ms.sourcegitcommit: aeb94601a81db3ead8610c2f36cff30eb9fe10e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "47429949"
---
# <a name="wipe-a-mobile-device-in-basic-mobility-and-security"></a><span data-ttu-id="e6312-103">Réinitialiser un appareil mobile dans la sécurité et la mobilité de base</span><span class="sxs-lookup"><span data-stu-id="e6312-103">Wipe a mobile device in Basic Mobility and Security</span></span>

<span data-ttu-id="e6312-104">Vous pouvez utiliser la mobilité et la sécurité de base intégrées pour Microsoft 365 pour supprimer uniquement les informations organisationnelles, ou pour effectuer une réinitialisation en usine afin de supprimer toutes les informations d’un appareil mobile et de les restaurer aux paramètres d’usine.</span><span class="sxs-lookup"><span data-stu-id="e6312-104">You can use built-in Basic Mobility and Security for Microsoft 365 to remove only organizational information, or to perform a factory reset to delete all information from a mobile device and restore it to factory settings.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e6312-105">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e6312-105">Before you begin</span></span>

<span data-ttu-id="e6312-106">Les appareils mobiles peuvent stocker des informations organisationnelles sensibles et fournir un accès aux ressources Microsoft 365 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e6312-106">Mobile devices can store sensitive organizational information and provide access to your organization's Microsoft 365 resources.</span></span> <span data-ttu-id="e6312-107">Pour vous aider à protéger les informations de votre organisation, vous pouvez procéder à la réinitialisation ou à la suppression des données d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="e6312-107">To help protect your organization's information, you can do Factory reset or Remove company data:</span></span>
    
- <span data-ttu-id="e6312-108">**Réinitialisation en usine**: supprime toutes les données sur l’appareil mobile d’un utilisateur, y compris les applications installées, les photos et les informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="e6312-108">**Factory reset**: Deletes all data on a user's mobile device, including installed applications, photos, and personal information.</span></span> <span data-ttu-id="e6312-109">Une fois la réinitialisation terminée, l’appareil est restauré à ses paramètres d’usine.</span><span class="sxs-lookup"><span data-stu-id="e6312-109">When the wipe is complete, the device is restored to its factory settings.</span></span>
    
- <span data-ttu-id="e6312-110">**Supprimer les données**de l’entreprise : supprime uniquement les données de l’organisation et laisse les applications, les photos et les informations personnelles installées sur l’appareil mobile d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6312-110">**Remove company data**: Removes only organization data and leaves installed applications, photos, and personal information on a user's mobile device.</span></span>   

- <span data-ttu-id="e6312-111">**Lorsqu’un appareil est effacé (réinitialisation ou suppression des données d’entreprise)**, l’appareil est supprimé de la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="e6312-111">**When a device is wiped (Factory Reset or Remove Company Data)**, the device is removed from the list of managed devices.</span></span>
    
- <span data-ttu-id="e6312-112">**Réinitialiser un appareil automatiquement**: vous pouvez configurer une stratégie de sécurité et de mobilité de base qui réinitialise automatiquement un appareil une fois que l’utilisateur n’a pas tenté d’entrer le mot de passe d’appareil un certain nombre de fois.</span><span class="sxs-lookup"><span data-stu-id="e6312-112">**Automatically reset a device**: You can set up a Basic Mobility and Security policy that automatically factory resets a device after the user unsuccessfully tries to enter the device password a specific number of times.</span></span> <span data-ttu-id="e6312-113">Pour ce faire, suivez les étapes décrites dans [Create Device Security Policies in Basic Mobility and Security](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e6312-113">To do this, follow the steps in [Create device security policies in basic mobility and security](create-device-security-policies.md).</span></span>
    
- <span data-ttu-id="e6312-114">**Si vous souhaitez connaître l’expérience utilisateur lors de la** réinitialisation de son appareil, consultez  [la rubrique quel est l’impact sur les utilisateurs et les appareils ?](#whats-the-user-and-device-impact).</span><span class="sxs-lookup"><span data-stu-id="e6312-114">**If you want to know the user experience** when you wipe their device, see  [What's the user and device impact?](#whats-the-user-and-device-impact).</span></span>   

## <a name="wipe-a-mobile-device"></a><span data-ttu-id="e6312-115">Réinitialiser un appareil mobile</span><span class="sxs-lookup"><span data-stu-id="e6312-115">Wipe a mobile device</span></span>

1. <span data-ttu-id="e6312-116">Accédez au [Centre d’administration Microsoft 365](https://support.microsoft.com/office/758befc4-0888-4009-9f14-0d147402fd23).</span><span class="sxs-lookup"><span data-stu-id="e6312-116">Go to the [Microsoft 365 admin center](https://support.microsoft.com/office/758befc4-0888-4009-9f14-0d147402fd23).</span></span>
    
2. <span data-ttu-id="e6312-117">Tapez gestion des appareils mobiles dans le champ de recherche, puis sélectionnez **gestion des appareils mobiles** dans la liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="e6312-117">Type Mobile Device Management into the search field, and select **Mobile Device Management** from the list of results.</span></span> 

    :::image type="content" source="../../media/basic-mobility-security/bms-6-mobile-device-management-option.png" alt-text="Option de gestion de l’appareil mobile secruity et de la mobilité de base":::

3. <span data-ttu-id="e6312-119">Sélectionnez **gérer les appareils**.</span><span class="sxs-lookup"><span data-stu-id="e6312-119">Select **Manage devices**.</span></span>

4. <span data-ttu-id="e6312-120">Sélectionnez l’appareil que vous voulez réinitialiser.</span><span class="sxs-lookup"><span data-stu-id="e6312-120">Select the device you want to wipe.</span></span>

5. <span data-ttu-id="e6312-121">Sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="e6312-121">Select **Manage**.</span></span>

6. <span data-ttu-id="e6312-122">Sélectionnez le type de réinitialisation à distance que vous voulez effectuer.</span><span class="sxs-lookup"><span data-stu-id="e6312-122">Select the type of remote wipe you want to do.</span></span>

    - <span data-ttu-id="e6312-123">Pour effectuer un nettoyage complet et restaurer les paramètres d’usine de l’appareil, sélectionnez **réinitialisation usine**.</span><span class="sxs-lookup"><span data-stu-id="e6312-123">To do a full wipe and restore the device to its factory settings, select **Factory reset**.</span></span>
    - <span data-ttu-id="e6312-124">Pour effectuer une réinitialisation sélective et supprimer uniquement les informations de l’organisation Microsoft 365, sélectionnez **Supprimer les données**de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e6312-124">To do a selective wipe and delete only Microsoft 365 organization information, select **Remove company data**.</span></span>
    - <span data-ttu-id="e6312-125">Pour supprimer l’appareil de votre organisation, sélectionnez **Supprimer l’appareil**.</span><span class="sxs-lookup"><span data-stu-id="e6312-125">To remove the device from your organization, select **Remove device**.</span></span>

7. <span data-ttu-id="e6312-126">Cliquez sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="e6312-126">Select **Yes** to confirm.</span></span>

## <a name="how-do-i-know-it-worked"></a><span data-ttu-id="e6312-127">Comment puis-je savoir si elle a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="e6312-127">How do I know it worked?</span></span>

<span data-ttu-id="e6312-128">L’appareil mobile n’apparaît plus dans la liste des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="e6312-128">You no longer see the mobile device in the list of managed devices.</span></span>

## <a name="why-would-you-want-to-wipe-a-device"></a><span data-ttu-id="e6312-129">Pourquoi effacer un appareil ?</span><span class="sxs-lookup"><span data-stu-id="e6312-129">Why would you want to wipe a device?</span></span>

<span data-ttu-id="e6312-130">Réinitialiser un appareil pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6312-130">Wipe a device for these reasons:</span></span>

- <span data-ttu-id="e6312-131">Les appareils mobiles tels que les smartphones et les tablettes sont de plus en plus complets.</span><span class="sxs-lookup"><span data-stu-id="e6312-131">Mobile devices like smartphones and tablets are becoming more full-featured all the time.</span></span> <span data-ttu-id="e6312-132">Cela signifie qu’il est plus facile pour vos utilisateurs de stocker des informations d’entreprise sensibles, telles que des communications personnelles ou confidentielles, et d’y accéder dès que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="e6312-132">This means it’s easier for your users to store sensitive corporate information such as personal identification or confidential communications and access it on the go.</span></span> <span data-ttu-id="e6312-133">Si l’un de ces appareils mobiles est perdu ou volé, l’effacement de l’appareil peut empêcher les informations de votre organisation de se terminer de façon incorrecte.</span><span class="sxs-lookup"><span data-stu-id="e6312-133">If one of these mobile devices is lost or stolen, wiping the device can help prevent your organization’s information from ending up in the wrong hands.</span></span>
- <span data-ttu-id="e6312-134">Lorsqu’un utilisateur quitte l’organisation à l’aide d’un appareil personnel qui est intégré à la mobilité et à la sécurité de base, vous pouvez empêcher les informations organisationnelles de passer à cet utilisateur en effectuant une réinitialisation d’usine.</span><span class="sxs-lookup"><span data-stu-id="e6312-134">When a user leaves the organization with a personal device that is enrolled in Basic Mobility and Security, you can help prevent organizational information from going with that user by performing a factory reset.</span></span>
- <span data-ttu-id="e6312-135">Si votre organisation fournit des appareils mobiles aux utilisateurs, vous devrez peut-être réaffecter des appareils de temps à autre.</span><span class="sxs-lookup"><span data-stu-id="e6312-135">If your organization provides mobile devices to users, you might need to reassign devices from time to time.</span></span> <span data-ttu-id="e6312-136">La réinitialisation d’une usine sur un appareil avant de l’affecter à un nouvel utilisateur permet de s’assurer que toutes les informations sensibles du propriétaire précédent sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="e6312-136">Doing a Factory Reset on a device before assigning it to a new user helps ensures that any sensitive information from the previous owner is deleted.</span></span>

## <a name="whats-the-user-and-device-impact"></a><span data-ttu-id="e6312-137">Quel est l’impact sur les utilisateurs et les appareils ?</span><span class="sxs-lookup"><span data-stu-id="e6312-137">What's the user and device impact?</span></span>

<span data-ttu-id="e6312-138">La réinitialisation est envoyée immédiatement à l’appareil mobile et l’appareil est marqué comme non conforme dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e6312-138">The wipe is sent immediately to the mobile device and the device is marked as not compliant in Azure active directory.</span></span> <span data-ttu-id="e6312-139">Tandis que toutes les données sont supprimées lorsqu’un appareil est réinitialisé aux valeurs par défaut d’origine, le tableau suivant décrit le contenu qui est supprimé pour chaque type d’appareil lorsque vous supprimez des données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e6312-139">While all data is removed when a device is reset to factory defaults, the following table describes what content is removed for each device type when a device when you remove company data.</span></span>

|<span data-ttu-id="e6312-140">**Impacer le contenu**</span><span class="sxs-lookup"><span data-stu-id="e6312-140">**Content impace**</span></span>|<span data-ttu-id="e6312-141">**iOS 10 et versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="e6312-141">**iOS 10 and later**</span></span>|<span data-ttu-id="e6312-142">**Android 5 et versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="e6312-142">**Android 5 and later**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6312-143">Les données de l’application Microsoft 365 sont effacées si l’appareil est protégé par les stratégies Intune App protection.</span><span class="sxs-lookup"><span data-stu-id="e6312-143">Microsoft 365 app data is wiped if the device is protected by Intune App Protection policies.</span></span> <span data-ttu-id="e6312-144">Les applications ne sont pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="e6312-144">The apps aren't removed.</span></span> <span data-ttu-id="e6312-145">Pour les appareils qui ne sont pas protégés par les stratégies de gestion des applications mobiles (MAM), Outlook et OneDrive ne supprimeront pas les données mises en cache.</span><span class="sxs-lookup"><span data-stu-id="e6312-145">For devices not protected by Mobile Application Management (MAM) policies, Outlook and OneDrive won't remove cached data.</span></span><br/><span data-ttu-id="e6312-146">**Note** Pour appliquer les stratégies de protection des applications Intune, vous devez disposer d’une licence Intune.</span><span class="sxs-lookup"><span data-stu-id="e6312-146">**Note** For applying Intune App protection policies you must have an Intune license.</span></span>|<span data-ttu-id="e6312-147">Oui</span><span class="sxs-lookup"><span data-stu-id="e6312-147">Yes</span></span>|<span data-ttu-id="e6312-148">Oui</span><span class="sxs-lookup"><span data-stu-id="e6312-148">Yes</span></span>|
|<span data-ttu-id="e6312-149">Les paramètres de stratégie appliqués par la sécurité et la mobilité de base aux appareils ne sont plus appliqués ; les utilisateurs peuvent modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e6312-149">Policy settings applied by Basic Mobility and Security to devices are no longer enforced; users can change the settings.</span></span>|<span data-ttu-id="e6312-150">Oui</span><span class="sxs-lookup"><span data-stu-id="e6312-150">Yes</span></span>|<span data-ttu-id="e6312-151">Oui</span><span class="sxs-lookup"><span data-stu-id="e6312-151">Yes</span></span>|
|<span data-ttu-id="e6312-152">Les profils de messagerie créés par la mobilité et la sécurité de base sont supprimés et le courrier mis en cache sur l’appareil est supprimé.</span><span class="sxs-lookup"><span data-stu-id="e6312-152">Email profiles created by Basic Mobility and Security are removed and cached email on the device is deleted.</span></span>|<span data-ttu-id="e6312-153">Oui</span><span class="sxs-lookup"><span data-stu-id="e6312-153">Yes</span></span>|<span data-ttu-id="e6312-154">N/D</span><span class="sxs-lookup"><span data-stu-id="e6312-154">N/A</span></span>|
>[!NOTE] 
><span data-ttu-id="e6312-155">L’application portail d’entreprise est disponible dans le magasin d’applications pour iOS et le magasin de jeux pour les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="e6312-155">Company Portal app is available at the App Store for iOS and the Play Store for Android devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6312-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6312-156">Related topics</span></span>

[<span data-ttu-id="e6312-157">Configurer Mobility + Security</span><span class="sxs-lookup"><span data-stu-id="e6312-157">Set up Basic Mobility and Security</span></span>](set-up.md)