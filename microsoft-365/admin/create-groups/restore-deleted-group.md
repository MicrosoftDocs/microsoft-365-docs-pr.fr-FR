---
title: Restaurer un groupe Office 365 supprimé
ms.reviewer: arvaradh
f1.keywords:
- CSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b7c66b59-657a-4e1a-8aa0-8163b1f4eb54
description: 'Découvrez comment restaurer un groupe Office 365 supprimé à l’aide du centre d’administration Exchange. '
ms.openlocfilehash: c88f10df27e5f3a0af79c93c7d0e347c5646abc9
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42352435"
---
# <a name="restore-a-deleted-office-365-group"></a><span data-ttu-id="02ba8-103">Restaurer un groupe Office 365 supprimé</span><span class="sxs-lookup"><span data-stu-id="02ba8-103">Restore a deleted Office 365 Group</span></span>

<span data-ttu-id="02ba8-104">Si vous êtes le propriétaire d’un groupe Office 365, vous pouvez restaurer le groupe vous-même en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="02ba8-104">If you are the owner of an Office 365 group, you can restore the group yourself by following these steps.</span></span>

1. <span data-ttu-id="02ba8-105">Sur la [page groupes supprimés](https://outlook.office.com/people/group/deleted), sélectionnez l’option **gérer les groupes** sous le nœud **groupes** , puis choisissez **supprimé**.</span><span class="sxs-lookup"><span data-stu-id="02ba8-105">On the [deleted groups page](https://outlook.office.com/people/group/deleted), select the **Manage groups** option under the **Groups** node, and then choose **Deleted**.</span></span>
2. <span data-ttu-id="02ba8-106">Cliquez sur l’onglet **restaurer** en regard du groupe que vous souhaitez restaurer.</span><span class="sxs-lookup"><span data-stu-id="02ba8-106">Click on the **Restore** tab next to the group you want to restore.</span></span>

<span data-ttu-id="02ba8-107">Si le groupe supprimé n’apparaît pas ici, contactez un administrateur.</span><span class="sxs-lookup"><span data-stu-id="02ba8-107">If the deleted group doesn't appear here, contact an administrator.</span></span>
  
<span data-ttu-id="02ba8-108">Si vous êtes un utilisateur qui souhaite restaurer un groupe Office 365, demandez à un administrateur de suivre ces étapes pour vous ou de contacter votre support technique.</span><span class="sxs-lookup"><span data-stu-id="02ba8-108">If you're a user who wants to restore an Office 365 group, ask an administrator to do these steps for you or contact your help desk.</span></span>  
   
<span data-ttu-id="02ba8-109">Si vous avez supprimé un groupe, il est conservé pendant 30 jours par défaut.</span><span class="sxs-lookup"><span data-stu-id="02ba8-109">If you've deleted a group, it will be retained for 30 days by default.</span></span> <span data-ttu-id="02ba8-110">Cette période de 30 jours est considérée comme une « suppression récupérable » car vous pouvez toujours restaurer le groupe.</span><span class="sxs-lookup"><span data-stu-id="02ba8-110">This 30-day period is considered a "soft-delete" because you can still restore the group.</span></span> <span data-ttu-id="02ba8-111">Après 30 jours, le groupe et le contenu associé sont supprimés définitivement et ne peuvent pas être restaurés.</span><span class="sxs-lookup"><span data-stu-id="02ba8-111">After 30 days, the group and its associated contents are permanently deleted and cannot be restored.</span></span>
  
<span data-ttu-id="02ba8-112">Pendant la période de suppression « récupérable », si un utilisateur tente d’accéder au site, il obtiendra un message de 404 _interdit_ .</span><span class="sxs-lookup"><span data-stu-id="02ba8-112">During the "soft-delete" period, if a user tries to access the site they will get a 404 _forbidden_ message.</span></span> <span data-ttu-id="02ba8-113">Après cette période, si un utilisateur tente d’accéder au site, il obtiendra un message 404 _introuvable_ .</span><span class="sxs-lookup"><span data-stu-id="02ba8-113">After this period, if a user tries to access the site, they will get a 404 _not found_ message.</span></span>
  
<span data-ttu-id="02ba8-114">En cas de restauration d'un groupe, le contenu suivant est restauré :</span><span class="sxs-lookup"><span data-stu-id="02ba8-114">When a group is restored, the following content is restored:</span></span>
  
- <span data-ttu-id="02ba8-115">Les groupes d’objets, propriétés et membres d’Azure Active Directory (AD) Office 365.</span><span class="sxs-lookup"><span data-stu-id="02ba8-115">Azure Active Directory (AD) Office 365 groups object, properties, and members.</span></span>
    
- <span data-ttu-id="02ba8-116">Adresses de messagerie du groupe.</span><span class="sxs-lookup"><span data-stu-id="02ba8-116">Group's e-mail addresses.</span></span>
    
- <span data-ttu-id="02ba8-117">Calendrier et boîte de réception partagés Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="02ba8-117">Exchange Online shared Inbox and calendar.</span></span>
    
- <span data-ttu-id="02ba8-118">Site et fichiers d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="02ba8-118">SharePoint Online team site and files.</span></span>
    
- <span data-ttu-id="02ba8-119">bloc-notes OneNote ;</span><span class="sxs-lookup"><span data-stu-id="02ba8-119">OneNote notebook</span></span>
    
- <span data-ttu-id="02ba8-120">Planificateur.</span><span class="sxs-lookup"><span data-stu-id="02ba8-120">Planner</span></span>
    
- <span data-ttu-id="02ba8-121">Teams</span><span class="sxs-lookup"><span data-stu-id="02ba8-121">Teams</span></span>

- <span data-ttu-id="02ba8-122">Groupe Yammer et contenu de groupe (si le groupe Office 365 a été créé à partir de Yammer)</span><span class="sxs-lookup"><span data-stu-id="02ba8-122">Yammer group and group content (If the Office 365 group was created from Yammer)</span></span>
    
<span data-ttu-id="02ba8-123">Vous pouvez [Supprimer un groupe Office 365 de manière définitive](#permanently-delete-an-office-365-group) si vous voulez supprimer définitivement le contenu avant la fin de la période de rétention de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="02ba8-123">You can also [Permanently delete an Office 365 group](#permanently-delete-an-office-365-group) if you can't wait the 30 days for the retention period to expire for the content to be permanently deleted.</span></span> 

> [!NOTE]
> <span data-ttu-id="02ba8-124">Le propriétaire du groupe Office 365 supprimé peut également restaurer le groupe.</span><span class="sxs-lookup"><span data-stu-id="02ba8-124">The owner of the deleted Office 365 group is also able to restore the group.</span></span> <span data-ttu-id="02ba8-125">Pour restaurer un groupe Office 365 à l’aide de l’autorisation propriétaire sans autorisation d’administrateur, voir [restaurer un groupe office 365 à l’aide de PowerShell](#restore-an-office-365-group-using-powershell).</span><span class="sxs-lookup"><span data-stu-id="02ba8-125">To restore an office 365 group using owner permission without administrator permission, see [Restore an Office 365 Group using PowerShell](#restore-an-office-365-group-using-powershell).</span></span>

## <a name="restore-an-office-365-group-using-the-exchange-admin-center"></a><span data-ttu-id="02ba8-126">Restaurer un groupe Office 365 via le Centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="02ba8-126">Restore an Office 365 Group using the Exchange admin center</span></span>

<span data-ttu-id="02ba8-127">Vous devez disposer des autorisations d’administrateur global d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="02ba8-127">You must have Office 365 global administrator permissions.</span></span>

1. <span data-ttu-id="02ba8-128">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="02ba8-128">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>
    
2. <span data-ttu-id="02ba8-129">Dans le Centre d'administration Exchange, sélectionnez **destinataires**, puis sélectionnez **groupes**.</span><span class="sxs-lookup"><span data-stu-id="02ba8-129">In the Exchange admin center, select **recipients**, and then choose **groups**.</span></span> <span data-ttu-id="02ba8-130">Vous pouvez voir si le groupe est actif ou supprimé de manière récupérable.</span><span class="sxs-lookup"><span data-stu-id="02ba8-130">You can view whether the group is Active or soft-deleted.</span></span> <span data-ttu-id="02ba8-131">Si le groupe a été supprimé de manière définitive, il n'est pas répertorié.</span><span class="sxs-lookup"><span data-stu-id="02ba8-131">If the group has been permanently deleted, it won't be listed at all.</span></span>
  
3. <span data-ttu-id="02ba8-132">Pour afficher l’heure exacte à laquelle le groupe a été supprimé de manière récupérable, sélectionnez le groupe et affichez les informations dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="02ba8-132">To view the exact time when the group was soft-deleted, select the group and view the info in the right pane.</span></span>
      
4. <span data-ttu-id="02ba8-133">Sélectionnez le groupe que vous souhaitez restaurer, puis sélectionnez l’icône restaurer.</span><span class="sxs-lookup"><span data-stu-id="02ba8-133">Select the group you want to restore, and then select the restore icon.</span></span>
    
    ![Sélectionnez le groupe que vous souhaitez restaurer, puis sélectionnez l’icône restaurer.](../../media/restore-group.png)
  
5. <span data-ttu-id="02ba8-135">Sélectionnez actualiser</span><span class="sxs-lookup"><span data-stu-id="02ba8-135">Select refresh</span></span> ![Icône Actualiser](../../media/6464df90-2a91-4c1f-92a6-9a38c7696ac3.gif) <span data-ttu-id="02ba8-137">pour mettre à jour les informations dans la page.</span><span class="sxs-lookup"><span data-stu-id="02ba8-137">to update the information on the page.</span></span> <span data-ttu-id="02ba8-138">Votre groupe aura l'état Actif.</span><span class="sxs-lookup"><span data-stu-id="02ba8-138">Your group will show as Active.</span></span> <span data-ttu-id="02ba8-139">Les formulaires et les données de formulaire associés à votre groupe seront également restaurés.</span><span class="sxs-lookup"><span data-stu-id="02ba8-139">Any forms and form data associated with your group will also be restored.</span></span>
    
## <a name="restore-an-office-365-group-using-powershell"></a><span data-ttu-id="02ba8-140">Restaurer un groupe Office 365 via PowerShell</span><span class="sxs-lookup"><span data-stu-id="02ba8-140">Restore an Office 365 Group using PowerShell</span></span>

<span data-ttu-id="02ba8-141">Vous devez disposer des autorisations d’administrateur global d’Office 365 ou être un ancien propriétaire du groupe Office 365 supprimé.</span><span class="sxs-lookup"><span data-stu-id="02ba8-141">You must have Office 365 global administrator permissions, or be a former owner of the deleted Office 365 group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02ba8-142">Si vous utilisez Remove-MsolGroup dans PowerShell pour supprimer un groupe, le groupe est définitivement supprimé.</span><span class="sxs-lookup"><span data-stu-id="02ba8-142">If you use Remove-MsolGroup in PowerShell to delete a group, this will delete the group permanently.</span></span> <span data-ttu-id="02ba8-143">Lorsque vous utilisez PowerShell pour supprimer des groupes, nous vous recommandons d'utiliser l'applet de commande **Remove-AzureADMSGroup** pour supprimer (suppression réversible) le groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="02ba8-143">When using PowerShell to delete groups, it's best practice to use **Remove-AzureADMSGroup** to soft-delete the Office 365 group.</span></span> <span data-ttu-id="02ba8-144">Vous pourrez ainsi le restaurer, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="02ba8-144">That way you can restore it if needed.</span></span> 
  
### <a name="install-the-preview-version-of-the-azure-active-directory-powershell-for-graph"></a><span data-ttu-id="02ba8-145">Installer la version d'essai de Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="02ba8-145">Install the preview version of the Azure Active Directory PowerShell for Graph</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02ba8-146">Vous ne pouvez pas installer simultanément les versions aperçu et GA sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02ba8-146">You cannot install both the preview and GA versions on the same computer at the same time.</span></span>
  
<span data-ttu-id="02ba8-147">En guise de meilleure pratique, nous vous recommandons de *toujours* rester à jour, c’est-à-dire de désinstaller l’ancienne AzureADPreview ou ancienne version AzureAD et d’obtenir la dernière version.</span><span class="sxs-lookup"><span data-stu-id="02ba8-147">As a best practice, we recommend *always* staying current, i.e. uninstall the old AzureADPreview or old AzureAD version and get the latest one.</span></span> 
  
 
1. <span data-ttu-id="02ba8-148">Dans la barre de recherche, tapez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02ba8-148">In your search bar, type Windows PowerShell.</span></span>
    
2. <span data-ttu-id="02ba8-149">Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="02ba8-149">Right-click on **Windows PowerShell** and select **Run as Administrator**.</span></span>
  
2. <span data-ttu-id="02ba8-150">Passez en revue vos modules installés :</span><span class="sxs-lookup"><span data-stu-id="02ba8-150">Review your installed modules:</span></span>
    
  ```
  Get-InstalledModule -Name "AzureAD*"
  ```

3. <span data-ttu-id="02ba8-151">Pour désinstaller une version précédente de AzureADPreview ou AzureAD, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="02ba8-151">To uninstall a previous version of AzureADPreview or AzureAD, run this command:</span></span>
  
```
   Uninstall-Module AzureADPreview
```

<span data-ttu-id="02ba8-152">ou</span><span class="sxs-lookup"><span data-stu-id="02ba8-152">or</span></span>
  
```
   Uninstall-Module AzureAD
```

4. <span data-ttu-id="02ba8-153">To install the latest version of AzureADPreview, run this command:</span><span class="sxs-lookup"><span data-stu-id="02ba8-153">To install the latest version of AzureADPreview, run this command:</span></span>
  
```
   Install-Module AzureADPreview
```



<span data-ttu-id="02ba8-154">At the message about an untrusted repository, type **Y**. It will take a minute or so for the new module to install. </span><span class="sxs-lookup"><span data-stu-id="02ba8-154">At the message about an untrusted repository, type **Y**. It will take a minute or so for the new module to install.</span></span>
  
### <a name="restore-the-deleted-group"></a><span data-ttu-id="02ba8-155">Restaurer le groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="02ba8-155">Restore the deleted group</span></span>
  
1. <span data-ttu-id="02ba8-156">Avez-vous installé le module **AzureADPreview** , comme indiqué dans la section previoius « installer la version d’évaluation du module Azure Active Directory pour Windows PowerShell » ?</span><span class="sxs-lookup"><span data-stu-id="02ba8-156">Did you install the **AzureADPreview** module, as instructed in the previoius section "Install the preview version of the Azure Active Directory Module for Windows PowerShell"?</span></span>  <span data-ttu-id="02ba8-157">Cette procédure ne fonctionne généralement pas si la version d' **évaluation** la plus récente du module est manquante.</span><span class="sxs-lookup"><span data-stu-id="02ba8-157">Not having the most current **preview** version is the #1 reason these steps don't work for people.</span></span> 
    
2. <span data-ttu-id="02ba8-158">Si ce n'est pas déjà fait, ouvrez une fenêtre Windows PowerShell sur votre ordinateur (il peut s'agir d'une fenêtre Windows PowerShell standard ou d'une fenêtre que vous avez ouvert en sélectionnant **Exécuter en tant qu'administrateur**).</span><span class="sxs-lookup"><span data-stu-id="02ba8-158">If you haven't already, open a Windows PowerShell window on your computer (it doesn't matter if it's a normal Windows PowerShell window, or one you opened by selecting **Run as administrator**).</span></span>
    
3. <span data-ttu-id="02ba8-159">Exécutez les commandes suivantes en appuyant sur **entrée** après chacune d’elles :</span><span class="sxs-lookup"><span data-stu-id="02ba8-159">Run the following commands by pressing **Enter** after each one:</span></span> 
    
  ```
  Import-Module AzureADPreview
  ```

  ```
  Connect-AzureAD
  ```



  <span data-ttu-id="02ba8-160">Dans l’écran Connectez-vous **à votre compte** qui s’ouvre, entrez le nom d’utilisateur et le mot de passe de votre compte administratif pour vous connecter à votre service Azure ad, puis sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="02ba8-160">On the **Sign in to your Account** screen that opens, enter your administrative account user name and password to connect you to your Azure AD service, and select **Sign in**.</span></span>
  
4. <span data-ttu-id="02ba8-161">Exécutez cette commande pour afficher tous les groupes Office 365 supprimés de votre organisation qui se trouvent encore dans la période de suppression logicielle de 30 jours :</span><span class="sxs-lookup"><span data-stu-id="02ba8-161">Run this command to display all soft-deleted Office 365 groups in your organization that are still within the 30 day soft-deletion period:</span></span>
    
  ```
  Get-AzureADMSDeletedGroup
  ```

5. <span data-ttu-id="02ba8-162">Prenez note de l'ID d'objet du ou des groupes que vous voulez restaurer.</span><span class="sxs-lookup"><span data-stu-id="02ba8-162">Take note of the object ID of the group, or groups, you want to restore.</span></span> <span data-ttu-id="02ba8-163">Si vous ne voyez pas le groupe que vous recherchez dans cette liste, il a probablement été définitivement purgé.</span><span class="sxs-lookup"><span data-stu-id="02ba8-163">If you don't see the group you're looking for on this list then it has likely been permanently purged already.</span></span>
    
    > [!CAUTION]
    > <span data-ttu-id="02ba8-164">Si un groupe a été créé avec le même alias ou la même adresse SMTP que votre groupe supprimé, vous devez supprimer ce nouveau groupe pour pouvoir restaurer le groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="02ba8-164">If a new group has been created with the same alias or SMTP address as your deleted group, you will have to delete that new group before you'll be able to restore your deleted group.</span></span> 
  
6. <span data-ttu-id="02ba8-165">Pour restaurer ce groupe, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="02ba8-165">To restore that group, run this command:</span></span>
    
  ```
  Restore-AzureADMSDeletedDirectoryObject -Id <objectId>
  ```

7. <span data-ttu-id="02ba8-166">Ce processus ne prend généralement que quelques minutes, mais dans quelques rares cas, il peut prendre jusqu’à 24 heures pour être entièrement restauré.</span><span class="sxs-lookup"><span data-stu-id="02ba8-166">This process usually takes just a few minutes but in a few rare cases it can take as long as 24 hours to be completely restored.</span></span> <span data-ttu-id="02ba8-167">Pour vérifier que le groupe a été correctement restauré, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="02ba8-167">To verify that the group has been successfully restored, run this command in PowerShell:</span></span>
    
  ```
  Get-AzureADGroup -ObjectId <objectId>
  ```

<span data-ttu-id="02ba8-p110">Une fois restauré, le groupe doit réapparaître dans le volet de navigation d'Outlook et d'Outlook sur le web. Tout le contenu restauré, y compris celui de SharePoint et du Planificateur, doivent être de nouveau accessibles aux membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="02ba8-p110">Once the restore has successfully completed, the group should reappear on the navigation pane in Outlook and Outlook on the web. All restored content, including SharePoint and Planner, should be available to the group members again.</span></span>
  
## <a name="permanently-delete-an-office-365-group"></a><span data-ttu-id="02ba8-170">Supprimer un groupe Office 365 de manière définitive</span><span class="sxs-lookup"><span data-stu-id="02ba8-170">Permanently delete an Office 365 group</span></span>

<span data-ttu-id="02ba8-171">Il peut arriver que vous souhaitiez purger définitivement un groupe sans attendre que la période de suppression du logiciel de 30 jours expire.</span><span class="sxs-lookup"><span data-stu-id="02ba8-171">Sometimes you may want to permanently purge a group without waiting for the 30 day soft-deletion period to expire.</span></span> <span data-ttu-id="02ba8-172">Pour ce faire, démarrez PowerShell et exécutez la commande suivante pour obtenir l'ID d'objet du groupe.</span><span class="sxs-lookup"><span data-stu-id="02ba8-172">To do that, start PowerShell and run this command to get the object ID of the group:</span></span>
  
```
Get-AzureADMSDeletedGroup
```

<span data-ttu-id="02ba8-173">Prenez note de l’ID d’objet du ou des groupes que vous souhaitez supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="02ba8-173">Take note of the object ID of the group, or groups, that you want to permanently delete.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="02ba8-174">La suppression définitive du groupe supprime le groupe et ses données pour toujours.</span><span class="sxs-lookup"><span data-stu-id="02ba8-174">Purging the group removes the group and its data forever.</span></span> 
  
<span data-ttu-id="02ba8-175">Pour supprimer définitivement le groupe, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="02ba8-175">To purge the group run this command in PowerShell:</span></span>
  
```
Remove-AzureADMSDeletedDirectoryObject -Id <objectId>
```

<span data-ttu-id="02ba8-p112">Pour vérifier que le groupe a été supprimé définitivement, réexécutez l'applet de commande  *Get-AzureADMSDeletedGroup*  pour confirmer que le groupe n'apparaît plus dans la liste des groupes supprimés (suppression réversible). Dans certains cas, la suppression définitive du groupe et de toutes ses données peut prendre jusqu'à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="02ba8-p112">To confirm that the group has been successfully purged, run the  *Get-AzureADMSDeletedGroup*  cmdlet again to confirm that the group no longer appears on the list of soft-deleted groups. In some cases it may take as long as 24 hours for the group and all of its data to be permanently deleted.</span></span> 
  
## <a name="got-questions-about-office-365-groups"></a><span data-ttu-id="02ba8-178">Vous avez des questions sur les groupes Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="02ba8-178">Got questions about Office 365 Groups?</span></span>

<span data-ttu-id="02ba8-179">Visitez la [communauté Microsoft Tech](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) pour publier des questions et participer à des conversations sur les groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="02ba8-179">Visit the [Microsoft Tech Community](https://techcommunity.microsoft.com/t5/Office-365-Groups/ct-p/Office365Groups) to post questions and participate in conversations about Office 365 Groups.</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="02ba8-180">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="02ba8-180">Related articles</span></span>

[<span data-ttu-id="02ba8-181">Utiliser PowerShell pour gérer les groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="02ba8-181">Manage Office 365 Groups with PowerShell</span></span>](https://support.office.com/article/aeb669aa-1770-4537-9de2-a82ac11b0540)
  
[<span data-ttu-id="02ba8-182">Supprimer des groupes à l'aide de l'applet de commande Remove-UnifiedGroup</span><span class="sxs-lookup"><span data-stu-id="02ba8-182">Delete groups using the Remove-UnifiedGroup cmdlet</span></span>](https://technet.microsoft.com/library/mt238270%28v=exchg.160%29.aspx)
  
[<span data-ttu-id="02ba8-183">Gérer les paramètres de votre site d'équipe connecté à un groupe</span><span class="sxs-lookup"><span data-stu-id="02ba8-183">Manage your group-connected team site settings</span></span>](https://support.office.com/article/8376034d-d0c7-446e-9178-6ab51c58df42.aspx)
  
[<span data-ttu-id="02ba8-184">Supprimer un groupe dans Outlook</span><span class="sxs-lookup"><span data-stu-id="02ba8-184">Delete a group in Outlook</span></span>](https://support.office.com/article/ca7f5a9e-ae4f-4cbe-a4bc-89c469d1726f.aspx)
