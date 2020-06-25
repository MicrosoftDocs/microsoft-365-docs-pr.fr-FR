---
title: Utiliser Exchange Online et le centre de sécurité et conformité pour se conformer à la règle SEC 17a-4
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: Configurer le Centre de conformité et Exchange Online pour de répondre aux exigences réglementaires de la règle CFTC 1.31 (c)-(d), règle FINRA 4511 et la règle SEC 17a -4.
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
ms.openlocfilehash: 6dc53ec9dd016a2423ca96886bba400e2f17e17a
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819074"
---
# <a name="use-exchange-online-and-the-security--compliance-center-to-comply-with-sec-rule-17a-4"></a><span data-ttu-id="19ecb-103">Utiliser Exchange Online et le centre de sécurité et conformité pour se conformer à la règle SEC 17a-4</span><span class="sxs-lookup"><span data-stu-id="19ecb-103">Use Exchange Online and the Security & Compliance Center to comply with SEC Rule 17a-4</span></span>

><span data-ttu-id="19ecb-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="19ecb-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="19ecb-105">If your organization needs to comply with regulatory standards for retaining your data, the Security & Compliance Center provides features to manage the lifecycle of your data in Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="19ecb-105">If your organization needs to comply with regulatory standards for retaining your data, the Security & Compliance Center provides features to manage the lifecycle of your data in Exchange Online.</span></span> <span data-ttu-id="19ecb-106">This includes the ability to retain, audit, search, and export your data.</span><span class="sxs-lookup"><span data-stu-id="19ecb-106">This includes the ability to retain, audit, search, and export your data.</span></span> <span data-ttu-id="19ecb-107">These capabilities are sufficient to meet the needs of most organizations.</span><span class="sxs-lookup"><span data-stu-id="19ecb-107">These capabilities are sufficient to meet the needs of most organizations.</span></span>

<span data-ttu-id="19ecb-108">However, some organizations in highly regulated industries are subject to more stringent regulatory requirements.</span><span class="sxs-lookup"><span data-stu-id="19ecb-108">However, some organizations in highly regulated industries are subject to more stringent regulatory requirements.</span></span> <span data-ttu-id="19ecb-109">For example, financial institutions such as banks or broker dealers are subject to Rule 17a-4 issued by the Securities and Exchange Commission (SEC).</span><span class="sxs-lookup"><span data-stu-id="19ecb-109">For example, financial institutions such as banks or broker dealers are subject to Rule 17a-4 issued by the Securities and Exchange Commission (SEC).</span></span> <span data-ttu-id="19ecb-110">Rule 17a-4 has specific requirements for electronic data storage, including many aspects of record management, such as the duration, format, quality, availability, and accountability of records retention.</span><span class="sxs-lookup"><span data-stu-id="19ecb-110">Rule 17a-4 has specific requirements for electronic data storage, including many aspects of record management, such as the duration, format, quality, availability, and accountability of records retention.</span></span>

<span data-ttu-id="19ecb-111">Pour aider ces organisations à mieux comprendre comment le Centre de Sécurité et Conformité peut être utilisé pour répondre à leurs obligations légales pour Exchange Online. plus précisément par rapport à la configuration requise relative à la règle 17 a-4, nous avons publié une évaluation en partenariat avec Cohasset Associates.</span><span class="sxs-lookup"><span data-stu-id="19ecb-111">To help these organizations better understand how the Security & Compliance Center can be leveraged to meet their regulatory obligations for Exchange Online, specifically in relation to Rule 17a-4 requirements, we have released an assessment in partnership with Cohasset Associates.</span></span>

<span data-ttu-id="19ecb-112">Cohasset validated that when Exchange Online and the Security & Compliance Center are configured as recommended, they meet the relevant storage requirements of CFTC Rule 1.31(c)-(d), FINRA Rule 4511, and SEC Rule 17a-4.</span><span class="sxs-lookup"><span data-stu-id="19ecb-112">Cohasset validated that when Exchange Online and the Security & Compliance Center are configured as recommended, they meet the relevant storage requirements of CFTC Rule 1.31(c)-(d), FINRA Rule 4511, and SEC Rule 17a-4.</span></span> <span data-ttu-id="19ecb-113">We targeted this set of rules because they represent the most prescriptive guidance globally for records retention for financial institutions.</span><span class="sxs-lookup"><span data-stu-id="19ecb-113">We targeted this set of rules because they represent the most prescriptive guidance globally for records retention for financial institutions.</span></span>

## <a name="download-the-cohasset-assessment"></a><span data-ttu-id="19ecb-114">Télécharger l’évaluation Cohasset</span><span class="sxs-lookup"><span data-stu-id="19ecb-114">Download the Cohasset assessment</span></span>

<span data-ttu-id="19ecb-115">Vous pouvez [télécharger ici l’évaluation Cohasset](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers).</span><span class="sxs-lookup"><span data-stu-id="19ecb-115">You can [download the Cohasset assessment here](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers).</span></span>

![La page de titre de l’évaluation téléchargeable par Cohasset Associates](../media/cohasset-associates-assessment.png)

## <a name="this-assessment-is-specific-to-exchange-online"></a><span data-ttu-id="19ecb-117">Cette évaluation est spécifique à Exchange Online</span><span class="sxs-lookup"><span data-stu-id="19ecb-117">This assessment is specific to Exchange Online</span></span>

<span data-ttu-id="19ecb-118">Note that this assessment is specific to Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="19ecb-118">Note that this assessment is specific to Exchange Online.</span></span> <span data-ttu-id="19ecb-119">The assessment does not include other Microsoft 365 services such as SharePoint Online or OneDrive for Business, although we are planning support for those services with respect to SEC 17a-4 in the future.</span><span class="sxs-lookup"><span data-stu-id="19ecb-119">The assessment does not include other Microsoft 365 services such as SharePoint Online or OneDrive for Business, although we are planning support for those services with respect to SEC 17a-4 in the future.</span></span>

<span data-ttu-id="19ecb-120">It's important to understand that Skype for Business and Teams also store data in Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="19ecb-120">It's important to understand that Skype for Business and Teams also store data in Exchange Online.</span></span> <span data-ttu-id="19ecb-121">Therefore, the assessment does cover messages from Skype for Business and channel and chat messages from Teams.</span><span class="sxs-lookup"><span data-stu-id="19ecb-121">Therefore, the assessment does cover messages from Skype for Business and channel and chat messages from Teams.</span></span>

## <a name="using-preservation-lock-is-key-to-the-recommended-configuration"></a><span data-ttu-id="19ecb-122">À l’aide de verrouillage de conservation est essentiel pour la configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="19ecb-122">Using Preservation Lock is key to the recommended configuration</span></span>

<span data-ttu-id="19ecb-123">Highly regulated industries are often required to store electronic communications to meet the WORM (write once, read many) requirement.</span><span class="sxs-lookup"><span data-stu-id="19ecb-123">Highly regulated industries are often required to store electronic communications to meet the WORM (write once, read many) requirement.</span></span> <span data-ttu-id="19ecb-124">The WORM requirement dictates a storage solution in which a record must be:</span><span class="sxs-lookup"><span data-stu-id="19ecb-124">The WORM requirement dictates a storage solution in which a record must be:</span></span>

- <span data-ttu-id="19ecb-125">Conservée pendant une période de rétention obligatoire qui ne peut pas être raccourcie uniquement augmentée.</span><span class="sxs-lookup"><span data-stu-id="19ecb-125">Retained for a required retention period that cannot be shortened, only increased.</span></span>
- <span data-ttu-id="19ecb-126">Immuable, ce qui signifie que l’enregistrement ne peut pas être remplacée, supprimée ou modifiée pendant la période de rétention requise.</span><span class="sxs-lookup"><span data-stu-id="19ecb-126">Immutable, meaning that the record cannot be overwritten, erased, or altered during the required retention period.</span></span>

<span data-ttu-id="19ecb-127">In Exchange Online, when a [retention policy](retention-policies.md) is applied to a user's mailbox, all the user's content will be retained based on the criteria of the policy.</span><span class="sxs-lookup"><span data-stu-id="19ecb-127">In Exchange Online, when a [retention policy](retention-policies.md) is applied to a user's mailbox, all the user's content will be retained based on the criteria of the policy.</span></span> <span data-ttu-id="19ecb-128">In fact, if a user attempts to delete or modify an email, a copy of the email before the change is made will be preserved in a secure, hidden location in the user's mailbox.</span><span class="sxs-lookup"><span data-stu-id="19ecb-128">In fact, if a user attempts to delete or modify an email, a copy of the email before the change is made will be preserved in a secure, hidden location in the user's mailbox.</span></span> <span data-ttu-id="19ecb-129">Retention policies can help ensure that an organization retains electronic communications, but those policies can be modified.</span><span class="sxs-lookup"><span data-stu-id="19ecb-129">Retention policies can help ensure that an organization retains electronic communications, but those policies can be modified.</span></span>

<span data-ttu-id="19ecb-130">By placing a Preservation Lock on a retention policy, an organization ensures that the policy cannot be modified.</span><span class="sxs-lookup"><span data-stu-id="19ecb-130">By placing a Preservation Lock on a retention policy, an organization ensures that the policy cannot be modified.</span></span> <span data-ttu-id="19ecb-131">In fact, after a Preservation Lock is applied to a retention policy, the following actions are restricted:</span><span class="sxs-lookup"><span data-stu-id="19ecb-131">In fact, after a Preservation Lock is applied to a retention policy, the following actions are restricted:</span></span>

- <span data-ttu-id="19ecb-132">La période de rétention de la stratégie peut uniquement être accrue, elle ne raccourcie pas.</span><span class="sxs-lookup"><span data-stu-id="19ecb-132">The retention period of the policy can only be increased, not shortened.</span></span>
- <span data-ttu-id="19ecb-133">Les utilisateurs peuvent être ajoutés à la stratégie, mais aucun utilisateur ne peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="19ecb-133">Users can be added to the policy, but no user can be removed.</span></span>
- <span data-ttu-id="19ecb-134">La stratégie de rétention ne peut pas être supprimée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="19ecb-134">The retention policy cannot be deleted by an administrator.</span></span>

<span data-ttu-id="19ecb-135">Le verrouillage de conservation peut vous aider à répondre aux exigences réglementaires SEC 17 a-4.</span><span class="sxs-lookup"><span data-stu-id="19ecb-135">Preservation Lock can help you meet the SEC 17a-4 regulatory requirements.</span></span>

## <a name="how-to-set-up-preservation-lock"></a><span data-ttu-id="19ecb-136">Comment configurer le verrouillage de conservation</span><span class="sxs-lookup"><span data-stu-id="19ecb-136">How to set up Preservation Lock</span></span>

<span data-ttu-id="19ecb-137">Vous pouvez verrouiller une stratégie de rétention à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19ecb-137">You can lock a retention policy by using PowerShell.</span></span> <span data-ttu-id="19ecb-138">Pour plus d’informations, voir [Utiliser le verrouillage de conservation pour se conformer aux exigences réglementaires](retention-policies.md#use-preservation-lock-to-comply-with-regulatory-requirements).</span><span class="sxs-lookup"><span data-stu-id="19ecb-138">For more information, see [Use Preservation Lock to comply with regulatory requirements](retention-policies.md#use-preservation-lock-to-comply-with-regulatory-requirements).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="19ecb-139">Limitations connues</span><span class="sxs-lookup"><span data-stu-id="19ecb-139">Known limitations</span></span>

<span data-ttu-id="19ecb-140">Il existe actuellement quelques limitations dans Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="19ecb-140">Currently, there are a few limitations for Exchange Online:</span></span>

- <span data-ttu-id="19ecb-141">Les fils de communications ne sont pas disponibles pour les messages de conversation et le canal équipes.</span><span class="sxs-lookup"><span data-stu-id="19ecb-141">Threaded communications are not available for Teams chat and channel messages.</span></span>
- <span data-ttu-id="19ecb-142">Les mentions j’aime ne sont pas conservées pour les messages de conversation et le canal équipes.</span><span class="sxs-lookup"><span data-stu-id="19ecb-142">Likes are not retained for Teams chat and channel messages.</span></span>

> [!NOTE]
> <span data-ttu-id="19ecb-143">L’audit au niveau de l’élément est désormais disponible pour les boîtes aux lettres de groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="19ecb-143">Item-level auditing is now available for Microsoft 365 group mailboxes.</span></span> <span data-ttu-id="19ecb-144">Pour plus d’informations, voir [Gérer l’audit de boîte aux lettres](enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="19ecb-144">For more information, see [Manage mailbox auditing](enable-mailbox-auditing.md).</span></span>
