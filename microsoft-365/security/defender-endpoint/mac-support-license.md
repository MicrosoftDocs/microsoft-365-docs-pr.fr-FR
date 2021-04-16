---
title: Résoudre les problèmes de licence pour Microsoft Defender pour Endpoint pour Mac
description: Résolution des problèmes de licence dans Microsoft Defender pour Point de terminaison pour Mac.
keywords: microsoft, defender, atp, mac, performances
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
ms.openlocfilehash: 3fb351d9ce8e9beef812e6aaa7d463161a6af8df
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51862186"
---
# <a name="troubleshoot-license-issues-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="16f68-104">Résoudre les problèmes de licence pour Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="16f68-104">Troubleshoot license issues for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="16f68-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="16f68-105">**Applies to:**</span></span>

- [<span data-ttu-id="16f68-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="16f68-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)
- [<span data-ttu-id="16f68-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="16f68-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="16f68-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="16f68-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="16f68-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="16f68-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="16f68-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="16f68-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="16f68-111">Pendant que vous êtes en cours d'utilisation de Microsoft Defender pour point de terminaison sur [macOS](microsoft-defender-endpoint-mac.md) et les tests de déploiement manuel ou d'une preuve de concept, vous pouvez obtenir l'erreur suivante : [](mac-install-manually.md)</span><span class="sxs-lookup"><span data-stu-id="16f68-111">While you are going through [Microsoft Defender for Endpoint on macOS](microsoft-defender-endpoint-mac.md) and [Manual deployment](mac-install-manually.md) testing or a Proof Of Concept (PoC), you might get the following error:</span></span>

![Image de l'erreur de licence](images/no-license-found.png)

<span data-ttu-id="16f68-113">**Message:**</span><span class="sxs-lookup"><span data-stu-id="16f68-113">**Message:**</span></span> 

<span data-ttu-id="16f68-114">Aucune licence trouvée</span><span class="sxs-lookup"><span data-stu-id="16f68-114">No license found</span></span>

<span data-ttu-id="16f68-115">Il semble que votre organisation n'a pas de licence pour l'abonnement Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="16f68-115">Looks like your organization does not have a license for Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="16f68-116">Contactez votre administrateur pour obtenir de l'aide.</span><span class="sxs-lookup"><span data-stu-id="16f68-116">Contact your administrator for help.</span></span>

<span data-ttu-id="16f68-117">**Cause :**</span><span class="sxs-lookup"><span data-stu-id="16f68-117">**Cause:**</span></span> 

<span data-ttu-id="16f68-118">Vous avez déployé et/ou installé microsoft Defender pour le point de terminaison sur le package macOS (« Télécharger le package d'installation ») mais vous avez peut-être exécuté le script de configuration (« Télécharger le package d'intégration »).</span><span class="sxs-lookup"><span data-stu-id="16f68-118">You deployed and/or installed the Microsoft Defender for Endpoint on macOS package ("Download installation package") but you might have run the configuration script ("Download onboarding package").</span></span>

<span data-ttu-id="16f68-119">**Solution :**</span><span class="sxs-lookup"><span data-stu-id="16f68-119">**Solution:**</span></span>

<span data-ttu-id="16f68-120">Suivez les instructions MicrosoftDefenderATPOnboardingMacOs.py documentées ici : [Configuration du client](mac-install-manually.md#client-configuration)</span><span class="sxs-lookup"><span data-stu-id="16f68-120">Follow the MicrosoftDefenderATPOnboardingMacOs.py instructions documented here: [Client configuration](mac-install-manually.md#client-configuration)</span></span>

