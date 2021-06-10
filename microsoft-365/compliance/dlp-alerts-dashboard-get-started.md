---
title: Prise en main du tableau de bord des alertes de protection contre la perte de données
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MET150
ms.custom:
- seo-marvel-apr2020
description: Prise en charge de la définition et de la gestion des alertes pour les stratégies de protection contre la perte de données.
ms.openlocfilehash: ad117eb0c5460b90c92c664f0c233b81d1882327
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843865"
---
# <a name="get-started-with-the-data-loss-prevention-alert-dashboard"></a><span data-ttu-id="379f4-103">Prise en main du tableau de bord des alertes de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="379f4-103">Get started with the data loss prevention alert dashboard</span></span>

<span data-ttu-id="379f4-104">Les stratégies de protection contre la perte de données (DLP) peuvent prendre des mesures de protection pour empêcher le partage involontaire d’éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="379f4-104">Data loss prevention (DLP) policies can take protective actions to prevent unintentional sharing of sensitive items.</span></span> <span data-ttu-id="379f4-105">Lorsqu’une action est prise sur un élément sensible, vous pouvez être averti en configurant des alertes pour DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-105">When an action is taken on a sensitive item, you can be notified by configuring alerts for DLP.</span></span> <span data-ttu-id="379f4-106">Cet article vous montre comment définir des stratégies d’alerte enrichies liées à vos stratégies de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="379f4-106">This article shows you how to define rich alert policies that are linked to your data loss prevention (DLP) policies.</span></span> <span data-ttu-id="379f4-107">Vous verrez comment utiliser le tableau de bord de gestion des alertes [DLP](https://compliance.microsoft.com/datalossprevention?viewid=dlpalerts) dans le centre de conformité [Microsoft 365](https://compliance.microsoft.com/) pour afficher les alertes, les événements et les métadonnées associées pour les violations de stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-107">You'll see how to use the [DLP alert management dashboard](https://compliance.microsoft.com/datalossprevention?viewid=dlpalerts) in the [Microsoft 365 compliance center](https://compliance.microsoft.com/) to view alerts, events, and associated metadata for DLP policy violations.</span></span>

<span data-ttu-id="379f4-108">Si vous débutez avec les alertes DLP, vous devez consulter le tableau de bord des alertes de protection [contre la perte de données.](dlp-alerts-dashboard-learn.md)</span><span class="sxs-lookup"><span data-stu-id="379f4-108">If you are new to DLP alerts, you should review [Learn about the data loss prevention alerts dashboard](dlp-alerts-dashboard-learn.md)</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="379f4-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="379f4-109">Before you begin</span></span>

<span data-ttu-id="379f4-110">Avant de commencer, assurez-vous que vous avez les conditions préalables nécessaires :</span><span class="sxs-lookup"><span data-stu-id="379f4-110">Before you begin, make sure you have the necessary prerequisites:</span></span>

-   <span data-ttu-id="379f4-111">Licences pour le tableau de bord de gestion des alertes DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-111">Licensing for the DLP alerts management dashboard</span></span>
-   <span data-ttu-id="379f4-112">Gestion des licences pour les options de configuration des alertes</span><span class="sxs-lookup"><span data-stu-id="379f4-112">Licensing for alert configuration options</span></span>
-   <span data-ttu-id="379f4-113">Rôles</span><span class="sxs-lookup"><span data-stu-id="379f4-113">Roles</span></span>

### <a name="licensing-for-the-dlp-alert-management-dashboard"></a><span data-ttu-id="379f4-114">Licences pour le tableau de bord de gestion des alertes DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-114">Licensing for the DLP alert management dashboard</span></span>

<span data-ttu-id="379f4-115">Tous les locataires éligibles pour Office 365 DLP peuvent accéder au tableau de bord de gestion des alertes DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-115">All eligible tenants for Office 365 DLP can access the DLP alert management dashboard.</span></span> <span data-ttu-id="379f4-116">Pour commencer, vous devez être éligible à la Office 365 DLP pour Exchange Online, SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="379f4-116">To get started, you should be eligible for Office 365 DLP for Exchange Online, SharePoint Online, and OneDrive for Business.</span></span> <span data-ttu-id="379f4-117">Pour plus d’informations sur les conditions de licence requises pour Office 365 DLP, voir [quelles licences](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#which-licenses-provide-the-rights-for-a-user-to-benefit-from-the-service-16)fournissent les droits d’un utilisateur pour bénéficier du service ? .</span><span class="sxs-lookup"><span data-stu-id="379f4-117">For more information about the licensing requirements for Office 365 DLP, see [Which licenses provide the rights for a user to benefit from the service?](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#which-licenses-provide-the-rights-for-a-user-to-benefit-from-the-service-16).</span></span>

<span data-ttu-id="379f4-118">Les clients qui utilisent le point de terminaison [DLP](endpoint-dlp-learn-about.md) éligibles pour [Teams DLP](dlp-microsoft-teams.md) voient leurs alertes de stratégie DLP de point de terminaison et les alertes de stratégie Teams DLP dans le tableau de bord de gestion des alertes DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-118">Customers who use [Endpoint DLP](endpoint-dlp-learn-about.md) who are eligible for [Teams DLP](dlp-microsoft-teams.md) will see their endpoint DLP policy alerts and Teams DLP policy alerts in the DLP alert management dashboard.</span></span>

<span data-ttu-id="379f4-119">La **fonctionnalité d’aperçu** de contenu est disponible uniquement pour les licences ci-après :</span><span class="sxs-lookup"><span data-stu-id="379f4-119">The **content preview** feature is available only for these licenses:</span></span>

- <span data-ttu-id="379f4-120">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="379f4-120">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="379f4-121">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="379f4-121">Office 365 (E5)</span></span>
- <span data-ttu-id="379f4-122">Ajout de la conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="379f4-122">Advanced Compliance (E5) add on</span></span>
- <span data-ttu-id="379f4-123">Microsoft 365 E5/A5 Information Protection and Governance</span><span class="sxs-lookup"><span data-stu-id="379f4-123">Microsoft 365 E5/A5 Information Protection and Governance</span></span>
- <span data-ttu-id="379f4-124">Conformité microsft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="379f4-124">Microsft 365 E5/A5 Compliance</span></span>

### <a name="licensing-for-alert-configuration-options"></a><span data-ttu-id="379f4-125">Gestion des licences pour les options de configuration des alertes</span><span class="sxs-lookup"><span data-stu-id="379f4-125">Licensing for alert configuration options</span></span>

<span data-ttu-id="379f4-126">**Configuration** d’alerte à événement unique : les organisations qui ont un abonnement E1, F1 ou G1 ou un abonnement E3 ou G3 peuvent créer des stratégies d’alerte uniquement lorsqu’une alerte est déclenchée chaque fois qu’une activité se produit.</span><span class="sxs-lookup"><span data-stu-id="379f4-126">**Single-event alert configuration**: Organizations that have an E1, F1, or G1 subscription or an E3 or G3 subscription can create alert policies only where an alert is triggered every time an activity occurs.</span></span>

<span data-ttu-id="379f4-127">**Configuration d’alerte agrégée**: pour configurer des stratégies d’alerte agrégées basées sur un seuil, vous devez avoir l’une de ces configurations de licence :</span><span class="sxs-lookup"><span data-stu-id="379f4-127">**Aggregated alert configuration**: To configure aggregate alert policies based on a threshold, you must one of these licensing configurations:</span></span>

- <span data-ttu-id="379f4-128">Un abonnement E5 ou G5</span><span class="sxs-lookup"><span data-stu-id="379f4-128">An E5 or G5 subscription</span></span>
- <span data-ttu-id="379f4-129">Un abonnement E1, F1 ou G1 ou E3 ou G3 qui inclut l’une des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="379f4-129">An E1, F1, or G1 subscription or an E3 or G3 subscription that includes one of the following features:</span></span>
    - <span data-ttu-id="379f4-130">Office 365 – Protection avancée contre les menaces Plan 2</span><span class="sxs-lookup"><span data-stu-id="379f4-130">Office 365 Advanced Threat Protection Plan 2</span></span>
    - <span data-ttu-id="379f4-131">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="379f4-131">Microsoft 365 E5 Compliance</span></span>
    - <span data-ttu-id="379f4-132">Microsoft 365 licence de modules de découverte électronique et d’audit</span><span class="sxs-lookup"><span data-stu-id="379f4-132">Microsoft 365 eDiscovery and Audit add-on license</span></span>

### <a name="roles"></a><span data-ttu-id="379f4-133">Rôles</span><span class="sxs-lookup"><span data-stu-id="379f4-133">Roles</span></span>


<span data-ttu-id="379f4-134">Si vous souhaitez afficher le tableau de bord de gestion des alertes DLP ou modifier les options de configuration des alertes dans une stratégie DLP, vous devez être membre de l’un de ces groupes de rôles :</span><span class="sxs-lookup"><span data-stu-id="379f4-134">If you want to view the DLP alert management dashboard or to edit the alert configuration options in a DLP policy, you must be a member of one of these role groups:</span></span>

- <span data-ttu-id="379f4-135">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="379f4-135">Compliance Administrator</span></span>
- <span data-ttu-id="379f4-136">Administrateur de données de conformité</span><span class="sxs-lookup"><span data-stu-id="379f4-136">Compliance Data Administrator</span></span>
- <span data-ttu-id="379f4-137">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="379f4-137">Security Administrator</span></span>
- <span data-ttu-id="379f4-138">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="379f4-138">Security Operator</span></span>
- <span data-ttu-id="379f4-139">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="379f4-139">Security Reader</span></span>

<span data-ttu-id="379f4-140">Pour accéder au tableau de bord de gestion des alertes DLP, vous devez :</span><span class="sxs-lookup"><span data-stu-id="379f4-140">To access the DLP alert management dashboard, you need the:</span></span>

- <span data-ttu-id="379f4-141">Gérer des alertes</span><span class="sxs-lookup"><span data-stu-id="379f4-141">Manage alerts</span></span>

<span data-ttu-id="379f4-142">et l’un de ces deux rôles :</span><span class="sxs-lookup"><span data-stu-id="379f4-142">and either of these two roles:</span></span>

- <span data-ttu-id="379f4-143">Gestion de la conformité DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-143">DLP Compliance Management</span></span>
- <span data-ttu-id="379f4-144">View-Only de conformité DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-144">View-Only DLP Compliance Management</span></span>

<span data-ttu-id="379f4-145">Pour accéder à la fonctionnalité d’aperçu de contenu et aux fonctionnalités de contexte et de contenu sensibles mis en correspondance, vous devez être membre des éléments :</span><span class="sxs-lookup"><span data-stu-id="379f4-145">To access the Content preview feature and the Matched sensitive content and context features you must be a member of:</span></span>

- <span data-ttu-id="379f4-146">Groupe de rôles Visionneuse de contenu de l’Explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="379f4-146">Content Explorer Content Viewer role group</span></span>

<span data-ttu-id="379f4-147">dont le rôle visionneuse de contenu de classification des données est pré-attribué.</span><span class="sxs-lookup"><span data-stu-id="379f4-147">which has the data classification content viewer role pre-assigned.</span></span>

## <a name="dlp-alert-configuration"></a><span data-ttu-id="379f4-148">Configuration des alertes DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-148">DLP alert configuration</span></span>

<span data-ttu-id="379f4-149">Pour savoir comment configurer une alerte dans votre stratégie DLP, consultez l’exemple par où commencer avec la protection [contre la perte de données.](create-test-tune-dlp-policy.md#where-to-start-with-data-loss-prevention)</span><span class="sxs-lookup"><span data-stu-id="379f4-149">To learn how to configure an alert in your DLP policy, see [Where to start with data loss prevention](create-test-tune-dlp-policy.md#where-to-start-with-data-loss-prevention).</span></span>

### <a name="aggregate-event-alert-configuration"></a><span data-ttu-id="379f4-150">Configuration agrégée des alertes d’événements</span><span class="sxs-lookup"><span data-stu-id="379f4-150">Aggregate event alert configuration</span></span>

<span data-ttu-id="379f4-151">Si votre organisation est titulaire d’une licence pour les options de configuration d’alerte agrégées, ces [options](#licensing-for-alert-configuration-options)s’offrent à vous lorsque vous créez ou modifiez une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-151">If your org is licensed for [aggregated alert configuration options](#licensing-for-alert-configuration-options), then you'll see these options when you create or edit a DLP policy.</span></span>

:::image type="content" source="../media/incident-reports-options-aggregated-alerts.png" alt-text="Capture d’écran montrant les options des rapports d’incident pour les utilisateurs éligibles pour les options de configuration d’alerte agrégées." border="false":::

<span data-ttu-id="379f4-153">Cette configuration vous permet de configurer une stratégie pour générer une alerte chaque fois qu’une activité correspond aux conditions de la stratégie ou lorsqu’un certain seuil est dépassé, en fonction du nombre d’activités ou du volume de données exfiltrées.</span><span class="sxs-lookup"><span data-stu-id="379f4-153">This configuration allows you to set up a policy to generate an alert every time an activity matches the policy conditions or when a certain threshold is exceeded, based on the number of activities or based on the volume of exfiltrated data.</span></span>

### <a name="single-event-alert-configuration"></a><span data-ttu-id="379f4-154">Configuration d’alerte d’événement unique</span><span class="sxs-lookup"><span data-stu-id="379f4-154">Single event alert configuration</span></span>

<span data-ttu-id="379f4-155">Si votre organisation est titulaire d’une licence pour les options de configuration d’alerte à événement unique, ces [options](#licensing-for-alert-configuration-options)s’offrent à vous lorsque vous créez ou modifiez une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-155">If your org is licensed for [single-event alert configuration options](#licensing-for-alert-configuration-options), then you'll see these options when you create or edit a DLP policy.</span></span> <span data-ttu-id="379f4-156">Utilisez cette option pour créer une alerte qui se produit chaque fois qu’une correspondance de règle DLP se produit.</span><span class="sxs-lookup"><span data-stu-id="379f4-156">Use this option to create an alert that's raised every time a DLP rule match happens.</span></span>

:::image type="content" source="../media/incident-reports-options-single-event-alerts.png" alt-text="Capture d’écran montrant les options des rapports d’incident pour les utilisateurs éligibles pour les options de configuration d’alerte à événement unique." border="false":::

## <a name="investigate-a-dlp-alert"></a><span data-ttu-id="379f4-158">Examiner une alerte DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-158">Investigate a DLP alert</span></span>

<span data-ttu-id="379f4-159">Pour travailler avec le tableau de bord de gestion des alertes DLP :</span><span class="sxs-lookup"><span data-stu-id="379f4-159">To work with the DLP alert management dashboard:</span></span>

1. <span data-ttu-id="379f4-160">Dans le centre [Microsoft 365 conformité,](https://www.compliance.microsoft.com)allez à **Protection contre la perte de données.**</span><span class="sxs-lookup"><span data-stu-id="379f4-160">In the [Microsoft 365 compliance center](https://www.compliance.microsoft.com), go to **Data Loss Prevention**.</span></span>
2. <span data-ttu-id="379f4-161">Sélectionnez **l’onglet Alertes** pour afficher le tableau de bord des alertes DLP.</span><span class="sxs-lookup"><span data-stu-id="379f4-161">Select the **Alerts** tab to view the DLP alerts dashboard.</span></span>
3. <span data-ttu-id="379f4-162">Sélectionnez une alerte pour voir les détails :</span><span class="sxs-lookup"><span data-stu-id="379f4-162">Select an alert to see details:</span></span>

:::image type="content" source="../media/alert-details.png" alt-text="Capture d’écran montrant les détails de l’alerte dans le tableau de bord de gestion des alertes DLP." border="false":::

4. <span data-ttu-id="379f4-164">Sélectionnez **l’onglet** Événements pour afficher tous les événements associés à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="379f4-164">Select the **Events** tab to view all of the events associated with the alert.</span></span> <span data-ttu-id="379f4-165">Vous pouvez choisir un événement particulier pour afficher ses détails.</span><span class="sxs-lookup"><span data-stu-id="379f4-165">You can choose a particular event to view its details.</span></span> <span data-ttu-id="379f4-166">Pour obtenir la liste de certains détails sur les événements disponibles, voir le tableau de bord Alertes de protection contre la perte [de données.](dlp-alerts-dashboard-learn.md)</span><span class="sxs-lookup"><span data-stu-id="379f4-166">For a list of some of the available event details, see, [Learn about the data loss prevention Alerts dashboard](dlp-alerts-dashboard-learn.md).</span></span>
5. <span data-ttu-id="379f4-167">Sélectionnez **Détails** pour ouvrir la page **Vue d’ensemble** de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="379f4-167">Select **Details** to open the **Overview** page for the alert.</span></span> <span data-ttu-id="379f4-168">La page vue d’ensemble fournit un résumé :</span><span class="sxs-lookup"><span data-stu-id="379f4-168">The overview page provides a summary:</span></span>
    1. <span data-ttu-id="379f4-169">de ce qui s’est passé</span><span class="sxs-lookup"><span data-stu-id="379f4-169">of what happened</span></span>
    1. <span data-ttu-id="379f4-170">qui a effectué les actions à l’origine de la correspondance de stratégie</span><span class="sxs-lookup"><span data-stu-id="379f4-170">who performed the actions that caused the policy match</span></span>
    1. <span data-ttu-id="379f4-171">informations sur la stratégie de correspondance, et plus encore</span><span class="sxs-lookup"><span data-stu-id="379f4-171">information about the matched policy, and more</span></span> 

6. <span data-ttu-id="379f4-172">Sélectionnez **l’onglet Événements** pour accéder aux :</span><span class="sxs-lookup"><span data-stu-id="379f4-172">Choose the **Events** tab to access the:</span></span>
    1. <span data-ttu-id="379f4-173">contenu impliqué</span><span class="sxs-lookup"><span data-stu-id="379f4-173">content involved</span></span>
    1. <span data-ttu-id="379f4-174">types d’informations sensibles qui correspondent</span><span class="sxs-lookup"><span data-stu-id="379f4-174">sensitive information types matched</span></span>
    1. <span data-ttu-id="379f4-175">métadonnées</span><span class="sxs-lookup"><span data-stu-id="379f4-175">metadata</span></span>

7. <span data-ttu-id="379f4-176">Sélectionnez **l’onglet Types d’informations** sensibles pour afficher les détails sur les types d’informations sensibles détectés dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="379f4-176">Select the **Sensitive Info Types** tab to view details about the sensitive information types detected in the content.</span></span> <span data-ttu-id="379f4-177">Les détails incluent la confiance, le nombre et le contenu qui correspond au type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="379f4-177">Details include confidence, count, and the content that matches the sensitive information type.</span></span>

8. <span data-ttu-id="379f4-178">Après avoir examiné l’alerte, revenir à l’onglet Vue d’ensemble où vous pouvez gérer le triage, gérer la disposition de l’alerte et ajouter des commentaires. </span><span class="sxs-lookup"><span data-stu-id="379f4-178">After you investigate the alert, return to the **Overview** tab where you can manage triage and manage the disposition of the alert and add comments.</span></span>

- <span data-ttu-id="379f4-179">Pour consulter l’historique de la gestion des flux de travail, sélectionnez **Journal de gestion.**</span><span class="sxs-lookup"><span data-stu-id="379f4-179">To see the history of workflow management, choose **Management log**.</span></span>
- <span data-ttu-id="379f4-180">Une fois que vous avez pris l’action requise pour l’alerte, définissez l’état de l’alerte **sur Résolu.**</span><span class="sxs-lookup"><span data-stu-id="379f4-180">After you take the required action for the alert, set the status of the alert to **Resolved**.</span></span>

## <a name="see-also"></a><span data-ttu-id="379f4-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="379f4-181">See also</span></span>

- [<span data-ttu-id="379f4-182">En savoir plus sur les alertes de protection contre la perte de données et le tableau de bord des alertes</span><span class="sxs-lookup"><span data-stu-id="379f4-182">Learn about data loss prevention alerts and the alerts dashboard</span></span>](dlp-alerts-dashboard-learn.md)
- [<span data-ttu-id="379f4-183">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="379f4-183">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)