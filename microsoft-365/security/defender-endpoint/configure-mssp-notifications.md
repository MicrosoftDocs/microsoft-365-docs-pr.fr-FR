---
title: Configurer les notifications d’alerte envoyées aux MSSP
description: Configurer les notifications d’alerte envoyées aux MSSP
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
ms.openlocfilehash: 67f7081e72b5ecc8bdb077f0537cf0cf92df38b9
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166052"
---
# <a name="configure-alert-notifications-that-are-sent-to-mssps"></a><span data-ttu-id="b18d8-104">Configurer les notifications d’alerte envoyées aux MSSP</span><span class="sxs-lookup"><span data-stu-id="b18d8-104">Configure alert notifications that are sent to MSSPs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b18d8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b18d8-105">**Applies to:**</span></span>
- [<span data-ttu-id="b18d8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b18d8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b18d8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b18d8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="b18d8-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="b18d8-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="b18d8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b18d8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mssp-support-abovefoldlink)


>[!NOTE]
><span data-ttu-id="b18d8-110">Cette étape peut être effectuée par le client MSSP ou MSSP.</span><span class="sxs-lookup"><span data-stu-id="b18d8-110">This step can be done by either the MSSP customer or MSSP.</span></span> <span data-ttu-id="b18d8-111">Les MSSP doivent avoir les autorisations appropriées pour configurer cette configuration au nom du client MSSP.</span><span class="sxs-lookup"><span data-stu-id="b18d8-111">MSSPs must be granted the appropriate permissions to configure this on behalf of the MSSP customer.</span></span>

<span data-ttu-id="b18d8-112">Une fois l’accès au portail accordé, des règles de notification d’alerte peuvent être créées afin que les messages électroniques soient envoyés aux MSSP lorsque des alertes associées au client sont créées et que des conditions définies sont remplies.</span><span class="sxs-lookup"><span data-stu-id="b18d8-112">After access the portal is granted, alert notification rules can to be created so that emails are sent to MSSPs when alerts associated with the tenant are created and set conditions are met.</span></span>

 
<span data-ttu-id="b18d8-113">Pour plus d’informations, voir [Créer des règles pour les notifications d’alerte.](configure-email-notifications.md#create-rules-for-alert-notifications)</span><span class="sxs-lookup"><span data-stu-id="b18d8-113">For more information, see [Create rules for alert notifications](configure-email-notifications.md#create-rules-for-alert-notifications).</span></span>
 

<span data-ttu-id="b18d8-114">Ces cases à cocher doivent être cochées :</span><span class="sxs-lookup"><span data-stu-id="b18d8-114">These check boxes must be checked:</span></span>
- <span data-ttu-id="b18d8-115">**Inclure le nom de l’organisation** : le nom du client sera ajouté aux notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="b18d8-115">**Include organization name** - The customer name will be added to email notifications</span></span>
- <span data-ttu-id="b18d8-116">**Inclure un lien portail** propre au client : l’URL du lien d’alerte aura un paramètre spécifique au client (tid=target_tenant_id) qui permet un accès direct au portail client cible</span><span class="sxs-lookup"><span data-stu-id="b18d8-116">**Include tenant-specific portal link** - Alert link URL will have tenant specific parameter (tid=target_tenant_id) that allows direct access to target tenant portal</span></span>


## <a name="related-topics"></a><span data-ttu-id="b18d8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b18d8-117">Related topics</span></span>
- [<span data-ttu-id="b18d8-118">Accorder l’accès MSSP au portail</span><span class="sxs-lookup"><span data-stu-id="b18d8-118">Grant MSSP access to the portal</span></span>](grant-mssp-access.md)
- [<span data-ttu-id="b18d8-119">Accéder au portail client MSSP</span><span class="sxs-lookup"><span data-stu-id="b18d8-119">Access the MSSP customer portal</span></span>](access-mssp-portal.md)
- [<span data-ttu-id="b18d8-120">Récupérer les alertes d’un client</span><span class="sxs-lookup"><span data-stu-id="b18d8-120">Fetch alerts from customer tenant</span></span>](fetch-alerts-mssp.md)
