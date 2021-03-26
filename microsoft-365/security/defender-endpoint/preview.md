---
title: Fonctionnalités d’aperçu de Microsoft Defender ATP
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
ms.openlocfilehash: 4aab7f12b250c1415ad65a9e706edf6b68050b2f
ms.sourcegitcommit: 1244bbc4a3d150d37980cab153505ca462fa7ddc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51222650"
---
# <a name="microsoft-defender-for-endpoint-preview-features"></a><span data-ttu-id="7cc42-104">Fonctionnalités de prévisualisation de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="7cc42-104">Microsoft Defender for Endpoint preview features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

>[!IMPORTANT]
><span data-ttu-id="7cc42-105">Les versions d’aperçu sont fournies sans contrat de niveau de service et ne sont pas recommandées pour les charges de travail de production.</span><span class="sxs-lookup"><span data-stu-id="7cc42-105">The preview versions are provided without a service level agreement, and it's not recommended for production workloads.</span></span> <span data-ttu-id="7cc42-106">Certaines fonctionnalités peuvent ne pas être pris en charge ou avoir des fonctionnalités contraintes.</span><span class="sxs-lookup"><span data-stu-id="7cc42-106">Certain features might not be supported or might have constrained capabilities.</span></span>

<span data-ttu-id="7cc42-107">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7cc42-107">**Applies to:**</span></span>
- [<span data-ttu-id="7cc42-108">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7cc42-108">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7cc42-109">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7cc42-109">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7cc42-110">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7cc42-110">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="7cc42-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7cc42-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="7cc42-112">Le service Defender for Endpoint est constamment mis à jour pour inclure de nouvelles améliorations et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7cc42-112">The Defender for Endpoint service is constantly being updated to include new feature enhancements and capabilities.</span></span>

<span data-ttu-id="7cc42-113">Découvrez les nouvelles fonctionnalités de la version d’évaluation de Defender for Endpoint et soyez parmi les premiers à essayer les fonctionnalités à venir en 2013.</span><span class="sxs-lookup"><span data-stu-id="7cc42-113">Learn about new features in the Defender for Endpoint preview release and be among the first to try upcoming features by turning on the preview experience.</span></span>

>[!TIP]
><span data-ttu-id="7cc42-114">Recevez une notification lorsque cette page est mise à jour en copiant et en coller l’URL suivante dans votre lecteur de flux : `https://docs.microsoft.com/api/search/rss?search=%22Microsoft+Defender+ATP+preview+features%22&locale=en-us`</span><span class="sxs-lookup"><span data-stu-id="7cc42-114">Get notified when this page is updated by copying and pasting the following URL into your feed reader: `https://docs.microsoft.com/api/search/rss?search=%22Microsoft+Defender+ATP+preview+features%22&locale=en-us`</span></span>

<span data-ttu-id="7cc42-115">Pour plus d’informations sur les nouvelles fonctionnalités généralement disponibles, voir [Nouveautés de Defender pour Point de terminaison.](whats-new-in-microsoft-defender-atp.md)</span><span class="sxs-lookup"><span data-stu-id="7cc42-115">For more information on new capabilities that are generally available, see [What's new in Defender for Endpoint](whats-new-in-microsoft-defender-atp.md).</span></span>

## <a name="turn-on-preview-features"></a><span data-ttu-id="7cc42-116">Activer les fonctionnalités d’aperçu</span><span class="sxs-lookup"><span data-stu-id="7cc42-116">Turn on preview features</span></span>

<span data-ttu-id="7cc42-117">Vous aurez accès aux fonctionnalités à venir sur qui vous pourrez nous faire part de vos commentaires afin d’améliorer l’expérience globale avant que les fonctionnalités ne soient généralement disponibles.</span><span class="sxs-lookup"><span data-stu-id="7cc42-117">You'll have access to upcoming features that you can provide feedback on to help improve the overall experience before features are generally available.</span></span>

<span data-ttu-id="7cc42-118">Activez le paramètre d’expérience de préversion pour être parmi les premiers à essayer les fonctionnalités à venir.</span><span class="sxs-lookup"><span data-stu-id="7cc42-118">Turn on the preview experience setting to be among the first to try upcoming features.</span></span>

1. <span data-ttu-id="7cc42-119">Dans le volet de navigation, sélectionnez **Paramètres**  >  **avancés fonctionnalités**  >  **d’aperçu.**</span><span class="sxs-lookup"><span data-stu-id="7cc42-119">In the navigation pane, select **Settings** > **Advanced features** > **Preview features**.</span></span>

2. <span data-ttu-id="7cc42-120">Basculez le paramètre entre **« Sur** » et « **Hors** » et sélectionnez Enregistrer **les préférences.**</span><span class="sxs-lookup"><span data-stu-id="7cc42-120">Toggle the setting between **On** and **Off** and select **Save preferences**.</span></span>

## <a name="preview-features"></a><span data-ttu-id="7cc42-121">Fonctionnalités de préversion</span><span class="sxs-lookup"><span data-stu-id="7cc42-121">Preview features</span></span>

<span data-ttu-id="7cc42-122">Les fonctionnalités suivantes sont incluses dans la version préliminaire :</span><span class="sxs-lookup"><span data-stu-id="7cc42-122">The following features are included in the preview release:</span></span>

- [<span data-ttu-id="7cc42-123">Filtrage de contenu Web</span><span class="sxs-lookup"><span data-stu-id="7cc42-123">Web Content Filtering</span></span>](web-content-filtering.md) <br> <span data-ttu-id="7cc42-124">Le filtrage de contenu Web fait partie des fonctionnalités de protection web de Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="7cc42-124">Web content filtering is part of web protection capabilities in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="7cc42-125">Il permet à votre organisation de suivre et de contrôler l’accès aux sites web en fonction de leurs catégories de contenu.</span><span class="sxs-lookup"><span data-stu-id="7cc42-125">It enables your organization to track and regulate access to websites based on their content categories.</span></span> <span data-ttu-id="7cc42-126">La plupart de ces sites web, bien que non malveillants, peuvent être problématiques en raison des réglementations de conformité, de l’utilisation de la bande passante ou d’autres problèmes.</span><span class="sxs-lookup"><span data-stu-id="7cc42-126">Many of these websites, while not malicious, might be problematic because of compliance regulations, bandwidth usage, or other concerns.</span></span>

- [<span data-ttu-id="7cc42-127">Rapport sur l’état et la conformité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="7cc42-127">Device health and compliance report</span></span>](machine-reports.md) <br/> <span data-ttu-id="7cc42-128">Le rapport sur l’état et la conformité de l’appareil fournit des informations de haut niveau sur les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7cc42-128">The device health and compliance report provides high-level information about the devices in your organization.</span></span>

> [!TIP] 
> <span data-ttu-id="7cc42-129">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7cc42-129">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="7cc42-130">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7cc42-130">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-preview-belowfoldlink)  
