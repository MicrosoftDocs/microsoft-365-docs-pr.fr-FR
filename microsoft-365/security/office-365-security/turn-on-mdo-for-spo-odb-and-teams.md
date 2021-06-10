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
ms.openlocfilehash: 07aea9551faa280cd51bda1d57f017e0a24028ea
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204467"
---
# <a name="turn-on-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="5505e-103">Activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5505e-103">Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="5505e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5505e-104">**Applies to**</span></span>
- [<span data-ttu-id="5505e-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="5505e-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="5505e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5505e-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="5505e-107">Microsoft Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span><span class="sxs-lookup"><span data-stu-id="5505e-107">Microsoft Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span></span> <span data-ttu-id="5505e-108">Pour plus d’informations, [voir Pièces jointes SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="5505e-108">For more information, see [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="5505e-109">Cet article contient les étapes d’activation et de configuration des pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5505e-109">This article contains the steps for enabling and configuring Safe Attachments for SharePoint, OneDrive, and Microsoft Teams.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="5505e-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5505e-110">What do you need to know before you begin?</span></span>

- <span data-ttu-id="5505e-111">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="5505e-111">You open the Security & Compliance Center at <https://protection.office.com>.</span></span> <span data-ttu-id="5505e-112">Pour aller directement à la page Pièces **jointes sécurisées ATP,** ouvrez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="5505e-112">To go directly to the **ATP Safe Attachments** page, open <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="5505e-113">Pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, vous  devez être  membre des groupes de rôles Gestion de l’organisation ou Administrateur de la sécurité dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="5505e-113">To turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="5505e-114">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="5505e-114">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="5505e-115">Pour utiliser SharePoint Online PowerShell afin d’empêcher les utilisateurs de télécharger [](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) des fichiers malveillants, vous devez être membre des rôles Administrateur général ou Administrateur [SharePoint](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#sharepoint-administrator) dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5505e-115">To use SharePoint Online PowerShell to prevent people from downloading malicious files, you need to be member of the [Global Administrator](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) or [SharePoint Administrator](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#sharepoint-administrator) roles in Azure AD.</span></span>

- <span data-ttu-id="5505e-116">Vérifiez que la journalisation d’audit est activée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5505e-116">Verify that audit logging is enabled for your organization.</span></span> <span data-ttu-id="5505e-117">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="5505e-117">For more information, see [Turn audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

- <span data-ttu-id="5505e-118">Laissez jusqu’à 30 minutes pour que les paramètres prennent effet.</span><span class="sxs-lookup"><span data-stu-id="5505e-118">Allow up to 30 minutes for the settings to take effect.</span></span>

## <a name="step-1-use-the-security--compliance-center-to-turn-on-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="5505e-119">Étape 1 : utiliser le Centre de sécurité & conformité pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5505e-119">Step 1: Use the Security & Compliance Center to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

1. <span data-ttu-id="5505e-120">Dans le Centre de sécurité &  conformité, allez dans Stratégie de gestion des menaces - Pièces \>  \> **jointes sécurisées**, puis cliquez sur **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="5505e-120">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and click **Global settings**.</span></span>

2. <span data-ttu-id="5505e-121">Dans le volant des **paramètres** globaux qui s’affiche, rendez-vous sur Activer Defender pour Office 365 pour **SharePoint, OneDrive** et Microsoft Teams paramètre.</span><span class="sxs-lookup"><span data-stu-id="5505e-121">In the **Global settings** fly out that appears, go to the **Turn on Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams** setting.</span></span> <span data-ttu-id="5505e-122">Déplacez le basculement vers la droite pour activer les pièces jointes sécurisées pour SharePoint, OneDrive ![ ](../../media/scc-toggle-on.png) et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5505e-122">Move the toggle to the right ![Toggle on](../../media/scc-toggle-on.png) to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams.</span></span>

   <span data-ttu-id="5505e-123">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5505e-123">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-to-turn-on-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="5505e-124">Utilisez Exchange Online PowerShell pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5505e-124">Use Exchange Online PowerShell to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="5505e-125">Si vous préférez utiliser PowerShell pour activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, connectez-vous à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5505e-125">If you'd rather use PowerShell to turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams, [connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) and run the following command:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableATPForSPOTeamsODB $true
```

<span data-ttu-id="5505e-126">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="5505e-126">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span></span>

## <a name="step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files"></a><span data-ttu-id="5505e-127">Étape 2 : (recommandé) Utilisez SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers malveillants</span><span class="sxs-lookup"><span data-stu-id="5505e-127">Step 2: (Recommended) Use SharePoint Online PowerShell to prevent users from downloading malicious files</span></span>

<span data-ttu-id="5505e-128">Par défaut, les utilisateurs ne peuvent pas ouvrir, déplacer, copier ou partager des fichiers malveillants détectés par la atp.</span><span class="sxs-lookup"><span data-stu-id="5505e-128">By default, users can't open, move, copy, or share malicious files that are detected by ATP.</span></span> <span data-ttu-id="5505e-129">Toutefois, ils peuvent supprimer et télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="5505e-129">However, they can delete and download malicious files.</span></span>

<span data-ttu-id="5505e-130">Pour empêcher les utilisateurs de télécharger des fichiers malveillants, connectez-vous [à SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5505e-130">To prevent users from downloading malicious files, [connect to SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) and run the following command:</span></span>

```powershell
Set-SPOTenant -DisallowInfectedFileDownload $true
```

<span data-ttu-id="5505e-131">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="5505e-131">**Notes**:</span></span>

- <span data-ttu-id="5505e-132">Ce paramètre affecte à la fois les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="5505e-132">This setting affects both users and admins.</span></span>
- <span data-ttu-id="5505e-133">Les utilisateurs peuvent toujours supprimer des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="5505e-133">People can still delete malicious files.</span></span>

<span data-ttu-id="5505e-134">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="5505e-134">For detailed syntax and parameter information, see [Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>

## <a name="step-3-recommended-use-the-security--compliance-center-to-create-an-alert-policy-for-detected-files"></a><span data-ttu-id="5505e-135">Étape 3 (recommandé) Utiliser le Centre de sécurité & conformité pour créer une stratégie d’alerte pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="5505e-135">Step 3 (Recommended) Use the Security & Compliance Center to create an alert policy for detected files</span></span>

<span data-ttu-id="5505e-136">Vous pouvez créer une stratégie d’alerte qui vous avertit, ainsi qu’à d’autres administrateurs, lorsque des pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams détectent un fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="5505e-136">You can create an alert policy that notifies you and other admins when Safe Attachments for SharePoint, OneDrive, and Microsoft Teams detects a malicious file.</span></span> <span data-ttu-id="5505e-137">Pour en savoir plus sur les alertes, voir Créer des alertes d’activité dans le Centre de [sécurité & conformité.](../../compliance/create-activity-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="5505e-137">To learn more about alerts, see [Create activity alerts in the Security & Compliance Center](../../compliance/create-activity-alerts.md).</span></span>

1. <span data-ttu-id="5505e-138">Dans le [Centre de sécurité & conformité,](https://protection.office.com)allez aux **stratégies d’alerte des alertes** \>  ou ouvrez <https://protection.office.com/alertpolicies> .</span><span class="sxs-lookup"><span data-stu-id="5505e-138">In the [Security & Compliance Center](https://protection.office.com), go to **Alerts** \> **Alert policies** or open <https://protection.office.com/alertpolicies>.</span></span>

2. <span data-ttu-id="5505e-139">Dans la page **Stratégies d’alerte,** cliquez **sur Nouvelle stratégie d’alerte.**</span><span class="sxs-lookup"><span data-stu-id="5505e-139">On the **Alert policies** page, click **New alert policy**.</span></span>

3. <span data-ttu-id="5505e-140">**L’Assistant Nouvelle stratégie** d’alerte s’ouvre dans un volant. Dans la page **Nom de votre** alerte, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5505e-140">The **New alert policy** wizard opens in a fly out. On the **Name your alert** page, configure the following settings:</span></span>

   - <span data-ttu-id="5505e-141">**Nom**: tapez un nom unique et descriptif.</span><span class="sxs-lookup"><span data-stu-id="5505e-141">**Name**: Type a unique and descriptive name.</span></span> <span data-ttu-id="5505e-142">Par exemple, fichiers malveillants dans les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="5505e-142">For example, Malicious Files in Libraries.</span></span>
   - <span data-ttu-id="5505e-143">**Description**: tapez une description facultative.</span><span class="sxs-lookup"><span data-stu-id="5505e-143">**Description**: Type an optional description.</span></span> <span data-ttu-id="5505e-144">Par exemple, avertit les administrateurs lorsque des fichiers malveillants sont détectés dans SharePoint Online, OneDrive ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5505e-144">For example, Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
   - <span data-ttu-id="5505e-145">**Gravité :** laissez la valeur par défaut **Faible** sélectionnée, ou sélectionnez **Moyenne** ou **Élevée**.</span><span class="sxs-lookup"><span data-stu-id="5505e-145">**Severity**: Leave the default value **Low** selected, or select **Medium** or **High**.</span></span>
   - <span data-ttu-id="5505e-146">**Sélectionnez une catégorie**: sélectionnez **Gestion des menaces.**</span><span class="sxs-lookup"><span data-stu-id="5505e-146">**Select a category**: Select **Threat management**.</span></span>

   <span data-ttu-id="5505e-147">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5505e-147">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="5505e-148">Dans la page **Créer des paramètres d’alerte,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5505e-148">On the **Create alert settings** page, configure the following settings:</span></span>

   - <span data-ttu-id="5505e-149">**Sur quoi voulez-vous alerter ? : l’activité consiste** à sélectionner **les programmes malveillants détectés dans le fichier.**</span><span class="sxs-lookup"><span data-stu-id="5505e-149">**What do you want to alert on?: Activity is**: Select **Detected malware in file**.</span></span>
   - <span data-ttu-id="5505e-150">**Comment voulez-vous que l’alerte** soit déclenchée ? : laissez la valeur par défaut chaque fois qu’une activité correspond à **la règle** sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5505e-150">**How do you want the alert to be triggered?**: Leave the default value **Every time an activity matches the rule** selected.</span></span>

   <span data-ttu-id="5505e-151">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5505e-151">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="5505e-152">Dans la page **Définir vos destinataires,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5505e-152">On the **Set your recipients** page, configure the following settings:</span></span>

   - <span data-ttu-id="5505e-153">**Envoyer des notifications par courrier** électronique : vérifiez que ce paramètre est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5505e-153">**Send email notifications**: Verify this setting is selected.</span></span> <span data-ttu-id="5505e-154">Dans la zone **Destinataires du courrier** électronique, sélectionnez un ou plusieurs administrateurs globaux, administrateurs de sécurité ou lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté.</span><span class="sxs-lookup"><span data-stu-id="5505e-154">In the **Email recipients** box, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span>
   - <span data-ttu-id="5505e-155">**Limite de notification quotidienne**: laissez la valeur par défaut **Aucune** limite sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5505e-155">**Daily notification limit**: Leave the default value **No limit** selected.</span></span>

   <span data-ttu-id="5505e-156">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5505e-156">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="5505e-157">Dans la page **Examiner vos paramètres,** examinez les paramètres, puis cliquez sur Modifier dans l’une des sections pour apporter des modifications. </span><span class="sxs-lookup"><span data-stu-id="5505e-157">On the **Review your settings** page, review the settings, and click **Edit** in any of the sections to make changes.</span></span>

   <span data-ttu-id="5505e-158">Dans la section **Voulez-vous activer** la stratégie immédiatement ? Laissez la valeur par défaut Oui, l’activer **immédiatement** sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5505e-158">In the **Do you want to turn the policy on right away?** section, leave the default value **Yes, turn it on right away** selected.</span></span>

   <span data-ttu-id="5505e-159">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="5505e-159">When you're finished, click **Finish**.</span></span>

### <a name="use-security--compliance-powershell-to-create-an-alert-policy-for-detected-files"></a><span data-ttu-id="5505e-160">Utiliser Security & Compliance PowerShell pour créer une stratégie d’alerte pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="5505e-160">Use Security & Compliance PowerShell to create an alert policy for detected files</span></span>

<span data-ttu-id="5505e-161">Si vous préférez utiliser PowerShell pour créer la même stratégie d’alerte que décrite dans la section précédente, connectez-vous au Centre de sécurité & conformité [PowerShell](/powershell/exchange/connect-to-scc-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5505e-161">If you'd rather use PowerShell to create the same alert policy as described in the previous section, [connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and run the following command:</span></span>

```powershell
New-ActivityAlert -Name "Malicious Files in Libraries" -Description "Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams" -Category ThreatManagement -Operation FileMalwareDetected -NotifyUser "admin1@contoso.com","admin2@contoso.com"
```

<span data-ttu-id="5505e-162">**Remarque**: la valeur _gravité par défaut_ est Faible.</span><span class="sxs-lookup"><span data-stu-id="5505e-162">**Note**: The default _Severity_ value is Low.</span></span> <span data-ttu-id="5505e-163">Pour spécifier Medium ou High, incluez le paramètre _Severity_ et la valeur dans la commande.</span><span class="sxs-lookup"><span data-stu-id="5505e-163">To specify Medium or High, include the _Severity_ parameter and value in the command.</span></span>

<span data-ttu-id="5505e-164">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir New-ActivityAlert.](/powershell/module/exchange/new-activityalert)</span><span class="sxs-lookup"><span data-stu-id="5505e-164">For detailed syntax and parameter information, see [New-ActivityAlert](/powershell/module/exchange/new-activityalert).</span></span>

### <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="5505e-165">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="5505e-165">How do you know these procedures worked?</span></span>

- <span data-ttu-id="5505e-166">Pour vérifier que vous avez bien désactivé les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5505e-166">To verify that you've successfully turned on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams, use either of the following steps:</span></span>

  - <span data-ttu-id="5505e-167">Dans le Centre de sécurité [&](https://protection.office.com)conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments,** select Global **settings**, and verify the value of the **Turn on Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams** setting.</span><span class="sxs-lookup"><span data-stu-id="5505e-167">In the [Security & Compliance Center](https://protection.office.com), go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, select **Global settings**, and verify the value of the **Turn on Defender for Office 365 for SharePoint, OneDrive, and Microsoft Teams** setting.</span></span>

  - <span data-ttu-id="5505e-168">Dans Exchange Online PowerShell, exécutez la commande suivante pour vérifier le paramètre de propriété :</span><span class="sxs-lookup"><span data-stu-id="5505e-168">In Exchange Online PowerShell, run the following command to verify the property setting:</span></span>

    ```powershell
    Get-AtpPolicyForO365 | Format-List EnableATPForSPOTeamsODB
    ```

    <span data-ttu-id="5505e-169">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-AtpPolicyForO365](/powershell/module/exchange/get-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="5505e-169">For detailed syntax and parameter information, see [Get-AtpPolicyForO365](/powershell/module/exchange/get-atppolicyforo365).</span></span>

- <span data-ttu-id="5505e-170">Pour vérifier que vous avez réussi à bloquer le téléchargement de fichiers malveillants, ouvrez SharePoint Online PowerShell et exécutez la commande suivante pour vérifier la valeur de la propriété :</span><span class="sxs-lookup"><span data-stu-id="5505e-170">To verify that you've successfully blocked people from downloading malicious files, open SharePoint Online PowerShell, and run the following command to verify the property value:</span></span>

  ```powershell
  Get-SPOTenant | Format-List DisallowInfectedFileDownload
  ```

  <span data-ttu-id="5505e-171">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="5505e-171">For detailed syntax and parameter information, see [Get-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>

- <span data-ttu-id="5505e-172">Pour vérifier que vous avez correctement configuré une stratégie d’alerte pour les fichiers détectés, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5505e-172">To verify that you've successfully configured an alert policy for detected files, use any of the following steps:</span></span>

  - <span data-ttu-id="5505e-173">Dans le Centre de sécurité & conformité, sélectionnez la stratégie d’alerte dans les **stratégies** d’alerte et vérifiez \>  \> les paramètres.</span><span class="sxs-lookup"><span data-stu-id="5505e-173">In the Security & Compliance Center, go to **Alerts** \> **Alert policies** \> select the alert policy, and verify the settings.</span></span>

  - <span data-ttu-id="5505e-174">Dans le Centre de sécurité & conformité PowerShell, remplacez par le nom de la stratégie d’alerte, exécutez la commande suivante et vérifiez les valeurs \<AlertPolicyName\> des propriétés :</span><span class="sxs-lookup"><span data-stu-id="5505e-174">In Security & Compliance Center PowerShell, replace \<AlertPolicyName\> with the name of the alert policy, run the following command, and verify the property values:</span></span>

    ```powershell
    Get-ActivityAlert -Identity "<AlertPolicyName>"
    ```

    <span data-ttu-id="5505e-175">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-ActivityAlert](/powershell/module/exchange/get-activityalert).</span><span class="sxs-lookup"><span data-stu-id="5505e-175">For detailed syntax and parameter information, see [Get-ActivityAlert](/powershell/module/exchange/get-activityalert).</span></span>

- <span data-ttu-id="5505e-176">Utilisez le [rapport d’état de la protection](view-email-security-reports.md#threat-protection-status-report) contre les menaces pour afficher les informations sur les fichiers détectés dans SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5505e-176">Use the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report) to view information about detected files in SharePoint, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="5505e-177">Plus précisément, vous pouvez utiliser l’affichage des données **par : Affichage des programmes \> malveillants** de contenu.</span><span class="sxs-lookup"><span data-stu-id="5505e-177">Specifically, you can use the **View data by: Content \> Malware** view.</span></span>