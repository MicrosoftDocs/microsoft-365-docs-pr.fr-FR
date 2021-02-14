---
title: Surveiller la connectivité Microsoft 365
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 8/4/2020
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- MOE150
- BCS160
ms.assetid: 53cdb60c-a6b2-4848-b3ff-e7b75dc3fd1f
description: Dans cet article, vous allez découvrir les outils et techniques que vous pouvez utiliser pour surveiller et maintenir la connectivité Microsoft 365.
ms.openlocfilehash: 7e62bcaae24f9e42fd0514c34c3d7dee764bc271
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689634"
---
# <a name="monitor-microsoft-365-connectivity"></a><span data-ttu-id="9248e-103">Surveiller la connectivité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9248e-103">Monitor Microsoft 365 connectivity</span></span>

<span data-ttu-id="9248e-104">Une fois que vous avez déployé Microsoft 365, vous pouvez maintenir la connectivité Microsoft 365 à l’aide de certains des outils et techniques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9248e-104">Once you've deployed Microsoft 365, you can maintain Microsoft 365 connectivity using some of the tools and techniques below.</span></span> <span data-ttu-id="9248e-105">Vous souhaiterez comprendre les instructions officielles relatives à la continuité et à l’état du [service,](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity) ainsi que nos meilleures pratiques d’utilisation de [Microsoft 365 sur un réseau lent.](https://support.office.com/article/fd16c8d2-4799-4c39-8fd7-045f06640166)</span><span class="sxs-lookup"><span data-stu-id="9248e-105">You'll want to understand the official [Service Health and Continuity](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity) guidelines as well as our [Best practices for using Microsoft 365 on a slow network](https://support.office.com/article/fd16c8d2-4799-4c39-8fd7-045f06640166).</span></span> <span data-ttu-id="9248e-106">Vous pouvez également récupérer l’application d’administration [Microsoft 365](https://blogs.office.com/2015/03/13/administer-on-the-go-with-the-updated-office-365-admin-app/) et mettre en signet notre Microsoft 365 pour les entreprises [- Aide de l’administrateur.](https://support.office.com/article/17d3ff3f-3601-466e-b5a1-482b31cfb791)</span><span class="sxs-lookup"><span data-stu-id="9248e-106">You'll also want to grab the [Microsoft 365 admin app](https://blogs.office.com/2015/03/13/administer-on-the-go-with-the-updated-office-365-admin-app/) and bookmark our [Microsoft 365 for business - Admin Help](https://support.office.com/article/17d3ff3f-3601-466e-b5a1-482b31cfb791).</span></span>
  
## <a name="monitoring-microsoft-365-connectivity"></a><span data-ttu-id="9248e-107">Surveillance de la connectivité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9248e-107">Monitoring Microsoft 365 Connectivity</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9248e-108">**Notification des nouveaux points de terminaison Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="9248e-108">**Getting notified of new Microsoft 365 endpoints**</span></span> <br/> |<span data-ttu-id="9248e-109">Si vous gérez des points de terminaison [Microsoft 365,](https://support.office.com/article/99cab9d4-ef59-4207-9f2b-3728eb46bf9a)vous souhaiterez recevoir des notifications lorsque nous publions de nouveaux points de terminaison, vous pouvez vous abonner à notre flux RSS à l’aide de votre lecteur RSS favori.</span><span class="sxs-lookup"><span data-stu-id="9248e-109">If you're [Managing Microsoft 365 endpoints](https://support.office.com/article/99cab9d4-ef59-4207-9f2b-3728eb46bf9a), you'll want to receive notifications when we publish new endpoints, you can subscribe to our RSS feed using your favorite RSS reader.</span></span> <span data-ttu-id="9248e-110">Voici comment vous abonner [via Outlook](https://go.microsoft.com/fwlink/p/?LinkId=532416) ou vous pouvez envoyer par courrier électronique les mises à jour de flux [RSS.](https://go.microsoft.com/fwlink/p/?LinkId=532417)</span><span class="sxs-lookup"><span data-stu-id="9248e-110">Here is how to [subscribe via Outlook](https://go.microsoft.com/fwlink/p/?LinkId=532416) or you can [have the RSS feed updates emailed to you](https://go.microsoft.com/fwlink/p/?LinkId=532417).</span></span>  <br/> |
|<span data-ttu-id="9248e-111">**Utiliser System Center pour surveiller Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="9248e-111">**Use System Center to Monitor Microsoft 365**</span></span> <br/> |<span data-ttu-id="9248e-112">Si vous utilisez Microsoft System Center, vous pouvez télécharger le pack d’administration System Center pour [Office 365](https://www.microsoft.com/download/details.aspx?id=43708) afin de commencer à surveiller Microsoft 365 dès aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="9248e-112">If you're using Microsoft System Center, you can download the [System Center Management Pack for Office 365](https://www.microsoft.com/download/details.aspx?id=43708) to begin monitoring Microsoft 365 today.</span></span> <span data-ttu-id="9248e-113">Pour obtenir des instructions plus détaillées, consultez le guide des opérations du pack d’administration ou ce billet de blog sur la surveillance [d’Office 365](https://blogs.msdn.com/b/mvpawardprogram/archive/2015/07/08/office365-monitoring-using-system-centre-operations-manager.aspx) à l’aide de System Centre Operations Manager</span><span class="sxs-lookup"><span data-stu-id="9248e-113">For more detailed guidance, please see the management pack operations guide or this blog post [Office365 Monitoring using System Centre Operations Manager](https://blogs.msdn.com/b/mvpawardprogram/archive/2015/07/08/office365-monitoring-using-system-centre-operations-manager.aspx)</span></span> <br/> |
|<span data-ttu-id="9248e-114">**Surveiller l’état d’Azure ExpressRoute**</span><span class="sxs-lookup"><span data-stu-id="9248e-114">**Monitoring the health of Azure ExpressRoute**</span></span> <br/> |<span data-ttu-id="9248e-115">Si vous vous connectez à Microsoft 365 à l’aide d’Azure ExpressRoute pour Microsoft 365, vous devez vous assurer que vous utilisez à la fois le tableau de bord d’état du service Microsoft 365 et Azure Réduisant le temps de dépannage avec l’état des ressources [Azure](https://azure.microsoft.com/blog/reduce-troubleshooting-time-with-azure-resource-health/)</span><span class="sxs-lookup"><span data-stu-id="9248e-115">If you are connecting to Microsoft 365 using Azure ExpressRoute for Microsoft 365, you'll want to ensure that you're using both the Microsoft 365 Service Health Dashboard as well as the Azure [Reducing troubleshooting time with Azure Resource health](https://azure.microsoft.com/blog/reduce-troubleshooting-time-with-azure-resource-health/)</span></span> <br/> |
|<span data-ttu-id="9248e-116">**Utiliser Azure AD Connect Health avec AD FS**</span><span class="sxs-lookup"><span data-stu-id="9248e-116">**Using Azure AD Connect Health with AD FS**</span></span> <br/> |<span data-ttu-id="9248e-117">Si vous utilisez AD FS pour Sign-On unique avec Microsoft 365, vous pouvez commencer à utiliser Azure AD Connect Health pour surveiller votre [infrastructure AD FS.](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect-health-adfs/)</span><span class="sxs-lookup"><span data-stu-id="9248e-117">If you're using AD FS for Single Sign-On with Microsoft 365, you'll want to begin [using Azure AD Connect Health to monitor your AD FS infrastructure](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect-health-adfs/).</span></span>  <br/> |
|<span data-ttu-id="9248e-118">**Surveiller Microsoft 365 par programme**</span><span class="sxs-lookup"><span data-stu-id="9248e-118">**Programmatically monitor Microsoft 365**</span></span> <br/> |<span data-ttu-id="9248e-119">Reportez-vous à nos conseils sur l’API de gestion [Microsoft 365.](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)</span><span class="sxs-lookup"><span data-stu-id="9248e-119">Refer to our guidance on the [Microsoft 365 Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span></span>  <br/> |

<span data-ttu-id="9248e-120">Voici un lien que vous pouvez utiliser pour revenir : [https://aka.ms/monitorconnectivity365](https://aka.ms/monitorconnectivity365)</span><span class="sxs-lookup"><span data-stu-id="9248e-120">Here's a short link you can use to come back: [https://aka.ms/monitorconnectivity365](https://aka.ms/monitorconnectivity365)</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="9248e-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9248e-121">Related topics</span></span>

[<span data-ttu-id="9248e-122">Configurer les applications et services Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9248e-122">Configure Microsoft 365 Enterprise services and applications</span></span>](configure-services-and-applications.md)
  
[<span data-ttu-id="9248e-123">Préparer votre organisation pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9248e-123">Get your organization ready for Microsoft 365 Enterprise</span></span>](get-your-organization-ready-for-office-365.md)
  
[<span data-ttu-id="9248e-124">Planification réseau et optimisation des performances pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9248e-124">Network planning and performance tuning for Microsoft 365</span></span>](network-planning-and-performance.md)
  
[<span data-ttu-id="9248e-125">Intégration de Microsoft 365 aux environnements locaux</span><span class="sxs-lookup"><span data-stu-id="9248e-125">Microsoft 365 integration with on-premises environments</span></span>](microsoft-365-integration.md)
  
[<span data-ttu-id="9248e-126">Gestion des points de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9248e-126">Managing Microsoft 365 endpoints</span></span>](managing-office-365-endpoints.md)
