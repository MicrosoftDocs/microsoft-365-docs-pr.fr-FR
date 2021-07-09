---
title: Activer ou désactiver la fonctionnalité d’audit
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
ms.custom: seo-marvel-apr2020
description: Comment activer ou désactiver la fonctionnalité de recherche du journal d’audit dans le Centre de conformité Microsoft 365 pour activer ou désactiver la possibilité pour les administrateurs de rechercher dans le journal d’audit.
ms.openlocfilehash: dd39b883036ce6060aef71c6a927c03f391d827f
ms.sourcegitcommit: 5db5047c24b56f3af90c2bc5c830a7a13eeeccad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "53341495"
---
# <a name="turn-auditing-on-or-off"></a><span data-ttu-id="b4122-103">Activer ou désactiver la fonctionnalité d’audit</span><span class="sxs-lookup"><span data-stu-id="b4122-103">Turn auditing on or off</span></span>

<span data-ttu-id="b4122-104">Nous activons par défaut la journalisation d’audit pour les organisations d’entreprise Microsoft 365 et Office 365.</span><span class="sxs-lookup"><span data-stu-id="b4122-104">Audit logging is turned on by default for Microsoft 365 and Office 365 enterprise organizations.</span></span> <span data-ttu-id="b4122-105">Lorsque l’audit dans le Centre de conformité Microsoft 365 est allumé, les activités des utilisateurs et des administrateurs de votre organisation sont enregistrées dans le journal d’audit et conservées pendant 90 jours et jusqu’à un an en fonction de la licence attribuée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b4122-105">When auditing in the Microsoft 365 compliance center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days, and up to one year depending on the license assigned to users.</span></span> <span data-ttu-id="b4122-106">Toutefois, votre organisation peut avoir des raisons de ne pas vouloir enregistrer et conserver les données du journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-106">However, your organization may have reasons for not wanting to record and retain audit log data.</span></span> <span data-ttu-id="b4122-107">Dans ce cas, un administrateur global peut décider de désactiver l’audit dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b4122-107">In those cases, a global admin may decide to turn off auditing in Microsoft 365.</span></span>

<span data-ttu-id="b4122-108">Lors de la configuration d’Microsoft 365 ou Office 365 organisation, vous pouvez vérifier l’état d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4122-108">When setting up a new Microsoft 365 or Office 365 organization, you can verify the auditing status for your organization.</span></span> <span data-ttu-id="b4122-109">Pour obtenir des instructions, consultez la section Vérifier [l’état d’audit](#verify-the-auditing-status-for-your-organization) de votre organisation dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b4122-109">For instructions, see the [Verify the auditing status for your organization](#verify-the-auditing-status-for-your-organization) section in this article.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4122-110">Si vous désactiver l’audit dans Microsoft 365, vous ne pouvez pas utiliser l’API activité de gestion Office 365 ou Azure Sentinel pour accéder aux données d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4122-110">If you turn off auditing in Microsoft 365, you can't use the Office 365 Management Activity API or Azure Sentinel to access auditing data for your organization.</span></span> <span data-ttu-id="b4122-111">La suppression de l’audit en suivant les étapes de cet article signifie qu’aucun résultat ne sera renvoyé lorsque vous effectuerez une recherche dans le journal d’audit à l’aide du Centre de conformité Microsoft 365 ou lorsque vous exécutez la cmdlet **Search-UnifiedAuditLog** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4122-111">Turning off auditing by following the steps in this article means that no results will be returned when you search the audit log using the Microsoft 365 compliance center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="b4122-112">Cela signifie également que les journaux d’audit ne seront pas disponibles via l Office 365 API Activité de gestion ou Azure Sentinel.</span><span class="sxs-lookup"><span data-stu-id="b4122-112">This also means that audit logs won't be available through the Office 365 Management Activity API or Azure Sentinel.</span></span>
  
## <a name="before-you-turn-auditing-on-or-off"></a><span data-ttu-id="b4122-113">Avant d’activer ou de désactiver l’audit</span><span class="sxs-lookup"><span data-stu-id="b4122-113">Before you turn auditing on or off</span></span>

- <span data-ttu-id="b4122-114">Le rôle Journaux d’audit doit vous être attribué dans Exchange Online pour activer ou désactiver l’audit dans Microsoft 365 organisation.</span><span class="sxs-lookup"><span data-stu-id="b4122-114">You have to be assigned the Audit Logs role in Exchange Online to turn auditing on or off in your Microsoft 365 organization.</span></span> <span data-ttu-id="b4122-115">Par défaut, ce rôle est attribué aux groupes de rôles Gestion de la conformité et Gestion de l’organisation dans la page **Autorisations** du Centre d Exchange de conformité.</span><span class="sxs-lookup"><span data-stu-id="b4122-115">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="b4122-116">Les administrateurs globaux Microsoft 365 sont membres du groupe de rôles Gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b4122-116">Global admins in Microsoft 365 are members of the Organization Management role group in Exchange Online.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4122-117">Des autorisations doivent être attribuées aux utilisateurs Exchange Online pour activer ou désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-117">Users have to be assigned permissions in Exchange Online to turn auditing on or off.</span></span> <span data-ttu-id="b4122-118">Si vous attribuez aux utilisateurs le rôle Journaux d’audit sur la page **Autorisations** de la Centre de conformité Microsoft 365, ils ne pourront pas activer ou désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-118">If you assign users the Audit Logs role on the **Permissions** page in the Microsoft 365 compliance center, they won't be able to turn auditing on or off.</span></span> <span data-ttu-id="b4122-119">Cela est dû au fait que l’cmdlet sous-jacente est Exchange Online cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4122-119">This is because the underlying cmdlet is an Exchange Online PowerShell cmdlet.</span></span>

- <span data-ttu-id="b4122-120">Pour obtenir des instructions détaillées sur la recherche dans le journal d’audit, voir [Rechercher dans le journal d’audit.](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="b4122-120">For step-by-step instructions on searching the audit log, see [Search the audit log](search-the-audit-log-in-security-and-compliance.md).</span></span> <span data-ttu-id="b4122-121">Pour plus d’informations sur l’API activité Microsoft 365 gestion des données, voir Prise en [Microsoft 365 API de gestion des données.](/office/office-365-management-api/get-started-with-office-365-management-apis)</span><span class="sxs-lookup"><span data-stu-id="b4122-121">For more information about the Microsoft 365 Management Activity API, see [Get started with Microsoft 365 Management APIs](/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span>

## <a name="verify-the-auditing-status-for-your-organization"></a><span data-ttu-id="b4122-122">Vérifier l’état d’audit de votre organisation</span><span class="sxs-lookup"><span data-stu-id="b4122-122">Verify the auditing status for your organization</span></span>

<span data-ttu-id="b4122-123">Pour vérifier que l’audit est allumé pour votre organisation, vous pouvez exécuter la commande suivante [dans Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="b4122-123">To verify that auditing is turned on for your organization, you can run the following command in [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell):</span></span>

```powershell
Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
```

<span data-ttu-id="b4122-124">La valeur `True` de la propriété  _UnifiedAuditLogIngestionEnabled_ indique que l’audit est allumé.</span><span class="sxs-lookup"><span data-stu-id="b4122-124">A value of `True` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that auditing is turned on.</span></span> <span data-ttu-id="b4122-125">La valeur indique `False` que l’audit n’est pas allumé.</span><span class="sxs-lookup"><span data-stu-id="b4122-125">A value of `False` indicates that auditing is not turned on.</span></span>

## <a name="turn-on-auditing"></a><span data-ttu-id="b4122-126">Activer l’audit</span><span class="sxs-lookup"><span data-stu-id="b4122-126">Turn on auditing</span></span>

<span data-ttu-id="b4122-127">Si l’audit n’est pas allumé pour votre organisation, vous pouvez l’activer dans le Centre de conformité Microsoft 365 ou à l’aide Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4122-127">If auditing is not turned on for your organization, you can turn it on in the Microsoft 365 compliance center or by using Exchange Online PowerShell.</span></span> <span data-ttu-id="b4122-128">L’opération d’audit peut prendre plusieurs heures avant que vous ne renvoyiez des résultats lors de la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-128">It may take several hours after you turn on auditing before you can return results when you search the audit log.</span></span>
  
### <a name="use-the-compliance-center-to-turn-on-auditing"></a><span data-ttu-id="b4122-129">Utiliser le centre de conformité pour activer l’audit</span><span class="sxs-lookup"><span data-stu-id="b4122-129">Use the compliance center to turn on auditing</span></span>

1. <span data-ttu-id="b4122-130">Accédez à <https://compliance.microsoft.com> et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="b4122-130">Go to <https://compliance.microsoft.com> and sign in.</span></span>

2. <span data-ttu-id="b4122-131">Dans le volet de navigation gauche du Centre de conformité Microsoft 365, cliquez sur **Audit.**</span><span class="sxs-lookup"><span data-stu-id="b4122-131">In the left navigation pane of the Microsoft 365 compliance center, click **Audit**.</span></span>

   <span data-ttu-id="b4122-132">Si l’audit n’est pas désactivé pour votre organisation, une bannière s’affiche pour vous invite à commencer à enregistrer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="b4122-132">If auditing is not turned on for your organization, a banner is displayed prompting you start recording user and admin activity.</span></span>

   ![Bannière sur la page Audit](../media/AuditingBanner.png)

3. <span data-ttu-id="b4122-134">Cliquez sur la **bannière Démarrer l’enregistrement de l’activité de l’utilisateur et de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="b4122-134">Click the **Start recording user and admin activity** banner.</span></span>

   <span data-ttu-id="b4122-135">L’application de la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="b4122-135">It may take up to 60 minutes for the change to take effect.</span></span>

### <a name="use-powershell-to-turn-on-auditing"></a><span data-ttu-id="b4122-136">Utiliser PowerShell pour activer l’audit</span><span class="sxs-lookup"><span data-stu-id="b4122-136">Use PowerShell to turn on auditing</span></span>

1. <span data-ttu-id="b4122-137">[Connectez-vous à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="b4122-137">[Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="b4122-138">Exécutez la commande PowerShell suivante pour activer l’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-138">Run the following PowerShell command to turn on auditing.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="b4122-139">Un message s’affiche pour vous dire que l’application de la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="b4122-139">A message is displayed saying that it may take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-auditing"></a><span data-ttu-id="b4122-140">Désactiver l’audit</span><span class="sxs-lookup"><span data-stu-id="b4122-140">Turn off auditing</span></span>

<span data-ttu-id="b4122-141">Vous devez utiliser Exchange Online PowerShell pour désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-141">You have to use Exchange Online PowerShell to turn off auditing.</span></span>
  
1. <span data-ttu-id="b4122-142">[Connectez-vous à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="b4122-142">[Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="b4122-143">Exécutez la commande PowerShell suivante pour désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="b4122-143">Run the following PowerShell command to turn off auditing.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="b4122-144">Après un certain temps, vérifiez que l’audit est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b4122-144">After a while, verify that auditing is turned off (disabled).</span></span> <span data-ttu-id="b4122-145">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="b4122-145">There are two ways to do this:</span></span>

    - <span data-ttu-id="b4122-146">Dans Exchange Online PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b4122-146">In Exchange Online PowerShell, run the following command:</span></span>

      ```powershell
      Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
      ```

      <span data-ttu-id="b4122-147">La valeur de  `False` la  _propriété UnifiedAuditLogIngestionEnabled_ indique que l’audit est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b4122-147">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that auditing is turned off.</span></span>

    - <span data-ttu-id="b4122-148">Go to the **Audit** page in the Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b4122-148">Go to the **Audit** page in the Microsoft 365 compliance center.</span></span>

      <span data-ttu-id="b4122-149">Si l’audit n’est pas désactivé pour votre organisation, une bannière s’affiche pour vous invite à commencer à enregistrer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="b4122-149">If auditing is not turned on for your organization, a banner is displayed prompting you start recording user and admin activity.</span></span>
