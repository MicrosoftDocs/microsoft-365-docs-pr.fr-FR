---
title: Autoriser les membres à envoyer en tant que ou envoyer de la part d’un groupe
ms.reviewer: arvaradh
f1.keywords:
- NOCSH
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
description: Découvrez comment autoriser les membres à envoyer des messages électroniques en tant que groupe Office 365 ou envoyer des courriers électroniques de la part d’un groupe Office 365.
ms.openlocfilehash: c0dca3a3bbed6617874d9dfbca06a4ec5d6b4ebc
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239245"
---
# <a name="allow-members-to-send-as-or-send-on-behalf-of-a-group"></a><span data-ttu-id="25173-103">Autoriser les membres à envoyer en tant que ou envoyer de la part d’un groupe</span><span class="sxs-lookup"><span data-stu-id="25173-103">Allow members to send as or send on behalf of a Group</span></span>

<span data-ttu-id="25173-104">Un membre d’un groupe Office 365 auquel ont été accordées des autorisations **Envoyer en tant** que ou **Envoyer de la part** de peuvent désormais envoyer des courriers électroniques en tant que groupe ou au nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="25173-104">A member of an Office 365 Group who has been granted **Send as** or **Send on behalf** permissions can now send email as the group, or on behalf of the group.</span></span> <span data-ttu-id="25173-105">Cette rubrique explique comment un administrateur peut définir ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="25173-105">This topic explains how an admin can set these permissions.</span></span>
  
<span data-ttu-id="25173-106">Par exemple, si Megan Bowen fait partie du groupe **formation** Office 365 et qu’il dispose des autorisations **Envoyer en tant** que pour le groupe, si elle envoie un message électronique en tant que groupe, il ressemblera au groupe de **formation** qui a envoyé le message.</span><span class="sxs-lookup"><span data-stu-id="25173-106">For example, if Megan Bowen is part of the **Training** Office 365 Group, and has **Send as** permissions on the group, if she sends an email as the Group, it will look like the **Training** group sent the email.</span></span> 
  
<span data-ttu-id="25173-107">L’autorisation **Envoyer de la part** de permet à un utilisateur d’envoyer des courriers électroniques de la part d’un groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="25173-107">The **Send on Behalf** permission lets a user send email on behalf of an Office 365 Group.</span></span> <span data-ttu-id="25173-108">Par exemple, si Alex Wilber fait partie du groupe Office **Marketing** 365 et qu’il dispose des autorisations **Envoyer de la part** de et qu’il envoie un message électronique en tant que groupe, le message électronique a été envoyé par **Alex Wilber pour le compte de marketing**.</span><span class="sxs-lookup"><span data-stu-id="25173-108">For example, if Alex Wilber is a part of the **Marketing** Office 365 Group, and has **Send on Behalf** permissions and sends an email as the group, the email looks like it was sent by **Alex Wilber on behalf of Marketing**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25173-109">Vous pouvez configurer la fonction **Envoyer en tant que** ou **Envoyer de la part** de pour un utilisateur donné, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="25173-109">You can configure **Send as** or **Send on behalf** for a given user, but not both.</span></span> <span data-ttu-id="25173-110">Si vous configurez les deux, il s’agit par défaut de la valeur **Envoyer en tant que**.</span><span class="sxs-lookup"><span data-stu-id="25173-110">If you configure both, it will default to **Send as**.</span></span>

> [!TIP]
> <span data-ttu-id="25173-111">Consultez les étapes de la procédure [envoyer 365 un courrier électronique à partir de ou pour](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx) pour savoir comment utiliser Outlook et Outlook sur le Web pour envoyer des courriers électroniques à partir d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="25173-111">Check the out the steps in [Send email from or on behalf of an Office 365 group](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx) to learn how to use Outlook and Outlook on the Web to send email from a Group.</span></span>
    
## <a name="allow-members-to-send-email-as-a-group"></a><span data-ttu-id="25173-112">Autoriser les membres à envoyer des messages électroniques en tant que groupe</span><span class="sxs-lookup"><span data-stu-id="25173-112">Allow members to send email as a Group</span></span>

<span data-ttu-id="25173-113">Cette section explique comment autoriser les utilisateurs à envoyer des courriers électroniques en tant que groupe dans le [Centre d’administration Exchange](https://go.microsoft.com/fwlink/p/?linkid=2059104) dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="25173-113">This section explains how to allow users to send email as a Group in the [Exchange admin center](https://go.microsoft.com/fwlink/p/?linkid=2059104) (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="25173-114">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>, accédez à **groupes**de **destinataires** \> .</span><span class="sxs-lookup"><span data-stu-id="25173-114">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="25173-115">Sélectionnez **modifier**![l’icône](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) du groupe de modification sur le groupe que vous souhaitez autoriser les utilisateurs à envoyer en tant que.  </span><span class="sxs-lookup"><span data-stu-id="25173-115">Select **Edit**  ![Edit group icon](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on Group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="25173-116">Sélectionnez **délégation de groupe**.</span><span class="sxs-lookup"><span data-stu-id="25173-116">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="25173-117">Dans la section **Envoyer en tant que** , **+** sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="25173-117">In the **Send As** section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Sélectionnez le signe plus pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe Office 365](../media/1df167f6-1eff-4f98-9ecd-4230fab46557.png)
  
5. <span data-ttu-id="25173-119">Tapez pour rechercher ou choisir un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="25173-119">Type to search or pick a user from the list.</span></span> <span data-ttu-id="25173-120">Sélectionnez **OK** et **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="25173-120">Select **OK** and **Save**.</span></span>
    
    ![Type de recherche ou de sélection d’un utilisateur dans la liste](../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)
  
## <a name="allow-members-to-send-email-on-behalf-of-a-group"></a><span data-ttu-id="25173-122">Autoriser les membres à envoyer des courriers électroniques pour le compte d’un groupe</span><span class="sxs-lookup"><span data-stu-id="25173-122">Allow members to send email on behalf of a Group</span></span>

<span data-ttu-id="25173-123">Cette section explique comment autoriser les utilisateurs à envoyer des courriers électroniques de la part d’un groupe dans le centre d’administration Exchange dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="25173-123">This section explains how to allow users to send email on behalf of a Group in the Exchange admin center (EAC) in Exchange Online.</span></span>
  
1. <span data-ttu-id="25173-124">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>, accédez à **groupes**de **destinataires** \> .</span><span class="sxs-lookup"><span data-stu-id="25173-124">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>, go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="25173-125">Sélectionnez **modifier** ![l’icône](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) modifier le groupe dans le groupe que vous souhaitez autoriser les utilisateurs à envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="25173-125">Select **Edit** ![Edit group icon](../media/0cfcb590-dc51-4b4f-9276-bb2ce300d87e.png) on the Group that you want to allow users to send as.</span></span> 
    
3. <span data-ttu-id="25173-126">Sélectionnez **délégation de groupe**.</span><span class="sxs-lookup"><span data-stu-id="25173-126">Select **group delegation**.</span></span>
    
4. <span data-ttu-id="25173-127">Dans la section envoyer de la part de, **+** sélectionnez le signe pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="25173-127">In the Send on Behalf section, select the **+** sign to add the users that you want to send as the Group.</span></span> 
    
    ![Sélectionnez le signe plus pour ajouter les utilisateurs que vous souhaitez envoyer en tant que groupe Office 365](../media/2bae0579-8907-4d6b-8920-ddd6555897b4.png)
  
5. <span data-ttu-id="25173-129">Tapez pour rechercher ou choisir un utilisateur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="25173-129">Type to search or pick a user from the list.</span></span> <span data-ttu-id="25173-130">Sélectionnez **OK** et **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="25173-130">Select **OK** and **Save**.</span></span>
    
    ![Type de recherche ou de sélection d’un utilisateur dans la liste](../media/522919cf-664c-4a25-8076-c51c8c9fbe43.png)

## <a name="related-articles"></a><span data-ttu-id="25173-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="25173-132">Related articles</span></span>

[<span data-ttu-id="25173-133">En savoir plus sur les groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="25173-133">Learn more about Office 365 Groups</span></span>](https://support.office.com/article/3f780e8e-61aa-4287-830d-ff6209cbc192.aspx)

[<span data-ttu-id="25173-134">Add-RecipientPermission</span><span class="sxs-lookup"><span data-stu-id="25173-134">Add-RecipientPermission</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=723960)

[<span data-ttu-id="25173-135">Set-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="25173-135">Set-UnifiedGroup</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=616189)
