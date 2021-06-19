---
title: Résoudre les problèmes Microsoft 365 Defender service
description: Trouver des solutions et des solutions de contournement pour les problèmes Microsoft 365 Defender connus
keywords: résoudre Microsoft 365 Defender, résoudre les problèmes, Microsoft Defender pour l’identité, problèmes, module add-on, page de paramètres
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 7891d61de7581a896a6599004eae91a4e47e1581
ms.sourcegitcommit: c70067b4ef9c6f8f04aca68c35bb5141857c4e4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53029944"
---
# <a name="troubleshoot-microsoft-365-defender-service-issues"></a><span data-ttu-id="aea21-104">Résoudre les problèmes Microsoft 365 Defender service</span><span class="sxs-lookup"><span data-stu-id="aea21-104">Troubleshoot Microsoft 365 Defender service issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="aea21-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="aea21-105">**Applies to:**</span></span>
- <span data-ttu-id="aea21-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="aea21-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="aea21-107">Cette section traite des problèmes qui peuvent survenir lorsque vous utilisez le service Microsoft 365 Defender service.</span><span class="sxs-lookup"><span data-stu-id="aea21-107">This section addresses issues that might arise as you use the Microsoft 365 Defender service.</span></span>

## <a name="i-dont-see-microsoft-365-defender-content"></a><span data-ttu-id="aea21-108">Je ne vois pas Microsoft 365 Defender contenu</span><span class="sxs-lookup"><span data-stu-id="aea21-108">I don't see Microsoft 365 Defender content</span></span>

<span data-ttu-id="aea21-109">Si vous ne voyez pas de fonctionnalités dans le volet de navigation, telles que les incidents, le centre de gestion des actions ou le hunting dans votre portail, vous devez vérifier que votre client dispose des licences appropriées.</span><span class="sxs-lookup"><span data-stu-id="aea21-109">If you don't see capabilities on the navigation pane such as the Incidents, Action center, or Hunting in your portal, you'll need to verify that your tenant has the appropriate licenses.</span></span>

<span data-ttu-id="aea21-110">Si vous souhaitez en savoir plus, consultez la page[Conditions préalables](prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="aea21-110">For more information, see [Prerequisites](prerequisites.md).</span></span>

## <a name="microsoft-defender-for-identity-alerts-are-not-showing-up-in-the-microsoft-365-defender-incidents"></a><span data-ttu-id="aea21-111">Les alertes Microsoft Defender pour l’identité ne s’affichent pas dans Microsoft 365 Defender incidents</span><span class="sxs-lookup"><span data-stu-id="aea21-111">Microsoft Defender for Identity alerts are not showing up in the Microsoft 365 Defender incidents</span></span>

<span data-ttu-id="aea21-112">Si Vous avez déployé Microsoft Defender pour l’identité dans votre environnement, mais que vous ne voyez pas les alertes Defender for Identity dans le cadre des incidents Microsoft 365 Defender, vous devez vous assurer que l’intégration de Microsoft Cloud App Security et defender pour l’identité est activée.</span><span class="sxs-lookup"><span data-stu-id="aea21-112">If you have Microsoft Defender for Identity deployed in your environment but you're not seeing Defender for Identity alerts as part of Microsoft 365 Defender incidents, you'll need to ensure that the Microsoft Cloud App Security and Defender for Identity integration is enabled.</span></span>

<span data-ttu-id="aea21-113">Pour plus d’informations, [voir Microsoft Defender pour l’intégration de l’identité.](/cloud-app-security/mdi-integration)</span><span class="sxs-lookup"><span data-stu-id="aea21-113">For more information, see [Microsoft Defender for Identity integration](/cloud-app-security/mdi-integration).</span></span>

## <a name="where-is-the-settings-page-for-turning-on-the-service"></a><span data-ttu-id="aea21-114">Où se trouve la page des paramètres pour l’ment du service ?</span><span class="sxs-lookup"><span data-stu-id="aea21-114">Where is the settings page for turning on the service?</span></span>

<span data-ttu-id="aea21-115">Pour activer la Microsoft 365 Defender, accédez **Paramètres** à partir du volet de navigation dans le centre Microsoft 365 de sécurité.</span><span class="sxs-lookup"><span data-stu-id="aea21-115">To turn on Microsoft 365 Defender, access **Settings** from the navigation pane in the Microsoft 365 security center.</span></span> <span data-ttu-id="aea21-116">Cet élément de navigation n’est visible que si vous avez les autorisations et [licences requises.](m365d-enable.md#check-license-eligibility-and-required-permissions)</span><span class="sxs-lookup"><span data-stu-id="aea21-116">This navigation item is visible only if you have the [prerequisite permissions and licenses](m365d-enable.md#check-license-eligibility-and-required-permissions).</span></span>

## <a name="how-do-i-create-an-exception-for-my-fileurl"></a><span data-ttu-id="aea21-117">Comment créer une exception pour mon fichier/URL ?</span><span class="sxs-lookup"><span data-stu-id="aea21-117">How do I create an exception for my file/URL?</span></span>

<span data-ttu-id="aea21-118">Un faux positif est un fichier ou une URL détecté comme malveillant, mais qui n’est pas une menace.</span><span class="sxs-lookup"><span data-stu-id="aea21-118">A false positive is a file or URL that is detected as malicious but is not a threat.</span></span> <span data-ttu-id="aea21-119">Vous pouvez créer des indicateurs et définir des exclusions pour débloquer et autoriser certains fichiers/URL.</span><span class="sxs-lookup"><span data-stu-id="aea21-119">You can create indicators and define exclusions to unblock and allow certain files/URLs.</span></span> <span data-ttu-id="aea21-120">Voir [Adresse faux positifs/négatifs dans Defender pour le point de terminaison.](/microsoft-365/security/defender-endpoint/defender-endpoint-false-positives-negatives)</span><span class="sxs-lookup"><span data-stu-id="aea21-120">See [Address false positives/negatives in Defender for Endpoint](/microsoft-365/security/defender-endpoint/defender-endpoint-false-positives-negatives).</span></span>
