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
description: Découvrez comment conserver les fichiers et messages électroniques d'un employé lorsque la personne quitte votre organisation.
ms.openlocfilehash: 17911e4a4551bba07d2c2ad034941bba737dcc1d
ms.sourcegitcommit: 223a36a86753fe9cebee96f05ab4c9a144133677
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51755605"
---
# <a name="get-access-to-and-back-up-a-former-users-data"></a><span data-ttu-id="4c6bf-103">Accéder aux données d'un ancien utilisateur et les sauvegarder</span><span class="sxs-lookup"><span data-stu-id="4c6bf-103">Get access to and back up a former user's data</span></span>


<span data-ttu-id="4c6bf-104">Lorsqu'un employé quitte votre organisation, vous souhaitez probablement accéder à ses données (documents et courriers électroniques) et les consulter, les back up ou les donner à un nouvel employé.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-104">When an employee leaves your organization, you probably want to access their data (documents and emails) and either review it, back it up, or give it to a new employee.</span></span>
  
    
## <a name="access-a-former-users-onedrive-documents"></a><span data-ttu-id="4c6bf-105">Accéder aux documents OneDrive d'un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c6bf-105">Access a former user's OneDrive documents</span></span>

<span data-ttu-id="4c6bf-106">Si vous supprimez la licence d'un utilisateur, mais que vous ne supprimez pas le compte, vous pouvez vous accorder l'accès au contenu du OneDrive de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-106">If you remove a user's license but don't delete the account, you can give yourself access to the content in the user's OneDrive.</span></span> <span data-ttu-id="4c6bf-107">Si vous supprimez le compte de l'utilisateur, vous avez 30 jours par défaut pour accéder aux données OneDrive de l'ancien utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-107">If you delete the user's account, you have 30 days by default to access the former user's OneDrive data.</span></span> <span data-ttu-id="4c6bf-108">[Découvrez comment définir la rétention OneDrive pour les utilisateurs supprimés.](/onedrive/set-retention)</span><span class="sxs-lookup"><span data-stu-id="4c6bf-108">[Learn how to set the OneDrive retention for deleted users](/onedrive/set-retention).</span></span> <span data-ttu-id="4c6bf-109">Si vous ne [restituerez pas de](/office365/admin/add-users/restore-user) compte d'utilisateur dans ce délai, son contenu OneDrive est supprimé.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-109">If you don't [restore a user account](/office365/admin/add-users/restore-user) within this time, their OneDrive content is deleted.</span></span> 

<span data-ttu-id="4c6bf-110">Pour conserver les fichiers OneDrive d'un ancien utilisateur, donnez-vous d'abord accès à son OneDrive, puis déplacez les fichiers que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-110">To preserve a former user's OneDrive files, first give yourself access to their OneDrive, and then move the files you want to keep.</span></span> 

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4c6bf-111">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-111">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

 1. <span data-ttu-id="4c6bf-112">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-112">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="4c6bf-113">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-113">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

::: moniker-end

2. <span data-ttu-id="4c6bf-114">Sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-114">Select a user.</span></span>

3. <span data-ttu-id="4c6bf-115">Dans le volet droit, sélectionnez **OneDrive.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-115">In the right pane, select **OneDrive**.</span></span> <span data-ttu-id="4c6bf-116">Sous **Obtenir l'accès aux fichiers,** **sélectionnez Créer un lien vers des fichiers.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-116">Under **Get access to files**, select **Create link to files**.</span></span>

4. <span data-ttu-id="4c6bf-117">Sélectionnez le lien pour ouvrir l'emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-117">Select the link to open the file location.</span></span> <span data-ttu-id="4c6bf-118">Téléchargez les fichiers sur  votre ordinateur, ou sélectionnez Déplacer vers ou Copier pour les déplacer ou les copier sur votre propre OneDrive ou dans une bibliothèque partagée. </span><span class="sxs-lookup"><span data-stu-id="4c6bf-118">Download the files to your computer, or select **Move to** or **Copy to** to move or copy them to your own OneDrive or to a shared library.</span></span> 

> [!NOTE]
> <span data-ttu-id="4c6bf-119">Vous pouvez déplacer ou copier jusqu'à 500 Mo de fichiers et de dossiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-119">You can move or copy up to 500 MB of files and folders at a time.</span></span><br/>
> <span data-ttu-id="4c6bf-120">Lorsque vous déplacez ou copiez des documents qui ont un historique des versions, seule la dernière version est déplacée.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-120">When you move or copy documents that have version history, only the latest version is moved.</span></span>  

## <a name="revoke-admin-access-to-a-users-onedrive"></a><span data-ttu-id="4c6bf-121">Révoquer l'accès administrateur au OneDrive d'un utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c6bf-121">Revoke admin access to a user's OneDrive</span></span>

<span data-ttu-id="4c6bf-122">En tant qu'administrateur global, vous pouvez vous accorder l'accès au contenu dans OneDrive d'un utilisateur, mais vous pouvez supprimer votre accès lorsque vous n'en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-122">As global admin, you can give yourself access to the content in a user's OneDrive, but you may want to remove your access when you no longer need it.</span></span> 

 ::: moniker range="o365-worldwide"

1. <span data-ttu-id="4c6bf-123">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-123">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4c6bf-124">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-124">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de</a>.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4c6bf-125">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-125">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

::: moniker-end 

2. <span data-ttu-id="4c6bf-126">Dans le volet gauche, sélectionnez **Centres d'administration** \> **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-126">In the left pane, select **Admin centers** \> **SharePoint**.</span></span> <span data-ttu-id="4c6bf-127">(Vous devrez peut-être sélectionner **Afficher tout** pour afficher la liste des centres d’administration.)</span><span class="sxs-lookup"><span data-stu-id="4c6bf-127">(You might need to select **Show all** to see the list of admin centers.)</span></span>

3. <span data-ttu-id="4c6bf-128">Si le Centre d'administration SharePoint classique apparaît, sélectionnez **Ouvrir** maintenant en haut de la page pour ouvrir le Centre d'administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-128">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the SharePoint admin center.</span></span>

4. <span data-ttu-id="4c6bf-129">Dans le volet gauche, sélectionnez **Autres fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-129">In the left pane, select **More features**.</span></span>

5. <span data-ttu-id="4c6bf-130">Sous **Profils utilisateur,** sélectionnez **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-130">Under **User profiles**, select **Open**.</span></span>

6. <span data-ttu-id="4c6bf-131">Sous **Personnes,** sélectionnez **Gérer les profils utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-131">Under **People**, select **Manage User Profiles**.</span></span>

7. <span data-ttu-id="4c6bf-132">Entrez le nom de l'utilisateur et sélectionnez **Rechercher.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-132">Enter the user's name and select **Find**.</span></span>

8. <span data-ttu-id="4c6bf-133">Cliquez avec le bouton droit sur l'utilisateur, puis choisissez **Gérer les propriétaires de collections de sites.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-133">Right-click the user, and then choose **Manage site collection owners**.</span></span>

9. <span data-ttu-id="4c6bf-134">Supprimez la personne qui n'a plus besoin d'accéder aux données de l'utilisateur, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-134">Remove the person who no longer needs access to the user's data, and then select **OK**.</span></span>

    
## <a name="access-the-outlook-data-of-a-former-user"></a><span data-ttu-id="4c6bf-135">Accéder aux données Outlook d'un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c6bf-135">Access the Outlook data of a former user</span></span>

<span data-ttu-id="4c6bf-136">Pour enregistrer les messages électroniques, le calendrier, les tâches et les contacts de l'ancien employé, exportez les informations dans un fichier de données Outlook (.pst).</span><span class="sxs-lookup"><span data-stu-id="4c6bf-136">To save the email messages, calendar, tasks, and contacts of the former employee, export the information to an Outlook Data File (.pst).</span></span>
  
1. <span data-ttu-id="4c6bf-137">[Ajoutez l'e-mail de l'ancien](https://support.microsoft.com/office/6e27792a-9267-4aa4-8bb6-c84ef146101b) employé à votre outlook (si vous réinitialisez le mot de passe de [l'utilisateur,](reset-passwords.md)vous pouvez le définir sur quelque chose que vous connaissez uniquement.)</span><span class="sxs-lookup"><span data-stu-id="4c6bf-137">[Add the former employee's email](https://support.microsoft.com/office/6e27792a-9267-4aa4-8bb6-c84ef146101b) to your Outlook (If you [reset the user's password](reset-passwords.md), you can set it to something only you know.)</span></span>
    
2. <span data-ttu-id="4c6bf-138">Dans Outlook, sélectionnez **Fichier**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-138">In Outlook, select **File**.</span></span>
    
    ![Voici à quoi ressemble le ruban dans Outlook 2016.](../../media/d7f66ed3-9861-4521-b410-e86a58ab15a7.png)
  
3. <span data-ttu-id="4c6bf-140">Sélectionnez **&amp; Ouvrir exporter** \> **l'importation/exportation.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-140">Select **Open &amp; Export** \> **Import/Export**.</span></span>
    
    ![Commande Importer/Exporter en affichage Backstage](../../media/6013919e-d8ce-4902-b7b4-78ff4260a2f8.jpg)
  
4. <span data-ttu-id="4c6bf-142">Sélectionnez **Exporter vers un fichier,** puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-142">Select **Export to a file**, and then select **Next**.</span></span>
    
    ![Exporter vers une option de fichier dans l'Assistant Importation et exportation](../../media/458466a0-366b-4fbf-a2db-1919412c6527.jpg)
  
5. <span data-ttu-id="4c6bf-144">Sélectionnez **fichier de données Outlook (.pst),** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-144">Select **Outlook Data File (.pst)**, and then select **Next**.</span></span>
    
6. <span data-ttu-id="4c6bf-145">Sélectionnez le compte que vous souhaitez exporter en sélectionnant le nom ou l'adresse de messagerie, tel que Mailbox - Anne Weiler ou anne@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-145">Select the account you want to export by selecting the name or email address, such as Mailbox - Anne Weiler or anne@contoso.com.</span></span> <span data-ttu-id="4c6bf-146">Si vous souhaitez exporter tout ce qui se trouve dans votre compte,  y compris la messagerie, le calendrier, les contacts, les tâches et les notes, assurez-vous que la case à cocher Inclure les sous-foldeurs est cocher.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-146">If you want to export everything in your account, including mail, calendar, contacts, tasks, and notes, make sure the **Include subfolders** check box is selected.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="4c6bf-147">Vous pouvez exporter un compte à la fois.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-147">You can export one account at a time.</span></span> <span data-ttu-id="4c6bf-148">Si vous souhaitez exporter plusieurs comptes, une fois qu'un compte est exporté, répétez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-148">If you want to export multiple accounts, after one account is exported, repeat these steps.</span></span> 
  
    ![Boîte de dialogue Exporter le fichier de données Outlook avec le dossier supérieur sélectionné et inclure les sous-dossiers sélectionnés](../../media/ce36616f-d76d-4ce2-b517-8ac4874e0971.jpg)
  
7. <span data-ttu-id="4c6bf-150">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-150">Select **Next**.</span></span>
    
8. <span data-ttu-id="4c6bf-151">Sélectionnez **Parcourir** pour sélectionner l'endroit où enregistrer le fichier de données Outlook (.pst).</span><span class="sxs-lookup"><span data-stu-id="4c6bf-151">Select **Browse** to select where to save the Outlook Data File (.pst).</span></span> <span data-ttu-id="4c6bf-152">Tapez  *un nom de fichier,* puis sélectionnez **OK** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-152">Type a  *file name*, and then select **OK** to continue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="4c6bf-153">Si vous avez déjà utilisé l'exportation, l'emplacement du dossier précédent et le nom de fichier apparaissent.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-153">If you've used export before, the previous folder location and file name appear.</span></span> <span data-ttu-id="4c6bf-154">Tapez *un autre nom de fichier* avant de sélectionner **OK.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-154">Type a  *different file name*  before selecting **OK**.</span></span> 
  
9. <span data-ttu-id="4c6bf-155">Si vous exportez vers un fichier de données Outlook existant (.pst), sous **Options,** spécifiez ce qu'il faut faire lors de l'exportation d'éléments qui existent déjà dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-155">If you are exporting to an existing Outlook Data File (.pst), under **Options**, specify what to do when exporting items that already exist in the file.</span></span>
    
10. <span data-ttu-id="4c6bf-156">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-156">Select **Finish**.</span></span>
    
<span data-ttu-id="4c6bf-157">Outlook commence immédiatement l'exportation, sauf si un nouveau fichier de données Outlook (.pst) est créé ou qu'un fichier protégé par mot de passe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-157">Outlook begins the export immediately unless a new Outlook Data File (.pst) is created or a password-protected file is used.</span></span>
  
   - <span data-ttu-id="4c6bf-158">Si vous créez un fichier de données Outlook (.pst), un mot de passe facultatif peut vous aider à protéger le fichier.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-158">If you're creating an Outlook Data File (.pst), an optional password can help protect the file.</span></span> <span data-ttu-id="4c6bf-159">Lorsque la boîte de dialogue Créer  un fichier de  données **Outlook** s'affiche, tapez le mot de passe dans les zones Mot de passe et Vérifier le mot de passe, puis sélectionnez **OK**. </span><span class="sxs-lookup"><span data-stu-id="4c6bf-159">When the **Create Outlook Data File** dialog box appears, type the  *password*  in the **Password** and **Verify Password** boxes, and then select **OK**.</span></span> <span data-ttu-id="4c6bf-160">Dans la boîte de dialogue Mot de passe du fichier de données **Outlook,** tapez le mot de *passe,* puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-160">In the **Outlook Data File Password** dialog box, type the  *password*, and then select **OK**.</span></span>
    
  - <span data-ttu-id="4c6bf-161">Si vous exportez vers un fichier de données Outlook (.pst) existant protégé par mot de passe, dans la boîte de dialogue Mot de passe du fichier de données **Outlook,** tapez le mot de *passe,* puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="4c6bf-161">If you're exporting to an existing Outlook Data File (.pst) that is password protected, in the **Outlook Data File Password** dialog box, type the  *password*, and then select **OK**.</span></span>
    
<span data-ttu-id="4c6bf-162">Découvrez comment exporter ou sauvegarder le courrier électronique, les contacts et le calendrier dans un fichier [.pst Outlook](https://support.microsoft.com/office/14252b52-3075-4e9b-be4e-ff9ef1068f91) dans Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-162">See how to [Export or backup email, contacts, and calendar to an Outlook .pst file](https://support.microsoft.com/office/14252b52-3075-4e9b-be4e-ff9ef1068f91) in Outlook 2010.</span></span> 
  
  
  > [!NOTE]
  > <span data-ttu-id="4c6bf-163">Par défaut, votre courrier électronique est disponible hors connexion pendant une période de 12 mois.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-163">By default, your email is available offline for a period of 12 months.</span></span> <span data-ttu-id="4c6bf-164">Si nécessaire, voir comment augmenter [les données disponibles hors connexion.](/outlook/troubleshoot/mailboxes/only-subset-items-synchronized)</span><span class="sxs-lookup"><span data-stu-id="4c6bf-164">If required, see how to [increase the data available offline](/outlook/troubleshoot/mailboxes/only-subset-items-synchronized).</span></span>
 
## <a name="give-another-user-access-to-a-former-users-email"></a><span data-ttu-id="4c6bf-165">Accorder à un autre utilisateur l'accès à la messagerie d'un ancien utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c6bf-165">Give another user access to a former user's email</span></span> 

<span data-ttu-id="4c6bf-166">Pour accorder à un autre employé l'accès aux messages électroniques, au calendrier, aux tâches et aux contacts de l'ancien employé, importez les informations dans la boîte de réception Outlook d'un autre employé.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-166">To give access to the email messages, calendar, tasks, and contacts of the former employee to another employee, import the information to another employee's Outlook inbox.</span></span>

> [!NOTE]
> <span data-ttu-id="4c6bf-167">Vous pouvez également convertir la boîte aux lettres de [l'ancien](/office365/admin/email/convert-user-mailbox-to-shared-mailbox) utilisateur en boîte aux lettres partagée ou envoyer le courrier électronique [d'un](/office365/admin/add-users/remove-former-employee#forward-a-former-employees-email-to-another-employee-or-convert-to-a-shared-mailbox)ancien employé à un autre employé.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-167">You can also [convert the former user's mailbox to a shared mailbox](/office365/admin/email/convert-user-mailbox-to-shared-mailbox) or [forward a former employee's email to another employee](/office365/admin/add-users/remove-former-employee#forward-a-former-employees-email-to-another-employee-or-convert-to-a-shared-mailbox).</span></span>

  
1. <span data-ttu-id="4c6bf-168">Dans Outlook, go to **File** \> **Open &amp; Export** \> **Import/Export**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-168">In Outlook, go to **File** \> **Open &amp; Export** \> **Import/Export**.</span></span>
    
    <span data-ttu-id="4c6bf-169">L'Assistant Importation et exportation démarre.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-169">This starts the Import and Export Wizard.</span></span>
    
2. <span data-ttu-id="4c6bf-170">Sélectionnez **Importer à partir d'un autre programme ou fichier,** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-170">Select **Import from another program or file**, and then select **Next**.</span></span>
    
    ![Assistant Importation et exportation](../../media/15cdd674-cd7b-492c-8e93-992cfa890f26.jpg)
  
3. <span data-ttu-id="4c6bf-172">Sélectionnez **fichier de données Outlook (.pst)** et sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-172">Select **Outlook Data File (.pst)**, and select **Next**.</span></span>
    
4. <span data-ttu-id="4c6bf-173">Accédez au fichier .pst à importer.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-173">Browse to the .pst file you want to import.</span></span>
    
5. <span data-ttu-id="4c6bf-174">Sous **Options,** choisissez la façon dont vous souhaitez traiter les doublons</span><span class="sxs-lookup"><span data-stu-id="4c6bf-174">Under **Options**, choose how you want to deal with duplicates</span></span>
    
6. <span data-ttu-id="4c6bf-175">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-175">Select **Next**.</span></span>
    
7. <span data-ttu-id="4c6bf-176">Si un mot de passe a été affecté au fichier de données Outlook (.pst), entrez le mot de passe, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-176">If a password was assigned to the Outlook Data File (.pst), enter the password, and then select **OK**.</span></span>
    
8. <span data-ttu-id="4c6bf-177">Définissez les options d'importation d'éléments.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-177">Set the options for importing items.</span></span> <span data-ttu-id="4c6bf-178">Les paramètres par défaut n'ont généralement pas besoin d'être modifiés.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-178">The default settings usually don't need to be changed.</span></span>
    
9. <span data-ttu-id="4c6bf-179">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-179">Select **Finish**.</span></span>

> [!NOTE]
> <span data-ttu-id="4c6bf-180">Les étapes restent les mêmes pour accéder aux données OneDrive et de messagerie d'un utilisateur existant.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-180">The steps remain the same for accessing an existing user's OneDrive and email data.</span></span>
    
> [!TIP]
> <span data-ttu-id="4c6bf-181">Si vous souhaitez importer ou restaurer uniquement quelques éléments à partir d'un fichier de données Outlook (.pst), vous pouvez ouvrir le fichier de données Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-181">If you want to import or restore only a few items from an Outlook Data File (.pst), you can open the Outlook Data File.</span></span> <span data-ttu-id="4c6bf-182">Ensuite, dans le volet de navigation, faites glisser les éléments des dossiers de fichiers de données Outlook vers vos dossiers Outlook existants.</span><span class="sxs-lookup"><span data-stu-id="4c6bf-182">Then, in the navigation pane, drag the items from Outlook Data File folders to your existing Outlook folders.</span></span> 
  
  
## <a name="related-articles"></a><span data-ttu-id="4c6bf-183">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="4c6bf-183">Related articles</span></span>
[<span data-ttu-id="4c6bf-184">Supprimer un ancien employé d'Office 365</span><span class="sxs-lookup"><span data-stu-id="4c6bf-184">Remove a former employee from Office 365</span></span>](remove-former-employee.md)

[<span data-ttu-id="4c6bf-185">Ajouter et supprimer des administrateurs sur un compte OneDrive</span><span class="sxs-lookup"><span data-stu-id="4c6bf-185">Add and remove admins on a OneDrive account</span></span>](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)

[<span data-ttu-id="4c6bf-186">Restaurer un OneDrive supprimé</span><span class="sxs-lookup"><span data-stu-id="4c6bf-186">Restore a deleted OneDrive</span></span>](/onedrive/restore-deleted-onedrive)
  
[<span data-ttu-id="4c6bf-187">Rétention et suppression sur OneDrive</span><span class="sxs-lookup"><span data-stu-id="4c6bf-187">OneDrive retention and deletion</span></span>](/onedrive/retention-and-deletion)
