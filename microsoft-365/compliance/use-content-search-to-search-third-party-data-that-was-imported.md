---
title: Utiliser la recherche de contenu pour rechercher des données tierces importées dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Utiliser l’outil eDiscovery de recherche de contenu pour rechercher des éléments importés dans des boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Vous pouvez créer une requête pour rechercher tous les éléments importés ou créer une requête pour rechercher des types de données tiers spécifiques. Cet article répertorie les valeurs que vous pouvez utiliser dans une requête de mot clé pour rechercher les types de données tiers que vous pouvez importer vers Office 365.
ms.openlocfilehash: 57a39049ae1df3707a96311c9138195b7cc4c83a
ms.sourcegitcommit: 1d376287f6c1bf5174873e89ed4bf7bb15bc13f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38685954"
---
# <a name="use-content-search-to-search-third-party-data-imported-to-office-365"></a><span data-ttu-id="8e4c0-105">Utiliser la recherche de contenu pour rechercher des données tierces importées dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8e4c0-105">Use Content Search to search third-party data imported to Office 365</span></span>

<span data-ttu-id="8e4c0-106">Vous pouvez utiliser l' [outil eDiscovery](content-search.md) de la recherche de contenu dans le centre de sécurité & conformité pour rechercher des éléments importés dans des boîtes aux lettres dans Office 365 à partir d’une source de données tierce.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="8e4c0-107">Vous pouvez créer une requête pour rechercher tous les éléments de données tiers importés ou créer une requête pour rechercher des éléments de données tiers spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-107">You can create a query to search all imported third-party data items or you can create a query to search specific third-party data items.</span></span> <span data-ttu-id="8e4c0-108">Par ailleurs, vous pouvez également créer une stratégie de rétention Office 365 basée sur une requête ou une conservation eDiscovery basée sur une requête pour conserver les données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-108">Also, you can also create a query-based Office 365 retention policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="8e4c0-109">Pour plus d’informations sur l’importation de données tierces et sur la liste des types de données tierces que vous pouvez importer vers Office 365, voir [collaborer avec un partenaire pour archiver des données tierces dans office 365](work-with-partner-to-archive-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="8e4c0-109">For more information about importing third-party data and a list of the third-party data types that you can import to Office 365, see [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="8e4c0-110">Création d’une requête pour rechercher toutes les données tierces</span><span class="sxs-lookup"><span data-stu-id="8e4c0-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="8e4c0-111">Pour rechercher (ou mettre en attente) tout type de données tierces que vous avez importées dans Office 365, vous pouvez utiliser `kind:externaldata` la paire message-valeur de la zone de mot clé pour une recherche de contenu ou lors de la création d’une conservation basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-111">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="8e4c0-112">Par exemple, pour rechercher des éléments importés à partir d’une source de données tierce et qui contiennent le mot « Contoso » dans la propriété Subject de l’élément importé, utilisez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="8e4c0-112">For example, to search for items imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```powershell
kind:externaldata AND subject:contoso
```

<span data-ttu-id="8e4c0-113">L’exemple de requête de mot clé précédent inclut la propriété Subject.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-113">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="8e4c0-114">Pour obtenir la liste des autres propriétés des éléments de données tierces pouvant être inclus dans une requête de mot-clé, voir la section « plus d’informations » dans [utilisation d’un partenaire pour archiver des données tierces dans Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="8e4c0-114">For a list of other properties for third-party data items that can include in a keyword query, see the "More information" section in [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="8e4c0-115">Lors de la création de requêtes de recherche et de conservation de données tierces, vous pouvez également utiliser des conditions pour affiner les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-115">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="8e4c0-116">Pour plus d’informations sur la création de requêtes de recherche de contenu, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="8e4c0-116">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="8e4c0-117">Création d’une requête pour rechercher des types spécifiques de données tierces</span><span class="sxs-lookup"><span data-stu-id="8e4c0-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="8e4c0-118">Au lieu de rechercher tous les types de données tierces, vous pouvez créer des requêtes qui recherchent uniquement un type précis de données tierces à l’aide de la paire de valeur de la *propriété* de message suivante dans la zone de mot clé pour une recherche de contenu :</span><span class="sxs-lookup"><span data-stu-id="8e4c0-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message *property:value* pair in the keyword box for a Content Search:</span></span>
  
```powershell
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="8e4c0-119">Par exemple, pour rechercher des données Facebook qui contiennent le mot « Contoso » dans la propriété Subject, vous devez utiliser la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="8e4c0-119">For example, to search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```powershell
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="8e4c0-120">Le tableau suivant répertorie les types de données tiers que vous pouvez rechercher et la valeur à utiliser pour la `itemclass:` propriété message afin de Rechercher spécifiquement ce type de données tierces.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-120">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="8e4c0-121">La syntaxe de la requête ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="8e4c0-121">The query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="8e4c0-122">**Type de données tiers**</span><span class="sxs-lookup"><span data-stu-id="8e4c0-122">**Third-party data type**</span></span>|<span data-ttu-id="8e4c0-123">**Valeur de `itemclass:` la propriété**</span><span class="sxs-lookup"><span data-stu-id="8e4c0-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e4c0-124">VISERA</span><span class="sxs-lookup"><span data-stu-id="8e4c0-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="8e4c0-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="8e4c0-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="8e4c0-126">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="8e4c0-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="8e4c0-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="8e4c0-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="8e4c0-128">Tréma</span><span class="sxs-lookup"><span data-stu-id="8e4c0-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="8e4c0-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="8e4c0-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="8e4c0-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="8e4c0-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="8e4c0-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="8e4c0-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="8e4c0-132">Espace réservé ax</span><span class="sxs-lookup"><span data-stu-id="8e4c0-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="8e4c0-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="8e4c0-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="8e4c0-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="8e4c0-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="8e4c0-135">BearShare</span><span class="sxs-lookup"><span data-stu-id="8e4c0-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="8e4c0-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="8e4c0-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="8e4c0-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="8e4c0-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="8e4c0-138">Journaux d’appels BlackBerry</span><span class="sxs-lookup"><span data-stu-id="8e4c0-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="8e4c0-139">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="8e4c0-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="8e4c0-140">Code confidentiel BlackBerry</span><span class="sxs-lookup"><span data-stu-id="8e4c0-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="8e4c0-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="8e4c0-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="8e4c0-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="8e4c0-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="8e4c0-143">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="8e4c0-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="8e4c0-144">Messages Bloomberg</span><span class="sxs-lookup"><span data-stu-id="8e4c0-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="8e4c0-145">Box</span><span class="sxs-lookup"><span data-stu-id="8e4c0-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="8e4c0-146">Serveur de &amp; présence de messagerie instantanée Cisco</span><span class="sxs-lookup"><span data-stu-id="8e4c0-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="8e4c0-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="8e4c0-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="8e4c0-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="8e4c0-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="8e4c0-149">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="8e4c0-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="8e4c0-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="8e4c0-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="8e4c0-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="8e4c0-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="8e4c0-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="8e4c0-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="8e4c0-153">Flickr</span><span class="sxs-lookup"><span data-stu-id="8e4c0-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="8e4c0-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="8e4c0-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="8e4c0-155">Google +</span><span class="sxs-lookup"><span data-stu-id="8e4c0-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="8e4c0-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="8e4c0-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="8e4c0-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="8e4c0-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="8e4c0-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="8e4c0-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="8e4c0-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="8e4c0-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="8e4c0-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="8e4c0-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="8e4c0-161">Connexions IBM</span><span class="sxs-lookup"><span data-stu-id="8e4c0-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="8e4c0-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="8e4c0-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="8e4c0-163">Conversation ICE</span><span class="sxs-lookup"><span data-stu-id="8e4c0-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="8e4c0-164">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="8e4c0-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="8e4c0-165">Instagram</span><span class="sxs-lookup"><span data-stu-id="8e4c0-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="8e4c0-166">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="8e4c0-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="8e4c0-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="8e4c0-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="8e4c0-168">SALLE</span><span class="sxs-lookup"><span data-stu-id="8e4c0-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="8e4c0-169">Jive</span><span class="sxs-lookup"><span data-stu-id="8e4c0-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="8e4c0-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="8e4c0-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="8e4c0-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="8e4c0-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="8e4c0-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="8e4c0-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="8e4c0-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="8e4c0-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="8e4c0-174">UC Microsoft</span><span class="sxs-lookup"><span data-stu-id="8e4c0-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="8e4c0-175">Correspondance des idées</span><span class="sxs-lookup"><span data-stu-id="8e4c0-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="8e4c0-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="8e4c0-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="8e4c0-177">SYMPATICO</span><span class="sxs-lookup"><span data-stu-id="8e4c0-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="8e4c0-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="8e4c0-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="8e4c0-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="8e4c0-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="8e4c0-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="8e4c0-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="8e4c0-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="8e4c0-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="8e4c0-182">Pivot</span><span class="sxs-lookup"><span data-stu-id="8e4c0-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="8e4c0-183">QQ</span><span class="sxs-lookup"><span data-stu-id="8e4c0-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="8e4c0-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="8e4c0-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="8e4c0-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="8e4c0-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="8e4c0-186">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="8e4c0-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="8e4c0-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="8e4c0-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="8e4c0-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="8e4c0-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="8e4c0-189">Squawker</span><span class="sxs-lookup"><span data-stu-id="8e4c0-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="8e4c0-190">Concert</span><span class="sxs-lookup"><span data-stu-id="8e4c0-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="8e4c0-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="8e4c0-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="8e4c0-192">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="8e4c0-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="8e4c0-193">Termes</span><span class="sxs-lookup"><span data-stu-id="8e4c0-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="8e4c0-194">TTT</span><span class="sxs-lookup"><span data-stu-id="8e4c0-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="8e4c0-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="8e4c0-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="8e4c0-196">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="8e4c0-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="8e4c0-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="8e4c0-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="8e4c0-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="8e4c0-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="8e4c0-199">Winny</span><span class="sxs-lookup"><span data-stu-id="8e4c0-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="8e4c0-200">Payant</span><span class="sxs-lookup"><span data-stu-id="8e4c0-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="8e4c0-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="8e4c0-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="8e4c0-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="8e4c0-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="8e4c0-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="8e4c0-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
