---
title: Comment configurer Exchange Server en local pour utiliser l’authentification moderne hybride
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/16/2020
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: cef3044d-d4cb-4586-8e82-ee97bd3b14ad
ms.collection:
- M365-security-compliance
f1.keywords:
- NOCSH
description: Découvrez comment configurer une Exchange Server local pour utiliser l’authentification moderne hybride (HMA), ce qui vous offre une authentification et une autorisation utilisateur plus sécurisées.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 46646f35d3b41821424269f66721fbf829d339f7
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50928201"
---
# <a name="how-to-configure-exchange-server-on-premises-to-use-hybrid-modern-authentication"></a><span data-ttu-id="ccbe2-103">Comment configurer Exchange Server en local pour utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="ccbe2-103">How to configure Exchange Server on-premises to use Hybrid Modern Authentication</span></span>

<span data-ttu-id="ccbe2-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="ccbe2-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="ccbe2-105">L’authentification moderne hybride (HMA) est une méthode de gestion des identités qui offre une authentification et une autorisation utilisateur plus sécurisées et est disponible pour les déploiements hybrides Exchange Server locaux.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-105">Hybrid Modern Authentication (HMA) is a method of identity management that offers more secure user authentication and authorization, and is available for Exchange server on-premises hybrid deployments.</span></span>

## <a name="fyi"></a><span data-ttu-id="ccbe2-106">Pour info</span><span class="sxs-lookup"><span data-stu-id="ccbe2-106">FYI</span></span>

<span data-ttu-id="ccbe2-107">Avant de commencer, j’appelle :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-107">Before we begin, I call:</span></span>

- <span data-ttu-id="ccbe2-108">Authentification moderne \> hybride HMA</span><span class="sxs-lookup"><span data-stu-id="ccbe2-108">Hybrid Modern Authentication \> HMA</span></span>

- <span data-ttu-id="ccbe2-109">EXCH exchange local \></span><span class="sxs-lookup"><span data-stu-id="ccbe2-109">Exchange on-premises \> EXCH</span></span>

- <span data-ttu-id="ccbe2-110">Exchange Online \> EXO</span><span class="sxs-lookup"><span data-stu-id="ccbe2-110">Exchange Online \> EXO</span></span>

<span data-ttu-id="ccbe2-111">En outre, si un graphique de cet article possède un objet « grisé » ou « grisé » qui signifie que l’élément affiché en gris n’est pas inclus dans la configuration propre à *HMA.*</span><span class="sxs-lookup"><span data-stu-id="ccbe2-111">Also, *if a graphic in this article has an object that's 'grayed-out' or 'dimmed' that means the element shown in gray is not included in HMA-specific configuration*.</span></span>

## <a name="enabling-hybrid-modern-authentication"></a><span data-ttu-id="ccbe2-112">Activation de l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="ccbe2-112">Enabling Hybrid Modern Authentication</span></span>

<span data-ttu-id="ccbe2-113">L’ment HMA signifie :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-113">Turning on HMA means:</span></span>

1. <span data-ttu-id="ccbe2-114">Veillez à respecter les préreqs avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-114">Being sure you meet the prereqs before you begin.</span></span>

1. <span data-ttu-id="ccbe2-115">Étant  donné que de nombreux prérequis sont courants pour Skype Entreprise et Exchange, la vue d’ensemble de l’authentification moderne hybride et les conditions préalables à son utilisation avec les serveurs Skype Entreprise et [Exchange locaux.](hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ccbe2-115">Since many **prerequisites** are common for both Skype for Business and Exchange, [Hybrid Modern Authentication overview and prerequisites for using it with on-premises Skype for Business and Exchange servers](hybrid-modern-auth-overview.md).</span></span> <span data-ttu-id="ccbe2-116">Faites-le avant de commencer l’une des étapes de cet article.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-116">Do this before you begin any of the steps in this article.</span></span>

1. <span data-ttu-id="ccbe2-117">Ajout d’URL de service web local en tant que noms principaux de **service (SNS)** dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-117">Adding on-premises web service URLs as **Service Principal Names (SPNs)** in Azure AD.</span></span>

1. <span data-ttu-id="ccbe2-118">S’assurer que tous les répertoires virtuels sont activés pour HMA</span><span class="sxs-lookup"><span data-stu-id="ccbe2-118">Ensuring all Virtual Directories are enabled for HMA</span></span>

1. <span data-ttu-id="ccbe2-119">Recherche de l’objet EvoSTS Auth Server</span><span class="sxs-lookup"><span data-stu-id="ccbe2-119">Checking for the EvoSTS Auth Server object</span></span>

1. <span data-ttu-id="ccbe2-120">Activation du HMA dans EXCH.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-120">Enabling HMA in EXCH.</span></span>

 <span data-ttu-id="ccbe2-121">**Remarque** Votre version d’Office prend-elle en charge MA ?</span><span class="sxs-lookup"><span data-stu-id="ccbe2-121">**Note** Does your version of Office support MA?</span></span> <span data-ttu-id="ccbe2-122">Découvrez comment fonctionne l’authentification moderne pour les applications [clientes Office 2013 et Office 2016.](modern-auth-for-office-2013-and-2016.md)</span><span class="sxs-lookup"><span data-stu-id="ccbe2-122">See [How modern authentication works for Office 2013 and Office 2016 client apps](modern-auth-for-office-2013-and-2016.md).</span></span>

## <a name="make-sure-you-meet-all-the-prerequisites"></a><span data-ttu-id="ccbe2-123">Assurez-vous que vous répondez à toutes les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="ccbe2-123">Make sure you meet all the prerequisites</span></span>

<span data-ttu-id="ccbe2-124">Étant donné que de nombreux prérequis sont courants pour Skype Entreprise et Exchange, examinez la vue d’ensemble de l’authentification moderne hybride et les conditions préalables à son utilisation avec les serveurs Skype Entreprise et [Exchange locaux.](hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ccbe2-124">Since many prerequisites are common for both Skype for Business and Exchange, review [Hybrid Modern Authentication overview and prerequisites for using it with on-premises Skype for Business and Exchange servers](hybrid-modern-auth-overview.md).</span></span> <span data-ttu-id="ccbe2-125">Faites-le  *avant de*  commencer l’une des étapes de cet article.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-125">Do this  *before*  you begin any of the steps in this article.</span></span>

## <a name="add-on-premises-web-service-urls-as-spns-in-azure-ad"></a><span data-ttu-id="ccbe2-126">Ajouter des URL de service web local en tant que SSN dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="ccbe2-126">Add on-premises web service URLs as SPNs in Azure AD</span></span>

<span data-ttu-id="ccbe2-127">Exécutez les commandes qui affectent vos URL de service web local en tant que SSN Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-127">Run the commands that assign your on-premises web service URLs as Azure AD SPNs.</span></span> <span data-ttu-id="ccbe2-128">Les SSN sont utilisés par les ordinateurs clients et les appareils lors de l’authentification et de l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-128">SPNs are used by client machines and devices during authentication and authorization.</span></span> <span data-ttu-id="ccbe2-129">Toutes les URL qui peuvent être utilisées pour se connecter en local à Azure Active Directory (Azure AD) doivent être enregistrées dans Azure AD (cela inclut les espaces de noms internes et externes).</span><span class="sxs-lookup"><span data-stu-id="ccbe2-129">All the URLs that might be used to connect from on-premises to Azure Active Directory (Azure AD) must be registered in Azure AD (this includes both internal and external namespaces).</span></span>

<span data-ttu-id="ccbe2-130">Tout d’abord, rassemblez toutes les URL que vous devez ajouter dans AAD.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-130">First, gather all the URLs that you need to add in AAD.</span></span> <span data-ttu-id="ccbe2-131">Exécutez les commandes ci-après en local :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-131">Run these commands on-premises:</span></span>

```powershell
Get-MapiVirtualDirectory | FL server,*url*
Get-WebServicesVirtualDirectory | FL server,*url*
Get-ClientAccessServer | fl Name, AutodiscoverServiceInternalUri
Get-OABVirtualDirectory | FL server,*url*
Get-AutodiscoverVirtualDirectory | FL server,*url*
Get-OutlookAnywhere | FL server,*url*
```

<span data-ttu-id="ccbe2-132">Assurez-vous que les url à qui les clients peuvent se connecter sont répertoriées en tant que noms principaux de service HTTPS dans AAD.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-132">Ensure the URLs clients may connect to are listed as HTTPS service principal names in AAD.</span></span>

1. <span data-ttu-id="ccbe2-133">Tout d’abord, connectez-vous à AAD [avec ces instructions.](connect-to-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="ccbe2-133">First, connect to AAD with [these instructions](connect-to-microsoft-365-powershell.md).</span></span>

   <span data-ttu-id="ccbe2-134">**Remarque** Vous devez utiliser l’option _Connect-MsolService_ à partir de cette page pour pouvoir utiliser la commande ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-134">**Note** You need to use the _Connect-MsolService_ option from this page to be able to use the command below.</span></span>

2. <span data-ttu-id="ccbe2-135">Pour vos URL liées à Exchange, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-135">For your Exchange-related URLs, type the following command:</span></span>

   ```powershell
   Get-MsolServicePrincipal -AppPrincipalId 00000002-0000-0ff1-ce00-000000000000 | select -ExpandProperty ServicePrincipalNames
   ```

   <span data-ttu-id="ccbe2-136">Prenez note (et capture d’écran pour comparaison ultérieure) de la sortie de cette commande, qui doit inclure un  *autodiscover.yourdomain.com*  https:// et une URL  *https:// mail.yourdomain.com,* mais principalement des SSN qui commencent par 00000002-0000-0ff1-ce00-0000000000000/.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-136">Take note of (and screenshot for later comparison) the output of this command, which should include an https://  *autodiscover.yourdomain.com*  and https://  *mail.yourdomain.com* URL, but mostly consist of SPNs that begin with 00000002-0000-0ff1-ce00-000000000000/.</span></span> <span data-ttu-id="ccbe2-137">Si des URL https:// de votre site local sont manquantes, nous devons ajouter ces enregistrements spécifiques à cette liste.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-137">If there are https:// URLs from your on-premises that are missing, we will need to add those specific records to this list.</span></span>

3. <span data-ttu-id="ccbe2-138">Si vous ne voyez pas vos enregistrements MAPI/HTTP, EWS, ActiveSync, OAB et Autodiscover internes et externes dans cette liste, vous devez les ajouter à l’aide de la commande ci-dessous (les exemples d’URL sont « ' » et « ' , mais vous devez remplacer les `mail.corp.contoso.com` `owa.contoso.com` **exemples d’URL** par les vôtres ) :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-138">If you don't see your internal and external MAPI/HTTP, EWS, ActiveSync, OAB, and Autodiscover records in this list, you must add them using the command below (the example URLs are '`mail.corp.contoso.com`' and '`owa.contoso.com`', but you'd **replace the example URLs with your own**):</span></span>

   ```powershell
   $x= Get-MsolServicePrincipal -AppPrincipalId 00000002-0000-0ff1-ce00-000000000000
   $x.ServicePrincipalnames.Add("https://mail.corp.contoso.com/")
   $x.ServicePrincipalnames.Add("https://owa.contoso.com/")
   Set-MSOLServicePrincipal -AppPrincipalId 00000002-0000-0ff1-ce00-000000000000 -ServicePrincipalNames $x.ServicePrincipalNames
   ```

4. <span data-ttu-id="ccbe2-139">Vérifiez que vos nouveaux enregistrements ont été ajoutés en exécutant à nouveau Get-MsolServicePrincipal commande de l’étape 2 et en regardant la sortie.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-139">Verify your new records were added by running the Get-MsolServicePrincipal command from step 2 again, and looking through the output.</span></span> <span data-ttu-id="ccbe2-140">Comparez la liste /capture d’écran d’avant à la nouvelle liste de SSN.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-140">Compare the list / screenshot from before to the new list of SPNs.</span></span> <span data-ttu-id="ccbe2-141">Vous pouvez également prendre une capture d’écran de la nouvelle liste pour vos enregistrements.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-141">You might also take a screenshot of the new list for your records.</span></span> <span data-ttu-id="ccbe2-142">Si vous avez réussi, vous verrez les deux nouvelles URL dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-142">If you were successful, you will see the two new URLs in the list.</span></span> <span data-ttu-id="ccbe2-143">En suivant notre exemple, la liste des SNS inclut désormais les URL spécifiques  `https://mail.corp.contoso.com`  et  `https://owa.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="ccbe2-143">Going by our example, the list of SPNs will now include the specific URLs  `https://mail.corp.contoso.com`  and  `https://owa.contoso.com`.</span></span>

## <a name="verify-virtual-directories-are-properly-configured"></a><span data-ttu-id="ccbe2-144">Vérifier que les répertoires virtuels sont correctement configurés</span><span class="sxs-lookup"><span data-stu-id="ccbe2-144">Verify Virtual Directories are Properly Configured</span></span>

<span data-ttu-id="ccbe2-145">Vérifiez maintenant qu’OAuth est correctement activé dans Exchange sur tous les répertoires virtuels qu’Outlook peut utiliser en exécutant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-145">Now verify OAuth is properly enabled in Exchange on all of the Virtual Directories Outlook might use by running the following commands:</span></span>

```powershell
Get-MapiVirtualDirectory | FL server,*url*,*auth*
Get-WebServicesVirtualDirectory | FL server,*url*,*oauth*
Get-OABVirtualDirectory | FL server,*url*,*oauth*
Get-AutoDiscoverVirtualDirectory | FL server,*oauth*
```

<span data-ttu-id="ccbe2-146">Vérifiez la sortie pour vous assurer **qu’OAuth** est activé sur chacun de ces VDirs, il ressemblera à ceci (et l’élément clé à examiner est « OAuth » ) :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-146">Check the output to make sure **OAuth** is enabled on each of these VDirs, it will look something like this (and the key thing to look at is 'OAuth'):</span></span>

```powershell
Get-MapiVirtualDirectory | fl server,*url*,*auth*

Server                        : EX1
InternalUrl                   : https://mail.contoso.com/mapi
ExternalUrl                   : https://mail.contoso.com/mapi
IISAuthenticationMethods      : {Ntlm, OAuth, Negotiate}
InternalAuthenticationMethods : {Ntlm, OAuth, Negotiate}
ExternalAuthenticationMethods : {Ntlm, OAuth, Negotiate}
```

<span data-ttu-id="ccbe2-147">Si OAuth est absent d’un serveur et de l’un des quatre répertoires virtuels, vous devez l’ajouter à l’aide des commandes pertinentes avant de poursuivre ([Set-MapiVirtualDirectory](/powershell/module/exchange/set-mapivirtualdirectory), [Set-WebServicesVirtualDirectory](/powershell/module/exchange/set-webservicesvirtualdirectory), [Set-OABVirtualDirectory](/powershell/module/exchange/set-oabvirtualdirectory)et [Set-AutodiscoverVirtualDirectory](/powershell/module/exchange/set-autodiscovervirtualdirectory)).</span><span class="sxs-lookup"><span data-stu-id="ccbe2-147">If OAuth is missing from any server and any of the four virtual directories, you need to add it using the relevant commands before proceeding ([Set-MapiVirtualDirectory](/powershell/module/exchange/set-mapivirtualdirectory), [Set-WebServicesVirtualDirectory](/powershell/module/exchange/set-webservicesvirtualdirectory), [Set-OABVirtualDirectory](/powershell/module/exchange/set-oabvirtualdirectory), and [Set-AutodiscoverVirtualDirectory](/powershell/module/exchange/set-autodiscovervirtualdirectory)).</span></span>

## <a name="confirm-the-evosts-auth-server-object-is-present"></a><span data-ttu-id="ccbe2-148">Vérifier que l’objet serveur d’th EvoSTS est présent</span><span class="sxs-lookup"><span data-stu-id="ccbe2-148">Confirm the EvoSTS Auth Server Object is Present</span></span>

<span data-ttu-id="ccbe2-149">Revenir à l’Exchange Management Shell local pour cette dernière commande.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-149">Return to the on-premises Exchange Management Shell for this last command.</span></span> <span data-ttu-id="ccbe2-150">Vous pouvez maintenant vérifier que votre site local dispose d’une entrée pour le fournisseur d’authentification evoSTS :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-150">Now you can validate that your on-premises has an entry for the evoSTS authentication provider:</span></span>

```powershell
Get-AuthServer | where {$_.Name -eq "EvoSts"}
```

<span data-ttu-id="ccbe2-151">Votre sortie doit afficher un AuthServer du nom EvoSts et l’état « Enabled » doit être True.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-151">Your output should show an AuthServer of the Name EvoSts and the 'Enabled' state should be True.</span></span> <span data-ttu-id="ccbe2-152">Si ce n’est pas le cas, vous devez télécharger et exécuter la version la plus récente de l’Assistant Configuration hybride.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-152">If you don't see this, you should download and run the most recent version of the Hybrid Configuration Wizard.</span></span>

 <span data-ttu-id="ccbe2-153">**Important** Si vous exécutez Exchange 2010 dans votre environnement, le fournisseur d’authentification EvoSTS ne sera pas créé.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-153">**Important** If you're running Exchange 2010 in your environment, the EvoSTS authentication provider won't be created.</span></span>

## <a name="enable-hma"></a><span data-ttu-id="ccbe2-154">Activer HMA</span><span class="sxs-lookup"><span data-stu-id="ccbe2-154">Enable HMA</span></span>

<span data-ttu-id="ccbe2-155">Exécutez la commande suivante dans l’Exchange Management Shell, en local :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-155">Run the following command in the Exchange Management Shell, on-premises:</span></span>

```powershell
Set-AuthServer -Identity EvoSTS -IsDefaultAuthorizationEndpoint $true
Set-OrganizationConfig -OAuth2ClientProfileEnabled $true
```

## <a name="verify"></a><span data-ttu-id="ccbe2-156">Vérifier</span><span class="sxs-lookup"><span data-stu-id="ccbe2-156">Verify</span></span>

<span data-ttu-id="ccbe2-157">Une fois que vous avez activé HMA, la connexion suivante d’un client utilise le nouveau flux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-157">Once you enable HMA, a client's next login will use the new auth flow.</span></span> <span data-ttu-id="ccbe2-158">Notez que le simple fait d’allumer HMA ne déclenche pas de réauthentication pour un client.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-158">Note that just turning on HMA won't trigger a reauthentication for any client.</span></span> <span data-ttu-id="ccbe2-159">Les clients se réauthentent en fonction de la durée de vie des jetons d’th et/ou des jetons dont ils ont.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-159">The clients reauthenticate based on the lifetime of the auth tokens and/or certs they have.</span></span>

<span data-ttu-id="ccbe2-160">Vous devez également maintenir la touche CTRL en même temps que vous cliquez avec le bouton droit sur l’icône du client Outlook (également dans le bac notifications Windows) et cliquez sur « État de la connexion ».</span><span class="sxs-lookup"><span data-stu-id="ccbe2-160">You should also hold down the CTRL key at the same time you right-click the icon for the Outlook client (also in the Windows Notifications tray) and click 'Connection Status'.</span></span> <span data-ttu-id="ccbe2-161">Recherchez l’adresse SMTP du client par rapport à un type « Authn » de « Bearer » qui représente le jeton du porteur utilisé dans \* OAuth.</span><span class="sxs-lookup"><span data-stu-id="ccbe2-161">Look for the client's SMTP address against an 'Authn' type of 'Bearer\*', which represents the bearer token used in OAuth.</span></span>

 <span data-ttu-id="ccbe2-162">**Remarque** Vous devez configurer Skype Entreprise avec HMA ?</span><span class="sxs-lookup"><span data-stu-id="ccbe2-162">**Note** Need to configure Skype for Business with HMA?</span></span> <span data-ttu-id="ccbe2-163">Vous aurez besoin de deux articles : un qui répertorie les [topologies](/skypeforbusiness/plan-your-deployment/modern-authentication/topologies-supported)pris en charge et un qui vous montre comment [faire la configuration](configure-skype-for-business-for-hybrid-modern-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="ccbe2-163">You'll need two articles: One that lists [supported topologies](/skypeforbusiness/plan-your-deployment/modern-authentication/topologies-supported), and one that shows you [how to do the configuration](configure-skype-for-business-for-hybrid-modern-authentication.md).</span></span>

## <a name="using-hybrid-modern-authentication-with-outlook-for-ios-and-android"></a><span data-ttu-id="ccbe2-164">Utilisation de l’authentification moderne hybride avec Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="ccbe2-164">Using hybrid Modern Authentication with Outlook for iOS and Android</span></span>

<span data-ttu-id="ccbe2-165">Si vous êtes un client local utilisant le serveur Exchange sur TCP 443, ignorez le traitement du trafic pour les plages d’adresses IP suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccbe2-165">If you are an on-premises customer using Exchange server on TCP 443, bypass traffic processing for the following IP ranges:</span></span>

```text
52.125.128.0/20
52.127.96.0/23
```

## <a name="related-topics"></a><span data-ttu-id="ccbe2-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccbe2-166">Related topics</span></span>

[<span data-ttu-id="ccbe2-167">Configuration requise pour l’authentification moderne pour la transition d’Office 365 dédié/ITAR vers vNext</span><span class="sxs-lookup"><span data-stu-id="ccbe2-167">Modern Authentication configuration requirements for transition from Office 365 dedicated/ITAR to vNext</span></span>](/exchange/troubleshoot/modern-authentication/modern-authentication-configuration)