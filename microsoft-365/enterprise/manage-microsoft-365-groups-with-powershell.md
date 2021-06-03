---
title: Gérer Microsoft 365 groupes avec PowerShell
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
- BSA160
- BCS160
ms.assetid: aeb669aa-1770-4537-9de2-a82ac11b0540
description: Dans cet article, découvrez comment effectuer des tâches de gestion courantes pour Microsoft 365 groupes dans PowerShell.
ms.openlocfilehash: 22bf4d1f3187746483d8d904378e675562a62142
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730557"
---
# <a name="manage-microsoft-365-groups-with-powershell"></a><span data-ttu-id="bb83b-103">Gérer Microsoft 365 groupes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb83b-103">Manage Microsoft 365 Groups with PowerShell</span></span>

<span data-ttu-id="bb83b-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="bb83b-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="bb83b-105">Cet article décrit les étapes à suivre pour effectuer des tâches de gestion courantes pour les groupes dans Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb83b-105">This article provides the steps for doing common management tasks for Groups in Microsoft PowerShell.</span></span> <span data-ttu-id="bb83b-106">Il répertorie également les cmdlets PowerShell pour les groupes.</span><span class="sxs-lookup"><span data-stu-id="bb83b-106">It also lists the PowerShell cmdlets for Groups.</span></span> <span data-ttu-id="bb83b-107">Pour plus d’informations sur la gestion SharePoint sites web, voir [Gérer SharePoint sites en ligne à l’aide de PowerShell.](/sharepoint/manage-team-and-communication-sites-in-powershell)</span><span class="sxs-lookup"><span data-stu-id="bb83b-107">For info about managing SharePoint sites, see [Manage SharePoint Online sites using PowerShell](/sharepoint/manage-team-and-communication-sites-in-powershell).</span></span>

## <a name="link-to-your-microsoft-365-groups-usage-guidelines"></a><span data-ttu-id="bb83b-108">Lien vers vos recommandations Microsoft 365'utilisation des groupes de sécurité</span><span class="sxs-lookup"><span data-stu-id="bb83b-108">Link to your Microsoft 365 Groups usage guidelines</span></span>
<span data-ttu-id="bb83b-109"><a name="BK_LinkToGuideLines"> </a></span><span class="sxs-lookup"><span data-stu-id="bb83b-109"><a name="BK_LinkToGuideLines"> </a></span></span>

<span data-ttu-id="bb83b-110">Lorsque les [utilisateurs créent ou modifient](https://support.office.com/article/04d0c9cf-6864-423c-a380-4fa858f27102.aspx)un groupe dans Outlook, vous pouvez leur afficher un lien vers les instructions d’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bb83b-110">When users [create or edit a group in Outlook](https://support.office.com/article/04d0c9cf-6864-423c-a380-4fa858f27102.aspx), you can show them a link to your organization's usage guidelines.</span></span> <span data-ttu-id="bb83b-111">Par exemple, si vous avez besoin d’ajouter un préfixe ou un suffixe spécifique à un nom de groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-111">For example, if you require a specific prefix or suffix to be added to a group name.</span></span>

<span data-ttu-id="bb83b-112">Utilisez la Azure Active Directory PowerShell (Azure AD) pour faire pointer vos utilisateurs vers les instructions d’utilisation de votre organisation pour Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="bb83b-112">Use the Azure Active Directory (Azure AD) PowerShell to point your users to your organization's usage guidelines for Microsoft 365 groups.</span></span> <span data-ttu-id="bb83b-113">Consultez [Azure Active Directory cmdlets](/azure/active-directory/enterprise-users/groups-settings-cmdlets) pour configurer les paramètres de groupe et suivez les étapes de la procédure Créer des **paramètres** au niveau du répertoire pour définir le lien hypertexte de recommandation d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="bb83b-113">Check out [Azure Active Directory cmdlets for configuring group settings](/azure/active-directory/enterprise-users/groups-settings-cmdlets) and follow the steps in the **Create settings at the directory level** to define the usage guideline hyperlink.</span></span> <span data-ttu-id="bb83b-114">Une fois que vous avez exécuté l’cmdlet AAD, les utilisateurs voient le lien vers vos instructions lorsqu’ils créent ou modifient un groupe dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="bb83b-114">Once you run the AAD cmdlet, users will see the link to your guidelines when they create or edit a group in Outlook.</span></span>

![Créer un groupe avec le lien Recommandations en matière d’utilisation](../media/3f74463f-3448-4f24-a0ec-086d9aa95caa.png)

![Cliquez sur Recommandations en matière d’utilisation des groupes pour voir vos organisations et Office 365 groupes](../media/d0d54ace-f0ec-4946-b2de-50ce23f17765.png)

## <a name="allow-users-to-send-as-the-microsoft-365-group"></a><span data-ttu-id="bb83b-117">Autoriser les utilisateurs à envoyer en tant que Microsoft 365 groupe</span><span class="sxs-lookup"><span data-stu-id="bb83b-117">Allow users to Send as the Microsoft 365 Group</span></span>
<span data-ttu-id="bb83b-118"><a name="BK_LinkToGuideLines"> </a></span><span class="sxs-lookup"><span data-stu-id="bb83b-118"><a name="BK_LinkToGuideLines"> </a></span></span>

<span data-ttu-id="bb83b-119">Si vous souhaitez activer vos groupes Microsoft 365 sur « Envoyer en tant que », utilisez les cmdlets [Add-RecipientPermission](/powershell/module/exchange/add-recipientpermission) et [Get-RecipientPermission](/powershell/module/exchange/get-recipientpermission) pour configurer cette configuration.</span><span class="sxs-lookup"><span data-stu-id="bb83b-119">If you want to enable your Microsoft 365 groups to "Send As", use the [Add-RecipientPermission](/powershell/module/exchange/add-recipientpermission) and [Get-RecipientPermission](/powershell/module/exchange/get-recipientpermission) cmdlets to configure this.</span></span> <span data-ttu-id="bb83b-120">Une fois ce paramètre activé, les Microsoft 365 de groupe peuvent utiliser Outlook ou Outlook sur le web pour envoyer et répondre à des messages électroniques en tant que Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-120">Once you enable this setting, Microsoft 365 group users can use Outlook or Outlook on the web to send and reply to email as the Microsoft 365 group.</span></span> <span data-ttu-id="bb83b-121">Les utilisateurs peuvent aller au groupe, créer un e-mail et modifier le champ « Envoyer en tant que » en l’adresse e-mail du groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-121">Users can go to the group, create a new email, and change the "Send As" field to the group's email address.</span></span>

<span data-ttu-id="bb83b-122">([Vous pouvez également le faire dans le Exchange Admin Center.)](/office365/admin/create-groups/allow-members-to-send-as-or-send-on-behalf-of-group)</span><span class="sxs-lookup"><span data-stu-id="bb83b-122">([You can also do this in the Exchange Admin Center](/office365/admin/create-groups/allow-members-to-send-as-or-send-on-behalf-of-group).)</span></span>

<span data-ttu-id="bb83b-123">Utilisez le script suivant, en remplaçant par l’alias du groupe que vous souhaitez mettre à jour, et par l’alias de l’utilisateur auquel vous souhaitez accorder *\<GroupAlias\>* *\<UserAlias\>* des autorisations.</span><span class="sxs-lookup"><span data-stu-id="bb83b-123">Use the following script, replacing *\<GroupAlias\>* with the alias of the group that you want to update, and *\<UserAlias\>* with the alias of the user to whom you want to grant permissions.</span></span> <span data-ttu-id="bb83b-124">[Connecter à Exchange Online PowerShell pour](/powershell/exchange/connect-to-exchange-online-powershell) exécuter ce script.</span><span class="sxs-lookup"><span data-stu-id="bb83b-124">[Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) to run this script.</span></span>

```PowerShell
$groupAlias = "<GroupAlias>"
$userAlias = "<UserAlias>"
$groupsRecipientDetails = Get-Recipient -RecipientTypeDetails groupmailbox -Identity $groupAlias

Add-RecipientPermission -Identity $groupsRecipientDetails.Name -Trustee $userAlias -AccessRights SendAs
```

<span data-ttu-id="bb83b-125">Une fois la cmdlet exécutée, les utilisateurs peuvent se rendre sur Outlook ou Outlook sur le web  pour envoyer en tant que groupe, en ajoutant l’adresse de messagerie du groupe au champ De.</span><span class="sxs-lookup"><span data-stu-id="bb83b-125">Once the cmdlet is executed, users can go to Outlook or Outlook on the web to send as the group, by adding the group email address to the **From** field.</span></span>

## <a name="create-classifications-for-microsoft-365-groups-in-your-organization"></a><span data-ttu-id="bb83b-126">Créer des classifications pour Microsoft 365 groupes de votre organisation</span><span class="sxs-lookup"><span data-stu-id="bb83b-126">Create classifications for Microsoft 365 Groups in your organization</span></span>

<span data-ttu-id="bb83b-127">Vous pouvez créer des étiquettes de niveau de sensibilité que les utilisateurs de votre organisation peuvent définir lorsqu’ils créent un Microsoft 365 de données.</span><span class="sxs-lookup"><span data-stu-id="bb83b-127">You can create sensitivity labels that the users in your organization can set when they create a Microsoft 365 Group.</span></span> <span data-ttu-id="bb83b-128">Si vous souhaitez classer des groupes, nous vous recommandons d’utiliser des étiquettes de niveau de sensibilité plutôt que la fonctionnalité de classification des groupes précédente.</span><span class="sxs-lookup"><span data-stu-id="bb83b-128">If you want to classify groups, we recommend using sensitivity labels instead of the previous groups classification feature.</span></span> <span data-ttu-id="bb83b-129">Pour plus d’informations sur l’utilisation d’étiquettes de sensibilité, voir Utiliser des étiquettes de niveau de Microsoft Teams, Microsoft 365 groupes et sites [SharePoint sites.](../compliance/sensitivity-labels-teams-groups-sites.md)</span><span class="sxs-lookup"><span data-stu-id="bb83b-129">For information about using sensitivity labels, see [Use sensitivity labels to protect content in Microsoft Teams, Microsoft 365 groups, and SharePoint sites](../compliance/sensitivity-labels-teams-groups-sites.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb83b-130">Si vous utilisez actuellement des étiquettes de classification, elles ne seront plus disponibles pour les utilisateurs qui créent des groupes une fois les étiquettes de niveau de sensibilité activées.</span><span class="sxs-lookup"><span data-stu-id="bb83b-130">If you are currently using classification labels, they will no longer be available to users who create groups once sensitivity labels are enabled.</span></span>

<span data-ttu-id="bb83b-131">Vous pouvez toujours utiliser la fonctionnalité de classification de groupes précédente.</span><span class="sxs-lookup"><span data-stu-id="bb83b-131">You can still use the previous groups classification feature.</span></span> <span data-ttu-id="bb83b-132">Vous pouvez créer des classifications que les utilisateurs de votre organisation peuvent définir lorsqu’ils créent Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-132">You can create classifications that the users in your organization can set when they create an Microsoft 365 Group.</span></span> <span data-ttu-id="bb83b-133">Par exemple, vous pouvez autoriser les utilisateurs à définir « Standard », « Secret » et « Top Secret » sur les groupes qu’ils créent.</span><span class="sxs-lookup"><span data-stu-id="bb83b-133">For example, you can allow users to set "Standard", "Secret", and "Top Secret" on groups they create.</span></span> <span data-ttu-id="bb83b-134">Les classifications de groupe ne sont pas définies par défaut et vous devez la créer pour que vos utilisateurs la définissent.</span><span class="sxs-lookup"><span data-stu-id="bb83b-134">Group classifications aren't set by default and you need to create it in order for your users to set it.</span></span> <span data-ttu-id="bb83b-135">Utilisez Azure Active Directory PowerShell pour faire pointer vos utilisateurs vers les instructions d’utilisation de votre organisation pour Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="bb83b-135">Use Azure Active Directory PowerShell to point your users to your organization's usage guidelines for Microsoft 365 Groups.</span></span>

<span data-ttu-id="bb83b-136">Consultez [Azure Active Directory cmdlets](/azure/active-directory/users-groups-roles/groups-settings-cmdlets) pour configurer les paramètres de groupe et suivez les étapes de la procédure Créer des **paramètres** au niveau du répertoire pour définir la classification des groupes Microsoft 365 de groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-136">Check out [Azure Active Directory cmdlets for configuring group settings](/azure/active-directory/users-groups-roles/groups-settings-cmdlets) and follow the steps in the **Create settings at the directory level** to define the classification for Microsoft 365 Groups.</span></span>

```powershell
$setting["ClassificationList"] = "Low Impact, Medium Impact, High Impact"
```

<span data-ttu-id="bb83b-137">Pour associer une description à chaque classification, vous pouvez utiliser l’attribut paramètres  *ClassificationDescriptions* pour définir.</span><span class="sxs-lookup"><span data-stu-id="bb83b-137">In order to associate a description to each classification you can use the settings attribute  *ClassificationDescriptions* to define.</span></span>

```powershell
$setting["ClassificationDescriptions"] ="Classification:Description,Classification:Description"
```

<span data-ttu-id="bb83b-138">où Classification correspond aux chaînes dans ClassificationList.</span><span class="sxs-lookup"><span data-stu-id="bb83b-138">where Classification matches the strings in the ClassificationList.</span></span>

<span data-ttu-id="bb83b-139">Exemple :</span><span class="sxs-lookup"><span data-stu-id="bb83b-139">Example:</span></span>

```powershell
$setting["ClassificationDescriptions"] = "Low Impact: General communication, Medium Impact: Company internal data , High Impact: Data that has regulatory requirements"
```

<span data-ttu-id="bb83b-140">Après avoir exécuté l’Azure Active Directory cmdlet ci-dessus pour définir votre classification, exécutez la cmdlet [Set-UnifiedGroup](/powershell/module/exchange/Set-UnifiedGroup) si vous souhaitez définir la classification pour un groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="bb83b-140">After you run the above Azure Active Directory cmdlet to set your classification, run the [Set-UnifiedGroup](/powershell/module/exchange/Set-UnifiedGroup) cmdlet if you want to set the classification for a specific group.</span></span>

```powershell
Set-UnifiedGroup <LowImpactGroup@constoso.com> -Classification <LowImpact>
```

<span data-ttu-id="bb83b-141">Vous pouvez également créer un groupe avec une classification.</span><span class="sxs-lookup"><span data-stu-id="bb83b-141">Or create a new group with a classification.</span></span>

```powershell
New-UnifiedGroup <HighImpactGroup@constoso.com> -Classification <HighImpact> -AccessType <Public>
```

<span data-ttu-id="bb83b-142">Consultez [l’utilisation](/powershell/exchange/exchange-online-powershell) de PowerShell Exchange Online et Connecter pour Exchange Online [PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) pour plus d’informations sur l’utilisation Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb83b-142">Check out [Using PowerShell with Exchange Online](/powershell/exchange/exchange-online-powershell) and [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) for more details on using Exchange Online PowerShell.</span></span>

<span data-ttu-id="bb83b-143">Une fois ces paramètres activés, le propriétaire du groupe peut choisir une classification dans le menu déroulant dans Outlook  sur le Web et Outlook, puis l’enregistrer à partir de la page Modifier le groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-143">Once these settings are enabled, the group owner will be able to choose a classification from the drop down menu in Outlook on the Web and Outlook, and save it from the **Edit** group page.</span></span>

![Choisir Microsoft 365 classification de groupe](../media/f8d4219a-6180-491d-b0e1-4313ac83998b.png)

## <a name="hide-microsoft-365-groups-from-the-global-address-list"></a><span data-ttu-id="bb83b-145">Masquez Microsoft 365 de la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="bb83b-145">Hide Microsoft 365 Groups from the global address list.</span></span>
<span data-ttu-id="bb83b-146"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="bb83b-146"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="bb83b-147">Vous pouvez spécifier si un groupe Microsoft 365 apparaît dans la liste d’adresses globale (LAL) et dans d’autres listes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bb83b-147">You can specify whether a Microsoft 365 Group appears in the global address list (GAL) and other lists in your organization.</span></span> <span data-ttu-id="bb83b-148">Par exemple, si vous avez un groupe de services juridiques que vous ne souhaitez pas afficher dans la liste d’adresses, vous pouvez empêcher ce groupe d’apparaître dans la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="bb83b-148">For example, if you have a legal department group that you don't want to show up in the address list, you can stop that group from appearing in the GAL.</span></span> <span data-ttu-id="bb83b-149">Exécutez la cmdlet Set-Unified groupe pour masquer le groupe dans la liste d’adresses comme ceci :</span><span class="sxs-lookup"><span data-stu-id="bb83b-149">Run the Set-Unified Group cmdlet to hide the group from the address list like this:</span></span>

```powershell
Set-UnifiedGroup -Identity "Legal Department" -HiddenFromAddressListsEnabled $true
```

## <a name="allow-only-internal-users-to-send-message-to-microsoft-365-groups"></a><span data-ttu-id="bb83b-150">Autoriser uniquement les utilisateurs internes à envoyer des messages à Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="bb83b-150">Allow only internal users to send message to Microsoft 365 Groups</span></span>
<span data-ttu-id="bb83b-151"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="bb83b-151"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="bb83b-152">Si vous ne souhaitez pas que les utilisateurs d’autres organisations envoient des courriers électroniques à un groupe Microsoft 365, vous pouvez modifier les paramètres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-152">If you don't want users from other organizations to send emails to a Microsoft 365 Group, you can change the settings for that group.</span></span> <span data-ttu-id="bb83b-153">Il permet uniquement aux utilisateurs internes d’envoyer un courrier électronique à votre groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-153">It will allow only internal users to send an email to your group.</span></span> <span data-ttu-id="bb83b-154">Si un utilisateur externe tente d’envoyer un message à ce groupe, il est rejeté.</span><span class="sxs-lookup"><span data-stu-id="bb83b-154">If an external user tries to send a message to that group, it will be rejected.</span></span>

<span data-ttu-id="bb83b-155">Exécutez lSet-UnifiedGroup cmdlet pour mettre à jour ce paramètre, comme ceci :</span><span class="sxs-lookup"><span data-stu-id="bb83b-155">Run the Set-UnifiedGroup cmdlet to update this setting, like this:</span></span>

```powershell
Set-UnifiedGroup -Identity "Internal senders only" -RequireSenderAuthenticationEnabled $true
```

## <a name="add-mailtips-to-microsoft-365-groups"></a><span data-ttu-id="bb83b-156">Ajouter des mailTips à Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="bb83b-156">Add MailTips to Microsoft 365 Groups</span></span>
<span data-ttu-id="bb83b-157"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="bb83b-157"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="bb83b-158">Chaque fois qu’un expéditeur tente d’envoyer un message électronique à un groupe Microsoft 365, une boîte aux lettres peut s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bb83b-158">Whenever a sender tries to send an email to a Microsoft 365 Group, a MailTip can be shown to them.</span></span>

<span data-ttu-id="bb83b-159">Exécutez la cmdlet Set-Unified groupe pour ajouter une mailTip au groupe :</span><span class="sxs-lookup"><span data-stu-id="bb83b-159">Run the Set-Unified Group cmdlet to add a mailTip to the group:</span></span>

```powershell
Set-UnifiedGroup -Identity "MailTip Group" -MailTip "This group has a MailTip"
```

<span data-ttu-id="bb83b-160">En plus de l’tip de courrier, vous pouvez également définir MailTipTranslations, qui spécifie des langues supplémentaires pour l’mailTip.</span><span class="sxs-lookup"><span data-stu-id="bb83b-160">Along with MailTip, you can also set MailTipTranslations, which specifies additional languages for the MailTip.</span></span> <span data-ttu-id="bb83b-161">Supposons que vous vouliez avoir la traduction espagnole, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bb83b-161">Suppose you want to have the Spanish translation, then run the following command:</span></span>

```powershell
Set-UnifiedGroup -Identity "MailaTip Group" -MailTip "This group has a MailTip" -MailTipTranslations "@{Add="ES:Esta caja no se supervisa."
```

## <a name="change-the-display-name-of-the-microsoft-365-group"></a><span data-ttu-id="bb83b-162">Modifier le nom complet du groupe de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bb83b-162">Change the display name of the Microsoft 365 Group</span></span>

<span data-ttu-id="bb83b-163">Le nom complet spécifie le nom du groupe Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-163">The display name specifies the name of the Microsoft 365 Group.</span></span> <span data-ttu-id="bb83b-164">Vous pouvez voir ce nom dans votre Centre d’administration Exchange ou Microsoft 365'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb83b-164">You can see this name in your exchange admin center or Microsoft 365 admin center.</span></span> <span data-ttu-id="bb83b-165">Vous pouvez modifier le nom complet du groupe ou attribuer un nom complet à un groupe Microsoft 365 existant en exécutant la commande Set-UnifiedGroup:</span><span class="sxs-lookup"><span data-stu-id="bb83b-165">You can edit the display name of the group or assign a display name to an existing Microsoft 365 Group by running the Set-UnifiedGroup command:</span></span>

```powershell
Set-UnifiedGroup -Identity "mygroup@contoso.com" -DisplayName "My new group"
```

## <a name="change-the-default-setting-of-microsoft-365-groups-for-outlook-to-public-or-private"></a><span data-ttu-id="bb83b-166">Modifier le paramètre par défaut de Microsoft 365 groupes pour Outlook public ou privé</span><span class="sxs-lookup"><span data-stu-id="bb83b-166">Change the default setting of Microsoft 365 Groups for Outlook to Public or Private</span></span>
<span data-ttu-id="bb83b-167"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="bb83b-167"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="bb83b-168">Microsoft 365 Les groupes dans Outlook sont créés comme privés par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb83b-168">Microsoft 365 Groups in Outlook are created as Private by default.</span></span> <span data-ttu-id="bb83b-169">Si votre organisation souhaite créer Microsoft 365 groupes publics par défaut (ou de nouveau en privé), utilisez la syntaxe de l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="bb83b-169">If your organization wants Microsoft 365 Groups to be created as Public by default (or back to Private), use this PowerShell cmdlet syntax:</span></span>

 `Set-OrganizationConfig -DefaultGroupAccessType Public`

<span data-ttu-id="bb83b-170">Pour définir sur Privé :</span><span class="sxs-lookup"><span data-stu-id="bb83b-170">To set to Private:</span></span>

 `Set-OrganizationConfig -DefaultGroupAccessType Private`

<span data-ttu-id="bb83b-171">Pour vérifier le paramètre :</span><span class="sxs-lookup"><span data-stu-id="bb83b-171">To verify the setting:</span></span>

 `Get-OrganizationConfig | ft DefaultGroupAccessType`

<span data-ttu-id="bb83b-172">Pour plus d’informations, [voir Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig) et [Get-OrganizationConfig](/powershell/module/exchange/get-organizationconfig).</span><span class="sxs-lookup"><span data-stu-id="bb83b-172">To learn more, see [Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig) and [Get-OrganizationConfig](/powershell/module/exchange/get-organizationconfig).</span></span>

## <a name="microsoft-365-groups-cmdlets"></a><span data-ttu-id="bb83b-173">Microsoft 365 Cmdlets de groupes</span><span class="sxs-lookup"><span data-stu-id="bb83b-173">Microsoft 365 Groups cmdlets</span></span>

<span data-ttu-id="bb83b-174">Les cmdlets suivantes peuvent être utilisées avec Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="bb83b-174">The following cmdlets can be used with Microsoft 365 Groups.</span></span>

|<span data-ttu-id="bb83b-175">**Nom de l'applet de commande**</span><span class="sxs-lookup"><span data-stu-id="bb83b-175">**Cmdlet name**</span></span>|<span data-ttu-id="bb83b-176">**Description**</span><span class="sxs-lookup"><span data-stu-id="bb83b-176">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb83b-177">Get-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="bb83b-177">Get-UnifiedGroup</span></span>](/powershell/module/exchange/get-unifiedgroup) <br/> |<span data-ttu-id="bb83b-178">Utilisez cette cmdlet pour rechercher des groupes Microsoft 365 existants et pour afficher les propriétés de l’objet groupe</span><span class="sxs-lookup"><span data-stu-id="bb83b-178">Use this cmdlet to look up existing Microsoft 365 Groups, and to view properties of the group object</span></span>  <br/> |
|[<span data-ttu-id="bb83b-179">Set-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="bb83b-179">Set-UnifiedGroup</span></span>](/powershell/module/exchange/set-unifiedgroup) <br/> |<span data-ttu-id="bb83b-180">Mettre à jour les propriétés d’un groupe Microsoft 365 spécifique</span><span class="sxs-lookup"><span data-stu-id="bb83b-180">Update the properties of a specific Microsoft 365 Group</span></span>  <br/> |
|[<span data-ttu-id="bb83b-181">New-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="bb83b-181">New-UnifiedGroup</span></span>](/powershell/module/exchange/new-unifiedgroup) <br/> |<span data-ttu-id="bb83b-182">Créez un groupe Microsoft 365'équipe.</span><span class="sxs-lookup"><span data-stu-id="bb83b-182">Create a new Microsoft 365 Group.</span></span> <span data-ttu-id="bb83b-183">Cette cmdlet fournit un ensemble minimal de paramètres.</span><span class="sxs-lookup"><span data-stu-id="bb83b-183">This cmdlet provides a minimal set of parameters.</span></span> <span data-ttu-id="bb83b-184">Pour définir des valeurs pour les propriétés étendues, utilisez Set-UnifiedGroup après la création du nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="bb83b-184">To set values for extended properties, use Set-UnifiedGroup after creating the new group</span></span>  <br/> |
|[<span data-ttu-id="bb83b-185">Remove-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="bb83b-185">Remove-UnifiedGroup</span></span>](/powershell/module/exchange/remove-unifiedgroup) <br/> |<span data-ttu-id="bb83b-186">Supprimer un groupe de Microsoft 365 existant</span><span class="sxs-lookup"><span data-stu-id="bb83b-186">Delete an existing Microsoft 365 Group</span></span>  <br/> |
|[<span data-ttu-id="bb83b-187">Get-UnifiedGroupLinks</span><span class="sxs-lookup"><span data-stu-id="bb83b-187">Get-UnifiedGroupLinks</span></span>](/powershell/module/exchange/get-unifiedgrouplinks) <br/> |<span data-ttu-id="bb83b-188">Récupérer les informations d’appartenance et de propriétaire d’Microsoft 365 groupe</span><span class="sxs-lookup"><span data-stu-id="bb83b-188">Retrieve membership and owner information for a Microsoft 365 Group</span></span>  <br/> |
|[<span data-ttu-id="bb83b-189">Add-UnifiedGroupLinks</span><span class="sxs-lookup"><span data-stu-id="bb83b-189">Add-UnifiedGroupLinks</span></span>](/powershell/module/exchange/add-unifiedgrouplinks) <br/> |<span data-ttu-id="bb83b-190">Ajouter des membres, des propriétaires et des abonnés à un groupe Microsoft 365 existant</span><span class="sxs-lookup"><span data-stu-id="bb83b-190">Add members, owners, and subscribers to an existing Microsoft 365 Group</span></span> <br/> |
|[<span data-ttu-id="bb83b-191">Remove-UnifiedGroupLinks</span><span class="sxs-lookup"><span data-stu-id="bb83b-191">Remove-UnifiedGroupLinks</span></span>](/powershell/module/exchange/remove-unifiedgrouplinks) <br/> |<span data-ttu-id="bb83b-192">Supprimer des propriétaires et des membres d’un groupe Microsoft 365 existant</span><span class="sxs-lookup"><span data-stu-id="bb83b-192">Remove owners and members from an existing Microsoft 365 Group</span></span>  <br/> |
|[<span data-ttu-id="bb83b-193">Get-UserPhoto</span><span class="sxs-lookup"><span data-stu-id="bb83b-193">Get-UserPhoto</span></span>](/powershell/module/exchange/get-userphoto) <br/> |<span data-ttu-id="bb83b-194">Utilisé pour afficher les informations sur la photo de l’utilisateur associée à un compte.</span><span class="sxs-lookup"><span data-stu-id="bb83b-194">Used to view information about the user photo associated with an account.</span></span> <span data-ttu-id="bb83b-195">Les photos de l’utilisateur sont stockées dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="bb83b-195">User photos are stored in Active Directory</span></span>  <br/> |
|[<span data-ttu-id="bb83b-196">Set-UserPhoto</span><span class="sxs-lookup"><span data-stu-id="bb83b-196">Set-UserPhoto</span></span>](/powershell/module/exchange/set-userphoto) <br/> |<span data-ttu-id="bb83b-197">Utilisé pour associer une photo d’utilisateur à un compte.</span><span class="sxs-lookup"><span data-stu-id="bb83b-197">Used to associate a user photo with an account.</span></span> <span data-ttu-id="bb83b-198">Les photos de l’utilisateur sont stockées dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="bb83b-198">User photos are stored in Active Directory</span></span>  <br/> |
|[<span data-ttu-id="bb83b-199">Remove-UserPhoto</span><span class="sxs-lookup"><span data-stu-id="bb83b-199">Remove-UserPhoto</span></span>](/powershell/module/exchange/remove-userphoto) <br/> |<span data-ttu-id="bb83b-200">Supprimer la photo d’un groupe Microsoft 365 de recherche</span><span class="sxs-lookup"><span data-stu-id="bb83b-200">Remove the photo for an Microsoft 365 Group</span></span>  <br/> |

## <a name="related-topics"></a><span data-ttu-id="bb83b-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb83b-201">Related topics</span></span>

[<span data-ttu-id="bb83b-202">Mettre à niveau les listes de distribution Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="bb83b-202">Upgrade distribution lists to Microsoft 365 Groups</span></span>](/office365/admin/manage/upgrade-distribution-lists)

[<span data-ttu-id="bb83b-203">Gérer les personnes autorisées à créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bb83b-203">Manage who can create Microsoft 365 Groups</span></span>](/office365/admin/create-groups/manage-creation-of-groups)

[<span data-ttu-id="bb83b-204">Gérer l’accès invité à Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="bb83b-204">Manage guest access to Microsoft 365 Groups</span></span>](https://support.office.com/article/bfc7a840-868f-4fd6-a390-f347bf51aff6)

[<span data-ttu-id="bb83b-205">Modifier l’appartenance à un groupe statique en dynamique dans</span><span class="sxs-lookup"><span data-stu-id="bb83b-205">Change static group membership to dynamic in</span></span>](/azure/active-directory/users-groups-roles/groups-change-type)
