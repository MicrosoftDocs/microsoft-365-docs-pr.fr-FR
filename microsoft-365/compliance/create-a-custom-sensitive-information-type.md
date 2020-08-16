---
title: Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/17/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Apprenez à créer, modifier, supprimer et tester des types d’informations sensibles personnalisés pour la protection contre la perte de données dans l’interface utilisateur graphique du Centre de sécurité et conformité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 0c54cd9d4969c87bbd83b3048883d8a84dd9bc59
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46686658"
---
<!-- rename md file to match the display name -->
# <a name="create-a-custom-sensitive-information-type-in-the-security--compliance-center"></a><span data-ttu-id="e99db-103">Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="e99db-103">Create a custom sensitive information type in the Security & Compliance Center</span></span>

<span data-ttu-id="e99db-104">Lisez cet article pour créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité ([https://protection.office.com](https://protection.office.com)).</span><span class="sxs-lookup"><span data-stu-id="e99db-104">Read this article to create a custom sensitive information type in the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span> <span data-ttu-id="e99db-105">Les types d’informations sensibles personnalisés que vous créez en utilisant cette méthode sont ajoutés au package de règles nommé `Microsoft.SCCManaged.CustomRulePack`.</span><span class="sxs-lookup"><span data-stu-id="e99db-105">The custom sensitive information types that you create by using this method are added to the rule package named `Microsoft.SCCManaged.CustomRulePack`.</span></span>

<span data-ttu-id="e99db-106">Vous pouvez également créer des types d’informations sensibles personnalisés à l’aide de PowerShell et de fonctionnalités de correspondance exacte des données.</span><span class="sxs-lookup"><span data-stu-id="e99db-106">You can also create custom sensitive information types by using PowerShell and Exact Data Match capabilities.</span></span> <span data-ttu-id="e99db-107">Pour en savoir plus sur ces méthodes, consultez :</span><span class="sxs-lookup"><span data-stu-id="e99db-107">To learn more about those methods, see:</span></span>
- [<span data-ttu-id="e99db-108">Créer un type d’informations sensibles personnalisé dans l’interface PowerShell du Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="e99db-108">Create a custom sensitive information type in Security & Compliance Center PowerShell</span></span>](create-a-custom-sensitive-information-type-in-scc-powershell.md)
- [<span data-ttu-id="e99db-109">Créer un type d’informations sensibles personnalisé pour DLP à l’aide d’une correspondance exacte des données</span><span class="sxs-lookup"><span data-stu-id="e99db-109">Create a custom sensitive information type for DLP with Exact Data Match (EDM)</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)

> [!NOTE]
> <span data-ttu-id="e99db-110">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="e99db-110">Microsoft 365 Information Protection now  supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="e99db-111">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="e99db-111">Chinese (simplified)</span></span>
> - <span data-ttu-id="e99db-112">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="e99db-112">Chinese (traditional)</span></span>
> - <span data-ttu-id="e99db-113">Korean</span><span class="sxs-lookup"><span data-stu-id="e99db-113">Korean</span></span>
> - <span data-ttu-id="e99db-114">Japanese</span><span class="sxs-lookup"><span data-stu-id="e99db-114">Japanese</span></span>
> 
><span data-ttu-id="e99db-115">Cette préversion est uniquement disponible dans le cloud commercial et le déploiement est limité aux pays suivants :</span><span class="sxs-lookup"><span data-stu-id="e99db-115">This preview is only in the commercial cloud and the rollout is limited to:</span></span>
> - <span data-ttu-id="e99db-116">Japon</span><span class="sxs-lookup"><span data-stu-id="e99db-116">Japan</span></span>
> - <span data-ttu-id="e99db-117">Corée</span><span class="sxs-lookup"><span data-stu-id="e99db-117">Korea</span></span>
> - <span data-ttu-id="e99db-118">Chine</span><span class="sxs-lookup"><span data-stu-id="e99db-118">China</span></span>
> - <span data-ttu-id="e99db-119">Hong Kong (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="e99db-119">Hong Kong</span></span>
> - <span data-ttu-id="e99db-120">Macao (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="e99db-120">Macau</span></span>
> - <span data-ttu-id="e99db-121">Taïwan</span><span class="sxs-lookup"><span data-stu-id="e99db-121">Taiwan</span></span>
>
><span data-ttu-id="e99db-122">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="e99db-122">This support is available for sensitive information types.</span></span> <span data-ttu-id="e99db-123">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="e99db-123">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e99db-124">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e99db-124">Before you begin</span></span>

> [!NOTE]
> <span data-ttu-id="e99db-125">Vous devez avoir une autorisation en tant qu’administrateur général ou d’administrateur de conformité pour créer, tester et déployer un type d’informations sensibles personnalisé via l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e99db-125">You should have Global admin or Compliance admin permissions to create, test, and deploy a custom sensitive information type through the UI.</span></span> <span data-ttu-id="e99db-126">Consulter [À propos des rôles d’administration](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles?view=o365-worldwide) dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="e99db-126">See [About admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles?view=o365-worldwide) in Office 365.</span></span>

- <span data-ttu-id="e99db-127">Votre organisation doit disposer d’un abonnement, par exemple, Office 365 Entreprise, qui inclut la protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="e99db-127">Your organization must have a subscription, such as Office 365 Enterprise, that includes Data Loss Prevention (DLP).</span></span> <span data-ttu-id="e99db-128">Voir [Description du service Stratégie et conformité de messagerie](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc).</span><span class="sxs-lookup"><span data-stu-id="e99db-128">See [Messaging Policy and Compliance ServiceDescription](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc).</span></span> 

- <span data-ttu-id="e99db-p106">Les types d’informations sensibles personnalisés exigent des connaissances relatives aux expressions régulières (RegEx). Pour plus d’informations sur le moteur Boost.RegEx (anciennement appelé RegEx++) utilisé pour le traitement du texte, consultez l’article [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span><span class="sxs-lookup"><span data-stu-id="e99db-p106">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="e99db-131">La division Support technique et Service clientèle Microsoft ne peut pas vous aider à créer des classifications personnalisées ou des modèles d’expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="e99db-131">Microsoft Customer Service & Support can't assist with creating custom classifications or regular expression patterns.</span></span> <span data-ttu-id="e99db-132">Les ingénieurs du support technique peuvent offrir un support limité pour la fonctionnalité, comme vous fournir des exemples de modèles d’expressions régulières à des fins de test, ou vous aider à résoudre un problème avec un modèle d’expression régulière existant qui n’opère pas de déclenchement comme prévu. En revanche, ils ne peuvent pas garantir que le développement correspondant à du contenu personnalisé répondra à vos exigences ou obligations.</span><span class="sxs-lookup"><span data-stu-id="e99db-132">Support engineers can provide limited support for the feature, such as, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected, but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="e99db-133">La protection contre la perte de données DLP utilise le robot de recherche pour identifier et classer des informations sensibles dans des sites SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="e99db-133">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites.</span></span> <span data-ttu-id="e99db-134">Pour identifier votre nouveau type d’informations sensibles personnalisé dans du contenu existant, celui-ci doit être ré-analysé.</span><span class="sxs-lookup"><span data-stu-id="e99db-134">To identify your new custom sensitive information type in existing content, the content must be re-crawled.</span></span> <span data-ttu-id="e99db-135">Le contenu est analysé sur la base d’un planning, mais vous pouvez le réanalyser manuellement pour une collection de sites, une liste ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e99db-135">Content is crawled based on a schedule, but you can manually re-crawl content for a site collection, list, or library.</span></span> <span data-ttu-id="e99db-136">Pour plus d’informations, voir [Demander manuellement l’analyse et la réindexation d’un site, d’une bibliothèque ou d’une liste](https://docs.microsoft.com/sharepoint/crawl-site-content).</span><span class="sxs-lookup"><span data-stu-id="e99db-136">For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="e99db-137">Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="e99db-137">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="e99db-138">Dans le Centre de Conformité et Sécurité, accédez à **Classifications** \> **Types d’informations sensibles** et cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="e99db-138">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="e99db-139">Les paramètres sont relativement évidents. Ils sont décrits sur la page associée de l’Assistant :</span><span class="sxs-lookup"><span data-stu-id="e99db-139">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="e99db-140">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e99db-140">**Name**</span></span>

- <span data-ttu-id="e99db-141">**Description**</span><span class="sxs-lookup"><span data-stu-id="e99db-141">**Description**</span></span>

- <span data-ttu-id="e99db-142">**Proximité**</span><span class="sxs-lookup"><span data-stu-id="e99db-142">**Proximity**</span></span>

- <span data-ttu-id="e99db-143">**Niveau de confiance**</span><span class="sxs-lookup"><span data-stu-id="e99db-143">**Confidence level**</span></span>

- <span data-ttu-id="e99db-144">**Élément de modèle principal** (mots clés, expression régulière ou dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="e99db-144">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="e99db-145">Facultatif **Éléments de modèle pris en charge** (mots clés, expression régulière ou dictionnaire) et une valeur de **Coût minimum** correspondante.</span><span class="sxs-lookup"><span data-stu-id="e99db-145">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="e99db-p109">Voici un scénario : vous souhaitez créer un type d’informations sensibles personnalisé qui détecte les numéros d’identification d’employé à 9 chiffres dans un contenu, ainsi que les mots clés « employé », « ID » et « badge ». Pour créer ce type d’informations sensibles personnalisé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e99db-p109">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="e99db-148">Dans le Centre de conformité et sécurité, accédez à **Classifications** \> **Types d’informations sensibles** et cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="e99db-148">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![Emplacement des types d’informations sensibles et bouton Créer](../media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="e99db-150">Sur la page **Choisir un nom et une description** qui s’ouvre, entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e99db-150">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="e99db-151">**Nom** : ID d’employé.</span><span class="sxs-lookup"><span data-stu-id="e99db-151">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="e99db-152">**Description** : détecte les numéros d’identification d’employé Contoso à neuf chiffres.</span><span class="sxs-lookup"><span data-stu-id="e99db-152">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![Nom et page de description](../media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="e99db-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e99db-154">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="e99db-155">Sur la page **Conditions requises pour la correspondance** qui s’ouvre, cliquez sur **Ajouter un élément** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e99db-155">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="e99db-156">**Détecter le contenu contenant** :</span><span class="sxs-lookup"><span data-stu-id="e99db-156">**Detect content containing**:</span></span>
 
      <span data-ttu-id="e99db-p110">a. Cliquez sur **L’un de ces éléments** et sélectionnez **Expression régulière**.</span><span class="sxs-lookup"><span data-stu-id="e99db-p110">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="e99db-p111">b. Dans la zone de l’expression régulière, entrez `(\s)(\d{9})(\s)` (numéros à neuf chiffres encadrés d’un espace blanc)</span><span class="sxs-lookup"><span data-stu-id="e99db-p111">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="e99db-161">**Éléments de prise en charge** : cliquez sur **Ajouter des éléments de prise en charge** et sélectionnez **Contient cette liste de mots clés**.</span><span class="sxs-lookup"><span data-stu-id="e99db-161">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="e99db-162">Dans la zone **Contient cette liste de mots clés** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e99db-162">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="e99db-163">**Liste de mots clés** : saisissez la valeur suivante : employé, ID, badge.</span><span class="sxs-lookup"><span data-stu-id="e99db-163">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="e99db-164">**Nombre minimal** : conservez la valeur par défaut 1.</span><span class="sxs-lookup"><span data-stu-id="e99db-164">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="e99db-165">Conservez la valeur par défaut **Niveau de confiance** 60.</span><span class="sxs-lookup"><span data-stu-id="e99db-165">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="e99db-166">Conservez la valeur par défaut **Caractère de proximité** 300.</span><span class="sxs-lookup"><span data-stu-id="e99db-166">Leave the default **Character proximity** value 300.</span></span>

    ![Configuration requise pour la page correspondante](../media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="e99db-168">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e99db-168">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="e99db-169">Sur la page **Revoir et finaliser** qui s’affiche, passez en revue les paramètres, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="e99db-169">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![Examen et finalisation de la page](../media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="e99db-p112">La page suivante vous encourage à tester le nouveau type d’informations sensibles personnalisés en cliquant sur **Oui**. Pour plus d’informations, reportez-vous à l’article [Tester des types d’informations sensibles personnalisés dans le Centre de conformité et sécurité](#test-custom-sensitive-information-types-in-the-security--compliance-center). Sinon, cliquez sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="e99db-p112">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![Page de recommandation de test](../media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e99db-175">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="e99db-175">How do you know this worked?</span></span>

<span data-ttu-id="e99db-176">Pour vérifier que vous avez correctement créé un nouveau type d’informations sensibles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e99db-176">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="e99db-177">Accédez à **Classifications** \> **Types d’informations sensibles** et vérifiez que le nouveau type d’informations sensibles personnalisé apparaît.</span><span class="sxs-lookup"><span data-stu-id="e99db-177">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="e99db-p113">Testez le nouveau type d’informations sensibles personnalisés. Pour plus d’informations, reportez-vous à la rubrique [Tester des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="e99db-p113">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="e99db-180">Modifier des types d’informations sensibles personnalisés dans le Centre de conformité et sécurité</span><span class="sxs-lookup"><span data-stu-id="e99db-180">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="e99db-181">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="e99db-181">**Notes**:</span></span>
<!-- check to see if this note contradicts the guidance in "customize a built in sensitive information type customize-a-built-in-sensitive-information-type it sure seems like it does-->
- <span data-ttu-id="e99db-p114">Vous pouvez modifier uniquement les types d’informations sensibles personnalisés ; vous ne pouvez pas modifier les types d’informations sensibles intégrés. Cependant, vous pouvez utiliser PowerShell pour exporter des types d’informations sensibles personnalisés intégrés, les personnaliser et les importer comme types d’informations sensibles personnalisés. Pour plus d’informations, consultez la rubrique [Personnaliser un type d’informations sensibles intégré](customize-a-built-in-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="e99db-p114">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="e99db-p115">Vous pouvez uniquement modifier les types d’informations sensibles personnalisés que vous avez créés dans l’interface utilisateur. Si vous avez utilisé la [procédure PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) pour importer un package de règles pour les types d’informations sensibles personnalisés, vous recevrez une erreur.</span><span class="sxs-lookup"><span data-stu-id="e99db-p115">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="e99db-187">Dans le Centre de conformité et sécurité, accédez à **Classifications** \> **Types d’informations sensibles**, sélectionnez le type d’informations sensibles personnalisé à modifier, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="e99db-187">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![Emplacement des types d’informations sensibles et bouton Modifier](../media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="e99db-p116">Les mêmes options sont disponibles ici comme lorsque vous avez créé le type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité. Pour plus d’informations, consultez la rubrique [Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="e99db-p116">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e99db-191">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="e99db-191">How do you know this worked?</span></span>

<span data-ttu-id="e99db-192">Pour vérifier que vous avez correctement modifié un type d’informations sensibles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e99db-192">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="e99db-193">Accédez à **Classifications** \> **Types d’informations sensibles** pour vérifier les propriétés du type d’informations sensibles personnalisé modifié.</span><span class="sxs-lookup"><span data-stu-id="e99db-193">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="e99db-p117">Testez le type d’informations sensibles personnalisés modifié. Pour plus d’informations, reportez-vous à la rubrique [Tester des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="e99db-p117">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="e99db-196">Supprimer des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="e99db-196">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="e99db-197">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="e99db-197">**Notes**:</span></span>

- <span data-ttu-id="e99db-198">Vous pouvez uniquement supprimer des types d’informations sensibles personnalisés ; vous ne pouvez pas supprimer des types d’informations sensibles intégrés.</span><span class="sxs-lookup"><span data-stu-id="e99db-198">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="e99db-199">Avant de supprimer un type d’informations sensibles personnalisé, vérifiez qu’aucune stratégie DLP ou règle de flux de courrier Exchange (également appelées règles de transport) ne référence toujours le type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="e99db-199">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="e99db-200">Dans le Centre de Conformité et Sécurité, accédez à **Classifications** \> **Types d’informations sensibles** et sélectionnez un ou plusieurs types d’informations sensibles personnalisés à supprimer.</span><span class="sxs-lookup"><span data-stu-id="e99db-200">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="e99db-201">Dans la boîte de dialogue qui s’ouvre, cliquez sur **Supprimer** (ou **Supprimer des types d’informations sensibles** si vous en avez sélectionnés plusieurs).</span><span class="sxs-lookup"><span data-stu-id="e99db-201">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![Emplacement des types d’informations sensibles et bouton Supprimer](../media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="e99db-203">Cliquez sur **Oui** lorsque le message d’avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e99db-203">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e99db-204">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="e99db-204">How do you know this worked?</span></span>

<span data-ttu-id="e99db-205">Pour vérifier que vous avez supprimé correctement un type d’informations sensibles personnalisé, accédez à **Classifications** \> **Types d’informations sensibles** pour vérifier que le type d’informations sensibles personnalisé n’est plus répertorié.</span><span class="sxs-lookup"><span data-stu-id="e99db-205">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="e99db-206">Tester des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="e99db-206">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="e99db-207">Dans le Centre de Conformité et Sécurité, accédez à **Classifications** \> **Types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="e99db-207">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="e99db-p118">Sélectionnez un ou plusieurs types d’informations sensibles personnalisés à tester. Dans la boîte de dialogue qui s’ouvre, cliquez sur **Type de test** (ou **Tester des types d’informations sensibles** si vous en avez sélectionnés plusieurs).</span><span class="sxs-lookup"><span data-stu-id="e99db-p118">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![Emplacement des types d’informations sensibles et bouton Tester le type](../media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="e99db-211">Dans la page **Télécharger le fichier à tester** qui s’ouvre, chargez un document à tester en faisant glisser un fichier ou en cliquant sur **Parcourir** et en sélectionnant un fichier.</span><span class="sxs-lookup"><span data-stu-id="e99db-211">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![Charger le fichier sur la page de test](../media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="e99db-213">Cliquez sur le bouton **Tester** pour rechercher des modèles dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="e99db-213">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="e99db-214">Sur la page **Mettre en correspondance les résultats**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="e99db-214">On the **Match results** page, click **Finish**.</span></span>

    ![Mettre en correspondance les résultats](../media/scc-cust-sens-info-type-test-results.png)
