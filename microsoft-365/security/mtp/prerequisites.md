---
title: Conditions préalables pour Microsoft 365 Defender
description: En savoir plus sur la gestion des licences, la configuration matérielle et logicielle requise, ainsi que d’autres paramètres de configuration pour Microsoft 365 Defender
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
ms.openlocfilehash: 415cdb79a6aa9371ee2f07de579cfb2f873f1acb
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844775"
---
# <a name="microsoft-365-defender-prerequisites"></a><span data-ttu-id="435bf-104">Conditions préalables pour Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="435bf-104">Microsoft 365 Defender prerequisites</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="435bf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="435bf-105">**Applies to:**</span></span>
- <span data-ttu-id="435bf-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="435bf-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="435bf-107">Découvrez les licences et autres conditions requises pour la mise en service et l’utilisation de [Microsoft 365 Defender](microsoft-threat-protection.md).</span><span class="sxs-lookup"><span data-stu-id="435bf-107">Learn about licensing and other requirements for provisioning and using [Microsoft 365 Defender](microsoft-threat-protection.md).</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="435bf-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="435bf-108">Licensing requirements</span></span>
<span data-ttu-id="435bf-109">L’une de ces licences vous donne accès aux fonctionnalités de Microsoft 365 Defender dans le centre de sécurité Microsoft 365 sans frais supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="435bf-109">Any of these licenses gives you access to Microsoft 365 Defender features in Microsoft 365 security center without additional cost:</span></span>

- <span data-ttu-id="435bf-110">Microsoft 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="435bf-110">Microsoft 365 E5 or A5</span></span>
- <span data-ttu-id="435bf-111">Microsoft 365 E5 sécurité ou a5 sécurité</span><span class="sxs-lookup"><span data-stu-id="435bf-111">Microsoft 365 E5 Security or A5 Security</span></span>
- <span data-ttu-id="435bf-112">Windows 10 entreprise E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="435bf-112">Windows 10 Enterprise E5 or A5</span></span>
- <span data-ttu-id="435bf-113">Enterprise Mobility + Security (EMS) E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="435bf-113">Enterprise Mobility + Security (EMS) E5 or A5</span></span> 
- <span data-ttu-id="435bf-114">Office 365 E5 ou a5</span><span class="sxs-lookup"><span data-stu-id="435bf-114">Office 365 E5 or A5</span></span>
- <span data-ttu-id="435bf-115">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="435bf-115">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="435bf-116">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="435bf-116">Microsoft Defender for Identity</span></span> 
- <span data-ttu-id="435bf-117">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="435bf-117">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="435bf-118">Defender pour Office 365 (plan 2)</span><span class="sxs-lookup"><span data-stu-id="435bf-118">Defender for Office 365 (Plan 2)</span></span>

> [!NOTE]
> <span data-ttu-id="435bf-119">Les licences d’évaluation pour Office 365 ne fournissent actuellement pas d’accès à Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="435bf-119">Trial licenses for Office 365 currently do not provide access to Microsoft 365 Defender.</span></span>

<span data-ttu-id="435bf-120">Pour plus d’informations, [consultez les plans de services d’entreprise Microsoft 365](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="435bf-120">For more information, [view the Microsoft 365 Enterprise service plans](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span></span>

> <span data-ttu-id="435bf-121">Vous n’avez pas encore de licence ?</span><span class="sxs-lookup"><span data-stu-id="435bf-121">Don't have license yet?</span></span> [<span data-ttu-id="435bf-122">Essayez ou achetez un abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="435bf-122">Try or buy a Microsoft 365 subscription</span></span>](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide)

### <a name="check-your-existing--licenses"></a><span data-ttu-id="435bf-123">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="435bf-123">Check your existing  licenses</span></span>
<span data-ttu-id="435bf-124">Accédez au centre d’administration Microsoft 365 ([admin.Microsoft.com](https://admin.microsoft.com/)) pour afficher vos licences existantes.</span><span class="sxs-lookup"><span data-stu-id="435bf-124">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span></span> <span data-ttu-id="435bf-125">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="435bf-125">In the admin center, go to **Billing** > **Licenses**.</span></span>

>[!NOTE]
> <span data-ttu-id="435bf-126">Vous devez disposer du rôle d' **administrateur de facturation** ou de **lecteur global** [dans Azure ad](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour être en mesure d’afficher les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="435bf-126">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see license information.</span></span> <span data-ttu-id="435bf-127">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="435bf-127">If you encounter access problems, contact a global admin.</span></span>

## <a name="required-permissions"></a><span data-ttu-id="435bf-128">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="435bf-128">Required permissions</span></span>
<span data-ttu-id="435bf-129">Vous devez être **administrateur général** ou administrateur de **sécurité** dans Azure Active Directory pour activer Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="435bf-129">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft 365 Defender.</span></span> <span data-ttu-id="435bf-130">Pour obtenir la liste des rôles requis pour utiliser Microsoft 365 Defender et des informations sur la façon dont l’accès aux données est réglementé, consultez la rubrique [Managing Access to microsoft 365 Defender](mtp-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="435bf-130">For the list of roles required to use Microsoft 365 Defender and information on how access to data is regulated, read about [managing access to Microsoft 365 Defender](mtp-permissions.md).</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="435bf-131">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="435bf-131">Browser requirements</span></span>
<span data-ttu-id="435bf-132">Accédez à Microsoft 365 Defender dans le centre de sécurité Microsoft 365 à l’aide de Microsoft Edge, d’Internet Explorer 11 ou de n’importe quel navigateur Web HTML 5.</span><span class="sxs-lookup"><span data-stu-id="435bf-132">Access Microsoft 365 Defender in the Microsoft 365 security center using Microsoft Edge, Internet Explorer 11, or any HTML 5 compliant web browser.</span></span>

## <a name="availability-to-us-gcc-gcc-high-and-other-us-government-institutions"></a><span data-ttu-id="435bf-133">Disponibilité aux États-Unis GCC, GCC High et d’autres établissements gouvernementaux américains</span><span class="sxs-lookup"><span data-stu-id="435bf-133">Availability to US GCC, GCC High, and other US government institutions</span></span>
<span data-ttu-id="435bf-134">Actuellement, Microsoft 365 Defender n’est *pas* disponible pour :</span><span class="sxs-lookup"><span data-stu-id="435bf-134">Currently, Microsoft 365 Defender is *not* available to:</span></span>
- <span data-ttu-id="435bf-135">Cloud communautaire pour le gouvernement américain (GCC)</span><span class="sxs-lookup"><span data-stu-id="435bf-135">US Government Community Cloud (GCC)</span></span>
- <span data-ttu-id="435bf-136">Niveau supérieur du Cloud communautaire pour le gouvernement américain (GCC High)</span><span class="sxs-lookup"><span data-stu-id="435bf-136">US Government Community Cloud High (GCC High)</span></span>
- <span data-ttu-id="435bf-137">Ministère américain de la défense</span><span class="sxs-lookup"><span data-stu-id="435bf-137">US Department of Defense</span></span>
- <span data-ttu-id="435bf-138">Tous les établissements gouvernementaux américains avec des licences commerciales</span><span class="sxs-lookup"><span data-stu-id="435bf-138">All US government institutions with commercial licenses</span></span>

## <a name="related-topics"></a><span data-ttu-id="435bf-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="435bf-139">Related topics</span></span>
- [<span data-ttu-id="435bf-140">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="435bf-140">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="435bf-141">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="435bf-141">Turn on Microsoft 365 Defender</span></span>](mtp-enable.md)
- [<span data-ttu-id="435bf-142">Gérer l’accès et les autorisations</span><span class="sxs-lookup"><span data-stu-id="435bf-142">Manage access and permissions</span></span>](mtp-permissions.md)
