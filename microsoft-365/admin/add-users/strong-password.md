---
title: Définir une condition de mot de passe fort pour les utilisateurs
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
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment définir des exigences de mots de passe forts pour vos utilisateurs, à l’aide de Windows PowerShell.
ms.openlocfilehash: 1230ff4b4235ac5acbc28aa823506dfa5af26c2d
ms.sourcegitcommit: 3165329d1fb5a7fd866ff287bea3b6354ea2be18
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2020
ms.locfileid: "48581019"
---
# <a name="set-strong-password-requirement-for-users"></a><span data-ttu-id="6eed5-103">Définir une condition de mot de passe fort pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6eed5-103">Set strong password requirement for users</span></span>

<span data-ttu-id="6eed5-104">Cet article explique comment définir les exigences de mots de passe forts pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6eed5-104">This article explains how to set strong password requirements for your users.</span></span> <span data-ttu-id="6eed5-105">Vous devez effectuer ces étapes à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6eed5-105">You have to complete these steps using PowerShell.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="6eed5-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6eed5-106">Before you begin</span></span>

<span data-ttu-id="6eed5-107">Cet article est destiné aux personnes qui gèrent la stratégie de mot de passe pour une entreprise, une école ou une organisation caritative.</span><span class="sxs-lookup"><span data-stu-id="6eed5-107">This article is for people who manage password policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="6eed5-108">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6eed5-108">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> <span data-ttu-id="6eed5-109">[Qu’est-ce qu’un compte d’administrateur ?](../admin-overview/admin-overview.md)</span><span class="sxs-lookup"><span data-stu-id="6eed5-109">[What's an admin account?](../admin-overview/admin-overview.md).</span></span> <span data-ttu-id="6eed5-110">Pour effectuer ces étapes, vous devez être [administrateur général ou administrateur de mots de passe](about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="6eed5-110">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

<span data-ttu-id="6eed5-111">Vous devez également vous connecter à Microsoft 365 avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6eed5-111">You must also connect to Microsoft 365 with PowerShell.</span></span>

## <a name="set-strong-passwords"></a><span data-ttu-id="6eed5-112">Définir des mots de passe forts</span><span class="sxs-lookup"><span data-stu-id="6eed5-112">Set strong passwords</span></span>

1. <span data-ttu-id="6eed5-113">[Connectez-vous à Microsoft 365 avec PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="6eed5-113">[Connect to Microsoft 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

2. <span data-ttu-id="6eed5-114">À l’aide de PowerShell, vous pouvez désactiver les mots de passe forts pour des utilisateurs spécifiques à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="6eed5-114">Using PowerShell, you can disable strong passwords for specific users with this command:</span></span>

    ```powershell
    Set-MsolUser –UserPrincipalName –StrongPasswordRequired  $false
    ```

> [!NOTE]
> <span data-ttu-id="6eed5-115">Le userPrincipalName doit être au format de connexion de style Internet, où le nom d’utilisateur est suivi par le signe arobase (@) et un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="6eed5-115">The userPrincipalName must be in the Internet-style sign-in format where the user name is followed by the at sign (@) and a domain name.</span></span> <span data-ttu-id="6eed5-116">Par exemple : user@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="6eed5-116">For example: user@contoso.com.</span></span>

## <a name="related-content"></a><span data-ttu-id="6eed5-117">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="6eed5-117">Related content</span></span>

[<span data-ttu-id="6eed5-118">Comment se connecter à Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="6eed5-118">How to connect to Microsoft 365 with PowerShell</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)

[<span data-ttu-id="6eed5-119">Plus d’informations sur les commandes MsolUser de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6eed5-119">More information on PowerShell MsolUser commands</span></span>](https://docs.microsoft.com/powershell/module/msonline/set-msoluser?view=azureadps-1.0)

[<span data-ttu-id="6eed5-120">Plus d’informations sur la stratégie de mot de passe</span><span class="sxs-lookup"><span data-stu-id="6eed5-120">More information on password policy</span></span>](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts)