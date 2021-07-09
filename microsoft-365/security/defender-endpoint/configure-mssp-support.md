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
ms.openlocfilehash: d82bffd6eea54256f2c6773f843030a19e27275d
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53339357"
---
# <a name="configure-managed-security-service-provider-integration"></a><span data-ttu-id="f394e-104">Configurer l’intégration des fournisseurs de services de sécurité gérés</span><span class="sxs-lookup"><span data-stu-id="f394e-104">Configure managed security service provider integration</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f394e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f394e-105">**Applies to:**</span></span>
- [<span data-ttu-id="f394e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f394e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f394e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f394e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="f394e-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f394e-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f394e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f394e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mssp-support-abovefoldlink)
 
[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="f394e-110">Vous devez suivre les étapes de configuration suivantes pour activer l’intégration du fournisseur de services de sécurité géré (MSSP).</span><span class="sxs-lookup"><span data-stu-id="f394e-110">You'll need to take the following configuration steps to enable the managed security service provider (MSSP) integration.</span></span>

>[!NOTE]
><span data-ttu-id="f394e-111">Les termes suivants sont utilisés dans cet article pour faire la distinction entre le fournisseur de services et le consommateur de services :</span><span class="sxs-lookup"><span data-stu-id="f394e-111">The following terms are used in this article to distinguish between the service provider and service consumer:</span></span>
> - <span data-ttu-id="f394e-112">MSSP : organisations de sécurité qui offrent de surveiller et de gérer les appareils de sécurité d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="f394e-112">MSSPs: Security organizations that offer to monitor and manage security devices for an organization.</span></span>
> - <span data-ttu-id="f394e-113">Clients MSSP : organisations qui engagent les services des MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-113">MSSP customers: Organizations that engage the services of MSSPs.</span></span>

<span data-ttu-id="f394e-114">L’intégration permettra aux MSSP d’agir comme suit :</span><span class="sxs-lookup"><span data-stu-id="f394e-114">The integration will allow MSSPs to take the following actions:</span></span>

- <span data-ttu-id="f394e-115">Accéder au portail Microsoft 365 Defender client MSSP</span><span class="sxs-lookup"><span data-stu-id="f394e-115">Get access to MSSP customer's Microsoft 365 Defender portal</span></span>
- <span data-ttu-id="f394e-116">Obtenir des notifications par courrier électronique et</span><span class="sxs-lookup"><span data-stu-id="f394e-116">Get email notifications, and</span></span> 
- <span data-ttu-id="f394e-117">Récupérer des alertes via les outils de gestion des événements et des informations de sécurité (SIEM)</span><span class="sxs-lookup"><span data-stu-id="f394e-117">Fetch alerts through security information and event management (SIEM) tools</span></span>

<span data-ttu-id="f394e-118">Avant que les MSSP ne prennent ces mesures, le client MSSP doit accorder l’accès à son client Defender for Endpoint afin que le MSSP puisse accéder au portail.</span><span class="sxs-lookup"><span data-stu-id="f394e-118">Before MSSPs can take these actions, the MSSP customer will need to grant access to their Defender for Endpoint tenant so that the MSSP can access the portal.</span></span> 
 

<span data-ttu-id="f394e-119">En règle générale, les clients MSSP prennent les étapes de configuration initiales pour accorder aux MSSP l’accès à Windows Defender client central de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f394e-119">Typically, MSSP customers take the initial configuration steps to grant MSSPs access to their Windows Defender Security Central tenant.</span></span> <span data-ttu-id="f394e-120">Une fois l’accès accordé, d’autres étapes de configuration peuvent être réalisées par le client MSSP ou le MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-120">After access is granted, other configuration steps can be done by either the MSSP customer or the MSSP.</span></span>


<span data-ttu-id="f394e-121">En règle générale, les étapes de configuration suivantes doivent être prises :</span><span class="sxs-lookup"><span data-stu-id="f394e-121">In general, the following configuration steps need to be taken:</span></span>


- <span data-ttu-id="f394e-122">**Accorder au MSSP l’accès Microsoft 365 Defender**</span><span class="sxs-lookup"><span data-stu-id="f394e-122">**Grant the MSSP access to Microsoft 365 Defender**</span></span> <br>
<span data-ttu-id="f394e-123">Cette action doit être effectuée par le client MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-123">This action needs to be done by the MSSP customer.</span></span> <span data-ttu-id="f394e-124">Il accorde au MSSP l’accès au client Defender for Endpoint du client MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-124">It grants the MSSP access to the MSSP customer's Defender for Endpoint tenant.</span></span>
 

- <span data-ttu-id="f394e-125">**Configurer les notifications d’alerte envoyées aux MSSP**</span><span class="sxs-lookup"><span data-stu-id="f394e-125">**Configure alert notifications sent to MSSPs**</span></span> <br>
<span data-ttu-id="f394e-126">Cette action peut être prise par le client MSSP ou MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-126">This action can be taken by either the MSSP customer or MSSP.</span></span> <span data-ttu-id="f394e-127">Cela permet aux MSSP de savoir quelles alertes ils doivent adresser pour le client MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-127">This lets the MSSPs know what alerts they need to address for the MSSP customer.</span></span>

- <span data-ttu-id="f394e-128">**Récupérer les alertes du client du client MSSP dans le système SIEM**</span><span class="sxs-lookup"><span data-stu-id="f394e-128">**Fetch alerts from MSSP customer's tenant into SIEM system**</span></span> <br> <span data-ttu-id="f394e-129">Cette action est prise par le MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-129">This action is taken by the MSSP.</span></span> <span data-ttu-id="f394e-130">Il permet aux MSSP de récupérer des alertes dans les outils SIEM.</span><span class="sxs-lookup"><span data-stu-id="f394e-130">It allows MSSPs to fetch alerts in SIEM tools.</span></span>

- <span data-ttu-id="f394e-131">**Récupérer des alertes à partir du client MSSP client à l’aide des API**</span><span class="sxs-lookup"><span data-stu-id="f394e-131">**Fetch alerts from MSSP customer's tenant using APIs**</span></span> <br>
<span data-ttu-id="f394e-132">Cette action est prise par le MSSP.</span><span class="sxs-lookup"><span data-stu-id="f394e-132">This action is taken by the MSSP.</span></span> <span data-ttu-id="f394e-133">Il permet aux MSSP de récupérer des alertes à l’aide d’API.</span><span class="sxs-lookup"><span data-stu-id="f394e-133">It allows MSSPs to fetch alerts using APIs.</span></span>

## <a name="multi-tenant-access-for-mssps"></a><span data-ttu-id="f394e-134">Accès multi-client pour les MSSP</span><span class="sxs-lookup"><span data-stu-id="f394e-134">Multi-tenant access for MSSPs</span></span>
<span data-ttu-id="f394e-135">Pour plus d’informations sur l’implémenter un accès délégué à plusieurs locataires, voir [Accès multi-locataire](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/multi-tenant-access-for-managed-security-service-providers/ba-p/1533440)pour les fournisseurs de services de sécurité gérée.</span><span class="sxs-lookup"><span data-stu-id="f394e-135">For information on how to implement a multi-tenant delegated access, see [Multi-tenant access for Managed Security Service Providers](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/multi-tenant-access-for-managed-security-service-providers/ba-p/1533440).</span></span>



## <a name="related-topics"></a><span data-ttu-id="f394e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f394e-136">Related topics</span></span>
- [<span data-ttu-id="f394e-137">Accorder l’accès MSSP au portail</span><span class="sxs-lookup"><span data-stu-id="f394e-137">Grant MSSP access to the portal</span></span>](grant-mssp-access.md)
- [<span data-ttu-id="f394e-138">Accéder au portail client MSSP</span><span class="sxs-lookup"><span data-stu-id="f394e-138">Access the MSSP customer portal</span></span>](access-mssp-portal.md)
- [<span data-ttu-id="f394e-139">Configurer des notifications d’alerte</span><span class="sxs-lookup"><span data-stu-id="f394e-139">Configure alert notifications</span></span>](configure-mssp-notifications.md)
- [<span data-ttu-id="f394e-140">Récupérer les alertes d’un client</span><span class="sxs-lookup"><span data-stu-id="f394e-140">Fetch alerts from customer tenant</span></span>](fetch-alerts-mssp.md)

