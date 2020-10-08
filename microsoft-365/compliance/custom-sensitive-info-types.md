---
title: Types d’informations sensibles personnalisés pour la protection contre la perte de données (DLP)
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/23/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: Obtenez une vue d’ensemble des types d’informations sensibles personnalisés pour la protection contre la perte de données (DLP), tels que le modèle primaire, la proximité des caractères et le niveau de confiance.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: d21d0be23847a8fbd27b6082ca28cdca2d4eed05
ms.sourcegitcommit: 5e40c760c1af2a4cc6d85cb782b17f5c979677c5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48379169"
---
# <a name="custom-sensitive-information-types"></a><span data-ttu-id="c2c92-103">Types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="c2c92-103">Custom sensitive information types</span></span>

<span data-ttu-id="c2c92-104">Microsoft 365 inclut différents types d’informations sensibles intégrés prêts à l’emploi, par exemple, pour la [protection contre la perte de données](data-loss-prevention-policies.md) (DLP) ou avec [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span><span class="sxs-lookup"><span data-stu-id="c2c92-104">Microsoft 365 includes many built-in sensitive information types that are ready for you to use in your organization, such as for [data loss prevention](data-loss-prevention-policies.md) (DLP), or with [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span></span> <span data-ttu-id="c2c92-105">Les types d’informations sensibles intégrés peuvent aider à identifier et à protéger des numéros de carte de crédit, de compte bancaire, de passeport et autres sur la base de modèles définis par une expression régulière (regex) ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="c2c92-105">Built-in sensitive information types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more, based on patterns that are defined by a regular expression (regex) or a function.</span></span> <span data-ttu-id="c2c92-106">Pour en savoir plus, voir [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="c2c92-106">To learn more, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>

<span data-ttu-id="c2c92-107">Mais que se passe-t-il si vous devez identifier et protéger un autre type d’informations sensibles, par exemple, des ID d’employé ou des numéros de projet, à l’aide d’un format spécifique de votre organisation ?</span><span class="sxs-lookup"><span data-stu-id="c2c92-107">But what if you need to identify and protect a different type of sensitive information, such as for employee IDs or project numbers, using a format that's specific to your organization?</span></span> <span data-ttu-id="c2c92-108">Vous pouvez créer un type d’informations sensibles personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c2c92-108">To do this, you can create a custom sensitive information type.</span></span>

<span data-ttu-id="c2c92-109">Les éléments fondamentaux d’un type d’informations sensibles personnalisé sont :</span><span class="sxs-lookup"><span data-stu-id="c2c92-109">The fundamental parts of a custom sensitive information type are:</span></span>

- <span data-ttu-id="c2c92-110">**Modèle principal** : numéros d’identification d’employé, numéros de projet, etc. Cela est généralement identifié par une expression régulière (RegEx) mais il peut aussi s’agir d’une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c2c92-110">**Primary pattern**: employee ID numbers, project numbers, etc. This is typically identified by a regular expression (RegEx), but it can also be a list of keywords.</span></span>

- <span data-ttu-id="c2c92-p103">**Preuves supplémentaires** : supposons que vous recherchez un numéro d’identification d’employé à neuf chiffres. Tous les numéros à neuf chiffres ne sont pas des numéros d’identification d’employé, donc vous pouvez rechercher un texte supplémentaire : les mots clés comme « employé », « badge », « ID » ou d’autres modèles de texte suivant d’autres expressions régulières. Cette preuve (également appelée preuve _justificative_ ou _probante_) augmente la probabilité que le nombre à neuf chiffres trouvé dans le contenu est réellement un numéro d’identification d’employé.</span><span class="sxs-lookup"><span data-stu-id="c2c92-p103">**Additional evidence**: Suppose you're looking for a nine-digit employee ID number. Not all nine-digit numbers are employee ID numbers, so you can look for additional text: keywords like "employee", "badge", "ID", or other text patterns based on additional regular expressions. This supporting evidence (also known as _supporting_ or _corroborative_ evidence) increases the likelihood that nine-digit number found in content is really an employee ID number.</span></span>

- <span data-ttu-id="c2c92-p104">**Proximité de caractère** : il est logique que plus le modèle principal et la preuve justificative sont proches, plus le contenu détecté a des chances d’être ce que vous recherchez. Vous pouvez spécifier la distance de caractère entre le modèle principal et la preuve justificative (également appelée _fenêtre de proximité_) comme illustré dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="c2c92-p104">**Character proximity**: It makes sense that the closer the primary pattern and the supporting evidence are to each other, the more likely the detected content is going to be what you're looking for. You can specify the character distance between the primary pattern and the supporting evidence (also known as the _proximity window_) as shown in the following diagram:</span></span>

    ![Diagramme de la fenêtre de proximité et de preuves probantes](../media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- <span data-ttu-id="c2c92-p105">**Niveau de confiance** : plus la preuve que vous possédez est justificative, plus la probabilité qu’un résultat contienne les informations sensibles que vous recherchez est élevée. Vous pouvez affecter des niveaux de confiance supérieurs pour les correspondances détectées en utilisant plus de preuves.</span><span class="sxs-lookup"><span data-stu-id="c2c92-p105">**Confidence level**: The more supporting evidence you have, the higher the likelihood that a match contains the sensitive information you're looking for. You can assign higher levels of confidence for matches that are detected by using more evidence.</span></span>

  <span data-ttu-id="c2c92-p106">Lorsqu’il est satisfait, un modèle renvoie un nombre et un niveau de confiance, que vous pouvez utiliser dans les conditions dans votre stratégie DLP. Lorsque vous ajoutez une condition de détection d’un type d’informations sensibles à une stratégie DLP, vous pouvez modifier le nombre et le niveau de confiance comme illustré dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="c2c92-p106">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policies. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown in the following diagram:</span></span>

    ![Nombre d’instances et options de précision de correspondance](../media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

## <a name="creating-custom-sensitive-information-types"></a><span data-ttu-id="c2c92-122">Création de types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="c2c92-122">Creating custom sensitive information types</span></span>

<span data-ttu-id="c2c92-123">Pour créer des types d’informations sensibles personnalisés dans le Centre de sécurité et conformité, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2c92-123">To create custom sensitive information types in the Security & Compliance Center, you can choose from several options:</span></span>

- <span data-ttu-id="c2c92-124">**Utiliser EDM** Vous pouvez configurer des types d’informations sensibles personnalisés à l’aide d’une classification de correspondance exacte des données (EDM).</span><span class="sxs-lookup"><span data-stu-id="c2c92-124">**Use EDM** You can set up custom sensitive information types using Exact Data Match (EDM)-based classification.</span></span> <span data-ttu-id="c2c92-125">Cette méthode vous permet de créer un type d’informations sensibles dynamique à l’aide d’une base de données sécurisée que vous pouvez actualiser régulièrement.</span><span class="sxs-lookup"><span data-stu-id="c2c92-125">This method enables you to create a dynamic sensitive information type using a secure database that you can refresh periodically.</span></span> <span data-ttu-id="c2c92-126">Voir l’article sur la [création d’un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span><span class="sxs-lookup"><span data-stu-id="c2c92-126">See [Create a custom sensitive information type with Exact Data Match based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

- <span data-ttu-id="c2c92-127">**Utiliser PowerShell** vous pouvez configurer des types d’informations sensibles personnalisés à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2c92-127">**Use PowerShell** You can set up custom sensitive information types using PowerShell.</span></span> <span data-ttu-id="c2c92-128">Bien que cette méthode soit plus complexe que celle de l’interface utilisateur, elle offre davantage d’options de configuration.</span><span class="sxs-lookup"><span data-stu-id="c2c92-128">Although this method is more complex than using the UI, you have more configuration options.</span></span> <span data-ttu-id="c2c92-129">Voir [Créer un type d’informations sensibles personnalisé dans l’interface PowerShell du Centre de sécurité et conformité](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c2c92-129">See [Create a custom sensitive information type in Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>

- <span data-ttu-id="c2c92-130">**Utiliser l’interface utilisateur** Vous pouvez configurer un type d’informations sensibles personnalisé à l’aide de l’interface utilisateur du Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="c2c92-130">**Use the UI** You can set up a custom sensitive information type using the Security & Compliance Center UI.</span></span> <span data-ttu-id="c2c92-131">Cette méthode vous permet d’utiliser des expressions régulières, des mots clés et des dictionnaires de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c2c92-131">With this method, you can use regular expressions, keywords, and keyword dictionaries.</span></span> <span data-ttu-id="c2c92-132">Pour en savoir plus, voir [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="c2c92-132">To learn more, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c2c92-133">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="c2c92-133">Microsoft 365 Information Protection now  supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="c2c92-134">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="c2c92-134">Chinese (simplified)</span></span>
> - <span data-ttu-id="c2c92-135">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="c2c92-135">Chinese (traditional)</span></span>
> - <span data-ttu-id="c2c92-136">Korean</span><span class="sxs-lookup"><span data-stu-id="c2c92-136">Korean</span></span>
> - <span data-ttu-id="c2c92-137">Japanese</span><span class="sxs-lookup"><span data-stu-id="c2c92-137">Japanese</span></span>
> 
><span data-ttu-id="c2c92-138">Cette préversion est uniquement disponible dans le cloud commercial et le déploiement est limité aux pays suivants :</span><span class="sxs-lookup"><span data-stu-id="c2c92-138">This preview is only in the commercial cloud and the rollout is limited to:</span></span>
> - <span data-ttu-id="c2c92-139">Japon</span><span class="sxs-lookup"><span data-stu-id="c2c92-139">Japan</span></span>
> - <span data-ttu-id="c2c92-140">Corée</span><span class="sxs-lookup"><span data-stu-id="c2c92-140">Korea</span></span>
> - <span data-ttu-id="c2c92-141">Chine</span><span class="sxs-lookup"><span data-stu-id="c2c92-141">China</span></span>
> - <span data-ttu-id="c2c92-142">Hong Kong (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="c2c92-142">Hong Kong</span></span>
> - <span data-ttu-id="c2c92-143">Macao (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="c2c92-143">Macau</span></span>
> - <span data-ttu-id="c2c92-144">Taïwan</span><span class="sxs-lookup"><span data-stu-id="c2c92-144">Taiwan</span></span>
>
><span data-ttu-id="c2c92-145">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="c2c92-145">This support is available for sensitive information types.</span></span> <span data-ttu-id="c2c92-146">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="c2c92-146">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

