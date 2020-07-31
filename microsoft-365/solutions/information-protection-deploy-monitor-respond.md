---
title: Surveillance et réponse aux incidents de confidentialité des données au sein de votre organisation
ms.author: bcarter
author: brendacarter
f1.keywords:
- NOCSH
manager: laurawi
ms.date: 06/09/2020
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- m365solution-infoprotection
ms.custom: ''
description: Utilisez les stratégies d’audit et d’alerte et les demandes des personnes concernées pour surveiller et répondre aux incidents de données personnelles.
ms.openlocfilehash: 8fdba5799ca9ee97a013c1322e5e79f6bf38764a
ms.sourcegitcommit: 0f71042edc7c3a7f10a7b92e1943abf51532cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/29/2020
ms.locfileid: "46522072"
---
# <a name="monitor-and-respond-to-data-privacy-incidents-in-your-organization"></a><span data-ttu-id="18e94-103">Surveillance et réponse aux incidents de confidentialité des données au sein de votre organisation</span><span class="sxs-lookup"><span data-stu-id="18e94-103">Monitor and respond to data privacy incidents in your organization</span></span>

<span data-ttu-id="18e94-104">Les fonctionnalités de Microsoft 365 sont disponibles pour vous aider à surveiller, examiner et répondre aux incidents de confidentialité des données au sein de votre organisation lorsque vous avez opérationnel les fonctionnalités connexes.</span><span class="sxs-lookup"><span data-stu-id="18e94-104">Microsoft 365 features are available to help you monitor, investigate, and respond to data privacy incidents in your organization as you operationalize related capabilities.</span></span> <span data-ttu-id="18e94-105">L’existence de processus, de procédures et d’autres documents pour chacun de ces éléments peut également être importante pour démontrer la conformité aux organismes de réglementation.</span><span class="sxs-lookup"><span data-stu-id="18e94-105">Having processes, procedures, and other documentation for each of these may also be important to demonstrate compliance to regulatory bodies.</span></span>

<span data-ttu-id="18e94-106">Cela inclut ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="18e94-106">These include:</span></span> 

- <span data-ttu-id="18e94-107">Stratégies d’audit et d’alerte</span><span class="sxs-lookup"><span data-stu-id="18e94-107">Auditing and alert policies</span></span>
- <span data-ttu-id="18e94-108">Demandes des personnes concernées (y compris la recherche de contenu et eDiscovery)</span><span class="sxs-lookup"><span data-stu-id="18e94-108">Data subject requests (including content search and eDiscovery)</span></span>
- <span data-ttu-id="18e94-109">Outils et rapports d’enquête supplémentaires</span><span class="sxs-lookup"><span data-stu-id="18e94-109">Additional investigative tools and reporting</span></span>

## <a name="data-privacy-regulations-impacting-the-use-of-monitoring-and-response-tools"></a><span data-ttu-id="18e94-110">Réglementations en matière de confidentialité des données ayant un impact sur l’utilisation des outils de surveillance et de réponse</span><span class="sxs-lookup"><span data-stu-id="18e94-110">Data privacy regulations impacting the use of monitoring and response tools</span></span>

<span data-ttu-id="18e94-111">Voici un exemple de liste de réglementations sur la confidentialité des données pouvant être liées aux contrôles de la gouvernance des informations :</span><span class="sxs-lookup"><span data-stu-id="18e94-111">Here is a sample listing of data privacy regulations that may relate to information governance controls:</span></span>

- <span data-ttu-id="18e94-112">Article 46 de la LGPD</span><span class="sxs-lookup"><span data-stu-id="18e94-112">LGPD Article 46</span></span>
- <span data-ttu-id="18e94-113">Article 48 de la LGPD</span><span class="sxs-lookup"><span data-stu-id="18e94-113">LGPD Article 48</span></span>
- <span data-ttu-id="18e94-114">Article RGPD (5) (1) (f)</span><span class="sxs-lookup"><span data-stu-id="18e94-114">GDPR Article (5)(1)(f)</span></span>
- <span data-ttu-id="18e94-115">Article RGPD (15) (1) (e)</span><span class="sxs-lookup"><span data-stu-id="18e94-115">GDPR Article (15)(1)(e)</span></span>
- <span data-ttu-id="18e94-116">HIPAA-HI (45 C.F.R.</span><span class="sxs-lookup"><span data-stu-id="18e94-116">HIPAA-HITECH (45 C.F.R.</span></span> <span data-ttu-id="18e94-117">164.308 (a) (1) (II) (D))</span><span class="sxs-lookup"><span data-stu-id="18e94-117">164.308(a)(1)(ii)(D))</span></span>
- <span data-ttu-id="18e94-118">HIPAA-HI (45 C.F.R.</span><span class="sxs-lookup"><span data-stu-id="18e94-118">HIPAA-HITECH (45 C.F.R.</span></span> <span data-ttu-id="18e94-119">164.308(a)(6)(ii)</span><span class="sxs-lookup"><span data-stu-id="18e94-119">164.308(a)(6)(ii)</span></span>
- <span data-ttu-id="18e94-120">HIPAA-HI (45 C.F.R.</span><span class="sxs-lookup"><span data-stu-id="18e94-120">HIPAA-HITECH (45 C.F.R.</span></span> <span data-ttu-id="18e94-121">164.312 (b))</span><span class="sxs-lookup"><span data-stu-id="18e94-121">164.312(b))</span></span>
- <span data-ttu-id="18e94-122">CCPA (1798.105 (c))</span><span class="sxs-lookup"><span data-stu-id="18e94-122">CCPA (1798.105(c))</span></span>

<span data-ttu-id="18e94-123">Pour plus d’informations, consultez la rubrique [évaluation des risques de confidentialité des données et identification des informations sensibles](information-protection-deploy-assess.md).</span><span class="sxs-lookup"><span data-stu-id="18e94-123">For more information, see [Assess data privacy risks and identify sensitive information](information-protection-deploy-assess.md).</span></span>

<span data-ttu-id="18e94-124">Les réglementations en matière de confidentialité des données appellent généralement ce qui suit pour la surveillance et la réponse :</span><span class="sxs-lookup"><span data-stu-id="18e94-124">The data privacy regulations generally call for the following for monitoring and response:</span></span>

- <span data-ttu-id="18e94-125">Audit, alerte et création de rapports pour les activités liées au stockage, au partage et au traitement des données personnelles</span><span class="sxs-lookup"><span data-stu-id="18e94-125">Auditing, alerting, and reporting for activities related to the storage, sharing and processing of personal data</span></span>
- <span data-ttu-id="18e94-126">La possibilité de répondre à une demande d’objet de données (DSR) et, dans certains cas, d’effectuer des actions d’enquête et d’autres mesures administratives pour se conformer à ces demandes.</span><span class="sxs-lookup"><span data-stu-id="18e94-126">The ability to respond to a data subject request (DSR) and in some cases, perform investigative and other administrative measures to comply with such requests.</span></span>

<span data-ttu-id="18e94-127">Votre organisation peut également souhaiter effectuer des activités de surveillance et de réponse à d’autres fins, telles que d’autres besoins en matière de conformité ou pour des raisons professionnelles.</span><span class="sxs-lookup"><span data-stu-id="18e94-127">Your organization may also wish to perform monitoring and response activities for other purposes, such as other compliance needs or for business reasons.</span></span> <span data-ttu-id="18e94-128">L’établissement de votre schéma de surveillance et de réponse pour la confidentialité des données doit être réalisé dans le cadre de la planification globale de la surveillance et de la réponse, de l’implémentation et de la gestion.</span><span class="sxs-lookup"><span data-stu-id="18e94-128">Establishing your monitoring and response scheme for data privacy should be done as part of overall monitoring and response planning, implementation, and management.</span></span>

<span data-ttu-id="18e94-129">Pour vous aider à prendre en main un schéma de surveillance et de réponse dans Microsoft 365 pour des réglementations sur la confidentialité des données, cet article répertorie les fonctionnalités utiles dans Microsoft 365 afin de répondre à des questions telles que :</span><span class="sxs-lookup"><span data-stu-id="18e94-129">To help you get started with a monitoring and response scheme in Microsoft 365 for data privacy regulations, this article lists useful capabilities in Microsoft 365 to answer questions such as:</span></span> 

- <span data-ttu-id="18e94-130">Quels sont les types de données de surveillance quotidienne, d’enquête et de création de rapports disponibles pour les différents types de données et sources ?</span><span class="sxs-lookup"><span data-stu-id="18e94-130">What sort of day-to-day monitoring, investigative and reporting techniques are available for the different data types and sources?</span></span>
- <span data-ttu-id="18e94-131">Les mécanismes qui seront nécessaires pour gérer les demandes des personnes concernées par les données (DSR) et les actions correctives, telles que l’anonymisation, la biffure et la suppression.</span><span class="sxs-lookup"><span data-stu-id="18e94-131">What mechanisms will be needed to handle data subject requests (DSRs) and any remedial actions, such as anonymization, redaction, and deletion.</span></span>

## <a name="auditing-and-alert-policies-in-the-security-and-compliance-center"></a><span data-ttu-id="18e94-132">Stratégies d’audit et d’alerte dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="18e94-132">Auditing and Alert Policies in the Security and Compliance Center</span></span>

<span data-ttu-id="18e94-133">Consultez les articles suivants pour configurer les stratégies d’audit, d’audit avancé et d’alerte :</span><span class="sxs-lookup"><span data-stu-id="18e94-133">See these articles for setting up auditing, advanced auditing, and alert policies:</span></span>

- [<span data-ttu-id="18e94-134">Audit unifié</span><span class="sxs-lookup"><span data-stu-id="18e94-134">Unified auditing</span></span>](../compliance/search-the-audit-log-in-security-and-compliance.md)
- [<span data-ttu-id="18e94-135">Audit de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="18e94-135">Mailbox auditing</span></span>](../compliance/enable-mailbox-auditing.md)
- [<span data-ttu-id="18e94-136">Audit avancé</span><span class="sxs-lookup"><span data-stu-id="18e94-136">Advanced audit</span></span>](../compliance/advanced-audit.md)
- [<span data-ttu-id="18e94-137">Stratégies d’alerte</span><span class="sxs-lookup"><span data-stu-id="18e94-137">Alert policies</span></span>](../compliance/alert-policies.md)

## <a name="data-subject-requests-for-the-gdpr-and-ccpa"></a><span data-ttu-id="18e94-138">Demandes des personnes concernées pour le RGPD et CCPA</span><span class="sxs-lookup"><span data-stu-id="18e94-138">Data subject requests for the GDPR and CCPA</span></span>

<span data-ttu-id="18e94-139">Consultez [demandes des personnes concernées pour RGPD et CCPA](../compliance/gdpr-dsr-office365.md) pour obtenir des informations sur la réponse à un DSR dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="18e94-139">See [Data Subject Requests for the GDPR and CCPA](../compliance/gdpr-dsr-office365.md) for information on responding to a DSR in Microsoft 365.</span></span>

## <a name="manage-deleted-users-in-microsoft-stream"></a><span data-ttu-id="18e94-140">Gérer les utilisateurs supprimés dans Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="18e94-140">Manage deleted users in Microsoft Stream</span></span>

<span data-ttu-id="18e94-141">Pour Microsoft Stream, lorsqu’un utilisateur est supprimé d’Azure Active Directory (Azure AD), si son nom était associé à un flux vidéo publié avant ce point, son adresse de messagerie reste associée à la vidéo.</span><span class="sxs-lookup"><span data-stu-id="18e94-141">For Microsoft Stream, when a user is deleted from Azure Active Directory (Azure AD), if their name was associated with a posted Stream video prior to that point, their email address remains associated with the video.</span></span> <span data-ttu-id="18e94-142">Consultez la rubrique [Manage Deleted users from Microsoft Stream](https://docs.microsoft.com/stream/managing-deleted-users) pour le supprimer.</span><span class="sxs-lookup"><span data-stu-id="18e94-142">See [Manage deleted users from Microsoft Stream](https://docs.microsoft.com/stream/managing-deleted-users) to remove it.</span></span>

## <a name="additional-investigative-tools"></a><span data-ttu-id="18e94-143">Outils d’enquête supplémentaires</span><span class="sxs-lookup"><span data-stu-id="18e94-143">Additional investigative tools</span></span>

<span data-ttu-id="18e94-144">Voici deux autres outils qui peuvent être utiles pour surveiller, examiner et résoudre les problèmes liés à la confidentialité des données au sein de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="18e94-144">Here are two additional tools that might be useful for monitoring, investigating, and remediating data privacy-related incidents in your organization:</span></span>

- <span data-ttu-id="18e94-145">La [gestion des risques initiés dans microsoft 365](../compliance/insider-risk-management.md), une fonctionnalité du centre d’administration de la conformité Microsoft afin de réduire les risques internes en vous permettant de détecter, d’examiner et de prendre des mesures pour les activités à risque au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="18e94-145">[Insider risk management in Microsoft 365](../compliance/insider-risk-management.md), a feature of the Microsoft Compliance admin center to help minimize internal risk by enabling you to detect, investigate, and take action on risky activities in your organization.</span></span>
- <span data-ttu-id="18e94-146">Les [enquêtes de données dans microsoft 365](../compliance/overview-data-investigations.md), une fonctionnalité du centre d’administration de la conformité Microsoft pour rechercher des données sensibles, malveillantes ou égarées dans Microsoft 365, puis Rechercher ce qui est advenu de prendre les mesures appropriées pour corriger l’incident.</span><span class="sxs-lookup"><span data-stu-id="18e94-146">[Data investigations in Microsoft 365](../compliance/overview-data-investigations.md), a feature of the Microsoft Compliance admin center to search for sensitive, malicious, or misplaced data across Microsoft 365, and then investigate what happened to take the appropriate actions to remediate the incident.</span></span>
