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
ms.openlocfilehash: f76ceda12bf48d26454a47e4b0b5d6ad42fbe55d
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817039"
---
# <a name="work-with-a-partner-to-archive-third-party-data"></a><span data-ttu-id="c28a1-103">Collaborer avec un partenaire pour archiver des données tierces</span><span class="sxs-lookup"><span data-stu-id="c28a1-103">Work with a partner to archive third-party data</span></span>

<span data-ttu-id="c28a1-104">Vous pouvez collaborer avec un partenaire Microsoft pour importer et archiver des données à partir d’une source de données tierce vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-104">You can work with a Microsoft Partner to import and archive data from a third-party data source to Microsoft 365.</span></span> <span data-ttu-id="c28a1-105">Un partenaire peut vous fournir un connecteur personnalisé configuré pour extraire les éléments de la source de données tierce (de manière régulière), puis les importer.</span><span class="sxs-lookup"><span data-stu-id="c28a1-105">A partner can provide you with a custom connector that is configured to extract items from the third-party data source (on a regular basis) and then import those items.</span></span> <span data-ttu-id="c28a1-106">Le connecteur partenaire convertit le contenu d’un élément de la source de données en un format de message électronique, puis stocke les éléments dans des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c28a1-106">The partner connector converts the content of an item from the data source to an email message format and then stores the items in mailboxes.</span></span> <span data-ttu-id="c28a1-107">Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité de Microsoft 365 telles que la conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit et les stratégies de rétention de Microsoft 365 à ces données.</span><span class="sxs-lookup"><span data-stu-id="c28a1-107">After third-party data is imported, you can apply Microsoft 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Microsoft 365 retention policies to this data.</span></span>
  
<span data-ttu-id="c28a1-108">Voici une vue d’ensemble du processus et des étapes nécessaires à l’utilisation d’un partenaire Microsoft pour importer des données tierces.</span><span class="sxs-lookup"><span data-stu-id="c28a1-108">Here's an overview of the process and the steps necessary to work with a Microsoft Partner to import third-party data.</span></span>

[<span data-ttu-id="c28a1-109">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="c28a1-109">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="c28a1-110">Étape 2 : création et configuration d’une boîte aux lettres de données tierce</span><span class="sxs-lookup"><span data-stu-id="c28a1-110">Step 2: Create and configure a third-party data mailbox</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="c28a1-111">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="c28a1-111">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="c28a1-112">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="c28a1-112">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="c28a1-113">Étape 5 : enregistrer le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c28a1-113">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="c28a1-114">Fonctionnement du processus d’importation de données tierces</span><span class="sxs-lookup"><span data-stu-id="c28a1-114">How the third-party data import process works</span></span>

<span data-ttu-id="c28a1-115">L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tiers lors de l’utilisation d’un partenaire.</span><span class="sxs-lookup"><span data-stu-id="c28a1-115">The following illustration and description explain how the third-party data import process works when working with a partner.</span></span>
  
![Fonctionnement du processus d’importation de données tierces](../media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="c28a1-117">Le client travaille avec son partenaire de choix pour configurer un connecteur qui extrait des éléments de la source de données tierce, puis importer ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-117">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Microsoft 365.</span></span>
    
2. <span data-ttu-id="c28a1-118">Le connecteur partenaire se connecte à des sources de données tierces via une API tierce (sur la base planifiée ou configurée) et extrait des éléments de la source de données.</span><span class="sxs-lookup"><span data-stu-id="c28a1-118">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="c28a1-119">Le connecteur partenaire convertit le contenu d’un élément dans un format de message électronique.</span><span class="sxs-lookup"><span data-stu-id="c28a1-119">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="c28a1-120">Consultez la section [more information](#more-information) pour obtenir une description du schéma de format de message.</span><span class="sxs-lookup"><span data-stu-id="c28a1-120">See the [More information](#more-information) section for a description of the message-format schema.</span></span> 
    
3. <span data-ttu-id="c28a1-121">Le connecteur partenaire se connecte au service Azure dans Microsoft 365 à l’aide du service Web Exchange (EWS) via un point de terminaison connu.</span><span class="sxs-lookup"><span data-stu-id="c28a1-121">Partner connector connects to the Azure service in Microsoft 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="c28a1-122">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox.</span><span class="sxs-lookup"><span data-stu-id="c28a1-122">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox.</span></span> <span data-ttu-id="c28a1-123">Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span><span class="sxs-lookup"><span data-stu-id="c28a1-123">Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
   1. <span data-ttu-id="c28a1-124">**Éléments dont l’ID d’utilisateur correspond à un compte d’utilisateur :** Si le connecteur partenaire peut mapper l’ID utilisateur de l’élément dans la source de données tierce à un ID d’utilisateur spécifique dans Office 365, l’élément est copié dans le dossier **purges** du dossier éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c28a1-124">**Items that have a user ID that corresponds to an user account:** If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="c28a1-125">Les utilisateurs ne peuvent pas accéder aux éléments du dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="c28a1-125">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="c28a1-126">Toutefois, vous pouvez utiliser les outils de découverte électronique pour rechercher des éléments dans le dossier purges.</span><span class="sxs-lookup"><span data-stu-id="c28a1-126">However, you can use eDiscovery tools to search for items in the Purges folder.</span></span>
    
   1. <span data-ttu-id="c28a1-127">**Éléments qui n’ont pas d’identifiant utilisateur correspondant à un compte d’utilisateur :** Si le connecteur partenaire ne peut pas mapper l’ID utilisateur d’un élément sur un ID d’utilisateur spécifique, l’élément est copié dans le dossier **boîte de réception** de la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="c28a1-127">**Items that don't have a user ID that corresponds to an user account:** If the partner connector can't map the user ID of an item to a specific user ID, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="c28a1-128">L’importation d’éléments dans la boîte de réception permet à un membre de votre organisation ou à vous-même de vous connecter à la boîte aux lettres tierce pour visualiser et gérer ces éléments, et de voir si des ajustements doivent être effectués dans la configuration du connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="c28a1-128">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="c28a1-129">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="c28a1-129">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="c28a1-130">Un composant clé pour l’archivage de données tierces dans Microsoft 365 est de trouver et d’utiliser un partenaire Microsoft spécialisé dans la capture de données à partir d’une source de données tierce et l’importation dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-130">A key component for archiving third-party data in Microsoft 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365.</span></span> <span data-ttu-id="c28a1-131">Une fois les données importées, elles peuvent être archivées et conservées avec les autres données Microsoft de votre organisation, telles que les messages électroniques provenant d’Exchange et de documents provenant de SharePoint et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="c28a1-131">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="c28a1-132">Un partenaire crée un connecteur qui extrait les données des sources de données tierces de votre organisation (par exemple, BlackBerry, Facebook, Google +, Thomson Reuters, Twitter et YouTube) et transmet ces données à une API Office 365 qui importe des éléments dans les boîtes aux lettres Exchange sous forme de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="c28a1-132">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="c28a1-133">Les sections suivantes répertorient les partenaires Microsoft (et les sources de données tierces qu’ils prennent en charge) qui participent au programme d’archivage de données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-133">The following sections list the Microsoft partners (and the third-party data sources they support) that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="c28a1-134">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="c28a1-134">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="c28a1-135">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="c28a1-135">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="c28a1-136">Globanet</span><span class="sxs-lookup"><span data-stu-id="c28a1-136">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="c28a1-137">OpenText</span><span class="sxs-lookup"><span data-stu-id="c28a1-137">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="c28a1-138">Smarsh</span><span class="sxs-lookup"><span data-stu-id="c28a1-138">Smarsh</span></span>](#smarsh)

[<span data-ttu-id="c28a1-139">Verba</span><span class="sxs-lookup"><span data-stu-id="c28a1-139">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="c28a1-140">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="c28a1-140">17a-4 LLC</span></span>

<span data-ttu-id="c28a1-141">[17A-4 LLC](https://www.17a-4.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-141">[17a-4 LLC](https://www.17a-4.com) supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="c28a1-142">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="c28a1-142">BlackBerry</span></span>
    
- <span data-ttu-id="c28a1-143">Flux de données Bloomberg</span><span class="sxs-lookup"><span data-stu-id="c28a1-143">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="c28a1-144">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="c28a1-144">Cisco Jabber</span></span>
    
- <span data-ttu-id="c28a1-145">FactSet</span><span class="sxs-lookup"><span data-stu-id="c28a1-145">FactSet</span></span>
    
- <span data-ttu-id="c28a1-146">HipChat</span><span class="sxs-lookup"><span data-stu-id="c28a1-146">HipChat</span></span>
    
- <span data-ttu-id="c28a1-147">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="c28a1-147">InvestEdge</span></span>
    
- <span data-ttu-id="c28a1-148">LivePerson</span><span class="sxs-lookup"><span data-stu-id="c28a1-148">LivePerson</span></span>
    
- <span data-ttu-id="c28a1-149">Flux de données MessageLabs</span><span class="sxs-lookup"><span data-stu-id="c28a1-149">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="c28a1-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="c28a1-150">OpenText</span></span>
    
- <span data-ttu-id="c28a1-151">Aide en direct « cliquer pour appeler » Oracle/ATG</span><span class="sxs-lookup"><span data-stu-id="c28a1-151">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="c28a1-152">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="c28a1-152">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="c28a1-153">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="c28a1-153">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="c28a1-154">MindAlign</span><span class="sxs-lookup"><span data-stu-id="c28a1-154">MindAlign</span></span>
    
- <span data-ttu-id="c28a1-155">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="c28a1-155">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="c28a1-156">Skype Entreprise (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="c28a1-156">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="c28a1-157">Skype Entreprise Online (Lync Online)</span><span class="sxs-lookup"><span data-stu-id="c28a1-157">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="c28a1-158">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="c28a1-158">SQL Databases</span></span>
    
- <span data-ttu-id="c28a1-159">Squawker</span><span class="sxs-lookup"><span data-stu-id="c28a1-159">Squawker</span></span>
    
- <span data-ttu-id="c28a1-160">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="c28a1-160">Thomson Reuters Eikon Messenger</span></span>
  

  
### <a name="archivesocial"></a><span data-ttu-id="c28a1-161">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="c28a1-161">ArchiveSocial</span></span>

<span data-ttu-id="c28a1-162">[ArchiveSocial](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-162">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="c28a1-163">Facebook</span><span class="sxs-lookup"><span data-stu-id="c28a1-163">Facebook</span></span>
    
- <span data-ttu-id="c28a1-164">Flickr</span><span class="sxs-lookup"><span data-stu-id="c28a1-164">Flickr</span></span>
    
- <span data-ttu-id="c28a1-165">Instagram</span><span class="sxs-lookup"><span data-stu-id="c28a1-165">Instagram</span></span>
    
- <span data-ttu-id="c28a1-166">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="c28a1-166">LinkedIn</span></span>
    
- <span data-ttu-id="c28a1-167">Pinterest</span><span class="sxs-lookup"><span data-stu-id="c28a1-167">Pinterest</span></span>
    
- <span data-ttu-id="c28a1-168">Twitter</span><span class="sxs-lookup"><span data-stu-id="c28a1-168">Twitter</span></span>
    
- <span data-ttu-id="c28a1-169">YouTube</span><span class="sxs-lookup"><span data-stu-id="c28a1-169">YouTube</span></span>
    
- <span data-ttu-id="c28a1-170">Vimeo</span><span class="sxs-lookup"><span data-stu-id="c28a1-170">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="c28a1-171">Globanet</span><span class="sxs-lookup"><span data-stu-id="c28a1-171">Globanet</span></span>

<span data-ttu-id="c28a1-172">[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-172">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="c28a1-173">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="c28a1-173">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="c28a1-174">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-174">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-175">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-175">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-176">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-176">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-177">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-177">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-178">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="c28a1-178">Bloomberg Chat</span></span>
    
- <span data-ttu-id="c28a1-179">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="c28a1-179">Bloomberg Mail</span></span>
    
- <span data-ttu-id="c28a1-180">Box</span><span class="sxs-lookup"><span data-stu-id="c28a1-180">Box</span></span>
    
- <span data-ttu-id="c28a1-181">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="c28a1-181">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="c28a1-182">Serveur de présence de messagerie instantanée Cisco &amp; (version 10, v 10.5.1 Su1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="c28a1-182">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="c28a1-183">Teams de Cisco Webex</span><span class="sxs-lookup"><span data-stu-id="c28a1-183">Cisco Webex Teams</span></span>

- <span data-ttu-id="c28a1-184">ShareFile de l’espace de travail de Citrix &amp;</span><span class="sxs-lookup"><span data-stu-id="c28a1-184">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="c28a1-185">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="c28a1-185">CrowdCompass</span></span>

- <span data-ttu-id="c28a1-186">Fichiers texte personnalisés, délimités</span><span class="sxs-lookup"><span data-stu-id="c28a1-186">Custom-delimited text files</span></span>
    
- <span data-ttu-id="c28a1-187">Fichiers XML personnalisés</span><span class="sxs-lookup"><span data-stu-id="c28a1-187">Custom XML files</span></span>
    
- <span data-ttu-id="c28a1-188">Facebook (pages)</span><span class="sxs-lookup"><span data-stu-id="c28a1-188">Facebook (Pages)</span></span>
    
- <span data-ttu-id="c28a1-189">Factset</span><span class="sxs-lookup"><span data-stu-id="c28a1-189">Factset</span></span>
    
- <span data-ttu-id="c28a1-190">FXConnect</span><span class="sxs-lookup"><span data-stu-id="c28a1-190">FXConnect</span></span>
    
- <span data-ttu-id="c28a1-191">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="c28a1-191">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="c28a1-192">Jive</span><span class="sxs-lookup"><span data-stu-id="c28a1-192">Jive</span></span>
    
- <span data-ttu-id="c28a1-193">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="c28a1-193">Macgregor XIP</span></span>

- <span data-ttu-id="c28a1-194">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="c28a1-194">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="c28a1-195">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="c28a1-195">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="c28a1-196">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c28a1-196">Microsoft Teams</span></span>
       
- <span data-ttu-id="c28a1-197">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="c28a1-197">Microsoft Yammer</span></span>
    
- <span data-ttu-id="c28a1-198">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="c28a1-198">Mobile Guard</span></span>
    
- <span data-ttu-id="c28a1-199">Pivot</span><span class="sxs-lookup"><span data-stu-id="c28a1-199">Pivot</span></span>
    
- <span data-ttu-id="c28a1-200">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="c28a1-200">Salesforce Chatter</span></span>

- <span data-ttu-id="c28a1-201">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="c28a1-201">Skype for Business Online</span></span>
    
- <span data-ttu-id="c28a1-202">Skype Entreprise, versions 2007 R2-2016 (sur site)</span><span class="sxs-lookup"><span data-stu-id="c28a1-202">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="c28a1-203">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="c28a1-203">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="c28a1-204">Concert</span><span class="sxs-lookup"><span data-stu-id="c28a1-204">Symphony</span></span>
    
- <span data-ttu-id="c28a1-205">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="c28a1-205">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="c28a1-206">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="c28a1-206">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="c28a1-207">Thomson Reuters Dealings 3000/FX Trading</span><span class="sxs-lookup"><span data-stu-id="c28a1-207">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="c28a1-208">Twitter</span><span class="sxs-lookup"><span data-stu-id="c28a1-208">Twitter</span></span>
    
- <span data-ttu-id="c28a1-209">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="c28a1-209">UBS Chat</span></span>
    
- <span data-ttu-id="c28a1-210">YouTube</span><span class="sxs-lookup"><span data-stu-id="c28a1-210">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="c28a1-211">OpenText</span><span class="sxs-lookup"><span data-stu-id="c28a1-211">OpenText</span></span>

<span data-ttu-id="c28a1-212">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-212">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="c28a1-213">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="c28a1-213">Axs Encrypted</span></span>
    
- <span data-ttu-id="c28a1-214">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="c28a1-214">Axs Exchange</span></span>
    
- <span data-ttu-id="c28a1-215">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="c28a1-215">Axs Local Archive</span></span>
    
- <span data-ttu-id="c28a1-216">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="c28a1-216">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="c28a1-217">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="c28a1-217">Axs Signed</span></span>
    
- <span data-ttu-id="c28a1-218">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="c28a1-218">Bloomberg</span></span>
    
- <span data-ttu-id="c28a1-219">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="c28a1-219">Thomson Reuters</span></span>
  
### <a name="smarsh"></a><span data-ttu-id="c28a1-220">Smarsh</span><span class="sxs-lookup"><span data-stu-id="c28a1-220">Smarsh</span></span>

<span data-ttu-id="c28a1-221">[Smarsh](https://www.smarsh.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-221">[Smarsh](https://www.smarsh.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="c28a1-222">VISERA</span><span class="sxs-lookup"><span data-stu-id="c28a1-222">AIM</span></span>
    
- <span data-ttu-id="c28a1-223">American Idol</span><span class="sxs-lookup"><span data-stu-id="c28a1-223">American Idol</span></span>
    
- <span data-ttu-id="c28a1-224">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="c28a1-224">Apple Juice</span></span>
    
- <span data-ttu-id="c28a1-225">AOL avec client Pivot</span><span class="sxs-lookup"><span data-stu-id="c28a1-225">AOL with Pivot client</span></span>
    
- <span data-ttu-id="c28a1-226">Tréma</span><span class="sxs-lookup"><span data-stu-id="c28a1-226">Ares</span></span>
    
- <span data-ttu-id="c28a1-227">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-227">Bazaar Voice</span></span>
    
- <span data-ttu-id="c28a1-228">Bear Share</span><span class="sxs-lookup"><span data-stu-id="c28a1-228">Bear Share</span></span>
    
- <span data-ttu-id="c28a1-229">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="c28a1-229">Bit Torrent</span></span>
    
- <span data-ttu-id="c28a1-230">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-230">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-231">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-231">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-232">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-232">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-233">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="c28a1-233">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="c28a1-234">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="c28a1-234">Bloomberg Mail</span></span>
    
- <span data-ttu-id="c28a1-235">CellTrust</span><span class="sxs-lookup"><span data-stu-id="c28a1-235">CellTrust</span></span>
    
- <span data-ttu-id="c28a1-236">Chat Import</span><span class="sxs-lookup"><span data-stu-id="c28a1-236">Chat Import</span></span>
    
- <span data-ttu-id="c28a1-237">Chat Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="c28a1-237">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="c28a1-238">Brouillage</span><span class="sxs-lookup"><span data-stu-id="c28a1-238">Chatter</span></span>
    
- <span data-ttu-id="c28a1-239">&amp;Serveur de présence de messagerie instantanée Cisco (version 9.0.1, version 9.1, v 9.1.1 Su1, version 10, v 10.5.1 Su1)</span><span class="sxs-lookup"><span data-stu-id="c28a1-239">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="c28a1-240">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="c28a1-240">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="c28a1-241">Collaboration Import</span><span class="sxs-lookup"><span data-stu-id="c28a1-241">Collaboration Import</span></span>
    
- <span data-ttu-id="c28a1-242">Collaboration Real Time Logging</span><span class="sxs-lookup"><span data-stu-id="c28a1-242">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="c28a1-243">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="c28a1-243">Direct Connect</span></span>
    
- <span data-ttu-id="c28a1-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="c28a1-244">Facebook</span></span>
    
- <span data-ttu-id="c28a1-245">FactSet</span><span class="sxs-lookup"><span data-stu-id="c28a1-245">FactSet</span></span>
    
- <span data-ttu-id="c28a1-246">FastTrack</span><span class="sxs-lookup"><span data-stu-id="c28a1-246">FastTrack</span></span>
    
- <span data-ttu-id="c28a1-247">Gnutella</span><span class="sxs-lookup"><span data-stu-id="c28a1-247">Gnutella</span></span>
    
- <span data-ttu-id="c28a1-248">Google +</span><span class="sxs-lookup"><span data-stu-id="c28a1-248">Google+</span></span>
    
- <span data-ttu-id="c28a1-249">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="c28a1-249">GoToMyPC</span></span>
    
- <span data-ttu-id="c28a1-250">Hopster</span><span class="sxs-lookup"><span data-stu-id="c28a1-250">Hopster</span></span>
    
- <span data-ttu-id="c28a1-251">HubConnex</span><span class="sxs-lookup"><span data-stu-id="c28a1-251">HubConnex</span></span>
    
- <span data-ttu-id="c28a1-252">IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)</span><span class="sxs-lookup"><span data-stu-id="c28a1-252">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="c28a1-253">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="c28a1-253">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="c28a1-254">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="c28a1-254">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="c28a1-255">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="c28a1-255">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="c28a1-256">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="c28a1-256">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="c28a1-257">IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)</span><span class="sxs-lookup"><span data-stu-id="c28a1-257">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="c28a1-258">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="c28a1-258">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="c28a1-259">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="c28a1-259">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="c28a1-260">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="c28a1-260">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="c28a1-261">GLACE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="c28a1-261">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="c28a1-262">IM Import</span><span class="sxs-lookup"><span data-stu-id="c28a1-262">IM Import</span></span>
    
- <span data-ttu-id="c28a1-263">IM Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="c28a1-263">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="c28a1-264">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="c28a1-264">Indii Messenger</span></span>
    
- <span data-ttu-id="c28a1-265">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="c28a1-265">Instant Bloomberg</span></span>
    
- <span data-ttu-id="c28a1-266">SALLE</span><span class="sxs-lookup"><span data-stu-id="c28a1-266">IRC</span></span>
    
- <span data-ttu-id="c28a1-267">Jive</span><span class="sxs-lookup"><span data-stu-id="c28a1-267">Jive</span></span>
    
- <span data-ttu-id="c28a1-268">Jive 6 Real Time Logging (version 6, version 7)</span><span class="sxs-lookup"><span data-stu-id="c28a1-268">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="c28a1-269">Jive Import</span><span class="sxs-lookup"><span data-stu-id="c28a1-269">Jive Import</span></span>
    
- <span data-ttu-id="c28a1-270">JXTA</span><span class="sxs-lookup"><span data-stu-id="c28a1-270">JXTA</span></span>
    
- <span data-ttu-id="c28a1-271">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="c28a1-271">LinkedIn</span></span>
    
- <span data-ttu-id="c28a1-272">Microsoft Lync (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="c28a1-272">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="c28a1-273">MFTP</span><span class="sxs-lookup"><span data-stu-id="c28a1-273">MFTP</span></span>
    
- <span data-ttu-id="c28a1-274">Microsoft Lync 2013 Voix</span><span class="sxs-lookup"><span data-stu-id="c28a1-274">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="c28a1-275">Microsoft SharePoint (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="c28a1-275">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="c28a1-276">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c28a1-276">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="c28a1-277">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="c28a1-277">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="c28a1-278">MindAlign</span><span class="sxs-lookup"><span data-stu-id="c28a1-278">MindAlign</span></span>
    
- <span data-ttu-id="c28a1-279">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="c28a1-279">Mobile Guard</span></span>
    
- <span data-ttu-id="c28a1-280">SYMPATICO</span><span class="sxs-lookup"><span data-stu-id="c28a1-280">MSN</span></span>
    
- <span data-ttu-id="c28a1-281">My Space</span><span class="sxs-lookup"><span data-stu-id="c28a1-281">My Space</span></span>
    
- <span data-ttu-id="c28a1-282">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="c28a1-282">NEONetwork</span></span>
    
- <span data-ttu-id="c28a1-283">Office 365 Lync dédié</span><span class="sxs-lookup"><span data-stu-id="c28a1-283">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="c28a1-284">MI partagée Office 365</span><span class="sxs-lookup"><span data-stu-id="c28a1-284">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="c28a1-285">Pinterest</span><span class="sxs-lookup"><span data-stu-id="c28a1-285">Pinterest</span></span>
    
- <span data-ttu-id="c28a1-286">Pivot</span><span class="sxs-lookup"><span data-stu-id="c28a1-286">Pivot</span></span>
    
- <span data-ttu-id="c28a1-287">QQ</span><span class="sxs-lookup"><span data-stu-id="c28a1-287">QQ</span></span>
    
- <span data-ttu-id="c28a1-288">Skype Entreprise 2015</span><span class="sxs-lookup"><span data-stu-id="c28a1-288">Skype for Business 2015</span></span>
    
- <span data-ttu-id="c28a1-289">SoftEther</span><span class="sxs-lookup"><span data-stu-id="c28a1-289">SoftEther</span></span>
    
- <span data-ttu-id="c28a1-290">Concert</span><span class="sxs-lookup"><span data-stu-id="c28a1-290">Symphony</span></span>
    
- <span data-ttu-id="c28a1-291">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="c28a1-291">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="c28a1-292">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="c28a1-292">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="c28a1-293">Termes</span><span class="sxs-lookup"><span data-stu-id="c28a1-293">Tor</span></span>
    
- <span data-ttu-id="c28a1-294">TTT</span><span class="sxs-lookup"><span data-stu-id="c28a1-294">TTT</span></span>
    
- <span data-ttu-id="c28a1-295">Twitter</span><span class="sxs-lookup"><span data-stu-id="c28a1-295">Twitter</span></span>
    
- <span data-ttu-id="c28a1-296">WinMX</span><span class="sxs-lookup"><span data-stu-id="c28a1-296">WinMX</span></span>
    
- <span data-ttu-id="c28a1-297">Winny</span><span class="sxs-lookup"><span data-stu-id="c28a1-297">Winny</span></span>
    
- <span data-ttu-id="c28a1-298">Yahoo</span><span class="sxs-lookup"><span data-stu-id="c28a1-298">Yahoo</span></span>
    
- <span data-ttu-id="c28a1-299">Yammer</span><span class="sxs-lookup"><span data-stu-id="c28a1-299">Yammer</span></span>
    
- <span data-ttu-id="c28a1-300">YouTube</span><span class="sxs-lookup"><span data-stu-id="c28a1-300">YouTube</span></span>
    

### <a name="verba"></a><span data-ttu-id="c28a1-301">Verba</span><span class="sxs-lookup"><span data-stu-id="c28a1-301">Verba</span></span>

<span data-ttu-id="c28a1-302">[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-302">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="c28a1-303">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="c28a1-303">Avaya Aura Video</span></span>
    
- <span data-ttu-id="c28a1-304">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-304">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="c28a1-305">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="c28a1-305">Avtec Radio</span></span>
    
- <span data-ttu-id="c28a1-306">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="c28a1-306">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="c28a1-307">BroadSoft Video</span><span class="sxs-lookup"><span data-stu-id="c28a1-307">BroadSoft Video</span></span>
    
- <span data-ttu-id="c28a1-308">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-308">BroadSoft Voice</span></span>
    
- <span data-ttu-id="c28a1-309">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-309">Centile Voice</span></span>
    
- <span data-ttu-id="c28a1-310">Cisco Jabber IM</span><span class="sxs-lookup"><span data-stu-id="c28a1-310">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="c28a1-311">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="c28a1-311">Cisco UC Video</span></span>
    
- <span data-ttu-id="c28a1-312">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-312">Cisco UC Voice</span></span>
    
- <span data-ttu-id="c28a1-313">Cisco UCCX/UCCE vidéo</span><span class="sxs-lookup"><span data-stu-id="c28a1-313">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="c28a1-314">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-314">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="c28a1-315">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="c28a1-315">ESChat Radio</span></span>
    
- <span data-ttu-id="c28a1-316">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="c28a1-316">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="c28a1-317">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-317">IP Trade Voice</span></span>
    
- <span data-ttu-id="c28a1-318">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="c28a1-318">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="c28a1-319">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="c28a1-319">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="c28a1-320">Mitel MiContact Center for Lync (prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="c28a1-320">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="c28a1-321">Oracle / Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="c28a1-321">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="c28a1-322">Oracle / Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-322">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="c28a1-323">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-323">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="c28a1-324">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="c28a1-324">SIPREC Video</span></span>
    
-  <span data-ttu-id="c28a1-325">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-325">SIPREC Voice</span></span> 
    
- <span data-ttu-id="c28a1-326">Skype Entreprise / MI Lync</span><span class="sxs-lookup"><span data-stu-id="c28a1-326">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="c28a1-327">Skype Entreprise / Vidéo Lync</span><span class="sxs-lookup"><span data-stu-id="c28a1-327">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="c28a1-328">Skype Entreprise / Voix Lync</span><span class="sxs-lookup"><span data-stu-id="c28a1-328">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="c28a1-329">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-329">Speakerbus Voice</span></span>
    
- <span data-ttu-id="c28a1-330">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="c28a1-330">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="c28a1-331">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-331">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="c28a1-332">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="c28a1-332">Truphone Voice</span></span>
    
- <span data-ttu-id="c28a1-333">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="c28a1-333">TwistedPair Radio</span></span>
    
- <span data-ttu-id="c28a1-334">Écran d’ordinateur de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="c28a1-334">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="c28a1-335">Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="c28a1-335">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="c28a1-336">Voici les étapes à suivre pour créer et configurer une boîte aux lettres de données tierce pour l’importation de données dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-336">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365.</span></span> <span data-ttu-id="c28a1-337">Comme indiqué précédemment, les éléments sont importés dans cette boîte aux lettres si le connecteur partenaire ne peut pas mapper l’ID utilisateur de l’élément sur un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c28a1-337">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an user account.</span></span>
  
 <span data-ttu-id="c28a1-338">**Effectuez ces tâches dans le centre d’administration Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="c28a1-338">**Complete these tasks in the Microsoft 365 admin center**</span></span>
  
1. <span data-ttu-id="c28a1-339">Créez un compte d’utilisateur et attribuez-lui une licence Exchange Online plan 2 ; Voir [Ajouter des utilisateurs à Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span><span class="sxs-lookup"><span data-stu-id="c28a1-339">Create a user account and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span></span> <span data-ttu-id="c28a1-340">Une licence plan 2 est nécessaire pour placer la boîte aux lettres en conservation pour litige ou pour activer une boîte aux lettres d’archivage dont le quota de stockage est illimité.</span><span class="sxs-lookup"><span data-stu-id="c28a1-340">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="c28a1-341">Ajoutez le compte d’utilisateur pour la boîte aux lettres de données tierce au rôle d’administrateur d' **administrateur Exchange** dans Office 365 ; consultez la rubrique [assigner des rôles d’administrateur dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="c28a1-341">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="c28a1-342">Notez les informations d’identification pour ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c28a1-342">Write down the credentials for this user account.</span></span> <span data-ttu-id="c28a1-343">Vous devez les fournir à votre partenaire, comme décrit à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="c28a1-343">You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="c28a1-344">**Effectuer ces tâches dans le centre d’administration Exchange**</span><span class="sxs-lookup"><span data-stu-id="c28a1-344">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="c28a1-345">Masquer la boîte aux lettres de données tierce dans le carnet d’adresses et les autres listes d’adresses de votre organisation ; consultez la rubrique [Manage User mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span><span class="sxs-lookup"><span data-stu-id="c28a1-345">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span></span> <span data-ttu-id="c28a1-346">Vous pouvez également exécuter la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="c28a1-346">Alternatively, you can run the following PowerShell command:</span></span>
    
    ```powershell
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="c28a1-347">Attribuer l’autorisation **FullAccess** à la boîte aux lettres de données tierce afin que les administrateurs ou les responsables de la mise en conformité puissent ouvrir la boîte aux lettres de données tierce dans le client de bureau Outlook ; consultez la rubrique [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="c28a1-347">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="c28a1-348">Activez les fonctionnalités liées à la conformité suivantes pour la boîte aux lettres de données tierce :</span><span class="sxs-lookup"><span data-stu-id="c28a1-348">Enable the following compliance-related features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="c28a1-349">Activer la boîte aux lettres d’archivage ; consultez la rubrique [activation des boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [activez un archivage illimité](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="c28a1-349">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="c28a1-350">Cela vous permet de libérer de l’espace de stockage dans la boîte aux lettres principale en configurant une stratégie d’archivage qui déplace les éléments de données tiers vers la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="c28a1-350">This lets you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="c28a1-351">Vous disposez ainsi d’un espace de stockage illimité pour les données tierces.</span><span class="sxs-lookup"><span data-stu-id="c28a1-351">This provides you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="c28a1-352">Placez la boîte aux lettres de données tierces en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="c28a1-352">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="c28a1-353">Vous pouvez également appliquer une stratégie de rétention Microsoft 365 dans le centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="c28a1-353">You can also apply a Microsoft 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="c28a1-354">Le fait de placer cette boîte aux lettres en conservation conserve des éléments de données tiers (indéfiniment ou pour une durée spécifiée) et les empêche d’être purgés de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c28a1-354">Placing this mailbox on hold retains third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="c28a1-355">Consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-355">See one of the following topics:</span></span>
    
      - [<span data-ttu-id="c28a1-356">Placer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="c28a1-356">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="c28a1-357">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="c28a1-357">Overview of retention policies</span></span>](retention-policies.md)
    
    - <span data-ttu-id="c28a1-358">Activez l’enregistrement d’audit des boîtes aux lettres pour l’accès des propriétaires, des délégués et des administrateurs à la boîte aux lettres de données tierce. Voir [activer l’audit de boîte aux lettres](enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="c28a1-358">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="c28a1-359">Cela vous permet d’auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="c28a1-359">This allows you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="c28a1-360">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="c28a1-360">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="c28a1-361">L’étape suivante consiste à configurer les boîtes aux lettres des utilisateurs pour prendre en charge les données tierces.</span><span class="sxs-lookup"><span data-stu-id="c28a1-361">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="c28a1-362">Effectuez ces tâches à l’aide du centre d’administration Exchange ou à l’aide des applets de commande Windows PowerShell correspondantes.</span><span class="sxs-lookup"><span data-stu-id="c28a1-362">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="c28a1-363">Activez la boîte aux lettres d’archivage pour chaque utilisateur ; consultez la rubrique [activation des boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [activez un archivage illimité](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="c28a1-363">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="c28a1-364">Placer les boîtes aux lettres utilisateur en conservation pour litige ou appliquer une stratégie de rétention Microsoft 365 ; consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-364">Place user mailboxes on Litigation Hold or apply a Microsoft 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="c28a1-365">Placer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="c28a1-365">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="c28a1-366">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="c28a1-366">Overview of retention policies</span></span>](retention-policies.md)
    
    <span data-ttu-id="c28a1-367">Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="c28a1-367">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="c28a1-368">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="c28a1-368">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="c28a1-369">La dernière étape consiste à fournir à votre partenaire les informations suivantes afin qu’il puisse configurer le connecteur de sorte qu’il se connecte à votre organisation pour importer les données dans les boîtes aux lettres utilisateur et dans la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="c28a1-369">The final step is to provide your partner with the following information so they can configure the connector to connect to your organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="c28a1-370">Le point de terminaison utilisé pour se connecter au service Azure dans Office 365 :</span><span class="sxs-lookup"><span data-stu-id="c28a1-370">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```http
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="c28a1-371">Les informations d’identification de connexion (ID d’utilisateur et mot de passe Microsoft 365) de la boîte aux lettres de données tierce que vous avez créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c28a1-371">The sign-in credentials (Microsoft 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="c28a1-372">Ces informations d’identification sont requises pour que le connecteur partenaire puisse accéder aux éléments et les importer dans les boîtes aux lettres utilisateur et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="c28a1-372">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="c28a1-373">Étape 5 : enregistrer le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c28a1-373">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="c28a1-374">À partir du 30 septembre 2018, le service Azure dans Office 365 commencera à utiliser l’authentification moderne dans Exchange Online pour authentifier les connecteurs de données tiers qui tentent de se connecter à votre organisation pour importer des données.</span><span class="sxs-lookup"><span data-stu-id="c28a1-374">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your organization to import data.</span></span> <span data-ttu-id="c28a1-375">La raison de cette modification est que l’authentification moderne fournit davantage de sécurité que la méthode actuelle, basée sur une liste verte pour les connecteurs tiers qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.</span><span class="sxs-lookup"><span data-stu-id="c28a1-375">The reason for this change is that modern authentication provides more security than the current method, which was based on an allow list for third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="c28a1-376">Pour permettre à un connecteur de données tiers de se connecter à Office 365 à l’aide de la nouvelle méthode d’authentification moderne, un administrateur de votre organisation doit consentir à inscrire le connecteur en tant qu’application de service approuvée dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c28a1-376">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="c28a1-377">Pour ce faire, vous devez accepter une demande d’autorisation pour permettre au connecteur d’accéder aux données de votre organisation dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c28a1-377">This is done by accepting a permission request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="c28a1-378">Une fois que vous avez accepté cette demande, le connecteur de données tiers est ajouté en tant qu’application d’entreprise à Azure Active Directory et représenté en tant que principal de service.</span><span class="sxs-lookup"><span data-stu-id="c28a1-378">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="c28a1-379">Pour plus d’informations sur le processus de consentement, consultez la rubrique consentement de l' [administrateur client](https://docs.microsoft.com/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="c28a1-379">For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="c28a1-380">Voici les étapes à suivre pour accéder à la demande et l’accepter pour enregistrer le connecteur :</span><span class="sxs-lookup"><span data-stu-id="c28a1-380">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="c28a1-381">Accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et connectez-vous à l’aide des informations d’identification d’un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="c28a1-381">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of a global administrator.</span></span>

   <span data-ttu-id="c28a1-382">La boîte de dialogue suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c28a1-382">The following dialog box is displayed.</span></span> <span data-ttu-id="c28a1-383">Vous pouvez développer les signes pour vérifier les autorisations qui seront affectées au connecteur.</span><span class="sxs-lookup"><span data-stu-id="c28a1-383">You can expand the carets to review the permissions that will be assigned to the connector.</span></span>

   ![La boîte de dialogue demande d’autorisations s’affiche.](../media/O365-ThirdPartyDataConnector-OptIn1.png)

2. <span data-ttu-id="c28a1-385">Cliquez sur **Accept (Accepter)**.</span><span class="sxs-lookup"><span data-stu-id="c28a1-385">Click **Accept**.</span></span>

<span data-ttu-id="c28a1-386">Une fois que vous avez accepté la demande, le [portail Azure](https://portal.azure.com) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c28a1-386">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="c28a1-387">Pour afficher la liste des applications pour votre organisation, cliquez sur applications d’entreprise **Azure Active Directory**  >  **Enterprise applications**.</span><span class="sxs-lookup"><span data-stu-id="c28a1-387">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="c28a1-388">Le connecteur de données tiers 365 Office est affiché dans le panneau **applications d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="c28a1-388">The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c28a1-389">Après le 30 septembre 2018, les données tierces ne seront plus importées dans les boîtes aux lettres de votre organisation si vous n’enregistrez pas un connecteur de données tiers dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c28a1-389">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="c28a1-390">Remarque les connecteurs de données tiers existants (ceux créés avant le 30 septembre 2018) doivent également être enregistrés dans Azure Active Directory en suivant la procédure de l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="c28a1-390">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="c28a1-391">Révocation du consentement pour un connecteur de données tiers</span><span class="sxs-lookup"><span data-stu-id="c28a1-391">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="c28a1-392">Une fois que votre organisation a accepté la demande d’autorisations pour enregistrer un connecteur de données tiers dans Azure Active Directory, votre organisation peut révoquer ce consentement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c28a1-392">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="c28a1-393">Toutefois, la révocation de l’autorisation pour un connecteur signifie que les données de la source de données tierce ne seront plus importées dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-393">However, revoking the consent for a connector means that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="c28a1-394">Pour révoquer le consentement d’un connecteur de données tiers, vous pouvez supprimer l’application (en supprimant l’entité de service correspondante) à partir d’Azure Active Directory à l’aide du panneau **applications d’entreprise** dans le portail Azure ou en utilisant la commande [Remove-MsolServicePrincipal](https://docs.microsoft.com/powershell/module/msonline/remove-msolserviceprincipal) dans Office 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c28a1-394">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell.</span></span> <span data-ttu-id="c28a1-395">Vous pouvez également utiliser l’applet de commande [Remove-AzureADServicePrincipal](https://docs.microsoft.com/powershell/module/azuread/remove-azureadserviceprincipal) dans Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c28a1-395">You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="c28a1-396">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="c28a1-396">More information</span></span>

- <span data-ttu-id="c28a1-397">Comme indiqué précédemment, les éléments des sources de données tierces sont importés vers les boîtes aux lettres Exchange en tant que messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="c28a1-397">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="c28a1-398">Le connecteur partenaire importe l’élément à l’aide d’un schéma requis par l’API Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-398">The partner connector imports the item using a schema required by the Office 365 API.</span></span> <span data-ttu-id="c28a1-399">Le tableau suivant décrit les propriétés de message d’un élément d’une source de données tierces après son importation vers une boîte aux lettres Exchange en tant que message électronique.</span><span class="sxs-lookup"><span data-stu-id="c28a1-399">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="c28a1-400">Le tableau indique également si la propriété de message est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c28a1-400">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="c28a1-401">Les propriétés obligatoires doivent être renseignées.</span><span class="sxs-lookup"><span data-stu-id="c28a1-401">Mandatory properties must be populated.</span></span> <span data-ttu-id="c28a1-402">Si une propriété obligatoire est manquante dans un élément, celui-ci ne sera pas importé dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-402">If an item is missing a mandatory property, it won't be imported to Office 365.</span></span> <span data-ttu-id="c28a1-403">Le processus d’importation renvoie un message d’erreur expliquant pourquoi un élément n’a pas été importé et quelle est la propriété manquante.</span><span class="sxs-lookup"><span data-stu-id="c28a1-403">The import process returns an error message explaining why an item wasn't imported and which property is missing.</span></span><br/><br/>
    
    |<span data-ttu-id="c28a1-404">**Propriété de message**</span><span class="sxs-lookup"><span data-stu-id="c28a1-404">**Message property**</span></span>|<span data-ttu-id="c28a1-405">**Obligatoire ?**</span><span class="sxs-lookup"><span data-stu-id="c28a1-405">**Mandatory?**</span></span>|<span data-ttu-id="c28a1-406">**Description**</span><span class="sxs-lookup"><span data-stu-id="c28a1-406">**Description**</span></span>|<span data-ttu-id="c28a1-407">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="c28a1-407">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="c28a1-408">**FROM**</span><span class="sxs-lookup"><span data-stu-id="c28a1-408">**FROM**</span></span> <br/> |<span data-ttu-id="c28a1-409">Oui</span><span class="sxs-lookup"><span data-stu-id="c28a1-409">Yes</span></span>  <br/> |<span data-ttu-id="c28a1-410">Utilisateur qui a initialement créé ou envoyé l’élément dans la source de données tierces.</span><span class="sxs-lookup"><span data-stu-id="c28a1-410">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="c28a1-411">Le connecteur partenaire tente de mapper l’ID utilisateur à partir de l’élément source (par exemple, un handle Twitter) sur un compte d’utilisateur pour tous les participants (les utilisateurs figurant dans les champs de et à).</span><span class="sxs-lookup"><span data-stu-id="c28a1-411">The partner connector attempts to map the user ID from the source item (for example a Twitter handle) to an user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="c28a1-412">Une copie du message sera importée dans la boîte aux lettres de chaque participant.</span><span class="sxs-lookup"><span data-stu-id="c28a1-412">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="c28a1-413">Si aucun des participants de l’élément ne peut être mappé à un compte d’utilisateur, l’élément sera importé dans la boîte aux lettres d’archivage tierce dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c28a1-413">If none of the participants from the item can be mapped to an user account, the item will be imported to the third-party archiving mailbox in Office 365.</span></span>  <br/> <br/> <span data-ttu-id="c28a1-414">Le participant identifié comme l’expéditeur de l’élément doit disposer d’une boîte aux lettres active dans l’organisation dans laquelle l’élément est importé.</span><span class="sxs-lookup"><span data-stu-id="c28a1-414">The participant who's identified as the sender of the item must have an active mailbox in the organization that the item is being imported to.</span></span> <span data-ttu-id="c28a1-415">Si l’expéditeur ne dispose pas d’une boîte aux lettres active, l’erreur suivante est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="c28a1-415">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="c28a1-416">**TO**</span><span class="sxs-lookup"><span data-stu-id="c28a1-416">**TO**</span></span> <br/> |<span data-ttu-id="c28a1-417">Oui</span><span class="sxs-lookup"><span data-stu-id="c28a1-417">Yes</span></span>  <br/> |<span data-ttu-id="c28a1-418">Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="c28a1-418">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="c28a1-419">**Objet**</span><span class="sxs-lookup"><span data-stu-id="c28a1-419">**SUBJECT**</span></span> <br/> |<span data-ttu-id="c28a1-420">Non</span><span class="sxs-lookup"><span data-stu-id="c28a1-420">No</span></span>  <br/> |<span data-ttu-id="c28a1-421">Objet de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="c28a1-421">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="c28a1-422">**JOURS**</span><span class="sxs-lookup"><span data-stu-id="c28a1-422">**DATE**</span></span> <br/> |<span data-ttu-id="c28a1-423">Oui</span><span class="sxs-lookup"><span data-stu-id="c28a1-423">Yes</span></span>  <br/> |<span data-ttu-id="c28a1-424">Date à laquelle l’élément a été initialement créé ou publié dans la source de données client.</span><span class="sxs-lookup"><span data-stu-id="c28a1-424">The date the item was originally created or posted in the customer data source.</span></span> <span data-ttu-id="c28a1-425">Par exemple, la date à laquelle un message Twitter a été tweeté.</span><span class="sxs-lookup"><span data-stu-id="c28a1-425">For example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="c28a1-426">**ENTITÉ**</span><span class="sxs-lookup"><span data-stu-id="c28a1-426">**BODY**</span></span> <br/> |<span data-ttu-id="c28a1-427">Non</span><span class="sxs-lookup"><span data-stu-id="c28a1-427">No</span></span>  <br/> |<span data-ttu-id="c28a1-428">Contenu du message ou de la publication.</span><span class="sxs-lookup"><span data-stu-id="c28a1-428">The contents of the message or post.</span></span> <span data-ttu-id="c28a1-429">Pour certaines sources de données, le contenu de cette propriété peut être identique au contenu de la propriété **SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="c28a1-429">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="c28a1-430">Pendant le processus d’importation, le connecteur partenaire tente de maintenir la fidélité complète de la source de contenu.</span><span class="sxs-lookup"><span data-stu-id="c28a1-430">During the import process, the partner connector attempts to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="c28a1-431">Si possible, les fichiers, les graphiques ou tout autre contenu du corps de l’élément source sont inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c28a1-431">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="c28a1-432">Sinon, le contenu de l’élément source est inclus dans la propriété **ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="c28a1-432">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="c28a1-433">Le contenu de cette propriété dépend du connecteur du partenaire et de la capacité de la plateforme source.</span><span class="sxs-lookup"><span data-stu-id="c28a1-433">The contents of this property depends on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="c28a1-434">**CONNEXION**</span><span class="sxs-lookup"><span data-stu-id="c28a1-434">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="c28a1-435">Non</span><span class="sxs-lookup"><span data-stu-id="c28a1-435">No</span></span>  <br/> |<span data-ttu-id="c28a1-436">Si un élément de la source de données (par exemple, un tweet dans Twitter ou une conversation de messagerie instantanée) a un fichier joint ou inclut des images, le partenaire Connect tente d’abord d’inclure les pièces jointes dans la propriété **Body** .</span><span class="sxs-lookup"><span data-stu-id="c28a1-436">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="c28a1-437">Si cela n’est pas possible, il est ajouté à la propriété \* \* ATTACHment \* \*.</span><span class="sxs-lookup"><span data-stu-id="c28a1-437">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="c28a1-438">Voici d’autres exemples de pièces jointes : mentions J’aime sur Facebook, métadonnées de la source de contenu et réponses à un message ou une publication.</span><span class="sxs-lookup"><span data-stu-id="c28a1-438">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |<span data-ttu-id="c28a1-439">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="c28a1-439">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="c28a1-440">Oui</span><span class="sxs-lookup"><span data-stu-id="c28a1-440">Yes</span></span>  <br/> | <span data-ttu-id="c28a1-441">Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par le connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="c28a1-441">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="c28a1-442">Le format de cette propriété est `IPM.NOTE.Source.Event` .</span><span class="sxs-lookup"><span data-stu-id="c28a1-442">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="c28a1-443">(Cette propriété doit commencer par `IPM.NOTE` .</span><span class="sxs-lookup"><span data-stu-id="c28a1-443">(This property must begin with  `IPM.NOTE`.</span></span> <span data-ttu-id="c28a1-444">Ce format est similaire à celui de la `IPM.NOTE.X` classe message.) Cette propriété inclut les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c28a1-444">This format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/><span data-ttu-id="c28a1-445">`Source`: Indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="c28a1-445">`Source`: Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="c28a1-446">`Event`: Indique le type d’activité qui a été effectué dans la source de données tierce qui a produit les éléments ; par exemple, un tweet dans Twitter ou un billet dans Facebook.</span><span class="sxs-lookup"><span data-stu-id="c28a1-446">`Event`: Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="c28a1-447">Les événements sont propres à la source de données.</span><span class="sxs-lookup"><span data-stu-id="c28a1-447">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="c28a1-448">L’un des objectifs de cette propriété est de filtrer des éléments spécifiques en fonction de la source de données d’origine d’un élément ou en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="c28a1-448">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="c28a1-449">Par exemple, lors d’une recherche de découverte électronique, vous pouvez créer une requête de recherche afin de trouver tous les tweets qui ont été publiés par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="c28a1-449">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="c28a1-450">Lorsque des éléments sont correctement importés dans des boîtes aux lettres dans Office 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="c28a1-450">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="c28a1-451">Cet identificateur, appelé `x-IngestionCorrelationID` , peut être utilisé à des fins de dépannage ultérieure par les partenaires pour le suivi de bout en bout des éléments.</span><span class="sxs-lookup"><span data-stu-id="c28a1-451">This identifier, called  `x-IngestionCorrelationID`, can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="c28a1-452">Nous recommandons que vos partenaires récupèrent ces informations et les conservent de leur côté.</span><span class="sxs-lookup"><span data-stu-id="c28a1-452">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="c28a1-453">Voici un exemple d’une réponse HTTP avec cet identifiant :</span><span class="sxs-lookup"><span data-stu-id="c28a1-453">Here's an example of an HTTP response showing this identifier:</span></span>

    ```http
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```

- <span data-ttu-id="c28a1-454">Vous pouvez utiliser l’outil de recherche de contenu dans le centre de sécurité et de conformité pour rechercher des éléments qui ont été importés dans des boîtes aux lettres à partir d’une source de données tierce.</span><span class="sxs-lookup"><span data-stu-id="c28a1-454">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes from a third-party data source.</span></span> <span data-ttu-id="c28a1-455">Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de propriétés-valeur de message suivantes dans la zone de mot clé pour une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="c28a1-455">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>
    
  - <span data-ttu-id="c28a1-456">**`kind:externaldata`**: Utilisez cette paire de valeur de propriété pour rechercher tous les types de données tiers.</span><span class="sxs-lookup"><span data-stu-id="c28a1-456">**`kind:externaldata`**: Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="c28a1-457">Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contenant le mot « Contoso » dans la propriété Subject de l’élément importé, vous devez utiliser la requête par mot clé `kind:externaldata AND subject:contoso` .</span><span class="sxs-lookup"><span data-stu-id="c28a1-457">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="c28a1-458">**`itemclass:ipm.externaldata.<third-party data type>`**: Utilisez cette paire de valeur de propriété pour rechercher uniquement un type précis de données tierces.</span><span class="sxs-lookup"><span data-stu-id="c28a1-458">**`itemclass:ipm.externaldata.<third-party data type>`**: Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="c28a1-459">Par exemple, pour rechercher uniquement les données Facebook qui contiennent le mot « Contoso » dans la propriété Subject, vous devez utiliser la requête par mot clé `itemclass:ipm.externaldata.Facebook* AND subject:contoso` .</span><span class="sxs-lookup"><span data-stu-id="c28a1-459">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="c28a1-460">Pour obtenir la liste complète des valeurs à utiliser pour les types de données tiers pour la `itemclass` propriété, voir [use content Search to Search tierce-Party Data imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md).</span><span class="sxs-lookup"><span data-stu-id="c28a1-460">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md).</span></span>
    
   <span data-ttu-id="c28a1-461">Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :</span><span class="sxs-lookup"><span data-stu-id="c28a1-461">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="c28a1-462">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="c28a1-462">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="c28a1-463">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="c28a1-463">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
