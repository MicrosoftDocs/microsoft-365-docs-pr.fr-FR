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
ms.openlocfilehash: 2b653575e9e79ffe3448f622ca5be2cef37999dd
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2020
ms.locfileid: "42633952"
---
# <a name="microsoft-threat-protection-prerequisites"></a><span data-ttu-id="e2f85-104">Conditions préalables pour la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e2f85-104">Microsoft Threat Protection prerequisites</span></span>

<span data-ttu-id="e2f85-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e2f85-105">**Applies to:**</span></span>
- <span data-ttu-id="e2f85-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e2f85-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="e2f85-107">Découvrez la gestion des licences, la configuration matérielle et logicielle requise, ainsi que d’autres paramètres de configuration pour mettre en service et utiliser la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2f85-107">Learn about the licensing, hardware and software requirements, and other configuration settings to provision and use Microsoft Threat Protection.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="e2f85-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="e2f85-108">Licensing requirements</span></span>
<span data-ttu-id="e2f85-109">Pour utiliser Microsoft Threat Protection, vous avez besoin de l' *une* des licences ou de la combinaison de licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2f85-109">To use Microsoft Threat Protection, you need *one* of the following licenses or combination of licenses:</span></span>

- <span data-ttu-id="e2f85-110">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="e2f85-110">Microsoft 365 E5</span></span>
- <span data-ttu-id="e2f85-111">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="e2f85-111">Microsoft 365 E5 Security</span></span>
- <span data-ttu-id="e2f85-112">Office 365 E5 et « Enterprise Mobility + Security E5 (EMS E5) » et Windows E5</span><span class="sxs-lookup"><span data-stu-id="e2f85-112">Office 365 E5 and "Enterprise Mobility + Security E5 (EMS E5)" and Windows E5</span></span>
- <span data-ttu-id="e2f85-113">Microsoft 365 A5</span><span class="sxs-lookup"><span data-stu-id="e2f85-113">Microsoft 365 A5</span></span>

<span data-ttu-id="e2f85-114">Pour plus d’informations, [consultez les plans de services d’entreprise Microsoft 365](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="e2f85-114">For more information, [view the Microsoft 365 Enterprise service plans](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span></span>

> <span data-ttu-id="e2f85-115">Vous n’avez pas encore de licence ?</span><span class="sxs-lookup"><span data-stu-id="e2f85-115">Don't have license yet?</span></span> [<span data-ttu-id="e2f85-116">Essayer ou acheter un abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e2f85-116">Try or buy a Microsoft 365 subscription</span></span>](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide)

### <a name="check-your-existing--licenses"></a><span data-ttu-id="e2f85-117">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="e2f85-117">Check your existing  licenses</span></span>
<span data-ttu-id="e2f85-118">Accédez au centre d’administration Microsoft 365 ([admin.Microsoft.com](https://admin.microsoft.com/)) pour afficher vos licences existantes.</span><span class="sxs-lookup"><span data-stu-id="e2f85-118">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span></span> <span data-ttu-id="e2f85-119">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="e2f85-119">In the admin center, go to **Billing** > **Licenses**.</span></span>

>[!NOTE]
> <span data-ttu-id="e2f85-120">Vous devez disposer du rôle d' **administrateur de facturation** ou de **lecteur global** [dans Azure ad](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour être en mesure d’afficher les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="e2f85-120">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see license information.</span></span> <span data-ttu-id="e2f85-121">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="e2f85-121">If you encounter access problems, contact a global admin.</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="e2f85-122">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="e2f85-122">Browser requirements</span></span>
<span data-ttu-id="e2f85-123">Accédez à la protection contre les menaces Microsoft dans le centre de sécurité Microsoft 365 à l’aide de Microsoft Edge, d’Internet Explorer 11 ou de n’importe quel navigateur Web compatible HTML 5.</span><span class="sxs-lookup"><span data-stu-id="e2f85-123">Access Microsoft Threat Protection in the Microsoft 365 security center using Microsoft Edge, Internet Explorer 11, or any HTML 5 compliant web browser.</span></span>

## <a name="microsoft-threat-protection-for-us-government-community-cloud-and-us-government-community-cloud-high-gcc-high-customers"></a><span data-ttu-id="e2f85-124">Protection Microsoft contre les menaces pour les clients du nuage communautaire du gouvernement américain et du Cloud communautaire pour le secteur public américain (GCC High)</span><span class="sxs-lookup"><span data-stu-id="e2f85-124">Microsoft Threat Protection for US Government Community Cloud and US Government Community Cloud High (GCC High) customers</span></span>
<span data-ttu-id="e2f85-125">Actuellement, la protection Microsoft contre les menaces n’est pas disponible pour les clients des États-Unis GCC et GCC High.</span><span class="sxs-lookup"><span data-stu-id="e2f85-125">Currently, Microsoft Threat Protection is not available to US GCC and GCC High customers.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="e2f85-126">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="e2f85-126">Related topics</span></span>
- [<span data-ttu-id="e2f85-127">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e2f85-127">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="e2f85-128">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e2f85-128">Turn on Microsoft Threat Protection</span></span>](mtp-enable.md)
