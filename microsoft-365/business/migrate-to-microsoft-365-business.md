---
title: Mettre à niveau vers Microsoft 365 Business Premium à partir de Microsoft 365 Business Standard
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: 5b4ba843-24b8-4526-8e1f-f9b9eab89d06
description: Découvrez la différence entre Microsoft 365 Business Standard et Microsoft 365 Business Premium et comment vous pouvez mettre à niveau vers Microsoft 365 Business Premium.
ms.openlocfilehash: 0968b877820590987f6f3ceca3efbd106b62cbd1
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52705487"
---
# <a name="upgrade-to-microsoft-365-business-premium-from-microsoft-365-business-standard"></a><span data-ttu-id="a31cd-103">Mettre à niveau vers Microsoft 365 Business Premium à partir de Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="a31cd-103">Upgrade to Microsoft 365 Business Premium from Microsoft 365 Business Standard</span></span>

<span data-ttu-id="a31cd-104">Si vous avez un abonnement [Microsoft 365](https://products.office.com/compare-all-microsoft-office-products-4-column?activetab=tab:primaryr2)entreprise, par exemple, Microsoft 365 Business Standard, vous pouvez facilement mettre à niveau Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="a31cd-104">If you have a [Microsoft 365 for business subscription](https://products.office.com/compare-all-microsoft-office-products-4-column?activetab=tab:primaryr2), for example, Microsoft 365 Business Standard, you can easily upgrade to Microsoft 365 Business Premium.</span></span> <span data-ttu-id="a31cd-105">Mise à niveau vers Microsoft 365 Business Premium si vous souhaitez ajouter :</span><span class="sxs-lookup"><span data-stu-id="a31cd-105">Upgrade to Microsoft 365 Business Premium if you want to add:</span></span>

- <span data-ttu-id="a31cd-106">Windows 10 Professionnel (sur les PC qui s’exécutent Windows 8 ou une ultérieure)</span><span class="sxs-lookup"><span data-stu-id="a31cd-106">Windows 10 Pro (to PCs running Windows 8 or later)</span></span>

- <span data-ttu-id="a31cd-107">Contrôles simples qui gèrent les données métiers sur les appareils</span><span class="sxs-lookup"><span data-stu-id="a31cd-107">Simple controls that manage business data on devices</span></span>

- <span data-ttu-id="a31cd-108">Fonctionnalités de sécurité avancées.</span><span class="sxs-lookup"><span data-stu-id="a31cd-108">Advanced security capabilities.</span></span>
<span data-ttu-id="a31cd-109">Pour en savoir plus sur les Microsoft 365 Business Premium, [Microsoft.com](https://www.microsoft.com/microsoft-365/business)</span><span class="sxs-lookup"><span data-stu-id="a31cd-109">Find out more about Microsoft 365 Business Premium at [Microsoft.com](https://www.microsoft.com/microsoft-365/business)</span></span>

## <a name="whats-the-difference-between-microsoft-365-business-standard-and-microsoft-365-business-premium"></a><span data-ttu-id="a31cd-110">Quelle est la différence entre Microsoft 365 Business Standard et Microsoft 365 Business Premium ?</span><span class="sxs-lookup"><span data-stu-id="a31cd-110">What's the difference between Microsoft 365 Business Standard and Microsoft 365 Business Premium?</span></span>

<span data-ttu-id="a31cd-111">Nous avons ajouté une comparaison côte à côte de ces deux plans à la description Microsoft 365 Business Premium [service.](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-business-service-description)</span><span class="sxs-lookup"><span data-stu-id="a31cd-111">We've added a side-by-side comparison of these two plans to the [Microsoft 365 Business Premium Service Description](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-business-service-description).</span></span> 

## <a name="before-you-begin"></a><span data-ttu-id="a31cd-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a31cd-112">Before you begin</span></span>

- <span data-ttu-id="a31cd-113">**Quand choisir de mettre à niveau ?**</span><span class="sxs-lookup"><span data-stu-id="a31cd-113">**When should I choose to upgrade?**</span></span> <span data-ttu-id="a31cd-114">La mise à niveau est le bon choix lorsque vous souhaitez mettre à niveau **tous les utilisateurs** affectés à un plan unique.</span><span class="sxs-lookup"><span data-stu-id="a31cd-114">Upgrade is the right choice when you want to upgrade **all users** assigned to a single plan.</span></span> <span data-ttu-id="a31cd-115">Lorsque vous choisissez la mise à niveau, tous les utilisateurs du plan basculent vers un autre plan en même temps.</span><span class="sxs-lookup"><span data-stu-id="a31cd-115">When you choose upgrade, all plan users get switched to another plan at the same time.</span></span> <span data-ttu-id="a31cd-116">Si vous ne souhaitez pas mettre à niveau toutes les personnes affectées à un plan unique, achetez des licences pour la nouvelle offre (dans ce cas Microsoft 365 Business Premium) et attribuez ces [licences](../admin/manage/assign-licenses-to-users.md) individuellement à chaque utilisateur que vous souhaitez mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="a31cd-116">If you don't want to upgrade everyone assigned to a single plan, buy licenses for the new plan (in this case Microsoft 365 Business Premium), and [assign those licenses individually](../admin/manage/assign-licenses-to-users.md) to each user that you want to upgrade.</span></span>

- <span data-ttu-id="a31cd-117">**Certains modules peuvent empêcher la mise à niveau** Si vous essayez de démarrer une mise à niveau et que vous avez un module qui vous empêche de continuer, vous pouvez d’abord supprimer le module, puis l’ajouter ultérieurement si vous en avez encore besoin.</span><span class="sxs-lookup"><span data-stu-id="a31cd-117">**Some add-ons might prevent the upgrade** If you try to start an upgrade and you have an add-on that prevents you from continuing, you can remove the add-on first, and then add it back later if you still need it.</span></span>

- <span data-ttu-id="a31cd-118">**Si vous avez prépayé votre offre** Il n’existe pas de chemin de mise à niveau simple pour les plans prépayés.</span><span class="sxs-lookup"><span data-stu-id="a31cd-118">**If you prepaid your plan** There isn't a straightforward upgrade path for prepaid plans.</span></span> <span data-ttu-id="a31cd-119">Vous savez si vous avez une offre prépayée, car vous la définissez à l’aide d’un ID produit que vous avez peut-être acheté dans un magasin.</span><span class="sxs-lookup"><span data-stu-id="a31cd-119">You'll know if you have a prepaid plan because you set up your plan using a product ID that you might have purchased in a store.</span></span> <span data-ttu-id="a31cd-120">Contactez un partenaire, Microsoft Store ou attendez l’expiration de votre plan prépayé pour basculer vers une nouvelle offre.</span><span class="sxs-lookup"><span data-stu-id="a31cd-120">Contact a partner, go to the Microsoft Store, or wait until your prepaid plan expires to switch to a new plan.</span></span>

## <a name="upgrade-to-microsoft-365-business-premium"></a><span data-ttu-id="a31cd-121">Mise à niveau vers Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="a31cd-121">Upgrade to Microsoft 365 Business Premium</span></span>

1. <span data-ttu-id="a31cd-122">Connectez-vous au Centre d’administration à <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> l’adresse .</span><span class="sxs-lookup"><span data-stu-id="a31cd-122">Sign into the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="a31cd-123">Go to the navigation pane and select **Billing** \> **Your products**.</span><span class="sxs-lookup"><span data-stu-id="a31cd-123">Go to the navigation pane and select **Billing** \> **Your products**.</span></span> <span data-ttu-id="a31cd-124">Recherchez votre abonnement actuel et sélectionnez-le pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="a31cd-124">Find your current subscription and select it to view the details.</span></span>

3. <span data-ttu-id="a31cd-125">Sur la page suivante, sélectionnez **Mettre à niveau.**</span><span class="sxs-lookup"><span data-stu-id="a31cd-125">On the next page, select **Upgrade**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="a31cd-126">Si vous voyez un message qui indique que la mise à niveau de votre abonnement n’est pas prise en charge avec la gestion des licences basée sur les groupes dans **Azure Active Directory,** vous pouvez l’ignorer en toute sécurité, sauf si vous avez une organisation très importante.</span><span class="sxs-lookup"><span data-stu-id="a31cd-126">If you see a message that says **Upgrading your subscription is not supported with group-based licensing in Azure Active Directory**, you can safely ignore this unless you have a very large organization.</span></span> <span data-ttu-id="a31cd-127">Les organisations qui ont sélectionné cette option savent qu’elles utilisent des licences basées sur des groupes.</span><span class="sxs-lookup"><span data-stu-id="a31cd-127">Organizations who have selected this option will be aware that they're using group-based licensing.</span></span>

4. <span data-ttu-id="a31cd-128">Ensuite, vous pouvez afficher la liste des plans vers qui vous pouvez mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="a31cd-128">Next, you can view a list of plans that you can upgrade to.</span></span> <span data-ttu-id="a31cd-129">Dans ce cas, recherchez l’Microsoft 365 Business Premium plan.</span><span class="sxs-lookup"><span data-stu-id="a31cd-129">In this case, find the Microsoft 365 Business Premium plan.</span></span> <span data-ttu-id="a31cd-130">Vous pouvez faire défiler vers le bas si vous souhaitez voir toutes les applications et services inclus dans ce plan.</span><span class="sxs-lookup"><span data-stu-id="a31cd-130">You can scroll down if you want to see all the apps and services that are included with this plan.</span></span> <span data-ttu-id="a31cd-131">Sous **Microsoft 365 Business Premium,** **sélectionnez Mettre à** niveau pour ajouter Microsoft 365 Business Premium à votre panier.</span><span class="sxs-lookup"><span data-stu-id="a31cd-131">Under **Microsoft 365 Business Premium**, select **Upgrade** to add Microsoft 365 Business Premium to your cart.</span></span>

5. <span data-ttu-id="a31cd-132">Dans le panier :</span><span class="sxs-lookup"><span data-stu-id="a31cd-132">In the cart:</span></span>

    1. <span data-ttu-id="a31cd-133">Nous inclurons automatiquement des licences pour tous vos utilisateurs actuels.</span><span class="sxs-lookup"><span data-stu-id="a31cd-133">We'll automatically include licenses for all your current users.</span></span> <span data-ttu-id="a31cd-134">Si vous avez besoin de plus ou moins de licences, vous devez acheter et [attribuer ces licences individuellement.](../admin/manage/assign-licenses-to-users.md)</span><span class="sxs-lookup"><span data-stu-id="a31cd-134">If you need more or fewer licenses, you need to [buy and assign those licenses individually](../admin/manage/assign-licenses-to-users.md).</span></span>  
    2. <span data-ttu-id="a31cd-135">Vous pouvez ajuster la façon dont vous souhaitez payer : mensuelle ou annuel.</span><span class="sxs-lookup"><span data-stu-id="a31cd-135">You can adjust how you'd like to pay: monthly or yearly.</span></span> <span data-ttu-id="a31cd-136">Sélectionnez le menu déroulant pour effectuer votre choix.</span><span class="sxs-lookup"><span data-stu-id="a31cd-136">Select the drop-down menu to make your choice.</span></span>

6. <span data-ttu-id="a31cd-137">Sélectionnez **Go to Checkout** où vous verrez un résumé de votre achat, y compris le mode de paiement de ce compte.</span><span class="sxs-lookup"><span data-stu-id="a31cd-137">Select **Go to Checkout** where you'll see a summary of your purchase, including the payment method for this account.</span></span> <span data-ttu-id="a31cd-138">Vous pouvez également ajouter un code promotionnel ici si vous en avez un.</span><span class="sxs-lookup"><span data-stu-id="a31cd-138">You can also add a promo code here if you have one.</span></span>

7. <span data-ttu-id="a31cd-139">Select **Place order** to complete your purchase.</span><span class="sxs-lookup"><span data-stu-id="a31cd-139">Select **Place order** to complete your purchase.</span></span>\
<span data-ttu-id="a31cd-140">La mise en place de vos nouvelles plans de service prend quelques minutes à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a31cd-140">It takes Microsoft a few minutes to set up your new service plans.</span></span> <span data-ttu-id="a31cd-141">Pour vérifier la progression, sélectionnez **Vérifier l’état de la mise à niveau.**</span><span class="sxs-lookup"><span data-stu-id="a31cd-141">To check on progress, select **Check upgrade status**.</span></span>

8. <span data-ttu-id="a31cd-142">Lorsque votre plan est prêt, vous devrez peut-être effectuer quelques étapes de configuration supplémentaires dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="a31cd-142">When your plan is ready, you might need to complete some additional setup steps in the admin center.</span></span> <span data-ttu-id="a31cd-143">Dans le volet de navigation, sélectionnez **Accueil** pour effectuer les étapes de configuration supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a31cd-143">In the navigation pane, select **Home** to complete any additional setup steps.</span></span>

> [!NOTE]
> <span data-ttu-id="a31cd-144">Vous recevrez un remboursement au prorat pour les licences Microsoft 365 dont vous n’avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="a31cd-144">You'll receive a prorated refund for the Microsoft 365 licenses that you no longer need.</span></span> <span data-ttu-id="a31cd-145">Votre compte bancaire ou carte bancaire sera facturé environ deux jours après la mise en place de la nouvelle plan.</span><span class="sxs-lookup"><span data-stu-id="a31cd-145">Your bank account or credit card will be charged about two days after you set up the new plan.</span></span>
  
## <a name="protect-user-devices-and-files"></a><span data-ttu-id="a31cd-146">Protéger les appareils et les fichiers des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a31cd-146">Protect user devices and files</span></span>

<span data-ttu-id="a31cd-147">Maintenant que Microsoft 365 Business Premium licences sont attribuées, vous devez effectuer les étapes nécessaires pour commencer à protéger les appareils et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a31cd-147">Now that Microsoft 365 Business Premium licenses have been assigned, complete steps to start protecting devices and files.</span></span> <span data-ttu-id="a31cd-148">Vous utiliserez de nouvelles options incluses dans le volet de navigation du Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="a31cd-148">You'll use some new options included in the admin center navigation pane.</span></span>
  
1. <span data-ttu-id="a31cd-149">Dans le centre d’administration, dans le volet de navigation, allez à **Stratégies des** \> **appareils.**</span><span class="sxs-lookup"><span data-stu-id="a31cd-149">In the admin center, in the navigation pane, go to **Devices** \> **Policies**.</span></span>

2. <span data-ttu-id="a31cd-150">Dans la page **Stratégies d’appareil,** **sélectionnez Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="a31cd-150">On the **Device policies** page, select **Add**.</span></span>

3. <span data-ttu-id="a31cd-151">Dans le **volet Ajouter** une stratégie, donnez un nom à la stratégie (par exemple, Protéger les fichiers de travail), puis choisissez un **type** de stratégie dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="a31cd-151">In the **Add policy** pane give the policy a name (for example, Protect work files), and then choose a **Policy type** from the drop-down list.</span></span>

    <span data-ttu-id="a31cd-152">Vous pouvez configurer des stratégies d’application pour la protection des fichiers sur les appareils Android et iPhone, ainsi que des Windows 10, et vous pouvez configurer des stratégies de configuration d’appareil pour les appareils Windows 10 entreprise.</span><span class="sxs-lookup"><span data-stu-id="a31cd-152">You can set up application policies for protecting files on Android and iPhone devices, as well as Windows 10, and you can set up device configuration policies for company owned Windows 10 devices.</span></span> <span data-ttu-id="a31cd-153">Pour plus d’informations, voir les liens suivants :</span><span class="sxs-lookup"><span data-stu-id="a31cd-153">See the following links for details:</span></span>

    - [<span data-ttu-id="a31cd-154">Définir les paramètres de protection des applications pour les appareils Android ou iOS</span><span class="sxs-lookup"><span data-stu-id="a31cd-154">Set app protection settings for Android or iOS devices</span></span>](app-protection-settings-for-android-and-ios.md)

    - [<span data-ttu-id="a31cd-155">Définir les paramètres de protection des applications pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="a31cd-155">Set application protection settings for Windows 10 devices</span></span>](protection-settings-for-windows-10-devices.md)

    - [<span data-ttu-id="a31cd-156">Définir les paramètres de protection des appareils pour Windows 10 PC</span><span class="sxs-lookup"><span data-stu-id="a31cd-156">Set device protection settings for Windows 10 PCs</span></span>](protection-settings-for-windows-10-pcs.md)

4. <span data-ttu-id="a31cd-157">Une fois les stratégies définies, vous et vos employés pouvez configurer des appareils :</span><span class="sxs-lookup"><span data-stu-id="a31cd-157">After you set up policies, you and your employees can set up devices:</span></span>

    - <span data-ttu-id="a31cd-158">Si vos Windows n’utilisent pas déjà la mise à jour Windows Pro Creator, vous devez les mettre à niveau [vers Windows Pro Creators Update](upgrade-to-windows-pro-creators-update.md).</span><span class="sxs-lookup"><span data-stu-id="a31cd-158">If your Windows devices aren't already using the Windows Pro Creator update, you'll need to [upgrade them to Windows Pro Creators Update](upgrade-to-windows-pro-creators-update.md).</span></span>

    - <span data-ttu-id="a31cd-159">Voir [Configurer des Windows pour les Microsoft 365 Business Premium utilisateurs pour](set-up-windows-devices.md) obtenir les étapes à suivre Windows appareils.</span><span class="sxs-lookup"><span data-stu-id="a31cd-159">See [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md) for steps for Windows devices.</span></span>

    - <span data-ttu-id="a31cd-160">Voir [Configurer des appareils mobiles pour Microsoft 365 Business Premium utilisateurs pour](set-up-mobile-devices.md) obtenir la procédure pour les téléphones et iPhone Android.</span><span class="sxs-lookup"><span data-stu-id="a31cd-160">See [Set up mobile devices for Microsoft 365 Business Premium users](set-up-mobile-devices.md) for steps for Android phones and iPhones.</span></span>