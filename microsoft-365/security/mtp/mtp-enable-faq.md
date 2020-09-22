---
title: Forum aux questions lors de l’activation de la protection contre les menaces Microsoft
description: Obtenez des réponses aux questions les plus fréquemment posées sur la gestion des licences, des autorisations, des paramètres initiaux et d’autres produits et services liés à l’activation de la protection contre les menaces Microsoft.
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
ms.openlocfilehash: 6b0d8d9be0cc84e61a3228f79fc14f1bfc9f8a83
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48198838"
---
# <a name="frequently-asked-questions-when-turning-on-microsoft-threat-protection"></a><span data-ttu-id="13274-104">Forum aux questions lors de l’activation de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="13274-104">Frequently asked questions when turning on Microsoft Threat Protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="13274-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="13274-105">**Applies to:**</span></span>
- <span data-ttu-id="13274-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="13274-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="13274-107">Lisez les réponses aux questions les plus fréquemment posées sur l’activation de la [protection contre les menaces Microsoft](microsoft-threat-protection.md), y compris les licences et autorisations requises, le déploiement des services de support et les paramètres initiaux.</span><span class="sxs-lookup"><span data-stu-id="13274-107">Read responses to the most commonly asked questions about turning on [Microsoft Threat Protection](microsoft-threat-protection.md), including required licenses and permissions, deploying support services, and initial settings.</span></span>

<span data-ttu-id="13274-108">Pour obtenir des instructions sur la façon d’activer le service, [Lisez activer la protection contre les menaces Microsoft](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="13274-108">For instructions on how to turn on the service, [read Turn on Microsoft Threat Protection](mtp-enable.md).</span></span>

## <a name="i-dont-have-a-microsoft-365-e5-license-can-i-still-use-microsoft-threat-protection"></a><span data-ttu-id="13274-109">Je n’ai pas de licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="13274-109">I don’t have a Microsoft 365 E5 license.</span></span> <span data-ttu-id="13274-110">Puis-je toujours utiliser Microsoft Threat Protection ?</span><span class="sxs-lookup"><span data-stu-id="13274-110">Can I still use Microsoft Threat Protection?</span></span>

<span data-ttu-id="13274-111">Les clients disposant des licences non E5 suivantes peuvent utiliser Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="13274-111">Customers with the following non-E5 licenses can use Microsoft Threat Protection:</span></span>

- <span data-ttu-id="13274-112">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="13274-112">Microsoft Defender Advanced Threat Protection</span></span>
- <span data-ttu-id="13274-113">Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="13274-113">Azure Advanced Threat Protection</span></span>
- <span data-ttu-id="13274-114">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="13274-114">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="13274-115">Office 365 – Protection avancée contre les menaces (plan 2)</span><span class="sxs-lookup"><span data-stu-id="13274-115">Office 365 Advanced Threat Protection (Plan 2)</span></span>
 
<span data-ttu-id="13274-116">Pour obtenir la liste complète des licences prises en charge, [Lisez les conditions requises en matière de licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="13274-116">For a full list of supported licenses, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

## <a name="do-i-need-to-install-or-deploy-anything-to-start-using-microsoft-threat-protection"></a><span data-ttu-id="13274-117">Dois-je installer ou déployer quoi que ce soit pour commencer à utiliser Microsoft Threat Protection ?</span><span class="sxs-lookup"><span data-stu-id="13274-117">Do I need to install or deploy anything to start using Microsoft Threat Protection?</span></span>

<span data-ttu-id="13274-118">Non, Microsoft Threat Protection consolide les données des services de sécurité Microsoft 365 que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="13274-118">No, Microsoft Threat Protection consolidates data from Microsoft 365 security services that you have already deployed.</span></span> <span data-ttu-id="13274-119">Une fois que vous l’activez, l’incident, l’automatisation et l’expérience de la chasse commenceront à fonctionner dans l’étendue des produits déployés.</span><span class="sxs-lookup"><span data-stu-id="13274-119">Once you turn it on, incident, automation, and hunting experiences will start working within the scope of the deployed products.</span></span> <span data-ttu-id="13274-120">Si aucun de ces produits n’est déployé correctement, la protection de Microsoft contre les menaces n’affichera pas de données et ne pourra effectuer aucune action.</span><span class="sxs-lookup"><span data-stu-id="13274-120">If none of these products are properly deployed, Microsoft Threat Protection will not display any data and is unable to take any action.</span></span>

<span data-ttu-id="13274-121">Pour optimiser vos expériences de protection contre les menaces Microsoft, nous vous recommandons de déployer *tous les* [produits et services de sécurité Microsoft 365](deploy-supported-services.md)pris en charge.</span><span class="sxs-lookup"><span data-stu-id="13274-121">To optimize your Microsoft Threat Protection experiences, we recommend deploying *all* supported [Microsoft 365 security products and services](deploy-supported-services.md).</span></span>

## <a name="where-does-microsoft-threat-protection-process-and-store-my-data"></a><span data-ttu-id="13274-122">Où le processus de protection contre les menaces Microsoft et stocke-t-il mes données ?</span><span class="sxs-lookup"><span data-stu-id="13274-122">Where does Microsoft Threat Protection process and store my data?</span></span>
<span data-ttu-id="13274-123">La protection contre les menaces Microsoft sélectionne automatiquement un emplacement optimal pour le centre de données où les données consolidées sont traitées et stockées.</span><span class="sxs-lookup"><span data-stu-id="13274-123">Microsoft Threat Protection automatically selects an optimal location for the data center where consolidated data is processed and stored.</span></span> <span data-ttu-id="13274-124">Si vous disposez de Microsoft Defender ATP, il sélectionne le même emplacement que celui utilisé par Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="13274-124">If you have Microsoft Defender ATP, it selects the same location used by Microsoft Defender ATP.</span></span>

>[!NOTE]
><span data-ttu-id="13274-125">Microsoft Defender s’approvisionne automatiquement dans les centres de données de l’Union européenne (UE) lors de l’activation via le centre de sécurité Azure.</span><span class="sxs-lookup"><span data-stu-id="13274-125">Microsoft Defender ATP automatically provisions in European Union (EU) data centers when turned on through Azure Security Center.</span></span> <span data-ttu-id="13274-126">La protection Microsoft contre les menaces est automatiquement mise en service dans le centre de données de l’UE pour les clients qui ont configuré Microsoft Defender ATP de cette manière.</span><span class="sxs-lookup"><span data-stu-id="13274-126">Microsoft Threat Protection will automatically provision in the same EU data center for customers who have provisioned Microsoft Defender ATP in this manner.</span></span> 

<span data-ttu-id="13274-127">L’emplacement du centre de données est affiché avant et après la mise en service du service dans la page Paramètres de protection contre les menaces Microsoft (**paramètres > protection contre les menaces Microsoft**).</span><span class="sxs-lookup"><span data-stu-id="13274-127">The data center location is shown before and after the service is provisioned in the settings page for Microsoft Threat Protection (**Settings > Microsoft Threat Protection**).</span></span> <span data-ttu-id="13274-128">Si vous préférez utiliser un autre emplacement pour les centres de données, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365 pour contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="13274-128">If you prefer to use another data center location, select **Need help?** in the Microsoft 365 security center to contact Microsoft support.</span></span>

## <a name="where-can-i-access-microsoft-threat-protection"></a><span data-ttu-id="13274-129">Où puis-je accéder à la protection contre les menaces Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="13274-129">Where can I access Microsoft Threat Protection?</span></span>

<span data-ttu-id="13274-130">Microsoft Threat Protection est disponible dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="13274-130">Microsoft Threat Protection is available in Microsoft 365 security center.</span></span> <span data-ttu-id="13274-131">Pour accéder au centre de sécurité, accédez à l’URL [https://security.microsoft.com](https://security.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="13274-131">To go to the security center, browse to the URL [https://security.microsoft.com](https://security.microsoft.com).</span></span>

##  <a name="what-permissions-do-i-need-to-access-microsoft-threat-protection-in-microsoft-365-security-center"></a><span data-ttu-id="13274-132">Quelles sont les autorisations nécessaires pour accéder à Microsoft Threat Protection dans le centre de sécurité Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="13274-132">What permissions do I need to access Microsoft Threat Protection in Microsoft 365 security center?</span></span>

<span data-ttu-id="13274-133">Les comptes affectés aux rôles Azure Active Directory (AD) suivants peuvent accéder aux fonctionnalités et données de la Protection Microsoft contre les menaces :</span><span class="sxs-lookup"><span data-stu-id="13274-133">Accounts assigned the following Azure Active Directory (AD) roles can access Microsoft Threat Protection functionality and data:</span></span>

- <span data-ttu-id="13274-134">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="13274-134">Global administrator</span></span>
- <span data-ttu-id="13274-135">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="13274-135">Security administrator</span></span>
- <span data-ttu-id="13274-136">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="13274-136">Security Operator</span></span>
- <span data-ttu-id="13274-137">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="13274-137">Global Reader</span></span>
- <span data-ttu-id="13274-138">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="13274-138">Security Reader</span></span>

>[!NOTE]
><span data-ttu-id="13274-139">Les paramètres de contrôle d’accès basé sur un rôle dans Microsoft Defender ATP influent sur l’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="13274-139">Role-based access control settings in Microsoft Defender ATP influence access to data.</span></span> <span data-ttu-id="13274-140">Pour plus d’informations, consultez la rubrique [gestion de l’accès à Microsoft Threat Protection](mtp-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="13274-140">For more information, read about [managing access to Microsoft Threat Protection](mtp-permissions.md).</span></span>

## <a name="what-time-zone-does-microsoft-threat-protection-default-to"></a><span data-ttu-id="13274-141">Sur quels fuseaux horaires la protection contre les menaces Microsoft est-elle par défaut ?</span><span class="sxs-lookup"><span data-stu-id="13274-141">What time zone does Microsoft Threat Protection default to?</span></span>
<span data-ttu-id="13274-142">Par défaut, Microsoft Threat Protection affiche des informations d’heure dans le fuseau horaire UTC.</span><span class="sxs-lookup"><span data-stu-id="13274-142">By default, Microsoft Threat Protection displays time information in the UTC time zone.</span></span> <span data-ttu-id="13274-143">Vous pouvez modifier ce paramètre pour utiliser votre fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="13274-143">You can change this setting to use your local time zone.</span></span> [<span data-ttu-id="13274-144">En savoir plus sur la définition du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="13274-144">Learn about setting the time zone</span></span>](mtp-time-zone.md)

## <a name="how-can-i-learn-about-new-microsoft-threat-protection-feature-and-ui-updates"></a><span data-ttu-id="13274-145">Comment puis-je obtenir des informations sur la nouvelle fonctionnalité de protection contre les menaces Microsoft et les mises à jour de l’interface utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="13274-145">How can I learn about new Microsoft Threat Protection feature and UI updates?</span></span>

<span data-ttu-id="13274-146">Microsoft fournit régulièrement des informations par le biais des différents canaux, notamment :</span><span class="sxs-lookup"><span data-stu-id="13274-146">Microsoft regularly provides information through the various channels, including:</span></span>

- <span data-ttu-id="13274-147">[Centre de messages](../../admin/manage/message-center.md) dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="13274-147">The [message center](../../admin/manage/message-center.md) in Microsoft 365 admin center</span></span>
- <span data-ttu-id="13274-148">Blogposts dans la [communauté technique de conformité des & de sécurité Microsoft 365](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/bg-p/securityprivacycompliance)</span><span class="sxs-lookup"><span data-stu-id="13274-148">Blogposts in the [Microsoft 365 security & compliance tech community](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/bg-p/securityprivacycompliance)</span></span>

<span data-ttu-id="13274-149">Obtenez les dernières expériences disponibles sur le public en activant l' [aperçu des fonctionnalités](preview.md).</span><span class="sxs-lookup"><span data-stu-id="13274-149">Get the latest publicly available experiences by turning on [preview features](preview.md).</span></span>

## <a name="is-microsoft-threat-protection-available-for-us-government-community-cloud-gcc-or-gcc-high"></a><span data-ttu-id="13274-150">La Protection Microsoft contre les menaces est-elle disponible pour cloud de la communauté pour le service public des États-Unis (GCC) ou GCC High ?</span><span class="sxs-lookup"><span data-stu-id="13274-150">Is Microsoft Threat Protection available for US Government Community Cloud (GCC) or GCC High?</span></span>
<span data-ttu-id="13274-151">Il n’est pas disponible pour le moment.</span><span class="sxs-lookup"><span data-stu-id="13274-151">At the moment, it is not available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13274-152">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="13274-152">Related topics</span></span>

- [<span data-ttu-id="13274-153">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="13274-153">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- <span data-ttu-id="13274-154">[Activez la protection contre les menaces Microsoft](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="13274-154">[Turn on Microsoft Threat Protection](mtp-enable.md).</span></span>
- [<span data-ttu-id="13274-155">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="13274-155">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="13274-156">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="13274-156">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="13274-157">Activer les fonctionnalités d’aperçu</span><span class="sxs-lookup"><span data-stu-id="13274-157">Turn on preview features</span></span>](preview.md)
