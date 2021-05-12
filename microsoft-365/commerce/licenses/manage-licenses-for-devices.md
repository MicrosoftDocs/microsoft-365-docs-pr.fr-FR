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
ms.openlocfilehash: 67bd0734953c64f51390aac949a7da477914c7b4
ms.sourcegitcommit: 967f64dfa1a05f31179c8316b96bfb7758a5d990
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52331657"
---
# <a name="manage-licenses-for-devices"></a><span data-ttu-id="e7c9c-103">Gérer les licences pour les appareils</span><span class="sxs-lookup"><span data-stu-id="e7c9c-103">Manage licenses for devices</span></span>

<span data-ttu-id="e7c9c-104">Si vous avez Microsoft 365 Apps pour entreprise (appareil) ou Microsoft 365 Apps pour Éducation (appareil), vous pouvez attribuer des licences à des appareils à l’aide de groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-104">If you have Microsoft 365 Apps for enterprise (device) or Microsoft 365 Apps for Education (device), you can assign licenses to devices by using Azure AD groups.</span></span> <span data-ttu-id="e7c9c-105">Lorsqu’un appareil dispose d’une licence, toute personne utilisant cet appareil peut utiliser les applications Microsoft 365 pour les entreprises (précédemment nommées Office 365 ProPlus).</span><span class="sxs-lookup"><span data-stu-id="e7c9c-105">When a device has a license, anyone who uses that device can use Microsoft 365 Apps for enterprise (previously named Office 365 ProPlus).</span></span> <span data-ttu-id="e7c9c-106">Par exemple, supposons que vous avez 20 ordinateurs portables et tablettes utilisés par les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-106">For example, let's say you have 20 laptops and tablets that are used by people in your organization.</span></span> <span data-ttu-id="e7c9c-107">Lorsque vous attribuez une licence à chaque appareil, chaque personne qui se connecte à l’un des appareils utilise Microsoft 365 Apps pour entreprise sans avoir besoin de sa propre licence.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-107">When you assign a license to each device, each person who logs in to one of the devices uses Microsoft 365 Apps for enterprise without the need for their own license.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7c9c-108">Les licences basées sur les appareils pour Microsoft 365 Apps pour entreprise sont disponibles uniquement en tant que licences de modules de développement pour certains clients commerciaux et certains clients de l’éducation.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-108">Device-based licensing for Microsoft 365 Apps for enterprise is available only as an add-on license for some commercial customers and some education customers.</span></span> <span data-ttu-id="e7c9c-109">Pour les clients commerciaux, la licence *est Microsoft 365 Apps for enterprise (appareil)* et n’est disponible que par le biais d’un abonnement contrat Entreprise/Contrat Entreprise.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-109">For commercial customers, the license is *Microsoft 365 Apps for enterprise (device)* and is available only through Enterprise Agreement/Enterprise Agreement Subscription.</span></span> <span data-ttu-id="e7c9c-110">Pour les clients de l’éducation, la licence *est Microsoft 365 Apps pour l’Éducation (appareil)* et est disponible uniquement par le biais de l’inscription pour les solutions d’éducation (EES).</span><span class="sxs-lookup"><span data-stu-id="e7c9c-110">For education customers, the license is *Microsoft 365 Apps for Education (device)* and is available only through Enrollment for Education Solutions (EES).</span></span> <span data-ttu-id="e7c9c-111">Pour plus d’informations, lisez le billet de blog sur la [disponibilité de l’éducation.](https://educationblog.microsoft.com/2019/08/attention-it-administrators-announcing-office-365-proplus-device-based-subscription-for-education)</span><span class="sxs-lookup"><span data-stu-id="e7c9c-111">For more information, read the blog post on [education availability](https://educationblog.microsoft.com/2019/08/attention-it-administrators-announcing-office-365-proplus-device-based-subscription-for-education).</span></span> <span data-ttu-id="e7c9c-112">Pour la disponibilité commerciale, contactez votre représentant de compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-112">For commercial availability, contact your Microsoft account representative.</span></span>

<span data-ttu-id="e7c9c-113">Pour commencer, vous créez un groupe dans le Centre d’administration Azure Active Directory, puis attribuez des appareils au groupe.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-113">To begin, you create a group in the Azure Active Directory admin center, and then assign devices to the group.</span></span> <span data-ttu-id="e7c9c-114">Pour en savoir plus sur la gestion des licences d’appareils, notamment la configuration requise pour les appareils, les types de groupes que vous pouvez utiliser et la configuration des applications Microsoft 365 pour les entreprises afin d’utiliser la gestion des licences d’appareils, voir Licences basées sur les appareils pour [Microsoft 365 Apps for enterprise.](/deployoffice/device-based-licensing)</span><span class="sxs-lookup"><span data-stu-id="e7c9c-114">To learn more about device licensing, including device requirements, what types of groups you can use, and how to configure Microsoft 365 Apps for enterprise to use device licensing, see [Device-based licensing for Microsoft 365 Apps for enterprise](/deployoffice/device-based-licensing).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7c9c-115">Vous devez être un administrateur global pour effectuer les tâches de cet article.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-115">You must be a Global admin to complete the tasks in this article.</span></span>

## <a name="assign-licenses-to-devices"></a><span data-ttu-id="e7c9c-116">Attribuer des licences à des appareils</span><span class="sxs-lookup"><span data-stu-id="e7c9c-116">Assign licenses to devices</span></span>

<span data-ttu-id="e7c9c-117">Lorsque vous attribuez des licences à un groupe, vous attribuez des licences à tous les appareils du groupe.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-117">When you assign licenses to a group, you assign licenses to all devices within the group.</span></span> <span data-ttu-id="e7c9c-118">Vous ne pouvez affecter qu’un seul abonnement à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-118">You can only assign one subscription to any single group.</span></span>

1. <span data-ttu-id="e7c9c-119">Dans le Centre d’administration Microsoft 365, allez sur la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation.</a></span><span class="sxs-lookup"><span data-stu-id="e7c9c-119">In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="e7c9c-120">Dans la page **Licences,** choisissez **Microsoft 365 Apps pour l’Éducation (appareil)** ou **Microsoft 365 Apps pour entreprise (appareil).**</span><span class="sxs-lookup"><span data-stu-id="e7c9c-120">On the **Licenses** page, choose **Microsoft 365 Apps for Education (device)** or **Microsoft 365 Apps for enterprise (device)**.</span></span>
3. <span data-ttu-id="e7c9c-121">Sur la page suivante, choisissez un abonnement, puis **sélectionnez Attribuer des licences.**</span><span class="sxs-lookup"><span data-stu-id="e7c9c-121">On the next page, choose a subscription, then choose **Assign licenses**.</span></span>
4. <span data-ttu-id="e7c9c-122">Dans le **volet Attribuer des licences** à un volet de groupe, commencez à taper un nom de groupe, puis choisissez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-122">In the **Assign licenses to a group** pane, begin typing a group name, and then choose it from the results to add it to the list.</span></span>
5. <span data-ttu-id="e7c9c-123">Choose **Assign,** then choose **Close**.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-123">Choose **Assign**, then choose **Close**.</span></span>

## <a name="unassign-licenses-from-devices"></a><span data-ttu-id="e7c9c-124">Désattribuer des licences à des appareils</span><span class="sxs-lookup"><span data-stu-id="e7c9c-124">Unassign licenses from devices</span></span>

<span data-ttu-id="e7c9c-125">Lorsque vous désattribuez des licences à un groupe, vous supprimez les licences de tous les appareils du groupe.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-125">When you unassign licenses from a group, you remove the licenses from all devices within the group.</span></span> <span data-ttu-id="e7c9c-126">Toutes les applications et leurs données associées sont ensuite en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-126">All apps and their associated data are then read-only.</span></span>

1. <span data-ttu-id="e7c9c-127">Dans le Centre d’administration, allez sur la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences de facturation.</a></span><span class="sxs-lookup"><span data-stu-id="e7c9c-127">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="e7c9c-128">Dans la page **Licences,** choisissez **Microsoft 365 Apps pour l’Éducation (appareil)** ou **Microsoft 365 Apps pour entreprise (appareil).**</span><span class="sxs-lookup"><span data-stu-id="e7c9c-128">On the **Licenses** page, choose **Microsoft 365 Apps for Education (device)** or **Microsoft 365 Apps for enterprise (device)**.</span></span>
3. <span data-ttu-id="e7c9c-129">On the next page, choose a subscription, choose **More actions,** then choose **Unassign licenses**.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-129">On the next page, choose a subscription, choose **More actions**, then choose **Unassign licenses**.</span></span>
4. <span data-ttu-id="e7c9c-130">In the **Unassign licenses** dialog box, choose **Unassign**.</span><span class="sxs-lookup"><span data-stu-id="e7c9c-130">In the **Unassign licenses** dialog box, choose **Unassign**.</span></span>
