---
title: Utiliser les rapports
description: Les différents rapports disponibles dans Bureau géré Microsoft
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 28035a9f0a669c1daa7526d0b1fefac52a77c81a
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52729967"
---
# <a name="work-with-reports"></a><span data-ttu-id="59e05-104">Utiliser les rapports</span><span class="sxs-lookup"><span data-stu-id="59e05-104">Work with reports</span></span>

<span data-ttu-id="59e05-105">Bureau géré Microsoft fournit plusieurs rapports et tableaux de bord que les administrateurs informatiques de votre organisation peuvent utiliser pour comprendre différents aspects de la population d’appareils.</span><span class="sxs-lookup"><span data-stu-id="59e05-105">Microsoft Managed Desktop provides several reports and dashboards that IT admins in your organization can use to understand various aspects of the population of devices.</span></span><span data-ttu-id="59e05-106">Vous trouverez des rapports à deux emplacements : dans [Microsoft Endpoint Manager](https://endpoint.microsoft.com) et dans le [centre d Microsoft 365'administration.](https://admin.microsoft.com/adminportal/home?previewoff=false#/microsoftmanageddesktop)</span><span class="sxs-lookup"><span data-stu-id="59e05-106"> You'll find reports in two locations: in [Microsoft Endpoint Manager](https://endpoint.microsoft.com) and in the [Microsoft 365 Admin Center](https://admin.microsoft.com/adminportal/home?previewoff=false#/microsoftmanageddesktop).</span></span> 

## <a name="reports-in-microsoft-endpoint-manager"></a><span data-ttu-id="59e05-107">Rapports dans Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="59e05-107">Reports in Microsoft Endpoint Manager</span></span>

<span data-ttu-id="59e05-108">La console Microsoft Endpoint Manager regroupe les rapports de plusieurs produits dans un emplacement unique pour vous aider à surveiller et à examiner les problèmes de configuration et d’appareils de votre organisation Azure AD (« client »).</span><span class="sxs-lookup"><span data-stu-id="59e05-108">The Microsoft Endpoint Manager console brings together reporting from several products into a single location to help you monitor and investigate issues with your Azure AD organization ("tenant") configuration and devices.</span></span> <span data-ttu-id="59e05-109">Bureau géré Microsoft comprend une section sous **Rapports** dans le menu principal où vous pouvez trouver des rapports spécifiques à Bureau géré Microsoft gestion des appareils que vous avez enregistrés.</span><span class="sxs-lookup"><span data-stu-id="59e05-109">Microsoft Managed desktop has a section under **Reports** in the main menu where you can find reports specific to Microsoft Managed Desktop's management of the devices you’ve registered.</span></span>

<span data-ttu-id="59e05-110">Ces rapports sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="59e05-110">These reports include:</span></span>
- <span data-ttu-id="59e05-111">**Appareils gérés**  >  **Mises à jour de fonctionnalités**: cet affichage affiche l’état global des mises à jour de fonctionnalités sur Bureau géré Microsoft appareils.</span><span class="sxs-lookup"><span data-stu-id="59e05-111">**Managed devices** > **Feature updates**: This view shows the overall status of feature updates across your Microsoft Managed Desktop devices.</span></span>
- <span data-ttu-id="59e05-112">**Appareils gérés**  >  **Office mises à** jour : cet affichage affiche l’état global des mises à jour Office mises à jour sur Bureau géré Microsoft appareils.</span><span class="sxs-lookup"><span data-stu-id="59e05-112">**Managed devices** > **Office updates**: This view shows the overall status of Office updates across your Microsoft Managed Desktop devices.</span></span>

<span data-ttu-id="59e05-113">En outre, dans plusieurs emplacements dans Microsoft Endpoint Manager vous pouvez filtrer les rapports provenant d’autres groupes de produits afin d’inclure ou d’exclure spécifiquement vos appareils gérés par Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59e05-113">Additionally, in several locations throughout Microsoft Endpoint Manager you can filter reports from other product groups to specifically include or exclude your devices that are managed by Microsoft Managed Desktop.</span></span> <span data-ttu-id="59e05-114">Ces rapports ont intégré cette fonctionnalité de filtrage :</span><span class="sxs-lookup"><span data-stu-id="59e05-114">These reports have integrated this filtering capability:</span></span>

- [<span data-ttu-id="59e05-115">Tous les appareils</span><span class="sxs-lookup"><span data-stu-id="59e05-115">All devices</span></span>](/mem/intune/remote-actions/device-management#get-to-your-devices)
- [<span data-ttu-id="59e05-116">Conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="59e05-116">Device compliance</span></span>](/mem/intune/fundamentals/reports#device-compliance-report-organizational)
- [<span data-ttu-id="59e05-117">Appareils non conformes</span><span class="sxs-lookup"><span data-stu-id="59e05-117">Noncompliant devices</span></span>](/mem/intune/fundamentals/reports#noncompliant-devices-report-operational)

> [!NOTE]
> <span data-ttu-id="59e05-118">Les rôles Bureau géré Microsoft personnalisés garantissent l’accès uniquement aux Bureau géré Microsoft rapports.</span><span class="sxs-lookup"><span data-stu-id="59e05-118">Custom Microsoft Managed Desktop roles guarantee access only to the Microsoft Managed Desktop reports.</span></span> <span data-ttu-id="59e05-119">Pour accéder à d’autres parties Microsoft Endpoint Manager, telles que tous les **appareils,** voir Contrôle d’accès basé sur un [rôle avec Microsoft Intune](/mem/intune/fundamentals/role-based-access-control).</span><span class="sxs-lookup"><span data-stu-id="59e05-119">To access other parts of Microsoft Endpoint Manager, such as **All devices**, see [Role-based access control with Microsoft Intune](/mem/intune/fundamentals/role-based-access-control).</span></span> 


 ## <a name="inventory-data"></a><span data-ttu-id="59e05-120">Données d’inventaire</span><span class="sxs-lookup"><span data-stu-id="59e05-120">Inventory data</span></span>

<span data-ttu-id="59e05-121">Outre les autres rapports, vous pouvez exporter des informations sur les appareils gérés par Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59e05-121">In addition to the other reports, you can export information about the devices managed by Microsoft Managed Desktop.</span></span> <span data-ttu-id="59e05-122">Dans la vue  **Appareils** de la zone Appareils  de Microsoft Endpoint Manager, utilisez l’onglet Exporter tout pour télécharger un [rapport d’inventaire détaillé.](device-inventory-report.md)</span><span class="sxs-lookup"><span data-stu-id="59e05-122">In the **Devices** view of the **Devices** area of Microsoft Endpoint Manager, use the **Export all** tab to [download a detailed inventory report](device-inventory-report.md).</span></span>