---
title: Activer ou désactiver la recherche dans un journal d’audit Office 365
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
description: Vous pouvez activer la fonctionnalité de recherche de journal d’audit dans le centre de sécurité & conformité. Si vous changez d’avis, vous pouvez le désactiver à tout moment. Lorsque le paramètre de recherche du journal d’audit est désactivé, les administrateurs ne peuvent pas rechercher dans le journal d’audit Office 365 des activités de l’utilisateur et de l’administrateur dans votre organisation.
ms.openlocfilehash: 4e382c9916a9460d2c837a336607734427416a1a
ms.sourcegitcommit: 1d376287f6c1bf5174873e89ed4bf7bb15bc13f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38685958"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="0893f-105">Activer ou désactiver la recherche dans un journal d’audit Office 365</span><span class="sxs-lookup"><span data-stu-id="0893f-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="0893f-106">Vous (ou un autre administrateur) devez activer la journalisation d’audit pour pouvoir commencer à rechercher dans le journal d’audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-106">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log.</span></span> <span data-ttu-id="0893f-107">Lorsque la recherche du journal d’audit dans le centre de sécurité & conformité est activée, l’activité de l’utilisateur et de l’administrateur de votre organisation est enregistrée dans le journal d’audit et conservée pendant 90 jours.</span><span class="sxs-lookup"><span data-stu-id="0893f-107">When audit log search in the Security & Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days.</span></span> <span data-ttu-id="0893f-108">Toutefois, il se peut que votre organisation ne souhaite pas enregistrer et conserver les données du journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-108">However, your organization may not want to record and retain audit log data.</span></span> <span data-ttu-id="0893f-109">Vous pouvez également utiliser une application de gestion des événements et des informations de sécurité tierces pour accéder à vos données d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-109">Or you may be using a third-party security information and event management (SIEM) application to access your auditing data.</span></span> <span data-ttu-id="0893f-110">Dans ce cas, un administrateur global peut désactiver la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-110">In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="0893f-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0893f-111">Before you begin</span></span>

- <span data-ttu-id="0893f-112">Vous devez disposer du rôle journaux d’audit dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-112">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization.</span></span> <span data-ttu-id="0893f-113">Par défaut, ce rôle est affecté aux groupes de rôles gestion de la conformité et gestion de l’organisation dans la page **autorisations** du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="0893f-113">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="0893f-114">Les administrateurs globaux dans Office 365 sont membres du groupe de rôles gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0893f-114">Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="0893f-115">Les utilisateurs doivent disposer d’autorisations dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-115">Users have to be assigned permissions in Exchange Online to turn audit log search on or off.</span></span> <span data-ttu-id="0893f-116">Si vous affectez des utilisateurs au rôle journaux d’audit sur la page **autorisations** dans le centre de sécurité & conformité, ils ne pourront pas activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-116">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn audit log search on or off.</span></span> <span data-ttu-id="0893f-117">Cela est dû au fait que la cmdlet sous-jacente est une applet de commande Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0893f-117">This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="0893f-118">Si vous désactivez la recherche dans le journal d’audit dans Office 365, vous ne pouvez pas utiliser l’API activité de gestion d’Office 365 pour accéder aux données d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0893f-118">If you turn off audit log search in Office 365, you can't use the Office 365 Management Activity API to access auditing data for your organization.</span></span> <span data-ttu-id="0893f-119">La désactivation de la recherche du journal d’audit en suivant les étapes décrites dans cet article signifie qu’aucun résultat n’est renvoyé lorsque vous effectuez une recherche dans le journal d’audit à l’aide du centre de sécurité & conformité ou lorsque vous exécutez la cmdlet **Search-UnifiedAuditLog** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0893f-119">Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="0893f-120">Cela signifie également que vos journaux d’audit ne seront pas disponibles via l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-120">This also means that your audit logs won't be available through the Office 365 Management Activity API.</span></span>  
    
- <span data-ttu-id="0893f-121">Pour obtenir des instructions détaillées sur la recherche dans le journal d’audit Office 365, voir [Search the audit log dans le centre de sécurité & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="0893f-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="0893f-122">Activer la recherche du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0893f-122">Turn on audit log search</span></span>

<span data-ttu-id="0893f-123">Vous pouvez utiliser le centre de sécurité & conformité ou PowerShell pour activer la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-123">You can use the Security & Compliance Center or PowerShell to turn on audit log search in Office 365.</span></span> <span data-ttu-id="0893f-124">L’activation de la recherche de journal d’audit peut prendre plusieurs heures avant de pouvoir renvoyer des résultats lors de la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-124">It may take several hours after you turn on audit log search before you can return results when you search the audit log.</span></span> <span data-ttu-id="0893f-125">Vous devez disposer du rôle journaux d’audit dans Exchange Online pour activer la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-125">You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security--compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="0893f-126">Utiliser le centre de sécurité & conformité pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0893f-126">Use the Security & Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="0893f-127">Dans le centre de sécurité & conformité, accédez à recherche dans le **Journal d’audit**de la **recherche** \> .</span><span class="sxs-lookup"><span data-stu-id="0893f-127">In the Security & Compliance Center, go to **Search** \> **Audit log search**.</span></span>
    
   <span data-ttu-id="0893f-128">Une bannière s’affiche indiquant que l’audit doit être activé pour enregistrer l’activité de l’utilisateur et de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0893f-128">A banner is displayed saying that auditing has to be turned on to record user and admin activity.</span></span>

2. <span data-ttu-id="0893f-129">Cliquez sur **activer l’audit**.</span><span class="sxs-lookup"><span data-stu-id="0893f-129">Click **Turn on auditing**.</span></span>
    
    ![Cliquez sur Activer l’audit](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="0893f-131">La bannière est mise à jour pour indiquer que le journal d’audit est en cours de préparation et que vous pouvez rechercher l’activité de l’utilisateur et de l’administrateur en quelques heures.</span><span class="sxs-lookup"><span data-stu-id="0893f-131">The banner is updated to say the audit log is being prepared and that you can search for user and admin activity in a few hours.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="0893f-132">Utiliser PowerShell pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0893f-132">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="0893f-133">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="0893f-133">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="0893f-134">Exécutez la commande PowerShell suivante pour activer la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-134">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="0893f-135">Un message s’affiche indiquant que la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="0893f-135">A message is displayed saying that it may take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="0893f-136">Désactiver la recherche de journal d’audit</span><span class="sxs-lookup"><span data-stu-id="0893f-136">Turn off audit log search</span></span>

<span data-ttu-id="0893f-137">Vous devez utiliser PowerShell à distance connecté à votre organisation Exchange Online pour désactiver la recherche de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-137">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search.</span></span> <span data-ttu-id="0893f-138">De la même manière que pour activer la recherche dans le journal d’audit, vous devez disposer du rôle journaux d’audit dans Exchange Online pour désactiver la recherche de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="0893f-138">Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="0893f-139">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="0893f-139">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="0893f-140">Exécutez la commande PowerShell suivante pour désactiver la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0893f-140">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="0893f-141">Après un certain temps, vérifiez que la recherche dans le journal d’audit est désactivée (désactivée).</span><span class="sxs-lookup"><span data-stu-id="0893f-141">After a while, verify that audit log search is turned off (disabled).</span></span> <span data-ttu-id="0893f-142">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="0893f-142">There are two ways to do this:</span></span>
    
    - <span data-ttu-id="0893f-143">Dans PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0893f-143">In PowerShell, run the following command:</span></span>

    ```powershell
    Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
    ```

      <span data-ttu-id="0893f-144">La valeur de `False` pour la propriété _UnifiedAuditLogIngestionEnabled_ indique que la recherche du journal d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0893f-144">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="0893f-145">Dans le centre de sécurité & conformité, accédez à recherche dans le **Journal d’audit**de la **recherche** \> .</span><span class="sxs-lookup"><span data-stu-id="0893f-145">In the Security & Compliance Center, go to **Search** \> **Audit log search**.</span></span>
    
      <span data-ttu-id="0893f-146">Une bannière s’affiche indiquant que l’audit doit être activé pour enregistrer l’activité de l’utilisateur et de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0893f-146">A banner is displayed saying that auditing has to be turned on in order to record user and admin activity.</span></span>
