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
description: Découvrez comment configurer Skype entreprise en local pour utiliser l’authentification moderne hybride (HMA) de manière à sécuriser l’authentification et l’autorisation des utilisateurs.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 74c8e3e0514fbfd8779c2f65e9c541c33b281c59
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695011"
---
# <a name="how-to-configure-skype-for-business-on-premises-to-use-hybrid-modern-authentication"></a><span data-ttu-id="e8a44-103">Comment configurer Skype Entreprise en local pour utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="e8a44-103">How to configure Skype for Business on-premises to use Hybrid Modern Authentication</span></span>

<span data-ttu-id="e8a44-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="e8a44-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="e8a44-105">L’authentification moderne est une méthode de gestion des identités qui offre une authentification et une autorisation utilisateur plus sécurisées, est disponible pour Skype entreprise Server local et Exchange Server local, ainsi que pour les hybrides Skype entreprise mixtes.</span><span class="sxs-lookup"><span data-stu-id="e8a44-105">Modern Authentication, is a method of identity management that offers more secure user authentication and authorization, is available for Skype for Business server on-premises and Exchange server on-premises, and split-domain Skype for Business hybrids.</span></span>
  
 <span data-ttu-id="e8a44-106">**Important** Souhaitez-vous en savoir plus sur l’authentification moderne (MA) et pourquoi choisir de l’utiliser dans votre entreprise ou organisation ?</span><span class="sxs-lookup"><span data-stu-id="e8a44-106">**Important** Would you like to know more about Modern Authentication (MA) and why you might prefer to use it in your company or organization?</span></span> <span data-ttu-id="e8a44-107">Pour obtenir une vue d’ensemble, consultez [ce document](hybrid-modern-auth-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a44-107">Check [this document](hybrid-modern-auth-overview.md) for an overview.</span></span> <span data-ttu-id="e8a44-108">Si vous avez besoin de savoir quelles topologies Skype entreprise sont prises en charge avec MA, il est documenté ici.</span><span class="sxs-lookup"><span data-stu-id="e8a44-108">If you need to know what Skype for Business topologies are supported with MA, that's documented here!</span></span>
  
 <span data-ttu-id="e8a44-109">**Avant de commencer**, j’utilise les termes suivants :</span><span class="sxs-lookup"><span data-stu-id="e8a44-109">**Before we begin**, I use these terms:</span></span>
  
- <span data-ttu-id="e8a44-110">Authentification moderne (MA)</span><span class="sxs-lookup"><span data-stu-id="e8a44-110">Modern Authentication (MA)</span></span>

- <span data-ttu-id="e8a44-111">Authentification moderne hybride (HMA)</span><span class="sxs-lookup"><span data-stu-id="e8a44-111">Hybrid Modern Authentication (HMA)</span></span>

- <span data-ttu-id="e8a44-112">Exchange local (EXCH)</span><span class="sxs-lookup"><span data-stu-id="e8a44-112">Exchange on-premises (EXCH)</span></span>

- <span data-ttu-id="e8a44-113">Exchange Online (EXO)</span><span class="sxs-lookup"><span data-stu-id="e8a44-113">Exchange Online (EXO)</span></span>

- <span data-ttu-id="e8a44-114">Skype entreprise en local (SFB)</span><span class="sxs-lookup"><span data-stu-id="e8a44-114">Skype for Business on-premises (SFB)</span></span>

- <span data-ttu-id="e8a44-115">Skype entreprise Online (SFBO)</span><span class="sxs-lookup"><span data-stu-id="e8a44-115">Skype for Business Online (SFBO)</span></span>

<span data-ttu-id="e8a44-116">En outre, si un objet graphique de cet article a un objet grisé ou grisé, cela signifie que l’élément affiché en gris **n’est pas** inclus dans la configuration propre à l’agent de récupération.</span><span class="sxs-lookup"><span data-stu-id="e8a44-116">Also, if a graphic in this article has an object that's grayed-out or dimmed that means the element shown in gray **isn't** included in MA-specific configuration.</span></span>
  
## <a name="read-the-summary"></a><span data-ttu-id="e8a44-117">Lire le résumé</span><span class="sxs-lookup"><span data-stu-id="e8a44-117">Read the summary</span></span>

<span data-ttu-id="e8a44-118">Cette synthèse décompose le processus en étapes qui pourraient autrement se perdre pendant l’exécution, et est utile pour une liste de vérification globale afin d’assurer le suivi de l’endroit où vous vous trouvez dans le processus.</span><span class="sxs-lookup"><span data-stu-id="e8a44-118">This summary breaks down the process into steps that might otherwise get lost during the execution, and is good for an overall checklist to keep track of where you are in the process.</span></span>
  
1. <span data-ttu-id="e8a44-119">Tout d’abord, assurez-vous que vous remplissez toutes les conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="e8a44-119">First, make sure you meet all the prerequisites.</span></span>

1. <span data-ttu-id="e8a44-120">Étant donné que de nombreuses **conditions préalables** sont communes pour Skype entreprise et Exchange, [consultez l’article de vue d’ensemble pour votre liste de vérification pré-req](hybrid-modern-auth-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8a44-120">Since many **prerequisites** are common for both Skype for Business and Exchange, [see the overview article for your pre-req checklist](hybrid-modern-auth-overview.md).</span></span> <span data-ttu-id="e8a44-121">Procédez comme suit  *avant*  de commencer l’une des étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e8a44-121">Do this  *before*  you begin any of the steps in this article.</span></span>

1. <span data-ttu-id="e8a44-122">Collectez les informations propres à la HMA dont vous aurez besoin dans un fichier, ou OneNote.</span><span class="sxs-lookup"><span data-stu-id="e8a44-122">Collect the HMA-specific info you'll need in a file, or OneNote.</span></span>

1. <span data-ttu-id="e8a44-123">Activez l’authentification moderne pour EXO (si elle n’est pas déjà activée).</span><span class="sxs-lookup"><span data-stu-id="e8a44-123">Turn ON Modern Authentication for EXO (if it isn't already turned on).</span></span>

1. <span data-ttu-id="e8a44-124">Activez l’authentification moderne pour SFBO (si elle n’est pas déjà activée).</span><span class="sxs-lookup"><span data-stu-id="e8a44-124">Turn ON Modern Authentication for SFBO (if it isn't already turned on).</span></span>

1. <span data-ttu-id="e8a44-125">Activez l’authentification moderne hybride pour Exchange sur site.</span><span class="sxs-lookup"><span data-stu-id="e8a44-125">Turn ON Hybrid Modern Authentication for Exchange on-premises.</span></span>

1. <span data-ttu-id="e8a44-126">Activez l’authentification moderne hybride pour Skype entreprise en local.</span><span class="sxs-lookup"><span data-stu-id="e8a44-126">Turn ON Hybrid Modern Authentication for Skype for Business on-premises.</span></span>

<span data-ttu-id="e8a44-127">Ces étapes activent l’agent de configuration pour SFB, SFBO, EXCH et EXO-autrement dit, tous les produits pouvant participer à une configuration de la haute disponibilité de SFB et SFBO (y compris les dépendances de EXCH/EXO).</span><span class="sxs-lookup"><span data-stu-id="e8a44-127">These steps turn on MA for SFB, SFBO, EXCH, and EXO - that is, all the products that can participate in an HMA configuration of SFB and SFBO (including dependencies on EXCH/EXO).</span></span> <span data-ttu-id="e8a44-128">En d’autres termes, si vos utilisateurs sont hébergés dans ou si des boîtes aux lettres sont créées dans n’importe quelle partie de l’environnement hybride (EXO + SFBO, EXO + SFB, EXCH + SFBO ou EXCH + SFB), votre produit fini se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="e8a44-128">In other words, if your users are homed in/have mailboxes created in any part of the Hybrid (EXO + SFBO, EXO + SFB, EXCH + SFBO, or EXCH + SFB), your finished product will look like this:</span></span>
  
![Une topologie de 6 Skype entreprise HMA mixte est associée aux quatre emplacements possibles.](../media/ab89cdf2-160b-49ac-9b71-0160800acfc8.png)
  
<span data-ttu-id="e8a44-130">Comme vous pouvez le constater, il y a quatre emplacements différents pour activer MA !</span><span class="sxs-lookup"><span data-stu-id="e8a44-130">As you can see there are four different places to turn on MA!</span></span> <span data-ttu-id="e8a44-131">Pour une expérience utilisateur optimale, nous vous recommandons d’activer MA dans les quatre emplacements.</span><span class="sxs-lookup"><span data-stu-id="e8a44-131">For the best user experience, we recommend you turn on MA in all four of these locations.</span></span> <span data-ttu-id="e8a44-132">Si vous ne pouvez pas activer l’agent de session sur tous ces emplacements, ajustez les étapes de façon à activer MA uniquement aux emplacements nécessaires pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="e8a44-132">If you can't turn MA on in all these locations, adjust the steps so that you turn on MA only in the locations that are necessary for your environment.</span></span>
  
<span data-ttu-id="e8a44-133">Consultez la rubrique relative à la [prise en charge de Skype entreprise avec ma](https://technet.microsoft.com/library/mt803262.aspx) pour les topologies prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e8a44-133">See the [Supportability topic for Skype for Business with MA](https://technet.microsoft.com/library/mt803262.aspx) for supported topologies.</span></span>
  
 <span data-ttu-id="e8a44-134">**Important** Vérifiez que vous avez rempli toutes les conditions préalables avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="e8a44-134">**Important** Double-check that you've met all the prerequisites before you begin.</span></span> <span data-ttu-id="e8a44-135">Ces informations s’affichent dans la [rubrique vue d’ensemble de l’authentification moderne hybride et conditions préalables](hybrid-modern-auth-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8a44-135">You'll find that information in [Hybrid modern authentication overview and prerequisites](hybrid-modern-auth-overview.md).</span></span>
  
## <a name="collect-all-hma-specific-info-youll-need"></a><span data-ttu-id="e8a44-136">Collecter toutes les informations propres à la HMA</span><span class="sxs-lookup"><span data-stu-id="e8a44-136">Collect all HMA-specific info you'll need</span></span>

<span data-ttu-id="e8a44-137">Une fois que vous avez vérifié que vous répondez aux [conditions préalables](hybrid-modern-auth-overview.md) pour utiliser l’authentification moderne (voir la remarque ci-dessus), vous devez créer un fichier pour conserver les informations dont vous aurez besoin pour configurer la mémoire haute définition dans les étapes à venir.</span><span class="sxs-lookup"><span data-stu-id="e8a44-137">After you've double-checked that you meet the [prerequisites](hybrid-modern-auth-overview.md) to use Modern Authentication (see the note above), you should create a file to hold the info you'll need for configuring HMA in the steps ahead.</span></span> <span data-ttu-id="e8a44-138">Exemples utilisés dans cet article :</span><span class="sxs-lookup"><span data-stu-id="e8a44-138">Examples used in this article:</span></span>
  
- <span data-ttu-id="e8a44-139">**Domaine SIP/SMTP**</span><span class="sxs-lookup"><span data-stu-id="e8a44-139">**SIP/SMTP domain**</span></span>

  - <span data-ttu-id="e8a44-140">Ex.</span><span class="sxs-lookup"><span data-stu-id="e8a44-140">Ex.</span></span> <span data-ttu-id="e8a44-141">contoso.com (est fédéré avec Office 365)</span><span class="sxs-lookup"><span data-stu-id="e8a44-141">contoso.com (is federated with Office 365)</span></span>

- <span data-ttu-id="e8a44-142">**ID client**</span><span class="sxs-lookup"><span data-stu-id="e8a44-142">**Tenant ID**</span></span>

  - <span data-ttu-id="e8a44-143">GUID qui représente votre client Office 365 (à la connexion de contoso.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="e8a44-143">The GUID that represents your Office 365 tenant (at the login of contoso.onmicrosoft.com).</span></span>

- <span data-ttu-id="e8a44-144">**URL du service Web SFB 2015 CU5**</span><span class="sxs-lookup"><span data-stu-id="e8a44-144">**SFB 2015 CU5 Web Service URLs**</span></span>

<span data-ttu-id="e8a44-145">vous aurez besoin d’URL de services Web internes et externes pour tous les pools SfB 2015 déployés.</span><span class="sxs-lookup"><span data-stu-id="e8a44-145">you'll need internal and external web service URLs for all SfB 2015 pools deployed.</span></span> <span data-ttu-id="e8a44-146">Pour obtenir ces informations, exécutez la commande suivante à partir de Skype entreprise Management Shell :</span><span class="sxs-lookup"><span data-stu-id="e8a44-146">To obtain these, run the following from Skype for Business Management Shell:</span></span>
  
```powershell
Get-CsService -WebServer | Select-Object PoolFqdn, InternalFqdn, ExternalFqdn | FL
```

- <span data-ttu-id="e8a44-147">Ex.</span><span class="sxs-lookup"><span data-stu-id="e8a44-147">Ex.</span></span> <span data-ttu-id="e8a44-148">Interne https://lyncwebint01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e8a44-148">Internal: https://lyncwebint01.contoso.com</span></span>

- <span data-ttu-id="e8a44-149">Ex.</span><span class="sxs-lookup"><span data-stu-id="e8a44-149">Ex.</span></span> <span data-ttu-id="e8a44-150">Façon https://lyncwebext01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e8a44-150">External: https://lyncwebext01.contoso.com</span></span>

<span data-ttu-id="e8a44-151">Si vous utilisez un serveur Standard Edition, l’URL interne sera vide.</span><span class="sxs-lookup"><span data-stu-id="e8a44-151">If you're using a Standard Edition server, the internal URL will be blank.</span></span> <span data-ttu-id="e8a44-152">Dans ce cas, utilisez le nom de domaine complet du pool pour l’URL interne.</span><span class="sxs-lookup"><span data-stu-id="e8a44-152">In this case, use the pool fqdn for the internal URL.</span></span>
  
## <a name="turn-on-modern-authentication-for-exo"></a><span data-ttu-id="e8a44-153">Activer l’authentification moderne pour EXO</span><span class="sxs-lookup"><span data-stu-id="e8a44-153">Turn on Modern Authentication for EXO</span></span>

<span data-ttu-id="e8a44-154">Suivez les instructions ci-dessous : [Exchange Online : comment activer votre client pour l’authentification moderne.](https://social.technet.microsoft.com/wiki/contents/articles/32711.exchange-online-how-to-enable-your-tenant-for-modern-authentication.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8a44-154">Follow the instructions here: [Exchange Online: How to enable your tenant for modern authentication.](https://social.technet.microsoft.com/wiki/contents/articles/32711.exchange-online-how-to-enable-your-tenant-for-modern-authentication.aspx)</span></span>
  
## <a name="turn-on-modern-authentication-for-sfbo"></a><span data-ttu-id="e8a44-155">Activer l’authentification moderne pour SFBO</span><span class="sxs-lookup"><span data-stu-id="e8a44-155">Turn on Modern Authentication for SFBO</span></span>

<span data-ttu-id="e8a44-156">Suivez les instructions ci-dessous : [Skype entreprise Online : activez votre client pour l’authentification moderne](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8a44-156">Follow the instructions here: [Skype for Business Online: Enable your tenant for modern authentication](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx).</span></span>
  
## <a name="turn-on-hybrid-modern-authentication-for-exchange-on-premises"></a><span data-ttu-id="e8a44-157">Activer l’authentification moderne hybride pour Exchange sur site</span><span class="sxs-lookup"><span data-stu-id="e8a44-157">Turn on Hybrid Modern Authentication for Exchange on-premises</span></span>

<span data-ttu-id="e8a44-158">Suivez les instructions ci-dessous : [procédure de configuration d’Exchange Server local pour utiliser l’authentification moderne hybride](configure-exchange-server-for-hybrid-modern-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="e8a44-158">Follow the instructions here: [How to configure Exchange Server on-premises to use Hybrid Modern Authentication](configure-exchange-server-for-hybrid-modern-authentication.md).</span></span>
  
## <a name="turn-on-hybrid-modern-authentication-for-skype-for-business-on-premises"></a><span data-ttu-id="e8a44-159">Activer l’authentification moderne hybride pour Skype entreprise en local</span><span class="sxs-lookup"><span data-stu-id="e8a44-159">Turn on Hybrid Modern Authentication for Skype for Business on-premises</span></span>

### <a name="add-on-premises-web-service-urls-as-spns-in-azure-active-directory"></a><span data-ttu-id="e8a44-160">Ajouter des URL de service Web sur site en tant que SPN dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8a44-160">Add on-premises web service URLs as SPNs in Azure Active Directory</span></span>

<span data-ttu-id="e8a44-161">À présent, vous devez exécuter des commandes pour ajouter les URL (collectées précédemment) en tant que principaux de service dans SFBO.</span><span class="sxs-lookup"><span data-stu-id="e8a44-161">Now you'll need to run commands to add the URLs (collected earlier) as Service Principals in SFBO.</span></span>
  
 <span data-ttu-id="e8a44-162">**Note** Les noms de principaux du service (SPN) identifient les services Web et les associent à un principal de sécurité (par exemple, un nom de compte ou un groupe) afin que le service puisse agir au nom d’un utilisateur autorisé.</span><span class="sxs-lookup"><span data-stu-id="e8a44-162">**Note** Service principal names (SPNs) identify web services and associate them with a security principal (such as an account name or group) so that the service can act on the behalf of an authorized user.</span></span> <span data-ttu-id="e8a44-163">Les clients qui s’authentifient sur un serveur utilisent les informations contenues dans les noms principaux de client.</span><span class="sxs-lookup"><span data-stu-id="e8a44-163">Clients authenticating to a server make use of information that's contained in SPNs.</span></span>
  
1. <span data-ttu-id="e8a44-164">Tout d’abord, connectez-vous à Azure Active Directory (Azure AD) avec [ces instructions](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="e8a44-164">First, connect to Azure Active Directory (Azure AD) with [these instructions](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-1.0).</span></span>

2. <span data-ttu-id="e8a44-165">Exécutez cette commande, en local, pour obtenir la liste des URL de service Web SFB.</span><span class="sxs-lookup"><span data-stu-id="e8a44-165">Run this command, on-premises, to get a list of SFB web service URLs.</span></span>

   <span data-ttu-id="e8a44-166">Notez que le AppPrincipalId commence par `00000004` .</span><span class="sxs-lookup"><span data-stu-id="e8a44-166">Note that the AppPrincipalId begins with `00000004`.</span></span> <span data-ttu-id="e8a44-167">Cela correspond à Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="e8a44-167">This corresponds to Skype for Business Online.</span></span>

   <span data-ttu-id="e8a44-168">Notez (et capture d’écran pour une comparaison ultérieure) la sortie de cette commande, qui inclura une URL SE et WS, mais qui se composent essentiellement de noms principaux de service qui commencent par `00000004-0000-0ff1-ce00-000000000000/` .</span><span class="sxs-lookup"><span data-stu-id="e8a44-168">Take note of (and screenshot for later comparison) the output of this command, which will include an SE and WS URL, but mostly consist of SPNs that begin with `00000004-0000-0ff1-ce00-000000000000/`.</span></span>

```powershell
Get-MsolServicePrincipal -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000 | Select -ExpandProperty ServicePrincipalNames
```

3. <span data-ttu-id="e8a44-169">Si les URL SFB internes **ou** externes de l’organisation locale sont manquantes (par exemple https://lyncwebint01.contoso.com , https://lyncwebext01.contoso.com) nous devons ajouter ces enregistrements spécifiques à cette liste.</span><span class="sxs-lookup"><span data-stu-id="e8a44-169">If the internal **or** external SFB URLs from on-premises are missing (for example, https://lyncwebint01.contoso.com and https://lyncwebext01.contoso.com) we will need to add those specific records to this list.</span></span>

    <span data-ttu-id="e8a44-170">N’oubliez pas de remplacer  *les exemples d’URL* ci-dessous par vos URL réelles dans la commande Add Commands !</span><span class="sxs-lookup"><span data-stu-id="e8a44-170">Be sure to replace  *the example URLs* below with your actual URLs in the Add commands!</span></span>
  
```powershell
$x= Get-MsolServicePrincipal -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000
$x.ServicePrincipalnames.Add("https://lyncwebint01.contoso.com/")
$x.ServicePrincipalnames.Add("https://lyncwebext01.contoso.com/")
Set-MSOLServicePrincipal -AppPrincipalId 00000004-0000-0ff1-ce00-000000000000 -ServicePrincipalNames $x.ServicePrincipalNames
```
  
4. <span data-ttu-id="e8a44-171">Vérifiez que vos nouveaux enregistrements ont été ajoutés en exécutant de nouveau la commande **Get-MsolServicePrincipal** à partir de l’étape 2 et en examinant la sortie.</span><span class="sxs-lookup"><span data-stu-id="e8a44-171">Verify your new records were added by running the **Get-MsolServicePrincipal** command from step 2 again, and looking through the output.</span></span> <span data-ttu-id="e8a44-172">Comparez la liste ou la capture d’écran de l’avant à la nouvelle liste de noms principaux de vente.</span><span class="sxs-lookup"><span data-stu-id="e8a44-172">Compare the list or screenshot from before to the new list of SPNs.</span></span> <span data-ttu-id="e8a44-173">Vous pouvez également créer une capture d’écran de la nouvelle liste pour vos enregistrements.</span><span class="sxs-lookup"><span data-stu-id="e8a44-173">You might also screenshot the new list for your records.</span></span> <span data-ttu-id="e8a44-174">Si vous avez réussi, vous verrez les deux nouvelles URL dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e8a44-174">If you were successful, you'll see the two new URLs in the list.</span></span> <span data-ttu-id="e8a44-175">À l’aide de notre exemple, la liste des SPN inclut désormais les URL spécifiques https://lyncwebint01.contoso.com et https://lyncwebext01.contoso.com/ .</span><span class="sxs-lookup"><span data-stu-id="e8a44-175">Going by our example, the list of SPNs will now include the specific URLs https://lyncwebint01.contoso.com and https://lyncwebext01.contoso.com/.</span></span>

### <a name="create-the-evosts-auth-server-object"></a><span data-ttu-id="e8a44-176">Créer l’objet serveur d’authentification EvoSTS</span><span class="sxs-lookup"><span data-stu-id="e8a44-176">Create the EvoSTS Auth Server Object</span></span>

<span data-ttu-id="e8a44-177">Exécutez la commande suivante dans Skype entreprise Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e8a44-177">Run the following command in the Skype for Business Management Shell.</span></span>
  
```powershell
New-CsOAuthServer -Identity evoSTS -MetadataURL https://login.windows.net/common/FederationMetadata/2007-06/FederationMetadata.xml -AcceptSecurityIdentifierInformation $true -Type AzureAD
```

### <a name="enable-hybrid-modern-authentication"></a><span data-ttu-id="e8a44-178">Activer l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="e8a44-178">Enable Hybrid Modern Authentication</span></span>

<span data-ttu-id="e8a44-179">Il s’agit de l’étape qui active réellement MA.</span><span class="sxs-lookup"><span data-stu-id="e8a44-179">This is the step that actually turns on MA.</span></span> <span data-ttu-id="e8a44-180">Toutes les étapes précédentes peuvent être exécutées à l’avance sans modifier le flux d’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="e8a44-180">All the previous steps can be run ahead of time without changing the client authentication flow.</span></span> <span data-ttu-id="e8a44-181">Lorsque vous êtes prêt à modifier le flux d’authentification, exécutez la commande suivante dans Skype for Business Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e8a44-181">When you're ready to change the authentication flow, run this command in the Skype for Business Management Shell.</span></span>

```powershell
Set-CsOAuthConfiguration -ClientAuthorizationOAuthServerIdentity evoSTS
```

## <a name="verify"></a><span data-ttu-id="e8a44-182">Vérifié</span><span class="sxs-lookup"><span data-stu-id="e8a44-182">Verify</span></span>

<span data-ttu-id="e8a44-183">Une fois que vous activez HMA, la prochaine connexion d’un client utilisera le nouveau flux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="e8a44-183">Once you enable HMA, a client's next login will use the new auth flow.</span></span> <span data-ttu-id="e8a44-184">Notez que l’activation de la mémoire HMA ne déclenche pas une réauthentification pour un client.</span><span class="sxs-lookup"><span data-stu-id="e8a44-184">Note that just turning on HMA won't trigger a reauthentication for any client.</span></span> <span data-ttu-id="e8a44-185">Les clients se ré-authentifient en fonction de la durée de vie des jetons d’authentification et/ou des certificats dont ils disposent.</span><span class="sxs-lookup"><span data-stu-id="e8a44-185">The clients reauthenticate based on the lifetime of the auth tokens and/or certs they have.</span></span>
  
<span data-ttu-id="e8a44-186">Pour tester que la haute-dernière fonctionne après l’avoir activée, déconnectez-vous d’un client Windows SFB de test et veillez à cliquer sur « supprimer mes informations d’identification ».</span><span class="sxs-lookup"><span data-stu-id="e8a44-186">To test that HMA is working after you've enabled it, sign out of a test SFB Windows client and be sure to click 'delete my credentials'.</span></span> <span data-ttu-id="e8a44-187">Reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="e8a44-187">Sign in again.</span></span> <span data-ttu-id="e8a44-188">Le client doit maintenant utiliser le flux d’authentification moderne et votre connexion inclut désormais une invite **Office 365** pour un compte professionnel ou scolaire, vu juste avant que le client ne contacte le serveur et vous connecte.</span><span class="sxs-lookup"><span data-stu-id="e8a44-188">The client should now use the Modern Auth flow and your login will now include an **Office 365** prompt for a 'Work or school' account, seen right before the client contacts the server and logs you in.</span></span>
  
<span data-ttu-id="e8a44-189">Vous devez également vérifier les « informations de configuration » pour les clients Skype entreprise pour une « autorité OAuth ».</span><span class="sxs-lookup"><span data-stu-id="e8a44-189">You should also check the 'Configuration Information' for Skype for Business Clients for an 'OAuth Authority'.</span></span> <span data-ttu-id="e8a44-190">Pour effectuer cette action sur votre ordinateur client, maintenez la touche CTRL enfoncée simultanément en cliquant avec le bouton droit sur l’icône Skype entreprise dans le bac de notification Windows.</span><span class="sxs-lookup"><span data-stu-id="e8a44-190">To do this on your client computer, hold down the CTRL key at the same time you right-click the Skype for Business Icon in the Windows Notification tray.</span></span> <span data-ttu-id="e8a44-191">Cliquez sur **informations de configuration** dans le menu qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e8a44-191">Click **Configuration Information** in the menu that appears.</span></span> <span data-ttu-id="e8a44-192">Dans la fenêtre « informations de configuration de Skype entreprise » qui s’affichent sur le bureau, recherchez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e8a44-192">In the 'Skype for Business Configuration Information' window that will appear on the desktop, look for the following:</span></span>
  
![Les informations de configuration d’un client Skype entreprise qui utilisent l’authentification moderne indiquent une URL d’autorisation OAUTH Lync et EWS de https://login.windows.net/common/oauth2/authorize .](../media/4e54edf5-c8f8-4e7f-b032-5d413b0232de.png)
  
<span data-ttu-id="e8a44-194">Vous devez également maintenir la touche CTRL enfoncée en même temps que vous cliquez avec le bouton droit sur l’icône du client Outlook (également dans le bac Windows notifications) et cliquez sur « état de la connexion ».</span><span class="sxs-lookup"><span data-stu-id="e8a44-194">You should also hold down the CTRL key at the same time you right-click the icon for the Outlook client (also in the Windows Notifications tray) and click 'Connection Status'.</span></span> <span data-ttu-id="e8a44-195">Recherchez l’adresse SMTP du client par rapport à un type d’authentification « porteur \* », qui représente le jeton du porteur utilisé dans OAuth.</span><span class="sxs-lookup"><span data-stu-id="e8a44-195">Look for the client's SMTP address against an AuthN type of 'Bearer\*', which represents the bearer token used in OAuth.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="e8a44-196">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="e8a44-196">Related articles</span></span>

<span data-ttu-id="e8a44-197">[Revenez à la vue d’ensemble de l’authentification moderne](hybrid-modern-auth-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8a44-197">[Link back to the Modern Authentication overview](hybrid-modern-auth-overview.md).</span></span>
  
<span data-ttu-id="e8a44-198">Avez-vous besoin de savoir comment utiliser l’authentification moderne (ADAL) pour vos clients Skype entreprise ?</span><span class="sxs-lookup"><span data-stu-id="e8a44-198">Do you need to know how to use Modern Authentication (ADAL) for your Skype for Business clients?</span></span> <span data-ttu-id="e8a44-199">Nous avons les étapes à suivre [ici](https://technet.microsoft.com/library/mt710548.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8a44-199">We've got steps [here](https://technet.microsoft.com/library/mt710548.aspx).</span></span>
