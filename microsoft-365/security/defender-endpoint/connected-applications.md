---
title: Applications connectées dans Microsoft Defender pour point de terminaison
ms.reviewer: ''
description: Afficher les applications partenaires connectées qui utilisent le protocole OAuth 2.0 standard pour s'authentifier et fournir des jetons à utiliser avec les API Microsoft Defender for Endpoint.
keywords: partenaires, applications, tiers, connexions, sentinelone, recherche, bitdefender, corrata, morphisec, paloalto, ziften, meilleure mobilité
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 26c531c0544f92d664bfa0f1a21e4f33a0765d24
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893496"
---
# <a name="connected-applications-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="63769-104">Applications connectées dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="63769-104">Connected applications in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="63769-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="63769-105">**Applies to:**</span></span>
- [<span data-ttu-id="63769-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="63769-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="63769-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="63769-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="63769-108">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="63769-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="63769-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="63769-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="63769-110">Les applications connectées s'intègrent à la plateforme Defender for Endpoint à l'aide des API.</span><span class="sxs-lookup"><span data-stu-id="63769-110">Connected applications integrates with the Defender for Endpoint platform using APIs.</span></span> 

<span data-ttu-id="63769-111">Les applications utilisent le protocole OAuth 2.0 standard pour s'authentifier et fournir des jetons à utiliser avec les API Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="63769-111">Applications use standard OAuth 2.0 protocol to authenticate and provide tokens for use with Microsoft Defender for Endpoint APIs.</span></span>  <span data-ttu-id="63769-112">En outre, les applications Azure Active Directory (Azure AD) permettent aux administrateurs client de définir un contrôle explicite sur les API accessibles à l'aide de l'application correspondante.</span><span class="sxs-lookup"><span data-stu-id="63769-112">In addition, Azure Active Directory (Azure AD) applications allow tenant admins to set explicit control over which APIs can be accessed using the corresponding app.</span></span>
 
<span data-ttu-id="63769-113">Vous devez suivre ces [étapes](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/apis-intro) pour utiliser les API avec l'application connectée.</span><span class="sxs-lookup"><span data-stu-id="63769-113">You'll need to follow [these steps](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/apis-intro) to use the APIs with the connected application.</span></span>
 
## <a name="access-the-connected-application-page"></a><span data-ttu-id="63769-114">Accéder à la page de l'application connectée</span><span class="sxs-lookup"><span data-stu-id="63769-114">Access the connected application page</span></span>
<span data-ttu-id="63769-115">Dans le menu de navigation de gauche, sélectionnez **Partenaires & API**  >  **connectées aux applications AAD.**</span><span class="sxs-lookup"><span data-stu-id="63769-115">From the left navigation menu, select **Partners & APIs** > **Connected AAD applications**.</span></span>

 
## <a name="view-connected-application-details"></a><span data-ttu-id="63769-116">Afficher les détails de l'application connectée</span><span class="sxs-lookup"><span data-stu-id="63769-116">View connected application details</span></span>
<span data-ttu-id="63769-117">La page Applications connectées fournit des informations sur les applications Azure AD connectées à Microsoft Defender pour endpoint dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="63769-117">The Connected applications page provides information about the Azure AD applications connected to Microsoft Defender for Endpoint in your organization.</span></span> <span data-ttu-id="63769-118">Vous pouvez passer en revue l'utilisation des applications connectées : dernière expérience, nombre de demandes au cours des dernières 24 heures et tendances des demandes au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="63769-118">You can review the usage of the connected applications: last seen, number of requests in the past 24 hours, and request trends in the last 30 days.</span></span>

![Image des applications connectées](images/connected-apps.png)
 
## <a name="edit-reconfigure-or-delete-a-connected-application"></a><span data-ttu-id="63769-120">Modifier, reconfigurer ou supprimer une application connectée</span><span class="sxs-lookup"><span data-stu-id="63769-120">Edit, reconfigure, or delete a connected application</span></span>
<span data-ttu-id="63769-121">Le **lien Ouvrir les paramètres de l'application** ouvre la page de gestion des applications Azure AD correspondante dans le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="63769-121">The **Open application settings** link opens the corresponding Azure AD application management page in the Azure portal.</span></span> <span data-ttu-id="63769-122">À partir du portail Azure, vous pouvez gérer les autorisations, reconfigurer ou supprimer les applications connectées.</span><span class="sxs-lookup"><span data-stu-id="63769-122">From the Azure portal, you can manage permissions, reconfigure, or delete the connected applications.</span></span>
