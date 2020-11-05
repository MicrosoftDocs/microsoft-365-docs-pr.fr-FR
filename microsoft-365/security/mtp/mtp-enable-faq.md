---
title: Forum aux questions lors de l’activation de Microsoft 365 Defender
description: Obtenez des réponses aux questions les plus fréquemment posées sur la gestion des licences, des autorisations, des paramètres initiaux et d’autres produits et services liés à l’activation de Microsoft 365 Defender
keywords: Forum aux questions, FAQ, GCC, mise en route, activer le MTP, protection Microsoft contre les menaces, M365, sécurité, emplacement des données, autorisations requises, éligibilité de la licence, page Paramètres
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
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
ms.openlocfilehash: 3dae9f208f5bb08d694322eb9f7cff35986930da
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920489"
---
# <a name="frequently-asked-questions-when-turning-on-microsoft-365-defender"></a><span data-ttu-id="3d71a-104">Forum aux questions lors de l’activation de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3d71a-104">Frequently asked questions when turning on Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="3d71a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3d71a-105">**Applies to:**</span></span>
- <span data-ttu-id="3d71a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3d71a-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="3d71a-107">Lisez les réponses aux questions les plus fréquemment posées sur l’activation de [Microsoft 365 Defender](microsoft-threat-protection.md), notamment les licences et autorisations requises, le déploiement des services de prise en charge et les paramètres initiaux.</span><span class="sxs-lookup"><span data-stu-id="3d71a-107">Read responses to the most commonly asked questions about turning on [Microsoft 365 Defender](microsoft-threat-protection.md), including required licenses and permissions, deploying support services, and initial settings.</span></span>

<span data-ttu-id="3d71a-108">Pour obtenir des instructions sur la façon d’activer le service, [Lisez activer Microsoft 365 Defender](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="3d71a-108">For instructions on how to turn on the service, [read Turn on Microsoft 365 Defender](mtp-enable.md).</span></span>

## <a name="i-dont-have-a-microsoft-365-e5-license-can-i-still-use-microsoft-365-defender"></a><span data-ttu-id="3d71a-109">Je n’ai pas de licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="3d71a-109">I don’t have a Microsoft 365 E5 license.</span></span> <span data-ttu-id="3d71a-110">Puis-je toujours utiliser Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-110">Can I still use Microsoft 365 Defender?</span></span>

<span data-ttu-id="3d71a-111">Les clients disposant des licences non E5 suivantes peuvent utiliser Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="3d71a-111">Customers with the following non-E5 licenses can use Microsoft 365 Defender:</span></span>

- <span data-ttu-id="3d71a-112">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3d71a-112">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="3d71a-113">Microsoft Defender pour identité</span><span class="sxs-lookup"><span data-stu-id="3d71a-113">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="3d71a-114">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3d71a-114">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="3d71a-115">Defender pour Office 365 (plan 2)</span><span class="sxs-lookup"><span data-stu-id="3d71a-115">Defender for Office 365 (Plan 2)</span></span>
 
<span data-ttu-id="3d71a-116">Pour obtenir la liste complète des licences prises en charge, [Lisez les conditions requises en matière de licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="3d71a-116">For a full list of supported licenses, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

## <a name="do-i-need-to-install-or-deploy-anything-to-start-using-microsoft-365-defender"></a><span data-ttu-id="3d71a-117">Dois-je installer ou déployer quoi que ce soit pour commencer à utiliser Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-117">Do I need to install or deploy anything to start using Microsoft 365 Defender?</span></span>

<span data-ttu-id="3d71a-118">Non, Microsoft 365 Defender consolide les données des services de sécurité Microsoft 365 que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="3d71a-118">No, Microsoft 365 Defender consolidates data from Microsoft 365 security services that you have already deployed.</span></span> <span data-ttu-id="3d71a-119">Une fois que vous l’activez, l’incident, l’automatisation et l’expérience de la chasse commenceront à fonctionner dans l’étendue des produits déployés.</span><span class="sxs-lookup"><span data-stu-id="3d71a-119">Once you turn it on, incident, automation, and hunting experiences will start working within the scope of the deployed products.</span></span> <span data-ttu-id="3d71a-120">Si aucun de ces produits n’est déployé correctement, Microsoft 365 Defender n’affiche pas de données et ne peut effectuer aucune action.</span><span class="sxs-lookup"><span data-stu-id="3d71a-120">If none of these products are properly deployed, Microsoft 365 Defender will not display any data and is unable to take any action.</span></span>

<span data-ttu-id="3d71a-121">Pour optimiser vos expériences Microsoft 365 Defender, nous vous recommandons de déployer *tous les* [produits et services de sécurité Microsoft 365](deploy-supported-services.md)pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3d71a-121">To optimize your Microsoft 365 Defender experiences, we recommend deploying *all* supported [Microsoft 365 security products and services](deploy-supported-services.md).</span></span>

## <a name="where-does-microsoft-365-defender-process-and-store-my-data"></a><span data-ttu-id="3d71a-122">Où Microsoft 365 Defender traite-t-il et stocke-t-il mes données ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-122">Where does Microsoft 365 Defender process and store my data?</span></span>
<span data-ttu-id="3d71a-123">Microsoft 365 Defender sélectionne automatiquement un emplacement optimal pour le centre de données où les données consolidées sont traitées et stockées.</span><span class="sxs-lookup"><span data-stu-id="3d71a-123">Microsoft 365 Defender automatically selects an optimal location for the data center where consolidated data is processed and stored.</span></span> <span data-ttu-id="3d71a-124">Si vous disposez de Microsoft Defender for Endpoint, il sélectionne le même emplacement que celui utilisé par Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="3d71a-124">If you have Microsoft Defender for Endpoint, it selects the same location used by Defender for Endpoint.</span></span>

>[!NOTE]
><span data-ttu-id="3d71a-125">Microsoft Defender for Endpoint provisions automatiques dans les centres de données de l’Union européenne (UE) lors de l’activation via Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="3d71a-125">Microsoft Defender for Endpoint automatically provisions in European Union (EU) data centers when turned on through Azure Defender.</span></span> <span data-ttu-id="3d71a-126">Microsoft 365 Defender est automatiquement mis en service dans le même centre de données UE pour les clients qui ont configuré Microsoft Defender pour un point de terminaison de cette manière.</span><span class="sxs-lookup"><span data-stu-id="3d71a-126">Microsoft 365 Defender will automatically provision in the same EU data center for customers who have provisioned Microsoft Defender for Endpoint in this manner.</span></span> 

<span data-ttu-id="3d71a-127">L’emplacement du centre de données est affiché avant et après la mise en service du service dans la page Paramètres de Microsoft 365 Defender ( **paramètres > microsoft 365 Defender** ).</span><span class="sxs-lookup"><span data-stu-id="3d71a-127">The data center location is shown before and after the service is provisioned in the settings page for Microsoft 365 Defender ( **Settings > Microsoft 365 Defender** ).</span></span> <span data-ttu-id="3d71a-128">Si vous préférez utiliser un autre emplacement pour les centres de données, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365 pour contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d71a-128">If you prefer to use another data center location, select **Need help?** in the Microsoft 365 security center to contact Microsoft support.</span></span>

## <a name="where-can-i-access-microsoft-365-defender"></a><span data-ttu-id="3d71a-129">Où puis-je accéder à Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-129">Where can I access Microsoft 365 Defender?</span></span>

<span data-ttu-id="3d71a-130">Microsoft 365 Defender est disponible dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d71a-130">Microsoft 365 Defender is available in Microsoft 365 security center.</span></span> <span data-ttu-id="3d71a-131">Pour accéder au centre de sécurité, accédez à l’URL [https://security.microsoft.com](https://security.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="3d71a-131">To go to the security center, browse to the URL [https://security.microsoft.com](https://security.microsoft.com).</span></span>

##  <a name="what-permissions-do-i-need-to-access-microsoft-365-defender-in-microsoft-365-security-center"></a><span data-ttu-id="3d71a-132">Quelles sont les autorisations nécessaires pour accéder à Microsoft 365 Defender dans le centre de sécurité Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-132">What permissions do I need to access Microsoft 365 Defender in Microsoft 365 security center?</span></span>

<span data-ttu-id="3d71a-133">Comptes affectés les rôles Azure Active Directory (AD) suivants peuvent accéder aux fonctionnalités et aux données de Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="3d71a-133">Accounts assigned the following Azure Active Directory (AD) roles can access Microsoft 365 Defender functionality and data:</span></span>

- <span data-ttu-id="3d71a-134">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="3d71a-134">Global administrator</span></span>
- <span data-ttu-id="3d71a-135">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3d71a-135">Security administrator</span></span>
- <span data-ttu-id="3d71a-136">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3d71a-136">Security Operator</span></span>
- <span data-ttu-id="3d71a-137">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="3d71a-137">Global Reader</span></span>
- <span data-ttu-id="3d71a-138">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3d71a-138">Security Reader</span></span>

>[!NOTE]
><span data-ttu-id="3d71a-139">Les paramètres de contrôle d’accès basé sur un rôle dans Microsoft Defender pour le point de terminaison influent sur l’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="3d71a-139">Role-based access control settings in Microsoft Defender for Endpoint influence access to data.</span></span> <span data-ttu-id="3d71a-140">Pour plus d’informations, consultez la rubrique [Managing Access to Microsoft 365 Defender](mtp-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3d71a-140">For more information, read about [managing access to Microsoft 365 Defender](mtp-permissions.md).</span></span>

## <a name="what-time-zone-does-microsoft-365-defender-default-to"></a><span data-ttu-id="3d71a-141">Sur quels fuseaux horaires la valeur par défaut de Microsoft 365 Defender est-elle définie ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-141">What time zone does Microsoft 365 Defender default to?</span></span>
<span data-ttu-id="3d71a-142">Par défaut, Microsoft 365 Defender affiche les informations d’heure dans le fuseau horaire UTC.</span><span class="sxs-lookup"><span data-stu-id="3d71a-142">By default, Microsoft 365 Defender displays time information in the UTC time zone.</span></span> <span data-ttu-id="3d71a-143">Vous pouvez modifier ce paramètre pour utiliser votre fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="3d71a-143">You can change this setting to use your local time zone.</span></span> [<span data-ttu-id="3d71a-144">En savoir plus sur la définition du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="3d71a-144">Learn about setting the time zone</span></span>](mtp-time-zone.md)

## <a name="how-can-i-learn-about-new-microsoft-365-defender-feature-and-ui-updates"></a><span data-ttu-id="3d71a-145">Comment puis-je en savoir plus sur la nouvelle fonctionnalité de Microsoft 365 Defender et les mises à jour de l’interface utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-145">How can I learn about new Microsoft 365 Defender feature and UI updates?</span></span>

<span data-ttu-id="3d71a-146">Microsoft fournit régulièrement des informations par le biais des différents canaux, notamment :</span><span class="sxs-lookup"><span data-stu-id="3d71a-146">Microsoft regularly provides information through the various channels, including:</span></span>

- <span data-ttu-id="3d71a-147">[Centre de messages](../../admin/manage/message-center.md) dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3d71a-147">The [message center](../../admin/manage/message-center.md) in Microsoft 365 admin center</span></span>
- <span data-ttu-id="3d71a-148">Blogposts dans la [communauté technique de conformité des & de sécurité Microsoft 365](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/bg-p/securityprivacycompliance)</span><span class="sxs-lookup"><span data-stu-id="3d71a-148">Blogposts in the [Microsoft 365 security & compliance tech community](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/bg-p/securityprivacycompliance)</span></span>

<span data-ttu-id="3d71a-149">Obtenez les dernières expériences disponibles sur le public en activant l' [aperçu des fonctionnalités](preview.md).</span><span class="sxs-lookup"><span data-stu-id="3d71a-149">Get the latest publicly available experiences by turning on [preview features](preview.md).</span></span>

## <a name="is-microsoft-365-defender-available-for-us-government-community-cloud-gcc-or-gcc-high"></a><span data-ttu-id="3d71a-150">Microsoft 365 Defender est-il disponible pour le Cloud Community Government (GCC) ou GCC High ?</span><span class="sxs-lookup"><span data-stu-id="3d71a-150">Is Microsoft 365 Defender available for US Government Community Cloud (GCC) or GCC High?</span></span>
<span data-ttu-id="3d71a-151">Il n’est pas disponible pour le moment.</span><span class="sxs-lookup"><span data-stu-id="3d71a-151">At the moment, it is not available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d71a-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d71a-152">Related topics</span></span>

- [<span data-ttu-id="3d71a-153">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3d71a-153">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
- <span data-ttu-id="3d71a-154">[Activez Microsoft 365 Defender](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="3d71a-154">[Turn on Microsoft 365 Defender](mtp-enable.md).</span></span>
- [<span data-ttu-id="3d71a-155">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="3d71a-155">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="3d71a-156">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d71a-156">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="3d71a-157">Activer les fonctionnalités d’aperçu</span><span class="sxs-lookup"><span data-stu-id="3d71a-157">Turn on preview features</span></span>](preview.md)
