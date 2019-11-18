---
title: Utilisation d’un classificateur prêt à l’emploi (préversion)
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft 365 est fourni avec un certain nombre de classifieurs d’apprentissage automatique prêts à l’emploi que vous pouvez utiliser pour identifier et étiqueter le contenu au sein de votre organisation. Cette rubrique vous explique comment vous préparer à l’utilisation de ces classifieurs prêts à l’emploi.
ms.openlocfilehash: 3387d8fa91e88ec966e570e8eca339ebaa45fa27
ms.sourcegitcommit: 7c977771fc295ca1e4e9b16a6d05faee8edeadad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2019
ms.locfileid: "38690319"
---
# <a name="using-a-ready-to-use-classifier-preview"></a><span data-ttu-id="0db05-104">Utilisation d’un classificateur prêt à l’emploi (préversion)</span><span class="sxs-lookup"><span data-stu-id="0db05-104">Using a ready to use classifier (preview)</span></span>

<span data-ttu-id="0db05-105">Microsoft a formé et testé un nombre de classifieurs utilisant de très grands exemples de jeux de données peut vous aider à identifier certaines catégories de contenu.</span><span class="sxs-lookup"><span data-stu-id="0db05-105">Microsoft has trained and tested number of classifiers using very large sample data sets can help to identify certain categories of content.</span></span> <span data-ttu-id="0db05-106">Voir [Getting Started with trainable Classifiers (Preview)](classifier-getting-started-with.md).</span><span class="sxs-lookup"><span data-stu-id="0db05-106">See [Getting started with trainable classifiers (preview)](classifier-getting-started-with.md).</span></span> <span data-ttu-id="0db05-107">Ces classifieurs s’affichent dans `Ready to use` le groupe par défaut.</span><span class="sxs-lookup"><span data-stu-id="0db05-107">These classifiers show up in the `Ready to use` group by default.</span></span>

- <span data-ttu-id="0db05-108">**Offensant**: détecte les éléments de texte qui contiennent des blasphèmes, Slurs, taunts et des expressions déguisées (qui sont des expressions qui ont la même signification qu’un terme plus offensant).</span><span class="sxs-lookup"><span data-stu-id="0db05-108">**Offensive Language**: detects text items which contain profanities, slurs, taunts, and disguised expressions (which are expressions that have the same meaning as a more offensive term).</span></span>
- <span data-ttu-id="0db05-109">**CV**: détecte les éléments qui sont des comptes textuels des qualifications personnelles, éducatives, qualifications professionnelles, expérience professionnelle et autres informations d’identification personnelle d’un demandeur.</span><span class="sxs-lookup"><span data-stu-id="0db05-109">**Resumes**: detects items which are textual accounts of an applicant's personal, educational, professional qualifications, work experience and other personally identifying information</span></span>
- <span data-ttu-id="0db05-110">**Sourcecode**: détecte des éléments qui contiennent un ensemble d’instructions et d’instructions écrites dans des langages de programmation informatique largement utilisés.</span><span class="sxs-lookup"><span data-stu-id="0db05-110">**SourceCode**: detects items which contain a set of instructions and statements written in widely used computer programming languages.</span></span>
- <span data-ttu-id="0db05-111">**Harcèlement**: détecte une catégorie spécifique d’éléments de texte de langue choquants liés à un comportement offensant ciblant une ou plusieurs personnes en fonction des caractéristiques suivantes : race, ethnique, religion, origine nationale, sexe, orientation sexuelle, âge, invalidité.</span><span class="sxs-lookup"><span data-stu-id="0db05-111">**Harassment**: detects a specific category of offensive language text items related to offensive conduct targeting one or multiple individuals based on the following traits: race, ethnicity, religion, national origin, gender, sexual orientation, age, disability.</span></span>
- <span data-ttu-id="0db05-112">**Blasphèmes**: détecte une catégorie spécifique d’éléments de texte de langue offensants qui contiennent des expressions qui déportent la plupart des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0db05-112">**Profanity**: detects a specific category of offensive language text items which contain expressions that embarrass most people</span></span>
- <span data-ttu-id="0db05-113">**Menace**: détecte une catégorie spécifique d’éléments de texte de langue offensant liés aux menaces pour valider la violence ou causer des dommages ou dégâts physiques à une personne ou à une propriété.</span><span class="sxs-lookup"><span data-stu-id="0db05-113">**Threat**: detects a specific category of offensive language text items related to threats to commit violence or do physical harm or damage to a person or property</span></span>

> [!NOTE]
> <span data-ttu-id="0db05-114">Avant d’utiliser des classifieurs prêts à utiliser dans votre classification et votre flux de travail d’étiquetage, vous devez le tester par rapport à un échantillon du contenu de votre organisation que vous jugez adapté à la catégorie afin de vérifier que ses prévisions de classification répondent à vos attentes.</span><span class="sxs-lookup"><span data-stu-id="0db05-114">Before using ready to use classifiers in your classification and labeling workflow, you should test it against a sample of your organization's content that you feel fits the category to verify that its classification predictions meet your expectations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0db05-115">Veuillez noter que le langage offensant, le harcèlement, le catégoriseur et les classifieurs de menaces ne fonctionnent qu’avec le texte pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="0db05-115">Please note that the offensive language, harassment, profanity, and threat classifiers only work with searchable text are not exhaustive or complete.</span></span>  <span data-ttu-id="0db05-116">De plus, les normes linguistiques et culturelles changent en permanence, et à la lumière de ces réalités, Microsoft se réserve le droit de mettre à jour ces classifieurs à sa discrétion.</span><span class="sxs-lookup"><span data-stu-id="0db05-116">Further, language and cultural standards continually change, and in light of these realities, Microsoft reserves the right to update these classifiers in its discretion.</span></span> <span data-ttu-id="0db05-117">Tandis que les classifieurs peuvent aider votre organisation à surveiller le offensant et d’autres langues, les classifieurs ne traitent pas les conséquences de cette langue et ne sont pas destinés à fournir aux seuls moyens de surveillance ou de réponse à l’utilisation de cette langue.</span><span class="sxs-lookup"><span data-stu-id="0db05-117">While the classifiers may assist your organization in monitoring offensive and other language used, the classifiers do not address consequences of such language and are not intended to provide your organization’s sole means of monitoring or responding to the use of such language.</span></span> <span data-ttu-id="0db05-118">Votre organisation, et non Microsoft ou ses filiales, reste responsable de toutes les décisions relatives à la surveillance, à l’application, au blocage, à la suppression et à la rétention de tout contenu identifié par un classificateur pré-formé.</span><span class="sxs-lookup"><span data-stu-id="0db05-118">Your organization, and not Microsoft or its subsidiaries, remains responsible for all decisions related to monitoring, enforcement, blocking, removal and retention of any content identified by a pre-trained classifier.</span></span>

## <a name="how-to-prepare-for-and-use-a-ready-to-use-classifier"></a><span data-ttu-id="0db05-119">Comment préparer et utiliser un classificateur prêt à utiliser</span><span class="sxs-lookup"><span data-stu-id="0db05-119">How to prepare for and use a ready to use classifier</span></span>

1. <span data-ttu-id="0db05-120">Collecter les éléments de contenu de test jetables qui vous semblent appartenir dans la catégorie du classifieur prêt à utiliser (correspondances positives) et ceux qui ne doivent pas être inclus (correspondances négatives) dans la catégorie que vous testez.</span><span class="sxs-lookup"><span data-stu-id="0db05-120">Collect disposable test content items that you feel belong in the category of the ready to use classifier (positive matches) and ones that should not be included (negative matches) in the category you are testing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0db05-121">Les éléments de l’exemple ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="0db05-121">The sample items must not be encrypted and they must be in English.</span></span>

2. <span data-ttu-id="0db05-122">Créez un dossier SharePoint Online dédié, attendez au moins une heure pour que le dossier soit ajouté à l’index de recherche.</span><span class="sxs-lookup"><span data-stu-id="0db05-122">Create a dedicated SharePoint Online folder, wait at least an hour for the folder to be added to the search index.</span></span> <span data-ttu-id="0db05-123">Notez l’URL du dossier.</span><span class="sxs-lookup"><span data-stu-id="0db05-123">Make note of the folder URL.</span></span>

3. <span data-ttu-id="0db05-124">Connectez-vous au centre de conformité Microsoft 365 avec l’administrateur de conformité ou l’accès au rôle d’administrateur de sécurité, puis ouvrez le **Centre de conformité Microsoft 365** ou **Microsoft 365 Centre** > **de sécurité gestion des enregistrements (aperçu)** > **stratégies d’étiquette** .</span><span class="sxs-lookup"><span data-stu-id="0db05-124">Sign in to Microsoft 365 compliance center with compliance admin or security admin role access and open **Microsoft 365 compliance center** or **Microsoft 365 security center** > **Records management (preview)** > **Label policies** tab.</span></span>

4. <span data-ttu-id="0db05-125">Choisissez `Auto-apply a label`.</span><span class="sxs-lookup"><span data-stu-id="0db05-125">Choose `Auto-apply a label`.</span></span>

5. <span data-ttu-id="0db05-126">Choisissez `Choose a label to auto-apply`.</span><span class="sxs-lookup"><span data-stu-id="0db05-126">Choose `Choose a label to auto-apply`.</span></span>

6. <span data-ttu-id="0db05-127">Choisissez `Create new labels` et créez une étiquette à utiliser uniquement avec ce test.</span><span class="sxs-lookup"><span data-stu-id="0db05-127">Choose `Create new labels` and create a label for use just with this test.</span></span> <span data-ttu-id="0db05-128">Dans ce cas, conservez `Retention` la valeur OFF.</span><span class="sxs-lookup"><span data-stu-id="0db05-128">When you do this, leave `Retention` set to off.</span></span> <span data-ttu-id="0db05-129">Vous ne souhaitez pas activer une rétention ou d’autres actions.</span><span class="sxs-lookup"><span data-stu-id="0db05-129">You don't want to turn on any retention or other actions.</span></span> <span data-ttu-id="0db05-130">Dans ce cas, vous utiliserez l’étiquette de rétention simplement comme étiquette de texte, sans appliquer les actions.</span><span class="sxs-lookup"><span data-stu-id="0db05-130">In this case, you'll be using using the retention label simply as a text label, without enforcing any actions.</span></span> <span data-ttu-id="0db05-131">Par exemple, vous pouvez créer une étiquette de rétention nommée « SourceCode classificateur test » sans action, puis appliquer automatiquement cette étiquette de rétention au contenu dont la condition a le classifieur de code source.</span><span class="sxs-lookup"><span data-stu-id="0db05-131">For example, you can create a retention label named "SourceCode classifier test" with no actions, and then auto-apply that retention label to content with that has Source code classifier as a condition.</span></span> <span data-ttu-id="0db05-132">Pour en savoir plus sur la création d’étiquettes de rétention, consultez la rubrique [Overview of retention labels](labels.md).</span><span class="sxs-lookup"><span data-stu-id="0db05-132">To learn more about creating retention labels, see [Overview of retention labels](labels.md).</span></span>
  
7. <span data-ttu-id="0db05-133">Choisissez `Auto-apply a label` , puis `Choose a label to auto-apply`.</span><span class="sxs-lookup"><span data-stu-id="0db05-133">Choose `Auto-apply a label` and then `Choose a label to auto-apply`.</span></span> <span data-ttu-id="0db05-134">Pour en savoir plus sur l’utilisation de la condition basée sur une étiquette, consultez la rubrique [appliquer automatiquement une stratégie d’étiquette de rétention basée sur une condition](labels.md#applying-a-retention-label-automatically-based-on-conditions).</span><span class="sxs-lookup"><span data-stu-id="0db05-134">To learn more about using condition based auto-apply a label see, [auto-apply retention label policy based on a condition](labels.md#applying-a-retention-label-automatically-based-on-conditions).</span></span>

8. <span data-ttu-id="0db05-135">Choisissez votre étiquette de test dans la liste, `Next`puis choisissez.</span><span class="sxs-lookup"><span data-stu-id="0db05-135">Choose your test label from the list and choose `Next`.</span></span>

9. <span data-ttu-id="0db05-136">Choisissez `Apply label to content that matches a trainable classifier`.</span><span class="sxs-lookup"><span data-stu-id="0db05-136">Choose `Apply label to content that matches a trainable classifier`.</span></span>

![sélection du classifieur comme condition](media/classifier-pre-trained-apply-label-match-trainable-classifier.png)<span data-ttu-id="0db05-138">.</span><span class="sxs-lookup"><span data-stu-id="0db05-138"></span></span>

10. <span data-ttu-id="0db05-139">Choisissez votre classifieur dans la liste, dans ce cas.`Source Code`</span><span class="sxs-lookup"><span data-stu-id="0db05-139">Choose your classifier from the list, in this case `Source Code`</span></span>

11. <span data-ttu-id="0db05-140">Nommez la stratégie, par exemple « code source prêt à utiliser le test de classifieur ».</span><span class="sxs-lookup"><span data-stu-id="0db05-140">Name the policy, for example "Source code ready to use classifier test".</span></span>

12. <span data-ttu-id="0db05-141">Choisissez `Let me choose specific locations`.</span><span class="sxs-lookup"><span data-stu-id="0db05-141">Choose `Let me choose specific locations`.</span></span>

13. <span data-ttu-id="0db05-142">Désactivez tous les `SharePoint sites` emplacements sauf `Choose sites`et choisissez.</span><span class="sxs-lookup"><span data-stu-id="0db05-142">Turn off all locations except `SharePoint sites` and choose `Choose sites`.</span></span>

14. <span data-ttu-id="0db05-143">Entrez l’URL du site à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="0db05-143">Enter the URL for the site from step 2.</span></span>

15. <span data-ttu-id="0db05-144">Terminez l’Assistant et choisissez`Auto-apply`</span><span class="sxs-lookup"><span data-stu-id="0db05-144">Finish the wizard and choose `Auto-apply`</span></span>

16. <span data-ttu-id="0db05-145">Placez les éléments de test dans le dossier SharePoint Online dédié.</span><span class="sxs-lookup"><span data-stu-id="0db05-145">Place the test items into the dedicated SharePoint Online folder.</span></span>

17. <span data-ttu-id="0db05-146">Autorisez l’application de l’étiquette sur une heure.</span><span class="sxs-lookup"><span data-stu-id="0db05-146">Allow an hour for the label to be applied.</span></span>

18. <span data-ttu-id="0db05-147">Vérifiez les propriétés des documents pour l’étiquette afin de déterminer si le classifieur a inclus et exclu le contenu de test comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="0db05-147">Check the properties of the documents for the label to see if the classifier included and excluded the test content as you expected.</span></span>

19. <span data-ttu-id="0db05-148">Passez en revue les éléments qui ont été étiquetés.</span><span class="sxs-lookup"><span data-stu-id="0db05-148">Review the items that were labeled .</span></span>

20. <span data-ttu-id="0db05-149">Supprimez le contenu et la stratégie d’étiquette si vous avez fini votre test.</span><span class="sxs-lookup"><span data-stu-id="0db05-149">Delete the content, and the label policy if you are done with your testing.</span></span>

<span data-ttu-id="0db05-150">Voir aussi :</span><span class="sxs-lookup"><span data-stu-id="0db05-150">See also:</span></span>

- [<span data-ttu-id="0db05-151">Prise en main des classificateurs de formation (préversion)</span><span class="sxs-lookup"><span data-stu-id="0db05-151">Getting started with trainable classifiers (preview)</span></span>](classifier-getting-started-with.md)
- [<span data-ttu-id="0db05-152">Vue d’ensemble des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="0db05-152">Overview of retention labels</span></span>](labels.md)
- [<span data-ttu-id="0db05-153">Application automatique d’une stratégie d’étiquette de rétention basée sur une condition</span><span class="sxs-lookup"><span data-stu-id="0db05-153">Auto-apply retention label policy based on a condition</span></span>](labels.md#applying-a-retention-label-automatically-based-on-conditions)