---
title: Accéder au portail client MSSP du Centre de sécurité Microsoft Defender
description: Accéder au portail client MSSP du Centre de sécurité Microsoft Defender
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
ms.openlocfilehash: 97122decede91e8b4f059b3b66999ac12b300172
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51164856"
---
# <a name="access-the-microsoft-defender-security-center-mssp-customer-portal"></a><span data-ttu-id="c7492-104">Accéder au portail client MSSP du Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="c7492-104">Access the Microsoft Defender Security Center MSSP customer portal</span></span>

<span data-ttu-id="c7492-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c7492-105">**Applies to:**</span></span>
- [<span data-ttu-id="c7492-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c7492-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="c7492-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c7492-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="c7492-108">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c7492-108">**Applies to:**</span></span>

- [<span data-ttu-id="c7492-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c7492-109">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="c7492-110">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c7492-110">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="c7492-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c7492-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mssp-support-abovefoldlink)




>[!NOTE] 
><span data-ttu-id="c7492-112">Ces étapes sont dirigées vers le MSSP.</span><span class="sxs-lookup"><span data-stu-id="c7492-112">These set of steps are directed towards the MSSP.</span></span> 

<span data-ttu-id="c7492-113">Par défaut, les clients MSSP accèdent à leur client centre de sécurité Microsoft Defender via l’URL suivante : `https://securitycenter.windows.com` .</span><span class="sxs-lookup"><span data-stu-id="c7492-113">By default, MSSP customers access their Microsoft Defender Security Center tenant through the following URL: `https://securitycenter.windows.com`.</span></span>
 

<span data-ttu-id="c7492-114">Toutefois, les MSSP doivent utiliser une URL propre au client au format suivant : pour accéder au portail client  `https://securitycenter.windows.com?tid=customer_tenant_id` MSSP.</span><span class="sxs-lookup"><span data-stu-id="c7492-114">MSSPs however, will need to use a tenant-specific URL in the following format:  `https://securitycenter.windows.com?tid=customer_tenant_id` to access the MSSP customer portal.</span></span> 

<span data-ttu-id="c7492-115">En règle générale, les MSSP doivent être ajoutés à chaque azure AD du client MSSP qu’il a l’intention de gérer.</span><span class="sxs-lookup"><span data-stu-id="c7492-115">In general, MSSPs will need to be added to each of the MSSP customer's Azure AD that they intend to manage.</span></span>


<span data-ttu-id="c7492-116">Utilisez les étapes suivantes pour obtenir l’ID de client MSSP, puis utilisez l’ID pour accéder à l’URL propre au client :</span><span class="sxs-lookup"><span data-stu-id="c7492-116">Use the following steps to obtain the MSSP customer tenant ID and then use the ID to access the tenant-specific URL:</span></span>

1. <span data-ttu-id="c7492-117">En tant que MSSP, connectez-vous à Azure AD avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c7492-117">As an MSSP, login to Azure AD with your credentials.</span></span> 

2. <span data-ttu-id="c7492-118">Basculez l’annuaire vers le client du MSSP.</span><span class="sxs-lookup"><span data-stu-id="c7492-118">Switch directory to the MSSP customer's tenant.</span></span>

3.  <span data-ttu-id="c7492-119">Sélectionnez **Les propriétés de > Azure Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="c7492-119">Select **Azure Active Directory > Properties**.</span></span> <span data-ttu-id="c7492-120">Vous trouverez l’ID de client dans le champ ID d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c7492-120">You'll find the tenant ID in the Directory ID field.</span></span> 

4. <span data-ttu-id="c7492-121">Accédez au portail client MSSP en remplaçant la `customer_tenant_id` valeur dans l’URL suivante : `https://securitycenter.windows.com?tid=customer_tenant_id` .</span><span class="sxs-lookup"><span data-stu-id="c7492-121">Access the MSSP customer portal by replacing the `customer_tenant_id` value in the following URL: `https://securitycenter.windows.com?tid=customer_tenant_id`.</span></span>


## <a name="related-topics"></a><span data-ttu-id="c7492-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7492-122">Related topics</span></span>
- [<span data-ttu-id="c7492-123">Accorder l’accès MSSP au portail</span><span class="sxs-lookup"><span data-stu-id="c7492-123">Grant MSSP access to the portal</span></span>](grant-mssp-access.md)
- [<span data-ttu-id="c7492-124">Configurer les notifications d’alerte</span><span class="sxs-lookup"><span data-stu-id="c7492-124">Configure alert notifications</span></span>](configure-mssp-notifications.md)
- [<span data-ttu-id="c7492-125">Récupérer des alertes à partir du client</span><span class="sxs-lookup"><span data-stu-id="c7492-125">Fetch alerts from customer tenant</span></span>](fetch-alerts-mssp.md)
