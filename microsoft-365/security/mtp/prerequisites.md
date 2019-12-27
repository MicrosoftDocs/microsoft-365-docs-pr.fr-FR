---
title: Conditions préalables pour la Protection Microsoft contre les menaces
description: En savoir plus sur les exigences en matière de licences, de matériel et de logiciels, ainsi que sur les autres paramètres de configuration de la Protection Microsoft contre les menaces.
keywords: conditions requises, configuration matérielle, logicielle, navigateur, MTP, M365, licence
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
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
ms.openlocfilehash: 2175ca328678e271056ae75d1bcbb7dc70a2198d
ms.sourcegitcommit: 5b0a2e11c86c00e6e6b534f8b0a19962d1bb2805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/27/2019
ms.locfileid: "40881965"
---
# <a name="microsoft-threat-protection-prerequisites"></a><span data-ttu-id="be0fb-104">Conditions préalables pour la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="be0fb-104">Microsoft Threat Protection prerequisites</span></span>

<span data-ttu-id="be0fb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="be0fb-105">**Applies to:**</span></span>
- <span data-ttu-id="be0fb-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="be0fb-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="be0fb-107">En savoir plus sur les exigences en matière de licences, de matériel et de logiciels, ainsi que sur les autres paramètres de configuration nécessaires à l'exécution et à l'utilisation du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="be0fb-107">Learn about the licensing, hardware and software requirements, and other configuration settings to run and use the Microsoft 365 security.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="be0fb-108">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="be0fb-108">Licensing requirements</span></span>
<span data-ttu-id="be0fb-109">Le Centre de sécurité Microsoft 365 nécessite l’une des licences suivantes :</span><span class="sxs-lookup"><span data-stu-id="be0fb-109">Microsoft 365 security requires one of the following licenses:</span></span>

- <span data-ttu-id="be0fb-110">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="be0fb-110">Microsoft 365 E5</span></span> 
- <span data-ttu-id="be0fb-111">Office 365 E5, Enterprise Mobility + Security E5 et Windows E5</span><span class="sxs-lookup"><span data-stu-id="be0fb-111">Office 365 E5, Enterprise Mobility + Security E5, and Windows E5</span></span>

<span data-ttu-id="be0fb-112">Vous pouvez acquérir ces licences à partir de la [page Microsoft 365 Entreprise](https://www.microsoft.com/en-us/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="be0fb-112">You can acquire these licenses from the [Microsoft 365 enterprise page](https://www.microsoft.com/en-us/microsoft-365/enterprise).</span></span>

### <a name="check-your-existing--licenses"></a><span data-ttu-id="be0fb-113">Vérifiez vos licences existantes</span><span class="sxs-lookup"><span data-stu-id="be0fb-113">Check your existing  licenses</span></span>
<span data-ttu-id="be0fb-114">Accédez au Centre d’administration Microsoft 365 sur [admin.microsoft.com](https://admin.microsoft.com/) pour afficher vos licences existantes.</span><span class="sxs-lookup"><span data-stu-id="be0fb-114">Go to Microsoft 365 admin center at [admin.microsoft.com](https://admin.microsoft.com/) to view your existing licenses.</span></span> <span data-ttu-id="be0fb-115">Dans le Centre d'administration, accédez à **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="be0fb-115">In the admin center, go to **Billing** > **Licenses**.</span></span>

<span data-ttu-id="be0fb-116">Vous devez être affecté à un rôle d’**Administrateur de facturation** ou **Lecteur général** [dans Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour afficher les informations de licence.</span><span class="sxs-lookup"><span data-stu-id="be0fb-116">You need to be assigned either the **Billing admin** or **Global reader** [role in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to be able to see licensing information.</span></span> <span data-ttu-id="be0fb-117">Si vous rencontrez des problèmes d’accès, veuillez contacter un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="be0fb-117">If you encounter access problems, contact a global admin.</span></span>  

## <a name="browser-requirements"></a><span data-ttu-id="be0fb-118">Configuration requise pour le navigateur</span><span class="sxs-lookup"><span data-stu-id="be0fb-118">Browser requirements</span></span>
<span data-ttu-id="be0fb-119">L’accès au Centre de sécurité Microsoft 365 est effectué via un navigateur.</span><span class="sxs-lookup"><span data-stu-id="be0fb-119">Access to Microsoft 365 security center is done through a browser.</span></span> <span data-ttu-id="be0fb-120">Internet Explorer 10et Microsoft Edge sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="be0fb-120">Internet Explorer and Microsoft Edge is supported.</span></span> <span data-ttu-id="be0fb-121">Les navigateurs compatibles HTML5 sont également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="be0fb-121">Any HTML5 compliant browsers are also supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be0fb-122">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="be0fb-122">Related topics</span></span>
- [<span data-ttu-id="be0fb-123">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="be0fb-123">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="be0fb-124">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="be0fb-124">Turn on Microsoft Threat Protection</span></span>](mtp-enable.md)