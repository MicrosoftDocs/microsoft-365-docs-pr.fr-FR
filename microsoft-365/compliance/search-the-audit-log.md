---
title: Rechercher dans le journal d’audit l’activité de l’utilisateur et de l’administrateur dans Office 365
f1.keywords:
- NOCSH
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
description: 'Le journal d’audit Office 365 est un journal d’audit unifié. Qu’est-ce qu’un journal d’audit unifié ? Étant donné que les événements provenant de la plupart des services Office 365 auxquels vous êtes abonné, sont enregistrés dans un seul journal d’audit que vous pouvez rechercher. Cela signifie que vous pouvez rechercher l’activité de l’utilisateur et de l’administrateur dans les services suivants :'
ms.openlocfilehash: 82ed3c1afd4f59136b04120982ddb1433f4dd0eb
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41597531"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="89481-106">Rechercher dans le journal d’audit l’activité de l’utilisateur et de l’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="89481-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="89481-107">Le journal d’audit Office 365 est un journal d’audit unifié.</span><span class="sxs-lookup"><span data-stu-id="89481-107">The Office 365 audit log is a unified audit log.</span></span> <span data-ttu-id="89481-108">Qu’est-ce qu’un journal d’audit unifié ?</span><span class="sxs-lookup"><span data-stu-id="89481-108">Why a unified audit log?</span></span> <span data-ttu-id="89481-109">Étant donné que les événements provenant de la plupart des services Office 365 auxquels vous êtes abonné, sont enregistrés dans un seul journal d’audit que vous pouvez rechercher.</span><span class="sxs-lookup"><span data-stu-id="89481-109">Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search.</span></span> <span data-ttu-id="89481-110">Cela signifie que vous pouvez rechercher l’activité de l’utilisateur et de l’administrateur dans les services suivants :</span><span class="sxs-lookup"><span data-stu-id="89481-110">That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="89481-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="89481-111">SharePoint</span></span>
- <span data-ttu-id="89481-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="89481-112">OneDrive</span></span>
- <span data-ttu-id="89481-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="89481-113">Exchange</span></span>
- <span data-ttu-id="89481-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="89481-114">Azure Active Directory</span></span>
- <span data-ttu-id="89481-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="89481-115">Microsoft Teams</span></span>
- <span data-ttu-id="89481-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="89481-116">eDiscovery</span></span>
- <span data-ttu-id="89481-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="89481-117">Power BI</span></span>
- <span data-ttu-id="89481-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="89481-118">Yammer</span></span>
- <span data-ttu-id="89481-119">Sway</span><span class="sxs-lookup"><span data-stu-id="89481-119">Sway</span></span>
- <span data-ttu-id="89481-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="89481-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="89481-121">Configurer l’audit</span><span class="sxs-lookup"><span data-stu-id="89481-121">Set up auditing</span></span>
  
<span data-ttu-id="89481-122">Vous devez effectuer quelques opérations avant de pouvoir effectuer une recherche dans le journal d’audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="89481-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="89481-123">[Activer la recherche du journal d’audit](turn-audit-log-search-on-or-off.md) pour commencer l’enregistrement des événements que vous pouvez rechercher</span><span class="sxs-lookup"><span data-stu-id="89481-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="89481-124">[Activer l’audit de boîte aux lettres](enable-mailbox-auditing.md) pour pouvoir Rechercher des événements liés à une boîte aux lettres ; par exemple lorsqu’un utilisateur se connecte à sa boîte aux lettres ou purge des éléments de son dossier éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="89481-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="89481-125">Effectuer une recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="89481-125">Search the audit log</span></span>
  
<span data-ttu-id="89481-126">Après avoir activé l’audit, vous recherchez des centaines de types d’événements individuels à partir de plusieurs services Office 365.</span><span class="sxs-lookup"><span data-stu-id="89481-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="89481-127">Rechercher les activités de l’utilisateur et de l’administrateur dans [le journal d’audit](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="89481-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="89481-128">[Comprendre les propriétés détaillées](detailed-properties-in-the-office-365-audit-log.md) de chaque enregistrement d’audit inclus dans les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="89481-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="89481-129">[Rechercher les activités de découverte électronique](search-for-ediscovery-activities-in-the-audit-log.md) effectuées par les administrateurs et les responsables de la conformité</span><span class="sxs-lookup"><span data-stu-id="89481-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
