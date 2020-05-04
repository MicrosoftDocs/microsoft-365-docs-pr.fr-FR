---
title: Conditions préalables pour la Protection Microsoft contre les menaces
description: En savoir plus sur les exigences en matière de licences, de matériel et de logiciels, ainsi que sur les autres paramètres de configuration de la Protection Microsoft contre les menaces.
keywords: conditions requises, configuration matérielle, logicielle, navigateur, MTP, M365, licence, E5, a5, EMS, acheter
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: dfc2136f04ed128fc655386c6eef7b91c5e5ef3a
ms.sourcegitcommit: bd8d55f82ca008af1b93a9bb4d1545f68e8188ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2020
ms.locfileid: "44011271"
---
# <a name="microsoft-threat-protection-prerequisites"></a><span data-ttu-id="cd1e2-104">Conditions préalables pour la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cd1e2-104">Microsoft Threat Protection prerequisites</span></span>

<span data-ttu-id="cd1e2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cd1e2-105">**Applies to:**</span></span>
- <span data-ttu-id="cd1e2-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cd1e2-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="cd1e2-107">Découvrez la gestion des licences, la configuration matérielle et logicielle requise, ainsi que d’autres paramètres de configuration pour mettre en service et utiliser la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-107">Learn about the licensing, hardware and software requirements, and other configuration settings to provision and use Microsoft Threat Protection.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="cd1e2-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="cd1e2-108">Licensing requirements</span></span>

>[!IMPORTANT]
><span data-ttu-id="cd1e2-109">À partir du 3 mai 2020, Microsoft mettra progressivement en place de nouvelles expériences optimisées en matière de licences et [d’activation de la protection contre les menaces Microsoft](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="cd1e2-109">Starting May 3, 2020, Microsoft will gradually roll out new, optimized experiences around licensing requirements and [turning on Microsoft Threat Protection](mtp-enable.md).</span></span> <span data-ttu-id="cd1e2-110">Pendant plusieurs semaines pendant cette période, certains clients commencent à voir les modifications apportées à leurs expériences de portail.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-110">For several weeks during this period, some customers will start to see changes to their portal experiences.</span></span> <span data-ttu-id="cd1e2-111">Les informations sur les nouvelles expériences sont marquées **nouvelle expérience** dans cet article.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-111">Information about the new experiences are marked **New experience** in this article.</span></span>

<span data-ttu-id="cd1e2-112">Pour utiliser la protection contre les menaces Microsoft, vous avez besoin d’une licence unique ou d’une combinaison de licences.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-112">To use Microsoft Threat Protection, you need either a single license or a combination of licenses.</span></span> <span data-ttu-id="cd1e2-113">Ces licences ou combinaisons de licences vous donnent accès aux fonctionnalités de protection contre les menaces de Microsoft sans frais supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-113">These licenses or license combinations give you access to Microsoft Threat Protection features without additional cost.</span></span>

### <a name="single-license"></a><span data-ttu-id="cd1e2-114">Licence unique</span><span class="sxs-lookup"><span data-stu-id="cd1e2-114">Single license</span></span>
<span data-ttu-id="cd1e2-115">Vous pouvez utiliser l' *une* des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd1e2-115">You can use *one* of the following licenses:</span></span>

- <span data-ttu-id="cd1e2-116">Microsoft 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-116">Microsoft 365 E5 or A5</span></span>
- <span data-ttu-id="cd1e2-117">Microsoft 365 E5 sécurité ou a5 sécurité</span><span class="sxs-lookup"><span data-stu-id="cd1e2-117">Microsoft 365 E5 Security or A5 Security</span></span>

### <a name="combination-of-licenses"></a><span data-ttu-id="cd1e2-118">Combinaison de licences</span><span class="sxs-lookup"><span data-stu-id="cd1e2-118">Combination of licenses</span></span>
<span data-ttu-id="cd1e2-119">Vous pouvez également utiliser une combinaison de licences pour les abonnements E5 ou a5 à Office 365, *Enterprise Mobility + Security (EMS)* et Windows.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-119">You can also use a combination of licenses for E5 or A5 subscriptions to Office 365, *Enterprise Mobility + Security (EMS)*, and Windows.</span></span> <span data-ttu-id="cd1e2-120">La combinaison de licences doit inclure *toutes* ces licences :</span><span class="sxs-lookup"><span data-stu-id="cd1e2-120">The license combination must include *all* of these licenses:</span></span>

- <span data-ttu-id="cd1e2-121">Office 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-121">Office 365 E5 or A5</span></span>
- <span data-ttu-id="cd1e2-122">*Enterprise Mobility + Security (EMS)* E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-122">*Enterprise Mobility + Security (EMS)* E5 or A5</span></span>
- <span data-ttu-id="cd1e2-123">Windows 10 entreprise E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-123">Windows 10 Enterprise E5 or A5</span></span>

<span data-ttu-id="cd1e2-124">Pour plus d’informations, [consultez les plans de services d’entreprise Microsoft 365](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="cd1e2-124">For more information, [view the Microsoft 365 Enterprise service plans](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span></span>

> <span data-ttu-id="cd1e2-125">Vous n’avez pas encore de licence ?</span><span class="sxs-lookup"><span data-stu-id="cd1e2-125">Don't have license yet?</span></span> [<span data-ttu-id="cd1e2-126">Essayez ou achetez un abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cd1e2-126">Try or buy a Microsoft 365 subscription</span></span>](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide)


<span data-ttu-id="cd1e2-127">**Nouvelle expérience :** À partir du 3 mai, 2020, les clients recevront progressivement les modifications apportées à cette expérience.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-127">**New experience:** Starting May 3, 2020, customers will gradually receive changes to this experience.</span></span> <span data-ttu-id="cd1e2-128">Pour les personnes ayant la nouvelle expérience, l’option d’activation de Microsoft Threat Protection sera disponible pour *tous* les clients disposant des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd1e2-128">For those with the new experience, the option to turn on Microsoft Threat Protection will be available to *all* customers with any of the following licenses:</span></span>

- <span data-ttu-id="cd1e2-129">Microsoft 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-129">Microsoft 365 E5 or A5</span></span>
- <span data-ttu-id="cd1e2-130">Microsoft 365 E5 sécurité ou a5 sécurité</span><span class="sxs-lookup"><span data-stu-id="cd1e2-130">Microsoft 365 E5 Security or A5 Security</span></span>
- <span data-ttu-id="cd1e2-131">Windows 10 entreprise E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-131">Windows 10 Enterprise E5 or A5</span></span>
- <span data-ttu-id="cd1e2-132">Enterprise Mobility + Security (EMS) E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-132">Enterprise Mobility + Security (EMS) E5 or A5</span></span> 
- <span data-ttu-id="cd1e2-133">Office 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="cd1e2-133">Office 365 E5 or A5</span></span>
- <span data-ttu-id="cd1e2-134">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cd1e2-134">Microsoft Defender Advanced Threat Protection</span></span> 
- <span data-ttu-id="cd1e2-135">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="cd1e2-135">Azure Advanced Threat Protection</span></span> 
- <span data-ttu-id="cd1e2-136">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cd1e2-136">Microsoft Cloud App Security</span></span> 
- <span data-ttu-id="cd1e2-137">Office 365 – Protection avancée contre les menaces (plan 2)</span><span class="sxs-lookup"><span data-stu-id="cd1e2-137">Office 365 Advanced Threat Protection (Plan 2)</span></span> 

### <a name="check-your-existing--licenses"></a><span data-ttu-id="cd1e2-138">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="cd1e2-138">Check your existing  licenses</span></span>
<span data-ttu-id="cd1e2-139">Accédez au centre d’administration Microsoft 365 ([admin.Microsoft.com](https://admin.microsoft.com/)) pour afficher vos licences existantes.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-139">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span></span> <span data-ttu-id="cd1e2-140">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-140">In the admin center, go to **Billing** > **Licenses**.</span></span>

>[!NOTE]
> <span data-ttu-id="cd1e2-141">Vous devez disposer du rôle d' **administrateur de facturation** ou de **lecteur global** [dans Azure ad](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour être en mesure d’afficher les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-141">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see license information.</span></span> <span data-ttu-id="cd1e2-142">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-142">If you encounter access problems, contact a global admin.</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="cd1e2-143">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="cd1e2-143">Browser requirements</span></span>
<span data-ttu-id="cd1e2-144">Accédez à la protection contre les menaces Microsoft dans le centre de sécurité Microsoft 365 à l’aide de Microsoft Edge, d’Internet Explorer 11 ou de n’importe quel navigateur Web compatible HTML 5.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-144">Access Microsoft Threat Protection in the Microsoft 365 security center using Microsoft Edge, Internet Explorer 11, or any HTML 5 compliant web browser.</span></span>

## <a name="microsoft-threat-protection-for-us-government-community-cloud-and-us-government-community-cloud-high-gcc-high-customers"></a><span data-ttu-id="cd1e2-145">Protection Microsoft contre les menaces pour les clients du nuage communautaire du gouvernement américain et du Cloud communautaire pour le secteur public américain (GCC High)</span><span class="sxs-lookup"><span data-stu-id="cd1e2-145">Microsoft Threat Protection for US Government Community Cloud and US Government Community Cloud High (GCC High) customers</span></span>
<span data-ttu-id="cd1e2-146">Actuellement, la protection Microsoft contre les menaces n’est pas disponible pour les clients des États-Unis GCC et GCC High.</span><span class="sxs-lookup"><span data-stu-id="cd1e2-146">Currently, Microsoft Threat Protection is not available to US GCC and GCC High customers.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="cd1e2-147">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="cd1e2-147">Related topics</span></span>
- [<span data-ttu-id="cd1e2-148">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cd1e2-148">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="cd1e2-149">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cd1e2-149">Turn on Microsoft Threat Protection</span></span>](mtp-enable.md)
