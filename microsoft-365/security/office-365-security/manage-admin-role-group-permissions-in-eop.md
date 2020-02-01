---
title: Gérer les autorisations de groupe de rôles d’administrateur dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Les administrateurs peuvent apprendre à attribuer ou supprimer des autorisations dans le centre d’administration Exchange dans Exchange Online Protection.
ms.openlocfilehash: ab574e4d33d84774ef63f73297447ea66a74430b
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599031"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a><span data-ttu-id="0f011-103">Gérer les autorisations de groupe de rôles d’administrateur dans EOP</span><span class="sxs-lookup"><span data-stu-id="0f011-103">Manage admin role group permissions in EOP</span></span>

<span data-ttu-id="0f011-p101">Dans Microsoft Exchange Online Protection (EOP), vous pouvez utiliser le Centre d'administration Exchange (CAE) pour inclure un utilisateur en tant que membre d'un ou de plusieurs groupes de rôles afin de lui attribuer des autorisations lui permettant de réaliser des tâches administratives particulières. Le CAE vous permet également de supprimer un utilisateur d'un ou de plusieurs groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="0f011-p101">In Microsoft Exchange Online Protection (EOP), you can use the Exchange admin center (EAC) to make a user a member of a role group or groups in order to assign them permissions to perform specific administrative tasks. You can also remove a user from a role group or groups by using the EAC.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="0f011-106">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0f011-106">What do you need to know before you begin?</span></span>

- <span data-ttu-id="0f011-107">Durée d'exécution estimée : 5 à 10 minutes</span><span class="sxs-lookup"><span data-stu-id="0f011-107">Estimated time to complete: 5-10 minutes</span></span>

- <span data-ttu-id="0f011-108">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="0f011-108">To open the Exchange admin center, see [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="0f011-p102">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="0f011-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span>

- <span data-ttu-id="0f011-111">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="0f011-111">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="0f011-112">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="0f011-112">Having problems?</span></span> <span data-ttu-id="0f011-113">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="0f011-113">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a><span data-ttu-id="0f011-114">Utiliser le Centre d'administration Exchange (CAE) pour affecter des membres à des groupes de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="0f011-114">Use the EAC to assign members to admin role groups</span></span>

1. <span data-ttu-id="0f011-115">Dans le centre d’administration Exchange, accédez à **rôles d’administrateur**des **autorisations** \> , cliquez sur le groupe de rôles auquel vous souhaitez ajouter l’utilisateur ou les utilisateurs,](../media/ITPro-EAC-EditIcon.gif)puis cliquez sur **modifier** ![l’icône modifier.</span><span class="sxs-lookup"><span data-stu-id="0f011-115">In the EAC, go to **Permissions** \> **Admin roles**, click the role group that you want to add the user or users to, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>

2. <span data-ttu-id="0f011-116">Sous membres, cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône Ajouter.</span><span class="sxs-lookup"><span data-stu-id="0f011-116">Under Members, click **Add** ![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="0f011-117">La fenêtre Sélectionner les membres s'affiche.</span><span class="sxs-lookup"><span data-stu-id="0f011-117">The Select Members window will appear.</span></span>

3. <span data-ttu-id="0f011-118">Recherchez le ou les utilisateurs à ajouter, ou sélectionnez-les dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0f011-118">Search for the user or users that you wish to add, or select them from the list.</span></span>

4. <span data-ttu-id="0f011-p105">Lorsque vous avez sélectionné les utilisateurs à ajouter, cliquez sur **Ajouter**, puis sur **OK**. La fenêtre Sélectionner les membres se ferme.</span><span class="sxs-lookup"><span data-stu-id="0f011-p105">When you have selected the user or users that you want to add, click **Add**, and then click **OK**. The Select Members window will close.</span></span>

5. <span data-ttu-id="0f011-p106">Vous constatez que les utilisateurs ont été ajoutés au volet **Membres**. Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0f011-p106">You will see that the user has been added to the **Members** pane. Click **Save**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0f011-123">Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.</span><span class="sxs-lookup"><span data-stu-id="0f011-123">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span>

## <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a><span data-ttu-id="0f011-124">Utiliser le Centre d'administration Exchange (CAE) pour supprimer des membres de groupes de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="0f011-124">Use the EAC to remove members from admin role groups</span></span>

1. <span data-ttu-id="0f011-125">Dans le centre d’administration Exchange, accédez à **rôles d’administrateur**des **autorisations** \> , cliquez sur le groupe de rôles duquel vous souhaitez supprimer un ou les utilisateurs, puis](../media/ITPro-EAC-EditIcon.gif)cliquez sur **modifier** ![l’icône de modification.</span><span class="sxs-lookup"><span data-stu-id="0f011-125">In the EAC, go to **Permissions** \> **Admin Roles**, click the role group that you want to remove a user or users from, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>

2. <span data-ttu-id="0f011-126">Sous membres, sélectionnez le ou les utilisateurs que vous souhaitez supprimer, puis cliquez sur **supprimer** ![l'](../media/ITPro-EAC-RemoveIcon.gif)icône Supprimer.</span><span class="sxs-lookup"><span data-stu-id="0f011-126">Under Members, select the user or users that you want to remove and click **Remove** ![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>

3. <span data-ttu-id="0f011-p107">Cliquez sur **Enregistrer** pour enregistrer la modification apportée au groupe de rôles et retourner à la page **Rôles d'administrateur**. Pour vérifier que vous avez supprimé l'utilisateur du groupe de rôles d'administrateur, assurez-vous que le membre n'apparaît plus sous Membres dans le volet Détails relatif au groupe de rôles sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0f011-p107">Click **Save** to save the change to the role group and return to the **Admin Roles** page. To verify that you've successfully removed the user from the administrator role group, make sure the member is no longer displayed under Members in the details pane for the selected role group.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0f011-129">Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.</span><span class="sxs-lookup"><span data-stu-id="0f011-129">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="0f011-130">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="0f011-130">For more information</span></span>

[<span data-ttu-id="0f011-131">Autorisations des fonctionnalités dans EOP</span><span class="sxs-lookup"><span data-stu-id="0f011-131">Feature permissions in EOP</span></span>](feature-permissions-in-eop.md)
