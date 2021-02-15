---
title: Protéger vos comptes d’administrateur
f1.keywords:
- NOCSH
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
- m365solution-smb
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
description: Découvrez comment configurer et protéger vos comptes d’administrateur.
ms.openlocfilehash: 73e4b69571b1e1d0a4d1585224fe256ff135c40a
ms.sourcegitcommit: 1b30ac6e05906c8a014b1fed33fc71e1821f6ad2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "50044487"
---
# <a name="protect-your-administrator-accounts"></a><span data-ttu-id="e3da9-103">Protéger vos comptes d’administrateur</span><span class="sxs-lookup"><span data-stu-id="e3da9-103">Protect your administrator accounts</span></span>

<span data-ttu-id="e3da9-104">Étant donné que les comptes d’administrateur ont des privilèges élevés, ils sont des cibles précieuses pour les pirates informatiques et les cybercriminels.</span><span class="sxs-lookup"><span data-stu-id="e3da9-104">Because admin accounts come with elevated privileges, they're valuable targets for hackers and cyber criminals.</span></span> <span data-ttu-id="e3da9-105">Cet article décrit les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="e3da9-105">This article describes:</span></span>

- <span data-ttu-id="e3da9-106">Comment configurer un compte d’administrateur supplémentaire pour les urgences.</span><span class="sxs-lookup"><span data-stu-id="e3da9-106">How to set up an additional administrator account for emergencies.</span></span>
- <span data-ttu-id="e3da9-107">Comment protéger ces comptes.</span><span class="sxs-lookup"><span data-stu-id="e3da9-107">How to protect these accounts.</span></span>

<span data-ttu-id="e3da9-108">Lorsque vous vous inscrivez à Microsoft 365 et entrez vos informations, vous devenez automatiquement l’administrateur global. Un administrateur global a le contrôle ultime des comptes d’utilisateur et de tous les autres paramètres dans le Centre d’administration Microsoft, mais il existe de nombreux types de comptes d’administrateur avec différents degrés d’accès.</span><span class="sxs-lookup"><span data-stu-id="e3da9-108">When you sign up for Microsoft 365 and enter your information, you automatically become the global admin. A global admin has the ultimate control of user accounts and all the other settings in the Microsoft admin center, but there are many different kinds of admin accounts with varying degrees of access.</span></span> <span data-ttu-id="e3da9-109">Pour plus [d’informations sur](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) les différents niveaux d’accès pour chaque type de rôle d’administrateur, voir les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e3da9-109">See [about admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) for information about the different access levels for each kind of admin role.</span></span>

## <a name="create-additional-admin-accounts"></a><span data-ttu-id="e3da9-110">Créer des comptes d’administrateur supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e3da9-110">Create additional admin accounts</span></span>

<span data-ttu-id="e3da9-111">Utilisez des comptes d’administrateur uniquement pour l’administration.</span><span class="sxs-lookup"><span data-stu-id="e3da9-111">Use admin accounts only for administration.</span></span> <span data-ttu-id="e3da9-112">Les administrateurs doivent avoir un compte d’utilisateur distinct pour une utilisation régulière des applications Office et utiliser leur compte d’administration uniquement lorsque cela est nécessaire pour gérer les comptes et les appareils, et tout en travaillant sur d’autres fonctions d’administration.</span><span class="sxs-lookup"><span data-stu-id="e3da9-112">Admins should have a separate user account for regular use of Office apps and only use their administrative account when necessary to manage accounts and devices, and while working on other admin functions.</span></span> <span data-ttu-id="e3da9-113">Il est également bon de supprimer la licence Microsoft 365 des comptes d’administrateur afin de ne pas avoir à les payer.</span><span class="sxs-lookup"><span data-stu-id="e3da9-113">It's also a good idea to remove the Microsoft 365 license from the admin accounts so you don't have to pay for them.</span></span>

<span data-ttu-id="e3da9-114">Vous pouvez configurer au moins un compte d’administrateur global supplémentaire pour accorder à l’administrateur l’accès à un autre employé approuvé.</span><span class="sxs-lookup"><span data-stu-id="e3da9-114">You'll want to set up at least one additional global admin account to give admin access to another trusted employee.</span></span> <span data-ttu-id="e3da9-115">Vous pouvez également créer des comptes d’administrateur distincts pour la gestion des utilisateurs (ce rôle est appelé **administrateur de gestion des utilisateurs).**</span><span class="sxs-lookup"><span data-stu-id="e3da9-115">You can also create separate admin accounts for user management (this role is called **User management administrator**).</span></span> <span data-ttu-id="e3da9-116">Pour plus d’informations, voir [les rôles d’administrateur.](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="e3da9-116">For more information, see [about admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span></span>

<span data-ttu-id="e3da9-117">Pour créer des comptes d’administrateur supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="e3da9-117">To create additional admin accounts:</span></span>

 1. <span data-ttu-id="e3da9-118">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="e3da9-118">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span></span>

    ![Sélectionnez Utilisateurs, puis Utilisateurs actifs dans le navigation gauche](../media/Activeusers.png)

 2. <span data-ttu-id="e3da9-120">Dans la page **Utilisateurs** actifs, sélectionnez Ajouter un utilisateur  en haut de la page, puis, dans le panneau Nouvel utilisateur, entrez le nom et d’autres informations. </span><span class="sxs-lookup"><span data-stu-id="e3da9-120">On the **Active users** page, select **Add a user** at the top of the page, and on the **New user** panel, enter the name and other information.</span></span>
 3. <span data-ttu-id="e3da9-121">Développez la section **Rôles,** puis choisissez **Administrateur général** pour accorder à cet utilisateur un accès d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="e3da9-121">Expand the **Roles** section, and choose **Global administrator** to give this user global admin access.</span></span> <span data-ttu-id="e3da9-122">Vous pouvez également choisir **un administrateur personnalisé et** choisir l’un des rôles affichés.</span><span class="sxs-lookup"><span data-stu-id="e3da9-122">You can also choose **Customized administrator** and choose any of the roles that are displayed.</span></span>

    <span data-ttu-id="e3da9-123">Entrez un autre message électronique dans la zone de texte **Adresse de messagerie** alternative.</span><span class="sxs-lookup"><span data-stu-id="e3da9-123">Enter an alternate email in the **Alternative email address** text box.</span></span> <span data-ttu-id="e3da9-124">Vous pouvez utiliser cette adresse pour récupérer les informations de votre mot de passe si vous êtes verrouillé. Pour les administrateurs globaux, un relevé de facturation est également envoyé à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="e3da9-124">You can use this address to recover your password information if you get locked out. For global admins, a billing statement will also be sent to this address.</span></span>

    ![Choisir le rôle d’administrateur](../media/adminroles.png)

 4. <span data-ttu-id="e3da9-126">Dans la section **Licences de** produits, déplacez le sélecteur de **Microsoft 365 Business** sur « **Hors** activité » et l’utilisateur Créer sans licence de produit **sur** **« On**».</span><span class="sxs-lookup"><span data-stu-id="e3da9-126">In the **Product licenses** section, move the selector for **Microsoft 365 Business** to **Off** and the **Create user without product license** to **On**.</span></span>

    ![Choisir la licence de produit](../media/productlicense.png)

## <a name="create-an-emergency-admin-account"></a><span data-ttu-id="e3da9-128">Créer un compte d’administrateur d’urgence</span><span class="sxs-lookup"><span data-stu-id="e3da9-128">Create an emergency admin account</span></span>

<span data-ttu-id="e3da9-129">Vous devez également créer un compte de sauvegarde qui n’est pas installé avec l’authentification multifacteur (MFA) afin de ne pas vous verrouiller accidentellement (par exemple, si vous perdez votre téléphone que vous utilisez comme deuxième forme de vérification).</span><span class="sxs-lookup"><span data-stu-id="e3da9-129">You should also create a backup account that isn't set up with multi-factor authentication (MFA) so you don't accidentally lock yourself out (for example if you lose your phone that you're using as a second form of verification).</span></span> <span data-ttu-id="e3da9-130">Assurez-vous que le mot de passe de ce compte est une expression d’au moins 16 caractères.</span><span class="sxs-lookup"><span data-stu-id="e3da9-130">Make sure that the password for this account is a phrase or at least 16 characters long.</span></span> <span data-ttu-id="e3da9-131">Ce compte est souvent appelé « compte à l’état « break-glass ».</span><span class="sxs-lookup"><span data-stu-id="e3da9-131">This is often referred to as a "break-glass account."</span></span>

## <a name="create-a-user-account-for-yourself"></a><span data-ttu-id="e3da9-132">Créer un compte d’utilisateur pour vous-même</span><span class="sxs-lookup"><span data-stu-id="e3da9-132">Create a user account for yourself</span></span>

<span data-ttu-id="e3da9-133">Utilisez votre compte d’utilisateur pour participer à la collaboration avec votre organisation, y compris la vérification de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="e3da9-133">Use your user account to participate in collaboration with your organization, including checking mail.</span></span> <span data-ttu-id="e3da9-134">Cela signifie que vos informations d’identification d’administrateur peuvent être similaires à  *Alice.Contrôlez <span></span> @Contoso.org* et que votre compte d’utilisateur normal peut être similaire à *Alice <span></span> @Contoso.com*.</span><span class="sxs-lookup"><span data-stu-id="e3da9-134">This means your admin credentials might be similar to  *Alice.Chavez <span></span>@Contoso.org* and your regular user account might be similar to *Alice<span></span>@Contoso.com*.</span></span>

<span data-ttu-id="e3da9-135">Pour créer un compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="e3da9-135">To create a new user account:</span></span>

1. <span data-ttu-id="e3da9-136">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="e3da9-136">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">admin center</a> and then choose **Users** \> **Active users** in the left nav.</span></span>
2. <span data-ttu-id="e3da9-137">Dans la page **Utilisateurs** actifs, sélectionnez Ajouter un utilisateur  en haut de la page, puis, dans le panneau Nouvel utilisateur, entrez le nom et d’autres informations. </span><span class="sxs-lookup"><span data-stu-id="e3da9-137">On the **Active users** page, select **Add a user** at the top of the page, and on the **New user** panel, enter the name and other information.</span></span>
3. <span data-ttu-id="e3da9-138">Développez la section **Rôles,** puis choisissez **Utilisateur (pas d’accès administratif).**</span><span class="sxs-lookup"><span data-stu-id="e3da9-138">Expand the **Roles** section, and choose **User (no administrative access)**.</span></span>
4. <span data-ttu-id="e3da9-139">Dans la section **Licences de produits,** déplacez le sélecteur **de Microsoft 365 Business** sur **On**.</span><span class="sxs-lookup"><span data-stu-id="e3da9-139">In the **Product licenses** section, move the selector for **Microsoft 365 Business** to **On**.</span></span>

## <a name="register-each-of-these-accounts-for-multi-factor-authentication"></a><span data-ttu-id="e3da9-140">Inscrire chacun de ces comptes pour l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="e3da9-140">Register each of these accounts for multi-factor authentication</span></span>

<span data-ttu-id="e3da9-141">Assurez-vous que ces comptes utilisent [l’authentification multifacteur.](m365-campaigns-multifactor-authenication.md)</span><span class="sxs-lookup"><span data-stu-id="e3da9-141">Make sure these accounts are using [multifactor authentication](m365-campaigns-multifactor-authenication.md).</span></span>

## <a name="additional-recommendations"></a><span data-ttu-id="e3da9-142">Recommandations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e3da9-142">Additional recommendations</span></span>

- <span data-ttu-id="e3da9-143">Assurez-vous que les comptes d’administrateur sont également mis en place pour l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="e3da9-143">Be sure that admin accounts are also set up for multi-factor authentication.</span></span> <span data-ttu-id="e3da9-144">Nous allons vous montrer comment faire dans [Configurer les stratégies d’accès conditionnel.](m365-campaigns-conditional-access.md)</span><span class="sxs-lookup"><span data-stu-id="e3da9-144">We'll show you how to do this in [Configure conditional access policies](m365-campaigns-conditional-access.md).</span></span>
- <span data-ttu-id="e3da9-145">Avant d’utiliser des comptes d’administrateur, fermez toutes les applications et sessions de navigateur non liées, y compris les comptes de messagerie personnels.</span><span class="sxs-lookup"><span data-stu-id="e3da9-145">Before using admin accounts, close out all unrelated browser sessions and apps, including personal email accounts.</span></span> <span data-ttu-id="e3da9-146">Vous pouvez également l’utiliser dans des fenêtres de navigateur privées ou privées.</span><span class="sxs-lookup"><span data-stu-id="e3da9-146">You can also use in private, or incognito browser windows.</span></span>
- <span data-ttu-id="e3da9-147">Après avoir terminé les tâches d’administration, n’oubliez pas de vous ausserer de la session du navigateur.</span><span class="sxs-lookup"><span data-stu-id="e3da9-147">After completing admin tasks, be sure to sign out of the browser session.</span></span>
