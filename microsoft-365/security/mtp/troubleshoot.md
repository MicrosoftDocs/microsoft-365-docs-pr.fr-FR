---
title: Résoudre les problèmes de service Microsoft 365 Defender
description: Trouver des solutions et contourner les problèmes connus de Microsoft 365 Defender
keywords: résoudre les problèmes de protection Microsoft contre les menaces, dépannage, Azure ATP, problèmes, module supplémentaire, page de paramètres
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: d01912532ad2a00abbecee0d0a337be7baf87017
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918665"
---
# <a name="troubleshoot-microsoft-365-defender-service-issues"></a><span data-ttu-id="9e019-104">Résoudre les problèmes de service Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9e019-104">Troubleshoot Microsoft 365 Defender service issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="9e019-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9e019-105">**Applies to:**</span></span>
- <span data-ttu-id="9e019-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9e019-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="9e019-107">Cette section traite des problèmes qui peuvent survenir lorsque vous utilisez le service Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="9e019-107">This section addresses issues that might arise as you use the Microsoft 365 Defender service.</span></span>

## <a name="i-dont-see-microsoft-365-defender-content"></a><span data-ttu-id="9e019-108">Je ne vois pas le contenu De Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9e019-108">I don't see Microsoft 365 Defender content</span></span>

<span data-ttu-id="9e019-109">Si vous ne voyez pas de fonctionnalités dans le volet de navigation, telles que les incidents, le centre de action ou le hunting dans votre portail, vous devez vérifier que votre client dispose des licences appropriées.</span><span class="sxs-lookup"><span data-stu-id="9e019-109">If you don't see capabilities on the navigation pane such as the Incidents, Action Center, or Hunting in your portal, you'll need to verify that your tenant has the appropriate licenses.</span></span>

<span data-ttu-id="9e019-110">Si vous souhaitez en savoir plus, consultez la page[Conditions préalables](prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9e019-110">For more information, see [Prerequisites](prerequisites.md).</span></span>

## <a name="microsoft-defender-for-identity-alerts-are-not-showing-up-in-the-microsoft-365-defender-incidents"></a><span data-ttu-id="9e019-111">Les alertes Microsoft Defender pour l’identité ne s’affichent pas dans les incidents Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9e019-111">Microsoft Defender for Identity alerts are not showing up in the Microsoft 365 Defender incidents</span></span>

<span data-ttu-id="9e019-112">Si Vous avez déployé Microsoft Defender pour l’identité dans votre environnement, mais que vous ne voyez pas les alertes Defender pour l’identité dans le cadre des incidents Microsoft 365 Defender, vous devez vous assurer que l’intégration de Microsoft Cloud App Security et Defender for Identity est activée.</span><span class="sxs-lookup"><span data-stu-id="9e019-112">If you have Microsoft Defender for Identity deployed in your environment but you're not seeing Defender for Identity alerts as part of Microsoft 365 Defender incidents, you'll need to ensure that the Microsoft Cloud App Security and Defender for Identity integration is enabled.</span></span>

<span data-ttu-id="9e019-113">Pour plus d’informations, [voir Microsoft Defender pour l’intégration de l’identité.](/cloud-app-security/mdi-integration)</span><span class="sxs-lookup"><span data-stu-id="9e019-113">For more information, see [Microsoft Defender for Identity integration](/cloud-app-security/mdi-integration).</span></span>

## <a name="where-is-the-settings-page-for-turning-the-service-on"></a><span data-ttu-id="9e019-114">Où se trouve la page de paramètres pour l’ment du service ?</span><span class="sxs-lookup"><span data-stu-id="9e019-114">Where is the settings page for turning the service on?</span></span>

<span data-ttu-id="9e019-115">Pour activer Microsoft 365 Defender, accédez aux **Paramètres** à partir du volet de navigation du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9e019-115">To turn on Microsoft 365 Defender, access **Settings** from the navigation pane in the Microsoft 365 security center.</span></span> <span data-ttu-id="9e019-116">Cet élément de navigation n’est visible que si vous avez les autorisations et [licences requises.](mtp-enable.md#check-license-eligibility-and-required-permissions)</span><span class="sxs-lookup"><span data-stu-id="9e019-116">This navigation item is visible only if you have the [prerequisite permissions and licenses](mtp-enable.md#check-license-eligibility-and-required-permissions).</span></span>