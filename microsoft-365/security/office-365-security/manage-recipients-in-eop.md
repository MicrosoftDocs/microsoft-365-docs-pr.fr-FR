---
title: Gestion des destinataires dans Exchange Online Protection (EOP)
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: Microsoft Exchange Online Protection (EOP) vous propose plusieurs façons de gérer vos destinataires de message. En tant qu’administrateur, vous pouvez effectuer certaines tâches de gestion dans le centre d’administration Exchange ou à l’aide de Windows PowerShell à distance et vérifier les autres tâches de gestion effectuées dans le centre d’administration 365 de Microsoft.
ms.openlocfilehash: 6b56bcf725fe461c7e059658e7981f27bd4c07eb
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080312"
---
# <a name="manage-recipients-in-eop"></a><span data-ttu-id="2d6d6-104">Gestion des destinataires dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="2d6d6-104">Manage recipients in EOP</span></span>

<span data-ttu-id="2d6d6-105">Microsoft Exchange Online Protection (EOP) vous propose plusieurs façons de gérer vos destinataires de message.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-105">Microsoft Exchange Online Protection (EOP) offers several ways to manage your mail recipients.</span></span> <span data-ttu-id="2d6d6-106">En tant qu’administrateur, vous pouvez effectuer certaines tâches de gestion dans le centre d’administration Exchange ou à l’aide de Windows PowerShell à distance et vérifier les autres tâches de gestion effectuées dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-106">As an administrator, you can perform certain management tasks within the Exchange admin center (EAC) or using remote Windows PowerShell, and verify other management tasks performed in the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="2d6d6-107">EOP prend en charge les types de destinataires suivants :</span><span class="sxs-lookup"><span data-stu-id="2d6d6-107">EOP supports the following types of recipients:</span></span>
  
- <span data-ttu-id="2d6d6-108">**Utilisateurs de messagerie**: les utilisateurs de messagerie sont des destinataires de vos domaines gérés EOP.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-108">**Mail Users**: Mail users are recipients in your EOP managed domains.</span></span> <span data-ttu-id="2d6d6-109">Ces destinataires ont des informations d’identification d’ouverture de session dans votre organisation Office 365, mais elles ont des adresses de messagerie externes, ce qui signifie que leurs boîtes aux lettres de destinataire se trouvent en dehors de votre organisation en nuage.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-109">These recipients have logon credentials in your Office 365 organization, but they have external email addresses, meaning that their recipient mailboxes are located outside of your cloud organization.</span></span>

  <span data-ttu-id="2d6d6-110">Vous pouvez ajouter des utilisateurs de messagerie afin qu’ils puissent recevoir des messages et que vous puissiez également créer des règles de flux de messagerie (également appelées règles de transport) pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-110">You can add mail users so that they can receive mail and you can also create mail flow rules (also known as transport rules) for specific users.</span></span> <span data-ttu-id="2d6d6-111">Vous pouvez également attribuer des rôles aux utilisateurs de messagerie de votre organisation ; les utilisateurs disposant de privilèges de groupe de rôles de gestion peuvent accéder au centre d’administration Exchange et effectuer certaines tâches de gestion.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-111">You can also assign roles to mail users in your organization; users with management role group privileges can access the Exchange admin center (EAC) and perform certain management tasks.</span></span> <span data-ttu-id="2d6d6-112">Pour en savoir plus sur les rôles d’utilisateur et sur l’attribution de rôles d’utilisateur dans EOP, consultez la rubrique [Manage admin Role Group Permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="2d6d6-112">To learn more about user roles and how to assign user roles in EOP, see [Manage admin role group permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span></span>

  <span data-ttu-id="2d6d6-113">Pour plus d'informations sur la gestion des utilisateurs de messagerie dans EOP, consultez la rubrique [Gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="2d6d6-113">For more information about managing mail users in EOP, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>

- <span data-ttu-id="2d6d6-114">**Groupes**: les utilisateurs de messagerie peuvent être regroupés dans des groupes de distribution ou des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2d6d6-114">**Groups**: Mail users can be grouped together into distribution groups or security groups.</span></span>

<span data-ttu-id="2d6d6-115">Pour plus d'informations sur la gestion des groupes dans EOP, consultez la rubrique [Gestion des groupes dans Exchange Online Protection (EOP)](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="2d6d6-115">For more information about managing groups in EOP, see [Manage groups in EOP](manage-groups-in-eop.md).</span></span>
