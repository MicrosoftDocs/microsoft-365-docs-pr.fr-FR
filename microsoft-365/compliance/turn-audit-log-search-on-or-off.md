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
ms.openlocfilehash: c5e1106617aa4828ec2db5afcc44ac55e91f2383
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080347"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="c2ee0-105">Activer ou désactiver la recherche dans un journal d’audit Office 365</span><span class="sxs-lookup"><span data-stu-id="c2ee0-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="c2ee0-106">Vous (ou un autre administrateur) devez activer la journalisation d’audit pour pouvoir commencer à rechercher dans le journal d’audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-106">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log.</span></span> <span data-ttu-id="c2ee0-107">Lorsque la recherche du journal d’audit dans le centre de sécurité & conformité est activée, l’activité de l’utilisateur et de l’administrateur de votre organisation est enregistrée dans le journal d’audit et conservée pendant 90 jours.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-107">When audit log search in the Security & Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days.</span></span> <span data-ttu-id="c2ee0-108">Toutefois, il se peut que votre organisation ne souhaite pas enregistrer et conserver les données du journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-108">However, your organization might not want to record and retain audit log data.</span></span> <span data-ttu-id="c2ee0-109">Vous pouvez également utiliser une application de gestion des événements et des informations de sécurité tierces pour accéder à vos données d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-109">Or you might be using a third-party security information and event management (SIEM) application to access your auditing data.</span></span> <span data-ttu-id="c2ee0-110">Dans ce cas, un administrateur global peut désactiver la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-110">In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="c2ee0-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c2ee0-111">Before you begin</span></span>

- <span data-ttu-id="c2ee0-112">Vous devez disposer du rôle journaux d’audit dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-112">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization.</span></span> <span data-ttu-id="c2ee0-113">Par défaut, ce rôle est affecté aux groupes de rôles gestion de la conformité et gestion de l’organisation dans la page **autorisations** du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-113">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="c2ee0-114">Les administrateurs globaux dans Office 365 sont membres du groupe de rôles gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-114">Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="c2ee0-115">Les utilisateurs doivent disposer d’autorisations dans Exchange Online pour activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-115">Users have to be assigned permissions in Exchange Online to turn audit log search on or off.</span></span> <span data-ttu-id="c2ee0-116">Si vous affectez des utilisateurs au rôle journaux d’audit sur la page **autorisations** dans le centre de sécurité & conformité, ils ne pourront pas activer ou désactiver la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-116">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn audit log search on or off.</span></span> <span data-ttu-id="c2ee0-117">Cela est dû au fait que la cmdlet sous-jacente est une applet de commande Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-117">This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="c2ee0-118">Si vous désactivez la recherche dans le journal d’audit dans Office 365, vous ne pourrez pas utiliser l’API activité de gestion d’Office 365 pour accéder aux données d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-118">If you turn off audit log search in Office 365, you won't be able to use the Office 365 Management Activity API to access auditing data for your organization.</span></span> <span data-ttu-id="c2ee0-119">La désactivation de la recherche du journal d’audit en suivant les étapes décrites dans cet article signifie qu’aucun résultat n’est renvoyé lorsque vous effectuez une recherche dans le journal d’audit à l’aide du centre de sécurité & conformité ou lors de l’exécution de la cmdlet **Search-UnifiedAuditLog** dans Exchange Online PowerShell .</span><span class="sxs-lookup"><span data-stu-id="c2ee0-119">Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="c2ee0-120">Cela signifie également que vos journaux d’audit ne seront pas disponibles via l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-120">This also means that your audit logs won't be available through the Office 365 Management Activity API.</span></span>  
    
- <span data-ttu-id="c2ee0-121">Pour obtenir des instructions détaillées sur la recherche dans le journal d’audit Office 365, voir [Search the audit log dans le centre de sécurité & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="c2ee0-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="c2ee0-122">Activer la recherche du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="c2ee0-122">Turn on audit log search</span></span>

<span data-ttu-id="c2ee0-123">Vous pouvez utiliser le centre de sécurité & conformité ou PowerShell pour activer la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-123">You can use the Security & Compliance Center or PowerShell to turn on audit log search in Office 365.</span></span> <span data-ttu-id="c2ee0-124">L’activation de la recherche de journal d’audit peut prendre plusieurs heures avant de pouvoir renvoyer des résultats lors de la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-124">It might take several hours after you turn on audit log search before you can return results when you search the audit log.</span></span> <span data-ttu-id="c2ee0-125">Vous devez disposer du rôle journaux d’audit dans Exchange Online pour activer la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-125">You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security--compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="c2ee0-126">Utiliser le centre de sécurité & conformité pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="c2ee0-126">Use the Security & Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="c2ee0-127">Dans le centre de sécurité & conformité, accédez à recherche dans le **Journal d’audit**de la **recherche** \> .</span><span class="sxs-lookup"><span data-stu-id="c2ee0-127">In the Security & Compliance Center, go to **Search** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="c2ee0-128">Cliquez sur **Démarrer l’enregistrement des activités de l’utilisateur et de l’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Cliquez sur Démarrer l’enregistrement des activités de l’utilisateur et de l’administrateur pour activer l’audit.](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="c2ee0-130">Une boîte de dialogue s’affiche, indiquant que l’activité de l’utilisateur et de l’administrateur dans votre organisation sera enregistrée dans le journal d’audit Office 365 et disponible pour être affichée dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="c2ee0-131">Cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="c2ee0-132">Un message s’affiche indiquant que le journal d’audit est en cours de préparation et que vous pouvez exécuter une recherche dans quelques heures après la fin de la préparation.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="c2ee0-133">Utiliser PowerShell pour activer la recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="c2ee0-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="c2ee0-134">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2ee0-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="c2ee0-135">Exécutez la commande PowerShell suivante pour activer la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="c2ee0-136">Un message s’affiche indiquant que la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="c2ee0-137">Désactiver la recherche de journal d’audit</span><span class="sxs-lookup"><span data-stu-id="c2ee0-137">Turn off audit log search</span></span>

<span data-ttu-id="c2ee0-138">Vous devez utiliser PowerShell à distance connecté à votre organisation Exchange Online pour désactiver la recherche de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-138">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search.</span></span> <span data-ttu-id="c2ee0-139">De la même manière que pour activer la recherche dans le journal d’audit, vous devez disposer du rôle journaux d’audit dans Exchange Online pour désactiver la recherche de journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-139">Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="c2ee0-140">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2ee0-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="c2ee0-141">Exécutez la commande PowerShell suivante pour désactiver la recherche dans le journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="c2ee0-142">Après un certain temps, vérifiez que la recherche dans le journal d’audit est désactivée (désactivée).</span><span class="sxs-lookup"><span data-stu-id="c2ee0-142">After a while, verify that audit log search is turned off (disabled).</span></span> <span data-ttu-id="c2ee0-143">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="c2ee0-143">There are two ways to do this:</span></span>
    
    - <span data-ttu-id="c2ee0-144">Dans PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c2ee0-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="c2ee0-145">La valeur de `False` pour la propriété _UnifiedAuditLogIngestionEnabled_ indique que la recherche du journal d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="c2ee0-146">Dans le centre de sécurité & conformité, accédez **à** \> **recherche dans le journal d’audit**, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-146">In the Security & Compliance Center, go to **Search** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="c2ee0-147">Un message s’affiche indiquant que la recherche du journal d’audit n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="c2ee0-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Un message s’affiche si l’audit est désactivé](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
