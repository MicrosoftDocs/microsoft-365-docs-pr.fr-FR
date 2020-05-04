---
title: Gérer les licences pour les appareils
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
description: Découvrez comment attribuer des licences à des groupes en vue de les utiliser avec des appareils.
ms.custom: okr_SMB
search.appverid:
- MET150
ms.openlocfilehash: 1a525117c25a2471ad696ef1447fd7e4ccb6bed0
ms.sourcegitcommit: bd8d55f82ca008af1b93a9bb4d1545f68e8188ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2020
ms.locfileid: "44011184"
---
# <a name="manage-licenses-for-devices"></a><span data-ttu-id="1a42f-103">Gérer les licences pour les appareils</span><span class="sxs-lookup"><span data-stu-id="1a42f-103">Manage licenses for devices</span></span>

<span data-ttu-id="1a42f-104">Si vous avez Microsoft 365 Apps for Enterprise (Device) ou Microsoft 365 Apps for Education (Device), vous pouvez attribuer des licences à des appareils à l’aide de groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1a42f-104">If you have Microsoft 365 Apps for enterprise (device) or Microsoft 365 Apps for Education (device), you can assign licenses to devices by using Azure AD groups.</span></span> <span data-ttu-id="1a42f-105">Lorsqu’un appareil dispose d’une licence, quiconque utilise ce périphérique peut utiliser les applications Microsoft 365 pour entreprise (précédemment nommé Office 365 ProPlus).</span><span class="sxs-lookup"><span data-stu-id="1a42f-105">When a device has a license, anyone who uses that device can use Microsoft 365 Apps for enterprise (previously named Office 365 ProPlus).</span></span> <span data-ttu-id="1a42f-106">Par exemple, imaginons que vous avez 20 ordinateurs portables et tablettes utilisés par les employés de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a42f-106">For example, let's say you have 20 laptops and tablets that are used by people in your organization.</span></span> <span data-ttu-id="1a42f-107">Lorsque vous attribuez une licence à chaque appareil, chaque personne qui se connecte à l’un des appareils utilise les applications Microsoft 365 pour Enterprise sans avoir à utiliser sa propre licence.</span><span class="sxs-lookup"><span data-stu-id="1a42f-107">When you assign a license to each device, each person who logs in to one of the devices uses Microsoft 365 Apps for enterprise without the need for their own license.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a42f-108">La gestion des licences basées sur les appareils pour les applications Microsoft 365 pour Enterprise est uniquement disponible en tant que licence de complément pour certains clients commerciaux et de formation.</span><span class="sxs-lookup"><span data-stu-id="1a42f-108">Device-based licensing for Microsoft 365 Apps for enterprise is available only as an add-on license for some commercial customers and some education customers.</span></span> <span data-ttu-id="1a42f-109">Pour les clients commerciaux, la licence est *Microsoft 365 apps pour entreprise (appareil)* et est disponible uniquement via un abonnement accord entreprise/accord entreprise.</span><span class="sxs-lookup"><span data-stu-id="1a42f-109">For commercial customers, the license is *Microsoft 365 Apps for enterprise (device)* and is available only through Enterprise Agreement/Enterprise Agreement Subscription.</span></span> <span data-ttu-id="1a42f-110">Pour les clients de l’éducation, la licence est *Microsoft 365 Apps for Education (Device)* et n’est disponible que par le biais de l’inscriptions for Education solutions (EES).</span><span class="sxs-lookup"><span data-stu-id="1a42f-110">For education customers, the license is *Microsoft 365 Apps for Education (device)* and is available only through Enrollment for Education Solutions (EES).</span></span> <span data-ttu-id="1a42f-111">Pour plus d’informations, consultez le billet de blog sur la disponibilité de l' [éducation](https://educationblog.microsoft.com/2019/08/attention-it-administrators-announcing-device-based-subscription-for-education/).</span><span class="sxs-lookup"><span data-stu-id="1a42f-111">For more information, read the blog post on [education availability](https://educationblog.microsoft.com/2019/08/attention-it-administrators-announcing-device-based-subscription-for-education/).</span></span> <span data-ttu-id="1a42f-112">Pour une disponibilité commerciale, contactez votre représentant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1a42f-112">For commercial availability, contact your Microsoft account representative.</span></span>

<span data-ttu-id="1a42f-113">Pour commencer, créez un groupe dans le centre d’administration Azure Active Directory, puis affectez des appareils au groupe.</span><span class="sxs-lookup"><span data-stu-id="1a42f-113">To begin, you create a group in the Azure Active Directory admin center, and then assign devices to the group.</span></span> <span data-ttu-id="1a42f-114">Pour en savoir plus sur les licences des appareils, notamment les exigences en matière de périphériques, les types de groupes que vous pouvez utiliser et comment configurer les applications Microsoft 365 pour entreprise afin d’utiliser la gestion des licences d’appareil, consultez la rubrique [relative aux licences basées sur les appareils pour les applications microsoft 365 pour les entreprises](https://go.microsoft.com/fwlink/p/?linkid=2094216).</span><span class="sxs-lookup"><span data-stu-id="1a42f-114">To learn more about device licensing, including device requirements, what types of groups you can use, and how to configure Microsoft 365 Apps for enterprise to use device licensing, see [Device-based licensing for Microsoft 365 Apps for enterprise](https://go.microsoft.com/fwlink/p/?linkid=2094216).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a42f-115">Vous devez être un administrateur général pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1a42f-115">You must be a Global admin to complete the tasks in this article.</span></span>

## <a name="assign-licenses-to-devices"></a><span data-ttu-id="1a42f-116">Attribuer des licences à des appareils</span><span class="sxs-lookup"><span data-stu-id="1a42f-116">Assign licenses to devices</span></span>

<span data-ttu-id="1a42f-117">Lorsque vous attribuez des licences à un groupe, vous attribuez des licences à tous les périphériques au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="1a42f-117">When you assign licenses to a group, you assign licenses to all devices within the group.</span></span> <span data-ttu-id="1a42f-118">Vous ne pouvez attribuer qu’un seul abonnement à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="1a42f-118">You can only assign one subscription to any single group.</span></span>

1. <span data-ttu-id="1a42f-119">Dans le centre d’administration Microsoft 365, accédez à la page<a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">licences</a> de **facturation** > .</span><span class="sxs-lookup"><span data-stu-id="1a42f-119">In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="1a42f-120">Sur la page **licences** , choisissez **Microsoft 365 Apps for Education (Device)** ou **Microsoft 365 apps pour entreprise (appareil)**.</span><span class="sxs-lookup"><span data-stu-id="1a42f-120">On the **Licenses** page, choose **Microsoft 365 Apps for Education (device)** or **Microsoft 365 Apps for enterprise (device)**.</span></span>
3. <span data-ttu-id="1a42f-121">Sur la page suivante, choisissez un abonnement, puis choisissez **attribuer des licences**.</span><span class="sxs-lookup"><span data-stu-id="1a42f-121">On the next page, choose a subscription, then choose **Assign licenses**.</span></span>
4. <span data-ttu-id="1a42f-122">Dans le volet **attribuer des licences à un groupe** , commencez à taper un nom de groupe, puis sélectionnez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="1a42f-122">In the **Assign licenses to a group** pane, begin typing a group name, and then choose it from the results to add it to the list.</span></span>
5. <span data-ttu-id="1a42f-123">Sélectionnez **affecter**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="1a42f-123">Choose **Assign**, then choose **Close**.</span></span>

## <a name="unassign-licenses-from-devices"></a><span data-ttu-id="1a42f-124">Désaffecter les licences des appareils</span><span class="sxs-lookup"><span data-stu-id="1a42f-124">Unassign licenses from devices</span></span>

<span data-ttu-id="1a42f-125">Lorsque vous désaffectez des licences à un groupe, vous supprimez les licences de tous les périphériques au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="1a42f-125">When you unassign licenses from a group, you remove the licenses from all devices within the group.</span></span> <span data-ttu-id="1a42f-126">Toutes les applications et leurs données associées sont alors en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1a42f-126">All apps and their associated data are then read-only.</span></span>

1. <span data-ttu-id="1a42f-127">Dans le centre d’administration, accédez à la page<a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">licences</a> de **facturation** > .</span><span class="sxs-lookup"><span data-stu-id="1a42f-127">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="1a42f-128">Sur la page **licences** , choisissez **Microsoft 365 Apps for Education (Device)** ou **Microsoft 365 apps pour entreprise (appareil)**.</span><span class="sxs-lookup"><span data-stu-id="1a42f-128">On the **Licenses** page, choose **Microsoft 365 Apps for Education (device)** or **Microsoft 365 Apps for enterprise (device)**.</span></span>
3. <span data-ttu-id="1a42f-129">Sur la page suivante, sélectionnez un abonnement, sélectionnez **autres actions**, puis **désaffecter les licences**.</span><span class="sxs-lookup"><span data-stu-id="1a42f-129">On the next page, choose a subscription, choose **More actions**, then choose **Unassign licenses**.</span></span>
4. <span data-ttu-id="1a42f-130">Dans la boîte de dialogue **Annuler l’attribution des licences** , sélectionnez Annuler l' **affectation**.</span><span class="sxs-lookup"><span data-stu-id="1a42f-130">In the **Unassign licenses** dialog box, choose **Unassign**.</span></span>