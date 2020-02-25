---
title: Accéder aux données d'un ancien utilisateur et les sauvegarder.
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: a6f7f9ad-e3f5-43de-ade5-e5a0d7531604
description: Découvrez comment conserver les fichiers et les e-mails d’un employé lorsque la personne quitte votre organisation.
ms.openlocfilehash: 92e863e3b849f6a89e6d67d805fdb5024879999f
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239385"
---
# <a name="get-access-to-and-back-up-a-former-users-data"></a><span data-ttu-id="82d94-103">Accéder aux données d'un ancien utilisateur et les sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="82d94-103">Get access to and back up a former user's data</span></span>


<span data-ttu-id="82d94-104">Quand un employé quitte votre organisation, vous voudrez probablement accéder à ses données (documents et courriers électroniques) et les consulter, les sauvegarder ou les transmettre à un nouvel employé.</span><span class="sxs-lookup"><span data-stu-id="82d94-104">When an employee leaves your organization, you probably want to access their data (documents and emails) and either review it, back it up, or give it to a new employee.</span></span>
  
    
## <a name="access-a-former-users-onedrive-documents"></a><span data-ttu-id="82d94-105">Accéder aux documents OneDrive d’un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="82d94-105">Access a former user's OneDrive documents</span></span>

<span data-ttu-id="82d94-106">Si vous supprimez la licence d’un utilisateur, mais que vous ne supprimez pas le compte, vous pouvez vous accorder l’accès au contenu dans le OneDrive de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82d94-106">If you remove a user's license but don't delete the account, you can give yourself access to the content in the user's OneDrive.</span></span> <span data-ttu-id="82d94-107">Si vous supprimez le compte de l’utilisateur, vous disposez de 30 jours par défaut pour accéder aux données OneDrive de l’ancien utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82d94-107">If you delete the user's account, you have 30 days by default to access the former user’s OneDrive data.</span></span> <span data-ttu-id="82d94-108">[Découvrez comment configurer la rétention OneDrive pour les utilisateurs supprimés](/onedrive/set-retention).</span><span class="sxs-lookup"><span data-stu-id="82d94-108">[Learn how to set the OneDrive retention for deleted users](/onedrive/set-retention).</span></span> <span data-ttu-id="82d94-109">Si vous ne [restaurez pas un compte d’utilisateur](/office365/admin/add-users/restore-user) pendant ce temps, son contenu OneDrive est supprimé.</span><span class="sxs-lookup"><span data-stu-id="82d94-109">If you don't [restore a user account](/office365/admin/add-users/restore-user) within this time, their OneDrive content is deleted.</span></span> 

<span data-ttu-id="82d94-110">Pour conserver les fichiers OneDrive d’un ancien utilisateur, commencez par vous accorder l’accès à son OneDrive, puis déplacez les fichiers que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="82d94-110">To preserve a former user's OneDrive files, first give yourself access to their OneDrive, and then move the files you want to keep.</span></span> 

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="82d94-111">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="82d94-111">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="82d94-112">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="82d94-112">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="82d94-113">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82d94-113">Select a user.</span></span>

3. <span data-ttu-id="82d94-114">Dans le volet droit, sélectionnez **OneDrive**.</span><span class="sxs-lookup"><span data-stu-id="82d94-114">In the right pane, select **OneDrive**.</span></span> <span data-ttu-id="82d94-115">Sous **accéder à des fichiers**, sélectionnez **créer un lien vers des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="82d94-115">Under **Get access to files**, select **Create link to files**.</span></span>

4. <span data-ttu-id="82d94-116">Sélectionnez le lien pour ouvrir l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="82d94-116">Select the link to open the file location.</span></span> <span data-ttu-id="82d94-117">Téléchargez les fichiers sur votre ordinateur ou sélectionnez **déplacer vers** ou **copier** vers pour les déplacer ou les copier vers votre propre OneDrive ou une bibliothèque partagée.</span><span class="sxs-lookup"><span data-stu-id="82d94-117">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span> 

> [!NOTE]
> <span data-ttu-id="82d94-118">Vous pouvez déplacer ou copier jusqu’à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="82d94-118">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="82d94-119">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="82d94-119">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="82d94-120">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="82d94-120">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="82d94-121">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82d94-121">Select a user.</span></span>

3. <span data-ttu-id="82d94-122">Dans le volet droit, développez **paramètres OneDrive**, puis en regard de **accès**, sélectionnez **fichiers Access**.</span><span class="sxs-lookup"><span data-stu-id="82d94-122">In the right pane, expand **OneDrive Settings**, and then next to **Access**, select **Access files**.</span></span>

4. <span data-ttu-id="82d94-123">Sélectionnez le lien pour ouvrir l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="82d94-123">Select the link to open the file location.</span></span> <span data-ttu-id="82d94-124">Téléchargez les fichiers sur votre ordinateur ou sélectionnez **déplacer vers** ou **copier** vers pour les déplacer ou les copier vers votre propre OneDrive ou une bibliothèque partagée.</span><span class="sxs-lookup"><span data-stu-id="82d94-124">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span> 

> [!NOTE]
> <span data-ttu-id="82d94-125">Vous pouvez déplacer ou copier jusqu’à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="82d94-125">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="82d94-126">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="82d94-126">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="82d94-127">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="82d94-127">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="82d94-128">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82d94-128">Select a user.</span></span>

3. <span data-ttu-id="82d94-129">Dans le volet droit, développez **paramètres OneDrive**, puis en regard de **accès**, sélectionnez **fichiers Access**.</span><span class="sxs-lookup"><span data-stu-id="82d94-129">In the right pane, expand **OneDrive Settings**, and then next to **Access**, select **Access files**.</span></span>

4. <span data-ttu-id="82d94-130">Sélectionnez le lien pour ouvrir l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="82d94-130">Select the link to open the file location.</span></span> <span data-ttu-id="82d94-131">Téléchargez les fichiers sur votre ordinateur ou sélectionnez **déplacer vers** ou **copier** vers pour les déplacer ou les copier vers votre propre OneDrive ou une bibliothèque partagée.</span><span class="sxs-lookup"><span data-stu-id="82d94-131">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span>  

> [!NOTE]
> <span data-ttu-id="82d94-132">Vous pouvez déplacer ou copier jusqu’à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="82d94-132">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="82d94-133">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="82d94-133">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

::: moniker-end
    


## <a name="revoke-admin-access-to-a-users-onedrive"></a><span data-ttu-id="82d94-134">Révoquer l’accès administrateur au OneDrive d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="82d94-134">Revoke admin access to a user’s OneDrive</span></span>

<span data-ttu-id="82d94-135">En tant qu’administrateur général, vous pouvez vous accorder l’accès au contenu dans OneDrive d’un utilisateur, mais vous pouvez supprimer votre accès lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="82d94-135">As global admin, you can give yourself access to the content in a user’s OneDrive, but you may want to remove your access when you no longer need it.</span></span> 

::: moniker range="o365-worldwide"

1. <span data-ttu-id="82d94-136">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration</a> en tant qu’administrateur général ou administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="82d94-136">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a>  as a global admin or SharePoint admin.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="82d94-137">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a> en tant qu’administrateur général ou administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="82d94-137">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>  as a global admin or SharePoint admin.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="82d94-138">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a> en tant qu’administrateur général ou administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="82d94-138">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>  as a global admin or SharePoint admin.</span></span>

::: moniker-end

   <span data-ttu-id="82d94-139">Si vous recevez un message indiquant que vous n’êtes pas autorisé à accéder au centre d’administration, vous ne disposez pas des autorisations d’administrateur dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82d94-139">If you get a message that you don't have permission to access the admin center, then you don't have administrator permissions in your organization.</span></span>

2. <span data-ttu-id="82d94-140">Dans le volet gauche, sélectionnez **centres** \> d’administration **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="82d94-140">In the left pane, select **Admin centers** \> **SharePoint**.</span></span> <span data-ttu-id="82d94-141">(Vous devrez peut-être sélectionner **Afficher tout** pour afficher la liste des centres d’administration.)</span><span class="sxs-lookup"><span data-stu-id="82d94-141">(You might need to select **Show all** to see the list of admin centers.)</span></span>

3. <span data-ttu-id="82d94-142">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="82d94-142">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

4. <span data-ttu-id="82d94-143">Dans le volet gauche, sélectionnez **plus de fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="82d94-143">In the left pane, select **More features**.</span></span>

5. <span data-ttu-id="82d94-144">Sous **profils utilisateur**, sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="82d94-144">Under **User profiles**, select **Open**.</span></span>

6. <span data-ttu-id="82d94-145">Sous **personnes**, sélectionnez **gérer les profils utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="82d94-145">Under **People**, select **Manage User Profiles**.</span></span>

7. <span data-ttu-id="82d94-146">Entrez le nom de l’utilisateur et sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="82d94-146">Enter the user's name and select **Find**.</span></span>

8. <span data-ttu-id="82d94-147">Cliquez avec le bouton droit sur l’utilisateur, puis choisissez **gérer les propriétaires de collection de sites**.</span><span class="sxs-lookup"><span data-stu-id="82d94-147">Right-click the user, and then choose **Manage site collection owners**.</span></span>

9. <span data-ttu-id="82d94-148">Supprimez la personne qui n’a plus besoin d’accéder aux données de l’utilisateur, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="82d94-148">Remove the person who no longer needs access to the user's data, and then select **OK**.</span></span>

    
## <a name="access-the-outlook-data-of-a-former-user"></a><span data-ttu-id="82d94-149">Accéder aux données Outlook d’un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="82d94-149">Access the Outlook data of a former user</span></span>

<span data-ttu-id="82d94-150">Pour enregistrer les messages électroniques, le calendrier, les tâches et les contacts de l’ancien employé, exportez les informations vers un fichier de données Outlook (. pst).</span><span class="sxs-lookup"><span data-stu-id="82d94-150">To save the email messages, calendar, tasks, and contacts of the former employee, export the information to an Outlook Data File (.pst).</span></span>
  
1. <span data-ttu-id="82d94-151">[Ajoutez le message électronique de l’ancien employé](https://support.office.com/article/6e27792a-9267-4aa4-8bb6-c84ef146101b.aspx) à votre Outlook (si vous [réinitialisez le mot de passe de l’utilisateur](reset-passwords.md), vous pouvez le définir sur une valeur qui ne vous indique que).</span><span class="sxs-lookup"><span data-stu-id="82d94-151">[Add the former employee's email](https://support.office.com/article/6e27792a-9267-4aa4-8bb6-c84ef146101b.aspx) to your Outlook (If you [reset the user's password](reset-passwords.md), you can set it to something only you know.)</span></span>
    
2. <span data-ttu-id="82d94-152">Dans Outlook, sélectionnez **fichier**.</span><span class="sxs-lookup"><span data-stu-id="82d94-152">In Outlook, select **File**.</span></span>
    
    ![Voici à quoi ressemble le ruban dans Outlook 2016.](../media/d7f66ed3-9861-4521-b410-e86a58ab15a7.png)
  
3. <span data-ttu-id="82d94-154">Sélectionnez \*\*ouvrir &amp; \*\* l' \> **importation/exportation**de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="82d94-154">Select **Open &amp; Export** \> **Import/Export**.</span></span>
    
    ![Commande d’importation/exportation en mode Backstage](../media/6013919e-d8ce-4902-b7b4-78ff4260a2f8.jpg)
  
4. <span data-ttu-id="82d94-156">Sélectionnez **Exporter vers un fichier**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="82d94-156">Select **Export to a file**, and then select **Next**.</span></span>
    
    ![Option Exporter vers un fichier dans l’Assistant d’importation et d’exportation](../media/458466a0-366b-4fbf-a2db-1919412c6527.jpg)
  
5. <span data-ttu-id="82d94-158">Sélectionnez **fichier de données Outlook (. pst)**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="82d94-158">Select **Outlook Data File (.pst)**, and then select **Next**.</span></span>
    
6. <span data-ttu-id="82d94-159">Sélectionnez le compte que vous souhaitez exporter en sélectionnant le nom ou l’adresse de messagerie, par exemple, Weiler ou anne@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="82d94-159">Select the account you want to export by selecting the name or email address, such as Mailbox - Anne Weiler or anne@contoso.com.</span></span> <span data-ttu-id="82d94-160">Si vous souhaitez exporter tout le contenu de votre compte, y compris le courrier, le calendrier, les contacts, les tâches et les notes, vérifiez que la case à cocher **inclure les sous-dossiers** est activée.</span><span class="sxs-lookup"><span data-stu-id="82d94-160">If you want to export everything in your account, including mail, calendar, contacts, tasks, and notes, make sure the **Include subfolders** check box is selected.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="82d94-161">Vous pouvez exporter un compte à la fois.</span><span class="sxs-lookup"><span data-stu-id="82d94-161">You can export one account at a time.</span></span> <span data-ttu-id="82d94-162">Si vous souhaitez exporter plusieurs comptes, après l’exportation d’un compte, répétez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="82d94-162">If you want to export multiple accounts, after one account is exported, repeat these steps.</span></span> 
  
    ![Boîte de dialogue Exporter le fichier de données Outlook avec le dossier supérieur sélectionné et inclure les sous-dossiers activés](../media/ce36616f-d76d-4ce2-b517-8ac4874e0971.jpg)
  
7. <span data-ttu-id="82d94-164">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82d94-164">Select **Next**.</span></span>
    
8. <span data-ttu-id="82d94-165">Sélectionnez **Parcourir** pour sélectionner l’emplacement d’enregistrement du fichier de données Outlook (. pst).</span><span class="sxs-lookup"><span data-stu-id="82d94-165">Select **Browse** to select where to save the Outlook Data File (.pst).</span></span> <span data-ttu-id="82d94-166">Tapez un *nom de fichier*, puis cliquez sur **OK** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="82d94-166">Type a  *file name*, and then select **OK** to continue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="82d94-167">Si vous avez utilisé l’exportation avant, l’emplacement du dossier et le nom de fichier précédents apparaissent.</span><span class="sxs-lookup"><span data-stu-id="82d94-167">If you've used export before, the previous folder location and file name appear.</span></span> <span data-ttu-id="82d94-168">Tapez un *autre nom de fichier* avant de sélectionner **OK**.</span><span class="sxs-lookup"><span data-stu-id="82d94-168">Type a  *different file name*  before selecting **OK**.</span></span> 
  
9. <span data-ttu-id="82d94-169">Si vous effectuez l’exportation vers un fichier de données Outlook (. pst) existant, sous **options**, spécifiez les actions à effectuer lors de l’exportation d’éléments qui existent déjà dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="82d94-169">If you are exporting to an existing Outlook Data File (.pst), under **Options**, specify what to do when exporting items that already exist in the file.</span></span>
    
10. <span data-ttu-id="82d94-170">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="82d94-170">Select **Finish**.</span></span>
    
<span data-ttu-id="82d94-171">Outlook commence l’exportation immédiatement sauf si un nouveau fichier de données Outlook (. pst) est créé ou si un fichier protégé par mot de passe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="82d94-171">Outlook begins the export immediately unless a new Outlook Data File (.pst) is created or a password-protected file is used.</span></span>
  
   - <span data-ttu-id="82d94-172">Si vous créez un fichier de données Outlook (. pst), un mot de passe facultatif peut aider à protéger le fichier.</span><span class="sxs-lookup"><span data-stu-id="82d94-172">If you're creating an Outlook Data File (.pst), an optional password can help protect the file.</span></span> <span data-ttu-id="82d94-173">Lorsque la boîte de dialogue **créer un fichier de données Outlook** s’affiche, tapez le *mot de passe* dans les zones **mot** de passe et **confirmer le mot de passe** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="82d94-173">When the **Create Outlook Data File** dialog box appears, type the  *password*  in the **Password** and **Verify Password** boxes, and then select **OK**.</span></span> <span data-ttu-id="82d94-174">Dans la boîte de dialogue **mot de passe du fichier de données Outlook** , tapez le *mot de passe*, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="82d94-174">In the **Outlook Data File Password** dialog box, type the  *password*, and then select **OK**.</span></span>
    
  - <span data-ttu-id="82d94-175">Si vous effectuez une exportation vers un fichier de données Outlook (. pst) qui est protégé par mot de passe, dans la boîte de dialogue **mot de passe du fichier de données Outlook** , tapez le *mot de passe*, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="82d94-175">If you're exporting to an existing Outlook Data File (.pst) that is password protected, in the **Outlook Data File Password** dialog box, type the  *password*, and then select **OK**.</span></span>
    
<span data-ttu-id="82d94-176">Découvrez comment [exporter ou sauvegarder des courriers électroniques, des contacts et des calendriers dans un fichier. pst Outlook](https://support.office.com/article/14252b52-3075-4e9b-be4e-ff9ef1068f91.aspx) dans Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="82d94-176">See how to [Export or backup email, contacts, and calendar to an Outlook .pst file](https://support.office.com/article/14252b52-3075-4e9b-be4e-ff9ef1068f91.aspx) in Outlook 2010.</span></span> 
  
## <a name="give-another-user-access-to-a-former-users-email"></a><span data-ttu-id="82d94-177">Accorder à un autre utilisateur l’accès à l’adresse de messagerie d’un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="82d94-177">Give another user access to a former user's email</span></span> 

<span data-ttu-id="82d94-178">Pour accorder l’accès aux messages électroniques, au calendrier, aux tâches et aux contacts de l’ancien employé à un autre employé, importez les informations dans la boîte de réception Outlook d’un autre employé.</span><span class="sxs-lookup"><span data-stu-id="82d94-178">To give access to the email messages, calendar, tasks, and contacts of the former employee to another employee, import the information to another employee's Outlook inbox.</span></span>

> [!NOTE]
> <span data-ttu-id="82d94-179">Vous pouvez également [convertir la boîte aux lettres de l’ancien utilisateur en boîte aux lettres partagée](https://docs.microsoft.com/office365/admin/email/convert-user-mailbox-to-shared-mailbox) ou [transférer le courrier électronique d’un ancien employé à un autre employé](https://docs.microsoft.com/office365/admin/add-users/remove-former-employee#forward-a-former-employees-email-to-another-employee-or-convert-to-a-shared-mailbox).</span><span class="sxs-lookup"><span data-stu-id="82d94-179">You can also [convert the former user's mailbox to a shared mailbox](https://docs.microsoft.com/office365/admin/email/convert-user-mailbox-to-shared-mailbox) or [forward a former employee's email to another employee](https://docs.microsoft.com/office365/admin/add-users/remove-former-employee#forward-a-former-employees-email-to-another-employee-or-convert-to-a-shared-mailbox).</span></span>

  
1. <span data-ttu-id="82d94-180">Dans Outlook, accédez à **fichier** \> **: &amp; ouvrir exporter** \> l' **importation/exportation**.</span><span class="sxs-lookup"><span data-stu-id="82d94-180">In Outlook, go to **File** \> **Open &amp; Export** \> **Import/Export**.</span></span>
    
    <span data-ttu-id="82d94-181">Cette opération démarre l’Assistant d’importation et d’exportation.</span><span class="sxs-lookup"><span data-stu-id="82d94-181">This starts the Import and Export Wizard.</span></span>
    
2. <span data-ttu-id="82d94-182">Sélectionnez **Importer à partir d’un autre programme ou fichier**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="82d94-182">Select **Import from another program or file**, and then select **Next**.</span></span>
    
    ![Assistant d’importation et d’exportation](../media/15cdd674-cd7b-492c-8e93-992cfa890f26.jpg)
  
3. <span data-ttu-id="82d94-184">Sélectionnez **fichier de données Outlook (. pst)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="82d94-184">Select **Outlook Data File (.pst)**, and select **Next**.</span></span>
    
4. <span data-ttu-id="82d94-185">Accédez au fichier. pst que vous souhaitez importer.</span><span class="sxs-lookup"><span data-stu-id="82d94-185">Browse to the .pst file you want to import.</span></span>
    
5. <span data-ttu-id="82d94-186">Sous **options**, choisissez le mode de traitement des doublons.</span><span class="sxs-lookup"><span data-stu-id="82d94-186">Under **Options**, choose how you want to deal with duplicates</span></span>
    
6. <span data-ttu-id="82d94-187">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82d94-187">Select **Next**.</span></span>
    
7. <span data-ttu-id="82d94-188">Si un mot de passe a été attribué au fichier de données Outlook (. pst), entrez le mot de passe, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="82d94-188">If a password was assigned to the Outlook Data File (.pst), enter the password, and then select **OK**.</span></span>
    
8. <span data-ttu-id="82d94-189">Définir les options d’importation des éléments.</span><span class="sxs-lookup"><span data-stu-id="82d94-189">Set the options for importing items.</span></span> <span data-ttu-id="82d94-190">Il n’est généralement pas nécessaire de modifier les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="82d94-190">The default settings usually don't need to be changed.</span></span>
    
9. <span data-ttu-id="82d94-191">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="82d94-191">Select **Finish**.</span></span>
    
> [!TIP]
> <span data-ttu-id="82d94-192">Si vous souhaitez importer ou restaurer uniquement quelques éléments à partir d’un fichier de données Outlook (. pst), vous pouvez ouvrir le fichier de données Outlook.</span><span class="sxs-lookup"><span data-stu-id="82d94-192">If you want to import or restore only a few items from an Outlook Data File (.pst), you can open the Outlook Data File.</span></span> <span data-ttu-id="82d94-193">Ensuite, dans le volet de navigation, faites glisser les éléments des dossiers du fichier de données Outlook vers vos dossiers Outlook existants.</span><span class="sxs-lookup"><span data-stu-id="82d94-193">Then, in the navigation pane, drag the items from Outlook Data File folders to your existing Outlook folders.</span></span> 
  
  
## <a name="related-articles"></a><span data-ttu-id="82d94-194">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="82d94-194">Related articles</span></span>
[<span data-ttu-id="82d94-195">Supprimer un ancien employé d'Office 365</span><span class="sxs-lookup"><span data-stu-id="82d94-195">Remove a former employee from Office 365</span></span>](remove-former-employee.md)

[<span data-ttu-id="82d94-196">Ajouter et supprimer des administrateurs sur un compte OneDrive</span><span class="sxs-lookup"><span data-stu-id="82d94-196">Add and remove admins on a OneDrive account</span></span>](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)

[<span data-ttu-id="82d94-197">Restaurer un OneDrive supprimé</span><span class="sxs-lookup"><span data-stu-id="82d94-197">Restore a deleted OneDrive</span></span>](/onedrive/restore-deleted-onedrive)
  
[<span data-ttu-id="82d94-198">Rétention et suppression de OneDrive</span><span class="sxs-lookup"><span data-stu-id="82d94-198">OneDrive retention and deletion</span></span>](/onedrive/retention-and-deletion)
  

