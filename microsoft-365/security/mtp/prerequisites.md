---
title: Conditions préalables de Microsoft 365 Defender
description: En savoir plus sur les licences, la configuration matérielle et logicielle requise et d’autres paramètres de configuration pour Microsoft 365 Defender
keywords: configuration requise, conditions préalables, matériel, logiciel, navigateur, MTP, M365, licence, E5, A5, EMS, achat
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: ee1777debdb91a6ac73737db2db48e434ed3e2e2
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930089"
---
# <a name="microsoft-365-defender-prerequisites"></a><span data-ttu-id="d1f34-104">Conditions préalables de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d1f34-104">Microsoft 365 Defender prerequisites</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="d1f34-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d1f34-105">**Applies to:**</span></span>
- <span data-ttu-id="d1f34-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d1f34-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="d1f34-107">Découvrez les licences et autres conditions requises pour l’approvisionnement et l’utilisation [de Microsoft 365 Defender.](microsoft-threat-protection.md)</span><span class="sxs-lookup"><span data-stu-id="d1f34-107">Learn about licensing and other requirements for provisioning and using [Microsoft 365 Defender](microsoft-threat-protection.md).</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="d1f34-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="d1f34-108">Licensing requirements</span></span>
<span data-ttu-id="d1f34-109">L’une de ces licences vous donne accès aux fonctionnalités de Microsoft 365 Defender dans le Centre de sécurité Microsoft 365 sans frais supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="d1f34-109">Any of these licenses gives you access to Microsoft 365 Defender features in Microsoft 365 security center without additional cost:</span></span>

- <span data-ttu-id="d1f34-110">Microsoft 365 E5 ou A5</span><span class="sxs-lookup"><span data-stu-id="d1f34-110">Microsoft 365 E5 or A5</span></span>
- <span data-ttu-id="d1f34-111">Sécurité Microsoft 365 E5 ou sécurité A5</span><span class="sxs-lookup"><span data-stu-id="d1f34-111">Microsoft 365 E5 Security or A5 Security</span></span>
- <span data-ttu-id="d1f34-112">Windows 10 Entreprise E5 ou A5</span><span class="sxs-lookup"><span data-stu-id="d1f34-112">Windows 10 Enterprise E5 or A5</span></span>
- <span data-ttu-id="d1f34-113">Enterprise Mobility + Security (EMS) E5 ou A5</span><span class="sxs-lookup"><span data-stu-id="d1f34-113">Enterprise Mobility + Security (EMS) E5 or A5</span></span> 
- <span data-ttu-id="d1f34-114">Office 365 E5 ou A5</span><span class="sxs-lookup"><span data-stu-id="d1f34-114">Office 365 E5 or A5</span></span>
- <span data-ttu-id="d1f34-115">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d1f34-115">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="d1f34-116">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="d1f34-116">Microsoft Defender for Identity</span></span> 
- <span data-ttu-id="d1f34-117">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d1f34-117">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="d1f34-118">Defender pour Office 365 (Plan 2)</span><span class="sxs-lookup"><span data-stu-id="d1f34-118">Defender for Office 365 (Plan 2)</span></span>

> [!NOTE]
> <span data-ttu-id="d1f34-119">Les licences d’essai pour Office 365 ne fournissent actuellement pas d’accès à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="d1f34-119">Trial licenses for Office 365 currently do not provide access to Microsoft 365 Defender.</span></span>

<span data-ttu-id="d1f34-120">Pour plus d’informations, consultez les plans de [service Microsoft 365 Entreprise.](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise)</span><span class="sxs-lookup"><span data-stu-id="d1f34-120">For more information, [view the Microsoft 365 Enterprise service plans](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span></span>

> <span data-ttu-id="d1f34-121">Vous n’avez pas encore de licence ?</span><span class="sxs-lookup"><span data-stu-id="d1f34-121">Don't have license yet?</span></span> [<span data-ttu-id="d1f34-122">Essayez ou achetez un abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d1f34-122">Try or buy a Microsoft 365 subscription</span></span>](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide)

### <a name="check-your-existing--licenses"></a><span data-ttu-id="d1f34-123">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="d1f34-123">Check your existing  licenses</span></span>
<span data-ttu-id="d1f34-124">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span><span class="sxs-lookup"><span data-stu-id="d1f34-124">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span></span> <span data-ttu-id="d1f34-125">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="d1f34-125">In the admin center, go to **Billing** > **Licenses**.</span></span>

>[!NOTE]
> <span data-ttu-id="d1f34-126">Vous devez avoir le  rôle d’administrateur de facturation ou de lecteur **global** dans [Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour pouvoir voir les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="d1f34-126">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see license information.</span></span> <span data-ttu-id="d1f34-127">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="d1f34-127">If you encounter access problems, contact a global admin.</span></span>

## <a name="required-permissions"></a><span data-ttu-id="d1f34-128">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="d1f34-128">Required permissions</span></span>
<span data-ttu-id="d1f34-129">Vous devez être administrateur **général ou** **administrateur** de sécurité dans Azure Active Directory pour activer Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="d1f34-129">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft 365 Defender.</span></span> <span data-ttu-id="d1f34-130">Pour obtenir la liste des rôles requis pour utiliser Microsoft 365 Defender et des informations sur la façon dont l’accès aux données est réglementé, voir la gestion de l’accès à [Microsoft 365 Defender.](mtp-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="d1f34-130">For the list of roles required to use Microsoft 365 Defender and information on how access to data is regulated, read about [managing access to Microsoft 365 Defender](mtp-permissions.md).</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="d1f34-131">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="d1f34-131">Browser requirements</span></span>
<span data-ttu-id="d1f34-132">Accédez à Microsoft 365 Defender dans le Centre de sécurité Microsoft 365 à l’aide de Microsoft Edge, d’Internet Explorer 11 ou de tout navigateur web conforme HTML 5.</span><span class="sxs-lookup"><span data-stu-id="d1f34-132">Access Microsoft 365 Defender in the Microsoft 365 security center using Microsoft Edge, Internet Explorer 11, or any HTML 5 compliant web browser.</span></span>

## <a name="availability-to-us-gcc-gcc-high-and-other-us-government-institutions"></a><span data-ttu-id="d1f34-133">Disponibilité pour LES ÉTATS-UNIS GCC, GCC High et d’autres institutions gouvernementales des États-Unis</span><span class="sxs-lookup"><span data-stu-id="d1f34-133">Availability to US GCC, GCC High, and other US government institutions</span></span>
<span data-ttu-id="d1f34-134">Actuellement, Microsoft 365 Defender *n’est pas* disponible pour :</span><span class="sxs-lookup"><span data-stu-id="d1f34-134">Currently, Microsoft 365 Defender is *not* available to:</span></span>
- <span data-ttu-id="d1f34-135">Cloud communautaire du gouvernement américain (GCC)</span><span class="sxs-lookup"><span data-stu-id="d1f34-135">US Government Community Cloud (GCC)</span></span>
- <span data-ttu-id="d1f34-136">Cloud communautaire du gouvernement américain élevé (GCC High)</span><span class="sxs-lookup"><span data-stu-id="d1f34-136">US Government Community Cloud High (GCC High)</span></span>
- <span data-ttu-id="d1f34-137">Département de la Défense des États-Unis</span><span class="sxs-lookup"><span data-stu-id="d1f34-137">US Department of Defense</span></span>
- <span data-ttu-id="d1f34-138">Toutes les institutions gouvernementales américaines titulaires de licences commerciales</span><span class="sxs-lookup"><span data-stu-id="d1f34-138">All US government institutions with commercial licenses</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1f34-139">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="d1f34-139">Related topics</span></span>
- [<span data-ttu-id="d1f34-140">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d1f34-140">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="d1f34-141">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d1f34-141">Turn on Microsoft 365 Defender</span></span>](mtp-enable.md)
- [<span data-ttu-id="d1f34-142">Gérer l’accès et les autorisations</span><span class="sxs-lookup"><span data-stu-id="d1f34-142">Manage access and permissions</span></span>](mtp-permissions.md)
