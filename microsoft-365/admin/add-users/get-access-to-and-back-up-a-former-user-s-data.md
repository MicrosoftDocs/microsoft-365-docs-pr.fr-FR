---
title: Accéder aux données d'un ancien utilisateur et les sauvegarder
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
- M365-subscription-management
- Adm_O365
- Adm_TOC
- SPO_Content
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: a6f7f9ad-e3f5-43de-ade5-e5a0d7531604
description: Découvrez comment conserver les fichiers et les e-mails d’un employé lorsque la personne quitte votre organisation.
ms.openlocfilehash: 2bf32aa9e7a3dcc76ae2114240bff07d697ce29d
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44387200"
---
# <a name="get-access-to-and-back-up-a-former-users-data"></a><span data-ttu-id="db149-103">Accéder aux données d'un ancien utilisateur et les sauvegarder</span><span class="sxs-lookup"><span data-stu-id="db149-103">Get access to and back up a former user's data</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="db149-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="db149-104">The admin center is changing.</span></span> <span data-ttu-id="db149-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="db149-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end


<span data-ttu-id="db149-106">Quand un employé quitte votre organisation, vous voudrez probablement accéder à ses données (documents et courriers électroniques) et les consulter, les sauvegarder ou les transmettre à un nouvel employé.</span><span class="sxs-lookup"><span data-stu-id="db149-106">When an employee leaves your organization, you probably want to access their data (documents and emails) and either review it, back it up, or give it to a new employee.</span></span>
  
    
## <a name="access-a-former-users-onedrive-documents"></a><span data-ttu-id="db149-107">Accéder aux documents OneDrive d’un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="db149-107">Access a former user's OneDrive documents</span></span>

<span data-ttu-id="db149-108">Si vous supprimez la licence d’un utilisateur, mais que vous ne supprimez pas le compte, vous pouvez vous accorder l’accès au contenu dans le OneDrive de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db149-108">If you remove a user's license but don't delete the account, you can give yourself access to the content in the user's OneDrive.</span></span> <span data-ttu-id="db149-109">Si vous supprimez le compte de l’utilisateur, vous disposez de 30 jours par défaut pour accéder aux données OneDrive de l’ancien utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db149-109">If you delete the user's account, you have 30 days by default to access the former user's OneDrive data.</span></span> <span data-ttu-id="db149-110">[Découvrez comment configurer la rétention OneDrive pour les utilisateurs supprimés](/onedrive/set-retention).</span><span class="sxs-lookup"><span data-stu-id="db149-110">[Learn how to set the OneDrive retention for deleted users](/onedrive/set-retention).</span></span> <span data-ttu-id="db149-111">Si vous ne [restaurez pas un compte d’utilisateur](/office365/admin/add-users/restore-user) pendant ce temps, son contenu OneDrive est supprimé.</span><span class="sxs-lookup"><span data-stu-id="db149-111">If you don't [restore a user account](/office365/admin/add-users/restore-user) within this time, their OneDrive content is deleted.</span></span> 

<span data-ttu-id="db149-112">Pour conserver les fichiers OneDrive d’un ancien utilisateur, commencez par vous accorder l’accès à son OneDrive, puis déplacez les fichiers que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="db149-112">To preserve a former user's OneDrive files, first give yourself access to their OneDrive, and then move the files you want to keep.</span></span> 

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="db149-113">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="db149-113">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="db149-114">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="db149-114">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="db149-115">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db149-115">Select a user.</span></span>

3. <span data-ttu-id="db149-116">Dans le volet droit, sélectionnez **OneDrive**.</span><span class="sxs-lookup"><span data-stu-id="db149-116">In the right pane, select **OneDrive**.</span></span> <span data-ttu-id="db149-117">Sous **accéder à des fichiers**, sélectionnez **créer un lien vers des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="db149-117">Under **Get access to files**, select **Create link to files**.</span></span>

4. <span data-ttu-id="db149-118">Sélectionnez le lien pour ouvrir l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="db149-118">Select the link to open the file location.</span></span> <span data-ttu-id="db149-119">Téléchargez les fichiers sur votre ordinateur ou sélectionnez **déplacer vers** ou **copier** vers pour les déplacer ou les copier vers votre propre OneDrive ou une bibliothèque partagée.</span><span class="sxs-lookup"><span data-stu-id="db149-119">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span> 

> [!NOTE]
> <span data-ttu-id="db149-120">Vous pouvez déplacer ou copier jusqu’à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="db149-120">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="db149-121">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="db149-121">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="db149-122">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="db149-122">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="db149-123">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db149-123">Select a user.</span></span>

3. <span data-ttu-id="db149-124">Dans le volet droit, développez **paramètres OneDrive**, puis en regard de **accès**, sélectionnez **fichiers Access**.</span><span class="sxs-lookup"><span data-stu-id="db149-124">In the right pane, expand **OneDrive Settings**, and then next to **Access**, select **Access files**.</span></span>

4. <span data-ttu-id="db149-125">Sélectionnez le lien pour ouvrir l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="db149-125">Select the link to open the file location.</span></span> <span data-ttu-id="db149-126">Téléchargez les fichiers sur votre ordinateur ou sélectionnez **déplacer vers** ou **copier** vers pour les déplacer ou les copier vers votre propre OneDrive ou une bibliothèque partagée.</span><span class="sxs-lookup"><span data-stu-id="db149-126">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span> 

> [!NOTE]
> <span data-ttu-id="db149-127">Vous pouvez déplacer ou copier jusqu’à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="db149-127">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="db149-128">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="db149-128">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="db149-129">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="db149-129">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="db149-130">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db149-130">Select a user.</span></span>

3. <span data-ttu-id="db149-131">Dans le volet droit, développez **paramètres OneDrive**, puis en regard de **accès**, sélectionnez **fichiers Access**.</span><span class="sxs-lookup"><span data-stu-id="db149-131">In the right pane, expand **OneDrive Settings**, and then next to **Access**, select **Access files**.</span></span>

4. <span data-ttu-id="db149-132">Sélectionnez le lien pour ouvrir l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="db149-132">Select the link to open the file location.</span></span> <span data-ttu-id="db149-133">Téléchargez les fichiers sur votre ordinateur ou sélectionnez **déplacer vers** ou **copier** vers pour les déplacer ou les copier vers votre propre OneDrive ou une bibliothèque partagée.</span><span class="sxs-lookup"><span data-stu-id="db149-133">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span>  

> [!NOTE]
> <span data-ttu-id="db149-134">Vous pouvez déplacer ou copier jusqu’à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="db149-134">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="db149-135">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="db149-135">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

::: moniker-end
    


## <a name="revoke-admin-access-to-a-users-onedrive"></a><span data-ttu-id="db149-136">Révoquer l’accès administrateur au OneDrive d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="db149-136">Revoke admin access to a user's OneDrive</span></span>

<span data-ttu-id="db149-137">En tant qu’administrateur général, vous pouvez vous accorder l’accès au contenu dans OneDrive d’un utilisateur, mais vous pouvez supprimer votre accès lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="db149-137">As global admin, you can give yourself access to the content in a user's OneDrive, but you may want to remove your access when you no longer need it.</span></span> 

::: moniker range="o365-worldwide"

1. <span data-ttu-id="db149-138">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration</a> en tant qu’administrateur général ou administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db149-138">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a> as a global admin or SharePoint admin.</span></span> 

    <span data-ttu-id="db149-139">Si vous recevez un message indiquant que vous n’êtes pas autorisé à accéder au centre d’administration, vous ne disposez pas des autorisations d’administrateur dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="db149-139">If you get a message that you don't have permission to access the admin center, then you don't have administrator permissions in your organization.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="db149-140">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a> en tant qu’administrateur général ou administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db149-140">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a> as a global admin or SharePoint admin.</span></span>

    <span data-ttu-id="db149-141">Si vous recevez un message indiquant que vous n’êtes pas autorisé à accéder au centre d’administration, vous ne disposez pas des autorisations d’administrateur dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="db149-141">If you get a message that you don't have permission to access the admin center, then you don't have administrator permissions in your organization.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="db149-142">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a> en tant qu’administrateur général ou administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db149-142">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a> as a global admin or SharePoint admin.</span></span>

    <span data-ttu-id="db149-143">Si vous recevez un message indiquant que vous n’êtes pas autorisé à accéder au centre d’administration, vous ne disposez pas des autorisations d’administrateur dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="db149-143">If you get a message that you don't have permission to access the admin center, then you don't have administrator permissions in your organization.</span></span>

::: moniker-end

2. <span data-ttu-id="db149-144">Dans le volet gauche, sélectionnez **centres d’administration** \> **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="db149-144">In the left pane, select **Admin centers** \> **SharePoint**.</span></span> <span data-ttu-id="db149-145">(Vous devrez peut-être sélectionner **Afficher tout** pour afficher la liste des centres d’administration.)</span><span class="sxs-lookup"><span data-stu-id="db149-145">(You might need to select **Show all** to see the list of admin centers.)</span></span>

3. <span data-ttu-id="db149-146">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db149-146">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

4. <span data-ttu-id="db149-147">Dans le volet gauche, sélectionnez **plus de fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="db149-147">In the left pane, select **More features**.</span></span>

5. <span data-ttu-id="db149-148">Sous **profils utilisateur**, sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="db149-148">Under **User profiles**, select **Open**.</span></span>

6. <span data-ttu-id="db149-149">Sous **personnes**, sélectionnez **gérer les profils utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="db149-149">Under **People**, select **Manage User Profiles**.</span></span>

7. <span data-ttu-id="db149-150">Entrez le nom de l’utilisateur et sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="db149-150">Enter the user's name and select **Find**.</span></span>

8. <span data-ttu-id="db149-151">Cliquez avec le bouton droit sur l’utilisateur, puis choisissez **gérer les propriétaires de collection de sites**.</span><span class="sxs-lookup"><span data-stu-id="db149-151">Right-click the user, and then choose **Manage site collection owners**.</span></span>

9. <span data-ttu-id="db149-152">Supprimez la personne qui n’a plus besoin d’accéder aux données de l’utilisateur, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="db149-152">Remove the person who no longer needs access to the user's data, and then select **OK**.</span></span>

    
## <a name="access-the-outlook-data-of-a-former-user"></a><span data-ttu-id="db149-153">Accéder aux données Outlook d’un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="db149-153">Access the Outlook data of a former user</span></span>

<span data-ttu-id="db149-154">Pour enregistrer les messages électroniques, le calendrier, les tâches et les contacts de l’ancien employé, exportez les informations vers un fichier de données Outlook (. pst).</span><span class="sxs-lookup"><span data-stu-id="db149-154">To save the email messages, calendar, tasks, and contacts of the former employee, export the information to an Outlook Data File (.pst).</span></span>
  
1. <span data-ttu-id="db149-155">[Ajoutez le message électronique de l’ancien employé](https://support.office.com/article/6e27792a-9267-4aa4-8bb6-c84ef146101b.aspx) à votre Outlook (si vous [réinitialisez le mot de passe de l’utilisateur](reset-passwords.md), vous pouvez le définir sur une valeur qui ne vous indique que).</span><span class="sxs-lookup"><span data-stu-id="db149-155">[Add the former employee's email](https://support.office.com/article/6e27792a-9267-4aa4-8bb6-c84ef146101b.aspx) to your Outlook (If you [reset the user's password](reset-passwords.md), you can set it to something only you know.)</span></span>
    
2. <span data-ttu-id="db149-156">Dans Outlook, sélectionnez **fichier**.</span><span class="sxs-lookup"><span data-stu-id="db149-156">In Outlook, select **File**.</span></span>
    
    ![Voici à quoi ressemble le ruban dans Outlook 2016.](../../media/d7f66ed3-9861-4521-b410-e86a58ab15a7.png)
  
3. <span data-ttu-id="db149-158">Sélectionnez \*\*ouvrir &amp; \*\* l' \> **importation/exportation**de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="db149-158">Select **Open &amp; Export** \> **Import/Export**.</span></span>
    
    ![Commande d’importation/exportation en mode Backstage](../../media/6013919e-d8ce-4902-b7b4-78ff4260a2f8.jpg)
  
4. <span data-ttu-id="db149-160">Sélectionnez **Exporter vers un fichier**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db149-160">Select **Export to a file**, and then select **Next**.</span></span>
    
    ![Option Exporter vers un fichier dans l’Assistant d’importation et d’exportation](../../media/458466a0-366b-4fbf-a2db-1919412c6527.jpg)
  
5. <span data-ttu-id="db149-162">Sélectionnez **fichier de données Outlook (. pst)**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db149-162">Select **Outlook Data File (.pst)**, and then select **Next**.</span></span>
    
6. <span data-ttu-id="db149-163">Sélectionnez le compte que vous souhaitez exporter en sélectionnant le nom ou l’adresse de messagerie, par exemple, Weiler ou anne@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="db149-163">Select the account you want to export by selecting the name or email address, such as Mailbox - Anne Weiler or anne@contoso.com.</span></span> <span data-ttu-id="db149-164">Si vous souhaitez exporter tout le contenu de votre compte, y compris le courrier, le calendrier, les contacts, les tâches et les notes, vérifiez que la case à cocher **inclure les sous-dossiers** est activée.</span><span class="sxs-lookup"><span data-stu-id="db149-164">If you want to export everything in your account, including mail, calendar, contacts, tasks, and notes, make sure the **Include subfolders** check box is selected.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="db149-165">Vous pouvez exporter un compte à la fois.</span><span class="sxs-lookup"><span data-stu-id="db149-165">You can export one account at a time.</span></span> <span data-ttu-id="db149-166">Si vous souhaitez exporter plusieurs comptes, après l’exportation d’un compte, répétez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="db149-166">If you want to export multiple accounts, after one account is exported, repeat these steps.</span></span> 
  
    ![Boîte de dialogue Exporter le fichier de données Outlook avec le dossier supérieur sélectionné et inclure les sous-dossiers activés](../../media/ce36616f-d76d-4ce2-b517-8ac4874e0971.jpg)
  
7. <span data-ttu-id="db149-168">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="db149-168">Select **Next**.</span></span>
    
8. <span data-ttu-id="db149-169">Sélectionnez **Parcourir** pour sélectionner l’emplacement d’enregistrement du fichier de données Outlook (. pst).</span><span class="sxs-lookup"><span data-stu-id="db149-169">Select **Browse** to select where to save the Outlook Data File (.pst).</span></span> <span data-ttu-id="db149-170">Tapez un *nom de fichier*, puis cliquez sur **OK** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="db149-170">Type a  *file name*, and then select **OK** to continue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="db149-171">Si vous avez utilisé l’exportation avant, l’emplacement du dossier et le nom de fichier précédents apparaissent.</span><span class="sxs-lookup"><span data-stu-id="db149-171">If you've used export before, the previous folder location and file name appear.</span></span> <span data-ttu-id="db149-172">Tapez un *autre nom de fichier* avant de sélectionner **OK**.</span><span class="sxs-lookup"><span data-stu-id="db149-172">Type a  *different file name*  before selecting **OK**.</span></span> 
  
9. <span data-ttu-id="db149-173">Si vous effectuez l’exportation vers un fichier de données Outlook (. pst) existant, sous **options**, spécifiez les actions à effectuer lors de l’exportation d’éléments qui existent déjà dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="db149-173">If you are exporting to an existing Outlook Data File (.pst), under **Options**, specify what to do when exporting items that already exist in the file.</span></span>
    
10. <span data-ttu-id="db149-174">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="db149-174">Select **Finish**.</span></span>
    
<span data-ttu-id="db149-175">Outlook commence l’exportation immédiatement sauf si un nouveau fichier de données Outlook (. pst) est créé ou si un fichier protégé par mot de passe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="db149-175">Outlook begins the export immediately unless a new Outlook Data File (.pst) is created or a password-protected file is used.</span></span>
  
   - <span data-ttu-id="db149-176">Si vous créez un fichier de données Outlook (. pst), un mot de passe facultatif peut aider à protéger le fichier.</span><span class="sxs-lookup"><span data-stu-id="db149-176">If you're creating an Outlook Data File (.pst), an optional password can help protect the file.</span></span> <span data-ttu-id="db149-177">Lorsque la boîte de dialogue **créer un fichier de données Outlook** s’affiche, tapez le *mot de passe* dans les zones **mot** de passe et **confirmer le mot de passe** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="db149-177">When the **Create Outlook Data File** dialog box appears, type the  *password*  in the **Password** and **Verify Password** boxes, and then select **OK**.</span></span> <span data-ttu-id="db149-178">Dans la boîte de dialogue **mot de passe du fichier de données Outlook** , tapez le *mot de passe*, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="db149-178">In the **Outlook Data File Password** dialog box, type the  *password*, and then select **OK**.</span></span>
    
  - <span data-ttu-id="db149-179">Si vous effectuez une exportation vers un fichier de données Outlook (. pst) qui est protégé par mot de passe, dans la boîte de dialogue **mot de passe du fichier de données Outlook** , tapez le *mot de passe*, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="db149-179">If you're exporting to an existing Outlook Data File (.pst) that is password protected, in the **Outlook Data File Password** dialog box, type the  *password*, and then select **OK**.</span></span>
    
<span data-ttu-id="db149-180">Découvrez comment [exporter ou sauvegarder des courriers électroniques, des contacts et des calendriers dans un fichier. pst Outlook](https://support.office.com/article/14252b52-3075-4e9b-be4e-ff9ef1068f91.aspx) dans Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="db149-180">See how to [Export or backup email, contacts, and calendar to an Outlook .pst file](https://support.office.com/article/14252b52-3075-4e9b-be4e-ff9ef1068f91.aspx) in Outlook 2010.</span></span> 
  
  
  > [!NOTE]
  > <span data-ttu-id="db149-181">Par défaut, votre courrier électronique est disponible hors connexion pendant une période de 12 mois.</span><span class="sxs-lookup"><span data-stu-id="db149-181">By default, your email is available offline for a period of 12 months.</span></span> <span data-ttu-id="db149-182">Si nécessaire, reportez-vous à la rubrique Comment [augmenter les données disponibles hors connexion](Https://docs.microsoft.com/outlook/troubleshoot/mailboxes/only-subset-items-synchronized).</span><span class="sxs-lookup"><span data-stu-id="db149-182">If required, see how to [increase the data available offline](Https://docs.microsoft.com/outlook/troubleshoot/mailboxes/only-subset-items-synchronized).</span></span>
 
## <a name="give-another-user-access-to-a-former-users-email"></a><span data-ttu-id="db149-183">Accorder à un autre utilisateur l’accès à l’adresse de messagerie d’un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="db149-183">Give another user access to a former user's email</span></span> 

<span data-ttu-id="db149-184">Pour accorder l’accès aux messages électroniques, au calendrier, aux tâches et aux contacts de l’ancien employé à un autre employé, importez les informations dans la boîte de réception Outlook d’un autre employé.</span><span class="sxs-lookup"><span data-stu-id="db149-184">To give access to the email messages, calendar, tasks, and contacts of the former employee to another employee, import the information to another employee's Outlook inbox.</span></span>

> [!NOTE]
> <span data-ttu-id="db149-185">Vous pouvez également [convertir la boîte aux lettres de l’ancien utilisateur en boîte aux lettres partagée](https://docs.microsoft.com/office365/admin/email/convert-user-mailbox-to-shared-mailbox) ou [transférer le courrier électronique d’un ancien employé à un autre employé](https://docs.microsoft.com/office365/admin/add-users/remove-former-employee#forward-a-former-employees-email-to-another-employee-or-convert-to-a-shared-mailbox).</span><span class="sxs-lookup"><span data-stu-id="db149-185">You can also [convert the former user's mailbox to a shared mailbox](https://docs.microsoft.com/office365/admin/email/convert-user-mailbox-to-shared-mailbox) or [forward a former employee's email to another employee](https://docs.microsoft.com/office365/admin/add-users/remove-former-employee#forward-a-former-employees-email-to-another-employee-or-convert-to-a-shared-mailbox).</span></span>

  
1. <span data-ttu-id="db149-186">Dans Outlook, accédez à **fichier** : \> **ouvrir &amp; Exporter** l' \> **importation/exportation**.</span><span class="sxs-lookup"><span data-stu-id="db149-186">In Outlook, go to **File** \> **Open &amp; Export** \> **Import/Export**.</span></span>
    
    <span data-ttu-id="db149-187">Cette opération démarre l’Assistant d’importation et d’exportation.</span><span class="sxs-lookup"><span data-stu-id="db149-187">This starts the Import and Export Wizard.</span></span>
    
2. <span data-ttu-id="db149-188">Sélectionnez **Importer à partir d’un autre programme ou fichier**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db149-188">Select **Import from another program or file**, and then select **Next**.</span></span>
    
    ![Assistant d’importation et d’exportation](../../media/15cdd674-cd7b-492c-8e93-992cfa890f26.jpg)
  
3. <span data-ttu-id="db149-190">Sélectionnez **fichier de données Outlook (. pst)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db149-190">Select **Outlook Data File (.pst)**, and select **Next**.</span></span>
    
4. <span data-ttu-id="db149-191">Accédez au fichier. pst que vous souhaitez importer.</span><span class="sxs-lookup"><span data-stu-id="db149-191">Browse to the .pst file you want to import.</span></span>
    
5. <span data-ttu-id="db149-192">Sous **options**, choisissez le mode de traitement des doublons.</span><span class="sxs-lookup"><span data-stu-id="db149-192">Under **Options**, choose how you want to deal with duplicates</span></span>
    
6. <span data-ttu-id="db149-193">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="db149-193">Select **Next**.</span></span>
    
7. <span data-ttu-id="db149-194">Si un mot de passe a été attribué au fichier de données Outlook (. pst), entrez le mot de passe, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="db149-194">If a password was assigned to the Outlook Data File (.pst), enter the password, and then select **OK**.</span></span>
    
8. <span data-ttu-id="db149-195">Définir les options d’importation des éléments.</span><span class="sxs-lookup"><span data-stu-id="db149-195">Set the options for importing items.</span></span> <span data-ttu-id="db149-196">Il n’est généralement pas nécessaire de modifier les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="db149-196">The default settings usually don't need to be changed.</span></span>
    
9. <span data-ttu-id="db149-197">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="db149-197">Select **Finish**.</span></span>

> [!NOTE]
> <span data-ttu-id="db149-198">Les étapes restent les mêmes pour accéder aux données de messagerie et à OneDrive d’un utilisateur existant.</span><span class="sxs-lookup"><span data-stu-id="db149-198">The steps remain the same for accessing an existing user's OneDrive and email data.</span></span>
    
> [!TIP]
> <span data-ttu-id="db149-199">Si vous souhaitez importer ou restaurer uniquement quelques éléments à partir d’un fichier de données Outlook (. pst), vous pouvez ouvrir le fichier de données Outlook.</span><span class="sxs-lookup"><span data-stu-id="db149-199">If you want to import or restore only a few items from an Outlook Data File (.pst), you can open the Outlook Data File.</span></span> <span data-ttu-id="db149-200">Ensuite, dans le volet de navigation, faites glisser les éléments des dossiers du fichier de données Outlook vers vos dossiers Outlook existants.</span><span class="sxs-lookup"><span data-stu-id="db149-200">Then, in the navigation pane, drag the items from Outlook Data File folders to your existing Outlook folders.</span></span> 
  
  
## <a name="related-articles"></a><span data-ttu-id="db149-201">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="db149-201">Related articles</span></span>
[<span data-ttu-id="db149-202">Supprimer un ancien employé d'Office 365</span><span class="sxs-lookup"><span data-stu-id="db149-202">Remove a former employee from Office 365</span></span>](remove-former-employee.md)

[<span data-ttu-id="db149-203">Ajouter et supprimer des administrateurs sur un compte OneDrive</span><span class="sxs-lookup"><span data-stu-id="db149-203">Add and remove admins on a OneDrive account</span></span>](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)

[<span data-ttu-id="db149-204">Restaurer un OneDrive supprimé</span><span class="sxs-lookup"><span data-stu-id="db149-204">Restore a deleted OneDrive</span></span>](/onedrive/restore-deleted-onedrive)
  
[<span data-ttu-id="db149-205">Rétention et suppression de OneDrive</span><span class="sxs-lookup"><span data-stu-id="db149-205">OneDrive retention and deletion</span></span>](/onedrive/retention-and-deletion)
  
