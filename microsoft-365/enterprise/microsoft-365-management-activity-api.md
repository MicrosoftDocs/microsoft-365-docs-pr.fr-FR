---
title: API Activité de gestion Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
f1.keywords:
- NOCSH
description: Dans cet article, vous trouverez un bref résumé de l’API activité de gestion d’Office 365 et des informations qu’elle fournit à partir des journaux d’activité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8d51f27f28b0adb84ef43004664ef310567263b9
ms.sourcegitcommit: c029834c8a914b4e072de847fc4c3a3dde7790c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47332303"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="1fde3-103">API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="1fde3-103">Office 365 Management Activity API</span></span>

<span data-ttu-id="1fde3-104">Microsoft fournit Reporting Services que vous pouvez utiliser pour obtenir des informations transactionnelles regroupées sur votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="1fde3-104">Microsoft provides reporting services you can use to obtain aggregated transactional information about your Office 365 tenant.</span></span> <span data-ttu-id="1fde3-105">L' [API activité de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview#office-365-management-activity-api) utilise une conception standard RESTful et OAuth v2 pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1fde3-105">The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview#office-365-management-activity-api) uses an industry-standard RESTful design and OAuth v2 for authentication.</span></span> <span data-ttu-id="1fde3-106">Ainsi, il est facile de commencer à expérimenter la récupération des données et de les inverser dans les applications et les outils de visualisation.</span><span class="sxs-lookup"><span data-stu-id="1fde3-106">This makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications.</span></span> <span data-ttu-id="1fde3-107">L’API fournit un flux de données avec des informations sur l’activité de l’utilisateur, de l’administrateur, des opérations et de la sécurité dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="1fde3-107">The API provides a data feed with information about user, administrator, operations, and security activity in Office 365.</span></span> <span data-ttu-id="1fde3-108">Les données peuvent être conservées à des fins de réglementation ou associées à des données de journal achetées à partir d’une infrastructure locale ou d’autres sources.</span><span class="sxs-lookup"><span data-stu-id="1fde3-108">The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources.</span></span> <span data-ttu-id="1fde3-109">Cela permet de créer une solution de surveillance pour les opérations, la sécurité et la conformité au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1fde3-109">This helps build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="1fde3-110">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1fde3-110">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="1fde3-111">L’API fournit un schéma d’audit cohérent avec plus de 10 champs communs à tous les services.</span><span class="sxs-lookup"><span data-stu-id="1fde3-111">The API provides a consistent audit schema with over 10 fields common across all the services.</span></span> <span data-ttu-id="1fde3-112">L’API permet aux organisations de se connecter facilement entre les événements et permet de créer des raisons de conséquence sur les données.</span><span class="sxs-lookup"><span data-stu-id="1fde3-112">The API allows organizations to make easy connections between events, and enables new ways to reason over the data.</span></span>

<span data-ttu-id="1fde3-113">Des dizaines de fournisseurs de logiciels indépendants (ISV) s’associent à Microsoft et ont créé des solutions basées sur l’API.</span><span class="sxs-lookup"><span data-stu-id="1fde3-113">Dozens of Independent Software Vendors (ISVs) partnered with Microsoft and have built solutions based on the API.</span></span> <span data-ttu-id="1fde3-114">Certaines solutions se concentrent uniquement sur les données Office 365 et d’autres sources de données à partir de plusieurs fournisseurs de Cloud et de systèmes locaux pour créer une vue unifiée de l’activité des opérations, de la sécurité et de la conformité.</span><span class="sxs-lookup"><span data-stu-id="1fde3-114">Some solutions focus solely on Office 365 data and others source data from multiple cloud providers and on-premises systems to create a unified view of operations, security, and compliance-related activity.</span></span> 

<span data-ttu-id="1fde3-115">Pour plus d’informations, reportez-vous à la [référence API activité de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="1fde3-115">For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
