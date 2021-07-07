---
title: Créer un dictionnaire de mots clés
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez les étapes principales de la création d’un dictionnaire de mots clés dans le Centre de sécurité et conformité Office 365.
ms.openlocfilehash: 8d313650f298f2ab26989bec9df1260918f7dd5c
ms.sourcegitcommit: 17d82e5617f0466eb825e15ab88594afcdaf4437
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2021
ms.locfileid: "53300104"
---
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="b65b0-103">Créer un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="b65b0-103">Create a keyword dictionary</span></span>

<span data-ttu-id="b65b0-104">La protection contre la perte de données (DLP) peut identifier, surveiller et protéger vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="b65b0-104">Data loss prevention (DLP) can identify, monitor, and protect your sensitive items.</span></span> <span data-ttu-id="b65b0-105">L’identification des éléments sensibles nécessite parfois la recherche de mots clés, en particulier lors de l’identification d’un contenu générique (comme une communication liée à la santé) ou d’un langage inapproprié ou explicite.</span><span class="sxs-lookup"><span data-stu-id="b65b0-105">Identifying sensitive items sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication), or inappropriate or explicit language.</span></span> <span data-ttu-id="b65b0-106">Bien que vous puissiez créer des listes de mots clés dans des types d’informations sensibles, ces listes sont de taille limitée et nécessitent la modification du XML pour les créer ou les modifier.</span><span class="sxs-lookup"><span data-stu-id="b65b0-106">Although you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them.</span></span> <span data-ttu-id="b65b0-107">Les dictionnaires de mots clés facilitent la gestion des mots clés à une échelle beaucoup plus grande, en prenant en charge jusqu’à 1 Mo de termes (après compression) dans le dictionnaire. De plus, toutes les langues sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b65b0-107">Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 1 MB of terms (post compression) in the dictionary and support any language.</span></span> <span data-ttu-id="b65b0-108">La limite du client est également de 1 Mo après compression.</span><span class="sxs-lookup"><span data-stu-id="b65b0-108">The tenant limit is also 1 MB after compression.</span></span> <span data-ttu-id="b65b0-109">1 Mo de limite après compression signifie que tous les dictionnaires combinés dans un client peuvent avoir près de 1 million de caractères.</span><span class="sxs-lookup"><span data-stu-id="b65b0-109">1 MB of post compression limit means that all dictionaries combined across a tenant can have close to 1 million characters.</span></span>

## <a name="keyword-dictionary-limits"></a><span data-ttu-id="b65b0-110">Limites du dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="b65b0-110">Keyword dictionary limits</span></span>

<span data-ttu-id="b65b0-111">Il existe une limite de 50 types d’informations sensibles basés sur un dictionnaire de mots clés que vous pouvez créer par client.</span><span class="sxs-lookup"><span data-stu-id="b65b0-111">There is a limit of 50 keyword dictionary based sensitive information types that can be created per tenant.</span></span> <span data-ttu-id="b65b0-112">Pour connaître le nombre de dictionnaires de mots clés de votre client, connectez-vous à l’aide des procédures de la section [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](/powershell/exchange/connect-to-scc-powershell) pour vous connecter à votre client et exécutez ce script PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b65b0-112">To find out how many keyword dictionaries you have in your tenant, connect using the procedures in [Connect to the Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) to connect to your tenant and run this PowerShell script.</span></span>

```powershell
$rawFile = $env:TEMP + "\rule.xml"

$kd = Get-DlpKeywordDictionary
$ruleCollections = Get-DlpSensitiveInformationTypeRulePackage
Set-Content -path $rawFile -Encoding Byte -Value $ruleCollections.SerializedClassificationRuleCollection
$UnicodeEncoding = New-Object System.Text.UnicodeEncoding
$FileContent = [System.IO.File]::ReadAllText((Resolve-Path $rawFile), $unicodeEncoding)

if($kd.Count -gt 0)
{
$count = 0
$entities = $FileContent -split "Entity id"
for($j=1;$j -lt $entities.Count;$j++)
{
for($i=0;$i -lt $kd.Count;$i++)
{
$Matches = Select-String -InputObject $entities[$j] -Pattern $kd[$i].Identity -AllMatches
$count = $Matches.Matches.Count + $count
if($Matches.Matches.Count -gt 0) {break}
}
}

Write-Output "Total Keyword Dictionary SIT:"
$count
}
else
{
$Matches = Select-String -InputObject $FileContent -Pattern $kd.Identity -AllMatches
Write-Output "Total Keyword Dictionary SIT:"
$Matches.Matches.Count
}

Remove-Item $rawFile
```

## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="b65b0-113">Étapes de base de la création d’un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="b65b0-113">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="b65b0-p103">Les mots clés de votre dictionnaire peuvent provenir de diverses sources, le plus souvent d’un fichier (par exemple, une liste .csv ou .txt) importé dans le service ou par cmdlet PowerShell, depuis une liste à laquelle vous accédez directement dans la cmdlet PowerShell ou depuis un dictionnaire existant. Lorsque vous créez un dictionnaire de mots clés, vous suivez les mêmes étapes fondamentales :</span><span class="sxs-lookup"><span data-stu-id="b65b0-p103">The keywords for your dictionary could come from various sources, most commonly from a file (such as a .csv or .txt list) imported in the service or by PowerShell cmdlet, from a list you enter directly in the PowerShell cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="b65b0-116">Utilisez le **Centre de sécurité et de conformité** ([https://protection.office.com](https://protection.office.com)) ou connectez-vous au **Centre de sécurité &amp; de conformité PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-116">Use the **Security & Compliance Center** ([https://protection.office.com](https://protection.office.com)) or connect to  **Security &amp; Compliance Center PowerShell**.</span></span>
    
2. <span data-ttu-id="b65b0-117">**Définissez ou chargez vos mots clés à partir de la source souhaitée**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-117">**Define or load your keywords from your intended source**.</span></span> <span data-ttu-id="b65b0-118">L’Assistant et le cmdlet acceptent une liste de mots clés séparés par des virgules pour la création d’un dictionnaire de mots clés personnalisé. Cette étape varie légèrement en fonction de l’origine de vos mots clés.</span><span class="sxs-lookup"><span data-stu-id="b65b0-118">The wizard and the cmdlet both accept a comma-separated list of keywords to create a custom keyword dictionary, so this step will vary slightly depending on where your keywords come from.</span></span> <span data-ttu-id="b65b0-119">Une fois chargés, les mots clés sont encodés et convertis en un tableau d’octets avant d’être importés.</span><span class="sxs-lookup"><span data-stu-id="b65b0-119">Once loaded, they're encoded and converted to a byte array before they're imported.</span></span>
    
3. <span data-ttu-id="b65b0-120">**Créez le dictionnaire**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-120">**Create your dictionary**.</span></span> <span data-ttu-id="b65b0-121">Choisissez un nom et une description, puis créez votre dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b65b0-121">Choose a name and description and create your dictionary.</span></span>

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a><span data-ttu-id="b65b0-122">Créer un dictionnaire de mots clés avec le Centre de sécurité et de conformité</span><span class="sxs-lookup"><span data-stu-id="b65b0-122">Create a keyword dictionary using the Security & Compliance Center</span></span>

<span data-ttu-id="b65b0-123">Procédez comme suit pour créer et importer des mots clés pour un dictionnaire personnalisé :</span><span class="sxs-lookup"><span data-stu-id="b65b0-123">Use the following steps to create and import keywords for a custom dictionary:</span></span>

1. <span data-ttu-id="b65b0-124">Connectez-vous au Centre de sécurité et de conformité([https://protection.office.com](https://protection.office.com)).</span><span class="sxs-lookup"><span data-stu-id="b65b0-124">Connect to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span>

2. <span data-ttu-id="b65b0-125">Accédez à **Classifications > Types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-125">Navigate to **Classifications > Sensitive info types**.</span></span>

3. <span data-ttu-id="b65b0-126">Sélectionnez **Créer** et entrez un **Nom** et une **Description** pour votre type d’informations sensibles, puis sélectionnez **Suivant**</span><span class="sxs-lookup"><span data-stu-id="b65b0-126">Select **Create** and enter a **Name** and **Description** for your sensitive info type, then select **Next**</span></span>

4. <span data-ttu-id="b65b0-127">Sélectionnez **Ajouter un élément**, puis sélectionnez **Dictionnaire (grands mots clés)** dans la liste déroulante **Détecter le contenu contenant**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-127">Select **Add an element**, then select **Dictionary (Large keywords)** in the **Detect content containing** drop-down list.</span></span>

5. <span data-ttu-id="b65b0-128">Sélectionnez **Ajouter un dictionnaire**</span><span class="sxs-lookup"><span data-stu-id="b65b0-128">Select **Add a dictionary**</span></span>

6. <span data-ttu-id="b65b0-129">Sous le Contrôle de recherche, sélectionnez **Vous pouvez créer de nouveaux dictionnaires de mots clés ici**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-129">Under the Search control, select **You can create new keyword dictionaries here**.</span></span>

7. <span data-ttu-id="b65b0-130">Entrez un **Nom** pour votre dictionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b65b0-130">Enter a **Name** for your custom dictionary.</span></span>

8. <span data-ttu-id="b65b0-131">Sélectionnez **Importer**, puis sélectionnez **À partir d’un fichier texte** ou **À partir d’un fichier CSV** selon votre type de fichier de mots clés.</span><span class="sxs-lookup"><span data-stu-id="b65b0-131">Select **Import**, and select either **From text** or **From csv** depending on your keyword file type.</span></span>

9. <span data-ttu-id="b65b0-132">Dans la boîte de dialogue du fichier, sélectionnez le fichier de mots clés sur votre PC local ou sur votre partage de fichiers réseau, puis sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-132">In the file dialog, select the keyword file from your local PC or network file share, then select **Open**.</span></span>

10. <span data-ttu-id="b65b0-133">Sélectionnez **Enregistrer**, puis sélectionnez votre dictionnaire personnalisé dans la liste **Dictionnaires de mots clés**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-133">Select **Save**, then select your custom dictionary from the **Keyword dictionaries** list.</span></span>

11. <span data-ttu-id="b65b0-134">Sélectionnez **Ajouter**, puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-134">Select **Add**, then select **Next**.</span></span>

12. <span data-ttu-id="b65b0-135">Passez en revue et finalisez vos sélections de type d’informations sensibles, puis sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-135">Review and finalize your sensitive info type selections, then select **Finish**.</span></span>
    
## <a name="create-a-keyword-dictionary-from-a-file-using-powershell"></a><span data-ttu-id="b65b0-136">Création d’un dictionnaire de mots clés à partir d’un fichier avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="b65b0-136">Create a keyword dictionary from a file using PowerShell</span></span>

<span data-ttu-id="b65b0-137">Lorsque vous devez créer un dictionnaire volumineux, c’est souvent pour utiliser les mots clés d’un fichier ou d’une liste exportée à partir d’une autre source.</span><span class="sxs-lookup"><span data-stu-id="b65b0-137">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source.</span></span> <span data-ttu-id="b65b0-138">Dans cet exemple, vous allez créer un dictionnaire de mots clés, contenant une liste de langages inappropriés à filtrer dans un courrier électronique externe.</span><span class="sxs-lookup"><span data-stu-id="b65b0-138">In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email.</span></span> <span data-ttu-id="b65b0-139">Vous devez d’abord [vous connecter à l’interface PowerShell du Centre de sécurité&amp; et de conformité](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="b65b0-139">You must first [Connect to Security &amp; Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="b65b0-140">Copiez les mots clés dans un fichier texte et assurez-vous que chaque mot clé est sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="b65b0-140">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="b65b0-p107">Enregistrez le fichier texte avec le codage Unicode. Dans le Bloc-notes \> **Enregistrer sous** \> **Codage** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="b65b0-p107">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="b65b0-143">Lisez le fichier dans une variable en exécutant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="b65b0-143">Read the file into a variable by running this cmdlet:</span></span>
    
    ```powershell
    $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
    ```

4. <span data-ttu-id="b65b0-144">Créez le dictionnaire en exécutant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="b65b0-144">Create the dictionary by running this cmdlet:</span></span>
    
    ```powershell
    New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
    ```
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="b65b0-145">Utilisation des dictionnaires de mots clés dans les types d’informations sensibles personnalisés et les stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="b65b0-145">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="b65b0-146">Les dictionnaires de mots clés peuvent être utilisés dans le cadre des exigences de correspondance pour un type d’information sensible personnalisé ou comme type d’information sensible eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="b65b0-146">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves.</span></span> <span data-ttu-id="b65b0-147">Dans les deux cas, la création d’un [type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type-in-scc-powershell.md) est requise.</span><span class="sxs-lookup"><span data-stu-id="b65b0-147">Both require you to create a [custom sensitive information type](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span> <span data-ttu-id="b65b0-148">Suivez les instructions de l’article lié pour créer un type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="b65b0-148">Follow the instructions in the linked article to create a sensitive information type.</span></span> <span data-ttu-id="b65b0-149">Une fois que vous avez le XML, vous aurez besoin de l’identificateur GUID que le dictionnaire utilise.</span><span class="sxs-lookup"><span data-stu-id="b65b0-149">Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```xml
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="b65b0-150">Pour obtenir l’identité de votre dictionnaire, exécutez la commande suivante et copiez la valeur de la propriété **Identité** :</span><span class="sxs-lookup"><span data-stu-id="b65b0-150">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```powershell
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="b65b0-151">Le résultat de la commande ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="b65b0-151">The output of the command looks like this:</span></span>
  
<span data-ttu-id="b65b0-152">`RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255`
`Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f`
`Name              : Diseases`
`Description       : Names of diseases and injuries from ICD-10-CM lexicon`
`KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo` `proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,`</span><span class="sxs-lookup"><span data-stu-id="b65b0-152">`RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255`
`Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f`
`Name              : Diseases`
`Description       : Names of diseases and injuries from ICD-10-CM lexicon`
`KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo` `proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,`</span></span>
                    `abrami's disease, abramo`
`IsValid           : True`
`ObjectState       : Unchanged`


<span data-ttu-id="b65b0-p109">Collez l’identité dans le code XML de votre type personnalisé d’informations sensibles et chargez-le. Votre dictionnaire s’affiche désormais dans votre liste de types d’informations sensibles et vous pouvez l’utiliser directement dans votre stratégie en indiquant le nombre de mots clés qui doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="b65b0-p109">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
```xml
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```

> [!NOTE]
> <span data-ttu-id="b65b0-155">Microsoft 365 Information Protection prend désormais en charge, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="b65b0-155">Microsoft 365 Information Protection supports double byte character set languages for:</span></span>
> - <span data-ttu-id="b65b0-156">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="b65b0-156">Chinese (simplified)</span></span>
> - <span data-ttu-id="b65b0-157">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="b65b0-157">Chinese (traditional)</span></span>
> - <span data-ttu-id="b65b0-158">Korean</span><span class="sxs-lookup"><span data-stu-id="b65b0-158">Korean</span></span>
> - <span data-ttu-id="b65b0-159">Japanese</span><span class="sxs-lookup"><span data-stu-id="b65b0-159">Japanese</span></span>
>
><span data-ttu-id="b65b0-160">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="b65b0-160">This support is available for sensitive information types.</span></span> <span data-ttu-id="b65b0-161">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-161">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

> [!TIP]
> <span data-ttu-id="b65b0-162">Pour détecter les modèles contenant des caractères chinois/japonais et des caractères d’octet unique ou pour détecter les modèles contenant du chinois/le japonais et l’anglais, définissez deux variantes du mot clé ou de regex.</span><span class="sxs-lookup"><span data-stu-id="b65b0-162">To detect patterns containing Chinese/Japanese characters and single byte characters or to detect patterns containing Chinese/Japanese and English, define two variants of the keyword or regex.</span></span> 
>
> <span data-ttu-id="b65b0-163">Par exemple, pour détecter un mot clé tel que « 机密的document », utilisez deux variantes du mot clé ; l’un avec un espace entre le texte japonais et anglais et l’autre sans espace entre le texte japonais et l’anglais.</span><span class="sxs-lookup"><span data-stu-id="b65b0-163">For example, to detect a keyword like "机密的document", use two variants of the keyword; one with a space between the Japanese and English text and another without a space between the Japanese and English text.</span></span> <span data-ttu-id="b65b0-164">Par conséquent, les mots clés à ajouter dans le SIT doivent être « 机密的 document » et « 机密的document ».</span><span class="sxs-lookup"><span data-stu-id="b65b0-164">So, the keywords to be added in the SIT should be "机密的 document" and "机密的document".</span></span> <span data-ttu-id="b65b0-165">De la même façon, pour détecter une expression « 東京オリンピック2020 », deux variantes doivent être utilisées : « 東京オリンピック 2020 » et « 東京オリンピック2020 ».</span><span class="sxs-lookup"><span data-stu-id="b65b0-165">Similarly, to detect a phrase "東京オリンピック2020", two variants should be used; "東京オリンピック 2020" and "東京オリンピック2020".</span></span>
>
> <span data-ttu-id="b65b0-p112">Lorsque vous créez une regex en utilisant un trait d'union à double octet ou un point à double octet, assurez-vous d'échapper les deux caractères comme on le ferait pour un trait d'union ou un point dans une regex. Voici un exemple regex pour référence :</span><span class="sxs-lookup"><span data-stu-id="b65b0-p112">While creating a regex using a double byte hyphen or a double byte period, make sure to escape both the characters like one would escape a hyphen or period in a regex. Here is a sample regex for reference:</span></span>
>
>    - <span data-ttu-id="b65b0-168">(?<!\d)([４][０-９]{3}[\-?\－\t]\*[０-９]{4}</span><span class="sxs-lookup"><span data-stu-id="b65b0-168">(?<!\d)([４][０-９]{3}[\-?\－\t]\*[０-９]{4}</span></span>
>
> <span data-ttu-id="b65b0-169">Nous vous recommandons d’utiliser une correspondance de chaîne au lieu d’une correspondance de mot dans une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="b65b0-169">We recommend using a string match instead of a word match in a keyword list.</span></span>
