---
title: FAQ sur les messages mis en quarantaine
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: troubleshooting
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs peuvent afficher les questions fréquemment posées et les réponses sur les messages mis en quarantaine dans Exchange Online Protection (EOP).
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: abd2304e83d2814cab55d13312535bd94308d8be
ms.sourcegitcommit: b3bb5bf5efa197ef8b16a33401b0b4f5663d3aa0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50032600"
---
# <a name="quarantined-messages-faq"></a><span data-ttu-id="dbd75-103">FAQ sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="dbd75-103">Quarantined messages FAQ</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="dbd75-104">Cette rubrique fournit des questions fréquemment posées et des réponses sur les messages électroniques mis en quarantaine pour les organisations Microsoft 365 ayant des boîtes aux lettres dans Exchange Online ou les organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="dbd75-104">This topic provides frequently asked questions and answers about quarantined email messages for Microsoft 365 organizations with mailboxes in Exchange Online, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span>

<span data-ttu-id="dbd75-105">Pour obtenir des questions et des réponses sur la protection anti-courrier indésirable, consultez la faq sur la [protection anti-courrier indésirable.](anti-spam-protection-faq.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-105">For questions and answers about anti-spam protection, see [Anti-spam protection FAQ](anti-spam-protection-faq.md).</span></span>

<span data-ttu-id="dbd75-106">Pour obtenir des questions et des réponses sur la protection anti-programme malveillant, consultez la [faq sur la protection anti-programme malveillant.](anti-malware-protection-faq-eop.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-106">For questions and answers about anti-malware protection, see [Anti-malware protection FAQ](anti-malware-protection-faq-eop.md).</span></span>

<span data-ttu-id="dbd75-107">Pour obtenir des questions et des réponses sur la protection contre l’usurpation d’informations, consultez la faq sur la protection contre l’usurpation [d’informations.](anti-spoofing-protection-faq.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-107">For questions and answers about anti-spoofing protection, see [Anti-spoofing protection FAQ](anti-spoofing-protection-faq.md).</span></span>

## <a name="how-do-i-manage-messages-that-were-quarantined-for-malware"></a><span data-ttu-id="dbd75-108">Comment gérer les messages mis en quarantaine pour les programmes malveillants ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-108">How do I manage messages that were quarantined for malware?</span></span>

<span data-ttu-id="dbd75-109">Seuls les administrateurs peuvent gérer les messages mis en quarantaine pour les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="dbd75-109">Only admins can manage messages that were quarantined for malware.</span></span> <span data-ttu-id="dbd75-110">Pour plus d’informations, voir Gérer les messages et fichiers mis en [quarantaine en tant qu’administrateur.](manage-quarantined-messages-and-files.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-110">For more information, see [Manage quarantined messages and files as an admin](manage-quarantined-messages-and-files.md).</span></span>

## <a name="how-do-i-quarantine-spam"></a><span data-ttu-id="dbd75-111">Comment mettre en quarantaine le courrier indésirable ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-111">How do I quarantine spam?</span></span>

<span data-ttu-id="dbd75-112">Par défaut, les messages classés comme courrier indésirable ou courrier en masse par filtrage du courrier indésirable sont remis à la boîte aux lettres de l’utilisateur et déplacés vers le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="dbd75-112">By default, messages that are classified as spam or bulk email by spam filtering are delivered to the user's mailbox, and are moved to the Junk Email folder.</span></span> <span data-ttu-id="dbd75-113">Toutefois, vous pouvez créer et configurer des stratégies anti-courrier indésirable pour mettre en quarantaine le courrier indésirable ou les messages électroniques en masse à la place.</span><span class="sxs-lookup"><span data-stu-id="dbd75-113">But you can create and configure anti-spam policies to quarantine spam or bulk email messages instead.</span></span> <span data-ttu-id="dbd75-114">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="dbd75-114">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

## <a name="how-do-i-give-users-access-to-the-quarantine"></a><span data-ttu-id="dbd75-115">Comment accorder aux utilisateurs l’accès à la mise en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-115">How do I give users access to the quarantine?</span></span>

<span data-ttu-id="dbd75-116">Un utilisateur doit avoir un compte valide pour accéder à ses propres messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="dbd75-116">A user must have a valid account to access their own messages in quarantine.</span></span> <span data-ttu-id="dbd75-117">EOP autonome exige que les utilisateurs soient représentés en tant qu’utilisateurs de messagerie dans EOP (créés ou créés manuellement via la synchronisation d’annuaires).</span><span class="sxs-lookup"><span data-stu-id="dbd75-117">Standalone EOP requires that users are represented as mail users in EOP (manually created or created via directory synchronization).</span></span> <span data-ttu-id="dbd75-118">Pour plus d’informations sur la gestion des utilisateurs dans des environnements EOP autonomes, voir Gérer les utilisateurs [de messagerie dans EOP.](manage-mail-users-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-118">For more information about managing users in standalone EOP environments, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>

## <a name="what-messages-can-end-users-access-in-quarantine"></a><span data-ttu-id="dbd75-119">Quels messages les utilisateurs finaux peuvent-ils accéder en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-119">What messages can end users access in quarantine?</span></span>

<span data-ttu-id="dbd75-120">Les utilisateurs peuvent accéder aux courriers indésirables, aux courriers électroniques en masse et (depuis avril 2020) aux messages de hameçonnage dont ils sont destinataires.</span><span class="sxs-lookup"><span data-stu-id="dbd75-120">Users can access spam, bulk email, and (as of April 2020) phishing messages where they are a recipient.</span></span> <span data-ttu-id="dbd75-121">Les utilisateurs finaux ne peuvent pas accéder aux programmes malveillants mis en quarantaine, au hameçonnage à haut niveau de confiance ou aux messages mis en quarantaine en raison de l’action Remettre le **message** à l’action de mise en quarantaine hébergée dans les règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="dbd75-121">End users can't access quarantined malware, high confidence phishing or messages that were quarantined because of the **Deliver the message to the hosted quarantine** action in mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="dbd75-122">Pour plus d’informations sur l’accès des utilisateurs aux messages mis en quarantaine, voir Rechercher et libérer les messages mis en quarantaine [en tant qu’utilisateur.](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-122">For more information about users accessing quarantined messages, see [Find and release quarantined messages as a user](find-and-release-quarantined-messages-as-a-user.md).</span></span>

## <a name="how-long-are-messages-kept-in-the-quarantine"></a><span data-ttu-id="dbd75-123">Pendant combien de temps les messages sont-ils mis en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-123">How long are messages kept in the quarantine?</span></span>

<span data-ttu-id="dbd75-124">Vous configurez la durée pendant combien de temps le courrier indésirable, le hameçonnage et les messages électroniques en nombre sont mis en quarantaine à l’aide de stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="dbd75-124">You configure how long spam, phishing, and bulk email messages are kept in the quarantine by using anti-spam policies.</span></span> <span data-ttu-id="dbd75-125">La valeur par défaut est 30 jours, ce qui est également la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="dbd75-125">The default is 30 days, which is also the maximum.</span></span> <span data-ttu-id="dbd75-126">Pour plus d’informations, voir [Configurer des stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="dbd75-126">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md)</span></span>

<span data-ttu-id="dbd75-127">Pour les messages mis en quarantaine par l’action de règle de flux de messagerie Remettre le **message** en quarantaine hébergé, les messages sont conservés en quarantaine pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="dbd75-127">For messages that were quarantined by the mail flow rule action **Deliver the message to the hosted quarantine**, the messages are kept in quarantine for 30 days.</span></span> <span data-ttu-id="dbd75-128">Vous ne pouvez pas configurer cette durée.</span><span class="sxs-lookup"><span data-stu-id="dbd75-128">You can't configure this duration.</span></span>

<span data-ttu-id="dbd75-129">Une fois la période expirée, les messages sont supprimés et ne sont pas récupérables.</span><span class="sxs-lookup"><span data-stu-id="dbd75-129">After the time period expires, the messages are deleted and are not recoverable.</span></span>

## <a name="can-i-release-or-report-more-than-one-quarantined-message-at-a-time"></a><span data-ttu-id="dbd75-130">Est-ce que je peux libérer ou signaler plusieurs messages mis en quarantaine à la fois ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-130">Can I release or report more than one quarantined message at a time?</span></span>

<span data-ttu-id="dbd75-131">Dans le Centre de sécurité & conformité, vous pouvez sélectionner et publier jusqu’à 100 messages à la fois.</span><span class="sxs-lookup"><span data-stu-id="dbd75-131">In the Security & Compliance Center, you can select and release up to 100 messages at a time.</span></span>

<span data-ttu-id="dbd75-132">Les administrateurs peuvent utiliser les cmdlets [Get-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/get-quarantinemessage) et [Release-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/release-quarantinemessage) dans Exchange Online PowerShell ou EOP PowerShell autonome pour rechercher et libérer les messages mis en quarantaine en bloc et signaler les faux positifs en bloc.</span><span class="sxs-lookup"><span data-stu-id="dbd75-132">Admins can use the the [Get-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/get-quarantinemessage) and [Release-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/release-quarantinemessage) cmdlets in Exchange Online PowerShell or standalone EOP PowerShell to find and release quarantined messages in bulk, and to report false positives in bulk.</span></span>

## <a name="are-wildcards-supported-when-searching-for-quarantined-messages-can-i-search-for-quarantined-messages-for-a-specific-domain"></a><span data-ttu-id="dbd75-133">Les caractères génériques sont-ils pris en charge lors de la recherche de messages mis en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-133">Are wildcards supported when searching for quarantined messages?</span></span> <span data-ttu-id="dbd75-134">Puis-je rechercher des messages mis en quarantaine pour un domaine spécifique ?</span><span class="sxs-lookup"><span data-stu-id="dbd75-134">Can I search for quarantined messages for a specific domain?</span></span>

<span data-ttu-id="dbd75-135">Les caractères génériques ne sont pas pris en charge dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="dbd75-135">Wildcards aren't supported in the Security & Compliance Center.</span></span> <span data-ttu-id="dbd75-136">Par exemple, lorsque vous recherchez un expéditeur, vous devez spécifier l’adresse de messagerie complète.</span><span class="sxs-lookup"><span data-stu-id="dbd75-136">For example, when searching for a sender, you need to specify the full email address.</span></span> <span data-ttu-id="dbd75-137">Toutefois, vous pouvez utiliser des caractères génériques dans Exchange Online PowerShell ou EOP PowerShell autonome.</span><span class="sxs-lookup"><span data-stu-id="dbd75-137">But, you can use wildcards in Exchange Online PowerShell or standalone EOP PowerShell.</span></span>

<span data-ttu-id="dbd75-138">Par exemple, copiez le code PowerShell suivant dans le Bloc-notes et enregistrez le fichier en tant que fichier .ps1 dans un emplacement facile à trouver (par exemple, C:\Data\QuarantineRelease.ps1).</span><span class="sxs-lookup"><span data-stu-id="dbd75-138">For example, copy the following PowerShell code into NotePad and save the file as .ps1 in a location that's easy for you to find (for example, C:\Data\QuarantineRelease.ps1).</span></span>

<span data-ttu-id="dbd75-139">Ensuite, après vous être connecté à [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) ou [Exchange Online Protection PowerShell,](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell)exécutez la commande suivante pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="dbd75-139">Then, after you connect to [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) or [Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell), run the following command to run the script:</span></span>

```powershell
& C:\Data\QuarantineRelease.ps1
```

<span data-ttu-id="dbd75-140">Le script fait les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbd75-140">The script does the following actions:</span></span>

- <span data-ttu-id="dbd75-141">Recherchez les messages non publiés qui ont été mis en quarantaine comme courrier indésirable de tous les expéditeurs dans le domaine fabrikam.</span><span class="sxs-lookup"><span data-stu-id="dbd75-141">Find unreleased messages that were quarantined as spam from all senders in the fabrikam domain.</span></span> <span data-ttu-id="dbd75-142">Le nombre maximal de résultats est de 50 000 (50 pages de 1 000 résultats).</span><span class="sxs-lookup"><span data-stu-id="dbd75-142">The maximum number of results is 50,000 (50 pages of 1000 results).</span></span>
- <span data-ttu-id="dbd75-143">Enregistrez les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="dbd75-143">Save the results to a CSV file.</span></span>
- <span data-ttu-id="dbd75-144">Libérer les messages mis en quarantaine correspondants à tous les destinataires d’origine.</span><span class="sxs-lookup"><span data-stu-id="dbd75-144">Release the matching quarantined messages to all original recipients.</span></span>

```powershell
$Page = 1
$List = $null

Do
{
Write-Host "Getting Page " $Page

$List = (Get-QuarantineMessage -Type Spam -PageSize 1000 -Page $Page | where {$_.Released -like "False" -and $_.SenderAddress -like "*fabrikam.com"})
Write-Host "                     " $List.count " rows in this page match"
Write-Host "                                                             Exporting list to appended CSV for logging"
$List | Export-Csv -Path "C:\Data\Quarantined Message Matches.csv" -Append -NoTypeInformation

Write-Host "Releasing page " $Page
$List | foreach {Release-QuarantineMessage -Identity $_.Identity -ReleaseToAll}

$Page = $Page + 1

} Until ($Page -eq 50)
```

<span data-ttu-id="dbd75-145">Après avoir publié un message, vous ne pouvez plus le libérer.</span><span class="sxs-lookup"><span data-stu-id="dbd75-145">After you release a message, you can't release it again.</span></span>
