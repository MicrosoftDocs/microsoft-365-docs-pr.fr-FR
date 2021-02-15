---
title: Activer ou désactiver la recherche dans le journal d’audit
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
description: Comment activer ou désactiver la fonctionnalité de recherche du journal d’audit dans le Centre de sécurité & conformité pour activer ou désactiver la possibilité pour les administrateurs de rechercher dans le journal d’audit.
ms.openlocfilehash: 1f3da9671b9e5287d715a438a11b0a0eef164584
ms.sourcegitcommit: 162c01dfaa2fdb3225ce4c24964c1065ce22ed5d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2021
ms.locfileid: "49976327"
---
# <a name="turn-audit-log-search-on-or-off"></a><span data-ttu-id="45bed-103">Activer ou désactiver la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="45bed-103">Turn audit log search on or off</span></span>

<span data-ttu-id="45bed-104">Nous activons par défaut la journalisation d’audit pour les organisations d’entreprise Microsoft 365 et Office 365.</span><span class="sxs-lookup"><span data-stu-id="45bed-104">Audit logging is turned on by default for Microsoft 365 and Office 365 enterprise organizations.</span></span> <span data-ttu-id="45bed-105">Cela inclut les organisations disposant d’abonnements E3/G3 ou E5/G5.</span><span class="sxs-lookup"><span data-stu-id="45bed-105">This includes organizations with E3/G3 or E5/G5 subscriptions.</span></span> <span data-ttu-id="45bed-106">Lorsque la recherche dans le journal d’audit dans le centre de conformité est désactivée, les activités des utilisateurs et des administrateurs de votre organisation sont enregistrées dans le journal d’audit et conservées pendant 90 jours, et jusqu’à un an en fonction de la licence attribuée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="45bed-106">When audit log search in the compliance center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days, and up to one year depending on the license assigned to users.</span></span> <span data-ttu-id="45bed-107">Toutefois, votre organisation peut avoir des raisons de ne pas vouloir enregistrer et conserver les données du journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="45bed-107">However, your organization may have reasons for not wanting to record and retain audit log data.</span></span> <span data-ttu-id="45bed-108">Dans ce cas, un administrateur global peut décider de désactiver l’audit dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="45bed-108">In those cases, a global admin may decide to turn off auditing in Microsoft 365.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45bed-109">Si vous désactiver la recherche dans le journal d’audit dans Microsoft 365, vous ne pouvez pas utiliser l’API Activité de gestion Office 365 ou Azure Sentinel pour accéder aux données d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="45bed-109">If you turn off audit log search in Microsoft 365, you can't use the Office 365 Management Activity API or Azure Sentinel to access auditing data for your organization.</span></span> <span data-ttu-id="45bed-110">La suppression de la recherche dans le journal d’audit en suivant les étapes de cet article signifie qu’aucun résultat ne sera renvoyé lorsque vous effectuerez une recherche dans le journal d’audit à l’aide du Centre de sécurité & conformité ou lorsque vous exécutez la cmdlet **Search-UnifiedAuditLog** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-110">Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="45bed-111">Cela signifie également que les journaux d’audit ne seront pas disponibles via l’API Activité de gestion Office 365 ou Azure Sentinel.</span><span class="sxs-lookup"><span data-stu-id="45bed-111">This also means that audit logs won't be available through the Office 365 Management Activity API or Azure Sentinel.</span></span>
  
## <a name="before-you-turn-audit-log-search-on-or-off"></a><span data-ttu-id="45bed-112">Avant d’activer ou de désactiver la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="45bed-112">Before you turn audit log search on or off</span></span>

- <span data-ttu-id="45bed-113">Vous devez avoir le rôle Journaux d’audit dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit dans votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="45bed-113">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Microsoft 365 organization.</span></span> <span data-ttu-id="45bed-114">Par défaut, ce rôle est affecté aux groupes de rôles Gestion de la conformité et Gestion de l’organisation dans la page **Autorisations** du Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="45bed-114">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="45bed-115">Les administrateurs globaux dans Microsoft 365 sont membres du groupe de rôles Gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="45bed-115">Global admins in Microsoft 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="45bed-116">Des autorisations doivent être attribuées aux utilisateurs dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="45bed-116">Users have to be assigned permissions in Exchange Online to turn audit log search on or off.</span></span> <span data-ttu-id="45bed-117">Si vous attribuez aux utilisateurs le rôle Journaux d’audit sur la page **Autorisations** du Centre de sécurité & conformité, ils ne pourront pas activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="45bed-117">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn audit log search on or off.</span></span> <span data-ttu-id="45bed-118">Cela est dû au fait que la cmdlet sous-jacente est une cmdlet Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-118">This is because the underlying cmdlet is an Exchange Online PowerShell cmdlet.</span></span> 
    
- <span data-ttu-id="45bed-119">Pour obtenir des instructions détaillées sur la recherche dans le journal d’audit, consultez la recherche dans le journal d’audit dans le Centre de sécurité [& conformité.](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="45bed-119">For step-by-step instructions on searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> <span data-ttu-id="45bed-120">Pour plus d’informations sur l’API Activité de gestion Microsoft 365, voir Prise en charge des API de gestion [Microsoft 365.](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)</span><span class="sxs-lookup"><span data-stu-id="45bed-120">For more information about the Microsoft 365 Management Activity API, see [Get started with Microsoft 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span>

- <span data-ttu-id="45bed-121">Pour vérifier que vous avez activé la recherche dans le journal d’audit, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="45bed-121">To verify that audit log search is turned on, you can run the following command in Exchange Online PowerShell:</span></span>

    ```powershell
    Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
    ```

    <span data-ttu-id="45bed-122">La valeur de  `True` la  _propriété UnifiedAuditLogIngestionEnabled_ indique que la recherche dans le journal d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="45bed-122">The value of  `True` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned on.</span></span> 
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="45bed-123">Activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="45bed-123">Turn on audit log search</span></span>

<span data-ttu-id="45bed-124">Si la recherche dans le journal d’audit n’est pas désactivée pour votre organisation, vous pouvez l’activer dans le centre de conformité ou à l’aide d’Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-124">If audit log search is not turned on for your organization, you can turn it on in the compliance center or by using Exchange Online PowerShell.</span></span> <span data-ttu-id="45bed-125">L’ouverture de la recherche dans le journal d’audit peut prendre plusieurs heures avant de pouvoir renvoyer des résultats lors de la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="45bed-125">It may take several hours after you turn on audit log search before you can return results when you search the audit log.</span></span>
  
### <a name="use-the-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="45bed-126">Utiliser le centre de conformité pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="45bed-126">Use the compliance center to turn on audit log search</span></span>

1. <span data-ttu-id="45bed-127">[Go to the compliance center](https://protection.office.com) and sign in.</span><span class="sxs-lookup"><span data-stu-id="45bed-127">[Go to the compliance center](https://protection.office.com) and sign in.</span></span>

2. <span data-ttu-id="45bed-128">Dans le centre de conformité, allez à la recherche **dans** le journal  >  **d’audit de recherche.**</span><span class="sxs-lookup"><span data-stu-id="45bed-128">In the compliance center, go to **Search** > **Audit log search**.</span></span>

   <span data-ttu-id="45bed-129">Si la recherche dans le journal d’audit n’est pas désactivée pour votre organisation, une bannière s’affiche pour vous dire que l’audit doit être allumé pour enregistrer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="45bed-129">If audit log search is not turned on for your organization, a banner is displayed saying that auditing has to be turned on to record user and admin activity.</span></span>

3. <span data-ttu-id="45bed-130">Cliquez **sur Activer l’audit.**</span><span class="sxs-lookup"><span data-stu-id="45bed-130">Click **Turn on auditing**.</span></span>

    ![Cliquez sur Activer l’audit](../media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="45bed-132">La bannière est mise à jour pour dire que le journal d’audit est en cours de préparation et que vous pouvez rechercher l’activité des utilisateurs et des administrateurs dans quelques heures.</span><span class="sxs-lookup"><span data-stu-id="45bed-132">The banner is updated to say the audit log is being prepared and that you can search for user and admin activity in a few hours.</span></span>

### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="45bed-133">Utiliser PowerShell pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="45bed-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="45bed-134">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="45bed-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)

2. <span data-ttu-id="45bed-135">Exécutez la commande PowerShell suivante pour activer la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="45bed-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="45bed-136">Un message s’affiche pour vous dire que l’application de la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="45bed-136">A message is displayed saying that it may take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="45bed-137">Désactiver la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="45bed-137">Turn off audit log search</span></span>

<span data-ttu-id="45bed-138">Vous devez utiliser Exchange Online PowerShell pour désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="45bed-138">You have to use Exchange Online PowerShell to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="45bed-139">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="45bed-139">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)

2. <span data-ttu-id="45bed-140">Exécutez la commande PowerShell suivante pour désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="45bed-140">Run the following PowerShell command to turn off audit log search.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="45bed-141">Après un certain temps, vérifiez que la recherche dans le journal d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="45bed-141">After a while, verify that audit log search is turned off (disabled).</span></span> <span data-ttu-id="45bed-142">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="45bed-142">There are two ways to do this:</span></span>

    - <span data-ttu-id="45bed-143">Dans Exchange Online PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="45bed-143">In Exchange Online PowerShell, run the following command:</span></span>

      ```powershell
      Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
      ```

      <span data-ttu-id="45bed-144">La valeur de  `False` la  _propriété UnifiedAuditLogIngestionEnabled_ indique que la recherche dans le journal d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="45bed-144">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 

    - <span data-ttu-id="45bed-145">Dans le centre [de conformité,](https://protection.office.com)allez à la recherche **dans** le journal \> **d’audit de recherche.**</span><span class="sxs-lookup"><span data-stu-id="45bed-145">In the [compliance center](https://protection.office.com), go to **Search** \> **Audit log search**.</span></span>

      <span data-ttu-id="45bed-146">Une bannière s’affiche pour vous dire que l’audit doit être allumé pour enregistrer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="45bed-146">A banner is displayed saying that auditing has to be turned on in order to record user and admin activity.</span></span>
