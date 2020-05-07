---
title: Autoriser les membres à envoyer en tant que ou envoyer de la part d’un groupe
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: get-started-article
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
ms.assetid: 0ad41414-0cc6-4b97-90fb-06bec7bcf590
description: Découvrez comment autoriser les membres à envoyer des messages électroniques en tant que groupe Microsoft 365 ou envoyer des courriers électroniques de la part d’un groupe Microsoft 365.
ms.openlocfilehash: ce4527321468ee01864177fc1a607fab6a474481
ms.sourcegitcommit: 5476c2578400894640ae74bfe8e93c3319f685bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44049386"
---
# <a name="allow-members-to-send-as-or-send-on-behalf-of-a-group"></a><span data-ttu-id="043c2-103">Autoriser les membres à envoyer en tant que ou envoyer de la part d’un groupe</span><span class="sxs-lookup"><span data-stu-id="043c2-103">Allow members to send as or send on behalf of a Group</span></span>

<span data-ttu-id="043c2-104">Un membre d’un groupe Microsoft 365 auquel ont été accordées des autorisations **Envoyer en tant** que ou **Envoyer de la part** de peuvent envoyer des messages électroniques en tant que groupe ou pour le compte du groupe.</span><span class="sxs-lookup"><span data-stu-id="043c2-104">A member of a Microsoft 365 group who has been granted **Send as** or **Send on behalf** permissions can send email as the group, or on behalf of the group.</span></span> <span data-ttu-id="043c2-105">Cette rubrique explique comment un administrateur peut définir ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="043c2-105">This topic explains how an admin can set these permissions.</span></span>
  
<span data-ttu-id="043c2-106">Par exemple, si Megan Bowen fait partie du groupe **formation** Microsoft 365 et dispose des autorisations **Envoyer en tant** que pour le groupe, si elle envoie un message électronique en tant que groupe, il ressemblera au groupe **formation** qui a envoyé le message.</span><span class="sxs-lookup"><span data-stu-id="043c2-106">For example, if Megan Bowen is part of the **Training** Microsoft 365 group, and has **Send as** permissions on the group, if she sends an email as the group, it will look like the **Training** group sent the email.</span></span> 
  
<span data-ttu-id="043c2-107">L’autorisation **Envoyer de la part** de permet à un utilisateur d’envoyer des courriers électroniques de la part d’un groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="043c2-107">The **Send on Behalf** permission lets a user send email on behalf of a Microsoft 365 group.</span></span> <span data-ttu-id="043c2-108">Par exemple, si Alex Wilber fait partie du groupe Microsoft 365 **marketing** et dispose des autorisations **Envoyer de la part** de, et envoie un message électronique en tant que groupe, le message électronique semble qu’il a été envoyé par **Alex Wilber pour le compte de marketing**.</span><span class="sxs-lookup"><span data-stu-id="043c2-108">For example, if Alex Wilber is a part of the **Marketing** Microsoft 365 group, and has **Send on Behalf** permissions and sends an email as the group, the email looks like it was sent by **Alex Wilber on behalf of Marketing**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="043c2-109">Vous pouvez configurer la fonction **Envoyer en tant que** ou **Envoyer de la part** de pour un utilisateur donné, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="043c2-109">You can configure **Send as** or **Send on behalf** for a given user, but not both.</span></span> <span data-ttu-id="043c2-110">Si vous configurez les deux, il s’agit par défaut de la valeur **Envoyer en tant que**.</span><span class="sxs-lookup"><span data-stu-id="043c2-110">If you configure both, it will default to **Send as**.</span></span>

> [!TIP]
> <span data-ttu-id="043c2-111">Pour savoir comment utiliser Outlook et Outlook sur le Web pour envoyer des courriers électroniques à partir d’un groupe, consultez la rubrique [Envoyer un courrier électronique à partir de ou pour le compte de Microsoft 365](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx) .</span><span class="sxs-lookup"><span data-stu-id="043c2-111">See [Send email from or on behalf of a Microsoft 365 group](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx) to learn how to use Outlook and Outlook on the Web to send email from a group.</span></span>
    
## <a name="allow-members-to-send-email-as-a-group"></a><span data-ttu-id="043c2-112">Autoriser les membres à envoyer des messages électroniques en tant que groupe</span><span class="sxs-lookup"><span data-stu-id="043c2-112">Allow members to send email as a group</span></span>

<span data-ttu-id="043c2-113">Cette section explique comment autoriser les utilisateurs à envoyer des courriers électroniques en tant que groupe dans le [Centre d’administration Exchange](https://go.microsoft.com/fwlink/p/?linkid=2059104) dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="043c2-113">This section explains how to allow users to send email as a group in the [Exchange admin center](https://go.microsoft.com/fwlink/p/?linkid=2059104) (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="043c2-114">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>, accédez à **groupes**de **destinataires** \> .</span><span class="sxs-lookup"><span data-stu-id="043c2-114">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="043c2-115">Sélectionnez **modifier**![l’icône](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) du groupe de modification sur le groupe que vous souhaitez autoriser les utilisateurs à envoyer en tant que.  </span><span class="sxs-lookup"><span data-stu-id="043c2-115">Select **Edit**  ![Edit group icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on Group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="043c2-116">Sélectionnez **délégation de groupe**.</span><span class="sxs-lookup"><span data-stu-id="043c2-116">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="043c2-117">Dans la section **Envoyer en tant que** , **+** sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="043c2-117">In the **Send As** section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Sélectionnez le signe plus pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe Microsoft 365](../../media/1df167f6-1eff-4f98-9ecd-4230fab46557.png)
  
5. <span data-ttu-id="043c2-119">Tapez pour rechercher ou choisir un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="043c2-119">Type to search or pick a user from the list.</span></span> <span data-ttu-id="043c2-120">Sélectionnez **OK** et **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="043c2-120">Select **OK** and **Save**.</span></span>
    
    ![Type de recherche ou de sélection d’un utilisateur dans la liste](../../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)
  
## <a name="allow-members-to-send-email-on-behalf-of-a-group"></a><span data-ttu-id="043c2-122">Autoriser les membres à envoyer des courriers électroniques pour le compte d’un groupe</span><span class="sxs-lookup"><span data-stu-id="043c2-122">Allow members to send email on behalf of a group</span></span>

<span data-ttu-id="043c2-123">Cette section explique comment autoriser les utilisateurs à envoyer des courriers électroniques de la part d’un groupe dans le centre d’administration Exchange dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="043c2-123">This section explains how to allow users to send email on behalf of a group in the Exchange admin center (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="043c2-124">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>, accédez à **groupes**de **destinataires** \> .</span><span class="sxs-lookup"><span data-stu-id="043c2-124">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="043c2-125">Sélectionnez **modifier** ![l’icône](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) modifier le groupe dans le groupe que vous souhaitez autoriser les utilisateurs à envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="043c2-125">Select **Edit** ![Edit group icon](../../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on the Group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="043c2-126">Sélectionnez **délégation de groupe**.</span><span class="sxs-lookup"><span data-stu-id="043c2-126">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="043c2-127">Dans la section envoyer de la part de, **+** sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="043c2-127">In the Send on Behalf section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Sélectionnez le signe plus pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe Microsoft 365](../../media/2bae0579-8907-4d6b-8920-ddd6555897b4.png)
  
5. <span data-ttu-id="043c2-129">Tapez pour rechercher ou choisir un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="043c2-129">Type to search or pick a user from the list.</span></span> <span data-ttu-id="043c2-130">Sélectionnez **OK** et **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="043c2-130">Select **OK** and **Save**.</span></span>
    
    ![Type de recherche ou de sélection d’un utilisateur dans la liste](../../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)

## <a name="related-articles"></a><span data-ttu-id="043c2-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="043c2-132">Related articles</span></span>

[<span data-ttu-id="043c2-133">En savoir plus sur les groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="043c2-133">Learn more about Microsoft 365 groups</span></span>](https://support.office.com/article/learn-about-office-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2)

[<span data-ttu-id="043c2-134">Add-RecipientPermission</span><span class="sxs-lookup"><span data-stu-id="043c2-134">Add-RecipientPermission</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=723960)

[<span data-ttu-id="043c2-135">Set-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="043c2-135">Set-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616189)
