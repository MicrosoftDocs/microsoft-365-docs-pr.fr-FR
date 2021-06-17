---
title: Recherchez les menaces sur les appareils, les e-mails, les applications et les identités avec le chasse avancée
description: Étudiez les scénarios de chasse courants et les exemples de requêtes qui couvrent les appareils, les e-mails, les applications et les identités.
keywords: recherche avancée, données Office365, appareils Windows, normalisation des e-mails Office365, courriers électroniques, applications, identités, recherche de menace, recherche, requête, télémétrie, Microsoft 365, Microsoft 365 Defender
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: aacd0745ff507356035f8f460ed2b4307e9da6ed
ms.sourcegitcommit: 1c11035dd4432e34603022740baef0c8f7ff4425
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2021
ms.locfileid: "52964872"
---
# <a name="hunt-for-threats-across-devices-emails-apps-and-identities"></a><span data-ttu-id="a3033-104">Repérer des menaces sur les appareils, les e-mails, les applications, et les identités</span><span class="sxs-lookup"><span data-stu-id="a3033-104">Hunt for threats across devices, emails, apps, and identities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a3033-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a3033-105">**Applies to:**</span></span>
- <span data-ttu-id="a3033-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3033-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a3033-107">[Le recherche avancée](advanced-hunting-overview.md) dans Microsoft 365 Defender vous permet de chercher de manière proactive les menaces dans :</span><span class="sxs-lookup"><span data-stu-id="a3033-107">[Advanced hunting](advanced-hunting-overview.md) in Microsoft 365 Defender allows you to proactively hunt for threats across:</span></span>
- <span data-ttu-id="a3033-108">Appareils gérés par Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a3033-108">Devices managed by Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="a3033-109">Courriers électroniques traitées par Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a3033-109">Emails processed by Microsoft 365</span></span>
- <span data-ttu-id="a3033-110">Activités des applications cloud, événements d’authentification et activités de contrôleur de domaine suivis par Microsoft Cloud App Security et Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="a3033-110">Cloud app activities, authentication events, and domain controller activities tracked by Microsoft Cloud App Security and Microsoft Defender for Identity</span></span>

<span data-ttu-id="a3033-111">Avec ce niveau de visibilité, vous pouvez rapidement chercher les menaces qui traversent des sections de votre réseau, y compris les intrusions sophistiquées qui arrivent sur le courrier électronique ou le web, élever les privilèges locaux, acquérir des informations d’identification de domaine privilégiées et passer par la suite sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="a3033-111">With this level of visibility, you can quickly hunt for threats that traverse sections of your network, including sophisticated intrusions that arrive on email or the web, elevate local privileges, acquire privileged domain credentials, and move laterally to across your devices.</span></span> 

<span data-ttu-id="a3033-112">Voici des techniques générales et des exemples de requêtes basés sur différents scénarios de chasse qui peuvent vous aider à explorer la façon dont vous pouvez créer des requêtes lors du recherche de menaces aussi sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="a3033-112">Here are general techniques and sample queries based on various hunting scenarios that can help you explore how you might construct queries when hunting for such sophisticated threats.</span></span>

## <a name="get-entity-info"></a><span data-ttu-id="a3033-113">Obtenir des informations sur l’entité</span><span class="sxs-lookup"><span data-stu-id="a3033-113">Get entity info</span></span>
<span data-ttu-id="a3033-114">Utilisez ces requêtes pour savoir comment obtenir rapidement des informations sur les comptes d’utilisateur, les appareils et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a3033-114">Use these queries to learn how you can quickly get information about user accounts, devices, and files.</span></span> 

### <a name="obtain-user-accounts-from-email-addresses"></a><span data-ttu-id="a3033-115">Obtenir des comptes d’utilisateur des adresses de messagerie électronique :</span><span class="sxs-lookup"><span data-stu-id="a3033-115">Obtain user accounts from email addresses</span></span>
<span data-ttu-id="a3033-116">Lorsque vous construisez des requêtes sur des [tableaux qui traitent des appareils et des e-mail](advanced-hunting-schema-tables.md), vous devez peut-être obtenir des noms de compte d’utilisateur à partir des adresses e-mail d’expéditeur ou de destinataire.</span><span class="sxs-lookup"><span data-stu-id="a3033-116">When constructing queries across [tables that cover devices and emails](advanced-hunting-schema-tables.md), you will likely need to obtain user account names from sender or recipient email addresses.</span></span> <span data-ttu-id="a3033-117">Vous pouvez généralement le faire pour l’adresse du destinataire ou de l’expéditeur à l’aide de l’hôte local à partir de l’adresse *e-mail.*</span><span class="sxs-lookup"><span data-stu-id="a3033-117">You can generally do this for either recipient or sender address using the *local-host* from the email address.</span></span>

<span data-ttu-id="a3033-118">Dans l’extrait de code ci-dessous, nous utilisons la fonction [tostring()](/azure/data-explorer/kusto/query/tostringfunction) Kusto pour extraire l’hôte local juste avant les adresses de messagerie du destinataire dans `@` la `RecipientEmailAddress` colonne.</span><span class="sxs-lookup"><span data-stu-id="a3033-118">In the snippet below, we use the [tostring()](/azure/data-explorer/kusto/query/tostringfunction) Kusto function to extract the local-host right before the `@` from recipient email addresses in the column `RecipientEmailAddress`.</span></span>

```kusto
//Query snippet showing how to extract the account name from an email address
AccountName = tostring(split(RecipientEmailAddress, "@")[0])
```
<span data-ttu-id="a3033-119">La requête ci-dessous montre comment cet extrait de code peut être utilisé :</span><span class="sxs-lookup"><span data-stu-id="a3033-119">The query below shows how this snippet can be used:</span></span>

```kusto
EmailEvents
| where Timestamp > ago(7d)
| project RecipientEmailAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
```

### <a name="merge-the-identityinfo-table"></a><span data-ttu-id="a3033-120">Fusionner la table IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="a3033-120">Merge the IdentityInfo table</span></span>

<span data-ttu-id="a3033-121">Vous pouvez obtenir des noms de compte et d’autres informations de compte en fusionnant ou en rejoignant la [table IdentityInfo.](advanced-hunting-identityinfo-table.md)</span><span class="sxs-lookup"><span data-stu-id="a3033-121">You can get account names and other account information by merging or joining the [IdentityInfo table](advanced-hunting-identityinfo-table.md).</span></span> <span data-ttu-id="a3033-122">La requête ci-dessous obtient la liste des détections de hameçonnage et de programmes malveillants à partir de la [table EmailEvents,](advanced-hunting-emailevents-table.md) puis joint ces informations au tableau pour obtenir des informations détaillées sur chaque `IdentityInfo` destinataire.</span><span class="sxs-lookup"><span data-stu-id="a3033-122">The query below obtains the list of phishing and malware detections from the [EmailEvents table](advanced-hunting-emailevents-table.md) and then joins that information with the `IdentityInfo` table to get detailed information about each recipient.</span></span> 

```kusto
EmailEvents
| where Timestamp > ago(7d)
//Get email processing events where the messages were identified as either phishing or malware
| where ThreatTypes has "Malware" or ThreatTypes has "Phish"
//Merge email events with identity info to get recipient details
| join (IdentityInfo | distinct AccountUpn, AccountDisplayName, JobTitle, 
Department, City, Country) on $left.RecipientEmailAddress == $right.AccountUpn 
//Show important message and recipient details
| project Timestamp, NetworkMessageId, Subject, ThreatTypes, 
SenderFromAddress, RecipientEmailAddress, AccountDisplayName, JobTitle, 
Department, City, Country
```

### <a name="get-device-information"></a><span data-ttu-id="a3033-123">Obtenir des informations sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="a3033-123">Get device information</span></span>
<span data-ttu-id="a3033-124">Le [schéma de recherche avancé fournit des](advanced-hunting-schema-tables.md) informations complètes sur l’appareil dans différents tableaux.</span><span class="sxs-lookup"><span data-stu-id="a3033-124">The [advanced hunting schema](advanced-hunting-schema-tables.md) provides extensive device information in various tables.</span></span> <span data-ttu-id="a3033-125">Par exemple, le tableau [DeviceInfo fournit](advanced-hunting-deviceinfo-table.md) des informations complètes sur l’appareil en fonction des données d’événements agrégées régulièrement.</span><span class="sxs-lookup"><span data-stu-id="a3033-125">For example, the [DeviceInfo table](advanced-hunting-deviceinfo-table.md) provides comprehensive device information based on event data aggregated regularly.</span></span> <span data-ttu-id="a3033-126">Cette requête utilise la table pour vérifier si un utilisateur potentiellement compromis ( ) s’est connecté à des appareils, puis répertorie les alertes qui ont été déclenchées sur `DeviceInfo` `<account-name>` ces appareils.</span><span class="sxs-lookup"><span data-stu-id="a3033-126">This query uses the `DeviceInfo` table to check if a potentially compromised user (`<account-name>`) has logged on to any devices and then lists the alerts that have been triggered on those devices.</span></span>

>[!Tip]
> <span data-ttu-id="a3033-127">Cette requête permet de spécifier une jointure interne, ce qui empêche `kind=inner` la déduplication des valeurs côté [](/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor)gauche pour `DeviceId` .</span><span class="sxs-lookup"><span data-stu-id="a3033-127">This query uses `kind=inner` to specify an [inner-join](/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor), which prevents deduplication of left side values for `DeviceId`.</span></span>

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


### <a name="get-file-event-information"></a><span data-ttu-id="a3033-128">Obtenir des informations sur les événements de fichier</span><span class="sxs-lookup"><span data-stu-id="a3033-128">Get file event information</span></span>

<span data-ttu-id="a3033-129">Utilisez la requête suivante pour obtenir des informations sur les événements liés au fichier.</span><span class="sxs-lookup"><span data-stu-id="a3033-129">Use the following query to get information on file related events.</span></span> 

```kusto
DeviceInfo
| where Timestamp > ago(1d)
| where ClientVersion startswith "20.1"
| summarize by DeviceId
| join kind=inner (
    DeviceFileEvents 
    | where Timestamp > ago(1d)
) on DeviceId
| take 10
```


### <a name="get-network-event-information"></a><span data-ttu-id="a3033-130">Obtenir des informations sur les événements réseau</span><span class="sxs-lookup"><span data-stu-id="a3033-130">Get network event information</span></span>

<span data-ttu-id="a3033-131">Utilisez la requête suivante pour obtenir des informations sur les événements liés au réseau.</span><span class="sxs-lookup"><span data-stu-id="a3033-131">Use the following query to get information on network related events.</span></span>

```kusto
DeviceInfo
| where Timestamp > ago(1d)
| where ClientVersion startswith "20.1"
| summarize by DeviceId
| join kind=inner (
    DeviceNetworkEvents 
    | where Timestamp > ago(1d)
) on DeviceId
| take 10
```

### <a name="get-device-agent-version-information"></a><span data-ttu-id="a3033-132">Obtenir les informations de version de l’agent d’appareil</span><span class="sxs-lookup"><span data-stu-id="a3033-132">Get device agent version information</span></span>

<span data-ttu-id="a3033-133">Utilisez la requête suivante pour obtenir la version de l’agent en cours d’exécution sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="a3033-133">Use the following query to get the version of the agent running on a device.</span></span>

```kusto
DeviceInfo
| where Timestamp > ago(1d)
| where ClientVersion startswith "20.1"
| summarize by DeviceId
| join kind=inner (
    DeviceNetworkEvents 
    | where Timestamp > ago(1d)
) on DeviceId
| take 10
```


### <a name="example-query-for-macos-devices"></a><span data-ttu-id="a3033-134">Exemple de requête pour les appareils macOS</span><span class="sxs-lookup"><span data-stu-id="a3033-134">Example query for macOS devices</span></span>

<span data-ttu-id="a3033-135">Utilisez l’exemple de requête suivant pour voir tous les appareils exécutant macOS avec une version antérieure à Celle-ci.</span><span class="sxs-lookup"><span data-stu-id="a3033-135">Use the following example query to see all devices running macOS with a version older than Catalina.</span></span>

```kusto
DeviceInfo
| where Timestamp > ago(1d)
| where OSPlatform == "macOS" and  OSVersion !contains "10.15" and OSVersion !contains "11."
| summarize by DeviceId
| join kind=inner (
    DeviceInfo
    | where Timestamp > ago(1d)
) on DeviceId
| take 10
```

### <a name="get-device-status-info"></a><span data-ttu-id="a3033-136">Obtenir les informations d’état de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a3033-136">Get device status info</span></span>

<span data-ttu-id="a3033-137">Utilisez la requête suivante pour obtenir l’état d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="a3033-137">Use the following query to get status of a device.</span></span> <span data-ttu-id="a3033-138">Dans l’exemple suivant, la requête vérifie si l’appareil est intégré.</span><span class="sxs-lookup"><span data-stu-id="a3033-138">In the following example, the query checks to see if the device is onboarded.</span></span>

```kusto
DeviceInfo
| where Timestamp > ago(1d)
| where OnboardingStatus != "Onboarded"
| summarize by DeviceId
| join kind=inner (
    DeviceInfo
    | where Timestamp > ago(1d)
) on DeviceId
| take 10
```


## <a name="hunting-scenarios"></a><span data-ttu-id="a3033-139">Scénarios de repérage</span><span class="sxs-lookup"><span data-stu-id="a3033-139">Hunting scenarios</span></span>

### <a name="list-logon-activities-of-users-that-received-emails-that-were-not-zapped-successfully"></a><span data-ttu-id="a3033-140">List logon activities of users that received emails that were notpé successfully</span><span class="sxs-lookup"><span data-stu-id="a3033-140">List logon activities of users that received emails that were not zapped successfully</span></span>
<span data-ttu-id="a3033-141">[La purge automatique d’heure zéro (ZAP)](../office-365-security/zero-hour-auto-purge.md) adresse les e-mails malveillants après leur réception.</span><span class="sxs-lookup"><span data-stu-id="a3033-141">[Zero-hour auto purge (ZAP)](../office-365-security/zero-hour-auto-purge.md) addresses malicious emails after they have been received.</span></span> <span data-ttu-id="a3033-142">En cas d’échec de ZAP, du code malveillant peut éventuellement s’exécuter sur l’appareil et laisser les comptes compromis.</span><span class="sxs-lookup"><span data-stu-id="a3033-142">If ZAP fails, malicious code might eventually run on the device and leave accounts compromised.</span></span> <span data-ttu-id="a3033-143">Cette requête vérifie si l’activité de la logon est réalisée par les destinataires des e-mails qui n’ont pas été correctement adressés par ZAP.</span><span class="sxs-lookup"><span data-stu-id="a3033-143">This query checks for logon activity made by the recipients of emails that were not successfully addressed by ZAP.</span></span>

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

### <a name="get-logon-attempts-by-domain-accounts-targeted-by-credential-theft"></a><span data-ttu-id="a3033-144">Obtenir des tentatives de connexion par des comptes de domaine ciblés par le vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="a3033-144">Get logon attempts by domain accounts targeted by credential theft</span></span>
<span data-ttu-id="a3033-145">Cette requête identifie d’abord toutes les alertes d’accès aux informations d’identification dans la `AlertInfo` table.</span><span class="sxs-lookup"><span data-stu-id="a3033-145">This query first identifies all credential access alerts in the `AlertInfo` table.</span></span> <span data-ttu-id="a3033-146">Il fusionne ou joint ensuite la table, qu’il recherche uniquement pour les noms des comptes ciblés et les filtres pour les comptes `AlertEvidence` joints au domaine.</span><span class="sxs-lookup"><span data-stu-id="a3033-146">It then merges or joins the `AlertEvidence` table, which it parses for the names of the targeted accounts and filters for domain-joined accounts only.</span></span> <span data-ttu-id="a3033-147">Enfin, il vérifie la table pour obtenir toutes les activités d’accès par les comptes ciblés `IdentityLogonEvents` joints au domaine.</span><span class="sxs-lookup"><span data-stu-id="a3033-147">Finally, it checks the `IdentityLogonEvents` table to get all logon activities by the domain-joined targeted accounts.</span></span>

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

### <a name="check-if-files-from-a-known-malicious-sender-are-on-your-devices"></a><span data-ttu-id="a3033-148">Vérifier si les fichiers d’un expéditeur malveillant connu figurent sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="a3033-148">Check if files from a known malicious sender are on your devices</span></span>
<span data-ttu-id="a3033-149">En supposant que vous connaissez une adresse de messagerie envoyant des fichiers malveillants ( ), vous pouvez exécuter cette requête pour déterminer si des fichiers de cet expéditeur existent `MaliciousSender@example.com` sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="a3033-149">Assuming you know of an email address sending malicious files (`MaliciousSender@example.com`), you can run this query to determine if files from this sender exist on your devices.</span></span> <span data-ttu-id="a3033-150">Vous pouvez utiliser cette requête, par exemple, pour identifier les appareils affectés par une campagne de distribution de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="a3033-150">You can use this query, for example, to identify devices affected by a malware distribution campaign.</span></span>

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

### <a name="review-logon-attempts-after-receipt-of-malicious-emails"></a><span data-ttu-id="a3033-151">Examiner les tentatives de connexion après la réception des e-mails malveillants</span><span class="sxs-lookup"><span data-stu-id="a3033-151">Review logon attempts after receipt of malicious emails</span></span>
<span data-ttu-id="a3033-152">Cette requête recherche les 10 dernières connexions effectuées par les destinataires du courrier dans un délai de 30 minutes après la réception des e-mails malveillants connus.</span><span class="sxs-lookup"><span data-stu-id="a3033-152">This query finds the 10 latest logons performed by email recipients within 30 minutes after they received known malicious emails.</span></span> <span data-ttu-id="a3033-153">Vous pouvez utiliser cette requête pour vérifier si les comptes des destinataires de l’e-mail ont été compromis.</span><span class="sxs-lookup"><span data-stu-id="a3033-153">You can use this query to check whether the accounts of the email recipients have been compromised.</span></span>

```kusto
//Define new table for malicious emails
let MaliciousEmails=EmailEvents
//List emails detected as malware, getting only pertinent columns
| where ThreatTypes has "Malware" 
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

### <a name="review-powershell-activities-after-receipt-of-emails-from-known-malicious-sender"></a><span data-ttu-id="a3033-154">Examiner les activités PowerShell après réception d'e-mails d'expéditeurs malveillants connus.</span><span class="sxs-lookup"><span data-stu-id="a3033-154">Review PowerShell activities after receipt of emails from known malicious sender</span></span>
<span data-ttu-id="a3033-155">Les e-mails malveillants contiennent souvent des documents et d'autres pièces jointes spécialement conçues qui exécutent des commandes PowerShell pour offrir d'autres charges utiles.</span><span class="sxs-lookup"><span data-stu-id="a3033-155">Malicious emails often contain documents and other specially crafted attachments that run PowerShell commands to deliver additional payloads.</span></span> <span data-ttu-id="a3033-156">Si vous avez connaissance d’e-mails provenant d’un expéditeur malveillant connu ( ), vous pouvez utiliser cette requête pour ré lister et passer en revue les activités PowerShell qui se sont produites dans les 30 minutes après la réception d’un e-mail de `MaliciousSender@example.com` l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a3033-156">If you are aware of emails coming from a known malicious sender (`MaliciousSender@example.com`), you can use this query to list and review PowerShell activities that occurred within 30 minutes after an email was received from the sender.</span></span>  

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

## <a name="related-topics"></a><span data-ttu-id="a3033-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3033-157">Related topics</span></span>
- [<span data-ttu-id="a3033-158">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a3033-158">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a3033-159">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a3033-159">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="a3033-160">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="a3033-160">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="a3033-161">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="a3033-161">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="a3033-162">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="a3033-162">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="a3033-163">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="a3033-163">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
