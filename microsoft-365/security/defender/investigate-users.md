---
title: Examiner les utilisateurs dans le Centre de sécurité Microsoft 365
description: examiner les utilisateurs dans le Centre de sécurité Microsoft 365
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, surveiller, signaler, identités, données, appareils, applications
ms.prod: m365-security
ms.mktglfcycl: deploy
localization_priority: Normal
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
ms.date: ''
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-jun2020
ms.technology: m365d
ms.openlocfilehash: f48716ebd9e25d1f8b24d9276aaa5890a335a808
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51056625"
---
# <a name="investigate-users-in-microsoft-365-security-center"></a><span data-ttu-id="9f219-104">Examiner les utilisateurs dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9f219-104">Investigate users in Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="9f219-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9f219-105">**Applies to:**</span></span>

- <span data-ttu-id="9f219-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9f219-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="9f219-107">Dans le cadre de votre enquête, vous pouvez découvrir qu’un utilisateur a été compromis.</span><span class="sxs-lookup"><span data-stu-id="9f219-107">As part of your investigation, you might find that a user has been compromised.</span></span>

<span data-ttu-id="9f219-108">La page utilisateur du Centre de sécurité Microsoft 365 combine les informations de Microsoft Defender pour le point de terminaison, Microsoft Defender pour l’identité et Microsoft Cloud App Security (en fonction des licences dont vous avez la licence).</span><span class="sxs-lookup"><span data-stu-id="9f219-108">The Microsoft 365 security center user page combines information from Microsoft Defender for Endpoint, Microsoft Defender for Identity, and Microsoft Cloud App Security (depending on what licenses you have).</span></span> <span data-ttu-id="9f219-109">Cette page est le point de départ idéal pour examiner les utilisateurs et les incidents potentiels.</span><span class="sxs-lookup"><span data-stu-id="9f219-109">This page is the ideal starting place for investigating users and potential incidents.</span></span>
<span data-ttu-id="9f219-110">![Page utilisateur](../../media/m3d-userpage.png)</span><span class="sxs-lookup"><span data-stu-id="9f219-110">![User page](../../media/m3d-userpage.png)</span></span>

<span data-ttu-id="9f219-111">Cette page affiche des informations spécifiques au risque de sécurité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f219-111">This page shows information specific to the security risk of a user.</span></span> <span data-ttu-id="9f219-112">Cela inclut un score qui permet d’évaluer les risques, les événements récents et les alertes qui ont contribué au risque global de l’utilisateur, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="9f219-112">This includes a score that helps assess risk, recent events and alerts that contributed to the overall risk of the user, and more.</span></span>

<span data-ttu-id="9f219-113">Vous pouvez accéder à cette page à partir de plusieurs zones du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9f219-113">You can access this page from multiple areas in the Microsoft 365 security center.</span></span> <span data-ttu-id="9f219-114">Vous pouvez accéder à cette page à partir d’un incident spécifique dans **l’onglet Utilisateurs.** Certaines alertes peuvent inclure des utilisateurs en tant que ressources affectées spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9f219-114">You can access this page from a specific incident in the **Users** tab. Some alerts might include users as a specific affected asset.</span></span> <span data-ttu-id="9f219-115">Vous pouvez également rechercher des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9f219-115">You can also search for users.</span></span>  

<span data-ttu-id="9f219-116">En savoir plus sur la façon d’examiner les utilisateurs et les risques potentiels [dans ce didacticiel Cloud App Security](/cloud-app-security/tutorial-ueba#:~:text=To%20identify%20who%20your%20riskiest,user%20page%20to%20investigate%20them).</span><span class="sxs-lookup"><span data-stu-id="9f219-116">Learn more about how to investigate users and potential risk [in this Cloud App Security tutorial](/cloud-app-security/tutorial-ueba#:~:text=To%20identify%20who%20your%20riskiest,user%20page%20to%20investigate%20them).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f219-117">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="9f219-117">Related topics</span></span>

- [<span data-ttu-id="9f219-118">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="9f219-118">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="9f219-119">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="9f219-119">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="9f219-120">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="9f219-120">Manage incidents</span></span>](manage-incidents.md)