---
title: Restaurer un groupe de Microsoft 365 supprimé
ms.reviewer: arvaradh
f1.keywords: CSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b7c66b59-657a-4e1a-8aa0-8163b1f4eb54
description: Un groupe supprimé est conservé pendant 30 jours et vous pouvez toujours le restaurer. Après 30 jours, le groupe et son contenu sont supprimés définitivement.
ms.openlocfilehash: 2c20c2bd3ce91331e7160132047dbf3ecd79c4b8
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635737"
---
# <a name="restore-a-deleted-microsoft-365-group"></a><span data-ttu-id="7ba1d-104">Restaurer un groupe de Microsoft 365 supprimé</span><span class="sxs-lookup"><span data-stu-id="7ba1d-104">Restore a deleted Microsoft 365 group</span></span>

<span data-ttu-id="7ba1d-105">Si vous avez supprimé un groupe, il sera conservé pendant 30 jours par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-105">If you've deleted a group, it will be retained for 30 days by default.</span></span> <span data-ttu-id="7ba1d-106">Cette période de 30 jours est considérée comme une « suppression possible », car vous pouvez toujours restaurer le groupe.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-106">This 30-day period is considered a "soft-delete" because you can still restore the group.</span></span> <span data-ttu-id="7ba1d-107">Après 30 jours, le groupe et son contenu associé sont supprimés définitivement et ne peuvent pas être restaurés.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-107">After 30 days, the group and its associated contents are permanently deleted and cannot be restored.</span></span>

<span data-ttu-id="7ba1d-108">En cas de restauration d'un groupe, le contenu suivant est restauré :</span><span class="sxs-lookup"><span data-stu-id="7ba1d-108">When a group is restored, the following content is restored:</span></span>
  
- <span data-ttu-id="7ba1d-109">Azure Active Directory (AD) Microsoft 365, propriétés et membres groups.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-109">Azure Active Directory (AD) Microsoft 365 Groups object, properties, and members.</span></span>
    
- <span data-ttu-id="7ba1d-110">Adresses de messagerie du groupe.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-110">Group's e-mail addresses.</span></span>
    
- <span data-ttu-id="7ba1d-111">Exchange Online boîte de réception et le calendrier partagés.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-111">Exchange Online shared Inbox and calendar.</span></span>
    
- <span data-ttu-id="7ba1d-112">SharePoint Site d’équipe et fichiers en ligne.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-112">SharePoint Online team site and files.</span></span>
    
- <span data-ttu-id="7ba1d-113">bloc-notes OneNote ;</span><span class="sxs-lookup"><span data-stu-id="7ba1d-113">OneNote notebook</span></span>
    
- <span data-ttu-id="7ba1d-114">Planificateur.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-114">Planner</span></span>
    
- <span data-ttu-id="7ba1d-115">Teams</span><span class="sxs-lookup"><span data-stu-id="7ba1d-115">Teams</span></span>

- <span data-ttu-id="7ba1d-116">Yammer de groupe et de groupe (si le groupe Microsoft 365 a été créé à partir de Yammer)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-116">Yammer group and group content (If the Microsoft 365 group was created from Yammer)</span></span>

> [!NOTE]
> <span data-ttu-id="7ba1d-117">Cet article décrit la restauration uniquement Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-117">This article describes restoring only Microsoft 365 groups.</span></span> <span data-ttu-id="7ba1d-118">Tous les autres groupes ne peuvent pas être restaurés une fois supprimés.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-118">All other groups cannot be restored once deleted.</span></span>

## <a name="restore-a-group"></a><span data-ttu-id="7ba1d-119">Restaurer un groupe</span><span class="sxs-lookup"><span data-stu-id="7ba1d-119">Restore a group</span></span>

# <a name="outlook"></a>[<span data-ttu-id="7ba1d-120">Outlook</span><span class="sxs-lookup"><span data-stu-id="7ba1d-120">Outlook</span></span>](#tab/outlook)

<span data-ttu-id="7ba1d-121">Si vous êtes propriétaire d’un groupe Microsoft 365, vous pouvez restaurer le groupe vous-même dans Outlook sur le web en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ba1d-121">If you are the owner of a Microsoft 365 group, you can restore the group yourself in Outlook on the web by following these steps:</span></span>

1. <span data-ttu-id="7ba1d-122">Dans la [page Groupes supprimés,](https://outlook.office.com/people/group/deleted)sélectionnez l’option  Gérer les groupes sous le nœud **Groupes,** puis choisissez **Supprimé.**</span><span class="sxs-lookup"><span data-stu-id="7ba1d-122">On the [deleted groups page](https://outlook.office.com/people/group/deleted), select the **Manage groups** option under the **Groups** node, and then choose **Deleted**.</span></span>

2. <span data-ttu-id="7ba1d-123">Cliquez sur **l’onglet Restaurer** en côté du groupe que vous souhaitez restaurer.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-123">Click on the **Restore** tab next to the group you want to restore.</span></span>

<span data-ttu-id="7ba1d-124">Si le groupe supprimé n’apparaît pas ici, contactez un administrateur.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-124">If the deleted group doesn't appear here, contact an administrator.</span></span>

# <a name="admin-center"></a>[<span data-ttu-id="7ba1d-125">Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="7ba1d-125">Admin center</span></span>](#tab/admin-center)

<span data-ttu-id="7ba1d-126">Si vous êtes administrateur général ou administrateur de groupes, vous pouvez restaurer un groupe supprimé dans le centre d Microsoft 365'administration :</span><span class="sxs-lookup"><span data-stu-id="7ba1d-126">If you are a global administrator or a groups administrator, you can restore a deleted group in the Microsoft 365 admin center:</span></span>

1. <span data-ttu-id="7ba1d-127">Allez au [centre administratif](https://admin.microsoft.com).      </span><span class="sxs-lookup"><span data-stu-id="7ba1d-127">Go to the [admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="7ba1d-128">Développez **Groupes,** puis cliquez **sur Groupes supprimés.**</span><span class="sxs-lookup"><span data-stu-id="7ba1d-128">Expand **Groups**, and then click **Deleted groups**.</span></span>
3. <span data-ttu-id="7ba1d-129">Sélectionnez le groupe à restaurer, puis cliquez sur **Restaurer le groupe.**</span><span class="sxs-lookup"><span data-stu-id="7ba1d-129">Select the group that you want to restore, and then click **Restore group**.</span></span>

> [!NOTE]
> <span data-ttu-id="7ba1d-130">Dans certains cas, la restauration du groupe et de toutes ses données peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-130">In some cases, it may take as long as 24 hours for the group and all of its data to be restored.</span></span> 

---

## <a name="got-questions-about-microsoft-365-groups"></a><span data-ttu-id="7ba1d-131">Vous avez des questions sur Microsoft 365 groupes ?</span><span class="sxs-lookup"><span data-stu-id="7ba1d-131">Got questions about Microsoft 365 Groups?</span></span>

<span data-ttu-id="7ba1d-132">Visitez la Community [Microsoft Tech pour](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) publier des questions et participer à des conversations sur Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-132">Visit the [Microsoft Tech Community](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) to post questions and participate in conversations about Microsoft 365 groups.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="7ba1d-133">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="7ba1d-133">Related content</span></span>

<span data-ttu-id="7ba1d-134">[Gérer Microsoft 365 groupes avec PowerShell](../../enterprise/manage-microsoft-365-groups-with-powershell.md) (article)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-134">[Manage Microsoft 365 Groups with PowerShell](../../enterprise/manage-microsoft-365-groups-with-powershell.md) (article)</span></span>\
<span data-ttu-id="7ba1d-135">[Supprimer des groupes à l’aide Remove-UnifiedGroup cmdlet](/powershell/module/exchange/remove-unifiedgroup) (article)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-135">[Delete groups using the Remove-UnifiedGroup cmdlet](/powershell/module/exchange/remove-unifiedgroup) (article)</span></span>\
<span data-ttu-id="7ba1d-136">[Gérer les paramètres de votre site](https://support.microsoft.com/office/8376034d-d0c7-446e-9178-6ab51c58df42) d’équipe connecté à un groupe (article)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-136">[Manage your group-connected team site settings](https://support.microsoft.com/office/8376034d-d0c7-446e-9178-6ab51c58df42) (article)</span></span>\
<span data-ttu-id="7ba1d-137">[Supprimer un groupe dans Outlook](https://support.microsoft.com/office/ca7f5a9e-ae4f-4cbe-a4bc-89c469d1726f) (article)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-137">[Delete a group in Outlook](https://support.microsoft.com/office/ca7f5a9e-ae4f-4cbe-a4bc-89c469d1726f) (article)</span></span>