---
title: Détecter les problèmes liés au service de Protection Microsoft contre les menaces
description: Trouver des solutions et contourner les problèmes connus de la Protection Microsoft contre les menaces
keywords: résolution des problèmes liés à la protection contre les menaces Microsoft, résolution des problèmes, Azure ATP, problèmes, module complémentaire, page Paramètres
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
ms.openlocfilehash: bbc7d5d434765b94b0b2707605be2edfbbc8e423
ms.sourcegitcommit: 2913fd74ad5086c7cac6388447285be9aa5a8e44
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/01/2020
ms.locfileid: "41661980"
---
# <a name="troubleshoot-microsoft-threat-protection-service-issues"></a><span data-ttu-id="22719-104">Détecter les problèmes liés au service de Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="22719-104">Troubleshoot Microsoft Threat Protection service issues</span></span>

<span data-ttu-id="22719-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="22719-105">**Applies to:**</span></span>
- <span data-ttu-id="22719-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="22719-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="22719-107">Cette section traite des problèmes qui peuvent survenir lorsque vous utilisez le service Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="22719-107">This section addresses issues that might arise as you use the Microsoft Threat Protection service.</span></span>


## <a name="i-dont-see-microsoft-threat-protection-content"></a><span data-ttu-id="22719-108">Je ne vois pas le contenu de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="22719-108">I don't see Microsoft Threat Protection content</span></span>
<span data-ttu-id="22719-109">Si vous ne voyez pas les fonctionnalités dans le volet de navigation, telles que les incidents, le centre de maintenance ou la chasse dans votre portail, vous devez vérifier que votre client dispose des licences appropriées.</span><span class="sxs-lookup"><span data-stu-id="22719-109">If you don't see capabilities on the navigation pane such as the Incidents, Action Center, or Hunting in your portal, you'll need to verify that your tenant has the appropriate licenses.</span></span> 

<span data-ttu-id="22719-110">Si vous souhaitez en savoir plus, consultez[conditions préalables](prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="22719-110">For more information, see [Prerequisites](prerequisites.md).</span></span>

## <a name="azure-atp-alerts-are-not-showing-up-in-the-microsoft-threat-protection-incidents"></a><span data-ttu-id="22719-111">Les alertes Azure ATP n’apparaissent pas dans les incidents de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="22719-111">Azure ATP alerts are not showing up in the Microsoft Threat Protection incidents</span></span>
<span data-ttu-id="22719-112">Si Azure ATP est déployé dans votre environnement, mais que vous ne voyez pas d’alertes Azure ATP dans le cadre des incidents de Protection Microsoft contre les menaces, vous devez vous assurer que les applications Microsoft Cloud App Security et Azure ATP sont activées.</span><span class="sxs-lookup"><span data-stu-id="22719-112">If you have Azure ATP deployed in your environment but you're not seeing Azure ATP alerts as part of Microsoft Threat Protection incidents, you'll need to ensure that the Microsoft Cloud App Security and Azure ATP integration is enabled.</span></span> 

<span data-ttu-id="22719-113">Pour plus d’informations, consultez [Intégration Azure ATP](https://docs.microsoft.com/cloud-app-security/aatp-integration).</span><span class="sxs-lookup"><span data-stu-id="22719-113">For more information, see [Azure ATP integration](https://docs.microsoft.com/cloud-app-security/aatp-integration).</span></span>

## <a name="is-microsoft-threat-protection-available-for-us-government-community-cloud-gcc-or-gcc-high"></a><span data-ttu-id="22719-114">La Protection Microsoft contre les menaces est-elle disponible pour cloud de la communauté pour le service public des États-Unis (GCC) ou GCC High ?</span><span class="sxs-lookup"><span data-stu-id="22719-114">Is Microsoft Threat Protection available for US Government Community Cloud (GCC) or GCC High?</span></span>
<span data-ttu-id="22719-115">Il n’est pas disponible pour le moment.</span><span class="sxs-lookup"><span data-stu-id="22719-115">At the moment, it is not available.</span></span>

## <a name="where-is-the-settings-page-for-turning-the-service-on"></a><span data-ttu-id="22719-116">Où se trouve la page Paramètres pour activer le service ?</span><span class="sxs-lookup"><span data-stu-id="22719-116">Where is the settings page for turning the service on?</span></span>
<span data-ttu-id="22719-117">Pour activer Microsoft Threat Protection, accédez aux **paramètres** à partir du volet de navigation dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="22719-117">To turn on Microsoft Threat Protection, access **Settings** from the navigation pane in the Microsoft 365 security center.</span></span> <span data-ttu-id="22719-118">Cet élément de navigation n’est visible que si vous disposez des [autorisations et des licences prérequises](mtp-enable.md#check-license-eligibility-and-required-permissions).</span><span class="sxs-lookup"><span data-stu-id="22719-118">This navigation item is visible only if you have the [prerequisite permissions and licenses](mtp-enable.md#check-license-eligibility-and-required-permissions).</span></span>

## <a name="can-i-use-an-add-on-instead-of-the-required-e5-licenses"></a><span data-ttu-id="22719-119">Puis-je utiliser un module complémentaire au lieu des licences E5 requises ?</span><span class="sxs-lookup"><span data-stu-id="22719-119">Can I use an add-on instead of the required E5 licenses?</span></span>
<span data-ttu-id="22719-120">Il n’existe actuellement aucun module complémentaire pour la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22719-120">There are currently no add-ons for Microsoft Threat Protection.</span></span> [<span data-ttu-id="22719-121">Consulter les conditions requises en matière de licences</span><span class="sxs-lookup"><span data-stu-id="22719-121">See licensing requirements</span></span>](prerequisites.md) 

