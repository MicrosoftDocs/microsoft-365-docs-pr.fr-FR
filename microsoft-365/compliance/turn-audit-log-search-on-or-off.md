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
description: Comment activer ou désactiver la fonctionnalité de recherche du journal d’audit dans le centre de conformité Microsoft 365 pour activer ou désactiver la possibilité pour les administrateurs d’effectuer des recherches dans le journal d’audit.
ms.openlocfilehash: 457f453b001f71a095bc60932c8e0cebf46aa7b1
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706663"
---
# <a name="turn-auditing-on-or-off"></a><span data-ttu-id="110cb-103">Activer ou désactiver la fonctionnalité d’audit</span><span class="sxs-lookup"><span data-stu-id="110cb-103">Turn auditing on or off</span></span>

<span data-ttu-id="110cb-104">Nous activons par défaut la journalisation d’audit pour les organisations d’entreprise Microsoft 365 et Office 365.</span><span class="sxs-lookup"><span data-stu-id="110cb-104">Audit logging is turned on by default for Microsoft 365 and Office 365 enterprise organizations.</span></span> <span data-ttu-id="110cb-105">Cela inclut les organisations disposant d’abonnements E3/G3 ou E5/G5.</span><span class="sxs-lookup"><span data-stu-id="110cb-105">This includes organizations with E3/G3 or E5/G5 subscriptions.</span></span> <span data-ttu-id="110cb-106">Lorsque l’audit dans le centre de conformité est allumé, les activités des utilisateurs et des administrateurs de votre organisation sont enregistrées dans le journal d’audit et conservées pendant 90 jours et jusqu’à un an en fonction de la licence attribuée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="110cb-106">When auditing in the compliance center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days, and up to one year depending on the license assigned to users.</span></span> <span data-ttu-id="110cb-107">Toutefois, votre organisation peut avoir des raisons de ne pas vouloir enregistrer et conserver les données du journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="110cb-107">However, your organization may have reasons for not wanting to record and retain audit log data.</span></span> <span data-ttu-id="110cb-108">Dans ce cas, un administrateur global peut décider de désactiver l’audit dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="110cb-108">In those cases, a global admin may decide to turn off auditing in Microsoft 365.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="110cb-109">Si vous désactiver l’audit dans Microsoft 365, vous ne pouvez pas utiliser l’API activité de gestion Office 365 ou Azure Sentinel pour accéder aux données d’audit de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="110cb-109">If you turn off auditing in Microsoft 365, you can't use the Office 365 Management Activity API or Azure Sentinel to access auditing data for your organization.</span></span> <span data-ttu-id="110cb-110">La suppression de l’audit en suivant les étapes de cet article signifie qu’aucun résultat ne sera renvoyé lorsque vous effectuerez une recherche dans le journal d’audit à l’aide du Centre de sécurité & conformité ou lorsque vous exécutez la cmdlet **Search-UnifiedAuditLog** dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="110cb-110">Turning off auditing by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="110cb-111">Cela signifie également que les journaux d’audit ne seront pas disponibles via l Office 365 API Activité de gestion ou Azure Sentinel.</span><span class="sxs-lookup"><span data-stu-id="110cb-111">This also means that audit logs won't be available through the Office 365 Management Activity API or Azure Sentinel.</span></span>
  
## <a name="before-you-turn-auditing-on-or-off"></a><span data-ttu-id="110cb-112">Avant d’activer ou de désactiver l’audit</span><span class="sxs-lookup"><span data-stu-id="110cb-112">Before you turn auditing on or off</span></span>

- <span data-ttu-id="110cb-113">Le rôle Journaux d’audit doit vous être attribué dans Exchange Online pour activer ou désactiver l’audit dans Microsoft 365 organisation.</span><span class="sxs-lookup"><span data-stu-id="110cb-113">You have to be assigned the Audit Logs role in Exchange Online to turn auditing on or off in your Microsoft 365 organization.</span></span> <span data-ttu-id="110cb-114">Par défaut, ce rôle est attribué aux groupes de rôles Gestion de la conformité et Gestion de l’organisation dans la page **Autorisations** du Centre d Exchange de conformité.</span><span class="sxs-lookup"><span data-stu-id="110cb-114">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="110cb-115">Les administrateurs globaux Microsoft 365 sont membres du groupe de rôles Gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="110cb-115">Global admins in Microsoft 365 are members of the Organization Management role group in Exchange Online.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="110cb-116">Des autorisations doivent être attribuées aux utilisateurs Exchange Online pour activer ou désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="110cb-116">Users have to be assigned permissions in Exchange Online to turn auditing on or off.</span></span> <span data-ttu-id="110cb-117">Si vous attribuez aux utilisateurs le rôle Journaux d’audit sur la page **Autorisations** du Centre de sécurité & conformité, ils ne pourront pas activer ou désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="110cb-117">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn auditing on or off.</span></span> <span data-ttu-id="110cb-118">Cela est dû au fait que l’cmdlet sous-jacente est Exchange Online cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="110cb-118">This is because the underlying cmdlet is an Exchange Online PowerShell cmdlet.</span></span> 

- <span data-ttu-id="110cb-119">Pour obtenir des instructions détaillées sur la recherche dans le journal d’audit, consultez la recherche dans le journal d’audit dans le Centre de sécurité [& conformité.](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="110cb-119">For step-by-step instructions on searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> <span data-ttu-id="110cb-120">Pour plus d’informations sur l’API activité Microsoft 365 gestion des données, voir Prise en [Microsoft 365 API de gestion des données.](/office/office-365-management-api/get-started-with-office-365-management-apis)</span><span class="sxs-lookup"><span data-stu-id="110cb-120">For more information about the Microsoft 365 Management Activity API, see [Get started with Microsoft 365 Management APIs](/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span>

- <span data-ttu-id="110cb-121">Pour vérifier que l’audit est allumé, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="110cb-121">To verify that auditing is turned on, you can run the following command in Exchange Online PowerShell:</span></span>

    ```powershell
    Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
    ```

    <span data-ttu-id="110cb-122">La valeur de  `True` la  _propriété UnifiedAuditLogIngestionEnabled_ indique que l’audit est allumé.</span><span class="sxs-lookup"><span data-stu-id="110cb-122">The value of  `True` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that auditing is turned on.</span></span> 

## <a name="turn-on-auditing"></a><span data-ttu-id="110cb-123">Activer l’audit</span><span class="sxs-lookup"><span data-stu-id="110cb-123">Turn on auditing</span></span>

<span data-ttu-id="110cb-124">Si l’audit n’est pas allumé pour votre organisation, vous pouvez l’activer dans le centre de conformité ou à l’aide Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="110cb-124">If auditing is not turned on for your organization, you can turn it on in the compliance center or by using Exchange Online PowerShell.</span></span> <span data-ttu-id="110cb-125">L’opération d’audit peut prendre plusieurs heures avant que vous ne renvoyiez des résultats lors de la recherche dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="110cb-125">It may take several hours after you turn on auditing before you can return results when you search the audit log.</span></span>
  
### <a name="use-the-compliance-center-to-turn-on-auditing"></a><span data-ttu-id="110cb-126">Utiliser le centre de conformité pour activer l’audit</span><span class="sxs-lookup"><span data-stu-id="110cb-126">Use the compliance center to turn on auditing</span></span>

1. <span data-ttu-id="110cb-127">Accédez à <https://compliance.microsoft.com> et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="110cb-127">Go to <https://compliance.microsoft.com> and sign in.</span></span>

2. <span data-ttu-id="110cb-128">Dans le volet de navigation gauche du centre Microsoft 365 conformité, cliquez sur Afficher **tout,** puis sur **Auditer.**</span><span class="sxs-lookup"><span data-stu-id="110cb-128">In the left navigation pane of the Microsoft 365 compliance center, click **Show all**, and then click **Audit**.</span></span>

   <span data-ttu-id="110cb-129">Si l’audit n’est pas désactivé pour votre organisation, une bannière s’affiche pour vous invite à commencer à enregistrer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="110cb-129">If auditing is not turned on for your organization, a banner is displayed prompting you start recording user and admin activity.</span></span>

   ![Bannière sur la page Audit](../media/AuditingBanner.png)

3. <span data-ttu-id="110cb-131">Cliquez sur la **bannière Démarrer l’enregistrement de l’activité de l’utilisateur et de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="110cb-131">Click the **Start recording user and admin activity** banner.</span></span>

   <span data-ttu-id="110cb-132">L’application de la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="110cb-132">It may take up to 60 minutes for the change to take effect.</span></span>

### <a name="use-powershell-to-turn-on-auditing"></a><span data-ttu-id="110cb-133">Utiliser PowerShell pour activer l’audit</span><span class="sxs-lookup"><span data-stu-id="110cb-133">Use PowerShell to turn on auditing</span></span>

1. [<span data-ttu-id="110cb-134">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="110cb-134">Connect to Exchange Online PowerShell</span></span>](/powershell/exchange/connect-to-exchange-online-powershell)

2. <span data-ttu-id="110cb-135">Exécutez la commande PowerShell suivante pour activer l’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="110cb-135">Run the following PowerShell command to turn on auditing in Office 365.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="110cb-136">Un message s’affiche pour vous dire que l’application de la modification peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="110cb-136">A message is displayed saying that it may take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-auditing"></a><span data-ttu-id="110cb-137">Désactiver l’audit</span><span class="sxs-lookup"><span data-stu-id="110cb-137">Turn off auditing</span></span>

<span data-ttu-id="110cb-138">Vous devez utiliser Exchange Online PowerShell pour désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="110cb-138">You have to use Exchange Online PowerShell to turn off auditing.</span></span>
  
1. [<span data-ttu-id="110cb-139">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="110cb-139">Connect to Exchange Online PowerShell</span></span>](/powershell/exchange/connect-to-exchange-online-powershell)

2. <span data-ttu-id="110cb-140">Exécutez la commande PowerShell suivante pour désactiver l’audit.</span><span class="sxs-lookup"><span data-stu-id="110cb-140">Run the following PowerShell command to turn off auditing.</span></span>

    ```powershell
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="110cb-141">Après un certain temps, vérifiez que l’audit est désactivé.</span><span class="sxs-lookup"><span data-stu-id="110cb-141">After a while, verify that auditing is turned off (disabled).</span></span> <span data-ttu-id="110cb-142">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="110cb-142">There are two ways to do this:</span></span>

    - <span data-ttu-id="110cb-143">Dans Exchange Online PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="110cb-143">In Exchange Online PowerShell, run the following command:</span></span>

      ```powershell
      Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
      ```

      <span data-ttu-id="110cb-144">La valeur de  `False` la  _propriété UnifiedAuditLogIngestionEnabled_ indique que l’audit est désactivé.</span><span class="sxs-lookup"><span data-stu-id="110cb-144">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that auditing is turned off.</span></span>

    - <span data-ttu-id="110cb-145">Go to the **Audit** page in the Microsoft 365 compliance center.</span><span class="sxs-lookup"><span data-stu-id="110cb-145">Go to the **Audit** page in the Microsoft 365 compliance center.</span></span>

      <span data-ttu-id="110cb-146">Si l’audit n’est pas désactivé pour votre organisation, une bannière s’affiche pour vous invite à commencer à enregistrer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="110cb-146">If auditing is not turned on for your organization, a banner is displayed prompting you start recording user and admin activity.</span></span>
