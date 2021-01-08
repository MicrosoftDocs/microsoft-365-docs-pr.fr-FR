---
title: Préparation d’un domaine non routable pour la synchronisation d’annuaires
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- O365E_SetupDirSyncLocalDir
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: e7968303-c234-46c4-b8b0-b5c93c6d57a7
description: Découvrez comment faire si vous avez un domaine non routable associé à vos comptes d’utilisateurs locaux avant de les synchroniser avec votre client Microsoft 365.
ms.openlocfilehash: dcd941bbae159afeb0cf6ef4f5acbaf409966295
ms.sourcegitcommit: ec293978e951b09903b79e6642aa587824935e0c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "49780331"
---
# <a name="prepare-a-non-routable-domain-for-directory-synchronization"></a><span data-ttu-id="48b92-103">Préparation d’un domaine non routable pour la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="48b92-103">Prepare a non-routable domain for directory synchronization</span></span>

<span data-ttu-id="48b92-104">Lorsque vous synchronisez votre annuaire local avec Microsoft 365, vous devez avoir un domaine vérifié dans Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="48b92-104">When you synchronize your on-premises directory with Microsoft 365, you have to have a verified domain in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="48b92-105">Seuls les noms d’utilisateur principaux (UPN) associés au domaine AD DS (Active Directory Domain Services) local sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="48b92-105">Only the User Principal Names (UPNs) that are associated with the on-premises Active Directory Domain Services (AD DS) domain are synchronized.</span></span> <span data-ttu-id="48b92-106">Toutefois, tout UPN qui contient un domaine non routable, tel que « .local » (exemple : billa@contoso.local), sera synchronisé avec un domaine .onmicrosoft.com (exemple : billa@contoso.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="48b92-106">However, any UPN that contains a non-routable domain, such as ".local" (example: billa@contoso.local), will be synchronized to an .onmicrosoft.com domain (example: billa@contoso.onmicrosoft.com).</span></span> 

<span data-ttu-id="48b92-107">Si vous utilisez actuellement un domaine « .local » pour vos comptes d’utilisateur dans AD DS, il est recommandé de les modifier pour utiliser un domaine vérifié, tel que billa@contoso.com, afin de synchroniser correctement avec votre domaine Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48b92-107">If you currently use a ".local" domain for your user accounts in AD DS, it's recommended that you change them to use a verified domain, such as billa@contoso.com, in order to properly synchronize with your Microsoft 365 domain.</span></span>
  
## <a name="what-if-i-only-have-a-local-on-premises-domain"></a><span data-ttu-id="48b92-108">Que se passe-t-il si je n’ai qu’un domaine local « .local » ?</span><span class="sxs-lookup"><span data-stu-id="48b92-108">What if I only have a ".local" on-premises domain?</span></span>

<span data-ttu-id="48b92-109">Vous utilisez Azure AD Connect pour synchroniser vos AD DS avec le client Azure AD de votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48b92-109">You use Azure AD Connect for synchronizing your AD DS to the Azure AD tenant of your Microsoft 365 tenant.</span></span> <span data-ttu-id="48b92-110">Pour plus d’informations, voir Intégration de vos [identités locales à Azure AD.](https://docs.microsoft.com/azure/architecture/reference-architectures/identity/azure-ad)</span><span class="sxs-lookup"><span data-stu-id="48b92-110">For more information, see [Integrating your on-premises identities with Azure AD](https://docs.microsoft.com/azure/architecture/reference-architectures/identity/azure-ad).</span></span>
  
<span data-ttu-id="48b92-111">Azure AD Connect synchronise l’UPN et le mot de passe de vos utilisateurs afin que les utilisateurs peuvent se connecter avec les mêmes informations d’identification qu’ils utilisent en local.</span><span class="sxs-lookup"><span data-stu-id="48b92-111">Azure AD Connect synchronizes your users' UPN and password so that users can sign in with the same credentials they use on-premises.</span></span> <span data-ttu-id="48b92-112">Toutefois, Azure AD Connect synchronise uniquement les utilisateurs avec les domaines vérifiés par Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48b92-112">However, Azure AD Connect only synchronizes users to domains that are verified by Microsoft 365.</span></span> <span data-ttu-id="48b92-113">Cela signifie que le domaine est également vérifié par Azure AD, car les identités Microsoft 365 sont gérées par Azure AD.</span><span class="sxs-lookup"><span data-stu-id="48b92-113">This means that the domain also is verified by Azure AD because Microsoft 365 identities are managed by Azure AD.</span></span> <span data-ttu-id="48b92-114">En d’autres termes, le domaine doit être un domaine Internet valide (par exemple, .com, .org, .net, .us).</span><span class="sxs-lookup"><span data-stu-id="48b92-114">In other words, the domain has to be a valid Internet domain (such as, .com, .org, .net, .us).</span></span> <span data-ttu-id="48b92-115">Si votre AD DS interne utilise uniquement un domaine non routable (par exemple, « .local »), cela ne peut pas correspondre au domaine vérifié dont vous avez besoin pour votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48b92-115">If your internal AD DS only uses a non-routable domain (for example, ".local"), this can't possibly match the verified domain you have for your Microsoft 365 tenant.</span></span> <span data-ttu-id="48b92-116">Vous pouvez résoudre ce problème en modifiant votre domaine principal dans votre AD DS local ou en ajoutant un ou plusieurs suffixes UPN.</span><span class="sxs-lookup"><span data-stu-id="48b92-116">You can fix this issue by either changing your primary domain in your on-premises AD DS, or by adding one or more UPN suffixes.</span></span>
  
### <a name="change-your-primary-domain"></a><span data-ttu-id="48b92-117">Modifier votre domaine principal</span><span class="sxs-lookup"><span data-stu-id="48b92-117">Change your primary domain</span></span>

<span data-ttu-id="48b92-118">Modifiez votre domaine principal en un domaine que vous avez vérifié dans Microsoft 365, par exemple, contoso.com.</span><span class="sxs-lookup"><span data-stu-id="48b92-118">Change your primary domain to a domain you have verified in Microsoft 365, for example, contoso.com.</span></span> <span data-ttu-id="48b92-119">Chaque utilisateur qui possède le domaine contoso.local est ensuite mis à jour contoso.com.</span><span class="sxs-lookup"><span data-stu-id="48b92-119">Every user that has the domain contoso.local is then updated to contoso.com.</span></span> <span data-ttu-id="48b92-120">Il s’agit toutefois d’un processus très complexe et une solution plus facile est décrite dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="48b92-120">This is a very involved process, however, and an easier solution is described in the following section.</span></span>
  
### <a name="add-upn-suffixes-and-update-your-users-to-them"></a><span data-ttu-id="48b92-121">Ajouter des suffixes UPN et mettre à jour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="48b92-121">Add UPN suffixes and update your users to them</span></span>

<span data-ttu-id="48b92-122">Vous pouvez résoudre le problème « .local » en enregistrant de nouveaux suffixes UPN dans AD DS pour qu’ils correspondent au ou aux domaines que vous avez vérifiés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48b92-122">You can solve the ".local" problem by registering new UPN suffix or suffixes in AD DS to match the domain (or domains) you verified in Microsoft 365.</span></span> <span data-ttu-id="48b92-123">Après avoir inscrit le nouveau suffixe, vous mettez à jour les UPN utilisateur pour remplacer le « .local » par le nouveau nom de domaine, par exemple, afin qu’un compte d’utilisateur ressemble à billa@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="48b92-123">After you register the new suffix, you update the user UPNs to replace the ".local" with the new domain name, for example, so that a user account looks like billa@contoso.com.</span></span>
  
<span data-ttu-id="48b92-124">Une fois que vous avez mis à jour les UPN pour utiliser le domaine vérifié, vous êtes prêt à synchroniser vos AD DS locaux avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48b92-124">After you have updated the UPNs to use the verified domain, you are ready to synchronize your on-premises AD DS with Microsoft 365.</span></span>
  
#### <a name="step-1-add-the-new-upn-suffix"></a><span data-ttu-id="48b92-125">Étape 1 : Ajouter le nouveau suffixe UPN\*\*</span><span class="sxs-lookup"><span data-stu-id="48b92-125">Step 1: Add the new UPN suffix\*\*</span></span>
  
1. <span data-ttu-id="48b92-126">Sur le contrôleur de domaine AD DS, dans le Gestionnaire de serveur, choisissez Outils Domaines et  \> **trusts Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="48b92-126">On the AD DS domain controller, in the Server Manager choose **Tools** \> **Active Directory Domains and Trusts**.</span></span>
    
    <span data-ttu-id="48b92-127">**Ou, si vous n’avez pas Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48b92-127">**Or, if you don't have Windows Server 2012**</span></span>
    
    <span data-ttu-id="48b92-128">Appuyez sur la touche  Windows + **R** pour ouvrir la boîte de dialogue Exécuter, puis tapez Domain.msc, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="48b92-128">Press **Windows key + R** to open the **Run** dialog, and then type in Domain.msc, and then choose **OK**.</span></span>
    
    ![Choisissez Domaines et trusts Active Directory.](../media/46b6e007-9741-44af-8517-6f682e0ac974.png)
  
2. <span data-ttu-id="48b92-130">Dans la **fenêtre Domaines et trusts Active Directory,** cliquez avec le bouton droit sur Domaines et **trusts Active Directory,** puis choisissez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="48b92-130">In the **Active Directory Domains and Trusts** window, right-click **Active Directory Domains and Trusts**, and then choose **Properties**.</span></span>
    
    ![Cliquez avec le bouton droit sur Domaines et trusts Active Directory et choisissez Propriétés](../media/39d20812-ffb5-4ba9-8d7b-477377ac360d.png)
  
3. <span data-ttu-id="48b92-132">Sous **l’onglet Suffixes UPN,** dans la zone Autres **suffixes UPN,** tapez votre  nouveau suffixe UPN ou suffixes, puis choisissez Ajouter \> **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="48b92-132">On the **UPN Suffixes** tab, in the **Alternative UPN Suffixes** box, type your new UPN suffix or suffixes, and then choose **Add** \> **Apply**.</span></span>
    
    ![Ajouter un nouveau suffixe UPN](../media/a4aaf919-7adf-469a-b93f-83ef284c0915.PNG)
  
    <span data-ttu-id="48b92-134">Choisissez **OK** lorsque vous avez terminé d’ajouter des suffixes.</span><span class="sxs-lookup"><span data-stu-id="48b92-134">Choose **OK** when you're done adding suffixes.</span></span> 
    
 #### <a name="step-2-change-the-upn-suffix-for-existing-users"></a><span data-ttu-id="48b92-135">Étape 2 : Modifier le suffixe UPN pour les utilisateurs existants</span><span class="sxs-lookup"><span data-stu-id="48b92-135">Step 2: Change the UPN suffix for existing users</span></span>
  
1. <span data-ttu-id="48b92-136">Sur le contrôleur de domaine AD DS, dans le Gestionnaire de serveur, choisissez **Outils** Utilisateurs \> **et ordinateurs Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="48b92-136">On the AD DS domain controller, in the Server Manager choose **Tools** \> **Active Directory Users and Computers**.</span></span>
    
    <span data-ttu-id="48b92-137">**Ou, si vous n’avez pas Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48b92-137">**Or, if you don't have Windows Server 2012**</span></span>
    
    <span data-ttu-id="48b92-138">Appuyez sur la touche  Windows + **R** pour ouvrir la boîte de dialogue Exécuter, puis tapez Dsa.msc, puis cliquez sur **OK**</span><span class="sxs-lookup"><span data-stu-id="48b92-138">Press **Windows key + R** to open the **Run** dialog, and then type in Dsa.msc, and then click **OK**</span></span>
    
2. <span data-ttu-id="48b92-139">Sélectionnez un utilisateur, cliquez avec le bouton droit, puis choisissez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="48b92-139">Select a user, right-click, and then choose **Properties**.</span></span>
    
3. <span data-ttu-id="48b92-140">Sous **l’onglet** Compte, dans la liste de listes des suffixes UPN, choisissez le nouveau suffixe UPN, puis **choisissez OK.**</span><span class="sxs-lookup"><span data-stu-id="48b92-140">On the **Account** tab, in the UPN suffix drop-down list, choose the new UPN suffix, and then choose **OK**.</span></span>
    
    ![Ajouter un nouveau suffixe UPN pour un utilisateur](../media/54876751-49f0-48cc-b864-2623c4835563.png)
  
4. <span data-ttu-id="48b92-142">Effectuer ces étapes pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48b92-142">Complete these steps for every user.</span></span>
    
   
### <a name="use-powershell-to-change-the-upn-suffix-for-all-of-your-users"></a><span data-ttu-id="48b92-143">Utiliser PowerShell pour modifier le suffixe UPN de tous vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="48b92-143">Use PowerShell to change the UPN suffix for all of your users</span></span>

<span data-ttu-id="48b92-144">Si vous avez un grand nombre de comptes d’utilisateur à mettre à jour, il est plus facile d’utiliser PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48b92-144">If you have a lot of user accounts to update, it's easier to use PowerShell.</span></span> <span data-ttu-id="48b92-145">L’exemple suivant utilise les cmdlets [Get-ADUser](https://go.microsoft.com/fwlink/p/?LinkId=624312) et [Set-ADUser](https://go.microsoft.com/fwlink/p/?LinkId=624313) pour modifier tous les suffixes contoso.local en contoso.com dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="48b92-145">The following example uses the cmdlets [Get-ADUser](https://go.microsoft.com/fwlink/p/?LinkId=624312) and [Set-ADUser](https://go.microsoft.com/fwlink/p/?LinkId=624313) to change all contoso.local suffixes to contoso.com in AD DS.</span></span> 

<span data-ttu-id="48b92-146">Par exemple, vous pouvez exécuter les commandes PowerShell suivantes pour mettre à jour tous les suffixes contoso.local contoso.com :</span><span class="sxs-lookup"><span data-stu-id="48b92-146">For example, you could run the following PowerShell commands to update all contoso.local suffixes to contoso.com:</span></span>
    
  ```powershell
  $LocalUsers = Get-ADUser -Filter "UserPrincipalName -like '*contoso.local'" -Properties userPrincipalName -ResultSetSize $null
  $LocalUsers | foreach {$newUpn = $_.UserPrincipalName.Replace("@contoso.local","@contoso.com"); $_ | Set-ADUser -UserPrincipalName $newUpn}
  ```

<span data-ttu-id="48b92-147">Consultez [le module Windows PowerShell Active Directory](https://go.microsoft.com/fwlink/p/?LinkId=624314) pour en savoir plus sur l Windows PowerShell dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="48b92-147">See [Active Directory Windows PowerShell module](https://go.microsoft.com/fwlink/p/?LinkId=624314) to learn more about using Windows PowerShell in AD DS.</span></span> 

