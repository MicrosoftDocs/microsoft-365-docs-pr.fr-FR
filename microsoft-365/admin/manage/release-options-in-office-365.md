---
title: Configurer les options de publications standard et ciblée dans Office 365
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
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 3b3adfa4-1777-4ff0-b606-fb8732101f47
description: Découvrez comment configurer l’option de publication pour les mises à jour de nouveaux produits et fonctionnalités dans le centre d’administration 365 de Microsoft.
ms.openlocfilehash: 2d4940003c791e50926eff46aaf6a299e60fb9aa
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42252797"
---
# <a name="set-up-the-standard-or-targeted-release-options-in-office-365"></a><span data-ttu-id="dde36-103">Configurer les options de publications standard et ciblée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="dde36-103">Set up the Standard or Targeted release options in Office 365</span></span>

<span data-ttu-id="dde36-p101">[] Avec Office 365, vous recevez les nouvelles mises à jour et fonctionnalités des produits dès que celles-ci sont disponibles. Vous n'avez donc plus besoin de procéder à des mises à jour onéreuses chaque année. De plus, vous pouvez gérer la manière dont votre organisation reçoit ces mises à jour. Par exemple, vous pouvez vous inscrire à une publication anticipée et faire profiter l'ensemble de votre organisation des mises à jour en avance, ou sélectionner un panel restreint d'utilisateurs qui les testeront. Vous pouvez également décider de rester sur le programme de publication standard et recevoir les mises à jour plus tard. Cette article présente les différents programmes de publication disponibles, et explique la manière dont vous pouvez les utiliser au profit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dde36-p101">With Office 365, you receive new product updates and features as they become available instead of doing costly updates every few years. You can manage how your organization receives these updates. For example, you can sign up for an early release so that your organization receives updates first. You can designate that only certain individuals receive the updates. Or, you can remain on the default release schedule and receive the updates later. This article explain the different release options and how you can use them for your organization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dde36-p102">Les mises à jour Office 365 décrites dans cet article s'appliquent à Office 365, SharePoint Online et Exchange Online, pas à Skype Entreprise et aux services qui y sont associés. Ces options de publication sont des canaux ciblés et privilégiés pour la publication de modifications apportées à Office 365. En revanche, ces options ne peuvent en aucun cas être garanties à chaque fois ou pour toutes les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="dde36-p102">The Office 365 updates described in this article apply to Office 365, SharePoint Online, and Exchange Online. They do not apply to Skype for Business and related services. These release options are targeted, best effort ways to release changes to Office 365 but cannot be guaranteed at all times or for all updates.</span></span> 
  
## <a name="how-it-works---release-validation"></a><span data-ttu-id="dde36-113">Mode de fonctionnement - Validation de publication</span><span class="sxs-lookup"><span data-stu-id="dde36-113">How it works - release validation</span></span>

<span data-ttu-id="dde36-114">Toute nouvelle version est d’abord testée et validée par l’équipe de fonctionnalité, puis par l’équipe de fonctionnalité Office 365, suivie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dde36-114">Any new release is first tested and validated by the feature team, then by the entire Office 365 feature team, followed by all of Microsoft.</span></span> <span data-ttu-id="dde36-115">Un fois les tests et la validation internes accomplis, l'étape suivante consiste en une **publication ciblée** (anciennement nommée First Release) à destination des clients inscrits.</span><span class="sxs-lookup"><span data-stu-id="dde36-115">After internal testing and validation, the next step is a **Targeted release** (formerly known as First release) to customers who opt in.</span></span> <span data-ttu-id="dde36-116">À chaque cycle de publication, Microsoft recueille des commentaires, puis valide davantage la qualité en surveillant des métriques d'utilisation clés.</span><span class="sxs-lookup"><span data-stu-id="dde36-116">At each release ring, Microsoft collects feedback and further validates quality by monitoring key usage metrics.</span></span> <span data-ttu-id="dde36-117">Cette validation progressive est en place pour s'assurer que la publication à l'échelle mondiale est aussi robuste que possible.</span><span class="sxs-lookup"><span data-stu-id="dde36-117">This series of progressive validation is in place to make sure the worldwide-release is as robust as possible.</span></span> <span data-ttu-id="dde36-118">Les publications sont illustrées dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="dde36-118">The releases are pictured in the following figure.</span></span> 
  
![Sonneries de validation de publication pour Office 365](../media/73611ed3-2d8c-4e7b-8074-9f03b239f9ed.png)
  
<span data-ttu-id="dde36-120">Pour les mises à jour importantes, les clients Office sont initialement avertis par la feuille de [route Microsoft 365](https://products.office.com/business/office-365-roadmap).</span><span class="sxs-lookup"><span data-stu-id="dde36-120">For significant updates, Office customers are initially notified by the [Microsoft 365 Roadmap](https://products.office.com/business/office-365-roadmap).</span></span> <span data-ttu-id="dde36-121">Une fois que la mise à jour s’avère plus proche du déploiement, elle est communiquée via votre [Centre de messages Office 365](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter).</span><span class="sxs-lookup"><span data-stu-id="dde36-121">As an update gets closer to rolling out, it is communicated through your [Office 365 Message center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter).</span></span>

> [!NOTE]
> <span data-ttu-id="dde36-122">Vous avez besoin d’un compte Office 365 ou Azure AD pour accéder à votre centre de messages via le [Centre d’administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center).</span><span class="sxs-lookup"><span data-stu-id="dde36-122">You need an Office 365 or Azure AD account to access your Message center through the [admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center).</span></span> <span data-ttu-id="dde36-123">Plan d’accueil Office 365 les utilisateurs ne disposent pas d’un centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="dde36-123">Office 365 home plan users do not have an admin center.</span></span>


## <a name="standard-release"></a><span data-ttu-id="dde36-124">Publication standard</span><span class="sxs-lookup"><span data-stu-id="dde36-124">Standard release</span></span>

<span data-ttu-id="dde36-125">Il s’agit de l’option par défaut où vous et vos utilisateurs recevez les dernières mises à jour lorsqu’elles sont publiées à grande échelle pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="dde36-125">This is the default option where you and your users receive the latest updates when they're released broadly to all customers.</span></span>
  
<span data-ttu-id="dde36-126">Une bonne pratique consiste à laisser à la majorité des utilisateurs de la **version standard** , aux professionnels de l’informatique et aux utilisateurs chevronnés de la **version ciblée** pour évaluer de nouvelles fonctionnalités et préparer teams pour prendre en charge les utilisateurs et les cadres professionnels.</span><span class="sxs-lookup"><span data-stu-id="dde36-126">A good practice is to leave the majority of users in **Standard release** and IT Pros and power users in **Targeted release** to evaluate new features and prepare teams to support business users and executives.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dde36-127">Si, après avoir souscrit au programme de publication ciblée, vous décidez de revenir au programme de publication standard, vos utilisateurs risquent de perdre l'accès aux fonctionnalités qui n'ont pas encore atteint le niveau de publication standard.</span><span class="sxs-lookup"><span data-stu-id="dde36-127">If you switch from targeted release back to standard release track, your users may lose access to features that haven't reached standard release yet.</span></span> 
  
## <a name="targeted-release"></a><span data-ttu-id="dde36-128">Version ciblée</span><span class="sxs-lookup"><span data-stu-id="dde36-128">Targeted release</span></span>

<span data-ttu-id="dde36-p106">Cette option vous permet, ainsi qu'à vos utilisateurs, d'être les premiers à profiter des dernières mises à jour, ainsi que de contribuer au développement du produit en envoyant des commentaires avant la mise à disposition générale. Vous pouvez choisir de diffuser les mises à jour de façon anticipée à des personnes spécifiques ou à l'ensemble de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="dde36-p106">With this option, you and your users can be the first to see the latest updates and help shape the product by providing early feedback. You can choose to have individuals or the entire organization receive updates early.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dde36-p107">Les mises à jour d'envergure ou complexes peuvent demander plus de temps avant d'être diffusées, de sorte qu'aucun utilisateur ne soit affecté. Aucune garantie ne peut être apportée quant au calendrier exact des publications.</span><span class="sxs-lookup"><span data-stu-id="dde36-p107">Large or complex updates may take longer than others so that no users are adversely affected. There is no guarantee on the exact timeline of a release.</span></span> 
  
### <a name="targeted-release-for-entire-organization"></a><span data-ttu-id="dde36-133">Publication ciblée pour l'organisation entière</span><span class="sxs-lookup"><span data-stu-id="dde36-133">Targeted release for entire organization</span></span>

<span data-ttu-id="dde36-134">Si vous [configurez l’option de publication dans le centre d’administration](#set-up-the-release-option-in-the-admin-center) pour cette option, tous vos utilisateurs bénéficieront de l’expérience de publication ciblée.</span><span class="sxs-lookup"><span data-stu-id="dde36-134">If you [Set up the release option in the admin center](#set-up-the-release-option-in-the-admin-center) for this option, all your users will get the Targeted release experience.</span></span> <span data-ttu-id="dde36-135">Aux organisations comptant plus de 300 utilisateurs, nous recommandons d'utiliser un abonnement d'essai pour cette option.</span><span class="sxs-lookup"><span data-stu-id="dde36-135">For organizations with more than 300 users, we recommend using a test subscription for this option.</span></span> <span data-ttu-id="dde36-136">Pour plus d'informations sur les abonnements d'essai, veuillez vous adresser à votre contact Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dde36-136">For test subscription information, please reach out to your Microsoft contact.</span></span> 
  
### <a name="targeted-release-for-selected-users"></a><span data-ttu-id="dde36-137">Publication ciblée pour des utilisateurs sélectionnés</span><span class="sxs-lookup"><span data-stu-id="dde36-137">Targeted release for selected users</span></span>

<span data-ttu-id="dde36-138">Si vous [configurez l’option de publication dans le centre d’administration](#set-up-the-release-option-in-the-admin-center) pour cette option, vous pouvez définir des utilisateurs spécifiques, généralement des utilisateurs avec pouvoir, pour bénéficier d’un accès anticipé aux fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dde36-138">If you [Set up the release option in the admin center](#set-up-the-release-option-in-the-admin-center) for this option, you can define specific users, usually power users, to receive early access to features and functionality.</span></span> 
  
## <a name="benefits-of-targeted-release"></a><span data-ttu-id="dde36-139">Avantages de la publication ciblée</span><span class="sxs-lookup"><span data-stu-id="dde36-139">Benefits of Targeted release</span></span>

<span data-ttu-id="dde36-140">Une publication ciblée permet aux administrateurs, aux gestionnaires de modification ou à toute autre personne responsable des mises à jour Office 365 de préparer des changements à venir en leur offrant la possibilité d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dde36-140">Targeted release allows admins, change managers, or anyone else responsible for Office 365 updates to prepare for the upcoming changes by letting them:</span></span>
  
- <span data-ttu-id="dde36-141">tester et valider les nouvelles mises à jour avant qu'elles soient publiées pour tous les utilisateurs au sein de l'organisation ;</span><span class="sxs-lookup"><span data-stu-id="dde36-141">Test and validate new updates before they are released to all the users in the organization.</span></span>
    
- <span data-ttu-id="dde36-142">préparer la notification et la documentation à l'adresse des utilisateurs avant la publication des mises à jour à l'échelle mondiale ;</span><span class="sxs-lookup"><span data-stu-id="dde36-142">Prepare user notification and documentation before updates are released worldwide.</span></span>
    
- <span data-ttu-id="dde36-143">préparer le support technique interne aux changements à venir ;</span><span class="sxs-lookup"><span data-stu-id="dde36-143">Prepare internal help-desk for upcoming changes.</span></span>
    
- <span data-ttu-id="dde36-144">effectuer les contrôles de sécurité et de conformité ;</span><span class="sxs-lookup"><span data-stu-id="dde36-144">Go through compliance and security reviews.</span></span>
    
- <span data-ttu-id="dde36-145">utiliser des contrôles de fonctionnalité, le cas échéant, pour contrôler la publication des mises à jour aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="dde36-145">Use feature controls, where applicable, to control the release of updates to end users.</span></span>
    
## <a name="set-up-the-release-option-in-the-admin-center"></a><span data-ttu-id="dde36-146">Configurer l’option de publication dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="dde36-146">Set up the release option in the admin center</span></span>

<span data-ttu-id="dde36-p109">Vous pouvez modifier la manière dont votre organisation reçoit les mises à jour Office 365 en procédant comme suit. Pour choisir cette options, vous devez être un administrateur général dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="dde36-p109">You can change how your organization receives Office 365 updates by following these steps. You have to be a global admin in Office 365 to opt in.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dde36-p110">Jusqu'à 24 heures peuvent être nécessaires pour que les modifications ci-dessous soient appliquées dans Office 365. Si vous décidez de ne plus participer au programme de publication ciblée après l'avoir activé, vos utilisateurs risquent de perdre l'accès aux fonctionnalités qui n'ont pas encore atteint le niveau de publication planifiée.</span><span class="sxs-lookup"><span data-stu-id="dde36-p110">It can take up to 24 hours for the below changes to take effect in Office 365. If you opt out of targeted release after enabling it, your users may lose access to features that haven't reached the scheduled release yet.</span></span> 
  
1. <span data-ttu-id="dde36-151">Dans le centre d’administration, accédez au \*\*\*\* > **paramètre**paramètres, puis sous l’onglet Profil de l' **organisation** , choisissez Modifier les **Préférences de publication**.</span><span class="sxs-lookup"><span data-stu-id="dde36-151">In the admin center, go to the **Settings** > **Setting**, and under the **Organization profile** tab, choose **Release preferences**.</span></span>

5. <span data-ttu-id="dde36-152">Pour désactiver la version ciblée, sélectionnez **version standard**, puis **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dde36-152">To disable targeted release, select **Standard release**, then select **Save changes**.</span></span> 
    
6. <span data-ttu-id="dde36-153">Pour activer la publication ciblée pour tous les utilisateurs de votre organisation, sélectionnez **publication ciblée pour tout le monde**, puis **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dde36-153">To enable targeted release for all users in your organization, select **Targeted release for everyone**, then select **Save changes**.</span></span> 
    
7. <span data-ttu-id="dde36-154">Pour activer la publication ciblée pour certaines personnes de votre organisation, sélectionnez **publication ciblée pour les utilisateurs sélectionnés**, puis cliquez sur **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dde36-154">To enable targeted release for some people in your organization, select **Targeted release for selected users**, then select **Save changes**.</span></span> 
    
8. <span data-ttu-id="dde36-155">Choisissez **Sélectionner les utilisateurs** pour ajouter un utilisateur à la fois ou **Télécharger des utilisateurs** pour les ajouter en bloc.</span><span class="sxs-lookup"><span data-stu-id="dde36-155">Choose **Select users** to add users one at a time, or **Upload users** to add them in bulk.</span></span>
    
9. <span data-ttu-id="dde36-156">Lorsque vous avez terminé d’ajouter des utilisateurs, sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dde36-156">When you're done adding users, select **Save changes**.</span></span>



## <a name="get-the-targeted-release-version-of-office"></a><span data-ttu-id="dde36-157">Obtenir la version ciblée d’Office</span><span class="sxs-lookup"><span data-stu-id="dde36-157">Get the Targeted release version of Office</span></span>

<span data-ttu-id="dde36-p111">Pour installer une build de publication ciblée d'Office, [suivez ces étapes](https://support.office.com/article/4dd8ba40-73c0-4468-b778-c7b744d03ead). Vous pourrez ainsi utiliser en avant-première les nouvelles fonctionnalités d'Office 2016 pour ordinateur de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="dde36-p111">To install a targeted release build of Office, [follow these steps](https://support.office.com/article/4dd8ba40-73c0-4468-b778-c7b744d03ead). This gives you early access to the new features of Office 2016 for Windows desktops.</span></span>
  
## <a name="learn-more"></a><span data-ttu-id="dde36-160">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="dde36-160">Learn more</span></span>

<span data-ttu-id="dde36-161">Découvrez comment [gérer les messages](https://docs.microsoft.com/office365/admin/manage/message-center) dans votre [Centre de messages Office 365](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter) pour obtenir des notifications sur les mises à jour et les versions ultérieures d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="dde36-161">Discover how to [manage messages](https://docs.microsoft.com/office365/admin/manage/message-center) in your [Office 365 Message center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter) to get notifications about upcoming Office 365 updates and releases.</span></span>
