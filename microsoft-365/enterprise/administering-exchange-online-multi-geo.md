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
description: Découvrez comment administrer les paramètres multi-géo Exchange Online dans votre environnement Microsoft 365 avec PowerShell.
ms.openlocfilehash: 645d48066ca02dbf3480e20ae30dc187f84293cf
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689613"
---
# <a name="administering-exchange-online-mailboxes-in-a-multi-geo-environment"></a><span data-ttu-id="749f6-103">Administration des boîtes aux lettres Exchange Online dans un environnement multigéographique</span><span class="sxs-lookup"><span data-stu-id="749f6-103">Administering Exchange Online mailboxes in a multi-geo environment</span></span>

<span data-ttu-id="749f6-104">Remote PowerShell est nécessaire pour afficher et configurer les propriétés multigéographiques dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="749f6-104">Remote PowerShell is required to view and configure multi geo properties in your Microsoft 365 environment.</span></span> <span data-ttu-id="749f6-105">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="749f6-105">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="749f6-106">Pour voir la propriété **PreferredDataLocation** sur les objets utilisateur, vous devez disposer du [module PowerShell Microsoft Azure Active Directory](https://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) v1.1.166.0 ou version v1.x ultérieure.</span><span class="sxs-lookup"><span data-stu-id="749f6-106">You need the [Microsoft Azure Active Directory PowerShell Module](https://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) v1.1.166.0 or later in v1.x to see the **PreferredDataLocation** property on user objects.</span></span> <span data-ttu-id="749f6-107">La valeur **PreferredDataLocation** des objets utilisateur synchronisés via AAD Connect dans AAD ne peut pas être modifiée directement via AAD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="749f6-107">User objects synchronized via AAD Connect into AAD cannot have their **PreferredDataLocation** value directly modified via AAD PowerShell.</span></span> <span data-ttu-id="749f6-108">Les objets utilisateur cloud uniquement peuvent être modifiés via AAD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="749f6-108">Cloud-only user objects can be modified via AAD PowerShell.</span></span> <span data-ttu-id="749f6-109">Pour vous connecter à Azure AD PowerShell, voir [Se connecter à PowerShell](connect-to-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="749f6-109">To connect to Azure AD PowerShell, see [Connect to PowerShell](connect-to-microsoft-365-powershell.md).</span></span>

## <a name="connect-directly-to-a-geo-location-using-exchange-online-powershell"></a><span data-ttu-id="749f6-110">Se connecter directement à un emplacement géographique à l’aide d’Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="749f6-110">Connect directly to a geo location using Exchange Online PowerShell</span></span>

<span data-ttu-id="749f6-111">En règle générale, Exchange Online PowerShell se connecte à l’emplacement géographique central.</span><span class="sxs-lookup"><span data-stu-id="749f6-111">Typically, Exchange Online PowerShell will connect to the central geo location.</span></span> <span data-ttu-id="749f6-112">Vous pouvez cependant aussi vous connecter directement à des emplacements satellites géographiques.</span><span class="sxs-lookup"><span data-stu-id="749f6-112">But, you can also connect directly to satellite geo locations.</span></span> <span data-ttu-id="749f6-113">En raison des améliorations apportées aux performances, nous vous recommandons de vous connecter directement à l’emplacement satellite géographique lorsque vous gérez uniquement des utilisateurs situés dans cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="749f6-113">Because of performance improvements, we recommend connecting directly to the satellite geo location when you only manage users in that location.</span></span>

<span data-ttu-id="749f6-114">Le paramètre *ConnectionUri* utilisé pour la connexion à un emplacement géographique spécifique diffère des instructions de connexion ordinaires.</span><span class="sxs-lookup"><span data-stu-id="749f6-114">To connect to a specific geo location, the *ConnectionUri* parameter is different than the regular connection instructions.</span></span> <span data-ttu-id="749f6-115">Les autres commandes et valeurs sont identiques.</span><span class="sxs-lookup"><span data-stu-id="749f6-115">The rest of the commands and values are the same.</span></span> <span data-ttu-id="749f6-116">Voici comment procéder :</span><span class="sxs-lookup"><span data-stu-id="749f6-116">The steps are:</span></span>

1. <span data-ttu-id="749f6-117">Sur votre ordinateur local, ouvrez Windows PowerShell, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-117">On your local computer, open Windows PowerShell and run the following command:</span></span>

   ```powershell
   $UserCredential = Get-Credential
   ```

   <span data-ttu-id="749f6-118">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez vos nom d’utilisateur et mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="749f6-118">In the **Windows PowerShell Credential Request** dialog box, type your work or school account and password, and then click **OK**.</span></span>

2. <span data-ttu-id="749f6-119">Remplacez `<emailaddress>` par l’adresse e-mail d’une boîte aux lettres **quelconque** dans l’emplacement géographique cible, puis exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="749f6-119">Replace `<emailaddress>` with the email address of **any** mailbox in the target geo location and run the following command.</span></span> <span data-ttu-id="749f6-120">Vos autorisations sur la boîte aux lettres et la relation à vos informations d’identification décrites à l’étape 1 ne constituent pas un facteur. L’adresse e-mail indique simplement à Exchange Online où se connecter.</span><span class="sxs-lookup"><span data-stu-id="749f6-120">Your permissions on the mailbox and the relationship to your credentials in Step 1 are not a factor; the email address simply tells Exchange Online where to connect.</span></span>
  
   ```powershell
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell?email=<emailaddress> -Credential $UserCredential -Authentication  Basic -AllowRedirection
   ```

   <span data-ttu-id="749f6-121">Par exemple, si olga@contoso.onmicrosoft.com est l’adresse e-mail d’une boîte aux lettres valide à l’emplacement géographique auquel vous voulez vous connecter, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-121">For example, if olga@contoso.onmicrosoft.com is the email address of a valid mailbox in the geo location where you want to connect, run the following command:</span></span>

   ```powershell
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell?email=olga@contoso.onmicrosoft.com -Credential $UserCredential -Authentication  Basic -AllowRedirection
   ```

3. <span data-ttu-id="749f6-122">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-122">Run the following command:</span></span>

    ```powershell
    Import-PSSession $Session
    ```

## <a name="view-the-available-geo-locations-that-are-configured-in-your-exchange-online-organization"></a><span data-ttu-id="749f6-123">Affichage des emplacements géographiques disponibles configurés dans votre organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="749f6-123">View the available geo locations that are configured in your Exchange Online organization</span></span>

<span data-ttu-id="749f6-124">Pour afficher la liste des emplacements géographiques configurés dans Microsoft 365 Multi-Geo, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="749f6-124">To see the list of configured geo locations in Microsoft 365 Multi-Geo, run the following command in Exchange Online PowerShell:</span></span>

```powershell
Get-OrganizationConfig | Select -ExpandProperty AllowedMailboxRegions | Format-Table
```

## <a name="view-the-central-geo-location-for-your-exchange-online-organization"></a><span data-ttu-id="749f6-125">Afficher l’emplacement géographique central de votre organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="749f6-125">View the central geo location for your Exchange Online organization</span></span>

<span data-ttu-id="749f6-126">Pour afficher l’emplacement géographique central de votre locataire, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="749f6-126">To view your tenant's central geo location, run the following command in Exchange Online PowerShell:</span></span>

```powershell
Get-OrganizationConfig | Select DefaultMailboxRegion
```

## <a name="find-the-geo-location-of-a-mailbox"></a><span data-ttu-id="749f6-127">Recherche de l’emplacement géographique d’une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="749f6-127">Find the geo location of a mailbox</span></span>

<span data-ttu-id="749f6-128">La cmdlet **Get-Mailbox** dans Exchange Online PowerShell affiche les propriétés multigéographiques associées suivantes sur les boîtes aux lettres :</span><span class="sxs-lookup"><span data-stu-id="749f6-128">The **Get-Mailbox** cmdlet in Exchange Online PowerShell displays the following multi-geo related properties on mailboxes:</span></span>

- <span data-ttu-id="749f6-129">**Database** : les 3 premières lettres du nom de base de données correspondent au géocode indiquant où la boîte aux lettres se trouve actuellement.</span><span class="sxs-lookup"><span data-stu-id="749f6-129">**Database**: The first 3 letters of the database name correspond to the geo code, which tells you where the mailbox is currently located.</span></span> <span data-ttu-id="749f6-130">Pour les boîtes aux lettres d’archivage en ligne, il convient d’utiliser la propriété **ArchiveDatabase**.</span><span class="sxs-lookup"><span data-stu-id="749f6-130">For Online Archive Mailboxes the **ArchiveDatabase** property should be used.</span></span>

- <span data-ttu-id="749f6-131">**MailboxRegion** : spécifie le code de géolocalisation défini par l’administrateur (synchronisé à partir de **PreferredDataLocation** dans Azure AD).</span><span class="sxs-lookup"><span data-stu-id="749f6-131">**MailboxRegion**: Specifies the geo location code that was set by the admin (synchronized from **PreferredDataLocation** in Azure AD).</span></span>

- <span data-ttu-id="749f6-132">**MailboxRegionLastUpdateTime** : indique quand la propriété MailboxRegion a été mise à jour (automatiquement ou manuellement) pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="749f6-132">**MailboxRegionLastUpdateTime**: Indicates when MailboxRegion was last updated (either automatically or manually).</span></span>

<span data-ttu-id="749f6-133">Pour afficher ces propriétés pour une boîte aux lettres, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-133">To see these properties for a mailbox, use the following syntax:</span></span>

```powershell
Get-Mailbox -Identity <MailboxIdentity> | Format-List Database,MailboxRegion*
```

<span data-ttu-id="749f6-134">Par exemple, pour afficher les informations d’emplacement géographique pour la boîte aux lettres chris@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-134">For example, to see the geo location information for the mailbox chris@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Get-Mailbox -Identity chris@contoso.onmicrosoft.com | Format-List Database, MailboxRegion*
```

<span data-ttu-id="749f6-135">Le résultat de la commande ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="749f6-135">The output of the command looks like this:</span></span>

```powershell
Database                    : EURPR03DG077-db007
MailboxRegion               : EUR
MailboxRegionLastUpdateTime : 2/6/2018 8:21:01 PM
```

> [!NOTE]
> <span data-ttu-id="749f6-136">Si le code d’emplacement géographique dans le nom de la base de données ne correspond pas à la valeur **MailboxRegion** , la boîte aux lettres est automatiquement placée dans une file d’attente de relocalisation et déplacée vers l’emplacement géographique spécifié par la valeur **MailboxRegion** (Exchange Online recherche une incompatibilité entre ces valeurs de propriétés).</span><span class="sxs-lookup"><span data-stu-id="749f6-136">If the geo location code in the database name doesn't match **MailboxRegion** value, the mailbox will be automatically be put into a relocation queue and moved to the geo location specified by the **MailboxRegion** value (Exchange Online looks for a mismatch between these property values).</span></span>

## <a name="move-an-existing-cloud-only-mailbox-to-a-specific-geo-location"></a><span data-ttu-id="749f6-137">Déplacer une boîte aux lettres cloud uniquement vers un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="749f6-137">Move an existing cloud-only mailbox to a specific geo location</span></span>

<span data-ttu-id="749f6-138">Un utilisateur cloud uniquement est un utilisateur qui n’est pas synchronisé avec le locataire via AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="749f6-138">A cloud-only user is a user not synchronized to the tenant via AAD Connect.</span></span> <span data-ttu-id="749f6-139">Cet utilisateur a été créé directement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="749f6-139">This user was created directly in Azure AD.</span></span> <span data-ttu-id="749f6-140">Pour afficher ou spécifier la zone géographique dans laquelle sera stockée la boîte aux lettres d’un utilisateur cloud uniquement, utilisez les cmdlets **Get-MsolUser** et **Set-MsolUser** dans le module Azure AD pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="749f6-140">Use the **Get-MsolUser** and **Set-MsolUser** cmdlets in the Azure AD Module for Windows PowerShell to view or specify the geo location where a cloud-only user's mailbox will be stored.</span></span>

<span data-ttu-id="749f6-141">Pour voir la valeur **PreferredDataLocation** pour un utilisateur, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="749f6-141">To view the **PreferredDataLocation** value for a user, use this syntax in Azure AD PowerShell:</span></span>

```powershell
Get-MsolUser -UserPrincipalName <UserPrincipalName> | Format-List UserPrincipalName,PreferredDataLocation
```

<span data-ttu-id="749f6-142">Par exemple, pour voir la valeur **PreferredDataLocation** pour l’utilisateur michelle@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-142">For example, to see the **PreferredDataLocation** value for the user michelle@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Get-MsolUser -UserPrincipalName michelle@contoso.onmicrosoft.com | Format-List
```

<span data-ttu-id="749f6-143">Pour modifier la valeur **PreferredDataLocation** d’un objet utilisateur cloud uniquement, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="749f6-143">To modify the **PreferredDataLocation** value for a cloud-only user object, use the following syntax in Azure AD PowerShell:</span></span>

```powershell
Set-MsolUser -UserPrincipalName <UserPrincipalName> -PreferredDataLocation <GeoLocationCode>
```

<span data-ttu-id="749f6-144">Par exemple, pour définir la valeur **PreferredDataLocation** sur la zone géographique Union européenne (EUR) pour l’utilisateur michelle@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-144">For example, to set the **PreferredDataLocation** value to the European Union (EUR) geo for the user michelle@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Set-MsolUser -UserPrincipalName michelle@contoso.onmicrosoft.com -PreferredDataLocation EUR
```

> [!NOTE]
> - <span data-ttu-id="749f6-145">Comme indiqué précédemment, vous ne pouvez pas utiliser cette procédure pour les objets utilisateur synchronisés à partir d’Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="749f6-145">As mentioned previously, you cannot use this procedure for synchronized user objects from on-premises Active Directory.</span></span> <span data-ttu-id="749f6-146">Vous devez modifier la valeur **PreferredDataLocation** dans Active Directory et la synchroniser à l’aide d’AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="749f6-146">You need to change the **PreferredDataLocation** value in Active Directory and synchronize it using AAD Connect.</span></span> <span data-ttu-id="749f6-147">Pour plus d’informations, voir [Synchronisation Azure Active Directory Connect : Configurer un emplacement de données par défaut pour les ressources Microsoft 365](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-preferreddatalocation).</span><span class="sxs-lookup"><span data-stu-id="749f6-147">For more information, see [Azure Active Directory Connect sync: Configure preferred data location for Microsoft 365 resources](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-preferreddatalocation).</span></span>
> 
> - <span data-ttu-id="749f6-148">Le temps nécessaire pour déplacer une boîte aux lettres vers un nouvel emplacement géographique dépend de plusieurs facteurs :</span><span class="sxs-lookup"><span data-stu-id="749f6-148">How long it takes to relocate a mailbox to a new geo location depends on several factors:</span></span>
> 
>   - <span data-ttu-id="749f6-149">la taille et le type de boîte aux lettres ;</span><span class="sxs-lookup"><span data-stu-id="749f6-149">The size and type of mailbox.</span></span>
> 
>   - <span data-ttu-id="749f6-150">le nombre total de boîtes aux lettres déplacées ;</span><span class="sxs-lookup"><span data-stu-id="749f6-150">The number of mailboxes being moved.</span></span>
> 
>   - <span data-ttu-id="749f6-151">la disponibilité des ressources nécessaires pour le déplacement.</span><span class="sxs-lookup"><span data-stu-id="749f6-151">The availability of move resources.</span></span>

### <a name="move-disabled-mailboxes-that-are-on-litigation-hold"></a><span data-ttu-id="749f6-152">Déplacer des boîtes aux lettres désactivées pour cause de Conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="749f6-152">Move disabled mailboxes that are on Litigation Hold</span></span>

<span data-ttu-id="749f6-153">Il est possible de déplacer des boîtes aux lettres désactivées pour cause de Conservation pour litige à des fins de découverte électronique (eDiscovery) en modifiant leur valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="749f6-153">Disabled mailboxes on Litigation Hold that are preserved for eDiscovery purposes cannot be moved by changing their **PreferredDataLocation** value in their disabled state.</span></span> <span data-ttu-id="749f6-154">Pour déplacer une boîte aux lettres désactivée pour cause de Conservation pour litige :</span><span class="sxs-lookup"><span data-stu-id="749f6-154">To move a disabled mailbox on litigation hold:</span></span>

1. <span data-ttu-id="749f6-155">Attribuez temporairement une licence à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="749f6-155">Temporarily assign a license to the mailbox.</span></span>

2. <span data-ttu-id="749f6-156">Modifiez la valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="749f6-156">Change the **PreferredDataLocation**.</span></span>

3. <span data-ttu-id="749f6-157">Une fois la boîte aux lettres déplacée vers l’emplacement géographique choisi, supprimez sa licence afin de la remettre à l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="749f6-157">Remove the license from the mailbox after it has been moved to the selected geo location to put it back into the disabled state.</span></span>

## <a name="create-new-cloud-mailboxes-in-a-specific-geo-location"></a><span data-ttu-id="749f6-158">Créer des boîtes aux lettres cloud dans un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="749f6-158">Create new cloud mailboxes in a specific geo location</span></span>

<span data-ttu-id="749f6-159">Pour créer une boîte aux lettres dans un emplacement géographique spécifique, vous devez effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="749f6-159">To create a new mailbox in a specific geo location, you need to do either of these steps:</span></span>

- <span data-ttu-id="749f6-160">Configurer la valeur **PreferredDataLocation** de la manière décrite dans la section précédente *avant* de créer la boîte aux lettres dans Exchange Online ;</span><span class="sxs-lookup"><span data-stu-id="749f6-160">Configure the **PreferredDataLocation** value as described in the previous section *before* the mailbox is created in Exchange Online.</span></span> <span data-ttu-id="749f6-161">par exemple, définir la valeur **PreferredDataLocation** sur un utilisateur avant l’attribution d’une licence.</span><span class="sxs-lookup"><span data-stu-id="749f6-161">For example, configure the **PreferredDataLocation** value on a user before assigning a license.</span></span>

- <span data-ttu-id="749f6-162">Attribuer une licence lors de la définition de la valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="749f6-162">Assign a license at the same time you set the **PreferredDataLocation** value.</span></span>

<span data-ttu-id="749f6-163">Pour créer un utilisateur titulaire d’une licence d’utilisation cloud uniquement (non synchronisé avec AAD Connect) dans une zone géographique spécifique, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="749f6-163">To create a new cloud-only licensed user (not AAD Connect synchronized) in a specific geo location, use the following syntax in Azure AD PowerShell:</span></span>

```powershell
New-MsolUser -UserPrincipalName <UserPrincipalName> -DisplayName "<Display Name>" [-FirstName <FirstName>] [-LastName <LastName>] [-Password <Password>] [-LicenseAssignment <AccountSkuId>] -PreferredDataLocation <GeoLocationCode>
```

<span data-ttu-id="749f6-164">Cet exemple montre comment créer un compte d’utilisateur pour Elizabeth Brunner avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="749f6-164">This example create a new user account for Elizabeth Brunner with the following values:</span></span>

- <span data-ttu-id="749f6-165">Nom d’utilisateur principal : ebrunner@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="749f6-165">User principal name: ebrunner@contoso.onmicrosoft.com</span></span>

- <span data-ttu-id="749f6-166">Prénom : Elizabeth</span><span class="sxs-lookup"><span data-stu-id="749f6-166">First name: Elizabeth</span></span>

- <span data-ttu-id="749f6-167">Nom : Brunner</span><span class="sxs-lookup"><span data-stu-id="749f6-167">Last name: Brunner</span></span>

- <span data-ttu-id="749f6-168">Nom d’affichage : Elizabeth Brunner</span><span class="sxs-lookup"><span data-stu-id="749f6-168">Display name: Elizabeth Brunner</span></span>

- <span data-ttu-id="749f6-169">Mot de passe : généré de façon aléatoire et affiché dans les résultats de la commande (étant donné que nous n’utilisons pas le paramètre *Password*)</span><span class="sxs-lookup"><span data-stu-id="749f6-169">Password: randomly-generated and shown in the results of the command (because we're not using the *Password* parameter)</span></span>

- <span data-ttu-id="749f6-170">Licence : `contoso:ENTERPRISEPREMIUM` (E5)</span><span class="sxs-lookup"><span data-stu-id="749f6-170">License: `contoso:ENTERPRISEPREMIUM` (E5)</span></span>

- <span data-ttu-id="749f6-171">Emplacement : Australie (AUS)</span><span class="sxs-lookup"><span data-stu-id="749f6-171">Location: Australia (AUS)</span></span>

```powershell
New-MsolUser -UserPrincipalName ebrunner@contoso.onmicrosoft.com -DisplayName "Elizabeth Brunner" -FirstName Elizabeth -LastName Brunner -LicenseAssignment contoso:ENTERPRISEPREMIUM -PreferredDataLocation AUS
```

<span data-ttu-id="749f6-172">Pour plus d’informations sur la création de comptes d’utilisateur et la recherche de valeurs LicenseAssignment dans Azure AD PowerShell, voir [Création de comptes d’utilisateurs avec PowerShell](create-user-accounts-with-microsoft-365-powershell.md) et [Afficher les licences et les services avec PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="749f6-172">For more information about creating new user accounts and finding LicenseAssignment values in Azure AD PowerShell, see [Create user accounts with PowerShell](create-user-accounts-with-microsoft-365-powershell.md) and [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>

> [!NOTE]
> <span data-ttu-id="749f6-173">Sii vous utilisez Exchange Online PowerShell pour activer une boîte aux lettres et avez besoin que la boîte aux lettres soit créée directement dans la zone géographique spécifiée dans **PreferredDataLocation**, vous devez utiliser une cmdlet Exchange Online telle que **Enable-Mailbox** ou **New-Mailbox** directement sur le service cloud.</span><span class="sxs-lookup"><span data-stu-id="749f6-173">If you are using Exchange Online PowerShell to enable a mailbox and need the mailbox to be created directly in the geo location that's specified in **PreferredDataLocation**, you need to use an Exchange Online cmdlet such as **Enable-Mailbox** or **New-Mailbox** directly against the cloud service.</span></span> <span data-ttu-id="749f6-174">Si vous utilisez la cmdlet **Enable-RemoteMailbox** dans le powerShell Exchange sur site, la boîte aux lettres est créée dans l’emplacement géographique central.</span><span class="sxs-lookup"><span data-stu-id="749f6-174">If you use the **Enable-RemoteMailbox** cmdlet in on-premises Exchange PowerShell, the mailbox will be created in the central geo location.</span></span>

## <a name="onboard-existing-on-premises-mailboxes-in-a-specific-geo-location"></a><span data-ttu-id="749f6-175">Intégrer des boîtes aux lettres locales existant dans un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="749f6-175">Onboard existing on-premises mailboxes in a specific geo location</span></span>

<span data-ttu-id="749f6-176">Vous pouvez vous servir des outils et processus d’intégration standard pour migrer une boîte aux lettres d’une organisation Exchange locale vers Exchange Online. Ces outils sont le [Tableau de bord de migration dans le Centre d’administration Exchange](https://support.office.com/article/d164b35c-f624-4f83-ac58-b7cae96ab331) et la cmdlet [New-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/new-migrationbatch) dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="749f6-176">You can use the standard onboarding tools and processes to migrate a mailbox from an on-premises Exchange organization to Exchange Online, including the [Migration dashboard in the EAC](https://support.office.com/article/d164b35c-f624-4f83-ac58-b7cae96ab331), and the [New-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/new-migrationbatch) cmdlet in Exchange Online PowerShell.</span></span>

<span data-ttu-id="749f6-177">La première étape consiste à vérifier qu’un objet utilisateur existe pour chaque boîte aux lettres à intégrer, et que la valeur **PreferredDataLocation** correcte est configurée dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="749f6-177">The first step is to verify a user object exists for each mailbox to be onboarded, and verify the correct **PreferredDataLocation** value is configured in Azure AD.</span></span> <span data-ttu-id="749f6-178">Les outils d’intégration respectent la valeur **PreferredDataLocation** et migrent les boîtes aux lettres directement vers la zone géographique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="749f6-178">The onboarding tools will respect the **PreferredDataLocation** value and will migrate the mailboxes directly to the specified geo location.</span></span>

<span data-ttu-id="749f6-179">Ou bien, pour intégrer les boîtes aux lettres directement dans un emplacement géographique à l’aide de la cmdlet [New-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/new-moverequest) dans Exchange Online PowerShell, vous pouvez également procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="749f6-179">Or, you can use the following steps to onboard mailboxes directly in a specific geo location using the [New-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/new-moverequest) cmdlet in Exchange Online PowerShell.</span></span>

1. <span data-ttu-id="749f6-180">Vérifiez que l’objet utilisateur existe pour chaque boîte aux lettres intégrée et que la valeur **PreferredDataLocation** est correctement définie dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="749f6-180">Verify the user object exists for each mailbox to be onboarded and that **PreferredDataLocation** is set to the desired value in Azure AD.</span></span> <span data-ttu-id="749f6-181">La valeur **PreferredDataLocation** est synchronisée avec l’attribut **MailboxRegion** de l’objet utilisateur de courrier correspondant dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="749f6-181">The value of **PreferredDataLocation** will be synchronized to the **MailboxRegion** attribute of the corresponding mail user object in Exchange Online.</span></span>

2. <span data-ttu-id="749f6-182">Connectez-vous directement à la zone géographique satellite spécifique en suivant les instructions de connexion figurant plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="749f6-182">Connect directly to the specific satellite geo location using the connection instructions from earlier in this topic.</span></span>

3. <span data-ttu-id="749f6-183">Dans Exchange Online PowerShell, stockez les informations d’identification d’administrateur locales utilisées pour effectuer une migration de boîte aux lettres dans une variable en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="749f6-183">In Exchange Online PowerShell, store the on-premises administrator credentials that's used to perform a mailbox migration in a variable by running the following command:</span></span>

   ```powershell
   $RC = Get-Credential
   ```

4. <span data-ttu-id="749f6-184">Dans Exchange Online PowerShell, créez une cmdlet **New-MoveRequest** similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="749f6-184">In Exchange Online PowerShell, create a new **New-MoveRequest** similar to the following example:</span></span>

   ```powershell
   New-MoveRequest -Remote -RemoteHostName mail.contoso.com -RemoteCredential $RC -Identity user@contoso.com -TargetDeliveryDomain <YourAppropriateDomain>
   ```

5. <span data-ttu-id="749f6-185">Répétez l’étape 4 pour chaque boîte aux lettres à migrer d’Exchange sur site vers l’emplacement géographique satellite auquel vous êtes actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="749f6-185">Repeat step #4 for every mailbox you need to migrate from on-premises Exchange to the satellite geo location you are currently connected to.</span></span>

6. <span data-ttu-id="749f6-186">Si vous devez migrer des boîtes aux lettres supplémentaires vers un autre emplacement géographique satellite, répétez les étapes 2 à 4 pour chaque emplacement spécifique.</span><span class="sxs-lookup"><span data-stu-id="749f6-186">If you need to migrate additional mailboxes to different satellite geo locations, repeat steps 2 through 4 for each specific location.</span></span>

## <a name="multi-geo-reporting"></a><span data-ttu-id="749f6-187">Génération de rapports multigéographiques</span><span class="sxs-lookup"><span data-stu-id="749f6-187">Multi-geo reporting</span></span>

<span data-ttu-id="749f6-188">Les **rapports d’utilisation multigéographique** dans le Centre d’administration Microsoft 365 affichent le nombre d’utilisateurs par emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="749f6-188">**Multi-Geo Usage Reports** in the Microsoft 365 admin center displays the user count by geo location.</span></span> <span data-ttu-id="749f6-189">Le rapport présente la répartition des utilisateurs pour le mois en cours et les données historiques des 6 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="749f6-189">The report displays user distribution for the current month and provides historical data for the past 6 months.</span></span>

## <a name="see-also"></a><span data-ttu-id="749f6-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="749f6-190">See also</span></span>

[<span data-ttu-id="749f6-191">Gestion de Microsoft 365 et d’Exchange Online avec Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="749f6-191">Managing Microsoft 365 and Exchange Online with Windows PowerShell</span></span>](https://support.office.com//article/06a743bb-ceb6-49a9-a61d-db4ffdf54fa6)
