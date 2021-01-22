---
title: Questions fréquemment posées lors de l' turning on Microsoft 365 Defender
description: Obtenez des réponses aux questions les plus fréquemment posées sur la gestion des licences, les autorisations, les paramètres initiaux et d’autres produits et services liés à l’activation de Microsoft 365 Defender
keywords: forum aux questions, FAQ, GCC, commencer, activer MTP, Protection Microsoft contre les menaces, M365, sécurité, emplacement des données, autorisations requises, éligibilité aux licences, page paramètres
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 2cb9aed070959644e3660188835386118d5f4d9b
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930185"
---
# <a name="frequently-asked-questions-when-turning-on-microsoft-365-defender"></a><span data-ttu-id="edf5c-104">Questions fréquemment posées lors de l' turning on Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="edf5c-104">Frequently asked questions when turning on Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="edf5c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="edf5c-105">**Applies to:**</span></span>
- <span data-ttu-id="edf5c-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="edf5c-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="edf5c-107">Lisez les réponses aux questions les plus fréquemment posées sur l’utilisation de [Microsoft 365 Defender,](microsoft-threat-protection.md)y compris les licences et autorisations requises, le déploiement des services de support et les paramètres initiaux.</span><span class="sxs-lookup"><span data-stu-id="edf5c-107">Read responses to the most commonly asked questions about turning on [Microsoft 365 Defender](microsoft-threat-protection.md), including required licenses and permissions, deploying support services, and initial settings.</span></span>

<span data-ttu-id="edf5c-108">Pour obtenir des instructions sur la façon d’activer le service, lisez [Activer Microsoft 365 Defender.](mtp-enable.md)</span><span class="sxs-lookup"><span data-stu-id="edf5c-108">For instructions on how to turn on the service, [read Turn on Microsoft 365 Defender](mtp-enable.md).</span></span>

## <a name="i-dont-have-a-microsoft-365-e5-license-can-i-still-use-microsoft-365-defender"></a><span data-ttu-id="edf5c-109">Je n’ai pas de licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="edf5c-109">I don’t have a Microsoft 365 E5 license.</span></span> <span data-ttu-id="edf5c-110">Puis-je toujours utiliser Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-110">Can I still use Microsoft 365 Defender?</span></span>

<span data-ttu-id="edf5c-111">Les clients titulaires des licences non E5 suivantes peuvent utiliser Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="edf5c-111">Customers with the following non-E5 licenses can use Microsoft 365 Defender:</span></span>

- <span data-ttu-id="edf5c-112">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="edf5c-112">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="edf5c-113">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="edf5c-113">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="edf5c-114">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="edf5c-114">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="edf5c-115">Defender pour Office 365 (Plan 2)</span><span class="sxs-lookup"><span data-stu-id="edf5c-115">Defender for Office 365 (Plan 2)</span></span>
 
<span data-ttu-id="edf5c-116">Pour obtenir la liste complète des licences pris en charge, [lisez les conditions requises pour les licences.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="edf5c-116">For a full list of supported licenses, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

## <a name="do-i-need-to-install-or-deploy-anything-to-start-using-microsoft-365-defender"></a><span data-ttu-id="edf5c-117">Dois-je installer ou déployer quoi que ce soit pour commencer à utiliser Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-117">Do I need to install or deploy anything to start using Microsoft 365 Defender?</span></span>

<span data-ttu-id="edf5c-118">Non, Microsoft 365 Defender consolide les données des services de sécurité Microsoft 365 que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="edf5c-118">No, Microsoft 365 Defender consolidates data from Microsoft 365 security services that you have already deployed.</span></span> <span data-ttu-id="edf5c-119">Une fois que vous l’avez mis en place, les expériences d’incident, d’automatisation et de recherche commenceront à fonctionner dans l’étendue des produits déployés.</span><span class="sxs-lookup"><span data-stu-id="edf5c-119">Once you turn it on, incident, automation, and hunting experiences will start working within the scope of the deployed products.</span></span> <span data-ttu-id="edf5c-120">Si aucun de ces produits n’est correctement déployé, Microsoft 365 Defender n’affiche aucune donnée et ne peut pas prendre d’action.</span><span class="sxs-lookup"><span data-stu-id="edf5c-120">If none of these products are properly deployed, Microsoft 365 Defender will not display any data and is unable to take any action.</span></span>

<span data-ttu-id="edf5c-121">Pour optimiser vos expériences Microsoft 365  Defender, nous vous recommandons de déployer tous les produits et services de sécurité [Microsoft 365 pris en charge.](deploy-supported-services.md)</span><span class="sxs-lookup"><span data-stu-id="edf5c-121">To optimize your Microsoft 365 Defender experiences, we recommend deploying *all* supported [Microsoft 365 security products and services](deploy-supported-services.md).</span></span>

## <a name="where-does-microsoft-365-defender-process-and-store-my-data"></a><span data-ttu-id="edf5c-122">Où Microsoft 365 Defender peut-il traiter et stocker mes données ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-122">Where does Microsoft 365 Defender process and store my data?</span></span>
<span data-ttu-id="edf5c-123">Microsoft 365 Defender sélectionne automatiquement un emplacement optimal pour le centre de données où les données consolidées sont traitées et stockées.</span><span class="sxs-lookup"><span data-stu-id="edf5c-123">Microsoft 365 Defender automatically selects an optimal location for the data center where consolidated data is processed and stored.</span></span> <span data-ttu-id="edf5c-124">Si vous avez Microsoft Defender pour point de terminaison, il sélectionne le même emplacement que celui utilisé par Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="edf5c-124">If you have Microsoft Defender for Endpoint, it selects the same location used by Defender for Endpoint.</span></span>

>[!NOTE]
><span data-ttu-id="edf5c-125">Microsoft Defender pour le point de terminaison met automatiquement en services les centres de données de l’Union européenne (UE) lorsqu’il est allumé par le biais d’Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="edf5c-125">Microsoft Defender for Endpoint automatically provisions in European Union (EU) data centers when turned on through Azure Defender.</span></span> <span data-ttu-id="edf5c-126">Microsoft 365 Defender sera automatiquement mis en service dans le même centre de données de l’UE pour les clients qui ont mis en service Microsoft Defender pour endpoint de cette manière.</span><span class="sxs-lookup"><span data-stu-id="edf5c-126">Microsoft 365 Defender will automatically provision in the same EU data center for customers who have provisioned Microsoft Defender for Endpoint in this manner.</span></span> 

<span data-ttu-id="edf5c-127">L’emplacement du centre de données s’affiche avant et après la mise en service du service dans la page des paramètres de Microsoft 365 Defender ( Paramètres >**Microsoft 365 Defender**).</span><span class="sxs-lookup"><span data-stu-id="edf5c-127">The data center location is shown before and after the service is provisioned in the settings page for Microsoft 365 Defender (**Settings > Microsoft 365 Defender**).</span></span> <span data-ttu-id="edf5c-128">Si vous préférez utiliser un autre emplacement de centre de données, sélectionnez Besoin d’aide **?** dans le Centre de sécurité Microsoft 365 pour contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="edf5c-128">If you prefer to use another data center location, select **Need help?** in the Microsoft 365 security center to contact Microsoft support.</span></span>

## <a name="where-can-i-access-microsoft-365-defender"></a><span data-ttu-id="edf5c-129">Où puis-je accéder à Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-129">Where can I access Microsoft 365 Defender?</span></span>

<span data-ttu-id="edf5c-130">Microsoft 365 Defender est disponible dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="edf5c-130">Microsoft 365 Defender is available in Microsoft 365 security center.</span></span> <span data-ttu-id="edf5c-131">Pour accéder au centre de sécurité, accédez à [https://security.microsoft.com](https://security.microsoft.com) l’URL.</span><span class="sxs-lookup"><span data-stu-id="edf5c-131">To go to the security center, browse to the URL [https://security.microsoft.com](https://security.microsoft.com).</span></span>

##  <a name="what-permissions-do-i-need-to-access-microsoft-365-defender-in-microsoft-365-security-center"></a><span data-ttu-id="edf5c-132">De quelles autorisations ai-je besoin pour accéder à Microsoft 365 Defender dans le Centre de sécurité Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-132">What permissions do I need to access Microsoft 365 Defender in Microsoft 365 security center?</span></span>

<span data-ttu-id="edf5c-133">Les comptes affectés aux rôles Azure Active Directory (AD) suivants peuvent accéder aux fonctionnalités et données de Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="edf5c-133">Accounts assigned the following Azure Active Directory (AD) roles can access Microsoft 365 Defender functionality and data:</span></span>

- <span data-ttu-id="edf5c-134">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="edf5c-134">Global administrator</span></span>
- <span data-ttu-id="edf5c-135">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="edf5c-135">Security administrator</span></span>
- <span data-ttu-id="edf5c-136">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="edf5c-136">Security Operator</span></span>
- <span data-ttu-id="edf5c-137">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="edf5c-137">Global Reader</span></span>
- <span data-ttu-id="edf5c-138">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="edf5c-138">Security Reader</span></span>

>[!NOTE]
><span data-ttu-id="edf5c-139">Les paramètres de contrôle d’accès en fonction du rôle dans Microsoft Defender pour point de terminaison influencent l’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="edf5c-139">Role-based access control settings in Microsoft Defender for Endpoint influence access to data.</span></span> <span data-ttu-id="edf5c-140">Pour plus d’informations, voir [la gestion de l’accès à Microsoft 365 Defender.](mtp-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="edf5c-140">For more information, read about [managing access to Microsoft 365 Defender](mtp-permissions.md).</span></span>

## <a name="what-time-zone-does-microsoft-365-defender-default-to"></a><span data-ttu-id="edf5c-141">Quel fuseau horaire Microsoft 365 Defender utilise-t-il par défaut ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-141">What time zone does Microsoft 365 Defender default to?</span></span>
<span data-ttu-id="edf5c-142">Par défaut, Microsoft 365 Defender affiche les informations d’heure dans le fuseau horaire UTC.</span><span class="sxs-lookup"><span data-stu-id="edf5c-142">By default, Microsoft 365 Defender displays time information in the UTC time zone.</span></span> <span data-ttu-id="edf5c-143">Vous pouvez modifier ce paramètre pour utiliser votre fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="edf5c-143">You can change this setting to use your local time zone.</span></span> [<span data-ttu-id="edf5c-144">En savoir plus sur la définition du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="edf5c-144">Learn about setting the time zone</span></span>](mtp-time-zone.md)

## <a name="how-can-i-learn-about-new-microsoft-365-defender-feature-and-ui-updates"></a><span data-ttu-id="edf5c-145">Comment puis-je en savoir plus sur les nouvelles fonctionnalités de Microsoft 365 Defender et les mises à jour de l’interface utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-145">How can I learn about new Microsoft 365 Defender feature and UI updates?</span></span>

<span data-ttu-id="edf5c-146">Microsoft fournit régulièrement des informations via les différents canaux, notamment :</span><span class="sxs-lookup"><span data-stu-id="edf5c-146">Microsoft regularly provides information through the various channels, including:</span></span>

- <span data-ttu-id="edf5c-147">Centre [de messages](../../admin/manage/message-center.md) dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="edf5c-147">The [message center](../../admin/manage/message-center.md) in Microsoft 365 admin center</span></span>
- <span data-ttu-id="edf5c-148">Billets de blog dans la communauté technique de sécurité et [conformité & Microsoft 365](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/bg-p/securityprivacycompliance)</span><span class="sxs-lookup"><span data-stu-id="edf5c-148">Blogposts in the [Microsoft 365 security & compliance tech community](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/bg-p/securityprivacycompliance)</span></span>

<span data-ttu-id="edf5c-149">Obtenez les dernières expériences disponibles publiquement en allumer les [fonctionnalités d’aperçu.](preview.md)</span><span class="sxs-lookup"><span data-stu-id="edf5c-149">Get the latest publicly available experiences by turning on [preview features](preview.md).</span></span>

## <a name="is-microsoft-365-defender-available-for-us-government-community-cloud-gcc-or-gcc-high"></a><span data-ttu-id="edf5c-150">Microsoft 365 Defender est-il disponible pour le cloud communautaire du gouvernement américain (GCC) ou GCC High ?</span><span class="sxs-lookup"><span data-stu-id="edf5c-150">Is Microsoft 365 Defender available for US Government Community Cloud (GCC) or GCC High?</span></span>
<span data-ttu-id="edf5c-151">Il n’est pas disponible pour le moment.</span><span class="sxs-lookup"><span data-stu-id="edf5c-151">At the moment, it is not available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edf5c-152">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="edf5c-152">Related topics</span></span>

- [<span data-ttu-id="edf5c-153">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="edf5c-153">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
- <span data-ttu-id="edf5c-154">[Activer Microsoft 365 Defender.](mtp-enable.md)</span><span class="sxs-lookup"><span data-stu-id="edf5c-154">[Turn on Microsoft 365 Defender](mtp-enable.md).</span></span>
- [<span data-ttu-id="edf5c-155">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="edf5c-155">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="edf5c-156">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf5c-156">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="edf5c-157">Activer les fonctionnalités d’aperçu</span><span class="sxs-lookup"><span data-stu-id="edf5c-157">Turn on preview features</span></span>](preview.md)
