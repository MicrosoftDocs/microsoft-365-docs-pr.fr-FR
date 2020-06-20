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
description: Comment activer ou désactiver la fonctionnalité de recherche de journal d’audit dans le centre de sécurité & conformité afin d’activer ou de désactiver la capacité des administrateurs à rechercher dans le journal d’audit.
ms.openlocfilehash: 4571c90c4fa680acd8925e83e32ffcf07de7d626
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819134"
---
# <a name="turn-audit-log-search-on-or-off"></a><span data-ttu-id="0d1c0-103">Activer ou désactiver la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0d1c0-103">Turn audit log search on or off</span></span>

<span data-ttu-id="0d1c0-104">Vous (ou un autre administrateur) devez activer la journalisation d’audit pour pouvoir commencer à rechercher dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-104">You (or another admin) must turn on audit logging before you can start searching the audit log.</span></span> <span data-ttu-id="0d1c0-105">Lorsque la recherche du journal d’audit dans le centre de sécurité & conformité est activée, l’activité de l’utilisateur et de l’administrateur de votre organisation est enregistrée dans le journal d’audit et conservée pendant 90 jours, et jusqu’à un an en fonction de la licence attribuée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-105">When audit log search in the Security & Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days, and up to one year depending on the license assigned to users.</span></span> <span data-ttu-id="0d1c0-106">Toutefois, votre organisation peut avoir des raisons de ne pas vouloir enregistrer et conserver les données du journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-106">However, your organization may have reasons for not wanting to record and retain audit log data.</span></span> <span data-ttu-id="0d1c0-107">Dans ce cas, un administrateur général peut décider de désactiver l’audit dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-107">In those cases, a global admin may decide to turn off auditing in Microsoft 365.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d1c0-108">Si vous désactivez la recherche de journal d’audit dans Microsoft 365, vous ne pouvez pas utiliser l’API activité de gestion d’Office 365 ou Azure sentinelle pour accéder aux données d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-108">If you turn off audit log search in Microsoft 365, you can't use the Office 365 Management Activity API or Azure Sentinel to access auditing data for your organization.</span></span> <span data-ttu-id="0d1c0-109">La désactivation de la recherche du journal d’audit en suivant les étapes décrites dans cet article signifie qu’aucun résultat n’est renvoyé lorsque vous effectuez une recherche dans le journal d’audit à l’aide du centre de sécurité & conformité ou lorsque vous exécutez la cmdlet **Search-UnifiedAuditLog** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-109">Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="0d1c0-110">Cela signifie également que les journaux d’audit ne seront pas disponibles via l’API activité de gestion d’Office 365 ou Azure sentinelle.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-110">This also means that audit logs won't be available through the Office 365 Management Activity API or Azure Sentinel.</span></span>
  
## <a name="before-you-turn-audit-log-search-on-or-off"></a><span data-ttu-id="0d1c0-111">Avant d’activer ou de désactiver la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0d1c0-111">Before you turn audit log search on or off</span></span>

- <span data-ttu-id="0d1c0-112">Vous devez disposer du rôle journaux d’audit dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit dans votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-112">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Microsoft 365 organization.</span></span> <span data-ttu-id="0d1c0-113">Par défaut, ce rôle est affecté aux groupes de rôles gestion de la conformité et gestion de l’organisation dans la page **autorisations** du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-113">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="0d1c0-114">Les administrateurs globaux de Microsoft 365 sont membres du groupe de rôles gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-114">Global admins in Microsoft 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="0d1c0-115">Les utilisateurs doivent disposer d’autorisations dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-115">Users have to be assigned permissions in Exchange Online to turn audit log search on or off.</span></span> <span data-ttu-id="0d1c0-116">Si vous affectez des utilisateurs au rôle journaux d’audit sur la page **autorisations** dans le centre de sécurité & conformité, ils ne pourront pas activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-116">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn audit log search on or off.</span></span> <span data-ttu-id="0d1c0-117">Cela est dû au fait que la cmdlet sous-jacente est une applet de commande Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-117">This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
    
- <span data-ttu-id="0d1c0-118">Pour obtenir des instructions détaillées sur la recherche dans le journal d’audit, voir [Search the audit log dans le centre de sécurité & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="0d1c0-118">For step-by-step instructions on searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> <span data-ttu-id="0d1c0-119">Pour plus d’informations sur l’API activité de gestion de Microsoft 365, reportez-vous à la rubrique [prise en main des API de gestion microsoft 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="0d1c0-119">For more information about the Microsoft 365 Management Activity API, see [Get started with Microsoft 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="0d1c0-120">Activer la recherche du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0d1c0-120">Turn on audit log search</span></span>

<span data-ttu-id="0d1c0-121">Vous pouvez utiliser le centre de sécurité & conformité ou PowerShell pour activer la recherche dans le journal d’audit dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-121">You can use the Security & Compliance Center or PowerShell to turn on audit log search in Microsoft 365.</span></span> <span data-ttu-id="0d1c0-122">L’activation de la recherche de journal d’audit peut prendre plusieurs heures avant de pouvoir renvoyer des résultats lors de la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-122">It may take several hours after you turn on audit log search before you can return results when you search the audit log.</span></span> <span data-ttu-id="0d1c0-123">Vous devez disposer du rôle journaux d’audit dans Exchange Online pour activer la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-123">You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security--compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="0d1c0-124">Utiliser le centre de sécurité & conformité pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0d1c0-124">Use the Security & Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="0d1c0-125">[Accédez au centre de sécurité & conformité](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-125">[Go to the Security & Compliance Center](https://protection.office.com) and sign in.</span></span>

2. <span data-ttu-id="0d1c0-126">Dans le centre de sécurité & conformité, accédez **Search** à recherche dans le \> **Journal d’audit**de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-126">In the Security & Compliance Center, go to **Search** \> **Audit log search**.</span></span>

   <span data-ttu-id="0d1c0-127">Une bannière s’affiche indiquant que l’audit doit être activé pour enregistrer l’activité de l’utilisateur et de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-127">A banner is displayed saying that auditing has to be turned on to record user and admin activity.</span></span>

3. <span data-ttu-id="0d1c0-128">Cliquez sur **activer l’audit**.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-128">Click **Turn on auditing**.</span></span>

    ![Cliquez sur Activer l’audit](../media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="0d1c0-130">La bannière est mise à jour pour indiquer que le journal d’audit est en cours de préparation et que vous pouvez rechercher l’activité de l’utilisateur et de l’administrateur en quelques heures.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-130">The banner is updated to say the audit log is being prepared and that you can search for user and admin activity in a few hours.</span></span>

### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="0d1c0-131">Utiliser PowerShell pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0d1c0-131">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="0d1c0-132">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d1c0-132">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)

2. <span data-ttu-id="0d1c0-133">Exécutez la commande PowerShell suivante pour activer la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-133">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="0d1c0-134">Un message s’affiche indiquant que la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-134">A message is displayed saying that it may take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="0d1c0-135">Désactiver la recherche de journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0d1c0-135">Turn off audit log search</span></span>

<span data-ttu-id="0d1c0-136">Vous devez utiliser PowerShell à distance connecté à votre organisation Exchange Online pour désactiver la recherche de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-136">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search.</span></span> <span data-ttu-id="0d1c0-137">De la même manière que pour activer la recherche dans le journal d’audit, vous devez disposer du rôle journaux d’audit dans Exchange Online pour désactiver la recherche de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-137">Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="0d1c0-138">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d1c0-138">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)

2. <span data-ttu-id="0d1c0-139">Exécutez la commande PowerShell suivante pour désactiver la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-139">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="0d1c0-140">Après un certain temps, vérifiez que la recherche dans le journal d’audit est désactivée (désactivée).</span><span class="sxs-lookup"><span data-stu-id="0d1c0-140">After a while, verify that audit log search is turned off (disabled).</span></span> <span data-ttu-id="0d1c0-141">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="0d1c0-141">There are two ways to do this:</span></span>

    - <span data-ttu-id="0d1c0-142">Dans PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0d1c0-142">In PowerShell, run the following command:</span></span>

    ```powershell
    Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
    ```

      <span data-ttu-id="0d1c0-143">La valeur de `False` pour la propriété _UnifiedAuditLogIngestionEnabled_ indique que la recherche du journal d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-143">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 

    - <span data-ttu-id="0d1c0-144">Dans le [Centre de sécurité & conformité](https://protection.office.com), accédez **Search** à recherche dans le \> **Journal d’audit**de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-144">In the [Security & Compliance Center](https://protection.office.com), go to **Search** \> **Audit log search**.</span></span>

      <span data-ttu-id="0d1c0-145">Une bannière s’affiche indiquant que l’audit doit être activé pour enregistrer l’activité de l’utilisateur et de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0d1c0-145">A banner is displayed saying that auditing has to be turned on in order to record user and admin activity.</span></span>