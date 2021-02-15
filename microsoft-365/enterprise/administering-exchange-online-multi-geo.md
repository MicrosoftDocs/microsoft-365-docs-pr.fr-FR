---
title: Administration des boîtes aux lettres Exchange Online dans un environnement multigéographique
ms.reviewer: adwood
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: o365-solutions
f1.keywords:
- NOCSH
ms.custom: seo-marvel-mar2020
localization_priority: normal
description: Découvrez comment administrer les paramètres Multi-Géo d’Exchange Online dans votre environnement Microsoft 365 avec PowerShell.
ms.openlocfilehash: 63eb1957611fd57e216012435188a6ddd1b232d3
ms.sourcegitcommit: 38d828ae8d4350ae774a939c8decf30cb36c3bea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49552006"
---
# <a name="administering-exchange-online-mailboxes-in-a-multi-geo-environment"></a><span data-ttu-id="e119a-103">Administration des boîtes aux lettres Exchange Online dans un environnement multigéographique</span><span class="sxs-lookup"><span data-stu-id="e119a-103">Administering Exchange Online mailboxes in a multi-geo environment</span></span>

<span data-ttu-id="e119a-104">Exchange Online PowerShell est requis pour afficher et configurer les propriétés multigéotiques dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e119a-104">Exchange Online PowerShell is required to view and configure multi geo properties in your Microsoft 365 environment.</span></span> <span data-ttu-id="e119a-105">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="e119a-105">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="e119a-106">Pour voir la propriété **PreferredDataLocation** sur les objets utilisateur, vous devez disposer du [module PowerShell Microsoft Azure Active Directory](https://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) v1.1.166.0 ou version v1.x ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e119a-106">You need the [Microsoft Azure Active Directory PowerShell Module](https://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) v1.1.166.0 or later in v1.x to see the **PreferredDataLocation** property on user objects.</span></span> <span data-ttu-id="e119a-107">La valeur **PreferredDataLocation** des objets utilisateur synchronisés via AAD Connect dans AAD ne peut pas être modifiée directement via AAD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e119a-107">User objects synchronized via AAD Connect into AAD cannot have their **PreferredDataLocation** value directly modified via AAD PowerShell.</span></span> <span data-ttu-id="e119a-108">Les objets utilisateur cloud uniquement peuvent être modifiés via AAD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e119a-108">Cloud-only user objects can be modified via AAD PowerShell.</span></span> <span data-ttu-id="e119a-109">Pour vous connecter à Azure AD PowerShell, voir [Se connecter à PowerShell](connect-to-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="e119a-109">To connect to Azure AD PowerShell, see [Connect to PowerShell](connect-to-microsoft-365-powershell.md).</span></span>

## <a name="connect-directly-to-a-geo-location-using-exchange-online-powershell"></a><span data-ttu-id="e119a-110">Se connecter directement à un emplacement géographique à l’aide d’Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="e119a-110">Connect directly to a geo location using Exchange Online PowerShell</span></span>

<span data-ttu-id="e119a-111">En règle générale, Exchange Online PowerShell se connecte à l’emplacement géographique central.</span><span class="sxs-lookup"><span data-stu-id="e119a-111">Typically, Exchange Online PowerShell will connect to the central geo location.</span></span> <span data-ttu-id="e119a-112">Vous pouvez cependant aussi vous connecter directement à des emplacements satellites géographiques.</span><span class="sxs-lookup"><span data-stu-id="e119a-112">But, you can also connect directly to satellite geo locations.</span></span> <span data-ttu-id="e119a-113">En raison des améliorations apportées aux performances, nous vous recommandons de vous connecter directement à l’emplacement satellite géographique lorsque vous gérez uniquement des utilisateurs situés dans cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="e119a-113">Because of performance improvements, we recommend connecting directly to the satellite geo location when you only manage users in that location.</span></span>

<span data-ttu-id="e119a-114">Les conditions requises pour l’installation et l’utilisation du module EXO V2 sont décrites dans [Installer et gérer le module EXO V2](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exo-v2-module).</span><span class="sxs-lookup"><span data-stu-id="e119a-114">The requirements for installing and using the EXO V2 module are described in [Install and maintain the EXO V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exo-v2-module).</span></span>

<span data-ttu-id="e119a-115">Pour connecter Exchange Online PowerShell à un emplacement géographique spécifique, le paramètre *ConnectionUri* est différent des instructions de connexion normales.</span><span class="sxs-lookup"><span data-stu-id="e119a-115">To connect Exchange Online PowerShell to a specific geo location, the *ConnectionUri* parameter is different than the regular connection instructions.</span></span> <span data-ttu-id="e119a-116">Les autres commandes et valeurs sont identiques.</span><span class="sxs-lookup"><span data-stu-id="e119a-116">The rest of the commands and values are the same.</span></span>

<span data-ttu-id="e119a-117">Plus précisément, vous devez ajouter la `?email=<emailaddress>` valeur à la fin de la valeur _ConnectionUri._</span><span class="sxs-lookup"><span data-stu-id="e119a-117">Specifically, you need to add the `?email=<emailaddress>` value to end of the _ConnectionUri_ value.</span></span> <span data-ttu-id="e119a-118">`<emailaddress>` est l’adresse e-mail **d’une boîte** aux lettres dans l’emplacement géographique cible.</span><span class="sxs-lookup"><span data-stu-id="e119a-118">`<emailaddress>` is the email address of **any** mailbox in the target geo location.</span></span> <span data-ttu-id="e119a-119">Vos autorisations sur cette boîte aux lettres ou la relation avec vos informations d’identification ne sont pas un facteur . l’adresse e-mail indique simplement à Exchange Online PowerShell où se connecter.</span><span class="sxs-lookup"><span data-stu-id="e119a-119">Your permissions to that mailbox or the relationship to your credentials are not a factor; the email address simply tells Exchange Online PowerShell where to connect.</span></span>

<span data-ttu-id="e119a-120">Les clients Microsoft 365 ou Microsoft 365 GCC n’ont généralement pas besoin d’utiliser le paramètre _ConnectionUri_ pour se connecter à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e119a-120">Microsoft 365 or Microsoft 365 GCC customers typically don't need to use the _ConnectionUri_ parameter to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="e119a-121">Toutefois, pour vous connecter à un emplacement géographique spécifique, vous devez utiliser le paramètre _ConnectionUri_ afin de pouvoir `?email=<emailaddress>` l’utiliser dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="e119a-121">But, to connect to a specific geo location, you do need to use _ConnectionUri_ parameter so you can use `?email=<emailaddress>` in the value.</span></span>

### <a name="connect-to-a-geo-location-in-exchange-online-powershell"></a><span data-ttu-id="e119a-122">Se connecter à un emplacement géographique dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="e119a-122">Connect to a geo location in Exchange Online PowerShell</span></span>

<span data-ttu-id="e119a-123">Les instructions de connexion suivantes fonctionnent pour les comptes qui sont ou ne sont pas configurés pour l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="e119a-123">The following connection instructions work for accounts that are or aren't configured for multi-factor authentication (MFA).</span></span>

1. <span data-ttu-id="e119a-124">Dans une fenêtre Windows PowerShell, chargez le module EXO V2 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e119a-124">In a Windows PowerShell window, load the EXO V2 module by running the following command:</span></span>

   ```powershell
   Import-Module ExchangeOnlineManagement
   ```

2. <span data-ttu-id="e119a-125">Dans l’exemple suivant, admin@contoso.onmicrosoft.com est le compte d’administrateur et l’emplacement géographique cible est l’emplacement olga@contoso.onmicrosoft.com boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e119a-125">In the following example, admin@contoso.onmicrosoft.com is the admin account, and the target geo location is where the mailbox olga@contoso.onmicrosoft.com resides.</span></span>

   ```powershell
   Connect-ExchangeOnline -UserPrincipalName admin@contoso.onmicrosoft.com -ConnectionUri https://outlook.office365.com/powershell?email=olga@contoso.onmicrosoft.com
   ```

3. <span data-ttu-id="e119a-126">Entrez le mot de passe du admin@contoso.onmicrosoft.com dans l’invite qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e119a-126">Enter the password for the admin@contoso.onmicrosoft.com in the prompt that appears.</span></span> <span data-ttu-id="e119a-127">Si le compte est configuré pour l’mffa, vous devez également entrer le code de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e119a-127">If the account is configured for MFA, you also need to enter the security code.</span></span>

## <a name="view-the-available-geo-locations-that-are-configured-in-your-exchange-online-organization"></a><span data-ttu-id="e119a-128">Affichage des emplacements géographiques disponibles configurés dans votre organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e119a-128">View the available geo locations that are configured in your Exchange Online organization</span></span>

<span data-ttu-id="e119a-129">Pour afficher la liste des emplacements géographiques configurés dans Microsoft 365 Multi-Geo, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="e119a-129">To see the list of configured geo locations in Microsoft 365 Multi-Geo, run the following command in Exchange Online PowerShell:</span></span>

```powershell
Get-OrganizationConfig | Select -ExpandProperty AllowedMailboxRegions | Format-Table
```

## <a name="view-the-central-geo-location-for-your-exchange-online-organization"></a><span data-ttu-id="e119a-130">Afficher l’emplacement géographique central de votre organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e119a-130">View the central geo location for your Exchange Online organization</span></span>

<span data-ttu-id="e119a-131">Pour afficher l’emplacement géographique central de votre locataire, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="e119a-131">To view your tenant's central geo location, run the following command in Exchange Online PowerShell:</span></span>

```powershell
Get-OrganizationConfig | Select DefaultMailboxRegion
```

## <a name="find-the-geo-location-of-a-mailbox"></a><span data-ttu-id="e119a-132">Recherche de l’emplacement géographique d’une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="e119a-132">Find the geo location of a mailbox</span></span>

<span data-ttu-id="e119a-133">La cmdlet **Get-Mailbox** dans Exchange Online PowerShell affiche les propriétés multigéographiques associées suivantes sur les boîtes aux lettres :</span><span class="sxs-lookup"><span data-stu-id="e119a-133">The **Get-Mailbox** cmdlet in Exchange Online PowerShell displays the following multi-geo related properties on mailboxes:</span></span>

- <span data-ttu-id="e119a-134">**Database** : les 3 premières lettres du nom de base de données correspondent au géocode indiquant où la boîte aux lettres se trouve actuellement.</span><span class="sxs-lookup"><span data-stu-id="e119a-134">**Database**: The first 3 letters of the database name correspond to the geo code, which tells you where the mailbox is currently located.</span></span> <span data-ttu-id="e119a-135">Pour les boîtes aux lettres d’archivage en ligne, il convient d’utiliser la propriété **ArchiveDatabase**.</span><span class="sxs-lookup"><span data-stu-id="e119a-135">For Online Archive Mailboxes the **ArchiveDatabase** property should be used.</span></span>

- <span data-ttu-id="e119a-136">**MailboxRegion** : spécifie le code de géolocalisation défini par l’administrateur (synchronisé à partir de **PreferredDataLocation** dans Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e119a-136">**MailboxRegion**: Specifies the geo location code that was set by the admin (synchronized from **PreferredDataLocation** in Azure AD).</span></span>

- <span data-ttu-id="e119a-137">**MailboxRegionLastUpdateTime** : indique quand la propriété MailboxRegion a été mise à jour (automatiquement ou manuellement) pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="e119a-137">**MailboxRegionLastUpdateTime**: Indicates when MailboxRegion was last updated (either automatically or manually).</span></span>

<span data-ttu-id="e119a-138">Pour afficher ces propriétés pour une boîte aux lettres, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="e119a-138">To see these properties for a mailbox, use the following syntax:</span></span>

```powershell
Get-Mailbox -Identity <MailboxIdentity> | Format-List Database,MailboxRegion*
```

<span data-ttu-id="e119a-139">Par exemple, pour afficher les informations d’emplacement géographique pour la boîte aux lettres chris@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e119a-139">For example, to see the geo location information for the mailbox chris@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Get-Mailbox -Identity chris@contoso.onmicrosoft.com | Format-List Database, MailboxRegion*
```

<span data-ttu-id="e119a-140">Le résultat de la commande ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="e119a-140">The output of the command looks like this:</span></span>

```powershell
Database                    : EURPR03DG077-db007
MailboxRegion               : EUR
MailboxRegionLastUpdateTime : 2/6/2018 8:21:01 PM
```

> [!NOTE]
> <span data-ttu-id="e119a-141">Si le code d’emplacement géographique dans le nom de la base de données ne correspond pas à la valeur **MailboxRegion,** la boîte aux lettres est automatiquement mise dans une file d’attente de déplacement et déplacée vers l’emplacement géographique spécifié par la valeur **MailboxRegion** (Exchange Online recherche une in correspondance entre ces valeurs de propriété).</span><span class="sxs-lookup"><span data-stu-id="e119a-141">If the geo location code in the database name doesn't match **MailboxRegion** value, the mailbox will be automatically be put into a relocation queue and moved to the geo location specified by the **MailboxRegion** value (Exchange Online looks for a mismatch between these property values).</span></span>

## <a name="move-an-existing-cloud-only-mailbox-to-a-specific-geo-location"></a><span data-ttu-id="e119a-142">Déplacer une boîte aux lettres cloud uniquement vers un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="e119a-142">Move an existing cloud-only mailbox to a specific geo location</span></span>

<span data-ttu-id="e119a-143">Un utilisateur cloud uniquement est un utilisateur qui n’est pas synchronisé avec le locataire via AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="e119a-143">A cloud-only user is a user not synchronized to the tenant via AAD Connect.</span></span> <span data-ttu-id="e119a-144">Cet utilisateur a été créé directement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e119a-144">This user was created directly in Azure AD.</span></span> <span data-ttu-id="e119a-145">Pour afficher ou spécifier la zone géographique dans laquelle sera stockée la boîte aux lettres d’un utilisateur cloud uniquement, utilisez les cmdlets **Get-MsolUser** et **Set-MsolUser** dans le module Azure AD pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e119a-145">Use the **Get-MsolUser** and **Set-MsolUser** cmdlets in the Azure AD Module for Windows PowerShell to view or specify the geo location where a cloud-only user's mailbox will be stored.</span></span>

<span data-ttu-id="e119a-146">Pour voir la valeur **PreferredDataLocation** pour un utilisateur, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="e119a-146">To view the **PreferredDataLocation** value for a user, use this syntax in Azure AD PowerShell:</span></span>

```powershell
Get-MsolUser -UserPrincipalName <UserPrincipalName> | Format-List UserPrincipalName,PreferredDataLocation
```

<span data-ttu-id="e119a-147">Par exemple, pour voir la valeur **PreferredDataLocation** pour l’utilisateur michelle@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e119a-147">For example, to see the **PreferredDataLocation** value for the user michelle@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Get-MsolUser -UserPrincipalName michelle@contoso.onmicrosoft.com | Format-List
```

<span data-ttu-id="e119a-148">Pour modifier la valeur **PreferredDataLocation** d’un objet utilisateur cloud uniquement, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="e119a-148">To modify the **PreferredDataLocation** value for a cloud-only user object, use the following syntax in Azure AD PowerShell:</span></span>

```powershell
Set-MsolUser -UserPrincipalName <UserPrincipalName> -PreferredDataLocation <GeoLocationCode>
```

<span data-ttu-id="e119a-149">Par exemple, pour définir la valeur **PreferredDataLocation** sur la zone géographique Union européenne (EUR) pour l’utilisateur michelle@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e119a-149">For example, to set the **PreferredDataLocation** value to the European Union (EUR) geo for the user michelle@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Set-MsolUser -UserPrincipalName michelle@contoso.onmicrosoft.com -PreferredDataLocation EUR
```

> [!NOTE]
>
> - <span data-ttu-id="e119a-150">Comme mentionné précédemment, vous ne pouvez pas utiliser cette procédure pour les objets utilisateur synchronisés à partir d’Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="e119a-150">As mentioned previously, you cannot use this procedure for synchronized user objects from on-premises Active Directory.</span></span> <span data-ttu-id="e119a-151">Vous devez modifier la valeur **PreferredDataLocation** dans Active Directory et la synchroniser à l’aide d’AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="e119a-151">You need to change the **PreferredDataLocation** value in Active Directory and synchronize it using AAD Connect.</span></span> <span data-ttu-id="e119a-152">Pour plus d’informations, voir [Synchronisation Azure Active Directory Connect : Configurer un emplacement de données par défaut pour les ressources Microsoft 365](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-preferreddatalocation).</span><span class="sxs-lookup"><span data-stu-id="e119a-152">For more information, see [Azure Active Directory Connect sync: Configure preferred data location for Microsoft 365 resources](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-preferreddatalocation).</span></span>
>
> - <span data-ttu-id="e119a-153">Le temps nécessaire pour déplacer une boîte aux lettres vers un nouvel emplacement géographique dépend de plusieurs facteurs :</span><span class="sxs-lookup"><span data-stu-id="e119a-153">How long it takes to relocate a mailbox to a new geo location depends on several factors:</span></span>
>
>   - <span data-ttu-id="e119a-154">la taille et le type de boîte aux lettres ;</span><span class="sxs-lookup"><span data-stu-id="e119a-154">The size and type of mailbox.</span></span>
>   - <span data-ttu-id="e119a-155">le nombre total de boîtes aux lettres déplacées ;</span><span class="sxs-lookup"><span data-stu-id="e119a-155">The number of mailboxes being moved.</span></span>
>   - <span data-ttu-id="e119a-156">la disponibilité des ressources nécessaires pour le déplacement.</span><span class="sxs-lookup"><span data-stu-id="e119a-156">The availability of move resources.</span></span>

### <a name="move-an-inactive-mailbox-to-a-specific-geo"></a><span data-ttu-id="e119a-157">Déplacer une boîte aux lettres inactive vers une géo spécifique</span><span class="sxs-lookup"><span data-stu-id="e119a-157">Move an inactive mailbox to a specific geo</span></span>

<span data-ttu-id="e119a-158">Vous ne pouvez pas déplacer les boîtes aux lettres inactives qui sont conservées à des fins de conformité (par exemple, les boîtes aux lettres en conservation pour litige) en modifiant leur valeur **PreferredDataLocation.**</span><span class="sxs-lookup"><span data-stu-id="e119a-158">You can't move inactive mailboxes that are preserved for compliance purposes (for example, mailboxes on Litigation Hold) by changing their **PreferredDataLocation** value.</span></span> <span data-ttu-id="e119a-159">Pour déplacer une boîte aux lettres inactive vers une autre géo, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e119a-159">To move an inactive mailbox to a different geo, do the following steps:</span></span>

1. <span data-ttu-id="e119a-160">Récupérez la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="e119a-160">Recover the inactive mailbox.</span></span> <span data-ttu-id="e119a-161">Pour obtenir des instructions, [voir Récupérer une boîte aux lettres inactive.](https://docs.microsoft.com/microsoft-365/compliance/recover-an-inactive-mailbox)</span><span class="sxs-lookup"><span data-stu-id="e119a-161">For instructions, see [Recover an inactive mailbox](https://docs.microsoft.com/microsoft-365/compliance/recover-an-inactive-mailbox).</span></span>

2. <span data-ttu-id="e119a-162">Empêchez l’Assistant Dossier géré de traiter la boîte aux lettres récupérée en remplaçant par le nom, l’alias, le compte ou l’adresse e-mail de la boîte aux lettres et en exécutant la commande suivante dans \<MailboxIdentity\> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="e119a-162">Prevent the Managed Folder Assistant from processing the recovered mailbox by replacing \<MailboxIdentity\> with the name, alias, account, or email address of the mailbox and running the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell):</span></span>

    ```powershell
    Set-Mailbox <MailboxIdentity> -ElcProcessingDisabled $true
    ```

3. <span data-ttu-id="e119a-163">Attribuez une **licence Exchange Online Plan 2** à la boîte aux lettres récupérée.</span><span class="sxs-lookup"><span data-stu-id="e119a-163">Assign an **Exchange Online Plan 2** license to the recovered mailbox.</span></span> <span data-ttu-id="e119a-164">Cette étape est nécessaire pour remettre la boîte aux lettres en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="e119a-164">This step is required to place the mailbox back on Litigation Hold.</span></span> <span data-ttu-id="e119a-165">Pour obtenir des instructions, voir [Attribuer des licences aux utilisateurs.](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users)</span><span class="sxs-lookup"><span data-stu-id="e119a-165">For instructions, see [Assign licenses to users](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users).</span></span>

4. <span data-ttu-id="e119a-166">Configurez la **valeur PreferredDataLocation** sur la boîte aux lettres comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="e119a-166">Configure the **PreferredDataLocation** value on the mailbox as described in the previous section.</span></span>

5. <span data-ttu-id="e119a-167">Une fois que vous avez confirmé que la boîte aux lettres a été déplacée vers le nouvel emplacement géographique, placez de nouveau la boîte aux lettres récupérée en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="e119a-167">After you've confirmed that the mailbox has moved to the new geo location, place the recovered mailbox back on Litigation Hold.</span></span> <span data-ttu-id="e119a-168">Pour plus d’instructions, [voir Placer une boîte aux lettres en attente pour litige.](https://docs.microsoft.com/microsoft-365/compliance/create-a-litigation-hold#place-a-mailbox-on-litigation-hold)</span><span class="sxs-lookup"><span data-stu-id="e119a-168">For instructions, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/microsoft-365/compliance/create-a-litigation-hold#place-a-mailbox-on-litigation-hold).</span></span>

6. <span data-ttu-id="e119a-169">Après avoir vérifié que la mise en attente pour litige est en place, autorisez l’Assistant Dossier géré à traiter à nouveau la boîte aux lettres en remplaçant par le nom, l’alias, le compte ou l’adresse e-mail de la boîte aux lettres et en exécutant la commande suivante dans \<MailboxIdentity\> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="e119a-169">After verifying that the Litigation Hold is in place, allow the Managed Folder Assistant to process the mailbox again by replacing \<MailboxIdentity\> with the name, alias, account, or email address of the mailbox and running the following command in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell):</span></span>

    ```powershell
    Set-Mailbox <MailboxIdentity> -ElcProcessingDisabled $false
    ```

7. <span data-ttu-id="e119a-170">Rendez la boîte aux lettres inactive en supprimant le compte d’utilisateur associé à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e119a-170">Make the mailbox inactive again by removing the user account that's associated with the mailbox.</span></span> <span data-ttu-id="e119a-171">Pour obtenir des instructions, [voir Supprimer un utilisateur de votre organisation.](https://docs.microsoft.com/microsoft-365/admin/add-users/delete-a-user)</span><span class="sxs-lookup"><span data-stu-id="e119a-171">For instructions, see [Delete a user from your organization](https://docs.microsoft.com/microsoft-365/admin/add-users/delete-a-user).</span></span> <span data-ttu-id="e119a-172">Cette étape libère également la licence Exchange Online Plan 2 pour d’autres utilisations.</span><span class="sxs-lookup"><span data-stu-id="e119a-172">This step also releases the Exchange Online Plan 2 license for other uses.</span></span>

<span data-ttu-id="e119a-173">**Remarque**: lorsque vous déplacez une boîte aux lettres inactive vers un autre emplacement géographique, vous pouvez affecter les résultats de recherche de contenu ou la possibilité de rechercher la boîte aux lettres à partir de l’ancien emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="e119a-173">**Note**: When you move an inactive mailbox to a different geo location, you might affect content search results or the ability to search the mailbox from the former geo location.</span></span> <span data-ttu-id="e119a-174">Pour plus d’informations, [voir Recherche et exportation de contenu dans des environnements multigéo géographiques.](https://docs.microsoft.com/microsoft-365/compliance/set-up-compliance-boundaries#searching-and-exporting-content-in-multi-geo-environments)</span><span class="sxs-lookup"><span data-stu-id="e119a-174">For more information, see [Searching and exporting content in Multi-Geo environments](https://docs.microsoft.com/microsoft-365/compliance/set-up-compliance-boundaries#searching-and-exporting-content-in-multi-geo-environments).</span></span>

## <a name="create-new-cloud-mailboxes-in-a-specific-geo-location"></a><span data-ttu-id="e119a-175">Créer des boîtes aux lettres cloud dans un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="e119a-175">Create new cloud mailboxes in a specific geo location</span></span>

<span data-ttu-id="e119a-176">Pour créer une boîte aux lettres dans un emplacement géographique spécifique, vous devez effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e119a-176">To create a new mailbox in a specific geo location, you need to do either of these steps:</span></span>

- <span data-ttu-id="e119a-177">Configurez la valeur **PreferredDataLocation** comme décrit dans la [section](#move-an-existing-cloud-only-mailbox-to-a-specific-geo-location) Précédente Déplacer une boîte aux lettres cloud existante uniquement vers une *section* d’emplacement géographique spécifique avant de créer la boîte aux lettres dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e119a-177">Configure the **PreferredDataLocation** value as described in the previous [Move an existing cloud-only mailbox to a specific geo location](#move-an-existing-cloud-only-mailbox-to-a-specific-geo-location) section *before* you create the mailbox in Exchange Online.</span></span> <span data-ttu-id="e119a-178">Par exemple, configurez la **valeur PreferredDataLocation** sur un utilisateur avant d’attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="e119a-178">For example, configure the **PreferredDataLocation** value on a user before you assign a license.</span></span>

- <span data-ttu-id="e119a-179">Attribuer une licence lors de la définition de la valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="e119a-179">Assign a license at the same time you set the **PreferredDataLocation** value.</span></span>

<span data-ttu-id="e119a-180">Pour créer un utilisateur titulaire d’une licence d’utilisation cloud uniquement (non synchronisé avec AAD Connect) dans une zone géographique spécifique, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="e119a-180">To create a new cloud-only licensed user (not AAD Connect synchronized) in a specific geo location, use the following syntax in Azure AD PowerShell:</span></span>

```powershell
New-MsolUser -UserPrincipalName <UserPrincipalName> -DisplayName "<Display Name>" [-FirstName <FirstName>] [-LastName <LastName>] [-Password <Password>] [-LicenseAssignment <AccountSkuId>] -PreferredDataLocation <GeoLocationCode>
```

<span data-ttu-id="e119a-181">Cet exemple montre comment créer un compte d’utilisateur pour Elizabeth Brunner avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e119a-181">This example create a new user account for Elizabeth Brunner with the following values:</span></span>

- <span data-ttu-id="e119a-182">Nom d’utilisateur principal : ebrunner@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="e119a-182">User principal name: ebrunner@contoso.onmicrosoft.com</span></span>
- <span data-ttu-id="e119a-183">Prénom : Elizabeth</span><span class="sxs-lookup"><span data-stu-id="e119a-183">First name: Elizabeth</span></span>
- <span data-ttu-id="e119a-184">Nom : Brunner</span><span class="sxs-lookup"><span data-stu-id="e119a-184">Last name: Brunner</span></span>
- <span data-ttu-id="e119a-185">Nom d’affichage : Elizabeth Brunner</span><span class="sxs-lookup"><span data-stu-id="e119a-185">Display name: Elizabeth Brunner</span></span>
- <span data-ttu-id="e119a-186">Mot de passe : généré de façon aléatoire et affiché dans les résultats de la commande (étant donné que nous n’utilisons pas le paramètre *Password*)</span><span class="sxs-lookup"><span data-stu-id="e119a-186">Password: randomly-generated and shown in the results of the command (because we're not using the *Password* parameter)</span></span>
- <span data-ttu-id="e119a-187">Licence : `contoso:ENTERPRISEPREMIUM` (E5)</span><span class="sxs-lookup"><span data-stu-id="e119a-187">License: `contoso:ENTERPRISEPREMIUM` (E5)</span></span>
- <span data-ttu-id="e119a-188">Emplacement : Australie (AUS)</span><span class="sxs-lookup"><span data-stu-id="e119a-188">Location: Australia (AUS)</span></span>

```powershell
New-MsolUser -UserPrincipalName ebrunner@contoso.onmicrosoft.com -DisplayName "Elizabeth Brunner" -FirstName Elizabeth -LastName Brunner -LicenseAssignment contoso:ENTERPRISEPREMIUM -PreferredDataLocation AUS
```

<span data-ttu-id="e119a-189">Pour plus d’informations sur la création de comptes d’utilisateur et la recherche de valeurs LicenseAssignment dans Azure AD PowerShell, voir [Création de comptes d’utilisateurs avec PowerShell](create-user-accounts-with-microsoft-365-powershell.md) et [Afficher les licences et les services avec PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="e119a-189">For more information about creating new user accounts and finding LicenseAssignment values in Azure AD PowerShell, see [Create user accounts with PowerShell](create-user-accounts-with-microsoft-365-powershell.md) and [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e119a-190">Sii vous utilisez Exchange Online PowerShell pour activer une boîte aux lettres et avez besoin que la boîte aux lettres soit créée directement dans la zone géographique spécifiée dans **PreferredDataLocation**, vous devez utiliser une cmdlet Exchange Online telle que **Enable-Mailbox** ou **New-Mailbox** directement sur le service cloud.</span><span class="sxs-lookup"><span data-stu-id="e119a-190">If you are using Exchange Online PowerShell to enable a mailbox and need the mailbox to be created directly in the geo location that's specified in **PreferredDataLocation**, you need to use an Exchange Online cmdlet such as **Enable-Mailbox** or **New-Mailbox** directly against the cloud service.</span></span> <span data-ttu-id="e119a-191">Si vous utilisez la cmdlet **Enable-RemoteMailbox** dans le powerShell Exchange sur site, la boîte aux lettres est créée dans l’emplacement géographique central.</span><span class="sxs-lookup"><span data-stu-id="e119a-191">If you use the **Enable-RemoteMailbox** cmdlet in on-premises Exchange PowerShell, the mailbox will be created in the central geo location.</span></span>

## <a name="onboard-existing-on-premises-mailboxes-in-a-specific-geo-location"></a><span data-ttu-id="e119a-192">Intégrer des boîtes aux lettres locales existant dans un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="e119a-192">Onboard existing on-premises mailboxes in a specific geo location</span></span>

<span data-ttu-id="e119a-193">Vous pouvez vous servir des outils et processus d’intégration standard pour migrer une boîte aux lettres d’une organisation Exchange locale vers Exchange Online. Ces outils sont le [Tableau de bord de migration dans le Centre d’administration Exchange](https://support.office.com/article/d164b35c-f624-4f83-ac58-b7cae96ab331) et la cmdlet [New-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/new-migrationbatch) dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e119a-193">You can use the standard onboarding tools and processes to migrate a mailbox from an on-premises Exchange organization to Exchange Online, including the [Migration dashboard in the EAC](https://support.office.com/article/d164b35c-f624-4f83-ac58-b7cae96ab331), and the [New-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/new-migrationbatch) cmdlet in Exchange Online PowerShell.</span></span>

<span data-ttu-id="e119a-194">La première étape consiste à vérifier qu’un objet utilisateur existe pour chaque boîte aux lettres à intégrer, et que la valeur **PreferredDataLocation** correcte est configurée dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e119a-194">The first step is to verify a user object exists for each mailbox to be onboarded, and verify the correct **PreferredDataLocation** value is configured in Azure AD.</span></span> <span data-ttu-id="e119a-195">Les outils d’intégration respectent la valeur **PreferredDataLocation** et migrent les boîtes aux lettres directement vers la zone géographique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e119a-195">The onboarding tools will respect the **PreferredDataLocation** value and will migrate the mailboxes directly to the specified geo location.</span></span>

<span data-ttu-id="e119a-196">Ou bien, pour intégrer les boîtes aux lettres directement dans un emplacement géographique à l’aide de la cmdlet [New-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/new-moverequest) dans Exchange Online PowerShell, vous pouvez également procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="e119a-196">Or, you can use the following steps to onboard mailboxes directly in a specific geo location using the [New-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/new-moverequest) cmdlet in Exchange Online PowerShell.</span></span>

1. <span data-ttu-id="e119a-197">Vérifiez que l’objet utilisateur existe pour chaque boîte aux lettres intégrée et que la valeur **PreferredDataLocation** est correctement définie dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e119a-197">Verify the user object exists for each mailbox to be onboarded and that **PreferredDataLocation** is set to the desired value in Azure AD.</span></span> <span data-ttu-id="e119a-198">La valeur **PreferredDataLocation** est synchronisée avec l’attribut **MailboxRegion** de l’objet utilisateur de courrier correspondant dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e119a-198">The value of **PreferredDataLocation** will be synchronized to the **MailboxRegion** attribute of the corresponding mail user object in Exchange Online.</span></span>

2. <span data-ttu-id="e119a-199">Connectez-vous directement à la zone géographique satellite spécifique en suivant les instructions de connexion figurant plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e119a-199">Connect directly to the specific satellite geo location using the connection instructions from earlier in this topic.</span></span>

3. <span data-ttu-id="e119a-200">Dans Exchange Online PowerShell, stockez les informations d’identification d’administrateur locales utilisées pour effectuer une migration de boîte aux lettres dans une variable en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e119a-200">In Exchange Online PowerShell, store the on-premises administrator credentials that's used to perform a mailbox migration in a variable by running the following command:</span></span>

   ```powershell
   $RC = Get-Credential
   ```

4. <span data-ttu-id="e119a-201">Dans Exchange Online PowerShell, créez une cmdlet **New-MoveRequest** similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e119a-201">In Exchange Online PowerShell, create a new **New-MoveRequest** similar to the following example:</span></span>

   ```powershell
   New-MoveRequest -Remote -RemoteHostName mail.contoso.com -RemoteCredential $RC -Identity user@contoso.com -TargetDeliveryDomain <YourAppropriateDomain>
   ```

5. <span data-ttu-id="e119a-202">Répétez l’étape 4 pour chaque boîte aux lettres à migrer d’Exchange sur site vers l’emplacement géographique satellite auquel vous êtes actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="e119a-202">Repeat step #4 for every mailbox you need to migrate from on-premises Exchange to the satellite geo location you are currently connected to.</span></span>

6. <span data-ttu-id="e119a-203">Si vous devez migrer des boîtes aux lettres supplémentaires vers un autre emplacement géographique satellite, répétez les étapes 2 à 4 pour chaque emplacement spécifique.</span><span class="sxs-lookup"><span data-stu-id="e119a-203">If you need to migrate additional mailboxes to different satellite geo locations, repeat steps 2 through 4 for each specific location.</span></span>

## <a name="multi-geo-reporting"></a><span data-ttu-id="e119a-204">Génération de rapports multigéographiques</span><span class="sxs-lookup"><span data-stu-id="e119a-204">Multi-geo reporting</span></span>

<span data-ttu-id="e119a-205">Les **rapports d’utilisation multigéographique** dans le Centre d’administration Microsoft 365 affichent le nombre d’utilisateurs par emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="e119a-205">**Multi-Geo Usage Reports** in the Microsoft 365 admin center displays the user count by geo location.</span></span> <span data-ttu-id="e119a-206">Le rapport présente la répartition des utilisateurs pour le mois en cours et les données historiques des 6 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="e119a-206">The report displays user distribution for the current month and provides historical data for the past 6 months.</span></span>

## <a name="see-also"></a><span data-ttu-id="e119a-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e119a-207">See also</span></span>

[<span data-ttu-id="e119a-208">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="e119a-208">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
