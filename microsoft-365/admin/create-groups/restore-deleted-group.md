---
title: Restaurer un groupe supprimé
ms.reviewer: arvaradh
f1.keywords: CSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b7c66b59-657a-4e1a-8aa0-8163b1f4eb54
description: Découvrez comment restaurer un groupe Microsoft 365 supprimé.
ms.openlocfilehash: a0e7aef090528b3fa183fe08f9c4d06c86f94a10
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43630030"
---
# <a name="restore-a-deleted-group"></a><span data-ttu-id="9f277-103">Restaurer un groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="9f277-103">Restore a deleted Group</span></span>

<span data-ttu-id="9f277-104">Si vous avez supprimé un groupe, il est conservé pendant 30 jours par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f277-104">If you've deleted a group, it will be retained for 30 days by default.</span></span> <span data-ttu-id="9f277-105">Cette période de 30 jours est considérée comme une « suppression récupérable » car vous pouvez toujours restaurer le groupe.</span><span class="sxs-lookup"><span data-stu-id="9f277-105">This 30-day period is considered a "soft-delete" because you can still restore the group.</span></span> <span data-ttu-id="9f277-106">Après 30 jours, le groupe et le contenu associé sont supprimés définitivement et ne peuvent pas être restaurés.</span><span class="sxs-lookup"><span data-stu-id="9f277-106">After 30 days, the group and its associated contents are permanently deleted and cannot be restored.</span></span>

<span data-ttu-id="9f277-107">En cas de restauration d'un groupe, le contenu suivant est restauré :</span><span class="sxs-lookup"><span data-stu-id="9f277-107">When a group is restored, the following content is restored:</span></span>
  
- <span data-ttu-id="9f277-108">Azure Active Directory (AD) Microsoft 365 groupes objet, propriétés et membres.</span><span class="sxs-lookup"><span data-stu-id="9f277-108">Azure Active Directory (AD) Microsoft 365 Groups object, properties, and members.</span></span>
    
- <span data-ttu-id="9f277-109">Adresses de messagerie du groupe.</span><span class="sxs-lookup"><span data-stu-id="9f277-109">Group's e-mail addresses.</span></span>
    
- <span data-ttu-id="9f277-110">Calendrier et boîte de réception partagés Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9f277-110">Exchange Online shared Inbox and calendar.</span></span>
    
- <span data-ttu-id="9f277-111">Site et fichiers d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="9f277-111">SharePoint Online team site and files.</span></span>
    
- <span data-ttu-id="9f277-112">bloc-notes OneNote ;</span><span class="sxs-lookup"><span data-stu-id="9f277-112">OneNote notebook</span></span>
    
- <span data-ttu-id="9f277-113">Planificateur.</span><span class="sxs-lookup"><span data-stu-id="9f277-113">Planner</span></span>
    
- <span data-ttu-id="9f277-114">Équipes</span><span class="sxs-lookup"><span data-stu-id="9f277-114">Teams</span></span>

- <span data-ttu-id="9f277-115">Groupe Yammer et contenu de groupe (si le groupe Microsoft 365 a été créé à partir de Yammer)</span><span class="sxs-lookup"><span data-stu-id="9f277-115">Yammer group and group content (If the Microsoft 365 group was created from Yammer)</span></span>

## <a name="restore-a-group-that-you-own-by-using-outlook"></a><span data-ttu-id="9f277-116">Restaurer un groupe dont vous êtes propriétaire à l’aide d’Outlook</span><span class="sxs-lookup"><span data-stu-id="9f277-116">Restore a group that you own by using Outlook</span></span>

<span data-ttu-id="9f277-117">Si vous êtes le propriétaire d’un groupe Microsoft 365, vous pouvez restaurer le groupe vous-même dans Outlook en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9f277-117">If you are the owner of a Microsoft 365 group, you can restore the group yourself in Outlook by following these steps:</span></span>

1. <span data-ttu-id="9f277-118">Sur la [page groupes supprimés](https://outlook.office.com/people/group/deleted), sélectionnez l’option **gérer les groupes** sous le nœud **groupes** , puis choisissez **supprimé**.</span><span class="sxs-lookup"><span data-stu-id="9f277-118">On the [deleted groups page](https://outlook.office.com/people/group/deleted), select the **Manage groups** option under the **Groups** node, and then choose **Deleted**.</span></span>

2. <span data-ttu-id="9f277-119">Cliquez sur l’onglet **restaurer** en regard du groupe que vous souhaitez restaurer.</span><span class="sxs-lookup"><span data-stu-id="9f277-119">Click on the **Restore** tab next to the group you want to restore.</span></span>

<span data-ttu-id="9f277-120">Si le groupe supprimé n’apparaît pas ici, contactez un administrateur.</span><span class="sxs-lookup"><span data-stu-id="9f277-120">If the deleted group doesn't appear here, contact an administrator.</span></span>

## <a name="restore-a-group-in-the-microsoft-365-admin-center"></a><span data-ttu-id="9f277-121">Restaurer un groupe dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9f277-121">Restore a group in the Microsoft 365 admin center</span></span>

<span data-ttu-id="9f277-122">Si vous êtes un administrateur général ou un administrateur de groupes, vous pouvez restaurer un groupe supprimé dans le centre d’administration 365 de Microsoft :</span><span class="sxs-lookup"><span data-stu-id="9f277-122">If you are a global administrator or a groups administrator, you can restore a deleted group in the Microsoft 365 admin center:</span></span>

1. <span data-ttu-id="9f277-123">Accédez au [Centre d’administration](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9f277-123">Go to the [admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="9f277-124">Développez **groupes**, puis cliquez sur **groupes supprimés**.</span><span class="sxs-lookup"><span data-stu-id="9f277-124">Expand **Groups**, and then click **Deleted groups**.</span></span>
3. <span data-ttu-id="9f277-125">Sélectionnez le groupe que vous souhaitez restaurer, puis cliquez sur **restaurer le groupe**.</span><span class="sxs-lookup"><span data-stu-id="9f277-125">Select the group that you want to restore, and then click **Restore group**.</span></span>
  
## <a name="permanently-delete-a-microsoft-365-group"></a><span data-ttu-id="9f277-126">Supprimer définitivement un groupe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9f277-126">Permanently delete a Microsoft 365 group</span></span>

<span data-ttu-id="9f277-127">Il peut arriver que vous souhaitiez purger définitivement un groupe sans attendre que la période de suppression du logiciel de 30 jours expire.</span><span class="sxs-lookup"><span data-stu-id="9f277-127">Sometimes you may want to permanently purge a group without waiting for the 30 day soft-deletion period to expire.</span></span> <span data-ttu-id="9f277-128">Pour ce faire, démarrez PowerShell et exécutez la commande suivante pour obtenir l'ID d'objet du groupe.</span><span class="sxs-lookup"><span data-stu-id="9f277-128">To do that, start PowerShell and run this command to get the object ID of the group:</span></span>
  
```
Get-AzureADMSDeletedGroup
```

<span data-ttu-id="9f277-129">Prenez note de l’ID d’objet du ou des groupes que vous souhaitez supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="9f277-129">Take note of the object ID of the group, or groups, that you want to permanently delete.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="9f277-130">La suppression définitive du groupe supprime le groupe et ses données pour toujours.</span><span class="sxs-lookup"><span data-stu-id="9f277-130">Purging the group removes the group and its data forever.</span></span> 
  
<span data-ttu-id="9f277-131">Pour supprimer définitivement le groupe, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9f277-131">To purge the group run this command in PowerShell:</span></span>
  
```
Remove-AzureADMSDeletedDirectoryObject -Id <objectId>
```

<span data-ttu-id="9f277-p103">Pour vérifier que le groupe a été supprimé définitivement, réexécutez l'applet de commande  *Get-AzureADMSDeletedGroup*  pour confirmer que le groupe n'apparaît plus dans la liste des groupes supprimés (suppression réversible). Dans certains cas, la suppression définitive du groupe et de toutes ses données peut prendre jusqu'à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="9f277-p103">To confirm that the group has been successfully purged, run the  *Get-AzureADMSDeletedGroup*  cmdlet again to confirm that the group no longer appears on the list of soft-deleted groups. In some cases it may take as long as 24 hours for the group and all of its data to be permanently deleted.</span></span> 
  
## <a name="got-questions-about-microsoft-365-groups"></a><span data-ttu-id="9f277-134">Vous avez des questions sur les groupes Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="9f277-134">Got questions about Microsoft 365 Groups?</span></span>

<span data-ttu-id="9f277-135">Visitez la [communauté Microsoft Tech](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) pour publier des questions et participer à des conversations sur les groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9f277-135">Visit the [Microsoft Tech Community](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) to post questions and participate in conversations about Microsoft 365 groups.</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="9f277-136">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="9f277-136">Related articles</span></span>

[<span data-ttu-id="9f277-137">Gérer les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="9f277-137">Manage Microsoft 365 Groups with PowerShell</span></span>](https://support.office.com/article/aeb669aa-1770-4537-9de2-a82ac11b0540)
  
[<span data-ttu-id="9f277-138">Supprimer des groupes à l'aide de l'applet de commande Remove-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="9f277-138">Delete groups using the Remove-UnifiedGroup cmdlet</span></span>](https://technet.microsoft.com/library/mt238270%28v=exchg.160%29.aspx)
  
[<span data-ttu-id="9f277-139">Gérer les paramètres de votre site d'équipe connecté à un groupe</span><span class="sxs-lookup"><span data-stu-id="9f277-139">Manage your group-connected team site settings</span></span>](https://support.office.com/article/8376034d-d0c7-446e-9178-6ab51c58df42.aspx)
  
[<span data-ttu-id="9f277-140">Supprimer un groupe dans Outlook</span><span class="sxs-lookup"><span data-stu-id="9f277-140">Delete a group in Outlook</span></span>](https://support.office.com/article/ca7f5a9e-ae4f-4cbe-a4bc-89c469d1726f.aspx)
