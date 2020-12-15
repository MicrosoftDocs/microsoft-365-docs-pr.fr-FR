---
title: Degré de sécurisation Microsoft
description: Décrit Microsoft Secure score dans le centre de sécurité Microsoft 365, comment améliorer votre position de sécurité et ce que les administrateurs de sécurité peuvent vous attendre.
keywords: score de sécurité Microsoft, score de sécurisation, score de sécurité Office 365, score de sécurité Microsoft, centre de sécurité Microsoft 365, actions d’amélioration
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
ms.openlocfilehash: 7fe5be065ee45700a1f08a39c8050757c3843f7b
ms.sourcegitcommit: 29eb89b8ba0628fbef350e8995d2c38369a4ffa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "49682570"
---
# <a name="microsoft-secure-score"></a><span data-ttu-id="8171e-104">Degré de sécurisation Microsoft</span><span class="sxs-lookup"><span data-stu-id="8171e-104">Microsoft Secure Score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="8171e-105">Microsoft Secure score est une mesure de la position de sécurité d’une organisation, avec un nombre supérieur indiquant d’autres actions d’amélioration.</span><span class="sxs-lookup"><span data-stu-id="8171e-105">Microsoft Secure Score is a measurement of an organization's security posture, with a higher number indicating more improvement actions taken.</span></span> <span data-ttu-id="8171e-106">Vous pouvez https://security.microsoft.com/securescore le trouver dans le [Centre de sécurité Microsoft 365](overview-security-center.md).</span><span class="sxs-lookup"><span data-stu-id="8171e-106">It can be found at https://security.microsoft.com/securescore in the [Microsoft 365 security center](overview-security-center.md).</span></span>

<span data-ttu-id="8171e-107">Le suivi des recommandations de score de sécurité peut protéger votre organisation contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="8171e-107">Following the Secure Score recommendations can protect your organization from threats.</span></span> <span data-ttu-id="8171e-108">À partir d’un tableau de bord centralisé dans le centre de sécurité Microsoft 365, les organisations peuvent surveiller et gérer la sécurité des identités, des applications et des appareils Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8171e-108">From a centralized dashboard in the Microsoft 365 security center, organizations can monitor and work on the security of their Microsoft 365 identities, apps, and devices.</span></span>

<span data-ttu-id="8171e-109">Le score de sécurité aide les organisations :</span><span class="sxs-lookup"><span data-stu-id="8171e-109">Secure Score helps organizations:</span></span>  

* <span data-ttu-id="8171e-110">Rapport sur l’état actuel de l’état de sécurité de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="8171e-110">Report on the current state of the organization's security posture.</span></span>
* <span data-ttu-id="8171e-111">Améliorez la position de la sécurité en fournissant des possibilités de détectabilité, de visibilité, de conseils et de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8171e-111">Improve their security posture by providing discoverability, visibility, guidance, and control.</span></span>  
* <span data-ttu-id="8171e-112">Comparez avec des benchmarks et établissez des indicateurs de performance clés (KPI).</span><span class="sxs-lookup"><span data-stu-id="8171e-112">Compare with benchmarks and establish key performance indicators (KPIs).</span></span>

<span data-ttu-id="8171e-113">Les organisations ont accès à des visualisations robustes de mesures et tendances, à une intégration à d’autres produits Microsoft, à une comparaison de scores avec des organisations similaires, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="8171e-113">Organizations gain access to robust visualizations of metrics and trends, integration with other Microsoft products, score comparison with similar organizations, and much more.</span></span> <span data-ttu-id="8171e-114">Le score peut également indiquer quand les solutions tierces ont résolu les actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="8171e-114">The score can also reflect when third-party solutions have addressed recommended actions.</span></span>

![Page d’accueil du score sécurisé](../../media/secure-score/secure-score-homepage-new.png)

## <a name="how-it-works"></a><span data-ttu-id="8171e-116">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="8171e-116">How it works</span></span>

<span data-ttu-id="8171e-117">Vous disposez de points pour les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8171e-117">You're given points for the following actions:</span></span>

- <span data-ttu-id="8171e-118">Configuration des fonctionnalités de sécurité recommandées</span><span class="sxs-lookup"><span data-stu-id="8171e-118">Configuring recommended security features</span></span>
- <span data-ttu-id="8171e-119">Exécution de tâches liées à la sécurité</span><span class="sxs-lookup"><span data-stu-id="8171e-119">Performing security-related tasks</span></span>
- <span data-ttu-id="8171e-120">Gestion de l’action d’amélioration avec une application ou un logiciel tiers, ou une autre limitation</span><span class="sxs-lookup"><span data-stu-id="8171e-120">Addressing the improvement action with a third-party application or software, or an alternate mitigation</span></span>

<span data-ttu-id="8171e-121">Certaines actions d’amélioration ne donnent de points qu’une fois complètement terminé.</span><span class="sxs-lookup"><span data-stu-id="8171e-121">Some improvement actions only give points when fully completed.</span></span> <span data-ttu-id="8171e-122">Certains fournissent des points partiels s’ils sont terminés pour certains appareils ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8171e-122">Some give partial points if they're completed for some devices or users.</span></span> <span data-ttu-id="8171e-123">Si vous ne pouvez pas ou ne souhaitez pas arrêter une des actions d’amélioration, vous pouvez choisir d’accepter le risque ou le risque restant.</span><span class="sxs-lookup"><span data-stu-id="8171e-123">If you can't or don't want to enact one of the improvement actions, you can choose to accept the risk or remaining risk.</span></span>

<span data-ttu-id="8171e-124">Si vous disposez d’une licence pour l’un des produits Microsoft pris en charge, vous verrez des recommandations pour ces produits.</span><span class="sxs-lookup"><span data-stu-id="8171e-124">If you have a license for one of the supported Microsoft products, then you'll see recommendations for those products.</span></span> <span data-ttu-id="8171e-125">Nous vous montrons l’ensemble des améliorations possibles pour un produit, indépendamment de la licence Edition, abonnement ou plan.</span><span class="sxs-lookup"><span data-stu-id="8171e-125">We show you the full set of possible improvements for a product, regardless of license edition, subscription, or plan.</span></span> <span data-ttu-id="8171e-126">De cette manière, vous pouvez comprendre les meilleures pratiques en matière de sécurité et améliorer votre score.</span><span class="sxs-lookup"><span data-stu-id="8171e-126">This way, you can understand security best practices and improve your score.</span></span> <span data-ttu-id="8171e-127">Votre position absolue de sécurité, représentée par la fonction de chiffrement sécurisé, reste la même quelle que soit la licence de votre organisation pour un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="8171e-127">Your absolute security posture, represented by Secure Score, stays the same no matter what licenses your organization owns for a specific product.</span></span> <span data-ttu-id="8171e-128">N’oubliez pas que la sécurité doit être équilibrée avec la convivialité et que toutes les recommandations ne peuvent pas fonctionner pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8171e-128">Keep in mind that security should be balanced with usability, and not every recommendation can work for your environment.</span></span>

<span data-ttu-id="8171e-129">Votre score est mis à jour en temps réel afin de refléter les informations présentées dans les pages de l’action visualisations et amélioration.</span><span class="sxs-lookup"><span data-stu-id="8171e-129">Your score is updated in real time to reflect the information presented in the visualizations and improvement action pages.</span></span> <span data-ttu-id="8171e-130">Le score sécurisé est également synchronisé quotidiennement pour recevoir les données système relatives aux points obtenus pour chaque action.</span><span class="sxs-lookup"><span data-stu-id="8171e-130">Secure Score also syncs daily to receive system data about your achieved points for each action.</span></span>

### <a name="key-scenarios"></a><span data-ttu-id="8171e-131">Scénarios clés</span><span class="sxs-lookup"><span data-stu-id="8171e-131">Key scenarios</span></span>

- [<span data-ttu-id="8171e-132">Vérifier votre score actuel</span><span class="sxs-lookup"><span data-stu-id="8171e-132">Check your current score</span></span>](microsoft-secure-score-improvement-actions.md#check-your-current-score)
- [<span data-ttu-id="8171e-133">Comparez votre score aux organisations comme la vôtre</span><span class="sxs-lookup"><span data-stu-id="8171e-133">Compare your score to organizations like yours</span></span>](microsoft-secure-score-history-metrics-trends.md#compare-your-score-to-organizations-like-yours)
- [<span data-ttu-id="8171e-134">Afficher les actions d’amélioration et décider d’un plan d’action</span><span class="sxs-lookup"><span data-stu-id="8171e-134">View improvement actions and decide an action plan</span></span>](microsoft-secure-score-improvement-actions.md#take-action-to-improve-your-score)
- [<span data-ttu-id="8171e-135">Initier des flux de travail pour enquêter ou implémenter</span><span class="sxs-lookup"><span data-stu-id="8171e-135">Initiate work flows to investigate or implement</span></span>](microsoft-secure-score-improvement-actions.md#view-improvement-action-details)
    - [<span data-ttu-id="8171e-136">Centre de sécurité Microsoft 365 et intégration ServiceNow</span><span class="sxs-lookup"><span data-stu-id="8171e-136">Microsoft 365 security center and ServiceNow integration</span></span>](tickets-security-center.md)

### <a name="how-improvement-actions-are-scored"></a><span data-ttu-id="8171e-137">Comment les actions d’amélioration sont évaluées</span><span class="sxs-lookup"><span data-stu-id="8171e-137">How improvement actions are scored</span></span>

<span data-ttu-id="8171e-138">Chaque action d’amélioration vaut 10 points maximum, et la plupart d’entre elles sont évaluées de manière binaire.</span><span class="sxs-lookup"><span data-stu-id="8171e-138">Each improvement action is worth 10 points or less, and most are scored in a binary fashion.</span></span> <span data-ttu-id="8171e-139">Si vous implémentez l’action d’amélioration, par exemple créer une nouvelle stratégie ou activer un paramètre spécifique, vous obtenez 100% des points.</span><span class="sxs-lookup"><span data-stu-id="8171e-139">If you implement the improvement action, like create a new policy or turn on a specific setting, you get 100% of the points.</span></span> <span data-ttu-id="8171e-140">Pour les autres actions d’amélioration, les points sont fournis sous la forme d’un pourcentage de la configuration totale.</span><span class="sxs-lookup"><span data-stu-id="8171e-140">For other improvement actions, points are given as a percentage of the total configuration.</span></span>

<span data-ttu-id="8171e-141">Par exemple, une action d’amélioration vous indique 10 points en protégeant tous vos utilisateurs à l’aide de l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="8171e-141">For example, an improvement action states you get 10 points by protecting all your users with multi-factor authentication.</span></span> <span data-ttu-id="8171e-142">Vous ne disposez que de 50 de 100 total d’utilisateurs protégés, vous obtiendrez un score partiel de 5 points (50 protégé/100 au total \* 10 pts max = 5 pts).</span><span class="sxs-lookup"><span data-stu-id="8171e-142">You only have 50 of 100 total users protected, so you'd get a partial score of 5 points (50 protected / 100 total \* 10 max pts = 5 pts).</span></span>

### <a name="products-included-in-secure-score"></a><span data-ttu-id="8171e-143">Produits inclus dans le score de sécurité</span><span class="sxs-lookup"><span data-stu-id="8171e-143">Products included in Secure Score</span></span>

<span data-ttu-id="8171e-144">Il existe actuellement des recommandations pour Microsoft 365 (y compris Exchange Online), Azure Active Directory, Microsoft Defender for Endpoint, Microsoft Defender for Identity et Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="8171e-144">Currently there are recommendations for Microsoft 365 (including Exchange Online), Azure Active Directory, Microsoft Defender for Endpoint, Microsoft Defender for Identity, and Cloud App Security.</span></span> <span data-ttu-id="8171e-145">Des recommandations pour d’autres produits de sécurité seront bientôt disponibles.</span><span class="sxs-lookup"><span data-stu-id="8171e-145">Recommendations for other security products are coming soon.</span></span> <span data-ttu-id="8171e-146">Les recommandations ne couvrent pas toutes les surfaces d’attaque associées à chaque produit, mais elles sont de bonnes bases.</span><span class="sxs-lookup"><span data-stu-id="8171e-146">The recommendations won't cover all the attack surfaces associated with each product, but they're a good baseline.</span></span> <span data-ttu-id="8171e-147">Vous pouvez également marquer les actions d’amélioration telles qu’elles sont couvertes par une atténuation tierce ou alternative.</span><span class="sxs-lookup"><span data-stu-id="8171e-147">You can also mark the improvement actions as covered by a third party or alternate mitigation.</span></span>

### <a name="security-defaults"></a><span data-ttu-id="8171e-148">Paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="8171e-148">Security defaults</span></span>

<span data-ttu-id="8171e-149">Microsoft Secure score a mis à jour les actions d’amélioration afin de prendre en charge les paramètres de [sécurité par défaut dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), ce qui facilite la protection de votre organisation avec des paramètres de sécurité préconfigurés pour les attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="8171e-149">Microsoft Secure Score has updated improvement actions to support [security defaults in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), which make it easier to help protect your organization with preconfigured security settings for common attacks.</span></span>

<span data-ttu-id="8171e-150">Si vous activez les paramètres de sécurité par défaut, vous recevrez des points complets pour les actions d’amélioration suivantes :</span><span class="sxs-lookup"><span data-stu-id="8171e-150">If you turn on security defaults, you'll be awarded full points for the following improvement actions:</span></span>

- <span data-ttu-id="8171e-151">Assurez-vous que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé (9 points).</span><span class="sxs-lookup"><span data-stu-id="8171e-151">Ensure all users can complete multi-factor authentication for secure access (9 points)</span></span>
- <span data-ttu-id="8171e-152">Exiger MFA pour les rôles d’administration (10 points)</span><span class="sxs-lookup"><span data-stu-id="8171e-152">Require MFA for administrative roles (10 points)</span></span>
- <span data-ttu-id="8171e-153">Activer la stratégie pour bloquer l’authentification héritée (7 points)</span><span class="sxs-lookup"><span data-stu-id="8171e-153">Enable policy to block legacy authentication (7 points)</span></span>

>[!IMPORTANT]
><span data-ttu-id="8171e-154">Les paramètres de sécurité par défaut incluent des fonctionnalités de sécurité qui fournissent une sécurité similaire aux actions d’amélioration « stratégie de risque de connexion » et « stratégie de risque utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="8171e-154">Security defaults include security features that provide similar security to the "sign-in risk policy" and "user risk policy" improvement actions.</span></span> <span data-ttu-id="8171e-155">Au lieu de configurer ces stratégies en plus des paramètres de sécurité par défaut, nous vous recommandons de mettre à jour leurs statuts sur « résolu par une autre atténuation ».</span><span class="sxs-lookup"><span data-stu-id="8171e-155">Instead of setting up these policies on top of the security defaults, we recommend updating their statuses to "Resolved through alternative mitigation."</span></span>

## <a name="required-permissions"></a><span data-ttu-id="8171e-156">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="8171e-156">Required permissions</span></span>

<span data-ttu-id="8171e-157">Pour avoir l’autorisation d’accéder à la note de sécurité Microsoft, vous devez disposer de l’un des rôles suivants dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8171e-157">To have permission to access Microsoft Secure Score, you must be assigned one of the following roles in Azure Active Directory.</span></span>

### <a name="read-and-write-roles"></a><span data-ttu-id="8171e-158">Rôles de lecture et d’écriture</span><span class="sxs-lookup"><span data-stu-id="8171e-158">Read and write roles</span></span>

<span data-ttu-id="8171e-159">Avec l’accès en lecture et en écriture, vous pouvez effectuer des modifications et interagir directement avec le score de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8171e-159">With read and write access, you can make changes and directly interact with Secure Score.</span></span> <span data-ttu-id="8171e-160">Vous pouvez également attribuer un accès en lecture seule aux autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8171e-160">You can also assign read-only access to other users.</span></span>

* <span data-ttu-id="8171e-161">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="8171e-161">Global administrator</span></span>
* <span data-ttu-id="8171e-162">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="8171e-162">Security administrator</span></span>
* <span data-ttu-id="8171e-163">Administrateur Exchange</span><span class="sxs-lookup"><span data-stu-id="8171e-163">Exchange administrator</span></span>
* <span data-ttu-id="8171e-164">Administrateur SharePoint</span><span class="sxs-lookup"><span data-stu-id="8171e-164">SharePoint administrator</span></span>
* <span data-ttu-id="8171e-165">Administrateur de compte</span><span class="sxs-lookup"><span data-stu-id="8171e-165">Account administrator</span></span>

### <a name="read-only-roles"></a><span data-ttu-id="8171e-166">Rôles en lecture seule</span><span class="sxs-lookup"><span data-stu-id="8171e-166">Read-only roles</span></span>

<span data-ttu-id="8171e-167">Avec un accès en lecture seule, vous ne pouvez pas modifier le statut ou les notes pour une action d’amélioration, modifier des zones de score ou modifier des comparaisons personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8171e-167">With read-only access, you aren't able to edit status or notes for an improvement action, edit score zones, or edit custom comparisons.</span></span>

* <span data-ttu-id="8171e-168">Administrateur du support technique</span><span class="sxs-lookup"><span data-stu-id="8171e-168">Helpdesk administrator</span></span>
* <span data-ttu-id="8171e-169">Administrateur d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8171e-169">User administrator</span></span>
* <span data-ttu-id="8171e-170">Administrateur de service</span><span class="sxs-lookup"><span data-stu-id="8171e-170">Service administrator</span></span>
* <span data-ttu-id="8171e-171">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="8171e-171">Security reader</span></span>
* <span data-ttu-id="8171e-172">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="8171e-172">Security operator</span></span>
* <span data-ttu-id="8171e-173">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="8171e-173">Global reader</span></span>

## <a name="risk-awareness"></a><span data-ttu-id="8171e-174">Sensibilisation aux risques</span><span class="sxs-lookup"><span data-stu-id="8171e-174">Risk awareness</span></span>

<span data-ttu-id="8171e-175">Microsoft Secure score est un résumé numérique de votre position de sécurité basée sur les configurations système, le comportement de l’utilisateur et d’autres mesures liées à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="8171e-175">Microsoft Secure Score is a numerical summary of your security posture based on system configurations, user behavior, and other security-related measurements.</span></span> <span data-ttu-id="8171e-176">Il ne s’agit pas d’une mesure absolue de la probabilité de violation de votre système ou de vos données.</span><span class="sxs-lookup"><span data-stu-id="8171e-176">It isn't an absolute measurement of how likely your system or data will be breached.</span></span> <span data-ttu-id="8171e-177">Il représente plutôt la mesure dans laquelle vous avez adopté des contrôles de sécurité dans votre environnement Microsoft afin de compenser le risque d’être compromis.</span><span class="sxs-lookup"><span data-stu-id="8171e-177">Rather, it represents the extent to which you have adopted security controls in your Microsoft environment that can help offset the risk of being breached.</span></span> <span data-ttu-id="8171e-178">Aucun service en ligne n’est totalement immunisé contre les violations de sécurité et le score sécurisé ne doit pas être interprété comme une garantie d’une violation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8171e-178">No online service is completely immune from security breaches, and secure score shouldn't be interpreted as a guarantee against security breach in any manner.</span></span>

## <a name="we-want-to-hear-from-you"></a><span data-ttu-id="8171e-179">Votre avis nous intéresse</span><span class="sxs-lookup"><span data-stu-id="8171e-179">We want to hear from you</span></span>

<span data-ttu-id="8171e-180">Si vous rencontrez des problèmes, informez-le en publiant dans la communauté [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) .</span><span class="sxs-lookup"><span data-stu-id="8171e-180">If you have any issues, let us know by posting in the [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) community.</span></span> <span data-ttu-id="8171e-181">Nous Surveillez la communauté et vous fournirons de l’aide.</span><span class="sxs-lookup"><span data-stu-id="8171e-181">We're monitoring the community and will provide help.</span></span>

## <a name="related-resources"></a><span data-ttu-id="8171e-182">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8171e-182">Related resources</span></span>

- [<span data-ttu-id="8171e-183">Évaluez votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="8171e-183">Assess your security posture</span></span>](microsoft-secure-score-improvement-actions.md)
- [<span data-ttu-id="8171e-184">Suivi de votre historique de score sécurisé Microsoft et atteindre les objectifs</span><span class="sxs-lookup"><span data-stu-id="8171e-184">Track your Microsoft Secure Score history and meet goals</span></span>](microsoft-secure-score-history-metrics-trends.md)
- [<span data-ttu-id="8171e-185">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="8171e-185">What's coming</span></span>](microsoft-secure-score-whats-coming.md)
- [<span data-ttu-id="8171e-186">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="8171e-186">What's new</span></span>](microsoft-secure-score-whats-new.md)
