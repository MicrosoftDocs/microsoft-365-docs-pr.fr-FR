---
title: Déclarer des enregistrements à l’aide d’étiquettes de rétention
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Déclarer des enregistrements à l’aide d’étiquettes de rétention.
ms.openlocfilehash: b5114253c99533e890d66248529b4713700b9016
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52903899"
---
# <a name="declare-records-by-using-retention-labels"></a><span data-ttu-id="d40df-103">Déclarer des enregistrements à l’aide d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="d40df-103">Declare records by using retention labels</span></span>

><span data-ttu-id="d40df-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).*</span><span class="sxs-lookup"><span data-stu-id="d40df-104">*[Microsoft 365 licensing guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).*</span></span>

<span data-ttu-id="d40df-105">Pour déclarer des documents et courriers électroniques comme [enregistrements](records-management.md#records), utilisez [des étiquettes de rétention](retention.md#retention-labels) qui servent à marquer du contenu comme **enregistrement** ou **enregistrement réglementaire**.</span><span class="sxs-lookup"><span data-stu-id="d40df-105">To declare documents and emails as [records](records-management.md#records), you use [retention labels](retention.md#retention-labels) that mark the content as a **record** or a **regulatory record**.</span></span>

<span data-ttu-id="d40df-106">Si vous n’êtes pas certain d’utiliser un enregistrement ou un enregistrement réglementaire, voir [comparer les restrictions relatives aux actions autorisées ou bloquées](records-management.md#compare-restrictions-for-what-actions-are-allowed-or-blocked).</span><span class="sxs-lookup"><span data-stu-id="d40df-106">If you're not sure whether to use a record or a regulatory record, see [Compare restrictions for what actions are allowed or blocked](records-management.md#compare-restrictions-for-what-actions-are-allowed-or-blocked).</span></span> <span data-ttu-id="d40df-107">Si vous avez besoin d’utiliser des enregistrements réglementaires, vous devez commencer par exécuter une commande PowerShell, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="d40df-107">If you need to use regulatory records, you must first run a PowerShell command, as described in the next section.</span></span>

<span data-ttu-id="d40df-108">Vous pouvez soit publier ces étiquettes dans une stratégie d’étiquette de rétention pour permettre aux utilisateurs et aux administrateurs de les appliquer au contenu, ou pour les étiquettes qui marquent les éléments comme enregistrements ( mais pas enregistrements réglementaire) appliquer automatiquement ces étiquettes au contenu que vous voulez marquer comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d40df-108">You can then either publish those labels in a retention label policy so that users and administrators can apply them to content, or for labels that mark items as records (but not regulatory records), auto-apply those labels to content that you want to declare a record.</span></span>

## <a name="how-to-display-the-option-to-mark-content-as-a-regulatory-record"></a><span data-ttu-id="d40df-109">Comment afficher l’option de marquage du contenu en tant qu’enregistrement réglementaire</span><span class="sxs-lookup"><span data-stu-id="d40df-109">How to display the option to mark content as a regulatory record</span></span>

>[!NOTE] 
> <span data-ttu-id="d40df-110">La procédure suivante est une action pouvant être audité, à l’aide de la journalisation **option d’enregistrement réglementaire activée pour les étiquettes de rétention** dans la section du journal d’audit [Stratégie de rétention et activités des étiquettes de rétention](search-the-audit-log-in-security-and-compliance.md#retention-policy-and-retention-label-activities).</span><span class="sxs-lookup"><span data-stu-id="d40df-110">The following procedure is an auditable action, logging **Enabled regulatory record option for retention labels** in the [Retention policy and retention label activities](search-the-audit-log-in-security-and-compliance.md#retention-policy-and-retention-label-activities) section of the audit log.</span></span>

<span data-ttu-id="d40df-111">Par défaut, l’option d’étiquette de rétention permettant de marquer du contenu en tant qu’enregistrement de réglementation n’apparaît pas dans l’assistant de l’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="d40df-111">By default, the retention label option to mark content as a regulatory record isn't displayed in the retention label wizard.</span></span> <span data-ttu-id="d40df-112">Pour afficher cette option, vous devez commencer par exécuter une commande PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d40df-112">To display this option, you must first run a PowerShell command:</span></span>

1. <span data-ttu-id="d40df-113">[Connectez-vous au PowerShell du Centre de sécurité et conformité Office 365](/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="d40df-113">[Connect to the Office 365 Security & Compliance Center PowerShell](/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="d40df-114">Exécutez la l’applet commande suivant :</span><span class="sxs-lookup"><span data-stu-id="d40df-114">Run the following cmdlet:</span></span>
    
    ```powershell
    Set-RegulatoryComplianceUI -Enabled $true
    ````
    <span data-ttu-id="d40df-115">Il n’y a pas d’invite à confirmer et le paramètre prend effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d40df-115">There is no prompt to confirm and the setting takes effect immediately.</span></span>

<span data-ttu-id="d40df-116">Si vous changez d’avis sur la façon de voir cette option dans l’assistant étiquette de rétention, vous pouvez la masquer à nouveau en exécutant le même applet de commande avec la **valeur** faux: `Set-RegulatoryComplianceUI -Enabled $false`</span><span class="sxs-lookup"><span data-stu-id="d40df-116">If you change your mind about seeing this option in the retention label wizard, you can hide it again by running the same cmdlet with the **false** value: `Set-RegulatoryComplianceUI -Enabled $false`</span></span> 

## <a name="configuring-retention-labels-to-declare-records"></a><span data-ttu-id="d40df-117">Configuration d’étiquettes de rétention pour déclarer des enregistrements</span><span class="sxs-lookup"><span data-stu-id="d40df-117">Configuring retention labels to declare records</span></span>

<span data-ttu-id="d40df-118">Lorsque vous créez une étiquette de rétention depuis la solution **Gestion des enregistrements** dans le centre de conformité Microsoft 365, vous pouvez marquer des éléments comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d40df-118">When you create a retention label from the **Records Management** solution in the Microsoft 365 compliance center, you have the option to mark items as a record.</span></span> <span data-ttu-id="d40df-119">Si vous avez exécuté la commande PowerShell à partir de la section précédente, vous pouvez marquer les éléments comme un enregistrement réglementaire de manière alternative.</span><span class="sxs-lookup"><span data-stu-id="d40df-119">If you ran the PowerShell command from the previous section, you can alternatively mark items as a regulatory record.</span></span>

<span data-ttu-id="d40df-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d40df-120">For example:</span></span>

![Configurer une étiquette de rétention pour marquer le contenu en tant qu’enregistrement ou réglementation](../media/recordversioning6.png)

<span data-ttu-id="d40df-122">En utilisant cette étiquette de rétention, vous pouvez désormais l’appliquer aux documents SharePoint ou OneDrive et aux messages électroniques Exchange, comme souhaité.</span><span class="sxs-lookup"><span data-stu-id="d40df-122">Using this retention label, you can now apply it to SharePoint or OneDrive documents and Exchange emails, as needed.</span></span> 

<span data-ttu-id="d40df-123">Pour instructions complètes :</span><span class="sxs-lookup"><span data-stu-id="d40df-123">For full instructions:</span></span>

- [<span data-ttu-id="d40df-124">Créer des étiquettes de rétention et les appliquer dans les applications</span><span class="sxs-lookup"><span data-stu-id="d40df-124">Create retention labels and apply them in apps</span></span>](create-apply-retention-labels.md)

- <span data-ttu-id="d40df-125">[Appliquer une étiquette de rétention au contenu automatiquement](apply-retention-labels-automatically.md) (non pris en charge pour les enregistrements réglementaires)</span><span class="sxs-lookup"><span data-stu-id="d40df-125">[Apply a retention label to content automatically](apply-retention-labels-automatically.md) (not supported for regulatory records)</span></span>


## <a name="applying-the-configured-retention-label-to-content"></a><span data-ttu-id="d40df-126">Application de l’étiquette de rétention configurée au contenu</span><span class="sxs-lookup"><span data-stu-id="d40df-126">Applying the configured retention label to content</span></span>

<span data-ttu-id="d40df-127">Lorsque des étiquettes de rétention qui marquent le contenu en tant qu’enregistrement ou enregistrement réglementaire sont mises à la disposition des utilisateurs pour qu’ils les appliquent dans les applications:</span><span class="sxs-lookup"><span data-stu-id="d40df-127">When retention labels that mark items as a record or regulatory record are made available for users to apply them in apps:</span></span>

- <span data-ttu-id="d40df-128">Pour Exchange, tout utilisateur disposant d’un accès en écriture à la boîte aux lettres peut appliquer ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="d40df-128">For Exchange, any user with write-access to the mailbox can apply these labels.</span></span> 
- <span data-ttu-id="d40df-129">Pour SharePoint et OneDrive, tous les utilisateurs du groupe Membres par défaut (niveau d’autorisation Collaboration) peuvent appliquer ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="d40df-129">For SharePoint and OneDrive, any user in the default Members group (the Contribute permission level) can apply these labels.</span></span>

<span data-ttu-id="d40df-130">Exemple d’un document marqué en tant qu’enregistrement à l’aide d’une étiquette de rétention :</span><span class="sxs-lookup"><span data-stu-id="d40df-130">Example of a document marked as record by using a retention label:</span></span>

![Volet Détails pour le document marqué comme enregistrement](../media/recordversioning7.png)

## <a name="searching-the-audit-log-for-labeled-items-that-were-declared-records"></a><span data-ttu-id="d40df-132">Effectuer une recherche du journal d’audit pour les éléments étiquetés déclarés comme enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d40df-132">Searching the audit log for labeled items that were declared records</span></span>

<span data-ttu-id="d40df-133">Les actions d’étiquetage pour déclarer des éléments comme enregistrements sont enregistrés dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="d40df-133">The actions of labeling to declare items as records are logged in the audit log.</span></span>

<span data-ttu-id="d40df-134">Pour les éléments SharePoint :</span><span class="sxs-lookup"><span data-stu-id="d40df-134">For SharePoint items:</span></span> 
- <span data-ttu-id="d40df-135">Dans **Activités sur les fichiers et les pages**, sélectionnez **Changement d’une étiquette de rétention pour un fichier**.</span><span class="sxs-lookup"><span data-stu-id="d40df-135">From **File and page activities**, select **Changed retention label for a file**.</span></span> <span data-ttu-id="d40df-136">Cet événement d’audit est destiné aux étiquettes de rétention marquant des éléments comme enregistrements, des enregistrements réglementaires ou qui sont des étiquettes de rétention standard.</span><span class="sxs-lookup"><span data-stu-id="d40df-136">This audit event is for retention labels that mark items as records, regulatory records, or that are standard retention labels.</span></span>

<span data-ttu-id="d40df-137">Pour les éléments Exchange :</span><span class="sxs-lookup"><span data-stu-id="d40df-137">For Exchange items:</span></span>
- <span data-ttu-id="d40df-138">Dans **Activités sur la boîte aux lettres Exchange**, sélectionnez **Message étiqueté comme enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="d40df-138">From **Exchange mailbox activities**, select **Labeled message as a record**.</span></span> <span data-ttu-id="d40df-139">Cet événement d’audit est destiné aux étiquettes de rétention marquant des éléments comme enregistrements ou des enregistrements réglementaires.</span><span class="sxs-lookup"><span data-stu-id="d40df-139">This audit event is for retention labels that mark items as records or regulatory records.</span></span>

<span data-ttu-id="d40df-140">Pour plus d’informations sur la recherche de ces événements, consultez [Effectuer une recherche dans le journal d’audit dans le centre de sécurité et conformité](search-the-audit-log-in-security-and-compliance.md#file-and-page-activities).</span><span class="sxs-lookup"><span data-stu-id="d40df-140">For more information about searching for these events, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#file-and-page-activities).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d40df-141">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d40df-141">Next steps</span></span>

<span data-ttu-id="d40df-142">Pour une liste des scénarios pris en charge par la gestion des documents, voir [Scénarios communs pour la gestion des documents](get-started-with-records-management.md#common-scenarios-for-records-management).</span><span class="sxs-lookup"><span data-stu-id="d40df-142">For a list of scenarios supported by records management, see [Common scenarios for records management](get-started-with-records-management.md#common-scenarios-for-records-management).</span></span>
