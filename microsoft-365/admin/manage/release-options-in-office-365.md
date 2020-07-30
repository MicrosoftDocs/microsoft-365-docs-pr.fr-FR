---
title: Configurer les options de publication standard ou ciblée
f1.keywords:
- CSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 3b3adfa4-1777-4ff0-b606-fb8732101f47
description: Découvrez comment configurer l’option de publication pour les mises à jour de nouveaux produits et fonctionnalités dans le centre d’administration 365 de Microsoft.
ms.openlocfilehash: 3baec050f33893357b25c832552643cf3a6d10d0
ms.sourcegitcommit: 1b83b6bcacb997324bc4be355deba6daf319591d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2020
ms.locfileid: "46502878"
---
# <a name="set-up-the-standard-or-targeted-release-options"></a><span data-ttu-id="cce51-103">Configurer les options de publication standard ou ciblée</span><span class="sxs-lookup"><span data-stu-id="cce51-103">Set up the Standard or Targeted release options</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="cce51-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="cce51-104">The admin center is changing.</span></span> <span data-ttu-id="cce51-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="cce51-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="cce51-106">Avec Microsoft 365, vous recevez de nouvelles mises à jour de produits et de nouvelles fonctionnalités dès qu’elles sont disponibles au lieu d’effectuer des mises à jour coûteuses tous les ans.</span><span class="sxs-lookup"><span data-stu-id="cce51-106">With Microsoft 365, you receive new product updates and features as they become available instead of doing costly updates every few years.</span></span> <span data-ttu-id="cce51-107">Vous n'avez donc plus besoin de procéder à des mises à jour onéreuses chaque année.</span><span class="sxs-lookup"><span data-stu-id="cce51-107">You can manage how your organization receives these updates.</span></span> <span data-ttu-id="cce51-108">De plus, vous pouvez gérer la manière dont votre organisation reçoit ces mises à jour.</span><span class="sxs-lookup"><span data-stu-id="cce51-108">For example, you can sign up for an early release so that your organization receives updates first.</span></span> <span data-ttu-id="cce51-109">Par exemple, vous pouvez vous inscrire à une publication anticipée et faire profiter l'ensemble de votre organisation des mises à jour en avance, ou sélectionner un panel restreint d'utilisateurs qui les testeront.</span><span class="sxs-lookup"><span data-stu-id="cce51-109">You can designate that only certain individuals receive the updates.</span></span> <span data-ttu-id="cce51-110">Vous pouvez également décider de rester sur le programme de publication standard et recevoir les mises à jour plus tard.</span><span class="sxs-lookup"><span data-stu-id="cce51-110">Or, you can remain on the default release schedule and receive the updates later.</span></span> <span data-ttu-id="cce51-111">Cet article décrit les différentes options de publication et comment vous pouvez les utiliser pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cce51-111">This article explains the different release options and how you can use them for your organization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cce51-112">Les mises à jour de Microsoft 365 décrites dans cet article s’appliquent à Microsoft 365, SharePoint Online et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cce51-112">The Microsoft 365 updates described in this article apply to Microsoft 365, SharePoint Online, and Exchange Online.</span></span> <span data-ttu-id="cce51-113">Ces options de publication sont des canaux ciblés et privilégiés pour la publication de modifications apportées à Office 365.</span><span class="sxs-lookup"><span data-stu-id="cce51-113">They do not apply to Skype for Business and related services.</span></span> <span data-ttu-id="cce51-114">Ces options de publication sont ciblées, meilleures moyens de publier les modifications apportées à Microsoft 365, mais elles ne sont pas garanties à tout moment ou pour toutes les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="cce51-114">These release options are targeted, best effort ways to release changes to Microsoft 365 but cannot be guaranteed at all times or for all updates.</span></span> 

> [!NOTE]
> <span data-ttu-id="cce51-115">Pour plus d’informations sur les canaux de mise à jour pour les applications, voir [vue d’ensemble des canaux de mise à jour pour les applications Microsoft 365](https://docs.microsoft.com/deployoffice/overview-update-channels).</span><span class="sxs-lookup"><span data-stu-id="cce51-115">For information about update channels for applications, see [Overview of update channels for Microsoft 365 Apps](https://docs.microsoft.com/deployoffice/overview-update-channels).</span></span> 
  
## <a name="how-it-works---release-validation"></a><span data-ttu-id="cce51-116">Mode de fonctionnement - Validation de publication</span><span class="sxs-lookup"><span data-stu-id="cce51-116">How it works - release validation</span></span>

<span data-ttu-id="cce51-117">Toute nouvelle version est d’abord testée et validée par l’équipe de fonctionnalité, puis par l’équipe de fonctionnalité Microsoft 365 entière, suivie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cce51-117">Any new release is first tested and validated by the feature team, then by the entire Microsoft 365 feature team, followed by all of Microsoft.</span></span> <span data-ttu-id="cce51-118">Un fois les tests et la validation internes accomplis, l'étape suivante consiste en une **publication ciblée** (anciennement nommée First Release) à destination des clients inscrits.</span><span class="sxs-lookup"><span data-stu-id="cce51-118">After internal testing and validation, the next step is a **Targeted release** (formerly known as First release) to customers who opt in.</span></span> <span data-ttu-id="cce51-119">À chaque cycle de publication, Microsoft recueille des commentaires, puis valide davantage la qualité en surveillant des métriques d'utilisation clés.</span><span class="sxs-lookup"><span data-stu-id="cce51-119">At each release ring, Microsoft collects feedback and further validates quality by monitoring key usage metrics.</span></span> <span data-ttu-id="cce51-120">Cette validation progressive est en place pour s'assurer que la publication à l'échelle mondiale est aussi robuste que possible.</span><span class="sxs-lookup"><span data-stu-id="cce51-120">This series of progressive validation is in place to make sure the worldwide-release is as robust as possible.</span></span> <span data-ttu-id="cce51-121">Les publications sont illustrées dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="cce51-121">The releases are pictured in the following figure.</span></span> 
  
![Sonneries de validation de publication pour Microsoft 365](../../media/73611ed3-2d8c-4e7b-8074-9f03b239f9ed.png)
  
<span data-ttu-id="cce51-123">Pour les mises à jour importantes, les clients sont initialement avertis par la feuille de [route Microsoft 365](https://products.office.com/business/office-365-roadmap).</span><span class="sxs-lookup"><span data-stu-id="cce51-123">For significant updates, customers are initially notified by the [Microsoft 365 Roadmap](https://products.office.com/business/office-365-roadmap).</span></span> <span data-ttu-id="cce51-124">Une fois que la mise à jour s’avère plus proche du déploiement, elle est communiquée via votre [Centre de messages Microsoft 365](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter).</span><span class="sxs-lookup"><span data-stu-id="cce51-124">As an update gets closer to rolling out, it is communicated through your [Microsoft 365 Message center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter).</span></span>

> [!NOTE]
> <span data-ttu-id="cce51-125">Vous avez besoin d’un compte Microsoft 365 ou Azure AD pour accéder à votre centre de messages via le [Centre d’administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center).</span><span class="sxs-lookup"><span data-stu-id="cce51-125">You need a Microsoft 365 or Azure AD account to access your Message center through the [admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center).</span></span> <span data-ttu-id="cce51-126">Plan d’accueil Microsoft 365 les utilisateurs ne disposent pas d’un centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="cce51-126">Microsoft 365 home plan users do not have an admin center.</span></span>


## <a name="standard-release"></a><span data-ttu-id="cce51-127">Publication standard</span><span class="sxs-lookup"><span data-stu-id="cce51-127">Standard release</span></span>

<span data-ttu-id="cce51-128">Il s’agit de l’option par défaut où vous et vos utilisateurs recevez les dernières mises à jour lorsqu’elles sont publiées à grande échelle pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="cce51-128">This is the default option where you and your users receive the latest updates when they're released broadly to all customers.</span></span>
  
<span data-ttu-id="cce51-129">Une bonne pratique consiste à laisser à la majorité des utilisateurs de la **version standard** , aux professionnels de l’informatique et aux utilisateurs chevronnés de la **version ciblée** pour évaluer de nouvelles fonctionnalités et préparer teams pour prendre en charge les utilisateurs et les cadres professionnels.</span><span class="sxs-lookup"><span data-stu-id="cce51-129">A good practice is to leave the majority of users in **Standard release** and IT Pros and power users in **Targeted release** to evaluate new features and prepare teams to support business users and executives.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cce51-130">Si, après avoir souscrit au programme de publication ciblée, vous décidez de revenir au programme de publication standard, vos utilisateurs risquent de perdre l'accès aux fonctionnalités qui n'ont pas encore atteint le niveau de publication standard.</span><span class="sxs-lookup"><span data-stu-id="cce51-130">If you switch from targeted release back to standard release track, your users may lose access to features that haven't reached standard release yet.</span></span> 
  
## <a name="targeted-release"></a><span data-ttu-id="cce51-131">Version ciblée</span><span class="sxs-lookup"><span data-stu-id="cce51-131">Targeted release</span></span>

<span data-ttu-id="cce51-p107">Cette option vous permet, ainsi qu'à vos utilisateurs, d'être les premiers à profiter des dernières mises à jour, ainsi que de contribuer au développement du produit en envoyant des commentaires avant la mise à disposition générale. Vous pouvez choisir de diffuser les mises à jour de façon anticipée à des personnes spécifiques ou à l'ensemble de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="cce51-p107">With this option, you and your users can be the first to see the latest updates and help shape the product by providing early feedback. You can choose to have individuals or the entire organization receive updates early.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cce51-p108">Les mises à jour d'envergure ou complexes peuvent demander plus de temps avant d'être diffusées, de sorte qu'aucun utilisateur ne soit affecté. Aucune garantie ne peut être apportée quant au calendrier exact des publications.</span><span class="sxs-lookup"><span data-stu-id="cce51-p108">Large or complex updates may take longer than others so that no users are adversely affected. There is no guarantee on the exact timeline of a release.</span></span> 
  
### <a name="targeted-release-for-entire-organization"></a><span data-ttu-id="cce51-136">Publication ciblée pour l'organisation entière</span><span class="sxs-lookup"><span data-stu-id="cce51-136">Targeted release for entire organization</span></span>

<span data-ttu-id="cce51-137">Si vous [configurez l’option de publication dans le centre d’administration](#set-up-the-release-option-in-the-admin-center) pour cette option, tous vos utilisateurs bénéficieront de l’expérience de publication ciblée.</span><span class="sxs-lookup"><span data-stu-id="cce51-137">If you [Set up the release option in the admin center](#set-up-the-release-option-in-the-admin-center) for this option, all your users will get the Targeted release experience.</span></span> <span data-ttu-id="cce51-138">Aux organisations comptant plus de 300 utilisateurs, nous recommandons d'utiliser un abonnement d'essai pour cette option.</span><span class="sxs-lookup"><span data-stu-id="cce51-138">For organizations with more than 300 users, we recommend using a test subscription for this option.</span></span> <span data-ttu-id="cce51-139">Pour plus d'informations sur les abonnements d'essai, veuillez vous adresser à votre contact Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cce51-139">For test subscription information, please reach out to your Microsoft contact.</span></span> 
  
### <a name="targeted-release-for-selected-users"></a><span data-ttu-id="cce51-140">Publication ciblée pour des utilisateurs sélectionnés</span><span class="sxs-lookup"><span data-stu-id="cce51-140">Targeted release for selected users</span></span>

<span data-ttu-id="cce51-141">Si vous [configurez l’option de publication dans le centre d’administration](#set-up-the-release-option-in-the-admin-center) pour cette option, vous pouvez définir des utilisateurs spécifiques, généralement des utilisateurs avec pouvoir, pour bénéficier d’un accès anticipé aux fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="cce51-141">If you [Set up the release option in the admin center](#set-up-the-release-option-in-the-admin-center) for this option, you can define specific users, usually power users, to receive early access to features and functionality.</span></span> 
  
## <a name="benefits-of-targeted-release"></a><span data-ttu-id="cce51-142">Avantages de la publication ciblée</span><span class="sxs-lookup"><span data-stu-id="cce51-142">Benefits of Targeted release</span></span>

<span data-ttu-id="cce51-143">La publication ciblée permet aux administrateurs, responsables des modifications ou autres personnes responsables des mises à jour de Microsoft 365 de se préparer aux modifications à venir en les autorisant :</span><span class="sxs-lookup"><span data-stu-id="cce51-143">Targeted release allows admins, change managers, or anyone else responsible for Microsoft 365 updates to prepare for the upcoming changes by letting them:</span></span>
  
- <span data-ttu-id="cce51-144">tester et valider les nouvelles mises à jour avant qu'elles soient publiées pour tous les utilisateurs au sein de l'organisation ;</span><span class="sxs-lookup"><span data-stu-id="cce51-144">Test and validate new updates before they are released to all the users in the organization.</span></span>
    
- <span data-ttu-id="cce51-145">préparer la notification et la documentation à l'adresse des utilisateurs avant la publication des mises à jour à l'échelle mondiale ;</span><span class="sxs-lookup"><span data-stu-id="cce51-145">Prepare user notification and documentation before updates are released worldwide.</span></span>
    
- <span data-ttu-id="cce51-146">préparer le support technique interne aux changements à venir ;</span><span class="sxs-lookup"><span data-stu-id="cce51-146">Prepare internal help-desk for upcoming changes.</span></span>
    
- <span data-ttu-id="cce51-147">effectuer les contrôles de sécurité et de conformité ;</span><span class="sxs-lookup"><span data-stu-id="cce51-147">Go through compliance and security reviews.</span></span>
    
- <span data-ttu-id="cce51-148">utiliser des contrôles de fonctionnalité, le cas échéant, pour contrôler la publication des mises à jour aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="cce51-148">Use feature controls, where applicable, to control the release of updates to end users.</span></span>
    
## <a name="set-up-the-release-option-in-the-admin-center"></a><span data-ttu-id="cce51-149">Configurer l’option de publication dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="cce51-149">Set up the release option in the admin center</span></span>

<span data-ttu-id="cce51-150">Vous pouvez modifier la façon dont votre organisation reçoit les mises à jour de Microsoft 365 en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="cce51-150">You can change how your organization receives Microsoft 365 updates by following these steps.</span></span> <span data-ttu-id="cce51-151">Vous devez être un administrateur général dans Microsoft 365 pour y participer.</span><span class="sxs-lookup"><span data-stu-id="cce51-151">You have to be a global admin in Microsoft 365 to opt in.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cce51-152">Le suivi des modifications suivantes peut prendre jusqu’à 24 heures pour être pris en compte dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cce51-152">It can take up to 24 hours for the below changes to take effect in Microsoft 365.</span></span> <span data-ttu-id="cce51-153">Si vous décidez de ne plus participer au programme de publication ciblée après l'avoir activé, vos utilisateurs risquent de perdre l'accès aux fonctionnalités qui n'ont pas encore atteint le niveau de publication planifiée.</span><span class="sxs-lookup"><span data-stu-id="cce51-153">If you opt out of targeted release after enabling it, your users may lose access to features that haven't reached the scheduled release yet.</span></span> 
  
1. <span data-ttu-id="cce51-154">Dans le centre d’administration, accédez au **Settings**  >  **paramètre org**paramètres, puis sous l’onglet Profil de l' **organisation** , choisissez **publier les préférences**.</span><span class="sxs-lookup"><span data-stu-id="cce51-154">In the admin center, go to the **Settings** > **Org Setting**, and under the **Organization profile** tab, choose **Release preferences**.</span></span>

5. <span data-ttu-id="cce51-155">Pour désactiver la version ciblée, sélectionnez **version standard**, puis **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cce51-155">To disable targeted release, select **Standard release**, then select **Save changes**.</span></span> 
    
6. <span data-ttu-id="cce51-156">Pour activer la publication ciblée pour tous les utilisateurs de votre organisation, sélectionnez **publication ciblée pour tout le monde**, puis **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cce51-156">To enable targeted release for all users in your organization, select **Targeted release for everyone**, then select **Save changes**.</span></span> 
    
7. <span data-ttu-id="cce51-157">Pour activer la publication ciblée pour certaines personnes de votre organisation, sélectionnez **publication ciblée pour les utilisateurs sélectionnés**, puis cliquez sur **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cce51-157">To enable targeted release for some people in your organization, select **Targeted release for selected users**, then select **Save changes**.</span></span> 
    
8. <span data-ttu-id="cce51-158">Choisissez **Sélectionner les utilisateurs** pour ajouter un utilisateur à la fois ou **Télécharger des utilisateurs** pour les ajouter en bloc.</span><span class="sxs-lookup"><span data-stu-id="cce51-158">Choose **Select users** to add users one at a time, or **Upload users** to add them in bulk.</span></span>
    
9. <span data-ttu-id="cce51-159">Lorsque vous avez terminé d’ajouter des utilisateurs, sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cce51-159">When you're done adding users, select **Save changes**.</span></span>


  
## <a name="learn-more"></a><span data-ttu-id="cce51-160">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="cce51-160">Learn more</span></span>

<span data-ttu-id="cce51-161">Découvrez comment [gérer les messages](https://docs.microsoft.com/office365/admin/manage/message-center) dans votre [Centre de messages Microsoft 365](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter) pour obtenir des notifications sur les mises à jour et les versions futures de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cce51-161">Discover how to [manage messages](https://docs.microsoft.com/office365/admin/manage/message-center) in your [Microsoft 365 Message center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter) to get notifications about upcoming Microsoft 365 updates and releases.</span></span>
