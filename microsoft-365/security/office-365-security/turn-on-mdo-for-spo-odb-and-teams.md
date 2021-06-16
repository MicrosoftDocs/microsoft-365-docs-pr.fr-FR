---
title: Activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.date: ''
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
- SPO_Content
description: Les administrateurs peuvent apprendre à activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, notamment comment définir des alertes pour les fichiers détectés.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: a654db40e5dec8d23d07ec7455216fe4e0a8c0e7
ms.sourcegitcommit: ac3e9ccb7b43a42e600af8f44e6f30019533faeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2021
ms.locfileid: "52933010"
---
# <a name="turn-on-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="8eec4-103">Activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8eec4-103">Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8eec4-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8eec4-104">**Applies to**</span></span>
- [<span data-ttu-id="8eec4-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="8eec4-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="8eec4-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8eec4-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="8eec4-107">Microsoft Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span><span class="sxs-lookup"><span data-stu-id="8eec4-107">Microsoft Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span></span> <span data-ttu-id="8eec4-108">Pour plus d’informations, [voir Pièces jointes SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="8eec4-108">For more information, see [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="8eec4-109">Cet article contient les étapes d’activation et de configuration des pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8eec4-109">This article contains the steps for enabling and configuring Safe Attachments for SharePoint, OneDrive, and Microsoft Teams.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8eec4-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8eec4-110">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8eec4-111">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="8eec4-111">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="8eec4-112">Pour aller directement à la page **Pièces jointes sécurisées,** ouvrez <https://security.microsoft.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="8eec4-112">To go directly to the **Safe Attachments** page, open <https://security.microsoft.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="8eec4-113">Pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, vous devez  être  membre des groupes de rôles Gestion de l’organisation ou Administrateur de la sécurité dans le portail Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8eec4-113">To turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="8eec4-114">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="8eec4-114">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="8eec4-115">Pour utiliser SharePoint Online PowerShell afin d’empêcher les utilisateurs de télécharger [](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) des fichiers malveillants, vous devez être membre des rôles Administrateur général ou Administrateur [SharePoint](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#sharepoint-administrator) dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8eec4-115">To use SharePoint Online PowerShell to prevent people from downloading malicious files, you need to be member of the [Global Administrator](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) or [SharePoint Administrator](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#sharepoint-administrator) roles in Azure AD.</span></span>

- <span data-ttu-id="8eec4-116">Vérifiez que la journalisation d’audit est activée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8eec4-116">Verify that audit logging is enabled for your organization.</span></span> <span data-ttu-id="8eec4-117">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="8eec4-117">For more information, see [Turn audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

- <span data-ttu-id="8eec4-118">Laissez jusqu’à 30 minutes pour que les paramètres prennent effet.</span><span class="sxs-lookup"><span data-stu-id="8eec4-118">Allow up to 30 minutes for the settings to take effect.</span></span>

## <a name="step-1-use-the-microsoft-365-defender-portal-to-turn-on-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="8eec4-119">Étape 1 : utiliser le portail Microsoft 365 Defender pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8eec4-119">Step 1: Use the Microsoft 365 Defender portal to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

1. <span data-ttu-id="8eec4-120">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** section Safe \>  \> **Attachments**.</span><span class="sxs-lookup"><span data-stu-id="8eec4-120">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="8eec4-121">Dans la page **Pièces jointes sécurisées,** cliquez **sur Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="8eec4-121">On the **Safe Attachments** page, click **Global settings**.</span></span>

3. <span data-ttu-id="8eec4-122">Dans la **section Paramètres globaux** qui **s’affiche,** rendez-vous dans la section Protéger SharePoint, OneDrive et Microsoft Teams protection.</span><span class="sxs-lookup"><span data-stu-id="8eec4-122">In the **Global settings** fly out that appears, go to the **Protect files in SharePoint, OneDrive, and Microsoft Teams** section.</span></span>

   <span data-ttu-id="8eec4-123">Déplacez le basculement Activer Defender pour Office 365 pour **SharePoint, OneDrive** et Microsoft Teams sur le basculement droit pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et ![ ](../../media/scc-toggle-on.png) Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8eec4-123">Move the **Turn on Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams** toggle to the right ![Toggle on](../../media/scc-toggle-on.png) to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams.</span></span>

   <span data-ttu-id="8eec4-124">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8eec4-124">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-to-turn-on-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="8eec4-125">Utilisez Exchange Online PowerShell pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8eec4-125">Use Exchange Online PowerShell to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="8eec4-126">Si vous préférez utiliser PowerShell pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8eec4-126">If you'd rather use PowerShell to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) and run the following command:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableATPForSPOTeamsODB $true
```

<span data-ttu-id="8eec4-127">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="8eec4-127">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span></span>

## <a name="step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files"></a><span data-ttu-id="8eec4-128">Étape 2 : (recommandé) Utilisez SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers malveillants</span><span class="sxs-lookup"><span data-stu-id="8eec4-128">Step 2: (Recommended) Use SharePoint Online PowerShell to prevent users from downloading malicious files</span></span>

<span data-ttu-id="8eec4-129">Par défaut, les utilisateurs ne peuvent pas ouvrir, déplacer, copier ou partager des fichiers malveillants détectés par des pièces jointes sécurisées pour SharePoint, OneDrive et <sup>\*</sup> Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8eec4-129">By default, users can't open, move, copy, or share<sup>\*</sup> malicious files that are detected by Safe Attachments for SharePoint, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="8eec4-130">Toutefois, ils peuvent supprimer et télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="8eec4-130">However, they can delete and download malicious files.</span></span>

<span data-ttu-id="8eec4-131"><sup>\*</sup> Si les utilisateurs **accèdent à Gérer l’accès,** l’option **Partager** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="8eec4-131"><sup>\*</sup> If users go to **Manage access**, the **Share** option is still available.</span></span>

<span data-ttu-id="8eec4-132">Pour empêcher les utilisateurs de télécharger des fichiers malveillants, connectez-vous [à SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8eec4-132">To prevent users from downloading malicious files, [connect to SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) and run the following command:</span></span>

```powershell
Set-SPOTenant -DisallowInfectedFileDownload $true
```

<span data-ttu-id="8eec4-133">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="8eec4-133">**Notes**:</span></span>

- <span data-ttu-id="8eec4-134">Ce paramètre affecte à la fois les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="8eec4-134">This setting affects both users and admins.</span></span>
- <span data-ttu-id="8eec4-135">Les utilisateurs peuvent toujours supprimer des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="8eec4-135">People can still delete malicious files.</span></span>

<span data-ttu-id="8eec4-136">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="8eec4-136">For detailed syntax and parameter information, see [Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>

## <a name="step-3-recommended-use-the-microsoft-365-defender-portal-to-create-an-alert-policy-for-detected-files"></a><span data-ttu-id="8eec4-137">Étape 3 (recommandé) Utiliser le portail Microsoft 365 Defender pour créer une stratégie d’alerte pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="8eec4-137">Step 3 (Recommended) Use the Microsoft 365 Defender portal to create an alert policy for detected files</span></span>

<span data-ttu-id="8eec4-138">Vous pouvez créer une stratégie d’alerte qui vous avertit, ainsi qu’à d’autres administrateurs, lorsque des pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams détectent un fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="8eec4-138">You can create an alert policy that notifies you and other admins when Safe Attachments for SharePoint, OneDrive, and Microsoft Teams detects a malicious file.</span></span> <span data-ttu-id="8eec4-139">Pour en savoir plus sur les alertes, voir Créer des alertes d’activité dans [le portail Microsoft 365 Defender.](../../compliance/create-activity-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="8eec4-139">To learn more about alerts, see [Create activity alerts in the Microsoft 365 Defender portal](../../compliance/create-activity-alerts.md).</span></span>

1. <span data-ttu-id="8eec4-140">Dans le portail Microsoft 365 Defender, allez à **Stratégies &** \> **Stratégies d’alerte** ou ouvrez <https://security.microsoft.com/alertpolicies> .</span><span class="sxs-lookup"><span data-stu-id="8eec4-140">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Alert policy** or open <https://security.microsoft.com/alertpolicies>.</span></span>

2. <span data-ttu-id="8eec4-141">Dans la page **Stratégie d’alerte,** cliquez **sur Nouvelle stratégie d’alerte.**</span><span class="sxs-lookup"><span data-stu-id="8eec4-141">On the **Alert policy** page, click **New alert policy**.</span></span>

3. <span data-ttu-id="8eec4-142">**L’Assistant Nouvelle stratégie** d’alerte s’ouvre dans un volant. Dans la page **Nom de votre** alerte, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8eec4-142">The **New alert policy** wizard opens in a fly out. On the **Name your alert** page, configure the following settings:</span></span>
   - <span data-ttu-id="8eec4-143">**Nom**: tapez un nom unique et descriptif.</span><span class="sxs-lookup"><span data-stu-id="8eec4-143">**Name**: Type a unique and descriptive name.</span></span> <span data-ttu-id="8eec4-144">Par exemple, fichiers malveillants dans les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="8eec4-144">For example, Malicious Files in Libraries.</span></span>
   - <span data-ttu-id="8eec4-145">**Description**: tapez une description facultative.</span><span class="sxs-lookup"><span data-stu-id="8eec4-145">**Description**: Type an optional description.</span></span> <span data-ttu-id="8eec4-146">Par exemple, avertit les administrateurs lorsque des fichiers malveillants sont détectés dans SharePoint Online, OneDrive ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8eec4-146">For example, Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
   - <span data-ttu-id="8eec4-147">**Gravité :** sélectionnez **Faible,** **Moyen** ou **Élevé** dans la liste de listes.</span><span class="sxs-lookup"><span data-stu-id="8eec4-147">**Severity**: Select **Low**, **Medium**, or **High** from the drop down list.</span></span>
   - <span data-ttu-id="8eec4-148">**Catégorie :** sélectionnez **La gestion des menaces** dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="8eec4-148">**Category**: Select **Threat management** from the drop down list.</span></span>

   <span data-ttu-id="8eec4-149">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8eec4-149">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="8eec4-150">Dans la page **Créer des paramètres d’alerte,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8eec4-150">On the **Create alert settings** page, configure the following settings:</span></span>
   - <span data-ttu-id="8eec4-151">**Sur quoi voulez-vous alerter ?** \> **l’activité de section** consiste à sélectionner les programmes \> **malveillants détectés dans le fichier** dans la liste de listes.</span><span class="sxs-lookup"><span data-stu-id="8eec4-151">**What do you want to alert on?** section \> **Activity is** \> Select **Detected malware in file** from the drop down list.</span></span>
   - <span data-ttu-id="8eec4-152">**Comment voulez-vous que l’alerte soit déclenchée ?** section : laissez la valeur par défaut **chaque fois qu’une activité correspond à la règle** sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8eec4-152">**How do you want the alert to be triggered?** section: Leave the default value **Every time an activity matches the rule** selected.</span></span>

   <span data-ttu-id="8eec4-153">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8eec4-153">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="8eec4-154">Dans la page **Définir vos destinataires,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8eec4-154">On the **Set your recipients** page, configure the following settings:</span></span>
   - <span data-ttu-id="8eec4-155">Vérifiez **que les notifications d’envoi** par courrier électronique sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="8eec4-155">Verify **Send email notifications** is selected.</span></span> <span data-ttu-id="8eec4-156">Dans la zone **Destinataires de** l’e-mail, sélectionnez un ou plusieurs administrateurs globaux, administrateurs de sécurité ou lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté.</span><span class="sxs-lookup"><span data-stu-id="8eec4-156">In the **Email recipients** box, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span>
   - <span data-ttu-id="8eec4-157">**Limite de notification quotidienne**: laissez la valeur par défaut **Aucune** limite sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8eec4-157">**Daily notification limit**: Leave the default value **No limit** selected.</span></span>

   <span data-ttu-id="8eec4-158">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8eec4-158">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="8eec4-159">Dans la page **Passer en revue vos paramètres,** examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="8eec4-159">On the **Review your settings** page, review your settings.</span></span> <span data-ttu-id="8eec4-160">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="8eec4-160">You can select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="8eec4-161">Vous pouvez également cliquer sur **Précédent** ou sélectionner la page spécifique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="8eec4-161">Or you can click **Back** or select the specific page in the wizard.</span></span>

   <span data-ttu-id="8eec4-162">Dans la section **Voulez-vous activer** la stratégie immédiatement ? Laissez la valeur par défaut Oui, l’activer **immédiatement** sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8eec4-162">In the **Do you want to turn the policy on right away?** section, leave the default value **Yes, turn it on right away** selected.</span></span>

   <span data-ttu-id="8eec4-163">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="8eec4-163">When you're finished, click **Finish**.</span></span>

### <a name="use-security--compliance-powershell-to-create-an-alert-policy-for-detected-files"></a><span data-ttu-id="8eec4-164">Utiliser Security & Compliance PowerShell pour créer une stratégie d’alerte pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="8eec4-164">Use Security & Compliance PowerShell to create an alert policy for detected files</span></span>

<span data-ttu-id="8eec4-165">Si vous préférez utiliser PowerShell pour créer la même stratégie d’alerte que décrite dans la section précédente, connectez-vous au Centre de sécurité & conformité [PowerShell](/powershell/exchange/connect-to-scc-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8eec4-165">If you'd rather use PowerShell to create the same alert policy as described in the previous section, [connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and run the following command:</span></span>

```powershell
New-ActivityAlert -Name "Malicious Files in Libraries" -Description "Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams" -Category ThreatManagement -Operation FileMalwareDetected -NotifyUser "admin1@contoso.com","admin2@contoso.com"
```

<span data-ttu-id="8eec4-166">**Remarque**: la valeur _gravité par défaut_ est Faible.</span><span class="sxs-lookup"><span data-stu-id="8eec4-166">**Note**: The default _Severity_ value is Low.</span></span> <span data-ttu-id="8eec4-167">Pour spécifier Medium ou High, incluez le paramètre _Severity_ et la valeur dans la commande.</span><span class="sxs-lookup"><span data-stu-id="8eec4-167">To specify Medium or High, include the _Severity_ parameter and value in the command.</span></span>

<span data-ttu-id="8eec4-168">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-ActivityAlert](/powershell/module/exchange/new-activityalert).</span><span class="sxs-lookup"><span data-stu-id="8eec4-168">For detailed syntax and parameter information, see [New-ActivityAlert](/powershell/module/exchange/new-activityalert).</span></span>

### <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="8eec4-169">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="8eec4-169">How do you know these procedures worked?</span></span>

- <span data-ttu-id="8eec4-170">Pour vérifier que vous avez bien désactivé les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8eec4-170">To verify that you've successfully turned on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams, use either of the following steps:</span></span>

  - <span data-ttu-id="8eec4-171">Dans le portail Microsoft 365 Defender, go to **Policies & rules** Threat Policies section Threat \> **Policies** section \>  Safe \> **Attachments,** select Global **settings**, and verify the value of the **Turn on Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams** setting.</span><span class="sxs-lookup"><span data-stu-id="8eec4-171">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Policies** section \> **Safe Attachments**, select **Global settings**, and verify the value of the **Turn on Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams** setting.</span></span>

  - <span data-ttu-id="8eec4-172">Dans Exchange Online PowerShell, exécutez la commande suivante pour vérifier le paramètre de propriété :</span><span class="sxs-lookup"><span data-stu-id="8eec4-172">In Exchange Online PowerShell, run the following command to verify the property setting:</span></span>

    ```powershell
    Get-AtpPolicyForO365 | Format-List EnableATPForSPOTeamsODB
    ```

    <span data-ttu-id="8eec4-173">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-AtpPolicyForO365](/powershell/module/exchange/get-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="8eec4-173">For detailed syntax and parameter information, see [Get-AtpPolicyForO365](/powershell/module/exchange/get-atppolicyforo365).</span></span>

- <span data-ttu-id="8eec4-174">Pour vérifier que vous avez réussi à bloquer le téléchargement de fichiers malveillants, ouvrez SharePoint Online PowerShell et exécutez la commande suivante pour vérifier la valeur de la propriété :</span><span class="sxs-lookup"><span data-stu-id="8eec4-174">To verify that you've successfully blocked people from downloading malicious files, open SharePoint Online PowerShell, and run the following command to verify the property value:</span></span>

  ```powershell
  Get-SPOTenant | Format-List DisallowInfectedFileDownload
  ```

  <span data-ttu-id="8eec4-175">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="8eec4-175">For detailed syntax and parameter information, see [Get-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>

- <span data-ttu-id="8eec4-176">Pour vérifier que vous avez correctement configuré une stratégie d’alerte pour les fichiers détectés, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8eec4-176">To verify that you've successfully configured an alert policy for detected files, use any of the following steps:</span></span>
  - <span data-ttu-id="8eec4-177">Dans le portail Microsoft 365 Defender, sélectionnez **Stratégies &** Stratégie d’alerte Sélectionnez la stratégie d’alerte et vérifiez \>  \> les paramètres.</span><span class="sxs-lookup"><span data-stu-id="8eec4-177">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Alert policy** \> select the alert policy, and verify the settings.</span></span>
  - <span data-ttu-id="8eec4-178">Dans Microsoft 365 Defender PowerShell, remplacez-le par le nom de la stratégie d’alerte, exécutez la commande suivante et vérifiez les valeurs \<AlertPolicyName\> des propriétés :</span><span class="sxs-lookup"><span data-stu-id="8eec4-178">In Microsoft 365 Defender portal PowerShell, replace \<AlertPolicyName\> with the name of the alert policy, run the following command, and verify the property values:</span></span>

    ```powershell
    Get-ActivityAlert -Identity "<AlertPolicyName>"
    ```

    <span data-ttu-id="8eec4-179">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-ActivityAlert](/powershell/module/exchange/get-activityalert).</span><span class="sxs-lookup"><span data-stu-id="8eec4-179">For detailed syntax and parameter information, see [Get-ActivityAlert](/powershell/module/exchange/get-activityalert).</span></span>

- <span data-ttu-id="8eec4-180">Utilisez le [rapport d’état de la protection](view-email-security-reports.md#threat-protection-status-report) contre les menaces pour afficher les informations sur les fichiers détectés dans SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8eec4-180">Use the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report) to view information about detected files in SharePoint, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="8eec4-181">Plus précisément, vous pouvez utiliser l’affichage des données **par : Affichage des programmes \> malveillants** de contenu.</span><span class="sxs-lookup"><span data-stu-id="8eec4-181">Specifically, you can use the **View data by: Content \> Malware** view.</span></span>
