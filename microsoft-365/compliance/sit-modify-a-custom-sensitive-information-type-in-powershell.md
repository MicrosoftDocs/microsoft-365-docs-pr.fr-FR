---
title: Modifier un type d’informations sensibles personnalisé à l’aide de PowerShell
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment modifier des informations sensibles personnalisées à l’aide de PowerShell.
ms.openlocfilehash: 9f8a9ef119e632c695113320ab86a3bdfef8a197
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322697"
---
# <a name="modify-a-custom-sensitive-information-type-using-powershell"></a><span data-ttu-id="4b439-103">Modifier un type d’informations sensibles personnalisé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b439-103">Modify a custom sensitive information type using PowerShell</span></span>

<span data-ttu-id="4b439-104">Dans PowerShell du centre de conformité, la modification d’un type d’informations sensibles personnalisé nécessite :</span><span class="sxs-lookup"><span data-stu-id="4b439-104">In Compliance center PowerShell, modifying a custom sensitive information type requires you to:</span></span>

1. <span data-ttu-id="4b439-105">Exportez le package de règles existant qui contient le type d’informations sensibles personnalisé dans un fichier XML (ou utilisez le fichier XML existant si vous avez un).</span><span class="sxs-lookup"><span data-stu-id="4b439-105">Export the existing rule package that contains the custom sensitive information type to an XML file (or use the existing XML file if you have it).</span></span>

2. <span data-ttu-id="4b439-106">Modifier le type d’informations sensibles personnalisé dans un fichier exporté XML.</span><span class="sxs-lookup"><span data-stu-id="4b439-106">Modify the custom sensitive information type in the exported XML file.</span></span>

3. <span data-ttu-id="4b439-107">Importer le fichier XML mis à jour vers le package de règles existant.</span><span class="sxs-lookup"><span data-stu-id="4b439-107">Import the updated XML file back into the existing rule package.</span></span>

<span data-ttu-id="4b439-108">Pour vous connecter à PowerShell du centre de conformité, consultez [Se connecter à PowerShell du centre de conformité](/powershell/exchange/exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="4b439-108">To connect to Compliance Center PowerShell, see [Connect to Compliance Center PowerShell](/powershell/exchange/exchange-online-powershell).</span></span>

### <a name="step-1-export-the-existing-rule-package-to-an-xml-file"></a><span data-ttu-id="4b439-109">Étape 1 : Exporter le package de règles existant vers un fichier XML</span><span class="sxs-lookup"><span data-stu-id="4b439-109">Step 1: Export the existing rule package to an XML file</span></span>

> [!NOTE]
> <span data-ttu-id="4b439-110">Si vous avez une copie du fichier XML (par exemple, vous venez de le créer et de l’importer), vous pouvez passer directement à l’étape suivante pour modifier le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="4b439-110">If you have a copy of the XML file (for example, you just created and imported it), you can skip to the next step to modify the XML file.</span></span>

1. <span data-ttu-id="4b439-111">Si vous ne connaissez pas encore le nom du package de règles personnalisé, exécutez la cmdlet [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtype) pour le trouver :</span><span class="sxs-lookup"><span data-stu-id="4b439-111">If you don't already know it, run the [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtype) cmdlet to find the name of the custom rule package:</span></span>

   ```powershell
   Get-DlpSensitiveInformationTypeRulePackage
   ```

   > [!NOTE]
   > <span data-ttu-id="4b439-p101">Le package de règles intégré qui contient les types d’informations sensibles intégrés s’intitule Microsoft Rule Package. Le package de règles qui contient les types d’informations sensibles personnalisés que vous avez créés dans l’interface utilisateur du Centre de conformité est nommé Microsoft.SCCManaged.CustomRulePack.</span><span class="sxs-lookup"><span data-stu-id="4b439-p101">The built-in rule package that contains the built-in sensitive information types is named Microsoft Rule Package. The rule package that contains the custom sensitive information types that you created in the Compliance center UI is named Microsoft.SCCManaged.CustomRulePack.</span></span>

2. <span data-ttu-id="4b439-114">Utilisez la cmdlet [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtyperulepackage) pour stocker le package de règles personnalisé dans une variable :</span><span class="sxs-lookup"><span data-stu-id="4b439-114">Use the [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtyperulepackage) cmdlet to store the custom rule package to a variable:</span></span>

   ```powershell
   $rulepak = Get-DlpSensitiveInformationTypeRulePackage -Identity "RulePackageName"
   ```

   <span data-ttu-id="4b439-115">Par exemple, si le nom du package de règles est « Package de règles personnalisé d’ID d’employé », exécutez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="4b439-115">For example, if the name of the rule package is "Employee ID Custom Rule Pack", run the following cmdlet:</span></span>

   ```powershell
   $rulepak = Get-DlpSensitiveInformationTypeRulePackage -Identity "Employee ID Custom Rule Pack"
   ```

3. <span data-ttu-id="4b439-116">Utilisez la cmdlet [Set-Content](/powershell/module/microsoft.powershell.management/set-content) pour exporter le package de règles personnalisé dans un fichier XML :</span><span class="sxs-lookup"><span data-stu-id="4b439-116">Use the [Set-Content](/powershell/module/microsoft.powershell.management/set-content) cmdlet to export the custom rule package to an XML file:</span></span>

   ```powershell
   Set-Content -Path "XMLFileAndPath" -Encoding Byte -Value $rulepak.SerializedClassificationRuleCollection
   ```

   <span data-ttu-id="4b439-117">Cet exemple exporte le package de règles dans le fichier nommé ExportedRulePackage.xml dans le dossier Documents C:\My Documents folder.</span><span class="sxs-lookup"><span data-stu-id="4b439-117">This example export the rule package to the file named ExportedRulePackage.xml in the C:\My Documents folder.</span></span>

   ```powershell
   Set-Content -Path "C:\My Documents\ExportedRulePackage.xml" -Encoding Byte -Value $rulepak.SerializedClassificationRuleCollection
   ```

#### <a name="step-2-modify-the-sensitive-information-type-in-the-exported-xml-file"></a><span data-ttu-id="4b439-118">Étape 2: Modifier le type d’informations sensibles personnalisé dans un fichier exporté XML.</span><span class="sxs-lookup"><span data-stu-id="4b439-118">Step 2: Modify the sensitive information type in the exported XML file</span></span>

<span data-ttu-id="4b439-119">Les types d’informations sensibles dans le fichier XML et d’autres éléments dans le fichier sont décrits précédemment dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4b439-119">Sensitive information types in the XML file and other elements in the file are described earlier in this topic.</span></span>

#### <a name="step-3-import-the-updated-xml-file-back-into-the-existing-rule-package"></a><span data-ttu-id="4b439-120">Étape 3: Importer de nouveau le fichier XML mis à jour vers le package de règles existant.</span><span class="sxs-lookup"><span data-stu-id="4b439-120">Step 3: Import the updated XML file back into the existing rule package</span></span>

<span data-ttu-id="4b439-121">Pour réimporter le XML mis à jour dans le package de règles existant, utilisez la cmdlet [Set-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/set-dlpsensitiveinformationtyperulepackage) :</span><span class="sxs-lookup"><span data-stu-id="4b439-121">To import the updated XML back into the existing rule package, use the [Set-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/set-dlpsensitiveinformationtyperulepackage) cmdlet:</span></span>

```powershell
Set-DlpSensitiveInformationTypeRulePackage -FileData ([Byte[]]$(Get-Content -Path "C:\My Documents\External Sensitive Info Type Rule Collection.xml" -Encoding Byte -ReadCount 0))
```

<span data-ttu-id="4b439-122">Pour une syntaxe détaillée et des informations de paramétrage, voir [Set-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/set-dlpsensitiveinformationtyperulepackage).</span><span class="sxs-lookup"><span data-stu-id="4b439-122">For detailed syntax and parameter information, see [Set-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/set-dlpsensitiveinformationtyperulepackage).</span></span>


## <a name="more-information"></a><span data-ttu-id="4b439-123">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="4b439-123">More information</span></span>

- [<span data-ttu-id="4b439-124">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="4b439-124">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)

- [<span data-ttu-id="4b439-125">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="4b439-125">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)

- [<span data-ttu-id="4b439-126">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="4b439-126">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
