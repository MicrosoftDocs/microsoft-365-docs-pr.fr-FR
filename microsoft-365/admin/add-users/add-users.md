---
title: Ajouter des utilisateurs individuellement ou en bloc
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_O365_Setup
- Adm_O365_TOC
ms.custom:
- MSStore_Link
- okr_smb
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 1970f7d6-03b5-442f-b385-5880b9c256ec
description: Découvrez comment ajouter des utilisateurs à Microsoft 365, un simultanément ou plusieurs utilisateurs à la fois à partir d’un fichier CSV.
ms.openlocfilehash: 1b63f09bf34f5ca54be83eedfac9188251578a05
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44387260"
---
# <a name="add-users-individually-or-in-bulk"></a><span data-ttu-id="a072d-103">Ajouter des utilisateurs individuellement ou en bloc</span><span class="sxs-lookup"><span data-stu-id="a072d-103">Add users individually or in bulk</span></span>

<span data-ttu-id="a072d-104">Les membres de votre équipe doivent disposer d’un compte d’utilisateur pour pouvoir se connecter et accéder à [Microsoft 365 pour les entreprises](https://go.microsoft.com/fwlink/?LinkID=519395).</span><span class="sxs-lookup"><span data-stu-id="a072d-104">The people on your team each need a user account before they can sign in and access [Microsoft 365 for business](https://go.microsoft.com/fwlink/?LinkID=519395).</span></span> <span data-ttu-id="a072d-105">Le moyen le plus simple d’ajouter des comptes d’utilisateurs consiste à les ajouter un par un dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a072d-105">The easiest way to add user accounts is to add them one at a time in the Microsoft 365 admin center.</span></span> <span data-ttu-id="a072d-106">Après avoir effectué cette étape, vos utilisateurs disposeront de licences Microsoft 365, de connexion et de boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a072d-106">After you do this step, your users will have Microsoft 365 licenses, sign in credentials, and Microsoft 365 mailboxes.</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="a072d-107">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="a072d-107">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="a072d-108">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="a072d-108">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="a072d-109">Accédez à **utilisateurs** > **actifs**, puis sélectionnez **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="a072d-109">Go to **Users** > **Active users**, and select **Add a user**.</span></span>
   
3. <span data-ttu-id="a072d-110">Dans le volet de **Configuration des concepts de base** , renseignez les informations suivantes, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a072d-110">In the **Set up the basics** pane, fill in the following information, and then select **Next**.</span></span> 
  
- <span data-ttu-id="a072d-111">**Name (nom** ) Indiquez le prénom, le nom, le nom d’affichage et le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-111">**Name** Fill in first, last, display name, and username.</span></span> 
    
- <span data-ttu-id="a072d-112">**Domain (domaine** ) Par exemple, si le nom d’utilisateur de l’utilisateur est Jakob et que son domaine est contoso.com, il se connectera en tapant jakob@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a072d-112">**Domain** For example, if the user's username is Jakob, and his domain is contoso.com, he'll sign in to by typing jakob@contoso.com.</span></span> 
    
- <span data-ttu-id="a072d-113">**Paramètres de mot de passe** Choisissez l’option utiliser un mot de passe généré automatiquement ou créez votre propre mot de passe fort pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-113">**Password settings** Choose to the use auto-generated password or create your own strong password for the user.</span></span> 
    
    - <span data-ttu-id="a072d-114">Il devra modifier son mot de passe après 90 jours.</span><span class="sxs-lookup"><span data-stu-id="a072d-114">They'll need to change their password after 90 days.</span></span> <span data-ttu-id="a072d-115">Ou vous pouvez demander à **cet utilisateur de modifier son mot de passe lors de sa première connexion**.</span><span class="sxs-lookup"><span data-stu-id="a072d-115">Or you can choose to **Require this user to change their password when they first sign in**.</span></span>
    
    - <span data-ttu-id="a072d-116">Indiquez si vous souhaitez envoyer le mot de passe par courrier électronique lorsque l’utilisateur a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="a072d-116">Choose whether you want to  send the password in email when the user has been added.</span></span> 
    
4. <span data-ttu-id="a072d-117">Dans le volet **attribuer des licences de produits** , sélectionnez l’emplacement et la licence appropriée pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-117">In the **Assign product licenses** pane, select the location and the appropriate license for the user.</span></span> <span data-ttu-id="a072d-118">Si vous n'avez pas de licences disponibles, vous pouvez toujours ajouter un utilisateur et acheter des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a072d-118">If you don't have any licenses available, you can still add a user and buy additional licenses.</span></span> <span data-ttu-id="a072d-119">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a072d-119">Select **Next**.</span></span>

5. <span data-ttu-id="a072d-120">Dans la page **paramètres facultatifs** , développez **rôles** si vous voulez faire de cet utilisateur un administrateur, puis développez informations sur le **Profil** si vous souhaitez ajouter des informations supplémentaires sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-120">In the **Optional settings** page, expand **Roles** if you want to make this user an admin, and expand **Profile info** if you want to add additional information about the user.</span></span> 

6. <span data-ttu-id="a072d-121">Sélectionnez **suivant**, vérifiez les paramètres de votre nouvel utilisateur, effectuez les modifications de votre choix, puis sélectionnez **terminer l’ajout**.</span><span class="sxs-lookup"><span data-stu-id="a072d-121">Select **Next**, review your new user's settings, make any changes you like, and then select **Finish adding**.</span></span> 

::: moniker-end


::: moniker range="o365-germany"

1. <span data-ttu-id="a072d-122">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span><span class="sxs-lookup"><span data-stu-id="a072d-122">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span></span>

2. <span data-ttu-id="a072d-123">Accédez à **utilisateurs** > **actifs**, puis sélectionnez **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="a072d-123">Go to **Users** > **Active users**, and select **Add a user**.</span></span>
   
  
   <span data-ttu-id="a072d-124">Dans le volet **nouvel utilisateur** , renseignez les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="a072d-124">In the **New user** pane, fill in the following information.</span></span> <span data-ttu-id="a072d-125">Sélectionnez **Ajouter** lorsque vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="a072d-125">Select **Add** when you are done.</span></span> 
  
- <span data-ttu-id="a072d-126">**Nom** Indiquez le prénom, le nom, le nom d'affichage et le nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-126">**Name** Fill in first, last, display name, and user name.</span></span> 
    
- <span data-ttu-id="a072d-127">**Domain (domaine** ) Par exemple, si le nom d’utilisateur de l’utilisateur est Jakob et que son domaine est contoso.com, il se connectera en tapant jakob@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a072d-127">**Domain** For example, if the user's username is Jakob, and his domain is contoso.com, he'll sign in to by typing jakob@contoso.com.</span></span> 
    
- <span data-ttu-id="a072d-128">**Informations de contact** Développez pour renseigner un numéro de téléphone mobile, une adresse, etc.</span><span class="sxs-lookup"><span data-stu-id="a072d-128">**Contact information** Expand to fill in a mobile phone number, address, and so on.</span></span> 
    
- <span data-ttu-id="a072d-129">**Mot de passe** Utilisez le mot de passe généré automatiquement ou développez pour définir un mot de passe fort pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-129">**Password** Use the auto-generated password or expand to specify a strong password for the user.</span></span> 
    
    <span data-ttu-id="a072d-p105">Il devra modifier son mot de passe après 90 jours. Vous pouvez aussi choisir de **Demander à cet utilisateur de modifier son mot de passe lors de sa première connexion**.</span><span class="sxs-lookup"><span data-stu-id="a072d-p105">They'll need to change their password after 90 days. Or you can choose to **Make this user change their password when they first sign in**.</span></span>
    
- <span data-ttu-id="a072d-132">**Rôles** Développez si vous devez faire de cet utilisateur un administrateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-132">**Roles** Expand if you need to make this user an admin.</span></span> 
    
- <span data-ttu-id="a072d-p106">**Licences de produits** Développez cette section, puis sélectionnez la licence appropriée. Si vous n'avez pas de licences disponibles, vous pouvez toujours ajouter un utilisateur et acheter des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a072d-p106">**Product licenses** Expand this section and select the appropriate license. If you don't have any licenses available, you can still add a user and buy additional licenses.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a072d-135">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span><span class="sxs-lookup"><span data-stu-id="a072d-135">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

2. <span data-ttu-id="a072d-136">Accédez à **utilisateurs** > **actifs**, puis sélectionnez **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="a072d-136">Go to **Users** > **Active users**, and select **Add a user**.</span></span>
   
  
   <span data-ttu-id="a072d-137">Dans le volet **nouvel utilisateur** , renseignez les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="a072d-137">In the **New user** pane, fill in the following information.</span></span> <span data-ttu-id="a072d-138">Sélectionnez **Ajouter** lorsque vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="a072d-138">Select **Add** when you are done.</span></span> 
  
- <span data-ttu-id="a072d-139">**Nom** Indiquez le prénom, le nom, le nom d'affichage et le nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-139">**Name** Fill in first, last, display name, and user name.</span></span> 
    
- <span data-ttu-id="a072d-140">**Domain (domaine** ) Par exemple, si le nom d’utilisateur de l’utilisateur est Jakob et que son domaine est contoso.com, il se connectera en tapant jakob@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a072d-140">**Domain** For example, if the user's username is Jakob, and his domain is contoso.com, he'll sign in to by typing jakob@contoso.com.</span></span> 
    
- <span data-ttu-id="a072d-141">**Informations de contact** Développez pour renseigner un numéro de téléphone mobile, une adresse, etc.</span><span class="sxs-lookup"><span data-stu-id="a072d-141">**Contact information** Expand to fill in a mobile phone number, address, and so on.</span></span> 
    
- <span data-ttu-id="a072d-142">**Mot de passe** Utilisez le mot de passe généré automatiquement ou développez pour définir un mot de passe fort pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-142">**Password** Use the auto-generated password or expand to specify a strong password for the user.</span></span> 
    
    <span data-ttu-id="a072d-p108">Il devra modifier son mot de passe après 90 jours. Vous pouvez aussi choisir de **Demander à cet utilisateur de modifier son mot de passe lors de sa première connexion**.</span><span class="sxs-lookup"><span data-stu-id="a072d-p108">They'll need to change their password after 90 days. Or you can choose to **Make this user change their password when they first sign in**.</span></span>
    
- <span data-ttu-id="a072d-145">**Rôles** Développez si vous devez faire de cet utilisateur un administrateur.</span><span class="sxs-lookup"><span data-stu-id="a072d-145">**Roles** Expand if you need to make this user an admin.</span></span> 
    
- <span data-ttu-id="a072d-p109">**Licences de produits** Développez cette section, puis sélectionnez la licence appropriée. Si vous n'avez pas de licences disponibles, vous pouvez toujours ajouter un utilisateur et acheter des licences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a072d-p109">**Product licenses** Expand this section and select the appropriate license. If you don't have any licenses available, you can still add a user and buy additional licenses.</span></span> 

::: moniker-end 
  
<span data-ttu-id="a072d-148">Après l'ajout d'un utilisateur, vous recevrez un courrier de l'équipe Microsoft Online Services.</span><span class="sxs-lookup"><span data-stu-id="a072d-148">After you add a user, you'll get an email notification from the Microsoft Online Services Team.</span></span> <span data-ttu-id="a072d-149">Le courrier électronique contiendra le nom d’utilisateur et le mot de passe de la personne afin de pouvoir se connecter à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a072d-149">The email will contain the person's user ID and password so they can sign in to Microsoft 365.</span></span> <span data-ttu-id="a072d-150">Vous devez indiquer à votre nouvel utilisateur les informations de connexion de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a072d-150">You need to tell your new user about their Microsoft 365 sign in information.</span></span> <span data-ttu-id="a072d-151">Nous vous conseillons d'utiliser le processus normal pour communiquer les nouveaux mots de passe.</span><span class="sxs-lookup"><span data-stu-id="a072d-151">Use your normal process for communicating new passwords.</span></span>

> [!NOTE]
><span data-ttu-id="a072d-152">Si vous créez des utilisateurs en migrant des boîtes aux lettres, vous devrez activer les comptes d’utilisateur en affectant des licences.</span><span class="sxs-lookup"><span data-stu-id="a072d-152">If you create users by migrating mail boxes, you will need to activate user accounts by assigning licenses.</span></span> <span data-ttu-id="a072d-153">Si vous n’attribuez pas de licence à un utilisateur, sa boîte aux lettres est désactivée après une période de grâce de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a072d-153">If you don't assign a license to a user, their mailbox will be disabled after a grace period of 30 days.</span></span> <span data-ttu-id="a072d-154">Découvrez comment [attribuer des licences à des utilisateurs](https://docs.microsoft.com/microsoft-365/admin/add-users/add-users) à l’aide du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a072d-154">See how to [assign licenses to users](https://docs.microsoft.com/microsoft-365/admin/add-users/add-users) using the Microsoft 365 admin center.</span></span>

### <a name="video-add-and-manage-users-in-the-admin-center"></a><span data-ttu-id="a072d-155">Vidéo : ajouter et gérer des utilisateurs dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="a072d-155">Video: Add and manage users in the admin center</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FOfN?autoplay=false]
  
## <a name="next-steps"></a><span data-ttu-id="a072d-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a072d-156">Next steps</span></span>

<span data-ttu-id="a072d-157">Partagez le [guide de démarrage rapide destiné aux employés](https://support.office.com/article/b9700090-ce64-4046-ab92-ce8488a7bc0f.aspx) avec les nouveaux utilisateurs de manière à ce qu'ils configurent leur environnement, par exemple, [Office sur un PC ou Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx) et les [applications mobiles Office](https://support.office.com/article/7dabb6cb-0046-40b6-81fe-767e0b1f014f.aspx).</span><span class="sxs-lookup"><span data-stu-id="a072d-157">Share the [Employee quick start guide](https://support.office.com/article/b9700090-ce64-4046-ab92-ce8488a7bc0f.aspx) with your new users to set things up, like [Office on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx) and [Office mobile apps](https://support.office.com/article/7dabb6cb-0046-40b6-81fe-767e0b1f014f.aspx).</span></span>
  
## <a name="need-help"></a><span data-ttu-id="a072d-158">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="a072d-158">Need help?</span></span>

<span data-ttu-id="a072d-159">[Contactez le support technique Microsoft 365 pour les entreprises](../contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="a072d-159">[Contact Microsoft 365 for business support](../contact-support-for-business-products.md).</span></span>  

## <a name="have-hundreds-or-thousands-of-users-to-add"></a><span data-ttu-id="a072d-160">Vous avez des centaines de milliers d'utilisateurs à ajouter ?</span><span class="sxs-lookup"><span data-stu-id="a072d-160">Have hundreds or thousands of users to add?</span></span>


<span data-ttu-id="a072d-161">Pour ajouter plusieurs utilisateurs simultanément, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a072d-161">To add multiple users at the same time, follow these steps:</span></span>
  
- <span data-ttu-id="a072d-162">**Utiliser une feuille de calcul pour ajouter des utilisateurs en bloc.**</span><span class="sxs-lookup"><span data-stu-id="a072d-162">**Use a spreadsheet to add people in bulk.**</span></span> <span data-ttu-id="a072d-163">Voir [ajouter plusieurs utilisateurs en même temps](https://docs.microsoft.com/office365/enterprise/add-several-users-at-the-same-time).</span><span class="sxs-lookup"><span data-stu-id="a072d-163">See [Add several users at the same time](https://docs.microsoft.com/office365/enterprise/add-several-users-at-the-same-time).</span></span>
    
- <span data-ttu-id="a072d-164">**Automatiser l'ajouter de comptes et l'affectation de licences.**</span><span class="sxs-lookup"><span data-stu-id="a072d-164">**Automate adding accounts and assigning licenses.**</span></span> <span data-ttu-id="a072d-165">Voir [Create User Accounts with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/create-user-accounts-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="a072d-165">See [Create user accounts with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/create-user-accounts-with-office-365-powershell).</span></span> <span data-ttu-id="a072d-166">Choisissez cette méthode si vous êtes déjà familiarisé avec l'utilisation des applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a072d-166">Choose this method if you're already familiar with using Windows PowerShell cmdlets.</span></span>
    
- <span data-ttu-id="a072d-167">**À l’aide d’ActiveDirectory ?**</span><span class="sxs-lookup"><span data-stu-id="a072d-167">**Using ActiveDirectory?**</span></span> <span data-ttu-id="a072d-168">[Configurez la synchronisation d’annuaires pour Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="a072d-168">[Set up directory synchronization for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization).</span></span> <span data-ttu-id="a072d-169">Utilisez l'outil Azure AD Connect pour répliquer les comptes d'utilisateur Active Directory (et autres objets Active Directory) dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="a072d-169">Use the Azure AD Connect tool to replicate Active Directory user accounts (and other Active Directory objects) in Office 365.</span></span> <span data-ttu-id="a072d-170">La synchronisation ajoute uniquement les comptes d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a072d-170">The sync only adds the user accounts.</span></span> <span data-ttu-id="a072d-171">Vous devrez attribuer des licences aux utilisateurs synchronisés pour qu'ils puissent utiliser le courrier et les autres applications Office.</span><span class="sxs-lookup"><span data-stu-id="a072d-171">You will need to assign licenses to the synced users before they can use email and other Office apps.</span></span>
    
- <span data-ttu-id="a072d-172">**Migration à partir d’Exchange ?**</span><span class="sxs-lookup"><span data-stu-id="a072d-172">**Migrating from Exchange?**</span></span> <span data-ttu-id="a072d-173">[Méthodes de migration de plusieurs comptes de messagerie vers Office 365](https://docs.microsoft.com/Exchange/mailbox-migration/mailbox-migration).</span><span class="sxs-lookup"><span data-stu-id="a072d-173">[Ways to migrate multiple email accounts to Office 365](https://docs.microsoft.com/Exchange/mailbox-migration/mailbox-migration).</span></span> <span data-ttu-id="a072d-174">Lorsque vous migrez plusieurs boîtes aux lettres vers Microsoft 365 en utilisant soit un basculement, intermédiaire, soit une méthode Exchange hybride, vous ajoutez automatiquement des utilisateurs dans le cadre de la migration.</span><span class="sxs-lookup"><span data-stu-id="a072d-174">When you migrate multiple mailboxes to Microsoft 365 by using either cutover, staged, or a hybrid Exchange method, you will add users automatically as part of the migration.</span></span> <span data-ttu-id="a072d-175">La migration ajoute uniquement les comptes d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a072d-175">The migration only adds the user accounts.</span></span> <span data-ttu-id="a072d-176">Vous devrez attribuer des licences aux utilisateurs pour qu'ils puissent utiliser le courrier et les autres applications Office.</span><span class="sxs-lookup"><span data-stu-id="a072d-176">You will need assign licenses to the users before they can use email and other Office apps.</span></span>

## <a name="related-articles"></a><span data-ttu-id="a072d-177">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a072d-177">Related articles</span></span>

[<span data-ttu-id="a072d-178">Ajouter un nouvel employé à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a072d-178">Add a new employee to Microsoft 365</span></span>](add-new-employee.md)

[<span data-ttu-id="a072d-179">Supprimer un utilisateur de votre organisation</span><span class="sxs-lookup"><span data-stu-id="a072d-179">Delete a user from your organization</span></span>](delete-a-user.md)

[<span data-ttu-id="a072d-180">Restaurer un utilisateur dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a072d-180">Restore a user in Microsoft 365</span></span>](restore-user.md)

[<span data-ttu-id="a072d-181">Ajouter plusieurs utilisateurs en même temps à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a072d-181">Add several users at the same time to Microsoft 365</span></span>](https://docs.microsoft.com/office365/enterprise/add-several-users-at-the-same-time)

