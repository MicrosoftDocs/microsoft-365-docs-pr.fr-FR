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
ms.openlocfilehash: c482e46cf51cbf11960c02663221df0c136b067c
ms.sourcegitcommit: fe4beef350ef9f39b1098755cff46fa2b8e7dc4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2020
ms.locfileid: "42857178"
---
# <a name="microsoft-threat-protection-prerequisites"></a><span data-ttu-id="99d13-104">Conditions préalables pour la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99d13-104">Microsoft Threat Protection prerequisites</span></span>

<span data-ttu-id="99d13-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="99d13-105">**Applies to:**</span></span>
- <span data-ttu-id="99d13-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99d13-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="99d13-107">Découvrez la gestion des licences, la configuration matérielle et logicielle requise, ainsi que d’autres paramètres de configuration pour mettre en service et utiliser la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="99d13-107">Learn about the licensing, hardware and software requirements, and other configuration settings to provision and use Microsoft Threat Protection.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="99d13-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="99d13-108">Licensing requirements</span></span>
<span data-ttu-id="99d13-109">Pour utiliser la protection contre les menaces Microsoft, vous avez besoin d’une licence unique ou d’une combinaison de licences.</span><span class="sxs-lookup"><span data-stu-id="99d13-109">To use Microsoft Threat Protection, you need either a single license or a combination of licenses.</span></span>

### <a name="single-license"></a><span data-ttu-id="99d13-110">Licence unique</span><span class="sxs-lookup"><span data-stu-id="99d13-110">Single license</span></span>
<span data-ttu-id="99d13-111">Vous pouvez utiliser l' *une* des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="99d13-111">You can use *one* of the following licenses:</span></span>

- <span data-ttu-id="99d13-112">Microsoft 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="99d13-112">Microsoft 365 E5 or A5</span></span>
- <span data-ttu-id="99d13-113">Microsoft 365 E5 sécurité ou a5 sécurité</span><span class="sxs-lookup"><span data-stu-id="99d13-113">Microsoft 365 E5 Security or A5 Security</span></span>

### <a name="combination-of-licenses"></a><span data-ttu-id="99d13-114">Combinaison de licences</span><span class="sxs-lookup"><span data-stu-id="99d13-114">Combination of licenses</span></span>
<span data-ttu-id="99d13-115">Vous pouvez également utiliser une combinaison de licences pour les abonnements E5 ou a5 à Office 365, *Enterprise Mobility + Security (EMS)* et Windows.</span><span class="sxs-lookup"><span data-stu-id="99d13-115">You can also use a combination of licenses for E5 or A5 subscriptions to Office 365, *Enterprise Mobility + Security (EMS)*, and Windows.</span></span> <span data-ttu-id="99d13-116">La combinaison de licences doit inclure *toutes* ces licences :</span><span class="sxs-lookup"><span data-stu-id="99d13-116">The license combination must include *all* of these licenses:</span></span>

- <span data-ttu-id="99d13-117">Office 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="99d13-117">Office 365 E5 or A5</span></span>
- <span data-ttu-id="99d13-118">*Enterprise Mobility + Security (EMS)* E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="99d13-118">*Enterprise Mobility + Security (EMS)* E5 or A5</span></span>
- <span data-ttu-id="99d13-119">Windows E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="99d13-119">Windows E5 or A5</span></span>

<span data-ttu-id="99d13-120">Pour plus d’informations, [consultez les plans de services d’entreprise Microsoft 365](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="99d13-120">For more information, [view the Microsoft 365 Enterprise service plans](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span></span>

> <span data-ttu-id="99d13-121">Vous n’avez pas encore de licence ?</span><span class="sxs-lookup"><span data-stu-id="99d13-121">Don't have license yet?</span></span> [<span data-ttu-id="99d13-122">Essayer ou acheter un abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="99d13-122">Try or buy a Microsoft 365 subscription</span></span>](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide)

### <a name="check-your-existing--licenses"></a><span data-ttu-id="99d13-123">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="99d13-123">Check your existing  licenses</span></span>
<span data-ttu-id="99d13-124">Accédez au centre d’administration Microsoft 365 ([admin.Microsoft.com](https://admin.microsoft.com/)) pour afficher vos licences existantes.</span><span class="sxs-lookup"><span data-stu-id="99d13-124">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span></span> <span data-ttu-id="99d13-125">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="99d13-125">In the admin center, go to **Billing** > **Licenses**.</span></span>

>[!NOTE]
> <span data-ttu-id="99d13-126">Vous devez disposer du rôle d' **administrateur de facturation** ou de **lecteur global** [dans Azure ad](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour être en mesure d’afficher les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="99d13-126">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see license information.</span></span> <span data-ttu-id="99d13-127">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="99d13-127">If you encounter access problems, contact a global admin.</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="99d13-128">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="99d13-128">Browser requirements</span></span>
<span data-ttu-id="99d13-129">Accédez à la protection contre les menaces Microsoft dans le centre de sécurité Microsoft 365 à l’aide de Microsoft Edge, d’Internet Explorer 11 ou de n’importe quel navigateur Web compatible HTML 5.</span><span class="sxs-lookup"><span data-stu-id="99d13-129">Access Microsoft Threat Protection in the Microsoft 365 security center using Microsoft Edge, Internet Explorer 11, or any HTML 5 compliant web browser.</span></span>

## <a name="microsoft-threat-protection-for-us-government-community-cloud-and-us-government-community-cloud-high-gcc-high-customers"></a><span data-ttu-id="99d13-130">Protection Microsoft contre les menaces pour les clients du nuage communautaire du gouvernement américain et du Cloud communautaire pour le secteur public américain (GCC High)</span><span class="sxs-lookup"><span data-stu-id="99d13-130">Microsoft Threat Protection for US Government Community Cloud and US Government Community Cloud High (GCC High) customers</span></span>
<span data-ttu-id="99d13-131">Actuellement, la protection Microsoft contre les menaces n’est pas disponible pour les clients des États-Unis GCC et GCC High.</span><span class="sxs-lookup"><span data-stu-id="99d13-131">Currently, Microsoft Threat Protection is not available to US GCC and GCC High customers.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="99d13-132">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="99d13-132">Related topics</span></span>
- [<span data-ttu-id="99d13-133">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99d13-133">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="99d13-134">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99d13-134">Turn on Microsoft Threat Protection</span></span>](mtp-enable.md)
