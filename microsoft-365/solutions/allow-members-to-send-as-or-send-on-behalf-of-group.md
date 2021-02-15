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
description: Découvrez comment autoriser les membres à envoyer des courriers électroniques en tant que groupe Microsoft 365 ou à envoyer du courrier électronique au nom d’un groupe Microsoft 365.
ms.openlocfilehash: 6dff559eceec1b719f31d577d7fff8f604636a47
ms.sourcegitcommit: 47de4402174c263ae8d70c910ca068a7581d04ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "49663582"
---
# <a name="allow-members-to-send-as-or-send-on-behalf-of-a-group"></a><span data-ttu-id="fd4ae-103">Autoriser les membres à envoyer en tant que ou de la part d’un groupe</span><span class="sxs-lookup"><span data-stu-id="fd4ae-103">Allow members to send as or send on behalf of a group</span></span>

<span data-ttu-id="fd4ae-104">Un membre d’un groupe Microsoft 365 qui  a reçu les autorisations Envoyer en tant que ou Envoyer de la part de peut envoyer des messages électroniques en tant que groupe ou au nom du groupe. </span><span class="sxs-lookup"><span data-stu-id="fd4ae-104">A member of a Microsoft 365 group who has been granted **Send as** or **Send on behalf** permissions can send email as the group, or on behalf of the group.</span></span> <span data-ttu-id="fd4ae-105">Cet article explique comment un administrateur général ou Exchange peut définir ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-105">This article explains how a global or Exchange administrator can set these permissions.</span></span>
  
<span data-ttu-id="fd4ae-106">Par exemple, si Megan Bowen fait partie du groupe **Formation** Microsoft 365 et dispose d’autorisations Envoyer en tant  que sur le groupe, si elle envoie un e-mail en tant que groupe, il semblera que le groupe de formation a envoyé le message électronique. </span><span class="sxs-lookup"><span data-stu-id="fd4ae-106">For example, if Megan Bowen is part of the **Training** Microsoft 365 group, and has **Send as** permissions on the group, if she sends an email as the group, it will look like the **Training** group sent the email.</span></span> 
  
<span data-ttu-id="fd4ae-107">L’autorisation Envoyer **de la part de** permet à un utilisateur d’envoyer des courriers électroniques au nom d’un groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-107">The **Send on Behalf** permission lets a user send email on behalf of a Microsoft 365 group.</span></span> <span data-ttu-id="fd4ae-108">Par exemple, si Alex Wilber fait partie du groupe **Marketing**  Microsoft 365, dispose des autorisations Envoyer de la part de et envoie un e-mail en tant que groupe, le message semble avoir été envoyé par **Alex Wilber** pour le compte du marketing.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-108">For example, if Alex Wilber is a part of the **Marketing** Microsoft 365 group, and has **Send on Behalf** permissions and sends an email as the group, the email looks like it was sent by **Alex Wilber on behalf of Marketing**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd4ae-109">Vous pouvez configurer **Envoyer en tant** que ou Envoyer de la part **d’un** utilisateur donné, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-109">You can configure **Send as** or **Send on behalf** for a given user, but not both.</span></span> <span data-ttu-id="fd4ae-110">Si vous configurez les deux, la valeur par défaut est **Envoyer en tant que**.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-110">If you configure both, it will default to **Send as**.</span></span>

> [!TIP]
> <span data-ttu-id="fd4ae-111">Pour découvrir comment utiliser Outlook et Outlook sur le web pour envoyer du courrier électronique à partir d’un groupe, voir Envoyer des courriers électroniques à partir d’un groupe ou au nom d’un groupe [Microsoft 365.](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b)</span><span class="sxs-lookup"><span data-stu-id="fd4ae-111">See [Send email from or on behalf of a Microsoft 365 group](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b) to learn how to use Outlook and Outlook on the Web to send email from a group.</span></span>
    
## <a name="allow-members-to-send-email-as-a-group"></a><span data-ttu-id="fd4ae-112">Autoriser les membres à envoyer des messages électroniques en tant que groupe</span><span class="sxs-lookup"><span data-stu-id="fd4ae-112">Allow members to send email as a group</span></span>

<span data-ttu-id="fd4ae-113">Cette section explique comment autoriser les utilisateurs à envoyer des messages électroniques en tant que groupe dans le Centre d’administration [Exchange](https://go.microsoft.com/fwlink/p/?linkid=2059104) (EAC) dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-113">This section explains how to allow users to send email as a group in the [Exchange admin center](https://go.microsoft.com/fwlink/p/?linkid=2059104) (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="fd4ae-114">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange,</a>allez à **Groupes de destinataires.** \> </span><span class="sxs-lookup"><span data-stu-id="fd4ae-114">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="fd4ae-115">Sélectionnez **Modifier** ![ l’icône de groupe sur le groupe que vous ](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) souhaitez autoriser les utilisateurs à envoyer en tant que.  </span><span class="sxs-lookup"><span data-stu-id="fd4ae-115">Select **Edit**  ![Edit group icon](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on the group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="fd4ae-116">Sélectionnez **délégation de groupe.**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-116">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="fd4ae-117">Dans la section **Envoyer en tant** que, sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez envoyer en tant que **+** groupe.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-117">In the **Send As** section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Capture d’écran de la boîte de dialogue Envoyer en tant que](../media/1df167f6-1eff-4f98-9ecd-4230fab46557.png)
  
5. <span data-ttu-id="fd4ae-119">Tapez pour rechercher ou sélectionner un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-119">Type to search or pick a user from the list.</span></span> <span data-ttu-id="fd4ae-120">Sélectionnez **OK** et **Enregistrez.**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-120">Select **OK** and **Save**.</span></span>
    
    ![Tapez pour rechercher ou sélectionner un utilisateur dans la liste](../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)
  
## <a name="allow-members-to-send-email-on-behalf-of-a-group"></a><span data-ttu-id="fd4ae-122">Autoriser les membres à envoyer des courriers électroniques au nom d’un groupe</span><span class="sxs-lookup"><span data-stu-id="fd4ae-122">Allow members to send email on behalf of a group</span></span>

<span data-ttu-id="fd4ae-123">Cette section explique comment autoriser les utilisateurs à envoyer des messages électroniques au nom d’un groupe dans le Centre d’administration Exchange (EAC) dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-123">This section explains how to allow users to send email on behalf of a group in the Exchange admin center (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="fd4ae-124">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange,</a>allez à **Groupes de destinataires.** \> </span><span class="sxs-lookup"><span data-stu-id="fd4ae-124">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="fd4ae-125">Sélectionnez **l’icône** Modifier le groupe sur le groupe que vous ![ ](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) souhaitez autoriser les utilisateurs à envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-125">Select **Edit** ![Edit group icon](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on the group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="fd4ae-126">Sélectionnez **délégation de groupe.**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-126">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="fd4ae-127">Dans la section Envoyer de la part de, sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez **+** envoyer en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-127">In the Send on Behalf section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Capture d’écran de la boîte de dialogue Envoyer de la part de](../media/2bae0579-8907-4d6b-8920-ddd6555897b4.png)
  
5. <span data-ttu-id="fd4ae-129">Tapez pour rechercher ou sélectionner un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-129">Type to search or pick a user from the list.</span></span> <span data-ttu-id="fd4ae-130">Sélectionnez **OK** et **Enregistrez.**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-130">Select **OK** and **Save**.</span></span>
    
    ![Tapez pour rechercher ou sélectionner un utilisateur dans la liste](../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)

## <a name="related-articles"></a><span data-ttu-id="fd4ae-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="fd4ae-132">Related articles</span></span>

[<span data-ttu-id="fd4ae-133">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="fd4ae-133">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="fd4ae-134">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="fd4ae-134">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)

[<span data-ttu-id="fd4ae-135">En savoir plus sur les groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fd4ae-135">Learn more about Microsoft 365 groups</span></span>](https://support.microsoft.com/office/b565caa1-5c40-40ef-9915-60fdb2d97fa2)

[<span data-ttu-id="fd4ae-136">Add-RecipientPermission</span><span class="sxs-lookup"><span data-stu-id="fd4ae-136">Add-RecipientPermission</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=723960)

[<span data-ttu-id="fd4ae-137">Set-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="fd4ae-137">Set-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616189)
