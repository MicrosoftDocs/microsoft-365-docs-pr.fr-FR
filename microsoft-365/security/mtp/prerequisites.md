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
ms.openlocfilehash: ef26a2ebc25d7f55e7dc22347d85767dab970536
ms.sourcegitcommit: 9224a7a5886c0c5fa0bc12bd9f7234a0eba90023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42372052"
---
# <a name="microsoft-threat-protection-prerequisites"></a><span data-ttu-id="ca91f-104">Conditions préalables pour la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ca91f-104">Microsoft Threat Protection prerequisites</span></span>

<span data-ttu-id="ca91f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ca91f-105">**Applies to:**</span></span>
- <span data-ttu-id="ca91f-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ca91f-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="ca91f-107">Découvrez la gestion des licences, la configuration matérielle et logicielle requise, ainsi que d’autres paramètres de configuration pour mettre en service et utiliser la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ca91f-107">Learn about the licensing, hardware and software requirements, and other configuration settings to provision and use Microsoft Threat Protection.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="ca91f-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="ca91f-108">Licensing requirements</span></span>
<span data-ttu-id="ca91f-109">Pour utiliser Microsoft Threat Protection, vous avez besoin de l' *une* des licences ou de la combinaison de licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="ca91f-109">To use Microsoft Threat Protection, you need *one* of the following licenses or combination of licenses:</span></span>

- <span data-ttu-id="ca91f-110">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="ca91f-110">Microsoft 365 E5</span></span>
- <span data-ttu-id="ca91f-111">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="ca91f-111">Microsoft 365 E5 Security</span></span>
- <span data-ttu-id="ca91f-112">Office 365 E5 et « Enterprise Mobility + Security E5 (EMS E5) » et Windows E5</span><span class="sxs-lookup"><span data-stu-id="ca91f-112">Office 365 E5 and "Enterprise Mobility + Security E5 (EMS E5)" and Windows E5</span></span>
- <span data-ttu-id="ca91f-113">Microsoft 365 A5</span><span class="sxs-lookup"><span data-stu-id="ca91f-113">Microsoft 365 A5</span></span>
- <span data-ttu-id="ca91f-114">Sécurité Microsoft 365 A5</span><span class="sxs-lookup"><span data-stu-id="ca91f-114">Microsoft 365 A5 Security</span></span>
- <span data-ttu-id="ca91f-115">Office 365 a5 et « Enterprise Mobility + Security a5 (EMS a5) » et Windows a5</span><span class="sxs-lookup"><span data-stu-id="ca91f-115">Office 365 A5 and "Enterprise Mobility + Security A5 (EMS A5)" and Windows A5</span></span>

<span data-ttu-id="ca91f-116">Pour plus d’informations, [consultez les plans de services d’entreprise Microsoft 365](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="ca91f-116">For more information, [view the Microsoft 365 Enterprise service plans](https://www.microsoft.com/licensing/product-licensing/microsoft-365-enterprise).</span></span>

> <span data-ttu-id="ca91f-117">Vous n’avez pas encore de licence ?</span><span class="sxs-lookup"><span data-stu-id="ca91f-117">Don't have license yet?</span></span> [<span data-ttu-id="ca91f-118">Essayer ou acheter un abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ca91f-118">Try or buy a Microsoft 365 subscription</span></span>](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide)

### <a name="check-your-existing--licenses"></a><span data-ttu-id="ca91f-119">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="ca91f-119">Check your existing  licenses</span></span>
<span data-ttu-id="ca91f-120">Accédez au centre d’administration Microsoft 365 ([admin.Microsoft.com](https://admin.microsoft.com/)) pour afficher vos licences existantes.</span><span class="sxs-lookup"><span data-stu-id="ca91f-120">Go to Microsoft 365 admin center ([admin.microsoft.com](https://admin.microsoft.com/)) to view your existing licenses.</span></span> <span data-ttu-id="ca91f-121">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="ca91f-121">In the admin center, go to **Billing** > **Licenses**.</span></span>

>[!NOTE]
> <span data-ttu-id="ca91f-122">Vous devez disposer du rôle d' **administrateur de facturation** ou de **lecteur global** [dans Azure ad](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour être en mesure d’afficher les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="ca91f-122">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see license information.</span></span> <span data-ttu-id="ca91f-123">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ca91f-123">If you encounter access problems, contact a global admin.</span></span>

## <a name="browser-requirements"></a><span data-ttu-id="ca91f-124">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="ca91f-124">Browser requirements</span></span>
<span data-ttu-id="ca91f-125">Accédez à la protection contre les menaces Microsoft dans le centre de sécurité Microsoft 365 à l’aide de Microsoft Edge, d’Internet Explorer 11 ou de n’importe quel navigateur Web compatible HTML 5.</span><span class="sxs-lookup"><span data-stu-id="ca91f-125">Access Microsoft Threat Protection in the Microsoft 365 security center using Microsoft Edge, Internet Explorer 11, or any HTML 5 compliant web browser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca91f-126">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="ca91f-126">Related topics</span></span>
- [<span data-ttu-id="ca91f-127">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ca91f-127">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="ca91f-128">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ca91f-128">Turn on Microsoft Threat Protection</span></span>](mtp-enable.md)
