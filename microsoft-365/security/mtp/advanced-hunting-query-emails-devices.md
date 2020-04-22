---
title: Trouvez des menaces sur divers appareils et messages électroniques à l’aide du repérage avancé
description: Étudiez les scénarios de repérage et les exemples de requêtes qui couvrent les appareils et les courriers électroniques.
keywords: repérage avancé, données Office 365, appareils Windows, normalisation des e-mails Office365, e-mails, repérage de menace, cybermenace, recherche, requête, télémétrie, Microsoft 365, Protection Microsoft contre les menaces
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: ec7f9083401fdf7a2114d99ddd2dcc009411e34b
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43633506"
---
# <a name="hunt-for-threats-across-devices-and-emails"></a><span data-ttu-id="640fb-104">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="640fb-104">Hunt for threats across devices and emails</span></span>

<span data-ttu-id="640fb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="640fb-105">**Applies to:**</span></span>
- <span data-ttu-id="640fb-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="640fb-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="640fb-107">La recherche [avancée](advanced-hunting-overview.md) dans la protection de Microsoft contre les menaces vous permet de rechercher de façon proactive les menaces entre vos appareils Windows et vos courriers électroniques Microsoft.</span><span class="sxs-lookup"><span data-stu-id="640fb-107">[Advanced hunting](advanced-hunting-overview.md) in Microsoft Threat Protection allows you to proactively hunt for threats across your Windows devices and Microsoft emails.</span></span> <span data-ttu-id="640fb-108">Voici quelques scénarios de repérage et exemples de requêtes qui peuvent vous aider à découvrir comment créer des requêtes sur les appareils et les e-mails.</span><span class="sxs-lookup"><span data-stu-id="640fb-108">Here are some hunting scenarios and sample queries that can help you explore how you might construct queries covering both devices and emails.</span></span>

## <a name="obtain-user-accounts-from-email-addresses"></a><span data-ttu-id="640fb-109">Obtenir des comptes d’utilisateur des adresses de messagerie électronique :</span><span class="sxs-lookup"><span data-stu-id="640fb-109">Obtain user accounts from email addresses</span></span>
<span data-ttu-id="640fb-110">Lorsque vous construisez des requêtes sur des [tableaux qui traitent des appareils et des e-mail](advanced-hunting-schema-tables.md), vous devez peut-être obtenir des noms de compte d’utilisateur à partir des adresses e-mail d’expéditeur ou de destinataire.</span><span class="sxs-lookup"><span data-stu-id="640fb-110">When constructing queries across [tables that cover devices and emails](advanced-hunting-schema-tables.md), you will likely need to obtain user account names from sender or recipient email addresses.</span></span> <span data-ttu-id="640fb-111">Pour ce faire, utilisez l'*hôte local* de l'adresse e-mail :</span><span class="sxs-lookup"><span data-stu-id="640fb-111">To do this use the *local-host* from the email address:</span></span>

```kusto
AccountName = tostring(split(SenderFromAddress, "@")[0])
```

<span data-ttu-id="640fb-112">Cette technique de normalisation est utilisée dans les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="640fb-112">This normalization technique is used in the succeeding scenarios.</span></span>

## <a name="hunting-scenarios"></a><span data-ttu-id="640fb-113">Scénarios de repérage</span><span class="sxs-lookup"><span data-stu-id="640fb-113">Hunting scenarios</span></span>

### <a name="check-if-files-from-a-known-malicious-sender-are-on-your-devices"></a><span data-ttu-id="640fb-114">Vérifier si les fichiers d’un expéditeur malveillant connu figurent sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="640fb-114">Check if files from a known malicious sender are on your devices</span></span>
<span data-ttu-id="640fb-115">En supposant que vous savez qu’une adresse e-mail envoie des fichiers malveillants, vous pouvez exécuter cette requête pour déterminer si des fichiers de cet expéditeur existent sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="640fb-115">Assuming you know of an email address sending malicious files, you can run this query to determine if files from this sender exist on your devices.</span></span> <span data-ttu-id="640fb-116">Vous pouvez utiliser cette requête (par exemple, pour déterminer le nombre d’appareils concernés par une campagne de distribution de programmes malveillants).</span><span class="sxs-lookup"><span data-stu-id="640fb-116">You can use this query, for example, to determine the number of devices affected by a malware distribution campaign.</span></span>

```kusto
//Get prevalence of files sent by a malicious sender in your organization
EmailAttachmentInfo
| where SenderFromAddress =~ "MaliciousSender@example.com"
| where isnotempty(SHA256)
| join (
DeviceFileEvents
| project FileName, SHA256
) on SHA256
```

### <a name="review-logon-attempts-after-receipt-of-malicious-emails"></a><span data-ttu-id="640fb-117">Examiner les tentatives de connexion après la réception des e-mails malveillants</span><span class="sxs-lookup"><span data-stu-id="640fb-117">Review logon attempts after receipt of malicious emails</span></span>
<span data-ttu-id="640fb-118">Cette requête recherche les 10 dernières connexions effectuées par les destinataires du courrier dans un délai de 30 minutes après la réception des e-mails malveillants connus.</span><span class="sxs-lookup"><span data-stu-id="640fb-118">This query finds the 10 latest logons performed by email recipients within 30 minutes after they received known malicious emails.</span></span> <span data-ttu-id="640fb-119">Vous pouvez utiliser cette requête pour vérifier si les comptes des destinataires de l’e-mail ont été compromis.</span><span class="sxs-lookup"><span data-stu-id="640fb-119">You can use this query to check whether the accounts of the email recipients have been compromised.</span></span>

```kusto
//Find logons that occurred right after malicious email was received
let MaliciousEmail=EmailEvents
| where MalwareFilterVerdict == "Malware" 
| project TimeEmail = Timestamp, Subject, SenderFromAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
MaliciousEmail
| join (
DeviceLogonEvents
| project LogonTime = Timestamp, AccountName, DeviceName
) on AccountName 
| where (LogonTime - TimeEmail) between (0min.. 30min)
| take 10
```

### <a name="review-powershell-activities-after-receipt-of-emails-from-known-malicious-sender"></a><span data-ttu-id="640fb-120">Examiner les activités PowerShell après réception d'e-mails d'expéditeurs malveillants connus.</span><span class="sxs-lookup"><span data-stu-id="640fb-120">Review PowerShell activities after receipt of emails from known malicious sender</span></span>
<span data-ttu-id="640fb-121">Les e-mails malveillants contiennent souvent des documents et d'autres pièces jointes spécialement conçues qui exécutent des commandes PowerShell pour offrir d'autres charges utiles.</span><span class="sxs-lookup"><span data-stu-id="640fb-121">Malicious emails often contain documents and other specially crafted attachments that run PowerShell commands to deliver additional payloads.</span></span> <span data-ttu-id="640fb-122">Si vous connaissez les e-mails provenant d’un expéditeur malveillant connu, vous pouvez utiliser cette requête pour répertorier et examiner les activités PowerShell qui se sont produites dans un délai de 30 minutes après la réception d’un e-mail envoyé par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="640fb-122">If you are aware of emails coming from a known malicious sender, you can use this query to list and review PowerShell activities that occurred within 30 minutes after an email was received from the sender .</span></span>  

```kusto
//Find PowerShell activities right after email was received from malicious sender
let x=EmailEvents
| where SenderFromAddress =~ "MaliciousSender@example.com"
| project TimeEmail = Timestamp, Subject, SenderFromAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
x
| join (
DeviceProcessEvents
| where FileName =~ "powershell.exe"
//| where InitiatingProcessParentFileName =~ "outlook.exe"
| project TimeProc = Timestamp, AccountName, DeviceName, InitiatingProcessParentFileName, InitiatingProcessFileName, FileName, ProcessCommandLine
) on AccountName 
| where (TimeProc - TimeEmail) between (0min.. 30min)
```

## <a name="related-topics"></a><span data-ttu-id="640fb-123">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="640fb-123">Related topics</span></span>
- [<span data-ttu-id="640fb-124">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="640fb-124">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="640fb-125">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="640fb-125">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="640fb-126">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="640fb-126">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="640fb-127">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="640fb-127">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="640fb-128">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="640fb-128">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="640fb-129">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="640fb-129">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
