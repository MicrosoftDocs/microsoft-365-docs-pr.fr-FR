---
title: Régir les informations soumises à la réglementation sur la confidentialité des données
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
description: Utilisez les étiquettes et stratégies de rétention Microsoft 365 pour gérer les données personnelles dans votre environnement Microsoft 365.
ms.openlocfilehash: 62c2386ac8f9c5b31650df8be2c2a411d8b75959
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50928435"
---
# <a name="govern-information-subject-to-data-privacy-regulation"></a><span data-ttu-id="1c723-103">Régir les informations soumises à la réglementation sur la confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="1c723-103">Govern information subject to data privacy regulation</span></span>

<span data-ttu-id="1c723-104">Les contrôles de gouvernance des informations peuvent être utilisés dans votre environnement pour répondre aux besoins de conformité de la confidentialité des données, y compris un nombre spécifique au Règlement général sur la protection des données (RGPD), HIPAA-HITECH (loi américaine sur la confidentialité des soins de santé), au CCPA (California Consumer Protection Act) et au LGPD (Brazil Data Protection Act).</span><span class="sxs-lookup"><span data-stu-id="1c723-104">Information governance controls can be employed in your environment to help address data privacy compliance needs, including a number that are specific to General Data Protection Regulation (GDPR), HIPAA-HITECH (the United States health care privacy act), California Consumer Protection Act (CCPA), and the Brazil Data Protection Act (LGPD).</span></span> 

<span data-ttu-id="1c723-105">Ces contrôles sont principalement pris en compte dans les zones de solution suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c723-105">These controls primarily fall into the following solution areas:</span></span>

- <span data-ttu-id="1c723-106">Stratégies de conservation</span><span class="sxs-lookup"><span data-stu-id="1c723-106">Retention policies</span></span>
- <span data-ttu-id="1c723-107">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="1c723-107">Retention labels</span></span>
- <span data-ttu-id="1c723-108">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="1c723-108">Records management</span></span>

## <a name="data-privacy-regulations-impacting-information-governance-controls"></a><span data-ttu-id="1c723-109">Réglementations en matière de confidentialité des données qui ont un impact sur les contrôles de gouvernance des informations</span><span class="sxs-lookup"><span data-stu-id="1c723-109">Data privacy regulations impacting information governance controls</span></span>

<span data-ttu-id="1c723-110">Voici un exemple de liste des réglementations de confidentialité des données qui peuvent être liées aux contrôles de gouvernance des informations :</span><span class="sxs-lookup"><span data-stu-id="1c723-110">Here is a sample listing of data privacy regulations that may relate to information governance controls:</span></span>

- <span data-ttu-id="1c723-111">Article R GDPR (13)(2)(a)</span><span class="sxs-lookup"><span data-stu-id="1c723-111">GDPR Article (13)(2)(a)</span></span>
- <span data-ttu-id="1c723-112">Article R GDPR (5)(1)(f)</span><span class="sxs-lookup"><span data-stu-id="1c723-112">GDPR Article (5)(1)(f)</span></span>
- <span data-ttu-id="1c723-113">HIPAA-HITECH (45 CFR 164.312(c)(2))</span><span class="sxs-lookup"><span data-stu-id="1c723-113">HIPAA-HITECH (45 CFR 164.312(c)(2))</span></span>
- <span data-ttu-id="1c723-114">HIPAA-HITECH (45 CFR 164.316(b)(1)(i))</span><span class="sxs-lookup"><span data-stu-id="1c723-114">HIPAA-HITECH (45 CFR 164.316(b)(1)(i))</span></span>
- <span data-ttu-id="1c723-115">HIPAA-HITECH (45 CFR 164.316(b)(1)(ii))</span><span class="sxs-lookup"><span data-stu-id="1c723-115">HIPAA-HITECH (45 CFR 164.316(b)(1)(ii))</span></span>
- <span data-ttu-id="1c723-116">LGPD Article 46</span><span class="sxs-lookup"><span data-stu-id="1c723-116">LGPD Article 46</span></span>

<span data-ttu-id="1c723-117">Pour plus d’informations sur ces réglementations, consultez l’article d’évaluation des risques de confidentialité des données [et d’identification des informations sensibles.](information-protection-deploy-assess.md)</span><span class="sxs-lookup"><span data-stu-id="1c723-117">For more information on these regulations, see the [assess data privacy risks and identify sensitive information article](information-protection-deploy-assess.md).</span></span>

<span data-ttu-id="1c723-118">Pour la gouvernance des informations, les réglementations en matière de confidentialité des données appellent généralement les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c723-118">For information governance, data privacy regulations typically call for the following:</span></span>

- <span data-ttu-id="1c723-119">Vous devez utiliser un schéma technique pour la rétention et la suppression des données personnelles stockées dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c723-119">You should employ a technical scheme for retention and deletion for personal data stored in Microsoft 365.</span></span>
- <span data-ttu-id="1c723-120">Si vous comptez stocker des données personnelles, informez l’objet de la durée de stock des données, ce qui est désormais une pratique standard sur les systèmes web frontaux.</span><span class="sxs-lookup"><span data-stu-id="1c723-120">If you're going to store personal data, inform the subject of how long the data will be stored, which is a standard practice now on front-end web systems.</span></span>
- <span data-ttu-id="1c723-121">Les données personnelles doivent être protégées contre le traitement accidentel, la perte ou l’altération à l’aide de méthodes vérifiables.</span><span class="sxs-lookup"><span data-stu-id="1c723-121">Personal data should be protected against accidental processing, loss, or alteration using verifiable methods.</span></span>
- <span data-ttu-id="1c723-122">Toute action exécutée sur des données personnelles doit être documentée et cette documentation doit être conservée pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1c723-122">Any action executed against personal data should be documented and that documentation should be retained for a specified period.</span></span>

<span data-ttu-id="1c723-123">Étant donné que les réglementations en matière de confidentialité des données ne sont pas très spécifiques en matière de rétention et de suppression des données, d’autres facteurs doivent être pris en compte pour dicter les instructions de gouvernance des informations relatives aux informations personnelles stockées dans votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c723-123">Because the data privacy regulations are not very specific when it comes to data retention and deletion, other factors need to be taken into consideration that may dictate information governance guidelines for personal information stored in your Microsoft 365 subscription.</span></span> <span data-ttu-id="1c723-124">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="1c723-124">Here are a few examples:</span></span>

- <span data-ttu-id="1c723-125">L’âge des comptes consommateur après 5 ans d’inactivité et nécessite la suppression ou l’anonymisation des données de compte après ce point, nécessitant une orchestration entre le système stockant les données et les flux de travail liés aux notifications et à d’autres automatisations.</span><span class="sxs-lookup"><span data-stu-id="1c723-125">Aging out consumer accounts after 5 years of inactivity and requires deletion or anonymization of account data after that point, requiring orchestration between the system storing the data and workflows related to notifications and other automation.</span></span>
- <span data-ttu-id="1c723-126">Configuration des règles de conservation des stratégies et procédures liées au R GDPR pendant trois ans après leur sur-place, ce qui s’aligne sur la planification de rétention de l’organisation pour les stratégies et procédures.</span><span class="sxs-lookup"><span data-stu-id="1c723-126">Configuring rules for keeping policies and procedures related to GDPR around for three years after they've been superseded, which aligns with the organization's retention schedule for policies and procedures.</span></span>
- <span data-ttu-id="1c723-127">Maintien d’un abonnement distinct pour la communication avec les consommateurs via son organisation de support.</span><span class="sxs-lookup"><span data-stu-id="1c723-127">Maintaining a separate subscription for communicating with consumers through its support organization.</span></span> <span data-ttu-id="1c723-128">Toutes les communications par courrier électronique ont été conservées et supprimées au bout de deux semaines afin de réduire l’endettement de confidentialité dans le système.</span><span class="sxs-lookup"><span data-stu-id="1c723-128">All email communications were retained and deleted after two weeks to reduce any privacy debt buildup in the system.</span></span>

<span data-ttu-id="1c723-129">Une question clé à se poser est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1c723-129">A key question to answer is:</span></span> 

- <span data-ttu-id="1c723-130">Combien de temps les informations contenant des données personnelles doivent-elles être conservées pour des raisons professionnelles valides afin d’éviter de « les conserver indéfiniment » ?</span><span class="sxs-lookup"><span data-stu-id="1c723-130">How long does information containing personal data need to be kept around for valid business reasons to avoid "keep it forever" practices?</span></span> <span data-ttu-id="1c723-131">Cela doit être équilibré avec les besoins de rétention pour la continuité de l’activité.</span><span class="sxs-lookup"><span data-stu-id="1c723-131">This must be balanced with retention needs for business continuity.</span></span>

<span data-ttu-id="1c723-132">Quelles que soient les raisons juridiques et professionnelles de conserver des informations personnelles ou de les supprimer, Microsoft fournit un certain nombre de fonctionnalités pour implémenter votre modèle de gouvernance des données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c723-132">Regardless of the legal and business reasons for keeping personal information around or deleting it, Microsoft provides a number of capabilities to implement your data governance scheme in Microsoft 365.</span></span>

## <a name="managing-information-governance-in-microsoft-365"></a><span data-ttu-id="1c723-133">Gestion de la gouvernance des informations dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1c723-133">Managing information governance in Microsoft 365</span></span>

<span data-ttu-id="1c723-134">Pour commencer, voir [Gérer la gouvernance des informations](../compliance/manage-information-governance.md) et la rétention, la suppression et la destruction des données dans Microsoft [365.](/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview)</span><span class="sxs-lookup"><span data-stu-id="1c723-134">To begin, see [Manage information governance](../compliance/manage-information-governance.md) and [Data Retention, Deletion and Destruction in Microsoft 365](/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview).</span></span>

### <a name="develop-data-retention-schedules-for-containers-email-and-content"></a><span data-ttu-id="1c723-135">Développer des planifications de rétention des données pour les conteneurs, la messagerie et le contenu</span><span class="sxs-lookup"><span data-stu-id="1c723-135">Develop data retention schedules for containers, email, and content</span></span>

<span data-ttu-id="1c723-136">Gardez les éléments suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="1c723-136">Keep the following in mind:</span></span>

- <span data-ttu-id="1c723-137">L’établissement d’une planification de rétention des données pour les types d’informations définis doit être considéré comme une condition préalable à l’implémentation de tout schéma de rétention ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="1c723-137">Establishing a data retention schedule for defined information types should be considered a prerequisite to implementing any retention or deletion scheme.</span></span>

- <span data-ttu-id="1c723-138">Étant donné le nombre de types d’informations que la plupart des organisations considèrent comme importants et les planifications de rétention des enregistrements importantes correspondantes qui vont de même, l’implémentation d’une stratégie de rétention et de gestion des enregistrements de données nécessite une planification.</span><span class="sxs-lookup"><span data-stu-id="1c723-138">Given the number of information types that most organizations consider important and the corresponding large records retention schedules that go along with them, implementing a data retention and records management strategy requires planning.</span></span> 

- <span data-ttu-id="1c723-139">La clé de l’établissement d’une stratégie de gouvernance des données efficace de ce type consiste à se concentrer sur les fonctions métiers et les types d’informations les plus prioritaires qui nécessitent une gestion plus formelle.</span><span class="sxs-lookup"><span data-stu-id="1c723-139">The key to establishing an effective data governance strategy of this type is to focus on the highest priority business functions and information types that require more formal management.</span></span> <span data-ttu-id="1c723-140">Les contrats juridiques, les états financiers et la documentation de conformité réglementaire en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="1c723-140">Examples are legal contracts, financial statements, and regulatory compliance documentation.</span></span> <span data-ttu-id="1c723-141">Essayez d’éviter d’avoir une planification de rétention distincte pour chaque type d’informations unique.</span><span class="sxs-lookup"><span data-stu-id="1c723-141">Try to avoid having a separate retention schedule for every single information type.</span></span> <span data-ttu-id="1c723-142">Essayez d’utiliser autant que possible des catégories générales, par exemple, avec des planifications de rétention de 7 ans pour le contenu d’entreprise général.</span><span class="sxs-lookup"><span data-stu-id="1c723-142">Try to utilize general categories as much as possible, for example, with retention schedules of 7 years for general business content.</span></span>

- <span data-ttu-id="1c723-143">Une fois que les types d’informations personnelles de votre environnement sont mieux connus, établissez des planifications de rétention et de suppression pour ce type de contenu et ajustez votre architecture des informations pour faciliter la gouvernance de ce type d’informations.</span><span class="sxs-lookup"><span data-stu-id="1c723-143">Once the personal information types in your environment are better known, establish retention and deletion schedules for this type of content and adjust your information architecture to make governance of this sort of information easier.</span></span> <span data-ttu-id="1c723-144">Par exemple, isolez les informations personnelles dans des sites, des bibliothèques ou des dossiers distincts avec un accès contrôlé.</span><span class="sxs-lookup"><span data-stu-id="1c723-144">For example, isolate personal information in separate sites, libraries, or folders with controlled access.</span></span>

### <a name="retention-policies-and-retention-labels"></a><span data-ttu-id="1c723-145">Stratégies de rétention et étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="1c723-145">Retention policies and retention labels</span></span>

<span data-ttu-id="1c723-146">Utilisez [des stratégies de rétention](../compliance/retention.md) et des étiquettes de rétention pour conserver ou supprimer du contenu dans Microsoft 365 qui contient ou est censé contenir des données personnelles.</span><span class="sxs-lookup"><span data-stu-id="1c723-146">Use [retention policies and retention labels](../compliance/retention.md) to retain or delete content in Microsoft 365 that contains or is expected to contain personal data.</span></span>

### <a name="records-management"></a><span data-ttu-id="1c723-147">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="1c723-147">Records management</span></span>

<span data-ttu-id="1c723-148">Utilisez des étiquettes de rétention qui déclarent le contenu d’un enregistrement pour implémenter une solution de [gestion](../compliance/records-management.md) des enregistrements pour les données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c723-148">Use retention labels that declare content a record to implement a [records management solution](../compliance/records-management.md) for data in Microsoft 365.</span></span>

<span data-ttu-id="1c723-149">Pour la confidentialité des données, les demandes des personnes responsables des données reçues par le service juridique sont déclarées comme un enregistrement et peuvent être stockées indéfiniment ou éliminées avec preuve, afin de respecter les spécifications de rétention des activités réglementaires.</span><span class="sxs-lookup"><span data-stu-id="1c723-149">For data privacy, data subject requests (DSRs) received by the legal department are declared a record and can be stored indefinitely or disposed of with proof, to adhere to regulatory activity retention specifications.</span></span>