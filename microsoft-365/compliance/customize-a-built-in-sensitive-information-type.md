---
title: Personnaliser un type d’informations sensibles intégré
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/08/2019
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Lorsque vous recherchez des informations sensibles dans du contenu, vous devez décrire ces informations dans ce que l’on appelle une règle. La protection contre la perte de données (DLP) comprend des règles pour les types d’informations sensibles les plus courants que vous pouvez utiliser immédiatement. Pour utiliser ces règles, vous devez les inclure dans une stratégie. Vous voudrez peut-être ajuster ces règles intégrées pour répondre aux besoins spécifiques de votre organisation, et vous pouvez le faire en créant un type d’informations sensibles personnalisé. Cette rubrique vous montre comment personnaliser le fichier XML qui contient la collection de règles existante pour détecter un plus large éventail d’informations potentielles relatives aux cartes de crédit.
ms.openlocfilehash: 2aa552fb7a2623aaa7783063e82101a1993b9d1c
ms.sourcegitcommit: f6840dfcfdbcadc53cda591fd6cf9ddcb749d303
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2020
ms.locfileid: "44327292"
---
# <a name="customize-a-built-in-sensitive-information-type"></a><span data-ttu-id="7b90b-107">Personnaliser un type d’informations sensibles intégré</span><span class="sxs-lookup"><span data-stu-id="7b90b-107">Customize a built-in sensitive information type</span></span>

<span data-ttu-id="7b90b-p102">Lorsque vous recherchez des informations sensibles dans du contenu, vous devez décrire ces informations dans ce que l’on appelle une *règle*. La protection contre la perte de données (DLP) comprend des règles pour les types d’informations sensibles les plus courants que vous pouvez utiliser immédiatement. Pour utiliser ces règles, vous devez les inclure dans une stratégie. Vous voudrez peut-être ajuster ces règles intégrées pour répondre aux besoins spécifiques de votre organisation, et vous pouvez le faire en créant un type d’informations sensibles personnalisé. Cette rubrique vous montre comment personnaliser le fichier XML qui contient la collection de règles existante pour détecter un plus large éventail d’informations potentielles relatives aux cartes de crédit.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p102">When looking for sensitive information in content, you need to describe that information in what's called a  *rule*  . Data loss prevention (DLP) includes rules for the most-common sensitive information types that you can use right away. To use these rules, you have to include them in a policy. You might find that you want to adjust these built-in rules to meet your organization's specific needs, and you can do that by creating a custom sensitive information type. This topic shows you how to customize the XML file that contains the existing rule collection to detect a wider range of potential credit-card information.</span></span> 
  
<span data-ttu-id="7b90b-p103">Vous pouvez prendre cet exemple et l’appliquer à d’autres types d’informations sensibles intégrés. Pour obtenir la liste des types d’informations sensibles par défaut et des définitions XML, voir [Définitions des entités de type information sensible](sensitive-information-type-entity-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="7b90b-p103">You can take this example and apply it to other built-in sensitive information types. For a list of default sensitive information types and XML definitions, see [Sensitive information type entity definitions](sensitive-information-type-entity-definitions.md).</span></span> 
  
## <a name="export-the-xml-file-of-the-current-rules"></a><span data-ttu-id="7b90b-115">Exporter le fichier XML des règles actuelles</span><span class="sxs-lookup"><span data-stu-id="7b90b-115">Export the XML file of the current rules</span></span>

<span data-ttu-id="7b90b-116">Pour exporter le fichier XML, vous devez vous [connecter au Centre de sécurité et conformité à l’aide de PowerShell à distance](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="7b90b-116">To export the XML, you need to [connect to the Security and Compliance Center via Remote PowerShell.](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="7b90b-p104">Dans PowerShell, saisissez la commande suivante pour afficher les règles de votre organisation à l’écran. Si vous n’avez pas créé votre propre règle, vous ne verrez que les règles intégrées par défaut, sous le libellé « Package de règles Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="7b90b-p104">In the PowerShell, type the following to display your organization's rules on screen. If you haven't created your own, you'll only see the default, built-in rules, labeled "Microsoft Rule Package."</span></span>

```powershell
Get-DlpSensitiveInformationTypeRulePackage
```    
2. <span data-ttu-id="7b90b-p105">Stockez les règles de votre organisation dans une variable en saisissant ce qui suit. Le stockage d’un élément dans une variable le rend facilement disponible ultérieurement dans un format adapté aux commandes PowerShell distantes.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p105">Store your organization's rules in a variable by typing the following. Storing something in a variable makes it easily available later in a format that works for remote PowerShell commands.</span></span>

```powershell    
$ruleCollections = Get-DlpSensitiveInformationTypeRulePackage
```
    
3. <span data-ttu-id="7b90b-p106">Saisissez ce qui suit pour créer un fichier XML mis en forme avec toutes ces données (`Set-content` est la partie de la cmdlet qui écrit le code XML dans le fichier).</span><span class="sxs-lookup"><span data-stu-id="7b90b-p106">Make a formatted XML file with all that data by typing the following. ( `Set-content` is the part of the cmdlet that writes the XML to the file.)</span></span> 
    
```powershell
Set-Content -path C:\custompath\exportedRules.xml -Encoding Byte -Value $ruleCollections.SerializedClassificationRuleCollection
```

> [!IMPORTANT]
> <span data-ttu-id="7b90b-p107">Assurez-vous que vous utilisez l’emplacement de fichier dans lequel votre pack de règles est effectivement stocké. `C:\custompath\` est un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p107">Make sure that you use the file location where your rule pack is actually stored.  `C:\custompath\` is a placeholder.</span></span> 
  
## <a name="find-the-rule-that-you-want-to-modify-in-the-xml"></a><span data-ttu-id="7b90b-125">Rechercher la règle à modifier dans le fichier XML</span><span class="sxs-lookup"><span data-stu-id="7b90b-125">Find the rule that you want to modify in the XML</span></span>

<span data-ttu-id="7b90b-p108">Les cmdlets ci-dessus ont exporté l’ensemble de la *collection de règles* qui inclut les règles par défaut que nous fournissons. Ensuite, vous devez rechercher la règle de numéro de carte de crédit spécifique à modifier.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p108">The cmdlets above exported the entire *rule collection*, which includes the default rules we provide. Next you'll need to look specifically for the Credit Card Number rule that you want to modify.</span></span> 
  
1. <span data-ttu-id="7b90b-128">Utilisez un éditeur de texte pour ouvrir le fichier XML que vous avez exporté dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="7b90b-128">Use a text editor to open the XML file that you exported in the previous section.</span></span>
    
2. <span data-ttu-id="7b90b-p109">Faites défiler l’écran jusqu’à la balise `<Rules>`, qui constitue le début de la section contenant les règles DLP. En effet, ce fichier XML contenant les informations de toute la collection de règles, il contient d’autres informations dans la partie supérieure que vous devez faire défiler pour accéder aux règles.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p109">Scroll down to the  `<Rules>` tag, which is the start of the section that contains the DLP rules. Because this XML file contains the information for the entire rule collection, it contains other information at the top that you need to scroll past to get to the rules.</span></span>
    
3. <span data-ttu-id="7b90b-p110">Recherchez *Func_credit_card* pour trouver la définition de règle de numéro de carte de crédit. En code XML, les noms des règles ne peuvent pas contenir d’espaces. Ces derniers sont donc généralement remplacés par des traits de soulignement, et les noms des règles sont parfois abrégés. Par exemple, la règle de numéro de sécurité sociale des États-Unis est abrégée en « SSN ». Le code XML de la règle de numéro de carte de crédit doit ressembler à l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p110">Look for *Func_credit_card* to find the Credit Card Number rule definition. In the XML, rule names can't contain spaces, so the spaces are usually replaced with underscores, and rule names are sometimes abbreviated. An example of this is the U.S. Social Security number rule, which is abbreviated "SSN." The Credit Card Number rule XML should look like the following code sample.</span></span>
    
  ```xml
  <Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085"
         patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
         <IdMatch idRef="Func_credit_card" />
          <Any minMatches="1">
            <Match idRef="Keyword_cc_verification" />
            <Match idRef="Keyword_cc_name" />
            <Match idRef="Func_expiration_date" />
          </Any>
        </Pattern>
      </Entity>
  ```

<span data-ttu-id="7b90b-p111">Maintenant que vous avez localisé la définition de règle de numéro de carte de crédit dans le XML, vous pouvez personnaliser le code XML de la règle en fonction de vos besoins. Pour un rappel des définitions XML, voir [Glossaire terminologique](#term-glossary) à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p111">Now that you have located the Credit Card Number rule definition in the XML, you can customize the rule's XML to meet your needs. For a refresher on the XML definitions, see the [Term glossary](#term-glossary) at the end of this topic.</span></span>
  
## <a name="modify-the-xml-and-create-a-new-sensitive-information-type"></a><span data-ttu-id="7b90b-137">Modifier le XML et créer un type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7b90b-137">Modify the XML and create a new sensitive information type</span></span>

<span data-ttu-id="7b90b-p112">Tout d’abord, vous devez créer un type d’informations sensibles, car vous ne pouvez pas modifier directement les règles par défaut. Vous pouvez effectuer de nombreuses actions avec les types d’informations sensibles personnalisés, comme l’illustre la section [Créer un type d’informations sensibles personnalisé dans l’interface PowerShell du Centre de sécurité et conformité](create-a-custom-sensitive-information-type-in-scc-powershell.md). Pour cet exemple, nous allons faire simple en nous contentant de supprimer les preuves corroborantes et d’ajouter des mots clés à la règle de numéro de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p112">First, you need to create a new sensitive information type because you can't directly modify the default rules. You can do a wide variety of things with custom sensitive information types, which are outlined in [Create a custom sensitive information type in Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). For this example, we'll keep it simple and only remove corroborative evidence and add keywords to the Credit Card Number rule.</span></span>
  
<span data-ttu-id="7b90b-p113">Toutes les définitions de règle XML sont construites sur le modèle général suivant. Vous devez copier et coller le XML de définition de numéro de carte de crédit dans le modèle, modifier certaines valeurs (remarquez les espaces réservés « . . ." dans l'exemple suivant), puis télécharger le XML modifié en tant que nouvelle règle pouvant être utilisée dans des stratégies.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p113">All XML rule definitions are built on the following general template. You need to copy and paste the Credit Card Number definition XML in the template, modify some values (notice the ". . ." placeholders in the following example), and then upload the modified XML as a new rule that can be used in policies.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="https://schemas.microsoft.com/office/2011/mce">
  <RulePack id=". . .">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id=". . ." /> 
    <Details defaultLangCode=". . .">
      <LocalizedDetails langcode=" . . . ">
         <PublisherName>. . .</PublisherName>
         <Name>. . .</Name>
         <Description>. . .</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
   <!-- Paste the Credit Card Number rule definition here.--> 
      <LocalizedStrings>
         <Resource idRef=". . .">
           <Name default="true" langcode=" . . . ">. . .</Name>
           <Description default="true" langcode=". . ."> . . .</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

<span data-ttu-id="7b90b-p114">Vous obtenez maintenant quelque chose qui ressemble au XML suivant. Étant donné que les packages de règles et les règles sont identifiés par leur GUID unique, vous devez générer deux GUID : un pour le package de règles et un pour remplacer le GUID de la règle de numéro de carte de crédit. Le GUID pour l’ID d’entité dans l’exemple de code suivant est celui de la définition de notre règle intégrée, que vous devez remplacer. Il existe plusieurs façons de générer des GUID, mais vous pouvez le faire facilement dans PowerShell en saisissant **[guid]::NewGuid()**.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p114">Now, you have something that looks similar to the following XML. Because rule packages and rules are identified by their unique GUIDs, you need to generate two GUIDs: one for the rule package and one to replace the GUID for the Credit Card Number rule. The GUID for the entity ID in the following code sample is the one for our built-in rule definition, which you need to replace with a new one. There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing **[guid]::NewGuid()**.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="https://schemas.microsoft.com/office/2011/mce">
  <RulePack id="8aac8390-e99f-4487-8d16-7f0cdee8defc">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id="8d34806e-cd65-4178-ba0e-5d7d712e5b66" />
    <Details defaultLangCode="en">
      <LocalizedDetails langcode="en">
        <PublisherName>Contoso Ltd.</PublisherName>
        <Name>Financial Information</Name>
        <Description>Modified versions of the Microsoft rule package</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f"
       patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
      <LocalizedStrings>
         <Resource idRef="db80b3da-0056-436e-b0ca-1f4cf7080d1f"> 
<!-- This is the GUID for the preceding Credit Card Number entity because the following text is for that Entity. -->
           <Name default="true" langcode="en-us">Modified Credit Card Number</Name>
           <Description default="true" langcode="en-us">Credit Card Number that looks for additional keywords, and another version of Credit Card Number that doesn't require keywords (but has a lower confidence level)</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

## <a name="remove-the-corroborative-evidence-requirement-from-a-sensitive-information-type"></a><span data-ttu-id="7b90b-150">Supprimer l’exigence de preuve crédible d’un type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7b90b-150">Remove the corroborative evidence requirement from a sensitive information type</span></span>

<span data-ttu-id="7b90b-151">À présent que vous disposez d’un nouveau type d’informations sensibles que vous pouvez charger vers le Centre de sécurité et de conformité, la prochaine étape consiste à rendre la règle plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="7b90b-151">Now that you have a new sensitive information type that you're able to upload to the Security &amp; Compliance Center, the next step is to make the rule more specific.</span></span> <span data-ttu-id="7b90b-152">Modifiez la règle de sorte qu’elle recherche uniquement un nombre à 16 chiffres qui passe la somme de contrôle, mais qu’elle ne nécessite pas de preuve (corroborante) supplémentaire comme des mots clés.</span><span class="sxs-lookup"><span data-stu-id="7b90b-152">Modify the rule so that it only looks for a 16-digit number that passes the checksum but doesn't require additional (corroborative) evidence, like keywords.</span></span> <span data-ttu-id="7b90b-153">Pour ce faire, vous devez retirer la partie du XML qui recherche la preuve corroborante.</span><span class="sxs-lookup"><span data-stu-id="7b90b-153">To do this, you need to remove the part of the XML that looks for corroborative evidence.</span></span> <span data-ttu-id="7b90b-154">Les preuves corroborantes sont très utiles pour réduire les faux positifs.</span><span class="sxs-lookup"><span data-stu-id="7b90b-154">Corroborative evidence is very helpful in reducing false positives.</span></span> <span data-ttu-id="7b90b-155">En l’occurrence, des mots clés ou une date d’expiration figurent généralement à proximité du numéro de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="7b90b-155">In this case there are usually certain keywords or an expiration date near the credit card number.</span></span> <span data-ttu-id="7b90b-156">Si vous supprimez cette preuve, vous devez également ajuster votre niveau de confiance par rapport au fait que vous avez trouvé un numéro de carte de crédit en abaissant la valeur du paramètre `confidenceLevel` qui est définie sur 85 dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7b90b-156">If you remove that evidence, you should also adjust how confident you are that you found a credit card number by lowering the  `confidenceLevel`, which is 85 in the example.</span></span>
  
```xml
<Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="300"
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
      </Pattern>
    </Entity>
```

## <a name="look-for-keywords-that-are-specific-to-your-organization"></a><span data-ttu-id="7b90b-157">Rechercher des mots clés propres à votre organisation</span><span class="sxs-lookup"><span data-stu-id="7b90b-157">Look for keywords that are specific to your organization</span></span>

<span data-ttu-id="7b90b-p116">Vous voulez peut-être exiger des preuves crédibles, mais aussi des mots clés différents ou supplémentaires, et vous voulez aussi peut-être modifier l’endroit où rechercher ces preuves. Vous pouvez ajuster le paramètre `patternsProximity` afin de développer ou réduire la fenêtre pour la preuve probante autour du numéro à 16 chiffres. Pour ajouter vos propres mots clés, vous devez définir une liste de mots clés et la référencer dans votre règle. Le XML suivant ajoute les mots clés « company card » et « Contoso card » de sorte que tous les messages qui contiennent ces expressions au sein des 150 caractères d’un numéro de carte de crédit soient identifiés comme des numéros de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p116">You might want to require corroborative evidence but want different or additional keywords, and perhaps you want to change where to look for that evidence. You can adjust the  `patternsProximity` to expand or shrink the window for corroborative evidence around the 16-digit number. To add your own keywords, you need to define a keyword list and reference it within your rule. The following XML adds the keywords "company card" and "Contoso card" so that any message that contains those phrases within 150 characters of a credit card number will be identified as a credit card number.</span></span>
  
```xml
<Rules>
<! -- Modify the patternsProximity to be "150" rather than "300." -->
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="150" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
<!-- Add the following XML, which references the keywords at the end of the XML sample. -->
          <Match idRef="My_Additional_Keywords" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
<!-- Add the following XML, and update the information inside the <Term> tags with the keywords that you want to detect. -->
    <Keyword id="My_Additional_Keywords">
      <Group matchStyle="word">
        <Term caseSensitive="false">company card</Term>
        <Term caseSensitive="false">Contoso card</Term>
      </Group>
    </Keyword>
```

## <a name="upload-your-rule"></a><span data-ttu-id="7b90b-162">Télécharger votre règle</span><span class="sxs-lookup"><span data-stu-id="7b90b-162">Upload your rule</span></span>

<span data-ttu-id="7b90b-163">Pour télécharger votre règle, vous devez procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="7b90b-163">To upload your rule, you need to do the following.</span></span>
  
1. <span data-ttu-id="7b90b-p117">Enregistrez-la en tant que fichier .xml avec le codage Unicode. Ceci est important car la règle ne fonctionne pas si le fichier est enregistré dans un codage différent.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p117">Save it as an .xml file with Unicode encoding. This is important because the rule won't work if the file is saved with a different encoding.</span></span>
    
2. [<span data-ttu-id="7b90b-166">Se connecter au Centre de sécurité et conformité à l’aide de PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="7b90b-166">Connect to the Security and Compliance Center via Remote PowerShell.</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
3. <span data-ttu-id="7b90b-167">Dans PowerShell, saisissez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7b90b-167">In the PowerShell, type the following.</span></span>

```powershell    
New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte).
```
> [!IMPORTANT]
> <span data-ttu-id="7b90b-p118">Assurez-vous que vous utilisez l’emplacement de fichier dans lequel votre pack de règles est effectivement stocké. `C:\custompath\` est un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p118">Make sure that you use the file location where your rule pack is actually stored.  `C:\custompath\` is a placeholder.</span></span> 
  
4. <span data-ttu-id="7b90b-170">Pour confirmer, saisissez Y, puis appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="7b90b-170">To confirm, type Y, and then press **Enter**.</span></span>
5. <span data-ttu-id="7b90b-171">Vérifiez que votre nouvelle règle a été chargée et son nom d’affichage en tapant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7b90b-171">Verify that your new rule was uploaded and it's display name by typing:</span></span>

```powershell
Get-DlpSensitiveInformationType
```

<span data-ttu-id="7b90b-p119">Pour commencer à utiliser la nouvelle règle afin de détecter des informations sensibles, vous devez l’ajouter à une stratégie DLP. Pour découvrir comment ajouter la règle à une stratégie, consultez l’article [Création d’une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md).</span><span class="sxs-lookup"><span data-stu-id="7b90b-p119">To start using the new rule to detect sensitive information, you need to add the rule to a DLP policy. To learn how to add the rule to a policy, see [Create a DLP policy from a template](create-a-dlp-policy-from-a-template.md).</span></span>
  
## <a name="term-glossary"></a><span data-ttu-id="7b90b-174">Glossaire terminologique</span><span class="sxs-lookup"><span data-stu-id="7b90b-174">Term glossary</span></span>

<span data-ttu-id="7b90b-175">Voici les définitions des termes que vous avez rencontrés au cours de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="7b90b-175">These are the definitions for the terms you encountered during this procedure.</span></span>
  
|<span data-ttu-id="7b90b-176">**Terme**</span><span class="sxs-lookup"><span data-stu-id="7b90b-176">**Term**</span></span>|<span data-ttu-id="7b90b-177">**Définition**</span><span class="sxs-lookup"><span data-stu-id="7b90b-177">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b90b-178">Entité</span><span class="sxs-lookup"><span data-stu-id="7b90b-178">Entity</span></span>|<span data-ttu-id="7b90b-p120">Les entités sont ce que nous appelons des types d'informations sensibles, comme les numéros de carte de crédit. Chaque entité possède un GUID unique qui constitue son ID. Si vous copiez un GUID et que vous le recherchez dans le XML, vous trouvez la définition de règle XML, ainsi que toutes les traductions localisées de cette règle XML. Vous pouvez également trouver cette définition en localisant le GUID de la traduction, puis en recherchant ce GUID.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p120">Entities are what we call sensitive information types, such as credit card numbers. Each entity has a unique GUID as its ID. If you copy a GUID and search for it in the XML, you'll find the XML rule definition and all the localized translations of that XML rule. You can also find this definition by locating the GUID for the translation and then searching for that GUID.</span></span>|
|<span data-ttu-id="7b90b-183">Fonctions</span><span class="sxs-lookup"><span data-stu-id="7b90b-183">Functions</span></span>|<span data-ttu-id="7b90b-p121">Le fichier XML fait référence à `Func_credit_card`, qui est une fonction dans le code compilé. Les fonctions sont utilisées pour exécuter des expressions régulières complexes et vérifier que les sommes de contrôle correspondent pour nos règles intégrées. Étant donné que tout ceci se passe dans le code, certaines variables ne figurent pas dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p121">The XML file references  `Func_credit_card`, which is a function in compiled code. Functions are used to run complex regexes and verify that checksums match for our built-in rules.) Because this happens in the code, some of the variables don't appear in the XML file.</span></span>|
|<span data-ttu-id="7b90b-186">IdMatch</span><span class="sxs-lookup"><span data-stu-id="7b90b-186">IdMatch</span></span>|<span data-ttu-id="7b90b-187">Il s’agit de l’identificateur auquel le modèle tente de correspondre, par exemple un numéro de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="7b90b-187">This is the identifier that the pattern is to trying to match—for example, a credit card number.</span></span>|
|<span data-ttu-id="7b90b-188">Listes de mots clés</span><span class="sxs-lookup"><span data-stu-id="7b90b-188">Keyword lists</span></span>|<span data-ttu-id="7b90b-p122">Le fichier XML fait également référence à `keyword_cc_verification` et à `keyword_cc_name`, qui sont des listes de mots clés dans lesquelles nous recherchons des correspondances à l’intérieur du paramètre `patternsProximity` pour l’entité. Ces éléments ne sont actuellement pas affichés dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p122">The XML file also references  `keyword_cc_verification` and  `keyword_cc_name`, which are lists of keywords from which we are looking for matches within the  `patternsProximity` for the entity. These aren't currently displayed in the XML.</span></span>|
|<span data-ttu-id="7b90b-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="7b90b-191">Pattern</span></span>|<span data-ttu-id="7b90b-192">Le modèle contient la liste de ce que le type sensible recherche.</span><span class="sxs-lookup"><span data-stu-id="7b90b-192">The pattern contains the list of what the sensitive type is looking for.</span></span> <span data-ttu-id="7b90b-193">Celle-ci inclut des mots clés, des expressions régulières et des fonctions internes qui effectuent des tâches telles que la vérification des sommes de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7b90b-193">This includes keywords, regexes, and internal functions, which perform tasks like verifying checksums.</span></span> <span data-ttu-id="7b90b-194">Ces types d’informations sensibles peuvent avoir plusieurs modèles avec des niveaux de confiance uniques.</span><span class="sxs-lookup"><span data-stu-id="7b90b-194">Sensitive information types can have multiple patterns with unique confidences.</span></span> <span data-ttu-id="7b90b-195">Ceci est utile lors de la création d’un type d’informations sensibles qui renvoie un niveau de confiance élevé si des preuves crédibles sont trouvées et un niveau de confiance faible dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7b90b-195">This is useful when creating a sensitive information type that returns a high confidence if corroborative evidence is found and a lower confidence if little or no corroborative evidence is found.</span></span>|
|<span data-ttu-id="7b90b-196">confidenceLevel</span><span class="sxs-lookup"><span data-stu-id="7b90b-196">Pattern confidenceLevel</span></span>|<span data-ttu-id="7b90b-p124">Il s’agit du niveau de confiance appliqué lorsque le moteur DLP trouve une correspondance. Ce niveau de confiance est associé à une correspondance pour le modèle si les exigences du modèle sont remplies. C’est la mesure de confiance à prendre en considération lorsque vous utilisez des règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="7b90b-p124">This is the level of confidence that the DLP engine found a match. This level of confidence is associated with a match for the pattern if the pattern's requirements are met. This is the confidence measure you should consider when using Exchange mail flow rules (also known as transport rules).</span></span>|
|<span data-ttu-id="7b90b-200">patternsProximity</span><span class="sxs-lookup"><span data-stu-id="7b90b-200">patternsProximity</span></span>|<span data-ttu-id="7b90b-201">Lorsque nous trouvons ce qui ressemble à un modèle de numéro de carte de crédit, `patternsProximity` correspond à la proximité de recherche de preuves crédibles autour de ce numéro.</span><span class="sxs-lookup"><span data-stu-id="7b90b-201">When we find what looks like a credit card number pattern,  `patternsProximity` is the proximity around that number where we'll look for corroborative evidence.</span></span>|
|<span data-ttu-id="7b90b-202">recommendedConfidence</span><span class="sxs-lookup"><span data-stu-id="7b90b-202">recommendedConfidence</span></span>|<span data-ttu-id="7b90b-p125">Il s’agit du niveau de confiance recommandé pour cette règle. La confiance recommandée s’applique aux entités et aux affinités. Pour les entités, ce nombre n’est jamais évalué par rapport au paramètre `confidenceLevel` pour le modèle. Il s’agit d’une simple suggestion pour vous aider à choisir un niveau de confiance, si vous voulez en appliquer un. Pour les affinités, le paramètre `confidenceLevel` du modèle doit être supérieur au nombre `recommendedConfidence` pour une action de règle de flux de messagerie à appeler. Le paramètre `recommendedConfidence` correspond au niveau de confiance par défaut utilisé dans les règles de flux de messagerie qui appelle une action. Si vous le souhaitez, vous pouvez modifier manuellement la règle de flux de messagerie à appeler pour le faire à partir du niveau de confiance du modèle.</span><span class="sxs-lookup"><span data-stu-id="7b90b-p125">This is the confidence level we recommend for this rule. The recommended confidence applies to entities and affinities. For entities, this number is never evaluated against the  `confidenceLevel` for the pattern. It's merely a suggestion to help you choose a confidence level if you want to apply one. For affinities, the  `confidenceLevel` of the pattern must be higher than the  `recommendedConfidence` number for a mail flow rule action to be invoked. The  `recommendedConfidence` is the default confidence level used in mail flow rules that invokes an action. If you want, you can manually change the mail flow rule to be invoked based off the pattern's confidence level, instead.</span></span>|
   
## <a name="for-more-information"></a><span data-ttu-id="7b90b-210">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="7b90b-210">For more information</span></span>

- [<span data-ttu-id="7b90b-211">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7b90b-211">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
    
- [<span data-ttu-id="7b90b-212">Créer un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="7b90b-212">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
    
- [<span data-ttu-id="7b90b-213">Vue d’ensemble des stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="7b90b-213">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
