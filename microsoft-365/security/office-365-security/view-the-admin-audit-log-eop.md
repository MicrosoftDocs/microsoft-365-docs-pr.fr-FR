---
title: Afficher le journal d’audit de l’administrateur dans EOP autonome
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 003d7a74-3e16-4453-ae0c-9dbae51f66d1
description: Les administrateurs peuvent apprendre à afficher et effectuer des recherches dans le journal d’audit de l’administrateur dans Exchange Online Protection (EOP) autonome.
ms.openlocfilehash: e8c12f622c4dc382b11d03424e45c33e3afe3cbf
ms.sourcegitcommit: 73b2426001dc5a3f4b857366ef51e877db549098
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2020
ms.locfileid: "44613323"
---
# <a name="view-the-admin-audit-log-in-standalone-eop"></a><span data-ttu-id="58598-103">Afficher le journal d’audit de l’administrateur dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="58598-103">View the admin audit log in standalone EOP</span></span>

<span data-ttu-id="58598-104">Dans les organisations Exchange Online (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez utiliser le centre d’administration Exchange ou le PowerShell autonome EOP pour rechercher et afficher des entrées dans le journal d’audit de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="58598-104">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can use the Exchange admin center (EAC) or standalone EOP PowerShell to search for and view entries in the admin audit log.</span></span>

<span data-ttu-id="58598-105">Le journal d’audit de l’administrateur enregistre des actions spécifiques, basées sur des applets de commande autonomes EOP PowerShell, effectuées par les administrateurs et les utilisateurs disposant de privilèges d’administration.</span><span class="sxs-lookup"><span data-stu-id="58598-105">The admin audit log records specific actions, based on standalone EOP PowerShell cmdlets, done by admins and users who have been assigned administrative privileges.</span></span> <span data-ttu-id="58598-106">Les entrées du journal d’audit de l’administrateur vous fournissent des informations sur la cmdlet qui a été exécutée, les paramètres utilisés, l’utilisateur qui a exécuté la cmdlet et les objets affectés.</span><span class="sxs-lookup"><span data-stu-id="58598-106">Entries in the admin audit log provide you with information about what cmdlet was run, which parameters were used, who ran the cmdlet, and what objects were affected.</span></span>

> [!NOTE]
> <ul><li><span data-ttu-id="58598-107">La journalisation d’audit de l’administrateur est activée par défaut et vous ne pouvez pas la désactiver.</span><span class="sxs-lookup"><span data-stu-id="58598-107">Admin auditing logging is enabled by default, and you can't disable it.</span></span></li><li><span data-ttu-id="58598-108">Le journal d’audit de l’administrateur n’enregistre pas les actions basées sur les cmdlets qui commencent par les verbes **Get**, **Search**ou **test**.</span><span class="sxs-lookup"><span data-stu-id="58598-108">The admin audit log doesn't record actions based on cmdlets that begins with the verbs **Get**, **Search**, or **Test**.</span></span></li><li><span data-ttu-id="58598-109">Les entrées du journal d'audit sont conservées pendant 90 jours.</span><span class="sxs-lookup"><span data-stu-id="58598-109">Audit log entries are kept for 90 days.</span></span> <span data-ttu-id="58598-110">Lorsqu’une entrée est antérieure à 90 jours, elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="58598-110">When an entry is older than 90 days, it's deleted</span></span></li></ul>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="58598-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="58598-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="58598-112">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="58598-112">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="58598-113">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="58598-113">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="58598-114">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="58598-114">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="58598-115">Plus précisément, vous avez besoin du rôle journaux d’audit ou journaux d’audit en affichage seul, qui sont attribués aux groupes de rôles ComplianceManagement, OrganizationManagement (administrateurs globaux) et SecurityAdministrator par défaut.</span><span class="sxs-lookup"><span data-stu-id="58598-115">Specifically, you need the Audit Logs or View-Only Audit Logs role, which are assigned to the ComplianceManagement, OrganizationManagement (global admins), and SecurityAdministrator role groups by default.</span></span> <span data-ttu-id="58598-116">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="58598-116">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="58598-117">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="58598-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="58598-118">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="58598-118">Having problems?</span></span> <span data-ttu-id="58598-119">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="58598-119">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-eac-to-view-the-admin-audit-log"></a><span data-ttu-id="58598-120">Utiliser le centre d’administration Exchange pour afficher le journal d’audit de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="58598-120">Use the EAC to view the admin audit log</span></span>

1. <span data-ttu-id="58598-121">Dans le centre d’administration Exchange, accédez à audit de **gestion de la conformité** \> **Auditing**, puis choisissez **exécuter le rapport du journal d’audit de l’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="58598-121">In the EAC, go to **Compliance management** \> **Auditing**, and then choose **Run the admin audit log report**.</span></span>

2. <span data-ttu-id="58598-122">Dans la page **Rechercher les modifications apportées aux groupes de rôles d’administrateur** qui s’ouvre, choisissez une **Date de début** et une date de **fin** (la plage par défaut est les deux dernières semaines), puis choisissez **recherche**.</span><span class="sxs-lookup"><span data-stu-id="58598-122">In the **Search for changes to administrator role groups** page that opens, choose a **Start date** and **End date** (the default range is the past two weeks), and then choose **Search**.</span></span> <span data-ttu-id="58598-123">Toutes les modifications de configuration effectuées pendant la période spécifiée sont affichées et peuvent être triées, avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="58598-123">All configuration changes made during the specified time period are displayed, and can be sorted, using the following information:</span></span>

   - <span data-ttu-id="58598-124">**Date**: date et heure de la modification de la configuration.</span><span class="sxs-lookup"><span data-stu-id="58598-124">**Date**: The date and time that the configuration change was made.</span></span> <span data-ttu-id="58598-125">La date et l'heure sont enregistrées au format temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="58598-125">The date and time are stored in Coordinated Universal Time (UTC) format.</span></span>

   - <span data-ttu-id="58598-126">**Cmdlet**: nom de la cmdlet qui a été utilisée pour la modification de la configuration.</span><span class="sxs-lookup"><span data-stu-id="58598-126">**Cmdlet**: The name of the cmdlet that was used to make the configuration change.</span></span>

   - <span data-ttu-id="58598-127">**User**: nom du compte d’utilisateur de l’utilisateur qui a effectué la modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="58598-127">**User**: The name of the user account of the user who made the configuration change.</span></span>

     <span data-ttu-id="58598-p107">Jusqu'à 5 000 entrées s'affichent sur plusieurs pages. Si vous devez affiner vos résultats, spécifiez une plage de dates plus courte. Si vous sélectionnez un seul résultat de recherche, l'information supplémentaire suivante s'affiche dans le volet de détails :</span><span class="sxs-lookup"><span data-stu-id="58598-p107">Up to 5000 entries will be displayed on multiple pages. Specify a smaller date range if you need to narrow your results. If you select an individual search result, the following additional information is displayed in the details pane:</span></span>

   - <span data-ttu-id="58598-131">**Objet modifié**: objet qui a été modifié par la cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58598-131">**Object modified**: The object that was modified by the cmdlet.</span></span>

   - <span data-ttu-id="58598-132">**Parameters (paramètre : valeur)**: paramètres de l’applet de commande qui ont été utilisés et n’importe quelle valeur spécifiée avec le paramètre.</span><span class="sxs-lookup"><span data-stu-id="58598-132">**Parameters (Parameter:Value)**: The cmdlet parameters that were used, and any value specified with the parameter.</span></span>

3. <span data-ttu-id="58598-133">Si vous souhaitez imprimer une entrée du journal d'audit spécifique, choisissez le bouton **Imprimer** dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="58598-133">If you want to print a specific audit log entry, choose the **Print** button in the details pane.</span></span>

## <a name="use-standalone-eop-powershell-to-view-the-admin-audit-log"></a><span data-ttu-id="58598-134">Utilisation d’EOP PowerShell autonome pour afficher le journal d’audit de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="58598-134">Use standalone EOP PowerShell to view the admin audit log</span></span>

<span data-ttu-id="58598-135">Vous pouvez utiliser la version autonome d’EOP PowerShell pour rechercher des entrées du journal d’audit correspondant aux critères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="58598-135">You can use standalone EOP PowerShell to search for audit log entries that meet the criteria you specify.</span></span> <span data-ttu-id="58598-136">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="58598-136">Use the following syntax:</span></span>

```PowerShell
Search-AdminAuditLog [-Cmdlets <Cmdlet1,Cmdlet2,...CmdletN>] [-Parameters <Parameter1,Parameter2,...ParameterN>] [-StartDate <UTCDateTime>] [-EndDate <UTCDateTime>] [-UserIds <"User1","User2",..."UserN">] [-ObjectIds <"Object1","Object2",..."ObjectN">] [-IsSuccess <$true | $false>]
```

<span data-ttu-id="58598-137">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="58598-137">**Notes**:</span></span>

- <span data-ttu-id="58598-138">Vous ne pouvez utiliser le paramètre _Parameters_ qu’avec le paramètre _cmdlets_ .</span><span class="sxs-lookup"><span data-stu-id="58598-138">You can only use the _Parameters_ parameter together with the _Cmdlets_ parameter.</span></span>

- <span data-ttu-id="58598-139">Le paramètre _ObjectID_ filtre les résultats par l’objet qui a été modifié par la cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58598-139">The _ObjectIds_ parameter filters the results by the object that was modified by the cmdlet.</span></span> <span data-ttu-id="58598-140">Une valeur valide dépend de la façon dont l’objet est représenté dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="58598-140">A valid value depends on how the object is represented in the audit log.</span></span> <span data-ttu-id="58598-141">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="58598-141">For example:</span></span>

  - <span data-ttu-id="58598-142">Nom</span><span class="sxs-lookup"><span data-stu-id="58598-142">Name</span></span>
  - <span data-ttu-id="58598-143">Nom unique canonique (par exemple, contoso.com/Users/Akia al-Zuhairi)</span><span class="sxs-lookup"><span data-stu-id="58598-143">Canonical distinguished name (for example, contoso.com/Users/Akia Al-Zuhairi)</span></span>

  <span data-ttu-id="58598-144">Vous devrez probablement utiliser d’autres paramètres de filtrage sur cette cmdlet pour affiner les résultats et identifier les types d’objets qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="58598-144">You'll likely need to use other filtering parameters on this cmdlet to narrow down the results and identify the types of objects that you're interested in.</span></span>

- <span data-ttu-id="58598-145">Le paramètre _userids_ filtre les résultats par l’utilisateur qui a effectué la modification (qui a exécuté l’applet de commande).</span><span class="sxs-lookup"><span data-stu-id="58598-145">The _UserIds_ parameter filters the results by the user who made the change (who ran the cmdlet).</span></span>

- <span data-ttu-id="58598-146">Pour les paramètres _StartDate_ et _EndDate_ , si vous spécifiez une valeur de date/heure sans fuseau horaire, la valeur est au format UTC (temps universel coordonné).</span><span class="sxs-lookup"><span data-stu-id="58598-146">For the _StartDate_ and _EndDate_ parameters, if you specify a date/time value without a time zone, the value is in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="58598-147">Pour spécifier une valeur date/heure pour ce paramètre, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="58598-147">To specify a date/time value for this parameter, use either of the following options:</span></span>

  - <span data-ttu-id="58598-148">Spécifier la valeur de date/heure au format UTC : par exemple, "06/05/2016 14:30:00z".</span><span class="sxs-lookup"><span data-stu-id="58598-148">Specify the date/time value in UTC: For example, "2016-05-06 14:30:00z".</span></span>

  - <span data-ttu-id="58598-149">Spécifiez la valeur date/heure sous la forme d’une formule qui convertit la date/l’heure de votre fuseau horaire local en heure UTC : par exemple, `(Get-Date "5/6/2016 9:30 AM").ToUniversalTime()` .</span><span class="sxs-lookup"><span data-stu-id="58598-149">Specify the date/time value as a formula that converts the date/time in your local time zone to UTC: For example, `(Get-Date "5/6/2016 9:30 AM").ToUniversalTime()`.</span></span> <span data-ttu-id="58598-150">Pour plus d’informations, consultez [Get-Date](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-date).</span><span class="sxs-lookup"><span data-stu-id="58598-150">For more information, see [Get-Date](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-date).</span></span>

- <span data-ttu-id="58598-151">L’applet de commande renvoie un maximum de 1 000 entrées de journal par défaut.</span><span class="sxs-lookup"><span data-stu-id="58598-151">The cmdlet returns a maximum of 1,000 log entries by default.</span></span> <span data-ttu-id="58598-152">Utilisez le paramètre _result_ pour spécifier jusqu’à 250 000 entrées de journal.</span><span class="sxs-lookup"><span data-stu-id="58598-152">Use the _ResultSize_ parameter to specify up to 250,000 log entries.</span></span> <span data-ttu-id="58598-153">Vous pouvez utiliser la valeur `Unlimited` pour renvoyer toutes les entrées.</span><span class="sxs-lookup"><span data-stu-id="58598-153">Or, use the value `Unlimited` to return all entries.</span></span>

<span data-ttu-id="58598-154">Cet exemple effectue une recherche portant sur toutes les entrées du journal d'audit avec les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="58598-154">This example performs a search for all audit log entries with the following criteria:</span></span>

- <span data-ttu-id="58598-155">**Date de début**: 4 août 2019</span><span class="sxs-lookup"><span data-stu-id="58598-155">**Start date**: August 4, 2019</span></span>
- <span data-ttu-id="58598-156">**Date de fin**: 3 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="58598-156">**End date**: October 3, 2019</span></span>
- <span data-ttu-id="58598-157">**Cmdlets**: Update-RoleGroupMember</span><span class="sxs-lookup"><span data-stu-id="58598-157">**Cmdlets**: Update-RoleGroupMember</span></span>

```PowerShell
Search-AdminAuditLog -Cmdlets Update-RoleGroupMember -StartDate (Get-Date "08/04/2019").ToUniversalTime() -EndDate (Get-Date "10/03/2019").ToUniversalTime()
```

<span data-ttu-id="58598-158">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-adminauditlog).</span><span class="sxs-lookup"><span data-stu-id="58598-158">For detailed syntax and parameter information, see [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/search-adminauditlog).</span></span>

### <a name="view-details-of-audit-log-entries"></a><span data-ttu-id="58598-159">Afficher le détail des entrées du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="58598-159">View details of audit log entries</span></span>

<span data-ttu-id="58598-160">L’applet de commande **Search-AdminAuditLog** renvoie les champs décrits dans la section [contenu du journal d’audit](#audit-log-contents) , plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="58598-160">The **Search-AdminAuditLog** cmdlet returns the fields described in the [Audit log contents](#audit-log-contents) section later in this topic.</span></span> <span data-ttu-id="58598-161">Parmi les champs renvoyés par l’applet de commande, deux champs, **CmdletParameters** et **ModifiedProperties**, contiennent des informations supplémentaires qui ne sont pas renvoyées par défaut.</span><span class="sxs-lookup"><span data-stu-id="58598-161">Of the fields returned by the cmdlet, two fields, **CmdletParameters** and **ModifiedProperties**, contain additional information that isn't returned by default.</span></span>

<span data-ttu-id="58598-162">Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties**, suivez la procédure ci-après.</span><span class="sxs-lookup"><span data-stu-id="58598-162">To view the contents of the **CmdletParameters** and **ModifiedProperties** fields, use the following steps.</span></span>

1. <span data-ttu-id="58598-163">Déterminez les critères sur lesquels doivent porter vos recherches, exécutez la cmdlet **Search-AdminAuditLog** et stockez les résultats dans une variable au moyen de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="58598-163">Decide the criteria you want to search for, run the **Search-AdminAuditLog** cmdlet, and store the results in a variable using the following command.</span></span>

    ```PowerShell
    $Results = Search-AdminAuditLog <search criteria>
    ```

2. <span data-ttu-id="58598-164">Chaque entrée du journal d’audit est stockée sous la forme d’un élément de tableau dans la variable `$Results` .</span><span class="sxs-lookup"><span data-stu-id="58598-164">Each audit log entry is stored as an array element in the variable `$Results`.</span></span> <span data-ttu-id="58598-165">Vous pouvez sélectionner un élément de tableau en précisant son index.</span><span class="sxs-lookup"><span data-stu-id="58598-165">You can select an array element by specifying its array element index.</span></span> <span data-ttu-id="58598-166">Les index des éléments de tableau commencent à zéro (0) pour le premier élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="58598-166">Array element indexes start at zero (0) for the first array element.</span></span> <span data-ttu-id="58598-167">Par exemple, pour extraire le cinquième élément de tableau dont l'index est 4, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="58598-167">For example, to retrieve the 5th array element, which has an index of 4, use the following command.</span></span>

    ```PowerShell
    $Results[4]
    ```

3. <span data-ttu-id="58598-p115">La commande précédente renvoie l'entrée du journal stockée dans l'élément de tableau 4. Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties** pour cette entrée du journal, utilisez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="58598-p115">The previous command returns the log entry stored in array element 4. To see the contents of the **CmdletParameters** and **ModifiedProperties** fields for this log entry, use the following commands.</span></span>

    ```PowerShell
    $Results[4].CmdletParameters
    $Results[4].ModifiedProperties
    ```

4. <span data-ttu-id="58598-170">Pour afficher le contenu des champs **CmdletParameters** ou **ModifiedParameters** dans une autre entrée du journal, modifiez l'index de l'élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="58598-170">To view the contents of the **CmdletParameters** or **ModifiedParameters** fields in another log entry, change the array element index.</span></span>

## <a name="audit-log-contents"></a><span data-ttu-id="58598-171">Contenu des journaux d'audit</span><span class="sxs-lookup"><span data-stu-id="58598-171">Audit log contents</span></span>

<span data-ttu-id="58598-172">Chaque entrée du journal d’audit contient les informations décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="58598-172">Each audit log entry contains the information described in the following table.</span></span> <span data-ttu-id="58598-173">Le journal d’audit contient une ou plusieurs entrées de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="58598-173">The audit log contains one or more audit log entries.</span></span>

|||
|---|---|
|<span data-ttu-id="58598-174">**Field**</span><span class="sxs-lookup"><span data-stu-id="58598-174">**Field**</span></span>|<span data-ttu-id="58598-175">**Description**</span><span class="sxs-lookup"><span data-stu-id="58598-175">**Description**</span></span>|
|`RunspaceId`|<span data-ttu-id="58598-176">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-176">This field is used internally by EOP.</span></span>|
|`ObjectModified`|<span data-ttu-id="58598-177">Ce champ contient l’objet qui a été modifié par la cmdlet spécifiée dans le `CmdletName` champ.</span><span class="sxs-lookup"><span data-stu-id="58598-177">This field contains the object that was modified by the cmdlet specified in the `CmdletName` field.</span></span>|
|`CmdletName`|<span data-ttu-id="58598-178">Ce champ contient le nom de la cmdlet exécutée par l’utilisateur dans le `Caller` champ.</span><span class="sxs-lookup"><span data-stu-id="58598-178">This field contains the name of the cmdlet that was run by the user in the `Caller` field.</span></span>|
|`CmdletParameters`|<span data-ttu-id="58598-179">Ce champ contient les paramètres qui ont été spécifiés lors de l’exécution de la cmdlet dans le `CmdletName` champ.</span><span class="sxs-lookup"><span data-stu-id="58598-179">This field contains the parameters that were specified when the cmdlet in the `CmdletName` field was run.</span></span> <span data-ttu-id="58598-180">La valeur spécifiée avec le paramètre est également stockée dans ce champ, mais invisible dans la sortie par défaut, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="58598-180">Also stored in this field, but not visible in the default output, is the value specified with the parameter, if any.</span></span>|
|`ModifiedProperties`|<span data-ttu-id="58598-181">Ce champ contient les propriétés qui ont été modifiées sur l’objet dans le `ObjectModified` champ.</span><span class="sxs-lookup"><span data-stu-id="58598-181">This field contains the properties that were modified on the object in the `ObjectModified` field.</span></span> <span data-ttu-id="58598-182">L’ancienne valeur de la propriété et la nouvelle valeur stockée sont également stockées dans ce champ, mais sont invisibles dans la sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="58598-182">Also stored in this field, but not visible in the default output, are the old value of the property and the new value that was stored.</span></span>|
|`Caller`|<span data-ttu-id="58598-183">Ce champ contient le compte d’utilisateur de l’utilisateur qui a exécuté la cmdlet dans le `CmdletName` champ.</span><span class="sxs-lookup"><span data-stu-id="58598-183">This field contains the user account of the user who ran the cmdlet in the `CmdletName` field.</span></span>|
|`ExternalAccess`|<span data-ttu-id="58598-184">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-184">This field is used internally by EOP.</span></span>|
|`Succeeded`|<span data-ttu-id="58598-185">Ce champ indique si la cmdlet dans le `CmdletName` champ a été exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="58598-185">This field specifies whether the cmdlet in the `CmdletName` field ran successfully.</span></span> <span data-ttu-id="58598-186">La valeur est soit `True` ou `False` .</span><span class="sxs-lookup"><span data-stu-id="58598-186">The value is either `True` or `False`.</span></span>|
|`Error`|<span data-ttu-id="58598-187">Ce champ contient le message d’erreur généré si l’exécution de la cmdlet dans le `CmdletName` champ a échoué.</span><span class="sxs-lookup"><span data-stu-id="58598-187">This field contains the error message generated if the cmdlet in the `CmdletName` field failed to complete successfully.</span></span>|
|`RunDate`|<span data-ttu-id="58598-188">Ce champ contient la date et l’heure d’exécution de la cmdlet dans le `CmdletName` champ.</span><span class="sxs-lookup"><span data-stu-id="58598-188">This field contains the date and time when the cmdlet in the `CmdletName` field was run.</span></span> <span data-ttu-id="58598-189">La date et l'heure sont enregistrées au format temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="58598-189">The date and time are stored in Coordinated Universal Time (UTC) format.</span></span>|
|`OriginatingServer`|<span data-ttu-id="58598-190">Ce champ indique le serveur sur lequel la cmdlet spécifiée dans le `CmdletName` champ a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="58598-190">This field indicates the server on which the cmdlet specified in the `CmdletName` field was run.</span></span>|
|`ClientIP`|<span data-ttu-id="58598-191">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-191">This field is used internally by EOP.</span></span>|
|`SessionId`|<span data-ttu-id="58598-192">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-192">This field is used internally by EOP.</span></span>|
|`AppId`|<span data-ttu-id="58598-193">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-193">This field is used internally by EOP.</span></span>|
|`ClientAppId`|<span data-ttu-id="58598-194">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-194">This field is used internally by EOP.</span></span>|
|`Identity`|<span data-ttu-id="58598-195">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-195">This field is used internally by EOP.</span></span>|
|`IsValid`|<span data-ttu-id="58598-196">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-196">This field is used internally by EOP.</span></span>|
|`ObjectState`|<span data-ttu-id="58598-197">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="58598-197">This field is used internally by EOP.</span></span>|
|
