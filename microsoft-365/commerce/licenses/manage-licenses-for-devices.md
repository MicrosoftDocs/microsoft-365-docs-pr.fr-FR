---
title: Gérer les licences pour les appareils
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: shegu, nicholak
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
description: Découvrez comment attribuer des licences à des groupes à utiliser avec des appareils.
ms.custom:
- AdminSurgePortfolio
- okr_SMB
- commerce_licensing
search.appverid: MET150
ms.date: 03/17/2021
ms.openlocfilehash: c590c2d47699c4c3cbea4b5145bea9e7c9fc79ec
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52535661"
---
# <a name="manage-licenses-for-devices"></a><span data-ttu-id="50251-103">Gérer les licences pour les appareils</span><span class="sxs-lookup"><span data-stu-id="50251-103">Manage licenses for devices</span></span>

<span data-ttu-id="50251-104">Si vous avez Applications Microsoft 365 pour les grandes entreprises (appareil) ou Microsoft 365 Apps Éducation (appareil), vous pouvez attribuer des licences à des appareils à l’aide de groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="50251-104">If you have Microsoft 365 Apps for enterprise (device) or Microsoft 365 Apps for Education (device), you can assign licenses to devices by using Azure AD groups.</span></span> <span data-ttu-id="50251-105">Lorsqu’un appareil dispose d’une licence, toute personne qui l’utilise peut Applications Microsoft 365 pour les grandes entreprises (précédemment Office 365 ProPlus).</span><span class="sxs-lookup"><span data-stu-id="50251-105">When a device has a license, anyone who uses that device can use Microsoft 365 Apps for enterprise (previously named Office 365 ProPlus).</span></span> <span data-ttu-id="50251-106">Par exemple, supposons que vous avez 20 ordinateurs portables et tablettes utilisés par les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="50251-106">For example, let's say you have 20 laptops and tablets that are used by people in your organization.</span></span> <span data-ttu-id="50251-107">Lorsque vous attribuez une licence à chaque appareil, chaque personne qui se connecte à l’un des appareils utilise Applications Microsoft 365 pour les grandes entreprises sans avoir besoin de sa propre licence.</span><span class="sxs-lookup"><span data-stu-id="50251-107">When you assign a license to each device, each person who logs in to one of the devices uses Microsoft 365 Apps for enterprise without the need for their own license.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50251-108">Les licences basées sur l’appareil Applications Microsoft 365 pour les grandes entreprises sont disponibles uniquement sous la mesure d’une licence de modules de développement pour certains clients commerciaux et éducation.</span><span class="sxs-lookup"><span data-stu-id="50251-108">Device-based licensing for Microsoft 365 Apps for enterprise is available only as an add-on license for some commercial customers and some education customers.</span></span> <span data-ttu-id="50251-109">Pour les clients commerciaux, la licence *est Applications Microsoft 365 pour les grandes entreprises (appareil)* et est disponible uniquement par Accord Entreprise/Accord Entreprise abonnement.</span><span class="sxs-lookup"><span data-stu-id="50251-109">For commercial customers, the license is *Microsoft 365 Apps for enterprise (device)* and is available only through Enterprise Agreement/Enterprise Agreement Subscription.</span></span> <span data-ttu-id="50251-110">Pour les clients de l’éducation, la licence *est Microsoft 365 Apps éducation (appareil)* et est disponible uniquement par le biais de l’inscription pour les solutions d’éducation (EES).</span><span class="sxs-lookup"><span data-stu-id="50251-110">For education customers, the license is *Microsoft 365 Apps for Education (device)* and is available only through Enrollment for Education Solutions (EES).</span></span> <span data-ttu-id="50251-111">Pour plus d’informations, lisez le billet de blog sur la [disponibilité de l’éducation.](https://educationblog.microsoft.com/2019/08/attention-it-administrators-announcing-office-365-proplus-device-based-subscription-for-education)</span><span class="sxs-lookup"><span data-stu-id="50251-111">For more information, read the blog post on [education availability](https://educationblog.microsoft.com/2019/08/attention-it-administrators-announcing-office-365-proplus-device-based-subscription-for-education).</span></span> <span data-ttu-id="50251-112">Pour la disponibilité commerciale, contactez votre représentant de compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="50251-112">For commercial availability, contact your Microsoft account representative.</span></span>

<span data-ttu-id="50251-113">Pour commencer, vous créez un groupe dans Azure Active Directory centre d’administration, puis attribuez des appareils au groupe.</span><span class="sxs-lookup"><span data-stu-id="50251-113">To begin, you create a group in the Azure Active Directory admin center, and then assign devices to the group.</span></span> <span data-ttu-id="50251-114">Pour en savoir plus sur la gestion des licences d’appareils, notamment la configuration requise pour les appareils, les types de groupes que vous pouvez utiliser et comment configurer Applications Microsoft 365 pour les grandes entreprises pour utiliser la gestion des licences d’appareils, voir Licences basées sur les [appareils pour Applications Microsoft 365 pour les grandes entreprises](/deployoffice/device-based-licensing).</span><span class="sxs-lookup"><span data-stu-id="50251-114">To learn more about device licensing, including device requirements, what types of groups you can use, and how to configure Microsoft 365 Apps for enterprise to use device licensing, see [Device-based licensing for Microsoft 365 Apps for enterprise](/deployoffice/device-based-licensing).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50251-115">Vous devez être un administrateur global pour effectuer les tâches de cet article.</span><span class="sxs-lookup"><span data-stu-id="50251-115">You must be a Global admin to complete the tasks in this article.</span></span>

## <a name="assign-licenses-to-devices"></a><span data-ttu-id="50251-116">Attribuer des licences à des appareils</span><span class="sxs-lookup"><span data-stu-id="50251-116">Assign licenses to devices</span></span>

<span data-ttu-id="50251-117">Lorsque vous attribuez des licences à un groupe, vous attribuez des licences à tous les appareils du groupe.</span><span class="sxs-lookup"><span data-stu-id="50251-117">When you assign licenses to a group, you assign licenses to all devices within the group.</span></span> <span data-ttu-id="50251-118">Vous ne pouvez affecter qu’un seul abonnement à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="50251-118">You can only assign one subscription to any single group.</span></span>

1. <span data-ttu-id="50251-119">Dans le centre Microsoft 365'administration, allez sur la page  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation.</a></span><span class="sxs-lookup"><span data-stu-id="50251-119">In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="50251-120">Dans la page **Licences,** choisissez **Microsoft 365 Apps Éducation (appareil)** **ou Applications Microsoft 365 pour les grandes entreprises (appareil).**</span><span class="sxs-lookup"><span data-stu-id="50251-120">On the **Licenses** page, choose **Microsoft 365 Apps for Education (device)** or **Microsoft 365 Apps for enterprise (device)**.</span></span>
3. <span data-ttu-id="50251-121">Sur la page suivante, choisissez un abonnement, puis **sélectionnez Attribuer des licences.**</span><span class="sxs-lookup"><span data-stu-id="50251-121">On the next page, choose a subscription, then choose **Assign licenses**.</span></span>
4. <span data-ttu-id="50251-122">Dans le **volet Attribuer des licences** à un volet de groupe, commencez à taper un nom de groupe, puis choisissez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="50251-122">In the **Assign licenses to a group** pane, begin typing a group name, and then choose it from the results to add it to the list.</span></span>
5. <span data-ttu-id="50251-123">Choose **Assign,** then choose **Close**.</span><span class="sxs-lookup"><span data-stu-id="50251-123">Choose **Assign**, then choose **Close**.</span></span>

## <a name="unassign-licenses-from-devices"></a><span data-ttu-id="50251-124">Désattribuer des licences à des appareils</span><span class="sxs-lookup"><span data-stu-id="50251-124">Unassign licenses from devices</span></span>

<span data-ttu-id="50251-125">Lorsque vous désattribuez des licences à un groupe, vous supprimez les licences de tous les appareils du groupe.</span><span class="sxs-lookup"><span data-stu-id="50251-125">When you unassign licenses from a group, you remove the licenses from all devices within the group.</span></span> <span data-ttu-id="50251-126">Toutes les applications et leurs données associées sont ensuite en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="50251-126">All apps and their associated data are then read-only.</span></span>

1. <span data-ttu-id="50251-127">Dans le Centre d’administration, allez sur la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation.</a></span><span class="sxs-lookup"><span data-stu-id="50251-127">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="50251-128">Dans la page **Licences,** choisissez **Microsoft 365 Apps Éducation (appareil)** **ou Applications Microsoft 365 pour les grandes entreprises (appareil).**</span><span class="sxs-lookup"><span data-stu-id="50251-128">On the **Licenses** page, choose **Microsoft 365 Apps for Education (device)** or **Microsoft 365 Apps for enterprise (device)**.</span></span>
3. <span data-ttu-id="50251-129">Sur la page suivante, choisissez un abonnement, sélectionnez les trois points (autres actions), puis choisissez **Désattribuer des licences.**</span><span class="sxs-lookup"><span data-stu-id="50251-129">On the next page, choose a subscription, select the three dots (more actions), and then choose **Unassign licenses**.</span></span>
4. <span data-ttu-id="50251-130">In the **Unassign licenses** dialog box, choose **Unassign**.</span><span class="sxs-lookup"><span data-stu-id="50251-130">In the **Unassign licenses** dialog box, choose **Unassign**.</span></span>
