---
title: Archiver des données tierces
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Les administrateurs peuvent importer des données tierces à partir de plateformes de réseaux sociaux, de plateformes de messagerie instantanée et de plateformes de collaboration sur des documents vers des boîtes aux lettres de votre organisation Microsoft 365. Cela vous permet d’archiver des données à partir de Facebook, de Twitter et d’autres sources de données tierces dans Microsoft 365. Vous pouvez ensuite utiliser et appliquer les fonctionnalités de conformité de Microsoft 365 (telles que la conservation légale, la découverte électronique, l’archivage inaltérable et les stratégies de rétention) pour les données tierces.
ms.openlocfilehash: 72afb48f74a30bac2904e857a33487a83eba48cd
ms.sourcegitcommit: f9b5eca20e025acc36635cbd1786ff3407295857
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2020
ms.locfileid: "43027654"
---
# <a name="archive-third-party-data"></a><span data-ttu-id="ae60a-105">Archiver des données tierces</span><span class="sxs-lookup"><span data-stu-id="ae60a-105">Archive third-party data</span></span>

<span data-ttu-id="ae60a-106">Microsoft 365 permet aux administrateurs d’importer et d’archiver des données tierces à partir de plateformes de médias sociaux, de plateformes de messagerie instantanée et de plateformes de collaboration sur des documents, vers des boîtes aux lettres de votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ae60a-106">Microsoft 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Microsoft 365 organization.</span></span> <span data-ttu-id="ae60a-107">Les exemples de sources de données tierces que vous pouvez importer dans Microsoft 365 incluent les services suivants :</span><span class="sxs-lookup"><span data-stu-id="ae60a-107">Examples of third-party data sources that you can import to Microsoft 365 include the following services:</span></span> 
  
- <span data-ttu-id="ae60a-108">**Social :** Facebook, LinkedIn, Twitter et Yammer</span><span class="sxs-lookup"><span data-stu-id="ae60a-108">**Social:** Facebook, LinkedIn, Twitter, and Yammer</span></span>

- <span data-ttu-id="ae60a-109">**Messagerie instantanée :** Yahoo Messenger et GoogleTalk</span><span class="sxs-lookup"><span data-stu-id="ae60a-109">**Instant messaging:** Yahoo Messenger and GoogleTalk</span></span>

- <span data-ttu-id="ae60a-110">**Collaboration sur les documents :** Boîte et DropBox</span><span class="sxs-lookup"><span data-stu-id="ae60a-110">**Document collaboration:** Box and DropBox</span></span>

- <span data-ttu-id="ae60a-111">**Secteurs verticaux :** Gestion des relations client (par exemple, Salesforce chatter) et services financiers (par exemple, Bloomberg et Thomson Reuters)</span><span class="sxs-lookup"><span data-stu-id="ae60a-111">**Vertical industries:** Customer Relationship Management (such as Salesforce Chatter) and Financial Services (such as Bloomberg and Thomson Reuters)</span></span>

- <span data-ttu-id="ae60a-112">**Messagerie SMS/texte :** BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ae60a-112">**SMS/text messaging:** BlackBerry</span></span>

<span data-ttu-id="ae60a-113">Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité de Microsoft 365 telles que la conservation pour litige, la découverte électronique, l’archivage inaltérable, l’audit, la conformité de la communication et les stratégies de rétention à ces données.</span><span class="sxs-lookup"><span data-stu-id="ae60a-113">After third-party data is imported, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, In-Place Archiving, Auditing, Communication compliance, and retention policies to this data.</span></span> <span data-ttu-id="ae60a-114">Par exemple, lorsqu’une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées.</span><span class="sxs-lookup"><span data-stu-id="ae60a-114">For example, when a mailbox is placed on Litigation Hold, third-party data is preserved.</span></span> <span data-ttu-id="ae60a-115">Vous pouvez effectuer des recherches dans des données tierces à l’aide des outils eDiscovery de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae60a-115">You can search third-party data by using Microsoft eDiscovery tools.</span></span> <span data-ttu-id="ae60a-116">Vous pouvez également appliquer des stratégies d’archivage et de rétention à des données tierces, comme vous pouvez le faire pour Microsoft Data.</span><span class="sxs-lookup"><span data-stu-id="ae60a-116">Or you can apply archiving and retention policies to third-party data just like you can for Microsoft data.</span></span> <span data-ttu-id="ae60a-117">En bref, l’archivage des données tierces dans Microsoft 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="ae60a-117">In short, archiving third-party data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

<span data-ttu-id="ae60a-118">Il existe deux façons d’importer et d’archiver des données tierces dans Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="ae60a-118">There are two ways to import and archive third-party data in Microsoft 365:</span></span>

- <span data-ttu-id="ae60a-119">**Utilisez un connecteur de données tiers dans le centre de conformité & de sécurité :** Utilisez un connecteur de données personnalisé disponible dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ae60a-119">**Use a third-party data connector in the Security & Compliance Center:** Use a custom data connector that's available in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ae60a-120">Une fois que vous avez configuré et configuré le connecteur, il se connecte à la source de données tierce, convertit le contenu d’un élément en format de message électronique, puis importe l’élément dans une boîte aux lettres dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ae60a-120">After you set up and configure the connector, it connects to the third-party data source, converts the content of an item to an email message format, and then imports the item to a mailbox in Microsoft 365.</span></span> <span data-ttu-id="ae60a-121">Actuellement, vous pouvez implémenter des connecteurs pour importer et archiver des données à partir de pages d’entreprise Facebook, de comptes Twitter d’entreprise, de LinkedIn, de Bloomberg ou de ressources humaines (RH) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae60a-121">Currently, you can implement connectors to import and archive data from Facebook Business pages, corporate Twitter accounts, LinkedIn, Instant Bloomberg, and your organization's human resources (HR) data.</span></span> <span data-ttu-id="ae60a-122">Pour obtenir des instructions détaillées sur la configuration de l’un de ces connecteurs, voir :</span><span class="sxs-lookup"><span data-stu-id="ae60a-122">For the step-by-step instructions to set up one of these connectors, see:</span></span>

   - <span data-ttu-id="ae60a-123">**Facebook :** [utiliser un connecteur pour archiver des données Facebook](archive-facebook-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="ae60a-123">**Facebook:** [Use a connector to archive Facebook data](archive-facebook-data-with-sample-connector.md)</span></span>

   - <span data-ttu-id="ae60a-124">**Twitter :** [utiliser un connecteur pour archiver les données Twitter](archive-twitter-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="ae60a-124">**Twitter:** [Use a connector to archive Twitter data](archive-twitter-data-with-sample-connector.md)</span></span>

   - <span data-ttu-id="ae60a-125">**LinkedIn :** [configurer un connecteur pour l’archivage des données LinkedIn](archive-linkedin-data.md)</span><span class="sxs-lookup"><span data-stu-id="ae60a-125">**LinkedIn:** [Set up a connector to archive LinkedIn data](archive-linkedin-data.md)</span></span>

   - <span data-ttu-id="ae60a-126">**Instant Bloomberg :** [configurer un connecteur pour l’archivage des données Bloomberg instantanées](archive-instant-bloomberg-data.md)</span><span class="sxs-lookup"><span data-stu-id="ae60a-126">**Instant Bloomberg:** [Set up a connector to archive Instant Bloomberg data](archive-instant-bloomberg-data.md)</span></span>

   - <span data-ttu-id="ae60a-127">**Données RH :** [configurer un connecteur pour importer des données RH](import-hr-data.md)</span><span class="sxs-lookup"><span data-stu-id="ae60a-127">**HR data:** [Set up a connector to import HR data](import-hr-data.md)</span></span>

- <span data-ttu-id="ae60a-128">**Travaillez avec un partenaire Microsoft :** Votre organisation travaille avec un partenaire Microsoft qui fournira un connecteur personnalisé qui sera configuré pour extraire régulièrement les éléments de la source de données tierce, puis se connecter au Cloud de Microsoft par une API tierce et importer ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ae60a-128">**Work with a Microsoft partner:** Your organization works with a Microsoft Partner who will provide a custom connector that will be configured to extract items from the third-party data source on a regular basis and then connect to the Microsoft cloud by a third-party API and import those items to Microsoft 365.</span></span> <span data-ttu-id="ae60a-129">Le connecteur partenaire convertit également le contenu d’un élément de la source de données tierce en message électronique, puis l’importe dans une boîte aux lettres dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ae60a-129">The partner connector also converts the content of an item from the third-party data source to an email message and then imports it to a mailbox in Microsoft 365.</span></span> <span data-ttu-id="ae60a-130">Pour obtenir la liste des partenaires avec lesquels vous pouvez travailler et le processus pas à pas pour cette méthode, consultez [collaborer avec un partenaire pour archiver des données tierces dans Microsoft 365](work-with-partner-to-archive-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="ae60a-130">For a list of partners that you can work with and the step-by-step process for this method, see [Work with a partner to archive third-party data in Microsoft 365](work-with-partner-to-archive-third-party-data.md).</span></span>
