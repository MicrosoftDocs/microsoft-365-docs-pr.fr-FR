---
title: Collaborer avec un partenaire pour archiver des données tierces dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Votre organisation peut collaborer avec un partenaire Microsoft pour configurer un connecteur personnalisé permettant d’importer des données tierces à partir de sources de données telles que Salesforce chatter, Yahoo Messenger ou Yammer. Cela vous permet d’archiver des données à partir de sources de données tierces dans Office 365 de sorte que vous puissiez utiliser les fonctionnalités de conformité d’Office 365 telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données tierces de votre organisation.
ms.openlocfilehash: 9a1767baadb237196161032166f78c06dc7e099b
ms.sourcegitcommit: 1d376287f6c1bf5174873e89ed4bf7bb15bc13f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38685986"
---
# <a name="work-with-a-partner-to-archive-third-party-data-in-office-365"></a><span data-ttu-id="5325c-104">Collaborer avec un partenaire pour archiver des données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5325c-104">Work with a partner to archive third-party data in Office 365</span></span>

<span data-ttu-id="5325c-105">Vous pouvez collaborer avec un partenaire Microsoft pour importer et archiver des données à partir d’une source de données tierce vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-105">You can work with a Microsoft Partner to import and archive data from a third-party data source to Office 365.</span></span> <span data-ttu-id="5325c-106">Un partenaire peut vous fournir un connecteur personnalisé configuré pour extraire les éléments de la source de données tierce (de manière régulière), puis les importer dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-106">A partner can provide you with a custom connector that is configured to extract items from the third-party data source (on a regular basis) and then import those items to Office 365.</span></span> <span data-ttu-id="5325c-107">Le connecteur partenaire convertit le contenu d’un élément de la source de données en un format de message électronique, puis stocke les éléments dans les boîtes aux lettres dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-107">The partner connector converts the content of an item from the data source to an email message format and then stores the items in mailboxes in Office 365.</span></span> <span data-ttu-id="5325c-108">Une fois les données tierces importées, vous pouvez appliquer des fonctionnalités de conformité Office 365 telles que la conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit et les stratégies de rétention d’Office 365 à ces données.</span><span class="sxs-lookup"><span data-stu-id="5325c-108">After third-party data is imported, you can apply Office 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies to this data.</span></span>
  
<span data-ttu-id="5325c-109">Voici une vue d’ensemble du processus et des étapes nécessaires à l’utilisation d’un partenaire Microsoft pour importer des données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-109">Here's an overview of the process and the steps necessary to work with a Microsoft Partner to import third-party data to Office 365.</span></span>

[<span data-ttu-id="5325c-110">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="5325c-110">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="5325c-111">Step 2: Create and configure a third-party data mailbox in Office 365</span><span class="sxs-lookup"><span data-stu-id="5325c-111">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="5325c-112">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="5325c-112">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="5325c-113">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="5325c-113">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="5325c-114">Étape 5 : enregistrer le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5325c-114">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="5325c-115">Fonctionnement du processus d’importation de données tierces</span><span class="sxs-lookup"><span data-stu-id="5325c-115">How the third-party data import process works</span></span>

<span data-ttu-id="5325c-116">L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tiers lors de l’utilisation d’un partenaire.</span><span class="sxs-lookup"><span data-stu-id="5325c-116">The following illustration and description explain how the third-party data import process works when working with a partner.</span></span>
  
![Fonctionnement du processus d’importation de données tierces](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="5325c-118">Le client travaille avec son partenaire de choix pour configurer un connecteur qui extraira les éléments de la source de données tierce, puis importez ces éléments dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-118">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="5325c-119">Le connecteur partenaire se connecte à des sources de données tierces via une API tierce (sur la base planifiée ou configurée) et extrait des éléments de la source de données.</span><span class="sxs-lookup"><span data-stu-id="5325c-119">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="5325c-120">Le connecteur partenaire convertit le contenu d’un élément dans un format de message électronique.</span><span class="sxs-lookup"><span data-stu-id="5325c-120">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="5325c-121">Consultez la section [more information](#more-information) pour obtenir une description du schéma de format de message.</span><span class="sxs-lookup"><span data-stu-id="5325c-121">See the [More information](#more-information) section for a description of the message-format schema.</span></span> 
    
3. <span data-ttu-id="5325c-122">Le connecteur partenaire se connecte au service Azure dans Office 365 à l’aide du service Web Exchange (EWS) via un point de terminaison connu.</span><span class="sxs-lookup"><span data-stu-id="5325c-122">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="5325c-p104">Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="5325c-p104">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="5325c-125">a.</span><span class="sxs-lookup"><span data-stu-id="5325c-125">a.</span></span> <span data-ttu-id="5325c-126">**Éléments dont l’ID d’utilisateur correspond à un compte d’utilisateur Office 365 :** Si le connecteur partenaire peut mapper l’ID utilisateur de l’élément dans la source de données tierce à un ID d’utilisateur spécifique dans Office 365, l’élément est copié dans le dossier **purges** du dossier éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5325c-126">**Items that have a user ID that corresponds to an Office 365 user account:** If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="5325c-127">Les utilisateurs ne peuvent pas accéder aux éléments du dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="5325c-127">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="5325c-128">Toutefois, vous pouvez utiliser les outils eDiscovery d’Office 365 pour rechercher des éléments dans le dossier purges.</span><span class="sxs-lookup"><span data-stu-id="5325c-128">However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="5325c-129">b.</span><span class="sxs-lookup"><span data-stu-id="5325c-129">b.</span></span> <span data-ttu-id="5325c-130">**Éléments qui n’ont pas d’ID utilisateur correspondant à un compte d’utilisateur Office 365 :** Si le connecteur partenaire ne peut pas mapper l’ID utilisateur d’un élément sur un ID d’utilisateur spécifique dans Office 365, l’élément est copié dans le dossier **boîte de réception** de la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="5325c-130">**Items that don't have a user ID that corresponds to an Office 365 user account:** If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="5325c-131">L’importation d’éléments dans la boîte de réception permet à un membre de votre organisation ou à vous-même de vous connecter à la boîte aux lettres tierce pour visualiser et gérer ces éléments, et de voir si des ajustements doivent être effectués dans la configuration du connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="5325c-131">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="5325c-132">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="5325c-132">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="5325c-133">Un composant clé pour l’archivage de données tierces dans Office 365 est de trouver et d’utiliser un partenaire Microsoft spécialisé dans la capture de données à partir d’une source de données tierce et l’importation dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-133">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365.</span></span> <span data-ttu-id="5325c-134">Une fois les données importées, elles peuvent être archivées et conservées avec les autres données Microsoft de votre organisation, telles que les messages électroniques provenant d’Exchange et de documents provenant de SharePoint et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="5325c-134">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="5325c-135">Un partenaire crée un connecteur qui extrait les données des sources de données tierces de votre organisation (par exemple, BlackBerry, Facebook, Google +, Thomson Reuters, Twitter et YouTube) et transmet ces données à une API Office 365 qui importe des éléments dans les boîtes aux lettres Exchange en tant que messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="5325c-135">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="5325c-136">Les sections suivantes répertorient les partenaires Microsoft (et les sources de données tierces qu’ils prennent en charge) qui participent au programme d’archivage de données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-136">The following sections list the Microsoft partners (and the third-party data sources they support) that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="5325c-137">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="5325c-137">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="5325c-138">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="5325c-138">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="5325c-139">Globanet</span><span class="sxs-lookup"><span data-stu-id="5325c-139">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="5325c-140">OpenText</span><span class="sxs-lookup"><span data-stu-id="5325c-140">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="5325c-141">Smarsh</span><span class="sxs-lookup"><span data-stu-id="5325c-141">Smarsh</span></span>](#smarsh)

[<span data-ttu-id="5325c-142">Verba</span><span class="sxs-lookup"><span data-stu-id="5325c-142">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="5325c-143">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="5325c-143">17a-4 LLC</span></span>

<span data-ttu-id="5325c-144">[17A-4 LLC](https://www.17a-4.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-144">[17a-4 LLC](https://www.17a-4.com) supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="5325c-145">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="5325c-145">BlackBerry</span></span>
    
- <span data-ttu-id="5325c-146">Flux de données Bloomberg</span><span class="sxs-lookup"><span data-stu-id="5325c-146">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="5325c-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="5325c-147">Cisco Jabber</span></span>
    
- <span data-ttu-id="5325c-148">FactSet</span><span class="sxs-lookup"><span data-stu-id="5325c-148">FactSet</span></span>
    
- <span data-ttu-id="5325c-149">HipChat</span><span class="sxs-lookup"><span data-stu-id="5325c-149">HipChat</span></span>
    
- <span data-ttu-id="5325c-150">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="5325c-150">InvestEdge</span></span>
    
- <span data-ttu-id="5325c-151">LivePerson</span><span class="sxs-lookup"><span data-stu-id="5325c-151">LivePerson</span></span>
    
- <span data-ttu-id="5325c-152">Flux de données MessageLabs</span><span class="sxs-lookup"><span data-stu-id="5325c-152">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="5325c-153">OpenText</span><span class="sxs-lookup"><span data-stu-id="5325c-153">OpenText</span></span>
    
- <span data-ttu-id="5325c-154">Aide en direct « cliquer pour appeler » Oracle/ATG</span><span class="sxs-lookup"><span data-stu-id="5325c-154">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="5325c-155">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="5325c-155">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="5325c-156">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="5325c-156">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="5325c-157">MindAlign</span><span class="sxs-lookup"><span data-stu-id="5325c-157">MindAlign</span></span>
    
- <span data-ttu-id="5325c-158">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="5325c-158">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="5325c-159">Skype Entreprise (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="5325c-159">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="5325c-160">Skype Entreprise Online (Lync Online)</span><span class="sxs-lookup"><span data-stu-id="5325c-160">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="5325c-161">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="5325c-161">SQL Databases</span></span>
    
- <span data-ttu-id="5325c-162">Squawker</span><span class="sxs-lookup"><span data-stu-id="5325c-162">Squawker</span></span>
    
- <span data-ttu-id="5325c-163">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="5325c-163">Thomson Reuters Eikon Messenger</span></span>
  

  
### <a name="archivesocial"></a><span data-ttu-id="5325c-164">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="5325c-164">ArchiveSocial</span></span>

<span data-ttu-id="5325c-165">[ArchiveSocial](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-165">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5325c-166">Facebook</span><span class="sxs-lookup"><span data-stu-id="5325c-166">Facebook</span></span>
    
- <span data-ttu-id="5325c-167">Flickr</span><span class="sxs-lookup"><span data-stu-id="5325c-167">Flickr</span></span>
    
- <span data-ttu-id="5325c-168">Instagram</span><span class="sxs-lookup"><span data-stu-id="5325c-168">Instagram</span></span>
    
- <span data-ttu-id="5325c-169">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5325c-169">LinkedIn</span></span>
    
- <span data-ttu-id="5325c-170">Pinterest</span><span class="sxs-lookup"><span data-stu-id="5325c-170">Pinterest</span></span>
    
- <span data-ttu-id="5325c-171">Twitter</span><span class="sxs-lookup"><span data-stu-id="5325c-171">Twitter</span></span>
    
- <span data-ttu-id="5325c-172">YouTube</span><span class="sxs-lookup"><span data-stu-id="5325c-172">YouTube</span></span>
    
- <span data-ttu-id="5325c-173">Vimeo</span><span class="sxs-lookup"><span data-stu-id="5325c-173">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="5325c-174">Globanet</span><span class="sxs-lookup"><span data-stu-id="5325c-174">Globanet</span></span>

<span data-ttu-id="5325c-175">[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-175">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5325c-176">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="5325c-176">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="5325c-177">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-177">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-178">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-178">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-179">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-179">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-180">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-180">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-181">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="5325c-181">Bloomberg Chat</span></span>
    
- <span data-ttu-id="5325c-182">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="5325c-182">Bloomberg Mail</span></span>
    
- <span data-ttu-id="5325c-183">Box</span><span class="sxs-lookup"><span data-stu-id="5325c-183">Box</span></span>
    
- <span data-ttu-id="5325c-184">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="5325c-184">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="5325c-185">Serveur de &amp; présence de messagerie instantanée Cisco (version 10, v 10.5.1 Su1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="5325c-185">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="5325c-186">Teams de Cisco Webex</span><span class="sxs-lookup"><span data-stu-id="5325c-186">Cisco Webex Teams</span></span>

- <span data-ttu-id="5325c-187">ShareFile de &amp; l’espace de travail de Citrix</span><span class="sxs-lookup"><span data-stu-id="5325c-187">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="5325c-188">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="5325c-188">CrowdCompass</span></span>

- <span data-ttu-id="5325c-189">Fichiers texte personnalisés, délimités</span><span class="sxs-lookup"><span data-stu-id="5325c-189">Custom-delimited text files</span></span>
    
- <span data-ttu-id="5325c-190">Fichiers XML personnalisés</span><span class="sxs-lookup"><span data-stu-id="5325c-190">Custom XML files</span></span>
    
- <span data-ttu-id="5325c-191">Facebook (pages)</span><span class="sxs-lookup"><span data-stu-id="5325c-191">Facebook (Pages)</span></span>
    
- <span data-ttu-id="5325c-192">Factset</span><span class="sxs-lookup"><span data-stu-id="5325c-192">Factset</span></span>
    
- <span data-ttu-id="5325c-193">FXConnect</span><span class="sxs-lookup"><span data-stu-id="5325c-193">FXConnect</span></span>
    
- <span data-ttu-id="5325c-194">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="5325c-194">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="5325c-195">Jive</span><span class="sxs-lookup"><span data-stu-id="5325c-195">Jive</span></span>
    
- <span data-ttu-id="5325c-196">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="5325c-196">Macgregor XIP</span></span>

- <span data-ttu-id="5325c-197">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="5325c-197">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="5325c-198">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="5325c-198">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="5325c-199">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5325c-199">Microsoft Teams</span></span>
       
- <span data-ttu-id="5325c-200">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="5325c-200">Microsoft Yammer</span></span>
    
- <span data-ttu-id="5325c-201">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="5325c-201">Mobile Guard</span></span>
    
- <span data-ttu-id="5325c-202">Pivot</span><span class="sxs-lookup"><span data-stu-id="5325c-202">Pivot</span></span>
    
- <span data-ttu-id="5325c-203">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="5325c-203">Salesforce Chatter</span></span>

- <span data-ttu-id="5325c-204">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="5325c-204">Skype for Business Online</span></span>
    
- <span data-ttu-id="5325c-205">Skype Entreprise, versions 2007 R2-2016 (sur site)</span><span class="sxs-lookup"><span data-stu-id="5325c-205">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="5325c-206">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="5325c-206">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="5325c-207">Concert</span><span class="sxs-lookup"><span data-stu-id="5325c-207">Symphony</span></span>
    
- <span data-ttu-id="5325c-208">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="5325c-208">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="5325c-209">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="5325c-209">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="5325c-210">Thomson Reuters Dealings 3000/FX Trading</span><span class="sxs-lookup"><span data-stu-id="5325c-210">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="5325c-211">Twitter</span><span class="sxs-lookup"><span data-stu-id="5325c-211">Twitter</span></span>
    
- <span data-ttu-id="5325c-212">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="5325c-212">UBS Chat</span></span>
    
- <span data-ttu-id="5325c-213">YouTube</span><span class="sxs-lookup"><span data-stu-id="5325c-213">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="5325c-214">OpenText</span><span class="sxs-lookup"><span data-stu-id="5325c-214">OpenText</span></span>

<span data-ttu-id="5325c-215">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-215">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5325c-216">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="5325c-216">Axs Encrypted</span></span>
    
- <span data-ttu-id="5325c-217">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="5325c-217">Axs Exchange</span></span>
    
- <span data-ttu-id="5325c-218">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="5325c-218">Axs Local Archive</span></span>
    
- <span data-ttu-id="5325c-219">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="5325c-219">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="5325c-220">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="5325c-220">Axs Signed</span></span>
    
- <span data-ttu-id="5325c-221">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="5325c-221">Bloomberg</span></span>
    
- <span data-ttu-id="5325c-222">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="5325c-222">Thomson Reuters</span></span>
  
### <a name="smarsh"></a><span data-ttu-id="5325c-223">Smarsh</span><span class="sxs-lookup"><span data-stu-id="5325c-223">Smarsh</span></span>

<span data-ttu-id="5325c-224">[Smarsh](https://www.smarsh.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-224">[Smarsh](https://www.smarsh.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5325c-225">VISERA</span><span class="sxs-lookup"><span data-stu-id="5325c-225">AIM</span></span>
    
- <span data-ttu-id="5325c-226">American Idol</span><span class="sxs-lookup"><span data-stu-id="5325c-226">American Idol</span></span>
    
- <span data-ttu-id="5325c-227">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="5325c-227">Apple Juice</span></span>
    
- <span data-ttu-id="5325c-228">AOL avec client Pivot</span><span class="sxs-lookup"><span data-stu-id="5325c-228">AOL with Pivot client</span></span>
    
- <span data-ttu-id="5325c-229">Tréma</span><span class="sxs-lookup"><span data-stu-id="5325c-229">Ares</span></span>
    
- <span data-ttu-id="5325c-230">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-230">Bazaar Voice</span></span>
    
- <span data-ttu-id="5325c-231">Bear Share</span><span class="sxs-lookup"><span data-stu-id="5325c-231">Bear Share</span></span>
    
- <span data-ttu-id="5325c-232">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="5325c-232">Bit Torrent</span></span>
    
- <span data-ttu-id="5325c-233">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-233">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-234">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-234">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-235">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-235">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-236">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="5325c-236">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5325c-237">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="5325c-237">Bloomberg Mail</span></span>
    
- <span data-ttu-id="5325c-238">CellTrust</span><span class="sxs-lookup"><span data-stu-id="5325c-238">CellTrust</span></span>
    
- <span data-ttu-id="5325c-239">Chat Import</span><span class="sxs-lookup"><span data-stu-id="5325c-239">Chat Import</span></span>
    
- <span data-ttu-id="5325c-240">Chat Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="5325c-240">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="5325c-241">Brouillage</span><span class="sxs-lookup"><span data-stu-id="5325c-241">Chatter</span></span>
    
- <span data-ttu-id="5325c-242">Serveur de &amp; présence de messagerie instantanée Cisco (version 9.0.1, version 9.1, v 9.1.1 Su1, version 10, v 10.5.1 Su1)</span><span class="sxs-lookup"><span data-stu-id="5325c-242">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="5325c-243">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="5325c-243">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="5325c-244">Collaboration Import</span><span class="sxs-lookup"><span data-stu-id="5325c-244">Collaboration Import</span></span>
    
- <span data-ttu-id="5325c-245">Collaboration Real Time Logging</span><span class="sxs-lookup"><span data-stu-id="5325c-245">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="5325c-246">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="5325c-246">Direct Connect</span></span>
    
- <span data-ttu-id="5325c-247">Facebook</span><span class="sxs-lookup"><span data-stu-id="5325c-247">Facebook</span></span>
    
- <span data-ttu-id="5325c-248">FactSet</span><span class="sxs-lookup"><span data-stu-id="5325c-248">FactSet</span></span>
    
- <span data-ttu-id="5325c-249">FastTrack</span><span class="sxs-lookup"><span data-stu-id="5325c-249">FastTrack</span></span>
    
- <span data-ttu-id="5325c-250">Gnutella</span><span class="sxs-lookup"><span data-stu-id="5325c-250">Gnutella</span></span>
    
- <span data-ttu-id="5325c-251">Google +</span><span class="sxs-lookup"><span data-stu-id="5325c-251">Google+</span></span>
    
- <span data-ttu-id="5325c-252">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="5325c-252">GoToMyPC</span></span>
    
- <span data-ttu-id="5325c-253">Hopster</span><span class="sxs-lookup"><span data-stu-id="5325c-253">Hopster</span></span>
    
- <span data-ttu-id="5325c-254">HubConnex</span><span class="sxs-lookup"><span data-stu-id="5325c-254">HubConnex</span></span>
    
- <span data-ttu-id="5325c-255">IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)</span><span class="sxs-lookup"><span data-stu-id="5325c-255">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="5325c-256">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="5325c-256">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="5325c-257">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="5325c-257">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="5325c-258">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="5325c-258">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="5325c-259">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="5325c-259">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="5325c-260">IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)</span><span class="sxs-lookup"><span data-stu-id="5325c-260">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="5325c-261">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="5325c-261">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="5325c-262">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="5325c-262">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="5325c-263">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="5325c-263">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="5325c-264">GLACE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="5325c-264">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="5325c-265">IM Import</span><span class="sxs-lookup"><span data-stu-id="5325c-265">IM Import</span></span>
    
- <span data-ttu-id="5325c-266">IM Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="5325c-266">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="5325c-267">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="5325c-267">Indii Messenger</span></span>
    
- <span data-ttu-id="5325c-268">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="5325c-268">Instant Bloomberg</span></span>
    
- <span data-ttu-id="5325c-269">SALLE</span><span class="sxs-lookup"><span data-stu-id="5325c-269">IRC</span></span>
    
- <span data-ttu-id="5325c-270">Jive</span><span class="sxs-lookup"><span data-stu-id="5325c-270">Jive</span></span>
    
- <span data-ttu-id="5325c-271">Jive 6 Real Time Logging (version 6, version 7)</span><span class="sxs-lookup"><span data-stu-id="5325c-271">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="5325c-272">Jive Import</span><span class="sxs-lookup"><span data-stu-id="5325c-272">Jive Import</span></span>
    
- <span data-ttu-id="5325c-273">JXTA</span><span class="sxs-lookup"><span data-stu-id="5325c-273">JXTA</span></span>
    
- <span data-ttu-id="5325c-274">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5325c-274">LinkedIn</span></span>
    
- <span data-ttu-id="5325c-275">Microsoft Lync (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="5325c-275">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="5325c-276">MFTP</span><span class="sxs-lookup"><span data-stu-id="5325c-276">MFTP</span></span>
    
- <span data-ttu-id="5325c-277">Microsoft Lync 2013 Voix</span><span class="sxs-lookup"><span data-stu-id="5325c-277">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="5325c-278">Microsoft SharePoint (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="5325c-278">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="5325c-279">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="5325c-279">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="5325c-280">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="5325c-280">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="5325c-281">MindAlign</span><span class="sxs-lookup"><span data-stu-id="5325c-281">MindAlign</span></span>
    
- <span data-ttu-id="5325c-282">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="5325c-282">Mobile Guard</span></span>
    
- <span data-ttu-id="5325c-283">SYMPATICO</span><span class="sxs-lookup"><span data-stu-id="5325c-283">MSN</span></span>
    
- <span data-ttu-id="5325c-284">My Space</span><span class="sxs-lookup"><span data-stu-id="5325c-284">My Space</span></span>
    
- <span data-ttu-id="5325c-285">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="5325c-285">NEONetwork</span></span>
    
- <span data-ttu-id="5325c-286">Office 365 Lync dédié</span><span class="sxs-lookup"><span data-stu-id="5325c-286">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="5325c-287">MI partagée Office 365</span><span class="sxs-lookup"><span data-stu-id="5325c-287">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="5325c-288">Pinterest</span><span class="sxs-lookup"><span data-stu-id="5325c-288">Pinterest</span></span>
    
- <span data-ttu-id="5325c-289">Pivot</span><span class="sxs-lookup"><span data-stu-id="5325c-289">Pivot</span></span>
    
- <span data-ttu-id="5325c-290">QQ</span><span class="sxs-lookup"><span data-stu-id="5325c-290">QQ</span></span>
    
- <span data-ttu-id="5325c-291">Skype Entreprise 2015</span><span class="sxs-lookup"><span data-stu-id="5325c-291">Skype for Business 2015</span></span>
    
- <span data-ttu-id="5325c-292">SoftEther</span><span class="sxs-lookup"><span data-stu-id="5325c-292">SoftEther</span></span>
    
- <span data-ttu-id="5325c-293">Concert</span><span class="sxs-lookup"><span data-stu-id="5325c-293">Symphony</span></span>
    
- <span data-ttu-id="5325c-294">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="5325c-294">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="5325c-295">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="5325c-295">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="5325c-296">Termes</span><span class="sxs-lookup"><span data-stu-id="5325c-296">Tor</span></span>
    
- <span data-ttu-id="5325c-297">TTT</span><span class="sxs-lookup"><span data-stu-id="5325c-297">TTT</span></span>
    
- <span data-ttu-id="5325c-298">Twitter</span><span class="sxs-lookup"><span data-stu-id="5325c-298">Twitter</span></span>
    
- <span data-ttu-id="5325c-299">WinMX</span><span class="sxs-lookup"><span data-stu-id="5325c-299">WinMX</span></span>
    
- <span data-ttu-id="5325c-300">Winny</span><span class="sxs-lookup"><span data-stu-id="5325c-300">Winny</span></span>
    
- <span data-ttu-id="5325c-301">Yahoo</span><span class="sxs-lookup"><span data-stu-id="5325c-301">Yahoo</span></span>
    
- <span data-ttu-id="5325c-302">Yammer</span><span class="sxs-lookup"><span data-stu-id="5325c-302">Yammer</span></span>
    
- <span data-ttu-id="5325c-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="5325c-303">YouTube</span></span>
    

### <a name="verba"></a><span data-ttu-id="5325c-304">Verba</span><span class="sxs-lookup"><span data-stu-id="5325c-304">Verba</span></span>

<span data-ttu-id="5325c-305">[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-305">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5325c-306">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="5325c-306">Avaya Aura Video</span></span>
    
- <span data-ttu-id="5325c-307">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-307">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="5325c-308">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="5325c-308">Avtec Radio</span></span>
    
- <span data-ttu-id="5325c-309">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="5325c-309">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="5325c-310">BroadSoft Video</span><span class="sxs-lookup"><span data-stu-id="5325c-310">BroadSoft Video</span></span>
    
- <span data-ttu-id="5325c-311">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-311">BroadSoft Voice</span></span>
    
- <span data-ttu-id="5325c-312">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-312">Centile Voice</span></span>
    
- <span data-ttu-id="5325c-313">Cisco Jabber IM</span><span class="sxs-lookup"><span data-stu-id="5325c-313">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="5325c-314">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="5325c-314">Cisco UC Video</span></span>
    
- <span data-ttu-id="5325c-315">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-315">Cisco UC Voice</span></span>
    
- <span data-ttu-id="5325c-316">Cisco UCCX/UCCE vidéo</span><span class="sxs-lookup"><span data-stu-id="5325c-316">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="5325c-317">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-317">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="5325c-318">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="5325c-318">ESChat Radio</span></span>
    
- <span data-ttu-id="5325c-319">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="5325c-319">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="5325c-320">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-320">IP Trade Voice</span></span>
    
- <span data-ttu-id="5325c-321">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="5325c-321">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="5325c-322">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="5325c-322">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="5325c-323">Mitel MiContact Center for Lync (prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="5325c-323">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="5325c-324">Oracle / Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="5325c-324">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="5325c-325">Oracle / Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-325">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="5325c-326">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-326">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="5325c-327">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="5325c-327">SIPREC Video</span></span>
    
-  <span data-ttu-id="5325c-328">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-328">SIPREC Voice</span></span> 
    
- <span data-ttu-id="5325c-329">Skype Entreprise / MI Lync</span><span class="sxs-lookup"><span data-stu-id="5325c-329">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="5325c-330">Skype Entreprise / Vidéo Lync</span><span class="sxs-lookup"><span data-stu-id="5325c-330">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="5325c-331">Skype Entreprise / Voix Lync</span><span class="sxs-lookup"><span data-stu-id="5325c-331">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="5325c-332">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-332">Speakerbus Voice</span></span>
    
- <span data-ttu-id="5325c-333">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="5325c-333">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="5325c-334">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-334">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="5325c-335">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="5325c-335">Truphone Voice</span></span>
    
- <span data-ttu-id="5325c-336">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="5325c-336">TwistedPair Radio</span></span>
    
- <span data-ttu-id="5325c-337">Écran d’ordinateur de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="5325c-337">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="5325c-338">Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5325c-338">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="5325c-339">Voici les étapes à suivre pour créer et configurer une boîte aux lettres de données tierce pour l’importation de données dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-339">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365.</span></span> <span data-ttu-id="5325c-340">Comme expliqué précédemment, les éléments sont importés dans cette boîte aux lettres si le connecteur partenaire ne peut pas mapper l’ID utilisateur de l’élément sur un compte d’utilisateur Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-340">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="5325c-341">**Effectuez ces tâches dans le centre d’administration Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="5325c-341">**Complete these tasks in the Microsoft 365 admin center**</span></span>
  
1. <span data-ttu-id="5325c-342">Créez un compte d’utilisateur dans Office 365 et attribuez-lui une licence Exchange Online plan 2 ; Voir [Ajouter des utilisateurs à Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span><span class="sxs-lookup"><span data-stu-id="5325c-342">Create a user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span></span> <span data-ttu-id="5325c-343">Une licence plan 2 est nécessaire pour placer la boîte aux lettres en conservation pour litige ou pour activer une boîte aux lettres d’archivage dont le quota de stockage est illimité.</span><span class="sxs-lookup"><span data-stu-id="5325c-343">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="5325c-344">Ajoutez le compte d’utilisateur pour la boîte aux lettres de données tierce au rôle d’administrateur d' **administrateur Exchange** dans Office 365 ; consultez la rubrique [assigner des rôles d’administrateur dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="5325c-344">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="5325c-345">Notez les informations d’identification pour ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5325c-345">Write down the credentials for this user account.</span></span> <span data-ttu-id="5325c-346">Vous devez les fournir à votre partenaire, comme décrit à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="5325c-346">You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="5325c-347">**Effectuer ces tâches dans le centre d’administration Exchange**</span><span class="sxs-lookup"><span data-stu-id="5325c-347">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="5325c-348">Masquer la boîte aux lettres de données tierce dans le carnet d’adresses et les autres listes d’adresses de votre organisation ; consultez la rubrique [Manage User mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span><span class="sxs-lookup"><span data-stu-id="5325c-348">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span></span> <span data-ttu-id="5325c-349">Vous pouvez également exécuter la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="5325c-349">Alternatively, you can run the following PowerShell command:</span></span>
    
    ```powershell
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="5325c-350">Attribuer l’autorisation **FullAccess** à la boîte aux lettres de données tierce afin que les administrateurs ou les responsables de la mise en conformité puissent ouvrir la boîte aux lettres de données tierce dans le client de bureau Outlook ; consultez la rubrique [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="5325c-350">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="5325c-351">Activez les fonctionnalités suivantes d’Office 365 liées à la conformité pour la boîte aux lettres de données tierce :</span><span class="sxs-lookup"><span data-stu-id="5325c-351">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="5325c-352">Activer la boîte aux lettres d’archivage ; consultez la rubrique [activation des boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [activez un archivage illimité](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="5325c-352">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="5325c-353">Cela vous permet de libérer de l’espace de stockage dans la boîte aux lettres principale en configurant une stratégie d’archivage qui déplace les éléments de données tiers vers la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="5325c-353">This lets you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="5325c-354">Vous disposez ainsi d’un espace de stockage illimité pour les données tierces.</span><span class="sxs-lookup"><span data-stu-id="5325c-354">This provides you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="5325c-355">Placez la boîte aux lettres de données tierces en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5325c-355">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="5325c-356">Vous pouvez également appliquer une stratégie de rétention Office 365 dans le centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5325c-356">You can also apply an Office 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="5325c-357">Le fait de placer cette boîte aux lettres en conservation conserve des éléments de données tiers (indéfiniment ou pour une durée spécifiée) et les empêche d’être purgés de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5325c-357">Placing this mailbox on hold retains third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="5325c-358">Consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-358">See one of the following topics:</span></span>
    
      - [<span data-ttu-id="5325c-359">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="5325c-359">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="5325c-360">Vue d'ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="5325c-360">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    - <span data-ttu-id="5325c-361">Activez la journalisation d’audit de boîte aux lettres pour l’accès de propriétaire, de délégué et d’administrateur à la boîte aux lettres de données tierces ; consultez la rubrique [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="5325c-361">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="5325c-362">Cela vous permet d’auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="5325c-362">This allows you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="5325c-363">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="5325c-363">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="5325c-364">L’étape suivante consiste à configurer les boîtes aux lettres des utilisateurs pour prendre en charge les données tierces.</span><span class="sxs-lookup"><span data-stu-id="5325c-364">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="5325c-365">Effectuez ces tâches à l’aide du centre d’administration Exchange ou à l’aide des applets de commande Windows PowerShell correspondantes.</span><span class="sxs-lookup"><span data-stu-id="5325c-365">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="5325c-366">Activez la boîte aux lettres d’archivage pour chaque utilisateur ; consultez la rubrique [activation des boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [activez un archivage illimité](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="5325c-366">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="5325c-367">Placer les boîtes aux lettres utilisateur en conservation pour litige ou appliquer une stratégie de rétention Office 365 ; consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-367">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="5325c-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="5325c-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="5325c-369">Vue d'ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="5325c-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="5325c-370">Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="5325c-370">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="5325c-371">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="5325c-371">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="5325c-372">La dernière étape consiste à fournir à votre partenaire les informations suivantes pour lui permettre de configurer le connecteur afin qu’il se connecte à votre organisation Office 365 pour importer les données vers les boîtes aux lettres des utilisateurs et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="5325c-372">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="5325c-373">Le point de terminaison utilisé pour se connecter au service Azure dans Office 365 :</span><span class="sxs-lookup"><span data-stu-id="5325c-373">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```text
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="5325c-374">Les informations d’identification de connexion (ID d’utilisateur et mot de passe Office 365) de la boîte aux lettres de données tierce que vous avez créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="5325c-374">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="5325c-375">Ces informations d’identification sont requises pour que le connecteur partenaire puisse accéder aux éléments et les importer dans les boîtes aux lettres utilisateur et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="5325c-375">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="5325c-376">Étape 5 : enregistrer le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5325c-376">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="5325c-377">À partir du 30 septembre 2018, le service Azure d’Office 365 commencera à utiliser l’authentification moderne dans Exchange Online pour authentifier les connecteurs de données tiers qui tentent de se connecter à votre organisation Office 365 pour importer des données.</span><span class="sxs-lookup"><span data-stu-id="5325c-377">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data.</span></span> <span data-ttu-id="5325c-378">La raison de cette modification est que l’authentification moderne offre davantage de sécurité que la méthode actuelle, basée sur des connecteurs tiers de liste d’accès aux utilisateurs qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.</span><span class="sxs-lookup"><span data-stu-id="5325c-378">The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="5325c-379">Pour permettre à un connecteur de données tiers de se connecter à Office 365 à l’aide de la nouvelle méthode d’authentification moderne, un administrateur de votre organisation Office 365 doit consentir à inscrire le connecteur en tant qu’application de service approuvée dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5325c-379">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="5325c-380">Pour ce faire, vous devez accepter une demande d’autorisation pour permettre au connecteur d’accéder aux données de votre organisation dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5325c-380">This is done by accepting a permission request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="5325c-381">Une fois que vous avez accepté cette demande, le connecteur de données tiers est ajouté en tant qu’application d’entreprise à Azure Active Directory et représenté en tant que principal de service.</span><span class="sxs-lookup"><span data-stu-id="5325c-381">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="5325c-382">Pour plus d’informations sur le processus de consentement, consultez la rubrique consentement de l' [administrateur client](https://docs.microsoft.com/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="5325c-382">For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="5325c-383">Voici les étapes à suivre pour accéder à la demande et l’accepter pour enregistrer le connecteur :</span><span class="sxs-lookup"><span data-stu-id="5325c-383">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="5325c-384">Accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et connectez-vous à l’aide des informations d’identification d’un administrateur général Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-384">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="5325c-385">La boîte de dialogue suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5325c-385">The following dialog box is displayed.</span></span> <span data-ttu-id="5325c-386">Vous pouvez développer les signes pour vérifier les autorisations qui seront affectées au connecteur.</span><span class="sxs-lookup"><span data-stu-id="5325c-386">You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="5325c-387">![La boîte de dialogue demande d’autorisations s’affiche.](media/O365-ThirdPartyDataConnector-OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="5325c-387">![The permissions request dialog is displayed](media/O365-ThirdPartyDataConnector-OptIn1.png)</span></span>
2. <span data-ttu-id="5325c-388">Cliquez sur **Accept (Accepter)**.</span><span class="sxs-lookup"><span data-stu-id="5325c-388">Click **Accept**.</span></span>

<span data-ttu-id="5325c-389">Une fois que vous avez accepté la demande, le [portail Azure](https://portal.azure.com) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5325c-389">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="5325c-390">Pour afficher la liste des applications pour votre organisation, cliquez sur**applications d’entreprise** **Azure Active Directory** > .</span><span class="sxs-lookup"><span data-stu-id="5325c-390">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="5325c-391">Le connecteur de données tiers 365 Office est affiché dans le panneau **applications d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="5325c-391">The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5325c-392">Après le 30 septembre 2018, les données tierces ne seront plus importées dans les boîtes aux lettres de votre organisation si vous n’enregistrez pas un connecteur de données tiers dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5325c-392">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="5325c-393">Remarque les connecteurs de données tiers existants (ceux créés avant le 30 septembre 2018) doivent également être enregistrés dans Azure Active Directory en suivant la procédure de l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="5325c-393">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="5325c-394">Révocation du consentement pour un connecteur de données tiers</span><span class="sxs-lookup"><span data-stu-id="5325c-394">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="5325c-395">Une fois que votre organisation a accepté la demande d’autorisations pour enregistrer un connecteur de données tiers dans Azure Active Directory, votre organisation peut révoquer ce consentement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="5325c-395">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="5325c-396">Toutefois, la révocation de l’autorisation pour un connecteur signifie que les données de la source de données tierce ne seront plus importées dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-396">However, revoking the consent for a connector means that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="5325c-397">Pour révoquer le consentement d’un connecteur de données tiers, vous pouvez supprimer l’application (en supprimant l’entité de service correspondante) à partir d’Azure Active Directory à l’aide du panneau **applications d’entreprise** dans le portail Azure ou en utilisant la commande [Remove-MsolServicePrincipal](https://docs.microsoft.com/powershell/module/msonline/remove-msolserviceprincipal) dans Office 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5325c-397">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell.</span></span> <span data-ttu-id="5325c-398">Vous pouvez également utiliser l’applet de commande [Remove-AzureADServicePrincipal](https://docs.microsoft.com/powershell/module/azuread/remove-azureadserviceprincipal) dans Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5325c-398">You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="5325c-399">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5325c-399">More information</span></span>

- <span data-ttu-id="5325c-400">Comme indiqué précédemment, les éléments des sources de données tierces sont importés vers les boîtes aux lettres Exchange en tant que messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="5325c-400">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="5325c-401">Le connecteur partenaire importe l’élément à l’aide d’un schéma requis par l’API Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-401">The partner connector imports the item using a schema required by the Office 365 API.</span></span> <span data-ttu-id="5325c-402">Le tableau suivant décrit les propriétés de message d’un élément d’une source de données tierces après son importation vers une boîte aux lettres Exchange en tant que message électronique.</span><span class="sxs-lookup"><span data-stu-id="5325c-402">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="5325c-403">Le tableau indique également si la propriété de message est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5325c-403">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="5325c-404">Les propriétés obligatoires doivent être renseignées.</span><span class="sxs-lookup"><span data-stu-id="5325c-404">Mandatory properties must be populated.</span></span> <span data-ttu-id="5325c-405">Si une propriété obligatoire est manquante dans un élément, celui-ci ne sera pas importé dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-405">If an item is missing a mandatory property, it won't be imported to Office 365.</span></span> <span data-ttu-id="5325c-406">Le processus d’importation renvoie un message d’erreur expliquant pourquoi un élément n’a pas été importé et quelle est la propriété manquante.</span><span class="sxs-lookup"><span data-stu-id="5325c-406">The import process returns an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="5325c-407">**Propriété de message**</span><span class="sxs-lookup"><span data-stu-id="5325c-407">**Message property**</span></span>|<span data-ttu-id="5325c-408">**Obligatoire ?**</span><span class="sxs-lookup"><span data-stu-id="5325c-408">**Mandatory?**</span></span>|<span data-ttu-id="5325c-409">**Description**</span><span class="sxs-lookup"><span data-stu-id="5325c-409">**Description**</span></span>|<span data-ttu-id="5325c-410">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="5325c-410">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="5325c-411">**FROM**</span><span class="sxs-lookup"><span data-stu-id="5325c-411">**FROM**</span></span> <br/> |<span data-ttu-id="5325c-412">Oui</span><span class="sxs-lookup"><span data-stu-id="5325c-412">Yes</span></span>  <br/> |<span data-ttu-id="5325c-413">Utilisateur qui a initialement créé ou envoyé l’élément dans la source de données tierces.</span><span class="sxs-lookup"><span data-stu-id="5325c-413">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="5325c-414">Le connecteur partenaire tente de mapper l’ID utilisateur à partir de l’élément source (par exemple, un handle Twitter) vers un compte d’utilisateur Office 365 pour tous les participants (utilisateurs figurant dans les champs de et à).</span><span class="sxs-lookup"><span data-stu-id="5325c-414">The partner connector attempts to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="5325c-415">Une copie du message sera importée dans la boîte aux lettres de chaque participant.</span><span class="sxs-lookup"><span data-stu-id="5325c-415">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="5325c-416">Si aucun des participants de l’élément ne peut être mappé à un compte d’utilisateur Office 365, l’élément sera importé dans la boîte aux lettres d’archivage tierce dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5325c-416">If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.</span></span>  <br/> <br/> <span data-ttu-id="5325c-417">Le participant identifié comme l’expéditeur de l’élément doit disposer d’une boîte aux lettres active dans l’organisation Office 365 pour laquelle l’élément est importé.</span><span class="sxs-lookup"><span data-stu-id="5325c-417">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to.</span></span> <span data-ttu-id="5325c-418">Si l’expéditeur ne dispose pas d’une boîte aux lettres active, l’erreur suivante est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="5325c-418">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="5325c-419">**TO**</span><span class="sxs-lookup"><span data-stu-id="5325c-419">**TO**</span></span> <br/> |<span data-ttu-id="5325c-420">Oui</span><span class="sxs-lookup"><span data-stu-id="5325c-420">Yes</span></span>  <br/> |<span data-ttu-id="5325c-421">Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="5325c-421">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="5325c-422">**Objet**</span><span class="sxs-lookup"><span data-stu-id="5325c-422">**SUBJECT**</span></span> <br/> |<span data-ttu-id="5325c-423">Non</span><span class="sxs-lookup"><span data-stu-id="5325c-423">No</span></span>  <br/> |<span data-ttu-id="5325c-424">Objet de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="5325c-424">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="5325c-425">**JOURS**</span><span class="sxs-lookup"><span data-stu-id="5325c-425">**DATE**</span></span> <br/> |<span data-ttu-id="5325c-426">Oui</span><span class="sxs-lookup"><span data-stu-id="5325c-426">Yes</span></span>  <br/> |<span data-ttu-id="5325c-427">Date à laquelle l’élément a été initialement créé ou publié dans la source de données client.</span><span class="sxs-lookup"><span data-stu-id="5325c-427">The date the item was originally created or posted in the customer data source.</span></span> <span data-ttu-id="5325c-428">Par exemple, la date à laquelle un message Twitter a été tweeté.</span><span class="sxs-lookup"><span data-stu-id="5325c-428">For example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="5325c-429">**ENTITÉ**</span><span class="sxs-lookup"><span data-stu-id="5325c-429">**BODY**</span></span> <br/> |<span data-ttu-id="5325c-430">Non</span><span class="sxs-lookup"><span data-stu-id="5325c-430">No</span></span>  <br/> |<span data-ttu-id="5325c-431">Contenu du message ou de la publication.</span><span class="sxs-lookup"><span data-stu-id="5325c-431">The contents of the message or post.</span></span> <span data-ttu-id="5325c-432">Pour certaines sources de données, le contenu de cette propriété peut être identique au contenu de la propriété **SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="5325c-432">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="5325c-433">Pendant le processus d’importation, le connecteur partenaire tente de maintenir la fidélité complète de la source de contenu.</span><span class="sxs-lookup"><span data-stu-id="5325c-433">During the import process, the partner connector attempts to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="5325c-434">Si possible, les fichiers, les graphiques ou tout autre contenu du corps de l’élément source sont inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5325c-434">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="5325c-435">Sinon, le contenu de l’élément source est inclus dans la propriété **ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="5325c-435">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="5325c-436">Le contenu de cette propriété dépend du connecteur du partenaire et de la capacité de la plateforme source.</span><span class="sxs-lookup"><span data-stu-id="5325c-436">The contents of this property depends on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="5325c-437">**CONNEXION**</span><span class="sxs-lookup"><span data-stu-id="5325c-437">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="5325c-438">Non</span><span class="sxs-lookup"><span data-stu-id="5325c-438">No</span></span>  <br/> |<span data-ttu-id="5325c-439">Si un élément de la source de données (par exemple, un tweet dans Twitter ou une conversation de messagerie instantanée) a un fichier joint ou inclut des images, le partenaire Connect tente d’abord d’inclure les pièces jointes dans la propriété **Body** .</span><span class="sxs-lookup"><span data-stu-id="5325c-439">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="5325c-440">Si cela n’est pas possible, il est ajouté à la propriété \* \* ATTACHment \* \*.</span><span class="sxs-lookup"><span data-stu-id="5325c-440">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="5325c-441">Voici d’autres exemples de pièces jointes : mentions J’aime sur Facebook, métadonnées de la source de contenu et réponses à un message ou une publication.</span><span class="sxs-lookup"><span data-stu-id="5325c-441">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |<span data-ttu-id="5325c-442">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="5325c-442">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="5325c-443">Oui</span><span class="sxs-lookup"><span data-stu-id="5325c-443">Yes</span></span>  <br/> | <span data-ttu-id="5325c-444">Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par le connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="5325c-444">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="5325c-445">Le format de cette propriété est `IPM.NOTE.Source.Event`.</span><span class="sxs-lookup"><span data-stu-id="5325c-445">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="5325c-446">(Cette propriété doit commencer par `IPM.NOTE`.</span><span class="sxs-lookup"><span data-stu-id="5325c-446">(This property must begin with  `IPM.NOTE`.</span></span> <span data-ttu-id="5325c-447">Ce format est similaire à celui de la `IPM.NOTE.X` classe message.) Cette propriété inclut les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5325c-447">This format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/><span data-ttu-id="5325c-448">`Source`: Indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="5325c-448">`Source`: Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="5325c-449">`Event`: Indique le type d’activité qui a été effectué dans la source de données tierce qui a produit les éléments ; par exemple, un tweet dans Twitter ou un billet dans Facebook.</span><span class="sxs-lookup"><span data-stu-id="5325c-449">`Event`: Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="5325c-450">Les événements sont propres à la source de données.</span><span class="sxs-lookup"><span data-stu-id="5325c-450">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="5325c-451">L’un des objectifs de cette propriété est de filtrer des éléments spécifiques en fonction de la source de données d’origine d’un élément ou en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="5325c-451">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="5325c-452">Par exemple, lors d’une recherche de découverte électronique, vous pouvez créer une requête de recherche afin de trouver tous les tweets qui ont été publiés par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="5325c-452">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="5325c-453">Lorsque des éléments sont correctement importés dans des boîtes aux lettres dans Office 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="5325c-453">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="5325c-454">Cet identificateur, appelé `x-IngestionCorrelationID`, peut être utilisé à des fins de dépannage ultérieure par les partenaires pour le suivi de bout en bout des éléments.</span><span class="sxs-lookup"><span data-stu-id="5325c-454">This identifier, called  `x-IngestionCorrelationID`, can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="5325c-455">Nous recommandons que vos partenaires récupèrent ces informations et les conservent de leur côté.</span><span class="sxs-lookup"><span data-stu-id="5325c-455">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="5325c-456">Voici un exemple d’une réponse HTTP avec cet identifiant :</span><span class="sxs-lookup"><span data-stu-id="5325c-456">Here's an example of an HTTP response showing this identifier:</span></span>

    ```text
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```

- <span data-ttu-id="5325c-457">Vous pouvez utiliser l’outil de recherche de contenu dans le centre de sécurité et de conformité pour rechercher des éléments qui ont été importés dans des boîtes aux lettres dans Office 365 à partir d’une source de données tierce.</span><span class="sxs-lookup"><span data-stu-id="5325c-457">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="5325c-458">Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de propriétés-valeur de message suivantes dans la zone de mot clé pour une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="5325c-458">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>
    
  - <span data-ttu-id="5325c-459">**`kind:externaldata`**: Utilisez cette paire de valeur de propriété pour rechercher tous les types de données tiers.</span><span class="sxs-lookup"><span data-stu-id="5325c-459">**`kind:externaldata`**: Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="5325c-460">Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contenant le mot « Contoso » dans la propriété Subject de l’élément importé, vous devez `kind:externaldata AND subject:contoso`utiliser la requête par mot clé.</span><span class="sxs-lookup"><span data-stu-id="5325c-460">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="5325c-461">**`itemclass:ipm.externaldata.<third-party data type>`**: Utilisez cette paire de valeur de propriété pour rechercher uniquement un type précis de données tierces.</span><span class="sxs-lookup"><span data-stu-id="5325c-461">**`itemclass:ipm.externaldata.<third-party data type>`**: Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="5325c-462">Par exemple, pour rechercher uniquement les données Facebook qui contiennent le mot « Contoso » dans la propriété Subject, vous devez utiliser la requête `itemclass:ipm.externaldata.Facebook* AND subject:contoso`par mot clé.</span><span class="sxs-lookup"><span data-stu-id="5325c-462">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="5325c-463">Pour obtenir la liste complète des valeurs à utiliser pour les types de données tiers pour `itemclass` la propriété, reportez-vous à la rubrique [utiliser la recherche de contenu pour rechercher des données tierces importées dans Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="5325c-463">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="5325c-464">Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :</span><span class="sxs-lookup"><span data-stu-id="5325c-464">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="5325c-465">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5325c-465">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="5325c-466">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="5325c-466">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
