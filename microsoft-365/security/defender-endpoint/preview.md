---
title: Fonctionnalités de prévisualisation de Microsoft Defender for Endpoint
description: Découvrez comment accéder aux fonctionnalités d’aperçu de Microsoft Defender for Endpoint.
keywords: aperçu, expérience d’aperçu, Microsoft Defender pour point de terminaison, fonctionnalités, mises à jour
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
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 0b6edbdcda61eaf402275ae0b6dc9a38c5fe19f7
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53339489"
---
# <a name="microsoft-defender-for-endpoint-preview-features"></a><span data-ttu-id="6c68a-104">Fonctionnalités de prévisualisation de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="6c68a-104">Microsoft Defender for Endpoint preview features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6c68a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6c68a-105">**Applies to:**</span></span>
- [<span data-ttu-id="6c68a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6c68a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6c68a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6c68a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="6c68a-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6c68a-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6c68a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6c68a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="6c68a-110">Le service Defender for Endpoint est constamment mis à jour pour inclure de nouvelles améliorations et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6c68a-110">The Defender for Endpoint service is constantly being updated to include new feature enhancements and capabilities.</span></span>

<span data-ttu-id="6c68a-111">Découvrez les nouvelles fonctionnalités de la version d’évaluation de Defender for Endpoint et soyez parmi les premiers à essayer les fonctionnalités à venir en 2013.</span><span class="sxs-lookup"><span data-stu-id="6c68a-111">Learn about new features in the Defender for Endpoint preview release and be among the first to try upcoming features by turning on the preview experience.</span></span>

>[!TIP]
><span data-ttu-id="6c68a-112">Recevez une notification lorsque cette page est mise à jour en copiant et en coller l’URL suivante dans votre lecteur de flux : `/api/search/rss?search=%22In+the+navigation+pane%2C+select+Settings+%3E+Advanced+features+%3E+Preview+features.%22&locale=en-us&facet=`</span><span class="sxs-lookup"><span data-stu-id="6c68a-112">Get notified when this page is updated by copying and pasting the following URL into your feed reader: `/api/search/rss?search=%22In+the+navigation+pane%2C+select+Settings+%3E+Advanced+features+%3E+Preview+features.%22&locale=en-us&facet=`</span></span>

<span data-ttu-id="6c68a-113">Pour plus d’informations sur les nouvelles fonctionnalités généralement disponibles, voir [Nouveautés de Defender pour Point de terminaison.](whats-new-in-microsoft-defender-atp.md)</span><span class="sxs-lookup"><span data-stu-id="6c68a-113">For more information on new capabilities that are generally available, see [What's new in Defender for Endpoint](whats-new-in-microsoft-defender-atp.md).</span></span>

 ## <a name="what-you-need-to-know"></a><span data-ttu-id="6c68a-114">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="6c68a-114">What you need to know</span></span>

<span data-ttu-id="6c68a-115">Lorsque vous travaillez avec des fonctionnalités en prévisualisation publique, ces fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="6c68a-115">When working with features in public preview, these features:</span></span>

- <span data-ttu-id="6c68a-116">Fonctionnalités restreintes ou limitées.</span><span class="sxs-lookup"><span data-stu-id="6c68a-116">May have restricted or limited functionality.</span></span> <span data-ttu-id="6c68a-117">Par exemple, la fonctionnalité ne peut s’appliquer qu’à une seule plateforme.</span><span class="sxs-lookup"><span data-stu-id="6c68a-117">For example, the feature may only apply to one platform.</span></span>
- <span data-ttu-id="6c68a-118">En règle générale, les modifications apportées aux fonctionnalités sont apportées avant d’être généralement disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c68a-118">Typically go through feature changes before they're generally available (GA).</span></span>
- <span data-ttu-id="6c68a-119">Sont entièrement pris en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c68a-119">Are fully supported by Microsoft.</span></span>
- <span data-ttu-id="6c68a-120">Peut être disponible uniquement dans les régions géographiques ou les environnements cloud sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="6c68a-120">May only be available in selected geographic regions or cloud environments.</span></span> <span data-ttu-id="6c68a-121">Par exemple, la fonctionnalité n’existe peut-être pas dans le cloud du gouvernement.</span><span class="sxs-lookup"><span data-stu-id="6c68a-121">For example, the feature may not exist in the government cloud.</span></span>
- <span data-ttu-id="6c68a-122">Les fonctionnalités individuelles en prévisualisation peuvent avoir davantage de restrictions d’utilisation et de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6c68a-122">Individual features in preview may have more usage and support restrictions.</span></span> <span data-ttu-id="6c68a-123">Si tel est le cas, ces informations sont généralement notées dans la documentation des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6c68a-123">If so, this information is typically noted in the feature documentation.</span></span>
- <span data-ttu-id="6c68a-124">Les versions d’aperçu sont fournies avec un niveau de prise en charge standard et peuvent être utilisées pour les environnements de production.</span><span class="sxs-lookup"><span data-stu-id="6c68a-124">The preview versions are provided with a standard support level, and can be used for production environments.</span></span> 



## <a name="turn-on-preview-features"></a><span data-ttu-id="6c68a-125">Activer les fonctionnalités d’aperçu</span><span class="sxs-lookup"><span data-stu-id="6c68a-125">Turn on preview features</span></span>

<span data-ttu-id="6c68a-126">Vous aurez accès aux fonctionnalités à venir sur qui vous pourrez nous faire part de vos commentaires afin d’améliorer l’expérience globale avant que les fonctionnalités ne soient généralement disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c68a-126">You'll have access to upcoming features that you can provide feedback on to help improve the overall experience before features are generally available.</span></span>

<span data-ttu-id="6c68a-127">Activez le paramètre d’expérience de préversion pour être parmi les premiers à essayer les fonctionnalités à venir.</span><span class="sxs-lookup"><span data-stu-id="6c68a-127">Turn on the preview experience setting to be among the first to try upcoming features.</span></span>

1. <span data-ttu-id="6c68a-128">Dans le volet de navigation, **sélectionnez** Paramètres  >  **fonctionnalités avancées d’aperçu.**  >  </span><span class="sxs-lookup"><span data-stu-id="6c68a-128">In the navigation pane, select **Settings** > **Advanced features** > **Preview features**.</span></span>

2. <span data-ttu-id="6c68a-129">Basculez le paramètre entre **« Sur** » et « **Hors** » et sélectionnez Enregistrer **les préférences.**</span><span class="sxs-lookup"><span data-stu-id="6c68a-129">Toggle the setting between **On** and **Off** and select **Save preferences**.</span></span>

## <a name="preview-features"></a><span data-ttu-id="6c68a-130">Fonctionnalités de préversion</span><span class="sxs-lookup"><span data-stu-id="6c68a-130">Preview features</span></span>

<span data-ttu-id="6c68a-131">Les fonctionnalités suivantes sont incluses dans la version préliminaire :</span><span class="sxs-lookup"><span data-stu-id="6c68a-131">The following features are included in the preview release:</span></span>

- [<span data-ttu-id="6c68a-132">Filtrage de contenu Web</span><span class="sxs-lookup"><span data-stu-id="6c68a-132">Web Content Filtering</span></span>](web-content-filtering.md) <br> <span data-ttu-id="6c68a-133">Le filtrage de contenu Web fait partie des fonctionnalités de protection web de Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6c68a-133">Web content filtering is part of web protection capabilities in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="6c68a-134">Il permet à votre organisation de suivre et de contrôler l’accès aux sites web en fonction de leurs catégories de contenu.</span><span class="sxs-lookup"><span data-stu-id="6c68a-134">It enables your organization to track and regulate access to websites based on their content categories.</span></span> <span data-ttu-id="6c68a-135">La plupart de ces sites web, bien qu’ils ne soient pas malveillants, peuvent être problématiques en raison des réglementations de conformité, de l’utilisation de la bande passante ou d’autres problèmes.</span><span class="sxs-lookup"><span data-stu-id="6c68a-135">Many of these websites, while not malicious, might be problematic because of compliance regulations, bandwidth usage, or other concerns.</span></span>

- [<span data-ttu-id="6c68a-136">Rapport d’intégrité et de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="6c68a-136">Device health and compliance report</span></span>](machine-reports.md) <br/> <span data-ttu-id="6c68a-137">Le rapport sur l’état et la conformité de l’appareil fournit des informations de haut niveau sur les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6c68a-137">The device health and compliance report provides high-level information about the devices in your organization.</span></span>

> [!TIP] 
> <span data-ttu-id="6c68a-138">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6c68a-138">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6c68a-139">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6c68a-139">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-preview-belowfoldlink)  
