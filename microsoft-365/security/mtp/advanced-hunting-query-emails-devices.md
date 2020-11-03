---
title: Recherche de menaces sur les appareils, les e-mails, les applications et les identités à l’aide de la chasse avancée
description: Étude des scénarios de chasse courants et des exemples de requêtes couvrant les appareils, les e-mails, les applications et les identités.
keywords: chasse avancée, données Office 365, appareils Windows, normalisation des courriers électroniques Office 365, e-mails, applications, identités, recherche de menace, recherche de menace, recherche, requête, télémétrie, Microsoft 365, protection contre les menaces Microsoft
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
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 97640c318908b87c211caed780624080508a255f
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847343"
---
# <a name="hunt-for-threats-across-devices-emails-apps-and-identities"></a><span data-ttu-id="59338-104">Recherche de menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="59338-104">Hunt for threats across devices, emails, apps, and identities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="59338-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="59338-105">**Applies to:**</span></span>
- <span data-ttu-id="59338-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="59338-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="59338-107">La [chasse avancée](advanced-hunting-overview.md) dans Microsoft 365 Defender vous permet de rechercher de façon proactive les menaces parmi les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="59338-107">[Advanced hunting](advanced-hunting-overview.md) in Microsoft 365 Defender allows you to proactively hunt for threats across:</span></span>
- <span data-ttu-id="59338-108">Appareils gérés par Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="59338-108">Devices managed by Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="59338-109">Messages électroniques traités par Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="59338-109">Emails processed by Microsoft 365</span></span>
- <span data-ttu-id="59338-110">Activités d’application Cloud, événements d’authentification et activités de contrôleur de domaine suivis par Microsoft Cloud App Security et Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="59338-110">Cloud app activities, authentication events, and domain controller activities tracked by Microsoft Cloud App Security and Microsoft Defender for Identity</span></span>

<span data-ttu-id="59338-111">Ce niveau de visibilité vous permet de rechercher rapidement les menaces qui traversent les sections de votre réseau, notamment les intrusions sophistiquées qui arrivent sur le courrier électronique ou le Web, d’élever les privilèges locaux, d’acquérir des informations d’identification de domaine privilégié et de se déplacer par la suite vers l’ensemble de vos appareils.</span><span class="sxs-lookup"><span data-stu-id="59338-111">With this level of visibility, you can quickly hunt for threats that traverse sections of your network, including sophisticated intrusions that arrive on email or the web, elevate local privileges, acquire privileged domain credentials, and move laterally to across your devices.</span></span> 

<span data-ttu-id="59338-112">Voici des techniques générales et des exemples de requêtes basés sur différents scénarios de chasse qui peuvent vous aider à découvrir comment créer des requêtes lors de la recherche de ces menaces sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="59338-112">Here are general techniques and sample queries based on various hunting scenarios that can help you explore how you might construct queries when hunting for such sophisticated threats.</span></span>

## <a name="get-entity-info"></a><span data-ttu-id="59338-113">Obtenir des informations sur l’entité</span><span class="sxs-lookup"><span data-stu-id="59338-113">Get entity info</span></span>
<span data-ttu-id="59338-114">Utilisez ces requêtes pour savoir comment obtenir rapidement des informations sur les comptes d’utilisateur, les appareils et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="59338-114">Use these queries to learn how you can quickly get information about user accounts, devices, and files.</span></span> 

### <a name="obtain-user-accounts-from-email-addresses"></a><span data-ttu-id="59338-115">Obtenir des comptes d’utilisateur des adresses de messagerie électronique :</span><span class="sxs-lookup"><span data-stu-id="59338-115">Obtain user accounts from email addresses</span></span>
<span data-ttu-id="59338-116">Lorsque vous construisez des requêtes sur des [tableaux qui traitent des appareils et des e-mail](advanced-hunting-schema-tables.md), vous devez peut-être obtenir des noms de compte d’utilisateur à partir des adresses e-mail d’expéditeur ou de destinataire.</span><span class="sxs-lookup"><span data-stu-id="59338-116">When constructing queries across [tables that cover devices and emails](advanced-hunting-schema-tables.md), you will likely need to obtain user account names from sender or recipient email addresses.</span></span> <span data-ttu-id="59338-117">Vous pouvez généralement effectuer cette opération pour le destinataire ou l’adresse de l’expéditeur à l’aide de l' *hôte local* à partir de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="59338-117">You can generally do this for either recipient or sender address using the *local-host* from the email address.</span></span>

<span data-ttu-id="59338-118">Dans l’extrait de code ci-dessous, nous utilisons la fonction [ToString ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/tostringfunction) Kusto pour extraire le droit de l’hôte local avant les `@` adresses de messagerie des destinataires dans la colonne `RecipientEmailAddress` .</span><span class="sxs-lookup"><span data-stu-id="59338-118">In the snippet below, we use the [tostring()](https://docs.microsoft.com/azure/data-explorer/kusto/query/tostringfunction) Kusto function to extract the local-host right before the `@` from recipient email addresses in the column `RecipientEmailAddress`.</span></span>

```kusto
//Query snippet showing how to extract the account name from an email address
AccountName = tostring(split(RecipientEmailAddress, "@")[0])
```
<span data-ttu-id="59338-119">La requête ci-dessous illustre l’utilisation de cet extrait de code :</span><span class="sxs-lookup"><span data-stu-id="59338-119">The query below shows how this snippet can be used:</span></span>

```kusto
EmailEvents
| where Timestamp > ago(7d)
| project RecipientEmailAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
```

### <a name="merge-the-identityinfo-table"></a><span data-ttu-id="59338-120">Fusionner la table IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="59338-120">Merge the IdentityInfo table</span></span>

<span data-ttu-id="59338-121">Vous pouvez obtenir des noms de compte et d’autres informations de compte en fusionnant ou en joignant la [table IdentityInfo](advanced-hunting-identityinfo-table.md).</span><span class="sxs-lookup"><span data-stu-id="59338-121">You can get account names and other account information by merging or joining the [IdentityInfo table](advanced-hunting-identityinfo-table.md).</span></span> <span data-ttu-id="59338-122">La requête ci-dessous obtient la liste des détections de hameçonnage et de programmes malveillants dans la [table EmailEvents](advanced-hunting-emailevents-table.md) , puis joint ces informations à la `IdentityInfo` table pour obtenir des informations détaillées sur chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="59338-122">The query below obtains the list of phishing and malware detections from the [EmailEvents table](advanced-hunting-emailevents-table.md) and then joins that information with the `IdentityInfo` table to get detailed information about each recipient.</span></span> 

```kusto
EmailEvents
| where Timestamp > ago(7d)
//Get email processing events where the messages were identified as either phishing or malware
| where MalwareFilterVerdict == 'Malware' or PhishFilterVerdict == 'Phish'
//Merge email events with identity info to get recipient details
| join (IdentityInfo | distinct AccountUpn, AccountDisplayName, JobTitle, 
Department, City, Country) on $left.RecipientEmailAddress == $right.AccountUpn 
//Show important message and recipient details
| project Timestamp, NetworkMessageId, Subject, PhishFilterVerdict, MalwareFilterVerdict,
SenderFromAddress, RecipientEmailAddress, AccountDisplayName, JobTitle, 
Department, City, Country
```

### <a name="get-device-information"></a><span data-ttu-id="59338-123">Obtenir des informations sur les appareils</span><span class="sxs-lookup"><span data-stu-id="59338-123">Get device information</span></span>
<span data-ttu-id="59338-124">Le [schéma de chasse avancé](advanced-hunting-schema-tables.md) fournit des informations détaillées sur l’appareil dans différentes tables.</span><span class="sxs-lookup"><span data-stu-id="59338-124">The [advanced hunting schema](advanced-hunting-schema-tables.md) provides extensive device information in various tables.</span></span> <span data-ttu-id="59338-125">Par exemple, le [tableau DeviceInfo](advanced-hunting-deviceinfo-table.md) fournit des informations complètes sur l’appareil en fonction des données d’événements regroupées régulièrement.</span><span class="sxs-lookup"><span data-stu-id="59338-125">For example, the [DeviceInfo table](advanced-hunting-deviceinfo-table.md) provides comprehensive device information based on event data aggregated regularly.</span></span> <span data-ttu-id="59338-126">Cette requête utilise la `DeviceInfo` table pour vérifier si un utilisateur potentiellement compromis () s' `<account-name>` est connecté à un appareil, puis répertorie les alertes déclenchées sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="59338-126">This query uses the `DeviceInfo` table to check if a potentially compromised user (`<account-name>`) has logged on to any devices and then lists the alerts that have been triggered on those devices.</span></span>

>[!Tip]
> <span data-ttu-id="59338-127">Cette requête utilise `kind=inner` pour spécifier une [jointure interne](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor), ce qui empêche la déduplication des valeurs côté gauche de `DeviceId` .</span><span class="sxs-lookup"><span data-stu-id="59338-127">This query uses `kind=inner` to specify an [inner-join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor), which prevents deduplication of left side values for `DeviceId`.</span></span>

```kusto
DeviceInfo
//Query for devices that the potentially compromised account has logged onto
| where LoggedOnUsers contains '<account-name>'
| distinct DeviceId
//Crosscheck devices against alert records in AlertEvidence and AlertInfo tables
| join kind=inner AlertEvidence on DeviceId
| project AlertId
//List all alerts on devices that user has logged on to
| join AlertInfo on AlertId
| project AlertId, Timestamp, Title, Severity, Category 
```

## <a name="hunting-scenarios"></a><span data-ttu-id="59338-128">Scénarios de repérage</span><span class="sxs-lookup"><span data-stu-id="59338-128">Hunting scenarios</span></span>

### <a name="list-logon-activities-of-users-that-received-emails-that-were-not-zapped-successfully"></a><span data-ttu-id="59338-129">Répertorier les activités de connexion des utilisateurs qui ont reçu des courriers électroniques qui n’ont pas été zapped</span><span class="sxs-lookup"><span data-stu-id="59338-129">List logon activities of users that received emails that were not zapped successfully</span></span>
<span data-ttu-id="59338-130">La [purge automatique à zéro heure (ZAP)](../office-365-security/zero-hour-auto-purge.md) traite les messages électroniques malveillants une fois qu’ils ont été reçus.</span><span class="sxs-lookup"><span data-stu-id="59338-130">[Zero-hour auto purge (ZAP)](../office-365-security/zero-hour-auto-purge.md) addresses malicious emails after they have been received.</span></span> <span data-ttu-id="59338-131">Si l’opération ZAP échoue, le code malveillant peut finir par s’exécuter sur l’appareil et laisser des comptes compromis.</span><span class="sxs-lookup"><span data-stu-id="59338-131">If ZAP fails, malicious code might eventually run on the device and leave accounts compromised.</span></span> <span data-ttu-id="59338-132">Cette requête vérifie l’activité d’ouverture de session effectuée par les destinataires des messages électroniques qui n’ont pas été correctement traités par ZAP.</span><span class="sxs-lookup"><span data-stu-id="59338-132">This query checks for logon activity made by the recipients of emails that were not successfully addressed by ZAP.</span></span>

```kusto
EmailPostDeliveryEvents 
| where Timestamp > ago(7d)
//List malicious emails that were not zapped successfully
| where ActionType has "ZAP" and ActionResult == "Error"
| project ZapTime = Timestamp, ActionType, NetworkMessageId , RecipientEmailAddress 
//Get logon activity of recipients using RecipientEmailAddress and AccountUpn
| join kind=inner IdentityLogonEvents on $left.RecipientEmailAddress == $right.AccountUpn
| where Timestamp between ((ZapTime-24h) .. (ZapTime+24h))
//Show only pertinent info, such as account name, the app or service, protocol, the target device, and type of logon
| project ZapTime, ActionType, NetworkMessageId , RecipientEmailAddress, AccountUpn, 
LogonTime = Timestamp, AccountDisplayName, Application, Protocol, DeviceName, LogonType
```

### <a name="get-logon-attempts-by-domain-accounts-targeted-by-credential-theft"></a><span data-ttu-id="59338-133">Obtenir des tentatives de connexion par des comptes de domaine ciblés par le vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="59338-133">Get logon attempts by domain accounts targeted by credential theft</span></span>
<span data-ttu-id="59338-134">Cette requête identifie d’abord toutes les alertes d’accès aux informations d’identification dans le `AlertInfo` tableau.</span><span class="sxs-lookup"><span data-stu-id="59338-134">This query first identifies all credential access alerts in the `AlertInfo` table.</span></span> <span data-ttu-id="59338-135">Il fusionne ou rejoint la `AlertEvidence` table, qu’elle analyse pour les noms des comptes et filtres ciblés pour les comptes joints au domaine uniquement.</span><span class="sxs-lookup"><span data-stu-id="59338-135">It then merges or joins the `AlertEvidence` table, which it parses for the names of the targeted accounts and filters for domain-joined accounts only.</span></span> <span data-ttu-id="59338-136">Enfin, il vérifie le `IdentityLogonEvents` tableau pour obtenir toutes les activités d’ouverture de session par les comptes ciblés joints au domaine.</span><span class="sxs-lookup"><span data-stu-id="59338-136">Finally, it checks the `IdentityLogonEvents` table to get all logon activities by the domain-joined targeted accounts.</span></span>

```kusto
AlertInfo
| where Timestamp > ago(30d)
//Get all credential access alerts
| where Category == "CredentialAccess"
//Get more info from AlertEvidence table to get the SID of the target accounts
| join AlertEvidence on AlertId
| extend IsJoined=(parse_json(AdditionalFields).Account.IsDomainJoined)
| extend TargetAccountSid=tostring(parse_json(AdditionalFields).Account.Sid)
//Filter for domain-joined accounts only
| where IsJoined has "true"
//Merge with IdentityLogonEvents to get all logon attempts by the potentially compromised target accounts
| join kind=inner IdentityLogonEvents on $left.TargetAccountSid == $right.AccountSid
//Show only pertinent info, such as account name, the app or service, protocol, the accessed device, and type of logon
| project AccountDisplayName, TargetAccountSid, Application, Protocol, DeviceName, LogonType
```

### <a name="check-if-files-from-a-known-malicious-sender-are-on-your-devices"></a><span data-ttu-id="59338-137">Vérifier si les fichiers d’un expéditeur malveillant connu figurent sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="59338-137">Check if files from a known malicious sender are on your devices</span></span>
<span data-ttu-id="59338-138">En supposant que vous connaissiez une adresse de messagerie qui envoie des fichiers malveillants ( `MaliciousSender@example.com` ), vous pouvez exécuter cette requête pour déterminer si les fichiers de cet expéditeur existent sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="59338-138">Assuming you know of an email address sending malicious files (`MaliciousSender@example.com`), you can run this query to determine if files from this sender exist on your devices.</span></span> <span data-ttu-id="59338-139">Vous pouvez utiliser cette requête, par exemple, pour identifier les appareils affectés par une campagne de distribution de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="59338-139">You can use this query, for example, to identify devices affected by a malware distribution campaign.</span></span>

```kusto
EmailAttachmentInfo
| where SenderFromAddress =~ "MaliciousSender@example.com"
//Get emails with attachments identified by a SHA-256
| where isnotempty(SHA256)
| join (
//Check devices for any activity involving the attachments
DeviceFileEvents
| project FileName, SHA256
) on SHA256
| project Timestamp, FileName , SHA256, DeviceName, DeviceId,  NetworkMessageId, SenderFromAddress, RecipientEmailAddress
```

### <a name="review-logon-attempts-after-receipt-of-malicious-emails"></a><span data-ttu-id="59338-140">Examiner les tentatives de connexion après la réception des e-mails malveillants</span><span class="sxs-lookup"><span data-stu-id="59338-140">Review logon attempts after receipt of malicious emails</span></span>
<span data-ttu-id="59338-141">Cette requête recherche les 10 dernières connexions effectuées par les destinataires du courrier dans un délai de 30 minutes après la réception des e-mails malveillants connus.</span><span class="sxs-lookup"><span data-stu-id="59338-141">This query finds the 10 latest logons performed by email recipients within 30 minutes after they received known malicious emails.</span></span> <span data-ttu-id="59338-142">Vous pouvez utiliser cette requête pour vérifier si les comptes des destinataires de l’e-mail ont été compromis.</span><span class="sxs-lookup"><span data-stu-id="59338-142">You can use this query to check whether the accounts of the email recipients have been compromised.</span></span>

```kusto
//Define new table for malicious emails
let MaliciousEmails=EmailEvents
//List emails detected as malware, getting only pertinent columns
| where MalwareFilterVerdict == "Malware"
| project TimeEmail = Timestamp, Subject, SenderFromAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
MaliciousEmails
| join (
//Merge malicious emails with logon events to find logons by recipients
IdentityLogonEvents
| project LogonTime = Timestamp, AccountName, DeviceName
) on AccountName 
//Check only logons within 30 minutes of receipt of an email
| where (LogonTime - TimeEmail) between (0min.. 30min)
| take 10
```

### <a name="review-powershell-activities-after-receipt-of-emails-from-known-malicious-sender"></a><span data-ttu-id="59338-143">Examiner les activités PowerShell après réception d'e-mails d'expéditeurs malveillants connus.</span><span class="sxs-lookup"><span data-stu-id="59338-143">Review PowerShell activities after receipt of emails from known malicious sender</span></span>
<span data-ttu-id="59338-144">Les e-mails malveillants contiennent souvent des documents et d'autres pièces jointes spécialement conçues qui exécutent des commandes PowerShell pour offrir d'autres charges utiles.</span><span class="sxs-lookup"><span data-stu-id="59338-144">Malicious emails often contain documents and other specially crafted attachments that run PowerShell commands to deliver additional payloads.</span></span> <span data-ttu-id="59338-145">Si vous êtes conscient des e-mails provenant d’un expéditeur malveillant connu ( `MaliciousSender@example.com` ), vous pouvez utiliser cette requête pour répertorier et passer en revue les activités PowerShell qui se sont produites dans les 30 minutes suivant la réception d’un message électronique de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="59338-145">If you are aware of emails coming from a known malicious sender (`MaliciousSender@example.com`), you can use this query to list and review PowerShell activities that occurred within 30 minutes after an email was received from the sender.</span></span>  

```kusto
//Define new table for emails from specific sender
let EmailsFromBadSender=EmailEvents
| where SenderFromAddress =~ "MaliciousSender@example.com"
| project TimeEmail = Timestamp, Subject, SenderFromAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
//Merge emails from sender with process-related events on devices
EmailsFromBadSender
| join (
DeviceProcessEvents
//Look for PowerShell activity
| where FileName =~ "powershell.exe"
//Add line below to check only events initiated by Outlook
//| where InitiatingProcessParentFileName =~ "outlook.exe"
| project TimeProc = Timestamp, AccountName, DeviceName, InitiatingProcessParentFileName, InitiatingProcessFileName, FileName, ProcessCommandLine
) on AccountName 
//Check only PowerShell activities within 30 minutes of receipt of an email
| where (TimeProc - TimeEmail) between (0min.. 30min)
```

## <a name="related-topics"></a><span data-ttu-id="59338-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59338-146">Related topics</span></span>
- [<span data-ttu-id="59338-147">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="59338-147">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="59338-148">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="59338-148">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="59338-149">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="59338-149">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="59338-150">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="59338-150">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="59338-151">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="59338-151">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="59338-152">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="59338-152">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
