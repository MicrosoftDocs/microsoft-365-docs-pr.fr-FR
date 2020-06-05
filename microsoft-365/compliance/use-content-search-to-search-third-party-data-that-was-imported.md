---
title: Utiliser la recherche de contenu pour rechercher des données importées tierces
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Utiliser l’outil eDiscovery de recherche de contenu pour rechercher des éléments importés dans des boîtes aux lettres dans Microsoft 365 à partir d’une source de données tierce. Vous pouvez créer une requête pour rechercher tous les éléments importés ou créer une requête pour rechercher des types de données tiers spécifiques. Cet article répertorie les valeurs que vous pouvez utiliser dans une requête de mot clé pour rechercher les types de données tiers que vous pouvez importer vers Microsoft 365.
ms.openlocfilehash: ab693ff8e2283e201b9d573e68f4bdfb9f859749
ms.sourcegitcommit: e6e704cbd9a50fc7db1e6a0cf5d3f8c6cbb94363
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2020
ms.locfileid: "44564967"
---
# <a name="use-content-search-to-search-third-party-data-imported-by-a-custom-partner-connector"></a><span data-ttu-id="4e54c-105">Utiliser la recherche de contenu pour rechercher des données tierces importées par un connecteur de partenaire personnalisé</span><span class="sxs-lookup"><span data-stu-id="4e54c-105">Use Content Search to search third-party data imported by a custom partner connector</span></span>

<span data-ttu-id="4e54c-106">Vous pouvez utiliser l' [outil eDiscovery](content-search.md) de la recherche de contenu dans le centre de sécurité & conformité pour rechercher des éléments importés dans des boîtes aux lettres dans Microsoft 365 à partir d’une source de données tierce.</span><span class="sxs-lookup"><span data-stu-id="4e54c-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items imported to mailboxes in Microsoft 365 from a third-party data source.</span></span> <span data-ttu-id="4e54c-107">Vous pouvez créer une requête pour rechercher tous les éléments de données tiers importés ou créer une requête pour rechercher des éléments de données tiers spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4e54c-107">You can create a query to search all imported third-party data items or you can create a query to search specific third-party data items.</span></span> <span data-ttu-id="4e54c-108">Par ailleurs, vous pouvez également créer une stratégie de rétention basée sur une requête ou une conservation eDiscovery basée sur une requête pour conserver les données tierces.</span><span class="sxs-lookup"><span data-stu-id="4e54c-108">Also, you can also create a query-based retention policy or a query-based eDiscovery hold to preserve third-party data.</span></span>
  
<span data-ttu-id="4e54c-109">Pour plus d’informations sur l’utilisation d’un partenaire pour importer des données tierces et la liste des types de données tierces que vous pouvez importer vers Microsoft 365, consultez [collaborer avec un partenaire pour archiver des données tierces dans Office 365](work-with-partner-to-archive-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="4e54c-109">For more information about working with a partner to import third-party data and a list of the third-party data types that you can import to Microsoft 365, see [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e54c-110">Les instructions de cet article s’appliquent uniquement aux données tierces qui ont été importées par un connecteur de partenaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4e54c-110">The guidance in this article only applies to third-party data that was imported by a custom partner connector.</span></span> <span data-ttu-id="4e54c-111">Cet article ne s’applique pas aux données tierces importées à l’aide des [connecteurs de données tiers](archiving-third-party-data.md#third-party-data-connectors) dans le centre de conformité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e54c-111">This article doesn't apply to third-party data that is imported by using the [third-party data connectors](archiving-third-party-data.md#third-party-data-connectors) in the Microsoft compliance center.</span></span>
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="4e54c-112">Création d’une requête pour rechercher toutes les données tierces</span><span class="sxs-lookup"><span data-stu-id="4e54c-112">Creating a query to search all third-party data</span></span>

<span data-ttu-id="4e54c-113">Pour rechercher (ou mettre en attente) tout type de données tierces que vous avez importées dans Office 365, vous pouvez utiliser la `kind:externaldata` paire message-valeur de la zone de mot clé pour une recherche de contenu ou lors de la création d’une conservation basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="4e54c-113">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="4e54c-114">Par exemple, pour rechercher des éléments importés à partir d’une source de données tierce et qui contiennent le mot « Contoso » dans la propriété Subject de l’élément importé, utilisez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="4e54c-114">For example, to search for items imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```powershell
kind:externaldata AND subject:contoso
```

<span data-ttu-id="4e54c-115">L’exemple de requête de mot clé précédent inclut la propriété Subject.</span><span class="sxs-lookup"><span data-stu-id="4e54c-115">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="4e54c-116">Pour obtenir la liste des autres propriétés des éléments de données tierces pouvant être inclus dans une requête de mot-clé, voir la section « plus d’informations » dans [utilisation d’un partenaire pour archiver des données tierces dans Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="4e54c-116">For a list of other properties for third-party data items that can include in a keyword query, see the "More information" section in [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="4e54c-117">Lors de la création de requêtes de recherche et de conservation de données tierces, vous pouvez également utiliser des conditions pour affiner les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="4e54c-117">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="4e54c-118">Pour plus d’informations sur la création de requêtes de recherche de contenu, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="4e54c-118">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="4e54c-119">Création d’une requête pour rechercher des types spécifiques de données tierces</span><span class="sxs-lookup"><span data-stu-id="4e54c-119">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="4e54c-120">Au lieu de rechercher tous les types de données tierces, vous pouvez créer des requêtes qui recherchent uniquement un type précis de données tierces à l’aide de la paire de valeur de la *propriété* de message suivante dans la zone de mot clé pour une recherche de contenu :</span><span class="sxs-lookup"><span data-stu-id="4e54c-120">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message *property:value* pair in the keyword box for a Content Search:</span></span>
  
```powershell
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="4e54c-121">Par exemple, pour rechercher des données Facebook qui contiennent le mot « Contoso » dans la propriété Subject, vous devez utiliser la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="4e54c-121">For example, to search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```powershell
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="4e54c-122">Le tableau suivant répertorie les types de données tiers que vous pouvez rechercher et la valeur à utiliser pour la `itemclass:` propriété message afin de Rechercher spécifiquement ce type de données tierces.</span><span class="sxs-lookup"><span data-stu-id="4e54c-122">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="4e54c-123">La syntaxe de la requête ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="4e54c-123">The query syntax isn't case-sensitive.</span></span> 
  
|<span data-ttu-id="4e54c-124">**Type de données tiers**</span><span class="sxs-lookup"><span data-stu-id="4e54c-124">**Third-party data type**</span></span>|<span data-ttu-id="4e54c-125">**Valeur de la `itemclass:` propriété**</span><span class="sxs-lookup"><span data-stu-id="4e54c-125">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e54c-126">VISERA</span><span class="sxs-lookup"><span data-stu-id="4e54c-126">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="4e54c-127">American Idol</span><span class="sxs-lookup"><span data-stu-id="4e54c-127">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="4e54c-128">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="4e54c-128">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="4e54c-129">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="4e54c-129">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="4e54c-130">Tréma</span><span class="sxs-lookup"><span data-stu-id="4e54c-130">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="4e54c-131">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="4e54c-131">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="4e54c-132">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="4e54c-132">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="4e54c-133">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="4e54c-133">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="4e54c-134">Espace réservé ax</span><span class="sxs-lookup"><span data-stu-id="4e54c-134">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="4e54c-135">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="4e54c-135">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="4e54c-136">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="4e54c-136">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="4e54c-137">BearShare</span><span class="sxs-lookup"><span data-stu-id="4e54c-137">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="4e54c-138">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="4e54c-138">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="4e54c-139">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="4e54c-139">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="4e54c-140">Journaux d’appels BlackBerry</span><span class="sxs-lookup"><span data-stu-id="4e54c-140">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="4e54c-141">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="4e54c-141">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="4e54c-142">Code confidentiel BlackBerry</span><span class="sxs-lookup"><span data-stu-id="4e54c-142">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="4e54c-143">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="4e54c-143">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="4e54c-144">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="4e54c-144">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="4e54c-145">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="4e54c-145">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="4e54c-146">Messages Bloomberg</span><span class="sxs-lookup"><span data-stu-id="4e54c-146">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="4e54c-147">Box</span><span class="sxs-lookup"><span data-stu-id="4e54c-147">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="4e54c-148">Serveur de présence de messagerie instantanée Cisco &amp;</span><span class="sxs-lookup"><span data-stu-id="4e54c-148">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="4e54c-149">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="4e54c-149">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="4e54c-150">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="4e54c-150">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="4e54c-151">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="4e54c-151">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="4e54c-152">Facebook</span><span class="sxs-lookup"><span data-stu-id="4e54c-152">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="4e54c-153">FastTrack</span><span class="sxs-lookup"><span data-stu-id="4e54c-153">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="4e54c-154">FXConnect</span><span class="sxs-lookup"><span data-stu-id="4e54c-154">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="4e54c-155">Flickr</span><span class="sxs-lookup"><span data-stu-id="4e54c-155">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="4e54c-156">Gnutella</span><span class="sxs-lookup"><span data-stu-id="4e54c-156">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="4e54c-157">Google +</span><span class="sxs-lookup"><span data-stu-id="4e54c-157">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="4e54c-158">Google Talk</span><span class="sxs-lookup"><span data-stu-id="4e54c-158">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="4e54c-159">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="4e54c-159">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="4e54c-160">HipChat</span><span class="sxs-lookup"><span data-stu-id="4e54c-160">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="4e54c-161">Hopster</span><span class="sxs-lookup"><span data-stu-id="4e54c-161">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="4e54c-162">HubConnex</span><span class="sxs-lookup"><span data-stu-id="4e54c-162">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="4e54c-163">Connexions IBM</span><span class="sxs-lookup"><span data-stu-id="4e54c-163">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="4e54c-164">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="4e54c-164">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="4e54c-165">Conversation ICE</span><span class="sxs-lookup"><span data-stu-id="4e54c-165">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="4e54c-166">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="4e54c-166">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="4e54c-167">Instagram</span><span class="sxs-lookup"><span data-stu-id="4e54c-167">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="4e54c-168">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="4e54c-168">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="4e54c-169">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="4e54c-169">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="4e54c-170">SALLE</span><span class="sxs-lookup"><span data-stu-id="4e54c-170">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="4e54c-171">Jive</span><span class="sxs-lookup"><span data-stu-id="4e54c-171">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="4e54c-172">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="4e54c-172">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="4e54c-173">JXTA</span><span class="sxs-lookup"><span data-stu-id="4e54c-173">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="4e54c-174">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4e54c-174">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="4e54c-175">MFTP</span><span class="sxs-lookup"><span data-stu-id="4e54c-175">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="4e54c-176">UC Microsoft</span><span class="sxs-lookup"><span data-stu-id="4e54c-176">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="4e54c-177">Correspondance des idées</span><span class="sxs-lookup"><span data-stu-id="4e54c-177">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="4e54c-178">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="4e54c-178">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="4e54c-179">SYMPATICO</span><span class="sxs-lookup"><span data-stu-id="4e54c-179">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="4e54c-180">MySpace</span><span class="sxs-lookup"><span data-stu-id="4e54c-180">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="4e54c-181">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="4e54c-181">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="4e54c-182">OpenNap</span><span class="sxs-lookup"><span data-stu-id="4e54c-182">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="4e54c-183">Pinterest</span><span class="sxs-lookup"><span data-stu-id="4e54c-183">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="4e54c-184">Pivot</span><span class="sxs-lookup"><span data-stu-id="4e54c-184">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="4e54c-185">QQ</span><span class="sxs-lookup"><span data-stu-id="4e54c-185">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="4e54c-186">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="4e54c-186">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="4e54c-187">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="4e54c-187">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="4e54c-188">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="4e54c-188">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="4e54c-189">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="4e54c-189">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="4e54c-190">SoftEther</span><span class="sxs-lookup"><span data-stu-id="4e54c-190">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="4e54c-191">Squawker</span><span class="sxs-lookup"><span data-stu-id="4e54c-191">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="4e54c-192">Concert</span><span class="sxs-lookup"><span data-stu-id="4e54c-192">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="4e54c-193">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="4e54c-193">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="4e54c-194">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="4e54c-194">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="4e54c-195">Termes</span><span class="sxs-lookup"><span data-stu-id="4e54c-195">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="4e54c-196">TTT</span><span class="sxs-lookup"><span data-stu-id="4e54c-196">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="4e54c-197">Twitter</span><span class="sxs-lookup"><span data-stu-id="4e54c-197">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="4e54c-198">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="4e54c-198">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="4e54c-199">Vimeo</span><span class="sxs-lookup"><span data-stu-id="4e54c-199">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="4e54c-200">WinMX</span><span class="sxs-lookup"><span data-stu-id="4e54c-200">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="4e54c-201">Winny</span><span class="sxs-lookup"><span data-stu-id="4e54c-201">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="4e54c-202">Payant</span><span class="sxs-lookup"><span data-stu-id="4e54c-202">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="4e54c-203">Yammer</span><span class="sxs-lookup"><span data-stu-id="4e54c-203">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="4e54c-204">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="4e54c-204">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="4e54c-205">YouTube</span><span class="sxs-lookup"><span data-stu-id="4e54c-205">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
