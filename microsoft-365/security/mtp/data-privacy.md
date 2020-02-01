---
title: Sécurité et confidentialité des données de la Protection Microsoft contre les menaces
description: Décrit la confidentialité et la sécurité des données du service.
keywords: confidentialité, données, sécurité, centre de gestion de la confidentialité, collecte d’informations
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
ms.openlocfilehash: d439321bd2c4ea2251f2d9069b814b1c63013f28
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600261"
---
# <a name="microsoft-threat-protection-data-security-and-privacy"></a><span data-ttu-id="27bb0-104">Sécurité et confidentialité des données de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="27bb0-104">Microsoft Threat Protection data security and privacy</span></span>

<span data-ttu-id="27bb0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="27bb0-105">**Applies to:**</span></span>
- <span data-ttu-id="27bb0-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="27bb0-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="27bb0-107">En utilisant la préversion Protection Microsoft contre les menaces, vous acceptez les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="27bb0-107">By using the Microsoft Threat Protection preview you consent to the following terms:</span></span>

<span data-ttu-id="27bb0-108">Vos données client applicables (telles que définies dans les conditions du service en ligne (« OST »)) seront transférées d’autres services Microsoft dans la Protection Microsoft contre les menaces et de cette dernière de nouveau vers les services Microsoft applicables.</span><span class="sxs-lookup"><span data-stu-id="27bb0-108">Your applicable Customer Data (as defined in the Online Service Terms ("OST")) will be transferred from other Microsoft services into Microsoft Threat Protection and from Microsoft Threat Protection back to applicable Microsoft services.</span></span> <span data-ttu-id="27bb0-109">Pendant toute la durée de cette préversion, l’utilisation de vos données client dans la Protection Microsoft contre les menaces suivra les normes et engagements en matière de gestion des données pour Microsoft Defender - Protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="27bb0-109">For the duration of this preview, use of your Customer Data in Microsoft Threat Protection will follow the data handling standards and commitments for Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP).</span></span> <span data-ttu-id="27bb0-110">Vous reconnaissez qu’il est possible que ces engagements diffèrent des services à partir desquels les données client sont transférées.</span><span class="sxs-lookup"><span data-stu-id="27bb0-110">You acknowledge that such commitments may differ from the services from which that Customer Data is transferred.</span></span> <span data-ttu-id="27bb0-111">De plus, les données client stockées dans la Protection Microsoft contre les menace seront stockées dans la zone géographique que vous avez sélectionnée pour le stockage de vos données client Microsoft Defender - Protection avancée contre les menaces, lesquelles peuvent différer de celle que vous avez sélectionnée en connexion avec d’autres services.</span><span class="sxs-lookup"><span data-stu-id="27bb0-111">Further, Customer Data stored in Microsoft Threat Protection will be stored at rest in the Geo you selected for storage of your Microsoft Defender ATP Customer Data, which may differ from the Geo you selected in connection with other services.</span></span> <span data-ttu-id="27bb0-112">Microsoft ne transférera pas les données client à l’extérieur de ce type de zone géographique, sauf indication contraire dans la section « emplacement des données » du centre de gestion de la confidentialité Microsoft dans [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="27bb0-112">Microsoft will not transfer the Customer Data outside of such Geo except as noted in the "Data Location" section of the Microsoft Trust Center located at [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span>

<span data-ttu-id="27bb0-113">De plus, lorsque vous déterminez lequel de vos utilisateurs peut accéder à la Protection Microsoft contre les menaces, celle-ci ne permet pas le contrôle de l’accès basé sur les rôles (« RBAC ») actuellement.</span><span class="sxs-lookup"><span data-stu-id="27bb0-113">Further, while you determine which of your users may access Microsoft Threat Protection, Microsoft Threat Protection does not currently allow for role-based access control ("RBAC").</span></span> <span data-ttu-id="27bb0-114">Vous reconnaissez que, dans la mesure où la Protection Microsoft contre les menaces reçoit les données d’un service Microsoft qui prend en charge RBAC, les niveaux d’accès dans ce service ne s’appliquent pas à la Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="27bb0-114">You acknowledge that to the extent Microsoft Threat Protection receives data from a Microsoft service that does support RBAC, access levels in that service will not apply in Microsoft Threat Protection.</span></span>


<span data-ttu-id="27bb0-115">Pour plus d’informations sur le stockage des données et la confidentialité concernant les produits spécifiques, voir :</span><span class="sxs-lookup"><span data-stu-id="27bb0-115">For more information on the data storage and privacy information of the specific products see:</span></span>
- [<span data-ttu-id="27bb0-116">Stockage de données et confidentialité Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="27bb0-116">Microsoft Defender ATP data storage and privacy</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
- [<span data-ttu-id="27bb0-117">Sécurité des données sur la sécurité et confidentialité Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="27bb0-117">Microsoft Cloud App Security data security and privacy</span></span>](https://docs.microsoft.com/cloud-app-security/cas-compliance-trust)
- [<span data-ttu-id="27bb0-118">Confidentialité, sécurité et transparence d’Office 365</span><span class="sxs-lookup"><span data-stu-id="27bb0-118">Office 365 privacy, security, and transparency</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/privacy-security-and-transparency#advanced-threat-protection)