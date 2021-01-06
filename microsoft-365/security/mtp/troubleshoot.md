---
title: Résoudre les problèmes liés au service Microsoft 365 Defender
description: Trouver des solutions et contourner vers des problèmes Microsoft 365 Defender connus
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
ms.openlocfilehash: b7b6ea55d084c114b79dfee0e061b09c8ede8632
ms.sourcegitcommit: 222fb7fe2b26dde3d8591b61cc02113d6135012c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49760457"
---
# <a name="troubleshoot-microsoft-365-defender-service-issues"></a><span data-ttu-id="e782f-104">Résoudre les problèmes liés au service Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e782f-104">Troubleshoot Microsoft 365 Defender service issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="e782f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e782f-105">**Applies to:**</span></span>
- <span data-ttu-id="e782f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e782f-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="e782f-107">Cette section traite des problèmes qui peuvent survenir lorsque vous utilisez le service Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="e782f-107">This section addresses issues that might arise as you use the Microsoft 365 Defender service.</span></span>

## <a name="i-dont-see-microsoft-365-defender-content"></a><span data-ttu-id="e782f-108">Je ne vois pas le contenu de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e782f-108">I don't see Microsoft 365 Defender content</span></span>

<span data-ttu-id="e782f-109">Si vous ne voyez pas les fonctionnalités dans le volet de navigation, telles que les incidents, le centre de maintenance ou la chasse dans votre portail, vous devez vérifier que votre client dispose des licences appropriées.</span><span class="sxs-lookup"><span data-stu-id="e782f-109">If you don't see capabilities on the navigation pane such as the Incidents, Action Center, or Hunting in your portal, you'll need to verify that your tenant has the appropriate licenses.</span></span>

<span data-ttu-id="e782f-110">Si vous souhaitez en savoir plus, consultez[conditions préalables](prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="e782f-110">For more information, see [Prerequisites](prerequisites.md).</span></span>

## <a name="microsoft-defender-for-identity-alerts-are-not-showing-up-in-the-microsoft-365-defender-incidents"></a><span data-ttu-id="e782f-111">Microsoft Defender pour les alertes d’identité ne s’affiche pas dans les incidents Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e782f-111">Microsoft Defender for Identity alerts are not showing up in the Microsoft 365 Defender incidents</span></span>

<span data-ttu-id="e782f-112">Si vous avez Microsoft Defender pour l’identité déployée dans votre environnement, mais que vous ne voyez pas Defender pour les alertes d’identité dans le cadre des incidents Microsoft 365 Defender, vous devez vous assurer que la sécurité de l’application Cloud de Microsoft et l’intégration des identités sont activées.</span><span class="sxs-lookup"><span data-stu-id="e782f-112">If you have Microsoft Defender for Identity deployed in your environment but you're not seeing Defender for Identity alerts as part of Microsoft 365 Defender incidents, you'll need to ensure that the Microsoft Cloud App Security and Defender for Identity integration is enabled.</span></span>

<span data-ttu-id="e782f-113">Pour plus d’informations, consultez la rubrique [Microsoft Defender for Identity Integration](https://docs.microsoft.com/cloud-app-security/mdi-integration).</span><span class="sxs-lookup"><span data-stu-id="e782f-113">For more information, see [Microsoft Defender for Identity integration](https://docs.microsoft.com/cloud-app-security/mdi-integration).</span></span>

## <a name="where-is-the-settings-page-for-turning-the-service-on"></a><span data-ttu-id="e782f-114">Où se trouve la page Paramètres pour activer le service ?</span><span class="sxs-lookup"><span data-stu-id="e782f-114">Where is the settings page for turning the service on?</span></span>

<span data-ttu-id="e782f-115">Pour activer Microsoft 365 Defender, accédez aux **paramètres** à partir du volet de navigation dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e782f-115">To turn on Microsoft 365 Defender, access **Settings** from the navigation pane in the Microsoft 365 security center.</span></span> <span data-ttu-id="e782f-116">Cet élément de navigation n’est visible que si vous disposez des [autorisations et des licences prérequises](mtp-enable.md#check-license-eligibility-and-required-permissions).</span><span class="sxs-lookup"><span data-stu-id="e782f-116">This navigation item is visible only if you have the [prerequisite permissions and licenses](mtp-enable.md#check-license-eligibility-and-required-permissions).</span></span>
