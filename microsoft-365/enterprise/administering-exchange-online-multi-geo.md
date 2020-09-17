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
ms.openlocfilehash: ea7090cd65634138f9677960beab7770825a6e86
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950675"
---
# <a name="administering-exchange-online-mailboxes-in-a-multi-geo-environment"></a><span data-ttu-id="3df08-103">Administration des boîtes aux lettres Exchange Online dans un environnement multigéographique</span><span class="sxs-lookup"><span data-stu-id="3df08-103">Administering Exchange Online mailboxes in a multi-geo environment</span></span>

<span data-ttu-id="3df08-104">Exchange Online PowerShell est requis pour afficher et configurer les propriétés multi-géo dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3df08-104">Exchange Online PowerShell is required to view and configure multi geo properties in your Microsoft 365 environment.</span></span> <span data-ttu-id="3df08-105">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="3df08-105">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="3df08-106">Pour voir la propriété **PreferredDataLocation** sur les objets utilisateur, vous devez disposer du [module PowerShell Microsoft Azure Active Directory](https://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) v1.1.166.0 ou version v1.x ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3df08-106">You need the [Microsoft Azure Active Directory PowerShell Module](https://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) v1.1.166.0 or later in v1.x to see the **PreferredDataLocation** property on user objects.</span></span> <span data-ttu-id="3df08-107">La valeur **PreferredDataLocation** des objets utilisateur synchronisés via AAD Connect dans AAD ne peut pas être modifiée directement via AAD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3df08-107">User objects synchronized via AAD Connect into AAD cannot have their **PreferredDataLocation** value directly modified via AAD PowerShell.</span></span> <span data-ttu-id="3df08-108">Les objets utilisateur cloud uniquement peuvent être modifiés via AAD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3df08-108">Cloud-only user objects can be modified via AAD PowerShell.</span></span> <span data-ttu-id="3df08-109">Pour vous connecter à Azure AD PowerShell, voir [Se connecter à PowerShell](connect-to-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="3df08-109">To connect to Azure AD PowerShell, see [Connect to PowerShell](connect-to-microsoft-365-powershell.md).</span></span>

## <a name="connect-directly-to-a-geo-location-using-exchange-online-powershell"></a><span data-ttu-id="3df08-110">Se connecter directement à un emplacement géographique à l’aide d’Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="3df08-110">Connect directly to a geo location using Exchange Online PowerShell</span></span>

<span data-ttu-id="3df08-111">En règle générale, Exchange Online PowerShell se connecte à l’emplacement géographique central.</span><span class="sxs-lookup"><span data-stu-id="3df08-111">Typically, Exchange Online PowerShell will connect to the central geo location.</span></span> <span data-ttu-id="3df08-112">Vous pouvez cependant aussi vous connecter directement à des emplacements satellites géographiques.</span><span class="sxs-lookup"><span data-stu-id="3df08-112">But, you can also connect directly to satellite geo locations.</span></span> <span data-ttu-id="3df08-113">En raison des améliorations apportées aux performances, nous vous recommandons de vous connecter directement à l’emplacement satellite géographique lorsque vous gérez uniquement des utilisateurs situés dans cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="3df08-113">Because of performance improvements, we recommend connecting directly to the satellite geo location when you only manage users in that location.</span></span>

<span data-ttu-id="3df08-114">Les conditions requises pour l’installation et l’utilisation du module EXO v2 sont décrites dans [Installer et gérer le module EXO v2](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exo-v2-module).</span><span class="sxs-lookup"><span data-stu-id="3df08-114">The requirements for installing and using the EXO V2 module are described in [Install and maintain the EXO V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exo-v2-module).</span></span>

<span data-ttu-id="3df08-115">Pour connecter Exchange Online PowerShell à un emplacement géographique spécifique, le paramètre *ConnectionUri* est différent des instructions de connexion normales.</span><span class="sxs-lookup"><span data-stu-id="3df08-115">To connect Exchange Online PowerShell to a specific geo location, the *ConnectionUri* parameter is different than the regular connection instructions.</span></span> <span data-ttu-id="3df08-116">Les autres commandes et valeurs sont identiques.</span><span class="sxs-lookup"><span data-stu-id="3df08-116">The rest of the commands and values are the same.</span></span>

<span data-ttu-id="3df08-117">Plus précisément, vous devez ajouter la `?email=<emailaddress>` valeur à la fin de la valeur _ConnectionUri_ .</span><span class="sxs-lookup"><span data-stu-id="3df08-117">Specifically, you need to add the `?email=<emailaddress>` value to end of the _ConnectionUri_ value.</span></span> <span data-ttu-id="3df08-118">`<emailaddress>` est l’adresse de messagerie de **n’importe quelle** boîte aux lettres dans l’emplacement géographique cible.</span><span class="sxs-lookup"><span data-stu-id="3df08-118">`<emailaddress>` is the email address of **any** mailbox in the target geo location.</span></span> <span data-ttu-id="3df08-119">Vos autorisations sur cette boîte aux lettres ou la relation avec vos informations d’identification n’est pas un facteur ; l’adresse de messagerie indique simplement à Exchange Online PowerShell où se connecter.</span><span class="sxs-lookup"><span data-stu-id="3df08-119">Your permissions to that mailbox or the relationship to your credentials are not a factor; the email address simply tells Exchange Online PowerShell where to connect.</span></span>

<span data-ttu-id="3df08-120">Les clients Microsoft 365 ou Microsoft 365 GCC n’ont généralement pas besoin d’utiliser le paramètre _ConnectionUri_ pour se connecter à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3df08-120">Microsoft 365 or Microsoft 365 GCC customers typically don't need to use the _ConnectionUri_ parameter to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="3df08-121">Toutefois, pour vous connecter à un emplacement géographique spécifique, vous devez utiliser le paramètre _ConnectionUri_ afin `?email=<emailaddress>` de pouvoir l’utiliser dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="3df08-121">But, to connect to a specific geo location, you do need to use _ConnectionUri_ parameter so you can use `?email=<emailaddress>` in the value.</span></span>

### <a name="connect-to-a-geo-location-in-exchange-online-powershell-using-multi-factor-authentication-mfa"></a><span data-ttu-id="3df08-122">Se connecter à un emplacement géographique dans Exchange Online PowerShell à l’aide de Multi-Factor Authentication (MFA)</span><span class="sxs-lookup"><span data-stu-id="3df08-122">Connect to a geo location in Exchange Online PowerShell using multi-factor authentication (MFA)</span></span>

1. <span data-ttu-id="3df08-123">Dans une fenêtre Windows PowerShell, chargez le module EXO V2 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-123">In a Windows PowerShell window, load the EXO V2 module by running the following command:</span></span>

   ```powershell
   Import-Module ExchangeOnlineManagement
   ```

2. <span data-ttu-id="3df08-124">Dans l’exemple suivant, admin@contoso.onmicrosoft.com est le compte d’administrateur et l’emplacement géographique cible est l’emplacement où réside la boîte aux lettres olga@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="3df08-124">In the following example, admin@contoso.onmicrosoft.com is the admin account, and the target geo location is where the mailbox olga@contoso.onmicrosoft.com resides.</span></span>

  ```powershell
  Connect-ExchangeOnline -UserPrincipalName admin@contoso.onmicrosoft.com -ShowProgress $true -ConnectionUri https://outlook.office365.com/powershell?email=olga@contoso.onmicrosoft.com
  ```

### <a name="connect-to-a-geo-location-in-exchange-online-powershell-without-using-mfa"></a><span data-ttu-id="3df08-125">Se connecter à un emplacement géographique dans Exchange Online PowerShell sans utiliser l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="3df08-125">Connect to a geo location in Exchange Online PowerShell without using MFA</span></span>

1. <span data-ttu-id="3df08-126">Dans une fenêtre Windows PowerShell, chargez le module EXO V2 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-126">In a Windows PowerShell window, load the EXO V2 module by running the following command:</span></span>

   ```powershell
   Import-Module ExchangeOnlineManagement
   ```

2. <span data-ttu-id="3df08-127">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-127">Run the following command:</span></span>

   ```powershell
   $UserCredential = Get-Credential
   ```

   <span data-ttu-id="3df08-128">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell** qui s’affiche, saisissez vos nom d’utilisateur et mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3df08-128">In the **Windows PowerShell Credential Request** dialog box that appears, type your work or school account and password, and then click **OK**.</span></span>

3. <span data-ttu-id="3df08-129">Dans l’exemple suivant, l’emplacement géographique cible est l’emplacement où réside la boîte aux lettres olga@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="3df08-129">In the following example, the target geo location is where the mailbox olga@contoso.onmicrosoft.com resides.</span></span>

   ```powershell
   Connect-ExchangeOnline -Credential $UserCredential -ShowProgress $true -ConnectionUri https://outlook.office365.com/powershell?email=olga@contoso.onmicrosoft.com
   ```

## <a name="view-the-available-geo-locations-that-are-configured-in-your-exchange-online-organization"></a><span data-ttu-id="3df08-130">Affichage des emplacements géographiques disponibles configurés dans votre organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3df08-130">View the available geo locations that are configured in your Exchange Online organization</span></span>

<span data-ttu-id="3df08-131">Pour afficher la liste des emplacements géographiques configurés dans Microsoft 365 Multi-Geo, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3df08-131">To see the list of configured geo locations in Microsoft 365 Multi-Geo, run the following command in Exchange Online PowerShell:</span></span>

```powershell
Get-OrganizationConfig | Select -ExpandProperty AllowedMailboxRegions | Format-Table
```

## <a name="view-the-central-geo-location-for-your-exchange-online-organization"></a><span data-ttu-id="3df08-132">Afficher l’emplacement géographique central de votre organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3df08-132">View the central geo location for your Exchange Online organization</span></span>

<span data-ttu-id="3df08-133">Pour afficher l’emplacement géographique central de votre locataire, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3df08-133">To view your tenant's central geo location, run the following command in Exchange Online PowerShell:</span></span>

```powershell
Get-OrganizationConfig | Select DefaultMailboxRegion
```

## <a name="find-the-geo-location-of-a-mailbox"></a><span data-ttu-id="3df08-134">Recherche de l’emplacement géographique d’une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="3df08-134">Find the geo location of a mailbox</span></span>

<span data-ttu-id="3df08-135">La cmdlet **Get-Mailbox** dans Exchange Online PowerShell affiche les propriétés multigéographiques associées suivantes sur les boîtes aux lettres :</span><span class="sxs-lookup"><span data-stu-id="3df08-135">The **Get-Mailbox** cmdlet in Exchange Online PowerShell displays the following multi-geo related properties on mailboxes:</span></span>

- <span data-ttu-id="3df08-136">**Database** : les 3 premières lettres du nom de base de données correspondent au géocode indiquant où la boîte aux lettres se trouve actuellement.</span><span class="sxs-lookup"><span data-stu-id="3df08-136">**Database**: The first 3 letters of the database name correspond to the geo code, which tells you where the mailbox is currently located.</span></span> <span data-ttu-id="3df08-137">Pour les boîtes aux lettres d’archivage en ligne, il convient d’utiliser la propriété **ArchiveDatabase**.</span><span class="sxs-lookup"><span data-stu-id="3df08-137">For Online Archive Mailboxes the **ArchiveDatabase** property should be used.</span></span>

- <span data-ttu-id="3df08-138">**MailboxRegion** : spécifie le code de géolocalisation défini par l’administrateur (synchronisé à partir de **PreferredDataLocation** dans Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3df08-138">**MailboxRegion**: Specifies the geo location code that was set by the admin (synchronized from **PreferredDataLocation** in Azure AD).</span></span>

- <span data-ttu-id="3df08-139">**MailboxRegionLastUpdateTime** : indique quand la propriété MailboxRegion a été mise à jour (automatiquement ou manuellement) pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="3df08-139">**MailboxRegionLastUpdateTime**: Indicates when MailboxRegion was last updated (either automatically or manually).</span></span>

<span data-ttu-id="3df08-140">Pour afficher ces propriétés pour une boîte aux lettres, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-140">To see these properties for a mailbox, use the following syntax:</span></span>

```powershell
Get-Mailbox -Identity <MailboxIdentity> | Format-List Database,MailboxRegion*
```

<span data-ttu-id="3df08-141">Par exemple, pour afficher les informations d’emplacement géographique pour la boîte aux lettres chris@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-141">For example, to see the geo location information for the mailbox chris@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Get-Mailbox -Identity chris@contoso.onmicrosoft.com | Format-List Database, MailboxRegion*
```

<span data-ttu-id="3df08-142">Le résultat de la commande ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="3df08-142">The output of the command looks like this:</span></span>

```powershell
Database                    : EURPR03DG077-db007
MailboxRegion               : EUR
MailboxRegionLastUpdateTime : 2/6/2018 8:21:01 PM
```

> [!NOTE]
> <span data-ttu-id="3df08-143">Si le code d’emplacement géographique dans le nom de la base de données ne correspond pas à la valeur **MailboxRegion** , la boîte aux lettres est automatiquement placée dans une file d’attente de relocalisation et déplacée vers l’emplacement géographique spécifié par la valeur **MailboxRegion** (Exchange Online recherche une incompatibilité entre ces valeurs de propriétés).</span><span class="sxs-lookup"><span data-stu-id="3df08-143">If the geo location code in the database name doesn't match **MailboxRegion** value, the mailbox will be automatically be put into a relocation queue and moved to the geo location specified by the **MailboxRegion** value (Exchange Online looks for a mismatch between these property values).</span></span>

## <a name="move-an-existing-cloud-only-mailbox-to-a-specific-geo-location"></a><span data-ttu-id="3df08-144">Déplacer une boîte aux lettres cloud uniquement vers un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="3df08-144">Move an existing cloud-only mailbox to a specific geo location</span></span>

<span data-ttu-id="3df08-145">Un utilisateur cloud uniquement est un utilisateur qui n’est pas synchronisé avec le locataire via AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="3df08-145">A cloud-only user is a user not synchronized to the tenant via AAD Connect.</span></span> <span data-ttu-id="3df08-146">Cet utilisateur a été créé directement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3df08-146">This user was created directly in Azure AD.</span></span> <span data-ttu-id="3df08-147">Pour afficher ou spécifier la zone géographique dans laquelle sera stockée la boîte aux lettres d’un utilisateur cloud uniquement, utilisez les cmdlets **Get-MsolUser** et **Set-MsolUser** dans le module Azure AD pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3df08-147">Use the **Get-MsolUser** and **Set-MsolUser** cmdlets in the Azure AD Module for Windows PowerShell to view or specify the geo location where a cloud-only user's mailbox will be stored.</span></span>

<span data-ttu-id="3df08-148">Pour voir la valeur **PreferredDataLocation** pour un utilisateur, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3df08-148">To view the **PreferredDataLocation** value for a user, use this syntax in Azure AD PowerShell:</span></span>

```powershell
Get-MsolUser -UserPrincipalName <UserPrincipalName> | Format-List UserPrincipalName,PreferredDataLocation
```

<span data-ttu-id="3df08-149">Par exemple, pour voir la valeur **PreferredDataLocation** pour l’utilisateur michelle@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-149">For example, to see the **PreferredDataLocation** value for the user michelle@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Get-MsolUser -UserPrincipalName michelle@contoso.onmicrosoft.com | Format-List
```

<span data-ttu-id="3df08-150">Pour modifier la valeur **PreferredDataLocation** d’un objet utilisateur cloud uniquement, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3df08-150">To modify the **PreferredDataLocation** value for a cloud-only user object, use the following syntax in Azure AD PowerShell:</span></span>

```powershell
Set-MsolUser -UserPrincipalName <UserPrincipalName> -PreferredDataLocation <GeoLocationCode>
```

<span data-ttu-id="3df08-151">Par exemple, pour définir la valeur **PreferredDataLocation** sur la zone géographique Union européenne (EUR) pour l’utilisateur michelle@contoso.onmicrosoft.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-151">For example, to set the **PreferredDataLocation** value to the European Union (EUR) geo for the user michelle@contoso.onmicrosoft.com, run the following command:</span></span>

```powershell
Set-MsolUser -UserPrincipalName michelle@contoso.onmicrosoft.com -PreferredDataLocation EUR
```

> [!NOTE]
>
> - <span data-ttu-id="3df08-152">Comme indiqué précédemment, vous ne pouvez pas utiliser cette procédure pour les objets utilisateur synchronisés à partir d’Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="3df08-152">As mentioned previously, you cannot use this procedure for synchronized user objects from on-premises Active Directory.</span></span> <span data-ttu-id="3df08-153">Vous devez modifier la valeur **PreferredDataLocation** dans Active Directory et la synchroniser à l’aide d’AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="3df08-153">You need to change the **PreferredDataLocation** value in Active Directory and synchronize it using AAD Connect.</span></span> <span data-ttu-id="3df08-154">Pour plus d’informations, voir [Synchronisation Azure Active Directory Connect : Configurer un emplacement de données par défaut pour les ressources Microsoft 365](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-preferreddatalocation).</span><span class="sxs-lookup"><span data-stu-id="3df08-154">For more information, see [Azure Active Directory Connect sync: Configure preferred data location for Microsoft 365 resources](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-preferreddatalocation).</span></span>
>
> - <span data-ttu-id="3df08-155">Le temps nécessaire pour déplacer une boîte aux lettres vers un nouvel emplacement géographique dépend de plusieurs facteurs :</span><span class="sxs-lookup"><span data-stu-id="3df08-155">How long it takes to relocate a mailbox to a new geo location depends on several factors:</span></span>
>
>   - <span data-ttu-id="3df08-156">la taille et le type de boîte aux lettres ;</span><span class="sxs-lookup"><span data-stu-id="3df08-156">The size and type of mailbox.</span></span>
>   - <span data-ttu-id="3df08-157">le nombre total de boîtes aux lettres déplacées ;</span><span class="sxs-lookup"><span data-stu-id="3df08-157">The number of mailboxes being moved.</span></span>
>   - <span data-ttu-id="3df08-158">la disponibilité des ressources nécessaires pour le déplacement.</span><span class="sxs-lookup"><span data-stu-id="3df08-158">The availability of move resources.</span></span>

### <a name="move-disabled-mailboxes-that-are-on-litigation-hold"></a><span data-ttu-id="3df08-159">Déplacer des boîtes aux lettres désactivées pour cause de Conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="3df08-159">Move disabled mailboxes that are on Litigation Hold</span></span>

<span data-ttu-id="3df08-160">Il est possible de déplacer des boîtes aux lettres désactivées pour cause de Conservation pour litige à des fins de découverte électronique (eDiscovery) en modifiant leur valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="3df08-160">Disabled mailboxes on Litigation Hold that are preserved for eDiscovery purposes cannot be moved by changing their **PreferredDataLocation** value in their disabled state.</span></span> <span data-ttu-id="3df08-161">Pour déplacer une boîte aux lettres désactivée pour cause de Conservation pour litige :</span><span class="sxs-lookup"><span data-stu-id="3df08-161">To move a disabled mailbox on litigation hold:</span></span>

1. <span data-ttu-id="3df08-162">Attribuez temporairement une licence à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3df08-162">Temporarily assign a license to the mailbox.</span></span>

2. <span data-ttu-id="3df08-163">Modifiez la valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="3df08-163">Change the **PreferredDataLocation**.</span></span>

3. <span data-ttu-id="3df08-164">Une fois la boîte aux lettres déplacée vers l’emplacement géographique choisi, supprimez sa licence afin de la remettre à l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="3df08-164">Remove the license from the mailbox after it has been moved to the selected geo location to put it back into the disabled state.</span></span>

## <a name="create-new-cloud-mailboxes-in-a-specific-geo-location"></a><span data-ttu-id="3df08-165">Créer des boîtes aux lettres cloud dans un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="3df08-165">Create new cloud mailboxes in a specific geo location</span></span>

<span data-ttu-id="3df08-166">Pour créer une boîte aux lettres dans un emplacement géographique spécifique, vous devez effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3df08-166">To create a new mailbox in a specific geo location, you need to do either of these steps:</span></span>

- <span data-ttu-id="3df08-167">Configurer la valeur **PreferredDataLocation** de la manière décrite dans la section précédente *avant* de créer la boîte aux lettres dans Exchange Online ;</span><span class="sxs-lookup"><span data-stu-id="3df08-167">Configure the **PreferredDataLocation** value as described in the previous section *before* the mailbox is created in Exchange Online.</span></span> <span data-ttu-id="3df08-168">par exemple, définir la valeur **PreferredDataLocation** sur un utilisateur avant l’attribution d’une licence.</span><span class="sxs-lookup"><span data-stu-id="3df08-168">For example, configure the **PreferredDataLocation** value on a user before assigning a license.</span></span>

- <span data-ttu-id="3df08-169">Attribuer une licence lors de la définition de la valeur **PreferredDataLocation**.</span><span class="sxs-lookup"><span data-stu-id="3df08-169">Assign a license at the same time you set the **PreferredDataLocation** value.</span></span>

<span data-ttu-id="3df08-170">Pour créer un utilisateur titulaire d’une licence d’utilisation cloud uniquement (non synchronisé avec AAD Connect) dans une zone géographique spécifique, utilisez la syntaxe suivante dans Azure AD PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3df08-170">To create a new cloud-only licensed user (not AAD Connect synchronized) in a specific geo location, use the following syntax in Azure AD PowerShell:</span></span>

```powershell
New-MsolUser -UserPrincipalName <UserPrincipalName> -DisplayName "<Display Name>" [-FirstName <FirstName>] [-LastName <LastName>] [-Password <Password>] [-LicenseAssignment <AccountSkuId>] -PreferredDataLocation <GeoLocationCode>
```

<span data-ttu-id="3df08-171">Cet exemple montre comment créer un compte d’utilisateur pour Elizabeth Brunner avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3df08-171">This example create a new user account for Elizabeth Brunner with the following values:</span></span>

- <span data-ttu-id="3df08-172">Nom d’utilisateur principal : ebrunner@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="3df08-172">User principal name: ebrunner@contoso.onmicrosoft.com</span></span>
- <span data-ttu-id="3df08-173">Prénom : Elizabeth</span><span class="sxs-lookup"><span data-stu-id="3df08-173">First name: Elizabeth</span></span>
- <span data-ttu-id="3df08-174">Nom : Brunner</span><span class="sxs-lookup"><span data-stu-id="3df08-174">Last name: Brunner</span></span>
- <span data-ttu-id="3df08-175">Nom d’affichage : Elizabeth Brunner</span><span class="sxs-lookup"><span data-stu-id="3df08-175">Display name: Elizabeth Brunner</span></span>
- <span data-ttu-id="3df08-176">Mot de passe : généré de façon aléatoire et affiché dans les résultats de la commande (étant donné que nous n’utilisons pas le paramètre *Password*)</span><span class="sxs-lookup"><span data-stu-id="3df08-176">Password: randomly-generated and shown in the results of the command (because we're not using the *Password* parameter)</span></span>
- <span data-ttu-id="3df08-177">Licence : `contoso:ENTERPRISEPREMIUM` (E5)</span><span class="sxs-lookup"><span data-stu-id="3df08-177">License: `contoso:ENTERPRISEPREMIUM` (E5)</span></span>
- <span data-ttu-id="3df08-178">Emplacement : Australie (AUS)</span><span class="sxs-lookup"><span data-stu-id="3df08-178">Location: Australia (AUS)</span></span>

```powershell
New-MsolUser -UserPrincipalName ebrunner@contoso.onmicrosoft.com -DisplayName "Elizabeth Brunner" -FirstName Elizabeth -LastName Brunner -LicenseAssignment contoso:ENTERPRISEPREMIUM -PreferredDataLocation AUS
```

<span data-ttu-id="3df08-179">Pour plus d’informations sur la création de comptes d’utilisateur et la recherche de valeurs LicenseAssignment dans Azure AD PowerShell, voir [Création de comptes d’utilisateurs avec PowerShell](create-user-accounts-with-microsoft-365-powershell.md) et [Afficher les licences et les services avec PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="3df08-179">For more information about creating new user accounts and finding LicenseAssignment values in Azure AD PowerShell, see [Create user accounts with PowerShell](create-user-accounts-with-microsoft-365-powershell.md) and [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>

> [!NOTE]
> <span data-ttu-id="3df08-180">Sii vous utilisez Exchange Online PowerShell pour activer une boîte aux lettres et avez besoin que la boîte aux lettres soit créée directement dans la zone géographique spécifiée dans **PreferredDataLocation**, vous devez utiliser une cmdlet Exchange Online telle que **Enable-Mailbox** ou **New-Mailbox** directement sur le service cloud.</span><span class="sxs-lookup"><span data-stu-id="3df08-180">If you are using Exchange Online PowerShell to enable a mailbox and need the mailbox to be created directly in the geo location that's specified in **PreferredDataLocation**, you need to use an Exchange Online cmdlet such as **Enable-Mailbox** or **New-Mailbox** directly against the cloud service.</span></span> <span data-ttu-id="3df08-181">Si vous utilisez la cmdlet **Enable-RemoteMailbox** dans le powerShell Exchange sur site, la boîte aux lettres est créée dans l’emplacement géographique central.</span><span class="sxs-lookup"><span data-stu-id="3df08-181">If you use the **Enable-RemoteMailbox** cmdlet in on-premises Exchange PowerShell, the mailbox will be created in the central geo location.</span></span>

## <a name="onboard-existing-on-premises-mailboxes-in-a-specific-geo-location"></a><span data-ttu-id="3df08-182">Intégrer des boîtes aux lettres locales existant dans un emplacement géographique spécifique</span><span class="sxs-lookup"><span data-stu-id="3df08-182">Onboard existing on-premises mailboxes in a specific geo location</span></span>

<span data-ttu-id="3df08-183">Vous pouvez vous servir des outils et processus d’intégration standard pour migrer une boîte aux lettres d’une organisation Exchange locale vers Exchange Online. Ces outils sont le [Tableau de bord de migration dans le Centre d’administration Exchange](https://support.office.com/article/d164b35c-f624-4f83-ac58-b7cae96ab331) et la cmdlet [New-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/new-migrationbatch) dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3df08-183">You can use the standard onboarding tools and processes to migrate a mailbox from an on-premises Exchange organization to Exchange Online, including the [Migration dashboard in the EAC](https://support.office.com/article/d164b35c-f624-4f83-ac58-b7cae96ab331), and the [New-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/new-migrationbatch) cmdlet in Exchange Online PowerShell.</span></span>

<span data-ttu-id="3df08-184">La première étape consiste à vérifier qu’un objet utilisateur existe pour chaque boîte aux lettres à intégrer, et que la valeur **PreferredDataLocation** correcte est configurée dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3df08-184">The first step is to verify a user object exists for each mailbox to be onboarded, and verify the correct **PreferredDataLocation** value is configured in Azure AD.</span></span> <span data-ttu-id="3df08-185">Les outils d’intégration respectent la valeur **PreferredDataLocation** et migrent les boîtes aux lettres directement vers la zone géographique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3df08-185">The onboarding tools will respect the **PreferredDataLocation** value and will migrate the mailboxes directly to the specified geo location.</span></span>

<span data-ttu-id="3df08-186">Ou bien, pour intégrer les boîtes aux lettres directement dans un emplacement géographique à l’aide de la cmdlet [New-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/new-moverequest) dans Exchange Online PowerShell, vous pouvez également procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="3df08-186">Or, you can use the following steps to onboard mailboxes directly in a specific geo location using the [New-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/new-moverequest) cmdlet in Exchange Online PowerShell.</span></span>

1. <span data-ttu-id="3df08-187">Vérifiez que l’objet utilisateur existe pour chaque boîte aux lettres intégrée et que la valeur **PreferredDataLocation** est correctement définie dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3df08-187">Verify the user object exists for each mailbox to be onboarded and that **PreferredDataLocation** is set to the desired value in Azure AD.</span></span> <span data-ttu-id="3df08-188">La valeur **PreferredDataLocation** est synchronisée avec l’attribut **MailboxRegion** de l’objet utilisateur de courrier correspondant dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3df08-188">The value of **PreferredDataLocation** will be synchronized to the **MailboxRegion** attribute of the corresponding mail user object in Exchange Online.</span></span>

2. <span data-ttu-id="3df08-189">Connectez-vous directement à la zone géographique satellite spécifique en suivant les instructions de connexion figurant plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3df08-189">Connect directly to the specific satellite geo location using the connection instructions from earlier in this topic.</span></span>

3. <span data-ttu-id="3df08-190">Dans Exchange Online PowerShell, stockez les informations d’identification d’administrateur locales utilisées pour effectuer une migration de boîte aux lettres dans une variable en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3df08-190">In Exchange Online PowerShell, store the on-premises administrator credentials that's used to perform a mailbox migration in a variable by running the following command:</span></span>

   ```powershell
   $RC = Get-Credential
   ```

4. <span data-ttu-id="3df08-191">Dans Exchange Online PowerShell, créez une cmdlet **New-MoveRequest** similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3df08-191">In Exchange Online PowerShell, create a new **New-MoveRequest** similar to the following example:</span></span>

   ```powershell
   New-MoveRequest -Remote -RemoteHostName mail.contoso.com -RemoteCredential $RC -Identity user@contoso.com -TargetDeliveryDomain <YourAppropriateDomain>
   ```

5. <span data-ttu-id="3df08-192">Répétez l’étape 4 pour chaque boîte aux lettres à migrer d’Exchange sur site vers l’emplacement géographique satellite auquel vous êtes actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="3df08-192">Repeat step #4 for every mailbox you need to migrate from on-premises Exchange to the satellite geo location you are currently connected to.</span></span>

6. <span data-ttu-id="3df08-193">Si vous devez migrer des boîtes aux lettres supplémentaires vers un autre emplacement géographique satellite, répétez les étapes 2 à 4 pour chaque emplacement spécifique.</span><span class="sxs-lookup"><span data-stu-id="3df08-193">If you need to migrate additional mailboxes to different satellite geo locations, repeat steps 2 through 4 for each specific location.</span></span>

## <a name="multi-geo-reporting"></a><span data-ttu-id="3df08-194">Génération de rapports multigéographiques</span><span class="sxs-lookup"><span data-stu-id="3df08-194">Multi-geo reporting</span></span>

<span data-ttu-id="3df08-195">Les **rapports d’utilisation multigéographique** dans le Centre d’administration Microsoft 365 affichent le nombre d’utilisateurs par emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="3df08-195">**Multi-Geo Usage Reports** in the Microsoft 365 admin center displays the user count by geo location.</span></span> <span data-ttu-id="3df08-196">Le rapport présente la répartition des utilisateurs pour le mois en cours et les données historiques des 6 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="3df08-196">The report displays user distribution for the current month and provides historical data for the past 6 months.</span></span>

## <a name="see-also"></a><span data-ttu-id="3df08-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3df08-197">See also</span></span>

[<span data-ttu-id="3df08-198">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="3df08-198">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
