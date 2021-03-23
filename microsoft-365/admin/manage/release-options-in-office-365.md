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
description: Découvrez comment configurer l’option de publication pour les nouvelles mises à jour de produits et de fonctionnalités dans le Centre d’administration Microsoft 365.
ms.openlocfilehash: e909cdf35ba9dd8282540783f7c362e5ae49212e
ms.sourcegitcommit: 8998f70d3f7bd673f93f8d1cf12ce981b1b771c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51034078"
---
# <a name="set-up-the-standard-or-targeted-release-options"></a><span data-ttu-id="97dd1-103">Configurer les options de publication standard ou ciblée</span><span class="sxs-lookup"><span data-stu-id="97dd1-103">Set up the Standard or Targeted release options</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="97dd1-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="97dd1-104">The admin center is changing.</span></span> <span data-ttu-id="97dd1-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="97dd1-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span></span>

::: moniker-end

> [!IMPORTANT]
> <span data-ttu-id="97dd1-106">Les mises à jour Microsoft 365 décrites dans cet article s’appliquent à Microsoft 365, SharePoint Online et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="97dd1-106">The Microsoft 365 updates described in this article apply to Microsoft 365, SharePoint Online, and Exchange Online.</span></span> <span data-ttu-id="97dd1-107">Ces options de publication sont des méthodes ciblées et efficaces pour publier les modifications apportées à Microsoft 365, mais ne peuvent pas être garanties en permanence ou pour toutes les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="97dd1-107">These release options are targeted, best effort ways to release changes to Microsoft 365 but cannot be guaranteed at all times or for all updates.</span></span> <span data-ttu-id="97dd1-108">Elles ne s’appliquent pas aux applications Microsoft 365, Skype Entreprise, Microsoft Teams et aux services associés.</span><span class="sxs-lookup"><span data-stu-id="97dd1-108">They do not apply to Microsoft 365 Apps, Skype for Business, Microsoft Teams, and related services.</span></span> <span data-ttu-id="97dd1-109">Pour plus d’informations sur les options de publication de Microsoft 365 Apps, voir Vue d’ensemble des canaux de mise à jour [pour Les applications Microsoft 365.](/deployoffice/overview-update-channels)</span><span class="sxs-lookup"><span data-stu-id="97dd1-109">For information about release options for Microsoft 365 Apps, see [Overview of update channels for Microsoft 365 Apps](/deployoffice/overview-update-channels).</span></span>

<span data-ttu-id="97dd1-110">Avec Microsoft 365, vous recevez de nouvelles mises à jour et fonctionnalités de produit dès qu’elles sont disponibles au lieu de faire des mises à jour coûteuses tous les quelques années.</span><span class="sxs-lookup"><span data-stu-id="97dd1-110">With Microsoft 365, you receive new product updates and features as they become available instead of doing costly updates every few years.</span></span> <span data-ttu-id="97dd1-111">Vous n'avez donc plus besoin de procéder à des mises à jour onéreuses chaque année.</span><span class="sxs-lookup"><span data-stu-id="97dd1-111">You can manage how your organization receives these updates.</span></span> <span data-ttu-id="97dd1-112">De plus, vous pouvez gérer la manière dont votre organisation reçoit ces mises à jour.</span><span class="sxs-lookup"><span data-stu-id="97dd1-112">For example, you can sign up for an early release so that your organization receives updates first.</span></span> <span data-ttu-id="97dd1-113">Par exemple, vous pouvez vous inscrire à une publication anticipée et faire profiter l'ensemble de votre organisation des mises à jour en avance, ou sélectionner un panel restreint d'utilisateurs qui les testeront.</span><span class="sxs-lookup"><span data-stu-id="97dd1-113">You can designate that only certain individuals receive the updates.</span></span> <span data-ttu-id="97dd1-114">Vous pouvez également décider de rester sur le programme de publication standard et recevoir les mises à jour plus tard.</span><span class="sxs-lookup"><span data-stu-id="97dd1-114">Or, you can remain on the default release schedule and receive the updates later.</span></span> <span data-ttu-id="97dd1-115">Cet article décrit les différentes options de publication et la façon dont vous pouvez les utiliser pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="97dd1-115">This article explains the different release options and how you can use them for your organization.</span></span>

## <a name="how-it-works---release-validation"></a><span data-ttu-id="97dd1-116">Mode de fonctionnement - Validation de publication</span><span class="sxs-lookup"><span data-stu-id="97dd1-116">How it works - release validation</span></span>

<span data-ttu-id="97dd1-117">Toute nouvelle version est d’abord testée et validée par l’équipe de fonctionnalités, puis par l’ensemble de l’équipe de fonctionnalités De Microsoft 365, puis par l’ensemble de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97dd1-117">Any new release is first tested and validated by the feature team, then by the entire Microsoft 365 feature team, followed by all of Microsoft.</span></span> <span data-ttu-id="97dd1-118">Un fois les tests et la validation internes accomplis, l'étape suivante consiste en une **publication ciblée** (anciennement nommée First Release) à destination des clients inscrits.</span><span class="sxs-lookup"><span data-stu-id="97dd1-118">After internal testing and validation, the next step is a **Targeted release** (formerly known as First release) to customers who opt in.</span></span> <span data-ttu-id="97dd1-119">À chaque cycle de publication, Microsoft recueille des commentaires, puis valide davantage la qualité en surveillant des métriques d'utilisation clés.</span><span class="sxs-lookup"><span data-stu-id="97dd1-119">At each release ring, Microsoft collects feedback and further validates quality by monitoring key usage metrics.</span></span> <span data-ttu-id="97dd1-120">Cette validation progressive est en place pour s'assurer que la publication à l'échelle mondiale est aussi robuste que possible.</span><span class="sxs-lookup"><span data-stu-id="97dd1-120">This series of progressive validation is in place to make sure the worldwide-release is as robust as possible.</span></span> <span data-ttu-id="97dd1-121">Les publications sont illustrées dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="97dd1-121">The releases are pictured in the following figure.</span></span> 
  
![Anneaux de validation de publication pour Microsoft 365](../../media/73611ed3-2d8c-4e7b-8074-9f03b239f9ed.png)
  
<span data-ttu-id="97dd1-123">Pour les mises à jour importantes, les clients sont initialement avertis par la feuille [de route Microsoft 365.](https://products.office.com/business/office-365-roadmap)</span><span class="sxs-lookup"><span data-stu-id="97dd1-123">For significant updates, customers are initially notified by the [Microsoft 365 Roadmap](https://products.office.com/business/office-365-roadmap).</span></span> <span data-ttu-id="97dd1-124">À mesure qu’une mise à jour approche du déploiement, elle est communiquée par le biais de votre centre de messages [Microsoft 365.](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter)</span><span class="sxs-lookup"><span data-stu-id="97dd1-124">As an update gets closer to rolling out, it is communicated through your [Microsoft 365 Message center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter).</span></span>

> [!NOTE]
> <span data-ttu-id="97dd1-125">Vous avez besoin d’un compte Microsoft 365 ou Azure AD pour accéder à votre centre de messages via le [Centre d’administration.](/office365/admin/admin-overview/about-the-admin-center)</span><span class="sxs-lookup"><span data-stu-id="97dd1-125">You need a Microsoft 365 or Azure AD account to access your Message center through the [admin center](/office365/admin/admin-overview/about-the-admin-center).</span></span> <span data-ttu-id="97dd1-126">Les utilisateurs du plan d’accueil Microsoft 365 n’ont pas de centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="97dd1-126">Microsoft 365 home plan users do not have an admin center.</span></span>


## <a name="standard-release"></a><span data-ttu-id="97dd1-127">Publication standard</span><span class="sxs-lookup"><span data-stu-id="97dd1-127">Standard release</span></span>

<span data-ttu-id="97dd1-128">Il s’agit de l’option par défaut dans laquelle vous et vos utilisateurs recevez les dernières mises à jour lorsqu’elles sont publiées largement pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="97dd1-128">This is the default option where you and your users receive the latest updates when they're released broadly to all customers.</span></span>
  
<span data-ttu-id="97dd1-129">Une bonne pratique consiste à laisser la majorité des utilisateurs  dans la version **Standard** et les professionnels de l’informatique et les utilisateurs avec pouvoir dans la version ciblée pour évaluer les nouvelles fonctionnalités et préparer les équipes à prendre en charge les utilisateurs professionnels et les cadres.</span><span class="sxs-lookup"><span data-stu-id="97dd1-129">A good practice is to leave the majority of users in **Standard release** and IT Pros and power users in **Targeted release** to evaluate new features and prepare teams to support business users and executives.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="97dd1-130">Si, après avoir souscrit au programme de publication ciblée, vous décidez de revenir au programme de publication standard, vos utilisateurs risquent de perdre l'accès aux fonctionnalités qui n'ont pas encore atteint le niveau de publication standard.</span><span class="sxs-lookup"><span data-stu-id="97dd1-130">If you switch from targeted release back to standard release track, your users may lose access to features that haven't reached standard release yet.</span></span> 
  
## <a name="targeted-release"></a><span data-ttu-id="97dd1-131">Version ciblée</span><span class="sxs-lookup"><span data-stu-id="97dd1-131">Targeted release</span></span>

<span data-ttu-id="97dd1-p107">Cette option vous permet, ainsi qu'à vos utilisateurs, d'être les premiers à profiter des dernières mises à jour, ainsi que de contribuer au développement du produit en envoyant des commentaires avant la mise à disposition générale. Vous pouvez choisir de diffuser les mises à jour de façon anticipée à des personnes spécifiques ou à l'ensemble de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="97dd1-p107">With this option, you and your users can be the first to see the latest updates and help shape the product by providing early feedback. You can choose to have individuals or the entire organization receive updates early.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="97dd1-p108">Les mises à jour d'envergure ou complexes peuvent demander plus de temps avant d'être diffusées, de sorte qu'aucun utilisateur ne soit affecté. Aucune garantie ne peut être apportée quant au calendrier exact des publications.</span><span class="sxs-lookup"><span data-stu-id="97dd1-p108">Large or complex updates may take longer than others so that no users are adversely affected. There is no guarantee on the exact timeline of a release.</span></span> 
  
### <a name="targeted-release-for-entire-organization"></a><span data-ttu-id="97dd1-136">Publication ciblée pour l'organisation entière</span><span class="sxs-lookup"><span data-stu-id="97dd1-136">Targeted release for entire organization</span></span>

<span data-ttu-id="97dd1-137">Si vous [définissez l’option de publication](#set-up-the-release-option-in-the-admin-center) dans le Centre d’administration pour cette option, tous vos utilisateurs obtiennent l’expérience de publication ciblée.</span><span class="sxs-lookup"><span data-stu-id="97dd1-137">If you [Set up the release option in the admin center](#set-up-the-release-option-in-the-admin-center) for this option, all your users will get the Targeted release experience.</span></span> <span data-ttu-id="97dd1-138">Aux organisations comptant plus de 300 utilisateurs, nous recommandons d'utiliser un abonnement d'essai pour cette option.</span><span class="sxs-lookup"><span data-stu-id="97dd1-138">For organizations with more than 300 users, we recommend using a test subscription for this option.</span></span> <span data-ttu-id="97dd1-139">Pour plus d'informations sur les abonnements d'essai, veuillez vous adresser à votre contact Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97dd1-139">For test subscription information, please reach out to your Microsoft contact.</span></span> 
  
### <a name="targeted-release-for-selected-users"></a><span data-ttu-id="97dd1-140">Publication ciblée pour des utilisateurs sélectionnés</span><span class="sxs-lookup"><span data-stu-id="97dd1-140">Targeted release for selected users</span></span>

<span data-ttu-id="97dd1-141">Si vous [définissez l’option](#set-up-the-release-option-in-the-admin-center) de publication dans le Centre d’administration pour cette option, vous pouvez définir des utilisateurs spécifiques, généralement des utilisateurs avec pouvoir, pour bénéficier d’un accès en avant-première aux fonctionnalités et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="97dd1-141">If you [Set up the release option in the admin center](#set-up-the-release-option-in-the-admin-center) for this option, you can define specific users, usually power users, to receive early access to features and functionality.</span></span> 
  
## <a name="benefits-of-targeted-release"></a><span data-ttu-id="97dd1-142">Avantages de la publication ciblée</span><span class="sxs-lookup"><span data-stu-id="97dd1-142">Benefits of Targeted release</span></span>

<span data-ttu-id="97dd1-143">La publication ciblée permet aux administrateurs, aux responsables des modifications ou à toute autre personne responsable des mises à jour Microsoft 365 de se préparer aux modifications à venir en leur permettant de :</span><span class="sxs-lookup"><span data-stu-id="97dd1-143">Targeted release allows admins, change managers, or anyone else responsible for Microsoft 365 updates to prepare for the upcoming changes by letting them:</span></span>
  
- <span data-ttu-id="97dd1-144">tester et valider les nouvelles mises à jour avant qu'elles soient publiées pour tous les utilisateurs au sein de l'organisation ;</span><span class="sxs-lookup"><span data-stu-id="97dd1-144">Test and validate new updates before they are released to all the users in the organization.</span></span>
    
- <span data-ttu-id="97dd1-145">préparer la notification et la documentation à l'adresse des utilisateurs avant la publication des mises à jour à l'échelle mondiale ;</span><span class="sxs-lookup"><span data-stu-id="97dd1-145">Prepare user notification and documentation before updates are released worldwide.</span></span>
    
- <span data-ttu-id="97dd1-146">préparer le support technique interne aux changements à venir ;</span><span class="sxs-lookup"><span data-stu-id="97dd1-146">Prepare internal help-desk for upcoming changes.</span></span>
    
- <span data-ttu-id="97dd1-147">effectuer les contrôles de sécurité et de conformité ;</span><span class="sxs-lookup"><span data-stu-id="97dd1-147">Go through compliance and security reviews.</span></span>
    
- <span data-ttu-id="97dd1-148">utiliser des contrôles de fonctionnalité, le cas échéant, pour contrôler la publication des mises à jour aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="97dd1-148">Use feature controls, where applicable, to control the release of updates to end users.</span></span>
    
## <a name="set-up-the-release-option-in-the-admin-center"></a><span data-ttu-id="97dd1-149">Configurer l’option de publication dans le Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="97dd1-149">Set up the release option in the admin center</span></span>

<span data-ttu-id="97dd1-150">Vous pouvez modifier la façon dont votre organisation reçoit les mises à jour Microsoft 365 en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="97dd1-150">You can change how your organization receives Microsoft 365 updates by following these steps.</span></span> <span data-ttu-id="97dd1-151">Vous devez être administrateur global dans Microsoft 365 pour vous y rendre.</span><span class="sxs-lookup"><span data-stu-id="97dd1-151">You have to be a global admin in Microsoft 365 to opt in.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="97dd1-152">L’application des modifications ci-dessous dans Microsoft 365 peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="97dd1-152">It can take up to 24 hours for the below changes to take effect in Microsoft 365.</span></span> <span data-ttu-id="97dd1-153">Si vous décidez de ne plus participer au programme de publication ciblée après l'avoir activé, vos utilisateurs risquent de perdre l'accès aux fonctionnalités qui n'ont pas encore atteint le niveau de publication planifiée.</span><span class="sxs-lookup"><span data-stu-id="97dd1-153">If you opt out of targeted release after enabling it, your users may lose access to features that haven't reached the scheduled release yet.</span></span> 
  
1. <span data-ttu-id="97dd1-154">Dans le Centre d’administration, sélectionnez **Paramètres** de l’organisation, puis sous l’onglet Profil de l’organisation, choisissez Préférences  >   **de publication.** </span><span class="sxs-lookup"><span data-stu-id="97dd1-154">In the admin center, go to the **Settings** > **Org Setting**, and under the **Organization profile** tab, choose **Release preferences**.</span></span>

5. <span data-ttu-id="97dd1-155">Pour désactiver la publication ciblée, sélectionnez **Publication standard,** puis **sélectionnez Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="97dd1-155">To disable targeted release, select **Standard release**, then select **Save changes**.</span></span> 
    
6. <span data-ttu-id="97dd1-156">Pour activer la publication ciblée pour tous les utilisateurs de votre organisation, sélectionnez Publication ciblée **pour** tout le monde, puis **sélectionnez Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="97dd1-156">To enable targeted release for all users in your organization, select **Targeted release for everyone**, then select **Save changes**.</span></span> 
    
7. <span data-ttu-id="97dd1-157">Pour activer la publication ciblée pour certaines personnes de votre organisation, sélectionnez **Publication** ciblée pour les utilisateurs sélectionnés, puis **sélectionnez Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="97dd1-157">To enable targeted release for some people in your organization, select **Targeted release for selected users**, then select **Save changes**.</span></span> 
    
8. <span data-ttu-id="97dd1-158">Sélectionnez **Sélectionner des utilisateurs** pour ajouter des utilisateurs un par un ou Charger des utilisateurs **pour** les ajouter en bloc.</span><span class="sxs-lookup"><span data-stu-id="97dd1-158">Choose **Select users** to add users one at a time, or **Upload users** to add them in bulk.</span></span>
    
9. <span data-ttu-id="97dd1-159">Lorsque vous avez terminé d’ajouter des utilisateurs, **sélectionnez Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="97dd1-159">When you're done adding users, select **Save changes**.</span></span>


  
## <a name="learn-more"></a><span data-ttu-id="97dd1-160">Si vous souhaitez en savoir plus</span><span class="sxs-lookup"><span data-stu-id="97dd1-160">Learn more</span></span>

<span data-ttu-id="97dd1-161">Découvrez comment gérer [les messages](/office365/admin/manage/message-center) dans votre centre de messages [Microsoft 365](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter) pour recevoir des notifications sur les mises à jour et les mises à jour Microsoft 365 à venir.</span><span class="sxs-lookup"><span data-stu-id="97dd1-161">Discover how to [manage messages](/office365/admin/manage/message-center) in your [Microsoft 365 Message center](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/MessageCenter) to get notifications about upcoming Microsoft 365 updates and releases.</span></span>

## <a name="related-articles"></a><span data-ttu-id="97dd1-162">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="97dd1-162">Related Articles</span></span>

[<span data-ttu-id="97dd1-163">Office Insider</span><span class="sxs-lookup"><span data-stu-id="97dd1-163">Office Insider</span></span>](https://insider.office.com/join/windows)
