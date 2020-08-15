---
title: Surveiller la connectivité de Microsoft 365
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
description: Dans cet article, vous découvrirez les outils et les techniques que vous pouvez utiliser pour surveiller et gérer la connectivité de Microsoft 365.
ms.openlocfilehash: 7e62bcaae24f9e42fd0514c34c3d7dee764bc271
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689634"
---
# <a name="monitor-microsoft-365-connectivity"></a><span data-ttu-id="bd1d1-103">Surveiller la connectivité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd1d1-103">Monitor Microsoft 365 connectivity</span></span>

<span data-ttu-id="bd1d1-104">Une fois que vous avez déployé Microsoft 365, vous pouvez maintenir la connectivité de Microsoft 365 à l’aide de certains des outils et techniques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bd1d1-104">Once you've deployed Microsoft 365, you can maintain Microsoft 365 connectivity using some of the tools and techniques below.</span></span> <span data-ttu-id="bd1d1-105">Vous voudrez comprendre les directives officielles en matière de [santé et de continuité des services](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity) , ainsi que nos [meilleures pratiques pour l’utilisation de Microsoft 365 sur un réseau lent](https://support.office.com/article/fd16c8d2-4799-4c39-8fd7-045f06640166).</span><span class="sxs-lookup"><span data-stu-id="bd1d1-105">You'll want to understand the official [Service Health and Continuity](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity) guidelines as well as our [Best practices for using Microsoft 365 on a slow network](https://support.office.com/article/fd16c8d2-4799-4c39-8fd7-045f06640166).</span></span> <span data-ttu-id="bd1d1-106">Vous pouvez également récupérer l’application d' [administration de microsoft 365](https://blogs.office.com/2015/03/13/administer-on-the-go-with-the-updated-office-365-admin-app/) et ajouter un signet à notre [Microsoft 365 pour les entreprises-aide de l’administrateur](https://support.office.com/article/17d3ff3f-3601-466e-b5a1-482b31cfb791).</span><span class="sxs-lookup"><span data-stu-id="bd1d1-106">You'll also want to grab the [Microsoft 365 admin app](https://blogs.office.com/2015/03/13/administer-on-the-go-with-the-updated-office-365-admin-app/) and bookmark our [Microsoft 365 for business - Admin Help](https://support.office.com/article/17d3ff3f-3601-466e-b5a1-482b31cfb791).</span></span>
  
## <a name="monitoring-microsoft-365-connectivity"></a><span data-ttu-id="bd1d1-107">Surveillance de la connectivité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd1d1-107">Monitoring Microsoft 365 Connectivity</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd1d1-108">**Notification des nouveaux points de terminaison Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="bd1d1-108">**Getting notified of new Microsoft 365 endpoints**</span></span> <br/> |<span data-ttu-id="bd1d1-109">Si vous [gérez des points de terminaison Microsoft 365](https://support.office.com/article/99cab9d4-ef59-4207-9f2b-3728eb46bf9a), vous pouvez recevoir des notifications lors de la publication de nouveaux points de terminaison, vous pouvez vous abonner à notre flux RSS à l’aide de votre lecteur RSS favori.</span><span class="sxs-lookup"><span data-stu-id="bd1d1-109">If you're [Managing Microsoft 365 endpoints](https://support.office.com/article/99cab9d4-ef59-4207-9f2b-3728eb46bf9a), you'll want to receive notifications when we publish new endpoints, you can subscribe to our RSS feed using your favorite RSS reader.</span></span> <span data-ttu-id="bd1d1-110">Voici comment [s’abonner via Outlook](https://go.microsoft.com/fwlink/p/?LinkId=532416) ou vous pouvez vous [Envoyer les mises à jour du flux RSS par courrier électronique](https://go.microsoft.com/fwlink/p/?LinkId=532417).</span><span class="sxs-lookup"><span data-stu-id="bd1d1-110">Here is how to [subscribe via Outlook](https://go.microsoft.com/fwlink/p/?LinkId=532416) or you can [have the RSS feed updates emailed to you](https://go.microsoft.com/fwlink/p/?LinkId=532417).</span></span>  <br/> |
|<span data-ttu-id="bd1d1-111">**Utiliser System Center pour surveiller Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="bd1d1-111">**Use System Center to Monitor Microsoft 365**</span></span> <br/> |<span data-ttu-id="bd1d1-112">Si vous utilisez Microsoft System Center, vous pouvez télécharger le [Pack d’administration System Center pour Office 365](https://www.microsoft.com/download/details.aspx?id=43708) afin de commencer la surveillance de Microsoft 365 dès aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="bd1d1-112">If you're using Microsoft System Center, you can download the [System Center Management Pack for Office 365](https://www.microsoft.com/download/details.aspx?id=43708) to begin monitoring Microsoft 365 today.</span></span> <span data-ttu-id="bd1d1-113">Pour obtenir des instructions plus détaillées, reportez-vous au Guide des opérations du pack d’administration ou au billet de blog [Office 365 Monitoring using System Center Operations Manager](https://blogs.msdn.com/b/mvpawardprogram/archive/2015/07/08/office365-monitoring-using-system-centre-operations-manager.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-113">For more detailed guidance, please see the management pack operations guide or this blog post [Office365 Monitoring using System Centre Operations Manager](https://blogs.msdn.com/b/mvpawardprogram/archive/2015/07/08/office365-monitoring-using-system-centre-operations-manager.aspx)</span></span> <br/> |
|<span data-ttu-id="bd1d1-114">**Surveiller l’état d’Azure ExpressRoute**</span><span class="sxs-lookup"><span data-stu-id="bd1d1-114">**Monitoring the health of Azure ExpressRoute**</span></span> <br/> |<span data-ttu-id="bd1d1-115">Si vous vous connectez à Microsoft 365 à l’aide d’Azure ExpressRoute pour Microsoft 365, vous devez vous assurer que vous utilisez à la fois le tableau de bord Microsoft 365 service Health et le service Azure de [résolution des problèmes avec Azure Resource Health](https://azure.microsoft.com/blog/reduce-troubleshooting-time-with-azure-resource-health/)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-115">If you are connecting to Microsoft 365 using Azure ExpressRoute for Microsoft 365, you'll want to ensure that you're using both the Microsoft 365 Service Health Dashboard as well as the Azure [Reducing troubleshooting time with Azure Resource health](https://azure.microsoft.com/blog/reduce-troubleshooting-time-with-azure-resource-health/)</span></span> <br/> |
|<span data-ttu-id="bd1d1-116">**Utiliser Azure AD Connect Health avec AD FS**</span><span class="sxs-lookup"><span data-stu-id="bd1d1-116">**Using Azure AD Connect Health with AD FS**</span></span> <br/> |<span data-ttu-id="bd1d1-117">Si vous utilisez les services ADFS (Active Directory Federation Services) pour l’authentification unique avec Microsoft 365, vous pouvez commencer [à utiliser Azure ad Connect Health pour surveiller votre infrastructure AD FS](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect-health-adfs/).</span><span class="sxs-lookup"><span data-stu-id="bd1d1-117">If you're using AD FS for Single Sign-On with Microsoft 365, you'll want to begin [using Azure AD Connect Health to monitor your AD FS infrastructure](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect-health-adfs/).</span></span>  <br/> |
|<span data-ttu-id="bd1d1-118">**Surveillance par programme de Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="bd1d1-118">**Programmatically monitor Microsoft 365**</span></span> <br/> |<span data-ttu-id="bd1d1-119">Consultez nos conseils sur l' [API de gestion de Microsoft 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span><span class="sxs-lookup"><span data-stu-id="bd1d1-119">Refer to our guidance on the [Microsoft 365 Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span></span>  <br/> |

<span data-ttu-id="bd1d1-120">Voici un lien que vous pouvez utiliser pour revenir : [https://aka.ms/monitorconnectivity365](https://aka.ms/monitorconnectivity365)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-120">Here's a short link you can use to come back: [https://aka.ms/monitorconnectivity365](https://aka.ms/monitorconnectivity365)</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="bd1d1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd1d1-121">Related topics</span></span>

[<span data-ttu-id="bd1d1-122">Configurer les applications et services d’entreprise Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd1d1-122">Configure Microsoft 365 Enterprise services and applications</span></span>](configure-services-and-applications.md)
  
[<span data-ttu-id="bd1d1-123">Préparer votre organisation pour Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="bd1d1-123">Get your organization ready for Microsoft 365 Enterprise</span></span>](get-your-organization-ready-for-office-365.md)
  
[<span data-ttu-id="bd1d1-124">Planification réseau et optimisation des performances pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd1d1-124">Network planning and performance tuning for Microsoft 365</span></span>](network-planning-and-performance.md)
  
[<span data-ttu-id="bd1d1-125">Intégration de Microsoft 365 aux environnements locaux</span><span class="sxs-lookup"><span data-stu-id="bd1d1-125">Microsoft 365 integration with on-premises environments</span></span>](microsoft-365-integration.md)
  
[<span data-ttu-id="bd1d1-126">Gestion des points de terminaison Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bd1d1-126">Managing Microsoft 365 endpoints</span></span>](managing-office-365-endpoints.md)
