---
title: Comparer les méthodes de blocage d’accès
f1.keywords:
- NOCSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5785d21d-1abd-4571-a04a-8cc5a65ca9b5
ROBOTS: NOINDEX
description: Découvrez comment bloquer l’accès aux Microsoft 365 lorsqu’un employé quitte votre organisation.
ms.openlocfilehash: b913655065d4c57322aee6dc04e53f7a35cf5760
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399433"
---
# <a name="compare-ways-to-block-access"></a><span data-ttu-id="97364-103">Comparer les méthodes de blocage d’accès</span><span class="sxs-lookup"><span data-stu-id="97364-103">Compare ways to block access</span></span>

<span data-ttu-id="97364-104">Lorsqu’un employé quitte votre organisation, dans de bonnes conditions ou dans de mauvaises conditions, vous devez bloquer son accès à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="97364-104">When an employee leaves your organization, on good terms or bad, you need to block their access to Microsoft 365.</span></span> <span data-ttu-id="97364-105">Voici quelques façons de le faire.</span><span class="sxs-lookup"><span data-stu-id="97364-105">Here are a few ways you can do that.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="97364-106">**Moyen de bloquer l’accès**</span><span class="sxs-lookup"><span data-stu-id="97364-106">**Way to block access**</span></span> <br/> |<span data-ttu-id="97364-107">**Définition**</span><span class="sxs-lookup"><span data-stu-id="97364-107">**Definition**</span></span> <br/> |<span data-ttu-id="97364-108">**Meilleure pratique**</span><span class="sxs-lookup"><span data-stu-id="97364-108">**Best practice**</span></span> <br/> |
|<span data-ttu-id="97364-109">Bloquer la sign-in</span><span class="sxs-lookup"><span data-stu-id="97364-109">Block sign-in</span></span>  <br/> |<span data-ttu-id="97364-110">Une façon d’empêcher un utilisateur d’accéder à Microsoft 365 consiste à modifier son statut de sign-in en **Sign-in blocked**.</span><span class="sxs-lookup"><span data-stu-id="97364-110">One way to block a user from accessing Microsoft 365 is to change their sign-in status to **Sign-in blocked**.</span></span> <span data-ttu-id="97364-111">Cela les empêche de se Microsoft 365 à partir de leurs ordinateurs et appareils mobiles, même s’ils peuvent toujours afficher des e-mails et des documents précédemment téléchargés ou synchronisés.</span><span class="sxs-lookup"><span data-stu-id="97364-111">This prevents them from signing into Microsoft 365 from their computers and mobile devices though they can still view previously downloaded or synced email and documents.</span></span> <span data-ttu-id="97364-112">Si vous utilisez Blackberry Enterprise Service, vous pouvez également désactiver leur accès.</span><span class="sxs-lookup"><span data-stu-id="97364-112">If you're using Blackberry Enterprise Service, you can disable their access there as well.</span></span>  <br/> |<span data-ttu-id="97364-113">À utiliser lorsqu’un employé prévoit de quitter l’organisation ou s’il prévoit de prendre un congé à long terme.</span><span class="sxs-lookup"><span data-stu-id="97364-113">Use when an employee plans to leave the organization or they plan to take a long-term leave of absence.</span></span>  <br/> |
|<span data-ttu-id="97364-114">Réinitialiser le mot de passe de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="97364-114">Reset user password</span></span>  <br/> |<span data-ttu-id="97364-115">Une autre façon d’empêcher un utilisateur d’accéder aux Microsoft 365 consiste à réinitialiser son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="97364-115">Another way to prevent a user from accessing Microsoft 365 is to reset their password.</span></span> <span data-ttu-id="97364-116">Cela les empêche d’utiliser leur compte même s’ils peuvent toujours afficher des e-mails et des documents précédemment téléchargés ou synchronisés.</span><span class="sxs-lookup"><span data-stu-id="97364-116">This prevents them from using their account though they can still view previously downloaded or synced email and documents.</span></span> <span data-ttu-id="97364-117">Vous pouvez ensuite vous y inscrire en tant que tel et modifier le mot de passe en l’un de vos choix.</span><span class="sxs-lookup"><span data-stu-id="97364-117">You can then sign in as them and change the password to one of your choosing.</span></span>  <br/> |<span data-ttu-id="97364-118">À utiliser lorsqu’un employé quitte soudainement et définitivement et que vous vous sentez préoccupé par les données métiers.</span><span class="sxs-lookup"><span data-stu-id="97364-118">Use when an employee leaves suddenly and permanently and you feel there is concern for business data.</span></span>  <br/> |
|<span data-ttu-id="97364-119">Supprimer toutes les licences attribuées</span><span class="sxs-lookup"><span data-stu-id="97364-119">Remove all assigned licenses</span></span>  <br/> |<span data-ttu-id="97364-120">Une autre option consiste à supprimer les licences Microsoft 365 attribuées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97364-120">Another option is to remove any Microsoft 365 licenses assigned to the user.</span></span> <span data-ttu-id="97364-121">Cela les empêche d’utiliser des applications et des services tels que la suite Office, les applications Office pour le web, Yammer et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="97364-121">This prevents them from using applications and services like the Office suite, Office apps for the web, Yammer, and SharePoint Online.</span></span> <span data-ttu-id="97364-122">Ils peuvent toujours se connecter, mais ne peuvent pas utiliser ces services.</span><span class="sxs-lookup"><span data-stu-id="97364-122">They can still sign in but cannot use these services.</span></span>  <br/> |<span data-ttu-id="97364-123">À utiliser lorsque vous pensez que cet utilisateur n’a plus besoin d’accéder à des fonctionnalités spécifiques Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="97364-123">Use when you feel this user no longer needs access to specific features in Microsoft 365.</span></span>  <br/> <br> <span data-ttu-id="97364-124">**Important :** Lorsque vous supprimez une licence, la boîte aux lettres de l’utilisateur est supprimée dans 30 jours.</span><span class="sxs-lookup"><span data-stu-id="97364-124">**Important:** When you remove a license, the user's mailbox will be deleted in 30 days.</span></span>
   
## <a name="related-articles"></a><span data-ttu-id="97364-125">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="97364-125">Related articles</span></span>

[<span data-ttu-id="97364-126">Hors de la base de données d’un Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="97364-126">Offboard a user from Microsoft 365</span></span>](../add-users/remove-former-employee.md)
    
[<span data-ttu-id="97364-127">Réinitialiser le mot de passe d’un utilisateur dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="97364-127">Reset a user's password in Microsoft 365</span></span>](../add-users/reset-passwords.md)
    
[<span data-ttu-id="97364-128">Attribuer des licences à des utilisateurs Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="97364-128">Assign licenses to users in Microsoft 365 for business</span></span>](../manage/assign-licenses-to-users.md)
    
[<span data-ttu-id="97364-129">Supprimer des licences d’utilisateurs Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="97364-129">Remove licenses from users in Microsoft 365 for business</span></span>](../manage/remove-licenses-from-users.md)
    

