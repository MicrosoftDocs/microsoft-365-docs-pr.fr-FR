---
title: Corriger les vulnérabilités avec la gestion des menaces et des vulnérabilités
description: Corriger les faiblesses de sécurité découvertes par le biais de recommandations de sécurité et créer des exceptions si nécessaire, dans la gestion des menaces et des vulnérabilités.
keywords: correction tvm microsoft defender atp, tvm mdatp, gestion des menaces et des vulnérabilités, gestion des vulnérabilités des menaces &, correction de la gestion des vulnérabilités des menaces &, correction tvm intune, sccm de correction tvm
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 0a0f70d81c3060f14f917cac49851af2e9dae210
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51068686"
---
# <a name="remediate-vulnerabilities-with-threat-and-vulnerability-management"></a><span data-ttu-id="924c5-104">Corriger les vulnérabilités avec la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="924c5-104">Remediate vulnerabilities with threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="924c5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="924c5-105">**Applies to:**</span></span>
- [<span data-ttu-id="924c5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="924c5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="924c5-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="924c5-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="924c5-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924c5-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="924c5-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="924c5-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="924c5-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="924c5-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

## <a name="request-remediation"></a><span data-ttu-id="924c5-111">Demander la correction</span><span class="sxs-lookup"><span data-stu-id="924c5-111">Request remediation</span></span>

<span data-ttu-id="924c5-112">La fonctionnalité de gestion des menaces et des vulnérabilités dans Microsoft Defender pour point de terminaison fait le lien entre la sécurité et les administrateurs informatiques via le flux de travail de demande de correction.</span><span class="sxs-lookup"><span data-stu-id="924c5-112">The threat and vulnerability management capability in Microsoft Defender for Endpoint bridges the gap between Security and IT administrators through the remediation request workflow.</span></span> <span data-ttu-id="924c5-113">Les administrateurs de sécurité comme vous pouvez demander à l’administrateur informatique de corriger une vulnérabilité à partir des **pages** de recommandations de sécurité vers Intune.</span><span class="sxs-lookup"><span data-stu-id="924c5-113">Security admins like you can request for the IT Administrator to remediate a vulnerability from the **Security recommendation** pages to Intune.</span></span>

### <a name="enable-microsoft-intune-connection"></a><span data-ttu-id="924c5-114">Activer la connexion Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="924c5-114">Enable Microsoft Intune connection</span></span>

<span data-ttu-id="924c5-115">Pour utiliser cette fonctionnalité, activez vos connexions Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="924c5-115">To use this capability, enable your Microsoft Intune connections.</span></span> <span data-ttu-id="924c5-116">Dans le Centre de sécurité Microsoft Defender, accédez aux **fonctionnalités générales**  >    >  **avancées des paramètres.**</span><span class="sxs-lookup"><span data-stu-id="924c5-116">In the Microsoft Defender Security Center, navigate to **Settings** > **General** > **Advanced features**.</span></span> <span data-ttu-id="924c5-117">Faites défiler vers le bas et **recherchez la connexion Microsoft Intune.**</span><span class="sxs-lookup"><span data-stu-id="924c5-117">Scroll down and look for **Microsoft Intune connection**.</span></span> <span data-ttu-id="924c5-118">Par défaut, le basculement est désactivé.</span><span class="sxs-lookup"><span data-stu-id="924c5-118">By default, the toggle is turned off.</span></span> <span data-ttu-id="924c5-119">Activer votre **connexion Microsoft Intune.** </span><span class="sxs-lookup"><span data-stu-id="924c5-119">Turn your **Microsoft Intune connection** toggle **On**.</span></span>

<span data-ttu-id="924c5-120">**Remarque**: si la connexion Intune est activée, vous pouvez créer une tâche de sécurité Intune lors de la création d’une demande de correction.</span><span class="sxs-lookup"><span data-stu-id="924c5-120">**Note**: If you have the Intune connection enabled, you get an option to create an Intune security task when creating a remediation request.</span></span> <span data-ttu-id="924c5-121">Cette option n’apparaît pas si la connexion n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="924c5-121">This option does not appear if the connection is not set.</span></span>

<span data-ttu-id="924c5-122">Pour [plus d’informations, voir Utiliser Intune](https://docs.microsoft.com/intune/atp-manage-vulnerabilities) pour corriger les vulnérabilités identifiées par Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="924c5-122">See [Use Intune to remediate vulnerabilities identified by Microsoft Defender for Endpoint](https://docs.microsoft.com/intune/atp-manage-vulnerabilities) for details.</span></span>

### <a name="remediation-request-steps"></a><span data-ttu-id="924c5-123">Étapes de la demande de correction</span><span class="sxs-lookup"><span data-stu-id="924c5-123">Remediation request steps</span></span>

1. <span data-ttu-id="924c5-124">Go to the threat and vulnerability management navigation menu in the Microsoft Defender Security Center, and select [**Security recommendations**](tvm-security-recommendation.md).</span><span class="sxs-lookup"><span data-stu-id="924c5-124">Go to the threat and vulnerability management navigation menu in the Microsoft Defender Security Center, and select [**Security recommendations**](tvm-security-recommendation.md).</span></span>

2. <span data-ttu-id="924c5-125">Sélectionnez une recommandation de sécurité pour la demande de correction, puis sélectionnez **Options de correction.**</span><span class="sxs-lookup"><span data-stu-id="924c5-125">Select a security recommendation you would like to request remediation for, and then select **Remediation options**.</span></span>

3. <span data-ttu-id="924c5-126">Remplissez le formulaire, y compris ce pour quoi vous demandez des corrections, les groupes d’appareils applicables, la priorité, la date d’échéance et les notes facultatives.</span><span class="sxs-lookup"><span data-stu-id="924c5-126">Fill out the form, including what you are requesting remediation for, applicable device groups, priority, due date, and optional notes.</span></span>
    1. <span data-ttu-id="924c5-127">Si vous choisissez l’option de correction « Attention requise », la sélection d’une date d’échéance n’est pas disponible, car il n’existe aucune action spécifique.</span><span class="sxs-lookup"><span data-stu-id="924c5-127">If you choose the "attention required" remediation option, selecting a due date will not be available since there is no specific action.</span></span>

4. <span data-ttu-id="924c5-128">Sélectionnez **Envoyer une demande.**</span><span class="sxs-lookup"><span data-stu-id="924c5-128">Select **Submit request**.</span></span> <span data-ttu-id="924c5-129">L’envoi d’une demande de correction crée un élément d’activité de correction dans la gestion des menaces et des vulnérabilités, qui peut être utilisé pour surveiller la progression de la correction pour cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="924c5-129">Submitting a remediation request creates a remediation activity item within threat and vulnerability management, which can be used for monitoring the remediation progress for this recommendation.</span></span> <span data-ttu-id="924c5-130">Cela ne déclenche pas de correction ou n’applique aucune modification aux appareils.</span><span class="sxs-lookup"><span data-stu-id="924c5-130">This will not trigger a remediation or apply any changes to devices.</span></span>

5. <span data-ttu-id="924c5-131">Informez votre administrateur informatique de la nouvelle demande et demandez-lui de se connecter à Intune pour approuver ou rejeter la demande et démarrer un déploiement de package.</span><span class="sxs-lookup"><span data-stu-id="924c5-131">Notify your IT Administrator about the new request and have them log into Intune to approve or reject the request and start a package deployment.</span></span>

6. <span data-ttu-id="924c5-132">Go to the [**Remediation**](tvm-remediation.md) page to view the status of your remediation request.</span><span class="sxs-lookup"><span data-stu-id="924c5-132">Go to the [**Remediation**](tvm-remediation.md) page to view the status of your remediation request.</span></span>

<span data-ttu-id="924c5-133">Si vous souhaitez vérifier la façon dont le ticket s’affiche dans Intune, voir Utiliser [Intune](https://docs.microsoft.com/intune/atp-manage-vulnerabilities) pour corriger les vulnérabilités identifiées par Microsoft Defender pour endpoint pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="924c5-133">If you want to check how the ticket shows up in Intune, see [Use Intune to remediate vulnerabilities identified by Microsoft Defender for Endpoint](https://docs.microsoft.com/intune/atp-manage-vulnerabilities) for details.</span></span>

>[!NOTE]
><span data-ttu-id="924c5-134">Si votre demande implique de corriger plus de 10 000 appareils, nous ne pouvons envoyer que 10 000 appareils pour correction à Intune.</span><span class="sxs-lookup"><span data-stu-id="924c5-134">If your request involves remediating more than 10,000 devices, we can only send 10,000 devices for remediation to Intune.</span></span>

<span data-ttu-id="924c5-135">Une fois les faiblesses de cybersécurité de votre organisation identifiées et mappées aux [recommandations](tvm-security-recommendation.md)de sécurité actionnables, commencez à créer des tâches de sécurité.</span><span class="sxs-lookup"><span data-stu-id="924c5-135">After your organization's cybersecurity weaknesses are identified and mapped to actionable [security recommendations](tvm-security-recommendation.md), start creating security tasks.</span></span> <span data-ttu-id="924c5-136">Vous pouvez créer des tâches via l’intégration avec Microsoft Intune où des tickets de correction sont créés.</span><span class="sxs-lookup"><span data-stu-id="924c5-136">You can create tasks through the integration with Microsoft Intune where remediation tickets are created.</span></span>

<span data-ttu-id="924c5-137">Diminuez l’exposition de votre organisation contre les vulnérabilités et augmentez votre configuration de sécurité en remédiant aux recommandations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="924c5-137">Lower your organization's exposure from vulnerabilities and increase your security configuration by remediating the security recommendations.</span></span>

## <a name="view-your-remediation-activities"></a><span data-ttu-id="924c5-138">Afficher vos activités de correction</span><span class="sxs-lookup"><span data-stu-id="924c5-138">View your remediation activities</span></span>

<span data-ttu-id="924c5-139">Lorsque vous envoyez une demande de correction à partir de la page Recommandations en matière de sécurité, une activité de correction démarre.</span><span class="sxs-lookup"><span data-stu-id="924c5-139">When you submit a remediation request from the Security recommendations page, it kicks-off a remediation activity.</span></span> <span data-ttu-id="924c5-140">Une tâche de sécurité est créée et peut être suivi dans la **page** de correction de la gestion des menaces et des vulnérabilités, et un ticket de correction est créé dans Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="924c5-140">A security task is created that can be tracked in the threat and vulnerability management **Remediation** page, and a remediation ticket is created in Microsoft Intune.</span></span>

<span data-ttu-id="924c5-141">Si vous avez choisi l’option de correction « Attention requise », il n’y aura aucune barre de progression, état du ticket ou date d’échéance, car il n’existe aucune action réelle que nous pouvons surveiller.</span><span class="sxs-lookup"><span data-stu-id="924c5-141">If you chose the "attention required" remediation option, there will be no progress bar, ticket status, or due date since there is no actual action we can monitor.</span></span>

<span data-ttu-id="924c5-142">Une fois que vous êtes dans la page Correction, sélectionnez l’activité de correction à afficher.</span><span class="sxs-lookup"><span data-stu-id="924c5-142">Once you are in the Remediation page, select the remediation activity that you want to view.</span></span> <span data-ttu-id="924c5-143">Vous pouvez suivre les étapes de correction, suivre l’avancement, afficher la recommandation associée, exporter vers CSV ou marquer comme terminé.</span><span class="sxs-lookup"><span data-stu-id="924c5-143">You can follow the remediation steps, track progress, view the related recommendation, export to CSV, or mark as complete.</span></span>
<span data-ttu-id="924c5-144">![Exemple de page de correction, avec une activité de correction sélectionnée, et le volant de cette activité répertoriant la description, les outils de gestion des services informatiques et des appareils, ainsi que la progression de la correction des périphériques.](images/remediation_flyouteolsw.png)</span><span class="sxs-lookup"><span data-stu-id="924c5-144">![Example of the Remediation page, with a selected remediation activity, and that activity's flyout listing the description, IT service and device management tools, and device remediation progress.](images/remediation_flyouteolsw.png)</span></span>

>[!NOTE]
> <span data-ttu-id="924c5-145">Il existe une période de rétention de 180 jours pour les activités de correction terminées.</span><span class="sxs-lookup"><span data-stu-id="924c5-145">There is a 180 day retention period for completed remediation activities.</span></span> <span data-ttu-id="924c5-146">Pour que la page de correction continue de s’exécuter de façon optimale, l’activité de correction sera supprimée 6 mois après sa fin.</span><span class="sxs-lookup"><span data-stu-id="924c5-146">To keep the Remediation page performing optimally, the remediation activity will be removed 6 months after its completion.</span></span>

### <a name="completed-by-column"></a><span data-ttu-id="924c5-147">Terminé par colonne</span><span class="sxs-lookup"><span data-stu-id="924c5-147">Completed by column</span></span>

<span data-ttu-id="924c5-148">Suivre qui a fermé l’activité de correction avec la colonne « Terminé par » dans la page Correction.</span><span class="sxs-lookup"><span data-stu-id="924c5-148">Track who closed the remediation activity with the "Completed by" column on the Remediation page.</span></span>

- <span data-ttu-id="924c5-149">**Adresse e-mail**: adresse de messagerie de la personne qui a effectué manuellement la tâche</span><span class="sxs-lookup"><span data-stu-id="924c5-149">**Email address**: The email of the person who manually completed the task</span></span>
- <span data-ttu-id="924c5-150">**Confirmation du** système : la tâche a été effectuée automatiquement (tous les appareils corrigés)</span><span class="sxs-lookup"><span data-stu-id="924c5-150">**System confirmation**: The task was automatically completed (all devices remediated)</span></span>
- <span data-ttu-id="924c5-151">**N/A**: les informations ne sont pas disponibles, car nous ne savons pas comment cette tâche plus ancienne a été achevée</span><span class="sxs-lookup"><span data-stu-id="924c5-151">**N/A**: Information is not available because we don't know how this older task was completed</span></span>

![Créé par et terminé par des colonnes de deux lignes.](images/tvm-completed-by.png)

### <a name="top-remediation-activities-in-the-dashboard"></a><span data-ttu-id="924c5-154">Principales activités de correction dans le tableau de bord</span><span class="sxs-lookup"><span data-stu-id="924c5-154">Top remediation activities in the dashboard</span></span>

<span data-ttu-id="924c5-155">Afficher les **principales activités de correction dans** le tableau de bord de gestion des menaces et des [vulnérabilités.](tvm-dashboard-insights.md)</span><span class="sxs-lookup"><span data-stu-id="924c5-155">View **Top remediation activities** in the [threat and vulnerability management dashboard](tvm-dashboard-insights.md).</span></span> <span data-ttu-id="924c5-156">Sélectionnez l’une des entrées pour aller à la page **Correction.**</span><span class="sxs-lookup"><span data-stu-id="924c5-156">Select any of the entries to go to the **Remediation** page.</span></span> <span data-ttu-id="924c5-157">Vous pouvez marquer l’activité de correction comme terminée une fois que l’équipe d’administration informatique a corrigé la tâche.</span><span class="sxs-lookup"><span data-stu-id="924c5-157">You can mark the remediation activity as completed after the IT admin team remediates the task.</span></span>

![Exemple de carte d’activités de correction supérieure avec un tableau répertoriant les principales activités générées à partir des recommandations de sécurité.](images/tvm-remediation-activities-card.png)

## <a name="related-articles"></a><span data-ttu-id="924c5-159">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="924c5-159">Related articles</span></span>

- [<span data-ttu-id="924c5-160">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="924c5-160">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="924c5-161">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="924c5-161">Dashboard</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="924c5-162">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="924c5-162">Security recommendations</span></span>](tvm-security-recommendation.md)