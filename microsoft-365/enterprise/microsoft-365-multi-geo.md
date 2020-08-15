---
title: Microsoft 365 Multi-Geo
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.custom: seo-marvel-apr2020
ms.collection: Strat_SP_gtc
localization_priority: Normal
f1.keywords:
- NOCSH
description: Dans cet article, Découvrez comment étendre votre présence Microsoft 365 à plusieurs régions géographiques avec Microsoft 365 multi-géo.
ms.openlocfilehash: a5843b98b5d64dfb3872c3d8a5d48c0e56949c02
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690044"
---
# <a name="microsoft-365-multi-geo"></a><span data-ttu-id="52060-103">Microsoft 365 Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="52060-103">Microsoft 365 Multi-Geo</span></span>

<span data-ttu-id="52060-104">Avec Microsoft 365 Multi-Geo, votre organisation peut étendre sa présence Microsoft 365 à plusieurs régions ou pays au sein de votre client existant.</span><span class="sxs-lookup"><span data-stu-id="52060-104">With Microsoft 365 Multi-Geo, your organization can expand its Microsoft 365 presence to multiple geographic regions and/or countries within your existing tenant.</span></span> <span data-ttu-id="52060-105">Pour inscrire votre entreprise internationale à Microsoft 365 Multi-Geo, contactez votre Équipe des comptes Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52060-105">Reach out to your Microsoft Account Team to sign up your Multi-National Company for Microsoft 365 Multi-Geo.</span></span>
  
<span data-ttu-id="52060-106">Microsoft 365 Multi-Geo vous permet d’approvisionner et de stocker des données au repos dans les emplacements géographiques de votre choix afin de répondre à des besoins spécifiques en matière de résidence des données, tout en déverrouillant le déploiement global d’expériences de productivité moderne à vos employés.</span><span class="sxs-lookup"><span data-stu-id="52060-106">With Microsoft 365 Multi-Geo, you can provision and store data at rest in the geo locations that you've chosen to meet data residency requirements, and at the same time unlock your global roll out of modern productivity experiences to your workforce.</span></span>

#### <a name="video-introducing-microsoft-365-multi-geo"></a><span data-ttu-id="52060-107">Vidéo : présentation de Microsoft 365 Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="52060-107">Video: Introducing Microsoft 365 Multi-Geo</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1Yk6B?autoplay=false]

<span data-ttu-id="52060-108">Dans un environnement Multi-Geo, votre client Microsoft 365 se compose d’un emplacement central (où votre abonnement Microsoft 365 d’origine a été approvisionné) et d’un ou plusieurs emplacements satellites.</span><span class="sxs-lookup"><span data-stu-id="52060-108">In a Multi-Geo environment, your Microsoft 365 tenant consists of a central location (where your Microsoft 365 subscription was originally provisioned) and one or more satellite locations.</span></span> <span data-ttu-id="52060-109">Dans un client multigéographique, les informations concernant les emplacements géographiques, les groupes et les informations utilisateur sont gérées dans Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="52060-109">In a multi-geo tenant, the information about geo locations, groups, and user information, is mastered in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="52060-110">Étant donné que les informations de votre client sont gérées de façon centralisée et synchronisées à chaque emplacement géographique, le partage et les expériences concernant tout membre de votre société impliquent une sensibilisation à l’échelle mondiale.</span><span class="sxs-lookup"><span data-stu-id="52060-110">Because your tenant information is mastered centrally and synchronized into each geo location, sharing and experiences involving anyone from your company contain global awareness.</span></span>

![Capture d’écran d’un mappage multigéographique du Centre d’administration SharePoint](../media/multi-geo-world-map.png)

<span data-ttu-id="52060-112">Notez que Microsoft 365 Multi-Geo n’est pas conçu pour optimiser les performances, mais pour répondre aux exigences de résidence des données.</span><span class="sxs-lookup"><span data-stu-id="52060-112">Note that Microsoft 365 Multi-Geo is not designed for performance optimization, it is designed to meet data residency requirements.</span></span> <span data-ttu-id="52060-113">Pour plus d’informations sur l’optimisation des performances pour Microsoft 365, voir [Planification réseau et optimisation des performances pour Microsoft 365](https://support.office.com/article/e5f1228c-da3c-4654-bf16-d163daee8848) ou contacter votre groupe de support.</span><span class="sxs-lookup"><span data-stu-id="52060-113">For information about performance optimization for Microsoft 365, see [Network planning and performance tuning for Microsoft 365](https://support.office.com/article/e5f1228c-da3c-4654-bf16-d163daee8848) or contact your support group.</span></span>

## <a name="terminology"></a><span data-ttu-id="52060-114">Terminologie</span><span class="sxs-lookup"><span data-stu-id="52060-114">Terminology</span></span>

<span data-ttu-id="52060-115">Voici les principaux termes utilisés dans la description de Microsoft 365 Multi-Geo :</span><span class="sxs-lookup"><span data-stu-id="52060-115">Here are the key terms used in describing Microsoft 365 Multi-Geo:</span></span>

- <span data-ttu-id="52060-116">**Emplacement central** : emplacement géographique où votre client a été approvisionné à l’origine.</span><span class="sxs-lookup"><span data-stu-id="52060-116">**Central location** - the geo location where your tenant was originally provisioned.</span></span>
- <span data-ttu-id="52060-117">**Administrateur de zone géographique** : un administrateur pouvant administrer un ou plusieurs emplacements satellites spécifiés.</span><span class="sxs-lookup"><span data-stu-id="52060-117">**Geo administrator** - An administrator who can administer one or more specified satellite locations.</span></span>
- <span data-ttu-id="52060-118">**Géocode** : code de trois lettres correspondant à un emplacement géographique donné.</span><span class="sxs-lookup"><span data-stu-id="52060-118">**Geo code** - a three-letter code for a given geo location.</span></span>
- <span data-ttu-id="52060-119">**Emplacement géographique** : emplacement géographique utilisable dans un client multigéographique pour héberger des données, notamment dans des boîtes aux lettres Exchange et des sites OneDrive ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="52060-119">**Geo location** – A geographic location that can be used in a multi-geo tenant to host data, including Exchange mailboxes and OneDrive and SharePoint sites.</span></span>
- <span data-ttu-id="52060-120">**Emplacement par défaut des données** : propriété d’utilisateur définie par l’administrateur, indiquant l’emplacement géographique où la boîte aux lettres Exchange et le OneDrive des utilisateurs doivent être déployés.</span><span class="sxs-lookup"><span data-stu-id="52060-120">**Preferred Data Location (PDL)** – A user property set by the administrator that indicates where the geo location where the users Exchange mailbox and OneDrive should be provisioned.</span></span> <span data-ttu-id="52060-121">L’emplacement par défaut des données détermine où sont déployés les sites SharePoint créés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52060-121">The PDL also determines where SharePoint sites that are created by the user are provisioned.</span></span>
- <span data-ttu-id="52060-122">**Emplacement satellite** : emplacement géographique où les charges de travail Microsoft 365 sensibles à la zone géographique (SharePoint, OneDrive et Exchange) sont activées dans un client multigéographique.</span><span class="sxs-lookup"><span data-stu-id="52060-122">**Satellite location** – The geo locations where the geo-aware Microsoft 365 workloads (SharePoint, OneDrive, and Exchange) are enabled in a multi-geo tenant.</span></span>
- <span data-ttu-id="52060-123">**Locataire** : représentation d’une organisation dans Microsoft 365 à laquelle sont généralement associés un ou plusieurs domaines (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="52060-123">**Tenant** – An organization's representation in Microsoft 365 which typically has one or more domains associated with it (for example, contoso.com).</span></span>

## <a name="licensing"></a><span data-ttu-id="52060-124">Licence</span><span class="sxs-lookup"><span data-stu-id="52060-124">Licensing</span></span>

<span data-ttu-id="52060-125">Microsoft 365 multi-Geo est disponible sous la forme d’un composant additionnel aux offres d’abonnement Microsoft 365 suivantes pour les clients EA ayant au moins 250 places de Microsoft 365 au sein de leur client, et 5% au minimum de ces sièges utilisant plusieurs Geo.</span><span class="sxs-lookup"><span data-stu-id="52060-125">Microsoft 365 Multi-Geo is available as an add-on to the following Microsoft 365 subscription plans for EA customers with a minimum of 250 Microsoft 365 seats in their tenant, and a minimum of 5% of those seats using multi-geo.</span></span> <span data-ttu-id="52060-126">Pour plus d’informations, contactez l’équipe de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52060-126">Please contact your Microsoft account team for details.</span></span>

- <span data-ttu-id="52060-127">Microsoft 365 F1, E1, E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="52060-127">Microsoft 365 F1, E1, E3, or E5</span></span>
- <span data-ttu-id="52060-128">Exchange Online (plan 1) ou plan 2</span><span class="sxs-lookup"><span data-stu-id="52060-128">Exchange Online Plan 1 or Plan 2</span></span>
- <span data-ttu-id="52060-129">OneDrive entreprise (plan 1 ou plan 2)</span><span class="sxs-lookup"><span data-stu-id="52060-129">OneDrive for Business Plan 1 or Plan 2</span></span>
- <span data-ttu-id="52060-130">SharePoint Online Plan 1 ou Plan 2</span><span class="sxs-lookup"><span data-stu-id="52060-130">SharePoint Online Plan 1 or Plan 2</span></span>

## <a name="microsoft-365-multi-geo-availability"></a><span data-ttu-id="52060-131">Disponibilité de Microsoft 365 Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="52060-131">Microsoft 365 Multi-Geo availability</span></span>

<span data-ttu-id="52060-132">Microsoft 365 Multi-Geo est actuellement disponible dans les régions et pays suivants :</span><span class="sxs-lookup"><span data-stu-id="52060-132">Microsoft 365 Multi-Geo is currently offered in these regions and countries:</span></span>

[!INCLUDE [Microsoft 365 Multi-Geo locations](../includes/microsoft-365-multi-geo-locations.md)]

## <a name="getting-started"></a><span data-ttu-id="52060-133">Prise en main</span><span class="sxs-lookup"><span data-stu-id="52060-133">Getting started</span></span>

<span data-ttu-id="52060-134">Pour commencer à utiliser la fonctionnalité multigéographique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="52060-134">Follow these steps to get started with multi-geo:</span></span>

1. <span data-ttu-id="52060-135">Travailler avec votre équipe de compte pour ajouter le plan de services des _fonctionnalités multigéographiques dans Microsoft 365_.</span><span class="sxs-lookup"><span data-stu-id="52060-135">Work with your account team to add the _Multi-Geo Capabilities in Microsoft 365_ service plan.</span></span> <span data-ttu-id="52060-136">Ils vous guident pour ajouter le nombre de licences nécessaires.</span><span class="sxs-lookup"><span data-stu-id="52060-136">They will guide you to add the number of licenses needed.</span></span> <span data-ttu-id="52060-137">La fonctionnalité Multi-Geo est actuellement disponible pour les clients Contrat Entreprise avec au moins 250 abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="52060-137">Multi-Geo feature is available to EA customers with a minimum of 250 Microsoft 365 subscriptions.</span></span>

   <span data-ttu-id="52060-138">Avant que vous puissiez commencer à utiliser Microsoft 365 Multi-Geo, Microsoft doit configurer votre client Exchange Online afin qu’il bénéficie d’une prise en charge multigéographique.</span><span class="sxs-lookup"><span data-stu-id="52060-138">Before you can start using Microsoft 365 Multi-Geo, Microsoft needs to configure your Exchange Online tenant for multi-geo support.</span></span> <span data-ttu-id="52060-139">Ce processus de configuration est déclenché lorsque vous commandez le plan de services des *fonctionnalités multigéographiques de Microsoft 365* et que les licences apparaissent dans votre client.</span><span class="sxs-lookup"><span data-stu-id="52060-139">This one-time configuration process is triggered after you order the *Multi-Geo Capabilities in Microsoft 365* service plan and the licenses show up in your tenant.</span></span> <span data-ttu-id="52060-140">Une fois vos licences multigéographiques appliquées, vous recevez des notifications dans le [Centre de messages Microsoft 365](https://support.office.com/article/38FB3333-BFCC-4340-A37B-DEDA509C2093) et pouvez commencer à configurer et à utiliser les fonctionnalités multigéographiques de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="52060-140">You'll receive notifications in the [Microsoft 365 message center](https://support.office.com/article/38FB3333-BFCC-4340-A37B-DEDA509C2093) once your Multi-Geo licenses are applied and you then may begin configuring and using your Microsoft 365 Multi-Geo capabilities.</span></span>

2. <span data-ttu-id="52060-141">Lisez [Planifier votre environnement multigéographique](plan-for-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="52060-141">Read [Plan your multi-geo environment](plan-for-multi-geo.md).</span></span>

3. <span data-ttu-id="52060-142">Découvrez [comment administrer un environnement multigéographique](administering-a-multi-geo-environment.md) et [comment vos utilisateurs feront l’expérience de cet environnement](multi-geo-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="52060-142">Learn about [administering a multi-geo environment](administering-a-multi-geo-environment.md) and [how your users will experience the environment](multi-geo-user-experience.md).</span></span>

4. <span data-ttu-id="52060-143">Lorsque vous êtes prêt à configurer Microsoft 365 Multi-Geo, [configurez votre client pour une utilisation multigéographique](multi-geo-tenant-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="52060-143">When you are ready to set up Microsoft 365 Multi-Geo, [configure your tenant for multi-geo](multi-geo-tenant-configuration.md).</span></span>

5. <span data-ttu-id="52060-144">[Configurez la recherche](configure-search-for-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="52060-144">[Set up search](configure-search-for-multi-geo.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="52060-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52060-145">See also</span></span>

[<span data-ttu-id="52060-146">Géo multiple dans Exchange Online et OneDrive</span><span class="sxs-lookup"><span data-stu-id="52060-146">Multi-Geo in Exchange Online and OneDrive</span></span>](https://Aka.ms/GoMultiGeo)

[<span data-ttu-id="52060-147">Fonctionnalités multigéographiques dans OneDrive et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="52060-147">Multi-Geo Capabilities in OneDrive and SharePoint Online</span></span>](multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365.md)

[<span data-ttu-id="52060-148">Fonctionnalités multi-localisés dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="52060-148">Multi-Geo Capabilities in Exchange Online</span></span>](multi-geo-capabilities-in-exchange-online.md)

[<span data-ttu-id="52060-149">Expérience Teams dans un environnement multigéographique</span><span class="sxs-lookup"><span data-stu-id="52060-149">Teams experience in a multi-geo environment</span></span>](https://docs.microsoft.com/microsoftteams/teams-experience-o365odb-spo-multi-geo)
