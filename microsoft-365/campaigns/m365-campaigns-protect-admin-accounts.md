---
title: Protéger vos comptes d’administrateur
ms.author: sirkkuw
author: sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-Campaigns
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
description: Découvrez comment configurer et protéger vos comptes d’administrateur.
ms.openlocfilehash: 33bf7f8a2a1e666a7822be1d52ac2d81fc681230
ms.sourcegitcommit: 75b97d1ff617bc4b1b0ef9135dfe6a8842ea1b52
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35772471"
---
# <a name="protect-your-administrator-accounts"></a><span data-ttu-id="f7973-103">Protéger vos comptes d’administrateur</span><span class="sxs-lookup"><span data-stu-id="f7973-103">Protect your administrator accounts</span></span>

<span data-ttu-id="f7973-104">Étant donné que les comptes administrateurs sont dotés de privilèges élevés, ils sont précieux pour les pirates et les cybercriminels.</span><span class="sxs-lookup"><span data-stu-id="f7973-104">Because the admin accounts come with elevated privileges, they are valuable targets for hackers and cyber criminals.</span></span> <span data-ttu-id="f7973-105">Cet article décrit les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="f7973-105">This article describes:</span></span>

- <span data-ttu-id="f7973-106">La configuration d’un compte d’administrateur supplémentaire pour les situations d’urgence.</span><span class="sxs-lookup"><span data-stu-id="f7973-106">How to set up an additional administrator account for emergencies.</span></span>
- <span data-ttu-id="f7973-107">Comment protéger ces comptes.</span><span class="sxs-lookup"><span data-stu-id="f7973-107">How to protect these accounts.</span></span>
 
<span data-ttu-id="f7973-108">Lorsque vous vous inscrivez à Microsoft 365 Business et que vous entrez vos informations, vous devenez automatiquement administrateur général. Un administrateur global a le contrôle ultime des comptes d’utilisateurs et de tous les autres paramètres dans le centre d’administration Microsoft, mais il existe de nombreux types de comptes d’administrateur avec différents degrés d’accès.</span><span class="sxs-lookup"><span data-stu-id="f7973-108">When you sign up for Microsoft 365 Business and enter your information, you automatically become the global admin. A global admin has the ultimate control of user accounts and all the other settings in the Microsoft admin center, but there are many different kinds of admin accounts with varying degrees of access.</span></span> <span data-ttu-id="f7973-109">Pour plus d’informations sur les différents niveaux d’accès pour chaque type de rôle d’administrateur, consultez la rubrique [à propos des rôles d’administrateur](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .</span><span class="sxs-lookup"><span data-stu-id="f7973-109">See [about admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) for information about the different access levels for each kind of admin role.</span></span>


## <a name="create-additional-admin-accounts"></a><span data-ttu-id="f7973-110">Créer des comptes d’administration supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f7973-110">Create additional admin accounts</span></span>

<span data-ttu-id="f7973-111">Utilisez les comptes administrateur uniquement pour l’administration.</span><span class="sxs-lookup"><span data-stu-id="f7973-111">Use admin accounts only for administration.</span></span> <span data-ttu-id="f7973-112">Les administrateurs doivent disposer d’un compte d’utilisateur distinct pour utiliser régulièrement les applications Office et utiliser uniquement leur compte administratif si nécessaire pour gérer les comptes, les appareils et les autres fonctions d’administration.</span><span class="sxs-lookup"><span data-stu-id="f7973-112">Admins should have a separate user account for regular use of Office apps and only use their administrative account when necessary to manage accounts, devices and while working on other admin functions.</span></span> <span data-ttu-id="f7973-113">Il est également recommandé de supprimer la licence d’entreprise Microsoft 365 des comptes administrateur afin de ne pas avoir à les payer.</span><span class="sxs-lookup"><span data-stu-id="f7973-113">It is also a good idea to remove the Microsoft 365 Business license from the admin accounts so you don't have to pay for them.</span></span>

<span data-ttu-id="f7973-114">Vous devez configurer au moins un compte d’administrateur global supplémentaire pour accorder un accès administrateur à un autre employé approuvé.</span><span class="sxs-lookup"><span data-stu-id="f7973-114">You'll want to set up at least one additional global admin account to give admin access to another trusted employee.</span></span> <span data-ttu-id="f7973-115">Vous pouvez également créer des comptes d’administration distincts pour la gestion des utilisateurs (ce rôle est appelé **administrateur de gestion des utilisateurs**).</span><span class="sxs-lookup"><span data-stu-id="f7973-115">You can also create separate admin accounts for user management (this role is called **User management administrator**).</span></span> <span data-ttu-id="f7973-116">Pour plus d’informations, consultez la rubrique [à propos des rôles d’administrateur](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .</span><span class="sxs-lookup"><span data-stu-id="f7973-116">See [about admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) for more information.</span></span>

<span data-ttu-id="f7973-117">Pour créer des comptes d’administration supplémentaires:</span><span class="sxs-lookup"><span data-stu-id="f7973-117">To create additional admin accounts:</span></span>

 1. <span data-ttu-id="f7973-118">Accédez au centre d' <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">administration</a> , puis sélectionnez \*\*\*\* \> utilisateurs **actifs** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="f7973-118">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span></span>

    ![Sélectionnez utilisateurs, puis utilisateurs actifs dans le volet de navigation de gauche](media/Activeusers.png)

2. <span data-ttu-id="f7973-120">Dans la page **utilisateurs actifs** , sélectionnez **Ajouter un utilisateur** en haut de la page et, dans le panneau **nouvel utilisateur** , entrez le nom et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="f7973-120">On the **Active users** page select **Add a user** on the top of the page and on the **New user** panel,  enter the name and other information.</span></span>
3. <span data-ttu-id="f7973-121">Développez la section **rôles** , puis choisissez **administrateur général** pour accorder à cet utilisateur l’accès administrateur global.</span><span class="sxs-lookup"><span data-stu-id="f7973-121">Expand the **Roles** section, and choose **Global administrator** to give this user global admin access.</span></span> <span data-ttu-id="f7973-122">Vous pouvez également choisir **administrateur personnalisé** et choisir l’un des rôles affichés.</span><span class="sxs-lookup"><span data-stu-id="f7973-122">You can also choose **Customized administrator** and choose any of the roles that are displayed.</span></span>

    <span data-ttu-id="f7973-123">Entrez un autre message dans la zone de texte adresse de messagerie de substitution.</span><span class="sxs-lookup"><span data-stu-id="f7973-123">Enter an alternate email in the Alternative email address text box.</span></span> <span data-ttu-id="f7973-124">Vous pouvez utiliser cette adresse pour récupérer vos informations de mot de passe si vous êtes verrouillé. Pour les administrateurs globaux, une déclaration de facturation est également envoyée à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="f7973-124">You can use this address to recover your password information if you get locked out. For global admins, a billing statement will also be sent to this address.</span></span>

    ![Choisir le rôle d’administrateur](media/adminroles.png)
    
4. <span data-ttu-id="f7973-126">Dans la **section licences de produit** , déplacez le sélecteur de **Microsoft 365 entreprise** sur **désactivé** et l' **utilisateur créer sans licence** de \*\*\*\* produit sur activé.</span><span class="sxs-lookup"><span data-stu-id="f7973-126">In the **Product licenses** section, move the selector for **Microsoft 365 Business** to **Off** and the **Create user without product license** to **On**.</span></span>

    ![Choisir la licence de produit](media/productlicense.png)

## <a name="create-an-emergency-admin-account"></a><span data-ttu-id="f7973-128">Créer un compte d’administrateur d’urgence</span><span class="sxs-lookup"><span data-stu-id="f7973-128">Create an emergency admin account</span></span>

<span data-ttu-id="f7973-129">Vous devez également créer un compte de sauvegarde qui n’est pas configuré avec l’authentification multifacteur (MFA), afin de ne pas vous verrouiller accidentellement (par exemple, si vous perdez votre téléphone que vous utilisez en tant que seconde à partir de la vérification).</span><span class="sxs-lookup"><span data-stu-id="f7973-129">You should also create a backup account that isn't set up with multi-factor authentication (MFA) so you don't accidentally lock yourself out (for example if you lose your phone that you are using as a second from of verification).</span></span> <span data-ttu-id="f7973-130">Assurez-vous que le mot de passe de ce compte est une phrase ou au moins 16 caractères.</span><span class="sxs-lookup"><span data-stu-id="f7973-130">Make sure that the password for this account is a phrase or at least 16 characters long.</span></span> <span data-ttu-id="f7973-131">On parle souvent de «compte de saut de ligne».</span><span class="sxs-lookup"><span data-stu-id="f7973-131">This is often referred to as a "break-glass account."</span></span>

## <a name="create-a-user-account-for-yourself"></a><span data-ttu-id="f7973-132">Créer un compte d’utilisateur pour vous-même</span><span class="sxs-lookup"><span data-stu-id="f7973-132">Create a user account for yourself</span></span>

<span data-ttu-id="f7973-133">Utilisez votre compte d’utilisateur pour participer à la collaboration avec votre organisation, notamment en vérifiant le courrier.</span><span class="sxs-lookup"><span data-stu-id="f7973-133">Use your user account to participate in collaboration with your organization, including checking mail.</span></span> <span data-ttu-id="f7973-134">Cela signifie que vos informations d’identification d’administrateur peuvent ressembler à *Alice. Chavez<span></span>@Contoso. org* et que votre compte d’utilisateur normal ressemble à *Alice<span></span>@Contoso. com*.</span><span class="sxs-lookup"><span data-stu-id="f7973-134">This means your admin credentials might be similar to  *Alice.Chavez<span></span>@Contoso.org* and your regular user account might be similar to *Alice<span></span>@Contoso.com*.</span></span>

<span data-ttu-id="f7973-135">Pour créer un compte d’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="f7973-135">To create a new user account:</span></span>
1. <span data-ttu-id="f7973-136">Accédez au centre d' <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">administration</a> , puis sélectionnez \*\*\*\* \> utilisateurs **actifs** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="f7973-136">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span></span>
2. <span data-ttu-id="f7973-137">Dans la page **utilisateurs actifs** , sélectionnez **Ajouter un utilisateur** en haut de la page et, dans le panneau **nouvel utilisateur** , entrez le nom et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="f7973-137">On the **Active users** page select **Add a user** on the top of the page and on the **New user** panel,  enter the name and other information.</span></span>
3. <span data-ttu-id="f7973-138">Développez la section **rôles** , puis choisissez **utilisateur (pas d’accès administratif)**.</span><span class="sxs-lookup"><span data-stu-id="f7973-138">Expand the **Roles** section, and choose **User (no administrative access)**.</span></span>
1. <span data-ttu-id="f7973-139">Dans la section **licences de produit** , déplacez le sélecteur de **Microsoft 365 Business** vers **activé**.</span><span class="sxs-lookup"><span data-stu-id="f7973-139">In the **Product licenses** section, move the selector for **Microsoft 365 Business** to **On**.</span></span> 

## <a name="register-each-of-these-accounts-for-multi-factor-authentication"></a><span data-ttu-id="f7973-140">Enregistrer chacun de ces comptes pour l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="f7973-140">Register each of these accounts for multi-factor authentication</span></span>


## <a name="additional-recommendations"></a><span data-ttu-id="f7973-141">Recommandations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f7973-141">Additional recommendations</span></span>

- <span data-ttu-id="f7973-142">Assurez-vous que les comptes administrateur sont également configurés pour l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="f7973-142">Be sure that admin accounts are also set up for multi-factor authentication.</span></span> <span data-ttu-id="f7973-143">Nous allons vous montrer comment procéder dans configurer les [stratégies d’accès conditionnel](m365-campaigns-conditional-access.md).</span><span class="sxs-lookup"><span data-stu-id="f7973-143">We'll show you how to do this in [Configure conditional access policies](m365-campaigns-conditional-access.md).</span></span>
- <span data-ttu-id="f7973-144">Avant d’utiliser les comptes d’administrateur, fermez toutes les sessions de navigateur et les applications qui ne sont pas associées, y compris les comptes de messagerie personnels.</span><span class="sxs-lookup"><span data-stu-id="f7973-144">Before using admin accounts, close out all unrelated browser sessions and apps, including personal email accounts.</span></span> <span data-ttu-id="f7973-145">Vous pouvez également utiliser dans des fenêtres de navigateur privées ou incognito.</span><span class="sxs-lookup"><span data-stu-id="f7973-145">You can also use in private, or incognito browser windows.</span></span>
- <span data-ttu-id="f7973-146">Après avoir effectué les tâches d’administration, veillez à vous déconnecter de la session du navigateur.</span><span class="sxs-lookup"><span data-stu-id="f7973-146">After completing admin tasks, be sure to sign out of the browser session.</span></span>