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
ms.openlocfilehash: c7c747d5f4d2408b717bf16068d23c7882c2d667
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42242323"
---
# <a name="manage-licenses-for-devices"></a><span data-ttu-id="ad04f-103">Gérer les licences pour les appareils</span><span class="sxs-lookup"><span data-stu-id="ad04f-103">Manage licenses for devices</span></span>

<span data-ttu-id="ad04f-104">Si vous disposez d’Office 365 ProPlus for Education (Device), vous pouvez attribuer des licences à des appareils à l’aide de groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ad04f-104">If you have Office 365 ProPlus for Education (device), you can assign licenses to devices by using Azure AD groups.</span></span> <span data-ttu-id="ad04f-105">Lorsqu’un appareil dispose d’une licence, quiconque utilise ce périphérique peut utiliser Office 365.</span><span class="sxs-lookup"><span data-stu-id="ad04f-105">When a device has a license, anyone who uses that device can use Office 365.</span></span> <span data-ttu-id="ad04f-106">Par exemple, imaginons que vous avez 20 ordinateurs portables et tablettes utilisés par les employés de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ad04f-106">For example, let’s say you have 20 laptops and tablets that are used by people in your organization.</span></span> <span data-ttu-id="ad04f-107">Lorsque vous attribuez une licence à chaque appareil, chaque personne qui se connecte à l’un des appareils utilise Office 365 sans qu’il soit nécessaire de posséder sa propre licence.</span><span class="sxs-lookup"><span data-stu-id="ad04f-107">When you assign a license to each device, each person who logs in to one of the devices uses Office 365 without the need for their own license.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad04f-108">Office 365 ProPlus for Education (Device) est uniquement disponible pour les clients de licence en volume a3 et a5.</span><span class="sxs-lookup"><span data-stu-id="ad04f-108">Office 365 ProPlus for Education (device) is only available to Education A3 and A5 volume licensing customers.</span></span>

<span data-ttu-id="ad04f-109">Pour commencer, créez un groupe dans le centre d’administration Azure Active Directory, puis affectez des appareils au groupe.</span><span class="sxs-lookup"><span data-stu-id="ad04f-109">To begin, you create a group in the Azure Active Directory admin center, and then assign devices to the group.</span></span> <span data-ttu-id="ad04f-110">Pour en savoir plus sur les licences d’appareil, notamment les exigences en matière de périphériques, les types de groupes que vous pouvez utiliser et la procédure de configuration d’Office 365 ProPlus pour utiliser les licences d’appareil, voir [device licensing for Office 365 ProPlus for Education Customers](https://go.microsoft.com/fwlink/p/?linkid=2094216).</span><span class="sxs-lookup"><span data-stu-id="ad04f-110">To learn more about device licensing, including device requirements, what types of groups you can use, and how to configure Office 365 ProPlus to use device licensing, see [Device licensing for Office 365 ProPlus for Education customers](https://go.microsoft.com/fwlink/p/?linkid=2094216).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad04f-111">Vous devez être un administrateur général pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="ad04f-111">You must be a Global admin to complete the tasks in this article.</span></span>

## <a name="assign-licenses-to-devices"></a><span data-ttu-id="ad04f-112">Attribuer des licences à des appareils</span><span class="sxs-lookup"><span data-stu-id="ad04f-112">Assign licenses to devices</span></span>

<span data-ttu-id="ad04f-113">Lorsque vous attribuez des licences à un groupe, vous attribuez des licences à tous les périphériques au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="ad04f-113">When you assign licenses to a group, you assign licenses to all devices within the group.</span></span> <span data-ttu-id="ad04f-114">Vous ne pouvez attribuer qu’un seul abonnement à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ad04f-114">You can only assign one subscription to any single group.</span></span>

1. <span data-ttu-id="ad04f-115">Dans le centre d’administration Microsoft 365, accédez à la page<a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">licences</a> de **facturation** > .</span><span class="sxs-lookup"><span data-stu-id="ad04f-115">In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="ad04f-116">Sur la page **licences** , sélectionnez **Office 365 ProPlus for Education (Device)**.</span><span class="sxs-lookup"><span data-stu-id="ad04f-116">On the **Licenses** page, choose **Office 365 ProPlus for Education (device)**.</span></span>
3. <span data-ttu-id="ad04f-117">Sur la page **Office 365 ProPlus for Education (Device)** , sélectionnez un abonnement, puis choisissez **attribuer des licences**.</span><span class="sxs-lookup"><span data-stu-id="ad04f-117">On the **Office 365 ProPlus for Education (device)** page, choose a subscription, then choose **Assign licenses**.</span></span>
4. <span data-ttu-id="ad04f-118">Dans le volet **attribuer des licences à un groupe** , commencez à taper un nom de groupe, puis sélectionnez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="ad04f-118">In the **Assign licenses to a group** pane, begin typing a group name, and then choose it from the results to add it to the list.</span></span>
6. <span data-ttu-id="ad04f-119">Sélectionnez **affecter**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ad04f-119">Choose **Assign**, then choose **Close**.</span></span>

## <a name="unassign-licenses-from-devices"></a><span data-ttu-id="ad04f-120">Désaffecter les licences des appareils</span><span class="sxs-lookup"><span data-stu-id="ad04f-120">Unassign licenses from devices</span></span>

<span data-ttu-id="ad04f-121">Lorsque vous désaffectez des licences à un groupe, vous supprimez les licences de tous les périphériques au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="ad04f-121">When you unassign licenses from a group, you remove the licenses from all devices within the group.</span></span> <span data-ttu-id="ad04f-122">Toutes les applications et leurs données associées sont alors en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ad04f-122">All apps and their associated data are then read-only.</span></span>

1. <span data-ttu-id="ad04f-123">Dans le centre d’administration, accédez à la page<a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">licences</a> de **facturation** > .</span><span class="sxs-lookup"><span data-stu-id="ad04f-123">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="ad04f-124">Sur la page **licences** , sélectionnez **Office 365 ProPlus for Education (Device)**.</span><span class="sxs-lookup"><span data-stu-id="ad04f-124">On the **Licenses** page, choose **Office 365 ProPlus for Education (device)**.</span></span>
3. <span data-ttu-id="ad04f-125">Sur la page **Office 365 ProPlus for Education (appareil)** , sélectionnez un abonnement, sélectionnez **autres actions**, puis **désaffecter les licences**.</span><span class="sxs-lookup"><span data-stu-id="ad04f-125">On the **Office 365 ProPlus for Education (device)** page, choose a subscription, choose **More actions**, then choose **Unassign licenses**.</span></span>
5. <span data-ttu-id="ad04f-126">Dans la boîte de dialogue **Annuler l’attribution des licences** , sélectionnez Annuler l' **affectation**.</span><span class="sxs-lookup"><span data-stu-id="ad04f-126">In the **Unassign licenses** dialog box, choose **Unassign**.</span></span>