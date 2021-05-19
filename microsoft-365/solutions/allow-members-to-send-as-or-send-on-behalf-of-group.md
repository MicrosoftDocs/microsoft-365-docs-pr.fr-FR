---
title: Autoriser les membres à envoyer en tant que ou de la part d’un groupe
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- m365solution-collabgovernance
search.appverid:
- MET150
ms.assetid: 0ad41414-0cc6-4b97-90fb-06bec7bcf590
recommendations: false
description: Découvrez comment autoriser les membres d’un groupe à envoyer des messages électroniques en tant que Microsoft 365 groupe ou à envoyer du courrier électronique au nom d’Microsoft 365 groupe.
ms.openlocfilehash: 07db8f415da46e6235c051e262237de79e61c8b9
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538254"
---
# <a name="allow-members-to-send-as-or-send-on-behalf-of-a-group"></a><span data-ttu-id="dddb9-103">Autoriser les membres à envoyer en tant que ou de la part d’un groupe</span><span class="sxs-lookup"><span data-stu-id="dddb9-103">Allow members to send as or send on behalf of a group</span></span>

<span data-ttu-id="dddb9-104">Un membre d’un groupe Microsoft 365 qui  a obtenu  des autorisations Envoyer en tant que ou Envoyer de la part de peut envoyer des messages électroniques en tant que groupe ou au nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="dddb9-104">A member of a Microsoft 365 group who has been granted **Send as** or **Send on behalf** permissions can send email as the group, or on behalf of the group.</span></span> <span data-ttu-id="dddb9-105">(Ces autorisations ne peuvent pas être accordées aux invités du groupe.)</span><span class="sxs-lookup"><span data-stu-id="dddb9-105">(Guests in the group cannot be granted these permissions.)</span></span>

<span data-ttu-id="dddb9-106">Cet article explique comment un administrateur général ou Exchange peut définir ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="dddb9-106">This article explains how a global or Exchange administrator can set these permissions.</span></span>
  
<span data-ttu-id="dddb9-107">Par exemple, si Megan Bowen fait partie du groupe  **Microsoft 365** de formation et dispose d’autorisations Envoyer en tant que  sur le groupe, si elle envoie un courrier électronique en tant que groupe, il semblera que le groupe de formation a envoyé le message électronique.</span><span class="sxs-lookup"><span data-stu-id="dddb9-107">For example, if Megan Bowen is part of the **Training** Microsoft 365 group, and has **Send as** permissions on the group, if she sends an email as the group, it will look like the **Training** group sent the email.</span></span> 
  
<span data-ttu-id="dddb9-108">L’autorisation Envoyer de **la part de** permet à un utilisateur d’envoyer des courriers électroniques au nom d’Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="dddb9-108">The **Send on Behalf** permission lets a user send email on behalf of a Microsoft 365 group.</span></span> <span data-ttu-id="dddb9-109">Par exemple, si Alex Wilber fait partie du groupe **Marketing** Microsoft 365, dispose des autorisations Envoyer de la part de et envoie un e-mail en tant que groupe, le message semble avoir été envoyé par **Alex Wilber** pour le compte du marketing. </span><span class="sxs-lookup"><span data-stu-id="dddb9-109">For example, if Alex Wilber is a part of the **Marketing** Microsoft 365 group, and has **Send on Behalf** permissions and sends an email as the group, the email looks like it was sent by **Alex Wilber on behalf of Marketing**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dddb9-110">Vous pouvez configurer **Envoyer en tant** que ou Envoyer de la part **d’un** utilisateur donné, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="dddb9-110">You can configure **Send as** or **Send on behalf** for a given user, but not both.</span></span> <span data-ttu-id="dddb9-111">Si vous configurez les deux, la valeur par défaut est **Envoyer en tant que**.</span><span class="sxs-lookup"><span data-stu-id="dddb9-111">If you configure both, it will default to **Send as**.</span></span>

> [!TIP]
> <span data-ttu-id="dddb9-112">Pour découvrir [Microsoft 365 comment](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b) utiliser Outlook et Outlook sur le Web pour envoyer des messages électroniques à partir d’un groupe, voir Envoyer des courriers électroniques à partir d’un groupe ou de la part d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="dddb9-112">See [Send email from or on behalf of a Microsoft 365 group](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b) to learn how to use Outlook and Outlook on the Web to send email from a group.</span></span>
    
## <a name="allow-members-to-send-email-as-a-group"></a><span data-ttu-id="dddb9-113">Autoriser les membres à envoyer des messages électroniques en tant que groupe</span><span class="sxs-lookup"><span data-stu-id="dddb9-113">Allow members to send email as a group</span></span>

<span data-ttu-id="dddb9-114">Cette section explique comment autoriser les utilisateurs à envoyer des messages électroniques en tant que groupe dans le Centre d’administration [Exchange](https://go.microsoft.com/fwlink/p/?linkid=2059104) (EAC) dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="dddb9-114">This section explains how to allow users to send email as a group in the [Exchange admin center](https://go.microsoft.com/fwlink/p/?linkid=2059104) (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="dddb9-115">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">centre Exchange' administration,</a>allez à **Groupes de destinataires.** \> </span><span class="sxs-lookup"><span data-stu-id="dddb9-115">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="dddb9-116">Sélectionnez **l’icône** Modifier le groupe sur le groupe que vous ![ ](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) souhaitez autoriser les utilisateurs à envoyer en tant que.  </span><span class="sxs-lookup"><span data-stu-id="dddb9-116">Select **Edit**  ![Edit group icon](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on the group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="dddb9-117">Sélectionnez **délégation de groupe.**</span><span class="sxs-lookup"><span data-stu-id="dddb9-117">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="dddb9-118">Dans la section **Envoyer en tant** que, sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez envoyer en tant que **+** groupe.</span><span class="sxs-lookup"><span data-stu-id="dddb9-118">In the **Send As** section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Capture d’écran de la boîte de dialogue Envoyer en tant que](../media/1df167f6-1eff-4f98-9ecd-4230fab46557.png)
  
5. <span data-ttu-id="dddb9-120">Tapez pour rechercher ou sélectionner un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="dddb9-120">Type to search or pick a user from the list.</span></span> <span data-ttu-id="dddb9-121">Sélectionnez **OK** et **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="dddb9-121">Select **OK** and **Save**.</span></span>
    
    ![Tapez pour rechercher ou sélectionner un utilisateur dans la liste](../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)
  
## <a name="allow-members-to-send-email-on-behalf-of-a-group"></a><span data-ttu-id="dddb9-123">Autoriser les membres à envoyer des courriers électroniques au nom d’un groupe</span><span class="sxs-lookup"><span data-stu-id="dddb9-123">Allow members to send email on behalf of a group</span></span>

<span data-ttu-id="dddb9-124">Cette section explique comment autoriser les utilisateurs à envoyer des messages électroniques au nom d’un groupe dans le Centre d’administration Exchange (EAC) dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="dddb9-124">This section explains how to allow users to send email on behalf of a group in the Exchange admin center (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="dddb9-125">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">centre Exchange' administration,</a>allez à **Groupes de destinataires.** \> </span><span class="sxs-lookup"><span data-stu-id="dddb9-125">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="dddb9-126">Sélectionnez **l’icône** Modifier le groupe sur le groupe que vous ![ ](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) souhaitez autoriser les utilisateurs à envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="dddb9-126">Select **Edit** ![Edit group icon](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on the group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="dddb9-127">Sélectionnez **délégation de groupe.**</span><span class="sxs-lookup"><span data-stu-id="dddb9-127">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="dddb9-128">Dans la section Envoyer de la part de, sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez **+** envoyer en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="dddb9-128">In the Send on Behalf section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Capture d’écran de la boîte de dialogue Envoyer de la part de](../media/2bae0579-8907-4d6b-8920-ddd6555897b4.png)
  
5. <span data-ttu-id="dddb9-130">Tapez pour rechercher ou sélectionner un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="dddb9-130">Type to search or pick a user from the list.</span></span> <span data-ttu-id="dddb9-131">Sélectionnez **OK** et **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="dddb9-131">Select **OK** and **Save**.</span></span>
    
    ![Tapez pour rechercher ou sélectionner un utilisateur dans la liste](../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)

## <a name="related-articles"></a><span data-ttu-id="dddb9-133">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="dddb9-133">Related articles</span></span>

[<span data-ttu-id="dddb9-134">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="dddb9-134">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="dddb9-135">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="dddb9-135">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)

[<span data-ttu-id="dddb9-136">En savoir plus sur Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="dddb9-136">Learn more about Microsoft 365 groups</span></span>](https://support.microsoft.com/office/b565caa1-5c40-40ef-9915-60fdb2d97fa2)

[<span data-ttu-id="dddb9-137">Add-RecipientPermission</span><span class="sxs-lookup"><span data-stu-id="dddb9-137">Add-RecipientPermission</span></span>](/powershell/module/exchange/add-recipientpermission)

[<span data-ttu-id="dddb9-138">Set-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="dddb9-138">Set-UnifiedGroup</span></span>](/powershell/module/exchange/set-unifiedgroup)