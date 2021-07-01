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
description: Découvrez comment configurer un connecteur personnalisé pour importer des données tierces à partir de sources de données telles que Salesforce Messenger, Yahoo Messenger ou Yammer.
ms.openlocfilehash: 2026e3c584cb0bc467a2db3903c51b7ed50e51e1
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228758"
---
# <a name="work-with-a-partner-to-archive-third-party-data"></a><span data-ttu-id="83015-103">Collaborer avec un partenaire pour archiver des données tierces</span><span class="sxs-lookup"><span data-stu-id="83015-103">Work with a partner to archive third-party data</span></span>

<span data-ttu-id="83015-104">Vous pouvez travailler avec un partenaire Microsoft pour importer et archiver des données à partir d’une source de données tierce vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-104">You can work with a Microsoft Partner to import and archive data from a third-party data source to Microsoft 365.</span></span> <span data-ttu-id="83015-105">Un partenaire peut vous fournir un connecteur personnalisé qui est configuré pour extraire des éléments de la source de données tierce (régulièrement), puis importer ces éléments.</span><span class="sxs-lookup"><span data-stu-id="83015-105">A partner can provide you with a custom connector that is configured to extract items from the third-party data source (on a regular basis) and then import those items.</span></span> <span data-ttu-id="83015-106">Le connecteur partenaire convertit le contenu d’un élément de la source de données au format de message électronique, puis stocke les éléments dans les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="83015-106">The partner connector converts the content of an item from the data source to an email message format and then stores the items in mailboxes.</span></span> <span data-ttu-id="83015-107">Une fois les données tierces importées, vous pouvez appliquer des fonctionnalités de conformité Microsoft 365 telles que la conservation pour litige, la découverte électronique, l’archivage In-Place, l’audit et les stratégies de rétention Microsoft 365 à ces données.</span><span class="sxs-lookup"><span data-stu-id="83015-107">After third-party data is imported, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, In-Place Archiving, Auditing, and Microsoft 365 retention policies to this data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83015-108">La [solution de conformité des](communication-compliance.md) communications Microsoft 365 ne peut pas être appliquée aux données tierces importées par les connecteurs partenaires mentionnés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="83015-108">The [Communication compliance](communication-compliance.md) solution in Microsoft 365 can't be applied to the third-party data imported by partner connectors mentioned in this article.</span></span>

<span data-ttu-id="83015-109">Voici une vue d’ensemble du processus et des étapes nécessaires pour travailler avec un partenaire Microsoft afin d’importer des données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-109">Here's an overview of the process and the steps necessary to work with a Microsoft Partner to import third-party data.</span></span>

[<span data-ttu-id="83015-110">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="83015-110">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="83015-111">Étape 2 : Créer et configurer une boîte aux lettres de données tierce</span><span class="sxs-lookup"><span data-stu-id="83015-111">Step 2: Create and configure a third-party data mailbox</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-microsoft-365)

[<span data-ttu-id="83015-112">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="83015-112">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="83015-113">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="83015-113">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="83015-114">Étape 5 : Inscrire le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="83015-114">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="83015-115">Fonctionnement du processus d’importation de données tierces</span><span class="sxs-lookup"><span data-stu-id="83015-115">How the third-party data import process works</span></span>

<span data-ttu-id="83015-116">L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tiers lorsque vous travaillez avec un partenaire.</span><span class="sxs-lookup"><span data-stu-id="83015-116">The following illustration and description explain how the third-party data import process works when working with a partner.</span></span>

![Fonctionnement du processus d’importation de données tierces](../media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)

1. <span data-ttu-id="83015-118">Le client travaille avec son partenaire de choix pour configurer un connecteur qui extraira des éléments de la source de données tierce, puis importera ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-118">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Microsoft 365.</span></span>

2. <span data-ttu-id="83015-119">Le connecteur partenaire se connecte à des sources de données tierces via une API tierce (sur une base programmée ou configurée) et extrait des éléments de la source de données.</span><span class="sxs-lookup"><span data-stu-id="83015-119">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="83015-120">Le connecteur partenaire convertit le contenu d’un élément dans un format de message électronique.</span><span class="sxs-lookup"><span data-stu-id="83015-120">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="83015-121">Consultez la section [Plus d’informations](#more-information) pour obtenir une description du schéma de format de message.</span><span class="sxs-lookup"><span data-stu-id="83015-121">See the [More information](#more-information) section for a description of the message-format schema.</span></span>

3. <span data-ttu-id="83015-122">Le connecteur partenaire se connecte au service Azure dans Microsoft 365 en utilisant Exchange Web Service (EWS) via un point de fin connu.</span><span class="sxs-lookup"><span data-stu-id="83015-122">Partner connector connects to the Azure service in Microsoft 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>

4. <span data-ttu-id="83015-p103">Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="83015-p103">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>

   1. <span data-ttu-id="83015-125">**Éléments dont l’ID d’utilisateur correspond à un compte d’utilisateur :** Si le connecteur partenaire peut ma cartographier l’ID utilisateur de l’élément de la source de données tierce sur un ID utilisateur spécifique dans Microsoft 365, l’élément est copié dans le dossier **Purges** du dossier Éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83015-125">**Items that have a user ID that corresponds to a user account:** If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Microsoft 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="83015-126">Les utilisateurs ne peuvent pas accéder aux éléments du dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="83015-126">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="83015-127">Toutefois, vous pouvez utiliser les outils eDiscovery pour rechercher des éléments dans le dossier Purges.</span><span class="sxs-lookup"><span data-stu-id="83015-127">However, you can use eDiscovery tools to search for items in the Purges folder.</span></span>

   1. <span data-ttu-id="83015-128">**Éléments qui n’ont pas d’ID d’utilisateur correspondant à un compte d’utilisateur :** Si le connecteur partenaire ne peut pas ma cartographier l’ID utilisateur d’un  élément sur un ID utilisateur spécifique, l’élément est copié dans le dossier Boîte de réception de la boîte aux lettres de données tierce.</span><span class="sxs-lookup"><span data-stu-id="83015-128">**Items that don't have a user ID that corresponds to a user account:** If the partner connector can't map the user ID of an item to a specific user ID, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="83015-129">L’importation d’éléments dans la boîte de réception permet à un membre de votre organisation ou à vous-même de vous connecter à la boîte aux lettres tierce pour visualiser et gérer ces éléments, et de voir si des ajustements doivent être effectués dans la configuration du connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="83015-129">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>

## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="83015-130">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="83015-130">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="83015-131">Un composant clé pour l’archivage des données tierces dans Microsoft 365 est la recherche et l’collaboration avec un partenaire Microsoft spécialisé dans la capture de données à partir d’une source de données tierce et son importation dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-131">A key component for archiving third-party data in Microsoft 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Microsoft 365.</span></span> <span data-ttu-id="83015-132">Une fois les données importées, elles peuvent être archivées et conservées avec les autres données Microsoft de votre organisation, telles que le courrier électronique provenant de Exchange et les documents de SharePoint et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="83015-132">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="83015-133">Un partenaire crée un connecteur qui extrait les données des sources de données tierces de votre organisation (telles que BlackBerry, Facebook, Google+, Thomson Reuters, Twitter et YouTube) et transmet ces données à une API Microsoft 365 qui importe des éléments dans des boîtes aux lettres Exchange sous forme de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="83015-133">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to a Microsoft 365 API that imports items to Exchange mailboxes as email messages.</span></span>

<span data-ttu-id="83015-134">Les sections suivantes indiquent les partenaires Microsoft (et les sources de données tierces qu’ils supportent) qui participent au programme d’archivage des données tierces dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-134">The following sections list the Microsoft partners (and the third-party data sources they support) that are participating in the program for archiving third-party data in Microsoft 365.</span></span>

[<span data-ttu-id="83015-135">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="83015-135">17a-4 LLC</span></span>](#17a-4-llc)

[<span data-ttu-id="83015-136">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="83015-136">ArchiveSocial</span></span>](#archivesocial)

[<span data-ttu-id="83015-137">Veritas</span><span class="sxs-lookup"><span data-stu-id="83015-137">Veritas</span></span>](#veritas)

[<span data-ttu-id="83015-138">OpenText</span><span class="sxs-lookup"><span data-stu-id="83015-138">OpenText</span></span>](#opentext)

[<span data-ttu-id="83015-139">Smarsh</span><span class="sxs-lookup"><span data-stu-id="83015-139">Smarsh</span></span>](#smarsh)

[<span data-ttu-id="83015-140">Verba</span><span class="sxs-lookup"><span data-stu-id="83015-140">Verba</span></span>](#verba)

### <a name="17a-4-llc"></a><span data-ttu-id="83015-141">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="83015-141">17a-4 LLC</span></span>

<span data-ttu-id="83015-142">[17a-4 LLC](https://www.17a-4.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-142">[17a-4 LLC](https://www.17a-4.com) supports the following third-party data sources:</span></span>

- <span data-ttu-id="83015-143">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="83015-143">BlackBerry</span></span>

- <span data-ttu-id="83015-144">Flux de données Bloomberg</span><span class="sxs-lookup"><span data-stu-id="83015-144">Bloomberg Data Streams</span></span>

- <span data-ttu-id="83015-145">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="83015-145">Cisco Jabber</span></span>

- <span data-ttu-id="83015-146">FactSet</span><span class="sxs-lookup"><span data-stu-id="83015-146">FactSet</span></span>

- <span data-ttu-id="83015-147">HipChat</span><span class="sxs-lookup"><span data-stu-id="83015-147">HipChat</span></span>

- <span data-ttu-id="83015-148">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="83015-148">InvestEdge</span></span>

- <span data-ttu-id="83015-149">LivePerson</span><span class="sxs-lookup"><span data-stu-id="83015-149">LivePerson</span></span>

- <span data-ttu-id="83015-150">Flux de données MessageLabs</span><span class="sxs-lookup"><span data-stu-id="83015-150">MessageLabs Data Streams</span></span>

- <span data-ttu-id="83015-151">OpenText</span><span class="sxs-lookup"><span data-stu-id="83015-151">OpenText</span></span>

- <span data-ttu-id="83015-152">Aide en direct « cliquer pour appeler » Oracle/ATG</span><span class="sxs-lookup"><span data-stu-id="83015-152">Oracle/ATG 'click-to-call' Live Help</span></span>

- <span data-ttu-id="83015-153">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="83015-153">Pivot IMTRADER</span></span>

- <span data-ttu-id="83015-154">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="83015-154">Microsoft SharePoint</span></span>

- <span data-ttu-id="83015-155">MindAlign</span><span class="sxs-lookup"><span data-stu-id="83015-155">MindAlign</span></span>

- <span data-ttu-id="83015-156">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="83015-156">Sitrion One (Newsgator)</span></span>

- <span data-ttu-id="83015-157">Skype Entreprise (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="83015-157">Skype for Business (Lync/OCS)</span></span>

- <span data-ttu-id="83015-158">Skype Entreprise Online (Lync Online)</span><span class="sxs-lookup"><span data-stu-id="83015-158">Skype for Business Online (Lync Online)</span></span>

- <span data-ttu-id="83015-159">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="83015-159">SQL Databases</span></span>

- <span data-ttu-id="83015-160">Squawker</span><span class="sxs-lookup"><span data-stu-id="83015-160">Squawker</span></span>

- <span data-ttu-id="83015-161">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="83015-161">Thomson Reuters Eikon Messenger</span></span>

### <a name="archivesocial"></a><span data-ttu-id="83015-162">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="83015-162">ArchiveSocial</span></span>

<span data-ttu-id="83015-163">[ArchiveSocial prend](https://www.archivesocial.com) en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-163">[ArchiveSocial](https://www.archivesocial.com) supports the following third-party data sources:</span></span>

- <span data-ttu-id="83015-164">Facebook</span><span class="sxs-lookup"><span data-stu-id="83015-164">Facebook</span></span>

- <span data-ttu-id="83015-165">Flickr</span><span class="sxs-lookup"><span data-stu-id="83015-165">Flickr</span></span>

- <span data-ttu-id="83015-166">Twitter</span><span class="sxs-lookup"><span data-stu-id="83015-166">Instagram</span></span>

- <span data-ttu-id="83015-167">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="83015-167">LinkedIn</span></span>

- <span data-ttu-id="83015-168">Pinterest</span><span class="sxs-lookup"><span data-stu-id="83015-168">Pinterest</span></span>

- <span data-ttu-id="83015-169">Twitter</span><span class="sxs-lookup"><span data-stu-id="83015-169">Twitter</span></span>

- <span data-ttu-id="83015-170">YouTube</span><span class="sxs-lookup"><span data-stu-id="83015-170">YouTube</span></span>

- <span data-ttu-id="83015-171">Vimeo</span><span class="sxs-lookup"><span data-stu-id="83015-171">Vimeo</span></span>

### <a name="veritas"></a><span data-ttu-id="83015-172">Veritas</span><span class="sxs-lookup"><span data-stu-id="83015-172">Veritas</span></span>

<span data-ttu-id="83015-173">[Veritas prend](https://www.globanet.com) en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-173">[Veritas](https://www.globanet.com) supports the following third-party data sources:</span></span>

- <span data-ttu-id="83015-174">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="83015-174">AOL with Pivot Client</span></span>

- <span data-ttu-id="83015-175">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-175">BlackBerry Call Logs (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-176">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-176">BlackBerry Messenger (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-177">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-177">BlackBerry PIN (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-178">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-178">BlackBerry SMS (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-179">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="83015-179">Bloomberg Chat</span></span>

- <span data-ttu-id="83015-180">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="83015-180">Bloomberg Mail</span></span>

- <span data-ttu-id="83015-181">Box</span><span class="sxs-lookup"><span data-stu-id="83015-181">Box</span></span>

- <span data-ttu-id="83015-182">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="83015-182">CipherCloud for Salesforce Chatter</span></span>

- <span data-ttu-id="83015-183">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="83015-183">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="83015-184">Cisco Webex Teams</span><span class="sxs-lookup"><span data-stu-id="83015-184">Cisco Webex Teams</span></span>

- <span data-ttu-id="83015-185">Citrix Workspace &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="83015-185">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="83015-186">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="83015-186">CrowdCompass</span></span>

- <span data-ttu-id="83015-187">Fichiers texte délimités par des personnalisés</span><span class="sxs-lookup"><span data-stu-id="83015-187">Custom-delimited text files</span></span>

- <span data-ttu-id="83015-188">Fichiers XML personnalisés</span><span class="sxs-lookup"><span data-stu-id="83015-188">Custom XML files</span></span>

- <span data-ttu-id="83015-189">Facebook (Pages)</span><span class="sxs-lookup"><span data-stu-id="83015-189">Facebook (Pages)</span></span>

- <span data-ttu-id="83015-190">Factset</span><span class="sxs-lookup"><span data-stu-id="83015-190">Factset</span></span>

- <span data-ttu-id="83015-191">FXConnect</span><span class="sxs-lookup"><span data-stu-id="83015-191">FXConnect</span></span>

- <span data-ttu-id="83015-192">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="83015-192">ICE Chat/YellowJacket</span></span>

- <span data-ttu-id="83015-193">Jive</span><span class="sxs-lookup"><span data-stu-id="83015-193">Jive</span></span>

- <span data-ttu-id="83015-194">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="83015-194">Macgregor XIP</span></span>

- <span data-ttu-id="83015-195">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="83015-195">Microsoft Exchange Server</span></span>

- <span data-ttu-id="83015-196">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="83015-196">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="83015-197">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="83015-197">Microsoft Teams</span></span>

- <span data-ttu-id="83015-198">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="83015-198">Microsoft Yammer</span></span>

- <span data-ttu-id="83015-199">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="83015-199">Mobile Guard</span></span>

- <span data-ttu-id="83015-200">Pivot</span><span class="sxs-lookup"><span data-stu-id="83015-200">Pivot</span></span>

- <span data-ttu-id="83015-201">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="83015-201">Salesforce Chatter</span></span>

- <span data-ttu-id="83015-202">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="83015-202">Skype for Business Online</span></span>

- <span data-ttu-id="83015-203">Skype Entreprise, versions 2007 R2-2016 (sur site)</span><span class="sxs-lookup"><span data-stu-id="83015-203">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>

- <span data-ttu-id="83015-204">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="83015-204">Slack Enterprise Grid</span></span>

- <span data-ttu-id="83015-205">Symphony</span><span class="sxs-lookup"><span data-stu-id="83015-205">Symphony</span></span>

- <span data-ttu-id="83015-206">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="83015-206">Thomson Reuters Eikon</span></span>

- <span data-ttu-id="83015-207">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="83015-207">Thomson Reuters Messenger</span></span>

- <span data-ttu-id="83015-208">Thomson Reuters Dealings 3000/FX Trading</span><span class="sxs-lookup"><span data-stu-id="83015-208">Thomson Reuters Dealings 3000 / FX Trading</span></span>

- <span data-ttu-id="83015-209">Twitter</span><span class="sxs-lookup"><span data-stu-id="83015-209">Twitter</span></span>

- <span data-ttu-id="83015-210">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="83015-210">UBS Chat</span></span>

- <span data-ttu-id="83015-211">YouTube</span><span class="sxs-lookup"><span data-stu-id="83015-211">YouTube</span></span>

### <a name="opentext"></a><span data-ttu-id="83015-212">OpenText</span><span class="sxs-lookup"><span data-stu-id="83015-212">OpenText</span></span>

<span data-ttu-id="83015-213">[OpenText prend](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-213">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span>

- <span data-ttu-id="83015-214">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="83015-214">Axs Encrypted</span></span>

- <span data-ttu-id="83015-215">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="83015-215">Axs Exchange</span></span>

- <span data-ttu-id="83015-216">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="83015-216">Axs Local Archive</span></span>

- <span data-ttu-id="83015-217">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="83015-217">Axs PlaceHolder</span></span>

- <span data-ttu-id="83015-218">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="83015-218">Axs Signed</span></span>

- <span data-ttu-id="83015-219">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="83015-219">Bloomberg</span></span>

- <span data-ttu-id="83015-220">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="83015-220">Thomson Reuters</span></span>

### <a name="smarsh"></a><span data-ttu-id="83015-221">Smarsh</span><span class="sxs-lookup"><span data-stu-id="83015-221">Smarsh</span></span>

<span data-ttu-id="83015-222">[Smarsh prend](https://www.smarsh.com) en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-222">[Smarsh](https://www.smarsh.com) supports the following third-party data sources:</span></span>

- <span data-ttu-id="83015-223">AIM</span><span class="sxs-lookup"><span data-stu-id="83015-223">AIM</span></span>

- <span data-ttu-id="83015-224">American Idol</span><span class="sxs-lookup"><span data-stu-id="83015-224">American Idol</span></span>

- <span data-ttu-id="83015-225">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="83015-225">Apple Juice</span></span>

- <span data-ttu-id="83015-226">AOL avec client Pivot</span><span class="sxs-lookup"><span data-stu-id="83015-226">AOL with Pivot client</span></span>

- <span data-ttu-id="83015-227">Ares</span><span class="sxs-lookup"><span data-stu-id="83015-227">Ares</span></span>

- <span data-ttu-id="83015-228">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="83015-228">Bazaar Voice</span></span>

- <span data-ttu-id="83015-229">Bear Share</span><span class="sxs-lookup"><span data-stu-id="83015-229">Bear Share</span></span>

- <span data-ttu-id="83015-230">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="83015-230">Bit Torrent</span></span>

- <span data-ttu-id="83015-231">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-231">BlackBerry Call Logs (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-232">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-232">BlackBerry Messenger (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-233">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-233">BlackBerry PIN (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-234">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="83015-234">BlackBerry SMS (v5, v10, v12)</span></span>

- <span data-ttu-id="83015-235">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="83015-235">Bloomberg Mail</span></span>

- <span data-ttu-id="83015-236">CellTrust</span><span class="sxs-lookup"><span data-stu-id="83015-236">CellTrust</span></span>

- <span data-ttu-id="83015-237">Chat Import</span><span class="sxs-lookup"><span data-stu-id="83015-237">Chat Import</span></span>

- <span data-ttu-id="83015-238">Chat Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="83015-238">Chat Real Time Logging and Policy</span></span>

- <span data-ttu-id="83015-239">Chatter</span><span class="sxs-lookup"><span data-stu-id="83015-239">Chatter</span></span>

- <span data-ttu-id="83015-240">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="83015-240">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>

- <span data-ttu-id="83015-241">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="83015-241">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>

- <span data-ttu-id="83015-242">Collaboration Import</span><span class="sxs-lookup"><span data-stu-id="83015-242">Collaboration Import</span></span>

- <span data-ttu-id="83015-243">Collaboration Real Time Logging</span><span class="sxs-lookup"><span data-stu-id="83015-243">Collaboration Real Time Logging</span></span>

- <span data-ttu-id="83015-244">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="83015-244">Direct Connect</span></span>

- <span data-ttu-id="83015-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="83015-245">Facebook</span></span>

- <span data-ttu-id="83015-246">FactSet</span><span class="sxs-lookup"><span data-stu-id="83015-246">FactSet</span></span>

- <span data-ttu-id="83015-247">FastTrack</span><span class="sxs-lookup"><span data-stu-id="83015-247">FastTrack</span></span>

- <span data-ttu-id="83015-248">Gnutella</span><span class="sxs-lookup"><span data-stu-id="83015-248">Gnutella</span></span>

- <span data-ttu-id="83015-249">Google+</span><span class="sxs-lookup"><span data-stu-id="83015-249">Google+</span></span>

- <span data-ttu-id="83015-250">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="83015-250">GoToMyPC</span></span>

- <span data-ttu-id="83015-251">Hopster</span><span class="sxs-lookup"><span data-stu-id="83015-251">Hopster</span></span>

- <span data-ttu-id="83015-252">HubConnex</span><span class="sxs-lookup"><span data-stu-id="83015-252">HubConnex</span></span>

- <span data-ttu-id="83015-253">IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)</span><span class="sxs-lookup"><span data-stu-id="83015-253">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>

- <span data-ttu-id="83015-254">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="83015-254">IBM Connections Chat Cloud</span></span>

- <span data-ttu-id="83015-255">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="83015-255">IBM Connections Social Cloud</span></span>

- <span data-ttu-id="83015-256">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="83015-256">IBM SameTime Advanced 8.5.2 IFR1</span></span>

- <span data-ttu-id="83015-257">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="83015-257">IBM SameTime Communicate 9.0</span></span>

- <span data-ttu-id="83015-258">IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)</span><span class="sxs-lookup"><span data-stu-id="83015-258">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>

- <span data-ttu-id="83015-259">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="83015-259">IBM SameTime Complete 9.0</span></span>

- <span data-ttu-id="83015-260">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="83015-260">IBM SameTime Conference 9.0</span></span>

- <span data-ttu-id="83015-261">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="83015-261">IBM SameTime Meeting 8.5.2 IFR1</span></span>

- <span data-ttu-id="83015-262">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="83015-262">ICE/YellowJacket</span></span>

- <span data-ttu-id="83015-263">IM Import</span><span class="sxs-lookup"><span data-stu-id="83015-263">IM Import</span></span>

- <span data-ttu-id="83015-264">IM Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="83015-264">IM Real Time Logging and Policy</span></span>

- <span data-ttu-id="83015-265">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="83015-265">Indii Messenger</span></span>

- <span data-ttu-id="83015-266">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="83015-266">Instant Bloomberg</span></span>

- <span data-ttu-id="83015-267">LASER</span><span class="sxs-lookup"><span data-stu-id="83015-267">IRC</span></span>

- <span data-ttu-id="83015-268">Jive</span><span class="sxs-lookup"><span data-stu-id="83015-268">Jive</span></span>

- <span data-ttu-id="83015-269">Jive 6 Real Time Logging (version 6, version 7)</span><span class="sxs-lookup"><span data-stu-id="83015-269">Jive 6 Real Time Logging (v6, v7)</span></span>

- <span data-ttu-id="83015-270">Jive Import</span><span class="sxs-lookup"><span data-stu-id="83015-270">Jive Import</span></span>

- <span data-ttu-id="83015-271">JXTA</span><span class="sxs-lookup"><span data-stu-id="83015-271">JXTA</span></span>

- <span data-ttu-id="83015-272">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="83015-272">LinkedIn</span></span>

- <span data-ttu-id="83015-273">Microsoft Lync (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="83015-273">Microsoft Lync (2010, 2013)</span></span>

- <span data-ttu-id="83015-274">MFTP</span><span class="sxs-lookup"><span data-stu-id="83015-274">MFTP</span></span>

- <span data-ttu-id="83015-275">Microsoft Lync 2013 Voix</span><span class="sxs-lookup"><span data-stu-id="83015-275">Microsoft Lync 2013 Voice</span></span>

- <span data-ttu-id="83015-276">Microsoft SharePoint (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="83015-276">Microsoft SharePoint (2010, 2013)</span></span>

- <span data-ttu-id="83015-277">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="83015-277">Microsoft SharePoint Online</span></span>

- <span data-ttu-id="83015-278">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="83015-278">Microsoft UC (Unified Communications)</span></span>

- <span data-ttu-id="83015-279">MindAlign</span><span class="sxs-lookup"><span data-stu-id="83015-279">MindAlign</span></span>

- <span data-ttu-id="83015-280">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="83015-280">Mobile Guard</span></span>

- <span data-ttu-id="83015-281">MSN</span><span class="sxs-lookup"><span data-stu-id="83015-281">MSN</span></span>

- <span data-ttu-id="83015-282">My Space</span><span class="sxs-lookup"><span data-stu-id="83015-282">My Space</span></span>

- <span data-ttu-id="83015-283">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="83015-283">NEONetwork</span></span>

- <span data-ttu-id="83015-284">Microsoft 365 Lync Dédié</span><span class="sxs-lookup"><span data-stu-id="83015-284">Microsoft 365 Lync Dedicated</span></span>

- <span data-ttu-id="83015-285">Microsoft 365 Messagerie instantanée partagée</span><span class="sxs-lookup"><span data-stu-id="83015-285">Microsoft 365 Shared IM</span></span>

- <span data-ttu-id="83015-286">Pinterest</span><span class="sxs-lookup"><span data-stu-id="83015-286">Pinterest</span></span>

- <span data-ttu-id="83015-287">Pivot</span><span class="sxs-lookup"><span data-stu-id="83015-287">Pivot</span></span>

- <span data-ttu-id="83015-288">QQ</span><span class="sxs-lookup"><span data-stu-id="83015-288">QQ</span></span>

- <span data-ttu-id="83015-289">Skype Entreprise 2015</span><span class="sxs-lookup"><span data-stu-id="83015-289">Skype for Business 2015</span></span>

- <span data-ttu-id="83015-290">SoftEther</span><span class="sxs-lookup"><span data-stu-id="83015-290">SoftEther</span></span>

- <span data-ttu-id="83015-291">Symphony</span><span class="sxs-lookup"><span data-stu-id="83015-291">Symphony</span></span>

- <span data-ttu-id="83015-292">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="83015-292">Thomson Reuters Eikon</span></span>

- <span data-ttu-id="83015-293">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="83015-293">Thomson Reuters Messenger</span></span>

- <span data-ttu-id="83015-294">Tor</span><span class="sxs-lookup"><span data-stu-id="83015-294">Tor</span></span>

- <span data-ttu-id="83015-295">TTT</span><span class="sxs-lookup"><span data-stu-id="83015-295">TTT</span></span>

- <span data-ttu-id="83015-296">Twitter</span><span class="sxs-lookup"><span data-stu-id="83015-296">Twitter</span></span>

- <span data-ttu-id="83015-297">WinMX</span><span class="sxs-lookup"><span data-stu-id="83015-297">WinMX</span></span>

- <span data-ttu-id="83015-298">Winny</span><span class="sxs-lookup"><span data-stu-id="83015-298">Winny</span></span>

- <span data-ttu-id="83015-299">Yahoo</span><span class="sxs-lookup"><span data-stu-id="83015-299">Yahoo</span></span>

- <span data-ttu-id="83015-300">Yammer</span><span class="sxs-lookup"><span data-stu-id="83015-300">Yammer</span></span>

- <span data-ttu-id="83015-301">YouTube</span><span class="sxs-lookup"><span data-stu-id="83015-301">YouTube</span></span>


### <a name="verba"></a><span data-ttu-id="83015-302">Verba</span><span class="sxs-lookup"><span data-stu-id="83015-302">Verba</span></span>

<span data-ttu-id="83015-303">[Verba prend](https://www.verba.com) en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-303">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span>

- <span data-ttu-id="83015-304">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="83015-304">Avaya Aura Video</span></span>

- <span data-ttu-id="83015-305">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="83015-305">Avaya Aura Voice</span></span>

- <span data-ttu-id="83015-306">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="83015-306">Avtec Radio</span></span>

- <span data-ttu-id="83015-307">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="83015-307">Bosch/Telex Radio</span></span>

- <span data-ttu-id="83015-308">BroadSoft Video</span><span class="sxs-lookup"><span data-stu-id="83015-308">BroadSoft Video</span></span>

- <span data-ttu-id="83015-309">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="83015-309">BroadSoft Voice</span></span>

- <span data-ttu-id="83015-310">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="83015-310">Centile Voice</span></span>

- <span data-ttu-id="83015-311">Cisco Jabber IM</span><span class="sxs-lookup"><span data-stu-id="83015-311">Cisco Jabber IM</span></span>

- <span data-ttu-id="83015-312">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="83015-312">Cisco UC Video</span></span>

- <span data-ttu-id="83015-313">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="83015-313">Cisco UC Voice</span></span>

- <span data-ttu-id="83015-314">Cisco UCCX/UCCE Video</span><span class="sxs-lookup"><span data-stu-id="83015-314">Cisco UCCX/UCCE Video</span></span>

- <span data-ttu-id="83015-315">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="83015-315">Cisco UCCX/UCCE Voice</span></span>

- <span data-ttu-id="83015-316">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="83015-316">ESChat Radio</span></span>

- <span data-ttu-id="83015-317">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="83015-317">Geoman Contact Expert</span></span>

- <span data-ttu-id="83015-318">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="83015-318">IP Trade Voice</span></span>

- <span data-ttu-id="83015-319">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="83015-319">Luware LUCS Contact Center</span></span>

- <span data-ttu-id="83015-320">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="83015-320">Microsoft UC (Unified Communications)</span></span>

- <span data-ttu-id="83015-321">Mitel MiContact Center for Lync (prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="83015-321">Mitel MiContact Center for Lync (prairieFyre)</span></span>

- <span data-ttu-id="83015-322">Oracle / Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="83015-322">Oracle / Acme Packet Session Border Controller Video</span></span>

- <span data-ttu-id="83015-323">Oracle / Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="83015-323">Oracle / Acme Packet Session Border Controller Voice</span></span>

- <span data-ttu-id="83015-324">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="83015-324">Singtel Mobile Voice</span></span>

- <span data-ttu-id="83015-325">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="83015-325">SIPREC Video</span></span>

-  <span data-ttu-id="83015-326">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="83015-326">SIPREC Voice</span></span>

- <span data-ttu-id="83015-327">Skype Entreprise / MI Lync</span><span class="sxs-lookup"><span data-stu-id="83015-327">Skype for Business / Lync IM</span></span>

- <span data-ttu-id="83015-328">Skype Entreprise / Vidéo Lync</span><span class="sxs-lookup"><span data-stu-id="83015-328">Skype for Business / Lync Video</span></span>

- <span data-ttu-id="83015-329">Skype Entreprise / Voix Lync</span><span class="sxs-lookup"><span data-stu-id="83015-329">Skype for Business / Lync Voice</span></span>

- <span data-ttu-id="83015-330">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="83015-330">Speakerbus Voice</span></span>

- <span data-ttu-id="83015-331">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="83015-331">Standard SIP/H.323 Video</span></span>

- <span data-ttu-id="83015-332">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="83015-332">Standard SIP/H.323 Voice</span></span>

- <span data-ttu-id="83015-333">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="83015-333">Truphone Voice</span></span>

- <span data-ttu-id="83015-334">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="83015-334">TwistedPair Radio</span></span>

- <span data-ttu-id="83015-335">Écran d’ordinateur de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="83015-335">Windows Desktop Computer Screen</span></span>

## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-microsoft-365"></a><span data-ttu-id="83015-336">Étape 2 : Créer et configurer une boîte aux lettres de données tierce dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="83015-336">Step 2: Create and configure a third-party data mailbox in Microsoft 365</span></span>

<span data-ttu-id="83015-337">Voici les étapes de création et de configuration d’une boîte aux lettres de données tierce pour l’importation de données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-337">Here are the steps for creating and configuring a third-party data mailbox for importing data to Microsoft 365.</span></span> <span data-ttu-id="83015-338">Comme indiqué précédemment, les éléments sont importés dans cette boîte aux lettres si le connecteur partenaire ne peut pas maser l’ID utilisateur de l’élément sur un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83015-338">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to a user account.</span></span>

 <span data-ttu-id="83015-339">**Effectuer ces tâches dans le Centre d’administration Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="83015-339">**Complete these tasks in the Microsoft 365 admin center**</span></span>

1. <span data-ttu-id="83015-340">Créez un compte d’utilisateur et attribuez-lui une licence Exchange Online Plan 2 ; voir [Ajouter des utilisateurs à Microsoft 365](../admin/add-users/add-users.md).</span><span class="sxs-lookup"><span data-stu-id="83015-340">Create a user account and assign it an Exchange Online Plan 2 license; see [Add users to Microsoft 365](../admin/add-users/add-users.md).</span></span> <span data-ttu-id="83015-341">Une licence Plan 2 est nécessaire pour placer la boîte aux lettres en conservation pour litige ou activer une boîte aux lettres d’archivage avec un quota de stockage illimité.</span><span class="sxs-lookup"><span data-stu-id="83015-341">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>

2. <span data-ttu-id="83015-342">Ajoutez le compte d’utilisateur pour la boîte aux lettres de données tierces au **rôle d’administrateur administrateur Exchange** dans Microsoft 365 ; voir [Attribuer des rôles d’administrateur dans Microsoft 365](../admin/add-users/assign-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="83015-342">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Microsoft 365; see [Assign admin roles in Microsoft 365](../admin/add-users/assign-admin-roles.md).</span></span>

    > [!TIP]
    > <span data-ttu-id="83015-p109">Notez les informations d’identification pour ce compte d’utilisateur. Vous devez les fournir à votre partenaire, comme décrit à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="83015-p109">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span>

 <span data-ttu-id="83015-345">**Effectuer ces tâches dans le centre d’administration Exchange de gestion**</span><span class="sxs-lookup"><span data-stu-id="83015-345">**Complete these tasks in the Exchange admin center**</span></span>

1. <span data-ttu-id="83015-346">Masquer la boîte aux lettres de données tierces dans le carnet d’adresses et les autres listes d’adresses de votre organisation ; voir [Gérer les boîtes aux lettres utilisateur.](/exchange/recipients-in-exchange-online/manage-user-mailboxes/manage-user-mailboxes)</span><span class="sxs-lookup"><span data-stu-id="83015-346">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](/exchange/recipients-in-exchange-online/manage-user-mailboxes/manage-user-mailboxes).</span></span> <span data-ttu-id="83015-347">Vous pouvez également exécuter la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="83015-347">Alternatively, you can run the following PowerShell command:</span></span>

    ```powershell
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="83015-348">Attribuez **l’autorisation FullAccess** à la boîte aux lettres de données tierce afin que les administrateurs ou les responsables de la mise en conformité peuvent ouvrir la boîte aux lettres de données tierces dans le client de bureau Outlook; voir [Gérer les autorisations pour les destinataires.](https://go.microsoft.com/fwlink/p/?LinkId=692104)</span><span class="sxs-lookup"><span data-stu-id="83015-348">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>

3. <span data-ttu-id="83015-349">Activez les fonctionnalités de conformité suivantes pour la boîte aux lettres de données tierces :</span><span class="sxs-lookup"><span data-stu-id="83015-349">Enable the following compliance-related features for the third-party data mailbox:</span></span>

    - <span data-ttu-id="83015-350">Activer la boîte aux lettres d’archivage ; voir [Activer les boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et Activer [l’archivage illimité.](enable-unlimited-archiving.md)</span><span class="sxs-lookup"><span data-stu-id="83015-350">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="83015-351">Cela vous permet de libérer de l’espace de stockage dans la boîte aux lettres principale en mettant en place une stratégie d’archivage qui déplace des éléments de données tiers vers la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="83015-351">This lets you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="83015-352">Vous disposez ainsi d’un espace de stockage illimité pour les données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-352">This provides you with unlimited storage for third-party data.</span></span>

    - <span data-ttu-id="83015-353">Placez la boîte aux lettres de données tierces en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="83015-353">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="83015-354">Vous pouvez également appliquer une stratégie Microsoft 365 rétention dans le centre de sécurité et conformité.</span><span class="sxs-lookup"><span data-stu-id="83015-354">You can also apply a Microsoft 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="83015-355">Le placement de cette boîte aux lettres en attente conserve les éléments de données tiers (indéfiniment ou pour une durée spécifiée) et les empêche d’être purgés de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="83015-355">Placing this mailbox on hold retains third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="83015-356">Consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-356">See one of the following topics:</span></span>

      - [<span data-ttu-id="83015-357">Placer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="83015-357">Place a mailbox on Litigation Hold</span></span>](./create-a-litigation-hold.md)

      - [<span data-ttu-id="83015-358">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="83015-358">Learn about retention policies and retention labels</span></span>](retention.md)

    - <span data-ttu-id="83015-359">Activer l’enregistrement d’audit de boîte aux lettres pour l’accès propriétaire, délégué et administrateur à la boîte aux lettres de données tierces ; voir [Activer l’audit de boîte aux lettres.](enable-mailbox-auditing.md)</span><span class="sxs-lookup"><span data-stu-id="83015-359">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="83015-360">Cela vous permet d’auditer toutes les activités effectuées par tout utilisateur ayant accès à la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-360">This allows you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="83015-361">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="83015-361">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="83015-362">L’étape suivante consiste à configurer les boîtes aux lettres des utilisateurs pour prendre en charge les données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-362">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="83015-363">Effectuer ces tâches à l’aide Exchange centre d’administration ou à l’aide des cmdlets Windows PowerShell correspondantes.</span><span class="sxs-lookup"><span data-stu-id="83015-363">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>

1. <span data-ttu-id="83015-364">Activer la boîte aux lettres d’archivage pour chaque utilisateur ; voir [Activer les boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et Activer [l’archivage illimité.](enable-unlimited-archiving.md)</span><span class="sxs-lookup"><span data-stu-id="83015-364">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>

2. <span data-ttu-id="83015-365">Placer les boîtes aux lettres des utilisateurs en conservation pour litige ou appliquer une stratégie Microsoft 365 rétention ; consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-365">Place user mailboxes on Litigation Hold or apply a Microsoft 365 retention policy; see one of the following topics:</span></span>

    - [<span data-ttu-id="83015-366">Placer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="83015-366">Place a mailbox on Litigation Hold</span></span>](./create-a-litigation-hold.md)

    - [<span data-ttu-id="83015-367">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="83015-367">Learn about retention policies and retention labels</span></span>](retention.md)

    <span data-ttu-id="83015-368">Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="83015-368">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="83015-369">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="83015-369">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="83015-370">La dernière étape consiste à fournir à votre partenaire les informations suivantes afin qu’il puisse configurer le connecteur pour qu’il se connecte à votre organisation afin d’importer des données dans les boîtes aux lettres des utilisateurs et dans la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-370">The final step is to provide your partner with the following information so they can configure the connector to connect to your organization to import data to user mailboxes and to the third-party data mailbox.</span></span>

- <span data-ttu-id="83015-371">Point de terminaison utilisé pour se connecter au service Azure dans Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="83015-371">The endpoint used to connect to the Azure service in Microsoft 365:</span></span>

    ```http
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="83015-372">Informations d’identification de connexion (Microsoft 365'utilisateur et mot de passe) de la boîte aux lettres de données tierces que vous avez créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="83015-372">The sign-in credentials (Microsoft 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="83015-373">Ces informations d’identification sont requises pour que le connecteur partenaire puisse accéder aux éléments et les importer dans les boîtes aux lettres utilisateur et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-373">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>

## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="83015-374">Étape 5 : Inscrire le connecteur de données tiers dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="83015-374">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="83015-375">À compter du 30 septembre 2018, le service Azure dans Microsoft 365 commence à utiliser l’authentification moderne dans Exchange Online pour authentifier les connecteurs de données tiers qui tentent de se connecter à votre organisation pour importer des données.</span><span class="sxs-lookup"><span data-stu-id="83015-375">Starting September 30, 2018, the Azure service in Microsoft 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your organization to import data.</span></span> <span data-ttu-id="83015-376">La raison de ce changement est que l’authentification moderne offre une sécurité plus renforcée que la méthode actuelle, qui était basée sur une liste d’applications pour les connecteurs tiers qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.</span><span class="sxs-lookup"><span data-stu-id="83015-376">The reason for this change is that modern authentication provides more security than the current method, which was based on an allow list for third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="83015-377">Pour permettre à un connecteur de données tiers de se connecter à Microsoft 365 à l’aide de la nouvelle méthode d’authentification moderne, un administrateur de votre organisation doit consentir à inscrire le connecteur en tant qu’application de service approuvé dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83015-377">To enable a third-party data connector to connect to Microsoft 365 using the new modern authentication method, an administrator in your organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="83015-378">Pour ce faire, acceptez une demande d’autorisation pour autoriser le connecteur à accéder aux données de votre organisation dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83015-378">This is done by accepting a permission request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="83015-379">Une fois que vous avez accepté cette demande, le connecteur de données tiers est ajouté en tant qu’application d’entreprise Azure Active Directory et représenté en tant que principal de service.</span><span class="sxs-lookup"><span data-stu-id="83015-379">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="83015-380">Pour plus d’informations sur le processus de consentement, voir [Consentement de l’administrateur client.](/skype-sdk/trusted-application-api/docs/tenantadminconsent)</span><span class="sxs-lookup"><span data-stu-id="83015-380">For more information the consent process, see  [Tenant Admin Consent](/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="83015-381">Voici les étapes à suivre pour accéder à la demande d’inscription du connecteur et l’accepter :</span><span class="sxs-lookup"><span data-stu-id="83015-381">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="83015-382">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of a global administrator.</span><span class="sxs-lookup"><span data-stu-id="83015-382">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of a global administrator.</span></span>

   <span data-ttu-id="83015-383">La boîte de dialogue suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="83015-383">The following dialog box is displayed.</span></span> <span data-ttu-id="83015-384">Vous pouvez développer les conseils pour passer en revue les autorisations qui seront attribuées au connecteur.</span><span class="sxs-lookup"><span data-stu-id="83015-384">You can expand the carets to review the permissions that will be assigned to the connector.</span></span>

   ![La boîte de dialogue de demande d’autorisations s’affiche](../media/O365-ThirdPartyDataConnector-OptIn1.png)

2. <span data-ttu-id="83015-386">Cliquez sur **Accept (Accepter)**.</span><span class="sxs-lookup"><span data-stu-id="83015-386">Click **Accept**.</span></span>

<span data-ttu-id="83015-387">Une fois la demande acceptée, le [portail Azure](https://portal.azure.com) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="83015-387">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="83015-388">Pour afficher la liste des applications de votre organisation, cliquez **sur Azure Active Directory**  >  **Enterprise applications.**</span><span class="sxs-lookup"><span data-stu-id="83015-388">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="83015-389">Le Microsoft 365 de données tiers est répertorié dans le **Enterprise applications.**</span><span class="sxs-lookup"><span data-stu-id="83015-389">The Microsoft 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83015-390">Après le 30 septembre 2018, les données tierces ne seront plus importées dans les boîtes aux lettres de votre organisation si vous n’inscrivez pas de connecteur de données tiers dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83015-390">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="83015-391">Notez que les connecteurs de données tiers existants (ceux créés avant le 30 septembre 2018) doivent également être enregistrés dans Azure Active Directory en suivant la procédure de l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="83015-391">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="83015-392">Révocation du consentement pour un connecteur de données tiers</span><span class="sxs-lookup"><span data-stu-id="83015-392">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="83015-393">Une fois que votre organisation a accepté la demande d’autorisations pour inscrire un connecteur de données tiers dans Azure Active Directory, votre organisation peut révoquer ce consentement à tout moment.</span><span class="sxs-lookup"><span data-stu-id="83015-393">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="83015-394">Toutefois, la révocation du consentement pour un connecteur signifie que les données de la source de données tierces ne seront plus importées dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-394">However, revoking the consent for a connector means that data from the third-party data source will no longer be imported into Microsoft 365.</span></span>

<span data-ttu-id="83015-395">Pour révoquer le consentement d’un connecteur de données tiers, vous pouvez supprimer l’application (en supprimant le principal de service correspondant) de Azure Active Directory à l’aide du portail **d’applications Enterprise** dans le portail Azure ou à l’aide de [Remove-MsolServicePrincipal](/powershell/module/msonline/remove-msolserviceprincipal) dans Microsoft 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83015-395">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](/powershell/module/msonline/remove-msolserviceprincipal) in Microsoft 365 PowerShell.</span></span> <span data-ttu-id="83015-396">Vous pouvez également utiliser [l’cmdlet Remove-AzureADServicePrincipal](/powershell/module/azuread/remove-azureadserviceprincipal) dans Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83015-396">You can also use the [Remove-AzureADServicePrincipal](/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>

## <a name="more-information"></a><span data-ttu-id="83015-397">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="83015-397">More information</span></span>

- <span data-ttu-id="83015-398">Comme indiqué précédemment, les éléments des sources de données tierces sont importés vers les boîtes aux lettres Exchange en tant que messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="83015-398">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="83015-399">Le connecteur partenaire importe l’élément à l’aide d’un schéma requis par Microsoft 365 API.</span><span class="sxs-lookup"><span data-stu-id="83015-399">The partner connector imports the item using a schema required by the Microsoft 365 API.</span></span> <span data-ttu-id="83015-400">Le tableau suivant décrit les propriétés de message d’un élément d’une source de données tierces après son importation vers une boîte aux lettres Exchange en tant que message électronique.</span><span class="sxs-lookup"><span data-stu-id="83015-400">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="83015-401">Le tableau indique également si la propriété de message est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="83015-401">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="83015-402">Les propriétés obligatoires doivent être renseignées.</span><span class="sxs-lookup"><span data-stu-id="83015-402">Mandatory properties must be populated.</span></span> <span data-ttu-id="83015-403">Si une propriété obligatoire est manquante, un élément n’est pas importé dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-403">If an item is missing a mandatory property, it won't be imported to Microsoft 365.</span></span> <span data-ttu-id="83015-404">Le processus d’importation renvoie un message d’erreur expliquant pourquoi un élément n’a pas été importé et quelle propriété est manquante.</span><span class="sxs-lookup"><span data-stu-id="83015-404">The import process returns an error message explaining why an item wasn't imported and which property is missing.</span></span><br/><br/>

    |<span data-ttu-id="83015-405">**Propriété de message**</span><span class="sxs-lookup"><span data-stu-id="83015-405">**Message property**</span></span>|<span data-ttu-id="83015-406">**Obligatoire ?**</span><span class="sxs-lookup"><span data-stu-id="83015-406">**Mandatory?**</span></span>|<span data-ttu-id="83015-407">**Description**</span><span class="sxs-lookup"><span data-stu-id="83015-407">**Description**</span></span>|<span data-ttu-id="83015-408">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="83015-408">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="83015-409">**FROM**</span><span class="sxs-lookup"><span data-stu-id="83015-409">**FROM**</span></span> <br/> |<span data-ttu-id="83015-410">Oui</span><span class="sxs-lookup"><span data-stu-id="83015-410">Yes</span></span>  <br/> |<span data-ttu-id="83015-411">Utilisateur qui a initialement créé ou envoyé l’élément dans la source de données tierces.</span><span class="sxs-lookup"><span data-stu-id="83015-411">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="83015-412">Le connecteur partenaire tente de ma cartographier l’ID utilisateur de l’élément source (par exemple, un handle Twitter) à un compte d’utilisateur pour tous les participants (utilisateurs dans les champs FROM et TO).</span><span class="sxs-lookup"><span data-stu-id="83015-412">The partner connector attempts to map the user ID from the source item (for example a Twitter handle) to a user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="83015-413">Une copie du message sera importée dans la boîte aux lettres de chaque participant.</span><span class="sxs-lookup"><span data-stu-id="83015-413">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="83015-414">Si aucun des participants de l’élément ne peut être mappé à un compte d’utilisateur, l’élément est importé dans la boîte aux lettres d’archivage tierce dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83015-414">If none of the participants from the item can be mapped to a user account, the item will be imported to the third-party archiving mailbox in Microsoft 365.</span></span>  <br/> <br/> <span data-ttu-id="83015-415">Le participant identifié comme expéditeur de l’élément doit avoir une boîte aux lettres active dans l’organisation dans qui l’élément est importé.</span><span class="sxs-lookup"><span data-stu-id="83015-415">The participant who's identified as the sender of the item must have an active mailbox in the organization that the item is being imported to.</span></span> <span data-ttu-id="83015-416">Si l’expéditeur ne dispose pas d’une boîte aux lettres active, l’erreur suivante est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="83015-416">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="83015-417">**TO**</span><span class="sxs-lookup"><span data-stu-id="83015-417">**TO**</span></span> <br/> |<span data-ttu-id="83015-418">Oui</span><span class="sxs-lookup"><span data-stu-id="83015-418">Yes</span></span>  <br/> |<span data-ttu-id="83015-419">Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="83015-419">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="83015-420">**Objet**</span><span class="sxs-lookup"><span data-stu-id="83015-420">**SUBJECT**</span></span> <br/> |<span data-ttu-id="83015-421">Non</span><span class="sxs-lookup"><span data-stu-id="83015-421">No</span></span>  <br/> |<span data-ttu-id="83015-422">Objet de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="83015-422">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="83015-423">**DATE**</span><span class="sxs-lookup"><span data-stu-id="83015-423">**DATE**</span></span> <br/> |<span data-ttu-id="83015-424">Oui</span><span class="sxs-lookup"><span data-stu-id="83015-424">Yes</span></span>  <br/> |<span data-ttu-id="83015-425">Date à laquelle l’élément a été initialement créé ou publié dans la source de données client.</span><span class="sxs-lookup"><span data-stu-id="83015-425">The date the item was originally created or posted in the customer data source.</span></span> <span data-ttu-id="83015-426">Par exemple, date à laquelle un message Twitter a été tweeté.</span><span class="sxs-lookup"><span data-stu-id="83015-426">For example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="83015-427">**BODY**</span><span class="sxs-lookup"><span data-stu-id="83015-427">**BODY**</span></span> <br/> |<span data-ttu-id="83015-428">Non</span><span class="sxs-lookup"><span data-stu-id="83015-428">No</span></span>  <br/> |<span data-ttu-id="83015-429">Contenu du message ou de la publication.</span><span class="sxs-lookup"><span data-stu-id="83015-429">The contents of the message or post.</span></span> <span data-ttu-id="83015-430">Pour certaines sources de données, le contenu de cette propriété peut être identique au contenu de la propriété **SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="83015-430">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="83015-431">Pendant le processus d’importation, le connecteur partenaire tente de maintenir une fidélité totale à partir de la source de contenu autant que possible.</span><span class="sxs-lookup"><span data-stu-id="83015-431">During the import process, the partner connector attempts to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="83015-432">Si possible, les fichiers, les graphiques ou tout autre contenu du corps de l’élément source sont inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="83015-432">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="83015-433">Sinon, le contenu de l’élément source est inclus dans la propriété **ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="83015-433">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="83015-434">Le contenu de cette propriété dépend du connecteur partenaire et de la fonctionnalité de la plateforme source.</span><span class="sxs-lookup"><span data-stu-id="83015-434">The contents of this property depends on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="83015-435">**PIÈCE JOINTE**</span><span class="sxs-lookup"><span data-stu-id="83015-435">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="83015-436">Non</span><span class="sxs-lookup"><span data-stu-id="83015-436">No</span></span>  <br/> |<span data-ttu-id="83015-437">Si un élément de la source de données (tel qu’un tweet dans Twitter ou une conversation par messagerie instantanée) possède un fichier joint ou inclut des images, le partenaire de connexion tente d’abord d’inclure des pièces jointes dans la propriété **BODY.**</span><span class="sxs-lookup"><span data-stu-id="83015-437">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="83015-438">Si ce n’est pas possible, il est ajouté à la propriété \*\* ATTACHMENT \*\*.</span><span class="sxs-lookup"><span data-stu-id="83015-438">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="83015-439">Voici d’autres exemples de pièces jointes : mentions J’aime sur Facebook, métadonnées de la source de contenu et réponses à un message ou une publication.</span><span class="sxs-lookup"><span data-stu-id="83015-439">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |<span data-ttu-id="83015-440">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="83015-440">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="83015-441">Oui</span><span class="sxs-lookup"><span data-stu-id="83015-441">Yes</span></span>  <br/> | <span data-ttu-id="83015-442">Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par le connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="83015-442">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="83015-443">Le format de cette propriété est  `IPM.NOTE.Source.Event` .</span><span class="sxs-lookup"><span data-stu-id="83015-443">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="83015-444">(Cette propriété doit commencer par  `IPM.NOTE` .</span><span class="sxs-lookup"><span data-stu-id="83015-444">(This property must begin with  `IPM.NOTE`.</span></span> <span data-ttu-id="83015-445">Ce format est similaire à celui de la classe  `IPM.NOTE.X` de message.) Cette propriété inclut les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="83015-445">This format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/><span data-ttu-id="83015-446">`Source`: indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="83015-446">`Source`: Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="83015-447">`Event`: indique le type d’activité effectuée dans la source de données tierce qui a produit les éléments ; par exemple, un tweet sur Twitter ou un billet sur Facebook.</span><span class="sxs-lookup"><span data-stu-id="83015-447">`Event`: Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="83015-448">Les événements sont propres à la source de données.</span><span class="sxs-lookup"><span data-stu-id="83015-448">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="83015-449">L’un des objectifs de cette propriété est de filtrer des éléments spécifiques en fonction de la source de données d’origine d’un élément ou en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="83015-449">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="83015-450">Par exemple, lors d’une recherche de découverte électronique, vous pouvez créer une requête de recherche afin de trouver tous les tweets qui ont été publiés par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="83015-450">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |

- <span data-ttu-id="83015-451">Lorsque des éléments sont correctement importés dans les boîtes aux lettres dans Microsoft 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="83015-451">When items are successfully imported to mailboxes in Microsoft 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="83015-452">Cet identificateur, appelé , peut être utilisé à des fins de dépannage ultérieure par les partenaires pour le suivi de bout en  `x-IngestionCorrelationID` bout des éléments.</span><span class="sxs-lookup"><span data-stu-id="83015-452">This identifier, called  `x-IngestionCorrelationID`, can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="83015-453">Nous recommandons que vos partenaires récupèrent ces informations et les conservent de leur côté.</span><span class="sxs-lookup"><span data-stu-id="83015-453">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="83015-454">Voici un exemple d’une réponse HTTP avec cet identifiant :</span><span class="sxs-lookup"><span data-stu-id="83015-454">Here's an example of an HTTP response showing this identifier:</span></span>

    ```http
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT
    ```

- <span data-ttu-id="83015-455">Vous pouvez utiliser l’outil de recherche de contenu dans le centre de sécurité et conformité pour rechercher des éléments qui ont été importés dans des boîtes aux lettres à partir d’une source de données tierce.</span><span class="sxs-lookup"><span data-stu-id="83015-455">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes from a third-party data source.</span></span> <span data-ttu-id="83015-456">Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires propriété-valeur de message suivantes dans la zone de mot clé pour une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="83015-456">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>

  - <span data-ttu-id="83015-457">**`kind:externaldata`**: Utilisez cette paire propriété-valeur pour rechercher tous les types de données tiers.</span><span class="sxs-lookup"><span data-stu-id="83015-457">**`kind:externaldata`**: Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="83015-458">Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et qui contenaient le mot « contoso » dans la propriété Subject de l’élément importé, utilisez la requête de mot clé  `kind:externaldata AND subject:contoso` .</span><span class="sxs-lookup"><span data-stu-id="83015-458">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>

  - <span data-ttu-id="83015-459">**`itemclass:ipm.externaldata.<third-party data type>`**: Utilisez cette paire propriété-valeur pour rechercher uniquement un type de données tierces spécifié.</span><span class="sxs-lookup"><span data-stu-id="83015-459">**`itemclass:ipm.externaldata.<third-party data type>`**: Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="83015-460">Par exemple, pour rechercher uniquement les données Facebook qui contiennent le mot « contoso » dans la propriété Subject, utilisez la requête de mot  `itemclass:ipm.externaldata.Facebook* AND subject:contoso` clé.</span><span class="sxs-lookup"><span data-stu-id="83015-460">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span>

  <span data-ttu-id="83015-461">Pour obtenir la liste complète des valeurs à utiliser pour les types de données tiers pour la propriété, voir Utiliser la recherche de contenu pour rechercher des données tierces importées dans `itemclass` [Microsoft 365](use-content-search-to-search-third-party-data-that-was-imported.md).</span><span class="sxs-lookup"><span data-stu-id="83015-461">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Microsoft 365](use-content-search-to-search-third-party-data-that-was-imported.md).</span></span>

   <span data-ttu-id="83015-462">Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :</span><span class="sxs-lookup"><span data-stu-id="83015-462">For more information about using Content Search and creating keyword search queries, see:</span></span>

  - [<span data-ttu-id="83015-463">Recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="83015-463">Content Search</span></span>](content-search.md)

  - [<span data-ttu-id="83015-464">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="83015-464">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)