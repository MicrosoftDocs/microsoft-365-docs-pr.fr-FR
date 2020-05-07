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
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment importer des données tierces à partir de plateformes de médias sociaux, de plateformes de messagerie instantanée et de plateformes de collaboration sur des documents vers des boîtes aux lettres Microsoft 365.
ms.openlocfilehash: 0db7019b607388b7c62fe19210b85b8410083f32
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44035482"
---
# <a name="archive-third-party-data"></a><span data-ttu-id="6dd1c-103">Archiver des données tierces</span><span class="sxs-lookup"><span data-stu-id="6dd1c-103">Archive third-party data</span></span>

<span data-ttu-id="6dd1c-104">Microsoft 365 permet aux administrateurs d’importer et d’archiver des données tierces à partir de plateformes de médias sociaux, de plateformes de messagerie instantanée et de plateformes de collaboration sur des documents, vers des boîtes aux lettres de votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-104">Microsoft 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Microsoft 365 organization.</span></span> <span data-ttu-id="6dd1c-105">Les exemples de sources de données tierces que vous pouvez importer dans Microsoft 365 incluent les services suivants :</span><span class="sxs-lookup"><span data-stu-id="6dd1c-105">Examples of third-party data sources that you can import to Microsoft 365 include the following services:</span></span> 
  
- <span data-ttu-id="6dd1c-106">**Social :** Facebook, LinkedIn, Twitter et Yammer</span><span class="sxs-lookup"><span data-stu-id="6dd1c-106">**Social:** Facebook, LinkedIn, Twitter, and Yammer</span></span>

- <span data-ttu-id="6dd1c-107">**Messagerie instantanée :** Yahoo Messenger et GoogleTalk</span><span class="sxs-lookup"><span data-stu-id="6dd1c-107">**Instant messaging:** Yahoo Messenger and GoogleTalk</span></span>

- <span data-ttu-id="6dd1c-108">**Collaboration sur les documents :** Boîte et DropBox</span><span class="sxs-lookup"><span data-stu-id="6dd1c-108">**Document collaboration:** Box and DropBox</span></span>

- <span data-ttu-id="6dd1c-109">**Secteurs verticaux :** Gestion des relations client (par exemple, Salesforce chatter) et services financiers (par exemple, Bloomberg et Thomson Reuters)</span><span class="sxs-lookup"><span data-stu-id="6dd1c-109">**Vertical industries:** Customer Relationship Management (such as Salesforce Chatter) and Financial Services (such as Bloomberg and Thomson Reuters)</span></span>

- <span data-ttu-id="6dd1c-110">**Messagerie SMS/texte :** BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6dd1c-110">**SMS/text messaging:** BlackBerry</span></span>

<span data-ttu-id="6dd1c-111">Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité de Microsoft 365 telles que la conservation pour litige, la découverte électronique, l’archivage inaltérable, l’audit, la conformité de la communication et les stratégies de rétention à ces données.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-111">After third-party data is imported, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, In-Place Archiving, Auditing, Communication compliance, and retention policies to this data.</span></span> <span data-ttu-id="6dd1c-112">Par exemple, lorsqu’une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-112">For example, when a mailbox is placed on Litigation Hold, third-party data is preserved.</span></span> <span data-ttu-id="6dd1c-113">Vous pouvez effectuer des recherches dans des données tierces à l’aide des outils eDiscovery de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-113">You can search third-party data by using Microsoft eDiscovery tools.</span></span> <span data-ttu-id="6dd1c-114">Vous pouvez également appliquer des stratégies d’archivage et de rétention à des données tierces, comme vous pouvez le faire pour Microsoft Data.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-114">Or you can apply archiving and retention policies to third-party data just like you can for Microsoft data.</span></span> <span data-ttu-id="6dd1c-115">En bref, l’archivage des données tierces dans Microsoft 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-115">In short, archiving third-party data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

<span data-ttu-id="6dd1c-116">Il existe deux façons d’importer et d’archiver des données tierces dans Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="6dd1c-116">There are two ways to import and archive third-party data in Microsoft 365:</span></span>

- <span data-ttu-id="6dd1c-117">**Utilisez un connecteur de données tiers dans le centre de conformité & de sécurité :** Utilisez un connecteur de données personnalisé disponible dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-117">**Use a third-party data connector in the Security & Compliance Center:** Use a custom data connector that's available in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="6dd1c-118">Une fois que vous avez configuré et configuré le connecteur, il se connecte à la source de données tierce, convertit le contenu d’un élément en format de message électronique, puis importe l’élément dans une boîte aux lettres dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-118">After you set up and configure the connector, it connects to the third-party data source, converts the content of an item to an email message format, and then imports the item to a mailbox in Microsoft 365.</span></span> <span data-ttu-id="6dd1c-119">Actuellement, vous pouvez implémenter des connecteurs pour importer et archiver des données à partir de pages d’entreprise Facebook, de comptes Twitter d’entreprise, de LinkedIn, de Bloomberg ou de ressources humaines (RH) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-119">Currently, you can implement connectors to import and archive data from Facebook Business pages, corporate Twitter accounts, LinkedIn, Instant Bloomberg, and your organization's human resources (HR) data.</span></span> <span data-ttu-id="6dd1c-120">Pour obtenir des instructions détaillées sur la configuration de l’un de ces connecteurs, voir :</span><span class="sxs-lookup"><span data-stu-id="6dd1c-120">For the step-by-step instructions to set up one of these connectors, see:</span></span>

   - <span data-ttu-id="6dd1c-121">**Facebook :** [utiliser un connecteur pour archiver des données Facebook](archive-facebook-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="6dd1c-121">**Facebook:** [Use a connector to archive Facebook data](archive-facebook-data-with-sample-connector.md)</span></span>

   - <span data-ttu-id="6dd1c-122">**Twitter :** [utiliser un connecteur pour archiver les données Twitter](archive-twitter-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="6dd1c-122">**Twitter:** [Use a connector to archive Twitter data](archive-twitter-data-with-sample-connector.md)</span></span>

   - <span data-ttu-id="6dd1c-123">**LinkedIn :** [configurer un connecteur pour l’archivage des données LinkedIn](archive-linkedin-data.md)</span><span class="sxs-lookup"><span data-stu-id="6dd1c-123">**LinkedIn:** [Set up a connector to archive LinkedIn data](archive-linkedin-data.md)</span></span>

   - <span data-ttu-id="6dd1c-124">**Instant Bloomberg :** [configurer un connecteur pour l’archivage des données Bloomberg instantanées](archive-instant-bloomberg-data.md)</span><span class="sxs-lookup"><span data-stu-id="6dd1c-124">**Instant Bloomberg:** [Set up a connector to archive Instant Bloomberg data](archive-instant-bloomberg-data.md)</span></span>

   - <span data-ttu-id="6dd1c-125">**Données RH :** [configurer un connecteur pour importer des données RH](import-hr-data.md)</span><span class="sxs-lookup"><span data-stu-id="6dd1c-125">**HR data:** [Set up a connector to import HR data](import-hr-data.md)</span></span>

- <span data-ttu-id="6dd1c-126">**Travaillez avec un partenaire Microsoft :** Votre organisation travaille avec un partenaire Microsoft qui fournira un connecteur personnalisé qui sera configuré pour extraire régulièrement les éléments de la source de données tierce, puis se connecter au Cloud de Microsoft par une API tierce et importer ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-126">**Work with a Microsoft partner:** Your organization works with a Microsoft Partner who will provide a custom connector that will be configured to extract items from the third-party data source on a regular basis and then connect to the Microsoft cloud by a third-party API and import those items to Microsoft 365.</span></span> <span data-ttu-id="6dd1c-127">Le connecteur partenaire convertit également le contenu d’un élément de la source de données tierce en message électronique, puis l’importe dans une boîte aux lettres dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6dd1c-127">The partner connector also converts the content of an item from the third-party data source to an email message and then imports it to a mailbox in Microsoft 365.</span></span> <span data-ttu-id="6dd1c-128">Pour obtenir la liste des partenaires avec lesquels vous pouvez travailler et le processus pas à pas pour cette méthode, consultez [collaborer avec un partenaire pour archiver des données tierces dans Microsoft 365](work-with-partner-to-archive-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="6dd1c-128">For a list of partners that you can work with and the step-by-step process for this method, see [Work with a partner to archive third-party data in Microsoft 365](work-with-partner-to-archive-third-party-data.md).</span></span>
