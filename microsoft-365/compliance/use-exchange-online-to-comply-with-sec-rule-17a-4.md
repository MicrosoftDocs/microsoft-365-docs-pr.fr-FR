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
ms.openlocfilehash: bba51bed4409bfb933b577419f48ab6963d4f7d6
ms.sourcegitcommit: c04f1207cfaddac2a9abef38967c17d689756a96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2020
ms.locfileid: "46577114"
---
# <a name="use-exchange-online-and-the-security--compliance-center-to-comply-with-sec-rule-17a-4"></a><span data-ttu-id="d2f43-103">Utiliser Exchange Online et le centre de sécurité et conformité pour se conformer à la règle SEC 17a-4</span><span class="sxs-lookup"><span data-stu-id="d2f43-103">Use Exchange Online and the Security & Compliance Center to comply with SEC Rule 17a-4</span></span>

><span data-ttu-id="d2f43-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="d2f43-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="d2f43-p101">Si votre organisation doit respecter les normes réglementaires pour conserver vos données, le Centre de sécurité et conformité fournit des fonctionnalités pour gérer le cycle de vie de vos données dans Exchange Online. Cela inclut la possibilité de conserver, d’audit, rechercher et exporter vos données. Ces fonctionnalités sont suffisantes pour répondre aux besoins de la plupart des organisations.</span><span class="sxs-lookup"><span data-stu-id="d2f43-p101">If your organization needs to comply with regulatory standards for retaining your data, the Security & Compliance Center provides features to manage the lifecycle of your data in Exchange Online. This includes the ability to retain, audit, search, and export your data. These capabilities are sufficient to meet the needs of most organizations.</span></span>

<span data-ttu-id="d2f43-p102">Toutefois, certaines organisations dans des secteurs hautement réglementés sont soumises à des exigences réglementaires plus stricts. Par exemple, les institutions financières de tels que les banques ou les courtiers sont soumis aux règle 17 a-4 émis par Securities and Exchange Commission (SEC). La Règle 17 a-4 a des exigences spécifiques pour le stockage de données électroniques, y compris de nombreux aspects de la gestion des enregistrements telles que la durée, le format, la qualité, la disponibilité et la responsabilité de rétention des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d2f43-p102">However, some organizations in highly regulated industries are subject to more stringent regulatory requirements. For example, financial institutions such as banks or broker dealers are subject to Rule 17a-4 issued by the Securities and Exchange Commission (SEC). Rule 17a-4 has specific requirements for electronic data storage, including many aspects of record management, such as the duration, format, quality, availability, and accountability of records retention.</span></span>

<span data-ttu-id="d2f43-111">Pour aider ces organisations à mieux comprendre comment le Centre de Sécurité et Conformité peut être utilisé pour répondre à leurs obligations légales pour Exchange Online. plus précisément par rapport à la configuration requise relative à la règle 17 a-4, nous avons publié une évaluation en partenariat avec Cohasset Associates.</span><span class="sxs-lookup"><span data-stu-id="d2f43-111">To help these organizations better understand how the Security & Compliance Center can be leveraged to meet their regulatory obligations for Exchange Online, specifically in relation to Rule 17a-4 requirements, we have released an assessment in partnership with Cohasset Associates.</span></span>

<span data-ttu-id="d2f43-p103">Cohasset a validé que lorsque Exchange Online et le Centre de Sécurité et Conformité sont configurés comme recommandé, ils répondent aux exigences de stockage pertinentes de la règle CFTC 1.31(c)-(d), la FINRA règle 4511 et la SEC règle 17 a-4. Nous avons ciblé cet ensemble de règles car elles représentent les conseils de la plupart des conseils globalement pour la rétention des enregistrements pour les institutions financières.</span><span class="sxs-lookup"><span data-stu-id="d2f43-p103">Cohasset validated that when Exchange Online and the Security & Compliance Center are configured as recommended, they meet the relevant storage requirements of CFTC Rule 1.31(c)-(d), FINRA Rule 4511, and SEC Rule 17a-4. We targeted this set of rules because they represent the most prescriptive guidance globally for records retention for financial institutions.</span></span>

## <a name="download-the-cohasset-assessment"></a><span data-ttu-id="d2f43-114">Télécharger l’évaluation Cohasset</span><span class="sxs-lookup"><span data-stu-id="d2f43-114">Download the Cohasset assessment</span></span>

<span data-ttu-id="d2f43-115">Vous pouvez [télécharger ici l’évaluation Cohasset](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers).</span><span class="sxs-lookup"><span data-stu-id="d2f43-115">You can [download the Cohasset assessment here](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers).</span></span>

![La page de titre de l’évaluation téléchargeable par Cohasset Associates](../media/cohasset-associates-assessment.png)

## <a name="this-assessment-is-specific-to-exchange-online"></a><span data-ttu-id="d2f43-117">Cette évaluation est spécifique à Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d2f43-117">This assessment is specific to Exchange Online</span></span>

<span data-ttu-id="d2f43-p104">Notez que cette évaluation est spécifique à Exchange Online. L’évaluation n’inclut pas les autres services Microsoft 365 tels que SharePoint Online ou OneDrive Entreprise, bien que nous envisageons la prise en charge dans ces services par rapport à SEC 17 a-4 à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="d2f43-p104">Note that this assessment is specific to Exchange Online. The assessment does not include other Microsoft 365 services such as SharePoint Online or OneDrive for Business, although we are planning support for those services with respect to SEC 17a-4 in the future.</span></span>

<span data-ttu-id="d2f43-p105">Il est important de comprendre que Skype Entreprise et Teams stockent également des données dans Exchange Online. Par conséquent, l’évaluation traite les messages de Skype Entreprise, le canal et les messages de conversation à partir de Teams.</span><span class="sxs-lookup"><span data-stu-id="d2f43-p105">It's important to understand that Skype for Business and Teams also store data in Exchange Online. Therefore, the assessment does cover messages from Skype for Business and channel and chat messages from Teams.</span></span>

## <a name="using-preservation-lock-is-key-to-the-recommended-configuration"></a><span data-ttu-id="d2f43-122">À l’aide de verrouillage de conservation est essentiel pour la configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="d2f43-122">Using Preservation Lock is key to the recommended configuration</span></span>

<span data-ttu-id="d2f43-p106">Les secteurs d’activités hautement rigoureuses ont souvent besoin de stocker les communications électroniques afin de répondre à la configuration requise WORM (plusieurs lectures, écriture une seule fois). La configuration requise WORM dicte une solution de stockage dans lequel un enregistrement doit être :</span><span class="sxs-lookup"><span data-stu-id="d2f43-p106">Highly regulated industries are often required to store electronic communications to meet the WORM (write once, read many) requirement. The WORM requirement dictates a storage solution in which a record must be:</span></span>

- <span data-ttu-id="d2f43-125">Conservée pendant une période de rétention obligatoire qui ne peut pas être raccourcie uniquement augmentée.</span><span class="sxs-lookup"><span data-stu-id="d2f43-125">Retained for a required retention period that cannot be shortened, only increased.</span></span>
- <span data-ttu-id="d2f43-126">Immuable, ce qui signifie que l’enregistrement ne peut pas être remplacée, supprimée ou modifiée pendant la période de rétention requise.</span><span class="sxs-lookup"><span data-stu-id="d2f43-126">Immutable, meaning that the record cannot be overwritten, erased, or altered during the required retention period.</span></span>

<span data-ttu-id="d2f43-p107">Dans Exchange Online, lorsqu’une[stratégie de rétention](retention.md) est appliquée à la boîte aux lettres d’un utilisateur, tout contenu de l’utilisateur sera conservée en fonction de critères de la stratégie. En fait, si un utilisateur tente de supprimer ou modifier un message électronique, une copie du message électronique avant la modification est effectuée et conservée dans un emplacement sécurisé, masqué dans la boîte aux lettres de l’utilisateur. Les stratégies de rétention peuvent vous assurer qu’une organisation conserve les communications électroniques, mais ces stratégies peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="d2f43-p107">In Exchange Online, when a [retention policy](retention.md) is applied to a user's mailbox, all the user's content will be retained based on the criteria of the policy. In fact, if a user attempts to delete or modify an email, a copy of the email before the change is made will be preserved in a secure, hidden location in the user's mailbox. Retention policies can help ensure that an organization retains electronic communications, but those policies can be modified.</span></span>

<span data-ttu-id="d2f43-p108">En plaçant un verrouillage de conservation dans une stratégie de rétention, une organisation garantit que la stratégie ne peut pas être modifiée. En fait, une fois un verrouillage de conservation est appliquée à une stratégie de rétention, les actions suivantes sont limitées :</span><span class="sxs-lookup"><span data-stu-id="d2f43-p108">By placing a Preservation Lock on a retention policy, an organization ensures that the policy cannot be modified. In fact, after a Preservation Lock is applied to a retention policy, the following actions are restricted:</span></span>

- <span data-ttu-id="d2f43-132">La période de rétention de la stratégie peut uniquement être accrue, elle ne raccourcie pas.</span><span class="sxs-lookup"><span data-stu-id="d2f43-132">The retention period of the policy can only be increased, not shortened.</span></span>
- <span data-ttu-id="d2f43-133">Les utilisateurs peuvent être ajoutés à la stratégie, mais aucun utilisateur ne peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="d2f43-133">Users can be added to the policy, but no user can be removed.</span></span>
- <span data-ttu-id="d2f43-134">La stratégie de rétention ne peut pas être supprimée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="d2f43-134">The retention policy cannot be deleted by an administrator.</span></span>

<span data-ttu-id="d2f43-135">Le verrouillage de conservation peut vous aider à répondre aux exigences réglementaires SEC 17 a-4.</span><span class="sxs-lookup"><span data-stu-id="d2f43-135">Preservation Lock can help you meet the SEC 17a-4 regulatory requirements.</span></span>

## <a name="how-to-set-up-preservation-lock"></a><span data-ttu-id="d2f43-136">Comment configurer le verrouillage de conservation</span><span class="sxs-lookup"><span data-stu-id="d2f43-136">How to set up Preservation Lock</span></span>

<span data-ttu-id="d2f43-137">Vous pouvez verrouiller une stratégie de rétention à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d2f43-137">You can lock a retention policy by using PowerShell.</span></span> <span data-ttu-id="d2f43-138">Pour plus d’informations, voir [Utiliser le verrouillage de conservation pour se conformer aux exigences réglementaires](retention.md#use-preservation-lock-to-comply-with-regulatory-requirements).</span><span class="sxs-lookup"><span data-stu-id="d2f43-138">For more information, see [Use Preservation Lock to comply with regulatory requirements](retention.md#use-preservation-lock-to-comply-with-regulatory-requirements).</span></span>

