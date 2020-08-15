---
title: Limites des ressources Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
description: Dans cet article, vous trouverez des informations sur les limites des ressources pour les différentes applications de Microsoft 365.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 6053740d41b02461432243c8527391a4f8ae22ea
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690041"
---
# <a name="resource-limits"></a><span data-ttu-id="1f73f-103">Limites de ressources</span><span class="sxs-lookup"><span data-stu-id="1f73f-103">Resource Limits</span></span>

<span data-ttu-id="1f73f-104">Les limites des ressources sont appliquées à l’aide de quotas (limites) et de la limitation.</span><span class="sxs-lookup"><span data-stu-id="1f73f-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="1f73f-105">Azure Active Directory (Azure AD) et les services individuels Microsoft 365 utilisent les deux.</span><span class="sxs-lookup"><span data-stu-id="1f73f-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="1f73f-106">Les limites sont propres aux services et changent au fil du temps lorsque de nouvelles fonctionnalités sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="1f73f-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="1f73f-107">Pour plus d’informations sur les limites actuelles pour les différents services, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f73f-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="1f73f-108">Limites et restrictions du service Azure AD</span><span class="sxs-lookup"><span data-stu-id="1f73f-108">Azure AD service limits and restrictions</span></span>](https://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="1f73f-109">Limites d’Exchange Online</span><span class="sxs-lookup"><span data-stu-id="1f73f-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/library/exchange-online-limits.aspx)
- [<span data-ttu-id="1f73f-110">Limites d’Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="1f73f-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="1f73f-111">Limites et frontières des logiciels SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1f73f-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="1f73f-112">Limites de Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="1f73f-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="1f73f-113">API REST Yammer et limites de débit</span><span class="sxs-lookup"><span data-stu-id="1f73f-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="1f73f-114">Limites de taille de fichier dans Sway</span><span class="sxs-lookup"><span data-stu-id="1f73f-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="1f73f-115">En plus de ces limites, plusieurs mécanismes de limitation sont utilisés dans Azure AD et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1f73f-115">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="1f73f-116">La limitation au sein du service est particulièrement importante, étant donné que les ressources réseau dans les centres de données de Microsoft sont optimisées pour l’ensemble des clients qui utilisent les services.</span><span class="sxs-lookup"><span data-stu-id="1f73f-116">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="1f73f-117">Les mécanismes de limitation sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="1f73f-117">Throttling mechanisms include:</span></span>

- <span data-ttu-id="1f73f-118">Azure AD et Microsoft 365 fonctionnalité de limitation au niveau de l’utilisateur, ce qui limite le nombre de transactions ou d’appels simultanés (par script ou code) qui peuvent être effectués par un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f73f-118">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="1f73f-119">Une stratégie de limitation PowerShell par défaut est attribuée à chaque client lors de la création du client.</span><span class="sxs-lookup"><span data-stu-id="1f73f-119">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="1f73f-120">Ces paramètres affectent d’autres éléments, tels que le nombre maximal de sessions PowerShell simultanées pouvant être ouvertes par un administrateur unique.</span><span class="sxs-lookup"><span data-stu-id="1f73f-120">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="1f73f-121">Chaque client Exchange Online a une stratégie de services Web Exchange (EWS) par défaut ajustée pour les opérations clientes EWS et la limitation qui s’applique à tous les clients Outlook.</span><span class="sxs-lookup"><span data-stu-id="1f73f-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
