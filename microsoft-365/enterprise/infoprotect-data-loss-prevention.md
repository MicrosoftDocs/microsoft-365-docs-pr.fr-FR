---
title: 'Étape 5 : configurer la prévention des pertes de données Office 365'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre et déployer Prévention des pertes de données Office 365 dans Microsoft 365.
ms.openlocfilehash: d0a8beae3797e59eb1eb130afb9fd123be57d909
ms.sourcegitcommit: 9d4319a015e493fb88c7e1855bca0121654eb39d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2019
ms.locfileid: "33308341"
---
# <a name="step-5-configure-office-365-data-loss-prevention"></a><span data-ttu-id="540b8-103">Étape 5 : configurer la prévention des pertes de données Office 365</span><span class="sxs-lookup"><span data-stu-id="540b8-103">Step 5: Configure Office 365 Data Loss Prevention</span></span>

<span data-ttu-id="540b8-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="540b8-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="540b8-105">Les stratégies de protection contre la perte de données (DLP) disponibles dans le Centre de sécurité et conformité Office 365 vous permettent d’identifier, de surveiller et de protéger automatiquement des informations sensibles dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="540b8-105">Protection of personal information in Office 365 includes using data loss prevention capabilities. With data loss prevention (DLP) policies in the Office 365 Security & Compliance Center, you can identify, monitor, and automatically protect sensitive information across Office 365.</span></span> <span data-ttu-id="540b8-106">Avec les stratégies DLP, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="540b8-106">With DLP, you can:</span></span>

- <span data-ttu-id="540b8-107">Identifier les informations sensibles à de nombreux emplacements, comme Exchange Online, SharePoint Online, OneDrive Entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="540b8-107">	Identify sensitive information across many locations, such as SharePoint Online and OneDrive for Business.</span></span>
- <span data-ttu-id="540b8-108">Empêcher le partage accidentel d’informations sensibles en bloquant l’accès à un document ou le courrier qui le contient.</span><span class="sxs-lookup"><span data-stu-id="540b8-108">Prevent the accidental sharing of sensitive information by blocking access to a document or blocking the email that contains it.</span></span>
- <span data-ttu-id="540b8-109">Surveiller et protéger les informations sensibles dans les versions de bureau d’Excel, de PowerPoint et de Word.</span><span class="sxs-lookup"><span data-stu-id="540b8-109">Monitor and protect sensitive information in the desktop versions of Excel 2016, PowerPoint 2016, and Word 2016.</span></span>
- <span data-ttu-id="540b8-110">Aider les utilisateurs à respecter les règles de conformité sans interrompre leur flux de travail avec des notifications e-mail et conseils de stratégie.</span><span class="sxs-lookup"><span data-stu-id="540b8-110">Help users learn how to stay compliant without interrupting their workflow with email notifications and policy tips.</span></span> 
- <span data-ttu-id="540b8-111">Consulter les rapports DLP présentant le contenu qui correspond aux stratégies DLP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="540b8-111">View DLP reports showing content that matches your organization’s DLP policies.</span></span>

<span data-ttu-id="540b8-112">Une stratégie DLP spécifie :</span><span class="sxs-lookup"><span data-stu-id="540b8-112">A DLP policy specifies:</span></span>

- <span data-ttu-id="540b8-113">**Où :** emplacements comme Exchange Online, SharePoint Online, sites OneDrive Entreprise et chats et canaux Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="540b8-113">**Where:** Locations such as Exchange Online, SharePoint Online, and OneDrive for Business sites, as well as Microsoft Teams chats and channels.</span></span>
- <span data-ttu-id="540b8-114">**Quand :** conditions auxquelles le contenu doit correspondre au sein d’une règle de stratégie spécifique.</span><span class="sxs-lookup"><span data-stu-id="540b8-114">**When:** Conditions the content must match within a specific policy rule.</span></span>
- <span data-ttu-id="540b8-115">**Comment :** actions dans cette règle de stratégie correspondante permettant d’adapter automatiquement les conditions correspondantes.</span><span class="sxs-lookup"><span data-stu-id="540b8-115">**How:** Actions within that matching policy rule to take automatically for the matching conditions.</span></span>

<span data-ttu-id="540b8-116">En d’autres termes :</span><span class="sxs-lookup"><span data-stu-id="540b8-116">In other words:</span></span>

- <span data-ttu-id="540b8-117">Pour un document dans cet emplacement (où), si le contenu remplit les conditions d’une règle (quand), alors automatiquement effectuer les actions spécifiées dans la règle (comment).</span><span class="sxs-lookup"><span data-stu-id="540b8-117">For a document in this location (where), if the content matches the conditions of a rule (when), then automatically take the actions specified in the rule (how).</span></span>

<span data-ttu-id="540b8-118">Pour déterminer l’ensemble de stratégies DLP dont vous avez besoin, vous devez analyser vos documents et les types de données y figurant nécessitant une protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="540b8-118">To determine the set of DLP policies you need, you must analyze your documents and the types of data within them that need protection from data loss.</span></span> <span data-ttu-id="540b8-119">Par exemple, si vous êtes une entreprise financière aux États-Unis, vous pouvez créer une stratégie DLP qui empêche le partage de documents avec des numéros de sécurité sociale en dehors de l’organisation ou envoyés dans un courrier électronique à des emplacements externes à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="540b8-119">For example, if you are a financial organization in the United States of America, you would create a DLP policy that prevents documents with social security numbers from being shared outside the organization or sent in email to locations outside the organization.</span></span>

<span data-ttu-id="540b8-120">Ensuite, vous configurez et testez les stratégies avec des emplacements tests pour vous assurer que le comportement DLP est correct et pour réduire les faux positifs.</span><span class="sxs-lookup"><span data-stu-id="540b8-120">Next, you configure and test the policies with test locations to ensure the correct DLP behavior and to minimize false positives.</span></span>

<span data-ttu-id="540b8-121">Enfin, vous le déployez dans votre organisation en informant les employés de nouvelles stratégies et leur comportement souhaité et vous élargissez l’étendue des emplacements.</span><span class="sxs-lookup"><span data-stu-id="540b8-121">Finally, you roll it out to your organization by informing the employees of the new policies and their desired behavior and widening the scope of the locations.</span></span>

<span data-ttu-id="540b8-122">Pour plus d’informations, voir [prise en main recommandations en matière de stratégie DLP](https://docs.microsoft.com/office365/securitycompliance/get-started-with-dlp-policy-recommendations).</span><span class="sxs-lookup"><span data-stu-id="540b8-122">For more information, see [Get started with DLP policy recommendations](https://docs.microsoft.com/office365/securitycompliance/get-started-with-dlp-policy-recommendations).</span></span>

<span data-ttu-id="540b8-123">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step5) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="540b8-123">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step5) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="540b8-124">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="540b8-124">Next step</span></span>


|||
|:-------|:-----|
|![](./media/stepnumbers/Step6.png)|[<span data-ttu-id="540b8-125">Configurez la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="540b8-125">Configure privileged access management for Office 365</span></span>](infoprotect-configure-privileged-access-management.md)|


