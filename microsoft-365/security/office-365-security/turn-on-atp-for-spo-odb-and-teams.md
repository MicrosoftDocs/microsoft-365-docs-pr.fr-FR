---
title: Activer l’ATP Office 365-SharePoint, OneDrive & teams
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
- SPO_Content
description: Découvrez comment activer la protection avancée contre les menaces pour SharePoint, OneDrive et Teams, y compris comment définir des alertes pour les fichiers détectés.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 1cd345ae74b81c23f92b9e9b7d712efa8b875503
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48326900"
---
# <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="7fe73-103">Activer PACM pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7fe73-103">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="7fe73-104">Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive et Microsoft teams protège votre organisation contre le partage accidentel de fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="7fe73-104">Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive, and Microsoft Teams protects your organization from inadvertently sharing malicious files.</span></span> <span data-ttu-id="7fe73-105">Pour plus d’informations, reportez-vous à la rubrique [ATP pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="7fe73-105">For more information, see [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="7fe73-106">Cet article décrit la procédure d’activation et de configuration de la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7fe73-106">This article contains the steps for enabling and configuring ATP for SharePoint, OneDrive, and Microsoft Teams.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7fe73-107">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7fe73-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7fe73-108">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="7fe73-108">You open the Security & Compliance Center at <https://protection.office.com>.</span></span> <span data-ttu-id="7fe73-109">Pour accéder directement à la page **pièces jointes approuvées ATP** , ouvrez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="7fe73-109">To go directly to the **ATP Safe Attachments** page, open <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="7fe73-110">Pour activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="7fe73-110">To turn on ATP for SharePoint, OneDrive, and Microsoft Teams, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center.</span></span> <span data-ttu-id="7fe73-111">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="7fe73-111">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="7fe73-112">Pour utiliser SharePoint Online PowerShell afin d’empêcher les utilisateurs de télécharger des fichiers malveillants, vous devez être membre des rôles administrateur [général](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) ou [administrateur SharePoint](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#sharepoint-administrator) dans Azure ad.</span><span class="sxs-lookup"><span data-stu-id="7fe73-112">To use SharePoint Online PowerShell to prevent people from downloading malicious files, you need to be member of the [Global Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-administrator--company-administrator) or [SharePoint Administrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#sharepoint-administrator) roles in Azure AD.</span></span>

- <span data-ttu-id="7fe73-113">Vérifiez que la journalisation d’audit est activée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7fe73-113">Verify that audit logging is enabled for your organization.</span></span> <span data-ttu-id="7fe73-114">Pour plus d’informations, voir [Activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="7fe73-114">For more information, see [Turn audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

- <span data-ttu-id="7fe73-115">Autorisez jusqu’à 30 minutes pour que les paramètres prennent effet.</span><span class="sxs-lookup"><span data-stu-id="7fe73-115">Allow up to 30 minutes for the settings to take effect.</span></span>

## <a name="step-1-use-the-security--compliance-center-to-turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="7fe73-116">Étape 1 : utiliser le centre de sécurité & conformité pour activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="7fe73-116">Step 1: Use the Security & Compliance Center to turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

1. <span data-ttu-id="7fe73-117">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \> **Policy** \> **pièces jointes ATP**et cliquez sur **paramètres globaux**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-117">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and click **Global settings**.</span></span>

2. <span data-ttu-id="7fe73-118">Dans les **paramètres globaux** , sélectionnez le passage à la sortie qui s’affiche, puis cliquez sur le paramètre Activer la protection avancée contre les menaces **pour SharePoint, OneDrive et Microsoft teams** .</span><span class="sxs-lookup"><span data-stu-id="7fe73-118">In the **Global settings** fly out that appears, go to the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** setting.</span></span> <span data-ttu-id="7fe73-119">Déplacez le bouton bascule vers la droite sur Activer pour activer la protection avancée contre les menaces ![ ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7fe73-119">Move the toggle to the right ![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) to turn on ATP for SharePoint, OneDrive, and Microsoft Teams.</span></span>

   <span data-ttu-id="7fe73-120">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-120">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-to-turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="7fe73-121">Utiliser Exchange Online PowerShell pour activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="7fe73-121">Use Exchange Online PowerShell to turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="7fe73-122">Si vous préférez utiliser PowerShell pour activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams, [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7fe73-122">If you'd rather use PowerShell to turn on ATP for SharePoint, OneDrive, and Microsoft Teams, [connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) and run the following command:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableATPForSPOTeamsODB $true
```

<span data-ttu-id="7fe73-123">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="7fe73-123">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

## <a name="step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files"></a><span data-ttu-id="7fe73-124">Étape 2 : (recommandé) utiliser SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers malveillants</span><span class="sxs-lookup"><span data-stu-id="7fe73-124">Step 2: (Recommended) Use SharePoint Online PowerShell to prevent users from downloading malicious files</span></span>

<span data-ttu-id="7fe73-125">Par défaut, les utilisateurs ne peuvent pas ouvrir, déplacer, copier ou partager des fichiers malveillants détectés par la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="7fe73-125">By default, users can't open, move, copy, or share malicious files that are detected by ATP.</span></span> <span data-ttu-id="7fe73-126">Toutefois, ils peuvent supprimer et télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="7fe73-126">However, they can delete and download malicious files.</span></span>

<span data-ttu-id="7fe73-127">Pour empêcher les utilisateurs de télécharger des fichiers malveillants, [Connectez-vous à SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7fe73-127">To prevent users from downloading malicious files, [connect to SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) and run the following command:</span></span>

```powershell
Set-SPOTenant -DisallowInfectedFileDownload $true
```

<span data-ttu-id="7fe73-128">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="7fe73-128">**Notes**:</span></span>

- <span data-ttu-id="7fe73-129">Ce paramètre affecte les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="7fe73-129">This setting affects both users and admins.</span></span>
- <span data-ttu-id="7fe73-130">Les utilisateurs peuvent toujours supprimer des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="7fe73-130">People can still delete malicious files.</span></span>

<span data-ttu-id="7fe73-131">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="7fe73-131">For detailed syntax and parameter information, see [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>

## <a name="step-3-recommended-use-the-security--compliance-center-to-create-an-alert-policy-for-detected-files"></a><span data-ttu-id="7fe73-132">Étape 3 (recommandé) utiliser le centre de sécurité & conformité pour créer une stratégie d’alerte pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="7fe73-132">Step 3 (Recommended) Use the Security & Compliance Center to create an alert policy for detected files</span></span>

<span data-ttu-id="7fe73-133">Vous pouvez créer une stratégie d’alerte qui vous avertit, ainsi que d’autres administrateurs, lorsque la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams détecte un fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="7fe73-133">You can create an alert policy that notifies you and other admins when ATP for SharePoint, OneDrive, and Microsoft Teams detects a malicious file.</span></span> <span data-ttu-id="7fe73-134">Pour en savoir plus sur les alertes, voir [créer des alertes d’activité dans le centre de sécurité & conformité](../../compliance/create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="7fe73-134">To learn more about alerts, see [Create activity alerts in the Security & Compliance Center](../../compliance/create-activity-alerts.md).</span></span>

1. <span data-ttu-id="7fe73-135">Dans le [Centre de sécurité & conformité](https://protection.office.com), accédez à **alertes** d' \> **alerte** ou ouvrez <https://protection.office.com/alertpolicies> .</span><span class="sxs-lookup"><span data-stu-id="7fe73-135">In the [Security & Compliance Center](https://protection.office.com), go to **Alerts** \> **Alert policies** or open <https://protection.office.com/alertpolicies>.</span></span>

2. <span data-ttu-id="7fe73-136">Sur la page **stratégies d’alerte** , cliquez sur **nouvelle stratégie d’alerte**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-136">On the **Alert policies** page, click **New alert policy**.</span></span>

3. <span data-ttu-id="7fe73-137">L’Assistant **nouvelle stratégie d’alerte** s’ouvre en un passage. Sur la page **nommer votre alerte** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fe73-137">The **New alert policy** wizard opens in a fly out. On the **Name your alert** page, configure the following settings:</span></span>

   - <span data-ttu-id="7fe73-138">**Nom**: tapez un nom unique et descriptif.</span><span class="sxs-lookup"><span data-stu-id="7fe73-138">**Name**: Type a unique and descriptive name.</span></span> <span data-ttu-id="7fe73-139">Par exemple, des fichiers malveillants dans les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="7fe73-139">For example, Malicious Files in Libraries.</span></span>
   - <span data-ttu-id="7fe73-140">**Description**: tapez une description facultative.</span><span class="sxs-lookup"><span data-stu-id="7fe73-140">**Description**: Type an optional description.</span></span> <span data-ttu-id="7fe73-141">Par exemple, avertir les administrateurs lorsque des fichiers malveillants sont détectés dans SharePoint Online, OneDrive ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7fe73-141">For example, Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
   - <span data-ttu-id="7fe73-142">**Gravité**: laissez la valeur par défaut **faible** sélectionnée ou sélectionnez **moyenne** ou **élevée**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-142">**Severity**: Leave the default value **Low** selected, or select **Medium** or **High**.</span></span>
   - <span data-ttu-id="7fe73-143">**Sélectionnez une catégorie**: sélectionnez **gestion des menaces**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-143">**Select a category**: Select **Threat management**.</span></span>

   <span data-ttu-id="7fe73-144">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-144">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="7fe73-145">Sur la page **créer des paramètres d’alerte** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fe73-145">On the **Create alert settings** page, configure the following settings:</span></span>

   - <span data-ttu-id="7fe73-146">**Sur quoi souhaitez-vous alerter ?: activité**: sélectionnez **programmes malveillants détectés dans le fichier**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-146">**What do you want to alert on?: Activity is**: Select **Detected malware in file**.</span></span>
   - <span data-ttu-id="7fe73-147">**Comment voulez-vous que l’alerte soit déclenchée ?**: conservez la valeur par défaut **chaque fois qu’une activité correspond à la règle** sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7fe73-147">**How do you want the alert to be triggered?**: Leave the default value **Every time an activity matches the rule** selected.</span></span>

   <span data-ttu-id="7fe73-148">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-148">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="7fe73-149">Sur la page **définir vos destinataires** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fe73-149">On the **Set your recipients** page, configure the following settings:</span></span>

   - <span data-ttu-id="7fe73-150">**Envoyer des notifications par courrier électronique**: Vérifiez que ce paramètre est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7fe73-150">**Send email notifications**: Verify this setting is selected.</span></span> <span data-ttu-id="7fe73-151">Dans la zone **destinataires du message** , sélectionnez un ou plusieurs administrateurs globaux, administrateurs de sécurité ou lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté.</span><span class="sxs-lookup"><span data-stu-id="7fe73-151">In the **Email recipients** box, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span>
   - <span data-ttu-id="7fe73-152">**Limite quotidienne des notifications**: laissez la valeur par défaut **aucune limite** sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7fe73-152">**Daily notification limit**: Leave the default value **No limit** selected.</span></span>

   <span data-ttu-id="7fe73-153">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-153">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="7fe73-154">Sur la page **vérifier vos paramètres** , passez en revue les paramètres, puis cliquez sur **modifier** dans n’importe quelle section pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="7fe73-154">On the **Review your settings** page, review the settings, and click **Edit** in any of the sections to make changes.</span></span>

   <span data-ttu-id="7fe73-155">Dans la section souhaitez **-vous activer la stratégie immédiatement ?** , conservez la valeur par défaut **Oui, activez-** la immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7fe73-155">In the **Do you want to turn the policy on right away?** section, leave the default value **Yes, turn it on right away** selected.</span></span>

   <span data-ttu-id="7fe73-156">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="7fe73-156">When you're finished, click **Finish**.</span></span>

### <a name="use-security--compliance-powershell-to-create-an-alert-policy-for-detected-files"></a><span data-ttu-id="7fe73-157">Utiliser la sécurité & PowerShell de conformité pour créer une stratégie d’alerte pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="7fe73-157">Use Security & Compliance PowerShell to create an alert policy for detected files</span></span>

<span data-ttu-id="7fe73-158">Si vous préférez utiliser PowerShell pour créer la même stratégie d’alerte que celle décrite dans la section précédente, [Connectez-vous au centre de sécurité & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7fe73-158">If you'd rather use PowerShell to create the same alert policy as described in the previous section, [connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell) and run the following command:</span></span>

```powershell
New-ActivityAlert -Name "Malicious Files in Libraries" -Description "Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams" -Category ThreatManagement -Operation FileMalwareDetected -NotifyUser "admin1@contoso.com","admin2@contoso.com"
```

<span data-ttu-id="7fe73-159">**Remarque**: la valeur de _gravité_ par défaut est faible.</span><span class="sxs-lookup"><span data-stu-id="7fe73-159">**Note**: The default _Severity_ value is Low.</span></span> <span data-ttu-id="7fe73-160">Pour spécifier une valeur moyenne ou élevée, incluez le paramètre de _gravité_ et la valeur dans la commande.</span><span class="sxs-lookup"><span data-stu-id="7fe73-160">To specify Medium or High, include the _Severity_ parameter and value in the command.</span></span>

<span data-ttu-id="7fe73-161">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-ActivityAlert](https://docs.microsoft.com/powershell/module/exchange/new-activityalert).</span><span class="sxs-lookup"><span data-stu-id="7fe73-161">For detailed syntax and parameter information, see [New-ActivityAlert](https://docs.microsoft.com/powershell/module/exchange/new-activityalert).</span></span>

### <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="7fe73-162">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="7fe73-162">How do you know these procedures worked?</span></span>

- <span data-ttu-id="7fe73-163">Pour vérifier que vous avez bien activé la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7fe73-163">To verify that you've successfully turned on ATP for SharePoint, OneDrive, and Microsoft Teams, use either of the following steps:</span></span>

  - <span data-ttu-id="7fe73-164">Dans le [Centre de sécurité & conformité](https://protection.office.com), accédez à la stratégie de **gestion des menaces** \> **Policy** \> **pièces jointes approuvées ATP**, sélectionnez **paramètres globaux**et vérifiez la valeur du paramètre **activer l’ATP pour SharePoint, OneDrive et Microsoft teams** .</span><span class="sxs-lookup"><span data-stu-id="7fe73-164">In the [Security & Compliance Center](https://protection.office.com), go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, select **Global settings**, and verify the value of the **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams** setting.</span></span>

  - <span data-ttu-id="7fe73-165">Dans Exchange Online PowerShell, exécutez la commande suivante pour vérifier le paramètre de la propriété :</span><span class="sxs-lookup"><span data-stu-id="7fe73-165">In Exchange Online PowerShell, run the following command to verify the property setting:</span></span>

    ```powershell
    Get-AtpPolicyForO365 | Format-List EnableATPForSPOTeamsODB
    ```

    <span data-ttu-id="7fe73-166">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/get-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="7fe73-166">For detailed syntax and parameter information, see [Get-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/get-atppolicyforo365).</span></span>

- <span data-ttu-id="7fe73-167">Pour vérifier que vous avez bien bloqué le téléchargement de fichiers malveillants, ouvrez SharePoint Online PowerShell et exécutez la commande suivante pour vérifier la valeur de la propriété :</span><span class="sxs-lookup"><span data-stu-id="7fe73-167">To verify that you've successfully blocked people from downloading malicious files, open SharePoint Online PowerShell, and run the following command to verify the property value:</span></span>

  ```powershell
  Get-SPOTenant | Format-List DisallowInfectedFileDownload
  ```

  <span data-ttu-id="7fe73-168">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="7fe73-168">For detailed syntax and parameter information, see [Get-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>

- <span data-ttu-id="7fe73-169">Pour vérifier que vous avez bien configuré une stratégie d’alerte pour les fichiers détectés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7fe73-169">To verify that you've successfully configured an alert policy for detected files, use any of the following steps:</span></span>

  - <span data-ttu-id="7fe73-170">Dans le centre de sécurité & conformité, accédez à **alertes** \> **Alert Policies** \> , sélectionnez la stratégie d’alerte et vérifiez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="7fe73-170">In the Security & Compliance Center, go to **Alerts** \> **Alert policies** \> select the alert policy, and verify the settings.</span></span>

  - <span data-ttu-id="7fe73-171">Dans sécurité & Centre de conformité PowerShell, remplacez \<AlertPolicyName\> par le nom de la stratégie d’alerte, exécutez la commande suivante et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="7fe73-171">In Security & Compliance Center PowerShell, replace \<AlertPolicyName\> with the name of the alert policy, run the following command, and verify the property values:</span></span>

    ```powershell
    Get-ActivityAlert -Identity "<AlertPolicyName>"
    ```

    <span data-ttu-id="7fe73-172">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-ActivityAlert](https://docs.microsoft.com/powershell/module/exchange/get-activityalert).</span><span class="sxs-lookup"><span data-stu-id="7fe73-172">For detailed syntax and parameter information, see [Get-ActivityAlert](https://docs.microsoft.com/powershell/module/exchange/get-activityalert).</span></span>

- <span data-ttu-id="7fe73-173">Utilisez le [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report) pour afficher les informations sur les fichiers détectés dans SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7fe73-173">Use the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report) to view information about detected files in SharePoint, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="7fe73-174">Plus précisément, vous pouvez utiliser l’affichage **des données en : affichage des \> programmes malveillants de contenu** .</span><span class="sxs-lookup"><span data-stu-id="7fe73-174">Specifically, you can use the **View data by: Content \> Malware** view.</span></span>
