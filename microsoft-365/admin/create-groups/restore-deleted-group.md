---
title: Restaurer un groupe Microsoft 365 supprimé
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
description: Découvrez comment restaurer un groupe Microsoft 365 supprimé.
ms.openlocfilehash: 091697be54b1127a5cb336179733d51519947e14
ms.sourcegitcommit: 3cdb670f10519f7af4015731e7910954ba9f70dc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48753242"
---
# <a name="restore-a-deleted-microsoft-365-group"></a><span data-ttu-id="63b61-103">Restaurer un groupe Microsoft 365 supprimé</span><span class="sxs-lookup"><span data-stu-id="63b61-103">Restore a deleted Microsoft 365 group</span></span>

<span data-ttu-id="63b61-104">Si vous avez supprimé un groupe, il sera conservé pendant 30 jours par défaut.</span><span class="sxs-lookup"><span data-stu-id="63b61-104">If you've deleted a group, it will be retained for 30 days by default.</span></span> <span data-ttu-id="63b61-105">Cette période de 30 jours est considérée comme une « suppression possible », car vous pouvez toujours restaurer le groupe.</span><span class="sxs-lookup"><span data-stu-id="63b61-105">This 30-day period is considered a "soft-delete" because you can still restore the group.</span></span> <span data-ttu-id="63b61-106">Après 30 jours, le groupe et son contenu associé sont supprimés définitivement et ne peuvent pas être restaurés.</span><span class="sxs-lookup"><span data-stu-id="63b61-106">After 30 days, the group and its associated contents are permanently deleted and cannot be restored.</span></span>

<span data-ttu-id="63b61-107">En cas de restauration d'un groupe, le contenu suivant est restauré :</span><span class="sxs-lookup"><span data-stu-id="63b61-107">When a group is restored, the following content is restored:</span></span>
  
- <span data-ttu-id="63b61-108">Objet, propriétés et membres groupes Microsoft 365 Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="63b61-108">Azure Active Directory (AD) Microsoft 365 Groups object, properties, and members.</span></span>
    
- <span data-ttu-id="63b61-109">Adresses de messagerie du groupe.</span><span class="sxs-lookup"><span data-stu-id="63b61-109">Group's e-mail addresses.</span></span>
    
- <span data-ttu-id="63b61-110">Boîte de réception et calendrier partagés Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="63b61-110">Exchange Online shared Inbox and calendar.</span></span>
    
- <span data-ttu-id="63b61-111">Site d’équipe Et fichiers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="63b61-111">SharePoint Online team site and files.</span></span>
    
- <span data-ttu-id="63b61-112">bloc-notes OneNote ;</span><span class="sxs-lookup"><span data-stu-id="63b61-112">OneNote notebook</span></span>
    
- <span data-ttu-id="63b61-113">Planificateur.</span><span class="sxs-lookup"><span data-stu-id="63b61-113">Planner</span></span>
    
- <span data-ttu-id="63b61-114">Teams</span><span class="sxs-lookup"><span data-stu-id="63b61-114">Teams</span></span>

- <span data-ttu-id="63b61-115">Yammer de groupe et de groupe (si le groupe Microsoft 365 a été créé à partir Yammer)</span><span class="sxs-lookup"><span data-stu-id="63b61-115">Yammer group and group content (If the Microsoft 365 group was created from Yammer)</span></span>

> [!NOTE]
> <span data-ttu-id="63b61-116">Cet article décrit la restauration uniquement des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="63b61-116">This article describes restoring only Microsoft 365 groups.</span></span> <span data-ttu-id="63b61-117">Tous les autres groupes ne peuvent pas être restaurés une fois supprimés.</span><span class="sxs-lookup"><span data-stu-id="63b61-117">All other groups cannot be restored once deleted.</span></span>

## <a name="restore-a-group"></a><span data-ttu-id="63b61-118">Restaurer un groupe</span><span class="sxs-lookup"><span data-stu-id="63b61-118">Restore a group</span></span>

# <a name="outlook"></a>[<span data-ttu-id="63b61-119">Outlook</span><span class="sxs-lookup"><span data-stu-id="63b61-119">Outlook</span></span>](#tab/outlook)

<span data-ttu-id="63b61-120">Si vous êtes propriétaire d’un groupe Microsoft 365, vous pouvez restaurer le groupe vous-même dans Outlook sur le web en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="63b61-120">If you are the owner of a Microsoft 365 group, you can restore the group yourself in Outlook on the web by following these steps:</span></span>

1. <span data-ttu-id="63b61-121">Dans la [page Groupes supprimés,](https://outlook.office.com/people/group/deleted)sélectionnez l’option  Gérer les groupes sous le nœud **Groupes,** puis choisissez **Supprimé.**</span><span class="sxs-lookup"><span data-stu-id="63b61-121">On the [deleted groups page](https://outlook.office.com/people/group/deleted), select the **Manage groups** option under the **Groups** node, and then choose **Deleted**.</span></span>

2. <span data-ttu-id="63b61-122">Cliquez sur **l’onglet** Restaurer en côté du groupe que vous souhaitez restaurer.</span><span class="sxs-lookup"><span data-stu-id="63b61-122">Click on the **Restore** tab next to the group you want to restore.</span></span>

<span data-ttu-id="63b61-123">Si le groupe supprimé n’apparaît pas ici, contactez un administrateur.</span><span class="sxs-lookup"><span data-stu-id="63b61-123">If the deleted group doesn't appear here, contact an administrator.</span></span>

# <a name="admin-center"></a>[<span data-ttu-id="63b61-124">Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="63b61-124">Admin center</span></span>](#tab/admin-center)

<span data-ttu-id="63b61-125">Si vous êtes administrateur général ou administrateur de groupes, vous pouvez restaurer un groupe supprimé dans le Centre d’administration Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="63b61-125">If you are a global administrator or a groups administrator, you can restore a deleted group in the Microsoft 365 admin center:</span></span>

1. <span data-ttu-id="63b61-126">Allez au [centre administratif](https://admin.microsoft.com).      </span><span class="sxs-lookup"><span data-stu-id="63b61-126">Go to the [admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="63b61-127">Développez **Groupes,** puis cliquez **sur Groupes supprimés.**</span><span class="sxs-lookup"><span data-stu-id="63b61-127">Expand **Groups**, and then click **Deleted groups**.</span></span>
3. <span data-ttu-id="63b61-128">Sélectionnez le groupe à restaurer, puis cliquez sur **Restaurer le groupe.**</span><span class="sxs-lookup"><span data-stu-id="63b61-128">Select the group that you want to restore, and then click **Restore group**.</span></span>

> [!NOTE]
> <span data-ttu-id="63b61-129">Dans certains cas, la restauration du groupe et de toutes ses données peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="63b61-129">In some cases, it may take as long as 24 hours for the group and all of its data to be restored.</span></span> 

---

## <a name="got-questions-about-microsoft-365-groups"></a><span data-ttu-id="63b61-130">Vous avez des questions sur les groupes Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="63b61-130">Got questions about Microsoft 365 Groups?</span></span>

<span data-ttu-id="63b61-131">Visitez la [communauté technique Microsoft pour](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) publier des questions et participer à des conversations sur les groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="63b61-131">Visit the [Microsoft Tech Community](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) to post questions and participate in conversations about Microsoft 365 groups.</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="63b61-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="63b61-132">Related articles</span></span>

[<span data-ttu-id="63b61-133">Gérer les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="63b61-133">Manage Microsoft 365 Groups with PowerShell</span></span>](https://docs.microsoft.com/microsoft-365/enterprise/manage-microsoft-365-groups-with-powershell)
  
[<span data-ttu-id="63b61-134">Supprimer des groupes à l'aide de l'applet de commande Remove-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="63b61-134">Delete groups using the Remove-UnifiedGroup cmdlet</span></span>](https://technet.microsoft.com/library/mt238270%28v=exchg.160%29.aspx)
  
[<span data-ttu-id="63b61-135">Gérer les paramètres de votre site d'équipe connecté à un groupe</span><span class="sxs-lookup"><span data-stu-id="63b61-135">Manage your group-connected team site settings</span></span>](https://support.microsoft.com/office/8376034d-d0c7-446e-9178-6ab51c58df42)
  
[<span data-ttu-id="63b61-136">Supprimer un groupe dans Outlook</span><span class="sxs-lookup"><span data-stu-id="63b61-136">Delete a group in Outlook</span></span>](https://support.microsoft.com/office/ca7f5a9e-ae4f-4cbe-a4bc-89c469d1726f)
