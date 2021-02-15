---
title: Surveiller et répondre aux incidents de confidentialité des données dans votre organisation
ms.author: bcarter
author: brendacarter
f1.keywords:
- NOCSH
manager: laurawi
ms.date: 01/04/2021
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- m365solution-infoprotection
- m365solution-scenario
ms.custom: ''
description: Utiliser des stratégies d’audit et d’alerte, ainsi que des demandes des personnes qui répondent aux incidents de données personnelles.
ms.openlocfilehash: 3ae0f2a6528f6188500c7cee7732c6447013eaa6
ms.sourcegitcommit: ae646779d84e993cf80b1207e76b856a21be5790
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2021
ms.locfileid: "49749586"
---
# <a name="monitor-and-respond-to-data-privacy-incidents-in-your-organization"></a><span data-ttu-id="ea59f-103">Surveiller et répondre aux incidents de confidentialité des données dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="ea59f-103">Monitor and respond to data privacy incidents in your organization</span></span>

<span data-ttu-id="ea59f-104">Les fonctionnalités de Microsoft 365 sont disponibles pour vous aider à surveiller, examiner et répondre aux incidents de confidentialité des données dans votre organisation au cours de l’opérationnalisation des fonctionnalités associées.</span><span class="sxs-lookup"><span data-stu-id="ea59f-104">Microsoft 365 features are available to help you monitor, investigate, and respond to data privacy incidents in your organization as you operationalize related capabilities.</span></span> <span data-ttu-id="ea59f-105">Il peut également être important d’avoir des processus, des procédures et d’autres documents pour chacun d’eux pour démontrer la conformité aux organismes de réglementation.</span><span class="sxs-lookup"><span data-stu-id="ea59f-105">Having processes, procedures, and other documentation for each of these may also be important to demonstrate compliance to regulatory bodies.</span></span>

<span data-ttu-id="ea59f-106">Cela inclut ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ea59f-106">These include:</span></span> 

- <span data-ttu-id="ea59f-107">Stratégies d’audit et d’alerte</span><span class="sxs-lookup"><span data-stu-id="ea59f-107">Auditing and alert policies</span></span>
- <span data-ttu-id="ea59f-108">Demandes des personnes objet de données (y compris la recherche de contenu et eDiscovery)</span><span class="sxs-lookup"><span data-stu-id="ea59f-108">Data subject requests (including content search and eDiscovery)</span></span>
- <span data-ttu-id="ea59f-109">Outils d’investigation et rapports supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ea59f-109">Additional investigative tools and reporting</span></span>

## <a name="data-privacy-regulations-impacting-the-use-of-monitoring-and-response-tools"></a><span data-ttu-id="ea59f-110">Réglementations en matière de confidentialité des données qui ont un impact sur l’utilisation des outils de surveillance et de réponse</span><span class="sxs-lookup"><span data-stu-id="ea59f-110">Data privacy regulations impacting the use of monitoring and response tools</span></span>

<span data-ttu-id="ea59f-111">Voici un exemple de liste des réglementations de confidentialité des données qui peuvent être liées aux contrôles de gouvernance des informations :</span><span class="sxs-lookup"><span data-stu-id="ea59f-111">Here is a sample listing of data privacy regulations that may relate to information governance controls:</span></span>

- <span data-ttu-id="ea59f-112">LGPD Article 46</span><span class="sxs-lookup"><span data-stu-id="ea59f-112">LGPD Article 46</span></span>
- <span data-ttu-id="ea59f-113">LGPD Article 48</span><span class="sxs-lookup"><span data-stu-id="ea59f-113">LGPD Article 48</span></span>
- <span data-ttu-id="ea59f-114">Article R GDPR (5)(1)(f)</span><span class="sxs-lookup"><span data-stu-id="ea59f-114">GDPR Article (5)(1)(f)</span></span>
- <span data-ttu-id="ea59f-115">Article R GDPR (15)(1)(e)</span><span class="sxs-lookup"><span data-stu-id="ea59f-115">GDPR Article (15)(1)(e)</span></span>
- <span data-ttu-id="ea59f-116">HIPAA-HITECH (45 C.F.R.</span><span class="sxs-lookup"><span data-stu-id="ea59f-116">HIPAA-HITECH (45 C.F.R.</span></span> <span data-ttu-id="ea59f-117">164.308(a)(1)(ii)(D))</span><span class="sxs-lookup"><span data-stu-id="ea59f-117">164.308(a)(1)(ii)(D))</span></span>
- <span data-ttu-id="ea59f-118">HIPAA-HITECH (45 C.F.R.</span><span class="sxs-lookup"><span data-stu-id="ea59f-118">HIPAA-HITECH (45 C.F.R.</span></span> <span data-ttu-id="ea59f-119">164.308(a)(6)(ii)</span><span class="sxs-lookup"><span data-stu-id="ea59f-119">164.308(a)(6)(ii)</span></span>
- <span data-ttu-id="ea59f-120">HIPAA-HITECH (45 C.F.R.</span><span class="sxs-lookup"><span data-stu-id="ea59f-120">HIPAA-HITECH (45 C.F.R.</span></span> <span data-ttu-id="ea59f-121">164.312(b))</span><span class="sxs-lookup"><span data-stu-id="ea59f-121">164.312(b))</span></span>
- <span data-ttu-id="ea59f-122">CCPA (1798.105(c))</span><span class="sxs-lookup"><span data-stu-id="ea59f-122">CCPA (1798.105(c))</span></span>

<span data-ttu-id="ea59f-123">Pour plus d’informations, voir Évaluer les risques de confidentialité des données [et identifier les informations sensibles.](information-protection-deploy-assess.md)</span><span class="sxs-lookup"><span data-stu-id="ea59f-123">For more information, see [Assess data privacy risks and identify sensitive information](information-protection-deploy-assess.md).</span></span>

<span data-ttu-id="ea59f-124">Les réglementations en matière de confidentialité des données appellent généralement les règles suivantes pour la surveillance et la réponse :</span><span class="sxs-lookup"><span data-stu-id="ea59f-124">The data privacy regulations generally call for the following for monitoring and response:</span></span>

- <span data-ttu-id="ea59f-125">Audit, alerte et rapport pour les activités liées au stockage, au partage et au traitement des données personnelles</span><span class="sxs-lookup"><span data-stu-id="ea59f-125">Auditing, alerting, and reporting for activities related to the storage, sharing and processing of personal data</span></span>
- <span data-ttu-id="ea59f-126">La possibilité de répondre à une demande d’objet de données (DSR) et, dans certains cas, d’effectuer des enquêtes et d’autres mesures administratives pour se conformer à ces demandes.</span><span class="sxs-lookup"><span data-stu-id="ea59f-126">The ability to respond to a data subject request (DSR) and in some cases, perform investigative and other administrative measures to comply with such requests.</span></span>

<span data-ttu-id="ea59f-127">Votre organisation peut également effectuer des activités de surveillance et de réponse à d’autres fins, telles que d’autres besoins de conformité ou pour des raisons professionnelles.</span><span class="sxs-lookup"><span data-stu-id="ea59f-127">Your organization may also wish to perform monitoring and response activities for other purposes, such as other compliance needs or for business reasons.</span></span> <span data-ttu-id="ea59f-128">L’établissement de votre schéma de surveillance et de réponse pour la confidentialité des données doit être effectué dans le cadre de la planification globale de la surveillance et de la réponse, de l’implémentation et de la gestion.</span><span class="sxs-lookup"><span data-stu-id="ea59f-128">Establishing your monitoring and response scheme for data privacy should be done as part of overall monitoring and response planning, implementation, and management.</span></span>

<span data-ttu-id="ea59f-129">Pour vous aider à démarrer avec un schéma de surveillance et de réponse dans Microsoft 365 pour les réglementations en matière de confidentialité des données, cet article répertorie les fonctionnalités utiles de Microsoft 365 pour répondre à des questions telles que :</span><span class="sxs-lookup"><span data-stu-id="ea59f-129">To help you get started with a monitoring and response scheme in Microsoft 365 for data privacy regulations, this article lists useful capabilities in Microsoft 365 to answer questions such as:</span></span> 

- <span data-ttu-id="ea59f-130">Quels types de techniques de surveillance, d’investigation et de rapport au quotidien sont disponibles pour les différents types de données et sources ?</span><span class="sxs-lookup"><span data-stu-id="ea59f-130">What sort of day-to-day monitoring, investigative and reporting techniques are available for the different data types and sources?</span></span>
- <span data-ttu-id="ea59f-131">Les mécanismes qui seront nécessaires pour gérer les demandes des personnes qui traitent des données (DSR) et les mesures correctives, telles que l’anonymisation, la suppression et la suppression.</span><span class="sxs-lookup"><span data-stu-id="ea59f-131">What mechanisms will be needed to handle data subject requests (DSRs) and any remedial actions, such as anonymization, redaction, and deletion.</span></span>

## <a name="auditing-and-alert-policies-in-the-security-and-compliance-center"></a><span data-ttu-id="ea59f-132">Stratégies d’audit et d’alerte dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="ea59f-132">Auditing and Alert Policies in the Security and Compliance Center</span></span>

<span data-ttu-id="ea59f-133">Consultez les articles suivants pour la configuration de l’audit, de l’audit avancé et des stratégies d’alerte :</span><span class="sxs-lookup"><span data-stu-id="ea59f-133">See these articles for setting up auditing, advanced auditing, and alert policies:</span></span>

- [<span data-ttu-id="ea59f-134">Audit unifié</span><span class="sxs-lookup"><span data-stu-id="ea59f-134">Unified auditing</span></span>](../compliance/search-the-audit-log-in-security-and-compliance.md)
- [<span data-ttu-id="ea59f-135">Audit de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ea59f-135">Mailbox auditing</span></span>](../compliance/enable-mailbox-auditing.md)
- [<span data-ttu-id="ea59f-136">Audit avancé</span><span class="sxs-lookup"><span data-stu-id="ea59f-136">Advanced audit</span></span>](../compliance/advanced-audit.md)
- [<span data-ttu-id="ea59f-137">Stratégies d’alerte</span><span class="sxs-lookup"><span data-stu-id="ea59f-137">Alert policies</span></span>](../compliance/alert-policies.md)

## <a name="data-subject-requests-for-the-gdpr-and-ccpa"></a><span data-ttu-id="ea59f-138">Demandes des personnes responsables des données concernant le R GDPR et le CCPA</span><span class="sxs-lookup"><span data-stu-id="ea59f-138">Data subject requests for the GDPR and CCPA</span></span>

<span data-ttu-id="ea59f-139">Pour [plus d’informations](../compliance/gdpr-dsr-office365.md) sur la réponse à une DSR dans Microsoft 365, voir demandes des personnes qui répondent aux données pour le R GDPR et le CCPA.</span><span class="sxs-lookup"><span data-stu-id="ea59f-139">See [Data Subject Requests for the GDPR and CCPA](../compliance/gdpr-dsr-office365.md) for information on responding to a DSR in Microsoft 365.</span></span>

## <a name="manage-deleted-users-in-microsoft-stream"></a><span data-ttu-id="ea59f-140">Gérer les utilisateurs supprimés dans Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="ea59f-140">Manage deleted users in Microsoft Stream</span></span>

<span data-ttu-id="ea59f-141">Pour Microsoft Stream, lorsqu’un utilisateur est supprimé d’Azure Active Directory (Azure AD), si son nom était associé à une vidéo Stream publiée avant ce point, son adresse de messagerie reste associée à la vidéo.</span><span class="sxs-lookup"><span data-stu-id="ea59f-141">For Microsoft Stream, when a user is deleted from Azure Active Directory (Azure AD), if their name was associated with a posted Stream video prior to that point, their email address remains associated with the video.</span></span> <span data-ttu-id="ea59f-142">Pour [le supprimer, voir](https://docs.microsoft.com/stream/managing-deleted-users) Gérer les utilisateurs supprimés de Microsoft Stream.</span><span class="sxs-lookup"><span data-stu-id="ea59f-142">See [Manage deleted users from Microsoft Stream](https://docs.microsoft.com/stream/managing-deleted-users) to remove it.</span></span>

## <a name="insider-risk-management-as-an-investigative-tool"></a><span data-ttu-id="ea59f-143">Gestion des risques internes en tant qu’outil d’investigation</span><span class="sxs-lookup"><span data-stu-id="ea59f-143">Insider risk management as an investigative tool</span></span>

<span data-ttu-id="ea59f-144">La gestion des risques internes dans [Microsoft 365](../compliance/insider-risk-management.md) est une fonctionnalité du Centre d’administration de conformité Microsoft pour vous aider à minimiser les risques internes en vous permettant de détecter, d’examiner et d’agir sur les activités à risque dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ea59f-144">[Insider risk management in Microsoft 365](../compliance/insider-risk-management.md) is a feature of the Microsoft Compliance admin center to help you minimize internal risk by enabling you to detect, investigate, and take action on risky activities in your organization.</span></span>
