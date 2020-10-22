---
title: Désactiver les exigences de mot de passe renforcé pour les utilisateurs
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
ms.openlocfilehash: f9a0b76d024cc18552657144e4ccf8de8a72f0d9
ms.sourcegitcommit: 3b1bd8aa1430bc9565743a446bbc27b199f30f73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "48655734"
---
# <a name="turn-off-strong-password-requirements-for-users"></a><span data-ttu-id="b81b4-103">Désactiver les exigences de mot de passe renforcé pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b81b4-103">Turn off strong password requirements for users</span></span>

<span data-ttu-id="b81b4-104">Cet article explique comment désactiver les exigences de mot de passe renforcé pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b81b4-104">This article explains how to turn off strong password requirements for your users.</span></span> <span data-ttu-id="b81b4-105">Les exigences de mot de passe fort sont activées par défaut dans votre organisation Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="b81b4-105">Strong password requirements are turned on by default in your Microsoft 365 for business organization.</span></span> <span data-ttu-id="b81b4-106">Votre organisation peut avoir besoin de désactiver des mots de passe forts.</span><span class="sxs-lookup"><span data-stu-id="b81b4-106">Your organization might have requirements to disable strong passwords.</span></span> <span data-ttu-id="b81b4-107">Suivez les étapes ci-dessous pour désactiver les exigences de mot de passe renforcé.</span><span class="sxs-lookup"><span data-stu-id="b81b4-107">Follow the steps below to turn off strong password requirements.</span></span> <span data-ttu-id="b81b4-108">Vous devez effectuer ces étapes à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b81b4-108">You have to complete these steps using PowerShell.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b81b4-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b81b4-109">Before you begin</span></span>

<span data-ttu-id="b81b4-110">Cet article est destiné aux personnes qui gèrent la stratégie de mot de passe pour une entreprise, une école ou une organisation caritative.</span><span class="sxs-lookup"><span data-stu-id="b81b4-110">This article is for people who manage password policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="b81b4-111">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b81b4-111">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> [<span data-ttu-id="b81b4-112">Qu’est-ce qu’un compte administrateur ?</span><span class="sxs-lookup"><span data-stu-id="b81b4-112">What's an admin account?</span></span>](../admin-overview/admin-overview.md) <span data-ttu-id="b81b4-113">Pour effectuer ces étapes, vous devez être [administrateur général ou administrateur de mots de passe](about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="b81b4-113">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

<span data-ttu-id="b81b4-114">Vous devez également vous connecter à Microsoft 365 avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b81b4-114">You must also connect to Microsoft 365 with PowerShell.</span></span>

## <a name="set-strong-passwords"></a><span data-ttu-id="b81b4-115">Définir des mots de passe forts</span><span class="sxs-lookup"><span data-stu-id="b81b4-115">Set strong passwords</span></span>

1. <span data-ttu-id="b81b4-116">[Connectez-vous à Microsoft 365 avec PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="b81b4-116">[Connect to Microsoft 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

2. <span data-ttu-id="b81b4-117">À l’aide de PowerShell, vous pouvez désactiver les exigences de mot de passe renforcé pour tous les utilisateurs à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b81b4-117">Using PowerShell, you can turn off strong password requirements for all users with the following command:</span></span>

    ```powershell
    Get-MsolUser | Set-MsolUser -StrongPasswordRequired $false

3. You can turn of strong password requirements for specific users with this command:

    ```powershell
    Set-MsolUser –UserPrincipalName –StrongPasswordRequired  $false
    ```

> [!NOTE]
> <span data-ttu-id="b81b4-118">Le userPrincipalName doit être au format de connexion de style Internet, où le nom d’utilisateur est suivi par le signe arobase (@) et un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="b81b4-118">The userPrincipalName must be in the Internet-style sign-in format where the user name is followed by the at sign (@) and a domain name.</span></span> <span data-ttu-id="b81b4-119">Par exemple : user@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="b81b4-119">For example: user@contoso.com.</span></span>

## <a name="related-content"></a><span data-ttu-id="b81b4-120">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="b81b4-120">Related content</span></span>

[<span data-ttu-id="b81b4-121">Comment se connecter à Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="b81b4-121">How to connect to Microsoft 365 with PowerShell</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)

[<span data-ttu-id="b81b4-122">Plus d’informations sur les commandes MsolUser de PowerShell</span><span class="sxs-lookup"><span data-stu-id="b81b4-122">More information on PowerShell MsolUser commands</span></span>](https://docs.microsoft.com/powershell/module/msonline/set-msoluser?view=azureadps-1.0)

[<span data-ttu-id="b81b4-123">Plus d’informations sur la stratégie de mot de passe</span><span class="sxs-lookup"><span data-stu-id="b81b4-123">More information on password policy</span></span>](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts)