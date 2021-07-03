---
title: Comment configurer Skype Entreprise en local pour utiliser l’authentification moderne hybride
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 12/3/2019
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 522d5cec-4e1b-4cc3-937f-293570717bc6
ms.collection:
- M365-security-compliance
f1.keywords:
- NOCSH
description: Découvrez comment configurer l Skype Entreprise local pour utiliser l’authentification moderne hybride (HMA), ce qui vous offre une authentification et une autorisation utilisateur plus sécurisées.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 9695815d0a085931b10f7f64b9fca2e997af9077
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53286056"
---
# <a name="how-to-configure-skype-for-business-on-premises-to-use-hybrid-modern-authentication"></a><span data-ttu-id="0bdfc-103">Comment configurer Skype Entreprise en local pour utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="0bdfc-103">How to configure Skype for Business on-premises to use Hybrid Modern Authentication</span></span>

<span data-ttu-id="0bdfc-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="0bdfc-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="0bdfc-105">L’authentification moderne, qui est une méthode de gestion des identités qui offre une authentification et une autorisation utilisateur plus sécurisées, est disponible pour les environnements hybrides Skype Entreprise serveur local et serveur Exchange, ainsi que pour les environnements Skype Entreprise partagés.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-105">Modern Authentication, is a method of identity management that offers more secure user authentication and authorization, is available for Skype for Business server on-premises and Exchange server on-premises, and split-domain Skype for Business hybrids.</span></span>

 <span data-ttu-id="0bdfc-106">**Important** Voulez-vous en savoir plus sur l’authentification moderne (MA) et pourquoi préférer l’utiliser dans votre entreprise ou organisation ?</span><span class="sxs-lookup"><span data-stu-id="0bdfc-106">**Important** Would you like to know more about Modern Authentication (MA) and why you might prefer to use it in your company or organization?</span></span> <span data-ttu-id="0bdfc-107">Consultez [ce document](hybrid-modern-auth-overview.md) pour obtenir une vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-107">Check [this document](hybrid-modern-auth-overview.md) for an overview.</span></span> <span data-ttu-id="0bdfc-108">Si vous avez besoin de savoir quelles topologies Skype Entreprise sont pris en charge avec MA, cela est documenté ici !</span><span class="sxs-lookup"><span data-stu-id="0bdfc-108">If you need to know what Skype for Business topologies are supported with MA, that's documented here!</span></span>

 <span data-ttu-id="0bdfc-109">**Avant de commencer,** j’utilise les termes ci-après :</span><span class="sxs-lookup"><span data-stu-id="0bdfc-109">**Before we begin**, I use these terms:</span></span>

- <span data-ttu-id="0bdfc-110">Authentification moderne (MA)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-110">Modern Authentication (MA)</span></span>

- <span data-ttu-id="0bdfc-111">Authentification moderne hybride (HMA)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-111">Hybrid Modern Authentication (HMA)</span></span>

- <span data-ttu-id="0bdfc-112">Exchange local (EXCH)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-112">Exchange on-premises (EXCH)</span></span>

- <span data-ttu-id="0bdfc-113">Exchange Online (EXO)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-113">Exchange Online (EXO)</span></span>

- <span data-ttu-id="0bdfc-114">Skype Entreprise local (SFB)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-114">Skype for Business on-premises (SFB)</span></span>

- <span data-ttu-id="0bdfc-115">Skype Entreprise Online (SFBO)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-115">Skype for Business Online (SFBO)</span></span>

<span data-ttu-id="0bdfc-116">En outre, si un graphique de cet article possède un objet grisé ou est grisé, cela signifie que l’élément affiché en gris **n’est** pas inclus dans la configuration propre à MA.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-116">Also, if a graphic in this article has an object that's grayed-out or dimmed that means the element shown in gray **isn't** included in MA-specific configuration.</span></span>

## <a name="read-the-summary"></a><span data-ttu-id="0bdfc-117">Lire le résumé</span><span class="sxs-lookup"><span data-stu-id="0bdfc-117">Read the summary</span></span>

<span data-ttu-id="0bdfc-118">Ce résumé décompose le processus en étapes qui pourraient sinon être perdues pendant l’exécution et est utile pour qu’une liste de contrôle globale puisse suivre l’endroit où vous vous trouvez dans le processus.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-118">This summary breaks down the process into steps that might otherwise get lost during the execution, and is good for an overall checklist to keep track of where you are in the process.</span></span>

1. <span data-ttu-id="0bdfc-119">Tout d’abord, assurez-vous que vous répondez à toutes les conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-119">First, make sure you meet all the prerequisites.</span></span>

1. <span data-ttu-id="0bdfc-120">Étant donné que **de nombreux** éléments prérequis sont courants pour Skype Entreprise et Exchange, consultez l’article de vue d’ensemble de votre liste de contrôle préalable à [la req.](hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-120">Since many **prerequisites** are common for both Skype for Business and Exchange, [see the overview article for your pre-req checklist](hybrid-modern-auth-overview.md).</span></span> <span data-ttu-id="0bdfc-121">Faites-le  *avant de*  commencer l’une des étapes de cet article.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-121">Do this  *before*  you begin any of the steps in this article.</span></span>

1. <span data-ttu-id="0bdfc-122">Collectez les informations spécifiques à HMA dont vous aurez besoin dans un fichier ou OneNote.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-122">Collect the HMA-specific info you'll need in a file, or OneNote.</span></span>

1. <span data-ttu-id="0bdfc-123">Activer l’authentification moderne pour EXO (si elle n’est pas déjà allumée).</span><span class="sxs-lookup"><span data-stu-id="0bdfc-123">Turn ON Modern Authentication for EXO (if it isn't already turned on).</span></span>

1. <span data-ttu-id="0bdfc-124">Activer l’authentification moderne pour SFBO (si elle n’est pas déjà allumée).</span><span class="sxs-lookup"><span data-stu-id="0bdfc-124">Turn ON Modern Authentication for SFBO (if it isn't already turned on).</span></span>

1. <span data-ttu-id="0bdfc-125">Activer l’authentification moderne hybride Exchange local.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-125">Turn ON Hybrid Modern Authentication for Exchange on-premises.</span></span>

1. <span data-ttu-id="0bdfc-126">Activer l’authentification moderne hybride Skype Entreprise en local.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-126">Turn ON Hybrid Modern Authentication for Skype for Business on-premises.</span></span>

<span data-ttu-id="0bdfc-127">Ces étapes allument MA pour SFB, SFBO, EXCH et EXO, c’est-à-dire tous les produits qui peuvent participer à une configuration HMA de SFB et SFBO (y compris les dépendances sur EXCH/EXO).</span><span class="sxs-lookup"><span data-stu-id="0bdfc-127">These steps turn on MA for SFB, SFBO, EXCH, and EXO - that is, all the products that can participate in an HMA configuration of SFB and SFBO (including dependencies on EXCH/EXO).</span></span> <span data-ttu-id="0bdfc-128">En d’autres termes, si vos utilisateurs sont des boîtes aux lettres d’accueil ou ont été créées dans une partie de l’hybride (EXO + SFBO, EXO + SFB, EXCH + SFBO ou EXCH + SFB), votre produit terminé ressemblera à ceci :</span><span class="sxs-lookup"><span data-stu-id="0bdfc-128">In other words, if your users are homed in/have mailboxes created in any part of the Hybrid (EXO + SFBO, EXO + SFB, EXCH + SFBO, or EXCH + SFB), your finished product will look like this:</span></span>

![Une topologie HMA mixte 6 Skype pour les entreprises dispose d’une topologie MA dans les quatre emplacements possibles.](../media/ab89cdf2-160b-49ac-9b71-0160800acfc8.png)

<span data-ttu-id="0bdfc-130">Comme vous pouvez le constater, il existe quatre endroits différents pour activer MA !</span><span class="sxs-lookup"><span data-stu-id="0bdfc-130">As you can see there are four different places to turn on MA!</span></span> <span data-ttu-id="0bdfc-131">Pour une expérience utilisateur de qualité, nous vous recommandons d’activer MA aux quatre emplacements ci-après.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-131">For the best user experience, we recommend you turn on MA in all four of these locations.</span></span> <span data-ttu-id="0bdfc-132">Si vous ne pouvez pas activer MA à tous ces emplacements, ajustez les étapes afin d’activer MA uniquement dans les emplacements nécessaires pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-132">If you can't turn MA on in all these locations, adjust the steps so that you turn on MA only in the locations that are necessary for your environment.</span></span>

<span data-ttu-id="0bdfc-133">Consultez la [rubrique Prise en charge de Skype Entreprise avec MA](/skypeforbusiness/plan-your-deployment/modern-authentication/topologies-supported) pour les topologies pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-133">See the [Supportability topic for Skype for Business with MA](/skypeforbusiness/plan-your-deployment/modern-authentication/topologies-supported) for supported topologies.</span></span>

 <span data-ttu-id="0bdfc-134">**Important** Vérifiez que toutes les conditions préalables sont remplies avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-134">**Important** Double-check that you've met all the prerequisites before you begin.</span></span> <span data-ttu-id="0bdfc-135">Vous trouverez ces informations dans la vue d’ensemble de l’authentification moderne hybride [et les conditions préalables.](hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-135">You'll find that information in [Hybrid modern authentication overview and prerequisites](hybrid-modern-auth-overview.md).</span></span>

## <a name="collect-all-hma-specific-info-youll-need"></a><span data-ttu-id="0bdfc-136">Collectez toutes les informations propres à HMA dont vous aurez besoin</span><span class="sxs-lookup"><span data-stu-id="0bdfc-136">Collect all HMA-specific info you'll need</span></span>

<span data-ttu-id="0bdfc-137">Une fois que vous avez vérifié que vous répondez aux conditions [préalables](hybrid-modern-auth-overview.md) à l’utilisation de l’authentification moderne (voir la remarque ci-dessus), vous devez créer un fichier pour contenir les informations dont vous aurez besoin pour configurer HMA dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-137">After you've double-checked that you meet the [prerequisites](hybrid-modern-auth-overview.md) to use Modern Authentication (see the note above), you should create a file to hold the info you'll need for configuring HMA in the steps ahead.</span></span> <span data-ttu-id="0bdfc-138">Exemples utilisés dans cet article :</span><span class="sxs-lookup"><span data-stu-id="0bdfc-138">Examples used in this article:</span></span>

- <span data-ttu-id="0bdfc-139">**Domaine SIP/SMTP**</span><span class="sxs-lookup"><span data-stu-id="0bdfc-139">**SIP/SMTP domain**</span></span>

  - <span data-ttu-id="0bdfc-140">Ex.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-140">Ex.</span></span> <span data-ttu-id="0bdfc-141">contoso.com (fédéré avec Office 365)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-141">contoso.com (is federated with Office 365)</span></span>

- <span data-ttu-id="0bdfc-142">**ID client**</span><span class="sxs-lookup"><span data-stu-id="0bdfc-142">**Tenant ID**</span></span>

  - <span data-ttu-id="0bdfc-143">GUID qui représente votre client Office 365 client (à la connexion de contoso.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="0bdfc-143">The GUID that represents your Office 365 tenant (at the login of contoso.onmicrosoft.com).</span></span>

- <span data-ttu-id="0bdfc-144">**URL de service Web CU5 SFB 2015**</span><span class="sxs-lookup"><span data-stu-id="0bdfc-144">**SFB 2015 CU5 Web Service URLs**</span></span>

<span data-ttu-id="0bdfc-145">Vous aurez besoin d’URL de service web interne et externe pour tous les pools SfB 2015 déployés.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-145">you'll need internal and external web service URLs for all SfB 2015 pools deployed.</span></span> <span data-ttu-id="0bdfc-146">Pour les obtenir, exécutez la liste suivante à partir Skype Entreprise Management Shell :</span><span class="sxs-lookup"><span data-stu-id="0bdfc-146">To obtain these, run the following from Skype for Business Management Shell:</span></span>

```powershell
Get-CsService -WebServer | Select-Object PoolFqdn, InternalFqdn, ExternalFqdn | FL
```

- <span data-ttu-id="0bdfc-147">Ex.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-147">Ex.</span></span> <span data-ttu-id="0bdfc-148">Interne : https://lyncwebint01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0bdfc-148">Internal: https://lyncwebint01.contoso.com</span></span>

- <span data-ttu-id="0bdfc-149">Ex.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-149">Ex.</span></span> <span data-ttu-id="0bdfc-150">Externe : https://lyncwebext01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0bdfc-150">External: https://lyncwebext01.contoso.com</span></span>

<span data-ttu-id="0bdfc-151">Si vous utilisez un serveur Édition Standard, l’URL interne est vide.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-151">If you're using a Standard Edition server, the internal URL will be blank.</span></span> <span data-ttu-id="0bdfc-152">Dans ce cas, utilisez le fqdn du pool pour l’URL interne.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-152">In this case, use the pool fqdn for the internal URL.</span></span>

## <a name="turn-on-modern-authentication-for-exo"></a><span data-ttu-id="0bdfc-153">Activer l’authentification moderne pour EXO</span><span class="sxs-lookup"><span data-stu-id="0bdfc-153">Turn on Modern Authentication for EXO</span></span>

<span data-ttu-id="0bdfc-154">Suivez les instructions ci-après [: Exchange Online : comment activer votre client pour l’authentification moderne.](https://social.technet.microsoft.com/wiki/contents/articles/32711.exchange-online-how-to-enable-your-tenant-for-modern-authentication.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-154">Follow the instructions here: [Exchange Online: How to enable your tenant for modern authentication.](https://social.technet.microsoft.com/wiki/contents/articles/32711.exchange-online-how-to-enable-your-tenant-for-modern-authentication.aspx)</span></span>

## <a name="turn-on-modern-authentication-for-sfbo"></a><span data-ttu-id="0bdfc-155">Activer l’authentification moderne pour SFBO</span><span class="sxs-lookup"><span data-stu-id="0bdfc-155">Turn on Modern Authentication for SFBO</span></span>

<span data-ttu-id="0bdfc-156">Suivez les instructions ci-après [: Skype Entreprise Online : activer votre client pour l’authentification moderne.](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-156">Follow the instructions here: [Skype for Business Online: Enable your tenant for modern authentication](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx).</span></span>

## <a name="turn-on-hybrid-modern-authentication-for-exchange-on-premises"></a><span data-ttu-id="0bdfc-157">Activer l’authentification moderne hybride pour Exchange local</span><span class="sxs-lookup"><span data-stu-id="0bdfc-157">Turn on Hybrid Modern Authentication for Exchange on-premises</span></span>

<span data-ttu-id="0bdfc-158">Suivez les instructions ci-après : Comment configurer Exchange Server [local pour utiliser l’authentification moderne hybride](configure-exchange-server-for-hybrid-modern-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="0bdfc-158">Follow the instructions here: [How to configure Exchange Server on-premises to use Hybrid Modern Authentication](configure-exchange-server-for-hybrid-modern-authentication.md).</span></span>

## <a name="turn-on-hybrid-modern-authentication-for-skype-for-business-on-premises"></a><span data-ttu-id="0bdfc-159">Activer l’authentification moderne hybride pour Skype Entreprise local</span><span class="sxs-lookup"><span data-stu-id="0bdfc-159">Turn on Hybrid Modern Authentication for Skype for Business on-premises</span></span>

### <a name="add-on-premises-web-service-urls-as-spns-in-azure-active-directory"></a><span data-ttu-id="0bdfc-160">Ajouter des URL de service web local en tant que SNS dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0bdfc-160">Add on-premises web service URLs as SPNs in Azure Active Directory</span></span>

<span data-ttu-id="0bdfc-161">Vous devez maintenant exécuter des commandes pour ajouter les URL (collectées précédemment) en tant que principaux de service dans SFBO.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-161">Now you'll need to run commands to add the URLs (collected earlier) as Service Principals in SFBO.</span></span>

 <span data-ttu-id="0bdfc-162">**Remarque** Les noms principaux de service (SSN) identifient les services web et les associent à un principal de sécurité (par exemple, un nom de compte ou un groupe) afin que le service puisse agir au nom d’un utilisateur autorisé.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-162">**Note** Service principal names (SPNs) identify web services and associate them with a security principal (such as an account name or group) so that the service can act on the behalf of an authorized user.</span></span> <span data-ttu-id="0bdfc-163">Les clients qui s’authentifier sur un serveur utilisent les informations contenues dans les SNS.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-163">Clients authenticating to a server make use of information that's contained in SPNs.</span></span>

1. <span data-ttu-id="0bdfc-164">Tout d’abord, connectez-Azure Active Directory (Azure AD) [avec ces instructions.](/powershell/azure/active-directory/overview)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-164">First, connect to Azure Active Directory (Azure AD) with [these instructions](/powershell/azure/active-directory/overview).</span></span>

2. <span data-ttu-id="0bdfc-165">Exécutez cette commande, en local, pour obtenir la liste des URL de service web SFB.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-165">Run this command, on-premises, to get a list of SFB web service URLs.</span></span>

   <span data-ttu-id="0bdfc-166">Notez que l’AppPrincipalId commence par `00000004` .</span><span class="sxs-lookup"><span data-stu-id="0bdfc-166">Note that the AppPrincipalId begins with `00000004`.</span></span> <span data-ttu-id="0bdfc-167">Cela correspond à Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-167">This corresponds to Skype for Business Online.</span></span>

   <span data-ttu-id="0bdfc-168">Prenez note (et capture d’écran pour comparaison ultérieure) de la sortie de cette commande, qui inclut un SE et une URL WS, mais se compose principalement de SNS qui commencent par `00000004-0000-0ff1-ce00-000000000000/` .</span><span class="sxs-lookup"><span data-stu-id="0bdfc-168">Take note of (and screenshot for later comparison) the output of this command, which will include an SE and WS URL, but mostly consist of SPNs that begin with `00000004-0000-0ff1-ce00-000000000000/`.</span></span>

```powershell
Get-MsolServicePrincipal -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000 | Select -ExpandProperty ServicePrincipalNames
```

3. <span data-ttu-id="0bdfc-169">Si les **URL** SFB internes ou externes de l’environnement local sont manquantes (par exemple, nous devons ajouter ces enregistrements spécifiques https://lyncwebint01.contoso.com à cette https://lyncwebext01.contoso.com) liste).</span><span class="sxs-lookup"><span data-stu-id="0bdfc-169">If the internal **or** external SFB URLs from on-premises are missing (for example, https://lyncwebint01.contoso.com and https://lyncwebext01.contoso.com) we will need to add those specific records to this list.</span></span>

    <span data-ttu-id="0bdfc-170">N’oubliez pas  *de remplacer les exemples d’URL* ci-dessous par vos URL réelles dans les commandes Ajouter !</span><span class="sxs-lookup"><span data-stu-id="0bdfc-170">Be sure to replace  *the example URLs* below with your actual URLs in the Add commands!</span></span>

```powershell
$x= Get-MsolServicePrincipal -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000
$x.ServicePrincipalnames.Add("https://lyncwebint01.contoso.com/")
$x.ServicePrincipalnames.Add("https://lyncwebext01.contoso.com/")
Set-MSOLServicePrincipal -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000 -ServicePrincipalNames $x.ServicePrincipalNames
```

4. <span data-ttu-id="0bdfc-171">Vérifiez que vos nouveaux enregistrements ont été ajoutés en exécutant à nouveau la commande **Get-MsolServicePrincipal** de l’étape 2 et en regardant la sortie.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-171">Verify your new records were added by running the **Get-MsolServicePrincipal** command from step 2 again, and looking through the output.</span></span> <span data-ttu-id="0bdfc-172">Comparez la liste ou la capture d’écran d’avant à la nouvelle liste de SSN.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-172">Compare the list or screenshot from before to the new list of SPNs.</span></span> <span data-ttu-id="0bdfc-173">Vous pouvez également faire une capture d’écran de la nouvelle liste pour vos enregistrements.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-173">You might also screenshot the new list for your records.</span></span> <span data-ttu-id="0bdfc-174">Si vous avez réussi, vous verrez les deux nouvelles URL dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-174">If you were successful, you'll see the two new URLs in the list.</span></span> <span data-ttu-id="0bdfc-175">En suivant notre exemple, la liste des SNS inclut désormais les URL spécifiques https://lyncwebint01.contoso.com et https://lyncwebext01.contoso.com/ .</span><span class="sxs-lookup"><span data-stu-id="0bdfc-175">Going by our example, the list of SPNs will now include the specific URLs https://lyncwebint01.contoso.com and https://lyncwebext01.contoso.com/.</span></span>

### <a name="create-the-evosts-auth-server-object"></a><span data-ttu-id="0bdfc-176">Créer l’objet serveur DNS EvoSTS</span><span class="sxs-lookup"><span data-stu-id="0bdfc-176">Create the EvoSTS Auth Server Object</span></span>

<span data-ttu-id="0bdfc-177">Exécutez la commande suivante dans Skype Entreprise Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-177">Run the following command in the Skype for Business Management Shell.</span></span>

```powershell
New-CsOAuthServer -Identity evoSTS -MetadataURL https://login.windows.net/common/FederationMetadata/2007-06/FederationMetadata.xml -AcceptSecurityIdentifierInformation $true -Type AzureAD
```

### <a name="enable-hybrid-modern-authentication"></a><span data-ttu-id="0bdfc-178">Activer l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="0bdfc-178">Enable Hybrid Modern Authentication</span></span>

<span data-ttu-id="0bdfc-179">Il s’agit de l’étape qui allume ma.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-179">This is the step that actually turns on MA.</span></span> <span data-ttu-id="0bdfc-180">Toutes les étapes précédentes peuvent être exécutés à l’avance sans modifier le flux d’authentification client.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-180">All the previous steps can be run ahead of time without changing the client authentication flow.</span></span> <span data-ttu-id="0bdfc-181">Lorsque vous êtes prêt à modifier le flux d’authentification, exécutez cette commande dans Skype Entreprise Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-181">When you're ready to change the authentication flow, run this command in the Skype for Business Management Shell.</span></span>

```powershell
Set-CsOAuthConfiguration -ClientAuthorizationOAuthServerIdentity evoSTS
```

## <a name="verify"></a><span data-ttu-id="0bdfc-182">Vérifier</span><span class="sxs-lookup"><span data-stu-id="0bdfc-182">Verify</span></span>

<span data-ttu-id="0bdfc-183">Une fois que vous avez activé HMA, la connexion suivante d’un client utilise le nouveau flux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-183">Once you enable HMA, a client's next login will use the new auth flow.</span></span> <span data-ttu-id="0bdfc-184">Notez que le simple fait d’allumer HMA ne déclenche pas de réauthentication pour un client.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-184">Note that just turning on HMA won't trigger a reauthentication for any client.</span></span> <span data-ttu-id="0bdfc-185">Les clients se réauthentent en fonction de la durée de vie des jetons d’th et/ou des jetons dont ils ont.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-185">The clients reauthenticate based on the lifetime of the auth tokens and/or certs they have.</span></span>

<span data-ttu-id="0bdfc-186">Pour tester que HMA fonctionne après l’avoir activé, dé sign out of a test SFB Windows client and be sure to click 'delete my credentials'.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-186">To test that HMA is working after you've enabled it, sign out of a test SFB Windows client and be sure to click 'delete my credentials'.</span></span> <span data-ttu-id="0bdfc-187">Connectez-vous à nouveau.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-187">Sign in again.</span></span> <span data-ttu-id="0bdfc-188">Le client doit maintenant utiliser le flux d’authentification moderne et votre connexion inclura désormais une invite **Office 365** pour un compte professionnel ou scolaire, visible juste avant que le client contacte le serveur et vous connecte.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-188">The client should now use the Modern Auth flow and your login will now include an **Office 365** prompt for a 'Work or school' account, seen right before the client contacts the server and logs you in.</span></span>

<span data-ttu-id="0bdfc-189">Vous devez également vérifier les « Informations de configuration » Skype Entreprise clients pour une « autorité OAuth ».</span><span class="sxs-lookup"><span data-stu-id="0bdfc-189">You should also check the 'Configuration Information' for Skype for Business Clients for an 'OAuth Authority'.</span></span> <span data-ttu-id="0bdfc-190">Pour ce faire sur votre ordinateur client, maintenez la touche Ctrl longue en même temps que vous cliquez avec le bouton droit sur l’icône Skype Entreprise dans la Windows notification.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-190">To do this on your client computer, hold down the CTRL key at the same time you right-click the Skype for Business Icon in the Windows Notification tray.</span></span> <span data-ttu-id="0bdfc-191">Cliquez **sur Informations de** configuration dans le menu qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-191">Click **Configuration Information** in the menu that appears.</span></span> <span data-ttu-id="0bdfc-192">Dans la fenêtre « Skype Entreprise configuration » qui s’affiche sur le Bureau, recherchez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0bdfc-192">In the 'Skype for Business Configuration Information' window that will appear on the desktop, look for the following:</span></span>

![Les informations de configuration d’Skype Entreprise client utilisant l’authentification moderne indiquent une URL d’autorité OAUTH Lync et EWS de https://login.windows.net/common/oauth2/authorize .](../media/4e54edf5-c8f8-4e7f-b032-5d413b0232de.png)

<span data-ttu-id="0bdfc-194">Vous devez également maintenir la touche CTRL en même temps que vous cliquez avec le bouton droit sur l’icône du client Outlook (également dans le bac Windows Notifications) et cliquez sur « État de la connexion ».</span><span class="sxs-lookup"><span data-stu-id="0bdfc-194">You should also hold down the CTRL key at the same time you right-click the icon for the Outlook client (also in the Windows Notifications tray) and click 'Connection Status'.</span></span> <span data-ttu-id="0bdfc-195">Recherchez l’adresse SMTP du client par rapport à un type AuthN de « Bearer » qui représente le jeton du porteur utilisé \* dans OAuth.</span><span class="sxs-lookup"><span data-stu-id="0bdfc-195">Look for the client's SMTP address against an AuthN type of 'Bearer\*', which represents the bearer token used in OAuth.</span></span>

## <a name="related-articles"></a><span data-ttu-id="0bdfc-196">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0bdfc-196">Related articles</span></span>

<span data-ttu-id="0bdfc-197">[Lien vers la vue d’ensemble de l’authentification moderne.](hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-197">[Link back to the Modern Authentication overview](hybrid-modern-auth-overview.md).</span></span>

<span data-ttu-id="0bdfc-198">Avez-vous besoin de savoir comment utiliser l’authentification moderne (ADAL) pour vos clients Skype Entreprise client ?</span><span class="sxs-lookup"><span data-stu-id="0bdfc-198">Do you need to know how to use Modern Authentication (ADAL) for your Skype for Business clients?</span></span> <span data-ttu-id="0bdfc-199">Nous avons des étapes [à suivre ici.](./hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0bdfc-199">We've got steps [here](./hybrid-modern-auth-overview.md).</span></span>