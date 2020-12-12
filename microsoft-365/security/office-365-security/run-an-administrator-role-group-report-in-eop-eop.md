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
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à exécuter un rapport de groupe de rôles d’administrateur dans Exchange Online Protection (EOP). Ce rapport enregistre les journaux lorsqu’un administrateur ajoute ou supprime des membres des groupes de rôles d’administrateur.
ms.openlocfilehash: cd7ca13a3d863240a0f2608ed13321cbe3d50ad2
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49659262"
---
# <a name="run-an-administrator-role-group-report-in-standalone-eop"></a><span data-ttu-id="04245-104">Exécuter un rapport de groupe de rôles d’administrateur dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="04245-104">Run an administrator role group report in standalone EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="04245-105">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, lorsqu’un administrateur ajoute ou supprime des membres de groupes de rôles d’administration, le service journalise chaque occurrence.</span><span class="sxs-lookup"><span data-stu-id="04245-105">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, when an admin adds members to or removes members from administrative role groups, the service logs each occurrence.</span></span> <span data-ttu-id="04245-106">Pour plus d’informations sur les groupes de rôles dans la version autonome d’EOP, consultez la rubrique [Permissions in standalone EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="04245-106">For more information about role groups in standalone EOP, see [Permissions in standalone EOP](feature-permissions-in-eop.md).</span></span>

<span data-ttu-id="04245-107">Lorsque vous exécutez un rapport de groupe de rôles d’administrateur dans le centre d’administration Exchange, les entrées s’affichent sous la forme de résultats de recherche et incluent les groupes de rôles affectés, la personne qui a modifié l’appartenance au groupe de rôles et le moment, ainsi que les mises à jour d’appartenance.</span><span class="sxs-lookup"><span data-stu-id="04245-107">When you run an administrator role group report in the Exchange admin center (EAC), entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made.</span></span> <span data-ttu-id="04245-108">Utilisez ce rapport pour surveiller les modifications aux autorisations administratives attribuées aux utilisateurs dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="04245-108">Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="04245-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="04245-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="04245-110">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="04245-110">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="04245-111">Pour pouvoir effectuer les procédures décrites dans cet article, vous devez disposer d’autorisations dans Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="04245-111">You need to be assigned permissions in Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="04245-112">Plus précisément, vous avez besoin du rôle journaux **d’audit** ou **journaux d’audit en affichage seul** , qui sont attribués par défaut aux groupes de rôles gestion de l' **organisation**, **gestion de la conformité** et administrateur de la **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="04245-112">Specifically, you need the **Audit Logs** or **View-Only Audit Logs** role, which are assigned to the **Organization Management**, **Compliance Management**, and **Security Administrator** role groups by default.</span></span> <span data-ttu-id="04245-113">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="04245-113">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="04245-114">Pour plus d’informations sur les raccourcis clavier applicables aux procédures décrites dans cet article, reportez-vous à [la rubrique raccourcis clavier du centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="04245-114">For information about keyboard shortcuts that may apply to the procedures in this article, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="04245-115">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="04245-115">Having problems?</span></span> <span data-ttu-id="04245-116">Demandez de l’aide dans le Forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="04245-116">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="04245-117">Utiliser le Centre d'administration Exchange (CAE) pour exécuter un rapport de groupe de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="04245-117">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="04245-118">Exécutez le rapport de groupe de rôles d’administrateur pour rechercher les modifications apportées aux groupes de rôles de gestion dans un laps de temps donné.</span><span class="sxs-lookup"><span data-stu-id="04245-118">Run the administrator role group report to find the changes to management role groups within a particular time frame.</span></span>

1. <span data-ttu-id="04245-119">Dans le centre d’administration Exchange, accédez à audit de **gestion de la conformité** \> , puis choisissez **exécuter un rapport de groupe de rôles d’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="04245-119">In the EAC, go to **Compliance management** \> **Auditing**, and then choose **Run an administrator role group report**.</span></span>

2. <span data-ttu-id="04245-120">Dans la page **Rechercher les modifications apportées aux groupes de rôles d’administrateur** qui s’ouvre, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="04245-120">In the **Search for changes to administrator role groups** page that opens, configure the following settings:</span></span>

   - <span data-ttu-id="04245-121">**Date de début** et **Date de fin**: entrez une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="04245-121">**Start date** and **End date**: Enter a date range.</span></span> <span data-ttu-id="04245-122">Par défaut, le rapport recherche toutes les modifications apportées aux groupes de rôles d'administrateur au cours des deux semaines passées.</span><span class="sxs-lookup"><span data-stu-id="04245-122">By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>

   - <span data-ttu-id="04245-123">**Sélectionner des groupes de rôles**: par défaut, tous les groupes de rôles sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="04245-123">**Select role groups**: By default, all role groups are searched.</span></span> <span data-ttu-id="04245-124">Pour filtrer les résultats par groupes de rôles spécifiques, cliquez sur **Sélectionner des groupes de rôles**.</span><span class="sxs-lookup"><span data-stu-id="04245-124">To filter the results by specific role groups, click **Select role groups**.</span></span> <span data-ttu-id="04245-125">Dans la boîte de dialogue qui s’affiche, sélectionnez un groupe de rôles, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="04245-125">In the dialog that appears, select a role group and click **add ->**.</span></span> <span data-ttu-id="04245-126">Répétez cette étape autant de fois que nécessaire, puis cliquez sur **OK** lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="04245-126">Repeat this step as many times as necessary, and then click **OK** when you're finished.</span></span>

3. <span data-ttu-id="04245-127">Lorsque vous avez terminé, cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="04245-127">When you're finished, click **Search**.</span></span>

<span data-ttu-id="04245-p108">Si des modifications correspondent aux critères que vous avez spécifiés, elles seront affichées dans le volet des résultats. Cliquez sur un groupe de rôles dans les résultats de la recherche pour afficher les modifications dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="04245-p108">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="04245-130">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="04245-130">How do you know this worked?</span></span>

<span data-ttu-id="04245-p109">Si vous avez bien exécuté un rapport de groupe de rôles d'administrateur, les groupes de rôles qui ont été modifiés dans la plage de dates s'affichent dans le volet des résultats de la recherche. En cas d'absence de résultats, cela signifie qu'aucune modification aux groupes de rôles n'a eu lieu dans la plage de dates indiquée. Si vous pensez que des résultats devraient apparaître, modifiez la plage de dates et réexécutez le rapport.</span><span class="sxs-lookup"><span data-stu-id="04245-p109">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>

## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="04245-134">Surveillances des modifications apportées à l'appartenance à des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="04245-134">Monitor changes to role group membership</span></span>

<span data-ttu-id="04245-p110">Lorsque des membres sont ajoutés ou supprimés dans groupe de rôles, les résultats de la recherche affichés dans le volet d'informations indiquent que l'appartenance à un groupe de rôles a été mise à jour et répertorient les membres actuels. Les résultats n'indiquent pas explicitement quel utilisateur a été ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="04245-p110">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>

<span data-ttu-id="04245-p111">Pour déterminer si un utilisateur a été ajouté ou supprimé, vous devez comparer deux entrées séparées dans le rapport. Par exemple, examinons les entrées de journal suivantes pour le groupe de rôles **Support technique**:</span><span class="sxs-lookup"><span data-stu-id="04245-p111">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span>

> <span data-ttu-id="04245-139">1/27/2018 4:43 PM</span><span class="sxs-lookup"><span data-stu-id="04245-139">1/27/2018 4:43 PM</span></span> <br> <span data-ttu-id="04245-140">Administrateur</span><span class="sxs-lookup"><span data-stu-id="04245-140">Administrator</span></span> <br> <span data-ttu-id="04245-141">Membres mis à jour : Administrateur;annb,florencef;pilarp</span><span class="sxs-lookup"><span data-stu-id="04245-141">Updated members: Administrator;annb,florencef;pilarp</span></span> <br> <span data-ttu-id="04245-142">2/06/2018 10:09 AM</span><span class="sxs-lookup"><span data-stu-id="04245-142">2/06/2018 10:09 AM</span></span> <br> <span data-ttu-id="04245-143">Administrateur</span><span class="sxs-lookup"><span data-stu-id="04245-143">Administrator</span></span> <br> <span data-ttu-id="04245-144">Membres mis à jour : Administrator;annb;florencef;pilarp;tonip</span><span class="sxs-lookup"><span data-stu-id="04245-144">Updated members: Administrator;annb;florencef;pilarp;tonip</span></span> <br> <span data-ttu-id="04245-145">2/19/2018 2:12 PM</span><span class="sxs-lookup"><span data-stu-id="04245-145">2/19/2018 2:12 PM</span></span> <br> <span data-ttu-id="04245-146">Administrateur</span><span class="sxs-lookup"><span data-stu-id="04245-146">Administrator</span></span> <br> <span data-ttu-id="04245-147">Membres mis à jour : Administrator;annb;florencef;tonip</span><span class="sxs-lookup"><span data-stu-id="04245-147">Updated members: Administrator;annb;florencef;tonip</span></span>

<span data-ttu-id="04245-148">Dans cet exemple, le compte d'utilisateur Administrateur a apporté les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="04245-148">In this example, the Administrator user account made the following changes:</span></span>

- <span data-ttu-id="04245-149">Le 2/06/2018, il a ajouté l’utilisateur tonip.</span><span class="sxs-lookup"><span data-stu-id="04245-149">On 2/06/2018, they added the user tonip.</span></span>
- <span data-ttu-id="04245-150">Le 2/19/2018, il a supprimé l’utilisateur pilarp.</span><span class="sxs-lookup"><span data-stu-id="04245-150">On 2/19/2018, they removed the user pilarp.</span></span>

## <a name="use-standalone-exchange-online-powershell-to-search-for-audit-log-entries"></a><span data-ttu-id="04245-151">Utiliser Exchange Online PowerShell autonome pour rechercher des entrées du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="04245-151">Use standalone Exchange Online PowerShell to search for audit log entries</span></span>

<span data-ttu-id="04245-152">Vous pouvez utiliser Exchange Online PowerShell pour rechercher des entrées du journal d’audit qui correspondent aux critères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="04245-152">You can use Exchange Online PowerShell to search for audit log entries that meet the criteria you specify.</span></span> <span data-ttu-id="04245-153">Pour obtenir la liste des critères de recherche, voir [Search-AdminAuditLog Search Criteria](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#search-adminauditlog-cmdlet).</span><span class="sxs-lookup"><span data-stu-id="04245-153">For a list of search criteria, see [Search-AdminAuditLog search criteria](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#search-adminauditlog-cmdlet).</span></span> <span data-ttu-id="04245-154">Cette procédure utilise la cmdlet **Search-AdminAuditLog** et affiche les résultats de la recherche dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04245-154">This procedure uses the **Search-AdminAuditLog** cmdlet and displays search results in Exchange Online PowerShell.</span></span> <span data-ttu-id="04245-155">Vous pouvez utiliser cette cmdlet si vous devez renvoyer un ensemble de résultats au-delà des limites définies dans la cmdlet **New-AdminAuditLogSearch** ou dans les rapports d'audit du Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="04245-155">You can use this cmdlet when you need to return a set of results that exceeds the limits defined on the **New-AdminAuditLogSearch** cmdlet or in the EAC Audit Reporting reports.</span></span>

<span data-ttu-id="04245-156">Pour effectuer une recherche dans le journal d'audit d'après les critères que vous avez définis, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="04245-156">To search the audit log for criteria you specify, use the following syntax.</span></span>

```PowerShell
Search-AdminAuditLog - Cmdlets <cmdlet 1, cmdlet 2, ...> -Parameters <parameter 1, parameter 2, ...> -StartDate <start date> -EndDate <end date> -UserIds <user IDs> -ObjectIds <object IDs> -IsSuccess <$True | $False >
```

> [!NOTE]
> <span data-ttu-id="04245-157">Par défaut, la cmdlet **Search-AdminAuditLog** renvoie un maximum de 1 000 entrées du journal.</span><span class="sxs-lookup"><span data-stu-id="04245-157">The **Search-AdminAuditLog** cmdlet returns a maximum of 1,000 log entries by default.</span></span> <span data-ttu-id="04245-158">Utilisez le paramètre _result_ pour spécifier jusqu’à 250 000 entrées de journal.</span><span class="sxs-lookup"><span data-stu-id="04245-158">Use the _ResultSize_ parameter to specify up to 250,000 log entries.</span></span> <span data-ttu-id="04245-159">Vous pouvez utiliser la valeur `Unlimited` pour renvoyer toutes les entrées.</span><span class="sxs-lookup"><span data-stu-id="04245-159">Or, use the value `Unlimited` to return all entries.</span></span>

<span data-ttu-id="04245-160">Cet exemple effectue une recherche portant sur toutes les entrées du journal d'audit avec les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="04245-160">This example performs a search for all audit log entries with the following criteria:</span></span>

- <span data-ttu-id="04245-161">**Date de début**: 08/04/2018</span><span class="sxs-lookup"><span data-stu-id="04245-161">**Start date**: 08/04/2018</span></span>
- <span data-ttu-id="04245-162">**Date de fin**: 10/03/2018</span><span class="sxs-lookup"><span data-stu-id="04245-162">**End date**: 10/03/2018</span></span>
- <span data-ttu-id="04245-163">**ID d’utilisateur**: `davids` , `chrisd` , `kima`</span><span class="sxs-lookup"><span data-stu-id="04245-163">**User IDs**: `davids`, `chrisd`, `kima`</span></span>
- <span data-ttu-id="04245-164">**Cmdlets**: **Set-Mailbox**</span><span class="sxs-lookup"><span data-stu-id="04245-164">**Cmdlets**: **Set-Mailbox**</span></span>
- <span data-ttu-id="04245-165">**Paramètres**: _ProhibitSendQuota_, _ProhibitSendReceiveQuota_, _IssueWarningQuota_, _MaxSendSize_, _MaxReceiveSize_</span><span class="sxs-lookup"><span data-stu-id="04245-165">**Parameters**: _ProhibitSendQuota_, _ProhibitSendReceiveQuota_, _IssueWarningQuota_, _MaxSendSize_, _MaxReceiveSize_</span></span>

```PowerShell
Search-AdminAuditLog -Cmdlets Set-Mailbox -Parameters ProhibitSendQuota,ProhibitSendReceiveQuota,IssueWarningQuota,MaxSendSize,MaxReceiveSize -StartDate 08/04/2018 -EndDate 10/03/2018 -UserIds davids,chrisd,kima
```

<span data-ttu-id="04245-p114">Cet exemple recherche les modifications apportées à une boîte aux lettres spécifique. Ceci est utile si vous effectuez des opérations de dépannage ou devez fournir des informations à des fins d'investigation. Les critères suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="04245-p114">This example searches for changes made to a specific mailbox. This is useful if you're troubleshooting or you need to provide information for an investigation. The following criteria are used:</span></span>

- <span data-ttu-id="04245-169">**Date de début**: 05/01/2018</span><span class="sxs-lookup"><span data-stu-id="04245-169">**Start date**: 05/01/2018</span></span>
- <span data-ttu-id="04245-170">**Date de fin**: 10/03/2018</span><span class="sxs-lookup"><span data-stu-id="04245-170">**End date**: 10/03/2018</span></span>
- <span data-ttu-id="04245-171">**ID d’objet**: contoso.com/users/Davids</span><span class="sxs-lookup"><span data-stu-id="04245-171">**Object ID**: contoso.com/Users/DavidS</span></span>

```PowerShell
Search-AdminAuditLog -StartDate 05/01/2018 -EndDate 10/03/2018 -ObjectID contoso.com/Users/DavidS
```

<span data-ttu-id="04245-172">Si vos recherches renvoient de nombreuses entrées de journal, nous vous recommandons d’utiliser la procédure décrite dans la rubrique **utiliser Exchange Online PowerShell pour rechercher des entrées du journal d’audit et envoyer les résultats à un destinataire** plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="04245-172">If your searches return many log entries, we recommend that you use the procedure provided in **Use Exchange Online PowerShell to search for audit log entries and send results to a recipient** later in this article.</span></span> <span data-ttu-id="04245-173">La procédure décrite dans cette section a pour objet d'envoyer aux destinataires que vous spécifiez un fichier XML sous forme de pièce jointe à un message électronique, ce qui vous permet d'extraire plus aisément les données qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="04245-173">The procedure in that section sends an XML file as an email attachment to the recipients you specify, enabling you to more easily extract the data you're interested in.</span></span>

<span data-ttu-id="04245-174">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-adminauditlog).</span><span class="sxs-lookup"><span data-stu-id="04245-174">For detailed syntax and parameter information, see [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-adminauditlog).</span></span>

### <a name="view-details-of-audit-log-entries"></a><span data-ttu-id="04245-175">Afficher le détail des entrées du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="04245-175">View details of audit log entries</span></span>

<span data-ttu-id="04245-176">L’applet de commande **Search-AdminAuditLog** renvoie les champs décrits dans le [contenu du journal d’audit](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#audit-log-contents).</span><span class="sxs-lookup"><span data-stu-id="04245-176">The **Search-AdminAuditLog** cmdlet returns the fields described in [Audit log contents](https://docs.microsoft.com/Exchange/policy-and-compliance/admin-audit-logging/admin-audit-logging#audit-log-contents).</span></span> <span data-ttu-id="04245-177">Parmi les champs renvoyés par la cmdlet, deux champs ( **CmdletParameters** et **ModifiedProperties** ) comportent des données supplémentaires qu'il est impossible de visualiser par défaut.</span><span class="sxs-lookup"><span data-stu-id="04245-177">Of the fields returned by the cmdlet, two fields, **CmdletParameters** and **ModifiedProperties**, contain additional information that isn't viewable by default.</span></span>

<span data-ttu-id="04245-178">Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties**, suivez la procédure ci-après.</span><span class="sxs-lookup"><span data-stu-id="04245-178">To view the contents of the **CmdletParameters** and **ModifiedProperties** fields, use the following steps.</span></span> <span data-ttu-id="04245-179">Vous pouvez utiliser la procédure décrite dans **utiliser Exchange Online PowerShell pour rechercher des entrées du journal d’audit et envoyer des résultats à un destinataire** plus loin dans cet article pour créer un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="04245-179">Or, you can use the procedure in **Use Exchange Online PowerShell to search for audit log entries and send results to a recipient** later in this article to create an XML file.</span></span>

<span data-ttu-id="04245-180">Cette procédure exploite les concepts suivants :</span><span class="sxs-lookup"><span data-stu-id="04245-180">This procedure uses the following concepts:</span></span>

- [<span data-ttu-id="04245-181">about_Arrays</span><span class="sxs-lookup"><span data-stu-id="04245-181">about_Arrays</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_arrays)

- [<span data-ttu-id="04245-182">about_Variables</span><span class="sxs-lookup"><span data-stu-id="04245-182">about_Variables</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_variables)

1. <span data-ttu-id="04245-183">Déterminez les critères sur lesquels doivent porter vos recherches, exécutez la cmdlet **Search-AdminAuditLog** et stockez les résultats dans une variable au moyen de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="04245-183">Decide the criteria you want to search for, run the **Search-AdminAuditLog** cmdlet, and store the results in a variable using the following command.</span></span>

   ```PowerShell
   $Results = Search-AdminAuditLog <search criteria>
   ```

2. <span data-ttu-id="04245-184">Chaque entrée du journal d’audit est stockée sous la forme d’un élément de tableau dans la variable `$Results` .</span><span class="sxs-lookup"><span data-stu-id="04245-184">Each audit log entry is stored as an array element in the variable `$Results`.</span></span> <span data-ttu-id="04245-185">Vous pouvez sélectionner un élément de tableau en précisant son index.</span><span class="sxs-lookup"><span data-stu-id="04245-185">You can select an array element by specifying its array element index.</span></span> <span data-ttu-id="04245-186">Les index des éléments de tableau commencent à zéro (0) pour le premier élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="04245-186">Array element indexes start at zero (0) for the first array element.</span></span> <span data-ttu-id="04245-187">Par exemple, pour extraire le cinquième élément de tableau dont l'index est 4, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="04245-187">For example, to retrieve the 5th array element, which has an index of 4, use the following command.</span></span>

   ```PowerShell
   $Results[4]
   ```

3. <span data-ttu-id="04245-p119">La commande précédente renvoie l'entrée du journal stockée dans l'élément de tableau 4. Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties** pour cette entrée du journal, utilisez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="04245-p119">The previous command returns the log entry stored in array element 4. To see the contents of the **CmdletParameters** and **ModifiedProperties** fields for this log entry, use the following commands.</span></span>

   ```PowerShell
   $Results[4].CmdletParameters
   $Results[4].ModifiedProperties
   ```

4. <span data-ttu-id="04245-190">Pour afficher le contenu des champs **CmdletParameters** ou **ModifiedParameters** dans une autre entrée du journal, modifiez l'index de l'élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="04245-190">To view the contents of the **CmdletParameters** or **ModifiedParameters** fields in another log entry, change the array element index.</span></span>
