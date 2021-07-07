---
title: Supprimer un type d’informations sensibles personnalisé à l’aide de PowerShell
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
description: Découvrez comment supprimer un type d’informations sensibles personnalisé à l’aide de PowerShell
ms.openlocfilehash: 9365eeff6100b16c94b9fa09b06dc51b272b60a6
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322692"
---
# <a name="remove-a-custom-sensitive-information-type-using-powershell"></a><span data-ttu-id="4a043-103">Supprimer un type d’informations sensibles personnalisé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a043-103">Remove a custom sensitive information type using PowerShell</span></span>



<span data-ttu-id="4a043-104">Dans PowerShell du centre de conformité, il existe deux méthodes pour supprimer des types d’informations sensibles personnalisés :</span><span class="sxs-lookup"><span data-stu-id="4a043-104">In Compliance center PowerShell, there are two methods to remove custom sensitive information types:</span></span>

- <span data-ttu-id="4a043-105">**Supprimer des types d’informations sensibles** personnalisés individuels : utilisez la méthode documentée dans Modifier un type d’informations sensibles personnalisé [à l’aide de PowerShell](sit-modify-a-custom-sensitive-information-type-in-powershell.md#modify-a-custom-sensitive-information-type-using-powershell).</span><span class="sxs-lookup"><span data-stu-id="4a043-105">**Remove individual custom sensitive information types**: Use the method documented in [Modify a custom sensitive information type using PowerShell](sit-modify-a-custom-sensitive-information-type-in-powershell.md#modify-a-custom-sensitive-information-type-using-powershell).</span></span> <span data-ttu-id="4a043-106">Vous exportez le package de règles personnalisé qui contient le type d’informations sensibles personnalisé, supprimez le type d’informations sensibles du fichier XML et importez de nouveau le fichier XML mis à jour dans le package de règles personnalisé existant.</span><span class="sxs-lookup"><span data-stu-id="4a043-106">You export the custom rule package that contains the custom sensitive information type, remove the sensitive information type from the XML file, and import the updated XML file back into the existing custom rule package.</span></span>

- <span data-ttu-id="4a043-107">**Supprimer un package de règles personnalisé et tous les types d’informations sensibles personnalisés qu’il contient**: cette méthode est présentée dans cette section.</span><span class="sxs-lookup"><span data-stu-id="4a043-107">**Remove a custom rule package and all custom sensitive information types that it contains**: This method is documented in this section.</span></span>

> [!NOTE]
> <span data-ttu-id="4a043-108">Avant de supprimer un type d’informations sensibles personnalisé, vérifiez qu’aucune stratégie DLP ou règle de flux de courrier Exchange (également appelées règles de transport) ne référence toujours le type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="4a043-108">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. [<span data-ttu-id="4a043-109">Se connecter à PowerShell du centre de conformité</span><span class="sxs-lookup"><span data-stu-id="4a043-109">Connect to Compliance center PowerShell</span></span>](/powershell/exchange/exchange-online-powershell)

2. <span data-ttu-id="4a043-110">Pour supprimer un règle de package personnalisé, utilisez la cmdlet [Remove-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/remove-dlpsensitiveinformationtyperulepackage) :</span><span class="sxs-lookup"><span data-stu-id="4a043-110">To remove a custom rule package, use the [Remove-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/remove-dlpsensitiveinformationtyperulepackage) cmdlet:</span></span>

   ```powershell
   Remove-DlpSensitiveInformationTypeRulePackage -Identity "RulePackageIdentity"
   ```

   <span data-ttu-id="4a043-111">Vous pouvez utiliser la valeur Nom (pour n’importe quelle langue) ou la`RulePack id` valeur (GUID) pour identifier le package de règles.</span><span class="sxs-lookup"><span data-stu-id="4a043-111">You can use the Name value (for any language) or the `RulePack id` (GUID) value to identify the rule package.</span></span>

   <span data-ttu-id="4a043-112">Cet exemple supprime le package de règles nommé « Package règle personnalisé employé ID ».</span><span class="sxs-lookup"><span data-stu-id="4a043-112">This example removes the rule package named "Employee ID Custom Rule Pack".</span></span>

   ```powershell
   Remove-DlpSensitiveInformationTypeRulePackage -Identity "Employee ID Custom Rule Pack"
   ```

   <span data-ttu-id="4a043-113">Pour une syntaxe détaillée et des informations de paramétrage, voir [Remove-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/remove-dlpsensitiveinformationtyperulepackage).</span><span class="sxs-lookup"><span data-stu-id="4a043-113">For detailed syntax and parameter information, see [Remove-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/remove-dlpsensitiveinformationtyperulepackage).</span></span>

3. <span data-ttu-id="4a043-114">Afin de vérifier que vous avez correctement retiré un nouveau type d’informations sensibles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a043-114">To verify that you've successfully removed a custom sensitive information type, do any of the following steps:</span></span>

   - <span data-ttu-id="4a043-115">Exécutez la cmdlet [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtyperulepackage) et vérifiez que le package de règles n’est plus répertorié :</span><span class="sxs-lookup"><span data-stu-id="4a043-115">Run the [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtyperulepackage) cmdlet and verify the rule package is no longer listed:</span></span>

     ```powershell
     Get-DlpSensitiveInformationTypeRulePackage
     ```

   - <span data-ttu-id="4a043-116">Exécutez la cmdlet [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) pour vérifier que les types d’informations sensibles dans le package de règles supprimé ne sont plus répertoriés :</span><span class="sxs-lookup"><span data-stu-id="4a043-116">Run the [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) cmdlet to verify the sensitive information types in the removed rule package are no longer listed:</span></span>

     ```powershell
     Get-DlpSensitiveInformationType
     ```

     <span data-ttu-id="4a043-117">Pour les types d’informations sensibles personnalisés, la valeur de propriété Publisher sera un numéro autre que Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="4a043-117">For custom sensitive information types, the Publisher property value will be something other than Microsoft Corporation.</span></span>

   - <span data-ttu-id="4a043-118">Remplacez \<Name\> avec la valeur Name du type d’informations sensibles (par exemple, ID d’employé), puis exécutez la cmdlet [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) pour vérifier que le type d’informations sensibles n’est plus répertorié :</span><span class="sxs-lookup"><span data-stu-id="4a043-118">Replace \<Name\> with the Name value of the sensitive information type (for example, Employee ID) and run the [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) cmdlet to verify the sensitive information type is no longer listed:</span></span>

     ```powershell
     Get-DlpSensitiveInformationType -Identity "<Name>"
     ```

## <a name="more-information"></a><span data-ttu-id="4a043-119">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="4a043-119">More information</span></span>

- [<span data-ttu-id="4a043-120">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="4a043-120">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)

- [<span data-ttu-id="4a043-121">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="4a043-121">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)

- [<span data-ttu-id="4a043-122">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="4a043-122">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
