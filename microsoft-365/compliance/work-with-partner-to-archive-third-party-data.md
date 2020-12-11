---
title: Collaborer avec un partenaire pour archiver des données tierces
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment configurer un connecteur personnalisé pour importer des données tierces à partir de sources de données telles que Salesforce chatter, Yahoo Messenger ou Yammer.
ms.openlocfilehash: 64e903604ea56e5f53e3cc154bd54459a6d8d554
ms.sourcegitcommit: 6fc6aaa2b7610e148f41018abd229e3c55b2f3d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49620210"
---
# <a name="work-with-a-partner-to-archive-third-party-data"></a><span data-ttu-id="f5af8-103">Collaborer avec un partenaire pour archiver des données tierces</span><span class="sxs-lookup"><span data-stu-id="f5af8-103">Work with a partner to archive third-party data</span></span>

<span data-ttu-id="f5af8-104">Vous pouvez collaborer avec un partenaire Microsoft pour importer et archiver des données à partir d’une source de données tierce vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-104">You can work with a Microsoft Partner to import and archive data from a third-party data source to Microsoft 365.</span></span> <span data-ttu-id="f5af8-105">Un partenaire peut vous fournir un connecteur personnalisé configuré pour extraire les éléments de la source de données tierce (de manière régulière), puis les importer.</span><span class="sxs-lookup"><span data-stu-id="f5af8-105">A partner can provide you with a custom connector that is configured to extract items from the third-party data source (on a regular basis) and then import those items.</span></span> <span data-ttu-id="f5af8-106">Le connecteur partenaire convertit le contenu d’un élément de la source de données en un format de message électronique, puis stocke les éléments dans des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="f5af8-106">The partner connector converts the content of an item from the data source to an email message format and then stores the items in mailboxes.</span></span> <span data-ttu-id="f5af8-107">Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité de Microsoft 365 telles que les stratégies de conservation pour litige, eDiscovery, In-Place archivage, d’audit et de rétention 365 à ces données.</span><span class="sxs-lookup"><span data-stu-id="f5af8-107">After third-party data is imported, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, In-Place Archiving, Auditing, and Microsoft 365 retention policies to this data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="f5af8-108">La solution de conformité de la [communication](communication-compliance.md) dans Microsoft 365 ne peut pas être appliquée aux données tierces importées par des connecteurs partenaires mentionnés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f5af8-108">The [Communication compliance](communication-compliance.md) solution in Microsoft 365 can't be applied to the third-party data imported by partner connectors mentioned in this article.</span></span> 

<span data-ttu-id="f5af8-109">Voici une vue d’ensemble du processus et des étapes nécessaires à l’utilisation d’un partenaire Microsoft pour importer des données tierces.</span><span class="sxs-lookup"><span data-stu-id="f5af8-109">Here's an overview of the process and the steps necessary to work with a Microsoft Partner to import third-party data.</span></span>

[<span data-ttu-id="f5af8-110">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="f5af8-110">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="f5af8-111">Étape 2 : création et configuration d’une boîte aux lettres de données tierce</span><span class="sxs-lookup"><span data-stu-id="f5af8-111">Step 2: Create and configure a third-party data mailbox</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-microsoft-365)

[<span data-ttu-id="f5af8-112">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="f5af8-112">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="f5af8-113">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="f5af8-113">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="f5af8-114">Étape 5 : enregistrer le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f5af8-114">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="f5af8-115">Fonctionnement du processus d’importation de données tierces</span><span class="sxs-lookup"><span data-stu-id="f5af8-115">How the third-party data import process works</span></span>

<span data-ttu-id="f5af8-116">L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tiers lors de l’utilisation d’un partenaire.</span><span class="sxs-lookup"><span data-stu-id="f5af8-116">The following illustration and description explain how the third-party data import process works when working with a partner.</span></span>
  
![Fonctionnement du processus d’importation de données tierces](../media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="f5af8-118">Le client travaille avec son partenaire de choix pour configurer un connecteur qui extrait des éléments de la source de données tierce, puis importer ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-118">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Microsoft 365.</span></span>
    
2. <span data-ttu-id="f5af8-119">Le connecteur partenaire se connecte à des sources de données tierces via une API tierce (sur la base planifiée ou configurée) et extrait des éléments de la source de données.</span><span class="sxs-lookup"><span data-stu-id="f5af8-119">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="f5af8-120">Le connecteur partenaire convertit le contenu d’un élément dans un format de message électronique.</span><span class="sxs-lookup"><span data-stu-id="f5af8-120">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="f5af8-121">Consultez la section [more information](#more-information) pour obtenir une description du schéma de format de message.</span><span class="sxs-lookup"><span data-stu-id="f5af8-121">See the [More information](#more-information) section for a description of the message-format schema.</span></span> 
    
3. <span data-ttu-id="f5af8-122">Le connecteur partenaire se connecte au service Azure dans Microsoft 365 à l’aide du service Web Exchange (EWS) via un point de terminaison connu.</span><span class="sxs-lookup"><span data-stu-id="f5af8-122">Partner connector connects to the Azure service in Microsoft 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="f5af8-p103">Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="f5af8-p103">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
   1. <span data-ttu-id="f5af8-125">**Éléments dont l’ID d’utilisateur correspond à un compte d’utilisateur :** Si le connecteur partenaire peut mapper l’ID utilisateur de l’élément dans la source de données tierce à un ID d’utilisateur spécifique dans Microsoft 365, l’élément est copié dans le dossier **purges** du dossier éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5af8-125">**Items that have a user ID that corresponds to a user account:** If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Microsoft 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="f5af8-126">Les utilisateurs ne peuvent pas accéder aux éléments du dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="f5af8-126">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="f5af8-127">Toutefois, vous pouvez utiliser les outils de découverte électronique pour rechercher des éléments dans le dossier purges.</span><span class="sxs-lookup"><span data-stu-id="f5af8-127">However, you can use eDiscovery tools to search for items in the Purges folder.</span></span>
    
   1. <span data-ttu-id="f5af8-128">**Éléments qui n’ont pas d’identifiant utilisateur correspondant à un compte d’utilisateur :** Si le connecteur partenaire ne peut pas mapper l’ID utilisateur d’un élément sur un ID d’utilisateur spécifique, l’élément est copié dans le dossier **boîte de réception** de la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="f5af8-128">**Items that don't have a user ID that corresponds to a user account:** If the partner connector can't map the user ID of an item to a specific user ID, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="f5af8-129">L’importation d’éléments dans la boîte de réception permet à un membre de votre organisation ou à vous-même de vous connecter à la boîte aux lettres tierce pour visualiser et gérer ces éléments, et de voir si des ajustements doivent être effectués dans la configuration du connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="f5af8-129">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="f5af8-130">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="f5af8-130">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="f5af8-131">Un composant clé pour l’archivage de données tierces dans Microsoft 365 est de trouver et d’utiliser un partenaire Microsoft spécialisé dans la capture de données à partir d’une source de données tierce et l’importation dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-131">A key component for archiving third-party data in Microsoft 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Microsoft 365.</span></span> <span data-ttu-id="f5af8-132">Une fois les données importées, elles peuvent être archivées et conservées avec les autres données Microsoft de votre organisation, telles que les messages électroniques provenant d’Exchange et de documents provenant de SharePoint et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="f5af8-132">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="f5af8-133">Un partenaire crée un connecteur qui extrait les données des sources de données tierces de votre organisation (par exemple, BlackBerry, Facebook, Google +, Thomson Reuters, Twitter et YouTube) et transmet ces données à une API 365 Microsoft qui importe des éléments dans les boîtes aux lettres Exchange sous forme de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="f5af8-133">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to a Microsoft 365 API that imports items to Exchange mailboxes as email messages.</span></span>
  
<span data-ttu-id="f5af8-134">Les sections suivantes répertorient les partenaires Microsoft (et les sources de données tierces qu’ils prennent en charge) qui participent au programme d’archivage de données tierces dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-134">The following sections list the Microsoft partners (and the third-party data sources they support) that are participating in the program for archiving third-party data in Microsoft 365.</span></span>

[<span data-ttu-id="f5af8-135">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="f5af8-135">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="f5af8-136">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="f5af8-136">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="f5af8-137">Globanet</span><span class="sxs-lookup"><span data-stu-id="f5af8-137">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="f5af8-138">OpenText</span><span class="sxs-lookup"><span data-stu-id="f5af8-138">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="f5af8-139">Smarsh</span><span class="sxs-lookup"><span data-stu-id="f5af8-139">Smarsh</span></span>](#smarsh)

[<span data-ttu-id="f5af8-140">Verba</span><span class="sxs-lookup"><span data-stu-id="f5af8-140">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="f5af8-141">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="f5af8-141">17a-4 LLC</span></span>

<span data-ttu-id="f5af8-142">[17A-4 LLC](https://www.17a-4.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-142">[17a-4 LLC](https://www.17a-4.com) supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="f5af8-143">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="f5af8-143">BlackBerry</span></span>
    
- <span data-ttu-id="f5af8-144">Flux de données Bloomberg</span><span class="sxs-lookup"><span data-stu-id="f5af8-144">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="f5af8-145">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="f5af8-145">Cisco Jabber</span></span>
    
- <span data-ttu-id="f5af8-146">FactSet</span><span class="sxs-lookup"><span data-stu-id="f5af8-146">FactSet</span></span>
    
- <span data-ttu-id="f5af8-147">HipChat</span><span class="sxs-lookup"><span data-stu-id="f5af8-147">HipChat</span></span>
    
- <span data-ttu-id="f5af8-148">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="f5af8-148">InvestEdge</span></span>
    
- <span data-ttu-id="f5af8-149">LivePerson</span><span class="sxs-lookup"><span data-stu-id="f5af8-149">LivePerson</span></span>
    
- <span data-ttu-id="f5af8-150">Flux de données MessageLabs</span><span class="sxs-lookup"><span data-stu-id="f5af8-150">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="f5af8-151">OpenText</span><span class="sxs-lookup"><span data-stu-id="f5af8-151">OpenText</span></span>
    
- <span data-ttu-id="f5af8-152">Aide en direct « cliquer pour appeler » Oracle/ATG</span><span class="sxs-lookup"><span data-stu-id="f5af8-152">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="f5af8-153">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="f5af8-153">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="f5af8-154">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="f5af8-154">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="f5af8-155">MindAlign</span><span class="sxs-lookup"><span data-stu-id="f5af8-155">MindAlign</span></span>
    
- <span data-ttu-id="f5af8-156">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="f5af8-156">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="f5af8-157">Skype Entreprise (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="f5af8-157">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="f5af8-158">Skype Entreprise Online (Lync Online)</span><span class="sxs-lookup"><span data-stu-id="f5af8-158">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="f5af8-159">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="f5af8-159">SQL Databases</span></span>
    
- <span data-ttu-id="f5af8-160">Squawker</span><span class="sxs-lookup"><span data-stu-id="f5af8-160">Squawker</span></span>
    
- <span data-ttu-id="f5af8-161">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="f5af8-161">Thomson Reuters Eikon Messenger</span></span>
  

  
### <a name="archivesocial"></a><span data-ttu-id="f5af8-162">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="f5af8-162">ArchiveSocial</span></span>

<span data-ttu-id="f5af8-163">[ArchiveSocial ](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-163">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="f5af8-164">Facebook</span><span class="sxs-lookup"><span data-stu-id="f5af8-164">Facebook</span></span>
    
- <span data-ttu-id="f5af8-165">Flickr</span><span class="sxs-lookup"><span data-stu-id="f5af8-165">Flickr</span></span>
    
- <span data-ttu-id="f5af8-166">Instagram</span><span class="sxs-lookup"><span data-stu-id="f5af8-166">Instagram</span></span>
    
- <span data-ttu-id="f5af8-167">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="f5af8-167">LinkedIn</span></span>
    
- <span data-ttu-id="f5af8-168">Pinterest</span><span class="sxs-lookup"><span data-stu-id="f5af8-168">Pinterest</span></span>
    
- <span data-ttu-id="f5af8-169">Twitter</span><span class="sxs-lookup"><span data-stu-id="f5af8-169">Twitter</span></span>
    
- <span data-ttu-id="f5af8-170">YouTube</span><span class="sxs-lookup"><span data-stu-id="f5af8-170">YouTube</span></span>
    
- <span data-ttu-id="f5af8-171">Vimeo</span><span class="sxs-lookup"><span data-stu-id="f5af8-171">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="f5af8-172">Globanet</span><span class="sxs-lookup"><span data-stu-id="f5af8-172">Globanet</span></span>

<span data-ttu-id="f5af8-173">[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-173">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="f5af8-174">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="f5af8-174">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="f5af8-175">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-175">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-176">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-176">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-177">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-177">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-178">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-178">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-179">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="f5af8-179">Bloomberg Chat</span></span>
    
- <span data-ttu-id="f5af8-180">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="f5af8-180">Bloomberg Mail</span></span>
    
- <span data-ttu-id="f5af8-181">Box</span><span class="sxs-lookup"><span data-stu-id="f5af8-181">Box</span></span>
    
- <span data-ttu-id="f5af8-182">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="f5af8-182">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="f5af8-183">Serveur de présence de messagerie instantanée Cisco &amp; (version 10, v 10.5.1 Su1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="f5af8-183">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="f5af8-184">Teams de Cisco Webex</span><span class="sxs-lookup"><span data-stu-id="f5af8-184">Cisco Webex Teams</span></span>

- <span data-ttu-id="f5af8-185">ShareFile de l’espace de travail de Citrix &amp;</span><span class="sxs-lookup"><span data-stu-id="f5af8-185">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="f5af8-186">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="f5af8-186">CrowdCompass</span></span>

- <span data-ttu-id="f5af8-187">Fichiers texte personnalisés, délimités</span><span class="sxs-lookup"><span data-stu-id="f5af8-187">Custom-delimited text files</span></span>
    
- <span data-ttu-id="f5af8-188">Fichiers XML personnalisés</span><span class="sxs-lookup"><span data-stu-id="f5af8-188">Custom XML files</span></span>
    
- <span data-ttu-id="f5af8-189">Facebook (pages)</span><span class="sxs-lookup"><span data-stu-id="f5af8-189">Facebook (Pages)</span></span>
    
- <span data-ttu-id="f5af8-190">Factset</span><span class="sxs-lookup"><span data-stu-id="f5af8-190">Factset</span></span>
    
- <span data-ttu-id="f5af8-191">FXConnect</span><span class="sxs-lookup"><span data-stu-id="f5af8-191">FXConnect</span></span>
    
- <span data-ttu-id="f5af8-192">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="f5af8-192">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="f5af8-193">Jive</span><span class="sxs-lookup"><span data-stu-id="f5af8-193">Jive</span></span>
    
- <span data-ttu-id="f5af8-194">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="f5af8-194">Macgregor XIP</span></span>

- <span data-ttu-id="f5af8-195">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="f5af8-195">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="f5af8-196">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="f5af8-196">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="f5af8-197">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f5af8-197">Microsoft Teams</span></span>
       
- <span data-ttu-id="f5af8-198">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="f5af8-198">Microsoft Yammer</span></span>
    
- <span data-ttu-id="f5af8-199">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="f5af8-199">Mobile Guard</span></span>
    
- <span data-ttu-id="f5af8-200">Pivot</span><span class="sxs-lookup"><span data-stu-id="f5af8-200">Pivot</span></span>
    
- <span data-ttu-id="f5af8-201">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="f5af8-201">Salesforce Chatter</span></span>

- <span data-ttu-id="f5af8-202">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="f5af8-202">Skype for Business Online</span></span>
    
- <span data-ttu-id="f5af8-203">Skype Entreprise, versions 2007 R2-2016 (sur site)</span><span class="sxs-lookup"><span data-stu-id="f5af8-203">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="f5af8-204">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="f5af8-204">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="f5af8-205">Symphony</span><span class="sxs-lookup"><span data-stu-id="f5af8-205">Symphony</span></span>
    
- <span data-ttu-id="f5af8-206">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="f5af8-206">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="f5af8-207">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="f5af8-207">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="f5af8-208">Thomson Reuters Dealings 3000/FX Trading</span><span class="sxs-lookup"><span data-stu-id="f5af8-208">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="f5af8-209">Twitter</span><span class="sxs-lookup"><span data-stu-id="f5af8-209">Twitter</span></span>
    
- <span data-ttu-id="f5af8-210">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="f5af8-210">UBS Chat</span></span>
    
- <span data-ttu-id="f5af8-211">YouTube</span><span class="sxs-lookup"><span data-stu-id="f5af8-211">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="f5af8-212">OpenText</span><span class="sxs-lookup"><span data-stu-id="f5af8-212">OpenText</span></span>

<span data-ttu-id="f5af8-213">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-213">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="f5af8-214">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="f5af8-214">Axs Encrypted</span></span>
    
- <span data-ttu-id="f5af8-215">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="f5af8-215">Axs Exchange</span></span>
    
- <span data-ttu-id="f5af8-216">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="f5af8-216">Axs Local Archive</span></span>
    
- <span data-ttu-id="f5af8-217">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="f5af8-217">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="f5af8-218">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="f5af8-218">Axs Signed</span></span>
    
- <span data-ttu-id="f5af8-219">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="f5af8-219">Bloomberg</span></span>
    
- <span data-ttu-id="f5af8-220">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="f5af8-220">Thomson Reuters</span></span>
  
### <a name="smarsh"></a><span data-ttu-id="f5af8-221">Smarsh</span><span class="sxs-lookup"><span data-stu-id="f5af8-221">Smarsh</span></span>

<span data-ttu-id="f5af8-222">[Smarsh](https://www.smarsh.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-222">[Smarsh](https://www.smarsh.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="f5af8-223">VISERA</span><span class="sxs-lookup"><span data-stu-id="f5af8-223">AIM</span></span>
    
- <span data-ttu-id="f5af8-224">American Idol</span><span class="sxs-lookup"><span data-stu-id="f5af8-224">American Idol</span></span>
    
- <span data-ttu-id="f5af8-225">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="f5af8-225">Apple Juice</span></span>
    
- <span data-ttu-id="f5af8-226">AOL avec client Pivot</span><span class="sxs-lookup"><span data-stu-id="f5af8-226">AOL with Pivot client</span></span>
    
- <span data-ttu-id="f5af8-227">Tréma</span><span class="sxs-lookup"><span data-stu-id="f5af8-227">Ares</span></span>
    
- <span data-ttu-id="f5af8-228">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-228">Bazaar Voice</span></span>
    
- <span data-ttu-id="f5af8-229">Bear Share</span><span class="sxs-lookup"><span data-stu-id="f5af8-229">Bear Share</span></span>
    
- <span data-ttu-id="f5af8-230">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="f5af8-230">Bit Torrent</span></span>
    
- <span data-ttu-id="f5af8-231">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-231">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-232">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-232">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-233">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-233">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-234">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="f5af8-234">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="f5af8-235">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="f5af8-235">Bloomberg Mail</span></span>
    
- <span data-ttu-id="f5af8-236">CellTrust</span><span class="sxs-lookup"><span data-stu-id="f5af8-236">CellTrust</span></span>
    
- <span data-ttu-id="f5af8-237">Chat Import</span><span class="sxs-lookup"><span data-stu-id="f5af8-237">Chat Import</span></span>
    
- <span data-ttu-id="f5af8-238">Chat Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="f5af8-238">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="f5af8-239">Brouillage</span><span class="sxs-lookup"><span data-stu-id="f5af8-239">Chatter</span></span>
    
- <span data-ttu-id="f5af8-240">&amp;Serveur de présence de messagerie instantanée Cisco (version 9.0.1, version 9.1, v 9.1.1 Su1, version 10, v 10.5.1 Su1)</span><span class="sxs-lookup"><span data-stu-id="f5af8-240">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="f5af8-241">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="f5af8-241">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="f5af8-242">Collaboration Import</span><span class="sxs-lookup"><span data-stu-id="f5af8-242">Collaboration Import</span></span>
    
- <span data-ttu-id="f5af8-243">Collaboration Real Time Logging</span><span class="sxs-lookup"><span data-stu-id="f5af8-243">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="f5af8-244">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="f5af8-244">Direct Connect</span></span>
    
- <span data-ttu-id="f5af8-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="f5af8-245">Facebook</span></span>
    
- <span data-ttu-id="f5af8-246">FactSet</span><span class="sxs-lookup"><span data-stu-id="f5af8-246">FactSet</span></span>
    
- <span data-ttu-id="f5af8-247">FastTrack</span><span class="sxs-lookup"><span data-stu-id="f5af8-247">FastTrack</span></span>
    
- <span data-ttu-id="f5af8-248">Gnutella</span><span class="sxs-lookup"><span data-stu-id="f5af8-248">Gnutella</span></span>
    
- <span data-ttu-id="f5af8-249">Google +</span><span class="sxs-lookup"><span data-stu-id="f5af8-249">Google+</span></span>
    
- <span data-ttu-id="f5af8-250">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="f5af8-250">GoToMyPC</span></span>
    
- <span data-ttu-id="f5af8-251">Hopster</span><span class="sxs-lookup"><span data-stu-id="f5af8-251">Hopster</span></span>
    
- <span data-ttu-id="f5af8-252">HubConnex</span><span class="sxs-lookup"><span data-stu-id="f5af8-252">HubConnex</span></span>
    
- <span data-ttu-id="f5af8-253">IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)</span><span class="sxs-lookup"><span data-stu-id="f5af8-253">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="f5af8-254">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="f5af8-254">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="f5af8-255">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="f5af8-255">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="f5af8-256">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="f5af8-256">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="f5af8-257">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="f5af8-257">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="f5af8-258">IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)</span><span class="sxs-lookup"><span data-stu-id="f5af8-258">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="f5af8-259">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="f5af8-259">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="f5af8-260">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="f5af8-260">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="f5af8-261">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="f5af8-261">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="f5af8-262">GLACE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="f5af8-262">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="f5af8-263">IM Import</span><span class="sxs-lookup"><span data-stu-id="f5af8-263">IM Import</span></span>
    
- <span data-ttu-id="f5af8-264">IM Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="f5af8-264">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="f5af8-265">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="f5af8-265">Indii Messenger</span></span>
    
- <span data-ttu-id="f5af8-266">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="f5af8-266">Instant Bloomberg</span></span>
    
- <span data-ttu-id="f5af8-267">SALLE</span><span class="sxs-lookup"><span data-stu-id="f5af8-267">IRC</span></span>
    
- <span data-ttu-id="f5af8-268">Jive</span><span class="sxs-lookup"><span data-stu-id="f5af8-268">Jive</span></span>
    
- <span data-ttu-id="f5af8-269">Jive 6 Real Time Logging (version 6, version 7)</span><span class="sxs-lookup"><span data-stu-id="f5af8-269">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="f5af8-270">Jive Import</span><span class="sxs-lookup"><span data-stu-id="f5af8-270">Jive Import</span></span>
    
- <span data-ttu-id="f5af8-271">JXTA</span><span class="sxs-lookup"><span data-stu-id="f5af8-271">JXTA</span></span>
    
- <span data-ttu-id="f5af8-272">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="f5af8-272">LinkedIn</span></span>
    
- <span data-ttu-id="f5af8-273">Microsoft Lync (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="f5af8-273">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="f5af8-274">MFTP</span><span class="sxs-lookup"><span data-stu-id="f5af8-274">MFTP</span></span>
    
- <span data-ttu-id="f5af8-275">Microsoft Lync 2013 Voix</span><span class="sxs-lookup"><span data-stu-id="f5af8-275">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="f5af8-276">Microsoft SharePoint (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="f5af8-276">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="f5af8-277">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="f5af8-277">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="f5af8-278">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="f5af8-278">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="f5af8-279">MindAlign</span><span class="sxs-lookup"><span data-stu-id="f5af8-279">MindAlign</span></span>
    
- <span data-ttu-id="f5af8-280">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="f5af8-280">Mobile Guard</span></span>
    
- <span data-ttu-id="f5af8-281">SYMPATICO</span><span class="sxs-lookup"><span data-stu-id="f5af8-281">MSN</span></span>
    
- <span data-ttu-id="f5af8-282">My Space</span><span class="sxs-lookup"><span data-stu-id="f5af8-282">My Space</span></span>
    
- <span data-ttu-id="f5af8-283">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="f5af8-283">NEONetwork</span></span>
    
- <span data-ttu-id="f5af8-284">Microsoft 365 Lync dédié</span><span class="sxs-lookup"><span data-stu-id="f5af8-284">Microsoft 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="f5af8-285">Messagerie instantanée partagée Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f5af8-285">Microsoft 365 Shared IM</span></span>
    
- <span data-ttu-id="f5af8-286">Pinterest</span><span class="sxs-lookup"><span data-stu-id="f5af8-286">Pinterest</span></span>
    
- <span data-ttu-id="f5af8-287">Pivot</span><span class="sxs-lookup"><span data-stu-id="f5af8-287">Pivot</span></span>
    
- <span data-ttu-id="f5af8-288">QQ</span><span class="sxs-lookup"><span data-stu-id="f5af8-288">QQ</span></span>
    
- <span data-ttu-id="f5af8-289">Skype Entreprise 2015</span><span class="sxs-lookup"><span data-stu-id="f5af8-289">Skype for Business 2015</span></span>
    
- <span data-ttu-id="f5af8-290">SoftEther</span><span class="sxs-lookup"><span data-stu-id="f5af8-290">SoftEther</span></span>
    
- <span data-ttu-id="f5af8-291">Symphony</span><span class="sxs-lookup"><span data-stu-id="f5af8-291">Symphony</span></span>
    
- <span data-ttu-id="f5af8-292">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="f5af8-292">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="f5af8-293">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="f5af8-293">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="f5af8-294">Termes</span><span class="sxs-lookup"><span data-stu-id="f5af8-294">Tor</span></span>
    
- <span data-ttu-id="f5af8-295">TTT</span><span class="sxs-lookup"><span data-stu-id="f5af8-295">TTT</span></span>
    
- <span data-ttu-id="f5af8-296">Twitter</span><span class="sxs-lookup"><span data-stu-id="f5af8-296">Twitter</span></span>
    
- <span data-ttu-id="f5af8-297">WinMX</span><span class="sxs-lookup"><span data-stu-id="f5af8-297">WinMX</span></span>
    
- <span data-ttu-id="f5af8-298">Winny</span><span class="sxs-lookup"><span data-stu-id="f5af8-298">Winny</span></span>
    
- <span data-ttu-id="f5af8-299">Yahoo</span><span class="sxs-lookup"><span data-stu-id="f5af8-299">Yahoo</span></span>
    
- <span data-ttu-id="f5af8-300">Yammer</span><span class="sxs-lookup"><span data-stu-id="f5af8-300">Yammer</span></span>
    
- <span data-ttu-id="f5af8-301">YouTube</span><span class="sxs-lookup"><span data-stu-id="f5af8-301">YouTube</span></span>
    

### <a name="verba"></a><span data-ttu-id="f5af8-302">Verba</span><span class="sxs-lookup"><span data-stu-id="f5af8-302">Verba</span></span>

<span data-ttu-id="f5af8-303">[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-303">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="f5af8-304">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="f5af8-304">Avaya Aura Video</span></span>
    
- <span data-ttu-id="f5af8-305">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-305">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="f5af8-306">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="f5af8-306">Avtec Radio</span></span>
    
- <span data-ttu-id="f5af8-307">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="f5af8-307">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="f5af8-308">BroadSoft Video</span><span class="sxs-lookup"><span data-stu-id="f5af8-308">BroadSoft Video</span></span>
    
- <span data-ttu-id="f5af8-309">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-309">BroadSoft Voice</span></span>
    
- <span data-ttu-id="f5af8-310">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-310">Centile Voice</span></span>
    
- <span data-ttu-id="f5af8-311">Cisco Jabber IM</span><span class="sxs-lookup"><span data-stu-id="f5af8-311">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="f5af8-312">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="f5af8-312">Cisco UC Video</span></span>
    
- <span data-ttu-id="f5af8-313">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-313">Cisco UC Voice</span></span>
    
- <span data-ttu-id="f5af8-314">Cisco UCCX/UCCE vidéo</span><span class="sxs-lookup"><span data-stu-id="f5af8-314">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="f5af8-315">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-315">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="f5af8-316">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="f5af8-316">ESChat Radio</span></span>
    
- <span data-ttu-id="f5af8-317">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="f5af8-317">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="f5af8-318">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-318">IP Trade Voice</span></span>
    
- <span data-ttu-id="f5af8-319">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="f5af8-319">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="f5af8-320">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="f5af8-320">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="f5af8-321">Mitel MiContact Center for Lync (prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="f5af8-321">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="f5af8-322">Oracle / Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="f5af8-322">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="f5af8-323">Oracle / Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-323">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="f5af8-324">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-324">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="f5af8-325">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="f5af8-325">SIPREC Video</span></span>
    
-  <span data-ttu-id="f5af8-326">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-326">SIPREC Voice</span></span> 
    
- <span data-ttu-id="f5af8-327">Skype Entreprise / MI Lync</span><span class="sxs-lookup"><span data-stu-id="f5af8-327">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="f5af8-328">Skype Entreprise / Vidéo Lync</span><span class="sxs-lookup"><span data-stu-id="f5af8-328">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="f5af8-329">Skype Entreprise / Voix Lync</span><span class="sxs-lookup"><span data-stu-id="f5af8-329">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="f5af8-330">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-330">Speakerbus Voice</span></span>
    
- <span data-ttu-id="f5af8-331">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="f5af8-331">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="f5af8-332">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-332">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="f5af8-333">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="f5af8-333">Truphone Voice</span></span>
    
- <span data-ttu-id="f5af8-334">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="f5af8-334">TwistedPair Radio</span></span>
    
- <span data-ttu-id="f5af8-335">Écran d’ordinateur de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="f5af8-335">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-microsoft-365"></a><span data-ttu-id="f5af8-336">Étape 2 : créez et configurez une boîte aux lettres de données tierce dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f5af8-336">Step 2: Create and configure a third-party data mailbox in Microsoft 365</span></span>

<span data-ttu-id="f5af8-337">Voici les étapes à suivre pour créer et configurer une boîte aux lettres de données tierce pour l’importation de données vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-337">Here are the steps for creating and configuring a third-party data mailbox for importing data to Microsoft 365.</span></span> <span data-ttu-id="f5af8-338">Comme indiqué précédemment, les éléments sont importés dans cette boîte aux lettres si le connecteur partenaire ne peut pas mapper l’ID utilisateur de l’élément sur un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5af8-338">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to a user account.</span></span>
  
 <span data-ttu-id="f5af8-339">**Effectuez ces tâches dans le centre d’administration Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="f5af8-339">**Complete these tasks in the Microsoft 365 admin center**</span></span>
  
1. <span data-ttu-id="f5af8-340">Créez un compte d’utilisateur et attribuez-lui une licence Exchange Online plan 2 ; Voir [Ajouter des utilisateurs à Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span><span class="sxs-lookup"><span data-stu-id="f5af8-340">Create a user account and assign it an Exchange Online Plan 2 license; see [Add users to Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span></span> <span data-ttu-id="f5af8-341">Une licence plan 2 est nécessaire pour placer la boîte aux lettres en conservation pour litige ou pour activer une boîte aux lettres d’archivage dont le quota de stockage est illimité.</span><span class="sxs-lookup"><span data-stu-id="f5af8-341">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="f5af8-342">Ajoutez le compte d’utilisateur pour la boîte aux lettres de données tierce au rôle **administrateur d’administrateur Exchange** dans Microsoft 365 ; consultez la rubrique [attribuer des rôles d’administrateur dans Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="f5af8-342">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Microsoft 365; see [Assign admin roles in Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f5af8-343">Notez les informations d’identification pour ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5af8-343">Write down the credentials for this user account.</span></span> <span data-ttu-id="f5af8-344">Vous devez les fournir à votre partenaire, comme décrit à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="f5af8-344">You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="f5af8-345">**Effectuer ces tâches dans le centre d’administration Exchange**</span><span class="sxs-lookup"><span data-stu-id="f5af8-345">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="f5af8-346">Masquer la boîte aux lettres de données tierce dans le carnet d’adresses et les autres listes d’adresses de votre organisation ; consultez la rubrique [Manage User mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span><span class="sxs-lookup"><span data-stu-id="f5af8-346">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span></span> <span data-ttu-id="f5af8-347">Vous pouvez également exécuter la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="f5af8-347">Alternatively, you can run the following PowerShell command:</span></span>
    
    ```powershell
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="f5af8-348">Attribuer l’autorisation **FullAccess** à la boîte aux lettres de données tierce afin que les administrateurs ou les responsables de la mise en conformité puissent ouvrir la boîte aux lettres de données tierce dans le client de bureau Outlook ; consultez la rubrique [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="f5af8-348">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="f5af8-349">Activez les fonctionnalités liées à la conformité suivantes pour la boîte aux lettres de données tierce :</span><span class="sxs-lookup"><span data-stu-id="f5af8-349">Enable the following compliance-related features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="f5af8-350">Activer la boîte aux lettres d’archivage ; consultez la rubrique [activation des boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [activez un archivage illimité](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="f5af8-350">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="f5af8-351">Cela vous permet de libérer de l’espace de stockage dans la boîte aux lettres principale en configurant une stratégie d’archivage qui déplace les éléments de données tiers vers la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="f5af8-351">This lets you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="f5af8-352">Vous disposez ainsi d’un espace de stockage illimité pour les données tierces.</span><span class="sxs-lookup"><span data-stu-id="f5af8-352">This provides you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="f5af8-353">Placez la boîte aux lettres de données tierces en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="f5af8-353">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="f5af8-354">Vous pouvez également appliquer une stratégie de rétention Microsoft 365 dans le centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="f5af8-354">You can also apply a Microsoft 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="f5af8-355">Le fait de placer cette boîte aux lettres en conservation conserve des éléments de données tiers (indéfiniment ou pour une durée spécifiée) et les empêche d’être purgés de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="f5af8-355">Placing this mailbox on hold retains third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="f5af8-356">Consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-356">See one of the following topics:</span></span>
    
      - [<span data-ttu-id="f5af8-357">Placer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="f5af8-357">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="f5af8-358">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="f5af8-358">Learn about retention policies and retention labels</span></span>](retention.md)
    
    - <span data-ttu-id="f5af8-359">Activez l’enregistrement d’audit des boîtes aux lettres pour l’accès des propriétaires, des délégués et des administrateurs à la boîte aux lettres de données tierce. Voir [activer l’audit de boîte aux lettres](enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="f5af8-359">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="f5af8-360">Cela vous permet d’auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="f5af8-360">This allows you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="f5af8-361">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="f5af8-361">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="f5af8-362">L’étape suivante consiste à configurer les boîtes aux lettres des utilisateurs pour prendre en charge les données tierces.</span><span class="sxs-lookup"><span data-stu-id="f5af8-362">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="f5af8-363">Effectuez ces tâches à l’aide du centre d’administration Exchange ou à l’aide des applets de commande Windows PowerShell correspondantes.</span><span class="sxs-lookup"><span data-stu-id="f5af8-363">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="f5af8-364">Activez la boîte aux lettres d’archivage pour chaque utilisateur ; consultez la rubrique [activation des boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [activez un archivage illimité](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="f5af8-364">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="f5af8-365">Placer les boîtes aux lettres utilisateur en conservation pour litige ou appliquer une stratégie de rétention Microsoft 365 ; consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-365">Place user mailboxes on Litigation Hold or apply a Microsoft 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="f5af8-366">Placer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="f5af8-366">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="f5af8-367">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="f5af8-367">Learn about retention policies and retention labels</span></span>](retention.md)
    
    <span data-ttu-id="f5af8-368">Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="f5af8-368">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="f5af8-369">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="f5af8-369">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="f5af8-370">La dernière étape consiste à fournir à votre partenaire les informations suivantes afin qu’il puisse configurer le connecteur de sorte qu’il se connecte à votre organisation pour importer les données dans les boîtes aux lettres utilisateur et dans la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="f5af8-370">The final step is to provide your partner with the following information so they can configure the connector to connect to your organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="f5af8-371">Le point de terminaison utilisé pour se connecter au service Azure dans Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="f5af8-371">The endpoint used to connect to the Azure service in Microsoft 365:</span></span>

    ```http
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="f5af8-372">Les informations d’identification de connexion (ID d’utilisateur et mot de passe Microsoft 365) de la boîte aux lettres de données tierce que vous avez créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="f5af8-372">The sign-in credentials (Microsoft 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="f5af8-373">Ces informations d’identification sont requises pour que le connecteur partenaire puisse accéder aux éléments et les importer dans les boîtes aux lettres utilisateur et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="f5af8-373">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="f5af8-374">Étape 5 : enregistrer le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f5af8-374">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="f5af8-375">À partir du 30 septembre 2018, le service Azure de Microsoft 365 commencera à utiliser l’authentification moderne dans Exchange Online pour authentifier les connecteurs de données tiers qui tentent de se connecter à votre organisation pour importer des données.</span><span class="sxs-lookup"><span data-stu-id="f5af8-375">Starting September 30, 2018, the Azure service in Microsoft 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your organization to import data.</span></span> <span data-ttu-id="f5af8-376">La raison de cette modification est que l’authentification moderne fournit davantage de sécurité que la méthode actuelle, basée sur une liste verte pour les connecteurs tiers qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.</span><span class="sxs-lookup"><span data-stu-id="f5af8-376">The reason for this change is that modern authentication provides more security than the current method, which was based on an allow list for third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="f5af8-377">Pour permettre à un connecteur de données tiers de se connecter à Microsoft 365 à l’aide de la nouvelle méthode d’authentification moderne, un administrateur de votre organisation doit consentir à inscrire le connecteur en tant qu’application de service approuvée dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5af8-377">To enable a third-party data connector to connect to Microsoft 365 using the new modern authentication method, an administrator in your organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="f5af8-378">Pour ce faire, vous devez accepter une demande d’autorisation pour permettre au connecteur d’accéder aux données de votre organisation dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5af8-378">This is done by accepting a permission request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="f5af8-379">Une fois que vous avez accepté cette demande, le connecteur de données tiers est ajouté en tant qu’application d’entreprise à Azure Active Directory et représenté en tant que principal de service.</span><span class="sxs-lookup"><span data-stu-id="f5af8-379">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="f5af8-380">Pour plus d’informations sur le processus de consentement, consultez la rubrique consentement de l'  [administrateur client](https://docs.microsoft.com/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="f5af8-380">For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="f5af8-381">Voici les étapes à suivre pour accéder à la demande et l’accepter pour enregistrer le connecteur :</span><span class="sxs-lookup"><span data-stu-id="f5af8-381">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="f5af8-382">Accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et connectez-vous à l’aide des informations d’identification d’un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="f5af8-382">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of a global administrator.</span></span>

   <span data-ttu-id="f5af8-383">La boîte de dialogue suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f5af8-383">The following dialog box is displayed.</span></span> <span data-ttu-id="f5af8-384">Vous pouvez développer les signes pour vérifier les autorisations qui seront affectées au connecteur.</span><span class="sxs-lookup"><span data-stu-id="f5af8-384">You can expand the carets to review the permissions that will be assigned to the connector.</span></span>

   ![La boîte de dialogue demande d’autorisations s’affiche.](../media/O365-ThirdPartyDataConnector-OptIn1.png)

2. <span data-ttu-id="f5af8-386">Cliquez sur **Accept (Accepter)**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-386">Click **Accept**.</span></span>

<span data-ttu-id="f5af8-387">Une fois que vous avez accepté la demande, le [portail Azure](https://portal.azure.com) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f5af8-387">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="f5af8-388">Pour afficher la liste des applications pour votre organisation, cliquez sur applications d’entreprise **Azure Active Directory**  >  .</span><span class="sxs-lookup"><span data-stu-id="f5af8-388">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="f5af8-389">Le connecteur de données tiers 365 de Microsoft est affiché dans le panneau **applications d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="f5af8-389">The Microsoft 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5af8-390">Après le 30 septembre 2018, les données tierces ne seront plus importées dans les boîtes aux lettres de votre organisation si vous n’enregistrez pas un connecteur de données tiers dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5af8-390">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="f5af8-391">Remarque les connecteurs de données tiers existants (ceux créés avant le 30 septembre 2018) doivent également être enregistrés dans Azure Active Directory en suivant la procédure de l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="f5af8-391">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="f5af8-392">Révocation du consentement pour un connecteur de données tiers</span><span class="sxs-lookup"><span data-stu-id="f5af8-392">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="f5af8-393">Une fois que votre organisation a accepté la demande d’autorisations pour enregistrer un connecteur de données tiers dans Azure Active Directory, votre organisation peut révoquer ce consentement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f5af8-393">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="f5af8-394">Toutefois, la révocation de l’autorisation pour un connecteur signifie que les données de la source de données tierce ne seront plus importées dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-394">However, revoking the consent for a connector means that data from the third-party data source will no longer be imported into Microsoft 365.</span></span>

<span data-ttu-id="f5af8-395">Pour révoquer le consentement d’un connecteur de données tiers, vous pouvez supprimer l’application (en supprimant l’entité de service correspondante) à partir d’Azure Active Directory à l’aide du panneau **applications d’entreprise** dans le portail Azure ou en utilisant la commande [Remove-MsolServicePrincipal](https://docs.microsoft.com/powershell/module/msonline/remove-msolserviceprincipal) dans Microsoft 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5af8-395">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/powershell/module/msonline/remove-msolserviceprincipal) in Microsoft 365 PowerShell.</span></span> <span data-ttu-id="f5af8-396">Vous pouvez également utiliser l’applet de commande [Remove-AzureADServicePrincipal](https://docs.microsoft.com/powershell/module/azuread/remove-azureadserviceprincipal) dans Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5af8-396">You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="f5af8-397">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f5af8-397">More information</span></span>

- <span data-ttu-id="f5af8-398">Comme indiqué précédemment, les éléments des sources de données tierces sont importés vers les boîtes aux lettres Exchange en tant que messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="f5af8-398">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="f5af8-399">Le connecteur partenaire importe l’élément à l’aide d’un schéma requis par l’API 365 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5af8-399">The partner connector imports the item using a schema required by the Microsoft 365 API.</span></span> <span data-ttu-id="f5af8-400">Le tableau suivant décrit les propriétés de message d’un élément d’une source de données tierces après son importation vers une boîte aux lettres Exchange en tant que message électronique.</span><span class="sxs-lookup"><span data-stu-id="f5af8-400">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="f5af8-401">Le tableau indique également si la propriété de message est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f5af8-401">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="f5af8-402">Les propriétés obligatoires doivent être renseignées.</span><span class="sxs-lookup"><span data-stu-id="f5af8-402">Mandatory properties must be populated.</span></span> <span data-ttu-id="f5af8-403">Si une propriété obligatoire est manquante dans un élément, celui-ci ne sera pas importé dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-403">If an item is missing a mandatory property, it won't be imported to Microsoft 365.</span></span> <span data-ttu-id="f5af8-404">Le processus d’importation renvoie un message d’erreur expliquant pourquoi un élément n’a pas été importé et quelle est la propriété manquante.</span><span class="sxs-lookup"><span data-stu-id="f5af8-404">The import process returns an error message explaining why an item wasn't imported and which property is missing.</span></span><br/><br/>
    
    |<span data-ttu-id="f5af8-405">**Propriété de message**</span><span class="sxs-lookup"><span data-stu-id="f5af8-405">**Message property**</span></span>|<span data-ttu-id="f5af8-406">**Obligatoire ?**</span><span class="sxs-lookup"><span data-stu-id="f5af8-406">**Mandatory?**</span></span>|<span data-ttu-id="f5af8-407">**Description**</span><span class="sxs-lookup"><span data-stu-id="f5af8-407">**Description**</span></span>|<span data-ttu-id="f5af8-408">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="f5af8-408">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f5af8-409">**FROM**</span><span class="sxs-lookup"><span data-stu-id="f5af8-409">**FROM**</span></span> <br/> |<span data-ttu-id="f5af8-410">Oui</span><span class="sxs-lookup"><span data-stu-id="f5af8-410">Yes</span></span>  <br/> |<span data-ttu-id="f5af8-411">Utilisateur qui a initialement créé ou envoyé l’élément dans la source de données tierces.</span><span class="sxs-lookup"><span data-stu-id="f5af8-411">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="f5af8-412">Le connecteur partenaire tente de mapper l’ID utilisateur à partir de l’élément source (par exemple, un handle Twitter) sur un compte d’utilisateur pour tous les participants (les utilisateurs figurant dans les champs de et à).</span><span class="sxs-lookup"><span data-stu-id="f5af8-412">The partner connector attempts to map the user ID from the source item (for example a Twitter handle) to a user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="f5af8-413">Une copie du message sera importée dans la boîte aux lettres de chaque participant.</span><span class="sxs-lookup"><span data-stu-id="f5af8-413">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="f5af8-414">Si aucun des participants de l’élément ne peut être mappé à un compte d’utilisateur, l’élément sera importé dans la boîte aux lettres d’archivage tierce dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f5af8-414">If none of the participants from the item can be mapped to a user account, the item will be imported to the third-party archiving mailbox in Microsoft 365.</span></span>  <br/> <br/> <span data-ttu-id="f5af8-415">Le participant identifié comme l’expéditeur de l’élément doit disposer d’une boîte aux lettres active dans l’organisation dans laquelle l’élément est importé.</span><span class="sxs-lookup"><span data-stu-id="f5af8-415">The participant who's identified as the sender of the item must have an active mailbox in the organization that the item is being imported to.</span></span> <span data-ttu-id="f5af8-416">Si l’expéditeur ne dispose pas d’une boîte aux lettres active, l’erreur suivante est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="f5af8-416">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="f5af8-417">**TO**</span><span class="sxs-lookup"><span data-stu-id="f5af8-417">**TO**</span></span> <br/> |<span data-ttu-id="f5af8-418">Oui</span><span class="sxs-lookup"><span data-stu-id="f5af8-418">Yes</span></span>  <br/> |<span data-ttu-id="f5af8-419">Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="f5af8-419">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="f5af8-420">**Objet**</span><span class="sxs-lookup"><span data-stu-id="f5af8-420">**SUBJECT**</span></span> <br/> |<span data-ttu-id="f5af8-421">Non</span><span class="sxs-lookup"><span data-stu-id="f5af8-421">No</span></span>  <br/> |<span data-ttu-id="f5af8-422">Objet de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="f5af8-422">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="f5af8-423">**JOURS**</span><span class="sxs-lookup"><span data-stu-id="f5af8-423">**DATE**</span></span> <br/> |<span data-ttu-id="f5af8-424">Oui</span><span class="sxs-lookup"><span data-stu-id="f5af8-424">Yes</span></span>  <br/> |<span data-ttu-id="f5af8-425">Date à laquelle l’élément a été initialement créé ou publié dans la source de données client.</span><span class="sxs-lookup"><span data-stu-id="f5af8-425">The date the item was originally created or posted in the customer data source.</span></span> <span data-ttu-id="f5af8-426">Par exemple, la date à laquelle un message Twitter a été tweeté.</span><span class="sxs-lookup"><span data-stu-id="f5af8-426">For example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="f5af8-427">**ENTITÉ**</span><span class="sxs-lookup"><span data-stu-id="f5af8-427">**BODY**</span></span> <br/> |<span data-ttu-id="f5af8-428">Non</span><span class="sxs-lookup"><span data-stu-id="f5af8-428">No</span></span>  <br/> |<span data-ttu-id="f5af8-429">Contenu du message ou de la publication.</span><span class="sxs-lookup"><span data-stu-id="f5af8-429">The contents of the message or post.</span></span> <span data-ttu-id="f5af8-430">Pour certaines sources de données, le contenu de cette propriété peut être identique au contenu de la propriété **SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-430">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="f5af8-431">Pendant le processus d’importation, le connecteur partenaire tente de maintenir la fidélité complète de la source de contenu.</span><span class="sxs-lookup"><span data-stu-id="f5af8-431">During the import process, the partner connector attempts to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="f5af8-432">Si possible, les fichiers, les graphiques ou tout autre contenu du corps de l’élément source sont inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="f5af8-432">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="f5af8-433">Sinon, le contenu de l’élément source est inclus dans la propriété **ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-433">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="f5af8-434">Le contenu de cette propriété dépend du connecteur du partenaire et de la capacité de la plateforme source.</span><span class="sxs-lookup"><span data-stu-id="f5af8-434">The contents of this property depends on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="f5af8-435">**CONNEXION**</span><span class="sxs-lookup"><span data-stu-id="f5af8-435">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="f5af8-436">Non</span><span class="sxs-lookup"><span data-stu-id="f5af8-436">No</span></span>  <br/> |<span data-ttu-id="f5af8-437">Si un élément de la source de données (par exemple, un tweet dans Twitter ou une conversation de messagerie instantanée) a un fichier joint ou inclut des images, le partenaire Connect tente d’abord d’inclure les pièces jointes dans la propriété **Body** .</span><span class="sxs-lookup"><span data-stu-id="f5af8-437">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="f5af8-438">Si cela n’est pas possible, il est ajouté à la propriété \* \* ATTACHment \* \*.</span><span class="sxs-lookup"><span data-stu-id="f5af8-438">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="f5af8-439">Voici d’autres exemples de pièces jointes : mentions J’aime sur Facebook, métadonnées de la source de contenu et réponses à un message ou une publication.</span><span class="sxs-lookup"><span data-stu-id="f5af8-439">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |<span data-ttu-id="f5af8-440">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="f5af8-440">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="f5af8-441">Oui</span><span class="sxs-lookup"><span data-stu-id="f5af8-441">Yes</span></span>  <br/> | <span data-ttu-id="f5af8-442">Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par le connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="f5af8-442">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="f5af8-443">Le format de cette propriété est  `IPM.NOTE.Source.Event` .</span><span class="sxs-lookup"><span data-stu-id="f5af8-443">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="f5af8-444">(Cette propriété doit commencer par  `IPM.NOTE` .</span><span class="sxs-lookup"><span data-stu-id="f5af8-444">(This property must begin with  `IPM.NOTE`.</span></span> <span data-ttu-id="f5af8-445">Ce format est similaire à celui de la  `IPM.NOTE.X` classe message.) Cette propriété inclut les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5af8-445">This format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/><span data-ttu-id="f5af8-446">`Source`: Indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="f5af8-446">`Source`: Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="f5af8-447">`Event`: Indique le type d’activité qui a été effectué dans la source de données tierce qui a produit les éléments ; par exemple, un tweet dans Twitter ou un billet dans Facebook.</span><span class="sxs-lookup"><span data-stu-id="f5af8-447">`Event`: Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="f5af8-448">Les événements sont propres à la source de données.</span><span class="sxs-lookup"><span data-stu-id="f5af8-448">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="f5af8-449">L’un des objectifs de cette propriété est de filtrer des éléments spécifiques en fonction de la source de données d’origine d’un élément ou en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="f5af8-449">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="f5af8-450">Par exemple, lors d’une recherche de découverte électronique, vous pouvez créer une requête de recherche afin de trouver tous les tweets qui ont été publiés par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f5af8-450">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="f5af8-451">Lorsque des éléments sont correctement importés dans des boîtes aux lettres dans Microsoft 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5af8-451">When items are successfully imported to mailboxes in Microsoft 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="f5af8-452">Cet identificateur, appelé  `x-IngestionCorrelationID` , peut être utilisé à des fins de dépannage ultérieure par les partenaires pour le suivi de bout en bout des éléments.</span><span class="sxs-lookup"><span data-stu-id="f5af8-452">This identifier, called  `x-IngestionCorrelationID`, can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="f5af8-453">Nous recommandons que vos partenaires récupèrent ces informations et les conservent de leur côté.</span><span class="sxs-lookup"><span data-stu-id="f5af8-453">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="f5af8-454">Voici un exemple d’une réponse HTTP avec cet identifiant :</span><span class="sxs-lookup"><span data-stu-id="f5af8-454">Here's an example of an HTTP response showing this identifier:</span></span>

    ```http
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```

- <span data-ttu-id="f5af8-455">Vous pouvez utiliser l’outil de recherche de contenu dans le centre de sécurité et de conformité pour rechercher des éléments qui ont été importés dans des boîtes aux lettres à partir d’une source de données tierce.</span><span class="sxs-lookup"><span data-stu-id="f5af8-455">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes from a third-party data source.</span></span> <span data-ttu-id="f5af8-456">Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de propriétés-valeur de message suivantes dans la zone de mot clé pour une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="f5af8-456">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>
    
  - <span data-ttu-id="f5af8-457">**`kind:externaldata`**: Utilisez cette paire de valeur de propriété pour rechercher tous les types de données tiers.</span><span class="sxs-lookup"><span data-stu-id="f5af8-457">**`kind:externaldata`**: Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="f5af8-458">Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contenant le mot « Contoso » dans la propriété Subject de l’élément importé, vous devez utiliser la requête par mot clé  `kind:externaldata AND subject:contoso` .</span><span class="sxs-lookup"><span data-stu-id="f5af8-458">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="f5af8-459">**`itemclass:ipm.externaldata.<third-party data type>`**: Utilisez cette paire de valeur de propriété pour rechercher uniquement un type précis de données tierces.</span><span class="sxs-lookup"><span data-stu-id="f5af8-459">**`itemclass:ipm.externaldata.<third-party data type>`**: Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="f5af8-460">Par exemple, pour rechercher uniquement les données Facebook qui contiennent le mot « Contoso » dans la propriété Subject, vous devez utiliser la requête par mot clé  `itemclass:ipm.externaldata.Facebook* AND subject:contoso` .</span><span class="sxs-lookup"><span data-stu-id="f5af8-460">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="f5af8-461">Pour obtenir la liste complète des valeurs à utiliser pour les types de données tiers pour la  `itemclass` propriété, voir [use content Search to Search tierce-Party Data imported to Microsoft 365](use-content-search-to-search-third-party-data-that-was-imported.md).</span><span class="sxs-lookup"><span data-stu-id="f5af8-461">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Microsoft 365](use-content-search-to-search-third-party-data-that-was-imported.md).</span></span>
    
   <span data-ttu-id="f5af8-462">Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :</span><span class="sxs-lookup"><span data-stu-id="f5af8-462">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="f5af8-463">Recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="f5af8-463">Content Search</span></span>](content-search.md)
    
  - [<span data-ttu-id="f5af8-464">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="f5af8-464">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
