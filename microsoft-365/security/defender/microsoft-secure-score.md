---
title: Degré de sécurisation Microsoft
description: Décrit le niveau de sécurité Microsoft dans le Centre de sécurité Microsoft 365, comment améliorer votre posture de sécurité et ce à quoi les administrateurs de sécurité peuvent s’attendre.
keywords: score de sécurité Microsoft, score sécurisé, score de sécurité Office 365, score de sécurité Microsoft, centre de sécurité Microsoft 365, actions d’amélioration
ms.prod: m365-security
ms.mktglfcycl: deploy
localization_priority: Normal
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
ms.technology: m365d
ms.openlocfilehash: 98f335a38b2e4f581d4b08def39353e53e1bafd4
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064609"
---
# <a name="microsoft-secure-score"></a><span data-ttu-id="1b653-104">Niveau de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="1b653-104">Microsoft Secure Score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="1b653-105">Le Niveau de sécurité Microsoft est une mesure de la posture de sécurité d'une organisation, un chiffre plus élevé indiquant que davantage de mesures d'amélioration ont été prises.</span><span class="sxs-lookup"><span data-stu-id="1b653-105">Microsoft Secure Score is a measurement of an organization's security posture, with a higher number indicating more improvement actions taken.</span></span> <span data-ttu-id="1b653-106">Vous pouvez le trouver dans le Centre de sécurité https://security.microsoft.com/securescore [Microsoft 365.](overview-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="1b653-106">It can be found at https://security.microsoft.com/securescore in the [Microsoft 365 security center](overview-security-center.md).</span></span>

<span data-ttu-id="1b653-107">En suivant les recommandations du Niveau de sécurité, vous pouvez protéger votre organisation contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="1b653-107">Following the Secure Score recommendations can protect your organization from threats.</span></span> <span data-ttu-id="1b653-108">À partir d’un tableau de bord centralisé dans le Centre de sécurité Microsoft 365, les organisations peuvent surveiller et travailler sur la sécurité de leurs identités, applications et appareils Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1b653-108">From a centralized dashboard in the Microsoft 365 security center, organizations can monitor and work on the security of their Microsoft 365 identities, apps, and devices.</span></span>

<span data-ttu-id="1b653-109">Score sécurisé aide les organisations :</span><span class="sxs-lookup"><span data-stu-id="1b653-109">Secure Score helps organizations:</span></span>  

* <span data-ttu-id="1b653-110">Rapport sur l'état actuel de la posture de sécurité de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="1b653-110">Report on the current state of the organization's security posture.</span></span>
* <span data-ttu-id="1b653-111">Améliorer leur posture de sécurité en leur offrant des possibilités de découverte, de visibilité, de guide et de contrôle.</span><span class="sxs-lookup"><span data-stu-id="1b653-111">Improve their security posture by providing discoverability, visibility, guidance, and control.</span></span>  
* <span data-ttu-id="1b653-112">Comparer avec des critères de référence et établir des indicateurs de performance clés (KPI).</span><span class="sxs-lookup"><span data-stu-id="1b653-112">Compare with benchmarks and establish key performance indicators (KPIs).</span></span>

<span data-ttu-id="1b653-113">Les organisations ont accès à des visualisations robustes de mesures et de tendances, à l’intégration avec d’autres produits Microsoft, à la comparaison des scores avec des organisations similaires, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="1b653-113">Organizations gain access to robust visualizations of metrics and trends, integration with other Microsoft products, score comparison with similar organizations, and much more.</span></span> <span data-ttu-id="1b653-114">Le score peut également refléter le moment où des solutions tierces ont traité les actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="1b653-114">The score can also reflect when third-party solutions have addressed recommended actions.</span></span>

![Page d’accueil du score de sécurisation](../../media/secure-score/secure-score-homepage-new.png)

## <a name="how-it-works"></a><span data-ttu-id="1b653-116">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="1b653-116">How it works</span></span>

<span data-ttu-id="1b653-117">Vous avez des points pour les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b653-117">You're given points for the following actions:</span></span>

- <span data-ttu-id="1b653-118">Configuration des fonctionnalités de sécurité recommandées</span><span class="sxs-lookup"><span data-stu-id="1b653-118">Configuring recommended security features</span></span>
- <span data-ttu-id="1b653-119">Effectuer des tâches liées à la sécurité</span><span class="sxs-lookup"><span data-stu-id="1b653-119">Doing security-related tasks</span></span>
- <span data-ttu-id="1b653-120">Traitement de l’action d’amélioration avec une application ou un logiciel tiers, ou une autre atténuation</span><span class="sxs-lookup"><span data-stu-id="1b653-120">Addressing the improvement action with a third-party application or software, or an alternate mitigation</span></span>

<span data-ttu-id="1b653-121">Certaines actions d’amélioration donnent uniquement des points lorsqu’elles sont entièrement terminées.</span><span class="sxs-lookup"><span data-stu-id="1b653-121">Some improvement actions only give points when fully completed.</span></span> <span data-ttu-id="1b653-122">Certains donnent des points partiels s’ils sont terminés pour certains appareils ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1b653-122">Some give partial points if they're completed for some devices or users.</span></span> <span data-ttu-id="1b653-123">Si vous ne pouvez pas ou ne souhaitez pas mettre en place l’une des actions d’amélioration, vous pouvez choisir d’accepter le risque ou le risque restant.</span><span class="sxs-lookup"><span data-stu-id="1b653-123">If you can't or don't want to enact one of the improvement actions, you can choose to accept the risk or remaining risk.</span></span>

<span data-ttu-id="1b653-124">Si vous avez une licence pour l’un des produits Microsoft pris en charge, vous verrez des recommandations pour ces produits.</span><span class="sxs-lookup"><span data-stu-id="1b653-124">If you have a license for one of the supported Microsoft products, then you'll see recommendations for those products.</span></span> <span data-ttu-id="1b653-125">Nous vous montrons l’ensemble complet des améliorations possibles pour un produit, indépendamment de l’édition de licence, de l’abonnement ou de l’offre.</span><span class="sxs-lookup"><span data-stu-id="1b653-125">We show you the full set of possible improvements for a product, regardless of license edition, subscription, or plan.</span></span> <span data-ttu-id="1b653-126">Ainsi, vous pouvez comprendre les meilleures pratiques en matière de sécurité et améliorer votre score.</span><span class="sxs-lookup"><span data-stu-id="1b653-126">This way, you can understand security best practices and improve your score.</span></span> <span data-ttu-id="1b653-127">Votre posture de sécurité absolue, représentée par le niveau de sécurisation, reste la même quelle que soit la licence dont votre organisation est propriétaire pour un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="1b653-127">Your absolute security posture, represented by Secure Score, stays the same no matter what licenses your organization owns for a specific product.</span></span> <span data-ttu-id="1b653-128">N’oubliez pas que la sécurité et la convivialité doivent s’équilibrer, et certaines recommandations peuvent ne pas convenir à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="1b653-128">Keep in mind that security should be balanced with usability, and not every recommendation can work for your environment.</span></span>

<span data-ttu-id="1b653-129">Votre score est mis à jour en temps réel pour refléter les informations présentées dans les pages d’action d’amélioration et de visualisation.</span><span class="sxs-lookup"><span data-stu-id="1b653-129">Your score is updated in real time to reflect the information presented in the visualizations and improvement action pages.</span></span> <span data-ttu-id="1b653-130">Secure Score se synchronise également quotidiennement pour recevoir des données système sur vos points obtenus pour chaque action.</span><span class="sxs-lookup"><span data-stu-id="1b653-130">Secure Score also syncs daily to receive system data about your achieved points for each action.</span></span>

### <a name="key-scenarios"></a><span data-ttu-id="1b653-131">Scénarios clés</span><span class="sxs-lookup"><span data-stu-id="1b653-131">Key scenarios</span></span>

- [<span data-ttu-id="1b653-132">Vérifier votre score actuel</span><span class="sxs-lookup"><span data-stu-id="1b653-132">Check your current score</span></span>](microsoft-secure-score-improvement-actions.md#check-your-current-score)
- [<span data-ttu-id="1b653-133">Comparer votre score à des organisations telles que les vôtres</span><span class="sxs-lookup"><span data-stu-id="1b653-133">Compare your score to organizations like yours</span></span>](microsoft-secure-score-history-metrics-trends.md#compare-your-score-to-organizations-like-yours)
- [<span data-ttu-id="1b653-134">Afficher les actions d’amélioration et décider d’un plan d’action</span><span class="sxs-lookup"><span data-stu-id="1b653-134">View improvement actions and decide an action plan</span></span>](microsoft-secure-score-improvement-actions.md#take-action-to-improve-your-score)
- [<span data-ttu-id="1b653-135">Lancer des flux de travail pour examiner ou implémenter</span><span class="sxs-lookup"><span data-stu-id="1b653-135">Initiate work flows to investigate or implement</span></span>](microsoft-secure-score-improvement-actions.md#view-improvement-action-details)

### <a name="how-improvement-actions-are-scored"></a><span data-ttu-id="1b653-136">Comment les actions d’amélioration sont note es</span><span class="sxs-lookup"><span data-stu-id="1b653-136">How improvement actions are scored</span></span>

<span data-ttu-id="1b653-137">Chaque action d’amélioration vaut 10 points ou moins, et la plupart d’entre eux sont marqués de manière binaire.</span><span class="sxs-lookup"><span data-stu-id="1b653-137">Each improvement action is worth 10 points or less, and most are scored in a binary fashion.</span></span> <span data-ttu-id="1b653-138">Si vous implémentez l’action d’amélioration, comme créer une stratégie ou activer un paramètre spécifique, vous obtenez 100 % des points.</span><span class="sxs-lookup"><span data-stu-id="1b653-138">If you implement the improvement action, like create a new policy or turn on a specific setting, you get 100% of the points.</span></span> <span data-ttu-id="1b653-139">Pour les autres actions d’amélioration, les points sont donnés sous forme de pourcentage de la configuration totale.</span><span class="sxs-lookup"><span data-stu-id="1b653-139">For other improvement actions, points are given as a percentage of the total configuration.</span></span>

<span data-ttu-id="1b653-140">Par exemple, une action d’amélioration indique que vous obtenez 10 points en protégeant tous vos utilisateurs avec l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="1b653-140">For example, an improvement action states you get 10 points by protecting all your users with multi-factor authentication.</span></span> <span data-ttu-id="1b653-141">Vous n’avez que 50 utilisateurs sur 100 au total protégés. Vous obtenez donc un score partiel de 5 points (50 protégé / 100 au total \* 10 pts max = 5 pts).</span><span class="sxs-lookup"><span data-stu-id="1b653-141">You only have 50 of 100 total users protected, so you'd get a partial score of 5 points (50 protected / 100 total \* 10 max pts = 5 pts).</span></span>

### <a name="products-included-in-secure-score"></a><span data-ttu-id="1b653-142">Produits inclus dans secure score</span><span class="sxs-lookup"><span data-stu-id="1b653-142">Products included in Secure Score</span></span>

<span data-ttu-id="1b653-143">Il existe actuellement des recommandations pour les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="1b653-143">Currently there are recommendations for the following products:</span></span>

- <span data-ttu-id="1b653-144">Microsoft 365 (y compris Exchange Online)</span><span class="sxs-lookup"><span data-stu-id="1b653-144">Microsoft 365 (including Exchange Online)</span></span>
- <span data-ttu-id="1b653-145">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1b653-145">Azure Active Directory</span></span>
- <span data-ttu-id="1b653-146">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1b653-146">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="1b653-147">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="1b653-147">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="1b653-148">Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="1b653-148">Cloud App Security</span></span>
- <span data-ttu-id="1b653-149">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1b653-149">Microsoft Teams</span></span>

<span data-ttu-id="1b653-150">Des recommandations pour d’autres produits de sécurité seront bientôt ajoutées.</span><span class="sxs-lookup"><span data-stu-id="1b653-150">Recommendations for other security products are coming soon.</span></span> <span data-ttu-id="1b653-151">Les recommandations ne couvrent pas toutes les surfaces d’attaque associées à chaque produit, mais elles sont une bonne base de référence.</span><span class="sxs-lookup"><span data-stu-id="1b653-151">The recommendations won't cover all the attack surfaces associated with each product, but they're a good baseline.</span></span> <span data-ttu-id="1b653-152">Vous pouvez également marquer les actions d’amélioration comme couvertes par une solution tierce ou autre.</span><span class="sxs-lookup"><span data-stu-id="1b653-152">You can also mark the improvement actions as covered by a third party or alternate mitigation.</span></span>

### <a name="security-defaults"></a><span data-ttu-id="1b653-153">Paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="1b653-153">Security defaults</span></span>

<span data-ttu-id="1b653-154">Microsoft Secure Score a mis à jour les actions d’amélioration pour prendre en charge les paramètres de sécurité par défaut dans [Azure Active Directory,](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)ce qui facilite la protection de votre organisation avec des paramètres de sécurité pré-configurés pour les attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="1b653-154">Microsoft Secure Score has updated improvement actions to support [security defaults in Azure Active Directory](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), which make it easier to help protect your organization with pre-configured security settings for common attacks.</span></span>

<span data-ttu-id="1b653-155">Si vous allumez les paramètres de sécurité par défaut, des points complets vous seront attribués pour les actions d’amélioration suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b653-155">If you turn on security defaults, you'll be awarded full points for the following improvement actions:</span></span>

- <span data-ttu-id="1b653-156">S’assurer que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé (9 points)</span><span class="sxs-lookup"><span data-stu-id="1b653-156">Ensure all users can complete multi-factor authentication for secure access (9 points)</span></span>
- <span data-ttu-id="1b653-157">Exiger l’mf pour les rôles d’administration (10 points)</span><span class="sxs-lookup"><span data-stu-id="1b653-157">Require MFA for administrative roles (10 points)</span></span>
- <span data-ttu-id="1b653-158">Activer la stratégie pour bloquer l’authentification héritée (7 points)</span><span class="sxs-lookup"><span data-stu-id="1b653-158">Enable policy to block legacy authentication (7 points)</span></span>

>[!IMPORTANT]
><span data-ttu-id="1b653-159">Les valeurs par défaut de sécurité incluent des fonctionnalités de sécurité qui fournissent une sécurité similaire à la « stratégie de risque de la signature » et aux actions d’amélioration de la « stratégie de risque utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="1b653-159">Security defaults include security features that provide similar security to the "sign-in risk policy" and "user risk policy" improvement actions.</span></span> <span data-ttu-id="1b653-160">Au lieu de définir ces stratégies en plus des paramètres de sécurité par défaut, nous vous recommandons de mettre à jour leurs statuts sur « Résolu via une autre atténuation ».</span><span class="sxs-lookup"><span data-stu-id="1b653-160">Instead of setting up these policies on top of the security defaults, we recommend updating their statuses to "Resolved through alternative mitigation."</span></span>

## <a name="required-permissions"></a><span data-ttu-id="1b653-161">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="1b653-161">Required permissions</span></span>

<span data-ttu-id="1b653-162">Pour avoir l’autorisation d’accéder au service Score de sécurité Microsoft, vous devez avoir l’un des rôles suivants dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b653-162">To have permission to access Microsoft Secure Score, you must be assigned one of the following roles in Azure Active Directory.</span></span>

### <a name="read-and-write-roles"></a><span data-ttu-id="1b653-163">Lire et écrire des rôles</span><span class="sxs-lookup"><span data-stu-id="1b653-163">Read and write roles</span></span>

<span data-ttu-id="1b653-164">Avec l’accès en lecture et en écriture, vous pouvez apporter des modifications et interagir directement avec le score de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1b653-164">With read and write access, you can make changes and directly interact with Secure Score.</span></span> <span data-ttu-id="1b653-165">Vous pouvez également attribuer un accès en lecture seule à d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1b653-165">You can also assign read-only access to other users.</span></span>

* <span data-ttu-id="1b653-166">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="1b653-166">Global administrator</span></span>
* <span data-ttu-id="1b653-167">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="1b653-167">Security administrator</span></span>
* <span data-ttu-id="1b653-168">Administrateur Exchange</span><span class="sxs-lookup"><span data-stu-id="1b653-168">Exchange administrator</span></span>
* <span data-ttu-id="1b653-169">Administrateur SharePoint</span><span class="sxs-lookup"><span data-stu-id="1b653-169">SharePoint administrator</span></span>
* <span data-ttu-id="1b653-170">Administrateur de compte</span><span class="sxs-lookup"><span data-stu-id="1b653-170">Account administrator</span></span>

### <a name="read-only-roles"></a><span data-ttu-id="1b653-171">Rôles en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b653-171">Read-only roles</span></span>

<span data-ttu-id="1b653-172">Avec l’accès en lecture seule, vous ne pouvez pas modifier l’état ou les notes d’une action d’amélioration, modifier des zones de score ou modifier des comparaisons personnalisées.</span><span class="sxs-lookup"><span data-stu-id="1b653-172">With read-only access, you aren't able to edit status or notes for an improvement action, edit score zones, or edit custom comparisons.</span></span>

* <span data-ttu-id="1b653-173">Administrateur du support technique</span><span class="sxs-lookup"><span data-stu-id="1b653-173">Helpdesk administrator</span></span>
* <span data-ttu-id="1b653-174">Administrateur d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1b653-174">User administrator</span></span>
* <span data-ttu-id="1b653-175">Administrateur de service</span><span class="sxs-lookup"><span data-stu-id="1b653-175">Service administrator</span></span>
* <span data-ttu-id="1b653-176">Lecteur Sécurité</span><span class="sxs-lookup"><span data-stu-id="1b653-176">Security reader</span></span>
* <span data-ttu-id="1b653-177">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="1b653-177">Security operator</span></span>
* <span data-ttu-id="1b653-178">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="1b653-178">Global reader</span></span>

## <a name="risk-awareness"></a><span data-ttu-id="1b653-179">Sensibilisation aux risques</span><span class="sxs-lookup"><span data-stu-id="1b653-179">Risk awareness</span></span>

<span data-ttu-id="1b653-180">Le score de sécurité Microsoft est un résumé numérique de votre posture de sécurité en fonction des configurations système, du comportement des utilisateurs et d’autres mesures liées à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1b653-180">Microsoft Secure Score is a numerical summary of your security posture based on system configurations, user behavior, and other security-related measurements.</span></span> <span data-ttu-id="1b653-181">Il ne s’agit pas d’une mesure absolue du risque de violation de votre système ou de vos données.</span><span class="sxs-lookup"><span data-stu-id="1b653-181">It isn't an absolute measurement of how likely your system or data will be breached.</span></span> <span data-ttu-id="1b653-182">Au lieu de cela, il représente la mesure dans laquelle vous avez adopté des contrôles de sécurité dans votre environnement Microsoft qui peuvent vous aider à compenser le risque de violation.</span><span class="sxs-lookup"><span data-stu-id="1b653-182">Rather, it represents the extent to which you have adopted security controls in your Microsoft environment that can help offset the risk of being breached.</span></span> <span data-ttu-id="1b653-183">Aucun service en ligne n’est contre les violations de sécurité et le score sécurisé ne doit pas être interprété comme une garantie contre les violations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1b653-183">No online service is immune from security breaches, and secure score shouldn't be interpreted as a guarantee against security breach in any manner.</span></span>

## <a name="we-want-to-hear-from-you"></a><span data-ttu-id="1b653-184">Votre avis nous intéresse</span><span class="sxs-lookup"><span data-stu-id="1b653-184">We want to hear from you</span></span>

<span data-ttu-id="1b653-185">Si vous avez des problèmes, faites-le nous savoir en publiant dans la communauté sécurité, confidentialité [& conformité.](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy)</span><span class="sxs-lookup"><span data-stu-id="1b653-185">If you have any issues, let us know by posting in the [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) community.</span></span> <span data-ttu-id="1b653-186">Nous surveillons la communauté et fournirons de l’aide.</span><span class="sxs-lookup"><span data-stu-id="1b653-186">We're monitoring the community and will provide help.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1b653-187">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1b653-187">Related resources</span></span>

- [<span data-ttu-id="1b653-188">Évaluez votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="1b653-188">Assess your security posture</span></span>](microsoft-secure-score-improvement-actions.md)
- [<span data-ttu-id="1b653-189">Suivre votre historique du Score de sécurité Microsoft et atteindre les objectifs</span><span class="sxs-lookup"><span data-stu-id="1b653-189">Track your Microsoft Secure Score history and meet goals</span></span>](microsoft-secure-score-history-metrics-trends.md)
- [<span data-ttu-id="1b653-190">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="1b653-190">What's coming</span></span>](microsoft-secure-score-whats-coming.md)
- [<span data-ttu-id="1b653-191">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="1b653-191">What's new</span></span>](microsoft-secure-score-whats-new.md)