---
title: Configurer la prise en charge des fournisseurs de services de sécurité gérés
description: Prendre les mesures nécessaires pour configurer l’intégration MSSP avec Microsoft Defender for Endpoint
keywords: fournisseur de services de sécurité géré, mssp, configurer, intégration
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6786d423d20ec90c12d2ea712003acc787ed599d
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165248"
---
# <a name="configure-managed-security-service-provider-integration"></a><span data-ttu-id="3bb3d-104">Configurer l’intégration des fournisseurs de services de sécurité gérés</span><span class="sxs-lookup"><span data-stu-id="3bb3d-104">Configure managed security service provider integration</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3bb3d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3bb3d-105">**Applies to:**</span></span>
- [<span data-ttu-id="3bb3d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3bb3d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3bb3d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3bb3d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="3bb3d-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="3bb3d-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="3bb3d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mssp-support-abovefoldlink)
 
[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="3bb3d-110">Vous devez suivre les étapes de configuration suivantes pour activer l’intégration du fournisseur de services de sécurité géré (MSSP).</span><span class="sxs-lookup"><span data-stu-id="3bb3d-110">You'll need to take the following configuration steps to enable the managed security service provider (MSSP) integration.</span></span>

>[!NOTE]
><span data-ttu-id="3bb3d-111">Les termes suivants sont utilisés dans cet article pour faire la distinction entre le fournisseur de services et le consommateur de services :</span><span class="sxs-lookup"><span data-stu-id="3bb3d-111">The following terms are used in this article to distinguish between the service provider and service consumer:</span></span>
> - <span data-ttu-id="3bb3d-112">MSSP : organisations de sécurité qui offrent de surveiller et de gérer les appareils de sécurité d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-112">MSSPs: Security organizations that offer to monitor and manage security devices for an organization.</span></span>
> - <span data-ttu-id="3bb3d-113">Clients MSSP : organisations qui engagent les services des MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-113">MSSP customers: Organizations that engage the services of MSSPs.</span></span>

<span data-ttu-id="3bb3d-114">L’intégration permettra aux MSSP d’agir comme suit :</span><span class="sxs-lookup"><span data-stu-id="3bb3d-114">The integration will allow MSSPs to take the following actions:</span></span>

- <span data-ttu-id="3bb3d-115">Accéder au portail Centre de sécurité Microsoft Defender du client MSSP</span><span class="sxs-lookup"><span data-stu-id="3bb3d-115">Get access to MSSP customer's Microsoft Defender Security Center portal</span></span>
- <span data-ttu-id="3bb3d-116">Obtenir des notifications par courrier électronique et</span><span class="sxs-lookup"><span data-stu-id="3bb3d-116">Get email notifications, and</span></span> 
- <span data-ttu-id="3bb3d-117">Récupérer des alertes via les outils de gestion des événements et des informations de sécurité (SIEM)</span><span class="sxs-lookup"><span data-stu-id="3bb3d-117">Fetch alerts through security information and event management (SIEM) tools</span></span>

<span data-ttu-id="3bb3d-118">Avant que les MSSP ne prennent ces mesures, le client MSSP doit accorder l’accès à son client Defender for Endpoint afin que le MSSP puisse accéder au portail.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-118">Before MSSPs can take these actions, the MSSP customer will need to grant access to their Defender for Endpoint tenant so that the MSSP can access the portal.</span></span> 
 

<span data-ttu-id="3bb3d-119">En règle générale, les clients MSSP prennent les étapes de configuration initiales pour accorder aux MSSP l’accès à Windows Defender client central de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-119">Typically, MSSP customers take the initial configuration steps to grant MSSPs access to their Windows Defender Security Central tenant.</span></span> <span data-ttu-id="3bb3d-120">Une fois l’accès accordé, d’autres étapes de configuration peuvent être réalisées par le client MSSP ou le MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-120">After access is granted, other configuration steps can be done by either the MSSP customer or the MSSP.</span></span>


<span data-ttu-id="3bb3d-121">En règle générale, les étapes de configuration suivantes doivent être prises :</span><span class="sxs-lookup"><span data-stu-id="3bb3d-121">In general, the following configuration steps need to be taken:</span></span>


- <span data-ttu-id="3bb3d-122">**Accorder au MSSP l’accès au Centre de sécurité Microsoft Defender**</span><span class="sxs-lookup"><span data-stu-id="3bb3d-122">**Grant the MSSP access to Microsoft Defender Security Center**</span></span> <br>
<span data-ttu-id="3bb3d-123">Cette action doit être effectuée par le client MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-123">This action needs to be done by the MSSP customer.</span></span> <span data-ttu-id="3bb3d-124">Il accorde au MSSP l’accès au client Defender for Endpoint du client MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-124">It grants the MSSP access to the MSSP customer's Defender for Endpoint tenant.</span></span>
 

- <span data-ttu-id="3bb3d-125">**Configurer les notifications d’alerte envoyées aux MSSP**</span><span class="sxs-lookup"><span data-stu-id="3bb3d-125">**Configure alert notifications sent to MSSPs**</span></span> <br>
<span data-ttu-id="3bb3d-126">Cette action peut être prise par le client MSSP ou MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-126">This action can be taken by either the MSSP customer or MSSP.</span></span> <span data-ttu-id="3bb3d-127">Cela permet aux MSSP de savoir quelles alertes ils doivent adresser pour le client MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-127">This lets the MSSPs know what alerts they need to address for the MSSP customer.</span></span>

- <span data-ttu-id="3bb3d-128">**Récupérer des alertes du client MSSP client dans le système SIEM**</span><span class="sxs-lookup"><span data-stu-id="3bb3d-128">**Fetch alerts from MSSP customer's tenant into SIEM system**</span></span> <br> <span data-ttu-id="3bb3d-129">Cette action est prise par le MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-129">This action is taken by the MSSP.</span></span> <span data-ttu-id="3bb3d-130">Il permet aux MSSP de récupérer des alertes dans les outils SIEM.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-130">It allows MSSPs to fetch alerts in SIEM tools.</span></span>

- <span data-ttu-id="3bb3d-131">**Récupérer des alertes à partir du client MSSP client à l’aide des API**</span><span class="sxs-lookup"><span data-stu-id="3bb3d-131">**Fetch alerts from MSSP customer's tenant using APIs**</span></span> <br>
<span data-ttu-id="3bb3d-132">Cette action est prise par le MSSP.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-132">This action is taken by the MSSP.</span></span> <span data-ttu-id="3bb3d-133">Il permet aux MSSP de récupérer des alertes à l’aide d’API.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-133">It allows MSSPs to fetch alerts using APIs.</span></span>

## <a name="multi-tenant-access-for-mssps"></a><span data-ttu-id="3bb3d-134">Accès multi-client pour les MSSP</span><span class="sxs-lookup"><span data-stu-id="3bb3d-134">Multi-tenant access for MSSPs</span></span>
<span data-ttu-id="3bb3d-135">Pour plus d’informations sur l’implémenter un accès délégué à plusieurs locataires, voir [Accès multi-locataire](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/multi-tenant-access-for-managed-security-service-providers/ba-p/1533440)pour les fournisseurs de services de sécurité gérée.</span><span class="sxs-lookup"><span data-stu-id="3bb3d-135">For information on how to implement a multi-tenant delegated access, see [Multi-tenant access for Managed Security Service Providers](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/multi-tenant-access-for-managed-security-service-providers/ba-p/1533440).</span></span>



## <a name="related-topics"></a><span data-ttu-id="3bb3d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bb3d-136">Related topics</span></span>
- [<span data-ttu-id="3bb3d-137">Accorder l’accès MSSP au portail</span><span class="sxs-lookup"><span data-stu-id="3bb3d-137">Grant MSSP access to the portal</span></span>](grant-mssp-access.md)
- [<span data-ttu-id="3bb3d-138">Accéder au portail client MSSP</span><span class="sxs-lookup"><span data-stu-id="3bb3d-138">Access the MSSP customer portal</span></span>](access-mssp-portal.md)
- [<span data-ttu-id="3bb3d-139">Configurer les notifications d’alerte</span><span class="sxs-lookup"><span data-stu-id="3bb3d-139">Configure alert notifications</span></span>](configure-mssp-notifications.md)
- [<span data-ttu-id="3bb3d-140">Récupérer des alertes à partir du client</span><span class="sxs-lookup"><span data-stu-id="3bb3d-140">Fetch alerts from customer tenant</span></span>](fetch-alerts-mssp.md)

