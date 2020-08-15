---
title: Ajouter un domaine à une location de client avec Windows PowerShell pour les partenaires DAP
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- M365-subscription-management
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.assetid: f49b4d24-9aa0-48a6-95dd-6bae9cf53d2c
description: 'Résumé : utilisez PowerShell pour Microsoft 365 pour ajouter un autre nom de domaine à un client existant.'
ms.openlocfilehash: 23137d2e2461e75a22d0403f9b8246a29e48019f
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690195"
---
# <a name="add-a-domain-to-a-client-tenancy-with-windows-powershell-for-delegated-access-permission-dap-partners"></a><span data-ttu-id="9cfe9-103">Ajout d’un domaine à la location d’un client avec Windows PowerShell pour les partenaires avec autorisation d’accès délégué</span><span class="sxs-lookup"><span data-stu-id="9cfe9-103">Add a domain to a client tenancy with Windows PowerShell for Delegated Access Permission (DAP) partners</span></span>

<span data-ttu-id="9cfe9-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="9cfe9-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="9cfe9-105">Vous pouvez créer et associer de nouveaux domaines à la location de votre client avec PowerShell pour Microsoft 365 plus rapidement que d’utiliser le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-105">You can create and associate new domains with your customer's tenancy with PowerShell for Microsoft 365 faster than using the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="9cfe9-106">Les partenaires avec autorisation d'accès délégué sont les partenaires de syndication et fournisseurs de solutions cloud.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-106">Delegated Access Permission (DAP) partners are Syndication and Cloud Solution Providers (CSP) Partners.</span></span> <span data-ttu-id="9cfe9-107">Il s’agit souvent de fournisseurs de réseau ou de télécommunication pour d’autres sociétés.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-107">They are frequently network or telecom providers to other companies.</span></span> <span data-ttu-id="9cfe9-108">Ils regroupent les abonnements Microsoft 365 dans leurs offres de service à leurs clients.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-108">They bundle Microsoft 365 subscriptions into their service offerings to their customers.</span></span> <span data-ttu-id="9cfe9-109">Lors de la vente d’un abonnement Microsoft 365, les autorisations d’administration pour le compte de (administrateur) sont automatiquement accordées aux clients pour qu’ils puissent administrer et rendre compte des locations des clients.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-109">When they sell a Microsoft 365 subscription, they are automatically granted Administer On Behalf Of (AOBO) permissions to the customer tenancies so they can administer and report on the customer tenancies.</span></span>
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9cfe9-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9cfe9-110">What do you need to know before you begin?</span></span>

<span data-ttu-id="9cfe9-111">Les procédures décrites dans cette rubrique vous obligent à vous connecter à [Microsoft 365 avec PowerShell](connect-to-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="9cfe9-111">The procedures in this topic require you to connect to [Connect to Microsoft 365 with PowerShell](connect-to-microsoft-365-powershell.md).</span></span>
  
<span data-ttu-id="9cfe9-112">Vous avez aussi besoin des informations d’identification d’administrateur de la location du partenaire.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-112">You also need your partner tenant administrator credentials.</span></span>
  
<span data-ttu-id="9cfe9-113">Vous avez également besoin des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cfe9-113">You also need the following information:</span></span>
  
- <span data-ttu-id="9cfe9-114">Vous avez besoin du nom de domaine complet (FQDN) que votre client souhaite utiliser.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-114">You need the fully qualified domain name (FQDN) that your customer wants.</span></span>
    
- <span data-ttu-id="9cfe9-115">Vous avez besoin du code **TenantID** du client.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-115">You need the customer's **TenantId**.</span></span>
    
- <span data-ttu-id="9cfe9-p102">Le nom de domaine complet doit être enregistré auprès d'un bureau d'enregistrement de domaines DNS Internet, comme GoDaddy. Pour plus d'informations sur l'inscription publique d'un nom de domaine, voir [Comment acheter un nom de domaine](https://go.microsoft.com/fwlink/p/?LinkId=532541).</span><span class="sxs-lookup"><span data-stu-id="9cfe9-p102">The FQDN must be registered with an Internet domain name service (DNS) registrar, such as GoDaddy. For more information on how to publically register a domain name, see [How to buy a domain name](https://go.microsoft.com/fwlink/p/?LinkId=532541).</span></span>
    
- <span data-ttu-id="9cfe9-118">Vous devez savoir comment ajouter un enregistrement TXT à la zone DNS enregistrée pour votre bureau d’enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-118">You need to know how to add a TXT record to the registered DNS zone for your DNS registrar.</span></span> <span data-ttu-id="9cfe9-119">Pour plus d’informations sur l’ajout d’un enregistrement TXT, consultez la rubrique [Ajouter des enregistrements DNS pour connecter votre domaine](https://go.microsoft.com/fwlink/p/?LinkId=532542).</span><span class="sxs-lookup"><span data-stu-id="9cfe9-119">For more information on how to add a TXT record, see [Add DNS records to connect your domain](https://go.microsoft.com/fwlink/p/?LinkId=532542).</span></span> <span data-ttu-id="9cfe9-120">Si ces procédures ne fonctionnent pas pour vous, vous devez rechercher les procédures pour votre bureau d’enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-120">If those procedures don't work for you, you will need to find the procedures for your DNS registrar.</span></span>
    
## <a name="create-domains"></a><span data-ttu-id="9cfe9-121">Création de domaines</span><span class="sxs-lookup"><span data-stu-id="9cfe9-121">Create domains</span></span>

 <span data-ttu-id="9cfe9-p104">Vos clients vous demanderont probablement de créer des domaines supplémentaires à associer à leur location, car ils ne voudront probablement pas que le domaine<domain>.onmicrosoft.comsoit le domaine principal qui représente leur identité d'entreprise aux yeux du monde entier. Cette procédure vous guide au fil du processus de création d'un domaine associé à la location de votre client.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-p104">Your customers will likely ask you to create additional domains to associate with their tenancy because they don't want the default <domain>.onmicrosoft.com domain to be the primary one that represents their corporate identities to the world. This procedure walks you through creating a new domain associated with your customer's tenancy.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9cfe9-124">Pour effectuer certaines de ces opérations, le compte d’administrateur partenaire avec lequel vous vous connectez doit être défini sur **administration complète** pour le paramètre **attribuer un accès administratif aux sociétés que vous prenez en charge** figurant dans les détails du compte administrateur dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-124">To perform some of these operations, the partner administrator account you sign in with must be set to **Full administration** for the **Assign administrative access to companies you support** setting found in the details of the admin account in the Microsoft 365 admin center.</span></span> <span data-ttu-id="9cfe9-125">Pour plus d’informations sur la gestion des rôles d’administrateur partenaire, consultez la rubrique [partenaires : proposer une administration déléguée](https://go.microsoft.com/fwlink/p/?LinkId=532435).</span><span class="sxs-lookup"><span data-stu-id="9cfe9-125">For more information on managing partner administrator roles, see [Partners: Offer delegated administration](https://go.microsoft.com/fwlink/p/?LinkId=532435).</span></span> 
  
### <a name="create-the-domain-in-azure-active-directory"></a><span data-ttu-id="9cfe9-126">Création du domaine dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9cfe9-126">Create the domain in Azure Active Directory</span></span>

<span data-ttu-id="9cfe9-127">Cette commande crée le domaine dans Azure Active Directory, mais ne l'associe pas au domaine inscrit publiquement.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-127">This command creates the domain in Azure Active Directory but does not associate it with the publicly registered domain.</span></span> <span data-ttu-id="9cfe9-128">Cela vient lorsque vous prouvez que vous êtes propriétaire du domaine inscrit publiquement à Microsoft Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-128">That comes when you prove that you own the publicly registered domain to Microsoft Microsoft 365 for enterprises.</span></span>
  
```powershell
New-MsolDomain -TenantId <customer TenantId> -Name <FQDN of new domain>
```

>[!Note]
><span data-ttu-id="9cfe9-129">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-129">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="9cfe9-130">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-130">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

### <a name="get-the-data-for-the-dns-txt-verification-record"></a><span data-ttu-id="9cfe9-131">Obtention des données pour l’enregistrement de vérification TXT DNS</span><span class="sxs-lookup"><span data-stu-id="9cfe9-131">Get the data for the DNS TXT verification record</span></span>

 <span data-ttu-id="9cfe9-132">Microsoft 365 générera les données spécifiques que vous devez placer dans l’enregistrement de vérification TXT DNS.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-132">Microsoft 365 will generate the specific data that you need to place into the DNS TXT verification record.</span></span> <span data-ttu-id="9cfe9-133">Pour obtenir les données, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-133">To get the data, run this command.</span></span>
  
```powershell
Get-MsolDomainVerificationDNS -TenantId <customer TenantId> -DomainName <FQDN of new domain> -Mode DnsTxtRecord
```

<span data-ttu-id="9cfe9-134">Elle vous fournira des résultats semblables à :</span><span class="sxs-lookup"><span data-stu-id="9cfe9-134">This will give you output like:</span></span>
  
 `Label: domainname.com`
  
 `Text: MS=ms########`
  
 `Ttl: 3600`
  
> [!NOTE]
> <span data-ttu-id="9cfe9-135">Vous aurez besoin de ce texte pour créer l'enregistrement TXT dans la zone DNS enregistrée publiquement.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-135">You will need this text to create the TXT record in the publicly registered DNS zone.</span></span> <span data-ttu-id="9cfe9-136">Copiez-le et enregistrez-le.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-136">Be sure to copy and save it.</span></span> 
  
### <a name="add-a-txt-record-to-the-publically-registered-dns-zone"></a><span data-ttu-id="9cfe9-137">Ajout d’un enregistrement TXT à la zone DNS enregistrée publiquement</span><span class="sxs-lookup"><span data-stu-id="9cfe9-137">Add a TXT record to the publically registered DNS zone</span></span>

<span data-ttu-id="9cfe9-138">Avant que Microsoft 365 n’accepte le trafic qui est dirigé vers le nom de domaine enregistré publiquement, vous devez prouver que vous êtes propriétaire du domaine et que vous disposez d’autorisations d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-138">Before Microsoft 365 will start accepting traffic that is directed to the publicly registered domain name, you must prove that you own and have administrator permissions to the domain.</span></span> <span data-ttu-id="9cfe9-139">Pour prouver que vous êtes propriétaire du domaine, créez un enregistrement TXT dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-139">You prove you own the domain by creating a TXT record in the domain.</span></span> <span data-ttu-id="9cfe9-140">Un enregistrement TXT n'a aucun effet sur votre domaine, et il peut être supprimé une fois qu'il est établi que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-140">A TXT record doesn't do anything in your domain, and it can be deleted after your ownership of the domain is established.</span></span> <span data-ttu-id="9cfe9-141">Pour créer les enregistrements TXT, suivez les procédures de la rubrique [Ajouter des enregistrements DNS pour connecter votre domaine](https://go.microsoft.com/fwlink/p/?LinkId=532542).</span><span class="sxs-lookup"><span data-stu-id="9cfe9-141">To create the TXT records, follow the procedures at [Add DNS records to connect your domain](https://go.microsoft.com/fwlink/p/?LinkId=532542).</span></span> <span data-ttu-id="9cfe9-142">Si ces procédures ne fonctionnent pas pour vous, vous devez rechercher les procédures pour votre bureau d'enregistrement DNS.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-142">If those procedures don't work for you , you need to find the procedures for your DNS registrar.</span></span>
  
<span data-ttu-id="9cfe9-p111">Confirmez la création de l'enregistrement TXT via nslookup. Suivez cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-p111">Confirm the successful creation of the TXT record via nslookup. Follow this syntax.</span></span>
  
```console
nslookup -type=TXT <FQDN of registered domain>
```

<span data-ttu-id="9cfe9-145">Elle vous fournira des résultats semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="9cfe9-145">This will give you output like:</span></span>
  
 `Non-authoritative answer:`
  
 `FQDN of the registered domain`
  
 `text=MS=ms########`
  
### <a name="validate-domain-ownership-in-microsoft-365"></a><span data-ttu-id="9cfe9-146">Valider la propriété de domaine dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9cfe9-146">Validate domain ownership in Microsoft 365</span></span>

<span data-ttu-id="9cfe9-147">Dans cette dernière étape, vous validez auprès de Microsoft 365 que vous êtes propriétaire du domaine inscrit publiquement.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-147">In this last step, you validate to Microsoft 365 that you own the publically registered domain.</span></span> <span data-ttu-id="9cfe9-148">Après cette étape, Microsoft 365 commencera à accepter le trafic acheminé vers le nouveau nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-148">After this step, Microsoft 365 will begin accepting traffic routed to the new domain name.</span></span> <span data-ttu-id="9cfe9-149">Pour terminer la création du domaine et le processus d’inscription, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-149">To complete the domain creation and registration process, run this command.</span></span> 
  
```powershell
Confirm-MsolDomain -TenantId <customer TenantId> -DomainName <FQDN of new domain>
```

<span data-ttu-id="9cfe9-150">Cette commande ne renvoie aucun résultat, par conséquent, pour vérifier qu’elle a fonctionné, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-150">This command won't return any output, so to confirm that this worked, run this command.</span></span>
  
```powershell
Get-MsolDomain -TenantId <customer TenantId> -DomainName <FQDN of new domain>
```

<span data-ttu-id="9cfe9-151">Celle-ci renverra des résultats semblables à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-151">This will return something like this</span></span>

```console
Name                   Status      Authentication
--------------------   ---------   --------------
FQDN of new domain     Verified    Managed
```

   
## <a name="see-also"></a><span data-ttu-id="9cfe9-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cfe9-152">See also</span></span>

#### 

[<span data-ttu-id="9cfe9-153">Aide pour les partenaires</span><span class="sxs-lookup"><span data-stu-id="9cfe9-153">Help for partners</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=533477)

