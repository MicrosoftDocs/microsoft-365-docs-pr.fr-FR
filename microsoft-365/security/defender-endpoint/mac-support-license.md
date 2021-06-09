---
title: Résoudre les problèmes de licence pour Microsoft Defender pour endpoint sur Mac
description: Résolution des problèmes de licence dans Microsoft Defender pour point de terminaison sur Mac.
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, mac, performances
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 1f8428c2995eec2dece290049eda67a3683b4c1e
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52244979"
---
# <a name="troubleshoot-license-issues-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="1f057-104">Résoudre les problèmes de licence pour Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="1f057-104">Troubleshoot license issues for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="1f057-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1f057-105">**Applies to:**</span></span>

- [<span data-ttu-id="1f057-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="1f057-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="1f057-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1f057-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1f057-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1f057-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1f057-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1f057-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1f057-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1f057-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="1f057-111">Pendant que vous êtes en cours d’utilisation de Microsoft Defender pour point de terminaison sur [macOS](microsoft-defender-endpoint-mac.md) et les tests de déploiement manuel ou d’une preuve de concept, vous pouvez obtenir l’erreur suivante : [](mac-install-manually.md)</span><span class="sxs-lookup"><span data-stu-id="1f057-111">While you are going through [Microsoft Defender for Endpoint on macOS](microsoft-defender-endpoint-mac.md) and [Manual deployment](mac-install-manually.md) testing or a Proof Of Concept (PoC), you might get the following error:</span></span>

![Image de l’erreur de licence](images/no-license-found.png)

<span data-ttu-id="1f057-113">**Message:**</span><span class="sxs-lookup"><span data-stu-id="1f057-113">**Message:**</span></span> 

<span data-ttu-id="1f057-114">Aucune licence trouvée</span><span class="sxs-lookup"><span data-stu-id="1f057-114">No license found</span></span>

<span data-ttu-id="1f057-115">Il semble que votre organisation ne soit pas titulaire d’une licence Microsoft 365 Entreprise abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f057-115">Looks like your organization does not have a license for Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="1f057-116">Contactez votre administrateur pour obtenir de l'aide.</span><span class="sxs-lookup"><span data-stu-id="1f057-116">Contact your administrator for help.</span></span>

<span data-ttu-id="1f057-117">**Cause :**</span><span class="sxs-lookup"><span data-stu-id="1f057-117">**Cause:**</span></span> 

<span data-ttu-id="1f057-118">Vous avez déployé et/ou installé le package Microsoft Defender for Endpoint pour macOS (« Télécharger le package d’installation ») mais vous avez peut-être exécuté le script de configuration (« Télécharger le package d’intégration ») ou vous n’avez pas attribué de licence à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f057-118">You deployed and/or installed the Microsoft Defender for Endpoint for macOS package ("Download installation package"), but you might have run the configuration script ("Download onboarding package"), or you have not assigned a license to the user.</span></span>

<span data-ttu-id="1f057-119">**Solution :**</span><span class="sxs-lookup"><span data-stu-id="1f057-119">**Solution:**</span></span>

<span data-ttu-id="1f057-120">Suivez les instructions MicrosoftDefenderATPOnboardingMacOs.py documentées ici : [Configuration du client](mac-install-manually.md#client-configuration)</span><span class="sxs-lookup"><span data-stu-id="1f057-120">Follow the MicrosoftDefenderATPOnboardingMacOs.py instructions documented here: [Client configuration](mac-install-manually.md#client-configuration)</span></span>
