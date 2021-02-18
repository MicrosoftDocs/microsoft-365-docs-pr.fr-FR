---
title: Exécuter un rapport de groupe de rôles d’administrateur dans EOP autonome
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à exécuter un rapport de groupe de rôles d’administrateur dans Exchange Online Protection (EOP) autonome. Ce rapport enregistre lorsqu’un administrateur ajoute des membres à des groupes de rôles d’administrateur ou en supprime.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d778e807a087a5e29b31645457d4a81bd05c5649
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50288018"
---
# <a name="run-an-administrator-role-group-report-in-standalone-eop"></a><span data-ttu-id="c0a5f-104">Exécuter un rapport de groupe de rôles d’administrateur dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="c0a5f-104">Run an administrator role group report in standalone EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="c0a5f-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c0a5f-105">**Applies to**</span></span>
-  [<span data-ttu-id="c0a5f-106">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="c0a5f-106">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="c0a5f-107">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, lorsqu’un administrateur ajoute des membres à des groupes de rôles d’administration ou en supprime, le service enregistre chaque occurrence.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-107">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, when an admin adds members to or removes members from administrative role groups, the service logs each occurrence.</span></span> <span data-ttu-id="c0a5f-108">Pour plus d’informations sur les groupes de rôles dans EOP autonome, voir [Autorisations dans EOP autonome.](feature-permissions-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="c0a5f-108">For more information about role groups in standalone EOP, see [Permissions in standalone EOP](feature-permissions-in-eop.md).</span></span>

<span data-ttu-id="c0a5f-109">Lorsque vous exécutez un rapport de groupe de rôles d’administrateur dans le Centre d’administration Exchange (EAC), les entrées sont affichées en tant que résultats de recherche et incluent les groupes de rôles affectés, qui a modifié l’appartenance au groupe de rôles et quand et quelles mises à jour d’appartenance ont été réalisées.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-109">When you run an administrator role group report in the Exchange admin center (EAC), entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made.</span></span> <span data-ttu-id="c0a5f-110">Utilisez ce rapport pour surveiller les modifications aux autorisations administratives attribuées aux utilisateurs dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-110">Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c0a5f-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c0a5f-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c0a5f-112">Pour ouvrir le Centre d’administration Exchange, consultez le [Centre d’administration Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="c0a5f-112">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="c0a5f-113">Des autorisations doivent vous être attribuées dans Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-113">You need to be assigned permissions in Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="c0a5f-114">Plus précisément, vous avez besoin du rôle Journaux  d’audit ou Journaux d’audit en affichage seul, qui sont attribués par défaut aux groupes de **rôles** Gestion de l’organisation, Gestion de la conformité et Administrateur de la sécurité.  </span><span class="sxs-lookup"><span data-stu-id="c0a5f-114">Specifically, you need the **Audit Logs** or **View-Only Audit Logs** role, which are assigned to the **Organization Management**, **Compliance Management**, and **Security Administrator** role groups by default.</span></span> <span data-ttu-id="c0a5f-115">Pour plus d’informations, voir [Autorisations](feature-permissions-in-eop.md) dans EOP autonome et utiliser le CAE pour modifier la liste des membres des groupes [de rôles.](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)</span><span class="sxs-lookup"><span data-stu-id="c0a5f-115">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="c0a5f-116">Pour plus d’informations sur les raccourcis clavier qui peuvent s’appliquer aux procédures de cet article, voir raccourcis clavier pour le Centre d’administration [Exchange dans Exchange Online.](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)</span><span class="sxs-lookup"><span data-stu-id="c0a5f-116">For information about keyboard shortcuts that may apply to the procedures in this article, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="c0a5f-117">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="c0a5f-117">Having problems?</span></span> <span data-ttu-id="c0a5f-118">Demandez de l’aide dans le Forum [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) .</span><span class="sxs-lookup"><span data-stu-id="c0a5f-118">Ask for help in the [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) forum.</span></span>

## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="c0a5f-119">Utiliser le Centre d'administration Exchange (CAE) pour exécuter un rapport de groupe de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="c0a5f-119">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="c0a5f-120">Exécutez le rapport de groupe de rôles d’administrateur pour rechercher les modifications apportées aux groupes de rôles de gestion dans un délai particulier.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-120">Run the administrator role group report to find the changes to management role groups within a particular time frame.</span></span>

1. <span data-ttu-id="c0a5f-121">Dans le EAC, sélectionnez **Audit** de la gestion de la conformité, puis exécutez un rapport de groupe de \>  **rôles d’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="c0a5f-121">In the EAC, go to **Compliance management** \> **Auditing**, and then choose **Run an administrator role group report**.</span></span>

2. <span data-ttu-id="c0a5f-122">Dans la page **Rechercher les modifications apportées** aux groupes de rôles d’administrateur qui s’ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0a5f-122">In the **Search for changes to administrator role groups** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="c0a5f-123">**Date de début** et **date de fin**: entrez une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-123">**Start date** and **End date**: Enter a date range.</span></span> <span data-ttu-id="c0a5f-124">Par défaut, le rapport recherche toutes les modifications apportées aux groupes de rôles d'administrateur au cours des deux semaines passées.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-124">By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>

   - <span data-ttu-id="c0a5f-125">**Sélectionner des groupes de rôles**: par défaut, tous les groupes de rôles sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-125">**Select role groups**: By default, all role groups are searched.</span></span> <span data-ttu-id="c0a5f-126">Pour filtrer les résultats par groupes de rôles spécifiques, cliquez **sur Sélectionner des groupes de rôles.**</span><span class="sxs-lookup"><span data-stu-id="c0a5f-126">To filter the results by specific role groups, click **Select role groups**.</span></span> <span data-ttu-id="c0a5f-127">Dans la boîte de dialogue qui s’affiche, sélectionnez un groupe de rôles et cliquez **sur Ajouter ->**.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-127">In the dialog that appears, select a role group and click **add ->**.</span></span> <span data-ttu-id="c0a5f-128">Répétez cette étape autant de fois que nécessaire, puis cliquez sur **OK** lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-128">Repeat this step as many times as necessary, and then click **OK** when you're finished.</span></span>

3. <span data-ttu-id="c0a5f-129">Lorsque vous avez terminé, cliquez sur **Rechercher.**</span><span class="sxs-lookup"><span data-stu-id="c0a5f-129">When you're finished, click **Search**.</span></span>

<span data-ttu-id="c0a5f-p108">Si des modifications correspondent aux critères que vous avez spécifiés, elles seront affichées dans le volet des résultats. Cliquez sur un groupe de rôles dans les résultats de la recherche pour afficher les modifications dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-p108">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="c0a5f-132">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="c0a5f-132">How do you know this worked?</span></span>

<span data-ttu-id="c0a5f-p109">Si vous avez bien exécuté un rapport de groupe de rôles d'administrateur, les groupes de rôles qui ont été modifiés dans la plage de dates s'affichent dans le volet des résultats de la recherche. En cas d'absence de résultats, cela signifie qu'aucune modification aux groupes de rôles n'a eu lieu dans la plage de dates indiquée. Si vous pensez que des résultats devraient apparaître, modifiez la plage de dates et réexécutez le rapport.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-p109">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>

## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="c0a5f-136">Surveillances des modifications apportées à l'appartenance à des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="c0a5f-136">Monitor changes to role group membership</span></span>

<span data-ttu-id="c0a5f-p110">Lorsque des membres sont ajoutés ou supprimés dans groupe de rôles, les résultats de la recherche affichés dans le volet d'informations indiquent que l'appartenance à un groupe de rôles a été mise à jour et répertorient les membres actuels. Les résultats n'indiquent pas explicitement quel utilisateur a été ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-p110">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>

<span data-ttu-id="c0a5f-p111">Pour déterminer si un utilisateur a été ajouté ou supprimé, vous devez comparer deux entrées séparées dans le rapport. Par exemple, examinons les entrées de journal suivantes pour le groupe de rôles **Support technique**:</span><span class="sxs-lookup"><span data-stu-id="c0a5f-p111">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span>

> <span data-ttu-id="c0a5f-141">27/1/2018 16:43</span><span class="sxs-lookup"><span data-stu-id="c0a5f-141">1/27/2018 4:43 PM</span></span> <br> <span data-ttu-id="c0a5f-142">Administrateur</span><span class="sxs-lookup"><span data-stu-id="c0a5f-142">Administrator</span></span> <br> <span data-ttu-id="c0a5f-143">Membres mis à jour : Administrateur;annb,florencef;pilarp</span><span class="sxs-lookup"><span data-stu-id="c0a5f-143">Updated members: Administrator;annb,florencef;pilarp</span></span> <br> <span data-ttu-id="c0a5f-144">06/02/2018 10:09</span><span class="sxs-lookup"><span data-stu-id="c0a5f-144">2/06/2018 10:09 AM</span></span> <br> <span data-ttu-id="c0a5f-145">Administrateur</span><span class="sxs-lookup"><span data-stu-id="c0a5f-145">Administrator</span></span> <br> <span data-ttu-id="c0a5f-146">Membres mis à jour : Administrator;annb;florencef;pilarp;tonip</span><span class="sxs-lookup"><span data-stu-id="c0a5f-146">Updated members: Administrator;annb;florencef;pilarp;tonip</span></span> <br> <span data-ttu-id="c0a5f-147">19/2/2018 14:12</span><span class="sxs-lookup"><span data-stu-id="c0a5f-147">2/19/2018 2:12 PM</span></span> <br> <span data-ttu-id="c0a5f-148">Administrateur</span><span class="sxs-lookup"><span data-stu-id="c0a5f-148">Administrator</span></span> <br> <span data-ttu-id="c0a5f-149">Membres mis à jour : Administrator;annb;florencef;tonip</span><span class="sxs-lookup"><span data-stu-id="c0a5f-149">Updated members: Administrator;annb;florencef;tonip</span></span>

<span data-ttu-id="c0a5f-150">Dans cet exemple, le compte d'utilisateur Administrateur a apporté les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0a5f-150">In this example, the Administrator user account made the following changes:</span></span>

- <span data-ttu-id="c0a5f-151">Le 06/02/2018, l’utilisateur a ajouté le tonip.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-151">On 2/06/2018, they added the user tonip.</span></span>
- <span data-ttu-id="c0a5f-152">Le 19/02/2018, l’utilisateur pilarp a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-152">On 2/19/2018, they removed the user pilarp.</span></span>

## <a name="use-standalone-exchange-online-powershell-to-search-for-audit-log-entries"></a><span data-ttu-id="c0a5f-153">Utiliser Exchange Online PowerShell autonome pour rechercher des entrées du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="c0a5f-153">Use standalone Exchange Online PowerShell to search for audit log entries</span></span>

<span data-ttu-id="c0a5f-154">Vous pouvez utiliser Exchange Online PowerShell pour rechercher des entrées du journal d’audit qui répondent aux critères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-154">You can use Exchange Online PowerShell to search for audit log entries that meet the criteria you specify.</span></span> <span data-ttu-id="c0a5f-155">Pour obtenir la liste des critères de recherche, voir Les critères de [recherche Search-AdminAuditLog.](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#search-adminauditlog-cmdlet)</span><span class="sxs-lookup"><span data-stu-id="c0a5f-155">For a list of search criteria, see [Search-AdminAuditLog search criteria](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#search-adminauditlog-cmdlet).</span></span> <span data-ttu-id="c0a5f-156">Cette procédure utilise la cmdlet **Search-AdminAuditLog** et affiche les résultats de recherche dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-156">This procedure uses the **Search-AdminAuditLog** cmdlet and displays search results in Exchange Online PowerShell.</span></span> <span data-ttu-id="c0a5f-157">Vous pouvez utiliser cette cmdlet si vous devez renvoyer un ensemble de résultats au-delà des limites définies dans la cmdlet **New-AdminAuditLogSearch** ou dans les rapports d'audit du Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-157">You can use this cmdlet when you need to return a set of results that exceeds the limits defined on the **New-AdminAuditLogSearch** cmdlet or in the EAC Audit Reporting reports.</span></span>

<span data-ttu-id="c0a5f-158">Pour effectuer une recherche dans le journal d'audit d'après les critères que vous avez définis, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-158">To search the audit log for criteria you specify, use the following syntax.</span></span>

```PowerShell
Search-AdminAuditLog - Cmdlets <cmdlet 1, cmdlet 2, ...> -Parameters <parameter 1, parameter 2, ...> -StartDate <start date> -EndDate <end date> -UserIds <user IDs> -ObjectIds <object IDs> -IsSuccess <$True | $False >
```

> [!NOTE]
> <span data-ttu-id="c0a5f-159">Par défaut, la cmdlet **Search-AdminAuditLog** renvoie un maximum de 1 000 entrées du journal.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-159">The **Search-AdminAuditLog** cmdlet returns a maximum of 1,000 log entries by default.</span></span> <span data-ttu-id="c0a5f-160">Utilisez le _paramètre ResultSize_ pour spécifier jusqu’à 250 000 entrées de journal.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-160">Use the _ResultSize_ parameter to specify up to 250,000 log entries.</span></span> <span data-ttu-id="c0a5f-161">Vous pouvez également utiliser la valeur `Unlimited` pour renvoyer toutes les entrées.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-161">Or, use the value `Unlimited` to return all entries.</span></span>

<span data-ttu-id="c0a5f-162">Cet exemple effectue une recherche portant sur toutes les entrées du journal d'audit avec les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="c0a5f-162">This example performs a search for all audit log entries with the following criteria:</span></span>

- <span data-ttu-id="c0a5f-163">**Date de** début : 04/08/2018</span><span class="sxs-lookup"><span data-stu-id="c0a5f-163">**Start date**: 08/04/2018</span></span>
- <span data-ttu-id="c0a5f-164">**Date de** fin : 03/10/2018</span><span class="sxs-lookup"><span data-stu-id="c0a5f-164">**End date**: 10/03/2018</span></span>
- <span data-ttu-id="c0a5f-165">**ID utilisateur :** `davids` , `chrisd` , `kima`</span><span class="sxs-lookup"><span data-stu-id="c0a5f-165">**User IDs**: `davids`, `chrisd`, `kima`</span></span>
- <span data-ttu-id="c0a5f-166">**Cmdlets**: **Set-Mailbox**</span><span class="sxs-lookup"><span data-stu-id="c0a5f-166">**Cmdlets**: **Set-Mailbox**</span></span>
- <span data-ttu-id="c0a5f-167">**Paramètres**: _ProhibitSendQuota_, _ProhibitSendReceiveQuota_, _IssueWarningQuota_, _MaxSendSize_, _MaxReceiveSize_</span><span class="sxs-lookup"><span data-stu-id="c0a5f-167">**Parameters**: _ProhibitSendQuota_, _ProhibitSendReceiveQuota_, _IssueWarningQuota_, _MaxSendSize_, _MaxReceiveSize_</span></span>

```PowerShell
Search-AdminAuditLog -Cmdlets Set-Mailbox -Parameters ProhibitSendQuota,ProhibitSendReceiveQuota,IssueWarningQuota,MaxSendSize,MaxReceiveSize -StartDate 08/04/2018 -EndDate 10/03/2018 -UserIds davids,chrisd,kima
```

<span data-ttu-id="c0a5f-p114">Cet exemple recherche les modifications apportées à une boîte aux lettres spécifique. Ceci est utile si vous effectuez des opérations de dépannage ou devez fournir des informations à des fins d'investigation. Les critères suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="c0a5f-p114">This example searches for changes made to a specific mailbox. This is useful if you're troubleshooting or you need to provide information for an investigation. The following criteria are used:</span></span>

- <span data-ttu-id="c0a5f-171">**Date de** début : 01/05/2018</span><span class="sxs-lookup"><span data-stu-id="c0a5f-171">**Start date**: 05/01/2018</span></span>
- <span data-ttu-id="c0a5f-172">**Date de** fin : 03/10/2018</span><span class="sxs-lookup"><span data-stu-id="c0a5f-172">**End date**: 10/03/2018</span></span>
- <span data-ttu-id="c0a5f-173">**ID d’objet**: contoso.com/Users/DavidS</span><span class="sxs-lookup"><span data-stu-id="c0a5f-173">**Object ID**: contoso.com/Users/DavidS</span></span>

```PowerShell
Search-AdminAuditLog -StartDate 05/01/2018 -EndDate 10/03/2018 -ObjectID contoso.com/Users/DavidS
```

<span data-ttu-id="c0a5f-174">Si vos recherches renvoient de nombreuses entrées de journal, nous vous recommandons d’utiliser la procédure fournie dans **Exchange Online PowerShell** pour rechercher des entrées du journal d’audit et envoyer des résultats à un destinataire plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-174">If your searches return many log entries, we recommend that you use the procedure provided in **Use Exchange Online PowerShell to search for audit log entries and send results to a recipient** later in this article.</span></span> <span data-ttu-id="c0a5f-175">La procédure décrite dans cette section a pour objet d'envoyer aux destinataires que vous spécifiez un fichier XML sous forme de pièce jointe à un message électronique, ce qui vous permet d'extraire plus aisément les données qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-175">The procedure in that section sends an XML file as an email attachment to the recipients you specify, enabling you to more easily extract the data you're interested in.</span></span>

<span data-ttu-id="c0a5f-176">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-adminauditlog).</span><span class="sxs-lookup"><span data-stu-id="c0a5f-176">For detailed syntax and parameter information, see [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-adminauditlog).</span></span>

### <a name="view-details-of-audit-log-entries"></a><span data-ttu-id="c0a5f-177">Afficher le détail des entrées du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="c0a5f-177">View details of audit log entries</span></span>

<span data-ttu-id="c0a5f-178">La cmdlet **Search-AdminAuditLog** renvoie les champs décrits dans le contenu [du journal d’audit.](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#audit-log-contents)</span><span class="sxs-lookup"><span data-stu-id="c0a5f-178">The **Search-AdminAuditLog** cmdlet returns the fields described in [Audit log contents](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#audit-log-contents).</span></span> <span data-ttu-id="c0a5f-179">Parmi les champs renvoyés par la cmdlet, deux champs ( **CmdletParameters** et **ModifiedProperties** ) comportent des données supplémentaires qu'il est impossible de visualiser par défaut.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-179">Of the fields returned by the cmdlet, two fields, **CmdletParameters** and **ModifiedProperties**, contain additional information that isn't viewable by default.</span></span>

<span data-ttu-id="c0a5f-180">Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties**, suivez la procédure ci-après.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-180">To view the contents of the **CmdletParameters** and **ModifiedProperties** fields, use the following steps.</span></span> <span data-ttu-id="c0a5f-181">Vous pouvez également utiliser la procédure d’utilisation **d’Exchange Online PowerShell** pour rechercher des entrées du journal d’audit et envoyer des résultats à un destinataire plus loin dans cet article pour créer un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-181">Or, you can use the procedure in **Use Exchange Online PowerShell to search for audit log entries and send results to a recipient** later in this article to create an XML file.</span></span>

<span data-ttu-id="c0a5f-182">Cette procédure exploite les concepts suivants :</span><span class="sxs-lookup"><span data-stu-id="c0a5f-182">This procedure uses the following concepts:</span></span>

- [<span data-ttu-id="c0a5f-183">about_Arrays</span><span class="sxs-lookup"><span data-stu-id="c0a5f-183">about_Arrays</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_arrays)

- [<span data-ttu-id="c0a5f-184">about_Variables</span><span class="sxs-lookup"><span data-stu-id="c0a5f-184">about_Variables</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_variables)

1. <span data-ttu-id="c0a5f-185">Déterminez les critères sur lesquels doivent porter vos recherches, exécutez la cmdlet **Search-AdminAuditLog** et stockez les résultats dans une variable au moyen de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-185">Decide the criteria you want to search for, run the **Search-AdminAuditLog** cmdlet, and store the results in a variable using the following command.</span></span>

   ```PowerShell
   $Results = Search-AdminAuditLog <search criteria>
   ```

2. <span data-ttu-id="c0a5f-186">Chaque entrée du journal d’audit est stockée en tant qu’élément de tableau dans la `$Results` variable.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-186">Each audit log entry is stored as an array element in the variable `$Results`.</span></span> <span data-ttu-id="c0a5f-187">Vous pouvez sélectionner un élément de tableau en précisant son index.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-187">You can select an array element by specifying its array element index.</span></span> <span data-ttu-id="c0a5f-188">Les index des éléments de tableau commencent à zéro (0) pour le premier élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-188">Array element indexes start at zero (0) for the first array element.</span></span> <span data-ttu-id="c0a5f-189">Par exemple, pour extraire le cinquième élément de tableau dont l'index est 4, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-189">For example, to retrieve the 5th array element, which has an index of 4, use the following command.</span></span>

   ```PowerShell
   $Results[4]
   ```

3. <span data-ttu-id="c0a5f-p119">La commande précédente renvoie l'entrée du journal stockée dans l'élément de tableau 4. Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties** pour cette entrée du journal, utilisez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-p119">The previous command returns the log entry stored in array element 4. To see the contents of the **CmdletParameters** and **ModifiedProperties** fields for this log entry, use the following commands.</span></span>

   ```PowerShell
   $Results[4].CmdletParameters
   $Results[4].ModifiedProperties
   ```

4. <span data-ttu-id="c0a5f-192">Pour afficher le contenu des champs **CmdletParameters** ou **ModifiedParameters** dans une autre entrée du journal, modifiez l'index de l'élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="c0a5f-192">To view the contents of the **CmdletParameters** or **ModifiedParameters** fields in another log entry, change the array element index.</span></span>
