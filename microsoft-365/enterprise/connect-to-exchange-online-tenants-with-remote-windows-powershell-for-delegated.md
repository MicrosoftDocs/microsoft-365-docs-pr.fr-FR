---
title: Connexion aux locataires Exchange Online avec Remote Windows PowerShell pour les partenaires DAP
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.assetid: ae5f1a87-8b77-4f93-a1b8-56f800aeb283
description: 'Résumé : Utilisez Windows PowerShell distant pour vous connecter à Exchange Online à l’aide de la valeur DelegatedOrg.'
ms.openlocfilehash: 1351a6a6d19fac408b673796c1179bca0ede9c9f
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689971"
---
# <a name="connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated-access-permissions-dap-partners"></a><span data-ttu-id="b898a-103">Connexion à des locataires Exchange Online avec Remote Windows PowerShell pour les partenaires avec autorisations d’accès délégué</span><span class="sxs-lookup"><span data-stu-id="b898a-103">Connect to Exchange Online tenants with remote Windows PowerShell for Delegated Access Permissions (DAP) partners</span></span>

<span data-ttu-id="b898a-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="b898a-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b898a-p101">Les procédures décrites dans cette rubrique sont uniquement destinées aux partenaires avec autorisation d’accès délégué (DAP). Si vous n’êtes pas un partenaire DAP, n’utilisez pas les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b898a-p101">The procedures in this topic are only for Delegated Access Permission (DAP) partners. If you aren't a DAP partner, don't use the procedures in this topic.</span></span> 
  
<span data-ttu-id="b898a-107">Les partenaires avec autorisation d'accès délégué sont les partenaires de syndication et fournisseurs de solutions cloud.</span><span class="sxs-lookup"><span data-stu-id="b898a-107">DAP partners are Syndication and Cloud Solution Providers (CSP) partners.</span></span> <span data-ttu-id="b898a-108">Il s'agit souvent de fournisseurs de réseau ou de télécommunication pour d'autres sociétés.</span><span class="sxs-lookup"><span data-stu-id="b898a-108">They are frequently network or telecom providers to other companies.</span></span> <span data-ttu-id="b898a-109">Ils regroupent les abonnements dans leurs offres de services pour les clients.</span><span class="sxs-lookup"><span data-stu-id="b898a-109">They bundle subscriptions into their service offerings to their customers.</span></span> <span data-ttu-id="b898a-110">Ils possèdent un client qui bénéficie automatiquement des autorisations d’administration pour le compte de (administrateur) pour leurs clients Microsoft 365, afin qu’ils puissent administrer et rendre compte de tous leurs locations de clients.</span><span class="sxs-lookup"><span data-stu-id="b898a-110">They own a partner tenancy that is automatically granted Administer On Behalf Of (AOBO) permissions to their Microsoft 365 customer tenancies so they can administer and report on all of their customer tenancies.</span></span>

<span data-ttu-id="b898a-111">Les partenaires DAP peuvent utiliser Exchange Online PowerShell pour gérer les paramètres Exchange Online du client et obtenir des rapports Microsoft 365 à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b898a-111">DAP partners can use Exchange Online PowerShell to manage customer Exchange Online settings and get Microsoft 365 reports from the command line.</span></span> <span data-ttu-id="b898a-112">Vous utilisez Windows PowerShell sur votre ordinateur local pour créer une session PowerShell distante vers Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b898a-112">You use Windows PowerShell on your local computer to create a remote PowerShell session to Exchange Online.</span></span> <span data-ttu-id="b898a-113">Il s’agit d’un processus simple en trois étapes dans lequel vous entrez vos informations d’identification, fournissez les paramètres de connexion requis, puis importez les applets de commande Exchange Online dans votre session Windows PowerShell locale afin de pouvoir les utiliser.</span><span class="sxs-lookup"><span data-stu-id="b898a-113">It's a simple three-step process where you enter your credentials, provide the required connection settings, and then import the Exchange Online cmdlets into your local Windows PowerShell session so that you can use them.</span></span>

> [!NOTE]
> <span data-ttu-id="b898a-p104">Les partenaires DAP ne peuvent pas utiliser les procédures décrites dans [Connexion à Exchange Online PowerShell avec l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell) pour se connecter à leur organisation locataire cliente dans Exchange Online PowerShell. L’authentification multifacteur et le module PowerShell distant Exchange Online ne fonctionnent pas avec l’authentification déléguée.</span><span class="sxs-lookup"><span data-stu-id="b898a-p104">DAP partners can't use the procedures in [Connect to Exchange Online PowerShell using multi-factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell) to connect to their customer tenant organizations in Exchange Online PowerShell. MFA and the Exchange Online Remote PowerShell Module don't work with delegated authentication.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b898a-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b898a-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b898a-117">Durée d’exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="b898a-117">Estimated time to complete: 5 minutes</span></span>

- <span data-ttu-id="b898a-118">Vous pouvez utiliser les versions de Windows suivantes :</span><span class="sxs-lookup"><span data-stu-id="b898a-118">You can use the following versions of Windows:</span></span>
    
  - <span data-ttu-id="b898a-119">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b898a-119">Windows 10</span></span>

  - <span data-ttu-id="b898a-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b898a-120">Windows 8.1</span></span>

  - <span data-ttu-id="b898a-121">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b898a-121">Windows Server 2016</span></span>

  - <span data-ttu-id="b898a-122">Windows Server 2012 ou Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b898a-122">Windows Server 2012 or Windows Server 2012 R2</span></span>

  - <span data-ttu-id="b898a-123">Windows 7 Service Pack 1 (SP1)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="b898a-123">Windows 7 Service Pack 1 (SP1)<sup>\*</sup></span></span>

  - <span data-ttu-id="b898a-124">Windows Server 2008 R2 SP1<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="b898a-124">Windows Server 2008 R2 SP1<sup>\*</sup></span></span>

    <span data-ttu-id="b898a-p105"><sup>\*</sup> Pour les versions antérieures de Windows, vous devez installer Microsoft.NET Framework 4.5 ou version ultérieure, puis une version mise à jour de Windows Management Framework : 3.0, 4.0 ou 5.1 (une seule). Pour plus d’informations, reportez-vous à [Installer le .NET Framework pour les développeurs](https://go.microsoft.com/fwlink/p/?LinkId=257868), [Windows Management Framework 3.0](https://go.microsoft.com/fwlink/p/?LinkId=272757), [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/p/?LinkId=391344) et [Windows Management Framework 5.1](https://aka.ms/wmf5download).</span><span class="sxs-lookup"><span data-stu-id="b898a-p105"><sup>\*</sup> For older versions of Windows, you need to install the Microsoft.NET Framework 4.5 or later and then an updated version of the Windows Management Framework: 3.0, 4.0, or 5.1 (only one). For more information, see [Installing the .NET Framework](https://go.microsoft.com/fwlink/p/?LinkId=257868), [Windows Management Framework 3.0](https://go.microsoft.com/fwlink/p/?LinkId=272757), [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/p/?LinkId=391344), and [Windows Management Framework 5.1](https://aka.ms/wmf5download).</span></span>

- <span data-ttu-id="b898a-p106">Windows PowerShell doit être configuré pour exécuter des scripts, ce qui n’est pas le cas par défaut. Vous obtenez l’erreur suivante lorsque vous essayez de vous connecter :</span><span class="sxs-lookup"><span data-stu-id="b898a-p106">Windows PowerShell needs to be configured to run scripts, and by default, it isn't. You'll get the following error when you try to connect:</span></span>

  `Files cannot be loaded because running scripts is disabled on this system. Provide a valid certificate with which to sign the files.`

  <span data-ttu-id="b898a-129">Pour exiger que tous les scripts PowerShell téléchargés depuis Internet soient signés par un éditeur approuvé, exécutez la commande suivante dans une fenêtre Windows PowerShell avec élévation de privilèges (c’est-à-dire une fenêtre Windows PowerShell ouverte en sélectionnant **Exécuter en tant qu’administrateur**) :</span><span class="sxs-lookup"><span data-stu-id="b898a-129">To require all PowerShell scripts that you download from the internet are signed by a trusted publisher, run the following command in an elevated Windows PowerShell window (a Windows PowerShell window you open by selecting **Run as administrator**):</span></span>

    ```
    Set-ExecutionPolicy RemoteSigned
    ```

  <span data-ttu-id="b898a-130">Vous devez configurer ce paramètre une fois seulement sur votre ordinateur, pas à chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="b898a-130">You need to configure this setting only once on your computer, not every time you connect.</span></span>

- <span data-ttu-id="b898a-131">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, consultez la rubrique [Raccourcis clavier dans le Centre d’administration Exchange](https://go.microsoft.com/fwlink/p/?LinkId=534017).</span><span class="sxs-lookup"><span data-stu-id="b898a-131">For information about keyboard shortcuts that might apply to the procedures in this topic, see [Keyboard shortcuts in the Exchange admin center](https://go.microsoft.com/fwlink/p/?LinkId=534017).</span></span>

## <a name="connect-to-exchange-online-for-customer-organizations"></a><span data-ttu-id="b898a-132">Connexion à Exchange Online pour les organisations clientes</span><span class="sxs-lookup"><span data-stu-id="b898a-132">Connect to Exchange Online for customer organizations</span></span>

1. <span data-ttu-id="b898a-133">Sur votre ordinateur local, ouvrez Windows PowerShell et exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b898a-133">On your local computer, open Windows PowerShell and run the following command.</span></span>
    
    ```
    $UserCredential = Get-Credential
    ```

    <span data-ttu-id="b898a-134">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez vos nom d’utilisateur et mot de passe d’administrateur DAP, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b898a-134">In the **Windows PowerShell Credential Request** dialog box, enter your DAP administrator user name and password, and then click **OK**.</span></span>
    
2. <span data-ttu-id="b898a-135">Remplacez _\<customer tenant domain name\>_ par le nom du domaine client auquel vous voulez vous connecter, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b898a-135">Replace _\<customer tenant domain name\>_ with the name of the tenant domain that you want to connect to, and run the following command:</span></span>
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid?DelegatedOrg=<customer tenant domain name> -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

    <span data-ttu-id="b898a-136">Dans cette commande, l'étape clé consiste à spécifier le client auquel accéder pour les informations de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="b898a-136">The key step in this command is specifying which customer to access for the reporting information.</span></span> <span data-ttu-id="b898a-137">Pour ce faire, utilisez le paramètre  _ConnectionUri_ , dans lequel vous indiquez le nom de domaine complet du nom de domaine initial comme valeur de `?DelegatedOrg=` .</span><span class="sxs-lookup"><span data-stu-id="b898a-137">You do this in the  _ConnectionURI_ parameter, where you provide the FQDN of the initial domain name as the value for `?DelegatedOrg=`.</span></span> <span data-ttu-id="b898a-138">Cette valeur indique le point de terminaison Exchange Online PowerShell correct auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="b898a-138">This value indicates the correct Exchange Online PowerShell endpoint to connect to.</span></span> <span data-ttu-id="b898a-139">Remote PowerShell doit se connecter à Microsoft 365 Reporting dans le contexte d’un client spécifique chaque fois qu’un rapport est exécuté.</span><span class="sxs-lookup"><span data-stu-id="b898a-139">Remote PowerShell must connect to Microsoft 365 reporting in the context of a specific customer each time a report is run.</span></span> <span data-ttu-id="b898a-140">Une fois que vous vous êtes connecté à Exchange Online PowerShell, toutes les commandes suivantes sont exécutées dans le contexte du client, ce qui vous permet d’accéder à tous les rapports disponibles pour le client.</span><span class="sxs-lookup"><span data-stu-id="b898a-140">After you connect to Exchange Online PowerShell, all subsequent commands are run in the context of the customer, which gives you access to all of the available reports for the customer.</span></span>
    
3. <span data-ttu-id="b898a-141">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b898a-141">Run the following command.</span></span>
    
    ```
    Import-PSSession $Session
    ```

> [!NOTE]
> <span data-ttu-id="b898a-p108">Trois sessions simultanées peuvent être exécutées sous un seul compte au maximum. N’oubliez pas de déconnecter la session PowerShell distante dès que vous avez terminé. Si vous fermez la fenêtre Windows PowerShell sans déconnecter la session, vous risquez d’épuiser toutes les sessions PowerShell distantes à votre disposition et vous devrez attendre que les sessions expirent. Pour déconnecter la session PowerShell distante, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b898a-p108">There's a limit of three simultaneous sessions that can run under one account. Be sure to disconnect the remote PowerShell session when you're finished. If you close the Windows PowerShell window without disconnecting the session, you can use up all the remote PowerShell sessions available to you, and you'll need to wait for the sessions to expire. To disconnect the remote PowerShell session, run the following command:</span></span>

```
Remove-PSSession $Session
```
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="b898a-146">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="b898a-146">How do you know this worked?</span></span>

<span data-ttu-id="b898a-p109">Après l’étape 3, les cmdlets Exchange Online sont importées dans votre session Windows PowerShell locale comme indiqué par une barre de progression. Si vous ne recevez aucune erreur, la connexion est établie. Un test rapide consiste à exécuter une cmdlet Exchange Online (par exemple, **Get-Mailbox**) et à consulter les résultats.</span><span class="sxs-lookup"><span data-stu-id="b898a-p109">After Step 3, the Exchange Online cmdlets are imported into your local Windows PowerShell session as tracked by a progress bar. If you don't receive any errors, you connected successfully. A quick test is to run an Exchange Online cmdlet (for example, **Get-Mailbox**) and see the results.</span></span>
  
<span data-ttu-id="b898a-150">Si vous recevez des erreurs, vérifiez les conditions requises suivantes :</span><span class="sxs-lookup"><span data-stu-id="b898a-150">If you receive errors, check the following requirements:</span></span>
  
- <span data-ttu-id="b898a-p110">Un mot de passe incorrect est un problème courant. Exécutez à nouveau les trois étapes et portez une attention particulière au nom d’utilisateur et au mot de passe que vous entrez à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="b898a-p110">A common problem is an incorrect password. Run the three steps again and pay close attention to the user name and password you enter in Step 1.</span></span>
    
- <span data-ttu-id="b898a-p111">Le compte que vous utilisez pour vous connecter à Exchange Online doit être activé pour PowerShell à distance. Pour plus d’informations, reportez-vous à l’article sur la [gestion de l’accès à PowerShell à distance dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=534018).</span><span class="sxs-lookup"><span data-stu-id="b898a-p111">The account you use to connect to Exchange Online must be enabled for remote PowerShell. For more information, see [Enable or disable access to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=534018).</span></span>
    
- <span data-ttu-id="b898a-p112">Le trafic du port TCP 80 doit être ouvert entre votre ordinateur local et Exchange Online. Il est probablement ouvert, mais vous devez y penser si votre organisation a une stratégie restrictive d'accès à Internet.</span><span class="sxs-lookup"><span data-stu-id="b898a-p112">TCP port 80 traffic needs to be open between your local computer and Exchange Online. It's probably open, but it's something to consider if your organization has a restrictive Internet access policy.</span></span>
    
## <a name="call-the-cmdlet-directly-with-invoke-command"></a><span data-ttu-id="b898a-157">Appel de la cmdlet directement avec la commande Invoke</span><span class="sxs-lookup"><span data-stu-id="b898a-157">Call the cmdlet directly with Invoke-Command</span></span>

<span data-ttu-id="b898a-p113">L’importation d’une session PowerShell distante (étape 3) peut être un processus long, car _toutes_ les cmdlets Exchange Online sont importées. Cela peut représenter un problème dans le cadre du traitement par lots, par exemple, lorsque vous exécutez des rapports ou effectuez des modifications en bloc pour différents clients. En guise d’alternative à l’utilisation d’**Import-PSSession**, vous pouvez appeler les cmdlets que vous voulez utiliser directement avec **Invoke-Command**. Par exemple, pour appeler la cmdlet **Get-Mailbox**, utilisez la syntaxe suivante à la place pour la commande `Import-PSSession $Session` à l’étape 3 :</span><span class="sxs-lookup"><span data-stu-id="b898a-p113">Importing a remote PowerShell session (Step 3) can be a lengthy process because it brings in _all_ Exchange Online cmdlets. This can be an issue in batch processing (for example, when you're running reports or making bulk changes for different tenants). As an alternative to using **Import-PSSession**, you can call cmdlets you want to use directly with **Invoke-Command**. For example, to call the **Get-Milbox** cmdlet, substitute this syntax for the `Import-PSSession $Session` command in Step 3:</span></span>
  
```
Invoke-Command -Session $Session -ScriptBlock {Get-Mailbox}
```

## <a name="more-reporting-cmdlets"></a><span data-ttu-id="b898a-162">Plus de cmdlets de création de rapports</span><span class="sxs-lookup"><span data-stu-id="b898a-162">More reporting cmdlets</span></span>

<span data-ttu-id="b898a-p114">Les cmdlets que vous utilisez dans cette rubrique sont des cmdlets Windows PowerShell. Pour plus d'informations à propos de ces cmdlets, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b898a-p114">The cmdlets that you used in this topic are Windows PowerShell cmdlets. For more information about these cmdlets, see the following topics:</span></span>
  
- [<span data-ttu-id="b898a-165">Get-Credential</span><span class="sxs-lookup"><span data-stu-id="b898a-165">Get-Credential</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=389618)
    
- [<span data-ttu-id="b898a-166">New-PSSession</span><span class="sxs-lookup"><span data-stu-id="b898a-166">New-PSSession</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=389621)
    
- [<span data-ttu-id="b898a-167">Import-PSSession</span><span class="sxs-lookup"><span data-stu-id="b898a-167">Import-PSSession</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=389619)
    
- [<span data-ttu-id="b898a-168">Remove-PSSession</span><span class="sxs-lookup"><span data-stu-id="b898a-168">Remove-PSSession</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=389620)
    
- [<span data-ttu-id="b898a-169">Set-ExecutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b898a-169">Set-ExecutionPolicy</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=389623)
    

