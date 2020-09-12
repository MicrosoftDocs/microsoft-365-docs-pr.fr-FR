---
title: Gérer les groupes Microsoft 365 avec PowerShell
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
description: Dans cet article, Découvrez comment effectuer des tâches de gestion courantes pour les groupes Microsoft 365 dans PowerShell.
ms.openlocfilehash: a02990b2890d9fdfd523209e1d912aafdaeac091
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47547925"
---
# <a name="manage-microsoft-365-groups-with-powershell"></a><span data-ttu-id="60f4b-103">Gérer les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="60f4b-103">Manage Microsoft 365 Groups with PowerShell</span></span>

<span data-ttu-id="60f4b-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="60f4b-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="60f4b-105">Cet article décrit les étapes à suivre pour effectuer des tâches de gestion courantes pour les groupes dans Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60f4b-105">This article provides the steps for doing common management tasks for Groups in Microsoft PowerShell.</span></span> <span data-ttu-id="60f4b-106">Il répertorie également les applets de commande PowerShell pour les groupes.</span><span class="sxs-lookup"><span data-stu-id="60f4b-106">It also lists the PowerShell cmdlets for Groups.</span></span> <span data-ttu-id="60f4b-107">Pour plus d’informations sur la gestion des sites SharePoint, voir [gérer les sites SharePoint Online à l’aide de PowerShell](https://docs.microsoft.com/sharepoint/manage-team-and-communication-sites-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="60f4b-107">For info about managing SharePoint sites, see [Manage SharePoint Online sites using PowerShell](https://docs.microsoft.com/sharepoint/manage-team-and-communication-sites-in-powershell).</span></span>

## <a name="link-to-your-microsoft-365-groups-usage-guidelines"></a><span data-ttu-id="60f4b-108">Lien vers les instructions d’utilisation de vos groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-108">Link to your Microsoft 365 Groups usage guidelines</span></span>
<span data-ttu-id="60f4b-109"><a name="BK_LinkToGuideLines"> </a></span><span class="sxs-lookup"><span data-stu-id="60f4b-109"><a name="BK_LinkToGuideLines"> </a></span></span>

<span data-ttu-id="60f4b-110">Lorsque les utilisateurs [créent ou modifient un groupe dans Outlook](https://support.office.com/article/04d0c9cf-6864-423c-a380-4fa858f27102.aspx), vous pouvez leur montrer un lien vers les instructions d’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="60f4b-110">When users [create or edit a group in Outlook](https://support.office.com/article/04d0c9cf-6864-423c-a380-4fa858f27102.aspx), you can show them a link to your organization's usage guidelines.</span></span> <span data-ttu-id="60f4b-111">Par exemple, si vous avez besoin d’ajouter un préfixe ou un suffixe spécifique à un nom de groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-111">For example, if you require a specific prefix or suffix to be added to a group name.</span></span>

<span data-ttu-id="60f4b-112">Utilisez Azure Active Directory (Azure AD) PowerShell pour faire pointer vos utilisateurs vers les instructions d’utilisation de votre organisation pour les groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-112">Use the Azure Active Directory (Azure AD) PowerShell to point your users to your organization's usage guidelines for Microsoft 365 groups.</span></span> <span data-ttu-id="60f4b-113">Consultez les [applets de commande Azure Active Directory pour configurer les paramètres de groupe](https://go.microsoft.com/fwlink/?LinkID=827484) et suivez les étapes décrites dans la **section créer des paramètres au niveau du répertoire** pour définir le lien hypertexte des indications d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="60f4b-113">Check out [Azure Active Directory cmdlets for configuring group settings](https://go.microsoft.com/fwlink/?LinkID=827484) and follow the steps in the **Create settings at the directory level** to define the usage guideline hyperlink.</span></span> <span data-ttu-id="60f4b-114">Une fois que vous avez exécuté la cmdlet AAD, les utilisateurs verront le lien vers vos instructions lors de la création ou de la modification d’un groupe dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="60f4b-114">Once you run the AAD cmdlet, user's will see the link to your guidelines when they create or edit a group in Outlook.</span></span>

![Créer un nouveau groupe avec les instructions d’utilisation lien](../media/3f74463f-3448-4f24-a0ec-086d9aa95caa.png)

![Cliquez sur conseils sur l’utilisation des groupes pour consulter les directives de groupes Office 365](../media/d0d54ace-f0ec-4946-b2de-50ce23f17765.png)

## <a name="allow-users-to-send-as-the-microsoft-365-group"></a><span data-ttu-id="60f4b-117">Autoriser les utilisateurs à envoyer en tant que groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-117">Allow users to Send as the Microsoft 365 Group</span></span>
<span data-ttu-id="60f4b-118"><a name="BK_LinkToGuideLines"> </a></span><span class="sxs-lookup"><span data-stu-id="60f4b-118"><a name="BK_LinkToGuideLines"> </a></span></span>

<span data-ttu-id="60f4b-119">Si vous souhaitez activer vos groupes Microsoft 365 sur « Envoyer en tant que », utilisez les cmdlets [Add-RecipientPermission](https://docs.microsoft.com/powershell/module/exchange/add-recipientpermission) et [Get-RecipientPermission](https://docs.microsoft.com/powershell/module/exchange/get-recipientpermission) pour configurer ce.</span><span class="sxs-lookup"><span data-stu-id="60f4b-119">If you want to enable your Microsoft 365 groups to "Send As", use the [Add-RecipientPermission](https://docs.microsoft.com/powershell/module/exchange/add-recipientpermission) and [Get-RecipientPermission](https://docs.microsoft.com/powershell/module/exchange/get-recipientpermission) cmdlets to configure this.</span></span> <span data-ttu-id="60f4b-120">Une fois que vous activez ce paramètre, les utilisateurs du groupe Microsoft 365 peuvent utiliser Outlook ou Outlook sur le Web pour envoyer et répondre à des messages électroniques en tant que groupe 365 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60f4b-120">Once you enable this setting, Microsoft 365 group users can use Outlook or Outlook on the web to send and reply to email as the Microsoft 365 group.</span></span> <span data-ttu-id="60f4b-121">Les utilisateurs peuvent accéder au groupe, créer un nouveau courrier électronique et modifier le champ « envoyer en tant que » sur l’adresse de messagerie du groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-121">Users can go to the group, create a new email, and change the "Send As" field to the group's email address.</span></span>

<span data-ttu-id="60f4b-122">([Vous pouvez également le faire dans le centre d’administration Exchange](https://docs.microsoft.com/office365/admin/create-groups/allow-members-to-send-as-or-send-on-behalf-of-group).)</span><span class="sxs-lookup"><span data-stu-id="60f4b-122">([You can also do this in the Exchange Admin Center](https://docs.microsoft.com/office365/admin/create-groups/allow-members-to-send-as-or-send-on-behalf-of-group).)</span></span>

<span data-ttu-id="60f4b-123">Utilisez le script suivant, *\<GroupAlias\>* en remplaçant par l’alias du groupe que vous souhaitez mettre à jour, et *\<UserAlias\>* par l’alias de l’utilisateur auquel vous souhaitez accorder des autorisations.</span><span class="sxs-lookup"><span data-stu-id="60f4b-123">Use the following script, replacing *\<GroupAlias\>* with the alias of the group that you want to update, and *\<UserAlias\>* with the alias of the user to whom you want to grant permissions.</span></span> <span data-ttu-id="60f4b-124">[Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) pour exécuter ce script.</span><span class="sxs-lookup"><span data-stu-id="60f4b-124">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) to run this script.</span></span>

```PowerShell
$groupAlias = "<GroupAlias>"
$userAlias = "<UserAlias>"
$groupsRecipientDetails = Get-Recipient -RecipientTypeDetails groupmailbox -Identity $groupAlias

Add-RecipientPermission -Identity $groupsRecipientDetails.Name -Trustee $userAlias -AccessRights SendAs
```

<span data-ttu-id="60f4b-125">Une fois l’applet de commande exécutée, les utilisateurs peuvent accéder à Outlook ou à Outlook sur le Web pour les envoyer en tant que groupe, en ajoutant l’adresse de messagerie du groupe au champ **de** .</span><span class="sxs-lookup"><span data-stu-id="60f4b-125">Once the cmdlet is executed, users can go to Outlook or Outlook on the web to send as the group, by adding the group email address to the **From** field.</span></span>

## <a name="create-classifications-for-office-groups-in-your-organization"></a><span data-ttu-id="60f4b-126">Créer des classifications pour les groupes Office dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="60f4b-126">Create classifications for Office groups in your organization</span></span>

<span data-ttu-id="60f4b-127">Vous pouvez créer des étiquettes de confidentialité que les utilisateurs de votre organisation peuvent définir lors de la création d’un groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-127">You can create sensitivity labels that the users in your organization can set when they create a Microsoft 365 Group.</span></span> <span data-ttu-id="60f4b-128">Si vous souhaitez classer les groupes, nous vous recommandons d’utiliser des étiquettes de confidentialité au lieu de la fonctionnalité de classification des groupes précédents.</span><span class="sxs-lookup"><span data-stu-id="60f4b-128">If you want to classify groups, we recommend using sensitivity labels instead of the previous groups classification feature.</span></span> <span data-ttu-id="60f4b-129">Pour plus d’informations sur l’utilisation des étiquettes de confidentialité, consultez la rubrique [utiliser des étiquettes de sensibilité pour protéger le contenu dans Microsoft Teams, les groupes microsoft 365 et les sites SharePoint](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span><span class="sxs-lookup"><span data-stu-id="60f4b-129">For information about using sensitivity labels, see [Use sensitivity labels to protect content in Microsoft Teams, Microsoft 365 groups, and SharePoint sites](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60f4b-130">Si vous utilisez actuellement des étiquettes de classification, ces derniers ne seront plus disponibles pour les utilisateurs qui créent des groupes une fois que les étiquettes de sensibilité seront activées.</span><span class="sxs-lookup"><span data-stu-id="60f4b-130">If you are currently using classification labels, they will no longer be available to users who create groups once sensitivity labels are enabled.</span></span>

<span data-ttu-id="60f4b-131">Vous pouvez toujours utiliser la fonctionnalité de classification de groupes précédente.</span><span class="sxs-lookup"><span data-stu-id="60f4b-131">You can still use the previous groups classification feature.</span></span> <span data-ttu-id="60f4b-132">Vous pouvez créer des classifications que les utilisateurs de votre organisation peuvent définir lors de la création d’un groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-132">You can create classifications that the users in your organization can set when they create an Office 365 group.</span></span> <span data-ttu-id="60f4b-133">Par exemple, vous pouvez autoriser les utilisateurs à définir « standard », « secret » et « top secret » dans les groupes qu’ils créent.</span><span class="sxs-lookup"><span data-stu-id="60f4b-133">For example, you can allow users to set "Standard", "Secret", and "Top Secret" on groups they create.</span></span> <span data-ttu-id="60f4b-134">Les classifications de groupe ne sont pas définies par défaut et vous devez les créer afin que les utilisateurs puissent la définir.</span><span class="sxs-lookup"><span data-stu-id="60f4b-134">Group classifications aren't set by default and you need to create it in order for your users to set it.</span></span> <span data-ttu-id="60f4b-135">Utilisez Azure Active Directory PowerShell pour faire pointer vos utilisateurs vers les instructions d’utilisation de votre organisation pour les groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-135">Use Azure Active Directory PowerShell to point your users to your organization's usage guidelines for Office 365 groups.</span></span>

<span data-ttu-id="60f4b-136">Consultez les [applets de commande Azure Active Directory pour configurer les paramètres de groupe](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets) et suivez les étapes décrites dans la **section Create Settings at the Directory Level** to define the Classification for Office 365 groups.</span><span class="sxs-lookup"><span data-stu-id="60f4b-136">Check out [Azure Active Directory cmdlets for configuring group settings](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets) and follow the steps in the **Create settings at the directory level** to define the classification for Office 365 groups.</span></span>

```powershell
$setting["ClassificationList"] = "Low Impact, Medium Impact, High Impact"
```

<span data-ttu-id="60f4b-137">Afin d’associer une description à chaque classification, vous pouvez utiliser l’attribut Settings  *ClassificationDescriptions* pour définir.</span><span class="sxs-lookup"><span data-stu-id="60f4b-137">In order to associate a description to each classification you can use the settings attribute  *ClassificationDescriptions* to define.</span></span>

```powershell
$setting["ClassificationDescriptions"] ="Classification:Description,Classification:Description"
```

<span data-ttu-id="60f4b-138">où la classification établit une correspondance avec les chaînes du ClassificationList.</span><span class="sxs-lookup"><span data-stu-id="60f4b-138">where Classification matches the strings in the ClassificationList.</span></span>

<span data-ttu-id="60f4b-139">Exemple :</span><span class="sxs-lookup"><span data-stu-id="60f4b-139">Example:</span></span>

```powershell
$setting["ClassificationDescriptions"] = "Low Impact: General communication, Medium Impact: Company internal data , High Impact: Data that has regulatory requirements"
```

<span data-ttu-id="60f4b-140">Après avoir exécuté la cmdlet Azure Active Directory ci-dessus pour définir votre classification, exécutez la cmdlet [Set-UnifiedGroup](https://docs.microsoft.com/powershell/module/exchange/Set-UnifiedGroup) si vous voulez définir la classification pour un groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="60f4b-140">After you run the above Azure Active Directory cmdlet to set your classification, run the [Set-UnifiedGroup](https://docs.microsoft.com/powershell/module/exchange/Set-UnifiedGroup) cmdlet if you want to set the classification for a specific group.</span></span>

```powershell
Set-UnifiedGroup <LowImpactGroup@constoso.com> -Classification <LowImpact>
```

<span data-ttu-id="60f4b-141">Ou créez un groupe avec une classification.</span><span class="sxs-lookup"><span data-stu-id="60f4b-141">Or create a new group with a classification.</span></span>

```powershell
New-UnifiedGroup <HighImpactGroup@constoso.com> -Classification <HighImpact> -AccessType <Public>
```

<span data-ttu-id="60f4b-142">Pour plus d’informations sur l’utilisation d’Exchange Online PowerShell, consultez [l’aide de PowerShell avec Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell) et [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) .</span><span class="sxs-lookup"><span data-stu-id="60f4b-142">Check out [Using PowerShell with Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell) and [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) for more details on using Exchange Online PowerShell.</span></span>

<span data-ttu-id="60f4b-143">Une fois ces paramètres activés, le propriétaire du groupe pourra choisir une classification dans le menu déroulant dans Outlook sur le Web et Outlook, puis enregistrez-le à partir de la page **modifier** le groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-143">Once these settings are enabled, the group owner will be able to choose a classification from the drop down menu in Outlook on the Web and Outlook, and save it from the **Edit** group page.</span></span>

![Choisir la classification de groupe Office 365](../media/f8d4219a-6180-491d-b0e1-4313ac83998b.png)

## <a name="hide-office-365-groups-from-gal"></a><span data-ttu-id="60f4b-145">Masquer les groupes Office 365 dans la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="60f4b-145">Hide Office 365 Groups from GAL</span></span>
<span data-ttu-id="60f4b-146"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="60f4b-146"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="60f4b-147">Vous pouvez spécifier si un groupe Office 365 apparaît dans la liste d’adresses globale (LAG) et d’autres listes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="60f4b-147">You can specify whether an Office 365 group appears in the global address list (GAL) and other lists in your organization.</span></span> <span data-ttu-id="60f4b-148">Par exemple, si vous avez un groupe de services légaux que vous ne voulez pas afficher dans la liste d’adresses, vous pouvez l’empêcher d’apparaître dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="60f4b-148">For example, if you have a legal department group that you don't want to show up in the address list, you can stop that group from appearing in GAL.</span></span> <span data-ttu-id="60f4b-149">Exécutez la cmdlet Set-Unified Group pour masquer le groupe de la liste d’adresses comme suit :</span><span class="sxs-lookup"><span data-stu-id="60f4b-149">Run the Set-Unified Group cmdlet to hide the group from address list like this:</span></span>

```powershell
Set-UnifiedGroup -Identity "Legal Department" -HiddenFromAddressListsEnabled $true
```

## <a name="allow-only-internal-users-to-send-message-to-office-365-group"></a><span data-ttu-id="60f4b-150">Autoriser uniquement les utilisateurs internes à envoyer un message au groupe Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-150">Allow only internal users to send message to Office 365 group</span></span>
<span data-ttu-id="60f4b-151"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="60f4b-151"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="60f4b-152">Si vous ne voulez pas que les utilisateurs d’autres organisations puissent envoyer des messages électroniques à un groupe Office 365, vous pouvez modifier les paramètres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-152">If you don't want users from other organization to send email to an Office 365 group, you can change the settings for that group.</span></span> <span data-ttu-id="60f4b-153">Il permettra uniquement aux utilisateurs internes d’envoyer un courrier électronique à votre groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-153">It will allow only internal users to send an email to your group.</span></span> <span data-ttu-id="60f4b-154">Si un utilisateur externe essaie d’envoyer un message à ce groupe, il sera rejeté.</span><span class="sxs-lookup"><span data-stu-id="60f4b-154">If external user try to send message to that group they will be rejected.</span></span>

<span data-ttu-id="60f4b-155">Exécutez la cmdlet Set-UnifiedGroup pour mettre à jour ce paramètre, comme suit :</span><span class="sxs-lookup"><span data-stu-id="60f4b-155">Run the Set-UnifiedGroup cmdlet to update this setting, like this:</span></span>

```powershell
Set-UnifiedGroup -Identity "Internal senders only" -RequireSenderAuthenticationEnabled $true
```

## <a name="add-mailtips-to-the-office-365-groups"></a><span data-ttu-id="60f4b-156">Ajouter des infos-courrier aux groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-156">Add MailTips to the Office 365 Groups</span></span>
<span data-ttu-id="60f4b-157"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="60f4b-157"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="60f4b-158">Chaque fois qu’un expéditeur tente d’envoyer un message électronique à un groupe Office 365, un info-courrier peut s’afficher.</span><span class="sxs-lookup"><span data-stu-id="60f4b-158">Whenever a sender tries to send an email to an Office 365 group, a MailTip can be shown to them.</span></span>

<span data-ttu-id="60f4b-159">Exécutez la cmdlet Set-Unified Group pour ajouter un info-courrier au groupe :</span><span class="sxs-lookup"><span data-stu-id="60f4b-159">Run the Set-Unified Group cmdlet to add a mailTip to the group:</span></span>

```powershell
Set-UnifiedGroup -Identity "MailTip Group" -MailTip "This group has a MailTip"
```

<span data-ttu-id="60f4b-160">Avec info-courrier, vous pouvez également définir MailTipTranslations, qui spécifie des langues supplémentaires pour l’info-courrier.</span><span class="sxs-lookup"><span data-stu-id="60f4b-160">Along with MailTip, you can also set MailTipTranslations, which specifies additional languages for the MailTip.</span></span> <span data-ttu-id="60f4b-161">Supposons que vous voulez avoir la traduction espagnole, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="60f4b-161">Suppose you want to have the Spanish translation, then run the following command:</span></span>

```powershell
Set-UnifiedGroup -Identity "MailaTip Group" -MailTip "This group has a MailTip" -MailTipTranslations "@{Add="ES:Esta caja no se supervisa."
```

## <a name="change-display-name-of-the-office-365-group"></a><span data-ttu-id="60f4b-162">Modifier le nom d’affichage du groupe Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-162">Change Display name of the Office 365 group</span></span>

<span data-ttu-id="60f4b-163">Nom d’affichage spécifie le nom du groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-163">Display name specifies the name of the Office 365 group.</span></span> <span data-ttu-id="60f4b-164">Vous pouvez voir ce nom dans votre centre d’administration Exchange ou dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-164">You can see this name in your exchange admin center or Microsoft 365 admin center.</span></span> <span data-ttu-id="60f4b-165">Vous pouvez modifier le nom d’affichage du groupe ou attribuer un nom d’affichage à un groupe Office 365 existant en exécutant la commande Set-UnifiedGroup :</span><span class="sxs-lookup"><span data-stu-id="60f4b-165">You can edit the display name of the group or assign a display name to an existing Office 365 group by running the Set-UnifiedGroup command:</span></span>

```powershell
Set-UnifiedGroup -Identity "mygroup@contoso.com" -DisplayName "My new group"
```

## <a name="change-the-default-setting-of-office-365-groups-for-outlook-to-public-or-private"></a><span data-ttu-id="60f4b-166">Modifier le paramètre par défaut des groupes Office 365 pour Outlook en mode public ou privé</span><span class="sxs-lookup"><span data-stu-id="60f4b-166">Change the default setting of Office 365 Groups for Outlook to Public or Private</span></span>
<span data-ttu-id="60f4b-167"><a name="BKMK_CreateClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="60f4b-167"><a name="BKMK_CreateClassification"> </a></span></span>

<span data-ttu-id="60f4b-168">Les groupes Office 365 dans Outlook sont créés comme étant privés par défaut.</span><span class="sxs-lookup"><span data-stu-id="60f4b-168">Office 365 Groups in Outlook are created as Private by default.</span></span> <span data-ttu-id="60f4b-169">Si votre organisation souhaite que les groupes Office 365 soient créés en tant que public par défaut (ou retour à privé), utilisez la syntaxe de cette cmdlet PowerShell :</span><span class="sxs-lookup"><span data-stu-id="60f4b-169">If your organization wants Office 365 Groups to be created as Public by default (or back to Private), use this PowerShell cmdlet syntax:</span></span>

 `Set-OrganizationConfig -DefaultGroupAccessType Public`

<span data-ttu-id="60f4b-170">Pour définir sur privé :</span><span class="sxs-lookup"><span data-stu-id="60f4b-170">To set to Private:</span></span>

 `Set-OrganizationConfig -DefaultGroupAccessType Private`

<span data-ttu-id="60f4b-171">Pour vérifier le paramètre :</span><span class="sxs-lookup"><span data-stu-id="60f4b-171">To verify the setting:</span></span>

 `Get-OrganizationConfig | ft DefaultGroupAccessType`

<span data-ttu-id="60f4b-172">Pour plus d’informations, consultez la rubrique [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig) et [Get-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/get-organizationconfig).</span><span class="sxs-lookup"><span data-stu-id="60f4b-172">To learn more, see [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig) and [Get-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/get-organizationconfig).</span></span>

## <a name="office-365-groups-cmdlets"></a><span data-ttu-id="60f4b-173">Cmdlets de groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-173">Office 365 Groups cmdlets</span></span>

<span data-ttu-id="60f4b-174">Les applets de commande suivantes peuvent être utilisées avec les groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-174">The following cmdlets can be used with Office 365 Groups.</span></span>

|<span data-ttu-id="60f4b-175">**Nom de l'applet de commande**</span><span class="sxs-lookup"><span data-stu-id="60f4b-175">**Cmdlet name**</span></span>|<span data-ttu-id="60f4b-176">**Description**</span><span class="sxs-lookup"><span data-stu-id="60f4b-176">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60f4b-177">Get-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="60f4b-177">Get-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616182) <br/> |<span data-ttu-id="60f4b-178">Utilisez cette applet de commande pour rechercher des groupes Office 365 existants et afficher les propriétés de l’objet de groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-178">Use this cmdlet to look up existing Office 365 Groups, and to view properties of the group object</span></span>  <br/> |
|[<span data-ttu-id="60f4b-179">Set-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="60f4b-179">Set-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616189) <br/> |<span data-ttu-id="60f4b-180">Mettre à jour les propriétés d’un groupe Office 365 spécifique</span><span class="sxs-lookup"><span data-stu-id="60f4b-180">Update the properties of a specific Office 365 Group</span></span>  <br/> |
|[<span data-ttu-id="60f4b-181">New-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="60f4b-181">New-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616183) <br/> |<span data-ttu-id="60f4b-182">Créez un groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="60f4b-182">Create a new Office 365 group.</span></span> <span data-ttu-id="60f4b-183">Cette applet de commande fournit un ensemble minimal de paramètres pour définir les valeurs des propriétés étendues, utilisez Set-UnifiedGroup après avoir créé le groupe.</span><span class="sxs-lookup"><span data-stu-id="60f4b-183">This cmdlet provides a minimal set of parameters, for setting values for extended properties use Set-UnifiedGroup after creating the new group</span></span>  <br/> |
|[<span data-ttu-id="60f4b-184">Remove-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="60f4b-184">Remove-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616186) <br/> |<span data-ttu-id="60f4b-185">Supprimer un groupe Office 365 existant</span><span class="sxs-lookup"><span data-stu-id="60f4b-185">Delete an existing Office 365 Group</span></span>  <br/> |
|[<span data-ttu-id="60f4b-186">Get-UnifiedGroupLinks</span><span class="sxs-lookup"><span data-stu-id="60f4b-186">Get-UnifiedGroupLinks</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616194) <br/> |<span data-ttu-id="60f4b-187">Récupérer les informations d’appartenance et de propriétaire pour un groupe Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-187">Retrieve membership and owner information for an Office 365 Group</span></span>  <br/> |
|[<span data-ttu-id="60f4b-188">Add-UnifiedGroupLinks</span><span class="sxs-lookup"><span data-stu-id="60f4b-188">Add-UnifiedGroupLinks</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616191) <br/> |<span data-ttu-id="60f4b-189">Ajouter des centaines ou des milliers d’utilisateurs ou de nouveaux propriétaires à un groupe Office 365 existant</span><span class="sxs-lookup"><span data-stu-id="60f4b-189">Add hundred or thousands of users, or new owners, to an existing Office 365 Group</span></span>  <br/> |
|[<span data-ttu-id="60f4b-190">Remove-UnifiedGroupLinks</span><span class="sxs-lookup"><span data-stu-id="60f4b-190">Remove-UnifiedGroupLinks</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616195) <br/> |<span data-ttu-id="60f4b-191">Supprimer des propriétaires et des membres d’un groupe Office 365 existant</span><span class="sxs-lookup"><span data-stu-id="60f4b-191">Remove owners and members from an existing Office 365 Group</span></span>  <br/> |
|[<span data-ttu-id="60f4b-192">Get-applet userphoto</span><span class="sxs-lookup"><span data-stu-id="60f4b-192">Get-UserPhoto</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=536510) <br/> |<span data-ttu-id="60f4b-193">Permet d’afficher des informations sur la photo de l’utilisateur associée à un compte.</span><span class="sxs-lookup"><span data-stu-id="60f4b-193">Used to view information about the user photo associated with an account.</span></span> <span data-ttu-id="60f4b-194">Les photos des utilisateurs sont stockées dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="60f4b-194">User photos are stored in Active Directory</span></span>  <br/> |
|[<span data-ttu-id="60f4b-195">Set-applet userphoto</span><span class="sxs-lookup"><span data-stu-id="60f4b-195">Set-UserPhoto</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=536511) <br/> |<span data-ttu-id="60f4b-196">Utilisé pour associer une photo d’utilisateur à un compte.</span><span class="sxs-lookup"><span data-stu-id="60f4b-196">Used to associate a user photo with an account.</span></span> <span data-ttu-id="60f4b-197">Les photos des utilisateurs sont stockées dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="60f4b-197">User photos are stored in Active Directory</span></span>  <br/> |
|[<span data-ttu-id="60f4b-198">Remove-applet userphoto</span><span class="sxs-lookup"><span data-stu-id="60f4b-198">Remove-UserPhoto</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=536512) <br/> |<span data-ttu-id="60f4b-199">Suppression de la photo d’un groupe Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-199">Remove the photo for an Office 365 group</span></span>  <br/> |

## <a name="related-topics"></a><span data-ttu-id="60f4b-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60f4b-200">Related topics</span></span>

[<span data-ttu-id="60f4b-201">Mettre à niveau des listes de distribution vers des groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-201">Upgrade distribution lists to Office 365 Groups</span></span>](https://docs.microsoft.com/office365/admin/manage/upgrade-distribution-lists)

[<span data-ttu-id="60f4b-202">Gérer les personnes autorisées à créer des groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-202">Manage who can create Office 365 Groups</span></span>](https://docs.microsoft.com/office365/admin/create-groups/manage-creation-of-groups)

[<span data-ttu-id="60f4b-203">Gérer l'accès invité aux groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="60f4b-203">Manage guest access to Office 365 Groups</span></span>](https://support.office.com/article/bfc7a840-868f-4fd6-a390-f347bf51aff6)

[<span data-ttu-id="60f4b-204">Modifier l’appartenance au groupe statique en membre dynamique dans</span><span class="sxs-lookup"><span data-stu-id="60f4b-204">Change static group membership to dynamic in</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-change-type)
