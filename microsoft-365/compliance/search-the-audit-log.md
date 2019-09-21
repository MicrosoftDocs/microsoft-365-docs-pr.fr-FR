---
title: Rechercher dans le journal d’audit l’activité de l’utilisateur et de l’administrateur dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'Le journal d’audit Office 365 est un journal d’audit unifié. Pourquoi un journal d’audit unifié ? Étant donné que les événements provenant de la plupart des services Office 365 auxquels vous êtes abonné, sont enregistrés dans un seul journal d’audit que vous pouvez rechercher. Cela signifie que vous pouvez rechercher l’activité de l’utilisateur et de l’administrateur dans les services suivants :'
ms.openlocfilehash: 1d3f45d24a8d1a83c20f5d36b12ced761e00f936
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079746"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="4ea9e-106">Rechercher dans le journal d’audit l’activité de l’utilisateur et de l’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4ea9e-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="4ea9e-107">Le journal d’audit Office 365 est un journal d’audit unifié.</span><span class="sxs-lookup"><span data-stu-id="4ea9e-107">The Office 365 audit log is a unified audit log.</span></span> <span data-ttu-id="4ea9e-108">Pourquoi un journal d’audit unifié ?</span><span class="sxs-lookup"><span data-stu-id="4ea9e-108">Why a unified audit log?</span></span> <span data-ttu-id="4ea9e-109">Étant donné que les événements provenant de la plupart des services Office 365 auxquels vous êtes abonné, sont enregistrés dans un seul journal d’audit que vous pouvez rechercher.</span><span class="sxs-lookup"><span data-stu-id="4ea9e-109">Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search.</span></span> <span data-ttu-id="4ea9e-110">Cela signifie que vous pouvez rechercher l’activité de l’utilisateur et de l’administrateur dans les services suivants :</span><span class="sxs-lookup"><span data-stu-id="4ea9e-110">That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="4ea9e-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="4ea9e-111">SharePoint</span></span>
- <span data-ttu-id="4ea9e-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="4ea9e-112">OneDrive</span></span>
- <span data-ttu-id="4ea9e-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4ea9e-113">Exchange</span></span>
- <span data-ttu-id="4ea9e-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="4ea9e-114">Azure Active Directory</span></span>
- <span data-ttu-id="4ea9e-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4ea9e-115">Microsoft Teams</span></span>
- <span data-ttu-id="4ea9e-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4ea9e-116">eDiscovery</span></span>
- <span data-ttu-id="4ea9e-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="4ea9e-117">Power BI</span></span>
- <span data-ttu-id="4ea9e-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="4ea9e-118">Yammer</span></span>
- <span data-ttu-id="4ea9e-119">Sway</span><span class="sxs-lookup"><span data-stu-id="4ea9e-119">Sway</span></span>
- <span data-ttu-id="4ea9e-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="4ea9e-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="4ea9e-121">Configurer l’audit</span><span class="sxs-lookup"><span data-stu-id="4ea9e-121">Set up auditing</span></span>
  
<span data-ttu-id="4ea9e-122">Vous devez effectuer quelques opérations avant de pouvoir effectuer une recherche dans le journal d’audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="4ea9e-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="4ea9e-123">[Activer la recherche du journal d’audit](turn-audit-log-search-on-or-off.md) pour commencer l’enregistrement des événements que vous pouvez rechercher</span><span class="sxs-lookup"><span data-stu-id="4ea9e-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="4ea9e-124">[Activer l’audit de boîte aux lettres](enable-mailbox-auditing.md) pour pouvoir Rechercher des événements liés à une boîte aux lettres ; par exemple lorsqu’un utilisateur se connecte à sa boîte aux lettres ou purge des éléments de son dossier éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="4ea9e-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="4ea9e-125">Effectuer une recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="4ea9e-125">Search the audit log</span></span>
  
<span data-ttu-id="4ea9e-126">Après avoir activé l’audit, vous recherchez des centaines de types d’événements individuels à partir de plusieurs services Office 365.</span><span class="sxs-lookup"><span data-stu-id="4ea9e-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="4ea9e-127">Rechercher les activités de l’utilisateur et de l’administrateur dans [le journal d’audit](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="4ea9e-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="4ea9e-128">[Comprendre les propriétés détaillées](detailed-properties-in-the-office-365-audit-log.md) de chaque enregistrement d’audit inclus dans les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="4ea9e-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="4ea9e-129">[Rechercher les activités de découverte électronique](search-for-ediscovery-activities-in-the-audit-log.md) effectuées par les administrateurs et les responsables de la conformité</span><span class="sxs-lookup"><span data-stu-id="4ea9e-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
