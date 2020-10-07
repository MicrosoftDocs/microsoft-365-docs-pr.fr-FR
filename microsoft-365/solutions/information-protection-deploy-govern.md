---
title: Régir les informations soumises au règlement de confidentialité des données
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
- m365solution-scenario
ms.custom: ''
description: Utilisez les étiquettes et les stratégies de rétention de Microsoft 365 pour gérer les données personnelles dans votre environnement Microsoft 365.
ms.openlocfilehash: c2a933e556213ae4b78db9dc5f903885df969b27
ms.sourcegitcommit: 9841058fcc95f7c2fed6af92bc3c3686944829b6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48377044"
---
# <a name="govern-information-subject-to-data-privacy-regulation"></a><span data-ttu-id="d7fdd-103">Régir les informations soumises au règlement de confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="d7fdd-103">Govern information subject to data privacy regulation</span></span>

<span data-ttu-id="d7fdd-104">Les contrôles de gouvernance des informations peuvent être employés dans votre environnement afin de répondre aux besoins de conformité des données en matière de confidentialité, y compris un numéro spécifique au règlement général sur la protection des données (RGPD), au HIPAA-Hi (la loi américaine Health Care Privacy Act), California Consumer Protection Act (CCPA) et le Brésil Data Protection Act (LGPD).</span><span class="sxs-lookup"><span data-stu-id="d7fdd-104">Information governance controls can be employed in your environment to help address data privacy compliance needs, including a number that are specific to General Data Protection Regulation (GDPR), HIPAA-HITECH (the United States health care privacy act), California Consumer Protection Act (CCPA), and the Brazil Data Protection Act (LGPD).</span></span> 

<span data-ttu-id="d7fdd-105">Ces contrôles appartiennent principalement aux sections de solution suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7fdd-105">These controls primarily fall into the following solution areas:</span></span>

- <span data-ttu-id="d7fdd-106">Stratégies de conservation</span><span class="sxs-lookup"><span data-stu-id="d7fdd-106">Retention policies</span></span>
- <span data-ttu-id="d7fdd-107">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="d7fdd-107">Retention labels</span></span>
- <span data-ttu-id="d7fdd-108">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="d7fdd-108">Records management</span></span>

## <a name="data-privacy-regulations-impacting-information-governance-controls"></a><span data-ttu-id="d7fdd-109">Réglementations en matière de confidentialité des données ayant un impact sur les contrôles de gouvernance des informations</span><span class="sxs-lookup"><span data-stu-id="d7fdd-109">Data privacy regulations impacting information governance controls</span></span>

<span data-ttu-id="d7fdd-110">Voici un exemple de liste de réglementations sur la confidentialité des données pouvant être liées aux contrôles de la gouvernance des informations :</span><span class="sxs-lookup"><span data-stu-id="d7fdd-110">Here is a sample listing of data privacy regulations that may relate to information governance controls:</span></span>

- <span data-ttu-id="d7fdd-111">Article RGPD (13) (2) (a)</span><span class="sxs-lookup"><span data-stu-id="d7fdd-111">GDPR Article (13)(2)(a)</span></span>
- <span data-ttu-id="d7fdd-112">Article RGPD (5) (1) (f)</span><span class="sxs-lookup"><span data-stu-id="d7fdd-112">GDPR Article (5)(1)(f)</span></span>
- <span data-ttu-id="d7fdd-113">HIPAA-Hi (45 CFR 164.312 (c) (2))</span><span class="sxs-lookup"><span data-stu-id="d7fdd-113">HIPAA-HITECH (45 CFR 164.312(c)(2))</span></span>
- <span data-ttu-id="d7fdd-114">HIPAA-Hi (45 CFR 164.316 (b) (1) (i))</span><span class="sxs-lookup"><span data-stu-id="d7fdd-114">HIPAA-HITECH (45 CFR 164.316(b)(1)(i))</span></span>
- <span data-ttu-id="d7fdd-115">HIPAA-Hi (45 CFR 164.316 (b) (1) (II))</span><span class="sxs-lookup"><span data-stu-id="d7fdd-115">HIPAA-HITECH (45 CFR 164.316(b)(1)(ii))</span></span>
- <span data-ttu-id="d7fdd-116">Article 46 de la LGPD</span><span class="sxs-lookup"><span data-stu-id="d7fdd-116">LGPD Article 46</span></span>

<span data-ttu-id="d7fdd-117">Pour plus d’informations sur ces réglementations, voir l’article relatif à l' [évaluation des risques de confidentialité des données et de l’identification des informations sensibles](information-protection-deploy-assess.md).</span><span class="sxs-lookup"><span data-stu-id="d7fdd-117">For more information on these regulations, see the [assess data privacy risks and identify sensitive information article](information-protection-deploy-assess.md).</span></span>

<span data-ttu-id="d7fdd-118">Pour la gouvernance des informations, les réglementations en matière de confidentialité des données appellent généralement les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7fdd-118">For information governance, data privacy regulations typically call for the following:</span></span>

- <span data-ttu-id="d7fdd-119">Vous devez utiliser un modèle technique de rétention et de suppression pour les données personnelles stockées dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-119">You should employ a technical scheme for retention and deletion for personal data stored in Microsoft 365.</span></span>
- <span data-ttu-id="d7fdd-120">Si vous envisagez de stocker des données personnelles, Informez l’objet de la durée de stockage des données, qui est une pratique standard sur les systèmes Web frontaux.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-120">If you're going to store personal data, inform the subject of how long the data will be stored, which is a standard practice now on front-end web systems.</span></span>
- <span data-ttu-id="d7fdd-121">Les données personnelles doivent être protégées contre le traitement, la perte ou la modification accidentels à l’aide de méthodes vérifiables.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-121">Personal data should be protected against accidental processing, loss, or alteration using verifiable methods.</span></span>
- <span data-ttu-id="d7fdd-122">Toute action exécutée sur des données personnelles doit être documentée et cette documentation doit être conservée pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-122">Any action executed against personal data should be documented and that documentation should be retained for a specified period.</span></span>

<span data-ttu-id="d7fdd-123">Étant donné que les réglementations sur la confidentialité des données ne sont pas très spécifiques en matière de rétention et de suppression des données, d’autres facteurs doivent être pris en considération afin de pouvoir imposer des directives de gouvernance des informations pour les informations personnelles stockées dans votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-123">Because the data privacy regulations are not very specific when it comes to data retention and deletion, other factors need to be taken into consideration that may dictate information governance guidelines for personal information stored in your Microsoft 365 subscription.</span></span> <span data-ttu-id="d7fdd-124">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="d7fdd-124">Here are a few examples:</span></span>

- <span data-ttu-id="d7fdd-125">Vieillissement des comptes des consommateurs après 5 ans d’inactivité et nécessite une suppression ou une anonymisation des données de compte après ce point, nécessitant une orchestration entre le système stockant les données et les flux de travail liés aux notifications et à d’autres automatisations.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-125">Aging out consumer accounts after 5 years of inactivity and requires deletion or anonymization of account data after that point, requiring orchestration between the system storing the data and workflows related to notifications and other automation.</span></span>
- <span data-ttu-id="d7fdd-126">La configuration des règles de conservation des stratégies et des procédures liées à RGPD pendant trois ans après leur remplacement, qui s’aligne sur la planification de rétention de l’Organisation pour les stratégies et les procédures.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-126">Configuring rules for keeping policies and procedures related to GDPR around for three years after they've been superseded, which aligns with the organization's retention schedule for policies and procedures.</span></span>
- <span data-ttu-id="d7fdd-127">Maintenance d’un abonnement distinct pour la communication avec les consommateurs via son organisation de support technique.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-127">Maintaining a separate subscription for communicating with consumers through its support organization.</span></span> <span data-ttu-id="d7fdd-128">Toutes les communications de messagerie ont été conservées et supprimées au bout de deux semaines afin de réduire les accumulations de dettes de confidentialité dans le système.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-128">All email communications were retained and deleted after two weeks to reduce any privacy debt buildup in the system.</span></span>

<span data-ttu-id="d7fdd-129">Une question clé à répondre est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d7fdd-129">A key question to answer is:</span></span> 

- <span data-ttu-id="d7fdd-130">Combien de temps les informations contenant des données personnelles doivent-elles être conservées pour des raisons professionnelles valides afin d’éviter les pratiques de « conserver définitivement » ?</span><span class="sxs-lookup"><span data-stu-id="d7fdd-130">How long does information containing personal data need to be kept around for valid business reasons to avoid "keep it forever" practices?</span></span> <span data-ttu-id="d7fdd-131">Cela doit être équilibré en fonction des besoins de rétention pour la continuité de l’activité.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-131">This must be balanced with retention needs for business continuity.</span></span>

<span data-ttu-id="d7fdd-132">Quelles que soient les raisons juridiques et professionnelles de conserver des informations personnelles ou de les supprimer, Microsoft fournit un certain nombre de fonctionnalités pour implémenter votre schéma de gouvernance des données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-132">Regardless of the legal and business reasons for keeping personal information around or deleting it, Microsoft provides a number of capabilities to implement your data governance scheme in Microsoft 365.</span></span>

## <a name="managing-information-governance-in-microsoft-365"></a><span data-ttu-id="d7fdd-133">Gestion de la gouvernance des informations dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d7fdd-133">Managing information governance in Microsoft 365</span></span>

<span data-ttu-id="d7fdd-134">Pour commencer, consultez la rubrique [Manage information Governance](../compliance/manage-information-governance.md) and [Data Retention, suppression et Destruction dans Microsoft 365](https://docs.microsoft.com/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview).</span><span class="sxs-lookup"><span data-stu-id="d7fdd-134">To begin, see [Manage information governance](../compliance/manage-information-governance.md) and [Data Retention, Deletion and Destruction in Microsoft 365](https://docs.microsoft.com/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview).</span></span>

### <a name="develop-data-retention-schedules-for-containers-email-and-content"></a><span data-ttu-id="d7fdd-135">Développer des planifications de conservation des données pour les conteneurs, le courrier électronique et le contenu</span><span class="sxs-lookup"><span data-stu-id="d7fdd-135">Develop data retention schedules for containers, email, and content</span></span>

<span data-ttu-id="d7fdd-136">Gardez les éléments suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="d7fdd-136">Keep the following in mind:</span></span>

- <span data-ttu-id="d7fdd-137">La création d’une planification de rétention des données pour les types d’informations définis doit être considérée comme une condition préalable à l’implémentation d’un modèle de rétention ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-137">Establishing a data retention schedule for defined information types should be considered a prerequisite to implementing any retention or deletion scheme.</span></span>

- <span data-ttu-id="d7fdd-138">Étant donné le nombre de types d’informations que la plupart des organisations considèrent importantes et les calendriers de rétention des enregistrements volumineux correspondants qui y sont associés, la mise en œuvre d’une stratégie de gestion des enregistrements et de rétention des données nécessite une planification.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-138">Given the number of information types that most organizations consider important and the corresponding large records retention schedules that go along with them, implementing a data retention and records management strategy requires planning.</span></span> 

- <span data-ttu-id="d7fdd-139">La clé de l’établissement d’une stratégie de gouvernance des données efficace de ce type consiste à vous concentrer sur les fonctions d’entreprise et les types d’informations de plus haute priorité qui nécessitent une gestion plus formelle.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-139">The key to establishing an effective data governance strategy of this type is to focus on the highest priority business functions and information types that require more formal management.</span></span> <span data-ttu-id="d7fdd-140">Il s’agit par exemple de contrats légaux, financiers et de la documentation sur la conformité réglementaire.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-140">Examples are legal contracts, financial statements, and regulatory compliance documentation.</span></span> <span data-ttu-id="d7fdd-141">Essayez d’éviter d’avoir un planning de rétention distinct pour chaque type d’information unique.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-141">Try to avoid having a separate retention schedule for every single information type.</span></span> <span data-ttu-id="d7fdd-142">Essayez d’utiliser les catégories générales autant que possible, par exemple, avec des calendriers de rétention de 7 ans pour le contenu professionnel général.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-142">Try to utilize general categories as much as possible, for example, with retention schedules of 7 years for general business content.</span></span>

- <span data-ttu-id="d7fdd-143">Une fois que les types d’informations personnelles de votre environnement sont mieux connus, établissez des calendriers de rétention et de suppression pour ce type de contenu et ajustez votre architecture d’informations pour faciliter la gestion de ce type d’informations.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-143">Once the personal information types in your environment are better known, establish retention and deletion schedules for this type of content and adjust your information architecture to make governance of this sort of information easier.</span></span> <span data-ttu-id="d7fdd-144">Par exemple, isolez les informations personnelles dans des sites, bibliothèques ou dossiers distincts avec un accès contrôlé.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-144">For example, isolate personal information in separate sites, libraries, or folders with controlled access.</span></span>

### <a name="retention-policies-and-retention-labels"></a><span data-ttu-id="d7fdd-145">Stratégies de rétention et étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-145">Retention policies and retention labels</span></span>

<span data-ttu-id="d7fdd-146">Utilisez [des stratégies de rétention et des étiquettes de rétention](../compliance/retention.md) pour conserver ou supprimer du contenu dans Microsoft 365 qui contient ou est supposé contenir des données personnelles.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-146">Use [retention policies and retention labels](../compliance/retention.md) to retain or delete content in Microsoft 365 that contains or is expected to contain personal data.</span></span>

### <a name="records-management"></a><span data-ttu-id="d7fdd-147">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="d7fdd-147">Records management</span></span>

<span data-ttu-id="d7fdd-148">Utilisez des étiquettes de rétention qui déclarent le contenu a record pour mettre en œuvre une [solution de gestion des enregistrements](../compliance/records-management.md) pour les données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-148">Use retention labels that declare content a record to implement a [records management solution](../compliance/records-management.md) for data in Microsoft 365.</span></span>

<span data-ttu-id="d7fdd-149">Pour la confidentialité des données, les demandes des personnes concernées (DSR) reçues par le service juridique sont déclarées en tant qu’enregistrements et peuvent être conservées indéfiniment ou cédées avec preuve, afin de respecter les spécifications de rétention des activités réglementaires.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-149">For data privacy, data subject requests (DSRs) received by the legal department are declared a record and can be stored indefinitely or disposed of with proof, to adhere to regulatory activity retention specifications.</span></span>

