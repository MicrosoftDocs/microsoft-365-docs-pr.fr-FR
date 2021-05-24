---
title: Envoyer un courrier électronique en tant que liste de distribution
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: a7c98273-067e-4162-b3a1-4ba081796012
description: Envoyez un courrier électronique en tant que liste de distribution Microsoft 365 de sorte que lorsqu’un membre répond à un message, il semble qu’il soit issu de la liste de distribution.
ms.openlocfilehash: 01bff7e1d2515670c5a6faa199355e7de591f1fb
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52624536"
---
# <a name="send-email-as-a-distribution-list"></a><span data-ttu-id="48681-103">Envoyer un courrier électronique en tant que liste de distribution</span><span class="sxs-lookup"><span data-stu-id="48681-103">Send email as a distribution list</span></span>

<span data-ttu-id="48681-104">Dans Microsoft 365, vous pouvez envoyer des messages électroniques en tant que liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="48681-104">In Microsoft 365, you can send email as a distribution list.</span></span> <span data-ttu-id="48681-105">Lorsqu’une personne membre de la liste de distribution répond à un message envoyé à la liste de distribution, le message semble être issu de la liste de distribution, et non de l’utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="48681-105">When a person who is a member of the distribution list replies to a message sent to the distribution list, the email appears to be from the distribution list, not from the individual user.</span></span> <span data-ttu-id="48681-106">Cette rubrique vous montre comment faire.</span><span class="sxs-lookup"><span data-stu-id="48681-106">This topic shows you how to do this.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="48681-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="48681-107">Before you begin</span></span>

<span data-ttu-id="48681-108">Avant d’effectuer ces étapes, assurez-vous que vous avez été ajouté à une liste de distribution Microsoft 365 et que vous avez reçu l’autorisation Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="48681-108">Before you perform these steps, make sure you've been added to a Microsoft 365 distribution list and you've have been granted Send as permission on it.</span></span>
  
 <span data-ttu-id="48681-109">Administrateurs : assurez-vous que vous avez suivi les **étapes** de la rubrique Ajouter un utilisateur ou un [contact Microsoft 365](../email/add-user-or-contact-to-distribution-list.md) à une liste et autoriser les membres à envoyer des courriers électroniques en tant que rubriques de groupe [Microsoft 365,](../../solutions/allow-members-to-send-as-or-send-on-behalf-of-group.md#allow-members-to-send-email-as-a-group) et que vous avez ajouté les personnes appropriées à la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="48681-109">**Admins**: Make sure you've followed the steps in the [Add a Microsoft 365 user or contact to a list](../email/add-user-or-contact-to-distribution-list.md) and [Allow members to send email as a Microsoft 365 Group](../../solutions/allow-members-to-send-as-or-send-on-behalf-of-group.md#allow-members-to-send-email-as-a-group) topics, and added the correct people to the distribution list.</span></span>
  
## <a name="outlook-on-the-web"></a><span data-ttu-id="48681-110">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="48681-110">Outlook on the web</span></span>

1. <span data-ttu-id="48681-111">Ouvrez Outlook sur le web et allez dans votre boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="48681-111">Open Outlook on the web and go to your inbox.</span></span> 
    
2. <span data-ttu-id="48681-112">Ouvrez un message envoyé à la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="48681-112">Open a message that was sent to the distribution list.</span></span> 
    
3. <span data-ttu-id="48681-113">Sélectionnez **Répondre.**</span><span class="sxs-lookup"><span data-stu-id="48681-113">Select **Reply**.</span></span> 
    
4. <span data-ttu-id="48681-114">At the bottom of the message, select **More** \> **Show from**.</span><span class="sxs-lookup"><span data-stu-id="48681-114">At the bottom of the message, select **More** \> **Show from**.</span></span><br/> <span data-ttu-id="48681-115">![Sélectionnez Plus, puis choisissez Afficher à partir de](../../media/534f13b7-9f15-48ea-8835-ea2ed1863ece.png)</span><span class="sxs-lookup"><span data-stu-id="48681-115">![Select More and then choose Show From](../../media/534f13b7-9f15-48ea-8835-ea2ed1863ece.png)</span></span>
  
5. <span data-ttu-id="48681-116">Cliquez avec le bouton droit sur l’adresse de l’utilisateur de provenance, par `Ina@weewalter.me` exemple, et choisissez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="48681-116">Right-click on the From address - such as `Ina@weewalter.me` - and choose **Remove**.</span></span><br/> <span data-ttu-id="48681-117">![Supprimer l’alias FROM](../../media/9b8d8e8f-dc46-499c-89bd-0a480603bf1f.png)</span><span class="sxs-lookup"><span data-stu-id="48681-117">![Remove the FROM alias](../../media/9b8d8e8f-dc46-499c-89bd-0a480603bf1f.png)</span></span>
  
6. <span data-ttu-id="48681-118">Tapez ensuite l’adresse de la liste de distribution telle support@contoso.com, puis envoyez le message.</span><span class="sxs-lookup"><span data-stu-id="48681-118">Then type the distribution list address such as support@contoso.com, and send the message.</span></span> <span data-ttu-id="48681-119">La prochaine fois que vous répondrez à partir de la liste de distribution, son adresse apparaîtra en tant qu’option dans la **liste De.**</span><span class="sxs-lookup"><span data-stu-id="48681-119">The next time you reply from the distribution list, its address will appear as an option in the **From** list.</span></span><br/><span data-ttu-id="48681-120">![L’alias de la boîte aux lettres partagée s’affiche](../../media/f7632a9a-9cab-446c-9e37-23ef50c5b975.png)</span><span class="sxs-lookup"><span data-stu-id="48681-120">![Alias of the shared mailbox appears](../../media/f7632a9a-9cab-446c-9e37-23ef50c5b975.png)</span></span>

## <a name="outlook"></a><span data-ttu-id="48681-121">Outlook</span><span class="sxs-lookup"><span data-stu-id="48681-121">Outlook</span></span>

1. <span data-ttu-id="48681-122">Ouvrez Outlook client de bureau.</span><span class="sxs-lookup"><span data-stu-id="48681-122">Open Outlook desktop client.</span></span>

2. <span data-ttu-id="48681-123">Rédigez un nouveau message électronique.</span><span class="sxs-lookup"><span data-stu-id="48681-123">Compose a New Email.</span></span> <span data-ttu-id="48681-124">Cliquez sur le **champ** De et sélectionnez **Autre adresse de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="48681-124">Click the **From** field and select **Other email address**.</span></span> <span data-ttu-id="48681-125">Si vous ne voyez pas le champ De, accédez à **Options** et sélectionnez **De** dans la section Afficher les champs.</span><span class="sxs-lookup"><span data-stu-id="48681-125">If you do not see the From field, navigate to **Options** and select **From** in the Show fields section.</span></span>

3. <span data-ttu-id="48681-126">Sélectionnez **l’adresse de la liste** de distribution dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="48681-126">Select the **Distribution List** address from the Global Address List.</span></span>

4. <span data-ttu-id="48681-127">Envoyez le message électronique.</span><span class="sxs-lookup"><span data-stu-id="48681-127">Send the email.</span></span>

## <a name="related-content"></a><span data-ttu-id="48681-128">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="48681-128">Related content</span></span>

<span data-ttu-id="48681-129">[Créer, modifier ou supprimer un groupe de](../email/create-edit-or-delete-a-security-group.md) sécurité dans le Centre d’administration Microsoft 365 (article)</span><span class="sxs-lookup"><span data-stu-id="48681-129">[Create, edit, or delete a security group in the Microsoft 365 admin center](../email/create-edit-or-delete-a-security-group.md) (article)</span></span>\
<span data-ttu-id="48681-130">[Collaboration par courrier](../email/email-collaboration.md) électronique (article)</span><span class="sxs-lookup"><span data-stu-id="48681-130">[Email collaboration](../email/email-collaboration.md) (article)</span></span>\
[<span data-ttu-id="48681-131">Ajouter un utilisateur ou un contact à un groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="48681-131">Add a user or contact to a distribution group</span></span>](../email/add-user-or-contact-to-distribution-list.md)