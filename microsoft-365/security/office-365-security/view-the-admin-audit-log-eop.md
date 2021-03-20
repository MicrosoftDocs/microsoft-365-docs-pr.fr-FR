---
title: Afficher le journal d’audit de l’administrateur dans EOP autonome
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 003d7a74-3e16-4453-ae0c-9dbae51f66d1
description: Les administrateurs peuvent découvrir comment afficher et effectuer des recherches dans le journal d’audit de l’administrateur dans Exchange Online Protection (EOP) autonome.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 5ed1d1eb121c06e6f5727e8782ba1d8bc8d23a99
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50908125"
---
# <a name="view-the-admin-audit-log-in-standalone-eop"></a><span data-ttu-id="9e549-103">Afficher le journal d’audit de l’administrateur dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="9e549-103">View the admin audit log in standalone EOP</span></span>

<span data-ttu-id="9e549-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9e549-104">**Applies to**</span></span>
- [<span data-ttu-id="9e549-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="9e549-105">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="9e549-106">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez utiliser le Centre d’administration Exchange (CAE) ou EOP PowerShell autonome pour rechercher et afficher des entrées dans le journal d’audit de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="9e549-106">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can use the Exchange admin center (EAC) or standalone EOP PowerShell to search for and view entries in the admin audit log.</span></span>

<span data-ttu-id="9e549-107">Le journal d’audit de l’administrateur enregistre des actions spécifiques, basées sur des cmdlets EOP PowerShell autonomes, réalisées par les administrateurs et les utilisateurs qui se sont vus attribuer des privilèges d’administration.</span><span class="sxs-lookup"><span data-stu-id="9e549-107">The admin audit log records specific actions, based on standalone EOP PowerShell cmdlets, done by admins and users who have been assigned administrative privileges.</span></span> <span data-ttu-id="9e549-108">Les entrées du journal d’audit de l’administrateur vous fournissent des informations sur la cmdlet qui a été exécuté, les paramètres utilisés, l’utilisateur qui a exécuté la cmdlet et les objets affectés.</span><span class="sxs-lookup"><span data-stu-id="9e549-108">Entries in the admin audit log provide you with information about what cmdlet was run, which parameters were used, who ran the cmdlet, and what objects were affected.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="9e549-109">La journalisation d’audit de l’administrateur est activée par défaut et vous ne pouvez pas la désactiver.</span><span class="sxs-lookup"><span data-stu-id="9e549-109">Admin auditing logging is enabled by default, and you can't disable it.</span></span>
>
> - <span data-ttu-id="9e549-110">Le journal d’audit de l’administrateur n’enregistre pas les actions basées sur les cmdlets qui commencent par les verbes **Get,** **Search** ou **Test**.</span><span class="sxs-lookup"><span data-stu-id="9e549-110">The admin audit log doesn't record actions based on cmdlets that begins with the verbs **Get**, **Search**, or **Test**.</span></span>
>
> - <span data-ttu-id="9e549-111">Les entrées du journal d'audit sont conservées pendant 90 jours.</span><span class="sxs-lookup"><span data-stu-id="9e549-111">Audit log entries are kept for 90 days.</span></span> <span data-ttu-id="9e549-112">Lorsqu’une entrée est plus ancienne que 90 jours, elle est supprimée</span><span class="sxs-lookup"><span data-stu-id="9e549-112">When an entry is older than 90 days, it's deleted</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9e549-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9e549-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9e549-114">Pour ouvrir le Centre d’administration Exchange, consultez le [Centre d’administration Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="9e549-114">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="9e549-115">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="9e549-115">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="9e549-116">Des autorisations doivent vous être attribuées dans Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="9e549-116">You need to be assigned permissions in Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="9e549-117">Plus précisément, vous avez besoin du rôle Journaux  d’audit ou Journaux d’audit en affichage seul, qui sont affectés par défaut aux groupes de **rôles** Gestion de l’organisation, Gestion de la conformité et Administrateur de la sécurité.  </span><span class="sxs-lookup"><span data-stu-id="9e549-117">Specifically, you need the **Audit Logs** or **View-Only Audit Logs** role, which are assigned to the **Organization Management**, **Compliance Management**, and **Security Administrator** role groups by default.</span></span> <span data-ttu-id="9e549-118">Pour plus d’informations, voir Autorisations dans [EOP](feature-permissions-in-eop.md) autonome et utiliser le CAE pour modifier la liste des membres des [groupes de rôles.](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)</span><span class="sxs-lookup"><span data-stu-id="9e549-118">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="9e549-119">Pour plus d’informations sur les raccourcis clavier qui peuvent s’appliquer aux procédures de cet article, voir raccourcis clavier pour le Centre d’administration [Exchange dans Exchange Online.](/Exchange/accessibility/keyboard-shortcuts-in-admin-center)</span><span class="sxs-lookup"><span data-stu-id="9e549-119">For information about keyboard shortcuts that may apply to the procedures in this article, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="9e549-120">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="9e549-120">Having problems?</span></span> <span data-ttu-id="9e549-121">Demandez de l’aide dans le Forum [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) .</span><span class="sxs-lookup"><span data-stu-id="9e549-121">Ask for help in the [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) forum.</span></span>

## <a name="use-the-eac-to-view-the-admin-audit-log"></a><span data-ttu-id="9e549-122">Utiliser le EAC pour afficher le journal d’audit de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="9e549-122">Use the EAC to view the admin audit log</span></span>

1. <span data-ttu-id="9e549-123">Dans le EAC, sélectionnez **Audit** de la gestion de la conformité, puis exécutez le rapport du journal \>  **d’audit de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="9e549-123">In the EAC, go to **Compliance management** \> **Auditing**, and then choose **Run the admin audit log report**.</span></span>

2. <span data-ttu-id="9e549-124">Dans **la** page Rechercher les modifications apportées aux groupes de rôles d’administrateur qui s’ouvre, choisissez une **date** de début et une **date** de fin (la plage par défaut est les deux dernières semaines), puis choisissez **Rechercher.**</span><span class="sxs-lookup"><span data-stu-id="9e549-124">In the **Search for changes to administrator role groups** page that opens, choose a **Start date** and **End date** (the default range is the past two weeks), and then choose **Search**.</span></span> <span data-ttu-id="9e549-125">Toutes les modifications de configuration effectuées pendant la période spécifiée sont affichées et peuvent être triées, avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e549-125">All configuration changes made during the specified time period are displayed, and can be sorted, using the following information:</span></span>

   - <span data-ttu-id="9e549-126">**Date**: date et heure de la modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="9e549-126">**Date**: The date and time that the configuration change was made.</span></span> <span data-ttu-id="9e549-127">La date et l'heure sont enregistrées au format temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="9e549-127">The date and time are stored in Coordinated Universal Time (UTC) format.</span></span>

   - <span data-ttu-id="9e549-128">**Cmdlet**: nom de la cmdlet utilisée pour modifier la configuration.</span><span class="sxs-lookup"><span data-stu-id="9e549-128">**Cmdlet**: The name of the cmdlet that was used to make the configuration change.</span></span>

   - <span data-ttu-id="9e549-129">**User**: nom du compte d’utilisateur de l’utilisateur qui a effectué la modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="9e549-129">**User**: The name of the user account of the user who made the configuration change.</span></span>

     <span data-ttu-id="9e549-p107">Jusqu'à 5 000 entrées s'affichent sur plusieurs pages. Si vous devez affiner vos résultats, spécifiez une plage de dates plus courte. Si vous sélectionnez un seul résultat de recherche, l'information supplémentaire suivante s'affiche dans le volet de détails :</span><span class="sxs-lookup"><span data-stu-id="9e549-p107">Up to 5000 entries will be displayed on multiple pages. Specify a smaller date range if you need to narrow your results. If you select an individual search result, the following additional information is displayed in the details pane:</span></span>

   - <span data-ttu-id="9e549-133">**Objet modifié**: objet modifié par l’cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e549-133">**Object modified**: The object that was modified by the cmdlet.</span></span>

   - <span data-ttu-id="9e549-134">**Parameters (Parameter:Value)**: paramètres de cmdlet utilisés et toute valeur spécifiée avec le paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e549-134">**Parameters (Parameter:Value)**: The cmdlet parameters that were used, and any value specified with the parameter.</span></span>

3. <span data-ttu-id="9e549-135">Si vous souhaitez imprimer une entrée du journal d'audit spécifique, choisissez le bouton **Imprimer** dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="9e549-135">If you want to print a specific audit log entry, choose the **Print** button in the details pane.</span></span>

## <a name="use-standalone-eop-powershell-to-view-the-admin-audit-log"></a><span data-ttu-id="9e549-136">Utiliser EOP PowerShell autonome pour afficher le journal d’audit de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="9e549-136">Use standalone EOP PowerShell to view the admin audit log</span></span>

<span data-ttu-id="9e549-137">Vous pouvez utiliser EOP PowerShell autonome pour rechercher des entrées de journal d’audit qui répondent aux critères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="9e549-137">You can use standalone EOP PowerShell to search for audit log entries that meet the criteria you specify.</span></span> <span data-ttu-id="9e549-138">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9e549-138">Use the following syntax:</span></span>

```PowerShell
Search-AdminAuditLog [-Cmdlets <Cmdlet1,Cmdlet2,...CmdletN>] [-Parameters <Parameter1,Parameter2,...ParameterN>] [-StartDate <UTCDateTime>] [-EndDate <UTCDateTime>] [-UserIds <"User1","User2",..."UserN">] [-ObjectIds <"Object1","Object2",..."ObjectN">] [-IsSuccess <$true | $false>]
```

<span data-ttu-id="9e549-139">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="9e549-139">**Notes**:</span></span>

- <span data-ttu-id="9e549-140">Vous pouvez uniquement utiliser _le paramètre Parameters_ avec le _paramètre Cmdlets._</span><span class="sxs-lookup"><span data-stu-id="9e549-140">You can only use the _Parameters_ parameter together with the _Cmdlets_ parameter.</span></span>

- <span data-ttu-id="9e549-141">Le _paramètre ObjectIds_ filtre les résultats en fonction de l’objet modifié par l’cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e549-141">The _ObjectIds_ parameter filters the results by the object that was modified by the cmdlet.</span></span> <span data-ttu-id="9e549-142">Une valeur valide dépend de la façon dont l’objet est représenté dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="9e549-142">A valid value depends on how the object is represented in the audit log.</span></span> <span data-ttu-id="9e549-143">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9e549-143">For example:</span></span>

  - <span data-ttu-id="9e549-144">Nom</span><span class="sxs-lookup"><span data-stu-id="9e549-144">Name</span></span>
  - <span data-ttu-id="9e549-145">Nom canonique (par exemple, contoso.com/Users/Akia Al-Zuhairi)</span><span class="sxs-lookup"><span data-stu-id="9e549-145">Canonical distinguished name (for example, contoso.com/Users/Akia Al-Zuhairi)</span></span>

  <span data-ttu-id="9e549-146">Vous devrez probablement utiliser d’autres paramètres de filtrage sur cette cmdlet pour affiner les résultats et identifier les types d’objets qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="9e549-146">You'll likely need to use other filtering parameters on this cmdlet to narrow down the results and identify the types of objects that you're interested in.</span></span>

- <span data-ttu-id="9e549-147">Le _paramètre UserIds_ filtre les résultats selon l’utilisateur qui a effectué la modification (qui a effectué la cmdlet).</span><span class="sxs-lookup"><span data-stu-id="9e549-147">The _UserIds_ parameter filters the results by the user who made the change (who ran the cmdlet).</span></span>

- <span data-ttu-id="9e549-148">Pour les _paramètres StartDate_ et _EndDate,_ si vous spécifiez une valeur de date/heure sans fuseau horaire, la valeur est au temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="9e549-148">For the _StartDate_ and _EndDate_ parameters, if you specify a date/time value without a time zone, the value is in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9e549-149">Pour spécifier une valeur date/heure pour ce paramètre, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e549-149">To specify a date/time value for this parameter, use either of the following options:</span></span>

  - <span data-ttu-id="9e549-150">Spécifier la valeur de date/heure au format UTC : par exemple, "06/05/2016 14:30:00z".</span><span class="sxs-lookup"><span data-stu-id="9e549-150">Specify the date/time value in UTC: For example, "2016-05-06 14:30:00z".</span></span>

  - <span data-ttu-id="9e549-151">Spécifiez la valeur date/heure en tant que formule qui convertit la date/l’heure dans votre fuseau horaire local en UTC : Par exemple, `(Get-Date "5/6/2016 9:30 AM").ToUniversalTime()` .</span><span class="sxs-lookup"><span data-stu-id="9e549-151">Specify the date/time value as a formula that converts the date/time in your local time zone to UTC: For example, `(Get-Date "5/6/2016 9:30 AM").ToUniversalTime()`.</span></span> <span data-ttu-id="9e549-152">Pour plus d’informations, consultez [Get-Date](/powershell/module/microsoft.powershell.utility/get-date).</span><span class="sxs-lookup"><span data-stu-id="9e549-152">For more information, see [Get-Date](/powershell/module/microsoft.powershell.utility/get-date).</span></span>

- <span data-ttu-id="9e549-153">La cmdlet renvoie un maximum de 1 000 entrées de journal par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e549-153">The cmdlet returns a maximum of 1,000 log entries by default.</span></span> <span data-ttu-id="9e549-154">Utilisez le _paramètre ResultSize_ pour spécifier jusqu’à 250 000 entrées de journal.</span><span class="sxs-lookup"><span data-stu-id="9e549-154">Use the _ResultSize_ parameter to specify up to 250,000 log entries.</span></span> <span data-ttu-id="9e549-155">Vous pouvez également utiliser la valeur `Unlimited` pour renvoyer toutes les entrées.</span><span class="sxs-lookup"><span data-stu-id="9e549-155">Or, use the value `Unlimited` to return all entries.</span></span>

<span data-ttu-id="9e549-156">Cet exemple effectue une recherche portant sur toutes les entrées du journal d'audit avec les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="9e549-156">This example performs a search for all audit log entries with the following criteria:</span></span>

- <span data-ttu-id="9e549-157">**Date de** début : 4 août 2019</span><span class="sxs-lookup"><span data-stu-id="9e549-157">**Start date**: August 4, 2019</span></span>
- <span data-ttu-id="9e549-158">**Date de** fin : 3 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="9e549-158">**End date**: October 3, 2019</span></span>
- <span data-ttu-id="9e549-159">**Cmdlets**: Update-RoleGroupMember</span><span class="sxs-lookup"><span data-stu-id="9e549-159">**Cmdlets**: Update-RoleGroupMember</span></span>

```PowerShell
Search-AdminAuditLog -Cmdlets Update-RoleGroupMember -StartDate (Get-Date "08/04/2019").ToUniversalTime() -EndDate (Get-Date "10/03/2019").ToUniversalTime()
```

<span data-ttu-id="9e549-160">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Search-AdminAuditLog](/powershell/module/exchange/search-adminauditlog).</span><span class="sxs-lookup"><span data-stu-id="9e549-160">For detailed syntax and parameter information, see [Search-AdminAuditLog](/powershell/module/exchange/search-adminauditlog).</span></span>

### <a name="view-details-of-audit-log-entries"></a><span data-ttu-id="9e549-161">Afficher le détail des entrées du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="9e549-161">View details of audit log entries</span></span>

<span data-ttu-id="9e549-162">La cmdlet **Search-AdminAuditLog** renvoie les champs décrits dans la section Contenu du journal [d’audit](#audit-log-contents) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9e549-162">The **Search-AdminAuditLog** cmdlet returns the fields described in the [Audit log contents](#audit-log-contents) section later in this article.</span></span> <span data-ttu-id="9e549-163">Des champs renvoyés par la cmdlet, deux champs, **CmdletParameters** et **ModifiedProperties,** contiennent des informations supplémentaires qui ne sont pas renvoyées par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e549-163">Of the fields returned by the cmdlet, two fields, **CmdletParameters** and **ModifiedProperties**, contain additional information that isn't returned by default.</span></span>

<span data-ttu-id="9e549-164">Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties**, suivez la procédure ci-après.</span><span class="sxs-lookup"><span data-stu-id="9e549-164">To view the contents of the **CmdletParameters** and **ModifiedProperties** fields, use the following steps.</span></span>

1. <span data-ttu-id="9e549-165">Déterminez les critères sur lesquels doivent porter vos recherches, exécutez la cmdlet **Search-AdminAuditLog** et stockez les résultats dans une variable au moyen de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9e549-165">Decide the criteria you want to search for, run the **Search-AdminAuditLog** cmdlet, and store the results in a variable using the following command.</span></span>

    ```PowerShell
    $Results = Search-AdminAuditLog <search criteria>
    ```

2. <span data-ttu-id="9e549-166">Chaque entrée du journal d’audit est stockée en tant qu’élément de tableau dans la `$Results` variable.</span><span class="sxs-lookup"><span data-stu-id="9e549-166">Each audit log entry is stored as an array element in the variable `$Results`.</span></span> <span data-ttu-id="9e549-167">Vous pouvez sélectionner un élément de tableau en précisant son index.</span><span class="sxs-lookup"><span data-stu-id="9e549-167">You can select an array element by specifying its array element index.</span></span> <span data-ttu-id="9e549-168">Les index des éléments de tableau commencent à zéro (0) pour le premier élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="9e549-168">Array element indexes start at zero (0) for the first array element.</span></span> <span data-ttu-id="9e549-169">Par exemple, pour extraire le cinquième élément de tableau dont l'index est 4, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9e549-169">For example, to retrieve the 5th array element, which has an index of 4, use the following command.</span></span>

    ```PowerShell
    $Results[4]
    ```

3. <span data-ttu-id="9e549-p115">La commande précédente renvoie l'entrée du journal stockée dans l'élément de tableau 4. Pour afficher le contenu des champs **CmdletParameters** et **ModifiedProperties** pour cette entrée du journal, utilisez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9e549-p115">The previous command returns the log entry stored in array element 4. To see the contents of the **CmdletParameters** and **ModifiedProperties** fields for this log entry, use the following commands.</span></span>

    ```PowerShell
    $Results[4].CmdletParameters
    $Results[4].ModifiedProperties
    ```

4. <span data-ttu-id="9e549-172">Pour afficher le contenu des champs **CmdletParameters** ou **ModifiedParameters** dans une autre entrée du journal, modifiez l'index de l'élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="9e549-172">To view the contents of the **CmdletParameters** or **ModifiedParameters** fields in another log entry, change the array element index.</span></span>

## <a name="audit-log-contents"></a><span data-ttu-id="9e549-173">Contenu des journaux d'audit</span><span class="sxs-lookup"><span data-stu-id="9e549-173">Audit log contents</span></span>

<span data-ttu-id="9e549-174">Chaque entrée du journal d’audit contient les informations décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9e549-174">Each audit log entry contains the information described in the following table.</span></span> <span data-ttu-id="9e549-175">Le journal d’audit contient une ou plusieurs entrées de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="9e549-175">The audit log contains one or more audit log entries.</span></span>

****

|<span data-ttu-id="9e549-176">Champ</span><span class="sxs-lookup"><span data-stu-id="9e549-176">Field</span></span>|<span data-ttu-id="9e549-177">Description</span><span class="sxs-lookup"><span data-stu-id="9e549-177">Description</span></span>|
|---|---|
|`RunspaceId`|<span data-ttu-id="9e549-178">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-178">This field is used internally by EOP.</span></span>|
|`ObjectModified`|<span data-ttu-id="9e549-179">Ce champ contient l’objet modifié par la cmdlet spécifiée dans le `CmdletName` champ.</span><span class="sxs-lookup"><span data-stu-id="9e549-179">This field contains the object that was modified by the cmdlet specified in the `CmdletName` field.</span></span>|
|`CmdletName`|<span data-ttu-id="9e549-180">Ce champ contient le nom de la cmdlet qui a été exécuté par l’utilisateur dans le `Caller` champ.</span><span class="sxs-lookup"><span data-stu-id="9e549-180">This field contains the name of the cmdlet that was run by the user in the `Caller` field.</span></span>|
|`CmdletParameters`|<span data-ttu-id="9e549-181">Ce champ contient les paramètres qui ont été spécifiés lors de l’exécutement de la cmdlet `CmdletName` dans le champ.</span><span class="sxs-lookup"><span data-stu-id="9e549-181">This field contains the parameters that were specified when the cmdlet in the `CmdletName` field was run.</span></span> <span data-ttu-id="9e549-182">La valeur spécifiée avec le paramètre est également stockée dans ce champ, mais invisible dans la sortie par défaut, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9e549-182">Also stored in this field, but not visible in the default output, is the value specified with the parameter, if any.</span></span>|
|`ModifiedProperties`|<span data-ttu-id="9e549-183">Ce champ contient les propriétés qui ont été modifiées sur l’objet dans le `ObjectModified` champ.</span><span class="sxs-lookup"><span data-stu-id="9e549-183">This field contains the properties that were modified on the object in the `ObjectModified` field.</span></span> <span data-ttu-id="9e549-184">L’ancienne valeur de la propriété et la nouvelle valeur stockée sont également stockées dans ce champ, mais sont invisibles dans la sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e549-184">Also stored in this field, but not visible in the default output, are the old value of the property and the new value that was stored.</span></span>|
|`Caller`|<span data-ttu-id="9e549-185">Ce champ contient le compte d’utilisateur de l’utilisateur qui a dirigé la cmdlet dans le `CmdletName` champ.</span><span class="sxs-lookup"><span data-stu-id="9e549-185">This field contains the user account of the user who ran the cmdlet in the `CmdletName` field.</span></span>|
|`ExternalAccess`|<span data-ttu-id="9e549-186">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-186">This field is used internally by EOP.</span></span>|
|`Succeeded`|<span data-ttu-id="9e549-187">Ce champ spécifie si la cmdlet du champ `CmdletName` s’est correctement réussie.</span><span class="sxs-lookup"><span data-stu-id="9e549-187">This field specifies whether the cmdlet in the `CmdletName` field ran successfully.</span></span> <span data-ttu-id="9e549-188">La valeur est l’une `True` ou l’autre. `False`</span><span class="sxs-lookup"><span data-stu-id="9e549-188">The value is either `True` or `False`.</span></span>|
|`Error`|<span data-ttu-id="9e549-189">Ce champ contient le message d’erreur généré si la cmdlet dans le `CmdletName` champ n’a pas pu se terminer correctement.</span><span class="sxs-lookup"><span data-stu-id="9e549-189">This field contains the error message generated if the cmdlet in the `CmdletName` field failed to complete successfully.</span></span>|
|`RunDate`|<span data-ttu-id="9e549-190">Ce champ contient la date et l’heure d’exécuter la cmdlet dans `CmdletName` le champ.</span><span class="sxs-lookup"><span data-stu-id="9e549-190">This field contains the date and time when the cmdlet in the `CmdletName` field was run.</span></span> <span data-ttu-id="9e549-191">La date et l'heure sont enregistrées au format temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="9e549-191">The date and time are stored in Coordinated Universal Time (UTC) format.</span></span>|
|`OriginatingServer`|<span data-ttu-id="9e549-192">Ce champ indique le serveur sur lequel la cmdlet spécifiée dans `CmdletName` le champ a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="9e549-192">This field indicates the server on which the cmdlet specified in the `CmdletName` field was run.</span></span>|
|`ClientIP`|<span data-ttu-id="9e549-193">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-193">This field is used internally by EOP.</span></span>|
|`SessionId`|<span data-ttu-id="9e549-194">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-194">This field is used internally by EOP.</span></span>|
|`AppId`|<span data-ttu-id="9e549-195">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-195">This field is used internally by EOP.</span></span>|
|`ClientAppId`|<span data-ttu-id="9e549-196">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-196">This field is used internally by EOP.</span></span>|
|`Identity`|<span data-ttu-id="9e549-197">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-197">This field is used internally by EOP.</span></span>|
|`IsValid`|<span data-ttu-id="9e549-198">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-198">This field is used internally by EOP.</span></span>|
|`ObjectState`|<span data-ttu-id="9e549-199">Ce champ est utilisé en interne par EOP.</span><span class="sxs-lookup"><span data-stu-id="9e549-199">This field is used internally by EOP.</span></span>|
|